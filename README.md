# 🔍 OpenFraudLabs - AI-Powered Financial Security
**Mission**: Build accessible fraud detection tools for African SMEs using open-source AI.

## 🚀 Quick Start
```bash

pip install -r requirements.txt
python train.py --data_path ../africa-fraud-data/synthetic_transactions.csv


# Our latest Model : Fraud Detection Using Sampling Techniques and XGBoost

published on : SSRN 

# Fraud Detection Using Sampling Techniques and XGBoost

This Model contains code and analysis for evaluating various sampling techniques to handle class imbalance in credit card fraud detection using the XGBoost classifier.

---

## Project Overview

Credit card fraud detection suffers from severe class imbalance, making it difficult for machine learning models to effectively detect fraudulent transactions. This project empirically compares several sampling methods—Random Under Sampling (RUS), SMOTE, ADASYN, Tomek Links, and SMOTE combined with Tomek Links—to assess their impact on the performance of an XGBoost classifier.

The analysis uses the publicly available Kaggle Credit Card Fraud dataset and evaluates models based on precision, recall, F1-score, and ROC AUC.

---

## Dataset

- Kaggle Credit Card Fraud Detection dataset  
- Source: [https://www.kaggle.com/mlg-ulb/creditcardfraud](https://www.kaggle.com/mlg-ulb/creditcardfraud)  
- Contains 284,807 transactions, with 492 labeled fraud cases (~0.172% fraud rate)

---

## Sampling Techniques Evaluated

- **No Sampling:** Baseline with original imbalanced data  
- **Random Under Sampling (RUS):** Randomly reduces majority class samples  
- **SMOTE:** Synthetic Minority Oversampling Technique  
- **ADASYN:** Adaptive Synthetic Sampling  
- **Tomek Links:** Removes borderline majority samples to clean data  
- **SMOTE + Tomek Links:** Combination of oversampling and cleaning  

---

## Methodology

- Data preprocessing includes scaling of the `Amount` feature using z-score normalization.  
- Train/test split with stratification to preserve class balance (80% train, 20% test).  
- Sampling applied only to training data.  
- Fixed XGBoost hyperparameters used for fair comparison.  
- Evaluation metrics: Precision, Recall, F1-score, and AUC.

---

## Usage

1. Clone the repository:

   ```bash

| Method             | Precision | Recall | F1   | AUC  |
| ------------------ | --------- | ------ | ---- | ---- |
| No Sampling        | 0.92      | 0.83   | 0.87 | 0.98 |
| RandomUnderSampler | 0.04      | 0.92   | 0.07 | 0.98 |
| SMOTE              | 0.27      | 0.90   | 0.41 | 0.98 |
| ADASYN             | 0.26      | 0.90   | 0.40 | 0.98 |
| TomekLinks         | 0.82      | 0.78   | 0.80 | 0.95 |
| SMOTE + Tomek      | 0.60      | 0.79   | 0.68 | 0.96 |


License
This project is licensed under the MIT License - see the LICENSE file for details.

Acknowledgements
Kaggle for providing the Credit Card Fraud dataset

The maintainers of imbalanced-learn and XGBoost Python libraries

Contact
For questions or collaboration, please contact:
Ayodele Odugbile
OpenFraudLabs Research Unit, Akure, Nigeria

Email: drolalekan.ayodele@gmail.com

References
Chawla, N.V., et al. (2002). SMOTE: Synthetic Minority Over-sampling Technique. Journal of Artificial Intelligence Research.

Bhattacharyya, S., et al. (2011). Data mining for credit card fraud: A comparative study. Decision Support Systems.

Chen, T., & Guestrin, C. (2016). XGBoost: A scalable tree boosting system. KDD.

He, H., et al. (2008). ADASYN: Adaptive synthetic sampling approach for imbalanced learning. IEEE International Joint Conference on Neural Networks.

Kaggle Dataset: https://www.kaggle.com/mlg-ulb/creditcardfraud



   git clone https://github.com/yourusername/fraud-detection-sampling-xgboost.git
   cd fraud-detection-sampling-xgboost
