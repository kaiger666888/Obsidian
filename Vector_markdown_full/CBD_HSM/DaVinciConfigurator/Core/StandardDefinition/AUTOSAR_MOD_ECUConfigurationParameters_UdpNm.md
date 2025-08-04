# UdpNm - 完整配置文档

*此文档由ARXML文件自动生成，采用层次化结构展示*

**生成时间**: 2025-06-16 14:52:00

## 📑 目录

- [📄 文件信息](#-文件信息)
- [🔧 模块定义](#-模块定义)
  - [UdpNm](#udpnm)
- [📦 包结构](#-包结构)

## 📄 文件信息

### Schema信息
- **Schema位置**: `http://autosar.org/schema/r4.0 AUTOSAR_4-0-3.xsd`
- **命名空间**: `http://autosar.org/schema/r4.0`

## 🔧 模块定义

### 1. UdpNm

#### 基本信息

- **UUID**: `ECUC:4c630c97-053b-44bd-8b50-e3d54b5f2522`
- **模块名称**: `UdpNm`
- **多重性**: [0..1]
- **支持的变体**:
  - VARIANT-LINK-TIME
  - VARIANT-PRE-COMPILE

#### 版本历史

共有 **1** 个版本记录：

##### 1. 版本 4.2.0

- **发布日期**: 2011-11-09
- **发布者**: AUTOSAR

*此版本无详细变更记录*

#### 配置容器

本模块包含 **6** 个配置容器：

##### 1. UdpNmGlobalConfig

**容器属性**:

- **UUID**: `ECUC:63ab75d0-7d69-401d-862f-fa131c1cfdb8`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `UdpNmGlobalConfig`
- **多重性**: [1..1]
- **多配置容器**: true

**容器描述**:

This container contains all global configuration parameters of UDP NM configured from the NM Module perspective.

###### 参数配置

此容器包含 **18** 个参数：

####### INTEGER 类型参数

######## 1. UdpNmCoordinatorId

- **UUID**: `ECUC:1a6b4267-7de8-45b9-b5ca-9388f8f177be`
- **参数名**: `UdpNmCoordinatorId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..3]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Set the NM coordination ID for this gateway.

######## 2. UdpNmNumberOfChannels

- **UUID**: `ECUC:f36bed8d-7ec3-4e15-b106-bf4cfa72fb8f`
- **参数名**: `UdpNmNumberOfChannels`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Number of NM channels allowed within one ECU.

####### BOOLEAN 类型参数

######## 1. UdpNmBusSynchronizationEnabled

- **UUID**: `ECUC:3945c8ec-1034-46a7-bfd8-e4b253c8ad04`
- **参数名**: `UdpNmBusSynchronizationEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Pre-processor switch for enabling bus synchronization support.

######## 2. UdpNmComControl_Enabled

- **UUID**: `ECUC:1373c619-bb72-476c-8751-c6bfdb5afd8a`
- **参数名**: `UdpNmComControl_Enabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Pre-processor switch for enabling the Communication Control support.

######## 3. UdpNmComUserDataSupport

- **UUID**: `ECUC:629ba5c5-50ff-41e7-83c5-3676c1cfa3a2`
- **参数名**: `UdpNmComUserDataSupport`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enable/disable the user data support.

######## 4. UdpNmCoordinatorEnabled

- **UUID**: `ECUC:5c79807b-2fea-4c9c-b3c2-d792548bedef`
- **参数名**: `UdpNmCoordinatorEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-PRE-COMPILE
- **描述**: Enable/disable the NM Coordination algorithm to being able to initiate the synchronization algorithm.

######## 5. UdpNmCoordinatorSyncSupport

- **UUID**: `ECUC:209e4cff-12e9-4cc0-8be4-55febadbe65d`
- **参数名**: `UdpNmCoordinatorSyncSupport`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enables/disables the coordinator synchronisation support.

######## 6. UdpNmDevErrorDetect

- **UUID**: `ECUC:b2cad9ec-c2dd-481b-b257-02d7a76c7a04`
- **参数名**: `UdpNmDevErrorDetect`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Pre-processor switch for enabling development error detection support.

######## 7. UdpNmImmediateRestartEnabled

- **UUID**: `ECUC:1f4617d1-05a0-4fbc-9c5a-e901bf6a129a`
- **参数名**: `UdpNmImmediateRestartEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Pre-processor switch for enabling the asynchronous transmission of a NM PACKET upon bus-communication request in Prepare-Bus-Sleep mode.

######## 8. UdpNmNodeDetectionEnabled

- **UUID**: `ECUC:b25d1e58-2f6b-4202-b905-850582263e0d`
- **参数名**: `UdpNmNodeDetectionEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Pre-processor switch for enabling the node detection support.

######## 9. UdpNmNodeIdEnabled

- **UUID**: `ECUC:7a218418-b07b-4780-8597-503fa00b01c3`
- **参数名**: `UdpNmNodeIdEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Pre-processor switch for enabling the source node identifier.

######## 10. UdpNmPassiveModeEnabled

- **UUID**: `ECUC:49e42ecf-551d-40e6-a805-1a38037ee5f6`
- **参数名**: `UdpNmPassiveModeEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Pre-processor switch for enabling support of the Passive Mode.

######## 11. UdpNmPduRxIndicationEnabled

- **UUID**: `ECUC:8093f0b9-3d2b-4cf2-9baa-5885ae355395`
- **参数名**: `UdpNmPduRxIndicationEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Pre-processor switch for enabling the PDU Rx Indication.

######## 12. UdpNmRemoteSleepIndEnabled

- **UUID**: `ECUC:0f793157-e2c9-4dad-a7d2-1e298f10041f`
- **参数名**: `UdpNmRemoteSleepIndEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Pre-processor switch for enabling remote sleep indication support.

######## 13. UdpNmRepeatMsgIndEnabled

- **UUID**: `ECUC:6f532435-a018-40cf-b533-8262182ef904`
- **参数名**: `UdpNmRepeatMsgIndEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enable/disable the notification that a RepeatMessageRequest bit has been received.

######## 14. UdpNmStateChangeIndEnabled

- **UUID**: `ECUC:3ac1a062-f61a-41d1-b8bc-fc6a3a5838f4`
- **参数名**: `UdpNmStateChangeIndEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Pre-processor switch for enabling the UDP NM state change notification.

######## 15. UdpNmUserDataEnabled

- **UUID**: `ECUC:050b6422-689f-4a60-ade0-fd47fc24be9a`
- **参数名**: `UdpNmUserDataEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Pre-processor switch for enabling user data support.

######## 16. UdpNmVersionInfoApi

- **UUID**: `ECUC:6bf6da5d-f5af-4349-bd6f-873d4910403a`
- **参数名**: `UdpNmVersionInfoApi`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Pre-processor switch for enabling version info API support.

###### 配置容器

本模块包含 **5** 个配置容器：

####### 1. UdpNmChannelConfig

**容器属性**:

- **UUID**: `ECUC:e1325106-da4a-41ce-bf5e-35cd50828ebb`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `UdpNmChannelConfig`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

This container contains the channel-specific configuration parameters of the UdpNm.

######## 参数配置

此容器包含 **13** 个参数：

######### INTEGER 类型参数

########## 1. UdpNmNodeId

- **UUID**: `ECUC:d2155218-8fce-4a97-8ff0-7a69e4edc276`
- **参数名**: `UdpNmNodeId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Node identifier of local node.

########## 2. UdpNmPduLength

- **UUID**: `ECUC:fd0077a4-20a9-47d0-b273-53cc7f9e3c44`
- **参数名**: `UdpNmPduLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..8]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the length of the NM PACKET in bytes.

########## 3. UdpNmUserDataLength

- **UUID**: `ECUC:9def7c0c-91d1-49ea-b731-340ff1071495`
- **参数名**: `UdpNmUserDataLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..8]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the length of the user data contained in the NM PACKET.

######### FLOAT 类型参数

########## 1. UpdNmMainFunctionPeriod

- **UUID**: `ECUC:a10f4184-38e5-4ff7-b9a8-5836e062ba10`
- **参数名**: `UpdNmMainFunctionPeriod`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0.001..0.255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Call cycle of UdpNm_MainFunction_x for the respective instance in [s].

########## 2. UpdNmMsgCycleOffset

- **UUID**: `ECUC:779f1019-0546-4e79-a1a4-a67eb484c8ab`
- **参数名**: `UpdNmMsgCycleOffset`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0..65.535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Time offset in the periodic transmission node. It determines the start delay of the transmission.

########## 3. UpdNmMsgCycleTime

- **UUID**: `ECUC:b88e9d62-7439-49fe-8289-db28bea050a1`
- **参数名**: `UpdNmMsgCycleTime`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0.001..65.535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Period of a NM-message. It determines the periodic rate in the "periodic transmission mode with bus load reduction" and is the basis for transmit scheduling in the "periodic transmission mode without bus load reduction".

########## 4. UpdNmMsgTimeoutTime

- **UUID**: `ECUC:1102aac7-9b16-476b-a775-6597bdba575d`
- **参数名**: `UpdNmMsgTimeoutTime`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0.001..65.535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Transmission Timout of NM-message. If there is no transmission confirmation by the UDP Interface within this timeout, the UDPNM module shall gibe an error notification.

########## 5. UpdNmRemoteSleepIndTime

- **UUID**: `ECUC:03bfa701-84e0-471a-ba23-7df014437c22`
- **参数名**: `UpdNmRemoteSleepIndTime`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0.001..65.535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Timeout for Remote Sleep Indication.

########## 6. UpdNmRepeatMessageTime

- **UUID**: `ECUC:5eba9538-90b4-4ff5-9c6f-3ee933ea4d83`
- **参数名**: `UpdNmRepeatMessageTime`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0..65.535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Timeout for Repeat Message State.

########## 7. UpdNmTimeoutTime

- **UUID**: `ECUC:c143e3dd-8d35-4bfb-8dd5-756d27fb9837`
- **参数名**: `UpdNmTimeoutTime`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0.002..65.535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Network Timeout for NM packets.

########## 8. UpdNmWaitBusSleepTime

- **UUID**: `ECUC:4180c1ae-0a74-4392-b779-7d938d0970d0`
- **参数名**: `UpdNmWaitBusSleepTime`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0.001..65.535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Timeout for bus calm down phase.

######### ENUMERATION 类型参数

########## 1. UdpNmPduCbvPosition

- **UUID**: `ECUC:907e8211-0182-477b-8ff1-7787f3d650b9`
- **参数名**: `UdpNmPduCbvPosition`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `UDPNM_PDU_BYTE_0` (来源: AUTOSAR_ECUC)
  - `UDPNM_PDU_BYTE_1` (来源: AUTOSAR_ECUC)
  - `UDPNM_PDU_OFF` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the position of the control bit vector within the NM PACKET.

########## 2. UdpNmPduNidPosition

- **UUID**: `ECUC:5a854a6b-ee2b-4be8-8913-957963a8478b`
- **参数名**: `UdpNmPduNidPosition`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `UDPNM_PDU_BYTE_0` (来源: AUTOSAR_ECUC)
  - `UDPNM_PDU_BYTE_1` (来源: AUTOSAR_ECUC)
  - `UDPNM_PDU_OFF` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the position of the source node identifier within the NM PACKET.

######## 引用关系

此容器包含 **1** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. UdpNmComMNetworkHandleRef

- **UUID**: `ECUC:bbca2ddc-438c-45cb-a7ad-a61d61c86900`
- **引用名**: `UdpNmComMNetworkHandleRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `ComMChannel`
- **完整路径**: `/AUTOSAR/EcucDefs/ComM/ComMConfigSet/ComMChannel`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This reference points to the unique channel defined by the ComMChannel and provides access to the unique channel index value in ComMChannelId.

######## 配置容器

本模块包含 **3** 个配置容器：

######### 1. UdpNmRxPdu

**容器属性**:

- **UUID**: `ECUC:480eeea9-ba4e-485a-952a-c231fb46da34`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `UdpNmRxPdu`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

This container describes the UdpNm RX PDU's.

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. UdpNmRxPduId

- **UUID**: `ECUC:16e3d251-052d-427f-8c83-ad8491ecce20`
- **参数名**: `UdpNmRxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4294967296]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: ID of the RxPdu that will be used by a RxIndication of the lower layer.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. UdpNmRxPduRef

- **UUID**: `ECUC:a2db0564-e229-41c7-9fce-110d6baa3958`
- **引用名**: `UdpNmRxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The reference to a PDU in the global PDU structure described in the AUTOSAR ECU Configuration Specification. This reference will be used by the UdpNm module to derive the PDU Id.

######### 2. UdpNmTxPdu

**容器属性**:

- **UUID**: `ECUC:5046d451-94f4-4aa9-b257-b9bec9bc27b7`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `UdpNmTxPdu`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

This container describes the UdpNm TX PDU's.

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. UdpNmTxConfirmationPduId

- **UUID**: `ECUC:1df43d6a-1c51-4232-8fb4-3ed791a1df64`
- **参数名**: `UdpNmTxConfirmationPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4294967296]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Id of the TxPdu that will be used by a TxConfirmation from the lower layer.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. UdpNmTxPduRef

- **UUID**: `ECUC:061a28ad-a374-4482-9b47-3b4c28f34600`
- **引用名**: `UdpNmTxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The reference to a PDU in the global PDU structure described in the AUTOSAR ECU Configuration Specification. This reference will be used by the UdpNm module to derive the PDU Id.

######### 3. UdpNmUserDataTxPdu

**容器属性**:

- **UUID**: `ECUC:85f5da66-01d5-4918-88a5-c8c9700e3eb7`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `UdpNmUserDataTxPdu`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This optional container is used to configure the UserNm PDU. This container is only available if UdpNmComUserDataSupport is enabled.

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. UdpNmTxUserDataPduId

- **UUID**: `ECUC:7f47b0d7-eb63-4b7f-a84d-ad47b0e2943d`
- **参数名**: `UdpNmTxUserDataPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the Handle ID of the NM User Data I-PDU.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. UdpNmTxUserDataPduRef

- **UUID**: `ECUC:1dbba522-37a1-4dd1-8369-341d390a6fb5`
- **引用名**: `UdpNmTxUserDataPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the NM User Data I-PDU in the global PDU collection.

####### 2. UdpNmRxPdu

**容器属性**:

- **UUID**: `ECUC:480eeea9-ba4e-485a-952a-c231fb46da34`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `UdpNmRxPdu`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

This container describes the UdpNm RX PDU's.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. UdpNmRxPduId

- **UUID**: `ECUC:16e3d251-052d-427f-8c83-ad8491ecce20`
- **参数名**: `UdpNmRxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4294967296]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: ID of the RxPdu that will be used by a RxIndication of the lower layer.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. UdpNmRxPduRef

