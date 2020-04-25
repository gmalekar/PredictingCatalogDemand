# Predicting Catalog Demand

## Project Overview
In this project, I will analyze a business problem in the mail-order catalog business. I have to predict how much money the company can expect to earn from sending out a catalog to new customers.   This task will involve building the predictive model and applying the results to provide a recommendation to management. 

## The Business Problem
You recently started working for a company that manufactures and sells high-end home goods. Last year the company sent out its first print catalog, and is preparing to send out this year's catalog in the coming months. The company has 250 new customers from their mailing list that they want to send the catalog to.

Your manager has been asked to determine how much profit the company can expect from sending a catalog to these customers. You, the business analyst, are assigned to help your manager run the numbers. While fairly knowledgeable about data analysis, your manager is not very familiar with predictive models.

You’ve been asked to predict the expected profit from these 250 new customers. Management does not want to send the catalog out to these new customers unless the expected profit contribution exceeds $10,000.

### Details
The costs of printing and distributing is $6.50 per catalog.
The average gross margin (price - cost) on all products sold through the catalog is 50%.

We will follow a CRISP-DM problem solving framwork to tackle this business issue.

## Understanding the business problem and data.

The objective of the project is to predict the profit we can expect by sending out a catalog to the new 250 customers.

The decision to make is whether we should send out a catalog to the new customers? The management wants to send out these catalogs to new customers only if the expected profit contribution exceeds $10,000.

We need data about how much it costs to produce and distribute the catalog. We also need historical data about previous sales. We need details about how many products on an average the customers bought what was their revenue.

## Analysis, Modeling, and Validation
**Target Variable:** The average sale amount is going to be our target variable, as we are trying to predict the profit.
**Predictor Variables:** To begin, we are first going to take a look at all the variables available and their data type.
| Variable | Data Type |
| Customer_ID | Numerical(Discreet) |
| Address | Categorical |
| City | Categorical |
| State | Categorical |
| ZIP | Numerical(Discreet) |
| Avg_Sale_Amount | Numerical |
| Store_Number | Categorical (nominal) |
| Responded_to_Last_Catalog | Bool |
| Avg_Num_Products_Purchased | Numerical |
| #Years_as_Customer | Numerical |

Straight away we are going to drop a few variables from contention, we are dropping these variables based on sound understanding of business as these variables will not affect the sales amount.
1. Name
2. Customer Id
3. Address
4. City
5. State

### Let us take a look at numerical variables first.
1. Avg_Num_Products_Purchased.
The correlation coefficient between the average number of products purchased and the average sale amount is 0.86. Also, you can see the same strong positive linear relationship in the graph below.
