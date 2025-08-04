# Fr - 完整配置文档

*此文档由ARXML文件自动生成，采用层次化结构展示*

**生成时间**: 2025-06-16 14:46:19

## 📑 目录

- [📄 文件信息](#-文件信息)
- [🔧 模块定义](#-模块定义)
  - [Fr](#fr)
- [📦 包结构](#-包结构)

## 📄 文件信息

### Schema信息
- **Schema位置**: `http://autosar.org/schema/r4.0 AUTOSAR_4-0-3.xsd`
- **命名空间**: `http://autosar.org/schema/r4.0`

## 🔧 模块定义

### 1. Fr

#### 基本信息

- **UUID**: `ECUC:2a15b11b-34e9-4d70-ba06-0db1ba1683f8`
- **模块名称**: `Fr`
- **多重性**: [0..infinite]
- **支持的变体**:
  - VARIANT-POST-BUILD
  - VARIANT-PRE-COMPILE

#### 模块描述

Configuration of the Fr (FlexRay driver) module.

#### 版本历史

共有 **1** 个版本记录：

##### 1. 版本 4.2.0

- **发布日期**: 2011-11-09
- **发布者**: AUTOSAR

*此版本无详细变更记录*

#### 配置容器

本模块包含 **7** 个配置容器：

##### 1. FrGeneral

**容器属性**:

- **UUID**: `ECUC:b3e5d20a-0749-49ce-868a-6e44e55bd319`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FrGeneral`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

General configuration (parameters) of the FlexRay Driver module.

###### 参数配置

此容器包含 **8** 个参数：

####### INTEGER 类型参数

######## 1. FrCtrlTestCount

- **UUID**: `ECUC:f7190b81-1f47-444c-9d32-9e0e82e0c9f7`
- **参数名**: `FrCtrlTestCount`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `1`
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Maxmimum number of iterations the FlexRay controller hardware test is performed during controller initialization.

######## 2. FrIndex

- **UUID**: `ECUC:5ee7a7bf-1cc4-47de-a427-f11ea06fbb2f`
- **参数名**: `FrIndex`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies the InstanceId of this module instance. If only one instance is present it shall have the Id 0.

######## 3. FrNumCtrlSupported

- **UUID**: `ECUC:2a9eb7e5-0f0b-41c1-a27b-5e4021e02ff1`
- **参数名**: `FrNumCtrlSupported`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..256]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Determines the maximum number of communication controllers that the driver supports.

####### BOOLEAN 类型参数

######## 1. FrBufferReconfig

- **UUID**: `ECUC:44d1b50b-97cc-4635-89b3-d5c48f4ff1fe`
- **参数名**: `FrBufferReconfig`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enables or disables buffer reconfiguration at runtime.

######## 2. FrDevErrorDetect

- **UUID**: `ECUC:c18a7dea-5161-442c-8232-61c38c251e94`
- **参数名**: `FrDevErrorDetect`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Switches the Development Error Detection and Notification

######## 3. FrRxStringentCheck

- **UUID**: `ECUC:46202616-b70b-4edf-adff-f10f6e750624`
- **参数名**: `FrRxStringentCheck`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: If stringent check is enabled (true), received frames are only

######## 4. FrRxStringentLengthCheck

- **UUID**: `ECUC:6f6fc996-4dcb-458b-acce-465a0db38d3f`
- **参数名**: `FrRxStringentLengthCheck`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: If stringent check is enabled (true), received frames are only

######## 5. FrVersionInfoApi

- **UUID**: `ECUC:33fda032-3791-4e79-a96d-bb26532308d7`
- **参数名**: `FrVersionInfoApi`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enables/disables the existence of the Fr_GetVersionInfo API.

##### 2. FrMultipleConfiguration

**容器属性**:

- **UUID**: `ECUC:b6bb3a2a-b636-4ae2-98ff-ae92b378962e`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FrMultipleConfiguration`
- **多重性**: [1..1]
- **多配置容器**: true

**容器描述**:

Configuration of the individual controllers.

###### 配置容器

本模块包含 **5** 个配置容器：

####### 1. FrController

**容器属性**:

- **UUID**: `ECUC:6757a371-4453-46b9-9e8d-a290a0727138`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FrController`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

Configuration of the individual controller.

######## 参数配置

此容器包含 **33** 个参数：

######### INTEGER 类型参数

########## 1. FrCtrlIdx

- **UUID**: `ECUC:3a32cd48-9beb-49bf-9f69-8d9f992db560`
- **参数名**: `FrCtrlIdx`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Determines index of CC within Fr.

########## 2. FrPAllowPassiveToActive

- **UUID**: `ECUC:dd94c5b2-37fb-4abb-9410-9e4e3d7a0e73`
- **参数名**: `FrPAllowPassiveToActive`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..31]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Number of consecutive even/odd cycle pairs that must have valid clock correction terms before the CC will be allowed to transition from the POC:normal passive state to POC:normal active state. If set to zero, the CC is not allowed to transition from POC:normal passive to POC:normal active

########## 3. FrPClusterDriftDamping

- **UUID**: `ECUC:d35d03fb-d515-4b9f-9579-2d3f8e99c174`
- **参数名**: `FrPClusterDriftDamping`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..20]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Local cluster drift damping factor used for rate correction [Microticks].

########## 4. FrPDecodingCorrection

- **UUID**: `ECUC:31d98484-adf6-4157-b2e5-d1fc9e78d70b`
- **参数名**: `FrPDecodingCorrection`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [12..143]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Value used by the receiver to calculate the difference between primary time reference point and secondary time reference point [Microticks].

########## 5. FrPDelayCompensationA

- **UUID**: `ECUC:9427d10c-a311-43a6-b1f9-2afebeabb656`
- **参数名**: `FrPDelayCompensationA`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..211]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Value used to compensate for reception delays on the indicated channel. This covers assumed propagation delay up to cPropagationDelayMax for microticks in the range of 0.0125us to 0.05us [Microticks].

########## 6. FrPDelayCompensationB

- **UUID**: `ECUC:7e207545-f11a-47b6-a69f-95b6ad773e2a`
- **参数名**: `FrPDelayCompensationB`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..211]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Value used to compensate for reception delays on the indicated channel. This covers assumed propagation delay up to cPropagationDelayMax for microticks in the range of 0.0125us to 0.05us [Microticks].

########## 7. FrPKeySlotId

- **UUID**: `ECUC:bec8cdb4-9d4f-40f6-bc34-7c4b1db8501e`
- **参数名**: `FrPKeySlotId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..1023]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: ID of the key slot, i.e., the slot used to transmit the startup frame, sync frame, or designated key slot frame. If this parameter is set to zero the node does not have a key slot.

########## 8. FrPLatestTx

- **UUID**: `ECUC:5c0ed691-4e48-4e92-8fc5-6f288bda5c75`
- **参数名**: `FrPLatestTx`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..7988]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Number of the last minislot in which a frame transmission can start in the dynamic segment.

########## 9. FrPMacroInitialOffsetA

- **UUID**: `ECUC:ad06786f-950d-4eb2-b459-ad62b8312238`
- **参数名**: `FrPMacroInitialOffsetA`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [2..68]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Integer number of macroticks between the static slot boundary and the following macrotick boundary of the secondary time reference point based on the nominal macrotick duration [Macroticks].

########## 10. FrPMacroInitialOffsetB

- **UUID**: `ECUC:20667922-deba-4f36-a9fd-38bb73a8cb06`
- **参数名**: `FrPMacroInitialOffsetB`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [2..68]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Integer number of macroticks between the static slot boundary and the following macrotick boundary of the secondary time reference point based on the nominal macrotick duration [Macroticks].

########## 11. FrPMicroInitialOffsetA

- **UUID**: `ECUC:40d9b3f2-34e9-4df6-b5de-8cdff1df15ca`
- **参数名**: `FrPMicroInitialOffsetA`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..239]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Number of microticks between the secondary time reference point

########## 12. FrPMicroInitialOffsetB

- **UUID**: `ECUC:51f90f36-3a2b-476f-8f62-adff14ce2630`
- **参数名**: `FrPMicroInitialOffsetB`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..239]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Number of microticks between the secondary time reference point

