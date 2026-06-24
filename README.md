# Evolution Fine-Tuning — Project Page

Project page for **_Evolution Fine-Tuning: Learning to Discover Across 371 Optimization Tasks_**.

🔗 **Live (after deploy):** https://open-galapagos.github.io/evolution_finetuning/

A static, dependency-free site (plain HTML/CSS/JS) designed for GitHub Pages.
No build step is required.

## Structure

```
.
├── index.html                 # the page
├── .nojekyll                  # serve static/ as-is (skip Jekyll)
└── static/
    ├── css/style.css          # Finch brand theme (palette from the paper)
    ├── js/main.js             # nav, scroll progress, copy-BibTeX, lightbox
    └── images/
        ├── figures/           # paper figures (PDF → PNG @200dpi)
        └── logos/             # Finch mascot + favicon
```

## Deploy to GitHub Pages

This repo is meant to live at **`Open-Galapagos/evolution_finetuning`**.

```bash
# from this directory
git init
git add .
git commit -m "Evolution Fine-Tuning project page"
git branch -M main
git remote add origin https://github.com/Open-Galapagos/evolution_finetuning.git
git push -u origin main
```

Then on GitHub: **Settings → Pages → Build and deployment → Source: _Deploy from a branch_ → Branch: `main` / `/ (root)`**.
The site goes live at `https://open-galapagos.github.io/evolution_finetuning/` within a minute or two.

## Before going public — fill in the links

Open `index.html` and search for **`data-todo`** (and `ARXIV_ID_PLACEHOLDER`). Update:

| Button   | Where                          | Set to |
|----------|--------------------------------|--------|
| Paper    | hero `data-todo` button        | arXiv abstract URL |
| Dataset  | hero `data-todo` button        | Hugging Face dataset URL |
| Models   | hero `data-todo` button        | Hugging Face models/collection URL |
| BibTeX   | `#bib` block + `<meta>` tags   | replace `ARXIV_ID_PLACEHOLDER` with the arXiv id |

The **Code** button already points at `github.com/Open-Galapagos/evolution_finetuning`.

## Local preview

```bash
python3 -m http.server 8000
# open http://localhost:8000
```

## Notes on the numbers

Figures and headline numbers were taken from the paper source and cross-checked
against the result tables. The page uses the paper's canonical values
(156K trajectories, 371 tasks, 10 domains, Finch 2B–9B, +10.22% avg over base on
22 held-out tasks). The paper's draft contains a few internal inconsistencies the
authors may want to reconcile before publication (e.g. the held-out avg gain is
written as 10.22 / 10.24 / 10.31 in different places, and the held-out task count
as 22 vs 32); the page follows the abstract/intro/conclusion wording.
