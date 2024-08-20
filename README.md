# credit-risk-classification
Module 20 Challenge

### Timeline
* Wednesday, August 14th 2:30 PM - Created Repo.
* Wednesday, August 14th 3:15 PM - Performed Split, Regression Test, Confusion Matrix.
* Monday, August 19th 6:20 PM - Answered question #4 in the ipynb file.
* Monday, August 19th 10:28 PM - Completed Overview of the Analysis.

### Resources
* Class Activity: predicting_diabetes_solution.ipynb
* Class Activity: classifying_social_media_influencers_solution.ipynb

-------------------------------------------------------------------------
# Overview of the Analysis

In this section, describe the analysis you completed for the machine learning models used in this Challenge. This might include:

* **Explain the purpose of the analysis.**

    The purpose of this analysis is to build a predictive model capable of identifying loans with a higher propensity for default. 

* **Explain what financial information the data was on, and what you needed to predict.** 

    The model will leverage seven key features or data variables:

        a. Loan size: The principal amount of the loan.
        b. Interest rate: The annual percentage rate charged on the loan.
        c. Borrower income: The annual income of the loan applicant.
        d. Debt-to-income ratio: The proportion of the borrower's income allocated to debt payments.
        e. Number of accounts: The total number of credit accounts held by the borrower.
        f. Derogatory marks: A count of negative credit events, such as late payments or bankruptcies.
        g. Total debt: The aggregate amount of debt owed by the borrower.

    By examining the relationships between the variables and loan default outcomes, the model aims to provide insights into the factors driving default risk and inform strategies for loan portfolio management and risk mitigation.

* **Provide basic information about the variables you were trying to predict (e.g., `value_counts`).**
    The features or data variables exhibited a diverse range of value types, including:
    * Decimals: Debt-to-Income Ratio
    * Percentages: Interest Rates
    * Binary: Derogatory Marks (0 or 1)
    * Integers: Number of Accounts
    * Currency: Loan Size, Borrower Income, Total Debt (in thousands of dollars)

* **Describe the stages of the machine learning process you went through as part of this analysis.**
    Stages of machine learning:
    1. Import the data
    2. Clean the data, if needed (e.g., remove outliers)
    3. Organize the data (transfrom the data as needed e.g., dummies, )
    4. Create training and testing data sets (e.g., split and fit the data)
    5. Select appropriate model (e.g., Logistic Regression model)
    6. Tune hyperparameters
    7. Run the prediction and classification report 
    8. Assess model's perfromance and determine if you need to adjust model or use for predictions.

* **Briefly touch on any methods you used (e.g., `LogisticRegression`).**
    
    Here are the methods used in Logistic Regression for model building and evaluation:
    * train_test_split: Divides a dataset into training and testing subsets for model development and evaluation.
    * fit: Trains a machine learning model on a specified dataset, learning patterns to make predictions
    * score: Evaluates a trained model's performance on a given dataset.
    * predict: Generates predictions for new, unseen data using a trained model.
    * confusion_matrix: Visualizes the performance of a classification model by displaying correct and incorrect predictions.
    * f. classification_report: Provides a summary of a classification model's performance, including precision, recall, F1-score, and support.

## Results

Using bulleted lists, describe the accuracy scores and the precision and recall scores of the machine learning model used.

* **Machine Learning Model 1:** LogisticRegresion
    * Overall Accuracy: 0.99
    * Class 0 = Healthy Loan
        * precision: 1.00
        * recall: 0.99
        * f1-score: 1.00
    * Class 1 = High-risk Loan
        * precision: 0.85
        * recall: 0.91
        * f1-score: 0.88

## Summary

Summarize the results of the machine learning models, and include a recommendation on the model to use, if any. For example:

    The Logistcial Regression Model does an excellent job of predicting a 'healthly loan' across precision, recall, and F1-Score, and does a good job of predicting a 'high risk loan' across precision, recall, and f1-score.   In other words the model does a better job of predicting the healthy loans vs the high risk loans. While the overall F1-score is high (0.94), the F1-score for Class 1 (0.88) indicates room for improvement, especially if the goal is to accurately identify default loans.