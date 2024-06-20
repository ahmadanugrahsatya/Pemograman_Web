# Materi Tailwind
## Perkenalan Kelompok
**Kelompok AFF**
- Ahmad Anugrah Satya
- Fachri Ramadhan
- Muhammad Fadhil Amir 

## Penjelasan Materi
Kami dari kelompok AFF mendapatkan materi eksplorasi css bagian Tailwind dan tujuan dari pembuatan file obsidian ini ialah untuk memberikan hasil dari kerja kelompok kami, adapun isi dari *penjelasan materi* ini akan terbagi menjadi instalasi, kostumisasi css, penggunaan component, dan responsive web. Untuk penjelasan lebih jelasnya akan di paparkan di bawah ini.
### Penjelasan Tailwind

### Instalasi Tailwindcss
1. Buatkan File Index.html
![](pemograman%20web/Tailwind/Tailwind/aset/cssss50.png)


2. Pastikan  Sudah Menginstall Tailwind CSS, Live Preview Dan Post CSS
   ![](pemograman%20web/Tailwind/Tailwind/aset/cssss51.png)

![](pemograman%20web/Tailwind/Tailwind/aset/cssss52.png)

![](pemograman%20web/Tailwind/Tailwind/aset/cssss53.png)

3. Buatkan Struktur HTML Sederhana 
![](pemograman%20web/Tailwind/Tailwind/aset/cssss54.png)

4. Masuk ke gitbash lalu ketik Kode Dibawah ini 
```
git init -y
```
![](pemograman%20web/Tailwind/Tailwind/aset/cssss55.png)



5. Lalu  Ketik install -d tailwindcss
![](pemograman%20web/Tailwind/Tailwind/aset/cssss56.png)


>[!info]- Penjelasan 
Masuk Ke Terminal Lalu Ketik `npm init -y`, `- y` ini berfungsi untuk mengisi secara otomatis yang ingin diisi dan membuat file  (package.json) 

Hasil yang tampil akan seperti berikut :
![](pemograman%20web/Tailwind/Tailwind/aset/cssss61.png)
npm  isntall -d tailwindcss berfungsi untuk menginstall tailwindcss dan juga direkomendasikan untuk menggunakan -D (Rekomendasi ini berasal dari website aslinya)


6.  Masuk ke tailwind.config.js 
![](pemograman%20web/Tailwind/Tailwind/aset/cssss58.png)
dibagian content ketik `["./public/**/*.{html,js}"]`


7. Masuk ke input.css lalu ketik kode dibawah ini
```bash
@tailwind base;
@tailwind component;
@tailwind utilities;
```
![](pemograman%20web/Tailwind/Tailwind/aset/cssss59.png)

8.  Ketik  Kode Di Bawah ini
```
npx tailwindcss -i ./src/input.css -o ./public/css/style.css --watch
```

![](pemograman%20web/Tailwind/Tailwind/aset/cssss60.png)


### Kostumisasi CSS 

#### THEME 

**Kode Program CSS**
```css
extend: {
      fontFamily: {
        'body': ['Roboto', 'sans-serif'],
        'heading': ['Montserrat', 'sans-serif'],
      },
      spacing: {
        '72': '18rem',
        '84': '21rem',
      },
      backgroundImage:{
        "anime" : "url(../aset/anime_1.png)"
      },
    }
```

>[!info] 
> - `fontFamily`: Bagian ini digunakan untuk menentukan jenis font yang akan digunakan dalam proyek. Kita mendefinisikan dua jenis font: `body` dan `heading`, masing-masing memiliki daftar font dengan preferensi tertentu. Jika font pertama tidak tersedia, font kedua dalam daftar akan digunakan.
> - `spacing`: Digunakan untuk menambahkan atau memodifikasi ukuran jarak (spacing) yang tersedia. Kita mendefinisikan dua ukuran tambahan di sini, yaitu `72` dan `84`, yang masing-masing setara dengan 18 rem dan 21 rem.
> - `backgroundImage`: Ini adalah bagian dari konfigurasi yang digunakan untuk menambahkan gambar latar belakang. Kita memberi nama gambar tersebut sebagai `anime` dan menyertakan path ke gambar tersebut menggunakan properti `url()`. Pastikan bahwa path ke gambar tersebut sesuai dengan struktur direktori proyek Anda.


