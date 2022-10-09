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

Math.sqrt()
Returns the positive square root of x.

Math.tan()
Returns the tangent of x.

```

dan masih banyak lagi.

Contoh penggunaannya:

```
function random(min, max) {
  const num = Math.floor(Math.random() * (max - min + 1)) + min;
  return num;
}

random(1, 10);
```

code diatas mengembalikan random integer dari dua batas (minimum dan maksimum) menggunakan math.floor dan math.random

- <b> Primitive & Non-Primitive </b>
  
Apa yang dimaksud dengan tipe data primitif dan non primitif? Kedua kategori ini mewakili dua cara berbeda tipe data ini disimpan ke dalam memori. Primitif disimpan berdasarkan nilai sedangkan Non-Primitif (Objek) disimpan berdasarkan referensi.
  
- Primitive

  Numbers,
  Strings,
  Booleans,
  undefined,
  null,
  
- Non-Primitive (referred to collectively as Objects)

  Objects,
  Arrays,
  Functions
  
## DOM (Document Object Model)
  
DOM merupakan singkatan dari Document Object Model. Artinya, dokumen (HTML) yang dimodelkan dalam sebuah objek. Objek dari dokumen ini menyediakan sekumpulan fungsi dan atribut/data yang bisa kita manfaatkan dalam membuat program Javascript. Inilah yang disebut API (Application Programming Interface).

<b> Bagaimana cara menggunakan DOM? </b>

Objek DOM di javascript bernama document. Objek ini berisi segala hal yang kita butuhkan untuk memanipulasi HTML.
Jika kita coba ketik document pada console Javascript, maka yang akan tampil adalah kode HTML.

![image](https://user-images.githubusercontent.com/114375139/193537785-6877f126-98e4-46c2-b705-1082827860b3.png)

Di dalam objek document, terdapat fungsi-fungsi dan atribut yang bisa kita gunakan untuk memanipulasi dokumen HTML.
Sebagai contoh fungsi `documen.write()`
Fungsi ini digunakan untuk menulis sesuatu ke dokumen HTML. Contohnya seperti:

```
document.write("Hello World");
document.write("<h2>Saya Sedang Belajar Javascript</h2>");
```

Hasilnya: <br>

![image](https://user-images.githubusercontent.com/114375139/193538683-0cd9ff0e-08cc-47b3-b618-335d38949126.png)

<b> Mengakses Elemen tertentu dengan DOM </b>

Objek document adalah model dari dokumen HTML. Objek ini berisi kumpulan fungsi dan atribut berupa objek dari elemen HTML yang bisa digambarkan dalam bentuk pohon seperti ini:

![image](https://user-images.githubusercontent.com/114375139/193539088-8ecfd619-10ca-42c8-82a3-4fe91482f69e.png)

Struktur pohon ini akan memudahkan kita dalam menggunakan elemen tertentu.
Contoh jika ingin mengakses objek <head> dan <body>:
  
```
  // mengakses objek head
document.head;

// mengakses objek body
document.body;

// melihat panakang judul pada objek title
document.title.length
```
  
Kita juga dapat mengakses elemen spesifik dengan cara-cara berikut:
  
```
getElementById() fungsi untuk memilih elemen berdasarkan atribut id.
  
getElementByName() fungsi untuk memilih elemen berdasarkan atribut name.
  
getElementByClassName() fungsi untuk memilih elemen berdasarkan atribut class.
 
getElementByTagName() fungsi untuk memilih elemen berdasarkan nama tag.
  
getElementByTagNameNS() fungsi untuk memilih elemen berdasarkan nama tag.
  
querySelector() fungsi untuk memilih elemen berdasarkan query.
  
querySelectorAll() fungsi untuk memilih elemen berdasarkan query.
  
dan lain-lain.
```
  
  <b> Manipulating Styles </b>

Kita juga dapat merubah style pada html seperti layaknya css, menggunakan javascript.
  
```
paragraf[0].style.color = "red"
```

Hasilnya seperti ini:
  
![image](https://user-images.githubusercontent.com/114375139/193541257-edc06228-fe51-40cd-86db-1fc172343179.png)
  
  
  <b> Traversing Elements </b>
  
Developer JavaScript yang baik perlu mengetahui cara traversing DOM, ini adalah tindakan dimana kita dapat memilih elemen dari elemen lain.

  - <b> Traversing Downwards </b>

Ada dua cara untuk traversal downwards

  - `QuerySelector` atau `querySelectorAll`
  - `children`

Contoh Analogi mencari ruangan dalam rumah, lebih cepat seperti ini daripada mencari ruangan dari luar rumah(the document):
  
```
<div class="component">
  <h2 class="component__title">Component title</h2>
</div>
```

```
const component = document.querySelector('.component')
const title = component.querySelector('.component__title')

console.log(title) // <h2 class="component__title"> ... </h2>
```
  
  
  <b> Traversing Upwards </b>
  
Seperti Downwards, upwards juga memiliki 2 metode

- `parentElement`
- `closest`

parentElement adalah property yang bisa memilih sebuah Parent element, parent element adalah element yang memiliki/menutupi current element, contoh:
  
```
const component = document.querySelector('.component')
const title = component.querySelector('.component__title')

console.log(title) // <h2 class="component__title"> ... </h2>
```

```
const firstListItem = document.querySelector('li')
const list = firstListItem.parentElement

console.log(list)
// <ul class="list">...</ul>
```

