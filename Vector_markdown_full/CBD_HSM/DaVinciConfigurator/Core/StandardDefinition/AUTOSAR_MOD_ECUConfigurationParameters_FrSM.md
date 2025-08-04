# FrSM - 完整配置文档

*此文档由ARXML文件自动生成，采用层次化结构展示*

**生成时间**: 2025-06-16 14:51:48

## 📑 目录

- [📄 文件信息](#-文件信息)
- [🔧 模块定义](#-模块定义)
  - [FrSM](#frsm)
- [📦 包结构](#-包结构)

## 📄 文件信息

### Schema信息
- **Schema位置**: `http://autosar.org/schema/r4.0 AUTOSAR_4-0-3.xsd`
- **命名空间**: `http://autosar.org/schema/r4.0`

## 🔧 模块定义

### 1. FrSM

#### 基本信息

- **UUID**: `ECUC:a98879b6-730a-48f4-9008-57f9d3935f4e`
- **模块名称**: `FrSM`
- **多重性**: [0..1]
- **支持的变体**:
  - VARIANT-LINK-TIME
  - VARIANT-POST-BUILD
  - VARIANT-PRE-COMPILE

#### 模块描述

Configuration of the FlexRay State Manager

#### 版本历史

共有 **1** 个版本记录：

##### 1. 版本 4.2.0

- **发布日期**: 2011-11-09
- **发布者**: AUTOSAR

*此版本无详细变更记录*

#### 配置容器

本模块包含 **4** 个配置容器：

##### 1. FrSMConfig

**容器属性**:

- **UUID**: `ECUC:88a6c179-1037-456f-b051-ba1e0e60df4e`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FrSMConfig`
- **多重性**: [1..1]
- **多配置容器**: true

**容器描述**:

This container comprises the cluster specific configuration of the FlexRay State Manager.

###### 配置容器

本模块包含 **2** 个配置容器：

####### 1. FrSMCluster

**容器属性**:

- **UUID**: `ECUC:06ffd925-d47c-4e72-ac9f-f4c5493e0f74`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FrSMCluster`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

This container specifies a FlexRay cluster and all related data. A FlexRay cluster may consist of more than one controller per ECU.

######## 参数配置

此容器包含 **12** 个参数：

######### INTEGER 类型参数

########## 1. FrSMMinNumberOfColdstarter

- **UUID**: `ECUC:68fdc9b4-34e0-4c84-9828-47f0a4738e51`
- **参数名**: `FrSMMinNumberOfColdstarter`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the number of coldstarter that should not be underrun. If this parameter is not configured the mainfunction shall not check the number of startup frames.

########## 2. FrSMNumWakeupPatterns

- **UUID**: `ECUC:4cd61d2c-be6c-46ff-a7b8-764e9ab3dd1b`
- **参数名**: `FrSMNumWakeupPatterns`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Maximum number of Wakeup Patterns the node may send before going to FRSM_STARTUP.

########## 3. FrSMStartupRepetitions

- **UUID**: `ECUC:d56fbbc1-2025-4426-89b4-b830a9025719`
- **参数名**: `FrSMStartupRepetitions`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The number of times an ECU may repeat the startup procedure for a FlexRay cluster.

########## 4. FrSMStartupRepetitionsWithWakeup

- **UUID**: `ECUC:254df245-0739-438d-9785-f139d395c9df`
- **参数名**: `FrSMStartupRepetitionsWithWakeup`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The number of times an ECU may repeat the startup procedure including a wakeup for a FlexRay cluster.

######### BOOLEAN 类型参数

########## 1. FrSMCheckWakeupReason

- **UUID**: `ECUC:44f793fc-177a-4598-b96a-a0cd92f520e2`
- **参数名**: `FrSMCheckWakeupReason`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: If FrSMCheckWakeupReason  is true, the FrSM will check the wakeup reason in order to skip the wakeup in case of wakeup by bus. If FrSMCheckWakeupReason  is false, the FrSM will always try to perform a wakeup.

########## 2. FrSMDelayStartupWithoutWakeup

- **UUID**: `ECUC:6cec37d5-45df-413b-a43e-039bc6eb3805`
- **参数名**: `FrSMDelayStartupWithoutWakeup`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: If true, timer t1 shall be started instead of immediately calling FrIf_AllowColdstart in case of a startup without wakeup.

########## 3. FrSMIsColdstartEcu

- **UUID**: `ECUC:d006fe48-3419-4c48-9b4f-0c79d70b17a5`
- **参数名**: `FrSMIsColdstartEcu`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: True: The ECU is a coldstart node for this FlexRay cluster.

########## 4. FrSMIsWakeupEcu

- **UUID**: `ECUC:775480ae-171e-4527-8024-c8c94e5b7844`
- **参数名**: `FrSMIsWakeupEcu`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: True: FrSM shall perform a wakeup for this cluster.

######### FLOAT 类型参数

########## 1. FrSMDurationT1

- **UUID**: `ECUC:d062fcc7-b32d-4669-ab94-f0cbfa827199`
- **参数名**: `FrSMDurationT1`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0..Inf]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The duration of timer t1 in seconds.

########## 2. FrSMDurationT2

- **UUID**: `ECUC:df901f89-f193-4d1e-8ea0-387ca7ff1fd5`
- **参数名**: `FrSMDurationT2`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0..Inf]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The duration of timer t2 in seconds.

########## 3. FrSMDurationT3

- **UUID**: `ECUC:d68c5e6b-b23e-4437-8cc3-bb9444d5069d`
- **参数名**: `FrSMDurationT3`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0..Inf]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The duration of timer t3 in seconds. The value of this parameter shall be larger than the value of FrSMDurationT1 parameter.

########## 4. FrSMMainFunctionCycleTime

- **UUID**: `ECUC:db31e4f1-2f37-495e-ab4d-465746a7d5a3`
- **参数名**: `FrSMMainFunctionCycleTime`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0..Inf]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the cycle time in seconds of the periodic calling of FrSM main function.

