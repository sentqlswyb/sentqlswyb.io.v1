![image-20241025105128429](C:\Users\宋铠仁\AppData\Roaming\Typora\typora-user-images\image-20241025105128429.png)

```
n,l=map(int,input().split())
position=list(map(int,input().split()))
position.sort()
distant=[0]*(n-1)
for x in range(1,n):
    distant[x-1]=(position[x]-position[x-1])/2
distant.append(position[0])
distant.append(l-position[n-1])
print(f"{max(distant):.10f}")
```