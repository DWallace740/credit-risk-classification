# Credit Risk Classification

## Overview of the Analysis
This project focuses on analyzing the creditworthiness of borrowers using **logistic regression**. A dataset of historical lending activity from a peer-to-peer lending service was used to build and evaluate a model that predicts whether a loan is **healthy (0)** or **high-risk (1)**.

## Results
### **1. Model Performance Metrics**
#### **Confusion Matrix**
```
[[14924   77]  
 [   31  476]]
```
- **True Negatives (TN):** 14,924 (Healthy loans correctly classified)
- **False Positives (FP):** 77 (Healthy loans incorrectly classified as high-risk)
- **False Negatives (FN):** 31 (High-risk loans incorrectly classified as healthy)
- **True Positives (TP):** 476 (High-risk loans correctly classified)

#### **Classification Report**
| Label | Precision | Recall | F1-Score | Support |
|--------|------------|--------|---------|---------|
| **0 (Healthy Loan)** | 1.00 | 0.99 | 1.00 | 15,001 |
| **1 (High-Risk Loan)** | 0.86 | 0.94 | 0.90 | 507 |

- **Accuracy:** 0.99
- **Macro Avg:** Precision = 0.93, Recall = 0.97, F1-score = 0.95
- **Weighted Avg:** Precision = 0.99, Recall = 0.99, F1-score = 0.99

### **2. Key Findings**
- The model has an overall accuracy of **99%**, making it highly effective at classifying loans.
- The model performs **exceptionally well for predicting healthy loans (0)**, with a precision and recall close to **1.00**.
- The model's **recall for high-risk loans (1) is 0.94**, meaning it correctly identifies most of the high-risk loans.
- **Precision for high-risk loans (1) is 0.86**, indicating that **14% of predicted high-risk loans were actually healthy loans**.

## Summary & Recommendation
### **Strengths:**
- High overall accuracy (**99%**).
- Strong classification of **healthy loans**.
- Good recall for **high-risk loans**, meaning most risky loans are correctly identified.

### **Weaknesses:**
- **Precision for high-risk loans is lower (0.86)** → Some healthy loans are misclassified as high-risk.
- The dataset is likely imbalanced, which can affect performance for the minority class (high-risk loans).

### **Recommendations:**
- Consider balancing the dataset using **oversampling techniques (e.g., SMOTE) or undersampling.**
- Test different models, such as **Random Forest or XGBoost**, to see if they improve classification performance.
- Fine-tune hyperparameters to optimize the logistic regression model further.

## Technologies Used
- **Python**
- **Pandas** for data manipulation
- **Scikit-Learn** for machine learning modeling
- **Jupyter Notebook** for development

## Repository Structure
```
📂 Credit-Risk-Classification
│── 📂 Credit_Risk
│   ├── credit_risk_classification.ipynb  # Jupyter Notebook with analysis
│   ├── lending_data.csv                   # Dataset used for modeling
│   ├── README.md                           # Project documentation
```

## How to Run
1. Clone the repository:
   ```bash
   git clone https://github.com/DWallace740/credit-risk-classification.git
   ```
2. Navigate to the project directory:
   ```bash
   cd credit-risk-classification/Credit_Risk
   ```
3. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```
4. Run the Jupyter Notebook:
   ```bash
   jupyter notebook credit_risk_classification.ipynb
   ```

## Resources and Support

ChatGPT (AI Assistant): For guidance on code logic, debugging, structuring the scripts and formatting my Readme file.

All external resources used are listed here for transparency.

## Author
Daena Wallace 

