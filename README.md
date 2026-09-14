# COMP2501 R Interactive Notebooks

Interactive, gamified R notebooks for **COMP2501 Introduction to Data Science** (HKU, RB Luo / 羅鉞邦). Each notebook mirrors a lecture's learning objectives and is designed to be **walked through by hand** in a browser — you read the concepts, fill in the blanks yourself, run the code, and predict the output — so the ideas stick the way git concepts stick.

## ▶ Open in Colab (one click)

| Notebook | What it covers | Open |
|----------|----------------|------|
| **Lec 1 — R Basics** | objects, `<-`, functions, atomic types, data frames, vectorization | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/onezion12344/comp2501-r-notebooks/blob/main/lectures/lec01-r-basics/lec01_r_basics.ipynb) |
| **Lec 2 — tidyverse & Data Import** | R Markdown, dplyr verbs + pipe, group_by/summarize, purrr, case_when, read_csv | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/onezion12344/comp2501-r-notebooks/blob/main/lectures/lec02-tidyverse/lec02_tidyverse.ipynb) |
| **Lec 3 — ggplot2 & Visualization in Practice** | grammar of graphics, aes inside/outside, scales, themes, distributions, boxplot/violin/density, faceting, log scales, Gapminder case study | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/onezion12344/comp2501-r-notebooks/blob/main/lectures/lec03-ggplot2/lec03_ggplot2.ipynb) |
| **Lec 4 — Viz, Wrangling & Scraping** | encoding hierarchy, pie-vs-bar, include 0, reorder, show-your-data, colors, pivot_longer/wider, separate, joins, set ops, rvest | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/onezion12344/comp2501-r-notebooks/blob/main/lectures/lec04-data-viz-wrangling-scraping/lec04_viz_wrangling_scraping.ipynb) |
| **Tutorial 1 — In-class Exercises 01** | the official exercises: mtcars + the 5 dplyr verbs | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/onezion12344/comp2501-r-notebooks/blob/main/tutorials/tut01-inclass-exercises/tut01_inclass_exercises.ipynb) |
| **Tutorial 3 — In-class Exercises 03** | Wikipedia scraping with rvest, `separate()` with fill/extra, top-with-ties, group counts | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/onezion12344/comp2501-r-notebooks/blob/main/tutorials/tut03-inclass-exercises/tut03_inclass_exercises.ipynb) |

> **After opening:** set the runtime to R — `Runtime ▸ Change runtime type ▸ R` (Colab usually auto-detects the R kernel from the notebook metadata).
>
> **Sharing note:** this repo is **private**. The Colab links work for you (signed in) and for anyone you add as a collaborator. To make the links work for *anyone*, flip the repo to public in GitHub → Settings → General → Danger Zone.


## Why these exist

The course teaches R + tidyverse. RStudio is just an IDE wrapper; the language and concepts run fine without it. These notebooks let you work **zero-install**:

- **Google Colab** (R runtime): best for running the code cells interactively. Free, no install.
- **posit Cloud**: best if you need to **knit an `.Rmd`** (the course's native format). Free plan ~25 compute hours/month.

The philosophy matches the course: AI can *write* R code for you, but you must be able to *read, predict, and understand* it. So most cells are deliberately **left blank or prompted as questions**, and the answer is in a collapsed section you reveal after trying.

## Structure — organized by lecture & tutorial

```
lectures/
  lec01-r-basics/        R objects, assignment, functions, atomic types, data frames (Lec 1)
  lec02-tidyverse/       tidyverse: dplyr verbs, importing data (Lec 2)
tutorials/
  tut01-env-setup/       environment setup (RStudio panes, packages) + zero-install alternative
  tut01-inclass-exercises/  the in-class exercises 01 (mtcars + dplyr), worked interactively
```

Each folder has its own `README.md` with an **Open in Colab** link and, where relevant, a matching `.Rmd`.

## How to use (the loop)

1. Open the notebook in Colab (link in each folder's README, or `File > Open notebook > GitHub`).
2. Make sure the runtime is **R**: `Runtime > Change runtime type > R`.
3. Walk top to bottom. **Read the concept cell → predict the output → write the code in the blank → run → compare.**
4. Reveal the answer cell only after you've genuinely tried.
5. Local changes stay in your own Colab copy. The GitHub repo is always a fresh reference copy — if you break something, re-open the notebook.

## Contribution / sharing

- Repo is **private** by default. To share with a classmate, either make it public (one command in GitHub settings) or add them as a collaborator.
- Anyone who opens a notebook via the Colab link always gets a fresh copy to play with — your edits never touch the repo.

---

### Note on this course's use of AI

This course explicitly *encourages* using LLMs to assist study, but the lecturer's rule of thumb is: **"make sure you understand what LLMs are doing, especially when they are making mistakes."** These notebooks are built around that exact rule — they force you to understand the output yourself rather than paste-and-run.
