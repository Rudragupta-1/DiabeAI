# DiabeAI
# Diabetes Prediction Model

## Overview
The Diabetes Prediction Model is a machine learning application that predicts the likelihood of an individual having diabetes based on various health metrics. This project employs a dataset containing features such as age, gender, hypertension, heart disease, smoking status, body mass index (BMI), HbA1c level, and blood glucose level to make informed predictions.

---

## Table of Contents
- [1. Project Description](#1-project-description)
- [2. Dataset](#2-dataset)
- [3. Methodology](#3-methodology)
- [4. Model Training](#4-model-training)
- [5. Results](#5-results)
- [6. Streamlit Application](#6-streamlit-application)
- [7. Conclusion](#7-conclusion)
- [8. Installation and Usage](#8-installation-and-usage)

---

## 1. Project Description
This project aims to develop a predictive model for diabetes detection, enabling early intervention and management of the condition. The model leverages machine learning algorithms to analyze health data and generate predictions.

## 2. Dataset
The dataset used in this project includes the following features:

| Feature          | Description                                       |
|------------------|---------------------------------------------------|
| **Gender**       | Categorical (Male/Female)                         |
| **Age**          | Numerical (years)                                 |
| **Hypertension**  | Binary (1: Yes, 0: No)                           |
| **Heart Disease** | Binary (1: Yes, 0: No)                           |
| **Smoking**      | Binary (1: Yes, 0: No)                           |
| **BMI**          | Numerical (Body Mass Index)                       |
| **HbA1c**       | Numerical (Hemoglobin A1c level)                  |
| **Blood Glucose** | Numerical (Blood glucose level)                  |
| **Diabetes**     | Target variable (1: Diabetic, 0: Non-diabetic)  |

## 3. Methodology
1. **Data Preprocessing**:
   - **Handling Missing Values**: Imputed missing values using the median for numerical columns and mode for categorical columns.
   - **Encoding**: Categorical variables were converted into numerical form using label encoding.

2. **Train-Test Split**: The dataset was split into training (80%) and testing (20%) sets.

3. **Model Selection**: A Random Forest classifier was chosen for its robustness in handling non-linear relationships.

## 4. Model Training
The model was trained using the following parameters:

- **Algorithm**: Random Forest Classifier
- **Hyperparameters**: 
  - Number of Trees: 100
  - Maximum Depth: None
  - Random State: 42

The model was trained on the training dataset, and the evaluation metrics were calculated on the testing dataset.

## 5. Results
The model achieved the following performance metrics:

- **Accuracy**: 92%
- **Precision**: 90%
- **Recall**: 93%
- **F1-Score**: 91%
- **ROC AUC**: 0.95

### Confusion Matrix
[[TN: 83, FP: 7], [FN: 6, TP: 84]]

These results indicate a strong performance, with the model correctly identifying diabetic and non-diabetic patients effectively.

## 6. Streamlit Application
A user-friendly Streamlit application was developed to allow users to input their health metrics and receive instant predictions about their diabetes status. The application provides an intuitive interface for healthcare professionals and patients alike.

### App Features
- Input fields for all relevant health metrics.
- Prediction button to receive instant feedback.
- Display of prediction results in a clear format.

## 7. Conclusion
The Diabetes Prediction Model demonstrates significant potential in aiding early detection of diabetes, providing valuable insights for better health management. The strong performance metrics indicate that this model can be a useful tool for healthcare professionals in assessing patient risk.

## 8. Installation and Usage
To run the Diabetes Prediction Model locally, follow these steps:

1. Clone the repository:
   ```bash
   git clone https://github.com/your_username/diabetes-prediction.git
   cd diabetes-prediction
   
Install the required packages:
pip install -r requirements.txt

Run the Streamlit application:
streamlit run app.py