- **UUID**: `ECUC:a2db0564-e229-41c7-9fce-110d6baa3958`
- **引用名**: `UdpNmRxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The reference to a PDU in the global PDU structure described in the AUTOSAR ECU Configuration Specification. This reference will be used by the UdpNm module to derive the PDU Id.

####### 3. UdpNmTxPdu

**容器属性**:

- **UUID**: `ECUC:5046d451-94f4-4aa9-b257-b9bec9bc27b7`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `UdpNmTxPdu`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

This container describes the UdpNm TX PDU's.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. UdpNmTxConfirmationPduId

- **UUID**: `ECUC:1df43d6a-1c51-4232-8fb4-3ed791a1df64`
- **参数名**: `UdpNmTxConfirmationPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4294967296]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Id of the TxPdu that will be used by a TxConfirmation from the lower layer.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. UdpNmTxPduRef

- **UUID**: `ECUC:061a28ad-a374-4482-9b47-3b4c28f34600`
- **引用名**: `UdpNmTxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The reference to a PDU in the global PDU structure described in the AUTOSAR ECU Configuration Specification. This reference will be used by the UdpNm module to derive the PDU Id.

####### 4. UdpNmUserDataTxPdu

**容器属性**:

- **UUID**: `ECUC:85f5da66-01d5-4918-88a5-c8c9700e3eb7`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `UdpNmUserDataTxPdu`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This optional container is used to configure the UserNm PDU. This container is only available if UdpNmComUserDataSupport is enabled.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. UdpNmTxUserDataPduId

- **UUID**: `ECUC:7f47b0d7-eb63-4b7f-a84d-ad47b0e2943d`
- **参数名**: `UdpNmTxUserDataPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the Handle ID of the NM User Data I-PDU.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. UdpNmTxUserDataPduRef

