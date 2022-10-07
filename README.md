Titanic Survival Prediction using Tensorflow in Python

we will be creating a Machine Learning Model to predict the survival chances of the Titanic passengers using the given information in the csv file
Libraries used: 

sklearn

from __future__ import absolute_import, division, print_function, unicode_literals


import numpy as np

import pandas as pd

import matplotlib.pyplot as plt

from IPython.display import clear_output

from six.moves import urllib

import tensorflow.compat.v2.feature_column as fc

import tensorflow as tf

we loaded two different datasets. This is because when we train models, we need two sets of data: training and testing.

In our dataset we have two different kinds of information: Categorical and Numeric
Our categorical data is anything that is not numeric! For example, the sex column does not use numbers, it uses the words "male" and "female".
Before we continue and create/train a model we must convet our categorical data into numeric data. We can do this by encoding each category with an integer (ex. male = 1, female = 2).
Fortunately for us TensorFlow has some tools to help!

And we now we have a model with a 74% accuracy (this will change each time)! Not crazy impressive but decent for our first try.


the following code is to predict the survival chances of the individual..

result = list(linear_est.predict(eval_input_fn))
print(dfeval.loc[3])
print(y_eval.loc[3])
print(result[3]['probabilities'][1])
