```
a=int(input())
d=[]
for i in range(a):
    b=int(input())
    if b%2==0:
        c=b/2-1
        d.append(int(c))
    else:
        c=(b-1)/2
        d.append(int(c))
for i in range(a):
    print(d[i])
```