# Customer Churn Prediction Using Tree Based Models

This project was done in collaboration with [David Gayan](https://www.linkedin.com/in/davidgadyan/) and Wang Chunfeng as part of the Barcelona School of Economics's Computational Machine Learning module. 

We were tasked with developing an algorithm that can predict if a customer will cancel their service (aka churn). We are given a dataset containing telecommunication information of 3,333 customers with the following features:

- Churn (target): 1 if customer cancelled service, 0 if not
- AccountWeeks: number of weeks customer has had active account
- ContractRenewal: 1 if customer recently renewed contract, 0 if not
- DataPlan: 1 if customer has data plan, 0 if not
- DataUsage: gigabytes of monthly data usage
- CustServCalls: number of calls into customer service
- DayMins: average daytime minutes per month
- DayCalls: average number of daytime calls
- MonthlyCharge: average monthly bill
- OverageFee: largest overage fee in last 12 months
- RoamMins: average number of roaming minutes

15% of these customers had churned.

We used decision tree based algorithms to accomplish the task. The model with the best performance was a Random Forest Classifier with an AUC of .905, meaning the model will use the data provided to predict churn accurately 90% of the time. 

Based on this model the features driving churn the most are the average daytime minutes per month, the average monthly bill, and number of calls into customer service. Given this information I went back to the data to see in what way these variables would affect churn. I found that customers that churned had on average higher daytime minutes per month and higher average monthly bills than those that didn't. Futhermore, the majority of customers that churned all shared an average monthly of $70 (and overall had higher bills than customers that didn't churn). Perhaps this was just a slew of customers that wanted to take advantage of a promotion and once it ended stop using the service. 

Some potential tactics that could be deployed to reduce churn based on this information:

- Find ways to reduce the number of calls into customer service by creating comprehensive documenation on products and services online.
- If a person is using many daytime minutes and is conscious they are above average in this regard, then they might be more likely to seek out better deals with other telecommunication providers. Rewarding high use customers with a small discount on their next monthly bill may reduce their desire to switch providers. 


