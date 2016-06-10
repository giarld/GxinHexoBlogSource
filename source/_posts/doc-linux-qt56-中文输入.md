---
title: Linux下Qt5.6 Fcitx无法输入中文输入解决办法
date: 2016-06-10 16:43:39
tags:
  - 知识文档
  - Qt
  - Linux
---

Qt5.6的解决办法和之前的版本有点不同，方法如下：
首先安装 fcitx-frontend-qt5。
然后执行：
``` bash
sudo cp /usr/lib/x86_64-linux-gnu/qt5/plugins/platforminputcontexts/libfcitxplatforminputcontextplugin.so /opt/Qt5.6.0/Tools/QtCreator/lib/Qt/plugins/platforminputcontexts/

sudo cp /usr/lib/x86_64-linux-gnu/qt5/plugins/platforminputcontexts/libfcitxplatforminputcontextplugin.so /opt/Qt5.6.0/5.6/gcc_64/plugins/platforminputcontexts/
```
OK！！！

亲测Ubuntu16.04有效，其他版本Ubuntu和其他发行版未知，如有发现可行或不可行的发行版请留言到邮箱：
[xinxinqqt@sina.com](mailto:xinxinqqt@sina.com)
