# Rte

## 模块描述

Configuration of the Rte (Runtime Environment) module.

## 容器列表

### 1. RteBswGeneral

**描述**: General configuration parameters of the Bsw Scheduler section.

#### 参数列表

```yaml
- 
  序号: 1
  名称: RteSchMVersionInfoApi
  长名称: ''
  描述: Enables the generation of the SchM_GetVersionInfo() API.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: RteUseComShadowSignalApi
  长名称: ''
  描述: This parameter defines whether the ComShadowSignalAPIs ((Com_UpdateShadowSignal,
      Com_InvalidateShadowSignal, Com_ReceiveShadowSignal) are used or not.
  默认值: false
  最小值: ''
  最大值: ''
```

### 2. RteBswModuleInstance

**描述**: Represents one instance of a Bsw-Module configured on one ECU.

该容器没有参数。

### 3. RteBswEventToTaskMapping

**描述**: Maps a BswSchedulableEntity onto one OsTask based on the activating BswEvent.

#### 参数列表

```yaml
- 
  序号: 1
  名称: RteBswActivationOffset
  长名称: ''
  描述: Activation offset in seconds.
  默认值: ''
  最小值: 0
  最大值: Inf
- 
  序号: 2
  名称: RteBswImmediateRestart
  长名称: ''
  描述: When RteBswImmediateRestart is set to true the BswSchedulableEntitiy shall be immediately
      re-started after termination if it was activated by this BswEvent while it was already
      started.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: RteBswPositionInTask
  长名称: ''
  描述: Each BswSchedulableEntity activation mapped to an OsTask has a specific position within the
      task execution.
  默认值: ''
  最小值: 0
  最大值: 65535
- 
  序号: 4
  名称: RteOsSchedulePoint
  长名称: ''
  描述: Introduce a schedule point by explicitly calling Os Schedule service after the execution of
      the ExecutableEntity.  The Rte generator is allowed to optimize several consecutive
      calls to Os schedule into one single call if the ExecutableEntity executions in between
      have been skipped.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 4. RteBswExclusiveAreaImpl

**描述**: Represents one ExclusiveArea of one BswImplementation. Used to specify the implementation means of
this ExclusiveArea.

#### 参数列表

```yaml
- 
  序号: 1
  名称: RteExclusiveAreaImplMechanism
  长名称: ''
  描述: To be used implementation mechanism for the specified ExclusiveArea.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 5. RteBswExternalTriggerConfig

**描述**: Defines the configuration of Inter Basic Software Module Entity Triggering

#### 参数列表

```yaml
- 
  序号: 1
  名称: RteBswTriggerSourceQueueLength
  长名称: ''
  描述: Length of trigger queue on the trigger source side.
  默认值: 0
  最小值: 0
  最大值: 4294967295
```

### 6. RteBswInternalTriggerConfig

**描述**: Defines the configuration of internal Basic Software Module Entity Triggering

#### 参数列表

```yaml
- 
  序号: 1
  名称: RteBswTriggerSourceQueueLength
  长名称: ''
  描述: Length of trigger queue on the trigger source side.
  默认值: 0
  最小值: 0
  最大值: 4294967295
```

### 7. RteBswRequiredModeGroupConnection

**描述**: Defines the connection between one requiredModeGroup of this BSW Module instance and one
providedModeGroup instance.

该容器没有参数。

### 8. RteBswRequiredTriggerConnection

**描述**: Defines the connection between one requiredTrigger of this BSW Module instance and one
releasedTrigger instance.

该容器没有参数。

### 9. RteGeneration

**描述**: This container holds the parameters for the configuration of the RTE Generation.

#### 参数列表

