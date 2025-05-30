Bayes Theorem and Naïve Bayes Classifier

Bayes’ Theorem: How to update probabilities when new evidence becomes available
P(A│B)= P(B│A)x P(A)/P(B) 
Example: For titanic dataset, find those who survived given that the were female and their passenger class was 3
P(survived│pclas=3, gender=female)=

      P(pclas=3, gender=female│survived)x P(survived)/P((pclas=3, gender=female│survived)) 

Naive Bayes: Implement Bayes’ theorem to solve classification problems
Naive because it assumes that all the features are independent

---

Normal calculations
    Let x = Our ase(i.e., N = 1, S = 0, W = 1) ... We want to calculate its probability
    Then P(x|Purchase = 1) = P(N=1 | 1) *  P(S= 0 | 1) * P (W = 1 | 1) * P(1)
    P(x|Purchase = 1) = 3 / 5 * 0 * 2/5 * 1/2 = 0
    Because of one 0, the whole probability is becoming 0, which is wrong.

Laplace smoothing: Adjust the formula slightly ...
    P(S = 0|1) = count + 1 / (total in class + k), count = number of occurrences of this class, k = number of possible           values this class can take... so...
    P(S = 0|1) = 0+1 / 5+2 = 1/7 ... Applying it to the other two cases...
    P(N = 1|1) = 4/7 and P(W=1|1) = 3/7

Revised answer: P(x|Purchase = 1) = 4/7 * 1/7 * 3/7 * 5/10 = 0.0175

Naïve Bayes – Customer Example

Id	Newsletter Subscriber?	Social Media Follower?	Visited Website?	Purchase?
1	0	1	0	1
2	1	0	1	0
3	1	1	0	1
4	0	0	0	0
5	1	0	0	0
6	1	1	1	1
7	1	0	1	0
8	0	1	1	1
9	1	0	1	1
10	1	1	0	0
11	0	1	1	?

### **Text and Tables:**

#### **Purchase**
|   | 1 | 0 |
|---|---|---|
| 1 | 3 | 4 |
| 0 | 2 | 1 |

#### **Newsletter**
|   | 1 | 0 |
|---|---|---|
| 1 | 3 | 4 |
| 0 | 2 | 1 |

#### **Social Media**
|   | 1 | 0 |
|---|---|---|
| 1 | 4 | 1 |
| 0 | 1 | 4 |

#### **Website**
|   | 1 | 0 |
|---|---|---|
| 1 | 3 | 2 |
| 0 | 2 | 3 |

### **Conditional probabilities**
- **P(News | Purchase)** = \( \frac{3}{5} \) = **60%**
- **P(No News | Purchase)** = \( \frac{2}{5} \) = **40%**
- **P(News | No Purchase)** = \( \frac{4}{5} \) = **80%**
- **P(No News | No Purchase)** = \( \frac{1}{5} \) = **20%**

Similarly, probabilities for **Social Media** and **Website** follow the same conditional logic.

### **Overall**
50% - 50%

---

P (News | Purchase)	60%
P (No News | Purchase)	40%
P (Social | Purchase)	80%
P (No Social | Purchase)	20%
P (Website | Purchase)	60%
P (No Website | Purchase)	40%
P (News | No Purchase)	80%
P (No News | No Purchase)	20%
P (Social | No Purchase)	20%
P (No Social| No Purchase)	80%
P (Website | No Purchase)	40%
P (No Website| No Purchase)	60%
P (Purchase)	50%
P (No Purchase)	50%

**Text:**
Predict for:

For these, we need to find:

**Table:**
| Newsletter Subscriber? | Social Media Follower? | Visited Website? |
|------------------------|------------------------|------------------|
| 0                      | 1                      | 1                |

**Probability Calculation:**
- **Given Purchase = 1**
  - P (No News | Purchase) × P (SM | Purchase) × P (Website | Purchase) × P (Purchase)  
  - 40% × 80% × 60% × 50% = **9.60%**
  
