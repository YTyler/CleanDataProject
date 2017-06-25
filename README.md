# CleanDataProject

#create directory for data and set working directory
if (!file.exists("./data")){dir.create("./data")}
setwd("./data")
#download zip file of data
fileURL = "https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip"
download.file(fileURL, destfile = "uci", mode = "wb")

unzip("./uci")

#Load dplyr package
library(dplyr)

#Read datasets from file
test <- read.table("./UCI HAR Dataset/test/X_test.txt")
telab <- read.table("./UCI HAR Dataset/test/y_test.txt")
tesub <- read.table("./UCI HAR Dataset/test/subject_test.txt")
train <- read.table("./UCI HAR Dataset/train/X_train.txt")
trlab <- read.table("./UCI HAR Dataset/train/y_train.txt")
trsub <- read.table("./UCI HAR Dataset/train/subject_train.txt")
act <- read.table("./UCI HAR Dataset/activity_labels.txt")
feat <- read.table("./UCI HAR Dataset/features.txt")

#Rename variables in primary datasets
names(test) <- feat$V2
names(train) <- feat$V2

#Code activity column & remove underscores
telab <- factor(telab$V1, levels = 1:6, labels = act$V2)
trlab <- factor(trlab$V1, levels = 1:6, labels = act$V2)
telab <- gsub("_","",telab)
trlab <- gsub("_","",trlab)
#Add subject & activity to datasets
test <- cbind("id" =  tesub$V1, "activity" = telab, test)
train <- cbind("id" =  trsub$V1, "activity" = trlab, train)

#Merge Primary Datasets
total <- bind_rows(test,train)

#Select mean & standard deviation variables
total <- select(total, 1:2,contains("mean()"),contains("std()"))
#Creates data set with the average of each variable for each activity and each subject
means <- group_by(total,id,activity)
means <- summarise_all(means,funs(mean))
#Renames variables for means dataset
meanlab <- gsub("^t","Average of t",names(means))
meanlab <- gsub("^f","Average of f",meanlab)
names(means) <- meanlab
View(means)
