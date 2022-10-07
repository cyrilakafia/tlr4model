# Machine Learning Model For Predicting Anti-Inflammatory Compounds
Building machine learning models for predicting inhibitors of the toll-like receptor 4 (TLR4)

## Dataset
Datasets were obtained from pubchem assays AID 861 and AID 1237. 
AID 1237 is a confirmatory assay that further divides the actives from AID 861 into actives and inactives.

All four csv files i.e. Active (358) and Inactive (195,623) for AID 861 and Active (220 Compounds) and Inactives (129 Compounds) for AID 1237 have been cleaned and their canonical smiles have been extracted.

All concentration was place on AID 861 

Simplified datasets in .csv formated have been generated for each file described above.
The consist of 
  i.  smiles csv
  ii. final csv

For AID 861 Inactives, the csv files can be located in the google drive. Due to their large size, they can't be uploaded to github 

## Molecular Descriptors
Using Mold2, Molecular Descriptors (777) have been computed for both the active and inactive datasets and the resulting csv files were combined to form a final.csv for model training, testing and applicability domain analysis.

## Resampling and Training
An iterative process then was employed by using different ratios of active and inactive to build models by leveraging resampling techniques.
The resampling techniques employed were:
  i. Synthetic Minority Oversampling Technique
  ii. Random Undersampling
  iii. Random Selection
  
The five iterations are explained below
Iteration 1: No resampling techniques were used. Model was trained on highly imbalance data.<br>
Iteration 2: 1:1 ratio was used by undersampling inactives to match actives <br>
Iteration 3: 1:3 ratio was used by undersampling inactives to about 3 times the number of active samples <br>
Iteration 4: 1:1 ratio was used by undersampling inactives to half of it original number of samples and then oversampling the actives to match this number <br>
Iteration 5: Randomly selecting 5,000 inactives from the inactive dataset and combining them with all samples on the active dataset. <br>

## Model Performance Evaluation
The models were evaluated using accuracy, precision, f1, recall, mcc and auroc

## Predictions
The top 5 models were selected and used to screen a library of peptidomimetics obtained from ChemDiv.
A total of 45 compounds were classified as active
The confidence values/probabilities of these compounds are also extracted for further decision making

## Applicabilty Domain
Applicability domain analysis was done on the train and test dataset from the main final.csv dataset
Applicability Domain Analysis will be computed for these compounds
