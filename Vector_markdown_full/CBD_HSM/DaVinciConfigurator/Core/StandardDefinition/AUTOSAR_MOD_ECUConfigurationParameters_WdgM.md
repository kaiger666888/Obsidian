# WdgM - 完整配置文档

*此文档由ARXML文件自动生成，采用层次化结构展示*

**生成时间**: 2025-06-16 14:52:01

## 📑 目录

- [📄 文件信息](#-文件信息)
- [🔧 模块定义](#-模块定义)
  - [WdgM](#wdgm)
- [📦 包结构](#-包结构)

## 📄 文件信息

### Schema信息
- **Schema位置**: `http://autosar.org/schema/r4.0 AUTOSAR_4-0-3.xsd`
- **命名空间**: `http://autosar.org/schema/r4.0`

## 🔧 模块定义

### 1. WdgM

#### 基本信息

- **UUID**: `ECUC:638595db-d815-40cb-8517-623305d0313e`
- **模块名称**: `WdgM`
- **多重性**: [0..1]
- **支持的变体**:
  - VARIANT-POST-BUILD
  - VARIANT-PRE-COMPILE

#### 模块描述

Configuration of the WdgM (Watchdog Manager) module.

#### 版本历史

共有 **1** 个版本记录：

##### 1. 版本 4.2.0

- **发布日期**: 2011-11-09
- **发布者**: AUTOSAR

*此版本无详细变更记录*

#### 配置容器

本模块包含 **15** 个配置容器：

##### 1. WdgMConfigSet

**容器属性**:

- **UUID**: `ECUC:df6338ce-c64d-4457-9304-67ac2b1aa516`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `WdgMConfigSet`
- **多重性**: [1..1]
- **多配置容器**: true

**容器描述**:

This container describes one of multiple configuration sets of WdgM.

###### 引用关系

此容器包含 **1** 个引用：

####### SYMBOLIC-NAME-REFERENCE 类型引用

######## 1. WdgMInitialMode

- **UUID**: `ECUC:0d4155c0-613a-4132-a555-e2454061c74c`
- **引用名**: `WdgMInitialMode`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `WdgMMode`
- **完整路径**: `/AUTOSAR/EcucDefs/WdgM/WdgMConfigSet/WdgMMode`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The mode that the Watchdog Manager is in after it has been initialized.

###### 配置容器

本模块包含 **8** 个配置容器：

####### 1. WdgMDemEventParameterRefs

**容器属性**:

- **UUID**: `ECUC:83469853-9485-490e-b532-f9d523b81681`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `WdgMDemEventParameterRefs`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Container for the references to DemEventParameter elements which shall be invoked using the API Dem_ReportErrorStatus API in case the corresponding error occurs. The EventId is taken from the referenced DemEventParameter's DemEventId value. The standardized errors are provided in the container and can be extended by vendor specific error references.

######## 引用关系

此容器包含 **3** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. WDGM_E_IMPROPER_CALLER

- **UUID**: `ECUC:2388851c-3bee-4dcc-b570-cb9d0db92777`
- **引用名**: `WDGM_E_IMPROPER_CALLER`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `DemEventParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemConfigSet/DemEventParameter`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the DemEventParameter which shall be issued when the defensive behavior checks have detected an improper caller.

########## 2. WDGM_E_MONITORING

- **UUID**: `ECUC:80360d1f-e977-41a3-a996-ecc2d8af4780`
- **引用名**: `WDGM_E_MONITORING`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `DemEventParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemConfigSet/DemEventParameter`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the DemEventParameter which shall be issued when the error "Monitoring has failed and a watchdog reset will occur" has occured.

########## 3. WDGM_E_SET_MODE

- **UUID**: `ECUC:e878340c-b52e-436b-9573-9605d3937379`
- **引用名**: `WDGM_E_SET_MODE`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `DemEventParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemConfigSet/DemEventParameter`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the DemEventParameter which shall be issued when the error "Watchdog drivers' mode switch has failed" has occured.

####### 2. WdgMMode

**容器属性**:

- **UUID**: `ECUC:57abb8dd-f2ae-4f7a-995f-5a102c125824`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `WdgMMode`
- **多重性**: [1..255]
- **多配置容器**: false

**容器描述**:

The container describes one of several modes of the Watchdog Manager.

######## 参数配置

此容器包含 **3** 个参数：

######### INTEGER 类型参数

########## 1. WdgMExpiredSupervisionCycleTol

- **UUID**: `ECUC:5527db00-defa-42f3-9b17-bf4ecbd64092`
- **参数名**: `WdgMExpiredSupervisionCycleTol`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter shall be used to define a value that fixes the amount of expired supervision cycles for how long the blocking of watchdog triggering shall be postponed, AFTER THE GLOBAL SUPERVISION STATUS HAS REACHED THE STATE EXPIRED.

########## 2. WdgMModeId

- **UUID**: `ECUC:2006dc2d-a878-4367-a2b2-b36b855468aa`
- **参数名**: `WdgMModeId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter fixes the identfier for the mode. This identifier is for instance passed as a parameter to the WdgM_SetMode service.

######### FLOAT 类型参数

########## 1. WdgMSupervisionCycle

- **UUID**: `ECUC:eb454bd1-fb86-45cc-9196-8f4e37f40091`
- **参数名**: `WdgMSupervisionCycle`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0..Inf]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the schedule period of the main function WdgM_MainFunction.

######## 配置容器

本模块包含 **6** 个配置容器：

######### 1. WdgMAliveSupervision

**容器属性**:

- **UUID**: `ECUC:c44ab53e-7a86-4f12-9c9c-f5a1b0a69e8c`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `WdgMAliveSupervision`
- **多重性**: [0..65535]
- **多配置容器**: false

**容器描述**:

This container collects all configuration parameters of Alive-Supervision of one Checkpoint. Note that each Checkpoint may have different parameters. For example, it may have different min and max margin.

########## 参数配置

此容器包含 **4** 个参数：

########### INTEGER 类型参数

############ 1. WdgMExpectedAliveIndications

- **UUID**: `ECUC:0adf20c6-581b-482d-943b-d868a65172ee`
- **参数名**: `WdgMExpectedAliveIndications`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter contains the amount of expected alive indications of the Checkpoint within the referenced amount of defined supervision cycles according to corresponding SE.

############ 2. WdgMMaxMargin

- **UUID**: `ECUC:54ba6825-39c2-4455-9f94-972c9d93f2d3`
- **参数名**: `WdgMMaxMargin`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter contains the amount of alive indications of the Checkpoint that are acceptable to be additional to the expected alive indications within the corresponding supervision reference cycle.

############ 3. WdgMMinMargin

- **UUID**: `ECUC:863ef215-dc2b-4e4b-8326-f66b16ac9b99`
- **参数名**: `WdgMMinMargin`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter contains the amount of alive indications of the Checkpoint that are acceptable to be missed from the expected alive indications within the corresponding supervision reference cycle.

############ 4. WdgMSupervisionReferenceCycle

- **UUID**: `ECUC:e7c93a08-a9c8-4d5b-ad81-cd5162629c17`
- **参数名**: `WdgMSupervisionReferenceCycle`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter shall contain the amount of supervision cycles to be used as reference by the alive-supervision mechanism to perform the checkup with counted alive indications according to corresponding SE.

########## 引用关系

此容器包含 **1** 个引用：

########### SYMBOLIC-NAME-REFERENCE 类型引用

############ 1. WdgMAliveSupervisionCheckpointRef

- **UUID**: `ECUC:13b0a782-86c1-4d7d-8881-296c1d7ae526`
- **引用名**: `WdgMAliveSupervisionCheckpointRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `WdgMCheckpoint`
- **完整路径**: `/AUTOSAR/EcucDefs/WdgM/WdgMGeneral/WdgMSupervisedEntity/WdgMCheckpoint`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to Checkpoint within a Supervised Entity that shall be supervised.

######### 2. WdgMDeadlineSupervision

**容器属性**:

- **UUID**: `ECUC:7d45be84-c819-4c3e-8708-f14e27a383bc`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `WdgMDeadlineSupervision`
- **多重性**: [0..65535]
- **多配置容器**: false

**容器描述**:

This container collects all configuration parameters for Deadline Supervision for a Supervised Entity.

########## 参数配置

此容器包含 **2** 个参数：

########### FLOAT 类型参数

############ 1. WdgMDeadlineMax

- **UUID**: `ECUC:3c3ce3fe-61c0-48eb-a57b-d9b3eaefa758`
- **参数名**: `WdgMDeadlineMax`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0..Inf]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter contains the longest time span after which the deadline is considered to be met.

############ 2. WdgMDeadlineMin

- **UUID**: `ECUC:84c81576-4bc3-4e78-afe8-03c6dbdddeae`
- **参数名**: `WdgMDeadlineMin`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0..Inf]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter contains the shortest time span after which the deadline is considered to be met.

########## 引用关系

此容器包含 **2** 个引用：

########### SYMBOLIC-NAME-REFERENCE 类型引用

############ 1. WdgMDeadlineStartRef

- **UUID**: `ECUC:7315c694-ea89-41db-8fa5-c1f157decc9d`
- **引用名**: `WdgMDeadlineStartRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `WdgMCheckpoint`
- **完整路径**: `/AUTOSAR/EcucDefs/WdgM/WdgMGeneral/WdgMSupervisedEntity/WdgMCheckpoint`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is the reference to the start Checkpoint for Deadline Supervision.

############ 2. WdgMDeadlineStopRef

- **UUID**: `ECUC:c8a36e45-cdee-4ae5-b13c-9b927ad65a14`
- **引用名**: `WdgMDeadlineStopRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `WdgMCheckpoint`
- **完整路径**: `/AUTOSAR/EcucDefs/WdgM/WdgMGeneral/WdgMSupervisedEntity/WdgMCheckpoint`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is the reference to the stop Checkpoint for Deadline Supervision.

######### 3. WdgMExternalLogicalSupervision

**容器属性**:

- **UUID**: `ECUC:43bc6246-1dca-4110-bf78-2515840be0c0`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `WdgMExternalLogicalSupervision`
- **多重性**: [0..65535]
- **多配置容器**: false

**容器描述**:

This container collects all configuration parameters for Logical Supervision for one external graph.

########## 引用关系

此容器包含 **2** 个引用：

########### SYMBOLIC-NAME-REFERENCE 类型引用

############ 1. WdgMExternalCheckpointFinalRef

- **UUID**: `ECUC:aa7d746c-d843-4a93-a671-57ea14c49e92`
- **引用名**: `WdgMExternalCheckpointFinalRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..65535]
- **目标**: `WdgMCheckpoint`
- **完整路径**: `/AUTOSAR/EcucDefs/WdgM/WdgMGeneral/WdgMSupervisedEntity/WdgMCheckpoint`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is the reference to the final Checkpoint(s) for this External Graph.

############ 2. WdgMExternalCheckpointInitialRef

- **UUID**: `ECUC:6d36e919-cc12-42b2-8396-0e80fe8cb29b`
- **引用名**: `WdgMExternalCheckpointInitialRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..65535]
- **目标**: `WdgMCheckpoint`
- **完整路径**: `/AUTOSAR/EcucDefs/WdgM/WdgMGeneral/WdgMSupervisedEntity/WdgMCheckpoint`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is the reference to the initial Checkpoint(s) for this External Graph.

########## 配置容器

本模块包含 **1** 个配置容器：

########### 1. WdgMExternalTransition

**容器属性**:

- **UUID**: `ECUC:7eac09e3-4835-49eb-a652-349678c049fb`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `WdgMExternalTransition`
- **多重性**: [0..65535]
- **多配置容器**: false

**容器描述**:

This container collects the Checkpoints for an External Transition across Supervised Entities.

############ 引用关系

此容器包含 **2** 个引用：

############# SYMBOLIC-NAME-REFERENCE 类型引用

############## 1. WdgMExternalTransitionDestRef

- **UUID**: `ECUC:efb75a7a-7f7a-402f-90b2-6bea69d9fa20`
- **引用名**: `WdgMExternalTransitionDestRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `WdgMCheckpoint`
- **完整路径**: `/AUTOSAR/EcucDefs/WdgM/WdgMGeneral/WdgMSupervisedEntity/WdgMCheckpoint`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is the reference to the destination Checkpoint of an External Transition.

############## 2. WdgMExternalTransitionSourceRef

- **UUID**: `ECUC:d51e9ba8-7460-4f0b-ac83-14f697366a1b`
- **引用名**: `WdgMExternalTransitionSourceRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `WdgMCheckpoint`
- **完整路径**: `/AUTOSAR/EcucDefs/WdgM/WdgMGeneral/WdgMSupervisedEntity/WdgMCheckpoint`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is the reference to the source Checkpoint of an External Transition.

######### 4. WdgMExternalTransition

**容器属性**:

- **UUID**: `ECUC:7eac09e3-4835-49eb-a652-349678c049fb`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `WdgMExternalTransition`
- **多重性**: [0..65535]
- **多配置容器**: false

**容器描述**:

This container collects the Checkpoints for an External Transition across Supervised Entities.

########## 引用关系

此容器包含 **2** 个引用：

########### SYMBOLIC-NAME-REFERENCE 类型引用

############ 1. WdgMExternalTransitionDestRef

- **UUID**: `ECUC:efb75a7a-7f7a-402f-90b2-6bea69d9fa20`
- **引用名**: `WdgMExternalTransitionDestRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `WdgMCheckpoint`
- **完整路径**: `/AUTOSAR/EcucDefs/WdgM/WdgMGeneral/WdgMSupervisedEntity/WdgMCheckpoint`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is the reference to the destination Checkpoint of an External Transition.

############ 2. WdgMExternalTransitionSourceRef

- **UUID**: `ECUC:d51e9ba8-7460-4f0b-ac83-14f697366a1b`
- **引用名**: `WdgMExternalTransitionSourceRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `WdgMCheckpoint`
- **完整路径**: `/AUTOSAR/EcucDefs/WdgM/WdgMGeneral/WdgMSupervisedEntity/WdgMCheckpoint`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is the reference to the source Checkpoint of an External Transition.

######### 5. WdgMLocalStatusParams

**容器属性**:

- **UUID**: `ECUC:7d6e9106-a46c-42f7-8099-2b025b6928f1`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `WdgMLocalStatusParams`
- **多重性**: [0..65535]
- **多配置容器**: false

**容器描述**:

This container collects all configuration parameters for the Local Status of a Supervised Entity.

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. WdgMFailedAliveSupervisionRefCycleTol

- **UUID**: `ECUC:19ecddaa-c38c-4575-a851-33956ce42842`
- **参数名**: `WdgMFailedAliveSupervisionRefCycleTol`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter shall contain the acceptable amount of reference cycles with incorrect/failed alive supervisions for this Supervised Entity.

########## 引用关系

此容器包含 **1** 个引用：

########### SYMBOLIC-NAME-REFERENCE 类型引用

############ 1. WdgMLocalStatusSupervisedEntityRef

- **UUID**: `ECUC:2c458ef3-034f-45e3-ba86-70d08b59842a`
- **引用名**: `WdgMLocalStatusSupervisedEntityRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `WdgMSupervisedEntity`
- **完整路径**: `/AUTOSAR/EcucDefs/WdgM/WdgMGeneral/WdgMSupervisedEntity`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is the reference to the Supervised Entity for which the Local Status parameters are specified.

######### 6. WdgMTrigger

**容器属性**:

- **UUID**: `ECUC:b81d7037-a060-4e9c-9e16-175443d60577`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `WdgMTrigger`
- **多重性**: [0..255]
- **多配置容器**: false

**容器描述**:

This container collects all configuration parameters for the triggering of hardware watchdogs.

########## 参数配置

此容器包含 **2** 个参数：

########### INTEGER 类型参数

############ 1. WdgMTriggerConditionValue

- **UUID**: `ECUC:05108bc5-d328-4bf1-8cd9-bbc37c0b971a`
- **参数名**: `WdgMTriggerConditionValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter shall contain the value that is passed to WdgIf_SetTriggerCondition for this watchdog.

########### ENUMERATION 类型参数

############ 1. WdgMWatchdogMode

- **UUID**: `ECUC:b69101dc-fbeb-4530-8fba-7201fd38e3b5`
- **参数名**: `WdgMWatchdogMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `WDGIF_FAST_MODE` (来源: AUTOSAR_ECUC)
  - `WDGIF_OFF_MODE` (来源: AUTOSAR_ECUC)
  - `WDGIF_SLOW_MODE` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter contains the watchdog mode that shall be used for the referenced watchdog in this Watchdog Manager mode.

########## 引用关系

此容器包含 **1** 个引用：

########### SYMBOLIC-NAME-REFERENCE 类型引用

############ 1. WdgMTriggerWatchdogRef

- **UUID**: `ECUC:8f3d8b0f-8da6-4cf4-8ca0-31c89ffc4670`
- **引用名**: `WdgMTriggerWatchdogRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `WdgMWatchdog`
- **完整路径**: `/AUTOSAR/EcucDefs/WdgM/WdgMGeneral/WdgMWatchdog`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter is a reference to the configured watchdog.

####### 3. WdgMAliveSupervision

**容器属性**:

- **UUID**: `ECUC:c44ab53e-7a86-4f12-9c9c-f5a1b0a69e8c`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `WdgMAliveSupervision`
- **多重性**: [0..65535]
- **多配置容器**: false

**容器描述**:

This container collects all configuration parameters of Alive-Supervision of one Checkpoint. Note that each Checkpoint may have different parameters. For example, it may have different min and max margin.

######## 参数配置

此容器包含 **4** 个参数：

######### INTEGER 类型参数

########## 1. WdgMExpectedAliveIndications

- **UUID**: `ECUC:0adf20c6-581b-482d-943b-d868a65172ee`
- **参数名**: `WdgMExpectedAliveIndications`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter contains the amount of expected alive indications of the Checkpoint within the referenced amount of defined supervision cycles according to corresponding SE.

########## 2. WdgMMaxMargin

- **UUID**: `ECUC:54ba6825-39c2-4455-9f94-972c9d93f2d3`
- **参数名**: `WdgMMaxMargin`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter contains the amount of alive indications of the Checkpoint that are acceptable to be additional to the expected alive indications within the corresponding supervision reference cycle.

########## 3. WdgMMinMargin

- **UUID**: `ECUC:863ef215-dc2b-4e4b-8326-f66b16ac9b99`
- **参数名**: `WdgMMinMargin`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter contains the amount of alive indications of the Checkpoint that are acceptable to be missed from the expected alive indications within the corresponding supervision reference cycle.

########## 4. WdgMSupervisionReferenceCycle

- **UUID**: `ECUC:e7c93a08-a9c8-4d5b-ad81-cd5162629c17`
- **参数名**: `WdgMSupervisionReferenceCycle`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter shall contain the amount of supervision cycles to be used as reference by the alive-supervision mechanism to perform the checkup with counted alive indications according to corresponding SE.

######## 引用关系

此容器包含 **1** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. WdgMAliveSupervisionCheckpointRef

- **UUID**: `ECUC:13b0a782-86c1-4d7d-8881-296c1d7ae526`
- **引用名**: `WdgMAliveSupervisionCheckpointRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `WdgMCheckpoint`
- **完整路径**: `/AUTOSAR/EcucDefs/WdgM/WdgMGeneral/WdgMSupervisedEntity/WdgMCheckpoint`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to Checkpoint within a Supervised Entity that shall be supervised.

####### 4. WdgMDeadlineSupervision

**容器属性**:

- **UUID**: `ECUC:7d45be84-c819-4c3e-8708-f14e27a383bc`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `WdgMDeadlineSupervision`
- **多重性**: [0..65535]
- **多配置容器**: false

**容器描述**:

This container collects all configuration parameters for Deadline Supervision for a Supervised Entity.

######## 参数配置

此容器包含 **2** 个参数：

######### FLOAT 类型参数

########## 1. WdgMDeadlineMax

- **UUID**: `ECUC:3c3ce3fe-61c0-48eb-a57b-d9b3eaefa758`
- **参数名**: `WdgMDeadlineMax`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0..Inf]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter contains the longest time span after which the deadline is considered to be met.

########## 2. WdgMDeadlineMin

- **UUID**: `ECUC:84c81576-4bc3-4e78-afe8-03c6dbdddeae`
- **参数名**: `WdgMDeadlineMin`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0..Inf]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter contains the shortest time span after which the deadline is considered to be met.

######## 引用关系

此容器包含 **2** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. WdgMDeadlineStartRef

- **UUID**: `ECUC:7315c694-ea89-41db-8fa5-c1f157decc9d`
- **引用名**: `WdgMDeadlineStartRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `WdgMCheckpoint`
- **完整路径**: `/AUTOSAR/EcucDefs/WdgM/WdgMGeneral/WdgMSupervisedEntity/WdgMCheckpoint`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is the reference to the start Checkpoint for Deadline Supervision.

########## 2. WdgMDeadlineStopRef

- **UUID**: `ECUC:c8a36e45-cdee-4ae5-b13c-9b927ad65a14`
- **引用名**: `WdgMDeadlineStopRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `WdgMCheckpoint`
- **完整路径**: `/AUTOSAR/EcucDefs/WdgM/WdgMGeneral/WdgMSupervisedEntity/WdgMCheckpoint`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is the reference to the stop Checkpoint for Deadline Supervision.

####### 5. WdgMExternalLogicalSupervision

**容器属性**:

- **UUID**: `ECUC:43bc6246-1dca-4110-bf78-2515840be0c0`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `WdgMExternalLogicalSupervision`
- **多重性**: [0..65535]
- **多配置容器**: false

**容器描述**:

This container collects all configuration parameters for Logical Supervision for one external graph.

######## 引用关系

此容器包含 **2** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. WdgMExternalCheckpointFinalRef

- **UUID**: `ECUC:aa7d746c-d843-4a93-a671-57ea14c49e92`
- **引用名**: `WdgMExternalCheckpointFinalRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..65535]
- **目标**: `WdgMCheckpoint`
- **完整路径**: `/AUTOSAR/EcucDefs/WdgM/WdgMGeneral/WdgMSupervisedEntity/WdgMCheckpoint`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is the reference to the final Checkpoint(s) for this External Graph.

