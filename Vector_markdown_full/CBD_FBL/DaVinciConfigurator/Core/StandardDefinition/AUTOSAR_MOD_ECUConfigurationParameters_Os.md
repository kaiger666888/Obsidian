# Os - 完整配置文档

*此文档由ARXML文件自动生成，采用层次化结构展示*

**生成时间**: 2025-06-16 14:48:54

## 📑 目录

- [📄 文件信息](#-文件信息)
- [🔧 模块定义](#-模块定义)
  - [Os](#os)
- [📦 包结构](#-包结构)

## 📄 文件信息

### Schema信息
- **Schema位置**: `http://autosar.org/schema/r4.0 AUTOSAR_4-2-1.xsd`
- **命名空间**: `http://autosar.org/schema/r4.0`

## 🔧 模块定义

### 1. Os

#### 基本信息

- **UUID**: `ECUC:8f6994a0-a4c8-48b9-bede-db9a5b9c2474`
- **模块名称**: `Os`
- **多重性**: [0..1]
- **支持的变体**:
  - VARIANT-PRE-COMPILE

#### 模块描述

Configuration of the Os (Operating System) module.

#### 版本历史

共有 **1** 个版本记录：

##### 1. 版本 4.6.0

- **发布日期**: 2014-10-31
- **发布者**: AUTOSAR

*此版本无详细变更记录*

#### 配置容器

本模块包含 **38** 个配置容器：

##### 1. OsAlarm

**容器属性**:

- **UUID**: `ECUC:f5bf116f-a0a2-4a8b-9f6a-1b023e6d9a13`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `OsAlarm`
- **多重性**: [0..infinite]

**容器描述**:

An OsAlarm may be used to asynchronously inform or activate a specific task. It is possible to start alarms automatically at system start-up depending on the application mode.

###### 引用关系

此容器包含 **2** 个引用：

####### REFERENCE 类型引用

######## 1. OsAlarmAccessingApplication

- **UUID**: `ECUC:7fe87d8e-e45a-4ce7-a368-b19db06f21cf`
- **引用名**: `OsAlarmAccessingApplication`
- **引用类型**: REFERENCE
- **多重性**: [0..infinite]
- **目标**: `OsApplication`
- **完整路径**: `/AUTOSAR/EcucDefs/Os/OsApplication`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to applications which have an access to this object.

######## 2. OsAlarmCounterRef

- **UUID**: `ECUC:2cfca734-698f-4fbe-b67f-60309f9d1df0`
- **引用名**: `OsAlarmCounterRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `OsCounter`
- **完整路径**: `/AUTOSAR/EcucDefs/Os/OsCounter`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the assigned counter for that alarm

###### 配置容器

本模块包含 **6** 个配置容器：

####### 1. OsAlarmActivateTask

**容器属性**:

- **UUID**: `ECUC:778af345-37da-4297-a5cf-617140faa94f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `OsAlarmActivateTask`
- **多重性**: [0..1]

**容器描述**:

This container specifies the parameters to activate a task.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. OsAlarmActivateTaskRef

- **UUID**: `ECUC:9d760cf7-d9fc-4fcf-a65f-1e5ac5d57eaf`
- **引用名**: `OsAlarmActivateTaskRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `OsTask`
- **完整路径**: `/AUTOSAR/EcucDefs/Os/OsTask`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the task that will be activated by that alarm action

####### 2. OsAlarmCallback

**容器属性**:

- **UUID**: `ECUC:d5df234a-b9c3-40e5-b30e-6ee6919a6c8e`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `OsAlarmCallback`
- **多重性**: [0..1]

**容器描述**:

This container specifies the parameters to call a callback OS alarm action.

######## 参数配置

此容器包含 **1** 个参数：

######### FUNCTION-NAME 类型参数

########## 1. OsAlarmCallbackName

- **UUID**: `ECUC:146cd561-a131-447a-8070-26ea050189b9`
- **参数名**: `OsAlarmCallbackName`
- **数据类型**: FUNCTION-NAME
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **函数变体**:
- **描述**: Name of the function that is called when this alarm callback is triggered.

####### 3. OsAlarmIncrementCounter

**容器属性**:

- **UUID**: `ECUC:e7f3faba-d482-41dd-9a78-a1bf24e96207`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `OsAlarmIncrementCounter`
- **多重性**: [0..1]

**容器描述**:

This container specifies the parameters to increment a counter.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. OsAlarmIncrementCounterRef

- **UUID**: `ECUC:f011f6a5-29e7-446b-85f5-b91034e9f12b`
- **引用名**: `OsAlarmIncrementCounterRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `OsCounter`
- **完整路径**: `/AUTOSAR/EcucDefs/Os/OsCounter`
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the counter that will be incremented by that alarm action

####### 4. OsAlarmSetEvent

**容器属性**:

- **UUID**: `ECUC:135c6787-8aad-4ca3-9c1b-f9db78eea4c0`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `OsAlarmSetEvent`
- **多重性**: [0..1]

**容器描述**:

This container specifies the parameters to set an event

######## 引用关系

此容器包含 **2** 个引用：

######### REFERENCE 类型引用

########## 1. OsAlarmSetEventRef

- **UUID**: `ECUC:1f077d18-ca8d-42bd-b867-4e59ce3d8e50`
- **引用名**: `OsAlarmSetEventRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `OsEvent`
- **完整路径**: `/AUTOSAR/EcucDefs/Os/OsEvent`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the event that will be set by that alarm action

########## 2. OsAlarmSetEventTaskRef

- **UUID**: `ECUC:db071009-6743-496a-ae4a-bb272eeb975a`
- **引用名**: `OsAlarmSetEventTaskRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `OsTask`
- **完整路径**: `/AUTOSAR/EcucDefs/Os/OsTask`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the task that will be activated by that event

####### 5. OsAlarmAutostart

**容器属性**:

- **UUID**: `ECUC:964053de-2482-4575-a091-31f2b2d62db1`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `OsAlarmAutostart`
- **多重性**: [0..1]

**容器描述**:

If present this container defines if an alarm is started automatically at system start-up depending on the application mode.

######## 参数配置

此容器包含 **3** 个参数：

######### INTEGER 类型参数

########## 1. OsAlarmAlarmTime

- **UUID**: `ECUC:60cfd12a-e181-4369-9286-c0432e6e5cf5`
- **参数名**: `OsAlarmAlarmTime`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..18446744073709551615]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: The relative or absolute tick value when the alarm expires for the first time. Note that for an alarm which is RELATIVE the value must be at bigger than 0.

########## 2. OsAlarmCycleTime

- **UUID**: `ECUC:3ad7702f-8f33-4b7d-87df-1fb32d89fb61`
- **参数名**: `OsAlarmCycleTime`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..18446744073709551615]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Cycle time of a cyclic alarm in ticks. If the value is 0 than the alarm is not cyclic.

######### ENUMERATION 类型参数

########## 1. OsAlarmAutostartType

- **UUID**: `ECUC:3aeb1a3f-7305-4179-b995-e284a9efb475`
- **参数名**: `OsAlarmAutostartType`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `ABSOLUTE` (来源: AUTOSAR_ECUC)
  - `RELATIVE` (来源: AUTOSAR_ECUC)
- **描述**: This specifies the type of autostart for the alarm..

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. OsAlarmAppModeRef

- **UUID**: `ECUC:a1c6da78-4cb0-4df2-92ae-69875adaedeb`
- **引用名**: `OsAlarmAppModeRef`
- **引用类型**: REFERENCE
- **多重性**: [1..infinite]
- **目标**: `OsAppMode`
- **完整路径**: `/AUTOSAR/EcucDefs/Os/OsAppMode`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the application modes for which the AUTOSTART shall be performed

####### 6. OsAlarmAction

**容器属性**:

- **UUID**: `ECUC:2acfb5a0-b476-4fa4-a34c-08e4acfe9858`
- **容器类型**: CHOICE-CONTAINER
- **容器名称**: `OsAlarmAction`
- **多重性**: [1..1]

**容器选择**:

- **OsAlarmActivateTask**
  - UUID: `ECUC:778af345-37da-4297-a5cf-617140faa94f`
  - 描述: This container specifies the parameters to activate a task.
- **OsAlarmCallback**
  - UUID: `ECUC:d5df234a-b9c3-40e5-b30e-6ee6919a6c8e`
  - 描述: This container specifies the parameters to call a callback OS alarm action.
- **OsAlarmIncrementCounter**
  - UUID: `ECUC:e7f3faba-d482-41dd-9a78-a1bf24e96207`
  - 描述: This container specifies the parameters to increment a counter.
- **OsAlarmSetEvent**
  - UUID: `ECUC:135c6787-8aad-4ca3-9c1b-f9db78eea4c0`
  - 描述: This container specifies the parameters to set an event

**容器描述**:

This container defines which type of notification is used when the alarm expires.

##### 2. OsAlarmActivateTask

**容器属性**:

- **UUID**: `ECUC:778af345-37da-4297-a5cf-617140faa94f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `OsAlarmActivateTask`
- **多重性**: [0..1]

**容器描述**:

This container specifies the parameters to activate a task.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. OsAlarmActivateTaskRef

- **UUID**: `ECUC:9d760cf7-d9fc-4fcf-a65f-1e5ac5d57eaf`
- **引用名**: `OsAlarmActivateTaskRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `OsTask`
- **完整路径**: `/AUTOSAR/EcucDefs/Os/OsTask`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the task that will be activated by that alarm action

##### 3. OsAlarmCallback

**容器属性**:

- **UUID**: `ECUC:d5df234a-b9c3-40e5-b30e-6ee6919a6c8e`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `OsAlarmCallback`
- **多重性**: [0..1]

**容器描述**:

This container specifies the parameters to call a callback OS alarm action.

###### 参数配置

此容器包含 **1** 个参数：

####### FUNCTION-NAME 类型参数

######## 1. OsAlarmCallbackName

- **UUID**: `ECUC:146cd561-a131-447a-8070-26ea050189b9`
- **参数名**: `OsAlarmCallbackName`
- **数据类型**: FUNCTION-NAME
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **函数变体**:
- **描述**: Name of the function that is called when this alarm callback is triggered.

##### 4. OsAlarmIncrementCounter

**容器属性**:

- **UUID**: `ECUC:e7f3faba-d482-41dd-9a78-a1bf24e96207`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `OsAlarmIncrementCounter`
- **多重性**: [0..1]

**容器描述**:

This container specifies the parameters to increment a counter.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. OsAlarmIncrementCounterRef

- **UUID**: `ECUC:f011f6a5-29e7-446b-85f5-b91034e9f12b`
- **引用名**: `OsAlarmIncrementCounterRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `OsCounter`
- **完整路径**: `/AUTOSAR/EcucDefs/Os/OsCounter`
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the counter that will be incremented by that alarm action

##### 5. OsAlarmSetEvent

**容器属性**:

- **UUID**: `ECUC:135c6787-8aad-4ca3-9c1b-f9db78eea4c0`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `OsAlarmSetEvent`
- **多重性**: [0..1]

**容器描述**:

This container specifies the parameters to set an event

###### 引用关系

此容器包含 **2** 个引用：

####### REFERENCE 类型引用

######## 1. OsAlarmSetEventRef

- **UUID**: `ECUC:1f077d18-ca8d-42bd-b867-4e59ce3d8e50`
- **引用名**: `OsAlarmSetEventRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `OsEvent`
- **完整路径**: `/AUTOSAR/EcucDefs/Os/OsEvent`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the event that will be set by that alarm action

######## 2. OsAlarmSetEventTaskRef

- **UUID**: `ECUC:db071009-6743-496a-ae4a-bb272eeb975a`
- **引用名**: `OsAlarmSetEventTaskRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `OsTask`
- **完整路径**: `/AUTOSAR/EcucDefs/Os/OsTask`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the task that will be activated by that event

##### 6. OsAlarmAutostart

**容器属性**:

- **UUID**: `ECUC:964053de-2482-4575-a091-31f2b2d62db1`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `OsAlarmAutostart`
- **多重性**: [0..1]

**容器描述**:

If present this container defines if an alarm is started automatically at system start-up depending on the application mode.

###### 参数配置

此容器包含 **3** 个参数：

####### INTEGER 类型参数

######## 1. OsAlarmAlarmTime

- **UUID**: `ECUC:60cfd12a-e181-4369-9286-c0432e6e5cf5`
- **参数名**: `OsAlarmAlarmTime`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..18446744073709551615]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: The relative or absolute tick value when the alarm expires for the first time. Note that for an alarm which is RELATIVE the value must be at bigger than 0.

######## 2. OsAlarmCycleTime

- **UUID**: `ECUC:3ad7702f-8f33-4b7d-87df-1fb32d89fb61`
- **参数名**: `OsAlarmCycleTime`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..18446744073709551615]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Cycle time of a cyclic alarm in ticks. If the value is 0 than the alarm is not cyclic.

####### ENUMERATION 类型参数

######## 1. OsAlarmAutostartType

- **UUID**: `ECUC:3aeb1a3f-7305-4179-b995-e284a9efb475`
- **参数名**: `OsAlarmAutostartType`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `ABSOLUTE` (来源: AUTOSAR_ECUC)
  - `RELATIVE` (来源: AUTOSAR_ECUC)
- **描述**: This specifies the type of autostart for the alarm..

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. OsAlarmAppModeRef

- **UUID**: `ECUC:a1c6da78-4cb0-4df2-92ae-69875adaedeb`
- **引用名**: `OsAlarmAppModeRef`
- **引用类型**: REFERENCE
- **多重性**: [1..infinite]
- **目标**: `OsAppMode`
- **完整路径**: `/AUTOSAR/EcucDefs/Os/OsAppMode`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the application modes for which the AUTOSTART shall be performed

##### 7. OsAppMode

**容器属性**:

- **UUID**: `ECUC:44b2af00-f4af-494b-9b23-6c4bd5ea9ca7`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `OsAppMode`
- **多重性**: [1..infinite]

**容器描述**:

OsAppMode is the object used to define OSEK OS properties for an OSEK OS application mode.

##### 8. OsApplication

**容器属性**:

- **UUID**: `ECUC:3fe22410-f7c0-4ae4-a89a-e6d8c2861115`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `OsApplication`
- **多重性**: [0..infinite]

**容器描述**:

An AUTOSAR OS must be capable of supporting a collection of OS objects (tasks, interrupts, alarms, hooks etc.) that form a cohesive functional unit. This collection of objects is termed an OS-Application.

###### 参数配置

此容器包含 **3** 个参数：

####### BOOLEAN 类型参数

######## 1. OsTrusted

- **UUID**: `ECUC:97ddd259-bb90-4c42-af70-aa8b24630faf`
- **参数名**: `OsTrusted`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Parameter to specify if an OS-Application is trusted or not.

######## 2. OsTrustedApplicationDelayTimingViolationCall

- **UUID**: `ECUC:fd5344b6-872d-4e27-a451-f55587b0a918`
- **参数名**: `OsTrustedApplicationDelayTimingViolationCall`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Parameter to specify if a timing violation which occurs within an trusted OS-Application is raised immediately of if it is delayed until the current task returns to the calling OS-Application (return of CallTrustedFunction)

######## 3. OsTrustedApplicationWithProtection

- **UUID**: `ECUC:e8a533a6-6a5d-4154-9ac4-2d7f90f12d44`
- **参数名**: `OsTrustedApplicationWithProtection`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Parameter to specify if a trusted OS-Application is executed with memory protection or not.

###### 引用关系

此容器包含 **8** 个引用：

####### REFERENCE 类型引用

######## 1. OsAppAlarmRef

- **UUID**: `ECUC:f682f3ec-e731-4683-9429-6f3139967bc4`
- **引用名**: `OsAppAlarmRef`
- **引用类型**: REFERENCE
- **多重性**: [0..infinite]
- **目标**: `OsAlarm`
- **完整路径**: `/AUTOSAR/EcucDefs/Os/OsAlarm`
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **描述**: Specifies the OsAlarms that belong to the OsApplication.

######## 2. OsAppCounterRef

- **UUID**: `ECUC:4a2dbf82-5e24-4d1b-b778-6691fa1cde23`
- **引用名**: `OsAppCounterRef`
- **引用类型**: REFERENCE
- **多重性**: [0..infinite]
- **目标**: `OsCounter`
- **完整路径**: `/AUTOSAR/EcucDefs/Os/OsCounter`
- **来源**: AUTOSAR_ECUC
- **描述**: References the OsCounters that belong to the OsApplication.

######## 3. OsAppEcucPartitionRef

- **UUID**: `ECUC:493ffec7-e80e-4945-bc55-09cfe0eb4c78`
- **引用名**: `OsAppEcucPartitionRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `EcucPartition`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPartitionCollection/EcucPartition`
- **来源**: AUTOSAR_ECUC
- **描述**: Denotes which "EcucPartition" is implemented by this "OSApplication".

######## 4. OsAppIsrRef

- **UUID**: `ECUC:ff388a32-96e2-44e3-852f-b565616152fb`
- **引用名**: `OsAppIsrRef`
- **引用类型**: REFERENCE
- **多重性**: [0..infinite]
- **目标**: `OsIsr`
- **完整路径**: `/AUTOSAR/EcucDefs/Os/OsIsr`
- **来源**: AUTOSAR_ECUC
- **描述**: references which OsIsrs belong to the OsApplication

######## 5. OsAppScheduleTableRef

- **UUID**: `ECUC:80e78dc3-aacf-442e-8c44-5b7ede865f44`
- **引用名**: `OsAppScheduleTableRef`
- **引用类型**: REFERENCE
- **多重性**: [0..infinite]
- **目标**: `OsScheduleTable`
- **完整路径**: `/AUTOSAR/EcucDefs/Os/OsScheduleTable`
- **来源**: AUTOSAR_ECUC
- **描述**: References the OsScheduleTables that belong to the OsApplication.

######## 6. OsAppTaskRef

- **UUID**: `ECUC:934a7899-f255-444b-a117-7d4ffead78e9`
- **引用名**: `OsAppTaskRef`
- **引用类型**: REFERENCE
- **多重性**: [0..infinite]
- **目标**: `OsTask`
- **完整路径**: `/AUTOSAR/EcucDefs/Os/OsTask`
- **来源**: AUTOSAR_ECUC
- **描述**: references which OsTasks belong to the OsApplication

######## 7. OsRestartTask

- **UUID**: `ECUC:d87bac0e-011a-4578-bfea-01885c0240f3`
- **引用名**: `OsRestartTask`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `OsTask`
- **完整路径**: `/AUTOSAR/EcucDefs/Os/OsTask`
- **来源**: AUTOSAR_ECUC
- **描述**: Optionally one task of an OS-Application may be defined as Restart Task.

####### SYMBOLIC-NAME-REFERENCE 类型引用

######## 1. OsApplicationCoreRef

- **UUID**: `ECUC:487eb46e-c2de-4b01-8138-31906865ee1f`
- **引用名**: `OsApplicationCoreRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `EcucCoreDefinition`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucHardware/EcucCoreDefinition`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the Core Definition in the Ecuc Module where the CoreId is defined. This reference is used to describe to which Core the OsApplication is bound.

###### 配置容器

本模块包含 **2** 个配置容器：

####### 1. OsApplicationHooks

**容器属性**:

- **UUID**: `ECUC:504b9c2f-8c8f-4650-878e-fbaa905cd5c6`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `OsApplicationHooks`
- **多重性**: [1..1]

**容器描述**:

Container to structure the OS-Application-specific hooks

######## 参数配置

此容器包含 **3** 个参数：

######### BOOLEAN 类型参数

########## 1. OsAppErrorHook

- **UUID**: `ECUC:dae2e0ce-2b38-4991-81df-93f1ebd88c4f`
- **参数名**: `OsAppErrorHook`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Select the OS-Application error hook.

########## 2. OsAppShutdownHook

- **UUID**: `ECUC:b0d64ef8-4929-4647-ac16-2c7e541a19a4`
- **参数名**: `OsAppShutdownHook`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Select the OS-Application specific shutdown hook for the OS-Application.

########## 3. OsAppStartupHook

- **UUID**: `ECUC:d30c7023-7afc-468a-86da-70498ba04654`
- **参数名**: `OsAppStartupHook`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Select the OS-Application specific startup hook for the OS-Application.

####### 2. OsApplicationTrustedFunction

**容器属性**:

- **UUID**: `ECUC:727531f6-47c8-441a-b36f-15d71e958b91`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `OsApplicationTrustedFunction`
- **多重性**: [0..infinite]

**容器描述**:

Container to structure the configuration parameters of trusted functions

######## 参数配置

此容器包含 **1** 个参数：

######### FUNCTION-NAME 类型参数

########## 1. OsTrustedFunctionName

- **UUID**: `ECUC:af3592ef-5e5c-4a29-8c5f-a3f80aa67ae7`
- **参数名**: `OsTrustedFunctionName`
- **数据类型**: FUNCTION-NAME
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **函数变体**:
- **描述**: Trusted function (as part of a trusted OS-Application) available to other OS-Applications. This also supersedes the OSEK OIL attribute TRUSTED in APPLICATION because the optionality of this parameter is describing that already.

##### 9. OsApplicationHooks

**容器属性**:

- **UUID**: `ECUC:504b9c2f-8c8f-4650-878e-fbaa905cd5c6`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `OsApplicationHooks`
- **多重性**: [1..1]

**容器描述**:

Container to structure the OS-Application-specific hooks

###### 参数配置

此容器包含 **3** 个参数：

####### BOOLEAN 类型参数

######## 1. OsAppErrorHook

- **UUID**: `ECUC:dae2e0ce-2b38-4991-81df-93f1ebd88c4f`
- **参数名**: `OsAppErrorHook`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Select the OS-Application error hook.

######## 2. OsAppShutdownHook

- **UUID**: `ECUC:b0d64ef8-4929-4647-ac16-2c7e541a19a4`
- **参数名**: `OsAppShutdownHook`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Select the OS-Application specific shutdown hook for the OS-Application.

######## 3. OsAppStartupHook

- **UUID**: `ECUC:d30c7023-7afc-468a-86da-70498ba04654`
- **参数名**: `OsAppStartupHook`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Select the OS-Application specific startup hook for the OS-Application.

##### 10. OsApplicationTrustedFunction

**容器属性**:

- **UUID**: `ECUC:727531f6-47c8-441a-b36f-15d71e958b91`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `OsApplicationTrustedFunction`
- **多重性**: [0..infinite]

**容器描述**:

Container to structure the configuration parameters of trusted functions

###### 参数配置

此容器包含 **1** 个参数：

####### FUNCTION-NAME 类型参数

######## 1. OsTrustedFunctionName

- **UUID**: `ECUC:af3592ef-5e5c-4a29-8c5f-a3f80aa67ae7`
- **参数名**: `OsTrustedFunctionName`
- **数据类型**: FUNCTION-NAME
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **函数变体**:
- **描述**: Trusted function (as part of a trusted OS-Application) available to other OS-Applications. This also supersedes the OSEK OIL attribute TRUSTED in APPLICATION because the optionality of this parameter is describing that already.

##### 11. OsCounter

**容器属性**:

- **UUID**: `ECUC:027f4979-a1d4-4ba0-a615-19a5a8081073`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `OsCounter`
- **多重性**: [0..infinite]

**容器描述**:

Configuration information for the counters that belong to the OsApplication.

###### 参数配置

此容器包含 **5** 个参数：

####### INTEGER 类型参数

######## 1. OsCounterMaxAllowedValue

- **UUID**: `ECUC:deceab52-a44e-40eb-9737-8eea4e860802`
- **参数名**: `OsCounterMaxAllowedValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..18446744073709551615]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Maximum possible allowed value of the system counter in ticks.

######## 2. OsCounterMinCycle

- **UUID**: `ECUC:4a0415c2-c296-49d6-b76a-3ce3e75112f3`
- **参数名**: `OsCounterMinCycle`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..18446744073709551615]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: The MINCYCLE attribute specifies the minimum allowed number of counter ticks for a cyclic alarm linked to the counter.

