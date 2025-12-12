# diabetesModel
Hera Ali — portfolio project on diabetes data for learning.

# Project 01 — Diabetes Classification (EDA + Baseline Models)

A small end-to-end machine learning project using a diabetes dataset:
- Load + inspect data
- Basic EDA (distributions, correlations)
- Train/test split (with stratification)
- Train multiple classification models
- Compare models using accuracy + confusion-matrix breakdown (TP/TN/FP/FN)
- Pick a “best model” depending on the goal (medical-style tradeoffs)

---

## Project Structure

project_01_health_EDA/
├── data/
│   └── diabetes.csv
├── notebook.ipynb
└── README.md

---

## Dataset

**Target column:** `Class`
- `1` = diabetic (positive class)
- `0` = non-diabetic (negative class)

Class counts (in the full dataset):
- `Class=1`: 225
- `Class=0`: 126

So the dataset is **not perfectly balanced** (more 1s than 0s).

---

## Environment / Setup

This project was run locally using Jupyter (Anaconda).
