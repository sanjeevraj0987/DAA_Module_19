# EX 1B Merge Sort
## DATE:26/04/2025
## AIM:
To write a python program to sort the first half of the list using merge sort.

## Algorithm
1.Read the number of elements n and store the input numbers in an array.

2.Call the function mergeSort(arr, 0, n - 1) to sort the array.

3.In mergeSort(arr, l, r):

  If l < r, find the middle index m.

  Sort the left half by calling mergeSort(arr, l, m).

  Sort the right half by calling mergeSort(arr, m + 1, r).

  Merge the two halves using the merge(arr, l, m, r) function.

4.In merge(arr, l, m, r):

  Create two temporary arrays for left and right halves.

  Copy the data from the original array into these temporary arrays.

  Compare and merge the elements back into the original array in sorted order.

5.Print the sorted array.   

## Program:
```py
/*
Program to implement Merge Sort
Developed by: YOGESH V S
Register Number: 212222040185 
*/
def merge(arr, l, m, r):
    n1 = m - l + 1
    n2 = r - m
    L = [0] * n1
    R = [0] * n2

    for i in range(n1):
        L[i] = arr[l + i]

    for j in range(n2):
        R[j] = arr[m + 1 + j]

    i = 0
    j = 0
    k = l

    while i < n1 and j < n2:
        if L[i] <= R[j]:
            arr[k] = L[i]
            i += 1
        else:
            arr[k] = R[j]
            j += 1
        k += 1

    while i < n1:
        arr[k] = L[i]
        i += 1
        k += 1

    while j < n2:
        arr[k] = R[j]
        j += 1
        k += 1

def mergeSort(arr, l, r):
    if l < r:
        m = (l + r) // 2
        mergeSort(arr, l, m)
        mergeSort(arr, m + 1, r)
        merge(arr, l, m, r)

# Main Program
arr = []
n = int(input("Enter number of elements: "))
for i in range(n):
    arr.append(int(input(f"Enter element {i+1}: ")))

print("\nGiven array is:")
for i in range(n):
    print(arr[i], end=" ")

mergeSort(arr, 0, n - 1)

print("\n\nSorted array is:")
for i in range(n):
    print(arr[i], end=" ")

```

## Output:
![image](https://github.com/user-attachments/assets/4fb69389-10ea-4e9b-96f0-a6ad3f50a455)



## Result:
The program successfully sorts the first half of the given array using merge sort. where only the first half is sorted, and the second half remains unchanged.
