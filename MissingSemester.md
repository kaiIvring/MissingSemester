# Lecture 1  Course overview + the shell

## ls

```shell
drwxr-xr-x 1 missing  users  4096 Jun 15  2019 missing
```

对于drwxr-xr-x ：''d''表示missing是一个文件夹，接下来九个字符每三个为一组''rwx'',''r-x'',r-x'',分别代表文件所有者(missing),用户组(users),以及其他所有人具有的权限

## rewire(重定向)：

< 输入，> 输出，>> 追加

e.g echo hello > hello.txt ; cat < hello.txt ； cat < hello.txt >> hello1.txt

## pipe " | "

"管道":将左边的输出作为右边的输出
e.g ls -l / | tali -n1

## root user

sudo su 启用超级用户模式，即"root","$"将会变为"#"

## quotes(引号)

single quotes: 保留单引号中所有内容的字面值(单引号不能在双引号中出现)
double quotes: 保留部分内容的字面值("!"有特殊含义)(双引号可以在单引号内出现(用escape:" \ "))

___

# Lecture 2 Shell Tools and Scripting

## bash 变量

- `$0` - 脚本名
- `$1` 到 `$9` - 脚本的参数。 `$1` 是第一个参数，依此类推。
- `$@` - 所有参数
- `$#` - 参数个数
- `$?` - 前一个命令的返回值
- `$$` - 当前脚本的进程识别码
- `!!` - 完整的上一条命令，包括参数。常见应用：当你因为权限不足执行命令失败时，可以使用 `sudo !!` 再尝试一次。
- `$_` - 上一条命令的最后一个参数。如果你正在使用的是交互式 shell，你可以通过按下 `Esc` 之后键入 . 来获取这个值。

## 命令替换 进程替换

*$( CMD )*     *<( CMD)*

## 通配

"*" : 配对一个 "?" : 配对多个 "{}" ： 处理多个文件时使用(convert image.{png,jpg})

## shebang
#!/bin/bash #!/usr/bin/env python

类似指定解释器 
___

# Lecture 3 Editors(vim)

## prctice it!
___

# Lecture 4 Data Wrangling

## Regular Expressions

\d:Any digit
\D:Any Non-digit character
".":everything
[]:方括号中的元素之一,i.e. [abc]:only a,b or c
[^abc]:not a,b nor c
[a-z]:a to z
\w:大小写字母，数字，下划线
\W:空格，标点符号，等特殊字符
{m}:m repetitions
{m,n}:m to n repetitions
"*":0 or more repetitions
"+":1 or more repetitions
"?":optional
\s:Any white space
\S:Any Non-white space character
^...$:starts and ends
(...):capture group
(abc|def):matches abc or def

___

# Lecture 5 Command-line Environment

## Job Control

## Terminal Multiplexers(tmux)

## Dotfiles

use dotfile to configure programs

## Remote Machines

___

# Lecture 6 Version Control(Git)

"commit = snap"

## 分支：
master是git init默认的一个reference，作用是指向一个snapshot，HEAD是标识当前woring directory，
HEAD->master就表示当前HEAD指向master且在同一文件夹下。
可以用git branch来创建一个新的reference，并利用git check out在不同reference之间切换

## Advanced git
.gitignore: 可以指定忽略文件夹中的内容

## fork
fork是用来在github上复制他人的仓库，并可以随意更改，之后可以发起pull request(PR),将自己做出的修改应用到原先复制的仓库
一般是fork后使用git clone来复制到本地进行工作，不这样做，而是直接git clone原仓库没有权限git commit和push

___

# Lecture 7 Debugging and Profiling

print and log ...

time ...
___

# Lecture 8 Metaprogramming

## makefile

## semantic versioning
语义化版本控制：MAJOR.MINOR.PATCH

## Continuous integration systems

___

# Lecture 9 Security and Cryptography

## Entropy

## Hash functions

## Key derivation functions(密钥生成函数)(KDFs) 

## 对称加密 非对称加密
非对称加密：加密(pub)，解密(pri)，签名(pri)，验证(pub)

___

# Lecture 10 Potpourri(大杂烩)

## keyborad remapping
## Deamons :进程守护
## FUSE(Filesystem in Userspace)
## Backups
## APIs(Application Programming Interface)
## Common command-line flags
## Window managers
## VPNs(Virtual Private Network)
## Markdown
## Hammerspoon(MacOs)
## Booting + Live USBs
## Docker,Vagrant,VMs,Cloud,OpenStack
## Notebook programming
## GitHub

___

# Lecture 11 Q&A

## vim macro(宏):
*录制宏*
按下q后接一个字母键，表示将宏录制到哪一个寄存器中，进行操作后按下q结束录制

*回放宏*
使用"@"后接寄存器名称来回放宏，利用数字前缀来多次回放

 
# Lecture finished!(2024.11.04)

___

