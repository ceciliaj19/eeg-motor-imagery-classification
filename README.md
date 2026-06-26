## EEG Motor Imagery Classification
This project uses EEG data to classify motor imagery signals using the blassic brain-computer interface pipeline.

## Project Goal
The goal is to classify two motor imagery conditions from EEG recordings using signal preprocessing,epoch extraction, Common Spatial Patterns (CSP), and Linear Distriminant Analysis (LDA)

## Dataset
This project uses Subject 1 from the PhysioNet EEG Motor Movement/ Imagery Dataset

Runs used:
- S001R06
- S001R10
- S001R14

## Methods

1. Loaded EEG recordings from EDF files
2. Combined multiple motor imagery runs
3. Filtered EEG signals from 8-30 Hz
4. Extracted 4-second motor imagery epochs
5. Trained a CSP + LDA classifier
6. Evaluated performance using 5-fold stratified cross-validation

## Results
The CSP + LDA model achieved approximately 88.9% mean cross-validation accuracy

##Figures

![Raw EEG](figures/raw_eeg_subject1.png)

![Confusion Matrix](figures/confusion_matrix.png)

## Project Structure 

```text
notebooks/
  01_dataset_exploration.ipynb
  02_preprocessing.ipynb
  03_feature_extraction.ipynb
  04_classification.ipynb

figures/
  raw_eeg_subject1.png
  confusion_matrix.png