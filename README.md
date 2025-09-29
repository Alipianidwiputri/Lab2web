# Penjelasan Langkah Langkah praktikum beserta hasil screenshot 

1. Membuat Dokumen HTML
Pertama, kita bikin file baru dengan nama lab2_css_dasar.html. Isinya adalah struktur dasar HTML, lengkap dengan <header>, menu navigasi <nav>, dan sebuah div dengan id="intro". Di dalamnya ada judul Hello World, sebuah paragraf penjelasan, dan link bertuliskan “Informasi selengkapnya”.

  Code:
```
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>CSS Dasar</title>
<head>
<body>
<header>
<h1>CSS Internal dan <i>Inline CSS</i></h1>
</header>
<nav>
<a href="lab2_css_dasar.html">CSS Dasar</a>
<a href="lab2_css_eksternal.html">CSS Eksternal</a>
<a href="lab1_tag_dasar.html">HTML Dasar</a>
</nav>
<!-- CSS ID Selector -->
<div id="intro">
<h1>Hello World</h1>
<p style="text-align: center; color: #ccd8e4;">Kami sedang belajar HTML dan CSS dasar, pada mata kuliah <b>Pemrograman
Web</b> di <i>Universitas Pelita Bangsa</i>. Pelajaran pertama yang kami dapat
adalah membuat tampilan web sederhana dalam rangka mengenal tag-tag dasar HTML
dan CSS.</p>
<!-- CSS Class Selector -->
<a class="button btn-primary" href="#intro">Informasi selengkapnya.</a>
</div>
</body>
</html>
```

Kalau sudah disimpan lalu dibuka di browser, kita akan melihat tampilan halaman HTML sederhana.

<img width="1756" height="311" alt="Screenshot 2025-09-29 124313" src="https://github.com/user-attachments/assets/c20c6e4a-073d-4a05-b179-86623fcac4e0" />




2. Menambahkan CSS Internal
Setelah itu, kita coba menambahkan CSS internal di bagian <head>. Kode CSS internal ditulis di dalam tag <style>. Contohnya: kita atur font, tinggi header, warna teks, dan posisi judul agar lebih rapi.

Code:
```
<head> 
    <title>CSS Dasar</title> 
    <style> 
        body { 
            font-family:'Open Sans', sans-serif; 
        } 
        header { 
            min-height: 80px; 
            border-bottom:1px solid #77CCEF; 
        } 
        h1 { 
            font-size: 24px; 
            color: #0F189F; 
            text-align: center; 
            padding: 20px 10px; 
        } 
        h1 i { 
            color:#6d6a6b; 
        } 
    </style> 
</head>
```

Kalau halaman di-refresh, tampilan teks akan berubah sesuai style yang kita atur tadi.

<img width="953" height="709" alt="Screenshot 2025-09-29 124606" src="https://github.com/user-attachments/assets/472f1fff-6afd-4559-a6e7-1b117ea3f932" />




3. Menambahkan Inline CSS
Selanjutnya, kita belajar pakai inline CSS. Caranya: menambahkan style langsung ke dalam tag HTML. Misalnya pada paragraf <p>, kita kasih aturan text-align:center dan warna teks tertentu.

Code:
```
<p style="text-align: center; color: #ccd8e4;">
```

Kalau disimpan dan dibuka lagi di browser, paragraf itu tampil beda dengan yang lain.

<img width="953" height="738" alt="Screenshot 2025-09-29 140115" src="https://github.com/user-attachments/assets/0d66d274-3cad-4b75-a00d-deba41655364" />




4. Membuat CSS Eksternal
Lanjut, kita bikin file baru bernama style_eksternal.css. Di file itu, kita tulis aturan CSS untuk menu navigasi: warna background, warna teks link, padding, dan efek hover. Supaya file CSS ini bisa dipakai di HTML.

Code:
```
nav { 
    background: #20A759; 
    color:#fff; 
    padding: 10px; 
} 
nav a { 
    color: #fff; 
    text-decoration: none; 
    padding:10px 20px; 
} 
nav .active,  
nav a:hover { 
    background: #0B6B3A; 
} 
```

kita hubungkan lewat tag <link> yang ditulis di bagian <head>.

Code:
```
<head>
<!-- menyisipkan css eksternal -->
<link rel="stylesheet" href="style_eksternal.css" type="text/css">
</head>
```

Setelah di-refresh, navigasi akan berubah sesuai style dari file CSS eksternal.

<img width="962" height="676" alt="Screenshot 2025-09-29 140538" src="https://github.com/user-attachments/assets/c2d40f85-3a5c-4505-a1d2-c0cedd6c78ec" />




5. Menambahkan CSS Selector (ID dan Class)
Terakhir, kita belajar selector. ID Selector (#intro) → dipakai untuk mengatur tampilan div dengan id intro, misalnya warna background, border, padding, dan teks judulnya. Class Selector (.button dan .btn-primary) → dipakai untuk mengatur tampilan tombol/link, misalnya warna background, padding, margin, dan dekorasi teks.

Code:
```
/* ID Selector */ 
#intro { 
    background: #418fb1; 
    border: 1px solid #099249; 
    min-height: 100px; 
    padding: 10px; 
} 
#intro h1 { 
    text-align: left; 
    border: 0; 
    color: #fff; 
} 
 
/* Class Selector */ 
.button { 
    padding: 15px 20px; 
    background: #bebcbd; 
    color: #fff; 
    display: inline-block; 
    margin: 10px; 
    text-decoration: none; 
} 
.btn-primary { 
    background: #E42A42; 
}
```

Kalau di-refresh lagi, sekarang halaman sudah punya navigasi, konten utama dengan warna berbeda, dan tombol/link dengan style lebih menarik.

<img width="954" height="800" alt="Screenshot 2025-09-29 140623" src="https://github.com/user-attachments/assets/f7b27853-e02f-46b8-a3e4-9172b370e9b0" />






