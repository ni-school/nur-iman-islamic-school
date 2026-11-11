# DEPLOYMENT GUIDE — NIIS WEBSITE

## Sebelum unggah
1. Minta pihak sekolah mengonfirmasi nominal biaya SD/SMP, biaya formulir, dan seluruh ketentuan PPDB 2027/2028. Data biaya di paket masih mengikuti situs lama.
2. Pastikan akun/repository tujuan adalah `ni-school/nur-iman-islamic-school`. Baseline branch `main` tidak boleh ditimpa saat tahap review.
3. Gunakan branch khusus, misalnya `niis-website-release`, untuk pemeriksaan awal.

## Isi yang diunggah
Unggah **isi folder `NIIS_WEBSITE_FINAL_RELEASE/`** ke root folder publikasi, bukan folder ZIP pembungkusnya. Struktur root harus memuat `index.html`, `profil-sd.html`, `profil-smp.html`, `galeri.html`, `style.css`, `assets/`, serta dokumen Markdown/JSON. Jangan mengubah nama atau memindahkan file di dalam `assets/`.

## GitHub Pages
1. Buka repository → Settings → Pages.
2. Pilih Deploy from a branch.
3. Pilih branch release dan folder `/ (root)` (atau folder yang memang dipilih sebagai document root).
4. Simpan, tunggu proses publikasi, lalu buka URL yang diberikan GitHub Pages.
5. Uji keempat halaman, menu mobile, filter galeri, validasi PPDB, pembentukan tautan WhatsApp (tanpa mengirim pesan), Maps, dan seluruh foto.

## Catatan aset
Logo dan foto gedung hero memakai URL raw GitHub pada branch `main`, bukan file lokal dalam paket. Pastikan `logo-nur-iman.jpg` dan `gedung-sekolah.jpg` tetap tersedia publik pada branch tersebut. Delapan foto dokumentasi SD/SMP disertakan di `assets/`.

## Rollback
Jika rilis bermasalah, ubah sumber GitHub Pages kembali ke branch/folder sebelumnya. Jangan menghapus baseline `main`.

## Batas verifikasi
Paket ini telah diperiksa secara statis. Browser QA visual/interaktif belum dapat diselesaikan pada lingkungan audit ini karena navigasi Chromium ke `localhost` dan `file://` diblokir oleh kebijakan lingkungan. Lakukan QA browser setelah paket dibuka secara lokal atau setelah deployment ke URL publik.
