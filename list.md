## 元素特征
列表的元素可重复，元素的类型也可以不同
## 列表的创建
#### 创建普通列表
```python
  + a = [1,2,c]
  + a = list(1,2,3)
```

#### 创建整数列表
```python
range(start = 0, end, step) #左闭右开
```

#### 创建空列表
```python
  +[]
  +list()
```
## 主要方法
```python
list.insert(index,objection) 
```

```python
list.pop(index = -1)  #默认最后一个元素
``` 

## 转换成列表 
list()方法可以解决大多数问题
#### 字典转换成列表
```python
dict = {'name': '张三', 'age': 18, 'sex': '男'}
keys = list(dict.keys())         # dict.keys()返回的是dict_keys(['name', 'age', 'sex'])，这是class "dict_keys"
values = list(dict.values())     # dict.values()返回的是dict_values(['张三', 18, '男'])，这是class "dict_values"
print(keys)
print(values)
```
#### 字符串转换成列表
```python
# 第一种
str1 = 'hello python'
str2= str1.split(' ')    # split方法返回字符串列表
print(str2)
```
```
>>> ['hello', 'python']
```
```python
# 第二种
str1 = 'bonjour'
print(list(str1))
```
```
>>> ['b', 'o', 'n', 'j', 'o', 'u', 'r']
```
#### 元组转换成列表
```python
tuple = (1, 2, 3)
list = list(tuple)
print(list)
```
```
>>> [1, 2, 3]
```
#### 集合转换成列表
```python
set1 = {1, 3, 4, 3, 2, 1}
list1 = list(set1)
print(list1)
```
```
>>> [1, 2, 3, 4]
```
## 嵌套列表 （Nested list）
#### 根据第1/2项对整个列表降序排列
```python
stu.sort(key = lambda x:x[0], reverse = True)
```
#### 根据第1项字符串长度对整个列表降序排列
```python
stu.sort(key = lambda x:len(x[0]), reverse = True)
```
#### 提取每个小列表第1项的数 
```python
[lst[1] for lst in stu]. # 列表推导式
```
#### 列表展平化
```python
nums = [[1,2,3],[4,5,6]]
c = [e for num in nums for e in num]
print(c)
```
```
>>> [1, 2, 3, 4, 5, 6]
```
## 生成全排列列表
```python
# method 1
import itertools
nums = [1,2,3]
permutations = list(itertools.permutations(nums))
print(permutations)
  
>>> [(1, 2, 3), (1, 3, 2), (2, 1, 3), (2, 3, 1), (3, 1, 2), (3, 2, 1)]
```

```python
# method 2
x = int(input())
y = int(input())
z = int(input())
n = int(input())
print ([ [ i, j, k] for i in range( x + 1) for j in range( y + 1) for k in range( z + 1) if ( ( i + j + k ) != n )])
```

## 整理列表
```python
# method 1
list.sort(cmp = None, key = None, reverse = False)
```
+ 描述：用于对原列表进行排序  
+ 参数：
  + cmp -- 可选参数, 如果指定了该参数会使用该参数的方法进行排序
  + key -- 主要是用来进行比较的元素，只有一个参数，具体的函数的参数就是取自于可迭代对象中，指定可迭代对象中的一个元素来进行排序。此函数必须遵守的规则为，大于则返回1，小于则返回-1，等于则返回0。   
  + reverse -- 排序规则，reverse = True 降序， reverse = False 升序（default）    
+ 返回：没有返回值，但是会在原列表的基础上对列表的对象进行排序

```python
# method 2
sorted(iterable, cmp = None, key = None, reverse = False)
```
+ 返回： 返回重新排序的列表
+ sort 与 sorted 区别：
  + sort 是应用在 list 上的方法，sorted 可以对所有可迭代的对象进行排序操作。
  + list 的 sort 方法返回的是对已经存在的列表进行操作，无返回值，而内建函数 sorted 方法返回的是一个新的 list，而不是在原来的基础上进行的操作。

