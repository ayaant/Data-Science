import pandas as pd

cars = pd.read_csv("cars.csv")
print(cars)
print(cars.info()) # gives information
print(cars.describe()) # gives all stats
print(cars.shape) # number of rows and columns
# .fillna() to fill a null value with something else
# .drop() to drop a column from data set
# .astype() to change 
cars.mpg = cars.mpg.astype(int)
cars.vs = cars.vs.fillna(cars.qsec.mean())
cars = cars.drop(columns= ["vs"])
#iloc = index location
print(cars.iloc[:,:])
print(cars.iloc[0:5,4])
print(cars.iloc[:,0])

print(cars["mpg"])
print(cars.loc[0:5,"mpg"]) # first 5
print(cars.loc[0:5,"mpg":"qsec"])
cars["am"] = 1
print(cars["am"]) #change value of column to 1

#sorting cyl column in ascending order
print(cars.sort_values(by= "cyl", ascending= False)) #ascending = False makes it descending

#cyl > 6 and hp > 300
good = ((cars["cyl"]>6) & (cars["hp"]>300))
good_cars = cars[good]
print(good_cars)
