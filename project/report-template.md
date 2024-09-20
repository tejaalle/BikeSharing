# Report: Predict Bike Sharing Demand with AutoGluon Solution
Tejeswar Reddy Alle

## Initial Training
### What did you realize when you tried to submit your predictions? What changes were needed to the output of the predictor to submit your results?
I reliazed the negative values are not accepted for submission while some of the predictors delivered negative values which were changed to zero before submission

### What was the top ranked model that performed?
The top ranked model is the model when we added extra features(second model) which has a rmse value of the top model is 33.944976

## Exploratory data analysis and feature creation
### What did the exploratory analysis find and how did you add additional features?
Exploratory data analysis helped me to category some columns and parse the datetime column as datetime and then make me realizes the further breaking down of datatime to day, month, year which will help me improve the model further

### How much better did your model preform after adding additional features and why do you think that is?
The model has improved by 70 percent after adding the additional features. It is because the model now can learn more on the day, uear and month seperately which will help model to learn more

## Hyper parameter tuning
### How much better did your model preform after trying different hyper parameters?
Suprisingly model performance has went down after hyper tuning the parameters. It may be because of the paramerts I used. I need experiment more

### If you were given more time with this dataset, where do you think you would spend more time?
I will spend more time working the tuning hyperparameters and also seeing If any other fatures I can add

### Create a table with the models you ran, the hyperparameters modified, and the kaggle score.
	model	hpo1	hpo2	hpo3	score
0	initial	prescribed_values	prescribed_values	presets: 'high quality' (auto_stack=True)	1.80160
1	add_features	prescribed_values	prescribed_values	presets: 'high quality' (auto_stack=True)	0.46195
2	hpo	Tree-Based Models: (XT, XGB )	{‘num_trials’: 20, ‘scheduler’ : ‘local’, ‘searcher’: ‘auto’}	presets: 'interpretable={‘auto_stack’: False, ‘hyperparameters’: ‘interpretable’}'	0.55036

### Create a line plot showing the top model score for the three (or more) training runs during the project.


model_rmse_score.png

### Create a line plot showing the top kaggle score for the three (or more) prediction submissions during the project.

model_test_score.png

## Summary
In summary I learnt to use the AutoGlon How it makes use of differnt models and select the best model and inportance od exploratory data analysis and hyper parameter tuning
