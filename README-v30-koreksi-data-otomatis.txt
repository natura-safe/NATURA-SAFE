NATURA-SAFE v30 — Koreksi integritas data dan media

Perubahan:
- Menghapus pin riwayat karhutla yang sebelumnya ditempatkan pada koordinat hotspot terdekat. Rekap luas karhutla provinsi kini tampil sebagai tabel, bukan lokasi kejadian.
- Mengosongkan katalog satwa terdampak karena data sebelumnya memuat klaim yang sebagian tidak didukung tautan laporan spesifik. Satwa ditampilkan setelah dikaitkan dengan kejadian dan sumber yang dapat diverifikasi.
- Menambahkan video MP4 pengantar dan video edukasi simulasi singkat (tanpa narasi suara; visual + teks).
- Menambahkan GitHub Actions workflow terjadwal untuk mencoba memperbarui hotspots.json melalui updater SiPongi. Otomatisasi baru berjalan setelah proyek di-push ke GitHub, Actions diaktifkan, dan workflow berhasil berjalan. Sumber SiPongi dapat mengubah format/unduhan sehingga perlu pemantauan.
- Menambahkan hotspots-meta.json sebagai metadata snapshot dan updater.

Batasan penting:
- File ZIP saja tidak dapat memperbarui dirinya di komputer. Otomatisasi memerlukan hosting/repository dan workflow aktif.
- Hotspot satelit bukan bukti pasti kebakaran di lokasi tersebut.
- Rekap provinsi bukan titik kejadian. Untuk pin riwayat kejadian, tambahkan catatan kejadian dengan koordinat spesifik dan sumber laporan.
- Satwa belum ditampilkan karena klaim lama belum memenuhi syarat sumber per kejadian. Ini disengaja agar website tidak menyajikan data yang menyesatkan.
- Gunung dan jalur pendakian belum seluruhnya diverifikasi secara faktual.
- Video merupakan prototipe edukasi tanpa voice-over; dapat diganti dengan video Canva dan narasi pengguna nanti.

Cara mengaktifkan pembaruan otomatis:
1. Upload seluruh folder ke repository GitHub.
2. Buka tab Actions dan aktifkan workflow bila diminta.
3. Jalankan workflow "Update NATURA-SAFE hotspots" secara manual sekali untuk menguji.
4. Periksa log job. Jadwal berjalan harian hanya jika workflow berhasil dan repository mengizinkan Actions.
