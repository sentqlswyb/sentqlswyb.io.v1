```
t=int(input())
for i in range(t):
    n,k=map(int,input().split())
    a=list(map(int,input().split()))
    b=list(map(int,input().split()))
    result=[]
    for x in range(n):
        c={}
        status=[]
        used_ord=[]
        for y in range(n):
            status.append(abs(a[x]-b[y]))
            c[abs(a[x]-b[y])]=y
            used_ord.append(y)
        while c[min(status)]  in used_ord:
            status.remove(min(status))
        if c[min(status)] not in used_ord:
            result.append(b[c[min(status)]])
            break
    print(*result)
```