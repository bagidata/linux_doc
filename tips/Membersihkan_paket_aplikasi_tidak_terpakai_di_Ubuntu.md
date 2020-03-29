## Membersihkan paket aplikasi tidak terpakai di Ubuntu

### Insttal aplikasi deborphan

```
apt-get install deborphan
```

### Jalankan Dorphan

```
deborphan
```

hasil :

```
libelf1
mktemp
libdrm-radeon1
libdrm-intel1
```

### parameter 
Parameter yang bisa dimanfaatkan untuk memperkirakan apakah ada calon – calon paket aplikasi lain di masa depan 
yang bisa dibersihkan:

```
deborphan --guess-all
```

hasil:

```
libelf1
mktemp
libapache2-mod-rpaf
libxext-dev
libdrm-radeon1
libdrm-intel1
libapache2-mod-ruid2
libapache2-mod-fcgid
```

### Menghapus paket aplikasi

```
apt-get remove libdrm-intel1
```
