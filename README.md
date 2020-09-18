# Getting-and-Cleaning-Data-Course-Project
This Repository is about getting and cleaning data project and it contains the following files:

  1-README.md file which provides an overview of the data set and how it was created.

  2-tidy_data.txt which contains the data set.

  3-CodeBook.md which describes the contents of the data set.

   4-run_analysis.R, the R script that was used to create the data set.
   
  ## Data description

The variables in the data X are sensor signals measured with waist-mounted smartphone from 30 subjects. The variable in the data Y indicates activity type the subjects performed during recording.

 ## Code explaination

The code combined training dataset and test dataset, and extracted partial variables to create another dataset with the averages of each variable for each activity.

## Creating the data set

 the generating dataset containes variables calculated based on the mean and standard deviation. Each row of the dataset is an average of each activity type for all subjects.
 
The R script run_analysis.R can be used to create the data set. It retrieves the source data set and transforms it to produce the final data set by implementing the following steps (see the Code book for details, as well as the comments in the script itself):

* Download and unzip source data.

* Merge the training and the test sets to create one data set.Use command rbind to combine training and test set.

* Extract only the measurements on the mean and standard deviation for each measurement.Use grep command to get column indexes for variable name contains "mean()" or "std()".

* Uses descriptive activity names to name the activities in the data set Convert activity labels to characters and add a new column as factor

* Appropriately labels the data set with descriptive variable names. Give the selected descriptive names to variable columns

* From the data set in step 4, creates a second, independent tidy data set with the average of each variable for each activity and each subject. Use pipeline command to create a new tidy dataset with command group_by and summarize_each in dplyr package.
