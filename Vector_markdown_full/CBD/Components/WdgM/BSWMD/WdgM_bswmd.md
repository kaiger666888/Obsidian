# WdgM - 完整配置文档

*此文档由ARXML文件自动生成，采用层次化结构展示*

**生成时间**: 2025-06-16 14:46:02

## 📑 目录

- [📄 文件信息](#-文件信息)
- [🔧 模块定义](#-模块定义)
  - [WdgM](#wdgm)
- [📦 包结构](#-包结构)
- [⚡ 实现信息](#-实现信息)
- [⚙️ 配置信息](#️-配置信息)

## 📄 文件信息

### Schema信息
- **Schema位置**: `http://autosar.org/schema/r4.0 AUTOSAR_4-0-3.xsd`
- **命名空间**: `http://autosar.org/schema/r4.0`

## 🔧 模块定义

### 1. WdgM

#### 基本信息

- **UUID**: `3d9e436f-54f3-45c6-882f-8c810c00ad7c`
- **模块名称**: `WdgM`
- **类别**: `VENDOR_SPECIFIC_MODULE_DEFINITION`
- **多重性**: [0..1]
- **支持的变体**:
  - VARIANT-PRE-COMPILE

#### 模块描述

Watchdog Manager. The manager supervises the program execution abstracting from the triggering of hardware watchdog entities (Supervised Entities).
When it detects a violation of the configured temporal and/ or logical constraints on program execution, it takes a number of configurable actions to recover from this failure.

#Safety #Supervision
#AUTOSAR #ServiceComponent

#### 版本历史

共有 **18** 个版本记录：

##### 1. 版本 5.00.00

- **状态**: released
- **发布日期**: 2016-02-16T03:38:30+01:00
- **发布者**: virchl

**变更内容**:

##### 2. 版本 6.00.00

- **状态**: released
- **发布日期**: 2016-03-22T04:20:49+01:00
- **发布者**: virchl

**变更内容**:

##### 3. 版本 6.00.01

- **状态**: released
- **发布日期**: 2016-07-29T10:37:00+02:00
- **发布者**: virchl

**变更内容**:

##### 4. 版本 6.00.02

- **状态**: released
- **发布日期**: 2016-08-08T04:55:42+02:00
- **发布者**: virchl

**变更内容**:

##### 5. 版本 6.00.03

- **状态**: released
- **发布日期**: 2016-10-11T07:53:50+02:00
- **发布者**: virchl

**变更内容**:

##### 6. 版本 6.01.00

- **状态**: released
- **发布日期**: 2017-02-22T04:44:25+01:00
- **发布者**: virchl

**变更内容**:

##### 7. 版本 6.01.01

- **状态**: released
- **发布日期**: 2017-10-25T15:39:33+02:00
- **发布者**: virchl

**变更内容**:

##### 8. 版本 6.01.02

- **状态**: released
- **发布日期**: 2018-04-10T10:31:05+02:00
- **发布者**: virchl

**变更内容**:

##### 9. 版本 6.02.00

- **状态**: released
- **发布日期**: 2018-04-24T09:03:51+02:00
- **发布者**: virchl

**变更内容**:

##### 10. 版本 6.02.01

- **状态**: released
- **发布日期**: 2018-12-18T08:56:05+01:00
- **发布者**: vircre

**变更内容**:

##### 11. 版本 6.03.00

- **状态**: released
- **发布日期**: 2019-07-12T10:28:58+02:00
- **发布者**: virbmz

**变更内容**:

##### 12. 版本 

- **状态**: released
- **发布日期**: 2019-07-25T10:31:13+02:00
- **发布者**: vircre

**变更内容**:

##### 13. 版本 6.03.01

- **状态**: released
- **发布日期**: 2019-11-29T10:55:39+01:00
- **发布者**: virsrl

**变更内容**:

##### 14. 版本 6.03.02

- **状态**: released
- **发布日期**: 2019-12-06T13:56:01+01:00
- **发布者**: virsrl

**变更内容**:

##### 15. 版本 6.03.03

- **状态**: released
- **发布日期**: 2020-08-17T17:03:13+02:00
- **发布者**: virbka

**变更内容**:

##### 16. 版本 6.03.04

- **状态**: released
- **发布日期**: 2020-11-25T12:38:30+01:00
- **发布者**: virsrl

**变更内容**:

##### 17. 版本 6.03.05

- **状态**: released
- **发布日期**: 2021-08-24T11:47:54+02:00
- **发布者**: virsrl

**变更内容**:

##### 18. 版本 6.03.06

- **状态**: released
- **发布日期**: 2021-12-13T13:09:34+01:00
- **发布者**: virsrl

**变更内容**:

#### 配置容器

本模块包含 **15** 个配置容器：

##### 1. WdgMConfigSet

**容器属性**:

- **UUID**: `2dbc28d5-018a-4415-8be7-da339d2a5b46`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `WdgMConfigSet`
- **多重性**: [1..1]
- **构建后可变**: false
- **多配置容器**: true

**容器描述**:

This container describes one of multiple configuration sets of WdgM.

This is a MultipleConfigurationContainer, i.e. this container and its sub-containers exist once per configuration set.

###### 引用关系

此容器包含 **1** 个引用：

####### SYMBOLIC-NAME-REFERENCE 类型引用

######## 1. WdgMInitialMode

- **UUID**: `418f2b84-5b5d-45ae-8319-ff5afb67a64d`
- **引用名**: `WdgMInitialMode`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `WdgMMode`
- **完整路径**: `/AUTOSAR/EcucDefs/WdgM/WdgMConfigSet/WdgMMode`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The mode that the Watchdog Manager is in after it has been initialized.

###### 配置容器

本模块包含 **8** 个配置容器：

####### 1. WdgMDemEventParameterRefs

**容器属性**:

- **UUID**: `56811dfb-d481-409f-b698-52b79aea9f8f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `WdgMDemEventParameterRefs`
- **多重性**: [0..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

Container for the references to DemEventParameter elements which shall be invoked using the API Dem_ReportErrorStatus API in case the corresponding error occurs. The EventId is taken from the referenced DemEventParameter's DemEventId value. The standardized errors are provided in the container and can be extended by vendor specific error references.

######## 引用关系

此容器包含 **3** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. WDGM_E_IMPROPER_CALLER

- **UUID**: `9d923b71-7742-4bf8-a0e7-a48ab9aec6d8`
- **引用名**: `WDGM_E_IMPROPER_CALLER`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `DemEventParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemConfigSet/DemEventParameter`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the DemEventParameter which shall be issued when the defensive behavior checks have detected an improper caller.

########## 2. WDGM_E_MONITORING

- **UUID**: `435446f1-e62b-45f6-8174-befa94529f1f`
- **引用名**: `WDGM_E_MONITORING`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `DemEventParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemConfigSet/DemEventParameter`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the DemEventParameter which shall be issued when the error "Monitoring has failed and a watchdog reset will occur" has occured.

########## 3. WDGM_E_SET_MODE

- **UUID**: `e175d039-9bc4-4f4d-9677-49f508c5bd9a`
- **引用名**: `WDGM_E_SET_MODE`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `DemEventParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemConfigSet/DemEventParameter`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Parameter not used.

Reference to the DemEventParameter which shall be issued when the error "Watchdog drivers' mode switch has failed" has occured.

####### 2. WdgMMode

**容器属性**:

- **UUID**: `e57d7de3-99ef-444c-bf4b-05ab61fcada5`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `WdgMMode`
- **多重性**: [1..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

The container describes one of several modes of the Watchdog Manager.

######## 参数配置

此容器包含 **8** 个参数：

######### INTEGER 类型参数

########## 1. WdgMExpiredSupervisionCycleTol

- **UUID**: `df12cf51-bd95-4777-80cf-afdcfa7baf3d`
- **参数名**: `WdgMExpiredSupervisionCycleTol`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter shall be used to define a value that fixes the amount of expired supervision cycles for how long the blocking of watchdog triggering shall be postponed.

########## 2. WdgMModeId

- **UUID**: `fb4a8d25-3b98-467d-a9ae-5d82bbb5ab2a`
- **参数名**: `WdgMModeId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter represents the WdgM mode.

########## 3. WdgMInitialTriggerModeId

- **UUID**: `93d2de70-0156-4bd7-b852-cd4c6b89cf07`
- **参数名**: `WdgMInitialTriggerModeId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..255]
- **来源**: Vector Informatik
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Denotes the ID of the Trigger Mode which shall be used at system start.

########## 4. WdgMModeCoreAssignment

- **UUID**: `212cac17-bb17-40ad-837b-277d032d7df5`
- **参数名**: `WdgMModeCoreAssignment`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..9]
- **来源**: Vector Informatik
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the assignment of configuration mode to a processor core ID. Maximal 10 cores are able to be used.

########## 5. WdgMTicksPerSecond

- **UUID**: `46824363-560a-40ef-b05f-e74dc6149d16`
- **参数名**: `WdgMTicksPerSecond`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the number of Watchdog Manager ticks per second.

######### BOOLEAN 类型参数

########## 1. WdgMReportStatusViaRte

- **UUID**: `985fdea7-9c8b-4faa-a5fd-17d9b4addaa8`
- **参数名**: `WdgMReportStatusViaRte`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter is used to enable the status reporting via Rte.

Notes:
- This parameter can only be set true if WdgMStatusReportingMechanism is _not_ WDGM_USE_NO_STATUS_REPORTING
- If this parameter is set true in any of the supervised entities or in WdgMMode, the global switch WdgMUseRte has to be set true, too.
- This parameter cannot be set true if global switch WdgMUseRte is set false.
- If this parameter is set true, the optional parameter WdgMGlobalStateChangeCbk must not exist.

######### FLOAT 类型参数

########## 1. WdgMSupervisionCycle

- **UUID**: `7afa4880-cddf-4a75-9f0e-4b8931d186b6`
- **参数名**: `WdgMSupervisionCycle`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0..1.7976931348623157E+308]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the period with which the main function (WdgM_MainFunction) is called.

######### FUNCTION-NAME 类型参数

########## 1. WdgMGlobalStateChangeCbk

- **UUID**: `f9df1e12-27fe-47e1-a544-a96c49652719`
- **参数名**: `WdgMGlobalStateChangeCbk`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Callback function for notifying Watchdog Manager global status change.

Note:
- This parameter can only be used if WdgMStatusReportingMechanism is set to WDGM_USE_NOTIFICATIONS.
- This parameter can only be used if parameter WdgMReportStatusViaRte of this WdgMMode is set false

######## 引用关系

此容器包含 **2** 个引用：

######### REFERENCE 类型引用

########## 1. WdgMOsCounterRef

- **UUID**: `8c278d8d-4132-4ade-8e9f-5566663e96d2`
- **引用名**: `WdgMOsCounterRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `OsCounter`
- **完整路径**: `/AUTOSAR/EcucDefs/Os/OsCounter`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the counter which shall be used for deadline monitoring.

######### CHOICE-REFERENCE 类型引用

########## 1. WdgMGlobalMemoryAppTaskRef

- **UUID**: `c5059eda-0e74-4f1d-bc42-99beef4e69f3`
- **引用名**: `WdgMGlobalMemoryAppTaskRef`
- **引用类型**: CHOICE-REFERENCE
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **需要索引**: false
- **目标引用列表**:
  - `/AUTOSAR/EcucDefs/Os/OsApplication`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to an OS Application where the WdgM is running. In case of OS SC3 (with memory protection) the global variables of the Watchdog Manager module should be placed in the same memory segment as the application in the context of which the Watchdog Manager is running.

######## 配置容器

本模块包含 **6** 个配置容器：

######### 1. WdgMAliveSupervision

**容器属性**:

- **UUID**: `17d83b33-4272-443a-aec7-7b73f961aed4`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `WdgMAliveSupervision`
- **多重性**: [0..65535]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container collects all configuration parameters of Alive-Supervision.

########## 参数配置

此容器包含 **4** 个参数：

########### INTEGER 类型参数

############ 1. WdgMExpectedAliveIndications

- **UUID**: `b565551d-d0c1-403e-85ca-6cd59f20d460`
- **参数名**: `WdgMExpectedAliveIndications`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter contains the amount of expected alive indications within the referenced amount of defined supervision cycles according to corresponding SE.

############ 2. WdgMMaxMargin

- **UUID**: `2bebf10e-04c2-4964-b4ba-31537ed41f5b`
- **参数名**: `WdgMMaxMargin`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter contains the amount of alive indications that are acceptable to be additional on the expected alive indications within the corresponding supervision reference cycle.

############ 3. WdgMMinMargin

- **UUID**: `b9ac601c-755d-4258-941d-fe67dc6a5131`
- **参数名**: `WdgMMinMargin`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter contains the amount of alive indications that are acceptable to be missed from the expected alive indications within the corresponding supervision reference cycle.

############ 4. WdgMSupervisionReferenceCycle

- **UUID**: `ef3e223c-a08c-4dab-89c7-0cb9e93c0594`
- **参数名**: `WdgMSupervisionReferenceCycle`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter contains the amount of supervision cycles to be used as reference by the alive-supervision mechanism to perform the checkup with counted alive indications according to corresponding SE.

########## 引用关系

此容器包含 **1** 个引用：

########### SYMBOLIC-NAME-REFERENCE 类型引用

############ 1. WdgMAliveSupervisionCheckpointRef

- **UUID**: `9c14cf8a-482d-4c4f-bbd3-7d8146c7703e`
- **引用名**: `WdgMAliveSupervisionCheckpointRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `WdgMCheckpoint`
- **完整路径**: `/AUTOSAR/EcucDefs/WdgM/WdgMGeneral/WdgMSupervisedEntity/WdgMCheckpoint`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the Checkpoint for which this alive counter is configured.

######### 2. WdgMDeadlineSupervision

**容器属性**:

- **UUID**: `31e680b5-fc6f-4feb-8c70-ddce7d29784a`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `WdgMDeadlineSupervision`
- **多重性**: [0..65535]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container collects all configuration parameters for Deadline Monitoring for a Supervised Entity.

########## 参数配置

此容器包含 **2** 个参数：

########### FLOAT 类型参数

############ 1. WdgMDeadlineMax

- **UUID**: `79cf6acd-1479-4a4b-9c25-5ac54b58afff`
- **参数名**: `WdgMDeadlineMax`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0.0..1.7976931348623157E+308]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter contains the longest time span after which the deadline is considered to be met.

############ 2. WdgMDeadlineMin

- **UUID**: `6bd050aa-5a0b-4266-a5dd-aac1c9b024c3`
- **参数名**: `WdgMDeadlineMin`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0.0..1.7976931348623157E+308]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter contains the shortest time span after which the deadline is considered to be met.

########## 引用关系

此容器包含 **2** 个引用：

########### SYMBOLIC-NAME-REFERENCE 类型引用

############ 1. WdgMDeadlineStartRef

- **UUID**: `447ca545-4f72-4dfc-b437-c7589ddcdb33`
- **引用名**: `WdgMDeadlineStartRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `WdgMCheckpoint`
- **完整路径**: `/AUTOSAR/EcucDefs/WdgM/WdgMGeneral/WdgMSupervisedEntity/WdgMCheckpoint`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is the reference to the start Checkpoint for Deadline Monitoring.

############ 2. WdgMDeadlineStopRef

- **UUID**: `ebe91d65-d95b-46ec-bf8f-a96848d151a2`
- **引用名**: `WdgMDeadlineStopRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `WdgMCheckpoint`
- **完整路径**: `/AUTOSAR/EcucDefs/WdgM/WdgMGeneral/WdgMSupervisedEntity/WdgMCheckpoint`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is the reference to the stop Checkpoint for Deadline Monitoring. Note that the deadline's start and stop references must match an existing local or a global transition.

######### 3. WdgMExternalLogicalSupervision

**容器属性**:

- **UUID**: `a7389008-8797-4ff3-8c29-3001838dfb32`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `WdgMExternalLogicalSupervision`
- **多重性**: [0..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container collects all configuration parameters for Logical Supervision for one external graph.

########## 引用关系

此容器包含 **2** 个引用：

########### SYMBOLIC-NAME-REFERENCE 类型引用

############ 1. WdgMExternalCheckpointFinalRef

- **UUID**: `54303b7c-9f68-4443-8e78-1cf288f293bd`
- **引用名**: `WdgMExternalCheckpointFinalRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..65535]
- **目标**: `WdgMCheckpoint`
- **完整路径**: `/AUTOSAR/EcucDefs/WdgM/WdgMGeneral/WdgMSupervisedEntity/WdgMCheckpoint`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: A reference to the final global Checkpoint. Note that there might be several final global checkpoints.

############ 2. WdgMExternalCheckpointInitialRef

- **UUID**: `52370a40-da98-40cc-8349-b36730e48f59`
- **引用名**: `WdgMExternalCheckpointInitialRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `WdgMCheckpoint`
- **完整路径**: `/AUTOSAR/EcucDefs/WdgM/WdgMGeneral/WdgMSupervisedEntity/WdgMCheckpoint`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: A reference to the global initial Checkpoint.

########## 配置容器

本模块包含 **1** 个配置容器：

########### 1. WdgMExternalTransition

**容器属性**:

- **UUID**: `9a8e9a25-92e4-435a-810f-5fd323edd887`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `WdgMExternalTransition`
- **多重性**: [0..65535]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container collects the Checkpoints for a Global Transition across Supervised Entities.

############ 引用关系

此容器包含 **2** 个引用：

############# SYMBOLIC-NAME-REFERENCE 类型引用

############## 1. WdgMExternalTransitionDestRef

- **UUID**: `738ec705-b880-4260-815c-fe7e06deb8c6`
- **引用名**: `WdgMExternalTransitionDestRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `WdgMCheckpoint`
- **完整路径**: `/AUTOSAR/EcucDefs/WdgM/WdgMGeneral/WdgMSupervisedEntity/WdgMCheckpoint`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is the reference to the destination Checkpoint of an External Transition.

############## 2. WdgMExternalTransitionSourceRef

- **UUID**: `cef4db25-a448-4795-866b-fec00a586aa4`
- **引用名**: `WdgMExternalTransitionSourceRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `WdgMCheckpoint`
- **完整路径**: `/AUTOSAR/EcucDefs/WdgM/WdgMGeneral/WdgMSupervisedEntity/WdgMCheckpoint`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is the reference to the source Checkpoint of an External Transition.

######### 4. WdgMExternalTransition

**容器属性**:

- **UUID**: `9a8e9a25-92e4-435a-810f-5fd323edd887`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `WdgMExternalTransition`
- **多重性**: [0..65535]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container collects the Checkpoints for a Global Transition across Supervised Entities.

########## 引用关系

此容器包含 **2** 个引用：

########### SYMBOLIC-NAME-REFERENCE 类型引用

############ 1. WdgMExternalTransitionDestRef

- **UUID**: `738ec705-b880-4260-815c-fe7e06deb8c6`
- **引用名**: `WdgMExternalTransitionDestRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `WdgMCheckpoint`
- **完整路径**: `/AUTOSAR/EcucDefs/WdgM/WdgMGeneral/WdgMSupervisedEntity/WdgMCheckpoint`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is the reference to the destination Checkpoint of an External Transition.

############ 2. WdgMExternalTransitionSourceRef

- **UUID**: `cef4db25-a448-4795-866b-fec00a586aa4`
- **引用名**: `WdgMExternalTransitionSourceRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `WdgMCheckpoint`
- **完整路径**: `/AUTOSAR/EcucDefs/WdgM/WdgMGeneral/WdgMSupervisedEntity/WdgMCheckpoint`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is the reference to the source Checkpoint of an External Transition.

######### 5. WdgMTrigger

**容器属性**:

- **UUID**: `e5f8eed7-2309-4f4a-a169-be93791bfa92`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `WdgMTrigger`
- **多重性**: [0..255]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container collects all configuration parameters for the triggering of hardware watchdogs.

########## 参数配置

此容器包含 **3** 个参数：

########### INTEGER 类型参数

############ 1. WdgMTriggerConditionValue

- **UUID**: `292ee535-f62c-45eb-b0d2-df847155bf47`
- **参数名**: `WdgMTriggerConditionValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the maximum possible trigger time where the watchdog trigger is accepted. The consumer of this parameter is the WdgIf_SetTriggerCondition for the corresponding watchdog.

############ 2. WdgMTriggerModeId

- **UUID**: `3a676183-68c1-4bdd-9231-ebf1ec194573`
- **参数名**: `WdgMTriggerModeId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..254]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter contains a unique identifier of the trigger mode.

########### ENUMERATION 类型参数

############ 1. WdgMWatchdogMode

- **UUID**: `74c429ed-60d9-4ff6-a274-d3a5f0d8641d`
- **参数名**: `WdgMWatchdogMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `WDGIF_FAST_MODE`
  - `WDGIF_OFF_MODE`
  - `WDGIF_SLOW_MODE`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter contains the watchdog mode that shall be used for the referenced watchdog in this Watchdog Manager mode.

Implementation Type: WdgIf_ModeType

########## 引用关系

此容器包含 **1** 个引用：

########### SYMBOLIC-NAME-REFERENCE 类型引用

############ 1. WdgMTriggerWatchdogRef

- **UUID**: `82b5c6db-c67b-4cb1-a1d4-6997e8c52b8c`
- **引用名**: `WdgMTriggerWatchdogRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `WdgMWatchdog`
- **完整路径**: `/AUTOSAR/EcucDefs/WdgM/WdgMGeneral/WdgMWatchdog`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter is a reference to the configured watchdog.

######### 6. WdgMLocalStatusParams

**容器属性**:

- **UUID**: `c5f89145-ad15-4030-a200-d8f0a856d560`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `WdgMLocalStatusParams`
- **多重性**: [0..65535]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container collects all configuration parameters for the Local Status of a Supervised Entity.

########## 参数配置

此容器包含 **6** 个参数：

########### INTEGER 类型参数

############ 1. WdgMFailedAliveSupervisionRefCycleTol

- **UUID**: `d4b7363f-b318-455b-9aaf-15b410e26324`
- **参数名**: `WdgMFailedAliveSupervisionRefCycleTol`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65534]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter contains the acceptable amount of failed alive supervisions for this Supervised Entity

############ 2. WdgMFailedDeadlineRefCycleTol

- **UUID**: `dbaaf237-fcfe-4d0e-a567-8fdd590b64f0`
- **参数名**: `WdgMFailedDeadlineRefCycleTol`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65534]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter contains the acceptable amount of violated deadlines for this Supervised Entity.

Note:
The AUTOSAR implementation can be simulated for deadline violations with:
WdgMDeadlineReferenceCycle = WdgMFailedDeadlineRefCycleTol = 0

############ 3. WdgMDeadlineReferenceCycle

- **UUID**: `29479764-7332-433e-9ae3-302a69463d7c`
- **参数名**: `WdgMDeadlineReferenceCycle`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter contains the amount of supervision cycles to be used as reference by the deadline supervisions of this SE.

Note:
The AUTOSAR implementation can be simulated for deadline violations with:
WdgMDeadlineReferenceCycle = WdgMFailedDeadlineRefCycleTol = 0

############ 4. WdgMFailedProgramFlowRefCycleTol

- **UUID**: `aacd8d0f-b112-4136-b5aa-71b245ec77be`
- **参数名**: `WdgMFailedProgramFlowRefCycleTol`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65534]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter contains the acceptable amount of program flow violations for this Supervised Entity.

Note:
The AUTOSAR implementation can be simulated for program flow violations with:
WdgMProgramFlowReferenceCycle = WdgMFailedProgramFlowRefCycleTol = 0

############ 5. WdgMProgramFlowReferenceCycle

- **UUID**: `8e0e4ba9-4606-45d1-a855-a7ca85cef560`
- **参数名**: `WdgMProgramFlowReferenceCycle`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter contains the amount of supervision cycles to be used as reference by the program flow supervisions of this SE.

Note:
The AUTOSAR implementation can be simulated for program flow violations with:
WdgMProgramFlowReferenceCycle = WdgMFailedProgramFlowRefCycleTol = 0

########### ENUMERATION 类型参数

############ 1. WdgMSupervisedEntityInitialMode

- **UUID**: `185cccc7-8eeb-4932-a6d2-f52784aaa8e4`
- **参数名**: `WdgMSupervisedEntityInitialMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `WDGM_LOCAL_STATUS_OK`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `WDGM_LOCAL_STATUS_DEACTIVATED`
  - `WDGM_LOCAL_STATUS_OK`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Initial local monitoring status of the supervised entity.

########## 引用关系

此容器包含 **1** 个引用：

########### SYMBOLIC-NAME-REFERENCE 类型引用

############ 1. WdgMLocalStatusSupervisedEntityRef

- **UUID**: `f347f1b1-b1c9-454e-8d3f-045f2daf60e5`
- **引用名**: `WdgMLocalStatusSupervisedEntityRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `WdgMSupervisedEntity`
- **完整路径**: `/AUTOSAR/EcucDefs/WdgM/WdgMGeneral/WdgMSupervisedEntity`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the Supervised Entity for which the parameters of this container are set.

####### 3. WdgMAliveSupervision

**容器属性**:

- **UUID**: `17d83b33-4272-443a-aec7-7b73f961aed4`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `WdgMAliveSupervision`
- **多重性**: [0..65535]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container collects all configuration parameters of Alive-Supervision.

######## 参数配置

此容器包含 **4** 个参数：

######### INTEGER 类型参数

########## 1. WdgMExpectedAliveIndications

- **UUID**: `b565551d-d0c1-403e-85ca-6cd59f20d460`
- **参数名**: `WdgMExpectedAliveIndications`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter contains the amount of expected alive indications within the referenced amount of defined supervision cycles according to corresponding SE.

########## 2. WdgMMaxMargin

- **UUID**: `2bebf10e-04c2-4964-b4ba-31537ed41f5b`
- **参数名**: `WdgMMaxMargin`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter contains the amount of alive indications that are acceptable to be additional on the expected alive indications within the corresponding supervision reference cycle.

########## 3. WdgMMinMargin

- **UUID**: `b9ac601c-755d-4258-941d-fe67dc6a5131`
- **参数名**: `WdgMMinMargin`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter contains the amount of alive indications that are acceptable to be missed from the expected alive indications within the corresponding supervision reference cycle.

########## 4. WdgMSupervisionReferenceCycle

- **UUID**: `ef3e223c-a08c-4dab-89c7-0cb9e93c0594`
- **参数名**: `WdgMSupervisionReferenceCycle`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter contains the amount of supervision cycles to be used as reference by the alive-supervision mechanism to perform the checkup with counted alive indications according to corresponding SE.

######## 引用关系

此容器包含 **1** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. WdgMAliveSupervisionCheckpointRef

- **UUID**: `9c14cf8a-482d-4c4f-bbd3-7d8146c7703e`
- **引用名**: `WdgMAliveSupervisionCheckpointRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `WdgMCheckpoint`
- **完整路径**: `/AUTOSAR/EcucDefs/WdgM/WdgMGeneral/WdgMSupervisedEntity/WdgMCheckpoint`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the Checkpoint for which this alive counter is configured.

####### 4. WdgMDeadlineSupervision

**容器属性**:

- **UUID**: `31e680b5-fc6f-4feb-8c70-ddce7d29784a`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `WdgMDeadlineSupervision`
- **多重性**: [0..65535]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container collects all configuration parameters for Deadline Monitoring for a Supervised Entity.

######## 参数配置

此容器包含 **2** 个参数：

######### FLOAT 类型参数

########## 1. WdgMDeadlineMax

- **UUID**: `79cf6acd-1479-4a4b-9c25-5ac54b58afff`
- **参数名**: `WdgMDeadlineMax`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0.0..1.7976931348623157E+308]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter contains the longest time span after which the deadline is considered to be met.

########## 2. WdgMDeadlineMin

- **UUID**: `6bd050aa-5a0b-4266-a5dd-aac1c9b024c3`
- **参数名**: `WdgMDeadlineMin`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0.0..1.7976931348623157E+308]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter contains the shortest time span after which the deadline is considered to be met.

######## 引用关系

此容器包含 **2** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. WdgMDeadlineStartRef

- **UUID**: `447ca545-4f72-4dfc-b437-c7589ddcdb33`
- **引用名**: `WdgMDeadlineStartRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `WdgMCheckpoint`
- **完整路径**: `/AUTOSAR/EcucDefs/WdgM/WdgMGeneral/WdgMSupervisedEntity/WdgMCheckpoint`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is the reference to the start Checkpoint for Deadline Monitoring.

########## 2. WdgMDeadlineStopRef

- **UUID**: `ebe91d65-d95b-46ec-bf8f-a96848d151a2`
- **引用名**: `WdgMDeadlineStopRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `WdgMCheckpoint`
- **完整路径**: `/AUTOSAR/EcucDefs/WdgM/WdgMGeneral/WdgMSupervisedEntity/WdgMCheckpoint`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is the reference to the stop Checkpoint for Deadline Monitoring. Note that the deadline's start and stop references must match an existing local or a global transition.

####### 5. WdgMExternalLogicalSupervision

**容器属性**:

- **UUID**: `a7389008-8797-4ff3-8c29-3001838dfb32`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `WdgMExternalLogicalSupervision`
- **多重性**: [0..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container collects all configuration parameters for Logical Supervision for one external graph.

######## 引用关系

此容器包含 **2** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. WdgMExternalCheckpointFinalRef

- **UUID**: `54303b7c-9f68-4443-8e78-1cf288f293bd`
- **引用名**: `WdgMExternalCheckpointFinalRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..65535]
- **目标**: `WdgMCheckpoint`
- **完整路径**: `/AUTOSAR/EcucDefs/WdgM/WdgMGeneral/WdgMSupervisedEntity/WdgMCheckpoint`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: A reference to the final global Checkpoint. Note that there might be several final global checkpoints.

########## 2. WdgMExternalCheckpointInitialRef

- **UUID**: `52370a40-da98-40cc-8349-b36730e48f59`
- **引用名**: `WdgMExternalCheckpointInitialRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `WdgMCheckpoint`
- **完整路径**: `/AUTOSAR/EcucDefs/WdgM/WdgMGeneral/WdgMSupervisedEntity/WdgMCheckpoint`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: A reference to the global initial Checkpoint.

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. WdgMExternalTransition

**容器属性**:

- **UUID**: `9a8e9a25-92e4-435a-810f-5fd323edd887`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `WdgMExternalTransition`
- **多重性**: [0..65535]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container collects the Checkpoints for a Global Transition across Supervised Entities.

########## 引用关系

此容器包含 **2** 个引用：

########### SYMBOLIC-NAME-REFERENCE 类型引用

############ 1. WdgMExternalTransitionDestRef

- **UUID**: `738ec705-b880-4260-815c-fe7e06deb8c6`
- **引用名**: `WdgMExternalTransitionDestRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `WdgMCheckpoint`
- **完整路径**: `/AUTOSAR/EcucDefs/WdgM/WdgMGeneral/WdgMSupervisedEntity/WdgMCheckpoint`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is the reference to the destination Checkpoint of an External Transition.

############ 2. WdgMExternalTransitionSourceRef

- **UUID**: `cef4db25-a448-4795-866b-fec00a586aa4`
- **引用名**: `WdgMExternalTransitionSourceRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `WdgMCheckpoint`
- **完整路径**: `/AUTOSAR/EcucDefs/WdgM/WdgMGeneral/WdgMSupervisedEntity/WdgMCheckpoint`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is the reference to the source Checkpoint of an External Transition.

####### 6. WdgMExternalTransition

**容器属性**:

- **UUID**: `9a8e9a25-92e4-435a-810f-5fd323edd887`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `WdgMExternalTransition`
- **多重性**: [0..65535]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container collects the Checkpoints for a Global Transition across Supervised Entities.

######## 引用关系

此容器包含 **2** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. WdgMExternalTransitionDestRef

- **UUID**: `738ec705-b880-4260-815c-fe7e06deb8c6`
- **引用名**: `WdgMExternalTransitionDestRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `WdgMCheckpoint`
- **完整路径**: `/AUTOSAR/EcucDefs/WdgM/WdgMGeneral/WdgMSupervisedEntity/WdgMCheckpoint`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is the reference to the destination Checkpoint of an External Transition.

########## 2. WdgMExternalTransitionSourceRef

- **UUID**: `cef4db25-a448-4795-866b-fec00a586aa4`
- **引用名**: `WdgMExternalTransitionSourceRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `WdgMCheckpoint`
- **完整路径**: `/AUTOSAR/EcucDefs/WdgM/WdgMGeneral/WdgMSupervisedEntity/WdgMCheckpoint`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is the reference to the source Checkpoint of an External Transition.

####### 7. WdgMTrigger

**容器属性**:

- **UUID**: `e5f8eed7-2309-4f4a-a169-be93791bfa92`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `WdgMTrigger`
- **多重性**: [0..255]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container collects all configuration parameters for the triggering of hardware watchdogs.

######## 参数配置

此容器包含 **3** 个参数：

######### INTEGER 类型参数

########## 1. WdgMTriggerConditionValue

- **UUID**: `292ee535-f62c-45eb-b0d2-df847155bf47`
- **参数名**: `WdgMTriggerConditionValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the maximum possible trigger time where the watchdog trigger is accepted. The consumer of this parameter is the WdgIf_SetTriggerCondition for the corresponding watchdog.

########## 2. WdgMTriggerModeId

- **UUID**: `3a676183-68c1-4bdd-9231-ebf1ec194573`
- **参数名**: `WdgMTriggerModeId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..254]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter contains a unique identifier of the trigger mode.

######### ENUMERATION 类型参数

########## 1. WdgMWatchdogMode

- **UUID**: `74c429ed-60d9-4ff6-a274-d3a5f0d8641d`
- **参数名**: `WdgMWatchdogMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `WDGIF_FAST_MODE`
  - `WDGIF_OFF_MODE`
  - `WDGIF_SLOW_MODE`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter contains the watchdog mode that shall be used for the referenced watchdog in this Watchdog Manager mode.

Implementation Type: WdgIf_ModeType

######## 引用关系

此容器包含 **1** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. WdgMTriggerWatchdogRef

- **UUID**: `82b5c6db-c67b-4cb1-a1d4-6997e8c52b8c`
- **引用名**: `WdgMTriggerWatchdogRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `WdgMWatchdog`
- **完整路径**: `/AUTOSAR/EcucDefs/WdgM/WdgMGeneral/WdgMWatchdog`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter is a reference to the configured watchdog.

####### 8. WdgMLocalStatusParams

**容器属性**:

- **UUID**: `c5f89145-ad15-4030-a200-d8f0a856d560`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `WdgMLocalStatusParams`
- **多重性**: [0..65535]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container collects all configuration parameters for the Local Status of a Supervised Entity.

######## 参数配置

此容器包含 **6** 个参数：

######### INTEGER 类型参数

########## 1. WdgMFailedAliveSupervisionRefCycleTol

- **UUID**: `d4b7363f-b318-455b-9aaf-15b410e26324`
- **参数名**: `WdgMFailedAliveSupervisionRefCycleTol`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65534]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter contains the acceptable amount of failed alive supervisions for this Supervised Entity

########## 2. WdgMFailedDeadlineRefCycleTol

- **UUID**: `dbaaf237-fcfe-4d0e-a567-8fdd590b64f0`
- **参数名**: `WdgMFailedDeadlineRefCycleTol`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65534]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter contains the acceptable amount of violated deadlines for this Supervised Entity.

Note:
The AUTOSAR implementation can be simulated for deadline violations with:
WdgMDeadlineReferenceCycle = WdgMFailedDeadlineRefCycleTol = 0

########## 3. WdgMDeadlineReferenceCycle

- **UUID**: `29479764-7332-433e-9ae3-302a69463d7c`
- **参数名**: `WdgMDeadlineReferenceCycle`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter contains the amount of supervision cycles to be used as reference by the deadline supervisions of this SE.

Note:
The AUTOSAR implementation can be simulated for deadline violations with:
WdgMDeadlineReferenceCycle = WdgMFailedDeadlineRefCycleTol = 0

########## 4. WdgMFailedProgramFlowRefCycleTol

- **UUID**: `aacd8d0f-b112-4136-b5aa-71b245ec77be`
- **参数名**: `WdgMFailedProgramFlowRefCycleTol`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65534]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter contains the acceptable amount of program flow violations for this Supervised Entity.

