# Predicting-sleep-efficiency

## Aim 
In this project I aim to predict sleep efficiency from lifestyle factors and sleep metrics using supervised machine learning methods such as linear, random forest, and boosted regression. I will compare how models trained lifestyle factors or sleep metrics perform and which type of regression is best at predicting the outcome. I expect that sleep metrics will lead to better predictions than lifestyle factors, as these are more directly related to sleep efficiency. However, I am curious to see whether lifestyle factors will perform well also.  

## Data
The data was obtained from kaggle. It contains the following variables:
* ID - unique identifier
* Age - age in years
* Gender - gender that the person identifies with
* Bedtime - time that the person goes to bed
* Wakeup time - time that the person wakes up
* Sleep duration - duration of time spent sleeping
* Sleep efficiency - this is our outcome variable, which is defined as the proportion of time spent in bed that is actually spent sleeping
* REM sleep percentage - percentage of sleep time spent in REM sleep
* Deep sleep percentage - percentage of sleep time spent in deep sleep
* Light sleep percentage - percentage of sleep time spent in light sleep
* Awakenings - the number of time the person awakes from sleep during the night
* Caffeine consumption - this contains information about caffeine consumption in the 24 hours prior to sleep time
* Alcohol consumption - this contains information about alcohol consumption in the 24 hours prior to sleep time
* Smoking status - whether or not the person smokes
* Exercise frequency - amount of times the person exercises [per week]

## Preprocessing 
To preprocess the data I convert the variables 'Bedtime' and 'Wakeup time' to integers and normalize them around midnight, so that e.g. -2 is 2 hours before midnight (10pm) and the value 3 corresponds to a 3am. Furthermore, I convert binary variables (Smoking_status and Gender) to numerical values. Moreover, I impute missing values using the K Nearest Neighbours (KNN) method to estimate the most likely values. 

## Analysis 
### Part 1: Predicting Sleep Efficiency from Lifestyle Factors
For part one, I create a new dataset without the sleep metrics (Sleep duration, Sleep efficiency, REM sleep percentage, Deep sleep percentage, Light sleep percentage, & Awakenings). Next I split the data into training (20%) and test data (80%). Next, I normalize the data before training the models and plotting the predicted values against the actual values. The models I train are linear regression, random forest regression, and a boosted regression model. 

### Part 2: Predicting Sleep Efficiency from Sleep Metrics
In part 2, I create a dataset including only the sleep metrics (mentioned above). Again, I train linear, random forest, and boosted regression models and compare the predicted and actual values. 

## Conclusion 
Linear regression does not perform well as a predictor in either case. Random forest and boosted regression are quite good at predicting sleep efficiency from sleep metrics (R squared is roughly 0.82 in both cases), but less effective if they are only accounting for lifestyle factors, with an R squared value of 0.31 and 0.28 respectively. It was expected that sleep metrics would lead to good prediction of sleep efficiency, however, I expected the predictions from lifestyle factors to be better than they turned out to be. 
