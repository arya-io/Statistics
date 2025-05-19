# What is current and historical data?

Current data is for the transactions happening now.
Data which will go into DBMS. Whatever is the Database.
Historical Data is still important as we might require that in future.

Data Analytics: we use historical data and current data to make decisions and make future predictions.

ChatGPT also uses historical data and make predictions, one word at a time.

# Using Data
e.g., We can check and predict if the transaction is valid or invalid.

# Operational Data (Data Comes In)

- An account holder transfers money
- A customer places an order
- A loan is granted

# Analytical Data (Data Goes Out)

- Last month money transfer history
- Top 5 order conversions
- Loans report

# Data Warehousing

Data Warehouse and Database
We will keep our current data in DataBase historical data on Data Warehouse
Why do we keep these data separate?
Because Our database will get overloaded
Think of extremely high transaction
Querying will become difficult
RDBMS will be used to organise DataBase.

But what about Data Warehouse?
Should it be flat files, nosql..?
Therefore, we have Data warehouse products.
Most popular DW product is SnowFlake.
We can use SQL there.
Internally whether it is RDBMS, we don't care.

In Databases, we don't want any duplications.
We want ACID properties to be followed here.
In DW, we want opposite of this.
We do want duplicacy, we don't want normalization.
when we want data from multiple datas, we need to join and that is a very expensive task.
Instead, we keep all the data in one table.
In DW, there are maximum SELECT queries on historical data.
Wastage of space does not matter.
We just want everything to be queried fast.

Some people think that DW is dustbin.
But it is not the case.
It has to be well designed.
WE need to draw intelligent reports, do analytics, and perform data mining.
DW is carefully moving our data into the warehouse.
For this, we perform ETL (Extract, Transform and Load).
Extract means to extract meaningful data from multiple sources of different formats.
For example, Amazon may provide data in a different format, but then we will have to transform it.

Example, there is a customer and the saving account holder name is Sachin Tendulkar.
Credit Card holder name is S R Tendulkar
Loan Taker name is Tendulkar S R
When this data will go into data warehouse, there will be three different names
Therefore, this require transform.
This is at data level.
So transform is not only about transforming from csv to text and so on but also these things.

# What is ETL and ELT?
Today's world is moving from ETL to ELT.
People started realizing that load operation is taking too much time because data is vast.
Then intelligent solutions came up like SnowFlake.
It said extract first, then load and then transform.
Because they generally run on cloud and not on our servers/datawarehouses, e.g., AWS, GCP.
We just pay for the usage.
Modern solutions are cloud based, we don't worry about disk space.
And therefore we concentrate more on our important work and that is transform.

CRM
Biling
ERM

# Data - What is There for Me?

Data Engineering (Infrastructure):
Focus: Creating and maintaining infrastructure for Data Analysts and Data Scientists, Big Data Analytics, Data Visualization
Skills: Programming (Python/R), Apache Spark, Kafka, Databases (SQL, MongoDB)

Data Analytics (Decisions):
What happened?:
What were the sales figures?
How many users registered?
How many subscriptions got cancelled?

What is likely to happen?:
What will the sale be in this quarter?
How many total users will we have?
Will subscription cancellation rate drop to 10%?

Why did it happen?:
Which products were sold the most?
Did we have more mobile users?
Did cancellations happen after watching a particular movie?

What action should we take?
How do we grow sales?
How do we get to 1M users?
How do we take the subscription cancellation rate to 5?

Netflix was on the verge of shutdown.
So they organized a questionnarire and asked users what do they want to watch?
Their users still dropped.
Then they went to a Data Analytics firm and it said:
Don't ask people, just observe them.
Then they started recommending movies to them and we know the Netflix what it is today.

Facebook added new feature News Feed where updates of friends other than our friends were notified to the users.
Facebook which was fairly static became all of a sudden dynamic.

# Types of Data Analytics

Descriptive Analytics (Hindsight): What happened in the past?
Diagnostic Analytics: Why did it happen? (Dashboards, Business Intelligence)
Predictive Analytics (Insight): What will happen in the future? (Forecasting, Data mining, Regression, Simulations)
Prescriptive Analytics (Foresight): What is the best action? (Optimization, Decision Trees)

The person who achieves all these things is called as Data Analyst.

Data Science (Modelling, Product building):

Focus-1: Advanced statistical modelling (e.g., Machine Learning)
