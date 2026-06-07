# RentalMobil App

Aplikasi Desktop (Java Swing/AWT) sederhana untuk manajemen penyewaan mobil (Car Rental System). Aplikasi ini dibangun dengan mengimplementasikan pola arsitektur **MVC (Model-View-Controller)** dan menggunakan **MySQL** sebagai basis data.

## 🚀 Fitur Utama
Aplikasi ini mendukung operasi dasar CRUD (Create, Read, Update, Delete) untuk mendata peminjam mobil:
- **Simpan (Create):** Menambahkan data peminjam baru (Nama, Lama Sewa, Jenis Kelamin, Jenis Mobil).
- **Tampil (Read):** Menampilkan daftar riwayat peminjam mobil di dalam tabel antarmuka.
- **Ubah (Update):** Mengubah data peminjam (Lama Sewa, Jenis Kelamin, Jenis Mobil) berdasarkan Nama.
- **Hapus (Delete):** Menghapus data peminjam dari database.
- **Form Reset (Baru):** Mengosongkan form isian dengan cepat.

## 🛠️ Teknologi yang Digunakan
- **Bahasa Pemrograman:** Java (JDK 8 atau lebih baru)
- **GUI Framework:** Java Swing
- **Arsitektur:** MVC (Model, View, Controller)
- **Database:** MySQL
- **IDE:** NetBeans IDE

## 📂 Struktur Proyek
- `src/com/controller`: Interface controller untuk mengatur alur logika CRUD (`controller_mobil.java`).
- `src/com/model`: Implementasi logika bisnis dan koneksi query database (`model_mobil.java`).
- `src/com/view`: Antarmuka grafis pengguna atau GUI (`form_mobil.java` & `.form`).
- `src/com/koneksi`: Kelas untuk menangani konfigurasi driver dan koneksi ke database MySQL (`koneksi.java`).

## ⚙️ Persyaratan Sistem & Instalasi
1. Pastikan **Java Development Kit (JDK)** telah terinstal di komputer.
2. Pastikan server lokal seperti **XAMPP / WAMP** berjalan (khususnya module MySQL).
3. Buat database baru di MySQL dengan nama `rentalmobil`.
4. Import atau buat tabel bernama `rental` di database tersebut. *(Terdapat file sql pendukung di folder `Data Basenya/` jika tersedia).*
    - Kolom yang dibutuhkan: `nama_peminjam` (VARCHAR/PK), `lama_sewa` (VARCHAR/INT), `kelamin_peminjam` (VARCHAR), `jenis_mobil` (VARCHAR).
5. Buka proyek ini menggunakan **NetBeans IDE**.
6. Pastikan library **MySQL JDBC Driver** sudah ditambahkan ke *Libraries* proyek atau akan diload otomatis lewat `Class.forName()`.
7. Jalankan proyek (Run Project / `Shift+F6` di `form_mobil.java`).

## 👨‍💻 Cara Penggunaan
1. Buka aplikasi.
2. Masukkan nama peminjam pada kolom **Nama**.
3. Masukkan lama penyewaan pada kolom **Lama Sewa** (contoh: 2 hari).
4. Pilih **Jenis Kelamin** melalui Radio Button.
5. Pilih **Jenis Mobil** melalui Dropdown (Combobox).
6. Klik tombol **Simpan** untuk memasukkan ke database.
7. Untuk mengubah atau menghapus data, **Klik** salah satu baris pada tabel, lalu klik tombol **Ubah** atau **Hapus**.

---
*Proyek ini dirancang sebagai sarana pembelajaran dasar implementasi Java Desktop, MVC, dan JDBC MySQL.*