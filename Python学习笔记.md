# 内容目录

[TOC]



# 11.14学习笔记

### Python环境安装

#### 1.认识Python

​	Python是一门解释型、面向对象的高级编程语言

​	Python是开源免费的、支持交互式、可跨平台移植的脚本语言（解释性执行的语言）

​	Python的2和3版本是不能兼容运行的（建议使用Python 3）

​	**特性：**

​	开源易于维护；

​	可以移植；

​	易于使用、简单优雅；

​	广泛的标准库、功能强大；

​	可扩展、可嵌入； 

​	**缺点：**

​	运行速度慢；

​	代码不能加密；

​    **人生苦短，我用Python**

#### 2.经典应用

​	框架，桌面开发，服务器软件、网络爬虫，游戏；

​	数据分析，科学计算，常规软件开发，人工智能，网络爬虫（主流是Python和Java），web开发。

#### 3.安装 Python

​	官网安装：www.python.org；根据系统选择相应版本

​	同时建议下载PyCharm

### 第一个Python程序

​	命令提示符运行python,注意配置好环境变量

​	pip是从网络上下载的程序

​	python之禅：

```python
The Zen of Python, by Tim Peters

Beautiful is better than ugly.
Explicit is better than implicit.
Simple is better than complex.
Complex is better than complicated.
Flat is better than nested.
Sparse is better than dense.
Readability counts.
Special cases aren't special enough to break the rules.
Although practicality beats purity.
Errors should never pass silently.
Unless explicitly silenced.
In the face of ambiguity, refuse the temptation to guess.
There should be one-- and preferably only one --obvious way to do it.
Although that way may not be obvious at first unless you're Dutch.
Now is better than never.
Although never is often better than *right* now.
If the implementation is hard to explain, it's a bad idea.
If the implementation is easy to explain, it may be a good idea.
Namespaces are one honking great idea -- let 's do more of those!
```

**结束（退出）Python命令提示符的方法：**

​	（1）使用exit()

​	（2）Ctrl+Z

**命令行执行文件**

​	命令行下转到文件所在目录使用

```
python xxxx.py
```



# 11.16学习笔记

### 用PyCharm编写程序

#### python单行注释

```python
#这是单行注释
```
#### python多行注释

```python
'''
（上下三个英文单引号）
这是第一行注释

这是第二行注释

'''
```

#### python输出

```python
#输出字符串

print("标准化字符串输出")

#输出变量

a = 10

print(a)

#输出字符串和变量

print("这是字符串",a)
```

#### 变量及类型

变量可以使任意的数据类型，在程序中用一个变量名表示

变量名必须是大小写英文、数字和下划线(_)的组合，且不能以数字开头

#### 标识符和关键字

标识符：变量名等

关键字：

```python
False	None	True	__peg_parser__	and		as	assert	async	await	break	class	continue	def		del	elif', 'else', 'except', 'finally', 'for', 'from', 'global', 'if', 'import', 'in', 'is', 'lambda', 'nonlocal', 'not', 'or', 'pass', 'raise', 'return', 'try', 'while', 'with', 'yield'
```

#### Python输出

```python
print("我的年纪是： %d 岁"%age)
  


#标准化格式输出，%d占位后面的%age是真实数值

#外加一些常用的占位格式符号

#%d  有符号十进制整数

#%s 通过str()字符串转化来格式化


#连接符号输出
print("www","baidu","com",sep = ".")

#换行输出
print("hello\n")


```

| 转换说明符 |                  解释                  |
| :--------: | :------------------------------------: |
|   %d、%i   |        转换为带符号的十进制整数        |
|     %o     |        转换为带符号的八进制整数        |
|   %x、%X   |       转换为带符号的十六进制整数       |
|     %e     | 转化为科学计数法表示的浮点数（e 小写） |
|     %E     | 转化为科学计数法表示的浮点数（E 大写） |
|   %f、%F   |           转化为十进制浮点数           |
|     %g     |       智能选择使用 %f 或 %e 格式       |
|     %G     |       智能选择使用 %F 或 %E 格式       |
|     %c     |        格式化字符及其 ASCII 码         |
|     %r     |  使用 repr() 函数将表达式转换为字符串  |
|     %s     |  使用 str() 函数将表达式转换为字符串   |

#### python输入

```python
passwd = input("请输入密码")

print("您刚才输入的密码为 %s "%passwd)
```

测试变量类型

```python
print(type(变量))

```



# 11.22学习笔记

### 条件判断语句

#### 查看数据类型

type(变量名)

input输入后是字符串类型



#### 强制类型转换

string转成int：直接在原有基础上加一个int类型的数字

或者：

数据类型(变量)

e.g.

```Python
a = input("input")

#此时a为string类型

int(a)

#将a转换为int类型
```

#### 运算符和表达式

##### 算数运算符

| 运算符 | 描述                                            | 实例                      |
| :----: | :---------------------------------------------- | :------------------------ |
|   +    | 加 - 两个对象相加                               | a + b 输出结果 31         |
|   -    | 减 - 得到负数或是一个数减去另一个数             | a - b 输出结果 -11        |
|   *    | 乘 - 两个数相乘或是返回一个被重复若干次的字符串 | a * b 输出结果 210        |
|   /    | 除 - x 除以 y                                   | b / a 输出结果 2.1        |
|   %    | 取模 - 返回除法的余数                           | b % a 输出结果 1          |
|   **   | 幂 - 返回x的y次幂                               | a**b 为10的21次方         |
|   //   | 取整除 - 向下取接近商的整数                     | `>>> 9//2 4 >>> -9//2 -5` |

##### 比较运算符

| 运算符 | 描述                                                         | 实例                  |
| :----- | :----------------------------------------------------------- | :-------------------- |
| ==     | 等于 - 比较对象是否相等                                      | (a == b) 返回 False。 |
| !=     | 不等于 - 比较两个对象是否不相等                              | (a != b) 返回 True。  |
| >      | 大于 - 返回x是否大于y                                        | (a > b) 返回 False。  |
| <      | 小于 - 返回x是否小于y。所有比较运算符返回1表示真，返回0表示假。这分别与特殊的变量True和False等价。注意，这些变量名的大写。 | (a < b) 返回 True。   |
| >=     | 大于等于 - 返回x是否大于等于y。                              | (a >= b) 返回 False。 |
| <=     | 小于等于 - 返回x是否小于等于y。                              | (a <= b) 返回 True。  |

