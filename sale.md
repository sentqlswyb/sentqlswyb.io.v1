```
a,b=map(int,input().split())
c=list(map(int,input().split()))
d=[]
for i in range(b):
    if min(c)<=0:
        d.append(min(c))
        c.remove(min(c))
print(-sum(d))
```