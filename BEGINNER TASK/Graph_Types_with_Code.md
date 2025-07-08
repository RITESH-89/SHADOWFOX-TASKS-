# Graph Types with Code Examples

This section demonstrates common graph types available in **Matplotlib** and **Seaborn**, including a brief explanation of when to use each, along with beginner-friendly code snippets.

---

## 1. 📈 Line Plot

**Use Case**: Visualizing trends over time or sequential data.

### ➤ Matplotlib
```python

import matplotlib.pyplot as plt

x = [1, 2, 3, 4, 5]
y = [10, 12, 8, 15, 20]

plt.plot(x, y)
plt.title("Line Plot Example")
plt.xlabel("X Axis")
plt.ylabel("Y Axis")
plt.grid(True)
plt.show()

### ➤ Seaborne
'''python

import seaborn as sns
import matplotlib.pyplot as plt

# Sample data
data = sns.load_dataset("flights")
sns.lineplot(data=data, x="year", y="passengers")
plt.title("Passengers Over Years")
plt.show()

## 2. 📊 Bar Chart
Use Case: Comparing quantities between different categories.

import matplotlib.pyplot as plt

categories = ["A", "B", "C", "D"]
values = [23, 45, 56, 78]

plt.bar(categories, values)
plt.title("Bar Chart Example")
plt.xlabel("Category")
plt.ylabel("Value")
plt.show()

import seaborn as sns
import matplotlib.pyplot as plt

data = sns.load_dataset("titanic")
sns.countplot(data=data, x="class")
plt.title("Passenger Count by Class")
plt.show()

3. 🔵 Scatter Plot
Use Case: Showing the relationship between two continuous variables.

import matplotlib.pyplot as plt

x = [5, 7, 8, 7, 2, 17, 2, 9]
y = [99, 86, 87, 88, 100, 86, 103, 87]

plt.scatter(x, y)
plt.title("Scatter Plot Example")
plt.xlabel("X Value")
plt.ylabel("Y Value")
plt.show()

import seaborn as sns
import matplotlib.pyplot as plt

data = sns.load_dataset("iris")
sns.scatterplot(data=data, x="sepal_length", y="sepal_width", hue="species")
plt.title("Sepal Size by Species")
plt.show()

4. 📉 Histogram
Use Case: Visualizing the distribution of a single numerical variable.

import matplotlib.pyplot as plt
import numpy as np

data = np.random.randn(1000)
plt.hist(data, bins=30, color='skyblue', edgecolor='black')
plt.title("Histogram Example")
plt.xlabel("Value")
plt.ylabel("Frequency")
plt.show()

import seaborn as sns
import matplotlib.pyplot as plt

data = sns.load_dataset("diamonds")
sns.histplot(data=data, x="price", bins=30, kde=True)
plt.title("Price Distribution of Diamonds")
plt.show()

5. 🧁 Pie Chart (Only in Matplotlib)

import matplotlib.pyplot as plt

labels = ['Apples', 'Bananas', 'Cherries', 'Dates']
sizes = [15, 30, 45, 10]

plt.pie(sizes, labels=labels, autopct='%1.1f%%', startangle=140)
plt.title("Fruit Distribution")
plt.axis('equal')
plt.show()

6. 📦 Box Plot
Use Case: Summarizing distribution using min, max, median, and outliers.

import matplotlib.pyplot as plt
import numpy as np

data = [np.random.normal(0, std, 100) for std in range(1, 4)]
plt.boxplot(data)
plt.title("Box Plot Example")
plt.xlabel("Dataset")
plt.ylabel("Value")
plt.show()

import seaborn as sns
import matplotlib.pyplot as plt

data = sns.load_dataset("tips")
sns.boxplot(data=data, x="day", y="total_bill")
plt.title("Bill Distribution by Day")
plt.show()

7. 🔥 Heatmap (Seaborn Only)
Use Case: Displaying correlation matrices or intensity values.

import seaborn as sns
import matplotlib.pyplot as plt

data = sns.load_dataset("iris")
corr = data.corr()

sns.heatmap(corr, annot=True, cmap="coolwarm")
plt.title("Correlation Heatmap")
plt.show()

