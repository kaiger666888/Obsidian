# Rte

## 模块描述

Runtime Environment (RTE). Scalable and highly optimized. Manages communication between the software
components (SWC), assures consistency of the overall information flow and represents the interface
between the functional software, basic software (BSW) and complex drivers (CDD).  Includes the SchM
(Schedule Manager) functionality.
#SWC #Scheduling #TaskMapping #RuntimeEnvironment
#AUTOSAR

## 容器列表

### 1. RteBswGeneral

**描述**: General configuration parameters of the Bsw Scheduler section.

#### 参数列表

```yaml
- 
  序号: 1
  名称: RteSchMVersionInfoApi
  长名称: SchM Version Info Api
  描述: Enables the generation of the SchM_GetVersionInfo() API.
  默认值: false
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
  描述: Activation offset.
  默认值: ''
  最小值: 0
  最大值: ''
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
  默认值: NONE
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: RteCyclicTriggerImplementation
  长名称: ''
  描述: |
    If set to 'Auto' the RTE generator automatically creates the necessary OS alarm to realize the
    cyclic trigger with the configured activation offset.
    If set to 'None' the trigger is not implemented by the RTE generator. It has to be implemented
    by the user either by configuring an appropriate OS alarm or an OS schedule table.
    The OS task and optional the OS event for that trigger can be found in the generated RTE report.
    
  默认值: Auto
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
  默认值: ALL_INTERRUPT_BLOCKING
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: RteExclusiveAreaOptimization
  长名称: ''
  描述: This parameter is not yet supported by the RTE generator. Changing the value has no impact on
      the generated code.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: RteExclusiveAreaGenerateFunction
  长名称: ''
  描述: |
    If set to false/undefined, the BSW Module ImplementationCodeType is used to determine the
    implementation if possible. If the BSW Module ImplementationCodeType is set to EcuCSourceCode,
    the following limitations apply: the RTE generator generates a function if the BSW Module is
    Postbuild loadable, or if the implementation mechanism is set to custom. Otherwise, a macro is
    generated.
    
    This parameter forces the RTE generator to generate a function for the ExclusiveArea interface
    implementation (disabling the RTE generator macro optimization).
  默认值: false
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

### 9. RteExclusiveAccessOptimization

**描述**: Configuration of the optimized access behavior to be generated. In other words, access shall be
mutually exclusive. How this is realized e.g. non preemptive task mapping, exclusive areas, mode
management, exclusive access during ECU startup and shutdown or scheduling in exclusive time slots
is up to the ECU integrator.

该容器没有参数。

### 10. RteGeneration

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
  默认值: 30
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
- 
  序号: 14
  名称: RteA2LVersion
  长名称: A2L Version
  描述: |
    When measurement is enabled, the RTE generator generates an A2L file that contains the
    measurement and characteristic objects of the generated RTE.
    This parameter specifies the ASAM MCD-2MC standard to which the A2L file is compliant.
    Version 1.6.0 supports additional features like linker map references for the measurement
    objects.
  默认值: V160
  最小值: ''
  最大值: ''
- 
  序号: 15
  名称: RteXcpEventSupport
  长名称: ''
  描述: |
    If set to true, the RTE generator uses the Xcp driver to send Xcp Events when the runnables of a
    task were processed. These events can be used to trigger the measurement of variables in a
    measurement and calibration tool.
    This also allows the measurement of sender / receiver ports when implicit inter-ECU
    communication is used.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 16
  名称: RteCalibrationBufferSize
  长名称: ''
  描述: |
    This parameter specifies the size of the RAM buffer for the calibration, if single-pointered or
    double-pointered online calibration is used.
    If set to 0, the RTE generator won't generate a RAM buffer.
  默认值: 0
  最小值: 0
  最大值: 4294967295
- 
  序号: 17
  名称: RteEnforceIoc
  长名称: ''
  描述: |
    Enforce the usage of IOCs for cross-partition communication.
    If this parameter is set to false, the RTE assumes that all partitions have read access to all
    RTE variables.
    Buffers are allocated to the writing partition and IOCs are only used for N:1 communication.
    Buffers that are used for cross-core communication need to be mapped to synchronized RAM so that
    spinlocks only need to
    be used for variables that cannot be accessed atomically.
    If this parameter is set to true, the RTE relies on OS IOC objects for cross-partition
    communication.
    As the OS does not know which runnables access the individual IOCs, this tends to be less
    efficient when it comes to
    interrupt/spinlock locking times, runtime, ram and rom consumption.
    The parameter is ignored for:
    - mode communication
    - inter-ECU client-server communication
    - nv data communication
    - sender-receiver communication when transformers and scaling are configured
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 18
  名称: RteVttVfbTraceFunction
  长名称: ''
  描述: The RTE generator shall enable VTT tracing for the given hook function.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 19
  名称: RteInitializeImplicitBuffers
  长名称: ''
  描述: |
    This parameter ensures that no undefined values are written back at runnable termination.
    If this parameter is set to true, the RTE will send the last written value.
    If no RTE API for implicit write is called before, the initValue will be sent.
    
    [SWS_Rte_08418]
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 20
  名称: RteComTimeoutSource
  长名称: ''
  描述: |
    This parameter specifies the source for deriving the ComTimeout parameter of a ComSignal /
    ComSignalGroup.
    
    SWC: The timeout value is derived from the ReceiverComSpec (AliveTimeout) of the SWC port
    description.
    SIGNAL: The timeout value is derived from the ISignalPort of the communication description. This
    still requires a timeout value (AliveTimoeut) at the ReceiverComSpec != 0 to generally enable
    the timeout handling.
  默认值: SWC
  最小值: ''
  最大值: ''
- 
  序号: 21
  名称: RteEnforceQueuedIoc
  长名称: ''
  描述: |
    Enforce the usage of IOCs for queued cross-partition communication.
    Unlike the RteEnforceIoc parameter, this parameter only affects queued communication.
    If this parameter is set to true, the RTE relies on OS IOC objects for queued cross-partition
    communication.
    If the OS provides spinlock free IOCs, this parameter can be set to true to avoid the spinlock
    generation in the RTE for queued
    sender-receiver communication.
    
    The parameter is ignored for:
    - mode communication
    - inter-ECU client-server communication
    - sender-receiver communication when transformers and scaling are configured
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 22
  名称: RteUseAbsAlarmInitialization
  长名称: Use AbsAlarm Initialization
  描述: The RTE generator shall use SetAbsAlarm() for alarm initialization.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 23
  名称: RteOptimizeLocksInASILPartitions
  长名称: ''
  描述: |
    If this parameter is set to true, the RTE generator also considers the task priorities and
    preemption settings to optimize APIs in ASIL partitions.
    Otherwise, the RTE generator uses a more conservative locking strategy for ASIL partitions to
    reduce the risk of data consistency problems when the APIs are accidentally called from the
    wrong task.
    Independently of the value of this switch, it is the responsibility of the user to call the APIs
    only from runnables that are configured to use the APIs.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 24
  名称: UseRteSemanticsForIntraLetCommunication
  长名称: ''
  描述: |
    Enables an alternative LET communication semantic.
    If this parameter is set to true the RTE generator treats the implicit communication within a
    LET interval as if it were the classic implicit communication. Otherwise the communication will
    be purely handled by LET semantics.
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 25
  名称: RteBasicRuntimeEnvironmentMode
  长名称: ''
  描述: Activates Generation of BRE.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 26
  名称: RteEnableLET
  长名称: ''
  描述: Enables generation of LET.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 27
  名称: RteEnableMemoryProtection
  长名称: ''
  描述: Is set to true if memory protection is configured.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 28
  名称: RteEnableMultiCore
  长名称: ''
  描述: Is set to true if multi core is configured.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 29
  名称: RteDisableInterEcuIntToIntDataConversion
  长名称: ''
  描述: |
    Disables inter ecu integer to integer data conversion.
    For BSW packages before R31, the switch gets automatically set to true if it is not configured.
    Starting with R31 the conversion is always enabled if not explicitly disabled by this switch.
    The RTE generator derives the conversion formula from the CompuMethod on the system signal and
    the data element.
    
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 30
  名称: RteAlarmGlobalStartOffset
  长名称: ''
  描述: global start offset for cyclic runnables when SetAbsAlarm or SetRelAlarm is used.
  默认值: 1
  最小值: 0
  最大值: 4294967295
- 
  序号: 31
  名称: RteDisableRteInitMemory
  长名称: ''
  描述: |
    The API function Rte_InitMemory and SomeIpXf_InitMemory is a MICROSAR Classic RTE/SomeIpXf
    specific extension and should be used to initialize RTE/SomeIpXf internal state variables if the
    compiler does not support initialized variables.
    If the system has already initialized the variables, the Rte_InitMemory and
    SomeIpXf_InitMemory-API can be deactivated and the API will no longer be generated to save ROM.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 32
  名称: RteDisableOsScheduleTableAndAlarmGeneration
  长名称: ''
  描述: |
    Disables the generation of the os schedule tables and alarms for timing events.
    The elements are no longer added to the OS configuration and the RTE no longer starts them in
    the RTE lifecycle APIs.
    This parameter can be used for cases where the tasks are activated manually by the integration
    code.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 11. RteVfbTraceClient

**描述**: The RTE shall add the VFB Trace client with the ShortName of this container as the client’s prefix.

#### 参数列表

```yaml
- 
  序号: 1
  名称: RteVfbTraceClientPosition
  长名称: ''
  描述: Defines the position within all trace clients at which to call the trace functions of this
      trace client. The bigger the number the later the start trace functions and the sooner
      the stop trace functions will be called.
  默认值: ''
  最小值: 0
  最大值: 65535
