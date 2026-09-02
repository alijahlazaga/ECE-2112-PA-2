# ECE-2112-PA-2

**Made by: Alijah B. Lazaga | 2ECE-B**

The content of this repository contains the Programming Assignment for the course "Advance Computer Programming" this S.Y. 2026-2027

Note: Before coding, put `import numpy as np` in order to import the Numerical Python library and rename it to np. This way, np will act as an acronym for numpy, shortening it so that we won't have to code numpy before every function.

# **A. Reproducible Normalization Problem**

Create a reproducible random 5x5 array named X. Normalize the array using the Z-Score formula.

The following functions and methods were used in this problem:

• `np.random.seed(2112)`- Acts as a starting point for generating randomized numbers for the array we are about to create. The number inside the parenthesis is a unique number that retrieves a set of randomized numbers.

• `np.random.randint(10, 101, size=(5, 5))` - Generates random integers in a specific starting point and end point,(10, 101). Python starts generating from 10 until 101, the 101 excluded. We have also indicated the size of the array, having 5 rows and 5 columns.

• `X =`- A python statement that names the 5 x 5 array we created as X. 

• `X.mean()` - A built-in function that calculates the arithmetic average or mean of array X. It calculates the sum of the elements inside the array and divides it by the total number of elements.

• `X.std()` - A built-in function that calculates the standard deviation of array X using the calculated mean.

• `X_normalized = (X - X.mean())/X.std()` - A python statement that normalizes the array X using the Z-score formula, it then renames the array into X_normalized.

We will then calculate the mean and standard deviation of array X_normalized before saving the array with `np.save("X_normalized.npy, X_normalized)`. By combining all of the code shown above, the final code for this problem is as follows:

```python
import numpy as np
np.random.seed(2112)
X = np.random.randint(10, 101, size=(5, 5))

X.mean()
X.std()

X_normalized = (X - X.mean())/X.std()
  X_normalized.mean()
  X_normalized.std()

np.save("X_normalized.npy", X_normalized)
```

# **B. Cubes Divisible by 4 Problem**

Using NumPy, create the first 100 positive integers, cube every element, and reshape the result into a 10 × 10 ndarray named C. Thus, C begins with 1^3 and ends with 100^3.

The following functions and methods were used in this problem:

• `np.arange(1, 101)` - Generates a 1 dimensional array with numbers starting from 1 until 101, the 101 excluded.

• `** 3` - A python statement that can be used to cube each element in an array.

• `.reshape` - A built-in function that reshapes an array to a specific number of rows and columns.

We then rename the array created as div_by_4. After renaming the array from C to div_by_4. We create the statement `C[C % 4 == 0]`, keeping elements that are divisible by 4. The % is a modulo operation wherein it returns the remainder of a division. We placed 2 equal signs and a zero to get elements that are truly divisible by 4.

• `np.save("div_by_4.npy", div_by_4)` - A built-in function that saves the array into an .npy file.

By combining all of the code shown above, the final code for this problem is as follows:

```python
N = np.arange(1, 101)
  C = (N ** 3).reshape(10, 10)

div_by_4 = C[C % 4 ==0]
  np.save("div_by_4.npy", div_by_4)
```

# **C. Above-mean Squares Problem**

Create a 6 × 6 ndarray named S containing the squares of the first 36 positive integers in increasing row-major order. Compute the mean of all elements of S and store it in S mean. Then use Boolean filtering to select only the elements strictly greater than S mean. 

The following functions and methods were used in this problem:

• `np.arange(1, 37)` - A built-in function that generates an array with integers that start from 1 and ends at 37. The 37 is excluded from the created array.

• `np.reshape(6, 6)` - A built-in function that reshapes the array's layout into 6 rows and 6 columns.

We can then shorten the lines of code into one line `--> `S = (np.arange(1, 37)** 2).reshape(6, 6) 
Note that we squared the elements inside the area using the statement `** 2`.

• `S_mean = S.mean()` - A built-in function that calculates the arithmetic average or mean of array S whilst renaming it S_mean.

• `above_mean =  S[S > S_mean]` - A python statement that uses boolean indexing to remove all false values, which are the elements below S_mean, keeping elements that are above the mean. We rename this array as above_mean. 

• `np.save("above_mean.npy", above_mean)` - A built-in function that saves the array into an .npy file.

By combining all of the code, the final code for this problem is as follows:

```python
S = (np.arange(1, 37)** 2).reshape(6, 6)
  S_mean = S.mean()

above_mean = S[S > S_mean]
np.save("above_mean.npy", above_mean)
```

You can use the following functions to check the number of elements and the rows and columns:

• `.shape` - Checks the number of rows and columns in an array.

• `.size` - Checks the number of elements inside the array.

Thank you for reading!!!

To fully see the main python program, please visit the link provided below:
https://github.com/alijahlazaga/ECE-2112-PA-2/blob/3af07ca4c4d2ecd3bc3ff9c572d8c0863223c0c3/ProgrammingAssignment2.ipynb

### **README file Version History:**

September 1, 2026 - initial README content uploaded

September 2, 2026 - Final README content uploaded





