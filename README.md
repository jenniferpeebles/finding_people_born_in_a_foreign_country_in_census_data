# Finding people born in a given foreign country in Census data
An R script for finding statistics about foreign-born people from a certain country in Census (American Community Survey) data using the Census API and tidycensus

This script uses the R programming language to find the numbers and percentages of the populations of the U.S., your state, your county, your MSA and/or your city who were born in a certain foreign country. 

### About the data

All data in this summary is from the 2019 5-year averages of the [American Community Survey](https://www.census.gov/programs-surveys/acs) done by the U.S. Census Bureau.

To use this script, you will need a free API key from the Census. You can [request one at this link](https://api.census.gov/data/key_signup.html).

ACS data is usually released about a year behind. ACS data for 2019 was released in calendar year 2020. Specifically, the 5-year ACS data is usually released in December, and the 5-year ACS data for 2019 was released in December 2020. 

The 5-year average data averages each metric over the previous five years to provide a less herky-jerky result than would be provided with annual data releases. Why do we use the 5-year average data? The Census Bureau only publishes 1-year data for the largest cities and counties in America. For everybody else, we have to use the 5-year data -- or nothing. 

ACS data is an estimate. The confidence interval is 90%. The Census Bureau publishes margins of error for each metric presented here. Always remember, the smaller the sample the estimate is taken from, the wider the margin of error. 

Much of the data in this summary specifically comes from ACS table B05006, [which you can read more about at here](https://censusreporter.org/tables/B05006/), "Place of Birth for the Foreign-Born Population in the United States." (If you are in Puerto Rico, you can check out table B05006PR_001, which is "Place of Birth for the Foreign-Born Population in Puerto Rico.")

### About this script

This script will retrieve data from the Census Bureau's online data repositories using the Census's Application Programming Interface (API) and the [tidycensus package](https://walker-data.com/tidycensus/) of the [R programming language](https://en.wikipedia.org/wiki/R_(programming_language)) written by Kyle Walker.

The script uses a number of R packages including the [tidyverse family of packages](https://www.tidyverse.org/) created by [Hadley Wickham](http://hadley.nz/) et al. Thank you to the brilliant people behind these packages who wrote all the code and keep it maintained. 

The summary the script produces, or can produce, uses the [knitr package](https://yihui.org/knitr/) and [R Markdown](https://rmarkdown.rstudio.com/index.html). The text in this README file, in the script and in the knitted summary has not been copy edited, so please forgive all typos and style errors. 

Like most of the code you'll find here on GitHub, this is a work in progress. As a relative newcomer to R, I'm sure there are more elegant ways to do many things I do here. All suggestions are welcome. 

