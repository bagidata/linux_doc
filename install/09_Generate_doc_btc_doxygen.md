## Generate Document Bitcoin dengan Doxygen

### Pesiapan

1. Install Doxygen :

```
sudo apt install doxygen
```

2. Install Graphviz :

```
sudo apt install graphviz
```

jika tidak berhasil coba dengan cara ini

```
sudo add-apt-repository universe
sudo apt update
sudo apt install graphviz
```

### Generate src bitcoin

Buat direkroti `doxygen` di `/doc/doxygen`

Kerjakan perintah berikut :
```
doxygen doc/Doxyfile.in
```

Selesai.