######## 3. OsCounterTicksPerBase

- **UUID**: `ECUC:25d694e2-85d2-4c8a-9ceb-6abafafbf40b`
- **参数名**: `OsCounterTicksPerBase`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: The TICKSPERBASE attribute specifies the number of ticks required to reach a counterspecific unit. The interpretation is implementation-specific.

####### FLOAT 类型参数

######## 1. OsSecondsPerTick

- **UUID**: `ECUC:7cbe21f0-2e73-4fc2-928e-3337f481cb10`
- **参数名**: `OsSecondsPerTick`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **取值范围**: [0..Inf]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Time of one counter tick in seconds.

####### ENUMERATION 类型参数

######## 1. OsCounterType

- **UUID**: `ECUC:77593730-3c82-4979-ba08-f9678e001cf3`
- **参数名**: `OsCounterType`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `HARDWARE` (来源: AUTOSAR_ECUC)
  - `SOFTWARE` (来源: AUTOSAR_ECUC)
- **描述**: This parameter contains the natural type or unit of the counter.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. OsCounterAccessingApplication

- **UUID**: `ECUC:48c50338-5eac-440a-860d-4158ed36ae2d`
- **引用名**: `OsCounterAccessingApplication`
- **引用类型**: REFERENCE
- **多重性**: [0..infinite]
- **目标**: `OsApplication`
- **完整路径**: `/AUTOSAR/EcucDefs/Os/OsApplication`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to applications which have an access to this object.

###### 配置容器

本模块包含 **2** 个配置容器：

####### 1. OsDriver

**容器属性**:

- **UUID**: `ECUC:5187c6ca-a5b2-4939-b6e0-1d5775ef679e`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `OsDriver`
- **多重性**: [0..1]

**容器描述**:

This Container contains the information who will drive the counter.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. OsGptChannelRef

