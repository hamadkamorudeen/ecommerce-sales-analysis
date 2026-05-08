# E-Commerce Sales Analysis — UK Online Retail (2010–2011)

![Python](https://img.shields.io/badge/Python-3.x-blue?logo=python&logoColor=white)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-orange?logo=jupyter&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-Data%20Analysis-150458?logo=pandas&logoColor=white)
![Matplotlib](https://img.shields.io/badge/Matplotlib-Visualization-11557c)
![Status](https://img.shields.io/badge/Status-Complete-brightgreen)

## Project Overview

This project is an end-to-end Exploratory Data Analysis (EDA) of a real-world e-commerce dataset from a UK-based online retailer. The dataset covers all transactions between December 2010 and December 2011 and was sourced from the [UCI Machine Learning Repository via Kaggle](https://www.kaggle.com/datasets/carrie1/ecommerce-data).

The analysis covers data cleaning, distribution exploration, sales trend analysis, customer segmentation by spending, and product performance — all structured around eight business questions.

---

## Dataset Summary

| Property | Value |
|---|---|
| Source | UCI Machine Learning Repository |
| Time Period | December 2010 – December 2011 |
| Raw Rows | 541,909 |
| Clean Rows (after cleaning) | 392,692 |
| Unique Customers | 4,338 |
| Unique Products | 3,877 |
| Countries | 37 |
| Total Revenue Generated | £8,887,208.89 |

---

## Business Questions Answered

1. What is the total revenue generated?
2. Which products generate the most revenue?
3. Which products are sold the most by quantity?
4. Which products generate low sales or appear rarely?
5. Who are the top customers based on total spending?
6. What are the sales trends over time (daily and monthly)?
7. Which locations generate the highest sales?
8. Are there any unusual transactions (very high quantity or price)?

---

## Key Findings

- **Total revenue** across the clean dataset was **£8,887,208.89**
- **PAPER CRAFT, LITTLE BIRDIE** was the top-performing product by both revenue and quantity sold
- **United Kingdom** accounted for the vast majority of all revenue across 37 countries
- Revenue showed a clear **Q4 spike (October–November)**, consistent with holiday gift buying — the retailer primarily sells occasion gifts
- **25% of raw transactions** had no CustomerID, pointing to guest checkouts or data collection gaps
- A small number of **high-volume wholesale orders** heavily skew the quantity distribution
- The **top 10 customers** generate a disproportionately high share of revenue, consistent with a B2B wholesale business model

---

## Data Cleaning Steps

| Step | Rows Removed | Rows Remaining |
|---|---|---|
| Raw dataset | — | 541,909 |
| Remove duplicates | 5,268 | 536,641 |
| Remove blank CustomerID | 135,037 | 401,604 |
| Remove negative Quantity | 10,624 | 390,980 |
| Remove invalid UnitPrice | 2,517 | 392,692 (after dedup overlap) |

---

## Project Structure

```
ecommerce-analysis/
│
├── data/
│   └── data.csv                        # Raw dataset (download from Kaggle)
│
├── ecommerce_task1_analysis.ipynb      # Main analysis notebook
│
├── charts/
│   ├── chart_distributions.png
│   ├── chart_monthly_frequency.png
│   ├── chart_top_revenue_products.png
│   ├── chart_top_qty_products.png
│   ├── chart_top_customers.png
│   ├── chart_sales_trends.png
│   └── chart_revenue_by_country.png
│
└── README.md
```

---

## How to Run This Project

**Step 1 — Clone the repository**
```bash
git clone https://github.com/YOUR-USERNAME/ecommerce-analysis.git
cd ecommerce-analysis
```

**Step 2 — Install required libraries**
```bash
pip install pandas matplotlib jupyter
```

**Step 3 — Download the dataset**

Go to [this Kaggle link](https://www.kaggle.com/datasets/carrie1/ecommerce-data), download `data.csv`, and place it inside the `data/` folder.

**Step 4 — Open the notebook**
```bash
jupyter notebook ecommerce_task1_analysis.ipynb
```

**Step 5 — Run all cells**

In Jupyter, go to **Kernel → Restart & Run All**. All charts will generate automatically.

---

## Tools Used

- **Python 3** — core programming language
- **Pandas** — data loading, cleaning, and aggregation
- **Matplotlib** — all charts and visualizations
- **Jupyter Notebook** — interactive analysis environment

---

## Charts Preview

> All charts are saved automatically as PNG files when you run the notebook.

| Chart | What it Shows |
|---|---|
| Quantity & Price Distributions | How orders and prices are spread across the dataset |
| Monthly Purchase Frequency | Number of invoices raised per month |
| Top 10 Products by Revenue | Highest-earning products |
| Top 10 Products by Quantity | Most units sold |
| Top 10 Customers by Spending | Highest-value customers |
| Monthly & Daily Revenue Trends | How revenue moved over the full year |
| Revenue by Country (Top 15) | Geographic breakdown of sales |

---

## Data Source

Chen, D. (2015). *Online Retail* [Dataset]. UCI Machine Learning Repository.  
Available via Kaggle: https://www.kaggle.com/datasets/carrie1/ecommerce-data

---

## Author

**Hamad**  
Actuarial Science Student | Data Analytics Enthusiast  
[LinkedIn](https://linkedin.com/in/YOUR-LINKEDIN) · [GitHub](https://github.com/YOUR-USERNAME)
