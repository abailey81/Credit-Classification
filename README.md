<div align="center">

# Credit Classification

### Machine Learning Loan Default Prediction

*SVM classifier · scikit-learn pipeline · feature engineering · reproducible Jupyter workflow*

<br>

[![Python](https://img.shields.io/badge/python-3.x-3776AB?style=for-the-badge&logo=python&logoColor=white)](https://www.python.org/)
[![scikit-learn](https://img.shields.io/badge/sklearn-F7931E?style=for-the-badge&logo=scikit-learn&logoColor=white)](https://scikit-learn.org/)
[![Pandas](https://img.shields.io/badge/Pandas-150458?style=for-the-badge&logo=pandas&logoColor=white)](https://pandas.pydata.org/)
[![Jupyter](https://img.shields.io/badge/Jupyter-F37626?style=for-the-badge&logo=jupyter&logoColor=white)](https://jupyter.org/)
[![License](https://img.shields.io/badge/MIT-green?style=for-the-badge)](LICENSE)

---

**End-to-end credit risk classification** predicting loan approval outcomes using an SVM classifier with StandardScaler preprocessing on 614 loan applicants.

<br>

| Metric | Value |
|:-------|:-----:|
| **Test Accuracy** | 83.33% |
| **Training Accuracy** | 79.86% |
| **Features** | 11 |
| **Model** | SVM (linear kernel) |

</div>

<br>

## Highlights

<table>
<tr>
<td width="50%">

**Data Pipeline**
- 614 loan applicants from Kaggle
- Missing value handling and cleaning
- Categorical to numerical encoding
- StandardScaler normalization

</td>
<td width="50%">

**Model & Evaluation**
- SVM with linear kernel (scikit-learn)
- 90/10 stratified train/test split
- Accuracy scoring on both train and test sets
- Predictive system for new loan applications

</td>
</tr>
</table>

---

## Dataset Features

| Feature | Type | Description |
|:--------|:-----|:------------|
| Gender | Categorical | Male / Female |
| Married | Categorical | Yes / No |
| Dependents | Numeric | Number of dependents (0-4) |
| Education | Categorical | Graduate / Not Graduate |
| Self_Employed | Categorical | Yes / No |
| ApplicantIncome | Numeric | Applicant income |
| CoapplicantIncome | Numeric | Co-applicant income |
| LoanAmount | Numeric | Loan amount (thousands) |
| Loan_Amount_Term | Numeric | Term of loan (months) |
| Credit_History | Binary | Credit history meets guidelines (1/0) |
| Property_Area | Categorical | Rural / Semiurban / Urban |

**Target:** `Loan_Status` (Approved = 1, Denied = 0)

---

## ML Pipeline

```
Raw Data (614 rows, 13 columns)
    │
    ├── Drop missing values → 480 rows
    ├── Encode categoricals → numerical
    ├── Drop Loan_ID
    │
    ├── StandardScaler (z-score normalization)
    ├── 90/10 stratified split (432 train / 48 test)
    │
    ├── SVM (linear kernel) training
    │
    └── Accuracy: 83.33% test / 79.86% train
```

---

## Getting Started

```bash
git clone https://github.com/abailey81/Credit-Classification.git
cd Credit-Classification

pip install -r requirements.txt
jupyter notebook notebooks/Loan\ prediction.ipynb
```

---

## Project Structure

```
Credit-Classification/
├── notebooks/
│   └── Loan prediction.ipynb    # Full analysis and modeling pipeline
├── src/
│   └── __init__.py              # Package placeholder
├── requirements.txt             # pandas, numpy, scikit-learn, matplotlib, seaborn
└── .gitignore
```

---

<div align="center">

**[MIT License](LICENSE)**

Built with scikit-learn, pandas, and Jupyter

</div>
