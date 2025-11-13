# 📘 Customer Transaction Data Processing & EDA Pipeline  

A complete end-to-end project for loading, cleaning, transforming, and enriching customer transaction data from **CSV**, **JSON**, and **SQL** sources.  
This project creates a fully processed dataset ready for **Analytics, Machine Learning, and Dashboarding**. 🚀

---

# 📂 1. Data Sources  

| File | Type | Description |
|------|--------|-------------|
| `users.csv` | 📄 CSV | Customer demographics (user_id, gender, region, etc.) |
| `sales.json` | 📦 JSON | Transaction-level data (transaction_id, user_id, product_id, amount, payment_type, date) |
| `inventory.sql` | 🗄️ SQL | Product catalog (product_id, product_name, category, price, stock) |

---

# 🧭 2. Data Understanding & Loading  

### ✔️ Tasks  
- Load all datasets (CSV, JSON, SQL)  
- Display top 5 rows  
- Show `.info()` summary  
- Identify  
  - Missing values  
  - Incorrect data types  
  - Inconsistent or invalid records  

### 🧪 Tools Used  
- `pd.read_json()`  
- `pd.read_csv()`  
- `sqlite3 + pd.read_sql_query()`  

---

# 🧹 3. Data Cleaning  

### ✔️ Steps Performed  
- Impute **numerical** missing values using `SimpleImputer(mean)`  
- Impute **categorical** missing values using `SimpleImputer(most_frequent)`  
- Use **KNNImputer** for multivariate numeric imputation  
- Fix invalid records:  
  - Negative amounts or prices  
  - Invalid dates  
  - Stripped whitespace and sta