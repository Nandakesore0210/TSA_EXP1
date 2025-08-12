# Ex.No: 01A PLOT A TIME SERIES DATA
###  Date: 12-8-2025

# AIM:
To Develop a python program to Plot a time series data (population/ market price of a commodity
/temperature.
# ALGORITHM:
1. Import the required packages like pandas and matplot
2. Read the dataset using the pandas
3. Calculate the mean for the respective column.
4. Plot the data according to need and can be altered monthly, or yearly.
5. Display the graph.
# PROGRAM:

```python
import pandas as pd
import matplotlib.pyplot as plt
data = pd.read_csv("Gold Price Prediction.csv")
data.head(10)

data.info()

data['Date'] = pd.to_datetime(data['Date'])
data.set_index('Date', inplace=True)

plt.figure(figsize=(10, 6))
plt.plot(data.index, data['Price Today'], label='Gold Price Today', color='blue')

plt.title('Gold Price Today Over Time')
plt.xlabel('Date')
plt.ylabel('Gold Price')
plt.grid(True)
plt.legend()

plt.show()
```
# OUTPUT:

<img width="1010" height="403" alt="image" src="https://github.com/user-attachments/assets/37979d52-eb8a-4abb-9405-2781b2607628" />

<img width="534" height="476" alt="image" src="https://github.com/user-attachments/assets/0d66ac96-2c7f-46c9-9625-28782ce13a56" />

<img width="876" height="537" alt="image" src="https://github.com/user-attachments/assets/28e8f9f0-5b1f-41c9-82fa-21a503acb747" />


# RESULT:
Thus we have created the python code for plotting the time series of given data.
