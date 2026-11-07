NATURA-SAFE v16 — PETA GUNUNG INTERAKTIF

Penambahan pada versi ini:
- Halaman Gunung dengan peta Leaflet terpisah dari peta hotspot karhutla.
- Marker gunung dan kartu yang bisa dipilih untuk membuka profil.
- Pencarian berdasarkan nama/wilayah dan filter pulau.
- Profil mencakup wilayah, perkiraan ketinggian, koordinat perkiraan, tipe, jalur populer, catatan rute, cuaca/musim, kesulitan, dan catatan status.
- Memisahkan status aktivitas gunung dari status buka/tutup jalur.
- Tautan ke MAGMA Indonesia dan ESDM.
- Memperbaiki navigasi yang sebelumnya memanggil halaman gunung yang belum ada.

BATASAN PENTING:
- Daftar gunung adalah katalog awal, bukan feed status langsung.
- Ketinggian, koordinat, dan jalur populer harus diverifikasi sebelum dipakai sebagai informasi operasional.
- Jarak rute, elevasi tiap pos, durasi, kontak basecamp, dan status jalur terkini belum tersedia secara lengkap; jangan menganggapnya sudah terverifikasi.
- Status aktivitas gunung harus diperiksa melalui PVMBG/MAGMA Indonesia dan status jalur melalui pengelola resmi/basecamp.
- Peta Leaflet membutuhkan koneksi internet.

CARA MENJALANKAN:
- Ekstrak ZIP.
- Buka folder proyek di VS Code.
- Jalankan dengan Live Server atau hosting statis. Menggunakan server lokal direkomendasikan agar fetch JSON berjalan.
- Buka menu Gunung dan klik marker atau kartu.

FITUR LAMA:
File dan alur hotspot SiPongi, data riwayat kebakaran, prakiraan BMKG, pembelajaran, simulasi, dan kuis dipertahankan; fitur-fitur itu tetap perlu dites di browser dan workflow GitHub Actions perlu dijalankan manual untuk memverifikasi updater.
