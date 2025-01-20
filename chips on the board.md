```
t=int(input())
for i in range(t):
    a_list=[]
    b_list=[]
    n=int(input())
    a=list(map(int,input().split()))
    b=list(map(int,input().split()))
    a.sort()
    b.sort()
    for x in range(n):
        a_list.append(a[x]+b[0])
    for y in range(n):
        b_list.append(b[y]+a[0])
    if sum(a_list)<=sum(b_list):
        print(sum(a_list))
    else:
        print(sum(b_list))
```