######## 引用关系

此容器包含 **2** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. FrSMComMNetworkHandleRef

- **UUID**: `ECUC:e2b79c8a-5548-4ed9-af29-350b61ae85df`
- **引用名**: `FrSMComMNetworkHandleRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `ComMChannel`
- **完整路径**: `/AUTOSAR/EcucDefs/ComM/ComMConfigSet/ComMChannel`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the unique handle to identify one certain FlexRay network correspond to one of the network handles of the ComM configuration.

########## 2. FrSMFrIfClusterRef

- **UUID**: `ECUC:dd461cfe-0a31-43a8-8446-3d8f2358423f`
- **引用名**: `FrSMFrIfClusterRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `FrIfCluster`
- **完整路径**: `/AUTOSAR/EcucDefs/FrIf/FrIfConfig/FrIfCluster`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: References the cluster configuration in the FlexRay Interface configuration.

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. FrSMClusterDemEventParameterRefs

**容器属性**:

- **UUID**: `ECUC:9f8654da-17b0-427d-8b3f-bdb04c809a83`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FrSMClusterDemEventParameterRefs`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Container for the references to DemEventParameter elements which shall be invoked using the API Dem_ReportErrorStatus in case the corresponding error occurs. The EventId is taken from the referenced DemEventParameter's DemEventId value.

########## 引用关系

此容器包含 **2** 个引用：

########### SYMBOLIC-NAME-REFERENCE 类型引用

############ 1. FRSM_E_CLUSTER_STARTUP

- **UUID**: `ECUC:637b2fa5-031c-4c62-8b02-eb0313e3b92d`
- **引用名**: `FRSM_E_CLUSTER_STARTUP`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `DemEventParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemConfigSet/DemEventParameter`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the DemEventParameter which shall be issued when the error "FRSM_E_CLUSTER_STARTUP" has occured. If the reference is not configured the error shall be reported as DET error.

############ 2. FRSM_E_CLUSTER_SYNC_LOSS

- **UUID**: `ECUC:30585f0b-2439-441e-8cbd-d7d6e7b51ae1`
- **引用名**: `FRSM_E_CLUSTER_SYNC_LOSS`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `DemEventParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemConfigSet/DemEventParameter`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the DemEventParameter which shall be issued when the error "FRSM_E_CLUSTER_SYNC_LOSS" has occurred. If the reference is not configured the error shall be reported as DET error.

####### 2. FrSMClusterDemEventParameterRefs

**容器属性**:

- **UUID**: `ECUC:9f8654da-17b0-427d-8b3f-bdb04c809a83`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FrSMClusterDemEventParameterRefs`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Container for the references to DemEventParameter elements which shall be invoked using the API Dem_ReportErrorStatus in case the corresponding error occurs. The EventId is taken from the referenced DemEventParameter's DemEventId value.

######## 引用关系

此容器包含 **2** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. FRSM_E_CLUSTER_STARTUP

- **UUID**: `ECUC:637b2fa5-031c-4c62-8b02-eb0313e3b92d`
- **引用名**: `FRSM_E_CLUSTER_STARTUP`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `DemEventParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemConfigSet/DemEventParameter`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the DemEventParameter which shall be issued when the error "FRSM_E_CLUSTER_STARTUP" has occured. If the reference is not configured the error shall be reported as DET error.

########## 2. FRSM_E_CLUSTER_SYNC_LOSS

