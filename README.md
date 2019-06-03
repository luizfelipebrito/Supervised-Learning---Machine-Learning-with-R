Machine Learning with R
================
Luiz Felipe de Almeida Brito



## Supervised Learning - Machine Learning with R

### Machine learning algorithms covered in this script:

  - Support Vector Machines
  - Decision Tree
  - Random Forest
  - Support Vector Machines + PCA

### What is the main objective? What am I trying to predict?

The main purpose of this experiment is predicted if there is the
presence or not of heart disease in the patient.

### Data Set Information:

This database contains 76 attributes, but I am using a subset of 14 of
them. The “goal” field refers to the presence of heart disease in the
patient. It is integer valued from 0 (no presence) to 4. Heart Disease
UCI:
<https://www.kaggle.com/ronitf/heart-disease-uci>

### 1º Step - Clear Workspace

### 2º Step - Clear console

### 3º Step - The packages below must be installed. Once installed, you can comment this chunk code.

  - e1071: Support Vector Machine (SVM)
  - tree: Decision Tree
  - randomForest: Random Forest
  - caret: Classification and Regression Training
  - dplyr: A Grammar of Data Manipulation
  - ggplot2: Create Elegant Data Visualisations Using the Grammar of
    Graphics

### 4º Step - Load libraries.

### 5º Step - Set up my work directory.

### 6º Step - Reading my database.

### 7º Step - Only 14 attributes are used. Renaming columns in order to make our exploratory analysis easier.

  - 1 (age) Age in years
  - 2 (sex) Sex (1 = male; 0 = female)
  - 3 (cp) Chest pain type – Value 0: typical angina – Value 1: atypical
    angina – Value 2: non-anginal pain – Value 3: asymptomatic
  - 4 (trestbps) Resting blood pressure (in mm Hg on admission to the
    hospital)
  - 5 (chol) Serum cholestoral in mg/dl
  - 6 (fbs) Fasting blood sugar \> 120 mg/dl (1 = true; 0 = false)
  - 7 (restecg) Resting electrocardiographic results – Value 0: normal /
    Value 1: having ST-T wave abnormality / Value 2: showing probable or
    definite left ventricular hypertrophy by Estes’ criteria
  - 8 (thalach) Maximum heart rate achieved
  - 9 (exang) Exercise induced angina (1 = yes; 0 = no)
  - 10 (oldpeak) ST depression induced by exercise relative to rest
  - 11 (slope) The slope of the peak exercise ST segment – Value 0:
    upsloping / Vaue 1: flat / Value 2: downsloping
  - 12 (ca) Number of major vessels (0-3) colored by flourosopy
  - 13 (thal) 3 = normal; 6 = fixed defect; 7 = reversable defect
  - 14 (target) The predicted attribute

### 8º Step - Missing Values

Missing Values plays an important role in statistics and data analysis.
Often, missing values must not be ignored, but rather they should be
carefully studied to see if there is an underlying pattern or cause for
their
missingness.

### 9º Step - After a careful reading of the dataset information it is possible

### to infer that the columns below can be transformed into factor types.

### Factors are used to represent caterorical data. One can think of a ,

### factor as an integer vector where each integer has a label.

Using factors with labels is better than using integers because factors
are self-describing. Have a variable that has values “Male” and “Female”
is better than 1 and 2.

### 10º Step - Outlier detection and treatment

Outliers in data can distort predictions and affect the accuracy, if you
don’t detect and handle them appropriately especially in regression
models. Why outliers treatment is important? Because, it can drastically
bias/change the fit estimates and predictions. A handy explanation of
Outiliers it can be found in :
<https://www.r-bloggers.com/outlier-detection-and-treatment-with-r/>

### 10.1º Step - Detect Outliers - Univariate approach

For a given continuous variable, outliers are those observations that
lie outside 1.5 \* IQR, where IQR, the ‘Inter Quartile Range’ is the
difference between 75th and 25th quartiles. Look at the points outside
the whiskers in below box
plot.

### 10.2º Step - We found Outliers only for following continuous variable:

Let’s to try a bivariate approach, so that we can visualize in box-plot
of the X and Y, for categorical X’ (target).

### 11º Step - Identification Of Near Zero Variance Predictors.

It diagnoses predictors that have one unique value (i.e. are zero
variance predictors) or predictors that are have both of the following
characteristics: they have very few unique values relative to the number
of samples and the ratio of the frequency of the most common value to
the frequency of the second most common value is large

### 12º Step - Exploratory Data Analysis.

Statistical Methods for Exploratory Analysis. Theses methods include
clustering and dimension reduction techiques. It comes to visualization
a high dimensional or multidimensional data. Clustering organizes things
that are close into groups. Probably, the most kind of familiar distance
metric is the Euclidean distance which is just kind of the stright-line
distance between any two points.

Hierarchical Clustering give us an ideia of the relationship between
variables or observation.

### 13º Step - Analytic Graphics.

They help us find patterns in data and understand its properties. They
suggest modeling strategies to communicate results. - Show Comparisons.
- Show causality, mechanism, explanation, systematic structure. - Shom
multivariate data. - Integrate multiple models of
evidence.

### 14º Step - Setting Random number seed with Set.seed ensure reproducibility.

Always set the random number seed when conducting a simulation.

### 15º Step - The training set is used to fit the models;

The test set is used for assessment of the generalization error of the
final chosen model. Ideally, the test set should be kept in a “vault,”
and be brought out only at the end of the data analysis. It generates
randomly the indices for test base. We split out 30% for testing and 70%
for training.

### 16º Step - SVM - Support Vector Machines

### 17º Step - Decision Tree

### 18º Step - Random Forest

### 19º Step - Principal Component Analysis (PCA)

The principal components are equal to the right singular values if you
first scale(Subtract the mean, divide by the standard deviation) the
variables. We do not use the “target” column when pca is applied. Pca’s
results (standard deviation, proportional variance and proportion of
cumulative variance)

### 19.1º Step - Principal Component Analysis (PCA)

We are going to use only The principal components that maintain a
cumulative variance of 100% of the total.

### 20º Step - SVM - Support Vector Machines + PCA
