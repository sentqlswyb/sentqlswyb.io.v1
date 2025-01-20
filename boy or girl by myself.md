```
a=input()
letter=[]
c=0
for i in range(len(a)):
    letter.append(ord(a[i]))
    b=int(letter.count(ord(a[i])))
    if b==1:
        c+=1
    else:
        c+=0
if c%2!=0:
    print("IGNORE HIM!")
else:
    print("CHAT WITH HER!")
```