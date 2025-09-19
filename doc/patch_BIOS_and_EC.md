# 指南: 解锁BIOS并刷修改EC

由于使用的是1vyrian项目中的`Flash a custom BIOS from URL`选项实现, 所以在自定义BIOS二进制文件时就可修改启动画面;

---

## 一、制作自定义的bios文件

### 准备工作

1. windows系统(如果你使用UEFITool的linux或其他系统的版本的话, 就不是必要)

2. [UEFITool](https://github.com/LongSoft/UEFITool), 注意截止到目前不能使用带有NE(New Engine)的版本, 因为似乎还没有替换功能

   - 官方[下载地址](https://github.com/LongSoft/UEFITool/releases/0.26.0)
   - 此项目中的[备份](../assets/LongSoft-UEFITool/)
   
3. [HxD](https://mh-nexus.de/en/hxd), 或者其他适合于你的16进制编辑器, 我这里只用HxD作为演示
   
   - 官方[下载地址](https://mh-nexus.de/en/downloads.php?product=HxD20)
   - 此项目中的[备份](../assets/mh-nexus-HxD/)
   
4. 从联想官方下载地址, 下载满足ec修改的bios版本对应的exe升级程序, 联想官网隐藏了旧版的下载入口但是没有取消下载地址, 以下是各个型号对应所需的升级程序下载地址
   - **T430**: [g1uj48us.exe](https://download.lenovo.com/pccbbs/mobiles/g1uj48us.exe)
   - **T430s**: [g7uj28us.exe](https://download.lenovo.com/pccbbs/mobiles/g7uj28us.exe)
   - **T530, T530i**: [g4uj40us.exe](https://download.lenovo.com/pccbbs/mobiles/g4uj40us.exe)
   - **W530**: [g5uj38us.exe](https://download.lenovo.com/pccbbs/mobiles/g5uj38us.exe)
   - **X230**: [g2uj31us.exe](https://download.lenovo.com/pccbbs/mobiles/g2uj31us.exe)
   - **X230t**: [gcuj32us.exe](https://download.lenovo.com/pccbbs/mobiles/gcuj32us.exe)
   - 此项目中也有对应[备份](../assets/Lenovo-upgrader)
   
   > [!Warning]
   >
   > 此上下载链接来自于[hamishcoleman/thinkpad-ec/Descriptions.txt](https://github.com/hamishcoleman/thinkpad-ec/blob/master/Descriptions.txt), 可能有错误注意对照一下[版本号](../README.md)。

### 自定义流程

