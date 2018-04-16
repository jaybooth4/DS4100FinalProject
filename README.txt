Final Project DS 4100

Analysis of Somerville Happiness data

This project is an analysis of a set of surveys conducted by the Town of Somerville every 2 years.
https://data.somervillema.gov/Happiness/Somerville-Happiness-Survey-responses-2011-2013-20/w898-3dfm

Data cleaning/pre-processing (ETL File):
In this file, the survey data is loaded from an API, cleaned, and written to csv files. Derived features are created, missing values are imputed, 
and string parsing is used to put the data in an analyzable format for the next stages.

There are two major types of analysis that I want to focus on in this project.

Regression Analysis:
Analyze responses to the how_satisfied_are_you_with_your_life_in_general survey question a multiple linear regression model to see what sorts of factors
 in the data are statistically significant in determining these scores. Fitting of regression parameters will be used to reduce features in the model to 
 only those which are statistically significant. The model will be assessed in terms of MSE, R-squared, and F-score. This regression will be run on the 
 dataFrames from 2013 and 2015 to see if there are any trends that can be seen over time. Lastly, to add another comparison a dataset from Kaggle which 
 contains the most important factors of happiness within countries from around the world will be read in and compared to the results.

Classification Analysis:
Next several classification models will be used to predict marital statu to see if there is a classifiable relationship between survey responses and 
this category. These models will be run only on the 2011 dataset because it has the most data of the three datafrmaes. Each model will be tuned and 
then compared against each other in terms of accuracy on a test datasetto see which one is the best fit.

Project structure
ETL file
--> Regression
--> Classification

Notes:
All paths must be changed if you would like to run this locally. The data from the API call is also included in a separate file if for some reason the API goes down.
I never ran into issue with rate limiting or outages during the project.