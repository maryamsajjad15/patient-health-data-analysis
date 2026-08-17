# Patient Health Data Analysis

A beginner data science project analyzing the UCI Heart Disease dataset. Covers data cleaning, exploratory analysis, and a baseline logistic regression model to predict heart disease, with an honest evaluation of the model's strengths and limitations.
📓 [View notebook with outputs](https://colab.research.google.com/github/maryamsajjad15/patient-health-data-analysis/blob/main/patient_health_analysis.ipynb)

## Dataset

UCI Heart Disease dataset (via Kaggle) — 302 unique patient records after removing duplicates, with 13 features including age, cholesterol, blood pressure, and chest pain type, plus a target column indicating presence of heart disease.

## What I did

- Checked for missing values and duplicates (found 723 duplicate rows out of 1025, removed them)
- Explored distributions of age and cholesterol
- Verified the target column encoding using medically-known variables (thalach, cp), since the dataset's documentation was inconsistent with the actual data
- Compared cholesterol and age between patients with and without heart disease
- Built a correlation heatmap to find which variables were most associated with heart disease
- Trained a Logistic Regression model to predict heart disease from the remaining features
- Evaluated the model using a confusion matrix and classification report, not just accuracy

## Key findings

- Chest pain type, max heart rate, exercise-induced angina, and oldpeak had the strongest correlation with heart disease
- Cholesterol alone was a surprisingly weak predictor in this dataset
- Age followed a roughly normal distribution; cholesterol was right-skewed with a few high outliers
- The logistic regression model reached 79% accuracy, but recall was uneven across classes: it correctly identified 90% of healthy patients but only 69% of patients who actually had heart disease
- This gap matters more than the overall accuracy number, since missing a disease case is more costly than a false alarm in a health context

## Tools

Python, pandas, numpy, matplotlib, seaborn, scikit-learn (Google Colab)
