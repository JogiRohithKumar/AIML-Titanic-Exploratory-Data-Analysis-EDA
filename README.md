# AIML-Titanic-Exploratory-Data-Analysis-EDA
This project focuses on applying *Exploratory Data Analysis (EDA)* to the famous *Titanic dataset. The goal is to understand the dataset through **summary statistics, **visualizations, and **feature relationships*, enabling better decision-making for future machine learning models.

---

## 📁 Dataset

The dataset used is the *Titanic passenger data* (titanic.csv), which includes the following columns:

- PassengerId  
- Survived  
- Pclass  
- Name  
- Sex  
- Age  
- SibSp  
- Parch  
- Ticket  
- Fare  
- Cabin  
- Embarked

---

## ✅ Steps Performed

### 1. Import Dataset & Generate Basic Info
- Loaded the dataset using pandas.
- Displayed structure using .info(), .describe().
- Identified null values with .isnull().sum().
- Explored data types and class distributions using .value_counts().

### 2. Summary Statistics
- Calculated *mean, **median, **mode, **standard deviation, **skewness, and **kurtosis* of numeric features.
- Interpreted insights about distributions and variability.

### 3. Histograms & Boxplots
- Plotted *histograms* for numerical features like Age and Fare.
- Used *boxplots* to detect and visualize outliers.
- Example: sns.boxplot(x='Survived', y='Age', data=df)

### 4. Correlation Matrix & Heatmap
- Computed correlation using df.corr().
- Visualized it with seaborn.heatmap() to identify relationships between variables.

### 5. Pairplots
- Plotted sns.pairplot(df, hue='Survived') to observe relationships between key features.

### 6. Interactive Visualization (Bonus)
- Used *Plotly Express* to create an interactive scatter plot:
  python
  import plotly.express as px
  fig = px.scatter(df, x='Age', y='Fare', color='Survived', hover_data=['Name'])
  fig.show()

### 7. Outlier Handling
- Used the IQR method to remove outliers from features like **Fare**



## 🛠️ Tools & Libraries Used

```python
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
import seaborn as sns
import plotly.express as px
