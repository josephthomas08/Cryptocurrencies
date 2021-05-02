# Cryptocurrencies
Crypto currencies 


## Deliverable 1.0 Requirements

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



