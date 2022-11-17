# Capstone Project Module 3: Travel Insurance Claim Prediction
Supervised Machine Learning

This repository was made for writer's study purpose as a Data Scientist and Machine Learning student in Purwadhika Digital Technologi School.

## Introduction
The data set contains a series of travel insurance information from a third-party travel insurance servicing company based in Singapore. The company wants to sell their insurance product to customer candidate. The company wants to know about the characteristic of customer whom going to claim insurance (which need to be avoided) and the ones who are not. With customer profiling, the company can optimize their cost by avoiding the ones who predicted to claim and allocate the marketing cost to the targeted customer precisely. 

## Problem Statement
Without customer profiling, the company tend to increase their cost by allocate the marketing and operational cost to the targeted customer randomly. Not only the possibility of company pay the cost on the wrong place, but it also can be worsened by selling the product to the customer whom tend to claim the insurance. This situation makes the company doubles the revenue loss by pay the customer's claim.

## Goals
Based on the problem statement, the company want to predict if the customer candidates are the ones who tend to claim the insurance that they purchased.

It's also very helpful for the company for do the marketing planning, customer/marketing research and customer segmentation. With good ML model,the company can be more focused on the specific customer candidate whom may fit with company's products.

## Analytic Approach
What the writer do here is analyzing and finding pattern to profiling customer who tends to claim the insurance or not.
After that, the writer build a classification model that can help the company to predict the probability of insurance being claimed by customer.

## About Dataset
This data set contains information of travel insurance with its features as follows (The columns' name represented in bracket).

Claim Status (Claim Status) <br>
Name of agency (Agency) <br>
Type of travel insurance agencies (Agency Type) <br>
Distribution channel of travel insurance agencies (Distribution Channel) <br>
Name of the travel insurance products (Product Name) <br>
Duration of travel (Duration) <br>
Destination of travel (Destination) <br>
Amount of sales of travel insurance policies (Net Sales) <br>
Commission received for travel insurance agency (Commission) <br>
Gender of insured (Gender) <br>
Age of insured (Age) <br>

## Brief Overview
### Data Analysis
This dataset has a huge amount of missing values (>70%) in Gender column which then removed.

The numerical data values (Duration, Net Sales, Commision (in value) and Age) distribution are right skewed that shows tendency towards smaller values. The Net Sales data contains widest range data among other numerical data. 

From the categorical data, all of them correlated with claim and the claim proportion whether the correlations are directly proportional and are inversely proportional.

The claim data is classified as immoderate imbalance with claim proportion only about 1.7%. 

## Machine Learning Making
Firstly, 'Net Sales' data as the numerical data with largest range of data and standard deviation in this dataset is binned. The writer already did some trials before with binning other numerical columns and do some ranges of binning, for the binning is done into 6 categories since it increases the model performance around 10%.

The caterogical data is encoded with one hot and binary method. These features are made into numerical features to include them in the machine learning modeling.

The Machine Learning model is selected by iteration of 8 classification models, 2 resampler method (Undersampling with Nearmiss Method, Oversampling with SMOTE) to balance the moderate imbalance claim variable and by scaled or unscaled model.  The outcome shows that the best model isUnscaled XGB model with undersampling technique which then tuned to increase its performance.
