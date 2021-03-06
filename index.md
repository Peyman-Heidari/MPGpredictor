---
title       : MPG prediction using linear regression
subtitle    : 
author      : Peyman H
job         : 
framework   : io2012        # {io2012, html5slides, shower, dzslides, ...}
highlighter : highlight.js  # {highlight.js, prettify, highlight}
hitheme     : tomorrow      # 
widgets     : []            # {mathjax, quiz, bootstrap}
mode        : selfcontained # {standalone, draft}
knit        : slidify::knit2slides
---

## What is this App?

1- This app enables the user to predict mpg of a car based on some measureable variables.



2- It works based on a linear regression models that was fitted to the mtcars data set. (can be found in datasets package of R)


3- Linear models are simple, yet useful tools to understand relationships between variables and predict new outputs.

Access the MPG predictor [App](https://peymanh.shinyapps.io/MPGPredictor/)

---

## mtcars dataset

The data was extracted from the 1974 Motor Trend US magazine, and comprises fuel consumption and 10 aspects of automobile design and performance for 32 automobiles (1973-74 models).This is a data frame with 32 observations on 11 variables.


1)   mpg	 Miles/(US) gallon                         2)	  cyl	 Number of cylinders

3)	 disp	 Displacement (cu.in.)                     4)	  hp	 Gross horsepower

5)   drat	 Rear axle ratio                           6)   wt	 Weight (1000 lbs)

7)	 qsec	 1/4 mile time                             8)   vs	 V/S

9)	 am	 Transmission (0 = automatic, 1 = manual)    10)  gear	 Number of forward gears

11)  carb	 Number of carburetors


Access the MPG predictor [App](https://peymanh.shinyapps.io/MPGPredictor/)

---

## Influential Variables

Based on our analysis mpg depends mostly on four variables, which are used in this app:

- Displacement volume of the engine

- Number of cylinders of the vehicle

- type of transmission (Manual/Automatic)

- Weight of the vehicle

Access the MPG predictor [App](https://peymanh.shinyapps.io/MPGPredictor/)

---

## Linear Regression Model
The following is the coefficients of the linear regression model used for this app.

```r
library(datasets)
mtcars$am <- as.factor(mtcars$am)
fit <- lm(mpg ~cyl+am+disp+wt,  data=mtcars)
fit
```

```
## 
## Call:
## lm(formula = mpg ~ cyl + am + disp + wt, data = mtcars)
## 
## Coefficients:
## (Intercept)          cyl          am1         disp           wt  
##   40.898313    -1.784173     0.129066     0.007404    -3.583425
```

Access the MPG predictor [App](https://peymanh.shinyapps.io/MPGPredictor/)
