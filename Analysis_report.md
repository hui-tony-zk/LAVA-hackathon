# Final_Analysis.Rmd
Tony Hui  
October 24, 2015  

# Prelimary analysis of the Data

## Load dependencies


```r
require(knitr)
```

```
## Loading required package: knitr
```

```r
opts_chunk$set(echo=F)
```


```
## Loading required package: ggplot2
## Loading required package: dplyr
## 
## Attaching package: 'dplyr'
## 
## The following objects are masked from 'package:stats':
## 
##     filter, lag
## 
## The following objects are masked from 'package:base':
## 
##     intersect, setdiff, setequal, union
## 
## Loading required package: stringr
## Loading required package: data.table
## 
## Attaching package: 'data.table'
## 
## The following objects are masked from 'package:dplyr':
## 
##     between, last
```

## Load data



### Sneak peak at the data


```
## [1] 30
```

Number of columns all over the place - assume that there should only be 26 "real" columns (plus the 4 columns of metadata that was added) - use this function to figure out what's wrong



### Issue fixed - went back and fixed the read file function and combined all data


|time      | Students.Listening| Students.IndividualWork| Students.ClickerQuestionInGroups| Students.Worksheet| Students.OtherGroupwork| Student.AnsweringQuestion| Student.AskingQuestion| Students.WholeClassDiscussion| Students.MakingPrediction| Students.Presentation| Students.Quiz| Students.Waiting| Students.Other| Instructor.Lecturing| Instructor.WritingOnBoard| Instructor.GivingFeedback| Instructor.AskingQuestion| Instructor.AskingClickerQuestion| Instructor.AnsweringQuestion| Instructor.MovingThroughGroup| Instructor.OneOnOne| Instructor.ShowingVideo| Instructor.Administration| Instructor.Waiting| Instructor.Other|course |instructor |semester |observation |
|:---------|------------------:|-----------------------:|--------------------------------:|------------------:|-----------------------:|-------------------------:|----------------------:|-----------------------------:|-------------------------:|---------------------:|-------------:|----------------:|--------------:|--------------------:|-------------------------:|-------------------------:|-------------------------:|--------------------------------:|----------------------------:|-----------------------------:|-------------------:|-----------------------:|-------------------------:|------------------:|----------------:|:------|:----------|:--------|:-----------|
|0-2 min   |                  1|                      NA|                                1|                 NA|                      NA|                        NA|                     NA|                            NA|                        NA|                    NA|            NA|               NA|             NA|                   NA|                        NA|                         1|                         1|                                1|                           NA|                            NA|                  NA|                      NA|                        NA|                 NA|               NA|11     |A          |1        |1           |
|2-4 min   |                 NA|                      NA|                                1|                 NA|                      NA|                        NA|                     NA|                            NA|                        NA|                    NA|            NA|               NA|             NA|                   NA|                        NA|                        NA|                         1|                               NA|                           NA|                            NA|                  NA|                      NA|                        NA|                 NA|               NA|11     |A          |1        |1           |
|4-6 min   |                  1|                      NA|                                1|                 NA|                      NA|                        NA|                     NA|                            NA|                        NA|                    NA|            NA|               NA|             NA|                    1|                        NA|                         1|                         1|                                1|                           NA|                            NA|                  NA|                      NA|                        NA|                 NA|               NA|11     |A          |1        |1           |
|6-8 min   |                 NA|                      NA|                                1|                 NA|                      NA|                        NA|                     NA|                            NA|                        NA|                    NA|            NA|               NA|             NA|                   NA|                        NA|                         1|                        NA|                                1|                           NA|                            NA|                  NA|                      NA|                        NA|                 NA|               NA|11     |A          |1        |1           |
|8-10 min  |                  1|                      NA|                               NA|                 NA|                      NA|                        NA|                      1|                            NA|                        NA|                    NA|            NA|               NA|             NA|                   NA|                        NA|                         1|                        NA|                               NA|                            1|                            NA|                  NA|                      NA|                        NA|                 NA|               NA|11     |A          |1        |1           |
|10-12 min |                  1|                      NA|                               NA|                  1|                      NA|                        NA|                     NA|                            NA|                        NA|                    NA|            NA|               NA|             NA|                   NA|                        NA|                         1|                         1|                               NA|                           NA|                            NA|                  NA|                      NA|                        NA|                 NA|               NA|11     |A          |1        |1           |






