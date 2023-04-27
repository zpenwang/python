## 特征
只读
## 创建元组
#### 创建空元组
```python
temp = ()
```
```python
temp = tuple()
```
#### 创建一个元素的元组
```python
temp = "hello",    # 尾部的逗号不可省略
```

```python
temp = ("hello",)   # 尾部的逗号不可省略
```
#### 创建多个元素的元组
```python
temp = (1,2,7)
```

```python
temp = 1,2,"Hello, world"
```
## 转换成元组
#### 字典转换成元组
```python
dict = {'name': 'xiaoming', 'age': 18}
tup1 = tuple(dict)  # 等同于tup1 = tuple(dict.keys())
print(tup1)   
tup2 = tuple(dict.values())
print(tup2)
```
```
>>> ('name', 'age')
>>> ('xiaoming', 18)
```
#### 列表/集合转换成元组
list()方法
#### 字符串转换成元组
字符串-->列表-->元组
