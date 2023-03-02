# 1 基础知识

## 1.1 注释

```python
print('hello world')

# print('hello Python')  #单行注释

"""
第一行注释
第二行注释
第三行注释
print("you are trash")
print("you are litter")
"""

'''
注释1
注释2
注释3
'''
```

## 1.2 变量

```python
"""
1. 定义变量
    语法：变量名 = 值
2. 使用变量
"""

# 定义变量：存储数据TOM
my_name = 'TOM'
print(my_name)

# 定义变量：存储数据 黑马程序员
schoolName = '我是Dr. 我爱Python'
print(schoolName)
```

## 1.3 认识数据类型

```python
# 01 int -- 整型
num1 = 1
print(type(num1))

# 02 float -- 浮点型，就是小数
num2 = 1.1
print(type(num2))

# 03 str -- 字符串，特点：数据都要带引号
a = 'hello world'
print(type(a))

# 04 bool -- 布尔型，通常判断使用，布尔型有两个取值 True 和 False
b = True
print(type(b))


# 05 list -- 列表
c = [10, 20, 30]
print(type(c))

# 06 tuple -- 元组
d = (10, 20, 30)
print(type(d))

# 07 set -- 集合
e = {10, 20, 30}
print(type(e))


# 08 dict -- 字典 -- 键值对
f = {'name': 'TOM', 'age': 18}
print(type(f))
```

## 1.4 格式化输出

```python
age = 18
name = 'TOM'
weight = 75.5
stu_id = 1
stu_id2 = 1000

# 1. 今年我的年龄是x岁 -- 整数 %d
print('今年我的年龄是%d岁' % age)

# 2. 我的名字是x -- 字符串 %s
print('我的名字是%s' % name)


# 3. 我的体重是x公斤 -- 浮点数 %f
print('我的体重是%.3f公斤' % weight)

# 4. 我的学号是x -- %d
print('我的学号是%d' % stu_id)

# 4.1 我的学号是001
print('我的学号是%03d' % stu_id)
print('我的学号是%03d' % stu_id2)


# 5. 我的名字是x，今年x岁了
print('我的名字是%s，今年%d岁了' % (name, age))
# 5.1 我的名字是x，明年x岁了
print('我的名字是%s，明年%d岁了' % (name, age + 1))


# 6. 我的名字是x，今年x岁了，体重x公斤，学号是x
print('我的名字是%s，今年%d岁了，体重%.2f公斤，学号是%06d' % (name, age, weight, stu_id))
```

## 1.5 f格式化字符串

```python
name = 'TOM'
age = 18

# 我的名字是x，今年x岁了

print('我的名字是%s，今年%s岁了' % (name, age))

# 语法 f'{表达式}'

print(f'我的名字是{name}，今年{age}岁了')
```

## 1.6 转义字符

```python
print('hello')
print('world')

print('hello\nPython')
print('\tabcd')
```

## 1.7 print的结束符

```python
print('elloh\n')
print('hello', end="\n")
print('world', end="\t")
print('hello', end="...")
print('Python')
```

## 1.8 复合值运算

```python
a = 10
a += 1  # a = a + 1
print(a)

b = 10
b -= 1  # b = b - 1
print(b)


# 注意： 先算复合赋值运算符右面的表达式； 再算复合赋值运算
c = 10
# c = 10 + 1 + 2
# c += 3 -- c = c + 3
c += 1 + 2
print(c)

d = 10
d *= 1 + 2
print(d)
```

## 1.9 输入

```python
"""
1. 书写input
    input('提示信息')

2. 观察特点
    2.1 遇到input，等待用户输入
    2.2 接收input存变量
    2.3 input接收到的数据类型都是字符串
"""

password = input('请输入您的密码：')
print(f'您输入的密码是{password}')

print(type(password))
```

## 1.10 逻辑运算符

```python
a = 0
b = 1
c = 2

# 1. and: 与: 都真才真
print((a < b) and (c > b))
print(a > b and c > b)


# 2. or：或 : 一真则真，都假才假
print(a < b or c > b)
print(a > b or c > b)


# 3. not： 非: 取反
print(not False)

print(not c > b)
```

## 1.11 数据类型转换

```python
num = input('请输入数字：')
print(num)

print(type(num))  # str

print(type(int(num)))  # int
```

## 1.12 数据类型转换函数

```python
# 1. float() -- 将数据转换成浮点型
num1 = 1
str1 = '10'
print(type(float(num1)))  # <class 'float'>
print(float(num1))  # 1.0

print(float(str1))  # 10.0


# 2. str() -- 将数据转换成字符串型
print(type(str(num1)))  # <class 'str'>


# 3. tuple() -- 将一个序列转换成元组
list1 = [10, 20, 30] 
print(tuple(list1)) # (10, 20, 30)


# 4. list() -- 将一个序列转换成列表
t1 = (100, 200, 300)
print(list(t1)) # [100, 200, 300]


# 5. eval() -- 计算在字符串中的有效Python表达式,并返回一个对象
str2 = '1'
str3 = '1.1'
str4 = '(1000, 2000, 3000)'
str5 = '[1000, 2000, 3000]'
print(type(eval(str2)))
print(type(eval(str3)))
print(type(eval(str4)))
print(type(eval(str5)))
```

## 1.13 if语句

```python
if False:
    print('条件成立执行的代码1')
    print('条件成立执行的代码2')

# 注意：在这个下方的没有加缩进的代码，不属于if语句块，即和条件成立与否无关
print('这个代码执行吗？')
```

## 1.14 if嵌套

```python
money = 0
seat = 1

if money == 1:
    print('土豪，请上车')

    # 判断是否能坐下

​    if seat == 1:
​        print('有空座，坐下了')
​    else:
​        print('没有空座，站着等....')
else:
​    print('朋友，没带钱，跟着跑，跑快点')
```

## 1.15 猜拳游戏

```python
"""
1. 出拳
    玩家：手动输入
    电脑：1. 固定：剪刀；2. 随机
2. 判断输赢
    2.1 玩家获胜
    2.2 平局
    2.3 电脑获胜
"""
import random

# 1. 出拳
# 玩家
player = int(input('请出拳：0--石头；1--剪刀；2--布：'))
# 电脑
# computer = 1
computer = random.randint(0, 2)
# print(computer)

# 2. 判断输赢
# 玩家获胜
if ((player == 0) and (computer == 1)) or ((player == 1) and (computer == 2)) or ((player == 2) and (computer == 0)):
    print('玩家获胜，哈哈哈哈')
# 平局
elif player == computer:
    print('平局，别走，再来一局')
else:
    print('电脑获胜')
```

##  1.16 随机数

```python
import random

num = random.randint(0, 2)

print(num)
```

## 1.17 三目运算符

```python
a = 1
b = 2

c = a if a > b else b
print(c)

# 需求： 有两个变量，比较大小 如果变量1 大于 变量2 执行 变量 1 - 变量2； 否则 变量2 - 变量1
aa = 10
bb = 6
cc = aa - bb if aa > bb else bb - aa
print(cc)
```

# 2 循环语句

## 2.1 循环

```python
i = 1
while i <= 5:
    print('媳妇儿，我错了')
    i += 1  # i = i + 1
```

## 2.2 循环习惯写法

```python
i = 0
while i < 5:
    print('媳妇儿，我错了')
    i += 1  # i = i + 1

print('原谅你了')
```

## 2.3 1-100累加

```python
# 准备数据
i = 1

# 结果变量
result = 0

# 循环
while i <= 100:
    # 加法运算 前两个数的结果 + 第三个数 -- 每计算一次加法则更新一次result变量值
    result = result + i
    i += 1

# 打印最终结果
print(result)
```

## 2.4 1-100偶数累加 取余

```python
i = 1
result = 0
while i <= 100:
    # 条件语句 -- if
    if i % 2 == 0:
        # 加法运算
        result += i
    i += 1

# 输出结果
print(result)
```

## 2.5 1-100偶数累加 步长

```python
i = 2
result = 0
while i <= 100:
    result += i
    i += 2

print(result)
```

## 2.6 break

```python
i = 1
while i <= 5:
    # 条件：如果吃到4 或 > 3 打印吃饱了不吃了
    if i == 4:
        print('吃饱了，不吃了')
        break # break：当某些条件成立，退出整个循环
    print(f'吃了第{i}个苹果')
    i += 1
```

## 2.7 continue

```python
i = 1
while i <= 5:
    # 条件
    if i == 3:
        print('吃出一个大虫子，这个苹果不吃了')
        # 如果使用continue，在continue之前一定要修改计数器，否则进入死循环
        i += 1
        continue # continue : 当条件成立，退出当前一次循环，继而执行下一次循环
    print(f'吃了第{i}个苹果')
    i += 1
```

## 2.8 打印星号 正方形

```python
"""
1. 打印1个星星
2. 一行5个： 循环 -- 5个星星在一行显示
3. 打印5行星星： 循环 -- 一行5个
"""
j = 0
while j < 5:
    # 一行星星开始
    i = 0
    while i < 5:
        print('*', end='')
        i += 1
    # 一行星星结束：换行显示下一行
    print()
    j += 1
```

## 2.9 打印星号 三角形

```python
j = 0
while j < 5:
    # 一行星星开始
    i = 0
    while i <= j:
        print('*', end='')
        i += 1
    # 一行星星结束：换行显示下一行
    print()
    j += 1
```

## 2.10 九九乘法表

```python
j = 1
while j <= 9:
    # 一行的表达式开始
    i = 1
    while i <= j:
        print(f'{i} * {j} = {i*j}', end='\t')
        i += 1
    # 一行的表达式结束
    print()
    j += 1
```

## 2.11 for循环快速体验

```python
str1 = 'itheima'
for i in str1:
    print(i)
```

## 2.12 break控制for循环

```python
str1 = 'itheima'
for i in str1:
    # 当某些条件成立退出循环 -- break：条件 i取到字符e
    if i == 'e':
        break
    print(i)
```

## 2.13 continue控制for循环

```python
str1 = 'itheima'
for i in str1:
    # 当某些条件成立退出循环 -- continue：条件 i取到字符e
    if i == 'e':
        continue
    print(i)
```

## 2.14 while...else...

