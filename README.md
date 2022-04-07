In this project, we train multiple models for predicting Formula 1 (F1) qualifying results based on historical data and data gathered during practice sessions. We compare their accuracy as well as their interpretability to the average F1 fan, based on how well broadcasters can incorporate the model’s explanation in their live feed. We also draw comparisons to the model developed by Amazon Web Services (AWS) that is currently used to create qualifying pace prediction graphics shown during F1 broadcasts.

The data for the training and testing of the models is gathered using the pyton library FastF1 (https://github.com/theOehrly/Fast-F1).

1. "F1_Quali_Prediction_Paper.pdf" is a short paper about this project, including a short literature review, an overview of the methods used and an evaluation of the results.
2. All used AWS predictions can be found in the folder "AWS_Predictions" algong with a file containing links to all the sites the predictions were taken from. Special thanks to the kind folks of reddit who helped me find the screenshots of the AWS Predictions.
3. The file "evaluation.csv" contains the key figures for all 48 trained models
4. The folder "cache_folder" is necessary to speed up the data collection with FastF1
5. The "Tyre_range.csv" file contains information about what range of tyres was used at what weekend for the 2017-2021 seasons. 
   The file was not used in the final program.
6. Running the "F1_Quali_Prediction.ipynb" takes around 5-6 hours. Note that you might have to install further packages in order to run the code. Even though the notebook contains some "!pip install ..." commands, these are by no means complete.
