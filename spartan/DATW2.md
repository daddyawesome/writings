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
