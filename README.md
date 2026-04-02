# Laporan Praktikum Pertemuan 1 - 4 

|                |                    |
| ------------------ | ------------------ |
|      _Nama_    | RO'UF MUHAMMAD FAUZAN |
|      _NIM_     |      312410157     |
|     _Kelas_    |      I241A    |
|  _Mata Kuliah_ | Bahasa Pemrograman Web 2 |

## CodeIgniter 4 Framework

## What is CodeIgniter?

CodeIgniter is a PHP full-stack web framework that is light, fast, flexible and secure.
More information can be found at the [official site](https://codeigniter.com).

This repository holds the distributable version of the framework.
It has been built from the
[development repository](https://github.com/codeigniter4/CodeIgniter4).

More information about the plans for version 4 can be found in [CodeIgniter 4](https://forum.codeigniter.com/forumdisplay.php?fid=28) on the forums.

You can read the [user guide](https://codeigniter.com/user_guide/)
corresponding to the latest version of the framework.

## Important Change with index.php

`index.php` is no longer in the root of the project! It has been moved inside the *public* folder,
for better security and separation of components.

This means that you should configure your web server to "point" to your project's *public* folder, and
not to the project root. A better practice would be to configure a virtual host to point there. A poor practice would be to point your web server to the project root and expect to enter *public/...*, as the rest of your logic and the
framework are exposed.

**Please** read the user guide for a better explanation of how CI4 works!

## Repository Management

We use GitHub issues, in our main repository, to track **BUGS** and to track approved **DEVELOPMENT** work packages.
We use our [forum](http://forum.codeigniter.com) to provide SUPPORT and to discuss
FEATURE REQUESTS.

This repository is a "distribution" one, built by our release preparation script.
Problems with it can be raised on our forum, or as issues in the main repository.

## Contributing

We welcome contributions from the community.

Please read the [*Contributing to CodeIgniter*](https://github.com/codeigniter4/CodeIgniter4/blob/develop/CONTRIBUTING.md) section in the development repository.

## Server Requirements

PHP version 8.2 or higher is required, with the following extensions installed:

- [intl](http://php.net/manual/en/intl.requirements.php)
- [mbstring](http://php.net/manual/en/mbstring.installation.php)

> [!WARNING]
> - The end of life date for PHP 7.4 was November 28, 2022.
> - The end of life date for PHP 8.0 was November 26, 2023.
> - The end of life date for PHP 8.1 was December 31, 2025.
> - If you are still using below PHP 8.2, you should upgrade immediately.
> - The end of life date for PHP 8.2 will be December 31, 2026.

Additionally, make sure that the following extensions are enabled in your PHP:

- json (enabled by default - don't turn it off)
- [mysqlnd](http://php.net/manual/en/mysqlnd.install.php) if you plan to use MySQL
- [libcurl](http://php.net/manual/en/curl.requirements.php) if you plan to use the HTTP\CURLRequest library

# Lab8Web

# Praktikum 1

<img width="1904" height="869" alt="571112352-8963c8fb-bdaa-4d9a-a5e6-b23fce5a6eb1" src="https://github.com/user-attachments/assets/f63dcbeb-6c05-476e-9e1e-12899c415e09" />

<img width="1914" height="770" alt="571112405-cdaf2ec1-4354-44fe-b700-35bda96daaf4" src="https://github.com/user-attachments/assets/c04b6aae-ff0f-40ce-8999-e39cdb8fa37e" />

<img width="1913" height="884" alt="571112444-75c12170-921b-477f-b17d-6de83b58110e" src="https://github.com/user-attachments/assets/cd869e24-d902-46ff-ae6c-51595f65836f" />


**Penjelasan Praktikum 1**
1. Persiapan dan Konfigurasi WebserverSebelum menginstal CodeIgniter 4, Anda perlu mengaktifkan beberapa ekstensi PHP melalui file php.ini agar framework dapat berjalan dengan baik.Ekstensi yang diperlukan: php-json, php-mysqlnd, php-xml, php-intl, dan libcurl (opsional).Cara aktivasi: Buka XAMPP Control Panel, klik tombol Config pada modul Apache, lalu pilih PHP (php.ini).Edit file: Cari baris ekstensi tersebut dan hilangkan tanda titik koma (;) di depannya untuk mengaktifkan. Setelah itu, restart Apache.2. Instalasi CodeIgniter 4Praktikum ini menggunakan metode instalasi manual:Unduh file CodeIgniter dari situs resminya.Ekstrak file tersebut ke dalam folder htdocs/lab11_ci.Ubah nama folder framework menjadi ci4.Akses melalui browser di alamat: http://localhost/lab11_ci/ci4/public/.3. Menjalankan Command Line Interface (CLI)CodeIgniter 4 menyediakan alat bantu berbasis teks (CLI) yang disebut Spark.Buka Command Prompt (CMD) dan arahkan ke direktori kerja project (xampp/htdocs/lab11_ci/ci4/).Gunakan perintah php spark untuk melihat daftar perintah yang tersedia.4. Mengaktifkan Mode DebuggingSecara default, CI4 menyembunyikan detail kesalahan (error) untuk keamanan.Langkah: Ubah nama file env di root direktori menjadi .env.Konfigurasi: Buka file tersebut dan ubah nilai CI_ENVIRONMENT dari production menjadi development.Ini akan membantu developer melihat pesan error yang spesifik jika terjadi kesalahan kode.5. Struktur Direktori dan Konsep MVCCodeIgniter 4 menggunakan pola Model-View-Controller (MVC):Model: Mengurusi pemodelan dan pengolahan data (database).View: Mengurusi tampilan atau User Interface (HTML/CSS).Controller: Penghubung antara Model dan View yang berisi logika program.Folder Utama: Fokus pengembangan ada di folder app (area kerja) dan folder public (tempat aset seperti CSS dan gambar).6. Routing dan Controller BaruRouting mengatur rute permintaan (request) untuk menentukan Controller mana yang akan merespon.Konfigurasi rute berada di file app/config/Routes.php.Anda bisa membuat route manual, contohnya: $routes->get('/about', 'Page::about'); yang mengarahkan alamat /about ke class Page dengan fungsi about.7. Membuat Layout SederhanaUntuk membuat tampilan yang konsisten, gunakan sistem template:Simpan file CSS (misal: style.css) di folder public.Pisahkan bagian tampilan menjadi header.php dan footer.php di dalam folder app/view/template/.Gunakan fungsi $this->include() untuk menggabungkan header, isi konten, dan footer dalam satu halaman.

**Praktikum 2**
<img width="1904" height="869" alt="571112352-8963c8fb-bdaa-4d9a-a5e6-b23fce5a6eb1" src="https://github.com/user-attachments/assets/f63dcbeb-6c05-476e-9e1e-12899c415e09" />

<img width="1914" height="770" alt="571112405-cdaf2ec1-4354-44fe-b700-35bda96daaf4" src="https://github.com/user-attachments/assets/c04b6aae-ff0f-40ce-8999-e39cdb8fa37e" />

<img width="1913" height="884" alt="571112444-75c12170-921b-477f-b17d-6de83b58110e" src="https://github.com/user-attachments/assets/cd869e24-d902-46ff-ae6c-51595f65836f" />

**Penjelasan**
1. Persiapan DatabaseLangkah pertama dalam membangun aplikasi CRUD (Create, Read, Update, Delete) adalah menyiapkan struktur data pada MySQL.Membuat Database: Gunakan perintah CREATE DATABASE lab_ci4;.Membuat Tabel: Buat tabel bernama artikel dengan kolom sebagai berikut:id: Primary Key dengan auto increment.judul, isi, gambar, status, dan slug untuk menyimpan konten artikel.Konfigurasi Koneksi: Hubungkan aplikasi dengan database melalui file .env dengan mengatur hostname, database name (lab_ci4), username (root), dan password.2. Pembuatan ModelModel berfungsi untuk menangani segala instruksi yang berkaitan dengan data.Buat file ArtikelModel.php di direktori app/Models.Model ini harus mendefinisikan nama tabel (artikel), primary key, dan kolom mana saja yang diperbolehkan untuk diisi melalui variabel $allowedFields.3. Pembuatan Controller dan View (Read)Bagian ini menangani pengambilan data dari database untuk ditampilkan kepada pengguna.Controller: Buat file Artikel.php di app/Controllers yang memanggil ArtikelModel dan menggunakan fungsi findAll() untuk mengambil semua data.View: Buat file index.php di folder app/views/artikel untuk menampilkan daftar artikel menggunakan perulangan foreach.Jika data masih kosong, sistem akan menampilkan pesan "Belum ada data".4. Fitur Detail ArtikelFitur ini memungkinkan pengguna melihat isi lengkap sebuah artikel saat judulnya diklik.Fungsi View: Tambahkan method view($slug) pada Controller yang mencari data berdasarkan slug menggunakan fungsi where()->first().Routing: Tambahkan aturan di app/config/Routes.php agar URL seperti /artikel/judul-berita dapat dikenali oleh sistem.5. Menu Admin dan Operasi CRUD (Update & Delete)Menu admin digunakan untuk mengelola seluruh data artikel melalui antarmuka tabel.Daftar Admin: Method admin_index() menampilkan tabel yang berisi kolom aksi seperti "Ubah" dan "Hapus".Tambah Data (Create): Method add() melakukan validasi input (seperti judul wajib diisi) sebelum menyimpan data baru ke database.Ubah Data (Update): Method edit($id) mengambil data lama berdasarkan ID, menampilkan form dengan data tersebut, lalu melakukan pembaruan jika ada perubahan.Hapus Data (Delete): Method delete($id) akan menghapus record dari database berdasarkan ID yang dipilih.

**Praktikum 3**
<img width="1919" height="949" alt="Cuplikan layar 2026-03-02 104132" src="https://github.com/user-attachments/assets/c4eb83b5-1f58-4856-b21a-6f679983e496" />

<img width="1919" height="945" alt="Cuplikan layar 2026-03-02 104354" src="https://github.com/user-attachments/assets/3df6dc84-c9dc-4a1d-ad01-99fe9b4d8d62" />

<img width="1918" height="945" alt="Cuplikan layar 2026-03-02 105756" src="https://github.com/user-attachments/assets/9be480d5-10d8-4f02-83a5-14a60da3c2da" />

<img width="1919" height="946" alt="Cuplikan layar 2026-03-02 113130" src="https://github.com/user-attachments/assets/75bbe583-b808-4b1f-b8e6-a56af7f80048" />

<img width="1919" height="956" alt="Cuplikan layar 2026-03-02 113815" src="https://github.com/user-attachments/assets/d3228baf-3759-417c-b80c-9fb44cdf8e76" />

<img width="1915" height="951" alt="Cuplikan layar 2026-03-02 114317" src="https://github.com/user-attachments/assets/69babf84-e89e-4e58-87b4-8eaa0efd37e7" />

**Peenjelasan**
1. Konsep View Layout (Template Utama)View Layout memungkinkan Anda membuat satu template induk (master) yang mendefinisikan struktur dasar HTML. Bagian konten yang berubah-ubah pada setiap halaman didefinisikan menggunakan Section.Membuat Layout Utama (main.php):
Template ini diletakkan di folder app/Views/layout/. Di dalamnya terdapat fungsi <?= $this->renderSection('content') ?> yang berfungsi sebagai wadah (placeholder) untuk konten dinamis dari halaman lain.Modifikasi File View:Untuk menggunakan layout ini, halaman seperti home.php harus menggunakan fungsi:$this->extend('layout/main'): Memberitahu CI4 untuk menggunakan template induk.$this->section('content') dan $this->endSection(): Membungkus konten spesifik halaman tersebut agar masuk ke dalam placeholder yang ada di layout utama.2. Konsep View Cell (Komponen Modular)View Cell adalah fitur untuk memanggil komponen tampilan tertentu secara modular. Fitur ini sangat berguna untuk elemen yang muncul berulang kali di berbagai halaman namun memiliki logika data sendiri, seperti sidebar atau daftar artikel terbaru.Membuat Class View Cell:
Anda membuat class di folder app/Cells/ (misalnya ArtikelTerkini.php) yang berisi logika pengambilan data dari database menggunakan Model.Membuat Tampilan Komponen:
Hasil olahan data dari class tersebut dikirim ke file view kecil di folder app/Views/components/ untuk dirender menjadi HTML (seperti daftar <ul> dan <li>).Cara Memanggil:
Di dalam Layout Utama, Anda cukup memanggilnya dengan satu baris kode: <?= view_cell('App\\Cells\\ArtikelTerkini::render') ?>.

**Praktikum 4**
<img width="959" height="443" alt="571117217-f0853d25-cf60-473c-b4c8-e2132eb7a8b2" src="https://github.com/user-attachments/assets/02a91bff-7c48-4a31-8ef5-3912a9dcf36e" />

**Penjelasan**
1. Persiapan DatabaseLangkah awal adalah menyiapkan tabel user pada database MySQL untuk menyimpan data kredensial. Struktur tabelnya adalah sebagai berikut:id: INT(11), Primary Key, auto_increment.username: VARCHAR(200).useremail: VARCHAR(200).userpassword: VARCHAR(200).2. Pembuatan Model (UserModel.php)Model ini berfungsi untuk berinteraksi dengan tabel user di database.Lokasi: app/Models/UserModel.php.Konfigurasi: Menentukan nama tabel (user), primary key (id), dan field yang diizinkan untuk diisi (username, useremail, userpassword).3. Pembuatan Controller (User.php)Controller ini menangani logika utama login dan logout.Method login(): Mengambil input email dan password dari form. Jika data cocok dengan database (menggunakan password_verify), data user akan disimpan ke dalam Session.Method logout(): Menghapus seluruh data session yang aktif dan mengarahkan kembali user ke halaman login.4. Pembuatan View Login (login.php)Halaman antarmuka bagi user untuk memasukkan email dan password.Lokasi: app/views/user/login.php.Fitur: Form menggunakan metode POST dan menyertakan pesan kesalahan (Flashdata) jika login gagal.5. Database SeederDigunakan untuk memasukkan data uji coba (dummy data) ke database melalui CLI.Perintah: php spark make:seeder UserSeeder.Data: Membuat user dengan username 'admin' dan password 'admin123' yang sudah di-hash.Eksekusi: Jalankan php spark db:seed UserSeeder.6. Implementasi Auth FilterFilter digunakan untuk membatasi akses ke halaman tertentu (misalnya halaman admin) agar hanya bisa diakses oleh user yang sudah login.Logika Filter: Jika session logged_in tidak ditemukan, user akan otomatis dialihkan ke halaman login.Konfigurasi: Daftarkan alias filter pada app/Config/Filters.php dan terapkan pada grup rute admin di app/Config/Routes.php.
