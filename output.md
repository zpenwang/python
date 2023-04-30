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
