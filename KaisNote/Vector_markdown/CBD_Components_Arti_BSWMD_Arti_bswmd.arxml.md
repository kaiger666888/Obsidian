# Arti

## 模块描述

The Arti Module serves as a superordinate container collecting all information and parameters
concerning ARTI.

## 容器列表

### 1. ArtiGeneric

**描述**: The ArtiGeneric container contains definitions for generic objects, i.e. not belonging to a standard
AUTOSAR module.

该容器没有参数。

### 2. ArtiGenericComponentClass

**描述**: The class definition describes the layout of the object (similar to a "class" definition in C++).

#### 参数列表

```yaml
- 
  序号: 1
  名称: ArtiGenericComponentClassName
  长名称: ''
  描述: Name of the class.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 3. ArtiGenericComponentClassParameter

**描述**: Parameter definition of a class.

#### 参数列表

```yaml
- 
  序号: 1
  名称: ArtiGenericComponentClassParameterName
  长名称: ''
  描述: Name of the parameter.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 4. ArtiGenericComponentInstance

**描述**: The instance definition describes a specific instantiated object.

#### 参数列表

```yaml
- 
  序号: 1
  名称: ArtiGenericComponentInstanceName
  长名称: ''
  描述: Name of the instance.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 5. ArtiGenericComponentInstanceParameter

**描述**: Parameter definition of an instance.

该容器没有参数。

### 6. ArtiHardware

**描述**: The ArtiHardware container contains ARTI extensions to the EcucHardware module.

该容器没有参数。

### 7. ArtiHardwareCoreClass

**描述**: Contains the layout of an ARTI "Core" object, extending the EcucCoreDefinition.

该容器没有参数。

### 8. ArtiHardwareCoreInstance

**描述**: Description: Represents an instance of an ARTI "Core" object, extending the EcucCoreDefinition. When
using ARTI for debugging or hardware based tracing, this is mandatory (i.e. multiplicity 1..*), else
optional.

#### 参数列表

```yaml
- 
  序号: 1
  名称: ArtiHardwareCoreInstanceCoreId
  长名称: ''
  描述: This parameter represents the "CoreID" as given by the OS, returned by GetCoreID().
  默认值: ''
  最小值: 0
  最大值: 18446744073709551615
```

### 9. ArtiOs

**描述**: The ArtiOs container contains ARTI extensions to the EcucDefs/Os module.

该容器没有参数。

### 10. ArtiOsAlarmClass

**描述**: Contains the layout of an ArtiOsAlarm object.

该容器没有参数。

### 11. ArtiOsAlarmInstance

**描述**: Represents an instance of an ArtiOsAlarm object, extending the EcuC OsTaskAlarm.

#### 参数列表

```yaml
- 
  序号: 1
  名称: ArtiOsAlarmInstanceAction
  长名称: ''
  描述: This attribute provides a string with a description of the action when the alarm expires, e.g.
      "ActivateTask TaskA".
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: ArtiOsAlarmInstanceCounter
  长名称: ''
  描述: This attribute provides a string containing the name of the counter used by this alarm.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 12. ArtiOsClass

**描述**: Contains the layout of an ARTI "Os" object, extending the EcuC OsOS.

该容器没有参数。

### 13. ArtiOsContextClass

**描述**: Contains the layout of an ARTI "OsContext" object.

该容器没有参数。

### 14. ArtiOsContextInstance

**描述**: Represents an instance of an "ArtiContext" object.

该容器没有参数。

### 15. ArtiOsInstance

**描述**: Represents an instance of an ARTI "Os" object, extending the EcuC OsOS.

该容器没有参数。

### 16. ArtiOsIsrClass

**描述**: Contains the layout of an ARTI "OsIsr" object, extending the EcuC OsIsr.

该容器没有参数。

### 17. ArtiOsIsrInstance

**描述**: Represents an instance of an ARTI "OsIsr" object, extending the EcuC OsIsr.

#### 参数列表

```yaml
- 
  序号: 1
  名称: ArtiOsIsrInstanceCategory
  长名称: ''
  描述: Specifies category of this ISR. If omitted the instance is related to a CATEGORY_2.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: ArtiOsIsrInstanceFunction
  长名称: ''
  描述: This parameter represents the C function name of the ISR routine.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: ArtiOsIsrInstanceId
  长名称: ''
  描述: This parameter represents the "ISRID" as given by the OS, returned by GetISRID().
  默认值: ''
  最小值: 0
  最大值: 18446744073709551615
```

