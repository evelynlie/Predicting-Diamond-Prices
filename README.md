<h1>Predicting Diamond Prices Using Statistical Modelling</h1>
<h2>Table of Contents</h2>

- [Introduction](#introduction)
- [Dataset Features](#dataset-features)
- [How to View the Report in Jupyter Notebook](#how-to-view-the-report-in-jupyter-notebook)
- [Contributors](#contributors)

## Introduction
In this report, we want to predict the diamond's price in US dollars based on the available features provided in the diamond's dataset. The dataset itself is taken from a website called Kaggle (``https://www.kaggle.com/datasets/shivam2503/diamonds``). Subsequently, we conducted data cleaning process by removing outliers which has a higher and lower carat than 1.5 times of the interquartile range, and identified if there any missing values occurs within the dataset. Eventually, we visualised and explored the dataset using 15 figures that plot and illustrate the relationship between different variables using Seaborn and Matplotlib, with explanations provided for each plot to analyse the patterns, correlations, and trends occurred. 
    
In order to forecast the price of diamonds using all of the features in the dataset, we first fit a multiple linear regression in the Full Model Overview. Next, we use the Statsmodels module to create the regression formula as a Python string that contains all of the independent variables from our dataset. The categorical features in our dataset are then one-hot encoded using Pandas' get_dummies function, and the regression model formula is updated to include the encoded features. After defining the regression model formula, we create an ordinary least squares (OLS) model to the encoded features. In order to better comprehend the difference between the real and predicted prices of diamonds, we then establish a new data frame to hold the actual price of diamonds, the predicted price of diamonds, as well as its residuals.

Next, we check whether the multiple linear regression model is valid or not by running diagnostic checks with 4 assumptions to satisfy, which are linearity, nearly normal residuals, constant variability, and independence of residuals. In backwards feature selection, we eliminate features that are not statistically significant by looking that features whose p-value is above 0.05 since statistical significance is indicated by a p-value of less than 0.05. We create a new OLS model and data frame that stores the actual price of diamonds, the predicted price of diamonds, and its residuals as well as to validate whether the model satisfies the previous 4 assumptions in our Reduced Model Overview and Reduced Model Diagnostic Checks. This is similar to what we did in the Full Model Overview and Full Model Diagnostic Checks, but with the insignificant features eliminated.

## Dataset Features
* Carat = Weight of diamond
* Cut = Quality of the cut
* Colour = Colour of diamond
* Clarity = Measurement of how clear the diamond is
* Depth = Total depth percentage of diamond
* Table = Width of top of diamond relative to widest point
* x = Length of diamond in milimetres
* y = Width of diamond in milimetres
* z = Depth of diamond in milimetres
* Price = Price of diamond in US Dollars

## How to View the Report in Jupyter Notebook
1. If you have never downloaded Python before, download Python from ``https://www.python.org/`` based on your device's operating system and install it to your device.
2. Download Anaconda from ``https://www.anaconda.com/products/distribution`` and install Anaconda to your device.
3a. For Windows users, go to the command prompt and type ``python -m pip install --upgrade pip``. If your device is already up-to-date, continue to type in ``python -m pip install jupyter`` to install juptyer notebook.
3b. For Mac users, go to the terminal and type in ``conda install -c conda-forge jupyterlab``. If there's a question asking to proceed, reply it with 'y'.
4. Once jupyter notebook has been installed, download the ZIP file of the repository and unpack it.
5. To open the report in jupyter notebook, simply type ``jupyter notebook`` in your command prompt (Windows)/terminal (Mac) and navigate to the folder where you keep the files that previously has been unpack from the ZIP file.

## Contributors
* Evelyn Lie, Bachelor of Software Engineering, RMIT University.
* Edward Lim Padmajaya, Bachelor of Computer Science, RMIT University.
* Go Chee Kin, Bachelor of Computer Science, RMIT University.
* Frandom Leo Inovejas, Bachelor of Computer Science, RMIT University.
