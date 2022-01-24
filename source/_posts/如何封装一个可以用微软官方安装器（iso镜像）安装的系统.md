# 如何封装一个可以用微软官方安装器（iso镜像）安装的系统

## 一、首先找到你想要的微软原版镜像

您可以去[MSDN我告诉你](https://msdn.itellyou.cn/)这个网站来下载微软官方的镜像文件，具体下载方法可以用迅雷、百度网盘（这玩意限速，除非你有SVIP）等的下载软件来进行下载。

## 二、把这个镜像完整安装在一台实体机/虚拟机上面

虚拟机推荐的软件有[VMware Workstation(点击下载vm16，密钥网上可以搜到)](https://download3.vmware.com/software/wkst/file/VMware-workstation-full-16.2.0-18760230.exe)剩下还有Vbox等好用的一些软件，这里就不一一列举了。下载安装完成之后，按照教程新建虚拟机，等待系统安装在虚拟机内。

## 三、安装你所需的软件以及功能并进行封装

安装软件这方面就不多说了，然后您需要一个封装工具[DISM++点此进入官方github进行下载](https://github.com/Chuyu-Team/Dism-Multi-language/releases)记得解压之后再运行主程序。

---

### 现在开始封装

点开软件，等待它加载出来界面，如图所示：

![软件界面](C:\Users\ASUS\Desktop\屏幕截图 2022-01-24 213527.png)

然后点击工具箱——系统备份

![点击教程](C:\Users\ASUS\Desktop\屏幕截图 2022-01-24 213213.png)

然后您就能看见这个界面，单击浏览，另存文件名最好为install.wim

![](C:\Users\ASUS\Desktop\屏幕截图 2022-01-24 213233.png)

等待完成后，您选择的存储路径就会出现一个install.wim的文件。

现在将您的原版镜像所有文件解压到一个空文件夹，并用DISM++的文件浏览器功能进行替换install.wim文件（可以无视权限）install.wim文件路径在你解压出来镜像文件的sources文件夹下，如图：

![](C:\Users\ASUS\Desktop\屏幕截图 2022-01-24 214302.png)

替换完成之后，使用dism++的iso生成器将镜像文件夹封装成.iso的镜像可启动文件

![](C:\Users\ASUS\Desktop\屏幕截图 2022-01-24 214522.png)

### <font face="微软雅黑">至此，教程完成，有问题可以在b站关注[一个不正经的Windows(点击跳转)](https://space.bilibili.com/543849786)私聊解决问题或者加入我的粉丝群QQ：669777423。</font>



