# 📂 data/raw — Dataset Instructions

## Dataset: Sample Superstore Sales

This project uses the **Sample Superstore** dataset — one of the most widely used retail analytics datasets for learning and portfolio projects.

---

## How to Download

### Option A: Kaggle (recommended)

1. Create a free account at [kaggle.com](https://www.kaggle.com)
2. Visit: [https://www.kaggle.com/datasets/vivek468/superstore-dataset-final](https://www.kaggle.com/datasets/vivek468/superstore-dataset-final)
3. Click **Download** → extract the ZIP
4. Place `Sample - Superstore.csv` in this folder (`data/raw/`)

### Option B: Kaggle CLI

```bash
pip install kaggle
kaggle datasets download -d vivek468/superstore-dataset-final
unzip superstore-dataset-final.zip -d data/raw/
```

---

## Dataset Details

| Property | Value |
|---|---|
| **Rows** | 9,994 transactions |
| **Columns** | 21 (Order ID, Date, Customer, Category, Sales, Quantity, Discount, Profit…) |
| **Date range** | January 2015 – December 2018 |
| **Categories** | Furniture, Office Supplies, Technology |
| **Regions** | West, East, Central, South |
| **File size** | ~2.5 MB |
| **Format** | CSV (latin-1 encoding) |
| **License** | Public / Educational use |

---

## How to Use the Real File

Once downloaded, open `notebooks/sales_forecasting.ipynb` and replace the synthetic data generator in **Section B** with:

```python
# Replace the generate_superstore_data() call with:
df_raw = pd.read_csv('../data/raw/Sample - Superstore.csv', encoding='latin-1')

# The real dataset uses 'Order Date' as a string — parse it:
df_raw['Order Date'] = pd.to_datetime(df_raw['Order Date'])

# Select only the columns this project uses:
df_raw = df_raw[['Order Date', 'Category', 'Region', 'Segment',
                  'Sales', 'Quantity', 'Discount', 'Profit']]
```

Everything else in the notebook works unchanged.

---

## Why This Dataset?

- **Real business structure** — actual retail transactions, not toy data
- **Temporal range** — 4 full years of data enables proper seasonality analysis
- **Multiple dimensions** — product category, region, customer segment
- **Industry standard** — used in Tableau, Power BI, and ML tutorials worldwide
- **Appropriate complexity** — beginner-friendly but rich enough for portfolio-level work

---

> **Note:** The synthetic generator in the notebook mirrors this dataset's statistical properties (lognormal sales distribution, seasonal multipliers, category proportions). Results will be very similar whether you use the synthetic data or the real CSV.
