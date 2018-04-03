# Hybrid Graphics

## Pendahuluan

Beberapa laptop dilengkapi dengan dua kartu grafis: satu untuk digunakan dalam aplikasi yang membutuhkan banyak daya komputasi seperti game, yang disebut _discrete GPU_ , dan yang kurang kuat, tetapi menghemat energi, yang disebut _integrated GPU_. _Integrated GPU_ sering ditanamkan pada CPU. Konsep ini disebut Hybrid Graphics.

Versi terbaru dari kernel Linux dapat mendukung grafis hibrida. Jika perangkat Anda memiliki pemilih perangkat keras, Anda dapat beralih dari satu GPU ke GPU lainnya melalui bendera **vga_switcheroo** .


> Metode ini tidak didukung oleh semua mesin dan hanya berfungsi jika Anda menggunakan driver open source ( [Nouveau](https://wiki.ubuntu-it.org/Hardware/Video/Nvidia/DriverNouveau) , [Radeon](https://wiki.ubuntu-it.org/Hardware/Video/Amd/Radeon) ) .

## Mengaktifkan vga_switcheroo
Untuk memverifikasi bahwa kernel dikompilasi dengan opsi yang benar, Anda dapat memeriksa file `config-*` di direktori `/boot` . Ketik terminal :

`grep -i switcheroo/boot/config-*` 

Mekanisme **vga_switcheroo** hanya akan aktif ketika kernel dimulai dengan opsi:

`"modeset = 1"`

dan / atau dengan opsi:

`"Nomodeset"`

absen.

Untuk memeriksa apakah **vga_switcheroo** diaktifkan, cari file `switch` dengan mengetik:

`sudo ls -l /sys/kernel/debug/vgaswitcheroo/switch`

jika file ditemukan maka **vga_switcheroo** diaktifkan.

Penggunaan vga_switcheroo
Setelah Anda memastikan vga_switcheroo tersedia, Anda dapat menggunakan opsi ini untuk mengubah GPU:

Untuk mengaktifkan GPU yang terputus (tetapi bukan output switching):

echo ON> /sys/kernel/debug/vgaswitcheroo/switch
Untuk menghubungkan kartu grafis terintegrasi dengan output:

echo IGD> /sys/kernel/debug/vgaswitcheroo/switch 
Untuk menghubungkan kartu grafis khusus dengan output:

echo DIS> /sys/kernel/debug/vgaswitcheroo/switch
Untuk menonaktifkan kartu grafis yang saat ini terputus:

echo OFF> /sys/kernel/debug/vgaswitcheroo/switch 
Ada juga opsi tambahan yang berguna dalam sesi X-Windows:

Untuk menambahkan switch ke grafis terintegrasi yang terjadi ketika server X di sebelah reboot:

gema DIGD> /sys/kernel/debug/vgaswitcheroo/switch 
Untuk menambahkan bagian ke grafik khusus yang terjadi ketika server X di sebelah reboot:

echo DDIS> /sys/kernel/debug/vgaswitcheroo/switch 
Pantau pengaturan
Anda dapat memeriksa pengaturan yang saat ini digunakan melalui perintah:

gedit /sys/kernel/debug/vgaswitcheroo/switch
yang dapat mengembalikan output seperti ini:

0: IGD: +: Pwr: 0000: 01: 05,0
1: DIS :: Off: 0000: 02: 00.0
Tabel berikut menunjukkan arti dari simbologi yang digunakan:

Sigla

makna

IGD

menunjukkan GPU terpadu, umumnya yang kurang berfungsi

DIS

menunjukkan GPU diskrit, yang berdedikasi, yang mampu menghasilkan kinerja grafis yang superior

+

menunjukkan bahwa GPU aktif, yaitu terhubung ke output video

pwr

menunjukkan bahwa GPU dinyalakan, yaitu didukung (oleh karena itu mengkonsumsi energi)

lepas

menunjukkan bahwa GPU dimatikan, yaitu tidak lagi didukung

Skrip untuk digunakan dalam sesi X
Anda dapat membuat skrip yang berguna untuk membuat antarmuka grafis untuk memilih antara kartu grafis.

Pastikan paket gxmessage dan libnotify-bin sudah diinstal .

Unduh beberapa file di direktori / usr / share / icons dengan mengetikkan perintah di terminal :

sudo wget P / usr / share / icons / http://lh4.ggpht.com/_Dw3SC8gD9Jk/S-MGVcEfaiI/AAAAAAAAAIA/Pguy_uSeqSk/s800/hardware_down.png

sudo wget P / usr / share / icons / http://lh5.ggpht.com/_Dw3SC8gD9Jk/S-MGVSO0JbI/AAAAAAAAAIE/_mdAnW7UiCQ/s800/hardware_up.png
Buat skrip dengan mengetik:

sudo sentuh /usr/bin/switch_between_cards.sh
Buka file /usr/bin/switch_between_cards.sh dengan hak akses administratif dan dengan editor teks dan masukkan di dalamnya:
===================================================
#!/bin/bash
# "switch_between_cards.sh" script by RM, with useful changes from LoLL
# version 20101107

pci_integrated=$(lspci | grep VGA | sed -n '1p' | cut -f 1 -d " ")
pci_discrete=$(lspci | grep VGA | sed -n '2p' | cut -f 1 -d " ")

integrated=$(cat /sys/kernel/debug/vgaswitcheroo/switch | grep $pci_integrated | grep -o -P ':.:...:')
discrete=$(cat /sys/kernel/debug/vgaswitcheroo/switch | grep $pci_discrete | grep -o -P ':.:...:')

name_integrated=$(lspci | grep VGA | sed -n '1p' | sed -e "s/.* VGA compatible controller[ :]*//g" | sed -e "s/ Corporation//g" | sed -e "s/ Technologies Inc//g" | sed -e 's/\[[0-9]*\]: //g' | sed -e 's/\[[0-9:a-z]*\]//g' | sed -e 's/(rev [a-z0-9]*)//g' | sed -e "s/ Integrated Graphics Controller//g")

name_discrete=$(lspci | grep VGA | sed -n '2p' | sed -e "s/.* VGA compatible controller[ :]*//g" | sed -e "s/ Corporation//g" | sed -e "s/ Technologies Inc//g" | sed -e 's/\[[0-9]*\]: //g' | sed -e 's/\[[0-9:a-z]*\]//g' | sed -e 's/(rev [a-z0-9]*)//g' | sed -e "s/ Integrated Graphics Controller//g")

if [ "$integrated" = ":+:Pwr:" ]
then
 integrated_condition="(*) - Power ON"
elif [ "$integrated" = ": :Pwr:" ]
then
 integrated_condition="( ) - Power ON"
elif [ "$integrated" = ": :Off:" ]
then
 integrated_condition="( ) - Power OFF"
fi

if [ "$discrete" = ":+:Pwr:" ]
then
 discrete_condition="(*) - Power ON"
elif [ "$discrete" = ": :Pwr:" ]
then
 discrete_condition="( ) - Power ON"
elif [ "$discrete" = ": :Off:" ]
then
 discrete_condition="( ) - Power OFF"
fi

gxmessage -center \
          -buttons "_Cancel":1,"switch to _Integrated":101,"switch to _Discrete":102 \
          -wrap \
          -title "Choose Hybrid Graphic Card" \
"Choose Hybrid Graphic Card
=================
Integrated: $integrated_condition : $name_integrated
Discrete: $discrete_condition : $name_discrete"


whichCard=$?

case "$whichCard" in

1)
 echo "Exit"
;;
101)
 if [ "$integrated" == ":+:Pwr:" ] && [ "$discrete" == ": :Pwr:" ]
 then
  notify-send -t 5000 --icon="/usr/share/icons/hardware_down.png" "switching to $name_integrated"
  echo OFF > /sys/kernel/debug/vgaswitcheroo/switch
 elif [ "$integrated" == ": :Pwr:" ] && [ "$discrete" == ":+:Pwr:" ]
 then
  notify-send -t 5000 --icon="/usr/share/icons/hardware_down.png" "switching to $name_integrated"
  echo DIGD > /sys/kernel/debug/vgaswitcheroo/switch
  if [ "$DESKTOP_SESSION" = "openbox" ]
  then
   killall -u "$USER"
  elif [ "$DESKTOP_SESSION" = "gnome" ]
  then
   gnome-session-save --logout
  fi
 elif [ "$integrated" == ": :Off:" ] && [ "$discrete" == ":+:Pwr:" ]
 then
  notify-send -t 5000 --icon="/usr/share/icons/hardware_down.png" "switching to $name_integrated"
  echo ON > /sys/kernel/debug/vgaswitcheroo/switch
  echo DIGD > /sys/kernel/debug/vgaswitcheroo/switch
  if [ "$DESKTOP_SESSION" = "openbox" ]
  then
   killall -u "$USER"
  elif [ "$DESKTOP_SESSION" = "gnome" ]
  then
   gnome-session-save --logout
  fi
 elif [ "$integrated" == ":+:Pwr:" ] && [ "$discrete" == ": :Off:" ]
 then
  notify-send -t 5000 --icon="/usr/share/icons/hardware_down.png" "already switched to $name_integrated"  
 fi
