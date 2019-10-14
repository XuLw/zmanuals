# Manjaro


## Install


1. 下载相应的安装包，manjaro有各种桌面的版本

2. 用rufus进行刻录，选择GPT分区模式，选用dd刻录（U盘空间被隐藏了，之后用在linux下进行格式化之后再回到windows进行格式化就可使用）

3. 安装的时候，要有一个100m的分区挂载在/boot/efi（flag： boot， efi），然后就是一个分区/、/home分区


## Configuration


1. 添加国内源： `sudo pacman-mirrors -i -c China -m rank`， 选择一个或者多个都行

2. 更新本地数据缓存 `sudo pacman -Syy`

3. 设置archlinuxcn源  [参考链接](https://www.cnblogs.com/lemos/p/7640680.html)
        修改 /etc/pacman.conf
        添加：
        [archlinuxcn]
        SigLevel = Optional TrustedOnly
        Server = https://mirrors.tuna.tsinghua.edu.cn/archlinuxcn/$arch

4. 安装archlinuxcn源 签名
        $ sudo pacman -Syy
        $ sudo pacman -S archlinuxcn-keyring

5. [Optional]更新系统 `sudo pacman -Syyu`

6. 安装搜狗输入法
        sudo pacman -S fcitx-im [全部安装]
        sudo pacman -S fcitx-configtool
        sudo pacman -S fcitx-sogoupinyin
        
        修改配置文件
        
        sudo vim(nano) ~/.xprofile
            
        添加

        export GTK_IM_MODULE=fcitx

        export QT_IM_MODULE=fcitx

        export XMODIFIERS="@im=fcitx"
        
        注销重启
        

## Bug

## pacman 

1. 搜索不确定的包 `sudo pacman -Ss name`

### 不能关机

1. 根据网上的资料，多半是NVIDIA显卡的问题，具体的操作可以
    + `sudo pacman -Syyu`更新系统
    + [屏蔽开源驱动nouveau](https://blog.csdn.net/tangcuyuha/article/details/80298500)
        