- **UUID**: `ECUC:1dbba522-37a1-4dd1-8369-341d390a6fb5`
- **引用名**: `UdpNmTxUserDataPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the NM User Data I-PDU in the global PDU collection.

####### 5. UdpNmDemEventParameterRefs

**容器属性**:

- **UUID**: `ECUC:86beb2bd-8df4-4ab3-8099-8bbe89570625`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `UdpNmDemEventParameterRefs`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Container for the references to DemEventParameter elements which shall be invoked using the API Dem_ReportErrorStatus API in case the corresponding error occurs. The EventId is taken from the referenced DemEventParameter's DemEventId value. The standardized errors are provided in the container and can be extended by vendor specific error references.

######## 引用关系

此容器包含 **3** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. UDPNM_E_INIT_FAILED

- **UUID**: `ECUC:ab206b1c-01a6-407b-9c0b-c0ae68933b31`
- **引用名**: `UDPNM_E_INIT_FAILED`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `DemEventParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemConfigSet/DemEventParameter`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the DemEventParameter which shall be issued when the error "UdpNm initialization has failed, e.g. selected configuration set doesn't exist" has occured.

########## 2. UDPNM_E_NETWORK_TIMEOUT

- **UUID**: `ECUC:72a8f20b-7396-48ea-b063-309f4995dae1`
- **引用名**: `UDPNM_E_NETWORK_TIMEOUT`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `DemEventParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemConfigSet/DemEventParameter`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the DemEventParameter which shall be issued when the error "NM-Timeout Timer has abnormally expired outside of the Ready Sleep State" has occured.

########## 3. UDPNM_E_TCPIP_TRANSMIT_ERROR

- **UUID**: `ECUC:8932b083-bacb-4cea-bf4d-d67a2a5fbe5b`
- **引用名**: `UDPNM_E_TCPIP_TRANSMIT_ERROR`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `DemEventParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemConfigSet/DemEventParameter`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the DemEventParameter which shall be issued when the error "A call to the TCP/IP stack has failedA call to the TCP/IP stack has failed" has occured.

##### 2. UdpNmChannelConfig

**容器属性**:

- **UUID**: `ECUC:e1325106-da4a-41ce-bf5e-35cd50828ebb`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `UdpNmChannelConfig`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

This container contains the channel-specific configuration parameters of the UdpNm.

###### 参数配置

此容器包含 **13** 个参数：

####### INTEGER 类型参数

######## 1. UdpNmNodeId

- **UUID**: `ECUC:d2155218-8fce-4a97-8ff0-7a69e4edc276`
- **参数名**: `UdpNmNodeId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Node identifier of local node.

