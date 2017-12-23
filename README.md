# Gain-insight-into-financial-data
Provide recommendations to the users of a fintech org about web pages they haven't used yet, but are likely to find valuable.

## Introduction  

A fintech org has a very complex product suite. The website alone contains over 1,000 distinct pages which
provides their clients with access to hundreds of different market and business intelligence datasets. This
complexity can often make it difficult both for the end users to find the information they need, and for the
company's employees to understand how the clients use their products.  

## Dataset

The dataset consists of page view events on their website for a selected three-month period. When a particular
user account loads a particular web page on the website, that consitiutes one page view event.
There are two files in the dataset:  
page_usage.csv — Conatins records of distinct page view events.  
page_names.csv — Contains metadata about the web pages.  
The columns in the page_usage.csv file are:  
userID — Indicates the user account that initiated the page view. The values are unique IDs for end
user accounts.  
pageID — Indicates the web page that the user viewed. The values are unique IDs for web pages on
the website.  
day — the day in the three-month period on which the page view occurred.  
time — indicates the time-of-day at which the page view occurred.  
The columns in the page_names.csv file are:  
pageID — Unique IDs for web pages on the the website. These are consistent with the pageID
column in the page_usage.csv file.  
Name — A human-readable name for each page  

## Objective  

1. Observe any general patterns in the data.  
2. Report any logical groupings of the users.  
3. Report any logical groupings of the pages.  
4. Report any outliers.  
5. Take any user and recommend users similar to that user.  
6. Do the same for pages.  

### Analysis  

** Data Exploration **  

Two observations that can be made immediately :  
* Just 15 percent of the users consitute more than 80% of the total views.  
* Out of a total of 720 distinct page categories, top 35 most viewed constitute more than 90% of all the views.  
* Total number of users are 1138.
* Data is clean - zero nulls in the entire dataset.  

** Outliers **
Following pages seem to be irrelevant to provide any insights on the financial product, meaning they can be removed.  
* Login  
* Password  
* Settings Summary  
* New User Signup: Step 4  
* Redirector  
* Excel View  
* PDF View  
* New User Signup: Step 3  
One of the users visited a page more than 1500 times on a given day. That seems suspicious. Hence should be removed.  

Most of the views seem to have happened between 3PM to 8PM.



