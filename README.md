# DiabeticDataAnalysis
A simple data analysis of diabetic data using python

## 1.	Introduction
The dataset ‘diabetic_data.csv’ contains records of diabetic patients admitted to US hospitals from 1999 to 2008. The goal is to monitor and prevent readmission of patients as this is a metric of potential poor care as well as a financial burden to patients, insurers, governments and health care providers by developing a predictive model that predicts which hospitalized diabetic patients will be readmitted for their condition at a later date and use a K-Means approach to propose a non-trivial set of patients’ clusters that may make business sense to the healthcare industry.

## 2. Exploring the dataset
•	Raw data shape – 101766 rows x 50 columns

![image](https://user-images.githubusercontent.com/80091397/171594145-41b7db3b-aae0-480f-919e-e243f1168fd3.png)

•	As the dataset has many missing values, we can drop columns that has more than fifty percent of missing values such as weight and also dropping columns for which over 95% of their values are the same.

•	Transforming the row column to its middle values, replacing all missing values of diag_1, diag_2, and diag_3 by the number 0 and drop all rows with missing values

•	Removing outliers to only keep values that are within 3 standard deviations away from the mean for each feature of the dataset and removed duplicates in ‘patient_nbr’ column.

•	Shape of the resulting data set - 18807 rows x 33 columns

![image](https://user-images.githubusercontent.com/80091397/171594212-0d04d11c-e055-4f22-a435-1e1b988d89a4.png)

## 3.	Data Exploration
•	Age vs Readmission

The plots below shows that age has higher impact on readmission so the hypothesis age has a higher impact on readmission is true.

![image](https://user-images.githubusercontent.com/80091397/171594529-5e92fa2e-47e8-4746-bf31-c338db48b27c.png)

![image](https://user-images.githubusercontent.com/80091397/171594560-1d1201fe-a2ec-4782-a64d-6d825d6aa42a.png)

•	Ethnic groups vs Readmission

The below shows us that Caucasian group is most likely to be readmitted rather than   African American so the hypothesis African Americans are more likely to be re-admitted than other ethnic group is false.

![image](https://user-images.githubusercontent.com/80091397/171594651-eb613bba-ebec-4d29-8402-6b29df8fa754.png)

•	Gender vs Readmission

As per plot below it can be said that the gender of the patient does not have more effect so the hypothesis Women patients are more likely to be re-admitted than men is false.

![image](https://user-images.githubusercontent.com/80091397/171594738-b6cb8ff3-b0dc-445e-b921-3b34cad7d2fd.png)

•	Primary diagnosis vs Readmission

As shown in the below column diag_1 is compressed into few categories as per Wikipedia and as we can observe diagnosis types have higher impact on re admission rates so the hypothesis Diagnose types have a higher impact on re-admission rates is true.

![image](https://user-images.githubusercontent.com/80091397/171594837-2ae939e0-611c-468d-a877-726e897afc9f.png)

## 4.	Model Building

•	The readmitted column has already been converted to values 0 or 1

•	The pre-processed data has been scaled using MaxAbsScaler to fit and increase model efficiency

•	This are the features for the model 'num_medications', 'number_outpatient', 'number_emergency', 'time_in_hospital', 'number_inpatient', 'encounter_id', 'age', 'num_lab_procedures', 'number_diagnoses', 'num_procedures', 'readmitted'.

•	Confusion matrix

![image](https://user-images.githubusercontent.com/80091397/171594933-6ed487c8-df96-4719-b5ec-a1bc46ffd6b5.png)

![image](https://user-images.githubusercontent.com/80091397/171595004-67889fae-178f-4aa8-9127-f26f87ce97f4.png)

![image](https://user-images.githubusercontent.com/80091397/171595023-0d883a98-5713-429e-a759-3a36cbe16f40.png)

•	Clustering

![image](https://user-images.githubusercontent.com/80091397/171595092-80f5e452-201e-4b4d-b31a-c007c68366d7.png)

![image](https://user-images.githubusercontent.com/80091397/171595130-51c94971-43aa-4bf6-856a-698736656364.png)

![image](https://user-images.githubusercontent.com/80091397/171595178-bd4b8a74-3040-49df-b60f-c3a59f228900.png)

![image](https://user-images.githubusercontent.com/80091397/171595197-291b6556-da88-4b4a-84a0-a705d578833a.png)

