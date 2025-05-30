## 📚 Bayes’ Theorem & Naïve Bayes Classifier 🤖

---

### 🧪 **Bayes’ Theorem: Updating Probabilities with New Evidence**

Bayes' Theorem helps us **update our beliefs (probabilities)** when we get new data or evidence.

#### 🔁 Formula:

$$
P(A | B) = \frac{P(B | A) \times P(A)}{P(B)}
$$

👉 **What it means:**

* **P(A | B)** = Probability of **A** happening **given** B has happened (This is what we want to find!)
* **P(B | A)** = Probability of seeing **B** if we know A happened
* **P(A)** = Overall probability of A
* **P(B)** = Overall probability of B

---

### 🚢 Example: Titanic Dataset

We want to find the probability that a person **survived**, given:

* They are **female**
* They were in **passenger class 3**

$$
P(\text{Survived} | \text{Pclass=3, Gender=Female}) = \frac{P(\text{Pclass=3, Gender=Female} | \text{Survived}) \times P(\text{Survived})}{P(\text{Pclass=3, Gender=Female})}
$$

#### 🎯 Real-world Interpretation:

You're using **prior survival statistics** (like how many women in class 3 survived) to predict whether someone survived, based on their **gender and class**.

---

### 🤓 Naïve Bayes Classifier: Simple Yet Powerful

This is a **machine learning algorithm** based on Bayes’ Theorem.

🔍 **Why "Naïve"?**
It assumes that **all features (like gender, age, class)** are **independent** of each other — which isn’t usually true in real life, but it still works surprisingly well in practice!

---

### 🛠 How Naïve Bayes Works:

* You **train** the model on labeled data (e.g., who survived/didn’t, with gender/class/age info)
* The model **calculates probabilities** of each class (e.g., Survived vs Not Survived)
* It uses **Bayes’ Theorem** to find the class with the highest probability for a new instance

---

### 🧠 Real-Life Analogy:

Imagine you’re guessing whether someone passed an exam based on:

* Whether they studied 📖
* Got enough sleep 💤
* Attended class 🎓

Even if these factors are connected, Naïve Bayes treats them separately — and still gives a good prediction!

---

## 🔢 Normal Calculations in Naïve Bayes & Laplace Smoothing 🧮✨

---

### 🤔 Problem: When Multiplying Probabilities, Zero Kills Everything! 💥

Imagine we want to calculate the probability of a certain customer profile making a purchase, given their features:

* **N = 1** (Newsletter subscriber = Yes)
* **S = 0** (Social media follower = No)
* **W = 1** (Visited website = Yes)

Using Naïve Bayes formula:

$$
P(x | \text{Purchase} = 1) = P(N=1|1) \times P(S=0|1) \times P(W=1|1) \times P(\text{Purchase}=1)
$$

From the data:

* $P(N=1|1) = \frac{3}{5}$
* $P(S=0|1) = 0$  ← **This zero causes the whole product to be zero!**
* $P(W=1|1) = \frac{2}{5}$
* $P(\text{Purchase}=1) = \frac{1}{2}$

So,

$$
P(x|1) = \frac{3}{5} \times 0 \times \frac{2}{5} \times \frac{1}{2} = 0
$$

But this is **wrong**! Because just one zero probability wipes out the whole calculation.

---

### 🧴 Solution: Laplace Smoothing (Add-One Smoothing)

To fix this, we **add 1 to all counts** to avoid zeros. This is called **Laplace smoothing**.

Formula for smoothed probability:

$$
P(\text{feature} = value | \text{class}) = \frac{\text{count} + 1}{\text{total in class} + k}
$$

* **count** = Number of times this feature value appears in the class
* **total in class** = Total number of samples in this class
* **k** = Number of possible values for the feature (e.g., 2 for binary features)

---

### 🧮 Calculations with Laplace Smoothing:

For $P(S=0|1)$, since count was 0 and total in class is 5, and $k=2$:

$$
P(S=0|1) = \frac{0 + 1}{5 + 2} = \frac{1}{7}
$$

Similarly:

$$
P(N=1|1) = \frac{3 + 1}{5 + 2} = \frac{4}{7}, \quad P(W=1|1) = \frac{2 + 1}{5 + 2} = \frac{3}{7}
$$

---

### 🎯 Final probability calculation:

$$
P(x|1) = \frac{4}{7} \times \frac{1}{7} \times \frac{3}{7} \times \frac{5}{10} = 0.0175
$$

---

## 👩‍💻 Naïve Bayes – Customer Purchase Example

