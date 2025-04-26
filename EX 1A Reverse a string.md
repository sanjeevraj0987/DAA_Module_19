# EX 1A Reverse a String
## DATE:26/04/2025
## AIM:
To write a program to create a recursive function to reverse a string.

## Algorithm
1. Define a recursive function revstr that takes a string as input.

2. Check if the length of the string is zero (base case).

3. If true, return the string.

4. Otherwise, call revstr on the substring excluding the first character and concatenate the first character at the end.

5. Take input from the user and call the recursive function.

6. Print the result.


## Program:
```py
/*
Program to implement Reverse a String
Developed by: YOGESH V S
Register Number: 212222040185 
*/

def revstr(str):
    if len(str) == 0:
        return str
    else:
        return revstr(str[1:]) + str[0]
str = input()
print(revstr(str))
```

## Output:
![image](https://github.com/user-attachments/assets/3be4b0e9-93a8-4884-b529-141ee6a706a1)



## Result:
The program successfully reverses the input string using recursion. When the user provides an input string, the output displays the reversed version of the string
