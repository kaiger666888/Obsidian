# Ea

## 模块描述

Configuration of the Ea (EEPROM Abstraction) module.

## 容器列表

### 1. EaBlockConfiguration

**描述**: Configuration of block specific parameters for the EEPROM abstraction module.

#### 参数列表

```yaml
- 
  序号: 1
  名称: EaBlockNumber
  长名称: ''
  描述: Block identifier (handle).
  默认值: ''
  最小值: 1
  最大值: 65534
- 
  序号: 2
  名称: EaBlockSize
  长名称: ''
  描述: Size of a logical block in bytes.
  默认值: ''
  最小值: 1
  最大值: 65535
- 
  序号: 3
  名称: EaImmediateData
  长名称: ''
  描述: Marker for high priority data.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: EaNumberOfWriteCycles
  长名称: ''
  描述: Number of write cycles required for this block.
  默认值: ''
  最小值: 0
  最大值: 4294967295
```

### 2. EaGeneral

**描述**: General configuration of the EEPROM abstraction module. This container lists block independent
configuration parameters.

#### 参数列表

```yaml
- 
  序号: 1
  名称: EaDevErrorDetect
  长名称: ''
  描述: Pre-processor switch to enable and disable development error detection.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: EaIndex
  长名称: ''
  描述: Specifies the InstanceId of this module instance. If only one instance is present it shall
      have the Id 0.
  默认值: ''
  最小值: 0
  最大值: 254
- 
  序号: 3
  名称: EaNvmJobEndNotification
  长名称: ''
  描述: Mapped to the job end notification routine provided by the upper layer module
      (NvM_JobEndNotification).
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: EaNvmJobErrorNotification
  长名称: ''
  描述: Mapped to the job error notification routine provided by the upper layer module
      (NvM_JobErrorNotification).
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: EaPollingMode
  长名称: ''
  描述: Pre-processor switch to enable and disable the polling mode for this module.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: EaSetModeSupported
  长名称: ''
  描述: Compile switch to enable / disable the function Ea_SetMode.
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: EaVersionInfoApi
  长名称: ''
  描述: Pre-processor switch to enable / disable the API to read out the modules version information.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 8
  名称: EaVirtualPageSize
  长名称: ''
  描述: The size in bytes to which logical blocks shall be aligned.
  默认值: ''
  最小值: 0
  最大值: 65535
```

### 3. EaPublishedInformation

**描述**: Additional published parameters not covered by CommonPublishedInformation container.

#### 参数列表

```yaml
- 
  序号: 1
  名称: EaBlockOverhead
  长名称: ''
  描述: Management overhead per logical block in bytes.
  默认值: ''
  最小值: 0
  最大值: 65535
- 
  序号: 2
  名称: EaMaximumBlockingTime
  长名称: ''
  描述: The maximum time the EA module's API routines shall be blocked (delayed) by internal
      operations. (EA070)
  默认值: ''
  最小值: 0
  最大值: Inf
- 
  序号: 3
  名称: EaPageOverhead
  长名称: ''
  描述: Management overhead per page in bytes.
  默认值: ''
  最小值: 0
  最大值: 65535
```