- **Given Purchase = 0**
  - P (No News | No Purchase) × P (SM | No Purchase) × P (Website | No Purchase) × P (No Purchase)  
  - 20% × 20% × 40% × 50% = **0.80%**

**Overall Purchase Probability:**
9.6% / (9.6% + 0.8%) = **92.3%** = PURCHASE

---

We have calculated P(x|Purchase = 1) = 0.0175
Now calculate P(x|Purchase = 0)
P(x|Purchase = 0) = P(N=1|0) * P(S=0|0) * P(W = 1|0) * P(0)
Conditional probabilities
    For Purchase = 0 (i.e., Given that purchase = 0)
        Count(Newsletter = 1) = 3    P(N = 1) = 3/5
        Count(Social media = 0) = 5    P(S = 1) = 5/5
        Count(Website visit = 1) = 3    P(W = 1) = 3/5
        Applying Laplace Smoothing, these will become 4/7, 6/7, and 4/7 respectively.

P(x|Purchase = 0) = 47 * 6/7 * 5/10 = 0.1399
So, P(x|Purchase = 1)
Conclusion: For N = 1, S = 0, W = 1 ... prediction is purchase = 0

---

Naïve Bayes Types

Gaussian Naive Bayes: Gaussian (normal) distribution (Example: Height, Weight, etc); less effective with categorical data, Normally distributed numerical data
Multinomial Naive Bayes: Suitable for discrete data, often used in text classification with word frequency calculation
Bernoulli Naive Bayes: Designed for binary/boolean features, useful for text classification with binary attributes
Complement Naive Bayes: For imbalanced datasets
Text Classification: Text classification tasks such as spam detection, sentiment analysis, and document categorization

---

Ambiguity

Ambiguity Examples

Question: What is the difference betweeen in-laws and outlaws?
Answer: Outlaws are wanted ... Ambiguity of wanted
Wanted could mean by the police, we wanting it, etc.

Question: Why should one never date a tennis player?
Answer: Love means nothing to them ... Ambiguity of love and nothing
Love = 0 in tennis

---

More on Ambiguity ...

Dependency ambiguity: Structural ambiguity can lead to this
Example: Maharashtra reports increased COVID-19 cases (TOI report)
Maharashtra reports    increased COVID-19 cases
Maharashtra reports increased    COVID-19 cases

Pragmatic ambiguity: Most complex
Example:
    Passenger: Thank you for sending me to Delhi and my luggage to Mumbai
    Passenger: Brilliant Service!
    Chatbot: Thank you for the appreciation

---

Decision Tree:

A flowchart for classification and regression (Hence: Classification And Regression Tree - CART)
Type of supervised machine learning

Supervised Machine Learning: We provide class labels
Unsupervised learning: Ask the model to group similar data / find patterns. We do not provide class labels.
Example: Predict customer churn
    How easy or difficult is it? (Is original data giving any clues?)
    Do we need to do anything further? (Would splitting on a feature help?)

Sample Data:

Transaction Id    Account type    Balance    Transaction    Fraud
1    savings    8000    deposit    No
2    current    4000    deposit    No
3    savings    3800    withdraw    Yes
4    savings    4900    deposit    Yes
5    current    50000    withdraw    Yes