######## 2. UdpNmPduLength

- **UUID**: `ECUC:fd0077a4-20a9-47d0-b273-53cc7f9e3c44`
- **参数名**: `UdpNmPduLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..8]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the length of the NM PACKET in bytes.

######## 3. UdpNmUserDataLength

- **UUID**: `ECUC:9def7c0c-91d1-49ea-b731-340ff1071495`
- **参数名**: `UdpNmUserDataLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..8]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the length of the user data contained in the NM PACKET.

####### FLOAT 类型参数

######## 1. UpdNmMainFunctionPeriod

- **UUID**: `ECUC:a10f4184-38e5-4ff7-b9a8-5836e062ba10`
- **参数名**: `UpdNmMainFunctionPeriod`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0.001..0.255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Call cycle of UdpNm_MainFunction_x for the respective instance in [s].

######## 2. UpdNmMsgCycleOffset

- **UUID**: `ECUC:779f1019-0546-4e79-a1a4-a67eb484c8ab`
- **参数名**: `UpdNmMsgCycleOffset`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0..65.535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Time offset in the periodic transmission node. It determines the start delay of the transmission.

######## 3. UpdNmMsgCycleTime

- **UUID**: `ECUC:b88e9d62-7439-49fe-8289-db28bea050a1`
- **参数名**: `UpdNmMsgCycleTime`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0.001..65.535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Period of a NM-message. It determines the periodic rate in the "periodic transmission mode with bus load reduction" and is the basis for transmit scheduling in the "periodic transmission mode without bus load reduction".

