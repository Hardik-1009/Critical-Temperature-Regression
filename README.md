# 🔬 Predicting Superconducting Critical Temperature using Machine Learning

This project builds an end-to-end machine learning system to predict the superconducting critical temperature (Tc) of materials using engineered physical and chemical descriptors. The goal is to accelerate materials discovery by identifying promising superconductors without expensive experimental trials.

---

## 🚀 Project Overview

Superconducting critical temperature prediction is a high-impact materials science problem where experimental evaluation is costly and slow. This project:

- Uses multiple regression models to predict Tc from material descriptors  
- Handles skewed scientific features and rare extreme values using robust preprocessing  
- Benchmarks linear, tree-based, and boosting models  
- Selects and tunes the best-performing model based on generalization performance  

---

## 📁 Dataset

- **Source:** SuperCon Database (NIMS)  
- **Instances:** 21,263 superconducting materials  
- **Features:** 81 engineered numerical descriptors  
- **Target:** `critical_temperature` (in Kelvin)  
- **Nature:** Highly non-linear scientific regression problem  

---

## 🧠 Modeling Approach

### Models Evaluated
- Linear Regression, Ridge, Lasso (baselines)
- Decision Tree Regressor
- Random Forest Regressor
- Gradient Boosting Regressor
- Support Vector Regression (SVR)
- XGBoost (final selected model)

### Key Techniques
- Median imputation for missing values  
- Robust scaling for skewed numeric features  
- Outlier-aware preprocessing (no blind removal)  
- Controlled experiments with PCA, ensembling, and target transformation  
- Hyperparameter tuning using RandomizedSearchCV  

### Final Model
- **Model:** XGBoost Regressor  
- **Hyperparameters:** Tuned with cross-validated randomized search  
- **Selection Criteria:** Best test RMSE and R²  

---

## 📈 Results (Test Set)

| Metric | Value |
|--------|--------|
| R² | ~0.93 |
| RMSE | ~8.7 K |
| MAE | ~5.0 K |

