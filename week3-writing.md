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

- Multidimensional array dapat menggunakan Property dan Method built-in Array.
```
let groceries = [
  ['Kaos Polos', 10],
  ['Jaket Hoodie', 12],
  ['Topi', 24],
  ['Celana Jeans', 8],
];
groceries.push(['Sawi', 7])
console.log(groceries);
```




<h2> Multidimensional Array </h2>

**Apa itu object?** 

Object adalah sebuah tipe data pada variabel yang menyimpan properti dan fungsi (method). Data-data dalam objek disebut **properti** dan aksi dari objek disebut **method**

- Membuat sebuah object sama seperti tipe data sebelumnya. Object dapat diassign kedalam sebuah variabel.
- Contoh object person dengan properti
```
let person = {
  name: 'Belva Aprilliano',
  age: 20,
  isAbove18: true,
};
```

- Mengakses Object dan Property Object
-
```
console.log(namaObjek.namaProperti);
```


- **Bracket Notation**

Kita juga bisa menggunakan bracket notation saat memanggil properti dari sebuah object.

```
let person = {
  name: 'Jokododong',
  age: 25,
  'current address': 'Bekasi, Indonesia',
};
console.log(person['name']);
console.log(person['current address']);
```

- Update Object

Update dapat menambahkan value baru di object

Contoh update data pada object:

```
// update current key dengan new value
person.age = 22;
// Add new key and value
person.telepon = 089646615043;
console.log(person);
```
Update data object harus menggunakan let pada deklarasi variabel

```
};
person = {
  fullname: 'Ahmad Vargandani'
}
console.log(person);
```

- Delete Object Property
 
Menghapus properti dari object menggunakan operator delete.

- Contoh delete property object age dari data people
```
delete people.age;
```

- Looping Object
```
for(let data in news) {
  console.log(news[data]);
};
for(let author in news.author.people) {
  console.log(news.author.people[author]);
}
```

<h2> Recursive </h2>

Recursive adalah function yang memanggil dirinya sendiri sampai kondisi tertentu. Recursive digunakan untuk case matematika, fisika, dan yang berhubungan dengan kalkulasi.

- Struktur recursive
```
function recursive() {
  // ...
  recursive();
  // ...
}
```

Recursive akan berhenti memanggil dirinya sendiri jika kondisi terpenuhi

```
function recursive() {
  if(condition) {
    // stop calling self
    // ...
  } else {
    recursive();
  }
}
```

New Paradigm:
  - procedural
  - conditional
  - looping
  - modular (function)
  - recursive
  
Sifat & Ciri Rekursif:
  - Fungsi rekursif selalu memiliki kondisi yang menyatakan kapan fungsi tersebut berhenti.
  - Fungsi rekursif selalu memanggil dirinya sendiri sambil mengurangi atau memecahkan data masukan setiap panggilannya.

- Contoh kasus rekursif 

Fungsi rekursif menghitung mundur number

```
function countDown(fromNumber) {
  console.log(fromNumber);
  let nextNumber - fromNumber - 1;
  //jika kondisi ini bernilai false maka recursive berhenti
  if (nextNumber > 0) {
    countDown(nextNumber);
  }
}
countDown(3);
```

<h2> Asynchrounous </h2>

Asynchronous mengizinkan komputer memproses task yang lain sambil menunggu proses yang masih berlangsung.

Cara-cara untuk membuat asynchronous:
  - Callback
  - Promises
  - Async/Await
  - 
**Callback** function adalah function yang kita letakan di dalam argumen/parameter pada function, dan function tersebut akan dieksekusi setelah function pertama menyelesaikan tugasnya.

- Contoh Callback

```
const mainFunc = (number1,number2,callBack) => {
  console.log(number1 + number2)
  callBack()
}
const myCallback = () => {
  console.log ('Done !')
}
main(1,2,myCallback) // output 3 Done!
```

Proses asynchronous identik dengan delay, dimana hasil dari proses membutuhkan selang waktu tertentu untuk menghasilkan output. Pada asynchronous kita menggunakan setTimeOut untuk simulasinya. Proses function pada p2 kita lewati sambil menunggu selesai, program lanjut ke function p3