- **UUID**: `ECUC:7a91b0f3-8545-4fb3-aa38-252294367014`
- **引用名**: `OsGptChannelRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `GptChannelConfiguration`
- **完整路径**: `/AUTOSAR/EcucDefs/Gpt/GptChannelConfigSet/GptChannelConfiguration`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the GPT channel.

####### 2. OsTimeConstant

**容器属性**:

- **UUID**: `ECUC:6488e442-e1ab-4d9a-9974-22cb3a102f4a`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `OsTimeConstant`
- **多重性**: [0..infinite]

**容器描述**:

Allows the user to define constants which can be e.g. used to compare time values with timer tick values.

######## 参数配置

此容器包含 **1** 个参数：

######### FLOAT 类型参数

########## 1. OsTimeValue

- **UUID**: `ECUC:daba8b10-b46e-4dc9-a6d3-8f6ab1126f30`
- **参数名**: `OsTimeValue`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0..Inf]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: This parameter contains the value of the constant in seconds.

##### 12. OsDriver

**容器属性**:

- **UUID**: `ECUC:5187c6ca-a5b2-4939-b6e0-1d5775ef679e`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `OsDriver`
- **多重性**: [0..1]

**容器描述**:

This Container contains the information who will drive the counter.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. OsGptChannelRef

- **UUID**: `ECUC:7a91b0f3-8545-4fb3-aa38-252294367014`
- **引用名**: `OsGptChannelRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `GptChannelConfiguration`
- **完整路径**: `/AUTOSAR/EcucDefs/Gpt/GptChannelConfigSet/GptChannelConfiguration`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the GPT channel.

##### 13. OsTimeConstant

**容器属性**:

- **UUID**: `ECUC:6488e442-e1ab-4d9a-9974-22cb3a102f4a`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `OsTimeConstant`
- **多重性**: [0..infinite]

**容器描述**:

Allows the user to define constants which can be e.g. used to compare time values with timer tick values.

###### 参数配置

此容器包含 **1** 个参数：

####### FLOAT 类型参数

######## 1. OsTimeValue

- **UUID**: `ECUC:daba8b10-b46e-4dc9-a6d3-8f6ab1126f30`
- **参数名**: `OsTimeValue`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0..Inf]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: This parameter contains the value of the constant in seconds.

##### 14. OsEvent

**容器属性**:

- **UUID**: `ECUC:08ff8745-1b33-4b16-829b-c1d7190a6ae6`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `OsEvent`
- **多重性**: [0..infinite]

**容器描述**:

Representation of OS events in the configuration context. Adopted from the OSEK OIL specification.

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. OsEventMask

- **UUID**: `ECUC:51c76d97-345c-4b78-9e45-25dd67fe7095`
- **参数名**: `OsEventMask`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: If event mask would be set to AUTO in OIL, this parameter should be omitted here.

##### 15. OsIoc

**容器属性**:

- **UUID**: `ECUC:8b83effd-234a-4731-8213-0b637df7eefc`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `OsIoc`
- **多重性**: [0..1]

**容器描述**:

Configuration of the IOC (Inter OS Application Communicator).

###### 配置容器

本模块包含 **4** 个配置容器：

####### 1. OsIocCommunication

**容器属性**:

- **UUID**: `ECUC:aba13287-7385-453e-9e67-fbdbe8c9f86f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `OsIocCommunication`
- **多重性**: [0..infinite]

**容器描述**:

Representation of a 1:1 or N:1 or N:M (unqueued only) communication between software parts located in different OS-Applications that are bound to the same or to different cores.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. OsIocBufferLength

- **UUID**: `ECUC:c70d8576-6d52-46f7-b8ff-17c313e635ea`
- **参数名**: `OsIocBufferLength`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: This attribute defines the size of the IOC internal queue to be allocated for a queued communication.

######## 配置容器

本模块包含 **3** 个配置容器：

######### 1. OsIocDataProperties

**容器属性**:

- **UUID**: `ECUC:5c503fab-e8a7-4dce-84b9-6d58467b7611`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `OsIocDataProperties`
- **多重性**: [1..infinite]

**容器描述**:

Data properties of the data to be transferred on the IOC communication channel.

########## 参数配置

此容器包含 **2** 个参数：

########### INTEGER 类型参数

############ 1. OsIocDataPropertyIndex

- **UUID**: `ECUC:ac4396f5-cb92-4713-b285-e5f8ea079275`
- **参数名**: `OsIocDataPropertyIndex`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: This parameter is used to define in which order the data is send, e.g. whether IocSendGroup(A,B) or IocSendGroup(B,A) shall be used.

########### STRING 类型参数

############ 1. OsIocInitValue

- **UUID**: `ECUC:8986f06e-9232-4f20-aec6-a8dcd936d1e8`
- **参数名**: `OsIocInitValue`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **描述**: Initial Value for the data to be transferred on the IOC communication channel.

########## 引用关系

此容器包含 **1** 个引用：

########### FOREIGN-REFERENCE 类型引用

############ 1. OsIocDataTypeRef

- **UUID**: `ECUC:37e02eb6-462c-41c1-9ca8-05f8ffd1c014`
- **引用名**: `OsIocDataTypeRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [1..1]
- **目标类型**: IMPLEMENTATION-DATA-TYPE
- **来源**: AUTOSAR_ECUC
- **描述**: This is the type of the data to be transferred on the IOC communication channel. This attribute is necessary to generate the parameter type of the Ioc functions. Additionally this information should be used to compute the data size for necessary data copy operations within the Ioc module.

######### 2. OsIocReceiverProperties

**容器属性**:

- **UUID**: `ECUC:7748837c-c78f-4d1d-be0a-96a61a7b5d03`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `OsIocReceiverProperties`
- **多重性**: [1..infinite]

**容器描述**:

Representation of receiver properties for one communication. For each OsIocCommunication one (1:1) or many receivers (N:M) have to be defined.  This container should be instantiated within an OsIocCommunication.

########## 参数配置

此容器包含 **2** 个参数：

########### ENUMERATION 类型参数

############ 1. OsIocFunctionImplementationKind

- **UUID**: `ECUC:7d3d9611-afaf-921c-4cc6-9a6878ace501`
- **参数名**: `OsIocFunctionImplementationKind`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `DO_NOT_CARE`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `DO_NOT_CARE` (来源: AUTOSAR_ECUC)
  - `FUNCTION` (来源: AUTOSAR_ECUC)
  - `MACRO` (来源: AUTOSAR_ECUC)
- **描述**: This parameter is used to select whether this communication is implemented as a macro or as a function.

########### FUNCTION-NAME 类型参数

############ 1. OsIocReceiverPullCB

- **UUID**: `ECUC:6a5d33f7-6833-492a-a7df-60cbc722edd6`
- **参数名**: `OsIocReceiverPullCB`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **函数变体**:
- **描述**: This attribute defines the name of a callback function that the IOC shall call on the receiving core for each data reception.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. OsIocReceivingOsApplicationRef

- **UUID**: `ECUC:4f6d8b5f-01eb-47c6-a977-9ac5a00359fd`
- **引用名**: `OsIocReceivingOsApplicationRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `OsApplication`
- **完整路径**: `/AUTOSAR/EcucDefs/Os/OsApplication`
- **来源**: AUTOSAR_ECUC
- **描述**: This attribute is a reference to the receiving OsApplication instance defined in the configuration file of the OS.

######### 3. OsIocSenderProperties

**容器属性**:

- **UUID**: `ECUC:19574439-317b-4c79-839b-e2e1db7db6ee`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `OsIocSenderProperties`
- **多重性**: [1..infinite]

**容器描述**:

Representation of sender properties for one communication. For each OsIocCommunication one (1:1) or many senders (N:1 or N:M) have to be defined. Multiplicity > 1 (N:1 or N:M communication) is only allowed for Multiplicity of OsIocDataTypeRef = 1.

########## 参数配置

此容器包含 **2** 个参数：

########### INTEGER 类型参数

############ 1. OsIocSenderId

- **UUID**: `ECUC:37e0ea2c-99bb-44bc-bd7c-022e8bfe7d41`
- **参数名**: `OsIocSenderId`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Representation of a sender in a N:1 or N:M communication to distinguish between senders.

########### ENUMERATION 类型参数

############ 1. OsIocFunctionImplementationKind

- **UUID**: `ECUC:1f4c56ce-199b-9178-1257-e6a439af3eec`
- **参数名**: `OsIocFunctionImplementationKind`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `DO_NOT_CARE`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `DO_NOT_CARE` (来源: AUTOSAR_ECUC)
  - `FUNCTION` (来源: AUTOSAR_ECUC)
  - `MACRO` (来源: AUTOSAR_ECUC)
- **描述**: This parameter is used to select whether this communication is implemented as a macro or as a function.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. OsIocSendingOsApplicationRef

- **UUID**: `ECUC:45c166df-7068-47de-84b7-75ed075aab39`
- **引用名**: `OsIocSendingOsApplicationRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `OsApplication`
- **完整路径**: `/AUTOSAR/EcucDefs/Os/OsApplication`
- **来源**: AUTOSAR_ECUC
- **描述**: This attribute is a reference to the sending OS-Application instance defined in the configuration file of the OS.

####### 2. OsIocDataProperties

**容器属性**:

- **UUID**: `ECUC:5c503fab-e8a7-4dce-84b9-6d58467b7611`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `OsIocDataProperties`
- **多重性**: [1..infinite]

**容器描述**:

Data properties of the data to be transferred on the IOC communication channel.

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. OsIocDataPropertyIndex

- **UUID**: `ECUC:ac4396f5-cb92-4713-b285-e5f8ea079275`
- **参数名**: `OsIocDataPropertyIndex`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: This parameter is used to define in which order the data is send, e.g. whether IocSendGroup(A,B) or IocSendGroup(B,A) shall be used.

######### STRING 类型参数

########## 1. OsIocInitValue

- **UUID**: `ECUC:8986f06e-9232-4f20-aec6-a8dcd936d1e8`
- **参数名**: `OsIocInitValue`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **描述**: Initial Value for the data to be transferred on the IOC communication channel.

######## 引用关系

此容器包含 **1** 个引用：

######### FOREIGN-REFERENCE 类型引用

########## 1. OsIocDataTypeRef

- **UUID**: `ECUC:37e02eb6-462c-41c1-9ca8-05f8ffd1c014`
- **引用名**: `OsIocDataTypeRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [1..1]
- **目标类型**: IMPLEMENTATION-DATA-TYPE
- **来源**: AUTOSAR_ECUC
- **描述**: This is the type of the data to be transferred on the IOC communication channel. This attribute is necessary to generate the parameter type of the Ioc functions. Additionally this information should be used to compute the data size for necessary data copy operations within the Ioc module.

####### 3. OsIocReceiverProperties

**容器属性**:

- **UUID**: `ECUC:7748837c-c78f-4d1d-be0a-96a61a7b5d03`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `OsIocReceiverProperties`
- **多重性**: [1..infinite]

**容器描述**:

Representation of receiver properties for one communication. For each OsIocCommunication one (1:1) or many receivers (N:M) have to be defined.  This container should be instantiated within an OsIocCommunication.

######## 参数配置

此容器包含 **2** 个参数：

######### ENUMERATION 类型参数

########## 1. OsIocFunctionImplementationKind

- **UUID**: `ECUC:7d3d9611-afaf-921c-4cc6-9a6878ace501`
- **参数名**: `OsIocFunctionImplementationKind`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `DO_NOT_CARE`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `DO_NOT_CARE` (来源: AUTOSAR_ECUC)
  - `FUNCTION` (来源: AUTOSAR_ECUC)
  - `MACRO` (来源: AUTOSAR_ECUC)
- **描述**: This parameter is used to select whether this communication is implemented as a macro or as a function.

######### FUNCTION-NAME 类型参数

########## 1. OsIocReceiverPullCB

- **UUID**: `ECUC:6a5d33f7-6833-492a-a7df-60cbc722edd6`
- **参数名**: `OsIocReceiverPullCB`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **函数变体**:
- **描述**: This attribute defines the name of a callback function that the IOC shall call on the receiving core for each data reception.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. OsIocReceivingOsApplicationRef

- **UUID**: `ECUC:4f6d8b5f-01eb-47c6-a977-9ac5a00359fd`
- **引用名**: `OsIocReceivingOsApplicationRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `OsApplication`
- **完整路径**: `/AUTOSAR/EcucDefs/Os/OsApplication`
- **来源**: AUTOSAR_ECUC
- **描述**: This attribute is a reference to the receiving OsApplication instance defined in the configuration file of the OS.

####### 4. OsIocSenderProperties

**容器属性**:

- **UUID**: `ECUC:19574439-317b-4c79-839b-e2e1db7db6ee`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `OsIocSenderProperties`
- **多重性**: [1..infinite]

**容器描述**:

Representation of sender properties for one communication. For each OsIocCommunication one (1:1) or many senders (N:1 or N:M) have to be defined. Multiplicity > 1 (N:1 or N:M communication) is only allowed for Multiplicity of OsIocDataTypeRef = 1.

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. OsIocSenderId

