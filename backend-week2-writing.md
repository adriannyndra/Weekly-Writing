<h1> Weekly Report 7 (Week 2 Back-End Bootcamp) </h1>

## MySQL Basic

### Apa yang dimaksud dengan  Database?
 **Database** merupakan sekumpulan tabel yang berisikan informasi untuk diolah yang kemudian data tersebut bisa digunakan di dalam sebuah sistem.

### Database Management System

**DBMS** adalah software yang dapat digunakan oleh user untuk berkomunikasi dengan data yang ada dalam media penyimpanan.

Tipe utama pada Database management System antara lain: 
  - Hierarchical 
  - Network 
  - Relational 
  - Non Relational
  - Object Oriented.

### Apa itu MySQL
MySQL adalah sistem manajemen basis data relasional open source berbasis SQL. Itu dirancang dan dioptimalkan untuk aplikasi web dan dapat berjalan di platform apa pun. Sebagai persyaratan baru dan berbeda muncul dengan internet, MySQL menjadi platform pilihan untuk pengembang web dan aplikasi berbasis web.

### SQL Data Types & Keys

- **Number**
- **String**
- **Boolean**
- **Date**
- **Default**
- **Null** (Kosong, atau belum di assign dengan value)

### Primary & Foreign Keys

- **Primary Key** adalah identifikasi untuk membedakan satu baris dengan baris lainnya dalam suatu tabel. Pada dasarnya, setiap tabel hanya memiliki satu primary key saja.

- **Foreign Key** adalah sebuah atribut atau gabungan atribut yang terdapat dalam suatu tabel yang digunakan untuk menciptakan hubungan (relasi) antara dua tabel

### SQL Commands

```SHOW DATABASES;``` menunjukkan seluruh list database

```CREATE DATABASES namadb;``` membuat database baru

```USE namadb;``` untuk menggunakan database yang sudah ada/dibuat

```DROP DATABASES namadb;``` untuk menghapus / menghilangkan database yang dipilih

```SHOW TABLES;``` untuk melihat semua isi tabel di database

<hr>

## MySQL Lanjutan

### Relations dalam SQL

- **One to Many** memiliki satu baris dalam tabel yang dapat memiliki beberapa baris di tabel relasinya

- **Many to Many** digunakan ketika tabel yang berelasi dapat memiliki beberapa baris di tabel relasinya

- **One to One** diimplementasikan dengan cara yang sama seperti *One to Many* tetapi dengan kondisi tambahan

### Key-key lain dalam SQL

- **Super Key**
  - Kumpulan dari satu atau lebih dari satu key yang dapat digunakan untuk mengidentifikasi record secara unik dalam sebuah tabel.
  - Super Key adalah superset dari Candidate Key.
- **Candidate Key** 
  - kumpulan satu atau lebih fields/columns yang dapat mengidentifikasi record secara unik dalam tabel.
  - Bisa jadi ada beberapa Candidate Keys di dalam satu tabel
  - Setiap Candidate Key bisa digunakan sebagai Primary Key.
  - Candidate Key adalah super key yang tidak mempunyai value yang berulang
  - **Unique Key**
  - Kumpulan dari satu atau lebih fields/columns di sebuah table database yang secara unik mengidentifikasi sebuah record dalam table database tersebut.
  - Hampir sama dengan Primary key, namun value dari Unique Key bisa berupa satu buah null value di dalam sebuah table database, dan Unique Key tidak bisa memiliki duplicate values

### Join Multiple Tables
Mengambil records dari dua atau lebih table database yang memiliki relationship dan akan di sajikan dalam single result set.

- **INNER JOIN** 
  - Semua baris akan diambil dari kedua table yang akan di JOIN, selama columns cocok dengan kondisi yang sudah di tentukan.
  - Memungkinkan baris dari salah satu tabel muncul di hasil jika dan hanya jika kedua tabel memenuhi kondisi yang ditentukan dalam klausa ON.
  ```
  SELECT column_name(s)
  FROM table1
  INNER JOIN table2
  ON table1.column_name = table2.column_name;
  ```
- **LEFT JOIN**
  - Pada JOIN ini, semua records dari table di sisi kiri JOIN statement akan di pilih.
  - Jika record yang di pilih dari table kiri tidak memiliki record yang cocok pada table JOIN yang kanan, maka record tersebut masih dipilih, dan kolom pada table yang kanan akan bernilai NULL.
  ```
  SELECT column_name(s)
  FROM table1
  LEFT JOIN table2
  ON table1.column_name = table2.column_name;
  ```
