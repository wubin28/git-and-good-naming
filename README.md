# 课前准备

## 1 准备git最新版v2.37.x

1.1 如果电脑操作系统是Windows 10

1.1.1 检查是否安装了git

在命令行运行“查看git版本”命令`git --version`

1.1.1.1 若没有显示版本信息

则表示没有安装git，需要参考[https://git-scm.com/downloads](https://git-scm.com/downloads)安装最新版v2.37.x。

1.1.1.2 若显示了版本信息，且版本号低于v2.37.x

则表示已经安装git，需要升级到最新版。

- 若版本高于v2.16.1，则运行“升级git”命令`git update-git-for-windows`
- 若版本在v2.14.2和v2.16.1之间，则运行“升级git”命令`git update`
- 若版本是v2.13及以下，则不具备升级git的命令，需要卸载并安装最新版本

1.1.1.3 用“查看git版本”命令git --version确认已经安装了v2.37.x版本

1.2 如果电脑操作系统是MacOS

1.2.1 检查是否安装了git

在命令行运行“查看git版本”命令`git --version`

1.2.1.1 若没有显示版本信息

则表示没有安装git，需要参考[https://git-scm.com/downloads](https://git-scm.com/downloads)安装最新版v2.37.x。

1.2.1.2 若显示了版本信息，且版本号低于v2.37.x

则表示已经安装git，需要升级到最新版。

可以参考[https://brew.sh/](https://brew.sh/)安装`Homebrew`。

用下面的步骤手工删除旧版git。

- 用`which git`找到git所在路径。
- 运行`sudo rm -rf <git所在路径>`删除git。
- 运行以下命令删除其他与旧版git相关的文件：
```
sudo rm /etc/paths.d/git
sudo rm /etc/manpaths.d/git
sudo pkgutil --forget --pkgs=GitOSX\.Installer\.git[A-Za-z0-9]*\.[a-z]*.pkg
```

使用下面命令，用Homebrew重新安装git。

```
brew uninstall git
brew update
brew install git
```

1.2.1.3 用“查看git版本”命令git --version确认已经安装了v2.37.x版本

## 2 准备 open jdk 8 或 oracle jdk 8

2.1 准备open jdk 8

若在Windows 10上安装open jdk 8，可以访问[https://jdk.java.net/java-se-ri/8-MR4](https://jdk.java.net/java-se-ri/8-MR4)下载安装。

若在MacOS上安装open jdk 8，可以运行命令`brew install openjdk@8`安装。

2.2 准备oracle jdk 8

可以访问[https://www.oracle.com/java/technologies/downloads/#java8](https://www.oracle.com/java/technologies/downloads/#java8)下载安装。


## 3 准备intellij idea community v2022.2.2

可以在Windows 10或Mac电脑上，安装JetBrains Toolbox ([https://www.jetbrains.com/toolbox-app/](https://www.jetbrains.com/toolbox-app/)) 安装IntelliJ IDEA Community Edition，安装和升级比较方便。

## 4 下载课上操练代码

在电脑上创建并进入一个操练文件夹，然后运行以下命令下载代码：

```
git clone https://github.com/wubin28/git-and-good-naming.git
```

## 5 验证代码可以运行

- 用IntelliJ IDEA打开下载代码中的`build.gradle`文件
- 打开左上角`src/main/java/org.example/Main`文件
- 鼠标右击`Main`文件，选择“运行`Main.main()`”
- 如果右下方Run窗口有“`Hello world!`”输出，则表示环境配置成功