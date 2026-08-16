# Loan Repayment Prediction

Binary classification on LendingClub data from 2007–2010: predict whether a borrower repaid their loan in full.

## Dataset

Publicly available LendingClub data, pre-cleaned (no NA values). The CSV is included in the repo.

**Features:**

| Column | Description |
|---|---|
| `credit.policy` | 1 if customer met LendingClub's underwriting criteria |
| `purpose` | Loan purpose (credit card, debt consolidation, etc.) |
| `int.rate` | Interest rate as a decimal (e.g. 0.11 = 11%) |
| `installment` | Monthly installment amount |
| `log.annual.inc` | Log of self-reported annual income |
| `dti` | Debt-to-income ratio |
| `fico` | FICO credit score |
| `days.with.cr.line` | Days the borrower has had a credit line |
| `revol.bal` | Revolving balance (unpaid credit card balance) |
| `revol.util` | Revolving line utilization rate |
| `inq.last.6mths` | Creditor inquiries in last 6 months |
| `delinq.2yrs` | Times 30+ days past due in past 2 years |
| `pub.rec` | Derogatory public records (bankruptcies, tax liens) |

**Target:** `not.fully.paid` — 1 if the loan was not repaid in full.

## Running it

Open `Loan Prediction.ipynb` in Jupyter. Requires `pandas`, `numpy`, `matplotlib`, `seaborn`, and `scikit-learn`.

```bash
jupyter notebook "Loan Prediction.ipynb"
```

## Context

LendingClub had an eventful 2016, but this data predates their IPO — it's from their early lending years and gives a clean view of their underwriting criteria and borrower profiles.
