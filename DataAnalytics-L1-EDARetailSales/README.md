# 📊 Exploratory Data Analysis (EDA) on Retail Sales Data

**Author:** Asmita Durugkar  
**Track:** Data Analytics (Level 1, Task 1)  
**Program:** Oasis Infobyte (OIBSIP) Internship  

---

## 📝 Project Overview
This project focuses on performing Exploratory Data Analysis (EDA) on a comprehensive retail sales dataset. The goal of the analysis is to uncover underlying purchasing patterns, understand customer demographics, and evaluate product performance to drive data-backed business decisions. 

## 🛠️ Tools & Technologies Used
* **Language:** Python
* **Libraries:** Pandas, NumPy, Seaborn, Matplotlib
* **Environment:** Jupyter Notebook / Google Colab

## 📈 Key Analyses Performed
1. **Data Cleaning & Preprocessing:** Handled datetime conversions, indexed time-series data, and merged multiple data tables (Transactions, Customers, and Products).
2. **Descriptive Statistics:** Calculated central tendencies, distributions, and summary metrics for numerical sales data.
3. **Time Series Analysis:** Analyzed monthly and quarterly sales trends to identify seasonal spikes and baseline sales volume.
4. **Customer Demographics:** Evaluated the age and gender distribution of the customer base using stacked visualizations.
5. **Product Performance:** Identified the top 10 best-selling products by volume and analyzed total revenue generation grouped by product category.
6. **Correlation Analysis:** Generated a correlation heatmap to test the mathematical relationships between customer age, purchase quantity, and discount rates.

## 💡 Strategic Business Insights
Based on the data visualizations and numerical analysis, the following strategic insights were formulated:

* **Strategic Bundling Over Discounts:** The correlation matrix revealed no significant relationship between discount size and purchase volume. Instead of price-dropping low-performing categories (like Groceries), items should be bundled with high-selling categories (like Electronics) to drive traffic.
* **Youth Market Expansion:** Customer age distribution is relatively flat across all brackets. There is a massive opportunity to capture a larger share of the younger demographic by introducing tech-forward loyalty programs or targeted social media campaigns.
* **Optimizing Female Apparel Sales:** While male shoppers currently drive a slightly higher sales volume, the demographic can be balanced by directly targeting female shoppers with tailored marketing for the already high-performing "Clothing" category.

## 📂 Repository Structure
* `retail_analysis.ipynb`: The main Jupyter Notebook containing the full Python code, data visualizations, and step-by-step markdown observations.
