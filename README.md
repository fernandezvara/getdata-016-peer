# Getting and Cleaning Data course project.

This _Readme_ gives an overview of the project scripts.


## Script.

### run_analysis.R

This script performs the data analysis.

- Downloads the file on the exercise into the _data_ folder. URL: https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip 
- Extracts the contents into the working directory and renames the extracted folder to the correct name.
- Reads from raw data from the extracted files.
- Performs the merging and cleaning of data required by project specification.
- Saves the tidy dataset in CSV format.


## How to run.

- Clone the repository

```
git clone git@github.com:fernandezvara/getdata-016-peer.git
```
- Open RStudio.
- Execute these commands in the RStudio console.

```
setwd( folder where you cloned the repository )
source("run_analysis.R")
```

- Results are stored in the working directory. (merged_data.txt, data_with_means.txt)


## Code Book

The code book for this project is in CodeBook.md file. Contains the description of variables, data and transformations done using run_analysis.R.


Student: Antonio Fernández Vara
