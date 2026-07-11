# 📘 Module 3 - Array Generation Functions (Part 1)

---

# Introduction

In Module 2, we learned how to create arrays using:

- np.array()
- np.zeros()
- np.ones()
- np.full()
- np.eye()
- np.identity()

These functions create arrays when we already know the values.

But in real-world projects, we don't always type every value manually.

Sometimes we need to generate numbers automatically.

For example,

- Employee IDs
- Student Roll Numbers
- Temperature Values
- Time Intervals
- Random OTP Numbers
- AI Training Data

NumPy provides special functions to generate these arrays automatically.

In this module, we'll learn those functions.

---

# np.arange()

## 📖 What is np.arange()?

`np.arange()` creates an array containing numbers within a given range.

It works similar to Python's built-in `range()` function.

The difference is

- `range()` returns a range object.
- `np.arange()` returns a NumPy Array.

---

## ❓ Why Do We Need It?

Imagine a company wants to generate Employee IDs.

Instead of typing

```python
[1001,1002,1003,1004,1005]
```

NumPy can generate them automatically.

---

## 📝 Syntax

```python
np.arange(start, stop, step)
```

| Parameter | Meaning |
|-----------|----------|
| start | Starting number |
| stop | Ending number (not included) |
| step | Difference between numbers |

---

## 🌍 Real-Life Example

### Employee ID Generator

A company wants employee IDs from 1001 to 1010.

---

## 🐍 Python Program

```python
import numpy as np

employee_ids = np.arange(1001, 1011)

print("Employee IDs")
print(employee_ids)
```

---

## ✅ Output

```text
Employee IDs

[1001 1002 1003 1004 1005 1006 1007 1008 1009 1010]
```

---

## 💡 Explanation

NumPy automatically generated employee IDs.

No need to type every value manually.

---

## Another Example

Suppose a parking area has only even-number parking slots.

```python
import numpy as np

parking_slots = np.arange(2, 22, 2)

print(parking_slots)
```

---

## Output

```text
[ 2  4  6  8 10 12 14 16 18 20]
```

---

## 🎯 Interview Tip

Difference between Python range() and np.arange()

| range() | np.arange() |
|-----------|------------|
| Returns range object | Returns NumPy Array |
| Used in loops | Used in numerical calculations |

---

## 📌 Important Note

The stop value is **never included**.

```python
np.arange(1,6)
```

Output

```text
[1 2 3 4 5]
```

---

# np.linspace()

## 📖 What is np.linspace()?

`np.linspace()` creates evenly spaced numbers between two values.

Instead of telling NumPy the **step size**, we tell it **how many values we need**.

---

## ❓ Why Do We Need It?

Suppose an air conditioner company wants to test temperatures between

20°C

and

40°C

They need exactly

10 temperatures.

Instead of calculating manually,

NumPy generates them automatically.

---

## 📝 Syntax

```python
np.linspace(start, stop, number_of_values)
```

---

## 🌍 Real-Life Example

### Temperature Testing

Generate 10 temperatures between 20°C and 40°C.

---

## 🐍 Python Program

```python
import numpy as np

temperature = np.linspace(20,40,10)

print(temperature)
```

---

## ✅ Output

```text
[20.
22.22222222
24.44444444
26.66666667
28.88888889
31.11111111
33.33333333
35.55555556
37.77777778
40.]
```

---

## 💡 Explanation

NumPy divided the complete range into

10 equal parts.

---

## Another Example

Suppose a road is

100 meters long.

Sensors need to be placed at

5 equal distances.

```python
import numpy as np

sensor_position = np.linspace(0,100,5)

print(sensor_position)
```

---

## Output

```text
[  0.  25.  50.  75. 100.]
```

---

## 🎯 Interview Tip

Difference between np.arange() and np.linspace()

| np.arange() | np.linspace() |
|--------------|---------------|
| We specify the step size | We specify the number of values |
| Stop value usually excluded | Stop value included |

---

## 📌 Important Note

`np.linspace()` includes both the start and stop values.

---

# np.logspace()

## 📖 What is np.logspace()?

`np.logspace()` generates numbers based on powers of 10.

Instead of increasing normally,

the numbers increase exponentially.

---

## ❓ Why Do We Need It?

Many scientific calculations use exponential values.

Examples

- Earthquake Magnitude
- Sound Intensity
- Radio Signals
- AI Learning Rates

---

## 📝 Syntax

```python
np.logspace(start_power, stop_power, number_of_values)
```

---

## 🌍 Real-Life Example

Suppose an AI Engineer wants to test different learning rates.

Learning rates

```
0.001

0.01

0.1

1

10
```

These are logarithmic values.

---

## 🐍 Python Program

```python
import numpy as np

learning_rate = np.logspace(-3,1,5)

print(learning_rate)
```

---

## ✅ Output

```text
[1.e-03
1.e-02
1.e-01
1.e+00
1.e+01]
```

---

## 💡 Explanation

NumPy generated

```
10⁻³

10⁻²

10⁻¹

10⁰

10¹
```

which become

```
0.001

0.01

0.1

1

10
```

---

## Another Example

Suppose a scientist wants to test light intensity.

```python
import numpy as np

intensity = np.logspace(1,4,4)

print(intensity)
```

---

## Output

```text
[   10.
   100.
  1000.
 10000.]
```

---

## 🎯 Interview Tip

Use

- np.arange()

for normal counting.

Use

- np.linspace()

for equal spacing.

Use

- np.logspace()

for exponential values.

---

## 📌 Important Note

`np.logspace()` is mostly used in

- Artificial Intelligence
- Machine Learning
- Scientific Computing
- Signal Processing
- Physics

---

# 📊 Comparison

| Function | Best Used For |
|-----------|---------------|
| np.arange() | Sequential numbers |
| np.linspace() | Equal spacing |
| np.logspace() | Exponential values |

---

# 💻 Intermediate Program

## Smart Factory Machine Testing

A factory tests machines at different speed levels.

```python
import numpy as np

machine_ids = np.arange(101,111)

temperature = np.linspace(25,45,10)

power_level = np.logspace(1,2,10)

print("Machine IDs")
print(machine_ids)

print("\nTemperature")
print(temperature)

print("\nPower Level")
print(power_level)
```

---

## Output

```text
Machine IDs
[101 102 103 104 105 106 107 108 109 110]

Temperature
[25.         27.22222222 29.44444444 31.66666667
33.88888889 36.11111111 38.33333333 40.55555556
42.77777778 45.        ]

Power Level
[ 10.
 12.91549665
 16.68100537
 21.5443469
 27.82559402
 35.93813664
 46.41588834
 59.94842503
 77.42636827
100.        ]
```

---

# 🎉 Part 1 Completed

You have learned

- ✅ np.arange()
- ✅ np.linspace()
- ✅ np.logspace()

These three functions are widely used in

- AI
- Machine Learning
- Data Science
- Scientific Computing
- Data Analysis
