<h1> Weekly Report 6 (Week 1 Back-End Bootcamp) </h1>

<h2> <b>Web Server & RESTful API</b> </h2>

<b> Apa itu web server?</b>


Web server adalah sebuah software (perangkat lunak) yang memberikan layanan berupa data. Berfungsi untuk menerima permintaan HTTP atau HTTPS dari klien atau kita kenal dengan web browser (Chrome, Firefox). Selanjutnya ia akan mengirimkan respon atas permintaan tersebut kepada client dalam bentuk halaman web. Web Server dapat dibagi menjadi 2 komponen yaitu <b> Hardware </b> dan <b> Software </b>

<b>Hardware</b> dari Web Server dapat dibilang komputer yang menyimpan perangkat lunak server web dan file komponen situs web. Server web terhubung ke Internet dan mendukung pertukaran data fisik dengan perangkat lain yang terhubung ke web.

<b>Software</b> dari server web mencakup beberapa bagian yang mengontrol bagaimana pengguna web mengakses file yang dihosting. ini adalah server HTTP. Server HTTP termasuk software yang memahami URL dan HTT. Server HTTP dapat diakses melalui nama domain situs web
, dan mengirimkan konten situs web yang dihosting ini ke perangkat pengguna akhir.


**Static Web Server**

Server web statis, atau tumpukan, terdiri dari komputer (perangkat keras) dengan server HTTP (perangkat lunak). Kami menyebutnya "statis" karena server mengirimkan file yang dihosting apa adanya ke browser Anda.

**Dynamic Web Server**

Sebuah server web dinamis terdiri dari server web statis ditambah software tambahan, paling sering server aplikasi dan database. Kami menyebutnya "dinamis" karena server aplikasi memperbarui file yang dihosting sebelum mengirim konten ke browser melalui server HTTP.

**Server Side Programming**
- Web Server menunggu pesan permintaan klien, memprosesnya saat tiba, dan membalas browser web dengan pesan respons HTTP. Respons berisi baris status yang menunjukkan apakah permintaan berhasil atau tidak (mis. "HTTP/1.1 200 OK" untuk berhasil).
  - **Static Sites**: situs yang mengembalikan konten hard-coded yang sama dari server setiap kali sumber daya tertentu diminta). Saat pengguna ingin menavigasi ke halaman, browser mengirimkan permintaan "GET" HTTP yang menentukan URL-nya.
  - **Dynamic Site**: situs di mana beberapa konten respons dihasilkan secara dinamis, hanya bila diperlukan. Di situs web dinamis, halaman HTML biasanya dibuat dengan memasukkan data dari database ke dalam placeholder di template HTML (ini adalah cara yang jauh lebih efisien untuk menyimpan konten dalam jumlah besar daripada menggunakan situs web statis).

**Apa itu REST?**

REST, atau Representational State Transfer, adalah gaya arsitektur untuk menyediakan standar antara sistem komputer di web, sehingga memudahkan sistem untuk berkomunikasi satu sama lain.
Dalam gaya arsitektur REST, implementasi klien dan implementasi server dapat dilakukan secara independen tanpa saling mengetahui satu sama lain.

## **Communication Between Clients & Servers**

**MAKING REQUESTS**

REST mengharuskan klien membuat permintaan ke server untuk mengambil atau mengubah data di server. Permintaan umumnya terdiri dari:
  - kata kerja HTTP, yang mendefinisikan jenis operasi apa yang harus dilakukan
  - header, yang memungkinkan klien untuk menyampaikan informasi tentang request
  - jalan menuju resource
  - message body opsional yang berisi data

**HTTP VERBS**

4 kata kerja HTTP dasar yang kami gunakan dalam permintaan untuk berinteraksi dengan resource dalam sistem REST:
  - GET — mengambil sumber daya tertentu (berdasarkan id) atau kumpulan sumber daya
  - POST — buat sumber daya baru
  - PUT — perbarui sumber daya tertentu (berdasarkan id)
  - DELETE — menghapus sumber daya tertentu dengan id

**Headers and Accept Parameters**

Di header permintaan, klien mengirimkan jenis konten yang dapat diterimanya dari server.

