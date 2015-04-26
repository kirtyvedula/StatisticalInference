---
title: "Project report - Statistical Inference"
author: "Kirty Vedula"
date: "04/24/2015"
output: pdf_document
---
## Libraries

```r
library(datasets)
library(ggplot2)
library(knitr)
library(markdown)
```

## Simulating exponential distribution with rexp commmand

```r
set.seed(3)
lambda <- 0.2
num_sim <- 1000
sample_size <- 40
sim <- matrix(rexp(num_sim*sample_size, rate=lambda), num_sim, sample_size)
row_means <- rowMeans(sim)
```

## ------------------------------------------------------------------------
## Plot the histogram of averages

```r
hist(row_means, breaks=50, prob=TRUE,
     main="Distribution of averages of samples,
     drawn from exponential distribution with lambda=0.2",
     xlab="")
```

![](Project1_files/figure-latex/histogram_averages-1.pdf) 
## Density of the averages of samples





















