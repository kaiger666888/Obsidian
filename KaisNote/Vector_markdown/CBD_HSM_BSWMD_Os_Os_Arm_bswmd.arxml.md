# Os

## 模块描述

Configuration of the MICROSAR OS (Operating System) module.

## 容器列表

### 1. OsAlarm

**描述**: An OsAlarm may be used to asynchronously inform or activate a specific task. It is possible to start
alarms automatically at system start-up depending on the application mode.

该容器没有参数。

### 2. OsAlarmActivateTask

**描述**: This container specifies the parameters to activate a task.

该容器没有参数。

### 3. OsAlarmCallback

**描述**: This container specifies the parameters to call a callback OS alarm action.

#### 参数列表

```yaml
- 
  序号: 1
  名称: OsAlarmCallbackName
  长名称: ''
  描述: Name of the function that is called when this alarm callback is triggered.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 4. OsAlarmIncrementCounter

**描述**: This container specifies the parameters to increment a counter.

该容器没有参数。

### 5. OsAlarmSetEvent

**描述**: This container specifies the parameters to set an event.

该容器没有参数。

### 6. OsAlarmScheduleEventRoundRobin

**描述**: This container specifies, that the alarm is used for round robin scheduling.
Exactly one alarm with this container is needed per core which has one or more tasks that have round
robin scheduling configured by means of the container: OsTaskRoundRobinScheduling.
Typically, this is enforced by a validator with a preferred solving action. So no need to add such
an alarm manually.


该容器没有参数。

### 7. OsAlarmAutostart

**描述**: If present this container defines if an alarm is started automatically at system start-up depending
on the application mode.

#### 参数列表

```yaml
- 
  序号: 1
  名称: OsAlarmAlarmTime
  长名称: ''
  描述: The relative or absolute tick value when the alarm expires for the first time. Note that for
      an alarm which is RELATIVE the value must be at bigger than 0.
  默认值: ''
  最小值: 0
  最大值: 4294967295
- 
  序号: 2
  名称: OsAlarmAutostartType
  长名称: ''
  描述: This specifies the type of autostart for the alarm..
  默认值: RELATIVE
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: OsAlarmCycleTime
  长名称: ''
  描述: Cycle time of a cyclic alarm in ticks. If the value is 0 than the alarm is not cyclic.
  默认值: 0
  最小值: 0
  最大值: 4294967295
```

### 8. OsAppMode

**描述**: OsAppMode is the object used to define an OS application mode.

该容器没有参数。

### 9. OsApplication

**描述**: An AUTOSAR OS must be capable of supporting a collection of OS objects (tasks, interrupts, alarms,
hooks etc.) that form a cohesive functional unit. This collection of objects is termed an
OS-Application.

#### 参数列表

```yaml
- 
  序号: 1
  名称: OsTrusted
  长名称: ''
  描述: Parameter to specify if an OS-Application is trusted or not.
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: OsTrustedApplicationDelayTimingViolationCall
  长名称: ''
  描述: Parameter to specify if a timing violation which occurs within an trusted OS-Application is
      raised immediately or if it is delayed until the current task returns to the calling
      OS-Application (return of CallTrustedFunction).
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: OsTrustedApplicationWithProtection
  长名称: ''
  描述: Parameter to specify if a trusted OS-Application is executed with memory protection or not.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: OsApplicationIsPrivileged
  长名称: ''
  描述: This parameter specifies whether the OS-Application shall run in supervisor (privileged) or
      user mode.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: OsAppMemoryProtectionIdentifier
  长名称: ''
  描述: This optional parameter can be used to specify a memory protection identifier for the
      OS-Application.
  默认值: 0
  最小值: 0
  最大值: 4294967295
- 
  序号: 6
  名称: OsAppUseTrustedFunctionStubs
  长名称: ''
  描述: |
    This parameter enables the MICROSAR OS extension to the standard trusted function feature.
    Trusted function stubs package all user configured parameters and provide an API to call the
    trusted function with the specified parameters.
    
    Syntax: Os_Call_<TrustedFunctionName>(arg1, arg2, ...)
    
    true: Trusted function stubs will be generated
    false: No stubs will be generated
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: OsAppCalloutStubsIncludeHeader
  长名称: ''
  描述: |
    This parameter could be used to specify user specific data types for trusted function stubs.
    Insert header files to be included in Os_Lcfg.h and Os_Service_Lcfg.c.
    
    Insert complete filenames including extension (e.g. MyHeader.h).
    
  默认值: ''
  最小值: ''
  最大值: ''
```

### 10. OsApplicationHooks

**描述**: Container to structure the OS-Application-specific hooks.

#### 参数列表

```yaml
- 
  序号: 1
  名称: OsAppErrorHook
  长名称: ''
  描述: Select the OS-Application specific error hook.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: OsAppShutdownHook
  长名称: ''
  描述: Select the OS-Application specific shutdown hook.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: OsAppStartupHook
  长名称: ''
  描述: Select the OS-Application specific startup hook.
  默认值: false
  最小值: ''
  最大值: ''
```

### 11. OsApplicationTrustedFunction

**描述**: Container to structure the configuration parameters of trusted functions.

#### 参数列表

```yaml
- 
  序号: 1
  名称: OsTrustedFunctionName
  长名称: ''
  描述: Trusted function (as part of a trusted OS-Application) available to other OS-Applications.
      This also supersedes the OSEK OIL attribute TRUSTED in APPLICATION because the
      optionality of this parameter is describing that already.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: OsTrustedFunctionReturnType
  长名称: ''
  描述: This parameter specifies the return value of the trusted function.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 12. OsTrustedFunctionParam

**描述**: This container includes all configuration sub-attributes of one trusted function parameter.
These will be used for trusted function stubs generation. This feature can be enabled with
/MICROSAR/Os/OsApplication/OsAppUseTrustedFunctionStubs.
If no parameter is specified, 'void' is generated.

Note: Passed pointers have to be checked for validity by the trusted function implementation.

#### 参数列表

```yaml
- 
  序号: 1
  名称: OsTrustedFunctionParamId
  长名称: ''
  描述: This parameter is used to order the trusted function parameters.
  默认值: 1
  最小值: 1
  最大值: 127
- 
  序号: 2
  名称: OsTrustedFunctionParamDataType
  长名称: ''
  描述: |
    This parameter defines the C data type of the trusted function parameter.
    
    Note: If IN parameter is a complex datatype, it shall be passed by reference ('const
    <DataType>*').
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: OsTrustedFunctionParamDirection
  长名称: ''
  描述: |
    This parameter defines the usage direction of a trusted function parameter.
    
    IN: Parameter is only used as input value (passed by value or reference: '<DataType> arg').
    OUT: Parameter is only used as output value (always passed by reference: '<DataType> *arg').
    IN_OUT: Parameter is used as input and output value (always passed by reference: '<DataType>
    *arg').
    
    Where <DataType> is the configured data type string.
  默认值: IN
  最小值: ''
  最大值: ''
```

### 13. OsApplicationFastTrustedFunction

**描述**: Container to structure the configuration parameters of MICROSAR OS fast trusted functions.

Note:
OsApplicationFastTrustedFunction is only provided as a Beta feature and must not be used in
productive projects.

#### 参数列表

```yaml
- 
  序号: 1
  名称: OsFastTrustedFunctionName
  长名称: ''
  描述: Fast trusted function (as part of a trusted OS-Application) available to other
      OS-Applications.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 14. OsApplicationNonTrustedFunction

**描述**: Container to structure the configuration parameters of MICROSAR OS non-trusted functions.

#### 参数列表

```yaml
- 
  序号: 1
  名称: OsNonTrustedFunctionName
  长名称: ''
  描述: Non-trusted function (as part of a non-trusted OS-Application) available to other
      OS-Applications.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: OsNonTrustedFunctionStacks
  长名称: ''
  描述: |
    Specifies the maximum number of stacks for the non-trusted function.
    
    Each parallel call of a non-trusted function needs its own stack. So this value must be equal to
    the maximum number of parallel calls of this function.
  默认值: 1
  最小值: 1
  最大值: 4294967295
- 
  序号: 3
  名称: OsNonTrustedFunctionStackSize
  长名称: ''
  描述: This attribute specifies the stack size of the non-trusted function in bytes. In case of
      parallel calls each stack is set up with the same size.
  默认值: 1024
  最小值: 0
  最大值: 4294967295
