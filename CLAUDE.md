# Notes for Claude

Static portfolio site for Bilal Tahir (materials engineer moving into ESG, carbon accounting and decarbonisation).

- Plain HTML/CSS/JS, no build step. The whole site is one page, `index.html`, with tabs: a sticky `.topbar` with `.tab` links and one `<section class="tabpanel" id="tab-<name>">` per tab. The hash (`#overview`, `#regulation-reader`, `#materiality-case`, `#crosswalk`) selects the tab; the list of tab ids lives in the small script at the end.
- Shared look: Newsreader (display), IBM Plex Sans (body), IBM Plex Mono (references). Colour tokens are defined once in the global :root, with light and dark themes. Each tab's CSS is scoped with its panel id (e.g. `#tab-crosswalk .row{...}`), and each tab's script is wrapped in its own function, so they don't clash.
- Adding a tab: add a `.tab` link, a scoped panel, its id in the tab script's list, and a project card in the Overview tab linking to `#<name>`.
- `projects/*.html` are redirect stubs for old links; don't put content there.
- Facts about Bilal: use only what he has confirmed. Never invent experience, numbers, employers or certifications.
- Regulatory facts (CSRD, ESRS, IFRS S2, CBAM, PPWR, SBTi, GHG Protocol) change often: check a current source before adding or changing a date, threshold or reference, and cite it in the page footer.
- Fictional case-study companies must stay clearly labelled as fictional.
- Commit only when Bilal asks; push to `main`. Use clear commit messages.
