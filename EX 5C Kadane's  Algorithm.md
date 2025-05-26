# EX 5C Kadane's Algorithm
## DATE:
## AIM:
To write a python program to find the maximum contiguous subarray.


## Algorithm
1. Start by initializing a variable max_sum to 0 to keep track of the maximum subarray sum found so far.
2. Loop through each index i from 0 to n-1 as the starting point of the subarray.
3. For each i, initialize a variable current_sum to 0 to store the sum of the current subarray.
4. Loop through each index j from i to n-1 to consider every subarray starting from index i.
5. Add the current element a[j] to current_sum to extend the subarray.
6. If current_sum is greater than max_sum, update max_sum; if current_sum becomes negative, reset it to 0 to start fresh.

## Program:
```
To implement the program to find the maximum contiguous subarray.
Developed by: Vinush CV
Register Number: 212222230176
```
```py
def maxSubArraySum(a,size):
    maxx=0
    # print(size)
    for i in range(size):
        sum=0
        for j in range(i,size):
            sum+=a[j]
            # maxx=max(maxx,sum)
            if sum>maxx:
                maxx=sum
            if sum<0:
                sum=0
    return maxx
    
n=int(input())  
a =[] #[-2, -3, 4, -1, -2, 1, 5, -3]
for i in range(n):
    a.append(int(input()))
  
print("Maximum contiguous sum is", maxSubArraySum(a,n))

```

## Output:
![image](https://github.com/user-attachments/assets/aebe05bd-5735-432c-91b2-f955266b4c9a)



## Result:
Thus the program was executed successfully for finding the maximum contiguous sum of subarray..
