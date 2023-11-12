# Ex:05 Feature Generation
# Aim:
To read the given data and perform Feature Generation process and save the data to a file.
# Explanation:
Feature Generation (also known as feature construction, feature extraction or feature engineering) is the process of transforming features into new features that better relate to the target.
# Algorithm:
STEP 1 :
Read the given Data

STEP 2 :
Clean the Data Set using Data Cleaning Process

STEP 3 :
Apply Feature Generation techniques to all the feature of the data set

STEP 4 :
Save the data to the file
#Program:
```py
NAME : Kanishka.V.s
REG NO : 212222230061
```
# Encoding.csv :
```py
import pandas as pd
df=pd.read_csv('Encoding Data.csv')
df.head()
df['ord_2'].unique()
from sklearn.preprocessing import LabelEncoder,OrdinalEncoder
climate = ['Cold','Warm','Hot']
en= OrdinalEncoder(categories = [climate])
df['ord_2']=en.fit_transform(df[["ord_2"]])
df
le = LabelEncoder()
df['Nom_0'] = le.fit_transform(df[["nom_0"]])
df
!pip install --upgrade category_encoders
from category_encoders import BinaryEncoder
be = BinaryEncoder()
data = be.fit_transform(df['bin_1'])
df  = pd.concat([df,data],axis=1)
df
be = BinaryEncoder()
data = be.fit_transform(df['bin_2'])
df  = pd.concat([df,data],axis=1)
df

```
# Output:
#For encoding.csv file:
![image](https://github.com/kanishka2305/ODD2023-Datascience-Ex-05/assets/113497357/bfafa977-c985-43ac-9949-96b60517c3bd)
![image](https://github.com/kanishka2305/ODD2023-Datascience-Ex-05/assets/113497357/5f72cc96-f044-49d5-b794-c161980def80)
![image](https://github.com/kanishka2305/ODD2023-Datascience-Ex-05/assets/113497357/16f56c79-b508-4cdb-bcaa-14e50a05c1a1)
![image](https://github.com/kanishka2305/ODD2023-Datascience-Ex-05/assets/113497357/d963c454-cfa6-42db-95f0-1cacbcad5fec)
![image](https://github.com/kanishka2305/ODD2023-Datascience-Ex-05/assets/113497357/8fb130a8-f3ca-4e87-944b-f2f8a43a6ad9)
![image](https://github.com/kanishka2305/ODD2023-Datascience-Ex-05/assets/113497357/a2bc1d2e-96b3-4cf8-b646-5ba2eb686c62)

# Data.csv :
```py
import pandas as pd
df1 = pd.read_csv("data.csv")
df1.head()
df1['Ord_1'].unique()
from sklearn.preprocessing import LabelEncoder,OrdinalEncoder
climate = ['Cold','Warm','Hot','Very Hot']
en= OrdinalEncoder(categories = [climate])
df1['Ord_1']=en.fit_transform(df1[["Ord_1"]])
df1
df1['Ord_2'].unique()
cl = ['High School','Diploma','Bachelors','Masters','PhD']
en= OrdinalEncoder(categories = [cl])
df1['Ord_2']=en.fit_transform(df1[["Ord_2"]])
df1
le = LabelEncoder()
df1['City'] = le.fit_transform(df1[["City"]])
df1
from category_encoders import BinaryEncoder
be = BinaryEncoder()
dat = be.fit_transform(df1['bin_1'])
df1  = pd.concat([df1,dat],axis=1)
df1
from category_encoders import BinaryEncoder
be = BinaryEncoder()
data1 = be.fit_transform(df1['bin_2'])
df1  = pd.concat([df1,data1],axis=1)
df1
```
# Output:
#For Data.csv file:
![image](https://github.com/kanishka2305/ODD2023-Datascience-Ex-05/assets/113497357/abbe6f19-2af9-4d68-a84d-f23c1709dfec)
![image](https://github.com/kanishka2305/ODD2023-Datascience-Ex-05/assets/113497357/64368eb0-96be-4d49-a520-b19dfc9e0d7c)
![image](https://github.com/kanishka2305/ODD2023-Datascience-Ex-05/assets/113497357/fafc14aa-2103-437f-878e-8c67ffa9470d)
![image](https://github.com/kanishka2305/ODD2023-Datascience-Ex-05/assets/113497357/f17a7951-1fde-4814-8a51-6e6b35fc0034)
![image](https://github.com/kanishka2305/ODD2023-Datascience-Ex-05/assets/113497357/c895f6bd-4628-488c-8973-bc944206ae5b)
![image](https://github.com/kanishka2305/ODD2023-Datascience-Ex-05/assets/113497357/378fc0f9-a263-4f4c-96a3-9a04f91d7d22)
![image](https://github.com/kanishka2305/ODD2023-Datascience-Ex-05/assets/113497357/ddf58336-8560-4491-a49e-a45c2466b16c)

# BMI.csv file:
```py
import pandas as pd
df2 = pd.read_csv("/content/bmi.csv")
df2.head()
be = BinaryEncoder()
data2 = be.fit_transform(df2['Gender'])
df2  = pd.concat([df2,data2],axis=1)
df2
df2 = pd.get_dummies(df2, prefix=['Index'] ,columns=['Index'])
df2
```
# Output:
#For bmi.csv file:
![image](https://github.com/kanishka2305/ODD2023-Datascience-Ex-05/assets/113497357/38cc5fb3-980c-498d-a182-31f6922fdf5d)
![image](https://github.com/kanishka2305/ODD2023-Datascience-Ex-05/assets/113497357/02594955-9bb2-4110-93f5-6ce311c080d6)
![image](https://github.com/kanishka2305/ODD2023-Datascience-Ex-05/assets/113497357/2ff902ed-e6f9-40ed-9b36-a4f4d57041e2)

# Result:

The Feature Generation process was performed and saved the data to a file.
