# 🎵 Spotify Scenario Dataset — Exploratory Data Analysis

![Python](https://img.shields.io/badge/Python-3.x-blue)
![Pandas](https://img.shields.io/badge/Pandas-EDA-green)
![Seaborn](https://img.shields.io/badge/Seaborn-Visualization-orange)
![Matplotlib](https://img.shields.io/badge/Matplotlib-Plots-red)
![NumPy](https://img.shields.io/badge/NumPy-Numeric-lightblue)

---

## 📌 Project Overview

An end-to-end Exploratory Data Analysis (EDA) on a **391,989-track Spotify dataset** covering audio features, popularity trends, AI-generated content, and short-form music behavior across three 2026 scenario categories: **mainstream**, **chill**, and **AI-generated**.

---

## 📂 Dataset

| Property | Details |
|----------|---------|
| **Rows** | 391,989 tracks |
| **Columns** | 20 features |
| **Memory** | ~153 MB |
| **Source** | Spotify Scenario Dataset (2026) |

### Key Features
- `acousticness`, `danceability`, `energy`, `instrumentalness`
- `loudness`, `tempo`, `valence`, `speechiness`, `liveness`
- `popularity`, `scenario`, `ai_generated`, `short_form`

---

## 🔍 Analysis Performed

### 🧹 Data Preprocessing
- Checked for missing values → None found ✓
- Identified and removed 1,011 duplicate rows
- Imputed numeric columns with median, categorical with mode

### 📊 Exploratory Data Analysis (EDA)
- **Popularity Distribution** — Histogram with KDE
- **Correlation Heatmap** — Audio features vs popularity
- **Scenario-Based Popularity** — Bar chart by scenario
- **Audio Feature Distribution** — Histograms for danceability, energy, valence
- **Energy vs Popularity** — Scatter plot
- **Danceability by Short-form Content** — Violin plot

---

## 📈 Key Findings

- 🎯 ~**78,000 tracks** have a popularity score of **0** (long-tail effect)
- 🌟 Mainstream success (popularity > 80) is limited to **< 1%** of the catalog
- 🔊 **Loudness (0.24)**, valence (0.14), and danceability (0.13) are the strongest correlates with popularity — all relatively weak
- 📱 **Short-form content** is biased toward higher danceability (~0.65 median vs 0.62 for full-length)
- 🤖 Popularity is **evenly distributed** across mainstream, chill, and AI-generated scenarios
- ⚡ Strong inter-feature relationships: energy ↔ loudness (0.75), acousticness ↔ energy (-0.71)

---

## 🛠️ Tools & Libraries

```
Python 3.x
├── pandas       — Data manipulation & preprocessing
├── numpy        — Numerical computation
├── matplotlib   — Base plotting
└── seaborn      — Statistical visualizations
```

---

## ⚙️ How to Run

```bash
# 1. Clone the repository
git clone https://github.com/Rishika-2011/spotify-scenario-analysis.git
cd spotify-scenario-analysis

# 2. Install dependencies
pip install -r requirements.txt

# 3. Launch the notebook
jupyter notebook spotify_analysis.ipynb
```

---

## 🤖 Modeling Recommendations

1. **Address Target Imbalance** — Use SMOTE, class weighting, or log-transform popularity
2. **Incorporate Non-Audio Features** — Artist followers, playlist inclusion, release date
3. **Engineer Interaction Features** — e.g., `danceability × short_form`
4. **Handle Bimodal Energy Distribution** — Cluster into acoustic vs mainstream content types
5. **Use Tree-Based Models** — XGBoost, LightGBM, or Random Forest over linear methods
6. **Define Success Metrics Carefully** — Use precision@k, NDCG@k, or MAE on log-popularity
7. **Validate by Scenario** — Evaluate separately for mainstream, chill, and AI-generated segments

---

## 👤 Author

> 📊 Data Scientist | Python · SQL · R · Power BI | Passionate about data-driven insights

---

## 📄 License

This project is open-source and available under the [MIT License](LICENSE).


---

## Kaggle Link for Large dataset

https://www.kaggle.com/datasets/rishikarr/spotify-dataset/data

---
## Project Visualized Graphs 

https://drive.google.com/drive/folders/1kOJs4rkKRJwKMpWb69RcVaZU_ZgoyPEB?usp=drive_link
