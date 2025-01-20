![image-20241129155553776](C:\Users\宋铠仁\AppData\Roaming\Typora\typora-user-images\image-20241129155553776.png)

```
n,a,b,c=map(int,input().split())
x=[a,b,c]
dp=[0]+[-5000]*n
for i in range(1,n+1):
    for s in [y for y in x if y<=i]:
        dp[i]=max(dp[i],1+dp[i-s])
print(dp[n])
```