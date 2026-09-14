# Tutorial 2 — In-class Exercises 02 (interactive)

The official **Exercises 02** — "the cookbook": seven plots of the `iris` dataset, one geometry each.

## Open in Colab

[<img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab">](https://colab.research.google.com/github/onezion12344/comp2501-r-notebooks/blob/main/tutorials/tut02-inclass-exercises/tut02_inclass_exercises.ipynb)

Set runtime to R: **Runtime ▸ Change runtime type ▸ R**.

## What's covered

| Part | Question | Geometry |
|---|---|---|
| a | inspect the data (`head`/`dim`/`names`/`str`) | — |
| b | relationship between two continuous variables | scatter |
| c | relationship, colored by category | scatter + `color` |
| d | distribution by category | boxplot |
| e | distribution of one continuous variable | histogram (binwidth!) |
| f | shape of a distribution by category | violin |
| g | comparing distributions across categories | density |

**Why this set matters:** it's a *lookup table* for "question type → geometry". Each part also reinforces the Lec 3 distinctions — **inside vs outside `aes()`**, and **which axis gets the categorical variable**.

## Files

| File | Purpose |
|------|---------|
| `tut02_inclass_exercises.ipynb` | Interactive walkthrough — run in Colab. |
| `tut02_inclass_exercises.Rmd` | R Markdown version — knit in posit Cloud / RStudio. |

## Notes

- Uses only `iris` (base R) — **no extra installs** beyond `tidyverse`.
- Part (e)'s `binwidth = 0.2` is deliberate: try 0.05 and 0.5 and watch the bimodality appear and vanish.
- The dataset is 150 flowers, 4 numeric columns + 1 factor (`Species`, 3 levels).
