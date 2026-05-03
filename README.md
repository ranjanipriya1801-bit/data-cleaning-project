Data Cleaning & Visualization Project


 Objective
To clean, process, and analyze a raw dataset and visualize meaningful insights using Python.

Dataset Used
Student Performance Dataset (contains marks of students in different subjects)

🛠 Tools & Libraries Used
Python
Pandas
Matplotlib
Seaborn

🔧 Steps Performed

1. Data Cleaning
Checked for missing values and filled them using mean/median
Removed duplicate rows
Handled outliers using filtering
Converted data types where required

2. Data Processing
Selected relevant columns (Name, Maths, Science, English)
Calculated average marks
Categorized students based on performance

3. Data Visualization
Created the following graphs:
📊 Bar chart → Subject-wise average marks
📈 Line chart → Student performance trend
🥧 Pie chart → Grade distribution
💻 Sample Python Code


Python

import pandas as pd
import matplotlib.pyplot as plt
import seaborn as sns
df = pd.read_csv("students.csv")
df.drop_duplicates(inplace=True)
df.fillna(df.mean(numeric_only=True), inplace=True)
df['Average'] = df[['Maths','Science','English']].mean(axis=1)
plt.figure()
df[['Maths','Science','English']].mean().plot(kind='bar')
plt.title("Average Marks per Subject")
plt.show()
plt.figure()
df['Average'].plot(kind='line')
plt.title("Student Average Trend")
plt.show()
plt.figure()
df['Average'].plot(kind='pie', autopct='%1.1f%%')
plt.title("Average Distribution")
plt.show()

📈 Key Insights
Most students scored higher in Maths
Few students had low performance due to outliers
Overall average performance is moderate

🎯 Conclusion
This project helped in understanding:
Data preprocessing techniques
Handling missing and inconsistent data
Creating meaningful visualizations
Extracting insights from raw data

✅ Expected Outcome Achieved
Successfully learned data cleaning, visualization, and storytelling with data.
