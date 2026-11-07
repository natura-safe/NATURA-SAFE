NATURA-SAFE v31 — Perapian otomatisasi dan status data

Dasar: NATURA-SAFE v30. Seluruh fitur dan aset v30 dipertahankan.

Perubahan v31:
1. Menggabungkan dua workflow pembaruan hotspot menjadi satu workflow resmi agar tidak berjalan bersamaan.
2. Workflow memeriksa ekspor publik SiPongi setiap 6 jam dan dapat dijalankan manual melalui GitHub Actions.
3. Menambahkan concurrency lock dan batas waktu job untuk mengurangi risiko proses ganda/tergantung.
4. Memperbarui keterangan pada halaman data agar tidak menjanjikan pembaruan real-time.
5. Mempertahankan integrasi prakiraan BMKG yang sudah ada di script.js. Pengguna memasukkan kode wilayah ADM4 lalu menekan Ambil Data BMKG.

Batasan yang harus diketahui:
- Workflow belum aktif di komputer lokal hanya karena ZIP dibuka. Upload repository ke GitHub dan aktifkan GitHub Actions.
- Keberhasilan pengambilan SiPongi bergantung pada ketersediaan ekspor publik dan perubahan tampilan situs. Jika gagal, workflow akan gagal dan snapshot sebelumnya tetap ada.
- Data hotspot adalah indikasi satelit, bukan konfirmasi kejadian kebakaran.
- BMKG yang saat ini terintegrasi adalah prakiraan cuaca, bukan pengamatan aktual. Pembaruan mengikuti jadwal BMKG.
- Belum ada server backend terpisah. Snapshot hotspot diperbarui di repository oleh GitHub Actions.

Aktivasi:
1. Buat/pilih repository GitHub dan unggah isi folder ini.
2. Pastikan Actions diizinkan pada Settings > Actions.
3. Buka Actions > Update NATURA-SAFE data > Run workflow.
4. Periksa job. Pastikan langkah Download and validate official SiPongi export berhasil.
5. Setelah workflow berhasil, periksa commit baru dan nilai updated_at_utc pada hotspots-meta.json.
6. Jika menggunakan GitHub Pages, pastikan Pages menerbitkan branch/folder repository yang berisi file website.

Uji lokal yang dilakukan pada paket:
- JSON hotspots, metadata, riwayat kebakaran, dan satwa dapat diparse.
- Script Python updater lolos pemeriksaan sintaks.
- JavaScript lolos pemeriksaan sintaks jika Node.js tersedia.