########## 2. WdgMExternalCheckpointInitialRef

- **UUID**: `ECUC:6d36e919-cc12-42b2-8396-0e80fe8cb29b`
- **引用名**: `WdgMExternalCheckpointInitialRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..65535]
- **目标**: `WdgMCheckpoint`
- **完整路径**: `/AUTOSAR/EcucDefs/WdgM/WdgMGeneral/WdgMSupervisedEntity/WdgMCheckpoint`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is the reference to the initial Checkpoint(s) for this External Graph.

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. WdgMExternalTransition

**容器属性**:

- **UUID**: `ECUC:7eac09e3-4835-49eb-a652-349678c049fb`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `WdgMExternalTransition`
- **多重性**: [0..65535]
- **多配置容器**: false

**容器描述**:

This container collects the Checkpoints for an External Transition across Supervised Entities.

########## 引用关系

此容器包含 **2** 个引用：

########### SYMBOLIC-NAME-REFERENCE 类型引用

############ 1. WdgMExternalTransitionDestRef

- **UUID**: `ECUC:efb75a7a-7f7a-402f-90b2-6bea69d9fa20`
- **引用名**: `WdgMExternalTransitionDestRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `WdgMCheckpoint`
- **完整路径**: `/AUTOSAR/EcucDefs/WdgM/WdgMGeneral/WdgMSupervisedEntity/WdgMCheckpoint`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is the reference to the destination Checkpoint of an External Transition.

