# Data.set-cars

Introduction to Cars Dataset
There is a dataset called `cars` which gives the data:  the speed of cars and the distances taken to stop. Note that the data were recorded in the 1920s. It has 50 observations and 2 variables 
```{r}
cars.data <- cars
dim(cars.data)
```
In the dataset `cars` the variables are speed and distance. As speed and distance can only be measured in numbers, we could only use numbers.We will begin by making a histogram. Looking at the dataset `cars`we can see that the majority of the cars have a top speed of 18-20 km. 
```{r}

str(cars.data)
hist(cars.data$speed, 20, col="red")
```
We can also see that the distance travelled is around 20km
```{r}
hist(cars$dist, 20, col="blue")
```
As we have made Histograms now, we will make a box plot. The dataset `cars`shows us that the speed has less variation compared to the distance.
```{r}
boxplot(cars.data,main= "Box plot",
       xlab="variable", ylab="Value" , col = "green"  , pch=19)
```
 The scatter plot shows us that the data is positively corealted. The speed depends on the distance or the other way around.
```{r}
plot(x=cars.data$speed,y=cars.data$dist, main="Cars Data scatter plot" , xlab="speed", ylab = "distance", pch=19, col="black")
```
```{r}
#lin.mod <- lm(cars.data$dist-cars.data$speed)
#pr.lm<- predict(lin.mood) 
 #lines(pr.lm-cars.data$speed,col= "turquoise",lwd=0,7) )


  
     
