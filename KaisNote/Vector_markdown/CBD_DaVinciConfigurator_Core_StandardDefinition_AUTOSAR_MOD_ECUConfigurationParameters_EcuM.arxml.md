# EcuM

## 模块描述

Configuration of the EcuM (ECU State Manager) module.

## 容器列表

### 1. EcuMConfiguration

**描述**: This container contains the configuration (parameters) of the ECU State Manager.

该容器没有参数。

### 2. EcuMCommonConfiguration

**描述**: This container contains the common configuration (parameters) of the ECU State Manager.

#### 参数列表

```yaml
- 
  序号: 1
  名称: EcuMConfigConsistencyHash
  长名称: ''
  描述: A hash value generated across all pre-compile and link-time parameters of all BSW modules.
      This hash value is compared against a field in the EcuM_ConfigType and hence allows
      checking the consistency of the entire configuration.
  默认值: ''
  最小值: 0
  最大值: 18446744073709551615
```

### 3. EcuMDefaultShutdownTarget

**描述**: This container describes the default shutdown target to be selected by EcuM. The actual shutdown
target may be overridden by the EcuM_SelectShutdownTarget service.

#### 参数列表

```yaml
- 
  序号: 1
  名称: EcuMDefaultState
  长名称: ''
  描述: This parameter describes the state part of the default shutdown target selected when the ECU
      comes out of reset. If EcuMStateSleep is selected, the parameter EcuMDefaultSleepModeRef
      selects the specific sleep mode.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 4. EcuMDemEventParameterRefs

**描述**: Container for the references to DemEventParameter elements which shall be invoked using the API
Dem_ReportErrorStatus in case the corresponding error occurs. The EventId is taken from the
referenced DemEventParameter's DemEventId value.

该容器没有参数。

### 5. EcuMDriverInitListOne

**描述**: Container for Init Block I.

该容器没有参数。

### 6. EcuMDriverInitItem

**描述**: These containers describe the entries in a driver init list.

#### 参数列表

```yaml
- 
  序号: 1
  名称: EcuMModuleID
  长名称: ''
  描述: Short name of the module to be initialized, e.g. Mcu, Gpt etc.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: EcuMModuleService
  长名称: ''
  描述: The service to be called to initialize that module, e.g. Init, PreInit, Start etc.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 7. EcuMDriverInitListZero

**描述**: Container for Init Block 0.

该容器没有参数。

### 8. EcuMDriverInitItem

**描述**: These containers describe the entries in a driver init list.

#### 参数列表

```yaml
- 
  序号: 1
  名称: EcuMModuleID
  长名称: ''
  描述: Short name of the module to be initialized, e.g. Mcu, Gpt etc.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: EcuMModuleService
  长名称: ''
  描述: The service to be called to initialize that module, e.g. Init, PreInit, Start etc.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 9. EcuMDriverRestartList

**描述**: List of module IDs.

该容器没有参数。

### 10. EcuMDriverInitItem

**描述**: These containers describe the entries in a driver init list.

#### 参数列表

```yaml
- 
  序号: 1
  名称: EcuMModuleID
  长名称: ''
  描述: Short name of the module to be initialized, e.g. Mcu, Gpt etc.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: EcuMModuleService
  长名称: ''
  描述: The service to be called to initialize that module, e.g. Init, PreInit, Start etc.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 11. EcuMSleepMode

**描述**: These containers describe the configured sleep modes.

#### 参数列表

```yaml
- 
  序号: 1
  名称: EcuMSleepModeId
  长名称: ''
  描述: This ID identifies this sleep mode in services like EcuM_SelectShutdownTarget.
  默认值: ''
  最小值: 0
  最大值: 255
- 
  序号: 2
  名称: EcuMSleepModeSuspend
  长名称: ''
  描述: Flag, which is set true, if the CPU is suspended, halted, or powered off in the sleep mode. If
      the CPU keeps running in this sleep mode, then this flag must be set to false.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 12. EcuMWakeupSource

**描述**: These containers describe the configured wakeup sources.

#### 参数列表

```yaml
- 
  序号: 1
  名称: EcuMValidationTimeout
  长名称: ''
  描述: The validation timeout (period for which the ECU State Manager will wait for the validation of
      a wakeup event) can be defined for each wakeup source independently. The timeout is
      specified in seconds.
  默认值: ''
  最小值: 0
  最大值: Inf