;;
102)
 if [ "$integrated" == ":+:Pwr:" ] && [ "$discrete" == ": :Pwr:" ]
 then
  notify-send -t 5000 --icon="/usr/share/icons/hardware_up.png" "switching to $name_discrete"
  echo DDIS > /sys/kernel/debug/vgaswitcheroo/switch
  if [ "$DESKTOP_SESSION" = "openbox" ]
  then
   killall -u "$USER"
  elif [ "$DESKTOP_SESSION" = "gnome" ]
  then
   gnome-session-save --logout
  fi
 elif [ "$integrated" == ": :Pwr:" ] && [ "$discrete" == ":+:Pwr:" ]
 then
  notify-send -t 5000 --icon="/usr/share/icons/hardware_up.png" "switching to $name_discrete"
  echo OFF > /sys/kernel/debug/vgaswitcheroo/switch
 elif [ "$integrated" == ":+:Pwr:" ] && [ "$discrete" == ": :Off:" ]
 then
  notify-send -t 5000 --icon="/usr/share/icons/hardware_up.png" "switching to $name_discrete"  
  echo ON > /sys/kernel/debug/vgaswitcheroo/switch
  echo DDIS > /sys/kernel/debug/vgaswitcheroo/switch
  if [ "$DESKTOP_SESSION" = "openbox" ]
  then
   killall -u "$USER"
  elif [ "$DESKTOP_SESSION" = "gnome" ]
  then
   gnome-session-save --logout
  fi
 elif [ "$integrated" == ": :Off:" ] && [ "$discrete" == ":+:Pwr:" ]
 then
  notify-send -t 5000 --icon="/usr/share/icons/hardware_up.png" "already switched to $name_discrete"  
 fi
