# CS 323 - Project 1: Anonymity

Author: James Bui, Bach Nguyen

This contains the code and analysis for **Project 1: Anonymity** for the course CS 323: Data Privacy

## Project Overview

This project implements a k-anonymization pipeline on the UCI Adult dataset.
We developed functions to perform attribute generalization, enforce **$k$-anonymity**, and compute utility metrics to evaluate the trade-off between privacy and data usability.

## Project Structure 
The project consists of 7 files:
- __cs323_project_1.ipnyb__: The main Jupyter Notebook that contains all of the code needed to run this project.
- __generalized_k2.csv__: Output csv file at k = 2
- __generalized_k4.csv__: Output csv file at k = 4
- __generalized_k6.csv__: Output csv file at k = 6
- __generalized_k15.csv__: Output csv file at k = 15

In the __data__ folder:
- __adult.data__: Main datafile
- __adult.names__: File containing metadata about the dataset

## How to run the Code

1. Dataset Setup
The dataset files (adult.data and adult.names) must be placed in the __data__ folder. Note: The main .data file does not contain column names. The .names file is parsed inside the Jupyter notebook to extract and assign column names automatically.

2. Run all of the Notebook Cells
   
3. Inspect the Output
Results are printed directly in the notebook. CSV files containing generalized data are saved in the working directory.

## Major Design Decisions

- Dynamic Generalization: Age bins are dynamically computed based on dataset min/max, making the approach dataset-agnostic.

- Flexible Generalization Levels: Each quasi-identifier supports multiple generalization levels, allowing experiments with different privacy-utility tradeoffs.

- Utility Evaluation: We selected three standard metrics from anonymization research to quantify information loss and usability.