```python
i = 1
while i <= 5:
    print('媳妇儿，我错了')
    i += 1
else:
    print('媳妇原谅我了，真开心呐，哈哈哈哈')
```

## 2.15 for...else...

```python
str1 = 'itheima'
for i in str1:
    print(i)
else:
    print('循环正常结束执行的else的代码')
```

# 3 数据——字符串

## 3.1 认识字符串

```python
a = 'hello ' \
    'world'
print(a) # hello world
print(type(a)) # <class 'str'>

b = "TOM"
print(type(b)) # <class 'str'>

# 三引号
e = '''i am TOM'''
print(type(e)) # <class 'str'>

f = """I 
am TOM"""
print(type(f)) # <class 'str'>
print(f) #I
         #am TOM

c = "I'm TOM"
print(c) # I'm TOM
print(type(c)) # <class 'str'>

d = 'I\'m TOM'
print(d) # I'm TOM
print(type(d)) # <class 'str'>
```

## 3.2 字符串的输出

```python
print("hello world")

name = 'ROSE'
# 我的名字是TOM
print('我的名字是%s' % name)
print(f'我的名字是{name}')
```

## 3.3 字符串的输入

```python
# 输入密码
password = input('请输入您的密码：')
print(f'您输入的密码是{password}')
print(type(password))
```

## 3.4 字符串切片

```python
# 序列名[开始位置的下标:结束位置的下标:步长]

str1 = '012345678'
print(str1[2:5:1])  # 234
print(str1[2:5:2])  # 24
print(str1[2:5])  # 234
print(str1[:5])  # 01234 -- 如果不写开始，默认从0开始选取
print(str1[2:])  # 2345678 -- 如果不写结束，表示选取到最后
print(str1[:])  # 012345678 -- 如果不写开始和结束，表示选取所有

# 负数测试
print(str1[::-1])  # 876543210 -- 如果步长为负数，表示倒叙选取
print(str1[-4:-1])  # 567 -- 下标-1表示最后一个数据，依次向前类推

# 终极测试
print(str1[-4:-1:1])  # 567
print(str1[-4:-1:-1])  # 不能选取出数据：从-4开始到-1结束，选取方向为从左到右，但是-1步长：从右向左选取
# **** 如果选取方向(下标开始到结束的方向) 和 步长的方向冲突，则无法选取数据

print(str1[-1:-4:-1])  # 876
```

## 3.5 字符串查找

```python
mystr = "hello world and itcast and itheima and Python"
# 1. find()
print(mystr.find('and'))  # 12
print(mystr.find('and', 15, 30))  # 23
print(mystr.find('ands'))  # -1 , ands子串不存在
print()
# 2.index()
print(mystr.index('and'))  # 12
print(mystr.index('and', 15, 30))  # 23
# print(mystr.index('ands'))  # 如果index查找子串不存在，报错
print()
# 3.count()
print(mystr.count('and', 15, 30)) # 1
print(mystr.count('and'))  # 3
print(mystr.count('ands'))  # 0
print()
# 4.rfind()
print(mystr.rfind('and')) # 35
print(mystr.rfind('ands')) # -1
print()
# 5.rindex()
print(mystr.rindex('and')) # 35
# print(mystr.rindex('ands'))
```

## 3.6 字符串修改Ⅰ

```python
mystr = "hello world and itcast and itheima and Python"

# 1 replace() 全部替换
new_str = mystr.replace('and', 'he')
print(new_str) # hello world he itcast he itheima he Python

# 1.1 替换1次
new_str = mystr.replace('and', 'he', 1)
print(new_str) # hello world he itcast and itheima and Python

# 1.2 替换10次,如果超出子串出现的次数,表示替换所有这个子串
new_str = mystr.replace('and', 'he', 10)
print(new_str) # hello world he itcast he itheima he Python

# ***** 调用了replace函数后，发现原有字符串的数据并没有做到修改，修改后的数据是replace函数的返回值
# --- 说明 字符串是不可变数据类型
# 数据是否可以改变划分为 可变类型 和 不可变类型
print(mystr) # hello world and itcast and itheima and Python

# mystr = "hello world and itcast and itheima and Python"
# 2 split() -- 分割，返回一个列表, 丢失分割字符
# 2.1 and——>，
list1 = mystr.split('and')
print(list1) # ['hello world ', ' itcast ', ' itheima ', ' Python']

# 2.2 分2个
list2 = mystr.split('and', 2) # ['hello world ', ' itcast ', ' itheima and Python']
print(list2)

# 2.3 分3个
list3 = mystr.split('and', 1) # ['hello world ', ' itcast and itheima and Python']
print(list3)

# 3. join() -- 合并列表里面的字符串数据为一个大字符串
mylist = ['aa', 'bb', 'cc']
new_str = '...'.join(mylist)
print(new_str) # aa...bb...cc
```

## 3.7 字符串修改Ⅱ

```python
mystr = "hello world and itcast and itheima and Python"

# 1. capitalize() 字符串首字母大写
new_str = mystr.capitalize()
print(new_str)

# 2.title(): 字符串中每个单词首字母大写
new_str = mystr.title()
print(new_str)

# 3. upper()：小写转大写
new_str = mystr.upper()
print(new_str)

# 4. lower(): 大写转小写
new_str = mystr.lower()
print(new_str)

mystr = "   hello world and itcast and itheima and Python   "
print(mystr)
# 1. lstrip(): 删除左侧空白字符
new_str = mystr.lstrip()
print(new_str)

# 2. rstrip(): 删除右侧空白字符
new_str = mystr.rstrip()
print(new_str)

# 3.strip()：删除两侧空白字符
new_str = mystr.strip()
print(new_str)
```

## 3.8 字符串判断

```python
mystr = "hello world and itcast and itheima and Python"
# 1. startswith(): 判断字符串是否以某个子串开头
print("第1部分")
print(mystr.startswith('hello')) # 1
print(mystr.startswith('hel')) # 1
print(mystr.startswith('hels')) # 0


# 2. endswith(): 判断字符串是否以某个子串结尾
print("第2部分")
print(mystr.endswith('Python')) # 1
print(mystr.endswith('Pythons')) # 0

# 3. isalpha(): 字母
print("第3部分")
print(mystr.isalpha()) #0
mystrx="youshouldloveyourconutry"
print(mystrx.isalpha()) # 1
mystry="youshouldloveyourcountry!"
print(mystry.isalpha()) # 0

# 4. isdigit(): 数字
print("第4部分")
print(mystr.isdigit()) # 0
mystr1 = '12345'
print(mystr1.isdigit()) # 1

# 5. isalnum() : 数字或字母或组合
print("第5部分")
mystr2 = 'abc123'
print(mystr2.isalnum()) # 1


# 6.isspace(): 空白
print("第6部分")
mystr3 = '        '
print(mystr3.isspace()) # 1
```

# 4 数据——列表

## 4.1 下表

```python
name_list = ['TOM', 'Lily', 'ROSE']

print(name_list)

print(name_list[1])
print(name_list[0])
print(name_list[2])
```

 ## 4.2 查找

```python
name_list = ['TOM', 'Lily', 'ROSE']

# 1. index()
print(name_list.index('TOM'))
# print(name_list.index('TOMS'))

# 2. count()
print(name_list.count('TOM'))
print(name_list.count('TOMS'))

# 3.len()
print(len(name_list))
```

## 4.3 判断是否存在

```python
name_list = ['TOM', 'Lily', 'ROSE']

# 1. in
print('TOM' in name_list)
print('TOMS' in name_list)

# 2. not in
print('TOM' not in name_list)
print('TOMs' not in name_list)
```

## 4.4 append——追加整个序列

```python
name_list = ['TOM', 'Lily', 'ROSE']

# name_list.append('xiaoming')
name_list.append([11, 22])

print(name_list)

# 1. 列表数据可改的 -- 列表可变类型
# 2. append函数追加数据的时候如果数据是一个序列，追加整个序列到列表的结尾
```

## 4.5 extend——逐一追加

```python
name_list = ['TOM', 'Lily', 'ROSE']

# name_list.extend('xiaoming')
name_list.extend(['xiaoming', 'xiaohong'])

print(name_list)

# extend() 追加数据是一个序列，把数据序列里面的数据拆开然后逐一追加到列表的结尾
```

## 4.6 insert

```python
name_list = ['TOM', 'Lily', 'ROSE']

# name_list.insert(下标, 数据)
name_list.insert(1, 'aaa')
name_list.insert(3, 'aa')
print(name_list)
```

## 4.7 删除

```python
name_list = ['TOM', 'Lily', 'ROSE']
del name_list # 或者 del(name_list)

name_list = ['TOM', 'Lily', 'ROSE']
del name_list[0]
print(name_list)

name_list = ['TOM', 'Lily', 'ROSE']
name1 = name_list.pop()
print(name1)
name2=name_list.pop()
print(name2)

name_list = ['TOM', 'Lily', 'ROSE']
name1 = name_list.pop(1)
print(name1)

name_list = ['TOM', 'Lily', 'ROSE']
name_list.remove('TOM')
print(name_list)

name_list = ['TOM', 'Lily', 'ROSE']
name_list.clear()
print(name_list)

```

## 4.8 修改

```python
name_list = ['TOM', 'Lily', 'ROSE']

# 1. 修改指定下标的数据
name_list[0] = 'aaa'
print(name_list)


# 2. 逆序 reverse()
list1 = [1, 3, 2, 5, 4, 6]
list1.reverse()
print(list1)

# 3. sort() 排序：升序(默认) 和 降序
list1.sort()
print(list1)
list1.sort(reverse=False)
print(list1)
list1.sort(reverse=True)
print(list1)
```

## 4.9 复制

```python
name_list = ['TOM', 'Lily', 'ROSE']

list1 = name_list.copy()

print(list1)
print(name_list)
```

## 4.10 列表循环-while

```python
name_list = ['TOM', 'Lily', 'ROSE']
i = 0
while i < len(name_list):
    print(name_list[i])
    i += 1
```

## 4.11 列表循环-for

```python
name_list = ['TOM', 'Lily', 'ROSE']
for i in name_list:
    # 遍历序列中的数据
    print(i)
```

## 4.12 列表嵌套

