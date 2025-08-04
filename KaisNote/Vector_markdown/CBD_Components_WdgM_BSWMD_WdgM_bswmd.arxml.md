# WdgM

## 模块描述

Watchdog Manager. The manager supervises the program execution abstracting from the triggering of
hardware watchdog entities (Supervised Entities).
When it detects a violation of the configured temporal and/ or logical constraints on program
execution, it takes a number of configurable actions to recover from this failure.

#Safety #Supervision
#AUTOSAR #ServiceComponent

## 容器列表

### 1. WdgMConfigSet

**描述**: This container describes one of multiple configuration sets of WdgM.

This is a MultipleConfigurationContainer, i.e. this container and its sub-containers exist once per
configuration set.

该容器没有参数。

### 2. WdgMDemEventParameterRefs

**描述**: Container for the references to DemEventParameter elements which shall be invoked using the API
Dem_ReportErrorStatus API in case the corresponding error occurs. The EventId is taken from the
referenced DemEventParameter's DemEventId value. The standardized errors are provided in the
container and can be extended by vendor specific error references.

该容器没有参数。

### 3. WdgMMode

**描述**: The container describes one of several modes of the Watchdog Manager.

#### 参数列表

```yaml
- 
  序号: 1
  名称: WdgMExpiredSupervisionCycleTol
  长名称: ''
  描述: This parameter shall be used to define a value that fixes the amount of expired supervision
      cycles for how long the blocking of watchdog triggering shall be postponed.
  默认值: ''
  最小值: 0
  最大值: 65535
- 
  序号: 2
  名称: WdgMModeId
  长名称: ''
  描述: This parameter represents the WdgM mode. 
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 3
  名称: WdgMSupervisionCycle
  长名称: ''
  描述: This parameter defines the period with which the main function (WdgM_MainFunction) is called.
  默认值: ''
  最小值: 0
  最大值: 1.7976931348623157E+308
- 
  序号: 4
  名称: WdgMInitialTriggerModeId
  长名称: ''
  描述: Denotes the ID of the Trigger Mode which shall be used at system start. 
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 5
  名称: WdgMModeCoreAssignment
  长名称: ''
  描述: This value specifies the assignment of configuration mode to a processor core ID. Maximal 10
      cores are able to be used.
  默认值: 0
  最小值: 0
  最大值: 9
- 
  序号: 6
  名称: WdgMGlobalStateChangeCbk
  长名称: ''
  描述: |
    Callback function for notifying Watchdog Manager global status change.
    
    Note:
    - This parameter can only be used if WdgMStatusReportingMechanism is set to
    WDGM_USE_NOTIFICATIONS.
    - This parameter can only be used if parameter WdgMReportStatusViaRte of this WdgMMode is set
    false
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: WdgMTicksPerSecond
  长名称: ''
  描述: This parameter defines the number of Watchdog Manager ticks per second.
  默认值: ''
  最小值: 0
  最大值: 4294967295
- 
  序号: 8
  名称: WdgMReportStatusViaRte
  长名称: ''
  描述: |
    This parameter is used to enable the status reporting via Rte.
    
    Notes:
    - This parameter can only be set true if WdgMStatusReportingMechanism is _not_
    WDGM_USE_NO_STATUS_REPORTING
    - If this parameter is set true in any of the supervised entities or in WdgMMode, the global
    switch WdgMUseRte has to be set true, too.
    - This parameter cannot be set true if global switch WdgMUseRte is set false.
    - If this parameter is set true, the optional parameter WdgMGlobalStateChangeCbk must not exist.
  默认值: true
  最小值: ''
  最大值: ''
```

### 4. WdgMAliveSupervision

**描述**: This container collects all configuration parameters of Alive-Supervision.

#### 参数列表

```yaml
- 
  序号: 1
  名称: WdgMExpectedAliveIndications
  长名称: ''
  描述: This parameter contains the amount of expected alive indications within the referenced amount
      of defined supervision cycles according to corresponding SE.
  默认值: ''
  最小值: 0
  最大值: 65535
- 
  序号: 2
  名称: WdgMMaxMargin
  长名称: ''
  描述: This parameter contains the amount of alive indications that are acceptable to be additional
      on the expected alive indications within the corresponding supervision reference cycle.
  默认值: ''
  最小值: 0
  最大值: 65535
- 
  序号: 3
  名称: WdgMMinMargin
  长名称: ''
  描述: This parameter contains the amount of alive indications that are acceptable to be missed from
      the expected alive indications within the corresponding supervision reference cycle.
  默认值: ''
  最小值: 0
  最大值: 65535
- 
  序号: 4
  名称: WdgMSupervisionReferenceCycle
  长名称: ''
  描述: This parameter contains the amount of supervision cycles to be used as reference by the
      alive-supervision mechanism to perform the checkup with counted alive indications
      according to corresponding SE.
  默认值: ''
  最小值: 1
  最大值: 65535
```

