# Notes for Claude

Static portfolio site for Bilal Tahir (materials engineer moving into ESG, carbon accounting and decarbonisation).

- Plain HTML/CSS/JS, no build step. Each page is self-contained (inline CSS). Keep the shared look: Newsreader (display), IBM Plex Sans (body), IBM Plex Mono (references); colour tokens in each page's :root, with light and dark themes.
- Every page carries the same top nav (`.sitenav`). When adding a page, add it to the nav on all pages and as a card on `index.html`.
- Facts about Bilal: use only what he has confirmed. Never invent experience, numbers, employers or certifications.
- Regulatory facts (CSRD, ESRS, IFRS S2, CBAM, PPWR, SBTi, GHG Protocol) change often: check a current source before adding or changing a date, threshold or reference, and cite it in the page footer.
- Fictional case-study companies must stay clearly labelled as fictional.
- Commit only when Bilal asks; push to `main`. Use clear commit messages.
