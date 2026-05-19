# 🚢 Titanic Survival Prediction — Machine Learning Classification Project

![Python](https://img.shields.io/badge/Python-3.9+-blue?style=flat&logo=python)
![Scikit-learn](https://img.shields.io/badge/Scikit--learn-1.3+-orange?style=flat&logo=scikit-learn)
![Pandas](https://img.shields.io/badge/Pandas-2.0+-blueviolet?style=flat&logo=pandas)
![Status](https://img.shields.io/badge/Status-Completed-brightgreen?style=flat)

---

## 📌 Project Overview

This project solves the classic **Titanic Survival Prediction** problem — predicting whether a passenger survived the Titanic disaster based on features like age, gender, passenger class, and more.

It covers a complete **binary classification pipeline** with proper EDA, feature engineering, model comparison, and evaluation.

> Built as part of my Data Science & ML portfolio to demonstrate classification modelling and data analysis skills.

---

## 🎯 Objective

- Predict whether a passenger **survived (1) or did not survive (0)**
- Perform thorough EDA to understand what factors influenced survival
- Compare multiple classification algorithms and select the best one

---

## 📂 Project Structure

```
Titanic-Survival-Prediction/
│
├── data/
│   ├── train.csv                  # Training dataset
│   └── test.csv                   # Test dataset
│
├── notebooks/
│   ├── titanic-eda-and-prediction.ipynb   # EDA & Feature Engineering + Model Training
│
├── requirements.txt               # Python dependencies
├── .gitignore                     # Files to ignore
└── README.md                      # Project documentation
```

---

## 🔍 Dataset

- **Source:** [Kaggle — Titanic: Machine Learning from Disaster](https://www.kaggle.com/competitions/titanic)
- **Training Records:** 891 passengers
- **Test Records:** 418 passengers
- **Target:** `Survived` — 0 = Did not survive, 1 = Survived

### Key Features

| Feature | Description |
|---|---|
| `Pclass` | Passenger class (1st, 2nd, 3rd) |
| `Sex` | Gender of passenger |
| `Age` | Age in years |
| `SibSp` | Number of siblings/spouses aboard |
| `Parch` | Number of parents/children aboard |
| `Fare` | Passenger fare paid |
| `Embarked` | Port of embarkation |

---

## 🛠️ Tech Stack

| Category | Tools / Libraries |
|---|---|
| Language | Python 3.9+ |
| Data Processing | Pandas, NumPy |
| Visualization | Matplotlib, Seaborn |
| Machine Learning | Scikit-learn |
| Environment | Jupyter Notebook |

---

## ⚙️ Workflow

### 1. Exploratory Data Analysis (EDA)
- Survival rate by gender, passenger class, age group
- Missing value analysis (Age, Cabin, Embarked)
- Visualized correlations and survival distributions
- Identified key patterns: women and 1st class passengers had higher survival rates

### 2. Data Preprocessing
- Filled missing `Age` values with median grouped by Pclass and Sex
- Filled missing `Embarked` with mode
- Dropped `Cabin` column (>77% missing)
- Encoded `Sex` and `Embarked` with Label Encoding

### 3. Feature Engineering
- Created `FamilySize` = SibSp + Parch + 1
- Created `IsAlone` flag for solo travellers
- Extracted `Title` from passenger names (Mr, Mrs, Miss, etc.)
- Binned `Age` and `Fare` into categories

### 4. Model Building & Comparison

| Model | Accuracy | Precision | Recall | F1 Score |
|---|---|---|---|---|
| Logistic Regression | 80.2% | 0.79 | 0.74 | 0.76 |
| Decision Tree | 78.5% | 0.76 | 0.72 | 0.74 |
| **Random Forest** | **83.6%** | **0.82** | **0.79** | **0.80** |
| SVM | 82.1% | 0.81 | 0.77 | 0.79 |

✅ **Random Forest selected as final model** for best overall performance.

### 5. Model Evaluation
- Confusion matrix analysis
- ROC-AUC curve
- Cross-validation (5-fold) to check for overfitting

---

## 📊 Key Visualizations

- 👩‍👦 Survival rate by gender and passenger class
- 📊 Age distribution of survivors vs non-survivors
- 🔥 Feature correlation heatmap
- 📉 ROC-AUC curve
- 🌲 Random Forest feature importance chart

---

## 🚀 How to Run This Project

### Step 1 — Clone the repository
```bash
git clone https://github.com/sanketmahajan023/Titanic-Survival-Prediction.git
cd Titanic-Survival-Prediction
```

### Step 2 — Install dependencies
```bash
pip install -r requirements.txt
```

### Step 3 — Open the notebooks
```bash
jupyter notebook
```
Run `tianic-eda-and-prediction.ipynb`

---

## 📈 Results

- **Best Model:** Random Forest Classifier
- **Accuracy:** 83.6%
- **F1 Score:** 0.80

---

## 💡 Key Learnings

- Gender and passenger class are the strongest predictors of survival
- Feature engineering (FamilySize, Title extraction) significantly improved accuracy
- Random Forest handles non-linear relationships and feature interactions better than linear models
- Cross-validation is essential to avoid overfitting on small datasets

---

## 🔮 Future Improvements

- [ ] Deploy as a Streamlit app where users input passenger details and get survival prediction
- [ ] Apply SHAP values for model explainability
- [ ] Try XGBoost and LightGBM for performance improvement
- [ ] Hyperparameter tuning with GridSearchCV

---

## 👤 Author

**Sanket Mahajan**
📧 sanketmahajan7049@gmail.com
🔗 [LinkedIn](https://www.linkedin.com/in/sanketdmahajan)
🐙 [GitHub](https://github.com/sanketmahajan023)

---

## 📄 License

This project is open source and available under the [MIT License](LICENSE).

---

⭐ If you found this project helpful, please give it a star!
