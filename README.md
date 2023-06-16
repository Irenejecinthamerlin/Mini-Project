# Mini-Project
## DATA ANALYSIS
# AIM:
To Perform Data Analysis on the given dataset and save the data to a file.

# Explanation
Data analytics is important because it helps businesses optimize their performance.Implementing it into the business model means companies can help reduce costs by identifying more efficient ways of doing business and by storing large amounts of data

# ALGORITHM
# STEP 1

## Read the given Data

# STEP 2

## Clean the Data Set using Data Cleaning Process

# STEP 3

## Apply Feature generation and selection techniques to all the features of the data set

# STEP 4
## Apply data visualization techniques to identify the patterns of the data.

# CODE:
```
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
import seaborn as sns
df=pd.read_csv("/content/ds_salaries.csv",encoding="ISO-8859-1")
dfdf.isnull()
df.info()
df.describe()
sns.lineplot(x="work_year",y="salary",data=df,marker='o')
plt.title("work_year vs salary")
plt.xticks(rotation = 90)
plt.show()

sns.barplot(x="work_year",y="salary",data=df)
plt.xticks(rotation = 90)
plt.show()
df.shape
df1 = df[(df.salary>= 60)]
df1.shape

plt.figure(figsize=(30,8))
states=df1.loc[:,["job_title","salary"]]
states=states.groupby(by=["job_title"]).sum().sort_values(by="salary")
sns.barplot(x=states.index,y="salary",data=states)
plt.xticks(rotation = 90)
plt.xlabel=("job_title")
plt.ylabel=("salary")
plt.show()
plt.figure(figsize=(30,8))
states=df1.loc[:,["job_title","salary"]]
states=states.groupby(by=["job_title"]).sum().sort_values(by="salary")
sns.barplot(x=states.index,y="salary",data=states)
plt.xticks(rotation = 90)
plt.xlabel=("job_title")
plt.ylabel=("salary")
plt.show()
sns.lineplot(x="company_size",y="salary",data=df)
plt.show()
states=df.loc[:,["work_year","salary"]]
states=states.groupby(by=["work_year"]).sum().sort_values(by="salary")
sns.barplot(x=states.index,y="salary",data=states)
plt.xticks(rotation = 90)
plt.xlabel=("work_year")
plt.ylabel=("salary")
plt.show()
df.groupby(['work_year']).sum().plot(kind='pie', y='salary',figsize=(6,9),pctdistance=1.7,labeldistance=1.2)
df["work_year"].corr(df["salary"])
df_corr = df.copy()
df_corr = df_corr[["work_year","salary"]]
df_corr.corr()
sns.pairplot(df_corr, kind="scatter")
plt.show()
grouped_data = df.groupby('employment_type')[['work_year', 'salary']].mean()
# Create a bar chart of the grouped data
fig, ax = plt.subplots()
ax.bar(grouped_data.index, grouped_data['work_year'], label='work_year')
ax.bar(grouped_data.index, grouped_data['salary'], bottom=grouped_data['work_year'], label='salary')
ax.set_xlabel('employment_title')
ax.set_ylabel('Value')
ax.legend()
plt.show()
grouped_data = df.groupby(['job_title', 'company_size'])[['work_year', 'salary']].mean()
pivot_data = grouped_data.reset_index().pivot(index='job_title', columns='company_size', values=['work_year', 'salary'])
# Create a bar chart of the grouped data
fig, ax = plt.subplots()
pivot_data.plot(kind='bar', ax=ax)
ax.set_xlabel('job_title')
ax.set_ylabel('Value')
plt.legend(title='company_size')
plt.show()
```
# OUTPUT:
![image](https://github.com/Irenejecinthamerlin/Mini-Project/assets/128350225/a25317e5-2054-4b80-a166-ddc4a3b2856a)

![image](https://github.com/Irenejecinthamerlin/Mini-Project/assets/128350225/213101f6-265f-41e0-be35-4d72d165bae1)

![image](https://github.com/Irenejecinthamerlin/Mini-Project/assets/128350225/74963a1c-8a68-4944-ac2a-51ba4cebfb53)

![image](https://github.com/Irenejecinthamerlin/Mini-Project/assets/128350225/9c97bfa2-6510-42f3-9d0b-80734cda425b)

![image](https://github.com/Irenejecinthamerlin/Mini-Project/assets/128350225/63b65eeb-0fe7-4b49-90b9-f8af4fd21b67)

![image](https://github.com/Irenejecinthamerlin/Mini-Project/assets/128350225/0f672208-3b94-4265-9092-35521586e863)

![image](https://github.com/Irenejecinthamerlin/Mini-Project/assets/128350225/bcfc76db-f1f5-4d35-b4b2-214765eb0383)

![image](https://github.com/Irenejecinthamerlin/Mini-Project/assets/128350225/50c70aaa-dbd3-4871-ab49-7c23ed246f6c)

![image](https://github.com/Irenejecinthamerlin/Mini-Project/assets/128350225/d685baef-2a57-4874-8cd8-3602caa42a46)

![image](https://github.com/Irenejecinthamerlin/Mini-Project/assets/128350225/07413333-3578-4b52-9751-2458b9da1624)

![image](https://github.com/Irenejecinthamerlin/Mini-Project/assets/128350225/086d859f-7e8f-44bd-8795-05fc70db279c)

![image](https://github.com/Irenejecinthamerlin/Mini-Project/assets/128350225/bf84db31-f326-46de-9b2a-eb0ba1d20bf4)


![image](https://github.com/Irenejecinthamerlin/Mini-Project/assets/128350225/fdcee79e-c18a-42a4-8302-288e4616f5a5)

![image](https://github.com/Irenejecinthamerlin/Mini-Project/assets/128350225/d40690c3-3cba-4e19-84df-3b85730ac836)

![image](https://github.com/Irenejecinthamerlin/Mini-Project/assets/128350225/396c8364-45bb-4460-ac8b-95984c8ab12e)

![image](https://github.com/Irenejecinthamerlin/Mini-Project/assets/128350225/b2145209-f494-4f2c-82c1-10b9d40d5960)

# Result:
Thus, Data analysis is performed on the given dataset and save the data to a file