| Id | Newsletter Subscriber? | Social Media Follower? | Visited Website? | Purchase?      |
| -- | ---------------------- | ---------------------- | ---------------- | -------------- |
| 1  | 0                      | 1                      | 0                | 1              |
| 2  | 1                      | 0                      | 1                | 0              |
| 3  | 1                      | 1                      | 0                | 1              |
| 4  | 0                      | 0                      | 0                | 0              |
| 5  | 1                      | 0                      | 0                | 0              |
| 6  | 1                      | 1                      | 1                | 1              |
| 7  | 1                      | 0                      | 1                | 0              |
| 8  | 0                      | 1                      | 1                | 1              |
| 9  | 1                      | 0                      | 1                | 1              |
| 10 | 1                      | 1                      | 0                | 0              |
| 11 | 0                      | 1                      | 1                | ? (to predict) |

---

### 📊 Frequency Tables

| **Purchase** | 1 (Yes) | 0 (No) |
| ------------ | ------- | ------ |
| Count        | 5       | 6      |

| **Newsletter** | 1 (Yes) | 0 (No) |
| -------------- | ------- | ------ |
| Purchase = 1   | 3       | 2      |
| Purchase = 0   | 4       | 2      |

| **Social Media** | 1 (Yes) | 0 (No) |
| ---------------- | ------- | ------ |
| Purchase = 1     | 4       | 1      |
| Purchase = 0     | 1       | 5      |

| **Visited Website** | 1 (Yes) | 0 (No) |
| ------------------- | ------- | ------ |
| Purchase = 1        | 3       | 2      |
| Purchase = 0        | 2       | 4      |

---

### 🔍 Conditional Probabilities Example

* $P(\text{Newsletter} = 1 | \text{Purchase} = 1) = \frac{3}{5} = 60\%$
* $P(\text{Newsletter} = 0 | \text{Purchase} = 1) = \frac{2}{5} = 40\%$
* $P(\text{Newsletter} = 1 | \text{Purchase} = 0) = \frac{4}{6} \approx 66.7\%$
* $P(\text{Newsletter} = 0 | \text{Purchase} = 0) = \frac{2}{6} \approx 33.3\%$

(Similar calculations apply for Social Media and Visited Website)

---

### ⚖️ Overall Class Distribution

* $P(\text{Purchase} = 1) = \frac{5}{11} \approx 45\%$
* $P(\text{Purchase} = 0) = \frac{6}{11} \approx 55\%$

---

### ✅ Summary

* Naïve Bayes **calculates the probability** of purchase based on features assuming independence
* Laplace smoothing helps avoid **zero probabilities**, which break calculations
* Use frequency tables to calculate **conditional probabilities**
* Use these probabilities to predict unknown cases, like customer #11

---

## 🔮 Naïve Bayes Prediction Example: Will the Customer Purchase? 🛒

---

### 👀 Given Information

We want to predict if a customer will **make a purchase** based on these features:

| Newsletter Subscriber? | Social Media Follower? | Visited Website? |
| ---------------------- | ---------------------- | ---------------- |
| 0 (No)                 | 1 (Yes)                | 1 (Yes)          |

---

### 📊 Given Probabilities

| Condition       | Probability   |     |
| --------------- | ------------- | --- |
| P(News          | Purchase = 1) | 60% |
| P(No News       | Purchase = 1) | 40% |
| P(Social        | Purchase = 1) | 80% |
| P(No Social     | Purchase = 1) | 20% |
| P(Website       | Purchase = 1) | 60% |
| P(No Website    | Purchase = 1) | 40% |
| P(News          | Purchase = 0) | 80% |
| P(No News       | Purchase = 0) | 20% |
| P(Social        | Purchase = 0) | 20% |
| P(No Social     | Purchase = 0) | 80% |
| P(Website       | Purchase = 0) | 40% |
| P(No Website    | Purchase = 0) | 60% |
| P(Purchase = 1) | 50%           |     |
| P(Purchase = 0) | 50%           |     |

---

### ⚙️ Step 1: Calculate Probability **Given Purchase = 1**

Multiply the conditional probabilities for each feature *and* the prior probability of purchase:

$$
P(x|Purchase=1) \times P(Purchase=1) = P(No\,News|1) \times P(Social|1) \times P(Website|1) \times P(1)
$$

Plugging in numbers:

$$
= 0.40 \times 0.80 \times 0.60 \times 0.50 = 0.096 = 9.60\%
$$

---

### ⚙️ Step 2: Calculate Probability **Given Purchase = 0**

Similarly, multiply conditional probabilities *and* prior for no purchase:

$$
P(x|Purchase=0) \times P(Purchase=0) = P(No\,News|0) \times P(Social|0) \times P(Website|0) \times P(0)
$$

$$
= 0.20 \times 0.20 \times 0.40 \times 0.50 = 0.008 = 0.80\%
$$

---

### ⚖️ Step 3: Calculate Overall Probability & Make Prediction

We calculate the normalized probability of purchase given the features:

$$
P(Purchase=1 | x) = \frac{P(x|1) \times P(1)}{P(x|1) \times P(1) + P(x|0) \times P(0)} = \frac{0.096}{0.096 + 0.008} = 0.923 = 92.3\%
$$

---

### ✅ **Conclusion:**

The model predicts **92.3% chance of PURCHASE** for this customer based on the features (No Newsletter, Social Media follower, Visited Website).

