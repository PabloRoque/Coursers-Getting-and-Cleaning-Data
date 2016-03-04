# Code Book file


CodeBook describing operations performed on the data for the programming assignments of the Coursera Getting and Cleaning Data course. The script run_analysis.R performs the following operations:

### Download, unzip, load into memory
    1. Download the appropiate data set (and unzip) from: https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip 
    2. Load files activity_labels.txt, features.txt. These file contain the appropiate labels for the numeric data
    3. Load the numeric data from the test and train dataset: y_test.txt, X_test.txt, y_train.txt, X_train.txt
    
### Label train and test datasets 
    1. Labels from activity_labels.txt, features.txt are placed as columns that identfy subjects, activities
    
### Combine training and test datasets into a single one
    1. Merge both datasets into a single data.frame

### Select the data we are interested in
    1. Parsing names() to search for the stings "mean" and "std"
    2. Select column names matching the above statement
    
### Perform the mean() operation
    1. We perform the operation aggregating the data by $subject and $activity
    
The final data is stored in the tidydata.txt file in this repo. 

Data is represented in the figure "Rplot.png" in this repo. 
It plots column values of the first 12 magnitudes in the tidydata set, i.e., t-gravity-acc-mean, t-body-acc-mean... for the 3 cartesian axis X,Y,Z. 
For each magnitude all the subjects of the analysis are listed in the x-axis of the plot. Different colors represent the 6 different activities (WALK, STANDING...). The size of the dots match the standar deviation of the corresponding magnitude (some columns to the right in the data table). I took the liberty of taking the absolute value of the std values, since I could not understand what negative std meant.

![Rplot.R](https://github.com/PabloRoque/Coursera-Getting-and-Cleaning-Data/blob/master/Rplot.png)
