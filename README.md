# AI-Driven Prediction of Patient Length of Stay

Machine learning project on hospital patient records that predicts length of stay and treatment cost with diabetic status taken into account, and classifies patients as **Low risk** or **High risk**.

## Repository Contents

| File | Description |
|------|-------------|
| `eda.ipynb` | Exploratory data analysis of the patient dataset |
| `disease_model.ipynb` | Disease-related modelling |
| `risk_model.ipynb` | Patient risk classification (Low / High risk) |
| `hospital_patient_dataset.xlsx` | Hospital patient dataset used by the notebooks |

## Dataset

Patient records including age, BMI, blood glucose, systolic and diastolic blood pressure, cholesterol, number of comorbidities, emergency admission flag, previous admissions, previous visits in the last year, medication count, and primary diagnosis.

## Risk Model

A classifier that predicts whether a patient is **High risk** or **Low risk**, with a `predict_risk(...)` helper that returns the risk label and probability for a new patient.

### Performance (test set, 50 patients: 42 Low risk, 8 High risk)

| Metric | Score |
|--------|-------|
| Accuracy | 0.96 |
| Precision | 0.875 |
| Recall | 0.875 |
| F1 score | 0.875 |
| ROC-AUC | 0.997 |

| Class | Precision | Recall | F1-score | Support |
|-------|-----------|--------|----------|---------|
| Low risk | 0.98 | 0.98 | 0.98 | 42 |
| High risk | 0.88 | 0.88 | 0.88 | 8 |
| Macro avg | 0.93 | 0.93 | 0.93 | 50 |
| Weighted avg | 0.96 | 0.96 | 0.96 | 50 |

The test set is small, so these scores should be read with caution.

### Feature Effects (log-odds of High risk)

| Feature | Coefficient |
|---------|-------------|
| N_Comorbidities | 2.309 |
| Previous_Admissions | 1.489 |
| Is_Emergency | 0.997 |
| Systolic_BP | 0.769 |
| Blood_Glucose_mgdL | 0.732 |
| Diastolic_BP | 0.557 |
| Age | 0.436 |
| Medications_Count | 0.303 |
| Previous_Visits_1Yr | 0.044 |
| BMI | -0.301 |
| Cholesterol_mgdL | -0.508 |

Number of comorbidities, previous admissions and emergency admission have the strongest effect on high-risk prediction.

## Requirements

- Python 3.8+
- Jupyter Notebook or JupyterLab
- pandas, numpy, matplotlib, scikit-learn, openpyxl

```bash
pip install pandas numpy matplotlib scikit-learn openpyxl jupyter
```

## How to Run

```bash
git clone https://github.com/Rithika-Chalva28/AI-Driven-Prediction-of-Patient-Length-of-Stay.git
cd AI-Driven-Prediction-of-Patient-Length-of-Stay
jupyter notebook
```

Run `eda.ipynb` first, then `disease_model.ipynb` and `risk_model.ipynb`.

## Author

**Rithika Chalva** — [GitHub: Rithika-Chalva28](https://github.com/Rithika-Chalva28)
**Y.Samuel Dan** — [GitHub: Rithika-Chalva28](https://github.com/NCS2005)
**N.Chaitanya Sandeep** — [GitHub: Rithika-Chalva28](https://github.com/samdan-honey)
