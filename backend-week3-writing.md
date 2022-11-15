<h1> Weekly Report 8 (Week 3 Back-End Bootcamp) </h1>

## MongoDB

### Apa itu MongoDB?

**MongoDB** adalah salah satu jenis database NoSQL yang cukup populer digunakan dalam pengembangan website. Berbeda dengan database jenis SQL yang menyimpan data menggunakan relasi tabel, MongoDB menggunakan dokumen dengan format JSON. 

Hal inilah yang dianggap membuat pengelolaan data menggunakan MongoDB lebih baik. Alhasil, banyak perusahaan besar seperti Adobe, Google dan ebay yang menggunakannya. 

## Mongoose
**Mongoose** adalah library yang bisa digunakan sebagai Object Modelling MongoDB untuk NodeJS.
Mongoose bisa digunakan untuk mengelola hubungan antara data, menyediakan validasi dan juga digunakan untuk menerjemahkan antara objek dalam kode dan representasi Objek tersebut di MongoDB.

### Schema Types

Ada beberapa schema type yang didukung oleh pustaka ini yaitu

- String
- Number
- Date
- Boolean
- Buffer (untuk data binary misalnya gambar, mp3 dll.)
- Mixed (data dengan tipe apa saja)
- Array
- ObjectId

### Creating Connection
Membuat koneksi dengan menggunakan MongoDB database, yang diletakkan di file .env
```
const mongoose = require('mongoose');
require('dotenv').config()
const url = process.env.MONGODB_URL;
mongoose.connect(url, {
  useNewUrlParser: true,
  useUnifiedTopology: true,
  useDindAndModify: false});
const db = mongoose.connection;
db.on('error', console.log.bind(console, 'koneksi error'));
db.once('open', () => console.log('terkoneksi'));
```
Best practice adalah menggunakan file .env untuk menyimpan URL atau *confidential data* yang tidak perlu dilihat di public.
```
MONGOOSE_URL=mongodb://localhost:27017/dbmongoose
```
### Defining your Schema
```
// defining schema
const Schema = mongoose.Schema;
var userSchema = new Schema({
  name: String,
  password: String,
  email: String,
  phoneNumber: String,
}, {
  timestamps: true
});
const User = mongoose.model('users', userSchema);
```
### CRUD
Lalu kita menggunakan model users dari schema yang telah dibuat untuk melakukan pengolahan data, atau operasi CRUD.
```
const User = mongoose.model('Users', userSchema)
```

Kita harus menginstall Express untuk routing dan body-parser, untuk menggunakan method Post dan testing API di postman.
```
npm install express
npm install body-parser
```

Dengan fungsi findById() dengan kode dibawah kita akan mendapatkan data user berdasarkan id
```
app.get('/users/:id', (req, res) => {
  User.findById({
    _id : req.params.id
  }, (error, users) => {
    if (error) {
      res.status(400).send({
        message: 'no data found',
      })
    } else {
      res.status(200).send({
        message: "showing data",
        result
      })
    }
  })
})
```
Menggunakan method deleteOne() kita dapat menghapus satu data berdasarkan ID
```
app.delete('/users/:id', (req, res) => {
  User.deleteOne({
    _id : req.params.id
  }, (error, users) => {
    if (error) {
      res.status(400).send({
        message: 'error, no id found, cannot delete'
      })
    }else {
      res.status(200).send({
        message: 'delete success',
      })
    }
  })
});
```
### Populate
**Populate** ada kaitannya dengan relasi database. Populate adalah proses penggabungan 2 collection atau lebih menjadi satu objek JSON.
## Docker
### Apa itu Docker?
Docker adalah layanan yang menyediakan kemampuan untuk mengemas dan menjalankan sebuah aplikasi dalam sebuah lingkungan terisolasi yang disebut dengan container. Dengan adanya isolasi dan keamanan yang memadai memungkinkan kamu untuk menjalankan banyak container di waktu yang bersamaan pada host tertentu.

### Container VS Virtual Machines

![image](https://user-images.githubusercontent.com/114375139/201895777-d959c0b1-8b28-4036-8e6c-7d0758546ba9.png)

Pembeda utama antara Container dan Virtual Machine adalah bahwa mesin virtual memvirtualisasikan seluruh mesin hingga ke lapisan perangkat keras dan kontainer hanya memvirtualisasikan lapisan perangkat lunak di atas level sistem operasi.