- **UUID**: `ECUC:37e0ea2c-99bb-44bc-bd7c-022e8bfe7d41`
- **参数名**: `OsIocSenderId`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Representation of a sender in a N:1 or N:M communication to distinguish between senders.

######### ENUMERATION 类型参数

########## 1. OsIocFunctionImplementationKind

- **UUID**: `ECUC:1f4c56ce-199b-9178-1257-e6a439af3eec`
- **参数名**: `OsIocFunctionImplementationKind`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `DO_NOT_CARE`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `DO_NOT_CARE` (来源: AUTOSAR_ECUC)
  - `FUNCTION` (来源: AUTOSAR_ECUC)
  - `MACRO` (来源: AUTOSAR_ECUC)
- **描述**: This parameter is used to select whether this communication is implemented as a macro or as a function.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. OsIocSendingOsApplicationRef

- **UUID**: `ECUC:45c166df-7068-47de-84b7-75ed075aab39`
- **引用名**: `OsIocSendingOsApplicationRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `OsApplication`
- **完整路径**: `/AUTOSAR/EcucDefs/Os/OsApplication`
- **来源**: AUTOSAR_ECUC
- **描述**: This attribute is a reference to the sending OS-Application instance defined in the configuration file of the OS.

##### 16. OsIocCommunication

**容器属性**:

- **UUID**: `ECUC:aba13287-7385-453e-9e67-fbdbe8c9f86f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `OsIocCommunication`
- **多重性**: [0..infinite]

**容器描述**:

Representation of a 1:1 or N:1 or N:M (unqueued only) communication between software parts located in different OS-Applications that are bound to the same or to different cores.

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. OsIocBufferLength

- **UUID**: `ECUC:c70d8576-6d52-46f7-b8ff-17c313e635ea`
- **参数名**: `OsIocBufferLength`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: This attribute defines the size of the IOC internal queue to be allocated for a queued communication.

###### 配置容器

本模块包含 **3** 个配置容器：

####### 1. OsIocDataProperties

**容器属性**:

- **UUID**: `ECUC:5c503fab-e8a7-4dce-84b9-6d58467b7611`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `OsIocDataProperties`
- **多重性**: [1..infinite]

**容器描述**:

Data properties of the data to be transferred on the IOC communication channel.

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. OsIocDataPropertyIndex

- **UUID**: `ECUC:ac4396f5-cb92-4713-b285-e5f8ea079275`
- **参数名**: `OsIocDataPropertyIndex`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: This parameter is used to define in which order the data is send, e.g. whether IocSendGroup(A,B) or IocSendGroup(B,A) shall be used.

######### STRING 类型参数

########## 1. OsIocInitValue

- **UUID**: `ECUC:8986f06e-9232-4f20-aec6-a8dcd936d1e8`
- **参数名**: `OsIocInitValue`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **描述**: Initial Value for the data to be transferred on the IOC communication channel.

######## 引用关系

此容器包含 **1** 个引用：

######### FOREIGN-REFERENCE 类型引用

########## 1. OsIocDataTypeRef

- **UUID**: `ECUC:37e02eb6-462c-41c1-9ca8-05f8ffd1c014`
- **引用名**: `OsIocDataTypeRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [1..1]
- **目标类型**: IMPLEMENTATION-DATA-TYPE
- **来源**: AUTOSAR_ECUC
- **描述**: This is the type of the data to be transferred on the IOC communication channel. This attribute is necessary to generate the parameter type of the Ioc functions. Additionally this information should be used to compute the data size for necessary data copy operations within the Ioc module.

####### 2. OsIocReceiverProperties

**容器属性**:

- **UUID**: `ECUC:7748837c-c78f-4d1d-be0a-96a61a7b5d03`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `OsIocReceiverProperties`
- **多重性**: [1..infinite]

**容器描述**:

Representation of receiver properties for one communication. For each OsIocCommunication one (1:1) or many receivers (N:M) have to be defined.  This container should be instantiated within an OsIocCommunication.

######## 参数配置

此容器包含 **2** 个参数：

######### ENUMERATION 类型参数

########## 1. OsIocFunctionImplementationKind

- **UUID**: `ECUC:7d3d9611-afaf-921c-4cc6-9a6878ace501`
- **参数名**: `OsIocFunctionImplementationKind`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `DO_NOT_CARE`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `DO_NOT_CARE` (来源: AUTOSAR_ECUC)
  - `FUNCTION` (来源: AUTOSAR_ECUC)
  - `MACRO` (来源: AUTOSAR_ECUC)
- **描述**: This parameter is used to select whether this communication is implemented as a macro or as a function.

######### FUNCTION-NAME 类型参数

########## 1. OsIocReceiverPullCB

- **UUID**: `ECUC:6a5d33f7-6833-492a-a7df-60cbc722edd6`
- **参数名**: `OsIocReceiverPullCB`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **函数变体**:
- **描述**: This attribute defines the name of a callback function that the IOC shall call on the receiving core for each data reception.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. OsIocReceivingOsApplicationRef

- **UUID**: `ECUC:4f6d8b5f-01eb-47c6-a977-9ac5a00359fd`
- **引用名**: `OsIocReceivingOsApplicationRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `OsApplication`
- **完整路径**: `/AUTOSAR/EcucDefs/Os/OsApplication`
- **来源**: AUTOSAR_ECUC
- **描述**: This attribute is a reference to the receiving OsApplication instance defined in the configuration file of the OS.

####### 3. OsIocSenderProperties

**容器属性**:

- **UUID**: `ECUC:19574439-317b-4c79-839b-e2e1db7db6ee`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `OsIocSenderProperties`
- **多重性**: [1..infinite]

**容器描述**:

Representation of sender properties for one communication. For each OsIocCommunication one (1:1) or many senders (N:1 or N:M) have to be defined. Multiplicity > 1 (N:1 or N:M communication) is only allowed for Multiplicity of OsIocDataTypeRef = 1.

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. OsIocSenderId

- **UUID**: `ECUC:37e0ea2c-99bb-44bc-bd7c-022e8bfe7d41`
- **参数名**: `OsIocSenderId`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Representation of a sender in a N:1 or N:M communication to distinguish between senders.

######### ENUMERATION 类型参数

########## 1. OsIocFunctionImplementationKind

- **UUID**: `ECUC:1f4c56ce-199b-9178-1257-e6a439af3eec`
- **参数名**: `OsIocFunctionImplementationKind`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `DO_NOT_CARE`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `DO_NOT_CARE` (来源: AUTOSAR_ECUC)
  - `FUNCTION` (来源: AUTOSAR_ECUC)
  - `MACRO` (来源: AUTOSAR_ECUC)
- **描述**: This parameter is used to select whether this communication is implemented as a macro or as a function.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. OsIocSendingOsApplicationRef

- **UUID**: `ECUC:45c166df-7068-47de-84b7-75ed075aab39`
- **引用名**: `OsIocSendingOsApplicationRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `OsApplication`
- **完整路径**: `/AUTOSAR/EcucDefs/Os/OsApplication`
- **来源**: AUTOSAR_ECUC
- **描述**: This attribute is a reference to the sending OS-Application instance defined in the configuration file of the OS.

##### 17. OsIocDataProperties

**容器属性**:

- **UUID**: `ECUC:5c503fab-e8a7-4dce-84b9-6d58467b7611`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `OsIocDataProperties`
- **多重性**: [1..infinite]

**容器描述**:

Data properties of the data to be transferred on the IOC communication channel.

###### 参数配置

此容器包含 **2** 个参数：

####### INTEGER 类型参数

######## 1. OsIocDataPropertyIndex

- **UUID**: `ECUC:ac4396f5-cb92-4713-b285-e5f8ea079275`
- **参数名**: `OsIocDataPropertyIndex`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: This parameter is used to define in which order the data is send, e.g. whether IocSendGroup(A,B) or IocSendGroup(B,A) shall be used.

####### STRING 类型参数

######## 1. OsIocInitValue

- **UUID**: `ECUC:8986f06e-9232-4f20-aec6-a8dcd936d1e8`
- **参数名**: `OsIocInitValue`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **描述**: Initial Value for the data to be transferred on the IOC communication channel.

###### 引用关系

此容器包含 **1** 个引用：

####### FOREIGN-REFERENCE 类型引用

######## 1. OsIocDataTypeRef

- **UUID**: `ECUC:37e02eb6-462c-41c1-9ca8-05f8ffd1c014`
- **引用名**: `OsIocDataTypeRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [1..1]
- **目标类型**: IMPLEMENTATION-DATA-TYPE
- **来源**: AUTOSAR_ECUC
- **描述**: This is the type of the data to be transferred on the IOC communication channel. This attribute is necessary to generate the parameter type of the Ioc functions. Additionally this information should be used to compute the data size for necessary data copy operations within the Ioc module.

##### 18. OsIocReceiverProperties

**容器属性**:

- **UUID**: `ECUC:7748837c-c78f-4d1d-be0a-96a61a7b5d03`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `OsIocReceiverProperties`
- **多重性**: [1..infinite]

**容器描述**:

Representation of receiver properties for one communication. For each OsIocCommunication one (1:1) or many receivers (N:M) have to be defined.  This container should be instantiated within an OsIocCommunication.

###### 参数配置

此容器包含 **2** 个参数：

####### ENUMERATION 类型参数

######## 1. OsIocFunctionImplementationKind

- **UUID**: `ECUC:7d3d9611-afaf-921c-4cc6-9a6878ace501`
- **参数名**: `OsIocFunctionImplementationKind`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `DO_NOT_CARE`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `DO_NOT_CARE` (来源: AUTOSAR_ECUC)
  - `FUNCTION` (来源: AUTOSAR_ECUC)
  - `MACRO` (来源: AUTOSAR_ECUC)
- **描述**: This parameter is used to select whether this communication is implemented as a macro or as a function.

####### FUNCTION-NAME 类型参数

######## 1. OsIocReceiverPullCB

- **UUID**: `ECUC:6a5d33f7-6833-492a-a7df-60cbc722edd6`
- **参数名**: `OsIocReceiverPullCB`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **函数变体**:
- **描述**: This attribute defines the name of a callback function that the IOC shall call on the receiving core for each data reception.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. OsIocReceivingOsApplicationRef

- **UUID**: `ECUC:4f6d8b5f-01eb-47c6-a977-9ac5a00359fd`
- **引用名**: `OsIocReceivingOsApplicationRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `OsApplication`
- **完整路径**: `/AUTOSAR/EcucDefs/Os/OsApplication`
- **来源**: AUTOSAR_ECUC
- **描述**: This attribute is a reference to the receiving OsApplication instance defined in the configuration file of the OS.

##### 19. OsIocSenderProperties

**容器属性**:

- **UUID**: `ECUC:19574439-317b-4c79-839b-e2e1db7db6ee`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `OsIocSenderProperties`
- **多重性**: [1..infinite]

**容器描述**:

Representation of sender properties for one communication. For each OsIocCommunication one (1:1) or many senders (N:1 or N:M) have to be defined. Multiplicity > 1 (N:1 or N:M communication) is only allowed for Multiplicity of OsIocDataTypeRef = 1.

###### 参数配置

此容器包含 **2** 个参数：

####### INTEGER 类型参数

######## 1. OsIocSenderId

- **UUID**: `ECUC:37e0ea2c-99bb-44bc-bd7c-022e8bfe7d41`
- **参数名**: `OsIocSenderId`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Representation of a sender in a N:1 or N:M communication to distinguish between senders.

####### ENUMERATION 类型参数

######## 1. OsIocFunctionImplementationKind

- **UUID**: `ECUC:1f4c56ce-199b-9178-1257-e6a439af3eec`
- **参数名**: `OsIocFunctionImplementationKind`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `DO_NOT_CARE`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `DO_NOT_CARE` (来源: AUTOSAR_ECUC)
  - `FUNCTION` (来源: AUTOSAR_ECUC)
  - `MACRO` (来源: AUTOSAR_ECUC)
- **描述**: This parameter is used to select whether this communication is implemented as a macro or as a function.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. OsIocSendingOsApplicationRef

- **UUID**: `ECUC:45c166df-7068-47de-84b7-75ed075aab39`
- **引用名**: `OsIocSendingOsApplicationRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `OsApplication`
- **完整路径**: `/AUTOSAR/EcucDefs/Os/OsApplication`
- **来源**: AUTOSAR_ECUC
- **描述**: This attribute is a reference to the sending OS-Application instance defined in the configuration file of the OS.

##### 20. OsIsr

**容器属性**:

- **UUID**: `ECUC:7d5716e3-c20e-4559-ba9c-2d90f50cfd28`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `OsIsr`
- **多重性**: [0..infinite]

**容器描述**:

The OsIsr container represents an OSEK interrupt service routine.

###### 参数配置

此容器包含 **1** 个参数：

####### ENUMERATION 类型参数

######## 1. OsIsrCategory

- **UUID**: `ECUC:5d95ea52-e3b6-4b84-bc0c-20a37ebfd672`
- **参数名**: `OsIsrCategory`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `CATEGORY_1` (来源: AUTOSAR_ECUC)
  - `CATEGORY_2` (来源: AUTOSAR_ECUC)
