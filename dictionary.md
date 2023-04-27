## 创建字典
```python
dic = {"name": Jack, "age":18, "height":180}
```
```python
dic = dict(name = "Jack", age = 18, height = 180)
```
```python
dic = dict([("name","jack"),("age",18)])
```
```python
dic = {i:i**2 for i in range(1,5)}
```
## 转换成字典
#### dict(list())
不能直接用；要求：必须是等长的二级容器,并且里面的元素个数是2个; 外层是列表/元组/集合，里层是列表/元组的等长二级容器

+ 外层是列表/元组,里层是列表/元组
```python
lst = [ ["a",1] , ("b",2) ]
dic = dict(lst)
print(dic)
```
```
>>> {'a': 1, 'b': 2} 
```

```python
tup = ( ["a",1] , ("b",2) )
dic = dict(tup)
print(dic)
```
```
>>> {'a': 1, 'b': 2}
```
+ 如果外层是集合,里层必须是元组
```python
setvar = { ("a",1) , ("b",2) }
dic = dict(setvar)
print(dic , type(dic))
```
```
>>> {'a': 1, 'b': 2} 
```

#### 列表转化成字典 
print(dict(list3))
```python
# method 1 利用dict(zip())
a = ["age","height","weight"]
b = [15,28,90]
print(dict(zip(a,b)))
```
```
>>> {'age': 15, 'height': 28, 'weight': 90}
```

```python
# method 2 利用添加键值对method1
list1 = ['name', 'age', 'sex']
list2 = ['张三', 18, '男']
dict = {}
for i in range(len(list1)):
   dict[list1[i]] = list2[i]
print(dict)
```
```
>>> {'name': '张三', 'age': 18, 'sex': '男'}
```
#### 嵌套列表转化成字典
```python
list3 = [['key1','value1'],['key2','value2'],['key3','value3']]
print(dict(list3))
```
#### 字符串转化为字典
```python
dic2 = eval("{'name':'xiaoming', 'age':18}")
print(dic2, type(dic2))
```

#### 元组不能转化为字典
#### 集合转化为字典
```
# method1 集合———>列表——>字典
```
```python
# method 2
PACKAGE_MAP = {}
package = {"今天天气很好", "明天天气也很好", "后天天气也是很好"}
PACKAGE_MAP["最近三天的天气情况"] = package
print(PACKAGE_MAP)
```
or
```python
PACKAGE_MAP = {}
package = {"今天天气很好", "明天天气也很好", "后天天气也是很好"}
PACKAGE_MAP = {"最近三天的天气情况": package}
print(PACKAGE_MAP)
```
```
>>> {'最近三天的天气情况': {'明天天气也很好', '后天天气也是很好', '今天天气很好'}}
```
## 添加键值对
```python
# method 1
dic = {}
dic["name"] = "zhangshan"
print(dic)
```
```
>>> {'name': 'zhangshan'}
```
```python
# method 2
dic = {}
key = "age"
value = 30
dic[key] = value
print(dic)
```
```
>>> {'age': 30}
```
## 键值对互换
```python
dic1 = {'a': 1, 'b': 2, 'c': 3}
dic2 = {value: key for key, value in dic1.items()}
print(dic2)
```
```
>>> {1: 'a', 2: 'b', 3: 'c'}
```
