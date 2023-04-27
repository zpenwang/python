## 集合的功用
集合的元素特征是无序不重复，用于关系测试和消除重复关系
## 创建集合
```set(1,2)```  
```{c,r,5}```
## 创建空集合
```set() # 创建空集合不能用{}因为这个是用于创建空字典的```
## 转换成集合
#### 字典转换成集合
```python
dict = {"height":185,"weight":85,"name":"wang"}
print(set(dict.keys()))      # dict.keys()返回的是dict_keys(['height', 'weight', 'name'])，属于class “dict_keys”
print(set(dict.values()))
print(set(dict.items()))
```
```
>>> {'name', 'height', 'weight'}
>>> {185, 85, 'wang'}
>>> {('height', 185), ('name', 'wang'), ('weight', 85)}
```
#### 字符串/元组/列表转换成集合
list()方法
