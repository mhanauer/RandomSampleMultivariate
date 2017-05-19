# RandomSampleMultivariate
---
title: "RandomSampleMultivariate"
output: html_document
---

```{r setup, include=FALSE}
knitr::opts_chunk$set(echo = TRUE)
```

Here is the process for getting a random sample of data from multiple variables
```{r}
# Load data file and specity column names of x (predictor) and y (predicted):
setwd("~/Desktop/QualData")
data = read.csv("selRegressBayesSmallSampleDis.csv", header = TRUE)
data = as.data.frame(data)
# Need to add back about 10 data points ones
set.seed(12345)
index = sample(1:nrow(data), 10, replace = FALSE)
data = data[index, ]
```

