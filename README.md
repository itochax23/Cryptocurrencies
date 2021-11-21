# Cryptocurrencies
This project aims to create an analysis for clients who are preparing to get into the cryptocurrency market.

Martha is a senior manager for the Advisory Services Team at Accountability Accounting. Accountability Accounting, a prominent investment bank, is interested in offering a new cryptocurrency investment portfolio for its customers. The company, however, is lost in the vast universe of cryptocurrencies. So, they’ve asked you to create a report that includes what cryptocurrencies are on the trading market and how they could be grouped to create a classification system for this new investment.

The data Martha will be working with is not ideal, so it will need to be processed to fit the machine learning models. Since there is no known output for what Martha is looking for, she has decided to use unsupervised learning. To group the cryptocurrencies, Martha decided on a clustering algorithm. She’ll use data visualizations to share her findings with the board.

## Process
### Preprocessing the Data for PCA

```
# Use get_dummies() to create variables for text features.
crypto = pd.get_dummies(df_crypto['Algorithm'])
dummy = pd.get_dummies(df_crypto['ProofType'])
combined = pd.concat([crypto,dummy],axis =1)
X_df = df_crypto.merge(combined,left_index = True,right_index = True)
X_df = X_df.drop(['Algorithm','ProofType'],axis = 1)
X_df.head()
```

### Reducing data dimensions using PCA

<img src="https://github.com/itochax23/Cryptocurrencies/blob/7ba407da9f0b45c659bc90f82bd808c44307a72c/Resources/pca_2.png" width="70%" height="70%">

### Clustering Cryptocurrencies Using K-means
<img src="https://github.com/itochax23/Cryptocurrencies/blob/37324b4905e7bdf05b1c43de36706c7b7c25b4c4/Resources/bokeh_plot.png" width="70%" height="70%">

### Visualizing Cryptocurrencies Results
<img src="https://github.com/itochax23/Cryptocurrencies/blob/37324b4905e7bdf05b1c43de36706c7b7c25b4c4/Resources/newplot.png" width="70%" height="70%">
