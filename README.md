# Information 
This is a project to demonstrate my analytical skills provided by ANZ Banking.Futhremore, the current project was created from the virtual intership program of the company.
# Code Samples
* Activating the libraries
```R
Registered S3 methods overwritten by 'dbplyr':
  method         from
  print.tbl_lazy     
  print.tbl_sql      
-- Attaching packages ------------------------------------------------------------------------ tidyverse 1.3.1 --
v ggplot2 3.3.5     v purrr   0.3.4
v tibble  3.1.4     v dplyr   1.0.7
v tidyr   1.1.3     v stringr 1.4.0
v readr   2.0.1     v forcats 0.5.1
-- Conflicts --------------------------------------------------------------------------- tidyverse_conflicts() --
x dplyr::filter() masks stats::filter()
x dplyr::lag()    masks stats::lag()
```
* Replacing 0 and 1 with False and True and replacing all NAs with 'Not Available'
```R
# 1 true and 0 false
# Moving to second column i need to take care of the NA values but i do not want to 
# miss 4000 observations from my dataset so i will replace NA WITH 'Not Available'
# After that i want to replace 0 and 1 with false and true

# Replacing 1 and 0 with true and false 

new <- as.logical(copied2$card_present_flag)

# Replacing NA with Not availableCopiedfile <- 
copied2 %>% replace_na(list(card_present_flag = 'Not Available'))
```

```R
glimpse(Copiedfile)
Rows: 12,043
Columns: 23
$ status            <chr> "authorized", "authorized", "authorized", "authorized", "authorized", "posted", "authorized",~
$ card_present_flag <dbl> 1, 0, 1, 1, 1, NA, 1, 1, 1, NA, NA, NA, 1, NA, NA, 1, NA, NA, NA, 1, 1, 0, 1, 0, 1, NA, NA, 1~
$ bpay_biller_code  <dbl> NA, NA, NA, NA, NA, NA, NA, NA, NA, NA, NA, NA, NA, NA, NA, NA, NA, NA, NA, NA, NA, NA, NA, N~
$ account           <chr> "ACC-1598451071", "ACC-1598451071", "ACC-1222300524", "ACC-1037050564", "ACC-1598451071", "AC~
$ currency          <chr> "AUD", "AUD", "AUD", "AUD", "AUD", "AUD", "AUD", "AUD", "AUD", "AUD", "AUD", "AUD", "AUD", "A~
$ long_lat          <chr> "153.41 -27.95", "153.41 -27.95", "151.23 -33.94", "153.10 -27.66", "153.41 -27.95", "151.22 ~
$ txn_description   <chr> "POS", "SALES-POS", "POS", "SALES-POS", "SALES-POS", "PAYMENT", "SALES-POS", "POS", "POS", "I~
$ merchant_id       <chr> "81c48296-73be-44a7-befa-d053f48ce7cd", "830a451c-316e-4a6a-bf25-e37caedca49e", "835c231d-8cd~
$ merchant_code     <dbl> NA, NA, NA, NA, NA, NA, NA, NA, NA, NA, NA, NA, NA, NA, NA, NA, NA, NA, NA, NA, NA, NA, NA, N~
$ first_name        <chr> "Diana", "Diana", "Michael", "Rhonda", "Diana", "Robert", "Kristin", "Kristin", "Tonya", "Mic~
$ balance           <dbl> 35.39, 21.20, 5.71, 2117.22, 17.95, 1705.43, 1248.36, 1232.75, 213.16, 466.58, 4348.50, 1203.~
$ date              <dttm> 2018-08-01, 2018-08-01, 2018-08-01, 2018-08-01, 2018-08-01, 2018-08-01, 2018-08-01, 2018-08-~
$ gender            <chr> "F", "F", "M", "F", "F", "M", "F", "F", "F", "M", "M", "F", "F", "M", "M", "M", "M", "F", "F"~
$ age               <dbl> 26, 26, 38, 40, 26, 20, 43, 43, 27, 40, 19, 43, 27, 23, 43, 30, 46, 26, 47, 24, 26, 37, 25, 4~
$ merchant_suburb   <chr> "Ashmore", "Sydney", "Sydney", "Buderim", "Mermaid Beach", NA, "Kalkallo", "Melbourne", "Yoki~
$ merchant_state    <chr> "QLD", "NSW", "NSW", "QLD", "QLD", NA, "VIC", "VIC", "WA", NA, NA, NA, "WA", NA, NA, "QLD", N~
$ extraction        <chr> "2018-08-01T01:01:15.000+0000", "2018-08-01T01:13:45.000+0000", "2018-08-01T01:26:15.000+0000~
$ amount            <dbl> 16.25, 14.19, 6.42, 40.90, 3.25, 163.00, 61.06, 15.61, 19.25, 21.00, 27.00, 29.00, 6.08, 25.0~
$ transaction_id    <chr> "a623070bfead4541a6b0fff8a09e706c", "13270a2a902145da9db4c951e04b51b9", "feb79e7ecd7048a5a36e~
$ country           <chr> "Australia", "Australia", "Australia", "Australia", "Australia", "Australia", "Australia", "A~
$ customer_id       <chr> "CUS-2487424745", "CUS-2487424745", "CUS-2142601169", "CUS-1614226872", "CUS-2487424745", "CU~
$ merchant_long_lat <chr> "153.38 -27.99", "151.21 -33.87", "151.21 -33.87", "153.05 -26.68", "153.44 -28.06", NA, "144~
$ movement          <chr> "debit", "debit", "debit", "debit", "debit", "debit", "debit", "debit", "debit", "debit", "de~                                 
```
# First things first

1. Settting the working directory
```R
setwd('C:/User/path/)
```

2. Specifing the path for the installed libraries
```R
.libPaths('/Path')
```

3. Installing the necessary libraries
```R
install.packages('readr')
install.packages('readxl')
install.packages('tidyverse')
```
# Languages
The project was created using 
```R
R
```
# Environement
**Rstudio**
# Phases for the project

1. Data Collection

Data have been collected from [ANZ Virtual Internship](https://www.theforage.com/virtual-internships/prototype/ZLJCsrpkHo9pZBJNY/ANZ-Virtual-Internship?ref=YZcMJxpBJgfMhAS7T)

2. Data Cleaning

```R
1. Dropping unnecessary columns
2. Renaming variables
3. Deciding what to do with NAs values
4. Remaking the date format
5. Spreading data from columns
```
3. Exploring the Data
Installing 
```	R
library('ggplot2)
```
i am given the chance to visualize my data and discover insights and trends and with
```R
library('writexl')
```
i will export the new tidy dataset that created for furhter analysis
