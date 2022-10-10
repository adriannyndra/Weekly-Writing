<h1> Weekly Recap 3 </h1>

Berikut materi yang telah saya pelajari pada minggu ke-3 (Web Development Advance)

- JavaScript Intermediate
  - Array ( & Array Multidimensional)
  - Objects
  - Recursive
  - Asynchronous ( & Promise)
 - Web Storage
 

## JavaScript Intermediate

<h2> Array's </h2>

Apa itu Array?

Array adalah sebuah <i>list</i> yang dapat menyimpan tipe data apapun di dalamnya. Array dapat menyimpan tipe data String, Number, Boolean, dan lainnya.

- <b> Contoh Array </b>

```
let groceries = [
    'Buku Belajar',
    'Baju',
    'Kopi Sachet'
];
console.log(groceries);
```
Array didefinisikan menggunakan square brackets `[]`

Array pada javascript dihitung dari index data ke-0.

- <b> Update Array </b>

```
let groceries = ['Buku Belajar', 'Baju', 'Kopi Sachet'];
groceries['0'] = 'Celana';
console.log(groceries);
```

- <b> Array Properties </b>

Array Properties adalah fitur built-in dari Javascript untuk memudahkan developer.

- Array memiliki 5 properti yang sering digunakan yaitu:
  - constructor
  - length
  - index
  - input
  - prototype
  
Contoh penggunaan properti '.length':

```
let groceries = ['Buku', 'Sayur', 'Kecap'];
console.log(groceries.length);
// Output: 3
```

- <b> Array Method </b> 

Array JS memiliki method built-in juga untuk memudahkan kita

- Array Built-in Methods memiliki 5 yaitu:
  - .push() menambahkan item array pada urutan yang paling akhir.
  - .pop() menghapus item array index terakhir.
  - .shift() menghapus item Array pada index pertama
  - .unshift() menambahkan item Array pada index pertama
  - .sort() mengurutkan secara Ascending atau Descending Alphanumeric
  
  
-  <b> Looping in Array </b>. 

Array juga memiliki built in methods untuk melakukan looping yaitu .map() dan .forEach()

  - .forEach() adalah method untuk melakukan looping pada setiap elemen array.
  - .map() melakukan perulangan/looping dengan membuat array baru.

 
<h2> Multidimensional Array </h2>


Bisa diartikan dengan array of array atau array didalam array.

- Contoh Multidimensional Array

```
let groceries = [
  ['Indomie', 5],
  ['Telor', 12],
  ['Beras', 24],
  ['Sawi', 8],
];
console.log(groceries);
```

- Akses index Multidimensional Array
```
let groceries = [
  ['Kaos Polos', 10],
  ['Jaket Hoodie', 12],
  ['Topi', 24],
  ['Celana Jeans', 8],
];
console.log(groceries[1][0]);
```

