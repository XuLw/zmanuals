# Tips of Using Vim

--------------------------------------------------------------
## 资源
1. vim 教程: https://vimjc.com/about.html



--------------------------------------------------------------
## 安装

### [vimrc](https://github.com/amix/vimrc)

+ ubuntu下会遇到vim版本太低问题,具体参考E1解决

### [配置](https://www.zhihu.com/question/47691414/answer/373700711)



--------------------------------------------------------------
## 使用

### [快捷键](https://www.cnblogs.com/markleaf/p/7808817.html)

#### 移动
    + hjkl 上下左右
    + wb 前后单词移动
    + 相对位置跳转: 行号 + jk
    + 跳至文首: gg
    + 跳至文尾: G
    + 跳至行首: 0
    + 跳至行尾: $
    + 跳至词尾: e

    + 页面移动
        + 移动页面: C-e
        + 翻页: C-f|u|b|d
    + 匹配括号移动
        + 将光标移动到括号"( | [ | {"上
        + 按 % 进行移动

#### 插入
    + 行末插入: A
    + a: 当前位置下一个 位置插入
    + I: 行首插l入
    + i: 当前位置插入
    + O: 往上插入一行
    + o: 往下插入一行
    + D: 删除至行末
    + cc | S: 删除当前行
    + .: 重复上一个操作 (n. 代表重复几次)
    + r: 字符替换

#### 后悔药
    + 撤销: u
    + 反撤销 C-r

#### 查找
    + 大小写敏感: /\c[pattarn]
    + 替换: %s/old/new/g
    + 替换时确认: %s/old/new/gc

#### 代码
    + 缩进格式化: gg=G
    + 自动补全: C-n C-p

#### 多文件
    + tabedit file: 新标签页中打开file
    + [n]gt[T]: 进行切换
    + vsp file: 垂直打开文件
    + vp file: 水平打开多文件
    
    + 关闭文件
        + 只显示当前窗口: :only
        + 所有文件wq操作: wqall

#### 块操作
    + 进入块操作: C-v
    + 移动进行块选择
    + 进入插入模式: I
    + 进行操作
    + 对选中块进行操作。

    + 对块进行拼接: J
    + 对块进行缩进: < >
    + 自动缩进: =


### 折叠
    + 折叠方法：set foldmethod=syntax | manual | indet | expr | syntax | diff | marker
    + 快捷键：
        + zR：打开所有折叠
        + zM：关闭所有折叠


### 其他



#### 鼠标 

1. `set mouse=a`

#### 窗口

1. `C-j`



### 特殊用法

+ 强制保存
   `w !sudo tee %`



--------------------------------------
## ERRORs

1. 升级版本:
    `sudo add-apt-repository ppa:jonathonf/vim`
    `sudo apt update`
    `sudo apt install vim`
