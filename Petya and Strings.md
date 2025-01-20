```
a=input().lower()
b=input().lower()
x=0
for i in range(len(a)):
    if ord(a[i])<ord(b[i]):
        print(str(-1))
        break
    elif ord(a[i])>ord(b[i]):
        print(str(1))
        break
    else :
        x+=1
if x==len(a):
    print(str(0))

```