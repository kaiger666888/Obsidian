# vFsmLib

## 模块描述

Vector Finite State Machine Library. The vFsmLib is used to configure and execute user defined
finite state machines (FSM).
The behavior of vFsmLib is based on concept of "Behavior State Machines" as described in the UML
specification.
#Library
#Vector

## 容器列表

### 1. vFsmLibGeneral

**描述**: General configuration parameters of the vFsmLib.

#### 参数列表

```yaml
- 
  序号: 1
  名称: vFsmLibDevErrorDetect
  长名称: ''
  描述: |
    Switches the Development Error Detection and Notification ON or OFF.
    
    true:   Development error detection is enabled.
    false:  Development error detection is disabled.
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: vFsmLibAdditionalIncludes
  长名称: ''
  描述: Definition of additional include files.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: vFsmLibMaxHierarchyDepth
  长名称: ''
  描述: |
    Definition of the maximum hierarchy depth for group transitions and transition paths.
    
    Can be reduced to optimize RAM usage.
  默认值: 8
  最小值: 1
  最大值: 255
- 
  序号: 4
  名称: vFsmLibStateBaseType
  长名称: ''
  描述: |
    Definition of the base type for vFsmLibStateType. It affects the maximum number of states of a
    single FSM configuration.
    
    Usable number of user defined states: Range of BaseType - 1
    
    Can be reduced to optimze ROM usage.
  默认值: UINT8
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: vFsmLibEventBaseType
  长名称: ''
  描述: |
    Definition of the base type for vFsmLibEventType. It affects the maximum number of events of a
    single FSM configuration.
    
    Usable number of user defined events: Range of BaseType - 6
    
    Can be reduced to optimze ROM usage.
  默认值: UINT8
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: vFsmLibVersionInfoApi
  长名称: ''
  描述: |
    Enables/disables the function vFsmLib_GetVersionInfo() to get major, minor and patch version
    information.
    
    TRUE: vFsmLib_GetVersionInfo() API service is available
    FALSE: vFsmLib_GetVersionInfo() API service is not available
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: vFsmLibSafeBswChecks
  长名称: ''
  描述: Selects if safety checks are used. These checks improve robustness as e.g. invalid parameters
      are checked before function is executed. This attribute has to be enabled for safety
      projects where this component is mapped to an ASIL partition.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 8
  名称: vFsmLibTriggerBaseType
  长名称: ''
  描述: |
    Definition of the base type for vFsmLibTriggerType. It affects the maximum number of trigger
    entries of a single FSM state. Trigger entries are the combined number of transitions and state
    behaviors (entry/exit/doActivity).
    
    Usable number of user defined trigger entries: Range of BaseType
    
    Can be reduced to optimze ROM usage.
  默认值: UINT8
  最小值: ''
  最大值: ''
```

### 2. vFsmLibFsm

**描述**: Configuration of a Finite State Maching (FSM).

#### 参数列表

```yaml
- 
  序号: 1
  名称: vFsmLibMaxTransitions
  长名称: ''
  描述: |
    Defines the maximum number of executed transitions during one processing cycle.
    
    This parameter can be used to limit the processing time for each processing cycle.
  默认值: 8
  最小值: 1
  最大值: 255
```

### 3. vFsmLibState

**描述**: Definition of a single FSM state.

#### 参数列表

```yaml
- 
  序号: 1
  名称: vFsmLibStateType
  长名称: ''
  描述: Definition of the type of the state.
  默认值: SimpleState
  最小值: ''
  最大值: ''
```

### 4. vFsmLibTransition

**描述**: Definition of a single state transition.

#### 参数列表

```yaml
- 
  序号: 1
  名称: vFsmLibGuardFunction
  长名称: ''
  描述: |
    Definition of the guard callout function.
    
    This function will be called when this transition is triggered. The transition will be activated
    only if the guard returns VFSMLIB_GUARD_TRUE.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: vFsmLibOrder
  长名称: ''
  描述: Definition of the order in which the transitions will be evaluated, beginning with the lowest
      value.
  默认值: 0
  最小值: 0
  最大值: 65535
- 
  序号: 3
  名称: vFsmLibGuardStub
  长名称: ''
  描述: The is parameter defines if a stub for the defined guard callout shall be created in
      vFsmLib_Callout_Stubs.c
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: vFsmLibBehaviorFunction
  长名称: ''
  描述: |
    Definition of the optional effect behavior callout function for this transition.
    
    The effect behavior will be called during transition after all exit behaviors are executed and
    before the first entry behavior is executed.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: vFsmLibTrigger
  长名称: ''
  描述: |
    Definition of how the transition is triggered.
    
    OnEvent:          The transition is triggered on a specific external event.
    OnAnyEvent:    The transition is triggered on any external event.
    OnCompletion:  The transition is triggered implicitly as soon as the doActivity behavior of  the
    parent state is completed.
  默认值: OnEvent
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: vFsmLibBehaviorStub
  长名称: ''
  描述: Defines if a stub for the defined effect behavior function shall be created in
      vFsmLib_Callout_Stubs.c
  默认值: false
  最小值: ''
  最大值: ''
```

### 5. vFsmLibBehavior

**描述**: Definition of a state behavior.

#### 参数列表

```yaml
- 
  序号: 1
  名称: vFsmLibType
  长名称: ''
  描述: |
    Definition of the type of the behavior.
    
    Entry:           The behavior is executed on entering the state
    Exit:             The behavior is executed on leaving the state
    DoActivity:   The behavior is executed once per processing cycle as long as the state is not
    left and the behavior returns VFSMLIB_BEHAVIOR_PENDING
  默认值: Entry
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: vFsmLibBehaviorStub
  长名称: ''
  描述: Defines if a stub for the defined behavior function shall be created in
      vFsmLib_Callout_Stubs.c
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: vFsmLibBehaviorFunction
  长名称: ''
  描述: Definition of the behavior callout function.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: vFsmLibOrder
  长名称: ''
  描述: Definition of the order in which the behaviors will be evaluated, beginning with the lowest
      value.
  默认值: 0
  最小值: 0
  最大值: 65535
```

### 6. vFsmLibEvent

**描述**: Definition of an external event.

该容器没有参数。

### 7. vFsmLibFsmGroup

**描述**: Definition of all groups of FSMs.

该容器没有参数。

### 8. vFsmLibGroupEvent

**描述**: Definition of a group event.

Group events can be used by all Finite State Machines which are part of the group.

该容器没有参数。

