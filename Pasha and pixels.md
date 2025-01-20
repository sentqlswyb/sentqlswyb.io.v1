![image-20241028161303469](C:\Users\宋铠仁\AppData\Roaming\Typora\typora-user-images\image-20241028161303469.png)

```
n,m,k=map(int,input().split())
b=0
s=0
c={}
a=[[0 for j in range(m)] for i in range(n)]
for x in range(k):
    i,j=map(int,input().split())
    i-=1
    j-=1
    a[i][j]=1
    if a[i][j] == 1:
        if i > 0 and j > 0 and a[i - 1][j] == 1 and a[i][j - 1] == 1 and a[i - 1][j - 1] ==1:
                b+=1
                s=x+1
                c[b]=s
        elif i > 0 and j < m - 1 and a[i - 1][j] == 1 and a[i - 1][j + 1] == 1 and a[i][j + 1] == 1:
                b+=1
                s=x+1
                c[b]=s
        elif i < n - 1 and j > 0 and a[i][j - 1] == 1 and a[i + 1][j] == 1 and a[i + 1][j - 1] == 1:
                b+=1
                s=x+1
                c[b]=s
        elif i < n - 1 and j < m - 1 and a[i][j + 1] == 1 and a[i + 1][j] == 1 and a[i + 1][j + 1] == 1:
                b+=1
                s=x+1
                c[b]=s
if b>0:
    print(c[1])
else:
    print(0)
```