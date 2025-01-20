```
a=int(input())
b=list(map(int,input().split()))
b.sort(reverse=True)
x=0
y=0
for i in range(a):
   x=x+b[i]
   y+=1
   if x>sum(b)-x:
       print(y)
       break
```