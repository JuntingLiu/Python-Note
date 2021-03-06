# Python编程：从入门到实践

## 第一阶段：基础部分

### 阶段掌握

**重点内容**
* 基本的编程概念、变量、表达式、运算符以及 Python 的数据类型
* 流程控制

**难点内容**
* 列表、元组以及字典的使用

**补充**
* 在熟悉书中所讲内容的前提下，延伸阅读第 4 章提到的 [PEP 8](https://www.python.org/dev/peps/pep-0008/)，了解 Python 编码规范指南。

### 知识点

**变量**

每种编程语言都有变量的概念，用来存储内容的容器；在`Python`中变量的声名不需要关键字，直接写变量名赋值就好；

> 变量明名规则：

    1、变量只能包含字母、数字和下划线。变量可以名可以字母或下划线打头，但不能以数字打头。
    2、变量名不能包含空格，但可以使用下划线来分割其中的单词。
    3、不要将`Python`关键字和函数名作变量名，即不要使用`Python`保留用于特殊用途的单词。
    4、变量名应即简短又具有描述性。
    5、慎用小写字母l和大写字母O，因为他们可能被人看成数字1和0

**字符串**

在`Python`中，用引号括起的都是字符串，引号可以是单引号、也可以是双引号。

```字符串相关使用

   name = 'ada lovelace'
   name.title()  // Ada Lovelace 单词首字母大写
   name.upper()  // ADA LOVELACE 全大写
   name.lower()  // ada lovelace 全小写

   字符串拼接使用 `+`
   非打印字符： 制表符（\t）、换行符（\n）、空格

   name.strip()  // ada lovelace  去除字符串两端空格
   name.lstrip() // 去除字符串开头空格
   name.rstrip() // 去除字符串末尾空格  
```

**列表**

列表按特定的顺序排列的元素组成，用括号（[]）来表示列表，并用逗号分隔其中的元素。直接使用`print()`输出列表，会原样返回内容。列表以键值对的格式存储数据，所以正确的访问形式根据该元素的位置或索引也就是键来访问。索引从0开始，访问第几个元素，当前位置减1就获取该位置的索引。
获取最后一位置的值，索引为-1，依次类推-2为倒数第二个...；列表的读取顺序是从左向右读取的。

列表操作
```列表相关操作
    motorcycles = ['honda', 'yamaha', 'suzuki']
    1、motorcycles[0] = 'ducati'         # 修改
    2、motorcycles.append('ducati')      # 末尾添加
    3、motorcycles.insert(0, 'ducati')   # 指定索引位置，插入值，该索引后的值右移1位
    4、del motorcycles[0]                # 指定索引删除
    5、motorcyles.pop()                  # 默认删除列表中的最后一位，并返回删除的值；也可以指定索引位置,形象比喻列表为一个栈，而删除列表末尾的元素相当与弹出栈顶元素
    6、motorcyles.remove('honda')        # 根据值，删除列表里的元素，这样后续也可以使用该删除的值；remove方法只删除列表里的一个指定的值，如果需要删除列表里其他的值，就需要使用循环来删除所有的值
```

组织列表（排序）

```
    cars = ['bmw', 'audi', 'toyota', 'subaru']
    1、cars.sort()        # 从小到大排序(这里以字母)，永久性排序，无法恢复原来的排序
    2、cars.sort(reverse = True) # 从大到小排序，永久性排序
    3、sorted(cars)  # 临时性的排序
    4、sorted(cars, severse=True) # 临时性排序，倒序的
    5、cars.severse() # 反转列表
```

**操作列表**

遍历列表

```for
    格式:

    for item in items:
        print(item)

    注意： 冒号、缩进；冒号后，循环体需要缩进，代码不再缩进，循环结束

```

数值列表

```range
    函数：
    range(start, end, step)  函数

    start   数值起始   end  数值结束    step 步长（下一个数是上一个数的 step 后位置）通过步长可以快速分奇偶

    简单的统计计算：
    digits = [1, 3, 2, 4, 6, 8, 6]

    min(digits)  # 最小值
    max(digits)  # 最大值
    sum(digits)  # 求和
```

> 乘方运算，Python 中使用 `**` 表示,2的平方 2**2 、 2的立方 2**3

列表解析

对3、4行简单的循环创建一个列表，可以通过列表解析为一行

```列表解析

    squares = []
    for value range(1, 11):
        squares.append(value)

    列表解析后：

    squares = [value**2, for value in range(1, 22) ]
```

 