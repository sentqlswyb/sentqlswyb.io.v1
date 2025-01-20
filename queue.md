![image-20241028195323301](C:\Users\宋铠仁\AppData\Roaming\Typora\typora-user-images\image-20241028195323301.png)

```
n=int(input())
b=0
c=0
time=list(map(int,input().split()))
time.sort()
a=n*[False]
a[0]=True
for i in range(n):
    if time[i]>=b:
        a[i]=True
        b+=time[i]
for x in a:
    if x:
        c+=1
print(c)
```