```

### 15. OsNonTrustedFunctionCaller

**描述**: This container structures all parameters to specify the maximum number of stacks for a non-trusted
function used by a specific OS-Application.

#### 参数列表

```yaml
- 
  序号: 1
  名称: OsNonTrustedFunctionAppStacks
  长名称: ''
  描述: |
    Specifies the maximum number of stacks for the non-trusted function used by the referenced
    OS-Application.
    
    Each parallel call of a non-trusted function needs its own stack. So this value must be equal to
    the maximum number of parallel calls from the referenced OS-Application.
  默认值: 1
  最小值: 0
  最大值: 4294967295
```

### 16. OsBarrier

**描述**: A barrier provides a method that synchronizes tasks. The calling task blocks until all participating
tasks reach the barrier. Only one task per core may participate in a barrier.

该容器没有参数。

### 17. OsCore

**描述**: This container defines all configuration parameters for a MICROSAR OS-Core.

Each physical core shall be represented by an OS-Core.

#### 参数列表

```yaml
- 
  序号: 1
  名称: OsCoreEntrySymbol
  长名称: ''
  描述: |
    This parameter defines the entry symbol (startup/reset vector) of the OS-Core. It shall be the
    linker label where the core starts on multi-core systems.
    
    Note: If no default entry symbol is configured, this parameter can be omitted.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: OsCoreIsAutostart
  长名称: ''
  描述: |
    Specifies whether the core has been already started before the OS initialization.
    
    Note: This could be done by hardware or software (e.g. hypervisor or startup code). If in doubt
    use the proposed default value.
    
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: OsCoreIsAutosar
  长名称: ''
  描述: Specifies whether the OS-Core is an AUTOSAR core or not. Which means this core is used with
      the MICROSAR OS.
  默认值: false
  最小值: ''
  最大值: ''
```

### 18. OsCoreStacks

**描述**: Contains all stack configuration attributes for one OS-Core.

#### 参数列表

```yaml
- 
  序号: 1
  名称: OsCoreKernelStackSize
  长名称: ''
  描述: |
    This attribute specifies the stack size of the OS kernel in bytes.
    
    The memory exception handling is executed on this stack.
  默认值: 1024
  最小值: 0
  最大值: 4294967295
- 
  序号: 2
  名称: OsCoreStartupStackSize
  长名称: ''
  描述: |
    This attribute specifies the OS startup stack size in bytes.
    
    All startup hooks (global and application specific) are executed on this stack.
  默认值: 1024
  最小值: 0
  最大值: 4294967295
- 
  序号: 3
  名称: OsCoreShutdownStackSize
  长名称: ''
  描述: |
    This attribute specifies the OS shutdown stack size in bytes.
    
    All shutdown hooks (global and application specific) are executed on this stack.
  默认值: 1024
  最小值: 0
  最大值: 4294967295
- 
  序号: 4
  名称: OsCoreErrorStackSize
  长名称: ''
  描述: |
    This attribute specifies the OS error stack size in bytes.
    
    All error hooks (global and application specific) are executed on this stack.
  默认值: 1024
  最小值: 0
  最大值: 4294967295
- 
  序号: 5
  名称: OsCoreProtectionStackSize
  长名称: ''
  描述: |
    This attribute specifies the OS protection stack size in bytes.
    
    The protection hook is executed on this stack.
  默认值: 1024
  最小值: 0
  最大值: 4294967295
- 
  序号: 6
  名称: OsCoreInitStackSize
  长名称: ''
  描述: |
    This attribute specifies the OS init stack size in bytes.
    
    The OS initialization is executed on this stack.
  默认值: 1024
  最小值: 0
  最大值: 4294967295
```

### 19. OsCoreXSignalChannel

**描述**: This container structures all parameters for a cross-core API call channel. It shall be used to
trigger APIs on another OS-Core.
Only one send channel per OS-Core is possible.

Valid APIs to be callable cross-core shall be defined in the corresponding receiver ISR
(OsIsr/OsIsrXSignalReceiver).

#### 参数列表

```yaml
- 
  序号: 1
  名称: OsCoreXSignalChannelSize
  长名称: ''
  描述: Specifies the number of cross-core service requests that can be queued.
  默认值: 1
  最小值: 0
  最大值: 65534
```

### 20. OsCounter

**描述**: Configuration information for the counters that belong to the OS-Application.

#### 参数列表

```yaml
- 
  序号: 1
  名称: OsCounterMaxAllowedValue
  长名称: ''
  描述: Maximum allowed value of the system counter in ticks.
  默认值: 1073741823
  最小值: 1
  最大值: 4294967295
- 
  序号: 2
  名称: OsCounterMinCycle
  长名称: ''
  描述: The MINCYCLE attribute specifies the minimum allowed number of counter ticks for a cyclic
      alarm linked to the counter.
  默认值: 1
  最小值: 1
  最大值: 4294967295
- 
  序号: 3
  名称: OsCounterTicksPerBase
  长名称: ''
  描述: |
    The TICKSPERBASE attribute specifies the number of ticks required to reach a counter specific
    unit. The interpretation is implementation-specific.
    The value is calculated by dividing the desired counter period (OsSecondsPerTick) by the period
    of a single hardware tick, which is calculated by the reciprocal of the frequency (1/fosc).
  默认值: 1
  最小值: 1
  最大值: 4294967295
- 
  序号: 4
  名称: OsCounterType
  长名称: ''
  描述: This parameter contains the natural type or unit of the counter.
  默认值: SOFTWARE
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: OsSecondsPerTick
  长名称: ''
  描述: |
    Time of one counter tick in seconds.
    The value specifies the desired tick period of the counter in seconds. (0.001 = 1ms)
  默认值: 0.001
  最小值: 0
  最大值: 4294967295
```

### 21. OsDriver

**描述**: This Container contains information of the driver of a hardware counter.

#### 参数列表

```yaml
- 
  序号: 1
  名称: OsDriverHighResolution
  长名称: ''
  描述: Specifies whether the counter is a high resolution timer or not.
  默认值: false
  最小值: ''
  最大值: ''
```

### 22. OsTimeConstant

**描述**: Allows the user to define constants which can be e.g. used to compare time values with timer tick
values.

#### 参数列表

```yaml
- 
  序号: 1
  名称: OsTimeValue
  长名称: ''
  描述: This parameter contains the value of the constant in seconds.
  默认值: ''
  最小值: 0
  最大值: 4294967295
```

### 23. OsEvent

**描述**: Representation of OS events in the configuration context.

#### 参数列表

```yaml
- 
  序号: 1
  名称: OsEventMask
  长名称: ''
  描述: |
    This parameter can be used to specify the bit mask for the event. If empty the event mask is
    automatically calculated.
    
    It is recommended to use automatically calculated event masks.
  默认值: 1
  最小值: 1
  最大值: 18446744073709551615
```

### 24. OsIoc

**描述**: Configuration of the IOC (Inter OS Application Communicator).

#### 参数列表

```yaml
- 
  序号: 1
  名称: OsIocIncludeHeader
  长名称: ''
  描述: |
    This parameter is used to specify header files to be included in the generated IOC header file.
    It could be necessary to provide user specific datatypes to the IOC module.
    
    Insert complete filenames including extension (e.g. MyHeader.h).
  默认值: ''
  最小值: ''
  最大值: ''
```

### 25. OsIocCommunication

**描述**: Representation of a 1:1 or N:1 or N:M (unqueued only) communication between software parts located
in different OS-Applications that are bound to the same or to different cores.

#### 参数列表

```yaml
- 
  序号: 1
  名称: OsIocBufferLength
  长名称: ''
  描述: This attribute defines the size of the IOC internal queue to be allocated for a queued
      communication.
  默认值: 0
  最小值: 0
  最大值: 4294967295
```

### 26. OsIocDataProperties

**描述**: Data properties of the data to be transferred on the IOC communication channel.

#### 参数列表

```yaml
- 
  序号: 1
  名称: OsIocDataPropertyIndex
  长名称: ''
  描述: This parameter is used to define in which order the data is send, e.g. whether
      IocSendGroup(A,B) or IocSendGroup(B,A) shall be used.
  默认值: 0
  最小值: 0
  最大值: 126
