# Census Data Vizualization

![Population](/docs/assets/img/population.png)

As part of our ST-558 coursework, we read census data and plotted variation in enrollment value/population for different years and states. 
Rstudio was used as a development tool, and the entire project was written in R. This blog post will include my project learnings and what 
changes I would have made to the project and overall process.

## Data processing

The data required for the project was obtained the census bureau in the form of csv files. In the data processing part I learned about how to read the data from csv files into a tibble, which can be further used for processing. During the data processing, I got a better understanding of how to split a variable into multiple variable get more parameters for analysis. I also learned to extract and filter only important features from the tibble and how to format some varaibles for example date to make dataset more valuable while analysis. 
With technical point of view, I learned how to work with tidyverse library and use select(), mutate(), rename(), pivot_longer(), as.Date(), as.numeric(), substr() functions of R. 
