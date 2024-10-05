Project: Churn Prediction Model
This project aims to build a predictive model to identify customers likely to churn based on historical data. The analysis was conducted using a logistic regression model and various feature selection techniques, such as Recursive Feature Elimination (RFE), to optimize predictive performance.

Dataset
Columns: State, Account length, Area code, International plan, Voice mail plan, Number vmail messages, Total day minutes, Total day calls, Total day charge, Total eve minutes, Total eve calls, Total eve charge, Total night minutes, Total night calls, Total night charge, Total intl minutes, Total intl calls, Total intl charge, Customer service calls, Churn.
The target variable is Churn (binary classification).

Steps and Methods

Data Exploration & Preparation:

Explored the dataset and summarized the data using descriptive statistics.
Checked for missing values and performed data cleaning.
Converted categorical variables like 'International plan' and 'Voice mail plan' to binary (1 for 'Yes', 0 for 'No').
Label encoded the 'State' feature.

Train-Test Split:

Split the dataset into training and testing sets (70% train, 30% test).

Churn Rate:

The churn rate in the dataset was calculated at 14.24%.

Correlation Analysis:

Created a heatmap to visualize feature correlations.

Feature Selection with RFE:

Used Recursive Feature Elimination (RFE) to select the top 8 important features for the logistic regression model.

Model Development:

Developed a Logistic Regression model using StatsModels.
Evaluated the model performance by plotting the ROC curve and calculating AUC.

Threshold Optimization:

Explored different probability cutoffs to optimize the balance between precision, recall, and accuracy.

Model Evaluation:

Evaluated the model using metrics like confusion matrix, accuracy, precision, and recall for both the training and test datasets.
Key Results
The optimal threshold for classification was determined to be 0.25 based on the precision-recall tradeoff.
The accuracy of the model on the test set was 86%.
Precision on the test set: 44%
Recall on the test set: 55%

Conclusions
The logistic regression model successfully predicts customer churn with reasonable accuracy.
Feature selection using RFE helped in reducing overfitting by selecting only the most important features.
The precision-recall analysis helped identify the ideal probability cutoff of 0.25, balancing false positives and negatives.
This model can be used for customer retention strategies, focusing efforts on customers with a high likelihood of churning.