- 
  序号: 2
  名称: OsIocInitValue
  长名称: ''
  描述: |
    Initial Value for the data to be transferred on the IOC communication channel.
    
    Note: If the used data is of a complex type the parameter has to define a name of a constant
    (not a value) which contains the initial value for the data. In case an intergral type is used
    the parameter may be both: a literal value or a name of a constant containing the value as
    above.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: OsIocDataType
  长名称: ''
  描述: |
    This is the type of the data to be transferred on the IOC communication channel. This attribute
    is necessary to generate the parameter type of the IOC functions.
    
    Currently this parameter is used instead of OsIocDataTypeRef to specify the data type.
    These types are recognised as primitive:
    All integer and float based types defined by AUTOSAR in StdTypes and PlatformTypes.
    Additionally, also the public integer based types and enumerations defined in Os_Types.h and
    Os_Types_Lcfg.h are recognised.
    These are:
    
    AccessType
    AlarmType
    ApplicationStateType
    ApplicationType
    AppModeType
    boolean
    CoreIdType
    CounterType
    EventMaskType
    float32
    float64
    IdleModeType
    ISRType
    MemorySizeType
    ObjectAccessType
    ObjectTypeType
    OSServiceIdType
    Os_BarrierIdType
    Os_ErrorParmIndexType
    Os_ExceptionSourceIdType
    Os_FastTrustedFunctionIndexType
    Os_InterruptSourceIdType
    Os_MemAccessType
    Os_NonTrustedFunctionIndexType
    Os_ObjectIdType
    Os_PeripheralIdType
    Os_StatusType
    Os_TickDiffType
    Os_TraceSpinlockIdType
    Os_TraceThreadIdType
    PhysicalTimeType
    ProtectionReturnType
    ResourceType
    RestartType
    ScheduleTableStatusType
    ScheduleTableType
    sint8
    sint8_least
    sint16
    sint16_least
    sint32
    sint32_least
    sint64
    SpinlockIdType
    StatusType
    Std_ReturnType
    TaskStateType
    TaskType
    TickType
    TrustedFunctionIndexType
    TryToGetSpinlockType
    uint8
    uint8_least
    uint16
    uint16_least
    uint32
    uint32_least
    uint64
    
    All other types used as OsIocDataType are handled as reference and invoke memory copy actions
    which increase runtime in comparison.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: OsIocDataTypeIsAtomic
  长名称: ''
  描述: Specifies if the type in OsIocDataType is an atomic data type or not. Which means it can be
      copied with one copy instruction and no locks are necessary.
  默认值: false
  最小值: ''
  最大值: ''
```

### 27. OsIocReceiverProperties

**描述**: Representation of receiver properties for one communication. For each OsIocCommunication one (1:1)
or many receivers (N:M) have to be defined.  This container should be instantiated within an
OsIocCommunication.

#### 参数列表

```yaml
- 
  序号: 1
  名称: OsIocFunctionImplementationKind
  长名称: ''
  描述: |
    This parameter is used to select whether this communication is implemented as a macro or as a
    function.
    Not all implementation kinds are allowed for each kind of communication.
    
    DO_NOT_CARE: Implementation kind is selected by the OS
    FUNCTION: User functions are generated as functions
    MACRO: User functions are generated as macros
  默认值: DO_NOT_CARE
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: OsIocReceiverPullCB
  长名称: ''
  描述: This attribute defines the name of a callback function that the IOC shall call on the
      receiving core for each data reception.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: OsIocReceiverPullCBStackSize
  长名称: ''
  描述: This attribute specifies the stack size of the IOC pull callback function in bytes.
  默认值: 1024
  最小值: 0
  最大值: 4294967295
```

### 28. OsIocSenderProperties

**描述**: Representation of sender properties for one communication. For each OsIocCommunication one (1:1) or
many senders (N:1 or N:M) have to be defined. Multiplicity > 1 (N:1 or N:M communication) is only
allowed for Multiplicity of OsIocDataTypeRef = 1.

#### 参数列表

```yaml
- 
  序号: 1
  名称: OsIocFunctionImplementationKind
  长名称: ''
  描述: |
    This parameter is used to select whether this communication is implemented as a macro or as a
    function.
    Not all implementation kinds are allowed for each kind of communication.
    
    DO_NOT_CARE: Implementation kind is selected by the OS
    FUNCTION: User functions are generated as functions
    MACRO: User functions are generated as macros
  默认值: DO_NOT_CARE
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: OsIocSenderId
  长名称: ''
  描述: Representation of a sender in a N:1 or N:M communication to distinguish between senders.
  默认值: 0
  最小值: 0
  最大值: 255
```

### 29. OsIsr

**描述**: The OsIsr container represents an interrupt service routine.

#### 参数列表

```yaml
- 
  序号: 1
  名称: OsIsrCategory
  长名称: ''
  描述: This attribute specifies the category of this ISR.
  默认值: CATEGORY_2
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: OsIsrInterruptType
  长名称: ''
  描述: This parameter specifies the interrupt source type of the ISR.
  默认值: EXTERNAL
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: OsIsrInterruptSource
  长名称: ''
  描述: Specifies the interrupt source number of the ISR.
  默认值: 1
  最小值: 0
  最大值: 4294967295
- 
  序号: 4
  名称: OsIsrInterruptPriority
  长名称: ''
  描述: |
    The priority (level) of an ISR is defined by the value of this attribute.
    
    This value represents the hardware specific interrupt priority, so refer to hardware manual for
    ordering and number of maximum priorities.
  默认值: 0
  最小值: 0
  最大值: 4294967295
- 
  序号: 5
  名称: OsIsrStackSize
  长名称: ''
  描述: |
    This attribute specifies the stack size of the Interrupt in bytes.
    
    Interrupts with disabled nesting will share one stack per core.
    Interrupts on the same level (priority) and enabled nesting will share one stack per level and
    core.
    In both cases the biggest configured size will be used to set up the stack size.
    
    Only applicable for category 2 ISRs. Category 1 ISRs will use the current active stack.
  默认值: 1024
  最小值: 0
  最大值: 4294967295
- 
  序号: 6
  名称: OsIsrMemoryProtectionIdentifier
  长名称: ''
  描述: |
    This optional parameter can be used to specify a memory protection identifier for the ISR.
    
    If this parameter is not set but the owner OS-Application has a memory protection identifier
    specified this value will be used for the interrupt.
  默认值: 0
  最小值: 0
  最大值: 4294967295
- 
  序号: 7
  名称: OsIsrSpecialFunctionName
  长名称: ''
  描述: |
    This parameter can be used to specify an user defined function name which is called if the
    configured interrupt occurs. By default the function name is created by the container name.
    
    This can be used if multiple interrupt sources shall share the same interrupt handler function.
    
    In case of a category 2 ISR the prefix "Os_Isr_" is internally added to the function name.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 8
  名称: OsIsrEnableNesting
  长名称: ''
  描述: |
    Specifies whether the ISR is interruptible by another ISR or not.
    
    true: Interrupts will be enabled before entering the interrupt handler function. So ISRs with
    higher priority can interrupt the ISR.
    false: Interrupting of the ISR is only possible by FIQs, NMIs or exceptions (Depending on
    hardware).
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 9
  名称: OsIsrUsesFpu
  长名称: ''
  描述: |
    This parameter is used to specify if this ISR uses the FPU unit.
    
    This parameter only takes effect, if the parameter /MICROSAR/Os/OsOS/OsFpuUsage is set to
    "INDIVIDUAL".
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 10
  名称: OsIsrInitialEnableInterruptSource
  长名称: ''
  描述: |
    Specifies whether the interrupt source shall be enabled by a call to
    Os_InitialEnableInterruptSources().
    
    true: Os_InitialEnableInterruptSources() will enable the interrupt source.
    false: Os_InitialEnableInterruptSources() will ignore the interrupt source.
  默认值: true
  最小值: ''
  最大值: ''
```

### 30. OsIsrTimingProtection

**描述**: This container contains all parameters which are related to timing protection.

Timing protection is only allowed if OS scalability class is set to SC2 or SC4.

#### 参数列表

```yaml
- 
  序号: 1
  名称: OsIsrAllInterruptLockBudget
  长名称: ''
  描述: This parameter contains the maximum time for which the ISR is allowed to lock all interrupts
      (via SuspendAllInterrupts() or DisableAllInterrupts()) (in seconds).
  默认值: 0
  最小值: 0
  最大值: 4294967295
- 
  序号: 2
  名称: OsIsrExecutionBudget
  长名称: ''
  描述: The parameter contains the maximum allowed execution time of the interrupt (in seconds).
  默认值: 0
  最小值: 0
  最大值: 4294967295
- 
  序号: 3
  名称: OsIsrOsInterruptLockBudget
  长名称: ''
  描述: This parameter contains the maximum time for which the ISR is allowed to lock all Category 2
      interrupts (via SuspendOSInterrupts()) (in seconds).
  默认值: 0
  最小值: 0
  最大值: 4294967295
- 
  序号: 4
  名称: OsIsrTimeFrame
  长名称: ''
  描述: This parameter contains the minimum inter-arrival time between successive interrupts (in
      seconds).
  默认值: ''
  最小值: 0
  最大值: 4294967295
