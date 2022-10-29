![Feature selection](/docs/assets/img/checklist.png)

# **Why Variable selection is important?**

**Feature selection** is a technique for **`reducing`** the number of features and thus the **`computational complexity`** of the model. We want to explain the data as simply as 
possible, so **redundant** predictors should be removed.Unnecessary predictors will introduce **`noise`** into the estimation of other quantities of interest. **Collinearity** 
occurs when too many variables attempt to perform the same function. We can save time and/or money by not measuring redundant predictors if the model is to be used 
for prediction.The goal of feature selection is to build a model that **`accurately`** predicts or explains the relationships in the data.

# **Methods to determine variables for regression.**

The selection of variables is an **important** part of regression because a model with a large number of variables can lead to computational complexity. There are
several methods for determining the variable that will help our regression model predict accurately. Depending on the `number of variables`, `type of data`, and 
`EDA analysis`, I intend to use the following methods for variable selection.
 
## Hierarchial Models
  Firstly, we consider hierarchical models i.e the model with **higher order** terms and **lower order** terms.Lower order terms should not be removed 
  from the model before higher order terms in the same variable
  
  - **Polynomial Models**
    - Lower order terms **`should not be removed`** in the presence of higher order terms. As we do not want **interpretation** to be influenced by the scale used.
    
  - **Models with Interactions**
    - Simply removing the interaction term would result in a surface that is **`parallel`** to the coordinate axes. This is **`difficult`** to interpret and should be **`avoided`** unless a specific meaning can be attached.
      
## Stepwise Procedures

### **Backward Elimination**
   - In the first step of backward elimination, we **`include`** all predictors and continue to remove the one with the **highest p-value** (>.05 the threshold limit). It will produce the final set of features that are **significant** enough to predict the outcome with the **`desired accuracy after`** a few iterations.
   
### **Forward selection**
  - In forward selection, we simply keep adding features. We **`do not remove`** the previously added feature. We only add features that **improve** the overall model fit in each iteration.

### **Stepwise regression** 
  - The Stepwise regression technique begins by **fitting** the model with each individual predictor and determining which has the **lowest p-value**. Then choose that variable, and then fit the model using the two variables that we already chose in the previous step, one by one. Again, we choose the one with the lowest p-value. Keep in mind that by including the new variable, the **impact** of the **`previously selected`** variable in the previous step should remain **significant**. We repeat this process until we find a **combination** with a p-value less than.05.

## **Lasso Regression**
  - Lasso regression will **automatically** select useful features while discarding **`useless`** or **`redundant`** features. In Lasso regression, removing a feature causes its coefficient to **equal** 0.  The concept of using Lasso regression for feature selection is thus very straightforward, we fit a Lasso regression on a scaled version of our dataset and we only take into account those features that have a coefficient **`different from 0`**. To achieve the desired Lasso regression, we must first tune the **hyperparameter**.  That will enable us to quickly identify useful features and **eliminate** unnecessary ones.

# **Choosing a method for variable selection**

There is no hard and fast rule that you must use the methods specified above or the following sequence of methods to select the features. It is entirely dependent on the number of variables under **`consideration`**, **`collinearity of the variables`**, **`ease of use`**, **`reproducibility`**, and **`improved generalization`**.

- When there are many variables to consider, I use **`forward selection`** to determine the **best** feature. This is because it starts with null variables and considers only the variables that are useful, **avoiding** the need to consider the entire model.
- I use **`backward selection`** because it takes into account all of the effects of all variables at the same time. It aids us in comprehending **`collinearity`**.
- Except when there are **more** number of features than events, I favor using **`backward selection`**. Otherwise, we can use **`forward selection`**.
- The models are **`simple to understand`**, **`straightforward`** to use, and gives a **`reproducible and objective`** way to reduce the number of predictors when compared to manually selecting variables when we use **`stepwise regression`**.
- I like to use **`lasso regularization`** for feature selection since it **prevents overfitting** and may be used when there are more features than data. **`Inference and fitting`** are **quick**, and it **automatically** chooses the better features.
