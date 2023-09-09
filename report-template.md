# Report: Predict Bike Sharing Demand with AutoGluon Solution
#### Priyanshu Kumar Singh

## Initial Training
### What did you realize when you tried to submit your predictions? What changes were needed to the output of the predictor to submit your results?
The output score was not good. I had to add extra feature to the dataframe, to improve the accuracy.

### What was the top ranked model that performed?
The top ranked model was the WeightedEnsemble_L3 model. 

## Exploratory data analysis and feature creation
### What did the exploratory analysis find and how did you add additional features?
The exploratory data analysis found there were 2 additional columns in the train data and were not present in the test data. The datetime column included all the dates and time in the same column. So the date and time were split into different columns

### How much better did your model preform after adding additional features and why do you think that is?
The accuracy improved quite good. Initially it was 1.784 after adding additional feature it was 0.50. Adding relevant new features give the model additional important data to understand the patterns and perform better.

## Hyper parameter tuning
### How much better did your model preform after trying different hyper parameters?
The model did not perform good compared to previous one after adding new features.

### If you were given more time with this dataset, where do you think you would spend more time?
I would spend in EDA and adding more features. And also in hyperparameter tuning.

### Create a table with the models you ran, the hyperparameters modified, and the kaggle score.
|model|GBM|RF|XGB|score|
|--|--|--|--|--|
|initial|-54.982779|-53.505912|-54.94277|1.78411|
|add_features|-30.410461|-32.441176|-31.450945|0.99719|
|hpo|-40.3616|-62.850821|-43.972327|0.59231|

### Create a line plot showing the top model score for the three (or more) training runs during the project.



![model_train_score.png](img/model_train_score.png)

### Create a line plot showing the top kaggle score for the three (or more) prediction submissions during the project.



![model_test_score.png](img/model_test_score.png)

## Summary
Initially I setup the environment in my local machine to get easier access to the project anytime. Calling of Kaggle API to particiapte in the contest. Then EDA was performed to pre process the data. Initialy the raw data was feeded to the model. Thereafter new features were added with aim to improve the score. After adding a feature the model accuracy significantly improved and but the score declined after hyperparameter tuning. I got to learn new method 'AutoGluon' to implement machine learning task.