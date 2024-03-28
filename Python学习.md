# Python学习

## 01.什么是操作系统

eg.windows\macos\linux...

有<u>操作系统</u>可以直接与硬件之间联系

如果没有操作系统就需要用<u>机器语言</u>与硬件沟通

> 什么是机器语言？
>
> 0101000111这类二进制语言

## 02.linux

在linux没有windows“盘”的概念

只有一个<u>根目录</u>

> /：根目录
>
> /home：系统默认家目录
>
> /etc：系统配置文件存放目录
>
> /bin：可执行二进制文件的目录

## 03.字面量

在代码中，被写在代码中==**固定的值**==就是字面量

![image-20240227122200701](/Users/mac/Documents/学习/python/python学习/image-20240227122200701.png)

⚠️：在python中，字符串的写法与我们在日常生活中不太一样。==需要加上“”双引号==

## 04.注释

python中添加注释（注释不会影响文件运行），有利于别人看懂我们的代码，增加可读性

1. 单行注释 `# （空格）后面是注释内容`
2. 多行注释 `""""中间的就是多行注释"""`

快捷键：command + / ：注释

<u>多行注释</u>一般写在文件的<u>开头位置</u>：

1. 用于解释整个python文件
2. 解释文件中的<u>类</u>
3. 解释文件中的<u>方法</u>

## 05.变量

在程序运行时<u>存储计算结果</u>或者<u>表示值</u>的抽象概念

`变量名称=变量值`

==记录变量是为了重复的使用它==

在python中如何输出多分内容`print(content1,content2,....,contantN)`

## 06.数据类型

- string类：字符串
- int类：整型
- float类：浮点型

`type(被查看数据)`用于得到变量==数据类型==

⚠️：在python中变量是没有类型的，但是存储的数据是有类型的

1. print直接输出

   `print(type(6))`

2. 用变量储存type()的结果，再打印出来 `string_type=type("黑马程序员")`

   `print(string_type)`

## 07.数据类型转换

为什么需要数据类型的转换？

有时候我们读取到的数据类型和我们所需要的数据类型是不一样的，这时候我们就需要数据类型转换。

![image-20240227122215202](/Users/mac/Documents/学习/python/python学习/image-20240227122215202.png)

注意⚠️：

1. 任何类型通过 `str()`都可以转化为字符串
2. 但是想将字符串转化为整数型，要求字符串全部为数字才可以
3. 浮点数和整数也可以互相转化，但是浮点数转整数会丢失掉一部分精度

## 08.标识符

什么是标识符？

在编程时，所用到的一系列名字，用于变量、类、方法等命名都可以称之为<u>标识符</u>

**命名规则：**

- 内容限定

​	只可以使用【英文、中文、数字、下划线】

​	⚠️：不推荐使用中文；==不可以将数字用在命名开头==

- 大小写敏感

  比如：Andy不等于Andy

- 不可以使用关键字（也大小写敏感）

![image-20240227122227861](/Users/mac/Documents/学习/python/python学习/image-20240227122227861.png)

## 09.运算符

基础运算符：

![image-20240227122237554](/Users/mac/Documents/学习/python/python学习/image-20240227122237554.png)

赋值运算符

![image-20240227150530701](/Users/mac/Documents/学习/python/python学习/image-20240227150530701.png)

## 10.字符串三种拓展

1. 单引号定义法 `name='黑马程序员'`
2. 双引号定义法 `name="黑马程序员"`
3. 三引号定义法 `name="""黑马程序员"""`

​	三引号和多行注释的写法一样，同样支持换行操作。

​	使用变量去接受就是字符串，不使用变量去接受就是多行注释。

注意⚠️：这三种都可以定义字符串，效果是一样的

![image-20240227151558145](/Users/mac/Documents/学习/python/python学习/image-20240227151558145.png)

例子1：

![image-20240227151727353](/Users/mac/Documents/学习/python/python学习/image-20240227151727353.png)

![image-20240227151805923](/Users/mac/Documents/学习/python/python学习/image-20240227151805923.png)

例子2:

![image-20240227152121736](/Users/mac/Documents/学习/python/python学习/image-20240227152121736.png)

![image-20240227152137970](/Users/mac/Documents/学习/python/python学习/image-20240227152137970.png)

## 11.字符串的拼接

如果我们有两个字符串，将其拼接成一个字符串，通过+号即可完成

![image-20240227152736881](/Users/mac/Documents/学习/python/python学习/image-20240227152736881.png)

## 12.字符串格式化

![image-20240227153406716](/Users/mac/Documents/学习/python/python学习/image-20240227153406716.png)

- **占位型拼接格式化**

多个变量占位，变量用括号括起来，并按照占位的顺序填入

`class_num=56`

`avg_salary=6000`

`message="The class %s,after learning python,the average salary is %s."%(class_num,avg_salary)`

![image-20240227155534047](/Users/mac/Documents/学习/python/python学习/image-20240227155534047.png)

![image-20240227155634111](/Users/mac/Documents/学习/python/python学习/image-20240227155634111.png)

- **格式化精度控制**（占位型）

![image-20240227155816578](/Users/mac/Documents/学习/python/python学习/image-20240227155816578.png)

注意⚠️：

1. `m.n`要求是数字才可以用

   ![image-20240227160250350](/Users/mac/Documents/学习/python/python学习/image-20240227160250350.png)

```python
num=11.1234
print("the result is %5.2f" %num)

>>the result is 11.12
```

2. 如果宽度m小于数字本身，那么它不会生效
3. 如果宽度m大于数字本身，它会在数字前面加上空格
4. n在对小数部分进行进度限制的同时，还会进行<u>四舍五入</u>

- **快速格式化**

`f"内容{变量}"`的方式进行快速格式化

注意⚠️：快速格式化的方法不限制格式类型，也不做精度控制

```python
name="小明"
brith_year=2003
month_salary=12345.2
print(f"他是{name},他出身于{brith_year},他现在的月薪是{month_salary}")

>>他是小明,他出身于2003,他现在的月薪是12345.2
```

- **表达式格式化**

什么是表达式？

<u>一条具==有明确执行结果==的代码语句，就称之为表达式</u>

![image-20240227162804948](/Users/mac/Documents/学习/python/python学习/image-20240227162804948.png)

```python
print("1*1的结果是 %s" %(1*1))
>>1*1的结果是 1
print(f"1*1的结果是{1*1}")
>>1*1的结果是1
#注意占位是括号（），而快速格式化是中括号{}
print("字符串在python中的类型是：%s" %type("字符串"))
>>字符串在python中的类型是：<class 'str'>
print("字符串在python中的类型是：%s，数值为 %d" %(type("字符串"),10*10))
>>字符串在python中的类型是：<class 'str'>，数值为 100
```

## 13.数据输入

`input()` 数据输入函数，它可以从键盘获取输入，使用一个变量接受（存储）input语句获取的键盘输入数据即可。

例子：

```python
#方法一
print("Please tell me, who are you?")
name=input()
print("Get!! You are %s"% name)
>>Please tell me, who are you?
xiaoming
Get!! You are xiaoming

#方法二
name=input("Please tell me, who are you?")
print("Get!! You are %s"% name)
>>Please tell me, who are you?xiaoming
Get!! You are xiaoming
```

数据输入默认是什么类型呢？

```python
num=input("what is your phone number")
print("your phone number type is:" , type(num))
>>what is your phone number123
your phone number type is: <class 'str'>
```

**数据输入，默认储存为string类型**

如果想要得到其他类型，需要手动转换

```python
#转换为int类型
num=int(input("what is your phone number"))
print("your phone number type is:" , type(num))

>>what is your phone number123
your phone number type is: <class 'int'>
```

## 14.布尔类型和比较运算符

逻辑运算中，只有**是和否**之分

- **布尔(bool)**

True记为真——数字1

Fasle记为假——数字0

定义变量存储布尔类型数据：
`变量名称=布尔类型字面量`

注意⚠️：

1. 布尔类型不仅可以通过自定义，同时也**可以通过比较计算得到布尔类型**
2. 布尔类型定义（True\Fasle）,**注意首字母大写**

```python
result=10>5 #这个就是一个比较运算
print(f"the result of 10>5 is {result},the result type of 10>5 is :{type(result)}")

>>the result of 10>5 is True,the result type of 10>5 is :<class 'bool'>
```

- **比较运算**

![image-20240228094600327](/Users/mac/Documents/学习/python/python学习/image-20240228094600327.png)

```python
# ==
num1=10
num2=10
print(f"the result of num1 equal to num2 is {num1==num2}")

>>the result of num1 equal to num2 is True

# !=
num1=10
num2=10
print(f"the result of num1 equal to num2 is {num1!=num2}") # 数字比较

>>the result of num1 equal to num2 is False

name1="hello"
name2="hallo"
print(f"the result of name1 equal to name2 is {name1!=name2}") # 字符串比较

>>the result of name1 equal to name2 is True

# >
num1=10
num2=5
print(f"thr result of 10>5 is :{num1>num2}")

>>thr result of 10>5 is :True

# <
num1=10
num2=5
print(f"thr result of 10<5 is :{num1<num2}")

>>thr result of 10<5 is :False

# >=
num1=10
num2=10
print(f"thr result of 10>=10 is :{num1>=num2}")

>>thr result of 10>= is :True

# <=
num1=10
num2=10
print(f"thr result of 10<=10 is :{num1<=num2}")

>>thr result of 10<=10 is :True
```

## 15.if语句的基本格式

格式：
`if要判断的条件：`

​	`条件成立时，要做的事情`

注意⚠️：

1. 不要忘记判断条件后面的冒号“：”
2. 在python中，是**通过缩进判断归属**的，所以不能忘了缩进
3. 判断语句的结果必须是布尔类型（True、Fasle），如果是True就会执行if内的代码，Fasle则不会

```python
# 1
age=int(input("how old are you?"))
if age>=18:
    print(f"you are {age} years old, is a adult.")
print("time go fast!")

>>how old are you?20
you are 20 years old, is a adult.
time go fast!
>>how old are you?8
time go fast!
```

## 16.if else 组合判断

当不满足if判断条件是，执行else内代码

格式：
`else:`

​	`else内要执行的语句`

注意⚠️：

1. else后面也需要加冒号“：”
2. else的判断条件是if条件的反面，所以else一定是和if搭配使用的，而且else后面不需要加判断条件
3. else同样需要缩进噢～

```python
age=int(input("how old are you?"))
if age>=18:
    print(f"you are {age} years old, you need to pay")
else:
    print(f"you are a child, you not need to pay")
print("have a good time!")

>>how old are you?20
you are 20 years old, you need to pay
have a good time!
>>how old are you?2
you are a child, you not need to pay
have a good time!
```

## 17.if elif else 语句

在某些场景下，判断条件不止一个时，我们需要

