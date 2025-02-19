---
show: step
version: 1.0
enable_checker: true
---

# 帮助手册

## 回忆上次内容

- 上次了解的是
	- 整型数字类变量
	- integer 
	- 前缀为i
	- 含义为整数

![图片描述](https://doc.shiyanlou.com/courses/uid1190679-20230806-1691331645026)

- 整数和字符串 输出结果都一样
	- 他们之间 到底有什么区别呢？？🤔

### 输出

- 两个不同类型的变量
	- i_age 
		- `整型`的 年龄变量
		- 其中i 代表 int 整数
	- s_age 
		- 字符串型的 年龄变量
		- 其中s 代表 string 字符串

![图片描述](https://doc.shiyanlou.com/courses/uid1190679-20221030-1667135622459)

- 在打印输出的时候
	- 这两个东西 看起来完全一样啊
- 具体类型不同 有作用么？

### 运算逻辑

- 首先就是 运算的逻辑
- 字符串的加法是
	- 拼接(cancatenate)在一起
- 整数的加法是
	- 按照数字的值 进行加法运算

![图片描述](https://doc.shiyanlou.com/courses/uid1190679-20221030-1667135698125)

- 为什么数字 int 类型
	- 能够按照值 进行加法运算 呢？

### 整型数字

- 这个变量是一个整型的变量
	- 定义的时候
	- 产生这个变量的时候
	- 就是为了运算

![图片描述](https://doc.shiyanlou.com/courses/uid1190679-20220522-1653185630666)

- 整型变量 和字符串变量不同
	- 字符串变量 是一个字符的串
	- 一开始就是 
		- 为了字符串查找、匹配、显示之类的目的
- 两种类型之间
	- 可以相互转化吗？

### 转化

```
i_apple = int(s_apple)
```

- 可以用int函数
	- 将字符串转化为整数

![图片描述](https://doc.shiyanlou.com/courses/uid1190679-20210905-1630849759482)

- 注意int是一个class(类)
	- 可以把字符串
		- 转化为 int 类的对象
	- 也可以把其他进制的数
		- 转化为十进制整型数字
- 什么是其他进制？

### 十二时辰

- 关于时间的时分秒
	- 其实都不是十进制的

![图片描述](https://doc.shiyanlou.com/courses/uid1190679-20230705-1688564753534)

- 中国传统十二地支
	- 可以看出这是一个循环的圆吗？

![图片描述](https://doc.shiyanlou.com/courses/uid1190679-20230705-1688565032947)

- int可以 
	- 将 十二进制 转化为 二进制 吗？

### 转化十二进制

- 两天又两个时辰
	- 总共多少个时辰？

![图片描述](https://doc.shiyanlou.com/courses/uid1190679-20230705-1688565176278)

- 总共26个时辰
	- 这如何理解呢？

### 转化

- int函数的第二个参数
	- 代表着使用的进制

![图片描述](https://doc.shiyanlou.com/courses/uid1190679-20230705-1688565176278)

- 下面这个就是
	- 将2进制的111 转化为十进制

![图片描述](https://doc.shiyanlou.com/courses/uid1190679-20230704-1688477274355)

- 一般语言比如 c、java 
	- 都把 int 当做关键字
- 但是在 python 这里 
	- int 是一个类

- 在编程语言中
  - 什么应该 当做类？
  - 什么应该 进入关键字？
- 每个语言都不一样
	- 真的很有意思

### int 类

- 这不同的分类 涉及很多东西
  - 分词 lexical analysis 如何拆成最小的词素
  - 语法 parser 这些元素应该如何组合
  - 语义分析 Syntax analysis 组合起来应该如何理解
  - 理解了之后 又该生成什么样的指令
- 类名int 被定义为变量名
	- 可能会引发问题
    - 如下图

![图片描述](https://doc.shiyanlou.com/courses/uid1190679-20210904-1630721181350)

- int、str 都是类名
	- 都要注意这些问题
- int 和 str
	- 都没有进入关键字
- 到底哪些字符串
	- 属于关键字呢？

### 关键字 keyword

- 下面是 python3.9 目前所有的关键字
	- 我们一起来捋一捋 见过的关键字

![图片描述](https://doc.shiyanlou.com/courses/uid1190679-20210904-1630721425779)

- 这里面我们见过
  - for
  - import
  - 还有这四个是一套的
	  - try
	  - except
	  - else
	  - finally
- 很多关键字的习惯来自于 c 语言
  - 还记得么？
	- 那个最早编写 hello world 所用的编程语言
  - 其实也是编 python解释器 用的语言
-  python 和 c 还是有一些区别
  - int 在 c 里面是声明整型变量的关键字
  - int 在 python 中是一个类 
	- 具体存的 是 整型数字类的 对象
	- 这个 int型的对象
		- 在电脑内存 里面长什么样子 呢？

### 二进制

- 在打印输出的时候 使用十进制
  - 这符合 我们的生活习惯
  - 因为 我们有 `十` 个手指头
- 但是计算机用的是 `二`进制
	- binary

![图片描述](https://doc.shiyanlou.com/courses/uid1190679-20210817-1629189782875)

- 在电脑存储和运算的时候 
  - 使用二进制(binary)
  - 一切东西在电脑内 都是用二进制方式存储的
  - 因为计算机里 只有高低电平(0 和 1)
  - 相当于 两个手指头
- 不管你有几个手指头
	- 同样是数 41 棵树
	- 数出来的数字是不会变的
	- 只是使用不同的表示方式而已
- 真的么？

### 二进制十进制转化

- (41)<sub>10 进制</sub> 和 (101001)<sub>2 进制</sub> 是相等的
	- 互相之间可以相互转化
- 其中的bin
	- 代表 binary 二进制

![图片描述](https://doc.shiyanlou.com/courses/uid1190679-20221030-1667136170218)

- 不论用 10 个手指头、还是 2 个手指头
  - 41 个苹果的数量本身不会变
  - 只是计数方法变了

![图片描述](https://doc.shiyanlou.com/courses/uid1190679-20221030-1667136257251)

- int(bin(i_age),2)
	- 这是什么意思呢？
- 先看括号里面 
	- bin该如何理解来着？

### 二进制(binary) 转 十进制(decimal)

- help(bin)

![图片描述](https://doc.shiyanlou.com/courses/uid1190679-20210817-1629189210344)

- bin(41)

![图片描述](https://doc.shiyanlou.com/courses/uid1190679-20221030-1667136410401)

- `'0b101001'`
	-  这是一个二进制形式的字符串
  - 其中 0 明确这是一个数字
  - b 明确这是一个二进制数字

### 进制转化

- bin(i_age)
	- 就是将整型变量i_age 转化为 二进制的字符串形态
	- 就是 `"0b101001"`

- 再查询int帮助 

![图片描述](https://doc.shiyanlou.com/courses/uid1190679-20220216-1645004631448)

- int(bin(i_age),2)
	- 把 `"0b101001"` 从二进制转化十进制

![图片描述](https://doc.shiyanlou.com/courses/uid1190679-20221030-1667136290134)

- int甚至可以
	- 把7进制数转化为10进制

![图片描述](https://doc.shiyanlou.com/courses/uid1190679-20220216-1645004683224)

- 七进制的123 转化为 十进制
	- 得到 66

### 二进制 binary字符串 转 十进制整数

- 用int函数
	- 将二进制的字符串形态
	- 转化为整型数字

```
int("0b101001", base = 2)
int("101001", base = 2)
int("101001", 2)
```

- int的意思是integer
	- 整数

![图片描述](https://doc.shiyanlou.com/courses/uid1190679-20210817-1629190293619)

- 这三条其实是等价的
  - "0b..."明确是二进制数字
  - base 是参数的名字
	- 标识着 用的是多少进制

### 总结

- 这次了解的是
	- 整型数字类变量
	- integer 
	- 前缀为i

![图片描述](https://doc.shiyanlou.com/courses/uid1190679-20230706-1688652346363)

- 整型变量 和 字符串变量 不同
	- 整型变量 是 直接存储二进制形式的
	- 可以用 int()函数 
		- 将 2进制形式的 字符串 
			- 转化为 十进制整数
- `int()`函数
	- 接受两个变量
		1. 待转化的字符串
	    2. 字符串使用的进制
- 二进制 和 十进制之间
	- 可以互相转化
		- bin(41) 
			- 把 10进制整型数字 转化为 2进制字形式符串
		- int("101001",2) 
			- 把 2进制形式字符串 转化为 10进制整型数字
- 除了 二进制、 十进制
	- 还有什么样的进制来着？
		- 怎么转化呢？🤔
- 下次再说👋🏻
