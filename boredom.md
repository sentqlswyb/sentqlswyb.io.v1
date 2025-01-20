![image-20241205114059709](C:\Users\宋铠仁\AppData\Roaming\Typora\typora-user-images\image-20241205114059709.png)

```
n = int(input())
x=list(map(int,input().split()))
M=max(x)
a=[0]*(M+1)
for y in x:
    a[y]+=1
dp = [[0, 0] for _ in range(M + 1)]
for i in range(1, M + 1):
    dp[i][0] = max(dp[i - 1][0], dp[i - 1][1])
    dp[i][1] = dp[i - 1][0] + a[i] * i
print(max(dp[M][0], dp[M][1]))
```