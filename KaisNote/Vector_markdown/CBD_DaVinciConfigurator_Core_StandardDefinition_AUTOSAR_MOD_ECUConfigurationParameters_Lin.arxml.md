# Lin

## 模块描述

Configuration of the Lin (LIN driver) module.

## 容器列表

### 1. LinGeneral

**描述**: This container contains the parameters related to each LIN Driver Unit.

#### 参数列表

```yaml
- 
  序号: 1
  名称: LinDevErrorDetect
  长名称: ''
  描述: Switches the Development Error Detection and Notification ON or OFF.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: LinIndex
  长名称: ''
  描述: Specifies the InstanceId of this module instance. If only one instance is present it shall
      have the Id 0.
  默认值: ''
  最小值: 0
  最大值: 255
- 
  序号: 3
  名称: LinTimeoutDuration
  长名称: ''
  描述: Specifies the maximum number of loops for blocking function until a timeout is raised in short
      term wait loops
  默认值: ''
  最小值: 0
  最大值: 65535
- 
  序号: 4
  名称: LinVersionInfoApi
  长名称: ''
  描述: Switches the Lin_GetVersionInfo function ON or OFF.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 2. LinGlobalConfig

**描述**: This container contains the global configuration parameter of the Lin driver. This container is a
MultipleConfigurationContainer, i.e. this container and its sub-containers exit once per
configuration set.

该容器没有参数。

### 3. LinChannel

**描述**: This container contains the configuration (parameters) of the LIN Controller(s).

#### 参数列表

```yaml
- 
  序号: 1
  名称: LinChannelBaudRate
  长名称: ''
  描述: Specifies the baud rate of the LIN channel
  默认值: ''
  最小值: 1000
  最大值: 20000
- 
  序号: 2
  名称: LinChannelId
  长名称: ''
  描述: Identifies the LIN channel. Replaces LIN_CHANNEL_INDEX_NAME from the LIN SWS.
  默认值: ''
  最小值: 0
  最大值: 65535
- 
  序号: 3
  名称: LinChannelWakeupSupport
  长名称: ''
  描述: Specifies if the LIN hardware channel supports wake up functionality
  默认值: ''
  最小值: ''
  最大值: ''
```

### 4. LinDemEventParameterRefs

**描述**: Container for the references to DemEventParameter elements which shall be invoked using the API
Dem_ReportErrorStatus API in case the corresponding error occurs. The EventId is taken from the
referenced DemEventParameter's DemEventId value. The standardized errors are provided in the
container and can be extended by vendor specific error references.

该容器没有参数。

