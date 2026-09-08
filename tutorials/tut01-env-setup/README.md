# Tut 1 — Environment Setup

How to get R running with **zero local install**. The course walks you through installing R + RStudio locally, but you don't need to — you can do everything in the browser.

## Why no local install

RStudio is just an IDE (a comfortable shell around R). The **language** and the concepts run fine without it. If you don't want to give up disk space (RStudio + R is ~1 GB+), use a browser environment instead.

## Option A — Google Colab (recommended for running code)

- Free, no install, no account setup beyond a Google sign-in.
- To use **R** specifically, create/open a notebook and set: **Runtime ▸ Change runtime type ▸ R**.
- ⚠️ Colab's R support is officially **"no ETA"** for a first-class kernel — it works, but you may be on an unofficial path. Sessions are ephemeral: VMs are recycled when idle, and packages reinstall each session.
- Colab is `.ipynb`-native — it has no "Knit" button for `.Rmd`.

## Option B — posit Cloud (recommended for knitting .Rmd)

- Browser-based RStudio, free plan ~**25 compute hours / month** (verified 2026), 50 projects, 1 CPU / 1 GB RAM per project, no credit card required.
- **Best for the course's `.Rmd` files** — it's real RStudio and can *knit* R Markdown natively.
- Overage is ~10¢/hour; 15-min idle suspension; projects suspend when idle.
- **How to use:** sign up → New Project → upload your `.Rmd` → Knit.
- There's also a **Cloud Plus** (~$5/month) if you outgrow free hours, and student plans give more headroom.

## Option C — install locally (if you ever have to)

The course's slides cover this: install **R** from CRAN, then **RStudio** from posit.co. Mac users need the Apple-silicon `.pkg` (M1/M2, `R-*-arm64.pkg`). See `Lec01` slides 40-46.

## Good habits (from the lecture)

- Get comfortable in the **Console** — it's interactive exploration. Save work as a script you can re-run.
- `ls()` lists objects; `rm(x)` removes one; `?function` opens docs; auto-complete with tab.
- Empty your environment / don't blindly "restore .RData" — it can cause silent bugs from leftover state.

## Which to pick for this course

| Task | Use |
|------|-----|
| Run R code interactively | **Colab** (fast, free) |
| Knit a `.Rmd` / submit course work | **posit Cloud** (native RStudio) |
| Follow the lecture exactly (install steps) | local install — optional |

Anything you want us to build (a Colab notebook, a knitted `.Rmd` from your exercise) — just ask.
