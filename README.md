# Group-10-HEART-DISEASE-PREDICTION PROJECT
## PREDICTING THE LIKELIHOOD OF HEART DISEASE FROM PATIENTS
## PROJECT UNDERSTANDING
#### Heart disease remains a significant public health concern in Kenya, with increasing cases linked to lifestyle changes, urbanization and inadequate access to preventive healthcare. Despite growing awareness, early detection and treatment, risk assessment remains a challenge due to limited local research and data-driven insights. This study aims to analyze key health indicators. By identifying major risk factors and trends, this research seeks to support healthcare professionals, policymakers, and researchers in developing targeted interventions, improving early diagnosis, and enhancing public health strategies to combat heart disease in Kenya. The model will leverage data from the "heart_disease.csv" dataset, which includes demographic information, clinical measurements and historical health data.
### Objectives
#### i) To develop a Predictive Model by creating a machine learning that accurately predicts the likelihood of heart disease based on patient data.
#### ii) To identify Key Risk Factors which are the most significant predictors of heart disease. 
#### iii) To provide healthcare professionals with a tool that aids in the early detection and management of heart disease.
#### iv) To make informed decisions regarding resource allocation and preventive care strategies based on model predictions.
#### V) Increase awareness of heart disease risk factors among patients and the general public through educational materials and outreach programs.
## DATA UNDERSTANDING
#### Our data was extracted from Kaggle (https://www.kaggle.com/datasets/oktayrdeki/heart-disease) which has 21 columns and 10,000 rows. The data has both numerical and categorical features. The lebel encoding was for used to assign unique numbers on categorical features because of it's nominal data to ensure that the model can interpret the data, detect patterns, and make predictions effectively. Data cleaninig was done to handle missing values and also check for outliers which showed there were no both missing values and outliers. The visualizations for outliers is as shown below:
![outliers](https://github.com/user-attachments/assets/d1dbf1f7-df05-415b-9c76-ae8397698db8)
### Visualizations
#### 1. A count plot visualizes the distribution of patients with and without heart disease. The visualization showed that our data is imbalanced thus it will need to be balanced.
![image](https://github.com/user-attachments/assets/96efd9c2-67f4-4092-833f-34af2ef21080)
#### 2. Histograms were plotted for all numerical features to  identify skewness, normality, and the presence of outliers.  Histograms showed that our numerical features are normally distributed.
![image](https://github.com/user-attachments/assets/e8e2959a-361e-42be-a126-e15e81db2830)
#### 3. Count plots were used to analyse categorical variables to determine the association of certain features with heart disease. It was observed that patients who smoke are higher than those who don't smoke in regards to heart disease. The same applies to those with high blood pressure.
![image](https://github.com/user-attachments/assets/60ae15e8-43eb-4066-9f9a-0e3c55d63678)
#### Correlation heatmap used to examine features with a strong correlation to heart disease e.g., cholesterol, exercise habits, smoking, e.t.c. These features will help us know the main risk factors leading to heart disease.
![image](https://github.com/user-attachments/assets/65fa64c6-3ee6-4428-8f2d-3883f4378d30)
## MODELING
### 1. Random Forest
#### The Random Forest model achieved the following performance metrics:
#### Accuracy: 0.80 (80.26%), 80% 0f the total predictions were correct
#### ROC AUC Score: 0.80
#### Precision: Measures the proportion of positive predictions that were actually correct
##### Class 0: 0.77
##### Class 1: 0.84, has a higher precision, meaning fewer false positives.
#### Recall: Measures the proportion of actual positives correctly identified
##### Class 0: 0.86, has higher recall meaning fewer false negatives
##### Class 1: 0.75
#### F1-Score: Balances precision and recall
##### Class 0: 0.81
##### Class 1: 0.79
### 2. Logistic Regression
#### The Logistic Regression Model achieved the following performance metrics:
#### Accuracy: 0.71 (71.44%), this means that 71.44% of the total predictions were correct.
#### Precision (measures the proportion of predicted positives that are actually positive):
##### Class 0: 0.71
##### Class 1: 0.72. The model has nearly balanced precision for both classes, meaning it has a similar rate of false positives for both.
#### Recall (measures the proportion of actual positives correctly identified):
##### Class 0: 0.72
##### Class 1: 0.71.  The recall values are also very close, meaning the model captures a similar proportion of actual positives in both classes.
#### F1-Score (harmonic mean of precision and recall):
##### Class 0: 0.72
##### Class 1: 0.71. The F1-scores indicate balanced performance between precision and recall for both classes.
### 3. GradientBoostingClassifier Model
#### The Gradient Boosting Classifier Model achieved the following performance metrics:
#### Accuracy: 0.756 (75.62%). The model correctly predicted 75.62% of the test data.
#### Precision (measures the proportion of predicted positives that are actually positive):
##### Class 0: 0.75
##### Class 1: 0.76. The precision values are balanced, indicating a similar false positive rate for both classes.
#### Recall (measures the proportion of actual positives correctly identified):
##### Class 0: 0.77
##### Class 1: 0.74. Class 0 has a slightly higher recall, which correctly identifies more true positives compared to Class 1.
#### F1-Score (harmonic mean of precision and recall):
##### Class 0: 0.76
##### Class 1: 0.75. The F1-scores indicate that the model performs consistently across both classes.
### 4. Support Vector Machine Model
#### The Support Vector Machine (SVM) Model achieved the following performance metrics:
#### Accuracy: 0.768 (76.81%). The model correctly predicted 76.81% of the test data.
#### Precision (proportion of predicted positives that are actually positive):
##### Class 0: 0.74
##### Class 1: 0.80. The model is more precise in predicting Class 1 (positive cases) than Class 0.
#### Recall (proportion of actual positives correctly identified):
##### Class 0: 0.82
##### Class 1: 0.72.  Class 0 has a higher recall, identifying more true negatives, while Class 1 has a slightly lower recall.
#### F1-Score (harmonic mean of precision and recall):
##### Class 0: 0.78
##### Class 1: 0.76. The F1-scores indicate that Class 0 has a slightly better balance between precision and recall compared to Class 1.

#### Best model selection
##### The Random Forest model achieved an accuracy of 80.26%, which has the best accuracy compared to the other models with an ROC AUC score of 0.80 which is near to 1.0 suggesting to be the most model. We shall therefore go ahead and tune the Random Forest Model to improve its performance

### ADVANCED MACHINE LEARNING (Hyperparameter Tuning)
#### The Random Forest model after hyperparameter tuning achieved the following metrics:
#### Accuracy: 0.807 (80.77%). The model correctly classified 80.77% of test cases, making it the best-performing model so far in terms of accuracy.
#### ROC AUC Score: 0.807 (80.73%) Indicating good discrimination between positive and negative classes.
#### Precision (Proportion of predicted positives that are actually positive):
##### Class 0: 0.78
##### Class 1: 0.85. The model is more precise in predicting Class 1 (positive cases) than Class 0.
#### Recall (Proportion of actual positives correctly identified):
##### Class 0: 0.86 (High recall, meaning fewer false negatives)
##### Class 1: 0.75
#### F1-Score (Harmonic mean of precision and recall):
##### Class 0: 0.82
##### Class 1: 0.80. The model balances precision and recall well for both classes.

## CONCLUSION
#### The project aimed to analyze and predict heart disease based on various health-related features. 















