# Starbuck Capstone Project
This is the project of my Starbucks capstone project as requirement to graduate from Udacity Data Scientist Nanodegree Program

## Introduction
The efficiency and effectivity of customer targeting is important for a business. This also
happens to Starbucks which their method is by giving offers to their customer through their
advertisement on apps.

## Project Domain Background
As a college student, I enjoy the promotional offering since it enables me to still have some
fun time and keep my wallet full. At the end of the rough academic week, I sometime spare
my time to go to mall to clear my mind and use the promotional offering to taste some type
of foods available.
Sometimes, it crossed my mind that some customers get different offer and probably that
customer won’t use that offer either. I wonder just how some company decide and optimize
that offer to their target customer which in this case I took this capstone project.

## Problem Statement
In this capstone project, we want to determine whether certain customer will accept the
offer based on datasets provided by Starbucks.

### Datasets and Inputs
There are three datasets provided from Starbucks in this capstone project:
i.
portfolio.json – containing offer ids and meta data about each offer (duration,
type, etc.) which consist of:
a. id (string) – offer id
b. offer_type (string) – type of offer ie BOGO, discount, informational
c. difficulty (int) – minimum required spend to complete an offer
d. reward (int) – reward given for completing an offere. duration (int) – time for offer to be open, in days
f. channels (list of strings)
ii.
profile.json – demographic data for each customer:
a. age (int)– age of the customer
b. became_member_on (int) – date when customer created an app account
c. gender (str) – gender of the customer (note some entries contain 'O' for
other rather than M or F)
d. id (str) – customer id
e. income (float) – customer's income
iii.
transcript.json – records for transactions, offers received, offers viewed, and
offers completed:
a. event (str) - record description (ie transaction, offer received, offer viewed,
etc.)
b. person (str) - customer id
c. time (int) - time in hours since start of test. The data begins at time t=0
d. value - (dict of strings) - either an offer id or transaction amount depending
on the record

## Solution Statement
This capstone project is basically a propensity modelling problem. Propensity modelling is a
statistical approach and a set of techniques which attempts to estimate the likelihood of
subjects performing certain types of behavior (e.g. the purchase of a product) by accounting
for independent variables (covariates) and confounding variables that affect such behavior
[1]. Since we are going to determine whether some people will accept and complete the
offer, then it is a classification problem, in this case is binary classification.
Some classifier model we could we here are Logistic Regression, SVM (Support Vector
Machines), and Neural Network. However, in this project I will use SVM as benchmark
model. We will also use hyperparameter tuning to get the best model we could get for each
of the classifier models [1][2].

## Benchmark Model
Benchmark model I will use is by taking SVM as the benchmark and then compare it with
other models.

## Set of Evaluation Metrics
Since this is a binary classification model, evaluation metrics we will use is accuracy,
precision, recall, and AUC (area under curve).


## Outline of the Project Design
Outline of the Project Design
My outline of project design is:
i. Create the needed environment for project (on Udacity Workspace).
ii. Do Exploratory Data Analysis:
a. Graph the distribution of each numerical and categorical column.
b. Graph the relationship between each column (with combining the csv file
together first).
iii.
Clean the data which consist of data imputation and row removal (which on is
more effective to the analysis).
iv. Perform feature engineering to dataset.
v. Build three types of model and optimize each of them based on their
hyperparameters to get the best possible prediction for each type.
vi. Evaluate and compare each of the model.
vii. Compile the result into report and blog post.
viii. Upload the project into Github.  

References:
[1] Data Science Foundation. 2015. “Propensity Modelling for Business” [Online].
www.datascience.foundation [Accessed on April 26, 2020]  
[2] Westreich, Daniel, Justin, Michele. 2011. “Propensity score estimation: machine learning
and classification methods as alternatives to logistic regression”.
https://www.ncbi.nlm.nih.gov/pmc/articles/PMC2907172/ [Accessed on April 26, 2020]

## Installation
To use this project, please install these:
1. Anaconda latest version
2. TPOT library: 'pip install tpot' on terminal
