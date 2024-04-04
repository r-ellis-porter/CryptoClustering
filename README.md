# CryptoClustering

## Overview/Purpose

The CryptoClustering project aims to use unsupervised learning techniques, specifically K-means clustering, to predict if cryptocurrencies are affected by 24-hour or 7-day price changes. By clustering cryptocurrencies based on their price change patterns, we can gain insights into how they behave in the market and potentially identify groups of cryptocurrencies with similar price dynamics.

## Summary

The project follows a systematic approach to analyze cryptocurrency market data and perform clustering using both original features and principal component analysis (PCA). The main steps include:

1. **Data preprocessing:** Loading the cryptocurrency market data, normalizing it using StandardScaler, and preparing the data for analysis.
2. **Finding the optimal number of clusters (k) using the elbow method:** This involves iterating through different values of k and selecting the one that minimizes the inertia, which measures the within-cluster sum of squared distances.
3. **Clustering cryptocurrencies using K-means:** Initializing and fitting the K-means model with the optimal number of clusters found in the previous step, then predicting cluster labels for the cryptocurrencies.
4. **Performing PCA:** Applying PCA to reduce the dimensionality of the data while preserving as much variance as possible.
5. **Finding the optimal k value with PCA data:** Similar to step 2, finding the optimal number of clusters using PCA-transformed data.
6. **Clustering cryptocurrencies using PCA data:** Using the optimal k value obtained from PCA, clustering the cryptocurrencies and visualizing the results.

## Important Findings

- The optimal number of clusters (k) determined using the original data was found to be 4, both visually and based on inertia values.
- PCA revealed that about 89.5% of the total variance could be explained by the first three principal components.
- The best value for k using PCA-transformed data was also 4, indicating consistency with the findings from the original data.
- Visualizing the clusters obtained from both approaches showed distinct groupings of cryptocurrencies based on their price change patterns.

## Screenshots

- **Elbow Curve Comparison**
- **Cluster Visualization Comparison**

## Technical Details

### Requirements

- Python 3.x
- Jupyter Notebook
- pandas
- scikit-learn
- hvplot

### Running the Code

1. Clone the repository to your local machine.
2. Install the required dependencies using `pip install -r requirements.txt`.
3. Open the Jupyter Notebook `Crypto_Clustering.ipynb`.
4. Execute each cell in the notebook sequentially to run the code.

## Conclusion

The CryptoClustering project demonstrates how unsupervised learning techniques can be used to gain insights into cryptocurrency market dynamics. By clustering cryptocurrencies based on their price change patterns, we can identify distinct groups that may exhibit similar behaviors in the market. This information can be valuable for investors, traders, and analysts looking to make informed decisions in the cryptocurrency space.