```yaml
- 
  序号: 1
  名称: RteCalibrationSupport
  长名称: ''
  描述: The RTE generator shall have the option to switch off support for calibration for generated
      RTE code. This option shall influence complete RTE code at once.
  默认值: NONE
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: RteCodeVendorId
  长名称: ''
  描述: Holds the vendor ID of the generated Rte code.
  默认值: ''
  最小值: 0
  最大值: 65535
- 
  序号: 3
  名称: RteDevErrorDetect
  长名称: ''
  描述: The Rte shall log development errors to the Det module.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: RteDevErrorDetectUninit
  长名称: ''
  描述: The Rte shall detect if it is started when its APIs are called, and the BSW Scheduler shall
      check if it is initialized when its APIs are called.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: RteGenerationMode
  长名称: ''
  描述: Switch between the two available generation modes of the RTE generator.
  默认值: COMPATIBILITY_MODE
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: RteIocInteractionReturnValue
  长名称: ''
  描述: Defines whether the return value of RTE APIs is based on RTE-IOC interaction or RTE-COM
      interaction.
  默认值: RTE_IOC
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: RteMeasurementSupport
  长名称: ''
  描述: The RTE generator shall have the option to switch off support for measurement for generated
      RTE code. This option shall influence complete RTE code at once.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 8
  名称: RteOptimizationMode
  长名称: ''
  描述: Switch between the two available optimization modes of the RTE generator.
  默认值: RUNTIME
  最小值: ''
  最大值: ''
- 
  序号: 9
  名称: RteToolChainSignificantCharacters
  长名称: ''
  描述: If present, the RTE generator shall provide the list of C RTE identifiers whose name is not
      unique when only the first RteToolChainSignificantCharacters characters are considered.
  默认值: 31
  最小值: 0
  最大值: 65535
- 
  序号: 10
  名称: RteValueRangeCheckEnabled
  长名称: ''
  描述: If set to true the RTE generator shall enable the value range checking for the specified
      VariableDataPrototypes.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 11
  名称: RteVfbTraceClientPrefix
  长名称: ''
  描述: Defines an additional prefix for all VFB trace functions to be generated. With this approach
      it is possible to have debugging and DLT trace functions at the same time.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 12
  名称: RteVfbTraceEnabled
  长名称: ''
  描述: The RTE generator shall globally enable VFB tracing when RteVfbTrace is set to "true".
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 13
  名称: RteVfbTraceFunction
  长名称: ''
  描述: The RTE generator shall enable VFB tracing for a given hook function when there is a #define
      in the RTE configuration header file for the hook function name and tracing is globally
      enabled.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 10. RteImplicitCommunication

**描述**: Configuration of the Implicit Communication behavior to be generated.

#### 参数列表

```yaml
- 
  序号: 1
  名称: RteCoherentAccess
  长名称: ''
  描述: If set to true the referenced VariableAccess'es of this RteImplicitCommunication container are
      in one CoherencyGroup.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: RteImmediateBufferUpdate
  长名称: ''
  描述: If set to true the RTE will perform preemption area specific buffer update immediately before
      (for VariableAccess in the role dataReadAccess) resp. after (for VariableAccess in the
      role dataWriteAccess) Runnable execution.
  默认值: false
  最小值: ''
  最大值: ''
```

### 11. RteInitializationBehavior

**描述**: Specifies the initialization strategy for variables allocated by RTE with the purpose to implement
VariableDataPrototypes.

#### 参数列表

```yaml
- 
  序号: 1
  名称: RteInitializationStrategy
  长名称: ''
  描述: Definition of the initialization strategy applicable for the SectionInitializationPolicys
      selected by RteSectionInitializationPolicy.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: RteSectionInitializationPolicy
  长名称: ''
  描述: This parameter describes the SectionInitializationPolicys for which a particular RTE
      initialization strategy applies.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 12. RteOsInteraction

**描述**: Interaction of the Rte with the Os.

该容器没有参数。

### 13. RteModeToScheduleTableMapping

**描述**: Provides configuration input in which Modes of a ModeDeclarionGroupPrototype of a Mode Manager a
OsScheudleTable shall be active.

该容器没有参数。

### 14. RteModeSchtblMapBsw

**描述**: Specifies an instance of a ModeDeclarationGroupPrototype of a Bsw-Module.

该容器没有参数。

### 15. RteModeSchtblMapSwc

**描述**: Specifies an instance of a ModeDeclarationGroupPrototype of a SwComponentPrototype.

该容器没有参数。

### 16. RteUsedOsActivation

**描述**: Attributes used in the activation of OsTasks and Runnable Entities.

#### 参数列表