### 5. WdgMDeadlineSupervision

**描述**: This container collects all configuration parameters for Deadline Monitoring for a Supervised
Entity.

#### 参数列表

```yaml
- 
  序号: 1
  名称: WdgMDeadlineMax
  长名称: ''
  描述: This parameter contains the longest time span after which the deadline is considered to be
      met.
  默认值: ''
  最小值: 0.0
  最大值: 1.7976931348623157E+308
- 
  序号: 2
  名称: WdgMDeadlineMin
  长名称: ''
  描述: This parameter contains the shortest time span after which the deadline is considered to be
      met.
  默认值: ''
  最小值: 0.0
  最大值: 1.7976931348623157E+308
```

### 6. WdgMExternalLogicalSupervision

**描述**: This container collects all configuration parameters for Logical Supervision for one external graph.

该容器没有参数。

### 7. WdgMExternalTransition

**描述**: This container collects the Checkpoints for a Global Transition across Supervised Entities.

该容器没有参数。

### 8. WdgMTrigger

**描述**: This container collects all configuration parameters for the triggering of hardware watchdogs.

#### 参数列表

```yaml
- 
  序号: 1
  名称: WdgMWatchdogMode
  长名称: ''
  描述: |
    This parameter contains the watchdog mode that shall be used for the referenced watchdog in this
    Watchdog Manager mode.
    
    Implementation Type: WdgIf_ModeType
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: WdgMTriggerConditionValue
  长名称: ''
  描述: This parameter defines the maximum possible trigger time where the watchdog trigger is
      accepted. The consumer of this parameter is the WdgIf_SetTriggerCondition for the
      corresponding watchdog.
  默认值: ''
  最小值: 1
  最大值: 65535
- 
  序号: 3
  名称: WdgMTriggerModeId
  长名称: ''
  描述: This parameter contains a unique identifier of the trigger mode.
  默认值: 0
  最小值: 0
  最大值: 254
```

### 9. WdgMLocalStatusParams

**描述**: This container collects all configuration parameters for the Local Status of a Supervised Entity.

#### 参数列表

```yaml
- 
  序号: 1
  名称: WdgMFailedAliveSupervisionRefCycleTol
  长名称: ''
  描述: This parameter contains the acceptable amount of failed alive supervisions for this Supervised
      Entity
  默认值: ''
  最小值: 0
  最大值: 65534
- 
  序号: 2
  名称: WdgMSupervisedEntityInitialMode
  长名称: ''
  描述: Initial local monitoring status of the supervised entity.
  默认值: WDGM_LOCAL_STATUS_OK
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: WdgMFailedDeadlineRefCycleTol
  长名称: ''
  描述: |
    This parameter contains the acceptable amount of violated deadlines for this Supervised Entity.
    
    Note:
    The AUTOSAR implementation can be simulated for deadline violations with:
    WdgMDeadlineReferenceCycle = WdgMFailedDeadlineRefCycleTol = 0
  默认值: 0
  最小值: 0
  最大值: 65534
- 
  序号: 4
  名称: WdgMDeadlineReferenceCycle
  长名称: ''
  描述: |
    This parameter contains the amount of supervision cycles to be used as reference by the deadline
    supervisions of this SE.
    
    Note:
    The AUTOSAR implementation can be simulated for deadline violations with:
    WdgMDeadlineReferenceCycle = WdgMFailedDeadlineRefCycleTol = 0
  默认值: 0
  最小值: 0
  最大值: 65535
- 
  序号: 5
  名称: WdgMFailedProgramFlowRefCycleTol
  长名称: ''
  描述: |
    This parameter contains the acceptable amount of program flow violations for this Supervised
    Entity.
    
    Note:
    The AUTOSAR implementation can be simulated for program flow violations with:
    WdgMProgramFlowReferenceCycle = WdgMFailedProgramFlowRefCycleTol = 0
  默认值: 0
  最小值: 0
  最大值: 65534
- 
  序号: 6
  名称: WdgMProgramFlowReferenceCycle
  长名称: ''
  描述: |
    This parameter contains the amount of supervision cycles to be used as reference by the program
    flow supervisions of this SE.
    
    Note:
    The AUTOSAR implementation can be simulated for program flow violations with:
    WdgMProgramFlowReferenceCycle = WdgMFailedProgramFlowRefCycleTol = 0
  默认值: 0
  最小值: 0
  最大值: 65535
```

