# Real-Time Predictive Maintenance using IoT Sensor Data and Machine Learning

## Author
Danush Uppalapaati Sudhakar  
MSc in Data Science  
Supervisor: Dr. Charles Nwankire

---

## Business Understanding

In industrial manufacturing, unplanned equipment failures lead to major production losses, increased maintenance costs, and safety risks. Traditional maintenance strategies — such as scheduled or reactive maintenance — are insufficient in environments that demand uptime, scalability, and operational resilience.

The goal of this project is to shift from reactive to **proactive maintenance** using **real-time IoT sensor data** and **predictive machine learning models** to detect early indicators of machine failure and inform timely maintenance interventions.

---

## Research Aim

To develop and validate a scalable predictive maintenance framework that integrates real-time sensor data with interpretable machine learning algorithms for accurate fault detection and failure forecasting in industrial equipment.

---

## Objectives

- Integrate high-frequency IoT sensor data with machine learning pipelines
- Identify critical features that predict equipment failure
- Train, evaluate, and compare classification models for predictive performance
- Enhance model transparency through explainable AI techniques
- Build a real-time dashboard to visualize predictions and insights
- Assess usability and performance through a pilot deployment

---

## Dataset Summary

- Source: Public dataset from Kaggle
- Data Type: Tabular time-series sensor data
- Features: Pressure, vibration, rotational speed, temperature, usage hours, etc.
- Target: Binary label indicating equipment failure
- Challenges Addressed:
  - Imbalanced classes (failures are rare)
  - Noisy and incomplete sensor readings
  - Feature redundancy

---

## Methodology

### Framework: CRISP-DM

1. **Business Understanding**: Define goals around downtime reduction and reliability
2. **Data Understanding**: Exploratory analysis to detect patterns, distributions, and sensor behavior
3. **Data Preparation**:
   - Missing value imputation
   - Log transformations
   - Outlier detection using boxplots
   - Class balancing using RandomUnderSampler and SMOTE
4. **Modeling**:
   - ML algorithms: Logistic Regression, Random Forest, Decision Tree, KNN, SVM
   - Hyperparameter tuning with GridSearchCV
5. **Evaluation**:
   - Precision, Recall, F1-Score, ROC-AUC
   - Confusion matrix and cross-validation
6. **Deployment**:
   - Interactive dashboard using Dash (Plotly)
   - Real-time failure visualization with sensor impact scores

---

## Model Performance

| Model                | Precision | Recall | F1 Score | ROC-AUC |
|---------------------|-----------|--------|----------|---------|
| Logistic Regression | 0.74      | 0.76   | 0.75     | 0.82    |
| Decision Tree       | 0.72      | 0.74   | 0.73     | 0.80    |
| K-Nearest Neighbors | 0.68      | 0.69   | 0.68     | 0.77    |
| SVM                 | 0.75      | 0.76   | 0.75     | 0.83    |
| **Random Forest**   | **0.87**  | **0.88** | **0.87** | **0.92**  |

**Conclusion**: Random Forest outperformed other models across all metrics and was selected for deployment.

---

## Explainable 

To ensure interpretability and stakeholder trust, the following explainability techniques were used:

- **SHAP (SHapley Additive Explanations)**: Provides local/global impact of each feature on prediction
- **Permutation Importance**: Measures how shuffling each feature affects model performance
- **LASSO Regression**: Identifies and penalizes less relevant features

### Top Features Identified:

- `Pressure_Reading`
- `Rotational_Speed`
- `Cumulative_Operating_Hours`

These features consistently appeared in the top ranks across all methods and explain most failure variance.

---

## Real-Time Dashboard

A user-friendly dashboard was built using Dash (Plotly) to deliver:

- Live failure probabilities
- Top influencing sensors
- Historical failure patterns
- Filtered equipment-level insights

