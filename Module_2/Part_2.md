---

# np.zeros()

## 📖 Explanation

`np.zeros()` creates a NumPy Array filled with **0**.

Instead of typing many zeros manually, NumPy creates them automatically.

---

## ❓ Why Do We Need It?

Suppose a cricket match is about to start.

Every player's score is initially **0**.

Instead of writing

```python
[0, 0, 0, 0, 0, 0]
```

we can simply use `np.zeros()`.

---

## 📝 Syntax

```python
np.zeros(shape)
```

---

## 🌍 Real-Life Example

Cricket Scoreboard

```python
import numpy as np

players_score = np.zeros(5)

print(players_score)
```

---

## ✅ Output

```text
[0. 0. 0. 0. 0.]
```

---

## 💡 Explanation

NumPy created five elements.

Every element contains **0**.

---

## 🎯 Interview Tip

`np.zeros()` is commonly used to initialize arrays before storing actual values.

---

## 📌 Important Note

By default, `np.zeros()` creates **floating-point numbers**.

---

# np.ones()

## 📖 Explanation

`np.ones()` creates an array filled entirely with **1**.

---

## ❓ Why Do We Need It?

Suppose a company wants to mark all employees as **Active**.

Here,

- Active = 1
- Inactive = 0

Instead of writing many ones manually, we use `np.ones()`.

---

## 📝 Syntax

```python
np.ones(shape)
```

---

## 🌍 Real-Life Example

```python
import numpy as np

employee_status = np.ones(5)

print(employee_status)
```

---

## ✅ Output

```text
[1. 1. 1. 1. 1.]
```

---

## 💡 Explanation

NumPy created five elements.

Every element contains **1**.

---

## 🎯 Interview Tip

`np.ones()` is useful for creating default values.

---

## 📌 Important Note

Like `np.zeros()`, it also creates floating-point values by default.

---

# np.empty()

## 📖 Explanation

`np.empty()` creates an array without assigning any initial values.

The values are whatever already existed in that memory location.

---

## ❓ Why Do We Need It?

When we know that we are going to replace every value immediately, `np.empty()` is slightly faster than filling the array with zeros or ones.

---

## 📝 Syntax

```python
np.empty(shape)
```

---

## 🌍 Real-Life Example

Suppose a company creates space for storing employee IDs.

The IDs are not entered yet.

```python
import numpy as np

employee_ids = np.empty(5)

print(employee_ids)
```

---

## ✅ Output

```text
[6.91e-310 0.00e+000 4.67e-310 0.00e+000 6.91e-310]
```

> **Note:** Your output will be different every time.

---

## 💡 Explanation

Memory is allocated.

Values are **not initialized**.

---

## 🎯 Interview Tip

Never depend on the values returned by `np.empty()`.

Always overwrite them before using.

---

## 📌 Important Note

Use `np.empty()` only when you will assign values immediately.

---

# np.full()

## 📖 Explanation

`np.full()` creates an array where **every element contains the same value**.

---

## ❓ Why Do We Need It?

Suppose every employee receives a ₹5000 festival bonus.

Instead of writing

```python
[5000,5000,5000,5000]
```

we can use `np.full()`.

---

## 📝 Syntax

```python
np.full(shape, value)
```

---

## 🌍 Real-Life Example

```python
import numpy as np

bonus = np.full(5,5000)

print(bonus)
```

---

## ✅ Output

```text
[5000 5000 5000 5000 5000]
```

---

## 💡 Explanation

NumPy created five elements.

Every element stores **5000**.

---

## 🎯 Interview Tip

`np.full()` is useful whenever every value starts with the same number.

---

## 📌 Important Note

You can use any value.

```python
np.full(4,100)

np.full(3,-5)

np.full(5,3.14)
```

---

# np.eye()

## 📖 Explanation

`np.eye()` creates an **Identity Matrix**.

An Identity Matrix contains

- 1 on the main diagonal
- 0 everywhere else

---

## 📝 Syntax

```python
np.eye(n)
```

---

## 🌍 Real-Life Example

Imagine a classroom.

Every student matches only with their own ID card.

```
Student 1 ✔

Student 2 ✔

Student 3 ✔
```

This is similar to an Identity Matrix.

---

## 🐍 Python Example

```python
import numpy as np

identity = np.eye(3)

print(identity)
```

---

## ✅ Output

```text
[[1. 0. 0.]
 [0. 1. 0.]
 [0. 0. 1.]]
```

---

## 💡 Explanation

The diagonal contains 1.

Everything else is 0.

---

## 🎯 Interview Tip

Identity Matrices are widely used in

- Machine Learning
- Linear Algebra
- Image Processing

---

## 📌 Important Note

`np.eye()` can also create **rectangular identity-like matrices**.

Example

```python
np.eye(3,5)
```

---

# np.identity()

## 📖 Explanation

`np.identity()` also creates an Identity Matrix.

The only difference is that it always creates a **square matrix**.

---

## 📝 Syntax

```python
np.identity(n)
```

---

## 🌍 Real-Life Example

```python
import numpy as np

matrix = np.identity(4)

print(matrix)
```

---

## ✅ Output

```text
[[1. 0. 0. 0.]
 [0. 1. 0. 0.]
 [0. 0. 1. 0.]
 [0. 0. 0. 1.]]
```

---

## 💡 Explanation

The number of rows and columns is always the same.

---

## 🎯 Interview Tip

**Difference**

`np.eye()` → Can create rectangular matrices.

`np.identity()` → Always creates square matrices.

---

## 📌 Important Note

Most beginners use either function for square identity matrices.

---

# 📊 Module 2 Summary

| Function | Purpose |
|----------|----------|
| `np.array()` | Creates an array from a list or tuple |
| `np.zeros()` | Creates an array filled with 0 |
| `np.ones()` | Creates an array filled with 1 |
| `np.empty()` | Creates an array without initializing values |
| `np.full()` | Creates an array filled with a specified value |
| `np.eye()` | Creates an identity matrix (supports rectangular matrices) |
| `np.identity()` | Creates a square identity matrix |

---

# 💻 Intermediate Program 1 – Student Result Management System

```python
import numpy as np

students = np.array([
    [85, 90, 80],
    [78, 82, 88],
    [91, 95, 93]
])

print("Student Marks")
print(students)

print("\nTotal Marks")
print(np.sum(students, axis=1))
```

### Output

```text
Student Marks
[[85 90 80]
 [78 82 88]
 [91 95 93]]

Total Marks
[255 248 279]
```

---

# 💻 Intermediate Program 2 – Employee Bonus System

```python
import numpy as np

salary = np.array([25000,30000,35000,45000])

bonus = np.full(4,5000)

final_salary = salary + bonus

print(final_salary)
```

### Output

```text
[30000 35000 40000 50000]
```

---

# 💻 Intermediate Program 3 – Cricket Scoreboard

```python
import numpy as np

players = np.array(["Virat","Rohit","Gill","Surya"])

score = np.zeros(4)

score[0] = 78
score[1] = 65
score[2] = 102
score[3] = 45

print(players)
print(score)
```

### Output

```text
['Virat' 'Rohit' 'Gill' 'Surya']

[ 78.  65. 102.  45.]
```

---

# 🎉 Congratulations!

You have successfully completed:

- ✅ Module 1 – NumPy Fundamentals
- ✅ Module 2 – Creating NumPy Arrays

You are now ready to learn **Module 3 – Array Attributes**, where you'll explore:

- `ndim`
- `shape`
- `size`
- `dtype`
- `itemsize`
- `nbytes`
- `astype()`

These concepts will help you understand the internal structure of NumPy arrays and are frequently asked in interviews.