########## 13. FrPMicroPerCycle

- **UUID**: `ECUC:ff796864-926f-40e2-bc7a-cf4a66ff0f93`
- **参数名**: `FrPMicroPerCycle`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [640..1280000]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Nominal number of microticks in the communication cycle of the local node. If nodes have different microtick durations this number will differ from node to node [Microticks].

########## 14. FrPOffsetCorrectionOut

- **UUID**: `ECUC:f18c4dbe-fe8e-4a72-8d55-4330369d3c2a`
- **参数名**: `FrPOffsetCorrectionOut`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [13..16082]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Magnitude of the maximum permissible offset correction value [Microticks]. Remark: Upper limit 15567 for FlexRay Protocol 2.1 Rev A compliance. Remark: Lower limit 15 for FlexRay Protocol 3.0 compliance.

########## 15. FrPOffsetCorrectionStart

- **UUID**: `ECUC:43ed0211-08ef-4c45-892c-079f9b547554`
- **参数名**: `FrPOffsetCorrectionStart`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [7..15999]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Start of the offset correction phase within the NIT, expressed as the number of macroticks from the start of cycle [Macroticks].

########## 16. FrPPayloadLengthDynMax

- **UUID**: `ECUC:43f079aa-f758-4d8a-9669-c2f1c04e26d3`
- **参数名**: `FrPPayloadLengthDynMax`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..127]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Maximum payload length for dynamic frames [16 bit words].

########## 17. FrPRateCorrectionOut

- **UUID**: `ECUC:b37acd1f-3189-480f-bfcb-5c1b977c5647`
- **参数名**: `FrPRateCorrectionOut`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [2..3846]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Magnitude of the maximum permissible rate correction value and the maximum drift offset between two nodes operating with unsynchronized clocks for one communication cycle [Microticks].

########## 18. FrPSecondKeySlotId

- **UUID**: `ECUC:c7c872e2-01cc-476d-b1b8-f84f79b9648b`
- **参数名**: `FrPSecondKeySlotId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..1023]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: ID of the second key slot, in which a second startup frame shall be sent when operating as a coldstart node in a TT-L or TT-D cluster. If this parameter is set to zero the node does not have a second key slot.

########## 19. FrPWakeupPattern

- **UUID**: `ECUC:a52c277d-177f-4992-b089-be89fe0aa5ed`
- **参数名**: `FrPWakeupPattern`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..63]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Number of repetitions of the wakeup symbol that are combined to form a wakeup pattern when the node enters the POC:wakeup send state.

########## 20. FrPdAcceptedStartupRange

- **UUID**: `ECUC:4ac029b8-197f-4cc4-83ca-25020717392a`
- **参数名**: `FrPdAcceptedStartupRange`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..2743]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Expanded range of measured clock deviation allowed for startup frames during integration [Microticks].

########## 21. FrPdListenTimeout

- **UUID**: `ECUC:0dbbe505-256f-425c-ab34-174f06f85168`
- **参数名**: `FrPdListenTimeout`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1284..2567692]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Value for the startup listen timeout and wakeup listen timeout. Although this is a node local parameter, the real time equivalent of this value should be the same for all nodes in the cluster [Microticks].

######### BOOLEAN 类型参数

########## 1. FrPAllowHaltDueToClock

- **UUID**: `ECUC:3f506b12-a90f-41c1-adb7-983f01e34a7c`
- **参数名**: `FrPAllowHaltDueToClock`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Boolean flag that controls the transition to the POC:halt state due to a clock synchronization errors. If set to true, the CC is allowed to transition to POC:halt. If set to false, the CC will not transition to the POC:halt state but will enter or remain in the POC:normal passive state (self healing would still be possible)

########## 2. FrPExternalSync

- **UUID**: `ECUC:61a1d599-e805-4930-99fe-5e1bf35fd853`
- **参数名**: `FrPExternalSync`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Flag indicating whether the node is externally synchronized (operating as time gateway sink in an TT-E cluster) or locally synchronized.

########## 3. FrPFallBackInternal

- **UUID**: `ECUC:2005326b-79c7-49c1-970f-add1213853cc`
- **参数名**: `FrPFallBackInternal`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Flag indicating whether a time gateway sink node will switch to local clock operation when synchronization with the time gateway source node is lost (FrPFallBackInternal = true) or will instead go to POC:ready (FrPFallBackInternal =false).

########## 4. FrPKeySlotOnlyEnabled

- **UUID**: `ECUC:d48290b7-aa14-422e-9a84-9097fc549a38`
- **参数名**: `FrPKeySlotOnlyEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Flag indicating whether or not the node shall enter key slot only mode following startup.

