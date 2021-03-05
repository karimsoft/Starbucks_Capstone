# starbucks_capstone

## Project Description
Starbucks Offer Dataset is one of the datasets that students can choose from to complete their capstone project for Udacity’s Data Science Nanodegree. The dataset contains simulated data that mimics customers' behavior after they received Starbucks offers. The data is collected via Starbucks rewards mobile apps and the offers were sent out once every few days to the users of the mobile app.


    The program used to create the data simulates how people make purchasing decisions and how those decisions are influenced by promotional offers.
    Each person in the simulation has some hidden traits that influence their purchasing patterns and are associated with their observable traits. People produce various events, including receiving offers, opening offers, and making purchases.
    As a simplification, there are no explicit products to track. Only the amounts of each transaction or offer are recorded.
    There are three types of offers that can be sent: buy-one-get-one (BOGO), discount, and informational. In a BOGO offer, a user needs to spend a certain amount to get a reward equal to that threshold amount. In a discount, a user gains a reward equal to a fraction of the amount spent. In an informational offer, there is no reward, but neither is there a requisite amount that the user is expected to spend. Offers can be delivered via multiple channels.
    The basic task is to use the data to identify which groups of people are most responsive to each type of offer, and how best to present each type of offer for yesr 2018 ic complet offer.


## Main Files: Project Structure
```
├── data          
|   ├── portfolio.json
|   ├── profile.json
|   └──transcript.json
|
├── README.md
|
├── Starbucks_Capstone_notebook.ipynb 

```

Datasets

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

The *data* folder contains the 3 datasets provided by Udacity.

The *Starbucks_Capstone_notebook.ipynb* is where all the analysis is.

## Tech Stack
- **Python3** is the main language.
- **Numpy**, **Pandas**, **matplotlib**, **seaborn**, and **sklearn** are the main packages that were used.
- **Jupyter Notebook** is where the code is hosted.

## Author and Acknowledgement

- Linda Chen is the only author of this project.

- Starbucks provided this dataset.

- [Udacity](https://www.udacity.com/) provided this Data Science Nanodegree Program and the access to this dataset.
