```
for i in range(1,6):
        a,b,c,d,e=map(int,input().split())
        if a+b+c+d+e>0:
                n=a*2+b*1+c*0+d*1+e*2+abs(i-3)
print(n)
```