########## 5. FrPKeySlotUsedForStartup

- **UUID**: `ECUC:810f7e48-5750-4a4e-8b21-152b66f130ea`
- **参数名**: `FrPKeySlotUsedForStartup`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Flag indicating whether the key slot is used to transmit a startup frame.

########## 6. FrPKeySlotUsedForSync

- **UUID**: `ECUC:1696b596-e09b-490b-bd0d-f9e18828881c`
- **参数名**: `FrPKeySlotUsedForSync`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Flag indicating whether the key slot is used to transmit a sync frame.

########## 7. FrPNmVectorEarlyUpdate

- **UUID**: `ECUC:2742b5f9-78a1-4afe-9302-a991716fe921`
- **参数名**: `FrPNmVectorEarlyUpdate`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Flag indicating when the update of the Network Management Vector

########## 8. FrPTwoKeySlotMode

- **UUID**: `ECUC:f9bc7991-84b4-4006-9293-4b069ef7e008`
- **参数名**: `FrPTwoKeySlotMode`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Flag indicating whether node operates as a coldstart node in a TT-E or TT-L cluster.

######### ENUMERATION 类型参数

########## 1. FrPChannels

- **UUID**: `ECUC:89ff60e9-30c8-447e-a909-381b3a08180f`
- **参数名**: `FrPChannels`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `FR_CHANNEL_A` (来源: AUTOSAR_ECUC)
  - `FR_CHANNEL_AB` (来源: AUTOSAR_ECUC)
  - `FR_CHANNEL_B` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Channels to which the node is connected.

########## 2. FrPSamplesPerMicrotick

- **UUID**: `ECUC:1ef53e04-3f48-4b0e-abc6-75e397bc291e`
- **参数名**: `FrPSamplesPerMicrotick`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `N1SAMPLES` (来源: AUTOSAR_ECUC)
  - `N2SAMPLES` (来源: AUTOSAR_ECUC)
  - `N4SAMPLES` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Number of samples per microtick. Remark: Allowed range N1SAMPLES, N2SAMPLES for FlexRay Protocol 3.0 compliance.

########## 3. FrPWakeupChannel

- **UUID**: `ECUC:5f91c8c6-e7c5-4c9d-a5d2-68ee4dfad7d5`
- **参数名**: `FrPWakeupChannel`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `FR_CHANNEL_A` (来源: AUTOSAR_ECUC)
  - `FR_CHANNEL_B` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Channel used by the node to send a wakeup pattern.

########## 4. FrPdMicrotick

- **UUID**: `ECUC:725263ab-2b44-4e77-b194-00c92500df40`
- **参数名**: `FrPdMicrotick`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `T100NS` (来源: AUTOSAR_ECUC)
  - `T12_5NS` (来源: AUTOSAR_ECUC)
  - `T25NS` (来源: AUTOSAR_ECUC)
  - `T50NS` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Duration of a microtick.

######## 配置容器

本模块包含 **4** 个配置容器：

######### 1. FrAbsoluteTimer

**容器属性**:

- **UUID**: `ECUC:a0b8d859-52ca-42da-98ae-4e83337a8c9a`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FrAbsoluteTimer`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

Specifies the absolute timer configuration parameters of the Fr.

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. FrAbsTimerIdx

- **UUID**: `ECUC:506f6ded-1210-4382-9eae-e064b94ed945`
- **参数名**: `FrAbsTimerIdx`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..254]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Contains the index of an absolute timer contained in Fr on a certain FlexRay CC.

######### 2. FrControllerDemEventParameterRefs

**容器属性**:

- **UUID**: `ECUC:ab12d9ad-0d6a-497b-ace4-5d9638033158`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FrControllerDemEventParameterRefs`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Container for the references to DemEventParameter elements which shall be invoked using the API Dem_ReportErrorStatus API in case the corresponding error occurs. The EventId is taken from the referenced DemEventParameter's DemEventId value. The standardized errors are provided in the container and can be extended by vendor specific error references.

########## 引用关系

此容器包含 **1** 个引用：

########### SYMBOLIC-NAME-REFERENCE 类型引用

############ 1. FrDemCtrlTestResultRef

- **UUID**: `ECUC:875582b1-4980-463c-a9f2-b1f9b1b2e00a`
- **引用名**: `FrDemCtrlTestResultRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `DemEventParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemConfigSet/DemEventParameter`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to DEM event Id that is reported for FlexRay

######### 3. FrFifo

**容器属性**:

- **UUID**: `ECUC:8cef4957-b4d3-49e6-a231-b775f3644c93`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FrFifo`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

One First In First Out (FIFO) queued receive structure, defining the admittance criteria to the FIFO, and mandating the ability to admit messages into the FIFO based on Message Id filtering criteria.

########## 参数配置

此容器包含 **7** 个参数：

########### INTEGER 类型参数

############ 1. FrBaseCycle

- **UUID**: `ECUC:318f7ec1-ad27-45b9-91b7-720d884775d3`
- **参数名**: `FrBaseCycle`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..63]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: FIFO cycle counter acceptance criteria.

############ 2. FrCycleRepetition

