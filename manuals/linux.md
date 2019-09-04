# some tips of linux use

## terminal
========================
### 快捷键

    + 删除单词: ctrl + w
    + 字符前后移动: ctrl + f/b
    + 词前后移动: alt + f/b
    + 清除输入: ctrl + c
    + delete: ctrl + d
    + 删除后半行: ctrl + k
    + 清屏: ctrl + l
    + 上下翻命令: Ctrl + p / n (输入一半可进行匹配)
    + 目录跳转: Alt + 方向键 

------------------------------------------------
## 系统
========================

### 开机配置

#### 开机脚本配置

1. 修改rc.local文件， 在exit(0)前添加代码

2. [自定义](https://www.jianshu.com/p/adec13ca8ed7)
    1. 创建脚本文件
    2. /bin/sh + /etc/init.d/README中写的[BEGIN INIT INFO]
    3. 赋予运行运行权限
    4. 在rc*.d中创建脚本文件的符号链接: ln /etc/script.sh /etc/rc*.d/S**script.sh


#### linux 启动项更改

+ 修改 /etc/default/grub
	+ 修改为上一次启动: `GRUB_SAVEDEFAULT=true
				GRUB_DEFAULT=saved`
