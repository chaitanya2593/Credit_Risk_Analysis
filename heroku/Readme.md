# Heart Disease Prediction
# Use Case Introduction

<p>The main objective of the repository is to demonstrate the Application of SVM and optimising the model using the Random and Grid hyperparameter tuning. <br>
Once the model has been build the same is deployed using the Heroku</p> 


- *Data Origin* : University of California, Irvine
- *URL*: https://archive.ics.uci.edu/ml/machine-learning-databases/heart-disease/

- *Brief Summary of the dataset*: The level of analysis is by person and it has demographic information (Age, Sex), pyshical status of the patient (Chest pain, Resting blood preasure, cholesterol, fasting blood pressure, resting ECG, max heart rate, exercise angina, old peak, slope of peak) and the diagnostic data (Hearth disease).

- *Objective of the Analysis*: Patient diagnostic prediction of hearth diseases using 11 varaibles from demographic and physical status of the patient.

- *Methodology*: We will be using 2 Kernels (Polynomial and RBF) as our classification model, each kernel will be optimized for F2 and F0.5 indicators using GridSearch as optimization techniques


### Detail Context
- Cardiovascular diseases (CVDs) are the number 1 cause of death globally, taking an estimated 17.9 million lives each year, which accounts for 31% of all deaths worldwide. Four out of 5CVD deaths are due to heart attacks and strokes, and one-third of these deaths occur prematurely in people under 70 years of age. Heart failure is a common event caused by CVDs and this dataset contains 11 features that can be used to predict a possible heart disease.

- People with cardiovascular disease or who are at high cardiovascular risk (due to the presence of one or more risk factors such as hypertension, diabetes, hyperlipidaemia or already established disease) need early detection and management wherein a machine learning model can be of great help.

### Attribute Information

- Age: age of the patient [years]
- Sex: sex of the patient [M: Male, F: Female]
- ChestPainType: chest pain type [TA: Typical Angina, ATA: Atypical Angina, NAP: Non-Anginal Pain, ASY: Asymptomatic]
- RestingBP: resting blood pressure [mm Hg]
- Cholesterol: serum cholesterol [mm/dl]
- FastingBS: fasting blood sugar [1: if FastingBS > 120 mg/dl, 0: otherwise]
- RestingECG: resting electrocardiogram results [Normal: Normal, ST: having ST-T wave abnormality (T wave inversions and/or ST elevation or depression of > 0.05 mV), LVH: showing probable or definite left ventricular hypertrophy by Estes' criteria]
- MaxHR: maximum heart rate achieved [Numeric value between 60 and 202]
- ExerciseAngina: exercise-induced angina [Y: Yes, N: No]
- Oldpeak: oldpeak = ST [Numeric value measured in depression]
- ST_Slope: the slope of the peak exercise ST segment [Up: upsloping, Flat: flat, Down: downsloping]
- HeartDisease: output class [1: heart disease, 0: Normal]

### Source
- This dataset was created by combining different datasets already available independently but not combined before. In this dataset, 5 heart datasets are combined over 11 common features which makes it the largest heart disease dataset available so far for research purposes. The five datasets used for its curation are:

    - Cleveland: 303 observations
    - Hungarian: 294 observations
    - Switzerland: 123 observations
    - Long Beach VA: 200 observations
    - Stalog (Heart) Data Set: 270 observations
    - Total: 1190 observations
    - Duplicated: 272 observations

- Final dataset: 918 observations

- Every dataset used can be found under the Index of heart disease datasets from UCI Machine Learning Repository on the following link: https://archive.ics.uci.edu/ml/machine-learning-databases/heart-disease/

## Deployment
- At first, during preprocessing the categorical variables label encoded and this encoding objects are stored by in label_dict.pkl and similar min_max_scaler.pkl file for the normalisation. 
- Then creating an account in heruko for free. Then created a dash python file named app.py(for convenience I used the generic name). As DASH uses flask, teh app was built for a flask deployment and it doesn't support static files.
- As third step I have designed code to capture all teh required fields for the model prediction.
- The model is tested locally just by invoking python file `python app.py`. 
- Now it is more of app deployment in heroku

### Heroku deployment
As a prerequsite, one should have the following files created 
1. requirements.txt - with all the python packages required for app.
2. Procfile - an no extension file with command `web: gunicorn app:server` (if you are using different name for the main dash file please replace the same in the command)

#### Initialize  heroku
In this step it is more about deploying the app in heroku app. 


> heroku create my-dash-app # change my-dash-app to a unique name<br>
> git add . # add all files to git<br>
> git commit -m 'Initial app boilerplate'<br>
> git push heroku master # deploy code to heroku<br>

Once this is successfully done you should get the url to access the website. In my case it is - `https://hdapp2593.herokuapp.com/`

## References:
- https://dash.plotly.com/deployment
- https://devcenter.heroku.com/articles/creating-apps



