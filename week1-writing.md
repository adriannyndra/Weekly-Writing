<h1> Weekly Recap 1 </h1>
Berikut hal-hal yang telah dipelajari di minggu pertama dari Web Development Basic

- Git & Github
- Unix Command line
- HTML
- CSS
- Git & Github
- Algoritma & JavaScript Dasar




## Git & Github
What is Git? and what is GitHub?

- <b>Git</b>
merupakan program/aplikasi untuk code versioning, tugasnya adalah melacak file dari suatu project,
yang bisa digunakan oleh programmer sebagai cara untuk me-mantain atau melacak perubahan proyek mereka

- <b>Github</b>
merupakan penyedia jasa cloud service yang memungkinkan programmer untuk menyimpan repositorynya di cloud secara remote, dan memiliki fitur-fitur lain yang mendukung operasi Git
(kontrol akses, pelacakan bug, permintaan fitur perangkat lunak, manajemen tugas, integrasi berkelanjutan, dan wiki untuk setiap proyek.)

<h3> Command di dalam Git & Github </h3>

  - <b>git init</b>, untuk membuat repositori baru

  - <b>git commit</b>, untuk melakukan commit atau menyimpan perubahan pada version control pada git. Dan kita bisa menambahkan pesan untuk membeikan checkout pada setiap perbuahan. contohnya "git commit -m "pesan checkout"

  - <b>git push origin</b>, untuk mempublish file atau aplikasi ke github

  - <b>git clone</b>, untuk melakukan cloning dari github ke komputer atau local
  
  
  
  
