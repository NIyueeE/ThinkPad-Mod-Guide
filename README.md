[Read this in English](./README.en.md)

# ThinkPad-Mod-Guide

本项目整合了 [**1vyrain**](https://github.com/n4ru/1vyrain)（一个免编程器 BIOS 破解项目）和 [**thinkpad-ec**](https://github.com/hamishcoleman/thinkpad-ec)（一个 EC 修改项目），旨在提供一个更清晰的操作流程，帮助 ThinkPad 用户实现以下高级功能：

- **解锁 BIOS 高级菜单**：移除无线网卡白名单，允许使用任意品牌的无线网卡。更多功能请参阅 [1vyrain 特性列表](https://github.com/n4ru/1vyrain#bios-mod-features)。
- **自定义开机动画**：替换默认的开机 Logo。
- **修改 EC (Embedded Controller)**：适配并启用经典的七行键盘。

---

## 兼容设备列表

在开始之前，请务必确认您的设备和 BIOS 版本是否在支持范围内。

### BIOS 破解与自定义开机动画 (1vyrain)

| 设备型号 | X230 | X230t | T430 | T430s | T530 | W530 |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| **支持** | ✔️ | ✔️ | ✔️ | ✔️ | ✔️ | ✔️ |

*详细支持列表请参考 [1vyrain 官方说明](https://github.com/n4ru/1vyrain#supported-systems)。*

### EC 修改以适配经典键盘 (thinkpad-ec)

| 设备型号 | 兼容的 BIOS 版本 (EC 版本) |
| :--- | :--- |
| **T430** | BIOS 2.81 (G1ETC1WW) / EC 1.13 (G1HT35WW) |
| **T430s** | BIOS 2.75 (G7ETB5WW) / EC 1.16 (G7HT39WW) |
| **T530, T530i** | BIOS 2.76 (G4ETB6WW) / EC 1.13 (G4HT39WW) |
| **W530** | BIOS 2.75 (G5ETB5WW) / EC 1.13 (G4HT39WW) |
| **X230** | BIOS 2.75 (G2ETB5WW) / EC 1.14 (G2HT35WW) |
| **X230t** | BIOS 2.73 (GCETB3WW) / EC 1.14 (GCHT25WW) |

> [!Important]
>
> 如果您希望在解锁 BIOS 的同时修改 EC，您刷写的自定义 BIOS 版本必须与上表中列出的版本完全对应。实现这一目标的最佳方法是利用 1vyrain 项目提供的“刷写自定义二进制文件”功能，将一个符合 EC 修改条件的官方 BIOS 文件刷入您的设备。

---

## 操作指南

- **仅解锁 BIOS**：[查看教程](./doc/patch_bios.md)
- **解锁 BIOS和自定义开机动画、修改 EC 并安装经典键盘**：[查看教程](./doc/patch_bios_and_ec.md)

---

## 致谢

本项目本质上是一个流程整合与文档梳理工作，旨在为社区提供更清晰的指引。所有操作流程均已在本人持有的 ThinkPad X230 上测试通过，但不保证在其他设备上同样有效，请您在操作前仔细评估风险。

最后，衷心感谢以下开源项目的开发者，没有他们的卓越工作，这一切都无法实现：

- **[1vyrain](https://github.com/n4ru/1vyrain)** by n4ru
- **[thinkpad-ec](https://github.com/hamishcoleman/thinkpad-ec)** by hamishcoleman