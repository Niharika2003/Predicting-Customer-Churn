# Predicting-Customer-Churn

### 1. Project Overview
#### 1.1. Introduction
The objective of this project is to predict customer churn using historical data from a telecommunications company. Customer churn refers to the phenomenon where customers stop using a company's services. Predicting churn helps companies to retain customers by proactively addressing their issues.

#### 1.2. Problem Statement
**Example**:
The problem is to identify the customers who are likely to churn based on their historical data and service usage patterns. The goal is to predict the churn status of customers with high accuracy.

#### 1.3. Data Description
**Example**:
The dataset consists of customer data with 21 features and one target variable, `Churn Value`. Features include demographic information, account information, service usage, and more. The target variable is binary, indicating whether a customer churned (1) or did not churn (0).

### 2. Data Preprocessing
#### 2.1. Data Cleaning

- Dropped irrelevant columns: `CustomerID`, `Lat Long`.
- Handled missing values by removing rows with missing data.
- Converted categorical variables to numeric using one-hot encoding.

#### 2.2. Feature Engineering
- Created dummy variables for categorical features using one-hot encoding.
- Standardized numerical features using `StandardScaler`.

### 3. Exploratory Data Analysis (EDA)
#### 3.1. Distribution Analysis
**Example**:
A count plot was created to visualize the distribution of the target variable, showing a significant imbalance between churned and non-churned customers.

#### 3.2. Correlation Analysis
A correlation matrix was plotted to identify relationships between features. Some features were found to be highly correlated, indicating potential multicollinearity.

### 4. Model Development
#### 4.1. Model Selection
Three models were selected:
- **Logistic Regression**: Chosen for its simplicity and interpretability.
- **Random Forest**: Chosen for its robustness and ability to handle feature importance.
- **Gradient Boosting**: Chosen for its high predictive accuracy.

#### 4.2. Model Training
The dataset was split into training (80%) and testing (20%) sets. Each model was trained using the training set. Cross-validation was performed to ensure robustness.

### 5. Model Evaluation
#### 5.1. Evaluation Metrics
Models were evaluated using accuracy, precision, recall, F1-score, and ROC AUC. These metrics provide a comprehensive evaluation of the model's performance, especially for imbalanced datasets.

#### 5.2. Results
- **Logistic Regression**: Accuracy = 0.963, ROC AUC = 0.936
- **Random Forest**: Accuracy = 0.997, ROC AUC = 0.995
- **Gradient Boosting**: Accuracy = 1.00, ROC AUC = 1.00

### 6. Model Interpretation
#### 6.1. Feature Importance
**Example**:
Feature importance was analyzed for Random Forest and Gradient Boosting. Features like `tenure`, `Monthly Charges`, and `Contract` were among the most important for predicting churn.

### 7. Conclusion
#### 7.1. Summary
Gradient Boosting achieved perfect accuracy, suggesting potential overfitting. Random Forest also performed exceptionally well. Logistic Regression, while slightly less accurate, offered good interpretability.

#### 7.2. Future Work
Future work could involve further hyperparameter tuning, testing on a more extensive dataset, and exploring other machine learning algorithms. Additionally, strategies to address class imbalance could be implemented.


