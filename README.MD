---
title: "README"
output: github_document
---
==============================================================
Run_Analysis.R R-script on Human Activity Recognition Using Smartphones Dataset
==============================================================

The run_analysis.R script reads data from the "Human Activity Recognition Using Smartphones Dataset" and produces a new - tidy dataset which may be used for further analysis.

The original dataset included the following data files:
=======================================================
- 'features.txt': List of all features.

- 'activity_labels.txt': List of class labels and their activity name.

- 'train/X_train.txt': Training set.

- 'train/y_train.txt': Training labels.

- 'train/subject_train.txt': ID's of subjects in the training data

- 'test/X_test.txt': Test set.

- 'test/y_test.txt': Test labels.

- 'test/subject_test.txt': ID's of subjects in the training data

A brief description of the script:
==================================
The run_analysis.R script merges data from a number of .txt files and produces a tidy data set which may be used for further analysis.

- First it checks to see if the required "reshape2" has been installed and then loads the "reshape2" package.

- It then reads all required .txt files and labels the datasets

- Consquently the appropriate "activity_id"'s and "subject_id"'s are appended to the "test" and the "training" data, which are then combined into one single data frame

- Using the "grep" function, all the columns with mean() and std() values are extracted and then a new data frame, including only the "activity_id", the "subject_id" and the mean() and std() columns, is created    

- Using the "merge" function, descriptive activity names are merged with the mean/standard deviation values dataset, to get one dataset with descriptive activity names

- Lastly, with the help of the "melt" and "dcast" functions of the "reshape2" package, the data is converted into a table containing mean values of all the included features, ordered by the activity name and the subject id, and the data is written to the "tidy_data.txt" file.

A description of the "tidy_data.txt" file may be found in the "CodeBook.md" file. 


A