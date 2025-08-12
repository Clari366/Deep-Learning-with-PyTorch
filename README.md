# PyTorch Basics Exercises

## AIM:
Write a Python program using PyTorch that performs the following tasks:

### Software Required:
- Python 3.x
- PyTorch
- Jupyter Notebook (for interactive development and execution)

## Algorithm:

### Step 1:
Perform standard imports
- Import `torch` and `NumPy`.

```python
import torch
import numpy as np
```

### Step 2:
Set the random seed for NumPy and PyTorch both to `42`.

```python
import numpy as np
import torch

np.random.seed(42) 
torch.manual_seed(42) 
```

### Step 3:
Create a NumPy array called `arr` that contains 6 random integers between 0 (inclusive) and 5 (exclusive).

```python
arr = np.random.randint(0, 5, size=6)

print(arr)
```

### Step 4:
Create a tensor `x` from the array above.

```python
x = torch.from_numpy(arr)

print(x)
```

### Step 5:
Change the dtype of `x` from `int32` to `int64`.

```python
x = x.type(torch.int64)

print(x)
print(x.dtype) 
```

### Step 6:
Reshape `x` into a `3x2` tensor.

```python
x = x.view(3, 2)   # or x.reshape(3, 2)

print(x)
```

### Step 7:
Return the right-hand column of tensor `x`.

```python
right_col = x[:, 1]

print(right_col)
```

### Step 8:
Without changing `x`, return a tensor of square values of `x`.

```python
squares = x ** 2   
```

### Step 9:
Create a tensor `y` with the same number of elements as `x`, that can be matrix-multiplied with `x`.
- Use PyTorch directly (not NumPy) to create a tensor of random integers between 0 (inclusive) and 5 (exclusive).

```python
y = torch.randint(0, 5, (2, 3))  # random integers [0, 5), shape (2, 3)

print(y)
print(y.shape) 
```

### Step 10:
Find the matrix product of `x` and `y`.

```python
product = torch.matmul(x, y)   # or x @ y

print(product)
```

## Output:
i) Import and set up PyTorch and NumPy.
ii) Create and manipulate tensors.
iii) Perform matrix operations.

## Result:
Thus, the PyTorch tensor operations, including reshaping, dtype conversion, and matrix multiplication, were successfully performed using the Python program.
