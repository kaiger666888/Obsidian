# vFsmLib - 完整配置文档

*此文档由ARXML文件自动生成，采用层次化结构展示*

**生成时间**: 2025-06-16 14:46:01

## 📑 目录

- [📄 文件信息](#-文件信息)
- [🔧 模块定义](#-模块定义)
  - [vFsmLib](#vfsmlib)
- [📦 包结构](#-包结构)
- [⚡ 实现信息](#-实现信息)
- [⚙️ 配置信息](#️-配置信息)

## 📄 文件信息

### Schema信息
- **Schema位置**: `http://autosar.org/schema/r4.0 autosar_4-0-3.xsd`
- **命名空间**: `http://autosar.org/schema/r4.0`

## 🔧 模块定义

### 1. vFsmLib

#### 基本信息

- **UUID**: `6c75b829-808b-4417-ad8e-f42a13b36938`
- **模块名称**: `vFsmLib`
- **类别**: `VENDOR_SPECIFIC_MODULE_DEFINITION`
- **多重性**: [0..1]
- **支持的变体**:
  - VARIANT-PRE-COMPILE

#### 模块描述

Vector Finite State Machine Library. The vFsmLib is used to configure and execute user defined finite state machines (FSM). 
The behavior of vFsmLib is based on concept of "Behavior State Machines" as described in the UML specification.
#Library
#Vector

#### 版本历史

共有 **4** 个版本记录：

##### 1. 版本 1.00.00

- **状态**: released
- **发布日期**: 2020-08-28T00:00:00+02:00
- **发布者**: visfsn

**变更内容**:

##### 2. 版本 1.00.01

- **状态**: released
- **发布日期**: 2022-02-21T00:00:00+02:00
- **发布者**: visci

**变更内容**:

##### 3. 版本 1.01.00

- **状态**: released
- **发布日期**: 2023-03-10T11:40:54+01:00
- **发布者**: visdlm

**变更内容**:

##### 4. 版本 

- **状态**: released
- **发布日期**: 2023-05-31T17:35:11+02:00
- **发布者**: visrcn

**变更内容**:

#### 配置容器

本模块包含 **8** 个配置容器：

##### 1. vFsmLibGeneral

**容器属性**:

- **UUID**: `66c54277-1dc7-41d8-a810-aa1f24aaa770`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vFsmLibGeneral`
- **多重性**: [1..1]
- **构建后可变**: false

**容器描述**:

General configuration parameters of the vFsmLib.

###### 参数配置

此容器包含 **8** 个参数：

####### INTEGER 类型参数

######## 1. vFsmLibMaxHierarchyDepth

- **UUID**: `e1956fcd-ba18-4b48-aaaf-4d81db5bd873`
- **参数名**: `vFsmLibMaxHierarchyDepth`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `8`
- **取值范围**: [1..255]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Definition of the maximum hierarchy depth for group transitions and transition paths.

Can be reduced to optimize RAM usage.

####### BOOLEAN 类型参数

######## 1. vFsmLibDevErrorDetect

- **UUID**: `d7ae1d0f-037a-4170-b7ec-b32bd9668a79`
- **参数名**: `vFsmLibDevErrorDetect`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Switches the Development Error Detection and Notification ON or OFF.

true:	Development error detection is enabled.
false:	Development error detection is disabled.

######## 2. vFsmLibVersionInfoApi

- **UUID**: `2ef6fabd-47ce-4006-9125-f3c05dce5489`
- **参数名**: `vFsmLibVersionInfoApi`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enables/disables the function vFsmLib_GetVersionInfo() to get major, minor and patch version information.

TRUE: vFsmLib_GetVersionInfo() API service is available
FALSE: vFsmLib_GetVersionInfo() API service is not available

######## 3. vFsmLibSafeBswChecks

- **UUID**: `3efa9a45-4b8f-4443-9489-5a18fa75e355`
- **参数名**: `vFsmLibSafeBswChecks`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Selects if safety checks are used. These checks improve robustness as e.g. invalid parameters are checked before function is executed. This attribute has to be enabled for safety projects where this component is mapped to an ASIL partition.

####### STRING 类型参数

######## 1. vFsmLibAdditionalIncludes

- **UUID**: `5b074b8e-0412-47ce-b1a6-2bd7d85dd144`
- **参数名**: `vFsmLibAdditionalIncludes`
- **数据类型**: STRING
- **多重性**: [0..infinite]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Definition of additional include files.

####### ENUMERATION 类型参数

######## 1. vFsmLibStateBaseType

- **UUID**: `f6f99899-87e3-4ec6-8858-7f8129ea5f8f`
- **参数名**: `vFsmLibStateBaseType`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `UINT8`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `UINT8`
  - `UINT16`
  - `UINT32`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Definition of the base type for vFsmLibStateType. It affects the maximum number of states of a single FSM configuration.

Usable number of user defined states: Range of BaseType - 1

Can be reduced to optimze ROM usage.

######## 2. vFsmLibEventBaseType

- **UUID**: `5661d819-3fa1-4031-99b2-7f97e9a3d7d6`
- **参数名**: `vFsmLibEventBaseType`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `UINT8`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `UINT8`
  - `UINT16`
  - `UINT32`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Definition of the base type for vFsmLibEventType. It affects the maximum number of events of a single FSM configuration.

Usable number of user defined events: Range of BaseType - 6

Can be reduced to optimze ROM usage.

######## 3. vFsmLibTriggerBaseType

- **UUID**: `7e4f7909-f8f1-46ac-89ed-740eda3f2e14`
- **参数名**: `vFsmLibTriggerBaseType`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `UINT8`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `UINT8`
  - `UINT16`
  - `UINT32`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Definition of the base type for vFsmLibTriggerType. It affects the maximum number of trigger entries of a single FSM state. Trigger entries are the combined number of transitions and state behaviors (entry/exit/doActivity).

Usable number of user defined trigger entries: Range of BaseType

Can be reduced to optimze ROM usage.

##### 2. vFsmLibFsm

**容器属性**:

- **UUID**: `89dcca4b-3f3b-41fb-a807-2911e6f1a9a3`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vFsmLibFsm`
- **多重性**: [0..infinite]
- **构建后可变**: false

**容器描述**:

Configuration of a Finite State Maching (FSM).

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. vFsmLibMaxTransitions

- **UUID**: `5658b745-f230-45da-8bfb-7a78aa4da4fc`
- **参数名**: `vFsmLibMaxTransitions`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `8`
- **取值范围**: [1..255]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the maximum number of executed transitions during one processing cycle.

This parameter can be used to limit the processing time for each processing cycle.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. vFsmLibInitState

- **UUID**: `a6aa161d-98c1-45c5-a7f4-42f637e85c28`
- **引用名**: `vFsmLibInitState`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `vFsmLibState`
- **完整路径**: `/MICROSAR/vFsmLib/vFsmLibFsm/vFsmLibState`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Definition of the initial state of the FSM.

This state will be reached implicitly after the first call of vFsmLib_ProcessFsm().

###### 配置容器

本模块包含 **4** 个配置容器：

####### 1. vFsmLibState

**容器属性**:

- **UUID**: `e66ebe2c-1443-42a3-a8bf-d8819ed2a00e`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vFsmLibState`
- **多重性**: [1..infinite]
- **构建后可变**: false

**容器描述**:

Definition of a single FSM state.

######## 参数配置

此容器包含 **1** 个参数：

######### ENUMERATION 类型参数

########## 1. vFsmLibStateType

- **UUID**: `e5b574a8-827a-4379-ad73-3c65a15ec355`
- **参数名**: `vFsmLibStateType`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `SimpleState`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `SimpleState`
  - `CompositeState`
  - `ChoiceState`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Definition of the type of the state.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. vFsmLibParentState

- **UUID**: `23f97c94-744e-4283-bbc4-bd264e16c7b2`
- **引用名**: `vFsmLibParentState`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `vFsmLibState`
- **完整路径**: `/MICROSAR/vFsmLib/vFsmLibFsm/vFsmLibState`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the parent (composite) state of this state.

######## 配置容器

本模块包含 **2** 个配置容器：

######### 1. vFsmLibTransition

**容器属性**:

- **UUID**: `1479504b-7a30-438f-8405-f729a3fd0c0d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vFsmLibTransition`
- **多重性**: [0..infinite]
- **构建后可变**: false

**容器描述**:

Definition of a single state transition.

########## 参数配置

此容器包含 **6** 个参数：

########### INTEGER 类型参数

############ 1. vFsmLibOrder

- **UUID**: `69360327-c6a3-43db-a776-b6aa377dda00`
- **参数名**: `vFsmLibOrder`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Definition of the order in which the transitions will be evaluated, beginning with the lowest value.

########### BOOLEAN 类型参数

############ 1. vFsmLibGuardStub

- **UUID**: `4a1614da-2b5d-45ec-86bf-dde30605d28e`
- **参数名**: `vFsmLibGuardStub`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The is parameter defines if a stub for the defined guard callout shall be created in vFsmLib_Callout_Stubs.c

############ 2. vFsmLibBehaviorStub

- **UUID**: `a9caede5-6275-48fe-af7f-245f1758d7cd`
- **参数名**: `vFsmLibBehaviorStub`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines if a stub for the defined effect behavior function shall be created in vFsmLib_Callout_Stubs.c

########### ENUMERATION 类型参数

############ 1. vFsmLibTrigger

- **UUID**: `b6cc017a-706c-4b26-badf-3644af87688c`
- **参数名**: `vFsmLibTrigger`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `OnEvent`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `OnEvent`
  - `OnAnyEvent`
  - `OnCompletion`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Definition of how the transition is triggered.

OnEvent:          The transition is triggered on a specific external event.
OnAnyEvent:    The transition is triggered on any external event.
OnCompletion:  The transition is triggered implicitly as soon as the doActivity behavior of  the parent state is completed.

########### FUNCTION-NAME 类型参数

############ 1. vFsmLibGuardFunction

- **UUID**: `f6d97631-cf41-4674-998e-a6d00f0ca726`
- **参数名**: `vFsmLibGuardFunction`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **函数变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Definition of the guard callout function. 

This function will be called when this transition is triggered. The transition will be activated only if the guard returns VFSMLIB_GUARD_TRUE.

############ 2. vFsmLibBehaviorFunction

- **UUID**: `f53848f8-ad78-4f31-87f7-06e15fb93914`
- **参数名**: `vFsmLibBehaviorFunction`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **函数变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Definition of the optional effect behavior callout function for this transition.

The effect behavior will be called during transition after all exit behaviors are executed and before the first entry behavior is executed.

########## 引用关系

此容器包含 **2** 个引用：

########### REFERENCE 类型引用

############ 1. vFsmLibNextState

- **UUID**: `d1005573-0c2e-4085-9809-a8495eb073c2`
- **引用名**: `vFsmLibNextState`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `vFsmLibState`
- **完整路径**: `/MICROSAR/vFsmLib/vFsmLibFsm/vFsmLibState`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Definition of the target state of the transition.

########### CHOICE-REFERENCE 类型引用

############ 1. vFsmLibTriggerEvent

- **UUID**: `f32117ad-89fd-4335-af1a-71164c5b534d`
- **引用名**: `vFsmLibTriggerEvent`
- **引用类型**: CHOICE-REFERENCE
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **需要索引**: false
- **目标引用列表**:
  - `/MICROSAR/vFsmLib/vFsmLibFsm/vFsmLibEvent`
  - `/MICROSAR/vFsmLib/vFsmLibFsmGroup/vFsmLibGroupEvent`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Definition of the event which shall trigger this transition.

Only relevant if "OnEvent" is selected as Trigger.

######### 2. vFsmLibBehavior

**容器属性**:

- **UUID**: `1f2e78b1-7d01-476f-bd82-c007f86586ad`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vFsmLibBehavior`
- **多重性**: [0..infinite]
- **构建后可变**: false

**容器描述**:

Definition of a state behavior.

########## 参数配置

此容器包含 **4** 个参数：

########### INTEGER 类型参数

############ 1. vFsmLibOrder

- **UUID**: `787ceab6-7ffe-45c0-9169-426695f782a4`
- **参数名**: `vFsmLibOrder`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Definition of the order in which the behaviors will be evaluated, beginning with the lowest value.

########### BOOLEAN 类型参数

############ 1. vFsmLibBehaviorStub

- **UUID**: `b2db7c3a-030d-4183-a196-99f3f4571027`
- **参数名**: `vFsmLibBehaviorStub`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines if a stub for the defined behavior function shall be created in vFsmLib_Callout_Stubs.c

########### ENUMERATION 类型参数

############ 1. vFsmLibType

- **UUID**: `971d1c20-014f-47ab-a953-3777362b2b83`
- **参数名**: `vFsmLibType`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `Entry`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `Entry`
  - `Exit`
  - `DoActivity`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Definition of the type of the behavior.

Entry:           The behavior is executed on entering the state
Exit:             The behavior is executed on leaving the state
DoActivity:   The behavior is executed once per processing cycle as long as the state is not left and the behavior returns VFSMLIB_BEHAVIOR_PENDING

########### FUNCTION-NAME 类型参数

############ 1. vFsmLibBehaviorFunction

- **UUID**: `b1b75c65-3611-48a4-8b41-0bd8e5cd5024`
- **参数名**: `vFsmLibBehaviorFunction`
- **数据类型**: FUNCTION-NAME
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **函数变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Definition of the behavior callout function.

####### 2. vFsmLibTransition

**容器属性**:

- **UUID**: `1479504b-7a30-438f-8405-f729a3fd0c0d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vFsmLibTransition`
- **多重性**: [0..infinite]
- **构建后可变**: false

**容器描述**:

Definition of a single state transition.

######## 参数配置

此容器包含 **6** 个参数：

######### INTEGER 类型参数

########## 1. vFsmLibOrder

- **UUID**: `69360327-c6a3-43db-a776-b6aa377dda00`
- **参数名**: `vFsmLibOrder`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Definition of the order in which the transitions will be evaluated, beginning with the lowest value.

######### BOOLEAN 类型参数

########## 1. vFsmLibGuardStub

- **UUID**: `4a1614da-2b5d-45ec-86bf-dde30605d28e`
- **参数名**: `vFsmLibGuardStub`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The is parameter defines if a stub for the defined guard callout shall be created in vFsmLib_Callout_Stubs.c

########## 2. vFsmLibBehaviorStub

- **UUID**: `a9caede5-6275-48fe-af7f-245f1758d7cd`
- **参数名**: `vFsmLibBehaviorStub`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines if a stub for the defined effect behavior function shall be created in vFsmLib_Callout_Stubs.c

######### ENUMERATION 类型参数

########## 1. vFsmLibTrigger

- **UUID**: `b6cc017a-706c-4b26-badf-3644af87688c`
- **参数名**: `vFsmLibTrigger`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `OnEvent`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `OnEvent`
  - `OnAnyEvent`
  - `OnCompletion`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Definition of how the transition is triggered.

OnEvent:          The transition is triggered on a specific external event.
OnAnyEvent:    The transition is triggered on any external event.
OnCompletion:  The transition is triggered implicitly as soon as the doActivity behavior of  the parent state is completed.

######### FUNCTION-NAME 类型参数

########## 1. vFsmLibGuardFunction

- **UUID**: `f6d97631-cf41-4674-998e-a6d00f0ca726`
- **参数名**: `vFsmLibGuardFunction`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **函数变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Definition of the guard callout function. 

This function will be called when this transition is triggered. The transition will be activated only if the guard returns VFSMLIB_GUARD_TRUE.

########## 2. vFsmLibBehaviorFunction

- **UUID**: `f53848f8-ad78-4f31-87f7-06e15fb93914`
- **参数名**: `vFsmLibBehaviorFunction`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **函数变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Definition of the optional effect behavior callout function for this transition.

The effect behavior will be called during transition after all exit behaviors are executed and before the first entry behavior is executed.

######## 引用关系

此容器包含 **2** 个引用：

######### REFERENCE 类型引用

########## 1. vFsmLibNextState

- **UUID**: `d1005573-0c2e-4085-9809-a8495eb073c2`
- **引用名**: `vFsmLibNextState`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `vFsmLibState`
- **完整路径**: `/MICROSAR/vFsmLib/vFsmLibFsm/vFsmLibState`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Definition of the target state of the transition.

######### CHOICE-REFERENCE 类型引用

########## 1. vFsmLibTriggerEvent

- **UUID**: `f32117ad-89fd-4335-af1a-71164c5b534d`
- **引用名**: `vFsmLibTriggerEvent`
- **引用类型**: CHOICE-REFERENCE
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **需要索引**: false
- **目标引用列表**:
  - `/MICROSAR/vFsmLib/vFsmLibFsm/vFsmLibEvent`
  - `/MICROSAR/vFsmLib/vFsmLibFsmGroup/vFsmLibGroupEvent`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Definition of the event which shall trigger this transition.

Only relevant if "OnEvent" is selected as Trigger.

####### 3. vFsmLibBehavior

**容器属性**:

- **UUID**: `1f2e78b1-7d01-476f-bd82-c007f86586ad`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vFsmLibBehavior`
- **多重性**: [0..infinite]
- **构建后可变**: false

**容器描述**:

Definition of a state behavior.

######## 参数配置

此容器包含 **4** 个参数：

######### INTEGER 类型参数

########## 1. vFsmLibOrder

- **UUID**: `787ceab6-7ffe-45c0-9169-426695f782a4`
- **参数名**: `vFsmLibOrder`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Definition of the order in which the behaviors will be evaluated, beginning with the lowest value.

######### BOOLEAN 类型参数

########## 1. vFsmLibBehaviorStub

- **UUID**: `b2db7c3a-030d-4183-a196-99f3f4571027`
- **参数名**: `vFsmLibBehaviorStub`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines if a stub for the defined behavior function shall be created in vFsmLib_Callout_Stubs.c

######### ENUMERATION 类型参数

########## 1. vFsmLibType

- **UUID**: `971d1c20-014f-47ab-a953-3777362b2b83`
- **参数名**: `vFsmLibType`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `Entry`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `Entry`
  - `Exit`
  - `DoActivity`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Definition of the type of the behavior.

Entry:           The behavior is executed on entering the state
Exit:             The behavior is executed on leaving the state
DoActivity:   The behavior is executed once per processing cycle as long as the state is not left and the behavior returns VFSMLIB_BEHAVIOR_PENDING

######### FUNCTION-NAME 类型参数

########## 1. vFsmLibBehaviorFunction

- **UUID**: `b1b75c65-3611-48a4-8b41-0bd8e5cd5024`
- **参数名**: `vFsmLibBehaviorFunction`
- **数据类型**: FUNCTION-NAME
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **函数变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Definition of the behavior callout function.

####### 4. vFsmLibEvent

**容器属性**:

- **UUID**: `061efa6b-e655-4519-bf9d-b5f5efcae481`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vFsmLibEvent`
- **多重性**: [0..infinite]
- **构建后可变**: false

**容器描述**:

Definition of an external event.

##### 3. vFsmLibState

**容器属性**:

- **UUID**: `e66ebe2c-1443-42a3-a8bf-d8819ed2a00e`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vFsmLibState`
- **多重性**: [1..infinite]
- **构建后可变**: false

**容器描述**:

Definition of a single FSM state.

###### 参数配置

此容器包含 **1** 个参数：

####### ENUMERATION 类型参数

######## 1. vFsmLibStateType

- **UUID**: `e5b574a8-827a-4379-ad73-3c65a15ec355`
- **参数名**: `vFsmLibStateType`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `SimpleState`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `SimpleState`
  - `CompositeState`
  - `ChoiceState`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Definition of the type of the state.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. vFsmLibParentState

- **UUID**: `23f97c94-744e-4283-bbc4-bd264e16c7b2`
- **引用名**: `vFsmLibParentState`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `vFsmLibState`
- **完整路径**: `/MICROSAR/vFsmLib/vFsmLibFsm/vFsmLibState`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the parent (composite) state of this state.

###### 配置容器

本模块包含 **2** 个配置容器：

####### 1. vFsmLibTransition

**容器属性**:

- **UUID**: `1479504b-7a30-438f-8405-f729a3fd0c0d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vFsmLibTransition`
- **多重性**: [0..infinite]
- **构建后可变**: false

**容器描述**:

Definition of a single state transition.

######## 参数配置

此容器包含 **6** 个参数：

######### INTEGER 类型参数

########## 1. vFsmLibOrder

- **UUID**: `69360327-c6a3-43db-a776-b6aa377dda00`
- **参数名**: `vFsmLibOrder`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Definition of the order in which the transitions will be evaluated, beginning with the lowest value.

######### BOOLEAN 类型参数

########## 1. vFsmLibGuardStub

- **UUID**: `4a1614da-2b5d-45ec-86bf-dde30605d28e`
- **参数名**: `vFsmLibGuardStub`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The is parameter defines if a stub for the defined guard callout shall be created in vFsmLib_Callout_Stubs.c

########## 2. vFsmLibBehaviorStub

- **UUID**: `a9caede5-6275-48fe-af7f-245f1758d7cd`
- **参数名**: `vFsmLibBehaviorStub`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines if a stub for the defined effect behavior function shall be created in vFsmLib_Callout_Stubs.c

######### ENUMERATION 类型参数

########## 1. vFsmLibTrigger

- **UUID**: `b6cc017a-706c-4b26-badf-3644af87688c`
- **参数名**: `vFsmLibTrigger`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `OnEvent`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `OnEvent`
  - `OnAnyEvent`
  - `OnCompletion`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Definition of how the transition is triggered.

OnEvent:          The transition is triggered on a specific external event.
OnAnyEvent:    The transition is triggered on any external event.
OnCompletion:  The transition is triggered implicitly as soon as the doActivity behavior of  the parent state is completed.

######### FUNCTION-NAME 类型参数

########## 1. vFsmLibGuardFunction

- **UUID**: `f6d97631-cf41-4674-998e-a6d00f0ca726`
- **参数名**: `vFsmLibGuardFunction`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **函数变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Definition of the guard callout function. 

This function will be called when this transition is triggered. The transition will be activated only if the guard returns VFSMLIB_GUARD_TRUE.

########## 2. vFsmLibBehaviorFunction

- **UUID**: `f53848f8-ad78-4f31-87f7-06e15fb93914`
- **参数名**: `vFsmLibBehaviorFunction`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **函数变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Definition of the optional effect behavior callout function for this transition.

The effect behavior will be called during transition after all exit behaviors are executed and before the first entry behavior is executed.

######## 引用关系

此容器包含 **2** 个引用：

######### REFERENCE 类型引用

########## 1. vFsmLibNextState

- **UUID**: `d1005573-0c2e-4085-9809-a8495eb073c2`
- **引用名**: `vFsmLibNextState`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `vFsmLibState`
- **完整路径**: `/MICROSAR/vFsmLib/vFsmLibFsm/vFsmLibState`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Definition of the target state of the transition.

######### CHOICE-REFERENCE 类型引用

########## 1. vFsmLibTriggerEvent

- **UUID**: `f32117ad-89fd-4335-af1a-71164c5b534d`
- **引用名**: `vFsmLibTriggerEvent`
- **引用类型**: CHOICE-REFERENCE
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **需要索引**: false
- **目标引用列表**:
  - `/MICROSAR/vFsmLib/vFsmLibFsm/vFsmLibEvent`
  - `/MICROSAR/vFsmLib/vFsmLibFsmGroup/vFsmLibGroupEvent`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Definition of the event which shall trigger this transition.

Only relevant if "OnEvent" is selected as Trigger.

####### 2. vFsmLibBehavior

**容器属性**:

- **UUID**: `1f2e78b1-7d01-476f-bd82-c007f86586ad`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vFsmLibBehavior`
- **多重性**: [0..infinite]
- **构建后可变**: false

**容器描述**:

Definition of a state behavior.

######## 参数配置

此容器包含 **4** 个参数：

######### INTEGER 类型参数

########## 1. vFsmLibOrder

- **UUID**: `787ceab6-7ffe-45c0-9169-426695f782a4`
- **参数名**: `vFsmLibOrder`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Definition of the order in which the behaviors will be evaluated, beginning with the lowest value.

######### BOOLEAN 类型参数

########## 1. vFsmLibBehaviorStub

- **UUID**: `b2db7c3a-030d-4183-a196-99f3f4571027`
- **参数名**: `vFsmLibBehaviorStub`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines if a stub for the defined behavior function shall be created in vFsmLib_Callout_Stubs.c

######### ENUMERATION 类型参数

########## 1. vFsmLibType

- **UUID**: `971d1c20-014f-47ab-a953-3777362b2b83`
- **参数名**: `vFsmLibType`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `Entry`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `Entry`
  - `Exit`
  - `DoActivity`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Definition of the type of the behavior.

Entry:           The behavior is executed on entering the state
Exit:             The behavior is executed on leaving the state
DoActivity:   The behavior is executed once per processing cycle as long as the state is not left and the behavior returns VFSMLIB_BEHAVIOR_PENDING

######### FUNCTION-NAME 类型参数

########## 1. vFsmLibBehaviorFunction

- **UUID**: `b1b75c65-3611-48a4-8b41-0bd8e5cd5024`
- **参数名**: `vFsmLibBehaviorFunction`
- **数据类型**: FUNCTION-NAME
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **函数变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Definition of the behavior callout function.

##### 4. vFsmLibTransition

**容器属性**:

- **UUID**: `1479504b-7a30-438f-8405-f729a3fd0c0d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vFsmLibTransition`
- **多重性**: [0..infinite]
- **构建后可变**: false

**容器描述**:

Definition of a single state transition.

###### 参数配置

此容器包含 **6** 个参数：

####### INTEGER 类型参数

######## 1. vFsmLibOrder

- **UUID**: `69360327-c6a3-43db-a776-b6aa377dda00`
- **参数名**: `vFsmLibOrder`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Definition of the order in which the transitions will be evaluated, beginning with the lowest value.

####### BOOLEAN 类型参数

######## 1. vFsmLibGuardStub

- **UUID**: `4a1614da-2b5d-45ec-86bf-dde30605d28e`
- **参数名**: `vFsmLibGuardStub`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The is parameter defines if a stub for the defined guard callout shall be created in vFsmLib_Callout_Stubs.c

######## 2. vFsmLibBehaviorStub

- **UUID**: `a9caede5-6275-48fe-af7f-245f1758d7cd`
- **参数名**: `vFsmLibBehaviorStub`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines if a stub for the defined effect behavior function shall be created in vFsmLib_Callout_Stubs.c

####### ENUMERATION 类型参数

######## 1. vFsmLibTrigger

- **UUID**: `b6cc017a-706c-4b26-badf-3644af87688c`
- **参数名**: `vFsmLibTrigger`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `OnEvent`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `OnEvent`
  - `OnAnyEvent`
  - `OnCompletion`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Definition of how the transition is triggered.

OnEvent:          The transition is triggered on a specific external event.
OnAnyEvent:    The transition is triggered on any external event.
OnCompletion:  The transition is triggered implicitly as soon as the doActivity behavior of  the parent state is completed.

####### FUNCTION-NAME 类型参数

######## 1. vFsmLibGuardFunction

- **UUID**: `f6d97631-cf41-4674-998e-a6d00f0ca726`
- **参数名**: `vFsmLibGuardFunction`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **函数变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Definition of the guard callout function. 

This function will be called when this transition is triggered. The transition will be activated only if the guard returns VFSMLIB_GUARD_TRUE.

######## 2. vFsmLibBehaviorFunction

- **UUID**: `f53848f8-ad78-4f31-87f7-06e15fb93914`
- **参数名**: `vFsmLibBehaviorFunction`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **函数变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Definition of the optional effect behavior callout function for this transition.

The effect behavior will be called during transition after all exit behaviors are executed and before the first entry behavior is executed.

###### 引用关系

此容器包含 **2** 个引用：

####### REFERENCE 类型引用

######## 1. vFsmLibNextState

- **UUID**: `d1005573-0c2e-4085-9809-a8495eb073c2`
- **引用名**: `vFsmLibNextState`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `vFsmLibState`
- **完整路径**: `/MICROSAR/vFsmLib/vFsmLibFsm/vFsmLibState`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Definition of the target state of the transition.

####### CHOICE-REFERENCE 类型引用

######## 1. vFsmLibTriggerEvent

- **UUID**: `f32117ad-89fd-4335-af1a-71164c5b534d`
- **引用名**: `vFsmLibTriggerEvent`
- **引用类型**: CHOICE-REFERENCE
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **需要索引**: false
- **目标引用列表**:
  - `/MICROSAR/vFsmLib/vFsmLibFsm/vFsmLibEvent`
  - `/MICROSAR/vFsmLib/vFsmLibFsmGroup/vFsmLibGroupEvent`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Definition of the event which shall trigger this transition.

Only relevant if "OnEvent" is selected as Trigger.

##### 5. vFsmLibBehavior

**容器属性**:

- **UUID**: `1f2e78b1-7d01-476f-bd82-c007f86586ad`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vFsmLibBehavior`
- **多重性**: [0..infinite]
- **构建后可变**: false

**容器描述**:

Definition of a state behavior.

###### 参数配置

此容器包含 **4** 个参数：

####### INTEGER 类型参数

######## 1. vFsmLibOrder

- **UUID**: `787ceab6-7ffe-45c0-9169-426695f782a4`
- **参数名**: `vFsmLibOrder`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Definition of the order in which the behaviors will be evaluated, beginning with the lowest value.

####### BOOLEAN 类型参数

######## 1. vFsmLibBehaviorStub

- **UUID**: `b2db7c3a-030d-4183-a196-99f3f4571027`
- **参数名**: `vFsmLibBehaviorStub`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines if a stub for the defined behavior function shall be created in vFsmLib_Callout_Stubs.c

####### ENUMERATION 类型参数

######## 1. vFsmLibType

- **UUID**: `971d1c20-014f-47ab-a953-3777362b2b83`
- **参数名**: `vFsmLibType`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `Entry`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `Entry`
  - `Exit`
  - `DoActivity`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Definition of the type of the behavior.

Entry:           The behavior is executed on entering the state
Exit:             The behavior is executed on leaving the state
DoActivity:   The behavior is executed once per processing cycle as long as the state is not left and the behavior returns VFSMLIB_BEHAVIOR_PENDING

####### FUNCTION-NAME 类型参数

######## 1. vFsmLibBehaviorFunction

- **UUID**: `b1b75c65-3611-48a4-8b41-0bd8e5cd5024`
- **参数名**: `vFsmLibBehaviorFunction`
- **数据类型**: FUNCTION-NAME
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **函数变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Definition of the behavior callout function.

##### 6. vFsmLibEvent

**容器属性**:

- **UUID**: `061efa6b-e655-4519-bf9d-b5f5efcae481`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vFsmLibEvent`
- **多重性**: [0..infinite]
- **构建后可变**: false

**容器描述**:

Definition of an external event.

##### 7. vFsmLibFsmGroup

**容器属性**:

- **UUID**: `d22b0583-3200-40a8-937f-d8bc36672b0b`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vFsmLibFsmGroup`
- **多重性**: [0..infinite]
- **构建后可变**: false

**容器描述**:

Definition of all groups of FSMs.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. vFsmLibFsm

- **UUID**: `b45c9782-f366-46c0-b84e-bf00d86193f6`
- **引用名**: `vFsmLibFsm`
- **引用类型**: REFERENCE
- **多重性**: [1..infinite]
- **目标**: `vFsmLibFsm`
- **完整路径**: `/MICROSAR/vFsmLib/vFsmLibFsm`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Definition of FSM group members.

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. vFsmLibGroupEvent

**容器属性**:

- **UUID**: `18fbdf97-0891-4323-8707-7f299f5b92f4`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vFsmLibGroupEvent`
- **多重性**: [0..infinite]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

Definition of a group event.

Group events can be used by all Finite State Machines which are part of the group.

##### 8. vFsmLibGroupEvent

**容器属性**:

- **UUID**: `18fbdf97-0891-4323-8707-7f299f5b92f4`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vFsmLibGroupEvent`
- **多重性**: [0..infinite]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

Definition of a group event.

Group events can be used by all Finite State Machines which are part of the group.

## 📦 包结构

此ARXML文件包含 **1** 个包：

### 1. MICROSAR

- **UUID**: `ff55d029-386d-43a2-b3c2-dfef4c7a5e36`
- **包名称**: `MICROSAR`
- **包含元素数量**: 4

#### 包含的元素

##### BSW-IMPLEMENTATION 类型元素

1. **vFsmLib_Impl**

##### ECUC-MODULE-DEF 类型元素

1. **vFsmLib**

##### ECUC-MODULE-CONFIGURATION-VALUES 类型元素

1. **vFsmLib_Pre**
2. **vFsmLib_Rec**

## ⚡ 实现信息

此ARXML文件包含 **1** 个实现：

### 1. vFsmLib_Impl

- **UUID**: `af647985-76dc-45b2-8ee6-5f81110e386b`
- **实现名称**: `vFsmLib_Impl`
- **编程语言**: C
- **软件版本**: 1.00.00
- **供应商ID**: 30
- **AUTOSAR版本**: 4.00.03
- **代码生成器**: DaVinci Configurator

## ⚙️ 配置信息

此ARXML文件包含 **2** 个配置：

### 1. vFsmLib_Pre

- **UUID**: `1f8f4987-2169-4190-98ef-97fde6e8e949`
- **配置名称**: `vFsmLib_Pre`
- **定义引用**: `/MICROSAR/vFsmLib`

### 2. vFsmLib_Rec

- **UUID**: `898dbdec-9505-45a5-9aa6-202259d7aeea`
- **配置名称**: `vFsmLib_Rec`
- **定义引用**: `/MICROSAR/vFsmLib`
