# Notes for Claude

Static portfolio site for Bilal Tahir (materials engineer moving into ESG, carbon accounting and decarbonisation).

- Two pages. `index.html` (home) is the materials portfolio: Instrument Serif headings, Inter Tight body, JetBrains Mono labels; paper #F3F1EA, forest ink #0F1A16, green #2F5D46, chartreuse accent #CFE38A; photos in `assets/`. It was exported from a Claude Design canvas, so styles are mostly inline. Its small script handles the project-detail toggles and the photo lightbox; a script in `<head>` forwards old sustainability hashes to `sustainability/`.
- The sustainability portfolio lives in `sustainability/index.html` and links back home with a "Materials portfolio" tab link. The notes below describe that page.
- Plain HTML/CSS/JS, no build step. The sustainability site is one page, `sustainability/index.html`, with tabs: a sticky `.topbar` with `.tab` links and one `<section class="tabpanel" id="tab-<name>">` per tab. The hash (`#overview`, `#regulation-reader`, `#materiality-case`, `#crosswalk`, `#case-studies`) selects the tab; the list of tab ids lives in the small script at the end.
- Shared look: the sustainability page uses the same theme as the home page — Instrument Serif headings (one weight only, so display text is set to 400), Inter Tight body, JetBrains Mono for labels, tabs and regulatory references; paper/forest/green in light, forest #0E1714 with chartreuse #CFE38A accent in dark. Sentence-case labels, no all-caps eyebrows, no arrow links. The Overview opens with a strip of five CSS-textured material swatches (steel, aluminium, cement, plastics, fibre) with the EU rules that apply to each. Colour tokens are defined once in the global :root, with light and dark themes. Each tab's CSS is scoped with its panel id (e.g. `#tab-crosswalk .row{...}`), and each tab's script is wrapped in its own function, so they don't clash.
- Adding a tab: add a `.tab` link, a scoped panel, its id in the tab script's list, and a project card in the Overview tab linking to `#<name>`.
- `projects/*.html` are redirect stubs for old links; don't put content there.
- Facts about Bilal: use only what he has confirmed. Never invent experience, numbers, employers or certifications.
- Regulatory facts (CSRD, ESRS, IFRS S2, CBAM, PPWR, SBTi, GHG Protocol) change often: check a current source before adding or changing a date, threshold or reference, and cite it in the page footer.
- Fictional case-study companies must stay clearly labelled as fictional.
- Commit only when Bilal asks; push to `main`. Use clear commit messages.
