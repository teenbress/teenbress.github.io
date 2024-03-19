---
layout: post
title: "Bitcoin Trading Package"
subtitle: 'Bayesian Model for Trend Prediction'
date:       2018-01-03 12:00:00
author:     "Qiao Yu"
header-img: "img/post-bg-bitcoin-prediction.jpg"
catalog: true
tags:
    - Data Science
---

# Bitcoin Trading Prediction Packages
Predicting the price variations of bitcoin, a virtual cryptographic currency. These predictions could be used as the foundation of a bitcoin trading strategy. To make these predictions, I implemented the Bayesian Regression model to predict the future price variation of bitcoin as described in the reference paper. 
The main parts of the package to focus on are the optimization of Sample Entropy and the prediction of price.
**The package develops both R and Python version**. [**CODE**](https://github.com/teenbress/Bitcoin-Price-Prediction_Package/tree/master)

# Logics of the BitBay Packages 
1. Compute the price variations (Δp1, Δp2, and Δp3) for train2 using train1 as input to the Bayesian Regression equation. Make sure to use the similarity metric in place of the Euclidean distance in Bayesian Regression.

2. Compute the linear regression parameters (w0, w1, w2, w3) by finding the best linear fit. Here you will need to use the ols function of statsmodels.formula.api. Your model should be fit using Δp1, Δp2, and Δp3 as the covariates. 

3. Use the linear regression model computed in Step 2 and Bayesian Regression estimates, to predict the price variations for the test dataset. Bayesian Regression estimates for test dataset are computed in the same way as they are computed for train2 dataset – using train1 as an input.

4. Once the price variations are predicted, compute the errors, predicting accuracy, profit and  sell/buy price. Visualize the result with the result_plots function.

![Prediction for Bitcoin Price Variation](https://github.com/teenbress/BitBay_Package/blob/master/Prediction%20for%20Bitcoin.png)





