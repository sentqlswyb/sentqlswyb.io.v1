```
n=int(input())
z=0
for i in range(n):
        a,b,c= map(int,input().split())
        if a+b+c>1:
            z+=1
print(z)
```