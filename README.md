#  Credit Card Fraud Detection  
## Model Selection Under Extreme Class Imbalance

---

##  Project Overview

Fraud detection is one of the most challenging machine learning problems due to extreme class imbalance.

In this dataset:
- Total transactions: 284,807
- Fraud cases: 492
- Fraud rate: ~0.17%

A model predicting all transactions as non-fraud achieves **99.8% accuracy** — yet detects zero fraud.

This project focuses on selecting the right evaluation strategy and modeling approach under extreme imbalance.

---

##  Objective

To compare supervised and unsupervised techniques for fraud detection and determine:

> Should fraud detection be treated as a classification problem or anomaly detection problem?

---

##  Dataset

The dataset used in this project is publicly available on Kaggle:

🔗 https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud

Due to GitHub file size limits, the dataset is not included in this repository.

### How to Use:

1. Download the dataset from Kaggle
2. Place `creditcard.csv` in the root directory of this project
3. Run the notebook

---

##  Dataset Information

- PCA-transformed features: V1–V28  
- Additional features: Time, Amount  
- Target variable:  
  - 0 → Normal Transaction  
  - 1 → Fraudulent Transaction  

Dataset is highly imbalanced and requires imbalance-aware evaluation.

---

##  Models Implemented

### 1️⃣ Random Forest (Supervised Learning)
- Class-weight balancing applied
- Probability outputs used for ROC & PR analysis

### 2️⃣ Isolation Forest (Unsupervised Anomaly Detection)

### 3️⃣ Local Outlier Factor (LOF)

### 4️⃣ DBSCAN (Density-Based Clustering)

---

##  Evaluation Metrics

Because of extreme imbalance, accuracy is NOT used as primary metric.

Instead, evaluation focuses on:

- Recall (Fraud Detection Rate)
- Precision
- F1 Score
- ROC-AUC
- Precision-Recall AUC
- Confusion Matrix

---

##  Key Insights

✔ Accuracy is misleading in imbalanced datasets  
✔ Precision-Recall curve is more informative than ROC in rare-event detection  
✔ Supervised learning significantly outperforms anomaly detection when labels exist  
✔ Fraud detection is a cost-sensitive classification problem  

---

##  Visualizations Included

- Class distribution analysis  
- Confusion Matrix  
- ROC Curve  
- Precision-Recall Curve  
- Feature Importance (Random Forest)  

---

##  Final Conclusion

When labeled fraud data is available, supervised models like Random Forest outperform unsupervised anomaly detection techniques.

However, model selection should align with business cost considerations:

- False Negatives → Financial loss  
- False Positives → Customer dissatisfaction  

Fraud detection is not just a modeling task — it is a risk management decision system.

---

##  Tech Stack

- Python
- Pandas
- NumPy
- Scikit-learn
- Matplotlib
- Seaborn


---

## 📬 Connect With Me

If you are working in:
- Risk Analytics
- Fraud Detection
- Machine Learning
- Financial Modeling

I would love to connect and discuss ideas.

---

⭐ If you found this project interesting, feel free to star the repository.
