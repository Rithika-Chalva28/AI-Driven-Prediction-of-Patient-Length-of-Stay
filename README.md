# AI-Driven Prediction of Patient Length of Stay

Machine learning project that predicts a hospital patient's **length of stay** and **treatment cost**, taking **diabetic status** into account.

## Project Overview

Hospitals need to plan beds, staff and budgets. This project uses patient data to:

- Explore patterns in hospital patient records (EDA)
- Predict how long a patient is likely to stay in the hospital
- Estimate treatment cost, with diabetic vs. non-diabetic patients analysed separately
- Assess patient risk

## Repository Contents

| File | Description |
|------|-------------|
| `eda.ipynb` | Exploratory data analysis of the patient dataset |
| `disease_model.ipynb` | Disease / diabetic status modelling |
| `risk_model.ipynb` | Patient risk modelling |
| `hospital_patient_dataset.xlsx` | Hospital patient dataset used by the notebooks |

## Requirements

- Python 3.8+
- Jupyter Notebook or JupyterLab
- pandas, numpy, matplotlib, scikit-learn, openpyxl

Install the dependencies:

```bash
pip install pandas numpy matplotlib scikit-learn openpyxl jupyter
```

## How to Run

1. Clone the repository:

   ```bash
   git clone https://github.com/Rithika-Chalva28/AI-Driven-Prediction-of-Patient-Length-of-Stay.git
   cd AI-Driven-Prediction-of-Patient-Length-of-Stay
   ```

2. Start Jupyter:

   ```bash
   jupyter notebook
   ```

3. Run the notebooks in this order:
   1. `eda.ipynb`
   2. `disease_model.ipynb`
   3. `risk_model.ipynb`

## Dataset

`hospital_patient_dataset.xlsx` contains hospital patient records used for analysis and model training.

## Results

_Add your model performance here (e.g. MAE / RMSE / R² for length of stay and cost, accuracy for diabetic status)._

## Author

**Rithika Chalva** — [GitHub: Rithika-Chalva28](https://github.com/Rithika-Chalva28)
