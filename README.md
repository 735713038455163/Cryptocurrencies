# Cryptocurrencies
 
# Machine Learning

# Overview of Project

Here is the list of deliverables:

- Deliverable 1: Preprocessing the Data for PCA
- Deliverable 2: Reducing Data Dimensions Using PCA
- Deliverable 3: Clustering Cryptocurrencies Using K-means
- Deliverable 4: Visualizing Cryptocurrencies Results


Specifically,

The files we will be using are the crypto_clustering1.ipynb , crypto_data.csv with Jupyter Notebook Libraries: pandas, hvplots.pandas, ployly.express, and scikit-learn 

# Purpose:
Using unsupervised machine learning on cryptocurrency , to process data, cluster, reduce dimensions, and reduce the principal components using PCA. 

# Results:

The following five preprocessing steps have been performed on the crypto_df DataFrame:

- All cryptocurrencies that are not being traded are removed

![D1](https://github.com/735713038455163/Cryptocurrencies/blob/master/Pictures/D1.PNG)

- The IsTrading column is dropped

![D1a](https://github.com/735713038455163/Cryptocurrencies/blob/master/Pictures/D1a.PNG)

line 2-18 in the crypto_clustering1.ipynb have the following:
- All the rows that have at least one null value are removed 
- All the rows that do not have coins being mined are removed 
- The CoinName column is dropped
- A new DataFrame is created that stores all cryptocurrency names from the CoinName column and retains the index from the crypto_df DataFrame

Finally,

![D1b](https://github.com/735713038455163/Cryptocurrencies/blob/master/Pictures/D1b.PNG)

- The get_dummies() method is used to create variables for the text features, which are then stored in a new DataFrame, X 
- The features from the X DataFrame have been standardized using the StandardScaler fit_transform() function 


- The PCA algorithm reduces the dimensions of the X DataFrame down to three principal components
 
![D2](https://github.com/735713038455163/Cryptocurrencies/blob/master/Pictures/D2.PNG)

- The pcs_df DataFrame is created and has the following three columns, PC 1, PC 2, and PC 3, and has the index from the crypto_df DataFrame 


- The clusters are plotted using a 3D scatter plot, and each data point shows the CoinName and Algorithm on hover
 
![D3](https://github.com/735713038455163/Cryptocurrencies/blob/master/Pictures/D3.PNG)

- A table with tradable cryptocurrencies is created using the hvplot.table() function 

- The total number of tradable cryptocurrencies is printed 

![D3a](https://github.com/735713038455163/Cryptocurrencies/blob/master/Pictures/D3a.PNG)

- A DataFrame is created that contains the clustered_df DataFrame index, the scaled data, and the CoinName and Class columns 
- A hvplot scatter plot is created where the X-axis is "TotalCoinsMined", the Y-axis is "TotalCoinSupply", the data is ordered by "Class", and it shows the CoinName when you hover over the data point

![D3b](https://github.com/735713038455163/Cryptocurrencies/blob/master/Pictures/D3b.PNG)


# Key Takeaways
- Describe the differences between supervised and unsupervised learning, including real-world examples of each.
- Preprocess data for unsupervised learning.
- Cluster data using the K-means algorithm.
- Determine the best number of centroids for K-means using the elbow curve.
- Use PCA to limit features and speed up the model.
