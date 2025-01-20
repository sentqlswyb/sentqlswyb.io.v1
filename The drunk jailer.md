```
o=int(input())
for y in range(o):
    n = int(input())
    a = n * [0]
    for i in range(n - 1):
        for x in range(n):
            if (x + 1) % (i + 2) == 0:
                if a[x] == 0:
                    a[x] = 1
                else:
                    a[x] = 0
    b = a.count(0)
    print(b)
```