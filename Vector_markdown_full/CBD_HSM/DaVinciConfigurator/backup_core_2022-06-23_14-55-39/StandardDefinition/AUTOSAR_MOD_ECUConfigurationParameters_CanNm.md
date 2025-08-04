# CanNm - 完整配置文档

*此文档由ARXML文件自动生成，采用层次化结构展示*

**生成时间**: 2025-06-16 14:51:08

## 📑 目录

- [📄 文件信息](#-文件信息)
- [🔧 模块定义](#-模块定义)
  - [CanNm](#cannm)
- [📦 包结构](#-包结构)

## 📄 文件信息

### Schema信息
- **Schema位置**: `http://autosar.org/schema/r4.0 AUTOSAR_4-0-3.xsd`
- **命名空间**: `http://autosar.org/schema/r4.0`

## 🔧 模块定义

### 1. CanNm

#### 基本信息

- **UUID**: `ECUC:8a83c6f1-5852-45b3-8852-d4ae2de240f0`
- **模块名称**: `CanNm`
- **多重性**: [0..1]
- **支持的变体**:
  - VARIANT-LINK-TIME
  - VARIANT-POST-BUILD
  - VARIANT-PRE-COMPILE

#### 模块描述

Configuration Parameters for the Can Nm module.

#### 版本历史

共有 **1** 个版本记录：

##### 1. 版本 4.2.0

- **发布日期**: 2011-11-09
- **发布者**: AUTOSAR

*此版本无详细变更记录*

#### 配置容器

本模块包含 **7** 个配置容器：

##### 1. CanNmGlobalConfig

**容器属性**:

- **UUID**: `ECUC:5adfcc42-72f3-4b31-8817-31cc191594f8`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CanNmGlobalConfig`
- **多重性**: [1..1]
- **多配置容器**: true

**容器描述**:

This container contains the global configuration parameter of the CanNm. The parameters and the parameters of the sub containers shall be mapped to the C data type CanNm_ConfigType (for parameters where it is possible) which is passed to the CanNm_Init function.

###### 参数配置

此容器包含 **20** 个参数：

####### INTEGER 类型参数

######## 1. CanNmNumberOfChannels

- **UUID**: `ECUC:7569af61-1d81-4341-bc28-a3d6942756e8`
- **参数名**: `CanNmNumberOfChannels`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Number of Can NM channels allowed within one ECU.

####### BOOLEAN 类型参数

######## 1. CanNmBusLoadReductionEnabled

- **UUID**: `ECUC:2f4ec8ee-6cab-47d2-a7cd-4a429eb7f8c9`
- **参数名**: `CanNmBusLoadReductionEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Pre-processor switch for enabling busload reduction support.

######## 2. CanNmBusSynchronizationEnabled

- **UUID**: `ECUC:f27f1a40-1ef7-465f-b7a9-018baec90c72`
- **参数名**: `CanNmBusSynchronizationEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Pre-processor switch for enabling bus synchronization support. This feature is required for gateway nodes only.

######## 3. CanNmComControlEnabled

- **UUID**: `ECUC:39e127e9-9bfb-4b66-91dc-69d319c5e033`
- **参数名**: `CanNmComControlEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Pre-processor switch for enabling the Communication Control support.

######## 4. CanNmComUserDataSupport

- **UUID**: `ECUC:f245f7fe-a9db-4eea-b241-6f5dff772a63`
- **参数名**: `CanNmComUserDataSupport`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enable/disable the user data support.

######## 5. CanNmCoordinatorSyncSupport

- **UUID**: `ECUC:88ba730b-a0ac-42c9-b182-bbda7da16a35`
- **参数名**: `CanNmCoordinatorSyncSupport`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enables/disables the coordinator synchronisation support.

######## 6. CanNmDevErrorDetect

- **UUID**: `ECUC:0c6b4279-9da7-411f-92da-bbe845f27408`
- **参数名**: `CanNmDevErrorDetect`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Pre-processor switch for enabling development error detection support.

######## 7. CanNmImmediateRestartEnabled

- **UUID**: `ECUC:a84a2b93-549c-4eaf-a29b-8533d2dcce66`
- **参数名**: `CanNmImmediateRestartEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Pre-processor switch for enabling the asynchronous transmission of a NM PDU upon bus-communication request in Prepare-Bus-Sleep mode.

######## 8. CanNmImmediateTxconfEnabled

- **UUID**: `ECUC:ede29802-8487-4471-ae68-0a530d246329`
- **参数名**: `CanNmImmediateTxconfEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enable/disable the immediate tx confirmation.

######## 9. CanNmNodeDetectionEnabled

- **UUID**: `ECUC:085768ca-fc78-4356-82af-7490ac1441b4`
- **参数名**: `CanNmNodeDetectionEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Precompile time switch to enable the node detection feature.

######## 10. CanNmPassiveModeEnabled

- **UUID**: `ECUC:89a4c7ef-a71f-4995-a457-3640bfc9e3c4`
- **参数名**: `CanNmPassiveModeEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Pre-processor switch for enabling support of the Passive Mode.

######## 11. CanNmPduRxIndicationEnabled

- **UUID**: `ECUC:abc8024d-f231-4568-a899-f6f8c8b257e3`
- **参数名**: `CanNmPduRxIndicationEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Pre-processor switch for enabling the PDU Rx Indication.

######## 12. CanNmPnEiraCalcEnabled

- **UUID**: `ECUC:0f09a983-43cd-4aaa-b090-01143ba63f8c`
- **参数名**: `CanNmPnEiraCalcEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies if CanNm calculates the PN request information for internal an external requests. (EIRA)

######## 13. CanNmRemoteSleepIndEnabled

- **UUID**: `ECUC:8b15eb81-8391-42a3-ac2e-3168ca0934e5`
- **参数名**: `CanNmRemoteSleepIndEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Pre-processor switch for enabling remote sleep indication support. This feature is required for gateway nodes only.

######## 14. CanNmRepeatMsgIndEnabled

- **UUID**: `ECUC:c112f5ca-6924-40b7-8068-ff41cac65063`
- **参数名**: `CanNmRepeatMsgIndEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enable/disable the notification that a RepeatMessageRequest bit has been received.

######## 15. CanNmStateChangeIndEnabled

- **UUID**: `ECUC:016766a9-f583-4d2f-9bc2-471e455ab810`
- **参数名**: `CanNmStateChangeIndEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Pre-processor switch for enabling the CAN NM state change notification.

######## 16. CanNmUserDataEnabled

- **UUID**: `ECUC:d2a7536b-14e2-4eea-86f5-ba095e740756`
- **参数名**: `CanNmUserDataEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Pre-processor switch for enabling user data support.

######## 17. CanNmVersionInfoApi

- **UUID**: `ECUC:18de9b2a-6920-4616-8921-efdb0143d9d4`
- **参数名**: `CanNmVersionInfoApi`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Pre-processor switch for enabling version info API support.

####### FLOAT 类型参数

######## 1. CanNmMainFunctionPeriod

- **UUID**: `ECUC:6fc20523-5f6d-4f5e-894e-29a40e3ef2c7`
- **参数名**: `CanNmMainFunctionPeriod`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0.001..0.255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Call cycle in seconds of CanNm_MainFunction.

######## 2. CanNmPnResetTime

- **UUID**: `ECUC:cceff8c4-88b2-454b-b189-70cf5941a9c4`
- **参数名**: `CanNmPnResetTime`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **取值范围**: [0.001..65.535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies the runtime of the reset timer in seconds. This reset time is valid for the reset of PN requests in the EIRA and in the ERA. The value shall be the same for every channel. Thus it is a global config parameter.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. CanNmPnEiraRxNSduRef

- **UUID**: `ECUC:2e5c6c98-a29a-46d1-b7da-e702de0d63a5`
- **引用名**: `CanNmPnEiraRxNSduRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a Pdu in the COM-Stack.

###### 配置容器

本模块包含 **6** 个配置容器：

####### 1. CanNmChannelConfig

**容器属性**:

- **UUID**: `ECUC:8f9f4fb9-8f74-4206-b178-9ed880e39529`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CanNmChannelConfig`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

This container contains the channel specific configuration parameter of the CanNm.

######## 参数配置

此容器包含 **24** 个参数：

######### INTEGER 类型参数

########## 1. CanNmCarWakeUpBitPosition

- **UUID**: `ECUC:2e5a9851-b764-44d9-8bc6-360bd5253f4f`
- **参数名**: `CanNmCarWakeUpBitPosition`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..7]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies the Bit position of the CWU within the NM-Message.

########## 2. CanNmCarWakeUpBytePosition

- **UUID**: `ECUC:7459386d-f35e-4ff5-8ec7-5c3f2a33268f`
- **参数名**: `CanNmCarWakeUpBytePosition`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [2..7]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies the Byte position of the CWU within the NM-Message.

########## 3. CanNmCarWakeUpFilterNodeId

- **UUID**: `ECUC:7fcec870-37fd-4166-9835-2344602fc85b`
- **参数名**: `CanNmCarWakeUpFilterNodeId`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Source node identifier for CWU filtering. If CWU filtering is supported, only the CWU bit within the NM message with source node identifier CanNmCarWakeUpFilterNodeId is considered as CWU request.

########## 4. CanNmImmediateNmTransmissions

- **UUID**: `ECUC:7fcb9567-5cb0-413d-9d9d-f5f5b7d7abaf`
- **参数名**: `CanNmImmediateNmTransmissions`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the number of immediate NM PDUs which shall be transmitted. If the value is zero no immediate NM PDUs are transmitted. The cycle time of immeditate NM PDUs is defined by CanNmImmediateNmCycleTime.

########## 5. CanNmNodeId

- **UUID**: `ECUC:e1a8b761-2721-45c0-9b76-eb3000e571d8`
- **参数名**: `CanNmNodeId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Node identifier of local node.

########## 6. CanNmUserDataLength

- **UUID**: `ECUC:bf864a7b-8003-4852-bc7c-104a56da6ff7`
- **参数名**: `CanNmUserDataLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..8]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the length of the user data contained in the NM PDU

######### BOOLEAN 类型参数

########## 1. CanNmAllNmMessagesKeepAwake

- **UUID**: `ECUC:c102fdeb-4831-4ada-9e0b-1c5125f3f909`
- **参数名**: `CanNmAllNmMessagesKeepAwake`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies if CanNm drops irrelevant NM messages.

########## 2. CanNmBusLoadReductionActive

- **UUID**: `ECUC:dec32a1b-7b95-402b-b284-d41f1c849f95`
- **参数名**: `CanNmBusLoadReductionActive`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines if bus load reduction for the respective NM channel is active or not.

########## 3. CanNmCarWakeUpFilterEnabled

- **UUID**: `ECUC:0a3657af-f39c-4912-8576-532ed0640fdc`
- **参数名**: `CanNmCarWakeUpFilterEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: If CWU filtering is supported, only the CWU bit within the NM message with source node identifier CanNmCarWakeUpFilterNodeId is considered as CWU request.

########## 4. CanNmCarWakeUpRxEnabled

- **UUID**: `ECUC:b50831a3-ae64-4020-8e65-835e3a6a7811`
- **参数名**: `CanNmCarWakeUpRxEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enables or disables support of CarWakeUp bit evaluation in received NM messages.

########## 5. CanNmPnEnabled

- **UUID**: `ECUC:1b3bcc11-49fa-4981-8233-c557b26537fa`
- **参数名**: `CanNmPnEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enables or disables support of partial networking.

########## 6. CanNmPnEraCalcEnabled

- **UUID**: `ECUC:3c603053-712a-4bcf-b0fc-e1777544559a`
- **参数名**: `CanNmPnEraCalcEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies if CanNm calculates the PN request information for external requests. (ERA)

########## 7. CanNmPnHandleMultipleNetworkRequests

- **UUID**: `ECUC:1d373ff7-5d82-4720-ab7c-9d6d4c8c4b34`
- **参数名**: `CanNmPnHandleMultipleNetworkRequests`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: false: CanNm_NetworkRequest is ignored in NO.

######### FLOAT 类型参数

########## 1. CanNmImmediateNmCycleTime

- **UUID**: `ECUC:4d249c1c-3176-4ea0-93eb-07d16128346d`
- **参数名**: `CanNmImmediateNmCycleTime`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **取值范围**: [0.001..65.535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the immediate NM PDU cycle time in seconds which is used for CanNmImmediateNmTransmissions NM PDU transmissions. This parameter is only valid if CanNmImmediateNmTransmissions is greater one.

########## 2. CanNmMsgCycleOffset

- **UUID**: `ECUC:be191aab-c6f6-4a39-903f-af940f5a0339`
- **参数名**: `CanNmMsgCycleOffset`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0..65.535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Time offset in the periodic transmission node. It determines the start delay of the transmission. Specified in seconds.

########## 3. CanNmMsgCycleTime

- **UUID**: `ECUC:21645185-ede2-413f-a98d-d2d27b5439f9`
- **参数名**: `CanNmMsgCycleTime`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0.001..65.535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Period of a NM-message in seconds. It determines the periodic rate in the "periodic transmission mode with bus load reduction" and is the basis for transmit scheduling in the "periodic transmission mode without bus load reduction".

########## 4. CanNmMsgReducedTime

- **UUID**: `ECUC:2e443262-a8d3-43b3-80c8-8e9cc95cc4e4`
- **参数名**: `CanNmMsgReducedTime`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0.001..65.535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Node specific bus cycle time in the periodic transmission mode with bus load reduction. Specified in seconds.

########## 5. CanNmMsgTimeoutTime

- **UUID**: `ECUC:b57d7962-6598-46c9-b891-cb6f28e306bc`
- **参数名**: `CanNmMsgTimeoutTime`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0.001..65.535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Transmission Timeout of NM-message. If there is no transmission confirmation by the CAN Interface within this timeout, the CANNM module shall give an error notification.

########## 6. CanNmRemoteSleepIndTime

- **UUID**: `ECUC:d11eee3e-14a4-486a-965a-7a2c2f9e5793`
- **参数名**: `CanNmRemoteSleepIndTime`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0..65.535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Timeout for Remote Sleep Indication.

########## 7. CanNmRepeatMessageTime

- **UUID**: `ECUC:fcceb68d-d4a5-4768-933e-9f44201e799d`
- **参数名**: `CanNmRepeatMessageTime`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0..65.535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Timeout for Repeat Message State.

########## 8. CanNmTimeoutTime

- **UUID**: `ECUC:d87091a6-9fbe-4875-85c4-d8eac6bf974d`
- **参数名**: `CanNmTimeoutTime`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0.002..65.535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Network Timeout for NM-Messages.

########## 9. CanNmWaitBusSleepTime

- **UUID**: `ECUC:527bf265-b1fb-41ac-8c73-7752563cbf22`
- **参数名**: `CanNmWaitBusSleepTime`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0.001..65.535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Timeout for bus calm down phase.

######### ENUMERATION 类型参数

########## 1. CanNmPduCbvPosition

- **UUID**: `ECUC:fd955a85-f2c8-4eb4-a31d-fbb0561f5965`
- **参数名**: `CanNmPduCbvPosition`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `CANNM_PDU_BYTE_0` (来源: AUTOSAR_ECUC)
  - `CANNM_PDU_BYTE_1` (来源: AUTOSAR_ECUC)
  - `CANNM_PDU_OFF` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the position of the control bit vector within the NM PDU.

########## 2. CanNmPduNidPosition

- **UUID**: `ECUC:14a3efb8-8926-4a6c-bdf2-42df6b95d5c7`
- **参数名**: `CanNmPduNidPosition`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `CANNM_PDU_BYTE_0` (来源: AUTOSAR_ECUC)
  - `CANNM_PDU_BYTE_1` (来源: AUTOSAR_ECUC)
  - `CANNM_PDU_OFF` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the position of the source node identifier within the NM PDU.

######## 引用关系

此容器包含 **2** 个引用：

######### REFERENCE 类型引用

########## 1. CanNmPnEraRxNSduRef

- **UUID**: `ECUC:37b6b74d-f4c6-463a-b271-276a852264ee`
- **引用名**: `CanNmPnEraRxNSduRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a Pdu in the COM-Stack. The SduRef is required for every CanNm Channel, because ERA is reported per channel.

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. CanNmComMNetworkHandleRef

- **UUID**: `ECUC:530c669d-24c1-46c2-88e4-d807280d907e`
- **引用名**: `CanNmComMNetworkHandleRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `ComMChannel`
- **完整路径**: `/AUTOSAR/EcucDefs/ComM/ComMConfigSet/ComMChannel`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This reference points to the unique channel defined by the ComMChannel and provides access to the unique channel index value in ComMChannelId.

######## 配置容器

本模块包含 **3** 个配置容器：

######### 1. CanNmRxPdu

**容器属性**:

- **UUID**: `ECUC:c620bd04-5aeb-400c-8943-b3da3707cb6d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CanNmRxPdu`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

This container is used to configure the Rx PDU properties that are used for the CanNm Channel.

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. CanNmRxPduId

- **UUID**: `ECUC:44ce4764-dd8e-4812-98bf-7fcf028339cd`
- **参数名**: `CanNmRxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the Rx PDU ID of the CanIf L-PDU range that is associated with this CanNmChannel instance.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. CanNmRxPduRef

- **UUID**: `ECUC:a847294c-efd1-4c3b-b141-9ccc994928ba`
- **引用名**: `CanNmRxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the global PDU that is used by this CanNmChannel instance.

######### 2. CanNmTxPdu

**容器属性**:

- **UUID**: `ECUC:60374ba6-0f1b-4b0e-a88f-35baecd95798`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CanNmTxPdu`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container contains the CanNmTxConfirmationPduId and the CanNmTxPduRef.

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. CanNmTxConfirmationPduId

- **UUID**: `ECUC:50820697-ec08-4c54-a032-3ebb637181cd`
- **参数名**: `CanNmTxConfirmationPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Handle Id to be used by the Lower Layer to confirm the transmission of the CanNmTxPdu to the LowerLayer.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. CanNmTxPduRef

- **UUID**: `ECUC:af4a2c58-b28e-40cc-a437-8a37b96b7230`
- **引用名**: `CanNmTxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The reference to the common PDU structure.

######### 3. CanNmUserDataTxPdu

**容器属性**:

- **UUID**: `ECUC:d2c3ba3c-7789-48b2-b5f9-724baef3655a`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CanNmUserDataTxPdu`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This optional container is used to configure the UserNm PDU. This container is only available if CanNmComUserDataSupport is enabled.

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. CanNmTxUserDataPduId

- **UUID**: `ECUC:fdd1a8bb-18a5-4143-898d-67ce5a51c78f`
- **参数名**: `CanNmTxUserDataPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the Handle ID of the NM User Data I-PDU.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. CanNmTxUserDataPduRef

- **UUID**: `ECUC:0f92a525-3d00-4381-b61e-03f0605f8c93`
- **引用名**: `CanNmTxUserDataPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the NM User Data I-PDU in the global PDU collection.

####### 2. CanNmRxPdu

**容器属性**:

- **UUID**: `ECUC:c620bd04-5aeb-400c-8943-b3da3707cb6d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CanNmRxPdu`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

This container is used to configure the Rx PDU properties that are used for the CanNm Channel.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. CanNmRxPduId

- **UUID**: `ECUC:44ce4764-dd8e-4812-98bf-7fcf028339cd`
- **参数名**: `CanNmRxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the Rx PDU ID of the CanIf L-PDU range that is associated with this CanNmChannel instance.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. CanNmRxPduRef

- **UUID**: `ECUC:a847294c-efd1-4c3b-b141-9ccc994928ba`
- **引用名**: `CanNmRxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the global PDU that is used by this CanNmChannel instance.

####### 3. CanNmTxPdu

**容器属性**:

- **UUID**: `ECUC:60374ba6-0f1b-4b0e-a88f-35baecd95798`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CanNmTxPdu`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container contains the CanNmTxConfirmationPduId and the CanNmTxPduRef.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. CanNmTxConfirmationPduId

- **UUID**: `ECUC:50820697-ec08-4c54-a032-3ebb637181cd`
- **参数名**: `CanNmTxConfirmationPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Handle Id to be used by the Lower Layer to confirm the transmission of the CanNmTxPdu to the LowerLayer.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. CanNmTxPduRef

- **UUID**: `ECUC:af4a2c58-b28e-40cc-a437-8a37b96b7230`
- **引用名**: `CanNmTxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The reference to the common PDU structure.

####### 4. CanNmUserDataTxPdu

**容器属性**:

- **UUID**: `ECUC:d2c3ba3c-7789-48b2-b5f9-724baef3655a`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CanNmUserDataTxPdu`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This optional container is used to configure the UserNm PDU. This container is only available if CanNmComUserDataSupport is enabled.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. CanNmTxUserDataPduId

- **UUID**: `ECUC:fdd1a8bb-18a5-4143-898d-67ce5a51c78f`
- **参数名**: `CanNmTxUserDataPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the Handle ID of the NM User Data I-PDU.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. CanNmTxUserDataPduRef

- **UUID**: `ECUC:0f92a525-3d00-4381-b61e-03f0605f8c93`
- **引用名**: `CanNmTxUserDataPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the NM User Data I-PDU in the global PDU collection.

####### 5. CanNmPnInfo

**容器属性**:

- **UUID**: `ECUC:0ccf5768-41f4-4e72-864d-50940ccdf6a6`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CanNmPnInfo`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

PN information configuration

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. CanNmPnInfoLength

- **UUID**: `ECUC:a0c4f3a8-7670-4243-9bdd-706add08df8f`
- **参数名**: `CanNmPnInfoLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..7]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies the length of the PN request information in the NM message.

########## 2. CanNmPnInfoOffset

- **UUID**: `ECUC:3ff9d02a-9aed-47d7-980d-4745fbda215a`
- **参数名**: `CanNmPnInfoOffset`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [1..7]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies the offset of the PN request information in the NM message.

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. CanNmPnFilterMaskByte

**容器属性**:

- **UUID**: `ECUC:f6506a2e-abb4-443d-b84c-9726fef9fb8a`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CanNmPnFilterMaskByte`
- **多重性**: [0..7]
- **多配置容器**: false

**容器描述**:

PN information configuration

########## 参数配置

此容器包含 **2** 个参数：

########### INTEGER 类型参数

############ 1. CanNmPnFilterMaskByteIndex

- **UUID**: `ECUC:70575bee-1cd4-49d5-8876-ac3306dc7403`
- **参数名**: `CanNmPnFilterMaskByteIndex`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..6]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies the offset of the PN request information in the NM message.

############ 2. CanNmPnFilterMaskByteValue

- **UUID**: `ECUC:42691f2f-b4b1-473e-8fe5-238527cdc3e6`
- **参数名**: `CanNmPnFilterMaskByteValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Parameter to configure the filter mask byte.

####### 6. CanNmPnFilterMaskByte

**容器属性**:

- **UUID**: `ECUC:f6506a2e-abb4-443d-b84c-9726fef9fb8a`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CanNmPnFilterMaskByte`
- **多重性**: [0..7]
- **多配置容器**: false

**容器描述**:

PN information configuration

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. CanNmPnFilterMaskByteIndex

- **UUID**: `ECUC:70575bee-1cd4-49d5-8876-ac3306dc7403`
- **参数名**: `CanNmPnFilterMaskByteIndex`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..6]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies the offset of the PN request information in the NM message.

########## 2. CanNmPnFilterMaskByteValue

- **UUID**: `ECUC:42691f2f-b4b1-473e-8fe5-238527cdc3e6`
- **参数名**: `CanNmPnFilterMaskByteValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Parameter to configure the filter mask byte.

##### 2. CanNmChannelConfig

**容器属性**:

- **UUID**: `ECUC:8f9f4fb9-8f74-4206-b178-9ed880e39529`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CanNmChannelConfig`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

This container contains the channel specific configuration parameter of the CanNm.

###### 参数配置

此容器包含 **24** 个参数：

####### INTEGER 类型参数

######## 1. CanNmCarWakeUpBitPosition

- **UUID**: `ECUC:2e5a9851-b764-44d9-8bc6-360bd5253f4f`
- **参数名**: `CanNmCarWakeUpBitPosition`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..7]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies the Bit position of the CWU within the NM-Message.

######## 2. CanNmCarWakeUpBytePosition

- **UUID**: `ECUC:7459386d-f35e-4ff5-8ec7-5c3f2a33268f`
- **参数名**: `CanNmCarWakeUpBytePosition`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [2..7]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies the Byte position of the CWU within the NM-Message.

######## 3. CanNmCarWakeUpFilterNodeId

- **UUID**: `ECUC:7fcec870-37fd-4166-9835-2344602fc85b`
- **参数名**: `CanNmCarWakeUpFilterNodeId`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Source node identifier for CWU filtering. If CWU filtering is supported, only the CWU bit within the NM message with source node identifier CanNmCarWakeUpFilterNodeId is considered as CWU request.

######## 4. CanNmImmediateNmTransmissions

- **UUID**: `ECUC:7fcb9567-5cb0-413d-9d9d-f5f5b7d7abaf`
- **参数名**: `CanNmImmediateNmTransmissions`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the number of immediate NM PDUs which shall be transmitted. If the value is zero no immediate NM PDUs are transmitted. The cycle time of immeditate NM PDUs is defined by CanNmImmediateNmCycleTime.

######## 5. CanNmNodeId

- **UUID**: `ECUC:e1a8b761-2721-45c0-9b76-eb3000e571d8`
- **参数名**: `CanNmNodeId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Node identifier of local node.

######## 6. CanNmUserDataLength

- **UUID**: `ECUC:bf864a7b-8003-4852-bc7c-104a56da6ff7`
- **参数名**: `CanNmUserDataLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..8]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the length of the user data contained in the NM PDU

####### BOOLEAN 类型参数

######## 1. CanNmAllNmMessagesKeepAwake

- **UUID**: `ECUC:c102fdeb-4831-4ada-9e0b-1c5125f3f909`
- **参数名**: `CanNmAllNmMessagesKeepAwake`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies if CanNm drops irrelevant NM messages.

######## 2. CanNmBusLoadReductionActive

- **UUID**: `ECUC:dec32a1b-7b95-402b-b284-d41f1c849f95`
- **参数名**: `CanNmBusLoadReductionActive`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines if bus load reduction for the respective NM channel is active or not.

######## 3. CanNmCarWakeUpFilterEnabled

- **UUID**: `ECUC:0a3657af-f39c-4912-8576-532ed0640fdc`
- **参数名**: `CanNmCarWakeUpFilterEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: If CWU filtering is supported, only the CWU bit within the NM message with source node identifier CanNmCarWakeUpFilterNodeId is considered as CWU request.

######## 4. CanNmCarWakeUpRxEnabled

- **UUID**: `ECUC:b50831a3-ae64-4020-8e65-835e3a6a7811`
- **参数名**: `CanNmCarWakeUpRxEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enables or disables support of CarWakeUp bit evaluation in received NM messages.

######## 5. CanNmPnEnabled

- **UUID**: `ECUC:1b3bcc11-49fa-4981-8233-c557b26537fa`
- **参数名**: `CanNmPnEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enables or disables support of partial networking.

######## 6. CanNmPnEraCalcEnabled

- **UUID**: `ECUC:3c603053-712a-4bcf-b0fc-e1777544559a`
- **参数名**: `CanNmPnEraCalcEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies if CanNm calculates the PN request information for external requests. (ERA)

######## 7. CanNmPnHandleMultipleNetworkRequests

- **UUID**: `ECUC:1d373ff7-5d82-4720-ab7c-9d6d4c8c4b34`
- **参数名**: `CanNmPnHandleMultipleNetworkRequests`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: false: CanNm_NetworkRequest is ignored in NO.

####### FLOAT 类型参数

######## 1. CanNmImmediateNmCycleTime

- **UUID**: `ECUC:4d249c1c-3176-4ea0-93eb-07d16128346d`
- **参数名**: `CanNmImmediateNmCycleTime`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **取值范围**: [0.001..65.535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the immediate NM PDU cycle time in seconds which is used for CanNmImmediateNmTransmissions NM PDU transmissions. This parameter is only valid if CanNmImmediateNmTransmissions is greater one.

######## 2. CanNmMsgCycleOffset

- **UUID**: `ECUC:be191aab-c6f6-4a39-903f-af940f5a0339`
- **参数名**: `CanNmMsgCycleOffset`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0..65.535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Time offset in the periodic transmission node. It determines the start delay of the transmission. Specified in seconds.

######## 3. CanNmMsgCycleTime

- **UUID**: `ECUC:21645185-ede2-413f-a98d-d2d27b5439f9`
- **参数名**: `CanNmMsgCycleTime`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0.001..65.535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Period of a NM-message in seconds. It determines the periodic rate in the "periodic transmission mode with bus load reduction" and is the basis for transmit scheduling in the "periodic transmission mode without bus load reduction".

######## 4. CanNmMsgReducedTime

- **UUID**: `ECUC:2e443262-a8d3-43b3-80c8-8e9cc95cc4e4`
- **参数名**: `CanNmMsgReducedTime`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0.001..65.535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Node specific bus cycle time in the periodic transmission mode with bus load reduction. Specified in seconds.

######## 5. CanNmMsgTimeoutTime

- **UUID**: `ECUC:b57d7962-6598-46c9-b891-cb6f28e306bc`
- **参数名**: `CanNmMsgTimeoutTime`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0.001..65.535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Transmission Timeout of NM-message. If there is no transmission confirmation by the CAN Interface within this timeout, the CANNM module shall give an error notification.

######## 6. CanNmRemoteSleepIndTime

- **UUID**: `ECUC:d11eee3e-14a4-486a-965a-7a2c2f9e5793`
- **参数名**: `CanNmRemoteSleepIndTime`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0..65.535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Timeout for Remote Sleep Indication.

######## 7. CanNmRepeatMessageTime

- **UUID**: `ECUC:fcceb68d-d4a5-4768-933e-9f44201e799d`
- **参数名**: `CanNmRepeatMessageTime`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0..65.535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Timeout for Repeat Message State.

######## 8. CanNmTimeoutTime

- **UUID**: `ECUC:d87091a6-9fbe-4875-85c4-d8eac6bf974d`
- **参数名**: `CanNmTimeoutTime`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0.002..65.535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Network Timeout for NM-Messages.

######## 9. CanNmWaitBusSleepTime

- **UUID**: `ECUC:527bf265-b1fb-41ac-8c73-7752563cbf22`
- **参数名**: `CanNmWaitBusSleepTime`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0.001..65.535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Timeout for bus calm down phase.

####### ENUMERATION 类型参数

######## 1. CanNmPduCbvPosition

- **UUID**: `ECUC:fd955a85-f2c8-4eb4-a31d-fbb0561f5965`
- **参数名**: `CanNmPduCbvPosition`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `CANNM_PDU_BYTE_0` (来源: AUTOSAR_ECUC)
  - `CANNM_PDU_BYTE_1` (来源: AUTOSAR_ECUC)
  - `CANNM_PDU_OFF` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the position of the control bit vector within the NM PDU.

######## 2. CanNmPduNidPosition

- **UUID**: `ECUC:14a3efb8-8926-4a6c-bdf2-42df6b95d5c7`
- **参数名**: `CanNmPduNidPosition`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `CANNM_PDU_BYTE_0` (来源: AUTOSAR_ECUC)
  - `CANNM_PDU_BYTE_1` (来源: AUTOSAR_ECUC)
  - `CANNM_PDU_OFF` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the position of the source node identifier within the NM PDU.

###### 引用关系

此容器包含 **2** 个引用：

####### REFERENCE 类型引用

######## 1. CanNmPnEraRxNSduRef

- **UUID**: `ECUC:37b6b74d-f4c6-463a-b271-276a852264ee`
- **引用名**: `CanNmPnEraRxNSduRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a Pdu in the COM-Stack. The SduRef is required for every CanNm Channel, because ERA is reported per channel.

####### SYMBOLIC-NAME-REFERENCE 类型引用

######## 1. CanNmComMNetworkHandleRef

- **UUID**: `ECUC:530c669d-24c1-46c2-88e4-d807280d907e`
- **引用名**: `CanNmComMNetworkHandleRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `ComMChannel`
- **完整路径**: `/AUTOSAR/EcucDefs/ComM/ComMConfigSet/ComMChannel`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This reference points to the unique channel defined by the ComMChannel and provides access to the unique channel index value in ComMChannelId.

###### 配置容器

本模块包含 **3** 个配置容器：

####### 1. CanNmRxPdu

**容器属性**:

- **UUID**: `ECUC:c620bd04-5aeb-400c-8943-b3da3707cb6d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CanNmRxPdu`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

This container is used to configure the Rx PDU properties that are used for the CanNm Channel.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. CanNmRxPduId

- **UUID**: `ECUC:44ce4764-dd8e-4812-98bf-7fcf028339cd`
- **参数名**: `CanNmRxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the Rx PDU ID of the CanIf L-PDU range that is associated with this CanNmChannel instance.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. CanNmRxPduRef

- **UUID**: `ECUC:a847294c-efd1-4c3b-b141-9ccc994928ba`
- **引用名**: `CanNmRxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the global PDU that is used by this CanNmChannel instance.

####### 2. CanNmTxPdu

**容器属性**:

- **UUID**: `ECUC:60374ba6-0f1b-4b0e-a88f-35baecd95798`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CanNmTxPdu`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container contains the CanNmTxConfirmationPduId and the CanNmTxPduRef.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. CanNmTxConfirmationPduId

- **UUID**: `ECUC:50820697-ec08-4c54-a032-3ebb637181cd`
- **参数名**: `CanNmTxConfirmationPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Handle Id to be used by the Lower Layer to confirm the transmission of the CanNmTxPdu to the LowerLayer.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. CanNmTxPduRef

- **UUID**: `ECUC:af4a2c58-b28e-40cc-a437-8a37b96b7230`
- **引用名**: `CanNmTxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The reference to the common PDU structure.

####### 3. CanNmUserDataTxPdu

**容器属性**:

- **UUID**: `ECUC:d2c3ba3c-7789-48b2-b5f9-724baef3655a`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CanNmUserDataTxPdu`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This optional container is used to configure the UserNm PDU. This container is only available if CanNmComUserDataSupport is enabled.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. CanNmTxUserDataPduId

- **UUID**: `ECUC:fdd1a8bb-18a5-4143-898d-67ce5a51c78f`
- **参数名**: `CanNmTxUserDataPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the Handle ID of the NM User Data I-PDU.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. CanNmTxUserDataPduRef

- **UUID**: `ECUC:0f92a525-3d00-4381-b61e-03f0605f8c93`
- **引用名**: `CanNmTxUserDataPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the NM User Data I-PDU in the global PDU collection.

##### 3. CanNmRxPdu

**容器属性**:

- **UUID**: `ECUC:c620bd04-5aeb-400c-8943-b3da3707cb6d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CanNmRxPdu`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

This container is used to configure the Rx PDU properties that are used for the CanNm Channel.

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. CanNmRxPduId

- **UUID**: `ECUC:44ce4764-dd8e-4812-98bf-7fcf028339cd`
- **参数名**: `CanNmRxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the Rx PDU ID of the CanIf L-PDU range that is associated with this CanNmChannel instance.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. CanNmRxPduRef

- **UUID**: `ECUC:a847294c-efd1-4c3b-b141-9ccc994928ba`
- **引用名**: `CanNmRxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the global PDU that is used by this CanNmChannel instance.

##### 4. CanNmTxPdu

**容器属性**:

- **UUID**: `ECUC:60374ba6-0f1b-4b0e-a88f-35baecd95798`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CanNmTxPdu`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container contains the CanNmTxConfirmationPduId and the CanNmTxPduRef.

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. CanNmTxConfirmationPduId

- **UUID**: `ECUC:50820697-ec08-4c54-a032-3ebb637181cd`
- **参数名**: `CanNmTxConfirmationPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Handle Id to be used by the Lower Layer to confirm the transmission of the CanNmTxPdu to the LowerLayer.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. CanNmTxPduRef

- **UUID**: `ECUC:af4a2c58-b28e-40cc-a437-8a37b96b7230`
- **引用名**: `CanNmTxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The reference to the common PDU structure.

##### 5. CanNmUserDataTxPdu

**容器属性**:

- **UUID**: `ECUC:d2c3ba3c-7789-48b2-b5f9-724baef3655a`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CanNmUserDataTxPdu`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This optional container is used to configure the UserNm PDU. This container is only available if CanNmComUserDataSupport is enabled.

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. CanNmTxUserDataPduId

- **UUID**: `ECUC:fdd1a8bb-18a5-4143-898d-67ce5a51c78f`
- **参数名**: `CanNmTxUserDataPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the Handle ID of the NM User Data I-PDU.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. CanNmTxUserDataPduRef

- **UUID**: `ECUC:0f92a525-3d00-4381-b61e-03f0605f8c93`
- **引用名**: `CanNmTxUserDataPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the NM User Data I-PDU in the global PDU collection.

##### 6. CanNmPnInfo

**容器属性**:

- **UUID**: `ECUC:0ccf5768-41f4-4e72-864d-50940ccdf6a6`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CanNmPnInfo`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

PN information configuration

###### 参数配置

此容器包含 **2** 个参数：

####### INTEGER 类型参数

######## 1. CanNmPnInfoLength

- **UUID**: `ECUC:a0c4f3a8-7670-4243-9bdd-706add08df8f`
- **参数名**: `CanNmPnInfoLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..7]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies the length of the PN request information in the NM message.

######## 2. CanNmPnInfoOffset

- **UUID**: `ECUC:3ff9d02a-9aed-47d7-980d-4745fbda215a`
- **参数名**: `CanNmPnInfoOffset`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [1..7]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies the offset of the PN request information in the NM message.

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. CanNmPnFilterMaskByte

**容器属性**:

- **UUID**: `ECUC:f6506a2e-abb4-443d-b84c-9726fef9fb8a`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CanNmPnFilterMaskByte`
- **多重性**: [0..7]
- **多配置容器**: false

**容器描述**:

PN information configuration

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. CanNmPnFilterMaskByteIndex

- **UUID**: `ECUC:70575bee-1cd4-49d5-8876-ac3306dc7403`
- **参数名**: `CanNmPnFilterMaskByteIndex`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..6]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies the offset of the PN request information in the NM message.

########## 2. CanNmPnFilterMaskByteValue

- **UUID**: `ECUC:42691f2f-b4b1-473e-8fe5-238527cdc3e6`
- **参数名**: `CanNmPnFilterMaskByteValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Parameter to configure the filter mask byte.

##### 7. CanNmPnFilterMaskByte

**容器属性**:

- **UUID**: `ECUC:f6506a2e-abb4-443d-b84c-9726fef9fb8a`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CanNmPnFilterMaskByte`
- **多重性**: [0..7]
- **多配置容器**: false

**容器描述**:

PN information configuration

###### 参数配置

此容器包含 **2** 个参数：

####### INTEGER 类型参数

######## 1. CanNmPnFilterMaskByteIndex

- **UUID**: `ECUC:70575bee-1cd4-49d5-8876-ac3306dc7403`
- **参数名**: `CanNmPnFilterMaskByteIndex`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..6]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies the offset of the PN request information in the NM message.

######## 2. CanNmPnFilterMaskByteValue

- **UUID**: `ECUC:42691f2f-b4b1-473e-8fe5-238527cdc3e6`
- **参数名**: `CanNmPnFilterMaskByteValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Parameter to configure the filter mask byte.

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

1. **CanNm**
