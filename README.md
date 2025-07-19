# 🚗 Used Car Price Prediction using Linear Regression

This project aims to predict the selling price of used cars using various regression models including Linear, Ridge, and Lasso Regression. It follows a complete machine learning workflow from data preprocessing to model evaluation and deployment.

---

## 📁 Project Structure
- data/ # Contains the raw and cleaned dataset
- notebooks/ # Jupyter Notebooks for EDA and modeling
- outputs/ # Trained models and evaluation results
- .gitignore # Specifies files/folders to be ignored by Git
- README.md # Project documentation


---

## 📊 Dataset Overview

- **File**: `car_price_prediction_raw.csv`

### Key Features
- `year` – Manufacturing year
- `km_driven` – Kilometers the car has been driven
- `fuel` – Type of fuel used
- `seller_type` – Type of seller (Dealer/Individual)
- `transmission` – Transmission type (Manual/Automatic)
- `owner` – Ownership status
- `brand` – Extracted from car name
- `engine_size` – Extracted from engine details
- `selling_price` – (Target) Price to be predicted

---

## ⚙️ Workflow Summary

### 1. Data Cleaning
- Converted `year` to `car_age`
- Extracted brand and engine size
- Handled duplicates and missing values
- Label encoding and one-hot encoding for categorical features

### 2. Model Training
- Trained and evaluated:
  - Linear Regression
  - Ridge Regression
  - Lasso Regression

### 3. Model Evaluation

| Model             | MAE        | MSE            | RMSE       | R² Score |
|------------------|------------|----------------|------------|----------|
| Linear Regression| 181065.93  | 1.49e+11       | 386378.57  | 0.5366   |
| Ridge Regression | 181161.29  | 1.50e+11       | 386666.91  | 0.5359   |
| Lasso Regression | 181391.16  | 1.50e+11       | 387163.96  | 0.5347   |

> ✅ Linear Regression was selected for final prediction based on overall performance.

---

## 📦 Outputs

Saved in `outputs/` directory:
- `linear_regression_model.pkl` – Trained model for linear regression
- `rideg_regression_model.pkl` – Trained model for ridge regression
- `lasso_regression_model.pkl` – Trained model for lasso regression
- `model_metrics.csv` – MAE, MSE, RMSE, R² Score for all 3 models
