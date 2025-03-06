# Telecom-Churn-Case-Study

# Overview
This case study focuses on predicting customer churn in the telecommunications industry using customer usage data from a leading telecom firm. The objective is to build predictive models to identify customers at high risk of churn and identify the main indicators of churn. The analysis considers high-value customers only, as they contribute significantly to the revenue.

# Business Objective
Predict customer churn in the ninth month using data from the first three months. The goal is to reduce churn of high-value customers and prevent revenue leakage.

# Dataset
The dataset contains customer-level information for four consecutive months - June, July, August, and September (encoded as 6, 7, 8, and 9, respectively).
# Analysis steps

**Data Cleaning and EDA (Exploratory Data Analysis)**

**Import Necessary Packages and Libraries:**  Loaded the dataset into a dataframe.

**Check Data Types and Null Values:** Identified columns with incorrect data types and checked for missing values.

**Handle Duplicates and Unique Identifiers:** Checked for duplicate records and set 'mobile_number' as the unique identifier.

**Column Renaming and Data Type Conversion:** Renamed columns for consistency and converted columns to appropriate data types.

**Filter High-Value Customers:** Selected customers whose 'Average_rech_amt' in months 6 and 7 are greater than or equal to the 70th percentile.

**Handle Missing Values:** Dropped columns with more than 50% missing values and imputed meaningful columns.

**Drop Irrelevant Columns:** Removed columns with only one unique value and those related to the churn phase (month 9).

**Tag Churn Variable:** Labeled the target variable for churn prediction.

**Final Dataset:** Retained 30,011 rows and 126 columns.

# Exploratory Data Analysis (EDA)
 * Analyzed customer usage patterns and identified key indicators of churn.

 * Performed correlation analysis and created derived variables.

 * Handled outliers by capping them at the 99th percentile.

 * Created dummy variables for categorical data.
 
# Pre-processing Steps

**Train-Test Split:** Divided the data into training and testing sets.

**Handle Class Imbalance:** Used the SMOTE technique to balance the classes.

**Standardize Predictors:** Standardized predictor columns to mean 0 and standard deviation 1.

# Modeling
# Model 1: Logistic Regression with RFE & Manual Elimination
  Identified the most important predictors of churn and their coefficients.
  
# Model 2: PCA + Logistic Regression  
**Train Performance:**

* Accuracy: 0.627

* Sensitivity: 0.918

* Specificity: 0.599

* Precision: 0.179

* F1-score: 0.3

** Test Performance:**

* Accuracy: 0.086

* Sensitivity: 1.0

* Specificity: 0.0

* Precision: 0.086

* F1-score: 0.158

# Model 3: PCA + Random Forest Classifier
**Train Performance:**

* Accuracy: 0.882

* Sensitivity: 0.816

* Specificity: 0.888

* Precision: 0.408

* F1-score: 0.544

**Test Performance:**

Accuracy: 0.86

Sensitivity: 0.80

Specificity: 0.78

Precision: 0.37

F1-score: 0.51

# Model 4: PCA + XGBoost
**Train Performance:**

* Accuracy: 0.873

* Sensitivity: 0.887

* Specificity: 0.872

* Precision: 0.396

* F1-score: 0.548

**Test Performance:**

* Accuracy: 0.086

* Sensitivity: 1.0

* Specificity: 0.0

* Precision: 0.086

* F1-score: 0.158

# Recommendations
**Indicator 1:** Concentrate on users with 1.27 standard deviations lower than average incoming calls from fixed line. They are most likely to churn.

**Indicator 2:** Focus on users who recharge less number of times (less than 1.2 standard deviations compared to average) in the 8th month. They are second most likely to churn.

**Model Choice:** Use the PCA + Logistic Regression model to predict churn, as it has an ROC score of 0.87 and test sensitivity of 100%.

# Contributer
* Sravana Sanka
* Srikrishna Jana

