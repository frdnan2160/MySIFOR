# MySIFOR - Panduan Pengguna
MySIFOR adalah aplikasi informasi Forum Kesiswaan TJKT berbasis Android.
Panduan ini mencakup peran:
- `Siswa`
- `Sekretaris` (special role)
- `Bendahara` (special role)
- `Koordinator/Petugas Kelas` (special role `petugas`)
- `Kebersihan Kelas` (special role `kebersihan`)
- `Peserta Ekstra TJKT`

Catatan penting:
- Akun, hak akses, dan konfigurasi sistem dikelola oleh Pengelola MySIFOR.
- `Sekretaris`, `Bendahara`, `Koordinator/Petugas`, dan `Kebersihan` adalah special role yang dapat ditempelkan ke akun.
- Jika data/akses tidak sesuai, laporkan ke Pengelola.
- Jika butuh bantuan, request fitur, atau koreksi data, hubungi WA Admin: `+62 851-9607-5120`.
- Pendaftaran ekstra TJKT akan dilakukan melalui platform pendaftaran yang disediakan.

## Status Rilis (2 Juli 2026)
- `Main`: `versionName 1.1.24` (`versionCode 33`)
- `Lite`: dihentikan per 4 April 2026. Gunakan `Main`.

## Highlight Update (2 Juli 2026)
- APK release-ready diperbaiki agar tidak force close akibat error permission Firestore async.
- Chat dan ringkasan siswa lebih stabil; warning sinkron chat permission noise tidak lagi mengganggu siswa.
- Naik Kelas sekarang memigrasikan data keuangan bendahara ke kelas tujuan dan membersihkan data kelas XII yang lulus.
- Jadwal pelajaran dan jadwal piket dihapus saat kelas naik agar bisa disusun ulang untuk tahun ajaran baru.
- Dashboard siswa dibuat lebih ringkas dengan teks pendek dan kartu kosong otomatis disembunyikan.

## Edisi Aplikasi
Saat ini hanya tersedia `Main`. Edisi `Lite` resmi dihentikan per 4 April 2026.

## Istilah Singkat
- `Piket`: jadwal tugas kebersihan kelas.
- `MBG`: jam pengambilan Makan Bergizi Gratis (berdasarkan jadwal pelajaran).
- `Event`: kegiatan kelas yang memiliki agenda dan kadang iuran.
- `Kas` dan `Infaq`: pembayaran rutin kelas.
- `Literasi`: laporan kegiatan membaca yang diinput siswa.
- `Pelanggaran`: catatan pelanggaran siswa yang dicatat oleh koordinator/petugas atau pengelola.
- `Denda Kebersihan`: denda dari kebersihan/piket yang dikonfirmasi bendahara.
- `Pendaftaran Ekstra TJKT`: pengajuan menjadi peserta ekstra TJKT melalui platform pendaftaran yang akan segera disediakan.

## Mulai Cepat
1. Install APK resmi.
2. Login dengan `username` dan `password`.
3. Aktifkan izin notifikasi.
4. Buka dashboard sesuai peran.

## Tutorial Download APK (Android)
1. Buka halaman rilis resmi MySIFOR (GitHub Releases) lewat browser HP.
2. Scroll ke bagian `Release`.
3. Pilih file `MySIFOR.apk` (Main).
4. Ketuk file untuk mulai download. Jika ada peringatan, pilih `Download anyway`.
5. Setelah selesai, buka file dari notifikasi atau folder `Download`.
6. Jika diminta, aktifkan izin `Install unknown apps` untuk browser yang dipakai.