![image-20240228102645830](/Users/mac/Documents/学习/python/python学习/image-20240228102645830-9087206.png)

方法一：

```python
age=int(input("how old are you?"))
vip_level=int(input("what is you vip level?"))
if age<18:
    print(f"you are a child, you not need to pay")
elif vip_level>3:
    print(f"your vip level is {vip_level}, you not need to pay")
else:
    print(f"you don't have flee condition,so you need to pay")
print("have a good time!")

>>how old are you?20
what is you vip level?4
your vip level is 4, you not need to pay
have a good time!
```

注意⚠️：

1. 判断是互斥且有顺序的
2. 如果满足条件1，那么将不会进入条件2、3
3. 如果所有if和elif的条件均不满足，则会进入else
4. else也可以省略不写，但是一般都会写:smile:

方法二：

```python
# 这种代码更简洁，而且可以简化输入
# age=int(input("how old are you?"))
# vip_level=int(input("what is you vip level?"))
if int(input("how old are you?"))<18:
    print(f"you are a child, you not need to pay")
elif int(input("what is you vip level?"))>3:
    print(f"your vip level is high enough, you not need to pay")
else:
    print(f"you don't have flee condition,so you need to pay")
print("have a good time!")

>>how old are you?3
you are a child, you not need to pay
have a good time!
```

**小练习：**
![image-20240228112804963](/Users/mac/Documents/学习/python/python学习/image-20240228112804963.png)

```python
# 定义一个数字
num1=10
# 请输入猜想
if int(input("请输入第一次猜想："))==10:
    print(f"我想的是{num1},你猜对了")
elif int(input("猜错了，请再猜一次："))==10:
    print(f"我想的是{num1},你猜对了")
elif int(input("猜错了，请再猜最后一次："))==10:
    print(f"我想的是{num1},你猜对了")
else:
    print(f"我想的是{num1},你猜错了")
    
>>请输入第一次猜想：1
猜错了，请再猜一次：2
猜错了，请再猜最后一次：3
我想的是10,你猜错了
```

## 18.判断语句嵌套

在使用时，很多条件并不是并列条件，会出现**满足前置条件才会二次判断的多层判断需求**。

‼️嵌套的关键点在于：**空格缩进**（通过空格来决定语句之间的层次关系）

`if条件1:`

​	`满足if条件1时，执行的事情1`

​	`满足if条件1时，执行的事情2`

​	`if条件2:`

​		`同时满足条件1、条件2时，做的事情1`

​		`同时满足条件1、条件2时，做的事情2`

**例题：**

![image-20240228121251094](/Users/mac/Documents/学习/python/python学习/image-20240228121251094.png)

```python
age=int(input("请输入你的年龄："))
if age>18:
    if age<30:
        print("你的年龄达标了")
        if int(input("请输入你的入职时间："))>2:
            print("可以领取礼物！")
        elif int(input("请输入你的级别："))>3:
            print("可以领取礼物！")
        else:
            print("您的入职时间和级别不达标，不好意思！")
    else:
        print("您的年龄太大了")
else:
    print("您的年龄太小了")
>>请输入你的年龄：23
你的年龄达标了
请输入你的入职时间：1
请输入你的级别：2
您的入职时间和级别不达标，不好意思！
```

**例题：**
![image-20240228131619650](/Users/mac/Documents/学习/python/python学习/image-20240228131619650.png)

```python
#方法一
import random
num=random.randint(1,10)
num1=int(input("Please enter a number between 1 and 10:"))
if num1==num:
    print(f"the random number is {num}, you are correct")
elif num1!=num:
    if num1<num:
        num2=int(input("please enter a larger number:"))
        if num2==num:
            print(f"the random number is {num}, you are correct")
        elif num2!=num:
            if num2<num:
                num3 = int(input("please enter a larger number:(last chance)"))
            elif num2 > num:
                num3 = int(input("please enter a smaller number:(last chance)"))
                if num3==num:
                    print(f"the random number is {num}, you are correct")
    elif num1>num:
        num2 = int(input("please enter a smaller number:"))
        if num2==num:
            print(f"the random number is {num}, you are correct")
        elif num2!=num:
            if num2<num:
                num3 = int(input("please enter a larger number:(last chance)"))
            elif num2 > num:
                num3 = int(input("please enter a smaller number:(last chance)"))
                if num3==num:
                    print(f"the random number is {num}, you are correct")
else:
    print("you are wrong")
    
# 方法二
import random
num=random.randint(1,10)
num1=int(input("Please enter a number between 1 and 10:"))
if num1==num:
    print(f"the random number is {num}, you are correct")
else:
    if num1<num:
        print("number is too small")
    else:
        print("number is too large")
    num2=int(input("Please enter a number between 1 and 10:"))
    if num2 == num:
        print(f"the random number is {num}, you are correct")
    else:
        if num2 < num:
            print("number is too small")
        else:
            print("number is too large")
        num3 = int(input("Please enter a number between 1 and 10:"))
        if num3 == num:
            print(f"the random number is {num}, you are correct")
        else:
            print("there is no chance")
```

## 19.while语句循环基础

![image-20240228164658882](/Users/mac/Documents/学习/python/python学习/image-20240228164658882-9110019.png)

**while中循环条件可以是一个变量值，每循环一次，while值加1**

```python
i=0
while i<10:
    print("今天也是很棒的一天呀～")
    i+=1
```

注意⚠️：

1. 如果没有结束语句，循环将永远进行
2. 循环一样需要空格缩进来判断从属关系

**小练习：**
![image-20240228170129662](/Users/mac/Documents/学习/python/python学习/image-20240228170129662-9110890.png)

```python
i=1
num=0
while i<=100:
    num=num+i
    i+=1
print(num)

>>5050
```

## 20.while循环的基础案例

设置一个范围1-100的随机变量，通过while循环，配合input语句，判断输入数字是否等于随机数字。

无限次机会，猜不中提示大了或者小了，猜完数字之后提示猜了几次。

```python
import random
num=random.randint(1,100)
num_guess=0
i=1

while num_guess!=num:
    num_guess=int(input("Please enter a number between 1 and 100:"))
    i+=1
    if num_guess>num:
        print("please enter a smaller number:")
    elif num_guess<num:
        print("please enter a larger number:")
print(f"You guess it! you guess the number at {i} times")
```

## 21.while中的嵌套案例

在外层的while循环内再写一个内层的while循环

```python
# 每天练习10道算法题，连续练习100天
i=1
while i<=100:
    print(f"today is the {i} day")
    j=1
    while j<=10:
        print(f"today have finish {j} problems")
        j+=1
    i+=1
```

注意⚠️：注意条件设置，避免出现无限循环

**补充知识**：

1. python中`print`输出不换行

在print后加入`end=’‘`

```python
print("hello ",end='')
print("world")
print("你好")
>>
hello world
你好
```

2. 制表符 `\t`

它可以让多行字符串进行<u>对齐</u>

用\t代替空格

```python
print("hello world")
print("thisis day")
print("hello\tworld")
print("thisis\tday")
>>
hello world
thisis day
hello	  world
thisis	day
```

**小练习：**

输出99乘法表：

```python
i=1
while i<=9:
    j=1
    while j<=i:
        print(f"{j}*{i}={i*j} ",end='')
        j+=1
    i+=1
    print("")
>>
1*1=1 
1*2=2 2*2=4 
1*3=3 2*3=6 3*3=9 
1*4=4 2*4=8 3*4=12 4*4=16 
1*5=5 2*5=10 3*5=15 4*5=20 5*5=25 
1*6=6 2*6=12 3*6=18 4*6=24 5*6=30 6*6=36 
1*7=7 2*7=14 3*7=21 4*7=28 5*7=35 6*7=42 7*7=49 
1*8=8 2*8=16 3*8=24 4*8=32 5*8=40 6*8=48 7*8=56 8*8=64 
1*9=9 2*9=18 3*9=27 4*9=36 5*9=45 6*9=54 7*9=63 8*9=72 9*9=81 
```

## 22.For 循环基础

for和while有点像，但是while点循环条件是自定义的，而for像是待办事件处理

for循环也叫**遍历循环**，<u>只能从被处理的数据集中，依次取出内容进行处理</u>

**待处理数据集可以为：字符串、列表、元组等**

`for 临时变量 in 待处理数据集`

​	`循环满足条件时执行代码`

```python
name="good"
for i in name:
    print(i,end='')
>>
good
```

**小例题**：
数一数有多少个o

```python
name="I finished two problems today"
count=0
for i in name:
    if i=='o':
        count+=1
print(f"there has {count} o")
>>
there has 3 o
```

## 23.range语句

range语句可以获得一个简单的**数字序列**

1. `range(num)`从0开始，到num结束的数字序列（不包含num本身）

`range(5)=[0,1,2,3,4]`

2. `range(num1,num2)`从num1开始到num2-1结束

`range(5,10)=[5,6,7,8,9]`

3. `range(num1,num2,step)` 从num1开始到num2结束，步长为step

`range(2,6,2)=[2,4]`

也可以用range来控制想执行的次数

```python
for i in range(2,6,2):
    print("哈哈哈哈") # 这样不调用i，只是以此来控制循环次数
>>
哈哈哈哈
哈哈哈哈
```

**小例题：**有多少个偶数

```python
num=0
for i in range(1,100):
    if i%2==0:
        num+=1

print(f"在1-99中有{num}个偶数")
>>
在1-99中有49个偶数
```

## 24.for循环临时变量作用域

如果想在for循环**外部访问临时变量**

需要在for循环之前，先将临时变量定义一次，后面临时变量会被覆盖

```python
i=0
for i in range(5):
    print(i)
print(i)
>>
0
1
2
3
4
4
```

## 25.for循环的嵌套使用

```python
# 每天练习10道算法题，连续练习100天
i=1
for i in range(1,101):
    print(f"today is the {i} day")
    for j in range(1,11):
        print(f"today have finish {j} problems")
```

**for循环打印9*9乘法表**

```python
for i in range(1,10):
    for j in range(1,i+1):
        print(f"{j}*{i}={j*i} ",end='')
    print('')
>>
1*1=1 
1*2=2 2*2=4 
1*3=3 2*3=6 3*3=9 
1*4=4 2*4=8 3*4=12 4*4=16 
1*5=5 2*5=10 3*5=15 4*5=20 5*5=25 
1*6=6 2*6=12 3*6=18 4*6=24 5*6=30 6*6=36 
1*7=7 2*7=14 3*7=21 4*7=28 5*7=35 6*7=42 7*7=49 
1*8=8 2*8=16 3*8=24 4*8=32 5*8=40 6*8=48 7*8=56 8*8=64 
1*9=9 2*9=18 3*9=27 4*9=36 5*9=45 6*9=54 7*9=63 8*9=72 9*9=81 
```

## 26.break和continue对循环的控制

无论是<u>while循环</u>还是<u>for循环</u>，都是重复性的执行特定操作

