# Data Visualizations from UCI Machine Learning Repository

### Statement
We plan to make a few data visualizations from the UCI Machine Learning Repository. Data visualization is interesting
because it enables us to understand and communicate complex data easily. By performing data visualizations in racket, we
hope to utilize several key concepts learned in class and explore racket plot, csv, array and matrix 
libraries.

### Analysis

In order to implement the project we plant to use several approaches from the class.

We will be using data abstraction by taking a data set from a CSV and storing it in a list of lists and 2d arrays, like
a table. We will also be using selectors to get at the various columns in the data

We will be using recursion throughout the project since several different list operations involve recursing through the 
list by using car and cdr. For example, since CSV stores everything in a string format, to perform operations on the 
numbers in a data set, they must first casted to numbers and the non-number fields need to be removed. Recursion will 
Also be used when making the plots. When ploting the plot function will recurvisely build a list of points to plot.

We will also be using mapping, filtering, and reductions to perform various data manipulations on, such as removing a 
certain column from our data. Also, we will be using higher order functions to perform operations on several elements 
in a 2d list or array. All the statics functions will all be varing foldr functions.

The array library in racket supports a lot of list manipulation we did in Haskell like slicing and comprehensions. 
The matrix library will enable us to perform standard linear algebra functions.

There is a bit of expersion evaultion going on in out project. The selectors hold 2 parts the lambdas to get at the data
and the name of the column. If the symbol 'name is passed the name of the column is retruned. Otherwise the lambda is returned.
Also in the plot2D function, the last arugement decides if a linear regression should be ploted or not. If the symbol 'none is
passed then it wont, otherwise it will. Although this doesn't make logical sesnse it was made as an intention to be expanded upon
in the future.

### External Technologies

Our project will be connecting to data sets from UCI (for example https://archive.ics.uci.edu/ml/datasets/Iris) or using
reading/writing from a CSV file.

### Data Sets or other Source Materials

We will be using the iris dataset from UCI (https://archive.ics.uci.edu/ml).

### Deliverable and Demonstration

At least two different data visualizations, one will be plot of a principal component analysis like the sample image 
below.

![pca image](/pca.png?raw=true "pca image")

The functions we plan on writing will be fairly general and should able to easily be applied to other data sets. 
For example the code casting numbers in a 2 dimensional list can be appled to any list of lists. 

### Evaluation of Results
We will know we are successful because we will produce the same plots made in FP3, The Iris data set is very good for 
testing out visualization techniques since the data set is well documented and very intuitive to understand. 

## Architecture Diagram
Upload the architecture diagram you made for your slide presentation to your repository, and include it in-line here.

![OPL_FP_image](/OPL_FP.png?raw=true "OPLFP image")

Data will be obtained from the UCI Machine Learning Repository in CSV format. We can then use the Racket CSV library to
move it into memory as a list of lists of strings. From there we can process the data using Racket until it is ready to
plot using the plot library.

## Schedule


### First Milestone (Sun Apr 9)

Writing code required to do initial manipulations from the raw csv data to a usable data abstraction.

### Second Milestone (Sun Apr 16)
completing the plots

### Public Presentation (Mon Apr 24, Wed Apr 26, or Fri Apr 28 [your date to be determined later])
additional data visualizations time permitting 

## Group Responsibilities

### Robert Farinelli @rfarinel
Data filitering and statciail analysis of data (total,count ,average, standard deviation, min, max)
Data visualization of data from UCI repository (2D point plots of 2 different features with linear regression, 3D point plots of 3 different features, and bar charts for statciail analysis)

### Christopher Pearce @cp0153
Principal Component Analysis of Iris or other similar data set on the UCI repository 
