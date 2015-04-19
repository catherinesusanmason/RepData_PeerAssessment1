# RR Peer assignment 1
Cathy Mason  
Friday, April 17, 2015  

This is an R Markdown document. Markdown is a simple formatting syntax for authoring HTML, PDF, and MS Word documents. For more details on using R Markdown see <http://rmarkdown.rstudio.com>.

When you click the **Knit** button a document will be generated that includes both content as well as the output of any embedded R code chunks within the document. 

##Loading and preprocessing the data

Analysis of number of steps taken during the day measured in 5 minute intervals

The variables included in this dataset are:
    steps: Number of steps taking in a 5-minute interval (missing values are coded as NA)
    date: The date on which the measurement was taken in YYYY-MM-DD format
    interval: Identifier for the 5-minute interval in which measurement was taken


```
## 
## Attaching package: 'dplyr'
## 
## The following object is masked from 'package:stats':
## 
##     filter
## 
## The following objects are masked from 'package:base':
## 
##     intersect, setdiff, setequal, union
```

## What is mean total number of steps taken per day?

The first analysis is to review the total number of steps taken per day? 
The histogram below shows the total number of steps taken each day

![](PA1_template_files/figure-html/unnamed-chunk-2-1.png) 

The mean and median of this data are:


```
## [1] 10766.19
```

```
## [1] 10765
```

## What is the average daily activity pattern?

How does the activity pattern vary throughout the day?

The chart below shows how the activity varies through the day per 5 minute interval based on the average number of steps taken, averaged across all days

![](PA1_template_files/figure-html/unnamed-chunk-4-1.png) 

The interval which on average across all the days in the dataset, contains the maximum number of steps is:


```
##     int mean_steps
## 104 835   206.1698
```

## Inputing missing values

We now want to look at the impact of missing data in the dataset. The number of missing measurements in the dataset is:


```
## [1] 2304
```

Next we fill in the missing values.  The method chosen is to calculate the mean per interval across all days and insert these into the dataset 

The charts below show a comparison of the original dataset and the modified dataset with the missing values replaced by the calcualted mean per 5 min interval.

![](PA1_template_files/figure-html/unnamed-chunk-7-1.png) 

## Are there differences in activity patterns between weekdays and weekends?

We now want to see if there is a difference between the number of steps made during weekdays and weekends.  Using the modified datset where the missing values have been replaced, the following charts show plots of the number of steps taken throughout the day for weekdays and weekends.  
![](PA1_template_files/figure-html/unnamed-chunk-8-1.png) 

We can clearly see that activity levels remain higher during the weekends.


Note that the `echo = FALSE` parameter was added to the code chunk to prevent printing of the R code that generated the plot.