在这个重复的过程中，会出现一些其他情况：

- 暂时跳过某次循环，直接进行下一次（contiue）
- 提前退出循环，不在继续（break）

**contiue**：
中断本次循环，直接加入下一次循环

![image-20240229162342211](/Users/mac/Documents/学习/python/python学习/image-20240229162342211.png)

```python
for  i in range(2):
    print("sentence 1")
    continue
    print("sentence 2")
>>
sentence 1
sentence 1
```

1. 当contiune在嵌套循环中使用时

<u>只会影响内层循环</u>

```python
for  i in range(2):
    print("sentence 3")
    for j in range(2):
        print("sentence 1")
        continue
        print("sentence 2")
        
>>
sentence 3
sentence 1
sentence 1
sentence 3
sentence 1
sentence 1
```

**Break**:
会直接结束循环

```python
for  i in range(2):
    print("sentence 3")
    for j in range(2):
        print("sentence 1")
        break
        print("sentence 2")
>>
sentence 3
sentence 1
sentence 3
sentence 1
```

**综合例题：**

```python
import random
all_salary=10000
n=0
for i in range(1,21):
    a = random.randint(1, 10)
    if a>=5:
        all_salary=all_salary-1000
        print(f"员工{i},绩效为{a},大于5，发放工资1000元，账户剩余{all_salary}")
        n+=1
    elif all_salary==0:
        print(f"本月工资发完了，下个月领取吧")
        break
    else:
        print(f"员工{i},绩效为{a},小于5，不发放工资")
 >>
员工1,绩效为2,小于5，不发放工资
员工2,绩效为2,小于5，不发放工资
员工3,绩效为7,大于5，发放工资1000元，账户剩余9000
员工4,绩效为10,大于5，发放工资1000元，账户剩余8000
员工5,绩效为9,大于5，发放工资1000元，账户剩余7000
员工6,绩效为1,小于5，不发放工资
员工7,绩效为7,大于5，发放工资1000元，账户剩余6000
员工8,绩效为5,大于5，发放工资1000元，账户剩余5000
员工9,绩效为8,大于5，发放工资1000元，账户剩余4000
员工10,绩效为5,大于5，发放工资1000元，账户剩余3000
员工11,绩效为4,小于5，不发放工资
员工12,绩效为6,大于5，发放工资1000元，账户剩余2000
员工13,绩效为4,小于5，不发放工资
员工14,绩效为8,大于5，发放工资1000元，账户剩余1000
员工15,绩效为6,大于5，发放工资1000元，账户剩余0
本月工资发完了，下个月领取吧
```

## 27.python中的函数

**函数：** <u>组织好的，可以重复使用的，用来实现特定功能的代码段</u>

python中本来也有很多内置的函数

**小练习**：
不调用python中自带的长度函数，写一个字符串长度计量函数

```python
str1="hello"
str2="good day"
str3="have fun"

def my_len(data):
    count=0
    for i in data:
        count+=1
    print(f"the length of the string {data} is {count}")

my_len(str1)
my_len(str2)
my_len(str3)

>>
the length of the string hello is 5
the length of the string good day is 8
the length of the string have fun is 8
```

**函数的定义：**
`def 函数名（传入函数）：`

​	`函数体`

​	`return 返回值`

注意⚠️：

1. python代码执行是从上到下的，需要**先定义后使用**
2. 参数不需要时，可以省略
3. 返回值不需要时，也可以省略

**函数的传入参数：**

传入参数的功能：在函数进行计算时，<u>接受外部提供的数据</u>

```python
def add_number(a,b):
    result=a+b
    print(f"the result of {a} add {b} is {result}")

add_number(2,4)
>>
the result of 2 add 4 is 6
```

- 形式参数：函数定义中提供的a，b （参数之间要用逗号隔开）
- 实际参数：函数调用时，按照顺序传入数据，使用逗号隔开

注意⚠️：
传入参数的数量是不受限制的（可以没有，也可以有无数个）

**函数的返回值：**
`def 函数（参数）：`
	`函数体`

​	`return 返回值`

`变量=函数（参数）`

注意⚠️：

==函数体遇到return之后就结束了，所以写在return之后的代码不会运行==

```python
def number_check(a,b):
    c=a+b
    return c

number1=number_check(1,3)
print(number1)
>>
4
```

> 如果一个函数没有写return那么它有返回值吗？
>
> 在python中有一个特殊的特殊的字面量 <u>None</u>
>
> None表示空、无实际意义的意思，在布尔类型中属于false
>
> 常应用于<u>函数返回值以及if判断中</u>
>
> 也可以中None声明无初始内容的变量
>
> ```python
> def check_age(age):
>     if age>18:
>         return "success"
>     else:
>         return None
> 
> result=check_age(16)
> if not result:
>     print("未成年")
> >>
> 未成年
> ```

**函数的说明文档：**

多行注释的形式，对函数进行说明

1. 函数整体说明
2. ：param +参数说明
3. return返回值说明

## 28.函数的嵌套调用

函数嵌套调用：一个函数里面又调用了另外一个函数

```python
def func_a():
    print("----1----")

def fun_b():
    func_a()
    print("----2----")
    print("----3----")

fun_b()
>>
----1----
----2----
----3----
```

## 29.变量作用域

- **局部变量**

定义在函数题内部的变量，即只在函数体内部生效

```python
def testA():
    num=100
    print(num)
testA()
print(num) # 在这里调用num就会报错
```

- **全局变量**

定义在函数外面，在<u>函数体内部外部都能生效</u>

```python
num=100
def testA():
    print(num)

def testB():
    print(num)

testB()
testA()
>>
100
100
```

- **在函数内修改全局变量**

```python
num=100
def testA():
    print(num)

def testB():
    global num # 如果想在函数内部直接改变全局变量，使用global
    num=200
    print(num)

testA()
testB()
print(num)

>>
100
200
100
```

**综合练习：**

```python
name=input("please inter your name：")
num_salary=5000000
def check_money():
    print("----------Checking balance---------")
    print(f"{name},hello,there are {num_salary}")

def make_deposit():
    print("----------Make a deposit---------")
    global input_salary
    input_salary=int(input("how much money you should input?"))
    print(f"{name}, you have input {input_salary} successfully!")
    print(f"{name}, there are {input_salary+num_salary} in total")

def make_withdrawal():
    print("----------Make a withdrawal----------")
    global output_salary
    output_salary = int(input("how much money you should output?"))
    print(f"{name}, you have input {output_salary} successfully!")
    print(f"{name}, there are {num_salary-output_salary} in total")
def menu():
    print("----------main menu----------")
    print(f"{name},welcome to ATM:")
    print("Checking balance\t[Enter 1]")
    print("Make a deposit\t\t[Enter 2]")
    print("Make a withdrawal\t[Enter 3]")
    print("Exit system\t\t\t[Enter 4]")

while name!=None:
    menu()
    num_input = int(input("please enter your choice:"))
    if num_input==1:
        check_money()
        continue
    elif num_input==2:
        make_deposit()
        continue
    elif num_input==3:
        make_withdrawal()
        continue
    elif num_input==4:
        break
```

## 30.数据容器

一种可以容纳多份数据的数据类型

容纳的每一份数据称之为**元素**

<u>每一个元素可以是任意类型</u>（字符串、数字、布尔....）

可以分为以下5种数据容器：

- 列表
- 元组
- 字符串
- 集合
- 字典

## 31.列表 list

**列表的定义：**

`[元素1，元素2，元素3....]`

**定义变量：**

`变量名称=[元素1，元素2，元素3...]`

定义空列表：
`变量名称=[]`

`变量名称=list()`

注意⚠️：

1. 列表可以储存多个数据
2. 可以支持不同数据类型
3. 支持嵌套
4. 元素：列表中的每一份数据都称之为元素

```python
list_1=['have a good day',2,True]
list_2=[1,2,list_1,4]
print(list_2)
print(type(list_2))
>>
[1, 2, ['have a good day', 2, True], 4]
<class 'list'>
```

**列表的下标索引：**

![image-20240302114121131](/Users/mac/Documents/学习/python/python学习/image-20240302114121131.png)

注意⚠️：坐标索引不要超过范围，会报错

从列表中取出元素：
`列表[下标索引]`

从前向后是0开始（0、1、2、3....）

![image-20240302114346765](/Users/mac/Documents/学习/python/python学习/image-20240302114346765.png)

**倒序输出：**

从后往前是-1、-2、-3.....

```python
list_1=['have a good day',2,True]
list_2=[1,2,list_1,4]
print(list_2[-1])
>>
4
```

如果是**嵌套列表，如何取值**呢？

![image-20240302114502808](/Users/mac/Documents/学习/python/python学习/image-20240302114502808.png)

`列表[][]`

```python
list_1=['have a good day',2,True]
list_2=[1,2,list_1,4]
print(list_2[2][0])
>>
have a good day
```

**常用操作：**

1. 功能（方法）

在pyhton中，如果将函数定义为class类的成员，那么函数会称为==方法==

`class Student:`

​	`def add(self,x,y):`

​	`	return x+y`

方法和函数功能一样，有传入参数，有返回值，只是方法的使用格式不同：

```python
class Student():
    def add(self,x,y):
        return x+y

student=Student()
num=student.add(1,2)
print(num)
>>
3
```

2. 查找某元素的下标

`列表.index(元素)`

<u>index就是列对象内置的方法</u>

```python
mylist=[1,2,3,4,5,6,7,8,9]
print(mylist.index(7))
>>
6
```

注意⚠️：如果元素找不到，会报错velue

3. 更改特定位置的元素值：

`列表[下标]=值`

```python
mylist=[1,2,3,4,5,6,7,8,9]
mylist[6]=10
print(mylista)
>>
[1, 2, 3, 4, 5, 6, 10, 8, 9]
```

4. 插入元素

`列表.insert(下标，元素)`

```python
mylist=[1,2,3,4,5,6,7,8,10]
mylist.insert(8,9)
print(mylist)
>>
[1, 2, 3, 4, 5, 6, 7, 8, 9, 10]
```

5. 追加元素

- 在列表的尾部增加一个元素

`列表.append(元素)`

```python
mylist=[1,2,3,4,5,6,7,8,9]
mylist.append(10)
print(mylist)
>>
[1, 2, 3, 4, 5, 6, 7, 8, 9, 10]
```

- 在尾部增加多个元素

`列表.extend(其他数据容器)`

```python
mylist=[1,2,3,4,5,6,7,8,9]
mylist.extend([10,11,12])
print(mylist)
>>
[1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12]
```

6. 删除元素(指定下标)

- `del列表[下标]`
- `列表.pop(下标)` 本质上是将元素取出来，然后返回回去。我们可以<u>==得到返回值==，这个元素也将从列表中删除</u>

