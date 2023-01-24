# ML FLOW PROJECT : Author ( ZAGHLOUL & HIRCHI & EKANE )

## Including SPHINX documentaion, MLFLOW lifecyle, SHAP model explainer

### STEP 1 : DOWNLOAD THE DATA

Since the csv files are too big to be on GitHub, please download with the link below and do not forget to put csv files in the right folder : "1_rawdata"

[https://www.kaggle.com/c/home-credit-default-risk/data?select=application_train.csv](https://www.kaggle.com/c/home-credit-default-risk/data?select=application_train.csv)

### STEP 2 : OPEN A CMD AND CD TO THE PROJECT LOCATION

cd path\to\the\project\location

### STEP 3 : INSTALL DEPENDENCIES

### Run these commands

pip3 install -r requirements.txt

Then below, you can choose your model (xgBoost.pkl, randomForest.pkl, GradientBoosting.pkl)

python 5_main.py --model "model name"

### STEP 4 : TRACK PARAMETERS AND MODELS IN MLFLOW UI

### Run this command

mlflow ui

![Untitled](ML%20FLOW%20PROJECT%20Author%20(%20ZAGHLOUL%20&%20HIRCHI%20&%20EKANE%20904432ab94c748df8f96df4178be2bab/Untitled.png)

### STEP 5 : OPEN A NEW CMD AND RUN MLFLOW TO DEPLOY A REST SERVER IN ORDER TO MAKE PREDICTION

### Run these commands

mlflow models serve –-model-uri path\to\the\runexperimentation\artifacts\model --no-conda -p 1234

Or this one below

mlflow models serve –m path\to\the\runexperimentation\artifacts\model --no-conda -p 1234

## STEP 6 : OPEN A NEW CMD TO POST REQUEST

### Run this command

python 6_request.py

## STEP 7 : Integrate SHAP Library

### Compute the average impact of each features :

![Untitled](ML%20FLOW%20PROJECT%20Author%20(%20ZAGHLOUL%20&%20HIRCHI%20&%20EKANE%20904432ab94c748df8f96df4178be2bab/Untitled%201.png)

### Visualize positive and negative relationships of the features with the target :

![Untitled](ML%20FLOW%20PROJECT%20Author%20(%20ZAGHLOUL%20&%20HIRCHI%20&%20EKANE%20904432ab94c748df8f96df4178be2bab/Untitled%202.png)