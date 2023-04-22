## 多次输入，每次的输入是数字+文字，如何只提取出数字（or文字）：
```python
N = int(input())
for i in range(N):
    method,*l = input().split()
    k = list(map(int,l))    #可以是int，也可以是float
    print(k)
```   
```
>>> input:2
          jisfoshf 7898
          jsfsjf 890
>>> output:[7898]
           [890]        
```

## 一次输入多个值，如何提取出不同位置的值(unpacking operator)
```python
a,b,*rest = range(5) #第一个位置的值分配给a，第二个位置的值被分配给b，其他位置的值被分配给rest
print(a)
print(b)
print(rest)
```
```
>>> a = 0
>>> b = 1
>>> rest = [2,3,4]
```

