# Crc

## 模块描述

Configuration of the CRC (Cyclic Redundancy Check) module.

## 容器列表

### 1. CrcGeneral

**描述**: General configuration of the CRC

#### 参数列表

```yaml
- 
  序号: 1
  名称: Crc16Mode
  长名称: 16bit-CRC Calculation Method
  描述: This switch selects one of the available CRC16 calculation methods.
  默认值: CRC_16_RUNTIME
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: Crc32Mode
  长名称: 32bit-CRC Calculation Method
  描述: This switch selects one of the available CRC32 calculation methods.
  默认值: CRC_32_RUNTIME
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: Crc8H2FMode
  长名称: 8bit-H2F CRC Calculation Method
  描述: This switch selects one of the available CRC 8-bit calculation methods with 0x2F CRC
      polynomial.
  默认值: CRC_8H2F_RUNTIME
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: Crc8Mode
  长名称: 8bit-CRC Calculation Method
  描述: This switch selects one of the available CRC 8-bit (SAE J1850) calculation methods.
  默认值: CRC_8_RUNTIME
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: CrcVersionInfoApi
  长名称: API service Crc_GetVersionInfo
  描述: This parameter enables/disables the function Crc_GetVersionInfo() to get major, minor and
      patch version information.
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: Crc32P4Mode
  长名称: 32bit-P4 CRC Calculation Method
  描述: Switch to select one of the available CRC 32-bit E2E Profile 4 calculation methods.
  默认值: CRC_32P4_RUNTIME
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: Crc64Mode
  长名称: 64-bit CRC Calculation Method
  描述: This switch selects one of the available CRC 64-bit (ECMA) calculation methods.
  默认值: CRC_64_RUNTIME
  最小值: ''
  最大值: ''
```

