# NovaRetail Sales Analysis with SQL and Pandas

## Project overview

This is a data analytics portfolio project about a fictional electronics retailer. It uses SQL and Pandas to answer four business questions:

1. How are sales changing over time?
2. Which product categories drive sales and estimated margin?
3. Which sales channel is largest?
4. How concentrated is customer value?

The complete analysis is contained in one Jupyter notebook:

**[`NovaRetail_SQL_Pandas_Analysis.ipynb`](NovaRetail_SQL_Pandas_Analysis.ipynb)**

> All data is synthetic. NovaRetail is not a real company.

## Tools used

- **SQL with SQLite:** joins, CTEs, aggregations, `LAG`, `DENSE_RANK`, and `NTILE`
- **Pandas:** loading, cleaning, validation, reshaping, and chart creation
- **Jupyter Notebook:** combines the code, results, charts, and written recommendations

SQLite is included with Python, so you do not need to install or manage a database server.

## Dataset

The project uses four related CSV files:

| File | Rows | Description |
|---|---:|---|
| `customers.csv` | 4,000 | Customer region, loyalty tier, and acquisition channel |
| `orders.csv` | 12,125 | Order date, customer, channel, and status |
| `order_items.csv` | 21,270 | Products, quantities, prices, and discounts |
| `products.csv` | 180 | Product category, brand, list price, and cost |

The data covers January 2023 through December 2025 and includes seasonal holiday peaks, channel growth, discounts, different product margins, and repeat customers.

## Main findings

- Net sales increased from **$2.05M in 2023 to $2.56M in 2025**, a 25.2% increase.
- Laptops and phones generated **62.9% of total sales**.
- Online was the largest channel, producing **48.8% of total sales**.
- The highest-spending customer quartile generated **56.2% of sales**.
- Smaller categories such as Accessories had less revenue but higher estimated product-margin percentages.

## Recommendation

NovaRetail should test a loyalty offer that bundles accessories with laptop or phone purchases for high-value online customers. This builds on the company's strongest channel, protects valuable customers, and adds higher-margin products to core-device purchases.

## Example charts

### Monthly sales

![Monthly sales](figures/monthly_sales.png)

### Category sales

![Category sales](figures/category_sales.png)

### Channel sales

![Channel sales](figures/channel_sales.png)

### Customer spending concentration

![Customer quartiles](figures/customer_quartiles.png)

## Project structure

```text
novaretail-sql-pandas-starter/
├── data/
│   ├── customers.csv
│   ├── orders.csv
│   ├── order_items.csv
│   └── products.csv
├── figures/
│   ├── monthly_sales.png
│   ├── category_sales.png
│   ├── channel_sales.png
│   └── customer_quartiles.png
├── docs/
│   └── GITHUB_INSTRUCTIONS.md
├── NovaRetail_SQL_Pandas_Analysis.ipynb
├── README.md
└── requirements.txt
```

## How to run the notebook

### Option 1: Anaconda

1. Install [Anaconda](https://www.anaconda.com/download).
2. Download or clone this repository.
3. Open Anaconda Navigator and launch Jupyter Notebook.
4. Browse to the project folder.
5. Open `NovaRetail_SQL_Pandas_Analysis.ipynb`.
6. Select **Kernel → Restart & Run All**.

### Option 2: Python and pip

Open a terminal in the project folder and run:

```bash
python -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
jupyter notebook
```

On Windows, activate the environment with:

```powershell
.venv\Scripts\activate
```

Then open the notebook and select **Kernel → Restart & Run All**.

## SQL skills demonstrated

The notebook contains four readable SQL analyses:

- Monthly sales trend using a **CTE**, `GROUP BY`, and `LAG`
- Category performance using multiple **JOINs** and `DENSE_RANK`
- Channel performance using joins and aggregations
- Customer spending quartiles using a CTE and `NTILE`

## Limitations

- The dataset is synthetic and should not be presented as real company data.
- Estimated product margin excludes shipping, labor, payment fees, and fixed costs.
- The findings show business patterns but do not prove that one factor caused another.

## What I learned

This project demonstrates how to connect multiple datasets, clean common data-quality issues, answer business questions with SQL, validate calculations with Pandas, create readable charts, and translate results into a recommendation.

For step-by-step publishing instructions, see [How to put this project on GitHub](docs/GITHUB_INSTRUCTIONS.md).