######## 4. UpdNmMsgTimeoutTime

- **UUID**: `ECUC:1102aac7-9b16-476b-a775-6597bdba575d`
- **参数名**: `UpdNmMsgTimeoutTime`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0.001..65.535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Transmission Timout of NM-message. If there is no transmission confirmation by the UDP Interface within this timeout, the UDPNM module shall gibe an error notification.

######## 5. UpdNmRemoteSleepIndTime

- **UUID**: `ECUC:03bfa701-84e0-471a-ba23-7df014437c22`
- **参数名**: `UpdNmRemoteSleepIndTime`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0.001..65.535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Timeout for Remote Sleep Indication.

######## 6. UpdNmRepeatMessageTime

- **UUID**: `ECUC:5eba9538-90b4-4ff5-9c6f-3ee933ea4d83`
- **参数名**: `UpdNmRepeatMessageTime`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0..65.535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Timeout for Repeat Message State.

######## 7. UpdNmTimeoutTime

- **UUID**: `ECUC:c143e3dd-8d35-4bfb-8dd5-756d27fb9837`
- **参数名**: `UpdNmTimeoutTime`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0.002..65.535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Network Timeout for NM packets.

######## 8. UpdNmWaitBusSleepTime

- **UUID**: `ECUC:4180c1ae-0a74-4392-b779-7d938d0970d0`
- **参数名**: `UpdNmWaitBusSleepTime`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0.001..65.535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Timeout for bus calm down phase.

