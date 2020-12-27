# ANOVA TEST on Continent's female employment rate

Data Analysis Tools - Week 1 

[Back](readme.md)

## Data
Data for this study comes from the Gapminder World Dataset collected by the Gapminder Foundation. The Gapminder World Dataset contains data collected from more than 200 countries/areas for more 500 variables.

## Description of Variables
Below is the description of the variables

1. Continents

2. Female Employment Rate (variable code: femaleemployrate, Unit: Percentage) - Employed females (age > 15) as a percentage of the total female population.
**Female Employment** Rate is the response variable 

**Start with import**   
![](https://snipboard.io/GRmIWp.jpg)

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
### using **Ordinary least squares** function for calculating the F-statistic and associated p value   
![](https://snipboard.io/U6p7Dd.jpg)  
![](https://snipboard.io/J0xkqz.jpg)  
![](https://snipboard.io/RcN9OD.jpg)  
Since our p-value is `0.0455` which is smaller than `0.05`, the data provides significant evidence against the null hypothesis. But, we cannot reject the null hypothesis and accept the alternate hypothesis, right away. To avoid Type I error we need to perform the POST HOC test

## Tukey HSD test   
![](https://snipboard.io/UdHxiR.jpg)   
From the result above we can only say that there is a significant difference between Africa and Asia's female employment rate.

For other pair of continents we fail to reject the NULL Hypothesis
