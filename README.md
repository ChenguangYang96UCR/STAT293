# STAT293 Final Project

This repository contains the complete analysis workflow for the STAT 293 final project on the Boston Housing dataset. The project focuses on exploratory data analysis, missing-data diagnostics, multiple imputation, regression modeling, and interpretation of housing-value relationships.

## Repository Structure

- `STAT293_Final.Rmd`  
  Main R Markdown file containing the full analysis pipeline. This is the primary source file to run if you want to reproduce the project results.

- `STAT293_Final.html`  
  Rendered HTML output generated from `STAT293_Final.Rmd`. This file shows the final report/results without needing to rerun the code.

- `housing.rdata`  
  Input dataset used by the analysis. The R Markdown file loads this file directly.

- `README.md`  
  Project overview and instructions for reproducing the analysis.

## What the Code Does

The analysis in `STAT293_Final.Rmd` includes the following main steps:

1. Load the Boston Housing dataset from `housing.rdata`
2. Clean variables and create transformed variables such as log-transformed predictors/outcomes
3. Perform exploratory data analysis (EDA), including:
   - histograms
   - scatterplots with LOESS smoothers
   - correlation analysis
   - boxplots
   - spatial plots
4. Diagnose missing-data patterns using:
   - missingness summaries
   - visualization of missingness
   - MCAR testing
   - decision-tree missingness diagnostics
   - logistic regression diagnostics for missingness
5. Perform multiple imputation using `mice`
6. Fit regression models on the imputed data
7. Summarize and interpret model results

## Requirements

You should use **R 4.3 or later** if possible.

### Required R packages

Install the following packages before running the project:

```r
install.packages(c(
  "tidyverse",
  "corrplot",
  "car",
  "MASS",
  "lmtest",
  "sandwich",
  "mice",
  "broom",
  "naniar",
  "rpart",
  "rpart.plot",
  "lme4"
))
```