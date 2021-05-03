# Cryptocurrencies
Crypto currencies 


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
	
<img width="956" alt="D3 1 Module 18" src="https://user-images.githubusercontent.com/75267605/116830608-76f39700-ab79-11eb-8403-bcdac682c815.png">





### D3.2 Predictions are made on the K clusters of the cryptocurrencies’ data 
	


<img width="681" alt="D3 2 Module 18" src="https://user-images.githubusercontent.com/75267605/116830612-7c50e180-ab79-11eb-84bb-39167237618a.png">

### D3.3 A new DataFrame is created with the same index as the crypto_df DataFrame and has the following columns: Algorithm, ProofType, TotalCoinsMined, TotalCoinSupply, PC 1, PC 2, PC 3, CoinName, and Class 
	
	
<img width="769" alt="D3 3 Module 18" src="https://user-images.githubusercontent.com/75267605/116830617-8246c280-ab79-11eb-9e1a-c27475cc90ad.png">

## Deliverable 4: Visualizing Cryptocurrencies Results



### D4.1 The clusters are plotted using a 3D scatter plot, and each data point shows the CoinName and Algorithm on hover 
### D4.2 A table with tradable cryptocurrencies is created using the hvplot.table() function 
### D4.3 The total number of tradable cryptocurrencies is printed 
### D4.3 A DataFrame is created that contains the clustered_df DataFrame index, the scaled data, and the CoinName and Class columns (5 pt)
### D4.3 A hvplot scatter plot is created where the X-axis is "TotalCoinsMined", the Y-axis is "TotalCoinSupply", the data is ordered by "Class", and it shows the CoinName when you hover over the data point (10 pt)