Note:
The AUTOSAR implementation can be simulated for program flow violations with:
WdgMProgramFlowReferenceCycle = WdgMFailedProgramFlowRefCycleTol = 0

########## 5. WdgMProgramFlowReferenceCycle

- **UUID**: `8e0e4ba9-4606-45d1-a855-a7ca85cef560`
- **参数名**: `WdgMProgramFlowReferenceCycle`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter contains the amount of supervision cycles to be used as reference by the program flow supervisions of this SE.

Note:
The AUTOSAR implementation can be simulated for program flow violations with:
WdgMProgramFlowReferenceCycle = WdgMFailedProgramFlowRefCycleTol = 0

######### ENUMERATION 类型参数

########## 1. WdgMSupervisedEntityInitialMode

- **UUID**: `185cccc7-8eeb-4932-a6d2-f52784aaa8e4`
- **参数名**: `WdgMSupervisedEntityInitialMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `WDGM_LOCAL_STATUS_OK`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `WDGM_LOCAL_STATUS_DEACTIVATED`
  - `WDGM_LOCAL_STATUS_OK`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Initial local monitoring status of the supervised entity.

######## 引用关系

此容器包含 **1** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. WdgMLocalStatusSupervisedEntityRef

- **UUID**: `f347f1b1-b1c9-454e-8d3f-045f2daf60e5`
- **引用名**: `WdgMLocalStatusSupervisedEntityRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `WdgMSupervisedEntity`
- **完整路径**: `/AUTOSAR/EcucDefs/WdgM/WdgMGeneral/WdgMSupervisedEntity`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the Supervised Entity for which the parameters of this container are set.

