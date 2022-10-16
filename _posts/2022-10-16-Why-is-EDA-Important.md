# Why is EDA important?

## What is EDA and what are the overall goals of the EDA?

Exploratory data analysis is used to thoroughly examine the data. EDA is used to discover what data can **reveal beyond** the formal modeling or hypothesis task 
and to gain a better understanding of the data. It also assists us in determining whether the statistical techniques considered for the data are appropriate. 
EDA aids in `maximizing data insights`, `identifying key variables`, and `selecting the best factor settings`. The goal of EDA is to it will help you **highlight important 
things** in the dataset. EDA can be defined as an attitude/philosophy about how a data analysis can be carried out.

## Important methods for EDA...

EDA can be carried out in a variety of ways, each with its own set of benefits. According to me, there are a few things that are critical in EDA and should be
completed before beginning any data analysis. To begin, I believe we should **look for missing values** in the datasets and handle them using `linear interpolation` or
`imputation`. We can plot a graph for the percentage of missing values in each feature and either **eliminate the feature** with the most missing values if it is not 
important for future analysis or **replace the missing values** using the methods described above. Then, to aid in data visualization in the future, we must categorize our 
features/variables as `discrete`, `continuous`, or `categorical`. It is critical to understand the distribution of the data. We can understand the shape of your features 
by using **Probability Density Functions (PDFs)** and **Probability Mass Functions (PMFs)**, with PMFs used for discrete features and PDFs for continuous features. 
Finding **correlations between variables or features** is an important aspect of data analysis, which can be accomplished using a `scatter plot` or the generation of a 
`correlation matrix`. Multivariate chart, which is a graphical representation of the relationships between factors and a response. Finding outliers in data is critical 
because they can skew our predictions and cause major issues when performing statistical tasks after EDA. **Box plot visualization** can help identify these outliers. 
We can gain more information and knowledge about our data and perform a better EDA by using these methods.

## Things I lookout for during EDA...

EDA is used to determine how to best manipulate data to get the `answers you need`, `discover patterns`, `spot anomalies`, `test a hypothesis`, or `check assumptions`. The 
first thing I do after receiving the data is look at the **size of the data**, **the number of rows and columns**, and decide which **IDE or software** can be used 
to work on this data. Jupyter notebook, for example, may be incapable of handling large amounts of data, necessitating the use of visual studio code or R studio. Identifying 
missing data is important because it can lead to bias. We can replace the data by using the mean or median of the feature and linear interpolation if the feature is important 
for the dataset. I try to **categorize the features or variables** at the start of EDA because it will aid us in data visualization during EDA. Learning about the distribution 
allows us to better understand the nature of the data, such as whether it exhibits a distinct behavior that occurs at regular intervals or a positive or negative trend 
over time. We can understand this distribution using the methods described above, `PDF or PMF`. This allows us to determine whether the data is `skewed`, `multimodal`, or 
`disconnected`. Correlation between variables helps us understand that if one feature is dependent on others, we can use this knowledge when analyzing the data. Outliers 
deviate substantially from other samples in your dataset and can cause serious issues while carrying out statistical activities in accordance with your EDA. It's crucial 
to identify these outliers, and box plot visualization can help with that. You can test presumptions about a dataset using a variety of exploratory data analysis (EDA) 
approaches. These include the normal probability plot, histogram, run sequence plot, and lag plot. Many statistical methods **assume** the existence of the data being 
examined, hence EDA is crucial to these methods. EDA is crucial because it enables data scientists to examine the data before drawing any conclusions.
