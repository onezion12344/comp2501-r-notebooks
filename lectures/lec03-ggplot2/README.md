# Lec 3 — Data Visualization with ggplot2 (and in practice)

The grammar of graphics, then distributions, then the Gapminder/Rosling case study.

## Open in Colab

[<img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab">](https://colab.research.google.com/github/onezion12344/comp2501-r-notebooks/blob/main/lectures/lec03-ggplot2/lec03_ggplot2.ipynb)

Set runtime to R: **Runtime ▸ Change runtime type ▸ R**.

## What's covered

**Part 1 — Why visualize, and how ggplot2 thinks**
- Table vs plot; EDA; Tukey's "greatest value of a picture"
- Where visualization shows up (John Snow 1854 → COVID dashboard → HK population pyramid → Rosling)
- **"Garbage in, garbage out"**: the Mars Climate Orbiter units failure, and the one-typo correlation demo
- The components of a graph: **data, geometry, aesthetic mapping** (+ coord, position, labels, theme, facet)
- ggplot objects; layers via `+` (and why `|>` ≠ `+`)
- `aes()` and the "bare column names" behaviour
- **Inside `aes()` = mapping; outside = fixed value** (`aes(color = region)` vs `color = 'blue'`)
- `nudge_x`; global vs local aes (local overrides)
- Scales (`scale_x_continuous(trans='log10')`, `scale_x_log10()`)
- Labels/titles (`labs`, `xlab`/`ylab`/`ggtitle`), legend titles
- `geom_abline` (a constant rate is slope 1 on log-log), `lty` line types
- `ggthemes`, `geom_text_repel`, `gridExtra::grid.arrange`
- The version-pinning note (dplyr 1.1.0 / `reframe`)

**Part 2 — Distributions**
- Variable types (ordinal/nominal, discrete/continuous)
- `geom_bar` vs `geom_col`; `count()` + proportion
- Histograms and why **binwidth is a modelling choice**
- Smoothed density (`adjust`, `alpha`, area = 1)
- Normal distribution, `stat_function(fun = dnorm)`, overlaying a fitted curve
- Boxplot: quartiles, IQR, outlier rule (Q1−1.5·IQR, Q3+1.5·IQR), `coord_flip()`
- Violin, Q-Q plot (`geom_qq` + `geom_qq_line`)
- **Stratification** as the unifying concept

**Part 3 — In practice (Gapminder / Hans Rosling)**
- Rosling's infant-mortality quiz — "more than ignorant, we are misinformed"
- Scatterplots: fertility vs life expectancy, colored by continent
- **Faceting**: `facet_grid(row ~ col)`, `.` for the unused dimension, `facet_wrap`
- **Why fixed scales matter** — and how `scales='free'` destroys the message
- Time series: `geom_line`, and reading the missing-data warning
- Labels instead of legends (`geom_textpath`)
- `dollars_per_day = gdp/population/365`; **log transformations** (multiplicative → additive)
- **Transform the scale, not the values** (and why); which base to use
- Multimodal distributions
- Boxplot / swarm / **ridge plots** (`ggridges`) — three ways to compare distributions
- 1970 vs 2010: **`intersect()` the country lists first**, then facet and compare

## Files

| File | Purpose |
|------|---------|
| `lec03_ggplot2.ipynb` | Interactive notebook — run in Colab. |
| `lec03_ggplot2.Rmd` | R Markdown version — knit in posit Cloud / RStudio. |

## Notes

- Needs `tidyverse` + `dslabs`; optional `ggthemes`, `ggrepel`, `ggridges`.
- **Keep the [ggplot2 cheat sheet](https://github.com/rstudio/cheatsheets/blob/main/data-visualization.pdf) open** — the lecturer explicitly says don't memorize the functions.
- The lecturer's own summary: *"The final exam won't demand a perfectly working copy of code... I care about correct understanding and good ideas."*
