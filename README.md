# Diabetes Classification (ML Models Comparison)

This is a small learning/portfolio project where I trained multiple ML models to predict diabetes (binary classification) and compared them using accuracy + confusion matrix metrics, with goal-based evaluation.

## Dataset
- File: `data/diabetes.csv`
- Target: `Class` (0 = non-diabetic, 1 = diabetic)

## What I did
- Basic EDA (distributions, correlations)
- Train/test split with stratification
- Scaling where appropriate (fit on train only → avoid leakage)
- Trained and compared:
  - Logistic Regression
  - KNN
  - Decision Tree
  - Random Forest
  - SVM (Linear, RBF)
  - XGBoost

## Results (test set)
| Model | Accuracy | TP | TN | FP | FN |
|------|----------|----|----|----|----|
| Logistic Regression | 0.9296 | 45 | 21 | 4 | 1 |
| KNN | 0.8873 | 46 | 17 | 8 | 0 |
| Decision Tree | 0.8732 | 42 | 20 | 5 | 4 |
| Random Forest | 0.9577 | 44 | 24 | 1 | 2 |
| SVM (Linear) | 0.8873 | 43 | 20 | 5 | 3 |
| SVM (RBF) | 0.9577 | 45 | 23 | 2 | 1 |
| XGBoost | 0.8169 | 46 | 12 | 13 | 0 |

## Goal-based takeaway
- If the priority is **minimizing false negatives (FN)**: KNN / XGBoost performed best here (FN = 0) but at the cost of more false positives.
- If the priority is a **balanced medical model**: SVM (RBF) and Random Forest performed strongly with high accuracy and low FP/FN.

## How to run
```bash
pip install -r requirements.txt
jupyter notebook
