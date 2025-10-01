# Superstore Data Cleaning & Analysis

This is my practice project in Excel for data cleaning and basic analysis using the **Superstore** dataset. I’m documenting each step as I go.

So far, I’ve done two phases:
1. **Cleaning the dataset** – making it usable and consistent  
2. **Pivot analysis** – exploring sales patterns with Pivot Tables & Charts  

---

## Project Files

```
data-cleaning-superstore/
│
├── data/
│   ├── superstore_raw.xls              # raw dataset
│   ├── superstore_cleaned_v1.xls       # after initial cleaning
│   ├── superstore_cleaned_v2.xls       # after nulls + pivots
│
├── reports/
│   ├── sales_by_category.xls           # pivot: sales by category
│   ├── pivot_cat_subcat.xls            # pivot + chart
│   ├── screenshots/
│       ├── sales_by_category.png
│       ├── pivot_cat_subcat.png
│
├── docs/
│   ├── data_documentation.xls          # structured audit log
│   ├── data_documentation.md           # narrative log

```

---

## Phase 1: Cleaning
- Renamed column headers (lowercase, underscores)  
- Trimmed text fields (removed hidden spaces)  
- Removed duplicates (`order_id`)  
- Standardized date formats (YYYY-MM-DD)  
- Checked/validated numeric columns (`sales`, `discount`, `profit`)  
- Verified unique values for states, cities, categories  
- Checked for missing/null values → none found  

**Output:** `data/superstore_cleaned_v1.xls`  

---

## Phase 2: Pivot Analysis
- Built a Pivot Table for **Sales by Category**  
- Added **Sub-Category** breakdown  
- Applied currency formatting (₱)  
- Created a clustered column chart for visualization  
- Saved a separate sheet for the report  

**Output:** `data/superstore_cleaned_v2.xls` with sheets:  
- `sales_by_category` (pivot table)  
- `pivot_cat_subcat` (pivot chart)  

---

## Documentation
- **Excel log:** [`docs/data_documentation.xlsx`](./docs/data_documentation.xlsx) – technical checks (unique values, nulls, etc.)  
- **Markdown log:** [`docs/data_documentation.md`](./docs/data_documentation.md) – daily notes and what I learned  

---

## Next Steps
- More pivot practice (sales by region, profit by segment, etc.)  
- Try dashboards in Excel / Google Data Studio  
- Summarize insights and write a short reflection  

---

## Example Chart
**Sales by Category and Sub-Category**

![Pivot Chart](./reports/screenshots/pivot_cat_subcat.png)
