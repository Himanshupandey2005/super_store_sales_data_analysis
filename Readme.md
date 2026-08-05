# 🛒 Superstore Sales Analysis

A complete SQL + Python data analysis project on 4 years (2015–2018) of retail transaction data, uncovering sales trends, customer purchasing behavior, product performance, and regional sales patterns to support data-driven business decisions.

---

## 📌 Business Problem

A retail superstore wants to understand:

- Which products, categories, and regions generate the highest and lowest sales?
- Who are the most valuable customers based on sales?
- Are there seasonal patterns in customer purchases?
- How have sales changed year over year?
- Which shipping modes and regions contribute the most to overall sales?

This project answers these questions using **SQL** for business queries and **Python (Pandas, Matplotlib, Seaborn, Plotly)** for exploratory data analysis and visualization.

---

## 📊 Dataset

- **Source:** Superstore Sales dataset (`train.csv`)
- **Size:** 9,800 transaction rows | 4,922 unique orders | 793 unique customers
- **Time Range:** 2015–2018
- **Columns:** Order details, Customer information, Product information, Sales, Shipping information, and Location (State, City, Region)

The raw CSV was normalized into a relational database consisting of four tables and loaded into **superstore_sales_fixed.db** for SQL-based analysis.

| Table | Description |
|--------|-------------|
| customers.csv | Customer ID, Customer Name, Segment, Country |
| orders.csv | Order ID, Order Date, Ship Date, Ship Mode, Customer ID, City, State, Postal Code, Region |
| products.csv | Product ID, Category, Sub-Category, Product Name |
| order_details.csv | Row ID, Order ID, Product ID, Sales |

> **Design Note:** State, City, and Region were intentionally stored in `orders.csv` instead of `customers.csv` because shipping location is an order-level attribute. A customer may place multiple orders shipped to different locations.

---

## 🛠️ Tools & Tech Stack

- **Python**
  - Pandas
  - Matplotlib
  - Seaborn
  - Plotly
- **SQL**
  - SQLite (`sqlite3`, `pandas.read_sql`)
- **Jupyter Notebook**

---

## 🔑 Key Insights

- California and New York together contribute nearly **33% of total sales**, making them the strongest-performing states.
- **Technology** is the highest-selling category with approximately **$827K** in sales.
- **Phones** are the best-performing sub-category, generating around **$327K** in sales.
- **Sean Miller** is the highest-value customer, contributing **$25,043** in total sales.
- **Standard Class** is the most frequently used shipping mode, accounting for approximately **59% of total sales**.
- Sales consistently peak during **September–December**, indicating strong holiday-season demand.
- Sales are generally lowest during **January–February**, suggesting seasonal fluctuations.
- Total annual sales increased from approximately **$479K in 2015** to **$722K in 2018**, showing steady year-over-year growth.
- **RFM Analysis** identified High-Value Loyal customers as approximately **25.6% of the customer base**, contributing around **42% of total sales**. At-Risk customers still represent over **$256K in sales**, highlighting opportunities for customer retention.
- **North Dakota, West Virginia, and Maine** recorded the lowest sales during the analysis period.

> **Note:** This dataset does **not** include a **Profit** column. Therefore, all analyses and insights are based on **Sales**, customer behavior, product performance, shipping preferences, and regional sales trends.

---

## 📈 Sample Visualizations

- Month-over-Month Sales Trend
- Sales by Category
- Sales by Sub-Category
- Sales by State
- Sales by Region
- Customer Segmentation (RFM)
- Customer Cohort Retention
- Top Customers
- Shipping Mode Distribution

See **index.ipynb** for the complete analysis and visualizations.

---

## 🚀 How to Run

```bash
# Clone the repository
git clone https://github.com/Himanshupandey2005/super_store_sales_data_analysis.git

# Navigate into the project
cd super_store_sales_data_analysis

# Install dependencies
pip install -r requirements.txt

# Launch Jupyter Notebook
jupyter notebook index.ipynb
```

---

## 📂 Project Structure

```
├── train.csv
├── Divided_data/
│   ├── customers.csv
│   ├── orders.csv
│   ├── products.csv
│   └── order_details.csv
├── superstore_sales_fixed.db
├── charts/
├── index.ipynb
├── requirements.txt
└── README.md
```

---

## 👤 Author

**Himanshu Pandey**

- Passionate about **Data Analytics**, **SQL**, and **Python**
- Interested in transforming raw business data into meaningful insights through data visualization and exploratory analysis.
