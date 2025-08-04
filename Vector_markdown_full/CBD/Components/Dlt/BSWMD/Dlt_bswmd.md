# Dlt - 完整配置文档

*此文档由ARXML文件自动生成，采用层次化结构展示*

**生成时间**: 2025-06-16 14:44:49

## 📑 目录

- [📄 文件信息](#-文件信息)
- [🔧 模块定义](#-模块定义)
  - [Dlt](#dlt)
- [📦 包结构](#-包结构)
- [⚡ 实现信息](#-实现信息)
- [⚙️ 配置信息](#️-配置信息)

## 📄 文件信息

### Schema信息
- **Schema位置**: `http://autosar.org/schema/r4.0 AUTOSAR_00044.xsd`
- **命名空间**: `http://autosar.org/schema/r4.0`

## 🔧 模块定义

### 1. Dlt

#### 基本信息

- **UUID**: `f9701d49-2d44-4c5c-a9fe-4f7f73750bae`
- **模块名称**: `Dlt`
- **类别**: `VENDOR_SPECIFIC_MODULE_DEFINITION`
- **多重性**: [0..1]
- **支持的变体**:
  - VARIANT-LINK-TIME
  - VARIANT-PRE-COMPILE

#### 模块描述

"Diagnostic Log and Trace.
DLT receives log information from DET, DEM, SW-Cs, or trace information of the RTE. The DLT module transmits this data either via communication busses or via XCP to make this information visible outside the ECU.
#AMD #Xcp #CANoe #CANape #Monitoring #Logging
#AUTOSAR #ServiceComponent"

#### 版本历史

共有 **20** 个版本记录：

##### 1. 版本 1.0.0

- **发布日期**: 2011-11-09
- **发布者**: AUTOSAR

**变更内容**:

##### 2. 版本 1.0.1

- **发布日期**: 2015-02-25T11:32:07+01:00
- **发布者**: viszda

**变更内容**:

##### 3. 版本 1.0.2

- **发布日期**: 2015-07-06T01:15:19+02:00
- **发布者**: viszda

**变更内容**:

##### 4. 版本 1.0.3

- **发布日期**: 2016-11-18T01:19:27+01:00
- **发布者**: viszda

**变更内容**:

##### 5. 版本 1.0.4

- **发布日期**: 2017-09-14T11:35:02+02:00
- **发布者**: viszda

**变更内容**:

##### 6. 版本 2.0.0

- **发布日期**: 2018-10-31T11:22:39+01:00
- **发布者**: viszda

**变更内容**:

##### 7. 版本 2.1.0

- **发布日期**: 2019-01-29T08:38:06+01:00
- **发布者**: viszda

**变更内容**:

##### 8. 版本 3.0.0

- **发布日期**: 2020-02-25T13:08:10+01:00
- **发布者**: viszda

**变更内容**:

##### 9. 版本 3.1.0

- **发布日期**: 2020-04-16T09:01:03+02:00
- **发布者**: viszda

**变更内容**:

##### 10. 版本 3.2.0

- **发布日期**: 2020-06-18T07:02:01+02:00
- **发布者**: viszda

**变更内容**:

##### 11. 版本 3.3.0

- **发布日期**: 2020-06-23T05:57:34+02:00
- **发布者**: viszda

**变更内容**:

##### 12. 版本 3.4.0

- **发布日期**: 2020-08-05T07:46:58+02:00
- **发布者**: viszda

**变更内容**:

##### 13. 版本 4.0.0

- **发布日期**: 2020-11-25T07:12:39+01:00
- **发布者**: viszda

**变更内容**:

##### 14. 版本 4.0.1

- **发布日期**: 2021-01-21T12:27:52+01:00
- **发布者**: viszda

**变更内容**:

##### 15. 版本 5.0.0

- **发布日期**: 2022-05-28T12:00:12+02:00
- **发布者**: viszda

**变更内容**:

##### 16. 版本 5.1.0

- **发布日期**: 2022-08-23T09:24:32+02:00
- **发布者**: visore

**变更内容**:

##### 17. 版本 6.0.0

- **发布日期**: 2022-12-20T10:39:11+01:00
- **发布者**: viszda

**变更内容**:

##### 18. 版本 7.0.0

- **发布日期**: 2023-03-16T12:04:50+02:00
- **发布者**: viszda

**变更内容**:

##### 19. 版本 7.0.1

- **发布日期**: 2023-10-12T12:05:08+02:00
- **发布者**: vismjv

**变更内容**:

##### 20. 版本 7.1.0

- **发布日期**: 2023-12-09T07:49:32+01:00
- **发布者**: viszda

**变更内容**:

#### 配置容器

本模块包含 **18** 个配置容器：

##### 1. DltConfigSet

**容器属性**:

- **UUID**: `f33c7e43-5c48-474a-b6b6-7782719a4288`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DltConfigSet`
- **多重性**: [1..1]
- **需要索引**: false

**容器描述**:

This container lists all the global Dlt functionalities that can be enabled or disabled at pre-compile time to optimize resource consumption.

###### 配置容器

本模块包含 **13** 个配置容器：

####### 1. DltLogLevelSetting

**容器属性**:

- **UUID**: `ed3fb8ee-35eb-486a-a8ef-f72ff33019aa`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DltLogLevelSetting`
- **多重性**: [1..1]
- **需要索引**: false

**容器描述**:

Contains settings for thresholds.

######## 参数配置

此容器包含 **1** 个参数：

######### ENUMERATION 类型参数

########## 1. DltDefaultLogLevel

- **UUID**: `9d4348db-ac86-4903-ad5d-378ec7239390`
- **参数名**: `DltDefaultLogLevel`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `DLT_LOG_WARN`
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `DLT_LOG_DEBUG` (来源: AUTOSAR_ECUC)
  - `DLT_LOG_ERROR` (来源: AUTOSAR_ECUC)
  - `DLT_LOG_FATAL` (来源: AUTOSAR_ECUC)
  - `DLT_LOG_INFO` (来源: AUTOSAR_ECUC)
  - `DLT_LOG_OFF` (来源: AUTOSAR_ECUC)
  - `DLT_LOG_VERBOSE` (来源: AUTOSAR_ECUC)
  - `DLT_LOG_WARN` (来源: AUTOSAR_ECUC)
- **描述**: This is the effective log level used in case no filter matches the given AppicationId and ContextId. This can be seen as a fall-through filter definition with wildcard for AppicationId and ContextId, which will be used, when no other filter matches.

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. DltLogLevelThreshold

**容器属性**:

- **UUID**: `773796b5-87e2-49d9-b43c-7b46a7342e94`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DltLogLevelThreshold`
- **多重性**: [0..infinite]
- **需要索引**: false

**容器描述**:

Contains settings for thresholds.

########## 参数配置

此容器包含 **1** 个参数：

########### ENUMERATION 类型参数

############ 1. DltThreshold

- **UUID**: `c7526f3a-26d9-415b-b858-d478a417ecfa`
- **参数名**: `DltThreshold`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `DLT_LOG_WARN`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `DLT_LOG_OFF` (来源: AUTOSAR_ECUC)
  - `DLT_LOG_FATAL` (来源: AUTOSAR_ECUC)
  - `DLT_LOG_ERROR` (来源: AUTOSAR_ECUC)
  - `DLT_LOG_WARN` (来源: AUTOSAR_ECUC)
  - `DLT_LOG_INFO` (来源: AUTOSAR_ECUC)
  - `DLT_LOG_DEBUG` (来源: AUTOSAR_ECUC)
  - `DLT_LOG_VERBOSE` (来源: AUTOSAR_ECUC)
- **描述**: The actual threshold.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. DltLogLevelThresholdSwcContextRef

- **UUID**: `052e4c1b-2f24-4eb7-b2e2-0c45cb34c0e3`
- **引用名**: `DltLogLevelThresholdSwcContextRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `DltSwcContext`
- **完整路径**: `/MICROSAR/Dlt/DltSwc/DltSwcContext`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **需要索引**: false
- **描述**: Reference to the SWC context.

####### 2. DltLogLevelThreshold

**容器属性**:

- **UUID**: `773796b5-87e2-49d9-b43c-7b46a7342e94`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DltLogLevelThreshold`
- **多重性**: [0..infinite]
- **需要索引**: false

**容器描述**:

Contains settings for thresholds.

######## 参数配置

此容器包含 **1** 个参数：

######### ENUMERATION 类型参数

########## 1. DltThreshold

- **UUID**: `c7526f3a-26d9-415b-b858-d478a417ecfa`
- **参数名**: `DltThreshold`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `DLT_LOG_WARN`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `DLT_LOG_OFF` (来源: AUTOSAR_ECUC)
  - `DLT_LOG_FATAL` (来源: AUTOSAR_ECUC)
  - `DLT_LOG_ERROR` (来源: AUTOSAR_ECUC)
  - `DLT_LOG_WARN` (来源: AUTOSAR_ECUC)
  - `DLT_LOG_INFO` (来源: AUTOSAR_ECUC)
  - `DLT_LOG_DEBUG` (来源: AUTOSAR_ECUC)
  - `DLT_LOG_VERBOSE` (来源: AUTOSAR_ECUC)
- **描述**: The actual threshold.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. DltLogLevelThresholdSwcContextRef

- **UUID**: `052e4c1b-2f24-4eb7-b2e2-0c45cb34c0e3`
- **引用名**: `DltLogLevelThresholdSwcContextRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `DltSwcContext`
- **完整路径**: `/MICROSAR/Dlt/DltSwc/DltSwcContext`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **需要索引**: false
- **描述**: Reference to the SWC context.

####### 3. DltLogOutput

**容器属性**:

- **UUID**: `900dc29a-8db2-4e85-bcdf-33760d131042`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DltLogOutput`
- **多重性**: [1..1]
- **需要索引**: false

**容器描述**:

Contains settings for log/trace message output

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. DltDefaultLogChannelRef

- **UUID**: `dabe39a5-021e-4070-8554-c4027d946d86`
- **引用名**: `DltDefaultLogChannelRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `DltLogChannel`
- **完整路径**: `/MICROSAR/Dlt/DltConfigSet/DltLogOutput/DltLogChannel`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to the default log channel, which has to be used for a log/trace output, if no other match has been found.

######## 配置容器

本模块包含 **3** 个配置容器：

######### 1. DltLogChannel

**容器属性**:

- **UUID**: `6b2f396e-74c8-43c3-9eb1-432409464b57`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DltLogChannel`
- **多重性**: [1..infinite]
- **需要索引**: false

**容器描述**:

Contains settings for log/trace message output

########## 参数配置

此容器包含 **11** 个参数：

########### INTEGER 类型参数

############ 1. DltLogChannelBufferSize

- **UUID**: `a1ddcd92-81cd-457d-9a24-0c0ad83c2f9c`
- **参数名**: `DltLogChannelBufferSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `1024`
- **取值范围**: [0..4294967295]
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Buffer size in bytes for the LogChannel specific message buffer.

############ 2. DltLogChannelMaxMessageLength

- **UUID**: `6d03f244-a388-45a1-bdf1-b05d97069016`
- **参数名**: `DltLogChannelMaxMessageLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `256`
- **取值范围**: [8..65535]
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: The maximum length of a Dlt log or trace message.

############ 3. DltLogChannelMaxNumOfRetries

- **UUID**: `7c77507b-c4df-443b-89f6-25007e5dd0e3`
- **参数名**: `DltLogChannelMaxNumOfRetries`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..255]
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: The maximum length of a Dlt log or trace message.
This parameter is not supported!

############ 4. DltLogChannelTrafficShapingBandwidth

- **UUID**: `1b827c75-a10b-463f-8489-b34bde061ebe`
- **参数名**: `DltLogChannelTrafficShapingBandwidth`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `4294967295`
- **取值范围**: [0..18446744073709551615]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Set the maximum possible bandwith in bit/s.

Notes:
1. This value is re-calculated to bytes/MainFunction to support the leaky bucket method.
Example:
 - MainFunction cycle is 10ms, so the configured value is divided by 8 (bit/8 = byte) and by 100 (MainFunction cycle = 10ms = 0.01s)
 - If 1024 bytes shall be transmittable per MainFunction cycle:
    - 1024[byte]*8*100[1/s] = 819200[bit/s]

2. If the traffic shaping value is not used completely in a MainFunction cycle, the unused bytes are not usable in the next MainFunction cycle. So, in each MainFunction cycle only the configured TrafficShaping value is available for transmission.

########### BOOLEAN 类型参数

############ 1. DltLogTraceStatusFlag

- **UUID**: `506f54c9-7e65-467b-8200-f64abfd67aba`
- **参数名**: `DltLogTraceStatusFlag`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Parameter to turn on/off on this LogChannel completely.

############ 2. DltLogChannelInitialDebugEvent

- **UUID**: `936ce63d-6374-4034-bddd-c63e73fb468d`
- **参数名**: `DltLogChannelInitialDebugEvent`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: This parameter is only relevant if DltLogChannelDebugMode is set to OnEvent_FirstIsBest!

Defines if log and trace messages shall be gathered before initialization.
This simulates a call of port "TriggerLogChannelDebugEvent" before initialization, as this port is only available after initialization.

########### FLOAT 类型参数

############ 1. DltLogChannelBufferOverflowTimer

- **UUID**: `cb5400c0-3fb9-4f6a-a14e-49571b3633fb`
- **参数名**: `DltLogChannelBufferOverflowTimer`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `0.1`
- **取值范围**: [0.001..1]
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Specifies the cycle time in seconds for resetting the buffer overflow flag in case a buffer overflow occurred.

############ 2. DltLogChannelTransmitCycle

- **UUID**: `c5202ec9-4acc-4016-8472-f117dc95a48a`
- **参数名**: `DltLogChannelTransmitCycle`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `0.01`
- **取值范围**: [0.001..1]
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Specifies the cycle time in seconds of the transmit functionality of this log channel.
This parameter is not supported!

########### STRING 类型参数

############ 1. DltLogChannelId

- **UUID**: `8597b361-4a97-4225-8e1f-3be0f370b04b`
- **参数名**: `DltLogChannelId`
- **数据类型**: STRING
- **多重性**: [1..1]
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **字符串变体**:
  - 默认值: `LCI0`
- **描述**: This is the 4 ASCII character long name of the log channel as used in the Dlt control messages as parameter name Dlt_interface

########### ENUMERATION 类型参数

############ 1. DltLogChannelThreshold

- **UUID**: `eb039867-026b-415a-89a4-abee7d281533`
- **参数名**: `DltLogChannelThreshold`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `DLT_LOG_WARN`
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `DLT_LOG_DEBUG` (来源: AUTOSAR_ECUC)
  - `DLT_LOG_ERROR` (来源: AUTOSAR_ECUC)
  - `DLT_LOG_FATAL` (来源: AUTOSAR_ECUC)
  - `DLT_LOG_INFO` (来源: AUTOSAR_ECUC)
  - `DLT_LOG_OFF` (来源: AUTOSAR_ECUC)
  - `DLT_LOG_VERBOSE` (来源: AUTOSAR_ECUC)
  - `DLT_LOG_WARN` (来源: AUTOSAR_ECUC)
- **描述**: LogLevel Threshold

############ 2. DltLogChannelDebugMode

- **UUID**: `d5b4d638-f3ec-4c0e-ad79-e8e8546cba54`
- **参数名**: `DltLogChannelDebugMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `Continuous_FirstIsBest`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `Continuous_FirstIsBest` (来源: Vector Informatik)
  - `OnEvent_FirstIsBest` (来源: Vector Informatik)
- **描述**: Specifies the debug mode of the log channel.
The debug mode can be changed during runtime via Dlt_SetDebugMode() and be requested during runtime via Dlt_GetDebugMode().
This parameter decides when buffering of Dlt log and trace messages happens and when sending happens.

The debug modes:
1. Continuous_FirstIsBest:
  - Buffering and sending is continuous.
  - When buffer is overflown, new log and trace messages are rejected.
2. OnEvent_FirstIsBest:
  - Buffering starts on event.
  - When buffer is overflown, buffering is stopped and sending is performed until buffer is empty.
  - The event can be triggered during runtime via Dlt_TriggerDebugEvent().

########## 配置容器

本模块包含 **1** 个配置容器：

########### 1. DltTxPdu

**容器属性**:

- **UUID**: `8529b383-9fcb-438a-a6c7-8b53ef7560d1`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DltTxPdu`
- **多重性**: [0..1]
- **需要索引**: false

**容器描述**:

Contains the configuration parameters of the AUTOSAR Dlt module's Tx Pdus.

############ 参数配置

此容器包含 **2** 个参数：

############# INTEGER 类型参数

############## 1. DltITxPduHandleId

- **UUID**: `721a15e6-dcd4-487d-8893-e11f136a22fd`
- **参数名**: `DltITxPduHandleId`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **需要索引**: false
- **描述**: The numerical value used as the ID of this I-PDU.

############# BOOLEAN 类型参数

############## 1. DltITxPduUsesTp

- **UUID**: `04267823-78c2-484c-a0a4-741024bb1b09`
- **参数名**: `DltITxPduUsesTp`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: If set to TRUE, the PDU is transmitted using the TP API. If FALSE, the IF API is used.

############ 引用关系

此容器包含 **1** 个引用：

############# REFERENCE 类型引用

############## 1. DltTxPduIdRef

- **UUID**: `8548c1f7-bcd4-431f-a2b7-db4d1f780941`
- **引用名**: `DltTxPduIdRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to the "global" Pdu structure to allow harmonization of handle IDs in the COM-Stack.

######### 2. DltTxPdu

**容器属性**:

- **UUID**: `8529b383-9fcb-438a-a6c7-8b53ef7560d1`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DltTxPdu`
- **多重性**: [0..1]
- **需要索引**: false

**容器描述**:

Contains the configuration parameters of the AUTOSAR Dlt module's Tx Pdus.

########## 参数配置

此容器包含 **2** 个参数：

########### INTEGER 类型参数

############ 1. DltITxPduHandleId

- **UUID**: `721a15e6-dcd4-487d-8893-e11f136a22fd`
- **参数名**: `DltITxPduHandleId`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **需要索引**: false
- **描述**: The numerical value used as the ID of this I-PDU.

########### BOOLEAN 类型参数

############ 1. DltITxPduUsesTp

- **UUID**: `04267823-78c2-484c-a0a4-741024bb1b09`
- **参数名**: `DltITxPduUsesTp`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: If set to TRUE, the PDU is transmitted using the TP API. If FALSE, the IF API is used.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. DltTxPduIdRef

- **UUID**: `8548c1f7-bcd4-431f-a2b7-db4d1f780941`
- **引用名**: `DltTxPduIdRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to the "global" Pdu structure to allow harmonization of handle IDs in the COM-Stack.

######### 3. DltLogChannelAssignment

**容器属性**:

- **UUID**: `2762e466-1cb6-4393-8aac-6eed8c9b076a`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DltLogChannelAssignment`
- **多重性**: [0..infinite]
- **需要索引**: false

**容器描述**:

This container contains a preconfiguration of ApplicationId / ContextId pairs and their assigned log channel.

########## 引用关系

此容器包含 **2** 个引用：

########### REFERENCE 类型引用

############ 1. DltLogChannelAssignmentSwcContextRef

- **UUID**: `2d832b05-e0d7-494b-890d-b420942072dc`
- **引用名**: `DltLogChannelAssignmentSwcContextRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `DltSwcContext`
- **完整路径**: `/MICROSAR/Dlt/DltSwc/DltSwcContext`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to an ApplicationId/ContextId pair that is assigned to a DltLogChannel.

############ 2. DltLogChannelRef

- **UUID**: `364d993a-728a-4f59-a3c6-74409f719467`
- **引用名**: `DltLogChannelRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `DltLogChannel`
- **完整路径**: `/MICROSAR/Dlt/DltConfigSet/DltLogOutput/DltLogChannel`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to a DltLogChannel that is assigned to an ApplicationId / ContextId pair.

####### 4. DltLogChannel

**容器属性**:

- **UUID**: `6b2f396e-74c8-43c3-9eb1-432409464b57`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DltLogChannel`
- **多重性**: [1..infinite]
- **需要索引**: false

**容器描述**:

Contains settings for log/trace message output

######## 参数配置

此容器包含 **11** 个参数：

######### INTEGER 类型参数

########## 1. DltLogChannelBufferSize

- **UUID**: `a1ddcd92-81cd-457d-9a24-0c0ad83c2f9c`
- **参数名**: `DltLogChannelBufferSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `1024`
- **取值范围**: [0..4294967295]
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Buffer size in bytes for the LogChannel specific message buffer.

########## 2. DltLogChannelMaxMessageLength

- **UUID**: `6d03f244-a388-45a1-bdf1-b05d97069016`
- **参数名**: `DltLogChannelMaxMessageLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `256`
- **取值范围**: [8..65535]
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: The maximum length of a Dlt log or trace message.

########## 3. DltLogChannelMaxNumOfRetries

- **UUID**: `7c77507b-c4df-443b-89f6-25007e5dd0e3`
- **参数名**: `DltLogChannelMaxNumOfRetries`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..255]
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: The maximum length of a Dlt log or trace message.
This parameter is not supported!

########## 4. DltLogChannelTrafficShapingBandwidth

- **UUID**: `1b827c75-a10b-463f-8489-b34bde061ebe`
- **参数名**: `DltLogChannelTrafficShapingBandwidth`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `4294967295`
- **取值范围**: [0..18446744073709551615]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Set the maximum possible bandwith in bit/s.

Notes:
1. This value is re-calculated to bytes/MainFunction to support the leaky bucket method.
Example:
 - MainFunction cycle is 10ms, so the configured value is divided by 8 (bit/8 = byte) and by 100 (MainFunction cycle = 10ms = 0.01s)
 - If 1024 bytes shall be transmittable per MainFunction cycle:
    - 1024[byte]*8*100[1/s] = 819200[bit/s]

2. If the traffic shaping value is not used completely in a MainFunction cycle, the unused bytes are not usable in the next MainFunction cycle. So, in each MainFunction cycle only the configured TrafficShaping value is available for transmission.

######### BOOLEAN 类型参数

########## 1. DltLogTraceStatusFlag

- **UUID**: `506f54c9-7e65-467b-8200-f64abfd67aba`
- **参数名**: `DltLogTraceStatusFlag`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Parameter to turn on/off on this LogChannel completely.

########## 2. DltLogChannelInitialDebugEvent

- **UUID**: `936ce63d-6374-4034-bddd-c63e73fb468d`
- **参数名**: `DltLogChannelInitialDebugEvent`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: This parameter is only relevant if DltLogChannelDebugMode is set to OnEvent_FirstIsBest!

Defines if log and trace messages shall be gathered before initialization.
This simulates a call of port "TriggerLogChannelDebugEvent" before initialization, as this port is only available after initialization.

######### FLOAT 类型参数

########## 1. DltLogChannelBufferOverflowTimer

- **UUID**: `cb5400c0-3fb9-4f6a-a14e-49571b3633fb`
- **参数名**: `DltLogChannelBufferOverflowTimer`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `0.1`
- **取值范围**: [0.001..1]
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Specifies the cycle time in seconds for resetting the buffer overflow flag in case a buffer overflow occurred.

########## 2. DltLogChannelTransmitCycle

- **UUID**: `c5202ec9-4acc-4016-8472-f117dc95a48a`
- **参数名**: `DltLogChannelTransmitCycle`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `0.01`
- **取值范围**: [0.001..1]
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Specifies the cycle time in seconds of the transmit functionality of this log channel.
This parameter is not supported!

######### STRING 类型参数

########## 1. DltLogChannelId

- **UUID**: `8597b361-4a97-4225-8e1f-3be0f370b04b`
- **参数名**: `DltLogChannelId`
- **数据类型**: STRING
- **多重性**: [1..1]
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **字符串变体**:
  - 默认值: `LCI0`
- **描述**: This is the 4 ASCII character long name of the log channel as used in the Dlt control messages as parameter name Dlt_interface

######### ENUMERATION 类型参数

########## 1. DltLogChannelThreshold

- **UUID**: `eb039867-026b-415a-89a4-abee7d281533`
- **参数名**: `DltLogChannelThreshold`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `DLT_LOG_WARN`
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `DLT_LOG_DEBUG` (来源: AUTOSAR_ECUC)
  - `DLT_LOG_ERROR` (来源: AUTOSAR_ECUC)
  - `DLT_LOG_FATAL` (来源: AUTOSAR_ECUC)
  - `DLT_LOG_INFO` (来源: AUTOSAR_ECUC)
  - `DLT_LOG_OFF` (来源: AUTOSAR_ECUC)
  - `DLT_LOG_VERBOSE` (来源: AUTOSAR_ECUC)
  - `DLT_LOG_WARN` (来源: AUTOSAR_ECUC)
- **描述**: LogLevel Threshold

########## 2. DltLogChannelDebugMode

- **UUID**: `d5b4d638-f3ec-4c0e-ad79-e8e8546cba54`
- **参数名**: `DltLogChannelDebugMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `Continuous_FirstIsBest`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `Continuous_FirstIsBest` (来源: Vector Informatik)
  - `OnEvent_FirstIsBest` (来源: Vector Informatik)
- **描述**: Specifies the debug mode of the log channel.
The debug mode can be changed during runtime via Dlt_SetDebugMode() and be requested during runtime via Dlt_GetDebugMode().
This parameter decides when buffering of Dlt log and trace messages happens and when sending happens.

The debug modes:
1. Continuous_FirstIsBest:
  - Buffering and sending is continuous.
  - When buffer is overflown, new log and trace messages are rejected.
2. OnEvent_FirstIsBest:
  - Buffering starts on event.
  - When buffer is overflown, buffering is stopped and sending is performed until buffer is empty.
  - The event can be triggered during runtime via Dlt_TriggerDebugEvent().

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. DltTxPdu

**容器属性**:

- **UUID**: `8529b383-9fcb-438a-a6c7-8b53ef7560d1`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DltTxPdu`
- **多重性**: [0..1]
- **需要索引**: false

**容器描述**:

Contains the configuration parameters of the AUTOSAR Dlt module's Tx Pdus.

########## 参数配置

此容器包含 **2** 个参数：

########### INTEGER 类型参数

############ 1. DltITxPduHandleId

- **UUID**: `721a15e6-dcd4-487d-8893-e11f136a22fd`
- **参数名**: `DltITxPduHandleId`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **需要索引**: false
- **描述**: The numerical value used as the ID of this I-PDU.

########### BOOLEAN 类型参数

############ 1. DltITxPduUsesTp

- **UUID**: `04267823-78c2-484c-a0a4-741024bb1b09`
- **参数名**: `DltITxPduUsesTp`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: If set to TRUE, the PDU is transmitted using the TP API. If FALSE, the IF API is used.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. DltTxPduIdRef

- **UUID**: `8548c1f7-bcd4-431f-a2b7-db4d1f780941`
- **引用名**: `DltTxPduIdRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to the "global" Pdu structure to allow harmonization of handle IDs in the COM-Stack.

####### 5. DltTxPdu

**容器属性**:

- **UUID**: `8529b383-9fcb-438a-a6c7-8b53ef7560d1`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DltTxPdu`
- **多重性**: [0..1]
- **需要索引**: false

**容器描述**:

Contains the configuration parameters of the AUTOSAR Dlt module's Tx Pdus.

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. DltITxPduHandleId

- **UUID**: `721a15e6-dcd4-487d-8893-e11f136a22fd`
- **参数名**: `DltITxPduHandleId`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **需要索引**: false
- **描述**: The numerical value used as the ID of this I-PDU.

######### BOOLEAN 类型参数

########## 1. DltITxPduUsesTp

- **UUID**: `04267823-78c2-484c-a0a4-741024bb1b09`
- **参数名**: `DltITxPduUsesTp`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: If set to TRUE, the PDU is transmitted using the TP API. If FALSE, the IF API is used.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. DltTxPduIdRef

- **UUID**: `8548c1f7-bcd4-431f-a2b7-db4d1f780941`
- **引用名**: `DltTxPduIdRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to the "global" Pdu structure to allow harmonization of handle IDs in the COM-Stack.

####### 6. DltLogChannelAssignment

**容器属性**:

- **UUID**: `2762e466-1cb6-4393-8aac-6eed8c9b076a`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DltLogChannelAssignment`
- **多重性**: [0..infinite]
- **需要索引**: false

**容器描述**:

This container contains a preconfiguration of ApplicationId / ContextId pairs and their assigned log channel.

######## 引用关系

此容器包含 **2** 个引用：

######### REFERENCE 类型引用

########## 1. DltLogChannelAssignmentSwcContextRef

- **UUID**: `2d832b05-e0d7-494b-890d-b420942072dc`
- **引用名**: `DltLogChannelAssignmentSwcContextRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `DltSwcContext`
- **完整路径**: `/MICROSAR/Dlt/DltSwc/DltSwcContext`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to an ApplicationId/ContextId pair that is assigned to a DltLogChannel.

########## 2. DltLogChannelRef

- **UUID**: `364d993a-728a-4f59-a3c6-74409f719467`
- **引用名**: `DltLogChannelRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `DltLogChannel`
- **完整路径**: `/MICROSAR/Dlt/DltConfigSet/DltLogOutput/DltLogChannel`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to a DltLogChannel that is assigned to an ApplicationId / ContextId pair.

####### 7. DltProtocol

**容器属性**:

- **UUID**: `bc91adb5-cfa6-4c0d-8b99-a77a5dfba574`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DltProtocol`
- **多重性**: [1..1]
- **需要索引**: false

**容器描述**:

Configuration parameters for handling the specific protocol variants.

######## 参数配置

此容器包含 **5** 个参数：

######### BOOLEAN 类型参数

########## 1. DltHeaderUseEcuId

- **UUID**: `213f5834-08e9-405f-adf6-efab72e70704`
- **参数名**: `DltHeaderUseEcuId`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Corresponds to field WEID (With ECU ID). If set ECU ID shall be placed in the header, else not.

########## 2. DltHeaderUseSessionID

- **UUID**: `dcf4be5b-cd1e-4e51-921c-33d94c0b6444`
- **参数名**: `DltHeaderUseSessionID`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Corresponds to field WSID (with Session ID). If set the Session ID shall be placed in the header, else not.

########## 3. DltHeaderUseTimestamp

- **UUID**: `94e76c83-967c-419b-acd0-df12ec6a6300`
- **参数名**: `DltHeaderUseTimestamp`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Corresponds to field WTMS (With Timestamp). If set the timestamp shall be placed in the header, else not.

########## 4. DltUseExtHeaderInNonVerbMode

- **UUID**: `7d16b1a6-1f86-40fb-86a4-6cfcc2476d5c`
- **参数名**: `DltUseExtHeaderInNonVerbMode`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Non Verbose messages (opposed to verbose messages) do not need an extended header. If this flag is set to true the extended header shall also be used for non verbose messages.

########## 5. DltUseVerboseMode

- **UUID**: `22f70795-eb43-4f12-9147-9ed8ea66a144`
- **参数名**: `DltUseVerboseMode`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: If this flag is set to TRUE, the payload shall be transmitted in verbose mode, else the payload shall be transmitted in none-verbose mode.

######## 配置容器

本模块包含 **3** 个配置容器：

######### 1. DltEcuIdCalloutChoice

**容器属性**:

- **UUID**: `87f90a5c-8b0d-4e43-92c4-c0d9b5a549bc`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DltEcuIdCalloutChoice`
- **多重性**: [0..1]
- **需要索引**: false

**容器描述**:

EcuId via user defined callout.
This choice is not supported!

########## 参数配置

此容器包含 **1** 个参数：

########### FUNCTION-NAME 类型参数

############ 1. DltEcuIdCallout

- **UUID**: `fa6e6aaa-5bb1-4104-9bed-92fe2b4c7b52`
- **参数名**: `DltEcuIdCallout`
- **数据类型**: FUNCTION-NAME
- **多重性**: [1..1]
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **函数变体**:
  - 默认值: `DltAppl_GetEcuId`
- **描述**: If this choice is used the EcuId shall be fetched by calling the here configured callout function.
This parameter is not supported!

######### 2. DltEcuIdValueChoice

**容器属性**:

- **UUID**: `b34157f0-9190-4f73-a88b-6c42642ad4b8`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DltEcuIdValueChoice`
- **多重性**: [0..1]
- **需要索引**: false

**容器描述**:

EcuId value configuration

########## 参数配置

此容器包含 **1** 个参数：

########### STRING 类型参数

############ 1. DltEcuIdValue

- **UUID**: `09aefb92-68f4-4bab-9a25-21e34bf40f36`
- **参数名**: `DltEcuIdValue`
- **数据类型**: STRING
- **多重性**: [1..1]
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **字符串变体**:
  - 默认值: `ECUI`
  - 最大长度: 4
  - 最小长度: 1
- **描述**: If this choice is used the EcuId shall be taken from the configured string.

######### 3. DltEcuId

**容器属性**:

- **UUID**: `92605436-79a4-4864-91bc-09b9d58a385b`
- **容器类型**: CHOICE-CONTAINER
- **容器名称**: `DltEcuId`
- **多重性**: [1..1]
- **需要索引**: false

**容器选择**:

- **DltEcuIdCalloutChoice**
  - UUID: `87f90a5c-8b0d-4e43-92c4-c0d9b5a549bc`
  - 描述: EcuId via user defined callout.
This choice is not supported!
- **DltEcuIdValueChoice**
  - UUID: `b34157f0-9190-4f73-a88b-6c42642ad4b8`
  - 描述: EcuId value configuration

**容器描述**:

This is a choice container to choose between a EcuId value or a callout to get the EcuId.

####### 8. DltEcuIdCalloutChoice

**容器属性**:

- **UUID**: `87f90a5c-8b0d-4e43-92c4-c0d9b5a549bc`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DltEcuIdCalloutChoice`
- **多重性**: [0..1]
- **需要索引**: false

**容器描述**:

EcuId via user defined callout.
This choice is not supported!

######## 参数配置

此容器包含 **1** 个参数：

######### FUNCTION-NAME 类型参数

########## 1. DltEcuIdCallout

- **UUID**: `fa6e6aaa-5bb1-4104-9bed-92fe2b4c7b52`
- **参数名**: `DltEcuIdCallout`
- **数据类型**: FUNCTION-NAME
- **多重性**: [1..1]
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **函数变体**:
  - 默认值: `DltAppl_GetEcuId`
- **描述**: If this choice is used the EcuId shall be fetched by calling the here configured callout function.
This parameter is not supported!

####### 9. DltEcuIdValueChoice

**容器属性**:

- **UUID**: `b34157f0-9190-4f73-a88b-6c42642ad4b8`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DltEcuIdValueChoice`
- **多重性**: [0..1]
- **需要索引**: false

**容器描述**:

EcuId value configuration

######## 参数配置

此容器包含 **1** 个参数：

######### STRING 类型参数

########## 1. DltEcuIdValue

- **UUID**: `09aefb92-68f4-4bab-9a25-21e34bf40f36`
- **参数名**: `DltEcuIdValue`
- **数据类型**: STRING
- **多重性**: [1..1]
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **字符串变体**:
  - 默认值: `ECUI`
  - 最大长度: 4
  - 最小长度: 1
- **描述**: If this choice is used the EcuId shall be taken from the configured string.

####### 10. DltRxPdu

**容器属性**:

- **UUID**: `efdf2e41-b88d-41a5-a5e2-10d79de64f17`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DltRxPdu`
- **多重性**: [0..infinite]
- **需要索引**: false

**容器描述**:

Contains the Pdu IDs to be used for Dlt control messages reception.

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. DltIRxPduHandleId

- **UUID**: `20ffbea7-88fe-4874-9a00-b6f3674df0f2`
- **参数名**: `DltIRxPduHandleId`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **需要索引**: false
- **描述**: The numerical value used as the ID of this I-PDU. The DltRxPduHandleId is required by the API calls Dlt_RxIndication, Dlt_TpRxIndication, Dlt_StartOfReception and Dlt_CopyRxData to receive I-PDUs from the PduR (DltIPduDirection: Receive), as well as the PduId passed to an Rx-I-PDU-callout.

######### BOOLEAN 类型参数

########## 1. DltIRxPduUsesTp

- **UUID**: `81e66fd4-2bad-410e-bd75-403889f09d1f`
- **参数名**: `DltIRxPduUsesTp`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: If set to TRUE, the PDU is received using the TP API. If FALSE, the IF API is used.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. DltRxPduIdRef

- **UUID**: `d36a42c4-b153-4aa0-bf0e-b9192ce66cf7`
- **引用名**: `DltRxPduIdRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to the "global" Pdu structure to allow harmonization of handle IDs in the COM-Stack.

####### 11. DltTraceStatusSetting

**容器属性**:

- **UUID**: `7d8c667f-b54f-4aed-8f9e-9d6e4675a179`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DltTraceStatusSetting`
- **多重性**: [1..1]
- **需要索引**: false

**容器描述**:

Contains settings for trace status

######## 参数配置

此容器包含 **1** 个参数：

######### BOOLEAN 类型参数

########## 1. DltDefaultTraceStatus

- **UUID**: `8a205e2c-605f-427f-a295-e0259dbe9469`
- **参数名**: `DltDefaultTraceStatus`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: This is the effective trace status used in case no filter matches the given ApplicationId and ContextId. This can be seen as a fall-through filter definition with wildcard for ApplicationId and ContextId, which will be used, when no other filter matches.

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. DltTraceStatusAssignment

**容器属性**:

- **UUID**: `e9c3c8ea-af03-4bbc-ab11-8214a0f0a9c0`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DltTraceStatusAssignment`
- **多重性**: [0..infinite]
- **需要索引**: false

**容器描述**:

This container contains a preconfiguration of ApplicationId / ContextId pairs and their assigned trace status.

########## 参数配置

此容器包含 **1** 个参数：

########### BOOLEAN 类型参数

############ 1. DltTraceStatus

- **UUID**: `3aa3c212-9589-4032-99f4-d2336e31ac3a`
- **参数名**: `DltTraceStatus`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Trace status for the given ApplicationId/ContextId tuple.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. DltTraceStatusAssignmentSwcContextRef

- **UUID**: `a71f18c7-30f1-42e7-b686-22bc9eb06ea1`
- **引用名**: `DltTraceStatusAssignmentSwcContextRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `DltSwcContext`
- **完整路径**: `/MICROSAR/Dlt/DltSwc/DltSwcContext`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to an ApplicationId/ContextId pair to which a DltTraceStatus is assigned.

####### 12. DltTraceStatusAssignment

**容器属性**:

- **UUID**: `e9c3c8ea-af03-4bbc-ab11-8214a0f0a9c0`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DltTraceStatusAssignment`
- **多重性**: [0..infinite]
- **需要索引**: false

**容器描述**:

This container contains a preconfiguration of ApplicationId / ContextId pairs and their assigned trace status.

######## 参数配置

此容器包含 **1** 个参数：

######### BOOLEAN 类型参数

########## 1. DltTraceStatus

- **UUID**: `3aa3c212-9589-4032-99f4-d2336e31ac3a`
- **参数名**: `DltTraceStatus`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Trace status for the given ApplicationId/ContextId tuple.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. DltTraceStatusAssignmentSwcContextRef

- **UUID**: `a71f18c7-30f1-42e7-b686-22bc9eb06ea1`
- **引用名**: `DltTraceStatusAssignmentSwcContextRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `DltSwcContext`
- **完整路径**: `/MICROSAR/Dlt/DltSwc/DltSwcContext`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to an ApplicationId/ContextId pair to which a DltTraceStatus is assigned.

####### 13. DltEcuId

**容器属性**:

- **UUID**: `92605436-79a4-4864-91bc-09b9d58a385b`
- **容器类型**: CHOICE-CONTAINER
- **容器名称**: `DltEcuId`
- **多重性**: [1..1]
- **需要索引**: false

**容器选择**:

- **DltEcuIdCalloutChoice**
  - UUID: `87f90a5c-8b0d-4e43-92c4-c0d9b5a549bc`
  - 描述: EcuId via user defined callout.
This choice is not supported!
- **DltEcuIdValueChoice**
  - UUID: `b34157f0-9190-4f73-a88b-6c42642ad4b8`
  - 描述: EcuId value configuration

**容器描述**:

This is a choice container to choose between a EcuId value or a callout to get the EcuId.

##### 2. DltLogLevelSetting

**容器属性**:

- **UUID**: `ed3fb8ee-35eb-486a-a8ef-f72ff33019aa`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DltLogLevelSetting`
- **多重性**: [1..1]
- **需要索引**: false

**容器描述**:

Contains settings for thresholds.

###### 参数配置

此容器包含 **1** 个参数：

####### ENUMERATION 类型参数

######## 1. DltDefaultLogLevel

- **UUID**: `9d4348db-ac86-4903-ad5d-378ec7239390`
- **参数名**: `DltDefaultLogLevel`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `DLT_LOG_WARN`
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `DLT_LOG_DEBUG` (来源: AUTOSAR_ECUC)
  - `DLT_LOG_ERROR` (来源: AUTOSAR_ECUC)
  - `DLT_LOG_FATAL` (来源: AUTOSAR_ECUC)
  - `DLT_LOG_INFO` (来源: AUTOSAR_ECUC)
  - `DLT_LOG_OFF` (来源: AUTOSAR_ECUC)
  - `DLT_LOG_VERBOSE` (来源: AUTOSAR_ECUC)
  - `DLT_LOG_WARN` (来源: AUTOSAR_ECUC)
- **描述**: This is the effective log level used in case no filter matches the given AppicationId and ContextId. This can be seen as a fall-through filter definition with wildcard for AppicationId and ContextId, which will be used, when no other filter matches.

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. DltLogLevelThreshold

**容器属性**:

- **UUID**: `773796b5-87e2-49d9-b43c-7b46a7342e94`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DltLogLevelThreshold`
- **多重性**: [0..infinite]
- **需要索引**: false

**容器描述**:

Contains settings for thresholds.

######## 参数配置

此容器包含 **1** 个参数：

######### ENUMERATION 类型参数

########## 1. DltThreshold

- **UUID**: `c7526f3a-26d9-415b-b858-d478a417ecfa`
- **参数名**: `DltThreshold`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `DLT_LOG_WARN`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `DLT_LOG_OFF` (来源: AUTOSAR_ECUC)
  - `DLT_LOG_FATAL` (来源: AUTOSAR_ECUC)
  - `DLT_LOG_ERROR` (来源: AUTOSAR_ECUC)
  - `DLT_LOG_WARN` (来源: AUTOSAR_ECUC)
  - `DLT_LOG_INFO` (来源: AUTOSAR_ECUC)
  - `DLT_LOG_DEBUG` (来源: AUTOSAR_ECUC)
  - `DLT_LOG_VERBOSE` (来源: AUTOSAR_ECUC)
- **描述**: The actual threshold.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. DltLogLevelThresholdSwcContextRef

- **UUID**: `052e4c1b-2f24-4eb7-b2e2-0c45cb34c0e3`
- **引用名**: `DltLogLevelThresholdSwcContextRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `DltSwcContext`
- **完整路径**: `/MICROSAR/Dlt/DltSwc/DltSwcContext`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **需要索引**: false
- **描述**: Reference to the SWC context.

##### 3. DltLogLevelThreshold

**容器属性**:

- **UUID**: `773796b5-87e2-49d9-b43c-7b46a7342e94`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DltLogLevelThreshold`
- **多重性**: [0..infinite]
- **需要索引**: false

**容器描述**:

Contains settings for thresholds.

###### 参数配置

此容器包含 **1** 个参数：

####### ENUMERATION 类型参数

######## 1. DltThreshold

- **UUID**: `c7526f3a-26d9-415b-b858-d478a417ecfa`
- **参数名**: `DltThreshold`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `DLT_LOG_WARN`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `DLT_LOG_OFF` (来源: AUTOSAR_ECUC)
  - `DLT_LOG_FATAL` (来源: AUTOSAR_ECUC)
  - `DLT_LOG_ERROR` (来源: AUTOSAR_ECUC)
  - `DLT_LOG_WARN` (来源: AUTOSAR_ECUC)
  - `DLT_LOG_INFO` (来源: AUTOSAR_ECUC)
  - `DLT_LOG_DEBUG` (来源: AUTOSAR_ECUC)
  - `DLT_LOG_VERBOSE` (来源: AUTOSAR_ECUC)
- **描述**: The actual threshold.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. DltLogLevelThresholdSwcContextRef

- **UUID**: `052e4c1b-2f24-4eb7-b2e2-0c45cb34c0e3`
- **引用名**: `DltLogLevelThresholdSwcContextRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `DltSwcContext`
- **完整路径**: `/MICROSAR/Dlt/DltSwc/DltSwcContext`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **需要索引**: false
- **描述**: Reference to the SWC context.

##### 4. DltLogOutput

**容器属性**:

- **UUID**: `900dc29a-8db2-4e85-bcdf-33760d131042`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DltLogOutput`
- **多重性**: [1..1]
- **需要索引**: false

**容器描述**:

Contains settings for log/trace message output

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. DltDefaultLogChannelRef

- **UUID**: `dabe39a5-021e-4070-8554-c4027d946d86`
- **引用名**: `DltDefaultLogChannelRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `DltLogChannel`
- **完整路径**: `/MICROSAR/Dlt/DltConfigSet/DltLogOutput/DltLogChannel`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to the default log channel, which has to be used for a log/trace output, if no other match has been found.

###### 配置容器

本模块包含 **3** 个配置容器：

####### 1. DltLogChannel

**容器属性**:

- **UUID**: `6b2f396e-74c8-43c3-9eb1-432409464b57`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DltLogChannel`
- **多重性**: [1..infinite]
- **需要索引**: false

**容器描述**:

Contains settings for log/trace message output

######## 参数配置

此容器包含 **11** 个参数：

######### INTEGER 类型参数

########## 1. DltLogChannelBufferSize

- **UUID**: `a1ddcd92-81cd-457d-9a24-0c0ad83c2f9c`
- **参数名**: `DltLogChannelBufferSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `1024`
- **取值范围**: [0..4294967295]
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Buffer size in bytes for the LogChannel specific message buffer.

########## 2. DltLogChannelMaxMessageLength

- **UUID**: `6d03f244-a388-45a1-bdf1-b05d97069016`
- **参数名**: `DltLogChannelMaxMessageLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `256`
- **取值范围**: [8..65535]
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: The maximum length of a Dlt log or trace message.

########## 3. DltLogChannelMaxNumOfRetries

- **UUID**: `7c77507b-c4df-443b-89f6-25007e5dd0e3`
- **参数名**: `DltLogChannelMaxNumOfRetries`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..255]
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: The maximum length of a Dlt log or trace message.
This parameter is not supported!

########## 4. DltLogChannelTrafficShapingBandwidth

- **UUID**: `1b827c75-a10b-463f-8489-b34bde061ebe`
- **参数名**: `DltLogChannelTrafficShapingBandwidth`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `4294967295`
- **取值范围**: [0..18446744073709551615]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Set the maximum possible bandwith in bit/s.

Notes:
1. This value is re-calculated to bytes/MainFunction to support the leaky bucket method.
Example:
 - MainFunction cycle is 10ms, so the configured value is divided by 8 (bit/8 = byte) and by 100 (MainFunction cycle = 10ms = 0.01s)
 - If 1024 bytes shall be transmittable per MainFunction cycle:
    - 1024[byte]*8*100[1/s] = 819200[bit/s]

2. If the traffic shaping value is not used completely in a MainFunction cycle, the unused bytes are not usable in the next MainFunction cycle. So, in each MainFunction cycle only the configured TrafficShaping value is available for transmission.

######### BOOLEAN 类型参数

########## 1. DltLogTraceStatusFlag

- **UUID**: `506f54c9-7e65-467b-8200-f64abfd67aba`
- **参数名**: `DltLogTraceStatusFlag`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Parameter to turn on/off on this LogChannel completely.

########## 2. DltLogChannelInitialDebugEvent

- **UUID**: `936ce63d-6374-4034-bddd-c63e73fb468d`
- **参数名**: `DltLogChannelInitialDebugEvent`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: This parameter is only relevant if DltLogChannelDebugMode is set to OnEvent_FirstIsBest!

Defines if log and trace messages shall be gathered before initialization.
This simulates a call of port "TriggerLogChannelDebugEvent" before initialization, as this port is only available after initialization.

######### FLOAT 类型参数

########## 1. DltLogChannelBufferOverflowTimer

- **UUID**: `cb5400c0-3fb9-4f6a-a14e-49571b3633fb`
- **参数名**: `DltLogChannelBufferOverflowTimer`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `0.1`
- **取值范围**: [0.001..1]
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Specifies the cycle time in seconds for resetting the buffer overflow flag in case a buffer overflow occurred.

########## 2. DltLogChannelTransmitCycle

- **UUID**: `c5202ec9-4acc-4016-8472-f117dc95a48a`
- **参数名**: `DltLogChannelTransmitCycle`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `0.01`
- **取值范围**: [0.001..1]
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Specifies the cycle time in seconds of the transmit functionality of this log channel.
This parameter is not supported!

######### STRING 类型参数

########## 1. DltLogChannelId

- **UUID**: `8597b361-4a97-4225-8e1f-3be0f370b04b`
- **参数名**: `DltLogChannelId`
- **数据类型**: STRING
- **多重性**: [1..1]
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **字符串变体**:
  - 默认值: `LCI0`
- **描述**: This is the 4 ASCII character long name of the log channel as used in the Dlt control messages as parameter name Dlt_interface

######### ENUMERATION 类型参数

########## 1. DltLogChannelThreshold

- **UUID**: `eb039867-026b-415a-89a4-abee7d281533`
- **参数名**: `DltLogChannelThreshold`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `DLT_LOG_WARN`
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `DLT_LOG_DEBUG` (来源: AUTOSAR_ECUC)
  - `DLT_LOG_ERROR` (来源: AUTOSAR_ECUC)
  - `DLT_LOG_FATAL` (来源: AUTOSAR_ECUC)
  - `DLT_LOG_INFO` (来源: AUTOSAR_ECUC)
  - `DLT_LOG_OFF` (来源: AUTOSAR_ECUC)
  - `DLT_LOG_VERBOSE` (来源: AUTOSAR_ECUC)
  - `DLT_LOG_WARN` (来源: AUTOSAR_ECUC)
- **描述**: LogLevel Threshold

########## 2. DltLogChannelDebugMode

- **UUID**: `d5b4d638-f3ec-4c0e-ad79-e8e8546cba54`
- **参数名**: `DltLogChannelDebugMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `Continuous_FirstIsBest`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `Continuous_FirstIsBest` (来源: Vector Informatik)
  - `OnEvent_FirstIsBest` (来源: Vector Informatik)
- **描述**: Specifies the debug mode of the log channel.
The debug mode can be changed during runtime via Dlt_SetDebugMode() and be requested during runtime via Dlt_GetDebugMode().
This parameter decides when buffering of Dlt log and trace messages happens and when sending happens.

The debug modes:
1. Continuous_FirstIsBest:
  - Buffering and sending is continuous.
  - When buffer is overflown, new log and trace messages are rejected.
2. OnEvent_FirstIsBest:
  - Buffering starts on event.
  - When buffer is overflown, buffering is stopped and sending is performed until buffer is empty.
  - The event can be triggered during runtime via Dlt_TriggerDebugEvent().

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. DltTxPdu

**容器属性**:

- **UUID**: `8529b383-9fcb-438a-a6c7-8b53ef7560d1`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DltTxPdu`
- **多重性**: [0..1]
- **需要索引**: false

**容器描述**:

Contains the configuration parameters of the AUTOSAR Dlt module's Tx Pdus.

########## 参数配置

此容器包含 **2** 个参数：

########### INTEGER 类型参数

############ 1. DltITxPduHandleId

- **UUID**: `721a15e6-dcd4-487d-8893-e11f136a22fd`
- **参数名**: `DltITxPduHandleId`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **需要索引**: false
- **描述**: The numerical value used as the ID of this I-PDU.

########### BOOLEAN 类型参数

############ 1. DltITxPduUsesTp

- **UUID**: `04267823-78c2-484c-a0a4-741024bb1b09`
- **参数名**: `DltITxPduUsesTp`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: If set to TRUE, the PDU is transmitted using the TP API. If FALSE, the IF API is used.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. DltTxPduIdRef

- **UUID**: `8548c1f7-bcd4-431f-a2b7-db4d1f780941`
- **引用名**: `DltTxPduIdRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to the "global" Pdu structure to allow harmonization of handle IDs in the COM-Stack.

####### 2. DltTxPdu

**容器属性**:

- **UUID**: `8529b383-9fcb-438a-a6c7-8b53ef7560d1`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DltTxPdu`
- **多重性**: [0..1]
- **需要索引**: false

**容器描述**:

Contains the configuration parameters of the AUTOSAR Dlt module's Tx Pdus.

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. DltITxPduHandleId

- **UUID**: `721a15e6-dcd4-487d-8893-e11f136a22fd`
- **参数名**: `DltITxPduHandleId`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **需要索引**: false
- **描述**: The numerical value used as the ID of this I-PDU.

######### BOOLEAN 类型参数

########## 1. DltITxPduUsesTp

- **UUID**: `04267823-78c2-484c-a0a4-741024bb1b09`
- **参数名**: `DltITxPduUsesTp`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: If set to TRUE, the PDU is transmitted using the TP API. If FALSE, the IF API is used.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. DltTxPduIdRef

- **UUID**: `8548c1f7-bcd4-431f-a2b7-db4d1f780941`
- **引用名**: `DltTxPduIdRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to the "global" Pdu structure to allow harmonization of handle IDs in the COM-Stack.

####### 3. DltLogChannelAssignment

**容器属性**:

- **UUID**: `2762e466-1cb6-4393-8aac-6eed8c9b076a`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DltLogChannelAssignment`
- **多重性**: [0..infinite]
- **需要索引**: false

**容器描述**:

This container contains a preconfiguration of ApplicationId / ContextId pairs and their assigned log channel.

######## 引用关系

此容器包含 **2** 个引用：

######### REFERENCE 类型引用

########## 1. DltLogChannelAssignmentSwcContextRef

- **UUID**: `2d832b05-e0d7-494b-890d-b420942072dc`
- **引用名**: `DltLogChannelAssignmentSwcContextRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `DltSwcContext`
- **完整路径**: `/MICROSAR/Dlt/DltSwc/DltSwcContext`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to an ApplicationId/ContextId pair that is assigned to a DltLogChannel.

########## 2. DltLogChannelRef

- **UUID**: `364d993a-728a-4f59-a3c6-74409f719467`
- **引用名**: `DltLogChannelRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `DltLogChannel`
- **完整路径**: `/MICROSAR/Dlt/DltConfigSet/DltLogOutput/DltLogChannel`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to a DltLogChannel that is assigned to an ApplicationId / ContextId pair.

##### 5. DltLogChannel

**容器属性**:

- **UUID**: `6b2f396e-74c8-43c3-9eb1-432409464b57`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DltLogChannel`
- **多重性**: [1..infinite]
- **需要索引**: false

**容器描述**:

Contains settings for log/trace message output

###### 参数配置

此容器包含 **11** 个参数：

####### INTEGER 类型参数

######## 1. DltLogChannelBufferSize

- **UUID**: `a1ddcd92-81cd-457d-9a24-0c0ad83c2f9c`
- **参数名**: `DltLogChannelBufferSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `1024`
- **取值范围**: [0..4294967295]
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Buffer size in bytes for the LogChannel specific message buffer.

######## 2. DltLogChannelMaxMessageLength

- **UUID**: `6d03f244-a388-45a1-bdf1-b05d97069016`
- **参数名**: `DltLogChannelMaxMessageLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `256`
- **取值范围**: [8..65535]
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: The maximum length of a Dlt log or trace message.

######## 3. DltLogChannelMaxNumOfRetries

- **UUID**: `7c77507b-c4df-443b-89f6-25007e5dd0e3`
- **参数名**: `DltLogChannelMaxNumOfRetries`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..255]
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: The maximum length of a Dlt log or trace message.
This parameter is not supported!

######## 4. DltLogChannelTrafficShapingBandwidth

- **UUID**: `1b827c75-a10b-463f-8489-b34bde061ebe`
- **参数名**: `DltLogChannelTrafficShapingBandwidth`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `4294967295`
- **取值范围**: [0..18446744073709551615]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Set the maximum possible bandwith in bit/s.

Notes:
1. This value is re-calculated to bytes/MainFunction to support the leaky bucket method.
Example:
 - MainFunction cycle is 10ms, so the configured value is divided by 8 (bit/8 = byte) and by 100 (MainFunction cycle = 10ms = 0.01s)
 - If 1024 bytes shall be transmittable per MainFunction cycle:
    - 1024[byte]*8*100[1/s] = 819200[bit/s]

2. If the traffic shaping value is not used completely in a MainFunction cycle, the unused bytes are not usable in the next MainFunction cycle. So, in each MainFunction cycle only the configured TrafficShaping value is available for transmission.

####### BOOLEAN 类型参数

######## 1. DltLogTraceStatusFlag

- **UUID**: `506f54c9-7e65-467b-8200-f64abfd67aba`
- **参数名**: `DltLogTraceStatusFlag`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Parameter to turn on/off on this LogChannel completely.

######## 2. DltLogChannelInitialDebugEvent

- **UUID**: `936ce63d-6374-4034-bddd-c63e73fb468d`
- **参数名**: `DltLogChannelInitialDebugEvent`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: This parameter is only relevant if DltLogChannelDebugMode is set to OnEvent_FirstIsBest!

Defines if log and trace messages shall be gathered before initialization.
This simulates a call of port "TriggerLogChannelDebugEvent" before initialization, as this port is only available after initialization.

####### FLOAT 类型参数

######## 1. DltLogChannelBufferOverflowTimer

- **UUID**: `cb5400c0-3fb9-4f6a-a14e-49571b3633fb`
- **参数名**: `DltLogChannelBufferOverflowTimer`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `0.1`
- **取值范围**: [0.001..1]
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Specifies the cycle time in seconds for resetting the buffer overflow flag in case a buffer overflow occurred.

######## 2. DltLogChannelTransmitCycle

- **UUID**: `c5202ec9-4acc-4016-8472-f117dc95a48a`
- **参数名**: `DltLogChannelTransmitCycle`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `0.01`
- **取值范围**: [0.001..1]
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Specifies the cycle time in seconds of the transmit functionality of this log channel.
This parameter is not supported!

####### STRING 类型参数

######## 1. DltLogChannelId

- **UUID**: `8597b361-4a97-4225-8e1f-3be0f370b04b`
- **参数名**: `DltLogChannelId`
- **数据类型**: STRING
- **多重性**: [1..1]
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **字符串变体**:
  - 默认值: `LCI0`
- **描述**: This is the 4 ASCII character long name of the log channel as used in the Dlt control messages as parameter name Dlt_interface

####### ENUMERATION 类型参数

######## 1. DltLogChannelThreshold

- **UUID**: `eb039867-026b-415a-89a4-abee7d281533`
- **参数名**: `DltLogChannelThreshold`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `DLT_LOG_WARN`
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `DLT_LOG_DEBUG` (来源: AUTOSAR_ECUC)
  - `DLT_LOG_ERROR` (来源: AUTOSAR_ECUC)
  - `DLT_LOG_FATAL` (来源: AUTOSAR_ECUC)
  - `DLT_LOG_INFO` (来源: AUTOSAR_ECUC)
  - `DLT_LOG_OFF` (来源: AUTOSAR_ECUC)
  - `DLT_LOG_VERBOSE` (来源: AUTOSAR_ECUC)
  - `DLT_LOG_WARN` (来源: AUTOSAR_ECUC)
- **描述**: LogLevel Threshold

######## 2. DltLogChannelDebugMode

- **UUID**: `d5b4d638-f3ec-4c0e-ad79-e8e8546cba54`
- **参数名**: `DltLogChannelDebugMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `Continuous_FirstIsBest`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `Continuous_FirstIsBest` (来源: Vector Informatik)
  - `OnEvent_FirstIsBest` (来源: Vector Informatik)
- **描述**: Specifies the debug mode of the log channel.
The debug mode can be changed during runtime via Dlt_SetDebugMode() and be requested during runtime via Dlt_GetDebugMode().
This parameter decides when buffering of Dlt log and trace messages happens and when sending happens.

The debug modes:
1. Continuous_FirstIsBest:
  - Buffering and sending is continuous.
  - When buffer is overflown, new log and trace messages are rejected.
2. OnEvent_FirstIsBest:
  - Buffering starts on event.
  - When buffer is overflown, buffering is stopped and sending is performed until buffer is empty.
  - The event can be triggered during runtime via Dlt_TriggerDebugEvent().

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. DltTxPdu

**容器属性**:

- **UUID**: `8529b383-9fcb-438a-a6c7-8b53ef7560d1`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DltTxPdu`
- **多重性**: [0..1]
- **需要索引**: false

**容器描述**:

Contains the configuration parameters of the AUTOSAR Dlt module's Tx Pdus.

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. DltITxPduHandleId

- **UUID**: `721a15e6-dcd4-487d-8893-e11f136a22fd`
- **参数名**: `DltITxPduHandleId`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **需要索引**: false
- **描述**: The numerical value used as the ID of this I-PDU.

######### BOOLEAN 类型参数

########## 1. DltITxPduUsesTp

- **UUID**: `04267823-78c2-484c-a0a4-741024bb1b09`
- **参数名**: `DltITxPduUsesTp`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: If set to TRUE, the PDU is transmitted using the TP API. If FALSE, the IF API is used.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. DltTxPduIdRef

- **UUID**: `8548c1f7-bcd4-431f-a2b7-db4d1f780941`
- **引用名**: `DltTxPduIdRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to the "global" Pdu structure to allow harmonization of handle IDs in the COM-Stack.

##### 6. DltTxPdu

**容器属性**:

- **UUID**: `8529b383-9fcb-438a-a6c7-8b53ef7560d1`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DltTxPdu`
- **多重性**: [0..1]
- **需要索引**: false

**容器描述**:

Contains the configuration parameters of the AUTOSAR Dlt module's Tx Pdus.

###### 参数配置

此容器包含 **2** 个参数：

####### INTEGER 类型参数

######## 1. DltITxPduHandleId

- **UUID**: `721a15e6-dcd4-487d-8893-e11f136a22fd`
- **参数名**: `DltITxPduHandleId`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **需要索引**: false
- **描述**: The numerical value used as the ID of this I-PDU.

####### BOOLEAN 类型参数

######## 1. DltITxPduUsesTp

- **UUID**: `04267823-78c2-484c-a0a4-741024bb1b09`
- **参数名**: `DltITxPduUsesTp`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: If set to TRUE, the PDU is transmitted using the TP API. If FALSE, the IF API is used.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. DltTxPduIdRef

- **UUID**: `8548c1f7-bcd4-431f-a2b7-db4d1f780941`
- **引用名**: `DltTxPduIdRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to the "global" Pdu structure to allow harmonization of handle IDs in the COM-Stack.

##### 7. DltLogChannelAssignment

**容器属性**:

- **UUID**: `2762e466-1cb6-4393-8aac-6eed8c9b076a`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DltLogChannelAssignment`
- **多重性**: [0..infinite]
- **需要索引**: false

**容器描述**:

This container contains a preconfiguration of ApplicationId / ContextId pairs and their assigned log channel.

###### 引用关系

此容器包含 **2** 个引用：

####### REFERENCE 类型引用

######## 1. DltLogChannelAssignmentSwcContextRef

- **UUID**: `2d832b05-e0d7-494b-890d-b420942072dc`
- **引用名**: `DltLogChannelAssignmentSwcContextRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `DltSwcContext`
- **完整路径**: `/MICROSAR/Dlt/DltSwc/DltSwcContext`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to an ApplicationId/ContextId pair that is assigned to a DltLogChannel.

######## 2. DltLogChannelRef

- **UUID**: `364d993a-728a-4f59-a3c6-74409f719467`
- **引用名**: `DltLogChannelRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `DltLogChannel`
- **完整路径**: `/MICROSAR/Dlt/DltConfigSet/DltLogOutput/DltLogChannel`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to a DltLogChannel that is assigned to an ApplicationId / ContextId pair.

##### 8. DltProtocol

**容器属性**:

- **UUID**: `bc91adb5-cfa6-4c0d-8b99-a77a5dfba574`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DltProtocol`
- **多重性**: [1..1]
- **需要索引**: false

**容器描述**:

Configuration parameters for handling the specific protocol variants.

###### 参数配置

此容器包含 **5** 个参数：

####### BOOLEAN 类型参数

######## 1. DltHeaderUseEcuId

- **UUID**: `213f5834-08e9-405f-adf6-efab72e70704`
- **参数名**: `DltHeaderUseEcuId`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Corresponds to field WEID (With ECU ID). If set ECU ID shall be placed in the header, else not.

######## 2. DltHeaderUseSessionID

- **UUID**: `dcf4be5b-cd1e-4e51-921c-33d94c0b6444`
- **参数名**: `DltHeaderUseSessionID`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Corresponds to field WSID (with Session ID). If set the Session ID shall be placed in the header, else not.

######## 3. DltHeaderUseTimestamp

- **UUID**: `94e76c83-967c-419b-acd0-df12ec6a6300`
- **参数名**: `DltHeaderUseTimestamp`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Corresponds to field WTMS (With Timestamp). If set the timestamp shall be placed in the header, else not.

######## 4. DltUseExtHeaderInNonVerbMode

- **UUID**: `7d16b1a6-1f86-40fb-86a4-6cfcc2476d5c`
- **参数名**: `DltUseExtHeaderInNonVerbMode`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Non Verbose messages (opposed to verbose messages) do not need an extended header. If this flag is set to true the extended header shall also be used for non verbose messages.

######## 5. DltUseVerboseMode

- **UUID**: `22f70795-eb43-4f12-9147-9ed8ea66a144`
- **参数名**: `DltUseVerboseMode`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: If this flag is set to TRUE, the payload shall be transmitted in verbose mode, else the payload shall be transmitted in none-verbose mode.

###### 配置容器

本模块包含 **3** 个配置容器：

####### 1. DltEcuIdCalloutChoice

**容器属性**:

- **UUID**: `87f90a5c-8b0d-4e43-92c4-c0d9b5a549bc`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DltEcuIdCalloutChoice`
- **多重性**: [0..1]
- **需要索引**: false

**容器描述**:

EcuId via user defined callout.
This choice is not supported!

######## 参数配置

此容器包含 **1** 个参数：

######### FUNCTION-NAME 类型参数

########## 1. DltEcuIdCallout

- **UUID**: `fa6e6aaa-5bb1-4104-9bed-92fe2b4c7b52`
- **参数名**: `DltEcuIdCallout`
- **数据类型**: FUNCTION-NAME
- **多重性**: [1..1]
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **函数变体**:
  - 默认值: `DltAppl_GetEcuId`
- **描述**: If this choice is used the EcuId shall be fetched by calling the here configured callout function.
This parameter is not supported!

####### 2. DltEcuIdValueChoice

**容器属性**:

- **UUID**: `b34157f0-9190-4f73-a88b-6c42642ad4b8`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DltEcuIdValueChoice`
- **多重性**: [0..1]
- **需要索引**: false

**容器描述**:

EcuId value configuration

######## 参数配置

此容器包含 **1** 个参数：

######### STRING 类型参数

########## 1. DltEcuIdValue

- **UUID**: `09aefb92-68f4-4bab-9a25-21e34bf40f36`
- **参数名**: `DltEcuIdValue`
- **数据类型**: STRING
- **多重性**: [1..1]
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **字符串变体**:
  - 默认值: `ECUI`
  - 最大长度: 4
  - 最小长度: 1
- **描述**: If this choice is used the EcuId shall be taken from the configured string.

####### 3. DltEcuId

**容器属性**:

- **UUID**: `92605436-79a4-4864-91bc-09b9d58a385b`
- **容器类型**: CHOICE-CONTAINER
- **容器名称**: `DltEcuId`
- **多重性**: [1..1]
- **需要索引**: false

**容器选择**:

- **DltEcuIdCalloutChoice**
  - UUID: `87f90a5c-8b0d-4e43-92c4-c0d9b5a549bc`
  - 描述: EcuId via user defined callout.
This choice is not supported!
- **DltEcuIdValueChoice**
  - UUID: `b34157f0-9190-4f73-a88b-6c42642ad4b8`
  - 描述: EcuId value configuration

**容器描述**:

This is a choice container to choose between a EcuId value or a callout to get the EcuId.

##### 9. DltEcuIdCalloutChoice

**容器属性**:

- **UUID**: `87f90a5c-8b0d-4e43-92c4-c0d9b5a549bc`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DltEcuIdCalloutChoice`
- **多重性**: [0..1]
- **需要索引**: false

**容器描述**:

EcuId via user defined callout.
This choice is not supported!

###### 参数配置

此容器包含 **1** 个参数：

####### FUNCTION-NAME 类型参数

######## 1. DltEcuIdCallout

- **UUID**: `fa6e6aaa-5bb1-4104-9bed-92fe2b4c7b52`
- **参数名**: `DltEcuIdCallout`
- **数据类型**: FUNCTION-NAME
- **多重性**: [1..1]
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **函数变体**:
  - 默认值: `DltAppl_GetEcuId`
- **描述**: If this choice is used the EcuId shall be fetched by calling the here configured callout function.
This parameter is not supported!

##### 10. DltEcuIdValueChoice

**容器属性**:

- **UUID**: `b34157f0-9190-4f73-a88b-6c42642ad4b8`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DltEcuIdValueChoice`
- **多重性**: [0..1]
- **需要索引**: false

**容器描述**:

EcuId value configuration

###### 参数配置

此容器包含 **1** 个参数：

####### STRING 类型参数

######## 1. DltEcuIdValue

- **UUID**: `09aefb92-68f4-4bab-9a25-21e34bf40f36`
- **参数名**: `DltEcuIdValue`
- **数据类型**: STRING
- **多重性**: [1..1]
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **字符串变体**:
  - 默认值: `ECUI`
  - 最大长度: 4
  - 最小长度: 1
- **描述**: If this choice is used the EcuId shall be taken from the configured string.

##### 11. DltRxPdu

**容器属性**:

- **UUID**: `efdf2e41-b88d-41a5-a5e2-10d79de64f17`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DltRxPdu`
- **多重性**: [0..infinite]
- **需要索引**: false

**容器描述**:

Contains the Pdu IDs to be used for Dlt control messages reception.

###### 参数配置

此容器包含 **2** 个参数：

####### INTEGER 类型参数

######## 1. DltIRxPduHandleId

- **UUID**: `20ffbea7-88fe-4874-9a00-b6f3674df0f2`
- **参数名**: `DltIRxPduHandleId`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **需要索引**: false
- **描述**: The numerical value used as the ID of this I-PDU. The DltRxPduHandleId is required by the API calls Dlt_RxIndication, Dlt_TpRxIndication, Dlt_StartOfReception and Dlt_CopyRxData to receive I-PDUs from the PduR (DltIPduDirection: Receive), as well as the PduId passed to an Rx-I-PDU-callout.

####### BOOLEAN 类型参数

######## 1. DltIRxPduUsesTp

- **UUID**: `81e66fd4-2bad-410e-bd75-403889f09d1f`
- **参数名**: `DltIRxPduUsesTp`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: If set to TRUE, the PDU is received using the TP API. If FALSE, the IF API is used.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. DltRxPduIdRef

- **UUID**: `d36a42c4-b153-4aa0-bf0e-b9192ce66cf7`
- **引用名**: `DltRxPduIdRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to the "global" Pdu structure to allow harmonization of handle IDs in the COM-Stack.

##### 12. DltTraceStatusSetting

**容器属性**:

- **UUID**: `7d8c667f-b54f-4aed-8f9e-9d6e4675a179`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DltTraceStatusSetting`
- **多重性**: [1..1]
- **需要索引**: false

**容器描述**:

Contains settings for trace status

###### 参数配置

此容器包含 **1** 个参数：

####### BOOLEAN 类型参数

######## 1. DltDefaultTraceStatus

- **UUID**: `8a205e2c-605f-427f-a295-e0259dbe9469`
- **参数名**: `DltDefaultTraceStatus`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: This is the effective trace status used in case no filter matches the given ApplicationId and ContextId. This can be seen as a fall-through filter definition with wildcard for ApplicationId and ContextId, which will be used, when no other filter matches.

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. DltTraceStatusAssignment

**容器属性**:

- **UUID**: `e9c3c8ea-af03-4bbc-ab11-8214a0f0a9c0`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DltTraceStatusAssignment`
- **多重性**: [0..infinite]
- **需要索引**: false

**容器描述**:

This container contains a preconfiguration of ApplicationId / ContextId pairs and their assigned trace status.

######## 参数配置

此容器包含 **1** 个参数：

######### BOOLEAN 类型参数

########## 1. DltTraceStatus

- **UUID**: `3aa3c212-9589-4032-99f4-d2336e31ac3a`
- **参数名**: `DltTraceStatus`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Trace status for the given ApplicationId/ContextId tuple.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. DltTraceStatusAssignmentSwcContextRef

- **UUID**: `a71f18c7-30f1-42e7-b686-22bc9eb06ea1`
- **引用名**: `DltTraceStatusAssignmentSwcContextRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `DltSwcContext`
- **完整路径**: `/MICROSAR/Dlt/DltSwc/DltSwcContext`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to an ApplicationId/ContextId pair to which a DltTraceStatus is assigned.

##### 13. DltTraceStatusAssignment

**容器属性**:

- **UUID**: `e9c3c8ea-af03-4bbc-ab11-8214a0f0a9c0`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DltTraceStatusAssignment`
- **多重性**: [0..infinite]
- **需要索引**: false

**容器描述**:

This container contains a preconfiguration of ApplicationId / ContextId pairs and their assigned trace status.

###### 参数配置

此容器包含 **1** 个参数：

####### BOOLEAN 类型参数

######## 1. DltTraceStatus

- **UUID**: `3aa3c212-9589-4032-99f4-d2336e31ac3a`
- **参数名**: `DltTraceStatus`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Trace status for the given ApplicationId/ContextId tuple.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. DltTraceStatusAssignmentSwcContextRef

- **UUID**: `a71f18c7-30f1-42e7-b686-22bc9eb06ea1`
- **引用名**: `DltTraceStatusAssignmentSwcContextRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `DltSwcContext`
- **完整路径**: `/MICROSAR/Dlt/DltSwc/DltSwcContext`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to an ApplicationId/ContextId pair to which a DltTraceStatus is assigned.

##### 14. DltGeneral

**容器属性**:

- **UUID**: `7bec15a9-b60d-4aa9-89e4-775f43ac7082`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DltGeneral`
- **多重性**: [1..1]
- **需要索引**: false

**容器描述**:

This container lists all the global Dlt functionalities that can be enabled or disabled at pre-compile time to optimize resource consumption.

###### 参数配置

此容器包含 **20** 个参数：

####### INTEGER 类型参数

######## 1. DltMaxNumberOfApplications

- **UUID**: `d29f5f5a-aaa6-4a8c-a159-1d451c007048`
- **参数名**: `DltMaxNumberOfApplications`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `10`
- **取值范围**: [2..65535]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Defines the maximum number of registered applications.

Note:
1. The configured value includes all configured applications.
     - Therefore, if additional applications shall be able to register at runtime, this value must be greater than the configured number of applications.
     - The minimum value is the number of configured applications + 1 for DEM + 1 for DET (+ 1 for OS if DltOsSoftwareTracing is enabled).
2. This value affects the required RAM usage of the Dlt.

######## 2. DltMaxNumberOfContextsPerApplication

- **UUID**: `a0928087-cc93-45ca-8baa-95fad5592c96`
- **参数名**: `DltMaxNumberOfContextsPerApplication`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `5`
- **取值范围**: [1..65535]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Defines the maximum number of registered contexts for any application.

Note:
1. The configured value includes the configured contexts.
     - Therefore, if additional contexts shall be able to register at runtime, this value must be greater than the configured number of contexts.
     - The minimum value is the maximum number of contexts any configured application has (+ 3 if DltOsSoftwareTracing is enabled).
2. This value affects the required RAM usage of the Dlt.

######## 3. DltServerPortQueueSizeForLogAndTraceMessages

- **UUID**: `fd6877f0-e7dd-41f8-bfd1-f9c617bd796e`
- **参数名**: `DltServerPortQueueSizeForLogAndTraceMessages`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `1`
- **取值范围**: [1..256]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Defines how many requests of SendLogMessage and SendTraceMessage can be triggered for same Server-Client Port.
Values greater one only required if multiple runnables of same SWC are using the same Dlt Server-Client Port to send log and trace messages.

####### BOOLEAN 类型参数

######## 1. DltGeneralDevErrorDetect

- **UUID**: `b861622a-3bd1-4d36-bccd-36cd443277b1`
- **参数名**: `DltGeneralDevErrorDetect`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: If the Default Error Tracer (Det) shall be used, this parameter shall be set to TRUE. Otherwise, it shall be set to FALSE.

######## 2. DltGeneralInjectionSupport

- **UUID**: `5d7d911b-cb1e-484b-98bc-ea96be3563cb`
- **参数名**: `DltGeneralInjectionSupport`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Enables or disables the Dlt Injection feature.

######## 3. DltGeneralRegisterContextNotification

- **UUID**: `08bb9d06-1b52-44b9-b56f-45f63a296021`
- **参数名**: `DltGeneralRegisterContextNotification`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: If this parameter is set to TRUE, a Dlt Control Message is sent every time a SWC registeres and/or de-registers at/from the Dlt Module. Else, this notification is not sent.
This parameter is not supported!

######## 4. DltGeneralRxDataPathSupport

- **UUID**: `d53c685b-61ad-4d39-b791-00720314bdb9`
- **参数名**: `DltGeneralRxDataPathSupport`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Enables or disables the Rx Data Path to control the Dlt module.

Note:
If this parameter is disabled: The used SocketConnection must know a specific Remote Address and Remote Port, otherwise the socket connection cannot be opened!
If this parameter is enabled: The Remote Address and Remote Port may be undefined. Then the socket is opened with the first received message.

######## 5. DltGeneralTimeStampSupport

- **UUID**: `8eab7959-7486-4d4d-ae56-0bba06c87291`
- **参数名**: `DltGeneralTimeStampSupport`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: If a Time Stamp shall be added to the Dlt messages, this configuration parameter shall be set to TRUE.

######## 6. DltGeneralTrafficShapingSupport

- **UUID**: `9b2e11d5-ed51-4cfb-9410-5afde14472ba`
- **参数名**: `DltGeneralTrafficShapingSupport`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Enables or disables the TrafficShaping feature to limit the maximum bandwidth for Dlt messages. If enabled, the maximum bandwidth can be configured per LogChannel.

Note: The TrafficShaping is based on the leaky bucket method. This means, transmissions are allowed in each call of Dlt_MainFunction, but it is limited to the configured maximum value.

######## 7. DltGeneralVersionInfoApi

- **UUID**: `e56fe22d-ad64-4084-a658-b92bf5c7f00d`
- **参数名**: `DltGeneralVersionInfoApi`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Pre-processor switch for enabling Version Info API support.

######## 8. DltSafeBswChecks

- **UUID**: `a20167a9-17ce-4a08-9de2-0b648afb69d8`
- **参数名**: `DltSafeBswChecks`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Selects if safety checks are used. These checks improve robustness as e.g. invalid parameters are checked before function is executed. This attribute has to be enabled for safety projects where this component is mapped to an ASIL partition.

######## 9. DltDemEventFiltering

- **UUID**: `f6aff3c6-bbf8-4521-817f-c293df6532ed`
- **参数名**: `DltDemEventFiltering`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: If active, forwarded DEM events are filtered if event status has not changed.
If inactive, all DEM events are sent.

######## 10. DltGeneralNvRAMSupport

- **UUID**: `5d4c2596-0432-4219-aba6-5fcc19fde787`
- **参数名**: `DltGeneralNvRAMSupport`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: If active, part of Dlt settings are persisted in non-volatile memory. During initalization the persisted settings are restored and used for initalization instead of the configured values.
If inactive, always the configured values are used for initialization.

######## 11. DltSupportDefaultAPI

- **UUID**: `8499190d-bdac-48ef-9e81-e63813566aa0`
- **参数名**: `DltSupportDefaultAPI`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: This parameter defines if the Dlt API is generated as specified by AUTOSAR:
If enabled:
- The API Dlt_(Get/Set)DefaultTraceStatus has a second parameter "LogChannelName".
- As specified by AUTOSAR
If disabled:
- The API Dlt_(Get/Set)DefaultTraceStatus has only one parameter.
- Deviation from AUTOSAR

######## 12. DltOsSoftwareTracing

- **UUID**: `d0900f51-f3b5-4297-a64b-256a615c27af`
- **参数名**: `DltOsSoftwareTracing`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: This parameter defines if the OS Software Tracing is enabled or not.

The OS Software Tracing make use of the Vector TimingHooks:
- OS_VTH_SCHEDULE
- OS_VTH_SETEVENT
- OS_VTH_ACTIVATION

If this feature is enabled, the DltGeneralTimeStampSupport shall be enabled to provide timestamps in the OS Tracing messages.

If this feature is enabled and the BSW runs on multiple cores, DltAssignedEcucCoreRef shall be set to provide the DLT on which core it is executed.

If DltGeneralNvRAMSupport is enabled, this parameter increases the required Nv memory of Dlt.

####### FLOAT 类型参数

######## 1. DltGeneralStartUpDelayTimer

- **UUID**: `8bc33e9b-86a0-4934-a152-3fcd9ee8319b`
- **参数名**: `DltGeneralStartUpDelayTimer`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **默认值**: `0.001`
- **取值范围**: [0.001..10]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Configurable delay in s of starting the transmission of Log and Trace messages after the Dlt module has been initialized.
This parameter is not supported!

######## 2. DltMainFunctionCycleTime

- **UUID**: `ba43cdfe-41f7-4b83-ae2e-4de185789615`
- **参数名**: `DltMainFunctionCycleTime`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `0.01`
- **取值范围**: [0.001..1]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Cycle time of DLT mainfunction.

A value of 10 [ms] is recommended.

####### STRING 类型参数

######## 1. DltUserConfigFile

- **UUID**: `519fd349-37ca-4ec1-91b3-20c683f18982`
- **参数名**: `DltUserConfigFile`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Reference to an external user configuration file that will be included during generation.
The content of the user configuration file will be added at the end of the generated module configuration file and allows altering or extending the generated code.
Caution: User configuration files can cause the software module to malfunction and must only be used with great care!

####### ENUMERATION 类型参数

######## 1. DltComLayer

- **UUID**: `ff21fa17-1843-4874-9827-231550b80a5f`
- **参数名**: `DltComLayer`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `XCP`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `XCP` (来源: Vector Informatik)
  - `PduR` (来源: Vector Informatik)
- **描述**: Defines the communication layer to be used.
 - XCP: Use XCP as transport protocol
 - PduR: Use PduR as transport protocol

######## 2. DltInitialGlobalState

- **UUID**: `82f2129d-69a3-456d-ae22-14bb240fe5a7`
- **参数名**: `DltInitialGlobalState`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `OFFLINE`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `OFFLINE` (来源: Vector Informatik)
  - `ONLINE` (来源: Vector Informatik)
- **描述**: Defines if the DLT shall be OFFLINE after initialization or ONLINE.
OFFLINE: Rejects log and trace messages after initialization.
ONLINE: Accepts log and trace messages after initialization.

In both cases, the state can be changed by the application with the port "SetState".

OFFLINE is the default state, but if DltOsSoftwareTracing is enabled, it is recommended to set this parameter to ONLINE. Otherwise, some thread transitions are missed in the trace.

###### 引用关系

此容器包含 **4** 个引用：

####### REFERENCE 类型引用

######## 1. DltAssignedEcucCoreRef

- **UUID**: `8030a336-3c81-4873-b8f3-9514cab5d92f`
- **引用名**: `DltAssignedEcucCoreRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `EcucCoreDefinition`
- **完整路径**: `/MICROSAR/EcuC/EcucHardware/EcucCoreDefinition`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **需要索引**: false
- **描述**: Optional reference to a EcuC Core.
It is required that the referenced core is an AUTOSAR core.
This reference is only required if the system supports multi core and DltOsSoftwareTracing is enabled.
The referenced core is the only core to be traced.

ATTENTION: the DLT does not support multicore, therefore all services must be called on the same core! This includes the StartOfReception, CopyRxData, CopyTxData, SendLogMessage, SendTraceMessage, RegisterContext, SetState, and (almost) all others.
ATTENTION: the DLT does not check that all services are called on the given core, this shall be verified by the system integrator.
The only exceptions are Dlt_DetForwardErrorTrace and Dlt_DemTriggerOnEventStatus. In these services the core is checked, therefore it is not possible to forward DETs and DEM events from other cores!

####### SYMBOLIC-NAME-REFERENCE 类型引用

######## 1. DltGeneralGptChannelRef

- **UUID**: `b45cfa77-9d8b-45de-86ae-dec20ebadfab`
- **引用名**: `DltGeneralGptChannelRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `GptChannelConfiguration`
- **完整路径**: `/AUTOSAR/EcucDefs/Gpt/GptChannelConfigSet/GptChannelConfiguration`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: If TimeStampSupport is used the Dlt module shall fetch the time from the Gpt module by calling Gpt_GetTimeElapsed with the here referenced GptChannel. The tick duration can be deduced from the GptChannelTickFrequency parameter of the GptChannelConfiguration container. This is necessary to calculate the microsecond resolution timestamp output in the Dlt message.

######## 2. DltGeneralNvRamRef

- **UUID**: `1c5255f3-222d-4875-9a61-a1ff69967a12`
- **引用名**: `DltGeneralNvRamRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `NvMBlockDescriptor`
- **完整路径**: `/AUTOSAR/EcucDefs/NvM/NvMBlockDescriptor`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: If the Dlt module shall be able to store modified parameters during runtime persistently, this reference shall be set and shall point to the NvmBlock.

######## 3. DltGeneralStbMTimeBaseRef

- **UUID**: `43166f84-175c-48cc-b0cc-bb1013f06b68`
- **引用名**: `DltGeneralStbMTimeBaseRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `StbMSynchronizedTimeBase`
- **完整路径**: `/AUTOSAR/EcucDefs/StbM/StbMSynchronizedTimeBase`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: If TimeStampSupport is used the Dlt module shall fetch the time from the StbM module by calling StbM_GetCurrentTime with the here referenced StbMSynchronizedTimeBase.

##### 15. DltSwc

**容器属性**:

- **UUID**: `f3656973-99dd-46a2-ba69-effe35687fed`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DltSwc`
- **多重性**: [0..infinite]
- **需要索引**: false

**容器描述**:

Contains necessary configuration parameters of the AUTOSAR Dlt module to interact with SWCs.

###### 参数配置

此容器包含 **4** 个参数：

####### INTEGER 类型参数

######## 1. DltSwcSessionId

- **UUID**: `a3f6e802-8395-47bd-8e80-c6fa9aaf257f`
- **参数名**: `DltSwcSessionId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..18446744073709551615]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: An ECU wide unique ID to identify the port a SWC (instance) uses.

######## 2. MaxSwcLogMessageLength

- **UUID**: `51bb7d8f-1eb1-461a-a343-4b357a48f3a9`
- **参数名**: `MaxSwcLogMessageLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `256`
- **取值范围**: [0..65535]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Defines the maximum allowed length (unit16) for LogMessages.
This parameter is not supported!

######## 3. MaxSwcTraceMessageLength

- **UUID**: `0d3d2396-03c9-4381-899d-ed2e49cbebfa`
- **参数名**: `MaxSwcTraceMessageLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `256`
- **取值范围**: [0..65535]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Defines the maximum allowed length (unit16) for TraceMessages.
This parameter is not supported!

####### BOOLEAN 类型参数

######## 1. DltSwcSupportLogLevelChangeNotification

- **UUID**: `1560405a-3291-4995-82a3-84c36ba1f7ef`
- **参数名**: `DltSwcSupportLogLevelChangeNotification`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Flag indicating, whether Dlt has to provide a R-Port for the notification of the SWC about LogLevel changes.

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. DltSwcContext

**容器属性**:

- **UUID**: `e2042124-2c7f-430a-923d-653bdb5c7a6d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DltSwcContext`
- **多重性**: [0..infinite]
- **需要索引**: false

**容器描述**:

This container contains the configuration of ApplicationId / ContextId pairs which are supported by this SWC.

If DltGeneralNvRAMSupport is enabled, increasing the number of this container will also increase the required Nv memory of Dlt.

######## 参数配置

此容器包含 **2** 个参数：

######### STRING 类型参数

########## 1. DltSwcApplicationId

- **UUID**: `16228469-74b7-432f-8ae3-d71c017b43c1`
- **参数名**: `DltSwcApplicationId`
- **数据类型**: STRING
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **字符串变体**:
  - 默认值: `MyAI`
- **描述**: Abbreviation for the SWC (4 characters)

########## 2. DltSwcContextId

- **UUID**: `837f8078-1887-45cd-b9ac-9b039440cd1c`
- **参数名**: `DltSwcContextId`
- **数据类型**: STRING
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **字符串变体**:
  - 默认值: `MyCI`
- **描述**: Abbreviation for the ContextId (4 characters)

##### 16. DltSwcContext

**容器属性**:

- **UUID**: `e2042124-2c7f-430a-923d-653bdb5c7a6d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DltSwcContext`
- **多重性**: [0..infinite]
- **需要索引**: false

**容器描述**:

This container contains the configuration of ApplicationId / ContextId pairs which are supported by this SWC.

If DltGeneralNvRAMSupport is enabled, increasing the number of this container will also increase the required Nv memory of Dlt.

###### 参数配置

此容器包含 **2** 个参数：

####### STRING 类型参数

######## 1. DltSwcApplicationId

- **UUID**: `16228469-74b7-432f-8ae3-d71c017b43c1`
- **参数名**: `DltSwcApplicationId`
- **数据类型**: STRING
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **字符串变体**:
  - 默认值: `MyAI`
- **描述**: Abbreviation for the SWC (4 characters)

######## 2. DltSwcContextId

- **UUID**: `837f8078-1887-45cd-b9ac-9b039440cd1c`
- **参数名**: `DltSwcContextId`
- **数据类型**: STRING
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **字符串变体**:
  - 默认值: `MyCI`
- **描述**: Abbreviation for the ContextId (4 characters)

##### 17. DltNonVerboseMessage

**容器属性**:

- **UUID**: `ae241dca-34b2-445f-a408-03664d9554ea`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DltNonVerboseMessage`
- **多重性**: [0..infinite]
- **需要索引**: false

**容器描述**:

Non-Verbose messages require a minimum bandwith as only its identifier will be transmitted over the network. The XCP tool will then resolve the identifier to the string defined as static data. To transmit a non-verbose message use the API: <Name>.

Hint: Use the verbose message API to transmit a runtime defined string over the network.

###### 参数配置

此容器包含 **2** 个参数：

####### INTEGER 类型参数

######## 1. DltMessageId

- **UUID**: `bee32f31-4da3-4d0b-943e-4aad2bc856c2`
- **参数名**: `DltMessageId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `3`
- **取值范围**: [3..4294967295]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: true
- **需要索引**: false
- **描述**: Message ID is the unique ID to characterize the information, which is transported by the non-verbose message itself. The message ID will be assigned automatically.

RESTRICTIONS: Message IDs used for Dem (1) and Det (2) are reserved and not usable for the application.

####### STRING 类型参数

######## 1. DltStaticData

- **UUID**: `48e03a30-9233-4cd6-bda7-5cc74f4b93d0`
- **参数名**: `DltStaticData`
- **数据类型**: STRING
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: true
- **需要索引**: false
- **字符串变体**:
  - 默认值: `My static message`
- **描述**: Data of static information that is associated with the Message ID. This data is not transmitted with the non-verbose message but is stored in the A2L file.

##### 18. DltEcuId

**容器属性**:

- **UUID**: `92605436-79a4-4864-91bc-09b9d58a385b`
- **容器类型**: CHOICE-CONTAINER
- **容器名称**: `DltEcuId`
- **多重性**: [1..1]
- **需要索引**: false

**容器选择**:

- **DltEcuIdCalloutChoice**
  - UUID: `87f90a5c-8b0d-4e43-92c4-c0d9b5a549bc`
  - 描述: EcuId via user defined callout.
This choice is not supported!
- **DltEcuIdValueChoice**
  - UUID: `b34157f0-9190-4f73-a88b-6c42642ad4b8`
  - 描述: EcuId value configuration

**容器描述**:

This is a choice container to choose between a EcuId value or a callout to get the EcuId.

## 📦 包结构

此ARXML文件包含 **1** 个包：

### 1. MICROSAR

- **UUID**: `ff55d029-386d-43a2-b3c2-dfef4c7a5e36`
- **包名称**: `MICROSAR`
- **包含元素数量**: 4

#### 包含的元素

##### ECUC-MODULE-DEF 类型元素

1. **Dlt**

##### BSW-IMPLEMENTATION 类型元素

1. **Dlt_Impl**

##### ECUC-MODULE-CONFIGURATION-VALUES 类型元素

1. **Dlt_Pre**
2. **Dlt_Rec**

## ⚡ 实现信息

此ARXML文件包含 **1** 个实现：

### 1. Dlt_Impl

- **UUID**: `900e76bf-9c7f-43e4-a802-f2f61703d072`
- **实现名称**: `Dlt_Impl`
- **编程语言**: C
- **软件版本**: 7.01.00
- **供应商ID**: 30
- **AUTOSAR版本**: 4.03.01
- **代码生成器**: cMSR

## ⚙️ 配置信息

此ARXML文件包含 **2** 个配置：

### 1. Dlt_Pre

- **UUID**: `cefedef2-7397-4cbc-a085-488bfd1d7ca3`
- **配置名称**: `Dlt_Pre`
- **定义引用**: `/MICROSAR/Dlt`

### 2. Dlt_Rec

- **UUID**: `7b81bc2b-2f4c-4ed1-85eb-fedbd345a9fe`
- **配置名称**: `Dlt_Rec`
- **定义引用**: `/MICROSAR/Dlt`
