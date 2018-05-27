---
layout: post
title: "Data Structure - Array"
date: 2018-05-27
---

## Basic knowledge

An array is a collection of items stored at continuous memory locations. The idea is to store multiple items of same type together. Array is call by rank (position).

## Advantages

- Arrays allow random access of elements. This makes accessing elements by position faster.

## Array in C/C++

- Declaration

```cpp
// Array declaration by specifying size
int arr[10];
// Array declaration by initializing elements 
int arr[] = {10, 20, 30, 40}
// Array declaration by specifying size and initializing elements 
int arr[6] = {10, 20, 30, 40} // default 0
```
- Access elements: By an integer index. No index out of bound.

## Array in Python

No native array data structure. Use Python lists instead of an array. NumPy's array is real array.

### Python List
- Declaration

```py
arr = [10,20,30]
```

- Access elements: Positive and negative indexing.

- Others
	1. No need to be the same type
	2. List operations  `a1 *= 2` `a1 += 1` `a1 + a1`
	3. A slice of a list is a copy of that part of the list


### NumPy array
- Declaration

```py
import numpy as np
a1 = np.arange(5)
# create from a numeric iterable
a2 = np.array([3,4,5,6])
a3 = np.array((3.14,23.4))
# other methods
np.ones(2,3)
np.zeros(2,3)
np.empty(2,3) #allocated array of junk
np.eye(5)
np.identity(5)
no.random.randint(lo,hi,size = (M,N,P,...))
# specify the element type
all_int32 = np.ones(4,5,6,dtype = np.int32)
```

- Others
	1. does not store Python int values (e.g. numpy.int32) 
	2. A slice of an ndarray is a view. Use .copy().
	3. Matrix operation `np.dot(a,a.T) # inner product`
	4. Many other methods available in numpy.linalg `la.inv(a1)` `la.det(a1)` `la.solve(a1,b) # solve Ax = b`