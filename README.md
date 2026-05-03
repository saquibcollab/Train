# Train
Data Exploration: Analyzed 1,460 records with 81 features, identifying Overall Quality and Living Area as the primary price drivers.
# House Price Prediction using Random Forest Regression

This project implements an end-to-end Machine Learning pipeline to predict residential real estate prices. Using the **train.csv** dataset, the project compares a baseline Linear Regression model against a more robust Random Forest Regressor.

## 🚀 Project Overview
The goal is to predict the `SalePrice` of houses based on a variety of features including quality ratings, square footage, and location.

## 📊 Dataset Description
The model is trained on the **train.csv** dataset, which includes:
- **1,460** observations.
- **81** features (categorical and numerical).
- **Target Variable:** `SalePrice`.

## 🛠️ Key Machine Learning Steps

### 1. Data Cleaning & Exploration
- Identified key drivers of price: `OverallQual`, `GrLivArea`, and `GarageCars`.
- Handled missing values through median imputation and categorical replacement.
- Dropped high-missingness columns like `PoolQC` and `MiscFeature`.

### 2. Feature Engineering
- **Ordinal Encoding:** Converted quality-based categorical ratings (Ex, Gd, TA, Fa, Po) into numerical scales (5-1).
- **One-Hot Encoding:** Transformed nominal variables like `Neighborhood` and `Foundation` into binary columns.

### 3. Model Training & Comparison
Two models were evaluated to determine the best fit for the data:
- **Linear Regression:** Served as the baseline.
- **Random Forest Regressor:** Selected for its ability to capture non-linear relationships.

## 📈 Performance Results

| Metric | Linear Regression | Random Forest |
| :--- | :--- | :--- |
| **MAE** | $25,319.86 | **$19,210.50** |
| **RMSE** | $39,710.99 | **$28,943.62** |
| **R² Score** | 0.7944 | **0.8908** |

**Conclusion:** The Random Forest model significantly outperformed the baseline, explaining **89%** of the variance in house prices.

## 📁 Repository Structure
- `train.csv`: The primary dataset.
- `house_price_analysis.ipynb`: Full Python implementation.
- `README.md`: Project documentation.

## ⚙️ Requirements
- Python 3.x
- Pandas
- NumPy
- Scikit-Learn
- Matplotlib / Seaborn

## 📝 How to Run
1. Clone the repository.
2. Ensure `train.csv` is in the root directory.
3. Run the notebook or script to train the model and view evaluation metrics.
