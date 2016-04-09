---
title: "CodeBook.rmd"
author: "Emily Smenderovac"
date: "April 8, 2016"
output: html_document
---











Number of measurements on Standard Deviation and Mean: 66

Original variables from X_test.txt and X_train.txt summarized: 


```
##  [1] "tBodyAcc-mean()-X"           "tBodyAcc-mean()-Y"          
##  [3] "tBodyAcc-mean()-Z"           "tBodyAcc-std()-X"           
##  [5] "tBodyAcc-std()-Y"            "tBodyAcc-std()-Z"           
##  [7] "tGravityAcc-mean()-X"        "tGravityAcc-mean()-Y"       
##  [9] "tGravityAcc-mean()-Z"        "tGravityAcc-std()-X"        
## [11] "tGravityAcc-std()-Y"         "tGravityAcc-std()-Z"        
## [13] "tBodyAccJerk-mean()-X"       "tBodyAccJerk-mean()-Y"      
## [15] "tBodyAccJerk-mean()-Z"       "tBodyAccJerk-std()-X"       
## [17] "tBodyAccJerk-std()-Y"        "tBodyAccJerk-std()-Z"       
## [19] "tBodyGyro-mean()-X"          "tBodyGyro-mean()-Y"         
## [21] "tBodyGyro-mean()-Z"          "tBodyGyro-std()-X"          
## [23] "tBodyGyro-std()-Y"           "tBodyGyro-std()-Z"          
## [25] "tBodyGyroJerk-mean()-X"      "tBodyGyroJerk-mean()-Y"     
## [27] "tBodyGyroJerk-mean()-Z"      "tBodyGyroJerk-std()-X"      
## [29] "tBodyGyroJerk-std()-Y"       "tBodyGyroJerk-std()-Z"      
## [31] "tBodyAccMag-mean()"          "tBodyAccMag-std()"          
## [33] "tGravityAccMag-mean()"       "tGravityAccMag-std()"       
## [35] "tBodyAccJerkMag-mean()"      "tBodyAccJerkMag-std()"      
## [37] "tBodyGyroMag-mean()"         "tBodyGyroMag-std()"         
## [39] "tBodyGyroJerkMag-mean()"     "tBodyGyroJerkMag-std()"     
## [41] "fBodyAcc-mean()-X"           "fBodyAcc-mean()-Y"          
## [43] "fBodyAcc-mean()-Z"           "fBodyAcc-std()-X"           
## [45] "fBodyAcc-std()-Y"            "fBodyAcc-std()-Z"           
## [47] "fBodyAccJerk-mean()-X"       "fBodyAccJerk-mean()-Y"      
## [49] "fBodyAccJerk-mean()-Z"       "fBodyAccJerk-std()-X"       
## [51] "fBodyAccJerk-std()-Y"        "fBodyAccJerk-std()-Z"       
## [53] "fBodyGyro-mean()-X"          "fBodyGyro-mean()-Y"         
## [55] "fBodyGyro-mean()-Z"          "fBodyGyro-std()-X"          
## [57] "fBodyGyro-std()-Y"           "fBodyGyro-std()-Z"          
## [59] "fBodyAccMag-mean()"          "fBodyAccMag-std()"          
## [61] "fBodyBodyAccJerkMag-mean()"  "fBodyBodyAccJerkMag-std()"  
## [63] "fBodyBodyGyroMag-mean()"     "fBodyBodyGyroMag-std()"     
## [65] "fBodyBodyGyroJerkMag-mean()" "fBodyBodyGyroJerkMag-std()"
```




Final data variables renamed:

```
##  [1] "subject"                                                   
##  [2] "activity"                                                  
##  [3] "datset"                                                    
##  [4] "timeBodyAccelerationAccelerometer-mean()-X"                
##  [5] "timeBodyAccelerationAccelerometer-mean()-Y"                
##  [6] "timeBodyAccelerationAccelerometer-mean()-Z"                
##  [7] "timeBodyAccelerationAccelerometer-std()-X"                 
##  [8] "timeBodyAccelerationAccelerometer-std()-Y"                 
##  [9] "timeBodyAccelerationAccelerometer-std()-Z"                 
## [10] "timeGravityAccelerometer-mean()-X"                         
## [11] "timeGravityAccelerometer-mean()-Y"                         
## [12] "timeGravityAccelerometer-mean()-Z"                         
## [13] "timeGravityAccelerometer-std()-X"                          
## [14] "timeGravityAccelerometer-std()-Y"                          
## [15] "timeGravityAccelerometer-std()-Z"                          
## [16] "timeBodyAccelerationAccelerometerJerk-mean()-X"            
## [17] "timeBodyAccelerationAccelerometerJerk-mean()-Y"            
## [18] "timeBodyAccelerationAccelerometerJerk-mean()-Z"            
## [19] "timeBodyAccelerationAccelerometerJerk-std()-X"             
## [20] "timeBodyAccelerationAccelerometerJerk-std()-Y"             
## [21] "timeBodyAccelerationAccelerometerJerk-std()-Z"             
## [22] "timeBodyAccelerationGyroscope-mean()-X"                    
## [23] "timeBodyAccelerationGyroscope-mean()-Y"                    
## [24] "timeBodyAccelerationGyroscope-mean()-Z"                    
## [25] "timeBodyAccelerationGyroscope-std()-X"                     
## [26] "timeBodyAccelerationGyroscope-std()-Y"                     
## [27] "timeBodyAccelerationGyroscope-std()-Z"                     
## [28] "timeBodyAccelerationGyroscopeJerk-mean()-X"                
## [29] "timeBodyAccelerationGyroscopeJerk-mean()-Y"                
## [30] "timeBodyAccelerationGyroscopeJerk-mean()-Z"                
## [31] "timeBodyAccelerationGyroscopeJerk-std()-X"                 
## [32] "timeBodyAccelerationGyroscopeJerk-std()-Y"                 
## [33] "timeBodyAccelerationGyroscopeJerk-std()-Z"                 
## [34] "timeBodyAccelerationAccelerometerMagnitude-mean()"         
## [35] "timeBodyAccelerationAccelerometerMagnitude-std()"          
## [36] "timeGravityAccelerometerMagnitude-mean()"                  
## [37] "timeGravityAccelerometerMagnitude-std()"                   
## [38] "timeBodyAccelerationAccelerometerJerkMagnitude-mean()"     
## [39] "timeBodyAccelerationAccelerometerJerkMagnitude-std()"      
## [40] "timeBodyAccelerationGyroscopeMagnitude-mean()"             
## [41] "timeBodyAccelerationGyroscopeMagnitude-std()"              
## [42] "timeBodyAccelerationGyroscopeJerkMagnitude-mean()"         
## [43] "timeBodyAccelerationGyroscopeJerkMagnitude-std()"          
## [44] "frequencyBodyAccelerationAccelerometer-mean()-X"           
## [45] "frequencyBodyAccelerationAccelerometer-mean()-Y"           
## [46] "frequencyBodyAccelerationAccelerometer-mean()-Z"           
## [47] "frequencyBodyAccelerationAccelerometer-std()-X"            
## [48] "frequencyBodyAccelerationAccelerometer-std()-Y"            
## [49] "frequencyBodyAccelerationAccelerometer-std()-Z"            
## [50] "frequencyBodyAccelerationAccelerometerJerk-mean()-X"       
## [51] "frequencyBodyAccelerationAccelerometerJerk-mean()-Y"       
## [52] "frequencyBodyAccelerationAccelerometerJerk-mean()-Z"       
## [53] "frequencyBodyAccelerationAccelerometerJerk-std()-X"        
## [54] "frequencyBodyAccelerationAccelerometerJerk-std()-Y"        
## [55] "frequencyBodyAccelerationAccelerometerJerk-std()-Z"        
## [56] "frequencyBodyAccelerationGyroscope-mean()-X"               
## [57] "frequencyBodyAccelerationGyroscope-mean()-Y"               
## [58] "frequencyBodyAccelerationGyroscope-mean()-Z"               
## [59] "frequencyBodyAccelerationGyroscope-std()-X"                
## [60] "frequencyBodyAccelerationGyroscope-std()-Y"                
## [61] "frequencyBodyAccelerationGyroscope-std()-Z"                
## [62] "frequencyBodyAccelerationAccelerometerMagnitude-mean()"    
## [63] "frequencyBodyAccelerationAccelerometerMagnitude-std()"     
## [64] "frequencyBodyAccelerationAccelerometerJerkMagnitude-mean()"
## [65] "frequencyBodyAccelerationAccelerometerJerkMagnitude-std()" 
## [66] "frequencyBodyAccelerationGyroscopeMagnitude-mean()"        
## [67] "frequencyBodyAccelerationGyroscopeMagnitude-std()"         
## [68] "frequencyBodyAccelerationGyroscopeJerkMagnitude-mean()"    
## [69] "frequencyBodyAccelerationGyroscopeJerkMagnitude-std()"
```
Summary applied to data :  mean

Data summaries were based on euclidean vector data in a range of -1 : 1.






