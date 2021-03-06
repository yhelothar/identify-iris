---
title       : Identify Iris Species
subtitle    : with sepal and petal measurements
author      : Mike Huang
job         : 
framework   : io2012        # {io2012, html5slides, shower, dzslides, ...}
highlighter : highlight.js  # {highlight.js, prettify, highlight}
hitheme     : tomorrow      # 
widgets     : []            # {mathjax, quiz, bootstrap}
mode        : selfcontained # {standalone, draft}
knit        : slidify::knit2slides
---


## Purpose

This app allows you to identify iris species by selecting four measurements:

1. Sepal Length
2. Sepal Width
3. Petal Length
4. Petal Width

--- 

## Iris Dataset 

This famous (Fisher's or Anderson's) iris data set gives the measurements in centimeters of the variables sepal length and width and petal length and width, respectively, for 50 flowers from each of 3 species of iris. The species are Iris setosa, versicolor, and virginica.

iris is a data frame with 150 cases (rows) and 5 variables (columns) named Sepal.Length, Sepal.Width, Petal.Length, Petal.Width, and Species.

<b>References</b>

Becker, R. A., Chambers, J. M. and Wilks, A. R. (1988) The New S Language. Wadsworth & Brooks/Cole. 

---

## Iris Model

```r
library(caret)
model<-train(Species~.,data=iris,method="rf")
model$finalModel$confusion
```

```
##            setosa versicolor virginica class.error
## setosa         50          0         0        0.00
## versicolor      0         47         3        0.06
## virginica       0          4        46        0.08
```

---

## Usage Instructions

1. Select sepal and petal measurements with the sliders. 
2. Read model prediction on the right. 