### 18. ArtiOsMessageContainerClass

**描述**: Contains the layout of an ARTI "OsMessageContainer" object. The "OsMessageContainer" object
represents an existing combination of OSEK messages.

该容器没有参数。

### 19. ArtiOsMessageContainerInstance

**描述**: Represents an instance of an "ArtiMessageContainer" object.

#### 参数列表

```yaml
- 
  序号: 1
  名称: ArtiOsMessageContainerInstanceMsgName
  长名称: ''
  描述: This attribute provides the name of the message as defined in OIL file.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: ArtiOsMessageContainerInstanceMsgType
  长名称: ''
  描述: This attribute provides the type of the message.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 20. ArtiOsResourceClass

**描述**: Contains the layout of an ArtiOsResource object. The ArtiOsResource object represents an OSEK
resource.

该容器没有参数。

### 21. ArtiOsResourceInstance

**描述**: Represents an instance of an ArtiOsResource object.

#### 参数列表

```yaml
- 
  序号: 1
  名称: ArtiOsResourceInstancePriority
  长名称: ''
  描述: This attribute has two components that state: that the RESOURCE is used by TASKs only or by
      TASKs and ISRs, and the priority that will be used when locking the RESOURCE.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 22. ArtiOsStackClass

**描述**: Contains the layout of an ArtiOsStack object. The ArtiOsStack object defines the memory area of any
stack in the system.

该容器没有参数。

### 23. ArtiOsStackInstance

**描述**: Represents an instance of an ArtiOsStack object.

#### 参数列表

```yaml
- 
  序号: 1
  名称: ArtiOsStackInstanceDirection
  长名称: ''
  描述: This attribute specifies the direction of stack growth and may have either "UP" or "DOWN" as
      its value. UP means growing from lower to higher addresses. DOWN means growing from
      higher addresses to lower addresses.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 24. ArtiOsTaskClass

**描述**: Contains the layout of an ARTI "OsTask" object, extending the EcuC OsTask.

该容器没有参数。

### 25. ArtiOsTaskInstance

**描述**: Represents an instance of an ARTI "OsTask" object, extending the EcuC OsTask.

#### 参数列表

```yaml
- 
  序号: 1
  名称: ArtiOsTaskInstanceFunction
  长名称: ''
  描述: This parameter represents the C function name of the task body.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: ArtiOsTaskInstanceId
  长名称: ''
  描述: This parameter represents the "TaskID" as given by the OSEK OS, returned by GetTaskID().
  默认值: ''
  最小值: 0
  最大值: 18446744073709551615
```

### 26. ArtiRte

**描述**: The ArtiRte Container contains all parameters for ARTI that are filled by the generators RTE.

该容器没有参数。

### 27. ArtiRteRunnableClass

**描述**: Contains the layout of an ArtiRteRunnable object.

该容器没有参数。

### 28. ArtiRteRunnableInstance

**描述**: Represents an instance of an ArtiRteRunnable object, extending the BswM RunnableEntity.

#### 参数列表

```yaml
- 
  序号: 1
  名称: ArtiRteRunnableInstanceSymbol
  长名称: ''
  描述: Specifies the symbol / function name that implements the runnable.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 29. ArtiRteSchedulableClass

**描述**: Contains the layout of an ArtiRteSchedulable object.

该容器没有参数。

### 30. ArtiRteSchedulableInstance

**描述**: Represents an instance of an ArtiRteSchedulable object, extending the Rte Schedulable Entity.

#### 参数列表

```yaml
- 
  序号: 1
  名称: ArtiRteSchedulableInstanceSymbol
  长名称: ''
  描述: Specifies the symbol / function name that implements the schedulable.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 31. ArtiRteVfbTraceHooks

**描述**: This container defines the parent container to which all trace hook containers are added.

该容器没有参数。

### 32. RteVfbTraceHook

**描述**: This container represents a specific VFB Trace hook. Its ShortName equals the hook function's C
symbol.

#### 参数列表

```yaml
- 
  序号: 1
  名称: RteVfbTraceHookType
  长名称: ''
  描述: This specifies the type of the hook.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 33. RteVfbTraceHookAccessPoint

