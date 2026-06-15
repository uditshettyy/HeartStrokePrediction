Optimized tool selection## README for Heart Disease Prediction Model

# Heart Disease Prediction Model

## Overview
This project predicts the presence of heart disease using a machine learning pipeline built in Python. It includes data exploration, preprocessing, model training, evaluation, and saving the best model artifacts.

## Dataset
- heart.csv contains the patient data used for modeling.
- Common features include:
  - `Age`
  - `Sex`
  - `ChestPainType`
  - `RestingBP`
  - `Cholesterol`
  - `FastingBS`
  - `RestingECG`
  - `MaxHR`
  - `ExerciseAngina`
  - `Oldpeak`
  - `ST_Slope`
  - `HeartDisease` (target)

## Key Steps
1. Load and inspect the dataset
2. Perform exploratory data analysis with plots
3. Clean data and handle invalid values
4. Encode categorical variables using one-hot encoding
5. Scale numerical features using `StandardScaler`
6. Train and compare multiple classifiers:
   - Logistic Regression
   - K-Nearest Neighbors
   - Naive Bayes
   - Decision Tree
   - SVM
7. Evaluate model performance using accuracy and F1 score
8. Save the final model and preprocessing objects

## Repository Files
- Heartdisease.ipynb – main notebook with the full workflow
- heart.csv – dataset file
- Saved artifacts:
  - `KNN_heart.pkl`
  - `scaler.pkl`
  - `columns.pkl`

## Installation
Install the required Python packages before running the notebook:

```bash
pip install numpy pandas seaborn matplotlib scikit-learn joblib
```

If using the optional analysis package:

```bash
pip install sheryanalysis==0.1.0
```

## Usage
1. Open Heartdisease.ipynb in Jupyter Notebook or JupyterLab.
2. Run cells sequentially to:
   - inspect the dataset
   - visualize feature distributions
   - preprocess data
   - train models
   - evaluate results
3. After training, the selected model and preprocessing tools are saved for later use.

## Notes
- Missing or invalid cholesterol and resting blood pressure values are replaced using the column mean.
- Numerical columns are standardized to improve classifier performance.
- One-hot encoding is used for categorical features, and `drop_first=True` avoids multicollinearity.

## Future Improvements
- Perform hyperparameter tuning for each model
- Add cross-validation for more stable evaluation
- Compare with ensemble models like Random Forest or XGBoost
- Build a prediction API for real-time inference

