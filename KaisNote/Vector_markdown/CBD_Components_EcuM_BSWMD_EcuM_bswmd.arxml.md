# EcuM

## 模块描述

Configuration of the ECU State Manager (EcuM) module. The EcuM manages the intialization and
de-initialization of OS, SchM, BswM and other base SW modules. It is responisble for startup,
shutdown, sleep modes and wakeup sources of the ECU.
#ModeManagement #Startup #Shutdown #Wakeup
#AUTOSAR #ServiceComponent

## 容器列表

### 1. EcuMConfiguration

**描述**: This container includes the configuration (parameters) of the ECU State Manager.

该容器没有参数。

### 2. EcuMCommonConfiguration

**描述**: This container includes the common configuration (parameters) of the ECU State Manager.

#### 参数列表

```yaml
- 
  序号: 1
  名称: EcuMConfigConsistencyHash
  长名称: ''
  描述: This value specifies a hash value generated across all pre-compile and link-time parameters of
      all BSW modules. This hash value is compared against a field in the EcuM_ConfigType and
      hence allows checking the consistency of the entire configuration.
  默认值: 0
  最小值: 0
  最大值: 18446744073709551615
```

### 3. EcuMDefaultShutdownTarget

**描述**: This container includes the default shutdown target to be selected by EcuM. The actual shutdown
target may be overridden by the EcuM_SelectShutdownTarget service.

#### 参数列表

```yaml
- 
  序号: 1
  名称: EcuMDefaultState
  长名称: ''
  描述: |
    This parameter defines the state part of the default shutdown target selected when the ECU comes
    out of reset.
    If EcuMStateSleep is selected, the parameter EcuMDefaultSleepModeRef selects the specific sleep
    mode. If EcuMStateReset is selected, the parameter EcuMDefaultResetModeRef selects the specific
    reset mode.
  默认值: EcuMStateOff
  最小值: ''
  最大值: ''
```

### 4. EcuMDemEventParameterRefs

**描述**: This container includes references to DemEventParameter elements which shall be invoked using the
API Dem_ReportErrorStatus in case the corresponding error occurs. The EventId is taken from the
referenced DemEventParameter's DemEventId value.

该容器没有参数。

### 5. EcuMDriverInitListOne

**描述**: This container includes a list of initialization items that will be handled after a reset from
within EcuM_Init function after the module has entered the state ECUM_STATE_STARTUP_ONE.

All items in this list are initialized before the post-build configuration has been loaded and the
OS is initialized. Therefore none of these items may use post-build configuration.

该容器没有参数。

### 6. EcuMDriverInitItem

**描述**: These containers include the configuration of one initialization item. This may either be a module
initialization function or any user defined code.

#### 参数列表

