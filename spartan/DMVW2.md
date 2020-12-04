# First Pyhon Program

Data Visualization - Week 2 

[Back](readme.md)

## Question
How employment rate is associated with a high suicide rate? 
- to answer this we use gapminder data.

**Start with import**
```
import pandas as pd
import numpy as np
```


### load gapminder dataset

I will be using url to get the data online (data is store online)

```
url = 'https://raw.githubusercontent.com/daddyawesome/Coursera_Capstone/master/data/gapminder.csv'
data = pd.read_csv(url)

data
```
![](https://snipboard.io/UILc3a.jpg)
```
# lower-case all DataFrame column names
data.columns = map(str.lower, data.columns)
# bug fix for display formats to avoid run time errors
pd.set_option('display.float_format', lambda x:'%f'%x)
data.dtypes
```
![](https://snipboard.io/zM2vme.jpg)
**Converting selected columns to numeric dtypes:**
```
cols = data.columns.drop('country')
data[cols] = data[cols].apply(pd.to_numeric, errors='coerce')

data.dtypes
```
![](https://snipboard.io/tWzn8R.jpg)
### Summary Statistics about the Suicide Data
```
print("Statistics for a Suicide Rate")
print(data['suicideper100th'].describe())
```

![](https://snipboard.io/s7ECeT.jpg)

Employment Rate Versus Suicide Rate

```
# EMPLOYMENT RATE
# frequency and percentage distritions for employment rate with a high suicide rate
print('frequency for employment rate with a high suicide rate')
ec = sub_copy['employrate'].value_counts(sort=False,bins=10)
print(ec)

print('percentage for employment rate with a high suicide rate')
pec = sub_copy['employrate'].value_counts(sort=False,bins=10,normalize=True)*100
print(pec)

# cumulative frequency and cumulative percentage for employment rate with a high suicide rate
ec1=[] # Cumulative Frequency
pec1=[] # Cumulative Percentage
cf=0
cp=0
for freq in bc:
    cf=cf+freq
    ec1.append(cf)    
    pf=cf*100/len(sub_copy)
    pec1.append(pf)
print('cumulative frequency for employment rate with a high suicide rate')
print(ec1)
print('cumulative percentage for employment rate with a high suicide rate')
print(pec1)
```

![](https://snipboard.io/Bc9R7J.jpg)
```
print('Employment Rate with a High Suicide Rate')
fmt1 = '%5s %12s %9s %12s %12s'
fmt2 = '%5.2f %10.d %10.2f %10.d %12.2f'
print(fmt1 % ('Rate','Freq.','Percent','Cum. Freq.','Cum. Percent'))
for i, (key, var1, var2, var3, var4) in enumerate(zip(ec.keys().left,ec,pec,ec1,pec1)):
    print(fmt2 % (key, var1, var2, var3, var4))
fmt3 = '%5s %10s %10s %10s %12s'   
print(fmt3 % ('NA', '2', '3.77', '53', '100.00'))
```
![](https://snipboard.io/ySXekc.jpg)

## Answer to question
The high suicide rate occurs at 55% of employment rate.
