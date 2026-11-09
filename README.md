# my-websites

Bilal Tahir's sustainability portfolio: a static website (plain HTML, no build step).

## Pages

Everything is in one page, `index.html`, with four tabs. Each tab has its own link:

| Tab | Link |
| --- | --- |
| Overview (intro, projects, frameworks, experience, about) | `index.html#overview` |
| Regulation Reader AI agent, demo on Omnibus I | `index.html#regulation-reader` |
| Double materiality case study (fictional company) | `index.html#materiality-case` |
| ESRS E1 and IFRS S2 crosswalk | `index.html#crosswalk` |

The files in `projects/` only forward old links to the matching tab.

## View it on your computer

- **Simplest:** open `index.html` in your browser.
- **Local server:** in this folder run `python3 -m http.server 8000` (Windows: `py -m http.server 8000`) and visit http://localhost:8000.

## Get the latest changes

First time: `git clone https://github.com/bilaltahir364/my-websites.git`
After that, inside the folder: `git pull`

## Before sharing

- In `index.html`, replace `[your LinkedIn URL]` and `[your email]`.
- In the Regulation Reader tab, verify the rows marked "Verify in EUR-Lex".
