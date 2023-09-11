# Determining the Cause of Departure Delays in Airports

Introduction: Why we chose our project
For our project, we chose to look at the possible causes for departure delays in airports. 
We found a large dataset from kaggle, link: https://www.kaggle.com/datasets/jl8771/2022-us-airlines-domestic-departure-data?select=Carriers.csv
And we had to cut it down so it was usable (it originally had 7million rows and was rather unwieldly. We parsed it down to just the month of January and 436000 rows).

Set up
Our libraries used were:
import matplotlib.pyplot as plt

import numpy as np

import pandas as pd

import sklearn as skl

from sklearn.preprocessing import LabelBinarizer

import scipy.stats as stats

from sklearn import linear_model

from scipy.stats import ttest_rel

import seaborn as sns



