Deskripsi Aplikasi FMS GA — Mayapada Hospital Bandung
Appsync FMS GA adalah sistem manajemen fasilitas terintegrasi berbasis web yang dikembangkan khusus untuk Departemen FMS-GA & K3L Mayapada Hospital Bandung. Dibangun di atas platform Google Apps Script dengan Google Sheets sebagai backend database, aplikasi ini menggabungkan seluruh kegiatan operasional departemen dalam satu antarmuka yang dapat diakses dari perangkat desktop maupun mobile.

Modul Utama
FMS — Facility Management System
Mengelola seluruh siklus peralatan dan fasilitas medis, meliputi:

Asset Management — Pencatatan data aset lengkap beserta riwayat perawatan
Preventive Maintenance — Penjadwalan PM otomatis dengan kalkulasi periode (harian, mingguan, bulanan, tahunan), pembuatan jadwal berikutnya otomatis setelah PM selesai, dan pencatatan parameter teknis
Corrective Maintenance — Pelaporan kerusakan dan tindak perbaikan dengan tracking status
Daily Inspection — Pencatatan inspeksi harian per shift dengan parameter kondisi alat
Uji Fungsi System — Pengujian fungsi peralatan dengan parameter dan standar per kategori alat
Tools Kit Engineering — Pengelolaan inventaris peralatan teknisi beserta stok opname
Logistik Teknik — Manajemen barang masuk/keluar dengan perhitungan stok akhir otomatis
Facility Audit — Pencatatan temuan audit dan pemantauan status tindak lanjut

GA — General Affairs
Mendukung kegiatan operasional umum departemen termasuk pemantauan aktivitas harian, pengelolaan kendaraan dinas, dan kebutuhan administrasi fasilitas.
K3L — Kesehatan, Keselamatan Kerja & Lingkungan
Modul pengawasan dan pemantauan aspek K3L di lingkungan rumah sakit, mencakup supervisi keselamatan dan monitoring indikator lingkungan.

Fitur Sistem

Dashboard real-time — Ringkasan KPI meliputi total aset, capaian PM, inspection rate, dan critical alert
Role-based access control — Pembatasan akses menu per pengguna berdasarkan role (Super Admin, Admin, Operator)
Auto-login via Google Account — Kemudahan login bagi Admin menggunakan akun Google aktif
Pencatatan parameter terstruktur — Setiap PM, inspeksi, dan uji fungsi mencatat parameter teknis sesuai standar per kategori alat
Report & Export — Ekspor data ke Excel dan PDF langsung dari aplikasi
Barcode scanning — Identifikasi aset melalui kode barcode/QR
Grafik capaian — Visualisasi pencapaian PM dan inspeksi bulanan sepanjang tahun


Teknologi
KomponenTeknologiPlatformGoogle Apps Script (Web App)DatabaseGoogle SheetsFrontendHTML, CSS, JavaScript (SPA)AutentikasiSession-based via CacheService + Google SSOAksesWeb browser (desktop & mobile)