### 10. WdgMGeneral

**描述**: Container structures all general configuration parameters of the Watchdog Manager.

#### 参数列表

```yaml
- 
  序号: 1
  名称: WdgMDevErrorDetect
  长名称: ''
  描述: |
    Preprocessor switch to enable/disable development error detection and reporting.
    Shall be used to remove unneeded code segments regarding DET features
    
    True: Development error detection is enabled
    False: Development error detection is disabled
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: WdgMDemReport
  长名称: ''
  描述: |
    Preprocessor switch to enable / disable calls to DEM in case of production error detection.
    
    True: DEM calls enabled in case of production errors
    False: DEM calls disabled in case of production errors
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: WdgMImmediateReset
  长名称: ''
  描述: |
    This preprocessor switch enables/disablse the immediate reset feature in case of alive, deadline
    or program flow failure.
    
    True: Immediate reset is enabled
    False: Immediate reset is disabled
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: WdgMOffModeEnabled
  长名称: ''
  描述: |
    This preprocessor switch enables/disables the selection of the "OffMode" of the watchdog driver.
    
    True: "OffMode" selection is allowed
    False: "OffMode" selection is disallowed
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: WdgMVersionInfoApi
  长名称: ''
  描述: |
    Preprocessor switch to enable/disable the existence of the API WdgM_GetVersionInfo. Shall be
    used to remove unneeded code segments.
    
    True: API is enabled
    False: API is disabled
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: WdgMDefensiveBehavior
  长名称: ''
  描述: Preprocessor switch to enable/disable the defensive behavior of the Watchdog Manager module.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: WdgMUseRte
  长名称: ''
  描述: |
    This preprocessor switch instructs the Watchdog Manager to use the by Rte generated defines and
    typedefs.
    
    True: the WdgM uses the by Rte generated defines and typedefs
    False: the WdgM uses own defines and typedefs
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 8
  名称: WdgMDemSupervisionReport
  长名称: ''
  描述: |
    Preprocessor switch to enable / disable call to DEM in case the Safe Watchdog Manager has the
    WDGM_GLOBAL_STATE_STOPPED reached.
    
    True: The DEM call is enabled
    False: The DEM call is disabled
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 9
  名称: WdgMFirstCycleAliveCounterReset
  长名称: ''
  描述: |
    When this preprocessor switch is enabled, then the Alive counters in the first Supervision cycle
    are not evaluated
    
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 10
  名称: WdgMAutosarDebugging
  长名称: ''
  描述: |
    Preprocessor switch to enable/disable the compilation of AUTOSAR debugging features, such as
    WdgM_GetFirstExpiredSEViolation.
    
    True: AUTOSAR debugging is enabled
    False: AUTOSAR debugging is disabled
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 11
  名称: WdgMUseOsSuspendInterrupt
  长名称: ''
  描述: |
    This preprocessor switch enables/disables the usage of OS suspend and resume interrupt services
    within WdgM.
    
    Note: Suspending and Resuming interrupts is done by SchM. Therefore, if this option is enabled,
    SchM_WdgM.h is included and not Os.h. Normally SchM_WdgM.h is generated by Rte. If so, also
    enable the parameter / option WdgMUseRte.
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 12
  名称: WdgMTimebaseSource
  长名称: ''
  描述: |
    This parameter selects the Tick counter source for Deadline monitoring.
    
    WDGM_INTERNAL_SOFTWARE_TICK: The counter is incremented each time `WdgM_MainFunction` is called.
    WDGM_OS_COUNTER_TICK: The timebase is based on the Os hardware counter.
    WDGM_EXTERNAL_TICK: The counter is incremented each time `WdgM_UpdateTickCount` is called.
    
  默认值: WDGM_INTERNAL_SOFTWARE_TICK
  最小值: ''
  最大值: ''
- 
  序号: 13
  名称: WdgMSecondResetPath
  长名称: ''
  描述: This preprocessor switch generally enables the access to the external Mcu_PerformReset()
      function. This function  is used as second reset path a specially when the primary reset
      path signals failure.
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 14
  名称: WdgMTickOverrunCorrection
  长名称: ''
  描述: This preprocessor switch enables/disables 32 bit timebase counter overflow detection and
      correction in case of WdgMTimebaseSource is selected to be WDGM_EXTERNAL_TICK.
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 15
  名称: WdgMEntityDeactivationEnabled
  长名称: ''
  描述: This preprocessor switch enables generally entity deactivation. Please see additional
      important safety information regarding this functionality in the WdgM Safety Manual.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 16
  名称: WdgMUseOsCoreIdentification
  长名称: ''
  描述: This preprocessor switch enables/disables the usage of the OS GetCoreID() service.
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 17
  名称: WdgMGenerateCPIdAsPortDefinedArgument
  长名称: ''
  描述: |
    This preprocessor switch enables/disables the generation of a port per checkpoint where the
    checkpoint id is added as port-defined argument.
    
    True: A port is generated in the software component (swc) for each checkpoint of a supervised
    entity with both supervised entity id and checkpoint id as port-defined arguments
    False: A port is generated in the software component (swc) only for each supervised entity with
    the supervised entity id as port-defined argument. The checkpoint id has to be added in the
    function call manually.
    
    Note: To obtain AUTOSAR behavior this parameter has to be set to false.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 18
  名称: WdgMStatusReportingMechanism
  长名称: ''
  描述: |
    This parameter selects which mechansim should be applied for status reporting.
    
    WDGM_USE_MODE_SWITCH_PORTS: ModeSwitchPorts are used to report a status change.
    WDGM_USE_NOTIFICATIONS: Notifications are used to report a status change.
    WDGM_USE_NO_STATUS_REPORTING: No reporting mechanism of a status change is used.
  默认值: WDGM_USE_MODE_SWITCH_PORTS
  最小值: ''
  最大值: ''
- 
  序号: 19
  名称: WdgMNotifyDetectedViolations
  长名称: ''
  描述: |
    This parameter enables or disables if the WdgM shall notify each detected Violation.
    
    If enabled, the integration code must implement the callout function
    'WdgM_NotifyDetectedViolations' defined within WdgM_Cfg.h
  默认值: false
  最小值: ''
  最大值: ''
```

