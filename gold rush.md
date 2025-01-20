![image-20241128231628116](C:\Users\宋铠仁\AppData\Roaming\Typora\typora-user-images\image-20241128231628116.png)

```
from functools import lru_cache
t=int(input())
@lru_cache(maxsize=None)
def yes_or_no(n,m):
    if n==m:
        return True
    if n%3==0:
        if yes_or_no(n/3*2,m):
            return True
        elif yes_or_no(n/3,m):
            return True
        else:
            return False
    else:
        return False
for i in range(t):
    n,m=map(int,input().split())
    if yes_or_no(n,m):
        print("YES")
    else:
        print("NO")
```