# Group-10-HEART-DISEASE-PREDICTION PROJECT
![image](https://github.com/user-attachments/assets/387869e7-6126-4183-9911-43295e6d41ec)
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
![image](https://github.com/user-attachments/assets/c226556f-7db6-4023-939c-c0fe8e5d9425)

#### Best model selection
##### The Random Forest model achieved an accuracy of 80.26%, which has the best accuracy compared to the other models with an ROC AUC score of 0.80 which is near to 1.0 suggesting to be the most model. We shall therefore go ahead and tune the Random Forest Model to improve its performance

### ADVANCED MACHINE LEARNING (Hyperparameter Tuning)
![image](https://github.com/user-attachments/assets/b75d7484-ddf5-4b56-a689-7668f3a05f7a)


## CONCLUSION
This project aimed to analyze and predict heart disease based on various health-related features. Through Exploratory Data Analysis (EDA), feature engineering, and model evaluation, we derived the following key insights:
1. Dataset Imbalance
- The count plot of patients with and without heart disease revealed an imbalanced dataset. Since an imbalanced dataset can negatively affect model performance, SMOTE (Synthetic Minority Over-sampling Technique) was applied to balance the classes before training machine learning models.
2. Data Distribution and Outliers
- Histogram analysis showed that the numerical features are normally distributed, which is beneficial for machine learning models that assume normality.
- Boxplots confirmed that there were no significant outliers, ensuring that extreme values would not distort predictions.
3. Key Risk Factors for Heart Disease
- A heatmap and feature correlation analysis revealed that features such as cholesterol levels, exercise habits, smoking, and stress levels had the strongest correlation with heart disease. These factors play a critical role in determining a patient's heart disease risk.
4. Feature Encoding
- Label Encoding was applied to transform categorical variables into numerical form. This was essential for incorporating ordinal categorical variables, such as exercise habits, into machine learning models.
5. Feature Importance and Correlation
- The correlation analysis showed BMI, Stress Level, and Homocysteine Level as the highest positively correlated features with heart disease, while Gender, Blood Pressure, and Alcohol Consumption had the lowest correlation.
6. Model Performance Comparison
- Four machine learning models—Random Forest, Logistic Regression, Gradient Boosting, and SVM—were trained and evaluated.
- Random Forest emerged as the best model with an accuracy of 80.25%.
- After hyperparameter tuning and advanced machine learning techniques, the Random Forest model’s accuracy improved from 80.25% to 80.76% with an ROC score of 0.8, indicating strong predictive capability.

## RECOMMENDATION
Based on these findings, the following recommendations are suggested:
1. Public Health Interventions
- Smoking, cholestral level, exercise habits, BMI, stress level and Homocysteine Level are strong indicators of heart disease risk. Awareness programs and lifestyle modification campaigns should be implemented to reduce these risk factors in at-risk populations.
2. Government interventions
- The government should come up with strict punishment such as fines for people who smoke in undesignated places. They can also advice manufacturers to consider filters which are less harmful to the smokers.
- The government should allocate more funds in the health sector to facilitate frequent health camps and mobile clinics which can help in detecting heart diseases early on.
- Additionally they should advice processors to correctly label ingredients such as quantity of sugar for consumer goods, this will aid consumers in their decision-making.
3. Clinical Application of the Model
- The improved Random Forest model (80.76% accuracy, 0.8 ROC score) can be integrated into a clinical decision support system (CDSS) to assist healthcare providers in identifying high-risk patients and making data-driven decisions.
4. Feature Refinement and Further Data Collection
- The correlation analysis showed that some features had minimal impact on heart disease prediction. Future research should focus on acquiring more relevant patient data, such as genetic factors or real-time heart monitoring metrics, to enhance model accuracy.
5. Deploying the Model in a Real-World Setting
- The model can be deployed as a web-based or mobile health application where users can input their health metrics and receive a risk assessment for heart disease. This could serve as an early warning system, prompting individuals to seek medical attention when necessary.
6. Continued Model Optimization
- Further improvements can be achieved through deep learning models, feature selection techniques, and real-time data analysis. Additionally, testing the model on external datasets will help validate its generalizability across different populations.












