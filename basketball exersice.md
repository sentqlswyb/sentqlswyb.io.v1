![image-20241203153812306](C:\Users\宋铠仁\AppData\Roaming\Typora\typora-user-images\image-20241203153812306.png)

```
n=int(input())
h1=list(map(int,input().split()))
h2=list(map(int,input().split()))
dp=[[0,0] for i in range(n+1)]
for i in range(1,n+1):
    dp[i][0]=max(dp[i-1][0],dp[i-1][1]+h1[i-1])
    dp[i][1]=max(dp[i-1][1],dp[i-1][0]+h2[i-1])
print(max(dp[n]))
```