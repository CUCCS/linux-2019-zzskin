# 第二章：Vimtutor学习

## 一、环境配置
- Ubuntu 18.04 Server 64bit
- 在asciinema注册一个账号，并在本地安装配置好asciinema

## 二、实验过程
### 1. 配置 asciinema
- 安装：
```bash
  sudo apt-add-repository ppa:zanchey/asciinema
  sudo apt-get update
  sudo apt-get install asciinema
```
- 注册账号：

```bash
root@ubuntu:~# asciinem auth
```

- 开始录制：

```bash
  #保存到本地
  root@ubuntu:~# asciinema rec filename

  #保存到远程服务器
  root@ubuntu:~# asciinema rec -t filename

```

- 结束录制：

```bash
root@ubuntu:~# exit
```

### 2. vimtutor学习

- Lesson 1：[https://asciinema.org/a/n6B0YLEr5aoT9rQTbteyCFqVn](https://asciinema.org/a/n6B0YLEr5aoT9rQTbteyCFqVn)
- Lesson 2：[https://asciinema.org/a/zZ3nNXWGHPkEHfrZdemWo0efK](https://asciinema.org/a/zZ3nNXWGHPkEHfrZdemWo0efK)
- Lesson 3： [https://asciinema.org/a/GgEtuw3QeMU7YwhiBPnxyOpjr](https://asciinema.org/a/GgEtuw3QeMU7YwhiBPnxyOpjr)
- Lesson 4：[ https://asciinema.org/a/nnzkCDIyMqBZwK1sjVHZ21Mji](https://asciinema.org/a/nnzkCDIyMqBZwK1sjVHZ21Mji)
- Lesson 5：[ https://asciinema.org/a/CJ4hh7S4Dl8joC0XRHAOt043K](https://asciinema.org/a/CJ4hh7S4Dl8joC0XRHAOt043K)
- Lesson 6：[ https://asciinema.org/a/Y5R5gNbIa0JxxV1A63QvbLQqC](https://asciinema.org/a/Y5R5gNbIa0JxxV1A63QvbLQqC)
- Lesson 7：[https://asciinema.org/a/5sxXAqmNObP76XH9o62mpg9f0](https://asciinema.org/a/5sxXAqmNObP76XH9o62mpg9f0)

#### lesson 1 
- `:q!` : 不保存退出
- `wq` : 保存退出
- `x` : 删除单个字符
- `i` : 在光标后进行插入
- `A` : 行尾插入

#### lesson 2
- `dw` : 删除光标开始到下一个词之间的内容
- `d$` : 删除当行光标后的所有内容
- `dd` : 删除整行
- `0` : 光标移到行首
- `u` : 取消上一次操作
- `U` : 取消一行里的所有改变
- `CTRL-R` : 重做被取消的操作

#### lesson 3
- `p` : 输出被删除的内容
- `r` : 替换光标上的字符
- `c$` : 改变从光标位置到行尾内容
- `ce` : 改变从光标到词尾内容

#### lesson 4
- `CTRL-G` : 显示光标在文件中的位置和文件状态
- `G` : 到文件尾部
- `number G` : 跳到number行
- `gg` : 跳到第一行
- `/word` : 向后找
- `?/word` : 向前找
- `%` : 匹配{}、[]、()
- `:s/old/new`，替换第一个，/g进行单行的全局替换
- `:#,#s/old/new/g`，#为行号，对选定范围内进行替换
- `:%s/old/new/g`，对整个文件进行替换
- `:%s/old/new/gc`，对整个文件替换，每次替换是询问是否替换

#### lesson 5
- `:!command` : 执行外部命令
- `:w filename` : 当前vim打开文件内容写入filename文件中
- `v motion :w filename` : 将选中行内容写入filename
- `:r filename` : 搜索filename文件，将其内容显示在光标下方
- `:r !cmd` : 将cmd的输出显示

#### lession 6
- `o` : 光标下打开一行，进入插入模式
- `O` : 光标上打开一行
- `a` : 光标后插入
- `A` : 行尾插入
- `e` : 移动到单词尾部
- `y` : copy 
- `p` : paste
- `R` : 进入替换模式
- `:set ic` : 忽略大小写
- `:set is` : 显示搜索短语的部分匹配
- `hls` : 高亮匹配短语

#### lesson 7
- `help`或按`<F1>`或`<Help>`打开帮助窗口
- `help cmd` : 查找cmd上的帮助
- `CTRL-W` : 跳转到另一个窗口
- `q` : 关闭帮助窗口
- `CTRL-D` : 查看可能的完成情况
- `<TAB>` : 完成


### 3. 自查清单


#### 你了解vim有哪几种工作模式？
- 命令模式(command-mode) ：在编辑状态下左下角可以输入命令
- 插入模式(insert-mode) i、a、o...
- 可视模式(visual-mode) v
- 正常模式(normal-mode) ：后进入的模式

#### Normal模式下，从当前行开始，一次向下移动光标10行的操作方法？

- 跳十行：`10j`

#### 如何快速移动到文件开始行和结束行？如何快速跳转到文件中的第N行？

- 开始行：`gg`
- 结束行：`G`
- 第N行：行号+G

#### Normal模式下，如何删除单个字符、单个单词、从当前光标位置一直删除到行尾、单行、当前行开始向下数N行？
- 删除单个字符：`x`
- 单个单词：`dw`
- 从当前光标位置一直删除到行尾：`d$`
- 单行：`dd`
- 当前行开始向下数N行：`dNd`
- 删除向下N行： `10dd`

#### 如何在vim中快速插入N个空行？如何在vim中快速输入80个-？
- 在vim中快速插入N个空行:  `N i 回车 esc`
- 在vim中快速输入80个-:  `80 i - esc`

#### 如何撤销最近一次编辑操作？如何重做最近一次被撤销的操作？
- 撤销：`u`
- 重做：`Ctrl + R`

#### vim中如何实现剪切粘贴单个字符？单个单词？单行？如何实现相似的复制粘贴操作呢？
- 复制 
	- 复制一行：`yy`  
	- 复制单个字符：`yl` 
	- 复制单词：`yw`

- 剪切
	- 剪切一行：`dd`  
	- 剪切单个字符：`dl` 
	- 剪切单词：`dw`

- 粘贴
	- 用`v`选中文本之后可以按`y`进行复制，如果按`d`就表示剪切，之后按`p`进行粘贴。

#### 为了编辑一段文本你能想到哪几种操作方式（按键序列）？
- `vim+`文件名，`i`插入（`o`在行尾插入），编写（剪切、复制、粘贴），`esc，:wq`保存（强制保存）

#### 查看当前正在编辑的文件名的方法？查看当前光标所在行的行号的方法？
- 查看当前正在编辑的文件名：`normal模式下 :f`
- 查看当前光标所在行的行号：`Ctrl+G`

#### 在文件中进行关键词搜索你会哪些方法？如何设置忽略大小写的情况下进行匹配搜索？如何将匹配的搜索结果进行高亮显示？如何对匹配到的关键词进行批量替换？
- 关键词搜索  : `/[words]`、`?[words]`
- 忽略大小写的情况下进行匹配搜索 : `:set ic`
- 高亮  : `:set hls is`
- 批量替换
	- `:#,#s/old/new/g` 其中，#,#是要更改的行号的范围
	- `:%s/old/new/g` 更改全文件中的所有事件。
	- `:%s/old/new/gc` 更改全文件中的所有事件,并给出替换与否的提示。 

#### 在文件中最近编辑过的位置来回快速跳转的方法？
- `Ctrl+O`（以前）
- `Ctrl+I`（以后）

#### 如何把光标定位到各种括号的匹配项？例如：找到(, [, or {对应匹配的),], or }
- `%`

#### 在不退出vim的情况下执行一个外部程序的方法？

- `:!+命令`

#### 如何使用vim的内置帮助系统来查询一个内置默认快捷键的使用方法？如何在两个不同的分屏窗口中移动光标？
- 查询一个内置默认快捷键  `:help+快捷键名称`
- 不同的分屏窗口中移动光标 `Ctrl+W` 

#### putty中vim与主机的复制粘贴
- 按住`shift`再加命令