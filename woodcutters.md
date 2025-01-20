![image-20241122163026301](C:\Users\宋铠仁\AppData\Roaming\Typora\typora-user-images\image-20241122163026301.png)

```
n=int(input())
a=[]
for i in range(n):
    x,h=map(int,input().split())
    a.append((x,h))
ed=1
num=0
for j in range(n):
    if j==0:
        num+=1
        ed=a[j][0]
    elif 0<j<n-1:
        if a[j][0] - a[j][1] > ed:
            num += 1
            ed = a[j][0]
        elif a[j + 1][0] - a[j][0] > a[j][1]:
            num += 1
            ed = a[j][0] + a[j][1]
        else:
            ed=a[j][0]
    else:
        num+=1
print(num)
```