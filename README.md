# Loan Eligibility Prediction 🏦

**Author:** Mobina Bagha Shanjani  
**Course:** Daneshkar Academy - Data Science Bootcamp  
**Date:** October 2025  

---

## 🎯 Project Overview
The primary objective of this project is to develop a predictive model capable of determining whether a loan application should be approved or rejected based on an applicant’s personal and financial details. 

### Key Goals:
* Identify critical factors influencing loan approval.
* Reduce manual processing time for applications.
* Support fair and consistent data-driven decision-making.

---

## 🛠️ Project Workflow
1. **Exploratory Data Analysis (EDA):** Analyzed feature distributions, correlations, and missing value patterns.
2. **Data Preprocessing:** * Handled missing values (Median for numeric, Mode for categorical).
    * Encoded categorical features.
    * Normalized numeric features for model stability.
3. **Model Building:** Tested and compared multiple algorithms including Logistic Regression, K-Nearest Neighbors (KNN), and MLP (Artificial Neural Networks).
4. **Evaluation:** Measured performance using Precision, Recall, and F1-Score.

---

## 📊 Key Insights from EDA
* **Credit History:** The strongest predictor of loan approval with a **0.56 correlation**.
* **Property Area:** Semi-urban applicants showed a higher likelihood of approval, while rural applicants had a slight negative correlation.
* **Marital Status:** Married applicants demonstrated a higher approval rate (0.09 correlation).

---

## 📈 Model Performance Comparison

| Model | Precision | Recall | F1-Score |
| :--- | :---: | :---: | :---: |
| **Logistic Regression** | 82.89% | **98.44%** | **90.00%** |
| **MLPClassifier (ANN)** | 82.89% | **98.44%** | **90.00%** |
| **K-Nearest Neighbors** | **84.51%** | 93.75% | 88.89% |

### Performance Summary:
* **Logistic Regression & MLP:** These models are the top performers due to superior **Recall**. They are highly effective at identifying eligible applicants with a very low false negative rate (1.08%).
* **KNN:** Shows the highest **Precision** (84.51%), making it better at reducing false positives (incorrect approvals).

---

## 🔍 Critical Analysis (Root Cause)
A major part of this project involved analyzing the **Credit History Imputation** methodology:
* **Suboptimal Imputation:** Using simple mode replacement for missing credit history may introduce systematic bias.
* **Missing Pattern Significance:** Data suggests that missing credit history might not be "Missing Completely at Random" (MCAR). Applicants with no history could represent distinct risk categories (e.g., young professionals or new immigrants) that require specialized assessment.

---

## 📁 Project Structure
* `Data/`: Raw dataset (loan.csv).
* `Notebooks/`: Main analysis and modeling (`loan_approval.ipynb`).
* `research/`: Experimental scripts for imputation and testing.
* `README.md`: Project documentation.

---

## 💻 How to Use
1. Clone the repository:
   ```bash
   git clone [https://github.com/mobinabagha/Loan-Eligibility-Prediction.git](https://github.com/mobinabagha/Loan-Eligibility-Prediction.git)
2. Install required libraries:
    pip install pandas numpy scikit-learn seaborn matplotlib
3. Run the Jupyter Notebook:
    jupyter notebook loan_approval.ipynb