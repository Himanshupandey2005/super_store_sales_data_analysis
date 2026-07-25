# 🛒 Superstore Sales Analysis

A complete SQL + Python data analysis project on 4 years (2015–2018) of retail transaction data, uncovering sales trends, top-performing customers/products, and regional performance gaps to support data-driven business decisions.

---

## 📌 Business Problem

A retail superstore wants to understand:
- Which products, categories, and regions are driving the most (and least) revenue?
- Who are the most valuable customers?
- Are there seasonal patterns in sales that the business should plan around?
- How is the business trending year-over-year?

This project answers these questions using SQL for structured business queries and Python (Pandas/Matplotlib/Seaborn) for exploratory data analysis and visualization.

---

## 📊 Dataset

- **Source:** Superstore Sales dataset (`train.csv`)
- **Size:** 9,800 transaction rows | 4,922 unique orders | 793 unique customers
- **Time Range:** 2015 – 2018
- **Columns:** Order details, Customer info, Product info, Sales, Shipping info, Location (State/City/Region)

The raw CSV was normalized into a **relational schema (4 tables)** for SQL-based analysis:

| Table | Description |
|---|---|
| `customers` | Customer ID, Name, Segment, Country |
| `orders` | Order ID, Order/Ship Date, Ship Mode, Customer ID, City, State, Postal Code, Region |
| `products` | Product ID, Category, Sub-Category, Product Name |
| `order_details` | Row ID, Order ID, Product ID, Sales |

> **Design note:** State/City/Region were intentionally placed in the `orders` table (not `customers`), since shipping location is an order-level attribute — a single customer can ship to multiple states across different orders.

---

## 🛠️ Tools & Tech Stack

- **Python** — Pandas, Matplotlib, Seaborn
- **SQL** — SQLite (via `sqlite3` + `pandas.read_sql`)
- **Jupyter Notebook** — analysis and visualization

---

## 🔑 Key Insights

- **Revenue concentration:** California and New York alone contribute ~33% of total sales.
- **Top category:** Technology leads with $827K in sales, driven mainly by Phones ($327K).
- **Top customer:** Sean Miller generated $25,043 in lifetime sales.
- **Shipping preference:** Standard Class accounts for ~59% of all sales — customers strongly prefer cost-effective delivery over speed.
- **Seasonality:** Sales consistently peak in Sep–Dec (holiday season) and dip in Jan–Feb every year.
- **Year-over-year growth:** Total sales grew from $479K (2015) to $722K (2018).
- **Underperforming states:** North Dakota, West Virginia, and Maine show minimal sales — potential opportunity or weak market reach.

---

## 📈 Sample Visualizations

- Monthly sales trend (2015–2018)
- Category & Sub-Category-wise sales breakdown
- Sales distribution & outlier detection
- State-wise performance comparison

*(See `/notebooks/index.ipynb` for full charts)*

---

## 🚀 How to Run

```bash
# 1. Clone the repo
git clone https://github.com/Himanshupandey2005/super_store_sales_data_analysis.git
cd super_store_sales_data_analysis

# 2. Install dependencies
pip install -r requirements.txt

# 3. Open the notebook
jupyter notebook notebooks/index.ipynb
```

---

## 📂 Project Structure

```
├── data/
│   ├── train.csv
│   ├── customers.csv
│   ├── orders.csv
│   ├── products.csv
│   ├── order_details.csv
│   └── superstore_sales_fixed.db
├── notebooks/
│   └── index.ipynb
├── README.md
└── requirements.txt
```

---

## 👤 Author

**Himanshu Pandey**