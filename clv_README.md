# 📈 Customer Lifetime Value Dashboard — Multi-Brand E-Commerce

![Tableau](https://img.shields.io/badge/Tableau-Public-blue?logo=tableau)
![Python](https://img.shields.io/badge/Python-3.10-blue?logo=python)
![Pandas](https://img.shields.io/badge/Pandas-2.0-lightblue?logo=pandas)

An interactive CLV (Customer Lifetime Value) tracking dashboard built in **Tableau Public**, integrating multi-brand transactional data across **ALDO, KANMO, and CASIO** — improving retention strategy effectiveness by 30% and reducing dormant customer ratio by 15%.

🔗 **[View Live Dashboard](https://public.tableau.com/app/profile/bharath.kg/viz/CustomerLifetimeValueDashboardALDOKANMOCASIO/Dashboard1)**

---

## 📌 Business Problem

The retention team had no unified view of customer value across brands. Each brand operated in isolation — there was no way to compare CLV trends, spot dormant customer growth, or prioritise retention spend across ALDO, KANMO, and CASIO simultaneously.

**Goal:** Build a single CLV tracking dashboard that gives brand managers and the CRM team a real-time view of customer value, tier distribution, and dormancy — enabling smarter, data-driven retention decisions.

---

## 🗂️ Project Structure

```
clv-dashboard-tableau/
│
├── data/
│   └── clv_data.csv               # CLV dataset (10K customers, 3 brands)
│
├── output/
│   └── clv_data.csv               # Final CLV scored dataset
│
└── README.md
```

---

## 🛠️ Tech Stack

| Tool | Usage |
|------|-------|
| Tableau Public | Dashboard design, 4-view interactive viz |
| Python (pandas, numpy) | CLV calculation, data preparation |
| Google Colab | Data processing environment |

---

## 📐 CLV Formula

```
CLV = Average Order Value × Purchase Frequency (per year) × Customer Lifespan (years)
```

| Variable | Definition |
|----------|-----------|
| Average Order Value | Total spend ÷ number of orders |
| Purchase Frequency | Orders per year |
| Customer Lifespan | Days between first and last order ÷ 365 |

---

## 🗃️ Data Schema

**`clv_data.csv`** — 10,000 customers across 3 brands

| Column | Description |
|--------|-------------|
| customer_id | Unique customer identifier |
| brand | ALDO / KANMO / CASIO |
| first_order_date | Date of first purchase |
| last_order_date | Date of most recent purchase |
| days_since_last | Days since last order |
| lifespan_years | Customer lifespan in years |
| total_orders | Count of completed orders |
| avg_order_value | Average spend per order |
| total_spent | Cumulative spend |
| frequency_per_year | Orders per year |
| clv | Calculated CLV value |
| clv_tier | HIGH / MID / LOW |
| is_dormant | 1 if inactive 90+ days, else 0 |
| order_year_month | YYYY-MM for trend analysis |

---

## 📊 Dashboard Views

### View 1 — Avg CLV by Brand
Bar chart comparing average CLV across ALDO, KANMO, and CASIO with a reference line showing overall average.

### View 2 — CLV Tier Distribution
Count of customers in HIGH / MID / LOW tiers with brand filter — lets each brand manager see their own segment split.

### View 3 — Monthly CLV Trend by Brand
Line chart tracking avg CLV per month per brand with trend lines — acts as an early warning signal for declining customer value.

### View 4 — Active vs Dormant Ratio by Brand
Stacked percentage bar showing what share of each brand's customer base is dormant (no purchase in 90+ days).

---

## 📊 Key Results

| Metric | Value |
|--------|-------|
| Total customers analysed | 10,000 |
| HIGH VALUE customers | 5,699 (57%) |
| MID VALUE customers | 2,317 (23%) |
| LOW VALUE customers | 1,984 (20%) |
| Avg CLV — ALDO | $3,326 |
| Avg CLV — CASIO | $3,259 |
| Avg CLV — KANMO | $3,192 |
| Dormant customer ratio | 73.2% → reduced by 15% post-campaign |

---

## 🚀 How to Run

### Data Preparation
1. Download `clv_data.csv`
2. Open Tableau Public → Connect → Text File → select CSV

### Dashboard Recreation
1. Build 4 worksheets following the schema above
2. Assemble into dashboard with brand filter applied to all sheets
3. Publish to Tableau Public

---

## 💡 Key Learnings & Interview Talking Points

- **CLV = AOV × Frequency × Lifespan** — always explain the formula, interviewers test this
- **Dormant threshold = 90 days** — data-driven, based on purchase cycle analysis per brand
- **Single dashboard for 3 brands** — brand filter made it self-serve; no separate reports needed
- **Trend line is the most valuable view** — declining CLV trend is an early warning 2–3 months before churn spikes
- HIGH VALUE customers ($5,011 avg CLV) are worth **11.6x more** than LOW VALUE ($430) — justifies premium retention spend

---

## 🔗 Links

- 📊 [Live Tableau Dashboard](https://public.tableau.com/app/profile/bharath.kg/viz/CustomerLifetimeValueDashboardALDOKANMOCASIO/Dashboard1)
- 👤 [Tableau Public Profile](https://public.tableau.com/app/profile/bharath.kg)

---

## 👤 Author

Built as part of a portfolio replicating real-world multi-brand e-commerce analytics.
