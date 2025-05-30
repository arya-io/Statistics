Factor Analysis/Dimensionality Reduction

Reduce the number of features without losing much information
Example: Credit card fraud – Day of the week, Time, Place, Reason, Amount, Online/Offline, …?
Data Summarization or Data Reduction technique
Also called Dimensionality reduction
One implementation: Principal Component Analysis (PCA), see C:\lectures\CDAC\DAI\PCA.docx
New components replace factors, so transformation technique, not selection technique
Component ≠ Factor/Feature
Analysis of relationships between Factors/Features -> Components
We only look for columns of high correlation values

---

Finding Components in PCA

Dataset C:\code\Data Analytics\pca_student_test_scores.csv
Scatterplots: pca_basics_student_test_scores.py (Output on the next slide)
Observation: Only Spelling-Vocabulary and Multiplication-Geometry are correlated

Student exercise : Create correlation plots among Spelling-Vocabulary and Multiplication-Geometry : pca_basics_student_test_scores_regression.py (Output on slide after next)

---

Whole PCA Part

---

# Resampling

Resampling: Modifying a dataset by changing its size or composition
How? Bootstrapping or Cross-validation
Bootstrapping: Draw random samples from the original data using replacement
Cross-validation: Split data into training set and a testing set
Example: K-fold cross validation
Divide data into k subsets (folds), e.g. sample 1, 2, and 3
Train the model on k-1 folds and tested on the remaining fold (e.g. Training: 1,2 and Test 3)
Repeat the process k times
Oversampling: Increase the size of the minority class by duplicating samples or generating synthetic data
Example: SMOTE (Synthetic Minority Oversampling Technique): Handles imbalanced datasets, where the minority class has significantly lower samples than the others (Code: gender-smote.py and smote.py)

---
