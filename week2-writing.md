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

## Data Types

<b> Apa yang dimaksud dengan Data Types? </b>

Semua bahasa pemrograman memiliki data structure bawaan, tetapi hal berbeda dari satu bahasa ke bahasa lainnya. Saya akan mencoba menjelaskan struktur data bawaan yang tersedia di JavaScript dan properti apa yang mereka miliki.

- <b> Strings </b>

String berguna untuk menampung data yang dapat direpresentasikan dalam bentuk teks. Beberapa operasi yang paling sering digunakan pada string adalah memeriksa panjangnya, membangun dan menggabungkannya menggunakan operator string + dan +=, memeriksa keberadaan atau lokasi substring dengan metode indexOf(), atau mengekstrak substring dengan substring () method

Cara pendeklarasian string bisa menggunakan cara berikut

```
const string1 = "A string primitive";
const string2 = 'Also a string primitive';
const string3 = `Yet another string primitive`;
```

bisa juga dideklarasikan sebagai Object menggunakan konstruktor String()

```
const string4 = new String("A String object");
```

- <b> Number </b>

Number adalah object wrapper primitif yang digunakan untuk mewakili dan memanipulasi angka seperti 37 atau -9,25.
Konstruktor Number berisi constants dan method untuk bekerja dengan angka. Nilai dari tipe lain dapat dikonversi ke angka menggunakan fungsi Number().

Begini cara kerja pengintepretasian Number

```
123; // one-hundred twenty-three
123.0; // same
123 === 123.0; // true
```

ketika digunakan dengan fungsi, Number(value) merubah string atau tipe lain menjadi tipe Number. Jika tidak bisa dikonversi outputnya akan menjadi NaN.
When used as a function, Number(value) converts a string or other value to the Number type. If the value can't be converted, it returns NaN.

```
Number("123"); // returns the number 123
Number("123") === 123; // true

Number("unicorn"); // NaN
Number(undefined); // NaN
```

- <b> Math </b>

Math adalah object bawaan JS yang memiliki properti dan metode untuk constant dan fungsi matematika. Ini bukan objek fungsi.
Matematika bekerja dengan data type <b> Number </b>. Ini tidak bekerja dengan BigInt.

Beberapa contoh fungsinya:
```
Math.pow()
Returns base x to the exponent power y (that is, xy).

Math.random()
Returns a pseudo-random number between 0 and 1.

Math.round()
Returns the value of the number x rounded to the nearest integer.

Math.sign()
Returns the sign of the x, indicating whether x is positive, negative, or zero.

Math.sin()
Returns the sine of x.

Math.sinh()
Returns the hyperbolic sine of x.

Math.sqrt()
Returns the positive square root of x.

Math.tan()
Returns the tangent of x.

Math.tanh()
Returns the hyperbolic tangent of x.

Math.trunc()
Returns the integer portion of x, removing any fractional digits.
```
Contoh 
