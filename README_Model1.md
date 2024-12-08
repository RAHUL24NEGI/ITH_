Project: Genetic Syndrome Detection from GMDB Dataset
This project provides a preprocessing pipeline for loading and exploring the Genetic Medical Database (GMDB) datasets, enabling further analysis or model training for genetic syndrome detection.

Table of Contents
1.Introduction
2.Dataset
3.Requirements
4.Setup Instructions
5.Code Workflow
6.Steps to Run
7.Expected Outputs
8.Acknowledgments


Introduction

The Genetic Medical Database (GMDB) dataset contains structured data on images and metadata used to detect genetic syndromes. This project focuses on:
Loading the datasets for different splits (train, test, validation).
Exploring the structure and content of the datasets.

DatasetComponents
Training Data: gmdb_train_images_v1.1.0.csv
Testing Data: gmdb_test_images_v1.1.0.csv
Validation Data: gmdb_val_images_v1.1.0.csv
Syndrome Metadata: gmdb_syndromes_v1.1.0.tsv
Image Metadata: image_metadata_v1.1.0.tsv
Image Directory: Folder containing cropped images.
Sample Paths
Update the file paths in the script to point to the correct dataset location:
gmdb_train = "path_to_train_images.csv"
gmdb_test = "path_to_test_images.csv"
gmdb_val = "path_to_val_images.csv"
gmdb_syndromes = "path_to_syndromes.tsv"
image_metadata = "path_to_metadata.tsv"
data_dir = "path_to_images_directory"


Requirements
Prerequisites
Python: 3.8 or higher
Libraries: pandas
Installation
Install the required libraries using:
pip install pandas


Setup Instructions
Clone the repository or copy the notebook file into your working directory.
Download and place the GMDB datasets into the appropriate paths.

Code Workflow
Step 1: Define Paths
Specify the file paths for all datasets, including training, testing, validation splits, and metadata files.

Step 2: Load Data
Use pandas to load the CSV and TSV files:
import pandas as pd
df_train = pd.read_csv(gmdb_train)
df_test = pd.read_csv(gmdb_test)
df_val = pd.read_csv(gmdb_val)

Step 3: Explore Data
Preview the datasets to verify successful loading:
df_train.head()
df_test.head()
df_val.head()
Steps to Run

Prepare the Environment:
Install Python and necessary libraries.
Ensure dataset files are accessible in the specified paths.
Execute the Notebook:

Open the Jupyter Notebook in your environment.
Run each cell sequentially.
Expected Outputs
Display of the first few rows from the training, testing, and validation datasets:
Training Data Sample:
   image_id  subject  label
0         1        1      0
1         2        2      1


Acknowledgments
Dataset Source: Genetic Medical Database (GMDB).
Libraries Used: pandas for data manipulation.

later you can follow same code sequentailly to plot graphs of accuracy validation and confusion matrix
and you can also have class wise accuracy there
