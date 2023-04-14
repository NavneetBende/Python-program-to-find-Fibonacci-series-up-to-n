Python program to find Fibonacci series up to n
Find the Fibonacci Series up to Nth Term in Python
Given an integer as an input, the objective is to find the Fibonacci series until the number input as the Nth term. Therefore, we write a program to Find the Fibonacci Series up to Nth Term in Python Language.

Example
Input : 4
Output : 0 1 1 2
Lets have a look at write a program to print fibonacci series in python

What is Fibonacci Series
It’s a unique sequence where the next number is the sum of previous two numbers.

Where the first two terms are always 0 and 1
In mathematical terms :
Fn = Fn-1 + Fn-2

Where,
F0 : 0
F1 : 1
Example Series
The series Looks like : 0, 1, 1, 2, 3, 5, 8, 13, 21, 34, 55, 89, 144 …
Find the Fibonacci Series up to Nth Term in Python Language
Given an integer input as the Nth value, the objective is to Find the Fibonacci Series up to the Nth Term using Loops and Recursion. The objective is to print all the number of the Fibonacci series until the Nth term given as an input. Here are some of the methods to solve the above mentioned problem

Method 1: Using Simple Iteration
Method 2: Using Recursive Function
Method 3: Using direct formulae
We’ll discuss the above mentioned methods in detail in the sections below. Do check out the blue box below for better understanding of the question.

Fibonacci Series in Python

Method 1: Using Simple Iteration
In this method we’ll use loops to iterate through and form the series up to the integer input N as the range. To print the series up to the Nth term we start a loop from 2 to the Nth term as 0 and 1 are the seed values for forming the series. 

Let’s implement the logic in Python Language.

Run

# Write a program to print fibonacci series upto n terms in python
num = 10
n1, n2 = 0, 1
print("Fibonacci Series:", n1, n2, end=" ")
for i in range(2, num):
    n3 = n1 + n2
    n1 = n2
    n2 = n3
    print(n3, end=" ")

print()
Python Code
Output
Fibonacci Series: 0 1 1 2 3 5 8 13 21 34 
Related Pages
Armstrong number

Armstrong number in a given range

Fibonacci Series upto nth term 

Find the Nth Term of the Fibonacci Series

Factorial of a number

Power of a number

Method 2: Using Recursive Function
In this method we’ll use recursion to find the Fibonacci Series up to the given integer input as the Nth range. To do so we take three variables and call the recursive function twice in return statement forming a recursion tree. To know more about recursion, Check out our page, Recursion in Python.

Let’s implement the above mentioned logic in Python Language.

Python Code
Run
# Python program to print Fibonacci Series
def fibonacciSeries(i):
if i <= 1:
return i
else:
return (fibonacciSeries(i - 1) + fibonacciSeries(i - 2))

num=10
if num <=0:
print("Please enter a Positive Number")
else:
print("Fibonacci Series:", end=" ")
for i in range(num):
print(fibonacciSeries(i), end=" ")
Output
Fibonacci Series: 0 1 1 2 3 5 8 13 21 34
Method 3
We can use direct formula to find nth term of Fibonacci Series as –

Fn = {[(√5 + 1)/2] ^ n} / √5

Run
# write a program to print fibonacci series in python
import math

def fibonacciSeries(phi, n):
    for i in range(0, n + 1):
        result = round(pow(phi, i) / math.sqrt(5))
        print(result, end=" ")


num = 10
phi = (1 + math.sqrt(5)) / 2
fibonacciSeries(phi, num)
Output
Fibonacci Series:0 1 1 2 3 5 8 13 21 34 55
