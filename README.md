# Superstore Sales Analysis: Regional and Discount Impact on Profitability

## Overview
This project analyzes a large retail dataset (~51,000 rows) from a global superstore. The goal is to explore **sales, profit, and discount patterns**, identify regions or categories where profitability is at risk, and quantify the impact of discounting on profit margins using Python and Excel.

The analysis focuses on:

- Regional profitability
- Category and discount sensitivity
- Revenue vs. profit mismatches
- Quantifying discount impact using linear regression

---

## Dataset
- 51,290 rows and 26 columns
- Key columns: `Category`, `Region`, `Discount`, `Sales`, `Profit`, `Profit_Margin`
- No missing values
- Source: fictional superstore dataset from Kaggle for educational purposes (can be replaced with real data)

---

## Tools and Libraries
- **Python:** pandas, numpy, matplotlib, seaborn, scikit-learn
- **Excel:** initial data exploration and cleaning
- **Jupyter Notebook:** visualization and analysis

---

## Analysis Steps

1. **Data Exploration**
   - Checked data types, non-null counts, summary statistics
   - Calculated `Profit_Margin = Profit / Sales`

2. **Category Analysis**
   - Calculated average profit margins by `Category`
   - Grouped by discount bins to show sensitivity:
     - Furniture, Technology, and Office Supplies all show **steep margin decline at high discounts**

3. **Regional Analysis**
   - Aggregated sales and profit by `Region`
   - Identified **Southeast Asia** as the lowest-performing region:
     - Sales: ~884k  
     - Profit Margin: 2%
   - Root cause analysis revealed **average discount of 27%**, the highest among all regions, as the primary driver

4. **Regression Analysis**
   - Built a **linear regression model** predicting `Profit_Margin` from `Discount`
   - Results:
     - Coefficient: -1.858 → every 10% increase in discount reduces margin by ~18 percentage points
     - R² = 0.717 → discount explains 71% of variation in profit margin
   - Visualizations show clear negative correlation between discount and margin

5. **Visualizations**
   - Scatterplots and line plots by region and category
   - Heatmaps of profit margins across categories and discount bins
   - Regression line overlay demonstrating impact of discount

---

## Key Insights

- **Discounting heavily affects profitability:** high discounts (30%+) can turn profitable products into losses
- **Southeast Asia is the most at-risk region** due to aggressive discounting
- **Furniture is the most discount-sensitive category**
- **Linear regression quantifies the effect:** 10% higher discount → ~18% lower profit margin

---

## Next Steps / Recommendations

- Limit discounts >30% for high-risk categories like Furniture
- Investigate regional pricing strategy for Southeast Asia
- Explore additional factors affecting margins (shipping costs, product mix, customer segments)
- Extend analysis with predictive models for category-level profit optimization
