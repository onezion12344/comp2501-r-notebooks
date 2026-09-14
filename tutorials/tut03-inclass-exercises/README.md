# Tutorial 3 — In-class Exercises 03 (interactive)

The official **Exercises 03** as a fill-in walkthrough: **web scraping with `rvest`**, then wrangling the scraped table.

## Open in Colab

[<img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab">](https://colab.research.google.com/github/onezion12344/comp2501-r-notebooks/blob/main/tutorials/tut03-inclass-exercises/tut03_inclass_exercises.ipynb)

Set runtime to R: **Runtime ▸ Change runtime type ▸ R**.

## What's covered

Scrape the Wikipedia "List of athletes with at least six Olympic appearances" table, then:

1. Clean it — rename columns, convert to integers, recompute `total` (the original has a footnote that makes it character)
2. Find the most gold / silver / bronze with **all ties** (`filter(col == max(col))`)
3. Longest age span — `separate()` on `' years '`, `remove = FALSE`
4. Split single-sport vs multi-sport athletes — `separate(fill=, extra=)` and `is.na()`
5. Most common sport among single-sport athletes — `group_by` → `summarise(n = n())`

## Files

| File | Purpose |
|------|---------|
| `tut03_inclass_exercises.ipynb` | Interactive walkthrough — run in Colab. |
| `tut03_inclass_exercises.Rmd` | R Markdown version — knit in posit Cloud / RStudio. |

## Notes

- Needs `rvest` (plus `dplyr`, `tidyr`).
- **Wikipedia changes.** The answer key's numbers (239 athletes, 47 shooters, etc.) were correct when written. If your counts differ slightly, that's Wikipedia being edited — the method is what matters.
- Exercise 4 is the real payoff of Lec 4's `separate(extra=, fill=)` lesson: one athlete competed in three sports, which breaks the naive 2-column split.