- **描述**: This attribute specifies the category of this ISR.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. OsIsrResourceRef

- **UUID**: `ECUC:eb6f779e-e5dd-4870-a9cb-8f784fcccebe`
- **引用名**: `OsIsrResourceRef`
- **引用类型**: REFERENCE
- **多重性**: [0..infinite]
- **目标**: `OsResource`
- **完整路径**: `/AUTOSAR/EcucDefs/Os/OsResource`
- **来源**: AUTOSAR_ECUC
- **描述**: This reference defines the resources accessed by this ISR.

###### 配置容器

本模块包含 **2** 个配置容器：

####### 1. OsIsrTimingProtection

**容器属性**:

- **UUID**: `ECUC:ed417020-f2f2-47e0-8abb-64e54cb4e8fd`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `OsIsrTimingProtection`
- **多重性**: [0..1]

**容器描述**:

This container contains all parameters which are related to timing protection

######## 参数配置

此容器包含 **4** 个参数：

######### FLOAT 类型参数

########## 1. OsIsrAllInterruptLockBudget

- **UUID**: `ECUC:911b5d2a-86c8-4a1c-9741-d1ada875c94e`
- **参数名**: `OsIsrAllInterruptLockBudget`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **取值范围**: [0..Inf]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: This parameter contains the maximum time for which the ISR is allowed to lock all interrupts (via SuspendAllInterrupts() or DisableAllInterrupts()) (in seconds).

########## 2. OsIsrExecutionBudget

- **UUID**: `ECUC:ff435610-1cde-4530-8b4d-1818caf9bf0f`
- **参数名**: `OsIsrExecutionBudget`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **取值范围**: [0..Inf]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: The parameter contains the maximum allowed execution time of the interrupt (in seconds).

########## 3. OsIsrOsInterruptLockBudget

- **UUID**: `ECUC:f13180b1-a237-4132-9f90-2e6e93e191cf`
- **参数名**: `OsIsrOsInterruptLockBudget`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **取值范围**: [0..Inf]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: This parameter contains the maximum time for which the ISR is allowed to lock all Category 2 interrupts (via SuspendOSInterrupts()) (in seconds).

########## 4. OsIsrTimeFrame

- **UUID**: `ECUC:3d855434-c46e-40a1-adcc-985f085d2efb`
- **参数名**: `OsIsrTimeFrame`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **取值范围**: [0..Inf]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: This parameter contains the minimum inter-arrival time between successive interrupts (in seconds).

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. OsIsrResourceLock

**容器属性**:

- **UUID**: `ECUC:2e290a5c-ef82-4b7d-8f75-d4bf62b2c3ab`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `OsIsrResourceLock`
- **多重性**: [0..infinite]

**容器描述**:

This container contains a list of times the interrupt uses resources.

########## 参数配置

此容器包含 **1** 个参数：

########### FLOAT 类型参数

############ 1. OsIsrResourceLockBudget

- **UUID**: `ECUC:3b769901-8b89-42be-b408-244ff46e3cbd`
- **参数名**: `OsIsrResourceLockBudget`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0..Inf]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: This parameter contains the maximum time the interrupt is allowed to hold the given resource (in seconds).

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. OsIsrResourceLockResourceRef

- **UUID**: `ECUC:7f296c7f-70f7-40db-85ce-c48b5974edb7`
- **引用名**: `OsIsrResourceLockResourceRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `OsResource`
- **完整路径**: `/AUTOSAR/EcucDefs/Os/OsResource`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the resource the locking time is depending on

####### 2. OsIsrResourceLock

**容器属性**:

- **UUID**: `ECUC:2e290a5c-ef82-4b7d-8f75-d4bf62b2c3ab`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `OsIsrResourceLock`
- **多重性**: [0..infinite]

**容器描述**:

This container contains a list of times the interrupt uses resources.

######## 参数配置

此容器包含 **1** 个参数：

######### FLOAT 类型参数

########## 1. OsIsrResourceLockBudget

- **UUID**: `ECUC:3b769901-8b89-42be-b408-244ff46e3cbd`
- **参数名**: `OsIsrResourceLockBudget`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0..Inf]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: This parameter contains the maximum time the interrupt is allowed to hold the given resource (in seconds).

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. OsIsrResourceLockResourceRef

- **UUID**: `ECUC:7f296c7f-70f7-40db-85ce-c48b5974edb7`
- **引用名**: `OsIsrResourceLockResourceRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `OsResource`
- **完整路径**: `/AUTOSAR/EcucDefs/Os/OsResource`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the resource the locking time is depending on

##### 21. OsIsrTimingProtection

**容器属性**:

- **UUID**: `ECUC:ed417020-f2f2-47e0-8abb-64e54cb4e8fd`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `OsIsrTimingProtection`
- **多重性**: [0..1]

**容器描述**:

This container contains all parameters which are related to timing protection

###### 参数配置

此容器包含 **4** 个参数：

####### FLOAT 类型参数

######## 1. OsIsrAllInterruptLockBudget

- **UUID**: `ECUC:911b5d2a-86c8-4a1c-9741-d1ada875c94e`
- **参数名**: `OsIsrAllInterruptLockBudget`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **取值范围**: [0..Inf]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: This parameter contains the maximum time for which the ISR is allowed to lock all interrupts (via SuspendAllInterrupts() or DisableAllInterrupts()) (in seconds).

######## 2. OsIsrExecutionBudget

- **UUID**: `ECUC:ff435610-1cde-4530-8b4d-1818caf9bf0f`
- **参数名**: `OsIsrExecutionBudget`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **取值范围**: [0..Inf]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: The parameter contains the maximum allowed execution time of the interrupt (in seconds).

######## 3. OsIsrOsInterruptLockBudget

- **UUID**: `ECUC:f13180b1-a237-4132-9f90-2e6e93e191cf`
- **参数名**: `OsIsrOsInterruptLockBudget`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **取值范围**: [0..Inf]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: This parameter contains the maximum time for which the ISR is allowed to lock all Category 2 interrupts (via SuspendOSInterrupts()) (in seconds).

######## 4. OsIsrTimeFrame

- **UUID**: `ECUC:3d855434-c46e-40a1-adcc-985f085d2efb`
- **参数名**: `OsIsrTimeFrame`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **取值范围**: [0..Inf]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: This parameter contains the minimum inter-arrival time between successive interrupts (in seconds).

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. OsIsrResourceLock

**容器属性**:

- **UUID**: `ECUC:2e290a5c-ef82-4b7d-8f75-d4bf62b2c3ab`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `OsIsrResourceLock`
- **多重性**: [0..infinite]

**容器描述**:

This container contains a list of times the interrupt uses resources.

######## 参数配置

此容器包含 **1** 个参数：

######### FLOAT 类型参数

########## 1. OsIsrResourceLockBudget

- **UUID**: `ECUC:3b769901-8b89-42be-b408-244ff46e3cbd`
- **参数名**: `OsIsrResourceLockBudget`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0..Inf]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: This parameter contains the maximum time the interrupt is allowed to hold the given resource (in seconds).

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. OsIsrResourceLockResourceRef

- **UUID**: `ECUC:7f296c7f-70f7-40db-85ce-c48b5974edb7`
- **引用名**: `OsIsrResourceLockResourceRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `OsResource`
- **完整路径**: `/AUTOSAR/EcucDefs/Os/OsResource`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the resource the locking time is depending on

##### 22. OsIsrResourceLock

**容器属性**:

- **UUID**: `ECUC:2e290a5c-ef82-4b7d-8f75-d4bf62b2c3ab`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `OsIsrResourceLock`
- **多重性**: [0..infinite]

**容器描述**:

This container contains a list of times the interrupt uses resources.

###### 参数配置

此容器包含 **1** 个参数：

####### FLOAT 类型参数

######## 1. OsIsrResourceLockBudget

- **UUID**: `ECUC:3b769901-8b89-42be-b408-244ff46e3cbd`
- **参数名**: `OsIsrResourceLockBudget`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0..Inf]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: This parameter contains the maximum time the interrupt is allowed to hold the given resource (in seconds).

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. OsIsrResourceLockResourceRef

- **UUID**: `ECUC:7f296c7f-70f7-40db-85ce-c48b5974edb7`
- **引用名**: `OsIsrResourceLockResourceRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `OsResource`
- **完整路径**: `/AUTOSAR/EcucDefs/Os/OsResource`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the resource the locking time is depending on

##### 23. OsOS

**容器属性**:

- **UUID**: `ECUC:037fee7c-9826-4ab9-9067-69b24b57fe12`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `OsOS`
- **多重性**: [1..1]

**容器描述**:

OS is the object used to define OSEK OS properties for an OSEK application.

###### 参数配置

此容器包含 **7** 个参数：

####### INTEGER 类型参数

######## 1. OsNumberOfCores

