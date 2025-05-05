# EXNO-5-DS-DATA VISUALIZATION USING MATPLOT LIBRARY

# Aim:
  To Perform Data Visualization using matplot python library for the given datas.

# EXPLANATION:
Data visualization is the graphical representation of information and data. By using visual elements like charts, graphs, and maps, data visualization tools provide an accessible way to see and understand trends, outliers, and patterns in data.

# Algorithm:
STEP 1:Include the necessary Library.

STEP 2:Read the given Data.

STEP 3:Apply data visualization techniques to identify the patterns of the data.

STEP 4:Apply the various data visualization tools wherever necessary.

STEP 5:Include Necessary parameters in each functions.

# Coding and Output:

```
import pandas as pd
import numpy as np
import seaborn as sns
import matplotlib.pyplot as plt
     

x = [1, 2, 3, 4, 5]
y = [3, 6, 2, 7, 1]
plt.figure(figsize=(6, 4))
plt.plot(x, y, label="Line XY", color='blue')
plt.xlabel("X Axis")
plt.ylabel("Y Axis")
plt.title("Line Graph with Labels and Legend")
plt.legend()
plt.grid(True)
plt.show()

```
![Screenshot (318)](https://github.com/user-attachments/assets/50ac2c07-85f1-4b71-beec-8cdc071f35f8)
```
x1 = [1, 2, 3]
y1 = [2, 4, 1]
x2 = [1, 2, 3]
y2 = [4, 1, 3]
plt.figure(figsize=(6, 4))
plt.plot(x1, y1, label="Line 1", marker='o')
plt.plot(x2, y2, label="Line 2", marker='x')
plt.xlabel("X Axis")
plt.ylabel("Y Axis")
plt.title("Two Line Plots")
plt.legend()
plt.grid(True)
plt.show()
```
![Screenshot (320)](https://github.com/user-attachments/assets/284024eb-4525-4812-b59e-c7d49702509f).
```
x = [1, 2, 3, 4, 5]
y1 = [10, 12, 14, 16, 18]
y2 = [5, 7, 9, 11, 13]
y3 = [2, 4, 6, 8, 10]

x_values = [0,1,2,3,4,5]
y_values = [0,1,4,9,16,25]

plt.figure(figsize=(6, 4))
plt.plot(x, y1, label="Line 1")
plt.fill_between(x, y2, y3, color='gray', alpha=0.3, label="Fill Between")
plt.xlabel("X Axis")
plt.ylabel("Y Axis")
plt.title("Line Graph with fill_between")
plt.legend()
plt.show()
```
![Screenshot (322)](https://github.com/user-attachments/assets/57cb9c70-9f42-454a-995d-e2e51a2c0e19).
```
x = np.array([1, 2, 3, 4, 5, 6, 7, 8, 9, 10])
y = np.array([2, 4, 5, 7, 8, 8, 9, 10, 11, 12])
x_new = np.linspace(x.min(), x.max(), 300)
spline = make_interp_spline(x, y, k=3)
y_smooth = spline(x_new)

plt.figure(figsize=(6, 4))
plt.plot(x_new, y_smooth, label="Cubic Spline", color="purple")
plt.scatter(x, y, color="red", label="Original Points")
plt.title("Cubic Spline Interpolation")
plt.xlabel("X")
plt.ylabel("Y")
plt.legend()
plt.grid(True)
plt.show()

```
![Screenshot (324)](https://github.com/user-attachments/assets/83c1aada-b4dc-4add-8ef7-79bc557e3c20).
```
values = [5, 6, 3, 7, 2]
names = ["A", "B", "C", "D", "E"]
plt.figure(figsize=(6, 4))
plt.bar(names, values, color='skyblue')
plt.xlabel("Categories")
plt.ylabel("Values")
plt.title("Simple Bar Graph")
plt.show()
```
![Screenshot (326)](https://github.com/user-attachments/assets/4543ddd2-b118-4644-858f-059a08b4600b)
```
import matplotlib.pyplot as plt

values = [5, 6, 3, 7, 2]
names  = ["A", "B", "C", "D", "E"]
colors = ['red', 'green', 'blue', 'orange', 'purple'] 


plt.figure(figsize=(6, 4))
plt.bar(names, values, color=colors)
plt.xlabel("Categories")
plt.ylabel("Values")
plt.title("Bar Graph Example")
plt.show()
```
![Screenshot (328)](https://github.com/user-attachments/assets/ef3e3cf3-c451-46d3-a9aa-4cb778d7a8ab)
```
import seaborn as sns
import matplotlib.pyplot as plt


df = sns.load_dataset("tips")


avg_total_bill = df.groupby("day")["total_bill"].mean()
avg_tip = df.groupby("day")["tip"].mean()


plt.figure(figsize=(8, 6))
plt.bar(avg_total_bill.index, avg_total_bill, label='Total Bill', color='skyblue')
plt.bar(avg_tip.index, avg_tip, bottom=avg_total_bill, label='Tip', color='lightgreen')


plt.xlabel('Day of the Week')
plt.ylabel('Amount')
plt.title('Average Total Bill and Tip by Day')
plt.legend()
plt.show()
```
![Screenshot (330)](https://github.com/user-attachments/assets/2953f343-467a-4289-b727-e103b99d2278)

```
x_values = [0, 1, 2, 3, 4, 5]
y_values = [0, 1, 4, 9, 16, 25]

plt.figure(figsize=(6, 4))
plt.scatter(x_values, y_values, color='blue')
plt.xlabel("X Axis")
plt.ylabel("Y Axis")
plt.title("Basic Scatter Plot")
plt.grid(True)
plt.show()

```
![Screenshot (332)](https://github.com/user-attachments/assets/5c022f0c-2dcb-4357-bee2-990ef532a2a9).
```
x = [1,2,3,4,5,6,7,8,9,10]
y = [2,4,5,7,6,8,9,11,12,12]

plt.figure(figsize=(6, 4))
plt.scatter(x, y, label="Stars", color="green", marker="*", s=100)
plt.xlabel("X Axis")
plt.ylabel("Y Axis")
plt.title("Custom Scatter Plot")
plt.legend()
plt.grid(True)
plt.show()

```
![Screenshot (334)](https://github.com/user-attachments/assets/b6ab133b-9c66-45eb-b47d-4a237919237e)
```
activities = ['eat', 'sleep', 'work', 'play']
slices = [3, 7, 8, 6]
colors = ['r', 'y', 'g', 'b']

plt.figure(figsize=(6, 6))
plt.pie(slices, labels=activities, colors=colors, autopct='%1.1f%%', startangle=140)
plt.title("Daily Activities Pie Chart")
plt.axis('equal')  # Equal aspect ratio ensures that pie is drawn as a circle.
plt.show()
```

![Screenshot (336)](https://github.com/user-attachments/assets/a763edbb-dde4-47bc-b1f5-85cb69158ed5)



# Result:
 Thus the program is executed successfully.