- **UUID**: `ECUC:454b7138-41d8-4c73-94ec-a6552230728f`
- **参数名**: `FrCycleRepetition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..64]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: FIFO cylce counter acceptance criteria. Valid values are  1,2,4,5,8,10,16,20,32,40,50,64.

############ 3. FrFifoDepth

- **UUID**: `ECUC:a3d62a6e-c11e-48b7-be8e-16b4a996ae36`
- **参数名**: `FrFifoDepth`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..2048]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Fifo Depth.

############ 4. FrMsgIdMask

- **UUID**: `ECUC:fe24e9f9-ac78-4890-8ae7-8f612d08af57`
- **参数名**: `FrMsgIdMask`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: FIFO message identifier acceptance criteria (Mask filter).

############ 5. FrMsgIdMatch

- **UUID**: `ECUC:31e96e81-1722-4483-a674-8c1ac007e9b9`
- **参数名**: `FrMsgIdMatch`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: FIFO message identifier acceptance criteria (Match filter).

########### BOOLEAN 类型参数

############ 1. FrAdmitWithoutMessageId

- **UUID**: `ECUC:26ee1fad-7fb9-490f-a2d0-54e10ba61e1d`
- **参数名**: `FrAdmitWithoutMessageId`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Determines whether or not frames received in the dynamic segment that don't contain a message ID will be admitted into the FIFO.

########### ENUMERATION 类型参数

############ 1. FrChannels

- **UUID**: `ECUC:ed2ae862-5f03-4f1d-bbd7-453c14c506c0`
- **参数名**: `FrChannels`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `FR_CHANNEL_A` (来源: AUTOSAR_ECUC)
  - `FR_CHANNEL_AB` (来源: AUTOSAR_ECUC)
  - `FR_CHANNEL_B` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: FIFO channel admittance criteria.

########## 配置容器

本模块包含 **1** 个配置容器：

########### 1. FrRange

**容器属性**:

- **UUID**: `ECUC:f989ae03-b776-4ea2-a8d3-f2d0b872350f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FrRange`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

FIFO Frame Id range acceptance criteria.

############ 参数配置

此容器包含 **2** 个参数：

############# INTEGER 类型参数

############## 1. FrRangeMax

- **UUID**: `ECUC:7217fbcd-ccbf-4958-a5ca-12d7c84c9410`
- **参数名**: `FrRangeMax`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..2047]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Last FrameId of this range that will be accepted by the FIFO.

############## 2. FrRangeMin

- **UUID**: `ECUC:1ea0cf4e-710f-4137-9df4-ce3975680ede`
- **参数名**: `FrRangeMin`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..2047]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: First FrameId of this range that will be accepted by the FIFO.

######### 4. FrRange

**容器属性**:

- **UUID**: `ECUC:f989ae03-b776-4ea2-a8d3-f2d0b872350f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FrRange`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

FIFO Frame Id range acceptance criteria.

########## 参数配置

此容器包含 **2** 个参数：

########### INTEGER 类型参数

############ 1. FrRangeMax

- **UUID**: `ECUC:7217fbcd-ccbf-4958-a5ca-12d7c84c9410`
- **参数名**: `FrRangeMax`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..2047]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Last FrameId of this range that will be accepted by the FIFO.

############ 2. FrRangeMin

- **UUID**: `ECUC:1ea0cf4e-710f-4137-9df4-ce3975680ede`
- **参数名**: `FrRangeMin`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..2047]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: First FrameId of this range that will be accepted by the FIFO.

####### 2. FrAbsoluteTimer

**容器属性**:

- **UUID**: `ECUC:a0b8d859-52ca-42da-98ae-4e83337a8c9a`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FrAbsoluteTimer`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

Specifies the absolute timer configuration parameters of the Fr.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. FrAbsTimerIdx

- **UUID**: `ECUC:506f6ded-1210-4382-9eae-e064b94ed945`
- **参数名**: `FrAbsTimerIdx`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..254]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Contains the index of an absolute timer contained in Fr on a certain FlexRay CC.

####### 3. FrControllerDemEventParameterRefs

**容器属性**:

- **UUID**: `ECUC:ab12d9ad-0d6a-497b-ace4-5d9638033158`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FrControllerDemEventParameterRefs`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Container for the references to DemEventParameter elements which shall be invoked using the API Dem_ReportErrorStatus API in case the corresponding error occurs. The EventId is taken from the referenced DemEventParameter's DemEventId value. The standardized errors are provided in the container and can be extended by vendor specific error references.

######## 引用关系

此容器包含 **1** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. FrDemCtrlTestResultRef

- **UUID**: `ECUC:875582b1-4980-463c-a9f2-b1f9b1b2e00a`
- **引用名**: `FrDemCtrlTestResultRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `DemEventParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemConfigSet/DemEventParameter`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to DEM event Id that is reported for FlexRay

####### 4. FrFifo

**容器属性**:

- **UUID**: `ECUC:8cef4957-b4d3-49e6-a231-b775f3644c93`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FrFifo`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

One First In First Out (FIFO) queued receive structure, defining the admittance criteria to the FIFO, and mandating the ability to admit messages into the FIFO based on Message Id filtering criteria.

######## 参数配置

此容器包含 **7** 个参数：

######### INTEGER 类型参数

########## 1. FrBaseCycle

- **UUID**: `ECUC:318f7ec1-ad27-45b9-91b7-720d884775d3`
- **参数名**: `FrBaseCycle`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..63]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: FIFO cycle counter acceptance criteria.

########## 2. FrCycleRepetition

- **UUID**: `ECUC:454b7138-41d8-4c73-94ec-a6552230728f`
- **参数名**: `FrCycleRepetition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..64]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: FIFO cylce counter acceptance criteria. Valid values are  1,2,4,5,8,10,16,20,32,40,50,64.

########## 3. FrFifoDepth

- **UUID**: `ECUC:a3d62a6e-c11e-48b7-be8e-16b4a996ae36`
- **参数名**: `FrFifoDepth`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..2048]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Fifo Depth.

########## 4. FrMsgIdMask

- **UUID**: `ECUC:fe24e9f9-ac78-4890-8ae7-8f612d08af57`
- **参数名**: `FrMsgIdMask`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: FIFO message identifier acceptance criteria (Mask filter).

########## 5. FrMsgIdMatch

- **UUID**: `ECUC:31e96e81-1722-4483-a674-8c1ac007e9b9`
- **参数名**: `FrMsgIdMatch`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: FIFO message identifier acceptance criteria (Match filter).

######### BOOLEAN 类型参数

########## 1. FrAdmitWithoutMessageId