##### 2. WdgMDemEventParameterRefs

**容器属性**:

- **UUID**: `56811dfb-d481-409f-b698-52b79aea9f8f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `WdgMDemEventParameterRefs`
- **多重性**: [0..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

Container for the references to DemEventParameter elements which shall be invoked using the API Dem_ReportErrorStatus API in case the corresponding error occurs. The EventId is taken from the referenced DemEventParameter's DemEventId value. The standardized errors are provided in the container and can be extended by vendor specific error references.

###### 引用关系

此容器包含 **3** 个引用：

####### SYMBOLIC-NAME-REFERENCE 类型引用

######## 1. WDGM_E_IMPROPER_CALLER

- **UUID**: `9d923b71-7742-4bf8-a0e7-a48ab9aec6d8`
- **引用名**: `WDGM_E_IMPROPER_CALLER`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `DemEventParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemConfigSet/DemEventParameter`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the DemEventParameter which shall be issued when the defensive behavior checks have detected an improper caller.

######## 2. WDGM_E_MONITORING

- **UUID**: `435446f1-e62b-45f6-8174-befa94529f1f`
- **引用名**: `WDGM_E_MONITORING`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `DemEventParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemConfigSet/DemEventParameter`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the DemEventParameter which shall be issued when the error "Monitoring has failed and a watchdog reset will occur" has occured.

######## 3. WDGM_E_SET_MODE

- **UUID**: `e175d039-9bc4-4f4d-9677-49f508c5bd9a`
- **引用名**: `WDGM_E_SET_MODE`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `DemEventParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemConfigSet/DemEventParameter`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Parameter not used.

Reference to the DemEventParameter which shall be issued when the error "Watchdog drivers' mode switch has failed" has occured.

##### 3. WdgMMode

**容器属性**:

- **UUID**: `e57d7de3-99ef-444c-bf4b-05ab61fcada5`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `WdgMMode`
- **多重性**: [1..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

The container describes one of several modes of the Watchdog Manager.

###### 参数配置

此容器包含 **8** 个参数：

####### INTEGER 类型参数

######## 1. WdgMExpiredSupervisionCycleTol

- **UUID**: `df12cf51-bd95-4777-80cf-afdcfa7baf3d`
- **参数名**: `WdgMExpiredSupervisionCycleTol`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter shall be used to define a value that fixes the amount of expired supervision cycles for how long the blocking of watchdog triggering shall be postponed.

######## 2. WdgMModeId

- **UUID**: `fb4a8d25-3b98-467d-a9ae-5d82bbb5ab2a`
- **参数名**: `WdgMModeId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter represents the WdgM mode.

