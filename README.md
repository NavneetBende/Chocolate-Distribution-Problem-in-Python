Chocolate Distribution Problem
Here on this page, we will learn to solve one of the popular question Chocolate Distribution Problem in Python Programing language.

Example :

Input : [12, 4, 7, 9, 2, 23, 25] , m = 4
Output: 7
Explanation: If we pick 2, 4, 7, and 9, we get the minimum difference between maximum and minimum packet sizes.
Chocolate Distribution Problem in Python
Problem Statement
 We are given an array of size n where each value represents the number of chocolates in a packet. Each packet can have a variable number of chocolates.   There are m students, the task is to distribute chocolate packets such that: 

Each student gets one packet.
The difference between minimum and maximum selected packet is minimum.
Algorithm
Start
Initialize a variable ans with value 1000
Sort the input array
Use  a for loop to iterate between range 0 to (l – m + 1)   using variable i
For each iteration if arr[i+m-1] – arr[i] is less then ans then change the value of ans to arr[i+m-1] – arr[i]
After completion of loop print the value of ans
Python Code for Chocolate Distribution Problem
Python Code
Run
def minDiff(arr, m, l):
    ans = 1000
    arr.sort()
    for i in range(l - (m - 1)):
        if arr[i + m - 1] - arr[i] < ans:
            ans = arr[i + m - 1] - arr[i]
    return ans


arr = [12, 4, 7, 9, 2, 23, 25]
m = 4
l = len(arr)
print(minDiff(arr, m, l))
Output
7
