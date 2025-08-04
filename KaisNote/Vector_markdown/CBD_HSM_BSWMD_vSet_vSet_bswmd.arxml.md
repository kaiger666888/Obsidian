# vSet

## 容器列表

### 1. vSetGeneral

**描述**: General parameters.

#### 参数列表

```yaml
- 
  序号: 1
  名称: vSetDummyStatementKind
  长名称: ''
  描述: Dummy statements used to avoid compiler warnings about e.g. unused parameters.
  默认值: None
  最小值: ''
  最大值: ''
```

### 2. vSetPlatform

**描述**: General platform and compiler specific parameters.

#### 参数列表

```yaml
- 
  序号: 1
  名称: vSetByteOrder
  长名称: ''
  描述: Byte order on memory level.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: vSetBitOrder
  长名称: ''
  描述: Bit order on register level.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: vSetCPUType
  长名称: ''
  描述: Register width of the CPU in bit.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: vSetSizeOfEnum
  长名称: ''
  描述: Size of type enum in bit.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: vSetSizeOfInt
  长名称: ''
  描述: Size of type int in bit.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: vSetSizeOfROMPointer
  长名称: ''
  描述: Size of ROM pointer in bit.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: vSetSizeOfRAMPointer
  长名称: ''
  描述: Size of RAM pointer in bit.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 3. vSetCalibration

**描述**: General calibration specific parameters.

#### 参数列表

```yaml
- 
  序号: 1
  名称: vSetPBCalibrationVirtualStartAddress
  长名称: ''
  描述: |
    Start address of the virtual memory segment for calibration of post-build loadable parameters.
    
    The memory segment is used by standard calibration tools like vCDMStudio to display and manage
    post-build loadable parameters in a physical representation. The segment is only available in
    the HEX-file and the data base of the calibration tool. It is not transferred to the ECU's
    memory. The address should not lie in the address range of the ECU. Recommended is an address
    beyond the ECU's address range because the virtual memory segment size depends on the concrete
    configuration and is calculated automatically.
  默认值: 0
  最小值: 0
  最大值: 4294967295
```