- **RIGHT JOIN**
  - Pada JOIN ini, semua records dari table di sisi kiri JOIN statement akan di pilih, bahkan jika table di sebelah kiri tidak memiliki record yang cocok.
  ```
  SELECT column_name(S)
  FROM table1
  RIGHT JOIN table2
  ON table1.column_name = table2.column_name;
  ```
- **Aggregate Functions** 
- Mengambil satu nilai setelah melakukan perhitugan pada sekumpulan nilai
- **Type of Aggregate Functions**
  - **MAX**
    - fungsi mengembalikan nilai terbesar dari kolom yang dipilih.
    ```
    SELECT MAX (column_name)
    FROM table_name
    WHERE condition;
    ```
  - **MIN**
    - fungsi mengembalikan nilai terkecil dari kolom yang dipilih.
    ```
    SELECT MIN (column_name)
    FROM table_name
    WHERE condition;
    ```
  - **SUM**
    - fungsi mengembalikan jumlah total kolom numerik.
    ```
    SELECT SUM(column_name)
    FROM table_name
    WHERE condition;
    ```
  - **COUNT**
    - fungsi mengembalikan jumlah baris yang cocok dengan kriteria yang ditentukan.
    ```
    SELECT COUNT(column_name)
    FROM table_name
    WHERE condition;
    ```
  - **AVG**
    - fungsi mengembalikan nilai rata-rata kolom numerik
    ```
    SELECT AVG(column_name)
    FROM table_name
    WHERE condition;
    ```
  - **UNION**
    - Digunakan untuk menggabungkan kumpulan hasil dari dua atau lebih pernyataan SELECT.
    - Setiap pernyataan SELECT dalam UNION harus memiliki jumlah kolom yang sama
    - Kolom juga harus memiliki tipe data yang serupa
    - Kolom dalam setiap pernyataan SELECT juga harus dalam urutan yang sama
    ```
    SELECT column_name(s) FROM table1
    UNION
    SELECT column_name(s) FROM table2;
    ```
  - **GROUP BY**
    - Mengelompokkan baris yang memiliki nilai yang sama ke dalam baris ringkasan
    - Sering digunakan dengan fungsi agregat untuk mengelompokkan kumpulan hasil dengan satu atau lebih kolom.
    ```
    SELECT column_name(s)
    FROM table_name
    WHERE condition
    GROUP BY column_name(s);
    ```
  - **HAVING**
    - HAVING ditambahkan ke SQL karena kata kunci WHERE tidak dapat digunakan dengan aggregate functions.
    ```
    SELECT column_name(s)
    FROM table_name
    WHERE condition
    GROUP BY column_name(s)
    HAVING condition
    ORDER BY column_name(s);
    ```
  - **LIKE & Wildcards**
    - Operator LIKE digunakan dalam klausa WHERE untuk mencari pola tertentu dalam kolom.
    - Karakter wildcard digunakan untuk menggantikan satu atau lebih karakter dalam sebuah string.
    ```
    SELECT column1, column2, ...
    FROM table_name
    WHERE columN LIKE pattern;
    ```

<hr>

## Authentication & Authorization in Express

### Apa itu authentication/autentikasi?
Autentikasi adalah verifikasi siapa Anda. seperti penjaga keamanan yang meminta untuk melihat tiket dan ID Anda untuk memverifikasi bahwa nama di ID Anda cocok dengan Anda.
Atentikasi bergantung pada satu atau lebih faktor untuk memverifikasi identitas, dan faktor-faktor ini datang dalam tiga jenis utama:
* Pengetahuan adalah sesuatu yang Anda ketahui, seperti nama pengguna dan kata sandi.
* Kepemilikan adalah sesuatu yang Anda miliki, seperti kartu keamanan atau perangkat seluler
* Inheren adalah sesuatu tentang Anda, yang umumnya mengacu pada data biometrik seperti sidik jari.
Otentikasi yang bergantung pada satu faktor, seperti kombinasi nama pengguna/sandi sederhana, disebut Otentikasi Satu Faktor, dan menjadi semakin tidak aman.

### Apa itu authorization/autorisasi
Otorisasi adalah verifikasi atas apa yang boleh Anda lakukan. Otorisasi sangat penting untuk keamanan web, dan bertanggung jawab atas segala hal mulai dari mencegah pengguna memodifikasi akun satu sama lain, melindungi aset back-end dari penyerang, hingga memberikan akses terbatas ke layanan eksternal. Otorisasi yang baik akan memungkinkan Anda membatasi pengguna dan layanan untuk hak istimewa yang mereka butuhkan; hanya karena seorang pengguna berwenang untuk mengelola satu grup tidak berarti mereka harus dapat mengelola semua grup, misalnya.

