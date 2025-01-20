![********](C:\Users\宋铠仁\AppData\Roaming\Typora\typora-user-images\image-20241112154233135.png)

```
while True:
    try:
        r,n=map(int,input().split())
        if r==n==-1:
            break
    except EOFError:
        break
    position=list(map(int,input().split()))
    position.sort()
    start=position[0]
    between=position[0]
    num=1
    for i in range(n):
            if position[i]<=start+r:
                between=position[i]
            else:
                if position[i]>between+r:
                    num+=1
                    start=position[i]
                    between=position[i]
    print(num)
```