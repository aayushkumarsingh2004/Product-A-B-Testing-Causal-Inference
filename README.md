# Product A/B Testing & Causal Inference 📊

## Overview
This repository contains a rigorous A/B test analysis conducted on e-commerce user interaction data. The goal of this project was to evaluate the conversion impact of a new product feature (a redesigned landing page) and provide a verifiable, data-driven recommendation to product stakeholders.

## Tech Stack
* **Language:** Python
* **Libraries:** Pandas, SciPy, Statsmodels, NumPy
* **Environment:** Jupyter Notebook

## Methodology
The analysis was conducted following standard data science and causal inference protocols:
1. **Data Cleaning:** Processed an initial dataset of 294,478 user sessions, filtering out 3,893 corrupted rows and handling duplicate users to ensure data integrity.
2. **Experimental Validation:** Conducted a Chi-Square test for **Sample Ratio Mismatch (SRM)**. 
   * *Result:* p-value = 0.9468. 
   * *Conclusion:* The traffic split was statistically valid (roughly 50/50), confirming the experimental design was sound.
3. **Statistical Testing:** Calculated raw conversion rates and performed a **Proportions Z-Test** to determine if the observed differences were statistically significant.

## Key Findings
* **Control Group (Old Page):** 12.04% Conversion Rate
* **Treatment Group (New Page):** 11.88% Conversion Rate
* **Z-Test p-value:** 0.9051

## Business Recommendation
**DO NOT LAUNCH.** Because the calculated p-value (0.9051) is significantly higher than the standard alpha threshold of 0.05, we fail to reject the null hypothesis. There is no statistical evidence that the new landing page improves user conversion. 

**Strategic Action:** Retain the current "Old Page." Launching the new feature carries a risk of regressing our conversion rate without any proven benefit. It is recommended to investigate why the "New Page" failed to engage users through user interviews or heatmaps before attempting a fresh design iteration.
