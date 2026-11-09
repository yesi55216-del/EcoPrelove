# EcoPreloved - Platform Marketplace Preloved Ramah Lingkungan

EcoPreloved (EcoMarket) adalah aplikasi web marketplace berbasis Single Page Application (SPA) yang dirancang untuk mendukung konsep ekonomi sirkular melalui transaksi barang bekas (preloved) berkualitas. Platform ini dilengkapi dengan integrasi AI Assistant (Google Gemini), sistem pesan instan antara pembeli dan penjual, dashboard manajemen penjual, dukungan PWA (Progressive Web App), serta fitur multi-bahasa (Indonesian & English).

## Fitur Utama

- **Katalog & Filter Produk Interaktif**: Pencarian real-time berdasarkan kata kunci, kategori (Fashion, Buku, Elektronik, Hobi & Koleksi), serta pengurutan harga (terendah/tertinggi) dan tanggal rilis produk.
- **Asisten AI Terintegrasi (EcoBot)**: Asisten cerdas memanfaatkan Google Gemini API dengan alur terstruktur untuk memberikan rekomendasi produk, navigasi kategori, dan edukasi seputar gaya hidup ramah lingkungan.
- **Sistem Chat Pembeli & Penjual**: Fitur komunikasi dua arah berbasis antarmuka pesan instan, mendukung penyimpanan riwayat percakapan di penyimpanan lokal (*LocalStorage*) dan notifikasi pesan otomatis saat transaksi.
- **Dashboard Penjual (Seller Dashboard)**: Ringkasan statistik penjualan, rating, total produk, manajemen inventaris (tambah, edit, hapus produk), serta pengelolaan kotak masuk pesan pembeli.
- **Keranjang Belanja & Simulasi Checkout**: Perhitungan subtotal, estimasi ongkos kirim, proteksi asuransi eco-friendly, hingga pembaruan otomatis status produk menjadi *Sold Out*.
- **Dukungan Multi-bahasa (Multilingual)**: Manajemen alih bahasa secara dinamis antara Bahasa Indonesia dan Bahasa Inggris, mencakup penyesuaian format mata uang (IDR/USD) dan tanggal.
- **Progressive Web App (PWA)**: Dilengkapi dengan Service Worker dan Web App Manifest untuk kemampuan akses *offline* serta penginstalan aplikasi di perangkat seluler maupun desktop.
- **Halaman Pengujian & Demo**: Menyediakan suite pengujian internal (`test.html`) dan halaman demonstrasi fitur (`demo.html`) untuk pengujian responsivitas, performa, dan kompatibilitas peramban.

## Arsitektur & Teknologi

- **Frontend**: HTML5 Semantic Markup, Custom CSS3 (CSS Variables, Flexbox, CSS Grid), Vanilla JavaScript (ES6+ Modules) tanpa ketergantungan pada *framework* JavaScript eksternal.
- **AI Engine**: Google Gemini API (`gemini-1.5-flash`) untuk pemrosesan teks dan rekomendasi konteks produk.
- **PWA & Caching**: Service Worker API untuk caching aset dan strategi *offline-first*.
- **Penyimpanan Data**: Persistent LocalStorage untuk sesi pengguna, status keranjang, inventaris produk, dan riwayat pesan chat.
- **Ikonografi & Tipografi**: Font Awesome 6.5.1 dan Google Fonts (Inter).

## Struktur Berkas Repositori

```
EcoPreloved/
├── index.html              # Halaman utama aplikasi (SPA Client)
├── demo.html               # Halaman demonstrasi fitur platform
├── test.html               # Suite pengujian internal aplikasi
├── seller-dashboard.html   # Antarmuka Dashboard Penjual
├── style.css               # Gaya CSS dasar, layout utama, dan variabel CSS
├── components.css          # Gaya komponen UI (tombol, kartu, modal, filter)
├── chat.css                # Gaya antarmuka chat dan widget EcoBot
├── seller.css              # Gaya modal pengajuan penjualan barang
├── seller-dashboard.css    # Gaya khusus antarmuka Dashboard Penjual
├── main.js                 # Inisialisasi aplikasi, alur utama, dan event listener
├── components.js           # Komponen rendering produk, kategori, dan modal
├── auth.js                 # Logika autentikasi pengguna dan sesi
├── cart.js                 # Logika keranjang belanja dan transaksi checkout
├── chat.js                 # Logika interaksi EcoBot AI dan pesan instan
├── data.js                 # Data mock awal (kategori, produk, pengguna, helper)
├── translations.js         # Kamus bahasa (ID & EN) dan TranslationManager
├── seller-dashboard.js     # Logika bisnis dan manajemen data pada Dashboard Penjual
├── manifest.json           # Konfigurasi Web App Manifest untuk PWA
└── sw.js                   # Service Worker untuk manajemen cache dan fungsi offline
```

## Panduan Penggunaan & Instalasi

### Prasyarat

- Peramban web modern yang mendukung ES6, LocalStorage, dan Service Worker (seperti Google Chrome, Mozilla Firefox, Microsoft Edge, atau Safari).
- Server lokal opsional (seperti Live Server pada VS Code, XAMPP, Nginx, atau HTTP Server Node.js) untuk performa Service Worker yang optimal.

### Langkah-Langkah

1. Salin atau *clone* repositori ini ke direktori lokal Anda:
   ```bash
   git clone https://github.com/username/WebOnlineShop.git
   ```

2. Buka folder proyek dan jalankan aplikasi:
   - **Metode 1 (Tanpa Server)**: Buka berkas `index.html` langsung melalui peramban web.
   - **Metode 2 (Menggunakan Server Lokal)**: Jalankan server lokal di direktori proyek, lalu akses alamat `http://localhost:5500` (atau port yang sesuai) melalui peramban.

3. Untuk mengakses Dashboard Penjual:
   - Buka berkas `seller-dashboard.html` atau pilih menu "Jual Barang" di halaman utama.

4. Untuk menjalankan suite pengujian internal:
   - Akses berkas `test.html` pada peramban web Anda.

## Hak Cipta & Lisensi

Proyek ini dikembangkan sebagai solusi marketplace barang preloved berbasis web yang berfokus pada keberlanjutan dan efisiensi energi.