Catatan:
Jangan pilih `Source code (zip)`. Yang dibutuhkan adalah file `.apk`.

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
- Jika pengelola menyalakan pengumuman, teks berjalan tampil di bagian atas aplikasi.
- Jika role atau data kelas berubah, menu akan menyesuaikan setelah login ulang.
- Label tab `Jadwal` bisa berubah sesuai peran akun.

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
- Riwayat pembayaran di profil menampilkan status lunas & belum dibayar.
- Ringkasan infaq di dashboard:
  - Jika ada infaq `sama rata` dan `custom` bersamaan, dashboard memisahkan keduanya.
  - Jika hanya `sama rata` (meski lebih dari satu), dashboard menjumlahkan jadi satu baris.
  - Infaq `custom` ditandai "nominal belum ditentukan" bila belum ada nominal.

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
- Kitab suci sesuai agama tersedia (Al-Qur'an atau Kitab).

J. Literasi
- Buat laporan literasi (judul/keterangan ringkas).
- Riwayat literasi tampil di profil.

K. Pelanggaran
- Terima catatan pelanggaran yang dibuat oleh pengelola.
- Riwayat pelanggaran tampil di profil siswa.

L. Kelompok Kelas
- Lihat daftar kelompok sesuai visibilitas yang ditentukan sekretaris.
- Buka detail untuk melihat anggota per kelompok.

### 2) Sekretaris (special role)
Tujuan sekretaris adalah administrasi dan monitoring aktivitas kelas.

A. Dashboard Sekretaris
- Ringkasan tugas, ujian, dan agenda kelas.
- Ringkasan pelanggaran/dresscode jika diaktifkan oleh Pengelola.

B. Jadwal Pelajaran
- Pantau jadwal pelajaran kelas.
- Pastikan jam pelajaran konsisten agar status pelajaran akurat.

C. Tugas dan Ujian
- Input tugas dan ujian kelas sesuai kebutuhan pengurus kelas.
- Pantau daftar tugas aktif dan jadwal ujian.

D. Agenda dan Kegiatan
- Catat agenda kelas dan kegiatan penting.
- Pastikan event yang sudah lewat tidak mengganggu ringkasan.

E. Chat
- Koordinasi dengan anggota kelas dan pengelola.
- Pengingat otomatis ke chat grup kelas saat masa penugasan (pengirim: Sekretaris {Kelas}).
- Riwayat pembayaran tersedia di profil (lunas/belum dibayar).

F. Kelompok Kelas
- Buat judul kelompok, tentukan mapel, jumlah kelompok/anggota, dan masa berlaku.
- Atur visibilitas (semua kelompok atau hanya kelompok masing-masing).
- Ubah nama kelompok dan hapus judul/kelompok bila diperlukan.
- Bagikan pembagian kelompok via WhatsApp.

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
- Kas dapat diliburkan per hari dan ditandai statusnya.

C. Infaq
- Buat infaq sekali per periode/tanggal.
- Checklist pembayaran per siswa di halaman detail.
- Pantau progres terkumpul dan sisa target.
- Mode infaq tersedia: sama rata atau custom (nama + nominal per entri).
- Ringkasan dashboard memisahkan `sama rata` dan `custom` bila keduanya ada.

D. Event
- Kelola pembayaran event kelas.
- Lihat daftar siswa yang sudah bayar dan belum bayar.
- Pantau target iuran dan realisasi.
- Progress event menampilkan persentase target terkumpul.

E. Denda Kebersihan
- Lihat daftar denda kebersihan dari role kebersihan kelas.
- Konfirmasi denda siswa agar statusnya berubah menjadi lunas/terbayar.
- Hapus denda jika ada kesalahan entry atau koreksi data.
- Setiap denda yang dikonfirmasi otomatis tercatat sebagai transaksi kas kategori `Denda Kebersihan`.
- Status denda yang sudah dikonfirmasi tersinkron ke dashboard/profil siswa dan riwayat pembayaran.

F. Laporan
- Rekap kas dan infaq (model event).
- Pantau ringkasan event untuk pelaporan ke kelas.

G. Chat
- Koordinasi terkait pembayaran dan laporan.
- Riwayat pembayaran tersedia di profil (lunas/belum dibayar).

### 4) Koordinator / Petugas Kelas (special role)
Tujuan koordinator adalah membantu pemantauan laporan kelas dan pencatatan pelanggaran sesuai kelasnya.

A. Dashboard Koordinator
- Akses cepat ke pencatatan pelanggaran.
- Lihat laporan pelanggaran kelas.
- Lihat laporan literasi kelas.

B. Pencatatan Pelanggaran
- Pilih siswa dari kelas yang sama.
- Pilih kategori dan detail pelanggaran.
- Data pelanggaran tersimpan untuk rekap pengelola.
- Poin pelanggaran tetap dipakai untuk rekap internal, tetapi tidak ditampilkan sebagai tulisan poin di dashboard/profil siswa.

C. Laporan
- Laporan pelanggaran dan literasi dapat dipantau per kelas.
- Data yang tampil mengikuti akses kelas koordinator.

### 5) Kebersihan Kelas (special role)
Tujuan kebersihan adalah mengelola checklist piket dan tindak lanjut kebersihan kelas.

A. Dashboard Kebersihan
- Checklist petugas piket kelas.
- Atur hari libur piket bila diperlukan.
- Kelola sanksi piket berulang atau denda kebersihan.

B. Checklist dan Libur Piket
- Tandai petugas piket yang sudah menjalankan tugas.
- Simpan catatan checklist bila ada keterangan tambahan.
- Liburkan piket untuk tanggal tertentu dengan alasan.

C. Sanksi dan Denda
- Buat sanksi piket berulang untuk siswa tertentu.
- Buat denda kebersihan dengan nominal dan jatuh tempo.
- Denda yang dibuat menunggu konfirmasi bendahara sebelum dianggap lunas.

### 6) Peserta Ekstra TJKT
Tujuan peserta ekstra TJKT adalah mengikuti aktivitas ekstra, membaca modul, mengerjakan tugas, dan absensi.

A. Dashboard Peserta Ekstra
- Scan QR absensi.
- Buka daftar modul TJKT.
- Buka daftar tugas TJKT.

B. Modul dan Tugas
- Baca modul dari link yang tersedia.
- Lihat deadline tugas.
- Tandai tugas sebagai selesai.

C. Absensi
- Scan QR saat sesi absensi dibuka.
- Satu sesi hanya dapat dicatat sekali untuk setiap peserta.

D. Pendaftaran Ekstra TJKT
- Siswa yang ingin bergabung ekstra TJKT akan mendaftar melalui platform pendaftaran yang akan segera disediakan.
- Data pendaftaran yang disiapkan: nama lengkap, kelas, NIS, email, dan nomor WA aktif.
- Tunggu konfirmasi setelah pendaftaran sebelum akses peserta ekstra TJKT aktif di aplikasi.
- Jika sudah dikonfirmasi tetapi menu belum muncul, login ulang atau hubungi WA Admin: `+62 851-9607-5120`.

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
3. Kirim laporan atau request ke WA Admin: `+62 851-9607-5120`.

Laporan yang detail mempercepat proses perbaikan.