############ 2. WdgMExternalTransitionSourceRef

- **UUID**: `ECUC:d51e9ba8-7460-4f0b-ac83-14f697366a1b`
- **引用名**: `WdgMExternalTransitionSourceRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `WdgMCheckpoint`
- **完整路径**: `/AUTOSAR/EcucDefs/WdgM/WdgMGeneral/WdgMSupervisedEntity/WdgMCheckpoint`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is the reference to the source Checkpoint of an External Transition.

####### 6. WdgMExternalTransition

**容器属性**:

- **UUID**: `ECUC:7eac09e3-4835-49eb-a652-349678c049fb`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `WdgMExternalTransition`
- **多重性**: [0..65535]
- **多配置容器**: false

**容器描述**:

This container collects the Checkpoints for an External Transition across Supervised Entities.

######## 引用关系

此容器包含 **2** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. WdgMExternalTransitionDestRef

- **UUID**: `ECUC:efb75a7a-7f7a-402f-90b2-6bea69d9fa20`
- **引用名**: `WdgMExternalTransitionDestRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `WdgMCheckpoint`
- **完整路径**: `/AUTOSAR/EcucDefs/WdgM/WdgMGeneral/WdgMSupervisedEntity/WdgMCheckpoint`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is the reference to the destination Checkpoint of an External Transition.

########## 2. WdgMExternalTransitionSourceRef

- **UUID**: `ECUC:d51e9ba8-7460-4f0b-ac83-14f697366a1b`
- **引用名**: `WdgMExternalTransitionSourceRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `WdgMCheckpoint`
- **完整路径**: `/AUTOSAR/EcucDefs/WdgM/WdgMGeneral/WdgMSupervisedEntity/WdgMCheckpoint`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is the reference to the source Checkpoint of an External Transition.

####### 7. WdgMLocalStatusParams

**容器属性**:

- **UUID**: `ECUC:7d6e9106-a46c-42f7-8099-2b025b6928f1`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `WdgMLocalStatusParams`
- **多重性**: [0..65535]
- **多配置容器**: false

**容器描述**:

This container collects all configuration parameters for the Local Status of a Supervised Entity.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. WdgMFailedAliveSupervisionRefCycleTol

- **UUID**: `ECUC:19ecddaa-c38c-4575-a851-33956ce42842`
- **参数名**: `WdgMFailedAliveSupervisionRefCycleTol`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter shall contain the acceptable amount of reference cycles with incorrect/failed alive supervisions for this Supervised Entity.

######## 引用关系

此容器包含 **1** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. WdgMLocalStatusSupervisedEntityRef

- **UUID**: `ECUC:2c458ef3-034f-45e3-ba86-70d08b59842a`
- **引用名**: `WdgMLocalStatusSupervisedEntityRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `WdgMSupervisedEntity`
- **完整路径**: `/AUTOSAR/EcucDefs/WdgM/WdgMGeneral/WdgMSupervisedEntity`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is the reference to the Supervised Entity for which the Local Status parameters are specified.

####### 8. WdgMTrigger

**容器属性**:

- **UUID**: `ECUC:b81d7037-a060-4e9c-9e16-175443d60577`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `WdgMTrigger`
- **多重性**: [0..255]
- **多配置容器**: false

**容器描述**:

This container collects all configuration parameters for the triggering of hardware watchdogs.

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. WdgMTriggerConditionValue

- **UUID**: `ECUC:05108bc5-d328-4bf1-8cd9-bbc37c0b971a`
- **参数名**: `WdgMTriggerConditionValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter shall contain the value that is passed to WdgIf_SetTriggerCondition for this watchdog.

######### ENUMERATION 类型参数

########## 1. WdgMWatchdogMode

- **UUID**: `ECUC:b69101dc-fbeb-4530-8fba-7201fd38e3b5`
- **参数名**: `WdgMWatchdogMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `WDGIF_FAST_MODE` (来源: AUTOSAR_ECUC)
  - `WDGIF_OFF_MODE` (来源: AUTOSAR_ECUC)
  - `WDGIF_SLOW_MODE` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter contains the watchdog mode that shall be used for the referenced watchdog in this Watchdog Manager mode.