- **UUID**: `ECUC:26ee1fad-7fb9-490f-a2d0-54e10ba61e1d`
- **参数名**: `FrAdmitWithoutMessageId`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Determines whether or not frames received in the dynamic segment that don't contain a message ID will be admitted into the FIFO.

######### ENUMERATION 类型参数

########## 1. FrChannels

- **UUID**: `ECUC:ed2ae862-5f03-4f1d-bbd7-453c14c506c0`
- **参数名**: `FrChannels`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `FR_CHANNEL_A` (来源: AUTOSAR_ECUC)
  - `FR_CHANNEL_AB` (来源: AUTOSAR_ECUC)
  - `FR_CHANNEL_B` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: FIFO channel admittance criteria.

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. FrRange

**容器属性**:

- **UUID**: `ECUC:f989ae03-b776-4ea2-a8d3-f2d0b872350f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FrRange`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

FIFO Frame Id range acceptance criteria.

########## 参数配置

此容器包含 **2** 个参数：

########### INTEGER 类型参数

############ 1. FrRangeMax

- **UUID**: `ECUC:7217fbcd-ccbf-4958-a5ca-12d7c84c9410`
- **参数名**: `FrRangeMax`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..2047]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Last FrameId of this range that will be accepted by the FIFO.

############ 2. FrRangeMin

- **UUID**: `ECUC:1ea0cf4e-710f-4137-9df4-ce3975680ede`
- **参数名**: `FrRangeMin`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..2047]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: First FrameId of this range that will be accepted by the FIFO.

####### 5. FrRange

**容器属性**:

- **UUID**: `ECUC:f989ae03-b776-4ea2-a8d3-f2d0b872350f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FrRange`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

FIFO Frame Id range acceptance criteria.

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. FrRangeMax

- **UUID**: `ECUC:7217fbcd-ccbf-4958-a5ca-12d7c84c9410`
- **参数名**: `FrRangeMax`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..2047]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Last FrameId of this range that will be accepted by the FIFO.

########## 2. FrRangeMin

- **UUID**: `ECUC:1ea0cf4e-710f-4137-9df4-ce3975680ede`
- **参数名**: `FrRangeMin`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..2047]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: First FrameId of this range that will be accepted by the FIFO.

##### 3. FrController

**容器属性**:

- **UUID**: `ECUC:6757a371-4453-46b9-9e8d-a290a0727138`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FrController`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

Configuration of the individual controller.

###### 参数配置

此容器包含 **33** 个参数：

####### INTEGER 类型参数

######## 1. FrCtrlIdx

- **UUID**: `ECUC:3a32cd48-9beb-49bf-9f69-8d9f992db560`
- **参数名**: `FrCtrlIdx`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Determines index of CC within Fr.

######## 2. FrPAllowPassiveToActive

- **UUID**: `ECUC:dd94c5b2-37fb-4abb-9410-9e4e3d7a0e73`
- **参数名**: `FrPAllowPassiveToActive`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..31]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Number of consecutive even/odd cycle pairs that must have valid clock correction terms before the CC will be allowed to transition from the POC:normal passive state to POC:normal active state. If set to zero, the CC is not allowed to transition from POC:normal passive to POC:normal active

######## 3. FrPClusterDriftDamping

- **UUID**: `ECUC:d35d03fb-d515-4b9f-9579-2d3f8e99c174`
- **参数名**: `FrPClusterDriftDamping`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..20]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Local cluster drift damping factor used for rate correction [Microticks].

######## 4. FrPDecodingCorrection

- **UUID**: `ECUC:31d98484-adf6-4157-b2e5-d1fc9e78d70b`
- **参数名**: `FrPDecodingCorrection`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [12..143]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Value used by the receiver to calculate the difference between primary time reference point and secondary time reference point [Microticks].

######## 5. FrPDelayCompensationA

- **UUID**: `ECUC:9427d10c-a311-43a6-b1f9-2afebeabb656`
- **参数名**: `FrPDelayCompensationA`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..211]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Value used to compensate for reception delays on the indicated channel. This covers assumed propagation delay up to cPropagationDelayMax for microticks in the range of 0.0125us to 0.05us [Microticks].

######## 6. FrPDelayCompensationB

- **UUID**: `ECUC:7e207545-f11a-47b6-a69f-95b6ad773e2a`
- **参数名**: `FrPDelayCompensationB`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..211]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Value used to compensate for reception delays on the indicated channel. This covers assumed propagation delay up to cPropagationDelayMax for microticks in the range of 0.0125us to 0.05us [Microticks].

######## 7. FrPKeySlotId

- **UUID**: `ECUC:bec8cdb4-9d4f-40f6-bc34-7c4b1db8501e`
- **参数名**: `FrPKeySlotId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..1023]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: ID of the key slot, i.e., the slot used to transmit the startup frame, sync frame, or designated key slot frame. If this parameter is set to zero the node does not have a key slot.

######## 8. FrPLatestTx

- **UUID**: `ECUC:5c0ed691-4e48-4e92-8fc5-6f288bda5c75`
- **参数名**: `FrPLatestTx`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..7988]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Number of the last minislot in which a frame transmission can start in the dynamic segment.

######## 9. FrPMacroInitialOffsetA

- **UUID**: `ECUC:ad06786f-950d-4eb2-b459-ad62b8312238`
- **参数名**: `FrPMacroInitialOffsetA`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [2..68]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Integer number of macroticks between the static slot boundary and the following macrotick boundary of the secondary time reference point based on the nominal macrotick duration [Macroticks].

######## 10. FrPMacroInitialOffsetB

- **UUID**: `ECUC:20667922-deba-4f36-a9fd-38bb73a8cb06`
- **参数名**: `FrPMacroInitialOffsetB`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [2..68]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Integer number of macroticks between the static slot boundary and the following macrotick boundary of the secondary time reference point based on the nominal macrotick duration [Macroticks].

######## 11. FrPMicroInitialOffsetA

- **UUID**: `ECUC:40d9b3f2-34e9-4df6-b5de-8cdff1df15ca`
- **参数名**: `FrPMicroInitialOffsetA`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..239]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Number of microticks between the secondary time reference point

######## 12. FrPMicroInitialOffsetB

