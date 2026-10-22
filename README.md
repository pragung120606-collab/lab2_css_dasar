Hasil CSS Internal:

(Tambahkan gambar screenshot penambahan Internal CSS di sini)
![Internal CSS](path_gambar_kamu)

3. Menambahkan Inline CSS

Menambahkan atribut style secara langsung pada tag paragraf <p> untuk mengubah tata letak dan warna teks.

<p style="text-align: center; color: #ccd8e4;">


Hasil Inline CSS:

(Tambahkan gambar screenshot penambahan Inline CSS di sini)
![Inline CSS](path_gambar_kamu)

4. Membuat dan Menyisipkan CSS Eksternal (style_eksternal.css)

Membuat file CSS terpisah bernama style_eksternal.css untuk mengatur tampilan navigasi, lalu memanggilnya di dalam tag <head> menggunakan tag <link>.

Aturan CSS (style_eksternal.css):

nav {
  background: #20A759;
  color: #fff;
  padding: 10px;
}
nav a {
  color: #fff;
  text-decoration: none;
  padding: 10px 20px;
}
nav .active,
nav a:hover {
  background: #0B6B3A;
}


Pemanggilan di HTML:

<link rel="stylesheet" href="style_eksternal.css" type="text/css">


Hasil Eksternal CSS:

(Tambahkan gambar screenshot penerapan Eksternal CSS di sini)
![Eksternal CSS](path_gambar_kamu)

5. Menambahkan CSS ID dan Class Selector

Menambahkan gaya untuk kontainer ID #intro serta Class .button dan .btn-primary di dalam file style_eksternal.css.

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


Hasil Akhir Praktikum:

(Tambahkan gambar screenshot hasil akhir di sini)
![Hasil Akhir](path_gambar_kamu)

❓ Jawaban Pertanyaan dan Tugas

1. Eksperimen CSS Cheat Sheet

Telah dilakukan pengujian beberapa properti tambahan dari CSS Cheat Sheet, seperti mengubah warna background, ketebalan font (font-weight), pengaturan margin/padding, dan efek hover pada tombol.

2. Perbedaan h1 {...} dan #intro h1 {...}

h1 {...}: Merupakan Element Selector. Aturan ini akan diterapkan secara global ke seluruh elemen h1 yang ada di dokumen HTML.

#intro h1 {...}: Merupakan Descendant Selector. Aturan ini bersifat spesifik dan hanya akan mempengaruhi elemen h1 yang berada di dalam elemen bersarang yang memiliki atribut id="intro".

3. Prioritas Penggunaan CSS (Inline vs Internal vs Eksternal)

Jika satu elemen yang sama dideklarasikan menggunakan ketiga cara penulisan CSS, maka deklarasi Inline CSS yang akan diprioritaskan dan ditampilkan di browser karena memiliki tingkat spesifisitas paling tinggi.

Urutan Prioritas:

Inline CSS (Tingkat tertinggi)

Internal CSS / Eksternal CSS (Tergantung mana yang dibaca paling akhir oleh browser)

Contoh:

<!-- Teks akan berwarna hijau karena dikontrol oleh Inline CSS -->
<p style="color: green;">Paragraf</p>


4. Prioritas ID Selector vs Class Selector

Apabila elemen HTML memiliki atribut ID dan Class sekaligus (contoh: <p id="paragraf-1" class="text-paragraf">), maka deklarasi dari ID Selector (#paragraf-1) yang akan ditampilkan di browser.

Penjelasan:
ID Selector memiliki bobot specificity (spesifisitas) yang jauh lebih tinggi daripada Class Selector, sehingga style dari ID akan menimpa style dari Class.

Contoh:

.text-paragraf {
  color: blue;
}

#paragraf-1 {
  color: red; /* Menang, teks akan berwarna merah */
}
