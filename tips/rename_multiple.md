## Rename Multiple file dengan perintah mv

Perintah `mv` hanya dapat mengganti nama satu file pada satu waktu.
Tetapi dapat digunakan bersamaan dengan perintah lain seperti `find` atau `inside`, perintah `for` atau `while` untuk mengganti nama beberapa file

contoh:

```
for f in *.html; do 
    mv -- "$f" "${f%.html}.php"
done
```

Penjelsan kode baris:
1. Baris pertama membuat list file yang berakhiran dengan .html.
1. Baris kedua akan melakukan rename pada tiap-tiap file dengan menggantikan `.html` dengan `.php`. bagian `${f%.html}` menggunakan ekspansi parameter untuk menghapus bagian `.html`
1. `done` digunakan sebagai akhir loop.
