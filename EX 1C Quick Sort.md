# EX 1C Quick Sort
## DATE:26/04/2025
## AIM:
To write a python program to implement quick sort using tha last element as pivot on the list of float values.

## Algorithm
1.Input the number of elements n and store them in an array.

2.Choose a pivot (usually the last element).

3. Partition the array so that:

    Elements smaller than the pivot go to the left.

    Elements greater go to the right.

4.Recursively apply Quick Sort to the left and right parts.

5.Print the sorted array.

  

## Program:
```py
/*
Program to implement implement quick sort using the last element as pivot on the list of float values.
Developed by: YOGESH V S
Register Number: 212222040185 
*/
def quickSort(nums,l,r):
    if len(nums)==1:
        return nums
    if l<r:
        pi=part(nums,l,r)
        quickSort(nums,l,pi-1)
        quickSort(nums,pi+1,r)
def part(nums,l,r):
    pi,ptr=nums[r],l
    for i in range(l,r):
        if nums[i]<=pi:
            nums[i],nums[ptr]=nums[ptr],nums[i]
            ptr+=1
    nums[ptr],nums[r]=nums[r],nums[ptr]
    return ptr
n=int(input())
arr=[float(input()) for i in range(n)]
quickSort(arr,0,n-1) 
print("Sorted array is:")
for i in range(n):
    print(arr[i])
```

## Output:
![image](https://github.com/user-attachments/assets/49a74a57-3344-475c-aa12-ca5cabcf8628)



## Result:
The program successfully sorts the input array using the QuickSort algorithm, arranging the elements in ascending order.
