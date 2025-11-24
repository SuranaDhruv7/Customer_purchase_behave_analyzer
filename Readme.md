# 📘 **README – Data Cleaning, Merging & Reporting Project**

## 📂 **1. Project Overview**
This project focuses on **cleaning, preprocessing, feature engineering, and merging** three datasets into one final analysis-ready master dataset.

### 📁 **Datasets Used**
- **Products Dataset** (`inventory.sql`) – Contains product-level information like product ID, name, price, stock, and category.  
- **Sales Dataset** (`sales.json`) – Contains each transaction with amount, payment type, user ID, product ID, and date.
- **Users Dataset** (`users.csv`) – Contains demographic and profile details of customers.

The goal was to **clean**, **merge**, and **generate a final summary report** showing:
- Records before vs after cleaning  
- Missing values before vs after  
- Outlier counts before vs after  
- Number of engineered features  

---

# 🧹 **2. Data Cleaning Workflow**

## 🔧 **2.1 Cleaning Steps**
The following steps were applied across datasets:

### 🟦 **Sales Dataset**
- Converted `date` to datetime  
- Filled missing numerical values (`amount`) using **median imputation**  
- Filled missing categorical values (`payment_type`) with **"Unknown"**  
- Removed duplicate rows  

### 🟩 **Products Dataset**
- Parsed SQL INSERT rows into structured DataFrame  
- Cleaned strings  
- Imputed missing `price` values with median  
- Imputed missing `stock` values with 0  

### 🟨 **Users Dataset**
- Cleaned string columns  
- Filled missing numerical values with median  
- Filled missing categorical fields with **"Unknown"**  

---