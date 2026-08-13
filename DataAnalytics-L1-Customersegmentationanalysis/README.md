# Customer Segmentation Analysis

This project performs customer segmentation on an e-commerce dataset to identify distinct purchasing behaviors and group customers accordingly. The analysis uses K-Means clustering to help tailor targeted marketing strategies, improve customer retention, and maximize lifetime value.

## Dataset
The project utilizes the [E-commerce Customer Behavior Dataset](https://www.kaggle.com/datasets/dhairyajeetsingh/ecommerce-customer-behavior-dataset) from Kaggle. It includes customer metrics such as:
- Age, Gender, Location
- Login Frequency
- Average Session Duration
- Cart Abandonment Rate
- Lifetime Value
- And more...

## Project Workflow

1. **Data Ingestion:** 
   - Uses the Kaggle API to programmatically download and unzip the dataset.
   - Loads the `ecommerce_customer_churn_dataset.csv` into a Pandas DataFrame.

2. **Data Preprocessing & Cleaning:**
   - Handles missing values by imputing the mean for columns like `Session_Duration_Avg`, `Product_Reviews_Written`, and `Pages_Per_Session`.
   - Uses median imputation for `Credit_Balance`.

3. **Feature Engineering & Scaling:**
   - Selects key behavioral features for clustering: `Lifetime_Value`, `Login_Frequency`, and `Session_Duration_Avg`.
   - Standardizes the selected features using `StandardScaler` to ensure optimal performance for the K-Means algorithm.

4. **Clustering Model (K-Means):**
   - Utilizes the **Elbow Method** (calculating Within-Cluster Sum of Squares) to determine the optimal number of clusters (K=3).
   - Fits the K-Means model to group the customer base into 3 distinct segments.

5. **Visualization & Profiling:**
   - Visualizes the clusters using Seaborn scatterplots (e.g., *Login Frequency vs Lifetime Value*).
   - Profiles each cluster by calculating the mean values of the selected features.

## Key Insights & Customer Segments

The clustering model successfully segmented the customers into three distinct profiles:

*   **Cluster 0 (High Value, High Engagement):** Highly active users with the highest average lifetime value (~2704), frequent logins, and long session durations. 
*   **Cluster 1 (Low Value, Low Frequency - "At-Risk/Window Shoppers"):** Customers who rarely log in, spend less time per session, and generate the lowest revenue (~857). 
    * *Actionable Insight:* Implement re-engagement campaigns with limited-time discount codes to build purchasing habits.
*   **Cluster 2 (Medium Value, Medium Engagement):** The middle tier of customers showing average login frequency and lifetime value (~1502).

## Technologies & Libraries Used
- **Python**
- **Pandas** (Data manipulation)
- **Scikit-Learn** (StandardScaler, KMeans clustering)
- **Matplotlib & Seaborn** (Data visualization)
- **Kaggle CLI** (Dataset retrieval)

## How to Run
1. Ensure you have your `kaggle.json` API token configured or loaded via Google Colab secrets if running in Colab.
2. Install necessary dependencies (`pandas`, `scikit-learn`, `matplotlib`, `seaborn`).
3. Run the cells in `Customersegmentanalysis.ipynb` sequentially.
