# Data

## Dataset — we8there.com Restaurant Reviews

This project uses two data files drawn from the **we8there.com restaurant review dataset**, originally compiled for academic NLP research.

---

### we8thereratings.csv

**6,166 rows × 5 columns** — one row per customer review, with ratings across five dimensions.

| Column | Description |
|---|---|
| `Food` | Food quality rating (1–5, 0 = missing) |
| `Service` | Service quality rating (1–5, 0 = missing) |
| `Value` | Value for money rating (1–5, 0 = missing) |
| `Atmosphere` | Atmosphere/ambiance rating (1–5, 0 = missing) |
| `Overall` | Overall experience rating (1–5) |

---

### we8therecounts.csv

**6,166 rows × 2,640 columns** — one row per review, one column per bigram (two-word phrase). Each cell contains the count of how many times that bigram appeared in that review. Most values are 0 (sparse matrix).

The rows in both files correspond to the same 6,166 reviews — they are joined by row index.

---

## Data Source and Citation

The dataset was collected from **we8there.com**, a US restaurant review website active approximately 2004–2007. It was used in the following academic paper and has since become a standard benchmark for multi-aspect sentiment analysis research:

> Snyder, B. & Barzilay, R. (2007). *Multiple Aspect Ranking using the Good Grief Algorithm.* Proceedings of NAACL-HLT 2007.

---

## Notes on Data Quality

- A small number of reviews have 0-ratings in Service, Value, and Atmosphere — these represent missing or invalid responses and are excluded from analyses involving those dimensions.
- The bigram text has been pre-processed (stemmed) — for example "very" appears as "veri" and "excellent" as "excel". This is standard NLP preprocessing from the original dataset.
- The two files must be kept in the same folder and loaded together. Row order corresponds across both files.