**描述**: In case of an RTE API Trace hook the ShortName of this container is the Access Point name part of
the VFB Trace hook (<ap> in SWS_Rte).

该容器没有参数。

### 34. RteVfbTraceHookApi

**描述**: In case of a BSW Scheduler API Trace hook or RTE API Trace hook the ShortName of this container is
the API name part of the VFB Trace hook (<api> in SWS_Rte).

该容器没有参数。

### 35. RteVfbTraceHookBswSchedulerNamePrefix

**描述**: In case of a BSW Scheduler API Trace hook or BSW Schedulable Entities Trace hook the ShortName of
this container is the BSW Scheduler Name Prefix name part of the VFB Trace hook (<bsnp> in SWS_Rte).

该容器没有参数。

### 36. RteVfbTraceHookComHookEvent

**描述**: In case of a COM Trace hook the ShortName of this container is the COM hook event part of the VFB
Trace hook (<Event> in SWS_Rte).

该容器没有参数。

### 37. RteVfbTraceHookComponentTypeSymbol

**描述**: In case of an RTE API Trace hook, Runnable Entity Trace hook or RPT Trace hook the ShortName of this
container is the component type symbol name part of the VFB Trace hook (<cts> in SWS_Rte).

该容器没有参数。

### 38. RteVfbTraceHookExecutableEntityName

**描述**: In case of a Runnable Entity Trace hook or BSW Schedulable Entities Trace hook the ShortName of this
container is the Executable Entity name part of the VFB Trace hook (<reName> or <entityName> in
SWS_Rte).

该容器没有参数。

### 39. RteVfbTraceHookName

**描述**: In case of a BSW Scheduler API Trace hook the ShortName of this container is the "Name provided by
the API" name part of the VFB Trace hook (<name> in SWS_Rte).

该容器没有参数。

### 40. RteVfbTraceHookOsApplication

**描述**: In case of an OS Trace hook the ShortName of this container is the application name part of the VFB
Trace hook (<application> in SWS_Rte).

该容器没有参数。

### 41. RteVfbTraceHookSignal

**描述**: In case of a COM Trace hook the ShortName of this container is the COM signal name part of the VFB
Trace hook (<signalName> in SWS_Rte).

该容器没有参数。

### 42. RteVfbTraceHookSignalGroup

**描述**: In case of a COM Trace hook the ShortName of this container is the COM signal group name part of the
VFB Trace hook (<signalGroupName> in SWS_Rte).

该容器没有参数。

### 43. RteVfbTraceHookTask

**描述**: In case of an OS Trace hook the ShortName of this container is the task name part of the VFB Trace
hook (<task> in SWS_Rte).

该容器没有参数。

### 44. RteVfbTraceHookVariable

**描述**: In case of an RPT Trace hook the ShortName of this container is the "identifying name of the RP
global buffer" name part of the VFB Trace hook (<var> in SWS_Rte).

该容器没有参数。

### 45. RteVfbTraceHookVendorApiInfix

**描述**: In case of a BSW Scheduler API Trace hook or BSW Schedulable Entities Trace hook the ShortName of
this container is the optional VendorApiInfix name part of the VFB Trace hook (<ai> in SWS_Rte).

该容器没有参数。

### 46. RteVfbTraceHookVendorId

**描述**: In case of a BSW Scheduler API Trace hook or BSW Schedulable Entities Trace hook the ShortName of
this container is the optional VendorId name part of the VFB Trace hook (<vi> in SWS_Rte).

#### 参数列表

```yaml
- 
  序号: 1
  名称: RteVfbTraceHookVendorIdIntegerValue
  长名称: ''
  描述: |
    The VendorId as Integer parameter.
    
    This parameter is an extension to ECUC_Rte_09188.
    It is required to work around an AUTOSAR inconsistency:
      - AUTOSAR defines the VendorId as Integer value
      - AUTOSAR defines that shortnames shall not begin with an Integer.
    Therefore, it is impossible to pass the VendorId as shortname of the container.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 47. ArtiValues

**描述**: The ArtiValues container collects all parameter values for ARTI that are filled by the generators
(OS, RTE, ...)

该容器没有参数。

### 48. ArtiConstant

**描述**: This container holds a constant value.

#### 参数列表

```yaml
- 
  序号: 1
  名称: ArtiConstantString
  长名称: ''
  描述: This is the constant value for a specific parameter.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 49. ArtiExpression

