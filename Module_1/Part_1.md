# 📘 Module 1 - NumPy Fundamentals

---

# What is NumPy?

## 📖 Introduction

Before learning NumPy, let's first understand why it was created.

Suppose you have marks of five students.

```python
marks = [85, 90, 78, 92, 88]
```

A Python List can easily store these values.

Now imagine you are working in a company like Google, Amazon, Microsoft, or Tesla where millions of records need to be processed every second.

Examples:

- Customer data
- Employee records
- Weather data
- AI datasets
- Medical reports
- Images
- Videos

A normal Python List can store the data, but it becomes slower when the data grows very large.

To solve this problem, Python provides **NumPy**.

---

## 📚 What is NumPy?

**NumPy (Numerical Python)** is a powerful Python library used for working with numbers and large amounts of data.

Instead of storing data inside Python Lists, NumPy stores data inside a special object called an **Array**.

NumPy performs calculations much faster than normal Python Lists.

It is one of the most important libraries used in:

- Artificial Intelligence (AI)
- Machine Learning (ML)
- Data Science
- Deep Learning
- Image Processing
- Scientific Computing
- Data Analysis

---

## ❓ Why Do We Need NumPy?

Let's understand this with a simple example.

Suppose your company stores the monthly salary of 10 lakh employees.

You want to give every employee a bonus of ₹5000.

Using Python Lists, you need to visit every salary one by one.

Using NumPy, the bonus can be added to all employees in a single operation.

This makes NumPy much faster and more efficient.

---

## 📝 Syntax

```python
import numpy as np
```

This imports the NumPy library.

`np` is just a short name (alias) used for NumPy.

---

# 🌍 Real-Life Example

### Company Salary Management System

Suppose a company has four employees.

Current Salaries

| Employee | Salary |
|----------|---------|
| Rahul | 25000 |
| Priya | 30000 |
| Arun | 45000 |
| Deepak | 50000 |

The company decides to increase everyone's salary by ₹5000.

---

## 🐍 Real-Time Python Example

```python
import numpy as np

salary = np.array([25000, 30000, 45000, 50000])

print("Current Salary:")
print(salary)

updated_salary = salary + 5000

print("\nUpdated Salary:")
print(updated_salary)
```

---

## ✅ Output

```text
Current Salary:
[25000 30000 45000 50000]

Updated Salary:
[30000 35000 50000 55000]
```

---

## 🔍 Step-by-Step Explanation

### Step 1

```python
import numpy as np
```

Imports the NumPy library.

---

### Step 2

```python
salary = np.array([25000,30000,45000,50000])
```

Creates a NumPy Array that stores employee salaries.

---

### Step 3

```python
updated_salary = salary + 5000
```

NumPy automatically adds ₹5000 to every employee's salary.

No loop is required.

---

### Step 4

```python
print(updated_salary)
```

Displays the updated salaries.

---

## 💡 Interview Tip

**Question**

What is NumPy?

**Answer**

NumPy is a Python library used for fast numerical computations. It stores data in arrays and performs mathematical operations much faster than Python Lists.

---

## 📌 Important Note

NumPy is mainly designed for numerical data.

If you want to work with large datasets containing numbers, NumPy is one of the best choices.

---

# Why NumPy?

## 📖 Explanation

Python Lists are very flexible.

They can store

- Numbers
- Strings
- Boolean values
- Objects

However, flexibility comes at the cost of speed.

When millions of calculations need to be performed, Python Lists become slower.

NumPy is specially designed to perform mathematical calculations very quickly.

---

## ❓ Why Do We Need NumPy?

Imagine you are working in a hospital.

The hospital stores the heart rate of one lakh patients.

Every heart rate needs to be increased by 2 after calibration.

Python List performs the operation one patient at a time.

NumPy performs the operation on the complete array together.

This saves both time and memory.

---

## 📝 Syntax

```python
import numpy as np

array_name = np.array(values)
```

---

# 🌍 Real-Life Example

### Hospital Heart Rate Monitoring System

Current Heart Rates

| Patient | Heart Rate |
|----------|------------|
| A | 72 |
| B | 68 |
| C | 75 |
| D | 70 |

After calibration, every value increases by 2.

---

## 🐍 Real-Time Python Example

```python
import numpy as np

heart_rate = np.array([72, 68, 75, 70])

print("Before Calibration")
print(heart_rate)

heart_rate = heart_rate + 2

print("\nAfter Calibration")
print(heart_rate)
```

---

## ✅ Output

```text
Before Calibration
[72 68 75 70]

After Calibration
[74 70 77 72]
```

---

## 🔍 Step-by-Step Explanation

The first line creates a NumPy array.

The second line prints the original heart rates.

The third line increases every value by 2.

Finally, the updated values are displayed.

---

## 💡 Interview Tip

**Question**

Why is NumPy preferred over Python Lists?

**Answer**

Because NumPy performs calculations faster, uses less memory, and supports vectorized mathematical operations.

---

## 📌 Important Note

Almost every Data Science and Machine Learning library like Pandas, Scikit-Learn, TensorFlow, and PyTorch internally works with NumPy arrays.

---

# Python List vs NumPy Array

## 📖 Explanation

Although both Python Lists and NumPy Arrays store data, they are designed for different purposes.

Python Lists are general-purpose containers.

NumPy Arrays are specially designed for numerical computations.

---

## 📊 Comparison Table

| Python List | NumPy Array |
|-------------|-------------|
| Slower for calculations | Faster calculations |
| Uses more memory | Uses less memory |
| Stores mixed data types | Usually stores same data type |
| Requires loops for calculations | Supports direct mathematical operations |
| Mainly used for general programming | Mainly used in AI, ML and Data Science |

---

## 🌍 Real-Life Example

Suppose a teacher wants to add 5 grace marks to every student.

### Using Python List

```python
marks = [80, 85, 90, 75]

updated_marks = []

for mark in marks:
    updated_marks.append(mark + 5)

print(updated_marks)
```

---

### Output

```text
[85, 90, 95, 80]
```

---

### Using NumPy

```python
import numpy as np

marks = np.array([80, 85, 90, 75])

updated_marks = marks + 5

print(updated_marks)
```

---

### Output

```text
[85 90 95 80]
```

---

## 🔍 Step-by-Step Explanation

Python List needs a loop.

NumPy does the calculation using a single statement.

This is called **Vectorized Operation**, which makes NumPy very fast.

---

## 💡 Interview Tip

If an interviewer asks,

**"Which is better: Python List or NumPy Array?"**

A good answer is:

- Python Lists are suitable for general-purpose programming.
- NumPy Arrays are better for mathematical operations and handling large numerical datasets efficiently.

---

## 📌 Important Note

For small datasets, the speed difference may not be noticeable.

For large datasets containing millions of values, NumPy performs significantly faster than Python Lists.
