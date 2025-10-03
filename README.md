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
│   ├── superstore_cleaned_v1.xls       # after cleaning only
│   ├── superstore_cleaned_v2.xls       # after cleaning + pivots
│
├── reports/
│   ├── sales_by_category.xls           # pivot: sales by category
│   ├── pivot_cat_subcat.xls            # pivot + chart
|   ├── top10_products_report.pdf       # one-page PDF report: top 10 products by sales
|   ├── sales_dashboard_2014_2017.xlsx  # consolidated dashboard (charts + pivots)
│   ├── screenshots/
│       ├── sales_by_category.png
│       ├── pivot_cat_subcat.png
│
├── excel_dashboards/
|   ├── superstore_dashboard.xlsx       # final output for superstore
|   ├── week1_summary.md                # learning reflection for week 1
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

## Phase 3: Report Generation
- Converted pivot analysis into a structured, presentation-ready report.
- Produced a Top 10 Products by Sales PDF with clear titles, styled headers, currency formatting, and source notes.

**Output:** `top10_products_report.pdf` (one-page PDF report stored in `/reports/`)

---

## Phase 4: Dashboard Creation
- Built a **Sales Dashboard (2014–2017)** combining bar + line charts with supporting pivot tables.
- Visualized sales by category and quarterly sales trends in one consolidated view.
- Dashboard designed to be **print-friendly** and presentation-ready.

**Output:** `sales_dashboard_2014_2017.xlsx` (stored in `/reports/`)

---

## Documentation
- **Excel log:** [`docs/data_documentation.xlsx`](./docs/data_documentation.xlsx) – technical checks (unique values, nulls, etc.)  
- **Markdown log:** [`docs/data_documentation.md`](./docs/data_documentation.md) – daily notes and what I learned  

---
## Superstore Dashboard (Excel Practice)##
This project is part of my Excel learning journey (Week 1), where I practiced creating dashboards using pivot tables, charts, and KPIs. The dataset used is the Sample Superstore dataset, a classic retail sales dataset for data visualization practice.

**Dashboard Overview**
The dashboard highlights:
- Total Sales, Profit, Orders, and Average Profit Margin (KPIs)
- Sales by Category – total sales across Furniture, Office Supplies, and Technology
- Profit by Sub-Category – diverging chart showing profit vs loss items
- Sales by Region – contribution of each region (Central, East, South, West)
- Quantity by Ship Mode – order volumes by shipping type

**Skills Practiced**
- Pivot Table creation and formatting
- Calculated fields (Profit Margin %)
- Multi-chart dashboard layout (2×2 grid)
- KPI card design
- Consistent use of professional color palettes (blue/orange/green/red)
- Data cleaning & number formatting

**Output:** `superstore_dashboard.xlsx` (stored in `/reports/`)
