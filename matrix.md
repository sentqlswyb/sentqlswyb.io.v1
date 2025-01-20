![image-20241113165737330](C:\Users\宋铠仁\AppData\Roaming\Typora\typora-user-images\image-20241113165737330.png)

```
n,m=map(int,input().split())
a=[]
for i in range(n):
    a.append(list(map(int,input().split())))
b=[["0" for i in range(m)] for j in range(n)]
a=[[0 for i in range(m+2)]]+[[0]+a[i]+[0] for i in range(n)]+[[0 for i in range(m+2)]]
for i in range(1,n+1):
    for j in range(1,m+1):
        if a[i][j]==0:
            if a[i-1][j]+a[i+1][j]+a[i][j-1]+a[i][j+1]+a[i-1][j-1]+a[i-1][j+1]+a[i+1][j-1]+a[i+1][j+1]==3:
                b[i-1][j-1]="1"
        else:
            if 2<=a[i-1][j]+a[i+1][j]+a[i][j-1]+a[i][j+1]+a[i-1][j-1]+a[i-1][j+1]+a[i+1][j-1]+a[i+1][j+1]<=3:
                b[i-1][j-1]="1"
for i in range(n):
    print(" ".join(b[i]))
```