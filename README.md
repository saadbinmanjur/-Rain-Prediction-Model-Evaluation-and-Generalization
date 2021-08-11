# Rain Prediction, Model Evaluation & Generalization
Predict next-day rain by training classification models on the target variable RainTomorrow. This dataset contains about 10 years of daily weather observations from many locations across Australia. RainTomorrow is the target variable to predict. It means -- did it rain the next day, Yes or No? This column is Yes if the rain for that day was 1mm or more.

Objectives:

- Developing an ML model that suits best for the datasets predicting the rain on the next day.

First, we select the feature, then we do some feature engineering on our selected feature. After that we handled missing values in numerical variables, categorical variables, outliers in numerical variables. And then we encode categorical variables before doing feature scaling.

At the model training we get
Training set score: 0.8487
Test set score: 0.8488
These two values are same in score. So, there is no question of overfitting.

In Logistic Regression, we use default value of C = 1. It provides good performance with approximately 85% accuracy on both the training and the test set. But the model performance on both the training and test set are very comparable. It is likely the case of underfitting.

I increased C and fit a more flexible model.
Then we get 
Training set score: 0.8487
Test set score: 0.8485
We can see that, C=100 results in higher test set accuracy and also a slightly increased training set accuracy.

After that we used more regularized model than the default value of C=1, by setting C=0.01.
And we get
Training set score: 0.8427
Test set score: 0.8415
So, if we use more regularized model by setting C=0.01, then both the training and test set accuracy decrease relative to the default parameters.

Lastly, we compared model accuracy with null accuracy and we get Null accuracy score: 0.7812

We can see that our model accuracy score is 0.8485 but null accuracy score is 0.7812. So, we can conclude that our Logistic Regression model is doing a very good job in predicting the class labels.


- How would you evaluate your model and why do you consider the model as a good fit?

At the model evaluation we get




- What are the steps you will prefer to do for improving your model for further analysis?