### Encryption
Salah satu alat inti untuk menegakkan otentikasi dan otorisasi adalah enkripsi. Enkripsi adalah proses mengubah data menjadi format yang tidak dapat dibaca kecuali Anda memiliki kunci yang benar untuk mendekripsinya. Enkripsi datang dalam dua jenis utama:
* Symmetric encryption
* Asymmetric encryption

### Contoh Detail Autentikasi
Tanggapan terhadap perintah autentikasi dapat dikategorikan ke dalam:
* Knowledge-Based: “Something You Know” contoh password, pin etc
* Possession-Based: “Something You Have” contoh phone or smart card
* Inherence-Based: “Something You Are” contoh fingerprint

### Session Based Authentication
- Pada session based authentication, server akan membuat session untuk user setelah user log in. Session id akan disimpan di dalam cookie pada browser yang digunakan user.
### Token Based Authentication
- Terdapat banyak aplikasi web menggunakan JSON Web Token (JWT) dibandingkan sessions untuk authentication. Pada aplikasi token based, server akan membuat JWT dengan rahasia dan mengirim JTW kepada client. Client kemudian menyimpan JWT (biasanya pada local storage) dan memasukan JWT kedalam headers untuk setiap request yang dilakukan oleh client.

## Web Session
Sesi web mengacu pada serangkaian interaksi pengguna selama jangka waktu tertentu. Data sesi disimpan di sisi server dan dikaitkan dengan ID sesi.
Pikirkan sesi sebagai memori jangka pendek untuk aplikasi web. Pada latihan berikutnya, kami akan menjelaskan di mana pengidentifikasi sesi ini disimpan sehingga browser (klien) dapat terus mengambil data sesi yang sama di antara pemuatan halaman yang berbeda.

## Session & Cookie
Agak kikuk bagi klien untuk mengingat untuk menempelkan ID sesi ke setiap permintaan. Karena itu, ID sesi sering disimpan di sisi klien dalam bentuk cookie sesi.
Cookie adalah potongan kecil data — file teks berukuran maksimal 4kb — browser menyimpan yang secara otomatis dikirim dengan permintaan HTTP ke aplikasi web. Cookie disetel oleh header respons HTTP dalam pasangan nilai kunci:
```
Set-Cookie: key=Velue
```
```
Set-Cookie: sessionID=34jgL79b
```
Ini kira-kira bagaimana sesi diimplementasikan dengan cookie:
1. Seorang pengguna pergi ke sebuah situs. Server web membuat sesi dan ID sesi.
2. Dalam respons server, ini memberi tahu browser untuk menyimpan cookie dengan ID sesi (tidak boleh menyertakan informasi pribadi apa pun).
3. Cookie ID sesi secara otomatis dilampirkan ke setiap permintaan HTTP berikutnya ke server.
4. Saat server membaca cookie ID sesi yang dikirim dengan permintaan HTTP berikutnya, server akan mengembalikan data sesi yang terkait dengan ID tersebut.
5. Proses berlanjut selama sesi aktif.
6. Cookie sesi dan ID sesi kedaluwarsa setelah pengguna menutup browser, logout, atau durasi sesi yang telah ditentukan (yaitu satu jam) berlalu.

## Cookie Security
Cookie sering kali menyimpan informasi sensitif, terutama saat digunakan dalam manajemen sesi. Cookie juga digunakan untuk menyimpan preferensi atau riwayat pribadi pengguna, yang juga harus tetap aman. 

Langkah pertama untuk mengamankan cookie dapat menambahkan tanggal kedaluwarsa atau durasi sehingga cookie tidak bertahan lebih lama dari yang dibutuhkan.Kami dapat menentukan informasi tersebut melalui header Set-Cookie dalam respons HTTP seperti:
```
Set-Cookie: Key=Value, expirea=monday, 29-Nov-2021 07:30:10 GMT
```
Atribut HttpOnly untuk header Set-Cookie memastikan bahwa data cookie tidak dapat diakses oleh skrip yang menjalankan sisi klien. Ini membantu mencegah serangan Cross-Site Scripting (XSS) yang mencoba mencuri cookie sesi dan mengambil alih milik korban. sesi, yang sangat umum.
```
Set-Cookie: Key=Value, expired=monday, 29-Nov-2021 07:30:10 GMT; HTTPOnly
```

## Sequelize 
### Apa itu Sequelize?
Sequelize adalah ORM (Object Relational Mapping) Node JS yang berbasis promise. Sequelize mendukung sebagian besar relational Database seperti MySQL, PostgresQL, MariaDB, SQLite dan Miscrosoft SQL Server.
### Apa itu ORM?
ORM adalah suatu metode/teknik pemrograman yang digunakan untuk mengkonversi data dari lingkungan bahasa pemrograman berorientasi objek (OOP) dengan lingkungan database relational.