subtipe yang umum digunakan:
  - gambar — gambar/png, gambar/jpeg, gambar/gif
  - audio — audio/wav, audio/mpeg
  - video — video/mp4, video/ogg
  - aplikasi — aplikasi/json, aplikasi/pdf, aplikasi/xml, aplikasi/octet-stream

## Sending Responses

**Content Types**

Misalnya, ketika klien mengakses sumber daya dengan id 23 di sumber artikel dengan Permintaan GET ini:

`GET/articles/23 HTTP/1.1
Accept: text/html, application/xhtml`

Server mungkin mengirim kembali konten dengan header respons:

`HTTP/1.1 200 (OK)
Content-Type: text/html`

**Response Codes**

HTTP status code adalah kode respons standar yang diberikan oleh server website di internet. Kode ini membantu mengidentifikasi penyebab masalah saat laman website atau sumber daya lain tidak dimuat dengan benar.
- Contoh:
  - 200 (OK): Ini adalah respons standar untuk permintaan HTTP yang berhasil.
  - 201 (CREATED): Ini adalah respons standar untuk permintaan HTTP yang menghasilkan item yang berhasil dibuat.
  - 204 (NO CONTENT): Ini adalah respons standar untuk permintaan HTTP yang berhasil, di mana tidak ada yang dikembalikan di badan respons.
  - 400 (BAD REQUEST): Permintaan tidak dapat diproses karena sintaks permintaan yang buruk, ukuran yang berlebihan, atau kesalahan klien lainnya.
  - 403 (FORBIDDEN): Klien tidak memiliki izin untuk mengakses sumber daya ini.
  - 404 (NOT FOUND): Sumber daya tidak dapat ditemukan saat ini. Mungkin sudah dihapus, atau belum ada.
  - 500 (Internal Server Error): HTTP status code ini adalah kode yang dikirimkan ketika server mengalami situasi yang tidak diketahui cara menanganinya.

<hr>

<h2><b>Intro & Essential Node JS</B></h2>

### Apa itu Node JS?
- Node.js adalah runtime development untuk JavaScript yang bersifat open-source dan cross-platform. Node.js menjalankan V8 JavaScript engine (yang juga merupakan inti dari Google Chrome) diluar browser.
### Node JS Architecture
- **Single Thread**, Javascript menggunakan konsep single thread, yang berarti hanya memiliki satu tumpukan panggilan yang digunakan untuk menjalankan program.
- **Event Loop** akan memfasilitasi kondisi ini, event loop akan memeriksa terus menerus, ketika antrian kosong di call stack maka akan menambah antrian baru dari event queue sampai semua perintah selesai di eksekusi.
- **Server side scripting**, dengan menggunakan NodeJS dapat menjalankan javascript di server side menggunakan terminal command line menggunakan perintah “node”.

### Membuat Web Server Dengan Node JS

Node.js memiliki built-in modul yang disebut HTTP, built-in modul ini memungkinkan Node JS mentransfer data melalui Hyper Text Transfer Protocol (HTTP).
  - Untuk menggunakan modul HTTP, gunakan require()
  - Gunakan method createServer() untuk membuat server HTTP
  - Callback function yang digunakan pada method http.createServer(), akan dijalankan ketika seseorang mencoba mengakses komputer pada port 8080.
```
const http = require('http');
//create a server object:
http.createServer(function (req, res) {
    res.write('Hello World!');
    res.end();
}).listen(8080);
```
Menambahkan HTTP Header
  - Bisa menggunakan method res.writeHead() untuk menambahkan header HTTP.
  - Argumen pertama dari method res.writeHead() adalah status code, 200 berarti semuanya OK
  - Argumen kedua adalah objek yang berisi header respons.
  - Contoh : Jika respons dari server HTTP seharusnya ditampilkan sebagai HTML, maka kita harus menambahkan header HTTP dengan tipe konten yang benar.
```
const http = require('http');
//create a server object:
http.createServer(function (req, res) {
    res.writeHead(200, {'Content-Type': 'text/html'});
    res.write('Hello World!');
    res.end();
}).listen(8080);
```
- Respons yang dikembalikan dari HTTP web server bisa dalam berbagai format.
- Contohnya, Bisa mengembalikan response dalam format JSON dan HTML, namun juga dapat mengembalikan format teks lain seperti XML dan CSV.
- Selain itu web server dapat mengembalikan data non-teks seperti PDF, file zip, audio, dan video.
- Format ini harus ditambahkan kedalam HTTP Header.
- Membaca Query String
  - Callback function pada method http.createServer() memiliki argumen req yang mewakili request dari klien, sebagai objek (objek http.IncomingMessage).
  - Objek ini memiliki sebuah properti yang disebut "url" yang menyimpan informasi url yang sedang mengakses.
