#This is my first Programming 
#for that i use the python 
#Importing the libries
import numpy as np
import pandas as pd
import seaborn as sns
import statsmodels.api as sn

#imprting my csv file
df=pd.read_csv("House_Price.csv",header=0)

#Disply data
df

#outliers
np.percentile(df.n_hot_rooms,[99])
np.percentile(df.n_hot_rooms,[99])[0]
uv=np.percentile(df.n_hot_rooms,[99])[0]
df[df.n_hot_rooms>uv]
df.n_hot_rooms[(df.n_hot_rooms>3*uv)]
df.n_hot_rooms[(df.n_hot_rooms>3*uv)]=3*uv
