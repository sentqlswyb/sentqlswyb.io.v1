```
a=int(input())
b=list(map(int,input().split()))
x=0
y=0
for i in range(a):
    if i==0:
        if b[i]==-1:
            x+=1
        else:
            y+=b[i]
    elif i>0:
        if b[i]>=1:
            y+=b[i]
        elif b[i]==-1:
            if y>0:
                y-=1
            elif y<=0:
                x+=1
print(x)
```

```
n = int(input())
a = list(map(int, input().split()))
cnt = 0
officers = 0
for i in a:
    if i == -1 and officers == 0:
        cnt += 1
        continue
    if i > 0:
        officers += i
        continue
    officers -= 1

print(cnt)
```