```
const http = require('http');
//create a server object:
http.createServer(function (req, res) {
    res.writeHead(200, {'Content-Type': 'text/html'});
    res.write('Hello World!');
    res.end();
}).listen(8080);
```
- Split Query String
  - Ada build-in module yang bisa kita gunakan untuk split query string menjadi beberapa bagian yang dapat dibaca.
  - Build-in modulenya adalah URL Module.
```
const http = require('http');
const url = require('url');
http.createServer(function (req, res) {
    res.writeHead(200, {'Content-Type': 'text/html'});
    const query = url.parse(req.url, true).query;
    const txt = q.year + " " + q.month;
    res.end(txt);
}).listen(8080);
```

## Express JS
### Apa itu Express JS ?
- Express.js, atau hanya express, adalah kerangka aplikasi web back end untuk Node.js, dirilis sebagai perangkat lunak sumber terbuka dan gratis di bawah lisensi MIT. Ini dirancang untuk membangun aplikasi web dan API. Ini telah disebut sebagai kerangka kerja server standar de facto untuk Node.js.
### Apa itu Back End Web Application?
- Back end app adalah aplikasi yang berjalan di server-side yang bekerja untuk memberikan informasi berupa data sesuai request dari client / browser / front end app.
- Kelebihan dari framework ini terletak pada fitur caching, support dengan Google V8 Engine, JavaScript, serta didukung oleh komunitas dan skalabilitas aplikasi yang baik.


**Basic Syntax expressJS**
```
const express = require('express');
const app = express();
const port = 3000
app.get('/', (req res) => {
  res.send('Hello World!')
})
app.listen(port, () => {
  console.log('Example app listening at http://localhost:${port}')
})
```

### Basic Routes
**Routes** adalah sebuah end point yang diapat kita akses menggunakan URL di website. Didalam routes kita perlu menentukan method API, alamat dan response apa saja yang akan dikeluarkan
```
app.get('/', (req res) => {
  res.send('Hello World!');
}) 
```
Kita bisa menjalankan aplikasi sederhana kita dengan cara menggunakan “node”. Dan aplikasi kita akan berjalan di alamat ‘http://localhost:3000’ Kemudian kita dapat mengaksesnya di website dan menambah route yang akan kita akses yaitu “/"
```
node app.js
```
**method**, Kita dapat menggunakan method yang dalam REST API seperti **POST, PUT, PATCH** dan **DELETE**
```
app.post('/add', (req res) => {
  res.send('Data berhasil ditambahkan')
})
app.delete('/delete', (req res) => {
  res.send('Data berhasil dihapus')
})
```
- **Response** Di dalam route kita dapat mengirim response menggunakan parameter dari route express.js yaitu “res.Send()” untuk mengirim plain text ketika kita mengakses route tersebut.
```
app.get('/hello', (req res) => {
  res.json({
    name : "nama",
    umur : 25,
    alamat : "kota",
  })
})
```
- Kita dapat mengirim response berupa output json yang biasa dipakai untuk back end application. Dengan menggunakan output json maka kita dapat mengirim data yang mudah diakses.
- **Status Code**
- Dalam pengaplikasian back end application, kita sangat perlu memberikan status code sebagai informasi apakah route yang kita akses berjalan sebagaimana mestinya dan tidak terjadi error.
```
app.get('/hello', (req res) => {
  res.status(200).json({
    name : "nama",
    umur : 25,
    alamat : "kota",
  })
})
```
**Query** merupakan parameter yang digunakan untuk membantu menentukan tindakan yang lebih spesifik daripada hanya sekedar router biasa. Biasanya query ditaruh di akhir route dengan memberikan informasi diawali dengan “?” kemudian tedapat key dan data yang dapat ditindak lanjuti. Ex : “?q=hello&age=23”
```
app.get('/hello', (req res) => {
  let name = req.query.name
  let umur = req.query.umur
  res.status(200).json({
    name : "nama",
    umur : 25,
    alamat : "kota",
  })
})
```
**Nested route** digunakan ketika terdapat banyak route yang memiliki nama yang sama atau ingin membuat route yang lebih mendalam.
```
app.use("/hello", hello)
const hello = require('express').Router();
hello.get('/rajqi', (req, res) => {
  res.send("hello saya adalah rajqi")
})
hello.get('/fakhri', (req, res) => {
  res.send("hello saya adalah fakhri")
})
```
### Express Middleware

