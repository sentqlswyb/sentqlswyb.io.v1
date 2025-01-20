```
a=int(input())
b=a//100
c=a-b*100
d=c//20
e=c-d*20
f=e//10
g=e-f*10
h=g//5
i=g-h*5
j=b+d+f+h+i
print(j)
```

```
a=[100,20,10,5,1]
b=int(input())
c=0
for i in range(5):
    c+=b//a[i]
    b=b-a[i]*(b//a[i])
print(c)
```