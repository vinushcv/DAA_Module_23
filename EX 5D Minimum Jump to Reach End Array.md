# EX 5D Minimum Jump to Reach End Array
## DATE:
## AIM:
To write a python program for finding the minimum number of jumps needed to reach end of the array using Dynamic Programming.


## Algorithm
1. If the array has 1 or fewer elements, return 0 as no jumps are needed.
2. Create a dp array of size n and initialize all values to infinity, except dp[0] = 0 (start position).
3. Loop over each index i from 1 to n-1 to find the minimum jumps needed to reach i.
4. For each i, loop over all previous indices j from 0 to i-1.
5. If index j can reach index i (i.e., j + arr[j] >= i), update dp[i] = min(dp[i], dp[j] + 1).
6. Return dp[n-1] as the minimum number of jumps required to reach the end of the array.

## Program:
```
To implement the program to finding the minimum number of jumps needed to reach end of the array.
Developed by: R Guruprasad
Register Number: 212222240033
```
```py
def minJumps(arr, n):
    if n<=1:
        return 0
    dp=[float('inf')]*n
    dp[0]=0
    
    for i in range(1,n):
        for j in range(i):
            if j+arr[j]>=i:
                dp[i]=min(dp[i],dp[j]+1)
                break
    return dp[-1]
    
    
    
arr = []
n = int(input()) #len(arr)
for i in range(n):
    arr.append(int(input()))
print('Minimum number of jumps to reach','end is', minJumps(arr,n))
 
```

## Output:
![image](https://github.com/user-attachments/assets/18333c5d-f33b-4703-aea7-a155e0892755)




## Result:
Thus the program was executed successfully for finding the minimum number of jumps to reach end.
