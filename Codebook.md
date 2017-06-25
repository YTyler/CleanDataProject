id		2
	Unique Participant Identifier
		01-30
activity
	Experimental Condition Category
		1. LAYING
		2. SITTING
		3. STANDING
		4. WALKING
		5. WALKINGDOWNSTAIRS
		6. WALKINGUPSTAIRS

Additional Variables (see notes below for description)
	Average of tBodyAcc-mean()-X
	Average of tBodyAcc-mean()-Y
	Average of tBodyAcc-mean()-Z
	Average of tGravityAcc-mean()-X
	Average of tGravityAcc-mean()-Y
	Average of tGravityAcc-mean()-Z
	Average of tBodyAccJerk-mean()-X
	Average of tBodyAccJerk-mean()-Y
	Average of tBodyAccJerk-mean()-Z
	Average of tBodyGyro-mean()-X
	Average of tBodyGyro-mean()-Y
	Average of tBodyGyro-mean()-Z
	Average of tBodyGyroJerk-mean()-X
	Average of tBodyGyroJerk-mean()-Y
	Average of tBodyGyroJerk-mean()-Z
	Average of tBodyAccMag-mean()
	Average of tGravityAccMag-mean()
	Average of tBodyAccJerkMag-mean()
	Average of tBodyGyroMag-mean()
	Average of tBodyGyroJerkMag-mean()
	Average of fBodyAcc-mean()-X
	Average of fBodyAcc-mean()-Y
	Average of fBodyAcc-mean()-Z
	Average of fBodyAccJerk-mean()-X
	Average of fBodyAccJerk-mean()-Y
	Average of fBodyAccJerk-mean()-Z
	Average of fBodyGyro-mean()-X
	Average of fBodyGyro-mean()-Y
	Average of fBodyGyro-mean()-Z
	Average of fBodyAccMag-mean()
	Average of fBodyBodyAccJerkMag-mean()
	Average of fBodyBodyGyroMag-mean()
	Average of fBodyBodyGyroJerkMag-mean()
	Average of tBodyAcc-std()-X
	Average of tBodyAcc-std()-Y
	Average of tBodyAcc-std()-Z
	Average of tGravityAcc-std()-X
	Average of tGravityAcc-std()-Y
	Average of tGravityAcc-std()-Z
	Average of tBodyAccJerk-std()-X
	Average of tBodyAccJerk-std()-Y
	Average of tBodyAccJerk-std()-Z
	Average of tBodyGyro-std()-X
	Average of tBodyGyro-std()-Y
	Average of tBodyGyro-std()-Z
	Average of tBodyGyroJerk-std()-X
	Average of tBodyGyroJerk-std()-Y
	Average of tBodyGyroJerk-std()-Z
	Average of tBodyAccMag-std()
	Average of tGravityAccMag-std()
	Average of tBodyAccJerkMag-std()
	Average of tBodyGyroMag-std()
	Average of tBodyGyroJerkMag-std()
	Average of fBodyAcc-std()-X
	Average of fBodyAcc-std()-Y
	Average of fBodyAcc-std()-Z
	Average of fBodyAccJerk-std()-X
	Average of fBodyAccJerk-std()-Y
	Average of fBodyAccJerk-std()-Z
	Average of fBodyGyro-std()-X
	Average of fBodyGyro-std()-Y
	Average of fBodyGyro-std()-Z
	Average of fBodyAccMag-std()
	Average of fBodyBodyAccJerkMag-std()
	Average of fBodyBodyGyroMag-std()
	Average of fBodyBodyGyroJerkMag-std()

Notes:

The features selected for this database come from the accelerometer and gyroscope 3-axial raw signals tAcc-XYZ and tGyro-XYZ. 
These time domain signals (prefix 't' to denote time) were captured at a constant rate of 50 Hz. Then they were filtered using a median filter and a 3rd order 
low pass Butterworth filter with a corner frequency of 20 Hz to remove noise. Similarly, the acceleration signal was then separated into body and gravity acceleration 
signals (tBodyAcc-XYZ and tGravityAcc-XYZ) using another low pass Butterworth filter with a corner frequency of 0.3 Hz. 
 
Subsequently, the body linear acceleration and angular velocity were derived in time to obtain Jerk signals (tBodyAccJerk-XYZ and tBodyGyroJerk-XYZ). Also the magnitude 
of these three-dimensional signals were calculated using the Euclidean norm (tBodyAccMag, tGravityAccMag, tBodyAccJerkMag, tBodyGyroMag, tBodyGyroJerkMag). 
 
Finally a Fast Fourier Transform (FFT) was applied to some of these signals producing fBodyAcc-XYZ, fBodyAccJerk-XYZ, fBodyGyro-XYZ, fBodyAccJerkMag, fBodyGyroMag, 
fBodyGyroJerkMag. (Note the 'f' to indicate frequency domain signals). 
 
These signals were used to estimate variables of the feature vector for each pattern:  
'-XYZ' is used to denote 3-axial signals in the X, Y and Z directions.

The additional variables seen above were computed by taking the average of every measurement for
each participant (as denoted by id) and experimental condition (denoted by activity)