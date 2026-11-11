# AUDIT REPORT — NIIS WEBSITE FINAL RELEASE

Tanggal audit ulang: 11 November 2026

## Keputusan rilis
**READY FOR DEPLOYMENT REVIEW.** Struktur paket dan pemeriksaan statis lulus. Browser QA visual/interaktif belum dapat dibuktikan karena Chromium diblokir oleh lingkungan eksekusi. Konfirmasi informasi biaya/PPDB sekolah masih diperlukan.

## Cakupan
Empat halaman HTML (`index.html`, `profil-sd.html`, `profil-smp.html`, `galeri.html`), stylesheet bersama, delapan foto dokumentasi lokal, serta README, manifest, hasil QA, dan panduan deployment. ZIP sumber diuji dan tidak melaporkan kerusakan arsip.

## Pemisahan foto
- **SD:** `1000825926.jpg`, `1000821940.jpg`, `1000821942.jpg`, `1000853316.jpg` (kelulusan putra), `1000853344.jpg` (kelulusan putri). Dipakai pada Beranda, Profil SD, dan Galeri umum sesuai kebutuhan halaman.
- **SMP:** `1000853322.jpg` (kelulusan putra), `1000853324.jpg` (kelulusan putri), `1000800280.jpg` (pembelajaran Al-Qur’an berseragam kotak-kotak biru). Hanya pada Profil SMP.
- `lab-komputer.webp` tidak digunakan dalam paket ini; aturan aset tersebut tetap: hanya Profil SMP.
- `gandengan-01.webp` tidak digunakan sebagai dokumentasi galeri; aturan aset khusus hero/PPDB tetap dipertahankan pada sumber proyek bila dipakai.
- Tidak ada foto generatif sebagai pengganti dokumentasi. Tidak ada file foto yang diduplikasi di paket.

## Static QA
Lulus: parsing HTML pada empat halaman; pemeriksaan ID duplikat; referensi file lokal dan tautan internal; sintaks JavaScript inline melalui Node.js; decoding delapan foto; dan pemeriksaan segregasi SD/SMP terhadap dokumen handover. Form PPDB memiliki field wajib dan pola nomor telepon; handler menyusun pesan WhatsApp ke Admin tanpa mengirim otomatis. Filter kategori galeri dan navigasi lintas halaman ditemukan pada kode.

## Browser QA dan responsivitas
**NOT VERIFIED.** Playwright/Chromium berhasil diluncurkan, tetapi navigasi ke `file://` dan `http://127.0.0.1` diblokir oleh kebijakan lingkungan (`ERR_BLOCKED_BY_ADMINISTRATOR`). Karena itu, tampilan pada 390/768/1366 px, horizontal overflow, klik nyata, console runtime, dan network failure belum dapat disahkan. Uji browser setelah dibuka pada komputer lokal atau URL publik.

## Informasi sekolah
Nama, alamat, WhatsApp, dan tautan Maps mengikuti sumber proyek. Biaya SD masuk Rp7.000.000 dan SPP Rp500.000/bulan; SMP masuk Rp6.000.000 dan SPP Rp400.000/bulan; biaya formulir Rp300.000. Angka ini masih data lama dan berstatus **NEEDS SCHOOL CONFIRMATION** sebelum publikasi. PPDB Tahun Ajaran 2027/2028 dipertahankan tanpa menambahkan tanggal gelombang kedaluwarsa.

## Dependensi eksternal
Logo dan foto gedung hero masih menggunakan URL raw GitHub `main`, sehingga bergantung pada koneksi dan keberadaan file di repository. Delapan foto dokumentasi dipaketkan lokal.

## Perlindungan baseline dan deployment
Baseline `index.html` SHA `afdeda4bde6b2ddc6aa44789bf8c431adc75e187` dan `style.css` SHA `d984f885e3fb866c771b177c890cb0edf5554f8d` tetap menjadi acuan dan tidak ditimpa. Tidak ada push GitHub atau deployment. Lihat `DEPLOYMENT-GUIDE.md`.
