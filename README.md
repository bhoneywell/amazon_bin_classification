# Amazon Bin Classification - Inventory Monitoring at Distribution Centers

This is a capstone project that was done to complete the AWS Machine Learning Engineer nanodegree.

## Background

Distribution centers often use robots to move objects as a part of their operations. Objects are carried in bins which can contain multiple objects. In this project, you will have to build a model that can count the number of objects in each bin. A system like this can be used to track inventory and make sure that delivery consignments have the correct number of items.

To build this project I used AWS SageMaker and good machine learning engineering practices to fetch data from a database, preprocess it, and then train a machine learning model. This project will serve as a demonstration of the end-to-end machine learning engineering skills that I have learned as a part of this nanodegree.

For this Udacity Capstone project the Amazon Bin Image Dataset was used to classify the number of objects in Amazon warehouse bins. Amazon is an internet based enterprise that focuses on providing e-commerce, cloud and digital services. In order to fulfill the orders placed on their e-commerce site they often store the products a customer has purchased in warehouse facilities. In these facilities the goods are stored in bins. Currently Amazon’s warehouses are overseen by fulfillment workers. Initially, pickers were used to update a bin’s capacity, but since 2012 robots have been added to improve the workload. To meet the 2 day delivery standards Amazon has in place for some of their customers they need to ensure they have the most efficient layout possible. 

## Problem Statement

Currently, Amazon associates work in conjunction with Kiva robots to ensure the warehouse floor is in order. One issue with the bin storage layout is that employees currently have to estimate or manually keep track of the number of items in a bin if they want to be aware of its capacity. This can consume extra time when an associate needs to manually inspect and log goods in a bin. Given how Amazon tries to automate most of its processes this leaves room for an area of improvement. The time it takes employees to manually track the bin’s capacity can be used better elsewhere. This capstone project serves to provide a solution to this issue.

## Dataset

In order to work on this project data will be collected from the [Amazon Bin Images Dataset](https://registry.opendata.aws/amazon-bin-imagery/). The Bin Image dataset contains over 500,000 images of bins from an Amazon Fulfillment Center. Although the entire dataset will not be used, part of it will be sampled to test, train and validate the model. The dataset consists of images of bins with 1-5 objects per image.

## Solution Statement

This project will serve to remedy that problem by predicting the number of items in a bin. Given an image of the Amazon storage bin, this project will use a convolutional neural network to classify the number of objects in each bin. A pre-trained RESNET model will be used as the additional layers will likely be needed for this complex model.   This algorithm will be built using Amazon Sagemaker. The platform will allow me to scale to meet the demands of the model. 

## Evaluation Metrics
The primary metric that will be used to evaluate this model will be accuracy. Other metrics that may be considered include MAE and RMSE. The accuracy will be used to ensure the neural network is giving correct predictions on the number of objects in a bin. A higher accuracy will suggest that the model is working well.

## Project Design
The process to complete this project will include understanding the problem/business objective, then working to process and analyze the data. Once the data is processed and in a state fit to build a model on, the model building process will commence. Upon model build completion it will be tested on a portion of the dataset mentioned prior. Depending on the accuracy the model may be tuned to fit the best hyperparameters. Once the performance is satisfactory the model will be evaluated using the evaluation metrics above. 

## Documents
The documents conatined in this repository are below:

[Analysis](analysis.ipynb) - this file contains the actual code that was ran to generate the machine learning model

[Train](train.py) - this file contains the pytorch code used for the image classification model.

