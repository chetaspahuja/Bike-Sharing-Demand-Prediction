# Report: Predict Bike Sharing Demand with AutoGluon Solution
#### NAME HERE: CHETAS PAHUJA


## Initial Training
### What did you realize when you tried to submit your predictions? What changes were needed to the output of the predictor to submit your results?
TODO: Add your explanation
At first the predictions were submitted without any feature engineering and exploratory data analysis. On submitting a kaggle score of 1.81967 was obtained which was very low. This was expected as the model was trained directly without any data preprocessing.

### What was the top ranked model that performed?
TODO: Add your explanation
The best model that performed was 'WeightedEnsemble_L3' which had a score of -52.465688.

## Exploratory data analysis and feature creation
### What did the exploratory analysis find and how did you add additional features?
TODO: Add your explanation
To perform data analysis, histograms and correlation matrix were created. This was done to analyse the relations between different columns among themseleves and target column. From correlation matrix it could be inferred that the target column 'count' is more strongly related to 'season', 'temp' and 'atemp'. As 'registered' and 'casual' columns were not present in test set they were not considered. Further 'datetime' was divided into 'year', 'month', 'day' and 'hours'. The 'season' and 'weather' features were also converted to categorical columns.

### How much better did your model preform after adding additional features and why do you think that is?
TODO: Add your explanation
Addition of these features improved the model score to a great extent. After adding features a kaggle score of 0.59395 was obtained.

## Hyper parameter tuning
### How much better did your model preform after trying different hyper parameters?
TODO: Add your explanation
Hyperparameter tuning improved the model score to some extent. After hyperparameter tuning a kaggle score of 0.48766 was obtained which is slightly better than what we obtained after adding new features. 

### If you were given more time with this dataset, where do you think you would spend more time?
TODO: Add your explanation
I would spend my time in performing hyperparameter tuning and feature engineering. I think working in these two areas could improve the score.

### Create a table with the models you ran, the hyperparameters modified, and the kaggle score.
|model|hpo1|hpo2|hpo3|score|
|--|--|--|--|--|
|initial|default_vals|default_vals|default_vals|1.81967|
|add_features|default_vals|default_vals|default_vals|0.59395|
|hpo|GBM: num_leaves: lower = 20, upper = 56|NN: dropout_prob: 0.0, 0.6|GBM: num_boost_round: 120|0.48766|


![image-2.png](attachment:image-2.png)

### Create a line plot showing the top model score for the three (or more) training runs during the project.

TODO: Replace the image below with your own.
![image.png](attachment:image.png)

### Create a line plot showing the top kaggle score for the three (or more) prediction submissions during the project.

TODO: Replace the image below with your own.

![image.png](attachment:image.png)


## Summary
TODO: Add your explanation

By performing EDA, various conclusion were drawn which helped in feature engineering. This further led to increase in kaggle score. 

In this project, various concepts were applied that were taught throughout the course. I was able to train models and obtain a good score on kaggle using Autogluon
