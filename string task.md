```
a=input()
letter=[]
b=["a","o","y","e","u","i"]
for i in a:
    i.lower()
    if i not in b:
        letter.append(i)
print("."+".".join(letter))
```