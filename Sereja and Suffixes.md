![image-20241129231227006](C:\Users\宋铠仁\AppData\Roaming\Typora\typora-user-images\image-20241129231227006.png)

```
n,m=map(int,input().split())
a=list(map(int,input().split()))
a.reverse()
b=[False]*(10**5+1)
dp=n*[1]
b[a[0]]=True
for i in range(1,n):
    if b[a[i]]:
        dp[i]=dp[i-1]
    else:
        dp[i]=dp[i-1]+1
    b[a[i]]=True
dp.reverse()
for j in range(m):
    l=int(input())
    print(dp[l-1])
```