![image](https://github.com/user-attachments/assets/a1d05deb-14a6-4123-804f-096369c41763)

Looking at the data and decision tree logic, transactions are classified as fraudulent based on the account type, balance, and transaction type.

1. **Transaction ID 1** (savings, balance = 8000, deposit) → Savings account with balance > 5000 → **Fraud = No**
2. **Transaction ID 2** (current, balance = 4000, deposit) → Current account with a deposit → **Fraud = No**
3. **Transaction ID 3** (savings, balance = 3800, withdraw) → Savings account with balance ≤ 5000 → **Fraud = Yes**
4. **Transaction ID 4** (savings, balance = 4900, deposit) → Savings account with balance ≤ 5000 → **Fraud = Yes**
5. **Transaction ID 5** (current, balance = 50000, withdraw) → Current account with a withdrawal → **Fraud = Yes**

---

Entropy

Entropy is the state of randomness

Entropy: Tells us how homogeneous a dataset is

High entropy: Less homogeneous = High variability

![image](https://github.com/user-attachments/assets/10ec2954-2f65-41c6-b2ed-77d391fab4a3)

Low entropy: More homogeneous = Low variability

![image](https://github.com/user-attachments/assets/e489827b-eba9-48be-99ed-4c1e888c95c7)

---

Consider two data sets:
D1: [A, B, C, D, E, F, G, H] -> Not at all homogeneous -> 8 classes -> Entropy = 3
D2: [A, A, A, A, B, B, B, B] -> Partially homogeneous -> 2 classes -> Entropy = 1
Entropy=−Ʃpi.log2(pi) for i=1 to n

log2(pi) This can be 0 or negative

n=number of classes in data, p = proportion of data points belonging to that class
Entropy(D1) = -[(1/8 x log2 (1/8) + (1/8 x log2 (1/8) …] 8 times 
                       = -[(1/8 x -3) + (1/8 x -3) …] 8 times
                       = -[-3/8          + -3/8          …] 8 times = -[-24/8 ] = 3
Entropy(D2) = -[(1/2 x log2 (1/2) + (1/2 x log2 (1/2)]
                       = -[(1/2 x -1)             + (1/2 x -1)]  = -[-1/2 – 1/2] = -[-2/2]
                       = 1

Exercise

We have data about some students. Decide the branching/split by calculating entropy and information gain.

Theory Study	Lab Study	Pass Exam
High	High	Yes
High	Medium	Yes
High	Medium	Yes
High	Low	Yes
Medium	High	Yes
Medium	Medium	No
Medium	Medium	Yes
Medium	Low	No
Low	Low	No

Overall entropy = 6/9 log2 6/9 + 3/9 log2 3/9 = 0.91
Splitting on Theory study
E(High) = 4/4 log2 4/4 + 0/4 log2 0/4 = 0
E(Medium) = 2/4 log2 2/4 + 2/4 log2 2/4 = 1
E(Low) = 0/1 log2 0/1 + 1/1 log2 1/1 = 0
Splitting on Lab study
E(High) = 2/2 log2 2/2 + 0/0 log2 0/0 = 0
E(Medium) = 3/4 log2 3/4 + 1/4 log2 1/4 = 0.81
E(Low) = 1/3 log2 1/3 + 2/3 log2 2/3 = 0.91

Weighted average of E(Theory Study) =
 4/9 x 0 + 4/9 x 1 + 1/9 x 0 = 0.444
Information gain = 0.91 – 0.444 = 0.47

Weighted average of E(Lab Study) =
 2/9 x 0 + 4/9 x 0.81 + 3/9 x 0.91 = 0.66
Information gain = 0.91 – 0.444 = 0.24

---

Decison Tree Calculation: Titanic

Original data: Total count: 891, survived = 0, count = 549, survived = 1, count: 342
Entropy (Original) = 0.96

Suppose we split on gender (male records: 577, female records: 314)
Count of gender = male, survived = 0 ... 468
Count of gender = male, survived = 1 ... 109
Count of gender = female, survived = 0 ... 81
Count of gender = female, survived = 1 ... 233
Entropy (gender = male) = 0.69
Entropy (gender = female) = 0.82
Weighted average of Entropy (gender) = 0.73
Informaton Gain (IG): Original entropy - Gender entropy = 0.95 - 0.73 = 0.23

---

Suppose we split on pclass (pclass 1 records: 216, pclass 2 records: 184, pclass 3 records: 491)
Count of pclass = 1, survived = 0 ... 80
Count of pclass = 1, survived = 1 ... 136
Count of pclass = 2, survived = 0 ... 97
Count of pclass = 2, survived = 1 ... 87
Count of pclass = 3, survived = 0 ... 372
Count of pclass = 3, survived = 1 ... 119

Entropy(pclass = 1) = 0.95
Entropy(pclass = 2) = 0.99
Entropy(pclass = 3) = 0.79

Weighted average of Entropy (gender) = 0.87
Information Gain (IG) = Original entropy - Gender entropy = 0.96 - 0.87 = 0.09
Conclusion: Split on gender is better
---

Exercise

You are a loan officer and decide whether to approve/reject a loan application based on two attributes
Income level (Categorical): High/Medium/Low
Credit history (Categorical): Good/Bad
Target variable
Loan approval (Approve/Reject)
Sample data
Calculate entropy
Initial
After split on income level
After split on credit history

Income level	Credit history	Loan approval
High	Good	Approve
Medium	Good	Approve
Low	Good	Approve
High	Bad	Approve
Medium	Bad	Reject
Low	Bad	Reject

Solution

Overall entropy
E(Original) = 4/6 log2 4/6 + 2/6 log2 2/6
E(Original) = 0.918
Splitting on Income level
E(High) = 2/2 log2 2/2 + 0/2 log2 0/2 = 0
E(Medium) = 1/2 log2 1/2 + 1/2 log2 0/2 = 1
E(Low) = 1/2 log2 1/2 + 1/2 log2 0/2 = 1
Splitting on Credit history
E(Good) = 3/3 log2 3/3 + 0/3 log2 0/3 = 0
E(Bad) = 1/3 log2 1/3 + 2/3 log2 2/3 = 0.918

Weighted average of E(Income level) =
 2/6 x 0 + 2/6 x 1 + 2/6 x 1 = 0.667
Information gain = 0.918 – 0.667 = 0.251

Weighted average of E(Credit history) =
 3/6 x 0 + 3/6 x 0.918
Information gain = 0.918 – 0.459 = 0.459

Decision: Split on Credit history first

After splitting on Credit history
For Good: All outcomes are Approve, so entropy = 0
For Bad: Calculate entropy and information gain by splitting on Income level
Income level = High: Approve = 1, Reject = 0, so entropy = 0
Income level = Medium: Approve = 0, Reject = 1, so entropy = 0
Income level = Low: Approve = 0, Reject = 1, so entropy = 0
Since all the subsets have 0 entropy, no further splitting is necessary

![image](https://github.com/user-attachments/assets/9298f473-55be-4398-9e73-1d0d7fcf63bd)

Decision Tree:

If Credit History is Good:
    Approve

Else If Credit History is Bad:
    If Income Level is High:
        Approve
    Else If Income Level is Medium:
        Reject
    Else If Income Level is Low:
        Reject

---

Deciding the Split

Entropy: Evenness between classes
High entropy: Not good for prediction (e.g. split on Gender)
Low entropy: Good for prediction (e.g. split on Last login)
Information Gain = Entropy before the split - Entropy after the split

---

Gini Index/Coefficient/Impurity

Gini impurity Alternative to entropy (Lower the better, 0 is the best)
Example: Predict fruit: A or B

P(A) = 10/20 = 0.5
P(B) = 10/20 = 0.5


![image](https://github.com/user-attachments/assets/cb013df0-1eca-4ede-a22c-46cc0d772d8d)

Entropy=−Ʃpi.log2(pi) for i=1 to n
Entropy=-[(-0.5 x log2(0.5))+(−0.5 x log2(0.5))]
Entropy= -(-0.5 x -1 + -0.5 x -1)
Entropy= -(-0.5 + -0.5) = 1

Gini impurity=1 −[P(A)2+P(B)2]
Gini impurity=1 −[(0.5)2+(0.5)2]
Gini impurity=1 −[0.25+0.25]
Gini impurity=0.5

---

When We Have More Classes

Consider we have three classes with probabilities of 0.4, 0.4, and 0.2 respectively
Gini impurity = 1 - (p1^2 + p2^2 + p3^2)
Gini impurity = 1 - (0.4^2 + 0.4^2 + 0.2^2)
Gini impurity = 1 - (0.16 + 0.16 + 0.04)
Gini impurity = 1 - 0.36
Gini impurity = 0.64

Conclusion: More classes, higher Gini impurity