- **UUID**: `ECUC:1369dbe1-88b9-4ff5-83d3-a62c5cf4106a`
- **参数名**: `OsNumberOfCores`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [1..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Maximum number of cores that are controlled by the OS.

####### BOOLEAN 类型参数

######## 1. OsStackMonitoring

- **UUID**: `ECUC:5e09948e-f8cb-44c6-9e7a-3595c1a2a6c4`
- **参数名**: `OsStackMonitoring`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Select stack monitoring of Tasks/Category 2 ISRs

######## 2. OsUseGetServiceId

- **UUID**: `ECUC:412bc048-fac1-432d-af87-1267b11f565b`
- **参数名**: `OsUseGetServiceId`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: As defined by OSEK

######## 3. OsUseParameterAccess

- **UUID**: `ECUC:742e833a-68cd-431e-94d8-2321a014481d`
- **参数名**: `OsUseParameterAccess`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: As defined by OSEK

######## 4. OsUseResScheduler

- **UUID**: `ECUC:ca31f39a-5057-484b-8408-ca0d0ed82a46`
- **参数名**: `OsUseResScheduler`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: The OsUseResScheduler attribute defines whether the resource RES_SCHEDULER is used within the application.

####### ENUMERATION 类型参数

######## 1. OsScalabilityClass

- **UUID**: `ECUC:a4c62701-41c5-417c-8b66-16c90d6d111f`
- **参数名**: `OsScalabilityClass`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `SC1` (来源: AUTOSAR_ECUC)
  - `SC2` (来源: AUTOSAR_ECUC)
  - `SC3` (来源: AUTOSAR_ECUC)
  - `SC4` (来源: AUTOSAR_ECUC)
- **描述**: A scalability class for each System Object "OS" has to be selected. In order to customize the operating system to the needs of the user and to take full advantage of the processor features the operating system can be scaled according to the scalability classes.

######## 2. OsStatus

- **UUID**: `ECUC:75a1986f-1458-49fb-9feb-b84c6e58956e`
- **参数名**: `OsStatus`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `EXTENDED` (来源: AUTOSAR_ECUC)
  - `STANDARD` (来源: AUTOSAR_ECUC)
- **描述**: The Status attribute specifies whether a system with standard or extended status has to be used. Automatic assignment is not supported for this attribute.

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. OsHooks

**容器属性**:

- **UUID**: `ECUC:e03dab8e-c227-44c9-bf9b-38f0564bd4df`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `OsHooks`
- **多重性**: [1..1]

**容器描述**:

Container to structure all hooks belonging to the OS

######## 参数配置

此容器包含 **6** 个参数：

######### BOOLEAN 类型参数

########## 1. OsErrorHook

- **UUID**: `ECUC:825a1254-49f2-4f16-aa94-d9eedd045480`
- **参数名**: `OsErrorHook`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Error hook as defined by OSEK

########## 2. OsPostTaskHook

- **UUID**: `ECUC:67f9db57-53e9-4e0e-8e47-23cc534733b5`
- **参数名**: `OsPostTaskHook`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Post-task hook as defined by OSEK

########## 3. OsPreTaskHook

- **UUID**: `ECUC:fbfe7932-0338-461a-b87d-58af3a85bbcb`
- **参数名**: `OsPreTaskHook`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Pre-task hook as defined by OSEK

########## 4. OsProtectionHook

- **UUID**: `ECUC:bafbef31-9d83-4b29-b534-300490f20f1f`
- **参数名**: `OsProtectionHook`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Switch to enable/disable the call to the (user supplied) protection hook.

########## 5. OsShutdownHook

- **UUID**: `ECUC:69032d37-2751-420e-9b13-75625e8f3e9f`
- **参数名**: `OsShutdownHook`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Shutdown hook as defined by OSEK

########## 6. OsStartupHook

- **UUID**: `ECUC:591b0fc5-9552-4b15-99d8-74b85ac249bd`
- **参数名**: `OsStartupHook`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Startup hook as defined by OSEK

##### 24. OsHooks

**容器属性**:

- **UUID**: `ECUC:e03dab8e-c227-44c9-bf9b-38f0564bd4df`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `OsHooks`
- **多重性**: [1..1]

**容器描述**:

Container to structure all hooks belonging to the OS

###### 参数配置

此容器包含 **6** 个参数：

####### BOOLEAN 类型参数

######## 1. OsErrorHook

- **UUID**: `ECUC:825a1254-49f2-4f16-aa94-d9eedd045480`
- **参数名**: `OsErrorHook`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Error hook as defined by OSEK

######## 2. OsPostTaskHook

- **UUID**: `ECUC:67f9db57-53e9-4e0e-8e47-23cc534733b5`
- **参数名**: `OsPostTaskHook`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Post-task hook as defined by OSEK

######## 3. OsPreTaskHook

- **UUID**: `ECUC:fbfe7932-0338-461a-b87d-58af3a85bbcb`
- **参数名**: `OsPreTaskHook`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Pre-task hook as defined by OSEK

######## 4. OsProtectionHook

- **UUID**: `ECUC:bafbef31-9d83-4b29-b534-300490f20f1f`
- **参数名**: `OsProtectionHook`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Switch to enable/disable the call to the (user supplied) protection hook.

######## 5. OsShutdownHook

- **UUID**: `ECUC:69032d37-2751-420e-9b13-75625e8f3e9f`
- **参数名**: `OsShutdownHook`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Shutdown hook as defined by OSEK

######## 6. OsStartupHook

- **UUID**: `ECUC:591b0fc5-9552-4b15-99d8-74b85ac249bd`
- **参数名**: `OsStartupHook`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Startup hook as defined by OSEK

##### 25. OsResource

**容器属性**:

- **UUID**: `ECUC:8a186c09-bd3e-413f-869f-40b71e71b89e`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `OsResource`
- **多重性**: [0..infinite]

**容器描述**:

An OsResource object is used to co-ordinate the concurrent access by tasks and ISRs to a shared resource, e.g. the scheduler, any program sequence, memory or any hardware area.

###### 参数配置

此容器包含 **1** 个参数：

####### ENUMERATION 类型参数

######## 1. OsResourceProperty

- **UUID**: `ECUC:00ff7313-1773-4a7c-a3f0-236baeb9dab5`
- **参数名**: `OsResourceProperty`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `INTERNAL` (来源: AUTOSAR_ECUC)
  - `LINKED` (来源: AUTOSAR_ECUC)
  - `STANDARD` (来源: AUTOSAR_ECUC)
- **描述**: This specifies the type of the resource.

###### 引用关系

此容器包含 **2** 个引用：

####### REFERENCE 类型引用

######## 1. OsResourceAccessingApplication

- **UUID**: `ECUC:feec2b3b-2a1e-4939-a9bf-f1debcd01166`
- **引用名**: `OsResourceAccessingApplication`
- **引用类型**: REFERENCE
- **多重性**: [0..infinite]
- **目标**: `OsApplication`
- **完整路径**: `/AUTOSAR/EcucDefs/Os/OsApplication`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to applications which have an access to this object.

######## 2. OsResourceLinkedResourceRef

- **UUID**: `ECUC:9ce7daad-5838-4fdb-aedd-031c7f5691cd`
- **引用名**: `OsResourceLinkedResourceRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `OsResource`
- **完整路径**: `/AUTOSAR/EcucDefs/Os/OsResource`
- **来源**: AUTOSAR_ECUC
- **描述**: The link to the resource. Must be valid if OsResourceProperty is LINKED. If OsResourceProperty is not LINKED the value is ignored.

##### 26. OsScheduleTable

**容器属性**:

- **UUID**: `ECUC:523c4517-6584-40ca-957a-8327c5c01843`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `OsScheduleTable`
- **多重性**: [0..infinite]

**容器描述**:

An OsScheduleTable addresses the synchronization issue by providing an encapsulation of a statically defined set of alarms that cannot be modified at runtime.

###### 参数配置

此容器包含 **2** 个参数：

####### INTEGER 类型参数

######## 1. OsScheduleTableDuration

- **UUID**: `ECUC:65aea8af-eeef-43c7-81bf-bec539d2290d`
- **参数名**: `OsScheduleTableDuration`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: This parameter defines the modulus of the schedule table (in ticks).

####### BOOLEAN 类型参数

######## 1. OsScheduleTableRepeating

- **UUID**: `ECUC:c901492e-c50c-45d9-9c20-9448c2f26a40`
- **参数名**: `OsScheduleTableRepeating`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: true: first expiry point on the schedule table shall be processed at final expiry point delay ticks after the final expiry point is processed.

###### 引用关系

此容器包含 **2** 个引用：

####### REFERENCE 类型引用

######## 1. OsSchTblAccessingApplication

- **UUID**: `ECUC:f3dc4356-37e5-4f5e-9aa9-6f9fbe362508`
- **引用名**: `OsSchTblAccessingApplication`
- **引用类型**: REFERENCE
- **多重性**: [0..infinite]
- **目标**: `OsApplication`
- **完整路径**: `/AUTOSAR/EcucDefs/Os/OsApplication`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to applications which have an access to this object.

######## 2. OsScheduleTableCounterRef

- **UUID**: `ECUC:f1c26a81-2cfd-4626-8d21-ad2e90b780ad`
- **引用名**: `OsScheduleTableCounterRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `OsCounter`
- **完整路径**: `/AUTOSAR/EcucDefs/Os/OsCounter`
- **来源**: AUTOSAR_ECUC
- **描述**: This parameter contains a reference to the counter which drives the schedule table.

###### 配置容器

本模块包含 **6** 个配置容器：

####### 1. OsScheduleTableAutostart

**容器属性**:

- **UUID**: `ECUC:ddae46d1-ae87-4bf1-9142-d38f36e01718`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `OsScheduleTableAutostart`
- **多重性**: [0..1]

**容器描述**:

This container specifies if and how the schedule table is started on startup of the Operating System. The options to start a schedule table correspond to the API calls to start schedule tables during runtime.

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. OsScheduleTableStartValue

- **UUID**: `ECUC:3253c9f1-8291-4424-9258-bd5e22b64bf8`
- **参数名**: `OsScheduleTableStartValue`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Absolute autostart tick value when the schedule table starts. Only used if the OsScheduleTableAutostartType is ABSOLUTE.

######### ENUMERATION 类型参数

########## 1. OsScheduleTableAutostartType

- **UUID**: `ECUC:b3a89925-bcbd-4c14-b18d-ce7ab18eab54`
- **参数名**: `OsScheduleTableAutostartType`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `ABSOLUTE` (来源: AUTOSAR_ECUC)
  - `RELATIVE` (来源: AUTOSAR_ECUC)
  - `SYNCHRON` (来源: AUTOSAR_ECUC)
- **描述**: This specifies the type of the autostart for the schedule table.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. OsScheduleTableAppModeRef

- **UUID**: `ECUC:a1e5af6a-7900-4b84-a608-d0199790ed2d`
- **引用名**: `OsScheduleTableAppModeRef`
- **引用类型**: REFERENCE
- **多重性**: [1..infinite]
- **目标**: `OsAppMode`
- **完整路径**: `/AUTOSAR/EcucDefs/Os/OsAppMode`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference in which application modes the schedule table should be started during startup

####### 2. OsScheduleTableExpiryPoint

**容器属性**:

- **UUID**: `ECUC:c7cd0a08-1a1b-4d8f-aba8-a93a48a1a2a8`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `OsScheduleTableExpiryPoint`
- **多重性**: [1..infinite]

**容器描述**:

The point on a Schedule Table at which the OS activates tasks and/or sets events

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. OsScheduleTblExpPointOffset

- **UUID**: `ECUC:ae9487c7-72d2-455b-84e3-0789069652ed`
- **参数名**: `OsScheduleTblExpPointOffset`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: The offset from zero (in ticks) at which the expiry point is to be processed.

######## 配置容器

本模块包含 **3** 个配置容器：

######### 1. OsScheduleTableEventSetting

**容器属性**:

- **UUID**: `ECUC:da6a454f-c51f-499f-bf85-327d654b710d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `OsScheduleTableEventSetting`
- **多重性**: [0..infinite]

**容器描述**:

Event that is triggered by that schedule table.

########## 引用关系

此容器包含 **2** 个引用：

########### REFERENCE 类型引用

############ 1. OsScheduleTableSetEventRef

- **UUID**: `ECUC:5b6d6723-ab99-4855-b3a1-7307dcfb568c`
- **引用名**: `OsScheduleTableSetEventRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `OsEvent`
- **完整路径**: `/AUTOSAR/EcucDefs/Os/OsEvent`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to event that will be set by action

############ 2. OsScheduleTableSetEventTaskRef

- **UUID**: `ECUC:9c00d427-05c7-4bf2-960f-818e9c527827`
- **引用名**: `OsScheduleTableSetEventTaskRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `OsTask`
- **完整路径**: `/AUTOSAR/EcucDefs/Os/OsTask`
- **来源**: AUTOSAR_ECUC

######### 2. OsScheduleTableTaskActivation

**容器属性**:

- **UUID**: `ECUC:f65324cd-90ca-4bd5-9ba2-7abc0b9a6489`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `OsScheduleTableTaskActivation`
- **多重性**: [0..infinite]

**容器描述**:

Task that is triggered by that schedule table.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. OsScheduleTableActivateTaskRef

- **UUID**: `ECUC:a39530bb-23f0-4ff3-96c7-07c979bcfa55`
- **引用名**: `OsScheduleTableActivateTaskRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `OsTask`
- **完整路径**: `/AUTOSAR/EcucDefs/Os/OsTask`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to task that will be activated by action

######### 3. OsScheduleTblAdjustableExpPoint

**容器属性**:

- **UUID**: `ECUC:4517e21c-7943-450e-8038-ac3dc14794f6`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `OsScheduleTblAdjustableExpPoint`
- **多重性**: [0..1]

**容器描述**:

Adjustable expiry point

########## 参数配置

此容器包含 **2** 个参数：

########### INTEGER 类型参数

############ 1. OsScheduleTableMaxLengthen

- **UUID**: `ECUC:6dfec9f1-1edd-4155-9aee-bcc5a7eff09d`
- **参数名**: `OsScheduleTableMaxLengthen`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: The maximum positive adjustment that can be made to the expiry point offset (in ticks).

############ 2. OsScheduleTableMaxShorten

- **UUID**: `ECUC:24814103-54dd-4a15-86ac-e315b1791fd0`
- **参数名**: `OsScheduleTableMaxShorten`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: The maximum negative adjustment that can be made to the expiry point offset (in ticks).

####### 3. OsScheduleTableEventSetting

**容器属性**:

- **UUID**: `ECUC:da6a454f-c51f-499f-bf85-327d654b710d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `OsScheduleTableEventSetting`
- **多重性**: [0..infinite]

**容器描述**:

Event that is triggered by that schedule table.

######## 引用关系

此容器包含 **2** 个引用：

######### REFERENCE 类型引用

########## 1. OsScheduleTableSetEventRef

- **UUID**: `ECUC:5b6d6723-ab99-4855-b3a1-7307dcfb568c`
- **引用名**: `OsScheduleTableSetEventRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `OsEvent`
- **完整路径**: `/AUTOSAR/EcucDefs/Os/OsEvent`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to event that will be set by action

########## 2. OsScheduleTableSetEventTaskRef

- **UUID**: `ECUC:9c00d427-05c7-4bf2-960f-818e9c527827`
- **引用名**: `OsScheduleTableSetEventTaskRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `OsTask`
- **完整路径**: `/AUTOSAR/EcucDefs/Os/OsTask`
- **来源**: AUTOSAR_ECUC

####### 4. OsScheduleTableTaskActivation

**容器属性**:

- **UUID**: `ECUC:f65324cd-90ca-4bd5-9ba2-7abc0b9a6489`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `OsScheduleTableTaskActivation`
- **多重性**: [0..infinite]

**容器描述**:

Task that is triggered by that schedule table.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. OsScheduleTableActivateTaskRef

- **UUID**: `ECUC:a39530bb-23f0-4ff3-96c7-07c979bcfa55`
- **引用名**: `OsScheduleTableActivateTaskRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `OsTask`
- **完整路径**: `/AUTOSAR/EcucDefs/Os/OsTask`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to task that will be activated by action

####### 5. OsScheduleTblAdjustableExpPoint

**容器属性**:

- **UUID**: `ECUC:4517e21c-7943-450e-8038-ac3dc14794f6`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `OsScheduleTblAdjustableExpPoint`
- **多重性**: [0..1]

**容器描述**:

Adjustable expiry point

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. OsScheduleTableMaxLengthen

- **UUID**: `ECUC:6dfec9f1-1edd-4155-9aee-bcc5a7eff09d`
- **参数名**: `OsScheduleTableMaxLengthen`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: The maximum positive adjustment that can be made to the expiry point offset (in ticks).

########## 2. OsScheduleTableMaxShorten

- **UUID**: `ECUC:24814103-54dd-4a15-86ac-e315b1791fd0`
- **参数名**: `OsScheduleTableMaxShorten`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: The maximum negative adjustment that can be made to the expiry point offset (in ticks).

####### 6. OsScheduleTableSync

**容器属性**:

- **UUID**: `ECUC:6242bbd5-43d6-45a6-9128-fad562be2af9`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `OsScheduleTableSync`
- **多重性**: [0..1]

**容器描述**:

This container specifies the synchronization parameters of the schedule table.

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. OsScheduleTblExplicitPrecision

- **UUID**: `ECUC:123e7dad-40fd-4311-9cd7-bb56c0a5c4de`
- **参数名**: `OsScheduleTblExplicitPrecision`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: This configuration is only valid if the explicit synchronization is used.

######### ENUMERATION 类型参数

########## 1. OsScheduleTblSyncStrategy

- **UUID**: `ECUC:b2420449-8111-4d58-8338-b9068501a1a6`
- **参数名**: `OsScheduleTblSyncStrategy`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `NONE`
- **来源**: AUTOSAR ECUC
- **符号名值**: false
- **可选值**:
  - `EXPLICIT` (来源: AUTOSAR_ECUC)
  - `IMPLICIT` (来源: AUTOSAR_ECUC)
  - `NONE` (来源: AUTOSAR_ECUC)
- **描述**: AUTOSAR OS provides support for synchronization in two ways: explicit and implicit.

##### 27. OsScheduleTableAutostart

**容器属性**:

- **UUID**: `ECUC:ddae46d1-ae87-4bf1-9142-d38f36e01718`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `OsScheduleTableAutostart`
- **多重性**: [0..1]

**容器描述**:

This container specifies if and how the schedule table is started on startup of the Operating System. The options to start a schedule table correspond to the API calls to start schedule tables during runtime.

###### 参数配置

此容器包含 **2** 个参数：

####### INTEGER 类型参数

######## 1. OsScheduleTableStartValue

- **UUID**: `ECUC:3253c9f1-8291-4424-9258-bd5e22b64bf8`
- **参数名**: `OsScheduleTableStartValue`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Absolute autostart tick value when the schedule table starts. Only used if the OsScheduleTableAutostartType is ABSOLUTE.

####### ENUMERATION 类型参数

######## 1. OsScheduleTableAutostartType

- **UUID**: `ECUC:b3a89925-bcbd-4c14-b18d-ce7ab18eab54`
- **参数名**: `OsScheduleTableAutostartType`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `ABSOLUTE` (来源: AUTOSAR_ECUC)
  - `RELATIVE` (来源: AUTOSAR_ECUC)
  - `SYNCHRON` (来源: AUTOSAR_ECUC)
- **描述**: This specifies the type of the autostart for the schedule table.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. OsScheduleTableAppModeRef

- **UUID**: `ECUC:a1e5af6a-7900-4b84-a608-d0199790ed2d`
- **引用名**: `OsScheduleTableAppModeRef`
- **引用类型**: REFERENCE
- **多重性**: [1..infinite]
- **目标**: `OsAppMode`
- **完整路径**: `/AUTOSAR/EcucDefs/Os/OsAppMode`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference in which application modes the schedule table should be started during startup

##### 28. OsScheduleTableExpiryPoint

**容器属性**:

- **UUID**: `ECUC:c7cd0a08-1a1b-4d8f-aba8-a93a48a1a2a8`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `OsScheduleTableExpiryPoint`
- **多重性**: [1..infinite]

**容器描述**:

The point on a Schedule Table at which the OS activates tasks and/or sets events

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. OsScheduleTblExpPointOffset

- **UUID**: `ECUC:ae9487c7-72d2-455b-84e3-0789069652ed`
- **参数名**: `OsScheduleTblExpPointOffset`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: The offset from zero (in ticks) at which the expiry point is to be processed.

###### 配置容器

本模块包含 **3** 个配置容器：

####### 1. OsScheduleTableEventSetting

**容器属性**:

- **UUID**: `ECUC:da6a454f-c51f-499f-bf85-327d654b710d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `OsScheduleTableEventSetting`
- **多重性**: [0..infinite]

**容器描述**:

Event that is triggered by that schedule table.

######## 引用关系

此容器包含 **2** 个引用：

######### REFERENCE 类型引用

########## 1. OsScheduleTableSetEventRef

- **UUID**: `ECUC:5b6d6723-ab99-4855-b3a1-7307dcfb568c`
- **引用名**: `OsScheduleTableSetEventRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `OsEvent`
- **完整路径**: `/AUTOSAR/EcucDefs/Os/OsEvent`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to event that will be set by action

########## 2. OsScheduleTableSetEventTaskRef

- **UUID**: `ECUC:9c00d427-05c7-4bf2-960f-818e9c527827`
- **引用名**: `OsScheduleTableSetEventTaskRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `OsTask`
- **完整路径**: `/AUTOSAR/EcucDefs/Os/OsTask`
- **来源**: AUTOSAR_ECUC

####### 2. OsScheduleTableTaskActivation

**容器属性**:

- **UUID**: `ECUC:f65324cd-90ca-4bd5-9ba2-7abc0b9a6489`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `OsScheduleTableTaskActivation`
- **多重性**: [0..infinite]

**容器描述**:

Task that is triggered by that schedule table.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. OsScheduleTableActivateTaskRef

- **UUID**: `ECUC:a39530bb-23f0-4ff3-96c7-07c979bcfa55`
- **引用名**: `OsScheduleTableActivateTaskRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `OsTask`
- **完整路径**: `/AUTOSAR/EcucDefs/Os/OsTask`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to task that will be activated by action

####### 3. OsScheduleTblAdjustableExpPoint

**容器属性**:

- **UUID**: `ECUC:4517e21c-7943-450e-8038-ac3dc14794f6`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `OsScheduleTblAdjustableExpPoint`
- **多重性**: [0..1]

**容器描述**:

Adjustable expiry point

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. OsScheduleTableMaxLengthen

- **UUID**: `ECUC:6dfec9f1-1edd-4155-9aee-bcc5a7eff09d`
- **参数名**: `OsScheduleTableMaxLengthen`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: The maximum positive adjustment that can be made to the expiry point offset (in ticks).

########## 2. OsScheduleTableMaxShorten

- **UUID**: `ECUC:24814103-54dd-4a15-86ac-e315b1791fd0`
- **参数名**: `OsScheduleTableMaxShorten`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: The maximum negative adjustment that can be made to the expiry point offset (in ticks).

##### 29. OsScheduleTableEventSetting

**容器属性**:

- **UUID**: `ECUC:da6a454f-c51f-499f-bf85-327d654b710d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `OsScheduleTableEventSetting`
- **多重性**: [0..infinite]

**容器描述**:

Event that is triggered by that schedule table.

###### 引用关系

此容器包含 **2** 个引用：

####### REFERENCE 类型引用

######## 1. OsScheduleTableSetEventRef

- **UUID**: `ECUC:5b6d6723-ab99-4855-b3a1-7307dcfb568c`
- **引用名**: `OsScheduleTableSetEventRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `OsEvent`
- **完整路径**: `/AUTOSAR/EcucDefs/Os/OsEvent`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to event that will be set by action

######## 2. OsScheduleTableSetEventTaskRef

- **UUID**: `ECUC:9c00d427-05c7-4bf2-960f-818e9c527827`
- **引用名**: `OsScheduleTableSetEventTaskRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `OsTask`
- **完整路径**: `/AUTOSAR/EcucDefs/Os/OsTask`
- **来源**: AUTOSAR_ECUC

##### 30. OsScheduleTableTaskActivation

**容器属性**:

- **UUID**: `ECUC:f65324cd-90ca-4bd5-9ba2-7abc0b9a6489`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `OsScheduleTableTaskActivation`
- **多重性**: [0..infinite]

**容器描述**:

Task that is triggered by that schedule table.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. OsScheduleTableActivateTaskRef

- **UUID**: `ECUC:a39530bb-23f0-4ff3-96c7-07c979bcfa55`
- **引用名**: `OsScheduleTableActivateTaskRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `OsTask`
- **完整路径**: `/AUTOSAR/EcucDefs/Os/OsTask`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to task that will be activated by action

##### 31. OsScheduleTblAdjustableExpPoint

**容器属性**:

- **UUID**: `ECUC:4517e21c-7943-450e-8038-ac3dc14794f6`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `OsScheduleTblAdjustableExpPoint`
- **多重性**: [0..1]

**容器描述**:

Adjustable expiry point

###### 参数配置

此容器包含 **2** 个参数：

####### INTEGER 类型参数

######## 1. OsScheduleTableMaxLengthen

- **UUID**: `ECUC:6dfec9f1-1edd-4155-9aee-bcc5a7eff09d`
- **参数名**: `OsScheduleTableMaxLengthen`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: The maximum positive adjustment that can be made to the expiry point offset (in ticks).

######## 2. OsScheduleTableMaxShorten

- **UUID**: `ECUC:24814103-54dd-4a15-86ac-e315b1791fd0`
- **参数名**: `OsScheduleTableMaxShorten`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: The maximum negative adjustment that can be made to the expiry point offset (in ticks).

##### 32. OsScheduleTableSync

**容器属性**:

- **UUID**: `ECUC:6242bbd5-43d6-45a6-9128-fad562be2af9`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `OsScheduleTableSync`
- **多重性**: [0..1]

**容器描述**:

This container specifies the synchronization parameters of the schedule table.

###### 参数配置

此容器包含 **2** 个参数：

####### INTEGER 类型参数

######## 1. OsScheduleTblExplicitPrecision

- **UUID**: `ECUC:123e7dad-40fd-4311-9cd7-bb56c0a5c4de`
- **参数名**: `OsScheduleTblExplicitPrecision`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: This configuration is only valid if the explicit synchronization is used.

####### ENUMERATION 类型参数

######## 1. OsScheduleTblSyncStrategy

- **UUID**: `ECUC:b2420449-8111-4d58-8338-b9068501a1a6`
- **参数名**: `OsScheduleTblSyncStrategy`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `NONE`
- **来源**: AUTOSAR ECUC
- **符号名值**: false
- **可选值**:
  - `EXPLICIT` (来源: AUTOSAR_ECUC)
  - `IMPLICIT` (来源: AUTOSAR_ECUC)
  - `NONE` (来源: AUTOSAR_ECUC)
- **描述**: AUTOSAR OS provides support for synchronization in two ways: explicit and implicit.

##### 33. OsSpinlock

**容器属性**:

- **UUID**: `ECUC:d693c889-237d-481d-836b-62c73ad00d48`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `OsSpinlock`
- **多重性**: [0..infinite]

**容器描述**:

An OsSpinlock object is used to co-ordinate concurrent access by TASKs/ISR2s on different cores to a shared resource.

###### 参数配置

此容器包含 **1** 个参数：

####### ENUMERATION 类型参数

######## 1. OsSpinlockLockMethod

- **UUID**: `ECUC:a6a46311-b3c8-4178-acab-c75fa0d24275`
- **参数名**: `OsSpinlockLockMethod`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `LOCK_NOTHING`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `LOCK_ALL_INTERRUPTS` (来源: AUTOSAR_ECUC)
  - `LOCK_CAT2_INTERRUPTS` (来源: AUTOSAR_ECUC)
  - `LOCK_NOTHING` (来源: AUTOSAR_ECUC)
  - `LOCK_WITH_RES_SCHEDULER` (来源: AUTOSAR_ECUC)
- **描述**: Lock method which is used when a spinlock is taken. Note that it is possible that a user (e.g. a Task) might hold more than one spinlock. In this case the last lock taken is forced to use at least a lock methode which locks as strong as the current one.

###### 引用关系

此容器包含 **2** 个引用：

####### REFERENCE 类型引用

######## 1. OsSpinlockAccessingApplication

- **UUID**: `ECUC:804a40be-efb2-4923-b684-7466bf088f7e`
- **引用名**: `OsSpinlockAccessingApplication`
- **引用类型**: REFERENCE
- **多重性**: [1..infinite]
- **目标**: `OsApplication`
- **完整路径**: `/AUTOSAR/EcucDefs/Os/OsApplication`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to OsApplications that have an access to this object.

######## 2. OsSpinlockSuccessor

- **UUID**: `ECUC:de2b3a13-fb51-4c88-980d-89bd9a102d2a`
- **引用名**: `OsSpinlockSuccessor`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `OsSpinlock`
- **完整路径**: `/AUTOSAR/EcucDefs/Os/OsSpinlock`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to OsApplications that have an access to this object.

##### 34. OsTask

**容器属性**:

- **UUID**: `ECUC:f9cd89d3-97e4-4f05-ad16-d8f577b726d0`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `OsTask`
- **多重性**: [0..infinite]

**容器描述**:

This container represents an OSEK task.

###### 参数配置

此容器包含 **3** 个参数：

####### INTEGER 类型参数

######## 1. OsTaskActivation

- **UUID**: `ECUC:f53345d4-aac0-420f-ba25-d5b65b0dc33d`
- **参数名**: `OsTaskActivation`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: This attribute defines the maximum number of queued activation requests for the task. A value equal to "1" means that at any time only a single activation is permitted for this task. Note that the value must be a natural number starting at 1.

######## 2. OsTaskPriority

- **UUID**: `ECUC:61428e85-21e3-4df8-980f-9a985a02ede4`
- **参数名**: `OsTaskPriority`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: The priority of a task is defined by the value of this attribute. This value has to be understood as a relative value, i.e. the values show only the relative ordering of the tasks.

####### ENUMERATION 类型参数

######## 1. OsTaskSchedule

- **UUID**: `ECUC:f9b59379-7036-4b07-ab5c-2adfabf501c9`
- **参数名**: `OsTaskSchedule`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `FULL` (来源: AUTOSAR_ECUC)
  - `NON` (来源: AUTOSAR_ECUC)
- **描述**: The OsTaskSchedule attribute defines the preemptability of the task.

###### 引用关系

此容器包含 **3** 个引用：

####### REFERENCE 类型引用

######## 1. OsTaskAccessingApplication

- **UUID**: `ECUC:171cf36f-49fc-411f-a6a6-1d7b2ad3980c`
- **引用名**: `OsTaskAccessingApplication`
- **引用类型**: REFERENCE
- **多重性**: [0..infinite]
- **目标**: `OsApplication`
- **完整路径**: `/AUTOSAR/EcucDefs/Os/OsApplication`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to applications which have an access to this object.

######## 2. OsTaskEventRef

- **UUID**: `ECUC:7044fce9-f730-49ac-a996-dc177040d49e`
- **引用名**: `OsTaskEventRef`
- **引用类型**: REFERENCE
- **多重性**: [0..infinite]
- **目标**: `OsEvent`
- **完整路径**: `/AUTOSAR/EcucDefs/Os/OsEvent`
- **来源**: AUTOSAR_ECUC
- **描述**: This reference defines the list of events the extended task may react on.

######## 3. OsTaskResourceRef

- **UUID**: `ECUC:62e61405-1641-428b-8bb0-16f229d5e20e`
- **引用名**: `OsTaskResourceRef`
- **引用类型**: REFERENCE
- **多重性**: [0..infinite]
- **目标**: `OsResource`
- **完整路径**: `/AUTOSAR/EcucDefs/Os/OsResource`
- **来源**: AUTOSAR_ECUC
- **描述**: This reference defines a list of resources accessed by this task.

###### 配置容器

本模块包含 **3** 个配置容器：

####### 1. OsTaskAutostart

**容器属性**:

- **UUID**: `ECUC:e9cb3483-f89a-4318-bbc9-ad010cc385b3`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `OsTaskAutostart`
- **多重性**: [0..1]

**容器描述**:

This container determines whether the task is activated during the system start-up procedure or not for some specific application modes.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. OsTaskAppModeRef

- **UUID**: `ECUC:e7ace4a7-9613-4f24-908c-30ccc5bf56e6`
- **引用名**: `OsTaskAppModeRef`
- **引用类型**: REFERENCE
- **多重性**: [1..infinite]
- **目标**: `OsAppMode`
- **完整路径**: `/AUTOSAR/EcucDefs/Os/OsAppMode`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to application modes in which that task is activated on startup of the OS

####### 2. OsTaskTimingProtection

**容器属性**:

- **UUID**: `ECUC:84e81766-4a5b-4236-9108-ef70def0f89f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `OsTaskTimingProtection`
- **多重性**: [0..1]

**容器描述**:

This container contains all parameters regarding timing protection of the task.

######## 参数配置

此容器包含 **4** 个参数：

######### FLOAT 类型参数

########## 1. OsTaskAllInterruptLockBudget

- **UUID**: `ECUC:8081828e-63a1-4557-aa36-499a08c8c7f5`
- **参数名**: `OsTaskAllInterruptLockBudget`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **取值范围**: [0..Inf]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: This parameter contains the maximum time for which the task is allowed to lock all interrupts (via SuspendAllInterrupts() or DisableAllInterrupts()) (in seconds).

########## 2. OsTaskExecutionBudget

- **UUID**: `ECUC:dfe8bdba-81ab-4678-9590-d572e5f51e63`
- **参数名**: `OsTaskExecutionBudget`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **取值范围**: [0..Inf]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: This parameter contains the maximum allowed execution time of the task (in seconds).

########## 3. OsTaskOsInterruptLockBudget

- **UUID**: `ECUC:76ffc748-10a8-4e58-8a72-eabb96ee8ec2`
- **参数名**: `OsTaskOsInterruptLockBudget`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **取值范围**: [0..Inf]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: This parameter contains the maximum time for which the task is allowed to lock all Category 2 interrupts (via SuspendOSInterrupts()) (in seconds).

########## 4. OsTaskTimeFrame

- **UUID**: `ECUC:faa19133-57b3-47fe-9ad3-3e028e0c5884`
- **参数名**: `OsTaskTimeFrame`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **取值范围**: [0..Inf]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: The minimum inter-arrival time between activations and/or releases of a task (in seconds).

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. OsTaskResourceLock

**容器属性**:

- **UUID**: `ECUC:4c924269-ca89-4c10-9481-cdccacc1a866`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `OsTaskResourceLock`
- **多重性**: [0..infinite]

**容器描述**:

This container contains the worst case time between getting and releasing a given resource (in seconds).

########## 参数配置

此容器包含 **1** 个参数：

########### FLOAT 类型参数

############ 1. OsTaskResourceLockBudget

- **UUID**: `ECUC:d22b3f26-8cf9-4334-a8e8-cd3657d64f9d`
- **参数名**: `OsTaskResourceLockBudget`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0..Inf]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: This parameter contains the maximum time the task is allowed to lock the resource (in seconds)

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. OsTaskResourceLockResourceRef

- **UUID**: `ECUC:ac350ae8-5ba7-4294-930a-d2e9c7cd6bc8`
- **引用名**: `OsTaskResourceLockResourceRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `OsResource`
- **完整路径**: `/AUTOSAR/EcucDefs/Os/OsResource`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the resource used by the task

####### 3. OsTaskResourceLock

**容器属性**:

- **UUID**: `ECUC:4c924269-ca89-4c10-9481-cdccacc1a866`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `OsTaskResourceLock`
- **多重性**: [0..infinite]

**容器描述**:

This container contains the worst case time between getting and releasing a given resource (in seconds).

######## 参数配置

此容器包含 **1** 个参数：

######### FLOAT 类型参数

########## 1. OsTaskResourceLockBudget

- **UUID**: `ECUC:d22b3f26-8cf9-4334-a8e8-cd3657d64f9d`
- **参数名**: `OsTaskResourceLockBudget`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0..Inf]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: This parameter contains the maximum time the task is allowed to lock the resource (in seconds)

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. OsTaskResourceLockResourceRef

