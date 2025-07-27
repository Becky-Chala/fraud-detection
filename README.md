# fraud-detection
# 🛡️ Fraud Detection Preprocessing (Task 1)

This repository contains preprocessing and exploratory data analysis (EDA) for building fraud detection models. The project is part of Adey Innovations Inc.’s initiative to enhance detection of fraudulent e-commerce and credit card transactions.

The **`task1.ipynb`** notebook includes:

* Data cleaning
* Exploratory Data Analysis (EDA)
* Merging geolocation data
* Feature engineering
* Handling class imbalance with SMOTE
* Feature scaling

---

## 📂 Project Structure

```
fraud-detection/
│
├── data/                # Raw datasets (ignored by git)
│   ├── Fraud_Data.csv
│   ├── IpAddress_to_Country.csv
│   └── creditcard.csv
│
├── .venv/               # Virtual environment (ignored by git)
│
├── task1.ipynb          # Task 1 notebook: preprocessing + EDA
├── .gitignore           # Ignores .venv, data, and temp files
└── README.md            # This file
```

---

## 🚀 Setup Instructions

1. **Clone the repository**

   ```bash
   git clone https://github.com/your-username/fraud-detection.git
   cd fraud-detection
   ```

2. **Create a virtual environment**

   ```bash
   python -m venv .venv
   source .venv/bin/activate  # Linux/Mac
   .venv\Scripts\activate     # Windows
   ```

3. **Install dependencies**

   ```bash
   pip install -r requirements.txt
   ```

4. **Download datasets**
   Place `Fraud_Data.csv`, `IpAddress_to_Country.csv`, and `creditcard.csv` in the `data/` folder.

---

## 📊 Features in Task 1

* **Missing Value Handling**: Checked and confirmed no missing values in all datasets.
* **Data Cleaning**: Removed duplicates, corrected data types (e.g., timestamps).
* **EDA**:

  * Class distribution visualization
  * Age and purchase value histograms
  * Time-based transaction patterns
  * Bivariate analysis with fraud class
* **Geolocation Analysis**: Mapped IP addresses to countries using interval matching.
* **Feature Engineering**:

  * Transaction frequency and velocity
  * Time-based features (hour\_of\_day, day\_of\_week, time\_since\_signup)
* **Class Imbalance Handling**: Applied SMOTE for oversampling.
* **Scaling**: Standardized numeric features using StandardScaler.

---

## 📦 Dependencies

* Python 3.8+
* pandas
* numpy
* matplotlib
* seaborn
* scikit-learn
* imbalanced-learn

---

## 🔥 Notes

* `.venv/` and `data/` are ignored by git (see `.gitignore`).
* Only code and configuration files are versioned.

---

## 📝 License

MIT License © Adey Innovations Inc.
