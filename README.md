# BONGANAY-PA-2
## Programming Assignment #2 
Programming Assignment #2
Bonganay, Hannah - 2ECE-B
```bash
pip install numpy
```

### 1.) NORMALIZATION PROBLEM
To create a random 5 x 5 ndarray and store it to variable X. Normalize X. 

##### 1. Import numpy
```python 
import numpy as np
```
##### 2. Create a random 5x5 array. And in my example, I used the number 6 for the seed.
```python 
np.random.seed(6)
X = np.random.rand(5,5)
```
##### 3. Get mean and standard deviation.
```python 
meanvalue = X.mean()
stdvalue = X.std()
```
##### 4. Normalize the array by subtracting the mean and divide by the std for every element.
```python
Z = (X-meanvalue)/stdvalue
```
##### 4. Print results
```python
print("MEAN:", meanvalue)
print("STANDARD DEVIATION:", stdvalue)
print(" ")
print("X:")
print(X)
print(" ")
print("NORMALIZED:")
print(Z)
```
##### 5. Save your normalized ndarray as X_normalized.npy. This creates an npy file for it in the directory.
```python
np.save("X_normalized.npy", Z)
```

### 2.) DIVISIBLE BY 3 MATRIX
To create the following 10 x 10 ndarray which are the squares of the first 100 positive integers. 
From this ndarray, determine all the elements that are divisible by 3.

##### 1. Import numpy
```python 
import numpy as np
```
##### 2. Generate the numbers and the squares, using np.arange(1,101) for numbers 1–100.
```python 
dnumbers = np.arange(1,101)
squares = numbers**2
```
##### 3. Reshape the 1D array into 10 rows by 10 columns.
```python
A = squares.reshape(10,10)
```
##### 4. Select the elements divisible by 3 using a boolean mask.
```python
divideby3 = A[A%3==0]
```
##### 5. Print both of tthe results
```python
print("MATRIX A SQUARES")
print(A)
print(" ")
print("SQUARES DIVISIBLE BY 3:")
print(divideby3)
```
##### 6. Save the result as div_by_3.npy which contains only the divisible numbers.
```python
np.save("div_by_3.npy", divideby3)
```