```yaml
- 
  序号: 1
  名称: EcuMModuleID
  长名称: ''
  描述: Short name of the module to be initialized, e.g. Mcu, Gpt etc.  For user defined code given in
      EcuMAdditionalInitCode 'Code' has to be given.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: EcuMModuleService
  长名称: ''
  描述: |
    This parameter defines the service to be called to initialize that module, e.g. Init, PreInit,
    Start etc. If the service is Init and the parameter EcuMModuleConfigurationRef has been set for
    that module,
    the corresponding pointer to the init structure (<Module>_ConfigType) and in case of multiple
    instantiation an uint8 value to identify the instance of the  module(<MSN>_CtrlIdx) are be
    passed as arguments.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: EcuMAdditionalInitCode
  长名称: ''
  描述: |
    This parameter defines an additional code in the callout function, e.g. Mcu_InitClock(). If this
    code needs other header files, they can be included via the parameter EcuMAdditionalIncludes.
    
    RESTRICTIONS: 'EcuMAdditionalInitCode' is only available, if 'EcuMModuleID' is set to 'Code'.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: EcuMModuleHeader
  长名称: ''
  描述: This parameter defines a header file needed for this driver init item.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 7. EcuMDriverInitListZero

**描述**: This container includes a list of initialization items that will be handled after a reset almost
directly after EcuM_Init has been called.

All items in this list are initialized before the post-build configuration has been loaded and the
OS is initialized. Therefore none of these items may use post-build configuration.

该容器没有参数。

### 8. EcuMDriverInitItem

**描述**: These containers include the configuration of one initialization item. This may either be a module
initialization function or any user defined code.

#### 参数列表

```yaml
- 
  序号: 1
  名称: EcuMModuleID
  长名称: ''
  描述: Short name of the module to be initialized, e.g. Mcu, Gpt etc. For user defined code given in
      EcuMAdditionalInitCode 'Code' has to be given.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: EcuMModuleService
  长名称: ''
  描述: |
    This parameter defines the service to be called to initialize that module, e.g. Init, PreInit,
    Start etc. If the service is Init and the parameter EcuMModuleConfigurationRef has been set for
    that module, the corresponding pointer to the init structure (<Module>_ConfigType) and in case
    of multiple instantiation an uint8 value to identify the instance of the module(<MSN>_CtrlIdx)
    are be passed as arguments.
    
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: EcuMAdditionalInitCode
  长名称: ''
  描述: |
    This parameter defines additional code in the callout function, e.g. Mcu_InitClock(). If this
    code needs other header files, they can be included via the parameter EcuMAdditionalIncludes.
    
    RESTRICTIONS: 'EcuMAdditionalInitCode' is only available, if 'EcuMModuleID' is set to 'Code'.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: EcuMModuleHeader
  长名称: ''
  描述: This parameter defines a header file needed for this driver init item.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 9. EcuMDriverRestartList

**描述**: This container includes a list of initialization items that will be handled after a restart from
SLEEP mode occurred.

EcuMDriverRestartList shall normally do the same initialization calls listed in the order in which
they occur in the EcuMDriverInitListZero and EcuMDriverInitListOne.


该容器没有参数。

### 10. EcuMDriverInitItem

**描述**: These containers include the configuration of one initialization item. This may either be a module
initialization function or any user defined code.

#### 参数列表

```yaml
- 
  序号: 1
  名称: EcuMModuleID
  长名称: ''
  描述: Short name of the module to be initialized, e.g. Mcu, Gpt etc. For user defined code given in
      EcuMAdditionalInitCode 'Code' has to be given.
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
- 
  序号: 3
  名称: EcuMAdditionalInitCode
  长名称: ''
  描述: |
    This parameter defines additional code in the callout function, e.g. Mcu_InitClock(). If this
    code needs other header files, they can be included via the parameter EcuMAdditionalIncludes.
    
    RESTRICTIONS: 'EcuMAdditionalInitCode' is only available, if 'EcuMModuleID' is set to 'Code'.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: EcuMModuleHeader
  长名称: ''
  描述: This parameter defines a header file needed for driver init items.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 11. EcuMSleepMode

**描述**: This container includes the configuration of one sleep modes. The name of this container specify the
symbolic name of a sleep mode and identifies the corresponding sources which should be active during
this sleep phase.

#### 参数列表

```yaml
- 
  序号: 1
  名称: EcuMSleepModeId
  长名称: ''
  描述: This value specifies the identifier of this sleep mode in services like
      EcuM_SelectShutdownTarget.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 2
  名称: EcuMSleepModeSuspend
  长名称: ''
  描述: |
    Not used!
    
    This parameter defines if the CPU is suspended, halted or powered off in the sleep mode. If the
    CPU keeps running in this sleep mode, then this flag must be set to false.
    
  默认值: false
  最小值: ''
  最大值: ''
```

### 12. EcuMWakeupSource

**描述**: This container includes the configuration of a wakeup source.

#### 参数列表

```yaml
- 
  序号: 1
  名称: EcuMValidationTimeout
  长名称: ''
  描述: The validation timeout (period for which the ECU State Manager will wait for the validation of
      a wakeup event) can be defined for each wakeup source independently. If the parameter is
      not defined or is defined to 0 the wakeup validation is disabled for this wakeup source.
  默认值: 0
  最小值: 0
  最大值: 65.535