####### ENUMERATION 类型参数

######## 1. UdpNmPduCbvPosition

- **UUID**: `ECUC:907e8211-0182-477b-8ff1-7787f3d650b9`
- **参数名**: `UdpNmPduCbvPosition`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `UDPNM_PDU_BYTE_0` (来源: AUTOSAR_ECUC)
  - `UDPNM_PDU_BYTE_1` (来源: AUTOSAR_ECUC)
  - `UDPNM_PDU_OFF` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the position of the control bit vector within the NM PACKET.

######## 2. UdpNmPduNidPosition

- **UUID**: `ECUC:5a854a6b-ee2b-4be8-8913-957963a8478b`
- **参数名**: `UdpNmPduNidPosition`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `UDPNM_PDU_BYTE_0` (来源: AUTOSAR_ECUC)
  - `UDPNM_PDU_BYTE_1` (来源: AUTOSAR_ECUC)
  - `UDPNM_PDU_OFF` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the position of the source node identifier within the NM PACKET.

###### 引用关系

此容器包含 **1** 个引用：

####### SYMBOLIC-NAME-REFERENCE 类型引用

######## 1. UdpNmComMNetworkHandleRef

- **UUID**: `ECUC:bbca2ddc-438c-45cb-a7ad-a61d61c86900`
- **引用名**: `UdpNmComMNetworkHandleRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `ComMChannel`
- **完整路径**: `/AUTOSAR/EcucDefs/ComM/ComMConfigSet/ComMChannel`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This reference points to the unique channel defined by the ComMChannel and provides access to the unique channel index value in ComMChannelId.

###### 配置容器

本模块包含 **3** 个配置容器：

####### 1. UdpNmRxPdu

**容器属性**:

- **UUID**: `ECUC:480eeea9-ba4e-485a-952a-c231fb46da34`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `UdpNmRxPdu`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

This container describes the UdpNm RX PDU's.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. UdpNmRxPduId

- **UUID**: `ECUC:16e3d251-052d-427f-8c83-ad8491ecce20`
- **参数名**: `UdpNmRxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4294967296]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: ID of the RxPdu that will be used by a RxIndication of the lower layer.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. UdpNmRxPduRef

