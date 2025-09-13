# 🏡 Predicting House Prices with Linear Regression

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/)

---

## 📌 Project Overview
This project focuses on predicting house prices using a dataset of **545 houses** with both **numerical and categorical features**.  
We apply **Exploratory Data Analysis (EDA)** to understand key factors affecting price, and then train a **Linear Regression model** to estimate house prices.

---

## 📂 Dataset
- **Rows:** 545  
- **Columns:** 13  
- **Target Variable:** `price`  
- **Features:**
  - **Numerical:** area, bedrooms, bathrooms, stories, parking  
  - **Categorical:** mainroad, guestroom, basement, airconditioning, furnishingstatus, etc.  

✅ No missing values found in the dataset.  

---

## 🔍 Exploratory Data Analysis

### Descriptive Statistics
- **Price:** Avg ≈ 4.76M | Range: 1.75M – 13.3M  
- **Area:** Avg ≈ 5150 sq. ft. | Range: 1650 – 16200  
- **Bedrooms:** Mostly 2–4  
- **Bathrooms & Stories:** Higher values generally linked to higher prices  

### Correlations
- Strong positive correlation with price: `area`, `bathrooms`, `stories`, `parking`  
- `bedrooms` shows weaker correlation compared to other features  

### Visual Findings
- **Price vs. Area:** Larger area → Higher price  
- **Price vs. Bathrooms/Stories:** Clear positive trend  
- **Categorical Features:**  
  - Houses on the **mainroad** and with **air conditioning** tend to cost more  
  - **Furnishing status** (furnished > semi-furnished > unfurnished) also impacts price  

---

## 🛠️ Data Preparation
- One-hot encoded categorical variables (e.g., furnishingstatus → furnished, semi-furnished, unfurnished)  
- Features (`X`) and Target (`y`) defined  
- Train-test split: **80% train, 20% test**

---

## 🤖 Model Training
- **Algorithm:** Linear Regression  
- **Input:** 12 features (numerical + encoded categorical)  
- **Output:** Predicted house price  

---

## 📊 Model Evaluation
- **Mean Squared Error (MSE):** ≈ **1.75 trillion**  
- **R-squared Score (R²):** ≈ **0.65**  

### Key Findings:
- Model explains ~65% of price variation  
- Performs well in low-to-mid price ranges  
- Struggles with high-value luxury houses (under/overestimation)  

---

## 📈 Visualizations

### Actual vs. Predicted Prices
- Most predictions align with the diagonal line → model captures general trends  
- Larger deviations at extreme prices  

### Residual Analysis
- Residuals are centered around zero (no strong bias)  
- Approximate bell-shaped distribution → satisfies linear regression assumptions  
- Some large residuals → outliers affecting predictions  

---

## 📝 Final Insights
- **Strongest Predictors:** Area, bathrooms, stories, parking, air conditioning, and furnishing status  
- **Weaker Predictors:** Bedrooms alone have less influence on price  
- **Business Implications:**  
  - Marketing should highlight size and amenities (AC, parking, furnished options)  
  - Consider different models (Ridge/Lasso, Decision Trees, Random Forests) for improved accuracy on luxury homes  

---

## 🚀 Conclusion
Linear Regression provides a **baseline model** with decent performance (R² = 0.65).  
Future improvements could include:
- Feature engineering (e.g., interaction terms between amenities)  
- Trying advanced models (Random Forest, Gradient Boosting)  
- Hyperparameter tuning and cross-validation  

---
