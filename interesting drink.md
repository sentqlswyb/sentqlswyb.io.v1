# ![image-20241112162423216](C:\Users\宋铠仁\AppData\Roaming\Typora\typora-user-images\image-20241112162423216.png)

```
n=int(input())
cost=list(map(int,input().split()))
q=int(input())
cost.sort()
for i in range(q):
    m=int(input())
    l=0
    r=n
    while l<r:
        mid=(l+r)//2
        if m<cost[mid]:
            r=mid
        else:
            l=mid+1
    else:
        print(r)
```