## Airfoil-Pressure-Prediction-Using-Regression-Models

The aim of this project is to predict the pressure coefficient (Cp) on airfoil surfaces using various regression models. Based on aerodynamic features such as angle of attack, chord length, free-stream velocity, and suction surface displacement thickness, the goal is to estimate the pressure coefficient through both linear and non-linear regression techniques. Initially, a linear regression model is applied for basic prediction, followed by the implementation of more complex algorithms like Random Forest to improve model performance. This study aims to highlight the potential of data-driven analysis in aerodynamic computations, particularly in engineering applications.

## Dataset Variables and Units

| Variable Name                 | Description                              | Unit           |
|-------------------------------|------------------------------------------|----------------|
| Frequency                     | Sound frequency                          | Hz             |
| Angle_of_attack               | Angle between airflow and airfoil        | Degrees (°)    |
| Chord_length                  | Width of the airfoil                     | Meters (m)     |
| Free_stream_velocity          | Speed of the airflow                     | Meters/second  |
| Suction_side_displacement_thickness | Displacement thickness of the airflow on suction side | Meters (m)     |
| Scaled_sound_pressure  | Output target: scaled sound pressure     | Decibels (dB)  |


##  Project Directory Structure

```
aircraft_anomaly_detection/
│
├── data/
│   ├── raw/                   # Original sensor data (unprocessed)
│   └── processed/             # Cleaned and preprocessed data
│
├── notebooks/
│   ├── 1_data_exploration.ipynb     # Initial data loading and EDA
│   ├── 2_feature_engineering.ipynb  # Creating and selecting features
│   ├── 3_Linear_Regression.ipynb    # Training machine learning models
│   ├── 3_Random_Forest.ipynb        # Training machine learning models
│   └── 4_evaluation_visuals1.ipynb  # Performance metrics and visual analysis (Linear Regression)
│   └── 4_evaluation_visuals2.ipynb  # Performance metrics and visual analysis (Random Forest)
├── models/
│   └── trained_models/        # Saved models (.pkl, .joblib, etc.) (Random Forest)
│
├── models/
│   └── trained_models/        # Saved models (.pkl, .joblib, etc.) (Linear Regression)
│
├── reports/
│   └── images/                # Generated graphs and charts
│   
│
│
├── requirements.txt           # Python dependencies
└── README.md                  # Project overview
```

## Summary

- **Objective:** Detect anomalies in aircraft engines using multivariate sensor data.
- **Dataset:** Engine sensor readings with no column names (manually assigned).
- **Tools:** Pandas, NumPy, Scikit-learn, Matplotlib, Seaborn, etc.
- **Steps Covered:**
  - Data loading and column assignment
  - Exploratory data analysis (EDA)
  - Feature engineering (e.g., mean, standard deviation, slope)
  - Anomaly labeling based on thresholds
  - Data visualization
  - Machine learning model training and evaluation

## Model Performance Metrics

| Model            | MAE   | RMSE  | R² Score |
|------------------|-------|-------|----------|
| Linear Regression| 4.079 | 5.145 | 0.472    |
| Random Forest    | 1.643 | 5.135 | 0.897    |

## Model Performance and Hyperparameters

| Metric                           | Value           |
|---------------------------------|-----------------|
| Best Hyperparameters             | bootstrap: False<br>max_depth: 39<br>max_features: log2<br>min_samples_leaf: 2<br>min_samples_split: 2<br>n_estimators: 413 |
| Best Cross-Validation R² Score  | 0.8839          |
| Test Set R² Score                | 0.8963          |
