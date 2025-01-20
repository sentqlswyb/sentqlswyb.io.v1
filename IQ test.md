```
a=int(input())
b=list(map(int,input().split()))
c=[]
for i in range(a):
    x=b[i]%2
    c.append(x)
if sum(c)==1:
    for i in range(a):
        if c[i]==1:
            print(i+1)
else:
    for i in range(a):
        if c[i]==0:
            print(i+1)
```