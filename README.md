# 📊 Python Data Science & Visualization Portfolio

> **Beginner to Intermediate projects covering NumPy, Pandas, Matplotlib & Seaborn**  
> Built with Jupyter Notebooks | Real datasets | Clean visualizations

---

## 👤 About This Repository

This repository contains my hands-on practice notebooks for Python's core Data Science libraries.
Each notebook is written from scratch — starting from zero knowledge and building up to real chart
visualizations, data cleaning, and statistical analysis.

---

## 📁 Repository Structure

```
📦 python-data-science-portfolio/
 ┣ 📓 Numpy.ipynb          → Array operations, math, reshaping
 ┣ 📓 Pandas.ipynb         → DataFrames, data cleaning, filtering
 ┣ 📓 Matplotlib.ipynb     → 8+ chart types with customization
 ┣ 📓 Seaborn.ipynb        → Statistical plots on real datasets
 ┗ 📄 README.md
```

---

## 🔢 NumPy — Array Computing

**File:** `Numpy.ipynb`

### What I Learned & Practiced:
- ✅ Creating 1D and 2D NumPy arrays
- ✅ Difference between Python lists and NumPy arrays (element-wise math)
- ✅ Array indexing and slicing (`arr[0]`, `arr[1:5]`, `arr[::2]`)
- ✅ 2D array (matrix) indexing — `arr[row, col]`
- ✅ Array properties — `.shape`, `.size`, `.ndim`
- ✅ Mathematical operations — `+`, `-`, `*`, `/` between arrays
- ✅ Useful functions — `np.sum()`, `np.min()`, `np.max()`, `np.mean()`
- ✅ Special arrays — `np.ones()`, `np.zeros()`, `np.arange()`, `np.linspace()`
- ✅ Reshaping arrays — `.reshape(rows, cols)`

### Key Code Snippet:
```python
import numpy as np

a = np.array([1, 2, 3])
b = np.array([4, 5, 6])
print(a + b)       # [5 7 9]  ← element-wise, unlike Python lists!

arr = np.array([10,20,30,40,50,60])
b = arr.reshape(2, 3)  # convert 1D → 2D matrix
```

---

## 🐼 Pandas — Data Analysis

**File:** `Pandas.ipynb`

### What I Learned & Practiced:
- ✅ Creating `pd.Series` (1D) and `pd.DataFrame` (2D table)
- ✅ Built a real smartphone price dataset (10 brands)
- ✅ Exploring data — `.head()`, `.tail()`, `.info()`, `.describe()`
- ✅ Data cleaning — `.dropna()`, `.fillna()`, `.isnull().sum()`, `.drop_duplicates()`
- ✅ Filtering rows — `df[df['Price'] > 30000]`
- ✅ Grouping & aggregation — `.groupby('Brands')['Price'].mean()`
- ✅ Sorting — `.sort_values('Price', ascending=False)`
- ✅ Row selection — `.loc[]` (label-based) and `.iloc[]` (index-based)
- ✅ Column statistics — `.mean()`, `.max()`, `.min()`, `.sum()`

### Key Code Snippet:
```python
import pandas as pd

data = {
    'Brands': ["Apple","Vivo","Samsung","Realme","Oppo","Oneplus","Redmi","Poco","Google","Infinix"],
    'Price':  [30000, 25000, 28000, 15000, 22000, 35000, 12000, 18000, 31000, 21000]
}
df = pd.DataFrame(data)
df[df['Price'] > 30000]              # filter expensive phones
df.groupby('Brands')['Price'].mean() # average price per brand
```

---

## 📈 Matplotlib — Data Visualization

**File:** `Matplotlib.ipynb`