```python
mylist=[1,2,3,4,5,6,7,8,9]
del mylist[8]
print(mylist)
>>
[1, 2, 3, 4, 5, 6, 7, 8]
```

```python
mylist=[1,2,3,4,5,6,7,8,9]
element=mylist.pop(8)
print(mylist)
print(element)
>>
[1, 2, 3, 4, 5, 6, 7, 8]
9
```

7. 删除元素（指定内容）

`列表.remove(元素)`

删除某元素在列表中的<u>第一个匹配项</u>

注意⚠️：不是全部匹配项噢！

```python
mylist=[1,2,3,4,5,6,7,8,9,2]
mylist.remove(2)
print(mylist)
>>
[1, 3, 4, 5, 6, 7, 8, 9, 2]
```

8. 清空列表

`列表.clear()`

```python
mylist=[1,2,3,4,5,6,7,8,9,2]
mylist.clear()
print(mylist)
>>
[]
```

9. 统计某个元素在列表中的数量

`列表.count(元素)`

```python
mylist=[1,2,3,4,5,6,7,8,9,2]
num=mylist.count(2)
print(num)
>>
2
```

10. 统计列表中全部元素数量

`len(列表)`

注意⚠️：就是列表长度

```python
mylist=[1,2,3,4,5,6,7,8,9,2]
num=len(mylist)
print(num)
>>
10
```

**列表的特点：**

1. 可以容纳多个元素
2. 可以容纳不同类型的元素
3. 数据是有序存储的
4. 允许可重复数据存在
5. 可以修改

## 32.列表遍历

可以用while循环

```python
mylist=[234,34,451,2341,231,678,897,420,218]
index=0
new_list=[]
while index<len(mylist):
    new_list.append(mylist[index])
    index+=1
print(f"new_list={new_list}")
>>
new_list=[234, 34, 451, 2341, 231, 678, 897, 420, 218]
```

可以用for循环

`for 临时变量 in 数据容器：`

​	`对临时变量进行处理`

```python
mylist=[234,34,451,2341,231,678,897,420,218]
new_list=[]
for i in mylist:
    new_list.append(i)
print(f"new_list={new_list}")
>>
new_list=[234, 34, 451, 2341, 231, 678, 897, 420, 218]
```

## 33.元组

元组和列表一样，都可以存储多个、不同类型的元素

==元组一旦定义完成，就不能修改==

‼️我们需要在程序中封装数据，但是又不希望数据被篡改，元组就非常合适

**元组的定义**：使用<u>小括号</u> （列表使用【】）

`(元素1，元素2，元素3，元素4....)`

`变量名称=(元素1，元素2，元素3，元素4....)`

定义<u>空元组</u>：
`变量名称=()`

`变量名称=tuple()`

```python
t1=()
t2=(1,2,'hello',True)
t3=(1,) #元组中如果只有一个数据，这个数据后面需要添加逗号。如果不添加就不是元组类型了！
t4=(1)
print(type(t1))
print(t2)
print(type(t3))
print(type(t4))
>>
<class 'tuple'>
(1, 2, 'hello', True)
<class 'tuple'>
<class 'int'>
```

**元组的嵌套及读取**：

```python
t1=((1,2,3),(1,3,4))
print(t1[1][2])
>>
4
```

**元组的相关操作：**

1. `index()`

   查找下标对应的元素

   ```python
   t1=(1,2,3)
   print(t1.index(2))
   >>
   1
   ```

2. `count()`

```python
t1=(1,2,3,2,2)
num=t1.count(2)
print(num)
>>
3
```

3. `len(元组)`

```python
t1=(1,2,3,2,2)
print(len(t1))
>>
5
```

**元组的遍历：**

- while

  ```python
  t1=(1,2,3,2,2)
  index=0
  while index<len(t1):
      print(t1[index])
      index+=1
  >>
  0
  1
  2
  3
  2
  2
  ```

- for

  ```python
  t1=(1,2,3,2,2)
  for i in t1:
      print(i)
  ```

注意⚠️：

1. 元组内容是不可以修改的
2. 但是如果元组里面有一个list，那么元组是可以被修改的

```python
t1=(1,2,[1,2,3])
t1[2][1]=5
print(t1)
>>
(1, 2, [1, 5, 3])
```

**小练习：**

```python
t_name=('jolin',20,['badminton','music'])
print(f"thw location of age in the tuple is {t_name.index(20)}")
print(f"the student name is {t_name[0]}")
t_name[2][0]='coding' # 这里只能删除或者替换，不能增加哦
print(t_name)
>>
thw location of age in the tuple is 1
the student name is jolin
('jolin', 20, ['coding', 'music'])
```

## 34.字符串

<u>字符串</u>也是一种数据容器

它和列表、元组一样，字符串也可以对下标进行访问

- 从前向后，0开始
- 从后向前，-1开始

```python
my_str="I don't know what's your mean."
value1=my_str[-2]
value2=my_str[-3]
print(value1)
print(value2)
>>
n
a
```

注意⚠️：字符串和元组一样，==无法修改数据==，而且==字符串数据容器只可以存储字符串==

如果非要修改，只能得到<u>一个新的字符串</u>

**字符串常规操作：**

1. 查找特定字符串的下标索引值

```python
字符串.index(字符串)
```

例题：

```python
my_str="I don't know what's your mean."
print(my_str.index("what"))
>>
13
```

2. 字符串的替换

`字符串.replace(字符串1,字符串2)`

将字符串内全部：字符串1，替换为：字符串2

注意⚠️：不是修改字符串本身，而是得到一个新的字符串哦

```python
my_str="I don't know what's your mean."
new_my_str=my_str.replace("your","你的")
print(new_my_str)
>>
I don't know what's 你的 mean.
```

3. 字符串的分割

`字符串.split(分隔字符串)`

按照分隔字符串，将字符串划分为多个字符串，并存入列表对象

```python
my_str="I don't know what's your mean."
new_my_str=my_str.split(' ')
print(new_my_str)
>>
['I', "don't", 'know', "what's", 'your', 'mean.']
```

4. 字符串的规整操作

- 去除**前后**空格

`字符串.strip()`

```python
my_str=" I don't know what's your mean. "
new_my_str=my_str.strip()
print(new_my_str)
>>I don't know what's your mean.
```

- 去除**前后**指定字符串

`字符串.strip(字符串)`

这个是按照<u>单个字符移除</u>

```python
my_str="12 I don't know what's your mean.21"
new_my_str=my_str.strip("12")
print(new_my_str)
>>
I don't know what's your mean.
```

5. 计算某字符串出现的次数

`字符串.count()`

```python
my_str="I don't know what's your mean."
num=my_str.count('n')
print(num)
>>
3
```

6. 字符串长度

`num=len(字符串)`

## 35.序列

序列是指，内容连续、有序，可以使用下标引索的一类容器

<u>列表、元组、字符串、均可以视为序列</u>

**序列切片**语法：
`序列[起始下标：结束下标：步长]`

**起始下标**：子序列从何处开始，留空表示从头开始

**结束下标**：子序列从何处结束（子序列不包含结束下标位置），留空表示截取到结尾

**步长**：取元素的间隔（步长为2，会隔一个取一次）；步长也可以为负（-1表示从后往前开始取，-2表示从后往前隔一个取一次）

注意⚠️；对序列切片并不会影响序列本身，而是会得到一个新的序列

```python
my_list=[1,2,3,4,5,6,7,8,9]
new_list=my_list[1:4]  # 1开始，4结束，步长为1
print(new_list)
new_list2=my_list[ : ]  # 从头到尾，步长为1
print(new_list2)
new_list3=my_list[ : :2]  # 从头到尾，步长为2
print(new_list3)
new_list4=my_list[ : :-1]  # 从头到尾，步长为-1
print(new_list4)
new_list4=my_list[3:1:-1]  # 从3到1，步长为-1
print(new_list4)
>>
[2, 3, 4]
[1, 2, 3, 4, 5, 6, 7, 8, 9]
[1, 3, 5, 7, 9]
[9, 8, 7, 6, 5, 4, 3, 2, 1]
[4, 3]
```

## 36.集合

![image-20240304145707900](/Users/mac/Documents/学习/python/python学习/image-20240304145707900.png)

局限性在于，支持重复元素且有序

集合 {}：<u>==不支持重复元素，且内部无序==</u>

基础定义语法：

```python
my_set={3,2,1,1,2,3,1,2,3}
print(f"the constant in my_set is {my_set}, the type is {type(my_set)}")
>>
the constant in my_set is {1, 2, 3}, the type is <class 'set'>
```

注意⚠️：
不支持下标索引，但是支持修改

**基础操作：**

1. 添加元素

`集合.add(元素)`

```python
my_set={3,2,1,1,2,3,1,2,3}
my_set.add(4)
print(my_set)
>>
{1, 2, 3, 4}
```

2. 移除元素

`集合.remove(元素)`

```python
my_set={3,2,1,1,2,3,1,2,3}
my_set.add(4)
my_set.remove(3)
print(my_set)
>>
{1,2,4}
```

3. 从集合中随机取出一个元素

`集合.pop()`

会有一个元素==<u>随机</u>==的从集合中取出来，==<u>同时集合本身被修改，元素被移除</u>==

```python
my_set={3,2,1,1,2,3,1,2,3}
element=my_set.pop()
print(element)
print(my_set)
>>
1
{2, 3}
```

4. 清空集合

```python
my_set={3,2,1,1,2,3,1,2,3}
my_set.clear() # 清空集合
print(my_set)
>>
set() # 表示空集合
```

5. 取两个集合的差集

`集合1.difference(集合2)`

取出集合1有，而集合2没有的

==得到一个新集合，集合1和集合2不变==

```python
set1={1,2,3}
set2={1,5,6}
set3=set1.difference(set2)
print(set1)
print(set2)
print(set3)
>>
{1, 2, 3}
{1, 5, 6}
{2, 3}
```

6. 消除差集

`集合1.difference_updata(集合2)`

对比集合1和集合2，==在集合1内，删除和集合2相同的元素==。

结果：<u>集合1被修改，集合2不变</u>

```python
set1={1,2,3}
set2={1,5,6}
set1.difference_update(set2)
print(set1)
print(set2)
>>
{2, 3}
{1, 5, 6}
```

7. 两个集合合并

`集合1.union(集合)`

功能：将集合1和集合2组合成新集合

结果：得到新集合（顺序不确定），集合1和集合2不变

```python
set1={1,2,3}
set2={1,5,6}
set3=set1.union(set1,set2)
print(set1)
print(set2)
print(set3)
>>
{1, 2, 3}
{1, 5, 6}
{1, 2, 3, 5, 6}
```

8. 统计集合元素数量

`len()`

**集合的遍历**

因为集合不支持下标索引，所以我们只能通过for循环遍历