```

### 31. OsIsrResourceLock

**描述**: This container contains a list of times the interrupt uses resources.

#### 参数列表

```yaml
- 
  序号: 1
  名称: OsIsrResourceLockBudget
  长名称: ''
  描述: This parameter contains the maximum time the interrupt is allowed to hold the given resource
      (in seconds).
  默认值: 0
  最小值: 0
  最大值: 4294967295
```

### 32. OsIsrXSignalReceiver

**描述**: This container structures all parameters for a cross-core channel receiver interrupt.

#### 参数列表

```yaml
- 
  序号: 1
  名称: OsIsrXSignalReceiverProvidedApis
  长名称: ''
  描述: Specify all APIs which shall be usable via a cross-core API call.
  默认值: ShutdownAllCores
  最小值: ''
  最大值: ''
```

### 33. OsMemoryProtection

**描述**: Container to structure all memory protection relevant configuration parameters.

Memory protection is only allowed if OS scalability class is set to SC3 or SC4.

该容器没有参数。

### 34. OsMemoryRegion

**描述**: Container to structure the configuration parameters of one memory protection region.

#### 参数列表

```yaml
- 
  序号: 1
  名称: OsMemoryRegionStartAddress
  长名称: ''
  描述: |
    Start address of a memory protection region. The address can be specified either as a valid
    decimal (1024) or hexadecimal (0x4000) value, or as a valid linker symbol.
    
    StartAddress <= Memory to be accessed
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: OsMemoryRegionEndAddress
  长名称: Memory Region Size or End
  描述: |
    If a core MPU is used:
    Size of a memory protection region. The size can be specified either as a valid decimal (16384)
    or hexadecimal (0x4000) value.
    The value is bound to be a power of 2.
    If a system MPU is used:
    End address of a memory protection region. The address can be specified either as a valid
    decimal (1024) or hexadecimal (0x4000) value, or as a valid linker symbol.
    Memory to be accessed <= EndAddress.
    
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: OsMemoryRegionIdentifier
  长名称: ''
  描述: |
    Defines the optional hardware specific memory protection region identifier.
    
    The interpretation of this parameter is hardware specific (e.g. PID, ProtectionSet or ASID).
  默认值: 0
  最小值: 0
  最大值: 4294967295
- 
  序号: 4
  名称: OsMemoryRegionProtectionUnitSlot
  长名称: ''
  描述: |
    This optional parameter specifies on which MPU slot the memory protection region shall be used.
    
    The interpretation of this parameter is hardware specific.
  默认值: 0
  最小值: 0
  最大值: 4294967295
```

### 35. OsAccessCheckRegion

**描述**: Container to structure the configuration parameters of one check memory access region.

These regions are used for the AUTOSAR Check[Task|ISR]MemoryAccess() APIs.

#### 参数列表

```yaml
- 
  序号: 1
  名称: OsAccessCheckRegionStartAddress
  长名称: ''
  描述: |
    Start address of a check memory access region. The address can be specified either as a valid
    decimal (1024) or hexadecimal (0x4000) value, or as a valid linker symbol.
    
    StartAddress <= Memory to be accessed
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: OsAccessCheckRegionEndAddress
  长名称: ''
  描述: |
    End address of a check memory access region. The address can be specified either as a valid
    decimal (1024) or hexadecimal (0x4000) value, or as a valid linker symbol.
    
    Memory to be accessed <= EndAddress
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: OsAccessCheckRegionAccessRights
  长名称: ''
  描述: |
    This parameter specifies the expected access rights for a check memory access region.
    It is possible to combine access types.
    
    READ: Read access right is granted
    WRITE: Write access right is granted
    EXECUTE: Execution right is granted
    STACK: It is a stack region
    
    If nothing selected, no access rights are granted.
  默认值: READ
  最小值: ''
  最大值: ''
```

### 36. OsPeripheralRegion

**描述**: Container to structure the configuration parameters of one peripheral region.

The container short name can be used to access this region.

#### 参数列表

```yaml
- 
  序号: 1
  名称: OsPeripheralRegionStartAddress
  长名称: ''
  描述: |
    Start address of a peripheral region. The address can be specified either as a valid decimal
    (1024) or hexadecimal (0x4000) value, or as a valid linker symbol.
    
    StartAddress <= Memory to be accessed
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: OsPeripheralRegionEndAddress
  长名称: ''
  描述: |
    End address of a peripheral region. The address can be specified either as a valid decimal
    (1024) or hexadecimal (0x4000) value, or as a valid linker symbol.
    
    Memory to be accessed <= EndAddress
  默认值: ''
  最小值: ''
  最大值: ''
```

### 37. OsOS

**描述**: This container structures basic OS configuration attributes.

#### 参数列表

```yaml
- 
  序号: 1
  名称: OsNumberOfCores
  长名称: ''
  描述: Maximum number of cores that are controlled by the OS.
  默认值: 1
  最小值: 1
  最大值: 65535
- 
  序号: 2
  名称: OsScalabilityClass
  长名称: ''
  描述: |
    A scalability class for each System Object "OS" has to be selected. In order to customize the
    operating system to the needs of the user and to take full advantage of the processor features
    the operating system can be scaled according to the scalability classes.
    
    SC1: OSEK compliant with AUTOSAR extensions
    SC2: Timing Protection
    SC3: Memory Protection
    SC4: Memory and Timing Protection
  默认值: SC1
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: OsStackMonitoring
  长名称: ''
  描述: Enable stack monitoring of Tasks and Category 2 ISRs.
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: OsStatus
  长名称: ''
  描述: This parameter specifies if the system shall use standard or extended status checks.
  默认值: EXTENDED
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: OsUseGetServiceId
  长名称: ''
  描述: If selected, the usage of the access macros to get the service ID information in the error
      hook is enabled.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: OsUseParameterAccess
  长名称: ''
  描述: If selected, the usage of the access macros to get the context related information in the
      error hook is enabled.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: OsUseResScheduler
  长名称: ''
  描述: |
    The OsUseResScheduler attribute defines whether the resource RES_SCHEDULER is used within the
    application.
    
    Note: For multi-core systems the RES_SCHEDULER is generated for each core with name
    'RES_SCHEDULER_<CoreName>'.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 8
  名称: OsForcibleTermination
  长名称: ''
  描述: This parameter specifies whether forcible termination (killing) is enabled or not.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 9
  名称: OsGenerateCalloutStubs
  长名称: ''
  描述: |
    Enable user callout function stub generation for system and OS-Application specific hooks.
    
    true: User callout function stubs will be generated into file Os_Callout_Stubs.c
    false: No callout stubs will be generated
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 10
  名称: OsGenerateMemMap
  长名称: ''
  描述: |
    This parameter defines if complete, reduced or empty AUTOSAR MemMap files (Os_MemMap*.h) are
    generated.
    
    Note: The parameter /Os/OsOS/OsGenerateMemMapForThreads could also be used to reduce compile
    time or number of user defined sections.
    
    COMPLETE:
    Generate complete MemMap files including compiler specific pragmas (recommended for systems with
    memory protection).
    
    USERCODE_AND_STACKS_GROUPED_PER_CORE:
    Same as COMPLETE but some sections are grouped to decrease number of user defined linker
    sections:
      - User callout code sections (Tasks, ISRs, Hooks, etc.) of a core are grouped into one user
    code section
      - All stack sections of a core are grouped into one stack data section
    If selected and memory protection is enabled, all configured stack sizes must match the MPU
    granularity and alignment.
    Otherwise stack protection cannot be ensured.
    
    EMPTY:
    Generate empty MemMap files to reduce compile time. If selected, the AUTOSAR memory mapping
    mechanism cannot be used.
  默认值: COMPLETE
  最小值: ''
  最大值: ''
