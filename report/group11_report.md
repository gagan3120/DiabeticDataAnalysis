1. **Introduction**

The dataset ‘diabetic\_data.csv’ contains records of diabetic patients admitted to US hospitals from 1999 to 2008. The goal is to monitor and prevent readmission of patients as this is a metric of potential poor care as well as a financial burden to patients, insurers, governments and health care providers by developing a predictive model that predicts which hospitalized diabetic patients will be readmitted for their condition at a later date and use a K-Means approach to propose a non-trivial set of patients’ clusters that may make business sense to the healthcare industry.

1. **Exploring the dataset**
- Raw data shape – 101766 rows x 50 columns

![](Aspose.Words.652e5f28-cae2-4ac8-a6b8-31a83344792c.001.png)

- As the dataset has many missing values, we can drop columns that has more than fifty percent of missing values such as weight and also dropping columns for which over 95% of their values are the same.
- Transforming the row column to its middle values, replacing all missing values of diag\_1, diag\_2, and diag\_3 by the number 0 and drop all rows with missing values
- Removing outliers to only keep values that are within 3 standard deviations away from the mean for each feature of the dataset and removed duplicates in ‘patient\_nbr’ column.
- Shape of the resulting data set - 18807 rows x 33 columns

![](Aspose.Words.652e5f28-cae2-4ac8-a6b8-31a83344792c.002.png)

1. **Data Exploration**
- Age vs Readmission

The plots below shows that age has higher impact on readmission so the hypothesis age has a higher impact on readmission is true.

![](Aspose.Words.652e5f28-cae2-4ac8-a6b8-31a83344792c.003.png)

![](Aspose.Words.652e5f28-cae2-4ac8-a6b8-31a83344792c.004.png)

- Ethnic groups vs Readmission

The below shows us that Caucasian group is most likely to be readmitted rather than   African American so the hypothesis African Americans are more likely to be re-admitted than other ethnic group is false.

`       `![](Aspose.Words.652e5f28-cae2-4ac8-a6b8-31a83344792c.005.png)

- Gender vs Readmission

As per plot below it can be said that the gender of the patient does not have more effect so the hypothesis Women patients are more likely to be re-admitted than men is false.

`        `![](Aspose.Words.652e5f28-cae2-4ac8-a6b8-31a83344792c.006.png)

- Primary diagnosis vs Readmission

As shown in the below column diag\_1 is compressed into few categories as per Wikipedia and as we can observe diagnosis types have higher impact on re admission rates so the hypothesis Diagnose types have a higher impact on re-admission rates is true.

`                   `![](Aspose.Words.652e5f28-cae2-4ac8-a6b8-31a83344792c.007.png)





1. **Model Building**
- The readmitted column has already been converted to values 0 or 1
- The pre-processed data has been scaled using MaxAbsScaler to fit and increase model efficiency
- This are the features for the model 'num\_medications', 'number\_outpatient', 'number\_emergency', 'time\_in\_hospital', 'number\_inpatient', 'encounter\_id', 'age', 'num\_lab\_procedures', 'number\_diagnoses', 'num\_procedures', 'readmitted'.
- Confusion matrix

`               `![](Aspose.Words.652e5f28-cae2-4ac8-a6b8-31a83344792c.008.png)

![](Aspose.Words.652e5f28-cae2-4ac8-a6b8-31a83344792c.009.png)![](Aspose.Words.652e5f28-cae2-4ac8-a6b8-31a83344792c.010.png)

- Clustering

![](Aspose.Words.652e5f28-cae2-4ac8-a6b8-31a83344792c.011.png)

![](Aspose.Words.652e5f28-cae2-4ac8-a6b8-31a83344792c.012.png)![](Aspose.Words.652e5f28-cae2-4ac8-a6b8-31a83344792c.013.png)

![](Aspose.Words.652e5f28-cae2-4ac8-a6b8-31a83344792c.014.png)
