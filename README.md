# 🤖 Loan Default Prediction – SAS Analytics Project

## 📘 Overview  
This project explores the factors that drive **loan defaults** using advanced analytical modeling in **SAS Enterprise Miner**. Through statistical exploration, decision trees, regression, and neural networks, we identify the key predictors and develop robust classification models to help financial institutions mitigate default risk and enhance lending strategies.

---

## 📊 Dataset  
- **Name**: Loan Default Dataset  
- **Observations**: Consumer-level loan data with features including income, loan amount, interest rate, employment history, credit score, DTI ratio, marital status, education, and more  
- **Target Variable**: `Default` (1 = Defaulted, 0 = Non-default)

---

## 🧠 Goals  
- Predict likelihood of loan default using multiple modeling techniques  
- Identify and rank the most influential features affecting default risk  
- Build business recommendations for credit risk management  

---

## 🔍 Key Insights from Statistical Exploration  
- **Higher Interest Rates** → Significantly more defaults (Default avg: 15.88% vs Non-default: 13.19%)  
- **Lower Income** and **higher Loan Amounts** → Strong indicators of default  
- **Shorter Employment Duration** and **Higher DTI Ratios** → Increase default probability  
- **Younger Age** groups show marginally higher default rates  
- **Credit Scores** are lower for defaulters, but effect size is small  
- **Loan Term** showed no significant predictive difference (uniform mean = 36 months)

---

## 🌲 Decision Tree Modeling  
- Created 3 models (ASE Tree, MAX Tree, MIS Tree)  
- **Best Performing Model**: **ASE Tree**  
  - **Validation ASE**: 0.09496  
  - Balanced complexity (49 leaves) and accuracy  
- **Insights from Leaves**:  
  - **Low risk group**: Age ≥ 39.5, interest rate < 12.9%, 46+ months employed, has dependents → **97.76% non-default**  
  - **High risk group**: Age < 39.5, interest > 15.04%, income < 35k, loan > 152k → **50.49% default**

---

## 📉 Regression Modeling  
- Built **4 regression models**: Full, Forward, Backward, Stepwise  
- **Best Model Chosen**: **Raw Forward Regression** (based on ASE and interpretability)

### 📌 Top Predictors (based on Wald Chi-Square):
- Age  
- Interest Rate  
- Income  
- DTI Ratio  
- Credit Score  
- Months Employed  
- Employment Type  
- Co-signer  
- Dependents  
- Education  

### 🎯 Odds Ratio Highlights:
- **Every 1% increase in DTI** → **+36.6% odds of default**  
- **Full-time employment** reduces odds by 36.9% vs unemployed  
- **Having dependents** and **no co-signer** both increase default odds by ~30%  
- **Older age** → 3.9% decrease in default odds per year

---

## 🧠 Neural Networks  
- Created 9 models (2H to 8H hidden layers)  
- All models **converged successfully**, except 5H (did not converge)  
- **Best Performing Model**: **Raw NN 2H**  
  - **ROC Index**: 0.755 (highest)  
  - **ASE**: 0.09105 (lowest)  
  - **Misclassification Rate**: ~11.3%  

### 🧾 Model Comparison Summary:
| Model            | ROC Index | ASE     | Notes                               |
|------------------|-----------|---------|-------------------------------------|
| Raw NN 2H        | 0.755     | 0.09105 | Best accuracy, low complexity       |
| Forward Reg      | 0.746     | 0.0924  | Interpretable, good baseline model  |
| ASE Tree         | 0.715     | 0.09496 | Interpretable with rule-based output|
| Misclass Tree    | 0.642     | 0.09825 | Underfits data                      |
| Raw NN 5H        | —         | —       | Did not converge                    |

---

## 📌 Business Recommendations  
- **Risk Profiling**: Use age, interest rate, DTI, income, and employment type to build a credit risk score  
- **Stricter Thresholds**: On high DTI and interest loans  
- **Require Co-signers**: For young or low-income applicants  
- **Leverage Neural Networks**: For high-volume automated loan approvals  
- **Use Logistic Regression**: In contexts needing high transparency (e.g., regulatory compliance)

---

## 🛠 Tools Used  
- **SAS Enterprise Miner**  
- **SAS Statistical Explorer, Regression, Decision Tree, Neural Network Nodes**  
- **Model Comparison Node** for final selection

---

## 🏁 Final Takeaway  
The combination of models provides both accuracy and interpretability. While the **Raw NN 2H model** is the most accurate, the **Forward Regression model** remains critical for stakeholder explanation. Together, they offer a balanced solution for real-time loan screening and long-term credit policy improvements.

---

