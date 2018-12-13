## Melihat daftar aplikasi yang di install
`dpkg -l`

atau disa juga dengan

`apt --installed list`

## Mengambil atau backup aplikasi yang sudah terisntall

Terlebih dahulu instal aplikasi untuk re-packing paket ubuntu nama aplikasi `fakeroot`

`sudo apt-get install dpkg-repack fakeroot`

### Paket tertentu saja

```
fakeroot -u dpkg-repack `dpkg --get-selections | grep gimp | cut -f1 `
```

Contoh di atas hanya mengambil aplikasi yang mengandung kata `gimp` saja.

### Semua paket

```
fakeroot -u dpkg-repack `dpkg --get-selections | grep install | cut -f1`
```

### Beberapa paket saja

```
fakeroot -u dpkg-repack `dpkg --get-selections | grep "gimp\\|cups\\|totem" | cut -f1`
```

Pada perintah di atas akan mengambil aplikasi yang mengandung kata `gimp` `cups` dan `totem`

## Re-Install paket yang sudah di backup

`sudo dpkg -i *.deb`