```
const p1 = () => {
  console.log('p1 selesai dijalankan');
};
const p2 = () => {
  setTimeout(() => {
    console.log('p2 selesai dijalankan')
  }, 3000)
};
const p3 = () => {
  p1()
  p2()
  console.log('p3 selesai dijalankan');
};
p3();
```

- **Promises**
- 
Promises  adalah salah satu fitur biasa digunakan untuk melakukan http request/fetch data dari API.

- Dalam pengambilan data, promise memiliki 3 possible state yaitu:
  - Pending (sedang proses)
  - Fulfilled (berhasil)
  - Rejected (gagal)
 
```
const contohPromise = () => {
  new Promise((resolve, rejected) => {
    let condition = true;
    if (condition) {
      resolve('request fulfilled)
    } else {
      reject(new Error('terjadi kesalahan, rejected'))
    }
  }).then(result => console.log(result))
    .catch(error => console.log(error))
}
contohPromise()
```


- **HTTP Request fetch()**

Fetch berguna untuk melakukan HTTP calls dari external network. `fetch()` memiliki parameter utama yaitu URL/endpoint API, dan parameter kedua yaitu options, options ini berisi method, headers dan body.

```
const URL = "https://5e92be81bbff810016969173.mockapi.io/api/v1/users"
const options = {
  method: "GET" / "POST",
  headers: {
    "Content-type": "application/json"
  },
  body: user
}
fetch(URL, options)
```


<h2> Web Storage </h2>

Dalam web storage, aplikasi web dapat menyimpan data secara lokal di machine pengguna

- **HTML Web Storage Objects**

HTML Web Storage menyediakan dua objek untuk menyimpan data pada klien yaitu:
  - ```window.localStorage``` untuk menyimpan data tanpa expiration date
  - ```window.sessionStorage``` untuk menyimpan data per sesi dan hilang saat browser ditutup
  -
Kita harus memeriksa dukungan browser untuk localStorage dan sessionStorage:

```
if (typeof(Storage) !== "undefined") {
  // Code for localStorage/sessionStorage.
} else {
  // No Web Storage Support!
}
```

- **localStorage Object** 

Local Storage Object dapat menyimpan data tanpa tanggal kedaluwarsa. Data tidak akan dihapus saat browser ditutup, dan dapat diakses kapan  pun

```
<!DOCTYPE html>
<html>
<body>
<div id="result"></div>
<script>
// Check browser support
if (typeof(Storage) !== "undefined") {
  // Store
  localStorage.setItem("lastname", "Smith");
  // Retrieve
  document.getElementById("result").innerHTML = localStorage.getItem("lastname");
} else {
  document.getElementById("result").innerHTML = "Sorry, your browser does not support Web Storage...";
}
</script>
</body>
</html>
```

Syntax untuk menghapus item localStorage "lastname" adalah sebagai berikut:

```
localStorage.removeItem("lastname");
```

- **sessionStorage Object** 

mirip dengan objek localStorage, kecuali objek tersebut menyimpan data hanya untuk satu sesi. Data dihapus ketika pengguna menutup tab browser tertentu.

- Contoh ini menghitung berapa kali tpmbol di klik sesi saat ini:

```
<!DOCTYPE html>
<html>
<head>
<script>
function clickCounter() {
  if (typeof(Storage) !== "undefined") {
    if (sessionStorage.clickcount) {
      sessionStorage.clickcount = Number(sessionStorage.clickcount)+1;
    } else {
      sessionStorage.clickcount = 1;
    }
    document.getElementById("result").innerHTML = "You have clicked the button " + sessionStorage.clickcount + " time(s) in this session.";
  } else {
    document.getElementById("result").innerHTML = "Sorry, your browser does not support web storage...";
  }
}
</script>
</head>
<body>
<p><button onclick="clickCounter()" type="button">Click me!</button></p>
<div id="result"></div>
<p>Click the button to see the counter increase.</p>
<p>Close the browser tab (or window), and try again, and the counter is reset.</p>
</body>
</html>
```
