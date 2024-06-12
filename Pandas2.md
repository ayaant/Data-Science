import pandas as pd

titanic = pd.read_csv("titanic.csv")
print(titanic.head()) #print first 5 columns
'''
print(titanic[["Name","Age"]]) #print 2 specified columns
print(titanic[titanic["Age"]>15]) #all passengers with age greater than 15
print(titanic.tail()) #print last 5 columns
print(titanic[(titanic["Pclass"]==2) | (titanic["Pclass"]==3)]) # | = or
print(titanic[titanic["Pclass"].isin([2,3])]) #prints passengers from Pclass 2 or 3
firstc = titanic[(titanic["Pclass"]== 1) & (titanic["Sex"]== "male")] #stores information on all male passengers in first class, and = &
print(firstc["Fare"].mean()) # prints mean fare of male first class

# get particular column out of a condition
print(titanic.loc[titanic["Age"]>18,"Name"]) #prints names of people with age > 18
print(titanic.iloc[9:25,2:5]) #slice columns and rows with index positions

#changing values in dataset
titanic.iloc[0:3,2] = "Ayaan"
titanic.to_csv("edited_titanic")

# creating new column
titanic["New Fare"] = titanic["Fare"] * titanic["Pclass"]
print(titanic.head())

#renaming column
rename = titanic.rename(columns= {'Pclass':'Passenger Class', 'Siblings/Spouses Aboard': 'SS Aboard'})
print(rename)

#print min max and median for Age and fare
print(titanic.agg({"Age":["min","max","median"], "Fare":["min","max","median"]}))
'''

#group by data category
dc = titanic.groupby("Sex")
print(dc)
print(titanic[["Sex","Age"]].groupby("Sex").mean()) #displays mean age for males and females
print(titanic.groupby(["Sex","Pclass"])["Fare"].mean()) #displays average fare according to sex and pclass
print(titanic["Pclass"].value_counts())