- **UUID**: `ECUC:30585f0b-2439-441e-8cbd-d7d6e7b51ae1`
- **引用名**: `FRSM_E_CLUSTER_SYNC_LOSS`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `DemEventParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemConfigSet/DemEventParameter`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the DemEventParameter which shall be issued when the error "FRSM_E_CLUSTER_SYNC_LOSS" has occurred. If the reference is not configured the error shall be reported as DET error.

##### 2. FrSMCluster

**容器属性**:

- **UUID**: `ECUC:06ffd925-d47c-4e72-ac9f-f4c5493e0f74`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FrSMCluster`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

This container specifies a FlexRay cluster and all related data. A FlexRay cluster may consist of more than one controller per ECU.

###### 参数配置

此容器包含 **12** 个参数：

####### INTEGER 类型参数

######## 1. FrSMMinNumberOfColdstarter

- **UUID**: `ECUC:68fdc9b4-34e0-4c84-9828-47f0a4738e51`
- **参数名**: `FrSMMinNumberOfColdstarter`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the number of coldstarter that should not be underrun. If this parameter is not configured the mainfunction shall not check the number of startup frames.

######## 2. FrSMNumWakeupPatterns

- **UUID**: `ECUC:4cd61d2c-be6c-46ff-a7b8-764e9ab3dd1b`
- **参数名**: `FrSMNumWakeupPatterns`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Maximum number of Wakeup Patterns the node may send before going to FRSM_STARTUP.

######## 3. FrSMStartupRepetitions

- **UUID**: `ECUC:d56fbbc1-2025-4426-89b4-b830a9025719`
- **参数名**: `FrSMStartupRepetitions`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The number of times an ECU may repeat the startup procedure for a FlexRay cluster.

######## 4. FrSMStartupRepetitionsWithWakeup

- **UUID**: `ECUC:254df245-0739-438d-9785-f139d395c9df`
- **参数名**: `FrSMStartupRepetitionsWithWakeup`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The number of times an ECU may repeat the startup procedure including a wakeup for a FlexRay cluster.

####### BOOLEAN 类型参数

######## 1. FrSMCheckWakeupReason

- **UUID**: `ECUC:44f793fc-177a-4598-b96a-a0cd92f520e2`
- **参数名**: `FrSMCheckWakeupReason`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: If FrSMCheckWakeupReason  is true, the FrSM will check the wakeup reason in order to skip the wakeup in case of wakeup by bus. If FrSMCheckWakeupReason  is false, the FrSM will always try to perform a wakeup.

######## 2. FrSMDelayStartupWithoutWakeup

- **UUID**: `ECUC:6cec37d5-45df-413b-a43e-039bc6eb3805`
- **参数名**: `FrSMDelayStartupWithoutWakeup`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: If true, timer t1 shall be started instead of immediately calling FrIf_AllowColdstart in case of a startup without wakeup.

######## 3. FrSMIsColdstartEcu

- **UUID**: `ECUC:d006fe48-3419-4c48-9b4f-0c79d70b17a5`
- **参数名**: `FrSMIsColdstartEcu`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: True: The ECU is a coldstart node for this FlexRay cluster.

######## 4. FrSMIsWakeupEcu

- **UUID**: `ECUC:775480ae-171e-4527-8024-c8c94e5b7844`
- **参数名**: `FrSMIsWakeupEcu`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: True: FrSM shall perform a wakeup for this cluster.

####### FLOAT 类型参数

######## 1. FrSMDurationT1

- **UUID**: `ECUC:d062fcc7-b32d-4669-ab94-f0cbfa827199`
- **参数名**: `FrSMDurationT1`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0..Inf]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The duration of timer t1 in seconds.

######## 2. FrSMDurationT2

- **UUID**: `ECUC:df901f89-f193-4d1e-8ea0-387ca7ff1fd5`
- **参数名**: `FrSMDurationT2`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0..Inf]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The duration of timer t2 in seconds.

######## 3. FrSMDurationT3

- **UUID**: `ECUC:d68c5e6b-b23e-4437-8cc3-bb9444d5069d`
- **参数名**: `FrSMDurationT3`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0..Inf]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The duration of timer t3 in seconds. The value of this parameter shall be larger than the value of FrSMDurationT1 parameter.

######## 4. FrSMMainFunctionCycleTime

- **UUID**: `ECUC:db31e4f1-2f37-495e-ab4d-465746a7d5a3`
- **参数名**: `FrSMMainFunctionCycleTime`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0..Inf]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the cycle time in seconds of the periodic calling of FrSM main function.

###### 引用关系

此容器包含 **2** 个引用：

####### SYMBOLIC-NAME-REFERENCE 类型引用

######## 1. FrSMComMNetworkHandleRef

- **UUID**: `ECUC:e2b79c8a-5548-4ed9-af29-350b61ae85df`
- **引用名**: `FrSMComMNetworkHandleRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `ComMChannel`
- **完整路径**: `/AUTOSAR/EcucDefs/ComM/ComMConfigSet/ComMChannel`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the unique handle to identify one certain FlexRay network correspond to one of the network handles of the ComM configuration.

