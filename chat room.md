```
s=input()
a=0
for i in s:
    if i=="h" and a==0:
        a=a+1
    elif i=="e" and a==1:
        a=a+1
    elif i=="l" and a==2:
        a=a+1
    elif i=="l" and a==3:
        a=a+1
    elif i=="o" and a==4:
        a=a+1
if a==5:
    print("YES")
else:
    print("NO")
```