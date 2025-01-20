![image-20241114112503655](C:\Users\宋铠仁\AppData\Roaming\Typora\typora-user-images\image-20241114112503655.png)

```
t=int(input())
for i in range(t):
    n=int(input())
    a=list(map(int,input().split()))
    b=list(map(int,input().split()))
    c=[]
    for j in range(n):
        c.append([a[j],b[j]])
    c.sort(reverse=True,key=lambda x:x[0])
    time_2=0
    for s in range(n):
        if s<n-1:
            if time_2+c[s][1]<c[s+1][0]:
                time_2+=c[s][1]
            else:
                print(min(time_2+c[s][1],c[s][0]))
                break
        else:
            print(min(time_2+c[s][1],c[s][0]))
            break
```