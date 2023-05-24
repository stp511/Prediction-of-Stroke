# Predicting Stroke
## Steven Phillips
### Problem:
The problem explored in this project is to discover which of several features increase the likelihood of stroke.
### Data:
The data used for this project originates from:
(https://www.kaggle.com/datasets/fedesoriano/stroke-prediction-dataset)

The data items include several features including: body mass index, age, marital status, average glucose level, smoking status, work type, gender, and the presence or heart disease or hypertension.
## Methods
The data were prepared by eliminating duplicates and focusing on age, smoking status, presence of heart disease and hypertension.
## Results 
### This first image showcases correlations between numeric variables.

<p align="center">
  <img src="https://user-images.githubusercontent.com/113748627/204377253-5f546f19-2713-4d47-a298-b413e51702f9.png">
</p>


### And the highest correlation amongst variable pairs is 0.33 between BMI and Age.

These next two images showcase distributions of stroke across the presence of hypertension and heart disease:

<p align="center">
  <img src="https://user-images.githubusercontent.com/113748627/205337774-0c17c919-ffde-4dfc-9b73-31073928237a.png">
</p>
 
## Here we see that a higher incidence of stroke exists for those with hypertension.

<p align="center">
 <img src="https://user-images.githubusercontent.com/113748627/205337854-12d3a142-52d3-4ec2-bbff-6f5a4502df0e.png">
</p>

## And here we see that a higher incidence of stroke exists for those with heart disease.

## Model
The model chosen is LightGBM with these hyperparameters:

Class Weight: 'balanced'
max_depth: 1
n_estimators: 2
num_leaves: 50
pca_n_components: 0.5

The metrics for evaluation of our optimized LightGBM Model on our test data are: 

Recall: 0.85
Accuracy: 0.68
Precision: 0.11
F1-score: 0.19

## Recommendations

The recall score of our model is 0.85.  This explains that our model is predicting 85% of the individuals who have stroke correctly.  This high recall score is reducing the incidence of unidentifying those individuals with stroke.  A lower recall score would lead to more incidence of informing individuals at risk of stroke that they are not and missing the opportunity to provide them with measures to prevent stroke such as medicine, exercise, or other treatments.
## Limitations & Next Steps
This recall score of 0.85 was not the highest recall score of all models explored, but it's accuracy measure was higher than other comparable models.  This secondary measure of the accuracy of the model measured predicting correctly those with and without stroke.  

## For more information:
For any additional questions, please contact me above.