```python
set1={1,2,3}
set2={1,5,6}
set3=set1.union(set1,set2)
print(set1)
print(set2)
print(set3)
for element in set3:
    print(element)
    
>>
{1, 2, 3}
{1, 5, 6}
{1, 2, 3, 5, 6}
1
2
3
5
6
```

**小例题：**
信息去重：

```python
my_list=['my','name','is','jolin','is','a','good','person']
list_set=set()
for element in my_list:
    list_set.add(element)

print(list_set)
>>
{'person', 'a', 'name', 'is', 'my', 'jolin', 'good'} # 体现了集合的无序性
```

## 37.字典

生活中的字典：

【字】——【含义】

python中的字典：
【key】——【value】

之前所学的列表、元组、字符串、序列、集合都不可以通过某个元素找到另外一个元素

**字典的定义：**
`my_dict={key:value,key:value,ley:value....}`

字典存储的元素是一个个键值队

定义空字典：
`my_dict={}`

`my_dict=dict()`

```python
my_dist={"xiaoming":99,"xiaohua":90,"xiaohuang":85}
print(f"the constant is {my_dist}, the type is {type(my_dist)}")
>>
the constant is {'xiaoming': 99, 'xiaohua': 90, 'xiaohuang': 85}, the type is <class 'dict'>
```

注意⚠️：
==字典中的key是不可重复的==

如果重复，同一个key，后定义的value会覆盖之前的value。

```python
my_dist={"xiaoming":99,"xiaohua":90,"xiaohuang":85,"xiaohua":92} # 这里重复定义了xiaohua
print(f"the constant is {my_dist}, the type is {type(my_dist)}")
>>
the constant is {'xiaoming': 99, 'xiaohua': 92, 'xiaohuang': 85}, the type is <class 'dict'>
```

**从字典中基于key获得value**：

```python
my_dist={"xiaoming":99,"xiaohua":90,"xiaohuang":85}
score=my_dist["xiaohua"] # 直接搜索key就好，会有匹配到value
print(score)
>>
90
```



在字典中，key和value可以说任意数据类型（⚠️但是key不可以为字典）

所以，字典是可以嵌套的

**字典的嵌套：**

![image-20240304192551295](/Users/mac/Documents/学习/python/python学习/image-20240304192551295.png)

```python
score_dist={"jack":{"chinese":77,"math":66,"English":33},
            "Mark":{"chinese":88,"math":86,"English":55},
            "jolin":{"chinese":99,"math":96,"English":66}}
print(score_dist)
score=score_dist["jolin"]["chinese"] # 嵌套字典查询
print(score)
>>
{'jack': {'chinese': 77, 'math': 66, 'English': 33}, 'Mark': {'chinese': 88, 'math': 86, 'English': 55}, 'jolin': {'chinese': 99, 'math': 96, 'English': 66}}
99
```

**字典的常用操作：**

1. 新增元素

`字典[key]=value`

字典被修改，新增了元素

```python
score_dist={"chinese":99,"math":96,"English":66}
score_dist["pc"]=87
print(score_dist)
>>
{'chinese': 99, 'math': 96, 'English': 66, 'pc': 87}
```

2. 更新元素

`字典[key]=value`

字典被修改，元素被更新

```python
score_dist={"chinese":99,"math":96,"English":66}
score_dist["English"]=87
print(score_dist)
>>
{'chinese': 99, 'math': 96, 'English': 87}
```

3.删除元素

`字典.pop(key)`

获得指定key的value；同时字典被修改，指定key的数据被删除

```python
score_dist={"chinese":99,"math":96,"English":66}
value=score_dist.pop("chinese")
print(score_dist)
print(value)
>>
{'math': 96, 'English': 66}
99
```

4. 清空字典

`字典.clear()`

结果：字典被修改，元素被清空

```python
score_dist={"chinese":99,"math":96,"English":66}
score_dist.clear()
print(score_dist)
>>
{}
```

5. 获得全部的key

```python
score_dist={"chinese":99,"math":96,"English":66}
keys=score_dist.keys()
print(keys)
>>
dict_keys(['chinese', 'math', 'English'])
```

6. 遍历字典

不支持while循环遍历

```python
# 方法1 通过获得全部的key来完成循环
score_dist={"chinese":99,"math":96,"English":66}
keys=score_dist.keys()
for key in keys:
    print(f"{key}:{score_dist[key]}")
>>
chinese:99
math:96
English:66

# 方法2 直接用for循环，每一次循环都是直接得到key
score_dist={"chinese":99,"math":96,"English":66}
for key in score_dist:
    print(f"{key}:{score_dist[key]}")

>>
chinese:99
math:96
English:66
```

7. 统计字典中元素数量

```python
score_dist={"chinese":99,"math":96,"English":66}
num=len(score_dist)
print(num)
>>
3
```

**小练习：**
![image-20240305101940467](/Users/mac/Documents/学习/python/python学习/image-20240305101940467.png)

```python
satff_dist={"王力宏":{"department":"technology department","salary":3000,"level":1},
            "周杰伦":{"department":"market department","salary":5000,"level":2},
            "林俊杰":{"department":"market department","salary":7000,"level":3},
            "张学友":{"department":"technology department","salary":4000,"level":1},
            "刘德华":{"department":"market department","salary":6000,"level":2}}
for key in satff_dist:
    for key1 in satff_dist[key]:
        if satff_dist[key][key1]==1:
            satff_dist[key][key1]+=1
            satff_dist[key]["salary"]+=1000

print(satff_dist)
>>
{'王力宏': {'department': 'technology department', 'salary': 4000, 'level': 2}, '周杰伦': {'department': 'market department', 'salary': 5000, 'level': 2}, '林俊杰': {'department': 'market department', 'salary': 7000, 'level': 3}, '张学友': {'department': 'technology department', 'salary': 5000, 'level': 2}, '刘德华': {'department': 'market department', 'salary': 6000, 'level': 2}}
```

## 38.类数据容器

![image-20240305105810584](/Users/mac/Documents/学习/python/python学习/image-20240305105810584.png)

**不支持下标索引和重复元素**：

集合、字典

<u>支持：列表、元组、字符串</u>

**不支持修改**：
元组、字符串

<u>支持：列表、集合、字典</u>

![image-20240305110448391](/Users/mac/Documents/学习/python/python学习/image-20240305110448391.png)

![image-20240305110609397](/Users/mac/Documents/学习/python/python学习/image-20240305110609397.png)

## 39.数据容器的通用操作

1. **遍历**

在遍历上，==5类数据容器都支持for循环==

列表、元组、字符串支持while循环，<u>集合、字典不支持</u>

2. **len**统计容器的元素

<u>5类数据类型都支持</u>

`len(my_list)\len(my_tuple)\len(my_str)`

3. **max**统计容器的最大元素

<u>5类数据类型都支持</u>

`max(my_list)\max(my_tuple)\max(my_str)`



```python
my_list=[1,2,3,4]
my_tuple=(1,2,3,4,5,6)
my_str="jolin"
print("最大元素:",end=' ')
print(max(my_list),end=' ')
print(max(my_tuple),end=' ')
print(max(my_str))
print("最小元素:",end=' ')
print(min(my_list),end=' ')
print(min(my_tuple),end=' ')
print(min(my_str))
print("容器内元素个数:",end=' ')
print(len(my_list),end=' ')
print(len(my_tuple),end=' ')
print(len(my_str))
>>
最大元素: 4 6 o
最小元素: 1 1 i
容器内元素个数: 4 6 5
```

4. **容器的通用类型转换**

没有办法转换成**字典**的，因为字典要求值储存为键值队

- `list(容器)` 将给定容器转换为列表

```python
my_list=[1,2,3,4]
my_tuple=(1,2,3,4,5,6)
my_str="jolin"
print(list(my_str))
print(list(my_tuple))
>>
['j', 'o', 'l', 'i', 'n']
[1, 2, 3, 4, 5, 6]
```

- `str(容器)`将给定容器转换为字符串

```python
my_list=[1,2,3,4]
my_tuple=(1,2,3,4,5,6)
my_str="jolin"
print(str(my_list))
print(str(my_tuple))
>>
[1, 2, 3, 4]
(1, 2, 3, 4, 5, 6)
```

- `tuple(容器)`将给定容器转换为元组

```python
my_list=[1,2,3,4]
my_tuple=(1,2,3,4,5,6)
my_str="jolin"
my_set={1,2,3,4,5}
my_dict={"key1":1,"key2":2,"key3":3}
print(tuple(my_list))
print(tuple(my_str))
print(tuple(my_set))
print(tuple(my_dict)) # 只会保存key，会丢失value
>>
(1, 2, 3, 4)
('j', 'o', 'l', 'i', 'n')
(1, 2, 3, 4, 5)
('key1', 'key2', 'key3')
```

- `set(容器)`将给定容器转化为集合

```python
my_list=[1,2,3,4]
my_tuple=(1,2,3,4,5,6)
my_str="jolin"
my_set={1,2,3,4,5}
my_dict={"key1":1,"key2":2,"key3":3}
print(set(my_list))
print(set(my_str))
print(set(my_tuple))
print(set(my_dict))
>>
{1, 2, 3, 4}
{'n', 'o', 'i', 'j', 'l'}
{1, 2, 3, 4, 5, 6}
{'key2', 'key1', 'key3'}
```

5. 容器通用排序功能

`sorted(容器,[reverse=True])` 将给定容器进行排序

```python
my_list=[1,2,3,4]
my_tuple=(1,2,3,4,5,6)
my_str="jolin"
my_set={1,2,3,4,5}
my_dict={"key1":1,"key2":2,"key3":3}
# 正向排序
print(sorted(my_list))
print(sorted(my_tuple))
print(sorted(my_str))
print(sorted(my_set))
print(sorted(my_dict))
>>
[1, 2, 3, 4]
[1, 2, 3, 4, 5, 6]
['i', 'j', 'l', 'n', 'o']
[1, 2, 3, 4, 5]
['key1', 'key2', 'key3']


my_list=[1,2,3,4]
my_tuple=(1,2,3,4,5,6)
my_str="jolin"
my_set={1,2,3,4,5}
my_dict={"key1":1,"key2":2,"key3":3}
# 降序排列
print(sorted(my_list,reverse=True))
print(sorted(my_tuple,reverse=True))
print(sorted(my_str,reverse=True))
print(sorted(my_set,reverse=True))
print(sorted(my_dict,reverse=True))
>>
[4, 3, 2, 1]
[6, 5, 4, 3, 2, 1]
['o', 'n', 'l', 'j', 'i']
[5, 4, 3, 2, 1]
['key3', 'key2', 'key1']
```

## 40.字符串大小比较

字符串通过min()和max(),可以将字符串排序

那么，它是以怎样的方式进行排序的呢？

![image-20240305151722022](/Users/mac/Documents/学习/python/python学习/image-20240305151722022.png)

通过ASCII码表中的<u>==码值==进行比较</u>

