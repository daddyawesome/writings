# Making Data Management Decisions

## Data Management and Visualization - Week 3  

[Back](readme.md)

## Questions: 
1. How employment rate is associated with a high suicide rate?
2. How Income per Person is associated with a high suicide rate? 
3. What is a number of breast cancer cases associated with a high suicide rate?   
	    
To answer this questions we are going to use gapminder data  
   
**Start with import**   
![](https://snipboard.io/QmMIJu.jpg)
### load gapminder dataset  

```
data = pd.read_csv('gapminder.csv',low_memory=False)
```
I will be using url to get the data online (data is store in github)  

![](https://snipboard.io/05JeUS.jpg)  

![](https://snipboard.io/2Y3gkl.jpg)    
    
     
     
**Converting selected columns to numeric dtypes:**    
![](https://snipboard.io/BTN7ad.jpg)    

![](https://snipboard.io/cILP4j.jpg)   
     
          
	     
### Summary Statistics about the Data   
![](https://snipboard.io/cKJogm.jpg)   
      
### Install sidetable   
- sidetable is a powerful tool for making summary table.   
![](https://snipboard.io/Sp09vX.jpg)   
     
## Statistics for Suicide Rates   
![](https://snipboard.io/YOhlnx.jpg)   
   
![](https://snipboard.io/Qh4oHI.jpg)   

Our new dataframe `sub_copy` contains all data with high suicide rate which we going to compare with employment rate, income per person and breast canrcer rate.     
      
          
	  
## Employment Rate Versus Suicide Rate   

![](https://snipboard.io/jERdzk.jpg)   
![](https://snipboard.io/csDYCj.jpg)   
From the frequency distribution above we are able to determine that group 2 which belongs to 51 to 59 employment rate has the highest number of suicide rate.     
    
         
## Income per Person Versus Suicide Rate   
![](https://snipboard.io/8W5tM3.jpg)    
![](https://snipboard.io/WhptDL.jpg)     
From the frequency table above we found out that there is no significant difference between quartiles when it come to high suicide rate.   
    
    
## BREAST CANCER RATE versus High Suicide Rate
![](https://snipboard.io/bhXdkr.jpg)  

For the breast cancer rate, I grouped the data into 4 groups by number of breast cancer cases (1-23, 24-46, 47-69, 70-92) using `pandas.cut` function.   
People with lower breast cancer rate experience a high suicide rate. 
