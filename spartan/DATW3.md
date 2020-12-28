# Pearson's Correlation on Female Employment Rate VS Alcohol Consumption and Female Employment Rate VS Breast Cancer

Data Analysis Tools - Week 3

[Back](readme.md)

## Data
Data for this study comes from the Gapminder World Dataset collected by the Gapminder Foundation. The Gapminder World Dataset contains data collected from more than 200 countries/areas for more 500 variables.

## Description of Variables
Below is the description of the variables

1. Female Employment Rate (variable code: femaleemployrate, Unit: Percentage) - Employed females (age > 15) as a percentage of the total female population.

2. breastcancerper100th - breast cancer per 100

3. alcconsumption - per capita alcohol consumption    
<br>
<br>
**Start with import**   
![](https://snipboard.io/QEczkS.jpg)

### load gapminder dataset

```
data = pd.read_csv('gapminder.csv',low_memory=False)
```
I will be using url to get the data online

![](https://snipboard.io/rXNxDT.jpg)  

![](https://snipboard.io/UrQWHi.jpg)  

## Preparing Data for Graph and Analysis
## Female Employment Rate VS Alcohol Consumption
![](https://snipboard.io/XdoeJ0.jpg)    
<br>
![](https://snipboard.io/kpXG7w.jpg)    
From the result above it shown that there is a **low degree of correlation** between female employ rate and alcconsumption
<br>
<br>
##Female Employment Rate VS Breast Cancer
<br>
![](https://snipboard.io/4onsAa.jpg)    
<br>
From the result above it shown that there is a ***low degree of correlation*** between female employ rate and Breast Cancer
