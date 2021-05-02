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
  
  <img width="682" alt="D1 1 4  Module 18" src="https://user-images.githubusercontent.com/75267605/116830018-7d800f80-ab75-11eb-9ba0-bad343ad620e.png">
  
  
	#### D1.1.5 CoinName column dropped 
  
  <img width="951" alt="D1 1 5 Module 18" src="https://user-images.githubusercontent.com/75267605/116830022-81139680-ab75-11eb-8035-e402428f9b07.png">
  
  
### D1.2 A new DataFrame is created that stores all cryptocurrency names from the CoinName column and retains the index from the crypto_df DataFrame 


<img width="827" alt="D1 2 Module 18" src="https://user-images.githubusercontent.com/75267605/116830032-84a71d80-ab75-11eb-9c30-91c088ab8b5f.png">


### D1.3 The get_dummies() method is used to create variables for the text features, which are then stored in a new DataFrame, 


<img width="1118" alt="D1 3 Module 18" src="https://user-images.githubusercontent.com/75267605/116830038-8a046800-ab75-11eb-997a-e3ba3e0f92b9.png">


### D1.4 The features from the X DataFrame have been standardized using the StandardScaler fit_transform() function 

<img width="747" alt="D1 4 Module 18" src="https://user-images.githubusercontent.com/75267605/116830042-8f61b280-ab75-11eb-83c4-38afc353cfb6.png">


## Deliverable 2.0 - Reducing Data Dimensions Using PCA

	### D2.1 The PCA algorithm reduces the dimensions of the X DataFrame down to three principal components 
	
	<img width="728" alt="D2 1 Module 18" src="https://user-images.githubusercontent.com/75267605/116830431-e36d9680-ab77-11eb-9516-7ed56549ea95.png">



	### D2.2 The pcs_df DataFrame is created and has the following three columns, PC 1, PC 2, and PC 3, and has the index from the crypto_df DataFrame 
	
	
	<img width="897" alt="D2 2 Module 18" src="https://user-images.githubusercontent.com/75267605/116830433-ea94a480-ab77-11eb-93af-2c90586fca31.png">
	
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





