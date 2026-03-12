# STAT293 Final Project

This repository contains the full workflow for the STAT 293 final project on Boston Housing data, including data preparation, missing-data diagnostics, multiple imputation, nonlinear/spatial modeling, sensitivity analysis, slides, and report outputs.

## Repository Structure

- `housing.rdata`: input data object used in analysis.
- `stat293 final.Rmd`: main analysis pipeline (missingness diagnostics, MICE, model fitting, pooling, MNAR sensitivity).
- `STAT293_Final.html`: rendered analysis output from the R Markdown workflow.
- `main.tex`: slide deck source.
- `report.tex`: final technical report source.
- `report.pdf`: compiled report.
- `1.jpg`, `2.jpg`, `3.jpg`, `4.jpg`: EDA figures used in the report.
- `Final_project_description.pdf`: course project requirements.

## Reproducibility: Step-by-Step

## 1. Environment

Use R (recommended: `R >= 4.3`) with the following packages:

- `tidyverse`
- `corrplot`
- `car`
- `MASS`
- `lmtest`
- `sandwich`
- `mice`
- `broom`
- `naniar`
- `rpart`
- `rpart.plot`
- `lme4`
- `splines` (base R)

For PDF compilation, use a LaTeX distribution with `pdflatex` (TinyTeX/TeX Live works).

## 2. Run the analysis

From project root:

```bash
Rscript -e "knitr::knit('stat293 final.Rmd', output='STAT293_Final.md')"
```

Or render HTML (if Pandoc is available):

```bash
Rscript -e "rmarkdown::render('stat293 final.Rmd')"
```

This produces the analysis outputs used to populate model and sensitivity results in the report.

## 3. Compile report

```bash
pdflatex report.tex
pdflatex report.tex
```

Running twice resolves cross-references.

## 4. Compile slides (optional)

```bash
pdflatex main.tex
pdflatex main.tex
```

## Notes

- The report includes pooled model results and MNAR sensitivity summaries from the analysis workflow.
- Missing-data handling is a core analytical component (not a preprocessing footnote): diagnostics, MAR-based MI, and MNAR sensitivity are all included.
- If you run on a different machine, record your R version and package versions for strict reproducibility.

## Team

- Luhan Tang
- Chenguang Yang