**描述**: This container holds a C like expression that a debugger can evaluate. This is similar to what is
already done in ORTI.

#### 参数列表

```yaml
- 
  序号: 1
  名称: ArtiExpressionString
  长名称: ''
  描述: This string represents a C like expression that a debugger can evaluate.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 50. ArtiHook

**描述**: This container represents an ARTI hook that is present in the module.

#### 参数列表

```yaml
- 
  序号: 1
  名称: ArtiHookClass
  长名称: ''
  描述: Name of the (schedule) class of macros. Classes can be one of the predefined classes or user
      defined.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: ArtiHookContext
  长名称: ''
  描述: Name of the execution context. One of NOSUSP, SPRVSR, or USER.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: ArtiHookEventName
  长名称: ''
  描述: The name of the event as defined for a particular class, or an arbitrary name for generic
      classes.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: ArtiHookInstance
  长名称: ''
  描述: Name of an instance of the (schedule) class.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: ArtiHookOnlyDeclarationNeeded
  长名称: ''
  描述: This parameter should be set to true in case the calling component never calls the hook with
      the configured parameter values but needs the respective identifiers declared. If this
      parameter is set to false ARTI expects that the hook is called with the configured
      parameter values.
  默认值: false
  最小值: ''
  最大值: ''
```

### 51. ArtiObjectClassParameter

**描述**: This container represents a parameter of an Arti object class definition.

该容器没有参数。

### 52. ArtiObjectInstanceParameter

**描述**: This container represents a parameter of an Arti object instance.

该容器没有参数。

### 53. ArtiParameterTypeMap

**描述**: A map of key/value pairs to map a parameter value to a display string and/or an Arti or EcuC object.

该容器没有参数。

### 54. ArtiParameterTypeMapPair

**描述**: A key/value pair to map a parameter value to a display string and/or an Arti or EcuC object.

#### 参数列表

```yaml
- 
  序号: 1
  名称: ArtiParameterTypeMapPairInput
  长名称: ''
  描述: The numerical value given by a parameter to translate.
  默认值: ''
  最小值: 0
  最大值: 65535
- 
  序号: 2
  名称: ArtiParameterTypeMapPairOutput
  长名称: ''
  描述: The string to display for the Input value.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 55. ArtiStates

**描述**: This container contains all states of tasks, isrs... that the EcuC uses.

#### 参数列表

```yaml
- 
  序号: 1
  名称: ArtiStatesTaskEnhanced
  长名称: ''
  描述: Set to true, if the OS provides an "enhanced" state model with "READY" split to "Activated",
      "Preempted", "Released".
  默认值: ''
  最小值: ''
  最大值: ''
```

### 56. ArtiStatesTaskState

**描述**: Each state used by the OS has to be listed as ArtiStatesTaskState Parameter with a choice of the
states.

#### 参数列表

```yaml
- 
  序号: 1
  名称: ArtiStatesTaskStateEnum
  长名称: ''
  描述: ArtiStatesTaskState choice of the states.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 57. ArtiGeneral

**描述**: General configuration parameters of ARTI.

#### 参数列表

```yaml
- 
  序号: 1
  名称: ArtiDevErrorDetect
  长名称: ''
  描述: |
    This parameter switches the Development Error Detection and Notification ON or OFF.
    
    true: Development error detection is enabled.
    false: Development error detection is disabled.
    
    Note: In general, the development error detection is recommended during pre-test phase. It is
    not recommended to enable the development error detection in production code due to increased
    runtime and ROM needs.
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: ArtiSafeBswChecks
  长名称: ''
  描述: Selects whether safety checks are used. These checks improve robustness as e.g. invalid
      parameter values are detected before a function is executed. This attribute has to be
      enabled for safety projects where this component is mapped to an ASIL partition.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: ArtiMacroAccessIncludeHeader
  长名称: ''
  描述: |
    Specifies the name of the header file containing the definition of the macro
    ARTI_WRITE_TRACE_HOOK_VAR(variableName, variableValue).
    This macro is called for all ArtiHookTraceVariable with an ArtiHookTraceVariableAccessType of
    "Macro".
    
    Note:
    Insert the complete filename including the extension (e.g. MyHeader.h).
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: ArtiEnableVfbTraceClient
  长名称: ''
  描述: |
    Selects whether the Arti Vfb Trace Client is enabled or disabled.
    When the client is enabled, the Arti module will generate the configured Rte Vfb Trace Hooks and
    register Arti as a Vfb Trace Client in the RTE.
    
  默认值: false
  最小值: ''
  最大值: ''
