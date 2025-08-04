# Nm - 完整配置文档

*此文档由ARXML文件自动生成，采用层次化结构展示*

**生成时间**: 2025-06-16 14:46:29

## 📑 目录

- [📄 文件信息](#-文件信息)
- [🔧 模块定义](#-模块定义)
  - [Nm](#nm)
- [📦 包结构](#-包结构)

## 📄 文件信息

### Schema信息
- **Schema位置**: `http://autosar.org/schema/r4.0 AUTOSAR_4-0-3.xsd`
- **命名空间**: `http://autosar.org/schema/r4.0`

## 🔧 模块定义

### 1. Nm

#### 基本信息

- **UUID**: `ECUC:85d327c1-7f75-4768-967d-2ed54a522a8c`
- **模块名称**: `Nm`
- **多重性**: [0..1]
- **支持的变体**:
  - VARIANT-LINK-TIME
  - VARIANT-PRE-COMPILE

#### 模块描述

The Generic Network Management Interface module

#### 版本历史

共有 **1** 个版本记录：

##### 1. 版本 4.2.0

- **发布日期**: 2011-11-09
- **发布者**: AUTOSAR

*此版本无详细变更记录*

#### 配置容器

本模块包含 **8** 个配置容器：

##### 1. NmChannelConfig

**容器属性**:

- **UUID**: `ECUC:842b96df-ba92-4b68-ac20-f463b92f08b9`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `NmChannelConfig`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

This container contains the configuration (parameters) of the bus channel(s). The channel parameter shall be harmonized within the whole communication stack.

###### 参数配置

此容器包含 **8** 个参数：

####### INTEGER 类型参数

######## 1. NmChannelId

- **UUID**: `ECUC:a12acb0a-6ce7-49b2-99fb-744d5c043996`
- **参数名**: `NmChannelId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter holds the unique channel index value. The value shall be the same as the ComMChannelId of the ComMChannel referenced by NmComMChannelRef.

######## 2. NmCoordClusterIndex

- **UUID**: `ECUC:bc7c10ec-1a35-495a-a04d-da39be8da935`
- **参数名**: `NmCoordClusterIndex`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: If this parameter is undefined for a channel, the corresponding bus does not belong to an NM coordination cluster.

####### BOOLEAN 类型参数

######## 1. NmActiveCoordinator

- **UUID**: `ECUC:b34cdb52-707b-4af1-8403-52611cb0f7b1`
- **参数名**: `NmActiveCoordinator`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter indicates whether a NM Coordinator is an active gateway (NmActiveCoordinator = TRUE) or a passive.

######## 2. NmChannelSleepMaster

- **UUID**: `ECUC:0335c4a7-8904-45ec-a525-d7490bbcdfa3`
- **参数名**: `NmChannelSleepMaster`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter shall be set to indicate if the sleep of this network can be absolutely decided by the local node only and that no other nodes can oppose that decision.

######## 3. NmPassiveModeEnabled

- **UUID**: `ECUC:971df935-600e-45aa-87a3-1a46c6161d00`
- **参数名**: `NmPassiveModeEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Pre-processor switch for enabling support of Passive Mode of the <BusNm>s.

######## 4. NmStateReportEnabled

- **UUID**: `ECUC:34d2798b-5bfb-4b0a-a4d4-b59a566954fe`
- **参数名**: `NmStateReportEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies if the NMS shall be set for the corresponding network.

######## 5. NmSynchronizingNetwork

- **UUID**: `ECUC:e8274329-e850-439c-8477-e29a4651ca61`
- **参数名**: `NmSynchronizingNetwork`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: If this parameter is true, then this network is a synchronizing network for the NM coordination cluster which it belongs to. The network is expected to call Nm_SynchronizationPoint() at regular intervals.

####### FLOAT 类型参数

######## 1. NmShutdownDelayTimer

- **UUID**: `ECUC:5ab3ca9a-18c0-4f55-b90f-0fbff5bae924`
- **参数名**: `NmShutdownDelayTimer`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0..Inf]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the time in seconds which the NM Coordination algorithm shall delay the release of this channel with.

###### 引用关系

此容器包含 **2** 个引用：

####### SYMBOLIC-NAME-REFERENCE 类型引用

######## 1. NmComMChannelRef

- **UUID**: `ECUC:833d8eee-a64b-4b28-a3f9-acf0a74117e9`
- **引用名**: `NmComMChannelRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `ComMChannel`
- **完整路径**: `/AUTOSAR/EcucDefs/ComM/ComMConfigSet/ComMChannel`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the corresponding ComM Channel.

######## 2. NmStateReportSignalRef

- **UUID**: `ECUC:bfde6ac3-3d19-4a27-bfb8-34e63dc69f2b`
- **引用名**: `NmStateReportSignalRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `ComSignal`
- **完整路径**: `/AUTOSAR/EcucDefs/Com/ComConfig/ComSignal`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the signal for setting the NMS by calling Com_SendSignal for the respective channel.

###### 配置容器

本模块包含 **3** 个配置容器：

####### 1. NmGenericBusNmConfig

**容器属性**:

- **UUID**: `ECUC:92af2901-de9c-4b91-86cb-1539013c5941`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `NmGenericBusNmConfig`
- **多重性**: [1..1]
- **多配置容器**: false

######## 参数配置

此容器包含 **1** 个参数：

######### STRING 类型参数

########## 1. NmGenericBusNmPrefix

- **UUID**: `ECUC:bb6fb5bb-3537-4848-b999-40a466d5ef00`
- **参数名**: `NmGenericBusNmPrefix`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The prefix which identifies the generic <BusNm>. This will be used to determine the API name to be called by Nm for the provided interfaces of the <BusNm>. This string will used for the module prefix before the "_" character in the API call name.

####### 2. NmStandardBusNmConfig

**容器属性**:

- **UUID**: `ECUC:f7089f32-1bb9-43c6-b980-9593e7d0e4ad`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `NmStandardBusNmConfig`
- **多重性**: [1..1]
- **多配置容器**: false

######## 参数配置

此容器包含 **1** 个参数：

######### ENUMERATION 类型参数

########## 1. NmStandardBusType

- **UUID**: `ECUC:85163822-730a-47cc-bc09-ca69fd6a8cbb`
- **参数名**: `NmStandardBusType`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `NM_BUSNM_CANNM` (来源: AUTOSAR_ECUC)
  - `NM_BUSNM_FRNM` (来源: AUTOSAR_ECUC)
  - `NM_BUSNM_LINNM` (来源: AUTOSAR_ECUC)
  - `NM_BUSNM_UDPNM` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Identifies the bus type of the channel for standard AUTOSAR <BusNm>s and is used to determine which set of API calls to be called by Nm for the <BusNm>s.

####### 3. NmBusType

**容器属性**:

- **UUID**: `ECUC:09004dec-3810-4de9-8b9f-fcb8a7b7f53e`
- **容器类型**: CHOICE-CONTAINER
- **容器名称**: `NmBusType`
- **多重性**: [1..1]

**容器选择**:

- **NmGenericBusNmConfig**
  - UUID: `ECUC:92af2901-de9c-4b91-86cb-1539013c5941`
- **NmStandardBusNmConfig**
  - UUID: `ECUC:f7089f32-1bb9-43c6-b980-9593e7d0e4ad`

##### 2. NmGenericBusNmConfig

**容器属性**:

- **UUID**: `ECUC:92af2901-de9c-4b91-86cb-1539013c5941`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `NmGenericBusNmConfig`
- **多重性**: [1..1]
- **多配置容器**: false

###### 参数配置

此容器包含 **1** 个参数：

####### STRING 类型参数

######## 1. NmGenericBusNmPrefix

- **UUID**: `ECUC:bb6fb5bb-3537-4848-b999-40a466d5ef00`
- **参数名**: `NmGenericBusNmPrefix`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The prefix which identifies the generic <BusNm>. This will be used to determine the API name to be called by Nm for the provided interfaces of the <BusNm>. This string will used for the module prefix before the "_" character in the API call name.

##### 3. NmStandardBusNmConfig

**容器属性**:

- **UUID**: `ECUC:f7089f32-1bb9-43c6-b980-9593e7d0e4ad`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `NmStandardBusNmConfig`
- **多重性**: [1..1]
- **多配置容器**: false

###### 参数配置

此容器包含 **1** 个参数：

####### ENUMERATION 类型参数

######## 1. NmStandardBusType

- **UUID**: `ECUC:85163822-730a-47cc-bc09-ca69fd6a8cbb`
- **参数名**: `NmStandardBusType`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `NM_BUSNM_CANNM` (来源: AUTOSAR_ECUC)
  - `NM_BUSNM_FRNM` (来源: AUTOSAR_ECUC)
  - `NM_BUSNM_LINNM` (来源: AUTOSAR_ECUC)
  - `NM_BUSNM_UDPNM` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Identifies the bus type of the channel for standard AUTOSAR <BusNm>s and is used to determine which set of API calls to be called by Nm for the <BusNm>s.

##### 4. NmGlobalConfig

**容器属性**:

- **UUID**: `ECUC:ed27fca6-b4e9-4dd2-b499-72b51d716b48`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `NmGlobalConfig`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

This container contains all global configuration parameters of the Nm Interface.

###### 配置容器

本模块包含 **3** 个配置容器：

####### 1. NmGlobalConstants

**容器属性**:

- **UUID**: `ECUC:651affe5-65bf-46cc-9776-9e296fd7b3f8`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `NmGlobalConstants`
- **多重性**: [1..1]
- **多配置容器**: false

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. NmNumberOfChannels

- **UUID**: `ECUC:c13a0439-d0e8-4c2b-94c8-8aa9a521f13e`
- **参数名**: `NmNumberOfChannels`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Number of NM channels allowed within one ECU.

####### 2. NmGlobalFeatures

**容器属性**:

- **UUID**: `ECUC:c71f0478-cc29-49a3-93c8-e9010f07b07f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `NmGlobalFeatures`
- **多重性**: [1..1]
- **多配置容器**: false

######## 参数配置

此容器包含 **14** 个参数：

######### BOOLEAN 类型参数

########## 1. NmBusSynchronizationEnabled

- **UUID**: `ECUC:b4b6f8dd-8b3f-403f-ad6a-870f65346dcc`
- **参数名**: `NmBusSynchronizationEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Pre-processor switch for enabling bus synchronization support of the <BusNm>s. This feature is required for NM Coordinator nodes only.

########## 2. NmCarWakeUpRxEnabled

- **UUID**: `ECUC:797d5792-89b9-4cc0-8e9b-ee6caedb6e3d`
- **参数名**: `NmCarWakeUpRxEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enables or disables CWU detection.

########## 3. NmComControlEnabled

- **UUID**: `ECUC:a29345dd-b421-44e3-ad37-979593f7efed`
- **参数名**: `NmComControlEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Pre-processor switch for enabling the Communication Control support.

########## 4. NmComUserDataSupport

- **UUID**: `ECUC:38c9a3f3-a55c-4329-965e-c6e5c073a465`
- **参数名**: `NmComUserDataSupport`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enable/Disable setting of NMUserData via SW-C. If NmComUserDataSupport is enabled the API Nm_SetUserData shall not be available.

########## 5. NmCoordinatorSupportEnabled

- **UUID**: `ECUC:30e5795b-0a84-43c5-af11-bb593f3c94d8`
- **参数名**: `NmCoordinatorSupportEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Pre-processor switch for enabling NM Coordinator support.

########## 6. NmNodeDetectionEnabled

- **UUID**: `ECUC:598ff339-5e53-4db2-a556-0c4c035b1351`
- **参数名**: `NmNodeDetectionEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Pre-processor switch for enabling the Node Detection feature.

########## 7. NmNodeIdEnabled

- **UUID**: `ECUC:19e7dea2-bbe2-4be5-ab4b-fd2619e94c7a`
- **参数名**: `NmNodeIdEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Pre-processor switch for enabling transmission of the source node identifier in NM messages.

########## 8. NmPduRxIndicationEnabled

- **UUID**: `ECUC:030ff2c7-699f-4261-8f5a-1b4cc2ba36d0`
- **参数名**: `NmPduRxIndicationEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Pre-processor switch for enabling the PDU Rx Indication.

########## 9. NmRemoteSleepIndEnabled

- **UUID**: `ECUC:d4af23a3-afd4-412f-8e83-97303d8a465e`
- **参数名**: `NmRemoteSleepIndEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Pre-processor switch for enabling Remote Sleep Indication support. This feature is required for NM Coordinator nodes only.

########## 10. NmRepeatMsgIndEnabled

- **UUID**: `ECUC:68a9c26e-e943-4a40-8fad-52474f18fea4`
- **参数名**: `NmRepeatMsgIndEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Pre-processor switch for enabling the Repeat Message Bit Indication.

########## 11. NmStateChangeIndEnabled

- **UUID**: `ECUC:f8af09e6-5046-47b9-a8b2-dd6fe01f6886`
- **参数名**: `NmStateChangeIndEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Pre-processor switch for enabling the Network Management state change notification.

########## 12. NmUserDataEnabled

- **UUID**: `ECUC:10110c11-2fef-4781-b55a-c875c8cc4e17`
- **参数名**: `NmUserDataEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Pre-processor switch for enabling User Data support.

######### FLOAT 类型参数

########## 1. NmGlobalCoordinatorTime

- **UUID**: `ECUC:ce98cd3e-0883-43c4-afae-4d39e58b7524`
- **参数名**: `NmGlobalCoordinatorTime`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **取值范围**: [0..Inf]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the maximum shutdown time of a connected and coordinated NM-Cluster.

######### FUNCTION-NAME 类型参数

########## 1. NmCarWakeUpCallback

- **UUID**: `ECUC:4b206fb3-ec14-4ca7-a0cc-901859f487ee`
- **参数名**: `NmCarWakeUpCallback`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **函数变体**:
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of the callback function to be called if Nm_CarWakeUpIndication() is called.

####### 3. NmGlobalProperties

**容器属性**:

- **UUID**: `ECUC:a4fbfe4d-0bfd-4740-9d2e-6422aa09a214`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `NmGlobalProperties`
- **多重性**: [1..1]
- **多配置容器**: false

######## 参数配置

此容器包含 **3** 个参数：

######### BOOLEAN 类型参数

########## 1. NmDevErrorDetect

- **UUID**: `ECUC:28c149cd-8f76-430e-a060-94f166a265b4`
- **参数名**: `NmDevErrorDetect`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Pre-processor switch for enabling development error detection and notification.

########## 2. NmVersionInfoApi

- **UUID**: `ECUC:85f60c55-9699-4cdc-b41a-491e125b6b00`
- **参数名**: `NmVersionInfoApi`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Pre-processor switch for enabling Version Info API support.

######### FLOAT 类型参数

########## 1. NmCycletimeMainFunction

- **UUID**: `ECUC:74bd8ad8-344c-4ee9-8a81-42cc0daa4d55`
- **参数名**: `NmCycletimeMainFunction`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0..Inf]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The period between successive calls to the Main Function of the NM Interface in seconds.

##### 5. NmGlobalConstants

**容器属性**:

- **UUID**: `ECUC:651affe5-65bf-46cc-9776-9e296fd7b3f8`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `NmGlobalConstants`
- **多重性**: [1..1]
- **多配置容器**: false

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. NmNumberOfChannels

- **UUID**: `ECUC:c13a0439-d0e8-4c2b-94c8-8aa9a521f13e`
- **参数名**: `NmNumberOfChannels`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Number of NM channels allowed within one ECU.

##### 6. NmGlobalFeatures

**容器属性**:

- **UUID**: `ECUC:c71f0478-cc29-49a3-93c8-e9010f07b07f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `NmGlobalFeatures`
- **多重性**: [1..1]
- **多配置容器**: false

###### 参数配置

此容器包含 **14** 个参数：

####### BOOLEAN 类型参数

######## 1. NmBusSynchronizationEnabled

- **UUID**: `ECUC:b4b6f8dd-8b3f-403f-ad6a-870f65346dcc`
- **参数名**: `NmBusSynchronizationEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Pre-processor switch for enabling bus synchronization support of the <BusNm>s. This feature is required for NM Coordinator nodes only.

######## 2. NmCarWakeUpRxEnabled

- **UUID**: `ECUC:797d5792-89b9-4cc0-8e9b-ee6caedb6e3d`
- **参数名**: `NmCarWakeUpRxEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enables or disables CWU detection.

######## 3. NmComControlEnabled

- **UUID**: `ECUC:a29345dd-b421-44e3-ad37-979593f7efed`
- **参数名**: `NmComControlEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Pre-processor switch for enabling the Communication Control support.

######## 4. NmComUserDataSupport

- **UUID**: `ECUC:38c9a3f3-a55c-4329-965e-c6e5c073a465`
- **参数名**: `NmComUserDataSupport`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enable/Disable setting of NMUserData via SW-C. If NmComUserDataSupport is enabled the API Nm_SetUserData shall not be available.

######## 5. NmCoordinatorSupportEnabled

- **UUID**: `ECUC:30e5795b-0a84-43c5-af11-bb593f3c94d8`
- **参数名**: `NmCoordinatorSupportEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Pre-processor switch for enabling NM Coordinator support.

######## 6. NmNodeDetectionEnabled

- **UUID**: `ECUC:598ff339-5e53-4db2-a556-0c4c035b1351`
- **参数名**: `NmNodeDetectionEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Pre-processor switch for enabling the Node Detection feature.

######## 7. NmNodeIdEnabled

- **UUID**: `ECUC:19e7dea2-bbe2-4be5-ab4b-fd2619e94c7a`
- **参数名**: `NmNodeIdEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Pre-processor switch for enabling transmission of the source node identifier in NM messages.

######## 8. NmPduRxIndicationEnabled

- **UUID**: `ECUC:030ff2c7-699f-4261-8f5a-1b4cc2ba36d0`
- **参数名**: `NmPduRxIndicationEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Pre-processor switch for enabling the PDU Rx Indication.

######## 9. NmRemoteSleepIndEnabled

- **UUID**: `ECUC:d4af23a3-afd4-412f-8e83-97303d8a465e`
- **参数名**: `NmRemoteSleepIndEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Pre-processor switch for enabling Remote Sleep Indication support. This feature is required for NM Coordinator nodes only.

######## 10. NmRepeatMsgIndEnabled

- **UUID**: `ECUC:68a9c26e-e943-4a40-8fad-52474f18fea4`
- **参数名**: `NmRepeatMsgIndEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Pre-processor switch for enabling the Repeat Message Bit Indication.

######## 11. NmStateChangeIndEnabled

- **UUID**: `ECUC:f8af09e6-5046-47b9-a8b2-dd6fe01f6886`
- **参数名**: `NmStateChangeIndEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Pre-processor switch for enabling the Network Management state change notification.

######## 12. NmUserDataEnabled

- **UUID**: `ECUC:10110c11-2fef-4781-b55a-c875c8cc4e17`
- **参数名**: `NmUserDataEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Pre-processor switch for enabling User Data support.

####### FLOAT 类型参数

######## 1. NmGlobalCoordinatorTime

- **UUID**: `ECUC:ce98cd3e-0883-43c4-afae-4d39e58b7524`
- **参数名**: `NmGlobalCoordinatorTime`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **取值范围**: [0..Inf]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the maximum shutdown time of a connected and coordinated NM-Cluster.

####### FUNCTION-NAME 类型参数

######## 1. NmCarWakeUpCallback

- **UUID**: `ECUC:4b206fb3-ec14-4ca7-a0cc-901859f487ee`
- **参数名**: `NmCarWakeUpCallback`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **函数变体**:
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of the callback function to be called if Nm_CarWakeUpIndication() is called.

##### 7. NmGlobalProperties

**容器属性**:

- **UUID**: `ECUC:a4fbfe4d-0bfd-4740-9d2e-6422aa09a214`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `NmGlobalProperties`
- **多重性**: [1..1]
- **多配置容器**: false

###### 参数配置

此容器包含 **3** 个参数：

####### BOOLEAN 类型参数

######## 1. NmDevErrorDetect

- **UUID**: `ECUC:28c149cd-8f76-430e-a060-94f166a265b4`
- **参数名**: `NmDevErrorDetect`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Pre-processor switch for enabling development error detection and notification.

######## 2. NmVersionInfoApi

- **UUID**: `ECUC:85f60c55-9699-4cdc-b41a-491e125b6b00`
- **参数名**: `NmVersionInfoApi`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Pre-processor switch for enabling Version Info API support.

####### FLOAT 类型参数

######## 1. NmCycletimeMainFunction

- **UUID**: `ECUC:74bd8ad8-344c-4ee9-8a81-42cc0daa4d55`
- **参数名**: `NmCycletimeMainFunction`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0..Inf]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The period between successive calls to the Main Function of the NM Interface in seconds.

##### 8. NmBusType

**容器属性**:

- **UUID**: `ECUC:09004dec-3810-4de9-8b9f-fcb8a7b7f53e`
- **容器类型**: CHOICE-CONTAINER
- **容器名称**: `NmBusType`
- **多重性**: [1..1]

**容器选择**:

- **NmGenericBusNmConfig**
  - UUID: `ECUC:92af2901-de9c-4b91-86cb-1539013c5941`
- **NmStandardBusNmConfig**
  - UUID: `ECUC:f7089f32-1bb9-43c6-b980-9593e7d0e4ad`

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

1. **Nm**
