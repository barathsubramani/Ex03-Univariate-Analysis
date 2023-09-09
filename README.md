# Ex03-Univariate-Analysis

## Aim:
To read the given data and perform the univariate analysis with different types of plots.

## Explanation:
Univariate analysis is basically the simplest form to analyze data. Uni means one and this means that the data has only one kind of variable. The major reason for univariate analysis is to use the data to describe. The analysis will take data, summarise it, and then find some pattern in the data.

## Algorithm:

Step 1:
Read the given data.

Step 2:
Get the information about the data.

Step 3:
Remove the null values from the data.

Step 4:
Mention the datatypes from the data.

Step 5:
Count the values from the data.

Step 6:
Do plots like boxplots,countplot,distribution plot,histogram plot.

## Code:
```
Name: Barath S
Ref no: 212222230018
```
```python

import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
import seaborn as sns

df = pd.read_csv("iris (2).csv")
df

df.head()

df.tail()

df.nunique()

df.iloc[:,4].value_counts()

for i in range(0, df.shape[1]):
  print("--------",df.columns[i],"--------")
  print(df.iloc[:,i].value_counts())
  print("---------------------------------")

sns.countplot(x = 'species',data = df)

dfv=df.loc[df['species']=='virginica']

plt.plot(dfv['sepal_length'],np.zeros_like(dfv['sepal_length']),'*')
plt.xlabel('sepal length')
plt.show()
##plt.plot(df_setosa['sepal_length'],np.zeros_like(df_setosa['sepal_length']),'o')

dfs=df.loc[df['species']=='setosa']
dfc=df.loc[df['species']=='versicolor']

plt.plot(dfs['sepal_length'],np.zeros_like(dfs['sepal_length']),'*')
plt.plot(dfc['sepal_length'],np.zeros_like(dfc['sepal_length']),'X')

plt.plot(dfv['sepal_length'],np.zeros_like(dfv['sepal_length']),'o')
plt.plot(dfs['sepal_length'],np.zeros_like(dfs['sepal_length']),'*')
plt.plot(dfc['sepal_length'],np.zeros_like(dfc['sepal_length']),'X')
plt.xlabel('petal_length')
plt.show()

plt.plot(dfv['sepal_length'],np.zeros_like(dfv['sepal_length']),'o')
plt.plot(dfs['sepal_length'],np.zeros_like(dfs['sepal_length']),'+')
plt.plot(dfc['sepal_length'],np.zeros_like(dfc['sepal_length']),'-')
plt.xlabel('SEPALLENGTH')
plt.show()
```

## Output:

## DataSet
![image]("https://github.com/barathsubramani/Ex03-Univariate-Analysis/blob/main/df.png")

## df.head()
![image]("https://github.com/barathsubramani/Ex03-Univariate-Analysis/blob/main/head.png")

## df.tail()
![model]("https://github.com/barathsubramani/Ex03-Univariate-Analysis/blob/main/tail.png")

## df.nunique()
![model]("https://github.com/barathsubramani/Ex03-Univariate-Analysis/blob/main/nuni.png")

## df.iloc()
![model]("https://github.com/barathsubramani/Ex03-Univariate-Analysis/blob/main/iloc.png")

## Sepal
![model]("https://github.com/barathsubramani/Ex03-Univariate-Analysis/blob/main/sepal1.png")
![model]("https://github.com/barathsubramani/Ex03-Univariate-Analysis/blob/main/sepal2.png")
![model]("https://github.com/barathsubramani/Ex03-Univariate-Analysis/blob/main/sepal3.png")
![model]("https://github.com/barathsubramani/Ex03-Univariate-Analysis/blob/main/sepal4.png")

## Countplot
![model]("https://github.com/barathsubramani/Ex03-Univariate-Analysis/blob/main/sns.png")

## dfv
![model]("https://github.com/barathsubramani/Ex03-Univariate-Analysis/blob/main/dfv.png")

## dfs
![model]("https://github.com/barathsubramani/Ex03-Univariate-Analysis/blob/main/dfs.png")

## petal_length
![model]("https://github.com/barathsubramani/Ex03-Univariate-Analysis/blob/main/plot.png")

## sepal_length
![model]("https://github.com/barathsubramani/Ex03-Univariate-Analysis/blob/main/last.png")

## Result:
The given datasets are read and outliers are detected and are removed using IQR and z-score methods.
