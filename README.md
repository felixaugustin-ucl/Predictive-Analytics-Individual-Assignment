# ECG Arrhythmia Classification -- Predictive Analytics

## Overview

This repository contains the full workflow for a multi-label ECG
arrhythmia classification project.

The project includes: - Exploratory Data Analysis (EDA) - Handcrafted
ECG feature engineering - Classical machine learning models (SGD,
XGBoost) - Threshold optimisation with emphasis on recall - Experimental
1D CNN (ResNet-style) - Model card and project log for transparency

All reported results and figures are embedded in the main notebook.

------------------------------------------------------------------------

## Repository Structure

ECG-Analysis SCLY4.ipynb → Main analysis notebook\
PROJECT_LOG.md → Development log\
modelcard.png → Model summary of final solution\
ecg_feature_list.txt → Engineered feature list\
README.md → This file

------------------------------------------------------------------------

## Dataset

This project uses the **ECG Arrhythmia Dataset** from PhysioNet:

https://physionet.org/content/ecg-arrhythmia/1.0.0/

The dataset (\~5.5 GB uncompressed) is NOT included in this repository
due to size and licensing considerations.

------------------------------------------------------------------------

## How to Download the Dataset

You may download the dataset using one of the following methods:

### Option 1 -- Download ZIP file (2.3 GB)

Download directly from PhysioNet and extract locally.

### Option 2 -- Using terminal (recommended)

wget -r -N -c -np https://physionet.org/files/ecg-arrhythmia/1.0.0/

### Option 3 -- Using AWS CLI

aws s3 sync --no-sign-request s3://physionet-open/ecg-arrhythmia/1.0.0/
DESTINATION

------------------------------------------------------------------------

## Important Setup Step

After downloading and extracting the dataset:

1. Rename the extracted PhysioNet folder to:

   ecg_data

2. Move the folder into the same directory as the notebook:

project_folder/
│
├── ECG-Analysis SCLY4.ipynb
├── ecg_data/      
├── Remaining_DX_Codes_SNOMED_Labels.csv
├── README.md

3. Move the file `Remaining_DX_Codes_SNOMED_Labels.csv` (included in this repository) 
   into the `ecg_data` folder.

Final required structure:

project_folder/
├── ECG-Analysis SCLY4.ipynb
├── README.md
├── PROJECT_LOG.md
├── ecg_feature_list.txt
├── modelcard.png
└── ecg_data/
├── WFDBRecords/
├── ... (other PhysioNet files)
└── Remaining_DX_Codes_SNOMED_Labels.csv

------------------------------------------------------------------------

## Running the Notebook

It is recommended to run the notebook locally due to dataset size and
compute requirements.

1.  Install required Python packages.
2.  Ensure the dataset is placed in ./ecg_data/
3.  Run the notebook from top to bottom.

Note: Full CNN training is computationally heavy and may be limited
depending on hardware constraints.

------------------------------------------------------------------------

## Data Integrity

The raw PhysioNet data has not been modified. No patient-identifiable
information is included in this repository. This repository contains
code only.

------------------------------------------------------------------------

## Author

Felix Augustin\
MSc Business Analytics -- UCL School of Management
