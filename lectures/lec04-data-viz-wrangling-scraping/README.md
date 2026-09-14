# Lec 4 — Visualization Principles, Data Wrangling & Web Scraping

Three parts that chain together: **scrape** messy data → **wrangle** it into shape → **visualize** it honestly.

## Open in Colab

[<img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab">](https://colab.research.google.com/github/onezion12344/comp2501-r-notebooks/blob/main/lectures/lec04-data-viz-wrangling-scraping/lec04_viz_wrangling_scraping.ipynb)

Set runtime to R: **Runtime ▸ Change runtime type ▸ R**.

## What's covered

**Part 1 — Visualization principles**
- The visual channels, and the **encoding hierarchy** (position always beats color/shade)
- Pie charts: why they're bad (Cleveland 1985), and what to use instead
- When to include 0 (bars) vs when cropping is OK (points); broken axes with `ggbreak`
- `reorder()` for meaningful category ordering
- Show your data: dynamite vs box vs violin vs swarm
- Colors: ≤6, hue vs shade, consistency, color-blind friendly palettes
- Adding a 3rd/4th variable — and why to stop
- Avoid pseudo-3D (use facets)
- Consistent decimal precision
- Case study: the vaccines/measles heatmap, built from scratch

**Part 2 — Data wrangling**
- Missing values (`is.na`, `na.rm`), dirty-data triage
- Tidy vs long vs wide (and why long ≠ automatically tidy)
- `pivot_longer` — backticks, the `1960:2015` trap, negative indexing
- Correct data types after reshaping
- `pivot_wider` and its merge rule
- `separate()` with `extra = 'merge'` and `fill = 'right'`
- The `pivot_longer → separate → pivot_wider` recipe
- Six joins (left/right/inner/full/semi/anti) + why `bind_cols` is dangerous
- Set operators: `intersect`, `union`, `setdiff`, `setequal`

**Part 3 — Web scraping**
- HTML structure (html/head/body, table/tr/td)
- `read_html` → `html_elements('table')` → `html_table()` → `setNames()`
- Ethics: `robots.txt`, ToS, rate limiting, public data only, the `polite` package
- SelectorGadget for finding CSS selectors

## Files

| File | Purpose |
|------|---------|
| `lec04_viz_wrangling_scraping.ipynb` | Interactive notebook — run in Colab. |

## Notes

- Needs `tidyverse` + `dslabs`; the scraping section needs `rvest`.
- The measles heatmap section downloads nothing — `us_contagious_diseases` ships with `dslabs`.
- Scraping Wikipedia live may return slightly different counts over time; the principles don't change.
