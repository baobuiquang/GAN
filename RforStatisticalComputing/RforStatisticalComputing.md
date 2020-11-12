---
title: R for Statistical Computing
has_children: true
nav_order: 5
---

# R for Statistical Computing

# Frequently Used Function

``` r
#Remove all previous var
rm(list=ls(all=TRUE))

#Set directory
setwd("D:/folder")

#Read data from csv file to a dataframe 
dataframe_name<-read.csv("filename.csv", header=TRUE)
attach(dataframe_name)

#Extract column's data to variable
var_name = dataframe_name$var_name

#Create data frame
r <- 1:10
S <- pi*r^2
dataframe_name = data.frame(Radius=r, Area=S)

#Function
f <- function(x) {
	return(x^2 + 2*x + 1)
}

#For loop
for(i in 1:10){
	count = count + 1
}

#If-else condition
if(num%%2 == 0){
	#num is an even
} else {
	#num is an odd
}

#Integrate
integrate(function(x) f(x), lower=-Inf, upper=Inf)

#Create array
seq_arr = seq(-5, 5, length.out=20)
sample_arr = sample(1:6, number_of_ele, TRUE) #int
runif_arr = runif(number_of_ele, 1, 10) #double, often use with round(..., 2)


#Graph
plot(x, f(x), type="h", ylab="Name of y-axis")
curve(f(x), from=-5, to=5, ylab="Name of y-axis")

```