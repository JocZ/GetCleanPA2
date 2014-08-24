###Code Book

The Code Book describes the variables, the data, and any transformations and any work performed to clean up the data.

###Raw Data

The raw data used in this analysis represent data collected from the accelerometers from the Samsung Galaxy S smartphone. A full description is available at the site where the data was obtained:

http://archive.ics.uci.edu/ml/datasets/Human+Activity+Recognition+Using+Smartphones

The data used is located here:

https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip

The dataset includes the following files:
=========================================

- 'features_info.txt': Shows information about the variables used on the feature vector.

- 'features.txt': List of all features.

- 'activity_labels.txt': Links the class labels with their activity name.

- 'train/X_train.txt': Training set.

- 'train/y_train.txt': Training labels.

- 'test/X_test.txt': Test set.

- 'test/y_test.txt': Test labels.

The following files are available for the train and test data. Their descriptions are equivalent. 

- 'train/subject_train.txt': Each row identifies the subject who performed the activity for each window sample. Its range is from 1 to 30. 


These signals were used to estimate variables of the feature vector for each pattern:  
'-XYZ' is used to denote 3-axial signals in the X, Y and Z directions.

tBodyAcc-XYZ
tGravityAcc-XYZ
tBodyAccJerk-XYZ
tBodyGyro-XYZ
tBodyGyroJerk-XYZ
tBodyAccMag
tGravityAccMag
tBodyAccJerkMag
tBodyGyroMag
tBodyGyroJerkMag
fBodyAcc-XYZ
fBodyAccJerk-XYZ
fBodyGyro-XYZ
fBodyAccMag
fBodyAccJerkMag
fBodyGyroMag
fBodyGyroJerkMag

The set of variables that were estimated from these signals are: 

mean(): Mean value
std(): Standard deviation
mad(): Median absolute deviation 
max(): Largest value in array
min(): Smallest value in array
sma(): Signal magnitude area
energy(): Energy measure. Sum of the squares divided by the number of values. 
iqr(): Interquartile range 
entropy(): Signal entropy
arCoeff(): Autorregresion coefficients with Burg order equal to 4
correlation(): correlation coefficient between two signals
maxInds(): index of the frequency component with largest magnitude
meanFreq(): Weighted average of the frequency components to obtain a mean frequency
skewness(): skewness of the frequency domain signal 
kurtosis(): kurtosis of the frequency domain signal 
bandsEnergy(): Energy of a frequency interval within the 64 bins of the FFT of each window.
angle(): Angle between to vectors.

### Transformation and Clean Up

the data resulting from the union of training and testing data  have 10299 observations and 561 variables. Afer adding the names and selecting the varibles related to mean and standar deviation, the resulting dataframe has 88 variables:

[1] "subjects"                             "tBodyAcc-mean()-X"                   
 [3] "tBodyAcc-mean()-Y"                    "tBodyAcc-mean()-Z"                   
 [5] "tBodyAcc-std()-X"                     "tBodyAcc-std()-Y"                    
 [7] "tBodyAcc-std()-Z"                     "tGravityAcc-mean()-X"                
 [9] "tGravityAcc-mean()-Y"                 "tGravityAcc-mean()-Z"                
[11] "tGravityAcc-std()-X"                  "tGravityAcc-std()-Y"                 
[13] "tGravityAcc-std()-Z"                  "tBodyAccJerk-mean()-X"               
[15] "tBodyAccJerk-mean()-Y"                "tBodyAccJerk-mean()-Z"               
[17] "tBodyAccJerk-std()-X"                 "tBodyAccJerk-std()-Y"                
[19] "tBodyAccJerk-std()-Z"                 "tBodyGyro-mean()-X"                  
[21] "tBodyGyro-mean()-Y"                   "tBodyGyro-mean()-Z"                  
[23] "tBodyGyro-std()-X"                    "tBodyGyro-std()-Y"                   
[25] "tBodyGyro-std()-Z"                    "tBodyGyroJerk-mean()-X"              
[27] "tBodyGyroJerk-mean()-Y"               "tBodyGyroJerk-mean()-Z"              
[29] "tBodyGyroJerk-std()-X"                "tBodyGyroJerk-std()-Y"               
[31] "tBodyGyroJerk-std()-Z"                "tBodyAccMag-mean()"                  
[33] "tBodyAccMag-std()"                    "tGravityAccMag-mean()"               
[35] "tGravityAccMag-std()"                 "tBodyAccJerkMag-mean()"              
[37] "tBodyAccJerkMag-std()"                "tBodyGyroMag-mean()"                 
[39] "tBodyGyroMag-std()"                   "tBodyGyroJerkMag-mean()"             
[41] "tBodyGyroJerkMag-std()"               "fBodyAcc-mean()-X"                   
[43] "fBodyAcc-mean()-Y"                    "fBodyAcc-mean()-Z"                   
[45] "fBodyAcc-std()-X"                     "fBodyAcc-std()-Y"                    
[47] "fBodyAcc-std()-Z"                     "fBodyAcc-meanFreq()-X"               
[49] "fBodyAcc-meanFreq()-Y"                "fBodyAcc-meanFreq()-Z"               
[51] "fBodyAccJerk-mean()-X"                "fBodyAccJerk-mean()-Y"               
[53] "fBodyAccJerk-mean()-Z"                "fBodyAccJerk-std()-X"                
[55] "fBodyAccJerk-std()-Y"                 "fBodyAccJerk-std()-Z"                
[57] "fBodyAccJerk-meanFreq()-X"            "fBodyAccJerk-meanFreq()-Y"           
[59] "fBodyAccJerk-meanFreq()-Z"            "fBodyGyro-mean()-X"                  
[61] "fBodyGyro-mean()-Y"                   "fBodyGyro-mean()-Z"                  
[63] "fBodyGyro-std()-X"                    "fBodyGyro-std()-Y"                   
[65] "fBodyGyro-std()-Z"                    "fBodyGyro-meanFreq()-X"              
[67] "fBodyGyro-meanFreq()-Y"               "fBodyGyro-meanFreq()-Z"              
[69] "fBodyAccMag-mean()"                   "fBodyAccMag-std()"                   
[71] "fBodyAccMag-meanFreq()"               "fBodyBodyAccJerkMag-mean()"          
[73] "fBodyBodyAccJerkMag-std()"            "fBodyBodyAccJerkMag-meanFreq()"      
[75] "fBodyBodyGyroMag-mean()"              "fBodyBodyGyroMag-std()"              
[77] "fBodyBodyGyroMag-meanFreq()"          "fBodyBodyGyroJerkMag-mean()"         
[79] "fBodyBodyGyroJerkMag-std()"           "fBodyBodyGyroJerkMag-meanFreq()"     
[81] "angle(tBodyAccMean,gravity)"          "angle(tBodyAccJerkMean),gravityMean)"
[83] "angle(tBodyGyroMean,gravityMean)"     "angle(tBodyGyroJerkMean,gravityMean)"
[85] "angle(X,gravityMean)"                 "angle(Y,gravityMean)"                
[87] "angle(Z,gravityMean)"                 "activity"                            


The tidy tidy data created represents a summary for each subject of each activity.  
