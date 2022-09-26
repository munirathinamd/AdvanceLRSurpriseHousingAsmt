# Surprise House Sale Price Prediction
> A US-based housing company named Surprise Housing has decided to enter the Australian market. The company uses data analytics to purchase houses at a price below their actual values and flip them on at a higher price.

> The company is looking at prospective properties to buy to enter the market. Need to build a regression model using regularisation in order to predict the actual value of the prospective properties and decide whether to invest in them or not.


## Table of Contents
* Business Objective 
* Technologies Used
* Steps
* Conclusion
* Contact

<!-- You can include any other section that is pertinent to your problem -->

## Business Objective
The company is looking at prospective properties to buy to enter the market. Need to build a regression model using regularisation in order to predict the actual value of the prospective properties and decide whether to invest in them or not.

The company wants to know:

   - Which variables are significant in predicting the price of a house, and

   - How well those variables describe the price of a house.

   - Determine the optimal value of lambda for ridge and lasso regression.
Required to model the price of houses with the available independent variables. This model will then be used by the management to understand how exactly the prices vary with the variables. They can accordingly manipulate the strategy of the firm and concentrate on areas that will yield high returns. Further, the model will be a good way for management to understand the pricing dynamics of a new market.


## Technologies Used
- Numpy Version: 1.20.3
- Pandas Version: 1.3.4
- Matplotlib Version: 3.4.3
- Seaborn Version: 0.11.2
- The scikit-learn Version: 0.24.2.
- The statsmodels Version: 0.12.2.

<!-- You don't have to answer all the questions - just the ones relevant to your project. -->

## Steps
1) Import Libraries
2) Data Overview
3) EDA
    - Data Cleaning 
    - Missing Data Treatment
    - Remove Irrelevant Variables wrt both data and business use cases
    - Outliers Analysis and Treatments
    - Deriving columns
    - Univariate Analysis
    - Bivariate Analysis
    - Multivariate Analysis
4) Model Preperation
    - Training and Test data split
    - Feature Scaling - StandardScaler
    - Feature Engineering & Selection using RFE and Variance Inflation factor
    - Model preperation
    - Regularization Ridge & Lasso Regression Model
    - Residual Analysis
    - Model Evaluation & Assessment
    - Prediction 
    - Conclusion

<!-- You don't have to answer all the questions - just the ones relevant to your project. -->

## Conclusion
> ## EDA Analysis:

    - BsmtFullBath: 0 bathrooms are high and 1 bathroom seems to be second common value
    - BedroomAbvGr: 3 bedroom are high
    - FullBath: Mostly 2 bathrooms are full bathroom above grade
    - TotRmsAbvGrd: Mostly 6 rooms are above grade
    - Fireplaces: Houses with no fire places are more.
    - Except 'MoSold', 'BsmtUnfSF' and 'YrSold_Age' variables, all other continuous variables are related to the SalePrice
    - YearbuiltAge,YearRemodel_Age and garageYRBT_Age have negative correlation
    - Higher sales prize is for MSSubClass 20
    - House with Residential Low Density MSZoning has higher sales
    - House with Regular LotShape and Inside Lotconfig has higher sales
    - North Ames neighborhood has higher sales prize
    - Single-family Detached building type has higher sales
    - House in normal sale condition with Typical/Average kitchen quality, Excellent heating quality, Average/ Typical exterior quality has higher sale prize
    - House with average overall quality and condition have higher sales prize
    - House with attached Garage type and though its unfinished has higher sales prize
    - Basement with height of Typical (80-89 inches) and Good (90-99 inches) and No Exposure have highest sales prize
    - House with Poured Concrete and Cinder Block foundations has more sales
    - Significant Variables wrt Correlation with SalesPrice
        - Positively correlated variables: TotalBsmtSF,1stFlrSF,GrLivArea,FullBath,TotRmsAbvGrd,GarageCars,GarageArea
        - Negatively correlated variables: YearBuilt_age, YearRemodAdd_age,GarageYrBlt_Age

> ## Model Results:
    - Linear Regression (RFE)
        - R2 Score Train : 85.2% 
        - R2 Test Score : 81.36% 
        - RMSE test is 0.175
    -  Ridge Regression 
        - Optimal lambda value : 10
        - R2 Score Train : 92.27% 
        - R2 Test Score : 89.17% 
        - RMSE test is 0.133
    - Lasso Regression 
        - Optimal lambda value : .0002 
        - R2 Score Train : 92.64% 
        - R2 Test Score : 89.45% 
        - RMSE test is 0.131
    - Linear Regression (RFE) model has low R2 value in compare to Ridge Regression and Lasso Regression models.
    - In comparison to Ridge Regression, Lasso Regression model has minimal increase in R2 and can say Lasso Regression model is slightly better in compare to Ridge Regression.
    - Finally, we can consider Lasso Regression Model for housing Sales Prize predition
    - As per Lasso, top recommended features are as below
        - MSZoning_FV
        - MSZoning_RL
        - MSZoning_RH
        - MSZoning_RM
        - Neighborhood_Crawfor
        - Neighborhood_StoneBr
        - GrLivArea
        - Neighborhood_NridgHt
        - Exterior1st_BrkFace
        - Neighborhood_Somerst
        - Neighborhood_NoRidge





<!-- As the libraries versions keep on changing, it is recommended to mention the version of library used in this project -->

## Contact
Created by [@munirathinamd] - feel free to contact me!


<!-- Optional -->
<!-- ## License -->
<!-- This project is open source and available under the [... License](). -->

<!-- You don't have to include all sections - just the one's relevant to your project -->
