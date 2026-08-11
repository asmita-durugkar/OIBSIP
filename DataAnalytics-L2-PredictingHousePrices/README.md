# Predicting House Prices with Linear Regression 🏡

## Overview
This project is part of the **Oasis Infobyte Data Analytics Internship (Level 2 - Task 1)**. The objective is to build a machine learning regression model to predict the price of houses based on various physical features and attributes.

## Dataset
The data used in this project is the **[House price prediction dataset](https://www.kaggle.com/datasets/shree1992/housedata)** sourced from Kaggle.
* **Total Records:** 4,600 houses
* **Key Features:** Price, Bedrooms, Bathrooms, Sqft Living, Sqft Lot, Floors, Waterfront, View, Condition, Sqft Above, Sqft Basement, Yr Built, Yr Renovated.

## Project Workflow
1. **Exploratory Data Analysis (EDA):** Checked for missing values, generated descriptive statistics, and visualized the distribution of the target variable (`price`).
2. **Data Preprocessing:** Dropped non-numeric and high-cardinality categorical columns (`date`, `street`, `city`, `statezip`, `country`) to streamline the baseline model and prevent overfitting.
3. **Feature Selection & Correlation:** Generated a correlation heatmap to identify which features most strongly correlate with the target variable.
4. **Model Training:** Split the dataset into training (80%) and testing (20%) sets and trained a baseline **Linear Regression** model.
5. **Model Evaluation:** Assessed model performance using Mean Squared Error (MSE), Root Mean Squared Error (RMSE), and the R² Score. Created scatter plots for Actual vs. Predicted prices and a Residual plot to check error distribution.
6. **Coefficient Analysis:** Extracted and sorted model coefficients to understand which features mathematically drove the price predictions.
7. **Bonus - Regularization:** Trained and compared **Ridge ($L_2$)** and **Lasso ($L_1$)** regression models against the baseline Linear Regression model.

## Key Findings
* **Top Correlated Features:** `sqft_living`, `sqft_above`, and `bathrooms` showed the highest positive correlation with house prices.
* **Highest Impact Features:** Features like `waterfront` and `floors` had massive coefficient weights, heavily influencing the model's price predictions.
* **Model Performance:** All three models (Linear, Ridge, Lasso) performed similarly. The R² score highlights that predicting real estate purely on basic numerical features is challenging due to massive price outliers (e.g., $0 anomalous entries and multi-million dollar mansions) present in the raw data.

## Technologies Used
* **Language:** Python
* **Libraries:** Pandas, NumPy, Matplotlib, Seaborn, Scikit-Learn
* **Environment:** Google Colab

## How to Run
1. Clone this repository to your local machine.
2. Download the dataset using the Kaggle API or manually from the link above.
3. Open `Predicting_House_Prices.ipynb` in Jupyter Notebook or Google Colab.
4. Run all cells sequentially to view the EDA, visualizations, and model evaluations.
