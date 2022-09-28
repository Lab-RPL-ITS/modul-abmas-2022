# Daftar Isi

- [Daftar Isi](#daftar-isi)
- [Persiapan](#persiapan)
- [HTML](#html)
  - [Dokumen HTML](#dokumen-html)
  - [Elemen, Tag, Attribut](#elemen-tag-attribut)
    - [Elemen](#elemen)
    - [Tag](#tag)
    - [Atribut](#atribut)
  - [Cara Kerja HTML](#cara-kerja-html)
  - [Struktur HTML](#struktur-html)
  - [Layout Dasar](#layout-dasar)
  - [Judul dan Paragraf](#judul-dan-paragraf)
    - [Tag Judul](#tag-judul)
    - [Tag Paragraf](#tag-paragraf)
    - [Tag Tautan](#tag-tautan)
    - [Tag Gambar](#tag-gambar)
    - [Tag Daftar (List)](#tag-daftar-list)
    - [Tag Table](#tag-table)
    - [Tag Form & Input](#tag-form--input)
    - [Tag div & span](#tag-div--span)
- [CSS](#css)
  - [Sintaks](#sintaks)
  - [Cara Menggunakan CSS](#cara-menggunakan-css)
  - [Selector](#selector)
    - [Simple Selector](#simple-selector)
    - [Combinator Selector](#combinator-selector)
    - [Pseudo-class Selector](#pseudo-class-selector)
    - [Pseudo-element Selector](#pseudo-element-selector)
    - [Attribute Selector](#attribute-selector)
  - [Property dan Value](#property-dan-value)
    - [Colors](#colors)
    - [Box Model](#box-model)
  - [Specificity](#specificity)
- [Referensi](#referensi)

# Persiapan

Sebelum memulai materi, terdapat beberapa hal yang perlu dipersiapkan:

1. Web Browser <br/>
   Contoh: Google Chrome (recommended), Mozilla Firefox, Microsoft Edge, atau Safari.
2. Text Editor <br/>
   Contoh: [Visual Studio Code](https://code.visualstudio.com/download) (recommended), Sublime Text, Atom, [Notepad++](https://notepad-plus-plus.org/downloads/v8.4.5/), atau Notepad.

# HTML

HTML atau Hypertext Markup Language adalah bahasa markup standar yang digunakan untuk membuat halaman website. HTML mendeskripsikan struktur dari halaman website yang akan ditampilkan pada web browser seperti Chrome, Edge, Safari dll.

## Dokumen HTML

Dalam menulis HTML, kode HTML akan disimpan dalam suatu file yang memiliki **.html** atau **.htm** di akhir nama file. Contoh : index<strong>.html</strong> atau index<strong>.htm</strong>

## Elemen, Tag, Attribut

Sebelum masuk lebih jauh, kita akan melihat tiga istilah utama yang harus diketahui ketika menulis HTML. Ketiga istilah tersebut adalah **elemen**, **tag**, dan **atribut**.

### Elemen

Elemen HTML merupakan komponen/bagian yang menetapkan peran sebuah objek dalam dokumen, termasuk struktur dan konten dari objek tersebut.

Contoh:

```html
<h1>Ini adalah judul utama.</h1>
<p>Ini adalah paragraf.</p>
```

Berdasarkan contoh kode diatas elemen `h1` digunakan untuk membuat tulisan yang berperan sebagai judul utama atau heading 1. Sedangkan elemen `p` digunakan untuk membuat tulisan yang berperan sebagai paragraf.

### Tag

Sebuah elemen biasanya dinyatakan dengan tag. Tag pembuka menandakan awal dari sebuah elemen, dan tag penutup menandakan akhir dari sebuah elemen. Tag pembuka dinyatakan dengan nama elemen yang diapit simbol kurang dari (<) dan lebih dari (>), contohnya `<h1>`. Tag penutup dituliskan dengan menambahkan garis miring (/) setelah simbol kurang dari (<). Misalnya, tag penutup untuk elemen `h1` adalah `</h1>`.

### Atribut

Atribut merupakan informasi tambahan yang dapat kita berikan pada sebuah elemen. Setiap elemen memiliki atribut yang berbeda-beda, namun terdapat beberapa atribut standar yang dapat digunakan oleh semua elemen.

Atribut khusus elemen merupakan atribut yang hanya dapat digunakan pada elemen tersebut. Sebagai contoh, pada elemen `img` yang digunakan untuk menampilkan gambar, terdapat atribut `src` untuk menentukan sumber gambar yang akan ditampilkan. Atribut ini tentunya tidak akan berguna untuk elemen `p`, yang hanya menampilkan teks.

Atribut standar yang dimiliki oleh semua elemen sendiri merupakan atribut yang umumnya dapat diimplementasikan oleh semua elemen, misalnya atribut `id` untuk identifikasi elemen, atau atribut `class` untuk melakukan penggolongan elemen.

Kode di bawah menunjukkan contoh elemen `a` yang digunakan dengan atribut wajib elemen tersebut yakni `href`:

```html
<a href="http://www.google.com">Ini adalah sebuah link yang akan membuka google</a>
```

Kode di atas memberikan contoh atribut `href` yang dimiliki oleh elemen `a`. Atribut ini berguna untuk menentukan link yang akan dituju ketika dibuka dari sebuah elemen (nama “href” sendiri merupakan kepanjangan dari hyperlink reference). Sedangkan kode berikut menunjukkan contoh elemen `img` yang digunakan dengan atribut khusus elemen tersebut yakni `src`:

```html
<img src="gambar.jpg" width="104" height="142">
```

Atribut-atribut yang dimiliki oleh tiap-tiap elemen akan dibahas lebih lanjut pada pembahasan masing-masing elemen.

## Cara Kerja HTML

Aturan pertama dalam penulisan kode HTML adalah mengapit teks dengan **tag**. Elemen HTML didefinisikan dengan tag pembuka, suatu konten, dan tag penutup, seperti yang sudah dijelaskan sebelumnya sebagai berikut:

```html
<namaelemen>Konten diketikkan disini</namaelemen>
```

> Catatan: <br>Namun terdapat beberapa elemen HTML yang tidak memiliki konten salah satunya `<br>`. Elemen tersebut dapat disebut sebagai elemen yang kosong. Oleh karena itu elemen kosong tidak memiliki tag penutup (`</namaelemen>`).

## Struktur HTML

Ada beberapa aturan dalam membuat dokumen HTML. Semua dokumen HTML harus dimulai dengan penjelasan tipe dokumen, dalam hal ini kita harus menyertakan `<!DOCTYPE html>` sebelum tag HTML lainnya. Selain itu dalam HTML, elemen `<head>` dan `<body>` wajib berada di dalam elemen `<html>` sebagai berikut:

```html
<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8" />
    <title>Judul Halaman</title>
    <link rel="stylesheet" href="stylesheet.css" />
  </head>
  <body>
    <h1>Ini adalah judul utama.</h1>
    <p>Ini adalah paragraf.</p>
  </body>
</html>
```

Berdasarkan contoh struktur HTML diatas, perlu diketahui:

1. `<!DOCTYPE html>` <br/>
   Ini akan menentukan versi HTML secara otomatis sehingga versi HTML situs web yang dibuat merupakan versi yang terbaru.
2. `<head>` <br/>
   Berisi informasi dokumen atau settingan dokumen HTML yang tidak terlihat ketika membuka halaman. Ada tiga elemen yang harus diletakkan di dalam `<head>` yaitu:
   - Pengkodean karakter (encoding) <br/>
     `<meta charset="utf-8">` untuk memastikan situs web menggunakan pengkodean karakter yang konsisten. UTF-8 adalah pengkodean karakter yang direkomendasikan untuk HTML5.
   - Judul situs web <br/>
     `<title>Judul Halaman</title>` judul yang muncul pada tab / bagian atas browser.
   - Hubungan dengan file CSS <br/>
     `<link rel="stylesheet" href="stylesheet.css">` agar HTML dapat terhubung dengan file CSS yang diinginkan, kita perlu menghubungkannya menggunakan elemen ini.
3. `<body>` <br/>
   Berisi konten yang terlihat di browser

## Layout Dasar

Layout atau tata letak adalah salah satu bagian paling penting dalam membuat situs web. Dengan menentukan terlebih dahulu layout dari suatu web yang ingin kita buat, dapat memudahkan kita dalam penataan elemen-elemen yang dibutuhkan.

![image1](https://user-images.githubusercontent.com/68275535/130474382-c674fb7f-72ef-4161-99f5-d7eed63104dd.png)

**Elemen Header**

Seperti namanya, header merupakan elemen yang berisi judul dan penjelasan lain situs web. Biasanya elemen ini diisikan dengan logo website, menu-menu umum (seperti login dan logout), maupun nama halaman yang sedang ditampilkan.

**Elemen Navigation**

Elemen navigasi, yang memberikan akses navigasi ke halaman-halaman lain dalam web.

**Elemen Sidebar**

Elemen ini merupakan hal-hal yang menjadi pendukung konten, dapat berupa pembantu navigasi konten seperti daftar isi, ataupun berbagai hal lain seperti daftar konten lain, iklan, atau menu tambahan. Sidebar dapat berada di kiri atau kanan konten, atau bahkan di kiri dan kanan konten, sesuai dengan kreatifitas perancangnya.

**Elemen Content**

Elemen ini merupakan isi utama dari situs web. Pengguna biasanya datang ke web untuk melihat teks yang berada pada bagian ini.

**Elemen Footer**

Bagian penutup dari website, yang dapat berisi informasi lain tentang website, seperti lisensi penggunaan, link ke halaman lain, ataupun link ke website lain.

Nah lalu bagaimana kita dapat membuat layout seperti contoh di atas? Kita dapat menggunakan tag `<div>` maupun tag yang telah tersedia seperti `<header>`, `<footer>`, dll.

## Judul dan Paragraf

### Tag Judul

Tag judul digunakan untuk memformat elemen judul. Tag ini bervariasi mulai dari `<h1>` hingga `<h6>`. Yang mana semakin besar angka semakin kecil ukuran textnya.

```html
<h1>Heading 1</h1>
<h2>Heading 2</h2>
<h3>Heading 3</h3>
<h4>Heading 4</h4>
<h5>Heading 5</h5>
<h6>Heading 6</h6>
```

### Tag Paragraf

Paragraf digunakan untuk menulis teks biasa. Sebuah paragraf selalu dimulai pada baris baru, dan pada paragraf tersebut terdapat margin/jarak pada bagian atas dan bawahnya. Untuk membuat paragraf dapat menggunakan tag `<p>`.

```html
<p>Paragraf pertama</p>
<p>Paragraf kedua</p>
```

### Tag Tautan

Kita dapat dengan mudah membuat tautan dengan menggunakan tag `<a>`. Teks yang berada di dalam tag tersebut akan ditampilkan pada browser sebagai teks tautan/teks yang dapat di-klik.

```html
<a href="https://www.google.com">Buka Google</a>
```

Setiap tautan memiliki link tujuan, maka dari itu agar tautan berfungsi kita harus menentukan URL tujuan dengan menambahkan atribut `href`. Seperti kode yang telah dijabarkan di atas, di mana isi dari atribut `href` bernilai alamat URL `https://www.google.com`.

### Tag Gambar

Tag `<img>` digunakan untuk menampilkan gambar. Kita dapat menetapkan gambar dengan menentukan sumber gambar di atribut `src`. Sumber gambar tersebut dapat kita arahkan ke penyimpanan lokal (folder yang ada di komputer) ataupun gambar yang ada di internet dengan menggunakan URL/link gambar tersebut.

```html
<img src="./folder gambar/foto.jpg" alt="Foto formal" height="60px" width="40px" />
```

Pada contoh tersebut kita mengisi atribut `src` dengan file yang berada di dalam folder gambar bernama `foto.jpg`. Adapula atribut lain seperti `alt` digunakan sebagai deskripsi alternatif dari gambar yang mana deskripsi ini akan ditampilkan apabila sumber gambar tidak dapat terbuka. Atribut `height` dan `width` digunakan untuk menentukan ukuran dari gambar, dalam contoh ini kita menggunakan satuan pixel sebagai ukuran gambar.

### Tag Daftar (List)

Terdapat 3 macam daftar yang dapat kita gunakan dalam HTML, yakni:

1. Unordered List (`ul`) <br/>
   Merupakan daftar yang tidak memiliki nomor urut. Penggunaan unordered list akan menghasilkan daftar dengan awalan suatu simbol, secara bawaan  simbol yang digunakan yakni simbol lingkaran (●). Untuk mengisi listnya kita dapat mengapit konten dengan tag `<li>`.

   ```html
   <h2>Contoh unordered list</h2>
   <ul>
     <li>Kopi</li>
     <li>Teh</li>
     <li>Susu</li>
   </ul>
   ```

   Ilustrasi:

   ![image1](https://user-images.githubusercontent.com/33245436/191101791-ade86151-457d-44a7-8a9a-72ba6824c098.png)
   
2. Ordered List (`ol`) <br/>
   Merupakan daftar yang yang memiliki nomor urut dengan awalan angka. Untuk mengisi listnya kita menggunakan tag `<li>`.

   ```html
   <h2>Contoh ordered list</h2>
   <ol>
     <li>Kopi</li>
     <li>Teh</li>
     <li>Susu</li>
   </ol>
   ```

   Ilustrasi:

   ![image2](https://user-images.githubusercontent.com/33245436/191101927-e885a3c6-ae4b-4756-ba4a-198d50496917.png)

3. Description List (`dl`) <br/>
   Merupakan daftar yang digunakan jika ingin menambahkan deskripsi untuk tiap daftar. Dengan menggunakan tag `<dt>` untuk mendefinisikan nama bagian dan tag `<dd>` untuk mendefinisikan deskripsinya.

   ```html
   <h2>Contoh description list</h2>
   <dl>
     <dt>Kopi</dt>
     <dd>Minuman pahit</dd>
     <dt>Susu</dt>
     <dd>Minuman manis</dd>
   </dl>
   ```

   Ilustrasi:

   ![image3](https://user-images.githubusercontent.com/33245436/191102126-5b3afdbd-6873-4e7e-a947-0b385bd7a9c7.png)

### Tag Table

Jika ingin membuat sebuah tabel pada website, maka kita dapat menggunakan tag `<table>`. Kemudian untuk membuat baris tabel kita dapat menggunakan tag `<tr>` (table row), lalu untuk membuat judul pada tabel kita dapat menggunakan tag `<th>` (table header), dan untuk isi dari tabel kita dapat menggunakan tag `<td>` (table data).

```html
<table>
  <tr>
    <th>No</th>
    <th>Nama</th>
  </tr>
  <tr>
    <td>1</td>
    <td>Ani</td>
  </tr>
  <tr>
    <td>2</td>
    <td>Boge</td>
  </tr>
</table>
```

Ilustrasi:

![image4](https://user-images.githubusercontent.com/68275535/130475305-df78906b-d4ff-4e4a-82c4-ce1befc797c5.png)

### Tag Form & Input

Jika kita ingin membuat suatu form dalam website maka kita dapat menggunakan tag `<form>` yang mana tag tersebut adalah wadah untuk berbagai jenis elemen input seperti: `fields`, `checkboxes`, `radio buttons`, `submit buttons`, dan masih banyak lainnya.

Atribut dari `<form>` yaitu:

1. Action <br/>
   Atribut yang mendefinisikan aksi yang akan dilakukan ketika formulir dikirimkan. Biasanya data formulir dikirim ke file di server ketika pengguna mengklik tombol kirim.

   Nilai dari atribut ini berupa URL. Contoh: `/simpan.php`.

2. Target <br/>
   Menentukkan tempat dari respon yang diterima setelah mengirim form.

   ![image5](https://user-images.githubusercontent.com/68275535/130475395-1778983d-d9cd-41a3-8126-3f2c4ae480c3.png)

3. Method <br/>
   Menentukkan metode HTTP yang digunakan oleh browser untuk mengirim data form.

   Nilainya berupa HTTP request method seperti `GET` apabila browser ingin mendapatkan data, kemudian terdapat request method `POST` apabila browser ingin mengirimkan data, dan masih banyak request method lainnya.

4. Autocomplete <br/>
   Menentukkan apakah kolom input dapat secara otomatis terisi atau tidak. Hal ini dilakukan secara otomatis (jika on) oleh browser dengan menampilkan tulisan yang sebelumnya pernah ditulis pada browser tersebut untuk menghindari penulisan berulang kali.

   Nilainya berupa `on` atau `off`.

Adapula elemen yang dapat digunakan untuk melengkapi sebuah form, diantaranya adalah sebagai berikut:

- `<button>`
- `<fieldset>`
- `<input>`
- `<label>`
- `<legend>`
- `<optgroup>`
- `<option>`
- `<select>`
- `<textarea>`

Adapun untuk input terdapat banyak jenisnya

- `<input type="text">`
- `<input type="password">`
- `<input type="number">`
- `<input type="email">`
- `<input type="radio">`
- `<input type="checkbox">`
- `<input type="file">`
- `<input type="hidden">`
- dan masih banyak lainnya

Contoh penggunaan tag `<form>` beserta inputnya

```html
<form action="#" method="post">
  <input type="text">
  <input type="password">
  <input type="radio" id="html" name="fav_language" value="HTML">
  <label for="html">HTML</label><br>
  <input type="radio" id="css" name="fav_language" value="CSS">
  <label for="css">CSS</label><br>
  <button type="submit">
</form>
```

Sangat banyak sekali atribut baik dari elemen yang dapat digunakan di dalam tag form ataupun atribut dari tag input itu sendiri. Maka untuk mempelajari lebih dalam bisa melalui https://www.w3schools.com/html/html_forms.asp

### Tag div & span

Tag `<div>` merupakan block-level elemen yakni elemen yang selalu dimulai dengan baris baru. Div dapat dikatakan pula sebagai container / wadah untuk elemen-elemen html. Pada tag ini kita dapat menggunakan atribut `style`, `class`, atau `id` untuk mempermudah styling dengan CSS yang akan kita pelajari pada materi selanjutnya.

```html
<div style="background-color:black;color:white;padding:20px;">
  <h2>London</h2>
  <p>
    London is the capital city of England. It is the most populous city in the
    United Kingdom, with a metropolitan area of over 13 million inhabitants.
  </p>
  <p>
    Standing on the River Thames, London has been a major settlement for two
    millennia, its history going back to its founding by the Romans, who named
    it Londinium.
  </p>
</div>
```

Ilustrasi:

![image6](https://user-images.githubusercontent.com/68275535/130475539-a8db8730-46e2-4996-8e1a-0829a163225e.png)

Tag <span> merupakan inline-level elemen yakni elemen yang tidak dimulai dengan baris baru. Sama seperti div, tag ini merupakan wadah untuk menandai bagian dari teks, atau bagian dari dokumen.

```html
<p>
  My mother has <span style="color: blue; font-weight: bold">blue</span>eyes and
  my father has
  <span style="color: darkolivegreen; font-weight: bold">dark green</span>
  eyes.
</p>
```

Ilustrasi:

![image7](https://user-images.githubusercontent.com/68275535/130475641-578b3af0-ee2a-449e-8758-f4ec1e223761.png)

# CSS

CSS (Cascading Style Sheets) adalah bahasa yang digunakan untuk mendeskripsikan style sebuah halaman web, agar web lebih bagus secara visual. Jika HTML adalah elemen-elemen yang membangun kerangka halaman web, CSS dipakai untuk mempercantik elemen tersebut. CSS dapat digunakan untuk beberapa halaman web sekaligus.

## Sintaks

![image1](https://user-images.githubusercontent.com/68275535/130475766-8e0e2807-ab77-4b15-adc2-74fd92719117.png)

**Selector** adalah elemen HTML yang ingin dipilih dan di-styling / dihias. Kemudian pada bagian **declaration** (dibuka dan ditutup dengan kurung kurawal) terdapat **property** yakni hal yang ingin diubah dan **value** yakni nilai property yang ingin digunakan dan diaplikasikan pada elemen dipilih.

## Cara Menggunakan CSS

Terdapat tiga cara menggunakan CSS, yaitu:

1. Inline <br/>
   Menulis CSS di dalam sebuah elemen HTML, pada atribut `style` suatu elemen HTML. Contoh di bawah, elemen `h1` dan `p` menggunakan CSS metode inline.

   ```html
   <!DOCTYPE html>
   <html>
     <body>
       <h1 style="color:blue;text-align:center;">This is a heading</h1>
       <p style="color:red;">This is a paragraph.</p>
     </body>
   </html>
   ```

Ilustrasi:

![image2](https://user-images.githubusercontent.com/33245436/191103212-0392b09e-fb33-49ad-8bf0-ac14e37b57d0.png)

2. Internal <br/>
   Menulis CSS langsung pada file HTML itu juga, namun perbedaannya dengan inline penulisan CSS ini diletakkan pada elemen `style`.

   ```html
   <!DOCTYPE html>
   <html>
     <head>
       <style>
         body {
           background-color: lightblue;
         }

         h1 {
           color: maroon;
           margin-left: 40px;
         }
       </style>
     </head>
     <body>
       <h1>This is a heading</h1>
       <p>This is a paragraph.</p>
     </body>
   </html>
   ```

Ilustrasi:

![image3](https://user-images.githubusercontent.com/33245436/191103797-69c7229a-4d2e-474c-920c-282740023083.png)

3. Eksternal <br/>
   Menulis CSS pada file terpisah berekstensi ‘.css’ dan dihubungkan pada HTML dengan elemen `link` seperti berikut.

   ```html
   <!DOCTYPE html>
   <html>
     <head>
       <link rel="stylesheet" href="style.css" />
     </head>
     <body>
       <h1>This is a heading</h1>
       <p>This is a paragraph.</p>
     </body>
   </html>
   ```

   Lalu pada file `style.css`, isinya sebagai berikut.

   ```css
   body {
     background-color: lightblue;
   }

   h1 {
     color: navy;
     margin-left: 20px;
   }
   ```

Ilustrasi:

![image4](https://user-images.githubusercontent.com/33245436/191104574-998e320a-7d73-4cfb-901c-24085ad2cb77.png)

## Selector

**Selector** adalah pemiliham elemen HTML yang ingin diberi style. Ada beberapa kategori selector:

### Simple Selector

1. Element Selector <br/>
   Pada contoh di bawah, selectornya adalah `p`. Maka semua elemen `p` akan terpengaruh oleh styling CSS tersebut.

   ```html
   <!DOCTYPE html>
   <html>
     <head>
       <style>
         p {
           text-align: center;
           color: red;
         }
       </style>
     </head>
     <body>
       <p>Semua paragraf akan terpengaruh dengan styling yang ada.</p>
       <p id="para1">Aku pun!</p>
       <p>Apalagi aku!</p>
     </body>
   </html>
   ```

Ilustrasi:

![image5](https://user-images.githubusercontent.com/33245436/191104950-0ab0d796-fd3f-4c9e-82b9-e8b4f889a838.png)

2. ID Selector <br/>
   Pada contoh di bawah, elemen dengan id `para1` akan terpengaruh styling CSS.

   ```html
   <!DOCTYPE html>
   <html>
     <head>
       <style>
         #para1 {
           text-align: center;
           color: red;
         }
       </style>
     </head>
     <body>
       <p id="para1">Hello World!</p>
       <p>Paragraf ini tidak terpengaruh dengan styling yang ada.</p>
     </body>
   </html>
   ```

Ilustrasi:

![image6](https://user-images.githubusercontent.com/33245436/191105116-ad4d8100-5dd2-46ba-b451-910e3d0e8574.png)

3. Class Selector <br/>
   Pada contoh di bawah, elemen dengan class `center` akan terpengaruh styling CSS.

   ```css
   .center {
     text-align: center;
     color: red;
   }
   ```

   Kamu juga bisa select elemen dan class tertentu. Pada contoh di bawah, hanya elemen p dengan class `center` yang akan terpengaruh styling CSS.

   ```css
   p.center {
     text-align: center;
     color: red;
   }
   ```

   ```html
   <!DOCTYPE html>
   <html>
     <head>
       <link rel="stylesheet" href="style.css" />
     </head>
     <body>
       <p class="center">Hello Again World!</p>
       <p>Paragraf ini tidak terpengaruh dengan styling yang ada.</p>
     </body>
   </html>
   ```

Ilustrasi:

![image7](https://user-images.githubusercontent.com/33245436/191105288-1a54c1c3-981e-47eb-9eed-7256a4ab3b61.png)

4. Universal Selector <br/>
   Dengan memakai \* , kita dapat men-select keseluruhan dokumen HTML.

   ```css
   * {
     text-align: center;
     color: blue;
   }
   ```

Ilustrasi:

![image8](https://user-images.githubusercontent.com/33245436/191105597-5036bf13-0441-4e28-ab88-4b5c0b4fc277.png)

5. Grouping Selector <br/>
   Dengan koma, kita bisa menggabungkan beberapa selector. Pada contoh dibawah, elemen `h1`, `h2`, dan `p` akan terpengaruh oleh CSS.

   ```css
   h1, h2, p {
     text-align: center;
     color: red;
   }
   ```

   ```html
   <!DOCTYPE html>
   <html>
     <head>
       <link rel="stylesheet" href="style.css" />
     </head>
     <body>
       <h1>This is a heading</h1>
       <h2>This is second heading</h2>
       <h3>This is third heading, I'm different!</h3>
       <p>This is a paragraph.</p>
     </body>
   </html>
   ```

Ilustrasi:

![image9](https://user-images.githubusercontent.com/33245436/191105950-c83f80d9-9e00-4b39-8a87-62c9e8fee206.png)

### Combinator Selector

Combinator selector menggunakan lebih dari 1 simple selector. Ada 4 jenis combinator selector.

1. Descendant Selector (spasi) <br/>
   Memilih suatu elemen di dalam elemen. Pada contoh di bawah, memilih semua `p` di dalam semua `div`.

   ```css
   div p {
     background-color: yellow;
   }
   ```

   ```html
   <!DOCTYPE html>
   <html>
     <head>
       <link rel="stylesheet" href="style.css" />
     </head>
     <body>
       <div>
         <p>Hello World!</p>
         <section>
           <p>Paragraf ini terdampak!</p>
         </section>
       </div>
     </body>
   </html>
   ```

Ilustrasi:

![image10](https://user-images.githubusercontent.com/33245436/191108283-c6de80bd-9fba-4353-9418-ad48a41cb5b5.png)

2. Child Selector (>) <br/>
   Memilih semua child / anak dari suatu elemen. Perbedaan child selector dengan descendant selector yakni child selector hanya mempengaruhi anak elemennya, tidak mempengaruhi cucunya atau anak dari anak elemen yang dipilih. Pada contoh di bawah, kita memilih semua elemen `p1` yang merupakan anak dari `div`.

   ```css
   div > p {
     background-color: yellow;
   }
   ```

   ```html
   <!DOCTYPE html>
   <html>
     <head>
       <link rel="stylesheet" href="style.css" />
     </head>
     <body>
       <div>
         <p>Hello World!</p>
         <section>
           <p>Paragraf ini tidak terpengaruh dengan styling yang ada.</p>
         </section>
         <p>Tapi ini terdampak.</p>
       </div>
     </body>
   </html>
   ```

Ilustrasi:

![image11](https://user-images.githubusercontent.com/33245436/191108508-b4b340f3-e30d-4992-b460-d43bf21fffb8.png)

3. Adjacent Sibling Selector (+) <br/>
   Untuk memilih suatu elemen yang tepat setelah satu elemen tersebut. Pada contoh di bawah, memilih semua elemen `p` yang terletak tepat setelah `div` bukan di dalamnya.

   ```css
   div + p {
     background-color: yellow;
   }
   ```

   ```html
   <!DOCTYPE html>
   <html>
     <head>
       <link rel="stylesheet" href="style.css" />
     </head>
     <body>
       <div>
        <p>Ini tidak terdampak.</p>
       </div>
       <p>Tapi ini terdampak.</p>
       <p>Sementara aku tidak terdampak.</p>
     </body>
   </html>
   ```

Ilustrasi:

![image12](https://user-images.githubusercontent.com/33245436/191109307-dcba9bb1-38c1-491c-bb2e-657ff2721de5.png)

4. General Sibling Selector (~) <br/>
   Untuk memilih elemen yang merupakan semua saudara selanjutnya suatu elemen. Pada contoh di bawah, kita akan memilih semua elemen `p` yang merupakan saudara selanjutnya dari elemen `div`

   ```css
   div ~ p {
     background-color: yellow;
   }
   ```

   ```html
   <!DOCTYPE html>
   <html>
     <head>
       <link rel="stylesheet" href="style.css" />
     </head>
     <body>
       <p>Hello World!</p>
       <div>
         <p>Paragraf ini tidak terpengaruh dengan styling yang ada.</p>
       </div>
       <p>Aku baru terdampak!</p>
       <p>Aku juga!</p>
     </body>
   </html>
   ```

Ilustrasi:

![image13](https://user-images.githubusercontent.com/33245436/191109113-f51d51a5-e684-4c89-98f8-0725a3232b2c.png)

### Pseudo-class Selector (:)

Pseudo-class dimanfaatkan untuk memilih suatu state / keadaan dari suatu elemen. Contohnya, saat elemen di-hover (ketika mouse berada di atas elemen) dan di-klik.

Contoh pseudo-class dapat dilihat pada pengaplikasiannya di elemen `a` berikut.

```css
/* link yang belum dibuka */
a:link {
  color: #ff0000;
}

/* link yang pernah dibuka */
a:visited {
  color: #00ff00;
}

/* mouse di atas link */
a:hover {
  color: #ff00ff;
}

/* link yang dipilih */
a:active {
  color: #0000ff;
}
```

Ilustrasi:

![image14](https://user-images.githubusercontent.com/33245436/191110093-a9700e60-ed18-43e6-9b59-f4f4150ef999.png)

![image15](https://user-images.githubusercontent.com/33245436/191110598-fbcff210-3e0d-4820-a6a2-b9afedf2d82f.png)

Pada contoh di bawah, kita akan memilih semua `p` yang merupakan anak pertama dari suatu elemen.

```css
p:first-child {
  color: blue;
}
```

```html
<!DOCTYPE html>
<html>
 <head>
   <link rel="stylesheet" href="style.css" />
 </head>
 <body>
   <div>
    <p>Hello World!</p>
    <p>Paragraf ini tidak terdampak.</p>
    <section>
      <p>Namun paragraf ini terdampak.</p>
    </section>
  </div>
  <p>Ini juga tidak terdampak.</p>
 </body>
</html>
```

Ilustrasi:

![image16](https://user-images.githubusercontent.com/33245436/191110843-c46e71d2-07cf-4e23-946c-51ea5c36641b.png)

### Pseudo-element Selector (::)

Pseudo-element digunakan untuk styling bagian tertentu dari sebuah elemen. Contohnya: styling huruf pertama, baris pertama dari suatu elemen, dan memasukkan sebuah konten sebelum atau sesudah suatu elemen.

1. ::first-line <br/>
   Untuk menambahkan style ke baris pertama sebuah elemen.

   ```css
   p::first-line {
     color: #ff0000;
     font-variant: small-caps;
   }
   ```

2. ::first-letter <br/>
   Untuk menambahkan style ke huruf pertama sebuah elemen

   ```css
   p::first-letter {
     color: #ff0000;
     font-size: xx-large;
   }
   ```

3. ::before <br/>
   Untuk insert sebuah content sebelum content di dalam sebuah elemen

   ```css
   h1::before {
     content: url(https://upload.wikimedia.org/wikipedia/commons/0/03/Smiley.jpg?20070707194955);
   }
   ```

Ilustrasi:

![image17](https://user-images.githubusercontent.com/33245436/191111658-f7aef3f9-8022-4c6f-9ddb-84aaa7a57e71.png)

### Attribute Selector

Untuk memilih elemen HTML yang mempunyai atribut tertentu. Berikut beberapa jenis attribute selector.

1. CSS \[attribute] Selector <br/>
   Pada contoh di bawah, akan memilih elemen `a` yang mempunyai atribut `target`. Atribut ini dipakai untuk menspesifikan apa yang akan terjadi jika elemen `a` di-klik.

   ```css
   a[target] {
     background-color: red;
   }
   ```

2. CSS \[attribute="value"] Selector <br/>
   Pada contoh di bawah, akan memilih elemen `a` yang mempunyai atribut `target` dan nilai “\_blank”

   ```css
   a[target="_blank"] {
     background-color: yellow;
   }
   ```

3. CSS \[attribute~="value"] Selector <br/>
   [attribute~="value"] selector digunakan untuk memilih elemen dengan nilai atribut mengandung suatu kata. Pada contoh di bawah, akan memilih elemen dengan atribut `title` dan nilai yang mengandung “flower”

   ```css
   [title~="flower"] {
     border: 5px solid blue;
   }
   ```

Ilustrasi:

![image18](https://user-images.githubusercontent.com/33245436/191112241-d8f5b893-eeec-47d5-9f3f-2206de17772c.png)

## Property dan Value

Ingat, apa itu property / properti dan value / nilai dengan melihat sintaks CSS di bawah ini.

![image19](https://user-images.githubusercontent.com/68275535/130475766-8e0e2807-ab77-4b15-adc2-74fd92719117.png)

CSS mempunyai beragam properti, di sini akan dijelaskan beberapa contoh untuk memahami dasarnya. Contoh properti di CSS, yaitu: Colors, Backgrounds, Borders, Margins, Padding, Height, Width, Outline, dan masih banyak lainnya.

### Colors

Nilai dari properti colors bisa berupa:

- nama warna (`red`, `green`, `black`, `violet`, dll)
- hex (`#ff0000` atau `#f00`)
- `rgb(255,0,0)`
- `rgb(100%,0%,0%)`

**Background Color**

```html
<h1 style="background-color:DodgerBlue;">Hello World</h1>
<p style="background-color:Tomato;">Lorem ipsum...</p>
```

Ilustrasi:

![image20](https://user-images.githubusercontent.com/68275535/130476063-e2c6effd-370c-440b-9e80-2906b48f5502.png)

**Text Color**

```html
<h1 style="color:Tomato;">Hello World</h1>
<p style="color:DodgerBlue;">Lorem ipsum...</p>
<p style="color:MediumSeaGreen;">Ut wisi enim...</p>
```

Ilustrasi:

![image21](https://user-images.githubusercontent.com/68275535/130476132-54e0010f-853f-4a84-a368-93caff0815f7.png)

### Box Model

Setiap elemen HTML dapat mempunyai properti Margin, Border, dan Padding. Gabungan dari margin, border, padding, dan content dinamakan Box Model. **Margin** adalah properti yang digunakan untuk mendefinisikan ruangan di sekeliling elemen, yang berada diluar border. Sedangkan **Padding** adalah properti yang digunakan untuk mendefinisikan ruangan di sekeliling elemen, yang berada di dalam border.

![image22](https://user-images.githubusercontent.com/68275535/130476218-d8c1b98d-1af8-4e64-ac0c-8a8186c9143a.png)

Contoh:

```css
p {
  margin: 25px 50px 75px 100px; /* top right bottom left */
  padding: 20px; /* Nilai dari semua sisi sama besar */
}
```

Selain dua properti diatas, CSS memiliki banyak properti dan cara menulis nilai yang beragam. Kalian dapat mempelajarinya lebih lanjut di https://www.w3schools.com/css/default.asp

## Specificity

CSS Specificity menentukan seberapa spesifik sebuah aturan pada CSS. Jika ada 2 atau lebih aturan pada sebuah elemen yang sama, maka aturan paling spesifik lah yang akan dipakai oleh browser.

Berikut hierarki atau urutan Specificity dari yang paling utama:

1. Inline styles
2. ID
3. Classes, attributes, dan pseudo-classes
4. Elements dan pseudo-elements

Jadi jika ada 2 style yang dituju pada elemen `a` seperti contoh di bawah, maka hierarki yang lebih tinggi yang akan menang (elemen `a` akan berwarna hijau)

```html
<div class="container">
  <div id="main">
    <p>
      <a href="#" id="id1" class="class1">Link</a>
    </p>
  </div>
</div>
```

```css
#id1 {
  color: green;
}

.class1 {
  color: yellow;
}
```

**Menghitung Specificity**

Specificity bisa dihitung skornya, dan yang lebih tinggi skornya maka dialah yang lebih kuat aturan CSS-nya. Cara menghitungnya: mulai dari 0; tambahkan 1000 untuk atribut `style`; tambahkan 100 untuk setiap `ID`; tambahkan 10 untuk setiap atribut, kelas, atau pseudo-class; tambahkan 1 untuk setiap nama elemen atau pseudo-element.

Contoh:

```
A: h1 { … }
B: #content h1 { … }
C: <div id="content"><h1 style="color: #ffffff">Heading</h1></div>
```

Specificity A adalah 1 (1 elemen)
Specificity B adalah 101 (1 ID, 1 elemen)
Specificity C adalah 1000 (inline styling)

Karena 1 < 101 < 1000, maka C mempunyai specificity yang paling besar, sehingga style itulah yang akan dipakai.

## Referensi

- https://www.w3schools.com/
- https://github.com/minons1/PelatihanSoftwareHouseHMTCITS/wiki/CSS
- http://dev.bertzzie.com/knowledge/desain-web-dasar/HTMLdanCSSDasar.html
- http://dev.bertzzie.com/knowledge/desain-web-dasar/Layout.html#
- https://gawibowo.com/css-specificity.htm
