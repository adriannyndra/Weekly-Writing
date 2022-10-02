<h1> Weekly Recap 2 </h1>

Berikut materi yang telah saya pelajari pada minggu ke-2 Web Dev Basic

- Javascript Scope & Function
- Data Type Built in Prototype & Method
- DOM
  - Selecting Elements
  - Traversing Elements
  - Manipulating Elements
  - Manipulating Styles


## Javascript Scope

- <b> Scope </b>

Scope adalah konsep dalam flow data variabel.  Menentukan suatu variabel bisa diakses pada scope tertentu atau tidak.
Scope mengacu pada konteks kode, yang menentukan aksesibilitas variabel dalam JavaScript.

- <b> Blocks </b>

Blocks adalah code yang berada didalam curly braces {}.
Conditional, function, dan  looping semua termasuk blocks.

- <b> Local & Global Scope </b>

<b> Local </b> scope berarti kita mendeklarasikan variabel didalam blocks seperti function, conditional, dan looping.
Maka variabel hanya bisa diakses didalam blocks saja. Tidak bisa diakses diluar block.

<img src="pics\local.jpg">

Pada gambar diatas variabel myName terdeklarasikan secara Lokal

<b> Global </b> scope berarti variabel yang kita buat dapat diakses dimanapun dalam suatu file.
Agar menjadi Global Scope, suatu variabel harus dideklarasikan diluar Blocks.

<img src="pics\global.jpg">

Pada contoh gambar diatas, pendeklarasian variabel bersifat Global karena diluar block of code (function)

## Javascript Function

<b> Apa itu Function? </b>

Function adalah sebuah blok kode dalam sebuah grup untuk menyelesaikan 1 task/1 fitur.
Saat kita membutuhkan block of code/melakukan task tersebut nantinya, kita bisa kembali menggunakannya.

<b> Bagaimana cara membuat Function? </b>

<img src="pics\kerangkafunction.jpg">

Gambar diatas menunjukan bagaimana struktur sintaks kerangka function, mulai dari <b> function keyword </b> untuk menandakan pembuatan sebuah function, 
<b> identifier </b> untuk menamakan function tersebut dan block of code yang akan dijalankan di tengah tengah <b> opening & closing bracket </b>

Ada juga cara lain yaitu dengan cara <b> Arrow Function </b>, apa itu? <b> Arrow function </b> adalah cara lain menuliskan function. Ini adalah fitur terbaru yang ada pada ES6 (Javascript Version) contohnya seperti gambar dibawah ini

![image](https://user-images.githubusercontent.com/114375139/193453501-3df13335-3baa-4cc8-86f2-6fae0e12f3dd.png)

Apakah wajib harus menggunakan return pada akhir function? Jadi return sendiri berfungsi untuk mengembalikan sebuah nilai, berbeda dengan console.log berfungsi untuk mencetak nilai ke terminal/console. Jadi jika kita ingin mengembalikan sebuah nilai, kita bisa memakai return.


<b> Bagaimana cara memanggil Function? </b>

<img src="pics\panggilfunction.jpg">

Bisa dilihat dari gambar diatas, pemanggilan function bisa dilakukan dengan menulis kembali nama (identifier) function tersebut dan menambahkan kurung buka dan tutup. Untuk menampilkan output dari function lewat console.log bisa dilakukan seperti contoh diatas.

<b> Bagaimana cara kerja Parameter & Arguments? </b>

<img src="pics\parameters.jpg">

Parameter fungsi tercantum di dalam tanda kurung () dalam definisi fungsi.
Argumen adalah nilai yang diterima oleh fungsi saat dipanggil.
Di dalam fungsi, argumen (parameter) berperilaku sebagai variabel lokal.