- 
  序号: 11
  名称: OsGenerateMemMapForNearAddressing
  长名称: ''
  描述: |
    This parameter specifies if additional memory sections for near addressing mode (e.g. sdata,
    sbss, sconst) shall be generated into Os_MemMap.h or not. This feature could be used to decrease
    compile time if memory sections for near addressing mode are not necessary according to the used
    compiler options.
    
    true: Generate additional memory sections for near addressing into Os_MemMap.h
    false: No memory sections for near addressing will be generated
    
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 12
  名称: OsGenerateMemMapForThreads
  长名称: ''
  描述: |
    This parameter specifies if additional memory sections for threads (Tasks and ISRs) shall be
    generated into Os_MemMap.h or not. This feature could be used to decrease compile time if memory
    sections for threads are not necessary.
    
    true: Generate additional memory sections for threads into Os_MemMap.h
    false: No memory sections for threads will be generated
    
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 13
  名称: OsServiceProtection
  长名称: ''
  描述: Enables service checks specified by AUTOSAR.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 14
  名称: OsStackUsageMeasurement
  长名称: ''
  描述: |
    Enables the MICROSAR OS feature to measure stack usage during runtime. There are several API
    functions (Os_Get*StackUsage) which can be used by the application to determine the current
    stack usage. Please refer to the TechnicalReference to see all available stack usage API
    functions and how to use this feature.
    
    This feature will increase OS start-up time because all configured stacks have to be filled with
    a check pattern.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 15
  名称: OsUseXSignalAsyncApiCalls
  长名称: ''
  描述: |
    This parameter is used to specify if cross-core API calls (XSignal) shall be performed
    synchronous (false) or asynchronous (true).
    
    It is only considered if at least one valid /MICROSAR/Os/OsCore/OsCoreXSignalChannel is
    configured.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 16
  名称: OsFpuUsage
  长名称: ''
  描述: |
    This parameter is used to specify the usage of the FPU unit, if it is available on the
    microcontroller. Using the FPU unit typically increases the size of the register context, which
    is saved and restored during a context switch.
    
    NONE: No thread uses the FPU unit.
    ALL: All the threads use the FPU unit.
    INDIVIDUAL: The usage is set individual for each thread.
    
    This parameter only takes effect on platforms, where the FPU context is great. On other
    platforms, the FPU context is always saved. Please refer to the Technical Reference for more
    detailed information about the concrete platforms.
  默认值: NONE
  最小值: ''
  最大值: ''
```

### 38. OsDebug

**描述**: Optional container to structure all debug support parameters for the OS. If not present all debug
supports will be disabled.

#### 参数列表

```yaml
- 
  序号: 1
  名称: OsAssertions
  长名称: ''
  描述: Enables additional OS assertions.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: OsORTIDebugSupport
  长名称: ''
  描述: |
    This parameter specifies if ORTI debug information is generated or not.
    
    ORTI_22_*: Support of standard ORTI 2.2 - one file for each AUTOSAR core is created
    (Os_Trace_<CoreName>.ORT)
    ORTI_23_*: Support of ORTI 2.2 inclusive SMP proposals (multi-core support) - single file
    (Os_Trace.ORT)
    
    *_STANDARD: Enables ORTI with tracing of Tasks and Isrs -- causes a small offset in runtime and
    memory consumption compared to non ORTI.
    *_ADDITIONAL: Same as *_STANDARD plus Service tracing -- causes a bigger offset in runtime and
    memory consumption than *_STANDARD.
    
    If nothing is selected (Parameter does not exist), no ORTI debug file is created.
  默认值: ORTI_22_ADDITIONAL
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: OsTimingHooksIncludeHeader
  长名称: ''
  描述: |
    This optional parameter is used to specify include files for the MICROSAR OS timing hooks.
    To enable timing hooks at least one include file has to be specified.
    
    Insert complete filenames including extension (e.g. MyTimingHooks.h).
  默认值: ''
  最小值: ''
  最大值: ''
```

### 39. OsHooks

**描述**: Container to structure all hooks belonging to the OS.

#### 参数列表

```yaml
- 
  序号: 1
  名称: OsErrorHook
  长名称: ''
  描述: |
    If selected, the ErrorHook routine is called, if an API function returns with an error code
    unequal to E_OK. It is also called if OS internal errors are detected.
    
    The function ErrorHook has to be provided by the application.
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: OsPostTaskHook
  长名称: ''
  描述: |
    If selected, the PostTaskHook routine will be called any time the operating system interrupts or
    terminates a task.
    
    The function PostTaskHook has to be provided by the application.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: OsPreTaskHook
  长名称: ''
  描述: |
    If selected, the PreTaskHook routine will be called any time the operating system starts or
    resumes a task.
    
    The function PreTaskHook has to be provided by the application.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: OsProtectionHook
  长名称: ''
  描述: Switch to enable/disable the call to the (user supplied) protection hook.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: OsShutdownHook
  长名称: ''
  描述: |
    If selected, the ShutdownHook routine will be called, if the API-function ShutdownOS is either
    called by the application or by the operating system.
    
    The function ShutdownHook has to be provided by the application.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: OsStartupHook
  长名称: ''
  描述: |
    If selected, the StartupHook routine will be called by the operating system in the startup phase
    (after calling StartOS and before starting the first task).
    
    The function StartupHook has to be provided by the application.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: OsPanicHook
  长名称: ''
  描述: |
    If selected, the PanicHook routine will be called by the operating system if an inconsistent OS
    state is detected and regular shutdown cannot be reached.
    
    The function Os_PanicHook has to be provided by the application.
  默认值: false
  最小值: ''
  最大值: ''
```

### 40. OsStackSummary

**描述**: This container provides an overview of all internal calculated OS stacks.
For example it can be used to determine which task uses which stack and how the size is configured.
The size has to be configured at the stack size parameter of the container which is referenced as
user.

Note: This stack summary is automatically created and updated during configuration. Manual
configuration of stacks in this summary is not supported.

该容器没有参数。

### 41. OsStack

**描述**: This container represents an OS stack.

#### 参数列表

```yaml
- 
  序号: 1
  名称: OsStackSize
  长名称: ''
  描述: |
    This value specifies the size of the stack in bytes.
    
    Note: For shared stacks the biggest configured stack size is used to set up this value.
  默认值: 1024
  最小值: 0
  最大值: 4294967295
- 
  序号: 2
  名称: OsStackType
  长名称: ''
  描述: |
    This parameter defines the type of the stack.
    
    Note: Each type refers to users assigned to the same core.
    
    CORE_CALLBACK_STACK: This stack is shared by all IOC receiver PullCBs.
    CORE_ERROR_STACK: This stack is shared by the global and all OS-Application specific ErrorHooks.
    CORE_INIT_STACK: This stack is used by the OS initialization.
    CORE_KERNEL_STACK: This stack is used by the memory exception handling.
    CORE_PROTECTION_STACK: This stack is used by the global ProtectionHook.
    CORE_STARTUP_STACK: This stack is shared by the global and all OS-Application specific
    StartupHooks.
    CORE_SHUTDOWN_STACK: This stack is shared by the global and all OS-Application specific
    ShutdownHooks.
    
    ISR_SHARED_CORE_STACK: This stack is shared by all non-nestable category 2 ISRs.
    ISR_SHARED_LEVEL_STACK: This stack is shared by all nestable category 2 ISRs configured to the
    same interrupt priority level.
    
    NTF_CALLER_STACK: This stack is used by exactly one caller of a non-trusted function.
    
    TASK_EXTENDED_STACK: This stack is only used by the extended user Task.
    TASK_SHARED_INTRES_STACK: This stack is shared by all basic Tasks with active stack sharing and
    the same internal resouce.
    TASK_SHARED_NONPRE_STACK: This stack is shared by all non-preemptable basic Tasks with active
    stack sharing.
    TASK_SHARED_PRIORITY_STACK: This stack is shared by all basic Tasks with the same priority.
  默认值: CORE_KERNEL_STACK
  最小值: ''
  最大值: ''
```

### 42. OsPublishedInformation

**描述**: OsPublishedInformation is used for additional published parameters and information.

#### 参数列表

```yaml
- 
  序号: 1
  名称: OsKernelVersion
  长名称: ''
  描述: Defines the kernel source code generation.
  默认值: 0
  最小值: 0
  最大值: 4294967295
- 
  序号: 2
  名称: OsPlatformName
  长名称: ''
  描述: Defines the name of the platform supported with this BSWMD.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 43. OsDerivativeInformation

**描述**: Contains all derivative specific information needed by the OS generator.

#### 参数列表

```yaml
- 
  序号: 1
  名称: OsMpuAlignment
  长名称: ''
  描述: |
    Defines the derivative specific alignment of stack linker sections in bytes.
    
    0: No alignment will be generated
    SIZE: Stack sections will be aligned to configured size
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: OsMpuMemoryGapSize
  长名称: ''
  描述: Defines the memory gap size in bytes between two consecutive memory sections.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: OsMpuEndAddressAccessible
  长名称: ''
  描述: |
    Defines whether the configured memory region end address is accessible or not.
    
    This depends on the hardware MPU evaluation of the effective address (EA):
    StartAddress <= EA <= EndAddress: True
    StartAddress <= EA  <  EndAddress: False
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: OsStackAlignment
  长名称: ''
  描述: |
    Defines the derivative specific alignment of stack linker sections in bytes.
    
    0: No alignment will be generated
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: OsInterruptVectorTableAlignment
  长名称: ''
  描述: |
    Defines the derivative specific alignment of interrupt vector table linker sections in bytes.
    
    0: No alignment will be generated
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: OsExceptionVectorTableAlignment
  长名称: ''
  描述: |
    Defines the derivative specific alignment of  exception vector table linker sections in bytes.
    
    0: No alignment will be generated
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: OsHardwareManuals
  长名称: ''
  描述: |
    Specifies the derivative specific hardware manuals including all relevant chapters.
    
    Specify name, version, release date of the document and all relevant chapters.
    e.g. Vendor Reference Manual, Rev. 1, 10/2016, chapters CORE, INTC, PIT, STM, MPU
  默认值: ''
  最小值: ''
  最大值: ''
```

