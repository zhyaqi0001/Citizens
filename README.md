# Citizens

The dataset contains house sales information and 73 other features that may affect the house sales in three states RI, MA, PA. What I would to achieve is to predict the house sales between 10-01-2018 and 12-31-2018 using the information before 10-01-2018. Usually house sales are affected by a lot of factors and are not very predictable. But I would like to be able to capture the illusive correlations and make predictions.

The dataset was first split into subdatasets based on the state name. The reason was that the useful features contained for each state were different. 
Feature engineering was performed for the three subdatasets. The columns with high percetage of nans or containing a lot of unique values were dropped out from the dataset. Only one column was kept for the columns that were linearly related with each other. For numeric columns, the log transformation was performed and missing values was filled with the column mean. 

The training data was fit to the LightGBM model. 52% of the predicted house sales within 10% estimation error was achieved for house price predictions.