######## 引用关系

此容器包含 **1** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. WdgMTriggerWatchdogRef

- **UUID**: `ECUC:8f3d8b0f-8da6-4cf4-8ca0-31c89ffc4670`
- **引用名**: `WdgMTriggerWatchdogRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `WdgMWatchdog`
- **完整路径**: `/AUTOSAR/EcucDefs/WdgM/WdgMGeneral/WdgMWatchdog`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter is a reference to the configured watchdog.

##### 2. WdgMDemEventParameterRefs

**容器属性**:

- **UUID**: `ECUC:83469853-9485-490e-b532-f9d523b81681`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `WdgMDemEventParameterRefs`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Container for the references to DemEventParameter elements which shall be invoked using the API Dem_ReportErrorStatus API in case the corresponding error occurs. The EventId is taken from the referenced DemEventParameter's DemEventId value. The standardized errors are provided in the container and can be extended by vendor specific error references.

###### 引用关系

此容器包含 **3** 个引用：

####### SYMBOLIC-NAME-REFERENCE 类型引用

######## 1. WDGM_E_IMPROPER_CALLER

- **UUID**: `ECUC:2388851c-3bee-4dcc-b570-cb9d0db92777`
- **引用名**: `WDGM_E_IMPROPER_CALLER`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `DemEventParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemConfigSet/DemEventParameter`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the DemEventParameter which shall be issued when the defensive behavior checks have detected an improper caller.

######## 2. WDGM_E_MONITORING

- **UUID**: `ECUC:80360d1f-e977-41a3-a996-ecc2d8af4780`
- **引用名**: `WDGM_E_MONITORING`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `DemEventParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemConfigSet/DemEventParameter`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the DemEventParameter which shall be issued when the error "Monitoring has failed and a watchdog reset will occur" has occured.

######## 3. WDGM_E_SET_MODE

- **UUID**: `ECUC:e878340c-b52e-436b-9573-9605d3937379`
- **引用名**: `WDGM_E_SET_MODE`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `DemEventParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemConfigSet/DemEventParameter`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the DemEventParameter which shall be issued when the error "Watchdog drivers' mode switch has failed" has occured.

##### 3. WdgMMode

**容器属性**:

- **UUID**: `ECUC:57abb8dd-f2ae-4f7a-995f-5a102c125824`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `WdgMMode`
- **多重性**: [1..255]
- **多配置容器**: false

**容器描述**:

The container describes one of several modes of the Watchdog Manager.

###### 参数配置

此容器包含 **3** 个参数：

####### INTEGER 类型参数

######## 1. WdgMExpiredSupervisionCycleTol

- **UUID**: `ECUC:5527db00-defa-42f3-9b17-bf4ecbd64092`
- **参数名**: `WdgMExpiredSupervisionCycleTol`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter shall be used to define a value that fixes the amount of expired supervision cycles for how long the blocking of watchdog triggering shall be postponed, AFTER THE GLOBAL SUPERVISION STATUS HAS REACHED THE STATE EXPIRED.

######## 2. WdgMModeId

- **UUID**: `ECUC:2006dc2d-a878-4367-a2b2-b36b855468aa`
- **参数名**: `WdgMModeId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter fixes the identfier for the mode. This identifier is for instance passed as a parameter to the WdgM_SetMode service.

####### FLOAT 类型参数

######## 1. WdgMSupervisionCycle

- **UUID**: `ECUC:eb454bd1-fb86-45cc-9196-8f4e37f40091`
- **参数名**: `WdgMSupervisionCycle`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0..Inf]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the schedule period of the main function WdgM_MainFunction.

###### 配置容器

本模块包含 **6** 个配置容器：

####### 1. WdgMAliveSupervision

**容器属性**:

- **UUID**: `ECUC:c44ab53e-7a86-4f12-9c9c-f5a1b0a69e8c`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `WdgMAliveSupervision`
- **多重性**: [0..65535]
- **多配置容器**: false

**容器描述**:

This container collects all configuration parameters of Alive-Supervision of one Checkpoint. Note that each Checkpoint may have different parameters. For example, it may have different min and max margin.

######## 参数配置

此容器包含 **4** 个参数：

######### INTEGER 类型参数

########## 1. WdgMExpectedAliveIndications

- **UUID**: `ECUC:0adf20c6-581b-482d-943b-d868a65172ee`
- **参数名**: `WdgMExpectedAliveIndications`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter contains the amount of expected alive indications of the Checkpoint within the referenced amount of defined supervision cycles according to corresponding SE.

########## 2. WdgMMaxMargin

- **UUID**: `ECUC:54ba6825-39c2-4455-9f94-972c9d93f2d3`
- **参数名**: `WdgMMaxMargin`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter contains the amount of alive indications of the Checkpoint that are acceptable to be additional to the expected alive indications within the corresponding supervision reference cycle.

########## 3. WdgMMinMargin

- **UUID**: `ECUC:863ef215-dc2b-4e4b-8326-f66b16ac9b99`
- **参数名**: `WdgMMinMargin`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter contains the amount of alive indications of the Checkpoint that are acceptable to be missed from the expected alive indications within the corresponding supervision reference cycle.

########## 4. WdgMSupervisionReferenceCycle

- **UUID**: `ECUC:e7c93a08-a9c8-4d5b-ad81-cd5162629c17`
- **参数名**: `WdgMSupervisionReferenceCycle`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter shall contain the amount of supervision cycles to be used as reference by the alive-supervision mechanism to perform the checkup with counted alive indications according to corresponding SE.

######## 引用关系

此容器包含 **1** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. WdgMAliveSupervisionCheckpointRef

- **UUID**: `ECUC:13b0a782-86c1-4d7d-8881-296c1d7ae526`
- **引用名**: `WdgMAliveSupervisionCheckpointRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `WdgMCheckpoint`
- **完整路径**: `/AUTOSAR/EcucDefs/WdgM/WdgMGeneral/WdgMSupervisedEntity/WdgMCheckpoint`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to Checkpoint within a Supervised Entity that shall be supervised.

####### 2. WdgMDeadlineSupervision

**容器属性**:

- **UUID**: `ECUC:7d45be84-c819-4c3e-8708-f14e27a383bc`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `WdgMDeadlineSupervision`
- **多重性**: [0..65535]
- **多配置容器**: false

**容器描述**:

This container collects all configuration parameters for Deadline Supervision for a Supervised Entity.

######## 参数配置

此容器包含 **2** 个参数：

######### FLOAT 类型参数

########## 1. WdgMDeadlineMax

- **UUID**: `ECUC:3c3ce3fe-61c0-48eb-a57b-d9b3eaefa758`
- **参数名**: `WdgMDeadlineMax`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0..Inf]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter contains the longest time span after which the deadline is considered to be met.

########## 2. WdgMDeadlineMin

- **UUID**: `ECUC:84c81576-4bc3-4e78-afe8-03c6dbdddeae`
- **参数名**: `WdgMDeadlineMin`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0..Inf]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter contains the shortest time span after which the deadline is considered to be met.

######## 引用关系

此容器包含 **2** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. WdgMDeadlineStartRef

- **UUID**: `ECUC:7315c694-ea89-41db-8fa5-c1f157decc9d`
- **引用名**: `WdgMDeadlineStartRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `WdgMCheckpoint`
- **完整路径**: `/AUTOSAR/EcucDefs/WdgM/WdgMGeneral/WdgMSupervisedEntity/WdgMCheckpoint`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is the reference to the start Checkpoint for Deadline Supervision.

########## 2. WdgMDeadlineStopRef

- **UUID**: `ECUC:c8a36e45-cdee-4ae5-b13c-9b927ad65a14`
- **引用名**: `WdgMDeadlineStopRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `WdgMCheckpoint`
- **完整路径**: `/AUTOSAR/EcucDefs/WdgM/WdgMGeneral/WdgMSupervisedEntity/WdgMCheckpoint`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is the reference to the stop Checkpoint for Deadline Supervision.

####### 3. WdgMExternalLogicalSupervision

**容器属性**:

- **UUID**: `ECUC:43bc6246-1dca-4110-bf78-2515840be0c0`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `WdgMExternalLogicalSupervision`
- **多重性**: [0..65535]
- **多配置容器**: false

**容器描述**:

This container collects all configuration parameters for Logical Supervision for one external graph.

######## 引用关系

此容器包含 **2** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. WdgMExternalCheckpointFinalRef

- **UUID**: `ECUC:aa7d746c-d843-4a93-a671-57ea14c49e92`
- **引用名**: `WdgMExternalCheckpointFinalRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..65535]
- **目标**: `WdgMCheckpoint`
- **完整路径**: `/AUTOSAR/EcucDefs/WdgM/WdgMGeneral/WdgMSupervisedEntity/WdgMCheckpoint`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is the reference to the final Checkpoint(s) for this External Graph.

########## 2. WdgMExternalCheckpointInitialRef