```python
name_list = [['TOM', 'Lily', 'Rose'], ['张三', '李四', '王五'], ['xiaohong', 'xiaoming', 'xiaolv']]

# print(name_list)

# 列表嵌套的时候的数据查询
print(name_list[0])
print(name_list[0][1])
```

## 4.13 随机分配办公室 

```python
# 需求：8位老师，3个办公室， 将8位老师随机分配到3个办公室
"""
步骤：
1. 准备数据
    1.1 8位老师 -- 列表
    1.2 3个办公室 - 列表嵌套

2. 分配老师到办公室
    *** 随机分配
    就是把老师的名字写入到办公室列表 -- 办公室列表追加老师名字数据

3. 验证是否分配成功
    打印办公室详细信息：每个办公室的人数和对应的老师名字
"""

import random

# 1. 准备数据
teachers = ['A', 'B', 'C', 'D', 'E', 'F', 'G', 'H']
offices = [[], [], []]

# 2. 分配老师到办公室 -- 取到每个老师放到办公室列表 -- 遍历老师列表数据
for name in teachers:
    # 列表追加数据 -- append（选中） extend insert
    # xx[0] -- 不能指定是具体某个下标 -- 随机
    num = random.randint(0, 2)
    offices[num].append(name)
# print(num)

# print(offices)

# 为了更贴合生活，把各个办公室子列表加一个办公室编号 1， 2， 3
i = 1
# 3. 验证是否分配成功
for office in offices:
    # 打印办公室人数 -- 子列表数据的个数  len()
    print(f'办公室{i}的人数是{len(office)}，老师分别是：')
    # 打印老师的名字
    # print()  --  每个子列表里面的名字个数不一定 -- 遍历 -- 子列表
    for name in office:
        print(name)

    i += 1
```

# 5 数据——元组

## 5.1 体验元组

```python
t1 = (10, 20, 30)
print(t1)

print(type(t1))
```

## 5.2 定义元组

```python
# 1. 多个数据元组
t1 = (10, 20, 30)
print(type(t1)) # tuple

# 2. 单个数据的元组
t2 = (10,)
print(type(t2)) # tuple 

# 3. 如果单个数据的元组不加逗号
t3 = (10)
print(type(t3))  # int

t4 = ('aaa')
print(type(t4))  # str

t5 = ('aaa',)
print(type(t5)) # tuple
```

## 5.3 元组常见操作

```python
t1 = ('aa', 'bb', 'cc', 'bb')

# 1. 下标
print(t1[0]) # aa

# 2. index()
print(t1.index('bb')) # bb
# print(t1.index('bbb'))

# 3. count()
print(t1.count('aa')) # 1
print(t1.count('aaa')) # 0

# 4. len()
print(len(t1)) # 4
```

## 5.4 元组修改操作

```python
t1 = ('aa', 'bb', 'cc', 'bb')
# t1[0] = 'aaa' # 元组的数据不能被改变

t2 = ('aa', 'bb', ['cc', 'dd'])
print(t2[2]) # ['cc', 'dd']
print(t2[2][0]) # cc
t2[2][0] = 'TOM'
print(t2) # ('aa', 'bb', ['TOM', 'dd'])

t2[2][0]=[1,2]
print(t2) # ('aa', 'bb', [[1, 2], 'dd'])
```

# 6 数据——字典

## 6.1  创建字典

```python
# {}  键值对  各个键值对用逗号隔开

# 1. 有数据的字典： name的值TOM， age的值是20， gender的值是男
dict1 = {'name': 'TOM', 'age': 20, 'gender': '男'}
print(dict1)
print(type(dict1))

# 2. 创建空字典
dict2 = {}
print(type(dict2))

dict3 = dict()
print(type(dict3))
```

## 6.2 字典——新增数据

```python
dict1 = {'name': 'TOM', 'age': 20, 'gender': '男'}

# 字典序列[key] = 值
# id的值是110
dict1['id'] = 110
print(dict1)

dict1['name'] = 'ROSE'
print(dict1)
```

## 6.3 字典——删除数据

```python
dict1 = {'name': 'TOM', 'age': 20, 'gender': '男'}

# del 删除字典或指定的键值对
# del(dict1)
print(dict1)

del dict1['name']
# del dict1['names']  # 报错
print(dict1)

# clear()
dict1.clear()
print(dict1)
```

## 6.4 字典——修改数据

```python
dict1 = {'name': 'TOM', 'age': 20, 'gender': '男'}

dict1['name'] = 'Lily'
print(dict1)

dict1['id'] = 110
print(dict1)
```

 ## 6.5 字典——查找数据

```python
dict1 = {'name': 'TOM', 'age': 20, 'gender': '男'}

# 1. [key]
print(dict1['name'])  # 返回对应的值(key存在) # TOM
# print(dict1['names'])

# 2. 函数
# 2.1 get()
print(dict1.get('name')) # TOM
print(dict1.get('names'))  # 如果key不存在，返回None
print(dict1.get('names', 'Lily'))

# 2.2 keys() 查找字典中所有的key，返回可迭代对象
print(dict1.keys())

# 2.3 values() 查找字典中的所有的value，返回可迭代对象
print(dict1.values())

# 2.4 items() 查找字典中所有的键值对，返回可迭代对象，里面的数据是元组，元组数据1是字典的key，元组数据2是字典key对应的值
print(dict1.items())
```

## 6.6 字典遍历——key

```python
dict1 = {'name': 'TOM', 'age': 20, 'gender': '男'}

for key in dict1.keys():
    print(key)
```

## 6.7 字典遍历——value

```python
dict1 = {'name': 'TOM', 'age': 20, 'gender': '男'}

for value in dict1.values():
    print(value)
```

## 6.8 字典遍历——item

```python
dict1 = {'name': 'TOM', 'age': 20, 'gender': '男'}

for item in dict1.items():
    print(item)
```

## 6.8 字典遍历——拆包

```python
dict1 = {'name': 'TOM', 'age': 20, 'gender': '男'}

# xx.items(): 返回可迭代对象，内部是元组，元组有2个数据
# 元组数据1是字典的key，元组数据2是字典的value
for key, value in dict1.items():
    print(key)
    print(value)
    # 目标： key=value
    print(f'{key}={value}')
```

# 7 数据——集合

## 7.1 创建集合

```python
# 1. 创建有数据的集合
s1 = {10, 20, 30, 40, 50}
print(s1) # {50, 20, 40, 10, 30}

s2 = {10, 30, 20, 40, 30, 20}
print(s2) # {40, 10, 20, 30}

s3 = set('abcdefg')
print(s3) # {'a', 'f', 'g', 'c', 'e', 'b', 'd'}

# 2. 创建空集合: set()
s4 = set()
print(s4) # set()
sx={}
print(sx) # {}
print(type(s4)) # <class 'set'>
print(type(sx)) # <class 'dict'>

s5 = {}
print(type(s5)) # <class 'dict'>

s6 = {11,34,55}
print(type(s6)) # <class 'set'>
```

 ## 7.2 集合——增加数据

```python
s1 = {10, 20}
# 1. 集合是可变类型
# add()
s1.add(100)
print(s1) # {100, 10, 20}

# 集合有去重功能，如果追加的数据是集合已有数据，则什么事情都不做
s1.add(100)
print(s1) # {100, 10, 20}

# s1.add([10, 20, 30])  # 报错
# print(s1)

# update()： 增加的数据是序列
s1.update([10, 20, 30, 40, 50]) #列表可以
print(s1) # {100, 40, 10, 50, 20, 30}

# s1.update(100)  # 报错
# print(s1)

s1.update({-10,-20}) # 集合也可以
print(s1)
```

## 7.3 集合——删除数据

```python
s1 = {10, 20, 30, 40, 50}

# remove(): 删除指定数据，如果数据不存在报错
s1.remove(10)
print(s1) # {50, 20, 40, 30}

# s1.remove(10)  # 报错
# print(s1)

# discard()：删除指定数据，如果数据不存在不报错
s1.discard(10)
print(s1) # {50, 20, 40, 30}
#
s1.discard(10)
print(s1) # {50, 20, 40, 30}

# pop(): 随机删除某个数据，并返回这个数据
del_num = s1.pop()
print(del_num) # 
print(s1)
```

## 7.4 集合——查找数据

```python
s1 = {10, 20, 30, 40, 50}

# in 或not in 判断数据10是否存在
print(10 in s1) # True

print(10 not in s1) # False
```

# 8 数据——公共操作

## 8.1 运算符——加号

```python
str1 = 'aa'
str2 = 'bb'

list1 = [1, 2]
list2 = [10, 20]

t1 = (1, 2)
t2 = (10, 20)

dict1 = {'name': 'Python'}
dict2 = {'age': 30}

# +: 合并
print(str1 + str2)
print(list1 + list2)
print(t1 + t2)

# print(dict1 + dict2)  # 报错：字典不支持合并运算
```

## 8.2 运算符——乘号

```python
str1 = 'a'
list1 = ['hello']
t1 = ('world',)
x={1:'you',2:'he',3:'me'}
# *:复制
print(str1 * 5) # aaaaa

# 打印10个-：
print('-' * 10) # ----------

print(list1 * 5) # ['hello', 'hello', 'hello', 'hello', 'hello']

print(t1 * 5) # ('world', 'world', 'world', 'world', 'world')

print(x * 3) #字典不能这么玩耍
```

## 8.3 运算符——判别是否存在

```python
str1 = 'abcd'
list1 = [10, 20, 30, 40]
t1 = (100, 200, 300, 400)
dict1 = {'name': 'Python', 'age': 30}

# in 和 not in
# 1. 字符a是否存在
print('a' in str1) # True
print('a' not in str1) # False

# 2. 数据10是否存在
print(10 in list1) # True
print(10 not in list1) # False

# 3. 100是否存在
print(100 not in t1) # False
print(100 in t1) #True

# 4. name是否存在
print('name' in dict1) # True
print('name' not in dict1) # False
print('name' in dict1.keys()) # True
print('name' in dict1.values()) # False
```

## 8.4 len

```python
str1 = 'abcdefg' # 字符串 7
list1 = [10, 10, 10, 40, 50] # 5
t1 = (10, 20, 30, 40, 50) # 5
s1 = {10, 20, 10, 10, 50} # 3
dict1 = {'name': 'TOM', 'age': 18} # 2

print(len(str1)) # 7

print(len(list1)) # 5

print(len(t1)) # 5

print(len(s1)) # 3

print(len(dict1)) # 2
```

