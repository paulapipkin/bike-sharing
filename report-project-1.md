# Report: Predict Bike Sharing Demand with AutoGluon Solution
#### Paula Pipkin

## Initial Training
### What did you realize when you tried to submit your predictions? What changes were needed to the output of the predictor to submit your results?
TODO: I only had to replace negatives values for 0's on my thrid model, other than that the other submissions were fine

### What was the top ranked model that performed?
TODO: For the first try the best model was WeightedEnsemble_L3, a model that combines the predictions from multiple models. Same for the subsequent tries

## Exploratory data analysis and feature creation
### What did the exploratory analysis find and how did you add additional features?
TODO: The features had different types of distribuition,but they all seemed to make sense. I created a hour and date column from the datetime feature using dt.time 

### How much better did your model preform after adding additional features and why do you think that is?
TODO: the second try scored 60% better, I believe that not only adding the feature but also setting the dtype to category for some features gave the more information about the features and helped improved how they were used in the prediction

## Hyper parameter tuning
### How much better did your model preform after trying different hyper parameters?
TODO: It drecreased almost 20%, my kaggle performance also went down quite a bit.

### If you were given more time with this dataset, where do you think you would spend more time?
TODO: I would try and play with different hyper parameters.

### Create a table with the models you ran, the hyperparameters modified, and the kaggle score.
|model|Best Quality|More Features|Hyper Parameter|score|
|--|--|--|--|--|
|initial|True|False|False|1.79514|
|add_features|True|True|False|1.76108|
|hpo|True|True|True|0.47090|

### Create a line plot showing the top model score for the three (or more) training runs during the project.

TODO: Replace the image below with your own.

![model_train_score.png](model_train_score.png)

### Create a line plot showing the top kaggle score for the three (or more) prediction submissions during the project.

TODO: Replace the image below with your own.

![model_test_score.png](model_test_score.png)

## Summary
TODO: During this project I experienced using AutoGluon. I had to review the individual parameters for the main models so I could use them do indiviadully tune my last run, and that result and much better predictions.Even though, tunning can take a good ammount of time, Auto Gluon definitely makes the work easier, because once the parameters are set, AutoGluon will run and evaluate each model 'at once'.

Independently of the tunning, for all 3 runs a WeightedEnsemble, a model that combines the predictions from multiple models, was ranked the best.

I also learned the importance of correctly set the correct type for each feature to help the model understand the weight of each feature.


