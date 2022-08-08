###### Nama : Azuzan Ananta F
###### Kelas : XIII RPL 1
###### No Absen : 17 

# Modul 4

### VIEW BLADE TEMPLATE 

TUGAS PRAKTIKUM 
1. Buatlah View untuk project anda 
2. Buatlah layout dengan master template blade untuk project anda 

Jawaban:

1) membuat folder dan file yang akan di isi

Nama folder yang harus dibuat 
- barang
- kategori
- layout

Nama file yang harus dibuat
- index.blade.php
- index.blade.php
- app.blade.php

folder dan file-file nya menjadi satu seperti 
contoh gambar yang terlihat seperti dibawah ini

![image](https://user-images.githubusercontent.com/109930500/183360936-9c394024-fe63-4e75-95bf-c25ecbfd8393.png)

2) pada folder layout `file app.blade.php` kita mengambil **css dan js di bootstrap** ini linknya
[Bootstrap](https://getbootstrap.com/docs/5.2/getting-started/introduction/)

>![image](https://user-images.githubusercontent.com/109929687/183342789-f6776591-ea33-4712-88ac-e847218de516.png)

gambar diatas adalah bagian bootstrap yang kita pakai sebagai css dengan menambahkan syntax sebagai berikut
```
    <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/bootstrap@5.2.0/dist/css/bootstrap.min.css">
```

selanjutnya bagian js dengan menambahkan syntax sebagai berikut
```
<script src="https://cdn.jsdelivr.net/npm/bootstrap@5.2.0/dist/js/bootstrap.bundle.min.js"></script>
```

Selanjutnya isi file `app.blade.php` dengan all codenya
```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/bootstrap@5.2.0/dist/css/bootstrap.min.css">
    <title>
      @yield('title')
</title>
</head>
<body>
      
     <!-- untuk navbar -->
     <div class="container">
     <nav class="navbar navbar-expand-lg bg-dark">
  <div class="container-fluid">
    <a class="navbar-brand text-white ml-5" href="#">Penjualan</a>
    <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarSupportedContent" aria-controls="navbarSupportedContent" aria-expanded="false" aria-label="Toggle navigation">
      <span class="navbar-toggler-icon"></span>
    </button>
    <div class="collapse navbar-collapse" id="navbarSupportedContent">
      <ul class="navbar-nav me-auto mb-2 mb-lg-0">
        <li class="nav-item">
          <a class="nav-link text-white" aria-current="page" href="/kategori">Kategori</a>
        </li>
        <li class="nav-item">
          <a class="nav-link text-white" href="/barang">Barang</a>
        </li>
    </div>
  </div>
</nav>
</div>

<!-- content -->
<div class="container">
  @yield('content')
</div>  

<script src="https://cdn.jsdelivr.net/npm/bootstrap@5.2.0/dist/js/bootstrap.bundle.min.js">
  </script>    
</body>
</html>
```

Selanjutnya folder **barang** yang berisi file `index.blade.php`

all codenya akan terlihat seperti dibawah ini karena kurang lebih saya memahami isi code dibawah
```
@extends('layout.app')

@section('title')
   Barang
@endsection

@section('content')
    <div class="mt-3">
      <table class="table table-striped">
         <thead>
            <tr>
               <th width="5%">No.</th>
               <th>Nama</th>
               <th width="15%">Kategori</th>
               <th width="15%">Qty</th>
               <th width="15%">Harga Beli</th>
               <th width="15%">Harga Jual</th>
               <th width="15%">Aksi</th>
            <tr>
         </thead>

         <tbody>
            <tr>
               <td>1</td>
               <td>Meja</td>
               <td>Atk</td>
               <td>10</td>
               <td>50000</td>
               <td>55000</td>
               <td>Hapus | Edit</td>
            </tr>
            <tr>
               <td>2</td>
               <td>Ac</td>
               <td>Elektronik</td>
               <td>15</td>
               <td>30000</td>
               <td>35000</td>
               <td>Hapus | Edit</td>
            </tr>
         </tbody>
      </table>
   </div>
@endsection
```

Selanjutnya pada folder **kategori** file `index.blade.php` 

all codenya akan ditampilkan di bawah ini
```
@extends('layout.app')

@section('title')
   Barang
@endsection

@section('content')
    <div class="mt-3">
      <table class="table table-striped">
         <thead>
            <tr>
               <th width="5%">No.</th>
               <th>Nama</th>
               <th width="15%">Kategori</th>
               <th width="15%">Qty</th>
               <th width="15%">Harga Beli</th>
               <th width="15%">Harga Jual</th>
               <th width="15%">Aksi</th>
            <tr>
         </thead>

         <tbody>
            <tr>
               <td>1</td>
               <td>Rcb</td>
               <td>Variasi</td>
               <td>10</td>
               <td>50000</td>
               <td>55000</td>
               <td>Hapus | Edit</td>
            </tr>
            <tr>
               <td>2</td>
               <td>Domino</td>
               <td>Variasi</td>
               <td>15</td>
               <td>30000</td>
               <td>35000</td>
               <td>Hapus | Edit</td>
            </tr>
         </tbody>
      </table>
   </div>
@endsection
```

<!-- @extends('layout.app') yang beratri mewariskan ke (folder.file) -->

<!-- @section('title') barang @endsection berarti mengelompokkan agar bisa dipanggil ke berbagai file seperti pewarisan -->

hasil dari code yang kita kerjakan akan terlihat seperti dibawah ini

code yang ditampilkan ini dari folder **barang** file `home.blade.php`

>![image](https://user-images.githubusercontent.com/109929687/183351770-7b9b7182-3815-42f7-9ebb-2e059eef5bf3.png)

lalu hasil folder **kategori** file `index.blade.php`

>![image](https://user-images.githubusercontent.com/109929687/183352926-8fbf9d75-acc8-4c72-ad68-7d1c6abdcbc2.png)


 
