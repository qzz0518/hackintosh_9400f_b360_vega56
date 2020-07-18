# hackintosh_9400f_b360_vega56

## 配置：

| 硬件 | 型号 | 
| --- | --- |
| 主板 | 华硕 Asus TUF B360M-PLUS-S |
| CPU | INTEL i5-9400F |
| 显卡 | 蓝宝石 Sapphire AMD VEGA56 |
| 内存 | 十铨 TeamGroup DDR4 2666 |
| 固态 | INTEL 760P 256G |
| 网卡 | BCM94360 |
| 机箱 | JONSBO RM3 |

## 版本状态：

系统版本：macOS Catalina 10.15.6

SMBIOS：iMac Pro 1.1

* 蓝牙 + Wifi + 接力（ Hand Off ） 正常
* 显卡 H264，HEVC 硬解正常
* 机箱前置 USB 3.0 接口所有设备正常
* 重启休眠正常
* 主板后置蓝绿口 USB 3.0 接口所有设备正常

## 问题

* 后置 USB-C 口，只支持 USB 3.1 Gen 1，不支持 USB 2.0 的 USB-C 设备

### 重启/关机 BIOS 被重置解决办法

如果您的主板在 10.15.4 及以上版本中，主动重启或者关机时，BIOS 被重置，提示需要点击 F1 才能跳过提示进入系统，请按照以下步骤操作：

#### 解决方法 1

1. 打开终端，进入到下载好的 `boot.efi` 目录中，如提示输入密码，请输入系统密码

```shell
sudo mount -uw /
sudo mv boot.efi /System/Library/CoreServices
```

2. 重启即可

#### 解决方法 2

1. 打开终端，直接执行如下命令，此方法不需要替换系统文件中的 `boot.efi` 

```shell
sudo nvram wake-failure=%00%00%00%00%00
```
2. 重启即可

