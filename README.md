# Credit-Card-Lead-Prediction

Credit Card Lead Prediction

OVERVIEW :- the Happy Customer Bank wants to cross sell its credit cards to its existing customers. The bank has identified a set of customers that are eligible for taking these credit cards.

TASK :- the bank is looking for help in identifying customers that could show higher intent towards a recommended credit card.

DATA GIVEN :- 

ID (Unique Identifier for a row)

Gender (Gender of the Customer)

Age  (Age of the Customer (in Years))

Region_Code  (Code of the Region for the customers)

Occupation  (Occupation Type for the customer)

Channel_Code  (Acquisition Channel Code for the Customer (Encoded))

Vintage  (Vintage for the Customer (In Months))

Credit_Product  (If the Customer has any active credit product (Home 		   loan, Personal loan, Credit Card etc.))

AvgAccountBalance  (Average Account Balance for the Customer in last 		     12 Months)

Is_Active  (If the Customer is Active in last 3 Months)

Is_Lead(Target)

If the Customer is interested for the Credit Card

0 : Customer is not interested

1 : Customer is interested


BUILDING THE MODEL :

STEP 1 -  Importing modules and loading the data
		modules imported - pandas, numpy, matplotlib, 		seaboran, sklearn.

STEP 2 -  Exploratory Data Analysis

	  Following insights were drawn after EDA 
	  1. Only 23.70% of the given data is a Lead. Hence Ml model will have data to learn from.
	  2. the above graph shows that male customers ahve responded better compared to female candidates.
	  3. Entrepreneurs are the most likely customers for credit card, as they have reponded multiple times for credit card services.
	  4. Channel X2 have the best lead generation ratio compared to others.
	  5. It is very intresting to observe that the missing values do actually have more leads. Thus we should fill the missing values.

STEPS 3 - Pre-Processing

	  1. Around 12% of credit product data is missing.Filling the NULL data with " Not Sure".
	  2. Encoding the string data with numerical codes to convertt them into int data type because ML model can only process int data type.
    
STEP 4 - Spliting the data.

	 1. We split the data into train and test data in ratio of 3:1 so that Ml model can learn from maximum data possible.

STEP 5 -  Applying Feature Scaling on the train and test set.

 	  Feature Scaling is a technique to standardize the independent features present in the data in a fixed range.If feature scaling is not done, then a machine learning 	  	     algorithm tends to weigh greater values, higher and consider smaller values as the lower values,regardless of the unit of the values.

STEP 6 -  Model training

	  Since the dependent varaiable is categorical in nature, we will be using Classification ML Models to predict the values.
	  We have used various classification model, like Logistic Regression, SVM, K-NN, Kernel SVM, Naive bayes, DecisionTree Classification and Random Forest Classification.
	  After execution of various ML models we foungd that Random Forest Classification gives the best accuracy.

STEP 7 - Confusion Matrix

	 A Confusion matrix is an N x N matrix used for evaluating the performance of a classification model, where N is the number of target classes. The matrix compares the          actual target values with those predicted by the machine learning model.The rows represent the predicted values of the target variable.

STEP 8 - loading the test data and repeating the above mention steps.
