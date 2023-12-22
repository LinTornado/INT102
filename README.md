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

## Different functionalities
(1) 

(2) 


## Software implementation
There are two ways to run 'main.py':

(1) Use cmd or terminal in Pycharm to run the code. We can run the code by typing 'python main.py --data_file1 X_train.csv --data_file2 y_train.csv --experiment <>' in the dialog. <> should be replaced by 'logistic_regression', 'random_forest', 'gradient_boosting', 'svm' or 'all'. When <> is replaced by one of the first four parameters, the corresponding model will be run. When <> is replaced by 'all', all models will be run and images will appear.

(2) Use Pycharm to run the code directly. We can click the 'Edit Parameters' button in the upper right corner of pycharm. Then we can enter the statement mentioned in (1) in the 'parameters' line of the 'main' file. The next step is to click 'apply' button. Finally, we need to run the 'main.py' and the corresponding results will come out.

## Reproducing the results


