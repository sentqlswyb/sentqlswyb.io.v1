```
n=int(input())
lucky_number=[]
for i in range(1,n+1):
    a=str(i)
    b=0
    for x in a:
        if x==str(4) or x==str(7):
            b=0
        else:
            b+=1
    if b==0:
        lucky_number.append(int(i))
c=0
for y in range(len(lucky_number)):
    if n%lucky_number[y]==0:
        c+=1
if c>0:
    print("YES")
else:
    print("NO")
```