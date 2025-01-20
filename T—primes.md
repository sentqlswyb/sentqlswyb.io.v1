```
n=input()
a=list(map(int,input().split()))
for x in range(len(a)):
    b=a[x]
    c=0
    for y in range(1,int(b**0.5)):
        if y!=1:
            if b%y==0:
                    c+=1
    if b**0.5%1==0 and c==0:
        print("YES")
    else:
        print("NO")
```