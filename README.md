# Berkeley Haas - Professional Certificate in Machine Learning and Artificial Intelligence - Module 5 - Practical Application 1

## Table of Contents
- [Background](#background)
- [Data Cleansing](#data-cleansing)
- [Explorary Findings](#exploratory-findings)
- [Bar Coupon Analysis](#bar-coupon-analysis)
- [Independent Investigation](#independent-investigation)
- [Next Steps](#next-steps)

## Background
This is a practical application assignment that focuses on using data analysis skills.
This project aims to analyze the data collected via a survey on Amazon Mechanical Turk. 

### There are two parts in this project: 
 1. Data cleansing and feature engineering 
 2. Visualize the data using different libraries and derive at the recommendations for which coupons to use.

## Link to Notebook:
[Explore Coupon Acceptance Factors by Customers](https://github.com/nbajam/BH-PCAIML-MOD5-PAA1/blob/main/prompt.ipynb)

## Data Used:
[In-Vehicle Coupon Recommendation](https://archive.ics.uci.edu/dataset/603/in+vehicle+coupon+recommendation)

## Data Cleansing

1. Step one

    Check for the number of null entries for each of the columns.

    "car" column has lot of empty values. Car column has lot of null values (12576 out of 12684 have null values). Given the very large percent of entries NULL, just dropping this column entirely.

    Comparatively Bar, Coffee House, CarryAway, RestaurantLessThan20 and Restaurant20To50 have few null columns. Filled in those few values with the most frequenly occuring value for each of these features.

2. Step two
    
    Check for the unique values for each of the columns. It is interesting to see observe that column 'toCoupon_GEQ5min' has only 1 value. i.e, No variance and hence this feature does not impact the output column or in other words, there is no way to find if this column has any impact on the outcome / output.

    Hence dropping 'toCoupon_GEQ5min' column as well.

## Exploratory Findings 
1. Only 56.8% of the customers used the coupons
2. More coupons get used during the warmer days than the colder days

## Bar Coupon Analysis
1. Only 41% of bar coupons were used by customers
2. Customers who went to bars more than 3 or 4 times in month used the coupons 76.9% of the time, where was customers who went lesser number of times used the coupons only 37.1% of the time.
3. Customers who went to bars more than once a month and are over age 25 used the coupons ~68% of the time, where was those went less than once and are below 25 years old used coupons 42% of the time.
4. Coupons for Bars have a higher usage rate irrespective of age
5. Coupons for Bars have a higher usage rate irrespective of being a widow.
6. Coupons for Bars hava a Higher usage rate compared to Coupons for Cheap Restaurants used by customers with less than 50K salary

## Independent Investigation
### Usage Rate of Coupon Types and 
1. Coupon Types and their Usage
    -  Bar plot below shows that "Carry Out & Take Away" coupons have the highest usage rate of 73.5%, followed by "Restaurant <20" coupons at 70.7%, 'Coffee House' coupons at 49.9%, 'Restaurant (20-50)'at 44.1% and 'Bar' coupon at 41%
    - ![Usage by Coupon Groups](https://github.com/nbajam/BH-PCAIML-MOD5-PAA1/blob/main/images/allcoupons.png)
2. 1-Day vs 2-Hour Coupons Usage
    - 1-Day Coupons are used more than 2-Hour Coupons
    - ![1-Day Coupon Usage](https://github.com/nbajam/BH-PCAIML-MOD5-PAA1/blob/main/images/daycoupons.png)
    - ![2-Hour Coupon Usage](https://github.com/nbajam/BH-PCAIML-MOD5-PAA1/blob/main/images/hourcoupons.png)
### Analysis of 'Restaurant (<20)' Coupons
1. Coupon Usage by Gender 
    - Coupon usage by Males (48.5%) is higher than Females (34.1%)
    - ![Coupon Usage by Gender](https://github.com/nbajam/BH-PCAIML-MOD5-PAA1/blob/main/images/rest20_bygender.png)
2. Coupon Usage by Age
    - Customers in the age groups 21 and 26 have higher coupon usage rate when compared to the other groups.
    - ![Coupon Usage by Age](https://github.com/nbajam/BH-PCAIML-MOD5-PAA1/blob/main/images/rest20_byage.png)
3. Coupon Usage by Income
    - Surprisingly Highest Earners have the highest coupon utilization rate.
    - ![Coupon Usage by Income](https://github.com/nbajam/BH-PCAIML-MOD5-PAA1/blob/main/images/rest20_byincome.png)
  
  ## Next Steps
  1. Feature Engineering
     - Find the correlations between features and look at ways to reduce the number of features.
     - Text tranformations: Convert textual data into numeric format
  2. Building Baseline Models for classification
    - Build models using Linear Regression, Decision Trees, K-Nearest Neighbors and SVMs for classification.
