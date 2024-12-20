### Analysis of Coupon Usage

#### Introduction
This project aims to analyze the data  collected via a survey on Amazon Mechanical Turk.  into protrain a classification model that can predict if a user will accept a coupon given his/her answers to some survey questions. There are two parts in this project: 1. Data cleansing and feature engineering 2. Visualize the data using different libraries and derive at the Recommendations for which coupons to use. 

#### Dataset
The data is from the UCI Machine Learning repository and was collected via a survey on Amazon Mechanical Turk. 
Data Used:
In-Vehicle Coupon Recommendation
This data has 12685 items with 25 features and 1 output  

#### Data Cleansing:
##### First step: 
Check for the number of null entries for each of the columns. 

"car" column has lot of empty values. 
Car column has lot of null values (12576 out of 12684 have null values). 
Given the very large percent of entries NULL, just dropping this column entirely. 

Comparatively Bar, Coffee House, CarryAway, RestaurantLessThan20 and Restaurant20To50 have few null columns.
Filled in those few values with the most frequenly occuring value for each of these features. 

##### Second Step: 
Check for the unique values for each of the columns. 
It is interesting to see observe that column 'toCoupon_GEQ5min' has only 1 value. i.e, No variance and hence this feature does not impact the output column or in other words, there is no way to find if this column has any impact on the outcome / output. 

Hence dropping this column as well.

#### Visualizations:


### Conclusions:
