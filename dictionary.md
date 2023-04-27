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
#### 列表转化成字典
```python
a = ["age","height","weight"]
b = [15,28,90]
d = zip(a,b)
print(dict(d))
```
```
{'age': 15, 'height': 28, 'weight': 90}
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
