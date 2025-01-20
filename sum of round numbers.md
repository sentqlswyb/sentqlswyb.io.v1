```
t=input()
d=[]
f=[]
for i in range(int(t)):
    a=0
    b=input()
    for x in b:
       if int(x)!=0:
           a+=1
    d.append(a)
    f.append(b)
for i in range(int(t)):
    e=[]
    print(d[i])
    c=int(f[i])
    for y in range(5):
        k=c//10**(4-y)
        c=c-10**(4-y)*k
        if k!=0:
            e.append(k*10**(4-y))
    print(*e)
```