##### 赋值运算符

| 运算符 | 描述                                                         | 实例                                                         |
| :----- | :----------------------------------------------------------- | :----------------------------------------------------------- |
| =      | 简单的赋值运算符                                             | c = a + b 将 a + b 的运算结果赋值为 c                        |
| +=     | 加法赋值运算符                                               | c += a 等效于 c = c + a                                      |
| -=     | 减法赋值运算符                                               | c -= a 等效于 c = c - a                                      |
| *=     | 乘法赋值运算符                                               | c *= a 等效于 c = c * a                                      |
| /=     | 除法赋值运算符                                               | c /= a 等效于 c = c / a                                      |
| %=     | 取模赋值运算符                                               | c %= a 等效于 c = c % a                                      |
| **=    | 幂赋值运算符                                                 | c **= a 等效于 c = c ** a                                    |
| //=    | 取整除赋值运算符                                             | c //= a 等效于 c = c // a                                    |
| **:=** | 海象运算符，可在表达式内部为变量赋值。**Python3.8 版本新增运算符**。 | 在这个示例中，赋值表达式可以避免调用 len() 两次:`if (n := len(a)) > 10:    print(f"List is too long ({n} elements, expected <= 10)")` |

##### 位运算符

| 运算符 | 描述                                                         | 实例                                                         |
| :----- | :----------------------------------------------------------- | :----------------------------------------------------------- |
| &      | 按位与运算符：参与运算的两个值,如果两个相应位都为1,则该位的结果为1,否则为0 | (a & b) 输出结果 12 ，二进制解释： 0000 1100                 |
| \|     | 按位或运算符：只要对应的二个二进位有一个为1时，结果位就为1。 | (a \| b) 输出结果 61 ，二进制解释： 0011 1101                |
| ^      | 按位异或运算符：当两对应的二进位相异时，结果为1              | (a ^ b) 输出结果 49 ，二进制解释： 0011 0001                 |
| ~      | 按位取反运算符：对数据的每个二进制位取反,即把1变为0,把0变为1。**~x** 类似于 **-x-1** | (~a ) 输出结果 -61 ，二进制解释： 1100 0011， 在一个有符号二进制数的补码形式。 |
| <<     | 左移动运算符：运算数的各二进位全部左移若干位，由"<<"右边的数指定移动的位数，高位丢弃，低位补0。 | a << 2 输出结果 240 ，二进制解释： 1111 0000                 |
| >>     | 右移动运算符：把">>"左边的运算数的各二进位全部右移若干位，">>"右边的数指定移动的位数 | a >> 2 输出结果 15 ，二进制解释： 0000 1111                  |

##### 逻辑运算符

Python语言支持逻辑运算符，以下假设变量 a 为 10, b为 20:

| 运算符 | 逻辑表达式 | 描述                                                         | 实例                    |
| :----- | :--------- | :----------------------------------------------------------- | :---------------------- |
| and    | x and y    | 布尔"与" - 如果 x 为 False，x and y 返回 x 的值，否则返回 y 的计算值。 | (a and b) 返回 20。     |
| or     | x or y     | 布尔"或" - 如果 x 是 True，它返回 x 的值，否则它返回 y 的计算值。 | (a or b) 返回 10。      |
| not    | not x      | 布尔"非" - 如果 x 为 True，返回 False 。如果 x 为 False，它返回 True。 | not(a and b) 返回 False |

##### 成员运算符

除了以上的一些运算符之外，Python还支持成员运算符，测试实例中包含了一系列的成员，包括字符串，列表或元组。

| 运算符 | 描述                                                    | 实例                                              |
| :----- | :------------------------------------------------------ | :------------------------------------------------ |
| in     | 如果在指定的序列中找到值返回 True，否则返回 False。     | x 在 y 序列中 , 如果 x 在 y 序列中返回 True。     |
| not in | 如果在指定的序列中没有找到值返回 True，否则返回 False。 | x 不在 y 序列中 , 如果 x 不在 y 序列中返回 True。 |

##### 身份运算符

身份运算符用于比较两个对象的存储单元

| 运算符 | 描述                                        | 实例                                                         |
| :----- | :------------------------------------------ | :----------------------------------------------------------- |
| is     | is 是判断两个标识符是不是引用自一个对象     | **x is y**, 类似 **id(x) == id(y)** , 如果引用的是同一个对象则返回 True，否则返回 False |
| is not | is not 是判断两个标识符是不是引用自不同对象 | **x is not y** ， 类似 **id(a) != id(b)**。如果引用的不是同一个对象则返回结果 True，否则返回 False。 |

