# Fee

## 模块描述

Configuration of the Fee (Flash EEPROM Emulation) module.

## 容器列表

### 1. FeeBlockConfiguration

**描述**: Configuration of block specific parameters for the Flash EEPROM Emulation module.

#### 参数列表

```yaml
- 
  序号: 1
  名称: FeeBlockNumber
  长名称: ''
  描述: Block identifier (handle).
  默认值: ''
  最小值: 1
  最大值: 65534
- 
  序号: 2
  名称: FeeBlockSize
  长名称: ''
  描述: Size of a logical block in bytes.
  默认值: ''
  最小值: 1
  最大值: 65535
- 
  序号: 3
  名称: FeeImmediateData
  长名称: ''
  描述: Marker for high priority data.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: FeeNumberOfWriteCycles
  长名称: ''
  描述: Number of write cycles required for this block.
  默认值: ''
  最小值: 0
  最大值: 4294967295
```

### 2. FeeGeneral

**描述**: Container for general parameters. These parameters are not specific to a block.

#### 参数列表

```yaml
- 
  序号: 1
  名称: FeeDevErrorDetect
  长名称: ''
  描述: Pre-processor switch to enable and disable development error detection.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: FeeIndex
  长名称: ''
  描述: Specifies the InstanceId of this module instance. If only one instance is present it shall
      have the Id 0.
  默认值: ''
  最小值: 0
  最大值: 254
- 
  序号: 3
  名称: FeeNvmJobEndNotification
  长名称: ''
  描述: Mapped to the job end notification routine provided by the upper layer module
      (NvM_JobEndNotification).
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: FeeNvmJobErrorNotification
  长名称: ''
  描述: Mapped to the job error notification routine provided by the upper layer module
      (NvM_JobErrorNotification).
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: FeePollingMode
  长名称: ''
  描述: Pre-processor switch to enable and disable the polling mode for this module.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: FeeSetModeSupported
  长名称: ''
  描述: Compiler switch to enable/disable the 'SetMode' functionality of the FEE module.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: FeeVersionInfoApi
  长名称: ''
  描述: Pre-processor switch to enable / disable the API to read out the modules version information.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 8
  名称: FeeVirtualPageSize
  长名称: ''
  描述: The size in bytes to which logical blocks shall be aligned.
  默认值: ''
  最小值: 0
  最大值: 65535
```

### 3. FeePublishedInformation

**描述**: Additional published parameters not covered by CommonPublishedInformation container.

#### 参数列表

```yaml
- 
  序号: 1
  名称: FeeBlockOverhead
  长名称: ''
  描述: Management overhead per logical block in bytes.
  默认值: ''
  最小值: 0
  最大值: 65535
- 
  序号: 2
  名称: FeeMaximumBlockingTime
  长名称: ''
  描述: The maximum time the FEE module's API routines shall be blocked (delayed) by internal
      operations.
  默认值: ''
  最小值: 0
  最大值: Inf
- 
  序号: 3
  名称: FeePageOverhead
  长名称: ''
  描述: Management overhead per page in bytes.
  默认值: ''
  最小值: 0
  最大值: 65535
```