## 8.5 del

```python
str1 = 'abcdefg'
list1 = [10, 20, 30, 40, 50]
t1 = (10, 20, 30, 40, 50)
s1 = {10, 20, 30, 40, 50}
dict1 = {'name': 'TOM', 'age': 18}

# del 目标 或del(目标)
# del str1
print(str1) # abcdefg

# del(list1)
# print(list1)
del(list1[0])
print(list1) # [20, 30, 40, 50]

# del s1
print(s1) # {50, 20, 40, 10, 30}
# del dict1
# print(dict1)
del dict1['name']
print(dict1) # {'age': 18}
```

## 8.6 max 和 min

```python
str1 = 'abcdefg'
list1 = [10, 20, 30, 40, 50]

# max() : 最大值
print(max(str1)) # g
print(max(list1)) # 50

# min() ： 最小值
print(min(str1)) # a
print(min(list1)) # 10
```

## 8.7 range

```python
# range(start, end, step)
print(range(1, 10, 1)) # range(1, 10)

# 1 2 3 4 5 6 7 8 9
for i in range(1, 10, 1):
    print(i, end=' ')
print()

# 1 2 3 4 5 6 7 8 9
for i in range(1, 10):
    print(i, end=' ')
print()
# 1 3 5 7 9
for i in range(1, 10, 2):
    print(i, end=" ")
print()

# 1. 如果不写开始，默认从0开始
# 2. 如果不写步长，默认为1
# 0 1 2 3 4 5 6 7 8 9
for i in range(10):
    print(i, end=" ")
```

## 8.8 enumerate

```python
list1 = ['a', 'b', 'c', 'd', 'e']

# enumerate 返回结果是元组，元组第一个数据是原迭代对象的数据对应的下标，元组第二个数据是原迭代对象的数据
for i in enumerate(list1):
    print(i, end=" ")
print()

for i in enumerate(list1, start=1):
    print(i,end=' ')
```

## 8.9 数据类型的转换

```python
list1 = [10, 20, 30, 20, 40, 50]
s1 = {100, 300, 200, 500, 200}
t1 = ('a', 'b', 'c', 'd', 'e')

# tuple(): 转换成元组
print(tuple(list1)) # (10, 20, 30, 20, 40, 50)
print(tuple(s1)) # (200, 100, 500, 300)

# list()：转换成列表
print(list(s1)) # [200, 100, 500, 300]
print(list(t1)) # ['a', 'b', 'c', 'd', 'e']

# set()：转换成集合
print(set(list1)) # {40, 10, 50, 20, 30}
print(set(t1)) # {'a', 'e', 'c', 'd', 'b'}
```

# 9 数据——推导式

## 9.1 推导式——初体验

```python
# while实现-------------
list1 = []

i = 0
while i < 10:
    list1.append(i)
    i += 1

print(list1)

# for 实现--------------
list1 = []
for i in range(10):
    list1.append(i)

print(list1)

# 列表推导式实现------------------------
list1 = [i for i in range(10)]
print(list1)
```

## 9.2 推导式——if

```python
# 需求：0-10偶数数据的列表
# 1. 简单列表推导式 range步长
list1 = [i for i in range(0, 10, 2)]
print(list1) # [0, 2, 4, 6, 8]

# 2. for循环加if 创建有规律的列表
list2 = []
for i in range(10):
    if i % 2 == 0:
        list2.append(i)
print(list2) # [0, 2, 4, 6, 8]

# 3. 把for循环配合if的代码 改写 带if的列表推导式
list3 = [i for i in range(10) if i % 2 == 0]
print(list3) # [0, 2, 4, 6, 8]
```

## 9.3 推导式——for

```python
# [(1, 0), (1, 1), (1, 2), (2, 0), (2, 1), (2, 2)]
# 数据1 ： 1 和 2  range(1,3)
# 数据2 ：0 1 2  range(3)
list1 = []
for i in range(1, 3): # i = 1 2
    for j in range(3): # j = 0 1 2
        # 列表里面追加元组： 循环前准备一个空列表，然后这里追加元组数据到列表
        list1.append((i, j))
print(list1)

# 多个for实现列表推导式
list2 = [(i, j) for i in range(1, 3) for j in range(3)]
print(list2)

# 多for的列表推导式等同于for循环嵌套
```

## 9.4 推导式——体验字典

```python
dict1 = {i: i**2 for i in range(1, 10)}
print(dict1)
```

## 9.5 合并列表为字典

```python
list1 = ['name', 'age', 'gender', 'id']
list2 = ['Tom', 20, 'man']

dict1 = {list1[i]: list2[i] for i in range(len(list2))}
print(dict1)

# 总结：
# 1. 如果两个列表数据个数相同，len统计任何一个列表的长度都可以
# 2. 如果两个列表数据个数不同，len统计数据多的列表数据个数会报错；len统计数据少的列表数据个数不会报错
```

## 9.6 提取字典中的目标数据

```python
counts = {'MBP': 268, 'HP': 125, 'DELL': 201, 'Lenovo': 199, 'acer': 99}

# 1. 需求：提取电脑台数大于等于200
# 获取所有键值对数据，判断v值大于等于200 返回  字典
# print(counts.items())
dict1 = {key: value for key, value in counts.items() if value >= 200}
print(dict1)
```

## 9.7 推导式——集合

```python
list1 = [-1, 1, -2, 2]

set1 = {i ** 2 for i in list1}
print(set1)
# 集合有去重功能所以这个集合数据只有两个数据分别是1, 4
```

# 10 初级函数

## 10.1 体验函数

```python
# 因为函数要先定义再调用，所以步骤2和3要在步骤1的上面书写
# 2. 确定选择功能界面： 显示余额 存款 取款； # 3. 封装函数

def sel_func():
    print('显示余额')
    print('存款')
    print('取款')

# 1. 搭建整体框架
"""
输入密码登录后显示功能； 查询余额后显示功能； 取完钱后显示功能
"""
print('恭喜您登录成功')
# 显示功能界面# 4. 在需要的位置调用函数
sel_func()

print('您的余额是10000000')
# 显示功能界面# 4. 在需要的位置调用函数
sel_func()

print('取了100元钱')
# 显示功能界面# 4. 在需要的位置调用函数
sel_func()
```

## 10.2 函数的注意事项

```python
# 1. 使用一个函数 2.测试注意事项
# 需求：一个函数：打印hello world

# info_print()  # 报错


# 定义函数
def info_print():
    print('hello world')


# 调用函数
info_print()


"""
结论：
1. 函数先定义后调用，如果先调用会报错
2. 如果没有调用函数，函数里面的代码不会执行
3. 函数执行流程***
    当调用函数的时候，解释器回到定义函数的地方去执行下方缩进的代码，当这些代码执行完，回到调用函数的地方继续向下执行
    定义函数的时候，函数体内部缩进的代码并没有执行
"""
```

## 10.3 函数的参数

```python
# 1. 函数：固定数据1 和 2 加法
def add_num1():
    result = 1 + 2
    print(result)
add_num1()

# 2. 参数形式传入真实数据  做加法运算
def add_num2(a, b):
    result = a + b
    print(result)
add_num2(10, 20)
add_num2(100, 200)

# add_num2(100)  # 报错，定义函数有2个参数，传入数据也要是2个
```

## 10.4 体验函数的返回值

```python
# 定义一个函数，返回 烟
def buy():
    return '烟'

goods = buy()
print(goods)

# return返回结果给函数调用的地方
```

## 10.5 return的特点

```python
def buy():
    # return '烟'
    print('ok')


goods = buy() # ok
print(goods) # None

buy() # ok

"""
return 作用：
1. 负责函数返回值
2. 退出当前函数：导致return下方的所有代码(函数体内部)不执行
"""
```

## 10.6 函数返回值的应用

```python
# 需求： 制作计算器：计算任意两个数字的加法的结果，并返回结果
"""
1. 定义函数：2个参数 和 return返回值
2. 调用函数，传入2个真实数据 -- 这里即有返回值结果，打印这个结果即可
"""


def sum_num(a, b):
    return a + b


result = sum_num(1, 2)
print(result)
```

## 10.7 函数的说明文档

```python
help(len)  # help函数作用：查看函数的说明文档(函数的解释说明的信息)

def sum_num(a, b):
    """求和函数"""
    return a + b

help(sum_num)

# 函数的说明文档的高级使用
def sum_num1(a, b):
    """
    求和函数sum_num1
    :param a: 参数1
    :param b: 参数2
    :return: 返回值
    """
    return a + b

help(sum_num1)
```

## 10.8 函数的嵌套调用

```python
# 两个函数 testA 和 testB  -- 在A里面嵌套调用B

# B函数
def testB():
    print()
    print('B函数开始-----')
    print('这是B函数')
    print('B函数结束-----')

# A函数
def testA():
    print()
    print('A函数开始-----')
    # 嵌套调用B
    testB()
    print('A函数结束-----')
    
test(A)
```

## 10.9 函数嵌套调用——打印横线图形

```python
# 1. 打印一条横线
def print_line():
    print('-' * 20)

# 2. 函数嵌套调用 实现多条横线
def print_lines(num):
    i = 0
    while i < num:
        print_line()
        i += 1

print_lines(5)
```

## 10.10 函数嵌套调用——函数计算

```python
# 1. 任意三个数之和
def sum_num(a, b, c):
    return a + b + c

result = sum_num(1, 2, 3)
print(result) # 6


# 2. 任意三个数求平均值
def average_num(a, b, c):
    sumResult = sum_num(a, b, c)
    return sumResult / 5

averageResult = average_num(1, 2, 3)
print(averageResult) # 1.2
```

# 11 中级函数

## 11.1 局部变量

```python
# 定义一个函数，声明一个变量：函数体内部访问、函数体外面访问
def testA():
    a = 100
    print(a)  # 函数体内部访问，能访问到a变量

testA()
# print(a)  # 报错： a变量是函数内部的变量，函数外部无法访问 -- a是一个局部变量

```

## 11.2 全局变量

```python
# 声明全局变量：函数体内外都能访问
a = 100

print(a)

def testA():
    print(a)

def testB():
    print(a)

def testC():
    print(a)

testA()
testB()
testC()
```

## 11.3 全局变量——global

```python
a = 100
print(a)  # 100

def boge1():
    print(a)

def boge2():
    a = 200
    print(a)

    global b
    b = -3
    print(b) # -3

boge1() # 100
boge2() # 200

print(b) # -3

"""
总结：
    1. 如果在函数里面直接把变量a=200赋值，此时的a不是全局变量的修改，而是相当于在函数内部声明了一个新的局部变量
    2. 函数体内部修改全局变量： 先global声明a为全局变量，然后再变量重新赋值
"""
```

## 11.4 多函数执行

```python
# 1. 声明全局变量；
# 2. 定义两个函数；
# 3. 函数1修改全局变量；
# 4. 函数2访问全局变量
glo_num = 0

def demo1():
    global glo_num
    glo_num = 100

def demo2():
    print(glo_num)

print(glo_num)  # 0 函数demo1()没执行

demo2()  # 0 函数demo1()没执行
demo1()  # glo_num=100 函数demo1()执行
demo2()  # 100，因为函数demo1()已经执行

print(glo_num)  # 100，因为函数demo1()已经执行
```

## 11.5 返回值作为参数传递

```python
# 1. 定义两个函数；
# 2. 函数1有返回值50；
# 3. 函数2把返回值50作为参数传入(定义函数2要有形参)

def t1():
    return 50

def t2(num):
    print(num)

# 先得到函数一的返回值，再把这个返回值传入到函数二
result = t1() # result=50
print(result) # 50

t2(result) # 50 调用t2()
```

## 11.6 多返回值

```python
# 需求：一个函数有两个返回值1和2
# 一个函数如果有多个return不能都执行，只执行第一个return：无法做法一个函数多个返回值

def return_num():
    return 1
    return 2

result = return_num() # result=1
print(result) # 1


# 一个函数多个返回值的写法
def return_num():
    return 1, 2   # 返回的是元组 # (1,2)
    # return后面可以直接书写 元组 列表 字典，返回多个值
    return (10, 20) # (10, 20)
    return [100, 200] # [100, 200]
    return {'name': 'Python', 'age': 30} # {'name': 'Python', 'age': 30}

result = return_num()
print(result)
```

## 11.7 参数——位置参数

```python
# 需求：函数3个参数name，age，gender
def user_info(name, age, gender):
    print(f'您的姓名是{name}, 年龄是{age}, 性别是{gender}')

# user_info('TOM', 20)  # 个数定义和传入不一致会报错
user_info(20, 'TOM', '男')  # 顺序也和定义必须是一致的，否则导致数据无意义
```

## 11.8 参数——关键字参数

```python
def user_info(name, age, gender):
    print(f'您的姓名是{name}, 年龄是{age}, 性别是{gender}')

# 调用函数传参
user_info('ROSE', age=20, gender='女')

user_info('小明', gender='男', age=18)  # 关键字参数之间不分先后顺序
# 位置参数必须写在关键字参数的前面
# user_info(age=20, gender='男', 'TOM') # 错误
```

## 11.9 参数——缺省参数

```python
def user_info(name, age, gender='男'):
    print(f'您的姓名是{name}, 年龄是{age}, 性别是{gender}')


user_info('TOM', 18)  # 没有为缺省参数传值，表示使用默认值
user_info('TOM', 18, gender='女')  # 为缺省参数传值，使用这个值，即修改了默认值
```

## 11.10 不定长参数——位置参数

```python
# 接收所有位置参数，返回一个元组
def user_info(*args):
    print(args)

user_info('TOM') # ('TOM',)
user_info('TOM', 20) # ('TOM', 20)
user_info('TOM', 20, 'man') # ('TOM', 20, 'man')
user_info() # ()
user_info([1,2,3,4]) # ([1, 2, 3, 4],)
user_info({1,2,3,4}) # ({1, 2, 3, 4},)
user_info((1,2,3,4)) # ((1, 2, 3, 4),)
user_info((1,),[2,],{3,4,5,3,3,3,3},) #((1,), [2], {3, 4, 5})
```

## 11.11 不定长参数——关键字参数

```python
# 收集所有关键字参数，返回一个字典
def user_info(**kwargs):
    print(kwargs)

user_info()  # {}
user_info(name='TOM')  # {'name': 'TOM'}
user_info(name='TOM', age=20)  # {'name': 'TOM', 'age': 20}
user_info(name='TOM', age=20, sex='man')  # {'name': 'TOM', 'age': 20, 'sex': 'man'}

user_info(name=[1, 2, 3, 4])  # {'name': [1, 2, 3, 4]}
user_info(age={1, 2, 3, 4})  # {'age': {1, 2, 3, 4}}
user_info(name=['Dr.', 'Lee'], age=(1, 2, 3, 4))  # {'name': ['Dr.', 'Lee'], 'age': (1, 2, 3, 4)}
user_info(one=(1,), two=[2, ], three={3, 4, 5, 3, 3, 3, 3}, )  # {'one': (1,), 'two': [2], 'three': {3, 4, 5}}
```

## 11.12 拆包

```python
# 1. 拆包元组数据
#返回元组 （100，200）
def return_num():
    return 100, 200

result = return_num()
print(result) # (100,200)

num1, num2 = return_num()
print(num1) # 100
print(num2) # 200


# 2. 字典数据拆包: 变量存储的数据是key值
# 先准备字典，然后拆包
dict1 = {'name': 'TOM', 'age': 20}
# dict1中有两个键值对，拆包的时候用两个变量接收数据
a, b = dict1
print("a=%s" % a)
print("b=%s" % b)

# v值
print("key=a, value=%s" % dict1[a])
print("key=b ,value=%s" % dict1[b])
```

## 11.3 交换变量的值

```python
a = 10
b = 20

# 1. 方法一
"""
1.1 定义中间的第三变量，为了临时存储a或b的数据
1.2 把a的数据存储到c，做保存
1.3 把b的数据赋值到a， a = 20
1.4 把c的数据赋值到b， b = 10
"""
c = 0 # c=0
c = a # c=10
a = b # a=20
b = c # b=10

print(a) # 20
print(b) # 10

a, b = 1, 2
print(a) # 1
print(b) # 2

a, b = b, a
print(a) # 2
print(b) # 1
```

## 11.4 了解引用

```python
# 1.数字
a=1
b=a
b=2
print(id(a)==id(b)) # False 此时b=2，需要另外开辟一块地址

b=1
print(id(a)==id(b)) # True


# 2.列表
a=[10,20,30]
b=a
b.append(40)
print(a) # [10, 20, 30, 40]
print(b) # [10, 20, 30, 40]
print(id(a)==id(b)) # True

b.remove(30)
print(a) # [10, 20, 40]
print(b) # [10, 20, 40]
print(id(a)==id(b)) # True
```

## 11.5 引用当作实参

```python
# 需求：引用是否可以当做实参
"""
1. 定义函数： 有形参
    1.1 访问打印形参看是否有数据
    1.2 访问形参的id
    1.3 改变形参的数据，查看这个形参并打印id，看id值是否相同
2. 调用函数 -- 把可变和不可变两种类型依次当做实参传入
"""
#函数定义-----------------------------
def t1(a):
    print(a)
    print(id(a))

    a += a
    print(a)
    print(id(a))
#函数定义-----------------------------

b = 100
t1(b)
''''''
def t1(a):
    print(a) # 100
    print(id(a)) # 1875002938832

    a += a
    print(a) # 200
    print(id(a)) # 1875002942096
''''''

c = [11, 22]
t1(c)
''''''
def t1(a):
    print(a) # [11, 22]
    print(id(a)) # 1875056811456

    a += a
    print(a) # [11, 22, 11, 22]
    print(id(a)) # 1875056811456
''''''
```

# 12 文件操作

```python
'r':默认值，表示从文件读取数据。
'w':表示要向文件写入数据，并截断以前的内容
'a':表示要向文件写入数据，添加到当前内容尾部
'r+':表示对文件进行可读写操作（删除以前的所有数据）
'r+a'：表示对文件可进行读写操作（添加到当前文件尾部）
'b':表示要读写二进制数据
```



## 12.1 文件操作——体验

```python
# 1. 打开 open()
f = open('testdemo.txt', 'w')

# 2. 读写操作 write() read()
f.write('you should not choose to die,because you are the one I love!')

# 3. 关闭 close()
f.close()
```

## 12.2 主访问模式

```python
"""
测试目标
1. 访问模式对文件的影响
2. 访问模式对write()的影响
3. 访问模式是否可以省略
"""

# r: 如果文件不存在，报错；不支持写入操作，表示只读
f = open('test1.txt', 'r')
f = open('test2.txt', 'r')
# f.write('aa') #
f.close()

# w：只写, 如果文件不存在，新建文件；执行写入，会覆盖原有内容
f = open('1.txt', 'w')
f.write('bbb')
f.close()

# a：追加，如果文件不存在，新建文件；在原有内容基础上，追加新内容
f = open('2.txt', 'a')
f.write('xyz')
f.close()

# 访问模式参数可以省略, 如果省略表示访问模式为r
f = open('demo.txt')
f.close()
```

## 12.3 读取函数——read

```python
# 假定test.txt中的文字是：This is a demo test!
"""
This is a
demo test
    !
"""
f = open('test.txt')

# 文件内容如果换行，底层有\n，会有字节占位，导致read书写参数读取出来的眼睛看到的个数和参数值不匹配
# read不写参数表示读取所有；

print(f.read(10)) # This is a
```

## 12.4 读取函数——readlines

```python
#readlines()方法读取整个文件所有行，保存在一个列表(list)变量中，每行作为一个元素，但读取大文件会比较占内存
"""
This is a
demo test
    !
"""
f = open('test.txt', 'r')

con = f.readlines()
print(con) # ['This is a\n', 'demo test\n', '    !']

f.close()
```

## 12.5 读取函数——readline

```python
#readline()方法每次读出一行内容，读取时占用内存小，比较适合大文件，该方法返回一个字符串对象。
"""
This is a
demo test
    !
"""
f = open('test.txt', 'r')

con = f.readline()
print(con) # This is a

con = f.readline()
print(con) # demo test

con = f.readline()
print(con) #     !

f.close()
```

## 12.6 访问模式特点

