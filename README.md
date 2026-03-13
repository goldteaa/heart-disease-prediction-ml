# heart-disease-prediction-ml
Machine learning pipeline for predicting heart disease using Logistic Regression and Random Forest with Python, Pandas, and Scikit-learn.


# Heart Disease Prediction using Machine Learning

This project builds a complete **machine learning pipeline** to predict the presence of heart disease using clinical data. The model analyzes patient features such as age, blood pressure, cholesterol levels, and ECG results to estimate the probability of heart disease.

The goal of this project is to demonstrate how machine learning can support **early risk detection and clinical decision-making**.

---

## Dataset

The dataset used in this project is the **Heart Disease dataset** containing **918 patient records** and **12 clinical features**, including:

- Age
- Sex
- Chest Pain Type
- Resting Blood Pressure
- Cholesterol
- Fasting Blood Sugar
- Resting ECG
- Maximum Heart Rate
- Exercise-induced Angina
- ST Depression (Oldpeak)
- ST Segment Slope

Target variable:
HeartDisease
0 = No disease
1 = Heart disease


---

## Project Pipeline

The project follows a complete data science workflow:

### 1. Data Cleaning
- Removed duplicates
- Handled missing values
- Corrected invalid cholesterol values
- Feature engineering for ECG signals

Notebook:  
`notebooks/1dataCleaning.ipynb`

---

### 2. Exploratory Data Analysis (EDA)

Data visualization was used to understand patterns and relationships between variables.

Examples of visualizations include:

- Feature distributions
- Correlation heatmaps
- Age vs heart disease boxplots
- Exercise angina vs disease risk
- Pair plots for key features

Notebook:  
`notebooks/2visualization.ipynb`

---

### 3. Feature Engineering

Key preprocessing steps included:

- Splitting the **Oldpeak** feature into:
  - ST Depression
  - ST Elevation
- Log transformation of skewed variables
- One-hot encoding for categorical features
- Standardization using **StandardScaler**

---

### 4. Machine Learning Models

Two supervised learning algorithms were trained and compared:

**Logistic Regression**

- Simple interpretable model
- Good baseline classifier

**Random Forest**

- Ensemble model
- Handles nonlinear relationships well
- Reduces overfitting

Notebook:  
`notebooks/3modeling.ipynb`

---

## Model Evaluation

Models were evaluated using:

- Accuracy
- Confusion Matrix
- Precision / Recall
- ROC Curve
- ROC-AUC Score

### Results

| Model | Accuracy |
|------|------|
| Logistic Regression | ~85% |
| Random Forest | ~87% |

Random Forest achieved slightly better performance and stronger ROC curve characteristics.

---

## Key Predictive Features

The most important predictors of heart disease were:

- ST segment slope
- Exercise-induced angina
- Maximum heart rate
- Age
- Chest pain type

These findings align with known cardiology risk factors.

---

## Repository Structure
heart-disease-prediction-ml

data/
HeartPrediction.csv
heart_cleaned.csv
heart_disease_predictions.csv

notebooks/
1dataCleaning.ipynb
2visualization.ipynb
3modeling.ipynb

models/
rf_model.pkl
scaler.pkl
columns.pkl

images/
visualization outputs and ROC curves


---

## Technologies Used

- Python
- Pandas
- NumPy
- Scikit-learn
- Matplotlib
- Seaborn
- Jupyter Notebook

---

## Future Improvements

Possible improvements to this project include:

- Hyperparameter tuning
- Additional ML models (XGBoost, Gradient Boosting)
- Cross-validation strategies
- Deployment as a prediction API
- Building a clinical risk dashboard

---

## Author

**A M**

Master's in Data Science & Business Analytics  
UNYT
