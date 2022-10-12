# Exploratory Data Analysis - Food Nutrients Analysis

![Food API Analysis](/docs/assets/img/food-API.jpg)

## Goal of the project and interesting findings.

Our goal with this project was to create a **vignette** about contacting an Food API using functions we have created to 
query, parse, and return well-structured data. We then usef our functions to obtain data from the API and do some exploratory data analysis. This was a group project
and I worked on this project with **Magaritte Nguyen**. We retrievef data from an [API](https://spoonacular.com/food-api/docs). To demonstrate, we will be interacting with 
the Spoonacular Recipe and Food API. We are going to to build a few functions to interact with some of the endpoints and explore some of the data that we can retrieve 
for the Spoonacular API. To use a function that connects with `complexSearch` end point of the API. It returns a list of lists containing recipe names that 
include certain restrictions, the user may either enter the type of cuisine, Recipes with a specific ingredient, number of recipes to get based on cuisine and ingredient
provided, type of diet and protein range.Our function can retrieve the data for multiple cuisines specified by the user. There is another function which can be used 
by the user to contact other endpoint of the API `findByNutrients` to get all the recipes based on carbohydrate content.

Some of the interesting findings were as follows:-
  - The **American cuisine** has **highest number** of recipes with all the ingredients and protein range between 10-100. 
  - Our hypothesis was that Vegetarian recipes will have less protein but looking at protein content in vegetarian and non vegetarian recipes, but protein is **not non-existent** in vegetarian meals.
  - From the plot, interestingly enough, when broken down by serving, the protein content in vegetarian meals (for some) have a **higher protein content** then the non vegetarian meals.
  - After plotting scatter plot for proteins vs carohydrates, we could see that there is **no real pattern** to be observed here. A few points may indicate increase in either one is an increase 
  in the other but over all protein stays low no matter how the carbohydrates varies. 
  
## Most difficult part of the logic and programming..

In this project, we were required to select one API from a list of **5** APIs. As a food enthusiast, my first choice was unquestionably a food API. However, when I 
attempted to explore the API, I discovered that it was a very complex API with **lists of lists** being returned for certain API calls. It was extremely difficult to
narrow down the endpoints to be considered for our project; however, we will obtain some useful data for further processing and analysis. After much deliberation, 
we settled on a 'complexSearch' and 'findByNutrients' endpoints that contain information about the nutrients in the recipes as well as prices. Also, we had access to
trial version of the API and this limited our API calls and which sometimes delayed our work because we exhausted that limit during our initial project days. 
Summary statistics were among the most difficult part of the logic for programming because the data received from the API calls was not clean and we needed to use 
functions like 'pivot wider()', 'transpose()', and'sapply()' to create a tibble that we could summarise. It tested our logical abilities to see which parameters 
could be used as categorical variables to produce a good contingency table or best explain the relationship between the variables.
