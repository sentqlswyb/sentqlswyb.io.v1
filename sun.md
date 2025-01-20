```
a=int(input())
for i in range(a):
    b=list(map(int,input().split()))
    if sum(b)/2!=b[0] and sum(b)/2!=b[1] and sum(b)/2!=b[2]:
        print("NO")
    else:
        print("YES")
```