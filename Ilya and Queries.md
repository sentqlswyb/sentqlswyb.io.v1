```
a=input()
m=int(input())
b=[0]*len(a)
for x in range(len(a)-1):
    if x==0:
        if a[x]==a[x+1]:
            b[1]=1
        else:
            b[1]=0
    else:
        if a[x]==a[x+1]:
            b[x+1]=b[x]+1
        else:
            b[x+1]=b[x]
for i in range(m):
    l,r=map(int,input().split())
    print(b[r-1]-b[l-1])
```

![image-20241024224737891](C:\Users\宋铠仁\AppData\Roaming\Typora\typora-user-images\image-20241024224737891.png)