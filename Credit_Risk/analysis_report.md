# Module 12 Report Template

## Overview of the Analysis

This model was created intending to identify the creditworthiness of borrowers. Specfically, can a borrower be classified as a healthy or high-risk loaner on the basis of a few factors: [loan amount, interest rate, borrower income, debt to income ratio, number of accounts, derogatory marks, total debt].

To test this, approximately 77,000 past lending cases were used to train a logistic regression model (whereby 0 would indicate a healthy loan, and 1 being a high-risk loan). Within this dataset, 75k cases were already classified as healthy cases, with the remaining 2.5k cases identified as being high-risk loans.

The data is split into training and test sets (75:25 ratio). After training and testing,Standard model metrics is then reported (precision, recall, accuracy).

Given the imbalance in the frequency of healthy and high-risk loans identified in the dataset, it is possible that an ordinary logistic regression may classify healthy loan cases(as they make up the majority of cases) well while performing poorly on high-risk cases. To counteract this, a second model was created with random oversampling was used to balance the ratios between healthy and high-risk cases in the training phase, hopefully improving performance in classifying the rarer high-risk loans in the testing phase.

## Results

Using bulleted lists, describe the balanced accuracy scores and the precision and recall scores of all machine learning models.

* Machine Learning Model 1 - Standard Logistic Regression:
  - Accuracy 0.99

  Healthy Loans:
  - Precision: 1
  - Recall: 0.99

  High-risk Loans:
  - Precision: 0.85
  - Recall - 0.91

* Machine Learning Model 2 - With Random Oversampling:
  - Accuracy 0.99

  Healthy Loans:
  - Precision: 1
  - Recall: 0.99

  High-risk Loans:
  - Precision: 0.84
  - Recall - 0.99

## Summary

Both models show high accuracy and perform well in predicting healthy loans. However, the main focus should be on the performance metrics for high-risk loans, as the dataset is imbalanced and because mis-identifying high-risk loans negatively impacts the company.

The original model has slightly higher precision for high-risk loans compared to the model trained with 'Random Oversampling', indicating that the first model has a marginally lower rate of false positive predictions. However, the model trained with 'Random Oversampling' shows improved recall for high-risk loans, meaning that it is better at identifying the positive instances among the actual positive instances.

Overall, I recommend the use of the second model as it is a general improvement over the first, given recall improvements (improved detection of high-risk loans) with essentially no drawbacks. 