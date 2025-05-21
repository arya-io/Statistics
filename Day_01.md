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

-------------------------------------------------------------------------------------

Numpy will make your code difficult to write and understand.
Instead use Pandas and code. We must only know the basics of Numpy.

# Pandas:
Pandas: Library for Data Analysis
Extremely powerful and flexible table (DataFrame) system built on top of NumPy
Computationally very efficient
Features
Read/Write data – Many formats supported
Indexing, Applying logic, Sub-setting, etc
Handle missing data
Adjust and restructure data

# NumPy Compared to Pandas

Numpy:
Aim: Numerical computation using n-dimensional arrays
Data types: Mainly Integer, Float
Performance: Very fast
Indexing: Integer-based (e.g. array [0,1]) 
Built-in operations: Numerical and linear-algebra related
Time-series data: No support

Pandas:
Aim: Data processing using series and dataframes
Data types: Numeric, Text, Date
Performance: Relative slower
Indexing: Additionally also supports label-indexing (e.g. df[‘age’]
Built-in operations: Data analysis tools such as merging, sorting, joining, handling missing data, etc
Time-series data: Excellent support such as date-based indexing, shifting, resampling, etc

# Pandas: Main Topics

Series and DataFrames
Conditional filtering and useful methods
Missing data
Grouping operations
Combining dataframes
Text methods and Time methods
Inputs and Outputs

# Series

Series: A data structure that holds an array of information along with a named index
The named index distinguishes it from a NumPy array

NumPy array has numeric index

Index	Data
0	1776
1	1867
2	1821![image](https://github.com/user-attachments/assets/66499689-a2dc-4646-b66d-ff8c5731f1fe)
Finding data using this index is not easy

Pandas series has a labelled index
Labelled Index	Data
USA	1776
Canada	1867
England	1821![image](https://github.com/user-attachments/assets/6a4f62ff-bf9e-4bd5-b7b9-c998d682cf1f)
Finding data using this index is very easy

Note: Data is internally still numerically organized!
Numeric Index	Labelled Index	Data
0	USA	1776
1	Canada	1867
2	England	1821![image](https://github.com/user-attachments/assets/088670c0-59fb-4d0d-8e88-ac936f2d8c89)
We can still use the numeric index, if we want

# DataFrame

DataFrame: Table of columns and rows that can be easily restructured/filtered
Series
Index	Year
USA	1776
Canada	1867
England	1821![image](https://github.com/user-attachments/assets/8e197680-6285-4e28-a8fd-ec1e43244509)

Multiple Series with the Same Index
Index	Year
USA	1776
Canada	1867
England	1821![image](https://github.com/user-attachments/assets/5f607abe-17d5-4f1d-8a83-9506bc3fe23d)
Index	Pop
USA	328
Canada	38
England	126![image](https://github.com/user-attachments/assets/16d52b28-1839-4e23-b699-63db39e0dc01)
Index	GDP
USA	20.5
Canada	1.7
England	3.9![image](https://github.com/user-attachments/assets/584cf1ab-c286-4649-9c26-eb793a700b05)
Dataframe
Index	Year	Pop	GDP
USA	1776	328	20.5
Canada	1867	38	1.7
England	1821	126	3.9![image](https://github.com/user-attachments/assets/ac50d367-841d-41d2-a87b-0e65faa02f9f)
So, Dataframe = Several series that share the same index, like a spreadsheet

---

Day 03:

# Individuals and Variables

Individual: Item in a dataset (e.g., Person)
Variable: Property of an individual (e.g., Hours of Study)
Independent Variable (Feature): Used to predict something (e.g., Hours of Study)
Dependent variable (Label): The predicted value (e.g., Grade)
Using Independent and Dependent Variables, we perform prediction tasks.
This classification is more Machine Learning and Data Analysis oriented
In Machine Learning Training, One or more Independent Variable -> Dependent Variable

# Variable Types: Qualitative and Quantitative

Qualitative: Categorical (e.g., Grade), Non-numeric
Quantitative variables: Numeric, Can be measured (e.g., Hours of Study)
These are known as Levels/Scales

Quantitative can be sub divided into Discrete and Continuous
Continuous can be sub divided into Interval and Ratio
Qualitative/Categorical can be sub divided into Nominal and Ordinal

# Quantitative Variable Sub-types

Discrete Variables: Countable and take specific values
e.g., Rank: 1, 2, 3 but not 1.8

Continuous variables: Measurable, but not a specific value
e.g., Height of a person: 5 feet 5 inches 5 cm 2 mm..

---
# Levels/Scales of Measurement of Data

There are 4 scales of data:

## Nominal:
Categorical data with no inherent order or ranking
e.g., Gender, colour, race, cuisine
We cannot create hierarchy here

## Ordinal:
Categorical data with a meaningful order or ranking, but intervals between ranks are inconsistent or unknown
e.g., Education level (High school, Bachelor's Master's), Customer satisfaction (Satisfied, Neutral, Unsatisfied)
Ordinal data is better than Nominal.

Interval and Ratio are numeric.

## Interval:
Numeric data with meaningful and consistent intervals between them without a true zero point.. Ratio cannot be measured
Intervals are fixed, they move consistently
e.g., IQ, Calendar data, Time of the day, Temperatures in Celsius or Fahrenheit

True Zero / Absolute Zero: Does the 0 in the data indicate starting point?
e.g. Suppose there is a exam with no negative marking. And someone gets 0 marks. So 0 is a starting point here.
e.g. Suppose there is a exam with negative marking. And someone gets 0 marks. So 0 is not the starting point here. Someone might also get negative marks.

## Ratio:
Numeric data where both intervals and ratios are meaningful and there is a true zero point
e.g., Height, Weight, Income, Distance travelled, Student marks

Among all above, Ratio data is the BEST and Nominal is the worst.
Ordinal is better than Nominal, Interval is better than Ordinal, Ratio is better than Interval.

---

# Measures of Location

Measures of Location / Measures of Central Tendency (Middle Value): A single value that represents the “centering” of a set of data, e.g. average
Example: Marks obtained by 10 students, arranged in an ascending order … 45,56,61,65,68,71,73,79,82,88,91
It includes Mean, Mode and Median.

![image](https://github.com/user-attachments/assets/3ef12b43-91a1-4c15-9f4b-2cbee2b2de9a)

Measures of Dispersion ("How Much Variation"):
Range(IQR)
Variance
Standard Deviation

---

# Basic Usage

Mean: Better if the data is normally distributed and there are no outliers … Used for interval and ratio data
Median: Better when the data is skewed (has extreme values) … Used for ordinal, interval, and ratio data
Mode: Useful for identifying the most common value or values in a dataset … Used in all the four scales … Best for categorical data

Normally Distributed Data:
![image](https://github.com/user-attachments/assets/64a4b852-730e-4e99-acbb-ce985645b798)

Skewed Data:
![image](https://github.com/user-attachments/assets/54a41ec7-41d7-4491-9192-b93a8dec8116)

---

# Mean

Mean: Average
Sample Marks: 45,56,61,65,68,71,73,79,82,88,91
Mean = 45+56+61+65+68+71+73+79+82+88+91/11
Mean = 789/11
Mean ≈ 71.727
In statistical terms: μ = ∑_i=1^n▒x_i/n
Extreme values (outliers) can impact mean
Test scores: 70, 80, 90, 85, and 75 … Mean: 80
Test scores: 70, 80, 90, 85, 75, and 2 … Mean: 66

---

# Median:

Median: The middle value when values are in ascending/descending order
Divides the dataset into two equal halves
Odd number of values in the dataset: Median is the middle value
Even number of values in the dataset: Median is the average of the two middle values
Scores: 62, 78, 84, 89, 91, 95, 97 ---> Median = 89
Scores: 62, 78, 84, 89, 91, 95 ---> Median = 84+89/2= 86.5
Outliers do not impact median as much as they impact mean
Mean of 56, 78, 45, 49, 55, 62 = 57.5
Mean of 56, 180, 45, 49, 55, 62 = 74.5
Corresponding medians = 55.5 and again = 55.5

Why is this not getting impacted by outliers?
Because outliers are present at the extremes.
And Median ignores extremes values.

---

# Mode

Mode: The value that occurs most frequently in a dataset
Data: 62, 78, 84, 89, 91, 95, 97, 89, 91, 89
Frequency: 62: 1, 78: 1, 84: 1, 89: 3, 91: 2, 95: 1, 97: 1
Mode  = 89
What if there are multiple values with the same highest frequency?: Multimodal data
If we have two modes: bi-modal
If we have three modes: tri-modal
Not used much in practice
No calculations in Mode, only counting

---

# Measures of Dispersion

Spread / Measures of Dispersion / Scatter:
How and by how much, our data set is spread out around its center?

![image](https://github.com/user-attachments/assets/3ad37d7a-28bb-45c3-9832-429a31ddcfd3)

# Range

Range: Difference between the maximum value and the minimum value in the data set 
Affected by outliers

![image](https://github.com/user-attachments/assets/965538e2-6704-47af-8518-f421feae94ef)

Example: 8, 11, 5, 9, 7, 6, 2500
Range = Max – Min = 2500 – 5 = 2495, which is quite meaningless
Solution: Inter Quartile Range (IQR)
But first, we need to understand percentile and quartile

---

# Percentile

Percentile (Relative): ≠ Percentage (Absolute)
Percentile: A value below which certain percentage of observations lie
Slices percentage data into two parts: Below a certain cut off, Above the same cut off
kth percentile = k% data is below it, and rest is above it
Examples: 
If you are in the 90th percentile in an examination, 90% students are below you and 10% students are above you
If a patient’s blood pressure is in the 60th percentile, 60% patients have a blood pressure less than this patient, and 40% patients have higher blood pressure than this patient
Median = 50th percentile

# Percentile Example

General Graph:

![image](https://github.com/user-attachments/assets/0c7bc7b0-72d7-41b9-ad34-842b7294f288)

Score at the 62nd percentile:

![image](https://github.com/user-attachments/assets/60e75f0e-0037-43af-9171-35bf1334ce16)

Sorted Marks of 20 students: 65,72,78,80,81,83,85,87,88,90,91,92,93,94,95,96,97,98,99,100
10th percentile position = Desired percentile/100 x Number of observations+1 = 10/100 x 21=2.10
Marks at 10th percentile = Marks at the second position ~ (72 +78)/2 = 75
Interpretation: 10% students lie below 75 marks, 90% are above 75 marks

90th percentile position =Desired percentile/100 x Number of observations +1 = 90/100 x 21=18.9 ~(98+99)/2 = 98.5
Marks at 90th percentile = Marks at the 18th position = 98.5
Interpretation: 90% students lie below 98.5 marks, 10% are above 98.5 marks

Sorted Marks of 20 students: 65,72,78,80,81,83,85,87,88,90,91,92,93,94,95,96,97,98,99,100

Another type of question: At what percentile are 85 marks in the above list?
Percentile for 85 marks = Number of observations below tℎe given value/Number of observations x 100=6/20 x 100 = 30
85 marks are at the 30th percentile
Interpretation: 30% students lie below 85 marks, 70% are above 85 marks
Note: Here we use Number of observations, and not Number of observations + 1

---

# US Household Net Worth and Percentile

Category	Percentile 	Net Worth
Poor	20th 	$10,000
Middle class	50th	$281,000
Wealthy	90th	$1.9 million

![image](https://github.com/user-attachments/assets/c8648efe-7f10-4912-9c07-4a1c90ab27df)

---

# Quartile

Percentile: Divides data into 100 equal parts
Quartile: Divides data into 4 equal parts
First Quartile (Q1) = 25th percentile
Second Quartile (Q2) = 50th percentile = Median
Third Quartile (Q3) = 75th percentile

Sorted Marks of 20 students: 65,72,78,80,81,83,85,87,88,90,91,92,93,94,95,96,97,98,99,100
Position of Q1 = Percentile/100 x (n+1)=25/100 x 21=525/100=5.25, So Q1 = Average of 81 and 83 = 82
Position of Q2 = Percentile/100 x (n+1)=50/100 x 21=1050/100=10.5, So Q2 = Average of 90 and 91 = 90.5
Position of Q3 = Percentile/100 x (n+1)=75/100 x 21=1575/100=15.75, So Q3 = Average of 95 and 96 = 95.5

![image](https://github.com/user-attachments/assets/bc5d962a-af84-4579-97e2-2055efb224b9)

Box Plot precisely shows Quartiles

---

# Inter Quartile Range (IQR)

Inter Quartile Range (IQR) = Q3 – Q1 = Middle 50% of the data
In the given example: IQR = Q3 – Q1 = 95.5 – 82 = 13.5
Handles outliers better than range, since the extreme values at both the ends are ignored in IQR
Since it uses percentiles rather than actual values, it is less affected by skewed data (See Skewness)
Outliers: Data points that are significantly outside of the typical range of values
Lower bound: Q1 – (1.5 * IQR) = 82 – (1.5 * 13.5) = 61.75
Upper bound: Q3 + (1.5 * IQR) = 82 + (1.5 * 13.5) = 102.25
Box Plot internally calculates Lower Bound and Upper Bound
Points below the lower bound or above the upper bound are outliers
In our example, there are no such points, so we do not have any outliers

# Outlier Example

Commute times for 14 randomly selected adults in minutes: 16, 8, 35, 17, 13, 15, 15, 5, 16, 25, 20, 20, 12, 10
Find outliers and draw a box plot
Solution: First sort them: 5, 8, 10, 12, 13, 15, 15, 16, 16, 17, 20, 20, 25, 35
Create a 5-number summary: Minimum, Q1, Q2, Q3, Maximum = 5, 12, 15.5, 20, and 35
Outlier
First calculate 1.5 * IQR = 1.5 x (20 – 12) = 1.5 x 8 = 12
Outliers calculation: Q1 – 12 = 12 – 12 = 0  and Q3 + 12 = 20 + 12 = 32
So, outliers = Commute time < 0 or > 32
Boxplot: Draw a vertical line between 5 and 35; Draw a box with 12 and 20; Draw a median line at 15.5, Show outlier points

---

# Outlier Code

import matplotlib.pyplot as plt
import seaborn as sns

# Data
commuter_times = [16, 8, 35, 17, 13, 15, 15, 5, 16, 25, 20, 20, 12, 10]

# Create the box plot
plt.figure(figsize=(10, 6))
sns.boxplot(data=commuter_times, orient='h')

# Add titles and labels
plt.title('Box Plot of Commuter Times')
plt.xlabel('Minutes')

# Show the plot
plt.show()

---

# Resulting Boxplot

![image](https://github.com/user-attachments/assets/325e00c2-df0b-4fd3-b2a6-d841b52e26af)

---

# Variance

Variance = How far are data points from their mean?
High variance = Data is more scattered from its mean. Data is less uniform.
Low variance = Data is less scattered from mean. Data is uniform.
Variance calculation:
Find the mean of the given data set
Subtract the mean from each value and square the result
The average of these squared values is the variance

## Variance Formula

Population variance (Whole data)
σ2 = ∑_i=1^N▒(xi − μ)2/N
xi = Data points
μ = Population mean
N = Number of observations (Population size)

Sample variance (Selected data)
S2 = ∑_i=1^n▒(xi − x ̅)2/n−1
xi = Data points
x ̅ = Sample mean
n = Number of observations (Sample size)

## Variance Example

Consider data values 5, 7, 10, 12, and 15
Step 1: Mean (μ) : (5 + 7 + 10 + 12 + 15)/5 = 9.8
Step 2: Subtract mean from each number and square the result
(5 - 9.8)2 = 20.24
(7 - 9.8)2 = 6.76
(10 - 9.8)2 = 0.04
(12 - 9.8)2 = 5.44
(15 - 9.8)2 = 27.04
Step 3: Add up the squared differences and divide by the total number of numbers: (20.24 + 6.76 + 0.04 + 5.44 + 27.04)/5 = 11.12 = Variance (σ2)

Why do we square values in Variance?
Because if we don't square, the negative and positive values will cancel out each other.
We want outliers to be highlighted or punished.

Why are the Differences Squared?

If we do not do this, then the positive and negative differences may cancel each other and we may not be able to find how the data points are dispersed from the mean
Example: Consider marks of 5 students: 55, 60, 65, 54, 64
Mean: 59.6, Variance: 20.24
But if we do not square the differences, what will happen?
Marks	Marks - Mean	(Marks - Mean) Squared
55	-4.6	21.16
60	0.4	0.16
65	5.4	29.16
54	-5.6	31.36
64	4.4	19.36
		
Mean	(Marks - Mean) / 5	((Marks - Mean) Squared)) / 5
59.6	0.00	20.24

![image](https://github.com/user-attachments/assets/35fa813b-cf6f-456e-9a0a-1f41329262c4)

# Limitation of Variance: How to Quantify?

Quantifying/measuring variance is tough
Example: Consider marks of 10 students: 32, 39, 44, 56, 56, 63, 71, 72, 81, 89
Mean: 60.3, Variance: 306.81
Variance seems to be high, but it does not convey any meaningful information beyond this
This is a limitation of variance

---

# Standard Deviation

Standard deviation = Square root of variance 
The scale of variance is not to the scale of the original data
But the scale of standard deviation is the same as scale of the original data
Variance: Difficult to interpret, Standard deviation: Easy to interpret
Formula: σ = √1/N∑_i=1^N▒(x_i − μ)^2

Variance is difficult to interpret, and Standard Deviation is easy to interpret

---

# Standard Deviation Example

Deviation	Deviation Squared
76 – 69.10 = 6.9	47.61
89 – 69.10 = 19.9	396.01
53 – 69.10 = -16.1	259.21
75 – 69.10 = 5.9	34.81
80 – 69.10 = 10.9	118.81
67 – 69.10 = -2.1	4.41
61 – 69.10 = -8.1	65.61
59 – 69.10 = -10.1	102.01
71 – 69.10 = 1.9	3.61
60 – 69.10 = -9.1	82.81
Total:	1114.90
Variance (σ2) =	1114.90 / 10 = 111.49

![image](https://github.com/user-attachments/assets/88128a1e-5268-49a0-b92f-ff2fb4250d45)

Marks of 10 students: 76, 89, 53, 75, 80, 67, 61, 59, 71, 60
Mean (μ): 76 + 89 + 53 + 75 + 80 + 67 + 61 + 59 + 71 + 60/ 10 = 691/10 = 69.10

Standard deviation (σ) = √111.49 = 10.56

---

# Exercise

Interpret the data below
Group A and Group B are two groups of people and we have data about their blood sugar level

A = 125, 118, 121, 123, 119, 122, 117, 121, 124, 116, 120, 122, 119, 124, 118, 120, 123, 122, 118, 121

B = 150, 90, 115, 145, 118, 112, 135, 121, 117, 122, 119, 128, 115, 145, 120, 90, 155, 135, 122, 115

# Interpreting Standard Deviation

![image](https://github.com/user-attachments/assets/e12b5182-2712-4587-9bd7-301963c2fe5e)

# Standard Deviation: True Indicator of Homogeneous/Heterogeneous Data

Consider blood sugar levels of two groups of people:

A = 125, 118, 121, 123, 119, 122, 117, 121, 124, 116, 120, 122, 119, 124, 118, 120, 123, 122, 118, 121
Mean = 120 mg/dL, SD = 2.35 mg/dL
Most close to the mean (Fit)

B = 150, 90, 115, 145, 118, 112, 135, 121, 117, 122, 119, 128, 115, 145, 120, 90, 155, 135, 122, 115
Mean = 120 mg/dL, SD = 17.31 mg/dL
Some close to the mean (Fit), some away from the mean (Unfit)

---

# Interpreting Standard Deviation

Again consider A = 125, 118, 121, 123, 119, 122, 117, 121, 124, 116, 120, 122, 119, 124, 118, 120, 123, 122, 118, 121
Mean = 120 mg/dL, SD = 2.35 mg/dL
How to calculate how many standard deviations away is an observation from the mean?
Formula: Our data point − Mean/Standard Deviation
Person 1: (125 −120/2.35) = +2.12 standard deviation away from the mean
Person 2 (118 −120/2.35) = -0.85 standard deviations away from the mean

---

# Coefficient of Variation (CV)

Coefficient of variation (CV): Standard deviation divided by mean
SD: Expressed in the original scale/units of data (Absolute measure)
CV: Expressed in percentage, so not dependent on the units of data (Relative measure)
High CV = Large SD compared to mean … If it is 100%, it means SD = mean
CV= SD/Mean x 100 %
Example: A pizza restaurant measures its delivery time in minutes. The mean delivery time is 20 minutes and the standard deviation is 5 minutes.
CV=SD/Mean x 100 %= 5/20 x 100 % = 25%

Now suppose a second pizza restaurant has a mean delivery time of 15 minutes and the standard deviation is 10 minutes. Calculate the coefficient of variation and compare with the first one.
CV=SD/Mean x 100 %= 10/15 x 100 % = 66%

Calculation for the first pizza restaurant was:
CV=SD/Mean x 100 %= 5/20 x 100 % = 25%

What will be our interpretation?
A lower Coefficient of Variance will be generally better.

---

# Problem

Two students A and B have appeared for five tests with the following results:
A: Mean score = 80, SD = 8
B: Mean score = 75, SD = 15
Who is more consistent?
CV for A = 8/80 x 100 = 10%
CV for B = 15/75 x 100 = 20%
A is more consistent

# Making Investment Decisions

Option A: Average return: 20%, SD: 15%
Option B: Average return: 6%, SD: 2%

Option A: CV=SD/Mean x 100 %= 15/20 x 100 % = 75%
Option B: CV=SD/Mean x 100 %= 2/6 x 100 % = 33%

Conclusion: Is Option B better?

---

# Skewness

Skew: Represents the asymmetry of a distribution around its mean
Skew = Where is the skew, not where is the data

Skew	Tail	Most Data	Interpretation
Right (Positive)	On the Right	On the Left	Most values are low
Left (Negative)	On the Left	On the Right	Most values are high

![image](https://github.com/user-attachments/assets/12aa1e43-4337-4fb6-811b-eff8f062ee99)

Students appearing in an Examination
No-skew: Student marks are evenly distributed (Data is symmetrical)
Right-skew: Most students get low marks => Long tail to the right  (higher values)
Left-skew: Most students get high marks => Long tail to the left (lower values)

---

![image](https://github.com/user-attachments/assets/d2febbe8-2512-498d-b24a-a5d86ccd0b32)

Zero-skew (No-skew): Mean = Median

Characteristic	Right (Positive) Skew	Left (Negative) Skew
Key feature	Most values are on the lower side, a few on are the higher side	Most values are on the higher side, a few are on the lower side
Statistics	Mean > Median	Mean < Median
Mean	Skewed to the right	Skewed to the left
Tail	Comes later - On the right (Represents high values)	Comes first - On the left (Represents low values)
More data points	On the left	On the right
Outliers	On the right	On the left
Ratings Example	Most people give ratings of 1 or 2 out of 5	Most people give ratings of 4 or 5 out of 5
Example	Incomes of people	Ages at the time of death
Why?	Most people have low incomes, Very few have very high income	Most people would die in older age, Very few children die

![image](https://github.com/user-attachments/assets/6d607473-70fa-4e15-841b-db5b2774387f)

# Simple Ratings Example

Consider 1 lakh people giving ratings on a scale of 1-5
No-skew: All ratings occur almost with the same frequency
Right-skew: Most people give low ratings (1/2)
Left-skew: Most people give high ratings (4/5)

![image](https://github.com/user-attachments/assets/7bae60be-5abc-4547-94db-34677a11ef3f)

# Covariance

Covariance: Quantifies how changes in one variable relate to changes in another
Scale: 
Covariance: Units of what we are measuring (difficult to interpret) 
Correlation: -1 and +1 (easy)

Example:

Area of the House	Price of the House
1200	75 lakhs
1300	90 lakhs
1500	1.10 crores![image](https://github.com/user-attachments/assets/5096e001-25e7-477f-8229-6acc5cba507b)

As area increases, price increases: But by how much? … Covariance

---

# Covariance Example

Height	Weight
65	68
67	69
68	70
66	69
64	65

![image](https://github.com/user-attachments/assets/f7d5395e-af08-4e40-86de-ae474e349c3e)

Cov (x,y) = ∑_i=1^n▒(x_i−x ̅)(yi−y ̅)/n−1
Mean height (x ̅) = 65+67+68+66+64/5 = 66
Mean weight (y ̅) = 68+69+70+69+65/5 = 68.2
For Heights: x_i−x ̅ = [65−66,67−66,68−66,66−66,64−66]=[−1,1,2,0,−2]
For Weights: y_i−y ̅ = [68−68.2,69−68.2,70−68.2,69−68.2,65−68.2]=[−0.2,0.8,1.8,0.8,−3.2]
(x_i−x ̅)(yi−y ̅) = (-1x-0.2) + (1x0.8) + (2x1.8) + (0x0.8) + (-2x-3.2) = 11
Cov (x,y) = ∑_i=1^n▒(x_i−x ̅)(yi−y ̅)/n−1= 11/4 = 2.75

# Covariance and Variance

As we know, Cov (x,y) = ∑_i=1^n▒(x_i−x ̅)(yi−y ̅)/n−1

What if we use x instead of y?
Cov (x,x) = ∑_i=1^n▒(x_i−x ̅)(x_i−x ̅)/n−1 

Remember: Variance (x) = ∑_i=1^n▒(x_i−x ̅)2/n−1= ∑_i=1^n▒(x_i−x ̅)(x_i−x ̅)/n−1 
So: Var (x) = Cov (x,x)

Covariance of x and y is nothing but variance of x and x.

---

# Correlation

Correlation: Are two numeric variables related?
Examples: Exercise and Health, Study and Marks, Experience and Salary
Correlation (x,y) = Cov (x, y)/σxσy
Measured using correlation coefficient (r)
Pearson Correlation Coefficient: Measures linear relationships between continuous variables
Spearman Rank Correlation Coefficient: Measures relationships, even if they are not strictly linear

# Pearson Correlation Coefficient Interpretation

Range: -1 to +1
Positive correlation: Variables move up together
Example: Correlation of 0.80 between Hours spent studying and test scores
Negative correlation: As one variable moves up, the other moves down
Example: Correlation of -0.70 between Hours spent watching TV and physical fitness
Zero correlation: Variables are unrelated
Example: Correlation of 0.02 between Shoe size and IQ score

# Positive, Negative, No Correlation

![image](https://github.com/user-attachments/assets/6e7ce3f5-2249-4407-acd9-09280d932f39)

















