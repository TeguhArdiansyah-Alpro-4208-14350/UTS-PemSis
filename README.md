## Teguh Ardiansyah
## A11.2022.14350
##### belum 100% selesai pak,, jadi ngumpul seadanya aja hehe
# Inventory Management API

## Deskripsi Proyek

Aplikasi ini dibuat untuk mengelola persediaan barang dalam sebuah toko, mencakup pengelolaan:
- Barang (Items)
- Kategori barang (Categories)
- Pemasok (Suppliers)
- Admin (Admins)

Setiap data dikelola oleh admin yang bertanggung jawab.

Framework: **Express.js**  
Database: **MySQL**  
Containerisasi: **Docker & Docker Compose**

---

## Alur Pengerjaan Proyek

- **Inisialisasi Proyek**
  - Membuat folder project dan melakukan `npm init -y`.
  - Install dependency utama: `express`, `sequelize`, `mysql2`, `dotenv`, `nodemon`.

- **Setup Struktur Folder**
  - Membuat struktur `src/` berisi:
    - `models/` untuk Sequelize model (Admin, Item, Category, Supplier).
    - `controllers/` untuk logika pengolahan data.
    - `routes/` untuk endpoint API.
    - `config/` untuk koneksi database.
    - `migrations/` dan `seeders/` untuk setup database.

- **Koneksi ke Database**
  - Membuat file konfigurasi Sequelize dan menghubungkan aplikasi ke MySQL.
  - Membuat file `.env` untuk environment variable (DB_HOST, DB_USER, DB_PASS, dll).

- **Pembuatan Model**
  - Membuat model Sequelize untuk:
    - `Admin`
    - `Item`
    - `Category`
    - `Supplier`
  - Menetapkan relasi antar tabel sesuai requirement.

- **Pembuatan API CRUD**
  - Membuat endpoint untuk:
    - Create & Read Item
    - Create & Read Category
    - Create & Read Supplier

- **Pembuatan Fitur Laporan**
  - Menampilkan:
    - Ringkasan stok barang (stok total, total nilai, rata-rata harga).
    - Daftar barang dengan stok di bawah ambang batas.
    - Laporan barang berdasarkan kategori.
    - Ringkasan per kategori (jumlah barang, total nilai, rata-rata harga).
    - Ringkasan barang per supplier (jumlah barang & total nilai).

- **Setup Docker**
  - Membuat `docker-compose.yml`:
    - Service untuk backend (Node.js Express).
    - Service untuk database (MySQL).
  - Konfigurasi agar otomatis membuat database saat container MySQL hidup.

- **Testing API**
  - Menggunakan Postman untuk:
    - Menambah data admin, item, kategori, supplier.
    - Mengecek laporan stok.
    - Menguji endpoint laporan kategori dan supplier.

- **Finalisasi Proyek**
  - Cleanup kode dan file yang tidak diperlukan.
  - Dokumentasi endpoint sederhana.
  - Push project ke GitHub.

---

## Cara Menjalankan Project

1. Pastikan Docker sudah terinstall.
2. Clone repo ini ke lokal.
3. Jalankan perintah berikut:


docker-compose up --build


4. Akses server di:


http://localhost:3000/


5. Gunakan Postman atau tools API client lain untuk mengakses endpoint.

---

## Teknologi yang Digunakan

- Node.js (Express.js)
- MySQL
- Sequelize ORM
- Docker & Docker Compose
- Postman (untuk testing API)

---

## Fitur Utama

- **CRUD Data**:
  - Items
  - Categories
  - Suppliers

- **Laporan Data**:
  - Ringkasan stok
  - Barang dengan stok rendah
  - Barang per kategori
  - Ringkasan per kategori
  - Ringkasan per pemasok
  - Ringkasan keseluruhan sistem
```
# UTS-PemSis