- 
  序号: 2
  名称: EcuMWakeupSourceId
  长名称: ''
  描述: This value specifies the identifier of this wakeup source.
  默认值: 0
  最小值: 0
  最大值: 31
- 
  序号: 3
  名称: EcuMWakeupSourcePolling
  长名称: ''
  描述: This parameter defines if the wakeup source needs polling.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: EcuMCheckWakeupTimeout
  长名称: ''
  描述: This parameter specifies the maximum time between the call of EcuM_CheckWakeup and an
      asynchronous call of EcuM_SetWakeupEvent of the same wakeup source. If the timeout
      expires the ECU is allowed to go to sleep state. For wakeup sources where it is ensured
      that the EcuM_SetWakeupEvent is called before EcuM_CheckWakeup function ends the timeout
      value shall be 0 or the parameter shall be deleted.
  默认值: 0
  最小值: 0
  最大值: 10
```

### 13. EcuMFixedConfiguration

**描述**: This container includes the configuration (parameters) of the EcuMFixed.

#### 参数列表

```yaml
- 
  序号: 1
  名称: EcuMNvramReadallTimeout
  长名称: ''
  描述: |
    Not used!
    
    Period given in seconds for which the ECU State Manager will wait until it considers a ReadAll
    job of the NVRAM Manager as failed.
  默认值: 60
  最小值: 0
  最大值: 60
- 
  序号: 2
  名称: EcuMNvramWriteallTimeout
  长名称: ''
  描述: Period given in seconds for which the ECU State Manager will wait until it considers a
      WriteAll job of the NVRAM Manager as failed.
  默认值: 60
  最小值: 0
  最大值: 60
- 
  序号: 3
  名称: EcuMRunMinimumDuration
  长名称: ''
  描述: Duration given in seconds for which the ECU State Manager will
  默认值: 5
  最小值: 0
  最大值: 60
- 
  序号: 4
  名称: EcuMNvmCancelWriteAllTimeout
  长名称: ''
  描述: This parameter specifies the time in seconds which shall be waited for NvM_WriteAll in case
      NvM_CancelWriteAll was called due to a wakeup event.
  默认值: 60
  最小值: 0
  最大值: 60
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
- 
  序号: 3
  名称: EcuMAdditionalInitCode
  长名称: ''
  描述: |
    This parameter defines an additional code in the callout function, e.g. Mcu_InitClock(). If this
    code needs other header files, they can be included via the parameter EcuMAdditionalIncludes.
    
    RESTRICTIONS: 'EcuMAdditionalInitCode' is only available, if 'EcuMModuleID' is set to 'Code'.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: EcuMModuleHeader
  长名称: ''
  描述: This parameter defines a header file needed for driver init items.
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
- 
  序号: 3
  名称: EcuMAdditionalInitCode
  长名称: ''
  描述: |
    This parameter defines an additional code in the callout function, e.g. Mcu_InitClock(). If this
    code needs other header files, they can be included via the parameter EcuMAdditionalIncludes.
    
    RESTRICTIONS: 'EcuMAdditionalInitCode' is only available, if 'EcuMModuleID' is set to 'Code'.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: EcuMModuleHeader
  长名称: ''
  描述: This parameter defines a header file needed for driver init items.
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
  默认值: 0
  最小值: 0
  最大值: 255
```

### 19. EcuMTTII

**描述**: Not used!

These containers describe the structures and the following configuration items describe its
elements. These structures are concatenated to build a list as indicated by Figure 27 -
Configuration Container Diagram.

#### 参数列表

```yaml
- 
  序号: 1
  名称: EcuMDivisor
  长名称: ''
  描述: This parameter defines the divisor pre load value.
  默认值: ''
  最小值: 0
  最大值: 18446744073709551615
```

### 20. EcuMFlexConfiguration

**描述**: This container includes the configuration (parameters) of the EcuMFlex.

该容器没有参数。

### 21. EcuMAlarmClock

**描述**: These containers include the configured alarm clocks.


#### 参数列表

```yaml
- 
  序号: 1
  名称: EcuMAlarmClockId
  长名称: ''
  描述: This ID identifies this alarmclock.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 2
  名称: EcuMAlarmClockTimeOut
  长名称: ''
  描述: |
    This parameter allows to define a timeout for this alarm clock.
    
    Not Used
  默认值: 0
  最小值: 0
  最大值: Inf
