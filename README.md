# Yuan Studio

Dashboard manajemen konten & penjadwalan posting untuk YouTube, TikTok, Instagram, Facebook, dan Threads — dikemas dalam **satu file HTML** tanpa dependency eksternal (selain Google Fonts).

![status](https://img.shields.io/badge/status-active-brightgreen) ![type](https://img.shields.io/badge/type-single--file--html-orange)

## ✨ Fitur

### Navigasi & Platform
- Routing SPA antar 7 section (Dashboard, Riwayat Aktivitas, Content Pool, Media Manual, Text Pool, Jadwal Posting, Pengaturan)
- Connect/disconnect akun per platform, tombol Start (simulasi upload), Detail (riwayat per platform)
- Sidebar akun menunjukkan status koneksi secara real-time

### Konten & Jadwal
- **Antrian Konten** dengan search/filter, tambah/hapus/posting
- **Kalender visual** di Jadwal Posting — klik tanggal untuk filter jadwal hari itu
- **Bulk Jadwal** — tambah banyak konten sekaligus dengan interval otomatis
- **Content Pool** dengan status Draft/Ready, filter tab, dan preview
- **Preview per platform** — mockup tampilan post untuk IG, TikTok, YouTube, Facebook, Threads

### Media & Teks
- **Media Manual** — upload file dari device, baca metadata & thumbnail, tagging/kategori dengan filter
- **Text Pool** — simpan caption, mendukung template variabel `{judul}`, `{tanggal}`, dll dengan form isi otomatis saat disalin

### Insight & Notifikasi
- **Grafik performa** sukses/gagal per platform
- **Rekomendasi waktu posting terbaik** berdasarkan histori
- **Notifikasi in-app** (bell icon) untuk kejadian gagal & reminder H-1 jam sebelum jadwal tayang
- **Riwayat Aktivitas** lengkap dengan search

### Pengaturan & Data
- Export/Import backup data (JSON)
- Reset semua data
- Dark/Light mode toggle
- Preferensi zona waktu, notifikasi, auto-retry

## 🛠️ Tech Stack

- HTML, CSS (custom properties untuk theming), vanilla JavaScript — tanpa framework/build step
- Font: [Space Grotesk](https://fonts.google.com/specimen/Space+Grotesk), [Inter](https://fonts.google.com/specimen/Inter), [JetBrains Mono](https://fonts.google.com/specimen/JetBrains+Mono)
- State persistence: `window.storage` API (jika tersedia) dengan fallback in-memory untuk penggunaan standalone di browser

## 🚀 Cara Pakai

1. Download `yuan-studio.html`
2. Buka langsung di browser (double click atau drag ke tab browser)
3. Semua fitur langsung berfungsi — tidak perlu server atau instalasi apapun

## ⚠️ Catatan Penting

Tombol **Connect/Start** pada tiap platform saat ini bersifat **simulasi** — belum terhubung ke API asli YouTube/TikTok/Instagram/Facebook/Threads. Untuk koneksi OAuth sungguhan dibutuhkan:

1. Registrasi OAuth App di masing-masing platform (Google Cloud Console, TikTok for Developers, Meta for Developers)
2. Backend server untuk menangani token exchange & penyimpanan client secret dengan aman
3. Endpoint refresh token

Fitur ini belum diimplementasikan karena di luar cakupan single-file HTML tanpa backend.

## 📌 Roadmap

- [ ] Integrasi OAuth nyata per platform (butuh backend)
- [ ] Multi-user / role (Admin, Editor)
- [ ] Approval flow sebelum konten dijadwalkan

## 📄 Lisensi

Proyek pribadi — bebas dimodifikasi sesuai kebutuhan.
