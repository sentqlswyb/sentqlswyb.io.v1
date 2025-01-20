![image-20241023091627992](C:\Users\宋铠仁\AppData\Roaming\Typora\typora-user-images\image-20241023091627992.png)

```
n=int(input())
computer=[]
c=0
for i in range(n):
    a,b=map(int,input().split())
    computer.append((a,b))
computer.sort(reverse=True,key=lambda x:x[1])
b=computer[0][0]
for x in range(n):
    if computer[x][0]<b:
        b=computer[x][0]
    elif computer[x][0]>b:
        c+=1
if c>0:
    print("Happy Alex")
else:
    print("Poor Alex")
```