```python
# w+: 没有该文件会新建文件
#文件指针在开头，用新内容覆盖原内容
f = open('test.txt', 'w+')

# a+:没有该文件会新建文件
#文件指针在结尾，无法读取数据(文件指针后面没有数据)
f = open('test.txt', 'a+')

# r+:  没有该文件则报错
# 文件指针在开头，能读取数据
f = open('test.txt', 'r+')

con = f.read()
print(con)
f.close()
```

## 12.7 tell()函数——指针位置

```python
"""
http://c.biancheng.net
"""
f = open("a.txt",'r')
print(f.tell()) # 0
print(f.read(3)) # htt
print(f.tell()) # 3
"""
当使用 open() 函数打开文件时，文件指针的起始位置为 0，表示位于文件的开头处;
当使用 read() 函数从文件中读取 3 个字符之后，文件指针同时向后移动了 3 个字符的位置。
"""
```

## 12.8 seek()函数

```python
"""
http://c.biancheng.net
"""
"""
seek() 函数用于将文件指针移动至指定位置
该函数的语法格式如下：
file.seek(offset[, whence])
file：表示文件对象；
whence：作为可选参数，用于指定文件指针要放置的位置，该参数的参数值有 3 个选择：
0 代表文件头（默认值）、1 代表当前位置、2 代表文件尾。
offset：表示相对于 whence 位置文件指针的偏移量，正数表示向后偏移，负数表示向前偏移。
例如:
当whence == 0 &&offset == 3（即 seek(3,0) ），表示文件指针移动至距离文件开头处 3 个字符的位置
当whence == 1 &&offset == 5（即 seek(5,1) ），表示文件指针向后移动，移动至距离当前位置 5 个字符处。
"""
f = open('a.txt', 'r')

# 判断文件指针的位置
print(f.tell()) # 0

# 读取一个字节，文件指针自动后移1个数据
print(f.read(2)) # ht
print(f.tell()) # 2

# 将文件指针从文件开头，向后移动到 5 个字符的位置
f.seek(5, 0)
print(f.tell()) # 5
print(f.read(1)) # /

# 将文件指针从当前位置，向后移动到 5 个字符的位置
# f.seek(5, 1)
# print(f.tell()) #
# print(f.read(1)) #

# 将文件指针从文件结尾，向前移动到距离 2 个字符的位置
# f.seek(-1, 2)
# print(f.tell()) #
# print(f.read(1)) #
```

## 12.9 MP3文件备份

```python
# 1. 用户输入目标文件  sound.mp3
# 实现准备一个名叫 sound.mp3 的英语片段
old_name = input('请输入您要备份的文件名：') # sound.mp3
print(old_name) # sound.mp3
print(type(old_name)) # <class 'str'>

# 2. 规划备份文件的名字
# 2.1 提取后缀 -- 找到名字中的点 -- 名字和后缀分离--最右侧的点才是后缀的点 -- 字符串查找某个子串rfind
index = old_name.rfind('.')
print(index) # 5

# 思考：有效文件才备份 .txt
if index > 0:
    # 提取后缀
    postfix = old_name[index:] # 提取mp3

# 2.2 组织新名字 = 原名字 + [备份] + 后缀
# 原名字就是字符串中的一部分子串 -- 切片[开始:结束:步长]
print(old_name[:index]) # sound
print(old_name[index:]) # .mp3

new_name = old_name[:index] + 'copy' + old_name[index:]
new_name = old_name[:index] + 'copy' + postfix

print(new_name) # soundcopy.mp3

# 3. 备份文件写入数据(数据和原文件一样)
# 3.1 打开 原文件 和 备份文件
old_f = open(old_name, 'rb') # 表示从文件读取数据
new_f = open(new_name, 'wb') # 表示要向文件写入数据，并截断以前的内容

# 3.2 原文件读取，备份文件写入
# 如果不确定目标文件大小，循环读取写入，当读取出来的数据没有了终止循环
while True:
    con = old_f.read(1024)
    if len(con) == 0:
        # 表示读取完成了
        break

    new_f.write(con)

# 3.3 关闭文件
old_f.close()
new_f.close()
```

## 12.10 文件和文件夹操作

```python
"""
1. 导入模块os
2. 使用模块内功能
"""
import os
'''
# 1. rename(): 重命名
os.rename('demo.txt', 'demoxdrlee.txt')
# 2. remove(): 删除文件
os.remove('demoxdrlee.txt')
'''
#
# 3. mkdir()：创建文件夹
# os.mkdir('you')

#
# 4.rmdir(): 删除文件夹
# os.rmdir('you')

# 5. getcwd(): 返回当前文件所在目录路径
# print(os.getcwd())

# 6. chdir():改变目录路径
# os.mkdir('you')
# os.mkdir('me')
#
# os.mkdir('you')
os.chdir('you')
# os.mkdir('me')
print(os.getcwd())

# # 7. listdir(): 获取某个文件夹下所有文件，返回一个列表
print(os.listdir())
```

## 12.11 批量文件夹命名

```python
# 需求:把code文件夹所有文件重命名 Python_xxxx
import os

# 1. 找到所有文件： 获取code文件夹的目录列表 -- listdir()
os.chdir('code')
print(os.getcwd()) # D:\BaiduSyncdisk\about python\06-文件操作\code
file_list = os.listdir()
print(file_list) # ['0', '1', '2', '3', '4', '5', '6', '7', '8']

# 2. 构造名字
for i in file_list:
        new_name = 'Python_' + i
        os.rename(i,new_name)

print(file_list) # ['Python_0', 'Python_1', 'Python_2', 'Python_3', 'Python_4', 'Python_5', 'Python_6', 'Python_7', 'Python_8']
```

# 13 面向对象——基础

## 13.1 体验面向对象

```python
# 需求：洗衣机，功能：能洗衣服
# 1. 定义洗衣机类
"""
class 类名():
    代码
"""

class Washer():
    def wash(self):
        print('能洗衣服')

# 2. 创建对象
# 对象名 =  类名()
haier = Washer()

# 3. 验证成果
# 打印haier对象
print(haier) # <__main__.Washer object at 0x0000017104A12C50>

# 使用wash功能 -- 实例方法/对象方法 -- 对象名.Wash()
haier.wash() # 能洗衣服
```

## 13.2 self指的是调用该函数的对象

```python
# 类：洗衣机 功能 洗衣服
class Washer():
    def wash(self):
        print('洗衣服')
        print(self)


haier = Washer() # 创建haier对象
print(haier) # <__main__.Washer object at 0x000001DCF35F2C50>

haier.wash()
"""
print('洗衣服') # 洗衣服
print(self) # <__main__.Washer object at 0x000002C0C6B92C50>
"""

# 由于打印对象和打印self得到的内存地址相同，所以self指的是调用该函数的对象
```

## 13.3 一个类可以创建多个对象

```python
# 1. 一个类可以创建多个对象； 2. 多个对象都调用函数的时候，self地址是否相同
class Washer():
    def wash(self):
        print('洗衣服')
        print(self)


haier1 = Washer()
haier1.wash()
# 洗衣服
# <__main__.Washer object at 0x00000269F2912C50>

haier2 = Washer()
haier2.wash()
# 洗衣服
# <__main__.Washer object at 0x00000269F2912FB0>
```

## 13.4 类外面——获取对象属性

```python
class Washer():
    def wash(self):
        print('洗衣服')


haier1 = Washer()

# 添加属性  对象名.属性名 = 值
haier1.width = 400
haier1.height = 500

# 获取属性 对象名.属性名
print(f'洗衣机的宽度是{haier1.width}') # 洗衣机的宽度是400
print(f'洗衣机的高度是{haier1.height}' # 洗衣机的高度是500
```

## 13.5 类里面——获取对象属性

```python
class Washer():
    def wash(self):
        print('洗衣服')

    # 获取实例属性
    def print_info(self):
        # self.属性名
        # print(self.width)
        print(f'洗衣机的宽度是{self.width}')
        print(f'洗衣机的高度是{self.height}')

haier1 = Washer()

# 添加属性
haier1.width = 400
haier1.height = 500

# 对象调用实例方法
haier1.print_info()
# 洗衣机的宽度是400
# 洗衣机的高度是500
```

## 13.6 类初始化——init

```python
# 目标： 定义init魔法方法设置初始化属性 并访问调用
"""
1. 定义类
    init魔法方法： width 和 height
    添加实例方法：访问实例属性

2. 创建对象
3. 验证成果
    调用实例方法
"""

class Washer():
    def __init__(self):
        # 添加实例属性
        self.width = 500
        self.height = 800

    def print_info(self):
        print(f'洗衣机的宽度是{self.width}')
        print(f'洗衣机的高度是{self.height}')


haier = Washer()

haier.print_info()
# 洗衣机的宽度是500
# 洗衣机的高度是800
```

## 13.7 类初始化——init (带参数)

```python
# 1. 定义类：带参数的init：宽度和高度； 实例方法：调用实例属性
class Washer():
    def __init__(self, width, height):
        self.width = width
        self.height = height

    def print_info(self):
        print(f'洗衣机的宽度是{self.width}, 洗衣机的高度是{self.height}')


# 2. 创建对象，创建多个对象且属性值不同；调用实例方法
haier1 = Washer(10, 20)
haier1.print_info() # 洗衣机的宽度是10, 洗衣机的高度是20

haier2 = Washer(100, 200) # 洗衣机的宽度是100, 洗衣机的高度是200
haier2.print_info()
```

## 13.8 str

```python
class Washer():
    def __init__(self):
        self.width = 300

    def __str__(self):
        return '解释说明：类的说明或对象状态的说明'

haier = Washer()

print(haier) # 解释说明：类的说明或对象状态的说明

```

## 13.9 del

```python
class Washer():
    def __init__(self):
        self.width = 300

    def __del__(self):
        print('对象已经删除')

haier = Washer() # 对象已经删除
```

## 13.10 烤地瓜

