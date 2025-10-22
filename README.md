# 🛒 Amazon Sales Data Cleaning & EDA

This repository contains the **cleaned and preprocessed Amazon Sales dataset (2025)**.  
The focus of this project is on preparing the data for **exploratory data analysis (EDA)** and gaining actionable insights through data visualization.

---

## 📘 Dataset

- Original source: Amazon Sales Data (Kaggle / internal dataset)
- Files included:
  - `amazon_sales_data 2025.csv` – Original raw dataset  
  - `cleaned_amazon_sales_data.csv` – Cleaned and preprocessed dataset  
  - `clean_preprocess.py` – Python script for data cleaning and preprocessing  
  - `eda_analysis.py` – Python script for performing EDA and generating visualizations  

---

## 🧹 Data Cleaning & Preprocessing Steps

1. **Removed Duplicates and Whitespace**
   - Dropped duplicate rows  
   - Trimmed whitespace from column names and string values  

2. **Handled Missing Values**
   - Filled numeric columns with the **median**  
   - Filled categorical columns with the **mode (most frequent)**  

3. **Converted Data Types**
   - Parsed date columns (like `Order Date`) to proper datetime format  
   - Converted numeric-looking columns from strings to numeric values  

4. **Outlier Handling**
   - Used the **IQR (Interquartile Range)** method to cap extreme values  

5. **Feature Engineering**
   - Extracted `Order_Month` and `Order_Year` from `Order Date` for trend analysis  

---

## 📊 Exploratory Data Analysis (EDA)

The EDA script (`eda_analysis.py`) generates visualizations to understand the dataset better.

### Key Analyses:
- **Summary statistics:** mean, median, std, etc.  
- **Histograms & boxplots:** distribution of numeric features  
- **Correlation heatmap:** identify relationships between features  
- **Category-level analysis:** top-performing categories and cities  
- **Monthly trends:** total sales per month  
- **Gender-based and age-based spending patterns (if available)**  

---

## 🧠 Usage Example

```python
import pandas as pd

# Load cleaned dataset
df = pd.read_csv('cleaned_amazon_sales_data.csv')

# Display first few rows
print(df.head())

# Example: total sales by category
category_sales = df.groupby('Category')['Amount'].sum().sort_values(ascending=False)
print(category_sales)
