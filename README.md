# Mini-Project
# DATA ANALYSIS

# AIM:
To Perform Data Analysis on the given dataset and save the data to a file.

# Explanation
Data analytics is important because it helps businesses optimize their performance.Implementing it into the business model means companies can help reduce costs by identifying more efficient ways of doing business and by storing large amounts of data

# ALGORITHM
# STEP 1
Read the given Data

# STEP 2
Clean the Data Set using Data Cleaning Process

# STEP 3
Apply Feature generation and selection techniques to all the features of the data set

# STEP 4
Apply data visualization techniques to identify the patterns of the data.

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
![image](https://github.com/Sahithya7/Mini-Project/assets/133002193/81bb124b-6409-4ace-bf5c-4608a55a0af1)

![image](https://github.com/Sahithya7/Mini-Project/assets/133002193/7e40e591-3026-4ff7-9297-1357a1d852d8)

![image](https://github.com/Sahithya7/Mini-Project/assets/133002193/6f413f97-d6dc-49bd-b237-dfb747215255)

![image](https://github.com/Sahithya7/Mini-Project/assets/133002193/32978a1b-f284-4691-bbe7-68f8c3e6ecdc)

![image](https://github.com/Sahithya7/Mini-Project/assets/133002193/67059c1c-0a9e-47cd-9e26-c302d51e866e)

![image](https://github.com/Sahithya7/Mini-Project/assets/133002193/88a098e9-3e7e-4cbf-a434-1f47f92de3ca)

![image](https://github.com/Sahithya7/Mini-Project/assets/133002193/fa7e47c1-59e7-42d4-8a4a-1ffc1c6a0a01)

![image](https://github.com/Sahithya7/Mini-Project/assets/133002193/7db0b566-3666-443a-8836-d999139f6d14)

![image](https://github.com/Sahithya7/Mini-Project/assets/133002193/20651501-eb93-43d9-818e-d2f614d3154f)

![image](https://github.com/Sahithya7/Mini-Project/assets/133002193/060a4433-d2bb-47f8-9003-1cb55a56a27a)

![image](https://github.com/Sahithya7/Mini-Project/assets/133002193/45f204be-4d59-4248-a983-cc3617163a35)

![image](https://github.com/Sahithya7/Mini-Project/assets/133002193/ec565b90-c429-499c-b201-acef4ac27133)

![image](https://github.com/Sahithya7/Mini-Project/assets/133002193/b2ba9657-05f7-4383-b920-63e82353a62c)

![image](https://github.com/Sahithya7/Mini-Project/assets/133002193/4b12178d-7022-4da2-9bfd-dcff4787f6e8)

![image](https://github.com/Sahithya7/Mini-Project/assets/133002193/4545451b-1c44-4fc5-8168-c20bb6f38d05)

![image](https://github.com/Sahithya7/Mini-Project/assets/133002193/23724ce9-fe89-4bfd-8bc8-a004d1b0a4b0)

# Result:
Thus, Data analysis is performed on the given dataset and save the data to a file
