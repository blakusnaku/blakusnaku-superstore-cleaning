# 🧹 Superstore Data Cleaning Project

## 📌 Project Overview  
This project demonstrates a **step-by-step data cleaning workflow** applied to the popular *Superstore* dataset. The goal is to transform the raw data into a clean, analysis-ready version, while documenting every step for transparency and reproducibility.  

---

## 📂 Files in This Repo
- **`superstore_raw.xls`** → Original dataset (uncleaned).  
- **`superstore_cleaned.xls`** → Fully cleaned dataset after Block 4.  
- **`data_documentation.xls`** → Detailed log of all cleaning steps (Block 1–4).  

---

## 🛠 Cleaning Workflow
The cleaning process was structured into **4 Blocks**, with each committed separately to GitHub for version control.

### 🔹 Block 1: Column & Text Cleanup
- Renamed headers to lowercase + underscores  
- Trimmed text fields (`TRIM`)  
- Checked missing values (`COUNTBLANK`)  
- Standardized date formats to `YYYY-MM-DD`

### 🔹 Block 2: Duplicate Validation
- Verified `row_id` uniqueness  
- Confirmed `order_id` repetition expected (across multiple products)  

### 🔹 Block 3: Data Types & Numeric Standards
- Converted IDs and postal codes to **Text**  
- Standardized numeric fields:  
  - `sales`, `profit`, `discount` → 2 decimals  
  - `quantity` → integer  
- Ensured categorical fields stored as Text  

### 🔹 Block 4: Categorical Standardization & Validation
- Converted categorical values (`region`, `segment`, `category`, `sub_category`, `state`, `city`) to lowercase  
- Extracted unique values for validation  
- Validated `state` against U.S. reference list (50 states + DC)  
- Reviewed city anomalies:  
  - `new york city` consistently used (no `new york`)  
  - All `saint` values fully spelled (no abbreviations)  
  - `port saint lucie` verified as an official city name  

---

## ✅ Final Deliverables
- A fully cleaned dataset: **`superstore_cleaned.xlsx`**  
- A transparent step-by-step **documentation log** (`data_documentation.xlsx`)   
