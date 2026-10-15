---
layout: default
title: "Statistical Thinking — Chapter 2: Data Frames & Frequency"
date: 2022-06-11
original: https://rpubs.com/kambonalytic/913634
---

[← Back to portfolio](../index.md)

*Published 2022-06-11 · Originally on [RPubs](https://rpubs.com/kambonalytic/913634) · Data: [Statistical Thinking datasets](http://pluto.huji.ac.il/~msby/StatThink/)*

## Reading a CSV File into R

```r
ex.1 <- read.csv("http://pluto.huji.ac.il/~msby/StatThink/Datasets/ex1.csv")# Read your data without downloading it
```

```r
head(ex.1) # Returns the first parts of the data frame
```

```text
##        id    sex height
## 1 5696379 FEMALE    182
## 2 3019088   MALE    168
## 3 2038883   MALE    172
## 4 1920587 FEMALE    154
## 5 6006813   MALE    174
## 6 4055945 FEMALE    176
```

```r
# read more: https://www.rdocumentation.org/packages/utils/versions/3.6.2/topics/head 
```

```r
tail(ex.1) # Returns the last parts of a data frame
```

```text
##          id    sex height
## 95  9448072 FEMALE    174
## 96  7085816   MALE    187
## 97  3596409 FEMALE    141
## 98  9383288   MALE    195
## 99  1582961 FEMALE    129
## 100 9805356   MALE    172
```

```r
# read more: https://stat.ethz.ch/R-manual/R-devel/library/utils/html/head.html
```

### Frequency

```r
work.hours <- c(5,6,3,3,2,4,7,5,2,3,5,6,5,4,4,3,5,2,5,3)
```

```r
table(work.hours) # This create a table that summarizes the different values of working hours and the frequency in which these values appear in the data
```

```text
## work.hours
## 2 3 4 5 6 7 
## 3 5 3 6 2 1
```

```r
# the function “`table`" takes as input a sequence of data and produces as output the frequencies of the different values.
```

```r
data.frame(table(work.hours)) # Applying the function “`data.frame`" to the output of the “`table`" function present the outcome as a frequency listing the different data values in ascending order and their frequencies.
```

```text
##   work.hours Freq
## 1          2    3
## 2          3    5
## 3          4    3
## 4          5    6
## 5          6    2
## 6          7    1
```

```r
# A frequency is the number of times a given datum occurs in a data set.
# The function “`data.frame`” transforms its input into a data frame, which is the standard way of storing statistical data
```

```r
# A relative frequency is the fraction of times a value occurs. 
# To find the relative frequencies, divide each frequency by the total number of students in the sample
# The Script below illustrate how to compute the relative frequencies

freq <- table(work.hours)
freq # This object store the frequencies
```

```text
## work.hours
## 2 3 4 5 6 7 
## 3 5 3 6 2 1
```

```r
sum(freq) # This gives the sample size of the freq object
```

```text
## [1] 20
```

```r
freq/sum(freq) # This give the relative frequency
```

```text
## work.hours
##    2    3    4    5    6    7 
## 0.15 0.25 0.15 0.30 0.10 0.05
```

```r
sum(freq/sum(freq)) # The cumulative relative frequency is the accumulation of previous relative frequencies
```

```text
## [1] 1
```

```r
sum(freq/sum(freq)) 
```

```text
## [1] 1
```

```r
#The cumulative relative frequency is the accumulation of previous relative frequencies.

# To find the cumulative relative frequencies, add all the previous relative frequencies to the relative frequency of the current value

cumsum(freq/sum(freq)) # The function cumsum is used to find the cumulative frequencies
```

```text
##    2    3    4    5    6    7 
## 0.15 0.40 0.55 0.85 0.95 1.00
```

### `R` functions introduced in this chapter

- `data.frame()` creates data frames, tightly coupled collections of variables which share many of the properties of matrices and of lists, used as the fundamental data structure by most of R’s modeling software.
- `head()` and `tail()` return the first or last parts of a data.frame.
- `sum()` and `cumsum()` returns the sum and cumulative sum of the values present in its arguments.
- `read.csv(file)` reads a file in table format and creates a data frame from it.
