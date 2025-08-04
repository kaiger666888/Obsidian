# FlsTst

## 容器列表

### 1. FlsTstConfigSet

**描述**: Multiple Configuration Set Container

#### 参数列表

```yaml
- 
  序号: 1
  名称: FlsTstBlockNumberBgnd
  长名称: ''
  描述: This parameter shall represent the number of test blocks available for the background test.
  默认值: ''
  最小值: 0
  最大值: 4294967295
- 
  序号: 2
  名称: FlsTstBlockNumberFgnd
  长名称: ''
  描述: This parameter shall represent the number of test blocks available for the foreground test.
  默认值: ''
  最小值: 0
  最大值: 4294967295
- 
  序号: 3
  名称: FlsTstTestCompletedNotification
  长名称: ''
  描述: Pointer to function, which shall be called after finishing the background Flash test interval.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 2. FlsTstBlockBgndConfigSet

**描述**: This container defines the blocks in background mode.

该容器没有参数。

### 3. FlsTstBlock

**描述**: This container specifies configuration parameters for an individual test block.

#### 参数列表

```yaml
- 
  序号: 1
  名称: FlsTstBlockBaseAddress
  长名称: ''
  描述: Start Address of the Flash block.
  默认值: ''
  最小值: 0
  最大值: 18446744073709551615
- 
  序号: 2
  名称: FlsTstBlockIndex
  长名称: ''
  描述: Foreground Test: Index identifies block to be tested by FlsTst_StartFgnd();
  默认值: ''
  最小值: 0
  最大值: 4294967295
- 
  序号: 3
  名称: FlsTstBlockSize
  长名称: ''
  描述: This parameter shall represent the Flash Test block size.
  默认值: ''
  最小值: 0
  最大值: 4294967295
- 
  序号: 4
  名称: FlsTstNumberOfTestedCells
  长名称: ''
  描述: Configures the Number of cells to be tested in background mode during one scheduled task
      (FlsTst_MainFunction() call).
  默认值: ''
  最小值: 0
  最大值: 4294967295
- 
  序号: 5
  名称: FlsTstSignatureAddress
  长名称: ''
  描述: Address of the signature reference value of the Flash test block.
  默认值: ''
  最小值: 0
  最大值: 18446744073709551615
- 
  序号: 6
  名称: FlsTstTestAlgorithm
  长名称: ''
  描述: This is the configuration of the test algorithm for foreground mode and background mode. The
      availability of algorithm is implementation specific.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 4. FlsTstBlockFgndConfigSet

**描述**: This container defines the blocks in foreground mode.

该容器没有参数。

### 5. FlsTstBlock

**描述**: This container specifies configuration parameters for an individual test block.

#### 参数列表

```yaml
- 
  序号: 1
  名称: FlsTstBlockBaseAddress
  长名称: ''
  描述: Start Address of the Flash block.
  默认值: ''
  最小值: 0
  最大值: 18446744073709551615
- 
  序号: 2
  名称: FlsTstBlockIndex
  长名称: ''
  描述: Foreground Test: Index identifies block to be tested by FlsTst_StartFgnd();
  默认值: ''
  最小值: 0
  最大值: 4294967295
- 
  序号: 3
  名称: FlsTstBlockSize
  长名称: ''
  描述: This parameter shall represent the Flash Test block size.
  默认值: ''
  最小值: 0
  最大值: 4294967295
- 
  序号: 4
  名称: FlsTstNumberOfTestedCells
  长名称: ''
  描述: Configures the Number of cells to be tested in background mode during one scheduled task
      (FlsTst_MainFunction() call).
  默认值: ''
  最小值: 0
  最大值: 4294967295
- 
  序号: 5
  名称: FlsTstSignatureAddress
  长名称: ''
  描述: Address of the signature reference value of the Flash test block.
  默认值: ''
  最小值: 0
  最大值: 18446744073709551615
- 
  序号: 6
  名称: FlsTstTestAlgorithm
  长名称: ''
  描述: This is the configuration of the test algorithm for foreground mode and background mode. The
      availability of algorithm is implementation specific.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 6. FlsTstConfigurationOfOptApiServices

#### 参数列表

```yaml
- 
  序号: 1
  名称: FlsTstGetCurrentStateApi
  长名称: ''
  描述: Adds / removes the service FlsTst_GetCurrentState() from the code.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: FlsTstGetErrorDetailsApi
  长名称: ''
  描述: Adds / removes the service FlsTst_GetErrorDetails() from the code.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: FlsTstGetTestResultBgndApi
  长名称: ''
  描述: Adds / removes the service FlsTst_GetTestResultBgnd() from the code.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: FlsTstGetTestResultFgndApi
  长名称: ''
  描述: Adds / removes the service FlsTst_GetTestResultFgnd() from the code.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: FlsTstGetTestSignatureBgndApi
  长名称: ''
  描述: Adds / removes the service FlsTst_GetTestSignatureBgnd() from the code.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: FlsTstGetTestSignatureFgndApi
  长名称: ''
  描述: Adds / removes the service FlsTst_GetTestSignatureFgnd() from the code.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: FlsTstStartFgndApi
  长名称: ''
  描述: Adds / removes the service FlsTst_StartFgnd() from the code.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 8
  名称: FlsTstSuspendResumeApi
  长名称: ''
  描述: Adds / removes the services FlsTst_Suspend() and FlsTst_Resume() from the code.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 9
  名称: FlsTstTestEccApi
  长名称: ''
  描述: Adds / removes the service FlsTst_TestEcc() from the code.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 10
  名称: FlsTstVersionInfoApi
  长名称: ''
  描述: Adds / removes the service FlsTst_GetVersionInfo() from the code.
  默认值: false
  最小值: ''
  最大值: ''
```

### 7. FlsTstDemEventParameterRefs

**描述**: Container for the references to DemEventParameter elements which shall be invoked using the API
Dem_ReportErrorStatus API in case the corresponding error occurs. The EventId is taken from the
referenced DemEventParameter's DemEventId value. The standardized errors are provided in the
container and can be extended by vendor specific error references.

该容器没有参数。

### 8. FlsTstGeneral

#### 参数列表

```yaml
- 
  序号: 1
  名称: FlsTstDevErrorDetect
  长名称: ''
  描述: Switch for enabling the development error detection.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: FlsTstNumberOfTestedCellsAtomic
  长名称: ''
  描述: Configures the Number of cells to be tested in background mode without checking user requests
      (Abort, Suspend).
  默认值: ''
  最小值: 0
  最大值: 4294967295
- 
  序号: 3
  名称: FlsTstTestCompletedNotificationSupported
  长名称: ''
  描述: Switch to indicate that the notification is supported.
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: FlsTstTestIntervalIdEndValue
  长名称: ''
  描述: Defines the end value of the Test Interval Id.
  默认值: ''
  最小值: 0
  最大值: 4294967295
- 
  序号: 5
  名称: FlsTstTestResultSignature
  长名称: ''
  描述: Configures the result of the test in background mode:
  默认值: false
  最小值: ''
  最大值: ''
```

