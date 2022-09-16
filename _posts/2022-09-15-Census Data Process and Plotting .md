# Census Data Visualization

![Population](/docs/assets/img/population.png)

As part of our ST-558 coursework, we read census data and plotted variation in enrollment value/population for different years and states. 
Rstudio was used as a development tool, and the entire project was written in R. This blog post will include my project learnings and what 
changes I would have made to the project and overall process.

## Learnings from the project

### Data processing

The data required for the project was obtained the census bureau in the form of **.csv** files. In the data processing section, I learned how to read data from csv files into a tibble, which can then be processed. During the data processing, I learned how to split a variable into multiple variables to obtain more parameters for analysis. I also learned how to extract and filter only important features from the tibble, as well as how to format some variables, such as dates, to make the dataset more valuable while analyzing it. The project also helped me understand how to visualize the extracted data. We can reach inferences from these plots by comparing and contrasting the values of two different variables.

In terms of technology,  I learned how to work with tidyverse library and use `select()`, `mutate()`, `rename()`, `pivot_longer()`, `as.Date()`, `as.numeric()`, `substr()`, `summarise()` functions of **dpylr** package. Additionally, the project required us to create R programming functions. I discovered how to write a **function** with default and optional arguments. This reusable function cleans up the markdown by reducing the amount of redundant code. It also helped me to dig into **Regex** part for pattern matching in R programming. The project helped me write custom plot function to plot based on class. We exploited **UseMethod("plot")** to determine how the appropriate plotting function works.

### Data Visualization

I was able to draw some inferences about the data using customized plot functions by plotting variances in population and year for a specific division or state. For instance, I saw a dramatic decline in the enrollment mean for the Mid-Atlantic division and decided to investigate more to learn more about the unexpected drop. 

