# 🧾 Superstore Cleaning Log

This document tracks the changes and cleaning iterations made on the Superstore dataset.  
Each version documents what was modified, added, or corrected for data integrity and analysis readiness.

## 🧹 Version: superstore_clean_extract_v1.xlsx  
**Date:** October 8, 2025  
**Purpose:** Cleaned extract for pivot preparation in Study Dashboard Block 3  

### Changes Made
- Split `Customer Name` into `First Name` and `Last Name`
- Applied `PROPER()` to text columns (City, Category, Segment)
- Converted text-formatted numbers (`Sales`, `Quantity`) to numeric types
- Standardized date format → `yyyy-mm-dd`
- Added `Clean_Status` column to flag invalid or incomplete rows
- Verified `Order ID` groups instead of removing duplicates

### Key Learnings
- Order IDs are not unique — represent grouped transactions
- Text-to-Columns + PROPER() combo ensures cleaner naming consistency
- Using `ISNUMBER()` helped catch hidden text-number errors

### Next Steps
- Use this cleaned version in upcoming pivot-building phase
- Explore automation of clean-check formulas in future iterations