# Richter-s-Predictor-Modeling-Earthquake-Damage
https://www.drivendata.org/competitions/57/nepal-earthquake/

<img src="https://s3.amazonaws.com/drivendata-public-assets/nepal-quake-bm-2.JPG">

#### Problem Statement

We're trying to predict the ordinal variable damage_grade, which represents a level of damage to the building that was hit by the earthquake. There are 3 grades of the damage:

1. represents low damage
2. represents a medium amount of damage
3. represents almost complete destruction

#### Features

The dataset mainly consists of information on the buildings' structure and their legal ownership. Each row in the dataset represents a specific building in the region that was hit by Gorkha earthquake.

There are 39 columns in this dataset, where the building_id column is a unique and random identifier. The remaining 38 features are described in the section below. Categorical variables have been obfuscated random lowercase ascii characters. The appearance of the same character in distinct columns does not imply the same original value.

#### Performance metric

We are predicting the level of damage from 1 to 3. The level of damage is an ordinal variable meaning that ordering is important. This can be viewed as a classification or an ordinal regression problem. (Ordinal regression is sometimes described as an problem somewhere in between classification and regression.)

To measure the performance of our algorithms, we'll use the F1 score which balances the precision and recall of a classifier. Traditionally, the F1 score is used to evaluate performance on a binary classifier, but since we have three possible labels we will use a variant called the micro averaged F1 score.

#### Submission format

The format for the submission file is two columns with the building_id and the damage_grade. The data type of damage_grade is an integer with values of 1,2,3, so make sure there is no decimal point and no other numbers in your submission. For example 1 would be valid, and 1.0 would not.

The first few lines of the .csv file that you submit would look like:

building_id | damage_grade
------------ | -------------
11456 | 1
16528 | 1
