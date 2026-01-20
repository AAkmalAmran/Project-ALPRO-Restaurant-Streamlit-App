# Sistem Manajemen Restoran (Restaurant Management System)

Repository ini berisi **Aplikasi Sistem Informasi Restoran** berbasis web yang dibangun menggunakan **Python (Streamlit)** dan **MySQL**. Proyek ini dibuat untuk memenuhi **Tugas Besar Kolaborasi Mata Kuliah Algoritma Pemrograman (Alpro) dan Sistem Basis Data (SBD)**.

Aplikasi ini memudahkan pengelolaan data restoran, mulai dari manajemen menu, pemesanan (order), hingga pencatatan data pelanggan.

## Teknologi yang Digunakan
* **Bahasa Pemrograman:** Python
* **Framework GUI:** [Streamlit](https://streamlit.io/)
* **Database:** MySQL
* **Library Pendukung:**
    * `mysql-connector-python` (Koneksi Database)
    * `pandas` (Manipulasi Data)
    * `Pillow` (Pengolahan Citra/Logo)

## Struktur Project


```

📁 Project-ALPRO-Restaurant-Streamlit-App
│
├── 📂 Tugas Besar Algoritma Pemrograman x Sistem Basis Data
│   ├── app.py                 # File utama aplikasi Streamlit
│   ├── restaurant_copy.sql    # File dump database MySQL
│   └── LOGO.jpeg              # Logo restoran untuk UI
│
└── README.md                  # Dokumentasi proyek

```

## Fitur Utama

### 1. Manajemen Menu (CRUD)
* Melihat daftar menu makanan dan minuman.
* Menambah menu baru ke database.
* Mengedit harga atau detail menu.
* Menghapus menu yang tidak tersedia.

### 2. Sistem Pemesanan (Ordering)
* Mencatat pesanan pelanggan.
* Menghitung total harga secara otomatis.
* Menyimpan riwayat transaksi ke database.

### 3. Database Terintegrasi
* Menggunakan skema relasional untuk tabel `Menu`, `Orders`, dan `Customers` (sesuai file `restaurant_copy.sql`).

## Cara Menjalankan Aplikasi

Ikuti langkah-langkah berikut untuk menjalankan proyek ini di komputer lokal:

### 1. Persiapan Database
1.  Pastikan **XAMPP** (atau MySQL Server lainnya) sudah aktif.
2.  Buka **phpMyAdmin** (biasanya di `http://localhost/phpmyadmin`).
3.  Buat database baru dengan nama **`restaurant`**.
4.  Import file **`restaurant_copy.sql`** ke dalam database tersebut.

### 2. Instalasi Library
Buka terminal atau command prompt, lalu install library yang dibutuhkan:

```bash
pip install streamlit mysql-connector-python pandas

```

### 3. Konfigurasi Koneksi (Penting!)

Buka file `app.py` dengan text editor (VS Code, Notepad, dll). Cari bagian koneksi database dan pastikan konfigurasi sesuai dengan XAMPP Anda:

```python
# Contoh konfigurasi di app.py
mydb = mysql.connector.connect(
  host="localhost",
  user="root",      # Default user XAMPP
  password="",      # Default password XAMPP (kosong)
  database="restaurant"
)

```

### 4. Jalankan Aplikasi

Arahkan terminal ke folder tempat `app.py` berada, lalu jalankan perintah:

```bash
cd "Tugas Besar Algoritma Pemrograman x Sistem Basis Data"
streamlit run app.py

```

Aplikasi akan otomatis terbuka di browser Anda (biasanya di `http://localhost:8501`).

---

**Catatan:**
Jika gambar logo tidak muncul, pastikan file `LOGO.jpeg` berada dalam satu folder dengan `app.py`.

```

```
