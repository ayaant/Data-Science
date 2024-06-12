" Display dataset head and info. Provide the mean, min, max for the following - petal_length, petal_width, sepal_length, sepal_width. If possible provide the count of rows present for each type of species present in the dataset."
'''
# Load the dataset
df = pd.read_csv("iris.csv")

# Display dataset head
print("Dataset Head:")
print(df.head())

# Display dataset info
print("\nDataset Info:")
print(df.info())

# Provide the mean, min, max for specified columns
print("\nStatistics for petal_length, petal_width, sepal_length, sepal_width:")
print(df[['petal_length', 'petal_width', 'sepal_length', 'sepal_width']].agg(['mean', 'min', 'max']))

# Count of rows present for each type of species
print("\nCount of rows for each species:")
print(df['species'].value_counts())
