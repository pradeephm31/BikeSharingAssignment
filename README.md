# Bike Sharing Assignment
> BoomBikes, a bike-sharing provider, has experienced a significant drop in revenue due to the pandemic and is seeking ways to recover once the economy stabilizes. To prepare for the post-lockdown demand, the company aims to understand the factors that influence bike-sharing demand in the American market. With a dataset on daily bike demand, including variables like weather conditions and demographic trends, BoomBikes plans to build a model that predicts bike demand based on these factors. This model will allow the company to gain insights into demand patterns, enabling them to adjust their business strategy accordingly to meet customer expectations and optimize service delivery as the market recovers.


## Table of Contents
* [General Info](#general-information)
* [Technologies Used](#technologies-used)
* [Conclusions](#conclusions)
* [Acknowledgements](#acknowledgements)

## General Information
- Problem Statement
	-  &nbsp;&nbsp;&nbsp;&nbsp;BoomBikes, a U.S. bike-sharing company, seeks to understand factors that impact the demand for shared bikes, particularly after the COVID-19 pandemic and lockdown.

- Data Set
	- Days Data Set was considered which has all the attributes contributing to the count of Bike rentals per day 
	 
- Approach for analysis
1. Perform EDA	
	- This step involves reading and understanding the dataset via Visualization

2. Data Prepartion for Dummy variables and splitting the data to Train and Test
	- In this step, we create dummy variables for Categorical Fileds and split the data as Train and Test set

3. Build Linear Regression Model
	- This part focuses on building the Linear Regression Model using relevant Feature selection methods
   
4. Residual Analysis of the Train Set
	- This part focuses on analyzing the Residual Errors to ensure they fulfill the assumptions of Linear Regression.

5. Predictions and Model Evaluation
	- Model Predictions with Test Set and Evaluation using R Squared.




## Conclusions
- OutCome of EDA 
	- temp , yr, season , weather_sit have a strong association with target cnt
	- holiday , working day have a correlation with target cnt but not very signoficant
	- weekday, mnth are dropped since the same reference can be obtained from other fields like holiday and season
	- multicollinearity exists bewteen fields temp , atemp
	
- OutCome of Dummy variables and splitting the data to Train and Test
    - Dummy variables Createdeted for season , weather_si and data was split as Train and Test
 
- Outcome of Build Linear Regression Model
    - LR model was created using statsmodel
	- atemp' was dropped since it had high VIF and p-value
	- 'hum' was dropped since it had high VIF
	- 'workingday' was dropped since it had high p-value
	
- Outcome of Residual Analysis 
	- Error Terms are normally distributed
	- Error Terms have a constant variance centered towards zero
	- Error Terms are independent of each other
	
- Outcome of Predictions and Model Evaluation
	- R squared was 0.80
	- The top 3 Features are temp , yr and weathersit(Light Rain and Snow)
    - $ cnt = 0.234 \times yr - 0.087 \times holiday + 0.466 \times temp - 0.154 \times windspeed - 0.082 \times season\_spring + 0.037 \times season\_summer + 0.075 \times season\_winter - 0.076 \times weathersit\_Cloudy - 0.279 \times weathersit\_LightRainSnow $
 	


## Technologies Used
- pandas - version 2.2.2
- numpy - version 1.26.4
- matplotlib - version 3.8.4
- seaborn - version 0.13.2
- scikit-learn - version 1.4.2
- statsmodels - version 0.14.2



## Acknowledgements
Give credit here.
- This project was inspired by Machine Learning Course and Lecture Notes as part of IIIT-B PG Program in a ML and AI


## Contact
Created by [@pradeephm31] - feel free to contact me!