**字符串比较：**
字符串是按位比较，也就是一位一位比，只要哪一位大，那么整体就大

eg. abd>abc; ab>a

## 41.函数多返回值

当一个函数，<u>存在两个reurn</u>

只执行了第一个return，原因因为return可以退出当前函数，<u>导致return下方的代码不执行</u>

```python
def test_return():
    return 1,"hello"
x,y=test_return()
print(x)
print(y)
>>
1
hello
```

## 42.函数的多种参数形式

**位置参数**：调用函数时，根据函数定义的<u>参数位置</u>来传递参数

注意⚠️：传递参数和定义的参数的顺序及个数必须一致

```python
def user_info(name,age,gender):
    print(f"your name is {name}, your age is {age}, your gender is {gender}")

user_info('Tom',20,'male')
>>
your name is Tom, your age is 20, your gender is man
```

**关键字参数：**
函数调用时，通过"**键=值"**形式，传递参数

可以让函数更加清晰、容易使用，同时也<u>清除了参数的顺序要求</u>

注意⚠️：<u>位置参数在关键字参数的**前面**</u>，但关键字参数之间不存在先后顺序

```python
def user_info(name,age,gender):
    print(f"your name is {name}, your age is {age}, your gender is {gender}")

user_info('Tom',20,'male')
user_info("xiaohua",gender='male',age=18)
>>
your name is Tom, your age is 20, your gender is male
your name is xiaohua, your age is 18, your gender is male
```

**缺省参数：**
默认值参数

注意⚠️：默认值必须是放在**最后**

```python
def user_info(name,age,gender='male'):
    print(f"your name is {name}, your age is {age}, your gender is {gender}") 

user_info('Tom',20) #这里没有定义，但是后面输出的时候还是gender=male
user_info("xiaohua",gender='male',age=18)
>>
your name is Tom, your age is 20, your gender is male
your name is xiaohua, your age is 18, your gender is male
```

**不定长参数：**
不定长参数也叫可变参数，用于<u>不确定调用的时候会传递多少个参数</u>

- 位置传递

传入的所有参数都会被收集，它会根据参数的位置合并为一个**元组**(tuple),也就是传递位置

```python
def user_info(*args):
    print(args)
user_info('Tom',12,34)
>>
('Tom', 12, 34)
```

- 关键字传递

```python
def user_info(**args):
    print(args)
user_info(name='Tom',age=12,level=34)
>>
{'name': 'Tom', 'age': 12, 'level': 34}
```

参数时“键=值”形式的情况下，所有键值都会被接受，会依次形成**字典**

## 43.匿名函数

**函数作为参数传递**：

这是一种**计算逻辑的传递**，而不是数据的传递

```python
def test_function(compute):
    reslut=compute(1,2)
    print(reslut)
    print(type(compute))
def compute(x,y):
    return x+y
test_function(compute)
>>
3
<class 'function'>
```

**lambda匿名函数：**

def关键字，可以<u>定义带有名称的函数</u>

lambda关键字，可以<u>定义匿名函数</u>（无名称）

有名称的函数，可以基于名称重复使用

==**无名称函数，只可以使用一次**== 用于临时构建一个函数

**定义语法：**

`lambda 传入函数：函数体（一行代码）`

```python
def test_function(compute):
    reslut=compute(1,2)
    print(reslut)
test_function(lambda x,y:x+y)
>>
3
```

## 44.文本

1. 本文文件通过编码技术（密码本）将内容翻译为0和1存入

编码技术：内容——二进制——内容 （<u>utf-8</u>,gbk,big5....)

2. **文件操作**

- 打开文件

`open()`使用open函数，可以打开一个已经存在的文件，或者创建一个新文件

语法：`open(name,mode,encoding)`

Name: 要打开文件名的字符串<u>（可以包含文件的具体路径）</u>

mode：设置打开文件的模式（只读、写入、追加）

encoding：编码格式

```python
f=open('python.txt','r',encoding=UTF-8) # 要使用关键字传参
```

其中，f是open函数的文件对象，拥有属性和方法，可以使用对.属性或者对象.方法对其进行访问

![image-20240306114058802](/Users/mac/Documents/学习/python/python学习/image-20240306114058802.png)

```python
f=open('python.txt','w',encoding="UTF-8")
print(type(f))
>>
<class '_io.TextIOWrapper'>
```

- 读写文件

**读取文件**

```python
f=open('python.txt','r',encoding="UTF-8")
print(f"the readed constant is {f.read(5)}")# 读5个字节

f=open('python.txt','r',encoding="UTF-8")
print(f"the readed constant is {f.read()}")# 读取全部字节

f=open('python.txt','r',encoding="UTF-8")
print(f"the readed constant is {f.readlines()}")# 读取全部行，然后封装到列表中
print(type(f.readlines()))
>>
the readed constant is ['jolin\n', '666']
<class 'list'>

f=open('python.txt','r',encoding="UTF-8")
print(f"the line1 constant is {f.readline()}")# 一次读一行
print(f"the line2 constant is {f.readline()}")# 一次读一行
>>
the line1 constant is jolin
the line2 constant is 666
```

**for循环读取文件：**

```python
f=open('python.txt','r',encoding="UTF-8")
for line in f: # 会读出每一行数据
    print(f"the constant is the {line}")
>>
the constant is the jolin
the constant is the 666
```

注意⚠️：当代码里面多次read文件时，第一次后面的read不会从头开始，而是会**接着读取**

**写入文件：**
`f=open('python.txt','w)`

`f.write("hello world")`

`f.flush`

直接调用write，内容并不会真正写入文件，而是会积攒在<u>缓冲区</u>

==当调用flush的时候，内容才会写入文件==

这样是为了避免频繁的操作硬盘，导致效率下降

注意⚠️：

w模式，文件不存在，会创建新文件

w模式，文件存在，会清空原有内容

<u>colse()自带flush()功能</u>

```python
f=open('test.txt','w',encoding="UTF-8")
f.write("Hello world!")
f.flush()
```

**追加文件：**

`f=open('python','a')`

`f.write("hello world")`

`f.flush()`

注意⚠️：

a模式，文件不存在会创建文件；

a模式，文件存在会在最后<u>追加写入文件</u>

```python
f=open('test.txt','a',encoding="UTF-8")
f.write("\nHallo world!")
f.flush()
f.close()
```

- 关闭文件

如果不关闭，文件会被程序占用文件

`f.close()`

还有另外一种方法：
`with open('python.txt','w',encoding="UTF-8")as f:`

这个语法会<u>自动关闭文件</u>

**小练习：**

统计文本中<u>某个字符串出现次数</u>

```python
f=open('python.txt','r',encoding="UTF-8")
count=0
for line in f:
    line=line.strip()
    words=line.split(" ")	
    for word in words:
        if word=='itheima':
            count+=1
print(count)
>>
6
```

**综合练习：**

```python
f=open('test.txt','r',encoding="UTF-8")
f1=open('test1.txt','w',encoding="UTF-8")
for line in f:
    line=line.strip()
    words=line.split(",")
    if words[4]=="测试":
        continue
    else:
        f1.write(f"\n {line}")
f.close()
f1.close()
```

## 45.异常

什么是异常？

当检测到一个错误时，python解释器无法继续执行——异常（Bug）

**捕获异常**：异常处理

对bug进行适当的提醒，整个程序继续运行

==提前假设某处会出现异常==，做好提前准备，当真的出现异常的时候，可以有后续手段

`try:`
	可能发生错误的代码

`except:`

​	如果出现异常，执行的代码

```python
try:
    f=open("abc.txt",'r',encoding="UTF-8")
except:
    print("there has a error")
    f=open("abc.txt",'w',encoding="UTF-8")
>>

```

**捕获指定异常：**
基本语法：

```python
try:
	print(name)
except NameError as e: # NameError类错误才会捕获
	print("name名称未定义错误")
```

1. ﻿如果尝试执行的代码的异常类型和要捕获的异常类型不一致，则无法捕获异常
2. ﻿﻿一般try下方只放一行尝试执行的代码

**捕获多个异常：**
基本语法：

```python
try:
	print(name)
except (NameError,ZeroDivisionError)as e:
	print("name名称未定义错误或除0错误")
```

**捕获所有异常：**
`except:` 和 `except Exception as e:` 都是捕获全部异常

```python
try:
    1/0
except Exception as e:
    print("异常")
```

**异常else：**

```python
try:
	print(1)
except Exception as e:
  print(e)
else:    # 如果没有异常时，执行的代码
	print("there is no false")
```

**异常finally：**

```python
try:
	f=open('test.txt','r')
except Exception as e:
	f=open('test.txt','w')
else:
	print('没有异常')
finally:   # 无论是否有异常，都要执行的代码
	f.close()
```

**异常的传递：**
当所有函数都没有捕获到异常的时候，程序就会出错

```python
def func1():
    print("start func1")
    num=1/0
    print("func1 end")
def fun2():
    print("start func2")
    func1()
    print("func2 end")
def main():
    try:
        fun2()
    except Exception as e:
        print("error")

main()
>>
start func2
start func1
error
```

这也就说明了，我们不一定要在低层级就捕获错误；我们可以在高层级进行捕获，因为他会传递上来

## 46.python模块

**模块的导入**

模块是一个pytho文件，模块内包含可执行代码

python中有很多不同的模块，每一个模块可以<u>帮助我们快速实现一些功能</u>

我们可以认为模块就是一个==工具包==

注意⚠️：
python模块导入需要写在<u>代码文件的开头位置</u>

导入方式：
`[from 模块名] import [模｜类｜变量｜函数｜*] [as 别名]`

```python
import 模块名
import 模块名1，模块名2
模块名.功能名()
```

```python
import time #导入python内置的time模块，模块中所有的功能都能用
print("start")
time.sleep(1)
print("end")
>>
start
end

from time import sleep #只导入time中的sleep方法
print("start")
sleep(1) # 所以这里也不需要time.sleep了
print("end")
>>
start
end

from time import* #这样的写法也是导入time的所有功能
print("start")
sleep(1) #只不过这里也可以直接调用就好
print("end")
>>
start
end

import time as tt # 给模块设置一个别名
print("start")
tt.sleep(1) # 后面调用的时候，直接用别名就好
print("end")
>>
start
end

from time import sleep as sl # 设置别名
print("start")
sl(1)
print("end")
>>
start
end
```

**自定义模块**

有时候我们需要一些个性化的模块，我们通过自定义模块实现，也就是自己制作一个模块

方法：
新建一个python文件，然后在文件里面定义函数；当我们要用的时候，直接import就好

注意⚠️：每一个文件的名称就是模块名，所以一定要<u>注意命名规则</u>

```python
import my_module1

my_module1.test(1,2) # 自己在另外一个文件里面
>>
3
```

如果有**重名模块**：

