```
a=int(input())
for i in range(a):
    b=int(input())
    while b%2==0:
        b=b/2
    if b>1:
        print("yes")
    else:
        print("no")
```