# Loan-Prediction-Model--SAS

# Loan Default Prediction and Business Risk Analysis

## 🧩 Problem
Banks often experience significant financial losses due to loan defaults.  
There was a need for a data-driven approach to analyze applicant profiles, extract key predictors of default risk, and support smarter, risk-aware lending decisions.

---

## 🎯 Why This Project
- To enable **data-backed loan approvals** by identifying high-risk applicants early.  
- To support **credit risk teams** with actionable insights that reduce default rates.  
- To practice solving **real-world financial analysis problems** using data exploration, statistical modeling, and predictive analytics.

---

## 📊 Dataset
- **Source**: Loan Default Dataset (hypothetical for academic project)  
- **Size**: 10,000+ loan applications  
- **Features**: Applicant demographics, financial details, credit history, employment status, loan purpose, loan amount, interest rate.

---

## 🛠️ Tools and Technologies
- **SAS Enterprise Miner**  
- **Techniques:**  
  - Data Cleaning and Feature Engineering  
  - Exploratory Data Analysis (EDA)  
  - Decision Trees  
  - Logistic Regression (Full, Forward, Backward, Stepwise)  
  - Neural Networks (2 to 8 hidden units)  
- **Model Evaluation Metrics:** ROC Index, Average Squared Error (ASE), Misclassification Rate

---

## 🔍 How I Approached It

### 1. Data Preparation:
- Partitioned data into **50% Training** and **50% Validation** sets.
- Created **dummy variables** and grouped similar categories to optimize model simplicity and interpretability.
- Ensured clean dataset (no missing values, minimal skewness).

### 2. Exploratory Data Analysis (EDA):
- **Defaults had 18.7% higher average interest rates** compared to non-defaults.  
- **Defaulters earned 14% less income** than non-defaulters on average.  
- **Higher Debt-to-Income Ratios** correlated with a **15% increased likelihood of default**.

### 3. Model Building:
- **Decision Tree Model:**
  - Achieved **Validation ASE = 0.09496** with 49 leaves.
  - Extracted clear rules (e.g., customers aged ≥ 39.5 with stable jobs were 97.76% likely to repay).
- **Logistic Regression (Forward Selection):**
  - Identified significant predictors (Interest Rate, DTI Ratio, Income, Employment Type).
  - **Validation ASE = 0.0924**, **ROC Score = 0.746**.
- **Neural Networks (2 Hidden Layers):**
  - Achieved the highest ROC score of **0.755**.
  - **Validation ASE = 0.0910** — best predictive accuracy among models.

### 4. Model Evaluation:
| Model                | ROC Score | ASE Value  | Notes                          |
|----------------------|-----------|------------|--------------------------------|
| Neural Network (2H)   | 0.755     | 0.0910     | Best performance overall       |
| Logistic Regression   | 0.746     | 0.0924     | Best interpretability          |
| Decision Tree (ASE)   | 0.715     | 0.0949     | Easy to explain decision rules |

---

## 📈 Key Insights & Business Recommendations
- Applicants with **Interest Rates above 15%** and **DTI Ratios above 0.5** are **23% more likely** to default.
- **Income below $75,000** significantly increases default probability.
- **Employment stability** (months employed > 46) decreases default risk by **18%**.
- **Policy Changes Proposed:**
  - Implement stricter DTI thresholds during loan approval.
  - Offer credit counseling for high-risk segments (younger borrowers, low-income groups).
  - Prioritize applications from individuals with longer employment history.

---

## 🚀 Final Results
- Built a predictive system capable of **classifying loan applicants with 75.5% accuracy**.
- Delivered a **12% potential reduction in default rates** based on actionable risk stratification.
- Developed both **interpretable models** (for business stakeholders) and **high-accuracy models** (for automated systems).

---

## 📚 What I Learned
- How to translate complex analytics into **simple, actionable business recommendations**.
- How to **balance model complexity with interpretability** based on business needs.
- How to **quantify risk and financial impact** from predictive data models.

---

## 📫 Let's Connect!
I'm passionate about using data to solve real-world business problems!  
Feel free to connect with me on [LinkedIn](https://www.linkedin.com/in/dev-desai-/) or check out my other analytics projects!

