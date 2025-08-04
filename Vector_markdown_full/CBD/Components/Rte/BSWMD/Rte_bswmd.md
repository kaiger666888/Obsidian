# Rte - 完整配置文档

*此文档由ARXML文件自动生成，采用层次化结构展示*

**生成时间**: 2025-06-16 14:45:46

## 📑 目录

- [📄 文件信息](#-文件信息)
- [🔧 模块定义](#-模块定义)
  - [Rte](#rte)
  - [RteCalculation](#rtecalculation)
  - [RteChecks](#rtechecks)
- [📦 包结构](#-包结构)
- [⚡ 实现信息](#-实现信息)
- [⚙️ 配置信息](#️-配置信息)

## 📄 文件信息

### Schema信息
- **Schema位置**: `http://autosar.org/schema/r4.0 AUTOSAR_4-0-3.xsd`
- **命名空间**: `http://autosar.org/schema/r4.0`

## 🔧 模块定义

### 1. Rte

#### 基本信息

- **UUID**: `57d62d1a-764f-4cb9-b785-044e2148b649`
- **模块名称**: `Rte`
- **类别**: `VENDOR_SPECIFIC_MODULE_DEFINITION`
- **多重性**: [0..1]
- **支持的变体**:
  - VARIANT-PRE-COMPILE
  - VARIANT-POST-BUILD-SELECTABLE

#### 模块描述

Runtime Environment (RTE). Scalable and highly optimized. Manages communication between the software components (SWC), assures consistency of the overall information flow and represents the interface between the functional software, basic software (BSW) and complex drivers (CDD).  Includes the SchM (Schedule Manager) functionality.
#SWC #Scheduling #TaskMapping #RuntimeEnvironment
#AUTOSAR

#### 版本历史

共有 **44** 个版本记录：

##### 1. 版本 3.90.00

- **发布日期**: 2012-08-17
- **发布者**: AUTOSAR

**变更内容**:

##### 2. 版本 4.00.00

- **发布日期**: 2012-11-08T03:06:56+01:00
- **发布者**: vissi

**变更内容**:

##### 3. 版本 4.01.00

- **发布日期**: 2013-03-15T07:06:59+01:00
- **发布者**: vissi

**变更内容**:

##### 4. 版本 4.01.01

- **发布日期**: 2013-05-27T17:08:00+01:00
- **发布者**: vissi

**变更内容**:

##### 5. 版本 4.02.00

- **发布日期**: 2013-09-13T02:30:18+02:00
- **发布者**: visso, vissi

**变更内容**:

##### 6. 版本 4.02.01

- **发布日期**: 2013-11-22T02:30:18+02:00
- **发布者**: vissi

**变更内容**:

##### 7. 版本 4.03.00

- **发布日期**: 2013-12-18T02:30:18+02:00
- **发布者**: vissi, visso

**变更内容**:

##### 8. 版本 4.04.00

- **发布日期**: 2014-05-12T02:30:18+02:00
- **发布者**: vissi, visso

**变更内容**:

##### 9. 版本 4.05.00

- **发布日期**: 2014-07-11T12:39:26+02:00
- **发布者**: visso

**变更内容**:

##### 10. 版本 4.06.00

- **发布日期**: 2015-01-19T11:00:16+01:00
- **发布者**: vispah

**变更内容**:

##### 11. 版本 4.07.00

- **发布日期**: 2015-02-20T11:00:16+01:00
- **发布者**: vissi

**变更内容**:

##### 12. 版本 4.08.00

- **发布日期**: 2015-06-19T10:40:49+02:00
- **发布者**: visso, viscfr

**变更内容**:

##### 13. 版本 4.08.01

- **发布日期**: 2015-09-11T09:48:00+02:00
- **发布者**: vissi

**变更内容**:

##### 14. 版本 4.09.00

- **发布日期**: 2015-12-01T10:18:54+01:00
- **发布者**: vispah, visso

**变更内容**:

##### 15. 版本 4.10.00

- **发布日期**: 2016-02-19T09:10:00+01:00
- **发布者**: vispah, visso

**变更内容**:

##### 16. 版本 4.11.00

- **发布日期**: 2016-04-19T09:10:00+01:00
- **发布者**: viscfr

**变更内容**:

##### 17. 版本 4.12.00

- **发布日期**: 2016-06-15T01:47:20+02:00
- **发布者**: visso

**变更内容**:

##### 18. 版本 4.12.01

- **发布日期**: 2016-09-19T10:02:00+02:00
- **发布者**: vissi

**变更内容**:

##### 19. 版本 4.13.00

- **发布日期**: 2016-10-21T10:08:00+02:00
- **发布者**: vissi

**变更内容**:

##### 20. 版本 4.13.01

- **发布日期**: 2017-02-19T10:08:00+02:00
- **发布者**: vissi

**变更内容**:

##### 21. 版本 4.14.00

- **发布日期**: 2017-02-23T18:12:00+02:00
- **发布者**: vissi

**变更内容**:

##### 22. 版本 4.15.00

- **发布日期**: 2017-05-19T09:00:00+01:00
- **发布者**: vissi

**变更内容**:

##### 23. 版本 4.16.00

- **发布日期**: 2017-06-30T09:00:00+01:00
- **发布者**: vissi

**变更内容**:

##### 24. 版本 4.17.00

- **发布日期**: 2017-08-29T13:30:00+01:00
- **发布者**: vissi

**变更内容**:

##### 25. 版本 4.18.00

- **发布日期**: 2017-11-20T14:00:00+01:00
- **发布者**: vissi

**变更内容**:

##### 26. 版本 4.19.00

- **发布日期**: 2018-05-05T15:05:54+02:00
- **发布者**: visso

**变更内容**:

##### 27. 版本 4.20.00

- **发布日期**: 2018-09-24T14:24:21+02:00
- **发布者**: visso, visgme, visfus

**变更内容**:

##### 28. 版本 4.21.00

- **发布日期**: 2019-07-22T16:46:07+02:00
- **发布者**: visso, visflh, vislsa

**变更内容**:

##### 29. 版本 4.22.00

- **发布日期**: 2019-08-28T14:53:54+02:00
- **发布者**: visso,visgme

**变更内容**:

##### 30. 版本 4.23.00

- **发布日期**: 2020-04-06T18:59:13+02:00
- **发布者**: visso

**变更内容**:

##### 31. 版本 4.24.00

- **发布日期**: 2020-09-21T17:14:19+02:00
- **发布者**: visso

**变更内容**:

##### 32. 版本 4.25.00

- **发布日期**: 2021-03-23T12:36:55+01:00
- **发布者**: visgme, visso

**变更内容**:

##### 33. 版本 4.26.00

- **发布日期**: 2021-09-08T10:33:56+02:00
- **发布者**: visso

**变更内容**:

##### 34. 版本 4.27.00

- **发布日期**: 2021-10-06T13:14:18+02:00
- **发布者**: visso

**变更内容**:

##### 35. 版本 4.28.00

- **发布日期**: 2021-12-07T14:23:37+01:00
- **发布者**: visso, visdes

**变更内容**:

##### 36. 版本 4.29.00

- **发布日期**: 2022-04-21T11:14:02+02:00
- **发布者**: visso

**变更内容**:

##### 37. 版本 4.30.00

- **发布日期**: 2022-07-07T10:00:11+02:00
- **发布者**: visso

**变更内容**:

##### 38. 版本 4.31.00

- **发布日期**: 2022-09-01T14:04:14+02:00
- **发布者**: visso

**变更内容**:

##### 39. 版本 4.32.00

- **发布日期**: 2022-10-18T15:58:15+02:00
- **发布者**: visso

**变更内容**:

##### 40. 版本 4.33.00

- **发布日期**: 2023-04-05T10:18:57+02:00
- **发布者**: visso

**变更内容**:

##### 41. 版本 4.34.00

- **发布日期**: 2023-07-04T09:47:11+02:00
- **发布者**: visso, visgme, jkugler

**变更内容**:

##### 42. 版本 4.35.00

- **发布日期**: 2023-09-14T17:22:19+02:00
- **发布者**: visso

**变更内容**:

##### 43. 版本 4.36.00

- **发布日期**: 2023-11-09T09:56:02+01:00
- **发布者**: visso, visgme

**变更内容**:

##### 44. 版本 4.37.00

- **发布日期**: 2024-03-14T14:37:00+01:00
- **发布者**: visso

**变更内容**:

#### 配置容器

本模块包含 **29** 个配置容器：

##### 1. RteBswGeneral

**容器属性**:

- **UUID**: `c30eb8a3-314d-4af2-b302-5637be63d9ab`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `RteBswGeneral`
- **多重性**: [1..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

General configuration parameters of the Bsw Scheduler section.

###### 参数配置

此容器包含 **2** 个参数：

####### BOOLEAN 类型参数

######## 1. RteSchMVersionInfoApi

- **UUID**: `e58cac75-8d1c-418a-86f6-c6c4349f385b`
- **参数名**: `RteSchMVersionInfoApi`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Enables the generation of the SchM_GetVersionInfo() API.

######## 2. RteUseComShadowSignalApi

- **UUID**: `01dced08-b993-49eb-b4f2-001b1542f957`
- **参数名**: `RteUseComShadowSignalApi`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter defines whether the ComShadowSignalAPIs ((Com_UpdateShadowSignal, Com_InvalidateShadowSignal, Com_ReceiveShadowSignal) are used or not.

##### 2. RteBswModuleInstance

**容器属性**:

- **UUID**: `2d21880b-043f-447e-aebc-b6759ee659d2`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `RteBswModuleInstance`
- **多重性**: [0..infinite]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

Represents one instance of a Bsw-Module configured on one ECU.

###### 引用关系

此容器包含 **2** 个引用：

####### FOREIGN-REFERENCE 类型引用

######## 1. RteBswImplementationRef

- **UUID**: `a5b8c45b-c045-48cd-bb75-c76146e5f998`
- **引用名**: `RteBswImplementationRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [1..1]
- **目标类型**: BSW-IMPLEMENTATION
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Reference to the BswImplementation for which the Rte /SchM is configured.

######## 2. RteBswModuleConfigurationRef

- **UUID**: `d808712a-3ad1-418c-9054-75384ac232a0`
- **引用名**: `RteBswModuleConfigurationRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [0..1]
- **目标类型**: MODULE-CONFIGURATION
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Reference to the ECU Configuration Values provided for this BswImplementation.

###### 配置容器

本模块包含 **6** 个配置容器：

####### 1. RteBswEventToTaskMapping

**容器属性**:

- **UUID**: `689a9711-30f6-48ed-a58c-5466db6776c2`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `RteBswEventToTaskMapping`
- **多重性**: [0..infinite]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

Maps a BswSchedulableEntity onto one OsTask based on the activating BswEvent.

######## 参数配置

此容器包含 **5** 个参数：

######### INTEGER 类型参数

########## 1. RteBswPositionInTask

- **UUID**: `3d5f32d9-6ffb-4bdc-9856-150235477f2a`
- **参数名**: `RteBswPositionInTask`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Each BswSchedulableEntity activation mapped to an OsTask has a specific position within the task execution.

######### BOOLEAN 类型参数

########## 1. RteBswImmediateRestart

- **UUID**: `b66a74ec-a021-4512-b120-6140aa31183d`
- **参数名**: `RteBswImmediateRestart`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: When RteBswImmediateRestart is set to true the BswSchedulableEntitiy shall be immediately re-started after termination if it was activated by this BswEvent while it was already started.

######### FLOAT 类型参数

########## 1. RteBswActivationOffset

- **UUID**: `db7fcf51-5387-4e07-a336-488514939e07`
- **参数名**: `RteBswActivationOffset`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **取值范围**: [0..]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Activation offset.

######### ENUMERATION 类型参数

########## 1. RteOsSchedulePoint

- **UUID**: `fd3dfe5a-8085-4d8a-a2b8-3a36910b35a8`
- **参数名**: `RteOsSchedulePoint`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `NONE`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CONDITIONAL`
  - `NONE`
  - `UNCONDITIONAL`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Introduce a schedule point by explicitly calling Os Schedule service after the execution of the ExecutableEntity.  The Rte generator is allowed to optimize several consecutive calls to Os schedule into one single call if the ExecutableEntity executions in between have been skipped.

########## 2. RteCyclicTriggerImplementation

- **UUID**: `67886850-1d5e-468f-b7bf-d0088f970956`
- **参数名**: `RteCyclicTriggerImplementation`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `Auto`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `Auto`
  - `None`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: If set to 'Auto' the RTE generator automatically creates the necessary OS alarm to realize the cyclic trigger with the configured activation offset. 
If set to 'None' the trigger is not implemented by the RTE generator. It has to be implemented by the user either by configuring an appropriate OS alarm or an OS schedule table. 
The OS task and optional the OS event for that trigger can be found in the generated RTE report.

######## 引用关系

此容器包含 **7** 个引用：

######### REFERENCE 类型引用

########## 1. RteBswMappedToTaskRef

- **UUID**: `44950cd8-4276-4f0d-a213-21ac32ebbfb5`
- **引用名**: `RteBswMappedToTaskRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `OsTask`
- **完整路径**: `/AUTOSAR/EcucDefs/Os/OsTask`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Reference to the OsTask the BswSchedulableEntity activated by the RteBswEventRef is mapped to.

########## 2. RteBswUsedOsAlarmRef

- **UUID**: `b2dbf5ca-cb5a-4c3e-826c-b2ec08645d72`
- **引用名**: `RteBswUsedOsAlarmRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `OsAlarm`
- **完整路径**: `/AUTOSAR/EcucDefs/Os/OsAlarm`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: If an OsAlarm is used to activate the OsTask this BswEvent is mapped to it shall be referenced here.

########## 3. RteBswUsedOsEventRef

- **UUID**: `de8edd5a-3cef-4563-a6df-1f3c38977f48`
- **引用名**: `RteBswUsedOsEventRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `OsEvent`
- **完整路径**: `/AUTOSAR/EcucDefs/Os/OsEvent`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: If an OsEvent is used to activate the OsTask this BswEvent is mapped to it shall be referenced here.

########## 4. RteBswUsedOsSchTblExpiryPointRef

- **UUID**: `7f85178d-5486-492c-8aa9-ac25f56162c4`
- **引用名**: `RteBswUsedOsSchTblExpiryPointRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `OsScheduleTableExpiryPoint`
- **完整路径**: `/AUTOSAR/EcucDefs/Os/OsScheduleTable/OsScheduleTableExpiryPoint`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: If an OsScheduleTableExpiryPoint is used to activate the OsTask this BswEvent is mapped to it shall be referenced here.

######### FOREIGN-REFERENCE 类型引用

########## 1. RteBswEventRef

- **UUID**: `48605e56-452e-44a8-9389-e344a6f7a2af`
- **引用名**: `RteBswEventRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [1..1]
- **目标类型**: BSW-EVENT
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Reference to the BswEvent which is pointing to the BswSchedulableEntity being mapped. This allows a fine grained mapping of BswSchedulableEntites based on the activating BswEvent.

########## 2. RteRipsFillRoutineRef

- **UUID**: `5b84fc20-2523-4573-a942-ef2172f85e65`
- **引用名**: `RteRipsFillRoutineRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [0..infinite]
- **目标类型**: CONTAINER
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Reference to a Buffer-Fill Routine implemented by an RTE Implementation Plug-In.

########## 3. RteRipsFlushRoutineRef

- **UUID**: `af92b9d4-28d3-40a1-8e9c-c4a90e01eda7`
- **引用名**: `RteRipsFlushRoutineRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [0..infinite]
- **目标类型**: CONTAINER
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Reference to a Buffer-Flush Routine implemented by an RTE Implementation Plug-In.

####### 2. RteBswExclusiveAreaImpl

**容器属性**:

- **UUID**: `f6c711bd-74bd-470f-8f88-eb52ad6792d3`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `RteBswExclusiveAreaImpl`
- **多重性**: [0..infinite]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

Represents one ExclusiveArea of one BswImplementation. Used to specify the implementation means of this ExclusiveArea.

######## 参数配置

此容器包含 **3** 个参数：

######### BOOLEAN 类型参数

########## 1. RteExclusiveAreaOptimization

- **UUID**: `87bd96ee-3cf1-4ce1-aefa-1be14f9625fd`
- **参数名**: `RteExclusiveAreaOptimization`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter is not yet supported by the RTE generator. Changing the value has no impact on the generated code.

########## 2. RteExclusiveAreaGenerateFunction

- **UUID**: `bad08024-0f02-4dbf-8056-75b7ec5a04f2`
- **参数名**: `RteExclusiveAreaGenerateFunction`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: If set to false/undefined, the BSW Module ImplementationCodeType is used to determine the implementation if possible. If the BSW Module ImplementationCodeType is set to EcuCSourceCode, the following limitations apply: the RTE generator generates a function if the BSW Module is Postbuild loadable, or if the implementation mechanism is set to custom. Otherwise, a macro is generated.

This parameter forces the RTE generator to generate a function for the ExclusiveArea interface implementation (disabling the RTE generator macro optimization).

######### ENUMERATION 类型参数

########## 1. RteExclusiveAreaImplMechanism

- **UUID**: `6d94023f-3028-4e42-9f26-d210fd261dec`
- **参数名**: `RteExclusiveAreaImplMechanism`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `ALL_INTERRUPT_BLOCKING`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `ALL_INTERRUPT_BLOCKING` (来源: AUTOSAR_ECUC)
  - `COOPERATIVE_RUNNABLE_PLACEMENT` (来源: AUTOSAR_ECUC)
  - `OS_INTERRUPT_BLOCKING` (来源: AUTOSAR_ECUC)
  - `OS_RESOURCE` (来源: AUTOSAR_ECUC)
  - `OS_SPINLOCK` (来源: AUTOSAR_ECUC)
  - `NONE` (来源: Vector Informatik)
  - `CUSTOM` (来源: Vector Informatik)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: To be used implementation mechanism for the specified ExclusiveArea.

######## 引用关系

此容器包含 **3** 个引用：

######### REFERENCE 类型引用

########## 1. RteBswExclusiveAreaOsResourceRef

- **UUID**: `caf87c29-5c1a-4d4c-8659-94aa922a46ce`
- **引用名**: `RteBswExclusiveAreaOsResourceRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `OsResource`
- **完整路径**: `/AUTOSAR/EcucDefs/Os/OsResource`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Optional reference to an OsResource in case RteExclusiveAreaImplMechanism is configured to OS_RESOURCE for this ExclusiveArea.

########## 2. RteBswExclusiveAreaOsSpinlockRef

- **UUID**: `ECUC:17fad2ad-eeff-411a-9b4a-2f8bee7c44f1`
- **引用名**: `RteBswExclusiveAreaOsSpinlockRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `OsSpinlock`
- **完整路径**: `/AUTOSAR/EcucDefs/Os/OsSpinlock`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Optional reference to an OsSpinlock in case RteExclusiveAreaImplMechanism is configured to OS_SPINLOCK for this ExclusiveArea.

######### FOREIGN-REFERENCE 类型引用

########## 1. RteBswExclusiveAreaRef

- **UUID**: `b956f3e6-c473-40e4-b15b-26bbfad691e1`
- **引用名**: `RteBswExclusiveAreaRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [1..1]
- **目标类型**: EXCLUSIVE-AREA
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Reference to the ExclusiveArea for which the implementation mechanism shall be specified.

####### 3. RteBswExternalTriggerConfig

**容器属性**:

- **UUID**: `9ea3544c-820e-41d6-b6cf-6392113d4286`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `RteBswExternalTriggerConfig`
- **多重性**: [0..infinite]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

Defines the configuration of Inter Basic Software Module Entity Triggering

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. RteBswTriggerSourceQueueLength

- **UUID**: `aa14658e-c12d-4f5d-899c-77390ba58c29`
- **参数名**: `RteBswTriggerSourceQueueLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Length of trigger queue on the trigger source side.

######## 引用关系

此容器包含 **1** 个引用：

######### FOREIGN-REFERENCE 类型引用

########## 1. RteBswTriggerSourceRef

- **UUID**: `9e0dee0c-5f3d-421f-b4b4-db04be364889`
- **引用名**: `RteBswTriggerSourceRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [1..1]
- **目标类型**: TRIGGER
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Reference to a Trigger instance in the role releasedTrigger of the related BSW Module instance.

####### 4. RteBswInternalTriggerConfig

**容器属性**:

- **UUID**: `7c9d27f9-aca0-4d67-a895-06b7e891325f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `RteBswInternalTriggerConfig`
- **多重性**: [0..infinite]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

Defines the configuration of internal Basic Software Module Entity Triggering

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. RteBswTriggerSourceQueueLength

- **UUID**: `ad0e35c0-29db-4e3e-9d07-7de6cd34f9a8`
- **参数名**: `RteBswTriggerSourceQueueLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Length of trigger queue on the trigger source side.

######## 引用关系

此容器包含 **1** 个引用：

######### FOREIGN-REFERENCE 类型引用

########## 1. RteBswTriggerSourceRef

- **UUID**: `ebf60df3-84b7-4307-93f7-cb34c269036d`
- **引用名**: `RteBswTriggerSourceRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [1..1]
- **目标类型**: BSW-INTERNAL-TRIGGERING-POINT
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Reference to a BswInternalTriggeringPoint of the related BSW Module instance.

####### 5. RteBswRequiredModeGroupConnection

**容器属性**:

- **UUID**: `64b34f5b-9f2f-4ee9-a5d7-211213055751`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `RteBswRequiredModeGroupConnection`
- **多重性**: [0..infinite]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

Defines the connection between one requiredModeGroup of this BSW Module instance and one providedModeGroup instance.

######## 引用关系

此容器包含 **3** 个引用：

######### REFERENCE 类型引用

########## 1. RteBswProvidedModeGrpModInstRef

- **UUID**: `8b3f7b0b-e8b6-451f-a924-02a50a600087`
- **引用名**: `RteBswProvidedModeGrpModInstRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `RteBswModuleInstance`
- **完整路径**: `/AUTOSAR/EcucDefs/Rte/RteBswModuleInstance`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Reference to the RteBswModuleInstance configuration container which identifies the instance of the BSW Module.

######### FOREIGN-REFERENCE 类型引用

########## 1. RteBswProvidedModeGroupRef

- **UUID**: `ac6ba743-c98a-4435-b80b-c5c687f2ad9f`
- **引用名**: `RteBswProvidedModeGroupRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [1..1]
- **目标类型**: MODE-DECLARATION-GROUP-PROTOTYPE
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: References the providedModeGroupPrototype to which this requiredModeGroup shall be connected.

########## 2. RteBswRequiredModeGroupRef

- **UUID**: `7dbdd9bc-5b6a-4ce8-a217-9bbf7369827d`
- **引用名**: `RteBswRequiredModeGroupRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [1..1]
- **目标类型**: MODE-DECLARATION-GROUP-PROTOTYPE
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: References requiredModeGroupPrototype which shall be connected to the providedModeGroupPrototype.

####### 6. RteBswRequiredTriggerConnection

**容器属性**:

- **UUID**: `817bdb91-58c6-480c-ba31-34b6f8c6f53f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `RteBswRequiredTriggerConnection`
- **多重性**: [0..infinite]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

Defines the connection between one requiredTrigger of this BSW Module instance and one releasedTrigger instance.

######## 引用关系

此容器包含 **3** 个引用：

######### REFERENCE 类型引用

########## 1. RteBswReleasedTriggerModInstRef

- **UUID**: `b675f63f-b064-4a49-bad5-8c0b3c161b1b`
- **引用名**: `RteBswReleasedTriggerModInstRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `RteBswModuleInstance`
- **完整路径**: `/AUTOSAR/EcucDefs/Rte/RteBswModuleInstance`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Reference to the RteBswModuleInstance configuration container which identifies the instance of the BSW Module.

######### FOREIGN-REFERENCE 类型引用

########## 1. RteBswReleasedTriggerRef

- **UUID**: `bf11e2e6-d39c-4487-8272-66e956090bad`
- **引用名**: `RteBswReleasedTriggerRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [1..1]
- **目标类型**: TRIGGER
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: References the releasedTrigger to which this requiredTrigger shall be connected.

########## 2. RteBswRequiredTriggerRef

- **UUID**: `e569a774-bb57-4307-9d97-10b6db0cd41a`
- **引用名**: `RteBswRequiredTriggerRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [1..1]
- **目标类型**: TRIGGER
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: References one requiredTrigger which shall be connected to the releasedTrigger.

##### 3. RteBswEventToTaskMapping

**容器属性**:

- **UUID**: `689a9711-30f6-48ed-a58c-5466db6776c2`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `RteBswEventToTaskMapping`
- **多重性**: [0..infinite]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

Maps a BswSchedulableEntity onto one OsTask based on the activating BswEvent.

###### 参数配置

此容器包含 **5** 个参数：

####### INTEGER 类型参数

######## 1. RteBswPositionInTask

- **UUID**: `3d5f32d9-6ffb-4bdc-9856-150235477f2a`
- **参数名**: `RteBswPositionInTask`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Each BswSchedulableEntity activation mapped to an OsTask has a specific position within the task execution.

####### BOOLEAN 类型参数

######## 1. RteBswImmediateRestart

- **UUID**: `b66a74ec-a021-4512-b120-6140aa31183d`
- **参数名**: `RteBswImmediateRestart`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: When RteBswImmediateRestart is set to true the BswSchedulableEntitiy shall be immediately re-started after termination if it was activated by this BswEvent while it was already started.

####### FLOAT 类型参数

######## 1. RteBswActivationOffset

- **UUID**: `db7fcf51-5387-4e07-a336-488514939e07`
- **参数名**: `RteBswActivationOffset`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **取值范围**: [0..]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Activation offset.

####### ENUMERATION 类型参数

######## 1. RteOsSchedulePoint

- **UUID**: `fd3dfe5a-8085-4d8a-a2b8-3a36910b35a8`
- **参数名**: `RteOsSchedulePoint`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `NONE`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CONDITIONAL`
  - `NONE`
  - `UNCONDITIONAL`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Introduce a schedule point by explicitly calling Os Schedule service after the execution of the ExecutableEntity.  The Rte generator is allowed to optimize several consecutive calls to Os schedule into one single call if the ExecutableEntity executions in between have been skipped.

######## 2. RteCyclicTriggerImplementation

- **UUID**: `67886850-1d5e-468f-b7bf-d0088f970956`
- **参数名**: `RteCyclicTriggerImplementation`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `Auto`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `Auto`
  - `None`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: If set to 'Auto' the RTE generator automatically creates the necessary OS alarm to realize the cyclic trigger with the configured activation offset. 
If set to 'None' the trigger is not implemented by the RTE generator. It has to be implemented by the user either by configuring an appropriate OS alarm or an OS schedule table. 
The OS task and optional the OS event for that trigger can be found in the generated RTE report.

###### 引用关系

此容器包含 **7** 个引用：

####### REFERENCE 类型引用

######## 1. RteBswMappedToTaskRef

- **UUID**: `44950cd8-4276-4f0d-a213-21ac32ebbfb5`
- **引用名**: `RteBswMappedToTaskRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `OsTask`
- **完整路径**: `/AUTOSAR/EcucDefs/Os/OsTask`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Reference to the OsTask the BswSchedulableEntity activated by the RteBswEventRef is mapped to.

######## 2. RteBswUsedOsAlarmRef

- **UUID**: `b2dbf5ca-cb5a-4c3e-826c-b2ec08645d72`
- **引用名**: `RteBswUsedOsAlarmRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `OsAlarm`
- **完整路径**: `/AUTOSAR/EcucDefs/Os/OsAlarm`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: If an OsAlarm is used to activate the OsTask this BswEvent is mapped to it shall be referenced here.

######## 3. RteBswUsedOsEventRef

- **UUID**: `de8edd5a-3cef-4563-a6df-1f3c38977f48`
- **引用名**: `RteBswUsedOsEventRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `OsEvent`
- **完整路径**: `/AUTOSAR/EcucDefs/Os/OsEvent`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: If an OsEvent is used to activate the OsTask this BswEvent is mapped to it shall be referenced here.

######## 4. RteBswUsedOsSchTblExpiryPointRef

- **UUID**: `7f85178d-5486-492c-8aa9-ac25f56162c4`
- **引用名**: `RteBswUsedOsSchTblExpiryPointRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `OsScheduleTableExpiryPoint`
- **完整路径**: `/AUTOSAR/EcucDefs/Os/OsScheduleTable/OsScheduleTableExpiryPoint`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: If an OsScheduleTableExpiryPoint is used to activate the OsTask this BswEvent is mapped to it shall be referenced here.

####### FOREIGN-REFERENCE 类型引用

######## 1. RteBswEventRef

- **UUID**: `48605e56-452e-44a8-9389-e344a6f7a2af`
- **引用名**: `RteBswEventRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [1..1]
- **目标类型**: BSW-EVENT
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Reference to the BswEvent which is pointing to the BswSchedulableEntity being mapped. This allows a fine grained mapping of BswSchedulableEntites based on the activating BswEvent.

######## 2. RteRipsFillRoutineRef

- **UUID**: `5b84fc20-2523-4573-a942-ef2172f85e65`
- **引用名**: `RteRipsFillRoutineRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [0..infinite]
- **目标类型**: CONTAINER
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Reference to a Buffer-Fill Routine implemented by an RTE Implementation Plug-In.

######## 3. RteRipsFlushRoutineRef

- **UUID**: `af92b9d4-28d3-40a1-8e9c-c4a90e01eda7`
- **引用名**: `RteRipsFlushRoutineRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [0..infinite]
- **目标类型**: CONTAINER
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Reference to a Buffer-Flush Routine implemented by an RTE Implementation Plug-In.

##### 4. RteBswExclusiveAreaImpl

**容器属性**:

- **UUID**: `f6c711bd-74bd-470f-8f88-eb52ad6792d3`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `RteBswExclusiveAreaImpl`
- **多重性**: [0..infinite]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

Represents one ExclusiveArea of one BswImplementation. Used to specify the implementation means of this ExclusiveArea.

###### 参数配置

此容器包含 **3** 个参数：

####### BOOLEAN 类型参数

######## 1. RteExclusiveAreaOptimization

- **UUID**: `87bd96ee-3cf1-4ce1-aefa-1be14f9625fd`
- **参数名**: `RteExclusiveAreaOptimization`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter is not yet supported by the RTE generator. Changing the value has no impact on the generated code.

######## 2. RteExclusiveAreaGenerateFunction

- **UUID**: `bad08024-0f02-4dbf-8056-75b7ec5a04f2`
- **参数名**: `RteExclusiveAreaGenerateFunction`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: If set to false/undefined, the BSW Module ImplementationCodeType is used to determine the implementation if possible. If the BSW Module ImplementationCodeType is set to EcuCSourceCode, the following limitations apply: the RTE generator generates a function if the BSW Module is Postbuild loadable, or if the implementation mechanism is set to custom. Otherwise, a macro is generated.

This parameter forces the RTE generator to generate a function for the ExclusiveArea interface implementation (disabling the RTE generator macro optimization).

####### ENUMERATION 类型参数

######## 1. RteExclusiveAreaImplMechanism

- **UUID**: `6d94023f-3028-4e42-9f26-d210fd261dec`
- **参数名**: `RteExclusiveAreaImplMechanism`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `ALL_INTERRUPT_BLOCKING`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `ALL_INTERRUPT_BLOCKING` (来源: AUTOSAR_ECUC)
  - `COOPERATIVE_RUNNABLE_PLACEMENT` (来源: AUTOSAR_ECUC)
  - `OS_INTERRUPT_BLOCKING` (来源: AUTOSAR_ECUC)
  - `OS_RESOURCE` (来源: AUTOSAR_ECUC)
  - `OS_SPINLOCK` (来源: AUTOSAR_ECUC)
  - `NONE` (来源: Vector Informatik)
  - `CUSTOM` (来源: Vector Informatik)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: To be used implementation mechanism for the specified ExclusiveArea.

###### 引用关系

此容器包含 **3** 个引用：

####### REFERENCE 类型引用

######## 1. RteBswExclusiveAreaOsResourceRef

- **UUID**: `caf87c29-5c1a-4d4c-8659-94aa922a46ce`
- **引用名**: `RteBswExclusiveAreaOsResourceRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `OsResource`
- **完整路径**: `/AUTOSAR/EcucDefs/Os/OsResource`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Optional reference to an OsResource in case RteExclusiveAreaImplMechanism is configured to OS_RESOURCE for this ExclusiveArea.

######## 2. RteBswExclusiveAreaOsSpinlockRef

- **UUID**: `ECUC:17fad2ad-eeff-411a-9b4a-2f8bee7c44f1`
- **引用名**: `RteBswExclusiveAreaOsSpinlockRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `OsSpinlock`
- **完整路径**: `/AUTOSAR/EcucDefs/Os/OsSpinlock`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Optional reference to an OsSpinlock in case RteExclusiveAreaImplMechanism is configured to OS_SPINLOCK for this ExclusiveArea.

####### FOREIGN-REFERENCE 类型引用

######## 1. RteBswExclusiveAreaRef

- **UUID**: `b956f3e6-c473-40e4-b15b-26bbfad691e1`
- **引用名**: `RteBswExclusiveAreaRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [1..1]
- **目标类型**: EXCLUSIVE-AREA
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Reference to the ExclusiveArea for which the implementation mechanism shall be specified.

##### 5. RteBswExternalTriggerConfig

**容器属性**:

- **UUID**: `9ea3544c-820e-41d6-b6cf-6392113d4286`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `RteBswExternalTriggerConfig`
- **多重性**: [0..infinite]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

Defines the configuration of Inter Basic Software Module Entity Triggering

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. RteBswTriggerSourceQueueLength

- **UUID**: `aa14658e-c12d-4f5d-899c-77390ba58c29`
- **参数名**: `RteBswTriggerSourceQueueLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Length of trigger queue on the trigger source side.

###### 引用关系

此容器包含 **1** 个引用：

####### FOREIGN-REFERENCE 类型引用

######## 1. RteBswTriggerSourceRef

- **UUID**: `9e0dee0c-5f3d-421f-b4b4-db04be364889`
- **引用名**: `RteBswTriggerSourceRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [1..1]
- **目标类型**: TRIGGER
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Reference to a Trigger instance in the role releasedTrigger of the related BSW Module instance.

##### 6. RteBswInternalTriggerConfig

**容器属性**:

- **UUID**: `7c9d27f9-aca0-4d67-a895-06b7e891325f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `RteBswInternalTriggerConfig`
- **多重性**: [0..infinite]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

Defines the configuration of internal Basic Software Module Entity Triggering

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. RteBswTriggerSourceQueueLength

- **UUID**: `ad0e35c0-29db-4e3e-9d07-7de6cd34f9a8`
- **参数名**: `RteBswTriggerSourceQueueLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Length of trigger queue on the trigger source side.

###### 引用关系

此容器包含 **1** 个引用：

####### FOREIGN-REFERENCE 类型引用

######## 1. RteBswTriggerSourceRef

- **UUID**: `ebf60df3-84b7-4307-93f7-cb34c269036d`
- **引用名**: `RteBswTriggerSourceRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [1..1]
- **目标类型**: BSW-INTERNAL-TRIGGERING-POINT
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Reference to a BswInternalTriggeringPoint of the related BSW Module instance.

##### 7. RteBswRequiredModeGroupConnection

**容器属性**:

- **UUID**: `64b34f5b-9f2f-4ee9-a5d7-211213055751`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `RteBswRequiredModeGroupConnection`
- **多重性**: [0..infinite]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

Defines the connection between one requiredModeGroup of this BSW Module instance and one providedModeGroup instance.

###### 引用关系

此容器包含 **3** 个引用：

####### REFERENCE 类型引用

######## 1. RteBswProvidedModeGrpModInstRef

- **UUID**: `8b3f7b0b-e8b6-451f-a924-02a50a600087`
- **引用名**: `RteBswProvidedModeGrpModInstRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `RteBswModuleInstance`
- **完整路径**: `/AUTOSAR/EcucDefs/Rte/RteBswModuleInstance`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Reference to the RteBswModuleInstance configuration container which identifies the instance of the BSW Module.

####### FOREIGN-REFERENCE 类型引用

######## 1. RteBswProvidedModeGroupRef

- **UUID**: `ac6ba743-c98a-4435-b80b-c5c687f2ad9f`
- **引用名**: `RteBswProvidedModeGroupRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [1..1]
- **目标类型**: MODE-DECLARATION-GROUP-PROTOTYPE
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: References the providedModeGroupPrototype to which this requiredModeGroup shall be connected.

######## 2. RteBswRequiredModeGroupRef

- **UUID**: `7dbdd9bc-5b6a-4ce8-a217-9bbf7369827d`
- **引用名**: `RteBswRequiredModeGroupRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [1..1]
- **目标类型**: MODE-DECLARATION-GROUP-PROTOTYPE
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: References requiredModeGroupPrototype which shall be connected to the providedModeGroupPrototype.

##### 8. RteBswRequiredTriggerConnection

**容器属性**:

- **UUID**: `817bdb91-58c6-480c-ba31-34b6f8c6f53f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `RteBswRequiredTriggerConnection`
- **多重性**: [0..infinite]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

Defines the connection between one requiredTrigger of this BSW Module instance and one releasedTrigger instance.

###### 引用关系

此容器包含 **3** 个引用：

####### REFERENCE 类型引用

######## 1. RteBswReleasedTriggerModInstRef

- **UUID**: `b675f63f-b064-4a49-bad5-8c0b3c161b1b`
- **引用名**: `RteBswReleasedTriggerModInstRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `RteBswModuleInstance`
- **完整路径**: `/AUTOSAR/EcucDefs/Rte/RteBswModuleInstance`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Reference to the RteBswModuleInstance configuration container which identifies the instance of the BSW Module.

####### FOREIGN-REFERENCE 类型引用

######## 1. RteBswReleasedTriggerRef

- **UUID**: `bf11e2e6-d39c-4487-8272-66e956090bad`
- **引用名**: `RteBswReleasedTriggerRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [1..1]
- **目标类型**: TRIGGER
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: References the releasedTrigger to which this requiredTrigger shall be connected.

######## 2. RteBswRequiredTriggerRef

- **UUID**: `e569a774-bb57-4307-9d97-10b6db0cd41a`
- **引用名**: `RteBswRequiredTriggerRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [1..1]
- **目标类型**: TRIGGER
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: References one requiredTrigger which shall be connected to the releasedTrigger.

##### 9. RteExclusiveAccessOptimization

**容器属性**:

- **UUID**: `823cf487-e33b-4462-a457-3bb5ca8dd8de`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `RteExclusiveAccessOptimization`
- **多重性**: [0..infinite]
- **构建后可变**: false

**容器描述**:

Configuration of the optimized access behavior to be generated. In other words, access shall be mutually exclusive. How this is realized e.g. non preemptive task mapping, exclusive areas, mode management, exclusive access during ECU startup and shutdown or scheduling in exclusive time slots is up to the ECU integrator.

###### 引用关系

此容器包含 **3** 个引用：

####### FOREIGN-REFERENCE 类型引用

######## 1. RteAccessingEntityRef

- **UUID**: `2fd0dd88-f097-4b25-9e86-3607b5ccd1b6`
- **引用名**: `RteAccessingEntityRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [0..infinite]
- **目标类型**: EXECUTABLE-ENTITY
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Reference to executable entities (e.g. NvM main function) that access the CommunicationGraph with non-modeled standardized interfaces.

####### INSTANCE-REFERENCE 类型引用

######## 1. RteSoftwareComponentReadRef

- **UUID**: `b328e2d2-4b74-430a-bd92-fcaa6c42380b`
- **引用名**: `RteSoftwareComponentReadRef`
- **引用类型**: INSTANCE-REFERENCE
- **多重性**: [0..1]
- **目标类型**: VARIABLE-ACCESS
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Reference to the read variableAccess role.

######## 2. RteSoftwareComponentWriteRef

- **UUID**: `2a799ad6-3ea5-4d3b-9004-7300dd89e298`
- **引用名**: `RteSoftwareComponentWriteRef`
- **引用类型**: INSTANCE-REFERENCE
- **多重性**: [0..1]
- **目标类型**: VARIABLE-ACCESS
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Reference to the VariableAccess in the dataSendPoint role of the writing software-component.

##### 10. RteGeneration

**容器属性**:

- **UUID**: `d18f2717-e93d-4fb9-9784-0efd72d25620`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `RteGeneration`
- **多重性**: [1..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container holds the parameters for the configuration of the RTE Generation.

###### 参数配置

此容器包含 **32** 个参数：

####### INTEGER 类型参数

######## 1. RteCodeVendorId

- **UUID**: `243571c1-8d81-49b1-8f51-54ffe3b0f48e`
- **参数名**: `RteCodeVendorId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `30`
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Holds the vendor ID of the generated Rte code.

######## 2. RteToolChainSignificantCharacters

- **UUID**: `bdc4a933-d907-4469-b8f1-ef9468fb75d0`
- **参数名**: `RteToolChainSignificantCharacters`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `31`
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: If present, the RTE generator shall provide the list of C RTE identifiers whose name is not unique when only the first RteToolChainSignificantCharacters characters are considered.

######## 3. RteCalibrationBufferSize

- **UUID**: `5a4b1896-fc95-4d24-9088-dc43709fb233`
- **参数名**: `RteCalibrationBufferSize`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter specifies the size of the RAM buffer for the calibration, if single-pointered or double-pointered online calibration is used.
If set to 0, the RTE generator won't generate a RAM buffer.

######## 4. RteAlarmGlobalStartOffset

- **UUID**: `2294b32e-67bd-4faf-820d-5dae21c8efcc`
- **参数名**: `RteAlarmGlobalStartOffset`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `1`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: global start offset for cyclic runnables when SetAbsAlarm or SetRelAlarm is used.

####### BOOLEAN 类型参数

######## 1. RteDevErrorDetect

- **UUID**: `84151a55-96f4-4115-8421-4d9fe60a7dc7`
- **参数名**: `RteDevErrorDetect`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: The Rte shall log development errors to the Det module.

######## 2. RteDevErrorDetectUninit

- **UUID**: `ae1411aa-7e58-412a-a915-c1170b7bbd9c`
- **参数名**: `RteDevErrorDetectUninit`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: The Rte shall detect if it is started when its APIs are called, and the BSW Scheduler shall check if it is initialized when its APIs are called.

######## 3. RteMeasurementSupport

- **UUID**: `c17e1881-02c6-4c57-8336-a91aa89a9430`
- **参数名**: `RteMeasurementSupport`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: The RTE generator shall have the option to switch off support for measurement for generated RTE code. This option shall influence complete RTE code at once.

######## 4. RteValueRangeCheckEnabled

- **UUID**: `f3483b83-4a3b-4b59-ad87-10699efd1e33`
- **参数名**: `RteValueRangeCheckEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: If set to true the RTE generator shall enable the value range checking for the specified VariableDataPrototypes.

######## 5. RteVfbTraceEnabled

- **UUID**: `7c2e7042-c01a-47ac-9567-c8669446060b`
- **参数名**: `RteVfbTraceEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: The RTE generator shall globally enable VFB tracing when RteVfbTrace is set to "true".

######## 6. RteXcpEventSupport

- **UUID**: `808feace-b102-4ec5-b102-775e754f8e5b`
- **参数名**: `RteXcpEventSupport`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: If set to true, the RTE generator uses the Xcp driver to send Xcp Events when the runnables of a task were processed. These events can be used to trigger the measurement of variables in a measurement and calibration tool.
This also allows the measurement of sender / receiver ports when implicit inter-ECU communication is used.

######## 7. RteEnforceIoc

- **UUID**: `0a9ba98b-098f-4836-94b0-0e091ff091bb`
- **参数名**: `RteEnforceIoc`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Enforce the usage of IOCs for cross-partition communication.
If this parameter is set to false, the RTE assumes that all partitions have read access to all RTE variables.
Buffers are allocated to the writing partition and IOCs are only used for N:1 communication.
Buffers that are used for cross-core communication need to be mapped to synchronized RAM so that spinlocks only need to 
be used for variables that cannot be accessed atomically.
If this parameter is set to true, the RTE relies on OS IOC objects for cross-partition communication.
As the OS does not know which runnables access the individual IOCs, this tends to be less efficient when it comes to
interrupt/spinlock locking times, runtime, ram and rom consumption.
The parameter is ignored for:
- mode communication
- inter-ECU client-server communication
- nv data communication
- sender-receiver communication when transformers and scaling are configured

######## 8. RteInitializeImplicitBuffers

- **UUID**: `504f6e2a-e000-428b-a0ff-abb8a23148f8`
- **参数名**: `RteInitializeImplicitBuffers`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter ensures that no undefined values are written back at runnable termination.
If this parameter is set to true, the RTE will send the last written value.
If no RTE API for implicit write is called before, the initValue will be sent.

[SWS_Rte_08418]

######## 9. RteEnforceQueuedIoc

- **UUID**: `3d249ee4-ce6b-4262-89ea-a881581cefc5`
- **参数名**: `RteEnforceQueuedIoc`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Enforce the usage of IOCs for queued cross-partition communication.
Unlike the RteEnforceIoc parameter, this parameter only affects queued communication.
If this parameter is set to true, the RTE relies on OS IOC objects for queued cross-partition communication.
If the OS provides spinlock free IOCs, this parameter can be set to true to avoid the spinlock generation in the RTE for queued
sender-receiver communication.

The parameter is ignored for:
- mode communication
- inter-ECU client-server communication
- sender-receiver communication when transformers and scaling are configured

######## 10. RteUseAbsAlarmInitialization

- **UUID**: `3da43555-f8d3-451c-9591-ce5835385726`
- **参数名**: `RteUseAbsAlarmInitialization`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: The RTE generator shall use SetAbsAlarm() for alarm initialization.

######## 11. RteOptimizeLocksInASILPartitions

- **UUID**: `20fd4241-d04c-409f-8c9a-d26559a8bc5b`
- **参数名**: `RteOptimizeLocksInASILPartitions`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: If this parameter is set to true, the RTE generator also considers the task priorities and preemption settings to optimize APIs in ASIL partitions.
Otherwise, the RTE generator uses a more conservative locking strategy for ASIL partitions to reduce the risk of data consistency problems when the APIs are accidentally called from the wrong task.
Independently of the value of this switch, it is the responsibility of the user to call the APIs only from runnables that are configured to use the APIs.

######## 12. UseRteSemanticsForIntraLetCommunication

- **UUID**: `502752a5-c270-4066-ba92-490e27e77000`
- **参数名**: `UseRteSemanticsForIntraLetCommunication`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `true`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Enables an alternative LET communication semantic.
If this parameter is set to true the RTE generator treats the implicit communication within a LET interval as if it were the classic implicit communication. Otherwise the communication will be purely handled by LET semantics.

######## 13. RteBasicRuntimeEnvironmentMode

- **UUID**: `bde36784-fa47-4f68-a57c-ece883645cfc`
- **参数名**: `RteBasicRuntimeEnvironmentMode`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Activates Generation of BRE.

######## 14. RteEnableLET

- **UUID**: `d605bc2f-fc32-4c69-8f36-3f8b8224a03e`
- **参数名**: `RteEnableLET`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Enables generation of LET.

######## 15. RteEnableMemoryProtection

- **UUID**: `4d3b2a92-8988-478c-bdc7-73ae76811667`
- **参数名**: `RteEnableMemoryProtection`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Is set to true if memory protection is configured.

######## 16. RteEnableMultiCore

- **UUID**: `7239e626-258e-411d-a391-51ceaa47a6c5`
- **参数名**: `RteEnableMultiCore`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Is set to true if multi core is configured.

######## 17. RteDisableInterEcuIntToIntDataConversion

- **UUID**: `077b2c02-9114-43f5-abf7-acccef398d6e`
- **参数名**: `RteDisableInterEcuIntToIntDataConversion`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Disables inter ecu integer to integer data conversion.
For BSW packages before R31, the switch gets automatically set to true if it is not configured. Starting with R31 the conversion is always enabled if not explicitly disabled by this switch. The RTE generator derives the conversion formula from the CompuMethod on the system signal and the data element.

######## 18. RteDisableRteInitMemory

- **UUID**: `f3a7169c-1ce8-4e51-98fd-68e537621d25`
- **参数名**: `RteDisableRteInitMemory`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: The API function Rte_InitMemory and SomeIpXf_InitMemory is a MICROSAR Classic RTE/SomeIpXf specific extension and should be used to initialize RTE/SomeIpXf internal state variables if the compiler does not support initialized variables.
If the system has already initialized the variables, the Rte_InitMemory and SomeIpXf_InitMemory-API can be deactivated and the API will no longer be generated to save ROM.

######## 19. RteDisableOsScheduleTableAndAlarmGeneration

- **UUID**: `375a6dff-b401-4285-b1a5-18213919ad4f`
- **参数名**: `RteDisableOsScheduleTableAndAlarmGeneration`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Disables the generation of the os schedule tables and alarms for timing events.
The elements are no longer added to the OS configuration and the RTE no longer starts them in the RTE lifecycle APIs.
This parameter can be used for cases where the tasks are activated manually by the integration code.

####### STRING 类型参数

######## 1. RteVttVfbTraceFunction

- **UUID**: `6f65a68b-630d-44bd-950a-d0ade119277f`
- **参数名**: `RteVttVfbTraceFunction`
- **数据类型**: STRING
- **多重性**: [0..infinite]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: The RTE generator shall enable VTT tracing for the given hook function.

####### ENUMERATION 类型参数

######## 1. RteCalibrationSupport

- **UUID**: `1679435b-da55-4a72-846c-ddc0d5ea50ff`
- **参数名**: `RteCalibrationSupport`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `NONE`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `DOUBLE_POINTERED` (来源: AUTOSAR_ECUC)
  - `INITIALIZED_RAM` (来源: AUTOSAR_ECUC)
  - `NONE` (来源: AUTOSAR_ECUC)
  - `SINGLE_POINTERED` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: The RTE generator shall have the option to switch off support for calibration for generated RTE code. This option shall influence complete RTE code at once.

######## 2. RteGenerationMode

- **UUID**: `4cbd6404-da96-4f1b-92b6-45759e3f1954`
- **参数名**: `RteGenerationMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `COMPATIBILITY_MODE`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `COMPATIBILITY_MODE` (来源: AUTOSAR_ECUC)
  - `VENDOR_MODE` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Switch between the two available generation modes of the RTE generator.

######## 3. RteIocInteractionReturnValue

- **UUID**: `65f3a2ac-807e-46a1-9be4-c71e2d536307`
- **参数名**: `RteIocInteractionReturnValue`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `RTE_IOC`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `RTE_COM` (来源: AUTOSAR_ECUC)
  - `RTE_IOC` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Defines whether the return value of RTE APIs is based on RTE-IOC interaction or RTE-COM interaction.

######## 4. RteOptimizationMode

- **UUID**: `b02183e1-5af9-46a0-9672-dffea60115f7`
- **参数名**: `RteOptimizationMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `RUNTIME`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `MEMORY` (来源: AUTOSAR_ECUC)
  - `RUNTIME` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Switch between the two available optimization modes of the RTE generator.

######## 5. RteA2LVersion

- **UUID**: `f5c43cb5-6b34-4aaa-9746-a1d8e3a47576`
- **参数名**: `RteA2LVersion`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `V160`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `V151`
  - `V160`
  - `V171`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: When measurement is enabled, the RTE generator generates an A2L file that contains the measurement and characteristic objects of the generated RTE.
This parameter specifies the ASAM MCD-2MC standard to which the A2L file is compliant.
Version 1.6.0 supports additional features like linker map references for the measurement objects.

######## 6. RteComTimeoutSource

- **UUID**: `7a282855-fc9d-45fd-9c3c-5d83e0077ffb`
- **参数名**: `RteComTimeoutSource`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `SWC`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `SWC` (来源: Vector Informatik)
  - `SIGNAL` (来源: Vector Informatik)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter specifies the source for deriving the ComTimeout parameter of a ComSignal / ComSignalGroup.

SWC: The timeout value is derived from the ReceiverComSpec (AliveTimeout) of the SWC port description.
SIGNAL: The timeout value is derived from the ISignalPort of the communication description. This still requires a timeout value (AliveTimoeut) at the ReceiverComSpec != 0 to generally enable the timeout handling.

####### FUNCTION-NAME 类型参数

######## 1. RteVfbTraceFunction

- **UUID**: `b1e9de8b-4dce-46d7-97a3-9f4a757e64da`
- **参数名**: `RteVfbTraceFunction`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..infinite]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: The RTE generator shall enable VFB tracing for a given hook function when there is a #define in the RTE configuration header file for the hook function name and tracing is globally enabled.

####### LINKER-SYMBOL 类型参数

######## 1. RteVfbTraceClientPrefix

- **UUID**: `da6020cc-8125-42a1-abc5-971035bf5f3a`
- **参数名**: `RteVfbTraceClientPrefix`
- **数据类型**: LINKER-SYMBOL
- **多重性**: [0..infinite]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Defines an additional prefix for all VFB trace functions to be generated. With this approach it is possible to have debugging and DLT trace functions at the same time.

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. RteVfbTraceClient

**容器属性**:

- **UUID**: `2bae121f-e80f-4cd3-b43a-f7a110d45fff`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `RteVfbTraceClient`
- **多重性**: [0..infinite]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

The RTE shall add the VFB Trace client with the ShortName of this container as the client’s prefix.

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. RteVfbTraceClientPosition

- **UUID**: `1c99d6d3-61ce-4f52-ac50-65f225c33dc2`
- **参数名**: `RteVfbTraceClientPosition`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..65535]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Defines the position within all trace clients at which to call the trace functions of this trace client. The bigger the number the later the start trace functions and the sooner the stop trace functions will be called.

######### FUNCTION-NAME 类型参数

########## 1. RteVfbTraceFunction

- **UUID**: `6ed46e9c-e5ae-4f7c-b7e9-60b0ad074641`
- **参数名**: `RteVfbTraceFunction`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..infinite]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: The RTE generator shall enable VFB tracing for a given hook function when its name starts with the string configured here. Example: If Rte_Dbg_WriteHook_i2 is configured, Rte_Dbg_WriteHook_i1_p1_a_Start will be enabled.

######## 引用关系

此容器包含 **1** 个引用：

######### FOREIGN-REFERENCE 类型引用

########## 1. RteVfbTraceHooksRef

- **UUID**: `6a6ff55e-35ce-46f9-b6f5-de2df979452f`
- **引用名**: `RteVfbTraceHooksRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [0..1]
- **目标类型**: CONTAINER
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Reference to the container in the VFB Trace client’s configuration to which the RTE shall add the descriptions of the trace hooks created for this client.

##### 11. RteVfbTraceClient

**容器属性**:

- **UUID**: `2bae121f-e80f-4cd3-b43a-f7a110d45fff`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `RteVfbTraceClient`
- **多重性**: [0..infinite]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

The RTE shall add the VFB Trace client with the ShortName of this container as the client’s prefix.

###### 参数配置

此容器包含 **2** 个参数：

####### INTEGER 类型参数

######## 1. RteVfbTraceClientPosition

- **UUID**: `1c99d6d3-61ce-4f52-ac50-65f225c33dc2`
- **参数名**: `RteVfbTraceClientPosition`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..65535]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Defines the position within all trace clients at which to call the trace functions of this trace client. The bigger the number the later the start trace functions and the sooner the stop trace functions will be called.

####### FUNCTION-NAME 类型参数

######## 1. RteVfbTraceFunction

- **UUID**: `6ed46e9c-e5ae-4f7c-b7e9-60b0ad074641`
- **参数名**: `RteVfbTraceFunction`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..infinite]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: The RTE generator shall enable VFB tracing for a given hook function when its name starts with the string configured here. Example: If Rte_Dbg_WriteHook_i2 is configured, Rte_Dbg_WriteHook_i1_p1_a_Start will be enabled.

###### 引用关系

此容器包含 **1** 个引用：

####### FOREIGN-REFERENCE 类型引用

######## 1. RteVfbTraceHooksRef

- **UUID**: `6a6ff55e-35ce-46f9-b6f5-de2df979452f`
- **引用名**: `RteVfbTraceHooksRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [0..1]
- **目标类型**: CONTAINER
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Reference to the container in the VFB Trace client’s configuration to which the RTE shall add the descriptions of the trace hooks created for this client.

##### 12. RteImplicitCommunication

**容器属性**:

- **UUID**: `30562a03-8972-4425-99b6-f2dd67ea0e31`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `RteImplicitCommunication`
- **多重性**: [0..infinite]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

Configuration of the Implicit Communication behavior to be generated.

###### 参数配置

此容器包含 **2** 个参数：

####### BOOLEAN 类型参数

######## 1. RteCoherentAccess

- **UUID**: `d9b65e0c-c6f7-4b95-a073-c80f4d6deeaa`
- **参数名**: `RteCoherentAccess`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: If set to true the referenced VariableAccess'es of this RteImplicitCommunication container are in one CoherencyGroup.

######## 2. RteImmediateBufferUpdate

- **UUID**: `e180363d-5127-42d0-81bd-d8ba5d042c61`
- **参数名**: `RteImmediateBufferUpdate`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: If set to true the RTE will perform preemption area specific buffer update immediately before (for VariableAccess in the role dataReadAccess) resp. after (for VariableAccess in the role dataWriteAccess) Runnable execution.

###### 引用关系

此容器包含 **3** 个引用：

####### FOREIGN-REFERENCE 类型引用

######## 1. RteVariableReadAccessRef

- **UUID**: `dd71339c-02a4-4b56-a146-a9f23fb3a0a2`
- **引用名**: `RteVariableReadAccessRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [0..infinite]
- **目标类型**: VARIABLE-ACCESS
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Reference to the VariableAccess in the dataReadAccess role.

######## 2. RteVariableWriteAccessRef

- **UUID**: `f7104e46-81d7-4949-bc6e-55f4c9ab0560`
- **引用名**: `RteVariableWriteAccessRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [0..infinite]
- **目标类型**: VARIABLE-ACCESS
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Reference to the VariableAccess in the dataWriteAccess role.

####### INSTANCE-REFERENCE 类型引用

######## 1. RteSoftwareComponentInstanceRef

- **UUID**: `1235e926-43b8-458c-bc55-9e124c38691f`
- **引用名**: `RteSoftwareComponentInstanceRef`
- **引用类型**: INSTANCE-REFERENCE
- **多重性**: [1..infinite]
- **目标类型**: SW-COMPONENT-PROTOTYPE
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Reference to a SwComponentPrototype.

##### 13. RteInitializationBehavior

**容器属性**:

- **UUID**: `1be0d90e-de23-4f43-824d-8c00b20f2a11`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `RteInitializationBehavior`
- **多重性**: [1..infinite]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

Specifies the initialization strategy for variables allocated by RTE with the purpose to implement VariableDataPrototypes.

###### 参数配置

此容器包含 **2** 个参数：

####### STRING 类型参数

######## 1. RteSectionInitializationPolicy

- **UUID**: `6a263088-0854-426f-a6bb-68d9ae8a1551`
- **参数名**: `RteSectionInitializationPolicy`
- **数据类型**: STRING
- **多重性**: [1..infinite]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter describes the SectionInitializationPolicys for which a particular RTE initialization strategy applies.

####### ENUMERATION 类型参数

######## 1. RteInitializationStrategy

- **UUID**: `819a4982-c4f0-4e57-b256-04310882ebfb`
- **参数名**: `RteInitializationStrategy`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `RTE_INITIALIZATION_STRATEGY_AT_RTE_START_AND_PARTITION_RESTART`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `RTE_INITIALIZATION_STRATEGY_AT_DATA_DECLARATION` (来源: AUTOSAR_ECUC)
  - `RTE_INITIALIZATION_STRATEGY_AT_DATA_DECLARATION_AND_PARTITION_RESTART` (来源: AUTOSAR_ECUC)
  - `RTE_INITIALIZATION_STRATEGY_AT_RTE_START_AND_PARTITION_RESTART` (来源: AUTOSAR_ECUC)
  - `RTE_INITIALIZATION_STRATEGY_NONE` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Definition of the initialization strategy applicable for the SectionInitializationPolicys selected by RteSectionInitializationPolicy.

##### 14. RteOsInteraction

**容器属性**:

- **UUID**: `7160a12e-86fa-4e32-a97e-5a6b6bfa1234`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `RteOsInteraction`
- **多重性**: [1..infinite]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

Interaction of the Rte with the Os.

###### 配置容器

本模块包含 **4** 个配置容器：

####### 1. RteModeToScheduleTableMapping

**容器属性**:

- **UUID**: `411cf0f2-4d23-4aba-961d-d92875106352`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `RteModeToScheduleTableMapping`
- **多重性**: [0..infinite]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

Provides configuration input in which Modes of a ModeDeclarionGroupPrototype of a Mode Manager a OsScheudleTable shall be active.

######## 引用关系

此容器包含 **2** 个引用：

######### REFERENCE 类型引用

########## 1. RteModeScheduleTableRef

- **UUID**: `31f248cc-3b5a-4dfa-afa2-0513d0939066`
- **引用名**: `RteModeScheduleTableRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `OsScheduleTable`
- **完整路径**: `/AUTOSAR/EcucDefs/Os/OsScheduleTable`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Reference to the OsScheduleTable which shall be active in the specified RteModeSchblMapModeDeclarationRefs.

######### FOREIGN-REFERENCE 类型引用

########## 1. RteModeSchtblMapModeDeclarationRef

- **UUID**: `20bf841c-abe2-4f24-9d01-72866e0108fd`
- **引用名**: `RteModeSchtblMapModeDeclarationRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [1..infinite]
- **目标类型**: MODE-DECLARATION
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Reference to the ModeDeclarations.

######## 配置容器

本模块包含 **2** 个配置容器：

######### 1. RteModeSchtblMapBsw

**容器属性**:

- **UUID**: `3cf22fc0-2a6e-4e1d-8657-f8d5992e3e3c`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `RteModeSchtblMapBsw`
- **多重性**: [0..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

Specifies an instance of a ModeDeclarationGroupPrototype of a Bsw-Module.

########## 引用关系

此容器包含 **2** 个引用：

########### REFERENCE 类型引用

############ 1. RteModeSchtblMapBswInstanceRef

- **UUID**: `6cdfb5dd-62bb-407b-b4a6-b4a299184c95`
- **引用名**: `RteModeSchtblMapBswInstanceRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `RteBswModuleInstance`
- **完整路径**: `/AUTOSAR/EcucDefs/Rte/RteBswModuleInstance`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Reference to an instance specification of a Bsw-Module.

########### FOREIGN-REFERENCE 类型引用

############ 1. RteModeSchtblMapBswProvidedModeGroupRef

- **UUID**: `eccf0465-ceee-4510-9910-fbb16567cfb5`
- **引用名**: `RteModeSchtblMapBswProvidedModeGroupRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [1..1]
- **目标类型**: MODE-DECLARATION-GROUP-PROTOTYPE
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Reference to an instance of a ModeDeclarationGroupPrototype of a Bsw-Module.

######### 2. RteModeSchtblMapSwc

**容器属性**:

- **UUID**: `863541a7-8054-4564-b205-aa7cfeeaa1d1`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `RteModeSchtblMapSwc`
- **多重性**: [0..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

Specifies an instance of a ModeDeclarationGroupPrototype of a SwComponentPrototype.

########## 引用关系

此容器包含 **2** 个引用：

########### REFERENCE 类型引用

############ 1. RteModeSchtblMapSwcInstanceRef

- **UUID**: `1ff62917-48b2-4ed7-9302-e18d154edab3`
- **引用名**: `RteModeSchtblMapSwcInstanceRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `RteSwComponentInstance`
- **完整路径**: `/AUTOSAR/EcucDefs/Rte/RteSwComponentInstance`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Reference to an instance specification of a SwComponentPrototype.

########### FOREIGN-REFERENCE 类型引用

############ 1. RteModeSchtblMapSwcPortRef

- **UUID**: `5a8ddca7-c77e-4fba-a284-c0d65f31d865`
- **引用名**: `RteModeSchtblMapSwcPortRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [1..1]
- **目标类型**: P-PORT-PROTOTYPE
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Reference to the PPortPrototype of a SwComponentPrototype.

####### 2. RteModeSchtblMapBsw

**容器属性**:

- **UUID**: `3cf22fc0-2a6e-4e1d-8657-f8d5992e3e3c`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `RteModeSchtblMapBsw`
- **多重性**: [0..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

Specifies an instance of a ModeDeclarationGroupPrototype of a Bsw-Module.

######## 引用关系

此容器包含 **2** 个引用：

######### REFERENCE 类型引用

########## 1. RteModeSchtblMapBswInstanceRef

- **UUID**: `6cdfb5dd-62bb-407b-b4a6-b4a299184c95`
- **引用名**: `RteModeSchtblMapBswInstanceRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `RteBswModuleInstance`
- **完整路径**: `/AUTOSAR/EcucDefs/Rte/RteBswModuleInstance`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Reference to an instance specification of a Bsw-Module.

######### FOREIGN-REFERENCE 类型引用

########## 1. RteModeSchtblMapBswProvidedModeGroupRef

- **UUID**: `eccf0465-ceee-4510-9910-fbb16567cfb5`
- **引用名**: `RteModeSchtblMapBswProvidedModeGroupRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [1..1]
- **目标类型**: MODE-DECLARATION-GROUP-PROTOTYPE
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Reference to an instance of a ModeDeclarationGroupPrototype of a Bsw-Module.

####### 3. RteModeSchtblMapSwc

**容器属性**:

- **UUID**: `863541a7-8054-4564-b205-aa7cfeeaa1d1`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `RteModeSchtblMapSwc`
- **多重性**: [0..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

Specifies an instance of a ModeDeclarationGroupPrototype of a SwComponentPrototype.

######## 引用关系

此容器包含 **2** 个引用：

######### REFERENCE 类型引用

########## 1. RteModeSchtblMapSwcInstanceRef

- **UUID**: `1ff62917-48b2-4ed7-9302-e18d154edab3`
- **引用名**: `RteModeSchtblMapSwcInstanceRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `RteSwComponentInstance`
- **完整路径**: `/AUTOSAR/EcucDefs/Rte/RteSwComponentInstance`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Reference to an instance specification of a SwComponentPrototype.

######### FOREIGN-REFERENCE 类型引用

########## 1. RteModeSchtblMapSwcPortRef

- **UUID**: `5a8ddca7-c77e-4fba-a284-c0d65f31d865`
- **引用名**: `RteModeSchtblMapSwcPortRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [1..1]
- **目标类型**: P-PORT-PROTOTYPE
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Reference to the PPortPrototype of a SwComponentPrototype.

####### 4. RteUsedOsActivation

**容器属性**:

- **UUID**: `86502546-eb26-4bc5-aa81-e6f2125c1db7`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `RteUsedOsActivation`
- **多重性**: [0..infinite]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

Attributes used in the activation of OsTasks and Runnable Entities.

######## 参数配置

此容器包含 **2** 个参数：

######### FLOAT 类型参数

########## 1. RteExpectedActivationOffset

- **UUID**: `75b4f494-95e0-4781-b58e-4d0d701ac9a9`
- **参数名**: `RteExpectedActivationOffset`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Activation offset.

########## 2. RteExpectedTickDuration

- **UUID**: `3e6976a0-d393-481e-bb0b-2af417f9d169`
- **参数名**: `RteExpectedTickDuration`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: The expected tick duration which shall be configured to drive the OsScheduleTables or OsAlarm.

######## 引用关系

此容器包含 **3** 个引用：

######### REFERENCE 类型引用

########## 1. RteActivationOsAlarmRef

- **UUID**: `b87517f3-82ce-472f-91ac-067aa222ce4b`
- **引用名**: `RteActivationOsAlarmRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `OsAlarm`
- **完整路径**: `/AUTOSAR/EcucDefs/Os/OsAlarm`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Reference to an OsAlarm.

########## 2. RteActivationOsSchTblRef

- **UUID**: `6b2fdc09-3aa5-440b-a111-3d438f669466`
- **引用名**: `RteActivationOsSchTblRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `OsScheduleTable`
- **完整路径**: `/AUTOSAR/EcucDefs/Os/OsScheduleTable`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Reference to an OsScheduleTable.

########## 3. RteActivationOsTaskRef

- **UUID**: `d3547a38-b37f-41dc-b93b-b9780e41034d`
- **引用名**: `RteActivationOsTaskRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `OsTask`
- **完整路径**: `/AUTOSAR/EcucDefs/Os/OsTask`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Reference to an OsTask.

##### 15. RteModeToScheduleTableMapping

**容器属性**:

- **UUID**: `411cf0f2-4d23-4aba-961d-d92875106352`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `RteModeToScheduleTableMapping`
- **多重性**: [0..infinite]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

Provides configuration input in which Modes of a ModeDeclarionGroupPrototype of a Mode Manager a OsScheudleTable shall be active.

###### 引用关系

此容器包含 **2** 个引用：

####### REFERENCE 类型引用

######## 1. RteModeScheduleTableRef

- **UUID**: `31f248cc-3b5a-4dfa-afa2-0513d0939066`
- **引用名**: `RteModeScheduleTableRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `OsScheduleTable`
- **完整路径**: `/AUTOSAR/EcucDefs/Os/OsScheduleTable`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Reference to the OsScheduleTable which shall be active in the specified RteModeSchblMapModeDeclarationRefs.

####### FOREIGN-REFERENCE 类型引用

######## 1. RteModeSchtblMapModeDeclarationRef

- **UUID**: `20bf841c-abe2-4f24-9d01-72866e0108fd`
- **引用名**: `RteModeSchtblMapModeDeclarationRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [1..infinite]
- **目标类型**: MODE-DECLARATION
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Reference to the ModeDeclarations.

###### 配置容器

本模块包含 **2** 个配置容器：

####### 1. RteModeSchtblMapBsw

**容器属性**:

- **UUID**: `3cf22fc0-2a6e-4e1d-8657-f8d5992e3e3c`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `RteModeSchtblMapBsw`
- **多重性**: [0..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

Specifies an instance of a ModeDeclarationGroupPrototype of a Bsw-Module.

######## 引用关系

此容器包含 **2** 个引用：

######### REFERENCE 类型引用

########## 1. RteModeSchtblMapBswInstanceRef

- **UUID**: `6cdfb5dd-62bb-407b-b4a6-b4a299184c95`
- **引用名**: `RteModeSchtblMapBswInstanceRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `RteBswModuleInstance`
- **完整路径**: `/AUTOSAR/EcucDefs/Rte/RteBswModuleInstance`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Reference to an instance specification of a Bsw-Module.

######### FOREIGN-REFERENCE 类型引用

########## 1. RteModeSchtblMapBswProvidedModeGroupRef

- **UUID**: `eccf0465-ceee-4510-9910-fbb16567cfb5`
- **引用名**: `RteModeSchtblMapBswProvidedModeGroupRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [1..1]
- **目标类型**: MODE-DECLARATION-GROUP-PROTOTYPE
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Reference to an instance of a ModeDeclarationGroupPrototype of a Bsw-Module.

####### 2. RteModeSchtblMapSwc

**容器属性**:

- **UUID**: `863541a7-8054-4564-b205-aa7cfeeaa1d1`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `RteModeSchtblMapSwc`
- **多重性**: [0..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

Specifies an instance of a ModeDeclarationGroupPrototype of a SwComponentPrototype.

######## 引用关系

此容器包含 **2** 个引用：

######### REFERENCE 类型引用

########## 1. RteModeSchtblMapSwcInstanceRef

- **UUID**: `1ff62917-48b2-4ed7-9302-e18d154edab3`
- **引用名**: `RteModeSchtblMapSwcInstanceRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `RteSwComponentInstance`
- **完整路径**: `/AUTOSAR/EcucDefs/Rte/RteSwComponentInstance`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Reference to an instance specification of a SwComponentPrototype.

######### FOREIGN-REFERENCE 类型引用

########## 1. RteModeSchtblMapSwcPortRef

- **UUID**: `5a8ddca7-c77e-4fba-a284-c0d65f31d865`
- **引用名**: `RteModeSchtblMapSwcPortRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [1..1]
- **目标类型**: P-PORT-PROTOTYPE
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Reference to the PPortPrototype of a SwComponentPrototype.

##### 16. RteModeSchtblMapBsw

**容器属性**:

- **UUID**: `3cf22fc0-2a6e-4e1d-8657-f8d5992e3e3c`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `RteModeSchtblMapBsw`
- **多重性**: [0..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

Specifies an instance of a ModeDeclarationGroupPrototype of a Bsw-Module.

###### 引用关系

此容器包含 **2** 个引用：

####### REFERENCE 类型引用

######## 1. RteModeSchtblMapBswInstanceRef

- **UUID**: `6cdfb5dd-62bb-407b-b4a6-b4a299184c95`
- **引用名**: `RteModeSchtblMapBswInstanceRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `RteBswModuleInstance`
- **完整路径**: `/AUTOSAR/EcucDefs/Rte/RteBswModuleInstance`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Reference to an instance specification of a Bsw-Module.

####### FOREIGN-REFERENCE 类型引用

######## 1. RteModeSchtblMapBswProvidedModeGroupRef

- **UUID**: `eccf0465-ceee-4510-9910-fbb16567cfb5`
- **引用名**: `RteModeSchtblMapBswProvidedModeGroupRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [1..1]
- **目标类型**: MODE-DECLARATION-GROUP-PROTOTYPE
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Reference to an instance of a ModeDeclarationGroupPrototype of a Bsw-Module.

##### 17. RteModeSchtblMapSwc

**容器属性**:

- **UUID**: `863541a7-8054-4564-b205-aa7cfeeaa1d1`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `RteModeSchtblMapSwc`
- **多重性**: [0..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

Specifies an instance of a ModeDeclarationGroupPrototype of a SwComponentPrototype.

###### 引用关系

此容器包含 **2** 个引用：

####### REFERENCE 类型引用

######## 1. RteModeSchtblMapSwcInstanceRef

- **UUID**: `1ff62917-48b2-4ed7-9302-e18d154edab3`
- **引用名**: `RteModeSchtblMapSwcInstanceRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `RteSwComponentInstance`
- **完整路径**: `/AUTOSAR/EcucDefs/Rte/RteSwComponentInstance`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Reference to an instance specification of a SwComponentPrototype.

####### FOREIGN-REFERENCE 类型引用

######## 1. RteModeSchtblMapSwcPortRef

- **UUID**: `5a8ddca7-c77e-4fba-a284-c0d65f31d865`
- **引用名**: `RteModeSchtblMapSwcPortRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [1..1]
- **目标类型**: P-PORT-PROTOTYPE
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Reference to the PPortPrototype of a SwComponentPrototype.

##### 18. RteUsedOsActivation

**容器属性**:

- **UUID**: `86502546-eb26-4bc5-aa81-e6f2125c1db7`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `RteUsedOsActivation`
- **多重性**: [0..infinite]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

Attributes used in the activation of OsTasks and Runnable Entities.

###### 参数配置

此容器包含 **2** 个参数：

####### FLOAT 类型参数

######## 1. RteExpectedActivationOffset

- **UUID**: `75b4f494-95e0-4781-b58e-4d0d701ac9a9`
- **参数名**: `RteExpectedActivationOffset`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Activation offset.

######## 2. RteExpectedTickDuration

- **UUID**: `3e6976a0-d393-481e-bb0b-2af417f9d169`
- **参数名**: `RteExpectedTickDuration`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: The expected tick duration which shall be configured to drive the OsScheduleTables or OsAlarm.

###### 引用关系

此容器包含 **3** 个引用：

####### REFERENCE 类型引用

######## 1. RteActivationOsAlarmRef

- **UUID**: `b87517f3-82ce-472f-91ac-067aa222ce4b`
- **引用名**: `RteActivationOsAlarmRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `OsAlarm`
- **完整路径**: `/AUTOSAR/EcucDefs/Os/OsAlarm`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Reference to an OsAlarm.

######## 2. RteActivationOsSchTblRef

- **UUID**: `6b2fdc09-3aa5-440b-a111-3d438f669466`
- **引用名**: `RteActivationOsSchTblRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `OsScheduleTable`
- **完整路径**: `/AUTOSAR/EcucDefs/Os/OsScheduleTable`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Reference to an OsScheduleTable.

######## 3. RteActivationOsTaskRef

- **UUID**: `d3547a38-b37f-41dc-b93b-b9780e41034d`
- **引用名**: `RteActivationOsTaskRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `OsTask`
- **完整路径**: `/AUTOSAR/EcucDefs/Os/OsTask`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Reference to an OsTask.

##### 19. RtePostBuildVariantConfiguration

**容器属性**:

- **UUID**: `23865f74-005b-45ca-b85e-57f1c359d43d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `RtePostBuildVariantConfiguration`
- **多重性**: [0..1]
- **构建后可变**: false
- **多配置容器**: true

**容器描述**:

Specifies the PostbuildVariantSets for each of the PostBuild configurations of the RTE.

###### 引用关系

此容器包含 **1** 个引用：

####### FOREIGN-REFERENCE 类型引用

######## 1. RtePostBuildUsedPredefinedVariant

- **UUID**: `1949da50-e452-494d-aab7-1201ceaa2a5e`
- **引用名**: `RtePostBuildUsedPredefinedVariant`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [1..infinite]
- **目标类型**: PREDEFINED-VARIANT
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Reference to the PredefinedVariant element which defines the values for PostBuildVariationCriterion elements.

##### 20. RteSwComponentInstance

**容器属性**:

- **UUID**: `d97803f2-539d-470a-bf56-ea50b6097b47`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `RteSwComponentInstance`
- **多重性**: [0..infinite]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

Representation of one SwComponentPrototype located on the to be configured ECU. All subcontainer configuration aspects are in relation to this SwComponentPrototype.

###### 引用关系

此容器包含 **1** 个引用：

####### FOREIGN-REFERENCE 类型引用

######## 1. RteSoftwareComponentInstanceRef

- **UUID**: `43bdbda5-042b-4226-83ba-f71d72c8af87`
- **引用名**: `RteSoftwareComponentInstanceRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [0..1]
- **目标类型**: SW-COMPONENT-PROTOTYPE
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Reference to a SwComponentPrototype.

###### 配置容器

本模块包含 **6** 个配置容器：

####### 1. RteEventToTaskMapping

**容器属性**:

- **UUID**: `266951b3-2154-4afa-b67b-14b75e1e8176`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `RteEventToTaskMapping`
- **多重性**: [0..infinite]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

Maps a RunnableEntity onto one OsTask based on the activating RTEEvent.

######## 参数配置

此容器包含 **6** 个参数：

######### INTEGER 类型参数

########## 1. RtePositionInTask

- **UUID**: `587a355b-6fd9-4f48-8fd4-523a8a0a4228`
- **参数名**: `RtePositionInTask`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Each RunnableEntity mapped to an OsTask has a specific position within the task execution.

########## 2. RteServerQueueLength

- **UUID**: `e6463e86-8a86-4f34-a76c-425c1a54f6a0`
- **参数名**: `RteServerQueueLength`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..65535]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Specifies the length of the queue for the server call serialization. This value overwrites the queueLength specified at the ServerComSpec.

######### BOOLEAN 类型参数

########## 1. RteImmediateRestart

- **UUID**: `63c6a8a1-e40b-4cf1-90cb-48b6bbe31f19`
- **参数名**: `RteImmediateRestart`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: When RteImmediateRestart is set to true the RunnableEntitiy shall be immediately re-started after termination if it was activated by this RTEEvent while it was already started.

######### FLOAT 类型参数

########## 1. RteActivationOffset

- **UUID**: `5e095bdd-05a2-4ad2-9ca4-b98bc9c173eb`
- **参数名**: `RteActivationOffset`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **取值范围**: [0..]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Activation offset.

######### ENUMERATION 类型参数

########## 1. RteOsSchedulePoint

- **UUID**: `55114fed-1208-41ea-961e-9708539a72cc`
- **参数名**: `RteOsSchedulePoint`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `NONE`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CONDITIONAL`
  - `NONE`
  - `UNCONDITIONAL`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Introduce a schedule point by explicitly calling Os Schedule service after the execution of the ExecutableEntity.  The Rte generator is allowed to optimize several consecutive calls to Os schedule into one single call if the ExecutableEntity executions in between have been skipped.

########## 2. RteCyclicTriggerImplementation

- **UUID**: `5ce396fc-5f2c-4bc3-b146-9bb183997655`
- **参数名**: `RteCyclicTriggerImplementation`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `Auto`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `Auto`
  - `None`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: If set to 'Auto' the RTE generator automatically creates the necessary OS alarm to realize the cyclic trigger with the configured activation offset. 
If set to 'None' the trigger is not implemented by the RTE generator. It has to be implemented by the user either by configuring an appropriate OS alarm or an OS schedule table. 
The OS task and optional the OS event for that trigger can be found in the generated RTE report.

######## 引用关系

此容器包含 **8** 个引用：

######### REFERENCE 类型引用

########## 1. RteMappedToTaskRef

- **UUID**: `3dd46183-d38e-4454-9cb0-d4ff0d60f252`
- **引用名**: `RteMappedToTaskRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `OsTask`
- **完整路径**: `/AUTOSAR/EcucDefs/Os/OsTask`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Reference to the OsTask the RunnableEntity activated by the RteEventRef is mapped to.

########## 2. RteUsedOsAlarmRef

- **UUID**: `106ae078-f43d-493f-8e16-fc0ccd79aebc`
- **引用名**: `RteUsedOsAlarmRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `OsAlarm`
- **完整路径**: `/AUTOSAR/EcucDefs/Os/OsAlarm`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: If an OsAlarm is used to activate the OsTask this RteEvent is mapped to it shall be referenced here.

########## 3. RteUsedOsEventRef

- **UUID**: `968e38c9-211e-4003-95ce-cff31aa31ef8`
- **引用名**: `RteUsedOsEventRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `OsEvent`
- **完整路径**: `/AUTOSAR/EcucDefs/Os/OsEvent`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: If an OsEvent is used to activate the OsTask this RteEvent is mapped to it shall be referenced here.

########## 4. RteUsedOsSchTblExpiryPointRef

- **UUID**: `5baa158b-67a7-4bb2-8563-9371a41e3e19`
- **引用名**: `RteUsedOsSchTblExpiryPointRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `OsScheduleTableExpiryPoint`
- **完整路径**: `/AUTOSAR/EcucDefs/Os/OsScheduleTable/OsScheduleTableExpiryPoint`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: If an OsScheduleTableExpiryPoint is used to activate the OsTask this RteEvent is mapped to it shall be referenced here.

########## 5. RteVirtuallyMappedToTaskRef

- **UUID**: `f1f7afe7-cdef-41c8-a471-bf90b6c4bc3f`
- **引用名**: `RteVirtuallyMappedToTaskRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `OsTask`
- **完整路径**: `/AUTOSAR/EcucDefs/Os/OsTask`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Optional reference to an OsTask where the activation of this RteEvent shall be evaluated. The actual execution of the Runnable Entity shall happen in the OsTask referenced by RteMappedToTaskRef.

######### FOREIGN-REFERENCE 类型引用

########## 1. RteEventRef

- **UUID**: `446bbd14-efca-4b9b-ab76-c4b5e948662f`
- **引用名**: `RteEventRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [1..1]
- **目标类型**: RTE-EVENT
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Reference to the description of the RTEEvent which is pointing to the RunnableEntity being mapped. This allows a fine grained mapping of RunnableEntites based on the activating RTEEvent.

########## 2. RteRipsFillRoutineRef

- **UUID**: `d6431ceb-440e-4b04-abb9-807a27b44823`
- **引用名**: `RteRipsFillRoutineRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [0..infinite]
- **目标类型**: CONTAINER
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Reference to a Buffer-Fill Routine implemented by an RTE Implementation Plug-In.

########## 3. RteRipsFlushRoutineRef

- **UUID**: `08306740-b049-4e5f-a350-b07980028320`
- **引用名**: `RteRipsFlushRoutineRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [0..infinite]
- **目标类型**: CONTAINER
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Reference to a Buffer-Flush Routine implemented by an RTE Implementation Plug-In.

####### 2. RteExclusiveAreaImplementation

**容器属性**:

- **UUID**: `b7bf58ec-783c-4604-b847-3175f6e5ec83`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `RteExclusiveAreaImplementation`
- **多重性**: [0..infinite]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

Specifies the implementation to be used for the data consistency of this ExclusiveArea.

######## 参数配置

此容器包含 **2** 个参数：

######### BOOLEAN 类型参数

########## 1. RteExclusiveAreaOptimization

- **UUID**: `8e689104-c948-470b-a83f-bf734596e15d`
- **参数名**: `RteExclusiveAreaOptimization`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `true`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: If set to true, the RTE generator tries to optimize the implementation (e.g. disable unnecessary interrupt lock)  of the exclusive area if possible.
If set to false, the RTE generator does not optimize the exclusive area.

######### ENUMERATION 类型参数

########## 1. RteExclusiveAreaImplMechanism

- **UUID**: `88f576dd-cd49-406b-ad51-33a3aa72f09c`
- **参数名**: `RteExclusiveAreaImplMechanism`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `OS_INTERRUPT_BLOCKING`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `ALL_INTERRUPT_BLOCKING` (来源: AUTOSAR_ECUC)
  - `COOPERATIVE_RUNNABLE_PLACEMENT` (来源: AUTOSAR_ECUC)
  - `OS_INTERRUPT_BLOCKING` (来源: AUTOSAR_ECUC)
  - `OS_RESOURCE` (来源: AUTOSAR_ECUC)
  - `NONE` (来源: Vector Informatik)
  - `CUSTOM` (来源: Vector Informatik)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: To be used implementation mechanism for the specified ExclusiveArea.

######## 引用关系

此容器包含 **2** 个引用：

######### REFERENCE 类型引用

########## 1. RteExclusiveAreaOsResourceRef

- **UUID**: `a04bb921-9da7-4bea-aa2c-76b95ef106f6`
- **引用名**: `RteExclusiveAreaOsResourceRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `OsResource`
- **完整路径**: `/AUTOSAR/EcucDefs/Os/OsResource`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Optional reference to an OsResource in case RteExclusiveAreaImplMechanism is configured to OS_RESOURCE for this ExclusiveArea.

######### FOREIGN-REFERENCE 类型引用

########## 1. RteExclusiveAreaRef

- **UUID**: `2986d534-4c53-4f1e-86ec-4ccb1fa1ee13`
- **引用名**: `RteExclusiveAreaRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [1..1]
- **目标类型**: EXCLUSIVE-AREA
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Reference to the ExclusiveArea.

####### 3. RteExternalTriggerConfig

**容器属性**:

- **UUID**: `3ec70857-d820-4a7d-88bd-80e0691000dc`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `RteExternalTriggerConfig`
- **多重性**: [0..infinite]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

Defines the configuration of External Trigger Event Communication for Software Components

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. RteTriggerSourceQueueLength

- **UUID**: `2aee9516-e602-4176-9807-953a63b63e77`
- **参数名**: `RteTriggerSourceQueueLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Length of trigger queue on the trigger source side.

######## 引用关系

此容器包含 **1** 个引用：

######### INSTANCE-REFERENCE 类型引用

########## 1. RteSwcTriggerSourceRef

- **UUID**: `52a29a46-afa7-4bbf-b58d-2ab1af834f16`
- **引用名**: `RteSwcTriggerSourceRef`
- **引用类型**: INSTANCE-REFERENCE
- **多重性**: [1..1]
- **目标类型**: TRIGGER
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Reference to a Trigger instance in the pPortPrototype of the related component instance.

####### 4. RteInternalTriggerConfig

**容器属性**:

- **UUID**: `8d6f23a9-6bf2-4f3a-bc11-f27f2808224c`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `RteInternalTriggerConfig`
- **多重性**: [0..infinite]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

Defines the configuration of Inter Runnable Triggering for Software Components

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. RteTriggerSourceQueueLength

- **UUID**: `52b45372-1fca-45bc-8040-50cbcc9cc480`
- **参数名**: `RteTriggerSourceQueueLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Length of trigger queue on the trigger source side.

######## 引用关系

此容器包含 **1** 个引用：

######### FOREIGN-REFERENCE 类型引用

########## 1. RteSwcTriggerSourceRef

- **UUID**: `d13de5b9-5a28-4a89-a3e6-f4568d78548a`
- **引用名**: `RteSwcTriggerSourceRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [1..1]
- **目标类型**: INTERNAL-TRIGGERING-POINT
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Reference to an InternalTriggeringPoint of the related component instance.

####### 5. RteModeMachineInstanceConfig

**容器属性**:

- **UUID**: `46882ca6-9d5a-4509-8116-364809d5a1a1`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `RteModeMachineInstanceConfig`
- **多重性**: [0..infinite]
- **构建后可变**: false

**容器描述**:

Defines the configuration of RTE assigned (<b>SWS_Rte_07533)</b> mode machine instances.

######## 引用关系

此容器包含 **1** 个引用：

######### INSTANCE-REFERENCE 类型引用

########## 1. RteSwcModeManagerRef

- **UUID**: `6bd7e1cc-d89d-4b4c-9f03-da0d61171310`
- **引用名**: `RteSwcModeManagerRef`
- **引用类型**: INSTANCE-REFERENCE
- **多重性**: [1..1]
- **目标类型**: MODE-DECLARATION-GROUP-PROTOTYPE
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Reference to a ModeDeclarationGroupPrototype instance in the provided PortPrototype (AbstractProvidedPortPrototype) of the related component instance.

####### 6. RteNvRamAllocation

**容器属性**:

- **UUID**: `417eee66-cbed-4c8a-819e-642611a893c8`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `RteNvRamAllocation`
- **多重性**: [0..infinite]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

Specifies the relationship between the AtomicSwComponentType's NVRAMMapping / NVRAM needs and the NvM module configuration.

######## 参数配置

此容器包含 **2** 个参数：

######### LINKER-SYMBOL 类型参数

########## 1. RteNvmRamBlockLocationSymbol

- **UUID**: `4e3a6bb0-8154-49b3-a9b0-9f730bfa061e`
- **参数名**: `RteNvmRamBlockLocationSymbol`
- **数据类型**: LINKER-SYMBOL
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This is the name of the linker object name where the NVRam Block will be mirrored by the Nvm.

########## 2. RteNvmRomBlockLocationSymbol

- **UUID**: `8b2c5764-66bd-424e-b1ba-a759a7e89499`
- **参数名**: `RteNvmRomBlockLocationSymbol`
- **数据类型**: LINKER-SYMBOL
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This is the name of the linker object name where the NVRom Block will be accessed by the Nvm.

######## 引用关系

此容器包含 **3** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. RteNvmBlockRef

- **UUID**: `dbd40f45-42b7-4e4d-88f2-36c71bbc9738`
- **引用名**: `RteNvmBlockRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `NvMBlockDescriptor`
- **完整路径**: `/AUTOSAR/EcucDefs/NvM/NvMBlockDescriptor`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Reference to the used NvM block for storage of the NVRAMMapping information.

######### FOREIGN-REFERENCE 类型引用

########## 1. RteSwNvRamMappingRef

- **UUID**: `28b15482-a508-4f58-9841-554d491e4b23`
- **引用名**: `RteSwNvRamMappingRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [0..1]
- **目标类型**: SWC-SERVICE-DEPENDENCY
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Reference to the SwServiceDependency which is used to specify the NvBlockNeeds.


If this reference exists RteSwNvBlockRamMappingRef must not exists (XOR)

########## 2. RteSwNvBlockDescriptorRef

- **UUID**: `e9933b46-16af-4fef-bb54-a432d9475de7`
- **引用名**: `RteSwNvBlockDescriptorRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [0..1]
- **目标类型**: NV-BLOCK-DESCRIPTOR
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Reference to the NvBlockDescriptor in case the RTE needs to call the NvM directly (e.g. for the supportDirtyFlag feature).

##### 21. RteEventToTaskMapping

**容器属性**:

- **UUID**: `266951b3-2154-4afa-b67b-14b75e1e8176`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `RteEventToTaskMapping`
- **多重性**: [0..infinite]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

Maps a RunnableEntity onto one OsTask based on the activating RTEEvent.

###### 参数配置

此容器包含 **6** 个参数：

####### INTEGER 类型参数

######## 1. RtePositionInTask

- **UUID**: `587a355b-6fd9-4f48-8fd4-523a8a0a4228`
- **参数名**: `RtePositionInTask`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Each RunnableEntity mapped to an OsTask has a specific position within the task execution.

######## 2. RteServerQueueLength

- **UUID**: `e6463e86-8a86-4f34-a76c-425c1a54f6a0`
- **参数名**: `RteServerQueueLength`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..65535]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Specifies the length of the queue for the server call serialization. This value overwrites the queueLength specified at the ServerComSpec.

####### BOOLEAN 类型参数

######## 1. RteImmediateRestart

- **UUID**: `63c6a8a1-e40b-4cf1-90cb-48b6bbe31f19`
- **参数名**: `RteImmediateRestart`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: When RteImmediateRestart is set to true the RunnableEntitiy shall be immediately re-started after termination if it was activated by this RTEEvent while it was already started.

####### FLOAT 类型参数

######## 1. RteActivationOffset

- **UUID**: `5e095bdd-05a2-4ad2-9ca4-b98bc9c173eb`
- **参数名**: `RteActivationOffset`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **取值范围**: [0..]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Activation offset.

####### ENUMERATION 类型参数

######## 1. RteOsSchedulePoint

- **UUID**: `55114fed-1208-41ea-961e-9708539a72cc`
- **参数名**: `RteOsSchedulePoint`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `NONE`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CONDITIONAL`
  - `NONE`
  - `UNCONDITIONAL`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Introduce a schedule point by explicitly calling Os Schedule service after the execution of the ExecutableEntity.  The Rte generator is allowed to optimize several consecutive calls to Os schedule into one single call if the ExecutableEntity executions in between have been skipped.

######## 2. RteCyclicTriggerImplementation

- **UUID**: `5ce396fc-5f2c-4bc3-b146-9bb183997655`
- **参数名**: `RteCyclicTriggerImplementation`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `Auto`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `Auto`
  - `None`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: If set to 'Auto' the RTE generator automatically creates the necessary OS alarm to realize the cyclic trigger with the configured activation offset. 
If set to 'None' the trigger is not implemented by the RTE generator. It has to be implemented by the user either by configuring an appropriate OS alarm or an OS schedule table. 
The OS task and optional the OS event for that trigger can be found in the generated RTE report.

###### 引用关系

此容器包含 **8** 个引用：

####### REFERENCE 类型引用

######## 1. RteMappedToTaskRef

- **UUID**: `3dd46183-d38e-4454-9cb0-d4ff0d60f252`
- **引用名**: `RteMappedToTaskRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `OsTask`
- **完整路径**: `/AUTOSAR/EcucDefs/Os/OsTask`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Reference to the OsTask the RunnableEntity activated by the RteEventRef is mapped to.

######## 2. RteUsedOsAlarmRef

- **UUID**: `106ae078-f43d-493f-8e16-fc0ccd79aebc`
- **引用名**: `RteUsedOsAlarmRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `OsAlarm`
- **完整路径**: `/AUTOSAR/EcucDefs/Os/OsAlarm`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: If an OsAlarm is used to activate the OsTask this RteEvent is mapped to it shall be referenced here.

######## 3. RteUsedOsEventRef

- **UUID**: `968e38c9-211e-4003-95ce-cff31aa31ef8`
- **引用名**: `RteUsedOsEventRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `OsEvent`
- **完整路径**: `/AUTOSAR/EcucDefs/Os/OsEvent`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: If an OsEvent is used to activate the OsTask this RteEvent is mapped to it shall be referenced here.

######## 4. RteUsedOsSchTblExpiryPointRef

- **UUID**: `5baa158b-67a7-4bb2-8563-9371a41e3e19`
- **引用名**: `RteUsedOsSchTblExpiryPointRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `OsScheduleTableExpiryPoint`
- **完整路径**: `/AUTOSAR/EcucDefs/Os/OsScheduleTable/OsScheduleTableExpiryPoint`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: If an OsScheduleTableExpiryPoint is used to activate the OsTask this RteEvent is mapped to it shall be referenced here.

######## 5. RteVirtuallyMappedToTaskRef

- **UUID**: `f1f7afe7-cdef-41c8-a471-bf90b6c4bc3f`
- **引用名**: `RteVirtuallyMappedToTaskRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `OsTask`
- **完整路径**: `/AUTOSAR/EcucDefs/Os/OsTask`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Optional reference to an OsTask where the activation of this RteEvent shall be evaluated. The actual execution of the Runnable Entity shall happen in the OsTask referenced by RteMappedToTaskRef.

####### FOREIGN-REFERENCE 类型引用

######## 1. RteEventRef

- **UUID**: `446bbd14-efca-4b9b-ab76-c4b5e948662f`
- **引用名**: `RteEventRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [1..1]
- **目标类型**: RTE-EVENT
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Reference to the description of the RTEEvent which is pointing to the RunnableEntity being mapped. This allows a fine grained mapping of RunnableEntites based on the activating RTEEvent.

######## 2. RteRipsFillRoutineRef

- **UUID**: `d6431ceb-440e-4b04-abb9-807a27b44823`
- **引用名**: `RteRipsFillRoutineRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [0..infinite]
- **目标类型**: CONTAINER
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Reference to a Buffer-Fill Routine implemented by an RTE Implementation Plug-In.

######## 3. RteRipsFlushRoutineRef

- **UUID**: `08306740-b049-4e5f-a350-b07980028320`
- **引用名**: `RteRipsFlushRoutineRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [0..infinite]
- **目标类型**: CONTAINER
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Reference to a Buffer-Flush Routine implemented by an RTE Implementation Plug-In.

##### 22. RteExclusiveAreaImplementation

**容器属性**:

- **UUID**: `b7bf58ec-783c-4604-b847-3175f6e5ec83`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `RteExclusiveAreaImplementation`
- **多重性**: [0..infinite]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

Specifies the implementation to be used for the data consistency of this ExclusiveArea.

###### 参数配置

此容器包含 **2** 个参数：

####### BOOLEAN 类型参数

######## 1. RteExclusiveAreaOptimization

- **UUID**: `8e689104-c948-470b-a83f-bf734596e15d`
- **参数名**: `RteExclusiveAreaOptimization`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `true`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: If set to true, the RTE generator tries to optimize the implementation (e.g. disable unnecessary interrupt lock)  of the exclusive area if possible.
If set to false, the RTE generator does not optimize the exclusive area.

####### ENUMERATION 类型参数

######## 1. RteExclusiveAreaImplMechanism

- **UUID**: `88f576dd-cd49-406b-ad51-33a3aa72f09c`
- **参数名**: `RteExclusiveAreaImplMechanism`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `OS_INTERRUPT_BLOCKING`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `ALL_INTERRUPT_BLOCKING` (来源: AUTOSAR_ECUC)
  - `COOPERATIVE_RUNNABLE_PLACEMENT` (来源: AUTOSAR_ECUC)
  - `OS_INTERRUPT_BLOCKING` (来源: AUTOSAR_ECUC)
  - `OS_RESOURCE` (来源: AUTOSAR_ECUC)
  - `NONE` (来源: Vector Informatik)
  - `CUSTOM` (来源: Vector Informatik)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: To be used implementation mechanism for the specified ExclusiveArea.

###### 引用关系

此容器包含 **2** 个引用：

####### REFERENCE 类型引用

######## 1. RteExclusiveAreaOsResourceRef

- **UUID**: `a04bb921-9da7-4bea-aa2c-76b95ef106f6`
- **引用名**: `RteExclusiveAreaOsResourceRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `OsResource`
- **完整路径**: `/AUTOSAR/EcucDefs/Os/OsResource`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Optional reference to an OsResource in case RteExclusiveAreaImplMechanism is configured to OS_RESOURCE for this ExclusiveArea.

####### FOREIGN-REFERENCE 类型引用

######## 1. RteExclusiveAreaRef

- **UUID**: `2986d534-4c53-4f1e-86ec-4ccb1fa1ee13`
- **引用名**: `RteExclusiveAreaRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [1..1]
- **目标类型**: EXCLUSIVE-AREA
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Reference to the ExclusiveArea.

##### 23. RteExternalTriggerConfig

**容器属性**:

- **UUID**: `3ec70857-d820-4a7d-88bd-80e0691000dc`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `RteExternalTriggerConfig`
- **多重性**: [0..infinite]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

Defines the configuration of External Trigger Event Communication for Software Components

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. RteTriggerSourceQueueLength

- **UUID**: `2aee9516-e602-4176-9807-953a63b63e77`
- **参数名**: `RteTriggerSourceQueueLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Length of trigger queue on the trigger source side.

###### 引用关系

此容器包含 **1** 个引用：

####### INSTANCE-REFERENCE 类型引用

######## 1. RteSwcTriggerSourceRef

- **UUID**: `52a29a46-afa7-4bbf-b58d-2ab1af834f16`
- **引用名**: `RteSwcTriggerSourceRef`
- **引用类型**: INSTANCE-REFERENCE
- **多重性**: [1..1]
- **目标类型**: TRIGGER
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Reference to a Trigger instance in the pPortPrototype of the related component instance.

##### 24. RteInternalTriggerConfig

**容器属性**:

- **UUID**: `8d6f23a9-6bf2-4f3a-bc11-f27f2808224c`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `RteInternalTriggerConfig`
- **多重性**: [0..infinite]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

Defines the configuration of Inter Runnable Triggering for Software Components

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. RteTriggerSourceQueueLength

- **UUID**: `52b45372-1fca-45bc-8040-50cbcc9cc480`
- **参数名**: `RteTriggerSourceQueueLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Length of trigger queue on the trigger source side.

###### 引用关系

此容器包含 **1** 个引用：

####### FOREIGN-REFERENCE 类型引用

######## 1. RteSwcTriggerSourceRef

- **UUID**: `d13de5b9-5a28-4a89-a3e6-f4568d78548a`
- **引用名**: `RteSwcTriggerSourceRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [1..1]
- **目标类型**: INTERNAL-TRIGGERING-POINT
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Reference to an InternalTriggeringPoint of the related component instance.

##### 25. RteModeMachineInstanceConfig

**容器属性**:

- **UUID**: `46882ca6-9d5a-4509-8116-364809d5a1a1`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `RteModeMachineInstanceConfig`
- **多重性**: [0..infinite]
- **构建后可变**: false

**容器描述**:

Defines the configuration of RTE assigned (<b>SWS_Rte_07533)</b> mode machine instances.

###### 引用关系

此容器包含 **1** 个引用：

####### INSTANCE-REFERENCE 类型引用

######## 1. RteSwcModeManagerRef

- **UUID**: `6bd7e1cc-d89d-4b4c-9f03-da0d61171310`
- **引用名**: `RteSwcModeManagerRef`
- **引用类型**: INSTANCE-REFERENCE
- **多重性**: [1..1]
- **目标类型**: MODE-DECLARATION-GROUP-PROTOTYPE
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Reference to a ModeDeclarationGroupPrototype instance in the provided PortPrototype (AbstractProvidedPortPrototype) of the related component instance.

##### 26. RteNvRamAllocation

**容器属性**:

- **UUID**: `417eee66-cbed-4c8a-819e-642611a893c8`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `RteNvRamAllocation`
- **多重性**: [0..infinite]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

Specifies the relationship between the AtomicSwComponentType's NVRAMMapping / NVRAM needs and the NvM module configuration.

###### 参数配置

此容器包含 **2** 个参数：

####### LINKER-SYMBOL 类型参数

######## 1. RteNvmRamBlockLocationSymbol

- **UUID**: `4e3a6bb0-8154-49b3-a9b0-9f730bfa061e`
- **参数名**: `RteNvmRamBlockLocationSymbol`
- **数据类型**: LINKER-SYMBOL
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This is the name of the linker object name where the NVRam Block will be mirrored by the Nvm.

######## 2. RteNvmRomBlockLocationSymbol

- **UUID**: `8b2c5764-66bd-424e-b1ba-a759a7e89499`
- **参数名**: `RteNvmRomBlockLocationSymbol`
- **数据类型**: LINKER-SYMBOL
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This is the name of the linker object name where the NVRom Block will be accessed by the Nvm.

###### 引用关系

此容器包含 **3** 个引用：

####### SYMBOLIC-NAME-REFERENCE 类型引用

######## 1. RteNvmBlockRef

- **UUID**: `dbd40f45-42b7-4e4d-88f2-36c71bbc9738`
- **引用名**: `RteNvmBlockRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `NvMBlockDescriptor`
- **完整路径**: `/AUTOSAR/EcucDefs/NvM/NvMBlockDescriptor`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Reference to the used NvM block for storage of the NVRAMMapping information.

####### FOREIGN-REFERENCE 类型引用

######## 1. RteSwNvRamMappingRef

- **UUID**: `28b15482-a508-4f58-9841-554d491e4b23`
- **引用名**: `RteSwNvRamMappingRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [0..1]
- **目标类型**: SWC-SERVICE-DEPENDENCY
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Reference to the SwServiceDependency which is used to specify the NvBlockNeeds.


If this reference exists RteSwNvBlockRamMappingRef must not exists (XOR)

######## 2. RteSwNvBlockDescriptorRef

- **UUID**: `e9933b46-16af-4fef-bb54-a432d9475de7`
- **引用名**: `RteSwNvBlockDescriptorRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [0..1]
- **目标类型**: NV-BLOCK-DESCRIPTOR
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Reference to the NvBlockDescriptor in case the RTE needs to call the NvM directly (e.g. for the supportDirtyFlag feature).

##### 27. RteSwComponentType

**容器属性**:

- **UUID**: `45a283f3-0f1c-4355-b12e-7574ddfb1b75`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `RteSwComponentType`
- **多重性**: [0..infinite]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

Representation of one SwComponentType for the base of all configuration parameter which are affecting the whole type and not a specific instance.

###### 参数配置

此容器包含 **1** 个参数：

####### BOOLEAN 类型参数

######## 1. RteSwcMemMapGeneration

- **UUID**: `76e3fd3c-9534-4cc3-9d6d-a0b453cdca6c`
- **参数名**: `RteSwcMemMapGeneration`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `true`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Enables or disables the generation of MemMap files for the specified Software Component by the RTE generator. Default is enabled when the generation is not done by the MemMap generator.

###### 引用关系

此容器包含 **2** 个引用：

####### FOREIGN-REFERENCE 类型引用

######## 1. RteComponentTypeRef

- **UUID**: `999c9774-291b-4dc1-9d1e-67b1a166ee05`
- **引用名**: `RteComponentTypeRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [1..1]
- **目标类型**: SW-COMPONENT-TYPE
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Reference to either AtomicSwComponentType or ParameterSwComponentType.

######## 2. RteImplementationRef

- **UUID**: `30254c70-cd57-4c5d-ad56-9ebad0ae83e0`
- **引用名**: `RteImplementationRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [0..1]
- **目标类型**: SWC-IMPLEMENTATION
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: The Implementation which shall be assiged to the SwComponentType.

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. RteComponentTypeCalibration

**容器属性**:

- **UUID**: `80e0186e-1d35-4d48-9818-984d6fc19bc2`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `RteComponentTypeCalibration`
- **多重性**: [0..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

Specifies for each ParameterSwComponentType or AtomicSwComponentType whether calibration is enabled.

######## 参数配置

此容器包含 **1** 个参数：

######### BOOLEAN 类型参数

########## 1. RteCalibrationSupportEnabled

- **UUID**: `68be19dc-ac4e-4c52-a58a-2d915fa9599d`
- **参数名**: `RteCalibrationSupportEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Enables calibration support for the specified ParameterSwComponentType or AtomicSwComponentType.

######## 引用关系

此容器包含 **1** 个引用：

######### FOREIGN-REFERENCE 类型引用

########## 1. RteCalibrationSwAddrMethodRef

- **UUID**: `3de2ed6d-1125-4ed4-885f-e40618ac8ff8`
- **引用名**: `RteCalibrationSwAddrMethodRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [0..infinite]
- **目标类型**: SW-ADDR-METHOD
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Reference to the SwAddrMethod for which software calibration support shall be enabled.

##### 28. RteComponentTypeCalibration

**容器属性**:

- **UUID**: `80e0186e-1d35-4d48-9818-984d6fc19bc2`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `RteComponentTypeCalibration`
- **多重性**: [0..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

Specifies for each ParameterSwComponentType or AtomicSwComponentType whether calibration is enabled.

###### 参数配置

此容器包含 **1** 个参数：

####### BOOLEAN 类型参数

######## 1. RteCalibrationSupportEnabled

- **UUID**: `68be19dc-ac4e-4c52-a58a-2d915fa9599d`
- **参数名**: `RteCalibrationSupportEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Enables calibration support for the specified ParameterSwComponentType or AtomicSwComponentType.

###### 引用关系

此容器包含 **1** 个引用：

####### FOREIGN-REFERENCE 类型引用

######## 1. RteCalibrationSwAddrMethodRef

- **UUID**: `3de2ed6d-1125-4ed4-885f-e40618ac8ff8`
- **引用名**: `RteCalibrationSwAddrMethodRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [0..infinite]
- **目标类型**: SW-ADDR-METHOD
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Reference to the SwAddrMethod for which software calibration support shall be enabled.

##### 29. RteInitializationRunnableBatch

**容器属性**:

- **UUID**: `adae44e9-3432-46a8-b7e5-7aeaaafc8350`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `RteInitializationRunnableBatch`
- **多重性**: [0..infinite]
- **构建后可变**: false

**容器描述**:

Presence of at least one RteInitializationRunnableBatch enables the Rte_StartTiming API.

### 2. RteCalculation

#### 基本信息

- **UUID**: `f7d30f61-2d2c-4467-84c1-c4f4a3d25e66`
- **模块名称**: `RteCalculation`
- **类别**: `VENDOR_SPECIFIC_MODULE_DEFINITION`
- **多重性**: [0..1]
- **支持的变体**:
  - VARIANT-PRE-COMPILE

#### 模块描述

Runtime Environment (RTE) calculation.
Automatically updates the configuration of modules that are used by the RTE generator (COM, LDCOM, NVM, OS) during the calculation phase in DaVinci CFG. 
If this module is part of the configuration: Allows disabling of the automatic calculation phase of the RTE in the generator selection.
The RTE generator then only displays validation messages with solving actions for the update. It might be necessary to regenerate the updated modules afterwards.
If this module is not part of the configuration: Automatic calculation is always done.
It is recommended to always execute the calculation.
However, when only local configuration changes are done, experts can deselect this module for faster generation.
#RuntimeEnvironment
#AUTOSAR

### 3. RteChecks

#### 基本信息

- **UUID**: `2a300105-b6c5-4554-900f-a90ac1f80d85`
- **模块名称**: `RteChecks`
- **类别**: `VENDOR_SPECIFIC_MODULE_DEFINITION`
- **多重性**: [0..1]
- **支持的变体**:
  - VARIANT-PRE-COMPILE

#### 模块描述

Runtime Environment (RTE) extended checks.
Checks the model with additional model consistency checks from the DaVinci Developer Framework.
If this module is part of the configuration: Allows disabling of the checks in the generator selection.
Beware that this may lead to undescriptive error messages and not compilable code.
If this module is not part of the configuration: Checks are always done.
It is recommended to always execute the checks.
However, when only local configuration changes are done, experts can deselect this module for faster generation.
#RuntimeEnvironment
#AUTOSAR

## 📦 包结构

此ARXML文件包含 **1** 个包：

### 1. MICROSAR

- **UUID**: `ff55d029-386d-43a2-b3c2-dfef4c7a5e36`
- **包名称**: `MICROSAR`
- **包含元素数量**: 6

#### 包含的元素

##### ECUC-MODULE-DEF 类型元素

1. **Rte**
2. **RteCalculation**
3. **RteChecks**

##### BSW-IMPLEMENTATION 类型元素

1. **Rte_Impl**

##### ECUC-MODULE-CONFIGURATION-VALUES 类型元素

1. **Rte_Pre**
2. **Rte_Rec**

## ⚡ 实现信息

此ARXML文件包含 **1** 个实现：

### 1. Rte_Impl

- **UUID**: `2fd08783-fe33-4df3-b51a-9cee3a7de75f`
- **实现名称**: `Rte_Impl`
- **编程语言**: C
- **软件版本**: 4.37.00
- **供应商ID**: 30
- **AUTOSAR版本**: 4.03.01
- **代码生成器**: DaVinci Configurator

## ⚙️ 配置信息

此ARXML文件包含 **2** 个配置：

### 1. Rte_Pre

- **UUID**: `5a032c40-ea3c-4e63-86de-394bea4fb3f8`
- **配置名称**: `Rte_Pre`
- **定义引用**: `/MICROSAR/Rte`

### 2. Rte_Rec

- **UUID**: `d54b1551-c732-49b2-96a7-3c4276404127`
- **配置名称**: `Rte_Rec`
- **定义引用**: `/MICROSAR/Rte`
