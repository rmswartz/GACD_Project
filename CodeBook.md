# Code Book for Getting and Cleaning Data Course Project

## Citation
The data described by this code book originated in a data set called "Human Activity Recognition Using Smartphones Dataset, Version 1.0" created by the following team:

Jorge L. Reyes-Ortiz, Davide Anguita, Alessandro Ghio, Luca Oneto.  
Smartlab - Non Linear Complex Systems Laboratory  
DITEN - Università degli Studi di Genova.  
Via Opera Pia 11A, I-16145, Genoa, Italy.  
activityrecognition@smartlab.ws  
www.smartlab.ws  

## Study Design
The team at Smartlab gathered a set of 30 subjects and recorded a large set of accelerometer/gyroscope measurements from a Samsung Galaxy S II attached to their waist while performing a variety of physical activities. They recorded the subject and the activity, and correlated this via video with the measurements coming from the phone to form a large dataset. Their initial purpose was to offer this data set in two components: a training set and a test set. The former could be used to train a machine learning model to categorize physical activity based upon measurements from the phone, then test that model with the test data set.

The data presented here originated from the Smartlab data, with the following processing steps generating the file 'final_data.txt':

* Ingest the training, test, and label data
* Align the training and test data with the corresponding subject number and activity references
* Combine the training and test data sets together to form one data set
* Subset the data set to only those variables used to label the subject or activity, and anything that provides a mean or standard deviation
* Convert the activity label (provided as a number) to a factor and translate to the descriptive activity name
* Rename the variable to be more descriptive and free from non-alpha numeric characters
* Convert the subject label (provided as a number) to a factor
* Melt the data, and recast to summarize the data to just a single measure for each subject, each activity the subject undertook, and the mean of each measurement variable - this results in 180 observations for 79 measurement variables (plus two variables tracking the subject and activity)

## Code Book
The processed data is comprised of the following variables:

Variable Name

Variable Name  | Position | Class | Description |
:------------- | :------: | :---: | :---------- |
Subject | 1 | Factor | Reference to the volunteer (number 1 through 30) whose movement generated the data |
Actvity | 2 | Factor | The activity the subject performed; 1 of 6 values - WALKING, WALKING_UPSTAIRS, WALKING_DOWNSTAIRS, SITTING, STANDING, LAYING |
