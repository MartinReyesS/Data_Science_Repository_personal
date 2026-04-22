# arXiv Metadata Analysis (2015–2025)
 
**Focus:** Data scraping, cleaning, SQLite, visualisation, text classification (NLP) on arXiv articles from `hep-th` and `gr-qc`.

**Link to data recompiled**: https://drive.google.com/file/d/15vXNbm77s9r1vY8ux8PXSWlVNG91mS0N/view?usp=drive_link

## Overview

This project collects metadata from arXiv using its public API, cleans and stores the data in SQLite, performs exploratory analysis (time series, word clouds, keyword trends), and trains a Logistic Regression classifier to predict the primary category from title+abstract.


## Key results

- **Articles collected:** 81,000+ (2015–2025, `hep-th` and `gr-qc`).
- **Top authors:** [`Salvatore Capozziello`, `Robert B. Mann`, `A. Morozov`, etc]
- **Keyword trends:** `black hole`, `quantum`, `gravity`.
- **Best classifier:** Logistic Regression – **77% accuracy** (multi‑class).

