# house_prices_predictino

Hier the houses price will be predicted on the base of some linear models and cat boost model.
The datasets and the task are taken from the kaggle competition House Prices - Advanced Regression Techniques.

The process is divided into several parts, each is contained in its own notebook.
1. data_manipulation/data_cleaning.ipynb clears data of null values on the basis of data_description.txt
    document and data analysis.

2. data_manipulation/data_manipulation.jpynb contains analysis which features could be important for the price prediction.
    Numeric features are analysed on the basis of the correlation value. Categorical features are chosen on the basis of CatBoosterRegressor. It is interesting, that one numeric feature was overlooked by correlation analysis, but proposed by CatBoosterRegressor.

3. data_manipulation/cat_booster_regression.ipynb is dedicated to use CatBoosterRegressor for unscaled data.
    R-squared (R^2): 0.8697

4. data_manipulation/linear_regression.ipynb contains a set of regressions such as LinearRegression, Hubert Regression, RANSAC and    Theil Sen Regression. RANSAC gave the best results.

5. data_manipulation/data_story_telling.ipynb would have to contain plots to describe important information about the data. For now it only writes the cleaned data with selected features to the file train_cleaned.csv which is used in Power BI.

6. power_bi/sales_story_telling.pbix contains some plots on the basis of cleaned train data.