######## 3. WdgMInitialTriggerModeId

- **UUID**: `93d2de70-0156-4bd7-b852-cd4c6b89cf07`
- **参数名**: `WdgMInitialTriggerModeId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..255]
- **来源**: Vector Informatik
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Denotes the ID of the Trigger Mode which shall be used at system start.

######## 4. WdgMModeCoreAssignment

- **UUID**: `212cac17-bb17-40ad-837b-277d032d7df5`
- **参数名**: `WdgMModeCoreAssignment`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..9]
- **来源**: Vector Informatik
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the assignment of configuration mode to a processor core ID. Maximal 10 cores are able to be used.

######## 5. WdgMTicksPerSecond

- **UUID**: `46824363-560a-40ef-b05f-e74dc6149d16`
- **参数名**: `WdgMTicksPerSecond`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the number of Watchdog Manager ticks per second.

####### BOOLEAN 类型参数

######## 1. WdgMReportStatusViaRte

- **UUID**: `985fdea7-9c8b-4faa-a5fd-17d9b4addaa8`
- **参数名**: `WdgMReportStatusViaRte`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter is used to enable the status reporting via Rte.

Notes:
- This parameter can only be set true if WdgMStatusReportingMechanism is _not_ WDGM_USE_NO_STATUS_REPORTING
- If this parameter is set true in any of the supervised entities or in WdgMMode, the global switch WdgMUseRte has to be set true, too.
- This parameter cannot be set true if global switch WdgMUseRte is set false.
- If this parameter is set true, the optional parameter WdgMGlobalStateChangeCbk must not exist.

####### FLOAT 类型参数

######## 1. WdgMSupervisionCycle

- **UUID**: `7afa4880-cddf-4a75-9f0e-4b8931d186b6`
- **参数名**: `WdgMSupervisionCycle`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0..1.7976931348623157E+308]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the period with which the main function (WdgM_MainFunction) is called.

####### FUNCTION-NAME 类型参数

######## 1. WdgMGlobalStateChangeCbk

- **UUID**: `f9df1e12-27fe-47e1-a544-a96c49652719`
- **参数名**: `WdgMGlobalStateChangeCbk`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Callback function for notifying Watchdog Manager global status change.

Note:
- This parameter can only be used if WdgMStatusReportingMechanism is set to WDGM_USE_NOTIFICATIONS.
- This parameter can only be used if parameter WdgMReportStatusViaRte of this WdgMMode is set false

###### 引用关系

此容器包含 **2** 个引用：

####### REFERENCE 类型引用

######## 1. WdgMOsCounterRef

- **UUID**: `8c278d8d-4132-4ade-8e9f-5566663e96d2`
- **引用名**: `WdgMOsCounterRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `OsCounter`
- **完整路径**: `/AUTOSAR/EcucDefs/Os/OsCounter`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the counter which shall be used for deadline monitoring.

####### CHOICE-REFERENCE 类型引用

######## 1. WdgMGlobalMemoryAppTaskRef

- **UUID**: `c5059eda-0e74-4f1d-bc42-99beef4e69f3`
- **引用名**: `WdgMGlobalMemoryAppTaskRef`
- **引用类型**: CHOICE-REFERENCE
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **需要索引**: false
- **目标引用列表**:
  - `/AUTOSAR/EcucDefs/Os/OsApplication`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to an OS Application where the WdgM is running. In case of OS SC3 (with memory protection) the global variables of the Watchdog Manager module should be placed in the same memory segment as the application in the context of which the Watchdog Manager is running.

###### 配置容器

本模块包含 **6** 个配置容器：

####### 1. WdgMAliveSupervision

**容器属性**:

- **UUID**: `17d83b33-4272-443a-aec7-7b73f961aed4`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `WdgMAliveSupervision`
- **多重性**: [0..65535]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container collects all configuration parameters of Alive-Supervision.

######## 参数配置

此容器包含 **4** 个参数：

######### INTEGER 类型参数

########## 1. WdgMExpectedAliveIndications

- **UUID**: `b565551d-d0c1-403e-85ca-6cd59f20d460`
- **参数名**: `WdgMExpectedAliveIndications`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter contains the amount of expected alive indications within the referenced amount of defined supervision cycles according to corresponding SE.

########## 2. WdgMMaxMargin

- **UUID**: `2bebf10e-04c2-4964-b4ba-31537ed41f5b`
- **参数名**: `WdgMMaxMargin`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter contains the amount of alive indications that are acceptable to be additional on the expected alive indications within the corresponding supervision reference cycle.

########## 3. WdgMMinMargin

- **UUID**: `b9ac601c-755d-4258-941d-fe67dc6a5131`
- **参数名**: `WdgMMinMargin`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter contains the amount of alive indications that are acceptable to be missed from the expected alive indications within the corresponding supervision reference cycle.

########## 4. WdgMSupervisionReferenceCycle

- **UUID**: `ef3e223c-a08c-4dab-89c7-0cb9e93c0594`
- **参数名**: `WdgMSupervisionReferenceCycle`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter contains the amount of supervision cycles to be used as reference by the alive-supervision mechanism to perform the checkup with counted alive indications according to corresponding SE.

######## 引用关系

此容器包含 **1** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. WdgMAliveSupervisionCheckpointRef

- **UUID**: `9c14cf8a-482d-4c4f-bbd3-7d8146c7703e`
- **引用名**: `WdgMAliveSupervisionCheckpointRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `WdgMCheckpoint`
- **完整路径**: `/AUTOSAR/EcucDefs/WdgM/WdgMGeneral/WdgMSupervisedEntity/WdgMCheckpoint`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the Checkpoint for which this alive counter is configured.

####### 2. WdgMDeadlineSupervision

**容器属性**:

- **UUID**: `31e680b5-fc6f-4feb-8c70-ddce7d29784a`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `WdgMDeadlineSupervision`
- **多重性**: [0..65535]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container collects all configuration parameters for Deadline Monitoring for a Supervised Entity.

######## 参数配置

此容器包含 **2** 个参数：

######### FLOAT 类型参数

########## 1. WdgMDeadlineMax

- **UUID**: `79cf6acd-1479-4a4b-9c25-5ac54b58afff`
- **参数名**: `WdgMDeadlineMax`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0.0..1.7976931348623157E+308]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter contains the longest time span after which the deadline is considered to be met.

########## 2. WdgMDeadlineMin

- **UUID**: `6bd050aa-5a0b-4266-a5dd-aac1c9b024c3`
- **参数名**: `WdgMDeadlineMin`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0.0..1.7976931348623157E+308]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter contains the shortest time span after which the deadline is considered to be met.

######## 引用关系

此容器包含 **2** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. WdgMDeadlineStartRef

- **UUID**: `447ca545-4f72-4dfc-b437-c7589ddcdb33`
- **引用名**: `WdgMDeadlineStartRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `WdgMCheckpoint`
- **完整路径**: `/AUTOSAR/EcucDefs/WdgM/WdgMGeneral/WdgMSupervisedEntity/WdgMCheckpoint`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is the reference to the start Checkpoint for Deadline Monitoring.

########## 2. WdgMDeadlineStopRef

- **UUID**: `ebe91d65-d95b-46ec-bf8f-a96848d151a2`
- **引用名**: `WdgMDeadlineStopRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `WdgMCheckpoint`
- **完整路径**: `/AUTOSAR/EcucDefs/WdgM/WdgMGeneral/WdgMSupervisedEntity/WdgMCheckpoint`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is the reference to the stop Checkpoint for Deadline Monitoring. Note that the deadline's start and stop references must match an existing local or a global transition.

####### 3. WdgMExternalLogicalSupervision

**容器属性**:

- **UUID**: `a7389008-8797-4ff3-8c29-3001838dfb32`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `WdgMExternalLogicalSupervision`
- **多重性**: [0..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container collects all configuration parameters for Logical Supervision for one external graph.

######## 引用关系

此容器包含 **2** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. WdgMExternalCheckpointFinalRef

- **UUID**: `54303b7c-9f68-4443-8e78-1cf288f293bd`
- **引用名**: `WdgMExternalCheckpointFinalRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..65535]
- **目标**: `WdgMCheckpoint`
- **完整路径**: `/AUTOSAR/EcucDefs/WdgM/WdgMGeneral/WdgMSupervisedEntity/WdgMCheckpoint`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: A reference to the final global Checkpoint. Note that there might be several final global checkpoints.

########## 2. WdgMExternalCheckpointInitialRef

