# MySIFOR - Panduan Pengguna

MySIFOR adalah aplikasi informasi Forum Kesiswaan TJKT berbasis Android.
Panduan ini ditujukan untuk pengguna:
- `Siswa`
- `Sekretaris` (special role)
- `Bendahara` (special role)

Catatan:
- Pengelolaan akun, role, dan konfigurasi sistem dilakukan oleh `Administrator`.
- Jika ada data/akses yang tidak sesuai, laporkan ke `Administrator`.

## Status Rilis (7 Maret 2026)

- `Main`: `versionName 1.1.1` (`versionCode 10`)
- `Lite`: `versionName 1.1.6-lite` (`versionCode 15`)

## Edisi Aplikasi (Main vs Lite)

### Ringkas Perbedaan
| Aspek | Main | Lite |
|---|---|---|
| Fokus | UI lebih kaya, komponen lebih lengkap | UI ringan, render cepat, hemat resource |
| Target perangkat | Spek menengah ke atas | Spek rendah sampai menengah |
| Komponen visual | Material card/statistik lengkap | Panel flat ringan dengan komponen AppCompat |
| Al-Qur'an | Detail surah bisa minimize + tafsir ayat bisa toggle | Mode v1 fokus ayat + arti, tampilan lebih sederhana |
| Channel update | `main` | `lite` |

### Fitur Utama Main
- Dashboard per role dengan komponen statistik lengkap dan visual lebih detail.
- Aksi Cepat Al-Qur'an di bagian paling atas area aksi cepat.
- Detail surah bisa di-minimize/tampilkan ulang sesuai kebutuhan baca.
- Tafsir per ayat tersedia dengan toggle, default tersembunyi untuk jaga performa.
- Cocok untuk pengguna yang ingin tampilan penuh dan informasi lebih kaya per layar.

### Fitur Utama Lite
- Dashboard tetap lengkap secara fungsi, tapi UI disederhanakan agar scrolling lebih ringan.
- Aksi Cepat Al-Qur'an tetap di posisi paling atas.
- Mode Al-Qur'an v1 berfokus pada ayat + arti agar akses cepat.
- Komponen tombol/panel dioptimalkan untuk perangkat RAM lebih kecil.
- Cocok untuk penggunaan harian yang mengutamakan respons cepat.

### Fitur yang Sama di Main dan Lite
- Login dan akses berbasis role (`Siswa`, `Sekretaris`, `Bendahara`, role lain sesuai akun).
- Chat (inbox, direct message, grup kelas, chat baru).
- Dashboard akademik: pelajaran, tugas, ujian, event, jadwal shalat, dan ringkasan pembayaran.
- Notifikasi penting dan reminder adzan.
- Mekanisme update APK dari channel masing-masing.


## 1. Tujuan Aplikasi

MySIFOR membantu pengguna untuk:
- Melihat ringkasan kegiatan harian.
- Memantau jadwal, tugas, ujian, dan agenda.
- Berkomunikasi melalui chat.
- Menerima notifikasi penting dan pengingat shalat.

## 2. Ringkasan Hak Akses

### 2.1 Siswa
- Akses dashboard siswa.
- Lihat jadwal, tugas, ujian, profil, dan ringkasan aktivitas.
- Gunakan fitur chat.

### 2.2 Sekretaris
- Akses menu sekretariat sesuai kewenangan.
- Pantau data administrasi dan agenda.
- Gunakan fitur chat untuk koordinasi.

### 2.3 Bendahara
- Akses menu keuangan sesuai kewenangan.
- Pantau infaq, kas, event, tunggakan, dan laporan.
- Gunakan fitur chat untuk koordinasi.

## 3. Persiapan Sebelum Pakai

Sebelum install/login, pastikan:
1. Kamu sudah menerima `username` dan `password` dari Administrator.
2. Internet stabil.
3. Memori penyimpanan cukup.
4. Izin notifikasi MySIFOR diaktifkan.

## 4. Instalasi APK (Android)

1. Download APK terbaru dari sumber resmi.
2. Buka file APK.
3. Jika diminta, aktifkan `Install unknown apps` untuk sumber tersebut.
4. Selesaikan instalasi.
5. Buka aplikasi dan login.

## 5. Login

1. Buka aplikasi MySIFOR.
2. Isi `Username`.
3. Isi `Password`.
4. Tekan `Masuk`.

Jika login gagal:
1. Cek kembali username/password (case-sensitive).
2. Pastikan internet aktif.
3. Tutup-buka aplikasi.
4. Jika tetap gagal, hubungi Administrator.

