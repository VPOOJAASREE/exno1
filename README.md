# Exno:1
NAME: V.POOJAA SREE

REG. NO.: 212223040147

Data Cleaning Process

# AIM
To read the given data and perform data cleaning and save the cleaned data to a file.

# Explanation
Data cleaning is the process of preparing data for analysis by removing or modifying data that is incorrect ,incompleted , irrelevant , duplicated or improperly formatted. Data cleaning is not simply about erasing data ,but rather finding a way to maximize datasets accuracy without necessarily deleting the information.

# Algorithm
STEP 1: Read the given Data

STEP 2: Get the information about the data

STEP 3: Remove the null values from the data

STEP 4: Save the Clean data to the file

STEP 5: Remove outliers using IQR

STEP 6: Use zscore of to remove outliers

# Coding and Output:

```
import pandas as pd
df=pd.read_csv('/content/SAMPLEIDS.csv')
df
```

# OUTPUT:
![1](https://github.com/user-attachments/assets/d176f421-3bc0-472f-ab88-1a6ef3962ff4)


```
df.head(5)
```

# OUTPUT:
![2](https://github.com/user-attachments/assets/b8f433f2-f7c1-4b9c-a9e1-d5253b0f8b0b)


```
df.tail(5)
```

# OUTPUT:
![3](https://github.com/user-attachments/assets/37bc2874-5b34-4a17-b359-4b2df0b463f8)


```
df.info()
```
OUTPUT:
![4](https://github.com/user-attachments/assets/f29ead14-49f5-4e18-af5d-f6c76b18a75b)


```
df.describe()
```
OUTPUT:
![5](https://github.com/user-attachments/assets/71b91452-89e1-4332-83ff-12a3aff9afc4)


```
df.shape
```
OUTPUT:
![6](https://github.com/user-attachments/assets/f481c6e5-b8cd-4a27-bcb3-b093723858e9)


```
df.isnull().sum()
```
OUTPUT:
![7](https://github.com/user-attachments/assets/2893da31-cf60-44b9-b508-8d5ce8e52bcc)


```
df.nunique()
```
OUTPUT:
![8](https://github.com/user-attachments/assets/31892dac-8754-4488-864a-cc0df51ff4f9)


```
mn=df.TOTAL.mean()
mn
```
OUTPUT:
![9](https://github.com/user-attachments/assets/a77a4d0f-ae64-40fc-971c-0b1887e4d03d)


```
df['GENDER'].value_counts()
```
OUTPUT:
![10](https://github.com/user-attachments/assets/a3eeb1fd-01d4-4b45-8c6f-5a11ddc892c0)


```
df.TOTAL.fillna(mn,inplace=True)
df.M4.fillna(0)
```
OUTPUT:
![11](https://github.com/user-attachments/assets/327305cc-4af8-4afe-bc47-1b9dc3e428c7)


```
min=df.M4.min()
min
```
OUTPUT:
![12](https://github.com/user-attachments/assets/a2e6ab2d-56bc-4f08-9ba0-36edcb989bc6)


```
df.M4.fillna(min,inplace=True)
df
```
OUTPUT:
![13](https://github.com/user-attachments/assets/15603c0f-db4b-40fc-bdfa-36f281201e10)


```
df.isnull()
```
OUTPUT:
![14](https://github.com/user-attachments/assets/e9cdd8da-d47b-43d0-aeba-051b4d63e82e)


```
import pandas as pd
import seaborn as sns
age=[1,3,28,27,25,92,30,39,40,50,26,24,29,94]
af=pd.DataFrame(age)
af
```
OUTPUT:


```
sns.boxplot(data=af)
```
OUTPUT:


```

```
OUTPUT:


```

```
OUTPUT:


```

```
OUTPUT:


```

```
OUTPUT:


```

```
OUTPUT:


```

```
OUTPUT:


```

```
OUTPUT:


```

```
OUTPUT:


            
# Result
          <<include your Result here>>
