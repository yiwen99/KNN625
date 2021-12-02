<!-- badges: start -->
[![R-CMD-check](https://github.com/yiwen99/KNN625/workflows/R-CMD-check/badge.svg)](https://github.com/yiwen99/KNN625/actions)
<!-- badges: end -->

# KNN625
## Introduction
This is a simple self written KNN package for UM BIOSTAT625 HW4. This package contains two functions: knn_func and knn1_func that correspond to the functions knn() and knn1() in library(class). knn_func() function does K-nearest neighbor classification on new test cases based on an inputted dataset with known labels. The idea for knn1() function is similar, only it does 1-nearest neighbor classification. The parameters of the two functions do not exactly match the ones in the original knn() and knn1(), but the two self-written functions are supposed to have the same output as knn() and knn1() in library(class).

## Installation
The installation process of packKNN will depend on "devtools" package.
To avoid some possible issues, it is recommended to start a new Rstudio session and restart R before installing this package.
First we install the "devtools" package using the example code below.
```
install.packages("devtools")
```
Then run:
```
library(devtools)
devtools::install_github("yiwen99/KNN625")
library(KNN625)
```
And the functions knn_func() and knn1_func() are ready to be called!

## Usage
Example usage:
```
library(KNN625)
train <- matrix(c(9,1,2,3,9,0,1,9,9,8,2,3,6,9,4,2,3,6),ncol=2)
test <- matrix(c(2,9,3,8),ncol=2)
cl <- as.factor(c("a","b","b","b","c","c","c","c","c"))
knn_func(train,test,cl,prob=TRUE,k=5) #output classification results b, c and corresponding probabilities 0.6, 0.6
knn1_func(train,test,cl) #output classification results b, a
```
More details on usage of the two functions can be found in the help pages in this repository.
