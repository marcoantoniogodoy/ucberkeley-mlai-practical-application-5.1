# Practical Application Assignment 5.1: Will the Customer Accept the Coupon?

## Overview:
This repository contains a data analysis performed by Marco A. Godoy as part of the Practical Application Assignment 5.1 for the UC Berkeley Professional Certificate in ML/AI Program (2023).   

For a link to the Jupyter Notebook, please click here: <br/>
https://github.com/marcoantoniogodoy/ucberkeley-mlai-practical-application-5.1/blob/main/prompt.ipynb

Contact Information:<br/>
https://www.linkedin.com/in/marco-antonio-godoy

## Data:
This data comes to us from the UCI Machine Learning repository and was collected via a survey on Amazon Mechanical Turk. The survey describes different driving scenarios, including the destination, current time, weather, passenger, etc., and then asks people whether they will accept the coupon if they are the driver. Answers given that the users will drive there “right away” or “later before the coupon expires” are labeled as “Y = 1”, and answers “no, I do not want the coupon” are labeled as “Y = 0”. There are five different types of coupons—less expensive restaurants (under $20), coffee houses, carry out and take away, bars, and more expensive restaurants ($20–$50).

## Summary of the results obtained from the analysis

### Conducted Analysis:
- Overall acceptance rate of bar coupons: 41.0%
- Acceptance rate by group:
    - Those who went to a bar 3 or fewer times in a month: 37.1% 
    - Those who went to a bar more than 3 times in a month: 76.9%
    - Drivers who are over 25 years old and visit a bar more than once a month accepted the coupon: 69.4% vs 33.6% (all others)
    - Drivers who go to bars more than once a month and had passengers who were not a kid and had occupations other than farming, fishing, or forestry: 71.2% vs 29.7% (all others)
    - Drivers who go to bars more than once a month, had passengers who were not a kid, and were not widowed: 71.2%
    - Drivers who go to bars more than once a month and are under the age of 30: 67.0% 
    - Drivers who go to bars more than once a month and are under the age of 31: 72.0%
    - Drivers who go to cheap restaurants more than 4 times a month and income is less than 50K: 45.3% 


<b>Hypothesis:</b></br>
Based on the data obtained thus far, we can draw the following hypothesis:
The highest acceptance rate for bar coupons will come from those who go to a bar more than 3 times a month, followed by drivers aged under 31 years old who go to the bar more than once in a month. On the other hand, we may predict that the lowest acceptance rate for bar coupons will come from those who go to a bar 3 or less times in a month. 


### Independent Investigation:
From the independent portion of this analysis, we draw the following conclusions about the characteristics of the population with the highest coupon engagement rate:

1. Their acceptance is higher for coupons of type "Coffee House", "Restaurant(<20)" and "Carry out & Take Away". 
2. They're of age "21 through 30", almost equally distributed among males and females, and with no children.   
3. Most of the population drives alone, followed by the population that travel with friends.
    - There is a higher engagement from those traveling alone in opposite direction to work. 
    - There is a higher engagement from those traveling alone in the same direction to home. 
    - Those traveling with friends engage while traveling to a "No Urgent Place" (not going to work or home).
4. They have an income between $12,500 and $37,499, and those with the occupation "Student" show higher acceptance than others. 
5. Their occupations are distributed among "Unemployed", "Student" and "Computer & Mathematical". The population with these three occupations represents slightly over half of the population that accepts coupons on the dataset. 
6. 97.9% of the entries on this subset of the data contain null values on the "car" column. For this analysis, we assumed that unless the car column contained the value "do not drive" the person is a driver. We support this assumption with the fact that the entries with NULL values also contain information about the passenger. Therefore, the assumption is that the null values represent missing information about the car type.
7. More than half of the population (57.9%) is single.
8. The vast majority of the coupons were accepted on a sunny day, with a higher proportion when the temperature is 80 F. 
9. The highest acceptance is at 6PM, with a higher proportion of coupons expiring within 1 day (1d).  
10. This population visits all establishment types 1~3 times per month, with a higher proportion on the "carry_away" establishment type.   
11. There's almost an exact proportion (~37%) of those with a "Bachelors degree" and those with "Some colle - no degree".  
12. Other characteristics about this population: 
	- They do not have children.
	- They accept the coupons when within a distance 15min and 25min to the establishment.
	- They drive in the opposite direction to their destination when they accept the coupon.

## Next Steps & Recommendations:
Although we've obtained valuable insights from this analysis, the fact that so many entries do not have a value (NULL) in the car column represents a concern about the results' quality. The assumption throughout this analysis was that entries without car information still meant drivers. This assumption is supported by most of those entries that also contained "passenger" information. Also, from the description provided with the dataset, it can be inferred that all entries had information about drivers.

However, a recommended next step would be to find out why this information was missing and try to obtain it from another source if possible. Once available, rerunning this analysis and comparing results would be best.

