# ST558-Project-2-Exploratory Data Analysis-Food Nutrients Analysis

![Food API Analysis](/docs/assets/img/food-API.jpg)

## Goal of the project and interesting findings.

Our goal with this project was to create a **vignette** about contacting an Food API using functions we have created to 
query, parse, and return well-structured data. We then usef our functions to obtain data from the API and do some exploratory data analysis. This was a group project
and I worked on this project with **Magaritte Nguyen**. We retrieved data from an [API](https://spoonacular.com/food-api/docs). 

We will use a function that connects with `complexSearch`, which is an end point of the API search. It returns a list of lists containing recipe names and other variables of interest that have default values or can be user defined. The user may either enter the type of cuisine, recipes with a specific ingredient, number of recipes to output based on modifications provided, type of diet, and protein range. We have another function that can retrieve the data for multiple cuisines specified by the user as well. We have a third function which can also be used to contact other endpoint of the API, `findByNutrients` to get all the recipes based on carbohydrate content. After, receiving the data we performed **data cleaning** in which we converted the data into usable format and performed **data analysis** on this modified data. We the **visualized** the data to understand the relationship between two variables or parameters of the data.

Some interesting findings for our specific vingette examples:
- Some vegetarian recipes are vegan as well
- Most of the unhealthy food recipes are from the **Foodista** source
- Recipes suggested by **Foodista** has the **maximum number** of **expensive** recipes, but also suggests **maximum number** of **inexpensive** recipes
- **Cinnamon French Toast Sticks** has a higher protein content than a non vegetarian meals like the **Turkey Burgers with Slaw**, even though it is a vegetarian recipe. This is surprising, but also makes sense due to the high protein content in eggs
- It can be seen that the number of **American** cuisine recipes are much **higher** in comparison to **Chinese** and **Latin American** cuisines for our vignette for the recipes containing fruit.
- The protein content in non vegetarian meals in generally much greater than the protein content in vegetarian meals as expected
- When broken down by serving, the protein content in vegetarian meals (for some) have a higher protein content then the non vegetarian meals
- There is **no real pattern** to be observed between carbohydrates and protein
- The regression line basically has **No change** in protein (g) at any amount of carbohydrates, confirming out plot that is only a scattet plot between protein and carbohydrates

## Most difficult part of the logic and programming.

In this project, we were required to select one API from a list of **5** APIs. As a food enthusiast, my first choice was unquestionably a food API. However, when I 
attempted to explore the API, I discovered that it was a very complex API with **lists of lists** being returned for certain API calls. It was extremely difficult to
narrow down the endpoints to be considered for our project; however, we will obtain some useful data for further processing and analysis. After much deliberation, 
we settled on a `complexSearch` and `findByNutrients` endpoints that contain information about the nutrients in the recipes as well as prices. Also, we had access to
trial version of the API and this limited our API calls and which sometimes delayed our work because we exhausted that limit during our initial project days. 

Summary statistics were among the most difficult part of the logic for programming because the data received from the API calls was not clean and we needed to use 
functions like `pivot wider()`, `transpose()`, and`sapply()` to create a tibble that we could summarise. It tested our logical abilities to see which parameters 
could be used as categorical variables to produce a good contingency table or **best explain** the relationship between the variables.

## What you would do differently?

We spent a lot of time finalizing the API endpoints because we didn't focus on reading the documentation and instead focused on reading and analyzing API calls to various endpoints and then deciding. In the future, I plan to thoroughly **read the API documentation to save time spent on trial and error**. In addition, I will keep a separate **list of categorical and quantitative variables** to make plotting easier and faster. As previously stated, we were both attempting to use the main branch for commits, which resulted in multiple merge conflicts. In the future, we will use **different branches** to commit our changes and raise a pull request to merge it with the main branch, which will **make teamwork easier**.

[Link to HTML document of the project 2](https://suyogd9.github.io/README1.html)

[Link to the vignette page of the project 2](https://pages.github.ncsu.edu/sdharma2/ST558_Project_2_C/)

[Link to Project 2 github repo](https://github.ncsu.edu/sdharma2/ST558_Project_2_C)
