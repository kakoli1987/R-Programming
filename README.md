

## R language Defination
R is a programming language for statistical computing and data visualization.The R programming language is an open source language. R is frequently used for data analysis.R has a convenient library of ready-to-use tools for data cleaning and analysis.

## R language installation
Download and instrall form this [link](https://cran.r-project.org/bin/windows/base/)

## R language packages
```{r  language packages}
#install.packages("tidyverse") 

library(tidyverse)
library(lubridate)
```
## R language Print function 

```{r}
print("Hello ")
```
## R Comments
```{r}

"hello world" # This is a comment 

```
## R Math
```{r Math + - / * }
1+1
2-1
3*3
6/2

```
## R Graphics
```{r plotting}
plot(4,4)
plot(3,7)


```

# R variable declaration
```{r variable declaration}
x<-c(2,3,6,8,9)
y<-c(3,4,2,8,9)
print(x)
print(y)

```

# R If else Statements and Conditions 
```{r if else statements}
a<- 20
b<- 30
if(a<b)
{
  print("b is greater than a")
  }else if(a>b)
{
  print(" a is greater than b")
}
```

# R for loop
```{r for loop}
x<-c(6,3,8,15,66)

for (a in x )
{
  print(a)
}

```
# R for loop break
```{r for loop break}
x<-list("A","B","C","D")

for (a in x )
{
  if(a=="C")
  {
 break
  }

     print(a)
}

```
# R while loop
```{r while loop}
a<-6
while(a>1)
{
   print(a)
   a<-a-1
}
```
# R Funtion call
```{r function call}
function_A<-function()
{ print(" Hello")
  }
function_A()
```
# R Recursion  
```{r Recursion }
recursion_test<- function(a){
  if(a > 0){
    b <- a + recursion_test(a - 1)
    print(b)
  }else{
    b=0
    return(b)
   }
}
recursion_test(3)
```
# R array  declaration
```{r}
array_test<- c(1:32)
array_test

```
# R one  dimension array  declaration
```{r}
array_test<- c(1:24)
array_test

dimension_array<-array(array_test,dim<-c(4,3))
dimension_array
```

# R  Data Frame
```{r}

id <- c(1:10)
name <- c("John ", "Rob ", "Rachel ", "Christy ", "Johnson ", "Candace ", "Carlson ", "Pansy ", "Darius ", " Garcia")


job_title <- c("Professional", "Programmer", "Management", "Clerical", "Developer", "Programmer", "Management", "Clerical", "Developer", "Programmer")


employee <- data.frame(id, name, job_title)
view(employee)
print(employee)


```
# R factor() function define
```{r}
# Create a factor
new_factor <- factor(c("A", "B", "C", "D", "E", "F", "G"))

# Print the factor
new_factor
length(new_factor)
```
# R Graphics

```{r}
plot(1, 3)

plot(c(1, 8), c(3, 10),col="red")

plot(1:10,col="blue")

```
# R line chart
```{r}
# Line chart variable type value is l (l for line)

plot(1:10, main=" Graph", xlab=" x-axis", ylab=" y axis",type ="l")
```


# R pie chart
```{r}
# Create a vector 
x <- c(6,14,24,34)
labels_list<-x

# Display the pie chart
pie(x)

# Display the pie chart with labels
pie(x, label = labels_list,x, main = "pie chart")

# Create a vector of colors
colors <- c("red", "orange", "purple", "green")
pie(x, label = x, main = "pie chart",col = colors)

# Display the explanation box


legend("topright", inset=.05, title="pie chart",legend =x, fill=colors )
```
# R bars charts
```{r}
x <- c("2011", "2012", "2013", "2014")
y <- c(40, 55, 66, 82)

barplot(y, names.arg = x, col = "blue")
```

#R environment by loading "tidyverse" ,"ggplot2" packages:

```{r}
# diamonds Data set
ggplot(data = diamonds)+
  geom_bar(mapping = aes(x=cut,fill  = clarity))

ggplot(data = diamonds)+
  geom_bar(mapping=aes(x= color,fill = cut))+
  facet_wrap(~cut)
```

# R min(), max() and mean() Function
# The min() function returns the minimum value of a vector or data frame.

```{r for min()}
#create a vector 
valus<-c(2,5,4,7,9,22,43,27)
min(valus,na.rm = FALSE)

```
# max() function returns the maximum value of a vector or data frame.

```{r for max()}
#create a vector 
valus<-c(2,5,4,7,9,22,43,27)
max(valus,na.rm = FALSE)
```
# mean() is the average of a data set.

```{r for mean()}
#create a vector 
valus<-c(2,5,4,7,9,22,43,27)
mean(valus)
```
# mode() is the most common number in a data set.
```{r for mode()}
#create a vector 
valus<-c(2,5,4,7,33,5,9,22,43,27,5)
#define a mode function
mode=function()
{
  
  return(names(sort(-table(valus)))[1])
}

#call the mode function
mode()

```
# median() is the middle of the set of numbers.
```{r for median }
#create a vector 
valus<-c(2,5,4,7,9,22,43,27)
median(valus)

```

