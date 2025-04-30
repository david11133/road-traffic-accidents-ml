# 🚗 Road Traffic Accidents - Severity Classification

This project explores, cleans, and models a dataset of road traffic accidents in Ethiopia, aiming to predict Accident Severity based on various features related to drivers, vehicles, and road conditions.

## 📁 Project Structure

```r
data/
├── raw/                  <- Original dataset
│   └── RTA Dataset.csv
├── processed/            <- Cleaned and preprocessed dataset
│   └── RTA_cleaned.csv

notebooks/
├── 01_data_exploration.ipynb         <- Initial data exploration & visualizations
├── 02_preprocessing_and_models.ipynb <- Preprocessing, encoding, and data cleaning
├── 03_modeling.ipynb                 <- ML modeling and evaluation

README.md                              <- You're here!

```

---

## 🧠 What’s Inside the Notebooks?

### 📊 01 - Data Exploration
- Loads and inspects the dataset.
- Visualizes missing values, class imbalance, and feature distributions.
- Key Insight: The data is **heavily imbalanced**, with 85% of cases being “Slight Injury.”

### 🧼 02 - Preprocessing
- Drops irrelevant or sparse columns.
- Fills missing values.
- Encodes categorical variables with `LabelEncoder`.
- Handles outliers via clipping.
- Saves a clean version of the dataset to `data/processed`.

### 🤖 03 - Modeling
- Applies **SMOTE** to balance classes.
- Trains and evaluates three classifiers:
  - **Random Forest**
  - **Support Vector Machine**
  - **Naive Bayes**
- Random Forest performed best with an accuracy of **~87%**.

---

## 🧪 Model Performance Summary

| Model           | Accuracy |
|----------------|----------|
| Random Forest  | 87.4%    |
| SVM            | 71.8%    |
| Naive Bayes    | 44.3%    |

> 📌 Note: Class imbalance was a major issue, and we handled it with SMOTE during model training.

---

## 🛠️ How to Run

1. Clone the repo.
2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```
3. Open the notebooks in Jupyter or VSCode.
4. Follow along from 01_data_exploration.ipynb to 03_modeling.ipynb.

---

📌 Dataset Info
- Source: RTA Dataset (assumed from data.gov.et)
- Size: ~12,000 records
- Target Variable: Accident_severity
   - Classes: Slight Injury, Serious Injury, Fatal Injury

 ---
 
🙌 Credits
Built for learning and experimenting with real-world classification problems using imbalanced data.