;;
esac
=============================================================

Simpan dan tutup file.
Pintasan keyboard
Anda dapat menetapkan pintasan keyboard ke skrip. Dalam hal ini, perlu untuk mengganti namanya dengan hak akses administratif di switch_between_cards tanpa ekstensi .sh.

Ketik jendela terminal :

sudo mv /usr/bin/switch_between_cards.sh / usr / bin / switch_between_cards
Buat file yang dapat dieksekusi dengan mengetik:

sudo chmod + x / usr / bin / switch_between_cards
Pilih Aplikasi → Personalisasi → Keyboard → Pintasan menu . Dengan mengklik tombol + , Anda dapat menetapkan kombinasi tombol seperti: Super + G atau Ctrl + Alt + G, dll. Sebagai perintah, Anda perlu memasukkan:

gksudo switch_between_cards
verifikasi
Untuk memverifikasi bahwa skrip berfungsi, ketik jendela terminal :

sudo switch_between_cards
Jika Anda telah memilih pintasan keyboard, ketikkan kombinasi tombol yang ditentukan untuk skrip dan lihat apakah itu dimulai.
Skrip untuk digunakan saat startup sistem
Pergantian kartu mungkin sesuai selama startup sistem, misalnya untuk mengaktifkan output untuk GPU yang digunakan Linux untuk query kata sandi untuk mendekripsi volume root (dan pesan boot lainnya) atau untuk menonaktifkan salah satu kartu selama boot untuk menghemat daya baterai.

Saat ini tidak ada opsi kernel untuk mengendalikan mekanisme vga_switcheroo , tetapi masih dimungkinkan untuk membuat skrip initramfs untuk mencapai hasil yang sama.

