# Notes for Claude

Static portfolio site for Bilal Tahir (materials engineer moving into ESG, carbon accounting and decarbonisation).

- One content page: `index.html` at the site root (moved from `sustainability/` at Bilal's request). The former materials home page was merged into its Overview tab (portrait, key figures, materials research cards, MSc lab gallery with lightbox, Cellulose Valley partners, expertise, experience, education, contact); photos are in `assets/`, referenced as `assets/`.
- `sustainability/index.html` is only a redirect to the root that keeps the hash, so old `/sustainability/#tab` links still work. Non-tab hashes on the sustainability page scroll to that element inside Overview.
- Plain HTML/CSS/JS, no build step. The site is one page, `index.html`, with tabs: a sticky `.topbar` with `.tab` links and one `<section class="tabpanel" id="tab-<name>">` per tab. The hash (`#overview`, `#regulation-reader`, `#materiality-case`, `#crosswalk`, `#case-studies`) selects the tab; the list of tab ids lives in the small script at the end.
- Shared look: the sustainability page uses the same theme as the home page — Instrument Serif headings (one weight only, so display text is set to 400), Inter Tight body, JetBrains Mono for labels, tabs and regulatory references; paper/forest/green in light, forest #0E1714 with chartreuse #CFE38A accent in dark. Sentence-case labels, no all-caps eyebrows, no arrow links. The Overview opens with the hero, the key figures, then the career map (a winding SVG road; stops are an HTML list, amber = education, green = work, ring = current). Colour tokens are defined once in the global :root, with light and dark themes. Each tab's CSS is scoped with its panel id (e.g. `#tab-crosswalk .row{...}`), and each tab's script is wrapped in its own function, so they don't clash.
- Adding a tab: add a `.tab` link, a scoped panel, its id in the tab script's list, and a project card in the Overview tab linking to `#<name>`.
- `projects/*.html` are redirect stubs (to `../index.html#<tab>`) for old links; don't put content there.
- Facts about Bilal: use only what he has confirmed. Never invent experience, numbers, employers or certifications.
- Regulatory facts (CSRD, ESRS, IFRS S2, CBAM, PPWR, SBTi, GHG Protocol) change often: check a current source before adding or changing a date, threshold or reference, and cite it in the page footer.
- Fictional case-study companies must stay clearly labelled as fictional.
- Commit only when Bilal asks; push to `main`. Use clear commit messages.
