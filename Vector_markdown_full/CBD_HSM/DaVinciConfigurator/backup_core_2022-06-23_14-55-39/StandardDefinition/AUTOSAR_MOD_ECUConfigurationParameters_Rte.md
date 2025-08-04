# Rte - 完整配置文档

*此文档由ARXML文件自动生成，采用层次化结构展示*

**生成时间**: 2025-06-16 14:51:29

## 📑 目录

- [📄 文件信息](#-文件信息)
- [🔧 模块定义](#-模块定义)
  - [Rte](#rte)
- [📦 包结构](#-包结构)

## 📄 文件信息

### Schema信息
- **Schema位置**: `http://autosar.org/schema/r4.0 AUTOSAR_4-0-3.xsd`
- **命名空间**: `http://autosar.org/schema/r4.0`

## 🔧 模块定义

### 1. Rte

#### 基本信息

- **UUID**: `ECUC:be51fc26-fc0c-4898-93e1-7b96a81df3be`
- **模块名称**: `Rte`
- **多重性**: [0..1]
- **支持的变体**:
  - VARIANT-POST-BUILD
  - VARIANT-PRE-COMPILE

#### 模块描述

Configuration of the Rte (Runtime Environment) module.

#### 版本历史

共有 **1** 个版本记录：

##### 1. 版本 4.2.0

- **发布日期**: 2011-11-09
- **发布者**: AUTOSAR

*此版本无详细变更记录*

#### 配置容器

本模块包含 **25** 个配置容器：

##### 1. RteBswGeneral

**容器属性**:

- **UUID**: `ECUC:666271c7-6518-49d1-bae6-d080da3a6dc0`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `RteBswGeneral`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

General configuration parameters of the Bsw Scheduler section.

###### 参数配置

此容器包含 **2** 个参数：

####### BOOLEAN 类型参数

######## 1. RteSchMVersionInfoApi

- **UUID**: `ECUC:4aad112b-e2d6-42c3-9b24-27f5fe3eb984`
- **参数名**: `RteSchMVersionInfoApi`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enables the generation of the SchM_GetVersionInfo() API.

######## 2. RteUseComShadowSignalApi

- **UUID**: `ECUC:9500f667-77bb-42d5-8796-eb2543901f11`
- **参数名**: `RteUseComShadowSignalApi`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines whether the ComShadowSignalAPIs ((Com_UpdateShadowSignal, Com_InvalidateShadowSignal, Com_ReceiveShadowSignal) are used or not.

##### 2. RteBswModuleInstance

**容器属性**:

- **UUID**: `ECUC:af1402cb-7cce-49b2-9736-e8db66dddd3e`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `RteBswModuleInstance`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

Represents one instance of a Bsw-Module configured on one ECU.

###### 引用关系

此容器包含 **2** 个引用：

####### FOREIGN-REFERENCE 类型引用

######## 1. RteBswImplementationRef

- **UUID**: `ECUC:7da6b61c-3790-4579-bbb8-56f8f3eeff7b`
- **引用名**: `RteBswImplementationRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [1..1]
- **目标类型**: BSW-IMPLEMENTATION
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the BswImplementation for which the Rte /SchM is configured.

######## 2. RteBswModuleConfigurationRef

- **UUID**: `ECUC:7bad62dd-8bbc-4c0b-bf17-da3d29df35c8`
- **引用名**: `RteBswModuleConfigurationRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [0..1]
- **目标类型**: MODULE-CONFIGURATION
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the ECU Configuration Values provided for this BswImplementation.

###### 配置容器

本模块包含 **6** 个配置容器：

####### 1. RteBswEventToTaskMapping

**容器属性**:

- **UUID**: `ECUC:08cf8b6e-658c-4155-b94c-ea8f896edf86`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `RteBswEventToTaskMapping`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

Maps a BswSchedulableEntity onto one OsTask based on the activating BswEvent.

######## 参数配置

此容器包含 **4** 个参数：

######### INTEGER 类型参数

########## 1. RteBswPositionInTask

- **UUID**: `ECUC:340833cb-ccb6-4344-b1d6-2a26c6cd37d8`
- **参数名**: `RteBswPositionInTask`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Each BswSchedulableEntity activation mapped to an OsTask has a specific position within the task execution.

######### BOOLEAN 类型参数

########## 1. RteBswImmediateRestart

- **UUID**: `ECUC:a2949613-66e5-410e-8d2f-342d6f979540`
- **参数名**: `RteBswImmediateRestart`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: When RteBswImmediateRestart is set to true the BswSchedulableEntitiy shall be immediately re-started after termination if it was activated by this BswEvent while it was already started.

######### FLOAT 类型参数

########## 1. RteBswActivationOffset

- **UUID**: `ECUC:401a3169-d17a-4a9a-bbd0-9fd78e30c954`
- **参数名**: `RteBswActivationOffset`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **取值范围**: [0..Inf]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Activation offset in seconds.

######### ENUMERATION 类型参数

########## 1. RteOsSchedulePoint

- **UUID**: `ECUC:10f88432-83be-8e8c-3fff-24665fee711c`
- **参数名**: `RteOsSchedulePoint`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `CONDITIONAL` (来源: AUTOSAR_ECUC)
  - `NONE` (来源: AUTOSAR_ECUC)
  - `UNCONDITIONAL` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Introduce a schedule point by explicitly calling Os Schedule service after the execution of the ExecutableEntity.  The Rte generator is allowed to optimize several consecutive calls to Os schedule into one single call if the ExecutableEntity executions in between have been skipped.

######## 引用关系

此容器包含 **5** 个引用：

######### REFERENCE 类型引用

########## 1. RteBswMappedToTaskRef

- **UUID**: `ECUC:5805eeeb-c5ac-4456-a9a3-4f1c0c6ffa4d`
- **引用名**: `RteBswMappedToTaskRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `OsTask`
- **完整路径**: `/AUTOSAR/EcucDefs/Os/OsTask`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the OsTask the BswSchedulableEntity activated by the RteBswEventRef is mapped to.

########## 2. RteBswUsedOsAlarmRef

- **UUID**: `ECUC:77e1d7a6-f016-4110-a9ca-6f63fd952985`
- **引用名**: `RteBswUsedOsAlarmRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `OsAlarm`
- **完整路径**: `/AUTOSAR/EcucDefs/Os/OsAlarm`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: If an OsAlarm is used to activate the OsTask this BswEvent is mapped to it shall be referenced here.

########## 3. RteBswUsedOsEventRef

- **UUID**: `ECUC:49171fb6-569b-4353-8367-1455283f619c`
- **引用名**: `RteBswUsedOsEventRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `OsEvent`
- **完整路径**: `/AUTOSAR/EcucDefs/Os/OsEvent`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: If an OsEvent is used to activate the OsTask this BswEvent is mapped to it shall be referenced here.

########## 4. RteBswUsedOsSchTblExpiryPointRef

- **UUID**: `ECUC:f8938c8c-d05a-4da3-873c-df1a8e623888`
- **引用名**: `RteBswUsedOsSchTblExpiryPointRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `OsScheduleTableExpiryPoint`
- **完整路径**: `/AUTOSAR/EcucDefs/Os/OsScheduleTable/OsScheduleTableExpiryPoint`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: If an OsScheduleTableExpiryPoint is used to activate the OsTask this BswEvent is mapped to it shall be referenced here.

######### FOREIGN-REFERENCE 类型引用

########## 1. RteBswEventRef

- **UUID**: `ECUC:19a5b0f2-3ab5-4781-a071-fe850e69fbf7`
- **引用名**: `RteBswEventRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [1..1]
- **目标类型**: BSW-EVENT
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the BswEvent which is pointing to the BswSchedulableEntity being mapped. This allows a fine grained mapping of BswSchedulableEntites based on the activating BswEvent.

####### 2. RteBswExclusiveAreaImpl

**容器属性**:

- **UUID**: `ECUC:ecd2f711-51be-4b48-83a2-219528eaaa17`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `RteBswExclusiveAreaImpl`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

Represents one ExclusiveArea of one BswImplementation. Used to specify the implementation means of this ExclusiveArea.

######## 参数配置

此容器包含 **1** 个参数：

######### ENUMERATION 类型参数

########## 1. RteExclusiveAreaImplMechanism

- **UUID**: `ECUC:99e2df6b-46ef-9a25-3991-e9af1b370716`
- **参数名**: `RteExclusiveAreaImplMechanism`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `ALL_INTERRUPT_BLOCKING` (来源: AUTOSAR_ECUC)
  - `COOPERATIVE_RUNNABLE_PLACEMENT` (来源: AUTOSAR_ECUC)
  - `OS_INTERRUPT_BLOCKING` (来源: AUTOSAR_ECUC)
  - `OS_RESOURCE` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: To be used implementation mechanism for the specified ExclusiveArea.

######## 引用关系

此容器包含 **2** 个引用：

######### REFERENCE 类型引用

########## 1. RteBswExclusiveAreaOsResourceRef

- **UUID**: `ECUC:bfaccb50-3017-44d5-9c2c-692cbd375d3d`
- **引用名**: `RteBswExclusiveAreaOsResourceRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `OsResource`
- **完整路径**: `/AUTOSAR/EcucDefs/Os/OsResource`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Optional reference to an OsResource in case RteExclusiveAreaImplMechanism is configured to OS_RESOURCE for this ExclusiveArea.

######### FOREIGN-REFERENCE 类型引用

########## 1. RteBswExclusiveAreaRef

- **UUID**: `ECUC:9a3b4142-244d-40d2-a461-6a6b3f605891`
- **引用名**: `RteBswExclusiveAreaRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [1..1]
- **目标类型**: EXCLUSIVE-AREA
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the ExclusiveArea for which the implementation mechanism shall be specified.

####### 3. RteBswExternalTriggerConfig

**容器属性**:

- **UUID**: `ECUC:688ea382-3121-41b8-9154-1dae22574bb1`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `RteBswExternalTriggerConfig`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

Defines the configuration of Inter Basic Software Module Entity Triggering

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. RteBswTriggerSourceQueueLength

- **UUID**: `ECUC:8e3f0109-f9d6-4d96-a7b4-426d34a2df8d`
- **参数名**: `RteBswTriggerSourceQueueLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Length of trigger queue on the trigger source side.

######## 引用关系

此容器包含 **1** 个引用：

######### FOREIGN-REFERENCE 类型引用

########## 1. RteBswTriggerSourceRef

- **UUID**: `ECUC:14e5c9f2-c045-4361-b468-014f05cff0c1`
- **引用名**: `RteBswTriggerSourceRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [1..1]
- **目标类型**: TRIGGER
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a Trigger instance in the role releasedTrigger of the related BSW Module instance.

####### 4. RteBswInternalTriggerConfig

**容器属性**:

- **UUID**: `ECUC:a5286cb1-c7f4-4443-8e6b-acdf95acd48f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `RteBswInternalTriggerConfig`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

Defines the configuration of internal Basic Software Module Entity Triggering

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. RteBswTriggerSourceQueueLength

- **UUID**: `ECUC:aa2dbdc3-da03-428c-bc5f-53c87a67924a`
- **参数名**: `RteBswTriggerSourceQueueLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Length of trigger queue on the trigger source side.

######## 引用关系

此容器包含 **1** 个引用：

######### FOREIGN-REFERENCE 类型引用

########## 1. RteBswTriggerSourceRef

- **UUID**: `ECUC:7562c2f1-f297-4db0-aaca-a5aac909df71`
- **引用名**: `RteBswTriggerSourceRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [1..1]
- **目标类型**: BSW-INTERNAL-TRIGGERING-POINT
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a BswInternalTriggeringPoint of the related BSW Module instance.

####### 5. RteBswRequiredModeGroupConnection

**容器属性**:

- **UUID**: `ECUC:aee0016a-18aa-47c1-86a0-3450fece2c57`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `RteBswRequiredModeGroupConnection`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

Defines the connection between one requiredModeGroup of this BSW Module instance and one providedModeGroup instance.

######## 引用关系

此容器包含 **3** 个引用：

######### REFERENCE 类型引用

########## 1. RteBswProvidedModeGrpModInstRef

- **UUID**: `ECUC:372f5d03-9e40-442f-bf89-c9b591bc3a1b`
- **引用名**: `RteBswProvidedModeGrpModInstRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `RteBswModuleInstance`
- **完整路径**: `/AUTOSAR/EcucDefs/Rte/RteBswModuleInstance`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the RteBswModuleInstance configuration container which identifies the instance of the BSW Module.

######### FOREIGN-REFERENCE 类型引用

########## 1. RteBswProvidedModeGroupRef

- **UUID**: `ECUC:10edd3bb-d7a0-4d50-ac2f-0dcf089f2057`
- **引用名**: `RteBswProvidedModeGroupRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [1..1]
- **目标类型**: MODE-DECLARATION-GROUP-PROTOTYPE
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: References the providedModeGroupPrototype to which this requiredModeGroup shall be connected.

########## 2. RteBswRequiredModeGroupRef

- **UUID**: `ECUC:f90387a5-def5-4c69-883c-ece7852aa501`
- **引用名**: `RteBswRequiredModeGroupRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [1..1]
- **目标类型**: MODE-DECLARATION-GROUP-PROTOTYPE
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: References requiredModeGroupPrototype which shall be connected to the providedModeGroupPrototype.

####### 6. RteBswRequiredTriggerConnection

**容器属性**:

- **UUID**: `ECUC:3912fa7d-b613-43a0-acc5-3bd48eba465a`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `RteBswRequiredTriggerConnection`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

Defines the connection between one requiredTrigger of this BSW Module instance and one releasedTrigger instance.

######## 引用关系

此容器包含 **3** 个引用：

######### REFERENCE 类型引用

########## 1. RteBswReleasedTriggerModInstRef

- **UUID**: `ECUC:a006e25a-d445-42a1-ad24-d5662dd09c50`
- **引用名**: `RteBswReleasedTriggerModInstRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `RteBswModuleInstance`
- **完整路径**: `/AUTOSAR/EcucDefs/Rte/RteBswModuleInstance`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the RteBswModuleInstance configuration container which identifies the instance of the BSW Module.

######### FOREIGN-REFERENCE 类型引用

########## 1. RteBswReleasedTriggerRef

- **UUID**: `ECUC:617f252e-dd66-4dba-bfe9-093d47bbde92`
- **引用名**: `RteBswReleasedTriggerRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [1..1]
- **目标类型**: TRIGGER
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: References the releasedTrigger to which this requiredTrigger shall be connected.

########## 2. RteBswRequiredTriggerRef

- **UUID**: `ECUC:b6ae012b-ad8e-4d2b-aaa9-27643c268fed`
- **引用名**: `RteBswRequiredTriggerRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [1..1]
- **目标类型**: TRIGGER
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: References one requiredTrigger which shall be connected to the releasedTrigger.

##### 3. RteBswEventToTaskMapping

**容器属性**:

- **UUID**: `ECUC:08cf8b6e-658c-4155-b94c-ea8f896edf86`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `RteBswEventToTaskMapping`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

Maps a BswSchedulableEntity onto one OsTask based on the activating BswEvent.

###### 参数配置

此容器包含 **4** 个参数：

####### INTEGER 类型参数

######## 1. RteBswPositionInTask

- **UUID**: `ECUC:340833cb-ccb6-4344-b1d6-2a26c6cd37d8`
- **参数名**: `RteBswPositionInTask`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Each BswSchedulableEntity activation mapped to an OsTask has a specific position within the task execution.

####### BOOLEAN 类型参数

######## 1. RteBswImmediateRestart

- **UUID**: `ECUC:a2949613-66e5-410e-8d2f-342d6f979540`
- **参数名**: `RteBswImmediateRestart`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: When RteBswImmediateRestart is set to true the BswSchedulableEntitiy shall be immediately re-started after termination if it was activated by this BswEvent while it was already started.

####### FLOAT 类型参数

######## 1. RteBswActivationOffset

- **UUID**: `ECUC:401a3169-d17a-4a9a-bbd0-9fd78e30c954`
- **参数名**: `RteBswActivationOffset`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **取值范围**: [0..Inf]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Activation offset in seconds.

####### ENUMERATION 类型参数

######## 1. RteOsSchedulePoint

- **UUID**: `ECUC:10f88432-83be-8e8c-3fff-24665fee711c`
- **参数名**: `RteOsSchedulePoint`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `CONDITIONAL` (来源: AUTOSAR_ECUC)
  - `NONE` (来源: AUTOSAR_ECUC)
  - `UNCONDITIONAL` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Introduce a schedule point by explicitly calling Os Schedule service after the execution of the ExecutableEntity.  The Rte generator is allowed to optimize several consecutive calls to Os schedule into one single call if the ExecutableEntity executions in between have been skipped.

###### 引用关系

此容器包含 **5** 个引用：

####### REFERENCE 类型引用

######## 1. RteBswMappedToTaskRef

- **UUID**: `ECUC:5805eeeb-c5ac-4456-a9a3-4f1c0c6ffa4d`
- **引用名**: `RteBswMappedToTaskRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `OsTask`
- **完整路径**: `/AUTOSAR/EcucDefs/Os/OsTask`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the OsTask the BswSchedulableEntity activated by the RteBswEventRef is mapped to.

######## 2. RteBswUsedOsAlarmRef

- **UUID**: `ECUC:77e1d7a6-f016-4110-a9ca-6f63fd952985`
- **引用名**: `RteBswUsedOsAlarmRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `OsAlarm`
- **完整路径**: `/AUTOSAR/EcucDefs/Os/OsAlarm`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: If an OsAlarm is used to activate the OsTask this BswEvent is mapped to it shall be referenced here.

######## 3. RteBswUsedOsEventRef

- **UUID**: `ECUC:49171fb6-569b-4353-8367-1455283f619c`
- **引用名**: `RteBswUsedOsEventRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `OsEvent`
- **完整路径**: `/AUTOSAR/EcucDefs/Os/OsEvent`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: If an OsEvent is used to activate the OsTask this BswEvent is mapped to it shall be referenced here.

######## 4. RteBswUsedOsSchTblExpiryPointRef

- **UUID**: `ECUC:f8938c8c-d05a-4da3-873c-df1a8e623888`
- **引用名**: `RteBswUsedOsSchTblExpiryPointRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `OsScheduleTableExpiryPoint`
- **完整路径**: `/AUTOSAR/EcucDefs/Os/OsScheduleTable/OsScheduleTableExpiryPoint`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: If an OsScheduleTableExpiryPoint is used to activate the OsTask this BswEvent is mapped to it shall be referenced here.

####### FOREIGN-REFERENCE 类型引用

######## 1. RteBswEventRef

- **UUID**: `ECUC:19a5b0f2-3ab5-4781-a071-fe850e69fbf7`
- **引用名**: `RteBswEventRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [1..1]
- **目标类型**: BSW-EVENT
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the BswEvent which is pointing to the BswSchedulableEntity being mapped. This allows a fine grained mapping of BswSchedulableEntites based on the activating BswEvent.

##### 4. RteBswExclusiveAreaImpl

**容器属性**:

- **UUID**: `ECUC:ecd2f711-51be-4b48-83a2-219528eaaa17`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `RteBswExclusiveAreaImpl`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

Represents one ExclusiveArea of one BswImplementation. Used to specify the implementation means of this ExclusiveArea.

###### 参数配置

此容器包含 **1** 个参数：

####### ENUMERATION 类型参数

######## 1. RteExclusiveAreaImplMechanism

- **UUID**: `ECUC:99e2df6b-46ef-9a25-3991-e9af1b370716`
- **参数名**: `RteExclusiveAreaImplMechanism`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `ALL_INTERRUPT_BLOCKING` (来源: AUTOSAR_ECUC)
  - `COOPERATIVE_RUNNABLE_PLACEMENT` (来源: AUTOSAR_ECUC)
  - `OS_INTERRUPT_BLOCKING` (来源: AUTOSAR_ECUC)
  - `OS_RESOURCE` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: To be used implementation mechanism for the specified ExclusiveArea.

###### 引用关系

此容器包含 **2** 个引用：

####### REFERENCE 类型引用

######## 1. RteBswExclusiveAreaOsResourceRef

- **UUID**: `ECUC:bfaccb50-3017-44d5-9c2c-692cbd375d3d`
- **引用名**: `RteBswExclusiveAreaOsResourceRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `OsResource`
- **完整路径**: `/AUTOSAR/EcucDefs/Os/OsResource`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Optional reference to an OsResource in case RteExclusiveAreaImplMechanism is configured to OS_RESOURCE for this ExclusiveArea.

####### FOREIGN-REFERENCE 类型引用

######## 1. RteBswExclusiveAreaRef

- **UUID**: `ECUC:9a3b4142-244d-40d2-a461-6a6b3f605891`
- **引用名**: `RteBswExclusiveAreaRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [1..1]
- **目标类型**: EXCLUSIVE-AREA
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the ExclusiveArea for which the implementation mechanism shall be specified.

##### 5. RteBswExternalTriggerConfig

**容器属性**:

- **UUID**: `ECUC:688ea382-3121-41b8-9154-1dae22574bb1`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `RteBswExternalTriggerConfig`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

Defines the configuration of Inter Basic Software Module Entity Triggering

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. RteBswTriggerSourceQueueLength

- **UUID**: `ECUC:8e3f0109-f9d6-4d96-a7b4-426d34a2df8d`
- **参数名**: `RteBswTriggerSourceQueueLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Length of trigger queue on the trigger source side.

###### 引用关系

此容器包含 **1** 个引用：

####### FOREIGN-REFERENCE 类型引用

######## 1. RteBswTriggerSourceRef

- **UUID**: `ECUC:14e5c9f2-c045-4361-b468-014f05cff0c1`
- **引用名**: `RteBswTriggerSourceRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [1..1]
- **目标类型**: TRIGGER
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a Trigger instance in the role releasedTrigger of the related BSW Module instance.

##### 6. RteBswInternalTriggerConfig

**容器属性**:

- **UUID**: `ECUC:a5286cb1-c7f4-4443-8e6b-acdf95acd48f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `RteBswInternalTriggerConfig`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

Defines the configuration of internal Basic Software Module Entity Triggering

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. RteBswTriggerSourceQueueLength

- **UUID**: `ECUC:aa2dbdc3-da03-428c-bc5f-53c87a67924a`
- **参数名**: `RteBswTriggerSourceQueueLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Length of trigger queue on the trigger source side.

###### 引用关系

此容器包含 **1** 个引用：

####### FOREIGN-REFERENCE 类型引用

######## 1. RteBswTriggerSourceRef

- **UUID**: `ECUC:7562c2f1-f297-4db0-aaca-a5aac909df71`
- **引用名**: `RteBswTriggerSourceRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [1..1]
- **目标类型**: BSW-INTERNAL-TRIGGERING-POINT
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a BswInternalTriggeringPoint of the related BSW Module instance.

##### 7. RteBswRequiredModeGroupConnection

**容器属性**:

- **UUID**: `ECUC:aee0016a-18aa-47c1-86a0-3450fece2c57`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `RteBswRequiredModeGroupConnection`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

Defines the connection between one requiredModeGroup of this BSW Module instance and one providedModeGroup instance.

###### 引用关系

此容器包含 **3** 个引用：

####### REFERENCE 类型引用

######## 1. RteBswProvidedModeGrpModInstRef

- **UUID**: `ECUC:372f5d03-9e40-442f-bf89-c9b591bc3a1b`
- **引用名**: `RteBswProvidedModeGrpModInstRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `RteBswModuleInstance`
- **完整路径**: `/AUTOSAR/EcucDefs/Rte/RteBswModuleInstance`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the RteBswModuleInstance configuration container which identifies the instance of the BSW Module.

####### FOREIGN-REFERENCE 类型引用

######## 1. RteBswProvidedModeGroupRef

- **UUID**: `ECUC:10edd3bb-d7a0-4d50-ac2f-0dcf089f2057`
- **引用名**: `RteBswProvidedModeGroupRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [1..1]
- **目标类型**: MODE-DECLARATION-GROUP-PROTOTYPE
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: References the providedModeGroupPrototype to which this requiredModeGroup shall be connected.

######## 2. RteBswRequiredModeGroupRef

- **UUID**: `ECUC:f90387a5-def5-4c69-883c-ece7852aa501`
- **引用名**: `RteBswRequiredModeGroupRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [1..1]
- **目标类型**: MODE-DECLARATION-GROUP-PROTOTYPE
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: References requiredModeGroupPrototype which shall be connected to the providedModeGroupPrototype.

##### 8. RteBswRequiredTriggerConnection

**容器属性**:

- **UUID**: `ECUC:3912fa7d-b613-43a0-acc5-3bd48eba465a`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `RteBswRequiredTriggerConnection`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

Defines the connection between one requiredTrigger of this BSW Module instance and one releasedTrigger instance.

###### 引用关系

此容器包含 **3** 个引用：

####### REFERENCE 类型引用

######## 1. RteBswReleasedTriggerModInstRef

- **UUID**: `ECUC:a006e25a-d445-42a1-ad24-d5662dd09c50`
- **引用名**: `RteBswReleasedTriggerModInstRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `RteBswModuleInstance`
- **完整路径**: `/AUTOSAR/EcucDefs/Rte/RteBswModuleInstance`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the RteBswModuleInstance configuration container which identifies the instance of the BSW Module.

####### FOREIGN-REFERENCE 类型引用

######## 1. RteBswReleasedTriggerRef

- **UUID**: `ECUC:617f252e-dd66-4dba-bfe9-093d47bbde92`
- **引用名**: `RteBswReleasedTriggerRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [1..1]
- **目标类型**: TRIGGER
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: References the releasedTrigger to which this requiredTrigger shall be connected.

######## 2. RteBswRequiredTriggerRef

- **UUID**: `ECUC:b6ae012b-ad8e-4d2b-aaa9-27643c268fed`
- **引用名**: `RteBswRequiredTriggerRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [1..1]
- **目标类型**: TRIGGER
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: References one requiredTrigger which shall be connected to the releasedTrigger.

##### 9. RteGeneration

**容器属性**:

- **UUID**: `ECUC:d822ac60-5646-4210-a4be-4fc35a19a365`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `RteGeneration`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

This container holds the parameters for the configuration of the RTE Generation.

###### 参数配置

此容器包含 **13** 个参数：

####### INTEGER 类型参数

######## 1. RteCodeVendorId

- **UUID**: `ECUC:c2e5d496-ff9c-4da2-8611-9e723d1dd6e1`
- **参数名**: `RteCodeVendorId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Holds the vendor ID of the generated Rte code.

######## 2. RteToolChainSignificantCharacters

- **UUID**: `ECUC:381990e5-b902-4e03-b147-93a316e8962f`
- **参数名**: `RteToolChainSignificantCharacters`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `31`
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: If present, the RTE generator shall provide the list of C RTE identifiers whose name is not unique when only the first RteToolChainSignificantCharacters characters are considered.

####### BOOLEAN 类型参数

######## 1. RteDevErrorDetect

- **UUID**: `ECUC:eda1bae0-a0c3-450a-a9d8-8c9ecc44429f`
- **参数名**: `RteDevErrorDetect`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The Rte shall log development errors to the Det module.

######## 2. RteDevErrorDetectUninit

- **UUID**: `ECUC:b6a5c6ab-4dc0-4268-891a-d0b2d7f79fd5`
- **参数名**: `RteDevErrorDetectUninit`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The Rte shall detect if it is started when its APIs are called, and the BSW Scheduler shall check if it is initialized when its APIs are called.

######## 3. RteMeasurementSupport

- **UUID**: `ECUC:fc3ac296-b5d0-436b-86c4-dbd2dbf9a980`
- **参数名**: `RteMeasurementSupport`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The RTE generator shall have the option to switch off support for measurement for generated RTE code. This option shall influence complete RTE code at once.

######## 4. RteValueRangeCheckEnabled

- **UUID**: `ECUC:c050b8bc-1a9c-4b25-b71f-22a3b2d6e33c`
- **参数名**: `RteValueRangeCheckEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: If set to true the RTE generator shall enable the value range checking for the specified VariableDataPrototypes.

######## 5. RteVfbTraceEnabled

- **UUID**: `ECUC:2d3d667f-3d74-4fcb-a2c7-f970f249ff82`
- **参数名**: `RteVfbTraceEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The RTE generator shall globally enable VFB tracing when RteVfbTrace is set to "true".

####### ENUMERATION 类型参数

######## 1. RteCalibrationSupport

- **UUID**: `ECUC:0c41004f-f5a1-4bbe-bd4f-fc2f31b33acf`
- **参数名**: `RteCalibrationSupport`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `NONE`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `DOUBLE_POINTERED` (来源: AUTOSAR_ECUC)
  - `INITIALIZED_RAM` (来源: AUTOSAR_ECUC)
  - `NONE` (来源: AUTOSAR_ECUC)
  - `SINGLE_POINTERED` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The RTE generator shall have the option to switch off support for calibration for generated RTE code. This option shall influence complete RTE code at once.

######## 2. RteGenerationMode

- **UUID**: `ECUC:62f31d7d-c2d5-4463-96b5-9e78bb45cc8e`
- **参数名**: `RteGenerationMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `COMPATIBILITY_MODE`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `COMPATIBILITY_MODE` (来源: AUTOSAR_ECUC)
  - `VENDOR_MODE` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Switch between the two available generation modes of the RTE generator.

######## 3. RteIocInteractionReturnValue

- **UUID**: `ECUC:3bc9b4a5-41c2-45de-8ebd-218acf24320a`
- **参数名**: `RteIocInteractionReturnValue`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `RTE_IOC`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `RTE_COM` (来源: AUTOSAR_ECUC)
  - `RTE_IOC` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines whether the return value of RTE APIs is based on RTE-IOC interaction or RTE-COM interaction.

######## 4. RteOptimizationMode

- **UUID**: `ECUC:f296fdb7-70d5-406d-8388-66ab083b5b40`
- **参数名**: `RteOptimizationMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `RUNTIME`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `MEMORY` (来源: AUTOSAR_ECUC)
  - `RUNTIME` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Switch between the two available optimization modes of the RTE generator.

####### FUNCTION-NAME 类型参数

######## 1. RteVfbTraceFunction

- **UUID**: `ECUC:30a2c139-8710-42c0-b309-5dd619ede8a2`
- **参数名**: `RteVfbTraceFunction`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..infinite]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **函数变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The RTE generator shall enable VFB tracing for a given hook function when there is a #define in the RTE configuration header file for the hook function name and tracing is globally enabled.

####### LINKER-SYMBOL 类型参数

######## 1. RteVfbTraceClientPrefix

- **UUID**: `ECUC:614246f7-4e1c-46aa-96d5-1408578a2549`
- **参数名**: `RteVfbTraceClientPrefix`
- **数据类型**: LINKER-SYMBOL
- **多重性**: [0..infinite]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines an additional prefix for all VFB trace functions to be generated. With this approach it is possible to have debugging and DLT trace functions at the same time.

##### 10. RteImplicitCommunication

**容器属性**:

- **UUID**: `ECUC:acef0099-d337-475d-aadf-4ac579c2b257`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `RteImplicitCommunication`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

Configuration of the Implicit Communication behavior to be generated.

###### 参数配置

此容器包含 **2** 个参数：

####### BOOLEAN 类型参数

######## 1. RteCoherentAccess

- **UUID**: `ECUC:4105e34e-2489-4675-a302-ba39a2f67b59`
- **参数名**: `RteCoherentAccess`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: If set to true the referenced VariableAccess'es of this RteImplicitCommunication container are in one CoherencyGroup.

######## 2. RteImmediateBufferUpdate

- **UUID**: `ECUC:6d2fe021-a6a8-41bf-876e-603aa0fed24e`
- **参数名**: `RteImmediateBufferUpdate`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: If set to true the RTE will perform preemption area specific buffer update immediately before (for VariableAccess in the role dataReadAccess) resp. after (for VariableAccess in the role dataWriteAccess) Runnable execution.

###### 引用关系

此容器包含 **3** 个引用：

####### FOREIGN-REFERENCE 类型引用

######## 1. RteVariableReadAccessRef

- **UUID**: `ECUC:0730bef6-369d-43c8-ac1b-71a0f3b1709f`
- **引用名**: `RteVariableReadAccessRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [0..infinite]
- **目标类型**: VARIABLE-ACCESS
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the VariableAccess in the dataReadAccess role.

######## 2. RteVariableWriteAccessRef

- **UUID**: `ECUC:2f22b7f0-7e49-49e1-9448-3369cf69ca96`
- **引用名**: `RteVariableWriteAccessRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [0..infinite]
- **目标类型**: VARIABLE-ACCESS
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the VariableAccess in the dataWriteAccess role.

####### INSTANCE-REFERENCE 类型引用

######## 1. RteSoftwareComponentInstanceRef

- **UUID**: `ECUC:56159496-6cce-4956-b6ad-50a858392103`
- **引用名**: `RteSoftwareComponentInstanceRef`
- **引用类型**: INSTANCE-REFERENCE
- **多重性**: [1..infinite]
- **目标类型**: SW-COMPONENT-PROTOTYPE
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a SwComponentPrototype.

##### 11. RteInitializationBehavior

**容器属性**:

- **UUID**: `ECUC:79c14dff-b2e4-41a6-9358-eee2beb9c801`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `RteInitializationBehavior`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

Specifies the initialization strategy for variables allocated by RTE with the purpose to implement VariableDataPrototypes.

###### 参数配置

此容器包含 **2** 个参数：

####### STRING 类型参数

######## 1. RteSectionInitializationPolicy

- **UUID**: `ECUC:614a2811-2efd-41e7-9109-fb467f80adf2`
- **参数名**: `RteSectionInitializationPolicy`
- **数据类型**: STRING
- **多重性**: [1..infinite]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter describes the SectionInitializationPolicys for which a particular RTE initialization strategy applies.

####### ENUMERATION 类型参数

######## 1. RteInitializationStrategy

- **UUID**: `ECUC:b35aa018-ac22-4135-a835-3c50cab1b405`
- **参数名**: `RteInitializationStrategy`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `RTE_INITIALIZATION_STRATEGY_AT_DATA_DECLARATION` (来源: AUTOSAR_ECUC)
  - `RTE_INITIALIZATION_STRATEGY_AT_DATA_DECLARATION_AND_PARTITION_RESTART` (来源: AUTOSAR_ECUC)
  - `RTE_INITIALIZATION_STRATEGY_AT_RTE_START_AND_PARTITION_RESTART` (来源: AUTOSAR_ECUC)
  - `RTE_INITIALIZATION_STRATEGY_NONE` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Definition of the initialization strategy applicable for the SectionInitializationPolicys selected by RteSectionInitializationPolicy.

##### 12. RteOsInteraction

**容器属性**:

- **UUID**: `ECUC:28d9953f-8082-4c32-96f6-db70006cbe8e`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `RteOsInteraction`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

Interaction of the Rte with the Os.

###### 配置容器

本模块包含 **4** 个配置容器：

####### 1. RteModeToScheduleTableMapping

**容器属性**:

- **UUID**: `ECUC:3963a985-ef8c-4107-b1cd-bb1794427f9d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `RteModeToScheduleTableMapping`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

Provides configuration input in which Modes of a ModeDeclarionGroupPrototype of a Mode Manager a OsScheudleTable shall be active.

######## 引用关系

此容器包含 **2** 个引用：

######### REFERENCE 类型引用

########## 1. RteModeScheduleTableRef

- **UUID**: `ECUC:6864a213-4aac-447b-9b1d-4ac60c4db010`
- **引用名**: `RteModeScheduleTableRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `OsScheduleTable`
- **完整路径**: `/AUTOSAR/EcucDefs/Os/OsScheduleTable`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the OsScheduleTable which shall be active in the specified RteModeSchblMapModeDeclarationRefs.

######### FOREIGN-REFERENCE 类型引用

########## 1. RteModeSchtblMapModeDeclarationRef

- **UUID**: `ECUC:85172466-6a8c-42b2-b930-2405da434c0a`
- **引用名**: `RteModeSchtblMapModeDeclarationRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [1..infinite]
- **目标类型**: MODE-DECLARATION
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the ModeDeclarations.

######## 配置容器

本模块包含 **2** 个配置容器：

######### 1. RteModeSchtblMapBsw

**容器属性**:

- **UUID**: `ECUC:8fda33d9-e70a-4a72-b5ef-ab0c0508736d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `RteModeSchtblMapBsw`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Specifies an instance of a ModeDeclarationGroupPrototype of a Bsw-Module.

########## 引用关系

此容器包含 **2** 个引用：

########### REFERENCE 类型引用

############ 1. RteModeSchtblMapBswInstanceRef

- **UUID**: `ECUC:82d8870e-9243-4bc4-92c2-404d844a35b9`
- **引用名**: `RteModeSchtblMapBswInstanceRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `RteBswModuleInstance`
- **完整路径**: `/AUTOSAR/EcucDefs/Rte/RteBswModuleInstance`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to an instance specification of a Bsw-Module.

########### FOREIGN-REFERENCE 类型引用

############ 1. RteModeSchtblMapBswProvidedModeGroupRef

- **UUID**: `ECUC:77074973-7919-4eb4-aeff-e8433ccc6216`
- **引用名**: `RteModeSchtblMapBswProvidedModeGroupRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [1..1]
- **目标类型**: MODE-DECLARATION-GROUP-PROTOTYPE
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to an instance of a ModeDeclarationGroupPrototype of a Bsw-Module.

######### 2. RteModeSchtblMapSwc

**容器属性**:

- **UUID**: `ECUC:6eec3900-61d9-487c-b0c1-b2c3d946eb59`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `RteModeSchtblMapSwc`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Specifies an instance of a ModeDeclarationGroupPrototype of a SwComponentPrototype.

########## 引用关系

此容器包含 **2** 个引用：

########### REFERENCE 类型引用

############ 1. RteModeSchtblMapSwcInstanceRef

- **UUID**: `ECUC:12d0c2a9-fa13-419b-b0b2-ed6f4e59f536`
- **引用名**: `RteModeSchtblMapSwcInstanceRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `RteSwComponentInstance`
- **完整路径**: `/AUTOSAR/EcucDefs/Rte/RteSwComponentInstance`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to an instance specification of a SwComponentPrototype.

########### FOREIGN-REFERENCE 类型引用

############ 1. RteModeSchtblMapSwcPortRef

- **UUID**: `ECUC:bdfe3267-90f3-4abc-aae8-5787c1cde2ee`
- **引用名**: `RteModeSchtblMapSwcPortRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [1..1]
- **目标类型**: P-PORT-PROTOTYPE
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the PPortPrototype of a SwComponentPrototype.

####### 2. RteModeSchtblMapBsw

**容器属性**:

- **UUID**: `ECUC:8fda33d9-e70a-4a72-b5ef-ab0c0508736d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `RteModeSchtblMapBsw`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Specifies an instance of a ModeDeclarationGroupPrototype of a Bsw-Module.

######## 引用关系

此容器包含 **2** 个引用：

######### REFERENCE 类型引用

########## 1. RteModeSchtblMapBswInstanceRef

- **UUID**: `ECUC:82d8870e-9243-4bc4-92c2-404d844a35b9`
- **引用名**: `RteModeSchtblMapBswInstanceRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `RteBswModuleInstance`
- **完整路径**: `/AUTOSAR/EcucDefs/Rte/RteBswModuleInstance`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to an instance specification of a Bsw-Module.

######### FOREIGN-REFERENCE 类型引用

########## 1. RteModeSchtblMapBswProvidedModeGroupRef

- **UUID**: `ECUC:77074973-7919-4eb4-aeff-e8433ccc6216`
- **引用名**: `RteModeSchtblMapBswProvidedModeGroupRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [1..1]
- **目标类型**: MODE-DECLARATION-GROUP-PROTOTYPE
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to an instance of a ModeDeclarationGroupPrototype of a Bsw-Module.

####### 3. RteModeSchtblMapSwc

**容器属性**:

- **UUID**: `ECUC:6eec3900-61d9-487c-b0c1-b2c3d946eb59`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `RteModeSchtblMapSwc`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Specifies an instance of a ModeDeclarationGroupPrototype of a SwComponentPrototype.

######## 引用关系

此容器包含 **2** 个引用：

######### REFERENCE 类型引用

########## 1. RteModeSchtblMapSwcInstanceRef

- **UUID**: `ECUC:12d0c2a9-fa13-419b-b0b2-ed6f4e59f536`
- **引用名**: `RteModeSchtblMapSwcInstanceRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `RteSwComponentInstance`
- **完整路径**: `/AUTOSAR/EcucDefs/Rte/RteSwComponentInstance`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to an instance specification of a SwComponentPrototype.

######### FOREIGN-REFERENCE 类型引用

########## 1. RteModeSchtblMapSwcPortRef

- **UUID**: `ECUC:bdfe3267-90f3-4abc-aae8-5787c1cde2ee`
- **引用名**: `RteModeSchtblMapSwcPortRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [1..1]
- **目标类型**: P-PORT-PROTOTYPE
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the PPortPrototype of a SwComponentPrototype.

####### 4. RteUsedOsActivation

**容器属性**:

- **UUID**: `ECUC:f025abf7-c579-4bee-a949-9fc81f463d5d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `RteUsedOsActivation`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

Attributes used in the activation of OsTasks and Runnable Entities.

######## 参数配置

此容器包含 **2** 个参数：

######### FLOAT 类型参数

########## 1. RteExpectedActivationOffset

- **UUID**: `ECUC:70132270-1ce0-465b-9a54-bc53328ef71a`
- **参数名**: `RteExpectedActivationOffset`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0..Inf]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Activation offset in seconds.

########## 2. RteExpectedTickDuration

- **UUID**: `ECUC:dee950e5-b82d-482d-a7a4-e4cffb7edad9`
- **参数名**: `RteExpectedTickDuration`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0..Inf]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The expected tick duration in seconds which shall be configured to drive the OsScheduleTables or OsAlarm.

######## 引用关系

此容器包含 **3** 个引用：

######### REFERENCE 类型引用

########## 1. RteActivationOsAlarmRef

- **UUID**: `ECUC:b8ec8697-3e87-4d7c-b677-2c8ccbd2e49c`
- **引用名**: `RteActivationOsAlarmRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `OsAlarm`
- **完整路径**: `/AUTOSAR/EcucDefs/Os/OsAlarm`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to an OsAlarm.

########## 2. RteActivationOsSchTblRef

- **UUID**: `ECUC:97b348c3-fa66-46ec-a890-9697cb73f2ff`
- **引用名**: `RteActivationOsSchTblRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `OsScheduleTable`
- **完整路径**: `/AUTOSAR/EcucDefs/Os/OsScheduleTable`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to an OsScheduleTable.

########## 3. RteActivationOsTaskRef

- **UUID**: `ECUC:fa2f62ca-b415-4849-8ead-27cf8b294802`
- **引用名**: `RteActivationOsTaskRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `OsTask`
- **完整路径**: `/AUTOSAR/EcucDefs/Os/OsTask`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to an OsTask.

##### 13. RteModeToScheduleTableMapping

**容器属性**:

- **UUID**: `ECUC:3963a985-ef8c-4107-b1cd-bb1794427f9d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `RteModeToScheduleTableMapping`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

Provides configuration input in which Modes of a ModeDeclarionGroupPrototype of a Mode Manager a OsScheudleTable shall be active.

###### 引用关系

此容器包含 **2** 个引用：

####### REFERENCE 类型引用

######## 1. RteModeScheduleTableRef

- **UUID**: `ECUC:6864a213-4aac-447b-9b1d-4ac60c4db010`
- **引用名**: `RteModeScheduleTableRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `OsScheduleTable`
- **完整路径**: `/AUTOSAR/EcucDefs/Os/OsScheduleTable`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the OsScheduleTable which shall be active in the specified RteModeSchblMapModeDeclarationRefs.

####### FOREIGN-REFERENCE 类型引用

######## 1. RteModeSchtblMapModeDeclarationRef

- **UUID**: `ECUC:85172466-6a8c-42b2-b930-2405da434c0a`
- **引用名**: `RteModeSchtblMapModeDeclarationRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [1..infinite]
- **目标类型**: MODE-DECLARATION
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the ModeDeclarations.

###### 配置容器

本模块包含 **2** 个配置容器：

####### 1. RteModeSchtblMapBsw

**容器属性**:

- **UUID**: `ECUC:8fda33d9-e70a-4a72-b5ef-ab0c0508736d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `RteModeSchtblMapBsw`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Specifies an instance of a ModeDeclarationGroupPrototype of a Bsw-Module.

######## 引用关系

此容器包含 **2** 个引用：

######### REFERENCE 类型引用

########## 1. RteModeSchtblMapBswInstanceRef

- **UUID**: `ECUC:82d8870e-9243-4bc4-92c2-404d844a35b9`
- **引用名**: `RteModeSchtblMapBswInstanceRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `RteBswModuleInstance`
- **完整路径**: `/AUTOSAR/EcucDefs/Rte/RteBswModuleInstance`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to an instance specification of a Bsw-Module.

######### FOREIGN-REFERENCE 类型引用

########## 1. RteModeSchtblMapBswProvidedModeGroupRef

- **UUID**: `ECUC:77074973-7919-4eb4-aeff-e8433ccc6216`
- **引用名**: `RteModeSchtblMapBswProvidedModeGroupRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [1..1]
- **目标类型**: MODE-DECLARATION-GROUP-PROTOTYPE
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to an instance of a ModeDeclarationGroupPrototype of a Bsw-Module.

####### 2. RteModeSchtblMapSwc

**容器属性**:

- **UUID**: `ECUC:6eec3900-61d9-487c-b0c1-b2c3d946eb59`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `RteModeSchtblMapSwc`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Specifies an instance of a ModeDeclarationGroupPrototype of a SwComponentPrototype.

######## 引用关系

此容器包含 **2** 个引用：

######### REFERENCE 类型引用

########## 1. RteModeSchtblMapSwcInstanceRef

- **UUID**: `ECUC:12d0c2a9-fa13-419b-b0b2-ed6f4e59f536`
- **引用名**: `RteModeSchtblMapSwcInstanceRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `RteSwComponentInstance`
- **完整路径**: `/AUTOSAR/EcucDefs/Rte/RteSwComponentInstance`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to an instance specification of a SwComponentPrototype.

######### FOREIGN-REFERENCE 类型引用

########## 1. RteModeSchtblMapSwcPortRef

- **UUID**: `ECUC:bdfe3267-90f3-4abc-aae8-5787c1cde2ee`
- **引用名**: `RteModeSchtblMapSwcPortRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [1..1]
- **目标类型**: P-PORT-PROTOTYPE
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the PPortPrototype of a SwComponentPrototype.

##### 14. RteModeSchtblMapBsw

**容器属性**:

- **UUID**: `ECUC:8fda33d9-e70a-4a72-b5ef-ab0c0508736d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `RteModeSchtblMapBsw`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Specifies an instance of a ModeDeclarationGroupPrototype of a Bsw-Module.

###### 引用关系

此容器包含 **2** 个引用：

####### REFERENCE 类型引用

######## 1. RteModeSchtblMapBswInstanceRef

- **UUID**: `ECUC:82d8870e-9243-4bc4-92c2-404d844a35b9`
- **引用名**: `RteModeSchtblMapBswInstanceRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `RteBswModuleInstance`
- **完整路径**: `/AUTOSAR/EcucDefs/Rte/RteBswModuleInstance`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to an instance specification of a Bsw-Module.

####### FOREIGN-REFERENCE 类型引用

######## 1. RteModeSchtblMapBswProvidedModeGroupRef

- **UUID**: `ECUC:77074973-7919-4eb4-aeff-e8433ccc6216`
- **引用名**: `RteModeSchtblMapBswProvidedModeGroupRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [1..1]
- **目标类型**: MODE-DECLARATION-GROUP-PROTOTYPE
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to an instance of a ModeDeclarationGroupPrototype of a Bsw-Module.

##### 15. RteModeSchtblMapSwc

**容器属性**:

- **UUID**: `ECUC:6eec3900-61d9-487c-b0c1-b2c3d946eb59`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `RteModeSchtblMapSwc`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Specifies an instance of a ModeDeclarationGroupPrototype of a SwComponentPrototype.

###### 引用关系

此容器包含 **2** 个引用：

####### REFERENCE 类型引用

######## 1. RteModeSchtblMapSwcInstanceRef

- **UUID**: `ECUC:12d0c2a9-fa13-419b-b0b2-ed6f4e59f536`
- **引用名**: `RteModeSchtblMapSwcInstanceRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `RteSwComponentInstance`
- **完整路径**: `/AUTOSAR/EcucDefs/Rte/RteSwComponentInstance`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to an instance specification of a SwComponentPrototype.

####### FOREIGN-REFERENCE 类型引用

######## 1. RteModeSchtblMapSwcPortRef

- **UUID**: `ECUC:bdfe3267-90f3-4abc-aae8-5787c1cde2ee`
- **引用名**: `RteModeSchtblMapSwcPortRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [1..1]
- **目标类型**: P-PORT-PROTOTYPE
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the PPortPrototype of a SwComponentPrototype.

##### 16. RteUsedOsActivation

**容器属性**:

- **UUID**: `ECUC:f025abf7-c579-4bee-a949-9fc81f463d5d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `RteUsedOsActivation`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

Attributes used in the activation of OsTasks and Runnable Entities.

###### 参数配置

此容器包含 **2** 个参数：

####### FLOAT 类型参数

######## 1. RteExpectedActivationOffset

- **UUID**: `ECUC:70132270-1ce0-465b-9a54-bc53328ef71a`
- **参数名**: `RteExpectedActivationOffset`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0..Inf]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Activation offset in seconds.

######## 2. RteExpectedTickDuration

- **UUID**: `ECUC:dee950e5-b82d-482d-a7a4-e4cffb7edad9`
- **参数名**: `RteExpectedTickDuration`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0..Inf]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The expected tick duration in seconds which shall be configured to drive the OsScheduleTables or OsAlarm.

###### 引用关系

此容器包含 **3** 个引用：

####### REFERENCE 类型引用

######## 1. RteActivationOsAlarmRef

- **UUID**: `ECUC:b8ec8697-3e87-4d7c-b677-2c8ccbd2e49c`
- **引用名**: `RteActivationOsAlarmRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `OsAlarm`
- **完整路径**: `/AUTOSAR/EcucDefs/Os/OsAlarm`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to an OsAlarm.

######## 2. RteActivationOsSchTblRef

- **UUID**: `ECUC:97b348c3-fa66-46ec-a890-9697cb73f2ff`
- **引用名**: `RteActivationOsSchTblRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `OsScheduleTable`
- **完整路径**: `/AUTOSAR/EcucDefs/Os/OsScheduleTable`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to an OsScheduleTable.

######## 3. RteActivationOsTaskRef

- **UUID**: `ECUC:fa2f62ca-b415-4849-8ead-27cf8b294802`
- **引用名**: `RteActivationOsTaskRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `OsTask`
- **完整路径**: `/AUTOSAR/EcucDefs/Os/OsTask`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to an OsTask.

##### 17. RtePostBuildVariantConfiguration

**容器属性**:

- **UUID**: `ECUC:adc969c3-7bcd-47f0-aef5-93e877978f6a`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `RtePostBuildVariantConfiguration`
- **多重性**: [1..1]
- **多配置容器**: true

**容器描述**:

Specifies the PostbuildVariantSets for each of the PostBuild configurations of the RTE.

###### 引用关系

此容器包含 **1** 个引用：

####### FOREIGN-REFERENCE 类型引用

######## 1. RtePostBuildUsedPredefinedVariant

- **UUID**: `ECUC:78bfdc70-d779-454a-bc49-5d4b020a5334`
- **引用名**: `RtePostBuildUsedPredefinedVariant`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [1..infinite]
- **目标类型**: PREDEFINED-VARIANT
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the PredefinedVariant element which defines the values for PostBuildVariationCriterion elements.

##### 18. RteSwComponentInstance

**容器属性**:

- **UUID**: `ECUC:fa1a7877-8a6a-4f02-967e-a2ad271002c6`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `RteSwComponentInstance`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

Representation of one SwComponentPrototype located on the to be configured ECU. All subcontainer configuration aspects are in relation to this SwComponentPrototype.

###### 引用关系

此容器包含 **1** 个引用：

####### FOREIGN-REFERENCE 类型引用

######## 1. RteSoftwareComponentInstanceRef

- **UUID**: `ECUC:950d21fa-8dcf-4fee-b7f6-35fb1a5b5698`
- **引用名**: `RteSoftwareComponentInstanceRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [0..1]
- **目标类型**: SW-COMPONENT-PROTOTYPE
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a SwComponentPrototype.

###### 配置容器

本模块包含 **5** 个配置容器：

####### 1. RteEventToTaskMapping

**容器属性**:

- **UUID**: `ECUC:55f79a11-b016-4684-baa0-b13ebe872218`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `RteEventToTaskMapping`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

Maps a RunnableEntity onto one OsTask based on the activating RTEEvent.

######## 参数配置

此容器包含 **4** 个参数：

######### INTEGER 类型参数

########## 1. RtePositionInTask

- **UUID**: `ECUC:db21f1ca-7010-40dc-b9ea-d83534e9fda0`
- **参数名**: `RtePositionInTask`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Each RunnableEntity mapped to an OsTask has a specific position within the task execution.

######### BOOLEAN 类型参数

########## 1. RteImmediateRestart

- **UUID**: `ECUC:5ae7b6fe-0b75-4b15-9605-28ed631e1d6b`
- **参数名**: `RteImmediateRestart`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: When RteImmediateRestart is set to true the RunnableEntitiy shall be immediately re-started after termination if it was activated by this RTEEvent while it was already started.

######### FLOAT 类型参数

########## 1. RteActivationOffset

- **UUID**: `ECUC:5670c865-e686-46a8-bd05-ee23c3c403d8`
- **参数名**: `RteActivationOffset`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **取值范围**: [0..Inf]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Activation offset in seconds.

######### ENUMERATION 类型参数

########## 1. RteOsSchedulePoint

- **UUID**: `ECUC:5e2092d5-ce48-93bb-4152-eb159506b3ae`
- **参数名**: `RteOsSchedulePoint`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `CONDITIONAL` (来源: AUTOSAR_ECUC)
  - `NONE` (来源: AUTOSAR_ECUC)
  - `UNCONDITIONAL` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Introduce a schedule point by explicitly calling Os Schedule service after the execution of the ExecutableEntity.  The Rte generator is allowed to optimize several consecutive calls to Os schedule into one single call if the ExecutableEntity executions in between have been skipped.

######## 引用关系

此容器包含 **6** 个引用：

######### REFERENCE 类型引用

########## 1. RteMappedToTaskRef

- **UUID**: `ECUC:54ed8fd8-7f54-48af-9999-3298e737f42c`
- **引用名**: `RteMappedToTaskRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `OsTask`
- **完整路径**: `/AUTOSAR/EcucDefs/Os/OsTask`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the OsTask the RunnableEntity activated by the RteEventRef is mapped to.

########## 2. RteUsedOsAlarmRef

- **UUID**: `ECUC:c28329bc-8af9-4bdd-a16d-81b65be4a22c`
- **引用名**: `RteUsedOsAlarmRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `OsAlarm`
- **完整路径**: `/AUTOSAR/EcucDefs/Os/OsAlarm`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: If an OsAlarm is used to activate the OsTask this RteEvent is mapped to it shall be referenced here.

########## 3. RteUsedOsEventRef

- **UUID**: `ECUC:8eaae343-6715-4407-874e-952aeff8431f`
- **引用名**: `RteUsedOsEventRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `OsEvent`
- **完整路径**: `/AUTOSAR/EcucDefs/Os/OsEvent`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: If an OsEvent is used to activate the OsTask this RteEvent is mapped to it shall be referenced here.

########## 4. RteUsedOsSchTblExpiryPointRef

- **UUID**: `ECUC:67d1ea7b-8df0-41f1-801d-24406799eec2`
- **引用名**: `RteUsedOsSchTblExpiryPointRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `OsScheduleTableExpiryPoint`
- **完整路径**: `/AUTOSAR/EcucDefs/Os/OsScheduleTable/OsScheduleTableExpiryPoint`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: If an OsScheduleTableExpiryPoint is used to activate the OsTask this RteEvent is mapped to it shall be referenced here.

########## 5. RteVirtuallyMappedToTaskRef

- **UUID**: `ECUC:a06ca1ba-8541-416c-ae14-5b3024c55921`
- **引用名**: `RteVirtuallyMappedToTaskRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `OsTask`
- **完整路径**: `/AUTOSAR/EcucDefs/Os/OsTask`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Optional reference to an OsTask where the activation of this RteEvent shall be evaluated. The actual execution of the Runnable Entity shall happen in the OsTask referenced by RteMappedToTaskRef.

######### FOREIGN-REFERENCE 类型引用

########## 1. RteEventRef

- **UUID**: `ECUC:8b0a26ff-adfc-43ed-97c6-6dfb72faf07e`
- **引用名**: `RteEventRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [1..1]
- **目标类型**: RTE-EVENT
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the description of the RTEEvent which is pointing to the RunnableEntity being mapped. This allows a fine grained mapping of RunnableEntites based on the activating RTEEvent.

####### 2. RteExclusiveAreaImplementation

**容器属性**:

- **UUID**: `ECUC:22d2982b-ad5c-4732-8261-a8c4026fd219`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `RteExclusiveAreaImplementation`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

Specifies the implementation to be used for the data consistency of this ExclusiveArea.

######## 参数配置

此容器包含 **1** 个参数：

######### ENUMERATION 类型参数

########## 1. RteExclusiveAreaImplMechanism

- **UUID**: `ECUC:cfe28085-a28d-960f-3851-70ddf4bc2f18`
- **参数名**: `RteExclusiveAreaImplMechanism`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `ALL_INTERRUPT_BLOCKING` (来源: AUTOSAR_ECUC)
  - `COOPERATIVE_RUNNABLE_PLACEMENT` (来源: AUTOSAR_ECUC)
  - `OS_INTERRUPT_BLOCKING` (来源: AUTOSAR_ECUC)
  - `OS_RESOURCE` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: To be used implementation mechanism for the specified ExclusiveArea.

######## 引用关系

此容器包含 **2** 个引用：

######### REFERENCE 类型引用

########## 1. RteExclusiveAreaOsResourceRef

- **UUID**: `ECUC:4437449b-4726-45df-a6f9-e5140dac45a4`
- **引用名**: `RteExclusiveAreaOsResourceRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `OsResource`
- **完整路径**: `/AUTOSAR/EcucDefs/Os/OsResource`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Optional reference to an OsResource in case RteExclusiveAreaImplMechanism is configured to OS_RESOURCE for this ExclusiveArea.

######### FOREIGN-REFERENCE 类型引用

########## 1. RteExclusiveAreaRef

- **UUID**: `ECUC:d13b3e1d-b539-415e-b180-5f72e267eb09`
- **引用名**: `RteExclusiveAreaRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [1..1]
- **目标类型**: EXCLUSIVE-AREA
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the ExclusiveArea.

####### 3. RteExternalTriggerConfig

**容器属性**:

- **UUID**: `ECUC:492cd7c7-08bb-4d9f-b57b-93f101030d4a`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `RteExternalTriggerConfig`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

Defines the configuration of External Trigger Event Communication for Software Components

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. RteTriggerSourceQueueLength

- **UUID**: `ECUC:83b0c418-daae-4fa6-b9c9-f1278b727989`
- **参数名**: `RteTriggerSourceQueueLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Length of trigger queue on the trigger source side.

######## 引用关系

此容器包含 **1** 个引用：

######### INSTANCE-REFERENCE 类型引用

########## 1. RteSwcTriggerSourceRef

- **UUID**: `ECUC:6d1ba104-9581-4004-b55f-7452656565dc`
- **引用名**: `RteSwcTriggerSourceRef`
- **引用类型**: INSTANCE-REFERENCE
- **多重性**: [1..1]
- **目标类型**: TRIGGER
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a Trigger instance in the pPortPrototype of the related component instance.

####### 4. RteInternalTriggerConfig

**容器属性**:

- **UUID**: `ECUC:bf95436e-1855-4955-9f07-a5105a62d79c`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `RteInternalTriggerConfig`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

Defines the configuration of Inter Runnable Triggering for Software Components

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. RteTriggerSourceQueueLength

- **UUID**: `ECUC:14a2048e-17be-40d4-b994-b9381b1f5af5`
- **参数名**: `RteTriggerSourceQueueLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Length of trigger queue on the trigger source side.

######## 引用关系

此容器包含 **1** 个引用：

######### FOREIGN-REFERENCE 类型引用

########## 1. RteSwcTriggerSourceRef

- **UUID**: `ECUC:5ce6febf-7565-4312-81dc-ee600c9d93b7`
- **引用名**: `RteSwcTriggerSourceRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [1..1]
- **目标类型**: INTERNAL-TRIGGERING-POINT
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to an InternalTriggeringPoint of the related component instance.

####### 5. RteNvRamAllocation

**容器属性**:

- **UUID**: `ECUC:bdb010d2-a51d-4eca-b2db-cf0231f3e4dd`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `RteNvRamAllocation`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

Specifies the relationship between the AtomicSwComponentType's NVRAMMapping / NVRAM needs and the NvM module configuration.

######## 参数配置

此容器包含 **2** 个参数：

######### LINKER-SYMBOL 类型参数

########## 1. RteNvmRamBlockLocationSymbol

- **UUID**: `ECUC:36efd7d0-9100-4744-987f-65801a66367f`
- **参数名**: `RteNvmRamBlockLocationSymbol`
- **数据类型**: LINKER-SYMBOL
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is the name of the linker object name where the NVRam Block will be mirrored by the Nvm.

########## 2. RteNvmRomBlockLocationSymbol

- **UUID**: `ECUC:b47d9a23-fef1-4a6e-8659-08412478eb25`
- **参数名**: `RteNvmRomBlockLocationSymbol`
- **数据类型**: LINKER-SYMBOL
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is the name of the linker object name where the NVRom Block will be accessed by the Nvm.

######## 引用关系

此容器包含 **2** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. RteNvmBlockRef

- **UUID**: `ECUC:e23479f3-7fee-4246-8834-3d17d8ad9e2f`
- **引用名**: `RteNvmBlockRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `NvMBlockDescriptor`
- **完整路径**: `/AUTOSAR/EcucDefs/NvM/NvMBlockDescriptor`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the used NvM block for storage of the NVRAMMapping information.

######### FOREIGN-REFERENCE 类型引用

########## 1. RteSwNvRamMappingRef

- **UUID**: `ECUC:cdba0597-501f-41bc-8dbd-d87e73c056f3`
- **引用名**: `RteSwNvRamMappingRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [1..1]
- **目标类型**: SWC-SERVICE-DEPENDENCY
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the SwSeriveDependency which is used to specify the NvBlockNeeds.

##### 19. RteEventToTaskMapping

**容器属性**:

- **UUID**: `ECUC:55f79a11-b016-4684-baa0-b13ebe872218`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `RteEventToTaskMapping`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

Maps a RunnableEntity onto one OsTask based on the activating RTEEvent.

###### 参数配置

此容器包含 **4** 个参数：

####### INTEGER 类型参数

######## 1. RtePositionInTask

- **UUID**: `ECUC:db21f1ca-7010-40dc-b9ea-d83534e9fda0`
- **参数名**: `RtePositionInTask`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Each RunnableEntity mapped to an OsTask has a specific position within the task execution.

####### BOOLEAN 类型参数

######## 1. RteImmediateRestart

- **UUID**: `ECUC:5ae7b6fe-0b75-4b15-9605-28ed631e1d6b`
- **参数名**: `RteImmediateRestart`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: When RteImmediateRestart is set to true the RunnableEntitiy shall be immediately re-started after termination if it was activated by this RTEEvent while it was already started.

####### FLOAT 类型参数

######## 1. RteActivationOffset

- **UUID**: `ECUC:5670c865-e686-46a8-bd05-ee23c3c403d8`
- **参数名**: `RteActivationOffset`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **取值范围**: [0..Inf]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Activation offset in seconds.

####### ENUMERATION 类型参数

######## 1. RteOsSchedulePoint

- **UUID**: `ECUC:5e2092d5-ce48-93bb-4152-eb159506b3ae`
- **参数名**: `RteOsSchedulePoint`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `CONDITIONAL` (来源: AUTOSAR_ECUC)
  - `NONE` (来源: AUTOSAR_ECUC)
  - `UNCONDITIONAL` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Introduce a schedule point by explicitly calling Os Schedule service after the execution of the ExecutableEntity.  The Rte generator is allowed to optimize several consecutive calls to Os schedule into one single call if the ExecutableEntity executions in between have been skipped.

###### 引用关系

此容器包含 **6** 个引用：

####### REFERENCE 类型引用

######## 1. RteMappedToTaskRef

- **UUID**: `ECUC:54ed8fd8-7f54-48af-9999-3298e737f42c`
- **引用名**: `RteMappedToTaskRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `OsTask`
- **完整路径**: `/AUTOSAR/EcucDefs/Os/OsTask`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the OsTask the RunnableEntity activated by the RteEventRef is mapped to.

######## 2. RteUsedOsAlarmRef

- **UUID**: `ECUC:c28329bc-8af9-4bdd-a16d-81b65be4a22c`
- **引用名**: `RteUsedOsAlarmRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `OsAlarm`
- **完整路径**: `/AUTOSAR/EcucDefs/Os/OsAlarm`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: If an OsAlarm is used to activate the OsTask this RteEvent is mapped to it shall be referenced here.

######## 3. RteUsedOsEventRef

- **UUID**: `ECUC:8eaae343-6715-4407-874e-952aeff8431f`
- **引用名**: `RteUsedOsEventRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `OsEvent`
- **完整路径**: `/AUTOSAR/EcucDefs/Os/OsEvent`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: If an OsEvent is used to activate the OsTask this RteEvent is mapped to it shall be referenced here.

######## 4. RteUsedOsSchTblExpiryPointRef

- **UUID**: `ECUC:67d1ea7b-8df0-41f1-801d-24406799eec2`
- **引用名**: `RteUsedOsSchTblExpiryPointRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `OsScheduleTableExpiryPoint`
- **完整路径**: `/AUTOSAR/EcucDefs/Os/OsScheduleTable/OsScheduleTableExpiryPoint`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: If an OsScheduleTableExpiryPoint is used to activate the OsTask this RteEvent is mapped to it shall be referenced here.

######## 5. RteVirtuallyMappedToTaskRef

- **UUID**: `ECUC:a06ca1ba-8541-416c-ae14-5b3024c55921`
- **引用名**: `RteVirtuallyMappedToTaskRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `OsTask`
- **完整路径**: `/AUTOSAR/EcucDefs/Os/OsTask`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Optional reference to an OsTask where the activation of this RteEvent shall be evaluated. The actual execution of the Runnable Entity shall happen in the OsTask referenced by RteMappedToTaskRef.

####### FOREIGN-REFERENCE 类型引用

######## 1. RteEventRef

- **UUID**: `ECUC:8b0a26ff-adfc-43ed-97c6-6dfb72faf07e`
- **引用名**: `RteEventRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [1..1]
- **目标类型**: RTE-EVENT
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the description of the RTEEvent which is pointing to the RunnableEntity being mapped. This allows a fine grained mapping of RunnableEntites based on the activating RTEEvent.

##### 20. RteExclusiveAreaImplementation

**容器属性**:

- **UUID**: `ECUC:22d2982b-ad5c-4732-8261-a8c4026fd219`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `RteExclusiveAreaImplementation`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

Specifies the implementation to be used for the data consistency of this ExclusiveArea.

###### 参数配置

此容器包含 **1** 个参数：

####### ENUMERATION 类型参数

######## 1. RteExclusiveAreaImplMechanism

- **UUID**: `ECUC:cfe28085-a28d-960f-3851-70ddf4bc2f18`
- **参数名**: `RteExclusiveAreaImplMechanism`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `ALL_INTERRUPT_BLOCKING` (来源: AUTOSAR_ECUC)
  - `COOPERATIVE_RUNNABLE_PLACEMENT` (来源: AUTOSAR_ECUC)
  - `OS_INTERRUPT_BLOCKING` (来源: AUTOSAR_ECUC)
  - `OS_RESOURCE` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: To be used implementation mechanism for the specified ExclusiveArea.

###### 引用关系

此容器包含 **2** 个引用：

####### REFERENCE 类型引用

######## 1. RteExclusiveAreaOsResourceRef

- **UUID**: `ECUC:4437449b-4726-45df-a6f9-e5140dac45a4`
- **引用名**: `RteExclusiveAreaOsResourceRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `OsResource`
- **完整路径**: `/AUTOSAR/EcucDefs/Os/OsResource`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Optional reference to an OsResource in case RteExclusiveAreaImplMechanism is configured to OS_RESOURCE for this ExclusiveArea.

####### FOREIGN-REFERENCE 类型引用

######## 1. RteExclusiveAreaRef

- **UUID**: `ECUC:d13b3e1d-b539-415e-b180-5f72e267eb09`
- **引用名**: `RteExclusiveAreaRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [1..1]
- **目标类型**: EXCLUSIVE-AREA
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the ExclusiveArea.

##### 21. RteExternalTriggerConfig

**容器属性**:

- **UUID**: `ECUC:492cd7c7-08bb-4d9f-b57b-93f101030d4a`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `RteExternalTriggerConfig`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

Defines the configuration of External Trigger Event Communication for Software Components

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. RteTriggerSourceQueueLength

- **UUID**: `ECUC:83b0c418-daae-4fa6-b9c9-f1278b727989`
- **参数名**: `RteTriggerSourceQueueLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Length of trigger queue on the trigger source side.

###### 引用关系

此容器包含 **1** 个引用：

####### INSTANCE-REFERENCE 类型引用

######## 1. RteSwcTriggerSourceRef

- **UUID**: `ECUC:6d1ba104-9581-4004-b55f-7452656565dc`
- **引用名**: `RteSwcTriggerSourceRef`
- **引用类型**: INSTANCE-REFERENCE
- **多重性**: [1..1]
- **目标类型**: TRIGGER
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a Trigger instance in the pPortPrototype of the related component instance.

##### 22. RteInternalTriggerConfig

**容器属性**:

- **UUID**: `ECUC:bf95436e-1855-4955-9f07-a5105a62d79c`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `RteInternalTriggerConfig`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

Defines the configuration of Inter Runnable Triggering for Software Components

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. RteTriggerSourceQueueLength

- **UUID**: `ECUC:14a2048e-17be-40d4-b994-b9381b1f5af5`
- **参数名**: `RteTriggerSourceQueueLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Length of trigger queue on the trigger source side.

###### 引用关系

此容器包含 **1** 个引用：

####### FOREIGN-REFERENCE 类型引用

######## 1. RteSwcTriggerSourceRef

- **UUID**: `ECUC:5ce6febf-7565-4312-81dc-ee600c9d93b7`
- **引用名**: `RteSwcTriggerSourceRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [1..1]
- **目标类型**: INTERNAL-TRIGGERING-POINT
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to an InternalTriggeringPoint of the related component instance.

##### 23. RteNvRamAllocation

**容器属性**:

- **UUID**: `ECUC:bdb010d2-a51d-4eca-b2db-cf0231f3e4dd`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `RteNvRamAllocation`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

Specifies the relationship between the AtomicSwComponentType's NVRAMMapping / NVRAM needs and the NvM module configuration.

###### 参数配置

此容器包含 **2** 个参数：

####### LINKER-SYMBOL 类型参数

######## 1. RteNvmRamBlockLocationSymbol

- **UUID**: `ECUC:36efd7d0-9100-4744-987f-65801a66367f`
- **参数名**: `RteNvmRamBlockLocationSymbol`
- **数据类型**: LINKER-SYMBOL
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is the name of the linker object name where the NVRam Block will be mirrored by the Nvm.

######## 2. RteNvmRomBlockLocationSymbol

- **UUID**: `ECUC:b47d9a23-fef1-4a6e-8659-08412478eb25`
- **参数名**: `RteNvmRomBlockLocationSymbol`
- **数据类型**: LINKER-SYMBOL
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is the name of the linker object name where the NVRom Block will be accessed by the Nvm.

###### 引用关系

此容器包含 **2** 个引用：

####### SYMBOLIC-NAME-REFERENCE 类型引用

######## 1. RteNvmBlockRef

- **UUID**: `ECUC:e23479f3-7fee-4246-8834-3d17d8ad9e2f`
- **引用名**: `RteNvmBlockRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `NvMBlockDescriptor`
- **完整路径**: `/AUTOSAR/EcucDefs/NvM/NvMBlockDescriptor`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the used NvM block for storage of the NVRAMMapping information.

####### FOREIGN-REFERENCE 类型引用

######## 1. RteSwNvRamMappingRef

- **UUID**: `ECUC:cdba0597-501f-41bc-8dbd-d87e73c056f3`
- **引用名**: `RteSwNvRamMappingRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [1..1]
- **目标类型**: SWC-SERVICE-DEPENDENCY
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the SwSeriveDependency which is used to specify the NvBlockNeeds.

##### 24. RteSwComponentType

**容器属性**:

- **UUID**: `ECUC:f14455b4-9c76-42db-9edd-fb506ce9ed5d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `RteSwComponentType`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

Representation of one SwComponentType for the base of all configuration parameter which are affecting the whole type and not a specific instance.

###### 引用关系

此容器包含 **2** 个引用：

####### FOREIGN-REFERENCE 类型引用

######## 1. RteComponentTypeRef

- **UUID**: `ECUC:cd4a4bd8-3991-476d-92d5-b70e5e06ccc0`
- **引用名**: `RteComponentTypeRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [1..1]
- **目标类型**: SW-COMPONENT-TYPE
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to either AtomicSwComponentType or ParameterSwComponentType.

######## 2. RteImplementationRef

- **UUID**: `ECUC:dc31ff20-0239-4fa1-87e8-3cc367dd94c7`
- **引用名**: `RteImplementationRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [0..1]
- **目标类型**: SWC-IMPLEMENTATION
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The Implementation which shall be assiged to the SwComponentType.

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. RteComponentTypeCalibration

**容器属性**:

- **UUID**: `ECUC:5e40d2d8-6d09-4118-a5cf-f0ebe34e59da`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `RteComponentTypeCalibration`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Specifies for each ParameterSwComponentType or AtomicSwComponentType whether calibration is enabled.

######## 参数配置

此容器包含 **1** 个参数：

######### BOOLEAN 类型参数

########## 1. RteCalibrationSupportEnabled

- **UUID**: `ECUC:6264b1ef-b235-4767-896d-42c14962a99a`
- **参数名**: `RteCalibrationSupportEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enables calibration support for the specified ParameterSwComponentType or AtomicSwComponentType.

######## 引用关系

此容器包含 **1** 个引用：

######### FOREIGN-REFERENCE 类型引用

########## 1. RteCalibrationSwAddrMethodRef

- **UUID**: `ECUC:f396ca1a-0cb3-4b87-a1dc-f2f7aca79926`
- **引用名**: `RteCalibrationSwAddrMethodRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [0..infinite]
- **目标类型**: SW-ADDR-METHOD
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the SwAddrMethod for which software calibration support shall be enabled.

##### 25. RteComponentTypeCalibration

**容器属性**:

- **UUID**: `ECUC:5e40d2d8-6d09-4118-a5cf-f0ebe34e59da`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `RteComponentTypeCalibration`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Specifies for each ParameterSwComponentType or AtomicSwComponentType whether calibration is enabled.

###### 参数配置

此容器包含 **1** 个参数：

####### BOOLEAN 类型参数

######## 1. RteCalibrationSupportEnabled

- **UUID**: `ECUC:6264b1ef-b235-4767-896d-42c14962a99a`
- **参数名**: `RteCalibrationSupportEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enables calibration support for the specified ParameterSwComponentType or AtomicSwComponentType.

###### 引用关系

此容器包含 **1** 个引用：

####### FOREIGN-REFERENCE 类型引用

######## 1. RteCalibrationSwAddrMethodRef

- **UUID**: `ECUC:f396ca1a-0cb3-4b87-a1dc-f2f7aca79926`
- **引用名**: `RteCalibrationSwAddrMethodRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [0..infinite]
- **目标类型**: SW-ADDR-METHOD
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the SwAddrMethod for which software calibration support shall be enabled.

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

1. **Rte**
