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

**描述**: The class definition describes the layout of the object (similar to a "class" definition in C).

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

### 31. ArtiValues

**描述**: The ArtiValues container collects all parameter values for ARTI that are filled by the generators
(OS, RTE, ...)

该容器没有参数。

### 32. ArtiConstant

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

### 33. ArtiExpression

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

### 34. ArtiHook

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
```

### 35. ArtiObjectClassParameter

**描述**: This container represents a parameter of an Arti object class definition.

该容器没有参数。

### 36. ArtiObjectInstanceParameter

**描述**: This container represents a parameter of an Arti object instance.

该容器没有参数。

### 37. ArtiParameterTypeMap

**描述**: A map of key/value pairs to map a parameter value to a display string and/or an Arti or EcuC object.

该容器没有参数。

### 38. ArtiParameterTypeMapPair

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

### 39. ArtiStates

**描述**: This container contains all states of tasks, isrs... that the EcuC uses.

该容器没有参数。

### 40. ArtiStatesTaskState

**描述**: Each state used by the OS has to be listed as ArtiStatesTaskState Parameter with a choice of the
states.

#### 参数列表

```yaml
- 
  序号: 1
  名称: ArtiStatesTaskStateEnhanced
  长名称: ''
  描述: Set to true, if the OS provides an "enhanced" state model with "READY" split to "Activated",
      "Preempted", "Released".
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: ArtiStatesTaskStateEnum
  长名称: ''
  描述: ArtiStatesTaskState choice of the states.
  默认值: ''
  最小值: ''
  最大值: ''
```

