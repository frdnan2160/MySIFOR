# MySIFOR - Panduan Pengguna (Siswa, Sekretaris, Bendahara)

MySIFOR adalah aplikasi informasi Forum Kesiswaan TJKT berbasis Android.
Panduan ini hanya untuk peran:
- `Siswa`
- `Sekretaris` (special role)
- `Bendahara` (special role)

Catatan penting:
- Akun, hak akses, dan konfigurasi sistem dikelola oleh Pengelola MySIFOR.
- `Sekretaris` dan `Bendahara` adalah special role yang dapat ditempelkan ke akun (contoh: akun siswa merangkap sekretaris/bendahara).
- Jika data/akses tidak sesuai, laporkan ke Pengelola.

## Status Rilis (27 Maret 2026)
- `Main`: `versionName 1.1.14` (`versionCode 23`)
- `Lite`: `versionName 1.1.17-lite` (`versionCode 26`)

## Edisi Aplikasi (Main vs Lite)

| Aspek | Main | Lite |
|---|---|---|
| Fokus | UI lebih kaya dan detail | UI ringan, hemat resource |
| Target perangkat | Spek menengah ke atas | Spek rendah sampai menengah |
| Komponen visual | Material card/statistik lengkap | Panel flat ringan |
| Al-Qur'an | Detail surah bisa minimize + tafsir ayat bisa toggle | Mode v1 fokus ayat + arti |
| Channel update | `main` | `lite` |

Rekomendasi:
- Pilih `Main` untuk tampilan lengkap.
- Pilih `Lite` jika HP terbatas atau ingin lebih ringan.

## Istilah Singkat
- `Piket`: jadwal tugas kebersihan kelas.
- `MBG`: jam pengambilan Makan Bergizi Gratis (berdasarkan jadwal pelajaran).
- `Event`: kegiatan kelas yang memiliki agenda dan kadang iuran.
- `Kas` dan `Infaq`: pembayaran rutin kelas.
- `Literasi`: laporan kegiatan membaca yang diinput siswa.
- `Pelanggaran`: catatan pelanggaran siswa yang dicatat petugas/guru/admin.

## Mulai Cepat
1. Install APK resmi.
2. Login dengan `username` dan `password`.
3. Aktifkan izin notifikasi.
4. Buka dashboard sesuai peran.

## Instalasi APK (Android)
1. Download APK terbaru dari sumber resmi.
2. Buka file APK.
3. Jika diminta, aktifkan `Install unknown apps`.
4. Selesaikan instalasi.
5. Buka aplikasi dan login.

## Login
1. Buka aplikasi MySIFOR.
2. Isi `Username`.
3. Isi `Password`.
4. Tekan `Masuk`.

Jika login gagal:
1. Cek kembali username dan password (case-sensitive).
2. Pastikan internet aktif.
3. Tutup-buka aplikasi.
4. Jika tetap gagal, hubungi Pengelola.

Catatan password default:
- Jika muncul notifikasi akun masih memakai password default, segera ganti password lewat web MySIFOR (menu `Ganti Password`).

## Navigasi Umum
- Menu yang tampil mengikuti peran akun.
- Tombol `Refresh` memuat data terbaru dari server.
- Badge pada ikon chat menandakan pesan baru.
- Jika admin menyalakan pengumuman, teks berjalan tampil di bagian atas aplikasi.
- Jika role atau data kelas berubah, menu akan menyesuaikan setelah login ulang.

## Keamanan & Privasi
- Pesan chat terenkripsi.

## Peran dan Fitur

### 1) Siswa
Tujuan siswa adalah memantau aktivitas belajar harian, menerima pengingat, dan berkomunikasi.

A. Dashboard Siswa
- Pelajaran hari ini dengan status `belum mulai`, `sedang berlangsung`, `jeda`, atau `selesai`.
- Ringkasan tugas aktif beserta jumlah tugas dan deadline terdekat.
- Ringkasan ujian terdekat.
- Ringkasan event/agenda kelas.
- Ringkasan pembayaran (kas/infaq/event) jika data tersedia.
- Informasi jadwal ibadah (menyesuaikan agama akun).

B. Cara Membaca Status Pelajaran
- `Belum mulai`: belum masuk jam pertama.
- `Sedang berlangsung`: jam pelajaran aktif.
- `Jeda`: jeda antar jam pelajaran.
- `Selesai`: semua jam pelajaran hari itu selesai.

C. Jadwal Pelajaran
- Lihat jadwal harian dan jadwal per minggu.
- Detail mapel per jam (format jam `07:00` dan `07.00` sama-sama valid).
- Jadwal otomatis menentukan status pelajaran real-time.

D. Tugas dan Ujian
- Tugas aktif menampilkan judul, mapel, dan deadline.
- Ujian terdekat tampil pada ringkasan dashboard.
- Tugas/ujian lama otomatis disembunyikan jika sudah lewat.

E. Event dan Agenda
- Event aktif tampil di ringkasan event.
- Detail event memuat judul, tanggal, dan keterangan.

F. Pembayaran
- Ringkasan kas/infaq/event tampil jika kelas memakai modul pembayaran.
- Peringatan tunggakan muncul bila ada pembayaran belum lunas.

