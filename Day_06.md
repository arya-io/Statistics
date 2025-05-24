Poisson Distribution

Binomial distribution: Perform n trials and determine success/failure
Poisson distribution: Considers the number of successes per unit of time (or another continuous unit, such as distance)
Example: On an average, we read 10 pages of a book in an hour – what are the chances of reading 8 pages in the next hour?
P(x) = λx e−λ/x!=108 e−10/8!=108 x 2. 718−10/8x7x6x5x4x3x2x1 = 0.113 or 11%

Note: e = 2.718, Euler's constant

In Binomial Distribution:
Success = x or k (out of)
Trials = n
Historical = p

In Poisson Distribution:
We are not interested in taking out number of trials.
Instead, we want to find in certain time interval.
We won't have 'n' here.

Success = x
Trials = Time Interval
Historical = λ

---

Example: Usually 15 cars pass a toll plaza every hour. We want to know the probability that 13 cars will pass through in the next hour.

P(x) = λx e−λ/x!=1513  2.718−15/13!=108 x 2. 718−10/8x7x6x5x4x3x2x1 = 0.0956 or 9.56%

---

# Binomial versus Poisson

ADD

---

# Poisson Distribution - Key Characteristics

ADD

---

Example: Usually 15 cars pass a toll plaza every hour. We want to know the probability that 13 cars will pass through in the next hour.

P(x) = λx e−λ/x!=1513  2.718−15/13!=108 x 2. 718−10/8x7x6x5x4x3x2x1 = 0.0956 or 9.56%

---

# Real life and Normal Distribution

Many real-life data points follow Normal Distribution:
People’s heights and weights
Population blood pressure
Test scores
Also called as Gaussian Distribution
Generally, less/non-natural phenomena do not have normal distributions, e.g. income of people

