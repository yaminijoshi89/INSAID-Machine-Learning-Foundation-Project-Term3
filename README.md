# Machine Learning Foundation Project (Term3)
#### Myocardial Infarction prediction Project 
__[Classification project]__

![title](mifem1.PNG)

__Contents of the PPT:__
1. Understanding Myocardial Infarction

2. Objective of Analysis and Data-Set Description EDA :

  - Age Distribution
  - Year Wise Outcome Frequency
  - Smoking Status
  - MI Symptoms Box-plots
  - MI Symptoms Frequency as per outcome
  - Survival and Mortality Ratio Pie-Chart
  - Correlation between Categorical Variables
  - Exploratory Data Analysis Summary
   
3. Classification Model Selection 

4. Model Selection and Evaluation (Confusion Matrix and Accuracy Score)

5. Model Evaluation using AUC/ROC Curve

6. Conclusion 

Myocardial Infarction is medical name of a heart attack. Heart Attack is caused by regular blockage in oxygen flow to the heart. 
Most heart attacks result from atherosclerosis (Narrowing and hardening of arteries due to a build-up of plaque round artery wall). Due to this build-up, the oxygen flow reduces and the arteries are damaged which result in heart attack or stroke. The risk factors for heart attack and atherosclerosis are basically the same: High BP, High Cholesterol, Diabetes, poor diet, no physical activity etc.

In early middle age, men have a greater risk of heart attack than women. However, a woman's risk increases once she begins menopause. This could be the result of a menopause-related decrease in levels of estrogen, a female sex hormone that may offer some protection against atherosclerosis.

## OBJECTIVE:

We are going to study/analyse mortality outcomes for females suffering from Myocardial Infarction.Each point in the dataset have had a case of myocardial infarction in past. According to sources, the common causes of MI are diabetes, old age, high cholesterol, poor diet, no exercise etc. Now, the objective of this research will be to find out whether these underlying causes actually contribute to MI or not. Also, the severity (dead or live) might depend on the underlying causes.

## Data Description

Our data have following explanatory/independent variables:
1. age (age at onset) : Age of the person when first diagnosed with MI
2. yronset (year of onset) : Year when the diagnosis took place
3. premi (previous myocardial infarction event, a factor with levels y, n, nk not known ) :  Value indicating MI event after diagnosis
4. Smstat (smoking status, a factor with levels c current, x ex-smoker, n non-smoker, nk not known) 
5. diabetes (a factor with levels y, n, nk not known)
6. highbp (high blood pressure, a factor with levels y, n, nk not known )
7. hichol (high cholesterol, a factor with levels y, n nk not known)
8. angina (a factor with levels y, n, nk not known) : Type of chest pain caused due to reduced blood flow to the heart
9. stroke (a factor with levels y, n, nk not known)

And target/response (dependent) variable:
10. outcome (mortality outcome, a factor with levels live, dead)

#### Models Used -
- Logistic Regression
- Decision Tree
- Random Forest 

#### Oversampling using SMOTE
-- In our dataset, we have two outcome classes 'live' or 'dead'. Since 75% of our data comprise of outcome 'live' and 25% 'dead', this leads to unbalanced classes. This means that if we use this data for prediction and it predicts every new data point as 'live', it would still be 75% accurate. But we still need to identify 'dead' outcome cases, to study the symptoms more accurately.
For this we do oversampling, using SMOTE we increase the data points of scarce class and bring it equal to the   other class.

#### Cross-validation using K-Fold
-- Using K-fold we divide the dataset K times (here K is any number) into train-test and check the model's accuracy on K different test data. Finally we take mean accuracy of all K runs and decide the best model or get an idea of model accuracy. 

#### Model Evaluation
- Confusion Matrix
- Accuracy Scores
- AUC/ROC curve
