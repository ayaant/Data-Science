import numpy as np
import pandas as pd

data_set = pd.read_csv("Data1.csv")
x = data_set.iloc[:,:3].values
print(x)
y = data_set.iloc[:,3].values
print(y)

# taking care of missing data
from sklearn.impute import SimpleImputer
imputer = SimpleImputer(missing_values=np.nan,strategy="mean")
imputer.fit(x[:,1:3])
x[:,1:3] = imputer.transform(x[:,1:3])
print(x)

from sklearn.compose import ColumnTransformer
from sklearn.preprocessing import OneHotEncoder #tranforms categorical data to something computer can understand numerical data
transformation = ColumnTransformer(transformers= [("Encoder",OneHotEncoder(),[0],remainder= "passthrough")])
