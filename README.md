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

**There are several models that I saved during training. They are uploaded as well in .zip file.**

## Recall score obtained from this project:

|          | Logistic regrssion | Random forest | XGBoost |
|----------|----------|----------|----------|
| No change  |   0.0     |   0.5123674911660777     |   0.43109540636042404     |
| cross validation with grid search  |   0.02120141342756184     |   0.5123674911660777    |   0.4628975265017668     |
| Oversampling  |   0.4452296819787986     |  0.5123674911660777     |   0.44876325088339225     |
| Oversampling with tuning  |   /     |   0.5123674911660777     |   0.5159010600706714     |
| Downsampling  |   /     |  0.5335689045936396    |   0.5300353356890459     |
| Downsampling with tuning  |   /     |   0.5724381625441696     |   recall = 0.5300353356890459     |
| SMOTE  |   /     |   0.49823321554770317     |   0.5795053003533569    |
| SMOTE fine-tune  |   /    |   /     |   0.7597173144876325     |

## Summary
- Analyzed fraud characteristics and designed a hierarchical alert system on a E-commerce company's 138K+ transaction data set to prevent fraudulent activities via **Python**.
- Identified potential fraud country information based on ip address and **reduce the look-up time** by 22%.
- Prepossessed data and utilized **feature engineering** containing customized encoding and feature reduction to extract useful information. 
- Built **logistic regression**, **random forest** and **XGBoost** model, compared various sampling methods to balance data such as oversampling in minor class, downsampling in major class and **SMOTE (Synthetic Minority Over-sampling Technique)**, fine-tuned parameter and **increased recall score** by 20%.
