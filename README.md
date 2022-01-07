# Central Tendency for Housing Data Project
### About: 

For this project, I implemented data analysis using R. I used the libraries readr, dplyr, and DescTools which helped me to build the project. I analyze the data of housing in NY to gain a better understanding and insight of the cost of living in each of the boroughs.

In this project, I find the mean, median, and mode cost of one-bedroom apartments in three of the five New York City boroughs: Brooklyn, Manhattan, and Queens as well as point out differences between the boroughs.
 
### Note:

This data comes from Streeteasy.com 

### Results:

First, I imported the datasets of the one-bedroom apartments in the three New York City's boroughs: Brooklyn, Manhattan, and Queens. I wanted to know about the amount of rent for the apartments in each borough.

```R
# Read in housing data
brooklyn_one_bed <- read_csv('brooklyn-one-bed.csv')
brooklyn_price <- brooklyn_one_bed$rent
manhattan_one_bed <- read_csv('manhattan-one-bed.csv')
manhattan_price <- manhattan_one_bed$rent
queens_one_bed <- read_csv('queens-one-bed.csv')
queens_price <- queens_one_bed$rent
```

Afterwards, I found the mode, average (mean), and median values of one-bedroom apartments in each borough and saved them.

```R
# Calculate Mean
brooklyn_mean <- mean(brooklyn_price)
manhattan_mean <- mean(manhattan_price)
queens_mean <- mean(queens_price)

# Calculate Median
brooklyn_median <- median(brooklyn_price)
manhattan_median <- median(manhattan_price)
queens_median <- median(queens_price)

# Calculate Mode
brooklyn_mode <- Mode(brooklyn_price)
manhattan_mode <- Mode(manhattan_price)
queens_mode <- Mode(queens_price)
```

I then wanted to be able to read the new data gained so I made print statements to read the median,mode and mean.

```R
# Mean
if(exists('brooklyn_mean')) {
  print(paste("The mean price in Brooklyn is" , round(brooklyn_mean, digits=2))) 
}else{
    print("The mean price in Brooklyn is not yet defined.")
}
if(exists("manhattan_mean")) {
    print(paste("The mean price in Manhattan is", round(manhattan_mean,digits=2)))
} else {
    print("The mean in Manhattan is not yet defined.")
}
if(exists("queens_mean")) {
    print(paste("The mean price in Queens is" , round(queens_mean,digits=2)))
} else {
  print("The mean price in Queens is not yet defined.")
}   
```

```R
# Median
if(exists("brooklyn_median")) {
  print(paste("The median price in Brooklyn is" , brooklyn_median)) 
}else{
    print("The median price in Brooklyn is not yet defined.")
}
if(exists("manhattan_median")) {
    print(paste("The median price in Manhattan is", manhattan_median))
} else {
    print("The median in Manhattan is not yet defined.")
}
if(exists("queens_median")) {
    print(paste("The median price in Queens is" , queens_median))
} else {
  print("The median price in Queens is not yet defined.")
} 
```

```R
#Mode
if(exists("brooklyn_mode")) {
  print(paste("The mode price in Brooklyn is" , brooklyn_mode)) 
}else{
    print("The mode price in Brooklyn is not yet defined.")
}
if(exists("manhattan_median")) {
    print(paste("The mode price in Manhattan is", manhattan_mode))
} else {
    print("The mode in Manhattan is not yet defined.")
}
if(exists("queens_median")) {
    print(paste("The mode price in Queens is" , queens_mode))
} else {
  print("The mode price in Queens is not yet defined.")
} 
```

Therefore, the product was, 

```R
## "The median price in Brooklyn is 3000"
## "The median price in Manhattan is 3800"
## "The median price in Queens is 2200"
## "The mode price in Brooklyn is 2500"
## "The mode price in Manhattan is 3500"
## "The mode price in Queens is 1750"
## "The mean price in Brooklyn is 3327.4"
## "The mean price in Manhattan is 3993.48"
## "The mean price in Queens is 2346.25"
```

Finally, we could analyze the histogram.

![2](https://user-images.githubusercontent.com/89553126/135773290-2e768ddd-57ae-4817-9adb-986fbddd6cbc.PNG)

![3](https://user-images.githubusercontent.com/89553126/135773291-3455267d-40c3-4aac-bdc2-a9822a634486.PNG)

![1](https://user-images.githubusercontent.com/89553126/135773292-e5183a91-f9fc-4593-8461-452c24af6c30.PNG)



After analyzing the data, Manhattan has the highest cost of rent (on average) for one apartment, while Brooklyn has the second highest, and third is the borough Queens.