- **UUID**: `ECUC:51f90f36-3a2b-476f-8f62-adff14ce2630`
- **参数名**: `FrPMicroInitialOffsetB`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..239]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Number of microticks between the secondary time reference point

######## 13. FrPMicroPerCycle

- **UUID**: `ECUC:ff796864-926f-40e2-bc7a-cf4a66ff0f93`
- **参数名**: `FrPMicroPerCycle`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [640..1280000]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Nominal number of microticks in the communication cycle of the local node. If nodes have different microtick durations this number will differ from node to node [Microticks].

######## 14. FrPOffsetCorrectionOut

- **UUID**: `ECUC:f18c4dbe-fe8e-4a72-8d55-4330369d3c2a`
- **参数名**: `FrPOffsetCorrectionOut`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [13..16082]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Magnitude of the maximum permissible offset correction value [Microticks]. Remark: Upper limit 15567 for FlexRay Protocol 2.1 Rev A compliance. Remark: Lower limit 15 for FlexRay Protocol 3.0 compliance.

######## 15. FrPOffsetCorrectionStart

- **UUID**: `ECUC:43ed0211-08ef-4c45-892c-079f9b547554`
- **参数名**: `FrPOffsetCorrectionStart`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [7..15999]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Start of the offset correction phase within the NIT, expressed as the number of macroticks from the start of cycle [Macroticks].

######## 16. FrPPayloadLengthDynMax

- **UUID**: `ECUC:43f079aa-f758-4d8a-9669-c2f1c04e26d3`
- **参数名**: `FrPPayloadLengthDynMax`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..127]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Maximum payload length for dynamic frames [16 bit words].

######## 17. FrPRateCorrectionOut

- **UUID**: `ECUC:b37acd1f-3189-480f-bfcb-5c1b977c5647`
- **参数名**: `FrPRateCorrectionOut`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [2..3846]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Magnitude of the maximum permissible rate correction value and the maximum drift offset between two nodes operating with unsynchronized clocks for one communication cycle [Microticks].

######## 18. FrPSecondKeySlotId

- **UUID**: `ECUC:c7c872e2-01cc-476d-b1b8-f84f79b9648b`
- **参数名**: `FrPSecondKeySlotId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..1023]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: ID of the second key slot, in which a second startup frame shall be sent when operating as a coldstart node in a TT-L or TT-D cluster. If this parameter is set to zero the node does not have a second key slot.

######## 19. FrPWakeupPattern

- **UUID**: `ECUC:a52c277d-177f-4992-b089-be89fe0aa5ed`
- **参数名**: `FrPWakeupPattern`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..63]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Number of repetitions of the wakeup symbol that are combined to form a wakeup pattern when the node enters the POC:wakeup send state.

######## 20. FrPdAcceptedStartupRange

- **UUID**: `ECUC:4ac029b8-197f-4cc4-83ca-25020717392a`
- **参数名**: `FrPdAcceptedStartupRange`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..2743]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Expanded range of measured clock deviation allowed for startup frames during integration [Microticks].

######## 21. FrPdListenTimeout

- **UUID**: `ECUC:0dbbe505-256f-425c-ab34-174f06f85168`
- **参数名**: `FrPdListenTimeout`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1284..2567692]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Value for the startup listen timeout and wakeup listen timeout. Although this is a node local parameter, the real time equivalent of this value should be the same for all nodes in the cluster [Microticks].

####### BOOLEAN 类型参数

######## 1. FrPAllowHaltDueToClock

- **UUID**: `ECUC:3f506b12-a90f-41c1-adb7-983f01e34a7c`
- **参数名**: `FrPAllowHaltDueToClock`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Boolean flag that controls the transition to the POC:halt state due to a clock synchronization errors. If set to true, the CC is allowed to transition to POC:halt. If set to false, the CC will not transition to the POC:halt state but will enter or remain in the POC:normal passive state (self healing would still be possible)

######## 2. FrPExternalSync

- **UUID**: `ECUC:61a1d599-e805-4930-99fe-5e1bf35fd853`
- **参数名**: `FrPExternalSync`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Flag indicating whether the node is externally synchronized (operating as time gateway sink in an TT-E cluster) or locally synchronized.

######## 3. FrPFallBackInternal

- **UUID**: `ECUC:2005326b-79c7-49c1-970f-add1213853cc`
- **参数名**: `FrPFallBackInternal`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Flag indicating whether a time gateway sink node will switch to local clock operation when synchronization with the time gateway source node is lost (FrPFallBackInternal = true) or will instead go to POC:ready (FrPFallBackInternal =false).

######## 4. FrPKeySlotOnlyEnabled

- **UUID**: `ECUC:d48290b7-aa14-422e-9a84-9097fc549a38`
- **参数名**: `FrPKeySlotOnlyEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Flag indicating whether or not the node shall enter key slot only mode following startup.

######## 5. FrPKeySlotUsedForStartup

- **UUID**: `ECUC:810f7e48-5750-4a4e-8b21-152b66f130ea`
- **参数名**: `FrPKeySlotUsedForStartup`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Flag indicating whether the key slot is used to transmit a startup frame.

######## 6. FrPKeySlotUsedForSync

- **UUID**: `ECUC:1696b596-e09b-490b-bd0d-f9e18828881c`
- **参数名**: `FrPKeySlotUsedForSync`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Flag indicating whether the key slot is used to transmit a sync frame.

######## 7. FrPNmVectorEarlyUpdate

- **UUID**: `ECUC:2742b5f9-78a1-4afe-9302-a991716fe921`
- **参数名**: `FrPNmVectorEarlyUpdate`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Flag indicating when the update of the Network Management Vector

######## 8. FrPTwoKeySlotMode

- **UUID**: `ECUC:f9bc7991-84b4-4006-9293-4b069ef7e008`
- **参数名**: `FrPTwoKeySlotMode`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Flag indicating whether node operates as a coldstart node in a TT-E or TT-L cluster.

####### ENUMERATION 类型参数

######## 1. FrPChannels

- **UUID**: `ECUC:89ff60e9-30c8-447e-a909-381b3a08180f`
- **参数名**: `FrPChannels`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `FR_CHANNEL_A` (来源: AUTOSAR_ECUC)
  - `FR_CHANNEL_AB` (来源: AUTOSAR_ECUC)
  - `FR_CHANNEL_B` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Channels to which the node is connected.