```python
# 1. 定义类：初始化属性、被烤和添加调料的方法、显示对象信息的str
class SweetPotato():
    def __init__(self):
        # 被烤的时间
        self.cook_time = 0
        # 烤的状态
        self.cook_state = '生的'
        # 调料列表
        self.condiments = []

    def cook(self, time):
        """烤地瓜方法"""
        # 1. 先计算地瓜整体烤过的时间
        self.cook_time += time
        # 2. 用整体烤过的时间再判断地瓜的状态
        if 0 <= self.cook_time < 3:
            # 生的
            self.cook_state = '生的'
        elif 3 <= self.cook_time < 5:
            # 半生不熟
            self.cook_state = '半生不熟'
        elif 5 <= self.cook_time < 8:
            # 熟了
            self.cook_state = '熟了'
        elif self.cook_time >= 8:
            # 烤糊了
            self.cook_state = '烤糊了'

    def add_condiments(self, condiment):
        # 用户意愿的调料追加到调料列表
        self.condiments.append(condiment)

    def __str__(self):
        return f'这个地瓜的被烤过的时间是{self.cook_time}, 状态是{self.cook_state}, 调料有{self.condiments}'

# 2. 创建对象并调用对应的实例方法
digua1 = SweetPotato()

print(digua1) # 初始状态 # 这个地瓜的被烤过的时间是0, 状态是生的, 调料有[]

digua1.cook(2)
digua1.add_condiments('辣椒面儿')
print(digua1) # 这个地瓜的被烤过的时间是2, 状态是生的, 调料有['辣椒面儿']

digua1.cook(2)
digua1.add_condiments('酱油')
print(digua1) # 这个地瓜的被烤过的时间是4, 状态是半生不熟, 调料有['辣椒面儿', '酱油']
```

## 13.11 搬家具

```python
class Furniture():
    def __init__(self, name, area):
        self.name = name
        self.area = area

class Home():
    def __init__(self, address, area):
        # 地理位置
        self.address = address
        # 房屋面积
        self.area = area
        # 剩余面积
        self.free_area = area
        # 家具列表
        self.furniture = []

    def __str__(self):
        return f'房子地理位置在{self.address}, 房屋面积是{self.area}, 剩余面积{self.free_area}, 家具有{self.furniture}'

    def add_furniture(self, item):
        """容纳家具"""
        # 如果 家具占地面积 <= 房子剩余面积：可以搬入(家具列表添加家具名字数据并房子剩余面积更新：
        # 房屋剩余面积 - 该家具的占地面积
        # 否则：提示用户家具太大，剩余面积不足，无法容纳
        # )
        if item.area <= self.free_area:
            self.furniture.append(item.name)
            self.free_area -= item.area
        else:
            print('家具太大，剩余面积不足，无法容纳')


# 双人床， 6
bed = Furniture('双人床', 6)
sofa = Furniture('沙发', 10)

# 房子1： 北京, 1000
jia1 = Home('北京', 1000)
print(jia1) # 房子地理位置在北京, 房屋面积是1000, 剩余面积1000, 家具有[]

jia1.add_furniture(bed)
print(jia1) # 房子地理位置在北京, 房屋面积是1000, 剩余面积994, 家具有['双人床']

ball = Furniture('篮球场', 2000)
jia1.add_furniture(ball) # 家具太大，剩余面积不足，无法容纳

print(jia1) # 房子地理位置在北京, 房屋面积是1000, 剩余面积994, 家具有['双人床']
```

# 14 面向对象——继承

## 14.1 继承

```python
# 继承：子类默认继承父类的所有属性和方法

# 1. 定义父类
class A(object):
    def __init__(self):
        self.num = 1

    def info_print(self):
        print(self.num)

# 2. 定义子类 继承父类
class B(A):
    pass

# 3. 创建对象，验证结论
result = B()
result.info_print() # 1
```

## 14.2 单继承

```python
# 1. 师父类，属性和方法
class Master(object):
    def __init__(self):
        self.kongfu = '[古法煎饼果子配方]'

    def make_cake(self):
        print(f'运用{self.kongfu}制作煎饼果子')

# 2. 定义徒弟类，继承师父类
class Prentice(Master):
    pass

# 3. 用徒弟类创建对象，调用实例属性和方法
daqiu = Prentice()

print(daqiu.kongfu) # [古法煎饼果子配方]

daqiu.make_cake() # 运用[古法煎饼果子配方]制作煎饼果子
```

## 14.3 多继承

```python
# 结论：如果一个类继承多个父类，优先继承第一个父类的同名属性和方法

# 1. 师父类，属性和方法
class Master(object):
    def __init__(self):
        self.kongfu = '[古法煎饼果子配方]'

    def make_cake(self):
        print(f'运用{self.kongfu}制作煎饼果子')

# 为了验证多继承，添加School父类
class School(object):
    def __init__(self):
        self.kongfu = '[黑马煎饼果子配方]'

    def make_cake(self):
        print(f'运用{self.kongfu}制作煎饼果子')

# 2. 定义徒弟类，继承师父类 和 学校类
class Prentice(School, Master):
    pass

# 3. 用徒弟类创建对象，调用实例属性和方法
daqiu = Prentice()

print(daqiu.kongfu) # [黑马煎饼果子配方]

daqiu.make_cake() # 运用[黑马煎饼果子配方]制作煎饼果子
```

## 14.4 子类重写父类同名属性和方法

```python
# 结论：如果子类和父类拥有同名属性和方法，子类创建对象调用属性和方法的时候，调用到的是子类里面的同名属性和方法

# 1. 师父类，属性和方法
class Master(object):
    def __init__(self):
        self.kongfu = '[古法煎饼果子配方]'

    def make_cake(self):
        print(f'运用{self.kongfu}制作煎饼果子')


# 为了验证多继承，添加School父类
class School(object):
    def __init__(self):
        self.kongfu = '[黑马煎饼果子配方]'

    def make_cake(self):
        print(f'运用{self.kongfu}制作煎饼果子')


# 2. 定义徒弟类，继承师父类 和 学校类， 添加和父类同名的属性和方法
class Prentice(School, Master):
    def __init__(self):
        self.kongfu = '[独创煎饼果子技术]'

    def make_cake(self):
        print(f'运用{self.kongfu}制作煎饼果子')


# 3. 用徒弟类创建对象，调用实例属性和方法
daqiu = Prentice()

print(daqiu.kongfu) # [独创煎饼果子技术]

daqiu.make_cake() # 运用[独创煎饼果子技术]制作煎饼果子
```

## 14.5 mro

```python
# 1. 师父类，属性和方法
class Master(object):
    def __init__(self):
        self.kongfu = '[古法煎饼果子配方]'

    def make_cake(self):
        print(f'运用{self.kongfu}制作煎饼果子')

# 2. 定义徒弟类，继承师父类 添加和父类同名的属性和方法
class Prentice(Master):
    def __init__(self):
        self.kongfu = '[独创煎饼果子技术]'

    def make_cake(self):
        print(f'运用{self.kongfu}制作煎饼果子')

# 3. 用徒弟类创建对象，调用实例属性和方法
daqiu = Prentice()

print(daqiu.kongfu) # [独创煎饼果子技术]

daqiu.make_cake() # 运用[独创煎饼果子技术]制作煎饼果子

print(Prentice.__mro__) # (<class '__main__.Prentice'>, <class '__main__.Master'>, <class 'object'>)
```

## 14.6 子类调用父类同名属性和方法

```python
# 1. 师父类，属性和方法
class Master(object):
    def __init__(self):
        self.kongfu = '[古法煎饼果子配方]'

    def make_cake(self):
        print(f'运用{self.kongfu}制作煎饼果子')


# 为了验证多继承，添加School父类
class School(object):
    def __init__(self):
        self.kongfu = '[黑马煎饼果子配方]'

    def make_cake(self):
        print(f'运用{self.kongfu}制作煎饼果子')


# 2. 定义徒弟类，继承师父类 和 学校类， 添加和父类同名的属性和方法
class Prentice(School, Master):
    def __init__(self):
        self.kongfu = '[独创煎饼果子技术]'

    def make_cake(self):
        # 加自己的初始化的原因：如果不加这个自己的初始化，kongfu属性值是上一次调用的init内的kongfu属性值
        self.__init__()
        print(f'运用{self.kongfu}制作煎饼果子')

    # 子类调用父类的同名方法和属性：把父类的同名属性和方法再次封装
    def make_master_cake(self):
        # 父类类名.函数()
        # 再次调用初始化的原因：这里想要调用父类的同名方法和属性，属性在init初始化位置，所以需要再次调用init
        Master.__init__(self)
        Master.make_cake(self)

    def make_school_cake(self):
        School.__init__(self)
        School.make_cake(self)


# 3. 用徒弟类创建对象，调用实例属性和方法
daqiu = Prentice()
daqiu.make_cake() # 运用[独创煎饼果子技术]制作煎饼果子

daqiu.make_master_cake() # 运用[古法煎饼果子配方]制作煎饼果子

daqiu.make_school_cake() # 运用[黑马煎饼果子配方]制作煎饼果子

daqiu.make_cake() # 运用[独创煎饼果子技术]制作煎饼果子
```

## 14.7 多层继承

```python
# 1. 师父类，属性和方法
class Master(object):
    def __init__(self):
        self.kongfu = '[古法煎饼果子配方]'

    def make_cake(self):
        print(f'运用{self.kongfu}制作煎饼果子')


# 为了验证多继承，添加School父类
class School(object):
    def __init__(self):
        self.kongfu = '[黑马煎饼果子配方]'

    def make_cake(self):
        print(f'运用{self.kongfu}制作煎饼果子')


# 2. 定义徒弟类，继承师父类 和 学校类， 添加和父类同名的属性和方法
class Prentice(School, Master):
    def __init__(self):
        self.kongfu = '[独创煎饼果子技术]'

    def make_cake(self):
        self.__init__()
        print(f'运用{self.kongfu}制作煎饼果子')

    # 子类调用父类的同名方法和属性：把父类的同名属性和方法再次封装
    def make_master_cake(self):
        Master.__init__(self)
        Master.make_cake(self)

    def make_school_cake(self):
        School.__init__(self)
        School.make_cake(self)


# 步骤：1. 创建类Tusun， 用这个类创建对象；2. 用这个对象调用父类的属性或方法看能否成功
class Tusun(Prentice):
    pass


xiaoqiu = Tusun()

xiaoqiu.make_cake() # 运用[独创煎饼果子技术]制作煎饼果子

xiaoqiu.make_master_cake() # 运用[古法煎饼果子配方]制作煎饼果子

xiaoqiu.make_school_cake() # 运用[黑马煎饼果子配方]制作煎饼果子

```

