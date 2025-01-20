```
t = int(input())

for _ in range(t):
    n, k = map(int, input().split())
    a = list(map(int, input().split()))
    b = list(map(int, input().split()))

    result = []
    used = set()

    for x in range(n):
        min_diff = float('inf')
        best_b_index = -1
        for y in range(n):
            if y not in used and abs(a[x] - b[y]) <= k:
                if abs(a[x] - b[y]) < min_diff:
                    min_diff = abs(a[x] - b[y])
                    best_b_index = y
        if best_b_index != -1:
            result.append(b[best_b_index])
            used.add(best_b_index)

    print(*result)
```