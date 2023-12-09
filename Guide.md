**We are going to give you basic idea about what to do. You have to put effort to understanding that particular**
**topic**

# Data Preprocessing

In Real life dataset there is null values in it. We have handle null(or Nan) values so that it can be used to train the   
the Machine Learning Model  
There are two categories to handle it:  
 - Numerical: Features(Columns) containing the numbers
 - Categorical: Features(Columns) containing the category values  
In these Problem Statement we are going to use numerical features:
 - You could drop the rows having the null values using **<dataframe>.dropna(subse=[columns])**
 - Use the **Simple Imputer** 


```python
import pandas as pd

df = pd.read_csv("Solar_Prediction.csv")
df.info()
```

    <class 'pandas.core.frame.DataFrame'>
    RangeIndex: 32398 entries, 0 to 32397
    Data columns (total 12 columns):
     #   Column                  Non-Null Count  Dtype  
    ---  ------                  --------------  -----  
     0   Unnamed: 0              32398 non-null  int64  
     1   UNIXTime                32398 non-null  int64  
     2   Date                    32398 non-null  object 
     3   Time                    32398 non-null  object 
     4   Radiation               32398 non-null  float64
     5   Temperature             32198 non-null  float64
     6   Pressure                32249 non-null  float64
     7   Humidity                32173 non-null  float64
     8   WindDirection(Degrees)  32273 non-null  float64
     9   Speed                   32258 non-null  float64
     10  TimeSunRise             32398 non-null  object 
     11  TimeSunSet              32398 non-null  object 
    dtypes: float64(6), int64(2), object(4)
    memory usage: 3.0+ MB


**As you can see above in RangeIndex: 32398 entries but Column: Temperature, Pressure, Humidity, WindDirection,**  
**Speed have less amount of non null entries**