---

### 💡 Real-Life Takeaway:

If you want to **target customers likely to buy**, this prediction tells you to **focus marketing efforts on customers matching these features** (active on social media and website, but not newsletter subscribers).


## 🔄 Calculating $P(x | \text{Purchase} = 0)$ with Laplace Smoothing

---

### 🔍 Given:

* Feature vector $x = \{ N=1, S=0, W=1 \}$
* We already have $P(x | \text{Purchase} = 1) = 0.0175$
* Now calculate $P(x | \text{Purchase} = 0)$

---

### Step 1: Calculate conditional probabilities (with Laplace smoothing)

| Feature             | Count (Purchase=0) | Probability (raw)   | Probability (smoothed)                        |
| ------------------- | ------------------ | ------------------- | --------------------------------------------- |
| Newsletter $N=1$    | 3                  | $\frac{3}{5} = 0.6$ | $\frac{3+1}{5+2} = \frac{4}{7} \approx 0.571$ |
| Social media $S=0$  | 5                  | $\frac{5}{5} = 1.0$ | $\frac{5+1}{5+2} = \frac{6}{7} \approx 0.857$ |
| Website visit $W=1$ | 3                  | $\frac{3}{5} = 0.6$ | $\frac{3+1}{5+2} = \frac{4}{7} \approx 0.571$ |

---

### Step 2: Calculate prior probability $P(\text{Purchase} = 0)$

Given total samples and prior knowledge:

$$
P(0) = \frac{5}{10} = 0.5
$$

---

### Step 3: Calculate $P(x | \text{Purchase} = 0)$

Multiply smoothed conditional probabilities and prior:

$$
P(x|0) = P(N=1|0) \times P(S=0|0) \times P(W=1|0) \times P(0)
$$

$$
= \frac{4}{7} \times \frac{6}{7} \times \frac{4}{7} \times 0.5
$$

Calculate step-by-step:

$$
\frac{4}{7} \times \frac{6}{7} = \frac{24}{49} \approx 0.4898
$$

$$
0.4898 \times \frac{4}{7} = 0.4898 \times 0.5714 \approx 0.2797
$$

$$
0.2797 \times 0.5 = 0.1399
$$

---

### Step 4: Compare with $P(x | \text{Purchase} = 1)$

Recall:

$$
P(x | \text{Purchase} = 1) = 0.0175
$$

Since

$$
0.1399 > 0.0175
$$

---

### ✅ **Conclusion:**

For the customer with features $N=1, S=0, W=1$, the **Naïve Bayes model predicts NO PURCHASE (Purchase = 0)**, because $P(x|0)$ is much higher than $P(x|1)$.

---

### 💡 Quick recap:

* Laplace smoothing prevents zero probabilities
* Multiply conditional probabilities for all features and prior class probability
* The class with the higher probability wins — in this case, **Purchase = 0**

---

## 🧠 Types of Naïve Bayes Classifiers Explained

---

### 1️⃣ **Gaussian Naïve Bayes** 🌡️

* **What it is:** Assumes that numerical features follow a **normal (Gaussian) distribution** — the classic bell curve.
* **When to use:** Best for **continuous numerical data** like height, weight, or temperature.
* **Example:** Predicting if a person will buy a product based on their age and income (which often fit a normal distribution).
* **Note:** Not very effective with categorical (non-numeric) data.

---

### 2️⃣ **Multinomial Naïve Bayes** 📝

* **What it is:** Designed for **discrete data** — counts or frequencies.
* **When to use:** Popular in **text classification** where features are word counts or term frequencies.
* **Example:** Classifying emails as spam or not spam based on how often certain words appear.

---

### 3️⃣ **Bernoulli Naïve Bayes** ✅❌

* **What it is:** Works with **binary/boolean features** (0 or 1).
* **When to use:** Good for text classification where features represent **presence or absence** of words (instead of frequency).
* **Example:** Checking if an email contains specific words (yes/no) to decide if it’s spam.

---

### 4️⃣ **Complement Naïve Bayes** ⚖️

* **What it is:** A variation of Multinomial Naïve Bayes, specifically designed to handle **imbalanced datasets** where some classes have many more samples than others.
* **When to use:** Helps improve performance when your data has class imbalance.
* **Example:** Spam detection where spam emails are far fewer than non-spam emails.

---

### 📝 **Where Naïve Bayes Shines: Text Classification**

Naïve Bayes models are widely used in text-related tasks like:

* **Spam detection:** Classify emails as spam or not spam
* **Sentiment analysis:** Determine if a review is positive or negative
* **Document categorization:** Assign topics to news articles or papers

---

### 🔑 **Summary:**

