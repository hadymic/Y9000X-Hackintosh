# Y9000X-Hackintosh

---
## EFI信息

* 配置：i7 9750H / 32G / FHD / 凯侠RC10 + PM971a / intel ax200
* Open Core引导（0.60版本）
* 支持10.15系统，实测更新到10.15.6没有问题
* 加入屏蔽PM981a补丁

## 重要

1. 本EFI为个人使用，基于[@WangRicky](https://github.com/WangRicky/Y9000X-HACKINTOSH)的版本进行了修改

2. **`config.plist`中的三码信息已删除，需要自己生成后填入**

   [生成教程](https://blog.xjn819.com/?p=543)，位于**2.7 Config—-PlatformInfo**

3. CFG Lock未解锁，如需解锁可参考

   **修改BIOS ROM有风险，请谨慎操作**

4. 由于未更换网卡，删除了DW1820a的相关驱动（还不是因为现在DW1820a价格也开始飙高）

5. 添加了[OpenIntelWireless](https://github.com/OpenIntelWireless)的WIFI及蓝牙驱动，实测可用

   WIFI驱动[itlwm](https://github.com/OpenIntelWireless/itlwm)目前为v1.0.0-alpha版本，等更新正式版后会进行更新，WIFI使用需配合[HeliPort](https://github.com/OpenIntelWireless/HeliPort)

6. 本人身边没有苹果设备，handoff 和 airdrop 也无从谈起

7. 耳机插入后能识别但无声，原因未知，能否有大佬为我解惑

前期准备
---

* 更换硬盘：PM981a无法安装黑苹果，所以必须更换或增加硬盘。由于有PM981a存在，系统在访问PM981a硬盘文件时会导致死机重启。必须拆下或者屏蔽这块硬盘。

* 关闭`secure boot`

* 切换硬盘模式为` AHCI`


## 工作

* 显示，背光调节正常 
* 麦克风，摄像头
* wifi 蓝牙
* 触控板全手势支持
* 电源管理 USB接口正常
* type-c接口可以正常接U盘

## 不工作

* 指纹
* FN热键
* 扬声器
* 耳机