#### KONFIGURASI 
**Kode Program CSS**
```css
theme: {
    
    fontFamily: {
      sans: ['Graphik', 'sans-serif'],
      serif: ['Merriweather', 'serif'],
      mono: ['ui-monospace', 'SFMono-Regular',]
    },
    extend: {
      spacing: {
        '8xl': '96rem',
        '9xl': '128rem',
      },
      borderRadius: {
        '4xl': '2rem',
      }
    }
```

>[!info]
>- `fontFamily`: Bagian ini digunakan untuk mendefinisikan jenis font yang akan digunakan dalam proyek, baik itu untuk jenis font sans-serif (`sans`) atau serif (`serif`). Setiap jenis font didefinisikan dengan daftar font yang diinginkan. Jika font pertama tidak tersedia, font kedua dalam daftar akan digunakan sebagai cadangan.
>- `extend`: Ini adalah bagian dari konfigurasi yang digunakan untuk menambahkan atau memperpanjang konfigurasi tema yang telah ada sebelumnya. Dalam kasus ini, kita menambahkan beberapa nilai tambahan untuk `spacing` dan `borderRadius`.
>- `spacing`: Digunakan untuk menambahkan atau memodifikasi ukuran jarak (spacing) yang tersedia. Di sini, kita menambahkan dua ukuran tambahan, yaitu `8xl` dan `9xl`, yang masing-masing setara dengan 96 rem dan 128 rem.
>- `borderRadius`: Digunakan untuk menambahkan atau memodifikasi ukuran radius sudut (border radius) yang tersedia. Dalam kasus ini, kita menambahkan satu nilai tambahan, yaitu 
>- `4xl`, yang setara dengan 2 rem.

