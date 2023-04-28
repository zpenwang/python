## 常用方法
```python
str.ljust(width[, fillchar])
```
+ 功用：返回一个原字符串左对齐,并使用填充字符填充至指定长度的新字符串。如果指定的长度小于原字符串的长度则返回原字符串  
+ 参数：
   + width -- 指定字符串长度。
   + fillchar -- 填充字符，默认为空格。
```python
str.center(width[, fillchar])
```
```python
str.rjust(width[, fillchar])
```
```python
str.split(str="", num) 
```  
+ 功用：通过指定分隔符对字符串进行切片
+ 参数:
  + str -- 分隔符，默认为所有的空字符，包括空格、换行(\n)、制表符(\t)等。
  + num -- 分割次数，分割成num+1个小字符串。默认为 -1, 即分隔所有。
+ 返回: 分割后的字符串列表    
    
```python
str.strip([chars])
```
+ 功用：移除字符串中头尾指定的字符序列[chars] 
+ 返回：新字符串    
```python
str.swapcase()
``` 
功用：大写-->小写，小写-->大写
```python
str.join(sequence)
```
+ 功用：用于将序列中的元素以指定的字符连接生成一个新的字符串
+ 返回：通过指定字符连接序列中元素后生成的新字符串
## 转换成字符串
#### 列表/元组转化成字符串
```python
list = ['人', '生', '苦', '短']
str1 = ''.join(list)
print(str1)
```
```python
# 变形1
list = ['人', '生', '苦', '短']
str1 = ''.join(map(str,list))
print(str1)
```
```python
# 变形 2
list = ['人', '生', '苦', '短']
str1 = ''.join(str(x) for x in list)
print(str1)
```
#### 集合/字典转成字符串
str()方法
## 字符串的连接
#### 中间有空格
```python
print("Hello","python")
```
```
>>> Hello python
```
#### 中间无空格
```python
# method1
print("Hello"+"python")
```
```python
# method2
print("Hello""python")
```
```
>>> Hellopython
```
```python
# method 3：str.join()方法
list = ['人', '生', '苦', '短']
str1 = ''.join(list)
print(str1)
```
```
>>> 人生苦短
```
## 字符串每int个截取一次
#### 换行输出
```python
# method 1
import textwrap
string = "This is a very very very very very long string."
print(textwrap.fill(string,8))
```
```
>>> This is  # 返回的是段落自动换行后的单独字符串
>>> a very
>>> very
>>> very
>>> very
>>> very
>>> long
>>> string.
```
```python
# method 2
for i in range(0,len(string)+1,max_width):
        result = string[i:i+max_width]
```
#### 不换行输出
```python
import textwrap
string = "abcdefghijklmnopq"
print(textwrap.wrap(string,4))
```
```
['abcd', 'efgh', 'ijkl', 'mnop', 'q']    # 返回的是截取后的字符串生成的列表
```
