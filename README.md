# Getting and Cleaning Data — Course Project

This repository contains my submission for the Coursera course **"Getting and Cleaning Data."**

## Files

- `run_analysis.R`  
  R script that downloads the data (if needed), merges training and test sets, extracts mean and standard deviation measurements, applies descriptive activity names, cleans variable names, and creates the final tidy data set.

- `tidy_data.txt`  
  The tidy data set with the average of each selected variable for each activity and each subject.

- `CodeBook.md`  
  Describes the variables, data, and transformations used to create `tidy_data.txt`.

## How to run

1. Place `run_analysis.R` in your working directory.
2. In R, run:

   ```r
   source("run_analysis.R")
