# Ex.No: 01A PLOT A TIME SERIES DATA
###  Date: 25-07-2026

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
df = pd.read_csv("AirPassengers.csv")
df["Month"] = pd.to_datetime(df["Month"])
plt.figure(figsize=(12,5))
plt.plot(df["Month"], df["#Passengers"], color="blue")
plt.title("Air Passengers Over Time")
plt.xlabel("Year")
plt.ylabel("Number of Passengers")
plt.grid(True)
plt.show()
```

# OUTPUT:

<img width="1404" height="587" alt="image" src="https://github.com/user-attachments/assets/d572aae2-48ed-4245-97dd-1dcdddfcfee4" />

# RESULT:
Thus, the Python program to plot the time series data of the year-wise average temperature from the given dataset was successfully developed and executed using the Pandas and Matplotlib libraries.
