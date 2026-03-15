# Sentiment Analysis of M-Tix (Cinema 21) App Reviews

Individual Assignment - Pemrosesan Bahasa Alami (PBA)
Ida Bagus Adhiraga Yudhistira - 5026231120
Information Systems, Sepuluh Nopember Institute of Technology

---

## Overview

This project performs sentiment analysis on user reviews of the **M-Tix** app (Cinema 21) scraped from Google Play Store. The analysis covers the full NLP pipeline from data collection to feature extraction.

**App:** [M-Tix - Cinema 21](https://play.google.com/store/apps/details?id=lds.cinema21&hl=id)

---

## Project Structure

```
pba-task-1a-individual/
├── data/
│   ├── raw/
│   │   └── mtix_raw.csv           # Raw scraped reviews
│   └── preprocessed/
│       └── mtix_preprocessed.csv  # Cleaned and labeled data
├── notebooks/
│   ├── 01_scraping_tokenization.ipynb
│   ├── 02_preprocessing_eda.ipynb
│   ├── 03_bow_ngrams.ipynb
│   ├── 04_tfidf.ipynb
│   └── 05_pos_tagging.ipynb
├── README.md
└── requirements.txt
```

---

## Notebooks

| # | Notebook | Description |
|---|----------|-------------|
| 01 | `01_scraping_tokenization.ipynb` | Scrape reviews from Google Play Store, tokenization, lowercasing, punctuation removal |
| 02 | `02_preprocessing_eda.ipynb` | Stopword removal, stemming, labeling, EDA with pie chart and bar chart |
| 03 | `03_bow_ngrams.ipynb` | Bag of Words and N-Grams feature extraction |
| 04 | `04_tfidf.ipynb` | TF-IDF feature extraction |
| 05 | `05_pos_tagging.ipynb` | Part-of-Speech tagging |

---

## Dataset

- **Source:** Google Play Store reviews for M-Tix (id: `lds.cinema21`)
- **Languages scraped:** Indonesian (`id`) and English (`en`)
- **Total reviews:** ~19,000+
- **Labels:** Positive (score ≥ 4), Negative (score ≤ 2), Neutral excluded

---

## Requirements

See `requirements.txt` for full dependencies. Main libraries used:

- `google-play-scraper` - Scraping reviews
- `PySastrawi` - Indonesian stemmer and stopword remover
- `nltk` - Tokenization
- `pandas`, `matplotlib`, `seaborn` - Data processing and visualization
- `scikit-learn` - Feature extraction (BoW, TF-IDF)

---

## How to Run

1. Open any notebook in [Google Colab](https://colab.research.google.com/)
2. Run all cells from top to bottom
3. Notebooks 02–05 require `mtix_preprocessed.csv` from `data/preprocessed/`

---

## Results

- Sentiment distribution visualized in a **pie chart** (positive vs negative)
- Top frequent words shown in a **horizontal bar chart**
- Feature matrices generated using BoW, N-Grams, and TF-IDF
