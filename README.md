# descripcion_de_pandas5.1

+ Here we import the libraries needed to make it work

import pandas as pd
import numpy as np

+ We import the csv data from the link and show it

cars1 = pd.read_csv("https://raw.githubusercontent.com/guipsamora/pandas_exercises/master/05_Merge/Auto_MPG/cars1.csv")
cars2 = pd.read_csv("https://raw.githubusercontent.com/guipsamora/pandas_exercises/master/05_Merge/Auto_MPG/cars2.csv")

print(cars1.head())
print(cars2.head())

+ Shows the point at which point you select from the table from the mpg column to the cars column

cars1 = cars1.loc[:, "mpg":"car"]
cars1.head()

+ We print the number of rows and columns

print(cars1.shape)
print(cars2.shape)

+ Collect what we have in cars 1 along with the cars2 data

cars = cars1.append(cars2)
cars

+ We only create random numbers from one range to another

nr_owners = np.random.randint(15000, high=73001, size=398, dtype='l')
nr_owners

+ Here the random numbers we create with your name now we add them to the table of cars where cars1 and cars2 are

cars['owners'] = nr_owners
cars.tail()