```python
# 模块1代码
def my_test(a,b):
  print(a+b)
  
# 模块2代码
def my_test(a,b):
	print(a-b)
  
# 导入模块和调用功能代码
from my_module1 import my_test
from my_module2 import my_test # 后面这个会把前面这个覆盖掉

# my_test函数是模块2种的函数
my_test(1,1)
```

**测试模块：**

在实际开发过程中，为了让模块能够在项目中达到想要的结果

```python
def test(a,b):
	print(a+b)
  
test(1,1) # 写完代码，进行测试
```

```python
# 解决方案
def test(a,b):
  print(a+b)
  
# 只在当前文件中调用改函数，其他导入文件时不会被直接输出
if __name__ =="__main__":
  test(1,1)
```

`if --name-- =="--main--":`

满足了测试时测试用例的运行，在文件被调用时不会被直接输出

**all**:

如果文件中有"--all--"变量，当使用`'from xxx import *'`导入时，只会导入列表中的函数

```python
__all__=['test1']
def test(a,b):
    print(a+b)
def test1(a,b):
    print(a-b)
if __name__ == '__main__':
    test(1,2)
    
from my_module1 import*

test(1,2)# 这里就会报错
```

## 47.python包

- **自定义包**

基于Python模块，我们可以在编写代码的时候，导入许多外部代码来丰富功能。但是，如果Python的模块太多了，就可能造成一定的混乱。

python模块就是文件；

python包就可以看成是一个<u>文件夹</u>，包的作用就是包含多个模块，帮助我们管理模块

![image-20240307210227204](/Users/mac/Documents/学习/python/python学习/image-20240307210227204.png)

`__init.py__`存在在文件夹里面的话就是python包，如果没有就算普通文件夹

选择新建一个包，包里面就会自动创建一个 `__init__.py`文件

**导入包：**

<u>方法一：</u>

`import 包名.模块名`

```python
# 方法1
import my_package.my_module1
import my_package.my_module2

my_package.my_module1.infp_print1()
my_package.my_module2.info_print2()

#方法2
from my_package import my_module1
from my_package import my_module2

my_module1.infp_print1()
my_module2.info_print2

#方法3
from my_package.my_module1 import infp_print1
from my_package.my_module2 import info_print2
infp_print1()
info_print2()
```

<u>方法二：</u>
必须在__init.py__文件中添加"--all--=[]",控制允许导入的模块列表

`from 包名 import*`

`模块名.目标`

```python
__all__=["my_module2"]

from my_package import *
my_module2.info_print2()
```

- **安装第三方包**

![image-20240307214752880](/Users/mac/Documents/学习/python/python学习/image-20240307214752880.png)

但是由于是第三方包，python没有内置，所以我们需要安装它们才能导入使用

第三方包的安装非常简单，我们只需要使用Python内置的**pip程序**即可

**方法：**

命令提示符程序，在里面输入：

pip install 包名称

即可通过网络快速安装第三方包

**综合练习：**
![image-20240307222231497](/Users/mac/Documents/学习/python/python学习/image-20240307222231497.png)

```python
def str_reverse(s):
    """
    return reverse string
    :param s: 接受字符串
    :return: 返回反转后对字符串
    """
    new_str=s[::-1]
    return new_str

def substr(s,x,y):
    """
    通过给定下标，对字符串切片
    :param s: 接受字符串
    :param x: 开始下标
    :param y: 结束下标
    :return:
    """
    return s[x:y]

if __name__ == '__main__':
    print(str_reverse("good day"))
    print(substr("hello",1,3))
```



```python
def print_file_info(file_name):
    """
    将给定路径对文件内容输出到控制台
    :param file_name: 文件路径
    :return: 文件内容
    """
    f=None
    try:
        f=open(file_name,'r',encoding="UTF-8")
        content=f.read()
        print("The content is :")
        print(content)
    except Exception as e:
        print(f"Error! The reson is {e}")
    else:
        print("there is no false")
    finally:
        if f: # 如果变量是None，表示False，如果有任何内容，就是True
            f.close()
def append_to_file(file_name):
    f=open(file_name,"a",encoding="UTF_8")
    f.write(data)
    f.write("\n")
    f.close()

if __name__ == '__main__':
    print_file_info()
```

## 48.数据可视化

主要使用，echarts

- **json数据格式**

json本质上是一个<u>带有特定格式的字符串</u>

==json是编程语言中通用的数据格式==，负责不同编程语言中的数据传递和交互；所以json是一种良好的中转数据格式。

在python语言来看，json数据格式就是一个字典，或者说包含字典的列表。

1. python数据与json数据的互相转换

```python
# 导入json模块
import json
# 准备符合json格式的要求的python数据
data=[{"name":"xiaoming","age":18},{"name":"xiaozhang","age":22}]
# 通过dumps方法将python数据转化为json数据
data=json.dumps(data)
# 通过loads方法将json数据转化为python数据
data=json.loads(data)
```

```python
import json

data=[{"name":"xiaoming","age":18},{"name":"xiaozhang","age":22}]
json_str=json.dumps(data) # 将列表转换为json格式
print(type(json_str))
print(json_str)
>>
<class 'str'> # 已经转换为str
[{"name": "xiaoming", "age": 18}, {"name": "xiaozhang", "age": 22}]

import json

s='[{"name":"xiaoming","age":18},{"name":"xiaozhang","age":22}]'
l=json.loads(s) #将json格式转化为
print(type(l))
print(l)
>>
<class 'list'>
[{'name': 'xiaoming', 'age': 18}, {'name': 'xiaozhang', 'age': 22}]

```

- **pyecharts模块**

Echarts是个由百度开源的数据可视化，凭借着良好的交互性，精巧的图表设计，得到了众多开发者的认可，而 Python 是门富有表达力的语言，很适合用于数据处理.当数据分析遇上数据可视化时pyecharts

官网画廊：https://gallery.pyecharts.org/

**用pycharts画折线图：**

```python
from pyecharts.charts import Line

line=Line() # 得到折线图对象 （得到一个空的二维坐标系）
line.add_xaxis(["China","USA","England"]) # 添加x轴数据
line.add_yaxis("GDP",[30,20,10]) # 添加y轴数据
line.render() # 生成图表
>>
会生成一个html文件
```

1. 全局配置选项

`set_gobal_opts`配置标题、图例、工具箱等

![image-20240310225033567](/Users/mac/Documents/学习/python/python学习/image-20240310225033567.png)

```python
from pyecharts.charts import Line
from pyecharts.options import TitleOpts,LegendOpts,ToolboxOpts,VisualMapOpts

line=Line() # 得到折线图对象
line.add_xaxis(["China","USA","England"]) # 添加x轴数据
line.add_yaxis("GDP",[30,20,10]) # 添加y轴数据
line.set_global_opts(
    title_opts=TitleOpts(title="show GDP",pos_left="center",pos_bottom="1%"),
    legend_opts=LegendOpts(is_show=True),
    toolbox_opts=ToolboxOpts(is_show=True),
    visualmap_opts=VisualMapOpts(is_show=True)
)
line.render() # 生成图表
```

2. 系列配置选项

具体数据

## 49.初识对象

1. 在程序中设计表格，设计**class**类

   ```python
   class Student:
   	name=None
   ```

2. 打印表单，创建**对象**

   ```python
   # 基于类创建对象
   stu_1=Student()
   stu_2=Student()
   ```

3. 在程序中填写表格，**对象属性赋值**

   ```python
   stu_1.name="jaychou"
   stu_2.name="linjj"
   ```

```python
class Student:
    name=None # 记录学生姓名
    gender=None # 记录学生性别
    nationality=None #记录学生国际
    native_place=None # 记录学生籍贯
    age=None

stu_1=Student()
stu_1.name="xiaochang"
stu_1.gender="man"
stu_1.nationality="China"
stu_1.native_place="Shandong"
stu_1.age=31

print(stu_1.name)
print(stu_1.gender)
print(stu_1.nationality)
print(stu_1.native_place)
print(stu_1.age)
```

## 50.类的成员方法

**类的定义和使用：**

class关键字，表示要定义类了

- 类的属性：类中的变量（成员变量）
- 类的行为：类中的函数（成员**方法**）

1. 创建类的语法：

   `对象=类名称()`

2. 成员方法的定义语法：

​	`def 方法名(self,形参1,形参2,形参3...)`
注意⚠️：

1. self关键字在成员方法定义的时候，<u>必须填写</u>

2. 用它来<u>表示类对象自身</u>的意思；
3. 在方法内部，想要<u>访问类的成员变量，必须使用self</u>
4. self关键字，尽管在参数列表中，但是传参的时候可以<u>忽略它</u>

```python
class Student:
    name=None
    def say_hi(self):
        print(f"Hello everyone,i am {self.name}")

stu=Student() #对象
stu.name="xiaohua"
stu.say_hi()
>>
Hello everyone,i am xiaohua
```

```python
class Student:
    name=None
    def say_hi(self):
        print(f"Hello everyone,i am {self.name}")
    def say_hi2(self,msg):
        print(f"Hello everyone,i am {self.name},{msg}")

stu=Student()
stu.name="xiaohua"
stu.say_hi2("I'm from hunan.")
>>
Hello everyone,i am xiaohua,I'm from hunan.
```

## 51.类和对象

面向对象编程：设计类，基于类创建对象；==由对象做具体工作==

```python
class Clock:
    id=None
    price=None

    def ring(self):
        import winsound # mac don't have this module
        winsound.Beep(2000,1000)
# creat two clock object and let them work
clock1=Clock()
clock1.id="00001"
clock1.price=19
print(f"The id: {clock1.id},the price:{clock1.price}")
clock1.ring()

clock2=Clock()
clock2.id="00002"
clock2.price=22
print(f"The id: {clock2.id},the price:{clock2.price}")
```

## 52.构造方法

![image-20240312113955989](/Users/mac/Documents/学习/python/python学习/image-20240312113955989.png)

- 属性变量赋值

```python
class Student:
    # there define is not necessary
    # name=None
    # age=None
    # tel=None

    def __init__(self,name,age,tel):
        self.name=name # 这里在赋值的同时，成员变量也就创建了
        self.age = age
        self.tel = tel
        print("Student class has creat an object")

stu=Student("xiaozhang",31,"15200800956")
>>
Student class has creat an object
```

注意⚠️：

在构造方法内定义成员变量，<u>需要使用self关键字</u>

## 53.内置方法

1. `__init__` 构造方法
2. `__str__` 字符串方法
3. `__lt__` 小于、大于符合比较
4. `__le__`  小于等于、大于等于符号比较
5. `__eq__` ==符号比较

还有很多内置方法，这里只关注几个较为常见的

```python
class Student:

    def __init__(self,name,age,tel):
        self.name=name
        self.age = age
        self.tel = tel
        print("Student class has creat an object")

stu=Student("xiaozhang",31,"15200800956")
print(stu)
print(str(stu))
>>
<__main__.Student object at 0x102dacad0> # 会返回内存地址,但是地址对我们来说没什么大用处
```

