# Comparative Analysis of Machine Learning Algorithms for Time-Series Classification (Classifying time-series robot sensor data for surface identification)
## Introduction

This study investigates the domain of robotics, focusing on classifying time-series sensor data from Inertial Measurement Units (IMUs) to identify various floor surfaces. In this project, Logistic Regression, Random Forest Classifier, Gradient Boosting Classifier and Support Vector Machine are chosen to research the classification performance. There are two files in this dataset, namely 'X_train' and 'y_train'. The former contains input data, such as the linear speed of the robot walking in the X-axis direction. The latter contains the target label which is the type of the ground.

## The structure of our code base
(1)'data_preprocessing.py': This file is used to import dattaset and preprocess the dataset. Preprocessing contains adding new feature, selecting data volume, removing unwanted features, standardization, windowing data, applying FFT for representation, splitting data.
(2)'LogisticRegression.py': This file is about the code that runs the Logistic Regression model. 
(3)'RandomForestClassifier.py': This file is about the code that runs the Random Forest Classifier model. 
(4)'GradientBoostingClassifier.py': This file is about the code that runs the Gradient Boosting Classifier model. 
(5)'SVM.py': This file is about the code that runs the Support Vector Machine model. 
(6)'plot.py': 
(7)'main.py': This file is a summary of all the above functions. It can help us print out the performance of different models by entering different parameters. It can also help us print out the images used in the report.

  
(8)'X_train.csv': The input data of the dataset.
(9)'y_train.csv': The target label of the dataset.


## Software implementation




## Dependencies

You'll need a working Python environment to run the code.
The recommended way to set up your environment is through the
[Anaconda Python distribution](https://www.anaconda.com/download/) which
provides the `conda` package manager.
Anaconda can be installed in your user directory and does not interfere with
the system Python installation.
The required dependencies are specified in the file `environment.yml`.

We use `conda` virtual environments to manage the project dependencies in
isolation.
Thus, you can install our dependencies without causing conflicts with your
setup (even with different Python versions).

Run the following command in the repository folder (where `environment.yml`
is located) to create a separate environment and install all required
dependencies in it:

    conda env create


## Reproducing the results

Before running any code you must activate the conda environment:

    source activate ENVIRONMENT_NAME

or, if you're on Windows:

    activate ENVIRONMENT_NAME

This will enable the environment for your current terminal session.
Any subsequent commands will use software that is installed in the environment.

To build and test the software, produce all results and figures, and compile
the manuscript PDF, run this in the top level of the repository:

    make all

If all goes well, the manuscript PDF will be placed in `manuscript/output`.

You can also run individual steps in the process using the `Makefile`s from the
`code` and `manuscript` folders. See the respective `README.md` files for
instructions.

Another way of exploring the code results is to execute the Jupyter notebooks
individually.
To do this, you must first start the notebook server by going into the
repository top level and running:

    jupyter notebook

This will start the server and open your default web browser to the Jupyter
interface. In the page, go into the `code/notebooks` folder and select the
notebook that you wish to view/run.

The notebook is divided into cells (some have text while other have code).
Each cell can be executed using `Shift + Enter`.
Executing text cells does nothing and executing code cells runs the code
and produces it's output.
To execute the whole notebook, run all cells in order.
