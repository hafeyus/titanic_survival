# titanic_survival
The goal is to predict whether a passenger would survive during the tragic crash of Titanic.
The predictions on test test was submitted to Kaggle for evaluation and my final score was ranked in top 5%.
I solved the problem using two method:
1. XGBClassifier
2. Stacking

(1) XGBClassifier
I did the feature analysis and feature engineering to clean up the data and add additional features.
Then I fit a XGBClassifier to the data and fine tuned the hyperparameters to get optimal performance.
However, the perforamce could stilled be imporved, so I moved on the second method.

(2) Stacking
I did the feature analysis and feature engieering a little differently to introduce even more features.
Then I fit RandomForestClassifier, AdaBoostClassifier, SVC, and GradientBoostingClassifier to the data
and fine tuned the model to get optimal performance for each model.
The next step is to combine the predicted results of training set for each classifier and feed them as
the input to XGBClassifier. After fine tuning the hyperparameters using grid search cross validation, 
the performance evaluated on cross-validation set imporved a lot, the final model is ready to go.
