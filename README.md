📊 Data Visualization with Matplotlib

This repository demonstrates different types of plots and charts using Matplotlib, one of the most popular Python libraries for data visualization.
It covers line plots, bar charts, histograms, scatter plots, pie charts, subplots, and even 3D plots.

🔧 Requirements

Install the required libraries before running the code:

pip install matplotlib pandas numpy

📈 Plots & Charts Covered
1️⃣ Line Plot

Used to show trends or relationships between variables.

import matplotlib.pyplot as plt
x = [1, 2, 3, 4, 5]
y = [5, 1, 7, 8, 2]

plt.plot(x, y, color='r', marker='o', linestyle='--')
plt.title("Line Plot Example")
plt.xlabel("X values")
plt.ylabel("Y values")
plt.show()

2️⃣ Bar Plot

Used to compare categorical variables.

x = ['A','B','C','D']
y = [4,6,1,2]

plt.bar(x, y, color='g')
plt.title("Bar Chart Example")
plt.show()


Horizontal bar chart:

plt.barh(x, y, color='orange')
plt.show()

3️⃣ Histogram

Shows distribution of numerical data.

import numpy as np
data = np.random.randn(1000)  # Normal distribution
plt.hist(data, bins=20, color='red')
plt.title("Histogram Example")
plt.show()


Stacked histogram for multiple datasets:

data1 = np.random.normal(0, 1, 5000)
data2 = np.random.normal(0, 1, 5000)

plt.hist([data1, data2], bins=20, color=['r','b'], label=['Dist1','Dist2'])
plt.legend()
plt.title("Stacked Histogram")
plt.show()

4️⃣ Scatter Plot

Shows relationship between two variables.

x = np.random.rand(50)
y = np.random.rand(50)

plt.scatter(x, y, c='blue', marker='X')
plt.title("Scatter Plot Example")
plt.show()


Using Pandas DataFrame:

import pandas as pd
data = pd.read_csv("Bank_churn (1).csv")

data.plot.scatter(x='Age', y='Balance')
plt.title("Age vs Balance")
plt.show()

5️⃣ Pie Chart

Shows percentage distribution of categorical data.

langs = ['C','Python','Java']
students = [20,100,40]

plt.pie(students, labels=langs, autopct='%1.1f%%', explode=(0,0.1,0.1), shadow=True)
plt.title("Pie Chart Example")
plt.show()

6️⃣ Subplots

Multiple plots in one figure.

x = np.linspace(0, 10, 100)

plt.subplot(1,2,1)
plt.plot(x, np.sin(x))

plt.subplot(1,2,2)
plt.plot(x, np.cos(x))

plt.suptitle("Sine & Cosine Waves")
plt.show()

7️⃣ 3D Plot
from mpl_toolkits.mplot3d import Axes3D

x = np.random.rand(20)
y = np.random.rand(20)
z = np.random.rand(20)

fig = plt.figure()
ax = fig.add_subplot(projection='3d')
ax.scatter(x, y, z, c='orange')
plt.title("3D Scatter Plot")
plt.show()

📌 Conclusion

This project demonstrates how to use Matplotlib for data visualization with different chart types.
These plots are widely used in data analysis, machine learning, and statistical research.

✅ Feel free to fork, clone, and contribute! 🚀
