# Ex.No: 01A PLOT A TIME SERIES DATA
###  Date: 28-07-2026

# AIM:
To develop a Python program to plot a time series data (temperature) by calculating the yearly average temperature from the given dataset using the Pandas and Matplotlib libraries.

# ALGORITHM:
1. Import the required libraries such as Pandas and Matplotlib.
2. Read the city_temperature.csv dataset using the read_csv() function.
3. Remove rows containing missing values in the AvgTemperature column.
4. Group the data by Year and calculate the mean of the AvgTemperature column.
5. Plot the yearly average temperature using a line graph.
6. Add the graph title, X-axis label, Y-axis label, and grid for better visualization.
7. Display the graph using plt.show().
   
# PROGRAM:
```python
import pandas as pd
import matplotlib.pyplot as plt
df = pd.read_csv("city_temperature.csv", low_memory=False)
df = df.dropna(subset=["AvgTemperature"])
yearly = df.groupby("Year")["AvgTemperature"].mean()
plt.figure(figsize=(10,5))
plt.plot(yearly.index, yearly.values, marker="o")
plt.title("Year-wise Average Temperature")
plt.xlabel("Year")
plt.ylabel("Average Temperature (°F)")
plt.grid(True)
plt.show()
```

# OUTPUT:

<img width="1297" height="588" alt="image" src="https://github.com/user-attachments/assets/38a5843e-14e8-42b9-abe4-d1483773eaa4" />

# RESULT:
Thus, the Python program to plot the time series data of the year-wise average temperature from the given dataset was successfully developed and executed using the Pandas and Matplotlib libraries.