######## 2. FrSMFrIfClusterRef

- **UUID**: `ECUC:dd461cfe-0a31-43a8-8446-3d8f2358423f`
- **引用名**: `FrSMFrIfClusterRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `FrIfCluster`
- **完整路径**: `/AUTOSAR/EcucDefs/FrIf/FrIfConfig/FrIfCluster`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: References the cluster configuration in the FlexRay Interface configuration.

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. FrSMClusterDemEventParameterRefs

**容器属性**:

- **UUID**: `ECUC:9f8654da-17b0-427d-8b3f-bdb04c809a83`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FrSMClusterDemEventParameterRefs`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Container for the references to DemEventParameter elements which shall be invoked using the API Dem_ReportErrorStatus in case the corresponding error occurs. The EventId is taken from the referenced DemEventParameter's DemEventId value.

######## 引用关系

此容器包含 **2** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. FRSM_E_CLUSTER_STARTUP

- **UUID**: `ECUC:637b2fa5-031c-4c62-8b02-eb0313e3b92d`
- **引用名**: `FRSM_E_CLUSTER_STARTUP`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `DemEventParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemConfigSet/DemEventParameter`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the DemEventParameter which shall be issued when the error "FRSM_E_CLUSTER_STARTUP" has occured. If the reference is not configured the error shall be reported as DET error.

########## 2. FRSM_E_CLUSTER_SYNC_LOSS

- **UUID**: `ECUC:30585f0b-2439-441e-8cbd-d7d6e7b51ae1`
- **引用名**: `FRSM_E_CLUSTER_SYNC_LOSS`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `DemEventParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemConfigSet/DemEventParameter`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the DemEventParameter which shall be issued when the error "FRSM_E_CLUSTER_SYNC_LOSS" has occurred. If the reference is not configured the error shall be reported as DET error.

##### 3. FrSMClusterDemEventParameterRefs

**容器属性**:

- **UUID**: `ECUC:9f8654da-17b0-427d-8b3f-bdb04c809a83`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FrSMClusterDemEventParameterRefs`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Container for the references to DemEventParameter elements which shall be invoked using the API Dem_ReportErrorStatus in case the corresponding error occurs. The EventId is taken from the referenced DemEventParameter's DemEventId value.

###### 引用关系

此容器包含 **2** 个引用：

####### SYMBOLIC-NAME-REFERENCE 类型引用

######## 1. FRSM_E_CLUSTER_STARTUP

- **UUID**: `ECUC:637b2fa5-031c-4c62-8b02-eb0313e3b92d`
- **引用名**: `FRSM_E_CLUSTER_STARTUP`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `DemEventParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemConfigSet/DemEventParameter`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the DemEventParameter which shall be issued when the error "FRSM_E_CLUSTER_STARTUP" has occured. If the reference is not configured the error shall be reported as DET error.

######## 2. FRSM_E_CLUSTER_SYNC_LOSS

- **UUID**: `ECUC:30585f0b-2439-441e-8cbd-d7d6e7b51ae1`
- **引用名**: `FRSM_E_CLUSTER_SYNC_LOSS`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `DemEventParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemConfigSet/DemEventParameter`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the DemEventParameter which shall be issued when the error "FRSM_E_CLUSTER_SYNC_LOSS" has occurred. If the reference is not configured the error shall be reported as DET error.

##### 4. FrSMGeneral

**容器属性**:

- **UUID**: `ECUC:c7bab0a0-434a-4b1b-9cbc-a4fa164375e0`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FrSMGeneral`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

This container contains the general configuration parameters of the FlexRay State Manager.

###### 参数配置

此容器包含 **3** 个参数：

####### BOOLEAN 类型参数

######## 1. FrSMDevErrorDetect

- **UUID**: `ECUC:876430b3-a273-44c7-b9cb-2a55ab4c5382`
- **参数名**: `FrSMDevErrorDetect`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enables and disables the development error detection and

######## 2. FrSMVersionInfoApi

- **UUID**: `ECUC:687f878a-ab78-487e-afd6-9cea1d16e990`
- **参数名**: `FrSMVersionInfoApi`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enables and disables the version info API

####### FUNCTION-NAME 类型参数

######## 1. FrSMSyncLossErrorIndicationName

- **UUID**: `ECUC:36e196cd-aca7-4ede-be0c-36684a5d4382`
- **参数名**: `FrSMSyncLossErrorIndicationName`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **函数变体**:
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of <Cdd>_SyncLossErrorIndication function that shall be called on loss of synchronization. If this parameter is omitted no indication shall take place.

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

1. **FrSM**
