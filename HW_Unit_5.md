---
title: "UNIT5_MSDS"
author: "Solange GarciadeAlford"
date: "September 29, 2018"
output: 
  html_document:
    keep_md: true
---



## Unit 5 - Question 1


```{ r}

myt = read.table('C:/Users/solan/HW_Unit_5/yob2016.txt',  sep = ";", fill=TRUE)

df <- data.frame(myt[,1:3])

##Add year column

dfy <- data.frame(c[,1])

df <- data.frame(df,dfy)


## Name the columns
names(df)[1] <- "Name"
names(df)[2] <- "Sex"
names(df)[3] <- "Number"
names(df)[4] <- "Year"

names(df)

df$Year[df$Year == 5] <- 2016

## get acquainted with your data
summary(df)
structure(df)
str(df)

##sort the file

library(dplyr)

df <- arrange(df, Name)


## find name with triple ys and display it
a <- grep("yyy$", df$Name, value=TRUE)
a
which(df$Name == a)

## remove 'a'

y2016 <- df[!(df$Name %in% a), ]

str(y2016)





```

## Unit 5 - Question 2



```{ r}


myt = read.table('C:/Users/solan/HW_Unit_5/yob2015.txt',  sep = ",", fill=TRUE)

y2015<- data.frame(myt[,1:3])
Year <- data.frame(c[,1])
y2015 <- data.frame(y2015,Year)

names(y2015)[1] <- "Name"
names(y2015)[2] <- "Sex"
names(y2015)[3] <- "Number"
names(y2015)[4] <- "Year"
names(y2015)



y2015$Year[y2015$Year == 5] <- 2015


## get acquainted with your data
summary(y2015)
structure(y2015)
str(y2015)

head(y2015, 10)


##sort the file

y2015 <- arrange(y2015, Name)

## display the last 10 rows

tail(y2015, 10)

## there are very few people named with the last 10 names in the file, for the sorted by name version of the file. The number of people for the last 10 names does not go higher than 30.

## The unsorted version of the file, the last 10 records are all girls.



## Part c or Q2 - Merge the files


final <- rbind(y2015, y2016)


## sort final by Number to try to locate NA Values

final <- arrange(final, Number)
head(final,10)
tail(final,10)

## Confirm there are no NA values, display NoNA
NoNA <- grep(NA, df$Number, value=TRUE)
NoNA






```

## Unit 5 
{```r}





```