### What I Learned & Practiced:
- ✅ **Line Chart** — basic and multiple lines on one figure
- ✅ **Bar Chart** — vertical bars with custom colors, titles, axis labels
- ✅ **Horizontal Bar Chart** — `plt.barh()`
- ✅ **Pie Chart** — with percentage labels using `autopct`
- ✅ **Scatter Plot** — relationship between two variables
- ✅ **Histogram** — frequency distribution of data
- ✅ Chart customization — `linestyle`, `marker`, `color`, `label`
- ✅ Chart elements — `plt.title()`, `plt.xlabel()`, `plt.ylabel()`, `plt.legend()`, `plt.grid()`
- ✅ **Subplots** — multiple charts in one figure using `plt.subplot()`
- ✅ **Saving charts** — `plt.savefig("graph.png")`
- ✅ **Value labels on bars** — `plt.text()` loop to show numbers on top of bars

### Key Code Snippet:
```python
import matplotlib.pyplot as plt

fruits = ["Mango","Kiwi","Banana","Apple","Grapes","Orange"]
sales  = [10, 25, 30, 40, 50, 30]

bars = plt.bar(fruits, sales, color="green")

# Add value labels on top of each bar
for bar in bars:
    plt.text(bar.get_x() + bar.get_width()/2,
             bar.get_height() + 0.5,
             str(int(bar.get_height())),
             ha='center', fontweight='bold')

plt.title("My Chart")
plt.xlabel("Fruits")
plt.ylabel("Sales")
plt.show()
```

---

## 🌊 Seaborn — Statistical Visualization

**File:** `Seaborn.ipynb`

### What I Learned & Practiced:
- ✅ `sns.displot()` — distribution plots (histogram + KDE)
- ✅ `sns.histplot()` — histogram with KDE overlay
- ✅ `sns.countplot()` — count of categorical values
- ✅ `sns.barplot()` — bar chart with confidence intervals
- ✅ `sns.scatterplot()` — relationship between two numeric columns
- ✅ `sns.lineplot()` — trends over time / ordered categories
- ✅ `sns.boxplot()` — median, quartiles, and outliers
- ✅ `sns.violinplot()` — distribution shape across categories
- ✅ Used **real built-in datasets** — `tips` (restaurant data)
- ✅ Custom titles, figure sizes with `plt.figure(figsize=...)`
- ✅ KDE (Kernel Density Estimate) — smooth distribution curve

### Key Code Snippet:
```python
import seaborn as sns
import matplotlib.pyplot as plt

tips = sns.load_dataset("tips")   # real restaurant dataset

sns.violinplot(x="day", y="total_bill", data=tips)
plt.title("Bill Distribution by Day")
plt.show()
```

---

## 🛠️ Tech Stack

| Tool | Version | Purpose |
|------|---------|---------|
| Python | 3.x | Core language |
| NumPy | latest | Numerical computing |
| Pandas | latest | Data manipulation |
| Matplotlib | latest | Plotting & visualization |
| Seaborn | latest | Statistical visualization |
| Jupyter Notebook | latest | Interactive coding environment |

---

## 🚀 How to Run

```bash
# 1. Clone the repository
git clone https://github.com/YOUR_USERNAME/python-data-science-portfolio.git
cd python-data-science-portfolio

# 2. Install dependencies
pip install numpy pandas matplotlib seaborn jupyter

# 3. Launch Jupyter Notebook
jupyter notebook
```

Then open any `.ipynb` file and run cells with `Shift + Enter`.

---

## 📌 Topics Covered at a Glance

```
NumPy    → Arrays · Indexing · Slicing · Math · Reshape · Special arrays
Pandas   → Series · DataFrame · Clean · Filter · GroupBy · Sort · loc/iloc
Matplotlib → Line · Bar · Pie · Scatter · Histogram · Subplot · Customize
Seaborn  → Dist · Count · Bar · Scatter · Line · Box · Violin · KDE · Tips dataset
```

---

## 🎯 What's Next

- [ ] Add real-world CSV dataset projects
- [ ] Exploratory Data Analysis (EDA) on Kaggle datasets
- [ ] Plotly interactive charts
- [ ] Machine Learning with Scikit-learn

---

## 🤝 Connect With Me
---

⭐ **If this helped you, please give the repo a star!**