- **UUID**: `52370a40-da98-40cc-8349-b36730e48f59`
- **引用名**: `WdgMExternalCheckpointInitialRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `WdgMCheckpoint`
- **完整路径**: `/AUTOSAR/EcucDefs/WdgM/WdgMGeneral/WdgMSupervisedEntity/WdgMCheckpoint`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: A reference to the global initial Checkpoint.

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. WdgMExternalTransition

**容器属性**:

- **UUID**: `9a8e9a25-92e4-435a-810f-5fd323edd887`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `WdgMExternalTransition`
- **多重性**: [0..65535]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container collects the Checkpoints for a Global Transition across Supervised Entities.

########## 引用关系

此容器包含 **2** 个引用：

########### SYMBOLIC-NAME-REFERENCE 类型引用

############ 1. WdgMExternalTransitionDestRef

- **UUID**: `738ec705-b880-4260-815c-fe7e06deb8c6`
- **引用名**: `WdgMExternalTransitionDestRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `WdgMCheckpoint`
- **完整路径**: `/AUTOSAR/EcucDefs/WdgM/WdgMGeneral/WdgMSupervisedEntity/WdgMCheckpoint`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is the reference to the destination Checkpoint of an External Transition.

############ 2. WdgMExternalTransitionSourceRef

- **UUID**: `cef4db25-a448-4795-866b-fec00a586aa4`
- **引用名**: `WdgMExternalTransitionSourceRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `WdgMCheckpoint`
- **完整路径**: `/AUTOSAR/EcucDefs/WdgM/WdgMGeneral/WdgMSupervisedEntity/WdgMCheckpoint`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is the reference to the source Checkpoint of an External Transition.

####### 4. WdgMExternalTransition

**容器属性**:

- **UUID**: `9a8e9a25-92e4-435a-810f-5fd323edd887`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `WdgMExternalTransition`
- **多重性**: [0..65535]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container collects the Checkpoints for a Global Transition across Supervised Entities.

######## 引用关系

此容器包含 **2** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. WdgMExternalTransitionDestRef

- **UUID**: `738ec705-b880-4260-815c-fe7e06deb8c6`
- **引用名**: `WdgMExternalTransitionDestRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `WdgMCheckpoint`
- **完整路径**: `/AUTOSAR/EcucDefs/WdgM/WdgMGeneral/WdgMSupervisedEntity/WdgMCheckpoint`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is the reference to the destination Checkpoint of an External Transition.

########## 2. WdgMExternalTransitionSourceRef

- **UUID**: `cef4db25-a448-4795-866b-fec00a586aa4`
- **引用名**: `WdgMExternalTransitionSourceRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `WdgMCheckpoint`
- **完整路径**: `/AUTOSAR/EcucDefs/WdgM/WdgMGeneral/WdgMSupervisedEntity/WdgMCheckpoint`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is the reference to the source Checkpoint of an External Transition.

####### 5. WdgMTrigger

**容器属性**:

- **UUID**: `e5f8eed7-2309-4f4a-a169-be93791bfa92`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `WdgMTrigger`
- **多重性**: [0..255]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container collects all configuration parameters for the triggering of hardware watchdogs.

######## 参数配置

此容器包含 **3** 个参数：

######### INTEGER 类型参数

########## 1. WdgMTriggerConditionValue

- **UUID**: `292ee535-f62c-45eb-b0d2-df847155bf47`
- **参数名**: `WdgMTriggerConditionValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the maximum possible trigger time where the watchdog trigger is accepted. The consumer of this parameter is the WdgIf_SetTriggerCondition for the corresponding watchdog.

########## 2. WdgMTriggerModeId

- **UUID**: `3a676183-68c1-4bdd-9231-ebf1ec194573`
- **参数名**: `WdgMTriggerModeId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..254]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter contains a unique identifier of the trigger mode.

######### ENUMERATION 类型参数

########## 1. WdgMWatchdogMode

- **UUID**: `74c429ed-60d9-4ff6-a274-d3a5f0d8641d`
- **参数名**: `WdgMWatchdogMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `WDGIF_FAST_MODE`
  - `WDGIF_OFF_MODE`
  - `WDGIF_SLOW_MODE`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter contains the watchdog mode that shall be used for the referenced watchdog in this Watchdog Manager mode.

Implementation Type: WdgIf_ModeType

######## 引用关系

此容器包含 **1** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. WdgMTriggerWatchdogRef

- **UUID**: `82b5c6db-c67b-4cb1-a1d4-6997e8c52b8c`
- **引用名**: `WdgMTriggerWatchdogRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `WdgMWatchdog`
- **完整路径**: `/AUTOSAR/EcucDefs/WdgM/WdgMGeneral/WdgMWatchdog`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter is a reference to the configured watchdog.

####### 6. WdgMLocalStatusParams

**容器属性**:

- **UUID**: `c5f89145-ad15-4030-a200-d8f0a856d560`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `WdgMLocalStatusParams`
- **多重性**: [0..65535]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container collects all configuration parameters for the Local Status of a Supervised Entity.

######## 参数配置

此容器包含 **6** 个参数：

######### INTEGER 类型参数

########## 1. WdgMFailedAliveSupervisionRefCycleTol

- **UUID**: `d4b7363f-b318-455b-9aaf-15b410e26324`
- **参数名**: `WdgMFailedAliveSupervisionRefCycleTol`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65534]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter contains the acceptable amount of failed alive supervisions for this Supervised Entity

########## 2. WdgMFailedDeadlineRefCycleTol

- **UUID**: `dbaaf237-fcfe-4d0e-a567-8fdd590b64f0`
- **参数名**: `WdgMFailedDeadlineRefCycleTol`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65534]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter contains the acceptable amount of violated deadlines for this Supervised Entity.

Note:
The AUTOSAR implementation can be simulated for deadline violations with:
WdgMDeadlineReferenceCycle = WdgMFailedDeadlineRefCycleTol = 0

########## 3. WdgMDeadlineReferenceCycle

- **UUID**: `29479764-7332-433e-9ae3-302a69463d7c`
- **参数名**: `WdgMDeadlineReferenceCycle`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter contains the amount of supervision cycles to be used as reference by the deadline supervisions of this SE.

Note:
The AUTOSAR implementation can be simulated for deadline violations with:
WdgMDeadlineReferenceCycle = WdgMFailedDeadlineRefCycleTol = 0

########## 4. WdgMFailedProgramFlowRefCycleTol

- **UUID**: `aacd8d0f-b112-4136-b5aa-71b245ec77be`
- **参数名**: `WdgMFailedProgramFlowRefCycleTol`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65534]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter contains the acceptable amount of program flow violations for this Supervised Entity.

Note:
The AUTOSAR implementation can be simulated for program flow violations with:
WdgMProgramFlowReferenceCycle = WdgMFailedProgramFlowRefCycleTol = 0

########## 5. WdgMProgramFlowReferenceCycle

- **UUID**: `8e0e4ba9-4606-45d1-a855-a7ca85cef560`
- **参数名**: `WdgMProgramFlowReferenceCycle`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter contains the amount of supervision cycles to be used as reference by the program flow supervisions of this SE.

Note:
The AUTOSAR implementation can be simulated for program flow violations with:
WdgMProgramFlowReferenceCycle = WdgMFailedProgramFlowRefCycleTol = 0

######### ENUMERATION 类型参数

########## 1. WdgMSupervisedEntityInitialMode

- **UUID**: `185cccc7-8eeb-4932-a6d2-f52784aaa8e4`
- **参数名**: `WdgMSupervisedEntityInitialMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `WDGM_LOCAL_STATUS_OK`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `WDGM_LOCAL_STATUS_DEACTIVATED`
  - `WDGM_LOCAL_STATUS_OK`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Initial local monitoring status of the supervised entity.

######## 引用关系

此容器包含 **1** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. WdgMLocalStatusSupervisedEntityRef

- **UUID**: `f347f1b1-b1c9-454e-8d3f-045f2daf60e5`
- **引用名**: `WdgMLocalStatusSupervisedEntityRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `WdgMSupervisedEntity`
- **完整路径**: `/AUTOSAR/EcucDefs/WdgM/WdgMGeneral/WdgMSupervisedEntity`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the Supervised Entity for which the parameters of this container are set.

##### 4. WdgMAliveSupervision

**容器属性**:

- **UUID**: `17d83b33-4272-443a-aec7-7b73f961aed4`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `WdgMAliveSupervision`
- **多重性**: [0..65535]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container collects all configuration parameters of Alive-Supervision.

###### 参数配置

此容器包含 **4** 个参数：

####### INTEGER 类型参数

######## 1. WdgMExpectedAliveIndications

- **UUID**: `b565551d-d0c1-403e-85ca-6cd59f20d460`
- **参数名**: `WdgMExpectedAliveIndications`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter contains the amount of expected alive indications within the referenced amount of defined supervision cycles according to corresponding SE.

######## 2. WdgMMaxMargin

- **UUID**: `2bebf10e-04c2-4964-b4ba-31537ed41f5b`
- **参数名**: `WdgMMaxMargin`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter contains the amount of alive indications that are acceptable to be additional on the expected alive indications within the corresponding supervision reference cycle.

######## 3. WdgMMinMargin

- **UUID**: `b9ac601c-755d-4258-941d-fe67dc6a5131`
- **参数名**: `WdgMMinMargin`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter contains the amount of alive indications that are acceptable to be missed from the expected alive indications within the corresponding supervision reference cycle.

######## 4. WdgMSupervisionReferenceCycle

- **UUID**: `ef3e223c-a08c-4dab-89c7-0cb9e93c0594`
- **参数名**: `WdgMSupervisionReferenceCycle`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter contains the amount of supervision cycles to be used as reference by the alive-supervision mechanism to perform the checkup with counted alive indications according to corresponding SE.

###### 引用关系

此容器包含 **1** 个引用：

####### SYMBOLIC-NAME-REFERENCE 类型引用

######## 1. WdgMAliveSupervisionCheckpointRef

- **UUID**: `9c14cf8a-482d-4c4f-bbd3-7d8146c7703e`
- **引用名**: `WdgMAliveSupervisionCheckpointRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `WdgMCheckpoint`
- **完整路径**: `/AUTOSAR/EcucDefs/WdgM/WdgMGeneral/WdgMSupervisedEntity/WdgMCheckpoint`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the Checkpoint for which this alive counter is configured.

##### 5. WdgMDeadlineSupervision

**容器属性**:

- **UUID**: `31e680b5-fc6f-4feb-8c70-ddce7d29784a`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `WdgMDeadlineSupervision`
- **多重性**: [0..65535]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container collects all configuration parameters for Deadline Monitoring for a Supervised Entity.

###### 参数配置

此容器包含 **2** 个参数：

####### FLOAT 类型参数

######## 1. WdgMDeadlineMax

- **UUID**: `79cf6acd-1479-4a4b-9c25-5ac54b58afff`
- **参数名**: `WdgMDeadlineMax`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0.0..1.7976931348623157E+308]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter contains the longest time span after which the deadline is considered to be met.

######## 2. WdgMDeadlineMin

- **UUID**: `6bd050aa-5a0b-4266-a5dd-aac1c9b024c3`
- **参数名**: `WdgMDeadlineMin`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0.0..1.7976931348623157E+308]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter contains the shortest time span after which the deadline is considered to be met.

###### 引用关系

此容器包含 **2** 个引用：

####### SYMBOLIC-NAME-REFERENCE 类型引用

######## 1. WdgMDeadlineStartRef

- **UUID**: `447ca545-4f72-4dfc-b437-c7589ddcdb33`
- **引用名**: `WdgMDeadlineStartRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `WdgMCheckpoint`
- **完整路径**: `/AUTOSAR/EcucDefs/WdgM/WdgMGeneral/WdgMSupervisedEntity/WdgMCheckpoint`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is the reference to the start Checkpoint for Deadline Monitoring.

######## 2. WdgMDeadlineStopRef

- **UUID**: `ebe91d65-d95b-46ec-bf8f-a96848d151a2`
- **引用名**: `WdgMDeadlineStopRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `WdgMCheckpoint`
- **完整路径**: `/AUTOSAR/EcucDefs/WdgM/WdgMGeneral/WdgMSupervisedEntity/WdgMCheckpoint`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is the reference to the stop Checkpoint for Deadline Monitoring. Note that the deadline's start and stop references must match an existing local or a global transition.

##### 6. WdgMExternalLogicalSupervision

**容器属性**:

