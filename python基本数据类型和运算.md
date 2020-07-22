# 1. 注释

在python中使用#注释一行。使用\``` \```或者"""  """注释多行。

`# 注释一行`

```python
​``` 
	注释多行
	注释多行
​```
"""
	注释多行
"""
```

# 2. 数据类型、变量、运算符

	### 	2.1 数据类型

​		因为计算机可以处理不同的数据，比如文本、音频等。针对不同的数据需要定义不同的数据类型。

​		python中的数据类型有：整数、浮点数、字符串、布尔类型。

		### 	2.2 变量

​		在计算机程序中，变量不仅可以是数字，还可以是任意数据类型。变量在程序中就是用一个变量名表示了，变量名必须是大小写英文、数字和\_的组合，且不能用数字开头。

``` python
a=1 #变量a是一个整数
b=2.01 #b是一个浮点数
_str=‘abc’ #_str是一个字符串
have1=False #have是一个布尔值False

1ab=2 #这种写法是错误的 变量名不能以数字开头
```

​	数据类型转换:

​		转换成整型int(a) 

​		转换成浮点型 float(a)

​		转换成字符串 str(obj)

​	获取数据类型 

​		type(object) 

​		isinstance(object,classinfo)

```python
#type 和 isinstance的区别在于 type不会考虑继承关系，而 isinstance则考虑。
#也就是说type不会认为父类和子类是同一类型，isinstance会认为是同一类型
print(type(5))		# <class 'int'>
print(type(True)) # <class 'bool'>
print(isinstance(5,int)) # True
print(isinstance(5,float)) # False
```

	### 	2.3 运算符

​		python中运算符包括算数运算符、比较运算符、逻辑运算符、位运算符、其他运算符。

​			2.3.1 算数运算符

​				加  + 、减 -、 乘 * 、除 /、整除 // 、 取余 %、 幂 **

```python
print(2+3)  # 5 print函数用于控制台打印数据 
print(3-2)  # 1
print(3*2)  # 6
print(3/2)  # 1.5
print(3//2) # 1
print(3%2)  # 1
print(3**3) # 27 3的3次方
```

​			2.3.2 比较运算符

​				大于 > 、小于 < 、等于 == 、 大于等于 >= 、小于等于 <= 、 不等于 !=。

```python
print(3>2)  # True 输出布尔值
print(3<2)  # False 
print(3==2) # False
print(3>=2) # True
print(3<=2) # False
print(3!=2) # True
```

​			2.3.3 逻辑运算符

​				与 and 、 或 or 、 非 not。逻辑运算符左右。and和or操作符左右两侧均为布尔类型。and左侧为False时不会对右侧进行判断了，左侧为True时会对右侧进行判断。

```python
print((3>2)and(2>5)) # False and操作符只有左右两侧均为True才为True，否则为False
print((3>2) or (2>5)) #True  or操作符只要一侧为True 结果就为True， 两侧均为False 结果才为False
print(not True)   #False not操作符是对布尔值取反
```

​			2.3.4 位运算

​				取反~ 、按位与 & 、 按位或 ｜ 、按位异或 ^ 、左移 << 、右移 >>。按位取反操作时 1取反为0，0取反为1。按位与操作时，两者对应的均是1，才会得到1，否则为0。按位或操作只要有一个是1就得到1，均为0，才是0。异或操作则是两者不同结果为1，相同结果为0。3<<2 表示3转位二进制数左移2位。4>>2表示4转位二进制数右移2位。

​				二进制有三种表现形式：原码、反码和补码。

​				原码：就是二进制表示。

​				反码：正数反码就是原码，负数的反码是符号位不变，其余位取反。

​				补码：正数补码就是原码，负数补码是反码加1。

​				符号位：最高位为符号位，0表示正数，1表示负数。在位运算中，符号位也参与运算。

​			2.3.5 其他运算符

​				是 is、不是 is not、存在 in、不存在 not in。

```python
#is和is not是对比两个变量的地址 == !=比较的是两个变量的值
a = 'a'
b = 'a'
print(a is b)               # 是    结果 True
print(a is not b)           # 不是   结果  False
print(5 in [2, 3, 4, 5])        # 存在于(在...中)     结果  True
print(5 not in [2, 3, 4, 5])    # 不存在(不在...中)    结果  False
```

​			2.3.6 运算符优先级

​				一元运算符高于二元运算。 先算数运算，后移位运算，最后位运算。逻辑运算最后结合。

# 3. 算法题

​	给定一个非空整数数组，除了某个元素只出现一次以外，其余每个元素均出现两次。找出那个只出现了一次的元

素。(位运算解题)

```python
def singleNumber (nums):
    res = 0
    for num in nums:
        res ^= num
    print(res)

nums = [2,4,4,1,2]
singleNumber(nums)

#结果 1
```







