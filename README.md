# Deep Learning Model for Loan Status Prediction

## Overview

This project focuses on building a deep learning model for predicting loan status using a subset of the LendingClub DataSet obtained from Kaggle [https://www.kaggle.com/wordsforthewise/lending-club]. The dataset contains historical data on loans given out by LendingClub, including information on whether or not the borrower defaulted (charge-off). The goal is to develop a model that can assess the status of a borrower paying back their loan, enabling the evaluation of new potential customers in the future.

## Data

The dataset has undergone comprehensive preprocessing, including data cleaning and feature engineering. Missing values have been addressed, unnecessary columns dropped, and categorical columns converted into numerical values for model compatibility. Exploratory data analysis (EDA) and visualization were conducted to gain insights into the dataset.

The project relies on two datasets:

lending_club_info.csv:** Information about each column in the lending_club_loan_two dataset.
lending_club_loan_two.csv:** The primary dataset containing borrower and loan details.
The primary dataset, lending_club_loan_two.csv, is large, and GitHub has file size limitations. Therefore, the dataset has been split into two parts. To access the full dataset, follow the instructions below.

Instructions for Accessing the Full Dataset
Download the Split Parts:

Download dataset.partaa and dataset.partab
Combine Split Files:

For Unix-based Systems (Linux, macOS):
cat dataset.part* > lending_club_loan_two.zip
For Windows:
copy /b dataset.part* lending_club_loan_two.zip
Extract the Combined File:

Extract the combined zip file to obtain lending_club_loan_two.csv.
Place the Datasets:

Place lending_club_loan_two.csv next to lending_club_info.csv in the project directory.


## Model

The deep learning model is implemented using TensorFlow and Keras. To mitigate overfitting, dropout layers have been incorporated. Data normalization has been applied to enhance model performance. The model's training process includes stopping criteria to prevent overfitting.

## Evaluation

The dataset was split into training, cross-validation, and test sets. The model was evaluated on the test set, producing the following classification Report:


Classification Report:

          precision    recall  f1-score   support

       0       0.95      0.45      0.61      7711
       1       0.88      0.99      0.94     31811


Results indicate an F1-score of 61% and 94% for classes 0 (default) and 1 (repayment), respectively. While these results are acceptable, there are opportunities for improvement through future work.

## Future Work

1. **Feature Engineering:** Explore additional features or transformations to enhance model understanding and predictive power.

2. **Model Architecture:** Experiment with different deep learning architectures to improve overall performance.

3. **Threshold Optimization:** Investigate the impact of the threshold (currently set at 0.5) on model performance by examining AUC and ROC curves. Adjust the threshold for optimal results.

4. **Hyperparameter Tuning:** Conduct grid search to fine-tune hyperparameters such as learning rate (alpha) for improved model generalization.