- **UUID**: `ECUC:6d36e919-cc12-42b2-8396-0e80fe8cb29b`
- **引用名**: `WdgMExternalCheckpointInitialRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..65535]
- **目标**: `WdgMCheckpoint`
- **完整路径**: `/AUTOSAR/EcucDefs/WdgM/WdgMGeneral/WdgMSupervisedEntity/WdgMCheckpoint`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is the reference to the initial Checkpoint(s) for this External Graph.

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. WdgMExternalTransition

**容器属性**:

- **UUID**: `ECUC:7eac09e3-4835-49eb-a652-349678c049fb`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `WdgMExternalTransition`
- **多重性**: [0..65535]
- **多配置容器**: false

**容器描述**:

This container collects the Checkpoints for an External Transition across Supervised Entities.

########## 引用关系

此容器包含 **2** 个引用：

########### SYMBOLIC-NAME-REFERENCE 类型引用

############ 1. WdgMExternalTransitionDestRef

- **UUID**: `ECUC:efb75a7a-7f7a-402f-90b2-6bea69d9fa20`
- **引用名**: `WdgMExternalTransitionDestRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `WdgMCheckpoint`
- **完整路径**: `/AUTOSAR/EcucDefs/WdgM/WdgMGeneral/WdgMSupervisedEntity/WdgMCheckpoint`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is the reference to the destination Checkpoint of an External Transition.

############ 2. WdgMExternalTransitionSourceRef

- **UUID**: `ECUC:d51e9ba8-7460-4f0b-ac83-14f697366a1b`
- **引用名**: `WdgMExternalTransitionSourceRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `WdgMCheckpoint`
- **完整路径**: `/AUTOSAR/EcucDefs/WdgM/WdgMGeneral/WdgMSupervisedEntity/WdgMCheckpoint`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is the reference to the source Checkpoint of an External Transition.

####### 4. WdgMExternalTransition

**容器属性**:

- **UUID**: `ECUC:7eac09e3-4835-49eb-a652-349678c049fb`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `WdgMExternalTransition`
- **多重性**: [0..65535]
- **多配置容器**: false

**容器描述**:

This container collects the Checkpoints for an External Transition across Supervised Entities.

######## 引用关系

此容器包含 **2** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. WdgMExternalTransitionDestRef

- **UUID**: `ECUC:efb75a7a-7f7a-402f-90b2-6bea69d9fa20`
- **引用名**: `WdgMExternalTransitionDestRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `WdgMCheckpoint`
- **完整路径**: `/AUTOSAR/EcucDefs/WdgM/WdgMGeneral/WdgMSupervisedEntity/WdgMCheckpoint`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is the reference to the destination Checkpoint of an External Transition.

########## 2. WdgMExternalTransitionSourceRef

- **UUID**: `ECUC:d51e9ba8-7460-4f0b-ac83-14f697366a1b`
- **引用名**: `WdgMExternalTransitionSourceRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `WdgMCheckpoint`
- **完整路径**: `/AUTOSAR/EcucDefs/WdgM/WdgMGeneral/WdgMSupervisedEntity/WdgMCheckpoint`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is the reference to the source Checkpoint of an External Transition.

####### 5. WdgMLocalStatusParams

**容器属性**:

- **UUID**: `ECUC:7d6e9106-a46c-42f7-8099-2b025b6928f1`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `WdgMLocalStatusParams`
- **多重性**: [0..65535]
- **多配置容器**: false

**容器描述**:

This container collects all configuration parameters for the Local Status of a Supervised Entity.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. WdgMFailedAliveSupervisionRefCycleTol

- **UUID**: `ECUC:19ecddaa-c38c-4575-a851-33956ce42842`
- **参数名**: `WdgMFailedAliveSupervisionRefCycleTol`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter shall contain the acceptable amount of reference cycles with incorrect/failed alive supervisions for this Supervised Entity.

######## 引用关系

此容器包含 **1** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. WdgMLocalStatusSupervisedEntityRef

- **UUID**: `ECUC:2c458ef3-034f-45e3-ba86-70d08b59842a`
- **引用名**: `WdgMLocalStatusSupervisedEntityRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `WdgMSupervisedEntity`
- **完整路径**: `/AUTOSAR/EcucDefs/WdgM/WdgMGeneral/WdgMSupervisedEntity`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is the reference to the Supervised Entity for which the Local Status parameters are specified.

####### 6. WdgMTrigger

**容器属性**:

- **UUID**: `ECUC:b81d7037-a060-4e9c-9e16-175443d60577`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `WdgMTrigger`
- **多重性**: [0..255]
- **多配置容器**: false

**容器描述**:

This container collects all configuration parameters for the triggering of hardware watchdogs.

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. WdgMTriggerConditionValue

- **UUID**: `ECUC:05108bc5-d328-4bf1-8cd9-bbc37c0b971a`
- **参数名**: `WdgMTriggerConditionValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter shall contain the value that is passed to WdgIf_SetTriggerCondition for this watchdog.

######### ENUMERATION 类型参数

########## 1. WdgMWatchdogMode

- **UUID**: `ECUC:b69101dc-fbeb-4530-8fba-7201fd38e3b5`
- **参数名**: `WdgMWatchdogMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `WDGIF_FAST_MODE` (来源: AUTOSAR_ECUC)
  - `WDGIF_OFF_MODE` (来源: AUTOSAR_ECUC)
  - `WDGIF_SLOW_MODE` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter contains the watchdog mode that shall be used for the referenced watchdog in this Watchdog Manager mode.

######## 引用关系

此容器包含 **1** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. WdgMTriggerWatchdogRef

- **UUID**: `ECUC:8f3d8b0f-8da6-4cf4-8ca0-31c89ffc4670`
- **引用名**: `WdgMTriggerWatchdogRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `WdgMWatchdog`
- **完整路径**: `/AUTOSAR/EcucDefs/WdgM/WdgMGeneral/WdgMWatchdog`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter is a reference to the configured watchdog.

##### 4. WdgMAliveSupervision

**容器属性**:

- **UUID**: `ECUC:c44ab53e-7a86-4f12-9c9c-f5a1b0a69e8c`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `WdgMAliveSupervision`
- **多重性**: [0..65535]
- **多配置容器**: false

**容器描述**:

This container collects all configuration parameters of Alive-Supervision of one Checkpoint. Note that each Checkpoint may have different parameters. For example, it may have different min and max margin.

###### 参数配置

此容器包含 **4** 个参数：

####### INTEGER 类型参数

######## 1. WdgMExpectedAliveIndications

- **UUID**: `ECUC:0adf20c6-581b-482d-943b-d868a65172ee`
- **参数名**: `WdgMExpectedAliveIndications`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter contains the amount of expected alive indications of the Checkpoint within the referenced amount of defined supervision cycles according to corresponding SE.

######## 2. WdgMMaxMargin

- **UUID**: `ECUC:54ba6825-39c2-4455-9f94-972c9d93f2d3`
- **参数名**: `WdgMMaxMargin`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter contains the amount of alive indications of the Checkpoint that are acceptable to be additional to the expected alive indications within the corresponding supervision reference cycle.

######## 3. WdgMMinMargin

- **UUID**: `ECUC:863ef215-dc2b-4e4b-8326-f66b16ac9b99`
- **参数名**: `WdgMMinMargin`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter contains the amount of alive indications of the Checkpoint that are acceptable to be missed from the expected alive indications within the corresponding supervision reference cycle.

######## 4. WdgMSupervisionReferenceCycle

- **UUID**: `ECUC:e7c93a08-a9c8-4d5b-ad81-cd5162629c17`
- **参数名**: `WdgMSupervisionReferenceCycle`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter shall contain the amount of supervision cycles to be used as reference by the alive-supervision mechanism to perform the checkup with counted alive indications according to corresponding SE.

###### 引用关系

此容器包含 **1** 个引用：

####### SYMBOLIC-NAME-REFERENCE 类型引用

######## 1. WdgMAliveSupervisionCheckpointRef

- **UUID**: `ECUC:13b0a782-86c1-4d7d-8881-296c1d7ae526`
- **引用名**: `WdgMAliveSupervisionCheckpointRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `WdgMCheckpoint`
- **完整路径**: `/AUTOSAR/EcucDefs/WdgM/WdgMGeneral/WdgMSupervisedEntity/WdgMCheckpoint`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to Checkpoint within a Supervised Entity that shall be supervised.

##### 5. WdgMDeadlineSupervision

**容器属性**:

- **UUID**: `ECUC:7d45be84-c819-4c3e-8708-f14e27a383bc`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `WdgMDeadlineSupervision`
- **多重性**: [0..65535]
- **多配置容器**: false

**容器描述**:

This container collects all configuration parameters for Deadline Supervision for a Supervised Entity.

###### 参数配置

此容器包含 **2** 个参数：

####### FLOAT 类型参数

######## 1. WdgMDeadlineMax

- **UUID**: `ECUC:3c3ce3fe-61c0-48eb-a57b-d9b3eaefa758`
- **参数名**: `WdgMDeadlineMax`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0..Inf]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter contains the longest time span after which the deadline is considered to be met.

######## 2. WdgMDeadlineMin

- **UUID**: `ECUC:84c81576-4bc3-4e78-afe8-03c6dbdddeae`
- **参数名**: `WdgMDeadlineMin`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0..Inf]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter contains the shortest time span after which the deadline is considered to be met.

