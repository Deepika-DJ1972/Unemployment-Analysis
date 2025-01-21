# Unemployment Analysis in India

This project analyzes the unemployment rate in India, focusing on the periods before and after COVID-19. The objective is to identify trends, compare regional impacts, and derive insights into labor participation and employment growth.

---

## 📊 Project Overview

This analysis covers:
- **Pre-COVID vs. Post-COVID Unemployment Rate Comparison**
- **Regional Analysis of Unemployment**
- **Employment Growth Trends**
- **Labor Participation Rate Analysis**

---

## 📁 Data Sources

The project utilizes two datasets:
1. **Unemployment in India (2019-2020):** Detailed unemployment and employment data across states and regions.
2. **Unemployment Rate up to November 2020:** Trends in unemployment up to late 2020.

---

## 🔧 Features and Steps

### Data Cleaning:
- Missing value imputation using mean/median.
- Conversion of date columns to datetime format.
- Removal of duplicates and unnecessary columns.

### Features Created:
- **Unemployment Change:** Percentage change by state/region.
- **Employment Growth:** Growth percentages calculated by region.
- **COVID Period Flag:** Categorizing data into pre- and post-COVID.

### Analysis & Visualizations:
- **Bar Charts:** Compare unemployment rates across regions pre- and post-COVID.
- **Line Graphs:** Trends in employment growth and labor participation.
- **Heatmaps:** Correlations between unemployment and labor participation rates.

---

## 🛠️ Tools and Libraries

- **Python**: Pandas, NumPy, Matplotlib, Seaborn
- **Jupyter Notebook**: For analysis and visualization
- **GitHub**: For version control and project hosting

---

## 💡 Key Insights

1. **Top Unemployment States Post-COVID:** Highlighted states with the largest increase in unemployment rates.
2. **Regional Trends:** Insights into regions with the lowest labor participation rates.
3. **Impact of COVID:** Significant changes in urban and rural unemployment levels.

---

## 📈 Sample Code Snippet

```python
import pandas as pd

# Grouping data by states and calculating unemployment change
df['Unemployment_Change'] = df.groupby(['States'])['Unemployment Rate'].pct_change() * 100

# Displaying top 5 states with the highest unemployment change
top_5_states = df.groupby('States')['Unemployment_Change'].mean().sort_values(ascending=False).head(5)
print(top_5_states)
