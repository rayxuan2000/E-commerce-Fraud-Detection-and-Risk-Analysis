# E-commerce-Fraud-Detection-and-Risk-Analysis

## Introduction
Fraud detection is an important topic especially in commerce or financial field. The main characterristic of fraud data is its highly imbalanced property (ratio between normal transactions and fraud cases is extremely high). This kind of dataset containing features of sign ups time, transaction time etc. are highly predictive of fraud. This make it easier to make actionable operation recommendations/proposal for business.

## Data and Code
The data and code has been uploaded to the repo. The basic structure of the first table is as follows: 
-user_id: Id of the user. Unique by user.
- signup_time: the time when the user created her account (GMT time)
- purchase_time: the time when the user bought the item (GMT time)
- purchase_value: the cost of the item purchased (USD)
- device_id : the device id. You can assume that it is unique by device. I.e., 2 transactions with the same device ID means that the same physical device was used to buy
- source : user marketing channel: ads, SEO, Direct (i.e. came to the site by directly typing the site address on the browser).
- browser : the browser used by the user.
- sex : user sex: Male/Female age : user age
- ip_address : user numeric ip address
- class : this is what we are trying to predict: whether the activity was fraudulent (1) or not (0).

The second table is as follows:

- lower_bound_ip_address : the lower bound of the numeric ip address for that country

- upper_bound_ip_address : the upper bound of the numeric ip address for that country

- country : the corresponding country. If a user has an ip address whose value is within the upper and lower bound, then she is based in this country.


## Summary
- Built machine learning models on a E-commerce company's 138K+ transaction data sets to predict fraudulent activities via **Python**.
- Identified potential fraud country information based on ip address and **reduce the look-up time** by 22% using binary search.
- Utilized feature engineering, built **logistic regression** and **random forest** model with and without **SMOTE (Synthetic
Minority Oversampling Technique)** method on minority set, performed parameter tuning, **increased recall score** by
20% , and analyzed fraud characteristics by presenting feature importance.
- Designed a real-time alert system to prevent fraudulent activities.
