<div align="center">

# 🧹 ApexPlanet Task 1 – Data Immersion & Wrangling

### Data Cleaning Pipeline using Python & Pandas

<img src="https://img.shields.io/badge/Python-3.13-blue?logo=python" />
<img src="https://img.shields.io/badge/Pandas-2.x-150458?logo=pandas" />
<img src="https://img.shields.io/badge/NumPy-013243?logo=numpy" />
<img src="https://img.shields.io/badge/Jupyter_Notebook-F37626?logo=jupyter&logoColor=white" />
<img src="https://img.shields.io/badge/Status-Completed-success" />

**ApexPlanet Software Pvt. Ltd. – Data Analytics Internship**

</div>

---

# 📌 Project Overview

This repository contains my submission for **Task 1 – Data Immersion & Wrangling** completed during the **ApexPlanet Data Analytics Internship**.

The objective was to inspect the raw sales dataset, assess data quality, clean inconsistencies, engineer useful features, and export an analysis-ready dataset using Python.

---

# 🎯 Objectives

- Understand the structure of the dataset
- Identify missing values
- Detect duplicate records
- Repair data quality issues
- Standardize date formats
- Engineer analysis-ready features
- Export a cleaned dataset for further analysis

---

# 🛠️ Tech Stack

| Tool | Purpose |
|------|---------|
| Python | Data Processing |
| Pandas | Data Cleaning |
| NumPy | Numerical Operations |
| Jupyter Notebook | Development Environment |

---

# 📂 Repository Structure

```
ApexPlanet-Task1-Data-Wrangling
│
├── 01_data
│   ├── ApexPlanet_DataAnalytics_Dataset.xlsx
│   └── cleaned_sales_dataset.csv
│
├── 02_notebook
│   └── ApexPlanet_Task1_Data_Wrangling.ipynb
│
├── 03_report
│   └── ApexPlanet_Task1_Data_Wrangling_Report.docx
│
├── 04_src
│   └── clean_pipeline.py
│
├── LICENSE
├── .gitignore
└── README.md
```

---

# 📊 Dataset Information

| Attribute | Value |
|-----------|-------|
| Records | 1,000 |
| Original Columns | 12 |
| Final Columns | 19 |
| Dataset Type | Sales Transactions |

---

# 🔍 Data Quality Assessment

The dataset was profiled before applying any transformations.

### Missing Values

| Column | Missing |
|---------|---------|
| Age | 20 |
| City | 13 |

### Duplicate Check

- ✅ No full-row duplicates
- ⚠️ 9 duplicated `Order_ID` values (different transactions)

### Date Format

- `Order_Date` stored as text
- Converted into proper datetime format

### Outlier Detection

IQR method applied on:

- Age
- Quantity
- Unit Price
- Total Sales

**Result:** No significant outliers detected.

---

# 🧹 Data Cleaning Pipeline

The following preprocessing steps were performed:

### ✅ Missing Value Treatment

- Filled missing **Age** values using the **median**
- Filled missing **City** values using **"Unknown"**

---

### ✅ Duplicate Handling

- Removed exact duplicate rows
- Repaired duplicate `Order_ID` values by assigning unique surrogate IDs
- Added an `Order_ID_Flag` column for traceability

---

### ✅ Date Standardization

Converted:

```
Order_Date
```

to

```
datetime64
```

using Pandas.

---

### ✅ Feature Engineering

Created five new features:

| Feature | Description |
|----------|-------------|
| Order_Year | Year of transaction |
| Order_Month | Numeric month |
| Order_Month_Name | Month name |
| Age_Group | Customer age segmentation |
| Avg_Price_Check | Total Sales ÷ Quantity |

---

# 📈 Final Output

After preprocessing:

- ✅ Missing values removed
- ✅ Duplicate IDs repaired
- ✅ Date standardized
- ✅ Five engineered features added
- ✅ Clean dataset exported

Output file:

```
cleaned_sales_dataset.csv
```

---

# 🚀 How to Run

Clone the repository:

```bash
git clone https://github.com/yourusername/ApexPlanet-Task1-Data-Wrangling.git
```

Navigate into the project:

```bash
cd ApexPlanet-Task1-Data-Wrangling
```

Install dependencies:

```bash
pip install pandas numpy openpyxl
```

Run the notebook:

```bash
jupyter notebook
```

or execute the pipeline:

```bash
python 04_src/clean_pipeline.py
```

---

# 📁 Deliverables

- ✅ Jupyter Notebook
- ✅ Python Cleaning Script
- ✅ Technical Report
- ✅ Cleaned CSV Dataset

---

# 📚 Skills Demonstrated

- Data Wrangling
- Data Cleaning
- Missing Value Treatment
- Duplicate Detection
- Feature Engineering
- Pandas
- NumPy
- Jupyter Notebook
- Python Programming

---

# 👨‍💻 Author

**Brojo Mohan Dutta**

Data Analytics Intern

GitHub: https://github.com/brojomohan58-boop

LinkedIn: www.linkedin.com/in/brojo-mohan-dutta

---

<div align="center">

⭐ If you found this project helpful, consider giving it a star.

</div>
