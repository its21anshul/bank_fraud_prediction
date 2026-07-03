# 💳 Fraud Detection Using Machine Learning

An end-to-end Machine Learning project for detecting fraudulent financial transactions using the PaySim dataset. The project covers data cleaning, exploratory data analysis (EDA), feature engineering, model training, threshold tuning, and model deployment preparation.

---

## 📌 Project Overview

Financial fraud causes significant losses for banks and digital payment platforms. This project builds a fraud detection system capable of identifying fraudulent transactions while minimizing false positives.

The project compares multiple machine learning models and optimizes the classification threshold to maximize fraud detection performance.

---

## 🚀 Features

- Data Cleaning
- Exploratory Data Analysis (EDA)
- Feature Engineering
- Handling Imbalanced Data
- Logistic Regression
- Random Forest
- XGBoost (Optional)
- Threshold Optimization
- Model Evaluation
- Model Serialization

---

## 📂 Dataset

**Dataset:** PaySim Mobile Money Transactions

The dataset contains over **6 million** simulated mobile money transactions.

Target variable:

- **isFraud**
  - 0 → Legitimate Transaction
  - 1 → Fraudulent Transaction

Features include:

- step
- type
- amount
- oldbalanceOrg
- newbalanceOrig
- oldbalanceDest
- newbalanceDest
- isFlaggedFraud

---

## 🛠️ Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- XGBoost
- Joblib
- Jupyter Notebook

---

## 📊 Exploratory Data Analysis

Performed:

- Missing value analysis
- Transaction type distribution
- Fraud distribution
- Balance analysis
- Correlation analysis
- Fraud vs Transaction Amount
- Merchant account analysis

Key findings:

- Dataset contains highly imbalanced classes.
- Fraud mainly occurs in TRANSFER and CASH_OUT transactions.
- Merchant destination balances are frequently zero by design.
- Large transaction amounts have a higher fraud probability.

---

## ⚙️ Feature Engineering

Features created:

- High Amount Transaction Flag
- Balance Difference Features
- Balance Error Features
- Encoded Transaction Types

---

## 🤖 Models Trained

### Logistic Regression

- Baseline model
- Class-balanced training

### Random Forest

- Tuned hyperparameters
- Balanced class weights

### XGBoost

- Histogram-based tree growth
- Scale positive weight
- Tuned learning rate
- Optimized tree depth

---

## 📈 Model Evaluation

Evaluation Metrics:

- Accuracy
- Precision
- Recall
- F1 Score
- ROC-AUC
- Precision-Recall Curve
- Confusion Matrix

Since fraud detection is an imbalanced classification problem, Precision-Recall AUC was used as the primary evaluation metric.

---

## 🎯 Threshold Optimization

Instead of using the default threshold (0.50), the model searches for the threshold that achieves:

- Recall ≥ 90%
- Maximum Precision

This significantly reduces false alarms while maintaining high fraud detection.

---

## 💾 Model Saving

The trained model is saved using Joblib.

```python
joblib.dump(model, "fraud_detection_model.pkl")
```

Load later:

```python
model = joblib.load("fraud_detection_model.pkl")
```

---

## 📁 Project Structure

```
Fraud-Detection/
│
├── Analysis.ipynb
├── fraud_detection_model.pkl
├── README.md
├── requirements.txt
└── dataset.csv
```

---

## ▶️ Installation

Clone the repository

```bash
git clone https://github.com/yourusername/Fraud-Detection.git
```

Move into the project directory

```bash
cd Fraud-Detection
```

Install dependencies

```bash
pip install -r requirements.txt
```

Launch Jupyter Notebook

```bash
jupyter notebook
```

---

## 📦 Requirements

```
pandas
numpy
matplotlib
seaborn
scikit-learn
xgboost
joblib
jupyter
```

---

## 📊 Results

The optimized model achieves:

- High fraud recall
- Improved precision through threshold tuning
- Robust performance on highly imbalanced data
- Reduced false positives compared to the default threshold

---

## 🔮 Future Improvements

- LightGBM implementation
- CatBoost comparison
- Hyperparameter optimization using Optuna
- SHAP Explainability
- FastAPI deployment
- Docker support
- Streamlit dashboard
- Real-time fraud prediction API

---

## 📚 Learning Outcomes

This project demonstrates:

- End-to-end ML workflow
- Handling imbalanced datasets
- Feature engineering
- Threshold optimization
- Model evaluation
- Production-ready model saving

---

## 👨‍💻 Author

**Anshul Yadav**

Machine Learning & Data Science Enthusiast

LinkedIn: *(Add your profile)*

GitHub: *(Add your profile)*

---

## ⭐ If you found this project useful, consider giving it a star.
