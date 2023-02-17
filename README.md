# Project-3-Machine-Learning----PWDK
Prediction apartment price in korea from kaggle data 


# ***Apartment Data in Korea***
### Data source : https://www.kaggle.com/datasets/gunhee/koreahousedata
### by : GUNHEE PARK 
### years : 2018

### **Contents**




1. Business Problem Understanding
2. Data Understanding
3. Data Preprocessing
4. Modeling
5. Conclusion
6. Recommendation

**Context**

Apartments are one of the answers to the housing needs of modern society due to limited residential land and dense business activities in urban areas. Therefore, it will be very interesting to examine apartment prices influenced by various internal and external factors. 

**Problem Statement**

Individuals or companies usually make apartment (unit) offers. Apartment owner can sell units on a platform by determining their apartments’ prices. If the price is too high compared to the market price, it will certainly be difficult to make sales. Conversely, if it is too low, the owner will find it difficult to get maximum profit.

**Goals**

The goals is to predict the apartment's prices based on provided data, therefore apartment owners could determine the suitable price for their apartment and the bidders could afford the appartment with fair price both for bidders and sellers (make the best machine learning with least error)

**Analytic Approach**

We will use the features (all other information unless sales prices) on provided data to predict the prices for each apartment by using machine learning algorithm. Finally, we will build the regression model to predict apartment prices with least error.

**Metric Evaluation**

There are 4 common metrics used for regression (MAE,RMSE,MAPE,MSE). And for this case we will use MAE, RMSE and MAPE. MSE is not used since it is harder to interpret and it could be represented by RMSE. 


**Conclusion**
1. The MAE metrics (₩ 36.690) of this model still need to improve since the MAE value is higher than the lowest sale price in dataset (₩ 32.743). It means that lowest data will assumed have ₩ 0. Suggest not to used this metrics if the apartment value is low (< ₩ 100.000)
2. The MAPE metrics (18.61%) of this model could be used for all range price of apartment but in the downside value that is overesimated (prediction higher than actual) will causing MAPE value is more significant than error in underestimated value
3. The RMSE metrics (47000.644) of this model tends higher than MAE metrics due to outliers data that is used as fitting data for machine learning
4. R square metrics define that based on this model, 80% variance of target already representated by the current features
5. Machine learning model tends to be heteroscadsticity (good when predict low apartment sale price < ₩ 100.000 and getting worse when predict apartment with high sale price)

**Recommendation**

To improve accuracy of this model, I suggest to separate the data into 3 different machine learning based on feature importance for example make specified machine learning for HallywayType 'Terrace','Corridor' and 'Mixed'. Hopefully by fragmanted the data could make the data more similar (same characteristics and less outlier). Therefore, the machine could predict more accurate
