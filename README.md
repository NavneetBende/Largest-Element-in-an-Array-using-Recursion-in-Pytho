# Largest-Element-in-an-Array-using-Recursion-in-Python

Largest Element in an Array
Given an array of integers “A”, the task is to write a Program for Finding the Largest Element in an Array in Python Language using recursion algorithm.

For instance,

Input: A = [1, 4, 3, -5, -4, 8, 6]
Output: 8
Find the Largest Element in an Array using Recursion in C

Largest Element in an Array
The objective is to recursively traverse the whole input array and compare each characters to find the Largest of them all. In order to do so we declare a function and pass the original array and it’s Length. With each recursive step call we’ll keep on decrementing the value of length “n” as shown in the image adjacent. The base condition for the function is given as such that the recursion terminates when the length “n”  becomes  1. as shown in the last block in the image.

Let’s understand the whole process in more depth by taking an example. Let the original array be A = [1, 4, 3, -5]. Now to recursively call the function giving the array “A” and it’s length “n” as arguments. The function returns the maximum of the last element of the array “A” and the value returned by the recursive call of the function findMaxRec(A,n-1) using max() function.

Once the function is called recursively, it goes on breaking down the string into tiny bits. The recursion is terminated when the base base is satisfied. It’ll return the first element of the array A[0]. The values are then compared as shown in the image and the maximum value is returned after comparing. 

Find the Largest Element in an Array using Recursion in C
Python Code
Run
def findMaxRec(A, n):
    if (n == 1):
        return A[0]
    return max(A[n - 1], findMaxRec(A, n - 1))
 
# Driver Code
if __name__ == "__main__":
     
    A = [1, 4, 45, 6, -50, 10, 2]
    n = len(A)
    print(findMaxRec(A, n))
Output
45
Explanation

The objective of the above code is to recursively traverse through the array “A” and print the Largest Element in an Array in Python.

The algorithm for the above code is as follows:

Define a function dinfMaxRec() which takes input array “A” and it’s length “n” as arguments.
Check if the length of the input array “A” is 1. if true return the first element of the input array.
Else recursively call the findMaxRec() function and return the Largest of A[n-1] and findMaxRec(A,n-1) using max() function.
Initialize variables and call the findMaxRec() function from the driver code.
Print using the print() function.
The output for the above code is the largest element in the input array i.e 45.

