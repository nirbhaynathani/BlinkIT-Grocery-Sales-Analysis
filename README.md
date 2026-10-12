# BlinkIT Grocery Sales Analysis

**Project brief:** Sapphire IQ — BlinkIT Grocery Sales Analysis  
**Domain:** Retail & Grocery Sales Analytics  
**Tools:** Python, Pandas, NumPy, Matplotlib, Seaborn, Jupyter Notebook

## Project objective
Turn the supplied BlinkIT grocery dataset into understandable business insights about product and category performance, outlet performance and location, recorded sales, ratings, data quality, and practical recommendations.

## Dataset
- Raw records: **8,523**
- Columns: **12**
- Distinct item identifiers: **1,559**
- Distinct outlet identifiers: **10**
- Missing item weights in the raw file: **1,463**
- Exact duplicate rows in the raw file: **0**

The workbook has the columns `Item Fat Content`, `Item Identifier`, `Item Type`, `Outlet Establishment Year`, `Outlet Identifier`, `Outlet Location Type`, `Outlet Size`, `Outlet Type`, `Item Visibility`, `Item Weight`, `Sales`, and `Rating`.

## Project structure
```text
BlinkIT_Grocery_Sales_Analysis_Project/
├── BlinkIT_Grocery_Sales_Analysis.ipynb
├── README.md
├── requirements.txt
├── data/
│   ├── blinkit_grocery_raw.csv
│   └── blinkit_grocery_cleaned.csv
└── outputs/
    ├── executive_summary.csv
    ├── charts/
    └── analysis tables (created when the notebook is run)
```

## How to run
1. Install Python 3.10+.
2. In a terminal, navigate to this project folder.
3. Install packages: `pip install -r requirements.txt`
4. Start Jupyter: `jupyter notebook`
5. Open `BlinkIT_Grocery_Sales_Analysis.ipynb` and run all cells from top to bottom.

The notebook expects the `data/` folder to remain beside it.

## Objectives covered from the supplied PDF
1. **Understand the business and its sales performance** — product types, outlets and locations, total recorded sales, ratings and product performance.
2. **Make sure the available information is reliable** — missing values, duplicates, unusual numeric values, consistent labels.
3. **Find out what is driving better sales performance** — category/outlet comparisons and descriptive associations between visibility, weight, ratings and sales.
4. **Help management make better business decisions** — contributor comparisons, improvement areas and practical recommendations.

## Initial findings
- Total recorded sales: **1,201,681.49** (the workbook does not explicitly state a currency unit).
- Highest category by total recorded sales: **Fruits and Vegetables**.
- Highest outlet type by total recorded sales: **Supermarket Type1**.
- Highest location tier by total recorded sales: **Tier 3**.
- Mean rating: **3.97**.
- Item Weight has **1,463** missing values in the raw dataset. The cleaning workflow imputes by item identifier median, then item type median, and keeps the raw file unchanged.

## Data limitations and responsible interpretation
The workbook does not contain transaction dates, quantity, profit, order status, payment method, or customer identifiers. Consequently, this project does not claim to analyze time-based growth, profit, order cancellations, or customer behavior. Outlet establishment year is a characteristic of the outlet, not a sales transaction date. Correlations are descriptive and do not establish causation. IQR outlier flags should be reviewed, not automatically deleted.

## Files
- `data/blinkit_grocery_raw.csv` — faithful CSV copy of the original worksheet.
- `data/blinkit_grocery_cleaned.csv` — cleaned labels and imputed item weights for analysis.
- `outputs/executive_summary.csv` — headline metrics.
- `outputs/charts/` — static charts generated from the supplied dataset.
