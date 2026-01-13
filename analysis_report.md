
# 📄 Data Analysis & Prediction Report

## 📌 Executive Summary
This report outlines the findings from the weekly internship task involving two distinct datasets: Sales Data and Customer Churn Data. The objective was to optimize code performance, enhance readability, and derive actionable business insights.

---

## 🔹 Part 1: Sales Data Analysis

### **Objective**
To evaluate sales performance across different dimensions (Time, Product, Region) and identify high-value customers.

### **Methodology**
- **Data Optimization**: utilized `parse_dates` during loading and `resample()` for time-series aggregation to reduce computational overhead.
- **Regional Analysis**: Added a granular breakdown of sales by Region (East, West, North, South) to identify underperforming markets.

### **Key Insights**
1.  **Revenue Trends**: Analysis of monthly sales data reveals specific seasonal trends, allowing for better inventory planning.
2.  **Top Products**: Identified the top 5 revenue-generating products. These items should be prioritized in marketing campaigns.
3.  **Customer Segmentation**: The analysis isolated the top 5 high-value customers, enabling targeted loyalty programs.

---

## 🔹 Part 2: Customer Churn Prediction

### **Objective**
To build a robust Machine Learning model capable of predicting whether a customer will churn (leave the service) and identifying the primary drivers of churn.

### **Methodology**
- **Pipeline Architecture**: Implemented a `Scikit-Learn Pipeline` ensuring that preprocessing steps (StandardScaling, OneHotEncoding) are applied consistently to both training and test data.
- **Model Selection**: Logistic Regression was chosen for its interpretability, allowing us to extract coefficients that explain feature impact.
- **Error Handling**: Implemented robust coercion for the `TotalCharges` column to handle dirty data (empty strings) without manual intervention.

### **Model Performance**
- **Metric**: The model was evaluated using Accuracy and a Confusion Matrix to balance False Positives and False Negatives.
- **Validation**: An 80/20 train-test split was used to validate the model's generalization capability.

### **Strategic Recommendations (Feature Importance)**
Based on the model coefficients, the following factors most strongly influence churn:
1.  **Contract Type**: Customers on "Month-to-month" contracts show a significantly higher likelihood of churning compared to 1-year or 2-year contracts.
2.  **Payment Method**: Specific payment methods (e.g., Electronic Check) correlate with higher churn rates.
3.  **Tenure**: Newer customers are at higher risk; retention efforts should focus heavily on the first 6 months.

---

## 🏁 Conclusion
The refactored codebase successfully meets the requirements for **modularity** and **optimization**. By transitioning from iterative loops to vectorized Pandas operations and implementing ML pipelines, the solution is now scalable, readable, and ready for production deployment.

```