### 44. OsPhysicalCore

**描述**: Derivative specific definition of a physical core.

#### 参数列表

```yaml
- 
  序号: 1
  名称: OsPhysicalCoreId
  长名称: ''
  描述: This parameter defines the physical Id of the core.
  默认值: 0
  最小值: 0
  最大值: 4294967295
- 
  序号: 2
  名称: OsPhysicalCoreType
  长名称: ''
  描述: Physical type of the physical core.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: OsPhysicalCoreDefaultEntrySymbol
  长名称: ''
  描述: Defines the default entry symbol of the core. It is used to setup OsCoreEntrySymbol of the
      referencing OsCore.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: OsPhysicalCoreExceptionSources
  长名称: ''
  描述: Defines the number of available exception sources on the physical core.
  默认值: 0
  最小值: 0
  最大值: 4294967295
- 
  序号: 5
  名称: OsPhysicalCoreIsAutostart
  长名称: ''
  描述: Defines whether the core is auto started after system reset.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: OsPhysicalCoreMasterStartAllowed
  长名称: ''
  描述: Defines whether the core is allowed to start the master core. Note that at most one physical
      core can be configured with this flag equal to True. Note that when this parameter is
      set to True, this core must be an auto-start core.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: OsPhysicalCorePrivelegedHwAccess
  长名称: ''
  描述: Defines whether the core has the privilege to initialize peripheral registers, e.g.: interrupt
      source registers in system interrupt controllers.
  默认值: false
  最小值: ''
  最大值: ''
```

### 45. OsPhysicalCoreIntCtrl

**描述**: Container to structure all core interrupt controller attributes.

#### 参数列表

```yaml
- 
  序号: 1
  名称: OsPhysicalCoreIntCtrlMaxSources
  长名称: ''
  描述: |
    This parameter specifies the highest configurable interrupt source.
    
    Example: If the interrupt controller supports 1024 interrupt sources (0-1023), the highest
    configurable interrupt source is 1023.
  默认值: 999
  最小值: 0
  最大值: 4294967295
- 
  序号: 2
  名称: OsPhysicalCoreIntCtrlMaxPrios
  长名称: ''
  描述: |
    This parameter specifies the highest configurable interrupt priority.
    
    Example: If an interrupt controller supports 64 priorities (0-63), the highest configurable
    priority is 63.
  默认值: 255
  最小值: 0
  最大值: 4294967295
- 
  序号: 3
  名称: OsPhysicalCoreIntCtrlPrioOrder
  长名称: ''
  描述: |
    This parameter is used to describe the interrupt priority interpretation.
    
    ASC: Higher values lead to higher priorities
    DESC: Lower values lead to higher priorities
  默认值: ASC
  最小值: ''
  最大值: ''
```

### 46. OsPhysicalCoreIntCtrlAddress

**描述**: Container to define a hardware specific address.

#### 参数列表

```yaml
- 
  序号: 1
  名称: OsPhysicalCoreIntCtrlAddressValue
  长名称: ''
  描述: This parameter specifies a hardware specific address value.
  默认值: 0
  最小值: 0
  最大值: 4294967295
```

### 47. OsPhysicalCoreIntCtrlSlaveConfig

**描述**: Container for interrupt controller cascading.
Mapping of configurable slave ports to physical master ports.


#### 参数列表

```yaml
- 
  序号: 1
  名称: OsPhysicalCoreIntCtrlMasterSource
  长名称: ''
  描述: This parameter specifies the physical master port of the interrupt controller.
  默认值: ''
  最小值: 0
  最大值: 4294967295
- 
  序号: 2
  名称: OsPhysicalCoreIntCtrlSlaveMinSource
  长名称: ''
  描述: This parameter specifies the lower limit of the slave port interval mapped to the physical
      port of the interrupt controller.
  默认值: ''
  最小值: 0
  最大值: 4294967295
- 
  序号: 3
  名称: OsPhysicalCoreIntCtrlSlaveMaxSource
  长名称: ''
  描述: This parameter specifies the upper limit of the slave port interval mapped to the physical
      port of the interrupt controller.
  默认值: ''
  最小值: 0
  最大值: 4294967295
```

### 48. OsPhysicalCoreMpu

**描述**: Container to structure all core memory protection unit attributes.

#### 参数列表

```yaml
- 
  序号: 1
  名称: OsPhysicalCoreMpuId
  长名称: ''
  描述: This parameter defines the physical Id of the core MPU.
  默认值: 0
  最小值: 0
  最大值: 4294967295
- 
  序号: 2
  名称: OsPhysicalCoreMpuType
  长名称: ''
  描述: Derivative specific type of the core MPU.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: OsPhysicalCoreMpuMaxRegions
  长名称: ''
  描述: This parameter specifies the maximum number of regions for the core MPU.
  默认值: 16
  最小值: 0
  最大值: 4294967295
```

### 49. OsPhysicalCoreMpuAddress

**描述**: Container to define a hardware specific address.

#### 参数列表

```yaml
- 
  序号: 1
  名称: OsPhysicalCoreMpuAddressValue
  长名称: ''
  描述: This parameter specifies a hardware specific address value.
  默认值: 0
  最小值: 0
  最大值: 4294967295
```

### 50. OsPhysicalCoreAddress

**描述**: Container to define a hardware specific address.

#### 参数列表

```yaml
- 
  序号: 1
  名称: OsPhysicalCoreAddressValue
  长名称: ''
  描述: This parameter specifies a hardware specific address value.
  默认值: 0
  最小值: 0
  最大值: 4294967295
```

### 51. OsHardwareTimer

**描述**: Derivative specific definition of a hardware timer module.

#### 参数列表

```yaml
- 
  序号: 1
  名称: OsHardwareTimerId
  长名称: ''
  描述: This parameter defines the physical Id of the hardware timer.
  默认值: 0
  最小值: 0
  最大值: 4294967295
- 
  序号: 2
  名称: OsHardwareTimerUnit
  长名称: ''
  描述: |
    Specifies the counting mode supported by the underlying hardware unit.
    FRT: A free running up counting timer.
    PIT: A periodic interrupt timer.
    FRTPIT: Hardware can be configured as PIT or FRT (e.g. via register flag).
  默认值: FRT
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: OsHardwareTimerType
  长名称: ''
  描述: Derivative specific type of the hardware timer.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: OsHardwareTimerSize
  长名称: ''
  描述: Derivative specific Bit size for the hardware timer.
  默认值: 32
  最小值: 4
  最大值: 32
- 
  序号: 5
  名称: OsHardwareTimerBaseAddress
  长名称: ''
  描述: Hardware specific base address of the timer module.
  默认值: 0
  最小值: 0
  最大值: 4294967295
```

### 52. OsHardwareTimerChannel

**描述**: Container to structure all hardware timer channel parameters.

#### 参数列表

```yaml
- 
  序号: 1
  名称: OsHardwareTimerChannelId
  长名称: ''
  描述: This parameter defines the physical Id of the hardware timer channel.
  默认值: 0
  最小值: 0
  最大值: 4294967295
- 
  序号: 2
  名称: OsHardwareTimerChannelIntSource
  长名称: ''
  描述: Specifies the hardware specific interrupt source number for the hardware timer channel.
  默认值: 0
  最小值: 0
  最大值: 4294967295
- 
  序号: 3
  名称: OsHardwareTimerChannelOffset
  长名称: ''
  描述: Specifies the offset from hardware timer unit base address (OsHardwareTimerBaseAddress) to
      timer channel register.
  默认值: 0
  最小值: 0
  最大值: 4294967295
```

### 53. OsHardwareTimerAddress

**描述**: Container to define a hardware specific address.

#### 参数列表

```yaml
- 
  序号: 1
  名称: OsHardwareTimerAddressValue
  长名称: ''
  描述: This parameter specifies a hardware specific address value.
  默认值: 0
  最小值: 0
  最大值: 4294967295
```

