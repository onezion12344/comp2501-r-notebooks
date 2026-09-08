# COMP2501 R Interactive Notebooks

Interactive, gamified R notebooks for **COMP2501 Introduction to Data Science** (HKU, RB Luo / 羅鉞邦). Each notebook mirrors a lecture's learning objectives and is designed to be **walked through by hand** in a browser — you read the concepts, fill in the blanks yourself, run the code, and predict the output — so the ideas stick the way git concepts stick.

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
