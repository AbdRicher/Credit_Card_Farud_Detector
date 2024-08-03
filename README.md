# Credit Card Fraud Detector
## 1. Data Preprocessing
### Exploratory Data Analysis (EDA)
Visualization Tools: We used Matplotlib and Seaborn for visualizations.
Initial Data Inspection: We performed an initial inspection of the dataset to understand the types of features, checked for missing values, and assessed the distribution of features. This included plotting histograms, box plots, and scatter plots to visualize the data and detect any patterns or anomalies.

### Encoding Categorical Variables
Ordinal Encoding: Applied for features where there is an inherent order in the categories, if any such features existed in the dataset.
Label Encoding: Used for the target variable 'Class' (fraud or not fraud), transforming it into a numerical format.
One-Hot Encoding: Implemented for nominal categorical features to create binary columns for each category, ensuring that the model can process these categorical variables effectively.

### Outlier Detection and Handling
Interquartile Range (IQR) Method: Outliers were identified using the IQR method:
Lower Bound: Q1 - 1.5 * IQR
Upper Bound: Q3 + 1.5 * IQR
Values outside these bounds were considered outliers and were replaced with the respective lower or upper bound values. This step helped manage extreme values and maintain data integrity.

### Feature Scaling
Standard Scaler: Applied to normalize the features, ensuring they have a mean of 0 and a standard deviation of 1. This transformation is crucial for algorithms like Logistic Regression to perform optimally, as it ensures all features contribute equally to the decision-making process.

## 2. Model Training
### Logistic Regression
Model Selection: Logistic Regression was chosen for its simplicity and effectiveness in binary classification problems like fraud detection.
Training and Testing: The preprocessed data was split into training and testing sets. The Logistic Regression model was trained on the training set.
Evaluation: The model's performance was evaluated using standard metrics such as accuracy, precision, recall, and F1 score. These metrics provided insights into the model's effectiveness in identifying fraudulent transactions.

### Conclusion
The comprehensive preprocessing approach, including encoding categorical variables, outlier imputation using the IQR method, and feature scaling, combined with Logistic Regression, resulted in a robust predictive model for credit card fraud detection. Each preprocessing step was crucial to prepare the data optimally for model training, contributing to the overall performance of the Logistic Regression model in identifying fraudulent transactions.
