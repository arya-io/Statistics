# Two Tailed and One-Tailed Tests

Rejection region is on both sides
Tail is on both sides
Tail is nothing but area of rejection and alpha
We don't use alpha but alpha/2 on both sides. We don't use entire alpha.

Null Hypothesis: equal to sign
Alternate Hypothesis: Not equal to sign

Two Tailed test: equal to sign
One Tailed Test: Greater than or equal to sign and less than or equal to sign

---

We can write H0 and H1 in three ways:

H0    H1    Type of Test
=    !=    Two-tailed test
<=    >    One-tailed test
>=    <    One-tailed test

Two-tailed test
    H0: A battery company claims its batteries last 20 hours on average (mu = 20)
    H1: The battery does not last for 20 hours on average (mu != 20)

One-tailed test:
    H0: A company claims its new medicine reduces fever duration from 16 weeks (mu >= 16)
    H1: The fever duration is significantly less than 16 (mu < 16)
    
Two-Tailed Tests:

Null and alternate hypothesis use = and != symbols
We are not predicting any direction between the variables
We are not saying one is greater or lesser than the other
We are just saying that they are different from each other
Conclusion: The difference could be in either direction (< or >)
So, rejection region would be in each tail of the distribution
Hence the name two-tailed - Regions of rejection in each tail
Reject H0 if test statistic < z-critical (at alpha/2) or test statistic > z-critical (at alpha/2)

If the statement contains reduces, it is definite one tailed test
If the statement contains changes, it is two tailed test

When rejection is present on only one side, then no need to divide alpha by 2.
alpha is the rejection zone 

Two-tailed test: Rejection zone at both sides
One-tailed test: Rejection zone only in one side
Example: A new medicine is being tested with current lifespan = 70 years
Two-tailed Test
H0: Lifespan = 70
H1: Lifespan ≠ 70
One-tailed Test
H0: Lifespan = 70
H1: Lifespan > 70

---

Two-tailed Test
H0: The average weight of chips in a packet is equal to 50 grams (μ = 50)
Ha: The average weight of chips in a packet is not equal to 50 grams (μ ≠ 50)
Rejection zone: Both to the left and to the right of 50

One-Tailed Test (Left-Tailed)
H₀: The average weight of chips in a packet is equal to or greater than 50 grams (μ ≥ 50)
Ha: The average weight of chips in a packet is less than 50 grams (μ < 50)
Rejection zone: Towards the left side of 50
One-Tailed Test (Right-Tailed):
H₀: The average weight of chips in a packet is equal to or less than 50 grams (μ ≤ 50)
Ha: The average weight of chips in a packet is greater than 50 grams (μ > 50)
Rejection zone: Towards the right side of 50

---

