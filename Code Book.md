#Code Book
This code book that describes the variables used, data, and any transformations task that was performed to clean up the data and produce tidy data.

#Raw data collection
Raw data were obtained from the UCI Machine Learning repository: http://archive.ics.uci.edu/ml/datasets/Human+Activity+Recognition+Using+Smartphones 



#Data Set Information
The experiments have been carried out with a group of 30 volunteers within an age bracket of 19-48 years. Each person performed six activities (Walking, Walking Upstairs, Walking Downstairs, Sitting, Standing, Laying) wearing a smartphone (Samsung Galaxy S II) on the waist. Using its embedded accelerometer and gyroscope, we captured 3-axial linear acceleration and 3-axial angular velocity at a constant rate of 50Hz. The experiments have been video-recorded to label the data manually. The obtained dataset has been randomly partitioned into two sets, where 70% of the volunteers was selected for generating the training data and 30% the test data.
The sensor signals (accelerometer and gyroscope) were pre-processed by applying noise filters and then sampled in fixed-width sliding windows of 2.56 sec and 50% overlap (128 readings/window). The sensor acceleration signal, which has gravitational and body motion components, was separated using a Butterworth low-pass filter into body acceleration and gravity. The gravitational force is assumed to have only low frequency components, therefore a filter with 0.3 Hz cutoff frequency was used. From each window, a vector of features was obtained by calculating variables from the time and frequency domain. 


#Input Variable Information:

For each record in the dataset the following is provided:
.Triaxial acceleration from the accelerometer (total acceleration) and the estimated body acceleration.
.Triaxial Angular velocity from the gyroscope.
.A 561-feature vector with time and frequency domain variables.
.The activity label.
.An identifier of the subject who carried out the experiment. 

Please refer to Readme file into 'UCI HAR Dataset' for more information.


#Raw Data transformation

The raw data sets are processed with the script run_analysis.R script to create a tidy data set.
Merge training and test sets Test and training data, subject ids and activity ids are merged to obtain a single data set. Variables are labelled with the names assigned by original collectors.
Extract mean and standard deviation variables Keep only the values of estimated mean and standard deviation .
Get descriptive activity names A new column is added to intermediate data set with the activity description.
Label variables appropriately from the original collectors were changed to get valid/more descriptive activity names 
Create a tidy data set From the intermediate data set is created a final tidy data set where numeric variables are averaged for each activity and each subject.

#Output Variables

The following table shows a table with all variables in the output file. The first column in the table shows the column number of the variable, the second column shows the variable name and column three shows the source variable used to compute the value of the variable.

