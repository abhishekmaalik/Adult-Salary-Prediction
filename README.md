# Adult-Salary-Prediction

A Python-based Machine Learning hands-on project to predict the Salary of an average Adult.

## Features and Limits

    Works best when age of the worker is in the inclusive range of [17, 90].
    Works perfectly for workers of all Education levels, viz. HS-grad/Bachelors etc.
    Works perfectly for workers of all Marital statuses, viz. married/divorced/single etc.
    Takes the Racial data (viz. Asian, Black, White etc) and Relationship data (viz. Husband/ Wife/ Own-child/ Other-relative/ No-relationships etc) to mimic the real-world scenario and predict as accurately as possible.
    Works for a wide range of Ocupations including Sales, Craft-repair, Tech-support, Fishing, Farming, Executive-Managerial, and various other fields of job.

Takes other factors in consideration such Country of Work, Total hours of work per week, etc, and predicts if the salary of the individual is above/below 50K.

    The data used for training the model is mostly dominated by US-residents. But to make the model capable of predicting non-US salaries as well, data from other places viz. Cuba, Taiwan, Mexico, India, etc has been used. But accounting for US-dominant data, it's safe to say that the model will have a higher accuracy for US-residents' test data, while also maintaining a pretty high accuracy for test data from any other countries.

## Installation

Python modules required to train/test the model or run the source file include:

    Pandas (works for all versions), Numpy, Seaborn (if if user is interested in viewing the CSV data in a graphical format), Matplotlib.

## Files present

    adult_data.csv containing the Training data,the data used to test the model's accuracy.
    Adult Salary Prediction.ipynb containing the source code to train the model.
    
## Model choice

    Execute the main.py script which will train a model on the cleaned data and export a it along with the required data info for deployment on Heroku.

     python3 incomePrediction/main.py
 
 I chose the LogisticRegression classifier from scikit-learn to get predictions (The test accuracy obtained is quite well ~ 85%). Cross-validation is done to choose the important hyperparameter (C) to control the degree of regularization. The script can be modified to use and tune any classifier available in scikit-learn. Both the training and test accuracies are comparable and hence, there seems to be no overfitting. I chose to go with Logistic Regression because it is a simple linear classifier whose results are interpretable and this is what I would expect from a model on such a dataset where the predictor-response relationship seems to be important in the analysis. I also tried building and tuning a RandomForest classifier and there was a 1% increase in the accuracies which is not much higher and therefore, a simpler model is a better choice.
