# Report: Predict Bike Sharing Demand with AutoGluon Solution
Sadiya Jamal

## Initial Training
### What did you realize when you tried to submit your predictions? What changes were needed to the output of the predictor to submit your results?
After I trained the model and tested it to create predictions on the test dataset, i had to check for negative values before submitting it to kaggle.

### What was the top ranked model that performed?
The best model for my case was the second model, where i added hour, day, month and year features. The score for the model was 0.49687.

## Exploratory data analysis and feature creation
### What did the exploratory analysis find and how did you add additional features?
I plotted histograms for all features for doing EDA. This gace a quick and clear picture of how the data eas distributed with respect to the different features like seasons, weather, holidays, working days etc. I also decided to then split the datetime feature into hour, day, month and year, which eventually gave a better represntation of the data and also led to a better model score.

### How much better did your model preform after adding additional features and why do you think that is?
After adding additional features mentioned in the previous response, my model performed better, hence showing that tweaking the right features eventaully improves the model performance.

## Hyper parameter tuning
### How much better did your model preform after trying different hyper parameters?
When i tuned the hyperparameters, my model was better as compared to the initial model, as the score was 1.80855 for the first model and 1.42531 after tuning the hyperparameters. 

### If you were given more time with this dataset, where do you think you would spend more time?
I would try doing some more feture engineering as i could see that this was defintitely improving the model.

### Create a table with the models you ran, the hyperparameters modified, and the kaggle score.

model|	time|	epochs|	boost_rounds|	score
0|	initial|	600|	default|	default|	1.80855
1|	add_features|	600	default|	default|	0.49687
2| hpo|	600|	5	|80|	1.42531

### Create a line plot showing the top model score for the three (or more) training runs during the project.
![model_train_score](https://github.com/udacity/nd009t-c1-intro-to-ml-project-starter/assets/144320807/510d1f52-b37d-4650-8fd1-155bbfd7ecd2)



### Create a line plot showing the top kaggle score for the three (or more) prediction submissions during the project.
![model_test_score](https://github.com/udacity/nd009t-c1-intro-to-ml-project-starter/assets/144320807/42415620-8260-4901-9a7f-f11cfbe75a79)



## Summary

The initial model had the poorest performance with the score of 1.80855. It improved significantly after adding features in the second model and score was 0.49687. The hyperparameters tuning gave better results as compared to the first model with a score of 1.42531 , however, it was not better than the second model.
