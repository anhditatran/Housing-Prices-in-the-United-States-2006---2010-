# U.S. Housing Price Analysis & Prediction (2006–2010)

## Overview
This project analyzes U.S. housing prices (Ames dataset, 2006–2010) to identify the strongest value drivers and evaluate predictive models during both stable years and the 2008 financial crisis. The goal is to understand **what determines housing value** and **how accurately we can predict sale prices**.

---

## Key Insights

### 1. Size & Quality Are the Strongest Predictors
- **Above-ground living area (GrLivArea)** and **Overall Quality** show the highest correlation with sale price.
- Quality **amplifies** the value of size — large, high-quality homes command significantly higher prices.

### 2. Location Creates Major Price Gaps
- Neighborhood differences produce **$100k–$200k** swings in median price.
- High-demand neighborhoods (NoRidge, StoneBr) consistently outperform lower-value areas.

### 3. 2008 Crisis Reduced Sales, Not Prices
- Average prices stayed steady (~$175k–$182k).
- **Sales volume dropped by ~50%** after 2008 due to rising delinquency rates and tighter lending.
- Demand collapsed even as mortgage rates fell.

### 4. Model Performance
**Model 1 – Top Predictors**
- Adj. R² ≈ **0.44**
- Best predictive performance and clearest interpretation

**Model 2 – Full Model**
- Adj. R² ≈ **0.50** (train), but lower stability on test data
- High feature overlap introduces noise

**Interaction Model (Quality × Size)**
- Improves accuracy, especially for higher-priced homes  
- Confirms complementary effect of size and quality

---
## Methods & Tools
- Python (pandas, numpy, scikit-learn, statsmodels)
- Log-transform of SalePrice for improved fit
- One-hot encoding for categorical features
- 80/20 train–test split for evaluation (RMSE, MAE, R²)
- Visual EDA: distributions, correlations, neighborhood trends

---

##  Extended Analysis
- **Mortgage Rates:** Higher rates → lower median prices.
- **Delinquency Rates:** Strong crisis indicator; explains drop in demand.
- **Property Age:** Newer homes sell higher; renovated older homes retain value.
- **Neighborhood Segmentation:** Strongest non-structural driver of price differences.

---

##  Conclusion
Housing prices are primarily driven by **size**, **quality**, and **location**.  
Macroeconomic conditions (delinquencies, credit tightening) shape **market activity** but do not significantly alter core pricing levels.  
Simple, well-selected models outperform complex ones for prediction and communication.

---

##  Future Work
- Test nonlinear or ML models (Random Forest, XGBoost)
- Add income, employment, and credit-access data
- Build an interactive dashboard for real estate decision-making

---