- **UUID**: `ECUC:ac350ae8-5ba7-4294-930a-d2e9c7cd6bc8`
- **引用名**: `OsTaskResourceLockResourceRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `OsResource`
- **完整路径**: `/AUTOSAR/EcucDefs/Os/OsResource`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the resource used by the task

##### 35. OsTaskAutostart

**容器属性**:

- **UUID**: `ECUC:e9cb3483-f89a-4318-bbc9-ad010cc385b3`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `OsTaskAutostart`
- **多重性**: [0..1]

**容器描述**:

This container determines whether the task is activated during the system start-up procedure or not for some specific application modes.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. OsTaskAppModeRef

- **UUID**: `ECUC:e7ace4a7-9613-4f24-908c-30ccc5bf56e6`
- **引用名**: `OsTaskAppModeRef`
- **引用类型**: REFERENCE
- **多重性**: [1..infinite]
- **目标**: `OsAppMode`
- **完整路径**: `/AUTOSAR/EcucDefs/Os/OsAppMode`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to application modes in which that task is activated on startup of the OS

##### 36. OsTaskTimingProtection

**容器属性**:

- **UUID**: `ECUC:84e81766-4a5b-4236-9108-ef70def0f89f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `OsTaskTimingProtection`
- **多重性**: [0..1]

