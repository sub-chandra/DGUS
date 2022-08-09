# Introduction

This program is a simply demo of Ammeter.

# Variable

> Variable Type: `Usigned Long` 4字节

## Sheet

|变量名称|变量地址|
|---|---|
|电压|`0x1000`|
|电流|`0x1005`|
|功率|`0x100A`|
|电量|`0X100F`|

## 修改访问

> 以变量电压为了例，

访问：`5a a5 04 83 1000 01` 或 `0x5a 0xa5 0x04 0x83 0x10 0x00 0x01`(Arduino)

**修改：**

- 以 `4Byte`整数输入，自动获取小数，比如传入 `0000 0064`则电压显示：0.100 V
- `5a a5 07 82 1000 0000 0064 ` $\to$ `1000`是变量地址 `0000 0064`是传入数据

# Other

型号为`DMG80480C070_03WTC`的屏默认为 `232`电平， 型号`HDL6628`电平为`TTL`

