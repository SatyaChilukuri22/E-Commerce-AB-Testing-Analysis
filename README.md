# E-Commerce A/B Testing Analysis — Landing Page Conversion Optimization

## 📌 Project Overview

This project performs a statistical analysis of an e-commerce A/B testing experiment to evaluate whether a **new landing page** improves user conversion rates compared to the **existing landing page**.

The objective is to determine whether the observed improvement is both **statistically significant** and **practically meaningful** before recommending a full rollout.

---

## 📁 Repository Contents

| File / Folder | Description |
|---|---|
| `AB_Testing/Ecommerce_AB_testing_analysis.ipynb` | Complete Python analysis: data cleaning, EDA, power analysis, hypothesis testing, confidence intervals, and visualizations |
| `AB_Testing/ab_data.csv` | Raw experiment dataset |
| `AB_Testing/ab_data_clean.csv` | Cleaned dataset produced during Phase 3 |
| `AB_Testing/phase4_daily_trend.csv` | Daily conversion trend, output of Phase 4 (EDA) |
| `AB_Testing/phase4_group_summary.csv` | Control vs. treatment summary, output of Phase 4 (EDA) |
| `AB_Testing/phase5_business_metrics.csv` | Conversion rate, lift, and business impact, output of Phase 5 |
| `AB_Testing/phase7_8_test_results.csv` | Hypothesis test and confidence interval results, output of Phases 7–8 |
| `AB_Testing/chart1_conversion_comparison.png` | Conversion rate comparison chart |
| `AB_Testing/chart2_daily_trend.png` | Daily conversion trend chart |
| `AB_Testing/chart3_traffic_split.png` | Control vs. treatment traffic split chart |
| `AB_Testing/chart4_daily_volume.png` | Daily visitor volume chart |
| `AB_testing.xlsx` | Excel workbook with raw data, pivot tables, summary statistics, and an executive dashboard |
| `requirements.txt` | Required Python libraries |
| `LICENSE` | MIT License |
| `README.md` | Project documentation |

---

## 📊 Dataset

The experiment dataset (`AB_Testing/ab_data.csv`) contains approximately **290K user records** with the following features:

| Column | Description |
|---|---|
| `user_id` | Unique visitor identifier |
| `timestamp` | Experiment event timestamp |
| `group` | Experiment group (`control` / `treatment`) |
| `landing_page` | Page version (`old_page` / `new_page`) |
| `converted` | Conversion indicator (0/1) |
| `Date` | Derived date field |

---

## 🎯 Business Problem

An e-commerce company launched a new landing page and wants to understand:

- Does the new page improve conversion rate?
- Is the improvement statistically significant?
- Is the increase large enough to justify a full implementation?

---

## 🧭 Analysis Workflow

### 1. Business Understanding
- Defined business objective
- Created hypotheses
- Established success criteria

### 2. Data Understanding
- Loaded and explored experiment data
- Checked dataset structure and quality

### 3. Data Cleaning & Validation
- Missing value analysis
- Duplicate detection
- Data consistency checks
- Group and landing page validation
- Sample Ratio Mismatch (SRM) check

### 4. Exploratory Data Analysis (EDA)
- User distribution across groups
- Conversion counts
- Conversion rates
- Daily experiment trends

### 5. Business Metrics
- Control conversion rate
- Treatment conversion rate
- Absolute conversion lift
- Relative conversion lift
- Estimated business impact

### 6. Power Analysis
- Required sample size
- Statistical power
- Ability to detect meaningful conversion changes

### 7. Hypothesis Testing

**Two-Proportion Z-Test**

**H₀ (Null Hypothesis):** There is no significant difference between old and new landing page conversion rates.

**H₁ (Alternative Hypothesis):** The new landing page significantly changes conversion rate.

**Significance Level:** α = 0.05

**Decision rule:**
- p-value < 0.05 → Reject H₀
- p-value ≥ 0.05 → Fail to Reject H₀

### 8. Confidence Interval Analysis
- 95% confidence interval
- Conversion rate difference range
- Practical significance

### 9. Data Visualization
- Conversion rate comparison charts
- User distribution charts
- Daily conversion trend analysis

---

## 📊 Excel Analysis

The `AB_testing.xlsx` workbook provides stakeholder-friendly analysis including:

- Raw data
- Pivot tables
- Group-level summaries
- Statistical calculations
- Executive dashboard

This allows non-technical stakeholders to understand experiment outcomes easily.

---

## 🛠️ Tools & Technologies

**Programming:** Python

**Libraries:** Pandas, NumPy, SciPy, Statsmodels, Matplotlib

**Analytics Tools:** Microsoft Excel, Pivot Tables, Statistical Analysis

**Environment:** Jupyter Notebook

---

## 🚀 How to Run

1. Clone the repository:
```bash
git clone https://github.com/SatyaChilukuri22/E-Commerce-AB-Testing-Analysis.git
cd E-Commerce-AB-Testing-Analysis
```

2. Install dependencies:
```bash
pip install -r requirements.txt
```

3. Launch the notebook:
```bash
jupyter notebook AB_Testing/Ecommerce_AB_testing_analysis.ipynb
```

The dataset (`ab_data.csv`) is already included in the `AB_Testing/` folder, so the notebook will run end-to-end without needing any external download.

---

## 📈 Key Business Question

Does the new landing page generate a statistically and practically significant improvement in conversion rate compared to the old landing page?

The final recommendation is available in:
- Notebook conclusion section
- Excel `Dashboard` sheet
- `phase7_8_test_results.csv` statistical test results

---

## 📌 Skills Demonstrated

- A/B Testing
- Statistical Hypothesis Testing
- Data Cleaning
- Exploratory Data Analysis
- Conversion Rate Optimization
- Business Analytics
- Excel Dashboarding
- Data Visualization

---

## 📄 License

This project is licensed under the [MIT License](LICENSE).
