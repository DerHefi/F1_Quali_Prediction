# Introduction #
In this project, we train multiple models for predicting Formula 1 (F1) qualifying results based on historical data and data gathered during practice sessions. We compare their accuracy as well as their interpretability to the average F1 fan, based on how well broadcasters can incorporate the model’s explanation in their live feed. We also draw comparisons to the model developed by Amazon Web Services (AWS) that is currently used to create qualifying pace prediction graphics shown during F1 broadcasts.

The data for the training and testing of the models is gathered using the pyton library FastF1 (https://github.com/theOehrly/Fast-F1).
We train 4 different kinds of models using data from the 2018-2020 seasons and test them using data from the 2021 season.
The 4 kinds of models are Linear Regression, Quadratic Linear Regression, Cubic Linear Regression and Multilayer Perceptron
Regression.
For each kind of model, we train 12 models based on different features, like the fastest time posted by the driver during a certain practice session, the track, the team, etc.

# TLDR Results #
The AWS predictions are pretty inaccurate considering their ressources. Some of the models trained in this project match their accuracy, while being a lot more explainable to the average F1 fan.

# Repo Description #
1. "F1_Quali_Prediction_Paper.pdf" is a short paper about this project, including a brief literature review, an overview of the methods used and an evaluation of the results.
2. All used AWS predictions can be found in the folder "AWS_Predictions" algong with a file containing links to all the sites the predictions were taken from. Special thanks to /u/peeinmyblackeyes and the kind folks of reddit who helped me track down some of the AWS Predictions I couldn't find myself.
3. The file "evaluation.csv" contains the key figures for all 48 trained models
4. The folder "cache_folder" is necessary to speed up the data collection with FastF1
5. The "Tyre_range.csv" file contains information about what range of tyres was used at what weekend for the 2017-2021 seasons. 
   The file was not used in the final program.
6. Running the "F1_Quali_Prediction.ipynb" takes around 5-6 hours. Most of the time is used to load the data (ca. 30 min) and to train the Multilayer Perceptron Regressors (ca. 4-5 hours). Note that you might have to install further packages in order to run the code. Even though the notebook contains some "!pip install ..." commands, these are by no means complete.
