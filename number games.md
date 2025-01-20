![image-20241126175605462](C:\Users\宋铠仁\AppData\Roaming\Typora\typora-user-images\image-20241126175605462.png)

```
import bisect
t=int(input())
for i in range(t):
    n=int(input())
    a=list(map(int,input().split()))
    a.sort()
    x=a.count(1)
    for k in range(x,-1,-1):
        y=bisect.bisect_right(a,k)
        r=y-1
        i=1
        p=k-1
        while r>=k:
            if a[r]<=k-i+1:
                p-=1
                r-=1
                i+=1
            elif a[r]>k-i+1:
                r-=1
        else:
            if p<=0:
                print(k)
                break
```