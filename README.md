# Housing Price Prediction

Predicting house sale prices on the Ames, Iowa housing dataset using regression models.

## Overview

An end-to-end machine learning pipeline for the classic Ames Housing regression
problem. The project walks through data cleaning, exploratory analysis, feature
engineering, and model comparison, with an emphasis on understanding *why* each
step is done rather than just running it.

## Data

This project uses the **Ames Housing** dataset from the Kaggle competition
[House Prices - Advanced Regression Techniques](https://www.kaggle.com/c/house-prices-advanced-regression-techniques).

The data is **not** included in this repository. To run the notebooks:

1. Download the competition data from Kaggle 
2. Place `train.csv` in the `data/` folder:
   ```
   data/train.csv
   ```

## Setup

```bash
git clone https://github.com/Jappieboef/housing-prediction-model.git
cd housing-prediction-model

pip install -r requirements.txt
```


## Approach

- **Missing values:** Distinguished structural absence (e.g. `NA` in `PoolQC`
  means "no pool") from genuinely missing measurements, and filled each
  accordingly — categorical absences with `"None"`, numeric absences with `0`,
  and true gaps with median/mode.
- **Target variable:** `SalePrice` is right-skewed, so it is log-transformed
  (`np.log1p`) for modeling, which makes errors proportional and the
  distribution closer to normal.

## Status

Work in progress.

- [x] Data loading and inspection
- [x] Missing value handling
- [x] Target variable analysis
- [X] Categorical encoding
- [X] Train/test split
- [X] Model training and comparison
