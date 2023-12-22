# Comparative Analysis of Machine Learning Algorithms for Time-Series Classification (Classifying time-series robot sensor data for surface identification)
## Introduction

This study investigates the domain of robotics, focusing on classifying time-series sensor data from Inertial Measurement Units (IMUs) to identify various floor surfaces. In this project, Logistic Regression, Random Forest Classifier, Gradient Boosting Classifier and Support Vector Machine are chosen to research the classification performance. There are two files in this dataset, namely 'X_train' and 'y_train'. The former contains input data, such as the linear speed of the robot walking in the X-axis direction. The latter contains the target label which is the type of the ground.

## The structure of our code base
(1)'data_preprocessing.py': This file is used to import dattaset and preprocess the dataset. Preprocessing contains adding new feature, selecting data volume, removing unwanted features, standardization, windowing data, applying FFT for representation, splitting data.

(2)'LogisticRegression.py': This file is about the code that runs the Logistic Regression model. 

(3)'RandomForestClassifier.py': This file is about the code that runs the Random Forest Classifier model. 

(4)'GradientBoostingClassifier.py': This file is about the code that runs the Gradient Boosting Classifier model. 

(5)'SVM.py': This file is about the code that runs the Support Vector Machine model. 

(6)'plot.py': This file is used to generate the images used in our report.

(7)'main.py': This file is a summary of all the above functions. It can help us print out the performance of different models by entering different parameters. It can also help us print out the images used in the report.

(8)'X_train.csv': The input data of the dataset.

(9)'y_train.csv': The target label of the dataset.

Among them, (2), (3), (4), (5) contain their own cross-validation, hyperparameter search, model fitting and model evaluation.

## Different functionalities of modules
(1) 'data_preprocessing.py'
+ def import_data：Import data.
+ def basic_standard_scaler: Standardize the data.
+ def preprocess_data: Preprocess data.

(2) 'LogisticRegression.py'
+ def experiment_logistic_regression: Run a logistic regression experiment.

(3)'RandomForestClassifier.py'
+ def experiment_random_forest: Run a Random Forest Classifier experiment.

(4)'GradientBoostingClassifier.py'
+ def experiment_gradient_boosting: Run a Gradient Boosting Classifier experiment.

(5)'SVM.py'
+ def experiment_svm: Run a SVM experiment.

(6)'plot.py'
+ def main: Plot two images. 

(7)'main.py'
+ def main: Process command line parameters, set hyperparameters and cross validation folds for experiments and run specific machine learning model experiments based on user selection.

## Software implementation
There are two ways to run 'main.py':

(1) Use cmd or terminal in Pycharm to run the code. We can run the code by typing 'python main.py --data_file1 X_train.csv --data_file2 y_train.csv --experiment <>' in the dialog. <> should be replaced by 'logistic_regression', 'random_forest', 'gradient_boosting', 'svm' or 'all'. When <> is replaced by one of the first four parameters, the corresponding model will be run. When <> is replaced by 'all', all models will be run and images will appear.

(2) Use Pycharm to run the code directly. We can click the 'Edit Parameters' button in the upper right corner of pycharm. Then we can enter the statement mentioned in (1) in the 'parameters' line of the 'main' file. The next step is to click 'apply' button. Finally, we need to run the 'main.py' and the corresponding results will come out.

## Expected behaviours
If the <> is replaced by 'all', two images about dataset will be shown and saved to the directory path. Besides, the four models will show their best combination of hyperparameters and average f1 score on the validation set. Besides, their f1 score on the test set on the test set under the optimal combination of hyperparameters will be shown. What's more, the hyperparameter search and cross-validation processes of a part of model will be shown.

For Logistic Regression, the running time will be about 1 minnutes 41 seconds. For Random Forest Classifier, the running time will be about 4 minnutes 19 seconds. For Gradient Boosting Classifier, the running time will be about 15 minnutes 47 seconds. For Support Vector Machine, the running time will be about 2.22 seconds.