![image](https://github.com/user-attachments/assets/6590ae45-931d-4425-a5e9-527134bec511)

![image](https://github.com/user-attachments/assets/4d000a65-448d-4d15-bde8-3449e895a3dc)

![image](https://github.com/user-attachments/assets/c059ecd1-00d5-470e-b726-15ca9c3ed405)

---

One Tailed Tests

Null Hypothesis uses <= or >= symbol
Rejection region would be concentrated in only one tail of the distribution
Hence the name one-tailed - Region of rejection is in one tail only
Two types: Left-tailed test and Right tailed test

---

LEFT TAILED TEST (Rejection on the Left):
H0: The medicine does not reduce fever duration - it is 16 weeks or more
H0: mu >= 16, H1: mu < 16
Left-tailed test: Tail (Rejection zone) is only on the left.. Why?
    If test statistic (i.e., z-score of our sample) >= 16, it means medicine is not showing effect, which matches with our null hypothesis, so do not reject H0
    But if test statistic is significantly < 16, medicine is effective, so reject H0
    If test statistic is significantly < 16, its z-score must be negative... why?
    Z = x(mean) - mu / s / root(n)... This would be negative if x(mean) < mu
    So, reject H0 if test-statistic < z-critical (at alpha)

RIGHT TAILED TEST (Rejection on the Right):
H0: A battery manufacturer claims that a battery which used run for 30 hours now runs for more than 30 hours due to new technology
H0: mu <= 30, H1: mu > 30
Left-tailed test: Tail (Rejection zone) is only on the right... Why?
    If test statistic (i.e., z-socre of our sample) <= 30, it means new battery technology is not showing effect, which matches with our null hypothesis, so do not reject H0.
    But if test statistic is significantly > 30, new technology is effective, so reject H0
    If test statistic is significantly > 30, its z-score must be positive ... why?
    Z = x(mean) - mu / s / square root of n... This would be positive if x(mean) > mu

    So, reject H0, if test statistic > z-critical (at alpha)
---

The possibility of a student getting placed before doing a C-DAC course is 40%.
Write null and alternate hypothesis for:
Also identify where would be the rejection zones and alpha values.

1. A two-tailed test
   H0: Placement possibility = 40% (mu = 40%)
   H1: Placement possiblity != 40% (mu != 40%)
   Rejection regions: 2, Each containing: alpha / 2 in each
   
2. A left-tailed test
   H0: Placement possibility >= 40% (mu >= 40%)
   H1: Placement possibility < 40% (mu < 40%)
   Rejection region: 1, alpha in the left/lower
   
3. A right-tailed test
   H0: Placement possibility <= 40% (mu <= 40%)
   H1: Placement possibility > 40% (mu > 40%)
   Rejection region: 1, alpha in the right side

---

Two-Tailed and One-Tailed Tests: Impact on Alpha

Two-tailed tests: Two rejection regions
    alpha (Rejection Region) is split equally into lower tail and upper tail
    So, if alpha = 0.05, we have alpha = 0.025 in the lower tail and alpha = 0.025 in the upper tail
    So, split alpha into two
One-tailed tests: Only one rejection region
    alpha (Region region) is only in one tail (depending on whether we are using left-tailed test or right-tailed test)
    So, if alpha = 0.05, we have entire alpha = 0.05 in only one of the tails
    So, do not split alpha into two

---

Two-Tailed Tests: p-Value

First calculate z-test statistic (could be positive or negative)
Look up in the z-table to get area under the probability distribution to the left of the z-value.
Example: z-test statistic = 1.23 in z-table, we get 0.8907
But for positive z-score, we are interested in the area to the right of z-value, not to the area to the left
To find area to the right, we calculate 1-0.8907 = 0.1903
But because this is a two-tailed test, the rejection area is not only to the right, but also to the left
So, we double 0.1093 = 2 * 0.1903 = 0.2186 = p-value
Reject H0 if p_value <= alpha

---

One-Tailed Tests (Left-Tailed): p-Value

First calculate z-test statistic (would be negative for a left-tailed test and positive for a Right-Tailed test)
Look up in the z-table to get area under the probability distribution to the left of the z-value.
Example: z-test statistic = 1.46 in z-table, we get 0.9279
But for positive z-score, we are interested in the area to the right of z-value, not to the area to the left
To find area to the right, we calculate 1-0.9279 = 0.0721 = p-value
No need to double, since the entire area of rejection is on the right
Reject H0 if p_value <= alpha

---

Rejection/Non-Rejection Criteria

Test Type	α 	p-value
Two-tailed	Consider α/2 to find critical value	Compare p-value with α/2
One-tailed	Consider α to find critical value	Compare p-value with α

Test Type	Condition	Decision
Two-tailed	|Test-statistic| >   |Critical Value|
|Test-statistic| <= |Critical Value|	Reject H0
Do not reject H0
Left-tailed	Test-statistic <   Critical value
Test-statistic >= Critical value	Reject H0
Do not reject H0
Right-tailed	Test-statistic >   Critical value
Test-statistic <= Critical value	Reject H0
Do not reject H0

---

Calculate Test Statistic

Suppose to test our earlier H0: Sample size = 50, Sample average (x̄) = 67 inches, SD (σ) = 5 inches
Z= x̄ − μ/s/√n  = 67 −65/5/√50=  2.82
Alpha = 0.05, but since this is a two-tailed test, we need to consider alpha / 2 = 0.05 = 0.025
See in Z-table (https://www.z-table.com/) the probability value of 0.025 to get the critical value (i.e. expected z-score as per normal distribution) … See next slide
Critical value = 1.96 (i.e. Up to ±1.96 of Z-score, we would not reject H0)
Since our calculated test statistic > critical value, we reject H0

---

P-value Calculation Example

We have Z-Score = 2.82 for a two-tailed test 

![image](https://github.com/user-attachments/assets/383a1326-bffa-4ec5-bc04-e69c292ad8df)

For Z-Score = 2.82, using Z-table, area under the curve = 0.9976

So, area to the right of Z = 2.82 = 1 - 0.9976 = 0.0024

Because it is a two-tailed test, P-value = 2 x 0.0024 = 0.0048

Since P-value < α, we do not reject H0

---

P-value

P-value = Area of rejection
Low p-value: Reject H0, High p-value: Fail to reject H0
Example: A pizza outlet claims they deliver pizza in <= 30 minutes on average
H0: Mean delivery time = 30 minutes
Ha: Mean delivery time <> 30 minutes
We test a few sample delivery times and get a p-value = 0.001
Since 0.001 is much less than 0.05, we reject H0

---

Critical Values for Different Levels of α

α	Left-Tailed Test	Right-Tailed Test	Two-Tailed Test
0.1	-1.28	+1.28	-1.64 and + 1.64
0.05	-1.64	+1.64	-1.96 and + 1.96
0.01	-2.33	+2.33	-2.58 and + 2.58

---

norm.cdf: What we know = z-score, what we want to find = p-value
norm.ppf: What we know = p-value, what we want to find = z-score

How to decide?

1. If z-statistic (z-score that we have calculated) < z-critical (z-score for the given alpha from z-table)
    Do not reject H0
Else
    Reject H0

2. If p-value (of our Z-Score)    > alpha/2 OR
    If 2* p-value (of our Z-Score)    > alpha

---

# Margin of Error

H0: On a social networking site, a random sample of 40 users tells us that the average number of friends per user is 130.8 with a SD of 53
Point estimate (x ̅): 130.8 friends (Single value estimate for a population parameter)
Margin of error: Add a range of uncertainty around the point estimate (e.g. instead of I am reaching in 10 minutes, say 5-15 minutes)
Interval estimate: Point estimate + Margin of Error

Margin of Error = Zc x Standard Error
Zc is Z-Critical here.

As we know: Standard Error = s/√n 
Standard error is standard error of sample / root of no. of observations

So, Margin of Error = 1.96 x 53/√40 = 16.4
Then Interval estimate = 130.8 ± 16.4
Interval estimate = 114.4 < μ <147.2
Now we can use this in H0

![image](https://github.com/user-attachments/assets/633a2df1-97c3-42cd-b1d5-2fe056f23251)

---

# Null Hypothesis – How to State?

Test	Null Hypothesis
One-sample T-Test	There is no significant difference between the sample mean and the hypothesized population mean

Z test and T test are almost some
The only difference is when we have less sample data (data points) then use T Test, let say less than 30
When we have large data use Z Test, let say greater than 30

Two-sample T-Test	The population means of the two groups are equal 

Paired T-Test	The means before and after of the same group are equal
e.g., Checking blood sugar level before, and then checking once again.

ANOVA	The means of more than two groups are equal
When we have more than two groups

Chi-Square Test	There is no association between the two categorical variables (they are independent)

Here starts machine learning
these are machine learning
yet they are known as statistical tests
Linear regression	The coefficients of the independent variables are equal to zero (no relationship)
Logistic regression	There is no association between the independent variables and the binary outcome![image](https://github.com/user-attachments/assets/eec2f058-efaa-42a2-9afd-2c95c428c9d5)

---

t-tests

t-test: Also called student’s t-test
Determines if there is a significant difference between the means of two samples
Difference from Z-test: Here, the sample size is expected to be <= 30
Types

Type of the t-test	Purpose
One sample t-test	Compare the mean of a sample with that of the population
Independent sample t-test	Compare the mean of two different populations
Paired sample t-test	Compare the mean of the same group at different times

---

# One-sample test

Compare sample mean with hypothesized population mean
H0: Sample mean (x ̅) = Population mean (μ)
Formula: t=x ̅−μ/SE= x ̅−μ/s/√n = Sample mean −Population mean/Sample standard deviation/√Sample size

This is the same as Z-test formula, but it is expected that here, the sample size should be <= 30

---

# One-Sample T-test : Example

It is claimed that the average amount of coffee in a cup is 12 units. We collect a random sample of 20 cups and measure the amount of coffee in each cup. We found sample mean = 11.5 with a standard deviation of 1.2 units.
 t=x ̅−μ/s/√n =  11.5−12/1.2/√20=2.08 
Degrees of freedom = Sample size – 1 = 20 – 1 = 19

Degrees of freedom is nothing but no.of observations
Look in T-table (See next slide)

we have t table similar to z table

---

T-table: At https://www.sjsu.edu/faculty/gerstman/StatPrimer/t-table.pdf, look for DF 19 and two-tails value of 0.05
Why 0.05? Because confidence interval is 95%, so significance level (alpha) is 0.05 
Calculated t-statistic (2.08) < Critical t-value (2.093) 
Conclusion: Fail to reject the null hypothesis
Conclusion: We do not have enough evidence to conclude that the average amount of coffee in a medium-sized cup served by the company is different from 12 units

---

# Two Independent Samples T-Test

Compare the mean of two independent groups (i.e. Samples from two different populations)
H0: There is no significant difference between the means of the two groups
Formula: t= X̄1 −X̄2/√s12/n1 + s22/n2 
X̄1 and X̄2: Sample means
s1 and s2: Sample standard deviations
n1 and n2: Sample sizes

![image](https://github.com/user-attachments/assets/54ab485b-0ca5-44fc-b919-0d176d2126ba)

---

# Example:

Marks obtained by two groups of students:
Group A = [85,88,90,92,95,87,89,91,94,86,88,92,90,93,85,89,91,87,92,90,88,93,86,89,91]
Group B = [78,82,80,85,88,81,83,79,84,87,80,82,85,78,81,83,79,82,80,85,78,81,83,79,84,87,80,82,85,78]

X̄1 = Sample mean of Group A = 89.04
X̄2 = Sample mean of Group B = 81.87
s1 = Sample standard deviation of Group A = 2.64
s2 = Sample standard deviation of Group B = 2.06
n1 = Sample size of Group A = 25
n2 = Sample size of Group B = 30
Test t-statistic = 9.96 and DF = 43.77
Critical value (t-table): 1.67 for DF = 43 and alpha = 0.05
Since t-statistic > critical value, we reject H0

---

# Paired t-test

Data from the same sample is tested before and after some event
Different from Two independent samples t-test (Where data comes from two completely different groups)
Example: Test the blood sugar levels of same patients before and after administering a diabetes medicine for 6 months
H0: There is no significant difference between the means of the two groups
Formula: t= X̄diff/(Sdiff/√n)  = Sample mean of the differences/(Sample standard deviations of the differences/√Sample size) 

Sample 1	Sample 2	Difference
13	9	4
14	11	3
14	12	2
15	12	3
16	14	2
17	16	1
17	18	-1
18	18	0
19	18	1
20	19	1
22	20	2
23	20	3
Mean of differences	1.75
Standard deviation of differences	1.422

t= X̄diff/(Sdiff/√n)  = 1.75/(1.422/√12) 
=4.26

For α = 0.05 and DF = 11, critical value = 2.201

Since test statistic > critical value, we reject H0

---

# Analysis of Variance (ANOVA)

Are means of three or more groups different?
“One way”: Because we are comparing just one variable across categories
“Two way”: If we compare two variables across categories
Compare variation within each sample, relative to the variation between samples
H0 = All group means are equal
Formula: Quite complex (See next two slides)

---

# ANOVA Example

Test scores of students:
Teaching Method A: [85, 88, 91, 78, 82]
Teaching Method B: [75, 79, 80, 82, 78]
Teaching Method C: [90, 85, 88, 92, 87]
H0: There are no significant differences in the mean test scores among the three teaching methods
Ha: At least one teaching method has a different mean test score than the others
Mean of Method A: (85 + 88 + 91 + 78 + 82) / 5 = 84.8
Mean of Method B: (75 + 79 + 80 + 82 + 78) / 5 = 78.8
Mean of Method C: (90 + 85 + 88 + 92 + 87) / 5 = 88.4
Grand Mean: (84.8 + 78.8 + 88.4) / 3 = 84

SST = Sum of Squares Treatment, measures the variability of group means
SST = Σ (Nt * (Mean of Group t - Grand Mean)^2)
SST = (5 * (84.8 - 84)^2) + (5 * (78.8 - 84)^2) + (5 * (88.4 - 84)^2)
SST ≈ 133.2
SSE = Sum of Squares Error, measures the variability in the groups
SSE = Σ Σ (Xi - Mean of Group i)^2
SSE = (85-84.8)^2 + (88-84.8)^2 + (91-84.8)^2 + (78-78.8)^2 + (82-78.8)^2 + (75-78.8)^2 + (79-78.8)^2 + (80-78.8)^2 + (82-78.8)^2 + (78-78.8)^2 + (90-88.4)^2 + (85-88.4)^2 + (88-88.4)^2 + (92-88.4)^2 + (87-88.4)^2
SSE ≈ 50.8

F = (SST / (k - 1)) / (SSE / (N - k))
Where k is the number of groups (3 in this case) and N is the total number of observations (15).
F = (133.2 / 2) / (50.8 / 12)
F ≈ 8.88
Now go to F-table (https://users.sussex.ac.uk/~grahamh/RM1web/F-ratio%20table%202005.pdf), go to column 2, row 12 (See next slide)
Since calculated F-value (8.88) > critical statistic (3.89), we reject the null hypothesis

# ANOVA Example: Why column 2, row 14?

Total Degrees of Freedom (df_total): Total number of observations minus 1 = 15 - 1 = 14
Between-Groups Degrees of Freedom (df_between): Number of groups minus 1 = 3 - 1 = 2
Within-Groups Degrees of Freedom (df_within): Subtract df_between from df_total 14 - 2 = 12
We need to go to df_between column and df_within row, hence column 2 and row 12

---
