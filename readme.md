# Artificial Pancreas Medical Control System

This is a three-part project focused on developing a better understanding of data mining techniques and their application to the Artificial Pancreas Medical Control System, specifically the Medtronic 670G system. The project involves extracting performance metrics, training a machine model to distinguish meal and no-meal time series data, and performing cluster validation to determine the amount of carbohydrates in each meal.

## Table of Contents

- [Introduction](#introduction)
- [Project 1: Extracting Time Series Properties of Glucose Levels in Artificial Pancreas](#project-1)
- [Project 2: Machine Model Training](#project-2)
- [Project 3: Cluster Validation](#project-3)
- [Installation and Usage](#installation-and-usage)
- [License](#license)

## Introduction

This project aims to improve the understanding of data mining concepts such as data pre-processing, feature extraction, clustering, cluster validation, and predictive modeling. The Medtronic system consists of a continuous glucose monitor (CGM) and the Guardian Sensor, which measures blood glucose every five minutes. The CGM sends the data to the MiniMed insulin pump, which adjusts insulin delivery based on CGM readings.

The project is divided into three parts:

1. Extracting Time Series Properties of Glucose Levels in Artificial Pancreas
2. Machine Model Training
3. Cluster Validation

## Project 1: Extracting Time Series Properties of Glucose Levels in Artificial Pancreas

In this part of the project, performance metrics of an Artificial Pancreas system are extracted from sensor data. The extracted metrics include:

- Percentage time in hyperglycemia (CGM > 180 mg/dL)
- Percentage of time in hyperglycemia critical (CGM > 250 mg/dL)
- Percentage time in range (CGM >= 70 mg/dL and CGM <= 180 mg/dL)
- Percentage time in range secondary (CGM >= 70 mg/dL and CGM <= 150 mg/dL)
- Percentage time in hypoglycemia level 1 (CGM < 70 mg/dL)
- Percentage time in hypoglycemia level 2 (CGM < 54 mg/dL)

These metrics are extracted for two modes: Manual mode and Auto mode.

## Project 2: Machine Model Training

In this part of the project, a machine model is trained to distinguish between meal and no-meal time series data. The training data set contains ground truth labels of Meal and No Meal for five subjects. The process involves extracting features from Meal and No Meal training data sets, ensuring that the features are discriminatory, and training a machine to recognize Meal or No Meal data.

## Project 3: Cluster Validation

In this part of the project, cluster validation is performed on the data set. The process involves extracting ground truth values for each data point in the data set and applying clustering techniques to separate the meal data into groups based on the amount of carbohydrates each meal contains. The clustering algorithms used include KMeans and Density Based Spatial Clustering of Applications with Noise (DBSCAN).

## Installation and Usage

To set up the project and run the code, follow these steps:

1. Clone this repository: `git clone https://github.com/yourusername/Artificial-Pancreas-Medical-Control-System.git`
2. Navigate to the project folder: `cd Artificial-Pancreas-Medical-Control-System`
3. Install required packages: `pip install -r requirements.txt`
4. Run the desired Python script from the command line, passing the required CSV files as arguments, for example: `python project_1.py CGMData.csv Insulin