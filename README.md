# 🏠 Airbnb Data Analysis — DSP Project
|
---

## 📌 Project Overview

This project performs exploratory data analysis (EDA) on a Melbourne, Australia Airbnb dataset to uncover pricing patterns, availability trends, and neighbourhood-level insights. The analysis is implemented in Python using Pandas, Matplotlib, Seaborn, and Plotly.

---

## 📂 Repository Structure

```
📦 airbnb-data-analysis/
├── 📄 README.md                                                       ← You are here
├── 📓 B1_B2_29_KrishSatdeve_B1_B2_33_AditiPaul(DSP_project).ipynb     ← Jupyter Notebook (Google Colab)
├── 📊 airbnb_listings.csv                                             ← Dataset (100 Melbourne listings)
└── 🌐 index.html                                                      ← Interactive frontend dashboard (GitHub Pages entry point)
```

---

## 📊 Dataset Description

**File:** `airbnb_listings.csv`
**Source:** Airbnb Open Data (Melbourne, Victoria, Australia)
**Records:** 100 listings | **Features:** 19 columns

| Column | Type | Description |
|--------|------|-------------|
| `id` | int | Unique listing identifier |
| `name` | string | Listing title |
| `host_id` | int | Host identifier |
| `host_name` | string | Name of the host |
| `neighbourhood_group` | bool | Neighbourhood group flag |
| `neighbourhood` | string | Area/suburb name (22 unique) |
| `latitude` | float | GPS latitude coordinate |
| `longitude` | float | GPS longitude coordinate |
| `room_type` | string | Entire home/apt, Private room, Shared room |
| `price` | float | Nightly price in AUD ($) |
| `minimum_nights` | int | Minimum stay required |
| `number_of_reviews` | int | Total reviews received |
| `last_review` | date | Date of most recent review |
| `reviews_per_month` | float | Average monthly reviews |
| `calculated_host_listings_count` | int | Total listings by host |
| `availability_365` | int | Days available per year |
| `number_of_reviews_ltm` | int | Reviews in last 12 months |
| `license` | bool | License status |

---

## 🎯 Objectives

1. **Most Expensive Areas** — Identify which Melbourne neighbourhoods command the highest average nightly price
2. **Average Price Per Neighbourhood** — Rank all 22 areas by mean price
3. **Availability Trends** — Understand how many days per year listings are open for booking
4. **Price Distribution** — Visualize the spread and skew of listing prices
5. **Geo Heatmap** — Map price intensity across Melbourne using latitude/longitude

---

## 🔍 Key Findings

### 💰 Top 5 Most Expensive Neighbourhoods
| Rank | Neighbourhood | Avg Price (AUD) |
|------|--------------|----------------|
| 1 | Bayside | $401.80 |
| 2 | Glen Eira | $268.33 |
| 3 | Melbourne | $261.60 |
| 4 | Yarra Ranges | $240.33 |
| 5 | Yarra | $198.20 |

### 📅 Availability Insights
- **Highest availability:** Hobsons Bay, Manningham, Melton, Whittlesea — all at **365 days/year**
- **Lowest availability:** Darebin, Moonee Valley — **0 days** (fully booked or inactive)
- **Most balanced:** Casey at **353 days**, Monash at **327 days**

### 🛏️ Room Type Breakdown
- **Entire home/apt** — Most common, higher prices (~$150–$400)
- **Private room** — Budget-friendly (~$40–$114)
- **Shared room** — Least common, lowest price point

### 📈 Price Distribution
- Majority of listings priced between **$50–$200**
- Heavy right skew — a few luxury listings push average up significantly
- Price range: **$35 (min)** to **$1,000 (max)**

---

## 🛠️ Tech Stack

| Tool | Purpose |
|------|---------|
| Python 3 | Core language |
| Pandas | Data manipulation & aggregation |
| Matplotlib | Static charts & plots |
| Seaborn | Statistical visualizations & heatmaps |
| Plotly Express | Interactive geo density map |
| Google Colab | Notebook execution environment |
| HTML/CSS/JS + Chart.js | Frontend dashboard (`index.html`) |

---

## ▶️ How to Run

### Option 1 — Google Colab (Notebook)
1. Upload `airbnb_listings.csv` when prompted
2. Run all cells sequentially
3. Visualizations render inline

### Option 2 — Local Jupyter
```bash
pip install pandas matplotlib seaborn plotly
jupyter notebook B1_B2_29_KrishSatdeve_...ipynb
```

### Option 3 — Frontend Dashboard
Simply open `index.html` in any modern browser — no server or dependencies required.

### Option 4 — GitHub Pages (Live Website)
1. Push all files to your GitHub repository
2. Go to **Settings → Pages**
3. Under *Source*, select **Deploy from a branch**
4. Choose `main` branch and `/ (root)` folder
5. Click **Save** — your dashboard will be live at:
   `https://<yourusername>.github.io/<yourrepo>/`

> ⚠️ The dashboard file is named `index.html` so GitHub Pages serves it automatically as the homepage.

---

## 📸 Visualizations Produced

- ✅ Price Distribution Histogram (with KDE curve)
- ✅ Average Price per Neighbourhood Heatmap
- ✅ Availability Trend Bar Chart
- ✅ Interactive Geo Density Heatmap (Plotly)
- ✅ Interactive Dashboard with filters (`index.html`)

---

## 📝 Notes

- Prices were stored as strings (e.g., `$95`) and cleaned using regex before analysis
- Rows with `"Invalid Number"` in `reviews_per_month` were handled appropriately
- The dataset represents a sample of 100 listings from Melbourne's greater metro area

---
