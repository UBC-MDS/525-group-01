# DSCI 525 - A project in Web and Cloud Computing

## Group 01
- Robin Dhillon
- Ritisha Sharma
- Tanmay Agarwal
- Mehdi Naji

## Introduction
The purpose of this project is to explore working with Big Data. We explore build and deploy ensemble machine learning models in the cloud to predict daily rainfall in Australia on a large dataset (~6 GB). The features are outputs of different climate models, and the target is the actual rainfall observation. The work completed for this project is organized into four sections, or milestones. For each milestone, you can find a corresponding file in the [project's public repository.](https://github.com/UBC-MDS/525-group-01).

## Data
We use the `figshare` API to obtain data corresponding to daily rainfall for New South Wales, Australia. The dataset is approximately 6GB in size and contains information of rainfall recorded at several weather stations and spans from 1889 to 2014. The dataset can be found [here](https://figshare.com/articles/dataset/Daily_rainfall_over_NSW_Australia/14096681).


## Overview

In `milestone-1`, after some initial steps like downloadig the data from figshare and combined the CSV files into a single one. Lastly, we transferred the dataframe from Python to R and performed a simple EDA in R. In this step of the project, we found out that there are large differences in the time it took to combine the data and load it to perform EDA between all the team members. The fastest time to combine the data was 5min 19s with 16.00 GB RAM, Apple M1 Pro processor, and with an SSD. The slowest was 26 min with 32.00 GB RAM, Intel(R) Core(TM) i7-1065G7 CPU @ 1.30GHz 1.50 GHz, with an SSD. The slowest method of loading the combined CSV was to just naively load it using pandas. Changing the datatype led to a large improvement in performance. Some team members were able to load the data using the improved methods in under a minute. Overall, this milestone provided a good opportunity to gain exposure to handling large datasets and exploring different techniques to reduce memory usage while performing EDA. 

In `Milestone-2`, we migrated to the cloud with the help of our AWS's student accounts. We set up a server in the cloud, a collaborative environment, moved data to the cloud, and wrangled the data in preparation for machine learning. The step had parts, setting up a collaborative environment and wrangling the data in preparation for machine learning. We set up an EC2 instance, added team members, set up a common data folder, installed and configured AWS CLI, and installed TLJH in the instance. This milestone helped us all to get familiarize with AWS, migrate the data to the cloud, and prepare it for machine learning.

In `Milestone-3` we focused on setting up a Spark cluster and developing a machine learning model to deploy it in the cloud. We started with setting up an EMR Spark cluster, developing our machine learning model using scikit-learn, and using Spark's MLlib to obtain the best hyperparameter settings for the model using the cluster set up. 

In `Milestone-4` we deployed the machine learning model trained in `Milestone-3`. In this step of the project we deployedthe API by seeting up an EC2 instance, copying the code to app.py, downloading the model from S3 to the EC2 instance, and installing the dependencies of the API. Now, the service can be started and accessed by typing the EC2 instance's public IPv4 address into a browser.

### Key learnings in this project
- Handling large datasets and exploring different techniques to reduce memory usage.
- Migrating data to the cloud and setting up a collaborative environment in the cloud with AWS EC2 instances and S3 buckets.
- Using Spark and MLlib to develop machine learning models and optimize hyperparameters in a distributed environment.
- Developing an API and deploying machine learning models to an EC2 instance in the cloud.
- Configuring security groups and the AWS CLI.
