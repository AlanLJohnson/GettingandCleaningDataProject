# Introduction

* First, all the similar data is merged using the `rbind()` function. 
* Then, only those columns with the mean and standard deviation measures are taken from the whole dataset.
* As activity data is addressed with values 1:6,  the activity names and IDs are taken from `activity_labels.txt` and they are substituted.
* Columns with non descriptive column names are corrected.
* A new dataset with all the average measures for each subject and activity type is then generated. 

# Variables

* `x_train`, `y_train`, `x_test`, `y_test`, `subject_train` and `subject_test` contain the data from the downloaded files.
* `x_data`, `y_data` and `subject_data` merge the former datasets.
* `features` contains the correct names for the `x_data` dataset, which are applied to the column names in `mean_and_std_features`
* Did the same with the `activities` variable.
* `all_data` merges `x_data`, `y_data` and `subject_data` gets put into a dataset.
* At the end `averages_data` contains the averages which will be later stored in a `.txt` file. `ddply()` from the plyr package is used to apply `colMeans()`
