# Automobile Import Price Prediction: Model Performance Comparison

## Introduction
This report compares the performance of various machine learning models in predicting automobile import prices. The models tested include **Linear Regression**, **Support Vector Regression (SVR)**, **K-Nearest Neighbors (KNN)**, **Decision Tree Regression (DTR)**, **Random Forest Regression (RFR)**, **XGBoost**, and **Gradient Boosting Regression (GBR)**. The comparison uses key metrics such as **MSE**, **RMSE**, **MAE**, **R²**, **Adjusted R²**, and **Cross-Validation (CV) scores** to identify the most effective model.

---

## Model Performance Comparison Table

| **Model**                    | **MSE (Before)**  | **RMSE (Before)** | **MAE (Before)**  | **R² (Before)**  | **Adj. R² (Before)** | **MSE (After)**   | **RMSE (After)**  | **MAE (After)**  | **R² (After)**  | **Adj. R² (After)** | **MSE (CV)**     | **RMSE (CV)**   | **MAE (CV)**     | **R² (CV)**   | **Adj. R² (CV)** |
|------------------------------|-------------------|-------------------|-------------------|------------------|----------------------|-------------------|-------------------|-------------------|------------------|---------------------|-------------------|------------------|------------------|-----------------|------------------|
| **Linear Regression**         | 19,596,379.22     | 4,426.78          | 3,007.02          | 0.84             | 0.68                 | 12,086,293.76     | 3,476.53          | 2,609.16          | 0.75             | 0.73                | 12,086,293.76     | 3,476.53          | 2,609.16          | 0.75             | 0.73              |
| **SVR**                       | 149,146,286.53    | 12,212.55         | 7,944.51          | -0.22            | -1.44                | 87,103,473.04     | 9,332.92          | 5,677.81          | 0.29             | -0.42               | 30,952,796.01     | 5,563.52          | 3,147.15          | 0.57             | 0.52              |
| **KNN**                       | 15,590,709.25     | 3,948.51          | 2,639.82          | 0.87             | 0.75                 | 11,977,800.15     | 3,460.90          | 2,190.36          | 0.90             | 0.80                | 12,543,043.69     | 3,541.62          | 2,188.56          | 0.73             | 0.69              |
| **Decision Tree**             | 9,235,088.39      | 3,038.93          | 2,083.07          | 0.92             | 0.85                 | 11,049,356.42     | 3,324.06          | 2,254.76          | 0.91             | 0.82                | 8,992,285.96      | 2,998.71          | 1,954.25          | 0.81             | 0.79              |
| **Random Forest**             | 18,360,051.87     | 4,284.86          | 2,809.38          | 0.85             | 0.70                 | 25,038,187.55     | 5,003.82          | 3,243.17          | 0.80             | 0.59                | 11,430,631.63     | 3,380.92          | 2,065.31          | 0.76             | 0.72              |
| **XGBoost**                   | 12,637,911.52     | 3,554.98          | 2,329.31          | 0.90             | 0.79                 | 11,182,182.12     | 3,343.98          | 2,058.15          | 0.91             | 0.82                | 7,102,279.77      | 2,665.01          | 1,831.23          | 0.85             | 0.83              |
| **Gradient Boosting**         | 9,099,383.57      | 3,016.52          | 1,933.99          | 0.93             | 0.85                 | 7,868,043.22      | 2,805.00          | 1,824.51          | 0.94             | 0.87                | 6,873,409.82      | 2,621.72          | 1,743.42          | 0.84             | 0.82              |

---

## Key Insights

1. **Best Performing Model**:
   - **Gradient Boosting Regression (GBR)** achieves the highest **R²** score (0.94) and **lowest MSE** (7,868,043.22), making it the **best model** for predicting automobile import prices.
   - Its **CV performance** (R² = 0.84) further confirms that it generalizes well across different data splits.

2. **Other Strong Models**:
   - **K-Nearest Neighbors (KNN)** performs well, with an **R²** of 0.90 after tuning and competitive **CV scores** (R² = 0.73).
   - **Decision Tree Regression (DTR)** is also a strong performer, with an **R²** of 0.91 post-tuning, and **CV performance** (R² = 0.81) shows it performs consistently on unseen data.
   - **XGBoost** is another top contender, showing an **R²** of 0.91 after tuning and strong **CV performance** (R² = 0.85).

3. **Models to Avoid**:
   - **Support Vector Regression (SVR)** underperforms with an **R²** of -0.22 before tuning and a marginal improvement to 0.29 after tuning.
   - Its **CV performance** is also weak (R² = 0.57), indicating poor generalization and suggesting it is **not a good fit** for this problem.

---

## Conclusion

- **Best Model**: **Gradient Boosting Regression (GBR)** stands out as the best model with the highest **R² (0.94)** and lowest **MSE (7,868,043.22)**, along with solid **cross-validation (CV)** performance.
- **Other Top Models**:  
  - **K-Nearest Neighbors (KNN)** and **Decision Tree Regression (DTR)** are also strong performers, with good R² and solid CV scores.
  - **XGBoost** performs well too, making it a viable alternative.

- **Avoid**:  
  - **Support Vector Regression (SVR)** should be avoided due to its consistently poor performance across all metrics, including **CV scores** (R² = 0.57).

### Summary

- **Top Model**: **Gradient Boosting Regression (GBR)**
- **Alternative Strong Models**: **KNN**, **DTR**, **XGBoost**
- **Avoid**: **SVR**

By choosing **GBR**, you can expect **accurate predictions** for automobile import prices with good generalization to unseen data.

---

### Why GBR?
The **Gradient Boosting Regression (GBR)** model provides **the best overall performance** in terms of prediction accuracy and generalization (cross-validation). This makes it the most reliable model for production use.
