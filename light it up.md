![image-20241121115657712](C:\Users\宋铠仁\AppData\Roaming\Typora\typora-user-images\image-20241121115657712.png)

```
n,m=map(int,input().split())
a=[0]+list(map(int,input().split()))+[m]
b=[0]*(n+2)
x=0
for i in range(1,n+2):
    b[i-1]=a[i]-a[i-1]
for s in range(n+2):
    if (s+1)%2==1:
        x+=b[s]
c=[]
for j in range(n+1):
    if (j+1)%2==0:
        c.append(b[j]-b[j+1])
c.reverse()
d=[0]+[0]*len(c)
for k in range(1,len(c)+1):
    d[k]=d[k-1]+c[k-1]
y=max(d)
if y>0:
    print(x+y-1)
if y<=0:
    print(x)
```