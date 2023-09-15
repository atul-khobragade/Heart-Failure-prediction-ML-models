Heart Failure Prediction
 Project Report


ABSTRACT
 In this report we will predict the chance of heart failure by applying machine learning techniques. The work is to design and develop models to  predict heart failure rate. With the advanced development in machine learning (ML), artificial intelligence (AI) and data science has been shown to be effective in assisting in decision making and predictions from the large quantity of data produced by the healthcare industry.
INTRODUCTION
Cardiovascular disorders(CVDs) are a common cause of heart failure. People who have cardiovascular disease or are at high cardiovascular risk due to one or more risk factors such as hypertension, diabetes, hyperlipidemia, or previously existing disease require early detection and management, which a machine learning model can provide.
DATA SET DESCRIPTION
The classification goal is to predict whether the patient has Cardiovascular disorders(CVDs) or not. The data set provides the patients’ information. It includes 918 records and 11 attributes. Each attribute is a potential risk factor. There are both demographic and medical risk factors.
Attributes:
Demographic:
Age: age of the patient [years]
Sex: sex of the patient [M: Male, F: Female]
Information on medical records:
ChestPainType: chest pain type [TA: Typical Angina, ATA: Atypical Angina, NAP: Non-Anginal Pain, ASY: Asymptomatic]
RestingBP: resting blood pressure [mm Hg]
Cholesterol: serum cholesterol [mm/dl]
FastingBS: fasting blood sugar [1: if FastingBS > 120 mg/dl, 0: otherwise]
RestingECG: resting electrocardiogram results [Normal: Normal, ST: having ST-T wave abnormality (T wave inversions and/or ST elevation or depression of > 0.05 mV), LVH: showing probable or definite left ventricular hypertrophy by Estes' criteria]
MaxHR: maximum heart rate achieved [Numeric value between 60 and 202]
ExerciseAngina: exercise-induced angina [Y: Yes, N: No]
Oldpeak: oldpeak = ST [Numeric value measured in depression]
ST_Slope: the slope of the peak exercise ST segment [Up: upsloping, Flat: flat,  Down: downsloping]

Target variable to predict:
Predicting Cardiovascular disorders (CVDs) — (binary: “1”, means “There is a heart failure”, “0” means “Normal”)
METHODOLOGY
The full code is implemented in Python and different classification algorithms are used. Below is a brief description of the general approach employed:
Data cleaning and preprocessing: Here we checked  if there is any null value in any row or duplicate variables from the data set as these can grossly affect the performance of different machine learning algorithms.
Exploratory Data Analysis: Here we wanted to gain important statistical insights from the data and the things that we checked for were the distributions of the different attributes, correlations of the attributes with each other, and the target variable and we calculated important odds and proportions for the categorical attributes.
  
Model development and comparison: We used five classification models, i.e., Random Forest Classifier, K-Neighbors, Decision Trees, XGboost Classifier, and LightGBM Classifier, After which we compared the performance of the models using their accuracy and F1 score.
EXPERIMENTATION
Model Development And Comparison:
Using the training set, we trained the above-mentioned five classifiers, after training each model and tuning their hyper-parameters using random search, we evaluated and compared their performance using the Accuracy score,  F1 Score, Precision Score, and ROC, as follows:
Random Forest Classifier

Hyper-parameters:
{'n_estimators': 275, 'min_samples_split': 5, 'min_samples_leaf': 4, 'max_features': 'log2', 'max_depth': 15, 'criterion': 'entropy'}


K-Neighbors Classifier

Hyper-parameters:
{'weights' : 'distance', 'p': 1, 'n_neighbors' : 7, 'leaf_size' : 36}
Decision Trees Classifier
 
Hyper-parameters:
{'splitter': 'best', 'min_samples_split': 7, 'min_samples_leaf': 7, 'max_features': 'auto', 'max_depth': 7, 'criterion': 'entropy'}
XGboost Classifier
 
Hyper-parameters:
{'n_estimators': 39, 'max_depth': 3}
LightGBM Classifier
 
Hyper-parameters:
{'num_leaves': 75, 'min_split_gain': 0.01, 'min_data_in_leaf': 11, 'max_depth': 4, 'learning_rate': 0.04, 'colsample_bytree': 0.4}
RESULT
The XGboost Classifier was the best performing model across all metrics. Its high Accuracy and F1 score also show that the model has a high true positive rate and is thus sensitive to predict if one has a CVD or not.




# Heart-Failure-prediction