| Naïve Bayes Type | Data Type          | Use Case                  | Example                             |
| ---------------- | ------------------ | ------------------------- | ----------------------------------- |
| Gaussian         | Continuous numeric | Normally distributed data | Predicting height, weight, income   |
| Multinomial      | Discrete counts    | Word frequency in text    | Spam detection using word counts    |
| Bernoulli        | Binary features    | Word presence/absence     | Spam detection using word presence  |
| Complement       | Imbalanced data    | Imbalanced classes        | Spam detection with skewed datasets |

---

## 🤔 What is Ambiguity?

**Ambiguity** happens when a word, phrase, or sentence can be understood in **more than one way** — it’s unclear or has multiple meanings.

---

## 🎯 Why Ambiguity Matters in Analytics & Language?

* In text analysis, ambiguity can cause **misinterpretations**.
* It’s important to **detect and resolve** ambiguity for accurate insights — like in sentiment analysis, chatbots, or AI conversations.

---

## 😂 Ambiguity Examples (With a Twist!)

---

### Example 1: In-laws vs Outlaws

**Q:** What is the difference between in-laws and outlaws?
**A:** Outlaws are wanted...

**Ambiguity:**
The word **"wanted"** here is ambiguous!

* *Wanted* by the police (criminals being chased)
* Or *wanted* as in “desired” or “welcomed” (which could apply to in-laws!)

---

### Example 2: Tennis Player Dating Advice

**Q:** Why should one never date a tennis player?
**A:** Love means nothing to them...

**Ambiguity:**

* **Love** in tennis means **zero points** (0).
* But **love** in normal life means **affection and care**.
* So "Love means nothing" is a pun, playing on the double meaning!

---

## 🧠 Takeaway:

Ambiguity makes language fun and tricky! In analytics, understanding context and disambiguating words is crucial for precise results.

---

## 🔍 More on Ambiguity: Types & Examples

---

### 1️⃣ Dependency Ambiguity (Structural Ambiguity) 🏗️

* Happens when the **structure of a sentence** can be understood in different ways — basically, *who* is connected to *what* is unclear.
* Also called **syntactic ambiguity**.

---

### Example:

**"Maharashtra reports increased COVID-19 cases"** (from TOI report)

* Interpretation 1:
  Maharashtra **reports** the fact that **COVID-19 cases have increased**.

* Interpretation 2:
  Maharashtra **reports increased COVID-19 cases** — meaning Maharashtra is the one *experiencing* increased cases and reporting them.

The ambiguity arises because it's unclear whether "increased" describes the **act of reporting** or the **cases themselves**.

---

### 2️⃣ Pragmatic Ambiguity 🎭

* The most complex kind of ambiguity.
* Arises from the **context or intention** behind what is said, not just the words themselves.
* Often happens in conversations, sarcasm, or irony.

---

### Example:

**Passenger:** "Thank you for sending me to Delhi and my luggage to Mumbai."
**Passenger:** "Brilliant Service!"
**Chatbot:** "Thank you for the appreciation."

* Here, the passenger is clearly unhappy (sarcastic), but the chatbot misses this and takes it literally.
* The ambiguity is in the **intended meaning vs literal meaning** of "Brilliant Service!"

---

## 💡 Why care about ambiguity in Analytics?

* Ambiguity can cause **wrong interpretations** in text analysis or chatbots.
* Understanding **context, sentence structure, and speaker intent** is key to resolving ambiguity.

---

# 🌳 Decision Tree (CART) — Simple Explanation

---

### What is a Decision Tree? 🤔

* A **flowchart-like tree structure** used for **classification and regression** tasks.
* CART stands for **Classification And Regression Tree**.
* It’s a type of **supervised machine learning** — meaning you train the model with **known labels** (like fraud = Yes/No).

---

### Supervised vs Unsupervised Learning 🧠

| Learning Type    | What it Means                                         | Example Use Case                   |
| ---------------- | ----------------------------------------------------- | ---------------------------------- |
| **Supervised**   | We provide **class labels** to guide learning         | Predict customer churn (Yes/No)    |
| **Unsupervised** | Model finds patterns or groups on its own (no labels) | Group customers by buying behavior |

---

### How does a Decision Tree work? 🌲

* It splits data based on **features** (like Account Type, Balance, Transaction Type).
* Each split tries to **separate the classes** (e.g., Fraud = Yes or No) as cleanly as possible.
* Final splits (leaves) give you the **predicted class**.

---

### Example Dataset: Fraud Detection

| Transaction Id | Account Type | Balance | Transaction | Fraud |
| -------------- | ------------ | ------- | ----------- | ----- |
| 1              | savings      | 8000    | deposit     | No    |
| 2              | current      | 4000    | deposit     | No    |
| 3              | savings      | 3800    | withdraw    | Yes   |
| 4              | savings      | 4900    | deposit     | Yes   |
| 5              | current      | 50000   | withdraw    | Yes   |

