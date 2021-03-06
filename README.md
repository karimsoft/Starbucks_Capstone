# starbucks capstone

## Project Overviewn
This is an in-depth data analysis and simulates data of how mobile app users respond to offers sent out by Starbucks. With a better understanding of customer behavior, Starbucks would be able to improve by promotional offers.

## Problem Statement
- What is the predict for event when have gender, age group, income group and offer type will complet offer or not in 20018 year ?
- What is the predict for most offer type in 20018 year ?
 
## Main Files: Project Structure
```
├── data          
|   ├── portfolio.json
|   ├── profile.json
|   └── transcript.zip >> transcript.json
|
├── README.md
├── Starbucks_Capstone_notebook.ipynb 
├── Starbucks_Capstone_notebook.html

```

## Data sets

portfolio.json (10 offers x 6 fields) - metadata for each offer (duration, type, etc.)

    id (str) - offer ID
    offer_type (str) - type of offer (BOGO, discount, informational)
    difficulty (int) - minimum required spend to complete an offer
    reward (int) - reward given for completing an offer
    duration (int) - time for offer to be open, in days
    channels (list[str]) - web, email, mobile, social

profile.json (17,000 users x 5 fields) - demographic data for each user

    age (int) - age of the customer (missing values are encoded as 118)
    became_member_on (int) - date when customer created an app account
    gender (str) - gender of the customer (some entries contain 'O' for other rather than 'M' or 'F')
    id (str) - customer ID
    income (float) - customer's income

transcript.json (306,534 transactions x 4 fields)- records for events (transactions, offers received, offers viewed, and offers completed)

    event (str) - record description (transaction, offer received, offer viewed, etc.)
    person (str) - customer ID
    time (int) - time in hours since start of test (the data begins at time t = 0)
    value - (dict) - either an offer ID or transaction amount depending on the record

## Table of Contents:

    Introduction:
        Data Viewing & Exploration
        Data Cleaning
    EDA Visualization
    Data Preprcessing
    Data Modeling

## Introduction

 ### Data Cleaning 
 ### Data Preprcessing

    Drop records with missing 
    Extract data from columns containing iterable data types (i.e. lists and dictionaries) into new columns
    Map ID hash strings to integers
    Recast columns to appropriate data types
 
 ### Data Modeling

    After pre-processing the dataset and after visualization the next part is to make a model that figure out whether the customer complet to offer or not.

    Here I used different types of models that will predict whether the customer complet to offer or not.

    To make a model we will split the data into  training and testing data.
 
    Target is the event predict complet offer or not and most offer type in 20018 year

The *data* folder contains the 3 datasets provided by Udacity.

The *Starbucks_Capstone_notebook.ipynb* is where all the analysis is.

## Tech Stack
- **Python3** is the main language.
- **Numpy**, **Pandas**, **matplotlib**, **seaborn**, and **sklearn** are the main packages that were used.
- **Jupyter Notebook** is where the code is hosted.

## Author and Acknowledgement

- [Udacity](https://www.udacity.com/) provided this Data Science Nanodegree Program and the access to this dataset.

- [medium](https://karimsoft.medium.com/karimsoft-starbucks-capstone-58821de875ac)
