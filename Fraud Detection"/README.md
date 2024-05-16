## **Introduction**
This project aims to detect fraudulent transactions related to money laundering in the banking
sector. This project seeks to fill this gap by producing a data-driven solution to combat money laundering in banking and enhance economic security measures. This will be achieved by employing machine learning algorithms to train on an existing dataset containing global money laundering transactions, with the goal of detecting future transactions that are likely part of money laundering activities.
## **Data Collection**
The collection of data for this project adhered to AI and Data Science ethical considerations. Data was voluntarily provided by an associate employed at JPMorgan Chase in September 2023. Data was received upon the submission of a signed Memorandum of Understanding (MoU) to the associate via email. The received dataset is a synthetic banking dataset with 1,484,536 rows and 11 columns. The columns contain information about transaction types, sender information, beneficiary information, the USD amount, and the timestamp. As the project aims to detect fraudulent transactions related to money laundering, the following columns are the key targets:
- Label: This is an indicator that flags transactions as money laundering.
- USD amount: The total amount of money being transferred to the beneficiary.
- Transaction type: Various types of sources/actions used to transact money.
