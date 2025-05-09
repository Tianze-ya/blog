---
title: Vim教程
date: 2024-08-08
categories: 软件
tags:
  - linux
---
# 简介
`Vim 是一款强大的文本编辑器`
如果你问程序员哪个代码编辑器好用，那么你会得到无数种答案
像：Dev-CPP、Visual Studio、VS Code、IDEA、Pycharm...
***但万中之神一定是Vim！！！***
学习Vim的一个重要理念就是，所有操作使用键盘，不使用鼠标
 
# 使用
## 简介
Vim一共有四种模式：
* 普通模式，当使用Vim打开文件时 默认进入普通模式
* 插入模式，在普通模式下按下`i`键进入插入模式
* 可视模式，选中文本时
* 命令模式，在普通模式下按下`:`键进入命令模式

在普通模式下可以操作文件 如：浏览，复制，粘粘、剪切、删除，查找等
在插入模式下，就像普通文本编辑器一样 按什么输入什么
在命令模式下，可以键入各种命令，如保存，退出等
在插入模式和命令模式下，按下`ESC`键返回普通模式
## 普通模式
- 光标移动
	最简单的方式就是用方向键 **但Vim并不推荐你去这样做，而是使用`hjkl`**
	`h 左`、`j 下`、`k 上`、`l 右`
	在移动光标前，输入数字，会像指定方向移动指定距离 如：`8k`就是向上移动8行
	
- 单词跳转
	按下`w`（word）键跳到下一个单词的开头 按下`b`（backword）键跳到上一个单词的开头
	
- 开头于结尾
	`gg`回到文件的开头，大写的`G`（Shift+g）到文件的末尾
	
- 翻页
	`Ctrl+U`对应 PageUP，`Ctrl+D`对应 PageDown
	
- 查找
	`f`+`latter` 跳转到下一个对应的字母 如：`fr` 跳转到下个字母r
	
- 复制与粘粘
	`yaw`来复制整个单词（Yank all word）
	同时`y`键后还可以接方向移动键，如`y4j`就是复制下四行，包括当前行（共五行）
	甚至还可以搭配find 如：`yfe`复制到下一个e
	使用`p`键来粘粘
	
- 删除 
	`d`删除，可以像`y`一样和其他命令搭配使用
	
- 撤销
	`u`撤销上一次的操作
## 插入模式
在普通模式下，可以通过以下方式进入插入模式
- 按下`i`键在当前位置进入，按下`a`键在下一个字母进入
- 按下`I`在当前行的开头进入，按下`A`在当前行的末尾进入
- `c`对应change，按下`caw`（change all word）会删除当前单词并进入（跟`y`一样可以和其他命令搭配）
- `cc`删除当前行并进入
- `o`转到下一行并进入
- `O`在上方插入一行并进入

## 命令模式
按下`:`打开命令模式，这里只介绍两种最简单的
- `w`保存文件，`w!`强制保存
- `q`退出，`q!`强制退出
- `wq`保存并退出

## 可视模式
按下`v`键进入可视模式，移动光标选中文本，可以搭配普通模式的命令、
按下`V`键可进入行选中模式