NATURA-SAFE V12 — AUTO-UPDATE SIPONGI

Yang ditambahkan:
- scripts/update_sipongi.py
- .github/workflows/update-sipongi.yml

Cara kerja:
SiPongi publik → GitHub Actions → ambil file XLSX resmi → normalisasi → hotspots.json → website NATURA-SAFE.

Jadwal:
Workflow berjalan otomatis setiap 6 jam dan juga bisa dijalankan manual dari tab Actions.

Catatan penting:
- V12 TIDAK mengubah peta, base map, jalan, label wilayah, atau tampilan hotspot.
- Workflow memakai halaman publik SiPongi dan kontrol unduhan XLSX yang terlihat di halaman, bukan API privat.
- Jika struktur halaman SiPongi berubah, workflow akan berhenti dengan pesan error agar tidak menimpa hotspots.json dengan data yang salah.
- Kolom yang diharapkan: Provinsi, Kab Kota, Kecamatan, Desa, Tanggal, Waktu, Satelit, Confidence, Latitude, Longitude.

Aktivasi:
1. Upload folder ini ke repository GitHub.
2. Pastikan GitHub Actions aktif.
3. Buka Actions → Update NATURA-SAFE hotspots from SiPongi → Run workflow untuk tes pertama.
4. Setelah berhasil, hotspots.json akan diperbarui otomatis sesuai jadwal.
5. Jika memakai GitHub Pages, perubahan hotspots.json akan ikut tersedia untuk website.

BMKG V11 tetap ada dan tidak diubah.
