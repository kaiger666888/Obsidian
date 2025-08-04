# WdgM

## 模块描述

Configuration of the WdgM (Watchdog Manager) module.

## 容器列表

### 1. WdgMConfigSet

**描述**: This container describes one of multiple configuration sets of WdgM.

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
      cycles for how long the blocking of watchdog triggering shall be postponed, AFTER THE
      GLOBAL SUPERVISION STATUS HAS REACHED THE STATE EXPIRED.
  默认值: ''
  最小值: 0
  最大值: 65535
- 
  序号: 2
  名称: WdgMModeId
  长名称: ''
  描述: This parameter fixes the identfier for the mode. This identifier is for instance passed as a
      parameter to the WdgM_SetMode service.
  默认值: ''
  最小值: 0
  最大值: 255
- 
  序号: 3
  名称: WdgMSupervisionCycle
  长名称: ''
  描述: This parameter defines the schedule period of the main function WdgM_MainFunction.
  默认值: ''
  最小值: 0
  最大值: Inf
```

### 4. WdgMAliveSupervision

**描述**: This container collects all configuration parameters of Alive-Supervision of one Checkpoint. Note
that each Checkpoint may have different parameters. For example, it may have different min and max
margin.

#### 参数列表

```yaml
- 
  序号: 1
  名称: WdgMExpectedAliveIndications
  长名称: ''
  描述: This parameter contains the amount of expected alive indications of the Checkpoint within the
      referenced amount of defined supervision cycles according to corresponding SE.
  默认值: ''
  最小值: 0
  最大值: 65535
- 
  序号: 2
  名称: WdgMMaxMargin
  长名称: ''
  描述: This parameter contains the amount of alive indications of the Checkpoint that are acceptable
      to be additional to the expected alive indications within the corresponding supervision
      reference cycle.
  默认值: ''
  最小值: 0
  最大值: 255
- 
  序号: 3
  名称: WdgMMinMargin
  长名称: ''
  描述: This parameter contains the amount of alive indications of the Checkpoint that are acceptable
      to be missed from the expected alive indications within the corresponding supervision
      reference cycle.
  默认值: ''
  最小值: 0
  最大值: 255
- 
  序号: 4
  名称: WdgMSupervisionReferenceCycle
  长名称: ''
  描述: This parameter shall contain the amount of supervision cycles to be used as reference by the
      alive-supervision mechanism to perform the checkup with counted alive indications
      according to corresponding SE.
  默认值: ''
  最小值: 1
  最大值: 65535
```

### 5. WdgMDeadlineSupervision

**描述**: This container collects all configuration parameters for Deadline Supervision for a Supervised
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
  最小值: 0
  最大值: Inf
- 
  序号: 2
  名称: WdgMDeadlineMin
  长名称: ''
  描述: This parameter contains the shortest time span after which the deadline is considered to be
      met.
  默认值: ''
  最小值: 0
  最大值: Inf
```

### 6. WdgMExternalLogicalSupervision

**描述**: This container collects all configuration parameters for Logical Supervision for one external graph.

该容器没有参数。

### 7. WdgMExternalTransition

**描述**: This container collects the Checkpoints for an External Transition across Supervised Entities.

该容器没有参数。

### 8. WdgMLocalStatusParams

**描述**: This container collects all configuration parameters for the Local Status of a Supervised Entity.

#### 参数列表

```yaml
- 
  序号: 1
  名称: WdgMFailedAliveSupervisionRefCycleTol
  长名称: ''
  描述: This parameter shall contain the acceptable amount of reference cycles with incorrect/failed
      alive supervisions for this Supervised Entity.
  默认值: ''
  最小值: 0
  最大值: 255
```

### 9. WdgMTrigger

**描述**: This container collects all configuration parameters for the triggering of hardware watchdogs.

#### 参数列表

```yaml
- 
  序号: 1
  名称: WdgMTriggerConditionValue
  长名称: ''
  描述: This parameter shall contain the value that is passed to WdgIf_SetTriggerCondition for this
      watchdog.
  默认值: ''
  最小值: 1
  最大值: 65535
- 
  序号: 2
  名称: WdgMWatchdogMode
  长名称: ''
  描述: This parameter contains the watchdog mode that shall be used for the referenced watchdog in
      this Watchdog Manager mode.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 10. WdgMGeneral

**描述**: Container defines all general configuration parameters of the Watchdog Manager.

#### 参数列表

```yaml
- 
  序号: 1
  名称: WdgMDefensiveBehavior
  长名称: ''
  描述: Preprocessor switch to enable/disable the defensive behavior of the Watchdog Manager module.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: WdgMDemStoppedSupervisionReport
  长名称: ''
  描述: Parameter to enable/disable the error reporting to DEM.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: WdgMDevErrorDetect
  长名称: ''
  描述: Preprocessor switch to enable/disable development error detection and reporting.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: WdgMImmediateReset
  长名称: ''
  描述: This parameter enables/disablse the immediate reset feature in case of alive-supervision
      failure.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: WdgMOffModeEnabled
  长名称: ''
  描述: This parameter enables/disables the selection of the "OffMode" of the watchdog driver.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: WdgMVersionInfoApi
  长名称: ''
  描述: Preprocessor switch to enable/disable the existence of the API WdgM_GetVersionInfo. Shall be
      used to remove unneeded code segments.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 11. WdgMCallerIds

**描述**: Contains the definition of valid CallerIds for the callers who have permission to call the function
WdgM_SetMode.

#### 参数列表

```yaml
- 
  序号: 1
  名称: WdgMCallerId
  长名称: ''
  描述: This parameter defines one valid CallerId for the callers who have permission to call the
      function WdgM_SetMode.
  默认值: ''
  最小值: 0
  最大值: 65535
```

### 12. WdgMSupervisedEntity

**描述**: This container collects all common (mode-independent) parameters of a Supervised Entity to be
supervised by the Watchdog Manager.

#### 参数列表

```yaml
- 
  序号: 1
  名称: WdgMSupervisedEntityId
  长名称: ''
  描述: This parameter shall contain the unique identifier of the supervised entity.
  默认值: ''
  最小值: 0
  最大值: 65535
```

### 13. WdgMCheckpoint

**描述**: This container collects all Checkpoints of this Supervised Entity. Each Supervised Entity has at
least one Checkpoint.

#### 参数列表

```yaml
- 
  序号: 1
  名称: WdgMCheckpointId
  长名称: ''
  描述: This parameter shall contain the unique identifier of Checkpoint.
  默认值: ''
  最小值: 0
  最大值: 65535
```

### 14. WdgMInternalTransition

**描述**: This container defines the graph of Internal Transitions within this Supervised Entity.

该容器没有参数。

### 15. WdgMWatchdog

**描述**: This container collects all common (mode-independent) parameters of a Watchdog to be triggered by
the Watchdog Manager.

#### 参数列表

```yaml
- 
  序号: 1
  名称: WdgMWatchdogName
  长名称: ''
  描述: This parameter shall contain the symbolic name of the watchdog instance.
  默认值: ''
  最小值: ''
  最大值: ''
```

