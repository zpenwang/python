## 功用
调用随机数函数时需要先调用这个库
## 主要函数
```python
import random
random.randint(index1, index2) # 函数返回index1和index2之间的任意整数
```
+ 参数：index1, index2必须是整数，两边都是闭区间

```python
import random
random.random()   #产生0-1之间的随机浮点数
```

```python
import random
random.randrange ([start,] stop [,step])   #产生start和stop的间隔为step的随机整数
```
+ 参数：左闭右开，step值默认为1
```python
import random
random.uniform(index1, index2)   #产生index1到index2之间的随机浮点数
```
+ 参数：index1，index2可以不是整数，左闭右开

```python
import random
random.choice(seq) #从seq中随机选择一个元素
```
+ 参数：seq可以是一个列表，元组或字符串。
