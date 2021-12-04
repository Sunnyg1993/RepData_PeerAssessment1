# Reproducible Research: Peer Assessment 1
#
### load_packages
#### packages used are: dplyr, lubridate, and ggplot2
#
## 1. Loading and preprocessing the data
#
### Download file --> Unzip file --> load data use read.csv()
#
### do check the data
#
### Process/transform the data: mutate date to the date format
#
## Q1: What is mean total number of steps taken per day?
### group the data by dat and summarise by sum the steps, ignore the NAs, get the statistics of the data by summary()
### ans: The mean total number of steps taken per day is 9354.
#
## Q2. What is the average daily activity pattern?
### plot a histogram of total_steps by day
### ans: about 10% of the days appear to be no movement, steps = 0, might be due to monitor faliure(?). Otherwise, most of the days, about 9%, the activity takes 10000 steps in total. 
![](https://github.com/Sunnyg1993/RepData_PeerAssessment1/blob/master/total_steps_daily.png)
#
## Q3. Imputing missing values
#
### using mean of 5-minute interval for the missing value
### 1. get the mean of 5-minute interval by group() and summarise()
### 2. give the missing steps of that interval the mean steps of that interval
#
## Q4. Are there differences in activity patterns between weekdays and weekends?
#
### 1. add a factor as weekends using factor()
### 2. group the data by inerval and weekends
### 3. plot the activity by intervals for weekdays and weekends using ggplot()
### ans: the activity peak hour on both weekdays and weekends appears around 8-9am. for the rest of the day, activities are more often in the afternoon and evening (especially around 8pm) on weekends. On weekdays, 5-8am and 6-7pm are quite busy, probably on the way to and back from work.
[activity_by_weekends.png](https://github.com/Sunnyg1993/RepData_PeerAssessment1/blob/master/activity_by_weekends.png)
