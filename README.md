# M-Tix Sentiment Analysis

End-to-end NLP pipeline on **19,000+ user reviews** of the [M-Tix](https://play.google.com/store/apps/details?id=lds.cinema21&hl=id) app (Cinema 21 ticketing) from Google Play Store. All text processing uses Indonesian language tools.

> Scraping → Preprocessing → BoW / N-Grams → TF-IDF → POS Tagging

---

## Notebooks

| # | Notebook | What it does |
|---|----------|--------------|
| 01 | `01_scraping_tokenization.ipynb` | Scrape all reviews, tokenization, lowercasing, punctuation removal |
| 02 | `02_preprocessing_eda.ipynb` | Remove stopwords, stem, label sentiment, visualize distributions |
| 03 | `03_bow_ngrams.ipynb` | Bag of Words, bigram/trigram analysis |
| 04 | `04_tfidf.ipynb` | TF-IDF extraction, top words per sentiment |
| 05 | `05_pos_tagging.ipynb` | POS tagging, POS distribution across reviews |

---

## Project Structure

```
pba-task-1a-individual/
├── data/
│   ├── raw/
│   │   ├── mtix_raw.csv
│   │   └── mtix_tokenized.csv
│   └── preprocessed/
│       └── mtix_preprocessed.csv
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

## Quick Start

**Colab (recommended):** Open any notebook and run all cells from top to bottom.

**Local:**

```bash
git clone https://github.com/adhiraga/pba-task-1a-individual.git
cd pba-task-1a-individual
pip install -r requirements.txt
```

> Run notebooks in order: 01 → 02 → 03 → 04 → 05. Notebooks 03–05 require `mtix_preprocessed.csv`.

---

## Tech Stack

| Category | Libraries |
|----------|-----------|
| Scraping | google-play-scraper |
| NLP | NLTK, PySastrawi |
| Feature Extraction | scikit-learn (CountVectorizer, TF-IDF) |
| Data | Pandas, NumPy |
| Viz | Matplotlib, Seaborn |

---

## App Info

| | |
|---|---|
| **App** | M-Tix - Cinema 21 |
| **App ID** | `lds.cinema21` |
| **Reviews** | 19,000+ (Indonesian + English) |
| **Rating split** | Score ≥ 4 → Positive, Score ≤ 2 → Negative, Score = 3 → excluded |

---

## Author

Ida Bagus Adhiraga Yudhistira — 5026231120 · Information Systems · Sepuluh Nopember Institute of Technology
