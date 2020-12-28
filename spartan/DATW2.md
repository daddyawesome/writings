# CHI Square Test of Independence on Continent's female employment rate

Data Analysis Tools - Week 2

[Back](readme.md)

## Data
Data for this study comes from the Gapminder World Dataset collected by the Gapminder Foundation. The Gapminder World Dataset contains data collected from more than 200 countries/areas for more 500 variables.

## Description of Variables
Below is the description of the variables

1. Continents

2. Female Employment Rate (variable code: femaleemployrate, Unit: Percentage) - Employed females (age > 15) as a percentage of the total female population.
**Female Employment** Rate is the response variable 

**Start with import**   
![](https://snipboard.io/QEczkS.jpg)

### load gapminder dataset

```
data = pd.read_csv('gapminder.csv',low_memory=False)
```
I will be using url to get the data online

![](https://snipboard.io/rXNxDT.jpg)  

![](https://snipboard.io/UrQWHi.jpg)  
![](https://snipboard.io/CwpjSe.jpg)  
   
   
**join the two dataframe**   


![](https://snipboard.io/s2ltpV.jpg)  
![](https://snipboard.io/IqVuKC.jpg)  
  
## New DataFrame for Analysis   
We create a dataframe `sub` out from the merge dataframe `df_outer`    
![](https://snipboard.io/Qe3gbB.jpg)  

## Binning the variables

Since we are doing an Chi Square test of Independence, both the response variable and the explanatory variable have to be categorical.

_Binning (categorizing) the response variable_:


Here the response variable **Female Employment Rate** has values between 10 and 90. We would categorize it into two categories.

Female Employment Rate lesser than 70 : Categorized as 0 (Low Female Employment Rate)

Female Employment Rate greater than 70 : Categorized as 1 (High Female Employment Rate)   
   
![](https://snipboard.io/tjfYNJ.jpg)  
<br>
### Choosing the required variables

Selecting only the **Continents** and **Categorize Female Employment Rate** from the data set and dropping the NA values.
![](https://snipboard.io/v1dfm0.jpg)

### Chi Square Test of Indepedence

### Hypothesis Testing

**Null Hypothesis**: There is no association between the Continents and Female Employment Rate.

**Alternative Hypothesis**: There is an association between the Continents and Female Employment Rate.

<br>

![](https://snipboard.io/3TCRXm.jpg)  

### Chi Square Test of Independence
<br>  

![](https://snipboard.io/st3LdR.jpg)   

The **p-value** is 0.00011960497881348971 (< 0.05), which concludes that the Continents and Female Employment Rate are significantly associated. They are not independent. So we can **reject** the **NULL hypothesis**.

## POST HOC Test
Since the explanatory variable has more than 2 levels and the statistical test is significant, we need to perform POST HOC test.
<br>   
### Bonferroni Adjustment
We would need to perform 15 comparisons for the four level of explanatory variable.

Hence the adjusted p-value due to Bonferroni Adjustment would be = 0.05/15 = 0.003333.

We would need to compare against this adjusted p-value of 0.003333.
<br>
![](https://snipboard.io/GVHMDU.jpg)   
<br>
![](https://snipboard.io/nGO5Ra.jpg)   
<br>
![](https://snipboard.io/UQzOCW.jpg)   
<br>
![](https://snipboard.io/0CuR52.jpg)   
<br>
![](https://snipboard.io/n8p4WD.jpg)   
<br>
![](https://snipboard.io/KjIaS6.jpg)   
<br>
![](https://snipboard.io/IaLuGf.jpg)   
<br>
![](https://snipboard.io/qHw82X.jpg)   
<br>
![](https://snipboard.io/d74sfh.jpg)   
<br>
The *p-values* for Comparison 11 (Between Europe and Oceania : 0.001892) and Comparison 7 (Between Asia and Oceania : 6.15627e-05) are less than the adjusted p-value due of 0.0033.

Thus we can only reject the Null hypothesis on these two comparisons.
