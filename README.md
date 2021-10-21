# MACHINE LEARNING - UNSUPERVISED ASSIGNMENT - Cryptocurrency Clusters

## Background
* You are on the Advisory Services Team of a financial consultancy. One of your clients, a prominent investment bank, is interested in offering a new cryptocurrency investment portfolio for its customers. The company, however, is lost in the vast universe of cryptocurrencies. They’ve asked you to create a report that includes what cryptocurrencies are on the trading market and determine whether they can be grouped to create a classification system for this new investment.


* You have been handed raw data, so you will first need to process it to fit the machine learning models. Since there is no known classification system, you will need to use unsupervised learning. You will use several clustering algorithms to explore whether the cryptocurrencies can be grouped together with other similar cryptocurrencies. You will use data visualization to share your findings with the investment bank.

## Approach
We will be using Unsupervised Learning concepts to try and answer the problems and arive at an conclusion whether the clusters created from the unclassified data can help the clients group their newly planned cryptocurrency with its own group.

We have tried to solve this problem using the following steps:

### Step 1: Data Preparation
* Input file: `crypto_data.csv`
* The input file was read using `PANDAS`
* Filtered the input dataframe to showcase the cryptocurrenies which are being traded `'IsTrading' = True`
* Droped any row which had null values from the dataframe
* Filtered on the cryptocurrency that had total coins mined greater than zero `TotalCoinsMined > 0`
* Removed the columns `CoinName` and `IsTrading` columns
![cleansed1t](Images/cleansed1t.png)
* Used skLearn's `LabelEncoder` to create dummy variables/encodes for the `Algorithm` and `ProofType` columns
  * Used this approach instead of get_dummies() for simplification
![labelencoder](Images/labelencoder.png)
* Used skLearn's `StandardScalar` to standardize the data
![stdscalar](Images/stdscalar.png)
* This completes all the Data preparation activities
