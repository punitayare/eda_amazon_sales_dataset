# 📊 Exploratory Data Analysis (EDA) — Interview Q&A

## 1. What is the purpose of EDA?
Exploratory Data Analysis (EDA) helps us **understand the structure, patterns, and relationships** within a dataset before applying any machine learning model.  
It helps identify:
- Missing values or outliers  
- Data distribution  
- Correlations between features  
- Potential errors or inconsistencies  

In short, EDA ensures the data is clean, reliable, and meaningful for analysis or model building.

---

## 2. How do boxplots help in understanding a dataset?
A **boxplot** visually summarizes the distribution of a numerical variable.  
It shows:
- The **median** (central tendency)  
- The **quartiles** (spread of the data)  
- **Outliers** (points lying beyond whiskers)  

Boxplots are especially useful to **detect outliers** and **compare distributions** across multiple categories quickly.

---

## 3. What is correlation and why is it useful?
**Correlation** measures the **strength and direction** of a linear relationship between two numerical variables.  
It’s represented by values between **-1 and +1**:
- `+1` → Perfect positive correlation  
- `-1` → Perfect negative correlation  
- `0` → No correlation  

Correlation is useful to identify **dependent variables** and **avoid redundant features** when building predictive models.

---

## 4. How do you detect skewness in data?
**Skewness** shows how much a distribution deviates from symmetry.  
It can be detected by:
- **Visual methods:** Histograms, KDE plots, or boxplots  
- **Statistical methods:** Using `df.skew()` in pandas  

For example:
- **Right (positive) skew:** Long tail on the right → log transformation helps.  
- **Left (negative) skew:** Long tail on the left → square or cube transformation may help.

---

## 5. What is multicollinearity?
**Multicollinearity** occurs when two or more independent variables are **highly correlated** with each other.  
This can make it difficult for ML models (like regression) to determine the effect of each variable correctly.  

It can be detected using:
- **Correlation matrix**  
- **Variance Inflation Factor (VIF)**  

Reducing multicollinearity improves model **stability** and **interpretability**.

---

## 6. What tools do you use for EDA?
Common tools and libraries for EDA include:
- **Python:** `pandas`, `numpy`, `matplotlib`, `seaborn`, `plotly`  
- **Jupyter Notebook** for visualization and documentation  
- **Tableau** or **Power BI** for interactive analysis  

---

## 7. Can you explain a time when EDA helped you find a problem?
During the **Amazon Sales EDA** project, I noticed that some product categories had **missing or zero sales** despite being active.  
EDA revealed:
- Data inconsistencies (wrong price entries)  
- Duplicate transaction IDs  
After cleaning, the overall sales trend became more accurate — showing how EDA directly improved data quality and model accuracy.

---

## 8. What is the role of visualization in ML?
Visualization plays a key role in:
- Understanding **feature relationships**  
- Detecting **patterns and anomalies**  
- Communicating **data insights** clearly  

Before modeling, it helps identify **data issues**; after modeling, it helps interpret **model performance** (e.g., confusion matrix, feature importance).  
In short, visualization bridges **data exploration and decision-making**.

---

✨ *EDA isn’t just about graphs — it’s about building a deep understanding of your data before trusting any prediction.*
