![image-20241129214924634](C:\Users\宋铠仁\AppData\Roaming\Typora\typora-user-images\image-20241129214924634.png)

```
n=int(input())
a=list(map(int,input().split()))
dp=[1]*n
for i in range(1,n):
    for j in range(i):
        if a[j]<a[i]:
            dp[i]=max(dp[i],1+dp[j])
print(max(dp))
```