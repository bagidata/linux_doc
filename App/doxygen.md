## Install Doxygen

```
sudo apt install doxygen
```

Untuk generate graph doxygen membutuhkan `graphviz`.
Install graphviz

```
sudo apt install graphviz
```

jika tidak berhasil coba dengan cara ini

```
sudo add-apt-repository universe
sudo apt update
sudo apt install graphviz
```

Memastikan bahwa doxygen sudah berhasil di install

```
$ which doxygen
/usr/bin/doxygen

$ doxygen --version
1.8.7
```

## Membuat file konfigurasi doxygen

```
doxygen -s -g nama_konfigurasi
```

Jika tidak mengiginkan ada komentar di file konfig hilangkan `-s`

```
doxygen -g nama_konfigurasi
```

Jika `nama_konfigurasi` dihilangkan atau tidak ada 
maka secara default akan dibuat file dengan nama `Doxyfile`

## Edit file konfigurasi

Biasanya file konfigurasi yang perlu di edit adalah
berikut contoh file konfigurasi

```
OUTPUT_DIRECTORY       = /lokasi/file/output/
OPTIMIZE_OUTPUT_FOR_C  = YES
INPUT                  = /lokasi/sumber/source_code/
FILE_PATTERNS          = *.c *.h
RECURSIVE              = YES
EXCLUDE_PATTERNS       = */Documentation/* */firmware/* */samples/* */scripts/* */tools/* */usr/* */virt/*
GENERATE_LATEX         = NO
DOT_NUM_THREADS        = 2
```

## Menjalankan Doxygen

```
doxygen nama_konfigurasi
```

Selesai
