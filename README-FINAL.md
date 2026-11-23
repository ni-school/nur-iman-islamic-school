# NUR IMAN ISLAMIC SCHOOL — RELEASE CANDIDATE

## Status

**Release candidate — pending final acceptance.** Static source inspection has passed for the key page and asset references. Browser QA and confirmation of school PPDB data remain outstanding. Production branch `main` has not been changed.

## Package contents

- `index.html` — Beranda, program, fasilitas, biaya, PPDB, kontak, dan peta.
- `profil-sd.html` — Profil serta dokumentasi SD.
- `profil-smp.html` — Profil serta dokumentasi SMP.
- `galeri.html` — Galeri umum dokumentasi SD dengan filter kategori.
- `style.css` — Stylesheet bersama.
- `logo-nur-iman.jpg` — Logo lokal.
- `gedung-sekolah.jpg` — Foto gedung untuk hero lokal.
- `assets/` — Delapan foto dokumentasi SD/SMP.
- `ASSET-MANIFEST.md`, `AUDIT-REPORT.md`, `QA-RESULTS.json`, `DEPLOYMENT-GUIDE.md` — Dokumen pendukung rilis.

## Run locally

From the repository root, run:

```bash
python -m http.server 8000
```

Then open `http://localhost:8000`.

## Assets

Logo, hero building image, and all eight documentation photographs are stored locally in this release branch. The four HTML pages use `logo-nur-iman.jpg`; `style.css` uses `gedung-sekolah.jpg`.

## School information requiring confirmation

The current page retains legacy figures: SD entry fee Rp7.000.000 and SPP Rp500.000/month; SMP entry fee Rp6.000.000 and SPP Rp400.000/month; registration form Rp300.000. These amounts must be confirmed by the school before publication. Confirm the PPDB 2027/2028 status, requirements, WhatsApp Admin number, address, and Maps destination as well.

## Release protection

The candidate is on `niis-website-release`. PR #1 targets `main` and remains unmerged. Do not change GitHub Pages source or merge until browser QA and school confirmation are complete and release approval is explicit.
