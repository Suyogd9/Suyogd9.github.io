# ST558-Project-3-Project-3-Creating predictive models and automating markdown reports - Online News Popularity Prediction

![Online News Predictions](/docs/assets/img/onlineNews.png)

## Goal of the project

The goal of this report is to create and compare predictive models using [Online News Popularity](https://archive.ics.uci.edu/ml/datasets/Online+News+Popularity) data from the UCI Machine Learning Repository. This was a group project and I worked on this project with **Bennet McAuley**. 

## What would you do differently?

- **Variable selection** is an important aspect of predicting using different models. I am currently using **`regsubsets()`** to select the best variables to use.  to accommodate various models For selecting the best variable, I use the 'Rsquared' value. I believe I could have investigated other techniques for variable selection, such as **`Principal Component Analysis`** for feature extraction, **`Lasso`** regression, which is a **`L1 regularization`** technique, and correlation tests such as `ANOVA test`, `Pearson Correlation Coefficient`, and `Chi-Square Test`.

- For the current data set, the response variable is count data, and I could have tried different `weight distributions` while training and getting a model fit. My theory is that it would have produced better results.

- Random Forest implementation was a bit **computationally heavy**, and I will try to find a way to **dynamically assign** the resources to memory intensive model techniques. I would like to look into some libraries that can help me understand and optimize the memory usage of fitting a model.

- I could have also added a few interaction terms or polynomials terms to my models while training them in order to get better results. 

## what was the most difficult part for you?

- Inorder to get good predictions, selecting good predictors is really important. It was really difficult to come up with a way that can give me best predictors to fit my model. We had to select best predictors for our model from the 61 variables that are available in the data frame. We explored many techniques and decided to move ahead by using `regsubsets()` for variable selection.
- **`Automation`** was another diffidult part where in we had to generate multiple .md files for different data channel using the same render function. Also, rendering was taking long time and if we did simple mistake in the content writing we need to render it again.
- Finally, deciding on an `evaluation metric` was a difficult task because **`Rsquared`** value was too low to compare different models and **`RMSE`** value was too high, and I am not sure if we are using the correct metric for evaluation. However, because the response variable was **count** data, we were unable to find a better evaluation metric and are currently investigating different evaluation metrics for count data.   

## what are your big take-aways from this project?

- **`Exploratory Data Analysis`** is critical in determining which variables can be used while fitting the model.
- I discovered **`regsubsets()`** which is extremely useful in determining important predictors required for fitting a model when we have a large number of variables.
- **`Automation`** is very important because it allows you to repeat the steps on different subsets of the dataset without having to code separately for each subset.
- One should always be on the lookout for **`better ways`** to do something. For example, even if you find one method for determining the best predictors for a model, you should keep looking for other methods or libraries that may provide a **better** solution.

[Link to the vignette page of the project 3](https://suyogd9.github.io/ST558-Project-3/)

[Link to Project 3 github repo](https://github.com/Suyogd9/ST558-Project-3)
