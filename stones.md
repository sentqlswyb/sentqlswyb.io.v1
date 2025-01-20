```
a=input()
b=input()
d=0
e=0
for c in b:
    if ord(c)!=d:
            d=ord(c)
    else:
            e+=1

print(e)
```

```
n = int(input())
l = input()

nCount = 0
p = l[0]
for i in range(1,n):
        if l[i]==p:
                nCount += 1
        else:
                p = l[i]

print(nCount)
```