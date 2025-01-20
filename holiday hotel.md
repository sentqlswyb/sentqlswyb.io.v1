![image-20241023114537479](C:\Users\宋铠仁\AppData\Roaming\Typora\typora-user-images\image-20241023114537479.png)

```
while True:
    try:
        n=int(input())
        if n==0:
            break
    except EOFError:
        break
    hotel = []
    num = 1
    a=0
    for i in range(n):
        d, c = map(int, input().split())
        hotel.append((d, c))
    hotel.sort(key=lambda x: (x[0], x[1]))
    a=hotel[0][1]
    for x in range(1,n):
        if hotel[x][1]<a:
            num+=1
            a=hotel[x][1]
    print(num)
```