G. Piket dan MBG
- Peringatan piket muncul saat jam pelajaran berlangsung hingga +15 menit setelah pelajaran selesai.
- Reminder MBG muncul 15 menit sebelum jadwal MBG dan saat MBG berlangsung.
- Peringatan tampil sebagai notifikasi dan dialog yang menutupi layar.

H. Chat
- Inbox chat untuk melihat pesan masuk.
- Direct message untuk chat pribadi.
- Grup kelas untuk komunikasi kelas.
- Arsip chat, pencarian chat, serta salin/hapus pesan.
- Semua pesan chat terenkripsi.

I. Profil
- Lihat identitas akun dan info kelas.

J. Literasi
- Buat laporan literasi (judul/keterangan ringkas).
- Riwayat literasi tampil di profil.

K. Pelanggaran
- Terima catatan pelanggaran yang dibuat petugas/guru/admin.
- Riwayat pelanggaran tampil di profil siswa.

### 2) Sekretaris (special role)
Tujuan sekretaris adalah administrasi dan monitoring aktivitas kelas.

A. Dashboard Sekretaris
- Ringkasan tugas, ujian, dan agenda kelas.
- Ringkasan pelanggaran/dresscode jika diaktifkan oleh Pengelola.

B. Jadwal Pelajaran
- Pantau jadwal pelajaran kelas.
- Pastikan jam pelajaran konsisten agar status pelajaran akurat.

C. Tugas dan Ujian
- Input tugas dan ujian kelas sesuai kebutuhan guru/pengurus.
- Pantau daftar tugas aktif dan jadwal ujian.

D. Agenda dan Kegiatan
- Catat agenda kelas dan kegiatan penting.
- Pastikan event yang sudah lewat tidak mengganggu ringkasan.

E. Chat
- Koordinasi dengan anggota kelas dan pengelola.

### 3) Bendahara (special role)
Tujuan bendahara adalah mengelola keuangan kelas.

A. Dashboard Bendahara
- Ringkasan kas/infaq/event.
- Ringkasan tunggakan dan status pembayaran.

B. Kas
- Catat transaksi kas harian.
- Pantau pembayaran siswa (lunas atau belum).
- Cek ringkasan tunggakan untuk minggu berjalan.
- Tracking kas bisa difilter per hari dengan dropdown hari dan nominal sesuai setup.

C. Infaq
- Buat infaq sekali per periode/tanggal.
- Checklist pembayaran per siswa di halaman detail.
- Pantau progres terkumpul dan sisa target.
- Mode infaq tersedia: sama rata atau custom (nama + nominal per entri).

D. Event
- Kelola pembayaran event kelas.
- Lihat daftar siswa yang sudah bayar dan belum bayar.
- Pantau target iuran dan realisasi.

E. Laporan
- Rekap kas dan infaq (model event).
- Pantau ringkasan event untuk pelaporan ke kelas.

F. Chat
- Koordinasi terkait pembayaran dan laporan.

## Notifikasi dan Pengingat
- Notifikasi dan suara adzan hanya dijadwalkan untuk akun `Islam`.
- `Shubuh` memakai channel/audio khusus Shubuh, waktu lain memakai adzan reguler.
- Reminder penting meliputi chat unread, tugas, ujian, event, serta piket/MBG.

Agar adzan berbunyi:
1. Aktifkan izin notifikasi aplikasi.
2. Pastikan volume media/alarm tidak nol.
3. Pastikan tidak mode senyap/DND.
4. Nonaktifkan pembatasan baterai ekstrem untuk MySIFOR.

Kompatibilitas:
- Minimal Android `6.0 (API 23)`.
- Android 13+ wajib izin notifikasi.

## Sinkronisasi Latar Belakang
- Aplikasi menyinkronkan data secara berkala agar reminder tetap berjalan meski aplikasi jarang dibuka.
- Disarankan membuka aplikasi sesekali agar data dan sesi tetap segar.

## Update Aplikasi
Saat ada versi baru, aplikasi dapat menampilkan prompt update.
Mekanisme update:
- APK diunduh di background.
- Instalasi tetap perlu konfirmasi pengguna.
- Jika update ditandai wajib, pengguna harus update sebelum melanjutkan.

Channel update:
- `Main` mengambil update dari jalur rilis Main.
- `Lite` mengambil update dari jalur rilis Lite.

## Troubleshooting

### Notifikasi tidak masuk
1. Cek izin notifikasi MySIFOR.
2. Cek pengaturan baterai (jangan dibatasi ketat).
3. Cek internet.
4. Restart HP.

### Notifikasi masuk tapi tanpa suara
1. Naikkan volume media/alarm.
2. Matikan mode senyap/DND.
3. Cek channel notifikasi MySIFOR (suara harus aktif).

### Aplikasi terasa lambat
1. Pastikan sudah di versi terbaru.
2. Gunakan koneksi stabil.
3. Tutup aplikasi berat lain.
4. Sisakan storage internal yang cukup.

### Gagal update APK
1. Cek storage.
2. Cek izin install unknown apps.
3. Hapus file APK lama yang rusak.
4. Download ulang APK terbaru.

## Bantuan
Jika ada masalah:
1. Catat waktu kejadian dan fitur yang bermasalah.
2. Sertakan screenshot.
3. Kirim laporan ke Pengelola.

Laporan yang detail mempercepat proses perbaikan.
