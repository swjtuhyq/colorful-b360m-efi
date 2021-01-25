# 黑苹果 OpenCore引导for 七彩虹 战斧C.B360M-HD 魔音版 V20

**硬件配置：**

- 主板： 七彩虹 战斧C.B360M-HD 魔音版 V20
- CPU： Intel I5 8400
- 内存： 32GB DDR2666 （16GX2）
- 硬盘： Samsung SSD 860 EVO 500GB
- 声卡： ALC662
- 网卡： Rtl8111/8168


**效果基本完美**

- 显卡正常（VGA、DVI、HDMI三个输出接口都正常使用，可同时使用三显示器）
- 声卡正常
- 网卡正常
- 睡眠正常
- USB接口正常（定制USB）


## 一、特别说明:

**注意：此版本EFI需要解锁CFG-LOCK使用** 

解锁CFG参考：[解锁CFG](https://www.zdynb.cn/2020/jie-suo-cfg-lock.html)

解锁CFG后不要恢复默认设置，否则又需要再次解锁


## 二、OpenCore 说明

包含如下内容：

### 1. ACPI部分
1. SSDT-AWAC.aml
2. SSDT-EC-USBX.aml
3. SSDT-PLUG.aml
4. SSDT-PMC.aml
5. SSDT-UIAC.aml USB定制

### 2. Kernel部分

1. Lilu.kext :用于注入其他驱动
2. VirtualSMC.kext :模拟SMC。
3. WhateverGreen.kext :用于修复可能存在的显示问题
4. AppleALC.kext :声卡驱动。
5. RealtekRTL8111.kext :有线网卡驱动

### 3. UEFI/Drivers

1. HfsPlus.efi :用于识别HFS+格式分区
2. OpenRuntime.efi :OpenCore核心环境

### 4. 其他Quirk

1. AllowNvramReset: true。否则无法重置nvram。
2. AllowSetDefault: true。否则无法使用Ctrl + 数字键设置默认系统。
3. BootProtect: None。
4. SecureBootModel: Disabled。
5. Vault：Optional。以上三个关闭OC安全启动功能。


