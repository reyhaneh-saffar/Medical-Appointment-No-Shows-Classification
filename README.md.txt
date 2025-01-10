# Medical Appointment No-Show Analysis

This project analyzes a dataset of medical appointments to identify factors influencing patient attendance. It implements data preprocessing, feature engineering, and model training to predict whether patients show up for their scheduled appointments. 

---

## Data Preprocessing
- **Exploration**: Analyzed column distributions and identified categorical variables.
- **Missing Values**: Confirmed no missing values; handled anomalies (e.g., unrealistic ages replaced with the mean age).
- **Datetime Features**: Converted and split datetime columns into date and time for granular analysis.
- **Irrelevant Features**: Removed columns like `PatientId` and `AppointmentID` to streamline analysis.

---

## Data Visualization
- **Class Imbalance**: Histograms highlighted imbalances in binary categorical variables, particularly the target variable `NoShow`.

---

## Feature Engineering
- **New Feature**: Created `TimeDifference`, representing the days between scheduling and appointment, providing critical temporal insights.
- **Encoding**: Transformed categorical variables using binary and one-hot encoding, increasing the feature count from 15 to 229.

---

## Scaling
- Standardized continuous variables (`Age` and `TimeDifference`) to ensure consistent scales across features.

---

## Data Sampling
- Addressed class imbalance in `NoShow` by resampling the majority class to match the minority class. The resulting balanced dataset contained 44,638 samples with the equal class distribution.

---

## Model Training
- **Algorithm**: Trained a Multi-Layer Perceptron (MLP) neural network for binary classification.
- **Training**: Optimized using binary cross-entropy loss and stochastic gradient descent (SGD). Metrics like loss and accuracy were monitored per epoch.