- **UUID**: `ECUC:a2db0564-e229-41c7-9fce-110d6baa3958`
- **引用名**: `UdpNmRxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The reference to a PDU in the global PDU structure described in the AUTOSAR ECU Configuration Specification. This reference will be used by the UdpNm module to derive the PDU Id.

####### 2. UdpNmTxPdu

**容器属性**:

- **UUID**: `ECUC:5046d451-94f4-4aa9-b257-b9bec9bc27b7`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `UdpNmTxPdu`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

This container describes the UdpNm TX PDU's.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. UdpNmTxConfirmationPduId

- **UUID**: `ECUC:1df43d6a-1c51-4232-8fb4-3ed791a1df64`
- **参数名**: `UdpNmTxConfirmationPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4294967296]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Id of the TxPdu that will be used by a TxConfirmation from the lower layer.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. UdpNmTxPduRef

- **UUID**: `ECUC:061a28ad-a374-4482-9b47-3b4c28f34600`
- **引用名**: `UdpNmTxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The reference to a PDU in the global PDU structure described in the AUTOSAR ECU Configuration Specification. This reference will be used by the UdpNm module to derive the PDU Id.

####### 3. UdpNmUserDataTxPdu

**容器属性**:

- **UUID**: `ECUC:85f5da66-01d5-4918-88a5-c8c9700e3eb7`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `UdpNmUserDataTxPdu`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This optional container is used to configure the UserNm PDU. This container is only available if UdpNmComUserDataSupport is enabled.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. UdpNmTxUserDataPduId

- **UUID**: `ECUC:7f47b0d7-eb63-4b7f-a84d-ad47b0e2943d`
- **参数名**: `UdpNmTxUserDataPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the Handle ID of the NM User Data I-PDU.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. UdpNmTxUserDataPduRef

- **UUID**: `ECUC:1dbba522-37a1-4dd1-8369-341d390a6fb5`
- **引用名**: `UdpNmTxUserDataPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the NM User Data I-PDU in the global PDU collection.

##### 3. UdpNmRxPdu

**容器属性**:

- **UUID**: `ECUC:480eeea9-ba4e-485a-952a-c231fb46da34`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `UdpNmRxPdu`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

This container describes the UdpNm RX PDU's.

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. UdpNmRxPduId

- **UUID**: `ECUC:16e3d251-052d-427f-8c83-ad8491ecce20`
- **参数名**: `UdpNmRxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4294967296]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: ID of the RxPdu that will be used by a RxIndication of the lower layer.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. UdpNmRxPduRef

