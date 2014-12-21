# Getting and Cleaning Data - Course Project CodeBook

This file describes the vatiables, data and any transformations performed to clean up the data received.


Data for the project: https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip

## run_analysis.R

Performs the following steps to clean the data:

- From _./data/train_ folder, reads X_train.txt, y_train.txt and subject_train.txt files, storing the data using trainData, trainLabel and trainSubject variables.
- From _./data/test_ folder, reads x_test.txt, y_test.txt and subject_test.txt files, storing the data in testData, testLabel and testSubject variables.
- Concatenate trainData with testData (10299x561 dataframe) as joinData.
- Concatenate trainLabel with testLabel (10299x1 dataframe) as joinLabel.
- Concatenate trainSubject with testSubject (10299x1 dataframe) as joinSubject.
- Read ./data/features.txt, storing data in the _features_ variable. Only extracting the measurements on the mean and standard variation. Getting a 66 indices list.
- Clean the column names of the subset, removing '(', ')', '-' symbols. Also we need to capitalize Mean and Std collumn names.
- Read ./data/activity_labels.txt, storing in _activity_ variable.
- Clean the activity names in _activity_ (second column). Transform them to camelCase, so all names are lowercase, but if activity name has an _ the next letter gets capitalized. So: test_variable -> testVariable.
- Transform the values of joinLabel according to the activity data frame.
- Combine joinSubject, joinLabel and joinData into a cleaned 10299x68 data frame, stored as cleanedData.
- Write cleanedData as ./merged_data.txt.
- Create a second dataset with the average of each variable for each activity and subject. (./data_with_means.txt)