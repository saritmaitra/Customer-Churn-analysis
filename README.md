# Customer-Churn-analysis using machine learning algorithm

This project performed an extensive descriptive analytics to explore different factors responsible for customers churn in a telecom company.

# Logistics Regression

Post decriptive, predictive and diagnostics analytics are performed using machine learning algorithm. Logistics regression and AUCROC score yields >70%, which is signifinat for modelling. The prediction_test and afterwards the accuracy score is measured and printed from this model.

# Survival Analysis

Logistic Regression is assigning a probability to each observation that describes how likely it is to belong to the positive class.
In any large enough group of customers like Telecom there are going to be people who have the same attributes / features. Some of those will churn and some of them won’t, and what Telecom company ideally like to know is the probability of churn for each group. This is what Logistic Regression provides. But it is not clear what time scale it is predicting for. Therefore, survival analysis was conducted for this purpose.

# Kaplan–Meier and Cox Proportional Hazards Model

Kaplan is fully parametric and the Cox PH Model is semi-parametric. Kaplan–Meier theory needs specification of the distribution of 
the underlying hazard. CoxPH analyses the covariates (features) of a dataset with regards to how long a customer survives. 
It describes how each feature proportionally increases risk over the baseline survival rate for a cohort. 
The expectation is that, churn is relatively low. Kaplan–Meier plot suggests that, the company retained almost 80-90% of their customers. 
But there is steady decline and after over 70 months, the company is able to retain almost 60% of their customers. 
This input is quite useful for the telecom company to understand the trend and business forecast.

To examine the effects of different variables, the Cox Proportional Hazards Model is used.

# CoxPH Model

Cox model is fits the coefficients of the Hazard function using partial likelihood method. The advantage of Cox Proportional Hazards regression is that the survival models can be fitted without the distribution assumption.
The time to event for a customer in the data-set is very important for the survival curves at the aggregate level; however, in real life situations along with the event data the covariates (features) of that individual will be present. Therefore, it is very important to know about the impact of covariates on the survival curve. This would help in predicting the survival probability of a customer, if the associated covariates values are known. The data has each customer's tenure when they churned (the event time T) and the customer's Gender, MonthlyCharges, Dependents, Partner, PhoneService etc. The other variables are the covariates here. It would be interesting to know how these covariates impacts the survival probability function. In such cases, it is the conditional survival function S(t|x) = P(T > t|x). x denotes the covariates. Company interested in S(tenure > t|(Gender, MonthlyCharges, Dependants, Partner, PhoneService etc)).

A well calibrated model and important business inputs are presented here to help telecom company to take necessary business strategy to retain customers.
