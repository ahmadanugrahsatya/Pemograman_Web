---
sticker: emoji//1f915
---
# Struktur Dasar HTML 
```html
<!DOCTYPE html>
<html>
  <head>
    <title>ini adalah judul</title>
  </head>
  
  <body>
    <p>No Body</p>
  </body>
</html>
```
![hasil_html|250x500](asettt/hasil_html.jpg)
- Tag `<!DOCTYPE html>` memberitahukan web browser bahwa dokumen HTML adalah versi 5.
- Tag pembuka `<html>` menandai awal sebuah dokumen HTML sampai dengan tag penutup `</html>`.
- Tag pembuka `<head>` berisi informasi tentang halaman HTML sampai dengan tag penutup `</head>`, biasanya dalam tag head terdapat tag `<titel>` untuk memberikan informasi judul halam HTML.
- apapun tag yang berada di antara tag pembuka `<body>` sampai dengan tag penutup `</body>` akan tampil di web browser.
# Anatomi Elemen HTML
```html
<a href="https://www.google.com">Klik Goggle</a>
```
![A|250x500](asettt/a.jpg)
- Tag pembuka `<a>` tag yang menandakan awalan dan `</a>` akhir URL/link.
-  atribut `href` digunakan untuk menentukan halaman web URL/link. Contoh nilai atribut https://www.google.com.
- isi konten itu untuk masuk ke URL/link yang sudah kita buat di atribut `href` yaitu "klik google"
## Tag Pembuka dan Tag Penutup
Tag pembuka dan tag penutup adalah dua bagian dari suatu elemen dalam HTML yang digunakan untuk menentukan awal dan akhir dari elemen tersebut. Tag pembuka dimulai dengan nama elemen yang diapit oleh tanda kurung sudut ("<" dan ">"). Tag penutup serupa dengan tag pembuka, tetapi memiliki karakter garis miring tambahan ("/") sebelum nama elemennya. contoh ini, `<p>` adalah tag pembuka, dan `</p>` adalah tag penutup
## Atribut Tag
Atribut tag merujuk pada informasi tambahan yang diberikan kepada elemen HTML untuk memberikan rincian atau pengaturan tertentu. Atribut dapat ditambahkan ke sebagian besar tag HTML dan berfungsi untuk mengontrol perilaku atau tampilan elemen tersebut. Contohnya, pada tag `<a>` (hipertaut), atribut `href` digunakan untuk menentukan URL tujuan. Begitu juga, pada tag `<img>`(gambar), atribut src menunjukkan sumber gambar. 
## Isi/Konten Tag
Isi atau konten tag merujuk pada teks, elemen, atau informasi yang ditempatkan di antara tag pembuka dan tag penutup dalam markup HTML. Contoh sederhana adalah tag paragraf `<p>`, di mana isi tag tersebut adalah teks yang ingin dimuat dalam paragraf. Contoh "Ini adalah contoh isi atau konten dalam tag paragraf." adalah isi atau konten yang akan ditampilkan atau diinterpretasikan oleh browser web ketika halaman HTML di-render.
# Tag Dasar
## Heading
```html
<!DOCTYPE html>
<html>
  <head>
    <title>ini adalah judul</title>
  </head>
  
  <body>
    <h1>kata kata hari ini</h1>
    <h2>word of the day</h2>
    <h3>今日の単語</h3>
    <h4>ك4لمة اليوم</h>
    <h5>Từ trong ngày</h5>
    <h6>오늘의 단어</h6>
    <p>No Body</p>
    <p>tidak ada yang tahu</p>
    <a href="https://www.google.com">Klik Goggle</a>
  </body>
</html>
```
![H1-H6|250x500](asettt/H1-H6.jpg)
- Tag `<h1>` Digunakan untuk judul utama atau level judul tertinggi
- Tag `<h2>` Menunjukkan tingkatan judul yang lebih rendah dari `<h1>` atau subjudul
- Tag `<h3>` Menunjukkan tingkatan judul yang lebih rendah atau subjudul dari `<h2>`
- Tag `<h4>` Menunjukkan tingkatan judul yang lebih rendah atau subjudul dari `<h3>`
- Tag `<h5>` Menunjukkan tingkatan judul yang lebih rendah atau subjudul dari `<h4>`
- Tag `<h6>` Menunjukkan tingkatan judul yang lebih rendah atau subjudul dari `<h5>` 
## Paragraf
```html
<!DOCTYPE html>
<html>
  <head>
    <title>ini adalah judul</title>
  </head>
  
  <body>
    <p>nama saya</p>
    <br>
    <p><b>kelas saya</b></p>
    <hr>
    <p><u>No Body</u></p>
    <p><i>tidak ada yang tahu</i></p>
    <a href="https://www.google.com">Klik Goggle</a>
  </body>
</html>
```
![p_b_u_i_br_hr|250x500](asettt/p_b_u_i_br_hr.jpg)
- Tag `<p>`digunakan untuk menandai paragraf pada halaman web dan di akhiri `</p>`. Ini memberikan jarak antara paragraf.
- Tag `<b>` digunakan untuk membuat teks menjadi tebal (bold) dan di akhiri `</b>`.
- Tag `<u>` digunakan untuk memberi garis bawah pada teks dan di akhiri `</u>`. 
- Tag `<i>` digunakan untuk membuat teks menjadi miring (italic) dan di akhiri `</i>`.
- Tag `<br>` digunakan untuk membuat jeda baris atau perpindahan ke baris berikutnya tanpa membuat paragraf baru.
- Tag `<hr>` digunakan untuk membuat garis horizontal, yang sering digunakan pemisah visual di antara bagian-bagian pada halaman web.