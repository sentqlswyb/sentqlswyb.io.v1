![](C:\Users\宋铠仁\AppData\Roaming\Typora\typora-user-images\image-20241023180604072.png)

```
n=int(input())
for i in range(n):
    time_max = []
    time_min = []
    a,b=map(int,input().split())
    ants=list(map(int,input().split()))
    for s in ants:
        time_max.append(max(s,a-s))
        time_min.append(min(s,a-s))
    print(max(time_min),max(time_max))
```