- **UUID**: `a7389008-8797-4ff3-8c29-3001838dfb32`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `WdgMExternalLogicalSupervision`
- **多重性**: [0..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container collects all configuration parameters for Logical Supervision for one external graph.

###### 引用关系

此容器包含 **2** 个引用：

####### SYMBOLIC-NAME-REFERENCE 类型引用

######## 1. WdgMExternalCheckpointFinalRef

- **UUID**: `54303b7c-9f68-4443-8e78-1cf288f293bd`
- **引用名**: `WdgMExternalCheckpointFinalRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..65535]
- **目标**: `WdgMCheckpoint`
- **完整路径**: `/AUTOSAR/EcucDefs/WdgM/WdgMGeneral/WdgMSupervisedEntity/WdgMCheckpoint`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: A reference to the final global Checkpoint. Note that there might be several final global checkpoints.

######## 2. WdgMExternalCheckpointInitialRef

- **UUID**: `52370a40-da98-40cc-8349-b36730e48f59`
- **引用名**: `WdgMExternalCheckpointInitialRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `WdgMCheckpoint`
- **完整路径**: `/AUTOSAR/EcucDefs/WdgM/WdgMGeneral/WdgMSupervisedEntity/WdgMCheckpoint`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: A reference to the global initial Checkpoint.

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. WdgMExternalTransition

**容器属性**:

- **UUID**: `9a8e9a25-92e4-435a-810f-5fd323edd887`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `WdgMExternalTransition`
- **多重性**: [0..65535]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container collects the Checkpoints for a Global Transition across Supervised Entities.

######## 引用关系

此容器包含 **2** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. WdgMExternalTransitionDestRef

- **UUID**: `738ec705-b880-4260-815c-fe7e06deb8c6`
- **引用名**: `WdgMExternalTransitionDestRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `WdgMCheckpoint`
- **完整路径**: `/AUTOSAR/EcucDefs/WdgM/WdgMGeneral/WdgMSupervisedEntity/WdgMCheckpoint`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is the reference to the destination Checkpoint of an External Transition.

########## 2. WdgMExternalTransitionSourceRef

- **UUID**: `cef4db25-a448-4795-866b-fec00a586aa4`
- **引用名**: `WdgMExternalTransitionSourceRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `WdgMCheckpoint`
- **完整路径**: `/AUTOSAR/EcucDefs/WdgM/WdgMGeneral/WdgMSupervisedEntity/WdgMCheckpoint`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is the reference to the source Checkpoint of an External Transition.

##### 7. WdgMExternalTransition

**容器属性**:

- **UUID**: `9a8e9a25-92e4-435a-810f-5fd323edd887`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `WdgMExternalTransition`
- **多重性**: [0..65535]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container collects the Checkpoints for a Global Transition across Supervised Entities.

###### 引用关系

此容器包含 **2** 个引用：

####### SYMBOLIC-NAME-REFERENCE 类型引用

######## 1. WdgMExternalTransitionDestRef

- **UUID**: `738ec705-b880-4260-815c-fe7e06deb8c6`
- **引用名**: `WdgMExternalTransitionDestRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `WdgMCheckpoint`
- **完整路径**: `/AUTOSAR/EcucDefs/WdgM/WdgMGeneral/WdgMSupervisedEntity/WdgMCheckpoint`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is the reference to the destination Checkpoint of an External Transition.

######## 2. WdgMExternalTransitionSourceRef

- **UUID**: `cef4db25-a448-4795-866b-fec00a586aa4`
- **引用名**: `WdgMExternalTransitionSourceRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `WdgMCheckpoint`
- **完整路径**: `/AUTOSAR/EcucDefs/WdgM/WdgMGeneral/WdgMSupervisedEntity/WdgMCheckpoint`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is the reference to the source Checkpoint of an External Transition.

##### 8. WdgMTrigger

**容器属性**:

- **UUID**: `e5f8eed7-2309-4f4a-a169-be93791bfa92`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `WdgMTrigger`
- **多重性**: [0..255]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container collects all configuration parameters for the triggering of hardware watchdogs.

###### 参数配置

此容器包含 **3** 个参数：

####### INTEGER 类型参数

######## 1. WdgMTriggerConditionValue

- **UUID**: `292ee535-f62c-45eb-b0d2-df847155bf47`
- **参数名**: `WdgMTriggerConditionValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the maximum possible trigger time where the watchdog trigger is accepted. The consumer of this parameter is the WdgIf_SetTriggerCondition for the corresponding watchdog.

######## 2. WdgMTriggerModeId

- **UUID**: `3a676183-68c1-4bdd-9231-ebf1ec194573`
- **参数名**: `WdgMTriggerModeId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..254]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter contains a unique identifier of the trigger mode.

####### ENUMERATION 类型参数

######## 1. WdgMWatchdogMode

- **UUID**: `74c429ed-60d9-4ff6-a274-d3a5f0d8641d`
- **参数名**: `WdgMWatchdogMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `WDGIF_FAST_MODE`
  - `WDGIF_OFF_MODE`
  - `WDGIF_SLOW_MODE`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter contains the watchdog mode that shall be used for the referenced watchdog in this Watchdog Manager mode.

Implementation Type: WdgIf_ModeType

###### 引用关系

此容器包含 **1** 个引用：

####### SYMBOLIC-NAME-REFERENCE 类型引用

######## 1. WdgMTriggerWatchdogRef

- **UUID**: `82b5c6db-c67b-4cb1-a1d4-6997e8c52b8c`
- **引用名**: `WdgMTriggerWatchdogRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `WdgMWatchdog`
- **完整路径**: `/AUTOSAR/EcucDefs/WdgM/WdgMGeneral/WdgMWatchdog`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter is a reference to the configured watchdog.

##### 9. WdgMLocalStatusParams

**容器属性**:

- **UUID**: `c5f89145-ad15-4030-a200-d8f0a856d560`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `WdgMLocalStatusParams`
- **多重性**: [0..65535]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container collects all configuration parameters for the Local Status of a Supervised Entity.

###### 参数配置

此容器包含 **6** 个参数：

####### INTEGER 类型参数

######## 1. WdgMFailedAliveSupervisionRefCycleTol

- **UUID**: `d4b7363f-b318-455b-9aaf-15b410e26324`
- **参数名**: `WdgMFailedAliveSupervisionRefCycleTol`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65534]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter contains the acceptable amount of failed alive supervisions for this Supervised Entity

######## 2. WdgMFailedDeadlineRefCycleTol

- **UUID**: `dbaaf237-fcfe-4d0e-a567-8fdd590b64f0`
- **参数名**: `WdgMFailedDeadlineRefCycleTol`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65534]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter contains the acceptable amount of violated deadlines for this Supervised Entity.

Note:
The AUTOSAR implementation can be simulated for deadline violations with:
WdgMDeadlineReferenceCycle = WdgMFailedDeadlineRefCycleTol = 0

######## 3. WdgMDeadlineReferenceCycle

- **UUID**: `29479764-7332-433e-9ae3-302a69463d7c`
- **参数名**: `WdgMDeadlineReferenceCycle`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter contains the amount of supervision cycles to be used as reference by the deadline supervisions of this SE.

Note:
The AUTOSAR implementation can be simulated for deadline violations with:
WdgMDeadlineReferenceCycle = WdgMFailedDeadlineRefCycleTol = 0

######## 4. WdgMFailedProgramFlowRefCycleTol

- **UUID**: `aacd8d0f-b112-4136-b5aa-71b245ec77be`
- **参数名**: `WdgMFailedProgramFlowRefCycleTol`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65534]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter contains the acceptable amount of program flow violations for this Supervised Entity.

Note:
The AUTOSAR implementation can be simulated for program flow violations with:
WdgMProgramFlowReferenceCycle = WdgMFailedProgramFlowRefCycleTol = 0

######## 5. WdgMProgramFlowReferenceCycle

- **UUID**: `8e0e4ba9-4606-45d1-a855-a7ca85cef560`
- **参数名**: `WdgMProgramFlowReferenceCycle`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter contains the amount of supervision cycles to be used as reference by the program flow supervisions of this SE.

Note:
The AUTOSAR implementation can be simulated for program flow violations with:
WdgMProgramFlowReferenceCycle = WdgMFailedProgramFlowRefCycleTol = 0

####### ENUMERATION 类型参数

######## 1. WdgMSupervisedEntityInitialMode

- **UUID**: `185cccc7-8eeb-4932-a6d2-f52784aaa8e4`
- **参数名**: `WdgMSupervisedEntityInitialMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `WDGM_LOCAL_STATUS_OK`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `WDGM_LOCAL_STATUS_DEACTIVATED`
  - `WDGM_LOCAL_STATUS_OK`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Initial local monitoring status of the supervised entity.

###### 引用关系

此容器包含 **1** 个引用：

####### SYMBOLIC-NAME-REFERENCE 类型引用

######## 1. WdgMLocalStatusSupervisedEntityRef

- **UUID**: `f347f1b1-b1c9-454e-8d3f-045f2daf60e5`
- **引用名**: `WdgMLocalStatusSupervisedEntityRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `WdgMSupervisedEntity`
- **完整路径**: `/AUTOSAR/EcucDefs/WdgM/WdgMGeneral/WdgMSupervisedEntity`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the Supervised Entity for which the parameters of this container are set.

##### 10. WdgMGeneral

**容器属性**:

