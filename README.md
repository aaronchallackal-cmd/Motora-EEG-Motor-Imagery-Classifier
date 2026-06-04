# NeuroPilot: EEG Motor Imagery Classification

NeuroPilot is a beginner neurotechnology project that uses public EEG recordings to classify imagined left hand movement versus imagined right hand movement.

The project uses MNE Python for EEG preprocessing, Common Spatial Patterns for feature extraction, and machine learning models to classify motor imagery brain states.

## Project Overview

This project explores whether EEG brain signals can be used to distinguish between two imagined movement conditions:

1. Imagined left hand movement
2. Imagined right hand movement

The dataset was processed using a full EEG machine learning workflow, including signal filtering, epoch extraction, feature extraction, model training, model comparison, and visualization.

## Tools Used

- Python
- Google Colab
- MNE Python
- NumPy
- Pandas
- Matplotlib
- Scikit-learn

## Methods

The project used public EEG data from the EEGBCI motor imagery dataset.

The analysis focused on runs 4, 8, and 12, which contain imagined left hand and imagined right hand movement tasks.

The EEG signals were filtered between 7 and 30 Hz, then segmented into epochs from 1 to 4 seconds after each task cue.

Common Spatial Patterns was used to extract spatial EEG features, and machine learning classifiers were trained to predict the imagined movement condition.

## Models Tested

- Logistic Regression
- Support Vector Machine
- Subject specific models
- Multi subject model
- Cross validation
- Leave one subject out testing

## Key Results

- Single subject model: 66.67 percent accuracy
- Five subject combined model: 52.63 percent accuracy
- Best cross validated subject: Subject 2 at 86.67 percent mean accuracy
- Best single split result: Subject 2 classified 11 out of 12 test trials correctly
- Leave one subject out testing ranged from 37.78 percent to 53.33 percent accuracy

## Main Finding

The project showed that EEG motor imagery classification worked best when models were trained and tested on the same participant.

When the model was tested on completely unseen participants, performance dropped substantially.

This suggests that EEG based brain computer interface systems may require individual calibration before performing well.

## Visualizations

The notebook includes:

- Raw EEG signal plot
- Subject specific accuracy comparison
- Cross validated accuracy graph with error bars
- Classifier comparison graph
- Leave one subject out graph
- Confusion matrix for the best subject
- EEG electrode map
- CSP spatial pattern visualization

## Conclusion

NeuroPilot demonstrates a complete beginner neurotechnology workflow using public brain signal data.

The project shows how EEG signals can be loaded, filtered, segmented, visualized, transformed into features, and classified using machine learning.

It also highlights an important challenge in neurotechnology: EEG models often perform better within individual participants than across new unseen participants.
