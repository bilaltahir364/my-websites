# Notes for Claude

Static portfolio site for Bilal Tahir (materials engineer moving into ESG, carbon accounting and decarbonisation).

- One content page: `sustainability/index.html`. The former materials home page was merged into its Overview tab (portrait, key figures, materials research cards, MSc lab gallery with lightbox, Cellulose Valley partners, expertise, experience, education, contact); photos are in `assets/`, referenced as `../assets/`.
- Root `index.html` is only a redirect to `sustainability/`; its script maps old home anchors (#about, #work, #lab, #journey, #expertise, #contact) and tab hashes to the right place. Non-tab hashes on the sustainability page scroll to that element inside Overview.
- Plain HTML/CSS/JS, no build step. The sustainability site is one page, `sustainability/index.html`, with tabs: a sticky `.topbar` with `.tab` links and one `<section class="tabpanel" id="tab-<name>">` per tab. The hash (`#overview`, `#regulation-reader`, `#materiality-case`, `#crosswalk`, `#case-studies`) selects the tab; the list of tab ids lives in the small script at the end.
- Shared look: the sustainability page uses the same theme as the home page — Instrument Serif headings (one weight only, so display text is set to 400), Inter Tight body, JetBrains Mono for labels, tabs and regulatory references; paper/forest/green in light, forest #0E1714 with chartreuse #CFE38A accent in dark. Sentence-case labels, no all-caps eyebrows, no arrow links. The Overview opens with a strip of five CSS-textured material swatches (steel, aluminium, cement, plastics, fibre) with the EU rules that apply to each. Colour tokens are defined once in the global :root, with light and dark themes. Each tab's CSS is scoped with its panel id (e.g. `#tab-crosswalk .row{...}`), and each tab's script is wrapped in its own function, so they don't clash.
- Adding a tab: add a `.tab` link, a scoped panel, its id in the tab script's list, and a project card in the Overview tab linking to `#<name>`.
- `projects/*.html` are redirect stubs for old links; don't put content there.
- Facts about Bilal: use only what he has confirmed. Never invent experience, numbers, employers or certifications.
- Regulatory facts (CSRD, ESRS, IFRS S2, CBAM, PPWR, SBTi, GHG Protocol) change often: check a current source before adding or changing a date, threshold or reference, and cite it in the page footer.
- Fictional case-study companies must stay clearly labelled as fictional.
- Commit only when Bilal asks; push to `main`. Use clear commit messages.