- **UUID**: `e7a76712-0412-499a-b9ab-8dcbcd038a04`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `WdgMGeneral`
- **多重性**: [1..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

Container structures all general configuration parameters of the Watchdog Manager.

###### 参数配置

此容器包含 **19** 个参数：

####### BOOLEAN 类型参数

######## 1. WdgMDevErrorDetect

- **UUID**: `1d802c58-233d-4981-89c1-d825e51c03ab`
- **参数名**: `WdgMDevErrorDetect`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Preprocessor switch to enable/disable development error detection and reporting.
Shall be used to remove unneeded code segments regarding DET features

True: Development error detection is enabled
False: Development error detection is disabled

######## 2. WdgMDemReport

- **UUID**: `50e42660-bc0c-4757-9cf7-f0b3d98a936b`
- **参数名**: `WdgMDemReport`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Preprocessor switch to enable / disable calls to DEM in case of production error detection.

True: DEM calls enabled in case of production errors
False: DEM calls disabled in case of production errors

######## 3. WdgMImmediateReset

- **UUID**: `d425bde4-b8cf-437c-9958-049448b4b187`
- **参数名**: `WdgMImmediateReset`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This preprocessor switch enables/disablse the immediate reset feature in case of alive, deadline or program flow failure.

True: Immediate reset is enabled
False: Immediate reset is disabled

######## 4. WdgMOffModeEnabled

- **UUID**: `119efb42-de08-420e-86b6-b7437348ee83`
- **参数名**: `WdgMOffModeEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This preprocessor switch enables/disables the selection of the "OffMode" of the watchdog driver.

True: "OffMode" selection is allowed
False: "OffMode" selection is disallowed

######## 5. WdgMVersionInfoApi

- **UUID**: `85618112-5378-44c2-9636-d64c45e453fb`
- **参数名**: `WdgMVersionInfoApi`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Preprocessor switch to enable/disable the existence of the API WdgM_GetVersionInfo. Shall be used to remove unneeded code segments.

True: API is enabled
False: API is disabled

######## 6. WdgMDefensiveBehavior

- **UUID**: `39bf3444-8c8c-4a56-aa61-3a20ee0559f1`
- **参数名**: `WdgMDefensiveBehavior`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Preprocessor switch to enable/disable the defensive behavior of the Watchdog Manager module.

######## 7. WdgMUseRte

- **UUID**: `DCE:f45351c2-0460-419e-8479-b17297e90c92`
- **参数名**: `WdgMUseRte`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This preprocessor switch instructs the Watchdog Manager to use the by Rte generated defines and typedefs.

True: the WdgM uses the by Rte generated defines and typedefs
False: the WdgM uses own defines and typedefs

######## 8. WdgMDemSupervisionReport

- **UUID**: `84a70523-8e81-451f-a03c-6463a89c00a3`
- **参数名**: `WdgMDemSupervisionReport`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Preprocessor switch to enable / disable call to DEM in case the Safe Watchdog Manager has the WDGM_GLOBAL_STATE_STOPPED reached.

True: The DEM call is enabled
False: The DEM call is disabled

######## 9. WdgMFirstCycleAliveCounterReset

- **UUID**: `2ee41282-ee51-4429-8b93-433fad17241c`
- **参数名**: `WdgMFirstCycleAliveCounterReset`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: When this preprocessor switch is enabled, then the Alive counters in the first Supervision cycle are not evaluated

######## 10. WdgMAutosarDebugging

- **UUID**: `6b4b203b-5f93-4d15-a048-69a010df04b5`
- **参数名**: `WdgMAutosarDebugging`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Preprocessor switch to enable/disable the compilation of AUTOSAR debugging features, such as WdgM_GetFirstExpiredSEViolation.

True: AUTOSAR debugging is enabled
False: AUTOSAR debugging is disabled

######## 11. WdgMUseOsSuspendInterrupt

- **UUID**: `ab1e808c-42d5-4448-82ef-0e5f1d32eef7`
- **参数名**: `WdgMUseOsSuspendInterrupt`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This preprocessor switch enables/disables the usage of OS suspend and resume interrupt services within WdgM.

Note: Suspending and Resuming interrupts is done by SchM. Therefore, if this option is enabled, SchM_WdgM.h is included and not Os.h. Normally SchM_WdgM.h is generated by Rte. If so, also enable the parameter / option WdgMUseRte.

######## 12. WdgMSecondResetPath

- **UUID**: `f24ee5b0-f655-4e9d-be82-fe94774d4631`
- **参数名**: `WdgMSecondResetPath`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This preprocessor switch generally enables the access to the external Mcu_PerformReset() function. This function  is used as second reset path a specially when the primary reset path signals failure.

######## 13. WdgMTickOverrunCorrection

- **UUID**: `e84b56de-5558-4890-b2c3-57ec1dc6403c`
- **参数名**: `WdgMTickOverrunCorrection`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This preprocessor switch enables/disables 32 bit timebase counter overflow detection and correction in case of WdgMTimebaseSource is selected to be WDGM_EXTERNAL_TICK.

######## 14. WdgMEntityDeactivationEnabled

- **UUID**: `42423127-45e3-407f-ba7d-a4f66b07c929`
- **参数名**: `WdgMEntityDeactivationEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This preprocessor switch enables generally entity deactivation. Please see additional important safety information regarding this functionality in the WdgM Safety Manual.

######## 15. WdgMUseOsCoreIdentification

- **UUID**: `ab1e818c-42d5-4348-82ef-0e3f1d32eef7`
- **参数名**: `WdgMUseOsCoreIdentification`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `true`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This preprocessor switch enables/disables the usage of the OS GetCoreID() service.

######## 16. WdgMGenerateCPIdAsPortDefinedArgument

- **UUID**: `8621e4b1-e8be-4348-b0e2-b42ff416116b`
- **参数名**: `WdgMGenerateCPIdAsPortDefinedArgument`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This preprocessor switch enables/disables the generation of a port per checkpoint where the checkpoint id is added as port-defined argument.

True: A port is generated in the software component (swc) for each checkpoint of a supervised entity with both supervised entity id and checkpoint id as port-defined arguments
False: A port is generated in the software component (swc) only for each supervised entity with the supervised entity id as port-defined argument. The checkpoint id has to be added in the function call manually.

Note: To obtain AUTOSAR behavior this parameter has to be set to false.

######## 17. WdgMNotifyDetectedViolations

- **UUID**: `e64cb0f8-19a5-48c6-a9a6-99536090e34c`
- **参数名**: `WdgMNotifyDetectedViolations`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter enables or disables if the WdgM shall notify each detected Violation. 

If enabled, the integration code must implement the callout function 'WdgM_NotifyDetectedViolations' defined within WdgM_Cfg.h

####### ENUMERATION 类型参数

######## 1. WdgMTimebaseSource

- **UUID**: `e9be11ab-f793-409c-a1c4-a42cf10d194b`
- **参数名**: `WdgMTimebaseSource`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `WDGM_INTERNAL_SOFTWARE_TICK`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `WDGM_INTERNAL_SOFTWARE_TICK` (来源: Vector Informatik)
  - `WDGM_OS_COUNTER_TICK` (来源: Vector Informatik)
  - `WDGM_EXTERNAL_TICK` (来源: Vector Informatik)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter selects the Tick counter source for Deadline monitoring.

WDGM_INTERNAL_SOFTWARE_TICK: The counter is incremented each time `WdgM_MainFunction` is called.
WDGM_OS_COUNTER_TICK: The timebase is based on the Os hardware counter.
WDGM_EXTERNAL_TICK: The counter is incremented each time `WdgM_UpdateTickCount` is called.

######## 2. WdgMStatusReportingMechanism

- **UUID**: `010babfb-75ea-4160-a011-a2004e419941`
- **参数名**: `WdgMStatusReportingMechanism`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `WDGM_USE_MODE_SWITCH_PORTS`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `WDGM_USE_MODE_SWITCH_PORTS` (来源: Vector Informatik)
  - `WDGM_USE_NOTIFICATIONS` (来源: Vector Informatik)
  - `WDGM_USE_NO_STATUS_REPORTING` (来源: Vector Informatik)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter selects which mechansim should be applied for status reporting.

WDGM_USE_MODE_SWITCH_PORTS: ModeSwitchPorts are used to report a status change.
WDGM_USE_NOTIFICATIONS: Notifications are used to report a status change.
WDGM_USE_NO_STATUS_REPORTING: No reporting mechanism of a status change is used.

###### 配置容器

本模块包含 **5** 个配置容器：

####### 1. WdgMSupervisedEntity

**容器属性**:

- **UUID**: `1f1b7f90-09ce-418d-9914-9fa978eaa8b9`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `WdgMSupervisedEntity`
- **多重性**: [0..65535]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container collects all common (mode-independent) parameters of a Supervised Entity to be supervised by the Watchdog Manager.

######## 参数配置

此容器包含 **4** 个参数：

######### INTEGER 类型参数

########## 1. WdgMSupervisedEntityId

- **UUID**: `5d11b234-1da9-499e-9813-61d8b6ea146d`
- **参数名**: `WdgMSupervisedEntityId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `65535`
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter shall contain the unique identifier of the supervised entity.

All supervised entity ids must form a zero-based list of integers.

######### BOOLEAN 类型参数

########## 1. WdgMEnableEntityDeactivation

- **UUID**: `8b5262a5-986b-4625-ac67-502059a51c25`
- **参数名**: `WdgMEnableEntityDeactivation`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enables deactivation of this supervised enitiy.

########## 2. WdgMReportStatusViaRte

- **UUID**: `504bd038-9420-4668-9f80-7eb011cde650`
- **参数名**: `WdgMReportStatusViaRte`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter is used to enable the status reporting via Rte.

Notes:
- This parameter can only be set true if WdgMStatusReportingMechanism is _not_ WDGM_USE_NO_STATUS_REPORTING
- If this parameter is set true in any of the supervised entities or in WdgMMode, the global switch WdgMUseRte has to be set true, too.
- This parameter cannot be set true if global switch WdgMUseRte is set false.
- If this parameter is set true, the optional parameter WdgMLocalStateChangeCbk must not exist.

######### FUNCTION-NAME 类型参数

########## 1. WdgMLocalStateChangeCbk

- **UUID**: `90266c73-7e46-465a-97f7-afd37e16fd1d`
- **参数名**: `WdgMLocalStateChangeCbk`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Callback function for notifying the supervised entity's status change.

Note:
- This parameter can only be used if WdgMStatusReportingMechanism is set to WDGM_USE_NOTIFICATIONS.
- This parameter can only be used if parameter WdgMReportStatusViaRte of this supervised entity is set false

######## 引用关系

此容器包含 **3** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. WdgMInternallCheckpointFinalRef

- **UUID**: `d17ccb90-6fd6-486f-9928-ef51b47de4a5`
- **引用名**: `WdgMInternallCheckpointFinalRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..65535]
- **目标**: `WdgMCheckpoint`
- **完整路径**: `/AUTOSAR/EcucDefs/WdgM/WdgMGeneral/WdgMSupervisedEntity/WdgMCheckpoint`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: A reference to the final local Checkpoint of this supervised entity. Note that there might be several final local checkpoints.

########## 2. WdgMInternalCheckpointInitialRef

- **UUID**: `e9e3a78f-46a7-4642-8c33-6d47199acb38`
- **引用名**: `WdgMInternalCheckpointInitialRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `WdgMCheckpoint`
- **完整路径**: `/AUTOSAR/EcucDefs/WdgM/WdgMGeneral/WdgMSupervisedEntity/WdgMCheckpoint`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: A reference to the initial local Checkpoint of this supervised entity.

######### CHOICE-REFERENCE 类型引用

########## 1. WdgMAppTaskRef

- **UUID**: `d0537c3a-7739-487f-b445-0b49b715ea47`
- **引用名**: `WdgMAppTaskRef`
- **引用类型**: CHOICE-REFERENCE
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **需要索引**: false
- **目标引用列表**:
  - `/AUTOSAR/EcucDefs/Os/OsApplication`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to an OS Application. In case of OS SC3 the local data of the supervised entity should be placed in the same memory segment as the application this supervised entity is part of.

######## 配置容器

本模块包含 **2** 个配置容器：

######### 1. WdgMCheckpoint

**容器属性**:

- **UUID**: `4162e1c3-29b2-4714-a81a-f529b92aa19a`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `WdgMCheckpoint`
- **多重性**: [1..65535]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container collects all Checkpoints of this Supervised Entity.

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. WdgMCheckpointId

- **UUID**: `822fbd5d-93cf-46bb-9592-aec82b80e415`
- **参数名**: `WdgMCheckpointId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `65535`
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter shall contain the unique identifier of checkpoint within a supervised entity.

All checkpoint ids must form a zero-based list of integers.

######### 2. WdgMInternalTransition

**容器属性**:

- **UUID**: `9c3078e8-0991-495d-912a-b176954bf595`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `WdgMInternalTransition`
- **多重性**: [0..65535]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container defines the graph of Internal Transitions within this Supervised Entity.

########## 引用关系

此容器包含 **2** 个引用：

########### SYMBOLIC-NAME-REFERENCE 类型引用

############ 1. WdgMInternalTransitionDestRef

- **UUID**: `6295dfa9-ae85-4892-b425-dc5345974767`
- **引用名**: `WdgMInternalTransitionDestRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `WdgMCheckpoint`
- **完整路径**: `/AUTOSAR/EcucDefs/WdgM/WdgMGeneral/WdgMSupervisedEntity/WdgMCheckpoint`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is the reference to the destination Checkpoint of an Internal Transition within this Supervised Entity.

############ 2. WdgMInternalTransitionSourceRef

- **UUID**: `587857ad-a04b-4270-afe9-62afbb02c92f`
- **引用名**: `WdgMInternalTransitionSourceRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `WdgMCheckpoint`
- **完整路径**: `/AUTOSAR/EcucDefs/WdgM/WdgMGeneral/WdgMSupervisedEntity/WdgMCheckpoint`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is the reference to the source Checkpoint of an Internal Transition within this Supervised Entity.

####### 2. WdgMCheckpoint

**容器属性**:

- **UUID**: `4162e1c3-29b2-4714-a81a-f529b92aa19a`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `WdgMCheckpoint`
- **多重性**: [1..65535]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container collects all Checkpoints of this Supervised Entity.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. WdgMCheckpointId

- **UUID**: `822fbd5d-93cf-46bb-9592-aec82b80e415`
- **参数名**: `WdgMCheckpointId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `65535`
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter shall contain the unique identifier of checkpoint within a supervised entity.

All checkpoint ids must form a zero-based list of integers.

####### 3. WdgMInternalTransition

**容器属性**:

- **UUID**: `9c3078e8-0991-495d-912a-b176954bf595`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `WdgMInternalTransition`
- **多重性**: [0..65535]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container defines the graph of Internal Transitions within this Supervised Entity.

######## 引用关系

此容器包含 **2** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. WdgMInternalTransitionDestRef

- **UUID**: `6295dfa9-ae85-4892-b425-dc5345974767`
- **引用名**: `WdgMInternalTransitionDestRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `WdgMCheckpoint`
- **完整路径**: `/AUTOSAR/EcucDefs/WdgM/WdgMGeneral/WdgMSupervisedEntity/WdgMCheckpoint`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is the reference to the destination Checkpoint of an Internal Transition within this Supervised Entity.

########## 2. WdgMInternalTransitionSourceRef

