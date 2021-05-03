# Cryptocurrencies
Crypto currencies 



## Project Overview

The Crypto currencies project main purpose is to analyse and visualize the cryptocurrenices data for an investment portofolio and the data provided is grouped to create a classification system for this portfolio by using unspervised machine learning model. 

The project incliudes the PCA data and vissualisation through the 3D scatter. The created and cleaned data with a table of tradeable crypto currencies with a total of 532 was scaled to create the scatter plot of these tradeable cryptocurrencies. I further made a new data frame and visualized the same data through hvplot scatter.

We use the following methods for the analysis:

1. Preprocess the provided data 
2. Reduce the data dimension using Principal Component Analysis,
3. Clustering cryptocurrencies using K-Means,
4. Visualizing classification results with 2D and 3D scatter plots.




**
Click [here](https://github.com/josephthomas08/Cryptocurrencies/blob/main/crypto_clustering.ipynb) to crosscheck and verify  the code.**



## Resources
Python 3.7 in Jupyter Notebook
Libraries: pandas, numpy, path, counter
scikit-learn: StandardScaler, MinMaxScaler, PCA, KMeans
hvplot
ploty express
Data: crypto_data.csv from CryptoCompare



# Results 

Aftersubjecting data with preprocessing and cleaning phase we have a total of **532** tradable cryptocurrencies.

## Deliverable 1.0 - Preprocessing the Data for PCA

### D1.1.0 The following five preprocessing steps have been performed on the crypto_df DataFrame as part of Deliverable 1:

#### D1.1.1 Cryptocurrencies that are not being traded are removed 


<img width="754" alt="D1 1 1 Module 18" src="https://user-images.githubusercontent.com/75267605/116830007-71944d80-ab75-11eb-9c94-33cb2d9992a5.png">



#### D1.1.2 IsTrading column is dropped 



<img width="741" alt="D1 1 2 Module 18" src="https://user-images.githubusercontent.com/75267605/116830010-75c06b00-ab75-11eb-8c25-af8991ba385d.png">





#### D1.1.3 Rows with one >= one null value are removed 
  
<img width="662" alt="D1 1 3 Module 18" src="https://user-images.githubusercontent.com/75267605/116830014-7953f200-ab75-11eb-8864-71d887189ef7.png">
  

#### D1.1.4 Rows without coins being mined are removed 
	
	
<img width="797" alt="D1 1 4 Module 18" src="https://user-images.githubusercontent.com/75267605/116832290-74e20600-ab82-11eb-900f-95bd1cf266ac.png">

  
 
#### D1.1.5 CoinName column dropped 
	
<img width="807" alt="D1 1 5 Module 18 " src="https://user-images.githubusercontent.com/75267605/116832294-79a6ba00-ab82-11eb-80a5-ea21fa2bbf2e.png">
  
  
  
### D1.2 A new DataFrame is created that stores all cryptocurrency names from the CoinName column and retains the index from the crypto_df DataFrame 


<img width="638" alt="D1 2 Module 18" src="https://user-images.githubusercontent.com/75267605/116832296-7dd2d780-ab82-11eb-9f29-07b01ffc23ba.png">


### D1.3 The get_dummies() method is used to create variables for the text features, which are then stored in a new DataFrame, 


<img width="1022" alt="D1 3 Module 18" src="https://user-images.githubusercontent.com/75267605/116832298-83302200-ab82-11eb-87ff-72942c2d913a.png">





### D1.4 The features from the X DataFrame have been standardized using the StandardScaler fit_transform() function 


<img width="670" alt="D1 4 Module 18 " src="https://user-images.githubusercontent.com/75267605/116832301-87f4d600-ab82-11eb-9316-04272c13b7e6.png">



## Deliverable 2.0 - Reducing Data Dimensions Using PCA

### D2.1 The PCA algorithm reduces the dimensions of the X DataFrame down to three principal components 
<img width="644" alt="D2 1 Module 18" src="https://user-images.githubusercontent.com/75267605/116832560-66481e80-ab83-11eb-81f6-2d2460a9fd59.png">




### D2.2 The pcs_df DataFrame is created and has the following three columns, PC 1, PC 2, and PC 3, and has the index from the crypto_df DataFrame 
<img width="752" alt="D2 2 Module 18" src="https://user-images.githubusercontent.com/75267605/116832551-5cbeb680-ab83-11eb-9c76-f689919dd747.png">

	
	
	
	
## Deliverable 3: Clustering Crytocurrencies Using K-Means


### D3.1 An elbow curve is created using hvPlot to find the best value for K 
	
<img width="956" alt="D3 1 Module 18" src="https://user-images.githubusercontent.com/75267605/116832895-79a7b980-ab84-11eb-8a6b-361241ad5cca.png">




The result from the above graph show that the  best k value appears to be 4 so we can safely  conclude on an output of 4 clusters to categorize the crytocurrencies.






### D3.2 Predictions are made on the K clusters of the cryptocurrencies’ data 


<img width="744" alt="D3 2 Module 18" src="https://user-images.githubusercontent.com/75267605/116832899-7e6c6d80-ab84-11eb-90e0-26fd864b5fc6.png">


	


### D3.3 A new DataFrame is created with the same index as the crypto_df DataFrame and has the following columns: Algorithm, ProofType, TotalCoinsMined, TotalCoinSupply, PC 1, PC 2, PC 3, CoinName, and Class 



<img width="809" alt="D3 3 Module 18 " src="https://user-images.githubusercontent.com/75267605/116832903-82988b00-ab84-11eb-8c08-ff3521820110.png">
	
	

## Deliverable 4: Visualizing Cryptocurrencies Results



### D4.1 The clusters are plotted using a 3D scatter plot, and each data point shows the CoinName and Algorithm on hover 




<img width="1015" alt="D4 1 Module 18 " src="https://user-images.githubusercontent.com/75267605/116833100-5df0e300-ab85-11eb-910b-36ee25f2055f.png">





### D4.2 A table with tradable cryptocurrencies is created using the hvplot.table() function 



<img width="1021" alt="D4 2 Module 18 " src="https://user-images.githubusercontent.com/75267605/116833104-60ebd380-ab85-11eb-914c-e37e83cc764c.png">





### D4.3 The total number of tradable cryptocurrencies is printed 


<img width="494" alt="D4 3 Module 18 " src="https://user-images.githubusercontent.com/75267605/116833107-647f5a80-ab85-11eb-8bca-d9c3d04a7e19.png">





### D4.3 A DataFrame is created that contains the clustered_df DataFrame index, the scaled data, and the CoinName and Class columns 


<img width="556" alt="D4 4 Module 18" src="https://user-images.githubusercontent.com/75267605/116833110-6812e180-ab85-11eb-9b5d-5affef50322c.png">




### D4.3 A hvplot scatter plot is created where the X-axis is "TotalCoinsMined", the Y-axis is "TotalCoinSupply", the data is ordered by "Class", and it shows the CoinName when you hover over the data point 


<img width="1014" alt="D4 5 Module 18 " src="https://user-images.githubusercontent.com/75267605/116833113-6ba66880-ab85-11eb-8875-2db4315b7742.png">





# Summary

We were able to identify classification of **532** cryptocurrencies based on similarities of their features.
We will need to further understand and  analyze features of each group  to further determine their performance and potential interest for the investment bank's clients.







