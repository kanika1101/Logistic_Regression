# Logistic_Regression
Studies with Logistic Regression in Python
The repository consists of the following projects:

## 1. Telecom Churn Prediction using Logistic Regression </b>
Based on all this past information of telecom users, you want to build a model which will predict whether a particular customer will churn or not, i.e. whether they will switch to a different service provider or not. So the variable of interest, i.e. the target variable here is ‘Churn’ which will tell us whether or not a particular customer has churned. It is a binary variable - 1 means that the customer has churned and 0 means the customer has not churned.

<b>Solution Overview:</b>

<b>Understanding and exploring the data</b>
<b>Preparing the Data: </b>

This involves splitting data into train and test, creating dummy variables and scaling the data
<b>Model building</b>

A logistic model is built using python statsmodel GLM (Generalized Linear Model). RFE is used here for feature elimination.

## 2. Scoring Leads of an online Education company

An education company named X Education sells online courses to industry professionals. On any given day, many professionals who are interested in the courses land on their website and browse for courses.
When these people fill up a form providing their email address or phone number, they are classified to be a lead. Moreover, the company also gets leads through past referrals. Once these leads are acquired, employees from the sales team start making calls, writing emails, etc. Through this process, some of the leads get converted while most do not.
The company requires you to build a model wherein you need to assign a lead score to each of the leads such that the customers with higher lead score have a higher conversion chance and the customers with lower lead score have a lower conversion chance.

<b>Solution Overview:</b>

A logistic Regression model has been built to classify whether a student whether a lead is going to be converted.The below solution methodology has been adopted to arrive at the best model that can assign a Lead Score between 0 to 100 based on various features.

<b> Data Analysis:</b>
A thorough EDA has been conducted to identify key drivers that can help achieve a conversion rate of atleast 80%.

Handling Categorical variables:

1.Variables with high skewness have been removed.

2.Handling Missing values and deriving new categories

4.All the categorical columns have been visually analysed using boxplots,bar charts as needed.

Handling Numerical variables:

1.Of the 5 numerical variables,the two variables - Asymmetrique Activity Score, Asymmetrique Profile Score have > 45% missing values and hence dropped from analysis.

2.For the remaining 3 columns,the missing values in the 2 columns-Total Visits,PageViews Per Visit,missing values have been imputed using the median(mean was also close to median) of the columns.

3.The outliers in these columns have been visualized using boxplots and have been treated by soft  capping the 99% value.

<b>Preprocessing and Data Preparation</b>

Dummy variable creation for categorical variables:

Binary variables with values Yes/No have been converted to 1/0.
Dummy variables for different categories have been created and the dummy columns of category “Others” have been dropped. 

Train test split
	Train size of 70% data and test size of 30% data was used.

Scaling data
	Standard scaling was used to scale all the numerical variables.

<b>Model Building</b>

For features identification, a combination of manual and automated(RFE) approach have been adopted.
A logistic regression model was built and was finalized with 13 variables with VIF < 5 and p-value < 0.1.
Optimal cutoff of 0.35 was decided based on accuracy,sensitivity and specificity trade off.
The model predicted the probabilities which were further used to calculate the Lead Score.

<b>Final Analysis</b>

The project contains the supporting files whhich discusses about the analysis and recommendation for the company
