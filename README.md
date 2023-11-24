# Linear Search and Binary search
## Aim:
To write a program to perform linear search and binary search using python programming.
## Equipment’s required:
1.	Hardware – PCs
2.	Anaconda – Python 3.7 Installation / Moodle-Code Runner
## Algorithm:
## Linear Search:
1.	Start from the leftmost element of array[] and compare k with each element of array[] one by one.
2.	If k matches with an element in array[] , return the index.
3.	If k doesn’t match with any of elements in array[], return -1 or element not found.
## Binary Search:
1.	Set two pointers low and high at the lowest and the highest positions respectively.
2.	Find the middle element mid of the array ie. arr[(low + high)/2]
3.	If x == mid, then return mid.Else, compare the element to be searched with m.
4.	If x > mid, compare x with the middle element of the elements on the right side of mid. This is done by setting low to low = mid + 1.
5.	Else, compare x with the middle element of the elements on the left side of mid. This is done by setting high to high = mid - 1.
6.	Repeat steps 2 to 5 until low meets high
## Program:
i)	#Use a linear search method to match the item in a list.
```PYTHON
Program for linear search method to match the item in a list
Developed by:RIYA P L
RegisterNumber: 23005672
'''
def linearSearch(array,n,k):
    for i in range(0,n):
        if(array[i]==k):
            return i
    return -1
array = eval(input())
k = eval(input())
n=len(array)
array.sort()
result=linearSearch(array,n,k)
if(result== -1):
    print(array)
    print("Element not found")
else:
    print(array)
    print("Element found at index: ",result)

```
ii)	# Find the element in a list using Binary Search(Iterative Method).
```PYTHON
Program to find the element in a list using Binary Search(Iterative Method)..
Developed by:RIYA P L
RegisterNumber: 23005672
'''
def binarysearchIter(array, k, low, high):
    while low<=high:
        mid = low+(high-low)//2
        if array[mid]==k:
            return mid
        elif array[mid]<k:
            low=mid+1
        else:
            high=mid-1
    return -1
array = eval(input())
array.sort()
k = eval(input())
result=binarysearchIter(array,k,0,len(array)-1)
if(result==-1):
    print(array)
    print("Element not found")
else:
    print(array)
    print("Element found at index: ",result)
```
iii)	# Find the element in a list using Binary Search (recursive Method).
```
Program to find the element in a list using Binary Search (recursive Method).
Developed by: RIYA P L
RegisterNumber: 23005672
'''
def BinarySearch(arr, k, low, high):
    if high>=low:
        mid=low + (high - low)//2
        if array[mid]==k:
            return mid
        elif array[mid]>k:
            return BinarySearch(array,k,low,mid-1)
        else:
            return BinarySearch(array,k,mid+1,high)
    else:
        return-1
array = eval(input())
array.sort()
k = eval(input())
result=BinarySearch(array,k,0,len(array)-1)
if(result==-1):
    print(array)
    print("Element not found")
else:
    print(array)
    print("Element found at index: ",result)
```
## Output
![linear1](https://github.com/23005672/Search-Algorithm/assets/138971519/0539ac9d-6a1d-4e5e-a248-f97ee07d0d05)
![linear2](https://github.com/23005672/Search-Algorithm/assets/138971519/3d3aee54-44d7-4864-ab5b-81fc76e96e2d)
![linear3](https://github.com/23005672/Search-Algorithm/assets/138971519/e1fae1ca-931b-43f1-9238-aa4e70091000)


## Result
Thus the linear search and binary search algorithm is implemented using python programming.
