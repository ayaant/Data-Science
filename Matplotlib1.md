import matplotlib.pyplot as plt
import numpy as np
import random 
'''
x = np.linspace(0,10,20)
y = np.linspace(10,0,20)
fig = plt.figure(figsize=(10,5))
fig1 = plt.subplot()
fig1.plot(x,y)
plt.show()
'''

#x = [0,1,2,3,4,5]
#y = [0,1,4,9,16,25]
#plt.plot(x,y)
#plt.xlim(0,5) # 0 start, 5 end
#plt.ylim(0,25) #0 start, 25 end
#plt.xticks(np.arange(0,5,step=1)) #x axis increases by 1 each time
#plt.yticks(np.arange(0,25,step=4)) # y axis increases by 4 each time

#how to automatically adjust axis ranges
#plt.autoscale(tight=True)

#calculate axis range with a buffer
#buffer_point = 5
#plt.xlim(min(x)-buffer_point,max(x)+buffer_point)
#plt.ylim(min(y)-buffer_point,max(y)+buffer_point)

#advanved axis range control
#fig,ax = plt.subplots()
#ax.plot(x,y) 
#ax.set_xlim(0,5)
#ax.set_ylim(0,25)

#different types of plotting
#plt.plot(x,y,"p--") # line along with the dots
#plt.plot(x,y,"r--") # just a red line
#plt.plot(x,y,"b-") # just a blue line
#plt.plot(x,y,"b--") # dotted blue line
#plt.plot(x,y,"g^") # line with traingles rather than dots
#plt.plot(x,y,"b--",label="y=x",linewidth = 5)
#plt.axis([0,10,0,50])
#plt.xlabel("X-Axis")
#plt.ylabel("Y-Axis")
#plt.title("Graph")
#plt.legend()

#plot multiple graphs on a single plot
#z = [0,1,8,27,64,125]
#plt.plot(x,y,"b-",label="y=x^2",linewidth = 3)
#plt.plot(x,z,"r--",label="y=x^3",linewidth = 3)
#plt.axis([0,10,0,150])
#plt.xlabel("X-Axis")
#plt.ylabel("Y-Axis")
#plt.title("Graph")
#plt.legend()

#year = [1972, 1982, 1992, 2002, 2012]
#e_india = [100.6, 158.61, 305.54, 394.96, 724.79]
#e_bangladesh = [10.5, 25.21, 58.65, 119.27, 274.87]

#plt.plot(year,e_india,color = "Blue", marker = "o", markersize = 12,label="Electricity Consumption of India", linewidth = 3)
#plt.plot(year,e_bangladesh,color = "Red", linestyle = "dashed",label="Electricity Consumption of Bangladesh", linewidth = 3)
#plt.axis([1972,2012,0,800])
#plt.xlabel("Year")
#plt.ylabel("Energy Consumption")
#plt.title("Yearly Energy Consumption")
#plt.legend()

#SCATTER PLOT
x = np.random.rand(50)
y = np.random.rand(50)
colors = np.random.rand(50)

#creating a scatter plot with color mapping
plt.scatter(x,y,c=colors,cmap="viridis",s=100,alpha=0.8)
cbar = plt.colorbar()
cbar.set_label("Colour Value")
plt.title("Scatter Plot")
plt.xlabel("X Value")
plt.ylabel("Y Value")

plt.show()
