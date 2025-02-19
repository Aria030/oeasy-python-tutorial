---
show: step
version: 1.0
enable_checker: true
---

# vim和shell的总结

## 回忆上次内容

- 上次看到了
	- 安德森仙话这个文本文件的 字节状态

![图片描述](https://doc.shiyanlou.com/courses/uid1190679-20230330-1680137203613)

- 每个字符都对应一个字节状态

![图片描述](https://doc.shiyanlou.com/courses/uid1190679-20220925-1664108814250)

- 关于vim也得到了很好的锻炼
	- 我们对于vim和shell要好好总结一下
		- 以后就不会 总提示得这么详细了

### 总体环境

- 总体环境是双击黑色小方块进入的shell

![图片描述](https://doc.shiyanlou.com/courses/uid1190679-20230406-1680786412931)

- 进入shell之后
	- 可以看到提示符(prompt):
		- 用户名shiyanlou
		- 当前路径~
		- 和一个$
- 这个shell状态
	- 是一切的基础

### shell

- 在shell中可以运行各种命令

![图片描述](https://doc.shiyanlou.com/courses/uid1190679-20230401-1680314537728)

- vi oeasy.py
	- 编辑oeasy.
	- 进入vi编辑器状态
- python3
	- 进入python游乐场状态
	- 出现>>>提示符(prompt)
- pwd
	- 输出当前文件夹
- cd 
	- 改变当前文件夹
- ll -l
	- 查询当前文件夹下的文件夹和文件
- git clone ...
	- 下载仓库
- ...

### shell中的python和vim

- shell中有两个命令会切换到程序状态 
	- python3
	- vim

![图片描述](https://doc.shiyanlou.com/courses/uid1190679-20230402-1680443257901)

- 进入这两个命令之后
	- 这两个命令就会接管输入和输出
- 我们先从python3开始

### 进入python3

- 我们运行python3之后
	- 从shell切换到了python3游乐场
	- 提示符prompt是>>>

![图片描述](https://doc.shiyanlou.com/courses/uid1190679-20230401-1680314963904)

- 我们可以在python3游乐场里面
	- 算1+1
	- 调用函数
- 都有什么函数来着？

### 函数总结

- ord
	- 根据字符得到序号
- chr
	- 根据序号得到字符
- bin
	- 根据数字得到二进制的字符串形态
- hex
	- 根据数字得到十六进制的字符串形态
- print
	- 进行输出
- quit
	- 退出游乐场
- ...

### 退出python3

- 我们可以使用quit()
	- 退出python3游乐场

![图片描述](https://doc.shiyanlou.com/courses/uid1190679-20230401-1680315064137)

- 从python3退出之后
	- 我们从游乐场退回到了
		- shell环境中
			- 这个shell是基础状态
- shell提示符prompt
	- 是shiyanlou:~/ $
		- 用户名
		- 当前目录
		- $
- 然后再去进入 vim编辑器 

### vim

- 键入vi oeasy.py
	- 这样就可以进入vim命令状态
		- 编辑oeasy.py 文件

![图片描述](https://doc.shiyanlou.com/courses/uid1190679-20230401-1680315282448)

- 进入vim之后是正常模式
- 正常模式能干什么事情呢？
	- <kbd>gg</kbd> 跳转到第一行第一列
	- <kbd>G</kbd> 跳转到最后一行
	- <kbd>yy</kbd> 复制当前行
	- <kbd>ygg</kbd> 从当前行复制到第一行
	- <kbd>yG</kbd> 从当前行复制到最后一行
	- <kbd>p</kbd> 在当前行后面粘贴
	- <kbd>P</kbd> 在当前行前面粘贴
	- <kbd>"*p</kbd> 从系统剪贴板粘贴到当前缓冲区
	- <kbd>u</kbd> 撤销之前的命令
	- <kbd>ctrl</kbd> + <kbd>r</kbd> 重做之前的命令
- 这些都是在正常模式(Normal Mode)下面完成的
	- 正常模式 是 基础状态
	- 可以从正常模式 切换到其他模式
- 如何进行模式切换呢？

### 模式切换

- 从正常模式按下<kbd>i</kbd>
	- 进入插入模式
		- 可以通过键盘输入到缓存(buffer)中

![图片描述](https://doc.shiyanlou.com/courses/uid1190679-20230401-1680315405214)

- 从插入模式
	- 按下<kbd>esc</kbd>
		- 退回到正常模式

### 底行命令模式

- 从正常模式下
	- 按下<kbd>:</kbd>
		- 进入底行命令模式

![图片描述](https://doc.shiyanlou.com/courses/uid1190679-20230401-1680315502246)

- 输入命令后回车
	- 回到正常模式
- 都有什么底行命令呢？

### 底行命令列表

- :w
	- write保存
- :q
	- quit退出
- :q!
	- 不保存强制退出
- :wq
	- 保存并退出

![图片描述](https://doc.shiyanlou.com/courses/uid1190679-20230401-1680315600008)

- :!python3 %
	- 使用外部命令python3运行当前文件
- :w|!python3 %
	- 保存并使用外部命令python3运行当前文件
- :%!xxd
	- 将当前文件所有行转储

### vim模式总结

- 主要就是这三种模式
	- 正常模式是基础

![图片描述](https://doc.shiyanlou.com/courses/uid1190679-20230401-1680315839628)

- :wq
	- 从vim退出后
		- 回到shell中

## 总结
- 这次我们总结了vim和shell中的一些常用操作

![图片描述](https://doc.shiyanlou.com/courses/uid1190679-20230402-1680443257901)

- 在vim中可以用
	- :%!xxd 将文件
		- 从字符形态 转成 字节形态
- 但是说到底
	- `为啥`要把字符 
		- 对应成字节呢？🤔
- 我们下次再说！👋