- 
  序号: 2
  名称: RteVfbTraceFunction
  长名称: ''
  描述: The RTE generator shall enable VFB tracing for a given hook function when its name starts with
      the string configured here. Example: If Rte_Dbg_WriteHook_i2 is configured,
      Rte_Dbg_WriteHook_i1_p1_a_Start will be enabled.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 12. RteImplicitCommunication

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

### 13. RteInitializationBehavior

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
  默认值: RTE_INITIALIZATION_STRATEGY_AT_RTE_START_AND_PARTITION_RESTART
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

### 14. RteOsInteraction

**描述**: Interaction of the Rte with the Os.

该容器没有参数。

### 15. RteModeToScheduleTableMapping

**描述**: Provides configuration input in which Modes of a ModeDeclarionGroupPrototype of a Mode Manager a
OsScheudleTable shall be active.

该容器没有参数。

### 16. RteModeSchtblMapBsw

**描述**: Specifies an instance of a ModeDeclarationGroupPrototype of a Bsw-Module.

该容器没有参数。

### 17. RteModeSchtblMapSwc

**描述**: Specifies an instance of a ModeDeclarationGroupPrototype of a SwComponentPrototype.

该容器没有参数。

### 18. RteUsedOsActivation

**描述**: Attributes used in the activation of OsTasks and Runnable Entities.

