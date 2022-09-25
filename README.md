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

## 2 准备 open jdk 8 或 oracle jdk 8

注意，准备open jdk 8 或 oracle jdk 8，二者只要准备好一个就可以。

2.1 准备open jdk 8

若在Windows 10上安装open jdk 8，可以访问[https://jdk.java.net/java-se-ri/8-MR4](https://jdk.java.net/java-se-ri/8-MR4)下载安装。

2.2 准备oracle jdk 8

可以访问[https://www.oracle.com/java/technologies/downloads/#java8](https://www.oracle.com/java/technologies/downloads/#java8)下载安装。


## 3 准备intellij idea community v2022.2.2

可以在Windows 10或Mac电脑上，安装JetBrains Toolbox ([https://www.jetbrains.com/toolbox-app/](https://www.jetbrains.com/toolbox-app/)) 安装IntelliJ IDEA Community Edition，安装和升级比较方便。

## 4 准备Powershell 7

访问[https://github.com/PowerShell/PowerShell](https://github.com/PowerShell/PowerShell)在Windows 10上安装Powershell 7。

## 5 准备posh-git

进入Powershell 7，然后运行以下3个命令。

安装`psget`
```
(new-object Net.WebClient).DownloadString("https://raw.githubusercontent.com/psget/psget/master/GetPsGet.ps1") | iex
```

安装`posh-git`
```
Install-Module posh-git
```

确保`posh-git`每次都能在每次打开Powershell 7时运行
```
Add-PoshGitToProfile
```

## 6 下载课上操练代码

在电脑上创建并进入一个操练文件夹，然后运行以下命令下载代码：

```
git clone https://github.com/wubin28/git-and-good-naming.git
```

## 7 验证代码可以运行

- 用IntelliJ IDEA打开下载代码中的`build.gradle`文件
- 打开左上角`src/main/java/org.example/Main`文件
- 鼠标右击`Main`文件，选择“运行`Main.main()`”
- 如果右下方Run窗口有“`Hello world!`”输出，则表示环境配置成功