![image-20241202200307071](C:\Users\宋铠仁\AppData\Roaming\Typora\typora-user-images\image-20241202200307071.png)

```
def min_rest_days(n, a):
    dp=[[1000,1000,1000] for i in range(n)]
    dp[0][0]=1
    if a[0]==1 or a[0]==3:
        dp[0][1]=0
    if a[0]==2 or a[0]==3:
        dp[0][2]=0
    for i in range(1,n):
        dp[i][0]=min(dp[i-1])+1
        if a[i]==1:
            dp[i][1]=min(dp[i-1][0],dp[i-1][2])
        elif a[i]==2:
            dp[i][2]=min(dp[i-1][1],dp[i-1][0])
        elif a[i]==3:
            dp[i][1]=min(dp[i-1][2],dp[i-1][0])
            dp[i][2]=min(dp[i-1][1],dp[i-1][0])
    return min(dp[n-1])
n=int(input())
a=list(map(int,input().split()))
print(min_rest_days(n,a))
```