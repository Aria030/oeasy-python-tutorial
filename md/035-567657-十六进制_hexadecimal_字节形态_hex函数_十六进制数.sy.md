---
show: step
version: 1.0
enable_checker: true
---

# 十六进制(hexadecimal)

## 回忆上次内容

- 词源由来
	- 二
		- two
		- double
		- binary
	- 十
		- ten
		- decimal
		- deca
- 计算机是用`字节`来存储的
	- 这些数字在`字节`里面`如何`存储呢？🤔

### 字节

- 首先明确字节`长`什么样子？

![图片描述](https://doc.shiyanlou.com/courses/uid1190679-20220911-1662859314078)

- 1 个 字节(byte)
  - 正好 8个 二进制位(binary digit)
	- 8-bit

![图片描述](https://doc.shiyanlou.com/courses/uid1190679-20220326-1648282566592)

- 如果我们用 十进制数 
	- 来表示 一个字节的话
	- 表示范围从0到2<sup>8</sup>-1
		- [0,255]
	- 至少需要3位数字
- 想要用 
	- 2位数字 得到字节状态
	- 有可能吗？🤔

### 一分为二

- 把8位 分成前后两段
	- 前4位
	- 后4位
- 每一段 
	- 范围是多少呢？

![图片描述](https://doc.shiyanlou.com/courses/uid1190679-20220924-1663991097055)

- 4位都是0 
	- 数值为0
- 4位都是1
	- 数值为15

![图片描述](https://doc.shiyanlou.com/courses/uid1190679-20220924-1664001766470)

- 从0到15
	- 总共16个数字
- 可以用 2个16进制数字
	- 来可以 表示一个字节吗？！😄

### 16进制

- 进入 python3 

![图片描述](https://doc.shiyanlou.com/courses/uid1190679-20230329-1680089077010)

- 键入help(hex)
	- 观察hex的帮助文件
		- 如下图所示

![图片描述](https://doc.shiyanlou.com/courses/uid1190679-20210220-1613809571245)

- hexadecimal 是什么意思？

![图片描述](https://doc.shiyanlou.com/courses/uid1190679-20210917-1631859393894)

### 动手

- ord("a")
	- 得到a的序号97
- hex(97)
	- 输出97对应的十六进制形式
- hex(ord("a"))
	- 找到a对应的数字对应的十六进制形式

![图片描述](https://doc.shiyanlou.com/courses/uid1190679-20210220-1613809987083)

- `0x61` 就是 十六进制的`61`
	- `0x` 是 
		- 十六进制数的 前缀标志
- 正如
	- `0b` 是 
		- 二进制数的 前缀标志


- 那这个0x61是怎么得到的呢？

### 16进制数

- 4位 二进制数 
	- 对应 1位 十六进制数
- 8位 二进制数 
	- 对应 2位 十六进制数
- 8 位(bit) 
	- 刚好 对应 1个字节(byte)

![图片描述](https://doc.shiyanlou.com/courses/uid1190679-20220918-1663466037148)

- 可以用 hex函数 
	- 把10进制数 转化为
		- 16进制字符串形式
- 就像我们会用 bin
	- 把10进制数 转化为
		- 2进制字符串形式

### 对应关系

![图片描述](https://doc.shiyanlou.com/courses/uid1190679-20230603-1685785439180)

- 字符 `a` 对应
	- (`97`) <sub> `10进制数` </sub> 
	- (`0b1100001`) <sub>`2进制数`</sub>
	- (`0x61`) <sub>`16进制数`</sub>

![图片描述](https://doc.shiyanlou.com/courses/uid1190679-20230603-1685785384607)

- 不过16进制数
	- 是怎么 出现16个数字的呢？

- 先回忆 为什么用10进制？

### 回忆

- 因为 我们有10根手指

![图片描述](https://doc.shiyanlou.com/courses/uid1190679-20220924-1664004546438)

- 16进制 有多少根手指 呢？

### 十六进制

- 16进制需要16根手指

![图片描述](https://doc.shiyanlou.com/courses/uid1190679-20220918-1663494822294)

- 这有点可怕啊！！！
- 我们真的需要 16根手指头 吗？
	- 印象深刻啊 ...
	- 不过 落实到 计数上...

- 真的可以有 比9大的数字 吗？
	- 超出我们 对于数字的认知了
- 具体 怎么表示?

### 比9大的数字

```
9 + 1 = 10
```

- 10在十六进制中
	- 表示为`a`

![图片描述](https://doc.shiyanlou.com/courses/uid1190679-20230313-1678712651050)

- 15在十六进制中
	- 表示为`f`
- 15再加1
	- 就进位了
	- 表示为`0x10`
		- 对应16了
		- 所以叫16进制

![图片描述](https://doc.shiyanlou.com/courses/uid1190679-20230603-1685785511553)

- 可以把`所有的`16进制数字
	- 列出来吗？

### 所有16进制数字

- 哪些字母 对应 这些超过9的数字 呢？

![图片描述](https://doc.shiyanlou.com/courses/uid1190679-20220918-1663494710478)

### 16进制

- 在ascii编码中的 小写字母`a`
	- 对应着(`97`)<sub>`10进制数`</sub> 
	- 对应着(`0b1100001`)<sub>`2进制数`</sub>
	- 对应着(`0x61`)<sub>`16进制数`</sub>

![图片描述](https://doc.shiyanlou.com/courses/uid1190679-20220924-1664005115077)

- 我们满16的时候 才进1
	- 从0到9 用的都是 原来的符号
	- 后面没有符号了
		- 用a到f
- "j" 这个字符对应 
	- (`6a`)<sub>`16进制数`</sub> 
- 这怎么理解？

### 对应关系 

- 1个16进制数(hexadecimal)
	- 有4位(bit)
- 1个字节(byte) 有 8位(bit)

![图片描述](https://doc.shiyanlou.com/courses/uid1190679-20220918-1663495749992)

- 1个字节
	- 正好对应 2位16进制数
- 三种进制了
	- 我应该如何数数呢？

###  数树

- 数树的结果 和 手指头的数量 没有关系
	- 2根 手指头
		- (0b1011)<sub>10</sub>
	- 10根 手指头
		- (11)<sub>10</sub>
	- 16根 手指
		- (0xb)<sub>16</sub>
		- 都不会影响 数出来的 树量

![图片描述](https://doc.shiyanlou.com/courses/uid1190679-20220918-1663495550786)

- 树还是那么多树
	- 只是 表示的形式 不同

## 总结

- 这次找到了
	- 字符 和 字节状态 之间的
		- 映射 对应关系
	- 字符 对应着 字节
	- 字节 也对应着 字符
- 这种字节状态 是用 
	- 2位16进制数 来表示的
- ord可以得到字符对应的序号
- bin(n)可以把数字转化为 
	- `2进制`字符串形式
		- 对应单词 binary
- hex(n)可以把数字转化为
	- `16进制`字符串形式
- 根据ascii中的 字符序号
	- 能够 把字符存储进 计算机的字节 了

![图片描述](https://doc.shiyanlou.com/courses/uid1190679-20220925-1664108814250)

- 这十进制、二进制、十六进制
	- 转来转去的有什么意义吗？
- 可以
	- 可以看得见摸得着吗？
- 我们下次再说！👋