# ST558-Project-3-Project-3-Creating predictive models and automating markdown reports - Online News Popularity Prediction

## Goal of the project

The goal of this report is to create and compare predictive models using [Online News Popularity](https://archive.ics.uci.edu/ml/datasets/Online+News+Popularity) data from the UCI Machine Learning Repository. This was a group project and I worked on this project with **Bennet McAuley**. 

## What would you do differently?

**Variable selection** is an important aspect of predicting using different models. I am currently using **`regsubsets()`** to select the best variables to use.  to accommodate various models For selecting the best variable, I use the 'Rsquared' value. I believe I could have investigated other techniques for variable selection, such as **`Principal Component Analysis`** for feature extraction, **`Lasso`** regression, which is a **`L1 regularization`** technique, and correlation tests such as `ANOVA test`, `Pearson Correlation Coefficient`, and `Chi-Square Test`.

For the current data set, the response variable is count data, and I could have tried different `weight distributions` while training and getting a model fit. My theory is that it would have produced better results.

Random Forest implementation was a bit **computationally heavy**, and I will try to find a way to **dynamically assign** the resources to memory intensive model techniques. I would like to look into some libraries that can help me understand and optimize the memory usage of fitting a model.

## what was the most difficult part for you?

## what are your big take-aways from this project?
