# Concrete Compressive Strength Prediction


## 1. Introduction
This project focuses on predicting Concrete Compressive Strength using a multivariate dataset. The main goal is to build a machine learning model capable of predicting the strength of concrete based on its composition.

* **Dataset:** 1030 records with 8 features.
* **Problem Type:** Regression (Continuous target variable).

## 2. Dataset Description
The dataset contains numerical values with no missing or zero values. There are no binary or categorical features.

**Features:**
1.  **Cement:** Amount of cement (kg/m³).
2.  **Blast Furnace Slag:** Byproduct of iron manufacturing.
3.  **Fly Ash:** Byproduct of cement.
4.  **Water:** Essential for strength.
5.  **Superplasticizer:** Additive to reduce water content.
6.  **Coarse Aggregate**
7.  **Fine Aggregate**
8.  **Age:** Age of the concrete in days.

**Target Variable:**
* Concrete Compressive Strength (MPa)

## 3. Data Preprocessing
* The dataset consists of continuous and integer values.
* No categorical values were present, eliminating the need for encoding.
* No missing values, so imputation (mean/mode/median) was not required.

## 4. Exploratory Data Analysis (EDA)
### Correlations
* **Cement:** Strong positive correlation (+0.5) with strength. Higher cement content generally leads to higher strength.
* **Superplasticizer:** Positive correlation (+0.37).
* **Water:** Negative correlation (-0.29). Excess water reduces strength.
* **Age:** Positive correlation (+0.33).

### Observations
* **Cement vs. Strength:** As cement content rises (300-500+ kg/m³), strength tends to be higher. However, at very high amounts (>400 kg/m³), the increase is not strictly linear.
* **Distribution:** The most common cement amount range is 189.6 - 277.2 kg/m³ (30.2% of data).

## 5. Machine Learning Model
We implemented a **Linear Regression** model suitable for continuous target variables.

**Results:**
* **Mean Squared Error (MSE):** 95.98
* **Root Mean Squared Error (RMSE):** 9.80
* **R² Score:** 0.63

## 6. Conclusion
The Linear Regression model achieved an R² value of 0.63 (predicting 63% of variance). While effective, future improvements could include:
* Hyperparameter Tuning.
* Using non-linear models (e.g., SVR, which showed promising preliminary results of 0.82 R²).
* Outlier detection and removal.