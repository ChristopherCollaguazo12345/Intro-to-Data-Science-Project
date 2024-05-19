### Problem Statement
Predict whether a loan application will be approved based on applicant and loan characteristics.

### Data Description
The dataset contains various features related to loan applications, including applicant details, loan amount, and loan status. The target variable is `Loan_Status`, indicating whether the loan was approved (Y) or not (N).

### Dataset Selection
The dataset is suitable for this problem as it includes a mix of categorical and numerical features that are relevant to loan approval decisions. The data can be used to train a classification model to predict the loan approval status.

### Expected Challenge One
The dataset is missing some values. We will need to handle the missing values before we can use the data for training the model.

Heres a plan to handle the missing values:
- `Gender, Married, Dependents, Self_Employed:` Fill missing values with the mode (most frequent value).
- `LoanAmount:` Fill missing values with the median, as it is less affected by outliers.
- `Loan_Amount_Term:` Fill missing values with the mode.
- `Credit_History:` Fill missing values with the mode, as it has a significant impact on loan approval.

### Methodology
Now that we have a train and test set, we can use the train set to train a model. For this project, we will 
a Logistic Regression model for classification due to the nature of the target variable and the simplicity of the model. Using a simple model allows for a faster training time and better performance, and it is a good starting point for a classification problem like this. Depending on the performance of the model, we can then move on to more complex models. 

- **Precision**: 95% for class 0 (not approved), 76% for class 1 (approved)
- **Recall**: 42% for class 0, 99% for class 1
- **F1-score**: 58% for class 0, 86% for class 1

The model performs well in predicting loan approvals (class 1) but struggles with loan rejections (class 0). This imbalance suggests a need for further improvement.

