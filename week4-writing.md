<h1> Weekly Recap 4 </h1>

Berikut adalah materi yang telah saya pelajari pada minggu ke-4 (Web Development Advance)

- JavaScript Intermediate
  - Fetch
  - Async Await
 - Responsive Web Design
 - Github Lanjutan
 - Bootstrap 5


<h2> Javascript intermediate </h2>


<h3> Fetch </h3>
Fetch merupakan cara dalam melakukan network request yang memanfaatkan sebuah Promise dalam penggunaanya. Karena cara kerja Fetch adalah mengembalikan sebuah Promise maka respon handling yang digunakan adalah then jika promise mengembalikan resolve dan catch jika promise mengembalikan nilai reject.

<h3> Async Await </h3>
Async await merupakan fitur baru JavaScript yang hadir sejak ES2017, async await merupakan suatu handler atau function khusus yang dapat menangani proses asyncronus yang bekerja dengan cara menunda eksekusi hingga proses asynchronous selesai.

```
async function myAsync () {
    let p = new Promise((resolve, reject) => {
        setTimeout(() => resolve("Hello World!"), 2000)
    });

    let result = await p;
    alert(result);
}

myAsync();
```

Code diatas merupakan penggunaan sederhana dari Async/Await pada Javascript. Berikut merupakan contoh lain dari penerapan Async/Await disertai pengambilan data melalui API yg ada di Github
```
async function gitAsync (name) {
    let github = await fetch(`https://api.github.com/users/${name}`);

    let githubUser = await github.json();
    let githubImgUrl = githubUser.avatar_url;

    window.open(githubImgUrl)
}

gitAsync("denoland")
```




<h2> Responsive Web Design </h2>

Responsive web design bertujuan agar website bisa di akses pada device apapun seperti smartphone, laptop, tablet dan gadget dengan ukuran layar variasi lainnya.

Berikut adalah beberapa cara agar website kita bisa menjadi Responsive

**Adding Meta Viewport in HTML**

Meta Tag Viewport to scale the website
```
<meta name="viewport" content="width=device-width, initial-scale=1.0">
```

**Media Query**

Media Query digunakan untuk membuat beberapa styles tergantung pada jenis device.
Jenis media query untuk responsive web design umumnya hanya menggunakan 2 jenis media query yaitu min-width dan max-width

Setting up media query:
```
@media screen and (min-width: your pixel) {
  /* your css*/
}
@media screen and (max-width: your pixel) {
  /* your css*/
}
```

**Breakpoint**

Perubahan yang terjadi pada tampilan saat berganti device atau ukuran width disebut breakpoint.
Breakpoint Media Query dapat menggunakan range media query min and max
```
body {
  background-color: white;
}
@media screen and (min-width: 500px) and (max-width: 700px) {
  body {
    background-color: aquamarine;
  }
}
```


<h2> Git & Github Lanjutan </h2>

Git & github selain menjadi alat bantu penyimpanan source code secara online/remote juga kita manfaatkan sebagai alat bantu yang memungkinkan kita untuk berkolaborasi dengan tim.

**Branching

Dari pembelajaran git awal, kita sudah mempelajari cara membuat branch dan cara pindah branch. Branching ini sangat essential untuk developer agar bisa berkolaborasi dengan tim yaitu dengan memiliki percabangan pada repo dimana tiap cabang memiliki isi code/versi project yg berbeda dan bisa kita gabungkan dengan branch lain sesuai kebutuhan.

**Pull Request 

Saat perubahan pada project bersama sudah kita ubah dan push ke remote repo kita, kita bisa memanfaatkan pull request untuk dapat mengirimkan request agar code yang kita buat dapat di review lebih lanjut oleh team leader.

**Merge

Jika tidak terjadi conflict dan pull request kita sudah diterima oleh team leader, kita bisa melakukan merge untuk menggabungkan perubahan yang ada pada branch yang kita buat sebelumnya ke dalam branch dev sebagai branch utama yang biasa digunakan oleh grup project dalam tahap development.

**Github Organization

Dengan memanfaatkan github organization kita bisa memantain/develop project dengan tim secara lebih efektif.


<h2> Bootstrap 5 </h2>

**Apa itu Boostrap & Mengapa kita harus menggunakannya?

Bootstrap adalah salah satu framework CSS, HTML, JS terpopuler yang dapat membantu kita dalam membangun <i> mobile first & responsive </i> web secara cepat. Bootstrap dapat mempercepat pembuatan Front-end Web karena CSS dan Script JS mereka yang sudah tersedia dan tinggal kita gunakan saja dan bisa kita jadikan fondasi dan bisa kita <i> improve upon </i> dengan design kita sendiri. Contoh component-component yang mereka siapkan termasuk seperti Jumbotron (tidak tersedia di Bootstrap 5) Modal, Carousel, Buttons dll.

**Layout pada Bootstrap

Seperti yang dijelaskan sebelumnya, **Breakpoint** adalah ukuran lebar yang menentukan tampilan responsif yang bergantung pada ukuran viewport.

- Dalam bootstrap ada beberapa breakpoint, yaitu:
  - sm
  - md
  - lg
  - xl
  - xxl


**Container** 

adalah elemen paling dasar dalam layout bootstrap. 

Terdapat 3 macam container dalam bootstrap

  - **Default Container**, Bersifat responsive dan fixed-width, lebarnya akan berubah pada setiap breakpoint.
  ```
  <div class="container">
    <!-- Content here -->
  </div>
  ```
  - **Fluid Container**, Class container-fluid memiliki lebar yang sama dengan viewport
  ```
  <div class="container-fluid">
    <!-- Content here -->
  </div>
  ```
  - **Responsive Container**, Responsive container, diurutkan dari breakpoint terkecil, terdiri dari:
    - .container-sm
    - .container-md
    - .container-lg
    - .container-xl
    - .container-xxl
  ```
  <div class="container-sm">100% wide until small breakpoint</div>
  <div class="container-md">100% wide until medium breakpoint</div>
  <div class="container-lg">100% wide until large breakpoint</div>
  <div class="container-xl">100% wide until extra large breakpoint</div>
  <div class="container-xxl">100% wide until extra extra large breakpoint</div>
  ```
  
**Grid** 

Grid mirip dengan flexbox, biasanya digunakan bersama dengan container. 
```
<div class="container">
  <div class="row">
    <div class="col">
      Column
    </div>
    <div class="col">
      Column
    </div>
    <div class="col">
      Column
    </div>
  </div>
</div>
```


