# Employee Attrition Prediction & Risk Scoring

Predicts the likelihood of an employee leaving the organization using HR data, and compares Random Forest, XGBoost, and CatBoost for the task.

**Best model:** CatBoost — ROC-AUC 0.792, Recall 0.49 on employees who left.

## Repo Structure

```
├── notebooks/
│   └── attrition_analysis.ipynb       # Full EDA, feature selection, modeling
├── Employee_Attrition_Project.pdf    # Full write-up (methodology, results, limitations)
└── README.md
```
**Dashboard:** [View on Tableau Public](<https://public.tableau.com/views/HrAnalysis_17886817555960/Dashboard6_1?:language=en-US&publish=yes&:sid=&:redirect=auth&:display_count=n&:origin=viz_share_link>)

> **Note:** The dataset used in this project is not included in this repository due to data sharing restrictions. The notebook and dashboard code are provided for reference — to run them end-to-end, you would need to supply your own dataset matching the column structure described in the Data Description section of the [project write-up](./Employee_Attrition_Project.pdf).

## Setup

```bash
git clone <repo-url>
cd employee-attrition-prediction
pip install -r requirements.txt
```

## Usage

```bash
jupyter notebook notebooks/attrition_analysis.ipynb
```

## Tech Stack

Python · pandas · numpy · scikit-learn · xgboost · catboost · scipy · statsmodels · matplotlib · seaborn

## Results

| Model | Recall (Attrition) | F1 (Attrition) | ROC-AUC |
|---|---|---|---|
| Random Forest (SMOTE) | 0.26 | 0.34 | 0.754 |
| XGBoost | 0.26 | 0.32 | 0.750 |
| **CatBoost** | **0.49** | **0.49** | **0.792** |

Full methodology, feature selection process, and limitations are documented in [`Employee_Attrition_Project.pdf`](./Employee_Attrition_Project.pdf).
