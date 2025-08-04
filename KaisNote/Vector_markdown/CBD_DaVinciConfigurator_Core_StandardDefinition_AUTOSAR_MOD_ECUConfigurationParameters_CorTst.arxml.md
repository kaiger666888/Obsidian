# CorTst

## 模块描述

Configuration of the CorTst module.

## 容器列表

### 1. CorTstBackgroundConfigSet

**描述**: Multiple Configuration Set Container, defines background mode.

该容器没有参数。

### 2. CorTstSelect

**描述**: This container specifies configuration parameters to select individual tests for foreground mode and
background mode. The availability is hardware and implementation specific.

#### 参数列表

```yaml
- 
  序号: 1
  名称: CorTstAddress
  长名称: ''
  描述: Enable/Disables core address test.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: CorTstAlu
  长名称: ''
  描述: Enable/Disables core ALU test.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: CorTstCache
  长名称: ''
  描述: Enable/Disables core cache test.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: CorTstInterrupt
  长名称: ''
  描述: Enable/Disables core interrupt test
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: CorTstMemoryIf
  长名称: ''
  描述: Enable/Disables core memory interface test
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: CorTstMpu
  长名称: ''
  描述: Enable/Disables core MPU test
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: CorTstRegister
  长名称: ''
  描述: Enable/Disables core register test
  默认值: false
  最小值: ''
  最大值: ''
```

### 3. CorTstConfigApiServices

#### 参数列表

```yaml
- 
  序号: 1
  名称: CorTstAbortApi
  长名称: ''
  描述: Adds / removes the service CorTst_Abort() from the code.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: CorTstGetCurrentStatus
  长名称: ''
  描述: Adds / removes the service CorTst_GetCurrentStatus() from the code.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: CorTstGetFgndSignature
  长名称: ''
  描述: Adds / removes the service CorTst_GetFgndSignature() from the code.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: CorTstGetSignature
  长名称: ''
  描述: Adds / removes the service CorTst_GetSignature() from the code.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: CorTstGetStateApi
  长名称: ''
  描述: Adds / removes the service CorTst_GetState() from the code.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: CorTstStartApi
  长名称: ''
  描述: Adds / removes the service CorTst_Start() from the code.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: CorTstVersionInfoApi
  长名称: ''
  描述: Adds / removes the service CorTst_GetVersionInfo() from the code.
  默认值: false
  最小值: ''
  最大值: ''
```

### 4. CorTstDemEventParameterRefs

**描述**: Container for the references to DemEventParameter elements which shall be invoked using the API
Dem_ReportErrorStatus in case the corresponding error occurs. The EventId is taken from the
referenced DemEventParameter's DemEventId value. The standardized errors are provided in the
container and can be extended by vendor specific error references.

该容器没有参数。

### 5. CorTstForegroundConfigSet

**描述**: Multiple Configuration Set Container , defines foreground mode.

#### 参数列表

```yaml
- 
  序号: 1
  名称: CorTstTestIdFgnd
  长名称: ''
  描述: This is the Id of this specific foreground test configuration. The value shall be used in the
      call to the API CorTst_Start(CorTst_TestIdFgndType TestId).
  默认值: ''
  最小值: 0
  最大值: 4294967295
```

### 6. CorTstSelect

**描述**: This container specifies configuration parameters to select individual tests for foreground mode and
background mode. The availability is hardware and implementation specific.

#### 参数列表

```yaml
- 
  序号: 1
  名称: CorTstAddress
  长名称: ''
  描述: Enable/Disables core address test.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: CorTstAlu
  长名称: ''
  描述: Enable/Disables core ALU test.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: CorTstCache
  长名称: ''
  描述: Enable/Disables core cache test.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: CorTstInterrupt
  长名称: ''
  描述: Enable/Disables core interrupt test
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: CorTstMemoryIf
  长名称: ''
  描述: Enable/Disables core memory interface test
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: CorTstMpu
  长名称: ''
  描述: Enable/Disables core MPU test
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: CorTstRegister
  长名称: ''
  描述: Enable/Disables core register test
  默认值: false
  最小值: ''
  最大值: ''
```

### 7. CorTstGeneral

#### 参数列表

```yaml
- 
  序号: 1
  名称: CorTstDevErrorDetect
  长名称: ''
  描述: Switch for enabling the development error detection.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: CorTstFgndTestNumber
  长名称: ''
  描述: This parameter holds the number of test configurations available for the foreground tests as
      defined in this configuration.
  默认值: ''
  最小值: 1
  最大值: 4294967295
- 
  序号: 3
  名称: CorTstNotificationSupported
  长名称: ''
  描述: Switch to indicate that the notification is supported.
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: CorTstTestIntervalIdEndValue
  长名称: ''
  描述: Defines the end value of the Test Interval Id.
  默认值: ''
  最小值: 0
  最大值: 4294967295
- 
  序号: 5
  名称: CorTstTestResultMode
  长名称: ''
  描述: Switch for enabling test result comparison within the Core test driver. In this mode a core
      test result OK or NOTOK shall not be calculated from the core test driver. Within core
      test driver no comparison against the reference value is processed.
  默认值: false
  最小值: ''
  最大值: ''
```

