## Introduction

This repository contains the Jupyter Notebook for the Application Assignment 11.1. This takes a sample jupyter notebook to complete the exercise to analyse Kaggle used car data in vehicles.csv file in the data folder of this repository to build a machine learning application that evaluates if vehicles features like Fuel, Condition, Size, Type, Color etc. can be used to determine used car prices for the Car Dealership and Sales Team. This evaluation will help the Car Dealership with fine tuning their inventory by stocking cars that consumers are interested in.

### How to use the files in this repository?
The notebooks are grouped into the following categories:

data – vehicles.csv data file from Kaggle Machine Learning dataset repository used in the notebooks
images – Image files used in Notebook and Project Description
notebook – What Drives the Price of a Car Notebook

## Business Understanding

During meiosis, how many times does the cell go through interphase and replicate its DNA?

twice

zero

once

It depends on whether the cell is a germ cell or a somatic cell.

<img width="1142" alt="image" src="https://github.com/user-attachments/assets/a88cc711-b632-4476-91ae-4414f409b388" />





## Data Understanding

The first thing that was apparent from the provided data was that it was not clean, it had missing values and some of the values were not realistic for used cars, for example, odometer with zero and single digit values; price with zero and single digits values.

<img width="1095" alt="image" src="https://github.com/user-attachments/assets/a6a6921f-ba0e-4a65-b571-f784dfed543b" />

As you can see from the Diagram above, there are car prices with zero value for all conditions.

## Data Preparation

Summary of the Data Preparation is as follows:

. Remove records with Zero Prices and Odometer values

. Remove records where some of the factors are not populated

. Drop a number of factors (i.e., VIN, id, region etc.) that are not significant in user car price determination

. Review and remove the other factors (i.e., state, paint color, manufacturer, transmission etc.) and check if they have an impact on car price based on the provided data

. Filtering the data based on year on manufacture = 1990 as the number of vehicles before 1990 were very low

<img width="959" alt="image" src="https://github.com/user-attachments/assets/d75be7f5-553f-4aa0-8024-531a0d285179" />


## Regression Models

We ran a number of models (7 to be exact) to create 7 ML Models or AI Applications using the full set of features after data manipulation and a subset of features based on the correlation matrix between the features and used car prices.

Additional filtering (i.e., Price and Odometer > 5000 and Year > 1990) were also used to create datasets used from some of the models below.

For Most of these Models, the accuracy was less than 50% with the exception of the last 2 models. See table below:

<img width="1013" alt="image" src="https://github.com/user-attachments/assets/fda644e4-1d44-40fc-b31a-4110c4ef17a1" />

her accuracy score with the highest score for training and testing data currently less than 50%

It's also not a coincidence that the highest score of 47.52% and 48.26% reflects the highest numbers for correlation between these features and price from the correlation matrix.

## Findings

In testing these models with the inputs, we observed the following for used car prices:

<img width="995" alt="image" src="https://github.com/user-attachments/assets/0ecb10ad-2a98-45e5-80bb-015df12451a4" />

As you can see, the Machine Learning application "Model" built using all the final dataset from the data manipulation phase which included features like Odometer, Year, Condition, fuel type, drive train and size returns a negative value (i.e., -$98,263.87) which is not realistic for a "new car with 100 miles, condition excellent and new with diesel and four wheel drive".

Same Model returned $29,013.33 for new car with 100 miles, condition good and with Electric and front wheel drive.

For ML Applications Model6 and Model7 which are the recommended/selected models, see below for the prediction testing results:

<img width="1018" alt="image" src="https://github.com/user-attachments/assets/3b57b4b8-6f0f-4ae9-bbc7-cb7325ecfe7b" />

When we analyze the importance of feature selection based on the trained model, we observe the following order

Model6 - Diesel Fuel, Odometer, Four Wheel Drive, Full Size and Year
Model7 - Diesel Fuel, Year, Odometer, Four Wheel Drive and Full Size
Next Steps and Recommendations
As the data provided is not that clean with null, NAN, zero, missing and unrealistic values, further filering of the data could be done, for example, selecting used car records with year => 2000.

<img width="911" alt="image" src="https://github.com/user-attachments/assets/e5eb8c5a-52eb-400d-aef9-8bceac93289a" />

This should allow the model to use more of the newer car features like model, cylinders, drive, size which may have a greater influence on newer used car prices with lower odometer. This may also lead to a higher/better model accuracy (i.e., > 50%)

More and better data can be collected to train the model. This data should include the newer features on used cars like Automated Driving Safety Features, Infotainment, Cameras, Remote Start, Car Mileage which have an impact on used car prices.

Additional Data on used car datasets can be downloaded from Kaggle Used Cars Datasets

We would recommend some form of classification/categories for features like paint_color, state etc so that we can include them with fewer permutations in the model.

From the current models created, Model6 and Model7 would be the recommended models to use.

These models were built with the following logic:

Model6 - Odometer and Price greater than 5000, Odometer, Year, fuel_diesel, drive_4wd and size_full-size as the only inputs

Model7 - Odometer and Price greater than 5000, Odometer, Year > 1990, Year, fuel_diesel, drive_4wd and size_full-size as the only inputs

These models provided the following model feature selection:

Model6 - Diesel Fuel, Odometer, Four Wheel Drive, Full Size and Year

Model7 - Diesel Fuel, Year, Odometer, Four Wheel Drive and Full Size

For Next Steps, while the recommended models (i.e., Model7 etc.) can be deployed, we would also recommend gathering more quality data that would produce a model with an accuracy of 75%+ based on used cars data no more than 10-15 years old.

Updated data should also provide a better indication on the latest features that consumers are looking for so that the Dealership can source these cars for their inventory.


