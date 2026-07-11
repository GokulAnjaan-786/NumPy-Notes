# 📗 Module 2 - Creating NumPy Arrays

---

# Introduction

Before performing calculations using NumPy, we first need to **create arrays**.

An array is the heart of NumPy.

Just like a Python List stores multiple values, a NumPy Array also stores multiple values. The difference is that NumPy Arrays are designed specifically for **fast numerical calculations**.

There are many ways to create arrays in NumPy.

In this module, we'll learn all the commonly used methods.

---

# Creating Arrays from List

## 📖 Explanation

The easiest way to create a NumPy Array is by converting a Python List.

Since most beginners already know Python Lists, NumPy allows us to convert a list into an array using **np.array()**.

---

## ❓ Why Do We Need It?

Suppose a teacher stores student marks in a Python List.

Later, she wants to calculate

- Total Marks
- Average Marks
- Highest Marks

NumPy makes these calculations much easier and faster.

---

## 📝 Syntax

```python
import numpy as np

array_name = np.array(list_name)
```

---

## 🌍 Real-Life Example

A teacher stores marks in a Python List.

```python
import numpy as np

marks = [85, 90, 78, 92, 88]

marks_array = np.array(marks)

print(marks_array)
```

---

## ✅ Output

```text
[85 90 78 92 88]
```

---

## 💡 Explanation

- `marks` is a Python List.
- `np.array()` converts the list into a NumPy Array.
- Now mathematical operations become much easier.

---

## 🎯 Interview Tip

**Question**

How do you convert a Python List into a NumPy Array?

**Answer**

```python
arr = np.array(list_name)
```

---

## 📌 Important Note

The original Python List remains unchanged.

Only a new NumPy Array is created.

---

# Creating Arrays from Tuple

## 📖 Explanation

NumPy can also convert Python Tuples into Arrays.

---

## ❓ Why Do We Need It?

Sometimes data is stored as a Tuple because Tuples cannot be modified.

When mathematical calculations are needed, we convert the Tuple into a NumPy Array.

---

## 📝 Syntax

```python
array_name = np.array(tuple_name)
```

---

## 🌍 Real-Life Example

Suppose a company stores monthly sales in a Tuple.

```python
import numpy as np

sales = (12000, 18000, 22000, 15000)

sales_array = np.array(sales)

print(sales_array)
```

---

## ✅ Output

```text
[12000 18000 22000 15000]
```

---

## 💡 Explanation

NumPy converts the Tuple into an Array.

Now we can perform mathematical operations easily.

---

## 🎯 Interview Tip

NumPy accepts both **Lists** and **Tuples** inside `np.array()`.

---

## 📌 Important Note

Whether you pass a List or a Tuple, the result is always a NumPy Array.

---

# Creating 1D Arrays

## 📖 Explanation

A **1D Array** stores data in a single row.

It is similar to a normal Python List.

---

## 🌍 Real-Life Example

Daily temperatures of one week.

| Day | Temperature |
|------|-------------|
| Monday | 31 |
| Tuesday | 32 |
| Wednesday | 33 |
| Thursday | 30 |
| Friday | 34 |

---

## 📝 Syntax

```python
array_name = np.array([values])
```

---

## 🐍 Python Example

```python
import numpy as np

temperature = np.array([31, 32, 33, 30, 34])

print(temperature)
```

---

## ✅ Output

```text
[31 32 33 30 34]
```

---

## 💡 Explanation

All values are stored in one row.

This is called a One-Dimensional Array.

---

## 🎯 Interview Tip

A 1D Array has only **one axis**.

---

## 📌 Important Note

Use 1D Arrays when storing

- Student Marks
- Daily Expenses
- Temperatures
- Product Prices

---

# Creating 2D Arrays

## 📖 Explanation

A **2D Array** contains both **rows** and **columns**.

It looks like an Excel sheet.

---

## 🌍 Real-Life Example

Student Marks

| Student | Maths | Science | English |
|----------|--------|----------|----------|
| Rahul | 85 | 90 | 80 |
| Priya | 88 | 92 | 81 |
| Arun | 79 | 87 | 95 |

---

## 📝 Syntax

```python
array_name = np.array([
    [row1],
    [row2]
])
```

---

## 🐍 Python Example

```python
import numpy as np

marks = np.array([
    [85, 90, 80],
    [88, 92, 81],
    [79, 87, 95]
])

print(marks)
```

---

## ✅ Output

```text
[[85 90 80]
 [88 92 81]
 [79 87 95]]
```

---

## 💡 Explanation

Each row represents one student.

Each column represents one subject.

---

## 🎯 Interview Tip

A 2D Array contains **Rows × Columns**.

---

## 📌 Important Note

Most datasets used in Machine Learning are stored as 2D Arrays.

---

# Creating 3D Arrays

## 📖 Explanation

A **3D Array** is a collection of multiple 2D Arrays.

Think of it as stacking multiple Excel sheets.

---

## 🌍 Real-Life Example

A school has marks of Class A and Class B.

Each class has two students.

Each student has marks in two subjects.

---

## 📝 Syntax

```python
array_name = np.array([
    [
        [values],
        [values]
    ],
    [
        [values],
        [values]
    ]
])
```

---

## 🐍 Python Example

```python
import numpy as np

school = np.array([
    [
        [85, 90],
        [88, 92]
    ],
    [
        [79, 87],
        [91, 94]
    ]
])

print(school)
```

---

## ✅ Output

```text
[[[85 90]
  [88 92]]

 [[79 87]
  [91 94]]]
```

---

## 💡 Explanation

First block → Class A

Second block → Class B

Each row → Student

Each column → Subject

---

## 🎯 Interview Tip

Images, Videos, MRI Scans, and AI datasets are commonly stored using multidimensional arrays.

---

## 📌 Important Note

A color image is usually stored as a 3D Array because it contains

- Height
- Width
- Color Channels (Red, Green, Blue)

---

# np.array()

## 📖 Explanation

`np.array()` is the most commonly used function in NumPy.

It converts Python Lists or Tuples into NumPy Arrays.

Almost every NumPy program starts with this function.

---

## 📝 Syntax

```python
np.array(object)
```

Where **object** can be

- List
- Tuple
- Nested List
- Nested Tuple

---

## 🌍 Real-Life Example

Suppose an online shopping company stores product prices in a Python List.

Later, they want to increase every price by ₹100.

---

## 🐍 Python Example

```python
import numpy as np

prices = np.array([250, 400, 550, 800])

print("Old Prices")
print(prices)

updated_prices = prices + 100

print("\nUpdated Prices")
print(updated_prices)
```

---

## ✅ Output

```text
Old Prices
[250 400 550 800]

Updated Prices
[350 500 650 900]
```

---

## 💡 Explanation

`np.array()` creates a NumPy Array.

Since NumPy supports vectorized operations, adding `100` updates every element automatically.

---

## 🎯 Interview Tip

`np.array()` is the foundation of NumPy.

Almost every array in NumPy is created using this function directly or indirectly.

---

## 📌 Important Note

`np.array()` can create

- 1D Arrays
- 2D Arrays
- 3D Arrays

depending on the input provided.

---
