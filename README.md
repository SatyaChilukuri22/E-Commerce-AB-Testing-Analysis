# E-Commerce A/B Testing Analysis — Landing Page Conversion Optimization

## 📌 Project Overview

This project performs a statistical analysis of an e-commerce A/B testing experiment to evaluate whether a **new landing page** improves user conversion rates compared to the **existing landing page**.

The objective is to determine whether the observed improvement is both **statistically significant** and **practically meaningful** before recommending a full rollout.

---

# 📁 Repository Contents

| File | Description |
|---|---|
| `AB_testing_analysis.ipynb` | Complete Python analysis including data cleaning, EDA, power analysis, hypothesis testing, confidence intervals, and visualizations |
| `AB_testing.xlsx` | Excel workbook containing raw data analysis, pivot tables, summary statistics, and executive dashboard |
| `README.md` | Project documentation |
| `requirements.txt` | Required Python libraries |

---

# 📊 Dataset

The experiment dataset (`ab_data.csv`) contains approximately **290K user records** with the following features:

| Column | Description |
|---|---|
| `user_id` | Unique visitor identifier |
| `timestamp` | Experiment event timestamp |
| `group` | Experiment group (`control` / `treatment`) |
| `landing_page` | Page version (`old_page` / `new_page`) |
| `converted` | Conversion indicator (0/1) |
| `Date` | Derived date field |

---

# 🎯 Business Problem

An e-commerce company launched a new landing page and wants to understand:

- Does the new page improve conversion rate?
- Is the improvement statistically significant?
- Is the increase large enough to justify a full implementation?

---

# 🧭 Analysis Workflow

## 1. Business Understanding

- Defined business objective
- Created hypotheses
- Established success criteria


## 2. Data Understanding

- Loaded and explored experiment data
- Checked dataset structure and quality


## 3. Data Cleaning & Validation

Performed:

- Missing value analysis
- Duplicate detection
- Data consistency checks
- Group and landing page validation
- Sample Ratio Mismatch (SRM) check


## 4. Exploratory Data Analysis (EDA)

Analyzed:

- User distribution across groups
- Conversion counts
- Conversion rates
- Daily experiment trends


## 5. Business Metrics

Calculated:

- Control conversion rate
- Treatment conversion rate
- Absolute conversion lift
- Relative conversion lift
- Estimated business impact


## 6. Power Analysis

Evaluated:

- Required sample size
- Statistical power
- Ability to detect meaningful conversion changes


## 7. Hypothesis Testing

Performed:

**Two-Proportion Z-Test**

Hypotheses:

**H₀ (Null Hypothesis):**  
There is no significant difference between old and new landing page conversion rates.

**H₁ (Alternative Hypothesis):**  
The new landing page significantly changes conversion rate.
Significance Level:
α = 0.05

Decision:

- p-value < 0.05 → Reject H₀
- p-value ≥ 0.05 → Fail to Reject H₀


## 8. Confidence Interval Analysis

Calculated:

- 95% confidence interval
- Conversion rate difference range
- Practical significance


## 9. Data Visualization

Created:

- Conversion rate comparison charts
- User distribution charts
- Daily conversion trend analysis

---

# 📊 Excel Analysis

The `AB_testing.xlsx` workbook provides stakeholder-friendly analysis including:

- Raw data
- Pivot tables
- Group-level summaries
- Statistical calculations
- Executive dashboard

This allows non-technical stakeholders to understand experiment outcomes easily.

---

# 🛠️ Tools & Technologies

### Programming
- Python

### Libraries
- Pandas
- NumPy
- SciPy
- Statsmodels
- Matplotlib

### Analytics Tools
- Microsoft Excel
- Pivot Tables
- Statistical Analysis

### Environment
- Jupyter Notebook

---

# 🚀 How to Run

Install dependencies:

```bash
pip install pandas numpy scipy statsmodels matplotlib
