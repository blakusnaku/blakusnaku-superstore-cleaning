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