## 6. Dashboard

### 6.1 Dashboard Siswa
Menampilkan:
- Pelajaran saat ini.
- Status tugas aktif.
- Ujian terdekat.
- Jadwal shalat hari ini.
- Ringkasan event dan pembayaran.

### 6.2 Dashboard Sekretaris
Menampilkan ringkasan administrasi, statistik tugas/event/ujian, dan akses cepat sekretariat.

### 6.3 Dashboard Bendahara
Menampilkan ringkasan infaq/kas/event, data tunggakan, dan akses cepat transaksi/laporan.

### 6.4 Aksi Cepat Al-Qur'an
- Tombol Al-Qur'an ada di bagian atas area aksi cepat dashboard.
- Halaman detail surah mendukung tombol minimize/tampilkan detail surat.
- Tafsir singkat per ayat bisa di-toggle dan default-nya tersembunyi (tap `Lihat tafsir` saat diperlukan).
- Pada channel `Lite` (v1), fokus utama tampilan adalah ayat + arti dengan mode lebih ringan.

## 7. Fitur Chat

### 7.1 Daftar Chat
- Lihat inbox dan arsip chat.
- Cari chat.
- Buka chat admin atau chat direct.

### 7.2 Ruang Chat
- Kirim dan baca pesan.
- Long press pesan untuk salin/hapus.
- Aksi room: arsipkan atau sembunyikan chat.

### 7.3 Chat Baru
- Tambah kontak lewat NIS/Email.
- Pilih kontak untuk membuka direct message.

## 8. Notifikasi Adzan

Perilaku audio:
- `Shubuh` memakai channel/audio khusus shubuh.
- `Dzuhur`, `Ashar`, `Maghrib`, `Isya` memakai adzan reguler.

Agar adzan berbunyi:
1. Aktifkan izin notifikasi aplikasi.
2. Pastikan volume media/alarm tidak nol.
3. Pastikan tidak mode senyap / DND.
4. Nonaktifkan pembatasan baterai ekstrem untuk MySIFOR.

Kompatibilitas:
- Minimal Android `6.0 (API 23)`.
- Android 13+ wajib izin notifikasi.

## 9. Notifikasi Saat Aplikasi Lama Tidak Dibuka

- Aplikasi memakai sinkronisasi background periodik.
- Notifikasi chat/reminder tetap dicek walau aplikasi lama tidak dibuka.
- Tetap disarankan membuka aplikasi sesekali agar sinkronisasi akun dan data lebih cepat.

## 10. Update Aplikasi

Saat ada versi baru, aplikasi dapat menampilkan prompt update.

Mekanisme yang didukung:
- Download APK di background.
- Instalasi tetap perlu konfirmasi pengguna.

Channel update:
- `Main` mengambil update dari jalur rilis Main.
- `Lite` mengambil update dari jalur rilis Lite.
- Versi aktif per 7 Maret 2026: Main `1.1.1 (10)` dan Lite `1.1.6-lite (15)`.


## 11. Troubleshooting

### 11.1 Notifikasi tidak masuk
1. Cek izin notifikasi MySIFOR.
2. Cek pengaturan baterai (jangan dibatasi ketat).
3. Cek internet.
4. Restart HP.

### 11.2 Notifikasi masuk tapi tanpa suara
1. Naikkan volume media/alarm.
2. Matikan mode senyap / DND.
3. Cek channel notifikasi MySIFOR (suara harus aktif).

### 11.3 Aplikasi terasa lambat
1. Pastikan sudah di versi terbaru.
2. Gunakan koneksi stabil.
3. Tutup aplikasi berat lain.
4. Sisakan storage internal yang cukup.

### 11.4 Gagal update APK
1. Cek storage.
2. Cek izin install unknown apps.
3. Hapus file APK lama yang rusak.
4. Download ulang APK terbaru.

## 12. FAQ

### Apakah semua role punya menu yang sama?
Tidak. Menu mengikuti role akun dan hak akses Administrator.

### Siapa yang bisa ubah role akun?
Hanya `Administrator`.

### Apakah update selalu wajib?
Tergantung kebijakan rilis. Jika ditandai wajib, user harus update untuk lanjut.

## 13. Bantuan

Jika ada masalah:
1. Catat waktu kejadian dan fitur yang bermasalah.
2. Sertakan screenshot.
3. Kirim laporan ke Administrator.

Laporan yang detail mempercepat proses perbaikan.
