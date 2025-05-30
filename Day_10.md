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

Pairs of Dimensions

![image](https://github.com/user-attachments/assets/482f1d5d-49cb-4ff6-8f02-ccf66279a855)

The graphs illustrate relationships between different academic skills using scatter plots. Here’s what each pair of dimensions represents:

1. **Spelling vs. Vocabulary**: This scatter plot shows a positive correlation, meaning higher spelling scores tend to align with higher vocabulary scores.
2. **Vocabulary vs. Multiplication**: The points are more scattered, suggesting a weaker or unclear correlation between vocabulary and multiplication skills.
3. **Spelling vs. Multiplication**: Similarly, this plot shows a weak or unclear correlation between spelling and multiplication skills.
4. **Multiplication vs. Geometry**: This pair appears to have a positive correlation, indicating that strong multiplication skills may be linked to stronger geometry performance.

---

# From Correlation to Components

PCA: Reduce multiple features into a component (e.g. here, two features to one component)
Step 1: Create a scatter plot of x and y and find its center
Step 2: Draw a line through the center in such a way that it will capture most of the variance

![image](https://github.com/user-attachments/assets/2f1d78fb-2ef4-42d4-b2b6-0bbd4a67abc6)

You’ve got it! The image visually explains **Principal Component Analysis (PCA)**—a dimensionality reduction technique. The idea is to replace multiple correlated features with a **single principal component** that captures most of the variance.

### Breaking it down:
1. **Scatter Plot & Center Calculation**  
   - You plot the original data (e.g., spelling vs. vocabulary scores).
   - The mean of all points is calculated to find the center.

2. **Drawing the Principal Component**  
   - A line is drawn through the center at an angle that **maximizes variance**—this becomes the **principal component**.
   - Instead of treating spelling and vocabulary as two separate features, PCA finds a new axis that best represents their combined variation.

### Why PCA?  
By reducing dimensionality, you can simplify datasets while preserving essential information. This helps with visualization, speed, and efficiency in machine learning models.

---

How to measure a component?

Weight: Position of a feature relative to the regression line
Weight = Component’s value for each original data point

Example

![image](https://github.com/user-attachments/assets/2c5142d7-2e9f-4b7e-ac92-b97190cc8de5)

Calculating weight by using the Pythagorean theorem:

d= √((x2−x1)^2+ ((y2−y1)^2) 
d= √((8.3−0)^2+ ((5.6−0^2) )
d= √(68.89 + 31.36)
d=10=Weight of tℎis point

The weight of a component is determined by its **position relative to the regression line**, effectively measuring how strongly a data point contributes to the principal component.

### Breakdown of the Example:
1. **Using the Pythagorean theorem**, the distance (or weight) of a data point from the origin is calculated:
   \[
   d = \sqrt{(x_2 - x_1)^2 + (y_2 - y_1)^2}
   \]
   - Given:
     - \( x_2 = 8.3, x_1 = 0 \)
     - \( y_2 = 5.6, y_1 = 0 \)
   - Substituting values:
     \[
     d = \sqrt{(8.3 - 0)^2 + (5.6 - 0)^2}
     \]
     \[
     d = \sqrt{68.89 + 31.36}
     \]
     \[
     d = 10
     \]
   - This distance is the **weight of this point**, representing how strongly it contributes to the principal component.

### Why It Matters:
- **Higher weights** mean the point plays a larger role in defining the principal component.
- **Smaller weights** indicate less influence on the overall variance.

This method helps transform multiple correlated features into a **single representative component**.

---

# Components for Spelling-Vocabulary and Multiplication-Geometry

StudentID	Spelling (S)	Vocabulary (V)	Component1 (S-V)	Multiplication (M)	Geometry (G)	Component2 (M-G)
1	1.8	2.1	2.8	5.4	5.6	7.8
2	2.9	3.1	4.3	6.6	5.7	8.7
3	4.6	5.7	7.3	2.8	1.6	3.2
4	8.0	7.1	10.7	3.5	3.4	4.9
5	8.1	8.0	11.4	1.3	2.2	2.6
6	8.3	5.6	10.0	7.0	9.1	11.5
7	4.4	4.2	6.1	9.1	7.3	11.6
8	7.2	6.3	9.6	8.1	7.8	11.3
9	4.2	5.1	6.6	9.9	9.3	13.6
10	8.7	10.3	13.5	8.2	8.7	12.0

---

Interpreting Components

Loadings/Coefficients: Explain the relationship between each component and the original dimensions (denoted by Y)
Calculations beyond the scope, but final result in our example:
Coefficient of Component1 (S-V) : Y = (0.72 . X1) + (0.69 . X2) + (-0.02 . X3) + (0.03 . X4)
Coefficient of Component2 (M-G): Y = (0.004 . X1) + (0.001 . X2) + (0.68 . X3) + (0.72 . X4)

---

Interpreting Components

![image](https://github.com/user-attachments/assets/a806c306-c05c-4d15-985e-d4311b6e51a3)

![image](https://github.com/user-attachments/assets/80e4cb88-6f31-4558-a2bc-4dc289c55a9e)

---

Final Result

StudentID	Language	Maths
1	2.8	7.8
2	4.3	8.7
3	7.3	3.2
4	10.7	4.9
5	11.4	2.6
6	10.0	11.5
7	6.1	11.6
8	9.6	11.3
9	6.6	13.6
10	13.5	12.0

---

# Resampling

Resampling: Modifying a dataset by changing its size or composition
A statistical technique used to generate new samples from an existing dataset
Changes the composition of our dataset
How? Bootstrapping or Cross-validation
Two methods: (1) Draw new samples from the dataset (Bootstrapping) or Splitting in different ways (K-Fold Cross Validation)

Bootstrapping: Draw random samples from the original data using replacement
Randomly draws samples with replacement
Same data point can appear multiple times in the same sample
Repeated multiple times
Helps when the dataset is small, to verify the model accuracy

Cross-validation: Split data into training set and a testing set
Example: K-fold cross validation
Divide data into k subsets (folds), e.g. sample 1, 2, and 3
Train the model on k-1 folds and tested on the remaining fold (e.g. Training: 1,2 and Test 3)
Repeat the process k times
Splits data into k equal parts (folds)
Each fold is used once as the test set,  and the rest as training data
No data fold is repeated in any fold (no replacement)

---

Oversampling: Increase the size of the minority class by duplicating samples or generating synthetic data
A technique used to handle imbalanced datasets by increasing the size of the minority class (i.e., predicted label)

Techniques:
  Duplicate samples from the minority class OR
  Generate synthetic samples using SMOTE
Example: SMOTE (Synthetic Minority Oversampling Technique): Handles imbalanced datasets, where the minority class has significantly lower samples than the others

SMOTE (Synthetic Minority Oversampling Technique)
  Creates synthetic samples for minority class (e.g., titanic: survived are less)
  Chooses a nearby neighbor and creates a new point in between
  Helps models learn better decision boundaries when one class is underrepresented
  Commonly used in binary classification problems where one class (e.g., fraud, disease, etc.) is rare.

---
