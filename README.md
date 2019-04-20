Table of Contents
=================
   * [nycflights13](#nycflights13)
   * [Lahman batting data](#lahman-batting-data)
   * [Historical Product Demand](#historical-product-demand)


# nycflights13
One of the dataset used in book [R for Data Science](https://github.com/hadley/r4ds).
```r
if (!require('Lahman')) install.packages('Lahman'); library('Lahman')

batting = as_tibble(Lahman::Batting)
write.csv(batting, 'Lahman_batting.csv', row.names=FALSE)
```

# Lahman batting data
One of the dataset used in book [R for Data Science](https://github.com/hadley/r4ds).
```r
if (!require('nycflights13')) install.packages('nycflights13'); library('nycflights13')

write.csv(flights, 'nycflights13.csv', row.names=FALSE)
```

# Historical Product Demand
Link: https://www.kaggle.com/felixzhao/productdemandforecasting/data  
Purpose: time series analysis