###### 引用关系

此容器包含 **2** 个引用：

####### SYMBOLIC-NAME-REFERENCE 类型引用

######## 1. WdgMDeadlineStartRef

- **UUID**: `ECUC:7315c694-ea89-41db-8fa5-c1f157decc9d`
- **引用名**: `WdgMDeadlineStartRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `WdgMCheckpoint`
- **完整路径**: `/AUTOSAR/EcucDefs/WdgM/WdgMGeneral/WdgMSupervisedEntity/WdgMCheckpoint`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is the reference to the start Checkpoint for Deadline Supervision.

######## 2. WdgMDeadlineStopRef

- **UUID**: `ECUC:c8a36e45-cdee-4ae5-b13c-9b927ad65a14`
- **引用名**: `WdgMDeadlineStopRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `WdgMCheckpoint`
- **完整路径**: `/AUTOSAR/EcucDefs/WdgM/WdgMGeneral/WdgMSupervisedEntity/WdgMCheckpoint`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is the reference to the stop Checkpoint for Deadline Supervision.

##### 6. WdgMExternalLogicalSupervision

**容器属性**:

- **UUID**: `ECUC:43bc6246-1dca-4110-bf78-2515840be0c0`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `WdgMExternalLogicalSupervision`
- **多重性**: [0..65535]
- **多配置容器**: false

**容器描述**:

This container collects all configuration parameters for Logical Supervision for one external graph.

###### 引用关系

此容器包含 **2** 个引用：

####### SYMBOLIC-NAME-REFERENCE 类型引用

######## 1. WdgMExternalCheckpointFinalRef

- **UUID**: `ECUC:aa7d746c-d843-4a93-a671-57ea14c49e92`
- **引用名**: `WdgMExternalCheckpointFinalRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..65535]
- **目标**: `WdgMCheckpoint`
- **完整路径**: `/AUTOSAR/EcucDefs/WdgM/WdgMGeneral/WdgMSupervisedEntity/WdgMCheckpoint`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is the reference to the final Checkpoint(s) for this External Graph.

######## 2. WdgMExternalCheckpointInitialRef

- **UUID**: `ECUC:6d36e919-cc12-42b2-8396-0e80fe8cb29b`
- **引用名**: `WdgMExternalCheckpointInitialRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..65535]
- **目标**: `WdgMCheckpoint`
- **完整路径**: `/AUTOSAR/EcucDefs/WdgM/WdgMGeneral/WdgMSupervisedEntity/WdgMCheckpoint`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is the reference to the initial Checkpoint(s) for this External Graph.

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. WdgMExternalTransition

**容器属性**:

- **UUID**: `ECUC:7eac09e3-4835-49eb-a652-349678c049fb`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `WdgMExternalTransition`
- **多重性**: [0..65535]
- **多配置容器**: false

**容器描述**:

This container collects the Checkpoints for an External Transition across Supervised Entities.

######## 引用关系

此容器包含 **2** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. WdgMExternalTransitionDestRef

- **UUID**: `ECUC:efb75a7a-7f7a-402f-90b2-6bea69d9fa20`
- **引用名**: `WdgMExternalTransitionDestRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `WdgMCheckpoint`
- **完整路径**: `/AUTOSAR/EcucDefs/WdgM/WdgMGeneral/WdgMSupervisedEntity/WdgMCheckpoint`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is the reference to the destination Checkpoint of an External Transition.

########## 2. WdgMExternalTransitionSourceRef

- **UUID**: `ECUC:d51e9ba8-7460-4f0b-ac83-14f697366a1b`
- **引用名**: `WdgMExternalTransitionSourceRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `WdgMCheckpoint`
- **完整路径**: `/AUTOSAR/EcucDefs/WdgM/WdgMGeneral/WdgMSupervisedEntity/WdgMCheckpoint`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is the reference to the source Checkpoint of an External Transition.

##### 7. WdgMExternalTransition

**容器属性**:

- **UUID**: `ECUC:7eac09e3-4835-49eb-a652-349678c049fb`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `WdgMExternalTransition`
- **多重性**: [0..65535]
- **多配置容器**: false

**容器描述**:

This container collects the Checkpoints for an External Transition across Supervised Entities.

###### 引用关系

此容器包含 **2** 个引用：

####### SYMBOLIC-NAME-REFERENCE 类型引用

######## 1. WdgMExternalTransitionDestRef

- **UUID**: `ECUC:efb75a7a-7f7a-402f-90b2-6bea69d9fa20`
- **引用名**: `WdgMExternalTransitionDestRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `WdgMCheckpoint`
- **完整路径**: `/AUTOSAR/EcucDefs/WdgM/WdgMGeneral/WdgMSupervisedEntity/WdgMCheckpoint`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is the reference to the destination Checkpoint of an External Transition.

######## 2. WdgMExternalTransitionSourceRef

- **UUID**: `ECUC:d51e9ba8-7460-4f0b-ac83-14f697366a1b`
- **引用名**: `WdgMExternalTransitionSourceRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `WdgMCheckpoint`
- **完整路径**: `/AUTOSAR/EcucDefs/WdgM/WdgMGeneral/WdgMSupervisedEntity/WdgMCheckpoint`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is the reference to the source Checkpoint of an External Transition.

##### 8. WdgMLocalStatusParams

**容器属性**:

- **UUID**: `ECUC:7d6e9106-a46c-42f7-8099-2b025b6928f1`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `WdgMLocalStatusParams`
- **多重性**: [0..65535]
- **多配置容器**: false

**容器描述**:

This container collects all configuration parameters for the Local Status of a Supervised Entity.

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. WdgMFailedAliveSupervisionRefCycleTol

- **UUID**: `ECUC:19ecddaa-c38c-4575-a851-33956ce42842`
- **参数名**: `WdgMFailedAliveSupervisionRefCycleTol`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter shall contain the acceptable amount of reference cycles with incorrect/failed alive supervisions for this Supervised Entity.

###### 引用关系

此容器包含 **1** 个引用：

####### SYMBOLIC-NAME-REFERENCE 类型引用

######## 1. WdgMLocalStatusSupervisedEntityRef

- **UUID**: `ECUC:2c458ef3-034f-45e3-ba86-70d08b59842a`
- **引用名**: `WdgMLocalStatusSupervisedEntityRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `WdgMSupervisedEntity`
- **完整路径**: `/AUTOSAR/EcucDefs/WdgM/WdgMGeneral/WdgMSupervisedEntity`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is the reference to the Supervised Entity for which the Local Status parameters are specified.

##### 9. WdgMTrigger

**容器属性**:

- **UUID**: `ECUC:b81d7037-a060-4e9c-9e16-175443d60577`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `WdgMTrigger`
- **多重性**: [0..255]
- **多配置容器**: false

**容器描述**:

This container collects all configuration parameters for the triggering of hardware watchdogs.

###### 参数配置

此容器包含 **2** 个参数：

####### INTEGER 类型参数

######## 1. WdgMTriggerConditionValue

- **UUID**: `ECUC:05108bc5-d328-4bf1-8cd9-bbc37c0b971a`
- **参数名**: `WdgMTriggerConditionValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter shall contain the value that is passed to WdgIf_SetTriggerCondition for this watchdog.

####### ENUMERATION 类型参数

######## 1. WdgMWatchdogMode

- **UUID**: `ECUC:b69101dc-fbeb-4530-8fba-7201fd38e3b5`
- **参数名**: `WdgMWatchdogMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `WDGIF_FAST_MODE` (来源: AUTOSAR_ECUC)
  - `WDGIF_OFF_MODE` (来源: AUTOSAR_ECUC)
  - `WDGIF_SLOW_MODE` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter contains the watchdog mode that shall be used for the referenced watchdog in this Watchdog Manager mode.

###### 引用关系

此容器包含 **1** 个引用：

####### SYMBOLIC-NAME-REFERENCE 类型引用

######## 1. WdgMTriggerWatchdogRef

- **UUID**: `ECUC:8f3d8b0f-8da6-4cf4-8ca0-31c89ffc4670`
- **引用名**: `WdgMTriggerWatchdogRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `WdgMWatchdog`
- **完整路径**: `/AUTOSAR/EcucDefs/WdgM/WdgMGeneral/WdgMWatchdog`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter is a reference to the configured watchdog.

##### 10. WdgMGeneral

**容器属性**:

- **UUID**: `ECUC:1755532e-b295-4ed0-8f64-04e06377e9a7`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `WdgMGeneral`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

Container defines all general configuration parameters of the Watchdog Manager.

###### 参数配置

此容器包含 **6** 个参数：

####### BOOLEAN 类型参数

######## 1. WdgMDefensiveBehavior

- **UUID**: `ECUC:8e23d4a8-05de-49af-8c47-40cd8bded4de`
- **参数名**: `WdgMDefensiveBehavior`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Preprocessor switch to enable/disable the defensive behavior of the Watchdog Manager module.

######## 2. WdgMDemStoppedSupervisionReport

- **UUID**: `ECUC:4a734197-70d0-48ae-a891-106170df87ea`
- **参数名**: `WdgMDemStoppedSupervisionReport`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Parameter to enable/disable the error reporting to DEM.