### 54. OsSystemIntCtrl

**描述**: Derivative specific definition of a system interrupt controller module.

#### 参数列表

```yaml
- 
  序号: 1
  名称: OsSystemIntCtrlType
  长名称: ''
  描述: Derivative specific type of the system interrupt controller.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: OsSystemIntCtrlMaxSources
  长名称: ''
  描述: |
    This parameter specifies the highest configurable interrupt source.
    
    Example: If the interrupt controller supports 1024 interrupt sources (0-1023), the highest
    configurable interrupt source is 1023.
  默认值: 999
  最小值: 0
  最大值: 4294967295
- 
  序号: 3
  名称: OsSystemIntCtrlMaxPrios
  长名称: ''
  描述: |
    This parameter specifies the highest configurable interrupt priority.
    
    Example: If an interrupt controller supports 64 priorities (0-63), the highest configurable
    priority is 63.
  默认值: 255
  最小值: 0
  最大值: 4294967295
- 
  序号: 4
  名称: OsSystemIntCtrlPrioOrder
  长名称: ''
  描述: |
    This parameter is used to describe the interrupt priority interpretation.
    
    ASC: Higher values lead to higher priorities
    DESC: Lower values lead to higher priorities
  默认值: ASC
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: OsSystemIntCtrlBaseAddress
  长名称: ''
  描述: Hardware specific base address of the system interrupt controller.
  默认值: 0
  最小值: 0
  最大值: 4294967295
```

### 55. OsSystemIntCtrlAddress

**描述**: Container to define a hardware specific address.

#### 参数列表

```yaml
- 
  序号: 1
  名称: OsSystemIntCtrlAddressValue
  长名称: ''
  描述: This parameter specifies a hardware specific address value.
  默认值: 0
  最小值: 0
  最大值: 4294967295
```

### 56. OsSystemIntCtrlSlaveConfig

**描述**: Container for interrupt controller cascading.
Mapping of configurable slave ports to physical master ports.


#### 参数列表

```yaml
- 
  序号: 1
  名称: OsSystemIntCtrlMasterSource
  长名称: ''
  描述: This parameter specifies the physical master port of the interrupt controller.
  默认值: ''
  最小值: 0
  最大值: 4294967295
- 
  序号: 2
  名称: OsSystemIntCtrlSlaveMinSource
  长名称: ''
  描述: This parameter specifies the lower limit of the slave port interval mapped to the physical
      port of the interrupt controller.
  默认值: ''
  最小值: 0
  最大值: 4294967295
- 
  序号: 3
  名称: OsSystemIntCtrlSlaveMaxSource
  长名称: ''
  描述: This parameter specifies the upper limit of the slave port interval mapped to the physical
      port of the interrupt controller.
  默认值: ''
  最小值: 0
  最大值: 4294967295
```

### 57. OsSystemMpu

**描述**: Derivative specific definition of a system memory protection unit.

#### 参数列表

```yaml
- 
  序号: 1
  名称: OsSystemMpuId
  长名称: ''
  描述: This parameter defines the physical Id of the system MPU.
  默认值: 0
  最小值: 0
  最大值: 4294967295
- 
  序号: 2
  名称: OsSystemMpuType
  长名称: ''
  描述: Derivative specific type of the system MPU.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: OsSystemMpuMaxRegions
  长名称: ''
  描述: This parameter specifies the maximum number of regions for the system MPU.
  默认值: 16
  最小值: 0
  最大值: 4294967295
- 
  序号: 4
  名称: OsSystemMpuBaseAddress
  长名称: ''
  描述: Hardware specific base address of the system MPU.
  默认值: 0
  最小值: 0
  最大值: 4294967295
```

### 58. OsSystemMpuAddress

**描述**: Container to define a hardware specific address.

#### 参数列表

```yaml
- 
  序号: 1
  名称: OsSystemMpuAddressValue
  长名称: ''
  描述: This parameter specifies a hardware specific address value.
  默认值: 0
  最小值: 0
  最大值: 4294967295
```

### 59. OsMemoryRegionSpecifics

**描述**: Derivative specific settings for a memory protection region.

该容器没有参数。

### 60. OsMemoryRegionAccess

#### 参数列表

```yaml
- 
  序号: 1
  名称: OsMemoryRegionAccessRights
  长名称: ''
  描述: |
    Defines the access rights for a memory protection region.
    
    NONE: No access rights
    R: Read access rights
    W: Write access rights
    X: Execution access rights
  默认值: NONE
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: OsMemoryRegionAccessType
  长名称: ''
  描述: Defines the access type for a memory protection region.
  默认值: SUPERVISOR
  最小值: ''
  最大值: ''
```

### 61. OsMemoryRegionBusMaster

**描述**: Defines a derivative specific bus master for a memory protection region.

#### 参数列表

```yaml
- 
  序号: 1
  名称: OsMemoryRegionBusMasterId
  长名称: ''
  描述: This parameter defines the physical Id of the memory region bus master.
  默认值: 0
  最小值: 0
  最大值: 4294967295
```

### 62. OsMemoryRegionFlag

**描述**: Defines a derivative specific memory protection region flag.

e.g. Debug, Cachable, ...

该容器没有参数。

### 63. OsMemoryRegionDefaults

**描述**: Default settings for automatically created OsMemoryRegions.

#### 参数列表

```yaml
- 
  序号: 1
  名称: OsMemoryRegionDefType
  长名称: ''
  描述: This parameter defines for which type of MPU region these default values shall be used.
  默认值: APPLICATION_TRUSTED
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: OsMemoryRegionDefIdentifier
  长名称: ''
  描述: Optional default value for OsMemoryRegionIdentifier.
  默认值: 0
  最小值: 0
  最大值: 4294967295
- 
  序号: 3
  名称: OsMemoryRegionDefProtectionUnitSlot
  长名称: ''
  描述: Optional default value for OsMemoryRegionProtectionUnitSlot.
  默认值: 0
  最小值: 0
  最大值: 4294967295
- 
  序号: 4
  名称: OsMemoryRegionDefAccessRights
  长名称: ''
  描述: Optional default values for OsMemoryRegionAccessRights.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: OsMemoryRegionDefFlags
  长名称: ''
  描述: Optional default references for OsMemoryRegionFlags.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: OsMemoryRegionDefBusMasters
  长名称: ''
  描述: Optional default references for OsMemoryRegionBusMasters.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 64. OsInterruptSupportedType

**描述**: Defines the derivative specific supported interrupt types.

#### 参数列表

```yaml
- 
  序号: 1
  名称: OsInterruptSupportedTypeSeparateSources
  长名称: ''
  描述: |
    This parameter defines whether the interrupt type (e.g. FIQ) has separate sources or not.
    
    true: The interrupt type has its own sources.
    false: Interrupt sources shall be unique independent from the type.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: OsInterruptSupportedTypeSeparatePriority
  长名称: ''
  描述: |
    This parameter defines whether the interrupt type (e.g. DMA) has a separate priority or not.
    
    true: The interrupt type has its own priority.
    false: The priority value needs to be validated according to interrupt category settings.
  默认值: false
  最小值: ''
  最大值: ''
```

### 65. OsResource

**描述**: An OsResource object is used to co-ordinate the concurrent access by tasks and ISRs to a shared
resource, e.g. the scheduler, any program sequence, memory or any hardware area.

#### 参数列表

```yaml
- 
  序号: 1
  名称: OsResourceProperty
  长名称: ''
  描述: This specifies the type of the resource.
  默认值: STANDARD
  最小值: ''
  最大值: ''
```

### 66. OsScheduleTable

**描述**: An OsScheduleTable addresses the synchronization issue by providing an encapsulation of a statically
defined set of alarms that cannot be modified at runtime.

#### 参数列表

```yaml
- 
  序号: 1
  名称: OsScheduleTableDuration
  长名称: ''
  描述: This parameter defines the modulus of the schedule table (in ticks).
  默认值: 1073741823
  最小值: 0
  最大值: 4294967295
- 
  序号: 2
  名称: OsScheduleTableRepeating
  长名称: ''
  描述: |
    true: First expiry point on the schedule table shall be processed at final expiry point delay
    ticks after the final expiry point is processed.
    false: The schedule table processing stops when the final expiry point is processed.
  默认值: false
  最小值: ''
  最大值: ''
