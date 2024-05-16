## **Introduction**
This project aims to detect fraudulent transactions related to money laundering in the banking
sector. This project seeks to fill this gap by producing a data-driven solution to combat money laundering in banking and enhance economic security measures. This will be achieved by employing machine learning algorithms to train on an existing dataset containing global money laundering transactions, with the goal of detecting future transactions that are likely part of money laundering activities.

## **Data Collection**
The collection of data for this project adhered to AI and Data Science ethical considerations. Data was voluntarily provided by an associate employed at JPMorgan Chase in September 2023. Data was received upon the submission of a signed Memorandum of Understanding (MoU) to the associate via email. The received dataset is a synthetic banking dataset with 1,484,536 rows and 11 columns. The columns contain information about transaction types, sender information, beneficiary information, the USD amount, and the timestamp. As the project aims to detect fraudulent transactions related to money laundering, the following columns are the key targets:
- Label: This is an indicator that flags transactions as money laundering.
- USD amount: The total amount of money being transferred to the beneficiary.
- Transaction type: Various types of sources/actions used to transact money.

## **The Dataset**
The dataset shows an imbalance with the target variable "label," where 21% of transactions are considered fraud, and 79% are not flagged as fraud. The dataset is considered unbalanced when there is a significant variance in the distribution of labels in terms of count.

## **Data Cleaning**
Data cleaning is a necessary step in Data Science as it aids model training and predictions by eliminating bad habits that the model may acquire from the noise in the data. Data was cleaned in two ways in this project. First, by checking for null values and replacing them with the mode. Null values were replaced with the mode because they were mostly found in categorical columns. Secondly, data was cleaned by checking for duplicates. The dataset did not contain any duplicates.
## **Data Resampling**
The distribution of the target variable indicates an imbalance in binary classification. To address this issue, the project employed data resampling, a technique used to balance the dataset through oversampling or undersampling. The project used a combination of oversampling and undersampling methods, specifically the Synthetic Minority Oversampling Technique (SMOTE) and Edited Nearest Neighbor (ENN).

## **Machine Learning Model**
Prior to model training and prediction, categorical variables in the dataset were converted to numerical using a label encoding function. This also assisted in determining the correlation of columns to the target column “label”. Using a feature selection, top ten features that are highly correlated to “label” were selected and used for model prediction.

## **Model prediction**
The project used a classification machine learning model called Random Forest. Random forest is suitable for both classification and regression problems. This machine-learning algorithm combines various decision trees to produce a more accurate and robust model. Random forest was chosen for its ability to handle large datasets with complex features (Rigatti, 2017). The obtained dataset is large, with over a million rows. The deployment of the ML model began by splitting the data into training and testing sets using a 70% to 30% ratio. The 70% was for training, and the remaining 30% was for testing the model's performance. Hyperparameter tuning was also applied to find the best fit for the model. Two hyperparameter tuning functions were used: grid search CV and random search CV, to ensure that the model avoids overfitting.
