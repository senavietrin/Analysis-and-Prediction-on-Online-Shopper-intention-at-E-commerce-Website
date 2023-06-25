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

## Exploratory Data Analysis

**1.Monthly Conversion**
![image](https://github.com/senavietrin/Analysis-and-Prediction-on-Online-Shopper-intention-at-E-commerce-Website/assets/116081571/d7323e3b-4402-4721-bc7c-801ac6f3098e)
- November sees the highest conversion rate (25%) although May sees the most visitors. The conversion significantly increased between February - March and June-November, but it sharply decreased in December

**2. Number of Visits and Duration Per Page By Visitor**
 - Administrative page: visited by revenue user about two times in a single session where they spent about 34 second at this page, while non revenue visitors have more duration and more visit
 - Product Related Page: revenue user visits this page about 24 times each session where they spent 15 minutes at this page, while non revenue visitors spent more duration and visit
 - Informational : users rarely visit this page , number of visitation and duration of revenue users is about 0 for this page
 - Informational Page: this page is rarely visited by users

**3. Bounce Rate, Exit Rate, and Pgae Value**
- Visitors who experience high Bounce Rate are more likely to have a high Exit Rate
- Visitors with Bouncer Rate higher than 0 and an Exit Rate higher than 0.016 are more likely tend to not purchase
- Returning visitors are more likely to abandon they journey because they have the greatest Bounce Rates and Exit Rates
  
**4. Top user region, traffic type, and browser type**
- Most users come from region 2 and 9 that dominated by around 80% returning visitors
- Most users use traffic type 16 and 7 that dominated by returning visitors
- Most users use browser type 12 and 13 where type 12 dominated by returning visitor and type 13 dominated by unsure/other visitors


## Model Building
![image](https://github.com/senavietrin/Analysis-and-Prediction-on-Online-Shopper-intention-at-E-commerce-Website/assets/116081571/efb1488b-0ed1-42d5-92af-6beaad98c576)
![image](https://github.com/senavietrin/Analysis-and-Prediction-on-Online-Shopper-intention-at-E-commerce-Website/assets/116081571/deeca04d-a7ba-48cf-acb8-d3075d7f4de7)
- best model is XGBoostClassifier with the F1 Score = 66% , precision = 74%, and recall = 59% and  AUC = 0.94
- True positive = 2510, False positive = 184, True negative = 265, False negative = 93
- Page value is the most influential features to the model

## SUMMARY
1. November saw the greatest conversion rate (25%).
2. Users tend to shop around holidays in February and May compared to special days in other months.
3. Users who successfully make a purchase or generate revenue typically visit and stay on pages for shorter periods of time than users who do not.
4. Due to their higher page value and income, new visitors have the potential to provide better conversions.
5. Returning visitors often only browse one page before leaving the website.
6. Regions 2 and 9 have the highest conversion rates, which are primarily made up of returning visitors.
7. The highest conversion rates are found in traffics 16 and 7, which are primarily made up of returning visitors.
8. The two browsers with the highest conversion rates are 12 and 13, with browser 12 dominated by returning visitors and browser 13 by other users.
9. Best Model is XGBoostClassifier with f1 score 66%

## Bussiness Recomendation
1. Because consumers frequently encounter high bounce rates and departure rates, companies must assess the content and user experience of their websites.
2. By running campaigns that capitalize on the month's holidays and related product highlights, monthly conversions can be raised.
3. Because returning visitor conversions are still lower than those of new visitors, they must be raised. This can be achieved by using points-based rewards and product suggestions that are relevant to user searches.
4. Provides customers from low-conversion regions with lower shipping cost
5. Adjusting the user experience to the user's preferred browser