```

### 22. EcuMFlexUserConfig

**描述**: This container includes the identifiers that are needed to refer to a software component or another
appropriate entity in the system which uses the EcuMFlex Interfaces. This container is only needed
if the parameter EcuMEnableDefBehaviour is active.

#### 参数列表

```yaml
- 
  序号: 1
  名称: EcuMFlexUser
  长名称: ''
  描述: This value specifies the identifier of the EcuMFlex user.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 2
  名称: EcuMGoDownRequestID
  长名称: ''
  描述: |
    This value specifies the corresponding BSW or SWC ModuleID. The parameter is necessary to
    translate the caller ID of the API EcuM_GoDown into an EcuM_FlexUser ID.
    
    This value depends on the configuration item EcuMEnableDefBehaviour. If (EcuMEnableDefBehaviour
    == true) then this parameter is optional configurable otherwise this parameter is ignored.
    
  默认值: 42
  最小值: 1
  最大值: 65535
```

### 23. EcuMGoDownAllowedUsers

**描述**: This container includes the collection of allowed users which are allowed to call the EcuM_GoDown
API.

该容器没有参数。

### 24. EcuMResetMode

**描述**: These containers include the configured reset modes.

#### 参数列表

```yaml
- 
  序号: 1
  名称: EcuMResetModeId
  长名称: ''
  描述: This value specifies the identifier to be used in services like EcuM_SelectShutdownTarget.
  默认值: 0
  最小值: 0
  最大值: 255
```

### 25. EcuMSetClockAllowedUsers

**描述**: This container includes the collection of allowed users which are allowed to call the EcuM_SetClock
API.

该容器没有参数。

### 26. EcuMShutdownCause

**描述**: These containers include the configured shut down or reset causes.

#### 参数列表

```yaml
- 
  序号: 1
  名称: EcuMShutdownCauseId
  长名称: ''
  描述: This values specifies the identifier for API calls for this shut down cause.
  默认值: 0
  最小值: 0
  最大值: 255
```

### 27. EcuMShutdownTarget

**描述**: This container is not used including the parameters.

These containers include the configured shut down targets.

#### 参数列表

```yaml
- 
  序号: 1
  名称: EcuMShutdownTargetId
  长名称: ''
  描述: This value specifies the identifier used for this shut down target in services like
      EcuM_SelectShutdownTarget.
  默认值: 0
  最小值: 0
  最大值: 255
```

### 28. EcuMDriverInitListBswM

**描述**: This container includes a list of initialization items that will be handled after the BswM has been
initialized.


该容器没有参数。

### 29. EcuMDriverInitItem

**描述**: These containers include the configuration of one initialization item. This may either be a module
initialization function or any user defined code.

#### 参数列表

```yaml
- 
  序号: 1
  名称: EcuMModuleID
  长名称: ''
  描述: Short name of the module to be initialized, e.g. Mcu, Gpt etc.  For user defined code given in
      EcuMAdditionalInitCode 'Code' has to be given.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: EcuMModuleService
  长名称: ''
  描述: |
    This parameter defines the service to be called to initialize that module, e.g. Init, PreInit,
    Start etc. If the service is Init and the parameter EcuMModuleConfigurationRef has been set for
    that module,
    the corresponding pointer to the init structure (<Module>_ConfigType) and in case of multiple
    instantiation an uint8 value to identify the instance of the  module(<MSN>_CtrlIdx) are be
    passed as arguments.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: EcuMAdditionalInitCode
  长名称: ''
  描述: |
    This parameter defines an additional code in the callout function, e.g. Mcu_InitClock(). If this
    code needs other header files, they can be included via the parameter EcuMAdditionalIncludes.
    
    RESTRICTIONS: 'EcuMAdditionalInitCode' is only available, if 'EcuMModuleID' is set to 'Code'.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: EcuMModuleHeader
  长名称: ''
  描述: This parameter defines a header file needed for driver init items.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 30. EcuMFixedGeneral

