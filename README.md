# 🏦 Bank Data Analysis Dashboard

---

## 📑 Table of Contents

1. Project Overview  
2. Dataset Description  
3. File Structure & Images  
4. Data Preparation & Transformations  
5. DAX Measures  
6. Key KPI Measures  
7. Branch / Location Measures  
8. Day / Time Analysis  
9. Dashboard Pages & Visualizations  
10. Navigation, Bookmarks & Page Navigator  
11. Drill-Down & Interactivity  
12. Performance Optimization  
13. How to Reproduce / Deliverables  
14. Business Insights & Recommendations  

---

# 📌 1. Project Overview

This project analyzes banking data to uncover insights related to:

- 💰 Loan distribution  
- 📊 Customer transactions  
- 🏦 Branch performance  
- 📈 Revenue trends  

### 🎯 Objective:
To help banks improve **decision-making, customer management, and financial performance** using data analytics.

---

# 📊 2. Dataset Description

The dataset contains banking transactional and customer data:

| Column Name        | Description |
|-------------------|------------|
| Customer_ID       | Unique customer identifier |
| Customer_Name     | Name of customer |
| Age               | Customer age |
| Gender            | Male / Female |
| Branch            | Bank branch |
| Account_Type      | Savings / Current |
| Loan_Amount       | Loan issued |
| Transaction_Amount| Amount per transaction |
| Transaction_Date  | Date of transaction |
| Transaction_Type  | Credit / Debit |
| Balance           | Account balance |


---

# 🧹 3. Data Preparation & Transformations

## Step 1: Data Cleaning
- Removed null values  
- Removed duplicates  
- Standardized column names  

---

## Step 2: Data Type Conversion
- Converted Transaction_Date to datetime  
- Ensured numeric columns  

---

## Step 3: Feature Engineering

### Extract Year & Month
```python id="b1"
df['Year'] = df['Transaction_Date'].dt.year
df['Month'] = df['Transaction_Date'].dt.month
```
### Create Transaction Type Category
- Credit / Debit classification
## Step 4: Data Validation
- Checked balance consistency
- Verified transaction totals


---
##  📐 5. DAX Measures (Power BI)
- ### Total Customers
Total Customers = DISTINCTCOUNT('Bank'[Customer_ID])
- ### Total Transactions
Total Transactions = COUNT('Bank'[Transaction_Amount])
- ### Total Loan Amount
Total Loan = SUM('Bank'[Loan_Amount])
- ### Total Balance
Total Balance = SUM('Bank'[Balance])

---
# 📊 6. Key KPI Measures
- 👥 Total Customers
- 💰 Total Balance
- 📊 Total Transactions
- 🏦 Total Loan Amount
- 📈 Average Transaction Value

---

# 📍 7. Branch / Location Measures

- ### Transactions by Branch
Branch Transactions = COUNT('Bank'[Branch])
- ### Revenue by Branch
Branch Revenue = SUM('Bank'[Transaction_Amount])



# 📊 8. Dashboard Pages & Visualizations

## 1️⃣ Overview Dashboard

### KPIs:

- Total Customers
- Total Balance
- Total Transactions
- Loan Amount

### Charts:

- Transaction trends
- Account type distribution

## 2️⃣Branch Analysis

### Charts:

- Transactions by branch
- Revenue by branch

## 3️⃣ Loan Analysis

### Charts:

- Loan distribution
- Loan by customer segment

## 4️⃣ Transaction Analysis

### Charts:

- Credit vs Debit
- Monthly transaction trends

---
# 🔍 9. Drill-Down & Interactivity

### Drill-Down:
- Year → Month 
- Branch → Customer
### Filters:
-Branch
- Account Type
- Date
### Interactivity:
- Cross-filtering
- Dynamic visuals

---
# ⚡ 10. Performance Optimization
- Removed unused columns
- Optimized DAX calculations
- Limited visuals per page
---

# 🚀 11. How to Reproduce / Deliverables
### Steps:
- Load dataset into Power BI / Tableau
- Clean and transform data
- Create measures and KPIs
- Build dashboard

### 📦 Deliverables
- ✅ Power BI Dashboard (.pbix)
- ✅ Tableau Dashboard (.twbx)
- ✅ Dataset
- ✅ Insights


# 📈 12. Business Insights

- 📊 Key Insights
- 🏦 Certain branches generate higher transactions
- 💰 Loan distribution varies across customers
- 📈 Transaction trends show seasonal variation
- 💳 Credit transactions dominate

---

# ⭐13. Conclusion

This project demonstrates:
- End-to-end banking data analysis
- Dashboard creation using Power BI & Tableau
- Strong business insight generation

---

# 💡14.Dashboard Images
### Power BI Dashboard 
<img src="https://github.com/GauriPise/Ecommerce-data-analysis/blob/main/Screenshot 2026-03-20 183033.png" width="1000"> <br> 

--

### Customer Insights
<img src="https://github.com/GauriPise/Ecommerce-data-analysis/blob/main/Screenshot 2026-03-20 183121.png" width="1000"> <br> 

--

### Profit Analysis
<img src="https://github.com/GauriPise/Ecommerce-data-analysis/blob/main/Screenshot 2026-03-20 183142.png" width="1000"> <br> 
