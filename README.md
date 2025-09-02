# Performance of LASSO and Ridge Regression for Variable Selection in Genome-Wide Association Studies of Maize Selection in Genome-Wide Association Studies of Maize Flowering Time

This repository contains the implementation and report for the project:

**Dipok Deb**  
PhD Student, Big Data Analytics, UCF  
Email: dipok.deb@ucf.edu  

📄 Full report: [`report/Performance_of_LASSO_and_Ridge.pdf`](report/Performance_of_LASSO_and_Ridge.pdf)

---

## 📖 Project Overview
Genome-Wide Association Studies (GWAS) are used to identify genetic variants linked to complex traits.  
This project investigates **maize flowering time** using a dataset of ~5,000 recombinant inbred lines across 8 environments.  

We compare two penalized regression methods:
- **LASSO Regression** (L1 penalty, feature selection)
- **Ridge Regression** (L2 penalty, coefficient shrinkage)

---

## 📊 Key Findings
- LASSO selected **45 features** at optimal α = 0.1  
- Ridge retained **4,211 features** at optimal α = 1000  
- **Ridge outperformed LASSO** with slightly lower prediction error:
  - LASSO → MSE = 12.7045, RMSE = 3.5643  
  - Ridge → MSE = 12.2223, RMSE = 3.4960  

---

## ⚙️ Methodology
1. **Data Preprocessing**  
   - 4,981 samples × 7,393 variables  
   - Missing values removed → 4,494 samples used  
   - Features: SNP markers  
   - Target: days to male flowering (`dtoa`)

2. **Model Training**  
   - Implemented using `scikit-learn`  
   - Hyperparameter tuning with `GridSearchCV` (5-fold CV)  
   - Evaluation using MSE & RMSE  

3. **Tools Used**  
   - Python, NumPy, Pandas, Scikit-learn, Matplotlib

