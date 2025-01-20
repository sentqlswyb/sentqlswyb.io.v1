![image-20241113163409416](C:\Users\宋铠仁\AppData\Roaming\Typora\typora-user-images\image-20241113163409416.png)

```
t=int(input())
for i in range(t):
    n,x=map(int,input().split())
    a=list(map(int,input().split()))
    if sum(a)%x!=0:
        print(n)
    else:
        l = -1
        r = n
        dp_l = 0
        dp_r = 0
        while l < n - 1:
            l += 1
            dp_l += a[l]
            if dp_l % x != 0:
                break
        while r > 0:
            r -= 1
            dp_r += a[r]
            if dp_r % x != 0:
                break
        if l == n - 1 and r == 0:
            print(-1)
        elif n - (l + 1) >= r:
            print(n - (l + 1))
        elif n - (l + 1) <r:
            print(r)
```