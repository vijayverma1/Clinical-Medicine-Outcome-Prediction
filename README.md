# Clinical-Medicine-Outcome-Prediction
Clinical adverse-event and treatment outcome prediction using Python, machine learning, and imbalanced classification techniques.
# Clinical Treatment Outcome & Adverse Event Prediction

**A clinical data analytics and machine learning project exploring treatment outcomes and adverse event prediction.**

## Overview

I am developing this project to explore how clinical and treatment-related data can be used to predict patient treatment outcomes and identify potential adverse events.

The project focuses on two complementary questions:

- **Treatment outcomes:** Can machine learning help predict whether a treatment outcome is favorable or unfavorable for a given clinical condition? Can patterns across treatments and patient characteristics help identify potentially promising treatment groups for further investigation?
- **Adverse events:** Can patient characteristics, clinical measurements, diagnoses, and treatment information help predict the likelihood of an adverse event?

The project combines data preparation, exploratory analysis, classification modeling, and model evaluation, with a planned Power BI dashboard to communicate the findings.

## Project Status

| Component | Status |
|---|---|
| Clinical data cleaning and preparation | Completed |
| Exploratory data analysis | Completed |
| Adverse event classification | Completed — initial model comparison |
| Treatment outcome prediction | Planned |
| Treatment and condition analysis | Planned |
| Power BI dashboard | Planned |

## Adverse Event Prediction

The first modeling phase focuses on predicting the occurrence of an adverse event using a binary classification approach.

I trained and compared six machine learning algorithms:

- Logistic Regression
- Random Forest
- CatBoost
- XGBoost
- AdaBoost
- LightGBM

Because the target classes are imbalanced, I evaluated models using precision, recall, F1-score, ROC-AUC, and confusion matrices rather than relying on accuracy alone. I also explored class weighting to improve the detection of adverse events.

### Initial Model Comparison

| Model | Adverse Event F1-score | ROC-AUC |
|---|---:|---:|
| Logistic Regression | 0.36 | 0.541 |
| Random Forest — original | 0.09 | 0.581 |
| Random Forest — class-weighted | 0.13 | 0.588 |
| CatBoost | **0.39** | **0.602** |
| XGBoost | 0.38 | 0.569 |
| AdaBoost | 0.38 | 0.569 |
| LightGBM | 0.38 | 0.568 |

*These are preliminary results from the current experimental setup, not final optimized model performance.*

CatBoost currently provides the strongest ROC-AUC and adverse-event F1-score among the models evaluated. The results also highlight the challenge of distinguishing adverse-event cases in an imbalanced dataset and the need for further model improvement.

## Treatment Outcome Prediction — Next Phase

The next phase will focus on predicting treatment outcomes and examining how outcomes vary across clinical conditions, treatments, and treatment combinations.

Planned work includes:

- Defining the prediction target and favorable versus unfavorable outcomes.
- Training and comparing classification models.
- Examining outcome patterns across diagnoses and treatment groups.
- Investigating potential interactions between clinical conditions and treatment combinations.
- Evaluating model performance and the limitations of the available data.

The goal is to identify patterns that may support further investigation, not to establish treatment effectiveness or make clinical recommendations.

## Technology Stack

**Python · Pandas · NumPy · Scikit-learn · CatBoost · XGBoost · LightGBM · Matplotlib · Seaborn · Jupyter Notebook · VS Code**

**Planned reporting:** Power BI

## Repository Contents

- Jupyter Notebook — data preparation, exploratory analysis, and adverse-event model development.
- `requirements.txt` — Python dependencies.

## Dataset & Limitations

This project uses synthetic clinical data rather than real patient records. Findings reflect patterns in the available dataset and may not generalize to real-world clinical populations.

The models are intended for educational and portfolio purposes only. Predictions and observed associations do not establish causation or clinical effectiveness and should not be used for medical decision-making.

## Future Development

- Further model tuning and evaluation.
- Comparison of class-weighting and resampling approaches.
- Treatment outcome modeling and treatment-condition analysis.
- Power BI dashboard for communicating key findings.
