# 📱 FMSGA PWA – Panduan Deploy & Instalasi

## File yang Diperlukan

```
fmsga-pwa/
├── index.html          ← App shell utama (file ini)
├── manifest.json       ← PWA manifest
├── sw.js               ← Service Worker
├── generate-icons.html ← Generator icon (buka sekali di browser)
├── icon-192.png        ← Icon app (generate dulu)
└── icon-512.png        ← Icon app besar (generate dulu)
```

---

## Langkah 1 — Generate Icon

1. Buka file `generate-icons.html` di browser
2. Klik **"Download icon-192.png"** dan **"Download icon-512.png"**
3. Letakkan kedua file PNG di folder yang sama dengan `index.html`

---

## Langkah 2 — Konfigurasi URL GAS

Buka `index.html`, cari baris:

```js
const GAS_URL = 'GANTI_DENGAN_URL_GAS_PARENT';
```

Ganti dengan URL deployment Google Apps Script parent, contoh:

```js
const GAS_URL = 'https://script.google.com/macros/s/AKfycb.../exec';
```

---

## Langkah 3 — Deploy (pilih salah satu)

### Opsi A: GitHub Pages ⭐ (Gratis, Direkomendasikan)

1. Buat repository baru di [github.com](https://github.com) (nama bebas, mis. `fmsga-app`)
2. Upload semua file ke repository
3. Buka **Settings → Pages → Source → main / (root)**
4. URL app akan menjadi: `https://[username].github.io/fmsga-app/`

### Opsi B: Netlify Drop (Paling Mudah)

1. Buka [app.netlify.com/drop](https://app.netlify.com/drop)
2. Drag & drop seluruh folder ke halaman tersebut
3. URL langsung aktif dalam hitungan detik

### Opsi C: Server Internal Rumah Sakit

Upload semua file ke web server internal (Apache/Nginx).
**Wajib HTTPS** agar Service Worker dan PWA install bisa berfungsi.

---

## Langkah 4 — Instalasi di Smartphone

### Android (Chrome) — Otomatis
Setelah membuka URL di Chrome Android, banner **"Pasang di layar utama"** akan muncul otomatis setelah beberapa detik. Ketuk **"Pasang"**.

### iPhone / iPad (Safari) — Manual
Banner panduan akan muncul otomatis. Ikuti langkah:
1. Ketuk ikon **Share** (kotak dengan panah ke atas) di Safari
2. Pilih **"Add to Home Screen"**
3. Ketuk **"Add"**

---

## Fitur PWA

| Fitur | Keterangan |
|---|---|
| 📱 Install ke Home Screen | Android otomatis, iOS via Safari |
| 🖥 Full Screen | Tampil seperti app native tanpa browser bar |
| ⚡ Splash Screen | Branded splash saat pertama buka |
| 📶 Offline Detection | Banner otomatis jika tidak ada koneksi |
| 🔄 Auto Update | Notifikasi saat ada versi baru |
| 🔒 HTTPS Ready | Wajib untuk PWA (GitHub Pages/Netlify sudah HTTPS) |

---

## Catatan Penting

- **Service Worker tidak bisa cache halaman GAS** (karena domain `script.google.com` berbeda). 
  App tetap butuh koneksi internet untuk beroperasi penuh.
- Jika URL GAS berubah (re-deploy), cukup update `GAS_URL` di `index.html` dan upload ulang.
- Untuk update app: edit file → upload ulang → user akan dapat notifikasi "Versi terbaru tersedia".

---

*Dikembangkan untuk FMSGA Integrated System – Mayapada Hospital Bandung*
*FMSGA Support MHBD · ext. 5920*