- 
  序号: 2
  名称: EcuMWakeupSourceId
  长名称: ''
  描述: This parameter defines the identifier of this wakeup source.
  默认值: ''
  最小值: 0
  最大值: 31
- 
  序号: 3
  名称: EcuMWakeupSourcePolling
  长名称: ''
  描述: This parameter describes if the wakeup source needs polling.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 13. EcuMFixedConfiguration

**描述**: This container contains the configuration (parameters) of the EcuMFixed.

#### 参数列表

```yaml
- 
  序号: 1
  名称: EcuMNvramReadallTimeout
  长名称: ''
  描述: Period given in seconds for which the ECU State Manager will wait until it considers a ReadAll
      job of the NVRAM Manager as failed.
  默认值: ''
  最小值: 0
  最大值: Inf
- 
  序号: 2
  名称: EcuMNvramWriteallTimeout
  长名称: ''
  描述: Period given in seconds for which the ECU State Manager will wait until it considers a
      WriteAll job of the NVRAM Manager as failed.
  默认值: ''
  最小值: 0
  最大值: Inf
- 
  序号: 3
  名称: EcuMRunMinimumDuration
  长名称: ''
  描述: Duration given in seconds for which the ECU State Manager will
  默认值: ''
  最小值: 0
  最大值: Inf
```

### 14. EcuMDriverInitListThree

**描述**: Container for Init Block III.

该容器没有参数。

### 15. EcuMDriverInitItem

**描述**: These containers describe the entries in a driver init list.

#### 参数列表

```yaml
- 
  序号: 1
  名称: EcuMModuleID
  长名称: ''
  描述: Short name of the module to be initialized, e.g. Mcu, Gpt etc.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: EcuMModuleService
  长名称: ''
  描述: The service to be called to initialize that module, e.g. Init, PreInit, Start etc.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 16. EcuMDriverInitListTwo

**描述**: Container for Init Block II.

该容器没有参数。

### 17. EcuMDriverInitItem

**描述**: These containers describe the entries in a driver init list.

#### 参数列表

```yaml
- 
  序号: 1
  名称: EcuMModuleID
  长名称: ''
  描述: Short name of the module to be initialized, e.g. Mcu, Gpt etc.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: EcuMModuleService
  长名称: ''
  描述: The service to be called to initialize that module, e.g. Init, PreInit, Start etc.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 18. EcuMFixedUserConfig

**描述**: These containers describe the identifiers that are needed to refer to a software component or
another appropriate entity in the system which is designated to request the RUN state. Application
requestors refer to entities above RTE, system requestors to entities below RTE (e.g. Communication
Manager).

#### 参数列表

```yaml
- 
  序号: 1
  名称: EcuMFixedUser
  长名称: ''
  描述: Parameter used to identify one user.
  默认值: ''
  最小值: 0
  最大值: 255
```

### 19. EcuMTTII

**描述**: These containers describe the structures and the following configuration items describe its
elements. These structures are concatenated to build a list as indicated by Figure 27 -
Configuration Container Diagram.

#### 参数列表

```yaml
- 
  序号: 1
  名称: EcuMDivisor
  长名称: ''
  描述: This parameter defines the divisor preload value.
  默认值: ''
  最小值: 0
  最大值: 18446744073709551615
```

### 20. EcuMFlexConfiguration

**描述**: This container contains the configuration (parameters) of the EcuMFlex.

该容器没有参数。

### 21. EcuMAlarmClock

**描述**: These containers describe the configured alarm clocks.

#### 参数列表

```yaml
- 
  序号: 1
  名称: EcuMAlarmClockId
  长名称: ''
  描述: This ID identifies this alarmclock.
  默认值: ''
  最小值: 0
  最大值: 255
- 
  序号: 2
  名称: EcuMAlarmClockTimeOut
  长名称: ''
  描述: This parameter allows to define a timout for this alarm clock.
  默认值: ''
  最小值: 0
  最大值: Inf
```

### 22. EcuMFlexUserConfig