**注：** [id()](https://www.runoob.com/python/python-func-id.html) 函数用于获取对象内存地址。

##### 运算符优先级

以下表格列出了从最高到最低优先级的所有运算符：

| 运算符                   | 描述                                                   |
| :----------------------- | :----------------------------------------------------- |
| **                       | 指数 (最高优先级)                                      |
| ~ + -                    | 按位翻转, 一元加号和减号 (最后两个的方法名为 +@ 和 -@) |
| * / % //                 | 乘，除，求余数和取整除                                 |
| + -                      | 加法减法                                               |
| >> <<                    | 右移，左移运算符                                       |
| &                        | 位 'AND'                                               |
| ^ \|                     | 位运算符                                               |
| <= < > >=                | 比较运算符                                             |
| == !=                    | 等于运算符                                             |
| = %= /= //= -= += *= **= | 赋值运算符                                             |
| is is not                | 身份运算符                                             |
| in not in                | 成员运算符                                             |
| not and or               | 逻辑运算符                                             |

#### 条件控制

##### if 语句

Python中if语句的一般形式如下所示：

```python
if condition_1:
	statement_block_1 
elif condition_2:
	statement_block_2
else:
	statement_block_3
    
#以下为例子
age = int(input("请输入你家狗狗的年龄: "))
print("")
if age <= 0:
    print("你是在逗我吧!")
elif age == 1:
    print("相当于 14 岁的人。")
elif age == 2:
    print("相当于 22 岁的人。")
elif age > 2:
    human = 22 + (age -2)*5
    print("对应人类年龄: ", human)
```



- 如果 "condition_1" 为 True 将执行 "statement_block_1" 块语句
- 如果 "condition_1" 为False，将判断 "condition_2"
- 如果"condition_2" 为 True 将执行 "statement_block_2" 块语句
- 如果 "condition_2" 为False，将执行"statement_block_3"块语句

Python 中用 **elif** 代替了 **else if**，所以if语句的关键字为：**if – elif – else**。

**注意：**

- 1、每个条件后面要使用冒号 **:**，表示接下来是满足条件后要执行的语句块。
- 2、使用缩进来划分语句块，相同缩进数的语句在一起组成一个语句块。
- 3、在Python中没有switch – case语句。

##### if中常用的操作运算符

| 操作符 | 描述                     |
| :----- | :----------------------- |
| `<`    | 小于                     |
| `<=`   | 小于或等于               |
| `>`    | 大于                     |
| `>=`   | 大于或等于               |
| `==`   | 等于，比较两个值是否相等 |
| `!=`   | 不等于                   |

#### random模块

Python 有一个可用于制作随机数的内建模块。

**`random`** 模块有一组如下的方法：

| 方法              | 描述                                                         |
| :---------------- | :----------------------------------------------------------- |
| seed()            | 初始化随机数生成器。                                         |
| getstate()        | 返回随机数生成器的当前内部状态。                             |
| setstate()        | 恢复随机数生成器的内部状态。                                 |
| getrandbits()     | 返回表示随机位的数字。                                       |
| randrange()       | 返回给定范围之间的随机数。                                   |
| randint()         | 返回给定范围之间的随机数。                                   |
| choice()          | 返回给定序列中的随机元素。                                   |
| choices()         | 返回一个列表，其中包含给定序列中的随机选择。                 |
| shuffle()         | 接受一个序列，并以随机顺序返回此序列。                       |
| sample()          | 返回序列的给定样本。                                         |
| random()          | 返回 0 与 1 之间的浮点数。                                   |
| uniform()         | 返回两个给定参数之间的随机浮点数。                           |
| triangular()      | 返回两个给定参数之间的随机浮点数，您还可以设置模式参数以指定其他两个参数之间的中点。 |
| betavariate()     | 基于 Beta 分布（用于统计学）返回 0 到 1 之间的随机浮点数。   |
| expovariate()     | 基于指数分布（用于统计学），返回 0 到 1 之间的随机浮点数，如果参数为负，则返回 0 到 -1 之间的随机浮点数。 |
| gammavariate()    | 基于 Gamma 分布（用于统计学）返回 0 到 1 之间的随机浮点数。  |
| gauss()           | 基于高斯分布（用于概率论）返回 0 到 1 之间的随机浮点数。     |
| lognormvariate()  | 基于对数正态分布（用于概率论）返回 0 到 1 之间的随机浮点数。 |
| normalvariate()   | 基于正态分布（用于概率论）返回 0 到 1 之间的随机浮点数。     |
| vonmisesvariate() | 基于 von Mises 分布（用于定向统计学）返回 0 到 1 之间的随机浮点数。 |
| paretovariate()   | 基于 Pareto 分布（用于概率论）返回 0 到 1 之间的随机浮点数。 |
| weibullvariate()  | 基于 Weibull 分布（用于统计学）返回 0 到 1 之间的随机浮点数。 |

#### Python包的导入

通过前面的学习我们知道，包其实本质上还是模块，因此导入模块的语法同样也适用于导入包。无论导入我们自定义的包，还是导入从他处下载的第三方包，导入方法可归结为以下 3 种：

1. `import 包名[.模块名 [as 别名]]`
2. `from 包名 import 模块名 [as 别名]`
3. `from 包名.模块名 import 成员名 [as 别名]`

用 [] 括起来的部分，是可选部分，即可以使用，也可以直接忽略。

> 注意，导入包的同时，会在包目录下生成一个含有 __init__.cpython-36.pyc 文件的 __pycache__ 文件夹。

##### 1) import 包名[.模块名 [as 别名]]

以前面创建好的 my_package 包为例，导入 module1 模块并使用该模块中成员可以使用如下代码：

```python
import my_package.module1my_package.module1.display("http://c.biancheng.net/java/")
```

运行结果为：

http://c.biancheng.net/java/

可以看到，通过此语法格式导入包中的指定模块后，在使用该模块中的成员（变量、函数、类）时，需添加“包名.模块名”为前缀。当然，如果使用 as 给包名.模块名”起一个别名的话，就使用直接使用这个别名作为前缀使用该模块中的方法了，例如：

```python
import my_package.module1 as modulemodule.display("http://c.biancheng.net/python/")
```

程序执行结果为：

http://c.biancheng.net/python/


另外，当直接导入指定包时，程序会自动执行该包所对应文件夹下的 __init__.py 文件中的代码。例如：

```python
import my_packagemy_package.module1.display("http://c.biancheng.net/linux_tutorial/")
```

直接导入包名，并不会将包中所有模块全部导入到程序中，它的作用仅仅是导入并执行包下的 __init__.py 文件，因此，运行该程序，在执行 __init__.py 文件中代码的同时，还会抛出 AttributeError 异常（访问的对象不存在）：

http://c.biancheng.net/python/
Traceback (most recent call last):
 File "C:\Users\mengma\Desktop\demo.py", line 2, in <module>
  my_package.module1.display("http://c.biancheng.net/linux_tutorial/")
AttributeError: module 'my_package' has no attribute 'module1'


我们知道，包的本质就是模块，导入模块时，当前程序中会包含一个和模块名同名且类型为 module 的变量，导入包也是如此：

```python
import my_packageprint(my_package)print(my_package.__doc__)print(type(my_package))
```

运行结果为：

http://c.biancheng.net/python/
<module 'my_package' from 'C:\\Users\\mengma\\Desktop\\my_package\\__init__.py'>

http://c.biancheng.net/
创建第一个 Python 包

<class 'module'>

##### 2) from 包名 import 模块名 [as 别名]

仍以导入 my_package 包中的 module1 模块为例，使用此语法格式的实现代码如下：

```python
from my_package import module1module1.display("http://c.biancheng.net/golang/")
```

运行结果为：

http://c.biancheng.net/python/
http://c.biancheng.net/golang/

可以看到，使用此语法格式导入包中模块后，在使用其成员时不需要带包名前缀，但需要带模块名前缀。

当然，我们也可以使用 as 为导入的指定模块定义别名，例如：

```python
from my_package import module1 as modulemodule.display("http://c.biancheng.net/golang/")
```

此程序的输出结果和上面程序完全相同。

同样，既然包也是模块，那么这种语法格式自然也支持 `from 包名 import *` 这种写法，它和 import 包名 的作用一样，都只是将该包的 __init__.py 文件导入并执行。

##### 3) from 包名.模块名 import 成员名 [as 别名]

此语法格式用于向程序中导入“包.模块”中的指定成员（变量、函数或类）。通过该方式导入的变量（函数、类），在使用时可以直接使用变量名（函数名、类名）调用，例如：

```python
from my_package.module1 import displaydisplay("http://c.biancheng.net/shell/")
```

运行结果为：

http://c.biancheng.net/python/
http://c.biancheng.net/shell/


当然，也可以使用 as 为导入的成员起一个别名，例如：

```python
from my_package.module1 import display as disdis("http://c.biancheng.net/shell/")
```

该程序的运行结果和上面相同。

另外，在使用此种语法格式加载指定包的指定模块时，可以使用 * 代替成员名，表示加载该模块下的所有成员。例如：

```python
from my_package.module1 import *display("http://c.biancheng.net/python")
```

​     

# 11.24学习笔记

## 列表（list）

Python 编程语言中有四种集合数据类型：

- *列表（List）*是一种有序和可更改的集合。允许重复的成员。
- *元组（Tuple）*是一种有序且不可更改的集合。允许重复的成员。
- *集合（Set）*是一个无序和无索引的集合。没有重复的成员。
- *词典（Dictionary）*是一个无序，可变和有索引的集合。没有重复的成员。

选择集合类型时，了解该类型的属性很有用。

为特定数据集选择正确的类型可能意味着保留含义，并且可能意味着提高效率或安全性。



### 增删改查

| **列表的添加**      | **append** | **追加，在列表的尾部加入指定的元素**                         |
| ------------------- | :--------: | ------------------------------------------------------------ |
|                     |   extend   | 将指定序列的元素依次追加到列表的尾部(合并),不会去重复内容    |
|                     |   insert   | 将指定的元素插入到对应的索引位上，注意负索引倒序插入，超过索引就会在末尾插入 |
| **列表的删除**      |    pop     | 弹出，返回并删除指定索引位上的数据，默认删除索引为-1的数据(从右向左删除) |
|                     |   remove   | 从左往右删除一个指定的元素                                   |
|                     |    del     | 删除整个列表或列表的数据，del是python内置功能，不是列表独有的 |
| **列表的查找**      |   count    | 计数，返回要计数的元素在列表当中的个数                       |
| 注:列表没有find方法 |   index    | 查找，从左往右返回查找到的第一个指定元素的索引，如果没有找到，报错 |
| **列表的排序**      |  reverse   | 顺序倒序                                                     |
|                     |    sort    | 按照ascii码表顺序进行排序                                    |



#### 列表

列表是一个有序且可更改的集合。在 Python 中，列表用方括号编写。

##### 实例

创建列表：

```
thislist = ["apple", "banana", "cherry"]
print(thislist)
```



#### 访问项目

您可以通过引用索引号来访问列表项：

##### 实例

打印列表的第二项：

```
thislist = ["apple", "banana", "cherry"]
print(thislist[1])
```

#### 负的索引

负索引表示从末尾开始，-1 表示最后一个项目，-2 表示倒数第二个项目，依此类推。

##### 实例

打印列表的最后一项：

```python
thislist = ["apple", "banana", "cherry"]
print(thislist[-1])
```

#### 索引范围

您可以通过指定范围的起点和终点来指定索引范围。

指定范围后，返回值将是包含指定项目的新列表。

##### 实例

返回第三、第四、第五项：

```python
thislist = ["apple", "banana", "cherry", "orange", "kiwi", "melon", "mango"]
print(thislist[2:5])
```

**注释：**搜索将从索引 2（包括）开始，到索引 5（不包括）结束。

请记住，第一项的索引为 0。

#### 负索引的范围

如果要从列表末尾开始搜索，请指定负索引：

##### 实例

此例将返回从索引 -4（包括）到索引 -1（排除）的项目：

```python
thislist = ["apple", "banana", "cherry", "orange", "kiwi", "melon", "mango"]
print(thislist[-4:-1])
```

#### 更改项目值

如需更改特定项目的值，请引用索引号：

##### 实例

更改第二项：

```python
thislist = ["apple", "banana", "cherry"]
thislist[1] = "mango"
print(thislist)
```

#### 遍历列表

您可以使用 for 循环遍历列表项：

##### 实例

逐个打印列表中的所有项目：

```python
thislist = ["apple", "banana", "cherry"]
for x in thislist:
  print(x)
```

#### 检查项目是否存在

如需确定列表中是否存在指定的项，请使用 in 关键字：

##### 实例

检查列表中是否存在 “apple”：

```
thislist = ["apple", "banana", "cherry"]
if "apple" in thislist:
  print("Yes, 'apple' is in the fruits list")
```

[运行实例](https://www.w3school.com.cn/tiy/t.asp?f=python_list_in)

#### 列表长度

如需确定列表中有多少项，请使用 len() 方法：

##### 实例

打印列表中的项目数：

```python
thislist = ["apple", "banana", "cherry"]
print(len(thislist))
```

#### 添加项目

如需将项目添加到列表的末尾，请使用 append() 方法：

##### 实例

使用 append() 方法追加项目：

```python
thislist = ["apple", "banana", "cherry"]
thislist.append("orange")
print(thislist)
```

要在指定的索引处添加项目，请使用 insert() 方法：

##### 实例

插入项目作为第二个位置：

```python
thislist = ["apple", "banana", "cherry"]
thislist.insert(1, "orange")
print(thislist)
```

#### 删除项目

有几种方法可以从列表中删除项目：

##### 实例

remove() 方法删除指定的项目：

```python
thislist = ["apple", "banana", "cherry"]
thislist.remove("banana")
print(thislist)
```

##### 实例

pop() 方法删除指定的索引（如果未指定索引，则删除最后一项）：

```python
thislist = ["apple", "banana", "cherry"]
thislist.pop()
print(thislist)
```

##### 实例

del 关键字删除指定的索引：

```python
thislist = ["apple", "banana", "cherry"]
del thislist[0]
print(thislist)
```

##### 实例

del 关键字也能完整地删除列表：

```python
thislist = ["apple", "banana", "cherry"]
del thislist
```

##### 实例

clear() 方法清空列表：

```python
thislist = ["apple", "banana", "cherry"]
thislist.clear()
print(thislist)
```

#### 复制列表

您只能通过键入 list2 = list1 来复制列表，因为：list2 将只是对 list1 的引用，list1 中所做的更改也将自动在 list2 中进行。

有一些方法可以进行复制，一种方法是使用内置的 List 方法 copy()。

##### 实例

使用 copy() 方法来复制列表：

```python
thislist = ["apple", "banana", "cherry"]
mylist = thislist.copy()
print(mylist)
```

制作副本的另一种方法是使用内建的方法 list()。

##### 实例

使用 list() 方法复制列表：

```python
thislist = ["apple", "banana", "cherry"]
mylist = list(thislist)
print(mylist)
```

#### 合并两个列表

在 Python 中，有几种方法可以连接或串联两个或多个列表。

最简单的方法之一是使用 + 运算符。

##### 实例

合并两个列表：

```python
list1 = ["a", "b" , "c"]
list2 = [1, 2, 3]

list3 = list1 + list2
print(list3)
```

连接两个列表的另一种方法是将 list2 中的所有项一个接一个地追加到 list1 中：

##### 实例

把 list2 追加到 list1 中：

```python
list1 = ["a", "b" , "c"]
list2 = [1, 2, 3]

for x in list2:
  list1.append(x)

print(list1)
```


或者，您可以使用 extend() 方法，其目的是将一个列表中的元素添加到另一列表中：

##### 实例

使用 extend() 方法将 list2 添加到 list1 的末尾：

```python
list1 = ["a", "b" , "c"]
list2 = [1, 2, 3]

list1.extend(list2)
print(list1)
```


#### list() 构造函数

也可以使用 list() 构造函数创建一个新列表。

##### 实例

使用 list() 构造函数创建列表：

```python
thislist = list(("apple", "banana", "cherry")) # 请注意双括号
print(thislist)
```

#### 列表方法

Python 有一组可以在列表上使用的内建方法。

| 方法                                                         | 描述                                                 |
| :----------------------------------------------------------- | :--------------------------------------------------- |
| [append()](https://www.w3school.com.cn/python/ref_list_append.asp) | 在列表的末尾添加一个元素                             |
| [clear()](https://www.w3school.com.cn/python/ref_list_clear.asp) | 删除列表中的所有元素                                 |
| [copy()](https://www.w3school.com.cn/python/ref_list_copy.asp) | 返回列表的副本                                       |
| [count()](https://www.w3school.com.cn/python/ref_list_count.asp) | 返回具有指定值的元素数量。                           |
| [extend()](https://www.w3school.com.cn/python/ref_list_extend.asp) | 将列表元素（或任何可迭代的元素）添加到当前列表的末尾 |
| [index()](https://www.w3school.com.cn/python/ref_list_index.asp) | 返回具有指定值的第一个元素的索引                     |
| [insert()](https://www.w3school.com.cn/python/ref_list_insert.asp) | 在指定位置添加元素                                   |
| [pop()](https://www.w3school.com.cn/python/ref_list_pop.asp) | 删除指定位置的元素                                   |
| [remove()](https://www.w3school.com.cn/python/ref_list_remove.asp) | 删除具有指定值的项目                                 |
| [reverse()](https://www.w3school.com.cn/python/ref_list_reverse.asp) | 颠倒列表的顺序                                       |
| [sort()](https://www.w3school.com.cn/python/ref_list_sort.asp) | 对列表进行排序                                       |



# Python3 元组

Python 的元组与列表类似，不同之处在于元组的元素不能修改。

元组使用小括号 **( )**，列表使用方括号 **[ ]**。

元组创建很简单，只需要在括号中添加元素，并使用逗号隔开即可。

![img](https://www.runoob.com/wp-content/uploads/2016/04/tup-2020-10-27-10-26-2.png)

## 实例(Python 3.0+)

\>>> tup1 = ('Google', 'Runoob', 1997, 2000)
\>>> tup2 = (1, 2, 3, 4, 5 )
\>>> tup3 = "a", "b", "c", "d"  #  不需要括号也可以
\>>> type(tup3)
<**class** 'tuple'>

创建空元组

```
tup1 = ()
```

元组中只包含一个元素时，需要在元素后面添加逗号，否则括号会被当作运算符使用：

## 实例(Python 3.0+)

\>>> tup1 = (50)
\>>> type(tup1)   # 不加逗号，类型为整型
<**class** 'int'>

\>>> tup1 = (50,)
\>>> type(tup1)   # 加上逗号，类型为元组
<**class** 'tuple'>

元组与字符串类似，下标索引从 0 开始，可以进行截取，组合等。

![img](https://www.runoob.com/wp-content/uploads/2016/04/py-tup-10-26.png)

------

## 访问元组

元组可以使用下标索引来访问元组中的值，如下实例:

## 实例(Python 3.0+)

\#!/usr/bin/python3  tup1 = ('Google', 'Runoob', 1997, 2000) tup2 = (1, 2, 3, 4, 5, 6, 7 )  print ("tup1[0]: ", tup1[0]) print ("tup2[1:5]: ", tup2[1:5])

以上实例输出结果：

```
tup1[0]:  Google
tup2[1:5]:  (2, 3, 4, 5)
```

------

## 修改元组

元组中的元素值是不允许修改的，但我们可以对元组进行连接组合，如下实例:

## 实例(Python 3.0+)

\#!/usr/bin/python3  tup1 = (12, 34.56) tup2 = ('abc', 'xyz')  # 以下修改元组元素操作是非法的。 # tup1[0] = 100  # 创建一个新的元组 tup3 = tup1 + tup2 print (tup3)

以上实例输出结果：

```
(12, 34.56, 'abc', 'xyz')
```

------

## 删除元组

元组中的元素值是不允许删除的，但我们可以使用del语句来删除整个元组，如下实例:

## 实例(Python 3.0+)

\#!/usr/bin/python3  tup = ('Google', 'Runoob', 1997, 2000)  print (tup) del tup print ("删除后的元组 tup : ") print (tup)

以上实例元组被删除后，输出变量会有异常信息，输出如下所示：

```
删除后的元组 tup : 
Traceback (most recent call last):
  File "test.py", line 8, in <module>
    print (tup)
NameError: name 'tup' is not defined
```

------

## 元组运算符

与字符串一样，元组之间可以使用 + 号和 * 号进行运算。这就意味着他们可以组合和复制，运算后会生成一个新的元组。

| Python 表达式                  | 结果                         | 描述         |
| :----------------------------- | :--------------------------- | :----------- |
| len((1, 2, 3))                 | 3                            | 计算元素个数 |
| (1, 2, 3) + (4, 5, 6)          | (1, 2, 3, 4, 5, 6)           | 连接         |
| ('Hi!',) * 4                   | ('Hi!', 'Hi!', 'Hi!', 'Hi!') | 复制         |
| 3 in (1, 2, 3)                 | True                         | 元素是否存在 |
| for x in (1, 2, 3): print (x,) | 1 2 3                        | 迭代         |

------

## 元组索引，截取

因为元组也是一个序列，所以我们可以访问元组中的指定位置的元素，也可以截取索引中的一段元素，如下所示：

元组：

```
tup = ('Google', 'Runoob', 'Taobao', 'Wiki', 'Weibo','Weixin')
```

![img](https://www.runoob.com/wp-content/uploads/2016/04/py-tup-7.png)

| Python 表达式 | 结果                                            | 描述                                             |
| :------------ | :---------------------------------------------- | :----------------------------------------------- |
| tup[1]        | 'Runoob'                                        | 读取第二个元素                                   |
| tup[-2]       | 'Weibo'                                         | 反向读取，读取倒数第二个元素                     |
| tup[1:]       | ('Runoob', 'Taobao', 'Wiki', 'Weibo', 'Weixin') | 截取元素，从第二个开始后的所有元素。             |
| tup[1:4]      | ('Runoob', 'Taobao', 'Wiki')                    | 截取元素，从第二个开始到第四个元素（索引为 3）。 |

运行实例如下：

## 实例

\>>> tup = ('Google', 'Runoob', 'Taobao', 'Wiki', 'Weibo','Weixin')
\>>> tup[1]
'Runoob'
\>>> tup[-2]
'Weibo'
\>>> tup[1:]
('Runoob', 'Taobao', 'Wiki', 'Weibo', 'Weixin')
\>>> tup[1:4]
('Runoob', 'Taobao', 'Wiki')
\>>>

------

## 元组内置函数

Python元组包含了以下内置函数

| 序号 | 方法及描述                               | 实例                                                         |
| :--- | :--------------------------------------- | :----------------------------------------------------------- |
| 1    | len(tuple) 计算元组元素个数。            | `>>> tuple1 = ('Google', 'Runoob', 'Taobao') >>> len(tuple1) 3 >>> ` |
| 2    | max(tuple) 返回元组中元素最大值。        | `>>> tuple2 = ('5', '4', '8') >>> max(tuple2) '8' >>> `      |
| 3    | min(tuple) 返回元组中元素最小值。        | `>>> tuple2 = ('5', '4', '8') >>> min(tuple2) '4' >>> `      |
| 4    | tuple(iterable) 将可迭代系列转换为元组。 | `>>> list1= ['Google', 'Taobao', 'Runoob', 'Baidu'] >>> tuple1=tuple(list1) >>> tuple1 ('Google', 'Taobao', 'Runoob', 'Baidu')` |

### 关于元组是不可变的

所谓元组的不可变指的是元组所指向的内存中的内容不可变。

\>>> tup = ('r', 'u', 'n', 'o', 'o', 'b')
\>>> tup[0] = 'g'   # 不支持修改元素
Traceback (most recent call last):
 File "<stdin>", line 1, **in** <module>
TypeError: 'tuple' object does **not** support item assignment
\>>> id(tup)   # 查看内存地址
4440687904
\>>> tup = (1,2,3)
\>>> id(tup)
4441088800   # 内存地址不一样了

从以上实例可以看出，重新赋值的元组 tup，绑定到新的对象了，不是修改了原来的对象。





# 2021.1.17学习笔记

# Python3 字典

字典是另一种可变容器模型，且可存储任意类型对象。

字典的每个键值 **key=>value** 对用冒号 **:** 分割，每个对之间用逗号(**,**)分割，整个字典包括在花括号 **{}** 中 ,格式如下所示：

```
d = {key1 : value1, key2 : value2, key3 : value3 }
```

![img](https://www.runoob.com/wp-content/uploads/2016/04/py-dict-3.png)

键必须是唯一的，但值则不必。

值可以取任何数据类型，但键必须是不可变的，如字符串，数字。

一个简单的字典实例：

```
dict = {'name': 'runoob', 'likes': 123, 'url': 'www.runoob.com'}
```

![img](https://www.runoob.com/wp-content/uploads/2016/04/py-dict-2.png)

也可如此创建字典：

```
dict1 = { 'abc': 456 }
dict2 = { 'abc': 123, 98.6: 37 }
```

------

### 访问字典里的值

把相应的键放入到方括号中，如下实例:

#### 实例

\#!/usr/bin/python3  dict = {'Name': 'Runoob', 'Age': 7, 'Class': 'First'}  print ("dict['Name']: ", dict['Name']) print ("dict['Age']: ", dict['Age'])

以上实例输出结果：

```
dict['Name']:  Runoob
dict['Age']:  7
```

如果用字典里没有的键访问数据，会输出错误如下：

#### 实例

\#!/usr/bin/python3  dict = {'Name': 'Runoob', 'Age': 7, 'Class': 'First'}  print ("dict['Alice']: ", dict['Alice'])

以上实例输出结果：

```
Traceback (most recent call last):
  File "test.py", line 5, in <module>
    print ("dict['Alice']: ", dict['Alice'])
KeyError: 'Alice'
```



使用`get`方法访问字典，如果没有找到对应的键，默认返回:None

实例

```python
print(info.get("gender"))
```
>None
没找到的时候可以设置默认值

```python
print(info.get("gender","m"))
```

> m

### 修改字典

向字典添加新内容的方法是增加新的键/值对，修改或删除已有键/值对如下实例:

#### 实例

\#!/usr/bin/python3  dict = {'Name': 'Runoob', 'Age': 7, 'Class': 'First'}  dict['Age'] = 8               # 更新 Age dict['School'] = "菜鸟教程"  # 添加信息   print ("dict['Age']: ", dict['Age']) print ("dict['School']: ", dict['School'])

以上实例输出结果：

```
dict['Age']:  8
dict['School']:  菜鸟教程
```



------

### 删除字典元素

能删单一的元素也能清空字典，清空只需一项操作。

显示删除一个字典用del命令，如下实例：

#### 实例

\#!/usr/bin/python3  dict = {'Name': 'Runoob', 'Age': 7, 'Class': 'First'}  del dict['Name'] # 删除键 'Name' dict.clear()     # 清空字典 del dict         # 删除字典  print ("dict['Age']: ", dict['Age']) print ("dict['School']: ", dict['School'])

但这会引发一个异常，因为用执行 del 操作后字典不再存在：

```
Traceback (most recent call last):
  File "test.py", line 9, in <module>
    print ("dict['Age']: ", dict['Age'])
TypeError: 'type' object is not subscriptable
```

**注：**del() 方法后面也会讨论。



### 增删改查

```python
#增
info = {"name":"吴彦祖","age = 18"}
newId = input("请输入新的学号")
info["ID"] = newID 

#删
#【del】
info = {"name":"吴彦祖","age = 18"}
print("删除前：%s"%info["name"])

del info["name"]

print("删除后：%s"%info["name"])

#删除后内容不存在，所以会报错，del是删除了制定键值对

del info
#从内存中删除了整个字典，再次访问时会报错 

#【clear】  清空
info = {"name":"吴彦祖","age = 18"}
print("清空前：%s"%info["name"])
>>{"name":"吴彦祖","age = 18"}

info.clear()

print("删除后：%s"%info["name"])
>>{}

#修改
info = {"name":"吴彦祖","age = 18"}
info["age"] = 20

#查  （遍历）
info = {"name":"吴彦祖","age = 18"}
print(info.keys()) #获取所有的键名 （列表形式）

print(info.values()) #获取所有的值 （列表形式）

print(info.items()) #获取所有的值 （列表形式）,每一个键值对是一个元组

#遍历所有的键
for key in info.keys():
    print(key)
#遍历所有的值
for value in info.values():
    print(value)
#遍历所有的键值对
for key,value in info.items():
    print("key=%s,value=%s"%(key,value))

```

> 

### 字典键的特性

字典值可以是任何的 python 对象，既可以是标准的对象，也可以是用户定义的，但键不行。

两个重要的点需要记住：



1）不允许同一个键出现两次。创建时如果同一个键被赋值两次，后一个值会被记住，如下实例：



## 实例

\#!/usr/bin/python3  dict = {'Name': 'Runoob', 'Age': 7, 'Name': '小菜鸟'}  print ("dict['Name']: ", dict['Name'])

以上实例输出结果：

```
dict['Name']:  小菜鸟
```

2）键必须不可变，所以可以用数字，字符串或元组充当，而用列表就不行，如下实例：

## 实例

\#!/usr/bin/python3  dict = {['Name']: 'Runoob', 'Age': 7}  print ("dict['Name']: ", dict['Name'])

以上实例输出结果：

```
Traceback (most recent call last):
  File "test.py", line 3, in <module>
    dict = {['Name']: 'Runoob', 'Age': 7}
TypeError: unhashable type: 'list'
```



------

## 字典内置函数&方法

Python字典包含了以下内置函数：

| 序号 | 函数及描述                                                   | 实例                                                         |
| :--- | :----------------------------------------------------------- | :----------------------------------------------------------- |
| 1    | len(dict) 计算字典元素个数，即键的总数。                     | `>>> dict = {'Name': 'Runoob', 'Age': 7, 'Class': 'First'} >>> len(dict) 3` |
| 2    | str(dict) 输出字典，以可打印的字符串表示。                   | `>>> dict = {'Name': 'Runoob', 'Age': 7, 'Class': 'First'} >>> str(dict) "{'Name': 'Runoob', 'Class': 'First', 'Age': 7}"` |
| 3    | type(variable) 返回输入的变量类型，如果变量是字典就返回字典类型。 | `>>> dict = {'Name': 'Runoob', 'Age': 7, 'Class': 'First'} >>> type(dict) <class 'dict'>` |

Python字典包含了以下内置方法：

| 序号 | 函数及描述                                                   |
| :--- | :----------------------------------------------------------- |
| 1    | [radiansdict.clear()](https://www.runoob.com/python3/python3-att-dictionary-clear.html) 删除字典内所有元素 |
| 2    | [radiansdict.copy()](https://www.runoob.com/python3/python3-att-dictionary-copy.html) 返回一个字典的浅复制 |
| 3    | [radiansdict.fromkeys()](https://www.runoob.com/python3/python3-att-dictionary-fromkeys.html) 创建一个新字典，以序列seq中元素做字典的键，val为字典所有键对应的初始值 |
| 4    | [radiansdict.get(key, default=None)](https://www.runoob.com/python3/python3-att-dictionary-get.html) 返回指定键的值，如果键不在字典中返回 default 设置的默认值 |
| 5    | [key in dict](https://www.runoob.com/python3/python3-att-dictionary-in.html) 如果键在字典dict里返回true，否则返回false |
| 6    | [radiansdict.items()](https://www.runoob.com/python3/python3-att-dictionary-items.html) 以列表返回可遍历的(键, 值) 元组数组 |
| 7    | [radiansdict.keys()](https://www.runoob.com/python3/python3-att-dictionary-keys.html) 返回一个迭代器，可以使用 list() 来转换为列表 |
| 8    | [radiansdict.setdefault(key, default=None)](https://www.runoob.com/python3/python3-att-dictionary-setdefault.html) 和get()类似, 但如果键不存在于字典中，将会添加键并将值设为default |
| 9    | [radiansdict.update(dict2)](https://www.runoob.com/python3/python3-att-dictionary-update.html) 把字典dict2的键/值对更新到dict里 |
| 10   | [radiansdict.values()](https://www.runoob.com/python3/python3-att-dictionary-values.html) 返回一个迭代器，可以使用 list() 来转换为列表 |
| 11   | [pop(key[,default\])](https://www.runoob.com/python3/python3-att-dictionary-pop.html) 删除字典给定键 key 所对应的值，返回值为被删除的值。key值必须给出。 否则，返回default值。 |
| 12   | [popitem()](https://www.runoob.com/python3/python3-att-dictionary-popitem.html) 随机返回并删除字典中的最后一对键和值。 |

------



# Python3 File(文件) 方法

### open() 方法

Python open() 方法用于打开一个文件，并返回文件对象，在对文件进行处理过程都需要使用到这个函数，如果该文件无法被打开，会抛出 OSError。

**注意：**使用 open() 方法一定要保证关闭文件对象，即调用 close() 方法。

open() 函数常用形式是接收两个参数：文件名(file)和模式(mode)。

```
open(file, mode='r')
```

完整的语法格式为：

```
open(file, mode='r', buffering=-1, encoding=None, errors=None, newline=None, closefd=True, opener=None)
```

参数说明:

- file: 必需，文件路径（相对或者绝对路径）。
- mode: 可选，文件打开模式
- buffering: 设置缓冲
- encoding: 一般使用utf8
- errors: 报错级别
- newline: 区分换行符
- closefd: 传入的file参数类型
- opener: 设置自定义开启器，开启器的返回值必须是一个打开的文件描述符。

mode 参数有：

| 模式 | 描述                                                         |
| :--- | :----------------------------------------------------------- |
| t    | 文本模式 (默认)。                                            |
| x    | 写模式，新建一个文件，如果该文件已存在则会报错。             |
| b    | 二进制模式。                                                 |
| +    | 打开一个文件进行更新(可读可写)。                             |
| U    | 通用换行模式（**Python 3 不支持**）。                        |
| r    | 以只读方式打开文件。文件的指针将会放在文件的开头。这是默认模式。 |
| rb   | 以二进制格式打开一个文件用于只读。文件指针将会放在文件的开头。这是默认模式。一般用于非文本文件如图片等。 |
| r+   | 打开一个文件用于读写。文件指针将会放在文件的开头。           |
| rb+  | 以二进制格式打开一个文件用于读写。文件指针将会放在文件的开头。一般用于非文本文件如图片等。 |
| w    | 打开一个文件只用于写入。如果该文件已存在则打开文件，并从开头开始编辑，即原有内容会被删除。如果该文件不存在，创建新文件。 |
| wb   | 以二进制格式打开一个文件只用于写入。如果该文件已存在则打开文件，并从开头开始编辑，即原有内容会被删除。如果该文件不存在，创建新文件。一般用于非文本文件如图片等。 |
| w+   | 打开一个文件用于读写。如果该文件已存在则打开文件，并从开头开始编辑，即原有内容会被删除。如果该文件不存在，创建新文件。 |
| wb+  | 以二进制格式打开一个文件用于读写。如果该文件已存在则打开文件，并从开头开始编辑，即原有内容会被删除。如果该文件不存在，创建新文件。一般用于非文本文件如图片等。 |
| a    | 打开一个文件用于追加。如果该文件已存在，文件指针将会放在文件的结尾。也就是说，新的内容将会被写入到已有内容之后。如果该文件不存在，创建新文件进行写入。 |
| ab   | 以二进制格式打开一个文件用于追加。如果该文件已存在，文件指针将会放在文件的结尾。也就是说，新的内容将会被写入到已有内容之后。如果该文件不存在，创建新文件进行写入。 |
| a+   | 打开一个文件用于读写。如果该文件已存在，文件指针将会放在文件的结尾。文件打开时会是追加模式。如果该文件不存在，创建新文件用于读写。 |
| ab+  | 以二进制格式打开一个文件用于追加。如果该文件已存在，文件指针将会放在文件的结尾。如果该文件不存在，创建新文件用于读写。 |

默认为文本模式，如果要以二进制模式打开，加上 **b** 。

### file 对象

file 对象使用 open 函数来创建，下表列出了 file 对象常用的函数：

| 序号 | 方法及描述                                                   |
| :--- | :----------------------------------------------------------- |
| 1    | [file.close()](https://www.runoob.com/python3/python3-file-close.html)关闭文件。关闭后文件不能再进行读写操作。 |
| 2    | [file.flush()](https://www.runoob.com/python3/python3-file-flush.html)刷新文件内部缓冲，直接把内部缓冲区的数据立刻写入文件, 而不是被动的等待输出缓冲区写入。 |
| 3    | [file.fileno()](https://www.runoob.com/python3/python3-file-fileno.html)返回一个整型的文件描述符(file descriptor FD 整型), 可以用在如os模块的read方法等一些底层操作上。 |
| 4    | [file.isatty()](https://www.runoob.com/python3/python3-file-isatty.html)如果文件连接到一个终端设备返回 True，否则返回 False。 |
| 5    | [file.next()](https://www.runoob.com/python3/python3-file-next.html)**Python 3 中的 File 对象不支持 next() 方法。**返回文件下一行。 |
| 6    | [file.read([size\])](https://www.runoob.com/python3/python3-file-read.html)从文件读取指定的字节数，如果未给定或为负则读取所有。 |
| 7    | [file.readline([size\])](https://www.runoob.com/python3/python3-file-readline.html)读取整行，包括 "\n" 字符。 |
| 8    | [file.readlines([sizeint\])](https://www.runoob.com/python3/python3-file-readlines.html)读取所有行并返回列表，若给定sizeint>0，返回总和大约为sizeint字节的行, 实际读取值可能比 sizeint 较大, 因为需要填充缓冲区。 |
| 9    | [file.seek(offset[, whence\])](https://www.runoob.com/python3/python3-file-seek.html)移动文件读取指针到指定位置 |
| 10   | [file.tell()](https://www.runoob.com/python3/python3-file-tell.html)返回文件当前位置。 |
| 11   | [file.truncate([size\])](https://www.runoob.com/python3/python3-file-truncate.html)从文件的首行首字符开始截断，截断文件为 size 个字符，无 size 表示从当前位置截断；截断之后后面的所有字符被删除，其中 windows 系统下的换行代表2个字符大小。 |
| 12   | [file.write(str)](https://www.runoob.com/python3/python3-file-write.html)将字符串写入文件，返回的是写入的字符长度。 |
| 13   | [file.writelines(sequence)](https://www.runoob.com/python3/python3-file-writelines.html)向文件写入一个序列字符串列表，如果需要换行则要自己加入每行的换行符。 |