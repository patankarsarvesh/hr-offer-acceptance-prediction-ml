# hr-offer-acceptance-prediction-ml

**Short description**  
Predict whether a candidate will **Join** or **Not Join** after receiving an offer. This student-friendly project covers data cleaning, EDA, encoding, handling class imbalance (SMOTE), and a baseline ML model (Logistic Regression) with evaluation (ROC/AUC).

---

## Project objective
Build a binary classification model that predicts the final joining status:

- `0` → Joined  
- `1` → Not Joined

This helps HR teams identify candidates who may not accept offers and plan follow-ups.

---

## Dataset
The dataset contains candidate and offer-related information such as notice period, expected vs offered hike, DOJ extension, candidate source, relocation, band, experience, age, gender, location, and final joining status.

> **Note:** Put the dataset file (example: `IMB553-XLS-ENG.xlsx`) in the repository root or a `data/` folder so the notebook can load it easily.

---

## Main steps performed
1. **Load data** — read the Excel file and inspect rows/columns.  
2. **Clean & format** — normalized column names, removed ID column, handled missing values (dropped for this version).  
3. **Exploratory Data Analysis (EDA)** — count plots, category vs. status plots, correlation heatmap, target distribution.  
4. **Feature encoding** — converted categorical features to one-hot/dummy variables.  
5. **Handle imbalance** — used SMOTE to create a balanced training dataset.  
6. **Train-test split** — 80/20 split on the balanced dataset.  
7. **Modeling** — trained a Logistic Regression baseline.  
8. **Evaluation** — confusion matrix, classification report, ROC curve and AUC.

---

## Quick results summary
- The dataset was imbalanced (majority Joined).  
- SMOTE balanced the classes before model training.  
- Logistic Regression baseline produced a usable ROC AUC (example ~0.82 on training evaluation).  
- The ROC curve provides a visual of classifier performance and can be used to pick an operating threshold.

---

## Files in this repository
