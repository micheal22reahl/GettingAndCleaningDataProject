# CodeBook for Getting and Cleaning Data Project

## Overview
This codebook describes the data, variables, and transformations used to create `tidy_data.txt`.

## Source Data
Original dataset:
https://archive.ics.uci.edu/ml/datasets/Human+Activity+Recognition+Using+Smartphones

## Variables

### subject
Integer ID for the subject who performed the activity (1–30).

### activity
Factor with these levels:
- WALKING
- WALKING_UPSTAIRS
- WALKING_DOWNSTAIRS
- SITTING
- STANDING
- LAYING

### Measurement variables
All other columns are the mean of the original mean/std measurements from the smartphone sensors, grouped by subject and activity (e.g. `time_BodyAcc_mean_X`, `time_BodyAcc_std_X`, `freq_BodyAcc_mean_X`, etc.).

## Transformations

1. Merged training and test sets into one data set.
2. Kept only features with `mean()` or `std()` in their names.
3. Replaced activity IDs with descriptive names from `activity_labels.txt`.
4. Cleaned variable names:
   - removed `()`  
   - replaced `-` with `_`  
   - prefixed `t` with `time_`, `f` with `freq_`.
5. Grouped data by `subject` and `activity`, and calculated the mean of each measurement to create `tidy_data.txt`.
