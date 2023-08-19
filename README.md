# Ex-01_DS_Data_Cleansing


## AIM
To read the given data and perform data cleaning and save the cleaned data to a file. 

# Explanation
Data cleaning is the process of preparing data for analysis by removing or modifying data that is incorrect ,incompleted , irrelevant , duplicated or improperly formatted. 
Data cleaning is not simply about erasing data ,but rather finding a way to maximize datasets accuracy without necessarily deleting the information. 

# ALGORITHM
### STEP 1
Read the given Data
### STEP 2
Get the information about the data
### STEP 3
Remove the null values from the data
### STEP 4
Save the Clean data to the file

# CODE 
## Data_set
```
import pandas as pd
df=pd.read_csv("/content/Data_set(1).csv")
print(df)

df.head(5)

df.info()

df.isnull()

df.isnull().sum()

df['show_name']=df['show_name'].fillna(df['aired_on'].mode()[0])
df['aired_on']=df['aired_on'].fillna(df['aired_on'].mode()[0])
df['original_network']=df['original_network'].fillna(df['aired_on'].mode()[0])
df.head()

df['rating']=df['rating'].fillna(df['rating'].mean())
df['current_overall_rank']=df['current_overall_rank'].fillna(df['current_overall_rank'].mean())
df.head()

df.head()

df['watchers']=df['watchers'].fillna(df['watchers'].median())
df.head()

df.info()

df.isnull().sum()
```
## Loan_data
```
import pandas as pd
df=pd.read_csv("/content/Loan_Data(1).csv")
print(df)

df.head(5)

df.info()

df.isnull()

df.isnull().sum()

df['Loan_ID']=df['Loan_ID'].fillna(df['Education'].mode()[0])
df['Education']=df['Education'].fillna(df['Education'].mode()[0])
df['Married']=df['Married'].fillna(df['Education'].mode()[0])
df.head()

df['ApplicantIncome']=df['ApplicantIncome'].fillna(df['ApplicantIncome'].mean())
df['LoanAmount']=df['LoanAmount'].fillna(df['LoanAmount'].mean())
df.head()

df.head()

df['Loan_Amount_Term']=df['Loan_Amount_Term'].fillna(df['Loan_Amount_Term'].median())
df.head()

df.info()

df.isnull().sum()
```

# OUTPUT
## Data_set
### Data
![image](https://github.com/vishnupriyaramesh17/ODD2023-Datascience-Ex01/assets/119393589/8c0c8618-cfba-44d1-8319-572ab4844622)
![image](https://github.com/vishnupriyaramesh17/ODD2023-Datascience-Ex01/assets/119393589/7771c4cf-4f42-426d-82a5-b612ac6822a7)

### Non-null before
![image](https://github.com/vishnupriyaramesh17/ODD2023-Datascience-Ex01/assets/119393589/c4da15c3-2d51-44d8-9417-4f7c7e4e7c9d)
![image](https://github.com/vishnupriyaramesh17/ODD2023-Datascience-Ex01/assets/119393589/2f393cb3-b1c0-4726-a85b-c80012d03d97)
![image](https://github.com/vishnupriyaramesh17/ODD2023-Datascience-Ex01/assets/119393589/4c78683d-de45-4bf4-9f5c-77c5dbc2245f)

### Mean
![image](https://github.com/vishnupriyaramesh17/ODD2023-Datascience-Ex01/assets/119393589/f2d14bb6-714f-4519-bd74-479f6a1e275c)

### Mode
![image](https://github.com/vishnupriyaramesh17/ODD2023-Datascience-Ex01/assets/119393589/8132d5a4-0295-41c1-84b1-cfb7916978ee)

### Median
![image](https://github.com/vishnupriyaramesh17/ODD2023-Datascience-Ex01/assets/119393589/a6e735b2-5293-4f29-8425-6595840c822b)

### Non-null after
![image](https://github.com/vishnupriyaramesh17/ODD2023-Datascience-Ex01/assets/119393589/b4bdacff-dfa7-4102-862e-c2dd70de4e43)

## Loan_data
### Data
![image](https://github.com/vishnupriyaramesh17/ODD2023-Datascience-Ex01/assets/119393589/88eb71b7-56b5-4242-9ee3-0aa0b30b07d6)
![image](https://github.com/vishnupriyaramesh17/ODD2023-Datascience-Ex01/assets/119393589/bc5b25f3-2547-41ef-a986-ff9291138398)

### Non-null before
![image](https://github.com/vishnupriyaramesh17/ODD2023-Datascience-Ex01/assets/119393589/d20ca2fc-23b0-4730-be2a-3c2acdac17e7)
![image](https://github.com/vishnupriyaramesh17/ODD2023-Datascience-Ex01/assets/119393589/d7bc73e5-82f9-45a6-b5fb-e194806c0ee7)
![image](https://github.com/vishnupriyaramesh17/ODD2023-Datascience-Ex01/assets/119393589/8a1dffd2-528b-4a92-b9ae-6b7c790a7503)

### Mean
![image](https://github.com/vishnupriyaramesh17/ODD2023-Datascience-Ex01/assets/119393589/21bc5f10-9230-4b9c-af10-3b5d1fe03840)

### Mode
![image](https://github.com/vishnupriyaramesh17/ODD2023-Datascience-Ex01/assets/119393589/8cdad450-c513-4748-af10-b5c984638c93)

### Median
![image](https://github.com/vishnupriyaramesh17/ODD2023-Datascience-Ex01/assets/119393589/aca1bf4c-1fb7-4d45-bffc-239e3a67b29f)

### Non-null after
![image](https://github.com/vishnupriyaramesh17/ODD2023-Datascience-Ex01/assets/119393589/bb81d062-67e1-4662-a093-e1662c4d8a9c)

# RESULT
Thus the given data is read,cleansed and the cleaned data is saved into the file.






