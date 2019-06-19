# Menggunakan aplikasi `dd` bawaan linux untuk cloning HDD

## Create Backup dari Partisi yang ada

Partisi `/dev/sdb1` backup ke image file `/backup/sdb1.img`

```
$ dd if=/dev/sdb1 of=/backup/sdb1.img
```

## Restore Backup ke partisi lain

Restore `/backup/sdb1.img` ke partisi lain misal `/dev/sdb2`
```
$ dd if=/backup/sdb1.img of=/dev/sdb2
```

## Clone partisi

Clone partisi `/dev/sdb1` ke '/dev/sde2' tanpa membuat backup apapun.
```
$ sudo dd if=/dev/sdb1 of=/dev/sde2
```
atau
```
sudo dd if=/dev/sde1 of=/dev/sde2 bs=4096 conv=notrunc,noerror,sync
```

if (input file): /dev/sdb1
of (output file): /dev/sde2

bs=4096 :
- set ukuran blok 4096
- Ukuran ideal untuk efisiensi read/write

conv=notrunc,noerror,sync:
- notrunc – Jangan memotong data apapun
- noerror – Lanjutkan operasi dan abaikan semua error, jika tidak maka akan berhenti pada saat error.
- sync – Tulis angka nol ke disk untuk error baca ini membuat data offset tetap sinkron.

## Clone semua HDD

Clone semua data di disk `/dev/sda` beserta partisi lainnya ke disk `/dev/sdb`
```
$ dd if=/dev/sda of=/dev/sdb bs=446 count=1
```

## Backup dan Restore MBR ke Image file

Backup MBR dari `/dev/sda` ke file `/backup/backup-mbr-sda.img`
```
$ dd if=/dev/sda of=/backup/backup-mbr-sda.img bs=512 count=1
```

Restore MBR ke disk lain
```
$ dd if=/backup/backup-mbr-sda.img of=/dev/sdb bs=446 count=1
```
