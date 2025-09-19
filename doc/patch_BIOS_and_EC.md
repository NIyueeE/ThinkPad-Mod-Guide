# 指南: 解锁BIOS并刷修改EC

由于使用的是1vyrian项目中的`Flash a custom BIOS from URL`选项实现, 所以在自定义BIOS二进制文件时就可修改启动画面;

前面的主要流程和[patch_BIOS教程](./patch_BIOS.md)中的相同。

---

## 一、制作自定义的bios文件

1. windows系统(如果你使用UEFITool的linux或其他系统的版本的话, 就不是必要)

2. [UEFITool](https://github.com/LongSoft/UEFITool), 注意截止到目前不能使用带有NE(New Engine)的版本, 因为似乎还没有替换功能

   - 官方[下载地址](https://github.com/LongSoft/UEFITool/releases/0.26.0)
   - 此项目中的[备份](../assets/LongSoft-UEFITool/)

   
