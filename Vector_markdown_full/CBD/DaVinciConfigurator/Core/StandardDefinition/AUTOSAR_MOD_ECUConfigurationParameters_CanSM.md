# CanSM - 完整配置文档

*此文档由ARXML文件自动生成，采用层次化结构展示*

**生成时间**: 2025-06-16 14:46:07

## 📑 目录

- [📄 文件信息](#-文件信息)
- [🔧 模块定义](#-模块定义)
  - [CanSM](#cansm)
- [📦 包结构](#-包结构)

## 📄 文件信息

### Schema信息
- **Schema位置**: `http://autosar.org/schema/r4.0 AUTOSAR_4-0-3.xsd`
- **命名空间**: `http://autosar.org/schema/r4.0`

## 🔧 模块定义

### 1. CanSM

#### 基本信息

- **UUID**: `ECUC:f603bffb-40d3-4056-be94-e28fd5eb1312`
- **模块名称**: `CanSM`
- **多重性**: [0..1]
- **支持的变体**:
  - VARIANT-LINK-TIME
  - VARIANT-POST-BUILD
  - VARIANT-PRE-COMPILE

#### 模块描述

Configuration of the CanSM module

#### 版本历史

共有 **1** 个版本记录：

##### 1. 版本 4.2.0

- **发布日期**: 2011-11-09
- **发布者**: AUTOSAR

*此版本无详细变更记录*

#### 配置容器

本模块包含 **5** 个配置容器：

##### 1. CanSMConfiguration

**容器属性**:

- **UUID**: `ECUC:2aff0394-611e-4368-b4e7-7551f7e10881`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CanSMConfiguration`
- **多重性**: [1..1]
- **多配置容器**: true

**容器描述**:

This container contains the global parameters of the CanSM and sub containers, which are for the CAN network specific configuration.

###### 参数配置

此容器包含 **2** 个参数：

####### INTEGER 类型参数

######## 1. CanSMModeRequestRepetitionMax

- **UUID**: `ECUC:fbd6f32b-a40f-4cb0-b0aa-ec95515d4924`
- **参数名**: `CanSMModeRequestRepetitionMax`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies the maximal amount of mode request repetitions without a respective mode indication from the CanIf module until the CanSM module reports a development error to the DET and tries to go back to no communication.

####### FLOAT 类型参数

######## 1. CanSMModeRequestRepetitionTime

- **UUID**: `ECUC:17b52ad9-6aa7-4241-92ee-a2473d8d919e`
- **参数名**: `CanSMModeRequestRepetitionTime`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0..65.535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies in which time duration the CanSM module shall repeat mode change requests by using the API of the CanIf module.

###### 配置容器

本模块包含 **3** 个配置容器：

####### 1. CanSMManagerNetwork

**容器属性**:

- **UUID**: `ECUC:d75eddcc-261d-499f-acf6-db8f46ad12ac`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CanSMManagerNetwork`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

This container contains the CAN network specific parameters of each CAN network

######## 参数配置

此容器包含 **5** 个参数：

######### INTEGER 类型参数

########## 1. CanSMBorCounterL1ToL2

- **UUID**: `ECUC:6afd2490-63a3-408a-acc7-6a259c18911b`
- **参数名**: `CanSMBorCounterL1ToL2`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This threshold defines the count of bus-offs until the bus-off recovery switches from level 1 (short recovery time) to level 2 (long recovery time).

######### BOOLEAN 类型参数

########## 1. CanSMBorTxConfirmationPolling

- **UUID**: `ECUC:d1288eea-fa2e-4cba-8f62-4d06654c68e9`
- **参数名**: `CanSMBorTxConfirmationPolling`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter shall configure, if the CanSM polls the CanIf_GetTxConfirmationState API to decide the bus-off state to be recovered instead of using the CanSMBorTimeTxEnsured parameter for this decision.

######### FLOAT 类型参数

########## 1. CanSMBorTimeL1

- **UUID**: `ECUC:553a838d-8ff8-45d0-8076-14a532d9c971`
- **参数名**: `CanSMBorTimeL1`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0..65.535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This time parameter defines in seconds the duration of the bus-off recovery time in level 1 (short recovery time).

########## 2. CanSMBorTimeL2

- **UUID**: `ECUC:16f2464e-677a-481d-b40c-8a12e3a5bd08`
- **参数名**: `CanSMBorTimeL2`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0..65.535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This time parameter defines in seconds the duration of the bus-off recovery time in level 2 (long recovery time).

########## 3. CanSMBorTimeTxEnsured

- **UUID**: `ECUC:172eb209-1cd3-4a9b-b0e2-0ed59e940257`
- **参数名**: `CanSMBorTimeTxEnsured`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0..65.535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines in seconds the duration of the bus-off event check. This check assesses, if the recovery has been successful after the recovery reenables the transmit path. If a new bus-off occurs during this time period, the CanSM assesses this bus-off as sequential bus-off without successful recovery. Because a bus-off only can be detected, when PDUs are transmitted, the time has to be great enough to ensure that PDUs are transmitted again (e. g. time period of the fastest cyclic transmitted PDU of the COM module / ComTxModeTimePeriodFactor).

######## 引用关系

此容器包含 **2** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. CanSMComMNetworkHandleRef

- **UUID**: `ECUC:38d80a04-8ea5-4ef0-a73d-fccc98346f9e`
- **引用名**: `CanSMComMNetworkHandleRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `ComMChannel`
- **完整路径**: `/AUTOSAR/EcucDefs/ComM/ComMConfigSet/ComMChannel`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Unique handle to identify one certain CAN network. Reference to one of the network handles configured for the ComM.

########## 2. CanSMTransceiverId

- **UUID**: `ECUC:6901aaa5-9333-4715-af47-ff3256224be4`
- **引用名**: `CanSMTransceiverId`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `CanIfTrcvCfg`
- **完整路径**: `/AUTOSAR/EcucDefs/CanIf/CanIfTrcvDrvCfg/CanIfTrcvCfg`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: ID of the CAN transceiver assigned to the configured network handle. Reference to one of the transceivers managed by the CanIf module.

######## 配置容器

本模块包含 **2** 个配置容器：

######### 1. CanSMController

**容器属性**:

- **UUID**: `ECUC:e1a0044e-723d-42ba-b1db-3b376c29d4d8`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CanSMController`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

This container contains the controller IDs assigned to a CAN network.

########## 引用关系

此容器包含 **1** 个引用：

########### SYMBOLIC-NAME-REFERENCE 类型引用

############ 1. CanSMControllerId

- **UUID**: `ECUC:aeebc335-a75f-4d6d-a66a-3168d73982e8`
- **引用名**: `CanSMControllerId`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `CanIfCtrlCfg`
- **完整路径**: `/AUTOSAR/EcucDefs/CanIf/CanIfCtrlDrvCfg/CanIfCtrlCfg`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Unique handle to identify one certain CAN controller. Reference to one of the CAN controllers managed by the CanIf module.

######### 2. CanSMDemEventParameterRefs

**容器属性**:

- **UUID**: `ECUC:a10827ae-af02-4cd0-abc9-db0aa085c1c1`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CanSMDemEventParameterRefs`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Container for the references to DemEventParameter elements which shall be invoked using the API Dem_ReportErrorStatus API in case the corresponding error occurs. The EventId is taken from the referenced DemEventParameter's DemEventId value. The standardized errors are provided in the container and can be extended by vendor specific error references.

########## 引用关系

此容器包含 **1** 个引用：

########### SYMBOLIC-NAME-REFERENCE 类型引用

############ 1. CANSM_E_BUS_OFF

- **UUID**: `ECUC:c5a06f69-0d10-47ef-8af5-21c9188e5c5d`
- **引用名**: `CANSM_E_BUS_OFF`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `DemEventParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemConfigSet/DemEventParameter`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to configured DEM event to report bus off errors for this CAN network.

####### 2. CanSMController

**容器属性**:

- **UUID**: `ECUC:e1a0044e-723d-42ba-b1db-3b376c29d4d8`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CanSMController`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

This container contains the controller IDs assigned to a CAN network.

######## 引用关系

此容器包含 **1** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. CanSMControllerId

- **UUID**: `ECUC:aeebc335-a75f-4d6d-a66a-3168d73982e8`
- **引用名**: `CanSMControllerId`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `CanIfCtrlCfg`
- **完整路径**: `/AUTOSAR/EcucDefs/CanIf/CanIfCtrlDrvCfg/CanIfCtrlCfg`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Unique handle to identify one certain CAN controller. Reference to one of the CAN controllers managed by the CanIf module.

####### 3. CanSMDemEventParameterRefs

**容器属性**:

- **UUID**: `ECUC:a10827ae-af02-4cd0-abc9-db0aa085c1c1`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CanSMDemEventParameterRefs`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Container for the references to DemEventParameter elements which shall be invoked using the API Dem_ReportErrorStatus API in case the corresponding error occurs. The EventId is taken from the referenced DemEventParameter's DemEventId value. The standardized errors are provided in the container and can be extended by vendor specific error references.

######## 引用关系

此容器包含 **1** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. CANSM_E_BUS_OFF

- **UUID**: `ECUC:c5a06f69-0d10-47ef-8af5-21c9188e5c5d`
- **引用名**: `CANSM_E_BUS_OFF`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `DemEventParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemConfigSet/DemEventParameter`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to configured DEM event to report bus off errors for this CAN network.

##### 2. CanSMManagerNetwork

**容器属性**:

- **UUID**: `ECUC:d75eddcc-261d-499f-acf6-db8f46ad12ac`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CanSMManagerNetwork`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

This container contains the CAN network specific parameters of each CAN network

###### 参数配置

此容器包含 **5** 个参数：

####### INTEGER 类型参数

######## 1. CanSMBorCounterL1ToL2

- **UUID**: `ECUC:6afd2490-63a3-408a-acc7-6a259c18911b`
- **参数名**: `CanSMBorCounterL1ToL2`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This threshold defines the count of bus-offs until the bus-off recovery switches from level 1 (short recovery time) to level 2 (long recovery time).

####### BOOLEAN 类型参数

######## 1. CanSMBorTxConfirmationPolling

- **UUID**: `ECUC:d1288eea-fa2e-4cba-8f62-4d06654c68e9`
- **参数名**: `CanSMBorTxConfirmationPolling`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter shall configure, if the CanSM polls the CanIf_GetTxConfirmationState API to decide the bus-off state to be recovered instead of using the CanSMBorTimeTxEnsured parameter for this decision.

####### FLOAT 类型参数

######## 1. CanSMBorTimeL1

- **UUID**: `ECUC:553a838d-8ff8-45d0-8076-14a532d9c971`
- **参数名**: `CanSMBorTimeL1`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0..65.535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This time parameter defines in seconds the duration of the bus-off recovery time in level 1 (short recovery time).

######## 2. CanSMBorTimeL2

- **UUID**: `ECUC:16f2464e-677a-481d-b40c-8a12e3a5bd08`
- **参数名**: `CanSMBorTimeL2`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0..65.535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This time parameter defines in seconds the duration of the bus-off recovery time in level 2 (long recovery time).

######## 3. CanSMBorTimeTxEnsured

- **UUID**: `ECUC:172eb209-1cd3-4a9b-b0e2-0ed59e940257`
- **参数名**: `CanSMBorTimeTxEnsured`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0..65.535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines in seconds the duration of the bus-off event check. This check assesses, if the recovery has been successful after the recovery reenables the transmit path. If a new bus-off occurs during this time period, the CanSM assesses this bus-off as sequential bus-off without successful recovery. Because a bus-off only can be detected, when PDUs are transmitted, the time has to be great enough to ensure that PDUs are transmitted again (e. g. time period of the fastest cyclic transmitted PDU of the COM module / ComTxModeTimePeriodFactor).

###### 引用关系

此容器包含 **2** 个引用：

####### SYMBOLIC-NAME-REFERENCE 类型引用

######## 1. CanSMComMNetworkHandleRef

- **UUID**: `ECUC:38d80a04-8ea5-4ef0-a73d-fccc98346f9e`
- **引用名**: `CanSMComMNetworkHandleRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `ComMChannel`
- **完整路径**: `/AUTOSAR/EcucDefs/ComM/ComMConfigSet/ComMChannel`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Unique handle to identify one certain CAN network. Reference to one of the network handles configured for the ComM.

######## 2. CanSMTransceiverId

- **UUID**: `ECUC:6901aaa5-9333-4715-af47-ff3256224be4`
- **引用名**: `CanSMTransceiverId`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `CanIfTrcvCfg`
- **完整路径**: `/AUTOSAR/EcucDefs/CanIf/CanIfTrcvDrvCfg/CanIfTrcvCfg`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: ID of the CAN transceiver assigned to the configured network handle. Reference to one of the transceivers managed by the CanIf module.

###### 配置容器

本模块包含 **2** 个配置容器：

####### 1. CanSMController

**容器属性**:

- **UUID**: `ECUC:e1a0044e-723d-42ba-b1db-3b376c29d4d8`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CanSMController`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

This container contains the controller IDs assigned to a CAN network.

######## 引用关系

此容器包含 **1** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. CanSMControllerId

- **UUID**: `ECUC:aeebc335-a75f-4d6d-a66a-3168d73982e8`
- **引用名**: `CanSMControllerId`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `CanIfCtrlCfg`
- **完整路径**: `/AUTOSAR/EcucDefs/CanIf/CanIfCtrlDrvCfg/CanIfCtrlCfg`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Unique handle to identify one certain CAN controller. Reference to one of the CAN controllers managed by the CanIf module.

####### 2. CanSMDemEventParameterRefs

**容器属性**:

- **UUID**: `ECUC:a10827ae-af02-4cd0-abc9-db0aa085c1c1`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CanSMDemEventParameterRefs`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Container for the references to DemEventParameter elements which shall be invoked using the API Dem_ReportErrorStatus API in case the corresponding error occurs. The EventId is taken from the referenced DemEventParameter's DemEventId value. The standardized errors are provided in the container and can be extended by vendor specific error references.

######## 引用关系

此容器包含 **1** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. CANSM_E_BUS_OFF

- **UUID**: `ECUC:c5a06f69-0d10-47ef-8af5-21c9188e5c5d`
- **引用名**: `CANSM_E_BUS_OFF`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `DemEventParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemConfigSet/DemEventParameter`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to configured DEM event to report bus off errors for this CAN network.

##### 3. CanSMController

**容器属性**:

- **UUID**: `ECUC:e1a0044e-723d-42ba-b1db-3b376c29d4d8`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CanSMController`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

This container contains the controller IDs assigned to a CAN network.

###### 引用关系

此容器包含 **1** 个引用：

####### SYMBOLIC-NAME-REFERENCE 类型引用

######## 1. CanSMControllerId

- **UUID**: `ECUC:aeebc335-a75f-4d6d-a66a-3168d73982e8`
- **引用名**: `CanSMControllerId`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `CanIfCtrlCfg`
- **完整路径**: `/AUTOSAR/EcucDefs/CanIf/CanIfCtrlDrvCfg/CanIfCtrlCfg`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Unique handle to identify one certain CAN controller. Reference to one of the CAN controllers managed by the CanIf module.

##### 4. CanSMDemEventParameterRefs

**容器属性**:

- **UUID**: `ECUC:a10827ae-af02-4cd0-abc9-db0aa085c1c1`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CanSMDemEventParameterRefs`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Container for the references to DemEventParameter elements which shall be invoked using the API Dem_ReportErrorStatus API in case the corresponding error occurs. The EventId is taken from the referenced DemEventParameter's DemEventId value. The standardized errors are provided in the container and can be extended by vendor specific error references.

###### 引用关系

此容器包含 **1** 个引用：

####### SYMBOLIC-NAME-REFERENCE 类型引用

######## 1. CANSM_E_BUS_OFF

- **UUID**: `ECUC:c5a06f69-0d10-47ef-8af5-21c9188e5c5d`
- **引用名**: `CANSM_E_BUS_OFF`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `DemEventParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemConfigSet/DemEventParameter`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to configured DEM event to report bus off errors for this CAN network.

##### 5. CanSMGeneral

**容器属性**:

- **UUID**: `ECUC:7df54934-eb9b-4605-96f3-8d0c28ba3ac8`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CanSMGeneral`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

Container for general pre-compile parameters of the CanSM module

###### 参数配置

此容器包含 **4** 个参数：

####### BOOLEAN 类型参数

######## 1. CanSMDevErrorDetect

- **UUID**: `ECUC:db5c43c4-2a04-4668-aa92-e6293ca26ac6`
- **参数名**: `CanSMDevErrorDetect`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enables and disables the development error detection and notification mechanism.

######## 2. CanSMVersionInfoApi

- **UUID**: `ECUC:755ac5e7-3bfb-458e-bf62-971dd0929455`
- **参数名**: `CanSMVersionInfoApi`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Activate/Deactivate the version information API (CanSM_GetVersionInfo).

######## 3. CanSmChangeBaudrateApi

- **UUID**: `ECUC:e867d5e0-54d8-4148-85f7-5b893481a47a`
- **参数名**: `CanSmChangeBaudrateApi`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The support of the Can_ChangeBaudrate API is optional.

####### FLOAT 类型参数

######## 1. CanSMMainFunctionTimePeriod

- **UUID**: `ECUC:753ef3fc-9b30-415b-a21a-b272e7629216`
- **参数名**: `CanSMMainFunctionTimePeriod`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0.001..65.535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the cycle time of the function CanSM_MainFunction in seconds

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

1. **CanSM**
