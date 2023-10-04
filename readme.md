# Practical Application Assigment 5.1: Will the Customer Accept the Coupon?

## Overview:
This repository contains an data analysis performed by Marco A. Godoy as part of the Practical Application Assigment for the UC Berkley Professional Certificate in ML/AI Program 2023.   

## Data:
This data comes to us from the UCI Machine Learning repository and was collected via a survey on Amazon Mechanical Turk. The survey describes different driving scenarios, including the destination, current time, weather, passenger, etc., and then asks people whether they will accept the coupon if they are the driver. Answers given that the users will drive there “right away” or “later before the coupon expires” are labeled as “Y = 1”, and answers “no, I do not want the coupon” are labeled as “Y = 0”. There are five different types of coupons—less expensive restaurants (under $20), coffee houses, carry out and take away, bars, and more expensive restaurants ($20–$50).

## Summary of the results obtained from the analysis

### Conducted Analysis:
- 41.0% of bar coupons were accepted
- 37.1% of those who went to a bar 3 or fewer times in a month
- 76.9% of those who went to a bar more than 3 times in a month
- 69.4% of drivers who are over 25 year old visit a bar more than once month accepted the coupon vs. an acceptance rate of 33.6% from all others
- 71.2% of drivers who go to bars more than once a month and had passengers that were not a kid and had occupations other than farming, fishing, or forestry accepted the coupon vs 29.7% from all others
- 71.2% of drivers go to bars more than once a month, had passengers that were not a kid, and were not widowed
- 67.0% of drivers that go to bars more than once a month and are under the age of 30 (please read note above)
- 72.0% of drivers that go to bars more than once a month and are under the age of 31 (please read note above)
- 45.3% of drivers that go to cheap restaurants more than 4 times a month and income is less than 50K


<b>Hypothesis:</b></br>
Based on the data obtained thus far, we can draw the following hypothesis:
The highest acceptance rate for bar coupons will come from those that go to a bar more than 3 times a month, followed by drivers aged under 31 years old that go to the bar more than once in a month. On the other hand, we may predict that the lowest acceptance rate for bar coupons will come from those who go to a bar 3 or less times in a month. 


### Independent Investigation:
From this independent analysis, we draw the following conclusions about the characteristics of the population with the highest coupon engagement rate:

1. They're acceptance is higher for coupons of type "Coffee House", "Restaurant(<20)" and "Carry out & Take Away". 
2. They're of age "21 through 30", almost equally distributed among males and females, and with no children.   
3. The majority of the population drives alone, followed by the population thats travel with friends.
    - There is a higher engagement from those traveling alone in opposite direction to work. 
    - There is a higher engagement from those traveling alone in the same direction to home. 
    - Those traveling with friends engage while traveling to a "No Urgent Place" (not going to work or home).
4. They have an income between $12,500 and $37,499, and those with occupation "Student" show higher acceptance than others. 
5. Their occupations is distributed among "Unemployed", "Student" and "Computer & Mathematical". The population with these three occupations represent slightly over half of the entire population that accepts coupons on the dataset. 
6. 97.9% of the entries on this subset of the data contain null values on the "car" column. For this analysis, we assumed that unless the car column contained the value "do not drive" the person is a driver. We support this assumption with the fact that the entries with NULL values also contain information about the passanger. Therefore, the assumption is that the null values represent missing information about the car type.
7. More than half of the population (57.9%) is single.
8. The vast majority of the coupons were accepted on a sunny day, with a higher proportion when the temperature is 80 F. 
9. The highest acceptance is at 6PM, with a higher proportion on coupons expiring witin 1 day (1d).  
10. This population visits all establishment types 1~3 times per month, with a higher proportion on the "carry_away" establishement type.   
11. Ther's almost an exact proportion (~37%) from those with a "Bachelors degree" and those with "Some colle - no degree".  
12. Other characteristics about this population: 
	- They do not have children.
	- They accept the coupons when in a distance to the coupon within 15min and 25min.
	- They drive in the opposite direction to their destination when they accept the coupon.
