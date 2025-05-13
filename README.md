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





