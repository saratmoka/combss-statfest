# combss-statfest

Companion repository for the StatFest talk *COMBSS: Scalable Best Subset Selection for Generalised Linear Models* (Sarat Moka, UNSW Sydney).

The repo contains runnable simulation and real-data demos in **R** and **Python** for the `combss` packages. Slides for the talk itself are produced separately in Keynote.

## Structure

```
combss-statfest/
├── _quarto.yml            # site config (HTML + PDF)
├── index.qmd              # landing
├── install.qmd            # R + Python install steps
├── demos/
│   ├── 01-simulation.qmd  # linear sim, n=300, p=30
│   ├── 02-khan.qmd        # Khan SRBCT, n=83, p=2308
│   └── 03-comparisons.qmd # head-to-head vs lasso
├── data/
│   ├── Khan_train.csv
│   └── Khan_test.csv
├── figures/               # static images (optional)
└── styles.css
```

## Build

```bash
# preview locally (live reload)
quarto preview

# one-shot render (HTML)
quarto render

# render the printable handout
quarto render --to pdf
```

The HTML site lands in `_site/`; the PDFs sit alongside each `.qmd` after a PDF render.

## Run the demos yourself

1. Install the packages — see `install.qmd`.
2. Open a `.qmd` in RStudio or VSCode and run the chunks interactively, **or** just read the rendered HTML.

## Data

- `data/Khan_train.csv` and `data/Khan_test.csv` — Khan et al. (2001) SRBCT microarray, $n_{\text{train}} = 63$, $n_{\text{test}} = 20$, $p = 2308$ genes, 4 tumour classes.
- Other demos are seeded simulations — no external data needed.

## Packages

- R — [combss on CRAN](https://cran.r-project.org/web/packages/combss/index.html)
- Python — [combss on PyPI](https://pypi.org/project/combss/)