- **UUID**: `ECUC:a2db0564-e229-41c7-9fce-110d6baa3958`
- **引用名**: `UdpNmRxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The reference to a PDU in the global PDU structure described in the AUTOSAR ECU Configuration Specification. This reference will be used by the UdpNm module to derive the PDU Id.

##### 4. UdpNmTxPdu

**容器属性**:

- **UUID**: `ECUC:5046d451-94f4-4aa9-b257-b9bec9bc27b7`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `UdpNmTxPdu`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

This container describes the UdpNm TX PDU's.

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. UdpNmTxConfirmationPduId

- **UUID**: `ECUC:1df43d6a-1c51-4232-8fb4-3ed791a1df64`
- **参数名**: `UdpNmTxConfirmationPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4294967296]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Id of the TxPdu that will be used by a TxConfirmation from the lower layer.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. UdpNmTxPduRef

- **UUID**: `ECUC:061a28ad-a374-4482-9b47-3b4c28f34600`
- **引用名**: `UdpNmTxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The reference to a PDU in the global PDU structure described in the AUTOSAR ECU Configuration Specification. This reference will be used by the UdpNm module to derive the PDU Id.

##### 5. UdpNmUserDataTxPdu

**容器属性**:

- **UUID**: `ECUC:85f5da66-01d5-4918-88a5-c8c9700e3eb7`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `UdpNmUserDataTxPdu`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This optional container is used to configure the UserNm PDU. This container is only available if UdpNmComUserDataSupport is enabled.

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. UdpNmTxUserDataPduId

- **UUID**: `ECUC:7f47b0d7-eb63-4b7f-a84d-ad47b0e2943d`
- **参数名**: `UdpNmTxUserDataPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the Handle ID of the NM User Data I-PDU.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. UdpNmTxUserDataPduRef

- **UUID**: `ECUC:1dbba522-37a1-4dd1-8369-341d390a6fb5`
- **引用名**: `UdpNmTxUserDataPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the NM User Data I-PDU in the global PDU collection.

##### 6. UdpNmDemEventParameterRefs

**容器属性**:

- **UUID**: `ECUC:86beb2bd-8df4-4ab3-8099-8bbe89570625`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `UdpNmDemEventParameterRefs`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Container for the references to DemEventParameter elements which shall be invoked using the API Dem_ReportErrorStatus API in case the corresponding error occurs. The EventId is taken from the referenced DemEventParameter's DemEventId value. The standardized errors are provided in the container and can be extended by vendor specific error references.

###### 引用关系

此容器包含 **3** 个引用：

####### SYMBOLIC-NAME-REFERENCE 类型引用

######## 1. UDPNM_E_INIT_FAILED

- **UUID**: `ECUC:ab206b1c-01a6-407b-9c0b-c0ae68933b31`
- **引用名**: `UDPNM_E_INIT_FAILED`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `DemEventParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemConfigSet/DemEventParameter`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the DemEventParameter which shall be issued when the error "UdpNm initialization has failed, e.g. selected configuration set doesn't exist" has occured.

######## 2. UDPNM_E_NETWORK_TIMEOUT

- **UUID**: `ECUC:72a8f20b-7396-48ea-b063-309f4995dae1`
- **引用名**: `UDPNM_E_NETWORK_TIMEOUT`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `DemEventParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemConfigSet/DemEventParameter`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the DemEventParameter which shall be issued when the error "NM-Timeout Timer has abnormally expired outside of the Ready Sleep State" has occured.

######## 3. UDPNM_E_TCPIP_TRANSMIT_ERROR

- **UUID**: `ECUC:8932b083-bacb-4cea-bf4d-d67a2a5fbe5b`
- **引用名**: `UDPNM_E_TCPIP_TRANSMIT_ERROR`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `DemEventParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemConfigSet/DemEventParameter`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the DemEventParameter which shall be issued when the error "A call to the TCP/IP stack has failedA call to the TCP/IP stack has failed" has occured.

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

1. **UdpNm**
