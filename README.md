# HOUSE PRICE PREDICTION

A machine learning project to predict house prices using **Linear Regression** on the Ames Housing dataset.

## Overview

I use house features (size, number of rooms, quality, garage, year built, etc.) to predict the final sale price (`SalePrice`).


  ## Dataset
    - **Source**: Ames Housing dataset (very popular on Kaggle)
    - **train.csv** : 1,460 houses with known prices (used for training)
    - **test.csv** : 1,459 houses (prices to predict)
    - **Total features**: 80 columns (numeric + categorical)

## Tools & Libraries i used
    
    - Python
    - pandas : data cleaning & EDA
    - numpy
    - scikit-learn : Linear Regression model
    - matplotlib & seaborn : simple visualizations

## Project structure:

    house-price-prediction/
    ├── train.csv
    ├── test.csv
    ├── sample_submission.csv
    ├── house_price_prediction.ipynb
    ├── README.md                        ::: you're reading this!
    |── requirements.txt 
    |── data_description.txt 

# Data cleaning & preparation

    - Handled missing values: Filled with 'None' for categoricals , median/mode/0 for others
    - Removed outliers: Houses with GrLivArea > 4500 sq ft 
    - Log transformation: Created `SalePrice_log` = log(1 + SalePrice) to handle skewed prices
    - Encoding: One-hot for categorical features, mapped ordinal
    - Scaling: StandardScaler on features
    - Split: 80/20 train-test from train.csv

## How to run 
1. Install the libraries:

   ```bash
   pip install pandas numpy scikit-learn matplotlib seaborn jupyter

2. Open notebook:

    ```bash
    jupyter notebook house_price_prediction.ipynb
    
3. Run all cells from top to bottom
                   
## Current results:

    - Trained on 80% of train.csv, tested on 20%
    - RMSE (original price scale): ≈ 20k
    - R²: ≈ 0.927 

(Note: Results may vary slightly with random split.)

## What i plan to improve:

    - Use test.csv for real predictions
    - Try advanced models (Random Forest, ... )
    - Better missing value handling 

# What I Learned:
    - Understand workflow : load data, clean, explore, preprocess, model, evaluate
    - Dealing with real-world data (missing values,ordinal , skewness)
    - Why log-transform prices & scale features
    - Regression metrics like RMSE and R²

Last updated: February 2026
