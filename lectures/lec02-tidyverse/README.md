# Lec 2 — R Markdown, tidyverse & Data Import

Covers: R Markdown (markdown + code chunks + knitr options), tidy data, the 5 core dplyr verbs + the pipe `|>`, the average-rate trap, `group_by`→`summarize`, purrr (`map`/`map_dbl`/`map_df`), conditional `case_when`/`between`, and importing data (`read_csv`, working directory, paths, encoding).

## Open in Colab

[<img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab">](https://colab.research.google.com/github/onezion12344/comp2501-r-notebooks/blob/main/lectures/lec02-tidyverse/lec02_tidyverse.ipynb)

Set runtime to R: **Runtime ▸ Change runtime type ▸ R**.

## Files

| File | Purpose |
|------|---------|
| `lec02_tidyverse.ipynb` | Interactive notebook — run in Colab. |
| `lec02_tidyverse.Rmd` | Same content as R Markdown — knit in posit Cloud / RStudio. |

## Notes

- Needs `tidyverse` (dplyr/readr/ggplot2/purrr). The `dslabs` package is used for the `murders` and `heights` examples — `install.packages("dslabs")` once.
- The COVID example reads from the course's URL (`bio8.cs.hku.hk`) — needs internet.
- The markdown-cheatsheet section is a real markdown cell; edit it to practice before moving to the code.
