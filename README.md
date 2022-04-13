# Ex-04-EDA
# AIM:
To perform EDA on the given data set.

# EXPLANATION:
The primary aim with exploratory analysis is to examine the data for distribution, outliers and anomalies to direct specific testing of your hypothesis.

# ALGORITHM:
### STEP 1:
Import the required packages(pandas,numpy,seaborn).

### STEP 2:
Read the given .csv file.

### STEP 3:
Convert the file into a dataframe and get information of the data.

### STEP 4:
Remove the non numerical data columns using drop() method.

### STEP 5:
Replace the null values using (.fillna).

### STEP 6:
Returns object containing counts of unique values using (value_counts()).

### STEP 7:
Plot the counts in the form of Histogram or Bar Graph.

### STEP 8:
Find the pairwise correlation of all columns in the dataframe(.corr()).

### STEP 9:
Save the final data set into the file.

## CODE:
~~~
import pandas as pd
import numpy as np
import seaborn as sns
df=pd.read_csv("supermarket.csv")
df.info()
df.head()
df.tail()
df.isnull().sum()
df["City"].value_counts()
df["Gender"].value_counts()
df["Payment"].value_counts()
sns.countplot(x="Invoice ID",data=df)
sns.countplot(x="Total",data=df)
sns.countplot(x='gross income',data=df)
sns.countplot(x='Payment',data=df)
sns.displot(df["cogs"])
sns.countplot(x="Gender",hue="Quantity",data=df)
sns.displot(df[df["Product line"]==0]["Total"])
pd.crosstab(df["Payment"],df["Quantity"])
pd.crosstab(df["Gender"],df["Quantity"])
df.corr()
sns.heatmap(df.corr(),annot=True)
~~~
## OUTPUT:
![1](https://user-images.githubusercontent.com/94980741/163091267-7c097a9d-aac8-4086-9223-a231073062b1.png)

![2](https://user-images.githubusercontent.com/94980741/163091324-065e64b8-4648-4331-97e5-e67ff1833071.jpg)

![15](https://user-images.githubusercontent.com/94980741/163091371-4fd7f16c-326a-4b10-88c3-6453cf48196a.jpg)

![3](https://user-images.githubusercontent.com/94980741/163091424-4eaca048-d796-428e-938c-cb73c07a90c5.png)

![4](https://user-images.githubusercontent.com/94980741/163091444-ba813571-cbf5-4e24-9a61-7db70d9b957f.png)

![5](https://user-images.githubusercontent.com/94980741/163091475-88c80f1d-d0f7-4fe8-bbc1-feb275e7bbc7.jpg)

![6](https://user-images.githubusercontent.com/94980741/163091495-3499d10a-853c-46a7-94f1-759c3e896edd.jpg)

![7](https://user-images.githubusercontent.com/94980741/163091531-4ffaafd7-bcd6-4d10-929e-c8f52703b8bc.jpg)

![8](https://user-images.githubusercontent.com/94980741/163091571-afeb326a-ba83-47bd-953f-85c720eb937d.jpg)

![9](https://user-images.githubusercontent.com/94980741/163091599-25a81bcf-9e22-4eab-9c85-c8a2eab5c689.jpg)

![10](https://user-images.githubusercontent.com/94980741/163091633-16fcdae9-84fe-4442-8497-f14f9c7d1881.jpg)

![11](https://user-images.githubusercontent.com/94980741/163091655-11578afa-8a1b-4f55-9e75-604fe3beef0d.jpg)

![11](https://user-images.githubusercontent.com/94980741/163091686-5fac6a5c-0aa3-4e22-a8aa-c0557fc3b134.jpg)

![12](https://user-images.githubusercontent.com/94980741/163091734-2b35776e-2acd-4439-a030-374c8f930458.jpg)

![13](https://user-images.githubusercontent.com/94980741/163091755-3d5bb4c0-a5b2-4208-9ea6-320c655052f1.jpg)


## Result:
Thus the Exploratory Data Analysis (EDA) on the given data set is successfully completed.
