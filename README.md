# ☕ SmartCafe Cashier - Premium Edition v2.5

[![GitHub Pages](https://img.shields.io/badge/GitHub%20Pages-Live-success?style=flat-square&logo=github)](https://cahyohndsm.github.io/SmartCafe-Cashier/)
[![Platform](https://img.shields.io/badge/Platform-Web--Browser-amber?style=flat-square)](https://en.wikipedia.org/wiki/Web_browser)
[![License](https://img.shields.io/badge/License-MIT-blue.svg?style=flat-square)](https://opensource.org/licenses/MIT)

**SmartCafe Cashier** adalah aplikasi sistem kasir digital (*Point of Sale*) modern berbasis web yang dirancang khusus untuk efisiensi operasional kafe, kedai kopi, atau UMKM kuliner. Aplikasi ini berjalan sepenuhnya di sisi klien (*client-side*) sehingga sangat ringan, cepat, dan tidak memerlukan server atau database eksternal yang rumit. 

Aplikasi ini telah dioptimalkan untuk perangkat tablet maupun desktop kasir, serta mendukung integrasi langsung dengan mesin cetak struk kertas thermal gulung.

---

## 🚀 Fitur Unggulan

### 1. 💾 Persistensi Data Otomatis (State Management via LocalStorage)
*   **Auto-Save & Sync**: Setiap perubahan pada katalog menu—baik menambah menu baru maupun menghapus menu lama—akan langsung disimpan secara otomatis ke dalam enkripsi JSON lokal pada browser (`localStorage`).
*   **Anti-Reset Data**: Data menu yang telah dikustomisasi tidak akan hilang atau kembali ke pengaturan awal (default) meskipun halaman disegarkan (*refresh*), browser ditutup, atau perangkat dimatikan.
*   **Fallback Mechanism**: Jika memori lokal kosong (pertama kali dibuka), aplikasi akan memuat 30 daftar menu *default* siap pakai secara otomatis.

### 2. 🛒 Sistem Kasir & Kalkulasi Real-Time
*   **Manajemen Keranjang Fleksibel**: Menambah, mengurangi, atau menghapus jumlah kuantitas item pesanan dilakukan secara instan hanya dengan satu klik pada panel ringkasan belanja.
*   **Komputasi Otomatis**: Aplikasi menghitung nilai Subtotal, Pajak Pertambahan Nilai (PPN) sebesar 10%, dan Total Akhir secara *real-time* tanpa adanya *delay*.
*   **Validasi Batas Transaksi**: Mencegah proses transaksi jika keranjang kosong atau jika nominal uang tunai yang diinput oleh kasir kurang dari total tagihan.

### 3. 💳 Fleksibilitas Metode Pembayaran
*   **Simulasi Multi-Payment**: Mendukung 3 jenis opsi pembayaran populer saat ini:
    *   **Cash (Tunai)**: Membuka input nominal uang diterima dan menghitung jumlah kembalian secara otomatis.
    *   **QRIS (Dompet Digital)**: Menandai transaksi lunas melalui e-payment secara otomatis tanpa input kembalian.
    *   **Debit (Kartu Bank)**: Menandai transaksi lunas via EDC mesin bank.

### 4. 🖨️ Pratinjau & Optimalisasi Cetak Struk (Thermal Print-Ready)
*   **CSS Print Media Query**: Layout struk telah dikunci menggunakan CSS khusus printer thermal ukuran standar **80mm atau 58mm**.
*   **Clean Print Output**: Saat tombol *Print* ditekan, seluruh elemen antarmuka aplikasi (seperti tombol, formulir input, dan navigasi) akan disembunyikan secara otomatis, sehingga printer hanya akan mencetak struk belanjaan yang bersih.
*   **Marketing & Engagement**: Struk belanja secara otomatis memuat informasi dinamis tanggal cetak, rincian PPN, serta bonus informasi kredensial Wi-Fi gratis untuk meningkatkan kepuasan pelanggan di kafe.

---

## 🛠️ Arsitektur Teknologi & Library

Proyek ini dibangun menggunakan pendekatan *modern vanilla web development stack* tanpa *build-tools* eksternal untuk menjaga kecepatan pemuatan halaman tetap di bawah 1 detik:

*   **HTML5 Semantic**: Untuk struktur kerangka aplikasi yang bersih, terorganisir, dan ramah aksesibilitas.
*   **Tailwind CSS v4.0 (via CDN)**: Digunakan untuk membangun antarmuka (*User Interface*) premium, bersih, minimalis, dan sepenuhnya responsif di berbagai resolusi layar.
*   **JavaScript (ES6+)**: Mengatur seluruh logika aplikasi, mulai dari manipulasi DOM tingkat tinggi, manajemen *array* data menu, hingga kalkulasi matematika transaksi.
*   **FontAwesome v6.4.0**: Menyediakan ikon grafis vektor yang tajam untuk mempermudah navigasi visual kasir.
*   **Web Storage API**: Memanfaatkan *LocalStorage* internal browser sebagai media penyimpanan *database side* yang aman dan instan.

---

## 📂 Dokumentasi Kode & Struktur File

```text
SmartCafe-Cashier/
│
├── index.html       # Arsitektur Utama (UI Layout, CSS Tailwind, & Logika JavaScript)
└── README.md        # Dokumentasi Resmi Proyek
