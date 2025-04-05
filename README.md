Overview of the Analysis:


  Purpose of the Analysis - The goal of this analysis is to determine if the Logistic Regression machine learning model can more accurately depict healthy loans vs. high-risk loans using the original dataset or a dataset using oversampling to increase the size of the      minority class (high-risk loans).

  The Dataset - The dataset used to perform the analysis consists of information on 77,536 loans.  The data includes columns for loan_size, interest_rate, borrower_income, debt_to_income ration, number_of_accounts, derotatory_marks, total_debt and loan_status.  The   
  category used to attempt prediction is loan_status.  The data provided in the other columns were used as features to train the data and inform the predictions.
  
  Stages of the Machine Learning Process - The stages of the machine learning process are very scripted.  If followed in order, they will provide you with an accurate assessment of the model's ability to make predictions.  The stages of the machine learning process are 
  as follows:
      - Prepare the data - Import the file, establish a Data Frame, evaluate the columns and features.
      - Separate the data into features and labels - The labels are what you are attempting to predict (the status of the healthy loan (0) or the high-risk loan (1).  The features are all of the remaining data you will use to train and test the model.
      - Train_Test_Split function - Use this function to separate the features and the labels data into training and testing datasets.
      - Import the machine learning model from the library - This instance I used the Logistic Regression fro SKLearn.
      - Instantiate the model.
      - Fit the model using the training data
      - Use the model to make predictions using the features test data.
      - Evaluate the predictions - These evaluations are done by calculating and comparing metrics like a balanced accuracy score, a confusion matrix, and a classification report.
      
  Machine Learning Methods Utilized:
       - LogisticRegression model from SKLearn - primary model used in the analysis
       - train_test_split from SKLearn - supporting functions used in the analysis
       - confusion_matrix, balanced_accuracy_score, classification_report from SKLearn - models were evaluated by these functions

Results

Using bulleted lists, describe the balanced accuracy scores and the precision and recall scores of all machine learning models.

* Machine Learning Model 1 - LogisticRegression:
  * Accuracy - While it was 99%, this can be misleading if the dataset is imbalanced.
  * Precision - For the healthy loans it was perfect, but the high-risk loans was .84 which means 16% of the predicted positives were fake.
  * Recall - Near perfect for healthy loans, but high-risk loans were at .94



* Machine Learning Model 2 - LogisticRegression (with oversampled data):
  * Accuracy - Again it was at 99%
  * Precision - For the healthy loans, it was perfect again and the high-risk loans stayed at .84
  * Recall - Near perfect for the healthy loans again, but the high-risk loans increased to .99 so it identified nearly all the high-risk loans.

Summary

The models used did a great job in using the original data to predict the values of the healthy loans.  Precision was 100% and recall was 99%.
The models used were pretty good at predicting the value of high-risk loans, but not as good as predicting the healthy loans.  Precision was 84% and recall was 99%.