**描述**: This container holds the general, pre-compile configuration parameters for the EcuMFixed.


#### 参数列表

```yaml
- 
  序号: 1
  名称: EcuMIncludeComM
  长名称: Include ComM
  描述: This configuration parameter defines whether the communication  manager is supported by EcuM.
      This feature is presented for development purpose to compile out the communication
      manager in the early debugging phase.
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: EcuMIncludeNvM
  长名称: Include NvM
  描述: |
    Not used!
    
    This configuration parameter defines whether the non volatile memory manager is supported by
    EcuM. This feature is presented for development purpose to compile out the volatile memory
    manager in the early debugging phase.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: EcuMIncludeNvramMgr
  长名称: ''
  描述: This configuration parameter defines whether the non volatile memory manager is supported by
      EcuM. If this parameter is active, NvM_WriteAll() handling will be done by EcuM.
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: EcuMTTIIEnabled
  长名称: ''
  描述: |
    Not used!
    
    Boolean switch to enable / disable TTII
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: EcuMIncludeRte
  长名称: ''
  描述: Enable/disables the use of the Rte.
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: EcuMGenModeSwitchPort
  长名称: ''
  描述: This parameter enables the generation of the EcuM_CurrentMode sender-receiver interface within
      the SW-C description and the usage of a callback function for mode switch notification.
      If this parameter is set to ON the ECUM will use the provided RTE function
      Rte_Switch_currentMode_currentMode().
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: EcuMModeSwitchRteAck
  长名称: ''
  描述: This parameter enables the synchronisation mechanism with RTE. In case this parameter is
      enabled, the EcuM waits on defined synchronistion points until the Rte switches into
      coresponding ECU mode. After receiving the ACK, EcuM will continue.
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 8
  名称: EcuMIncludeDem
  长名称: ''
  描述: Enable/disables the use of the Dem.
  默认值: true
  最小值: ''
  最大值: ''
```

### 31. EcuMFlexGeneral

**描述**: General configuration parameters of the EcuMFlex.

#### 参数列表

```yaml
- 
  序号: 1
  名称: EcuMAlarmClockPresent
  长名称: ''
  描述: This flag indicates whether the optional AlarmClock feature is present.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: EcuMEnableDefBehaviour
  长名称: ''
  描述: This parameter defines if the defensive behavior is enabled.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: EcuMResetLoopDetection
  长名称: ''
  描述: |
    Not used!
    
    If false, no reset loop detection is performed.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: EcuMModeHandling
  长名称: ''
  描述: Defines if the mode handling is enabled.
  默认值: false
  最小值: ''
  最大值: ''
```

### 32. EcuMGeneral

**描述**: General configuration parameters of the ECUM.

#### 参数列表

