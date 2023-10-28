# dsci-100-project_template
Template project repository for DSCI-100
Xiaoyu Chen, Kerry Li


Title
Heart Disease Prediction


Introduction
Background: 
Heart disease, a prevalent and serious condition affecting the circulatory system, has become a critical public health concern. According to 2017-2018 data from the Canadian Chronic Disease Surveillance System (CCDSS), about 1 in 12 (or 2.6 million) Canadian adults aged 20 and over live with diagnosed heart disease, and every hour, about 14 Canadian adults aged 20 and over with diagnosed heart disease die.

Given the alarming prevalence of heart disease and its associated mortality rates, it is important to establish a model capable of predicting an individual's susceptibility to heart disease. Key factors indicating the risk of developing heart disease include age, resting BP, heart rate, and cholesterol levels.

Question: 
The key question that our project aims to address: 
Can we use the available data for age, resting BP, cholesterol, and MaxHR to predict an individual's susceptibility to heart disease?

Dataset:
The dataset used in this project is called the Heart Failure Prediction Dataset. To meet our goal, we have selected 5 columns, which we refer to as "heart." In the "heart" dataset, there are 214 recorded observations, each with 5 different clinical features:
Age: age of the patient (years)
RestingBP: resting blood pressure (mm Hg)
Cholesterol: serum cholesterol (mm/dl)
MaxHR: maximum heart rate achieved (Numeric value between 60 and 202)
HeartDisease: output class (1: heart disease, 0: Normal)
Preliminary Exploratory Data Analysis


Methods
Objective:
The primary objective of this study is to develop a K-Nearest Neighbors (KNN) regression model to predict the probability of heart disease in patients based on selected physiological and clinical features.
1. Data Preprocessing:
Cleaning: Initial inspection and cleaning of the dataset will be performed to ensure there are no missing or inconsistent data points.
Feature Selection: We have selected the features 'Age', 'Cholesterol', and 'MaxHR' for model training due to their significance in heart disease prediction.
Frequency Encoding: The categorical variable ST_Slope will undergo frequency encoding, where each category will be replaced with its occurrence count in the dataset. This encoded feature will be used alongside the previously mentioned features for model development.
Data Split: The dataset will be partitioned into training and testing subsets. An estimated 80% of the data will serve as the training set, while the remaining 20% will be reserved for model validation.
2. Feature Scaling:
All features, including the frequency-encoded ST_Slope, will undergo standardization using the recipes package from tidymodels. This is crucial for the KNN algorithm, ensuring each feature contributes equally to the distance computation.
3. Model Training:
KNN Classification: The K-Nearest Neighbors classification algorithm will be employed, aiming to categorize patients as having or not having heart disease based on the selected features.
Hyperparameter Tuning: To achieve optimal performance, the number of neighbors 'k' will be tuned using cross-validation techniques.
4. Model Evaluation:
The KNN classification model's efficacy will be gauged using the test subset.



Expected Outcomes and Significance
1.What do you expect to find? 
I expect to determine whether the classifier can accurately predict an individual's susceptibility to heart disease based on the given features.
2.What impact could such findings have?
Early detection is crucial in the management of heart disease. If the classifier proves effective, it could aid in identifying at-risk individuals earlier, potentially leading to timely interventions, better patient outcomes, and reduced healthcare costs.
3.What future questions could this lead to?
How can we further improve the accuracy of the classifier?
What additional features or medical tests could enhance the model's predictive power?
How does the model perform in diverse populations and age groups?
Can the model be integrated into routine medical check-ups for proactive heart disease screening?
Are there other medical conditions that can be predicted using a similar approach?

Please make this 500 words or less without changing the meaning of this.
