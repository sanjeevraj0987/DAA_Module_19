# EX 1D Linear search
## DATE:26/04/2025
## AIM:
To write a python program for a search function with parameter list name and the value to be searched using string values.



## Algorithm
1.Input the number of elements s and store them in a list.

2.Input the element n to search for.

3.Traverse the list from the beginning to the end.

4.If an element matches n, print "Found" and stop.

5.If the element is not found after checking all elements, print "Not Found".

   

## Program:
```py
/*
Program to implement a search function with parameter list name and the value to be searched using string values.
Developed by: YOGESH V S
Register Number: 212222040185
*/
def search(List, n):
    for i in List:
        if i == n:
            print("Found")
            break
    else:
        print("Not Found")

# Input the number of elements in the list
s = int(input("Enter number of elements in the list: "))

# Input the list of elements
List = [input("Enter element: ") for i in range(s)]

# Input the element to search for
n = input("Enter element to search: ")

# Call the search function
search(List, n)

```

## Output:
![image](https://github.com/user-attachments/assets/40709c78-dd0b-4dba-bc72-d5426e1f6ba6)



## Result:
The program was executed successfully, and it correctly checks if the input element is present in the list, printing "Found" if the element exists or "Not Found" if it does not.
