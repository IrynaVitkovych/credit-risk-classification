# credit-risk-classification
### Overview of the Analysis

This analysis aims to create a supervised machine learning model that will predict if a loan is healthy (class 0) or high-risk (class 1). We will use logistic regression as a binary classifier for our model here. The analysis was conducted on financial data, specifically focusing on loan size, interest rate, borrower income, debt-to-income ratio, number of accounts, derogatory marks, and total debt. The objective was to predict the loan status as a healthy loan (0) or a high-risk loan (1). The data used is a 77,537-line CSV file.


The stages of the machine learning process in this analysis included:

* Splitting Data: The data was divided into labels and features. The label was determined by the loan status, categorized as either healthy or high-risk, while the remaining seven columns constituted the features.

* Data Splitting: Subsequently, the dataset was split into training and testing subsets to facilitate model training and evaluation.

* Model Creation: A Logistic Regression model from the sklearn library was instantiated. Logistic Regression was chosen as a binary classifier, given the task of classifying loans as either healthy or high-risk, with no other possible outcomes.

* Model Fitting: The Logistic Regression model was fitted with the training data to learn patterns and relationships within the dataset.

* Prediction: Using the fitted model, predictions were generated for the test data to assess the model's performance on unseen data.

* Performance Evaluation: The model's performance was evaluated using standard evaluation metrics such as accuracy, precision, and recall scores, providing insights into its effectiveness in classifying loans into the appropriate categories.

Description of Logistic Regression Model Accuracy, Precision, and Recall Scores
Accuracy: The overall accuracy of the model is 0.99, indicating that it correctly classifies 99% of the instances.

Precision
Healthy Loan (class 0): 1.00
High-Risk Loan (class 1): 0.84

Recall
Healthy Loan (class 0): 0.99
High-Risk Loan (class 1): 0.94

Summary

The logistic regression model demonstrates strong predictive performance in classifying healthy loans (class 0), achieving precision of 1.00 and recall of 0.99. However, for high-risk loans (class 1), while the model still performs well, precision drops to 0.84 and recall to 0.94.

The lower precision and recall in predicting high-risk loans (class 1) can be attributed to the imbalanced dataset, where the support test data for class 1 is only 619 compared to 18765 for class 0. With significantly fewer high-risk loans in the dataset, the model has limited examples to learn from, impacting its ability to accurately predict this class.

To improve the model's performance in identifying high-risk loans, it's essential to address the imbalance in the dataset. Adding more high-risk loans to the training data could enhance the model's learning and lead to better predictions for this class.

In the context of loan classification, prioritizing the prevention of high-risk loans is crucial, as the potential losses from defaulted loans outweigh the interest earned from successful loans. Despite the challenges with predicting high-risk loans, the overall accuracy of the model remains high at 99%.