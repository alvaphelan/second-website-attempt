# Using Packages in Python 

While python is extremely useful on it's own, many packages can be used to help make life a bit easier. The main ones are explained below.

## Numpy

Numpy is an extremely useful library that lets python work with data at a high speed. You will be using it regularly throughout your code. First, you need to import the package at the start of your notebook.


```python
import numpy as np
```

One of the most important things numpy can do is import data, but this will be dealt with in it's own section here (*link*).

Arrays are a very useful aspect of numpy and are used widely. An array is just a grid of values and can be both 1 or 2 dimensional. 


```python
# example of 1 dimensional array
one_d = np.array([2, 4, 6, 8, 10])
# example of 2 dimensional array 
two_d = np.array([(1,3,5), (2,4,6)]) #(2x3 matrix in this case)
```

Numpy has a lot of tools to find out about arrays (very useful if dealing with long ones) and creating them!

#### Finding information about arrays

It is possible to find the size of an array by using the command 'np.size()', or you can use the pure python function 'len()'.



```python
print(np.size(one_d))
print(len(one_d))
```

    5
    5
    

However, you have to be careful with the 'len()' function, as for two dimensional arrays, it only returns the number of rows!



```python
print(np.size(two_d))
print(len(two_d))
```

    6
    2
    

It is possible to get certain elements of interest by the name of the array, followed by a square bracket surrounding the position of interest in an arry.
*note: the first element is always 0, not 1!*


```python
#to find the first and third element of the one d array
print(one_d[0])
print(one_d[2])
```

    2
    6
    

The same works for a two dimensional array, but remember to put in the full position!


```python
#to find the element in the first row, third column
print(two_d[0, 2])
```

    5
    

#### Creating arrays


##### Slicing
If creating a smaller array from a larger one that already exists, e.g. looking at a particular part of interest, slicing is a good way to do so. It works similarly to gettinga specific element, except in this case you put a ':' in between the first element of interest and the one after the last. (for example, [2:6] means the third element up to but not including the 7th element).

*note: simply putting [:] will return the original array, while [:4] will return all points up to but not inlcuding the fifth element and vice versa.


```python
#for example, to make a smaller array of the second, third and fourth 
#element of the one d array
sliced_array = one_d[1:5]
print(sliced_array)
```

    [ 4  6  8 10]
    

This also works for two dimensional arrays.


```python
# to get second row, all columns
print(two_d[1,:])
# to get all rows but second column
print(two_d[:,1])
```

    [2 4 6]
    [3 4]
    

##### Aranging
If creating an array from scratch, it is possible to make an evenly spaced out array where you customise the start point, end point and step size. 

*Be mindful, as in the slicing, it is up to but not including the end point*


```python
# for example to get from 1 to 5 in steps of 0.5
space = np.arange(1, 5.5, 0.5)
print(space)
```

    [1.  1.5 2.  2.5 3.  3.5 4.  4.5 5. ]
    

If you want to create an array but with a certain number of steps, rather than a step size, you can use the function 'linspace()' where you customise the start point, endpoint and number of steps


```python
# for example go from 1 to 10 in 5 steps
numbers = np.linspace(1,10,5)
print(numbers)
```

    [ 1.    3.25  5.5   7.75 10.  ]
    

##### Various Arrays

There are many numpy functions that can be used to create arrays. If looking to create one containing only 0's, you can use 'np.zeros()' and fill in the bracket with the length of the array you want, 'np.ones()' will do the same but fill with only 1's, 'np.eye(4)' will create a 4x4 identity matrix (fill with whatever square matrix is needed). 


```python

```
