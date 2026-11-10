# PRCP-1000 – Portuguese Bank Marketing

Capstone project: predict which customers will subscribe to a term deposit after a direct phone-marketing campaign, and give recommendations to the bank's marketing team.

All work is in a single notebook: **[PRCP-1000-Portuguese-Bank.ipynb](PRCP-1000-Portuguese-Bank.ipynb)**

## Contents of the notebook
1. **Task 1 – Data Analysis Report**: data quality, target balance, feature distributions and key findings
2. **Task 2 – Predictive Model**: preprocessing and four models (Logistic Regression, Decision Tree, Random Forest, Gradient Boosting)
3. **Model Comparison Report**: the best model for production
4. **Report on Challenges Faced**
5. **Task 3 – Suggestions to the Marketing Team**

## Result
| Model | Accuracy | Recall | F1 | ROC-AUC |
|---|---|---|---|---|
| **Gradient Boosting** (recommended) | 0.850 | 0.652 | 0.495 | 0.815 |
| Random Forest | 0.855 | 0.638 | 0.498 | 0.813 |
| Logistic Regression | 0.831 | 0.645 | 0.462 | 0.800 |
| Decision Tree | 0.851 | 0.629 | 0.488 | 0.798 |

`duration` is excluded because it is only known after the call (data leakage).

## Data
`data/bank-additional-full.csv`: 41,188 customers, 21 columns, from a Portuguese bank's campaigns (May 2008 – Nov 2010).
Source: [UCI Machine Learning Repository – Bank Marketing](https://archive.ics.uci.edu/dataset/222/bank+marketing) (Moro et al., 2014).

## How to run
```bash
python -m venv .venv
.venv\Scripts\activate        # Windows  (macOS/Linux: source .venv/bin/activate)
pip install -r requirements.txt
jupyter notebook PRCP-1000-Portuguese-Bank.ipynb
```
Then run **Kernel → Restart & Run All**.