```python
# 1.__str__
class Student:

    def __init__(self,name,age,tel):
        self.name=name
        self.age = age
        self.tel = tel
        print("Student class has creat an object")

    def __str__(self):
        return f"Student,name={self.name},age={self.age},tel={self.tel}" # 不再输出内存地址，而是输出自定义输出内容

stu=Student("xiaozhang",31,"15200800956")
print(stu)
>>
Student class has creat an object
Student,name=xiaozhang,age=31,tel=15200800956
```

```python
# 2.__lt__（同理__le__;__eq__;
class Student:

    def __init__(self,name,age,tel):
        self.name=name
        self.age = age
        self.tel = tel


stu1=Student("xiaozhang",31,"15200800956")
stu2=Student("xiaozhang",21,"12345643")
print(stu1<stu2) # 直接对两个对象进行比较少不可以的
>>
Traceback (most recent call last):
  File "/Users/mac/Documents/学习/python/project1/project1/钱包余额.py", line 11, in <module>
    print(stu1<stu2)
          ^^^^^^^^^
TypeError: '<' not supported between instances of 'Student' and 'Student'
```

```python
class Student:

    def __init__(self,name,age,tel):
        self.name=name
        self.age = age
        self.tel = tel
    def __lt__(self,other): # 可以同时完成小于和大于两种比较
        return self.age < other.age

stu1=Student("xiaozhang",31,"15200800956")
stu2=Student("xiaozhang",21,"12345643")
print(stu1<stu2)
print(stu1>stu2)
>>
False
True
```

## 54.封装

面向对象三大特性：封装、继承、多态

私有成员：`__作为开头的成员变量以及成员方法`

既然现实事物有不公开的属性和行为，那么作为现实事物在程序中映射的类，也应该支持<u>私有成员变量</u>、<u>私有成员方法</u>。

![image-20240312155402188](/Users/mac/Documents/学习/python/python学习/image-20240312155402188.png)

```python
class Phone:
    IMEI=None
    producer=None

    __current_voltage=None
    def call_by_Sg(self):
        print("call is enable")

    def __keep_single(self):
        print("keep is single")

phone=Phone()
phone.__keep_single=33 # 私有方法无法直接被类对象使用 
phone.__keep_single() # 私有变量无法赋值，也无法获取值
>>
error
```

注意⚠️： 私有成员无法被类对象使用，但是**可以被其他成员使用**，也就是说私有成员可以在内部使用，但是没法到类对象那里使用

```python
class Phone:
    __current_voltage=1

    def __keep_singlr_core(self):
        print("single core")

    def call_by_5g(self):
        if self.__current_voltage>=1:
            print("5g is open")
        else:
            self.__keep_singlr_core()
            print("voltage is low")

phone=Phone()
phone.call_by_5g()
>>
5g is open
```

**小练习：**
![image-20240312164105574](/Users/mac/Documents/学习/python/python学习/image-20240312164105574.png)

```python
class Phone:
    __current_voltage=True
    def __check_5g(self):
        if self.__current_voltage==True:
            print("open 5g")
        else:
            print("close 5g, open 4g")
    def call_by_5g(self):
        self.__check_5g()
        print("calling...")

phone=Phone()
phone.call_by_5g()
>>
open 5g
calling...
```

## 55.继承

![image-20240312171253188](/Users/mac/Documents/学习/python/python学习/image-20240312171253188.png)

基于**之前的类**进行修改

- 单继承 （一个子类继承一个父类）

```python
class 类名（父类名）：
	类内容体
```

```python
class Phone:
    IMEI=None
    producer="China"

    def call_by_4g(self):
        print("called by 4g")

class newPhone(Phone):
    face_id="1001"
    def call_by_5g(self):
        print("called by 5g")

phone=newPhone()
print(phone.producer) # 这个不在newPhone里面，但是依旧可以调用		
phone.call_by_4g()
phone.call_by_5g()
>>
China
called by 4g
called by 5g
```

- 多继承 （一个子类继承多个父类）

```python
class Phone:
    IMEI=None
    producer="China"

    def call_by_4g(self):
        print("called by 4g")

class NFCReader:
    nfc_type=5
    producer="China"

    def read_card(self):
        print("reading")

    def write_card(self):
        print("writing card")

class RemoteControl:
    rc_type="RemoteControl"
    def control(self):
        print("control")

class myPhone(Phone,RemoteControl,NFCReader):
    pass #

phone=myPhone()
phone.call_by_4g()
phone.read_card()
phone.write_card()
phone.control()
>>
called by 4g
reading
writing card
control
```

注意⚠️：

1. 如果父类中的成员==同名==，那么默认以<u>继承顺序（从左到右）为优先级</u>

> 比如class myPhone(Phone,RemoteControl,NFCReader):其中Phone里面有name=xiaohua，RemoteControl=xiaoming，那么最后调用结果为xiaohua

2. pass是占位语句，用来保证函数或定义的完整，表示无内容，空的意思

- 复写父类成员的语法

子类继承父类的成员属性和成员方法，如果对其“不满意”可以进行复写

```python
class Phone:
    IMEI=None
    producter="ITCAST"

    def call_by_sg(self):
        print("called by 5g")

class newPhone(Phone):
    producter = "CAST"

    def call_by_sg(self):
        print("called by 5g new")

phone=newPhone()
phone.call_by_sg()
print(phone.producter)
>>
called by 5g new
CAST
```

- 在子类中调用父类成员

1. 调用父类成员

使用成员变量：父类名.成员变量

使用成员方法：父类名.成员方法(self)

2. 使用super()

使用成员变量：super().成员变量

使用成员方法：super().成员方法()

```python
# 方法1
class Phone:
    IMEI=None
    producter="ITCAST"

    def call_by_sg(self):
        print("called by 5g")

class newPhone(Phone):
    producter = "CAST"

    def call_by_sg(self):
        print("called by 5g new")
        Phone.call_by_sg(self) #调用父类成员

phone=newPhone()
phone.call_by_sg()
print(phone.producter)
>>
called by 5g new
called by 5g
CAST

# 方法2
class Phone:
    IMEI=None
    producter="ITCAST"

    def call_by_sg(self):
        print("called by 5g")

class newPhone(Phone):
    producter = "CAST"

    def call_by_sg(self):
        print("called by 5g new")
        super().call_by_sg() #调用父类成员

phone=newPhone()
phone.call_by_sg()
print(phone.producter)
>>
called by 5g new
called by 5g
CAST
```

注意⚠️：

父类同名函数，如果子类复写会被代替，但是调用父类成员时还是不会变的

## 56.类型注解

![image-20240312215930860](/Users/mac/Documents/学习/python/python学习/image-20240312215930860.png)

- 变量

变量的类型注解：

`变量:类型`

```python
var_1:int=10
var_2:float=3.14
var_3:bool=True
var_4:str="hello"
```

```python
class Student:
	pass
stu:Student=Student()
```

- 容器

```python
# 容器类型注解
my_list:list=[1,2,3]
my_tuple:tuple=(1,2,3)
my_set:set={1,2,3}
my_dict:dict={"China":1}
my_str:str="love"
```

```python
# 容器类型详细注解
my_list:list[int]=[1,2,3]
my_tuple:tuple[str,int,bool]=("china",1,True)
my_set:set[int]={1,2,3}
my_dict:dict[str,int]={"China":1}
my_str:str="love"
```

- 通过注释对类型进行注解 `#type:类型`

```python
import random
import json


class student:
    pass

var_1=random.randint(1,10) # type: int
var_1=json.loads('{"name":"zhangshan"}') # type: dict[str,str]

def func():
    return 10

var_3=func() # type:int
```

注意⚠️：

1. 一般在<u>无法直接看到变量类型</u>的时候添加变量的类型注解

![image-20240312224313975](/Users/mac/Documents/学习/python/python学习/image-20240312224313975.png)

2. 类型注解只是提示性的，**并不会对真正的类型做验证和判断**

```python
var_1:int="china"
var_2:str=1
# 这样也不会报错
```

- 函数和方法类型注解

![image-20240312225316552](/Users/mac/Documents/学习/python/python学习/image-20240312225316552.png)

```python
# 对形参进行注解
def add(x:int, y:int) :
    return x + y
  
# 对返回值进行注解
ef func(data:list)->list:
    return data
```

- Union 类型

注解描述混合类型

```python
my_list:list[int]=[1,2,3]
my_dict:dict[str,int]={"age",11}
# 但是出现混合情况怎么定义呢？
my_list=[1,2,"china"]
my_dict={"name":"xiaohua","age":11}
```

导入union

```python
from typing import Union
my_list:list[Union[str,int]]=[1,2,"china","haha"] # Union对混合变量注解
my_dict:dict[str,Union[str,int]]={"name":"xiahua","age":11}
```

```python
def func(data:Union[int,str])->Union[int,str]: # Union对函数注解
    pass
```

## 57.多态

**多态**，指的是：多种状态，即完成某个行为时，使用不同的对象会得到不同的状态。

1. <u>以父类做声明定义</u>
2. <u>以子类做实际工作</u>
3. 用以获得同一行为，不同状态

> 比如函数方法形参声明接受父类对象，但是实际传入子类对象进行工作

```python
class Animal:
    def speak(self):
        pass # 这里是一个空实现，所以称之为抽象方法

class Dog(Animal):
    def speak(self):
        print("dog")

class Cat(Animal):
    def speak(self):
        print("cat")

def make_noise(animal:Animal):
    animal.speak()

dog=Dog()
cat=Cat()
make_noise(dog)
make_noise(cat)
>>
dog
cat
```

抽象，一般用于顶层设计；我们<u>并不直接使用抽象类，而是使用它的具体子类</u>

配合多态，**完成抽象的父类设计以及具体的子类实现**

```python
class AC:
    def cool_wind(self):
        pass # 抽象类，用于顶层设计
    def hot_wind(self):
        pass
    def swing_wind(self):
        pass

class madi_AC(AC):
    def cool_wind(self):
        print("core technology") # 子类实际工作状态
    def hot_wind(self):
        print("hot technology")
    def swing_wind(self):
        print("switch technology")

class geli_AC(AC):
    def cool_wind(self):
        print("geli technology")
    def hot_wind(self):
        print("geli hot technology")
    def swing_wind(self):
        print("geli switch technology")

def make_cool(ac:AC):
    ac.cool_wind()

madi_ac=madi_AC()
geli_ac=geli_AC()

make_cool(madi_ac)
make_cool(geli_ac)
>>
core technology
geli technology
```

## 58.SQL

**数据库：**存储数据

库-表-数据

sql语言，就是对<u>数据库、数据进行操作、管理、查询的工具</u>，借助sql语言，完成对数据的**增删改差**





