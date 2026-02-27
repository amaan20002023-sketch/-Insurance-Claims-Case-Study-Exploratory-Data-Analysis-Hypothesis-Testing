# -Insurance-Claims-Case-Study-Exploratory-Data-Analysis-Hypothesis-Testing by python
# Insurance Claims Case Study  
**Exploratory Data Analysis + Hypothesis Testing**

![Python](https://img.shields.io/badge/Python-3.9%2B-blue) 
![Pandas](https://img.shields.io/badge/Pandas-2.x-green)
![Seaborn](https://img.shields.io/badge/Seaborn-0.13+-yellow)
![SciPy](https://img.shields.io/badge/SciPy-1.11+-orange)

---https://github.com/amaan20002023-sketch/-Insurance-Claims-Case-Study-Exploratory-Data-Analysis-Hypothesis-Testing

## 📋 Project Overview

This repository contains a complete **end-to-end data analysis** for the **AnalytixLabs Insurance Claims Case Study**.  

The goal was to:
- Create a **360-degree customer view** by merging claims and demographics data
- Perform thorough **data cleaning & feature engineering**
- Answer **20 business questions** through EDA and visualizations
- Conduct **statistical hypothesis testing** with detailed interpretation and business implications

---

## 📁 Dataset

| File                    | Description                          | Rows  | Columns |
|-------------------------|--------------------------------------|-------|---------|
| `claims.csv`            | Insurance claim records              | 1,100 | 10      |
| `cust_demographics.csv` | Customer demographic information     | 1,085 | 6       |
| `Insurance Claims Case Study.pdf` | Full case study brief          | -     | -       |

**Key variables**: `claim_amount`, `incident_cause`, `fraudulent`, `Segment`, `DateOfBirth`, `total_policy_claims`, etc.

---

## 🛠️ Technologies & Libraries

- **Python 3.9+**
- `pandas` – data manipulation
- `numpy` – numerical operations
- `matplotlib` & `seaborn` – visualization
- `scipy.stats` – hypothesis testing
- `datetime` – date handling

---

## 📂 Project Structure

```bash
insurance-claims-case-study/
├── insurance_case_3.ipynb          # Main Jupyter Notebook (full analysis)
├── claims.csv
├── cust_demographics.csv
├── Insurance Claims Case Study.pdf # Original case brief
├── README.md                       # This file

## Business Questions Answered

### Data Preparation & Feature Engineering
- Merged claims + demographics → 360° customer view
- Cleaned & standardized data types
- Removed currency symbol and converted `claim_amount` to numeric
- Created police unreported alert flag
- Handled duplicates → kept most recent record per customer
- Imputed missing values (mean for numeric, mode for categorical)
- Calculated customer age & created age groups: Youth (18–30), Adult (30–60), Senior (>60)

### Exploratory Data Analysis (EDA)
- Average claim amount by customer segment
- Total claim amount for incidents reported ≥ 20 days before Oct 1, 2018
- Count of adult drivers (TX, DE, AK) with driver-related claims
- **Pie chart**: Claim amount distribution by Gender × Segment (%)
- **Bar chart**: Driver-related claims by Gender
- **Bar chart**: Fraudulent claims by Age group
- **Line chart**: Monthly trend of total claimed amount (chronological order)
- **Faceted bar chart**: Avg claim amount by Gender & Age group — Fraud vs Non-Fraud

### Statistical Hypothesis Testing
- 16. Similarity in claim amounts: Males vs Females → t-test
- 17. Association between Age group & Segment → Chi-square
- 18. 2018 claims significantly higher than $10,000 historical avg → one-sample t-test
- 19. Difference in claims across age groups → ANOVA
- 20. Correlation between # of policy claims & claim amount → Pearson

## 🔍 Key Takeaways for the Business

- **Alert: Significant rise in average claim value in 2018** compared to $10,000 historical benchmark (statistically confirmed)  
  → Potential early warning of fraud wave or changing claim patterns — **prioritize review**
- **Highest fraud proportion in Youth (18–30) segment**  
  → Age-based risk segmentation and enhanced verification recommended
- Claim amounts show **no statistically significant gender difference**  
  → Supports fair, non-gendered pricing models
- **Driver error is the leading incident cause**, disproportionately claimed by males  
  → Targeted education / telematics programs could reduce loss ratio
- **Weak to no relationship** between number of prior claims and claim severity  
  → Number of claims alone is not a reliable indicator for high-value losses

All conclusions are backed by appropriate statistical tests (t-test, ANOVA, Chi-square, correlation) with p-value interpretation.

