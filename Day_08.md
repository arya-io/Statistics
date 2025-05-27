# Chi-Square Test

Chi-square test: A statistical test used to compare observed results with expected results of categorical variables
Three types
Chi-square test of Independence (Are two categories independent? : Are gender and pet preference related?)
Chi-square test of Homogeneity (Is data within a category proportionate?: Do different servers of a company fail roughly at the same rate?)
Chi-square test of Goodness of Fit (Does data fit a particular distribution?: Is tossing a fair coin following binomial distribution?)
Data is arranged in a contingency table (crosstab_tips.py)

---

# Chi-Square Test – Formula

![image](https://github.com/user-attachments/assets/a605df0b-cb38-4739-9ee3-d8a79bea7d94)

Degrees of freedom is the number of variables that can vary in a calculation
The degrees of freedom for a Chi-square grid are equal to the number of rows minus one times the number of columns minus one: that is, (R-1)*(C-1). In our 2x2 grid, the degrees of independence will be (2-1)*(2-1), or 1

---

# Chi-square Test of Independence

Does gender affect which pet is liked more, for the following data?

Solution: First define Hypotheses
H0: Gender and preference for cats or dogs are independent.
H1: Gender and preference for cats or dogs are not independent.

Add up all the row and column values

Calculate “Expected value” for each cell by multiplying each row total by each column total and dividing it by the overall total

The estimated value for each cell is the total for its row multiplied by the total for its column, then divided by the total for the table: that is, (RowTotal*ColTotal)/GridTotal.

![image](https://github.com/user-attachments/assets/12041e10-02da-40db-92a0-a3d294db0fe6)

![image](https://github.com/user-attachments/assets/324f260c-0179-4f92-a67a-98bb04916812)

Resulting “Expected values” table

Subtract expected from observed, square it, and divide by expected

![image](https://github.com/user-attachments/assets/16b6fbca-d97a-4625-9532-46496c8df4c5)

![image](https://github.com/user-attachments/assets/c90ae294-e24e-42bd-a704-59fbb5fb2d3c)

![image](https://github.com/user-attachments/assets/2fd39436-3717-44a0-a1a8-a9896b69231b)

Now add up the calculated values
1.099 + 0.918 + 1.136 + 0.949 = 4.102
Chi-Square test statistic is 4.102
Now calculate Degrees of freedom = (row count – 1) x (column count – 1) = (2 – 1) x (2 – 1) = 1
Look up in the Chi-square table (https://people.richland.edu/james/lecture/m170/tbl-chi.html) for DF = 1 and alpha level of 0.05. The value (called as critical value) is 3.841, which is less than our Chi-square value.
Conclusion: Observed value (i.e. our Test statistic) > Critical value (i.e. the Chi-square Table value), so we reject the null hypothesis.

---

Determine the probability of an observed frequency of events, given its expected frequency
Example
We toss a coin 18 times and get 12 heads
Is it due to chance or is the coin biased?
Chi-square formula: Considers sum of square distances between observed values O and expected values E, divided by each expected value E
χ^2=∑▒(O−E)^2/E= (12−9)^2/9 + (6−9)^2/9 = 2.0

How to interpret this value (also called Test statistic)?
χ^2=∑▒(O−E)^2/E= (12−9)^2/9 + (6−9)^2/9 = 2.0

Low chi-square value = High correlation between observed and expected values (Because we are subtracting E from O and squaring it, and if it is low, it means E and O are close to each other)
Degrees of Freedom = Number of possible outcomes - 1 = 2 - 1 = 1
Because we have either Heads or Tails
Critical value with DF = 1 and α = 0.05 is 3.841 (https://www.scribbr.com/statistics/chi-square-distribution-table/)
H0 = 12 heads in 18 tosses is reasonable for a fair coin
Since Test statistic (2.0) < Critical value (3.841), we fail to reject H0

---

# Chi-square Test

What if we get 16 heads in 18 coin tosses?
χ^2=∑▒(O−E)^2/E= (16−9)^2/9 + (2−9)^2/9 = 10.88

High chi-square value = Low correlation between observed and expected values (Because we are subtracting E from O and squaring it, and if it is high, it means E and O are not close to each other)
Degrees of Freedom = Number of possible outcomes - 1 = 2 - 1 = 1
Because we have either Heads or Tails
Critical value with DF = 1 and α = 0.05 is 3.841 (https://www.scribbr.com/statistics/chi-square-distribution-table/)
H0 = 16 heads in 18 tosses is reasonable for a fair coin
Since Test statistic (10.88) > Critical value (3.841), we reject H0

---

# Chi-Square Test of Homogeneity

A company runs six identical servers for its IT infrastructure
It wants to find out if server failure is occurring at the same rate for all the servers
Assumptions
When a server fails, it does not necessarily mean that it will fail again (When we get Heads in a toss of a coin, it does not say anything about the next toss)
One server’s failure is not impacting any other server in any way
A server is either healthy or has failed – No in-between states
H0: There is no statistically significant difference between server failure rates

---

# Chi-Square Test of Homogeneity

Server failure actual values are given to us: We need to calculate expected values using them

Server	Observed Failure Count	Expected Failure Count
A	46	40
B	36	40
C	52	40
D	26	40
E	42	40
F	38	40
Total	240	

We expect all servers to have equal failure rate

Since Total Observed Count = 240, we need to divide it by the number of servers, 6 

So, Expected Failure Count for each server = 240 / 6 = 40

Chi-Square calculations		 χ^2=∑▒(O−E)^2/E

Finding Critical value using Python

from scipy.stats import chi2
print(chi2.isf(0.05, 5))

Server	O	E	O - E	(O - E)2 	𝑂−𝐸2𝐸
A	46	40	6	36	0.9
B	36	40	-4	16	0.4
C	52	40	12	144	3.6
D	26	40	-14	196	4.9
E	42	40	2	4	0.1
F	38	40	-2	4	0.1
Total	240				10

Chi-square Test statistic = 10

DF = 6 - 1 = 5
α = 0.05

Critical value = 11.07

Since Test statistic < Critical value, we fail to reject H0

---

# Predictive Modelling/Analytics

Predictive Analytics: Use statistics and modeling techniques to make predictions about future outcomes
Types: Regression and Classification
Common types: Linear regression, Logistic regression, Decision trees, Random forest, Neural networks, Time series forecasting, K Nearest Neighbors (KNN), Naïve Bayes, Clustering

---

# Regression

Regression: Predict a dependent variable (target) using independent variable(s) (features/predictors)
y: Dependent numeric variable
X: Independent variable(s)
We know X and we want to predict y
Linear regression: y is numeric
Logistic regression: y is categorical

---

Regression and Classification

Regression: Numeric target, Classification: Class target

Regression examples	Classification examples 
How many page views will we get?	Is this a fraudulent transaction?
What will be the amount of loss?	Whose face is in this picture?
What will be the blood sugar level?	Which product is best fit for the customer?

---

Regression gives numeric output while classification gives categories output.
Confusion About Regression

Why Logistic Regression comes under Classification even after being Regression because Regression and Classification are two different things?

![image](https://github.com/user-attachments/assets/abc14d6e-4889-4f27-96f4-37a5ef198dc2)

---

Main Types of Regression

Simple Linear Regression: Relationship between the independent variable and the dependent variable is linear (Taxi milage -> Bill amount)
Multiple Linear Regression: More than one independent variable – Also called multivariate analysis (Years of Work Experience + Education Level -> Salary)
Logistic Regression: Binary classification problems (Customer Tenure + Monthly Subscription Cost + Customer Complaints -> Churn?)

---

# Linear Regression

aka Least Squared Line
Line of Linear Regression is also known as "Line of 'Best Fit'"
Best means it should pass through most of the points
It minimizes the distance between the line and each data point
How is the best line selected?

![image](https://github.com/user-attachments/assets/35ee3248-4e27-48e9-bcaa-4346a9c5eb70)

y ̂=b_0+b_1x

b0 = y-intercept (Value of y when x = 0)
It tells at which point on y axis, the line is being started

b1 = slope (How much y changes per unit change in x)
It is the angle through which the line gets created in the graph.

Example:

Salary (y) = 3,00,000 + 1,00,000x

Here, b0 = 3,00,000 and b1 = 1,00,000

Experience (Years)	Salary (Rupees in Lakhs)
0	3
1	4
2	5
3	6
4	7
5	8
6	9
7	10
8	11
9	12
10	13

---

# Simple and Multiple Linear Regression

Simple linear regression
Single independent variable (x)
y ̂=b_0+b_1x 
Example: Year of Experience -> Salary
Multiple linear regression: 
Multiple independent variables (x1, x2, …)
y ̂=b_0+b_1x1+b2x2+ …+bnxn
Example: Years of Experience, Education, Skills -> Salary

---

# Least Squared Error

Suppose our line satisfies the equation y = 10 + 0.5x

x	y (Actual)	y (Line)	Error	Squared Error
10	10	15	5	25
20	25	20	-5	25
30	20	25	5	25
35	30	27.5	-2.5	6.25
40	40	30	-10	100
50	15	35	20	400
60	40	40	0	0
65	30	42.5	12.5	156.25
70	50	45	-5	25
80	40	50	10	100
Sum of Squared Error (SSE)	862.5

![image](https://github.com/user-attachments/assets/c0422dde-ce15-42e8-8936-1715256e4259)
![image](https://github.com/user-attachments/assets/6d004808-7357-4373-8e3c-0da281b0fb8c)

Repeat this process with different lines and calculate Sum of Squared Error (SSE)
Line of best fit = Line where we get the smallest SSE
Problem: We cannot do this ourselves
Solution: Use machine learning

---

Interpreting Results(Formulae: Next Slide)

R-squared (R2)
A percentage that tells us how much of the variance in data is explained by our model
Example: R-squared = 90.27% for an example where we predict a person’s weight based on the height means that this much of variance is covered by our model
The higher the better (Calculation on the next slide)
Mean Absolute Error (MAE)
By how many units is the model prediction different from the actual values
Lower the better
Mean Squared Error (MSE)
Amplifies outliers, does not tell use about the direction of the errors because of squaring
Lower the better
Root Mean Squared Error (RMSE)
Square root of MSE, so it is in the unit of the target variable – Easier to interpret
Lower the better

MAE: Is not impacted by large outliers

RMSE: Is impacted by large outliers (Since it is based on MSE, which is impacted by large outliers)

These three explain how well the model predicts, not how it explains variance

---

R-Squared Calculation

R2 = 1 − SSE/TSS 
SSE = Sum of Squared Error (Total distance between predicted and actual values, squared) 
       = ∑_i▒(yi −predictioni)2
TSS = Total Sum of Squares (Total distance between each y value and the mean , squared) = ∑_i▒(yi − y ̅)2

x	y	prediction	(y – predicted)2	ẏ	(y -ẏ)2
10	10	16	36	30	400
20	25	20	25	30	25
30	20	24	16	30	100
35	30	26	16	30	0
40	40	28	144	30	100
50	15	32	289	30	225
60	40	36	16	30	100
65	30	38	64	30	0
70	50	40	100	30	400
80	40	44	16	30	100

Total	NA	NA	722	NA	1450

R2 = 1 − SSE/TSS  
        = 1 − 722/1450  = 0.502
---

Evaluation Metrics for Linear Regression

What do all these values indicate?
What to use when?

Mean Absolute Error (MAE)
Mean of the absolute value of errors
Average error, Easiest to understand
Formula: 1/n∑_i ̇=1^n▒|y_i−y ̂_i|

Mean Squared Error (MSE)
Square each difference first, then add all squares of differences
More popular, as it punishes large errors
Formula: 1/n∑_i ̇=1^n▒(y_i−y ̂_i)2

Root Mean Squared Error (RMSE) = √MSE
Square root of mean of the squared errors
Most popular, because it is interpretable in y units
Formula: √1/n∑_i=1^n▒(y_i−y ̂_i)^2

All these are called Loss functions, because we want to minimize them

In height-weight example:

R-squared: 90 … Good

MAE: 8 pounds
MSE: 101
RMSE: 10 pounds

(Average weight in the dataset is 161 pounds, so RMSE is 6% of the average, which is good)

---

Linear Regression: Python Implementations

LinearRegression()	OLS()
Part of scikit-learn	Part of statsmodels
Mainly used for machine learning tasks	Mainly used for statistical analysis
Focus on predictive modelling	Focus on understanding relationships between variables
Less focus on statistical details	Provides detailed statistics
Includes intercept by default	Need to add intercept using sm.add_constant()
Focus on metrics such as MSE, R2 etc	Focus on coefficients, t-statistics (e.g. is there a linear relationship between a feature and the predicted variable?), p-value, CI*

---

Scaling and Encoding

Predictive analytics: Use one or more features (e.g. Years of experience) to predict a label (Salary)
Problem: Labels on different scale (age and income) or of categorical types (e.g. gender)
Solution: Scaling and Encoding
Scaling: Converting numeric features to a common scale
Example: Age (0-100) and income ($0-$1 million)
Encoding: Converting categorical variables to a numeric scale
Example: Gender values of Male and Female

---

Scaling: Bring Numeric Data on a Common Scale

Scaling: Putting all the features on the same ruler/scale

![image](https://github.com/user-attachments/assets/f58b6dc3-34bc-4f5e-9b69-cad21e962316)

Standardization/Normalization: Subtracts the mean and divides by the standard deviation
Min-max scaling: Scales to a specific range based on the minimum and maximum values

---

Standardized Scaling (Normalized Scaling)

Age	Income	Age Scaled = (𝑨𝒈𝒆 −𝑨𝒈𝒆 𝑴𝒆𝒂𝒏)𝑨𝒈𝒆 𝑺𝑫	Income Scaled = (𝑰𝒏𝒄𝒐𝒎𝒆 −𝑰𝒏𝒄𝒐𝒎𝒆 𝑴𝒆𝒂𝒏)𝑰𝒏𝒄𝒐𝒎𝒆 𝑺𝑫

25	35,000	-1.22	-1.08
40	50,000	-0.26	-0.43
55	70,000	0.70	0.43
68	1,00,000	1.54	1.73
32	45,000	-0.77	-0.65
Mean: 44	60,000		
SD: 15.61	23,128.91		

---

Min-Max Scaling

Because we use range also, it is called min-max (both get used)

Age	Income	Age 
– 
Minimum Age	Income 
– 
Minimum Income	Age Normalized = (𝐀𝐠𝐞 −𝐌𝐢𝐧𝐢𝐦𝐮𝐦 𝐀𝐠𝐞)𝑨𝒈𝒆 𝑹𝒂𝒏𝒈𝒆	Income Normalized = (𝐈𝐧𝐜𝐨𝐦𝐞 −𝐌𝐢𝐧𝐢𝐦𝐮𝐦 𝐈𝐧𝐜𝐨𝐦𝐞)𝐈𝐧𝐜𝐨𝐦𝐞 𝑹𝒂𝒏𝒈𝒆
25	35,000	0	0	0	0
40	50,000	15	15,000	0.34	0.23
55	70,000	30	35,000	0.69	0.53
68	1,00,000	43	65,000	1	1
32	45,000	7	10,000	0.16	0.15
Minimum: 25	35,000				
Range: 
68 - 25 = 43	1,00,000 – 35,000 = 65,000

---

Working with Non-Numeric Features – Encoding

Encoding: Transform categorical data into a numeric form (e.g. Passenger Class: Business, has 20% travellers, Economy Plus, has 30% travellers, Economy, has 50% travellers)

![image](https://github.com/user-attachments/assets/a9450c3e-4c84-4a0d-88e2-1227f1531667)

One-Hot Encoding: Business = 100, Economy Plus = 010, Economy = 001
Label Encoding: Business = 0, Economy Plus = 1, Economy = 2
Frequency encoding: Business = 0.20, Economy Plus = 0.30, Economy = 0.50

---

One-Hot Encoding: Columns

One-Hot encoding adds a column per category
Example: Dataset before and after One-Hot encoding

Computer	OS
PC-01	Windows
PC-02	Linux
PC-03	Linux
PC-04	Linux
PC-05	Windows
PC-06	Mac

Computer	OHE (Windows)	OHE (Linux)	OHE (Mac)
PC-01	1	0	0
PC-02	0	1	0
PC-03	0	1	0
PC-04	0	1	0
PC-05	1	0	0
PC-06	0	0	1

---

Logistic Regression

Logistic regression: Classification technique to predict the probability of a binary (true/false) outcome
Forms an S-shaped curve between 0 and 1

![image](https://github.com/user-attachments/assets/1df7d4fe-d4ea-4ea3-b60e-14e48a6cded7)

Because the middle line looks like a regression line, the term "regression" is used... But note that logistic regression does not have a single straightish line unlike linear regression ... Instead, it has three lines...
Logistic Regression is a type of Neural Network

LOGISTIC REGRESSION LOGIC

z = w0 + w1x1 + w2x2 + ... + wnxn = WTx
x = Input vector (features such as Glucose, Insulin, etc)
w = weight vector (learned during training)
z = logit (Raw prediction score)
z is converted into a probability: y = sigmoid(z) = 1 / (1 + e**z)
If sigma(z) >= 0.5, predict 1 (positive class) else predict 0 (negative class)

---

Confusion Matrix

Test to check if patients have a disease (H0: Patient does not have a disease)

n = 165	Predicted: NO	Predicted: YES
Actual: NO	TN = 50	FP = 10 (Type I Error)
Actual: YES	FN = 5 (Type II Error)	TP = 100!

True Positive (TP) 		Prediction: Disease 		Reality: Disease
True Negative (TN) 	Prediction: No Disease 	Reality: No Disease
False Positive (FP) 	Prediction: Disease 		Reality: No Disease
False Negative (FP) 	Prediction: No Disease 	Reality: Disease

---

Confusion Matrix - Exercise

Out of 1000 emails, 800 non-spams were classified correctly, 20 were incorrectly classified as spam, 40 were incorrectly classified as non-spam, and the remaining spams were identified correctly
Write the null hypothesis and create a confusion matrix 

Out of 1000 emails, 800 non-spams were classified correctly, 20 were incorrectly classified as spam, 40 were incorrectly classified as non-spam, and the remaining spams were identified correctly
Write the null hypothesis and create a confusion matrix 
H0: Email is not spam

n = 1000	Predicted: NO	Predicted: YES
Actual: NO	TN = 800	FP = 20 (Type I Error)
Actual: YES	FN = 40 (Type II Error)	TP = 140

---

Metrics Derived from Confusion Matrix

Accuracy: Overall correctness of the model's predictions
Precision (Positive Predictive Value): Accuracy of positive predictions
Recall (Sensitivity or True Positive Rate): Ability of the model to identify all positive instances
Specificity (True Negative Rate): Ability of the model to identify all negative instances
F1 Score: Harmonic mean of precision and recall and provides a balance between the two metrics

---

Metrics for Our Example

Accuracy =TP+TN/Total = 140+800/1000=940/1000 = 0.94 = 94%
Precision =TP/TP+ FP = 140/140+20=140/160 = 0.875 = 87.5%
Recall=TP/TP+FN = 140/140+40=140/180 = 0.77 = 77%
Specificity=TN/TN+FP = 800/800+20=800/820 = 0.97 = 97%
F1 Score =2 x (Precision x Recall)/Precision+Recall = 2 x (0.875 x 0.77)/0.875+0.77= 0.81 = 81%

---
