```
n = int(input())
for _ in range(n):
    s = input()
    cnt = 0
    res = []
    i = 0
    for c in s:
        i += 1
        if c != '0':
            cnt += 1
            res.append( int(c) * (10 ** (len(s) - i)) )
    print(cnt)
    print(*res)
```