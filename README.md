# Mobile App Recommendation Mechanism

This repository includes my participation in the ["Machine Learning Challenge for Young Talents"](https://www.kaggle.com/competitions/turkiye-is-bankasi-ml-challenge-5/overview) organized on Kaggle. The goal is to develop an artificial intelligence model that recommends the most needed menu for each user by working on the usage data of a mobile application.

## Data Set

- **train_final.parquet**: Training data set containing usage data from October/November/December 2022.
- **test_final.parquet**: Test data set containing usage data from January 2023.
- **submission_sample_final.parquet**: Sample submission file with the correct format.

## Data Set Descriptions

- **ID**: Masked customer ID.
- **MONTH**: Month of the transaction.
- **N_SECONDS_[*]**: Time spent in menus (given in target order).
- **CARRIER**: Phone carrier for the transaction.
- **DEVICEBRAND**: Brand of the device for the transaction.
- **FEATURE_[*]**: Masked features representing customer-specific data.
- **TARGET**: Top 3 menus that the customer spent the most time on in a specific month.

## Solution Explanation

In this solution, the CatBoost algorithm was used, and model parameters were optimized using the `study` function of CatBoost. External data such as periodic inflation data, salary payment days, official and religious holiday data, exchange rates, and average temperature data according to the season in the country were used.


## Installation

To run the project locally:

1. Clone this repository.
2. Create a virtual environment compatible with Python 3.x.
3. Install the necessary dependencies in Notebooks (pip install catboost study).

