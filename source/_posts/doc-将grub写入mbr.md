---
title: 将grub写入mbr
date: 2016-06-10 16:14:59
tags:
  - 知识文档
  - Linux
---

## 把grub重新安装到MBR上面

现在习惯了开机启动的方法，所以我们把grub重新安装到硬盘的MBR上面。

这个步骤也有两种方法，一是安装grub4dos,然后启动，选中搜索硬盘上的linux引导文件，进入Linux之后再安装grub到MBR上面;

还有就是从光盘启动去之后，再安装grub。

由于不想安装grub4dos,这里我们选择后者，从光盘或ISO启动到linux系统之后。

### 打开终端（Ctrl+ALT+T）,取得管理员权限：
``` bash
sudo su
```

### 查找linux的根目录分区：
``` bash
fdisk -l
```

### 然后挂载你的linux主分区，运行以下命令
``` bash
cd /media
mkdir sda1
```

**注意** 挂载的是你linux所在的位置 如我的是sda1
``` bash
mount /dev/sda1 /media/sda1
```

*这里补充一下，sda是你的第一块硬盘，sda1大概就是你第一块硬盘的第1个分区吧*

### 然后安装grub到第一块硬盘的MBR上面
``` bash
grub-install --root-directory=/media/sda1 /dev/sda
```

安装完之后，重启电脑就可以看到原来的菜单了。
