E: Unable to locate package <nama-package>

Hal ini terjadi pada saat **apt-get install** tidak dapat ditemukan paket, 
paket yang ingin Anda instal tidak dapat ditemukan dalam repositori yang 
telah Anda tambahkan (yang ada di dalam /etc/apt/sources.listdan di bawah /etc/apt/sources.list.d/).

Prosedur (umum) berikut membantu untuk menyelesaikan ini:

1. Pastikan Anda telah mengaktifkan repositori Ubuntu:

Untuk mengaktifkan semua repositori ( main, universe, restricted, multiverse), gunakan perintah berikut:

```
sudo add-apt-repository main
sudo add-apt-repository universe
sudo add-apt-repository restricted
sudo add-apt-repository multiverse
```

Untuk informasi lebih lanjut. [https://help.ubuntu.com/community/Repositories/Ubuntu]

2. Untuk menemukan PPA untuk paket lainnya:

2.1 Cari paket didalam [Paket Ubuntu](http://packages.ubuntu.com/).

2.2 Untuk repositori Eksternal, Kunjungi [Ubuntu update] (http://www.ubuntuupdates.org/) dan cari dengan  layartombol. 
atau Kunjungi [AKP](http://www.ubuntuupdates.org/ppas) .

2.3 Atau Cari di [Launchpad ppa](https://launchpad.net/ubuntu/+ppas)

2.4 Temukan ppa yang tepat sesuai dengan versi rilis Ubuntu Anda.


3. Tambahkan PPA (dengan baris perintah) :

Gunakan perintah ini:

`sudo add-apt-repository ppa:<repository-name>`

Kunjungi [komunitas Ubuntu](https://help.ubuntu.com/community/Repositories/CommandLine) untuk informasi lebih lanjut.

4. Jangan lupa untuk update (pastikan Anda mengetahui perubahan Anda):

**Sangat penting untuk menjalankan perintah ini setelah mengubah repositori:**

`sudo apt-get update`

Memilih server unduhan terbaik dapat membantu mempercepat pembaruan.

5. Selanjutnya instal paket:

sudo apt-get install <package>
Lihat manajemen Paket berdasarkan commandline .

Tambahan / Kiat : Anda dapat menemukan nama-paket yang benar (yaitu nama dalam repositori) menggunakan apt-cache search <package-name>.
