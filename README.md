# Y9000X-Hackintosh

## 更新日志

### 2020-08-29

1. 更新`VoodooI2C`及`VoodooI2CHID`驱动至`2.4.4`
2. 根据[Issue](https://github.com/Hadymic/Y9000X-Hackintosh/issues/3)修复开机分辨率的问题（感谢[@zomgit](https://github.com/zomgit)）

### 2020-08-26

1. [itlwm](https://github.com/OpenIntelWireless/itlwm)已更新至`v1.0.0_stable`正式版，注意[HeliPort](https://github.com/OpenIntelWireless/HeliPort)也需同步更新
2. 睡眠唤醒黑屏问题，根据[Issue](https://github.com/WangRicky/Y9000X-HACKINTOSH/issues/19)，删除了补丁`PciRoot(0x0)/Pci(0x2,0x0)`，已修复

## EFI信息

* 配置：i7 9750H / 32G / FHD / 凯侠RC10 + PM981a / Intel ax200
* Open Core引导（0.60版本）
* 支持10.15系统，实测更新到10.15.6没有问题
* 加入屏蔽PM981a补丁

## 重要说明

1. 本EFI为个人使用，基于[@WangRicky](https://github.com/WangRicky/Y9000X-HACKINTOSH)的版本进行了修改（感谢[@WangRicky](https://github.com/WangRicky)提供几乎可以完美使用的EFI），其他配置需自行测试

2. **`config.plist`中的三码信息已删除，需要自己生成后填入**

   [生成教程](https://blog.xjn819.com/?p=543)，位于**2.7 Config—-PlatformInfo**

3. CFG Lock未解锁，如需解锁可参考[此教程进行操作](http://bbs.pcbeta.com/viewthread-1845189-1-1.html)

   **修改BIOS ROM有风险，请谨慎操作**

4. 由于未更换网卡，删除了DW1820a的相关驱动（还不是因为现在DW1820a价格也开始飙高）

5. 添加了[OpenIntelWireless](https://github.com/OpenIntelWireless)的WIFI及蓝牙驱动，实测可用

   ~~WIFI驱动[itlwm](https://github.com/OpenIntelWireless/itlwm)目前为`v1.0.0-alpha`版本，等更新正式版后会进行更新~~，WIFI使用需配合[HeliPort](https://github.com/OpenIntelWireless/HeliPort)

6. 本人身边没有苹果设备，handoff 和 airdrop 也无从谈起

7. ~~可睡眠，但唤醒黑屏，重启后正常~~

前期准备
---

* 更换硬盘：PM981a无法安装黑苹果，所以必须更换或增加硬盘。由于有PM981a存在，系统在访问PM981a硬盘文件时会导致死机重启。必须拆下或者屏蔽这块硬盘。
* 关闭`secure boot`
* 切换硬盘模式为` AHCI`
* 关闭`VT`，否则耳机无声


## 工作

* 显示，背光调节正常 
* 耳机，麦克风，摄像头
* WIFI 蓝牙
* 触控板全手势支持
* 电源管理 USB接口正常
* Type-c接口可以正常接U盘

## 不工作

* 指纹
* FN热键
* 扬声器

## 参考链接

* https://github.com/WangRicky/Y9000X-HACKINTOSH
* https://github.com/hsd815/Y9000X-4K-hackintosh
* http://bbs.pcbeta.com/viewthread-1848662-1-1.html
* http://bbs.pcbeta.com/viewthread-1838959-1-1.html
* https://github.com/Corazon0513/VoodooI2CTAS2770

## 致谢

感谢各位大佬的辛勤付出，能让本小白一次点亮

在此期待各位大佬能在外放上有所突破 [TAS2770](https://github.com/Corazon0513/VoodooI2CTAS2770)
