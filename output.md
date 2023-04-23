## 格式化
#### format用法
```python
print("{} {}".format("Hello","World")) # 不设置指定位置，按默认顺序
```
```python
print("{0}{1}{0}".format("Hello","World")) # 设置指定位置
```
```python
print("{a}{b}".format(a = "Hello", b = "World")) # 设置参数
```
```python
a = "hello"
b = "world"
print(f"{a} {b}") # format用法变形: f"xxxx"(字符串前面加f)
```
```
>>> 'hello world'
```
```python
print("{:.2f}".format(3.1415926)) # 数字格式化
```
<img width="837" alt="截屏2023-04-22 22 45 04" src="https://user-images.githubusercontent.com/131491147/233805989-ade77de4-0534-41d9-a49a-3b9c351f6dd0.png">

## 不换行输出
```python
print("Asia",end = "") #两段输出之间没有空格
print("community")
``` 
```
>>> Asiacommunity
```
```python
print("string",end = " ") # 两段输出之间有空格
```   
```python
print("string",end = "@") #两段输出之间有符号
```   

## 换行输出
#### 字符串换行输出
```python
print("bonjour\nmadame")  # \n一定要在“”里面
```
```
>>> bonjour
>>> madame
```

```python
print('''hello
world''')       #前后三个引号，字符串内部换行 
```
#### 变量换行输出
```python
A = "A"
B = "B"
C = "C"
print(A,B,C,sep='\n'). 
```
```
>>> A
>>> B
>>> C
```
