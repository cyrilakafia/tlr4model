# tlr4model
Building machine learning models for predicting inhibitors of the toll-like receptor 4 (TLR4)

## dataset
Datasets were obtained from pubchem assays AID 861 and AID 1237. 
AID 1237 is a confirmatory assay that further divides the actives from AID 861 into actives and inactives.

We are yet to decide which one we would use

All four csv files i.e. Active (358) and Inactive (195,623) for AID 861 and Active (220 Compounds) and Inactives (129 Compounds) for AID 1237 have been cleaned and their canonical smiles have been extracted.

Simplified datasets in .csv formated have been generated for each file described above.
The consist of 
  i.  smiles csv
  ii. final csv

For AID 861 Inactives, the csv files can be located in the google drive. Due to their large size, they can't be uploaded to github 

## to-do

  i.    Undersampling
  ii.   SMOTE
  iii.  Molecular descriptors