```

### 67. OsScheduleTableAutostart

**描述**: This container specifies if and how the schedule table is started on startup of the Operating
System. The options to start a schedule table correspond to the API calls to start schedule tables
during runtime.

#### 参数列表

```yaml
- 
  序号: 1
  名称: OsScheduleTableAutostartType
  长名称: ''
  描述: This specifies the type of the autostart for the schedule table.
  默认值: ABSOLUTE
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: OsScheduleTableStartValue
  长名称: ''
  描述: Absolute autostart tick value when the schedule table starts. Only used if the
      OsScheduleTableAutostartType is ABSOLUTE.
  默认值: 0
  最小值: 0
  最大值: 4294967295
```

### 68. OsScheduleTableExpiryPoint

**描述**: The point on a Schedule Table at which the OS activates tasks and/or sets events.

#### 参数列表

```yaml
- 
  序号: 1
  名称: OsScheduleTblExpPointOffset
  长名称: ''
  描述: The offset from zero (in ticks) at which the expiry point is to be processed.
  默认值: ''
  最小值: 0
  最大值: 4294967295
```

### 69. OsScheduleTableEventSetting

**描述**: Event that is triggered by that schedule table.

该容器没有参数。

### 70. OsScheduleTableTaskActivation

**描述**: Task that is triggered by that schedule table.

该容器没有参数。

### 71. OsScheduleTblAdjustableExpPoint

**描述**: Adjustable expiry point.

#### 参数列表

```yaml
- 
  序号: 1
  名称: OsScheduleTableMaxLengthen
  长名称: ''
  描述: The maximum positive adjustment that can be made to the expiry point offset (in ticks).
  默认值: ''
  最小值: 0
  最大值: 4294967295
- 
  序号: 2
  名称: OsScheduleTableMaxShorten
  长名称: ''
  描述: The maximum negative adjustment that can be made to the expiry point offset (in ticks).
  默认值: ''
  最小值: 0
  最大值: 4294967295
```

### 72. OsScheduleTableSync

**描述**: This container specifies the synchronization parameters of the schedule table.

#### 参数列表

```yaml
- 
  序号: 1
  名称: OsScheduleTblExplicitPrecision
  长名称: ''
  描述: This configuration is only valid if the explicit synchronization is used (in ticks).
  默认值: 0
  最小值: 0
  最大值: 4294967295
- 
  序号: 2
  名称: OsScheduleTblSyncStrategy
  长名称: ''
  描述: AUTOSAR OS provides support for synchronization in two ways: explicit and implicit.
  默认值: NONE
  最小值: ''
  最大值: ''
```

### 73. OsSpinlock

**描述**: An OsSpinlock object is used to co-ordinate concurrent access by tasks and category 2 ISRs on
different cores to a shared resource.

#### 参数列表

```yaml
- 
  序号: 1
  名称: OsSpinlockLockMethod
  长名称: ''
  描述: Lock method which is used when a spinlock is taken. Note that it is possible that a user (e.g.
      a Task) might hold more than one spinlock. In this case the last lock taken is forced to
      use at least a lock methode which locks as strong as the current one.
  默认值: LOCK_CAT2_INTERRUPTS
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: OsSpinlockLockType
  长名称: ''
  描述: |
    Allows to select an optimized fast way for spinlock administration.
    
    STANDARD: Standard AUTOSAR implementation
    OPTIMIZED: Fast optimized MICROSAR OS implementation
  默认值: STANDARD
  最小值: ''
  最大值: ''
```

### 74. OsTask

**描述**: This container represents a task.

#### 参数列表

```yaml
- 
  序号: 1
  名称: OsTaskActivation
  长名称: ''
  描述: This attribute defines the maximum number of queued activation requests for the task. A value
      equal to "1" means that at any time only a single activation is permitted for this task.
      Note that the value must be a natural number starting at 1.
  默认值: 1
  最小值: 1
  最大值: 255
- 
  序号: 2
  名称: OsTaskPriority
  长名称: ''
  描述: |
    The priority of a task is defined by the value of this attribute. This value has to be
    understood as a relative value, i.e. the values show only the relative ordering of the tasks.
    
    Note: The generator has a special treatment for the idle task. The idle task has the virtual
    priority 0xFFFFFFFF to differentiate it from regular tasks. It will be generated to have the
    lowest priority, even if there are tasks configured with priority 0.
  默认值: 0
  最小值: 0
  最大值: 4294967295
- 
  序号: 3
  名称: OsTaskSchedule
  长名称: ''
  描述: The OsTaskSchedule attribute defines the preemptability of the task.
  默认值: FULL
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: OsTaskMemoryProtectionIdentifier
  长名称: ''
  描述: |
    This optional parameter can be used to specify a memory protection identifier for the task.
    
    If this parameter is not set but the owner OS-Application has a memory protection identifier
    specified this value will be used for the task.
  默认值: 0
  最小值: 0
  最大值: 4294967295
- 
  序号: 5
  名称: OsTaskStackSharing
  长名称: ''
  描述: |
    Specifies whether the task shall share a stack with other basic tasks or not.
    Basic tasks with same priority always share a stack independently from this parameter.
    For detailed information about task stack sharing please refer to the TechnicalReference_Os.pdf
    chapter "Task Stack Sharing".
    
    true: The task is enabled for additional stack sharing.
    false: The task is not marked for additional stack sharing.
    
    Attention:
    Basic tasks which have this attribute set to TRUE must never call the OS service Schedule().
    
    Note:
    For shared stacks the biggest configured size will be used to set up the stack size.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: OsTaskStackSize
  长名称: ''
  描述: This attribute specifies the stack size of the task in bytes.
  默认值: 1024
  最小值: 0
  最大值: 4294967295
- 
  序号: 7
  名称: OsTaskType
  长名称: ''
  描述: |
    This parameter specifies the type of task. If AUTO (should be used) the type is calculated
    automatically from other parameters.
    
    It is possible to preselect the type, if there are restrictions to use a special task type. An
    error message is created if there are differences between the preselected and the calculated
    task type.
  默认值: AUTO
  最小值: ''
  最大值: ''
- 
  序号: 8
  名称: OsTaskUsesFpu
  长名称: ''
  描述: |
    This parameter is used to specify if this task uses the FPU unit.
    
    This parameter only takes effect, if the parameter /MICROSAR/Os/OsOS/OsFpuUsage is set to
    "INDIVIDUAL".
  默认值: false
  最小值: ''
  最大值: ''
```

### 75. OsTaskAutostart

**描述**: This container determines whether the task is activated during the system start-up procedure or not
for some specific application modes.

该容器没有参数。

### 76. OsTaskTimingProtection

**描述**: This container contains all parameters regarding timing protection of the task.

Timing protection is only allowed if OS scalability class is set to SC2 or SC4.

#### 参数列表

```yaml
- 
  序号: 1
  名称: OsTaskAllInterruptLockBudget
  长名称: ''
  描述: This parameter contains the maximum time for which the task is allowed to lock all interrupts
      (via SuspendAllInterrupts() or DisableAllInterrupts()) (in seconds).
  默认值: 0
  最小值: 0
  最大值: 4294967295
- 
  序号: 2
  名称: OsTaskExecutionBudget
  长名称: ''
  描述: This parameter contains the maximum allowed execution time of the task (in seconds).
  默认值: 0
  最小值: 0
  最大值: 4294967295
- 
  序号: 3
  名称: OsTaskOsInterruptLockBudget
  长名称: ''
  描述: This parameter contains the maximum time for which the task is allowed to lock all Category 2
      interrupts (via SuspendOSInterrupts()) (in seconds).
  默认值: 0
  最小值: 0
  最大值: 4294967295
- 
  序号: 4
  名称: OsTaskTimeFrame
  长名称: ''
  描述: The minimum inter-arrival time between activations and/or releases of a task (in seconds).
  默认值: ''
  最小值: 0
  最大值: 4294967295
```

### 77. OsTaskResourceLock

**描述**: This container contains the worst case time between getting and releasing a given resource (in
seconds).

#### 参数列表

```yaml
- 
  序号: 1
  名称: OsTaskResourceLockBudget
  长名称: ''
  描述: This parameter contains the maximum time the task is allowed to lock the resource (in
      seconds).
  默认值: 0
  最小值: 0
  最大值: 4294967295
```

### 78. OsTaskRoundRobinScheduling

**描述**: This container holds the parameter needed for round robin scheduling.
If this container exists for a task, the task is considered to participate in round robin
scheduling.
If a task has this container configured, all tasks on the same core with the same priority shall
also have this container configured
(So round robin scheduling has either to be used for all tasks of a specific priority or for none of
these).


#### 参数列表

```yaml
- 
  序号: 1
  名称: OsTaskNumScheduleEventsRoundRobin
  长名称: ''
  描述: Defines the number of TimeSlices this task may consume.
  默认值: 1
  最小值: 1
  最大值: 4294967295
```

