# The Lending Club
## Problem Domain
Finance/Banking
## Problem Statement
You work for a consumer finance company which specializes in lending various types of loans to urban customers.

* Data engineering team should clean the data so the other team can use them.
* Should also calculate risk score on which company can approve or disapprove the loan request.

This is important for the following two reasons:

* If the applicant is likely to pay, but the company disappropves, then it's a business loss for the company.
* If the applicant is unlikely to pay, but the company approves, then it's a financial loss to the company.

## Dataset Used
* The lending club dataset (1.7 gb), 1 csv file, 118 columns and 2+ million records.
* [Link to the data source]
  <https://www.kaggle.com/datasets/wordsforthewise/lending-club/>
## Data Source Mock Up
* In real world, the fintech dataset is generally large, and have multiple files. In order to simulate that, I have divided the single csv file, into the following datasets:
  * customers
  * loans
  * loan repayments
  * loan defaulters
* Data is in the CSV format.
## Data Preprocessing
The raw data in each csv file is processed and cleaned. Some cleaning strategies applied are:
* Changing the columns to suitable datatype
* Renaming columns
* Removing null values
* Removing duplicates
* Adding ingestion date
  
The cleaned data is stored to the output folder using the dataframe writer API in csv and parquet format.
## Data Processing
* Created external tables for each type of data, so that the other team can use them.
* Created a view that gave a single overview of complete loans data.
* Created a table for the single overview of complete loans data.
* Calculated loan scores using loan repayment history, loan defaulters history, and customer's financial health data.