## 14.8 获取和修改私有属性

```python
class Prentice():
    def __init__(self):
        self.kongfu = '[独创煎饼果子技术]'
        # 定义私有属性
        self.__money = 2000000

    # 定义函数：获取私有属性值 get_xx
    def get_money(self):
        return self.__money

    # 定义函数：修改私有属性值 set_xx
    def set_money(self):
        self.__money = 500

class Tusun(Prentice):
    pass


xiaoqiu = Tusun()

print(xiaoqiu.get_money()) # 2000000

xiaoqiu.set_money()

print(xiaoqiu.get_money()) # 500

```

## 14.9 私有权限

```python
# Master 类
class Master(object):
    def __init__(self):
        pass

# School 类
class School(object):
    def __init__(self):
        pass

# Prentice 类 先继承School类，再继承Master类
class Prentice(School, Master):
    def __init__(self):
        # 定义私有属性
        self.money = 2000000

    # 定义私有方法
    def info_print(self):
        print('这是私有方法')

class Tusun(Prentice):
    pass

xiaoqiu = Tusun()

print(xiaoqiu.money) # 2000000

xiaoqiu.info_print() # 这是私有方法
```

## 14.10 super

```python
# 使用super()是一个好的习惯。一般我们在子类中需要调用父类的方法时才会这么用。
# super()的好处就是可以避免直接使用父类的名字.主要用于多重继承

class A:
    def m(self):
        print('A')


class B:
    def m(self):
        print('B')


class C(A):
    def m(self):
        print('C')
        super().m()

x=C()

x.m()
```

# 15 面向对象——多态

## 15.1 多态体验

```python
# 需求：警务人员和警犬一起工作，警犬分2种：追击敌人和追查毒品，携带不同的警犬，执行不同的工作

# 1. 定义父类，提供公共方法： 警犬 和 人
class Dog(object):
    def work(self):
        pass

# 2. 定义子类，子类重写父类方法：定义2个类表示不同的警犬
class ArmyDog(Dog):
    def work(self):
        print('追击敌人...')

class DrugDog(Dog):
    def work(self):
        print('追查毒品...')

# 定义人类
class Person(object):
    def work_with_dog(self, dog):
        dog.work()

# 3. 创建对象，调用不同的功能，传入不同的对象，观察执行的结果
ad = ArmyDog()
dd = DrugDog()

daqiu = Person()
daqiu.work_with_dog(ad) # 追击敌人...
daqiu.work_with_dog(dd) # 追查毒品...
```

## 15.2 类属性——设置和访问

```python
# 1. 定义类，定义类属性
class Dog(object):
    tooth = 10

# 2. 创建对象
wangcai = Dog()
xiaohei = Dog()

# 3. 访问类属性： 类和对象
print(Dog.tooth)
print(wangcai.tooth)
print(xiaohei.tooth)
```

## 15.3 类属性——修改

```python
class Dog(object):
    tooth = 10

wangcai = Dog()
xiaohei = Dog()

# 1. 类 类.类属性 = 值
Dog.tooth = 20
print(Dog.tooth) # 20
print(wangcai.tooth) # 20
print(xiaohei.tooth) # 20

# 2. 测试通过对象修改类属性
wangcai.tooth = 200

print(Dog.tooth)  # 20
print(wangcai.tooth)  # 200
print(xiaohei.tooth)  # 20
```

## 15.4 类方法

```python
# 1. 定义类：私有类属性，类方法获取这个私有类属性
class Dog(object):
    __tooth = 10

    # 定义类方法
    @classmethod
    def get_tooth(cls):
        return cls.__tooth

# 2. 创建对象，调用类方法
wangcai = Dog()
result = wangcai.get_tooth()
print(result) # 10

```

## 15.5 静态方法

```python
# 1. 定义类，定义静态方法
class Dog(object):
    @staticmethod
    def info_print():
        print('这是一个静态方法')

# 2. 创建对象
wangcai = Dog()

# 3. 调用静态方法：类 和 对象
wangcai.info_print() # 这是一个静态方法

Dog.info_print() # 这是一个静态方法
```

# 16 异常

## 16.1 体验异常

```python
# 需求：尝试打开demo.txt，如果文件不存在，只写方式打开w
"""
try:
    可能发生错误的代码
except:
    发生错误的时候执行的代码
"""

try:
    f = open('demo.txt', 'r')
except:
    f=open('demo.txt', 'w') # 设置文件对象

    str="You should like me "

    f.write(str)  # 将字符串写入文件中
```

## 16.2 异常类型

```python
# NameError
print(num)

# ZeroDivisionError
print(1/0)
```

## 16.2 捕获指定异常

```python
try:
    print(num)
except NameError:
    print('Oh,shit')

try:
    print(1/0)
except ZeroDivisionError:
    print('Oh,wrong')
```

## 16.3 捕获多个异常

```python
try:
    print(1/0)
except (NameError, ZeroDivisionError):
    print('有错误')
```

## 16.4 捕获异常描述信息

```python
try:
    print(1/0)
except (NameError, ZeroDivisionError) as result:
    print(result) # division by zero

try:
    print(num)
except (NameError, ZeroDivisionError) as result:
    print(result) # name 'num' is not defined
```

## 16.5 捕获所有异常

```python
try:
    print('Do you love me ?')
    print(sum)

except Exception as result:
    print(result)
```

## 16.6 Exception & else

```python
try:
    print(1) # 1
except Exception as result:
    print(result)
else:
    print('我是else，当没有异常的时候执行的代码') # 我是else，当没有异常的时候执行的代码
```

## 16.7 Exception & finally

```python
# 需求：尝试以r打开文件，如果有异常以w打开这个文件，最终关闭文件
try:
    f = open('test100.txt', 'r')
except Exception as e:
    f = open('test100.txt', 'w')
finally:
    f.close()
```

## 16.8 异常的传递

```python
# 需求1： 尝试只读打开test.txt 文件存在读取内容，不存在提示用户
# 需求2： 读取内容：循环读取，当无内容的时候退出循环，如果用户意外终止，提示用户已经被意外终止
import time
try:
    f = open('test.txt')
    # 尝试循环读取内容
    try:
        while True:
            con = f.readline()
            # 如果读取完成退出循环
            if len(con) == 0:
                break

            time.sleep(3)
            print(con)
    except:
        # 在命令提示符中如果按下ctrl+C结束终止的键
        print('程序被意外终止')
except:
    print('该文件不存在')
```

## 16.9 自定义异常

```python
# 1. 自定义异常类， 继承Exception， 魔法方法有init和str(设置异常描述信息)
class ShortInputError(Exception):
    def __init__(self, length, min_len):
        # 用户输入的密码长度
        self.length = length
        # 系统要求的最少长度
        self.min_len = min_len

    # 设置异常描述信息
    def __str__(self):
        return f'您输入的密码长度是{self.length}, 密码不能少于{self.min_len}'


def main():
    # 2. 抛出异常: 尝试执行：用户输入密码，如果长度小于3，抛出异常
    try:
        password = input('请输入密码：')
        if len(password) < 3:
            # 抛出异常类创建的对象
            raise ShortInputError(len(password), 3)
    # 3. 捕获该异常
    except Exception as result:
        print(result)
    else:
        print('没有异常，密码输入完成')


main()
```

# 17 模块和包

## 17.1 模块和包的使用方法

```python
# 需求：math模块下sqrt() 开平方计算
"""
1. 导入模块
2. 测试是否导入成功：调用该模块内的sqrt功能
"""
# 方法一：import 模块名; 模块名.功能
# import math
# print(math.sqrt(9))


# 方法二： from 模块名 import 功能1, 功能2...; 功能调用（不需要书写模块名.功能）
# from math import sqrt
# print(sqrt(9))


# 方法三：from 模块名 import *; 功能调用（不需要书写模块名.功能）
from math import *
print(sqrt(9))
```

## 17.2 模块别名和功能别名

```python
# 需求： 运行后暂停2秒打印hello
"""
1. 导入time模块或导入time模块的sleep功能
2. 调用功能
3. 打印hello
"""

# 1. 模块别名
# import time as tt
# tt.sleep(2)
# time.sleep(2)
# print('hello')

# 2. 功能别名
from time import sleep as sl
sl(1)
print('hello')
```

## 17.3 自制module

```python
"""
# module1
# 需求：一个函数 完成任意两个数字加法运算
def testA(a, b):
    print(a + b)

print(__name__)

# __name__是系统变量，是模块的标识符，值是：如果是自身模块值是__main__, 否则是当前的模块的名字
if __name__ == '__main__':
    testA(1, 1)
    
"""

# 1. 导入模块
import module1

# 2. 调用功能
module1.testA(2, 2) # 4
```

## 17.4 模块定位顺序

```python
# 1. 自己的文件名不能和已有模块名重复，如果重复导致模块无法使用 -- random
import random
num = random.randint(1, 5)
print(num) # 1-5之间的随机数

# 2. 当使用from xx import 功能 导入模块的功能的时候，如果功能名字重复，导入的时候后定义或后导入的这个同名功能
# 场景 time.sleep()
def sleep():
    print('我是自定义的sleep')

sleep() # 我是自定义的sleep

# 问题：import 模块名  是否担心 功能名字重复的问题  -- 不需要
import time
print(time) # <module 'time' (built-in)>

time = 1
print(time) # 1

# 问题：为什么变量也能覆盖模块？ -- 在Python语言中，数据是通过 引用 传递的。
```

## 17.5  all 列表——只有all列表里面的功能才能导入

```python
"""
# module2
# 定义多个功能，把某个功能添加到__all__
__all__ = ['testA']


def testA():
    print('testA')


def testB():
    print('testB')
"""

from module import *

testA() # testA

# 因为testB函数没有添加到all列表，只有all列表里面的功能才能导入
# testB()
```

## 17.6 导入包

```python
# 方法一
"""
1. 导入
import 包名.模块名
2. 调用功能
包名.模块名.功能()
"""

# 方法二：注意 设置__init__.py文件里面的all列表，添加的是允许导入的模块
"""
from 包名 import *
模块名.目标
"""
from mypackage import *
```

