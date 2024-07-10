import matplotlib.pyplot as plt
import pandas as pd
import numpy as np

'''
car = pd.read_csv("cars.csv")
print(car.head())
df = pd.DataFrame(car) #dataframe is required to pick particular things
name = df["model"].head(10)
cylinders = df["cyl"].head(10)
print(name)
print(cylinders)
fig,ax = plt.subplots(figsize=(16,10))
#plt.bar(name,cylinders)
ax.barh(name,cylinders)
ax.invert_yaxis()
ax.set_title("Car Cylinders") 
# add annotation to bars
for i in ax.patches:
    plt.text(i.get_width()+0.2,i.get_y()+0.5,str(round(i.get_width(),2)),fontsize=10,fontweight="bold",color="black")
plt.show()
'''

#multiple barplots
#set width of the bar
bar_width = 0.25
fig = plt.subplots(figsize=(16,10))
it = [66,78,53,92,59]
ece = [72,87,66,81,57]
cse = [57,85,72,91,43]

#setting pos of bars on the x axis
bar1 = np.arange(len(it))
bar2 = []
for i in bar1:
    bar2.append(i + bar_width)
bar3 = [i + bar_width for i in bar2]

#create the plot
plt.bar(bar1,color="black",width=bar_width,edgecolor="white",label = "IT")
plt.bar(bar2,color="red",width=bar_width,edgecolor="white",label = "ECE")
plt.bar(bar3,color="blue",width = bar_width, edgecolor="white",label="CSE")
plt.xlabel("Branch of Engineering",fontweight="bold",fontsize=8)
plt.ylabel("Successful Students",fontweight="italics",fontsize=8)
#plt.xticks(['2018','2019','2020','2021','2022'])
plt.legend()
plt.show()

