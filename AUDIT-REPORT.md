# AUDIT REPORT — NIIS WEBSITE RELEASE CANDIDATE

Audit update: 23 November 2026  
Repository: `ni-school/nur-iman-islamic-school`  
Release branch: `niis-website-release`  
Production branch: `main` (unchanged; GitHub Pages production source has not been switched)

## Current decision

**NOT YET APPROVED FOR PRODUCTION RELEASE.** Repository and static source checks are in good condition, and the local logo/building assets are present. Browser-based visual and end-to-end QA remains unverified, and the school must confirm the displayed PPDB fee information before publication.

## Scope inspected

- Pages: `index.html`, `profil-sd.html`, `profil-smp.html`, `galeri.html`
- Shared stylesheet: `style.css`
- Root images: `logo-nur-iman.jpg`, `gedung-sekolah.jpg`
- Eight local documentation photographs in `assets/`
- Release documentation: README, deployment guide, QA results, and asset manifest

## Findings — PASS

- All four HTML pages reference the local logo `logo-nur-iman.jpg`; the former raw GitHub logo URL is absent from those pages.
- `style.css` uses the local hero image `gedung-sekolah.jpg`.
- Both root image files and all eight documentation photographs were found in the release branch.
- The five SD photographs are used on the home page / SD profile / general gallery as mapped in the source. The three SMP photographs are confined to the SMP profile page.
- Navigation links between the four pages are present.
- The home page includes a required-field PPDB form. Its submit handler validates the form and prepares a WhatsApp message to Admin; it does not send the message automatically.
- The gallery includes category filters and updates `aria-pressed` on filter buttons.
- The release branch is 10 commits ahead of `main` and 0 behind at the time of this audit. PR #1 remains open and unmerged.

## Findings — BLOCKED / NOT VERIFIED

- **Browser QA: NOT VERIFIED.** No successful browser-driven test evidence is available in this audit. Responsive rendering, horizontal overflow, real click behavior, browser console, network requests, and WhatsApp handoff must not be treated as passed.
- **School data confirmation: REQUIRED.** The page currently displays SD entry fee Rp7.000.000, SD SPP Rp500.000/month, SMP entry fee Rp6.000.000, SMP SPP Rp400.000/month, and registration form fee Rp300.000. The page itself says these figures follow the old website and require confirmation. Do not approve production publication until the school confirms or replaces them.
- Confirm that PPDB 2027/2028 is the correct active intake period and that the requirements / registration status remain current.
- Confirm the current WhatsApp admin number and school contact/address before production release.

## Asset dependencies

The logo and hero building photograph are now local files in the release branch. The eight documentation photos are also local. No raw GitHub URL is required for these images in the four pages or stylesheet.

## Release protection

No merge was performed. No GitHub Pages source change was performed. Keep `main` as the production baseline until the school confirms the outstanding data and browser QA passes. PR #1 must not be merged without explicit release approval.
