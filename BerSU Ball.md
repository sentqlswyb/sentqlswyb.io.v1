![image-20241023140752218](C:\Users\宋铠仁\AppData\Roaming\Typora\typora-user-images\image-20241023140752218.png)

```
b=int(input())
boy=list(map(int,input().split()))
g=int(input())
girl=list(map(int,input().split()))
boy.sort()
girl.sort()
index_a=0
girl_paired=[]
num=0
for i in range(b):
    a=2
    c=0
    for j in range(g):
        if abs(boy[i]-girl[j])<a and j not in girl_paired:
            index_a=j
            c+=1
            break
    if c!=0:
        girl_paired.append(index_a)
        num+=1
print(num)
```