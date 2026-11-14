# NUR IMAN ISLAMIC SCHOOL — FINAL RELEASE PACKAGE

## Status
**READY FOR DEPLOYMENT REVIEW**. Paket telah dirapikan dan lolos pemeriksaan statis. Browser QA visual/interaktif diblokir oleh lingkungan audit; konfirmasi biaya dan ketentuan PPDB sekolah masih diperlukan.

## Isi paket
- `index.html` — Beranda, program, fasilitas, biaya, PPDB, PORTER, kontak dan peta.
- `profil-sd.html` — Profil serta dokumentasi SD.
- `profil-smp.html` — Profil serta dokumentasi SMP.
- `galeri.html` — Galeri umum dokumentasi SD dengan filter kategori.
- `style.css` — Stylesheet bersama responsif.
- `assets/` — Delapan foto dokumentasi asli yang dipulihkan dari dokumen handover.
- `ASSET-MANIFEST.md` — Ukuran, dimensi, dan checksum aset.
- `AUDIT-REPORT.md` — Ringkasan audit dan batasan rilis.
- `QA-RESULTS.json` — Hasil pemeriksaan teknis terstruktur.
- `DEPLOYMENT-GUIDE.md` — Langkah unggah dan rollback GitHub Pages.

## Menjalankan lokal
Ekstrak ZIP, buka terminal di folder hasil ekstraksi, lalu jalankan `python -m http.server 8000`. Buka `http://localhost:8000`.

## Pemasangan GitHub Pages
1. Buat branch khusus renovasi agar baseline tetap aman.
2. Unggah **isi folder ZIP** ke root branch publikasi (bukan folder pembungkus ZIP).
3. Pastikan `index.html` berada di root dan folder `assets/` ikut diunggah.
4. Aktifkan GitHub Pages dari branch/folder tersebut.
5. Uji keempat halaman pada URL publik, termasuk menu mobile, filter galeri, formulir WhatsApp, logo, foto hero, dan tautan Maps.

## Ketergantungan aset eksternal
Logo dan foto gedung hero masih menggunakan URL raw GitHub dari repository `ni-school/nur-iman-islamic-school` branch `main`. Kedua file tersebut harus tetap tersedia dan dapat diakses publik. Delapan foto dokumentasi SD/SMP sudah disertakan lokal di dalam ZIP.

## Data yang dipertahankan dari situs lama
- PPDB Tahun Ajaran 2027/2028.
- WhatsApp Admin: `+62 852-1888-9192`.
- Biaya lama: SD masuk Rp7.000.000 dan SPP Rp500.000/bulan; SMP masuk Rp6.000.000 dan SPP Rp400.000/bulan; formulir Rp300.000.
- Alamat: Jl. Tumaritis 1 No. 8, Harjamukti, Cimanggis, Depok.
- Google Maps: https://maps.app.goo.gl/Vww3KEgYdHxDn97V7

**Penting:** nominal biaya dan ketentuan pendaftaran perlu konfirmasi sekolah sebelum publikasi. Tidak ada tanggal gelombang atau tanggal kegiatan yang ditambahkan.

Baseline lama `index.html` dan `style.css` tidak diubah. Tidak ada push atau deployment yang dilakukan.
