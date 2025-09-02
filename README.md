# Performance of LASSO and Ridge Regression for Variable Selection in Genome-Wide Association Studies of Maize Flowering Time

This project was completed as part of **"STA 6366: Data Science I"** at the University of Central Florida. The initial goal was to apply penalized regression techniques (LASSO and Ridge) to Genome-Wide Association Studies (GWAS) for identifying genetic variants associated with maize flowering time.

📄 Full report: https://github.com/Dipok009/LASSO-Ridge_Regression-GWAS-Maize_Data/blob/main/Performance%20of%20LASSO%20and%20Ridge%20Regression%20for%20Variable%20Selection.pdf

---

## 📖 Project Overview
Genome-Wide Association Studies (GWAS) are widely used to identify genetic variants associated with complex traits.  
This study investigates **maize flowering time**, a critical adaptive trait, by applying two regularized regression methods:  

- **LASSO Regression (L1 penalty)** – performs variable selection by shrinking some coefficients to zero.  
- **Ridge Regression (L2 penalty)** – shrinks coefficients but keeps all features, capturing broader genetic context.  

The models are compared in terms of feature selection and predictive accuracy on high-dimensional genomic data.  

---

## 📊 Key Findings
- LASSO selected **45 features** at optimal α = 0.1. LASSO helps to identify the most significant SNPs by enforcing sparsity.   
- Ridge retained **4,211 features** at optimal α = 1000. Ridge regression captures more genetic information by retaining many features.    
- **Ridge outperformed LASSO** with slightly lower prediction error:
  - LASSO → MSE = 12.7045, RMSE = 3.5643  
  - Ridge → MSE = 12.2223, RMSE = 3.4960

---

## Dataset  
- **Maize Nested Association Mapping (NAM) population**  
- ~5,000 recombinant inbred lines (RILs) across 25 families  
- **7,393 SNP markers** as predictors  
- Target variable: **days to male flowering (dtoa)**  
- After removing missing values: **4,494 samples × 7,393 features**  

---

## Methodology
1. **Data Preprocessing**  
   - 4,981 samples × 7,393 variables  
   - Missing values removed → 4,494 samples used  
   - Features: SNP markers  
   - Target: days to male flowering (`dtoa`)

2. **Methods/Model**  
   **LASSO Regression**  
      - L1 regularization  
      - Encourages sparsity (zeroes out coefficients)  
      - Selects the most impactful SNPs  

   **Ridge Regression**  
      - L2 regularization  
      - Retains all features but shrinks coefficients  
      - Provides stability in correlated high-dimensional data  

3. **Model Training**  
   - Implemented using `scikit-learn`  
   - Hyperparameter tuning with `GridSearchCV` (5-fold CV)  
   - Evaluation using MSE & RMSE  

4. **Tools Used**  
   - Python, NumPy, Pandas, Scikit-learn, Matplotlib

---

## Results  

| Model  | Selected Features | α (alpha) | MSE     | RMSE   |  
|--------|------------------|-----------|---------|--------|  
| LASSO  | 45               | 0.1       | 12.7045 | 3.5643 |  
| Ridge  | 4211             | 1000      | 12.2223 | 3.4960 |  

- **Ridge regression slightly outperformed LASSO**, achieving lower MSE and RMSE.  
- **LASSO** provided strong feature selection, reducing the dataset to a smaller set of meaningful SNPs.  

---

## Course Info  
- **Course:** STA 6366 – Data Science I  
- **Institution:** Department of Statistics and Data Science, University of Central Florida  
- **Instructor:** [Dr. Rui Xie]  
- **Term:** [Fall 2024]  

---

## Citation  
If you use this work, please cite:  

Deb, Dipok, "Performance of LASSO and Ridge Regression for Variable Selection in Genome-Wide Association Studies of Maize Flowering Time" (2025). Data Science and Data Mining. 42.
https://stars.library.ucf.edu/data-science-mining/42

---

## Contact  
For questions or collaborations, feel free to reach out via **GitHub Issues** or connect on **LinkedIn**.  