No|Variables|Source Variables
--|:--------|:--------------
1|subject|subject id from subjects file
2|activity|activity id from labels file
3|timeBodyAccelerometer-Mean-X|tBodyAcc-mean()-X
4|timeBodyAccelerometer-Mean-Y|tBodyAcc-mean()-Y
5|timeBodyAccelerometer-Mean-Z|tBodyAcc-mean()-Z
6|timeBodyAccelerometer-StandardDeviation-X|tBodyAcc-std()-X
7|timeBodyAccelerometer-StandardDeviation-Y|tBodyAcc-std()-Y
8|timeBodyAccelerometer-StandardDeviation-Z|tBodyAcc-std()-Z
9|timeGravityAccelerometer-Mean-X|tGravityAcc-mean()-X
10|timeGravityAccelerometer-Mean-Y|tGravityAcc-mean()-Y
11|timeGravityAccelerometer-Mean-Z|tGravityAcc-mean()-Z
12|timeGravityAccelerometer-StandardDeviation-X|tGravityAcc-std()-X
13|timeGravityAccelerometer-StandardDeviation-Y|tGravityAcc-std()-Y
14|timeGravityAccelerometer-StandardDeviation-Z|tGravityAcc-std()-Z
15|timeBodyAccelerometerJerk-Mean-X|tBodyAccJerk-mean()-X
16|timeBodyAccelerometerJerk-Mean-Y|tBodyAccJerk-mean()-Y
17|timeBodyAccelerometerJerk-Mean-Z|tBodyAccJerk-mean()-Z
18|timeBodyAccelerometerJerk-StandardDeviation-X|tBodyAccJerk-std()-X
19|timeBodyAccelerometerJerk-StandardDeviation-Y|tBodyAccJerk-std()-Y
20|timeBodyAccelerometerJerk-StandardDeviation-Z|tBodyAccJerk-std()-Z
21|timeBodyGyroscope-Mean-X|tBodyGyro-mean()-X
22|timeBodyGyroscope-Mean-Y|tBodyGyro-mean()-Y
23|timeBodyGyroscope-Mean-Z|tBodyGyro-mean()-Z
24|timeBodyGyroscope-StandardDeviation-X|tBodyGyro-std()-X
25|timeBodyGyroscope-StandardDeviation-Y|tBodyGyro-std()-Y
26|timeBodyGyroscope-StandardDeviation-Z|tBodyGyro-std()-Z
27|timeBodyGyroscopeJerk-Mean-X|tBodyGyroJerk-mean()-X
28|timeBodyGyroscopeJerk-Mean-Y|tBodyGyroJerk-mean()-Y
29|timeBodyGyroscopeJerk-Mean-Z|tBodyGyroJerk-mean()-Z
30|timeBodyGyroscopeJerk-StandardDeviation-X|tBodyGyroJerk-std()-X
31|timeBodyGyroscopeJerk-StandardDeviation-Y|tBodyGyroJerk-std()-Y
32|timeBodyGyroscopeJerk-StandardDeviation-Z|tBodyGyroJerk-std()-Z
33|timeBodyAccelerometerMagnitude-Mean|tBodyAccMag-mean()
34|timeBodyAccelerometerMagnitude-StandardDeviation|tBodyAccMag-std()
35|timeGravityAccelerometerMagnitude-Mean|tGravityAccMag-mean()
36|timeGravityAccelerometerMagnitude-StandardDeviation|tGravityAccMag-std()
37|timeBodyAccelerometerJerkMagnitude-Mean|tBodyAccJerkMag-mean()
38|timeBodyAccelerometerJerkMagnitude-StandardDeviation|tBodyAccJerkMag-std()
39|timeBodyGyroscopeMagnitude-Mean|tBodyGyroMag-mean()
40|timeBodyGyroscopeMagnitude-StandardDeviation|tBodyGyroMag-std()
41|timeBodyGyroscopeJerkMagnitude-Mean|tBodyGyroJerkMag-mean()
42|timeBodyGyroscopeJerkMagnitude-StandardDeviation|tBodyGyroJerkMag-std()
43|frequencyBodyAccelerometer-Mean-X|fBodyAcc-mean()-X
44|frequencyBodyAccelerometer-Mean-Y|fBodyAcc-mean()-Y
45|frequencyBodyAccelerometer-Mean-Z|fBodyAcc-mean()-Z
46|frequencyBodyAccelerometer-StandardDeviation-X|fBodyAcc-std()-X
47|frequencyBodyAccelerometer-StandardDeviation-Y|fBodyAcc-std()-Y
48|frequencyBodyAccelerometer-StandardDeviation-Z|fBodyAcc-std()-Z
49|frequencyBodyAccelerometerJerk-Mean-X|fBodyAccJerk-mean()-X
50|frequencyBodyAccelerometerJerk-Mean-Y|fBodyAccJerk-mean()-Y
51|frequencyBodyAccelerometerJerk-Mean-Z|fBodyAccJerk-mean()-Z
52|frequencyBodyAccelerometerJerk-StandardDeviation-X|fBodyAccJerk-std()-X
53|frequencyBodyAccelerometerJerk-StandardDeviation-Y|fBodyAccJerk-std()-Y
54|frequencyBodyAccelerometerJerk-StandardDeviation-Z|fBodyAccJerk-std()-Z
55|frequencyBodyGyroscope-Mean-X|fBodyGyro-mean()-X
56|frequencyBodyGyroscope-Mean-Y|fBodyGyro-mean()-Y
57|frequencyBodyGyroscope-Mean-Z|fBodyGyro-mean()-Z
58|frequencyBodyGyroscope-StandardDeviation-X|fBodyGyro-std()-X
59|frequencyBodyGyroscope-StandardDeviation-Y|fBodyGyro-std()-Y
60|frequencyBodyGyroscope-StandardDeviation-Z|fBodyGyro-std()-Z
61|frequencyBodyAccelerometerMagnitude-Mean|fBodyAccMag-mean()
62|frequencyBodyAccelerometerMagnitude-StandardDeviation|fBodyAccMag-std()
63|frequencyBodyAccelerometerJerkMagnitude-Mean|fBodyBodyAccJerkMag-mean()
64|frequencyBodyAccelerometerJerkMagnitude-StandardDeviation|fBodyBodyAccJerkMag-std()
65|frequencyBodyGyroscopeMagnitude-Mean|fBodyBodyGyroMag-mean()
66|frequencyBodyGyroscopeMagnitude-StandardDeviation|fBodyBodyGyroMag-std()
67|frequencyBodyGyroscopeJerkMagnitude-Mean|fBodyBodyGyroJerkMag-mean()
68|frequencyBodyGyroscopeJerkMagnitude-StandardDeviation|fBodyBodyGyroJerkMag-std()



The source variables consist of the following parts:
The first letter defines the domain: t for time or f for frequency
The next part defines the source variable: BodyAcc (BodyAcceleration), GravityAcc (GravityAcceleration) or BodyGyro (BodyGyroscope)
The next (optional) part describes the method that was used to derive the variable: Mag (Magnitued), Jerk or JerkMag (JerkMagnitude)
The part after the dash describes the function that was used to compute the feature mean (Mean) or std (Standarddeviation)
In case of three axial measurements, the last part of the variable defines the axis (X, Y or Z)

#Output Variable Units

* subject: identifier of an observed volunteer within an age bracket of 19-48 years.
    * Data type: Numeric
    * Value range: 1 - 30
* activity: Label string of the observed activity a person was performing
    * Data type: factor
    * Labels: WALKING, WALKING_UPSTAIRS, WALKING_DOWNSTAIRS, SITTING, STANDING, LAYING
* Rows 3 - 68: Means of selected features per subject and activity
    * Data type: The feature means have the same units as their input data. Due to the normalization they do not have units attached
    * Value range: [-1, 1]

#Tidy Data

The tidy data set contains :

* Subject : Identifier of the subject who carried out the experiment. Its range is from 1 to 30. 
* Activity : Activity label: Walking, Walking Upstairs, Walking Downstairs, Sitting, Standing, Laying
* Mean of all other variables are measurement collected from the accelerometer and gyroscope 3-axial raw signal (numeric value)

The data set is written to the file 'tidydata.txt'.
The tidy data set a set of variables for each activity and each subject. 10299 instances are split into 180 groups (30 subjects and 6 activities) and 66 mean and standard deviation features are averaged for each group. The resulting data table has 180 rows and 69 columns – 33 Mean variables + 33 Standard deviation variables + 1 Subject( 1 of of the 30 test subjects) + ActivityName + ActivityNum . The tidy data set’s first row is the header containing the names for each column.
