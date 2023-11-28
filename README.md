# Contents

1. [Fabric Hackathon for Heart disease prediction](#heart-disease-prediction)


### Heart Disease Prediction

**Scenario**

Heart disease is one of the major causes of fatality in millions of people worldwide. Early detection and diagnosis of heart disease can help prevent complications and improve patient outcomes. In this sample we will use a sample dataset with attributes like age, resting blood pressure, chest pain type, etc. to build a Machine Learning model to aide in decision making and prediction based on the data produced by healthcare sector globally.

data is available [here](https://raw.githubusercontent.com/raghu4sangeeth/Data/master/heartdisease.csv)

Given attributes in the order -

1. age
2. gender
3. chest pain type (4 values – 0 to 3)
4. resting blood pressure
5. cholesterol in mg/dl
6. fasting blood sugar \> 120 mg/dl
7. resting electrocardiographic results (values 0,1,2)
8. maximum heart rate achieved
9. exercise induced angina
10. ldpeak = ST depression induced by exercise relative to rest
11. the slope of the peak exercise ST segment
12. number of major vessels (0-3) colored by flourosopy
13. thal: 0 = normal; 1 = fixed defect; 2 = reversable defect
14. heartdisease: target

**Scope**

Please note the intent of the hackathon is to demonstrate how Fabric can be used for the application of data science and may not represent the best, ideal solution. Also, the dataset used only has limited data and is not meant to be used in real world applications.

**Probable Architecture**

The proposed architecture might look like this. Feel free to use the components of your choice to perform activities. for example: you may chose to use SQL code to clean and transform. 

![image](https://github.com/raghu4sangeeth/Data/assets/34170707/793c13f1-066e-410f-8703-08d0b5dd0daf)

**Recommended Completion**

1. Show creation of lakehouse using Fabric to ingest the data from the sample file. preferably Dataflows, Pipelines and Notebooks. 
2. Use the SQL end point to run queries to understand the data. Sample queries may include - Total number of samples with heart diseases, try identifying missing values etc. Provide screenshots of SQL Queries with results.
3. Clean and Transform the data using your preferred approach. Preferably a note book or stored procedure. You can use describe function in dataframe to see the statistics. 
4. Add cholestorol levels  - <200 healthy, <240 atrisk, rest highrisk. Save it to a delta table along with other data
5. Create an experiment using mlflow to do random split of the data and perform feature engineering.
6. Use [LightGBM classifier](https://lightgbm.readthedocs.io/en/v3.3.2/) to classify the data. show the predictions and metrics.
7. Use Faker package to generate the test data and use the model saved above to start predicting. Save the results as delta table.
8. User Power BI to connect to the saved delta table and display the results. 
