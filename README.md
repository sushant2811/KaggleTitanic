# KaggleTitanic
ML101

Jupyter notebook for predicting survival probability in the Titanic disaster.
Data from Kaggle
Heavily modeled after the Titanic Data Science solutions notebook on Kaggle

The notebook consists of four predictions.  Two each for random forest classifier 
and the support vector classifier.  The two predictions for the each model 
are with and without the Age * Pclass feature.  Following is summary of results

Random forest		 : with Age * Pclass feature:  score = 0.78468
Random forest		 : w/o Age * Pclass feature:   score = 0.76076

Support vector classifier: with Age * Pclass feature:  score = 0.78947
Support vector classifier: w/o Age * Pclass feature:   score = 0.7799


Following are some of the improvements that can be made:

1) Create a FamilyParameter * Pclass feature.  Large families for Pclass = 1 
survived, but large families from Pclass = 3 didn't. 

2) More importantly, we need to have a cross_validation set. Split up the 
training data into cross_validation and training sets.  Use the cross_validation 
set to decide the paramters in our model.  For example, things like the 
strength of regularization parameter C.  Looking at learning curves might also be 
a good idea. 
sklearn's model_selection library would come in handy.  
Especially, the train_test_split function to split the training and test sets. 


