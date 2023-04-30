## 常用方法
```python
str.title()
```
+ 功用：返回"标题化"的字符串,就是说所有单词都是以大写开始，其余字母均为小写
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
>>> ['abcd', 'efgh', 'ijkl', 'mnop', 'q']    # 返回的是截取后的字符串生成的列表
```
## 字符串格式化
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
print("{:.2f}".format(3.1415926)) # 数字格式化
```
<img width="837" alt="截屏2023-04-22 22 45 04" src="https://user-images.githubusercontent.com/131491147/233805989-ade77de4-0534-41d9-a49a-3b9c351f6dd0.png">

*数值类型不加# vs 加#：*      
*二进制整数'1111011''0b1111011'开头是否显示 0b*   
*八进制整数'173''0o173'开头是否显示 0o*   
*十进制整数'123''123'无区别*   
*十六进制整数（小写字母）'7b''0x7b'开头是否显示 0x*   
*十六进制整数（大写字母）'7B''0X7B'开头是否显示 0X*    

#### f-string用法
+ {}填入变量名
```python
a = "hello"
b = "world"
print(f"{a} {b}") 
```
+ {}评估表达式
```python
num1 = 83
num2 = 9
print(f"The product of {num1} and {num2} is {num1 * num2}.")
```
```
# output
The product of 83 and 9 is 747.
```
+ {}调用函数
```python
def choice(c):
  if c%2 ==0:
    return "Learn Python!"
  else:
    return "Learn JavaScript!"
print(f"Hello Python, tell me what I should learn. {choice(3)}")
```
```
# output
Hello Python, tell me what I should learn. Learn JavaScript!
```
+ {}填入lambda函数
```python
aa = 123.456
f"{(lambda x:x*5-2)(aa):.2f}"

bb = 8
cc = 2
f"{(lambda x,y:x+y)(bb,cc)}"   # 第一个小括号是lambda表达式，第二个小括号是传入参数
```
```
# output
615.28
10
```
+ {}填入条件语句（三元运算符）
```python
num = 87
print(f"Is num even? {True if num%2==0 else False}")
```
+ f-string 填充
1. 默认使用空格填充
```python
name = "Huang Wei"
print(f"{name:>20}") #向右对齐
print(f"{name:<20}") #向左对齐
print(f"{name:^20}") #中间对齐
```
```
#output
'           Huang Wei'
'Huang Wei           '
'     Huang Wei      '
```
2. 使用指定符号填充
```python
name = "Huang Wei"
f"{name:_>20}"
```
```
#output
'___________Huang Wei'
```
+ 数字格式化
1. 符号       
![02095935_62e88507378829371](https://user-images.githubusercontent.com/131491147/235367426-15f6dd05-57fd-48d3-848b-b5f3e37008a1.png)
```python
a = 12
b = -25
print(f"{a:+}")
print(f"{b:+}")

print(f"{a:-}")
print(f"{b:-}")

print(f"{a: }")
print(f"{b: }")
```
```
# output
'+12'
'-25'

'12'
'-25'

' 12'
'-25'
```
2. 宽度与精度

![02095935_62e8850752ea457966](https://user-images.githubusercontent.com/131491147/235367378-3e840fc3-b4f2-4e84-93cc-0594cd7e1287.png)
```python
a = 123.456   
print(f"{a:10}")    # 只指定width
print(f"{a:010}")   # 只指定0width
print(f"{a:8.1f}")  # 使用width.precision
print(f"{a:2f}")    # 在width后面，直接加f，表示补足小数点后的位数至默认精度6
```
```
#output
'   123.456'
'000123.456'
'   123.5'
'123.456000'
```

3. 千位分隔符
```python
print(f"a is {a:,f}")
print(f"a is {a:_f}")
```
```
# output
'a is 1,234,567,890.098765'
'a is 1_234_567_890.098765'
```
4. 格式描述符含义
s：普通字符串格式  字符串  
b：二进制整数格式  整数  
c：字符格式，按unicode编码将整数转换为对应字符  整数  
d：十进制整数格式  整数  
o：八进制整数格式  整数  
x：十六进制整数格式（小写字母） 整数  
X：十六进制整数格式（大写字母） 整数  
e/E：科学计数格式，用e或者E来表示数学上的底数10，而后面紧跟次方数用+number或者-number来表示   浮点数、复数、整数（自动转换为浮点数）  
f：定点数格式，默认精度（precision）是6    浮点数、复数、整数（自动转换为浮点数）    
%：百分比格式，数字自动乘上100后按 f 格式排版，并加 % 后缀    浮点数、整数（自动转换为浮点数）  
```python
a = 1234
print(f"a is {a:^#10X}")     # 居中，宽度10位，十六进制整数（大写字母），显示0X前缀
```
```
# output
'a is   0X4D2   '
```
```python
import datetime
e = datetime.datetime.today()
f('the time is {e:%Y-%m-%d (%a) %H:%M:%S}')   # datetime时间格式
```
```
# output
'the time is 2018-07-14 (Sat) 20:46:02'
```