- **UUID**: `587857ad-a04b-4270-afe9-62afbb02c92f`
- **引用名**: `WdgMInternalTransitionSourceRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `WdgMCheckpoint`
- **完整路径**: `/AUTOSAR/EcucDefs/WdgM/WdgMGeneral/WdgMSupervisedEntity/WdgMCheckpoint`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is the reference to the source Checkpoint of an Internal Transition within this Supervised Entity.

####### 4. WdgMWatchdog

**容器属性**:

- **UUID**: `97ffb261-94c1-4c06-b9ee-db4b2438f249`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `WdgMWatchdog`
- **多重性**: [0..255]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container collects all common (mode-independent) parameters of a Watchdog to be triggered by the Watchdog Manager.

######## 参数配置

此容器包含 **1** 个参数：

######### STRING 类型参数

########## 1. WdgMWatchdogName

- **UUID**: `34b7583c-0063-41bd-8163-d37122ebec3c`
- **参数名**: `WdgMWatchdogName`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter is a symbolic name of the Watchdog. Is used as comment only.

######## 引用关系

此容器包含 **1** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. WdgMWatchdogDeviceRef

- **UUID**: `18932417-a0b0-47d5-aa4f-779f42f86cd4`
- **引用名**: `WdgMWatchdogDeviceRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `WdgIfDevice`
- **完整路径**: `/AUTOSAR/EcucDefs/WdgIf/WdgIfDevice`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to one device container of Watchdog Interface. In the referenced container WdgIfDevice, the parameter WdgIfDeviceIndex contains the Index parameter that WdgM has to use for WdgIf_SetTriggerCondition calls for that watchdog instance.

####### 5. WdgMCallerIds

**容器属性**:

- **UUID**: `da6a51af-e6c2-4999-b39a-75ae5f68c2f1`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `WdgMCallerIds`
- **多重性**: [1..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

Contains the definition of valid CallerIds for the callers who have permission to call the function WdgM_SetMode

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. WdgMCallerId

- **UUID**: `af28aff6-ff31-4716-a35b-c1477327216f`
- **参数名**: `WdgMCallerId`
- **数据类型**: INTEGER
- **多重性**: [1..255]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines one valid CallerId for the callers who have permission to
 call the function WdgM_SetMode.

##### 11. WdgMSupervisedEntity

**容器属性**:

- **UUID**: `1f1b7f90-09ce-418d-9914-9fa978eaa8b9`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `WdgMSupervisedEntity`
- **多重性**: [0..65535]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container collects all common (mode-independent) parameters of a Supervised Entity to be supervised by the Watchdog Manager.

###### 参数配置

此容器包含 **4** 个参数：

####### INTEGER 类型参数

######## 1. WdgMSupervisedEntityId

- **UUID**: `5d11b234-1da9-499e-9813-61d8b6ea146d`
- **参数名**: `WdgMSupervisedEntityId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `65535`
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter shall contain the unique identifier of the supervised entity.

All supervised entity ids must form a zero-based list of integers.

####### BOOLEAN 类型参数

######## 1. WdgMEnableEntityDeactivation

- **UUID**: `8b5262a5-986b-4625-ac67-502059a51c25`
- **参数名**: `WdgMEnableEntityDeactivation`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enables deactivation of this supervised enitiy.

######## 2. WdgMReportStatusViaRte

- **UUID**: `504bd038-9420-4668-9f80-7eb011cde650`
- **参数名**: `WdgMReportStatusViaRte`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter is used to enable the status reporting via Rte.

Notes:
- This parameter can only be set true if WdgMStatusReportingMechanism is _not_ WDGM_USE_NO_STATUS_REPORTING
- If this parameter is set true in any of the supervised entities or in WdgMMode, the global switch WdgMUseRte has to be set true, too.
- This parameter cannot be set true if global switch WdgMUseRte is set false.
- If this parameter is set true, the optional parameter WdgMLocalStateChangeCbk must not exist.

####### FUNCTION-NAME 类型参数

######## 1. WdgMLocalStateChangeCbk

- **UUID**: `90266c73-7e46-465a-97f7-afd37e16fd1d`
- **参数名**: `WdgMLocalStateChangeCbk`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Callback function for notifying the supervised entity's status change.

Note:
- This parameter can only be used if WdgMStatusReportingMechanism is set to WDGM_USE_NOTIFICATIONS.
- This parameter can only be used if parameter WdgMReportStatusViaRte of this supervised entity is set false

###### 引用关系

此容器包含 **3** 个引用：

####### SYMBOLIC-NAME-REFERENCE 类型引用

######## 1. WdgMInternallCheckpointFinalRef

- **UUID**: `d17ccb90-6fd6-486f-9928-ef51b47de4a5`
- **引用名**: `WdgMInternallCheckpointFinalRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..65535]
- **目标**: `WdgMCheckpoint`
- **完整路径**: `/AUTOSAR/EcucDefs/WdgM/WdgMGeneral/WdgMSupervisedEntity/WdgMCheckpoint`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: A reference to the final local Checkpoint of this supervised entity. Note that there might be several final local checkpoints.

######## 2. WdgMInternalCheckpointInitialRef

- **UUID**: `e9e3a78f-46a7-4642-8c33-6d47199acb38`
- **引用名**: `WdgMInternalCheckpointInitialRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `WdgMCheckpoint`
- **完整路径**: `/AUTOSAR/EcucDefs/WdgM/WdgMGeneral/WdgMSupervisedEntity/WdgMCheckpoint`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: A reference to the initial local Checkpoint of this supervised entity.

####### CHOICE-REFERENCE 类型引用

######## 1. WdgMAppTaskRef

- **UUID**: `d0537c3a-7739-487f-b445-0b49b715ea47`
- **引用名**: `WdgMAppTaskRef`
- **引用类型**: CHOICE-REFERENCE
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **需要索引**: false
- **目标引用列表**:
  - `/AUTOSAR/EcucDefs/Os/OsApplication`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to an OS Application. In case of OS SC3 the local data of the supervised entity should be placed in the same memory segment as the application this supervised entity is part of.

###### 配置容器

本模块包含 **2** 个配置容器：

####### 1. WdgMCheckpoint

**容器属性**:

- **UUID**: `4162e1c3-29b2-4714-a81a-f529b92aa19a`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `WdgMCheckpoint`
- **多重性**: [1..65535]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container collects all Checkpoints of this Supervised Entity.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. WdgMCheckpointId

- **UUID**: `822fbd5d-93cf-46bb-9592-aec82b80e415`
- **参数名**: `WdgMCheckpointId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `65535`
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter shall contain the unique identifier of checkpoint within a supervised entity.

All checkpoint ids must form a zero-based list of integers.

####### 2. WdgMInternalTransition

**容器属性**:

- **UUID**: `9c3078e8-0991-495d-912a-b176954bf595`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `WdgMInternalTransition`
- **多重性**: [0..65535]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container defines the graph of Internal Transitions within this Supervised Entity.

######## 引用关系

此容器包含 **2** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. WdgMInternalTransitionDestRef

- **UUID**: `6295dfa9-ae85-4892-b425-dc5345974767`
- **引用名**: `WdgMInternalTransitionDestRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `WdgMCheckpoint`
- **完整路径**: `/AUTOSAR/EcucDefs/WdgM/WdgMGeneral/WdgMSupervisedEntity/WdgMCheckpoint`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is the reference to the destination Checkpoint of an Internal Transition within this Supervised Entity.

########## 2. WdgMInternalTransitionSourceRef

- **UUID**: `587857ad-a04b-4270-afe9-62afbb02c92f`
- **引用名**: `WdgMInternalTransitionSourceRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `WdgMCheckpoint`
- **完整路径**: `/AUTOSAR/EcucDefs/WdgM/WdgMGeneral/WdgMSupervisedEntity/WdgMCheckpoint`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is the reference to the source Checkpoint of an Internal Transition within this Supervised Entity.

##### 12. WdgMCheckpoint

**容器属性**:

- **UUID**: `4162e1c3-29b2-4714-a81a-f529b92aa19a`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `WdgMCheckpoint`
- **多重性**: [1..65535]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container collects all Checkpoints of this Supervised Entity.

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. WdgMCheckpointId

- **UUID**: `822fbd5d-93cf-46bb-9592-aec82b80e415`
- **参数名**: `WdgMCheckpointId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `65535`
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter shall contain the unique identifier of checkpoint within a supervised entity.

All checkpoint ids must form a zero-based list of integers.

##### 13. WdgMInternalTransition

**容器属性**:

- **UUID**: `9c3078e8-0991-495d-912a-b176954bf595`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `WdgMInternalTransition`
- **多重性**: [0..65535]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container defines the graph of Internal Transitions within this Supervised Entity.

###### 引用关系

此容器包含 **2** 个引用：

####### SYMBOLIC-NAME-REFERENCE 类型引用

######## 1. WdgMInternalTransitionDestRef

- **UUID**: `6295dfa9-ae85-4892-b425-dc5345974767`
- **引用名**: `WdgMInternalTransitionDestRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `WdgMCheckpoint`
- **完整路径**: `/AUTOSAR/EcucDefs/WdgM/WdgMGeneral/WdgMSupervisedEntity/WdgMCheckpoint`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is the reference to the destination Checkpoint of an Internal Transition within this Supervised Entity.

######## 2. WdgMInternalTransitionSourceRef

- **UUID**: `587857ad-a04b-4270-afe9-62afbb02c92f`
- **引用名**: `WdgMInternalTransitionSourceRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `WdgMCheckpoint`
- **完整路径**: `/AUTOSAR/EcucDefs/WdgM/WdgMGeneral/WdgMSupervisedEntity/WdgMCheckpoint`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is the reference to the source Checkpoint of an Internal Transition within this Supervised Entity.

##### 14. WdgMWatchdog

**容器属性**:

- **UUID**: `97ffb261-94c1-4c06-b9ee-db4b2438f249`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `WdgMWatchdog`
- **多重性**: [0..255]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container collects all common (mode-independent) parameters of a Watchdog to be triggered by the Watchdog Manager.

###### 参数配置

此容器包含 **1** 个参数：

####### STRING 类型参数

######## 1. WdgMWatchdogName

- **UUID**: `34b7583c-0063-41bd-8163-d37122ebec3c`
- **参数名**: `WdgMWatchdogName`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter is a symbolic name of the Watchdog. Is used as comment only.

###### 引用关系

此容器包含 **1** 个引用：

####### SYMBOLIC-NAME-REFERENCE 类型引用

######## 1. WdgMWatchdogDeviceRef

- **UUID**: `18932417-a0b0-47d5-aa4f-779f42f86cd4`
- **引用名**: `WdgMWatchdogDeviceRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `WdgIfDevice`
- **完整路径**: `/AUTOSAR/EcucDefs/WdgIf/WdgIfDevice`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to one device container of Watchdog Interface. In the referenced container WdgIfDevice, the parameter WdgIfDeviceIndex contains the Index parameter that WdgM has to use for WdgIf_SetTriggerCondition calls for that watchdog instance.

##### 15. WdgMCallerIds

**容器属性**:

- **UUID**: `da6a51af-e6c2-4999-b39a-75ae5f68c2f1`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `WdgMCallerIds`
- **多重性**: [1..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

Contains the definition of valid CallerIds for the callers who have permission to call the function WdgM_SetMode

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. WdgMCallerId

- **UUID**: `af28aff6-ff31-4716-a35b-c1477327216f`
- **参数名**: `WdgMCallerId`
- **数据类型**: INTEGER
- **多重性**: [1..255]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines one valid CallerId for the callers who have permission to
 call the function WdgM_SetMode.

## 📦 包结构

此ARXML文件包含 **1** 个包：

### 1. MICROSAR

- **UUID**: `ff55d029-386d-43a2-b3c2-dfef4c7a5e36`
- **包名称**: `MICROSAR`
- **包含元素数量**: 4

#### 包含的元素

##### BSW-IMPLEMENTATION 类型元素

1. **WdgM_Impl**

##### ECUC-MODULE-DEF 类型元素

1. **WdgM**

##### ECUC-MODULE-CONFIGURATION-VALUES 类型元素

1. **WdgM_Pre**
2. **WdgM_Rec**

## ⚡ 实现信息

此ARXML文件包含 **1** 个实现：

### 1. WdgM_Impl

- **UUID**: `fd26c7c1-00dc-4cd6-b4f6-f6e9f892aecc`
- **实现名称**: `WdgM_Impl`
- **编程语言**: C
- **软件版本**: 6.01.00
- **供应商ID**: 30
- **AUTOSAR版本**: 4.02.02
- **代码生成器**: DaVinci Configurator

## ⚙️ 配置信息

此ARXML文件包含 **2** 个配置：

### 1. WdgM_Pre

- **UUID**: `68f4e362-c89d-450c-905d-79fcedbb9a6c`
- **配置名称**: `WdgM_Pre`
- **定义引用**: `/MICROSAR/WdgM`

### 2. WdgM_Rec

- **UUID**: `789d2022-f9dc-404b-9013-5f6651060f9f`
- **配置名称**: `WdgM_Rec`
- **定义引用**: `/MICROSAR/WdgM`
