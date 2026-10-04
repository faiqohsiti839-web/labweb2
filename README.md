# labweb2
# Lab2Web.
Tugas Post Test Praktikum 2
# Lab2Web — Praktikum 2: HTML Lanjutan

**Mata Kuliah:** Pemrograman Web
**Dosen Pengampu:** Agung Nugroho
**Nama:** Siti Faiqoh Almarufi
**NIM:** 312510168
**Program Studi:** Teknik Informatika
**Kampus:** Universitas Pelita Bangsa, Bekasi

---
## Langkah-langkah Praktikum

### 1. Membuat Tabel Data Mahasiswa

**Penjelasan:** Tabel dibuat dengan elemen `<table>`. Baris dibuat dengan `<tr>`, sel judul kolom dengan `<th>`, dan sel data dengan `<td>`. Atribut `border="1"` menampilkan garis tepi tabel.

```html
<!DOCTYPE html>
<html>
<head><title>HTML Lanjutan</title></head>
<body>
<h1>Data Mahasiswa</h1>
<table border="1">
 <tr><th>NIM</th><th>Nama</th><th>Program Studi</th></tr>
 <tr><td>31241001</td><td>Andi</td><td>Teknik Informatika</td></tr>
 <tr><td>31241002</td><td>Budi</td><td>Teknik Informatika</td></tr>
</table>
</body>
</html>
```

**Tugas tambahan:** menambahkan minimal tiga data mahasiswa.

**Hasil:**

<img width="301" height="146" alt="Screenshot 2026-10-04 130426" src="https://github.com/user-attachments/assets/9958ddc7-89fb-40bb-ad11-e875513a0196" />
---

### 2. Mengembangkan Tabel dengan `thead`, `tbody`, dan `tfoot`

**Penjelasan:** Tabel dikelompokkan menjadi tiga bagian agar lebih terstruktur:

- `<caption>` : judul tabel.
- `<thead>` : bagian kepala tabel (judul kolom).
- `<tbody>` : bagian isi tabel.
- `<tfoot>` : bagian kaki tabel (ringkasan, misalnya rata-rata).
- `colspan` : menggabungkan beberapa kolom menjadi satu sel.

```html
<table border="1">
 <caption>Nilai Praktikum</caption>
 <thead><tr><th>No</th><th>Nama</th><th>Nilai</th></tr></thead>
 <tbody>
 <tr><td>1</td><td>Andi</td><td>85</td></tr>
 <tr><td>2</td><td>Budi</td><td>90</td></tr>
 </tbody>
 <tfoot><tr><td colspan="2">Rata-rata</td><td>87.5</td></tr></tfoot>
</table>
```

**Eksperimen:** mengubah data, menambahkan baris, dan menggunakan `colspan` untuk menggabungkan sel.

**Hasil:**

<img width="285" height="132" alt="Screenshot 2026-10-04 130452" src="https://github.com/user-attachments/assets/3df4cb59-8e6d-4799-b9ea-f8615c39632b" />---

### 3. Membuat Form Registrasi Mahasiswa

**Penjelasan:** Form dibuat dengan `<form>`. Setiap input diberi `<label>` yang terhubung melalui atribut `for` dan `id`. Jenis input yang digunakan:

| Tipe Input | Fungsi |
|---|---|
| `text` | Teks biasa (nama lengkap) |
| `email` | Alamat email (format divalidasi browser) |
| `password` | Teks tersembunyi (titik/bintang) |
| `date` | Pemilih tanggal |

Tombol `submit` mengirim form, sedangkan `reset` mengosongkan semua isian.

```html
<h1>Form Registrasi Mahasiswa</h1>
<form>
 <label for="nama">Nama Lengkap</label><br>
 <input type="text" id="nama" name="nama"><br><br>
 <label for="email">Email</label><br>
 <input type="email" id="email" name="email"><br><br>
 <label for="password">Password</label><br>
 <input type="password" id="password" name="password"><br><br>
 <label for="tanggal">Tanggal Lahir</label><br>
 <input type="date" id="tanggal" name="tanggal"><br><br>
 <button type="submit">Daftar</button>
 <button type="reset">Reset</button>
</form>
```

**Hasil:**

<img width="364" height="238" alt="Screenshot 2026-10-04 130521" src="https://github.com/user-attachments/assets/8c47ef5b-7770-452c-bf06-b5512cce4a62" />---

### 4. Radio Button dan Checkbox

**Penjelasan:**