**描述**: These containers describe the identifiers that are needed to refer to a software component or
another appropriate entity in the system which uses the EcuMFlex Interfaces.

#### 参数列表

```yaml
- 
  序号: 1
  名称: EcuMFlexUser
  长名称: ''
  描述: Parameter used to identify one user.
  默认值: ''
  最小值: 0
  最大值: 255
```

### 23. EcuMGoDownAllowedUsers

**描述**: This container describes the collection of allowed users which are allowed to call the EcuM_GoDown
API.

该容器没有参数。

### 24. EcuMResetMode

**描述**: These containers describe the configured reset modes.

#### 参数列表

```yaml
- 
  序号: 1
  名称: EcuMResetModeId
  长名称: ''
  描述: This ID identifies this reset mode in services like EcuM_SelectShutdownTarget.
  默认值: ''
  最小值: 0
  最大值: 255
```

### 25. EcuMSetClockAllowedUsers

**描述**: This container describes the collection of allowed users which are allowed to call the EcuM_SetClock
API.

该容器没有参数。

### 26. EcuMShutdownCause

**描述**: These containers describe the configured shut down or reset causes.

#### 参数列表

```yaml
- 
  序号: 1
  名称: EcuMShutdownCauseId
  长名称: ''
  描述: This ID identifies this shut down cause.
  默认值: ''
  最小值: 0
  最大值: 255
```

### 27. EcuMShutdownTarget

**描述**: These containers describe the configured shut down targets.

#### 参数列表

```yaml
- 
  序号: 1
  名称: EcuMShutdownTargetId
  长名称: ''
  描述: This ID identifies this shut down target in services like EcuM_SelectShutdownTarget.
  默认值: ''
  最小值: 0
  最大值: 255
```

### 28. EcuMFixedGeneral

**描述**: This container holds the general, pre-compile configuration parameters for the EcuMFixed.

#### 参数列表

```yaml
- 
  序号: 1
  名称: EcuMIncludeComM
  长名称: ''
  描述: This configuration parameter defines whether the communication  manager is supported by EcuM.
      This feature is presented for development purpose to compile out the communication
      manager in the early debugging phase.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: EcuMIncludeNvM
  长名称: ''
  描述: This configuration parameter defines whether the non volatile memory manager is supported by
      EcuM. This feature is presented for development purpose to compile out the volatile
      memory manager in the early debugging phase.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: EcuMIncludeNvramMgr
  长名称: ''
  描述: If NVRAM manager is enabled but both flash and EEPROM driver are missing, then an error shall
      be flagged by the configuration tool
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: EcuMTTIIEnabled
  长名称: ''
  描述: Boolean switch to enable / disable TTII
  默认值: ''
  最小值: ''
  最大值: ''
```

### 29. EcuMFlexGeneral

**描述**: This container holds the general, pre-compile configuration parameters for the EcuMFlex.

#### 参数列表

```yaml
- 
  序号: 1
  名称: EcuMAlarmClockPresent
  长名称: ''
  描述: This flag indicates whether the optional AlarmClock feature is present.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: EcuMEnableDefBehaviour
  长名称: ''
  描述: Switches the defensive behaviour on or off.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: EcuMResetLoopDetection
  长名称: ''
  描述: If false, no reset loop detection is performed.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 30. EcuMGeneral

**描述**: This container holds the general, pre-compile configuration parameters.

#### 参数列表

```yaml
- 
  序号: 1
  名称: EcuMDevErrorDetect
  长名称: ''
  描述: If false, no debug artifacts (e.g. calls to DET) shall remain in the executable object.
      Initialization of DET, however is controlled by configuration of optional BSW modules.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: EcuMIncludeDem
  长名称: ''
  描述: If enabled, the according BSW module will be included to the ECU State Manager.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: EcuMIncludeDet
  长名称: ''
  描述: If defined, the according BSW module will be initialized by the ECU State Manager
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: EcuMMainFunctionPeriod
  长名称: ''
  描述: This parameter defines the schedule period of EcuM_MainFunction.
  默认值: ''
  最小值: 0
  最大值: Inf
- 
  序号: 5
  名称: EcuMVersionInfoApi
  长名称: ''
  描述: Switches the version info API on or off
  默认值: ''
  最小值: ''
  最大值: ''
```

