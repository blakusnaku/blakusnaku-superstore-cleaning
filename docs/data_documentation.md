## Sept 30, 2025 – Data Cleaning
- Removed duplicates
- Standardized column headers
- Extracted unique values ( see [`data_documentation.xls`](./data_documentation.xls))
- Saved output as `superstore_cleaned.xlsx`

## Oct 1, 2025 - Handling MIssing Values and Pivot Setup
- Checked each column using Filter -> looked for "(Blank)"
- Result: No blanks found (`category`,`sub-category`,`sales`,etc.)
- Action: no imputation needed
- Reference log of column checks in [`data_documentation.xls`](./data_documentation.xls)
- Saved output as `superstore_cleaned_v2.xls`

## Oct 1, 2025 - Pivot Table (sales by Category)
- Created first Pivot table using `superstore_cleaned_v2.xls`
- Placed `category` in Rows and `sales` in Values
- Changed Values field to **Sum of Sales** (instead of Count)
- Renamed field to `Total Sales` for clarity
- Applied ₱ currency formatting with commas and 2 decimals
- Verified Grand Total - ₱2,2970,200.86 (mathes raw dataset sum)
- Outpit: Pivot Table saves in new worksheet

## Oct 1, 2025 - Pivot Report (Category + Sub-Category)
- Extended the pivot table by adding `sub_category` under `category`
- Applied currency formatting (₱, commas, 2 decimals) to all sales values
- Inserted a Pivot Chart (Clustered Column) to visualize sales by category and sub_category
- Added chart title "Sales by Category and Sub-Category"
- Addex axis titles:
	- X-axis - "Category / Sub-Category"
	- Y-axis - "Sales (₱)"
- Cleaned up chart by removing reduntdant legend
- Saved chart as a new sheet: `PivotReport_Category_SubCategory`

## Oct 2, 2025 - Block 1 : Find and Replace in Excel
- Practiced using Find and Replace (Ctrl+H) for quick cleanup
- Checked **Math entire cell contents** to avoid partial word replacements
- Applied the following replacements
	- `CA` - `California`
	- `TX` - `Texas`
	- `West` - `West`
- Verified replacement were correct and consistent across the dataset

## Oct 2, 2025 - Block 2 : Top 10 Products by sales
- Created a new Pivot Table to rank products by total sales
- Added `product_name` - Rows and `sales` - Values (SUM)
- Sorted sales in descending order
- Applied Top 10 filter  - Sum of sales
- Formatted values in ₱ currency
- Saved sheet as `top10_products_sales`

## Oct 2, 2025 - Block 3 : Generate Top 10 Product Reports (Excel - PDF)
- Opened Pivot Table sheet `top10_products_sales`
- Added title row **Top 10 Products by sales - Superstore Datasheet**
- Bolded headers (`Product Name`, `Total Sales`) and adjusted column widths
- Applied borders around the table; shaded Grand Total row
- Inserted footer note: *"Source: Superstore dataset (cleaned). Report generated via Excel Pivot Table, Oct 2, 2025."*
- Exported finalized sheet as PDF: `top10_products_report.pdf`
- Saved PDF in `/reports/` folder of GitHub repo

## Oct 3, 2025 - Block 1: Conditional formatting
- Applied conditional formatting in Excel to highlight top sales values greater than **₱1,000.**
- Ensured formatting rules applied only to numeric field (avoided applying to headers or text)
- Verified results visually by spot-checking high-value Rows

## Oct 3, 2025 - Block 2: Basic Charts
- Built **bar chart (Sales by Category)** using pivot table summary.
- Built **line chart (Quarterly Sales Trend 2014-2017):
	- Encountered issue grouping dates - Excel threw "Cannot group section."
	- Troubleshoot by scanning for blanks in the dataset;
		- Found that although cells appeared filled, Excel still detected blanks due to trailing rows (~55k).
		- **Fix:** Cleared excess rows beyond row 9995, then grouping worked.
	- Final grouping set to **Quarterly** for readability.
- Formatted charts:
	- Simplied data labels
	- Adjusted chart spacing and interval display for clarity

## Oct 3 2025 - Block 3: Mini Dashboard
- Designed a **Sales Dashboard (2014-2017)** on a single sheet.
- Layout:
	- Top-left: Bar chart (Sales by Category)
	- Top-right: Line chart (Quarterly Sales Trend 2014–2017)
	- Bottom-left: Pivot Table (Sales by Category)
	- Bottom-right: Pivot Table (Quarterly Sales with drilldown by year)
- Formatting improvements:
	- Added y-axis labels for clarity.
	- Cleaned up pivot table formatting (currency ₱, alignment).
	- Dashboard arranged to fit on a single landscape PDF page.
- Final Output: Ready as a presentation-ready dashboard for reporting.