# Cryptocurrencies
## Overview 

This purpose of this project was to create an analysis for our client who is preparing to get into the cryptocurrency market, to do this we needed to analyze the dataset from many alternative cryptocurrencies to spot trends that make a firm or person want to invest in them. 

I noticed that the problem with cryptos is that the most common ones, like bitcoin or ethereum, are becoming unaffordable for the common public, with that being said, I will be using unsupervised machine learning to see if I can spot any trends that will produce results of opportunities of other affordable cryptos for my client.

## Results

### Preprocessing the Data for PCA
1.	Import data
2.	Keep all the cryptocurrencies that are being traded.
3.	Drop the IsTrading column.
4.	Remove rows that have at least one null value.
5.	Filter the crypto_df DataFrame so it only has rows where coins have been mined.
6.	Create a new DataFrame that holds only the cryptocurrency names, and use the crypto_df DataFrame index as the index for this new DataFrame.
7.	Remove the CoinName column from the crypto_df DataFrame since it's not going to be used on the clustering algorithm.

![delivarable1](https://github.com/backwater-graphics/Cryptocurrencies/blob/main/images/deliverable1.jpg)
---

### Reducing Data Dimensions Using PCA

1.	The PCA algorithm reduces the dimensions of the X DataFrame down to three principal components 
2.	The pcs_df DataFrame is created and has the following three columns, PC 1, PC 2, and PC 3, and has the index from the crypto_df DataFrame

![deliverable2](https://github.com/backwater-graphics/Cryptocurrencies/blob/main/images/deliverable2.jpg)
---

### Clustering Cryptocurrencies Using K-means

1.	An elbow curve is created using hvPlot to find the best value for K 
2.	Predictions are made on the K clusters of the cryptocurrencies’ data 
3.	A new DataFrame is created with the same index as the crypto_df DataFrame and has the following columns: Algorithm, ProofType, TotalCoinsMined, TotalCoinSupply, PC 1, PC 2, PC 3, CoinName, and Class 

![deliverable3](https://github.com/backwater-graphics/Cryptocurrencies/blob/main/images/deliverable3.jpg)
---

### Visualizing Cryptocurrencies Results

1.	The clusters are plotted using a 3D scatter plot, and each data point shows the CoinName and Algorithm on hover 
![deliverable4](https://github.com/backwater-graphics/Cryptocurrencies/blob/main/images/deliverable4.jpg)
---
2.	A table with tradable cryptocurrencies is created using the hvplot.table() function 
3.	The total number of tradable cryptocurrencies is printed 

![deliverable4.1](https://github.com/backwater-graphics/Cryptocurrencies/blob/main/images/deliverable4.1.jpg)
---

4.	A DataFrame is created that contains the clustered_df DataFrame index, the scaled data, and the CoinName and Class columns 
5.	A hvplot scatter plot is created where the X-axis is "TotalCoinsMined", the Y-axis is "TotalCoinSupply", the data is ordered by "Class", and it shows the CoinName when you hover over the data point 
![deliverable4.2](https://github.com/backwater-graphics/Cryptocurrencies/blob/main/images/deliverable4.2.jpg)
---

## Summary

This project I used unsupervised machine learning, which is used to discover patterns or groups of data when there is no known output. By using unsupervised machine learning it helped me to create an analysis that was successful at grouping cryptocurrencies into 4 groups. If I needed to create a crypto investment portfolio, I would need to further analyze the clusters that I discovered during this project. Regardless of this fact, I have a good starting point where I can see that the most profitable and known cryptos are somewhat in the 2 groups that have less supply and mined coins in comparison to others. These cryptos are Bitcoin and Ethereum. Based on what I see I recommend that they should keep look into cryptos with the innovations of technology where new altcoins are being created with very interesting value propositions.
