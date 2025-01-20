![image-20241212200200903](C:\Users\宋铠仁\AppData\Roaming\Typora\typora-user-images\image-20241212200200903.png)

```
t,k=map(int,input().split())
x=10**5+1
dp=[[0,0] for y in range(x+1)]
ans=[0]*(x+1)
ans[1]=1
dp[0][0]=1
for i in range(1,x+1):
    dp[i][0]=(dp[i-1][0]+dp[i-1][1])%(10**9+7)
    if i-k>=0:
        dp[i][1]=(dp[i-k][1]+dp[i-k][0])%(10**9+7)
    else:
        dp[i][1]=0
    ans[i]=ans[i-1]+sum(dp[i])
for s in range(t):
    a,b=map(int,input().split())
    print((ans[b]-ans[a-1])%(10**9+7))
```