![Decision Tree Example](https://github.com/user-attachments/assets/a1d05deb-14a6-4123-804f-096369c41763)

---

### Step-by-step Decision Tree Logic for Fraud Detection:

1. **Transaction 1:**

   * Account: savings
   * Balance: 8000 (> 5000)
   * Transaction: deposit
     → **Prediction:** Fraud = No

2. **Transaction 2:**

   * Account: current
   * Transaction: deposit
     → **Prediction:** Fraud = No

3. **Transaction 3:**

   * Account: savings
   * Balance: 3800 (≤ 5000)
   * Transaction: withdraw
     → **Prediction:** Fraud = Yes

4. **Transaction 4:**

   * Account: savings
   * Balance: 4900 (≤ 5000)
   * Transaction: deposit
     → **Prediction:** Fraud = Yes

5. **Transaction 5:**

   * Account: current
   * Transaction: withdraw
     → **Prediction:** Fraud = Yes

---

### Summary 💡

* Decision Trees **split the data** at decision points based on feature values.
* Helps to **predict outcomes** (like fraud) by navigating the tree.
* Easy to **interpret and visualize**.
* Useful for **both classification (fraud/no fraud)** and regression problems.

---

# 🔥 Entropy: Understanding Randomness and Homogeneity

---

### What is Entropy? 🤔

* **Entropy** measures the **randomness or disorder** in a dataset.
* It tells us **how mixed or pure** a group of data is.

---

### Why is Entropy Important? 🧠

* In Decision Trees, entropy helps decide the **best splits** by measuring the **homogeneity** of the data.
* Lower entropy means the data is more **pure** (most items belong to the same class).
* Higher entropy means the data is more **mixed** (many different classes present).

---

### Visual Explanation:

---

### 🔴 High Entropy = High Randomness = Less Homogeneous

* The data is very mixed, different classes are scattered evenly.
* More uncertainty in predicting the class.

![High Entropy](https://github.com/user-attachments/assets/10ec2954-2f65-41c6-b2ed-77d391fab4a3)

---

### 🔵 Low Entropy = Low Randomness = More Homogeneous

* Most data points belong to the same class.
* Less uncertainty, easier to predict outcomes.

![Low Entropy](https://github.com/user-attachments/assets/e489827b-eba9-48be-99ed-4c1e888c95c7)

---

### Summary:

| Entropy Level | Meaning                | Data Characteristics          |
| ------------- | ---------------------- | ----------------------------- |
| High Entropy  | More randomness        | Data is mixed, less pure      |
| Low Entropy   | Less randomness (pure) | Data is mostly from one class |

---

# 🔢 Entropy & Information Gain: How Decision Trees Decide Splits

---

### What is Entropy? 🔥

Entropy measures the **uncertainty** or **randomness** in data.

* More classes mixed = **higher entropy** (more disorder)
* Fewer classes (more pure) = **lower entropy** (less disorder)

---

### Entropy Formula:

$$
\text{Entropy}(D) = - \sum_{i=1}^{n} p_i \log_2(p_i)
$$

* $n$ = number of classes
* $p_i$ = proportion of data points in class $i$
* $\log_2(p_i)$ can be 0 or negative (since $0 < p_i \leq 1$)

---

### Example 1: Two Datasets & Their Entropy

| Dataset | Classes                   | Homogeneity               | Entropy           |
| ------- | ------------------------- | ------------------------- | ----------------- |
| D1      | \[A, B, C, D, E, F, G, H] | 8 classes (all different) | 3 (high entropy)  |
| D2      | \[A, A, A, A, B, B, B, B] | 2 classes, balanced       | 1 (lower entropy) |

---

#### Calculation of Entropy for D1:

* Each class has $\frac{1}{8}$ proportion
* So,

$$
\text{Entropy}(D1) = -8 \times \frac{1}{8} \times \log_2\left(\frac{1}{8}\right) = - \log_2\left(\frac{1}{8}\right) = 3
$$

(Since $\log_2(1/8) = -3$)

---

#### Calculation of Entropy for D2:

* Two classes each with $\frac{1}{2}$ proportion
* So,

$$
\text{Entropy}(D2) = -2 \times \frac{1}{2} \times \log_2\left(\frac{1}{2}\right) = -\log_2\left(\frac{1}{2}\right) = 1
$$

(Since $\log_2(1/2) = -1$)

---

# 📊 Exercise: Calculating Entropy & Information Gain for Student Exam Data

---

### Dataset:

| Theory Study | Lab Study | Pass Exam |
| ------------ | --------- | --------- |
| High         | High      | Yes       |
| High         | Medium    | Yes       |
| High         | Medium    | Yes       |
| High         | Low       | Yes       |
| Medium       | High      | Yes       |
| Medium       | Medium    | No        |
| Medium       | Medium    | Yes       |
| Medium       | Low       | No        |
| Low          | Low       | No        |

---

### Step 1: Calculate Overall Entropy

* Pass = Yes: 6/9
* Pass = No: 3/9

$$
\text{Entropy(Overall)} = -\left(\frac{6}{9} \log_2 \frac{6}{9} + \frac{3}{9} \log_2 \frac{3}{9}\right) = 0.91
$$

---

### Step 2: Calculate Entropy for Splits

---

#### Split on **Theory Study** levels:

* High (4 samples, all pass = Yes):

$$
E(High) = - \left(1 \times \log_2 1 + 0 \times \log_2 0\right) = 0
$$

* Medium (4 samples, 2 Yes & 2 No):

$$
E(Medium) = - \left(\frac{2}{4} \log_2 \frac{2}{4} + \frac{2}{4} \log_2 \frac{2}{4}\right) = 1
$$

* Low (1 sample, No):

$$
E(Low) = - \left(0 \times \log_2 0 + 1 \times \log_2 1 \right) = 0
$$

---

#### Weighted Average Entropy (Theory Study):

$$
E = \frac{4}{9} \times 0 + \frac{4}{9} \times 1 + \frac{1}{9} \times 0 = 0.444
$$

---

#### Split on **Lab Study** levels:

* High (2 samples, all Yes):

$$
E(High) = 0
$$

* Medium (4 samples, 3 Yes & 1 No):

$$
E(Medium) = -\left(\frac{3}{4} \log_2 \frac{3}{4} + \frac{1}{4} \log_2 \frac{1}{4}\right) = 0.81
$$

* Low (3 samples, 1 Yes & 2 No):

$$
E(Low) = -\left(\frac{1}{3} \log_2 \frac{1}{3} + \frac{2}{3} \log_2 \frac{2}{3}\right) = 0.91
$$

---

#### Weighted Average Entropy (Lab Study):

$$
E = \frac{2}{9} \times 0 + \frac{4}{9} \times 0.81 + \frac{3}{9} \times 0.91 = 0.66
$$

---

### Step 3: Calculate Information Gain

$$
\text{Information Gain} = \text{Entropy(Overall)} - \text{Weighted Entropy of Split}
$$

* For **Theory Study**:

$$
0.91 - 0.444 = 0.47
$$

* For **Lab Study**:

$$
0.91 - 0.66 = 0.24
$$

---

### Conclusion:

* **Theory Study** gives a **higher information gain** → better choice for splitting the data.

---

# 🚦 Decision Tree Calculation: Titanic Dataset Example

---

### Original Data Summary:

* Total passengers = **891**
* Survived = 1: **342**
* Did not survive = 0: **549**

---

### Step 1: Calculate Original Entropy

$$
p(\text{survived}) = \frac{342}{891} \approx 0.38, \quad p(\text{not survived}) = \frac{549}{891} \approx 0.62
$$

$$
\text{Entropy(Original)} = - \left(0.38 \log_2 0.38 + 0.62 \log_2 0.62\right) = 0.96
$$

---

### Step 2: Split Data on Gender

| Gender | Survived = 0 | Survived = 1 | Total |
| ------ | ------------ | ------------ | ----- |
| Male   | 468          | 109          | 577   |
| Female | 81           | 233          | 314   |

---

### Step 3: Calculate Entropy for Each Gender Group

---

#### For **Male** passengers:

$$
p(\text{survived} | \text{male}) = \frac{109}{577} \approx 0.19, \quad p(\text{not survived} | \text{male}) = \frac{468}{577} \approx 0.81
$$

$$
\text{Entropy(male)} = - (0.19 \log_2 0.19 + 0.81 \log_2 0.81) = 0.69
$$

---

#### For **Female** passengers:

$$
p(\text{survived} | \text{female}) = \frac{233}{314} \approx 0.74, \quad p(\text{not survived} | \text{female}) = \frac{81}{314} \approx 0.26
$$

$$
\text{Entropy(female)} = - (0.74 \log_2 0.74 + 0.26 \log_2 0.26) = 0.82
$$

---

### Step 4: Calculate Weighted Average Entropy After Split

$$
\text{Weighted Entropy} = \frac{577}{891} \times 0.69 + \frac{314}{891} \times 0.82 = 0.73
$$

---

### Step 5: Calculate Information Gain (IG)

$$
\text{Information Gain} = \text{Entropy(Original)} - \text{Weighted Entropy} = 0.96 - 0.73 = 0.23
$$

---

### **Interpretation:**

* Splitting on **Gender** reduces entropy from 0.96 to 0.73 → less uncertainty about survival.
* IG = 0.23 means the split gives us **good information** to predict survival.
* This is why gender is an important feature in predicting Titanic survival.

---

# 🚦 Decision Tree Calculation: Titanic Dataset — Splitting on **Passenger Class (pclass)**

---

### Data Summary for Split by pclass:

| pclass | Survived = 0 | Survived = 1 | Total |
| ------ | ------------ | ------------ | ----- |
| 1      | 80           | 136          | 216   |
| 2      | 97           | 87           | 184   |
| 3      | 372          | 119          | 491   |

---

### Step 1: Calculate Entropy for Each pclass

---

#### pclass = 1

$$
p(\text{survived}|pclass=1) = \frac{136}{216} \approx 0.63, \quad p(\text{not survived}|pclass=1) = \frac{80}{216} \approx 0.37
$$

$$
\text{Entropy(pclass=1)} = - (0.63 \log_2 0.63 + 0.37 \log_2 0.37) = 0.95
$$

---

#### pclass = 2

$$
p(\text{survived}|pclass=2) = \frac{87}{184} \approx 0.47, \quad p(\text{not survived}|pclass=2) = \frac{97}{184} \approx 0.53
$$

$$
\text{Entropy(pclass=2)} = - (0.47 \log_2 0.47 + 0.53 \log_2 0.53) = 0.99
$$

---

#### pclass = 3

$$
p(\text{survived}|pclass=3) = \frac{119}{491} \approx 0.24, \quad p(\text{not survived}|pclass=3) = \frac{372}{491} \approx 0.76
$$

$$
\text{Entropy(pclass=3)} = - (0.24 \log_2 0.24 + 0.76 \log_2 0.76) = 0.79
$$

---

### Step 2: Calculate Weighted Average Entropy After Split on pclass

$$
\text{Weighted Entropy} = \frac{216}{891} \times 0.95 + \frac{184}{891} \times 0.99 + \frac{491}{891} \times 0.79 = 0.87
$$

---

### Step 3: Calculate Information Gain (IG) for pclass

$$
\text{Information Gain} = \text{Entropy(Original)} - \text{Weighted Entropy} = 0.96 - 0.87 = 0.09
$$

---

### ✅ Conclusion:

* **Information Gain for gender split = 0.23**
* **Information Gain for pclass split = 0.09**

Splitting on **gender** gives **higher information gain**, meaning it is a **better feature to split on** for predicting survival on the Titanic than pclass.

---

# 🏦 Loan Approval Decision Tree Exercise

You are a loan officer and want to decide whether to **approve** or **reject** a loan application based on:

* **Income level** (Categorical): High / Medium / Low
* **Credit history** (Categorical): Good / Bad
* **Target variable:** Loan approval (Approve / Reject)

---

### Sample Data:

| Income Level | Credit History | Loan Approval |
| ------------ | -------------- | ------------- |
| High         | Good           | Approve       |
| Medium       | Good           | Approve       |
| Low          | Good           | Approve       |
| High         | Bad            | Approve       |
| Medium       | Bad            | Reject        |
| Low          | Bad            | Reject        |

---

## Step 1: Calculate Overall Entropy (Before Split)

Total samples = 6
Approvals = 4
Rejections = 2

$$
E(\text{Original}) = -\left(\frac{4}{6} \log_2 \frac{4}{6} + \frac{2}{6} \log_2 \frac{2}{6}\right) = 0.918
$$

---

## Step 2: Calculate Entropy After Split on **Income Level**

* **High Income (2 samples):** Approve = 2, Reject = 0

  $$
  E(\text{High}) = -\left(1 \times \log_2 1 + 0 \right) = 0
  $$

* **Medium Income (2 samples):** Approve = 1, Reject = 1

  $$
  E(\text{Medium}) = -\left(\frac{1}{2} \log_2 \frac{1}{2} + \frac{1}{2} \log_2 \frac{1}{2}\right) = 1
  $$

* **Low Income (2 samples):** Approve = 1, Reject = 1

  $$
  E(\text{Low}) = 1 \quad (\text{same as Medium})
  $$

---

### Weighted Average Entropy for Income Level Split:

$$
E(\text{Income Level}) = \frac{2}{6} \times 0 + \frac{2}{6} \times 1 + \frac{2}{6} \times 1 = 0.667
$$

---

## Step 3: Calculate Entropy After Split on **Credit History**

* **Good Credit (3 samples):** Approve = 3, Reject = 0

  $$
  E(\text{Good}) = 0
  $$

* **Bad Credit (3 samples):** Approve = 1, Reject = 2

  $$
  E(\text{Bad}) = -\left(\frac{1}{3} \log_2 \frac{1}{3} + \frac{2}{3} \log_2 \frac{2}{3}\right) = 0.918
  $$

---

### Weighted Average Entropy for Credit History Split:

$$
E(\text{Credit History}) = \frac{3}{6} \times 0 + \frac{3}{6} \times 0.918 = 0.459
$$

---

## Step 4: Calculate Information Gain (IG)

| Split Attribute | IG = Entropy Original - Weighted Entropy |
| --------------- | ---------------------------------------- |
| Income Level    | 0.918 - 0.667 = **0.251**                |
| Credit History  | 0.918 - 0.459 = **0.459**                |

---

## Decision:

**Split on Credit History first** because it gives higher information gain (0.459 > 0.251).

---

## Step 5: Further Splitting after Credit History

* For **Good Credit:** All Approve → Entropy = 0 → No further split required
* For **Bad Credit:**

  * Split by Income Level:

    * High Income: Approve = 1, Reject = 0 → Entropy = 0
    * Medium Income: Approve = 0, Reject = 1 → Entropy = 0
    * Low Income: Approve = 0, Reject = 1 → Entropy = 0
  * All subsets have entropy 0 → No further splits needed

---

# 🌳 Final Decision Tree:

```
If Credit History is Good:
    → Approve Loan

Else If Credit History is Bad:
    If Income Level is High:
        → Approve Loan
    Else If Income Level is Medium:
        → Reject Loan
    Else If Income Level is Low:
        → Reject Loan
```

---

### Summary:

* Start splitting with **Credit History**
* Then split **Bad Credit** by **Income Level**
* Final decisions are clear and entropy is minimized (pure subsets).

---

### How to Decide the Best Split in a Decision Tree?

| Concept              | Explanation                                                                                     |
| -------------------- | ----------------------------------------------------------------------------------------------- |
| **Entropy**          | Measures impurity or disorder in the data.                                                      |
| **High Entropy**     | Data is mixed (e.g., many classes mixed together) → harder to predict → **bad split**.          |
| **Low Entropy**      | Data is more pure/homogeneous → easier to predict → **good split**.                             |
| **Information Gain** | Difference between entropy before and after the split. The goal: **maximize information gain**. |

---

### Formula recap:

$$
\text{Information Gain} = \text{Entropy(before split)} - \text{Entropy(after split)}
$$

* The higher the Information Gain, the better the feature to split on.
* The best split is the one that reduces uncertainty the most.

---

### Intuition:

* If splitting on **Gender** gives high entropy (because classes are mixed roughly equally in male and female groups), it won’t help much.
* If splitting on **Last Login** groups data such that one group is mostly positive and the other mostly negative, entropy drops → it’s a better split.

---

## 🍎 Gini Index / Gini Impurity: A Measure of Impurity in Data

Gini Index (or Gini Impurity) is another way to measure how “mixed” or impure a dataset is — just like **Entropy**.

* **Goal:** The lower the Gini impurity, the better the split (more pure the data).
* **Best case:** Gini impurity = 0 means the data is perfectly pure (all items belong to one class).

---

### How to calculate Gini Impurity:

$$
\text{Gini impurity} = 1 - \sum (p_i)^2
$$

where $p_i$ is the proportion of class $i$ in the dataset.

---

### Example: Predict Fruit Type (A or B)

* Total fruits = 20
* Class A fruits = 10 → $P(A) = \frac{10}{20} = 0.5$
* Class B fruits = 10 → $P(B) = 0.5$

**Calculate Gini impurity:**

$$
1 - (0.5^2 + 0.5^2) = 1 - (0.25 + 0.25) = 1 - 0.5 = 0.5
$$

---

### For comparison, Entropy for the same data:

$$
\text{Entropy} = -\sum p_i \log_2(p_i)
$$

$$
= -[(0.5 \times \log_2 0.5) + (0.5 \times \log_2 0.5)]
$$

Since $\log_2 0.5 = -1$,

$$
= -[(0.5 \times -1) + (0.5 \times -1)] = -[-0.5 - 0.5] = 1
$$

---

### Summary:

| Measure           | Formula                | Value in Example | Interpretation                                           |
| ----------------- | ---------------------- | ---------------- | -------------------------------------------------------- |
| **Entropy**       | $-\sum p_i \log_2 p_i$ | 1                | Higher when classes are balanced (max uncertainty)       |
| **Gini impurity** | $1 - \sum p_i^2$       | 0.5              | Also higher for balanced classes, but scaled differently |

---

### Quick notes:

* Both Entropy and Gini are used to decide the best split in decision trees.
* Gini impurity is often preferred in **CART (Classification and Regression Trees)** because it’s easier to compute.
* Entropy is used in **ID3** and **C4.5** algorithms.
* Both aim to find splits that **reduce impurity** the most.

---

## Gini Impurity with More Than Two Classes

When your dataset contains **multiple classes**, the Gini impurity formula stays the same, but you sum the squared probabilities of *all* classes.

---

### Formula Recap:

$$
\text{Gini impurity} = 1 - \sum_{i=1}^n p_i^2
$$

where:

* $p_i$ = proportion of class $i$
* $n$ = number of classes

---

### Example: 3 classes with probabilities

* $p_1 = 0.4$
* $p_2 = 0.4$
* $p_3 = 0.2$

Calculate:

$$
\text{Gini impurity} = 1 - (0.4^2 + 0.4^2 + 0.2^2) = 1 - (0.16 + 0.16 + 0.04) = 1 - 0.36 = 0.64
$$

---

### What does this mean?

* **Higher Gini impurity means more mixed classes**, so the dataset is less pure.
* Compared to a 2-class split where the max impurity is 0.5, having **more classes can lead to higher Gini impurity values**, reflecting greater uncertainty.

---

### Quick note:

* The **maximum Gini impurity** increases as the number of classes increases.
* For *n* classes, maximum Gini impurity is:

$$
1 - \frac{1}{n}
$$

when all classes are equally likely.

---
