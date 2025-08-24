# Paycheck Protection Program (PPP) Loan Data Analysis  

This project analyzes **PPP loan distribution during the COVID-19 pandemic** using the U.S. Small Business Administration’s (SBA) publicly available data. While the PPP program provided vital relief to small businesses, controversy arose as larger firms also received significant loan amounts.  

The analysis focuses on:  
1. Loan distribution by **amount and industry**  
2. Normalizing loan distribution by **jobs supported (payroll costs)**  
3. Identifying differences in **loan amounts by gender**  
4. Comparing **PPP loans to women-owned businesses** vs. their share in the U.S. economy  

---

## 📊 Research Background & Goals  

During the pandemic, PPP loans were intended to help small businesses keep their doors open. This analysis seeks to answer:  

- What is the breakdown of loans by **loan amount and industry**?  
- How much relief went to businesses with **larger payrolls** vs. smaller payrolls?  
- Are there **gender disparities** in PPP loan distribution?  

Findings from this study can help policymakers understand inequities and recommend improvements for future relief programs.  

---

## 📂 Data Overview  

- **Source**: U.S. Small Business Administration ([sba.gov](https://www.sba.gov))  
- **Files**: 9 CSVs (≈ **3 GB**, ~**7.34 million rows**)  
- **Columns**: 51, including loan amount, borrower demographics, industry (NAICS), and jobs reported  
- **Tools Used**:  
  - **Python** (Pandas, NumPy, SciPy, Seaborn, Matplotlib, Statsmodels)  
  - **Google Colab** (for scalable analysis)  
- **Data Wrangling**:  
  - Merged 9 CSVs into one DataFrame  
  - Cleaned unnecessary columns, handled missing values  
  - Joined NAICS industry codes for readability  

---

## 🔍 Key Insights  

### Loan Distribution  
- **82%** of loans were for amounts < **$100K**  
- Only **1.4%** of loans were > **$1M**, but those accounted for **30.7% of total loan volume**  

### Payroll Normalization  
- PPP loans were designed to cover 2.5 months of payroll (capped at $100K/employee)  
- Analysis revealed:  
  - **9% of loans** supported payroll > **$100K per job**  
  - **17.5K loans (~$5.1B)** supported payroll > **$200K per job**  

### Gender Disparities  
- Median loan amounts were significantly **higher for male-owned businesses** than female-owned businesses  
- Ratio of male to female median loan amount: **~1.55x overall**  
- Disparities persisted even after adjusting for company size:  
  - Small businesses: **1.31x** higher for men  
  - Medium businesses: **1.50x** higher for men  
  - Large businesses: **1.30x** higher for men  

### Women-Owned Businesses  
- Only **28% of PPP loans** went to women-owned businesses, while women own **37% of U.S. businesses**  
- Statistically significant underrepresentation (p < 0.01)  
- Caveat: 68% of borrowers did not disclose gender, which may bias results  

---

## 📈 Visualizations  

The analysis includes:  
- **Pie charts** for loan count & volume distribution by loan size  
- **Pie charts** for loan amount per job supported (payroll buckets)  
- **Bar charts** for loan distribution by industry  
- **Box plots** comparing loan amounts by gender & company size  

---

## 🧪 Hypothesis Testing  

- **t-tests** were conducted to compare mean loan amounts by gender  
- **z-test** performed to compare % of women-owned PPP loans vs. U.S. baseline (37%)  
- Results showed statistically significant disparities in both loan amounts and representation  

---

## 📌 Findings & Recommendations  

**Findings**  
- Large loans (> $1M) disproportionately represented loan **volume**  
- Loans exceeded **intended payroll caps** ($100K/employee)  
- Women-owned businesses received significantly **smaller loans** and **fewer loans**  

**Recommendations**  
- Enforce a stricter **$100K/employee cap** on PPP loans  
- Audit outlier loans (> $200K/employee) for misuse or errors  
- Investigate reasons for **gender loan disparities**  
- Increase **outreach & education** for women-owned businesses in future relief programs  

---

## 🚀 How to Run  

1. Clone this repo  
   ```bash
   git clone https://github.com/yourusername/ppp-loan-analysis.git
   cd ppp-loan-analysis
