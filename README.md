# Exno:1 - Data Cleaning Process

# AIM
To read the given data and perform data cleaning and save the cleaned data to a file.

# Explanation
Data cleaning is the process of preparing data for analysis by removing or modifying data that is incorrect ,incompleted , irrelevant , duplicated or improperly formatted. Data cleaning is not simply about erasing data ,but rather finding a way to maximize datasets accuracy without necessarily deleting the information.

# Algorithm

STEP 1:

Read the given Data

STEP 2:

Get the information about the data

STEP 3:

Remove the null values from the data

STEP 4: 

Save the Clean data to the file

STEP 5: 

Remove outliers using IQR

STEP 6: 

Use zscore of to remove outliers

# code

DEVELOPED BY: KANISHKAR M

REGISTER NUMBER: 212222240044

```PY
import pandas as pd
df=pd.read_csv("/content/Data_set.csv")
print(df)
df.head(5)
df.info()
df.isnull().sum()
df['show_name']=df['show_name'].fillna(df['aired_on'].mode()[0])
df['aired_on']=df['aired_on'].fillna(df['aired_on'].mode()[0])
df['original_network']=df['original_network'].fillna(df['aired_on'].mode()[0])
df.head()
df['rating']=df['rating'].fillna(df['rating'].mean())
df['current_overall_rank']=df['current_overall_rank'].fillna(df['current_overall_rank'
df.head()
df['watchers']=df['watchers'].fillna(df['watchers'].median())
df.head()
df.info()
df.isnull().sum()
```
# output
![image](https://github.com/Praveen0500/exno1/assets/120218611/d4d4254e-bf3d-4f4c-93c3-14f951a45106)

![image](https://github.com/Praveen0500/exno1/assets/120218611/4e40ffda-9511-44ba-8ae8-f1e568a98df8)

![image](https://github.com/Praveen0500/exno1/assets/120218611/0874d02b-b0e3-41da-83c5-2150198d1855)

![image](https://github.com/Praveen0500/exno1/assets/120218611/12628fa2-4891-4784-a637-8f79316694f1)

# mode
![image](https://github.com/Praveen0500/exno1/assets/120218611/749d7cf0-6ca1-4c74-adc7-2e16def50e9b)


# mean
![image](https://github.com/Praveen0500/exno1/assets/120218611/876ae87e-6156-4141-8cf8-5e03e8ccc516)


# median
![image](https://github.com/Praveen0500/exno1/assets/120218611/7eff1583-927c-490d-b576-3c8a60ddf58d)



# after clean
![image](https://github.com/Praveen0500/exno1/assets/120218611/d1de89a6-b9ba-472c-8054-4f9e25f0f963)

![image](https://github.com/Praveen0500/exno1/assets/120218611/8f4189b7-b714-4087-b9ca-ad56e2db8fea)

# Result
 Thus the given data is read,cleansed and the cleaned data is saved into the file.