######## 3. WdgMDevErrorDetect

- **UUID**: `ECUC:7fadc294-2062-4035-b2db-c28f8a23faf8`
- **参数名**: `WdgMDevErrorDetect`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Preprocessor switch to enable/disable development error detection and reporting.

######## 4. WdgMImmediateReset

- **UUID**: `ECUC:641b480f-2063-44b0-af19-22b91539967c`
- **参数名**: `WdgMImmediateReset`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter enables/disablse the immediate reset feature in case of alive-supervision failure.

######## 5. WdgMOffModeEnabled

- **UUID**: `ECUC:794445b1-a701-4566-8042-30dd301b3602`
- **参数名**: `WdgMOffModeEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter enables/disables the selection of the "OffMode" of the watchdog driver.

######## 6. WdgMVersionInfoApi

- **UUID**: `ECUC:11f4b027-9e88-4470-a5fe-c42783064e79`
- **参数名**: `WdgMVersionInfoApi`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Preprocessor switch to enable/disable the existence of the API WdgM_GetVersionInfo. Shall be used to remove unneeded code segments.

###### 配置容器

本模块包含 **5** 个配置容器：

####### 1. WdgMCallerIds

**容器属性**:

- **UUID**: `ECUC:ba7d98cc-8a17-44c6-a11c-f4c2c60a7ea1`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `WdgMCallerIds`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Contains the definition of valid CallerIds for the callers who have permission to call the function WdgM_SetMode.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. WdgMCallerId

- **UUID**: `ECUC:b8c93e4b-2637-4197-a71f-a99a668878b5`
- **参数名**: `WdgMCallerId`
- **数据类型**: INTEGER
- **多重性**: [0..255]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines one valid CallerId for the callers who have permission to call the function WdgM_SetMode.

####### 2. WdgMSupervisedEntity

**容器属性**:

- **UUID**: `ECUC:5f5bb922-48ae-42f0-9451-736ac72782b0`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `WdgMSupervisedEntity`
- **多重性**: [0..65535]
- **多配置容器**: false

**容器描述**:

This container collects all common (mode-independent) parameters of a Supervised Entity to be supervised by the Watchdog Manager.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. WdgMSupervisedEntityId

- **UUID**: `ECUC:6fd59806-5dfc-4a53-b7a1-4da1ca289b9c`
- **参数名**: `WdgMSupervisedEntityId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter shall contain the unique identifier of the supervised entity.

######## 引用关系

此容器包含 **4** 个引用：

######### REFERENCE 类型引用

########## 1. WdgMEcucPartitionRef

- **UUID**: `ECUC:e6e1e8d5-8366-42ba-a3ef-2dac597eb971`
- **引用名**: `WdgMEcucPartitionRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `EcucPartition`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPartitionCollection/EcucPartition`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Denotes in which "EcucPartition" the supervised entity is executed. When the partition is stopped, the supervised entity shall be de-activated in the WdgM to avoid an ECU reset.

########## 2. WdgMOsApplicationRef

- **UUID**: `ECUC:082ceae7-4934-428c-874e-04da887f52e5`
- **引用名**: `WdgMOsApplicationRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `OsApplication`
- **完整路径**: `/AUTOSAR/EcucDefs/Os/OsApplication`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Optional reference to an OS Application. Beware, the Watchdog Manager module will trigger a partition restart of this OS Application when the corresponding Supervised Entity reaches WDGM_LOCAL_STATUS_FAILED.

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. WdgMInternalCheckpointInitialRef

- **UUID**: `ECUC:5746a48a-8ecd-4ef0-b1dd-3db3b2ae2dab`
- **引用名**: `WdgMInternalCheckpointInitialRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `WdgMCheckpoint`
- **完整路径**: `/AUTOSAR/EcucDefs/WdgM/WdgMGeneral/WdgMSupervisedEntity/WdgMCheckpoint`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is the reference to the initial Checkpoint for this Supervised Entity.

########## 2. WdgMInternallCheckpointFinalRef

- **UUID**: `ECUC:f8fe0091-0fc0-46e5-b54b-a0894bbd2ab7`
- **引用名**: `WdgMInternallCheckpointFinalRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..65535]
- **目标**: `WdgMCheckpoint`
- **完整路径**: `/AUTOSAR/EcucDefs/WdgM/WdgMGeneral/WdgMSupervisedEntity/WdgMCheckpoint`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is the reference to the final Checkpoint(s) for this Supervised Entity.

######## 配置容器

本模块包含 **2** 个配置容器：

######### 1. WdgMCheckpoint

**容器属性**:

- **UUID**: `ECUC:f25db5c0-5a1a-49a2-814c-0cea1de8c551`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `WdgMCheckpoint`
- **多重性**: [1..65535]
- **多配置容器**: false

**容器描述**:

This container collects all Checkpoints of this Supervised Entity. Each Supervised Entity has at least one Checkpoint.

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. WdgMCheckpointId

- **UUID**: `ECUC:2f217747-69c5-4c3c-8c30-98b776f7127b`
- **参数名**: `WdgMCheckpointId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter shall contain the unique identifier of Checkpoint.

######### 2. WdgMInternalTransition

**容器属性**:

- **UUID**: `ECUC:ef466640-151f-4554-8242-54b3cb11af12`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `WdgMInternalTransition`
- **多重性**: [0..65535]
- **多配置容器**: false

**容器描述**:

This container defines the graph of Internal Transitions within this Supervised Entity.

########## 引用关系

此容器包含 **2** 个引用：

########### SYMBOLIC-NAME-REFERENCE 类型引用

############ 1. WdgMInternalTransitionDestRef

- **UUID**: `ECUC:741dd3c3-e647-4757-9154-9dba9ce5150e`
- **引用名**: `WdgMInternalTransitionDestRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `WdgMCheckpoint`
- **完整路径**: `/AUTOSAR/EcucDefs/WdgM/WdgMGeneral/WdgMSupervisedEntity/WdgMCheckpoint`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is the reference to the destination Checkpoint of a Internal Transition within this Supervised Entity.

############ 2. WdgMInternalTransitionSourceRef

- **UUID**: `ECUC:0d6768c3-17dd-44d6-8a61-a6bc32cd79dd`
- **引用名**: `WdgMInternalTransitionSourceRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `WdgMCheckpoint`
- **完整路径**: `/AUTOSAR/EcucDefs/WdgM/WdgMGeneral/WdgMSupervisedEntity/WdgMCheckpoint`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is the reference to the source Checkpoint of a Internal Transition within this Supervised Entity.

####### 3. WdgMCheckpoint

**容器属性**:

- **UUID**: `ECUC:f25db5c0-5a1a-49a2-814c-0cea1de8c551`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `WdgMCheckpoint`
- **多重性**: [1..65535]
- **多配置容器**: false

**容器描述**:

This container collects all Checkpoints of this Supervised Entity. Each Supervised Entity has at least one Checkpoint.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. WdgMCheckpointId

- **UUID**: `ECUC:2f217747-69c5-4c3c-8c30-98b776f7127b`
- **参数名**: `WdgMCheckpointId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter shall contain the unique identifier of Checkpoint.

####### 4. WdgMInternalTransition

**容器属性**:

- **UUID**: `ECUC:ef466640-151f-4554-8242-54b3cb11af12`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `WdgMInternalTransition`
- **多重性**: [0..65535]
- **多配置容器**: false

**容器描述**:

This container defines the graph of Internal Transitions within this Supervised Entity.

######## 引用关系

此容器包含 **2** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. WdgMInternalTransitionDestRef

- **UUID**: `ECUC:741dd3c3-e647-4757-9154-9dba9ce5150e`
- **引用名**: `WdgMInternalTransitionDestRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `WdgMCheckpoint`
- **完整路径**: `/AUTOSAR/EcucDefs/WdgM/WdgMGeneral/WdgMSupervisedEntity/WdgMCheckpoint`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is the reference to the destination Checkpoint of a Internal Transition within this Supervised Entity.

########## 2. WdgMInternalTransitionSourceRef

- **UUID**: `ECUC:0d6768c3-17dd-44d6-8a61-a6bc32cd79dd`
- **引用名**: `WdgMInternalTransitionSourceRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `WdgMCheckpoint`
- **完整路径**: `/AUTOSAR/EcucDefs/WdgM/WdgMGeneral/WdgMSupervisedEntity/WdgMCheckpoint`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is the reference to the source Checkpoint of a Internal Transition within this Supervised Entity.

####### 5. WdgMWatchdog

**容器属性**:

- **UUID**: `ECUC:406fc502-fe65-4bb3-ac8c-2c67c4dff4f3`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `WdgMWatchdog`
- **多重性**: [0..255]
- **多配置容器**: false

**容器描述**:

This container collects all common (mode-independent) parameters of a Watchdog to be triggered by the Watchdog Manager.

######## 参数配置

此容器包含 **1** 个参数：

######### STRING 类型参数

########## 1. WdgMWatchdogName

- **UUID**: `ECUC:e143bfad-485e-49f5-9c9e-76afc19ac707`
- **参数名**: `WdgMWatchdogName`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter shall contain the symbolic name of the watchdog instance.

######## 引用关系

此容器包含 **1** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. WdgMWatchdogDeviceRef

- **UUID**: `ECUC:befa2f09-fb95-4cd7-ae44-b972712b6298`
- **引用名**: `WdgMWatchdogDeviceRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `WdgIfDevice`
- **完整路径**: `/AUTOSAR/EcucDefs/WdgIf/WdgIfDevice`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to one device container of Watchdog Interface. In the referenced container WdgIfDevice, the parameter WdgIfDeviceIndex contains the Index parameter that WdgM has to use for WdgIf_SetTriggerCondition calls for that watchdog instance.

