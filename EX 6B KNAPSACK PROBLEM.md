# EX 6B KNAPSACK PROBLEM
## DATE:
## AIM:
To demonstrate a python program using dynamic programming for 0/1 knapsack problem.

## Algorithm
1. Base case : If there are no items left or the capacity is 0, return 0.
2. Item exclusion : If the current item's weight is greater than the remaining capacity, skip it.
3. Item inclusion : Otherwise, choose between including the item or excluding it.
4. Recursive calls : Recursively solve the problem by either excluding or including the item.
5. Return maximum value : At each step, return the maximum value of including or excluding the current item. 

## Program:
```
Developed by: SAKTHIVEL R
Register Number: 212222100044
```
```py
def knapSack(W, wt, val, n):
	if n == 0 or W == 0 :
		return 0
	if (wt[n-1] > W):
		return knapSack(W, wt, val, n-1)
	else:
		return max(val[n-1] + knapSack(W-wt[n-1], wt, val, n-1), knapSack(W, wt, val, n-1))
x=int(input())
y=int(input())
W=int(input())
val=[]
wt=[]
for i in range(x):
    val.append(int(input()))
for y in range(y):
    wt.append(int(input()))
n = len(val)
print('The maximum value that can be put in a knapsack of capacity W is: ',knapSack(W, wt, val, n))
```

## Output:

![24b](https://github.com/user-attachments/assets/5999041c-85e9-49ac-9ec1-57604bf2825f)



## Result:

Thus the program was executed successfully for finding the maximum value that can be put in a knap sack of capacity.