### 11. WdgMSupervisedEntity

**描述**: This container collects all common (mode-independent) parameters of a Supervised Entity to be
supervised by the Watchdog Manager.

#### 参数列表

```yaml
- 
  序号: 1
  名称: WdgMSupervisedEntityId
  长名称: ''
  描述: |
    This parameter shall contain the unique identifier of the supervised entity.
    
    All supervised entity ids must form a zero-based list of integers.
  默认值: 65535
  最小值: 0
  最大值: 65535
- 
  序号: 2
  名称: WdgMEnableEntityDeactivation
  长名称: ''
  描述: Enables deactivation of this supervised enitiy.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: WdgMLocalStateChangeCbk
  长名称: ''
  描述: |
    Callback function for notifying the supervised entity's status change.
    
    Note:
    - This parameter can only be used if WdgMStatusReportingMechanism is set to
    WDGM_USE_NOTIFICATIONS.
    - This parameter can only be used if parameter WdgMReportStatusViaRte of this supervised entity
    is set false
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: WdgMReportStatusViaRte
  长名称: ''
  描述: |
    This parameter is used to enable the status reporting via Rte.
    
    Notes:
    - This parameter can only be set true if WdgMStatusReportingMechanism is _not_
    WDGM_USE_NO_STATUS_REPORTING
    - If this parameter is set true in any of the supervised entities or in WdgMMode, the global
    switch WdgMUseRte has to be set true, too.
    - This parameter cannot be set true if global switch WdgMUseRte is set false.
    - If this parameter is set true, the optional parameter WdgMLocalStateChangeCbk must not exist.
  默认值: true
  最小值: ''
  最大值: ''
```

### 12. WdgMCheckpoint

**描述**: This container collects all Checkpoints of this Supervised Entity.

#### 参数列表

```yaml
- 
  序号: 1
  名称: WdgMCheckpointId
  长名称: ''
  描述: |
    This parameter shall contain the unique identifier of checkpoint within a supervised entity.
    
    All checkpoint ids must form a zero-based list of integers.
  默认值: 65535
  最小值: 0
  最大值: 65535
```

### 13. WdgMInternalTransition

**描述**: This container defines the graph of Internal Transitions within this Supervised Entity.

该容器没有参数。

### 14. WdgMWatchdog

**描述**: This container collects all common (mode-independent) parameters of a Watchdog to be triggered by
the Watchdog Manager.

#### 参数列表

```yaml
- 
  序号: 1
  名称: WdgMWatchdogName
  长名称: ''
  描述: This parameter is a symbolic name of the Watchdog. Is used as comment only.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 15. WdgMCallerIds

**描述**: Contains the definition of valid CallerIds for the callers who have permission to call the function
WdgM_SetMode


#### 参数列表

```yaml
- 
  序号: 1
  名称: WdgMCallerId
  长名称: ''
  描述: |
    This parameter defines one valid CallerId for the callers who have permission to
     call the function WdgM_SetMode.
    
  默认值: 0
  最小值: 0
  最大值: 65535
```