######## 2. FrPSamplesPerMicrotick

- **UUID**: `ECUC:1ef53e04-3f48-4b0e-abc6-75e397bc291e`
- **参数名**: `FrPSamplesPerMicrotick`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `N1SAMPLES` (来源: AUTOSAR_ECUC)
  - `N2SAMPLES` (来源: AUTOSAR_ECUC)
  - `N4SAMPLES` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Number of samples per microtick. Remark: Allowed range N1SAMPLES, N2SAMPLES for FlexRay Protocol 3.0 compliance.

######## 3. FrPWakeupChannel

- **UUID**: `ECUC:5f91c8c6-e7c5-4c9d-a5d2-68ee4dfad7d5`
- **参数名**: `FrPWakeupChannel`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `FR_CHANNEL_A` (来源: AUTOSAR_ECUC)
  - `FR_CHANNEL_B` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Channel used by the node to send a wakeup pattern.

######## 4. FrPdMicrotick

- **UUID**: `ECUC:725263ab-2b44-4e77-b194-00c92500df40`
- **参数名**: `FrPdMicrotick`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `T100NS` (来源: AUTOSAR_ECUC)
  - `T12_5NS` (来源: AUTOSAR_ECUC)
  - `T25NS` (来源: AUTOSAR_ECUC)
  - `T50NS` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Duration of a microtick.

###### 配置容器

本模块包含 **4** 个配置容器：

####### 1. FrAbsoluteTimer

**容器属性**:

- **UUID**: `ECUC:a0b8d859-52ca-42da-98ae-4e83337a8c9a`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FrAbsoluteTimer`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

Specifies the absolute timer configuration parameters of the Fr.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. FrAbsTimerIdx

- **UUID**: `ECUC:506f6ded-1210-4382-9eae-e064b94ed945`
- **参数名**: `FrAbsTimerIdx`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..254]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Contains the index of an absolute timer contained in Fr on a certain FlexRay CC.

####### 2. FrControllerDemEventParameterRefs

**容器属性**:

- **UUID**: `ECUC:ab12d9ad-0d6a-497b-ace4-5d9638033158`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FrControllerDemEventParameterRefs`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Container for the references to DemEventParameter elements which shall be invoked using the API Dem_ReportErrorStatus API in case the corresponding error occurs. The EventId is taken from the referenced DemEventParameter's DemEventId value. The standardized errors are provided in the container and can be extended by vendor specific error references.

######## 引用关系

此容器包含 **1** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. FrDemCtrlTestResultRef

- **UUID**: `ECUC:875582b1-4980-463c-a9f2-b1f9b1b2e00a`
- **引用名**: `FrDemCtrlTestResultRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `DemEventParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemConfigSet/DemEventParameter`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to DEM event Id that is reported for FlexRay

####### 3. FrFifo

**容器属性**:

- **UUID**: `ECUC:8cef4957-b4d3-49e6-a231-b775f3644c93`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FrFifo`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

One First In First Out (FIFO) queued receive structure, defining the admittance criteria to the FIFO, and mandating the ability to admit messages into the FIFO based on Message Id filtering criteria.

######## 参数配置

此容器包含 **7** 个参数：

######### INTEGER 类型参数

########## 1. FrBaseCycle

- **UUID**: `ECUC:318f7ec1-ad27-45b9-91b7-720d884775d3`
- **参数名**: `FrBaseCycle`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..63]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: FIFO cycle counter acceptance criteria.

########## 2. FrCycleRepetition

- **UUID**: `ECUC:454b7138-41d8-4c73-94ec-a6552230728f`
- **参数名**: `FrCycleRepetition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..64]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: FIFO cylce counter acceptance criteria. Valid values are  1,2,4,5,8,10,16,20,32,40,50,64.

########## 3. FrFifoDepth

- **UUID**: `ECUC:a3d62a6e-c11e-48b7-be8e-16b4a996ae36`
- **参数名**: `FrFifoDepth`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..2048]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Fifo Depth.

########## 4. FrMsgIdMask

- **UUID**: `ECUC:fe24e9f9-ac78-4890-8ae7-8f612d08af57`
- **参数名**: `FrMsgIdMask`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: FIFO message identifier acceptance criteria (Mask filter).

########## 5. FrMsgIdMatch

- **UUID**: `ECUC:31e96e81-1722-4483-a674-8c1ac007e9b9`
- **参数名**: `FrMsgIdMatch`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: FIFO message identifier acceptance criteria (Match filter).

######### BOOLEAN 类型参数

########## 1. FrAdmitWithoutMessageId

- **UUID**: `ECUC:26ee1fad-7fb9-490f-a2d0-54e10ba61e1d`
- **参数名**: `FrAdmitWithoutMessageId`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Determines whether or not frames received in the dynamic segment that don't contain a message ID will be admitted into the FIFO.

######### ENUMERATION 类型参数

########## 1. FrChannels

- **UUID**: `ECUC:ed2ae862-5f03-4f1d-bbd7-453c14c506c0`
- **参数名**: `FrChannels`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `FR_CHANNEL_A` (来源: AUTOSAR_ECUC)
  - `FR_CHANNEL_AB` (来源: AUTOSAR_ECUC)
  - `FR_CHANNEL_B` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: FIFO channel admittance criteria.

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. FrRange

**容器属性**:

- **UUID**: `ECUC:f989ae03-b776-4ea2-a8d3-f2d0b872350f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FrRange`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

FIFO Frame Id range acceptance criteria.

########## 参数配置

此容器包含 **2** 个参数：

########### INTEGER 类型参数

############ 1. FrRangeMax

- **UUID**: `ECUC:7217fbcd-ccbf-4958-a5ca-12d7c84c9410`
- **参数名**: `FrRangeMax`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..2047]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Last FrameId of this range that will be accepted by the FIFO.

############ 2. FrRangeMin

- **UUID**: `ECUC:1ea0cf4e-710f-4137-9df4-ce3975680ede`
- **参数名**: `FrRangeMin`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..2047]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: First FrameId of this range that will be accepted by the FIFO.

####### 4. FrRange

**容器属性**:

- **UUID**: `ECUC:f989ae03-b776-4ea2-a8d3-f2d0b872350f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FrRange`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

FIFO Frame Id range acceptance criteria.

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. FrRangeMax

- **UUID**: `ECUC:7217fbcd-ccbf-4958-a5ca-12d7c84c9410`
- **参数名**: `FrRangeMax`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..2047]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Last FrameId of this range that will be accepted by the FIFO.

########## 2. FrRangeMin

- **UUID**: `ECUC:1ea0cf4e-710f-4137-9df4-ce3975680ede`
- **参数名**: `FrRangeMin`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..2047]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: First FrameId of this range that will be accepted by the FIFO.

##### 4. FrAbsoluteTimer

**容器属性**:

- **UUID**: `ECUC:a0b8d859-52ca-42da-98ae-4e83337a8c9a`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FrAbsoluteTimer`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