Buat skrip dengan mengetik di terminal :

sudo touch / etc / initramfs-tools / scripts / local-top / hybrid_boot_options
Buka dengan hak administrator dan dengan editor teks file / etc / initramfs-tools / scripts / local-top / hybrid_boot_options dan masuk ke dalamnya:

====================================================
#
# Standard initramfs preamble
#
prereqs()
{
:
}

case $1 in
prereqs)
        prereqs
        exit 0
        ;;
esac

# source for log_*_msg() functions, see LP: #272301
. /scripts/functions

#
# Helper functions
#
message()
{
        if [ -x /bin/plymouth ] && plymouth --ping; then
                plymouth message --text="$@"
        elif [ -p /dev/.initramfs/usplash_outfifo ] && [ -x /sbin/usplash_write ]; then
                usplash_write "TEXT-URGENT $@"
        else
                echo "$@" >&2
        fi
        return 0
}

run_switcheroo()
{
        local hybridopts
        hybridopts="$1"

        if [ -z "$hybridopts" ]; then
                return 1
        fi

        local IFS=" ,"
        for x in $hybridopts; do
                message "Switching hybrid graphics to $x"
                echo $x > /sys/kernel/debug/vgaswitcheroo/switch
        done
        return 0
}

#
# Begin real processing
#

# Do we have any kernel boot arguments?
for opt in $(cat /proc/cmdline); do
        case $opt in
        hybridopts=*)
                run_switcheroo "${opt#hybridopts=}"
                ;;
        esac
done

exit 0
======================================================

Buat skrip dieksekusi dengan mengetik:

chmod + x / etc / initramfs-tools / scripts / local-top / hybrid_boot_options
Buat file initramfs baru dengan initramfs-tools dengan mengetik:

initramfs-tools -c -k semua
Jika perintah initramfs-tools tidak berfungsi, ketik:

update-initramfs -c -k semua
Opsi boot
Pada titik ini adalah mungkin untuk menambahkan opsi boot kernel di file / etc / default / grub . Misalnya, membuka dengan hak akses administratif dan dengan editor teks file / etc / default / grub , memasukkan dalam baris:

GRUB_CMDLINE_LINUX_DEFAULT = "mode splash yang tenang = 1 hybridopts = ON, IGD, OFF"
kedua GPU diaktifkan, sakelar dibuat pada GPU terintegrasi dan akhirnya GPU khusus dimatikan.

Untuk membuat opsi diterapkan ke Grub efektif, Anda akan memerlukan perintah:

sudo update-grub 


Untuk menguji opsi selama startup, tekan tombol E di Grub dan opsi "hybridopts =" setelah simbol = untuk memasukkan / menghapus perintah yang dipisahkan koma.

Pemecahan masalah
Kipas berjalan pada kecepatan maksimum
Seperti yang dijelaskan ke alamat berikut, adalah mungkin untuk mematikan sistem ketika ada masalah di mana penggemar akan berjalan pada kecepatan maksimum jika kedua papan tidak dinyalakan.

Untuk mengatasi masalah, sebelum mematikan sistem, cukup ketik terminal :

echo ON> / sys / kernel / debug / vgaswitcheroo / switch
kecerahan
Kecerahan layar laptop saat startup mungkin sangat rendah. Jika Anda memiliki layar hampir hitam saat startup, Anda cukup menekan pintasan keyboard untuk meningkatkan kecerahan laptop Anda.

GPU default
GPU yang diaktifkan oleh BIOS selama boot mungkin tergantung pada apakah laptop terhubung ke listrik atau tidak.

Konsol FB
Melalui parameter fbcon dimungkinkan untuk memilih perangkat yang akan digunakan oleh kernel untuk fase start-up konsol. Misalnya dapat digunakan:

"fbcon = map: 1"
untuk / dev / fb1 .



Sebagai alternatif, jika Anda ingin membuat GPU dinonaktifkan kapan saja, Anda dapat membuat daftar hitam driver yang relevan, memperbarui initramfs dan kemudian menyingkirkan salah satu perangkat fb.

Sumber : https://wiki.ubuntu-it.org/Hardware/Video/GraficaIbrida/Vga_switcheroo
