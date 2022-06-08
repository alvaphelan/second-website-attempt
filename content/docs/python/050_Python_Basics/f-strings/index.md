---
title: Python formatted string literals (f-strings)
linktitle: f-strings
date: 2019-05-05
type: book
toc: true
---
# 

The latest and greatest way to format strings in Python


<!--more-->

{{< toc hide_on="xl" >}}


## Introduction

There are several ways to format strings in Python and the Python
community has recently
[introduced](https://www.python.org/dev/peps/pep-0498/) (in Python
3.6) f-strings, which are very easy to use and the preferred way to do
sting formatting now in Python. If you are familiar with Python's
`.format()` method to format strings then f-strings will be very
straightforward, as they follow the [Format Specification Mini-Language](https://docs.python.org/3.6/library/string.html#formatspec)

A comparison of the various Python string format methods can be found
[here](https://realpython.com/python-f-strings/) and a search for 'python f-string' wil reveal many online tutorials with examples.

The official Python documentation on f-strings can be found [here](https://docs.python.org/3/reference/lexical_analysis.html#f-strings)


## Basic usage
To make an f-string prepend the string with "f" or "F" and the refer to the variables within
the string between braces "{}".

It is probably easier to explain f-strings is probably by example:

### String Examples:
Here are some examples with strings:

```python
In [1]: name="Albert"

In [2]: f"My name is {name}!"         # assign to a variable
Out[2]: My name is Albert!

In [3]: announce = f"My name is {name}!"         # assign to a variable
In [4]: print(announce)                          # print variable
My name is Albert!

In [5]: print(f"My name is {name.upper()}!")   # use a function (convert to upper case)
My name is ALBERT!

In [6]: print(f"My name is {name:>*10}!")  # right-aligned, width 10, pad with "*"
My name is ****Albert!

In [7]: print(f"My name is {name.upper()} and it has {len(name)} characters!")
My name is ALBERT and it has 6 characters!
```

### Numeric Examples

Here are some examples with numbers:

```python

In [1]: import math
In [2]: pi=math.pi

In [3]: print(f"pi has the value {pi}")
pi has the value 3.141592653589793

In [4]: print(f"pi has the value {pi:.3f}")
pi has the value 3.142

# right aligned, 7 chars with 3 after decimal point, pad with spaces and then '0's
In [5]: print(f"pi has the value {pi:>7.3f} or {pi:>07.3f}")  
pi has the value   3.142 or 003.142

# do simple calculation
In [6]: theta=pi/4
In [7]: print(f"theta = {theta:.2f} radians = {theta/pi*180:.2f} degrees")
theta = 0.79 radians = 45.00 degrees

# number bases.
In [8]: x=77 
In [9]: print(f"x = {x} (decimal) = {x:08b} (binary)")                         
x = 77 (decimal) = 01001101 (binary)
```

## Self-documenting variables

Python 3.8 [introduced a new "=" operator](https://docs.python.org/3.8/whatsnew/3.8.html#f-strings-support-for-self-documenting-expressions-and-debugging) with f-strings to print the
name and value of a variable:

```python
In [1]: user="Albert Einstein"
In [2]: f"{user=}"
Out[2]: "user='Albert Einstein'"
```
Note: this is not yet available on the computers in the APL as they
have to been upgraded to Python 3.8.





