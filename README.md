# Real-Time Predictive Maintenance with IoT Sensor Data and Machine Learning

## Author
Danush Uppalapaati Sudhakar
MSc in Data Science

## Business Understanding

Unexpected equipment breakdowns in industrial production lead to substantial losses in output, increased maintenance costs, and risk to safety. Scheduled or reactive maintenance strategies — which are traditional approaches — lag behind in uptime, scalability, and operational robustness-driven settings.

The aim of this project is to shift towards **proactive maintenance** using the assistance of **real-time IoT sensor data** and **predictive machine learning models** to detect preliminary warning signs of machine failure and inform timely maintenance interventions.

---

## Research Aim

To develop and validate a scalable predictive maintenance model integrating real-time sensor data and understandable machine learning algorithms for accurate fault detection and failure prediction in industrial equipment.

---

## Objectives

- Integrate high-frequency IoT sensor data into machine learning workflows
- Identify prominent features that are predictive of equipment failure
- Train, test, and compare prediction performance of classification models
- Make the model more interpretable using explainable AI techniques
- Create a real-time dashboard to display predictions and insights
- Assess usability and performance via pilot deployment

---

## Summary of Dataset

- Origin: Public dataset on Kaggle
- Type: Tabular time-series sensor data
- Features: Pressure, vibration, rotational speed, temperature, usage hours, etc.
- Target: Binary label of equipment failure
- Challenges Addressed:
  - Imbalanced classes (failures are the exception)
  - Noisy and missing sensor readings
  - Redundancy of features

----

## Methodology

### Framework: CRISP-DM

1. **Business Understanding**: Define objectives in terms of downtime reduction and reliability
2. **Data Understanding**: Data exploration to determine patterns, distributions, and sensor trends
3. **Data Preparation**:
   - Missing value imputation
- Log transformations
- Detection of outliers using boxplots
- Balancing classes using RandomUnderSampler and SMOTE
4. **Modeling**:
   - ML algorithms: Logistic Regression, Random Forest, Decision Tree, KNN, SVM
   - Hyperparameter tuning using GridSearchCV
5. **Evaluation**:
   - Precision, Recall, F1-Score, ROC-AUC
   - Confusion matrix and cross-validation
6. **Deployment**:
   - Interactive dashboard using Dash (Plotly)
- In-situ failure visualization with sensor influence scores

---

## Model Performance


Random Forest outperformed other models for every measure and was selected for deployment.

---

## Explainable

To ensure it is interpretable and earn stakeholder trust, the following explainability techniques were used:

- **SHAP (SHapley Additive Explanations)**: Local/global contribution of each feature to prediction
- **Permutation Importance**: Measures how shuffling all features affects model performance
- **LASSO Regression**: Identifies and penalizes less significant features

### Top Features Emerged:

- `Pressure_Reading`
- `Rotational_Speed`
- `Cumulative_Operating_Hours`

These features consistently ranked in the top positions across all techniques and explain most failure variance.

---
## Real-Time Dashboard

An easy-to-use dashboard was developed with Dash (Plotly) to present:

- Real-time failure probabilities
- Top sensors contributing to failures
- Failure patterns over time
- Filtered equipment-level information

# Monitoring Metrics (For Production Readiness)

| Benefit                | Outcome                                    |
| ---------------------- | ------------------------------------------ |
| Downtime Reduction     | Planned stops through early prediction  
| Cost Optimization      | Optimal utilization of resources and spares  
| Safety Improvement     | Warns in advance of critical failures  
| Human Decision Support | Trust from technicians through interpretable AI
| Scalability            | Framework can scale between factories


# Research Contributions
Shown Random Forest is highly accurate and interpretable on real-world sensor data

Shown end-to-end CRISP-DM-based predictive pipeline

Shown proof that XAI tools (SHAP, LASSO) can enhance industrial AI trust

Developed a usable dashboard prototype that can be deployed into factory systems

Stressed the scope for scalable PdM models in Industry 4.0

## Dashboard Screenshots

### Real-Time Failure Probability Display
![Failure Probability](Screenshot%202025-05-20%20124224.png)

### Sensor Data Trends
![Sensor Trends](Screenshot%202025-05-20%20124242.png)

### Equipment Risk Table
![Risk Table](Screenshot%202025-05-20%20124326.png)

### Feature Importance Visualization
![Feature Importance](Screenshot%202025-05-20%20124501.png)

### SHAP Interpretation Output
![SHAP Summary](Screenshot%202025-05-20%20124526.png)

### Confusion Matrix Output
![Confusion Matrix](Screenshot%202025-05-20%20124609.png)

### Historical Failure Overview
![Historical Failures](Screenshot%202025-05-20%20124631%20-%20Copy.png)

### Live Sensor Feed Snapshot
![Live Feed](Screenshot%202025-05-20%20124702%20-%20Copy.png)

### Revision History
# Project starting Date
![](https://github.com/Danush-US/Enhancing-predictive-maintainance-in-manufacturing-using-ML/blob/main/Screenshot%202025-05-21%20144632.png)
# Project finishing date
![](https://github.com/Danush-US/Enhancing-predictive-maintainance-in-manufacturing-using-ML/blob/main/Screenshot%202025-05-21%20144619.png)