```yaml
- 
  序号: 1
  名称: RteExpectedActivationOffset
  长名称: ''
  描述: Activation offset in seconds.
  默认值: ''
  最小值: 0
  最大值: Inf
- 
  序号: 2
  名称: RteExpectedTickDuration
  长名称: ''
  描述: The expected tick duration in seconds which shall be configured to drive the OsScheduleTables
      or OsAlarm.
  默认值: ''
  最小值: 0
  最大值: Inf
```

### 17. RtePostBuildVariantConfiguration

**描述**: Specifies the PostbuildVariantSets for each of the PostBuild configurations of the RTE.

该容器没有参数。

### 18. RteSwComponentInstance

**描述**: Representation of one SwComponentPrototype located on the to be configured ECU. All subcontainer
configuration aspects are in relation to this SwComponentPrototype.

该容器没有参数。

### 19. RteEventToTaskMapping

**描述**: Maps a RunnableEntity onto one OsTask based on the activating RTEEvent.

#### 参数列表

```yaml
- 
  序号: 1
  名称: RteActivationOffset
  长名称: ''
  描述: Activation offset in seconds.
  默认值: ''
  最小值: 0
  最大值: Inf
- 
  序号: 2
  名称: RteImmediateRestart
  长名称: ''
  描述: When RteImmediateRestart is set to true the RunnableEntitiy shall be immediately re-started
      after termination if it was activated by this RTEEvent while it was already started.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: RteOsSchedulePoint
  长名称: ''
  描述: Introduce a schedule point by explicitly calling Os Schedule service after the execution of
      the ExecutableEntity.  The Rte generator is allowed to optimize several consecutive
      calls to Os schedule into one single call if the ExecutableEntity executions in between
      have been skipped.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: RtePositionInTask
  长名称: ''
  描述: Each RunnableEntity mapped to an OsTask has a specific position within the task execution.
  默认值: ''
  最小值: 0
  最大值: 65535
```

### 20. RteExclusiveAreaImplementation

**描述**: Specifies the implementation to be used for the data consistency of this ExclusiveArea.

#### 参数列表

```yaml
- 
  序号: 1
  名称: RteExclusiveAreaImplMechanism
  长名称: ''
  描述: To be used implementation mechanism for the specified ExclusiveArea.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 21. RteExternalTriggerConfig

**描述**: Defines the configuration of External Trigger Event Communication for Software Components

#### 参数列表

```yaml
- 
  序号: 1
  名称: RteTriggerSourceQueueLength
  长名称: ''
  描述: Length of trigger queue on the trigger source side.
  默认值: 0
  最小值: 0
  最大值: 4294967295
```

### 22. RteInternalTriggerConfig

**描述**: Defines the configuration of Inter Runnable Triggering for Software Components

#### 参数列表

```yaml
- 
  序号: 1
  名称: RteTriggerSourceQueueLength
  长名称: ''
  描述: Length of trigger queue on the trigger source side.
  默认值: 0
  最小值: 0
  最大值: 4294967295
```

### 23. RteNvRamAllocation

**描述**: Specifies the relationship between the AtomicSwComponentType's NVRAMMapping / NVRAM needs and the
NvM module configuration.

#### 参数列表

```yaml
- 
  序号: 1
  名称: RteNvmRamBlockLocationSymbol
  长名称: ''
  描述: This is the name of the linker object name where the NVRam Block will be mirrored by the Nvm.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: RteNvmRomBlockLocationSymbol
  长名称: ''
  描述: This is the name of the linker object name where the NVRom Block will be accessed by the Nvm.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 24. RteSwComponentType

**描述**: Representation of one SwComponentType for the base of all configuration parameter which are
affecting the whole type and not a specific instance.

该容器没有参数。

### 25. RteComponentTypeCalibration

**描述**: Specifies for each ParameterSwComponentType or AtomicSwComponentType whether calibration is enabled.

#### 参数列表

```yaml
- 
  序号: 1
  名称: RteCalibrationSupportEnabled
  长名称: ''
  描述: Enables calibration support for the specified ParameterSwComponentType or
      AtomicSwComponentType.
  默认值: ''
  最小值: ''
  最大值: ''
```

