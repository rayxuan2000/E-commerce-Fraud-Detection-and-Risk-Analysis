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

## Some numeric values obtained from this project:
#### Logistic regression
(1) No change

precision = 0.0

recall = 0.0

f1_score = 0.0

(2) Cross validation with grid search

precision = 0.8571428571428571

recall = 0.02120141342756184

f1_score = 0.041379310344827586

(3) Oversampling

precision = 0.3230769230769231

recall = 0.4452296819787986

f1_score = 0.37444279346210996

#### Random forest
(1) No change

precision = 1.0

recall = 0.5123674911660777

f1_score = 0.6775700934579438

(2) Cross validation with grid search

precision = 1.0

recall = 0.5123674911660777

f1_score = 0.6775700934579438

(3) Oversampling (without or with tuning)

precision = 1.0

recall = 0.5123674911660777

f1_score = 0.6775700934579438

(4) Downsampling

precision = 0.6651982378854625

recall = 0.5335689045936396

f1_score = 0.592156862745098

(5) Downsampling with tuning

precision = 0.1610337972166998

recall = 0.5724381625441696

f1_score = 0.25135764158262214

(6) SMOTE

precision = 0.9527027027027027

recall = 0.49823321554770317

f1_score = 0.654292343387471

#### XGBoost
(1) No change

precision = 0.991869918699187

recall = 0.43109540636042404

f1_score = 0.6009852216748769

(2) Cross validation with grid search

precision = 0.9703703703703703

recall = 0.4628975265017668

f1_score = 0.6267942583732058

(3) Oversampling

precision = 0.8355263157894737

recall = 0.44876325088339225

f1_score = 0.5839080459770115

(4) Oversampling with tuning

precision = 0.8848484848484849

recall = 0.5159010600706714

f1_score = 0.6517857142857143

(5) Downsampling 

precision = 0.35294117647058826

recall = 0.5300353356890459

f1_score = 0.423728813559322

(6) Downsampling with tuning

precision = 0.35294117647058826

recall = 0.5300353356890459

f1_score = 0.423728813559322

(7) SMOTE

precision = 0.018655443066772835

recall = 0.5795053003533569

f1_score = 0.03614723385497024

(8) Fine tune on SMOTE

recall = 0.7597173144876325

|          | Logistic regrssion | Random forest | XGBoost |
|----------|----------|----------|----------|
| No change  |   A1     |   B1     |   C1     |
| cross validation with grid search  |   A2     |   B2     |   C2     |
| Oversampling  |   A3     |   B3     |   C3     |
| Oversampling with tuning  |   A3     |   B3     |   C3     |
| Downsampling  |   A3     |   B3     |   C3     |
| Downsampling with tuning  |   A3     |   B3     |   C3     |
| SMOTE  |   A3     |   B3     |   C3     |
| SMOTE fine-tune  |   /    |   /     |   0.7597173144876325     |

## Summary
- Analyzed fraud characteristics and designed a hierarchical alert system on a E-commerce company's 138K+ transaction data set to prevent fraudulent activities via **Python**.
- Identified potential fraud country information based on ip address and **reduce the look-up time** by 22%.
- Prepossessed data and utilized **feature engineering** containing customized encoding and feature reduction to extract useful information. 
- Built **logistic regression**, **random forest** and **XGBoost** model, compared various sampling methods to balance data such as oversampling in minor class, downsampling in major class and **SMOTE (Synthetic Minority Over-sampling Technique)**, fine-tuned parameter and **increased recall score** by 20%.
