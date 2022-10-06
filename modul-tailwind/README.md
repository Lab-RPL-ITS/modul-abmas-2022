# Tailwind 

# Table of contents

- [Table of contents](#table-of-contents)
- [Persiapan](#persiapan)
- [Intro](#intro)
  - [Requirement](#requirement)
  - [Tailwind Documentation](#tailwind-documentation)

- [Setup](#setup)
  - [Instalation](#installation)

- [Tailwind Concepts](#tailwind-concepts)
  - [Utility-First Fundamental](#utility-first-fundamental)
  - [Basic CSS with Tailwind](#basic-css-with-tailwind)
    - [CSS Syntax vs Tailwind Utility](#css-syntax-vs-tailwind-utility)
    - [Box Model](#box-model)
    - [Color](#css)
    - [Typography](#typography)
    - [display](#display)
    - [Arbitary Value](#arbitary-value)
    - [Arbitary Variant](#arbitary-variant)
  - [States Styling (Hover, Focus, Active, etc)](#state-styling-(hover,-focus,active,-etc))
  - [Reusing Style](#reusing-style)
  - [Tailwind Directives](#tailwind-directives)
    - [@tailwind](#tailwind)
    - [@layer](#layer)
    - [@apply](#apply)


- [Referensi](#referensi)

# Persiapan

Sebelum memulai materi, terdapat beberapa hal yang perlu dipersiapkan:

1. Web Browser <br/>
   Contoh: Google Chrome (recommended), Mozilla Firefox, Microsoft Edge, atau Safari.
2. Text Editor <br/>
   Contoh: [Visual Studio Code](https://code.visualstudio.com/download) (recommended), Sublime Text, Atom, [Notepad++](https://notepad-plus-plus.org/downloads/v8.4.5/), atau Notepad.
3. Koneksi Internet <br/>

# Intro

Apa itu Tailwind? 
> ### Rapidly build modern websites without ever leaving your HTML. 
> A utility-first CSS framework packed with classes like flex, pt-4, text-center and rotate-90 that can be composed to build any design, directly in your markup 
>
>~ [tailwindcss.com](https://tailwindcss.com/)

 
Tailwind CSS merupakan sebuah *utility-first CSS framework*. Tailwind dapat diibaratkan sebagai kerangka kerja yang akan memudahkan penggunanya dalam melakukan *styling* pada web dengan menggunakan CSS.

<!-- # css. -->


Tailwind akan menyediakan `class` utilitas yang dapat kita gunakan langsung dari HTML seperti class `pt-3` untuk menambahkan padding sebesar 16px, `text-center` untuk membuat teks rata tengah (justify) dan masih banyak class-class utilitas lainnya.

Dengan memanfaat class-class utitlitas dari Tailwind kita dapat dengan mudah melakukan *styling* langsung dari file HTML tanpa harus berpindah-pindah antara file HTML dengan file CSS.

## Requirement

Sebelum mempelajari course Tailwind ini, kamu diharapkan memahami dasar materi di bawah:
- HTML
- CSS

## Tailwind Documentation

Sebelum mulai untuk menggunakan Tailwind, kita harus mengenal dokumentasi milik Tailwind terlebih dahulu. Dokumentasi Tailwind ini digunakan sebagai panduan oleh karena itu dalam penggunaannya kita akan sering melibatkan dokumentasi Tailwind tersebut. <br>
Dokumentasi tailwind dapat di akses pada website resmi Tailwind https://tailwindcss.com/docs 
<br><br><br>

# Setup
## Installation
Setidaknya terdapat 4 cara/panduan utama dalam untuk melakukan instalasi tailwind:
1. Tailwind CLI (Command Line Interface)
2. Play CDN (content delivery network)
3. Menggunakan PostCSS
4. Mengikuti Panduan untuk suatu Framework tertentu

Dalam kesempatan kali ini, kita akan menggunakan cara yang paling mudah dan cepat untuk dilakukan yaitu dengan Tailwind Play CDN.

- #### Play CDN [(⊙_⊙;)](https://tailwindcss.com/docs/installation/play-cdn)

Untuk mempermudah penggunaan Tailwind, sangat direkomendasikan untuk menggunakan *extension* [Tailwind CSS IntelliSense](https://marketplace.visualstudio.com/items?itemName=bradlc.vscode-tailwindcss) (untuk vscode)
Untuk mengaktifkan intellisense jika menggunakan play cdn, silahkan tambahakan file dengan nama `tailwind.config.js` pada folder project. 

<br><br><br>
# Tailwind Concepts
## Utility-First Fundamental
Sejauh ini kita telah belajar mengenai HTML serta melakukan styling menggunakan CSS. Dalam menggunakan CSS kita biasanya mulai dengan memberikan class pada suatu tag HTML, lalu melakukan styling untuk class tersebut pada file CSS lain.
seperti berikut 
``` html
    <div class="chat-notification">
        <div class="chat-notification-logo-wrapper">
          <img class="chat-notification-logo" src="https://png.pngitem.com/pimgs/s/34-349739_chat-png-icon-free-download-searchpng-transparent-chat.png" alt="ChitChat Logo">
        </div>
        <div class="chat-notification-content">
          <h4 class="chat-notification-title">ChitChat</h4>
          <p class="chat-notification-message">You have a new message!</p>
          <p>without Tailwind</p>
        </div>
    </div>
      
    <style>
        .chat-notification {
          display: flex;
          max-width: 24rem;
          margin: 0 auto;
          padding: 1.5rem;
          border-radius: 0.5rem;
          background-color: #fff;
          box-shadow: 0 20px 25px -5px rgba(0, 0, 0, 0.1), 0 10px 10px -5px rgba(0, 0, 0, 0.04);
        }
        .chat-notification-logo-wrapper {
          flex-shrink: 0;
        }
        .chat-notification-logo {
          height: 3rem;
          width: 3rem;
        }
        .chat-notification-content {
          margin-left: 1.5rem;
          padding-top: 0.25rem;
        }
        .chat-notification-title {
          color: #1a202c;
          font-size: 1.25rem;
          line-height: 1.25;
        }
        .chat-notification-message {
          color: #718096;
          font-size: 1rem;
          line-height: 1.5;
        }
    </style>
```
Namun dengan menggunakan Tailwind kita dapat membuat hal yang serupa dengan memanfaatkan class-class yang telah disediakan oleh Tailwind seperti berikut
```html
<div class="p-6 max-w-sm mx-auto bg-white rounded-xl shadow-lg flex items-center space-x-4">
  <div class="shrink-0">
    <img class="h-12 w-12" src="https://png.pngitem.com/pimgs/s/34-349739_chat-png-icon-free-download-searchpng-transparent-chat.png" alt="ChitChat Logo">
  </div>
  <div>
    <div class="text-xl font-medium text-black">ChitChat</div>
    <p class="text-slate-500">You have a new message!</p>
    <p>with Tailwind</p>
  </div>
</div>
```

![image](https://user-images.githubusercontent.com/70748569/181674826-cb6ec486-bcc9-457a-944c-30038ee25404.png)

Dengan *utility-first* frameworks (dalam hal ini: Tailwind) yang menyediakan low-level class seperti margin, padding, color dll. kita dapat mengkostumisasi design web yang kita inginkan dengan lebih leluasa langsung dari file HTML.

### Kenapa pakai Inline-style css saja ?
Penggunaan class styling memiliki banyak kelebihan dari pada penggunaan inline-styling, diantaranya sebagai berikut:
- class dapat menggunakan media-query
- class membatasi pengulangan CSS
- class dapat mencakup beberapa properti sekaligus.
- class mendukung pseudo selectors dan pseudo elements dll.
- class dapat menentukan keyframes untuk animasi
- class (stylesheet) dapat diproses dengan Post-CSS, SASS, dll. 
- class utilitas tidak mengembangkan CSS Anda dari waktu ke waktu. Jauh lebih mudah untuk mempertahankan.
- class dapat diterapkan ke HTML baru di WYSIWYGs (What-You-See-Is-What-You-Get).
- class utilitas lebih mudah didokumentasikan dan dipelajari.
- bisa mendapatkan auto-complete untuk menemukan apa yang dibutuhkan dan kesalahan jika ada sesuatu yang salah.
- dengan class tailwind kita bisa mendapatkan penggunaan property dan value yan tepat.

## Basic CSS with Tailwind
### CSS Syntax vs Tailwind Utility
Pada penulisan syntax CSS kita mengenal tentang `selector`, `property`, dan `value`

![image](https://user-images.githubusercontent.com/70748569/181472135-cd5da443-b710-455b-9aab-fbc394a02acb.png)
```html
    <h1 class="big-text">Hello World</h1>
      
    <style>
        .big-text {
            font-size: 20px;
        }
    </style>
```
Tidak jauh berbeda, utility class yang telah disediakan oleh Tailwind juga memiliki pola yang cukup mirip. Secara umum bagian pertama pada class merujuk pada property CSS yang akan digunakan selanjutnya diikuti dengan value dari property yang diinginkan.
```html
    <h1 class="text-xl">Hello World</h1>
```
`text` merujuk pada property untuk font, `xl` menunjukan 2 hal, yaitu (1) property yang akan diubah merupakan *size* dari font, (2) dan besarnya adalah xl = 1.25rem = 20px sesuai pada dekumentasi Tailwind [berikut](https://tailwindcss.com/docs/font-size#setting-the-font-size).

#### Box Model
Kita telah mempelajari dalam memberikan *styling* pada Boxmodel terdapat beberapa property yang dapat kita gunakan yaitu Margin, Border, Padding, dan Content dari tag HTML itu sediri


![image](https://user-images.githubusercontent.com/68275535/130476218-d8c1b98d-1af8-4e64-ac0c-8a8186c9143a.png)

1. Margin [(☞ﾟヮﾟ)☞](https://tailwindcss.com/docs/margin)

| Tailwind   | CSS        | Description  |
| ---------- |:----------| -----------|
| m-0       | margin: 0px;   | memberikan margin dari seluruh arah(atas, kanan, bawah, kiri)            |
| mx-0    |     margin-left: 0px; <br>margin-right: 0px;    |  memberikan margin secara horizontal          |
|      my-0      |margin-top: 0px; <br> margin-bottom: 0px;            |    memberikan margin secara vertical         |
|  mt-0          |   margin-top: 0px         |       Memberikan margin dari satu arah tertentu      |
|  mb-0          |   margin-bottom: 0px         |     -        |
|  mr-0          |   margin-right: 0px          |      -       |
|  ml-0          |   margin-left: 0px          |        -     |




2. Padding [(☞ﾟヮﾟ)☞](https://tailwindcss.com/docs/padding)

| Tailwind   | CSS        | Description  |
| ---------- |:----------| -----------|
| p-0       | padding: 0px;   | memberikan padding dari seluruh arah(atas, kanan, bawah, kiri)            |
| px-0    |     padding-left: 0px; <br>padding-right: 0px;    |  memberikan padding secara horizontal          |
| py-0      |padding-top: 0px; <br> padding-bottom: 0px;            |    memberikan padding secara vertical         |
| pt-0          |   padding-top: 0px         |       Memberikan padding dari satu arah tertentu      |
| pb-0          |   padding-bottom: 0px         |     -        |
| pr-0          |   padding-right: 0px          |      -       |
| pl-0          |   padding-left: 0px          |        -     |

Berikut contoh implementasinya

![image](https://user-images.githubusercontent.com/70748569/181518177-51241529-e66a-496d-abcc-b6ff12482c98.png)

```html
    <div class="pt-6 ...">pt-6</div>
    <div class="px-8 ...">px-8</div>
    <div class="py-8 ...">py-8</div>
    <div class="p-8 ...">p-8</div>
```

3. Border [(☞ﾟヮﾟ)☞](https://tailwindcss.com/docs/border-width)

Untuk informasi lebih lengkap mengenai property/value lainnya yang tersedia silahkan melihat dokumentasi Tailwind yang telah tersedia.
<br>
#### Color [(☞ﾟヮﾟ)☞](https://tailwindcss.com/docs/customizing-colors)
Dengan tailwind kita dapat memberikan warna pada suatu property layaknya saat menggunakan CSS seperti biasannya. Untuk menambahkan warna pada suatu property kita hanya perlu menuliskan nama warna tersebut dan tingkat kepekatan warna.

```html
    <h1 class="text-blue-500 bg-teal-200/80">Ini Warna Biru</h1>
```

![image](https://user-images.githubusercontent.com/70748569/181491399-14f3b500-baa1-4430-b2c1-0e54a59843dd.png)
- `text, bg` menunjukkan property yang akan diberikan warna
- `blue, teal` menunjukkan nama warna yang akan digunakan
- `500, 200` menunjukkan tingkat kepekatan warna yang digunakan
- `/80` bersifat optional, value ini akan menentukan tingkat opasitas dari warna yang diberikan 

![image](https://user-images.githubusercontent.com/70748569/181488904-e0de49c0-74e4-41c6-820f-4a5930fc9792.png)

Untuk informasi lebih lengkap mengenai property/value lainnya yang tersedia silahkan melihat dokumentasi Tailwind yang telah tersedia.
<br>
#### Typography  [(☞ﾟヮﾟ)☞](https://tailwindcss.com/docs/font-family)
Kita dapat melakukan styling pada jenis/cara penulisan (typography) kita di html dengan Tailwind. Hampir semua jenis styling typography pada css telah dicover pada tailwind css. Berikut jenis styling typography yang akan sering digunakan :
- Font family [▶️](https://tailwindcss.com/docs/font-family), memungkinkan kita mengganti jenis font yang digunakan pada html, bergantung pada jenis font yang telah tersedia atau telah di insert pada web.
```html
<p class="font-sans ">The quick brown fox ...</p>
<p class="font-serif ">The quick brown fox ...</p>
<p class="font-mono ">The quick brown fox ...</p>
```
- Font sizing [▶️](https://tailwindcss.com/docs/font-size), Melakukan perubahan ukuran font sesuai keinginan kita.
```html
<p class="text-sm ">The quick brown fox ...</p>
<p class="text-base ">The quick brown fox ...</p>
<p class="text-lg ">The quick brown fox ...</p>
<p class="text-xl ">The quick brown fox ...</p>
<p class="text-2xl ">The quick brown fox ...</p>
```
- Font weight[▶️](https://tailwindcss.com/docs/font-weight), Melakukan perubahan ketebalan font sesuai keinginan kita.
```html
<p class="font-light ">The quick brown fox ...</p>
<p class="font-normal ">The quick brown fox ...</p>
<p class="font-medium ">The quick brown fox ...</p>
<p class="font-semibold ">The quick brown fox ...</p>
<p class="font-bold ">The quick brown fox ...</p>
```
- Text align[▶️](https://tailwindcss.com/docs/text-align), Melakukan perubahan posisi penulisan teks (aligning)
```html
<p class="text-left ">So I started to walk into the water...</p>
<p class="text-center ">So I started to walk into the water...</p>
<p class="text-right ">So I started to walk into the water...</p>
<p class="text-justify ">So I started to walk into the water...</p>
```
- Text coloring[▶️](https://tailwindcss.com/docs/text-color), Melakukan perubahan warna teks (coloring)
```html
<p class="text-sky-400">The quick brown fox...</p>
<p class="text-black">The quick brown fox...</p>
<p class="text-white">The quick brown fox...</p>
```
Dan masih banyak lagi, untuk lebih lengkapnya bisa di cek pada dokumentasi tailwind pada bagian typograpy.
<br>
#### Display
The display property specifies the display behavior (the type of rendering box) of an element.

In HTML, the default display property value is taken from the HTML specifications or from the browser/user default style sheet. The default value in XML is inline, including SVG elements.
Properti display menentukan perilaku tampilan (tipe kotak rendering) dari suatu elemen.

Dalam HTML, nilai properti display secara default diambil dari spesifikasi tag HTML atau dari stylesheet browser/pengguna. Berikut display yang akan sering ditemukan: 
- inline :  tidak dimulai pada baris baru dan akan mwmiliki lebar/width yang sesuai dengan yang dibutuhkan (fit width), semua property styling height dan width tidak akan berpengaruh. ex: `<span>`, `<em>`, `<i>`
- block	: selalu dimulai pada line baru dan memiliki width yang memenuhi lebar maksimal layar (full width), dapat dipengaruhi dengan styling height atau width. ex: `<div>`, `<p>`, `<h(1-6)>`
- inline-block : tidak dimulai pada line baru, tetapi dapat dipengaruhi dengan styling height atau widht.
[info lanjut](https://www.w3schools.com/cssref/pr_class_display.asp)
<br>
#### Arbitary Value
Dengan Menggunakan Tailwind atau frameworks CSS lainnya, kita akan terbiasa untuk menggunakan default value atau batasan yang telah disediakan framework atau menggunakan custom value yang kita definisikan sendiri. Akan tetapi pada suatu kondisi kita akan mendapatkan kondisi dimana kita perlu keluar dari batasan yang telah didefinisikan framework untuk mendapatkan hasil yang benar-benar spesifik seperti yang kita inginkan. 

Mungkin pada kondisi tersebut kita membutuhkan sesuatu seperti `padding: 25.5px, background-color: #39b2f3`. Hal tersebut mungkin tidak disediak oleh class utlitas default milik Tailwind, akan tetapi Tailwind telah memberikan kita fitur untuk memasukkan nilai sembarang sesuai keinginan kita terhadapa class utilitas yang dimiliki Tailwind yang disebut dengan *arbitrary-value*. 

Hal ini dapat digunakan dengan mudah. Kita cukup menambahkan value yang kita inginkan kedalam *bracket* `[value]` setelah property class yang kita inginkan.
```html
      <div class="p-[25.5px] bg-[#39b2f3]">
        Arbitrary Value
      </div>
```
![image](https://user-images.githubusercontent.com/70748569/181917046-d1b521fd-0c73-44f8-ae2e-8f499f8b3fb2.png)
<br>
#### Arbitary Variant
Jika arbitrary value digunakan untuk membuat custom value, Dengan arbitrary variant kita dapat membuat custom variant untuk dijadikan layaknya kostum selector. Ini merupakan fitur baru yang ditambahkan Tailwind pada update Tailwind 3.1 .

Tidak jauh berbeda, kita hanya perlu menambahakan *bracket* disertai custom property yang akan diberikan. Fitur ini dapat dimanfaatkan membuat custom selector untuk mengimplentasikan class utilitas pada suatu element yang spesifik.
barikut contoh implementasinya

![image](https://user-images.githubusercontent.com/70748569/181918443-64a8319a-6807-4fd4-b0d0-87f4ad26d364.png)

```html
          <div class="mt-3 flex space-x-2 overflow-hidden">
            <img class="rounded-3xl border-4 h-28" src="https://picsum.photos/200/300?avatar=2" alt=""/>
            <img class="rounded-3xl border-4 h-28" src="https://picsum.photos/200/300?avatar=3" alt=""/>
            <img class="rounded-3xl border-4 h-28" src="https://picsum.photos/200/300?avatar=4" alt=""/>
            <img class="rounded-3xl border-4 h-28" src="https://picsum.photos/200/300?avatar=5" alt=""/>
          </div>

```
Bagaiman jika ingin selain element nomor 2 yang terakhir memiliki border dengan warna `teal-400`. Hal ini dapat mudah dilakukan jika kita mengetahui berapa jumlah element yang ada dengan cukup menambahkan styling khusus untuk element tersebut. Tetapi jika jumlah element bersifat dinamis, jumlahnya menjadi tidak menentu, hal ini menjadi sulit untuk dilakukan. Pada kondisi ini arbitrary variant dapat berguna untuk menciptakan selector khusus yang akan merujuk pada element tersebut. 
```html
          <div class="mt-3 flex space-x-2 overflow-hidden [&>:not(:nth-last-child(2))]:border-teal-400">
            <img class="rounded-3xl border-4 h-28" src="https://picsum.photos/200/300?avatar=2" alt=""/>
            <img class="rounded-3xl border-4 h-28" src="https://picsum.photos/200/300?avatar=3" alt=""/>
            <img class="rounded-3xl border-4 h-28" src="https://picsum.photos/200/300?avatar=4" alt=""/>
            <img class="rounded-3xl border-4 h-28" src="https://picsum.photos/200/300?avatar=5" alt=""/>
          </div>

```
![image](https://user-images.githubusercontent.com/70748569/181918812-b7e2ef9c-a3ed-46ce-bc72-115d3e054cae.png)

Pada contoh diatas, kita menambahkan `[&>:not(:nth-last-child(2))]:border-teal-400` pada class milik parent element. 
- `&` merupakan selector yang merujuk pada element utama yang merupakan tempat class ini ditambahkan.
- `>` menunjukkan hubungan antara selector element di sebelah kiri dengan selector elemen disebelah kanan adalah hubungan parent to child (*[parent] > [child]*) 
- `:not()` negasi selector, mengambil "yang bukan"
- `:nth-last-child(2)` selector yang memilih child ke-n dari belakang/terakhir
- `:not(:nth-last-child(2))` = "ambil yang bukan child ke-2 dari belakang"

Dengan begitu element ke-2 dari belakang tidak akan dikenakan styling seperti yang telah kita implementasikan diatas.

untuk informasi mengenai jenis selector, dapat diliat pada link [berikut](https://www.w3schools.com/cssref/css_selectors.asp)

## States Styling (Hover, Focus, Active, etc) [\(￣︶￣*\))](https://tailwindcss.com/docs/hover-focus-and-other-states)
Dalam styling menggunakan CSS kita dapat menggunakan *pseudo-class* seperti:
- `hover`: Kondisi disaat pointer berada di pada element tertentu
- `focus`: Kondisi disaat suatu element dalam keadaan fokus seperti saat mengetik pada element input
- `active`: Kondisi disaat suatu element sedang dalam keadaan aktif, seperti disaat element button ditekan
-dll.

contohnya: 
```CSS
.btn-primary {
  background-color: #white;
  /* ... */
}
.btn-primary:hover {
  background-color: #black;
  transform: scale(1.1);
}
```
Sebelum Hover
<br>

![image](https://user-images.githubusercontent.com/70748569/181544479-e6f0ad30-789e-432d-9738-50c7ee9c1bdc.png)<br>

Setelah di hover <br>
![image](https://user-images.githubusercontent.com/70748569/181545063-57f2999b-fa0c-41c1-b8e0-e158bcb72d07.png)


Tailwind juga mampu mengakomodasi styling dalam kondisi-kondisi tersebut dengan lebih mudah dan simpel. 

Kita hanya perlu menambahkah `hover` atau kondisi lainnya sebagai *prefix* diikuti dengan titik dua (`:`) lalu class utilitas yang ingin kita gunakan pada kondisi tersebut.

```html
<button class="bg-teal-300 hover:bg-sky-600 hover:scale-110 ..."> Button</button> 
```
Dengan begitu kita bisa mendapatkan hasil yang sama dalam kondisi hover. Kita dapat menggunakan utilitas apapun yang memungkinkan seperti mengubah ukuran, jenis/warna teks dll. 

Tidak hanya terbatas pada pseudo-class seperti hover, Tailwind juga dapat mengatasi kondisi-kondisi lain diantaranya:
1. Pseudo-classes, seperti :hover, :focus, :first-child, and :required
2. Pseudo-elements, seperti ::before, ::after, ::placeholder, and ::selection
3. Media queries, seperti *responsive breakpoints*, mode gelap, dan prefers-reduced-motion
4. Attribute selectors, seperti [dir="rtl"] dan [open]

Kita juga dapat menumpuk beberapa kondisi yang memungkinkan untuk kondisi yang lebih spesifik sekaligus seperti berikut:
```html
<button class="md:hover:bg-fuchsia-600 ...">Button</button>
```


# Reusing Style
Dalam melakukan styling tentunya kita akan sering bertemu pada kondisi dimana kita akan menggunakan style yang sama untuk elemen-elemen yang serupa.

![image](https://user-images.githubusercontent.com/70748569/181678313-a7116aba-141a-4a39-9cd8-2df156eed41e.png)
```html
<div>
    <div class="flex items-center space-x-2 text-base">
      <h4 class="font-semibold text-slate-900">Kontributor</h4>
      <span class="rounded-full bg-slate-100 px-2 py-1 text-xs font-semibold text-slate-700">205</span>
    </div>
    <div class="mt-3 flex -space-x-2 overflow-hidden">
      <img class="inline-block h-12 w-12 rounded-full ring-2 ring-white" src="https://picsum.photos/200/300?avatar=2" alt=""/>
      <img class="inline-block h-12 w-12 rounded-full ring-2 ring-white" src="https://picsum.photos/200/300?avatar=3" alt=""/>
      <img class="inline-block h-12 w-12 rounded-full ring-2 ring-white" src="https://picsum.photos/200/300?avatar=4" alt=""/>
      <img class="inline-block h-12 w-12 rounded-full ring-2 ring-white" src="https://picsum.photos/200/300?avatar=5" alt=""/>
    </div>
    <div class="mt-3 text-sm font-medium">
      <a href="#" class="text-teal-500">+ 201 Lainnya</a>
    </div>
</div>
```
Dari contoh di atas dapat dilihat bahwa terjadi banyak pengulangan class
``inline-block h-12 w-12 rounded-full ring-2 ring-white``. Tentunya hal tersebut kurang efisien.
Sebenarnya terdapat beberapa cara untuk mengatasi hal tersebut, seperti menggunakan perluang (looping) dengan memanfaatkan JavaScript, atau kembali membuat CSS class seperti biasanya. Akan tetapi Tailwind punya caranya sendiri.
### Membuat/Mengekstrak Class dengan @apply
Untuk mengatasi masalah diatas Tailwind menyediakan fitur dimana kita dapat membuat class baru dengan tetap menggunakan class utilitas dari Tailwind itu sendiri seperti berikut.
1. Menentukan nama class yang akan kita implementasikan
```html
    <div class="mt-3 flex -space-x-2 overflow-hidden">
      <img class="frame-bulat-bulat" src="https://picsum.photos/200/300?avatar=2" alt=""/>
      <img class="frame-bulat-bulat" src="https://picsum.photos/200/300?avatar=3" alt=""/>
      <img class="frame-bulat-bulat" src="https://picsum.photos/200/300?avatar=4" alt=""/>
      <img class="frame-bulat-bulat" src="https://picsum.photos/200/300?avatar=5" alt=""/>
    </div>
```
disini ``inline-block h-12 w-12 rounded-full ring-2 ring-white`` telah diubah menjadi ``frame-bulat-bulat``. Akan tetapi Tailwind belum memiliki class dengan nama ``frame-bulat-bulat``, oleh karena itu kita akan "mengenalkan" class tersebut kepada Tailwind.

2. Membuat class baru dengan @apply pada layer yang sesai
- Jika menggunakan Play CDN tambahkan class di tag `<style type="text/tailwindcss">` pada `<head>` 
```html
<head>
   <!-- ... -->
    <style type="text/tailwindcss">
        @layer component {
          .frame-bulat-bulat {
            @apply inline-block h-12 w-12 rounded-full ring-2 ring-blue-200;
          }
        }
    </style>
</head>
```
Dengan begitu sekarang Tailwind telah mengenal class `frame-bulat-bulat` sebagai `inline-block h-12 w-12 rounded-full ring-2 ring-white` yang kita letakan pada layer `component`.

<br><br><br>
# Tailwind Directives [ヾ(￣▽￣) ](https://tailwindcss.com/docs/functions-and-directives)
### Directives 
Directives merupakan custom [*at-rules*](https://developer.mozilla.org/en-US/docs/Web/CSS/At-rule) khusus yang dimiliki Tailwind. Tailwind Directives ini memberikan fungsionalitas spesial untuk proyek/web yang menggunakan Tailwind.

> ℹ **at-rules** merupakan salah satu perintah CSS yang memberikan instruksi untuk css dalam berprilaku. At-rules dimulai dengan tanda `@`. <br> 
> contohnya `@media`: sekelompok aturan yang akan diaplikaskan jika perangkat memenuhi kriteria yang didefinisikan dengan *media-query*

Berikut macam-macam Tailwind Directives

## @tailwind
`@tailwind` directive digunakan untuk meng-*insert* styling/rule dari `base`, `componnent`, `utilities` dan `variants` kedalam CSS.   

1. `@tailwind base` memasukkan styling dasar Tailwind dan styling dasar apa pun yang didaftarkan oleh plugin. contohnya pada css reset milik Tailwind, seperti menghilang defaul margini yang dimiliki beberapa tag html berikut. 


```css
blockquote,dl,dd,h1,h2,h3,h4,h5,h6,hr,figure,p,pre 
{
  margin: 0;
}

fieldset {
  margin: 0;
  padding: 0;
}
```

2. `@tailwind components` memasukkan class components Tailwind dan class components apa pun yang didaftarkan oleh plugin. berisi komponent yang berisi sekumpulan class utilitas untuk membuat sebuah kelas komponent CSS tertentu 


3. `@tailwind utilities` memasukkan class utilitas Tailwind dan class utilitas apa pun yang didaftarkan oleh plugin. Disinilah letak semua class utilitas yang kita gunakan untuk seperti `p-2`, `mx-auto`, `rounded-xl` dll.

4. `@tailwind variants` directive ini digunakan untuk mengontrol kondisi seperti hover, focus, responsive, mode gelap, dan varian lain dari setiap kelas. Jika dihilangkan, Tailwind akan menambahkan kelas-kelas ini ke bagian akhir dari stylessheet (file css) secara default.

## @layer
Jika `@tailwind` digunakan untuk memasukkan default styling milik tailwind, `@layer` digunakan untuk memasukkan class kostum milik kita sendiri. Pada saat kita menggunakan `@tailwind base, components, utilities, variants` tiap-tiap directive `@tailwind` telah memiliki *layer*/lapisan sendiri untuk menghindari kesalahan dalam persoalan *specifity*  dimana class yang lebih spesifik akan diutamakan dalam pengimplementasiannya. Secara urutan `base` berada pada layer paling pertama. 
`@layer` digunakan untuk mendefinisikan dimana layer/letak kostum class yang akan dibuat.
berikut contohnya:
```css
@tailwind base;
@tailwind components;
@tailwind utilities;

@layer base {
  h1 {
    @apply text-2xl;
  }
  h2 {
    @apply text-xl;
  }
}

@layer components {
  .btn-blue {
    @apply bg-blue-500 hover:bg-blue-700 text-white font-bold py-2 px-4 rounded;
  }
}

@layer utilities {
  .filter-none {
    filter: none;
  }
  .filter-grayscale {
    filter: grayscale(100%);
  }
}
```

## @apply
Tailwind directives yang terkahir adalah `@apply`. Seperti yang telah kita pelajari pada *Reusing Style*, Tailwind directive ini digunakan untuk membuat kostum css sendiri dengan tetap menggunakan class utilitas milik Tailwind. 
contohnya:
```css
.select2-dropdown {
  @apply rounded-b-lg shadow-md;
}
.select2-search {
  @apply border border-gray-300 rounded;
}
.select2-results__group {
  @apply text-lg font-bold text-gray-900;
}
```
Semua perintah yang dibuat dengan `@apply` tidak akan memiliki `!important` yang biasa digunakan dalam css untuk memakai suatu perintah tanpa memperhatikan *specifity* class tersebut.
```css
/* Input */
.foo {
  color: blue !important;
}

.bar {
  @apply foo;
}

/* Output */
.foo {
  color: blue !important;
}

.bar {
  color: blue;
}
```

Untuk menggunakan perintah `!important` kita hanya perlu menambahakan `!` pada suatu utilitas class yang digunakan, atau menambahkan `!important` di depan kelas-kelas utilitas yang digunakan
```css
/* Input */
.btn {
  @apply font-bold py-2 px-4 rounded !important;
}
.title{
    @apply !font-bold text-center;
}

/* Output */
.btn {
  font-weight: 700 !important;
  padding-top: .5rem !important;
  padding-bottom: .5rem !important;
  padding-right: 1rem !important;
  padding-left: 1rem !important;
  border-radius: .25rem !important;
}
.title{
    font-weight: 700 !important;
    text-align: center;
}

```

<br><br><br>
# Referensi
- https://tailwindcss.com/
https://darkghosthunter.medium.com/tailwind-the-base-the-components-and-the-utilities-a81137c52534
- https://www.w3schools.com/cssref/css_selectors.asp
- https://darkghosthunter.medium.com/tailwind-the-base-the-components-and-the-utilities-a81137c52534