```yaml
- 
  序号: 1
  名称: EcuMDevErrorDetect
  长名称: ''
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
  名称: EcuMIncludeDem
  长名称: ''
  描述: |
    Not used!
    
    This parameter defines if the header of the DEM module will be included within the source of the
    ECU State Manager.
    
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: EcuMIncludeDet
  长名称: ''
  描述: |
    Not used!
    
    If defined, the according BSW module will be initialized by the ECU State Manager
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: EcuMMainFunctionPeriod
  长名称: ''
  描述: This value specifies the schedule period of EcuM_MainFunction.
  默认值: 0.01
  最小值: 0.001
  最大值: 0.255
- 
  序号: 5
  名称: EcuMVersionInfoApi
  长名称: ''
  描述: This parameter enables/disables the function EcuM_GetVersionInfo() to get major, minor and
      patch version information.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: EcuMAdditionalIncludes
  长名称: ''
  描述: This parameter defines header files needed for driver init lists.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: EcuMUserConfigurationFile
  长名称: ''
  描述: |
    Reference to an external text file that will be included during generation to <Module>_Cfg.h.
    The content of the user configuration file will be added at the end of the generated module
    configuration file and allows altering or extending the generated code.
    
    Caution: User configuration files can cause the software module to malfunction and must only be
    used with great care!
    
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 8
  名称: EcuMDeferredBswMNotification
  长名称: Deferred BswM Notification
  描述: |
    Notification to the BswM via BswM_EcuM_CurrentWakeup is done immediate in the context of the
    EcuM API EcuM_SetWakeupEvent or EcuM_ValidateWakeupEvent. This APIs are often called in the
    context of an interrupt and the BswM notification will extend the interrupt runtime.
    
    If the value is True, the notification will be done deferred in the next EcuM_MainFunction.
    
    
    
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 9
  名称: EcuMSlaveCoreHandling
  长名称: ''
  描述: |
    This parameter indicates if in case of a MultiCore Ecu the MasterCore synchronizes with the
    slave cores in sleep and off modes. If synchronization is active the MasterCore waits on the way
    to ECUM_STATE_SLEEP and ECUM_STATE_OFF till the SlaveCores has entered their state.
    
    
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 10
  名称: EcuMEnableFixBehavior
  长名称: ''
  描述: |
    Enables or Disables the EcuM Fixed Behavior.
    
    The EcuM Fixed Behavior does automatically control ECU phases like Startup / Run / PostRun /
    Sleep or Off.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 11
  名称: EcuMBswCoreId
  长名称: ''
  描述: Specifies on which core the BSW shall run. This parameter is only relevant if more than one
      core is configured in the OS configuration.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 12
  名称: EcuMNonChannelWakeupInRun
  长名称: ''
  描述: |
    Allows wakeups for wakeup sources without referenced communication channel during the RUN phase.
    
    If this parameter is false, only wakeup sources with a communication channel refernce lead to a
    valid wakeup event.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 13
  名称: EcuMSchMStartInitialization
  长名称: SchM Start
  描述: |
    In case that this parameter is set, the EcuM uses the SchM and BswM initialization sequence
    SchM_Start(); SchM_Init(); BswM_Init(); SchM_StartTiming();
    which uses additional SchM init functions defined in ASR 4.3.0 but keeps the old order of
    execution of SchM_Init and BswM_Init
    
    If the parameter is false, the initialization sequence is
    SchM_Init(); BswM_Init();
    
    
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 14
  名称: EcuMSafeBswChecks
  长名称: ''
  描述: Selects if safety checks are used. These checks improve robustness as e.g. invalid parameters
      are checked before function is executed. This attribute has to be enabled for safety
      projects.
  默认值: false
  最小值: ''
  最大值: ''
```

### 33. EcuMGeneration

**描述**: Contains the generation configuration parameters of the module EcuM.

#### 参数列表

```yaml
- 
  序号: 1
  名称: EcuMOutOfBoundsWriteSanitizer
  长名称: ''
  描述: |
    This parameter activates/deactivates the generation of runtime checks which call a DET error
    notification function to find easily out of bounds write problems.
    
    FALSE:  no checks are generated in the data access.
    TRUE: the data access is enriched with DET checks to validate indexes.
    
    For more details, refer to TechnicalReference_ComStackLib.pdf
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: EcuMOutOfBoundsReadSanitizer
  长名称: ''
  描述: |
    This parameter activates/deactivates the generation of runtime checks which call a DET error
    notification function to find easily out of bounds read problems.
    
    FALSE:  no checks are generated in the data access.
    TRUE: the data access is enriched with DET checks to validate indexes.
    
    For more details, refer to TechnicalReference_ComStackLib.pdf
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: EcuMInterfacesForDeactivatedData
  长名称: ''
  描述: |
    This parameter activates/deactivates the capability to generate bsw data interfaces for
    deactivated data elements. This is an advantage for the BSW developer to reduce the time to
    market with a development environment using auto completition.
    
    FALSE: data interfaces are not generated if the data elementis deactivated.
    TRUE: data interfaces are generated as e.g. emty macros.
    
    For more details, refer to TechnicalReference_ComStackLib.pdf
  默认值: false
  最小值: ''
  最大值: ''
```

