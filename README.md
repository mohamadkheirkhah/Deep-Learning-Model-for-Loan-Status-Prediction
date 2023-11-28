# Deep Learning Model for Loan Status Prediction

## Overview

This project focuses on building a deep learning model for predicting loan status using a subset of the LendingClub DataSet obtained from Kaggle. The dataset contains historical data on loans given out by LendingClub, including information on whether or not the borrower defaulted (charge-off). The goal is to develop a model that can assess the likelihood of a borrower paying back their loan, enabling the evaluation of new potential customers in the future.

## Data

The dataset has undergone comprehensive preprocessing, including data cleaning and feature engineering. Missing values have been addressed, unnecessary columns dropped, and categorical columns converted into numerical values for model compatibility. Exploratory data analysis and visualization were conducted to gain insights into the dataset.

## Model

The deep learning model is implemented using TensorFlow and Keras. To mitigate overfitting, dropout layers have been incorporated. Data normalization has been applied to enhance model performance. The model's training process includes stopping criteria to prevent overfitting.

## Evaluation

The dataset was split into training, cross-validation, and test sets. The model was evaluated on the test set, producing the following confusion matrix:

[[ 3479 4232]
[ 164 31647]]


Classification Report:
          precision    recall  f1-score   support

       0       0.95      0.45      0.61      7711
       1       0.88      0.99      0.94     31811

accuracy                           0.89     39522


Results indicate an F1-score of 61% and 94% for classes 0 (default) and 1 (repayment), respectively. While these results are acceptable, there are opportunities for improvement through future work.

## Future Work

1. **Feature Engineering:** Explore additional features or transformations to enhance model understanding and predictive power.

2. **Model Architecture:** Experiment with different deep learning architectures to improve overall performance.

3. **Threshold Optimization:** Investigate the impact of the threshold (currently set at 0.5) on model performance by examining AUC and ROC curves. Adjust the threshold for optimal results.

4. **Hyperparameter Tuning:** Conduct grid search to fine-tune hyperparameters such as learning rate (alpha) for improved model generalization.

5. **Documentation:** Provide detailed documentation on data preprocessing, model architecture, and evaluation metrics for future reference.

Feel free to adapt and expand upon this README to provide additional context and details about your project.