## Unix Command Line
  
  - <b>Shell</b>
  
  Dalam komputasi, shell adalah program komputer yang memaparkan layanan sistem operasi kepada pengguna manusia atau program lain. Secara umum, shell sistem operasi 
  menggunakan antarmuka baris perintah atau antarmuka pengguna grafis, tergantung pada peran komputer dan operasi tertentu.
  
  - <b>Terminal</b>
  
  Terminal bisa dibilang sebuah penghubung user dengan komputer, dimana user dapat mengetikan atau memberikan suatu perintah. Disinilah tempat dimana shell akan berperan.

 - <b>CLI (Command Line Interface)</b>
  
  Sama seperti terminal, CLI biasanya digunakan untuk mendeskripsikan sebuah program/aplikasi dimana user dapat menginput command yang berkomunikasi dengan operating system
  
  <h3>File System Structure</h3>
  
  Adalah cara bagaimana OS menyimpan data dalam sistem. Contoh dalam Sistem Operasi Windows struktur file yang disimpan menggunakan struktur yang bentuknya seperti gambar dibawah.
  
  ![](https://cdn.ttgtmedia.com/rms/onlineImages/TT_tree_mobile.jpg)
  
  <h3>List of Commands</h3>
  
  - <b>pwd (print working directory)</b>, untuk melihat current working directory
  - <b>dir (directory)</b>, untuk melihat directory
  - <b>cd (change directory)</b>, untuk pindah directory
  - <b>ls (list)</b>, untuk melihat isi file di dalam directory
  - <b>touch</b>, untuk membuat file directory
  - <b>cp (copy)</b>, untuk menyalin file directory
  - <b>mv (move)</b>, untuk memindahkan file directory
  - <b>rm (remove)</b>, untuk menghapus file directory




## HTML
  
  - Apa itu HTML?

HTML adalah Hypertext Markup Language, digunakan untuk membuat kerangka atau struktur untuk Web pages (halaman website) di internet. Apa peran HTML pada web development? HTML dibaca oleh Web browser seperti Chrome, Firefox, Edge, Safari, atau Opera. Dokumen HTML yang berisi tag-tag HTML akan memberitahu browser bagaimana cara menampilkan sebuah konten.


  - Kerangka HTML
  
  
  ```
  <html>
  <head>
    <title>
      Judul
    </title>
    <body>
      Konten
    </body>
  </html>
  
   ```
   
   Diatas adalah contoh dari syntax HTML, dari Tag title yang memberikan Judul pada suatu website, dan Tag Body yang berisikan konten dari website tersebut. Contoh     diatas adalah contoh yang paling basic, ada banyak lagi Tag yang memiliki fungsi beragam
   
   
  - <b> Tag HTML </b>
  
Tag adalah sebauh penanda awalan dan akhiran dari sebuah elemen di HTML. Tag dibuat dengan kurung siku ( <...> ), lalu di dalamnya berisi nama tag dan kadang juga ditambahkan dengan atribut. Contoh: ``` <p> , <a> , <body> , <head> ```  dan sebagainya sama seperti contoh snippet yang diberikan diatas. Tag selalu ditulis berpasangan, namun ada jenis-jenis tag yang bersifat self closing yaitu tidak perlu closing tag
  
Contoh-contoh Tag pada HTML:

   <b>Tag untuk membuat tulisan tebal dan miring</b>

 
    <b>Tebal</b> <i>Miring</i>

    
    
   <b>Tag Untuk Membuat Daftar/List</b>

    `- Ordered List

      <ol>
        Dafunda
        <li>Dafunda Tekno</li>
        <li>Dafunda Otaku</li>
        <li>Dafunda Games</li>
      </ol>
      
    - Unordered List
    
      <ul>
        Dafunda
        <li>Dafunda Tekno</li>
        <li>Dafunda Otaku</li>
        <li>Dafunda Games</li>
      </ul>`

   <b> Tag HTML Untuk Menampilkan gambar </b>
   
```

    <img src="https://bit.ly/2FKluzq" alt="Si Kucing"></img>
    
```



<b>Deploy HTML</b>
    
Deploy adalah sebuah proses untuk menyebarkan aplikasi yang sudah kita kerjakan supaya bisa digunakan oleh orang-orang. Jika aplikasi kita HTML atau Web App kita   perlu mendeploy ke server. Untuk melakukan hal tersebut kita bisa menggunakan layanan yang bernama Netlify
      
    
    
 ## CSS
 
 - Apa itu CSS?

CSS adalah bahasa komputer yang digunakan untuk menambahkan design ke suatu halaman website di internet agar terlihat lebih cantik/menarik. CSS adalah singkatan dari Cascading Style Sheets. Kita ibaratkan HTML adalah kerangka yang memberi sturuktur pada website, maka CSS adalah baju yang memberi warna dan layout pada website.

 - Bagaimana cara menggunakan CSS?

Terdapat 3 cara kita dapat menggunakan CSS pada website kita yaitu Internal, Inline, dan eksternal
    
  - Internal CSS
    
    Cara penggunaan inline CSS adalah dengan menggunakan element/tag `<style>` untuk menyisipkan kode CSS. element/tag `<style>` diletakkan di dalam element `<head>`
    
  - Inline CSS
    
    Kita menambahkann CSS langsung pada atribut HTML, contoh: `<p style="color:red">Tulisan ini berwarna merah</p>`
    
  - Eksternal CSS
    
    Cara penggunaan eksternal CSS adalah dengan menyisipkan kode CSS dengan cara membuat file CSS terpisah, dan lalu menyambungkannya dengan file HTML dengan menggunakan tag seperti ini `<link rel="stylesheet" href="styles.css" />`
    
    
 - CSS Syntax

CSS Syntax adalah syntax yang digunakan untuk menunjuk atau memilih HTML element mana yang ingin diberi style (dihias). CSS syntax terdiri dari selector, property, dan value. contoh:

```
p {
  color: blue;
}
```

P adalah selector, color adalah property mana yang akan diubah, blue adalah valuenya

    
 ## Algoritma & Struktur Data
 
 - Apa itu Algoritma?

Suatu upaya dengan urutan operasi yang disusun secara logis dan sistematis untuk menyelesaikan suatu masalah untuk menghasilkan suatu output tertentu.

 - Apa saja manfaat Algoritma?
    - Membantu menyederhanakan suatu program yang rumit dan juga besar.
    - Mempermudah pembuatan program yang dapat menyelesaikan masalah tertentu.
    - Membantu menyelesaikan suatu masalah dengan logika dan juga sistematis.

 - Kualitas Wajib dari Algoritma
    - Input dan output harus didefinisikan terlebih dahulu
    - Setiap step jelas, dan tidak ambigu
    - Algoritma harus dibuat agar dapat digunakan dalam bahasa pemograman apapun. 

 - Apa itu Pseudocode?

Pseudocode adalah menuliskan algoritma sebelum kita implementasikan ke bahasa pemograman tertentu.

<b> Kriteria penulisan Pseudocode: </b>
  
  - Menggunakan HURUF BESAR pada kata kunci (key commands). CONTOH: IF number is > 10 THEN …

  - 1 statement = 1 baris

  - Gunakan indentasi

  - Simple & Easy to understand by humans

<b> Contoh Procedural </b>

```
STORE "width" with any number
STORE "height" with any nummber
STORE "area" without any value

CALCULATE "width" times "height"
SET "area" value with calculation result
DISPLAY "area"
```

<b> Contoh Cnditional </b>

```
IF "bright"
DO "go to the market"
ELSE
DO "stay at home"
```

<b> Contoh Loop </b>

```
STORE "count" t0 1

WHILE "count" < 11
DISPLAY "count"
CALCULATE "count" mod 2
STORE "reminder" value with calculation result
IF "reminder" equals to 0
DISPLAY "EVEN!"
ELSE
DISPLAY "ODD!"
```


 - Recursive

Recursive adalah pola pikir dalam algoritma yang memanggil method/function didalam sebuah function
