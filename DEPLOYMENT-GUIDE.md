# DEPLOYMENT GUIDE — NIIS WEBSITE RELEASE

## Release state

Candidate branch: `niis-website-release`  
Production branch: `main`  
PR: #1 — open, not merged (as last checked 23 November 2026)

**Do not switch GitHub Pages to the release branch or merge PR #1 yet.** The production website remains on its existing source.

## Pre-deployment gates

1. Obtain written confirmation from the school for SD/SMP entry fees, monthly SPP, registration form fee, PPDB 2027/2028 requirements and current registration status.
2. Confirm the WhatsApp Admin number, school address, and Google Maps destination.
3. Complete browser QA on the candidate URL or local web server:
   - 390 px, 768 px, and 1366 px viewport widths
   - all four pages load without missing assets
   - mobile navigation opens, closes, and updates `aria-expanded`
   - gallery category filters show the correct cards
   - required PPDB fields block invalid submission
   - valid PPDB submission prepares the WhatsApp message; do not send a test message
   - Maps and WhatsApp links point to the intended destinations
   - no horizontal overflow, broken images, console errors, or failed network requests
4. Record the QA outcome and school confirmation before release approval.

## Candidate structure

The publication root must contain `index.html`, `profil-sd.html`, `profil-smp.html`, `galeri.html`, `style.css`, `logo-nur-iman.jpg`, `gedung-sekolah.jpg`, and `assets/`. The documentation files may remain in the repository root.

## GitHub Pages release procedure — only after approval

1. Open repository Settings → Pages.
2. Confirm the existing production source before changing anything.
3. Only after explicit approval, select `niis-website-release` and `/(root)` as the Pages source.
4. Wait for GitHub Pages deployment to complete.
5. Run the browser QA checklist again against the published URL.
6. Keep the previous production source available for rollback.

## Rollback

If the candidate deployment fails, restore the previous GitHub Pages source (the existing production branch/folder). Do not delete `main`, the release branch, or repository data.

## Known limitations

Browser QA has not yet been certified. Static source inspection is not a substitute for real browser testing. The PPDB fee values are legacy figures pending school confirmation.
