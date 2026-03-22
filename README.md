# 🧾 Fake Bill Detection using Machine Learning

![Python](https://img.shields.io/badge/Python-3.10-blue)
![scikit-learn](https://img.shields.io/badge/ML-Scikit--Learn-orange)
![Status](https://img.shields.io/badge/Status-Completed-brightgreen)
![Accuracy](https://img.shields.io/badge/Accuracy-99.3%25-success)
![F1 Score](https://img.shields.io/badge/F1%20Score-0.995-success)

---

## 🚀 Project Overview

This project builds a **high-performance fraud detection system** that classifies whether a bill is **genuine or fake** using machine learning.

The focus is not just accuracy, but:

* Minimizing **missed fraud cases (False Negatives)**
* Ensuring **high recall and precision**
* Building a **robust and production-ready ML pipeline**

---

## 🎯 Problem Statement

In fraud detection systems:

* ❌ Missing a fake bill → **High risk (financial loss)**
* ⚠️ False alarm → **Less critical**

👉 Therefore, the model is optimized for:

* **High Recall**
* Strong **F1 Score**

---

## 📂 Dataset

* File: `fake_bills.csv`
* Total Features: 6 (Numerical)

| Feature      | Description          |
| ------------ | -------------------- |
| diagonal     | Bill diagonal length |
| height_left  | Left height          |
| height_right | Right height         |
| margin_low   | Lower margin         |
| margin_up    | Upper margin         |
| length       | Bill length          |

### 🎯 Target Variable

* `is_genuine`

  * `True` → Genuine
  * `False` → Fake

---

## ⚙️ Tech Stack

* **Language:** Python
* **Libraries:**

  * Pandas, NumPy
  * Scikit-learn
  * Imbalanced-learn (SMOTE)
  * Matplotlib, Seaborn

---

## 🧠 Machine Learning Pipeline

```text
Data → Preprocessing → SMOTE → Scaling → Model → Evaluation
```

### Steps:

1. Data Cleaning (handling missing values)
2. Train-Test Split (80/20)
3. Handling Imbalance using **SMOTE**
4. Feature Scaling using **RobustScaler**
5. Model Training (**Logistic Regression**)
6. Hyperparameter Tuning using **GridSearchCV**
7. Evaluation using multiple metrics

---

## 🏆 Final Model

### ✅ Logistic Regression + SMOTE (Best Performing Model)

**Best Hyperparameters:**

* `C = 10`
* `penalty = l2`
* `solver = lbfgs`

---

## 📊 Model Performance

| Metric    | Score     |
| --------- | --------- |
| Accuracy  | **0.993** |
| Precision | **0.995** |
| Recall    | **0.995** |
| F1 Score  | **0.995** |

---

## 📉 Confusion Matrix

```
[[ 85   1]
 [  1 206]]
```

### 🔍 Interpretation:

* Only **1 fake bill missed** ✅
* Only **1 false alarm** ✅
* Extremely balanced performance

---

## 📈 ROC Curve

* **AUC Score: 1.00**
* Indicates near-perfect class separation

---

## 📊 Precision-Recall Curve

* **PR AUC: 1.00**
* Critical for imbalanced datasets
* Confirms strong fraud detection capability

---

## 🔍 Model Comparison

| Model                       | F1 Score   |
| --------------------------- | ---------- |
| Logistic Regression + SMOTE | **0.9928** |
| Random Forest + SMOTE       | 0.9938     |
| XGBoost + SMOTE             | 0.9912     |
| Gradient Boosting           | 0.9902     |

### ✅ Final Choice Reason:

Although Random Forest had slightly higher CV score, Logistic Regression was chosen because:

* More **stable**
* Less **overfitting risk**
* More **interpretable** (important in fraud systems)

---

## 💡 Key Insights

* Simpler models can outperform complex ones on structured data
* SMOTE significantly improves minority class detection
* RobustScaler handles outliers better than StandardScaler
* Cross-validation is essential for reliable model selection

---

## ⚠️ Challenges Faced

* Numerical instability with PowerTransformer
* Class imbalance
* Avoiding data leakage with SMOTE

---

## 🚀 How to Run

```bash
git clone https://github.com/your-username/fake-bill-detection.git
cd fake-bill-detection
pip install -r requirements.txt
python main.py
```

---

## 🔮 Future Improvements

* Threshold tuning for business optimization
* Deploy using **Flask / Streamlit**
* Add real-time prediction API
* Test on larger and real-world datasets

---

## 📬 Author

**Durgesh Surnkar**

---

## ⭐ Support

If you found this project useful:

* ⭐ Star this repository
* 🍴 Fork it
* 📢 Share with others

---