Specifies the absolute timer configuration parameters of the Fr.

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. FrAbsTimerIdx

- **UUID**: `ECUC:506f6ded-1210-4382-9eae-e064b94ed945`
- **参数名**: `FrAbsTimerIdx`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..254]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Contains the index of an absolute timer contained in Fr on a certain FlexRay CC.

##### 5. FrControllerDemEventParameterRefs

**容器属性**:

- **UUID**: `ECUC:ab12d9ad-0d6a-497b-ace4-5d9638033158`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FrControllerDemEventParameterRefs`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Container for the references to DemEventParameter elements which shall be invoked using the API Dem_ReportErrorStatus API in case the corresponding error occurs. The EventId is taken from the referenced DemEventParameter's DemEventId value. The standardized errors are provided in the container and can be extended by vendor specific error references.

###### 引用关系

此容器包含 **1** 个引用：

####### SYMBOLIC-NAME-REFERENCE 类型引用

######## 1. FrDemCtrlTestResultRef

- **UUID**: `ECUC:875582b1-4980-463c-a9f2-b1f9b1b2e00a`
- **引用名**: `FrDemCtrlTestResultRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `DemEventParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemConfigSet/DemEventParameter`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to DEM event Id that is reported for FlexRay

##### 6. FrFifo

**容器属性**:

- **UUID**: `ECUC:8cef4957-b4d3-49e6-a231-b775f3644c93`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FrFifo`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

One First In First Out (FIFO) queued receive structure, defining the admittance criteria to the FIFO, and mandating the ability to admit messages into the FIFO based on Message Id filtering criteria.

###### 参数配置

此容器包含 **7** 个参数：

####### INTEGER 类型参数

######## 1. FrBaseCycle

- **UUID**: `ECUC:318f7ec1-ad27-45b9-91b7-720d884775d3`
- **参数名**: `FrBaseCycle`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..63]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: FIFO cycle counter acceptance criteria.

######## 2. FrCycleRepetition

- **UUID**: `ECUC:454b7138-41d8-4c73-94ec-a6552230728f`
- **参数名**: `FrCycleRepetition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..64]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: FIFO cylce counter acceptance criteria. Valid values are  1,2,4,5,8,10,16,20,32,40,50,64.

######## 3. FrFifoDepth

- **UUID**: `ECUC:a3d62a6e-c11e-48b7-be8e-16b4a996ae36`
- **参数名**: `FrFifoDepth`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..2048]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Fifo Depth.

######## 4. FrMsgIdMask

- **UUID**: `ECUC:fe24e9f9-ac78-4890-8ae7-8f612d08af57`
- **参数名**: `FrMsgIdMask`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: FIFO message identifier acceptance criteria (Mask filter).

######## 5. FrMsgIdMatch

- **UUID**: `ECUC:31e96e81-1722-4483-a674-8c1ac007e9b9`
- **参数名**: `FrMsgIdMatch`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: FIFO message identifier acceptance criteria (Match filter).

####### BOOLEAN 类型参数

######## 1. FrAdmitWithoutMessageId

- **UUID**: `ECUC:26ee1fad-7fb9-490f-a2d0-54e10ba61e1d`
- **参数名**: `FrAdmitWithoutMessageId`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Determines whether or not frames received in the dynamic segment that don't contain a message ID will be admitted into the FIFO.

####### ENUMERATION 类型参数

######## 1. FrChannels

- **UUID**: `ECUC:ed2ae862-5f03-4f1d-bbd7-453c14c506c0`
- **参数名**: `FrChannels`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `FR_CHANNEL_A` (来源: AUTOSAR_ECUC)
  - `FR_CHANNEL_AB` (来源: AUTOSAR_ECUC)
  - `FR_CHANNEL_B` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: FIFO channel admittance criteria.

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. FrRange

**容器属性**:

- **UUID**: `ECUC:f989ae03-b776-4ea2-a8d3-f2d0b872350f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FrRange`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

FIFO Frame Id range acceptance criteria.

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. FrRangeMax

- **UUID**: `ECUC:7217fbcd-ccbf-4958-a5ca-12d7c84c9410`
- **参数名**: `FrRangeMax`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..2047]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Last FrameId of this range that will be accepted by the FIFO.

########## 2. FrRangeMin

- **UUID**: `ECUC:1ea0cf4e-710f-4137-9df4-ce3975680ede`
- **参数名**: `FrRangeMin`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..2047]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: First FrameId of this range that will be accepted by the FIFO.

##### 7. FrRange

**容器属性**:

- **UUID**: `ECUC:f989ae03-b776-4ea2-a8d3-f2d0b872350f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FrRange`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

FIFO Frame Id range acceptance criteria.

###### 参数配置

此容器包含 **2** 个参数：

####### INTEGER 类型参数

######## 1. FrRangeMax

- **UUID**: `ECUC:7217fbcd-ccbf-4958-a5ca-12d7c84c9410`
- **参数名**: `FrRangeMax`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..2047]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Last FrameId of this range that will be accepted by the FIFO.

######## 2. FrRangeMin

- **UUID**: `ECUC:1ea0cf4e-710f-4137-9df4-ce3975680ede`
- **参数名**: `FrRangeMin`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..2047]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: First FrameId of this range that will be accepted by the FIFO.

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

1. **Fr**
