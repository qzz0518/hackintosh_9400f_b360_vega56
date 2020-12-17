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

系统版本：macOS Big Sur 11.1

SMBIOS：iMac Pro 1.1

## 说明

配置参考于

@Leichunh [远景链接](http://bbs.pcbeta.com/forum.php?mod=viewthread&tid=1876085)

如果你是 10.15.* 直升 11.1 可能会遇到进入安装页面无限重启的情况，请使用 u 盘制作 11.1 的启动盘并使用启动盘升级你的系统。

## 请自行 config 添加三码

```
<dict>
	<key>AdviseWindows</key>
	<false/>
	<key>MLB</key>
	<string>请修改我</string>
	<key>ProcessorType</key>
	<integer>0</integer>
	<key>SystemMemoryStatus</key>
	<string>Auto</string>
	<key>ROM</key>
	<data></data>
	<key>SpoofVendor</key>
	<true/>
	<key>SystemProductName</key>
	<string>iMacPro1,1</string>
	<key>SystemSerialNumber</key>
	<string>请修改我</string>
	<key>SystemUUID</key>
	<string>请修改我</string>
</dict>
```