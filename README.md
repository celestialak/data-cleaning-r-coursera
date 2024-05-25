# data-cleaning-r-coursera

The following steps explain how the run_analysis.R script works to produce the required output for the project which is the Tidy dataset text file.

Download the dataset using the link "https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip".
Unzip the file and save the dataset in the working directory and rename the UCI HAR Dataset as "samsungdata".
Download the run_analysis.R script to your working directory.
Load R studio and set your working directory using setwd().
To run the run_analysis.R code, you need to install (data.table) and (plyr) packages.
Load the R script using source("run_analysis.R")
After the R script is executed, a tidy dataset with name "TidyData" can be found with 180 observations of 88 variables and a Tidy.txt file is created in your working directory.
The run_analysis.R code does the following to generate the tidy dataset output:

Loads the Test and Training datasets along with the features and activity_labels using read.table function.
Merges the Test and Training datasets into one dataset using rbind function.
Names the variables of the mergedData with names from features.txt and add subject and activity columns to the merged Dataset.
Extracts only the columns with measurements on the mean and standard deviation for each measurement.
Makes a dataframe called "RequiredDataset" with subject,activity and meanSTD columns.
Replaces the Activity Ids with activity labels.
Labels the variable names of the "RequiredDataset" with descriptive names.
Using plyr package and ddply function, creates a final, independent tidy data set with the average of each variable for each activity and each subject.
Using write.table function creates a Tidy.txt file in the working directory.