![image](https://github.com/user-attachments/assets/3b0e8688-973a-4fb8-b427-493d3a6f8163)

---

# Normal Distribution: Key Features

Symmetry: Perfect symmetry around the mean
Mean = Median = Mode = Center point of the normal distribution
Bell-shaped curve
Empirical rule: 
68% of the data falls within Mean ± 1 SD
95% of the data falls within Mean ± 2 SD
99.7% of the data falls within Mean ± 3 SD
Z-score (Standard score): Useful in finding relative position of an observation with respect to the overall population
It tells How far away are you from the mean?
![image](https://github.com/user-attachments/assets/eb79273e-f407-4249-8705-e942246f8f6e)

---

# Z-Score Interpretation

![image](https://github.com/user-attachments/assets/e633de4b-406d-4949-b6aa-8498ed86aa5c)

---

# Normal Distribution: Example

ADD

---

# Using Z-Score

ADD

---

# Z-Score Calculations

Z-Score (Standard Score): Describes how many standard deviations away a data point is from the mean

Z−Score= x − μ/σ

x: individual data value
μ: population mean
σ: population standard deviation

![image](https://github.com/user-attachments/assets/7c263f9a-af45-4fd7-8754-761e93bc8310)
![image](https://github.com/user-attachments/assets/2900bd23-9b18-4a1a-878b-6b7f3d9e4c07)

---

Z-Score: Problem

A runner participated in a 200m race and a 500m race
Consider the following, calculate Z-scores and determine where she did better

Race	Average time	Standard deviation	Runner’s time
200m	31s	1.5s	28s
500m	125s	8.2s	132s

Z= X − μ/σ=28 −31/1.5=−2
Z= X − μ/σ=132 −125/8.2.=0.854

---

The top Z Scores in each era in Cricket

--

# Visualizing Z - Scores

In this example, a lower time would be preferable when completing a race and so, the lower z-score would be better

In other examples, positive/higher Z-score will be better, e.g. marks obtained by a student – Because, here the student would want to be above average

![image](https://github.com/user-attachments/assets/effd7c84-0a59-4fd8-813a-b8a009facbde)

---

# Normal Distribution and Probability

Standard normal distribution = Normal distribution with mean of 0 and standard deviation of 1

![image](https://github.com/user-attachments/assets/5b0ccf67-cc1b-415f-932a-5259a5379c0c)

Total area under the curve = 1
Can be used to map Z-Score to probability of area under the curve (Next)

---

# Is our Data Normally Distributed?

Shapiro-Wilk Test: p-value should be > 0.05 (Data size <= 5000 rows) for more data, use Anderson test
QQ plot (Quantile-Quantile): Ideal is straight line

![image](https://github.com/user-attachments/assets/78e92282-c4fc-40af-895e-486a6c686436)

---

# The Central Limit Theorem (CLT)

Problem: Suppose population data does not follow normal distribution (i.e. it is left/right-skewed)
Population->Samples
Example: 10 lakh examination result of students->500 samples of 100 students each
For each sample, calculate average marks (Sample mean or x̄)
Plot these sample means on a graph
They will follow normal distribution: Central Limit Theorem (CLT)
Generally, minimum sample size = 30
How many such samples? No such number
Result: Consider original population also as normally distributed now

---

CLT

![image](https://github.com/user-attachments/assets/e696b9e6-487e-436c-82c1-8718e8ac87a4)

---

Hypothesis: Not possible to test entire population, so test sample and draw conclusions about the population (Inferential statistics)
Hypothesis testing: Lets us evaluate how well a sample supports an assumption about the population using these steps:
State our assumption (Null hypothesis and Alternate hypothesis)
Determine probability of making an error (Level of significance) called α
Check how well the data supports our assumption (Calculate Test statistic)
Translate that into a probability that supports it (p-value)
Conclusion: Is p-value < α?
Yes – Our assumption was wrong – Reject Null hypothesis
No – Our assumption was correct – Fail to reject Null hypothesis
Alternatively, compare test statistic with Critical value and decide
Sample statistic: x ̅ (Sample mean) -> Population parameter: μ (Population mean)

---

# Null And alternate Hypotheses

Null hypothesis: Neutral statement (status quo)
Alternate hypothesis: What we actually want to be true
Example: Suppose, the chances of a student getting placed before doing a C-DAC course are 40%
Null Hypothesis (H0): There is no change in the chances of placement for a student after completing a C-DAC course (μ = 40)
Null hypothesis will always have a <= or = or >= sign
Alternate Hypothesis (Ha or H1): There is a significant difference: Three options
If we are just interested in checking if there is a change: μ ≠ 40
If we are just interested in checking if there is a reduction in the chances: μ  < 40
If we are just interested in checking if there is an improvement in the chances: μ  > 40
Note: We never prove/accept a hypothesis; we either reject or do not reject a hypothesis
Why?

---

# Type I, II Errors, Alpha Beta

	H0 is True	H0 is False
Reject H0	Type I Error, Alpha	Correct
Do not Reject H0	Correct	Type II Error, Beta

Why can this happen? Bad sample data …
Example: We got a bad sample where Average sample score = 80
We would reject H0 because in our sample it seemed so, although in general it is true, considering all the other samples
Note: Try to reduce Type I errors => Try not to reject H0 (See table above)
But it automatically means a scope for increase in Type II errors (See table above)

---

# Type I and Type II Errors – Example

H0: John’s used car is safe to drive
Possibilities
John thinks that his car may be safe when in fact it is not safe - Error
John thinks that his car may be safe when in fact it is safe - Ok
John thinks that his car may not be safe when in fact it is not safe - Ok
John thinks that his car may be not be safe when in fact it is safe – Error
Which of these is Type I and which is Type II Error?

Remember:
Type I Error occurs when H0 is true
Type II Error occurs when H0 is false
In this example: H0: John’s used car is safe to drive
So:
(d) is Type I error
(a) is Type II error
Which error is more serious?
Type II

---

# Type I and Type II Errors – Another Example

In a criminal court case, H0: The defendant is innocent
Possibilities:  
The jury believes that the defendant is guilty when she is innocent - Error
The jury believes that the defendant is guilty when she is not innocent - Ok
The jury believes that the defendant is innocent when she is not innocent - Error
The jury believes that the defendant is innocent when she is innocent – Ok

What are Type I and Type II errors here, and which one is more dangerous?

Remember:
Type I Error occurs when H0 is true
Type II Error occurs when H0 is false
In this example: H0: Defendant is innocent
(c) Type II error
(a) Type I error
Which one is more serious?
Perhaps (c), but then someone can also argue it is (a), depending on the situation and the crime
