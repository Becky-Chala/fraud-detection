# Fraud Detection with Machine Learning (Week 8 & 9 Challenge)

## 📌 Overview

This project is part of the **10 Academy AI Mastery Program** (Weeks 8 & 9).
The objective is to **detect fraudulent transactions** in e-commerce and banking datasets using machine learning.

We:

* Preprocessed and engineered features
* Built and evaluated machine learning models
* Applied **model explainability (SHAP)** to interpret the predictions

Fraud detection is highly imbalanced (fraud cases are very rare), so we emphasize evaluation metrics like **AUC-PR** and **F1-score**, not just accuracy.

---

## 🗂️ Project Structure

```text
├── data/                  # (ignored in git) raw and processed data files
├── notebooks/
│   ├── task1and2.ipynb     # Data preprocessing, model training
│   └── task3_shap.ipynb    # Model explainability
├── models/                # Saved models (ignored in git)
├── requirements.txt        # Python dependencies
├── .gitignore              # Ignore large data and temp files
└── README.md               # Project documentation
```

---

## 🗂️ Datasets

1. **Fraud\_Data.csv** – e-commerce transactions with features like device, browser, signup time, purchase time, IP, etc.
2. **creditcard.csv** – anonymized credit card transactions with PCA-transformed features (V1–V28).
3. **IpAddress\_to\_Country.csv** – IP-to-country mapping for geolocation features.

> ⚠️ These data files are excluded from Git (see `.gitignore`) due to size/sensitivity.

---

## ⚙️ Installation

Clone the repo and install dependencies:

```bash
git clone https://github.com/yourusername/fraud-detection.git
cd fraud-detection
pip install -r requirements.txt
```

Dependencies (see `requirements.txt`):

* `pandas`, `numpy`
* `scikit-learn`
* `matplotlib`
* `shap`
* *(optional)* `imbalanced-learn`, `seaborn`

---

## 🚀 Usage

### 1. Data Preprocessing & Model Training

Open the notebook:

```bash
jupyter notebook notebooks/task1and2.ipynb
```

* Cleans and preprocesses the datasets
* Handles missing values, duplicates, and feature engineering
* Applies scaling & resampling for class imbalance
* Trains and evaluates models:

  * Logistic Regression (baseline)
  * Random Forest (ensemble, selected as best)

### 2. Model Explainability

Open the notebook:

```bash
jupyter notebook notebooks/task3_shap.ipynb
```

* Loads the best-performing model
* Uses **SHAP** (Shapley Additive Explanations)
* Produces:

  * **Summary Plot** – global feature importance
  * **Bar Plot** – ranking by mean SHAP value
  * **Waterfall & Decision Plots** – local explanations for single transactions

---

## 📊 Results

* **Best Model:** Random Forest on Fraud\_Data
* **Key Metrics:**

  * F1-score (fraud class)
  * AUC-PR (robust to imbalance)
* **Key Drivers of Fraud (from SHAP):**

  1. **Time\_since\_signup** – very short time between signup and purchase increases fraud likelihood
  2. **Purchase\_value** – unusually high amounts often flagged
  3. **Device/Browser mismatch** – fraudsters frequently switch environments
  4. **Velocity/frequency features** – abnormal transaction patterns

---

## 📞 Deliverables

* **Notebooks:** Clean, reproducible Jupyter notebooks for each task
* **Visualizations:** SHAP plots for interpretability
* **Documentation:** This README, `.gitignore`, and requirements

---

## 👩‍💻 Authors

* \[Your Name] – Data Scientist @ 10 Academy AI Mastery
* Tutors: Mahlet, Rediet, Kerod, Rehmet

---

## 📜 License

This project is for educational purposes as part of 10 Academy. Not for production use.
