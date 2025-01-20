```
def gcd(a, b):
    while b != 0:
        a, b = b, a % b
    return a

# 读取输入
import sys
input = sys.stdin.read
data = input().strip().split('\n')

# 处理每组数据
results = []
for line in data:
    a, b = map(int, line.split())
    results.append(gcd(a, b))

# 输出结果
for result in results:
    print(result)
```