**Referensi Font Tailwind : [Font Family - Tailwind CSS](https://tailwindcss.com/docs/font-family)**

#### Color Objek Syntax
**Kode Program CSS**
```css
theme: {
    colors: {
      transparent: 'transparent',
      current: 'currentColor',
      'white': '#ffffff',
      'tahiti': {
        100: '#cffafe',
        200: '#a5f3fc',
        300: '#67e8f9',
        400: '#22d3ee',
        500: '#06b6d4',
        600: '#0891b2',
        700: '#0e7490',
        800: '#155e75',
        900: '#164e63',
      },
      // ...
    },
  },
```

>[!info]
>- theme: Ini adalah objek utama yang berisi konfigurasi tema Tailwind CSS.
>- colors: Ini adalah bagian dari tema yang mendefinisikan palet warna yang dapat Anda gunakan dalam proyek Anda.
>- transparent: Ini adalah warna transparan yang dapat digunakan sebagai nilai pada properti warna.
>- current: Ini adalah warna saat ini yang dapat digunakan sebagai nilai pada properti warna.
>- 'white': '#ffffff': Ini mendefinisikan warna putih dengan kode heksadesimal #ffffff.
>- tahiti': Ini adalah nama untuk palet warna yang Anda definisikan, dalam hal ini, palet warna yang disebut "tahiti".
>- '100': '#cffafe': Ini adalah warna dengan tingkat kecerahan 100 pada palet "tahiti" dengan kode heksadesimal #cffafe.
>- '200': '#a5f3fc': Ini adalah warna dengan tingkat kecerahan 200 pada palet "tahiti" dengan kode heksadesimal #a5f3fc.

**Referensi Color Tailwind : [Customizing Colors - Tailwind CSS](https://tailwindcss.com/docs/customizing-colors)**
#### Using Custom Color
**Kode Program CSS**
```css
theme: {
    colors: {
      transparent: 'transparent',
      current: 'currentColor',
      'white': '#ffffff',
      'purple': '#3f3cbb',
      'midnight': '#121063',
      'metal': '#565584',
      'tahiti': '#3ab7bf',
      'silver': '#ecebff',
      'bubble-gum': '#ff77e9',
      'bermuda': '#78dcca',
    },
  },
```

>[!info]
>- theme: Ini adalah objek utama yang berisi konfigurasi tema Tailwind CSS.
>- colors: Ini adalah bagian dari tema yang mendefinisikan palet warna yang dapat Anda gunakan dalam proyek Anda.
>- transparent: Ini adalah warna transparan yang dapat digunakan sebagai nilai pada properti warna.
>- current: Ini adalah warna saat ini yang dapat digunakan sebagai nilai pada properti warna.
>- 'white': '#ffffff': Ini mendefinisikan warna putih dengan kode heksadesimal #ffffff.
>- 'purple': '#3f3cbb': Ini adalah warna ungu dengan kode heksadesimal #3f3cbb.
>- midnight': '#121063': Ini adalah warna midnight blue dengan kode heksadesimal #121063.
>- metal': '#565584': Ini adalah warna metal dengan kode heksadesimal #565584.
>- tahiti': '#3ab7bf': Ini adalah warna tahiti dengan kode heksadesimal #3ab7bf.
>- silver': '#ecebff': Ini adalah warna silver dengan kode heksadesimal #ecebff.
>- bubble-gum': '#ff77e9': Ini adalah warna bubble gum dengan kode heksadesimal #ff77e9.
>- 'bermuda': '#78dcca': Ini adalah warna bermuda dengan kode heksadesimal #78dcca.

**Contoh penggunaan nya: 
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <link href="https://cdn.jsdelivr.net/npm/tailwindcss@2.2.19/dist/tailwind.min.css" rel="stylesheet">
    <link href="style.css" rel="stylesheet">
</head>
<body class="font-body">
    <div class="bg-anime p-72 text- text-center">
        <h1 class="font-heading">Heading</h1>
        <p class="font-sans">Lorem ipsum, dolor sit amet consectetur adipisicing elit. Molestiae fugit ea cupiditate nemo expedita, tempora commodi. Ipsam sunt, vitae nemo non illum dolor fuga repudiandae suscipit! Eos deserunt accusamus impedit, reprehenderit debitis ab, molestiae nesciunt blanditiis magnam deleniti dignissimos repellendus error obcaecati quod porro labore maxime quidem! Quod velit libero incidunt est! Earum, alias ab nisi quibusdam quidem atque molestias. Delectus mollitia eum corporis accusamus nemo eaque vel id, sint soluta harum iusto officia sapiente consectetur ut fugiat cumque distinctio! Eius error repellat illo iure magni ex. Accusamus modi saepe ut aspernatur fugit repudiandae magnam et fuga? Iure, officia quod!</p>
    </div>
    <div class="bg-purple p-72 text-white text-center">
        <h2 class="font-heading">Another Section</h2>
        <p class="font-sans">Lorem ipsum dolor sit amet, consectetur adipisicing elit. Optio repellat sequi error aspernatur exercitationem at impedit sunt fugit ab vitae atque, ea ipsam quo, iure delectus nulla quibusdam eius pariatur, nihil quam aut voluptate alias cupiditate magni. Magnam ea, aspernatur autem ullam perferendis qui repellendus suscipit sit exercitationem nostrum, eius neque omnis delectus reprehenderit, expedita cum quis nihil! Molestias quasi libero, quos omnis ad maxime officiis quas et velit, praesentium consequatur. Cupiditate a doloribus corporis sequi illo aperiam? Magnam tenetur repellat consectetur nam quas architecto illo cumque rerum ea labore. Est maiores aut porro nam officiis rem nihil mollitia aspernatur?</p>
    </div>
    <div class="bg-midnight p-72 text-white text-center">
        <h3 class="font-heading">Yet Another Section</h3>
        <p class="font-sans">Lorem ipsum dolor sit amet consectetur, adipisicing elit. Alias laboriosam quaerat suscipit porro officiis deleniti exercitationem nam sed! Ut officiis, possimus incidunt doloremque distinctio accusamus alias aperiam iusto animi doloribus soluta error repellendus minus ipsum facere earum provident ullam veritatis quidem molestiae iste dolorum voluptatibus tenetur. Ipsam accusantium quidem earum omnis debitis exercitationem? Recusandae error non laudantium quaerat mollitia blanditiis hic ea iste optio. Sit odit aut culpa qui minima? Officia, quos quam. Vitae placeat recusandae voluptatum sunt odit, quae, libero magni porro iste fuga nemo explicabo, molestias ipsa maiores minima animi eius laudantium. Cumque fuga labore quae expedita iusto.
        </p>
    </div>  
    <div class="bg-metal p-72 text-white text-center">
        <h4 class="font-heading">Last Section</h4>
        <p class="font-sans">Lorem ipsum dolor sit amet consectetur adipisicing elit. Sed quos natus, velit fugiat inventore alias quae laudantium dolorum error, sit rerum vel iure eaque et itaque ipsa, exercitationem consectetur quo repellendus nobis ea. Debitis quaerat porro nam ea provident minus dolorum, quod assumenda officiis quisquam quae voluptatibus quidem id. Corrupti, aut. Doloremque minima sequi minus eligendi! Commodi, sint sequi, reprehenderit sed numquam velit, ipsa beatae inventore explicabo ab unde incidunt illo tempore neque ullam totam! Architecto est illum dolorem inventore placeat corporis accusamus. Fuga veniam neque minus inventore. Porro recusandae beatae totam numquam dolores maiores ratione, adipisci explicabo sequi deserunt!</p>
    </div>
    <div class="bg-tahiti-500 rounded-4xl p-8 text-white text-center">
        <h5 class="font-heading">Special Section</h5>
        <p class="font-sans">Lorem ipsum dolor sit amet consectetur adipisicing elit. Officiis natus obcaecati fugit adipisci iusto vitae, laboriosam cumque hic, aperiam nobis eligendi tempore velit ipsa! Dolor consectetur eligendi dolorum ex, facere voluptatem tempore ut laborum delectus minus! Aliquam pariatur quo vero inventore temporibus aperiam voluptates molestiae nostrum labore vitae voluptatum ratione tempora at incidunt sint hic quidem perferendis, molestias nam impedit dolor tempore. Ad at ex pariatur. Maiores iure accusamus porro suscipit officia fugiat delectus laboriosam? Molestiae error delectus maiores quo quis ipsum dignissimos eum iure eligendi repudiandae corrupti quas dolore, nulla, quibusdam porro. Iusto laboriosam impedit libero deserunt ad temporibus.</p>
    </div>
</body>
</html>
```

**Hasil**
![](pemograman%20web/Tailwind/Tailwind/aset/cssss66.png)

![](pemograman%20web/Tailwind/Tailwind/aset/cssss67.png)

![](pemograman%20web/Tailwind/Tailwind/aset/cssss68.png)

![](pemograman%20web/Tailwind/Tailwind/aset/cssss69.png)

![](pemograman%20web/Tailwind/Tailwind/aset/cssss65.png)


**Referensi Color Tailwind : [Customizing Colors - Tailwind CSS](https://tailwindcss.com/docs/customizing-colors)**
### Penggunaan Komponen
#### Kode Program CSS
```css
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    <div class="container mx-auto ml-1">
        <nav class="p-4 -mt-4">
            <div class="container flex justify-between items-center">
                <span class="flex flex-wrap">
                    <img src="../../aset/logo.png" class="w-10 m-3">
                    <ul class="flex space-x-4 pt-2 pl-2 mt-3 font-bold">
                        <li><a href="#" class="bg-blue-900 text-white rounded-md px-3 py-2 text-sm font-medium m-3" aria-current="page">Home</a></li>
                        <li><a href="#" class="text-blue-900 m-3">About</a></li>
                        <li><a href="#" class="text-blue-900 m-3">Services</a></li>
                        <li><a href="#" class="text-blue-900 m-3">Contact</a></li>
                    </ul>
                </span>
                <div class="p-4 -mr-10 font-bold">
                    <button class="bg-blue-900 text-white rounded-md px-3 py-2 text-sm font-medium m-3 p-4">
                        <a href="#" class="rounded-md">Sign In</a>
                    </button>
                    <button class="bg-transparent text-blue-900 rounded-md px-3 py-2 text-sm font-medium">
                        <a href="#" class="rounded-none">Sign Up</a>
                    </button>
                </div>
            </div>
        </nav>
    </div>
    
</body>
</html>
```
 
> [!info]- Analisis
> `p-4` : untuk memberi jarak (padding) antara objek lain sebesar 4px
> `mt`: untuk memberi jarak objek pada objek di atasnya
>`justify-between`: untuk memberi jarak pada setiap item di container
> `item-center`: untuk menengahkan sebuah item
> `flex-wrap`: untuk mengontrol item item pada container
> `w-10`: untuk memngatur lebar sebuah objek sebesar 10px
> `m-3`: untuk mengatur ketebalan margin sebesar 3px
> `font-bold`: untuk memberikan ketebalan kepada teks
> `space-x-4 `: digunakan untuk menentukan ruang horizontal antara elemen-elemen yang sejajar (horizontal) didalam suatu flex container.
> `pt-2`: untuk memberi jarak antara teks ke item sebesar 2px
> `bg-blue-900` : digunakan untuk memberikan warna latar belakang biru angka 900 menunjukkan kecerahan atau kegelapan warna biru, semakin tinggi angkanya maka semakin gelap warnanya
> `text-white` : untuk memberikan warna putih pada teks angka 900 menunjukkan kecerahan atau kegelapan warna biru, semakin tinggi angkanya maka semakin gelap warnanya
> `rounded-md` : digunakan untuk memberikan sudut yang sedang dibulatkan pada halaman html.
> `px-3`: Memberikan padding horizontal sebesar 0.75 rem (12px). berarti elemen tersebut akan memiliki padding sebesar 12 piksel di sisi kiri dan kanan.
>`py-2` : Memberikan padding vertikal sebesar 0.5 rem (8px). berarti elemen tersebut akan memiliki padding sebesar 8 piksel di sisi atas dan bawah.
> `text-sm` : digunakan untuk mengatur ukuran teks menjadi lebih kecil.
> `font-medium`: digunakan untuk memberikan bobot huruf yang medium pada teks .
> ` aria-current`: digunakan untuk menandai elemen yang merepresentasikan halaman atau bagian halaman yang saat ditampilkan.
>`"bg-transparent`: membuat background menjadi transparan 
 


### Responsive
Kode Program :
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Contoh Responsive Web dengan Tailwind CSS</title>
    <link href="https://cdn.jsdelivr.net/npm/tailwindcss@2.2.19/dist/tailwind.min.css" rel="stylesheet">
    <style>
    
    </style>
</head>
<body class="bg-gradient-to-br from-green-500 to-pink-500 min-h-screen flex items-center justify-center">
    <div class="max-w-2xl bg-white p-8 rounded-lg shadow-lg">
        <h1 class="text-4xl font-bold mb-4 text-center text-gray-800">Selamat Datang di Situs ?</h1>
        <p class="text-lg text-gray-700 mb-6">Temukan Informasi .</p>
        <div class="grid grid-cols-1 md:grid-cols-2 gap-8">
            <div class="flex items-center justify-center bg-gradient-to-br from-green-400 to-blue-500 p-8 rounded-lg shadow-lg">
                <h2 class="text-2xl font-semibold text-white">Seputar AFF Bola</h2>
            </div>
            <div class="flex items-center justify-center bg-gradient-to-br from-yellow-400 to-orange-500 p-8 rounded-lg shadow-lg">
                <h2 class="text-2xl font-semibold text-white"> Seputar AFF </h2>
            </div>
           
        </div>
    </div>
</body>
</html>
```

> [!info]- Analisis
>>- `<link href="https://cdn.jsdelivr.net/npm/tailwindcss@2.2.19/dist/tailwind.min.css" rel="stylesheet">`: Mengimpor Tailwind CSS dari CDN.
>>- `<style>`: Bagian untuk menambahkan CSS kustom jika diperlukan. 
>>- `<body class="bg-gradient-to-br from-green-500 to-pink-500 min-h-screen flex items-center justify-center">`: Elemen tubuh dokumen HTML dengan kelas Tailwind CSS untuk mengatur tata letak, tampilan, memberikan warna .
>>- `<div class="max-w-2xl bg-white p-8 rounded-lg shadow-lg">`: Membuat div dengan batasan lebar maksimal, latar belakang putih, padding, sudut yang dibulatkan, dan bayangan (shadow) menggunakan kelas Tailwind CSS.
>>- `<h1 class="text-4xl font-bold mb-4 text-center text-gray-800">`Selamat Datang di Situs ?`</h1>:` Membuat heading level 1 dengan ukuran teks besar, tebal, dan berwarna abu-abu menggunakan kelas Tailwind CSS.
>>- `<p class="text-lg text-gray-700 mb-6">Temukan Informasi .</p>`: Membuat paragraf dengan ukuran teks besar dan warna abu-abu menggunakan kelas Tailwind CSS.
>>- `<div class="grid grid-cols-1 md:grid-cols-2 gap-8">`: Membuat grid dengan satu kolom pada perangkat seluler dan dua kolom pada perangkat dengan lebar minimal MD (medium), dengan jarak antara elemen-elemen grid.
>>- `<div class="flex items-center justify-center bg-gradient-to-br from-green-400 to-blue-500 p-8 rounded-lg shadow-lg">`: Membuat div dengan tata letak flexbox, latar belakang gradien, padding, sudut yang dibulatkan, dan bayangan menggunakan kelas Tailwind CSS.
>>- `<h2 class="text-2xl font-semibold text-white">Seputar AFF Bola</h2>`: Membuat heading level 2 dengan ukuran teks besar, tebal, dan berwarna putih menggunakan kelas Tailwind CSS.
>>- `</div>`: Penutup dari div.
>>- `<div class="flex items-center justify-center bg-gradient-to-br from-yellow-400 to-orange-500 p-8 rounded-lg shadow-lg">`: Elemen div kedua dengan kelas yang sama seperti sebelumnya tetapi dengan gradien warna yang berbeda.
>>- `<h2 class="text-2xl font-semibold text-white">Seputar AFF</h2>`: Heading level 2 dengan kelas yang sama seperti sebelumnya tetapi dengan teks yang berbeda.


Dan hasil programnya akan seperti berikut :
![](pemograman%20web/Tailwind/Tailwind/aset/cssss62.png)
Cara Pengerjaan :
1. Membuat background berwarna biru yang di gradasikan dengan pink dengan cara mengetikkan kode `<body class="bg-gradient-to-br from-green-500 to-pink-500 min-h-screen flex items-center justify-center">`
2. Lalu membuat box yang berisikan teks "Selamat Datang DI situs ?" dan "Temukan Informasi." dan dua container di dalamnya dengan cara `<h1 class="text-4xl font-bold mb-4 text-center text-gray-800">`,`<p class="text-lg text-gray-700 mb-6">Temukan Informasi .</p>` dan dua box didalammnya
3. Lalu membuat dua kolom dengan tulisan "Seputar AFF Bola" dan "Seputar AFF" dengan cara  mengetikkan `<div class="grid grid-cols-1 md:grid-cols-2 gap-8"`,`<h2 class="text-2xl font-semibold text-white">Seputar AFF Bola</h2>` dan `<h2 class="text-2xl font-semibold text-white">Seputar AFF</h2>`.
4. Lalu mengatur posisi seluruh boxnya dengan kode `<div class="flex items-center justify-center bg-gradient-to-br from-green-400 to-blue-500 p-8 rounded-lg shadow-lg">`

Dan berikut ialah hasil setelah mengatur responsivenya :
![](pemograman%20web/Tailwind/Tailwind/aset/cssss63.png)
1. untuk mengatur responsivenya kita menggunakan kode 
```
<div class="grid grid-cols-1 md:grid-cols-2 gap-8">`

```
### Implementasi

**Kode Program**
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Daftar Barang</title>
    <link href="https://cdn.jsdelivr.net/npm/tailwindcss@2.2.19/dist/tailwind.min.css" rel="stylesheet">
</head>
<body style="background-image: url(../aset/deku.png); background-size: 1500px;">
<nav class="bg-white shadow">
    <div class="container mx-auto px-4 flex justify-between items-center">
        <div class="flex">
            <a class="navbar-brand l" href="#">Ada Kah</a>
            <ul class="flex flex-col sm:flex-row sm:items-center sm:justify-center sm:space-x-3 pl-3">
                <li class="nav-item pl-3">
                    <a class="nav-link active rounded hover:bg-blue-600" aria-current="page" href="#">Home</a>
                </li>
                <li class="nav-item pl-3">
                    <a class="nav-link rounded hover:bg-blue-600" href="#">About</a>
                </li>
                <li class="nav-item pl-3">
                    <a class="nav-link rounded hover:bg-blue-600" href="#">Services</a>
                </li>
                <li class="nav-item pl-3">
                    <a class="nav-link rounded hover:bg-blue-600" href="#">Contact</a>
                </li>
            </ul>
        </div>
        <div class="flex">
            <button class="bg-blue-500 hover:bg-blue-700 text-white font-bold py-2 px-4 rounded mx-2"><a href="soal2.html" class="text-white">Sign Up</a></button>
            <button class="bg-white hover:bg-gray-100 text-gray-800 font-semibold py-2 px-4 border border-gray-400 rounded shadow">Sign In</button>
        </div>
    </div>
</nav>
<div class="container mx-auto">
    <h1 class="text-center mt-5">Ada Ji Mau di Give Apa</h1>
    <div class="row mt-3">
        <div class="col-md-6">
            <select id="categoryFilter" class="form-select mb-2">
                <option value="elektronik">elektronik</option>
                <option value="fashion">Fashion</option>
                <option value="alat_rumah_tangga">alat_rumah_tangga</option>
                <option value="">Semua Kategori</option>
            </select>
        </div>
    </div>
    <div class="grid grid-cols-1 sm:grid-cols-2 md:grid-cols-3 lg:grid-cols-4 xl:grid-cols-5 gap-4">
        <div>
            <ul class="divide-y divide-gray-200 text-red-500">
                <li class="p-4 hover:bg-gray-100 cursor-pointer" data-category="elektronik">Laptop</li>
                <li class="p-4 hover:bg-gray-100 cursor-pointer" data-category="elektronik">Smartphone</li>
                <li class="p-4 hover:bg-gray-100 cursor-pointer" data-category="fashion">Sepatu</li>
                <li class="p-4 hover:bg-gray-100 cursor-pointer" data-category="fashion">Baju</li>
                <li class="p-4 hover:bg-gray-100 cursor-pointer" data-category="alat_rumah_tangga">Panci</li>
                <li class="p-4 hover:bg-gray-100 cursor-pointer" data-category="alat_rumah_tangga">Piring</li>
            </ul>
        </div>
        <div>
            <ul class="divide-y divide-gray-200 text-red-500">
                <li class="p-4 hover:bg-gray-100 cursor-pointer" data-category="elektronik">laptop</li>
                <li class="p-4 hover:bg-gray-100 cursor-pointer" data-category="elektronik">Smartphone</li>
                <li class="p-4 hover:bg-gray-100 cursor-pointer" data-category="fashion">Sepatu</li>
                <li class="p-4 hover:bg-gray-100 cursor-pointer" data-category="fashion">Baju</li>
                <li class="p-4 hover:bg-gray-100 cursor-pointer" data-category="alat_rumah_tangga">Panci</li>
                <li class="p-4 hover:bg-gray-100 cursor-pointer" data-category="alat_rumah_tangga">Piring</li>
            </ul>
        </div>
        <div>
            <ul class="divide-y divide-gray-200 text-red-500">
                <li class="p-4 hover:bg-gray-100 cursor-pointer" data-category="elektronik">laptop</li>
                <li class="p-4 hover:bg-gray-100 cursor-pointer" data-category="elektronik">Smartphone</li>
                <li class="p-4 hover:bg-gray-100 cursor-pointer" data-category="fashion">Sepatu</li>
                <li class="p-4 hover:bg-gray-100 cursor-pointer" data-category="fashion">Baju</li>
                <li class="p-4 hover:bg-gray-100 cursor-pointer" data-category="alat_rumah_tangga">Panci</li>
                <li class="p-4 hover:bg-gray-100 cursor-pointer" data-category="alat_rumah_tangga">Piring</li>
            </ul>
        </div>
        <div>
            <ul class="divide-y divide-gray-200 text-red-500">
                <li class="p-4 hover:bg-gray-100 cursor-pointer" data-category="elektronik">Laptop</li>
                <li class="p-4 hover:bg-gray-100 cursor-pointer" data-category="elektronik">Smartphone</li>
                <li class="p-4 hover:bg-gray-100 cursor-pointer" data-category="fashion">Sepatu</li>
                <li class="p-4 hover:bg-gray-100 cursor-pointer" data-category="fashion">Baju</li>
                <li class="p-4 hover:bg-gray-100 cursor-pointer" data-category="alat_rumah_tangga">Panci</li>
                <li class="p-4 hover:bg-gray-100 cursor-pointer" data-category="alat_rumah_tangga">Piring</li>
            </ul>
        </div>
    </div>
</div>
<script src="https://ajax.googleapis.com/ajax/libs/jquery/3.5.1/jquery.min.js"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/popper.js/1.16.0/umd/popper.min.js"></script>
<script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/js/bootstrap.min.js"></script>
<script>
    document.querySelectorAll('.list-group-item').forEach(item => {
        item.addEventListener('click', () => {
            item.classList.toggle('active'); // Toggle class 'active' on the clicked item
        });
    });

    document.querySelectorAll('.item').forEach(item => {
        item.addEventListener('click', () => {
            const category = item.getAttribute('data-category');
            document.querySelectorAll('.item').forEach(otherItem => {
                if (otherItem !== item && otherItem.getAttribute('data-category') !== category) {
                    otherItem.classList.add('disabled');
                } else {
                    otherItem.classList.remove('disabled');
                }
            });
        });
    });

    const maxSelection = 1; // Maximum number of items that can be selected
    let selectedItems = 0;

    document.querySelectorAll('.item').forEach(item => {
        item.addEventListener('click', () => {
            if (item.classList.contains('disabled')) return; // Check if item is disabled

            if (item.classList.contains('active')) {
                item.classList.remove('active');
                selectedItems--;
            } else {
                if (selectedItems < maxSelection) {
                    item.classList.add('active');
                    selectedItems++;
                }
            }

            // Disable other items if maximum selection is reached
            document.querySelectorAll('.item').forEach(otherItem => {
                if (otherItem !== item && !otherItem.classList.contains('active')) {
                    if (selectedItems >= maxSelection) {
                        otherItem.classList.add('disabled');
                    } else {
                        otherItem.classList.remove('disabled');
                    }
                }
            });
        });
    });

    document.getElementById('nextButton').addEventListener('click', () => {
        // Remove 'active' class from all items
        document.querySelectorAll('.item').forEach(item => {
            item.classList.remove('active');
        });
        selectedItems = 0;

        // Enable all items
        document.querySelectorAll('.item').forEach(item => {
            item.classList.remove('disabled');
        });
    });
</script>
</body>
</html>

```


#### Hasil :
![](pemograman%20web/Tailwind/Tailwind/aset/cssss64.png)

#### Penjelasan :
1. **Container** (`container`): Mengatur lebar konten di dalamnya. Pada kode Anda, digunakan untuk mengelompokkan elemen-elemen konten.
    
2. **Flex Container** (`flex`): Mengatur elemen-elemen anak menjadi flex items di dalam flex container. Digunakan untuk mengatur layout navbar dan tombol Sign Up dan Sign In.
    
3. **Navbar** (`navbar`): Membuat navigasi bar. Pada kode Anda, digunakan untuk membuat navbar di bagian atas halaman.
    
4. **Button** (`bg-blue-500`, `bg-blue-700`, `bg-white`, `hover:bg-blue-600`, `hover:bg-gray-100`): Membuat tombol. Digunakan untuk tombol Sign Up dan Sign In dengan variasi warna dan efek hover.
    
5. **Text** (`text-red-500`, `text-white`, `text-gray-800`, `font-bold`, `font-semibold`): Mengatur warna teks dan ketebalan teks. Digunakan untuk menyesuaikan warna dan gaya teks pada tombol dan daftar barang.
    
6. **Padding** (`p-4`): Memberikan padding pada elemen. Digunakan untuk memberikan ruang di sekitar teks pada daftar barang.
    
7. **Hover Effect** (`hover:bg-gray-100`): Memberikan efek hover pada elemen. Digunakan untuk memberikan efek warna latar belakang saat kursor diarahkan ke atas elemen.
    
8. **Grid Container** (`grid`, `grid-cols-1`, `sm:grid-cols-2`, `md:grid-cols-3`, `lg:grid-cols-4`, `xl:grid-cols-5`, `gap-4`): Membuat layout grid dengan jumlah kolom yang berbeda-beda tergantung ukuran layar. Digunakan untuk menyusun daftar barang menjadi grid.
    
9. **List Item** (`divide-y`, `divide-gray-200`): Memberikan garis pemisah antara item pada daftar. Digunakan untuk memisahkan setiap item pada daftar barang.
    
10. **Cursor Pointer** (`cursor-pointer`): Mengubah ikon kursor menjadi tanda panah saat mengarahkan kursor ke elemen. Digunakan untuk menunjukkan bahwa elemen tersebut dapat diklik.