- **Radio button** (`type="radio"`) : hanya **satu** pilihan dalam satu grup. Grup ditentukan oleh `name` yang sama (`jk`).
- **Checkbox** (`type="checkbox"`) : boleh memilih **lebih dari satu** pilihan.

```html
<h2>Jenis Kelamin</h2>
<input type="radio" id="laki" name="jk" value="L">
<label for="laki">Laki-laki</label>
<input type="radio" id="perempuan" name="jk" value="P">
<label for="perempuan">Perempuan</label>

<h2>Keahlian</h2>
<input type="checkbox" id="html" name="skill" value="HTML">
<label for="html">HTML</label>
<input type="checkbox" id="css" name="skill" value="CSS">
<label for="css">CSS</label>
<input type="checkbox" id="js" name="skill" value="JavaScript">
<label for="js">JavaScript</label>
```

**Hasil:**

<img width="323" height="158" alt="Screenshot 2026-10-04 130541" src="https://github.com/user-attachments/assets/b80de846-96ec-4e40-abe3-846daf99c0ab" />---

### 5. Select dan Textarea

**Penjelasan:**

- `<select>` dengan `<option>` : menu dropdown untuk memilih satu opsi dari daftar.
- `<textarea>` : kolom input teks **multibaris**. Ukurannya diatur dengan `rows` (jumlah baris) dan `cols` (jumlah kolom).

```html
<label for="prodi">Program Studi</label>
<select id="prodi" name="prodi">
 <option value="">-- Pilih Prodi --</option>
 <option value="ti">Teknik Informatika</option>
 <option value="si">Sistem Informasi</option>
</select>
<br><br>
<label for="alamat">Alamat</label><br>
<textarea id="alamat" name="alamat" rows="5" cols="40"></textarea>
```

**Hasil:**

<img width="314" height="158" alt="Screenshot 2026-10-04 130557" src="https://github.com/user-attachments/assets/8b327e8b-810a-4968-ae6c-8b42c5b5a26c" />---

### 6. Validasi Form Dasar

**Penjelasan:** HTML5 menyediakan validasi bawaan tanpa JavaScript:

| Atribut | Fungsi |
|---|---|
| `required` | Input wajib diisi |
| `minlength` | Jumlah karakter minimal |
| `min` / `max` | Nilai angka minimum / maksimum |
| `type="email"` | Memastikan format email valid |

```html
<form>
 <label for="nama">Nama</label>
 <input type="text" id="nama" name="nama" required minlength="3">
 <label for="email">Email</label>
 <input type="email" id="email" name="email" required>
 <label for="umur">Umur</label>
 <input type="number" id="umur" name="umur" min="17" max="60" required>
 <button type="submit">Kirim</button>
</form>
```

**Pengamatan:** saat tombol **Kirim** ditekan tanpa mengisi data, browser menampilkan pesan validasi dan menahan pengiriman form sampai isian memenuhi aturan.

**Hasil:**

<img width="272" height="156" alt="Screenshot 2026-10-04 130613" src="https://github.com/user-attachments/assets/9154d87a-189b-4bbe-9d61-34483ab3985e" />---

### 7. Membuat Halaman Semantic HTML

**Penjelasan:** Semantic HTML memakai elemen yang maknanya jelas sehingga struktur halaman mudah dipahami oleh developer, browser, mesin pencari, dan screen reader.

```html
<!DOCTYPE html>
<html>
<head><title>Portal Mahasiswa</title></head>
<body>
<header><h1>Portal Mahasiswa</h1></header>
<nav>
 <a href="#">Beranda</a>
 <a href="#">Profil</a>
 <a href="#">Kontak</a>
</nav>
<main>
 <section>
 <h2>Informasi Akademik</h2>
 <article>
 <h3>Praktikum HTML Lanjutan</h3>
 <p>Mahasiswa mempelajari tabel, form, semantic HTML,
 multimedia, dan validasi.</p>
 </article>
 </section>
 <aside>Informasi tambahan mahasiswa.</aside>
</main>
<footer><p>&copy; 2026 Teknik Informatika</p></footer>
</body>
</html>
```

**Hasil:**

<img width="415" height="236" alt="Screenshot 2026-10-04 130631" src="https://github.com/user-attachments/assets/5bc2919a-99f7-4e8c-b2f8-4d77807655cf" />---

### 8. Menambahkan Multimedia

**Penjelasan:** Elemen `<audio>` dan `<video>` memutar media langsung di browser. Atribut `controls` menampilkan tombol kontrol (play, pause, volume). Teks di dalam elemen menjadi *fallback* jika browser tidak mendukung.