**Apa itu Middleware ?**
**Middleware function** adalah sebuah fungsi yang memiliki akses ke object request (req), object response (res), dan sebuah fungsi next didalam request-response cycle. Fungsi next biasanya di berikan nama variable next.

- Pada Dasarnya, sebuah middleware function dapat melakukan tugas-tugas berikut:
  - Menjalankan kode apapun.
  - Memodifikasi Object Request dan Object Response.
  - Menghentikan request-response cycle.
  - Melanjutkan ke middleware function selanjutnya atau ke handler function dalam suatu request response cycle.

### Contoh Menjalankan kode apapun
Sebuah function middleware bisa digunakan untuk mengeksekusi kode apapun untuk suatu tujuan tertentu.
Sebagai contoh, kita akan membuat sebuah middleware function yang akan mencetak tulisan “Halo User!” Ketika sebuah HTTP Request masuk kedalam middleware function ini. 
Middleware Function ini akan diberi nama dengan greetLogger.
```
const greetLogger = function (req, res, next) {
    console.log('Halo User!')
    next()
}
```

### Contoh Memodifikasi Object Request dan Object Response.
Sebuah function middleware bisa digunakan untuk memodifikasi Object Request dan Object Response.
Sebagai contoh, kita akan membuat sebuah middleware function yang akan menambahkan informasi request time pada object request.
Middleware Function ini akan diberi nama dengan addRequestTime.
``` 
const addRequestTime = function (req, res, next) {
    req.requestTime = Date.now()
    next()
}
```

### Contoh Menghentikan request-response cycle.
Sebuah function middleware bisa digunakan untuk menghentikan request-response cycle.
Sebagai contoh, kita akan membuat sebuah middleware function yang akan menghentikan request-response cycle.
Middleware Function ini akan diberi nama dengan stopHere.
Request tidak akan pernah sampai ke handler function, karena middleware telah menghentikan request-response cycle dengan res.send() dan tidak memanggil next()
```
const stopHere = function (req, res, next) {
    res.send('<p>request stop from middleware</p>')
}
```

## Jenis Express Middleware Berdasarkan Cara Penggunaan

### Application Level Middleware
- Application Level Middleware adalah sebuh function middleware yang melekat ke instance object Application Express.
- Penggunaannya dengan cara memanggil method app.use().
- Application Level Middleware akan di jalankan setiap kali Express Application menerima sebuah HTTP Request.
```
const addRequestTime = function (req, res, next) {
    req.requestTime = Date.now()
    next()
}
app.user(addRequestTime)
```

### Router Level Middleware
- Router Level Middleware adalah sebuh function middleware yang cara kerjanya sama persis dengan application level middleware, yang menjadikan perbedaan adalah middleware function ini melekat ke instance object Router Express.
- Penggunaannya dengan cara memanggil method express.Router().
- Router Level Middleware hanya akan di jalankan setiap kali sebuah Express Router yang menggunakan middleware ini menerima sebuah HTTP Request, sedangan pada Router yang lain tidak akan dijalankan.

### Error Handling Middleware
- Error Handling mengacu kepada bagaimana cara sebuah Express Application menangkap dan memproses error yang terjadi, baik itu berupa kesalahan yang synchronous maupun asynchronous.
- Express Application sudah menyediakan error handle function default, sehingga kita tidak perlu lagi membuat sendiri functionnya.
- Error handle function default milik Express Application hanyalah kerangka functionnya saja, kita tetap harus menuliskan di dalam function ini bagaimana sebuah error akan di handle.
- Error Handling Middleware digunakan pada Application Level Middleware
```
const express = require("express")
const app = express()
const errorHandling = function(err, req, res, next) {
    console.error(err.stack)
    res.status(500).send('Something broke!')
}
app.use(errorHandling)
```
Sebuah error handling middleware function harus memberikan 4 (empat) buah argument (err, req, res, next) agar bisa di deteksi oleh Express Application sebagai error handling middleware, sekalipun kita tidak akan pernah menggunakan function next dalam error handling middleware ini.

