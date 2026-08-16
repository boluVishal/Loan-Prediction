# Loan Prediction

This project explores historical LendingClub loan data and builds classification models to predict whether a borrower will **not fully repay a loan**.

The analysis is contained in `Loan Prediction.ipynb`, and the cleaned dataset used by the notebook is included as `loan_data.csv`.

## Problem

LendingClub connects borrowers with investors. From an investor's perspective, the key question is whether a borrower is likely to repay the loan in full.

The target variable in this dataset is:

- `not.fully.paid = 0`: loan was fully paid
- `not.fully.paid = 1`: loan was not fully paid

## Dataset

The notebook uses 9,578 loan records with 14 columns.

Key fields include:

- `credit.policy` — whether the borrower meets LendingClub's credit underwriting criteria
- `purpose` — reason for the loan
- `int.rate` — interest rate
- `installment` — monthly installment amount
- `log.annual.inc` — log of annual income
- `dti` — debt-to-income ratio
- `fico` — FICO credit score
- `days.with.cr.line` — credit history length
- `revol.bal` — revolving balance
- `revol.util` — revolving credit utilization
- `inq.last.6mths` — recent creditor inquiries
- `delinq.2yrs` — delinquencies in the previous two years
- `pub.rec` — derogatory public records
- `not.fully.paid` — prediction target

## Analysis

The notebook includes:

1. Data loading and inspection
2. Exploratory data analysis and visualisation
3. Conversion of categorical loan-purpose values into model-ready variables
4. Train/test splitting
5. Decision Tree classification
6. Random Forest classification
7. Evaluation using confusion matrices and classification reports

## Models

### Decision Tree

A `DecisionTreeClassifier` is trained as the first classification model.

### Random Forest

The notebook also trains a `RandomForestClassifier` with 600 estimators and compares its classification performance with the Decision Tree.

The evaluation shows an important class-imbalance issue: overall accuracy is relatively high, but identifying the minority `not.fully.paid = 1` class is substantially harder. This is visible in the precision and recall reported in the notebook.

## Repository structure

```text
.
├── Loan Prediction.ipynb
├── README.md
└── loan_data.csv
```

## Running the notebook

Clone the repository and open the notebook in Jupyter:

```bash
git clone https://github.com/boluVishal/Loan-Prediction.git
cd Loan-Prediction
jupyter notebook "Loan Prediction.ipynb"
```

The notebook imports pandas, NumPy, Matplotlib, Seaborn, and scikit-learn.

## Note

This is an exploratory machine-learning notebook based on historical LendingClub data. The reported model performance should be interpreted in the context of the dataset and the class imbalance present in the target variable.