Struktur folder media:

```
praktikum-2-html-lanjutan/
├── index.html
└── media/
    ├── audio.mp3
    └── video.mp4
```

```html
<h2>Audio</h2>
<audio controls>
 <source src="media/audio.mp3" type="audio/mpeg">
 Browser tidak mendukung audio.
</audio>

<h2>Video</h2>
<video controls width="480">
 <source src="media/video.mp4" type="video/mp4">
 Browser tidak mendukung video.
</video>
```

**Hasil:**

<img width="417" height="380" alt="Screenshot 2026-10-04 130713" src="https://github.com/user-attachments/assets/82dd2cde-b8f1-475d-b6fa-4fb3f7c81250" />---

## Proyek Mini: Form Biodata Mahasiswa

**Deskripsi:** Halaman biodata mahasiswa yang menggabungkan seluruh materi praktikum:

| Komponen | Implementasi |
|---|---|
| Semantic structure | `header`, `nav`, `main`, `section`, `footer` |
| Tabel data | Tabel biodata (NIM, Nama, Program Studi) |
| Form | Input teks, email, select, dan textarea |
| Validasi dasar | Atribut `required` pada seluruh input |
| Multimedia | Elemen `<video>` / `<audio>` |

```html
<!DOCTYPE html>
<html>
<head><title>Biodata Mahasiswa</title></head>
<body>
<header><h1>Biodata Mahasiswa</h1></header>
<nav>
 <a href="index.html">Beranda</a>
 <a href="#biodata">Biodata</a>
 <a href="#form">Form</a>
</nav>
<main>
<section id="biodata">
 <h2>Data Mahasiswa</h2>
 <table border="1">
 <tr><th>Data</th><th>Keterangan</th></tr>
 <tr><td>NIM</td><td>312510141</td></tr>
 <tr><td>Nama</td><td>Fajar Dwi Santoso</td></tr>
 <tr><td>Program Studi</td><td>Teknik Informatika</td></tr>
 </table>
</section>

<section id="form">
 <h2>Form Biodata</h2>
 <form>
 <label for="nama">Nama</label>
 <input type="text" id="nama" name="nama" required>
 <br><br>
 <label for="email">Email</label>
 <input type="email" id="email" name="email" required>
 <br><br>
 <label for="prodi">Program Studi</label>
 <select id="prodi" name="prodi" required>
 <option value="">-- Pilih --</option>
 <option value="ti">Teknik Informatika</option>
 <option value="si">Sistem Informasi</option>
 </select>
 <br><br>
 <label for="alamat">Alamat</label><br>
 <textarea id="alamat" name="alamat" required></textarea>
 <br><br>
 <button type="submit">Simpan</button>
 <button type="reset">Reset</button>
 </form>
</section>

<section id="multimedia">
 <h2>Video Perkenalan</h2>
 <video controls width="480">
 <source src="media/video.mp4" type="video/mp4">
 Browser tidak mendukung video.
 </video>
</section>
</main>
<footer><p>&copy; 2026 Teknik Informatika</p></footer>
</body>
</html>
```

> Kode modul belum memuat elemen multimedia, sehingga bagian `<section id="multimedia">` ditambahkan sendiri agar memenuhi ketentuan tugas.

**Hasil:**

<img width="577" height="525" alt="Screenshot 2026-10-04 130749" src="https://github.com/user-attachments/assets/b6f29103-937e-448b-b9c2-5e894674852c" />

<img width="587" height="286" alt="Screenshot 2026-10-04 130810" src="https://github.com/user-attachments/assets/0b883269-19f4-426e-92fb-9bd1e3652733" />

---



## Cara Menjalankan

1. Clone repository:
   ```bash
   git clone https://github.com/<username>/Lab2Web.git
   ```
2. Masuk ke folder proyek:
   ```bash
   cd Lab2Web
   ```
3. Buka `index.html` dengan browser (klik dua kali, atau gunakan ekstensi *Live Server* di VS Code).

## Kesimpulan

Melalui Praktikum 2 ini, saya mempelajari cara menyusun data dengan tabel, membuat form dengan berbagai jenis input, menerapkan validasi dasar HTML5, menyusun halaman dengan semantic HTML, serta menyisipkan audio dan video. Seluruh materi digabungkan dalam proyek mini Biodata Mahasiswa yang menunjukkan bagaimana elemen-elemen tersebut bekerja bersama dalam satu halaman web.