Jika hal ini tidak dilakukan, maka Express Application tidak akan mengenali middleware function ini sebagai error handling middleware, dan akan memperlakukan middleware ini sebagai Application Level Middleware seperti biasa.
<hr>

<h2><b>Design Database With MySQL</b></h2>

## Apa itu Basis Data Relasional (RDBMS)?
RDBMS atau Relational Database Management System adalah sebuah system yang dirancang khusus untuk management database agar tersusun dan terintegrasi.
karena system inilah yang memungkinkan user mengelola database, mulai dari membuat database, membaca isi database, mengubah isi database dan menghapus isi database atau CRUD
  - Create
  - Read
  - Update
  - Delete

## Relation Between Tables 

Relasi adalah istilah dalam relational database (tabel) yang mengacu ke bagaimana tabel dalam database itu bisa saling terkait. dalam pembuatan relasi database itu dihubungkan dengan Foreign Key pada kolom tabel A dan Primary Key pada kolom tabel B.
- Istilah-istilah relasi antar tabel
  - Primary Key
  - Foreign Key


## Primary Key & Foreign Key

- **Primary** merupakan kunci utama pada field tertentu dalam sebuah tabel yang biasa digunakan untuk mendefinisikan rows data tertentu.
- **Foreign** adalah atribut pada tabel yang menunjukan hubungan (relasi) ke tabel induk ( yang mempunyai primary key).

## Jenis-jenis Relasi Antar Tabel di Database
Jenis relasi database diantaranya ada 3 yaitu:
  - One To One Field
  - One To Many
  - Many To Many 
- **One to One Field** merupakan relasi dari saru baris tabel A ke sau baris ke tabel B
- **One to Many** adalah relasi dimana satu baris tabel (tabel A) dihubungkan ke satu baris atau lebih (Tabel B).
- **Many To Many** adalah relasi yang dimana lebih dari satu baris (tabel A) dihubungkan di lebih dari satu baris (tabel B).


## Merancang database
### 1. Mendefinisikan persyaratan
Hal pertama yang harus dipikirkan saat membuat database adalah untuk apa kita menginginkannya. Ini mungkin tampak jelas, tetapi layak untuk dinyatakan secara eksplisit. Persyaratan yang berbeda akan menghasilkan struktur informasi, hubungan, desain, dan implementasi yang berbeda

### 2. Membuat Rencana berdasarkana kebutuhan
Hal pertama yang harus dilakukan adalah membaca dokumen persyaratan dengan cermat, mencatat hal-hal yang mungkin menjadi entitas dalam database kita, dan kemungkinan hubungan di antara mereka.

Penting pada tahap ini untuk mengajukan pertanyaan untuk memperjelas persyaratan. Itu wajar bagi orang yang bekerja dengan sesuatu setiap hari untuk memikirkan beberapa hal sebagai 'akal sehat' atau jelas, ketika mereka mungkin tidak jelas bagi seseorang yang datang dari luar area kerja itu. Juga, orang terkadang tidak terbiasa memikirkan aspek-aspek pekerjaan mereka dengan ketelitian yang diperlukan untuk membuat database.
Langkah perantara yang sangat berguna antara mendapatkan persyaratan dan mengimplementasikan database kami di SQL adalah membuat Entity Relationship Diagram (ERD). Ini adalah, seperti yang mungkin Anda antisipasi, diagram yang memetakan hubungan antara entitas yang akan kita bangun ke dalam database kita. Proses menyusun diagram ini dapat membantu kita meluruskan hubungan dan mengidentifikasi wawasan penting atau atribut yang berlebihan seiring berjalannya waktu.

### 3. Mengidentifikasi entitas
apa saja identitasnya

### 4. Atribut mana yang ingin kita simpan?
Langkah selanjutnya adalah memikirkan atribut mana yang ingin kita simpan untuk setiap entitas kita. Ini mungkin dijabarkan secara rinci dalam dokumen persyaratan kami, atau mungkin memerlukan lebih banyak kebijaksanaan dari pihak pengembang basis data.

### 5. Memetakan hubungan
menentukan hubungan antara satu entitas ke entitas lain, misal one to one, one to many, many to many dll
