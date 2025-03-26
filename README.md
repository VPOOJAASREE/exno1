# Exno:1
NAME: V.POOJAA SREE

REG. NO.: 212223040147

Data Cleaning Process

# AIM:
To read the given data and perform data cleaning and save the cleaned data to a file.

# Explanation:
Data cleaning is the process of preparing data for analysis by removing or modifying data that is incorrect ,incompleted , irrelevant , duplicated or improperly formatted. Data cleaning is not simply about erasing data ,but rather finding a way to maximize datasets accuracy without necessarily deleting the information.

# Algorithm:
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

# OUTPUT:
![4](https://github.com/user-attachments/assets/f29ead14-49f5-4e18-af5d-f6c76b18a75b)


```
df.describe()
```

# OUTPUT:
![5](https://github.com/user-attachments/assets/71b91452-89e1-4332-83ff-12a3aff9afc4)


```
df.shape
```

# OUTPUT:
![6](https://github.com/user-attachments/assets/f481c6e5-b8cd-4a27-bcb3-b093723858e9)


```
df.isnull().sum()
```

# OUTPUT:
![7](https://github.com/user-attachments/assets/2893da31-cf60-44b9-b508-8d5ce8e52bcc)


```
df.nunique()
```

# OUTPUT:
![8](https://github.com/user-attachments/assets/31892dac-8754-4488-864a-cc0df51ff4f9)


```
mn=df.TOTAL.mean()
mn
```

# OUTPUT:
![9](https://github.com/user-attachments/assets/a77a4d0f-ae64-40fc-971c-0b1887e4d03d)


```
df['GENDER'].value_counts()
```

# OUTPUT:
![10](https://github.com/user-attachments/assets/a3eeb1fd-01d4-4b45-8c6f-5a11ddc892c0)


```
df.TOTAL.fillna(mn,inplace=True)
df.M4.fillna(0)
```

# OUTPUT:
![11](https://github.com/user-attachments/assets/327305cc-4af8-4afe-bc47-1b9dc3e428c7)


```
min=df.M4.min()
min
```

# OUTPUT:
![12](https://github.com/user-attachments/assets/a2e6ab2d-56bc-4f08-9ba0-36edcb989bc6)


```
df.M4.fillna(min,inplace=True)
df
```

# OUTPUT:
![13](https://github.com/user-attachments/assets/15603c0f-db4b-40fc-bdfa-36f281201e10)


```
df.isnull()
```

# OUTPUT:
![14](https://github.com/user-attachments/assets/e9cdd8da-d47b-43d0-aeba-051b4d63e82e)


```
import pandas as pd
import seaborn as sns
age=[1,3,28,27,25,92,30,39,40,50,26,24,29,94]
af=pd.DataFrame(age)
af
```

# OUTPUT:
![15](https://github.com/user-attachments/assets/95c3df3f-8792-4820-81da-a51b6e35843b)


```
sns.boxplot(data=af)
```

# OUTPUT:
![16](https://github.com/user-attachments/assets/42016433-7281-4a56-8995-b34df2369c7a)


```
sns.scatterplot(data=af)
```

# OUTPUT:
![17](https://github.com/user-attachments/assets/04c91661-1d2e-4bb4-b7f3-5cf286286660)


```
q1=af.quantile(0.25)
q2=af.quantile(0.5)
q3=af.quantile(0.75)
iqr=q3-q1
iqr
```

# OUTPUT:
![18](https://github.com/user-attachments/assets/5155977d-e9d8-40c4-8d96-d672cc83263c)


```
low=q1-1.5*iqr
low
```

# OUTPUT:
![19](https://github.com/user-attachments/assets/a5f5f09a-2593-43b6-8d42-1fd4d8ff147c)


```
high=q3+1.5*iqr
high
```

# OUTPUT:
![20](https://github.com/user-attachments/assets/1a4a08ab-acad-4c71-b44b-bf6ef7c93996)


```
af=af[((af>=low)&(af<=high))]
af
```

# OUTPUT:
![21](https://github.com/user-attachments/assets/2930763c-e991-4b35-ae72-2a513b05a20d)


```
af.dropna()
```

# OUTPUT:
![22](https://github.com/user-attachments/assets/afb33c78-a7b6-441b-aa1c-ebd4517e474f)


```
sns.boxplot(data=af)
```

# OUTPUT:
![23](https://github.com/user-attachments/assets/048bb54b-41aa-4b81-ac64-b2f572c85e03)


```
data=[1,12,15,18,21,24,27,20,33,36,39,42,45,48,51,54,57,60,63,66,69,72,75,78,81,84,87,90,93,96,99,158]
df=pd.DataFrame(data)
df
```

# OUTPUT:
![24](https://github.com/user-attachments/assets/adfe9ac6-0b94-44e4-91b0-1bfed16fa5f7)


```
import numpy as np
from scipy import stats
z=np.abs(stats.zscore(df))
z
```

# OUTPUT:
![25](https://github.com/user-attachments/assets/add12b9f-a547-49ab-9b0e-70191eb0bd56)


            
# Result:

Thus, we have read the given data and performed data cleaning and saved the cleaned data to a file successfully.
