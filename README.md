# Pertemuan 2
## Pemograman Web
## Profil
| Variable | Isi |
| -------- | --- |
| **Nama** | Dafa Alfiana Erlangga |
| **NIM** | 312210446 |
| **Kelas** | TI.22.A.4 |
| **Mata Kuliah** | Pemograman Web |

# Instruksi Praktikum 
1. Persiapkan text editor misalnya VSCode. 
2. Buat file baru dengan nama lab2_css_dasar.html 
3. Buat struktur dasar dari dokumen HTML. 
4. Ikuti langkah-langkah praktikum yang akan dijelaskan berikutnya. 
5. Lakukan validasi dokumen css dengan mengakses https://jigsaw.w3.org/css-validator/ 

## 1. Membuat Dokumen Html
```HTML
<!DOCTYPE html> 
<html lang="en"> 
<head> 
    <meta charset="UTF-8"> 
    <meta name="viewport" content="width=device-width, initial-scale=1.0"> 
    <title>CSS Dasar</title> 
</head> 
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
        <p>Kami sedang belajar HTML dan CSS dasar, pada mata kuliah <b>Pemrograman 
Web</b> di <i>Universitas Pelita Bangsa</i>.<br> Pelajaran pertama yang kami dapat 
adalah membuat tampilan web sederhana dalam rangka mengenal tag-tag dasar HTML 
dan CSS.</p> 
        <!-- CSS Class Selector --> 
        <a class="button btn-primary" href="#intro">Informasi selengkapnya.</a> 
    </div> 
</body> 
</html> 

```
**Hasil :**

![](https://github.com/Angga674/Praktikum_2_Pemograman_Web/blob/main/Gambar/1.png?raw=true)

## 2. Mendeklarasikan CSS Internal 
```CSS
<head>
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

**Hasil :**

![](https://github.com/Angga674/Praktikum_2_Pemograman_Web/blob/main/Gambar/2.png?raw=true)

# 3. Menambahkan Inline CSS 
```HTML
<p style="text-align: center; color: #ccd8e4;"> 
```
**Hasil :**

![](https://github.com/Angga674/Praktikum_2_Pemograman_Web/blob/main/Gambar/3.png?raw=true)

# 4. Membuat CSS Eksternal 
Buatlah file baru dengan nama style_eksternal.css kemudian buatlah deklarasi CSS seperti berikut. 
```CSS
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
Kemudian tambahkan tag <link> untuk merujuk file css yang sudah dibuat pada bagian <head>
```CSS
<head> 
    <!-- menyisipkan css eksternal --> 
    <link rel="stylesheet" href="style_eksternal.css" type="text/css"> 
</head> 
```
**Hasil**

![alt text](https://github.com/Angga674/Praktikum_2_Pemograman_Web/blob/main/Gambar/4.png?raw=true)

# 5. Menambahkan CSS Selector 
Selanjutnya menambahkan CSS Selector menggunakan ID dan Class Selector. Pada file 
style_eksternal.css, tambahkan kode berikut. 
```CSS
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
Kemudian simpan kembali dan refresh browser untuk melihat perubahannya. 

** Hasil : **

![alt text](?raw=true)


## Pertanyaan dan Tugas
1. Lakukan eksperimen dengan mengubah dan menambah properti dan nilai pada kode CSS
dengan mengacu pada CSS Cheat Sheet yang diberikan pada file terpisah dari modul ini.

2. Apa perbedaan pendeklarasian CSS elemen h1 {...} dengan #intro h1 {...}? berikan penjelasannya!

3. Apabila ada deklarasi CSS secara internal, lalu ditambahkan CSS eksternal dan inline CSS pada
elemen yang sama. Deklarasi manakah yang akan ditampilkan pada browser? Berikan penjelasan dan contohnya!

4. Pada sebuah elemen HTML terdapat ID dan Class, apabila masing-masing selector tersebut
terdapat deklarasi CSS, maka deklarasi manakah yang akan ditampilkan pada browser?
Berikan penjelasan dan contohnya! `<p id="paragraf-1" class="text-paragraf">`

## Jawaban
1.

2. `h1 {...}:`
    Ini adalah sebuah selektor CSS umum yang akan mempengaruhi semua elemen `<h1>` di halaman HTML.
    Dalam hal ini, gaya yang didefinisikan akan berlaku untuk setiap elemen `<h1>` di seluruh halaman.

   `#intro h1 {...}:`
    Ini adalah selektor CSS yang lebih spesifik dan berlaku hanya untuk elemen `<h1>` yang berada di dalam elemen dengan ID intro.
    Dalam hal ini, gaya yang didefinisikan hanya akan mempengaruhi elemen `<h1>` yang merupakan turunan dari elemen dengan ID intro.
   
    Dalam kedua kasus di atas, h1 dan `#intro h1` adalah selektor CSS yang mengacu pada elemen `<h1>`. 
    Namun, perbedaannya terletak pada ruang lingkup elemen yang dipengaruhi oleh gaya yang didefinisikan. 
    `h1 {...}` akan mempengaruhi semua elemen `<h1>` di halaman, sedangkan `#intro h1 {...}` akan mempengaruhi hanya elemen `<h1>` yang berada di dalam elemen dengan ID intro.

3. Urutan penulisan berperan ketika spesifisitasnya sama. Spesifisitas diukur berdasarkan kombinasi dari selektor CSS yang digunakan. Semakin spesifik selektor, semakin tinggi              spesifisitasnya.
   Umumnya, urutan prioritas adalah sebagai berikut (dari yang paling rendah ke yang paling tinggi):

    - 1). Deklarasi CSS dari file eksternal.
    - 2). Deklarasi CSS yang ada secara internal.
    - 3). Deklarasi inline CSS.

4. - Deklarasi CSS menggunakan ID memiliki keutamaan lebih tinggi daripada deklarasi CSS menggunakan class.
   - Ketika ada konflik, deklarasi CSS dengan ID akan menggantikan deklarasi CSS dengan class.
  
   CONTOH :

   Misalkan ada dekralasi CSS sebagai berikut.
     ```CSS
     #paragraf-1 {
     color: red;
     font-weight: bold;
     }

     .text-paragraf {
     color: blue;
     }
     ```

   Dan element HTML seperti ini.
     ```HTML
     <p id="paragraf-1" class="text-paragraf">Contoh paragraf</p>
     ```
     
   Dalam contoh di atas, meskipun elemen `<p>` memiliki class `"text-paragraf"`, deklarasi CSS dengan ID `#paragraf-1` akan mendominasi dan mengaturnya menjadi teks berwarna merah dan      tebal (sesuai dengan deklarasi di atas). Deklarasi `color: blue;` dari class akan diabaikan dalam hal ini.
   Jadi, deklarasi dengan ID memiliki prioritas lebih tinggi daripada deklarasi dengan class dalam menentukan gaya elemen.
 