##### 11. WdgMCallerIds

**容器属性**:

- **UUID**: `ECUC:ba7d98cc-8a17-44c6-a11c-f4c2c60a7ea1`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `WdgMCallerIds`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Contains the definition of valid CallerIds for the callers who have permission to call the function WdgM_SetMode.

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. WdgMCallerId

- **UUID**: `ECUC:b8c93e4b-2637-4197-a71f-a99a668878b5`
- **参数名**: `WdgMCallerId`
- **数据类型**: INTEGER
- **多重性**: [0..255]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines one valid CallerId for the callers who have permission to call the function WdgM_SetMode.

##### 12. WdgMSupervisedEntity

**容器属性**:

- **UUID**: `ECUC:5f5bb922-48ae-42f0-9451-736ac72782b0`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `WdgMSupervisedEntity`
- **多重性**: [0..65535]
- **多配置容器**: false

**容器描述**:

This container collects all common (mode-independent) parameters of a Supervised Entity to be supervised by the Watchdog Manager.

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. WdgMSupervisedEntityId

- **UUID**: `ECUC:6fd59806-5dfc-4a53-b7a1-4da1ca289b9c`
- **参数名**: `WdgMSupervisedEntityId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter shall contain the unique identifier of the supervised entity.

###### 引用关系

此容器包含 **4** 个引用：

####### REFERENCE 类型引用

######## 1. WdgMEcucPartitionRef

- **UUID**: `ECUC:e6e1e8d5-8366-42ba-a3ef-2dac597eb971`
- **引用名**: `WdgMEcucPartitionRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `EcucPartition`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPartitionCollection/EcucPartition`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Denotes in which "EcucPartition" the supervised entity is executed. When the partition is stopped, the supervised entity shall be de-activated in the WdgM to avoid an ECU reset.

######## 2. WdgMOsApplicationRef

- **UUID**: `ECUC:082ceae7-4934-428c-874e-04da887f52e5`
- **引用名**: `WdgMOsApplicationRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `OsApplication`
- **完整路径**: `/AUTOSAR/EcucDefs/Os/OsApplication`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Optional reference to an OS Application. Beware, the Watchdog Manager module will trigger a partition restart of this OS Application when the corresponding Supervised Entity reaches WDGM_LOCAL_STATUS_FAILED.

####### SYMBOLIC-NAME-REFERENCE 类型引用

######## 1. WdgMInternalCheckpointInitialRef

- **UUID**: `ECUC:5746a48a-8ecd-4ef0-b1dd-3db3b2ae2dab`
- **引用名**: `WdgMInternalCheckpointInitialRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `WdgMCheckpoint`
- **完整路径**: `/AUTOSAR/EcucDefs/WdgM/WdgMGeneral/WdgMSupervisedEntity/WdgMCheckpoint`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is the reference to the initial Checkpoint for this Supervised Entity.

######## 2. WdgMInternallCheckpointFinalRef

- **UUID**: `ECUC:f8fe0091-0fc0-46e5-b54b-a0894bbd2ab7`
- **引用名**: `WdgMInternallCheckpointFinalRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..65535]
- **目标**: `WdgMCheckpoint`
- **完整路径**: `/AUTOSAR/EcucDefs/WdgM/WdgMGeneral/WdgMSupervisedEntity/WdgMCheckpoint`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is the reference to the final Checkpoint(s) for this Supervised Entity.

###### 配置容器

本模块包含 **2** 个配置容器：

####### 1. WdgMCheckpoint

**容器属性**:

- **UUID**: `ECUC:f25db5c0-5a1a-49a2-814c-0cea1de8c551`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `WdgMCheckpoint`
- **多重性**: [1..65535]
- **多配置容器**: false

**容器描述**:

This container collects all Checkpoints of this Supervised Entity. Each Supervised Entity has at least one Checkpoint.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. WdgMCheckpointId

- **UUID**: `ECUC:2f217747-69c5-4c3c-8c30-98b776f7127b`
- **参数名**: `WdgMCheckpointId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter shall contain the unique identifier of Checkpoint.

####### 2. WdgMInternalTransition

**容器属性**:

- **UUID**: `ECUC:ef466640-151f-4554-8242-54b3cb11af12`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `WdgMInternalTransition`
- **多重性**: [0..65535]
- **多配置容器**: false

**容器描述**:

This container defines the graph of Internal Transitions within this Supervised Entity.

######## 引用关系

此容器包含 **2** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. WdgMInternalTransitionDestRef

- **UUID**: `ECUC:741dd3c3-e647-4757-9154-9dba9ce5150e`
- **引用名**: `WdgMInternalTransitionDestRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `WdgMCheckpoint`
- **完整路径**: `/AUTOSAR/EcucDefs/WdgM/WdgMGeneral/WdgMSupervisedEntity/WdgMCheckpoint`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is the reference to the destination Checkpoint of a Internal Transition within this Supervised Entity.

########## 2. WdgMInternalTransitionSourceRef

- **UUID**: `ECUC:0d6768c3-17dd-44d6-8a61-a6bc32cd79dd`
- **引用名**: `WdgMInternalTransitionSourceRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `WdgMCheckpoint`
- **完整路径**: `/AUTOSAR/EcucDefs/WdgM/WdgMGeneral/WdgMSupervisedEntity/WdgMCheckpoint`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is the reference to the source Checkpoint of a Internal Transition within this Supervised Entity.

##### 13. WdgMCheckpoint

**容器属性**:

- **UUID**: `ECUC:f25db5c0-5a1a-49a2-814c-0cea1de8c551`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `WdgMCheckpoint`
- **多重性**: [1..65535]
- **多配置容器**: false

**容器描述**:

This container collects all Checkpoints of this Supervised Entity. Each Supervised Entity has at least one Checkpoint.

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. WdgMCheckpointId

- **UUID**: `ECUC:2f217747-69c5-4c3c-8c30-98b776f7127b`
- **参数名**: `WdgMCheckpointId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter shall contain the unique identifier of Checkpoint.

##### 14. WdgMInternalTransition

**容器属性**:

- **UUID**: `ECUC:ef466640-151f-4554-8242-54b3cb11af12`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `WdgMInternalTransition`
- **多重性**: [0..65535]
- **多配置容器**: false

**容器描述**:

This container defines the graph of Internal Transitions within this Supervised Entity.

###### 引用关系

此容器包含 **2** 个引用：

####### SYMBOLIC-NAME-REFERENCE 类型引用

######## 1. WdgMInternalTransitionDestRef

- **UUID**: `ECUC:741dd3c3-e647-4757-9154-9dba9ce5150e`
- **引用名**: `WdgMInternalTransitionDestRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `WdgMCheckpoint`
- **完整路径**: `/AUTOSAR/EcucDefs/WdgM/WdgMGeneral/WdgMSupervisedEntity/WdgMCheckpoint`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is the reference to the destination Checkpoint of a Internal Transition within this Supervised Entity.

######## 2. WdgMInternalTransitionSourceRef

- **UUID**: `ECUC:0d6768c3-17dd-44d6-8a61-a6bc32cd79dd`
- **引用名**: `WdgMInternalTransitionSourceRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `WdgMCheckpoint`
- **完整路径**: `/AUTOSAR/EcucDefs/WdgM/WdgMGeneral/WdgMSupervisedEntity/WdgMCheckpoint`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is the reference to the source Checkpoint of a Internal Transition within this Supervised Entity.

##### 15. WdgMWatchdog

**容器属性**:

- **UUID**: `ECUC:406fc502-fe65-4bb3-ac8c-2c67c4dff4f3`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `WdgMWatchdog`
- **多重性**: [0..255]
- **多配置容器**: false

**容器描述**:

This container collects all common (mode-independent) parameters of a Watchdog to be triggered by the Watchdog Manager.

###### 参数配置

此容器包含 **1** 个参数：

####### STRING 类型参数

######## 1. WdgMWatchdogName

- **UUID**: `ECUC:e143bfad-485e-49f5-9c9e-76afc19ac707`
- **参数名**: `WdgMWatchdogName`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter shall contain the symbolic name of the watchdog instance.

###### 引用关系

此容器包含 **1** 个引用：

####### SYMBOLIC-NAME-REFERENCE 类型引用

######## 1. WdgMWatchdogDeviceRef

- **UUID**: `ECUC:befa2f09-fb95-4cd7-ae44-b972712b6298`
- **引用名**: `WdgMWatchdogDeviceRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `WdgIfDevice`
- **完整路径**: `/AUTOSAR/EcucDefs/WdgIf/WdgIfDevice`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to one device container of Watchdog Interface. In the referenced container WdgIfDevice, the parameter WdgIfDeviceIndex contains the Index parameter that WdgM has to use for WdgIf_SetTriggerCondition calls for that watchdog instance.

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

1. **WdgM**
