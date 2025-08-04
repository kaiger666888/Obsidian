# Icu

## 模块描述

Configuration of the Icu (Input Capture Unit) module.

## 容器列表

### 1. IcuConfigSet

**描述**: This container is the base for a multiple configuration set

#### 参数列表

```yaml
- 
  序号: 1
  名称: IcuMaxChannel
  长名称: ''
  描述: This parameter contains the number of Channels configured. It will be gathered by tools during
      the configuration stage.
  默认值: ''
  最小值: 0
  最大值: 65535
```

### 2. IcuChannel

**描述**: Configuration of an individual ICU channel.

#### 参数列表

```yaml
- 
  序号: 1
  名称: IcuChannelId
  长名称: ''
  描述: Channel Id of the ICU channel. This value will be assigned to the symbolic name derived of the
      IcuChannel container short name.
  默认值: ''
  最小值: 0
  最大值: 65535
- 
  序号: 2
  名称: IcuDefaultStartEdge
  长名称: ''
  描述: Configures the default-activation-edge which shall be used for this channel if there was no
      activation-edge configured by the call of service Icu_SetActivationCondition().
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: IcuMeasurementMode
  长名称: ''
  描述: Configures the measurement mode of this channel.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: IcuWakeupCapability
  长名称: ''
  描述: Information about the wakeup-capability of this channel.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 3. IcuSignalEdgeDetection

**描述**: This container contains the configuration (parameters) in case the measurement mode is
"IcuSignalEdgeDetection"

#### 参数列表

```yaml
- 
  序号: 1
  名称: IcuSignalNotification
  长名称: ''
  描述: Notification function for signal notification.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 4. IcuSignalMeasurement

**描述**: This container contains the configuration (parameters) in case the measurement mode is
"IcuSignalMeasurement"

#### 参数列表

```yaml
- 
  序号: 1
  名称: IcuSignalMeasurementProperty
  长名称: ''
  描述: Configures the property that could be measured in case the mode is "IcuSignalMeasurement".
  默认值: ''
  最小值: ''
  最大值: ''
```

### 5. IcuTimestampMeasurement

**描述**: This container contains the configuration (parameters) in case the measurement mode is
"IcuTimestamp"

#### 参数列表

```yaml
- 
  序号: 1
  名称: IcuTimestampMeasurementProperty
  长名称: ''
  描述: Configures the handling of the buffer in case the mode is "Timestamp"
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: IcuTimestampNotification
  长名称: ''
  描述: Notification function if the number of requested timestamps
  默认值: ''
  最小值: ''
  最大值: ''
```

### 6. IcuWakeup

**描述**: This container contains the configuration (parameters) needed to configure a wakeup capable channel

该容器没有参数。

### 7. IcuGeneral

**描述**: Configuration of general ICU parameters.

#### 参数列表

```yaml
- 
  序号: 1
  名称: IcuDevErrorDetect
  长名称: ''
  描述: Switches the Development Error Detection and Notification
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: IcuIndex
  长名称: ''
  描述: Specifies the InstanceId of this module instance. If only one instance is present it shall
      have the Id 0.
  默认值: ''
  最小值: 0
  最大值: 255
- 
  序号: 3
  名称: IcuReportWakeupSource
  长名称: ''
  描述: Switch for enabling Wakeup source reporting.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 8. IcuOptionalApis

**描述**: This container contains all configuration switches for configuring optional API services of the ICU
driver.

#### 参数列表

```yaml
- 
  序号: 1
  名称: IcuDeInitApi
  长名称: ''
  描述: Adds / removes the service Icu_DeInit() from the code.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: IcuDisableWakeupApi
  长名称: ''
  描述: Adds / removes the service Icu_DisableWakeup() from the code.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: IcuEdgeCountApi
  长名称: ''
  描述: Adds / removes all services related to the edge counting functionality as listed below, from
      the code: Icu_ResetEdgeCount(), Icu_EnableEdgeCount(), Icu_DisableEdgeCount(),
      Icu_GetEdgeNumbers().
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: IcuEdgeDetectApi
  长名称: ''
  描述: Adds / removes the services related to the edge detection functionality, from the code:
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: IcuEnableWakeupApi
  长名称: ''
  描述: Adds / removes the service Icu_EnableWakeup() from the code.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: IcuGetDutyCycleValuesApi
  长名称: ''
  描述: Adds / removes the service Icu_GetDutyCycleValues() from the code.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: IcuGetInputStateApi
  长名称: ''
  描述: Adds / removes the service Icu_GetInputState() from the code.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 8
  名称: IcuGetTimeElapsedApi
  长名称: ''
  描述: Adds / removes the service Icu_GetTimeElapsed() from the code.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 9
  名称: IcuGetVersionInfoApi
  长名称: ''
  描述: Adds / removes the service Icu_GetVersionInfo() from the code.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 10
  名称: IcuSetModeApi
  长名称: ''
  描述: Adds / removes the service Icu_SetMode() from the code.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 11
  名称: IcuSignalMeasurementApi
  长名称: ''
  描述: Adds / removes the services Icu_StartSignalMeasurement() and Icu_StopSignalMeasurement() from
      the code.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 12
  名称: IcuTimestampApi
  长名称: ''
  描述: Adds / removes all services related to the timestamping functionality as listed below from the
      code: Icu_StartTimestamp(), Icu_StopTimestamp(), Icu_GetTimestampIndex().
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 13
  名称: IcuWakeupFunctionalityApi
  长名称: ''
  描述: Adds / removes the service Icu_CheckWakeup() from the code.
  默认值: ''
  最小值: ''
  最大值: ''
```

