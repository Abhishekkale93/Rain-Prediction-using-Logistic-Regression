# Rain-Prediction-using-Logistic-Regression

## Overview
This project uses **Logistic Regression** to predict whether it will rain tomorrow in Australia based on historical weather data. The dataset includes features such as temperature, humidity, and rainfall.

---

##  Dataset
- **Source**: [Kaggle - "https://www.kaggle.com/datasets/jsphyg/weather-dataset-rattle-package"]
- **File**: `weatherAUS.csv`
- **Target Variable**: `RainTomorrow` (Yes/No)

---

##  Problem Statement
Build a classification model to predict the `RainTomorrow` value using historical weather conditions. This helps in better planning and can be applied in agricultural or logistic sectors.

---

##  Technologies Used
- Python
- Pandas, NumPy
- Matplotlib, Seaborn
- Scikit-learn

---

##  EDA (Exploratory Data Analysis)
- Distribution of `RainTomorrow`
- Relationship between `Humidity3pm`, `Rainfall`, and `RainTomorrow`
- Visualizations: countplot, boxplot, pairplot

---

##  Preprocessing
- Dropped rows with missing values
- Encoded `RainToday` and `RainTomorrow` as binary values
- Scaled features using `StandardScaler`

---

##  Model Training
- Model: `LogisticRegression(max_iter=1000)`
- Train-Test Split: 80/20
- Evaluation: Accuracy, Confusion Matrix, Classification Report

---

##  Results
- Accuracy: ~84%
- Key Features: `Humidity3pm`, `RainToday`, `Rainfall`
- Confusion Matrix and Classification Report show balanced performance

---

##  Sample Prediction
```python
sample = np.array([[15.0, 25.0, 2.5, 70.0, 1]])
sample_scaled = scaler.transform(sample)
prediction = model.predict(sample_scaled)
