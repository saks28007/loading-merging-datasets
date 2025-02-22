# EXP 1 : Loading and Merging Datasets from the UCIML Repository.
This repository includes the code and results for the first experiment in the Introduction to Data Science with Python course. It focuses on loading, cleaning, and merging datasets from the UCI Machine Learning Repository, covering key data preparation steps and simple visualizations for analysis.

# Experiment Overview
# Steps:
**1. Loading Data :** *Datasets are imported using the Pandas library from the UCI Machine Learning Repository.*
<br>
**2. Exploring Data :** *A quick preview of the first few rows of each dataset is displayed to grasp their structure and content.*
<br>
**3. Combining Data :** *Datasets are merged based on a shared column (such as 'ID') to create a unified dataset.*
<br>
**4. Exporting Data :** *The combined dataset is optionally saved to a CSV file for further use or analysis.*

# Key Concepts Applied: 
**-Pandas Library :** _A tool for working with and analyzing data easily._
<br>
**-DataFrames :** _A structure used in Pandas to store and organize data in tables._
<br>
**-Merging Datasets :** _The pd.merge() function is used to join two datasets together based on a common column, creating one unified dataset._

# Action Plan
**1. Get started with Google Colab :**

 *~Launch Google Colab.*
 <br>
 *~Start a fresh notebook.*

**2. Import required libraries :**

*~Initialize the necessary libraries for the analysis.*
```
import pandas as pd
```

**3. Fetch the Datasets :**

*~Download the datasets from the UCI Machine Learning Repository and mount Google Drive to access them.*
```
df1 = pd.read_csv('/content/drive/MyDrive/winequality-red.csv',delimiter=';')
df2 = pd.read_csv('/content/drive/MyDrive/winequality-white.csv',delimiter=';')
```

**4. Examine the Datasets :**

*~Display the initial rows of each dataset to ensure they are loaded properly.*
```
print("Red Wine Data: ")
df1['type']='red'
print(df1.head())


print("White Wine Data: ")
df2['type']='white'
print(df2.head())
```

**5. Merge the Datasets :**

*~Merge the datasets on a common column (e.g., 'ID').*
```
merged= pd.concat([df1, df2], ignore_index=True)
```

**6. Review the combined dataset :**

*~Show the first few rows of the merged dataset to confirm the integration.*
```
print("Combined: ")
print(merged.head())
```

**7. Export the combined dataset :**

*~Save the combined dataset as a CSV file for subsequent analysis and reference.*
```
merged.to_csv('merged_dataset.csv', index=False)
```
