# Analysis-and-Prediction-on-Online-Shopper-intention-at-E-commerce-Website
I utilize a dataset from https://archive.ics.uci.edu/ for this project. to examine and foresee how customers will behave when making purchases from an e-commerce website. Companies can use the findings of analysis and forecasts to enhance their marketing and revenue strategy for the upcoming year.

## Background 
In order to enhance marketing and boost income in the upcoming year, Company X plans to examine consumer activity patterns on their e-commerce website and their effect on revenue. Additionally, businesses require a model that accurately forecasts whether a user has the ability to boost revenue or not

## Objective
1. Get insights into visitor intention from duration, Page visit, and Conversion toward revenue
2. Build model to predict visitor behaviour towards revenue using classification method
3. Develop business recommendations to increase revenue from visitor sessions

## Data dictionary
this dataset consist of 12330 visitors session where the conversion visitors only 15% among them. The columns are :
1. `Administrative` : Number of pages visited by the visitor about account management
2. `Administrative_Duration` : the amount of time (in seconds) spent on administrative page type
3. `Informational` : Number of pages visited by the visitor about Web site, communication and address information of the shopping site
4. `Informational_Duration`: The amount of time spent (in seconds) on informational page type
5. `ProductRelated` : Number of pages visted by visitor about product related pages
6. `ProductRelated_Duration`: the amount of time spent (in seconds) of product related page
7. `BounceRates` : The percentage of visitors who enter the website through that page and exit without triggering any additional tasks
8. `ExitRates` : The percentage of pageviews on the website that end at that specific page
9. `PageValues` : the average value of the page averaged over the value of the target page and/or the completion of an eCommerce
10. `SpecialDay` : this value represents the closeness of site visiting time date to specific special days (e.g Mother's Day or valentine's Day).  
11. `OperatingSystems` : an integer value representing the operating system that the user was on when viewing the page
12. `Month`: contains the month of page view occured (in string form)
13. `Browser` : an integer value representng the browser that the user was using to view the page
14. `Region` : an integer value representing which region the user located in
15. `TrafficType` : an integer value representing what type traffic that the user is categorized into (e.g banner, SMS, direct)
16. `VisitorType` :string representing wheter a visitoer is new vistor, returning visitor, or other
17. `Weekend` : a boolean representing wheter the session is on weekend
18. `Revenue` : a boolean representing wheter or not the use completed the purchase

**Note** :
The "Special Day" feature indicates the closeness of the site visiting time to a specific special day (e.g. Mother’s Day, Valentine's Day) in which the sessions are more likely to be finalized with transaction. The value of this attribute is determined by considering the dynamics of e-commerce such as the duration between the order date and delivery date. For example, for Valentina’s day, this value takes a nonzero value between February 2 and February 12 ( 2 week before the special day), zero before and after this date unless it is close to another special day, and its maximum value of 1 on February 8 ( a week before special day.

