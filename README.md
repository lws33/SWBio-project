# SWBio-project
A repository for the SWBio Data Science and Machine Learning project

What does the code do?

This short project analyses the breast cancer dataset from Scikit-learn. The key point of this analysis is to identify certain variables in the dataset which can be used to predict cancer with a good level of accuracy. This analysis utilises a logistic regression, and due to the binary classification of benign or cancerous, further utilises a classification report to identify accuracy, precision, and recall of the model.

The following libraries and functions are required to be imported for this code to run:
•	pandas as pd
•	numpy as np
•	matplotlib.pyplot as plt
•	seaborn as sns
•	from sklearn.model_selection import train_test_split
•	from sklearn.linear_model import LogisticRegression
•	from sklearn import metrics
•	from sklearn.metrics import classification_report


As this is a model dataset from Scikit-learn, it can be directly loaded in using the following code which generates a pandas dataframe:

from sklearn.datasets import load_breast_cancer
cancer = load_breast_cancer()
df =  pd.DataFrame(cancer.data, columns = cancer.feature_names)


To access the classification information (cancer or benign) in the data for the analysis performed here, the following code is required:

df["target"] = cancer.target


A brief breakdown of the workflow of the notebook:

I.	Data loading 
II.	Visualising and exploring the data
III.	Splitting the data by classification and descriptive statistics
IV.	Logistic regression modelling 
V.	Evaluation of the model 
VI.	Visualisation of the model
VII.	Classification report for model prediction and accuracy


A brief summary of the results:

•	Some variables are highly correlated whilst most show no relationship to each other
•	Descriptive statistics revealed mean radius and mean perimeter are variables which differ between cancer and benign classification
•	The logistic regression has a good model score with a good level of accuracy (~90% - please note the exact result will change each time the code is run due to the training of the model here) 
•	The logistic regression model could be further improved
•	The classification report demonstrates that the model is slightly better at predicting benign tumours 
o	This may be explained by greater training on benign data and an uneven split in the dataset (benign vs cancer)
![image](https://github.com/lws33/SWBio-project/assets/153205117/a077a88e-68e4-4fc5-afa4-8a8be6a413c0)
