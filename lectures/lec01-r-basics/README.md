# Lec 1 — R Basics

Covers: R objects & `<-`, workspace / `ls()` / `rm()`, case-sensitivity, functions & arguments (`log`, `?help`), atomic types (`numeric`/`integer`/`logical`/`character`/`factor`), integer-vs-numeric & indexing, data frames (`str`/`head`/`names`/`dim`/`$`), plus vectorization & recycling.

## Open in Colab

[<img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab">](https://colab.research.google.com/github/onezion12344/comp2501-r-notebooks/blob/main/lectures/lec01-r-basics/lec01_r_basics.ipynb)

Once open, set the runtime to R: **Runtime ▸ Change runtime type ▸ R** (it may auto-detect).

## Files

| File | Purpose |
|------|---------|
| `lec01_r_basics.ipynb` | The interactive notebook — run in Colab. R kernel. |
| `lec01_r_basics.Rmd` | Same content as an R Markdown file — use this if you want to *knit* (posit Cloud native). |

## Notes

- Uses base R datasets (`mtcars`) so it runs with **no extra installs**. The optional `dslabs::murders` section needs `install.packages("dslabs")`.
- Every task has a collapsed "Reveal answer" — try before you look.
