# 🎧 Wireless Bluetooth Headphones Price Predictor

> A complete end-to-end ML project that scrapes real headphone listings from Amazon India, engineers 25+ features, and predicts prices using machine learning.

![Python](https://img.shields.io/badge/Python-3.10+-blue?style=flat&logo=python)
![ML](https://img.shields.io/badge/ML-LightGBM%20%7C%20XGBoost-orange?style=flat)
![Data](https://img.shields.io/badge/Data-Amazon%20Scraped-yellow?style=flat)
![Status](https://img.shields.io/badge/Status-Complete-green?style=flat)

---

## 🚀 Features

- 🕷️ **Amazon Web Scraper** — scraped real headphone listings with name, price, rating, reviews
- 🔧 **Feature Engineering** — 25+ engineered features from raw product names
- 🏷️ **Brand Intelligence** — brand tier, popularity score, country of origin scoring
- 📊 **EDA & Preprocessing** — data cleaning, merging, price/rating band classification
- 🤖 **ML Price Prediction** — trained on real Amazon data to predict headphone prices

---

## 📁 Project Structure

```
Wireless-Bluetooth-Headphones-Price-Predictor/
├── scraper.py                          # Amazon scraper (pages 1-6)
├── scraper2.py                         # Amazon scraper (pages 7-12)
├── merge.py                            # Merges scraped CSV files
├── enhance.py                          # Feature engineering pipeline
├── merged.csv                          # Combined scraped dataset
├── Headphones_price_prediction.ipynb   # ML model — EDA, training, evaluation
└── README.md
```

---

## 🔧 Feature Engineering Highlights

From raw Amazon product names, the pipeline automatically extracts:

| Feature | Description |
|---------|-------------|
| `brand` | Detected brand (Bose, Sony, JBL, boAt, etc.) |
| `brand_tier` | Budget / Mid / Premium / Luxury |
| `brand_popularity` | Score 1–10 based on market presence |
| `country_of_origin` | USA, Japan, Germany, India, China, etc. |
| `country_score` | Quality score by country |
| `battery_life_hours` | Extracted from product name (regex) |
| `driver_size_mm` | Driver size extracted from name |
| `audio_latency_ms` | Latency extracted from name |
| `anc` | Active Noise Cancellation (0/1) |
| `fast_charging` | Fast charging support (0/1) |
| `form_factor` | TWS / Neckband / Over-ear / On-ear |
| `is_wireless` | Bluetooth/Wireless detection (0/1) |
| `has_mic` | Microphone presence (0/1) |
| `has_ipx` | Water resistance rating (0/1) |
| `has_spatial_audio` | Dolby/3D audio support (0/1) |
| `price_band` | Budget / Mid / Upper-mid / Premium |
| `rating_band` | Low / Medium / High / Top |
| `spec_completeness` | Score for how complete the listing is |

---

## 🛠️ Tech Stack

| Layer | Technology |
|-------|-----------|
| Scraping | Python, Requests, BeautifulSoup |
| Data Processing | Pandas, NumPy, Regex |
| Feature Engineering | Custom Python pipeline (enhance.py) |
| ML Model | LightGBM, XGBoost, Scikit-learn |
| EDA & Visualization | Matplotlib, Seaborn |
| Notebook | Jupyter Notebook |

---

## ⚙️ Setup & Usage

### 1. Clone the repository
```bash
git clone https://github.com/GeethaBurigalla/Wireless-Bluetooth-Headphones-Price-Predictor.git
cd Wireless-Bluetooth-Headphones-Price-Predictor
```

### 2. Install dependencies
```bash
pip install pandas numpy scikit-learn lightgbm xgboost beautifulsoup4 requests matplotlib seaborn
```

### 3. Run the pipeline
```bash
# Step 1 - Scrape Amazon listings
python scraper.py
python scraper2.py

# Step 2 - Merge datasets
python merge.py

# Step 3 - Engineer features
python enhance.py

# Step 4 - Open ML notebook
jupyter notebook Headphones_price_prediction.ipynb
```

---

## 📊 Dataset

- **Source:** Amazon India — Wireless Bluetooth Headphones category
- **Size:** ~1,200+ product listings (merged.csv)
- **Features:** 25+ engineered features from raw product names + listing data
- **Brands covered:** Bose, Sony, Sennheiser, Apple, JBL, Samsung, boAt, Noise, Realme, OnePlus, pTron

---

## 👥 Contributors

| Name | GitHub |
|------|--------|
| Geetha Burigalla | [@GeethaBurigalla](https://github.com/GeethaBurigalla) |
| An Chowdary | [@anchowdary-04](https://github.com/anchowdary-04) |

---


