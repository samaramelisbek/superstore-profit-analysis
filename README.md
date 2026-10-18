# Where Does Superstore Make and Lose Money?

**A profit analysis of 9,994 retail orders (2014–2017) using Python, pandas, and matplotlib.**

![Profit margin by discount level](images/margin_by_discount.png)

## The question
Superstore, a U.S. retailer of furniture, office supplies, and technology, earned **$2.30M in sales** but kept only **$286K in profit (12.5% margin)** over four years. I wanted to find out where the company makes money, where it loses money, and why.

## Key findings
1. **Discounts above 20% turn sales into losses.** Orders with no discount earn a **29.5% margin**, orders with 1–20% off still earn **11.9%**, but orders with 21–40% off lose money (**−15.3%**), and orders with more than 40% off lose **77 cents on every dollar sold**.
2. **Furniture sells well but barely makes money.** Furniture brought in $742K in sales, almost the same as Office Supplies, but its margin is only **2.5%** compared with about **17%** for Technology and Office Supplies. Two furniture sub-categories, **Tables (about −$17.7K)** and **Bookcases**, lose money overall, and so does Supplies in Office Supplies. Meanwhile, **Copiers** are the single most profitable sub-category.
3. **The Central region gives the biggest discounts and has the weakest margin.** Central's average discount is **24%**, about twice the West's 10.9%, and its margin is **7.9%**, about half of the West's 14.9%.

![Profit by sub-category](images/profit_by_subcategory.png)
![Average discount vs. margin by region](images/region_discount_vs_margin.png)

## Recommendations
- **Cap most discounts at 20%**, and require approval for anything higher.
- **Review Furniture pricing and shipping costs**, starting with Tables, the biggest loss-maker.
- **Look into Central's discount policy** and compare it with the West region, which earns the highest margin with the smallest discounts.

## Limitations
- These results show **patterns, not proof of cause.** With only four regions, other factors (such as product mix) could also explain the margin differences.
- The dataset is a well-known **sample dataset**, so the findings show my analysis process rather than a real company's results.

## How I did it
1. **Checked the data:** no missing values and no duplicate rows; converted order dates to real dates.
2. **Summarized** sales, profit, and margin by category, sub-category, region, and discount level using `groupby` (like an Excel PivotTable).
3. **Grouped discounts** into levels with `pd.cut` to compare their margins.
4. **Visualized** the results with matplotlib and saved the charts.

## Tools
Python · pandas · matplotlib · Jupyter (VS Code)

## Files
- `analysis.ipynb`: the full analysis, with code, tables, and charts
- `Sample - Superstore.csv`: the dataset
- `images/`: charts used in this README

## Data source
Superstore Dataset, [Kaggle](https://www.kaggle.com/datasets/vivek468/superstore-dataset-final).

---
**Samara Melisbek kyzy** · Data Science & Business Management, Knox College · [LinkedIn](https://www.linkedin.com/in/samara-m1) · [GitHub](https://github.com/samaramelisbekdata)
