## tcping.exe - ping over a tcp connection

tcping.exe is a console application that operates similarly to 'ping', however it works over a tcp port. There are many different implementions of this floating around, written independently by different people. There are many like it, but this one is mine.


### https://elifulkerson.com/projects/tcping.php


![cpp.png][1]

## 首先安装 [Visual Studio Code](https://code.visualstudio.com/) 和 [TDM Gcc](https://jmeubank.github.io/tdm-gcc/) 
- 本站参考文章 https://262235.xyz/index.php/tag/vscode/

## 安装 C/C++ Makefile Project 插件 [参考文章]((https://262235.xyz/index.php/archives/897/))
- 文章 [VS Code 使用 C/C++ Makefile Project 插件建立项目](https://262235.xyz/index.php/archives/897/)

## 使用 C/C++ Makefile Project 插件建立 `Makefile`
- 修改三处: `CXXFLAGS`  `LDFLAGS`  `APPNAME` 参考如下
```
# Compiler settings - Can be customized.
CC = g++
CXXFLAGS = -std=c++11  -Wall -O2 -s -shared-libstdc++
# -fexec-charset=gbk -finput-charset=UTF-8  -O2 -s  -shared-libstdc++  -m64  -m32
LDFLAGS  = -lws2_32

# Makefile settings - Can be customized.
APPNAME = tcping
EXT = .cpp
SRCDIR = .
OBJDIR = .
```

## 使用 `make` 编译项目
- `D:\TDM-GCC-64\bin\mingw32-make.exe` 复制副本，改名成 `make.exe`
- VS Code 新建终端，如演示动画，输入 `make` 命令进行编译

![make.gif][2]

## tcping - ping over a tcp connection
tcping 是一个控制台应用程序，其操作类似于“ping”，但它通过 tcp 端口工作。 

- 官方: https://elifulkerson.com/projects/tcping.php
- 配置Makefile项目:  https://github.com/srgb888/tcping



  [1]: https://262235.xyz/usr/uploads/2022/01/87426035.png
  [2]: https://262235.xyz/usr/uploads/2022/01/2115598247.gif