#### 参数列表

```yaml
- 
  序号: 1
  名称: RteExpectedActivationOffset
  长名称: ''
  描述: Activation offset.
  默认值: 0
  最小值: 0
  最大值: ''
- 
  序号: 2
  名称: RteExpectedTickDuration
  长名称: ''
  描述: The expected tick duration which shall be configured to drive the OsScheduleTables or OsAlarm.
  默认值: 0
  最小值: 0
  最大值: ''
```

### 19. RtePostBuildVariantConfiguration

**描述**: Specifies the PostbuildVariantSets for each of the PostBuild configurations of the RTE.

该容器没有参数。

### 20. RteSwComponentInstance

**描述**: Representation of one SwComponentPrototype located on the to be configured ECU. All subcontainer
configuration aspects are in relation to this SwComponentPrototype.

该容器没有参数。

### 21. RteEventToTaskMapping

**描述**: Maps a RunnableEntity onto one OsTask based on the activating RTEEvent.

#### 参数列表

```yaml
- 
  序号: 1
  名称: RteActivationOffset
  长名称: ''
  描述: Activation offset.
  默认值: ''
  最小值: 0
  最大值: ''
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
  默认值: NONE
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
- 
  序号: 5
  名称: RteCyclicTriggerImplementation
  长名称: ''
  描述: |
    If set to 'Auto' the RTE generator automatically creates the necessary OS alarm to realize the
    cyclic trigger with the configured activation offset.
    If set to 'None' the trigger is not implemented by the RTE generator. It has to be implemented
    by the user either by configuring an appropriate OS alarm or an OS schedule table.
    The OS task and optional the OS event for that trigger can be found in the generated RTE report.
    
  默认值: Auto
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: RteServerQueueLength
  长名称: ''
  描述: Specifies the length of the queue for the server call serialization. This value overwrites the
      queueLength specified at the ServerComSpec.
  默认值: ''
  最小值: 0
  最大值: 65535
```

### 22. RteExclusiveAreaImplementation

**描述**: Specifies the implementation to be used for the data consistency of this ExclusiveArea.

#### 参数列表

```yaml
- 
  序号: 1
  名称: RteExclusiveAreaImplMechanism
  长名称: ''
  描述: To be used implementation mechanism for the specified ExclusiveArea.
  默认值: OS_INTERRUPT_BLOCKING
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: RteExclusiveAreaOptimization
  长名称: ''
  描述: |
    If set to true, the RTE generator tries to optimize the implementation (e.g. disable unnecessary
    interrupt lock)  of the exclusive area if possible.
    If set to false, the RTE generator does not optimize the exclusive area.
  默认值: true
  最小值: ''
  最大值: ''
```

### 23. RteExternalTriggerConfig

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

### 24. RteInternalTriggerConfig

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

### 25. RteModeMachineInstanceConfig

**描述**: Defines the configuration of RTE assigned (<b>SWS_Rte_07533)</b> mode machine instances.

该容器没有参数。

### 26. RteNvRamAllocation

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

### 27. RteSwComponentType

**描述**: Representation of one SwComponentType for the base of all configuration parameter which are
affecting the whole type and not a specific instance.

#### 参数列表

```yaml
- 
  序号: 1
  名称: RteSwcMemMapGeneration
  长名称: MemMap Generation
  描述: Enables or disables the generation of MemMap files for the specified Software Component by the
      RTE generator. Default is enabled when the generation is not done by the MemMap
      generator.
  默认值: true
  最小值: ''
  最大值: ''
```

### 28. RteComponentTypeCalibration

**描述**: Specifies for each ParameterSwComponentType or AtomicSwComponentType whether calibration is enabled.

#### 参数列表

```yaml
- 
  序号: 1
  名称: RteCalibrationSupportEnabled
  长名称: ''
  描述: Enables calibration support for the specified ParameterSwComponentType or
      AtomicSwComponentType.
  默认值: false
  最小值: ''
  最大值: ''
```

### 29. RteInitializationRunnableBatch

**描述**: Presence of at least one RteInitializationRunnableBatch enables the Rte_StartTiming API.

该容器没有参数。

