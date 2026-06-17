Unemployment Analysis in India
Project Overview

This project analyzes unemployment data in India using Python. The objective is to understand unemployment trends over time and compare unemployment rates across different regions of the country through data visualization and analysis.

Dataset

The dataset contains information about:

Region
Date
Frequency
Estimated Unemployment Rate (%)
Estimated Employed
Estimated Labour Participation Rate (%)
Area (Urban/Rural)

Dataset File:
Unemployment in India.csv

Technologies Used
Python
Pandas
Matplotlib
Seaborn
Google Colab
Project Objectives
Analyze unemployment trends in India.
Visualize unemployment rates over time.
Compare unemployment rates across different states/regions.
Identify regions with the highest unemployment rates.
Project Workflow
1. Import Required Libraries
import pandas as pd
import matplotlib.pyplot as plt
import seaborn as sns
2. Load Dataset
df = pd.read_csv("Unemployment in India.csv")
3. Data Cleaning

Remove extra spaces from column names and convert the Date column into datetime format.

df.columns = df.columns.str.strip()
df['Date'] = pd.to_datetime(df['Date'])
4. Unemployment Trend Analysis

Visualize unemployment rates over time using a line chart.

plt.plot(df['Date'], df['Estimated Unemployment Rate (%)'])
5. Regional Unemployment Analysis

Compare unemployment rates across different regions using a bar chart.

sns.barplot(
    x='Region',
    y='Estimated Unemployment Rate (%)',
    data=df
)
6. Identify Highest Unemployment Regions

Calculate average unemployment rates by region.

region_unemployment = df.groupby('Region')['Estimated Unemployment Rate (%)'].mean()
Results
Unemployment Rate Over Time

A line graph was created to visualize changes in unemployment rates across different time periods.

Average Unemployment Rate by Region

A bar chart was used to compare unemployment levels among regions.

Top 10 Regions with Highest Average Unemployment Rate
Region	Average Unemployment Rate (%)
Tripura	28.35
Haryana	26.28
Jharkhand	20.59
Bihar	18.92
Himachal Pradesh	18.54
Delhi	16.50
Jammu & Kashmir	16.19
Chandigarh	15.99
Rajasthan	14.06
Uttar Pradesh	12.55
Visualizations
Unemployment Rate Trend Over Time
Average Unemployment Rate by Region

These visualizations help in understanding regional disparities and overall unemployment patterns in India.

Future Enhancements
Predict future unemployment rates using Machine Learning.
Create interactive dashboards using Power BI or Tableau.
Compare unemployment rates between Urban and Rural areas.
Perform state-wise trend forecasting.
Conclusion

This project provides insights into unemployment patterns across India. Through data visualization and statistical analysis, it helps identify regions with higher unemployment rates and understand employment trends over time.

Author

Rithiga

Data Analysis Project using Python, Pandas, Matplotlib, and Seaborn.