**容器描述**:

This container contains all parameters regarding timing protection of the task.

###### 参数配置

此容器包含 **4** 个参数：

####### FLOAT 类型参数

######## 1. OsTaskAllInterruptLockBudget

- **UUID**: `ECUC:8081828e-63a1-4557-aa36-499a08c8c7f5`
- **参数名**: `OsTaskAllInterruptLockBudget`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **取值范围**: [0..Inf]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: This parameter contains the maximum time for which the task is allowed to lock all interrupts (via SuspendAllInterrupts() or DisableAllInterrupts()) (in seconds).

######## 2. OsTaskExecutionBudget

- **UUID**: `ECUC:dfe8bdba-81ab-4678-9590-d572e5f51e63`
- **参数名**: `OsTaskExecutionBudget`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **取值范围**: [0..Inf]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: This parameter contains the maximum allowed execution time of the task (in seconds).

######## 3. OsTaskOsInterruptLockBudget

- **UUID**: `ECUC:76ffc748-10a8-4e58-8a72-eabb96ee8ec2`
- **参数名**: `OsTaskOsInterruptLockBudget`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **取值范围**: [0..Inf]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: This parameter contains the maximum time for which the task is allowed to lock all Category 2 interrupts (via SuspendOSInterrupts()) (in seconds).

######## 4. OsTaskTimeFrame

- **UUID**: `ECUC:faa19133-57b3-47fe-9ad3-3e028e0c5884`
- **参数名**: `OsTaskTimeFrame`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **取值范围**: [0..Inf]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: The minimum inter-arrival time between activations and/or releases of a task (in seconds).

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. OsTaskResourceLock

**容器属性**:

- **UUID**: `ECUC:4c924269-ca89-4c10-9481-cdccacc1a866`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `OsTaskResourceLock`
- **多重性**: [0..infinite]

**容器描述**:

This container contains the worst case time between getting and releasing a given resource (in seconds).

######## 参数配置

此容器包含 **1** 个参数：

######### FLOAT 类型参数

########## 1. OsTaskResourceLockBudget

- **UUID**: `ECUC:d22b3f26-8cf9-4334-a8e8-cd3657d64f9d`
- **参数名**: `OsTaskResourceLockBudget`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0..Inf]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: This parameter contains the maximum time the task is allowed to lock the resource (in seconds)

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. OsTaskResourceLockResourceRef

- **UUID**: `ECUC:ac350ae8-5ba7-4294-930a-d2e9c7cd6bc8`
- **引用名**: `OsTaskResourceLockResourceRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `OsResource`
- **完整路径**: `/AUTOSAR/EcucDefs/Os/OsResource`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the resource used by the task

##### 37. OsTaskResourceLock

**容器属性**:

- **UUID**: `ECUC:4c924269-ca89-4c10-9481-cdccacc1a866`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `OsTaskResourceLock`
- **多重性**: [0..infinite]

**容器描述**:

This container contains the worst case time between getting and releasing a given resource (in seconds).

###### 参数配置

此容器包含 **1** 个参数：

####### FLOAT 类型参数

######## 1. OsTaskResourceLockBudget

- **UUID**: `ECUC:d22b3f26-8cf9-4334-a8e8-cd3657d64f9d`
- **参数名**: `OsTaskResourceLockBudget`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0..Inf]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: This parameter contains the maximum time the task is allowed to lock the resource (in seconds)

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. OsTaskResourceLockResourceRef

- **UUID**: `ECUC:ac350ae8-5ba7-4294-930a-d2e9c7cd6bc8`
- **引用名**: `OsTaskResourceLockResourceRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `OsResource`
- **完整路径**: `/AUTOSAR/EcucDefs/Os/OsResource`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the resource used by the task

##### 38. OsAlarmAction

**容器属性**:

- **UUID**: `ECUC:2acfb5a0-b476-4fa4-a34c-08e4acfe9858`
- **容器类型**: CHOICE-CONTAINER
- **容器名称**: `OsAlarmAction`
- **多重性**: [1..1]

**容器选择**:

- **OsAlarmActivateTask**
  - UUID: `ECUC:778af345-37da-4297-a5cf-617140faa94f`
  - 描述: This container specifies the parameters to activate a task.
- **OsAlarmCallback**
  - UUID: `ECUC:d5df234a-b9c3-40e5-b30e-6ee6919a6c8e`
  - 描述: This container specifies the parameters to call a callback OS alarm action.
- **OsAlarmIncrementCounter**
  - UUID: `ECUC:e7f3faba-d482-41dd-9a78-a1bf24e96207`
  - 描述: This container specifies the parameters to increment a counter.
- **OsAlarmSetEvent**
  - UUID: `ECUC:135c6787-8aad-4ca3-9c1b-f9db78eea4c0`
  - 描述: This container specifies the parameters to set an event

**容器描述**:

This container defines which type of notification is used when the alarm expires.

## 📦 包结构

此ARXML文件包含 **2** 个包：

### 1. AUTOSAR

- **UUID**: `ECUC:AUTOSAR`
- **包名称**: `AUTOSAR`
- **包含元素数量**: 0

### 2. EcucDefs

- **UUID**: `ECUC:ECUCDEFS`
- **包名称**: `EcucDefs`
- **包含元素数量**: 1

#### 包含的元素

##### ECUC-MODULE-DEF 类型元素

1. **Os**
