# DoIPInt - 完整配置文档

*此文档由ARXML文件自动生成，采用层次化结构展示*

**生成时间**: 2025-06-16 14:44:49

## 📑 目录

- [📄 文件信息](#-文件信息)
- [🔧 模块定义](#-模块定义)
  - [DoIPInt](#doipint)
- [📦 包结构](#-包结构)
- [⚡ 实现信息](#-实现信息)

## 📄 文件信息

### Schema信息
- **Schema位置**: `http://autosar.org/schema/r4.0 AUTOSAR_4-2-2.xsd`
- **命名空间**: `http://autosar.org/schema/r4.0`

## 🔧 模块定义

### 1. DoIPInt

#### 基本信息

- **UUID**: `ceb5f6b7-ab86-4053-9592-ee97e30e3ebb`
- **模块名称**: `DoIPInt`
- **类别**: `VENDOR_SPECIFIC_MODULE_DEFINITION`
- **多重性**: [0..1]
- **支持的变体**:
  - VARIANT-PRE-COMPILE

#### 模块描述

The Diagnostic over IP for vehicle internal communication (DoIPInt) module implements a transport protocol for diagnostic data over the Internet Protocol. It is derived from the DoIP module according to ISO Standard 13400 and adapted to fit the vehicle internal communication needs.
#Ethernet #Diag
#Vector

#### 版本历史

共有 **18** 个版本记录：

##### 1. 版本 1.00.00

- **发布日期**: 2017-02-10T10:34:26+01:00
- **发布者**: vismda

**变更内容**:

##### 2. 版本 2.00.00

- **发布日期**: 2019-11-04T18:07:50+01:00
- **发布者**: viskjs

**变更内容**:

##### 3. 版本 2.00.01

- **发布日期**: 2020-04-23T14:46:57+02:00
- **发布者**: visjsb

**变更内容**:

##### 4. 版本 2.00.02

- **发布日期**: 2020-06-19T15:43:50+02:00
- **发布者**: viskjs

**变更内容**:

##### 5. 版本 2.00.03

- **发布日期**: 2020-10-22T15:11:20+02:00
- **发布者**: visjsb

**变更内容**:

##### 6. 版本 2.00.04

- **发布日期**: 2021-05-11T09:41:55+02:00
- **发布者**: vismda

**变更内容**:

##### 7. 版本 3.00.00

- **发布日期**: 2021-11-22T10:32:48+01:00
- **发布者**: viseje

**变更内容**:

##### 8. 版本 3.00.01

- **发布日期**: 2021-12-13T15:56:11+01:00
- **发布者**: viseje

**变更内容**:

##### 9. 版本 3.01.00

- **发布日期**: 2022-02-17T08:11:44+01:00
- **发布者**: viseje

**变更内容**:

##### 10. 版本 4.00.00

- **发布日期**: 2022-03-15T16:54:40+01:00
- **发布者**: viseje

**变更内容**:

##### 11. 版本 4.01.00

- **发布日期**: 2022-06-24T07:15:55+02:00
- **发布者**: viseje

**变更内容**:

##### 12. 版本 4.02.00

- **发布日期**: 2022-08-03T14:26:55+02:00
- **发布者**: viseje

**变更内容**:

##### 13. 版本 5.00.00

- **发布日期**: 2022-11-28T12:57:58+01:00
- **发布者**: viseje

**变更内容**:

##### 14. 版本 6.00.00

- **发布日期**: 2023-05-04T16:25:50+02:00
- **发布者**: visgyv

**变更内容**:

##### 15. 版本 

- **发布日期**: 2023-05-12T10:44:39+02:00
- **发布者**: visgyv

**变更内容**:

##### 16. 版本 6.01.00

- **发布日期**: 2023-07-10T11:02:17+02:00
- **发布者**: ygretzinger

**变更内容**:

##### 17. 版本 7.00.00

- **发布日期**: 2023-12-13T10:16:13+01:00
- **发布者**: jelsaesser

**变更内容**:

##### 18. 版本 7.01.00

- **发布日期**: 2024-04-08T10:11:43+02:00
- **发布者**: jelsaesser

**变更内容**:

#### 配置容器

本模块包含 **19** 个配置容器：

##### 1. DoIPIntConfigSet

**容器属性**:

- **UUID**: `5aea9bd5-2dc3-4c76-a02b-4d78f2ed1326`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPIntConfigSet`
- **多重性**: [1..1]
- **需要索引**: false

**容器描述**:

This container contains the configuration parameters and sub containers of the DoIPInt module.

###### 配置容器

本模块包含 **15** 个配置容器：

####### 1. DoIPIntChannel

**容器属性**:

- **UUID**: `1a565ba0-1477-4dc6-a66e-3305a8158c40`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPIntChannel`
- **多重性**: [1..65535]
- **需要索引**: false

**容器描述**:

This container includes the configuration to describe the link to the upper layer PDUR module,

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. DoIPIntChannelId

- **UUID**: `48ab7ba3-0ae2-458c-b040-6ec9c10d9291`
- **参数名**: `DoIPIntChannelId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65534]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: true
- **需要索引**: false
- **描述**: This parameter defines the Channel ID required for API calls using channels (e.g. DoIPInt_OverwriteLogicalAddresses()).

######### BOOLEAN 类型参数

########## 1. DoIPIntChannelReadyNotification

- **UUID**: `6244e7ff-f139-463e-9fe7-a4ca8c73d958`
- **参数名**: `DoIPIntChannelReadyNotification`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: This parameter defines whether this channel is related to the channel ready notification.
true:	BswM is notified when a TCP connection establishment succeeded.
false:	BswM is not notified.

######## 引用关系

此容器包含 **3** 个引用：

######### REFERENCE 类型引用

########## 1. DoIPIntLocalAddressRef

- **UUID**: `a26c4642-037c-4daa-8000-d2013081bfa8`
- **引用名**: `DoIPIntLocalAddressRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `DoIPIntLocalAddress`
- **完整路径**: `/MICROSAR/DoIPInt/DoIPIntConfigSet/DoIPIntLocalAddress`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **需要索引**: false
- **描述**: Reference to a DoIPIntLocalAddress which is used as logical address in diagnostic messages (e.g. as source address in case of transmission).

########## 2. DoIPIntRemoteAddressRef

- **UUID**: `bf045da4-e906-4e2e-9e9f-372831d9c899`
- **引用名**: `DoIPIntRemoteAddressRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `DoIPIntRemoteAddress`
- **完整路径**: `/MICROSAR/DoIPInt/DoIPIntConfigSet/DoIPIntRemoteAddress`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **需要索引**: false
- **描述**: Reference to a DoIPIntRemoteAddress which is used as logical address in diagnostic messages (e.g. as target address in case of transmission).

######### CHOICE-REFERENCE 类型引用

########## 1. DoIPIntClientOrServerConnectionRef

- **UUID**: `5deac71a-8c1c-4afb-84e1-8a98d1e244a9`
- **引用名**: `DoIPIntClientOrServerConnectionRef`
- **引用类型**: CHOICE-REFERENCE
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **需要索引**: false
- **目标引用列表**:
  - `/MICROSAR/DoIPInt/DoIPIntConfigSet/DoIPIntConnections/DoIPIntClientConnection`
  - `/MICROSAR/DoIPInt/DoIPIntConfigSet/DoIPIntConnections/DoIPIntServerConnection`
- **描述**: Reference to the DoIPIntClientConnection or DoIPIntServerConnection which is used to send or receive data for this channel.

######## 配置容器

本模块包含 **2** 个配置容器：

######### 1. DoIPIntPduRRxPdu

**容器属性**:

- **UUID**: `a226f39a-9abd-45ed-8bf1-a586d00c5571`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPIntPduRRxPdu`
- **多重性**: [0..1]
- **需要索引**: false

**容器描述**:

This container contains the Rx Pdu for the channel.

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. DoIPIntPduRRxPduId

- **UUID**: `b36fa7eb-195a-4c81-9752-a7b6fab9aa09`
- **参数名**: `DoIPIntPduRRxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: true
- **需要索引**: false
- **描述**: This parameter defines the Pdu ID required for  the TP API calls. (e.g. DoIPInt_TpCancelReceive()) to handle reception to PDUR.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. DoIPIntPduRRxPduRef

- **UUID**: `7715c382-31e9-49fd-a4c3-3f601957209d`
- **引用名**: `DoIPIntPduRRxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **需要索引**: false
- **描述**: Reference to the "global" Pdu structure to allow harmonization of handle IDs in the COM-Stack.

######### 2. DoIPIntPduRTxPdu

**容器属性**:

- **UUID**: `becefe37-757a-43a7-9eef-22d6ed6cdcd6`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPIntPduRTxPdu`
- **多重性**: [0..1]
- **需要索引**: false

**容器描述**:

This container contains the Tx Pdu for the channel

########## 参数配置

此容器包含 **2** 个参数：

########### INTEGER 类型参数

############ 1. DoIPIntPduRTxPduId

- **UUID**: `494601eb-0f3e-4e95-8211-bc440159aba3`
- **参数名**: `DoIPIntPduRTxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: true
- **需要索引**: false
- **描述**: This parameter defines the Pdu ID required for the TP and IF API calls. (e.g. DoIPInt_TpTransmit()) to send data from PDUR.

########### ENUMERATION 类型参数

############ 1. DoIPIntPduType

- **UUID**: `e3e74d75-b8c6-4919-912f-2c6bc2c2565c`
- **参数名**: `DoIPIntPduType`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `DOIPINT_TPPDU`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `DOIPINT_IFPDU` (来源: Vector Informatik)
  - `DOIPINT_TPPDU` (来源: Vector Informatik)
- **描述**: This parameter defines the API Type to use for communication with PduR.
DOIPINT_IFPDU for UUDT messages,
DOIPINT_TPPDU for all other diagnostic messages.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. DoIPIntPduRTxPduRef

- **UUID**: `896e01a8-59fb-4a8c-a965-4a1ad38f0a6a`
- **引用名**: `DoIPIntPduRTxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **需要索引**: false
- **描述**: Reference to the "global" Pdu structure to allow harmonization of handle IDs in the COM-Stack.

####### 2. DoIPIntPduRRxPdu

**容器属性**:

- **UUID**: `a226f39a-9abd-45ed-8bf1-a586d00c5571`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPIntPduRRxPdu`
- **多重性**: [0..1]
- **需要索引**: false

**容器描述**:

This container contains the Rx Pdu for the channel.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. DoIPIntPduRRxPduId

- **UUID**: `b36fa7eb-195a-4c81-9752-a7b6fab9aa09`
- **参数名**: `DoIPIntPduRRxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: true
- **需要索引**: false
- **描述**: This parameter defines the Pdu ID required for  the TP API calls. (e.g. DoIPInt_TpCancelReceive()) to handle reception to PDUR.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. DoIPIntPduRRxPduRef

- **UUID**: `7715c382-31e9-49fd-a4c3-3f601957209d`
- **引用名**: `DoIPIntPduRRxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **需要索引**: false
- **描述**: Reference to the "global" Pdu structure to allow harmonization of handle IDs in the COM-Stack.

####### 3. DoIPIntPduRTxPdu

**容器属性**:

- **UUID**: `becefe37-757a-43a7-9eef-22d6ed6cdcd6`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPIntPduRTxPdu`
- **多重性**: [0..1]
- **需要索引**: false

**容器描述**:

This container contains the Tx Pdu for the channel

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. DoIPIntPduRTxPduId

- **UUID**: `494601eb-0f3e-4e95-8211-bc440159aba3`
- **参数名**: `DoIPIntPduRTxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: true
- **需要索引**: false
- **描述**: This parameter defines the Pdu ID required for the TP and IF API calls. (e.g. DoIPInt_TpTransmit()) to send data from PDUR.

######### ENUMERATION 类型参数

########## 1. DoIPIntPduType

- **UUID**: `e3e74d75-b8c6-4919-912f-2c6bc2c2565c`
- **参数名**: `DoIPIntPduType`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `DOIPINT_TPPDU`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `DOIPINT_IFPDU` (来源: Vector Informatik)
  - `DOIPINT_TPPDU` (来源: Vector Informatik)
- **描述**: This parameter defines the API Type to use for communication with PduR.
DOIPINT_IFPDU for UUDT messages,
DOIPINT_TPPDU for all other diagnostic messages.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. DoIPIntPduRTxPduRef

- **UUID**: `896e01a8-59fb-4a8c-a965-4a1ad38f0a6a`
- **引用名**: `DoIPIntPduRTxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **需要索引**: false
- **描述**: Reference to the "global" Pdu structure to allow harmonization of handle IDs in the COM-Stack.

####### 4. DoIPIntConnections

**容器属性**:

- **UUID**: `1cab9af2-e698-4c6a-b015-6bf7288cfab3`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPIntConnections`
- **多重性**: [1..1]
- **需要索引**: false

**容器描述**:

This container contains the connections to the lower layer SOAD module.

######## 配置容器

本模块包含 **6** 个配置容器：

######### 1. DoIPIntClientConnection

**容器属性**:

- **UUID**: `1502115f-5545-4109-8380-b41a3b2156c5`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPIntClientConnection`
- **多重性**: [0..32767]
- **需要索引**: false

**容器描述**:

This container includes the connection configuration to the lower layer SOAD module for TCP client connections.

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. DoIPIntClientConnectionId

- **UUID**: `31afe52b-a3ba-404c-bc9e-3198d47041eb`
- **参数名**: `DoIPIntClientConnectionId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: true
- **需要索引**: false
- **描述**: This parameter gives a unique identifier for client and server connections required for API calls using connections (e.g. DoIPInt_CloseConnection(), DoIPInt_TransmitOemSpecificPayloadType()).

########## 配置容器

本模块包含 **2** 个配置容器：

########### 1. DoIPIntClientSoAdRxPdu

**容器属性**:

- **UUID**: `84c99d8a-bc48-4173-943c-e65e266bb923`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPIntClientSoAdRxPdu`
- **多重性**: [1..1]
- **需要索引**: false

**容器描述**:

This container contains the Rx Pdu for the TCP connection.

############ 参数配置

此容器包含 **1** 个参数：

############# INTEGER 类型参数

############## 1. DoIPIntClientSoAdRxPduId

- **UUID**: `4ff1698b-b980-4a5e-813a-8c3a8ea2e0ab`
- **参数名**: `DoIPIntClientSoAdRxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: true
- **需要索引**: false
- **描述**: This parameter defines the Pdu ID required for  the TP API calls. (e.g. DoIPInt_SoAdTpRxIndication()) to receive TCP data from SOAD.

############ 引用关系

此容器包含 **1** 个引用：

############# REFERENCE 类型引用

############## 1. DoIPIntClientSoAdRxPduRef

- **UUID**: `50b41288-42e4-420c-818c-f9438594af8c`
- **引用名**: `DoIPIntClientSoAdRxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **需要索引**: false
- **描述**: Reference to the "global" Pdu structure to allow harmonization of handle IDs in the COM-Stack.

########### 2. DoIPIntClientSoAdTxPdu

**容器属性**:

- **UUID**: `957a7f2b-faab-4637-9916-9520f08e600e`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPIntClientSoAdTxPdu`
- **多重性**: [1..1]
- **需要索引**: false

**容器描述**:

This container contains the Tx Pdu for the TCP connection.

############ 参数配置

此容器包含 **1** 个参数：

############# INTEGER 类型参数

############## 1. DoIPIntClientSoAdTxPduId

- **UUID**: `547ab530-1838-4ecd-bb38-6a3e6f64d404`
- **参数名**: `DoIPIntClientSoAdTxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: true
- **需要索引**: false
- **描述**: This parameter defines the Pdu ID required for  the TP API calls. (e.g. DoIPInt_SoAdTpTxConfirmation()) to confirm TCP data from SOAD.

############ 引用关系

此容器包含 **1** 个引用：

############# REFERENCE 类型引用

############## 1. DoIPIntClientSoAdTxPduRef

- **UUID**: `ac9aac90-c75f-4d1b-b6bb-11398ee19b5d`
- **引用名**: `DoIPIntClientSoAdTxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **需要索引**: false
- **描述**: Reference to the "global" Pdu structure to allow harmonization of handle IDs in the COM-Stack.

######### 2. DoIPIntClientSoAdRxPdu

**容器属性**:

- **UUID**: `84c99d8a-bc48-4173-943c-e65e266bb923`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPIntClientSoAdRxPdu`
- **多重性**: [1..1]
- **需要索引**: false

**容器描述**:

This container contains the Rx Pdu for the TCP connection.

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. DoIPIntClientSoAdRxPduId

- **UUID**: `4ff1698b-b980-4a5e-813a-8c3a8ea2e0ab`
- **参数名**: `DoIPIntClientSoAdRxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: true
- **需要索引**: false
- **描述**: This parameter defines the Pdu ID required for  the TP API calls. (e.g. DoIPInt_SoAdTpRxIndication()) to receive TCP data from SOAD.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. DoIPIntClientSoAdRxPduRef

- **UUID**: `50b41288-42e4-420c-818c-f9438594af8c`
- **引用名**: `DoIPIntClientSoAdRxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **需要索引**: false
- **描述**: Reference to the "global" Pdu structure to allow harmonization of handle IDs in the COM-Stack.

######### 3. DoIPIntClientSoAdTxPdu

**容器属性**:

- **UUID**: `957a7f2b-faab-4637-9916-9520f08e600e`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPIntClientSoAdTxPdu`
- **多重性**: [1..1]
- **需要索引**: false

**容器描述**:

This container contains the Tx Pdu for the TCP connection.

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. DoIPIntClientSoAdTxPduId

- **UUID**: `547ab530-1838-4ecd-bb38-6a3e6f64d404`
- **参数名**: `DoIPIntClientSoAdTxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: true
- **需要索引**: false
- **描述**: This parameter defines the Pdu ID required for  the TP API calls. (e.g. DoIPInt_SoAdTpTxConfirmation()) to confirm TCP data from SOAD.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. DoIPIntClientSoAdTxPduRef

- **UUID**: `ac9aac90-c75f-4d1b-b6bb-11398ee19b5d`
- **引用名**: `DoIPIntClientSoAdTxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **需要索引**: false
- **描述**: Reference to the "global" Pdu structure to allow harmonization of handle IDs in the COM-Stack.

######### 4. DoIPIntServerConnection

**容器属性**:

- **UUID**: `83411892-40f2-4935-8b1e-dc2278037c82`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPIntServerConnection`
- **多重性**: [0..32767]
- **需要索引**: false

**容器描述**:

This container includes the connection configuration to the lower layer SOAD module for TCP server connections.

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. DoIPIntServerConnectionId

- **UUID**: `81a9d93c-5c64-4d3a-8d9e-1b6d2f15c425`
- **参数名**: `DoIPIntServerConnectionId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: true
- **需要索引**: false
- **描述**: This parameter gives a unique identifier for client and server connections required for API calls using connections (e.g. DoIPInt_CloseConnection(), DoIPInt_TransmitOemSpecificPayloadType()).

########## 配置容器

本模块包含 **2** 个配置容器：

########### 1. DoIPIntServerSoAdRxPdu

**容器属性**:

- **UUID**: `4d120950-9c0f-4de4-80e7-3941acb8d328`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPIntServerSoAdRxPdu`
- **多重性**: [1..1]
- **需要索引**: false

**容器描述**:

This container contains the Rx Pdu for the TCP connection.

############ 参数配置

此容器包含 **1** 个参数：

############# INTEGER 类型参数

############## 1. DoIPIntServerSoAdRxPduId

- **UUID**: `6650d417-9186-4013-8609-f18f8a1bbd69`
- **参数名**: `DoIPIntServerSoAdRxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: true
- **需要索引**: false
- **描述**: This parameter defines the Pdu ID required for  the TP API calls. (e.g. DoIPInt_SoAdTpRxIndication()) to receive TCP data from SOAD.

############ 引用关系

此容器包含 **1** 个引用：

############# REFERENCE 类型引用

############## 1. DoIPIntServerSoAdRxPduRef

- **UUID**: `8792e6a7-8961-4d9b-8d71-6fc9952c3035`
- **引用名**: `DoIPIntServerSoAdRxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **需要索引**: false
- **描述**: Reference to the "global" Pdu structure to allow harmonization of handle IDs in the COM-Stack.

########### 2. DoIPIntServerSoAdTxPdu

**容器属性**:

- **UUID**: `15ffffe8-cbcf-455f-8529-9b63af6e3bf1`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPIntServerSoAdTxPdu`
- **多重性**: [1..1]
- **需要索引**: false

**容器描述**:

This container contains the Tx Pdu for the TCP connection.

############ 参数配置

此容器包含 **1** 个参数：

############# INTEGER 类型参数

############## 1. DoIPIntServerSoAdTxPduId

- **UUID**: `a5e8e43a-9ddb-490a-8fe6-1c1812db9fdb`
- **参数名**: `DoIPIntServerSoAdTxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: true
- **需要索引**: false
- **描述**: This parameter defines the Pdu ID required for  the TP API calls. (e.g. DoIPInt_SoAdTpTxConfirmation()) to confirm TCP data from SOAD.

############ 引用关系

此容器包含 **1** 个引用：

############# REFERENCE 类型引用

############## 1. DoIPIntServerSoAdTxPduRef

- **UUID**: `353ccf8e-3839-4cd9-aa20-a437a5daa19f`
- **引用名**: `DoIPIntServerSoAdTxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **需要索引**: false
- **描述**: Reference to the "global" Pdu structure to allow harmonization of handle IDs in the COM-Stack.

######### 5. DoIPIntServerSoAdRxPdu

**容器属性**:

- **UUID**: `4d120950-9c0f-4de4-80e7-3941acb8d328`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPIntServerSoAdRxPdu`
- **多重性**: [1..1]
- **需要索引**: false

**容器描述**:

This container contains the Rx Pdu for the TCP connection.

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. DoIPIntServerSoAdRxPduId

- **UUID**: `6650d417-9186-4013-8609-f18f8a1bbd69`
- **参数名**: `DoIPIntServerSoAdRxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: true
- **需要索引**: false
- **描述**: This parameter defines the Pdu ID required for  the TP API calls. (e.g. DoIPInt_SoAdTpRxIndication()) to receive TCP data from SOAD.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. DoIPIntServerSoAdRxPduRef

- **UUID**: `8792e6a7-8961-4d9b-8d71-6fc9952c3035`
- **引用名**: `DoIPIntServerSoAdRxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **需要索引**: false
- **描述**: Reference to the "global" Pdu structure to allow harmonization of handle IDs in the COM-Stack.

######### 6. DoIPIntServerSoAdTxPdu

**容器属性**:

- **UUID**: `15ffffe8-cbcf-455f-8529-9b63af6e3bf1`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPIntServerSoAdTxPdu`
- **多重性**: [1..1]
- **需要索引**: false

**容器描述**:

This container contains the Tx Pdu for the TCP connection.

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. DoIPIntServerSoAdTxPduId

- **UUID**: `a5e8e43a-9ddb-490a-8fe6-1c1812db9fdb`
- **参数名**: `DoIPIntServerSoAdTxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: true
- **需要索引**: false
- **描述**: This parameter defines the Pdu ID required for  the TP API calls. (e.g. DoIPInt_SoAdTpTxConfirmation()) to confirm TCP data from SOAD.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. DoIPIntServerSoAdTxPduRef

- **UUID**: `353ccf8e-3839-4cd9-aa20-a437a5daa19f`
- **引用名**: `DoIPIntServerSoAdTxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **需要索引**: false
- **描述**: Reference to the "global" Pdu structure to allow harmonization of handle IDs in the COM-Stack.

####### 5. DoIPIntClientConnection

**容器属性**:

- **UUID**: `1502115f-5545-4109-8380-b41a3b2156c5`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPIntClientConnection`
- **多重性**: [0..32767]
- **需要索引**: false

**容器描述**:

This container includes the connection configuration to the lower layer SOAD module for TCP client connections.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. DoIPIntClientConnectionId

- **UUID**: `31afe52b-a3ba-404c-bc9e-3198d47041eb`
- **参数名**: `DoIPIntClientConnectionId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: true
- **需要索引**: false
- **描述**: This parameter gives a unique identifier for client and server connections required for API calls using connections (e.g. DoIPInt_CloseConnection(), DoIPInt_TransmitOemSpecificPayloadType()).

######## 配置容器

本模块包含 **2** 个配置容器：

######### 1. DoIPIntClientSoAdRxPdu

**容器属性**:

- **UUID**: `84c99d8a-bc48-4173-943c-e65e266bb923`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPIntClientSoAdRxPdu`
- **多重性**: [1..1]
- **需要索引**: false

**容器描述**:

This container contains the Rx Pdu for the TCP connection.

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. DoIPIntClientSoAdRxPduId

- **UUID**: `4ff1698b-b980-4a5e-813a-8c3a8ea2e0ab`
- **参数名**: `DoIPIntClientSoAdRxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: true
- **需要索引**: false
- **描述**: This parameter defines the Pdu ID required for  the TP API calls. (e.g. DoIPInt_SoAdTpRxIndication()) to receive TCP data from SOAD.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. DoIPIntClientSoAdRxPduRef

- **UUID**: `50b41288-42e4-420c-818c-f9438594af8c`
- **引用名**: `DoIPIntClientSoAdRxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **需要索引**: false
- **描述**: Reference to the "global" Pdu structure to allow harmonization of handle IDs in the COM-Stack.

######### 2. DoIPIntClientSoAdTxPdu

**容器属性**:

- **UUID**: `957a7f2b-faab-4637-9916-9520f08e600e`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPIntClientSoAdTxPdu`
- **多重性**: [1..1]
- **需要索引**: false

**容器描述**:

This container contains the Tx Pdu for the TCP connection.

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. DoIPIntClientSoAdTxPduId

- **UUID**: `547ab530-1838-4ecd-bb38-6a3e6f64d404`
- **参数名**: `DoIPIntClientSoAdTxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: true
- **需要索引**: false
- **描述**: This parameter defines the Pdu ID required for  the TP API calls. (e.g. DoIPInt_SoAdTpTxConfirmation()) to confirm TCP data from SOAD.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. DoIPIntClientSoAdTxPduRef

- **UUID**: `ac9aac90-c75f-4d1b-b6bb-11398ee19b5d`
- **引用名**: `DoIPIntClientSoAdTxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **需要索引**: false
- **描述**: Reference to the "global" Pdu structure to allow harmonization of handle IDs in the COM-Stack.

####### 6. DoIPIntClientSoAdRxPdu

**容器属性**:

- **UUID**: `84c99d8a-bc48-4173-943c-e65e266bb923`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPIntClientSoAdRxPdu`
- **多重性**: [1..1]
- **需要索引**: false

**容器描述**:

This container contains the Rx Pdu for the TCP connection.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. DoIPIntClientSoAdRxPduId

- **UUID**: `4ff1698b-b980-4a5e-813a-8c3a8ea2e0ab`
- **参数名**: `DoIPIntClientSoAdRxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: true
- **需要索引**: false
- **描述**: This parameter defines the Pdu ID required for  the TP API calls. (e.g. DoIPInt_SoAdTpRxIndication()) to receive TCP data from SOAD.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. DoIPIntClientSoAdRxPduRef

- **UUID**: `50b41288-42e4-420c-818c-f9438594af8c`
- **引用名**: `DoIPIntClientSoAdRxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **需要索引**: false
- **描述**: Reference to the "global" Pdu structure to allow harmonization of handle IDs in the COM-Stack.

####### 7. DoIPIntClientSoAdTxPdu

**容器属性**:

- **UUID**: `957a7f2b-faab-4637-9916-9520f08e600e`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPIntClientSoAdTxPdu`
- **多重性**: [1..1]
- **需要索引**: false

**容器描述**:

This container contains the Tx Pdu for the TCP connection.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. DoIPIntClientSoAdTxPduId

- **UUID**: `547ab530-1838-4ecd-bb38-6a3e6f64d404`
- **参数名**: `DoIPIntClientSoAdTxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: true
- **需要索引**: false
- **描述**: This parameter defines the Pdu ID required for  the TP API calls. (e.g. DoIPInt_SoAdTpTxConfirmation()) to confirm TCP data from SOAD.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. DoIPIntClientSoAdTxPduRef

- **UUID**: `ac9aac90-c75f-4d1b-b6bb-11398ee19b5d`
- **引用名**: `DoIPIntClientSoAdTxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **需要索引**: false
- **描述**: Reference to the "global" Pdu structure to allow harmonization of handle IDs in the COM-Stack.

####### 8. DoIPIntServerConnection

**容器属性**:

- **UUID**: `83411892-40f2-4935-8b1e-dc2278037c82`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPIntServerConnection`
- **多重性**: [0..32767]
- **需要索引**: false

**容器描述**:

This container includes the connection configuration to the lower layer SOAD module for TCP server connections.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. DoIPIntServerConnectionId

- **UUID**: `81a9d93c-5c64-4d3a-8d9e-1b6d2f15c425`
- **参数名**: `DoIPIntServerConnectionId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: true
- **需要索引**: false
- **描述**: This parameter gives a unique identifier for client and server connections required for API calls using connections (e.g. DoIPInt_CloseConnection(), DoIPInt_TransmitOemSpecificPayloadType()).

######## 配置容器

本模块包含 **2** 个配置容器：

######### 1. DoIPIntServerSoAdRxPdu

**容器属性**:

- **UUID**: `4d120950-9c0f-4de4-80e7-3941acb8d328`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPIntServerSoAdRxPdu`
- **多重性**: [1..1]
- **需要索引**: false

**容器描述**:

This container contains the Rx Pdu for the TCP connection.

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. DoIPIntServerSoAdRxPduId

- **UUID**: `6650d417-9186-4013-8609-f18f8a1bbd69`
- **参数名**: `DoIPIntServerSoAdRxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: true
- **需要索引**: false
- **描述**: This parameter defines the Pdu ID required for  the TP API calls. (e.g. DoIPInt_SoAdTpRxIndication()) to receive TCP data from SOAD.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. DoIPIntServerSoAdRxPduRef

- **UUID**: `8792e6a7-8961-4d9b-8d71-6fc9952c3035`
- **引用名**: `DoIPIntServerSoAdRxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **需要索引**: false
- **描述**: Reference to the "global" Pdu structure to allow harmonization of handle IDs in the COM-Stack.

######### 2. DoIPIntServerSoAdTxPdu

**容器属性**:

- **UUID**: `15ffffe8-cbcf-455f-8529-9b63af6e3bf1`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPIntServerSoAdTxPdu`
- **多重性**: [1..1]
- **需要索引**: false

**容器描述**:

This container contains the Tx Pdu for the TCP connection.

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. DoIPIntServerSoAdTxPduId

- **UUID**: `a5e8e43a-9ddb-490a-8fe6-1c1812db9fdb`
- **参数名**: `DoIPIntServerSoAdTxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: true
- **需要索引**: false
- **描述**: This parameter defines the Pdu ID required for  the TP API calls. (e.g. DoIPInt_SoAdTpTxConfirmation()) to confirm TCP data from SOAD.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. DoIPIntServerSoAdTxPduRef

- **UUID**: `353ccf8e-3839-4cd9-aa20-a437a5daa19f`
- **引用名**: `DoIPIntServerSoAdTxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **需要索引**: false
- **描述**: Reference to the "global" Pdu structure to allow harmonization of handle IDs in the COM-Stack.

####### 9. DoIPIntServerSoAdRxPdu

**容器属性**:

- **UUID**: `4d120950-9c0f-4de4-80e7-3941acb8d328`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPIntServerSoAdRxPdu`
- **多重性**: [1..1]
- **需要索引**: false

**容器描述**:

This container contains the Rx Pdu for the TCP connection.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. DoIPIntServerSoAdRxPduId

- **UUID**: `6650d417-9186-4013-8609-f18f8a1bbd69`
- **参数名**: `DoIPIntServerSoAdRxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: true
- **需要索引**: false
- **描述**: This parameter defines the Pdu ID required for  the TP API calls. (e.g. DoIPInt_SoAdTpRxIndication()) to receive TCP data from SOAD.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. DoIPIntServerSoAdRxPduRef

- **UUID**: `8792e6a7-8961-4d9b-8d71-6fc9952c3035`
- **引用名**: `DoIPIntServerSoAdRxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **需要索引**: false
- **描述**: Reference to the "global" Pdu structure to allow harmonization of handle IDs in the COM-Stack.

####### 10. DoIPIntServerSoAdTxPdu

**容器属性**:

- **UUID**: `15ffffe8-cbcf-455f-8529-9b63af6e3bf1`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPIntServerSoAdTxPdu`
- **多重性**: [1..1]
- **需要索引**: false

**容器描述**:

This container contains the Tx Pdu for the TCP connection.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. DoIPIntServerSoAdTxPduId

- **UUID**: `a5e8e43a-9ddb-490a-8fe6-1c1812db9fdb`
- **参数名**: `DoIPIntServerSoAdTxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: true
- **需要索引**: false
- **描述**: This parameter defines the Pdu ID required for  the TP API calls. (e.g. DoIPInt_SoAdTpTxConfirmation()) to confirm TCP data from SOAD.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. DoIPIntServerSoAdTxPduRef

- **UUID**: `353ccf8e-3839-4cd9-aa20-a437a5daa19f`
- **引用名**: `DoIPIntServerSoAdTxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **需要索引**: false
- **描述**: Reference to the "global" Pdu structure to allow harmonization of handle IDs in the COM-Stack.

####### 11. DoIPIntRemoteAddress

**容器属性**:

- **UUID**: `73fb2f4c-5ea1-475e-a693-82e97ce1bced`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPIntRemoteAddress`
- **多重性**: [1..65535]
- **需要索引**: false

**容器描述**:

This container defines the logical remote address which is used in the diagnostic messages (e.g. as target address in case of transmission).

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. DoIPIntRemoteAddressValue

- **UUID**: `de8f8185-16e8-43ae-88bd-4109741fb234`
- **参数名**: `DoIPIntRemoteAddressValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: This parameter defines the logical remote address which is sent within diagnostic messages.

####### 12. DoIPIntLocalAddress

**容器属性**:

- **UUID**: `999c06e3-1d7e-4945-8607-fdf3d308791b`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPIntLocalAddress`
- **多重性**: [1..65535]
- **需要索引**: false

**容器描述**:

This container defines the logical local address which is used in the diagnostic messages (e.g. as source address in case of transmission).

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. DoIPIntLocalAddressValue

- **UUID**: `526bdd13-e346-430a-a8bc-54c6981242d3`
- **参数名**: `DoIPIntLocalAddressValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: This parameter defines the logical local address which is sent within diagnostic messages.

####### 13. DoIPIntOemPayload

**容器属性**:

- **UUID**: `565919a0-5eb1-4a2b-97f3-3761451716ab`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPIntOemPayload`
- **多重性**: [0..1]
- **需要索引**: false

**容器描述**:

This container defines parameter (Tx/Rx buffer and callback configuration) for OEM payload type messages.

######## 参数配置

此容器包含 **1** 个参数：

######### FUNCTION-NAME 类型参数

########## 1. DoIPIntOemPayloadRxCallback

- **UUID**: `8cc3a758-b519-4d01-9e95-dd89c5c6c060`
- **参数名**: `DoIPIntOemPayloadRxCallback`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **函数变体**:
  - 默认值: `Appl_DoIPInt_ReceiveOemSpecificPayloadType`
- **描述**: This parameter defines a callback function to forward received manufacturer-specific payload types to a user via <User>_DoIPIntReceiveOemSpecificPayloadType.

Note: In case no DoIPIntOemPayloadRxBuffer is configured which can be used for a connection no reception of OEM specific messages is supported on this connection and the reception of the message is skipped.

######## 配置容器

本模块包含 **2** 个配置容器：

######### 1. DoIPIntOemPayloadTxBuffer

**容器属性**:

- **UUID**: `086e0c4b-72d1-4b91-aae0-cc18088ce3eb`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPIntOemPayloadTxBuffer`
- **多重性**: [0..65535]
- **需要索引**: false

**容器描述**:

This container provides parameter to configure a Tx buffer which is used for messages with OEM payload type.

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. DoIPIntOemPayloadTxBufferSize

- **UUID**: `a15e1c33-c06c-43ee-8c4d-372c01928a9b`
- **参数名**: `DoIPIntOemPayloadTxBufferSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `1500`
- **取值范围**: [1..65535]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: This parameter defines the size of the Tx buffer for OEM payload type.

########## 引用关系

此容器包含 **1** 个引用：

########### CHOICE-REFERENCE 类型引用

############ 1. DoIPIntOemPayloadTxBufferClientOrServerConnectionRef

- **UUID**: `a778d695-a018-47dc-8f33-043b038eded0`
- **引用名**: `DoIPIntOemPayloadTxBufferClientOrServerConnectionRef`
- **引用类型**: CHOICE-REFERENCE
- **多重性**: [0..65535]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **需要索引**: false
- **目标引用列表**:
  - `/MICROSAR/DoIPInt/DoIPIntConfigSet/DoIPIntConnections/DoIPIntClientConnection`
  - `/MICROSAR/DoIPInt/DoIPIntConfigSet/DoIPIntConnections/DoIPIntServerConnection`
- **描述**: Reference to the dedicated client or server connections the Tx buffer is used for.
In case a reference exists this buffer is reserved for the dedicated connections.
In case no reference exists the buffer can be used for transmission on any connection.

######### 2. DoIPIntOemPayloadRxBuffer

**容器属性**:

- **UUID**: `bc8415da-bf7a-45a8-ad07-6e3521c2ac10`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPIntOemPayloadRxBuffer`
- **多重性**: [0..65535]
- **需要索引**: false

**容器描述**:

This container provides parameter to configure an Rx buffer which is used for messages with OEM payload type.

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. DoIPIntOemPayloadRxBufferSize

- **UUID**: `1d8558d1-51cc-4ddf-9a1f-fb2771298293`
- **参数名**: `DoIPIntOemPayloadRxBufferSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `1500`
- **取值范围**: [1..65535]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: This parameter defines the size of the Rx buffer for OEM payload type.

########## 引用关系

此容器包含 **1** 个引用：

########### CHOICE-REFERENCE 类型引用

############ 1. DoIPIntOemPayloadRxBufferClientOrServerConnectionRef

- **UUID**: `5cbe8d6c-37c2-4da0-9a2b-43fa02d9451d`
- **引用名**: `DoIPIntOemPayloadRxBufferClientOrServerConnectionRef`
- **引用类型**: CHOICE-REFERENCE
- **多重性**: [0..65535]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **需要索引**: false
- **目标引用列表**:
  - `/MICROSAR/DoIPInt/DoIPIntConfigSet/DoIPIntConnections/DoIPIntClientConnection`
  - `/MICROSAR/DoIPInt/DoIPIntConfigSet/DoIPIntConnections/DoIPIntServerConnection`
- **描述**: Reference to the dedicated client or server connections the Rx buffer is used for.
In case a reference exists this buffer is reserved for the dedicated connections.
In case no reference exists the buffer can be used for reception on any connection.

####### 14. DoIPIntOemPayloadTxBuffer

**容器属性**:

- **UUID**: `086e0c4b-72d1-4b91-aae0-cc18088ce3eb`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPIntOemPayloadTxBuffer`
- **多重性**: [0..65535]
- **需要索引**: false

**容器描述**:

This container provides parameter to configure a Tx buffer which is used for messages with OEM payload type.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. DoIPIntOemPayloadTxBufferSize

- **UUID**: `a15e1c33-c06c-43ee-8c4d-372c01928a9b`
- **参数名**: `DoIPIntOemPayloadTxBufferSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `1500`
- **取值范围**: [1..65535]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: This parameter defines the size of the Tx buffer for OEM payload type.

######## 引用关系

此容器包含 **1** 个引用：

######### CHOICE-REFERENCE 类型引用

########## 1. DoIPIntOemPayloadTxBufferClientOrServerConnectionRef

- **UUID**: `a778d695-a018-47dc-8f33-043b038eded0`
- **引用名**: `DoIPIntOemPayloadTxBufferClientOrServerConnectionRef`
- **引用类型**: CHOICE-REFERENCE
- **多重性**: [0..65535]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **需要索引**: false
- **目标引用列表**:
  - `/MICROSAR/DoIPInt/DoIPIntConfigSet/DoIPIntConnections/DoIPIntClientConnection`
  - `/MICROSAR/DoIPInt/DoIPIntConfigSet/DoIPIntConnections/DoIPIntServerConnection`
- **描述**: Reference to the dedicated client or server connections the Tx buffer is used for.
In case a reference exists this buffer is reserved for the dedicated connections.
In case no reference exists the buffer can be used for transmission on any connection.

####### 15. DoIPIntOemPayloadRxBuffer

**容器属性**:

- **UUID**: `bc8415da-bf7a-45a8-ad07-6e3521c2ac10`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPIntOemPayloadRxBuffer`
- **多重性**: [0..65535]
- **需要索引**: false

**容器描述**:

This container provides parameter to configure an Rx buffer which is used for messages with OEM payload type.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. DoIPIntOemPayloadRxBufferSize

- **UUID**: `1d8558d1-51cc-4ddf-9a1f-fb2771298293`
- **参数名**: `DoIPIntOemPayloadRxBufferSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `1500`
- **取值范围**: [1..65535]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: This parameter defines the size of the Rx buffer for OEM payload type.

######## 引用关系

此容器包含 **1** 个引用：

######### CHOICE-REFERENCE 类型引用

########## 1. DoIPIntOemPayloadRxBufferClientOrServerConnectionRef

- **UUID**: `5cbe8d6c-37c2-4da0-9a2b-43fa02d9451d`
- **引用名**: `DoIPIntOemPayloadRxBufferClientOrServerConnectionRef`
- **引用类型**: CHOICE-REFERENCE
- **多重性**: [0..65535]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **需要索引**: false
- **目标引用列表**:
  - `/MICROSAR/DoIPInt/DoIPIntConfigSet/DoIPIntConnections/DoIPIntClientConnection`
  - `/MICROSAR/DoIPInt/DoIPIntConfigSet/DoIPIntConnections/DoIPIntServerConnection`
- **描述**: Reference to the dedicated client or server connections the Rx buffer is used for.
In case a reference exists this buffer is reserved for the dedicated connections.
In case no reference exists the buffer can be used for reception on any connection.

##### 2. DoIPIntChannel

**容器属性**:

- **UUID**: `1a565ba0-1477-4dc6-a66e-3305a8158c40`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPIntChannel`
- **多重性**: [1..65535]
- **需要索引**: false

**容器描述**:

This container includes the configuration to describe the link to the upper layer PDUR module,

###### 参数配置

此容器包含 **2** 个参数：

####### INTEGER 类型参数

######## 1. DoIPIntChannelId

- **UUID**: `48ab7ba3-0ae2-458c-b040-6ec9c10d9291`
- **参数名**: `DoIPIntChannelId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65534]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: true
- **需要索引**: false
- **描述**: This parameter defines the Channel ID required for API calls using channels (e.g. DoIPInt_OverwriteLogicalAddresses()).

####### BOOLEAN 类型参数

######## 1. DoIPIntChannelReadyNotification

- **UUID**: `6244e7ff-f139-463e-9fe7-a4ca8c73d958`
- **参数名**: `DoIPIntChannelReadyNotification`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: This parameter defines whether this channel is related to the channel ready notification.
true:	BswM is notified when a TCP connection establishment succeeded.
false:	BswM is not notified.

###### 引用关系

此容器包含 **3** 个引用：

####### REFERENCE 类型引用

######## 1. DoIPIntLocalAddressRef

- **UUID**: `a26c4642-037c-4daa-8000-d2013081bfa8`
- **引用名**: `DoIPIntLocalAddressRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `DoIPIntLocalAddress`
- **完整路径**: `/MICROSAR/DoIPInt/DoIPIntConfigSet/DoIPIntLocalAddress`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **需要索引**: false
- **描述**: Reference to a DoIPIntLocalAddress which is used as logical address in diagnostic messages (e.g. as source address in case of transmission).

######## 2. DoIPIntRemoteAddressRef

- **UUID**: `bf045da4-e906-4e2e-9e9f-372831d9c899`
- **引用名**: `DoIPIntRemoteAddressRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `DoIPIntRemoteAddress`
- **完整路径**: `/MICROSAR/DoIPInt/DoIPIntConfigSet/DoIPIntRemoteAddress`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **需要索引**: false
- **描述**: Reference to a DoIPIntRemoteAddress which is used as logical address in diagnostic messages (e.g. as target address in case of transmission).

####### CHOICE-REFERENCE 类型引用

######## 1. DoIPIntClientOrServerConnectionRef

- **UUID**: `5deac71a-8c1c-4afb-84e1-8a98d1e244a9`
- **引用名**: `DoIPIntClientOrServerConnectionRef`
- **引用类型**: CHOICE-REFERENCE
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **需要索引**: false
- **目标引用列表**:
  - `/MICROSAR/DoIPInt/DoIPIntConfigSet/DoIPIntConnections/DoIPIntClientConnection`
  - `/MICROSAR/DoIPInt/DoIPIntConfigSet/DoIPIntConnections/DoIPIntServerConnection`
- **描述**: Reference to the DoIPIntClientConnection or DoIPIntServerConnection which is used to send or receive data for this channel.

###### 配置容器

本模块包含 **2** 个配置容器：

####### 1. DoIPIntPduRRxPdu

**容器属性**:

- **UUID**: `a226f39a-9abd-45ed-8bf1-a586d00c5571`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPIntPduRRxPdu`
- **多重性**: [0..1]
- **需要索引**: false

**容器描述**:

This container contains the Rx Pdu for the channel.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. DoIPIntPduRRxPduId

- **UUID**: `b36fa7eb-195a-4c81-9752-a7b6fab9aa09`
- **参数名**: `DoIPIntPduRRxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: true
- **需要索引**: false
- **描述**: This parameter defines the Pdu ID required for  the TP API calls. (e.g. DoIPInt_TpCancelReceive()) to handle reception to PDUR.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. DoIPIntPduRRxPduRef

- **UUID**: `7715c382-31e9-49fd-a4c3-3f601957209d`
- **引用名**: `DoIPIntPduRRxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **需要索引**: false
- **描述**: Reference to the "global" Pdu structure to allow harmonization of handle IDs in the COM-Stack.

####### 2. DoIPIntPduRTxPdu

**容器属性**:

- **UUID**: `becefe37-757a-43a7-9eef-22d6ed6cdcd6`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPIntPduRTxPdu`
- **多重性**: [0..1]
- **需要索引**: false

**容器描述**:

This container contains the Tx Pdu for the channel

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. DoIPIntPduRTxPduId

- **UUID**: `494601eb-0f3e-4e95-8211-bc440159aba3`
- **参数名**: `DoIPIntPduRTxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: true
- **需要索引**: false
- **描述**: This parameter defines the Pdu ID required for the TP and IF API calls. (e.g. DoIPInt_TpTransmit()) to send data from PDUR.

######### ENUMERATION 类型参数

########## 1. DoIPIntPduType

- **UUID**: `e3e74d75-b8c6-4919-912f-2c6bc2c2565c`
- **参数名**: `DoIPIntPduType`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `DOIPINT_TPPDU`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `DOIPINT_IFPDU` (来源: Vector Informatik)
  - `DOIPINT_TPPDU` (来源: Vector Informatik)
- **描述**: This parameter defines the API Type to use for communication with PduR.
DOIPINT_IFPDU for UUDT messages,
DOIPINT_TPPDU for all other diagnostic messages.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. DoIPIntPduRTxPduRef

- **UUID**: `896e01a8-59fb-4a8c-a965-4a1ad38f0a6a`
- **引用名**: `DoIPIntPduRTxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **需要索引**: false
- **描述**: Reference to the "global" Pdu structure to allow harmonization of handle IDs in the COM-Stack.

##### 3. DoIPIntPduRRxPdu

**容器属性**:

- **UUID**: `a226f39a-9abd-45ed-8bf1-a586d00c5571`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPIntPduRRxPdu`
- **多重性**: [0..1]
- **需要索引**: false

**容器描述**:

This container contains the Rx Pdu for the channel.

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. DoIPIntPduRRxPduId

- **UUID**: `b36fa7eb-195a-4c81-9752-a7b6fab9aa09`
- **参数名**: `DoIPIntPduRRxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: true
- **需要索引**: false
- **描述**: This parameter defines the Pdu ID required for  the TP API calls. (e.g. DoIPInt_TpCancelReceive()) to handle reception to PDUR.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. DoIPIntPduRRxPduRef

- **UUID**: `7715c382-31e9-49fd-a4c3-3f601957209d`
- **引用名**: `DoIPIntPduRRxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **需要索引**: false
- **描述**: Reference to the "global" Pdu structure to allow harmonization of handle IDs in the COM-Stack.

##### 4. DoIPIntPduRTxPdu

**容器属性**:

- **UUID**: `becefe37-757a-43a7-9eef-22d6ed6cdcd6`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPIntPduRTxPdu`
- **多重性**: [0..1]
- **需要索引**: false

**容器描述**:

This container contains the Tx Pdu for the channel

###### 参数配置

此容器包含 **2** 个参数：

####### INTEGER 类型参数

######## 1. DoIPIntPduRTxPduId

- **UUID**: `494601eb-0f3e-4e95-8211-bc440159aba3`
- **参数名**: `DoIPIntPduRTxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: true
- **需要索引**: false
- **描述**: This parameter defines the Pdu ID required for the TP and IF API calls. (e.g. DoIPInt_TpTransmit()) to send data from PDUR.

####### ENUMERATION 类型参数

######## 1. DoIPIntPduType

- **UUID**: `e3e74d75-b8c6-4919-912f-2c6bc2c2565c`
- **参数名**: `DoIPIntPduType`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `DOIPINT_TPPDU`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `DOIPINT_IFPDU` (来源: Vector Informatik)
  - `DOIPINT_TPPDU` (来源: Vector Informatik)
- **描述**: This parameter defines the API Type to use for communication with PduR.
DOIPINT_IFPDU for UUDT messages,
DOIPINT_TPPDU for all other diagnostic messages.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. DoIPIntPduRTxPduRef

- **UUID**: `896e01a8-59fb-4a8c-a965-4a1ad38f0a6a`
- **引用名**: `DoIPIntPduRTxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **需要索引**: false
- **描述**: Reference to the "global" Pdu structure to allow harmonization of handle IDs in the COM-Stack.

##### 5. DoIPIntConnections

**容器属性**:

- **UUID**: `1cab9af2-e698-4c6a-b015-6bf7288cfab3`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPIntConnections`
- **多重性**: [1..1]
- **需要索引**: false

**容器描述**:

This container contains the connections to the lower layer SOAD module.

###### 配置容器

本模块包含 **6** 个配置容器：

####### 1. DoIPIntClientConnection

**容器属性**:

- **UUID**: `1502115f-5545-4109-8380-b41a3b2156c5`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPIntClientConnection`
- **多重性**: [0..32767]
- **需要索引**: false

**容器描述**:

This container includes the connection configuration to the lower layer SOAD module for TCP client connections.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. DoIPIntClientConnectionId

- **UUID**: `31afe52b-a3ba-404c-bc9e-3198d47041eb`
- **参数名**: `DoIPIntClientConnectionId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: true
- **需要索引**: false
- **描述**: This parameter gives a unique identifier for client and server connections required for API calls using connections (e.g. DoIPInt_CloseConnection(), DoIPInt_TransmitOemSpecificPayloadType()).

######## 配置容器

本模块包含 **2** 个配置容器：

######### 1. DoIPIntClientSoAdRxPdu

**容器属性**:

- **UUID**: `84c99d8a-bc48-4173-943c-e65e266bb923`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPIntClientSoAdRxPdu`
- **多重性**: [1..1]
- **需要索引**: false

**容器描述**:

This container contains the Rx Pdu for the TCP connection.

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. DoIPIntClientSoAdRxPduId

- **UUID**: `4ff1698b-b980-4a5e-813a-8c3a8ea2e0ab`
- **参数名**: `DoIPIntClientSoAdRxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: true
- **需要索引**: false
- **描述**: This parameter defines the Pdu ID required for  the TP API calls. (e.g. DoIPInt_SoAdTpRxIndication()) to receive TCP data from SOAD.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. DoIPIntClientSoAdRxPduRef

- **UUID**: `50b41288-42e4-420c-818c-f9438594af8c`
- **引用名**: `DoIPIntClientSoAdRxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **需要索引**: false
- **描述**: Reference to the "global" Pdu structure to allow harmonization of handle IDs in the COM-Stack.

######### 2. DoIPIntClientSoAdTxPdu

**容器属性**:

- **UUID**: `957a7f2b-faab-4637-9916-9520f08e600e`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPIntClientSoAdTxPdu`
- **多重性**: [1..1]
- **需要索引**: false

**容器描述**:

This container contains the Tx Pdu for the TCP connection.

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. DoIPIntClientSoAdTxPduId

- **UUID**: `547ab530-1838-4ecd-bb38-6a3e6f64d404`
- **参数名**: `DoIPIntClientSoAdTxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: true
- **需要索引**: false
- **描述**: This parameter defines the Pdu ID required for  the TP API calls. (e.g. DoIPInt_SoAdTpTxConfirmation()) to confirm TCP data from SOAD.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. DoIPIntClientSoAdTxPduRef

- **UUID**: `ac9aac90-c75f-4d1b-b6bb-11398ee19b5d`
- **引用名**: `DoIPIntClientSoAdTxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **需要索引**: false
- **描述**: Reference to the "global" Pdu structure to allow harmonization of handle IDs in the COM-Stack.

####### 2. DoIPIntClientSoAdRxPdu

**容器属性**:

- **UUID**: `84c99d8a-bc48-4173-943c-e65e266bb923`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPIntClientSoAdRxPdu`
- **多重性**: [1..1]
- **需要索引**: false

**容器描述**:

This container contains the Rx Pdu for the TCP connection.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. DoIPIntClientSoAdRxPduId

- **UUID**: `4ff1698b-b980-4a5e-813a-8c3a8ea2e0ab`
- **参数名**: `DoIPIntClientSoAdRxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: true
- **需要索引**: false
- **描述**: This parameter defines the Pdu ID required for  the TP API calls. (e.g. DoIPInt_SoAdTpRxIndication()) to receive TCP data from SOAD.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. DoIPIntClientSoAdRxPduRef

- **UUID**: `50b41288-42e4-420c-818c-f9438594af8c`
- **引用名**: `DoIPIntClientSoAdRxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **需要索引**: false
- **描述**: Reference to the "global" Pdu structure to allow harmonization of handle IDs in the COM-Stack.

####### 3. DoIPIntClientSoAdTxPdu

**容器属性**:

- **UUID**: `957a7f2b-faab-4637-9916-9520f08e600e`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPIntClientSoAdTxPdu`
- **多重性**: [1..1]
- **需要索引**: false

**容器描述**:

This container contains the Tx Pdu for the TCP connection.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. DoIPIntClientSoAdTxPduId

- **UUID**: `547ab530-1838-4ecd-bb38-6a3e6f64d404`
- **参数名**: `DoIPIntClientSoAdTxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: true
- **需要索引**: false
- **描述**: This parameter defines the Pdu ID required for  the TP API calls. (e.g. DoIPInt_SoAdTpTxConfirmation()) to confirm TCP data from SOAD.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. DoIPIntClientSoAdTxPduRef

- **UUID**: `ac9aac90-c75f-4d1b-b6bb-11398ee19b5d`
- **引用名**: `DoIPIntClientSoAdTxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **需要索引**: false
- **描述**: Reference to the "global" Pdu structure to allow harmonization of handle IDs in the COM-Stack.

####### 4. DoIPIntServerConnection

**容器属性**:

- **UUID**: `83411892-40f2-4935-8b1e-dc2278037c82`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPIntServerConnection`
- **多重性**: [0..32767]
- **需要索引**: false

**容器描述**:

This container includes the connection configuration to the lower layer SOAD module for TCP server connections.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. DoIPIntServerConnectionId

- **UUID**: `81a9d93c-5c64-4d3a-8d9e-1b6d2f15c425`
- **参数名**: `DoIPIntServerConnectionId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: true
- **需要索引**: false
- **描述**: This parameter gives a unique identifier for client and server connections required for API calls using connections (e.g. DoIPInt_CloseConnection(), DoIPInt_TransmitOemSpecificPayloadType()).

######## 配置容器

本模块包含 **2** 个配置容器：

######### 1. DoIPIntServerSoAdRxPdu

**容器属性**:

- **UUID**: `4d120950-9c0f-4de4-80e7-3941acb8d328`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPIntServerSoAdRxPdu`
- **多重性**: [1..1]
- **需要索引**: false

**容器描述**:

This container contains the Rx Pdu for the TCP connection.

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. DoIPIntServerSoAdRxPduId

- **UUID**: `6650d417-9186-4013-8609-f18f8a1bbd69`
- **参数名**: `DoIPIntServerSoAdRxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: true
- **需要索引**: false
- **描述**: This parameter defines the Pdu ID required for  the TP API calls. (e.g. DoIPInt_SoAdTpRxIndication()) to receive TCP data from SOAD.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. DoIPIntServerSoAdRxPduRef

- **UUID**: `8792e6a7-8961-4d9b-8d71-6fc9952c3035`
- **引用名**: `DoIPIntServerSoAdRxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **需要索引**: false
- **描述**: Reference to the "global" Pdu structure to allow harmonization of handle IDs in the COM-Stack.

######### 2. DoIPIntServerSoAdTxPdu

**容器属性**:

- **UUID**: `15ffffe8-cbcf-455f-8529-9b63af6e3bf1`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPIntServerSoAdTxPdu`
- **多重性**: [1..1]
- **需要索引**: false

**容器描述**:

This container contains the Tx Pdu for the TCP connection.

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. DoIPIntServerSoAdTxPduId

- **UUID**: `a5e8e43a-9ddb-490a-8fe6-1c1812db9fdb`
- **参数名**: `DoIPIntServerSoAdTxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: true
- **需要索引**: false
- **描述**: This parameter defines the Pdu ID required for  the TP API calls. (e.g. DoIPInt_SoAdTpTxConfirmation()) to confirm TCP data from SOAD.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. DoIPIntServerSoAdTxPduRef

- **UUID**: `353ccf8e-3839-4cd9-aa20-a437a5daa19f`
- **引用名**: `DoIPIntServerSoAdTxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **需要索引**: false
- **描述**: Reference to the "global" Pdu structure to allow harmonization of handle IDs in the COM-Stack.

####### 5. DoIPIntServerSoAdRxPdu

**容器属性**:

- **UUID**: `4d120950-9c0f-4de4-80e7-3941acb8d328`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPIntServerSoAdRxPdu`
- **多重性**: [1..1]
- **需要索引**: false

**容器描述**:

This container contains the Rx Pdu for the TCP connection.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. DoIPIntServerSoAdRxPduId

- **UUID**: `6650d417-9186-4013-8609-f18f8a1bbd69`
- **参数名**: `DoIPIntServerSoAdRxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: true
- **需要索引**: false
- **描述**: This parameter defines the Pdu ID required for  the TP API calls. (e.g. DoIPInt_SoAdTpRxIndication()) to receive TCP data from SOAD.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. DoIPIntServerSoAdRxPduRef

- **UUID**: `8792e6a7-8961-4d9b-8d71-6fc9952c3035`
- **引用名**: `DoIPIntServerSoAdRxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **需要索引**: false
- **描述**: Reference to the "global" Pdu structure to allow harmonization of handle IDs in the COM-Stack.

####### 6. DoIPIntServerSoAdTxPdu

**容器属性**:

- **UUID**: `15ffffe8-cbcf-455f-8529-9b63af6e3bf1`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPIntServerSoAdTxPdu`
- **多重性**: [1..1]
- **需要索引**: false

**容器描述**:

This container contains the Tx Pdu for the TCP connection.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. DoIPIntServerSoAdTxPduId

- **UUID**: `a5e8e43a-9ddb-490a-8fe6-1c1812db9fdb`
- **参数名**: `DoIPIntServerSoAdTxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: true
- **需要索引**: false
- **描述**: This parameter defines the Pdu ID required for  the TP API calls. (e.g. DoIPInt_SoAdTpTxConfirmation()) to confirm TCP data from SOAD.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. DoIPIntServerSoAdTxPduRef

- **UUID**: `353ccf8e-3839-4cd9-aa20-a437a5daa19f`
- **引用名**: `DoIPIntServerSoAdTxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **需要索引**: false
- **描述**: Reference to the "global" Pdu structure to allow harmonization of handle IDs in the COM-Stack.

##### 6. DoIPIntClientConnection

**容器属性**:

- **UUID**: `1502115f-5545-4109-8380-b41a3b2156c5`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPIntClientConnection`
- **多重性**: [0..32767]
- **需要索引**: false

**容器描述**:

This container includes the connection configuration to the lower layer SOAD module for TCP client connections.

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. DoIPIntClientConnectionId

- **UUID**: `31afe52b-a3ba-404c-bc9e-3198d47041eb`
- **参数名**: `DoIPIntClientConnectionId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: true
- **需要索引**: false
- **描述**: This parameter gives a unique identifier for client and server connections required for API calls using connections (e.g. DoIPInt_CloseConnection(), DoIPInt_TransmitOemSpecificPayloadType()).

###### 配置容器

本模块包含 **2** 个配置容器：

####### 1. DoIPIntClientSoAdRxPdu

**容器属性**:

- **UUID**: `84c99d8a-bc48-4173-943c-e65e266bb923`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPIntClientSoAdRxPdu`
- **多重性**: [1..1]
- **需要索引**: false

**容器描述**:

This container contains the Rx Pdu for the TCP connection.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. DoIPIntClientSoAdRxPduId

- **UUID**: `4ff1698b-b980-4a5e-813a-8c3a8ea2e0ab`
- **参数名**: `DoIPIntClientSoAdRxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: true
- **需要索引**: false
- **描述**: This parameter defines the Pdu ID required for  the TP API calls. (e.g. DoIPInt_SoAdTpRxIndication()) to receive TCP data from SOAD.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. DoIPIntClientSoAdRxPduRef

- **UUID**: `50b41288-42e4-420c-818c-f9438594af8c`
- **引用名**: `DoIPIntClientSoAdRxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **需要索引**: false
- **描述**: Reference to the "global" Pdu structure to allow harmonization of handle IDs in the COM-Stack.

####### 2. DoIPIntClientSoAdTxPdu

**容器属性**:

- **UUID**: `957a7f2b-faab-4637-9916-9520f08e600e`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPIntClientSoAdTxPdu`
- **多重性**: [1..1]
- **需要索引**: false

**容器描述**:

This container contains the Tx Pdu for the TCP connection.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. DoIPIntClientSoAdTxPduId

- **UUID**: `547ab530-1838-4ecd-bb38-6a3e6f64d404`
- **参数名**: `DoIPIntClientSoAdTxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: true
- **需要索引**: false
- **描述**: This parameter defines the Pdu ID required for  the TP API calls. (e.g. DoIPInt_SoAdTpTxConfirmation()) to confirm TCP data from SOAD.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. DoIPIntClientSoAdTxPduRef

- **UUID**: `ac9aac90-c75f-4d1b-b6bb-11398ee19b5d`
- **引用名**: `DoIPIntClientSoAdTxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **需要索引**: false
- **描述**: Reference to the "global" Pdu structure to allow harmonization of handle IDs in the COM-Stack.

##### 7. DoIPIntClientSoAdRxPdu

**容器属性**:

- **UUID**: `84c99d8a-bc48-4173-943c-e65e266bb923`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPIntClientSoAdRxPdu`
- **多重性**: [1..1]
- **需要索引**: false

**容器描述**:

This container contains the Rx Pdu for the TCP connection.

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. DoIPIntClientSoAdRxPduId

- **UUID**: `4ff1698b-b980-4a5e-813a-8c3a8ea2e0ab`
- **参数名**: `DoIPIntClientSoAdRxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: true
- **需要索引**: false
- **描述**: This parameter defines the Pdu ID required for  the TP API calls. (e.g. DoIPInt_SoAdTpRxIndication()) to receive TCP data from SOAD.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. DoIPIntClientSoAdRxPduRef

- **UUID**: `50b41288-42e4-420c-818c-f9438594af8c`
- **引用名**: `DoIPIntClientSoAdRxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **需要索引**: false
- **描述**: Reference to the "global" Pdu structure to allow harmonization of handle IDs in the COM-Stack.

##### 8. DoIPIntClientSoAdTxPdu

**容器属性**:

- **UUID**: `957a7f2b-faab-4637-9916-9520f08e600e`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPIntClientSoAdTxPdu`
- **多重性**: [1..1]
- **需要索引**: false

**容器描述**:

This container contains the Tx Pdu for the TCP connection.

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. DoIPIntClientSoAdTxPduId

- **UUID**: `547ab530-1838-4ecd-bb38-6a3e6f64d404`
- **参数名**: `DoIPIntClientSoAdTxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: true
- **需要索引**: false
- **描述**: This parameter defines the Pdu ID required for  the TP API calls. (e.g. DoIPInt_SoAdTpTxConfirmation()) to confirm TCP data from SOAD.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. DoIPIntClientSoAdTxPduRef

- **UUID**: `ac9aac90-c75f-4d1b-b6bb-11398ee19b5d`
- **引用名**: `DoIPIntClientSoAdTxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **需要索引**: false
- **描述**: Reference to the "global" Pdu structure to allow harmonization of handle IDs in the COM-Stack.

##### 9. DoIPIntServerConnection

**容器属性**:

- **UUID**: `83411892-40f2-4935-8b1e-dc2278037c82`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPIntServerConnection`
- **多重性**: [0..32767]
- **需要索引**: false

**容器描述**:

This container includes the connection configuration to the lower layer SOAD module for TCP server connections.

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. DoIPIntServerConnectionId

- **UUID**: `81a9d93c-5c64-4d3a-8d9e-1b6d2f15c425`
- **参数名**: `DoIPIntServerConnectionId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: true
- **需要索引**: false
- **描述**: This parameter gives a unique identifier for client and server connections required for API calls using connections (e.g. DoIPInt_CloseConnection(), DoIPInt_TransmitOemSpecificPayloadType()).

###### 配置容器

本模块包含 **2** 个配置容器：

####### 1. DoIPIntServerSoAdRxPdu

**容器属性**:

- **UUID**: `4d120950-9c0f-4de4-80e7-3941acb8d328`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPIntServerSoAdRxPdu`
- **多重性**: [1..1]
- **需要索引**: false

**容器描述**:

This container contains the Rx Pdu for the TCP connection.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. DoIPIntServerSoAdRxPduId

- **UUID**: `6650d417-9186-4013-8609-f18f8a1bbd69`
- **参数名**: `DoIPIntServerSoAdRxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: true
- **需要索引**: false
- **描述**: This parameter defines the Pdu ID required for  the TP API calls. (e.g. DoIPInt_SoAdTpRxIndication()) to receive TCP data from SOAD.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. DoIPIntServerSoAdRxPduRef

- **UUID**: `8792e6a7-8961-4d9b-8d71-6fc9952c3035`
- **引用名**: `DoIPIntServerSoAdRxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **需要索引**: false
- **描述**: Reference to the "global" Pdu structure to allow harmonization of handle IDs in the COM-Stack.

####### 2. DoIPIntServerSoAdTxPdu

**容器属性**:

- **UUID**: `15ffffe8-cbcf-455f-8529-9b63af6e3bf1`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPIntServerSoAdTxPdu`
- **多重性**: [1..1]
- **需要索引**: false

**容器描述**:

This container contains the Tx Pdu for the TCP connection.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. DoIPIntServerSoAdTxPduId

- **UUID**: `a5e8e43a-9ddb-490a-8fe6-1c1812db9fdb`
- **参数名**: `DoIPIntServerSoAdTxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: true
- **需要索引**: false
- **描述**: This parameter defines the Pdu ID required for  the TP API calls. (e.g. DoIPInt_SoAdTpTxConfirmation()) to confirm TCP data from SOAD.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. DoIPIntServerSoAdTxPduRef

- **UUID**: `353ccf8e-3839-4cd9-aa20-a437a5daa19f`
- **引用名**: `DoIPIntServerSoAdTxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **需要索引**: false
- **描述**: Reference to the "global" Pdu structure to allow harmonization of handle IDs in the COM-Stack.

##### 10. DoIPIntServerSoAdRxPdu

**容器属性**:

- **UUID**: `4d120950-9c0f-4de4-80e7-3941acb8d328`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPIntServerSoAdRxPdu`
- **多重性**: [1..1]
- **需要索引**: false

**容器描述**:

This container contains the Rx Pdu for the TCP connection.

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. DoIPIntServerSoAdRxPduId

- **UUID**: `6650d417-9186-4013-8609-f18f8a1bbd69`
- **参数名**: `DoIPIntServerSoAdRxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: true
- **需要索引**: false
- **描述**: This parameter defines the Pdu ID required for  the TP API calls. (e.g. DoIPInt_SoAdTpRxIndication()) to receive TCP data from SOAD.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. DoIPIntServerSoAdRxPduRef

- **UUID**: `8792e6a7-8961-4d9b-8d71-6fc9952c3035`
- **引用名**: `DoIPIntServerSoAdRxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **需要索引**: false
- **描述**: Reference to the "global" Pdu structure to allow harmonization of handle IDs in the COM-Stack.

##### 11. DoIPIntServerSoAdTxPdu

**容器属性**:

- **UUID**: `15ffffe8-cbcf-455f-8529-9b63af6e3bf1`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPIntServerSoAdTxPdu`
- **多重性**: [1..1]
- **需要索引**: false

**容器描述**:

This container contains the Tx Pdu for the TCP connection.

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. DoIPIntServerSoAdTxPduId

- **UUID**: `a5e8e43a-9ddb-490a-8fe6-1c1812db9fdb`
- **参数名**: `DoIPIntServerSoAdTxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: true
- **需要索引**: false
- **描述**: This parameter defines the Pdu ID required for  the TP API calls. (e.g. DoIPInt_SoAdTpTxConfirmation()) to confirm TCP data from SOAD.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. DoIPIntServerSoAdTxPduRef

- **UUID**: `353ccf8e-3839-4cd9-aa20-a437a5daa19f`
- **引用名**: `DoIPIntServerSoAdTxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **需要索引**: false
- **描述**: Reference to the "global" Pdu structure to allow harmonization of handle IDs in the COM-Stack.

##### 12. DoIPIntRemoteAddress

**容器属性**:

- **UUID**: `73fb2f4c-5ea1-475e-a693-82e97ce1bced`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPIntRemoteAddress`
- **多重性**: [1..65535]
- **需要索引**: false

**容器描述**:

This container defines the logical remote address which is used in the diagnostic messages (e.g. as target address in case of transmission).

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. DoIPIntRemoteAddressValue

- **UUID**: `de8f8185-16e8-43ae-88bd-4109741fb234`
- **参数名**: `DoIPIntRemoteAddressValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: This parameter defines the logical remote address which is sent within diagnostic messages.

##### 13. DoIPIntLocalAddress

**容器属性**:

- **UUID**: `999c06e3-1d7e-4945-8607-fdf3d308791b`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPIntLocalAddress`
- **多重性**: [1..65535]
- **需要索引**: false

**容器描述**:

This container defines the logical local address which is used in the diagnostic messages (e.g. as source address in case of transmission).

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. DoIPIntLocalAddressValue

- **UUID**: `526bdd13-e346-430a-a8bc-54c6981242d3`
- **参数名**: `DoIPIntLocalAddressValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: This parameter defines the logical local address which is sent within diagnostic messages.

##### 14. DoIPIntOemPayload

**容器属性**:

- **UUID**: `565919a0-5eb1-4a2b-97f3-3761451716ab`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPIntOemPayload`
- **多重性**: [0..1]
- **需要索引**: false

**容器描述**:

This container defines parameter (Tx/Rx buffer and callback configuration) for OEM payload type messages.

###### 参数配置

此容器包含 **1** 个参数：

####### FUNCTION-NAME 类型参数

######## 1. DoIPIntOemPayloadRxCallback

- **UUID**: `8cc3a758-b519-4d01-9e95-dd89c5c6c060`
- **参数名**: `DoIPIntOemPayloadRxCallback`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **函数变体**:
  - 默认值: `Appl_DoIPInt_ReceiveOemSpecificPayloadType`
- **描述**: This parameter defines a callback function to forward received manufacturer-specific payload types to a user via <User>_DoIPIntReceiveOemSpecificPayloadType.

Note: In case no DoIPIntOemPayloadRxBuffer is configured which can be used for a connection no reception of OEM specific messages is supported on this connection and the reception of the message is skipped.

###### 配置容器

本模块包含 **2** 个配置容器：

####### 1. DoIPIntOemPayloadTxBuffer

**容器属性**:

- **UUID**: `086e0c4b-72d1-4b91-aae0-cc18088ce3eb`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPIntOemPayloadTxBuffer`
- **多重性**: [0..65535]
- **需要索引**: false

**容器描述**:

This container provides parameter to configure a Tx buffer which is used for messages with OEM payload type.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. DoIPIntOemPayloadTxBufferSize

- **UUID**: `a15e1c33-c06c-43ee-8c4d-372c01928a9b`
- **参数名**: `DoIPIntOemPayloadTxBufferSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `1500`
- **取值范围**: [1..65535]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: This parameter defines the size of the Tx buffer for OEM payload type.

######## 引用关系

此容器包含 **1** 个引用：

######### CHOICE-REFERENCE 类型引用

########## 1. DoIPIntOemPayloadTxBufferClientOrServerConnectionRef

- **UUID**: `a778d695-a018-47dc-8f33-043b038eded0`
- **引用名**: `DoIPIntOemPayloadTxBufferClientOrServerConnectionRef`
- **引用类型**: CHOICE-REFERENCE
- **多重性**: [0..65535]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **需要索引**: false
- **目标引用列表**:
  - `/MICROSAR/DoIPInt/DoIPIntConfigSet/DoIPIntConnections/DoIPIntClientConnection`
  - `/MICROSAR/DoIPInt/DoIPIntConfigSet/DoIPIntConnections/DoIPIntServerConnection`
- **描述**: Reference to the dedicated client or server connections the Tx buffer is used for.
In case a reference exists this buffer is reserved for the dedicated connections.
In case no reference exists the buffer can be used for transmission on any connection.

####### 2. DoIPIntOemPayloadRxBuffer

**容器属性**:

- **UUID**: `bc8415da-bf7a-45a8-ad07-6e3521c2ac10`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPIntOemPayloadRxBuffer`
- **多重性**: [0..65535]
- **需要索引**: false

**容器描述**:

This container provides parameter to configure an Rx buffer which is used for messages with OEM payload type.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. DoIPIntOemPayloadRxBufferSize

- **UUID**: `1d8558d1-51cc-4ddf-9a1f-fb2771298293`
- **参数名**: `DoIPIntOemPayloadRxBufferSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `1500`
- **取值范围**: [1..65535]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: This parameter defines the size of the Rx buffer for OEM payload type.

######## 引用关系

此容器包含 **1** 个引用：

######### CHOICE-REFERENCE 类型引用

########## 1. DoIPIntOemPayloadRxBufferClientOrServerConnectionRef

- **UUID**: `5cbe8d6c-37c2-4da0-9a2b-43fa02d9451d`
- **引用名**: `DoIPIntOemPayloadRxBufferClientOrServerConnectionRef`
- **引用类型**: CHOICE-REFERENCE
- **多重性**: [0..65535]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **需要索引**: false
- **目标引用列表**:
  - `/MICROSAR/DoIPInt/DoIPIntConfigSet/DoIPIntConnections/DoIPIntClientConnection`
  - `/MICROSAR/DoIPInt/DoIPIntConfigSet/DoIPIntConnections/DoIPIntServerConnection`
- **描述**: Reference to the dedicated client or server connections the Rx buffer is used for.
In case a reference exists this buffer is reserved for the dedicated connections.
In case no reference exists the buffer can be used for reception on any connection.

##### 15. DoIPIntOemPayloadTxBuffer

**容器属性**:

- **UUID**: `086e0c4b-72d1-4b91-aae0-cc18088ce3eb`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPIntOemPayloadTxBuffer`
- **多重性**: [0..65535]
- **需要索引**: false

**容器描述**:

This container provides parameter to configure a Tx buffer which is used for messages with OEM payload type.

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. DoIPIntOemPayloadTxBufferSize

- **UUID**: `a15e1c33-c06c-43ee-8c4d-372c01928a9b`
- **参数名**: `DoIPIntOemPayloadTxBufferSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `1500`
- **取值范围**: [1..65535]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: This parameter defines the size of the Tx buffer for OEM payload type.

###### 引用关系

此容器包含 **1** 个引用：

####### CHOICE-REFERENCE 类型引用

######## 1. DoIPIntOemPayloadTxBufferClientOrServerConnectionRef

- **UUID**: `a778d695-a018-47dc-8f33-043b038eded0`
- **引用名**: `DoIPIntOemPayloadTxBufferClientOrServerConnectionRef`
- **引用类型**: CHOICE-REFERENCE
- **多重性**: [0..65535]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **需要索引**: false
- **目标引用列表**:
  - `/MICROSAR/DoIPInt/DoIPIntConfigSet/DoIPIntConnections/DoIPIntClientConnection`
  - `/MICROSAR/DoIPInt/DoIPIntConfigSet/DoIPIntConnections/DoIPIntServerConnection`
- **描述**: Reference to the dedicated client or server connections the Tx buffer is used for.
In case a reference exists this buffer is reserved for the dedicated connections.
In case no reference exists the buffer can be used for transmission on any connection.

##### 16. DoIPIntOemPayloadRxBuffer

**容器属性**:

- **UUID**: `bc8415da-bf7a-45a8-ad07-6e3521c2ac10`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPIntOemPayloadRxBuffer`
- **多重性**: [0..65535]
- **需要索引**: false

**容器描述**:

This container provides parameter to configure an Rx buffer which is used for messages with OEM payload type.

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. DoIPIntOemPayloadRxBufferSize

- **UUID**: `1d8558d1-51cc-4ddf-9a1f-fb2771298293`
- **参数名**: `DoIPIntOemPayloadRxBufferSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `1500`
- **取值范围**: [1..65535]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: This parameter defines the size of the Rx buffer for OEM payload type.

###### 引用关系

此容器包含 **1** 个引用：

####### CHOICE-REFERENCE 类型引用

######## 1. DoIPIntOemPayloadRxBufferClientOrServerConnectionRef

- **UUID**: `5cbe8d6c-37c2-4da0-9a2b-43fa02d9451d`
- **引用名**: `DoIPIntOemPayloadRxBufferClientOrServerConnectionRef`
- **引用类型**: CHOICE-REFERENCE
- **多重性**: [0..65535]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **需要索引**: false
- **目标引用列表**:
  - `/MICROSAR/DoIPInt/DoIPIntConfigSet/DoIPIntConnections/DoIPIntClientConnection`
  - `/MICROSAR/DoIPInt/DoIPIntConfigSet/DoIPIntConnections/DoIPIntServerConnection`
- **描述**: Reference to the dedicated client or server connections the Rx buffer is used for.
In case a reference exists this buffer is reserved for the dedicated connections.
In case no reference exists the buffer can be used for reception on any connection.

##### 17. DoIPIntGeneral

**容器属性**:

- **UUID**: `d15ce67e-47a1-47ae-8b93-8d0584eb7566`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPIntGeneral`
- **多重性**: [1..1]
- **需要索引**: false

**容器描述**:

This container contains general configuration parameters of the DoIPInt module.

###### 参数配置

此容器包含 **12** 个参数：

####### INTEGER 类型参数

######## 1. DoIPIntTxProcessLimit

- **UUID**: `886f2c86-a757-49d6-88a7-6bb8f5678d66`
- **参数名**: `DoIPIntTxProcessLimit`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `1`
- **取值范围**: [1..255]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: This parameter specifies how many transmission requests are processed in one main function cycle.
A value greater than 1 is only applicable if multiple transmission requests can be processed by SoAd (SoAdTxTpOptimized enabled).

######## 2. DoIPIntTxQueueSize

- **UUID**: `e5927f73-85f6-4e16-9ee3-258e7016e46f`
- **参数名**: `DoIPIntTxQueueSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `16`
- **取值范围**: [1..65535]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: This parameter specifies the maximum size of the transmission queue per connection.
The transmission queue stores the number of parallel transmission requests on a connection.
This parameter does not apply to a connection with a smaller number of DoIPIntChannels than the value specified by this parameter. In this case the number of DoIPIntChannels equals the size of the transmission queue.

######## 3. DoIPIntIfPayloadType

- **UUID**: `9ebbe2bf-af29-4d72-8a52-166bdf2cccea`
- **参数名**: `DoIPIntIfPayloadType`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `32769`
- **取值范围**: [0..65535]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: This parameter specifies which payload type shall be used for IF-PDUs.
This parameter is only applicable if an IF-PDU is configured and if ISO is used as DoIPIntHeaderStructure.

######## 4. DoIPIntProtocolVersion

- **UUID**: `69169280-f17c-48a4-bb29-7d11709d5d1b`
- **参数名**: `DoIPIntProtocolVersion`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `3`
- **取值范围**: [2..255]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: This value specifies the DoIP protocol version used in the generic DoIP header. The valid range of this parameter is defined by the always latest release of ISO 13400-2 and can be extended with every new release of the ISO document. As example a value of 0x03 defines the ISO 13400-2:2019 release.

Note: The version 0xFF should not be used as it is the default protocol version of the ISO.

####### BOOLEAN 类型参数

######## 1. DoIPIntDevErrorDetect

- **UUID**: `b9923213-b648-4250-9882-e635fbf75d33`
- **参数名**: `DoIPIntDevErrorDetect`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: This parameter switches the Development Error Detection and Notification ON or OFF.
true: Development error detection is enabled.
false: Development error detection is disabled.

Note: In general, the development error detection is recommended during pre-test phase. It is not recommended to enable the development error detection in production code due to increased runtime and ROM needs.

######## 2. DoIPIntSafeBswChecks

- **UUID**: `680fed39-26cd-4e36-83fb-7e84b7752c47`
- **参数名**: `DoIPIntSafeBswChecks`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Selects if safety checks are used. These checks improve robustness as e.g. invalid parameters are checked before function is executed. This attribute has to be enabled for safety projects where this component is mapped to an ASIL partition.

######## 3. DoIPIntVersionInfoApi

- **UUID**: `c1ec9fca-514d-485b-9652-bfdc3c2aeda2`
- **参数名**: `DoIPIntVersionInfoApi`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: This parameter activates/deactivates the DoIP_GetVersionInfo() API.

####### FLOAT 类型参数

######## 1. DoIPIntMainFunctionPeriod

- **UUID**: `98fe5a6d-32f3-4588-a654-4231712324ff`
- **参数名**: `DoIPIntMainFunctionPeriod`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `0.005`
- **取值范围**: [0..0.1]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: This parameter defines the main function call period.

######## 2. DoIPIntRxRetryTimeout

- **UUID**: `b06c3b53-5c12-41ef-91eb-9febb14489ba`
- **参数名**: `DoIPIntRxRetryTimeout`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `0.2`
- **取值范围**: [0.05..5]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: This parameter specifies the retry timeout which is used in two different reception contexts.
1. In case reception to user fails (PduR_DoIPIntTpStartOfReception() API).
The module retries the reception until the timeout elapses. The message is dropped as soon as the timeout has elapsed.
2. In case all applicable OEM specific reception buffers are currently in use.
The module retries getting a buffer until the timeout elapses. The message is dropped as soon as the timeout has elapsed.

####### STRING 类型参数

######## 1. DoIPIntUserConfigFile

- **UUID**: `60b4df06-ae0b-4d39-b7cf-95a55f83f337`
- **参数名**: `DoIPIntUserConfigFile`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **字符串变体**:
  - 最大长度: 255
  - 最小长度: 0
- **描述**: Reference to an external user configuration file that will be included during generation.
The content of the user configuration file will be added at the end of the generated module configuration file and allows altering or extending the generated code.
Caution: User configuration files can cause the software module to malfunction and must only be used with great care!

######## 2. DoIPIntApplicationHeaderFileInclusion

- **UUID**: `0b509ed9-bb07-498f-bdee-31465f0b1f82`
- **参数名**: `DoIPIntApplicationHeaderFileInclusion`
- **数据类型**: STRING
- **多重性**: [0..255]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **字符串变体**:
  - 最大长度: 255
  - 最小长度: 3
- **描述**: This parameter defines a list of header files to be included containing application specific functionality (e.g. for DoIPIntOemPayloadRxCallback configuration).
These header files are included in the SoAd_Lcfg.c file.

####### ENUMERATION 类型参数

######## 1. DoIPIntHeaderStructure

- **UUID**: `e18c94cd-d8d2-4d82-8245-eec1eb8c316d`
- **参数名**: `DoIPIntHeaderStructure`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `ISO`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `ISO` (来源: Vector Informatik)
  - `LIGHT` (来源: Vector Informatik)
- **描述**: This parameter specifies the header structure which is expected on reception and used on transmission.

ISO: Version | Inv. Version | Payload Type | Payload Length | Src. Address | Tgt. Address | User Data
LIGHT: Src. Address | Tgt. Address | Payload Length | User Data

###### 配置容器

本模块包含 **2** 个配置容器：

####### 1. DoIPIntGeneration

**容器属性**:

- **UUID**: `15043fa7-d6a4-4b2f-9cbf-d6c574e2ffcb`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPIntGeneration`
- **多重性**: [1..1]
- **需要索引**: false

**容器描述**:

This container contains parameters to change general generation behavior.

######## 参数配置

此容器包含 **16** 个参数：

######### INTEGER 类型参数

########## 1. DoIPIntReduceBoolDataByNegationThreshold

- **UUID**: `aff67abf-8fc7-4f07-88ea-002134cdc030`
- **参数名**: `DoIPIntReduceBoolDataByNegationThreshold`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `2`
- **取值范围**: [0..9223372036854775807]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: This parameter activates/deactivates the capability to compress boolean CONFIG-CLASS PRE-COMPILE ROM data by using the negation operator.

0: The optimization is deactivated.
>0: If the number of deduplicateable elements is greater than this threshold the data optimization can be performed.

########## 2. DoIPIntReduceBoolDataByNumericalComparisonThreshold

- **UUID**: `dc3dc09a-5980-4af7-bd1c-47dc7a3dc823`
- **参数名**: `DoIPIntReduceBoolDataByNumericalComparisonThreshold`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `2`
- **取值范围**: [0..9223372036854775807]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: This parameter activates/deactivates the capability to compress boolean CONFIG-CLASS PRE-COMPILE ROM data by using numerical comparison with other ROM data.

0: The optimization is deactivated.
>0: If the number of deduplicateable elements is greater than this threshold the data optimization can be performed.

########## 3. DoIPIntReduceBoolDataByNumericalRelationThreshold

- **UUID**: `718dcdbd-13e7-4b8a-8fc7-66221b3cc9be`
- **参数名**: `DoIPIntReduceBoolDataByNumericalRelationThreshold`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `2`
- **取值范围**: [0..9223372036854775807]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: This parameter activates/deactivates the capability to compress boolean CONFIG-CLASS PRE-COMPILE ROM data by using relational comparison with other ROM data.

0: The optimization is deactivated.
>0: If the number of deduplicateable elements is greater than this threshold the data optimization can be performed.

########## 4. DoIPIntReduceNumericalDataByOffsetThreshold

- **UUID**: `58d527a6-6463-4f5b-9737-ddfac5f73bed`
- **参数名**: `DoIPIntReduceNumericalDataByOffsetThreshold`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `2`
- **取值范围**: [0..9223372036854775807]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: This parameter activates/deactivates the capability to compress numerical CONFIG-CLASS PRE-COMPILE ROM data by using a constant offset.

0: The optimization is deactivated.
>0: If the number of deduplicateable elements is greater than this threshold the data optimization can be performed.

########## 5. DoIPIntReduceNumericalDataByArraySubtractionThreshold

- **UUID**: `cd30914d-9491-40d3-a30b-82604a682b98`
- **参数名**: `DoIPIntReduceNumericalDataByArraySubtractionThreshold`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `2`
- **取值范围**: [0..9223372036854775807]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: This parameter activates/deactivates the capability to compress numerical CONFIG-CLASS PRE-COMPILE ROM data by using a subtraction with other ROM data.

0: The optimization is deactivated.
>0: If the number of deduplicateable elements is greater than this threshold the data optimization can be performed.

######### BOOLEAN 类型参数

########## 1. DoIPIntOutOfBoundsWriteSanitizer

- **UUID**: `0b494b03-c2ec-4000-9307-880cfc8f735c`
- **参数名**: `DoIPIntOutOfBoundsWriteSanitizer`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: This parameter activates/deactivates the generation of runtime checks which call a DET error notification function to find easily out of bounds write problems.

FALSE:  no checks are generated in the data access.
TRUE: the data access is enriched with DET checks to validate indexes.

########## 2. DoIPIntOutOfBoundsReadSanitizer

- **UUID**: `aa688836-6415-4958-9393-3c6c16a03e8f`
- **参数名**: `DoIPIntOutOfBoundsReadSanitizer`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: This parameter activates/deactivates the generation of runtime checks which call a DET error notification function to find easily out of bounds read problems.

FALSE:  no checks are generated in the data access.
TRUE: the data access is enriched with DET checks to validate indexes.

########## 3. DoIPIntReduceConstantData2Define

- **UUID**: `46715e4c-33f3-4fe8-871b-849f88828a2e`
- **参数名**: `DoIPIntReduceConstantData2Define`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: This parameter activates/deactivates the capability to generate CONFIG-CLASS PRE-COMPILE ROM arrays as constant define.

FALSE: ROM arrays are generated as data even if all values are identical.
TRUE: ROM arrays are generated as constant define if all values are identical.

########## 4. DoIPIntDeduplicateIndirectedData

- **UUID**: `472a1a67-796d-4e7d-9cb0-7b4c7b406b5e`
- **参数名**: `DoIPIntDeduplicateIndirectedData`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: This parameter activates/deactivates the capability to compress 0:N relational ROM data in all CONFIG-CLASSES without increasing the runtime.

FALSE: 0:N relational ROM data is not compressed.
TRUE: 0:N relational ROM data is compressed without increasing the runtime.

########## 5. DoIPIntShortSymbols

- **UUID**: `94bc6381-d95c-4367-9d07-100b8c00eb79`
- **参数名**: `DoIPIntShortSymbols`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: This parameter activates/deactivates the capability to generate shortened symbol names.

FALSE: symbol names are generated in a human readable style based on the MIP, tags and variant names.
TRUE: symbol names are generated based on the MIP and a CRC32.

########## 6. DoIPIntInterfacesForDeactivatedData

- **UUID**: `8f8508f5-0918-445d-8938-b96e73e76623`
- **参数名**: `DoIPIntInterfacesForDeactivatedData`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: This parameter activates/deactivates the capability to generate bsw data interfaces for deactivated data elements. This is an advantage for the BSW developer to reduce the time to market with a development environment using auto completition and to investigate potential interfaces.

FALSE: data interfaces are not generated if the data elementis deactivated.
TRUE: data interfaces are generated as e.g. emty macros.

########## 7. DoIPIntReferringKeysInComments

- **UUID**: `ff0eee4b-3a79-40ad-b5f7-8f9bbfc8a7e2`
- **参数名**: `DoIPIntReferringKeysInComments`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: This parameter activates/deactivates the capability to generate referring keys in comments. This is an advantage for the developer to investigate indirections, but this feature reduces the overall readability of the generated data.

FALSE: referring keys are not generated in comments.
TRUE: referring keys are generated in comments.

######### ENUMERATION 类型参数

########## 1. DoIPIntOutOfBoundsWriteProtectionStrategy

- **UUID**: `1384a98a-6188-4d84-bc4c-5cc9969ba2db`
- **参数名**: `DoIPIntOutOfBoundsWriteProtectionStrategy`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `NONE`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `NONE` (来源: Vector Informatik)
  - `INDEX_SATURATION` (来源: Vector Informatik)
  - `INDEX_CHECKING` (来源: Vector Informatik)
- **描述**: This parameter is used to configure a strategy to protect the code to write out of bounds.

NONE: no protection strategy is generated in the data access.
INDEX_SATURATION: arrays are blown up and the data access index is saturated by an appropriate mask. The advantage is the speed of the data access, but own data elements at other indexes of the same variable can be overridden.
INDEX_CHECKING: the data access index is validated by a runtime check. The advantage is that values are never written to incorrect indexes of the data access.

########## 2. DoIPIntBoolDataInArrayOfStructStrategy

- **UUID**: `03474318-c660-48a4-929b-112b8a1a7847`
- **参数名**: `DoIPIntBoolDataInArrayOfStructStrategy`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `BITMASKING`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `BOOLEAN` (来源: Vector Informatik)
  - `BITFIELD` (来源: Vector Informatik)
  - `BITMASKING` (来源: Vector Informatik)
- **描述**: This parameter is used to tailor the usage of boolean data in structures in all CONFIG-CLASSES ROM data. The difference between BITFIELD and BITMASKING depends on your compiler options and memory mapping.

BOOLEAN: the datatype of boolean data is native boolean.
BITFIELD: the bitfield type is used and the compiler extracts the boolean data from structures.
BITMASKING: generated masks are used to extract the boolean data from structures.

########## 3. DoIPIntDataDeduplicationStrategy

- **UUID**: `78a35bf2-d420-41a6-8123-3c39efd137e0`
- **参数名**: `DoIPIntDataDeduplicationStrategy`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `DEDUPLICATE_CONST_DATA_WITH_CAST`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `NONE` (来源: Vector Informatik)
  - `DEDUPLICATE_CONST_DATA_WITHOUT_CAST` (来源: Vector Informatik)
  - `DEDUPLICATE_CONST_DATA_WITH_CAST` (来源: Vector Informatik)
- **描述**: This parameter is used to taylor the the deduplication of CONFIG-CLASS PRE-COMPILE  ROM data.

NONE: The generated data is not deduplicated.
DEDUPLICATE_CONST_DATA_WITHOUT_CAST: The data is deduplicated without using casts.
DEDUPLICATE_CONST_DATA_WITH_CAST: The data is deduplicated using casts.

########## 4. DoIPIntReduceBoolDataByNumericalOperandStrategy

- **UUID**: `39927c2f-8664-47ca-b54d-d126e711666c`
- **参数名**: `DoIPIntReduceBoolDataByNumericalOperandStrategy`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `DEDUPLICATE_DATA_WITH_ANY_VALUE`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `NONE` (来源: Vector Informatik)
  - `DEDUPLICATE_DATA_WITH_ZERO` (来源: Vector Informatik)
  - `DEDUPLICATE_DATA_WITH_ANY_VALUE` (来源: Vector Informatik)
- **描述**: This parameter is used to taylor the CONFIG-CLASS PRE-COMPILE ROM bool data with number deduplication mechanisms. A comparison with 0 is very efficient, but a numerical comparison with a value not 0 can be used to increase the ROM data compression rate.

NONE: ROM data deduplications are switched off.
DEDUPLICATE_DATA_WITH_ZERO: ROM data deduplications can be applied with the value 0.
DEDUPLICATE_DATA_WITH_ANY_VALUE: ROM data deduplications can be applied with any numerical value.

####### 2. DoIPIntEventCallback

**容器属性**:

- **UUID**: `9e3d7c13-bce9-41b2-ba19-d2414d65001a`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPIntEventCallback`
- **多重性**: [0..1]
- **需要索引**: false

**容器描述**:

This container provides parameter to configure an event callback and all its related parameter.

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. DoIPIntEventMaxUserDataLength

- **UUID**: `d0817d0b-12d1-4ca6-8aea-391dbdb32356`
- **参数名**: `DoIPIntEventMaxUserDataLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: This parameter defines the maximum user data length that shall be forwarded inisde the configured event callback function.

######### FUNCTION-NAME 类型参数

########## 1. DoIPIntEventCallback

- **UUID**: `a40fc2dd-20c7-4b62-b91a-fe77c19a35ef`
- **参数名**: `DoIPIntEventCallback`
- **数据类型**: FUNCTION-NAME
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **函数变体**:
  - 默认值: `Appl_DoIPInt_Event`
- **描述**: This parameter defines a callback function to report events via <User>_DoIPIntEvent.

##### 18. DoIPIntGeneration

**容器属性**:

- **UUID**: `15043fa7-d6a4-4b2f-9cbf-d6c574e2ffcb`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPIntGeneration`
- **多重性**: [1..1]
- **需要索引**: false

**容器描述**:

This container contains parameters to change general generation behavior.

###### 参数配置

此容器包含 **16** 个参数：

####### INTEGER 类型参数

######## 1. DoIPIntReduceBoolDataByNegationThreshold

- **UUID**: `aff67abf-8fc7-4f07-88ea-002134cdc030`
- **参数名**: `DoIPIntReduceBoolDataByNegationThreshold`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `2`
- **取值范围**: [0..9223372036854775807]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: This parameter activates/deactivates the capability to compress boolean CONFIG-CLASS PRE-COMPILE ROM data by using the negation operator.

0: The optimization is deactivated.
>0: If the number of deduplicateable elements is greater than this threshold the data optimization can be performed.

######## 2. DoIPIntReduceBoolDataByNumericalComparisonThreshold

- **UUID**: `dc3dc09a-5980-4af7-bd1c-47dc7a3dc823`
- **参数名**: `DoIPIntReduceBoolDataByNumericalComparisonThreshold`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `2`
- **取值范围**: [0..9223372036854775807]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: This parameter activates/deactivates the capability to compress boolean CONFIG-CLASS PRE-COMPILE ROM data by using numerical comparison with other ROM data.

0: The optimization is deactivated.
>0: If the number of deduplicateable elements is greater than this threshold the data optimization can be performed.

######## 3. DoIPIntReduceBoolDataByNumericalRelationThreshold

- **UUID**: `718dcdbd-13e7-4b8a-8fc7-66221b3cc9be`
- **参数名**: `DoIPIntReduceBoolDataByNumericalRelationThreshold`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `2`
- **取值范围**: [0..9223372036854775807]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: This parameter activates/deactivates the capability to compress boolean CONFIG-CLASS PRE-COMPILE ROM data by using relational comparison with other ROM data.

0: The optimization is deactivated.
>0: If the number of deduplicateable elements is greater than this threshold the data optimization can be performed.

######## 4. DoIPIntReduceNumericalDataByOffsetThreshold

- **UUID**: `58d527a6-6463-4f5b-9737-ddfac5f73bed`
- **参数名**: `DoIPIntReduceNumericalDataByOffsetThreshold`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `2`
- **取值范围**: [0..9223372036854775807]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: This parameter activates/deactivates the capability to compress numerical CONFIG-CLASS PRE-COMPILE ROM data by using a constant offset.

0: The optimization is deactivated.
>0: If the number of deduplicateable elements is greater than this threshold the data optimization can be performed.

######## 5. DoIPIntReduceNumericalDataByArraySubtractionThreshold

- **UUID**: `cd30914d-9491-40d3-a30b-82604a682b98`
- **参数名**: `DoIPIntReduceNumericalDataByArraySubtractionThreshold`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `2`
- **取值范围**: [0..9223372036854775807]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: This parameter activates/deactivates the capability to compress numerical CONFIG-CLASS PRE-COMPILE ROM data by using a subtraction with other ROM data.

0: The optimization is deactivated.
>0: If the number of deduplicateable elements is greater than this threshold the data optimization can be performed.

####### BOOLEAN 类型参数

######## 1. DoIPIntOutOfBoundsWriteSanitizer

- **UUID**: `0b494b03-c2ec-4000-9307-880cfc8f735c`
- **参数名**: `DoIPIntOutOfBoundsWriteSanitizer`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: This parameter activates/deactivates the generation of runtime checks which call a DET error notification function to find easily out of bounds write problems.

FALSE:  no checks are generated in the data access.
TRUE: the data access is enriched with DET checks to validate indexes.

######## 2. DoIPIntOutOfBoundsReadSanitizer

- **UUID**: `aa688836-6415-4958-9393-3c6c16a03e8f`
- **参数名**: `DoIPIntOutOfBoundsReadSanitizer`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: This parameter activates/deactivates the generation of runtime checks which call a DET error notification function to find easily out of bounds read problems.

FALSE:  no checks are generated in the data access.
TRUE: the data access is enriched with DET checks to validate indexes.

######## 3. DoIPIntReduceConstantData2Define

- **UUID**: `46715e4c-33f3-4fe8-871b-849f88828a2e`
- **参数名**: `DoIPIntReduceConstantData2Define`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: This parameter activates/deactivates the capability to generate CONFIG-CLASS PRE-COMPILE ROM arrays as constant define.

FALSE: ROM arrays are generated as data even if all values are identical.
TRUE: ROM arrays are generated as constant define if all values are identical.

######## 4. DoIPIntDeduplicateIndirectedData

- **UUID**: `472a1a67-796d-4e7d-9cb0-7b4c7b406b5e`
- **参数名**: `DoIPIntDeduplicateIndirectedData`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: This parameter activates/deactivates the capability to compress 0:N relational ROM data in all CONFIG-CLASSES without increasing the runtime.

FALSE: 0:N relational ROM data is not compressed.
TRUE: 0:N relational ROM data is compressed without increasing the runtime.

######## 5. DoIPIntShortSymbols

- **UUID**: `94bc6381-d95c-4367-9d07-100b8c00eb79`
- **参数名**: `DoIPIntShortSymbols`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: This parameter activates/deactivates the capability to generate shortened symbol names.

FALSE: symbol names are generated in a human readable style based on the MIP, tags and variant names.
TRUE: symbol names are generated based on the MIP and a CRC32.

######## 6. DoIPIntInterfacesForDeactivatedData

- **UUID**: `8f8508f5-0918-445d-8938-b96e73e76623`
- **参数名**: `DoIPIntInterfacesForDeactivatedData`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: This parameter activates/deactivates the capability to generate bsw data interfaces for deactivated data elements. This is an advantage for the BSW developer to reduce the time to market with a development environment using auto completition and to investigate potential interfaces.

FALSE: data interfaces are not generated if the data elementis deactivated.
TRUE: data interfaces are generated as e.g. emty macros.

######## 7. DoIPIntReferringKeysInComments

- **UUID**: `ff0eee4b-3a79-40ad-b5f7-8f9bbfc8a7e2`
- **参数名**: `DoIPIntReferringKeysInComments`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: This parameter activates/deactivates the capability to generate referring keys in comments. This is an advantage for the developer to investigate indirections, but this feature reduces the overall readability of the generated data.

FALSE: referring keys are not generated in comments.
TRUE: referring keys are generated in comments.

####### ENUMERATION 类型参数

######## 1. DoIPIntOutOfBoundsWriteProtectionStrategy

- **UUID**: `1384a98a-6188-4d84-bc4c-5cc9969ba2db`
- **参数名**: `DoIPIntOutOfBoundsWriteProtectionStrategy`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `NONE`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `NONE` (来源: Vector Informatik)
  - `INDEX_SATURATION` (来源: Vector Informatik)
  - `INDEX_CHECKING` (来源: Vector Informatik)
- **描述**: This parameter is used to configure a strategy to protect the code to write out of bounds.

NONE: no protection strategy is generated in the data access.
INDEX_SATURATION: arrays are blown up and the data access index is saturated by an appropriate mask. The advantage is the speed of the data access, but own data elements at other indexes of the same variable can be overridden.
INDEX_CHECKING: the data access index is validated by a runtime check. The advantage is that values are never written to incorrect indexes of the data access.

######## 2. DoIPIntBoolDataInArrayOfStructStrategy

- **UUID**: `03474318-c660-48a4-929b-112b8a1a7847`
- **参数名**: `DoIPIntBoolDataInArrayOfStructStrategy`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `BITMASKING`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `BOOLEAN` (来源: Vector Informatik)
  - `BITFIELD` (来源: Vector Informatik)
  - `BITMASKING` (来源: Vector Informatik)
- **描述**: This parameter is used to tailor the usage of boolean data in structures in all CONFIG-CLASSES ROM data. The difference between BITFIELD and BITMASKING depends on your compiler options and memory mapping.

BOOLEAN: the datatype of boolean data is native boolean.
BITFIELD: the bitfield type is used and the compiler extracts the boolean data from structures.
BITMASKING: generated masks are used to extract the boolean data from structures.

######## 3. DoIPIntDataDeduplicationStrategy

- **UUID**: `78a35bf2-d420-41a6-8123-3c39efd137e0`
- **参数名**: `DoIPIntDataDeduplicationStrategy`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `DEDUPLICATE_CONST_DATA_WITH_CAST`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `NONE` (来源: Vector Informatik)
  - `DEDUPLICATE_CONST_DATA_WITHOUT_CAST` (来源: Vector Informatik)
  - `DEDUPLICATE_CONST_DATA_WITH_CAST` (来源: Vector Informatik)
- **描述**: This parameter is used to taylor the the deduplication of CONFIG-CLASS PRE-COMPILE  ROM data.

NONE: The generated data is not deduplicated.
DEDUPLICATE_CONST_DATA_WITHOUT_CAST: The data is deduplicated without using casts.
DEDUPLICATE_CONST_DATA_WITH_CAST: The data is deduplicated using casts.

######## 4. DoIPIntReduceBoolDataByNumericalOperandStrategy

- **UUID**: `39927c2f-8664-47ca-b54d-d126e711666c`
- **参数名**: `DoIPIntReduceBoolDataByNumericalOperandStrategy`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `DEDUPLICATE_DATA_WITH_ANY_VALUE`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `NONE` (来源: Vector Informatik)
  - `DEDUPLICATE_DATA_WITH_ZERO` (来源: Vector Informatik)
  - `DEDUPLICATE_DATA_WITH_ANY_VALUE` (来源: Vector Informatik)
- **描述**: This parameter is used to taylor the CONFIG-CLASS PRE-COMPILE ROM bool data with number deduplication mechanisms. A comparison with 0 is very efficient, but a numerical comparison with a value not 0 can be used to increase the ROM data compression rate.

NONE: ROM data deduplications are switched off.
DEDUPLICATE_DATA_WITH_ZERO: ROM data deduplications can be applied with the value 0.
DEDUPLICATE_DATA_WITH_ANY_VALUE: ROM data deduplications can be applied with any numerical value.

##### 19. DoIPIntEventCallback

**容器属性**:

- **UUID**: `9e3d7c13-bce9-41b2-ba19-d2414d65001a`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPIntEventCallback`
- **多重性**: [0..1]
- **需要索引**: false

**容器描述**:

This container provides parameter to configure an event callback and all its related parameter.

###### 参数配置

此容器包含 **2** 个参数：

####### INTEGER 类型参数

######## 1. DoIPIntEventMaxUserDataLength

- **UUID**: `d0817d0b-12d1-4ca6-8aea-391dbdb32356`
- **参数名**: `DoIPIntEventMaxUserDataLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: This parameter defines the maximum user data length that shall be forwarded inisde the configured event callback function.

####### FUNCTION-NAME 类型参数

######## 1. DoIPIntEventCallback

- **UUID**: `a40fc2dd-20c7-4b62-b91a-fe77c19a35ef`
- **参数名**: `DoIPIntEventCallback`
- **数据类型**: FUNCTION-NAME
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **函数变体**:
  - 默认值: `Appl_DoIPInt_Event`
- **描述**: This parameter defines a callback function to report events via <User>_DoIPIntEvent.

## 📦 包结构

此ARXML文件包含 **1** 个包：

### 1. MICROSAR

- **UUID**: `ff55d029-386d-43a2-b3c2-dfef4c7a5e36`
- **包名称**: `MICROSAR`
- **包含元素数量**: 2

#### 包含的元素

##### BSW-IMPLEMENTATION 类型元素

1. **DoIPInt_Impl**

##### ECUC-MODULE-DEF 类型元素

1. **DoIPInt**

## ⚡ 实现信息

此ARXML文件包含 **1** 个实现：

### 1. DoIPInt_Impl

- **UUID**: `494ff045-db42-43ac-9c29-43bf56637310`
- **实现名称**: `DoIPInt_Impl`
- **编程语言**: C
- **软件版本**: 7.01.00
- **供应商ID**: 30
- **AUTOSAR版本**: 4.02.02
- **代码生成器**: DaVinci Configurator