```

### 58. ArtiHookTraceVariable

**描述**: Holds the configuration of a hook trace variable. These variables provide information on hook
parameters to an external debugging or tracing tool.

Note:
The prefix "Arti_" is added to the name of the hook trace variable in all generated files.

#### 参数列表

```yaml
- 
  序号: 1
  名称: ArtiHookTraceVariableAccessType
  长名称: ''
  描述: |
    Specifies in which way the trace variable is accessed.
    
    Direct:
    The trace variable will be accessed directly.
    
    Macro:
    The trace variable will be accessed using the ARTI_WRITE_TRACE_HOOK_VAR macro.
    This allows the implementation of further steps like signaling an event or writing the value
    directly into a register.
    Note: In this case the header that defines the macro must be specified in
    /MICROSAR/Arti/ArtiGeneral/ArtiMacroAccessIncludeHeader.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 59. ArtiHookTraceVariableCondition

**描述**: This container holds the different conditions of the trace variable. Hooks with matching parameter
values will use this variable for writing their information.

#### 参数列表

```yaml
- 
  序号: 1
  名称: ArtiHookConditionPart
  长名称: ''
  描述: |
    This parameter is used to configure which hook parameter shall be taken as a condition.
    The hook trace variable will be written, if the respective hook parameters match the values
    configured at:
    /MICROSAR/Arti/ArtiHookTraceVariable/ArtiHookTraceVariableCondition/ArtiHookConditionStringValue.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: ArtiHookConditionStringValue
  长名称: ''
  描述: |
    This parameter specifies the string value corresponding to the configuration in:
    /MICROSAR/Arti/ArtiHookTraceVariable/ArtiHookTraceVariableCondition/ArtiHookConditionPart.
    The string value is compared against the respective hook parameter value. The hook trace
    variable will only be written in case of equality.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 60. ArtiHookTraceVariableIndex

**描述**: This sub-container shall be added to the hook trace variable configuration in case it shall be an
array variable.

#### 参数列表

```yaml
- 
  序号: 1
  名称: ArtiHookIndexPart
  长名称: ''
  描述: |
    Specifies the hook parameter that will be used as the array index. Currently, only
    HookInstanceParameter is supported.
    Mind that ARTI needs to know the value range. Therefore, the respective
    ArtiHookInstanceParameterTypeRef needs to be configured.
  默认值: HookInstanceParameter
  最小值: ''
  最大值: ''
```

### 61. ArtiHookTraceVariablePart

**描述**: This container configures a part of a hook trace variable. The parameters in this container
configure which hook parameters shall be stored at which start bit and with which size.

#### 参数列表

```yaml
- 
  序号: 1
  名称: ArtiHookPartPart
  长名称: ''
  描述: |
    Specifies the content that is stored in the part:
    
    HookContext:
    Stores an ID corresponding to the Context of the Hook.
    
    HookClass:
    Stores an ID corresponding to the Class of the Hook.
    
    HookEventName:
    Stores an ID corresponding to the EventName of the Hook.
    
    HookInstance:
    Stores an ID corresponding to the Instance of the Hook.
    
    HookEventParameter:
    Stores the event parameter of the Hook.
    
    HookInstanceParameter:
    Stores the instance parameter of the Hook.
    
    One:
    Stores one bits.
    
    Zero:
    Stores zero bits.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: ArtiHookStartBit
  长名称: ''
  描述: |
    Specifies the bit of the trace variable that the part starts at where 0 is considered to be the
    least significant bit.
    
    Note: ArtiHookStartBit + ArtiHookBitCount has to be smaller than or equal to 32
  默认值: ''
  最小值: 0
  最大值: 31
- 
  序号: 3
  名称: ArtiHookBitCount
  长名称: ''
  描述: |
    Specifies the number of bits that the part uses in the trace variable.
    
    Note: ArtiHookStartBit + ArtiHookBitCount has to be smaller than or equal to 32
  默认值: ''
  最小值: 1
  最大值: 32
```

