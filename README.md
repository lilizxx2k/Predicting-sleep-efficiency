# Predicting-sleep-efficiency

## Aim 
In this project I aim to predict sleep efficiency using supervised machine learning methods such as linear, random forest, and boosted regression. 

## Data
The data was obtained from kaggle. It contains the following variables:
* ID
* Age
* Gender
* Bedtime
* Wakeup time
* Sleep duration
* Sleep efficiency
* REM sleep percentage
* Deep sleep percentage
* Light sleep percentage
* Awakenings
* Caffeine consumption
* Alcohol consumption
* Smoking status
* Exercise frequency
* Smoking_status

## Preprocessing 
To preprocess the data I convert the variables 'Bedtime' and 'Wakeup time' to integers and normalize them around midnight, so that e.g. -2 is 2 hours before midnight (10pm) and the value 3 corresponds to a 3am. Moreover, I impute missing values using K Nearest Neighbours (KNN). 

## Analysis 
### Part 1: Predicting Sleep Efficiency from Lifestyle Factors
### Part 2: Predicting Sleep Efficiency from Sleep Metrics

## Conclusion 
