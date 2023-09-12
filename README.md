# Determining the Cause of Departure Delays in Airports
 describe the data, recommendations.
Introduction: Why we chose our project<br />
For our project, we chose to look at the possible causes for departure delays in airports.<br />
No one likes to have their flight delayed and if we can find out a way to reduce those times, then everyone in the system could benefit.<br />
We found a large dataset from kaggle, link: https://www.kaggle.com/datasets/jl8771/2022-us-airlines-domestic-departure-data?select=Carriers.csv<br />
And we had to cut it down so it was usable (it originally had 7million rows and was rather unwieldly. We parsed it down to just the month of January and 436000 rows).<br />

Research Questions & Answers:<br />
1-	What are the biggest factors in determining flight delays?<br />
    From our research, there does not appear to a set condition in determining factors that cause flight delays. We found that the airport with the highest average flight delay was EYW, Key West        International airport, and that it was not the biggest airport, nor the busiest, and not even the airport with the worst weather. <br />
    
2-	Is there a subset of the data (Aircraft age, aircraft type, time in air, departure/arrival airport, etc.) that provides a true correlation to flight delays?<br />
    As for determining a subset of the data, we decided to group our data by the origins of each flight to have a more even and compact dataset. From there, we determined that -amongst the data         used- “Taxi Time per Flight”, which is the time it takes for the airplane to travel the tarmac in order to have a clear route for liftoff, was the most impactful factor in determining pre-          flight delays via a multilinear regression.<be />
    
3-	Does the number of delays early on in the year cause airlines to receive less business in the latter part of the year?<br />
    Our last research question was not answerable as the data set was too large initially to be manipulated and we decided that in order to be able to use the data that we would only use one            month’s worth of data as that still contained over 500000 rows of flights. If we move forward with this project, parsing through different months would be an interesting direction for us to         take.<br />

Set up<br />
Our libraries used were:<br />
import matplotlib.pyplot as plt<br />
import numpy as np<br />
import pandas as pd<br />
import sklearn as skl<br />
from sklearn.preprocessing import LabelBinarizer<br />
import scipy.stats as stats<br />
from sklearn import linear_model<br />
from scipy.stats import ttest_rel<br />
import seaborn as sns<br />

Our final dataset used was over 463000 rows and had 20 columns. We used a group me to break these numbers down by airport, as well as to add new measurables to try to discern answers to our research questions. That groupme dataframe ended up being 72 rows of airports and 11 columns of measurables. <br />

Conclusion<br />
In conclusion, we found that there was no discerning pattern in finding a catch all factor when talking about flight delays from data. We did however determine that the most impactful factor was Taxi Time per Flight and corroborated its impact being statistically relevant via t test. As we stated earlier, we were not able to parse throguh the entirety of the data, with our main limiting factor as having only one month of data instead of the whole year, but we would love to look over the rest of the year to see if there are any other details that may arise.



