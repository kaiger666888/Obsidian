# MemIf

## 模块描述

Memory Abstraction Interface. The interface abstracts from the number of
underlying FEE or EA modules.

#NVRAM #NVMemory #Memory #DataStorage
#AUTOSAR

## 容器列表

### 1. MemIfGeneral

**描述**: General configuration parameters of the MemIf.


#### 参数列表

```yaml
- 
  序号: 1
  名称: MemIfDevErrorDetect
  长名称: Development Error Detection
  描述: |
    This parameter switches the Development Error Detection and Notification ON or OFF.
    true:   Development error detection is enabled.
    false:  Development error detection is disabled.
    
    Note: In general, the development error detection is recommended during pre-test phase. It is
    not recommended to enable the development error detection in production code due to increased
    runtime and ROM needs.
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: MemIfNumberOfDevices
  长名称: Number of devices
  描述: |
    This value specifies the concrete number of underlying memory abstraction modules.
    
    Note: Parameter not used.
  默认值: 1
  最小值: 1
  最大值: 255
- 
  序号: 3
  名称: MemIfVersionInfoApi
  长名称: Version Info Api
  描述: This parameter enables/disables the function MemIf_GetVersionInfo() to get major, minor and
      patch version information.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: MemIfSafeBswChecks
  长名称: Safe Bsw Checks
  描述: |
    This parameter defines if safety checks are used. These checks improve robustness as e.g.
    invalid parameters are checked before function is executed. This attribute has to be enabled for
    safety projects where this component is mapped to an ASIL partition.
    
    True: safety checks shall be enabled.
    False: safety checks shall NOT be enabled.
  默认值: false
  最小值: ''
  最大值: ''
```

### 2. MemIfMemHwA

**描述**: This container includes the configuration of one underlaying Memory Hardware Abstraction module.

#### 参数列表

```yaml
- 
  序号: 1
  名称: MemIfMemHwAId
  长名称: Memory Hardware Abstraction Id
  描述: This value specifies the unique handle to address the underlaying Memory Hardware Abstraction
      module.
  默认值: 0
  最小值: 0
  最大值: 254
```

### 3. MemIfMemHwAAPI

**描述**: This container includes API names of memory hardware abstraction device.

#### 参数列表

```yaml
- 
  序号: 1
  名称: MemIfMemHwACancel
  长名称: Cancel API
  描述: This parameter defines the API service name of the FEE / EA which is used to cancel a current
      job.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: MemIfMemHwAEraseImmediateBlock
  长名称: EraseImmediate API
  描述: This parameter defines the API service name of the FEE / EA which is used to erase a block
      which is configured to hold high priority data.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: MemIfMemHwAGetJobResult
  长名称: GetJobResult API
  描述: This parameter defines the API service name of the FEE / EA which is used to get the result of
      the last requested job.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: MemIfMemHwAGetStatus
  长名称: GetStatus API
  描述: This parameter defines the API service name of the FEE / EA which is used to get the current
      status of the FEE / EA.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: MemIfMemHwAIncludeFile
  长名称: Include File
  描述: This parameter defines the include file of the FEE / EA which declares the API service names.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: MemIfMemHwAInvalidateBlock
  长名称: InvalidateBlock API
  描述: This parameter defines the API service name of the FEE / EA which is used to invalidate a
      block.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: MemIfMemHwARead
  长名称: Read API
  描述: This parameter defines the API service name of the FEE / EA which is used to read data.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 8
  名称: MemIfMemHwASetMode
  长名称: SetMode API
  描述: This parameter defines the API service name of the FEE / EA which is used to set the mode.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 9
  名称: MemIfMemHwAWrite
  长名称: Write API
  描述: This parameter defines the API service name of the FEE / EA which is used to write data.
  默认值: ''
  最小值: ''
  最大值: ''
```

