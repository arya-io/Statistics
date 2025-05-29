Bayes Theorem and Naïve Bayes Classifier

Bayes’ Theorem: How to update probabilities when new evidence becomes available
P(A│B)= P(B│A)x P(A)/P(B) 
Example: For titanic dataset, find those who survived given that the were female and their passenger class was 3
P(survived│pclas=3, gender=female)=

      P(pclas=3, gender=female│survived)x P(survived)/P((pclas=3, gender=female│survived)) 

Naive Bayes: Implement Bayes’ theorem to solve classification problems
Naive because it assumes that all the features are independent

---

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

REMAIN

---

NAIVE BAYES PART

---

Naïve Bayes Types

Gaussian Naive Bayes: Gaussian (normal) distribution (Example: Height, Weight, etc); less effective with categorical data, Normally distributed numerical data
Multinomial Naive Bayes: Suitable for discrete data, often used in text classification with word frequency calculation
Bernoulli Naive Bayes: Designed for binary/boolean features, useful for text classification with binary attributes
Complement Naive Bayes: For imbalanced datasets
Text Classification: Text classification tasks such as spam detection, sentiment analysis, and document categorization

---

Ambiguity

---

Decision Tree:

A flowchart for classification and regression (Hence: Classification And Regression Tree - CART)
Type of supervised machine learning

Supervised Machine Learning: We provide class labels
Unsupervised learning: Ask the model to group similar data / find patterns. We do not provide class labels.
![image](https://github.com/user-attachments/assets/a1d05deb-14a6-4123-804f-096369c41763)
Example: Predict customer churn
    How easy or difficult is it? (Is original data giving any clues?)
    Do we need to do anything further? (Would splitting on a feature help?)

TABLE TO BE ADDED

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

ANOTHER EXAMPLE TO BE ADDED

---

TITANIC EXAMPLE



Weighted

---

TWO EXERCISES

---

Gini Index/Coefficient/Impurity

---
