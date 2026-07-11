---

# Advantages of NumPy

## 📖 Explanation

NumPy is one of the most powerful Python libraries because it makes working with numerical data **faster**, **easier**, and **more efficient**.

Instead of writing long loops to perform calculations, NumPy allows us to perform operations on the entire array using a single line of code.

This saves both **time** and **memory**.

---

## 🎯 Why Do We Need NumPy?

Imagine you are working in a company that stores the monthly sales of **5 lakh products**.

The company decides to increase the price of every product by ₹100.

Using Python Lists, you need to update each product one by one using a loop.

Using NumPy, the update happens in a single operation.

This is why companies working with huge datasets prefer NumPy.

---

# ⭐ Advantages of NumPy

## 1. Faster Execution

NumPy performs calculations much faster than Python Lists because it is internally written using the C programming language.

### Real-Life Example

Suppose an online shopping company wants to increase the prices of all products by ₹100.

### Python Example

```python
import numpy as np

prices = np.array([250, 400, 550, 800])

print("Old Prices")
print(prices)

new_prices = prices + 100

print("\nUpdated Prices")
print(new_prices)
```

### Output

```text
Old Prices
[250 400 550 800]

Updated Prices
[350 500 650 900]
```

### Explanation

NumPy automatically updates every value.

No loop is required.

---

## 2. Less Memory Usage

NumPy stores data more efficiently than Python Lists.

Because of this, it consumes less memory.

This becomes very useful when working with large datasets.

### Real-Life Example

Imagine a hospital storing the age of 20 lakh patients.

NumPy can store this data using less memory than Python Lists.

---

### Python Example

```python
import numpy as np

ages = np.array([21, 35, 42, 28, 30])

print(ages)
```

### Output

```text
[21 35 42 28 30]
```

---

## 3. Easy Mathematical Operations

One of the biggest advantages of NumPy is that mathematical calculations become very easy.

### Real-Life Example

A company gives every employee a ₹5000 salary increment.

### Python Example

```python
import numpy as np

salary = np.array([25000, 30000, 35000, 45000])

updated_salary = salary + 5000

print(updated_salary)
```

### Output

```text
[30000 35000 40000 50000]
```

---

## 4. Supports Multi-Dimensional Arrays

NumPy can store data in different dimensions.

- 1D Array
- 2D Array
- 3D Array

This makes it useful for

- Student databases
- Images
- Videos
- Medical reports
- AI datasets

---

## 5. Used in Artificial Intelligence and Machine Learning

Almost every AI and Data Science library uses NumPy internally.

Examples include:

- Pandas
- TensorFlow
- PyTorch
- Scikit-learn
- OpenCV
- SciPy

Learning NumPy makes it much easier to learn these libraries.

---

## 💡 Interview Tip

**Question**

What are the advantages of NumPy?

**Answer**

- Faster calculations
- Uses less memory
- Easy mathematical operations
- Supports multidimensional arrays
- Widely used in AI, Machine Learning, and Data Science

---

## 📌 Important Note

If your program involves numbers, calculations, statistics, or machine learning, NumPy is almost always a better choice than Python Lists.

---

# Installing NumPy

## 📖 Explanation

Before using NumPy, we need to install it.

Python does not include NumPy by default.

We install it using the **pip** package manager.

---

## ❓ Why Do We Need to Install NumPy?

Think of Python as a mobile phone.

The phone comes with some basic applications.

If you want WhatsApp, Instagram, or YouTube, you need to install them separately.

Similarly, NumPy is an external Python library.

We install it before using it.

---

## 📝 Syntax

Open **Command Prompt**, **Terminal**, or **PowerShell** and type:

```bash
pip install numpy
```

---

## 🖥 Example

```bash
pip install numpy
```

### Output

```text
Collecting numpy
Installing collected packages: numpy
Successfully installed numpy
```

If NumPy is already installed, you may see:

```text
Requirement already satisfied: numpy
```

This means NumPy is already available on your computer.

---

## 💡 Interview Tip

**Question**

How do you install NumPy?

**Answer**

```bash
pip install numpy
```

---

## 📌 Important Note

Always install packages using **pip** in your project's Python environment.

---

# Importing NumPy

## 📖 Explanation

After installing NumPy, we need to import it into our Python program.

Without importing, Python will not recognize NumPy functions.

---

## ❓ Why Do We Import NumPy as `np`?

Instead of writing

```python
numpy.array()
```

every time, programmers use a shorter name.

```python
import numpy as np
```

Here,

- `numpy` → Original library name
- `np` → Alias (short name)

This makes the code shorter and easier to read.

---

## 📝 Syntax

```python
import numpy as np
```

---

## 🌍 Real-Life Example

Suppose a company stores monthly sales.

```python
import numpy as np

sales = np.array([12000, 18000, 22000, 15000])

print(sales)
```

---

## ✅ Output

```text
[12000 18000 22000 15000]
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
sales = np.array([...])
```

Creates a NumPy Array.

---

### Step 3

```python
print(sales)
```

Displays the array.

---

## 💡 Interview Tip

**Question**

Why do we write

```python
import numpy as np
```

instead of

```python
import numpy
```

**Answer**

Because `np` is a commonly used alias that makes the code shorter, cleaner, and easier to read.

---

## 📌 Important Note

Although you can use any alias, almost every Python developer uses **np**.

Using the standard alias improves code readability.

---

# Checking NumPy Version

## 📖 Explanation

Every software gets updated over time.

Similarly, NumPy has different versions.

Sometimes a feature works only in a specific version.

So, it is good practice to check which version of NumPy is installed.

---

## 📝 Syntax

```python
import numpy as np

print(np.__version__)
```

---

## 🌍 Real-Life Example

Suppose you are working on a team project.

Before running the code, your team leader asks everyone to verify that they are using the same NumPy version.

```python
import numpy as np

print("Installed NumPy Version:")
print(np.__version__)
```

---

## ✅ Output

```text
Installed NumPy Version:
2.3.1
```

> **Note:** Your version number may be different depending on when you installed NumPy.

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
print(np.__version__)
```

Displays the installed version of NumPy.

---

## 💡 Interview Tip

**Question**

How do you check the installed version of NumPy?

**Answer**

```python
import numpy as np

print(np.__version__)
```

---

## 📌 Important Note

Always verify the NumPy version when following tutorials, debugging code, or collaborating on projects to avoid compatibility issues.

---

# ✅ Module 1 Summary

| Topic | Description |
|--------|-------------|
| What is NumPy? | A Python library for fast numerical computing |
| Why NumPy? | Faster calculations and efficient memory usage |
| Python List vs NumPy Array | NumPy is optimized for numerical operations |
| Advantages | Faster, memory-efficient, supports multidimensional arrays, widely used in AI & ML |
| Installing NumPy | `pip install numpy` |
| Importing NumPy | `import numpy as np` |
| Checking Version | `print(np.__version__)` |

---
