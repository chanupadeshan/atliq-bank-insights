# Atliq Bank Project

## 1. Project Overview
The Atliq Bank Project is a comprehensive data analysis and A/B testing case study using synthetic banking data. The project covers customer profiling, credit analysis, transaction behavior, and the impact of targeted marketing campaigns. The analysis is performed in two main phases:
- **Phase 01:** Data cleaning, preprocessing, and exploratory data analysis (EDA) on customer, credit, and transaction data.
- **Phase 02:** A/B testing and statistical analysis to evaluate the effectiveness of a marketing campaign targeting the 18-25 age group.

## 2. Folder Structure
```
ATLIQ BANK PROJECT/
├── datasets/
│   ├── avg_transactions_after_campaign.csv
│   ├── credit_profiles.csv
│   ├── customers.csv
│   └── transactions.csv
├── Phase_01_atliq_bank.ipynb
├── Phase_02.ipynb
└── README.md
```

## 3. Data Sources & Structure
The project uses the following datasets (CSV files, typically in a `datasets/` folder):
- `customers.csv`: Customer demographic and profile data
- `credit_profiles.csv`: Credit score and credit limit information
- `transactions.csv`: Detailed transaction records
- `avg_transactions_after_campaign.csv`: Aggregated transaction data for A/B testing

## 4. Data Cleaning & Preprocessing
**Phase 01** includes extensive data cleaning steps:
- **Handling Missing Values:**
  - Imputation of missing `annual_income` and `credit_limit` using median values by occupation or credit score range.
  - Outlier detection and correction for `annual_income`, `age`, and `outstanding_debt`.
- **Duplicates:**
  - Removal of duplicate customer and credit records.
- **Outlier Treatment:**
  - Outliers in `annual_income` and `age` are replaced with occupation/age group medians.
  - Transaction outliers are capped or replaced with category means.
- **Data Consistency:**
  - Ensured all categorical and numerical columns are in the correct format.
  - Standardized transaction amounts and filled missing platform values.

## 5. Exploratory Data Analysis (EDA)
- **Customer Demographics:**
  - Distribution of age, income, gender, occupation, and marital status.
  - Median income and age by occupation.
- **Credit Profiles:**
  - Distribution and segmentation of credit scores.
  - Analysis of credit utilization, outstanding debt, and credit limits.
  - Correlation analysis between age, income, credit score, and debt.
- **Transaction Analysis:**
  - Transaction volume and amount by platform, product category, and payment type.
  - Outlier and zero-amount transaction handling.
  - Visualization of transaction amount distributions.

## 6. A/B Testing & Statistical Analysis (Phase 02)
- **Target Group:** Customers aged 18-25 (~25% of the base).
- **Pre-campaign Analysis:**
  - Power analysis to determine required sample size for detecting effect sizes.
  - Justification of sample size for statistical significance.
- **Post-campaign Analysis:**
  - Comparison of average transaction amounts between control and test groups.
  - Visualization of distributions and daily averages.
  - Z-test for statistical significance of observed differences.
  - Test group outperformed control in ~71% of cases; statistical tests confirmed significance.

## 7. Key Insights & Outcomes
- **Customer Insights:**
  - Young customers (18-25) have lower income and credit history, and prefer non-credit card payment types.
  - Median income and age vary significantly by occupation.
- **Credit Insights:**
  - Strong correlation between credit score and credit limit (0.84), and between credit limit and outstanding debt (0.81).
  - Outliers and data errors in credit profiles were identified and corrected.
- **Transaction Insights:**
  - Electronics and Fashion are top product categories.
  - Outlier and zero-value transactions were systematically handled.
- **A/B Test Outcome:**
  - The marketing campaign for 18-25 year olds led to a statistically significant increase in average transaction amounts for the test group.

## 8. How to Run/Use the Notebooks
1. **Clone the repository** and ensure all datasets are in the correct `datasets/` folder.
2. **Open the notebooks:**
   - `Phase_01_atliq_bank.ipynb` for data cleaning and EDA.
   - `Phase_02.ipynb` for A/B testing and statistical analysis.
3. **Run all cells** in order. The notebooks are self-contained and include code, outputs, and visualizations.

## 9. Requirements
- Python 3.7+
- Jupyter Notebook or JupyterLab
- pandas
- numpy
- matplotlib
- seaborn
- scipy
- statsmodels

Install requirements with:
```bash
pip install pandas numpy matplotlib seaborn scipy statsmodels
```

---
**Author:** Chanupa Deshan Munassinghe

**Note:** This project is for educational and demonstration purposes only. All data is synthetic.
