```
t=int(input())
a=list(map(int,input().split()))
if sum(a)%3!=0:
    print(0)
else:
    m=n=0
    b = [0] * len(a)
    b[0] = a[0]
    x = int(sum(a) / 3)
    for i in range(1, len(a)):
        b[i] = a[i] + b[i - 1]
    for j in range(t):
        if 0 < j < t - 1 and b[j] == 2 * x:
            n += m
        if b[j] == x:
            m += 1
    print(n)
```

![image-20241119223307758](C:\Users\宋铠仁\AppData\Roaming\Typora\typora-user-images\image-20241119223307758.png)