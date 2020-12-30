# Regression Modeling in Practice
## Week 1: Writing About Your Data
Before I dive into a multiple regression analysis of my data, I’ll take a moment to describe some of it.    
    <br>
**Sample**    
I am using the [GapMinder](https://raw.githubusercontent.com/daddyawesome/Coursera_Capstone/master/data/gapminder.csv) dataset to investigate the relationship between internet usage in a country and that country’s GDP, overall employment rate and female employment rate

The sample contains data on a country-level for 215 regions (the 192 U.N. countries, with Serbia and Montenegro aggregated into one, as well as 24 other non-country regions, such as Monaco for instance).    

The study population is these 215 countries and regions and my sample data is the same; ie, the population is small enough that no sample is necessary to make the data collecting and processing more manageable.   

**Data**   
Data for this study comes from the Gapminder World Dataset collected by the [Gapminder Foundation](https://www.gapminder.org/). The Gapminder World Dataset contains data collected from more than 200 countries/areas for more 500 variables.

Description of Variables
Below is the description of the variables
1. Internet User Rate
2. Income per Person
3. Continents    
Continents is Testesd for Potential Moderator   
  
**Procedure**    

The data has been collected by the non-profit venture GapMinder from a handful of sources, including the Institute for Health Metrics and Evaluation, the US Census Bureau’s International Database, the United Nations Statistics Division, and the World Bank. In the case of each data collection organization, data was collected from detailed surveys of the country’s population (such as in a national census) and based mainly upon 2010 data. Employment rate data comes from 2007 and polity score from 2009. Polity score is calculated by subtracting the autocracy score from the democracy score from the Polity IV project’s research. GapMinder’s goal in collecting this data is to help world leaders and their citizens to better understand the forces shaping the geopolitical landscape around the globe.

**Measures**      


My response variable is the internet use rate and my explanatory variables are income per person, employment rate, female employment rate, and polity score. Internet use rate, employment rate, and female employment rate are scaled as percentages of the country’s population. Income per person is simply Gross Domestic Product per capita (the country’s total, country-wide income divided by the population). 
The internet use rate of a country was collected by the World Bank in their World Development Indicators. 
Income per person is simply the 2010 Gross Domestic Product per capita in constant 2000 USD. The inflation, but not the differences in the cost of living between countries, has been taken into account (this can lead to the seemingly odd case of a having negative income per person, when that country already has very low income relative to the United States plus high inflation, relative to the United States).
 Both employment rate and female employment rate have been provided by the International Labour Organization. 
 

I have gone through the data and removed entries where data is missing, when necessary, and sometimes have aggregated data into bins, for histograms, for instance, but otherwise have not modified the data in any way. 

Deeper data management was unnecessary for the analysis.
