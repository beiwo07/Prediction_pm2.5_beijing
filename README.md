# Predicting Particulate Matter of 2.5 Microns or Less in Diameter (PM 2.5)

## The Beijing Multi-Site Air-Quality Data

# Background and importance 

PM2.5 is a widespread and inhalable air pollutant with serious health implications, making accurate data on its concentration essential for informing policies aimed at reducing pollution. In developed countries, most urban areas have multiple PM2.5 monitors, with an estimated one monitor per 100,000 to 600,000 residents in Europe and North America (World Health Organization, 2018). However, in less developed regions, air quality monitoring is severely lacking; for instance, sub-Saharan Africa has only one monitor per 15.9 million residents (WHO Global Ambient Air Quality Database, 2016). Given these disparities, my goal focuses on developing a model that leverages available PM2.5 data to predict pollution levels in areas with little to no monitoring.

# Task

My task is a regression task predicting outdoor PM.2.5 (ug/m^3) using the Beijing Multi-site air quality data. The original dataset has 420768 hourly observations over 5 years (2013-17) across 12 air-quality monitoring sites in Beijing, China. The dataframe stores 420768 observation of air quality across 12 sites, each site has data over 5 years with 35064 observation in each year. 

**Disclosure**

Given the large sample size of the data and my computer power, I was not able to perform many model training techniques. For instance, I performed GridSearchCV and RandomSearchCV with 3-folds cross-validation and a few combinations of parameters; I was not able to run it within a reasonable time. So, I decided to add this step in data preprocessing to randomly select a subset of the full dataset, although this might not be the best solution in practice.

[Download the data](https://archive.ics.uci.edu/ml/datasets/Beijing+Multi-Site+Air-Quality+Data)

# Method 

**Attribute information**

- No: row number of observation in each site
- year: year of data in this row
- month: month of data in this row
- day: day of data in this row
- hour: hour of data in this row
- PM2.5: PM2.5 concentration (ug/m^3)
- PM10: PM10 concentration (ug/m^3)
- SO2: SO2 concentration (ug/m^3)
- NO2: NO2 concentration (ug/m^3)
- CO: CO concentration (ug/m^3)
- O3: O3 concentration (ug/m^3)
- TEMP: temperature (degree Celsius)
- PRES: pressure (hPa)
- DEWP: dew point temperature (degree Celsius)
- RAIN: precipitation (mm)
- wd: wind direction
- WSPM: wind speed (m/s)
- station: name of the air-quality monitoring site

  

**Model training & evaluation**

I apply several methods, including simple linear regression model, Lasso regression, support vector regression, decision tree regression, and randomforest regression. General models selection steps are as follow:
- Hyper-parameter tuning: apply GridSearch and a 3-5-folds cross validation in the training set to select the best model
- Evaluate the best model performance in the test set that was set aside
- Error analysis for the final best model

# Results 








