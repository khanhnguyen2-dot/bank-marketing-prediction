# Bank Marketing Prediction — ML Classification

**Group 5** · Class **DS67B** · National Economics University (NEU – College of Technology)  
Members: **Nguyễn Thị Ngọc Khánh** · **Chu Khánh Ly** · **Đặng Nguyễn Thảo My**  
Supervisor: Dr. **Lương Văn Thiện** · Hanoi, December 2025

---

## Overview

This project builds and compares machine learning classification models to predict whether a bank customer will subscribe to a term deposit following a marketing campaign.

**Dataset:** [UCI Bank Marketing Dataset](https://archive.ics.uci.edu/ml/datasets/Bank+Marketing) — 41,188 records, 20 features covering customer demographics, financial profile, campaign history, and macroeconomic indicators.

**Best model:** LightGBM

---

## Models Compared

| Model | Notes |
|---|---|
| Random Forest | Ensemble of decision trees |
| Gradient Boosting | Sequential boosting |
| XGBoost | Optimized gradient boosting |
| **LightGBM** | **Best overall performance** |

---

## Key Findings

- **LightGBM** delivered the strongest and most stable performance across all metrics
- Top predictive features: `duration` (call length), `euribor3m`, `emp.var.rate`, and prior contact history
- Class imbalance was a key challenge — addressed through evaluation metrics beyond accuracy (F1, ROC-AUC)

---

## Workflow

1. **EDA** — distribution plots, correlation analysis, feature inspection
2. **Preprocessing** — handling missing values, encoding categoricals, outlier treatment
3. **Feature Selection** — correlation-based and importance-based filtering
4. **Model Training** — train/test split, cross-validation
5. **Evaluation** — Accuracy, Precision, Recall, F1-score, ROC-AUC, Confusion Matrix

---

## Repository Structure

```
bank-marketing-prediction/
├── code/
│   └── Marketing_Data_Analysis_in_Banking.ipynb   # main notebook
├── dataset/
│   └── bank-additional-full.csv                   # UCI Bank Marketing dataset
├── report/
│   └── report.pdf                                 # full project report
└── README.md
```

---

## Requirements

```
pandas
numpy
scikit-learn
lightgbm
xgboost
matplotlib
seaborn
```

Install with:
```bash
pip install -r requirements.txt
```

---

## How to Run

```bash
git clone https://github.com/khanhnguyen2-dot/bank-marketing-prediction.git
cd bank-marketing-prediction
jupyter notebook Marketing_Data_Analysis_in_Banking.ipynb
```

---

## Data Source

Moro, S., Cortez, P., & Rita, P. (2014). A data-driven approach to predict the success of bank telemarketing. *Decision Support Systems*, 62, 22–31.  
Available at: [UCI ML Repository](https://archive.ics.uci.edu/ml/datasets/Bank+Marketing)

---

## License

MIT
