Credit card fraud detection

The aim of the project is to judge whether the transaction is a fraudulent transaction or not. Here, we have used the dataset that has been taken from Kaggle which can be accessed using the link "https://www.google.com/url?q=https%3A%2F%2Fwww.kaggle.com%2Fmlg-ulb%2Fcreditcardfraud%3Fselect%3Dcreditcard.csv".

The dataset comprises credit card transactions made by European cardholders in September 2013. It includes transactions from a span of two days, with 492 fraudulent transactions out of a total of 284,807. This results in a highly imbalanced dataset, where the positive class (frauds) represents only 0.172% of all transactions.

All input variables in the dataset are numerical and have undergone PCA transformation. to maintain the confidentiality, the original features and additional background information are not available. The response variable, 'Class,' is set to 1 in the case of fraud and 0 otherwise.

First, we have done in depth EDA, and have done univariate and bivariate analysis for all the features. As we have a highly imbalanced class variable, we have done under sampling to make the dataset balanced.

We have used correlation heat map to measure the linear relationship between features. Using boxplot, we also have detected the outliers and then removed them.

We have a data that is high dimensional and visualising any patterns in higher than 3 is not possible. So, to see how our data would look like we have used dimensionality reduction techniques for visualisation of our data.

As we have a classification problem on our hands we have applied classification models and calculate the cross validation score to identify the best fit for our data.

Some of the models that we have used are:

-LogisticRegression

-KNeighborsClassifier

-Support Vector Classifier

-DecisionTreeClassifier


We have used sklearn cross_val_score to compare model performances, for this we have checked which model has best mean average accuracy over given number of folds. We tried to look for the best set of paramters for models using gridsearch.

We have used these to evaluate our model:

-Cross_val_score

-ROC AUC Score

-ROC Curve

-Confusion Matrix, Classification report

-Average precison score, Area under precision recall curve

And we found out that SVC and Logistic regression have best cross validation score. Also, we observed that SVC has better ROC AUC Score.
