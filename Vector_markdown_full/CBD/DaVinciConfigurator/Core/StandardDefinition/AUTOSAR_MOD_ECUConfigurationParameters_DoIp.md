# DoIP - 完整配置文档

*此文档由ARXML文件自动生成，采用层次化结构展示*

**生成时间**: 2025-06-16 14:46:13

## 📑 目录

- [📄 文件信息](#-文件信息)
- [🔧 模块定义](#-模块定义)
  - [DoIP](#doip)
- [📦 包结构](#-包结构)

## 📄 文件信息

### Schema信息
- **Schema位置**: `http://autosar.org/schema/r4.0 file:///D:/bla/ASR403/AUTOSAR_4-0-3.xsd`
- **命名空间**: `http://autosar.org/schema/r4.0`

## 🔧 模块定义

### 1. DoIP

#### 基本信息

- **UUID**: `01a84faa-a44a-4934-b166-0c0854fb77aa`
- **模块名称**: `DoIP`
- **多重性**: [0..1]
- **支持的变体**:
  - VARIANT-LINK-TIME
  - VARIANT-POST-BUILD
  - VARIANT-PRE-COMPILE

#### 模块描述

Configuration of the DoIP (Diagnostic over IP) module.

#### 版本历史

共有 **1** 个版本记录：

##### 1. 版本 4.3.0

- **发布日期**: 2012-08-01
- **发布者**: AUTOSAR

*此版本无详细变更记录*

#### 配置容器

本模块包含 **24** 个配置容器：

##### 1. DoIPConfigSet

**容器属性**:

- **UUID**: `8d69e9a6-7dde-43cc-b8a5-6a893adec2c1`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPConfigSet`
- **多重性**: [1..1]
- **构建后可变**: false
- **多配置容器**: true

**容器描述**:

This container contains the configuration parameters and sub containers of the AUTOSAR DoIP module. This container is a MultipleConfigurationContainer, i.e. this container and its sub-containers exist once per configuration set.

###### 参数配置

此容器包含 **3** 个参数：

####### INTEGER 类型参数

######## 1. DoIPEid

- **UUID**: `c95693a7-1fa8-4ec3-82d8-278e9a7c4b78`
- **参数名**: `DoIPEid`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [1..281474976710656]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Configured EID (Entity ID of) for vehicle identification/vehicle announcement. Only necessary if DoIPUseMacAddressForIdentification is set to FALSE.

######## 2. DoIPGid

- **UUID**: `1a8fb635-bf3f-4bcc-9d25-44369902fd98`
- **参数名**: `DoIPGid`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [1..281474976710656]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Configured GID (Group ID of) for vehicle identification/vehicle announcement.

######## 3. DoIPLogicalAddress

- **UUID**: `1084b0a2-dd48-4589-af11-a38fe122145a`
- **参数名**: `DoIPLogicalAddress`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Describes the logical address of the DoIP entity, i.e. the SA that will route diagnostic requests to the Dcm of the DoIP entity.

###### 配置容器

本模块包含 **19** 个配置容器：

####### 1. DoIPInterface

**容器属性**:

- **UUID**: `ECUC:789e2362-020e-4531-b21a-6f65ae92c662`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPInterface`
- **多重性**: [1..255]

**容器描述**:

This container defines a logical IP interface and collects properties to configure this interface.

######## 参数配置

此容器包含 **12** 个参数：

######### INTEGER 类型参数

########## 1. DoIPInterfaceId

- **UUID**: `ECUC:1b2e63b0-6029-4653-b54a-f59977514a0c`
- **参数名**: `DoIPInterfaceId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **描述**: This parameter is an identifier of the DoIPInterface. The value of this parameter will be assigned to the symbolic name derived from the container short name.

########## 2. DoIPMaxTesterConnections

- **UUID**: `ECUC:4ee8c2a0-3924-41c7-a5d1-3bcf431efb0e`
- **参数名**: `DoIPMaxTesterConnections`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Maximum amount of tester connections that shall be maintained at one time before alive check is performed.

########## 3. DoIPVehicleAnnouncementCount

- **UUID**: `ECUC:18720174-b4fb-4222-8e3b-9de228019753`
- **参数名**: `DoIPVehicleAnnouncementCount`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [1..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Number of vehicle announcement messages on IP address assignment. Represents parameter A_DoIP_Announce_Num of ISO 13400-2:2012.

######### BOOLEAN 类型参数

########## 1. DoIPInterfaceActLineCtrl

- **UUID**: `ECUC:6e2237e3-5bac-41e9-bf4a-ae8559979fa6`
- **参数名**: `DoIPInterfaceActLineCtrl`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: This attribute defines whether the network interface

########## 2. DoIPUseMacAddressForIdentification

- **UUID**: `ECUC:364c701f-a202-4a4b-b7bc-ee6cf58cddb3`
- **参数名**: `DoIPUseMacAddressForIdentification`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Provided the information if a configured EID at vehicle identification response/vehicle announment is used or the MAC address.

########## 3. DoIPUseVehicleIdentificationSyncStatus

- **UUID**: `ECUC:77dc8eda-649f-4728-9915-a08f25f81905`
- **参数名**: `DoIPUseVehicleIdentificationSyncStatus`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Defines if the optional VIN/GID synchronization status is used additionally in the vehicle identification/announcement.

######### FLOAT 类型参数

########## 1. DoIPAliveCheckResponseTimeout

- **UUID**: `ECUC:a680c7fa-c06d-4139-b2a8-e60b1ee21fa6`
- **参数名**: `DoIPAliveCheckResponseTimeout`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0..INF]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Timeout  in [s] for waiting for a response to an Alive Check request before the connection is considered to be disconnected. Represents parameter T_TCP_AliveCheck of ISO 13400-2:2012.

########## 2. DoIPGeneralInactivityTime

- **UUID**: `ECUC:3c672e92-2dff-4c0d-98eb-0c9379bcafec`
- **参数名**: `DoIPGeneralInactivityTime`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0..INF]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Timeout in [s] for maximum inactivity of a TCP socket connection before the DoIP module will close the according socket connection. Represents parameter T_TCP_General_Inactivity of ISO 13400-2:2012

########## 3. DoIPInitialInactivityTime

- **UUID**: `ECUC:f455792f-afbc-4de1-ab70-30d56a927828`
- **参数名**: `DoIPInitialInactivityTime`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0..INF]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Timeout in [s] used for initial inactivity of a connected TCP socket connection directly after socket connection. Represents parameter T_TCP_Initial_Inactivity of ISO 13400-2:2012

########## 4. DoIPInitialVehicleAnnouncementTime

- **UUID**: `ECUC:f2ce0a2d-fc67-453a-8b22-6f0f033507b2`
- **参数名**: `DoIPInitialVehicleAnnouncementTime`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0..INF]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Time to wait in [s] for sending first vehicle anouncement message after IP address assignment. Represents parameter A_DoIP_Announce_Wait of ISO 13400-2:2012

########## 5. DoIPVehicleAnnouncementInterval

- **UUID**: `ECUC:53d5e0b6-56d1-459d-a3ec-69ce6e1c46c1`
- **参数名**: `DoIPVehicleAnnouncementInterval`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **取值范围**: [0..INF]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Time to wait in [s] for sending subsequent vehicle anouncement messages. Represents parameter A_DoIP_Announce_Interval of ISO 13400-2:2012

######### ENUMERATION 类型参数

########## 1. DoIPInterfaceAnnouncementStart

- **UUID**: `ECUC:c7a33c91-d135-444a-8806-80515d8ae9fe`
- **参数名**: `DoIPInterfaceAnnouncementStart`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `DOIP_AUTOMATIC_ANNOUNCE`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `DOIP_AUTOMATIC_ANNOUNCE` (来源: AUTOSAR_ECUC)
  - `DOIP_ONTRIGGER_ANNOUNCE` (来源: AUTOSAR_ECUC)
- **描述**: This attribute defines, when vehicle announcement is started on a DoIPInterface

######## 配置容器

本模块包含 **18** 个配置容器：

######### 1. DoIPChannel

**容器属性**:

- **UUID**: `ECUC:ce8927a0-58c7-4099-a996-3ee43001e9e8`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPChannel`
- **多重性**: [1..65536]

**容器描述**:

Configuration of one DoIPChannel.

########## 引用关系

此容器包含 **2** 个引用：

########### REFERENCE 类型引用

############ 1. DoIPChannelSARef

- **UUID**: `ECUC:893cf71a-c06b-4044-812c-8df50e45d13e`
- **引用名**: `DoIPChannelSARef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `DoIPTester`
- **完整路径**: `/AUTOSAR/EcucDefs/DoIP/DoIPConfigSet/DoIPInterface/DoIPTester`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the DoIPTester.

############ 2. DoIPChannelTARef

- **UUID**: `ECUC:cbe1685e-4306-4efc-8345-5a1446b28405`
- **引用名**: `DoIPChannelTARef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `DoIPTargetAddress`
- **完整路径**: `/AUTOSAR/EcucDefs/DoIP/DoIPConfigSet/DoIPInterface/DoIPConnections/DoIPTargetAddress`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the target address.

########## 配置容器

本模块包含 **2** 个配置容器：

########### 1. DoIPPduRRxPdu

**容器属性**:

- **UUID**: `ECUC:63341ec1-b4ca-4bbc-82b5-a883d528b7c1`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPPduRRxPdu`
- **多重性**: [0..1]

**容器描述**:

This container contains the Rx Pdus to connect with the Rx Pdus of the PduR.

############ 参数配置

此容器包含 **1** 个参数：

############# INTEGER 类型参数

############## 1. DoIPPduRRxPduId

- **UUID**: `ECUC:affbfe09-cf4f-43ed-91f0-957c1e71f17f`
- **参数名**: `DoIPPduRRxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **描述**: The DoIPPduRRxPduId is required by the API call DoIP_TpCancelReceive.

############ 引用关系

此容器包含 **1** 个引用：

############# REFERENCE 类型引用

############## 1. DoIPPduRRxPduRef

- **UUID**: `ECUC:0fb53490-8f12-418b-a048-feaf0c60d6b0`
- **引用名**: `DoIPPduRRxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the "global" Pdu structure to allow harmonization of handle IDs in the COM-Stack.

########### 2. DoIPPduRTxPdu

**容器属性**:

- **UUID**: `ECUC:ecf769bc-a264-4426-a107-185d357d42b4`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPPduRTxPdu`
- **多重性**: [0..1]

**容器描述**:

This container contains the Tx Pdus to connect with the Tx Pdus of the PduR.  If the parameter is not configured the channel is for functional addressing.

############ 参数配置

此容器包含 **2** 个参数：

############# INTEGER 类型参数

############## 1. DoIPPduRTxPduId

- **UUID**: `ECUC:4ec22559-5780-41ca-af56-0b32ecdd6dae`
- **参数名**: `DoIPPduRTxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **描述**: The DoIPPduRTxPduId is required by DoIP_TpTransmit or DoIP_IfTransmit and DoIP_TpCancelTransmit.

############# ENUMERATION 类型参数

############## 1. DoIPPduType

- **UUID**: `ECUC:17c8aace-cda8-471d-8cb2-e474dda9c61a`
- **参数名**: `DoIPPduType`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `DOIP_TPPDU`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `DOIP_IFPDU` (来源: AUTOSAR_ECUC)
  - `DOIP_TPPDU` (来源: AUTOSAR_ECUC)
- **描述**: API Type to use for communication with PduR. DOIP_IFPDU for UUDT messages, DOIP_TPPDU for all other diagnostic messages.

############ 引用关系

此容器包含 **1** 个引用：

############# REFERENCE 类型引用

############## 1. DoIPPduRTxPduRef

- **UUID**: `ECUC:f703fb82-d2e7-4545-a97c-3275ff0bfc5d`
- **引用名**: `DoIPPduRTxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the "global" Pdu structure to allow harmonization of handle IDs in the COM-Stack.

######### 2. DoIPPduRRxPdu

**容器属性**:

- **UUID**: `ECUC:63341ec1-b4ca-4bbc-82b5-a883d528b7c1`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPPduRRxPdu`
- **多重性**: [0..1]

**容器描述**:

This container contains the Rx Pdus to connect with the Rx Pdus of the PduR.

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. DoIPPduRRxPduId

- **UUID**: `ECUC:affbfe09-cf4f-43ed-91f0-957c1e71f17f`
- **参数名**: `DoIPPduRRxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **描述**: The DoIPPduRRxPduId is required by the API call DoIP_TpCancelReceive.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. DoIPPduRRxPduRef

- **UUID**: `ECUC:0fb53490-8f12-418b-a048-feaf0c60d6b0`
- **引用名**: `DoIPPduRRxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the "global" Pdu structure to allow harmonization of handle IDs in the COM-Stack.

######### 3. DoIPPduRTxPdu

**容器属性**:

- **UUID**: `ECUC:ecf769bc-a264-4426-a107-185d357d42b4`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPPduRTxPdu`
- **多重性**: [0..1]

**容器描述**:

This container contains the Tx Pdus to connect with the Tx Pdus of the PduR.  If the parameter is not configured the channel is for functional addressing.

########## 参数配置

此容器包含 **2** 个参数：

########### INTEGER 类型参数

############ 1. DoIPPduRTxPduId

- **UUID**: `ECUC:4ec22559-5780-41ca-af56-0b32ecdd6dae`
- **参数名**: `DoIPPduRTxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **描述**: The DoIPPduRTxPduId is required by DoIP_TpTransmit or DoIP_IfTransmit and DoIP_TpCancelTransmit.

########### ENUMERATION 类型参数

############ 1. DoIPPduType

- **UUID**: `ECUC:17c8aace-cda8-471d-8cb2-e474dda9c61a`
- **参数名**: `DoIPPduType`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `DOIP_TPPDU`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `DOIP_IFPDU` (来源: AUTOSAR_ECUC)
  - `DOIP_TPPDU` (来源: AUTOSAR_ECUC)
- **描述**: API Type to use for communication with PduR. DOIP_IFPDU for UUDT messages, DOIP_TPPDU for all other diagnostic messages.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. DoIPPduRTxPduRef

- **UUID**: `ECUC:f703fb82-d2e7-4545-a97c-3275ff0bfc5d`
- **引用名**: `DoIPPduRTxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the "global" Pdu structure to allow harmonization of handle IDs in the COM-Stack.

######### 4. DoIPConnections

**容器属性**:

- **UUID**: `ECUC:06a174a5-5ad6-4b7a-8ce8-c64883f2e5c5`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPConnections`
- **多重性**: [1..1]

**容器描述**:

Container contains all lower layer connection specific information, i.e. the single Pdu References and Handle IDs to the SoAd.

########## 配置容器

本模块包含 **9** 个配置容器：

########### 1. DoIPTargetAddress

**容器属性**:

- **UUID**: `ECUC:11b8faaf-bc59-49fe-97b5-29df73fa6ee7`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPTargetAddress`
- **多重性**: [1..65535]

**容器描述**:

This container describes a possible TargetAddress that is supported by DoIP.

############ 参数配置

此容器包含 **1** 个参数：

############# INTEGER 类型参数

############## 1. DoIPTargetAddressValue

- **UUID**: `ECUC:c46011a4-ab1a-42cf-a2f8-b71632fcfd59`
- **参数名**: `DoIPTargetAddressValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Valid Target Address of a DoIP target address.

########### 2. DoIPTcpConnection

**容器属性**:

- **UUID**: `ECUC:e3ccdc1d-8a6b-40a0-abbf-59a1db67e267`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPTcpConnection`
- **多重性**: [1..255]

**容器描述**:

This container describes a TCP connection to the lower layer SoAd module.

############ 参数配置

此容器包含 **2** 个参数：

############# BOOLEAN 类型参数

############## 1. DoIPRequestAddressAssignment

- **UUID**: `ECUC:5fac5a9e-0915-86f1-5a0e-df77eade14b8`
- **参数名**: `DoIPRequestAddressAssignment`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: The DoIP module shall request IP address assignment by calling SoAd_RequestIpAddrAssignment() for the TcpIpLocalAddr related to this DoIpConnection.

############## 2. DoIPTcpConnectionSecurityRequired

- **UUID**: `ECUC:e723d1bf-784e-4527-892c-4fcbf9e11e05`
- **参数名**: `DoIPTcpConnectionSecurityRequired`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Indicates if the associated TCP socket uses a secure connection (e.g. TLS)

############ 配置容器

本模块包含 **2** 个配置容器：

############# 1. DoIPSoAdTcpRxPdu

**容器属性**:

- **UUID**: `ECUC:f8ff31c4-d60d-4316-b021-67cb31934ee7`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPSoAdTcpRxPdu`
- **多重性**: [1..1]

**容器描述**:

This container describes a Rx PDU received via SoAd over TCP

############## 参数配置

此容器包含 **1** 个参数：

############### INTEGER 类型参数

################ 1. DoIPSoAdTcpRxPduId

- **UUID**: `ECUC:87bc6f78-b949-44dd-a958-16f6c2003d78`
- **参数名**: `DoIPSoAdTcpRxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **描述**: The DoIPSoAdTcpRxPduId is required by the API call DoIP_SoAdTpRxIndication to receive I-PDUs from the SoAd.

############## 引用关系

此容器包含 **1** 个引用：

############### REFERENCE 类型引用

################ 1. DoIPSoAdTcpRxPduRef

- **UUID**: `ECUC:7fa9533f-a369-48ce-8666-1982b51d007d`
- **引用名**: `DoIPSoAdTcpRxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the "global" Pdu structure to allow harmonization of handle IDs in the COM-Stack.

############# 2. DoIPSoAdTcpTxPdu

**容器属性**:

- **UUID**: `ECUC:b94850e4-7ec7-4c7a-95d7-e883570c386f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPSoAdTcpTxPdu`
- **多重性**: [1..1]

**容器描述**:

This container describes a Tx PDU sent via SoAd over TCP

############## 参数配置

此容器包含 **1** 个参数：

############### INTEGER 类型参数

################ 1. DoIPSoAdTcpTxPduId

- **UUID**: `ECUC:18866fc8-b1b6-4749-866c-8d0dff665d6e`
- **参数名**: `DoIPSoAdTcpTxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **描述**: The DoIPSoAdTcpTxPduId is required by the API call DoIP_SoAdTpTxConfirmation that is called by the SoAd to confirm that the IPdu has been transmitted successfully.

############## 引用关系

此容器包含 **1** 个引用：

############### REFERENCE 类型引用

################ 1. DoIPSoAdTcpTxPduRef

- **UUID**: `ECUC:71678586-2f21-4e4f-aefc-997db5b282a4`
- **引用名**: `DoIPSoAdTcpTxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the "global" Pdu structure to allow harmonization of handle IDs in the COM-Stack.

########### 3. DoIPSoAdTcpRxPdu

**容器属性**:

- **UUID**: `ECUC:f8ff31c4-d60d-4316-b021-67cb31934ee7`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPSoAdTcpRxPdu`
- **多重性**: [1..1]

**容器描述**:

This container describes a Rx PDU received via SoAd over TCP

############ 参数配置

此容器包含 **1** 个参数：

############# INTEGER 类型参数

############## 1. DoIPSoAdTcpRxPduId

- **UUID**: `ECUC:87bc6f78-b949-44dd-a958-16f6c2003d78`
- **参数名**: `DoIPSoAdTcpRxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **描述**: The DoIPSoAdTcpRxPduId is required by the API call DoIP_SoAdTpRxIndication to receive I-PDUs from the SoAd.

############ 引用关系

此容器包含 **1** 个引用：

############# REFERENCE 类型引用

############## 1. DoIPSoAdTcpRxPduRef

- **UUID**: `ECUC:7fa9533f-a369-48ce-8666-1982b51d007d`
- **引用名**: `DoIPSoAdTcpRxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the "global" Pdu structure to allow harmonization of handle IDs in the COM-Stack.

########### 4. DoIPSoAdTcpTxPdu

**容器属性**:

- **UUID**: `ECUC:b94850e4-7ec7-4c7a-95d7-e883570c386f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPSoAdTcpTxPdu`
- **多重性**: [1..1]

**容器描述**:

This container describes a Tx PDU sent via SoAd over TCP

############ 参数配置

此容器包含 **1** 个参数：

############# INTEGER 类型参数

############## 1. DoIPSoAdTcpTxPduId

- **UUID**: `ECUC:18866fc8-b1b6-4749-866c-8d0dff665d6e`
- **参数名**: `DoIPSoAdTcpTxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **描述**: The DoIPSoAdTcpTxPduId is required by the API call DoIP_SoAdTpTxConfirmation that is called by the SoAd to confirm that the IPdu has been transmitted successfully.

############ 引用关系

此容器包含 **1** 个引用：

############# REFERENCE 类型引用

############## 1. DoIPSoAdTcpTxPduRef

- **UUID**: `ECUC:71678586-2f21-4e4f-aefc-997db5b282a4`
- **引用名**: `DoIPSoAdTcpTxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the "global" Pdu structure to allow harmonization of handle IDs in the COM-Stack.

########### 5. DoIPUdpConnection

**容器属性**:

- **UUID**: `ECUC:113b6883-6d62-4e20-9cb6-680252dad2b0`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPUdpConnection`
- **多重性**: [1..255]

**容器描述**:

This Container describes a Udp connection to the lower layer SoAd module.

############ 参数配置

此容器包含 **1** 个参数：

############# BOOLEAN 类型参数

############## 1. DoIPRequestAddressAssignment

- **UUID**: `ECUC:8d1ae703-ec0c-9471-4b05-edd862510501`
- **参数名**: `DoIPRequestAddressAssignment`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: The DoIP module shall request IP address assignment by calling SoAd_RequestIpAddrAssignment() for the TcpIpLocalAddr related to this DoIpConnection.

############ 配置容器

本模块包含 **2** 个配置容器：

############# 1. DoIPSoAdUdpRxPdu

**容器属性**:

- **UUID**: `ECUC:799689c9-1f1f-4245-8228-18b7bf0c2dee`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPSoAdUdpRxPdu`
- **多重性**: [1..1]

**容器描述**:

This container describes a Rx PDU received via SoAd over UDP.

############## 参数配置

此容器包含 **1** 个参数：

############### INTEGER 类型参数

################ 1. DoIPSoAdUdpRxPduId

- **UUID**: `ECUC:103f1b68-c87a-4b28-ad2b-a9a27b600be2`
- **参数名**: `DoIPSoAdUdpRxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **描述**: The DoIPSoAdUdpRxPduId is required by the API call DoIP_SoAdIfRxIndication to receive I-PDUs from the SoAd.

############## 引用关系

此容器包含 **1** 个引用：

############### REFERENCE 类型引用

################ 1. DoIPSoAdUdpRxPduRef

- **UUID**: `ECUC:fd7f5cdf-7cf4-45f4-a627-2d343a8f7ed5`
- **引用名**: `DoIPSoAdUdpRxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the "global" Pdu structure to allow harmonization of handle IDs in the COM-Stack.

############# 2. DoIPSoAdUdpTxPdu

**容器属性**:

- **UUID**: `ECUC:b3d21ded-7966-4862-8d48-ddf2775239cc`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPSoAdUdpTxPdu`
- **多重性**: [1..1]

**容器描述**:

This container describes a Tx PDU sent via SoAd over UDP.

############## 参数配置

此容器包含 **1** 个参数：

############### INTEGER 类型参数

################ 1. DoIPSoAdUdpTxPduId

- **UUID**: `ECUC:2f55a1ec-664b-4bd6-9da3-2f80f2a73746`
- **参数名**: `DoIPSoAdUdpTxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **描述**: The DoIPSoAdUdpTxPduId is required by the API call DoIP_SoAdIfTxConfirmation that is called by the SoAd to confirm that the IPdu has been transmitted successfully.

############## 引用关系

此容器包含 **1** 个引用：

############### REFERENCE 类型引用

################ 1. DoIPSoAdUdpTxPduRef

- **UUID**: `ECUC:c31e5dee-28e5-4b32-8cec-51f54e77a3a3`
- **引用名**: `DoIPSoAdUdpTxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the "global" Pdu structure to allow harmonization of handle IDs in the COM-Stack.

########### 6. DoIPSoAdUdpRxPdu

**容器属性**:

- **UUID**: `ECUC:799689c9-1f1f-4245-8228-18b7bf0c2dee`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPSoAdUdpRxPdu`
- **多重性**: [1..1]

**容器描述**:

This container describes a Rx PDU received via SoAd over UDP.

############ 参数配置

此容器包含 **1** 个参数：

############# INTEGER 类型参数

############## 1. DoIPSoAdUdpRxPduId

- **UUID**: `ECUC:103f1b68-c87a-4b28-ad2b-a9a27b600be2`
- **参数名**: `DoIPSoAdUdpRxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **描述**: The DoIPSoAdUdpRxPduId is required by the API call DoIP_SoAdIfRxIndication to receive I-PDUs from the SoAd.

############ 引用关系

此容器包含 **1** 个引用：

############# REFERENCE 类型引用

############## 1. DoIPSoAdUdpRxPduRef

- **UUID**: `ECUC:fd7f5cdf-7cf4-45f4-a627-2d343a8f7ed5`
- **引用名**: `DoIPSoAdUdpRxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the "global" Pdu structure to allow harmonization of handle IDs in the COM-Stack.

########### 7. DoIPSoAdUdpTxPdu

**容器属性**:

- **UUID**: `ECUC:b3d21ded-7966-4862-8d48-ddf2775239cc`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPSoAdUdpTxPdu`
- **多重性**: [1..1]

**容器描述**:

This container describes a Tx PDU sent via SoAd over UDP.

############ 参数配置

此容器包含 **1** 个参数：

############# INTEGER 类型参数

############## 1. DoIPSoAdUdpTxPduId

- **UUID**: `ECUC:2f55a1ec-664b-4bd6-9da3-2f80f2a73746`
- **参数名**: `DoIPSoAdUdpTxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **描述**: The DoIPSoAdUdpTxPduId is required by the API call DoIP_SoAdIfTxConfirmation that is called by the SoAd to confirm that the IPdu has been transmitted successfully.

############ 引用关系

此容器包含 **1** 个引用：

############# REFERENCE 类型引用

############## 1. DoIPSoAdUdpTxPduRef

- **UUID**: `ECUC:c31e5dee-28e5-4b32-8cec-51f54e77a3a3`
- **引用名**: `DoIPSoAdUdpTxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the "global" Pdu structure to allow harmonization of handle IDs in the COM-Stack.

########### 8. DoIPUdpVehicleAnnouncementConnection

**容器属性**:

- **UUID**: `ECUC:ec10775c-9dc4-49d9-b17b-73c202f875ed`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPUdpVehicleAnnouncementConnection`
- **多重性**: [1..255]

**容器描述**:

This container describes the UDP multicast connections to the lower layer SoAd module.

############ 参数配置

此容器包含 **1** 个参数：

############# BOOLEAN 类型参数

############## 1. DoIPRequestAddressAssignment

- **UUID**: `ECUC:67eff5dd-1c6e-902a-5fca-f998126ea83e`
- **参数名**: `DoIPRequestAddressAssignment`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: The DoIP module shall request IP address assignment by calling SoAd_RequestIpAddrAssignment() for the TcpIpLocalAddr related to this DoIpConnection.

############ 配置容器

本模块包含 **1** 个配置容器：

############# 1. DoIPSoAdUdpVehicleAnnouncementTxPdu

**容器属性**:

- **UUID**: `ECUC:ca2c98f1-142e-4d74-b3e2-a2c7a5d2a5a7`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPSoAdUdpVehicleAnnouncementTxPdu`
- **多重性**: [1..1]

**容器描述**:

This container describes the vehicle announcement TxPdu sent via the SoAd.

############## 参数配置

此容器包含 **1** 个参数：

############### INTEGER 类型参数

################ 1. DoIPSoAdUdpVehicleAnnouncementTxPduId

- **UUID**: `ECUC:d714703b-f033-4dcf-91de-1b6f531e9af7`
- **参数名**: `DoIPSoAdUdpVehicleAnnouncementTxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **描述**: The DoIPSoAdUdpVehicleAnnouncementTxPduId is required by the API call DoIP_SoAdIfTxConfirmation() that is called by the SoAd to confirm that the IPdu has been transmitted successfully.

############## 引用关系

此容器包含 **1** 个引用：

############### REFERENCE 类型引用

################ 1. DoIPSoAdUdpVehicleAnnouncementTxPduRef

- **UUID**: `ECUC:90da376e-29ea-4262-aa92-05bf32a3971e`
- **引用名**: `DoIPSoAdUdpVehicleAnnouncementTxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the "global" PDU structure to allow harmonization of handle IDs in the COM-Stack.

########### 9. DoIPSoAdUdpVehicleAnnouncementTxPdu

**容器属性**:

- **UUID**: `ECUC:ca2c98f1-142e-4d74-b3e2-a2c7a5d2a5a7`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPSoAdUdpVehicleAnnouncementTxPdu`
- **多重性**: [1..1]

**容器描述**:

This container describes the vehicle announcement TxPdu sent via the SoAd.

############ 参数配置

此容器包含 **1** 个参数：

############# INTEGER 类型参数

############## 1. DoIPSoAdUdpVehicleAnnouncementTxPduId

- **UUID**: `ECUC:d714703b-f033-4dcf-91de-1b6f531e9af7`
- **参数名**: `DoIPSoAdUdpVehicleAnnouncementTxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **描述**: The DoIPSoAdUdpVehicleAnnouncementTxPduId is required by the API call DoIP_SoAdIfTxConfirmation() that is called by the SoAd to confirm that the IPdu has been transmitted successfully.

############ 引用关系

此容器包含 **1** 个引用：

############# REFERENCE 类型引用

############## 1. DoIPSoAdUdpVehicleAnnouncementTxPduRef

- **UUID**: `ECUC:90da376e-29ea-4262-aa92-05bf32a3971e`
- **引用名**: `DoIPSoAdUdpVehicleAnnouncementTxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the "global" PDU structure to allow harmonization of handle IDs in the COM-Stack.

######### 5. DoIPTargetAddress

**容器属性**:

- **UUID**: `ECUC:11b8faaf-bc59-49fe-97b5-29df73fa6ee7`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPTargetAddress`
- **多重性**: [1..65535]

**容器描述**:

This container describes a possible TargetAddress that is supported by DoIP.

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. DoIPTargetAddressValue

- **UUID**: `ECUC:c46011a4-ab1a-42cf-a2f8-b71632fcfd59`
- **参数名**: `DoIPTargetAddressValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Valid Target Address of a DoIP target address.

######### 6. DoIPTcpConnection

**容器属性**:

- **UUID**: `ECUC:e3ccdc1d-8a6b-40a0-abbf-59a1db67e267`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPTcpConnection`
- **多重性**: [1..255]

**容器描述**:

This container describes a TCP connection to the lower layer SoAd module.

########## 参数配置

此容器包含 **2** 个参数：

########### BOOLEAN 类型参数

############ 1. DoIPRequestAddressAssignment

- **UUID**: `ECUC:5fac5a9e-0915-86f1-5a0e-df77eade14b8`
- **参数名**: `DoIPRequestAddressAssignment`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: The DoIP module shall request IP address assignment by calling SoAd_RequestIpAddrAssignment() for the TcpIpLocalAddr related to this DoIpConnection.

############ 2. DoIPTcpConnectionSecurityRequired

- **UUID**: `ECUC:e723d1bf-784e-4527-892c-4fcbf9e11e05`
- **参数名**: `DoIPTcpConnectionSecurityRequired`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Indicates if the associated TCP socket uses a secure connection (e.g. TLS)

########## 配置容器

本模块包含 **2** 个配置容器：

########### 1. DoIPSoAdTcpRxPdu

**容器属性**:

- **UUID**: `ECUC:f8ff31c4-d60d-4316-b021-67cb31934ee7`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPSoAdTcpRxPdu`
- **多重性**: [1..1]

**容器描述**:

This container describes a Rx PDU received via SoAd over TCP

############ 参数配置

此容器包含 **1** 个参数：

############# INTEGER 类型参数

############## 1. DoIPSoAdTcpRxPduId

- **UUID**: `ECUC:87bc6f78-b949-44dd-a958-16f6c2003d78`
- **参数名**: `DoIPSoAdTcpRxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **描述**: The DoIPSoAdTcpRxPduId is required by the API call DoIP_SoAdTpRxIndication to receive I-PDUs from the SoAd.

############ 引用关系

此容器包含 **1** 个引用：

############# REFERENCE 类型引用

############## 1. DoIPSoAdTcpRxPduRef

- **UUID**: `ECUC:7fa9533f-a369-48ce-8666-1982b51d007d`
- **引用名**: `DoIPSoAdTcpRxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the "global" Pdu structure to allow harmonization of handle IDs in the COM-Stack.

########### 2. DoIPSoAdTcpTxPdu

**容器属性**:

- **UUID**: `ECUC:b94850e4-7ec7-4c7a-95d7-e883570c386f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPSoAdTcpTxPdu`
- **多重性**: [1..1]

**容器描述**:

This container describes a Tx PDU sent via SoAd over TCP

############ 参数配置

此容器包含 **1** 个参数：

############# INTEGER 类型参数

############## 1. DoIPSoAdTcpTxPduId

- **UUID**: `ECUC:18866fc8-b1b6-4749-866c-8d0dff665d6e`
- **参数名**: `DoIPSoAdTcpTxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **描述**: The DoIPSoAdTcpTxPduId is required by the API call DoIP_SoAdTpTxConfirmation that is called by the SoAd to confirm that the IPdu has been transmitted successfully.

############ 引用关系

此容器包含 **1** 个引用：

############# REFERENCE 类型引用

############## 1. DoIPSoAdTcpTxPduRef

- **UUID**: `ECUC:71678586-2f21-4e4f-aefc-997db5b282a4`
- **引用名**: `DoIPSoAdTcpTxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the "global" Pdu structure to allow harmonization of handle IDs in the COM-Stack.

######### 7. DoIPSoAdTcpRxPdu

**容器属性**:

- **UUID**: `ECUC:f8ff31c4-d60d-4316-b021-67cb31934ee7`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPSoAdTcpRxPdu`
- **多重性**: [1..1]

**容器描述**:

This container describes a Rx PDU received via SoAd over TCP

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. DoIPSoAdTcpRxPduId

- **UUID**: `ECUC:87bc6f78-b949-44dd-a958-16f6c2003d78`
- **参数名**: `DoIPSoAdTcpRxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **描述**: The DoIPSoAdTcpRxPduId is required by the API call DoIP_SoAdTpRxIndication to receive I-PDUs from the SoAd.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. DoIPSoAdTcpRxPduRef

- **UUID**: `ECUC:7fa9533f-a369-48ce-8666-1982b51d007d`
- **引用名**: `DoIPSoAdTcpRxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the "global" Pdu structure to allow harmonization of handle IDs in the COM-Stack.

######### 8. DoIPSoAdTcpTxPdu

**容器属性**:

- **UUID**: `ECUC:b94850e4-7ec7-4c7a-95d7-e883570c386f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPSoAdTcpTxPdu`
- **多重性**: [1..1]

**容器描述**:

This container describes a Tx PDU sent via SoAd over TCP

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. DoIPSoAdTcpTxPduId

- **UUID**: `ECUC:18866fc8-b1b6-4749-866c-8d0dff665d6e`
- **参数名**: `DoIPSoAdTcpTxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **描述**: The DoIPSoAdTcpTxPduId is required by the API call DoIP_SoAdTpTxConfirmation that is called by the SoAd to confirm that the IPdu has been transmitted successfully.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. DoIPSoAdTcpTxPduRef

- **UUID**: `ECUC:71678586-2f21-4e4f-aefc-997db5b282a4`
- **引用名**: `DoIPSoAdTcpTxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the "global" Pdu structure to allow harmonization of handle IDs in the COM-Stack.

######### 9. DoIPUdpConnection

**容器属性**:

- **UUID**: `ECUC:113b6883-6d62-4e20-9cb6-680252dad2b0`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPUdpConnection`
- **多重性**: [1..255]

**容器描述**:

This Container describes a Udp connection to the lower layer SoAd module.

########## 参数配置

此容器包含 **1** 个参数：

########### BOOLEAN 类型参数

############ 1. DoIPRequestAddressAssignment

- **UUID**: `ECUC:8d1ae703-ec0c-9471-4b05-edd862510501`
- **参数名**: `DoIPRequestAddressAssignment`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: The DoIP module shall request IP address assignment by calling SoAd_RequestIpAddrAssignment() for the TcpIpLocalAddr related to this DoIpConnection.

########## 配置容器

本模块包含 **2** 个配置容器：

########### 1. DoIPSoAdUdpRxPdu

**容器属性**:

- **UUID**: `ECUC:799689c9-1f1f-4245-8228-18b7bf0c2dee`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPSoAdUdpRxPdu`
- **多重性**: [1..1]

**容器描述**:

This container describes a Rx PDU received via SoAd over UDP.

############ 参数配置

此容器包含 **1** 个参数：

############# INTEGER 类型参数

############## 1. DoIPSoAdUdpRxPduId

- **UUID**: `ECUC:103f1b68-c87a-4b28-ad2b-a9a27b600be2`
- **参数名**: `DoIPSoAdUdpRxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **描述**: The DoIPSoAdUdpRxPduId is required by the API call DoIP_SoAdIfRxIndication to receive I-PDUs from the SoAd.

############ 引用关系

此容器包含 **1** 个引用：

############# REFERENCE 类型引用

############## 1. DoIPSoAdUdpRxPduRef

- **UUID**: `ECUC:fd7f5cdf-7cf4-45f4-a627-2d343a8f7ed5`
- **引用名**: `DoIPSoAdUdpRxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the "global" Pdu structure to allow harmonization of handle IDs in the COM-Stack.

########### 2. DoIPSoAdUdpTxPdu

**容器属性**:

- **UUID**: `ECUC:b3d21ded-7966-4862-8d48-ddf2775239cc`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPSoAdUdpTxPdu`
- **多重性**: [1..1]

**容器描述**:

This container describes a Tx PDU sent via SoAd over UDP.

############ 参数配置

此容器包含 **1** 个参数：

############# INTEGER 类型参数

############## 1. DoIPSoAdUdpTxPduId

- **UUID**: `ECUC:2f55a1ec-664b-4bd6-9da3-2f80f2a73746`
- **参数名**: `DoIPSoAdUdpTxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **描述**: The DoIPSoAdUdpTxPduId is required by the API call DoIP_SoAdIfTxConfirmation that is called by the SoAd to confirm that the IPdu has been transmitted successfully.

############ 引用关系

此容器包含 **1** 个引用：

############# REFERENCE 类型引用

############## 1. DoIPSoAdUdpTxPduRef

- **UUID**: `ECUC:c31e5dee-28e5-4b32-8cec-51f54e77a3a3`
- **引用名**: `DoIPSoAdUdpTxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the "global" Pdu structure to allow harmonization of handle IDs in the COM-Stack.

######### 10. DoIPSoAdUdpRxPdu

**容器属性**:

- **UUID**: `ECUC:799689c9-1f1f-4245-8228-18b7bf0c2dee`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPSoAdUdpRxPdu`
- **多重性**: [1..1]

**容器描述**:

This container describes a Rx PDU received via SoAd over UDP.

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. DoIPSoAdUdpRxPduId

- **UUID**: `ECUC:103f1b68-c87a-4b28-ad2b-a9a27b600be2`
- **参数名**: `DoIPSoAdUdpRxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **描述**: The DoIPSoAdUdpRxPduId is required by the API call DoIP_SoAdIfRxIndication to receive I-PDUs from the SoAd.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. DoIPSoAdUdpRxPduRef

- **UUID**: `ECUC:fd7f5cdf-7cf4-45f4-a627-2d343a8f7ed5`
- **引用名**: `DoIPSoAdUdpRxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the "global" Pdu structure to allow harmonization of handle IDs in the COM-Stack.

######### 11. DoIPSoAdUdpTxPdu

**容器属性**:

- **UUID**: `ECUC:b3d21ded-7966-4862-8d48-ddf2775239cc`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPSoAdUdpTxPdu`
- **多重性**: [1..1]

**容器描述**:

This container describes a Tx PDU sent via SoAd over UDP.

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. DoIPSoAdUdpTxPduId

- **UUID**: `ECUC:2f55a1ec-664b-4bd6-9da3-2f80f2a73746`
- **参数名**: `DoIPSoAdUdpTxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **描述**: The DoIPSoAdUdpTxPduId is required by the API call DoIP_SoAdIfTxConfirmation that is called by the SoAd to confirm that the IPdu has been transmitted successfully.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. DoIPSoAdUdpTxPduRef

- **UUID**: `ECUC:c31e5dee-28e5-4b32-8cec-51f54e77a3a3`
- **引用名**: `DoIPSoAdUdpTxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the "global" Pdu structure to allow harmonization of handle IDs in the COM-Stack.

######### 12. DoIPUdpVehicleAnnouncementConnection

**容器属性**:

- **UUID**: `ECUC:ec10775c-9dc4-49d9-b17b-73c202f875ed`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPUdpVehicleAnnouncementConnection`
- **多重性**: [1..255]

**容器描述**:

This container describes the UDP multicast connections to the lower layer SoAd module.

########## 参数配置

此容器包含 **1** 个参数：

########### BOOLEAN 类型参数

############ 1. DoIPRequestAddressAssignment

- **UUID**: `ECUC:67eff5dd-1c6e-902a-5fca-f998126ea83e`
- **参数名**: `DoIPRequestAddressAssignment`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: The DoIP module shall request IP address assignment by calling SoAd_RequestIpAddrAssignment() for the TcpIpLocalAddr related to this DoIpConnection.

########## 配置容器

本模块包含 **1** 个配置容器：

########### 1. DoIPSoAdUdpVehicleAnnouncementTxPdu

**容器属性**:

- **UUID**: `ECUC:ca2c98f1-142e-4d74-b3e2-a2c7a5d2a5a7`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPSoAdUdpVehicleAnnouncementTxPdu`
- **多重性**: [1..1]

**容器描述**:

This container describes the vehicle announcement TxPdu sent via the SoAd.

############ 参数配置

此容器包含 **1** 个参数：

############# INTEGER 类型参数

############## 1. DoIPSoAdUdpVehicleAnnouncementTxPduId

- **UUID**: `ECUC:d714703b-f033-4dcf-91de-1b6f531e9af7`
- **参数名**: `DoIPSoAdUdpVehicleAnnouncementTxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **描述**: The DoIPSoAdUdpVehicleAnnouncementTxPduId is required by the API call DoIP_SoAdIfTxConfirmation() that is called by the SoAd to confirm that the IPdu has been transmitted successfully.

############ 引用关系

此容器包含 **1** 个引用：

############# REFERENCE 类型引用

############## 1. DoIPSoAdUdpVehicleAnnouncementTxPduRef

- **UUID**: `ECUC:90da376e-29ea-4262-aa92-05bf32a3971e`
- **引用名**: `DoIPSoAdUdpVehicleAnnouncementTxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the "global" PDU structure to allow harmonization of handle IDs in the COM-Stack.

######### 13. DoIPSoAdUdpVehicleAnnouncementTxPdu

**容器属性**:

- **UUID**: `ECUC:ca2c98f1-142e-4d74-b3e2-a2c7a5d2a5a7`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPSoAdUdpVehicleAnnouncementTxPdu`
- **多重性**: [1..1]

**容器描述**:

This container describes the vehicle announcement TxPdu sent via the SoAd.

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. DoIPSoAdUdpVehicleAnnouncementTxPduId

- **UUID**: `ECUC:d714703b-f033-4dcf-91de-1b6f531e9af7`
- **参数名**: `DoIPSoAdUdpVehicleAnnouncementTxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **描述**: The DoIPSoAdUdpVehicleAnnouncementTxPduId is required by the API call DoIP_SoAdIfTxConfirmation() that is called by the SoAd to confirm that the IPdu has been transmitted successfully.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. DoIPSoAdUdpVehicleAnnouncementTxPduRef

- **UUID**: `ECUC:90da376e-29ea-4262-aa92-05bf32a3971e`
- **引用名**: `DoIPSoAdUdpVehicleAnnouncementTxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the "global" PDU structure to allow harmonization of handle IDs in the COM-Stack.

######### 14. DoIPFurtherActionByteCallback

**容器属性**:

- **UUID**: `ECUC:5aac8f6a-2a4d-4d01-af2e-645e910e158d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPFurtherActionByteCallback`
- **多重性**: [0..1]

**容器描述**:

This container describes the Callbackfunction to get the Further Action byte. This container shall always be present. If the DoIPFurtherActionByteDirect parameter is not present, the DoIP module will use an RPort of ServiceInterface CallbackGetFurtherActionByte with the name "CBGetFurtherActionByte_<shortname of enclosing DoIPInterface container>".

########## 参数配置

此容器包含 **1** 个参数：

########### FUNCTION-NAME 类型参数

############ 1. DoIPFurtherActionByteDirect

- **UUID**: `ECUC:b16ec364-7eb2-447e-ad3a-c55fe58378cb`
- **参数名**: `DoIPFurtherActionByteDirect`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **函数变体**:
- **描述**: Direct C Callback function to get the OEM specific Further Action Byte for the DoIP vehicle identification response/vehicle announcement. If the DoIPFurtherActionByteDirect parameter is present, the DoIP module will not use an RPort of ServiceInterface "CBGetFurtherActionByte" but will call the configured function.

######### 15. DoIPRoutingActivation

**容器属性**:

- **UUID**: `ECUC:8c07e2b0-4dd1-45fc-89ae-19a97da7e734`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPRoutingActivation`
- **多重性**: [0..255]

**容器描述**:

This container describes the routing activation possibilities by representing for each container a possible routing activation request message to the DoIP entity and the according references to the activated diagnostic messages.

########## 参数配置

此容器包含 **2** 个参数：

########### INTEGER 类型参数

############ 1. DoIPRoutingActivationNumber

- **UUID**: `ECUC:335e310b-8d47-48bf-b643-5c12468a5f01`
- **参数名**: `DoIPRoutingActivationNumber`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Identifies the Routing activation Number which is received for a DoIP routing activation request message.

########### BOOLEAN 类型参数

############ 1. DoIPRoutingActivationSecurityRequired

- **UUID**: `ECUC:d645dea9-213c-4ac7-9407-a6cc7586ae8f`
- **参数名**: `DoIPRoutingActivationSecurityRequired`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Indicates if a routing activation requires a secure TCP connection

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. DoIPTargetAddressRef

- **UUID**: `ECUC:ebc9f44b-f588-4a77-a371-08bfa7d33272`
- **引用名**: `DoIPTargetAddressRef`
- **引用类型**: REFERENCE
- **多重性**: [1..65535]
- **目标**: `DoIPTargetAddress`
- **完整路径**: `/AUTOSAR/EcucDefs/DoIP/DoIPConfigSet/DoIPInterface/DoIPConnections/DoIPTargetAddress`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to all DoIPTargetAddress which are activated on this Routing activation.

########## 配置容器

本模块包含 **2** 个配置容器：

########### 1. DoIPRoutingActivationAuthenticationCallback

**容器属性**:

- **UUID**: `ECUC:726377c7-0039-4edc-b57c-dd98bc5e99b7`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPRoutingActivationAuthenticationCallback`
- **多重性**: [0..1]

**容器描述**:

Container describes the Callbackfunction to call on a Routing Activation Request for Authentication. If this container is configured but the DoIPRoutingActivationAuthenticationFunc parameter is not present, the DoIP module will use an RPort of ServiceInterface <RoutingActivation>_RoutingActivation with the name "CB<RoutingActivation>RoutingActivation". <RoutingActivation> is the ShortName of the DoIPRoutingActiviation container.

############ 参数配置

此容器包含 **3** 个参数：

############# INTEGER 类型参数

############## 1. DoIPRoutingActivationAuthenticationReqLength

- **UUID**: `ECUC:2abdcf96-9b8e-4936-afc0-ede76b21f3a7`
- **参数名**: `DoIPRoutingActivationAuthenticationReqLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Describes the amount of bytes used to handle to the authentication function on routing activation. If 0 is configured as length the parameter AuthenticationReqData will not be handled to the API.

############## 2. DoIPRoutingActivationAuthenticationResLength

- **UUID**: `ECUC:45e1fc22-6491-40ed-87b8-7917007771a8`
- **参数名**: `DoIPRoutingActivationAuthenticationResLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Describes the amount of bytes used to read by the authentication function on routing activation. If 0 is configured as length the parameter AuthenticationResData will not be fetched via the API.

############# FUNCTION-NAME 类型参数

############## 1. DoIPRoutingActivationAuthenticationFunc

- **UUID**: `ECUC:05ef7a06-64da-467c-be24-d40bac66acc3`
- **参数名**: `DoIPRoutingActivationAuthenticationFunc`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **函数变体**:
- **描述**: Direct C Callback function to trigger the authentication function for routing activation. If the DoIPRoutingActivationAuthenticationFunc parameter is present, the DoIP module will not use an RPort of ServiceInterface <RoutingActivation>_RoutingActivation but call the configured function.

########### 2. DoIPRoutingActivationConfirmationCallback

**容器属性**:

- **UUID**: `ECUC:7e1d1ce3-eff6-43ab-a071-e6b83dfa4855`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPRoutingActivationConfirmationCallback`
- **多重性**: [0..1]

**容器描述**:

Container describes the Callbackfunction to call on a Routing Activation Request for Confirmation. If this container is configured but the DoIPRoutingActivationConfirmationFunc parameter is not present the DoIP module will use an RPort of ServiceInterface <RoutingActivation>_RoutingActivation with the name "CB<RoutingActivation>RoutingActivation". <RoutingActivation> is the ShortName of the DoIPRoutingActiviation container.

############ 参数配置

此容器包含 **3** 个参数：

############# INTEGER 类型参数

############## 1. DoIPRoutingActivationConfirmationReqLength

- **UUID**: `ECUC:b5b1030f-ad9f-4bbf-b2a0-9674bf5f20a7`
- **参数名**: `DoIPRoutingActivationConfirmationReqLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Describes the amount of bytes used to handle to the confirmation function on routing activation. If 0 is configured as length the parameter ConfirmedReqData will not be handled to the API.

############## 2. DoIPRoutingActivationConfirmationResLength

- **UUID**: `ECUC:701e1997-d200-4ee4-8372-e5eb0dc94c56`
- **参数名**: `DoIPRoutingActivationConfirmationResLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Describes the amount of bytes used to read by the confirmation function on routing activation. If 0 is configured as length the parameter ConfirmedResData will not be fetched via the API.

############# FUNCTION-NAME 类型参数

############## 1. DoIPRoutingActivationConfirmationFunc

- **UUID**: `ECUC:4630dc00-f4e8-4bf0-b18c-1a98a4f2f7c9`
- **参数名**: `DoIPRoutingActivationConfirmationFunc`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **函数变体**:
- **描述**: Direct C Callback function to trigger the confirmation function for routing activation. If the DoIPRoutingActivationConfirmationFunc parameter is present the DoIP module will not use an RPort of ServiceInterface <RoutingActivation>_RoutingActivation but call the configured function.

######### 16. DoIPRoutingActivationAuthenticationCallback

**容器属性**:

- **UUID**: `ECUC:726377c7-0039-4edc-b57c-dd98bc5e99b7`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPRoutingActivationAuthenticationCallback`
- **多重性**: [0..1]

**容器描述**:

Container describes the Callbackfunction to call on a Routing Activation Request for Authentication. If this container is configured but the DoIPRoutingActivationAuthenticationFunc parameter is not present, the DoIP module will use an RPort of ServiceInterface <RoutingActivation>_RoutingActivation with the name "CB<RoutingActivation>RoutingActivation". <RoutingActivation> is the ShortName of the DoIPRoutingActiviation container.

########## 参数配置

此容器包含 **3** 个参数：

########### INTEGER 类型参数

############ 1. DoIPRoutingActivationAuthenticationReqLength

- **UUID**: `ECUC:2abdcf96-9b8e-4936-afc0-ede76b21f3a7`
- **参数名**: `DoIPRoutingActivationAuthenticationReqLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Describes the amount of bytes used to handle to the authentication function on routing activation. If 0 is configured as length the parameter AuthenticationReqData will not be handled to the API.

############ 2. DoIPRoutingActivationAuthenticationResLength

- **UUID**: `ECUC:45e1fc22-6491-40ed-87b8-7917007771a8`
- **参数名**: `DoIPRoutingActivationAuthenticationResLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Describes the amount of bytes used to read by the authentication function on routing activation. If 0 is configured as length the parameter AuthenticationResData will not be fetched via the API.

########### FUNCTION-NAME 类型参数

############ 1. DoIPRoutingActivationAuthenticationFunc

- **UUID**: `ECUC:05ef7a06-64da-467c-be24-d40bac66acc3`
- **参数名**: `DoIPRoutingActivationAuthenticationFunc`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **函数变体**:
- **描述**: Direct C Callback function to trigger the authentication function for routing activation. If the DoIPRoutingActivationAuthenticationFunc parameter is present, the DoIP module will not use an RPort of ServiceInterface <RoutingActivation>_RoutingActivation but call the configured function.

######### 17. DoIPRoutingActivationConfirmationCallback

**容器属性**:

- **UUID**: `ECUC:7e1d1ce3-eff6-43ab-a071-e6b83dfa4855`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPRoutingActivationConfirmationCallback`
- **多重性**: [0..1]

**容器描述**:

Container describes the Callbackfunction to call on a Routing Activation Request for Confirmation. If this container is configured but the DoIPRoutingActivationConfirmationFunc parameter is not present the DoIP module will use an RPort of ServiceInterface <RoutingActivation>_RoutingActivation with the name "CB<RoutingActivation>RoutingActivation". <RoutingActivation> is the ShortName of the DoIPRoutingActiviation container.

########## 参数配置

此容器包含 **3** 个参数：

########### INTEGER 类型参数

############ 1. DoIPRoutingActivationConfirmationReqLength

- **UUID**: `ECUC:b5b1030f-ad9f-4bbf-b2a0-9674bf5f20a7`
- **参数名**: `DoIPRoutingActivationConfirmationReqLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Describes the amount of bytes used to handle to the confirmation function on routing activation. If 0 is configured as length the parameter ConfirmedReqData will not be handled to the API.

############ 2. DoIPRoutingActivationConfirmationResLength

- **UUID**: `ECUC:701e1997-d200-4ee4-8372-e5eb0dc94c56`
- **参数名**: `DoIPRoutingActivationConfirmationResLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Describes the amount of bytes used to read by the confirmation function on routing activation. If 0 is configured as length the parameter ConfirmedResData will not be fetched via the API.

########### FUNCTION-NAME 类型参数

############ 1. DoIPRoutingActivationConfirmationFunc

- **UUID**: `ECUC:4630dc00-f4e8-4bf0-b18c-1a98a4f2f7c9`
- **参数名**: `DoIPRoutingActivationConfirmationFunc`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **函数变体**:
- **描述**: Direct C Callback function to trigger the confirmation function for routing activation. If the DoIPRoutingActivationConfirmationFunc parameter is present the DoIP module will not use an RPort of ServiceInterface <RoutingActivation>_RoutingActivation but call the configured function.

######### 18. DoIPTester

**容器属性**:

- **UUID**: `ECUC:5ec2063c-2a23-4da2-be67-e7cd0a80ee93`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPTester`
- **多重性**: [0..255]

**容器描述**:

This container describes the properties of the possible connectable Tester for the DoIP entity.

########## 参数配置

此容器包含 **2** 个参数：

########### INTEGER 类型参数

############ 1. DoIPNumByteDiagAckNack

- **UUID**: `ECUC:2cdb3b03-189a-4c0d-847c-ec5cbe717265`
- **参数名**: `DoIPNumByteDiagAckNack`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Specifies the number of original Diagnostic request bytes the DoIP entity responses on a NACK of a diagnostic response message to the Tester.

############ 2. DoIPTesterSA

- **UUID**: `ECUC:44ccb383-1ad0-47a4-a3c4-5056f05a922d`
- **参数名**: `DoIPTesterSA`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Source Address of the Tester sent via routing activation or diagnostic message.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. DoIPRoutingActivationRef

- **UUID**: `ECUC:cc241bfa-5d3c-4e9b-b190-f764add15a77`
- **引用名**: `DoIPRoutingActivationRef`
- **引用类型**: REFERENCE
- **多重性**: [1..255]
- **目标**: `DoIPRoutingActivation`
- **完整路径**: `/AUTOSAR/EcucDefs/DoIP/DoIPConfigSet/DoIPInterface/DoIPRoutingActivation`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to a DoIPRoutingActivation describing the possible routing activations of the DoIPTester

####### 2. DoIPChannel

**容器属性**:

- **UUID**: `ECUC:ce8927a0-58c7-4099-a996-3ee43001e9e8`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPChannel`
- **多重性**: [1..65536]

**容器描述**:

Configuration of one DoIPChannel.

######## 引用关系

此容器包含 **2** 个引用：

######### REFERENCE 类型引用

########## 1. DoIPChannelSARef

- **UUID**: `ECUC:893cf71a-c06b-4044-812c-8df50e45d13e`
- **引用名**: `DoIPChannelSARef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `DoIPTester`
- **完整路径**: `/AUTOSAR/EcucDefs/DoIP/DoIPConfigSet/DoIPInterface/DoIPTester`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the DoIPTester.

########## 2. DoIPChannelTARef

- **UUID**: `ECUC:cbe1685e-4306-4efc-8345-5a1446b28405`
- **引用名**: `DoIPChannelTARef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `DoIPTargetAddress`
- **完整路径**: `/AUTOSAR/EcucDefs/DoIP/DoIPConfigSet/DoIPInterface/DoIPConnections/DoIPTargetAddress`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the target address.

######## 配置容器

本模块包含 **2** 个配置容器：

######### 1. DoIPPduRRxPdu

**容器属性**:

- **UUID**: `ECUC:63341ec1-b4ca-4bbc-82b5-a883d528b7c1`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPPduRRxPdu`
- **多重性**: [0..1]

**容器描述**:

This container contains the Rx Pdus to connect with the Rx Pdus of the PduR.

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. DoIPPduRRxPduId

- **UUID**: `ECUC:affbfe09-cf4f-43ed-91f0-957c1e71f17f`
- **参数名**: `DoIPPduRRxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **描述**: The DoIPPduRRxPduId is required by the API call DoIP_TpCancelReceive.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. DoIPPduRRxPduRef

- **UUID**: `ECUC:0fb53490-8f12-418b-a048-feaf0c60d6b0`
- **引用名**: `DoIPPduRRxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the "global" Pdu structure to allow harmonization of handle IDs in the COM-Stack.

######### 2. DoIPPduRTxPdu

**容器属性**:

- **UUID**: `ECUC:ecf769bc-a264-4426-a107-185d357d42b4`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPPduRTxPdu`
- **多重性**: [0..1]

**容器描述**:

This container contains the Tx Pdus to connect with the Tx Pdus of the PduR.  If the parameter is not configured the channel is for functional addressing.

########## 参数配置

此容器包含 **2** 个参数：

########### INTEGER 类型参数

############ 1. DoIPPduRTxPduId

- **UUID**: `ECUC:4ec22559-5780-41ca-af56-0b32ecdd6dae`
- **参数名**: `DoIPPduRTxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **描述**: The DoIPPduRTxPduId is required by DoIP_TpTransmit or DoIP_IfTransmit and DoIP_TpCancelTransmit.

########### ENUMERATION 类型参数

############ 1. DoIPPduType

- **UUID**: `ECUC:17c8aace-cda8-471d-8cb2-e474dda9c61a`
- **参数名**: `DoIPPduType`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `DOIP_TPPDU`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `DOIP_IFPDU` (来源: AUTOSAR_ECUC)
  - `DOIP_TPPDU` (来源: AUTOSAR_ECUC)
- **描述**: API Type to use for communication with PduR. DOIP_IFPDU for UUDT messages, DOIP_TPPDU for all other diagnostic messages.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. DoIPPduRTxPduRef

- **UUID**: `ECUC:f703fb82-d2e7-4545-a97c-3275ff0bfc5d`
- **引用名**: `DoIPPduRTxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the "global" Pdu structure to allow harmonization of handle IDs in the COM-Stack.

####### 3. DoIPPduRRxPdu

**容器属性**:

- **UUID**: `ECUC:63341ec1-b4ca-4bbc-82b5-a883d528b7c1`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPPduRRxPdu`
- **多重性**: [0..1]

**容器描述**:

This container contains the Rx Pdus to connect with the Rx Pdus of the PduR.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. DoIPPduRRxPduId

- **UUID**: `ECUC:affbfe09-cf4f-43ed-91f0-957c1e71f17f`
- **参数名**: `DoIPPduRRxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **描述**: The DoIPPduRRxPduId is required by the API call DoIP_TpCancelReceive.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. DoIPPduRRxPduRef

- **UUID**: `ECUC:0fb53490-8f12-418b-a048-feaf0c60d6b0`
- **引用名**: `DoIPPduRRxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the "global" Pdu structure to allow harmonization of handle IDs in the COM-Stack.

####### 4. DoIPPduRTxPdu

**容器属性**:

- **UUID**: `ECUC:ecf769bc-a264-4426-a107-185d357d42b4`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPPduRTxPdu`
- **多重性**: [0..1]

**容器描述**:

This container contains the Tx Pdus to connect with the Tx Pdus of the PduR.  If the parameter is not configured the channel is for functional addressing.

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. DoIPPduRTxPduId

- **UUID**: `ECUC:4ec22559-5780-41ca-af56-0b32ecdd6dae`
- **参数名**: `DoIPPduRTxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **描述**: The DoIPPduRTxPduId is required by DoIP_TpTransmit or DoIP_IfTransmit and DoIP_TpCancelTransmit.

######### ENUMERATION 类型参数

########## 1. DoIPPduType

- **UUID**: `ECUC:17c8aace-cda8-471d-8cb2-e474dda9c61a`
- **参数名**: `DoIPPduType`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `DOIP_TPPDU`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `DOIP_IFPDU` (来源: AUTOSAR_ECUC)
  - `DOIP_TPPDU` (来源: AUTOSAR_ECUC)
- **描述**: API Type to use for communication with PduR. DOIP_IFPDU for UUDT messages, DOIP_TPPDU for all other diagnostic messages.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. DoIPPduRTxPduRef

- **UUID**: `ECUC:f703fb82-d2e7-4545-a97c-3275ff0bfc5d`
- **引用名**: `DoIPPduRTxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the "global" Pdu structure to allow harmonization of handle IDs in the COM-Stack.

####### 5. DoIPConnections

**容器属性**:

- **UUID**: `ECUC:06a174a5-5ad6-4b7a-8ce8-c64883f2e5c5`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPConnections`
- **多重性**: [1..1]

**容器描述**:

Container contains all lower layer connection specific information, i.e. the single Pdu References and Handle IDs to the SoAd.

######## 配置容器

本模块包含 **9** 个配置容器：

######### 1. DoIPTargetAddress

**容器属性**:

- **UUID**: `ECUC:11b8faaf-bc59-49fe-97b5-29df73fa6ee7`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPTargetAddress`
- **多重性**: [1..65535]

**容器描述**:

This container describes a possible TargetAddress that is supported by DoIP.

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. DoIPTargetAddressValue

- **UUID**: `ECUC:c46011a4-ab1a-42cf-a2f8-b71632fcfd59`
- **参数名**: `DoIPTargetAddressValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Valid Target Address of a DoIP target address.

######### 2. DoIPTcpConnection

**容器属性**:

- **UUID**: `ECUC:e3ccdc1d-8a6b-40a0-abbf-59a1db67e267`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPTcpConnection`
- **多重性**: [1..255]

**容器描述**:

This container describes a TCP connection to the lower layer SoAd module.

########## 参数配置

此容器包含 **2** 个参数：

########### BOOLEAN 类型参数

############ 1. DoIPRequestAddressAssignment

- **UUID**: `ECUC:5fac5a9e-0915-86f1-5a0e-df77eade14b8`
- **参数名**: `DoIPRequestAddressAssignment`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: The DoIP module shall request IP address assignment by calling SoAd_RequestIpAddrAssignment() for the TcpIpLocalAddr related to this DoIpConnection.

############ 2. DoIPTcpConnectionSecurityRequired

- **UUID**: `ECUC:e723d1bf-784e-4527-892c-4fcbf9e11e05`
- **参数名**: `DoIPTcpConnectionSecurityRequired`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Indicates if the associated TCP socket uses a secure connection (e.g. TLS)

########## 配置容器

本模块包含 **2** 个配置容器：

########### 1. DoIPSoAdTcpRxPdu

**容器属性**:

- **UUID**: `ECUC:f8ff31c4-d60d-4316-b021-67cb31934ee7`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPSoAdTcpRxPdu`
- **多重性**: [1..1]

**容器描述**:

This container describes a Rx PDU received via SoAd over TCP

############ 参数配置

此容器包含 **1** 个参数：

############# INTEGER 类型参数

############## 1. DoIPSoAdTcpRxPduId

- **UUID**: `ECUC:87bc6f78-b949-44dd-a958-16f6c2003d78`
- **参数名**: `DoIPSoAdTcpRxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **描述**: The DoIPSoAdTcpRxPduId is required by the API call DoIP_SoAdTpRxIndication to receive I-PDUs from the SoAd.

############ 引用关系

此容器包含 **1** 个引用：

############# REFERENCE 类型引用

############## 1. DoIPSoAdTcpRxPduRef

- **UUID**: `ECUC:7fa9533f-a369-48ce-8666-1982b51d007d`
- **引用名**: `DoIPSoAdTcpRxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the "global" Pdu structure to allow harmonization of handle IDs in the COM-Stack.

########### 2. DoIPSoAdTcpTxPdu

**容器属性**:

- **UUID**: `ECUC:b94850e4-7ec7-4c7a-95d7-e883570c386f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPSoAdTcpTxPdu`
- **多重性**: [1..1]

**容器描述**:

This container describes a Tx PDU sent via SoAd over TCP

############ 参数配置

此容器包含 **1** 个参数：

############# INTEGER 类型参数

############## 1. DoIPSoAdTcpTxPduId

- **UUID**: `ECUC:18866fc8-b1b6-4749-866c-8d0dff665d6e`
- **参数名**: `DoIPSoAdTcpTxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **描述**: The DoIPSoAdTcpTxPduId is required by the API call DoIP_SoAdTpTxConfirmation that is called by the SoAd to confirm that the IPdu has been transmitted successfully.

############ 引用关系

此容器包含 **1** 个引用：

############# REFERENCE 类型引用

############## 1. DoIPSoAdTcpTxPduRef

- **UUID**: `ECUC:71678586-2f21-4e4f-aefc-997db5b282a4`
- **引用名**: `DoIPSoAdTcpTxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the "global" Pdu structure to allow harmonization of handle IDs in the COM-Stack.

######### 3. DoIPSoAdTcpRxPdu

**容器属性**:

- **UUID**: `ECUC:f8ff31c4-d60d-4316-b021-67cb31934ee7`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPSoAdTcpRxPdu`
- **多重性**: [1..1]

**容器描述**:

This container describes a Rx PDU received via SoAd over TCP

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. DoIPSoAdTcpRxPduId

- **UUID**: `ECUC:87bc6f78-b949-44dd-a958-16f6c2003d78`
- **参数名**: `DoIPSoAdTcpRxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **描述**: The DoIPSoAdTcpRxPduId is required by the API call DoIP_SoAdTpRxIndication to receive I-PDUs from the SoAd.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. DoIPSoAdTcpRxPduRef

- **UUID**: `ECUC:7fa9533f-a369-48ce-8666-1982b51d007d`
- **引用名**: `DoIPSoAdTcpRxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the "global" Pdu structure to allow harmonization of handle IDs in the COM-Stack.

######### 4. DoIPSoAdTcpTxPdu

**容器属性**:

- **UUID**: `ECUC:b94850e4-7ec7-4c7a-95d7-e883570c386f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPSoAdTcpTxPdu`
- **多重性**: [1..1]

**容器描述**:

This container describes a Tx PDU sent via SoAd over TCP

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. DoIPSoAdTcpTxPduId

- **UUID**: `ECUC:18866fc8-b1b6-4749-866c-8d0dff665d6e`
- **参数名**: `DoIPSoAdTcpTxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **描述**: The DoIPSoAdTcpTxPduId is required by the API call DoIP_SoAdTpTxConfirmation that is called by the SoAd to confirm that the IPdu has been transmitted successfully.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. DoIPSoAdTcpTxPduRef

- **UUID**: `ECUC:71678586-2f21-4e4f-aefc-997db5b282a4`
- **引用名**: `DoIPSoAdTcpTxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the "global" Pdu structure to allow harmonization of handle IDs in the COM-Stack.

######### 5. DoIPUdpConnection

**容器属性**:

- **UUID**: `ECUC:113b6883-6d62-4e20-9cb6-680252dad2b0`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPUdpConnection`
- **多重性**: [1..255]

**容器描述**:

This Container describes a Udp connection to the lower layer SoAd module.

########## 参数配置

此容器包含 **1** 个参数：

########### BOOLEAN 类型参数

############ 1. DoIPRequestAddressAssignment

- **UUID**: `ECUC:8d1ae703-ec0c-9471-4b05-edd862510501`
- **参数名**: `DoIPRequestAddressAssignment`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: The DoIP module shall request IP address assignment by calling SoAd_RequestIpAddrAssignment() for the TcpIpLocalAddr related to this DoIpConnection.

########## 配置容器

本模块包含 **2** 个配置容器：

########### 1. DoIPSoAdUdpRxPdu

**容器属性**:

- **UUID**: `ECUC:799689c9-1f1f-4245-8228-18b7bf0c2dee`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPSoAdUdpRxPdu`
- **多重性**: [1..1]

**容器描述**:

This container describes a Rx PDU received via SoAd over UDP.

############ 参数配置

此容器包含 **1** 个参数：

############# INTEGER 类型参数

############## 1. DoIPSoAdUdpRxPduId

- **UUID**: `ECUC:103f1b68-c87a-4b28-ad2b-a9a27b600be2`
- **参数名**: `DoIPSoAdUdpRxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **描述**: The DoIPSoAdUdpRxPduId is required by the API call DoIP_SoAdIfRxIndication to receive I-PDUs from the SoAd.

############ 引用关系

此容器包含 **1** 个引用：

############# REFERENCE 类型引用

############## 1. DoIPSoAdUdpRxPduRef

- **UUID**: `ECUC:fd7f5cdf-7cf4-45f4-a627-2d343a8f7ed5`
- **引用名**: `DoIPSoAdUdpRxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the "global" Pdu structure to allow harmonization of handle IDs in the COM-Stack.

########### 2. DoIPSoAdUdpTxPdu

**容器属性**:

- **UUID**: `ECUC:b3d21ded-7966-4862-8d48-ddf2775239cc`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPSoAdUdpTxPdu`
- **多重性**: [1..1]

**容器描述**:

This container describes a Tx PDU sent via SoAd over UDP.

############ 参数配置

此容器包含 **1** 个参数：

############# INTEGER 类型参数

############## 1. DoIPSoAdUdpTxPduId

- **UUID**: `ECUC:2f55a1ec-664b-4bd6-9da3-2f80f2a73746`
- **参数名**: `DoIPSoAdUdpTxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **描述**: The DoIPSoAdUdpTxPduId is required by the API call DoIP_SoAdIfTxConfirmation that is called by the SoAd to confirm that the IPdu has been transmitted successfully.

############ 引用关系

此容器包含 **1** 个引用：

############# REFERENCE 类型引用

############## 1. DoIPSoAdUdpTxPduRef

- **UUID**: `ECUC:c31e5dee-28e5-4b32-8cec-51f54e77a3a3`
- **引用名**: `DoIPSoAdUdpTxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the "global" Pdu structure to allow harmonization of handle IDs in the COM-Stack.

######### 6. DoIPSoAdUdpRxPdu

**容器属性**:

- **UUID**: `ECUC:799689c9-1f1f-4245-8228-18b7bf0c2dee`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPSoAdUdpRxPdu`
- **多重性**: [1..1]

**容器描述**:

This container describes a Rx PDU received via SoAd over UDP.

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. DoIPSoAdUdpRxPduId

- **UUID**: `ECUC:103f1b68-c87a-4b28-ad2b-a9a27b600be2`
- **参数名**: `DoIPSoAdUdpRxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **描述**: The DoIPSoAdUdpRxPduId is required by the API call DoIP_SoAdIfRxIndication to receive I-PDUs from the SoAd.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. DoIPSoAdUdpRxPduRef

- **UUID**: `ECUC:fd7f5cdf-7cf4-45f4-a627-2d343a8f7ed5`
- **引用名**: `DoIPSoAdUdpRxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the "global" Pdu structure to allow harmonization of handle IDs in the COM-Stack.

######### 7. DoIPSoAdUdpTxPdu

**容器属性**:

- **UUID**: `ECUC:b3d21ded-7966-4862-8d48-ddf2775239cc`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPSoAdUdpTxPdu`
- **多重性**: [1..1]

**容器描述**:

This container describes a Tx PDU sent via SoAd over UDP.

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. DoIPSoAdUdpTxPduId

- **UUID**: `ECUC:2f55a1ec-664b-4bd6-9da3-2f80f2a73746`
- **参数名**: `DoIPSoAdUdpTxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **描述**: The DoIPSoAdUdpTxPduId is required by the API call DoIP_SoAdIfTxConfirmation that is called by the SoAd to confirm that the IPdu has been transmitted successfully.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. DoIPSoAdUdpTxPduRef

- **UUID**: `ECUC:c31e5dee-28e5-4b32-8cec-51f54e77a3a3`
- **引用名**: `DoIPSoAdUdpTxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the "global" Pdu structure to allow harmonization of handle IDs in the COM-Stack.

######### 8. DoIPUdpVehicleAnnouncementConnection

**容器属性**:

- **UUID**: `ECUC:ec10775c-9dc4-49d9-b17b-73c202f875ed`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPUdpVehicleAnnouncementConnection`
- **多重性**: [1..255]

**容器描述**:

This container describes the UDP multicast connections to the lower layer SoAd module.

########## 参数配置

此容器包含 **1** 个参数：

########### BOOLEAN 类型参数

############ 1. DoIPRequestAddressAssignment

- **UUID**: `ECUC:67eff5dd-1c6e-902a-5fca-f998126ea83e`
- **参数名**: `DoIPRequestAddressAssignment`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: The DoIP module shall request IP address assignment by calling SoAd_RequestIpAddrAssignment() for the TcpIpLocalAddr related to this DoIpConnection.

########## 配置容器

本模块包含 **1** 个配置容器：

########### 1. DoIPSoAdUdpVehicleAnnouncementTxPdu

**容器属性**:

- **UUID**: `ECUC:ca2c98f1-142e-4d74-b3e2-a2c7a5d2a5a7`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPSoAdUdpVehicleAnnouncementTxPdu`
- **多重性**: [1..1]

**容器描述**:

This container describes the vehicle announcement TxPdu sent via the SoAd.

############ 参数配置

此容器包含 **1** 个参数：

############# INTEGER 类型参数

############## 1. DoIPSoAdUdpVehicleAnnouncementTxPduId

- **UUID**: `ECUC:d714703b-f033-4dcf-91de-1b6f531e9af7`
- **参数名**: `DoIPSoAdUdpVehicleAnnouncementTxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **描述**: The DoIPSoAdUdpVehicleAnnouncementTxPduId is required by the API call DoIP_SoAdIfTxConfirmation() that is called by the SoAd to confirm that the IPdu has been transmitted successfully.

############ 引用关系

此容器包含 **1** 个引用：

############# REFERENCE 类型引用

############## 1. DoIPSoAdUdpVehicleAnnouncementTxPduRef

- **UUID**: `ECUC:90da376e-29ea-4262-aa92-05bf32a3971e`
- **引用名**: `DoIPSoAdUdpVehicleAnnouncementTxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the "global" PDU structure to allow harmonization of handle IDs in the COM-Stack.

######### 9. DoIPSoAdUdpVehicleAnnouncementTxPdu

**容器属性**:

- **UUID**: `ECUC:ca2c98f1-142e-4d74-b3e2-a2c7a5d2a5a7`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPSoAdUdpVehicleAnnouncementTxPdu`
- **多重性**: [1..1]

**容器描述**:

This container describes the vehicle announcement TxPdu sent via the SoAd.

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. DoIPSoAdUdpVehicleAnnouncementTxPduId

- **UUID**: `ECUC:d714703b-f033-4dcf-91de-1b6f531e9af7`
- **参数名**: `DoIPSoAdUdpVehicleAnnouncementTxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **描述**: The DoIPSoAdUdpVehicleAnnouncementTxPduId is required by the API call DoIP_SoAdIfTxConfirmation() that is called by the SoAd to confirm that the IPdu has been transmitted successfully.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. DoIPSoAdUdpVehicleAnnouncementTxPduRef

- **UUID**: `ECUC:90da376e-29ea-4262-aa92-05bf32a3971e`
- **引用名**: `DoIPSoAdUdpVehicleAnnouncementTxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the "global" PDU structure to allow harmonization of handle IDs in the COM-Stack.

####### 6. DoIPTargetAddress

**容器属性**:

- **UUID**: `ECUC:11b8faaf-bc59-49fe-97b5-29df73fa6ee7`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPTargetAddress`
- **多重性**: [1..65535]

**容器描述**:

This container describes a possible TargetAddress that is supported by DoIP.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. DoIPTargetAddressValue

- **UUID**: `ECUC:c46011a4-ab1a-42cf-a2f8-b71632fcfd59`
- **参数名**: `DoIPTargetAddressValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Valid Target Address of a DoIP target address.

####### 7. DoIPTcpConnection

**容器属性**:

- **UUID**: `ECUC:e3ccdc1d-8a6b-40a0-abbf-59a1db67e267`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPTcpConnection`
- **多重性**: [1..255]

**容器描述**:

This container describes a TCP connection to the lower layer SoAd module.

######## 参数配置

此容器包含 **2** 个参数：

######### BOOLEAN 类型参数

########## 1. DoIPRequestAddressAssignment

- **UUID**: `ECUC:5fac5a9e-0915-86f1-5a0e-df77eade14b8`
- **参数名**: `DoIPRequestAddressAssignment`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: The DoIP module shall request IP address assignment by calling SoAd_RequestIpAddrAssignment() for the TcpIpLocalAddr related to this DoIpConnection.

########## 2. DoIPTcpConnectionSecurityRequired

- **UUID**: `ECUC:e723d1bf-784e-4527-892c-4fcbf9e11e05`
- **参数名**: `DoIPTcpConnectionSecurityRequired`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Indicates if the associated TCP socket uses a secure connection (e.g. TLS)

######## 配置容器

本模块包含 **2** 个配置容器：

######### 1. DoIPSoAdTcpRxPdu

**容器属性**:

- **UUID**: `ECUC:f8ff31c4-d60d-4316-b021-67cb31934ee7`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPSoAdTcpRxPdu`
- **多重性**: [1..1]

**容器描述**:

This container describes a Rx PDU received via SoAd over TCP

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. DoIPSoAdTcpRxPduId

- **UUID**: `ECUC:87bc6f78-b949-44dd-a958-16f6c2003d78`
- **参数名**: `DoIPSoAdTcpRxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **描述**: The DoIPSoAdTcpRxPduId is required by the API call DoIP_SoAdTpRxIndication to receive I-PDUs from the SoAd.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. DoIPSoAdTcpRxPduRef

- **UUID**: `ECUC:7fa9533f-a369-48ce-8666-1982b51d007d`
- **引用名**: `DoIPSoAdTcpRxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the "global" Pdu structure to allow harmonization of handle IDs in the COM-Stack.

######### 2. DoIPSoAdTcpTxPdu

**容器属性**:

- **UUID**: `ECUC:b94850e4-7ec7-4c7a-95d7-e883570c386f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPSoAdTcpTxPdu`
- **多重性**: [1..1]

**容器描述**:

This container describes a Tx PDU sent via SoAd over TCP

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. DoIPSoAdTcpTxPduId

- **UUID**: `ECUC:18866fc8-b1b6-4749-866c-8d0dff665d6e`
- **参数名**: `DoIPSoAdTcpTxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **描述**: The DoIPSoAdTcpTxPduId is required by the API call DoIP_SoAdTpTxConfirmation that is called by the SoAd to confirm that the IPdu has been transmitted successfully.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. DoIPSoAdTcpTxPduRef

- **UUID**: `ECUC:71678586-2f21-4e4f-aefc-997db5b282a4`
- **引用名**: `DoIPSoAdTcpTxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the "global" Pdu structure to allow harmonization of handle IDs in the COM-Stack.

####### 8. DoIPSoAdTcpRxPdu

**容器属性**:

- **UUID**: `ECUC:f8ff31c4-d60d-4316-b021-67cb31934ee7`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPSoAdTcpRxPdu`
- **多重性**: [1..1]

**容器描述**:

This container describes a Rx PDU received via SoAd over TCP

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. DoIPSoAdTcpRxPduId

- **UUID**: `ECUC:87bc6f78-b949-44dd-a958-16f6c2003d78`
- **参数名**: `DoIPSoAdTcpRxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **描述**: The DoIPSoAdTcpRxPduId is required by the API call DoIP_SoAdTpRxIndication to receive I-PDUs from the SoAd.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. DoIPSoAdTcpRxPduRef

- **UUID**: `ECUC:7fa9533f-a369-48ce-8666-1982b51d007d`
- **引用名**: `DoIPSoAdTcpRxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the "global" Pdu structure to allow harmonization of handle IDs in the COM-Stack.

####### 9. DoIPSoAdTcpTxPdu

**容器属性**:

- **UUID**: `ECUC:b94850e4-7ec7-4c7a-95d7-e883570c386f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPSoAdTcpTxPdu`
- **多重性**: [1..1]

**容器描述**:

This container describes a Tx PDU sent via SoAd over TCP

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. DoIPSoAdTcpTxPduId

- **UUID**: `ECUC:18866fc8-b1b6-4749-866c-8d0dff665d6e`
- **参数名**: `DoIPSoAdTcpTxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **描述**: The DoIPSoAdTcpTxPduId is required by the API call DoIP_SoAdTpTxConfirmation that is called by the SoAd to confirm that the IPdu has been transmitted successfully.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. DoIPSoAdTcpTxPduRef

- **UUID**: `ECUC:71678586-2f21-4e4f-aefc-997db5b282a4`
- **引用名**: `DoIPSoAdTcpTxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the "global" Pdu structure to allow harmonization of handle IDs in the COM-Stack.

####### 10. DoIPUdpConnection

**容器属性**:

- **UUID**: `ECUC:113b6883-6d62-4e20-9cb6-680252dad2b0`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPUdpConnection`
- **多重性**: [1..255]

**容器描述**:

This Container describes a Udp connection to the lower layer SoAd module.

######## 参数配置

此容器包含 **1** 个参数：

######### BOOLEAN 类型参数

########## 1. DoIPRequestAddressAssignment

- **UUID**: `ECUC:8d1ae703-ec0c-9471-4b05-edd862510501`
- **参数名**: `DoIPRequestAddressAssignment`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: The DoIP module shall request IP address assignment by calling SoAd_RequestIpAddrAssignment() for the TcpIpLocalAddr related to this DoIpConnection.

######## 配置容器

本模块包含 **2** 个配置容器：

######### 1. DoIPSoAdUdpRxPdu

**容器属性**:

- **UUID**: `ECUC:799689c9-1f1f-4245-8228-18b7bf0c2dee`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPSoAdUdpRxPdu`
- **多重性**: [1..1]

**容器描述**:

This container describes a Rx PDU received via SoAd over UDP.

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. DoIPSoAdUdpRxPduId

- **UUID**: `ECUC:103f1b68-c87a-4b28-ad2b-a9a27b600be2`
- **参数名**: `DoIPSoAdUdpRxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **描述**: The DoIPSoAdUdpRxPduId is required by the API call DoIP_SoAdIfRxIndication to receive I-PDUs from the SoAd.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. DoIPSoAdUdpRxPduRef

- **UUID**: `ECUC:fd7f5cdf-7cf4-45f4-a627-2d343a8f7ed5`
- **引用名**: `DoIPSoAdUdpRxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the "global" Pdu structure to allow harmonization of handle IDs in the COM-Stack.

######### 2. DoIPSoAdUdpTxPdu

**容器属性**:

- **UUID**: `ECUC:b3d21ded-7966-4862-8d48-ddf2775239cc`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPSoAdUdpTxPdu`
- **多重性**: [1..1]

**容器描述**:

This container describes a Tx PDU sent via SoAd over UDP.

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. DoIPSoAdUdpTxPduId

- **UUID**: `ECUC:2f55a1ec-664b-4bd6-9da3-2f80f2a73746`
- **参数名**: `DoIPSoAdUdpTxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **描述**: The DoIPSoAdUdpTxPduId is required by the API call DoIP_SoAdIfTxConfirmation that is called by the SoAd to confirm that the IPdu has been transmitted successfully.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. DoIPSoAdUdpTxPduRef

- **UUID**: `ECUC:c31e5dee-28e5-4b32-8cec-51f54e77a3a3`
- **引用名**: `DoIPSoAdUdpTxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the "global" Pdu structure to allow harmonization of handle IDs in the COM-Stack.

####### 11. DoIPSoAdUdpRxPdu

**容器属性**:

- **UUID**: `ECUC:799689c9-1f1f-4245-8228-18b7bf0c2dee`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPSoAdUdpRxPdu`
- **多重性**: [1..1]

**容器描述**:

This container describes a Rx PDU received via SoAd over UDP.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. DoIPSoAdUdpRxPduId

- **UUID**: `ECUC:103f1b68-c87a-4b28-ad2b-a9a27b600be2`
- **参数名**: `DoIPSoAdUdpRxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **描述**: The DoIPSoAdUdpRxPduId is required by the API call DoIP_SoAdIfRxIndication to receive I-PDUs from the SoAd.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. DoIPSoAdUdpRxPduRef

- **UUID**: `ECUC:fd7f5cdf-7cf4-45f4-a627-2d343a8f7ed5`
- **引用名**: `DoIPSoAdUdpRxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the "global" Pdu structure to allow harmonization of handle IDs in the COM-Stack.

####### 12. DoIPSoAdUdpTxPdu

**容器属性**:

- **UUID**: `ECUC:b3d21ded-7966-4862-8d48-ddf2775239cc`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPSoAdUdpTxPdu`
- **多重性**: [1..1]

**容器描述**:

This container describes a Tx PDU sent via SoAd over UDP.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. DoIPSoAdUdpTxPduId

- **UUID**: `ECUC:2f55a1ec-664b-4bd6-9da3-2f80f2a73746`
- **参数名**: `DoIPSoAdUdpTxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **描述**: The DoIPSoAdUdpTxPduId is required by the API call DoIP_SoAdIfTxConfirmation that is called by the SoAd to confirm that the IPdu has been transmitted successfully.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. DoIPSoAdUdpTxPduRef

- **UUID**: `ECUC:c31e5dee-28e5-4b32-8cec-51f54e77a3a3`
- **引用名**: `DoIPSoAdUdpTxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the "global" Pdu structure to allow harmonization of handle IDs in the COM-Stack.

####### 13. DoIPUdpVehicleAnnouncementConnection

**容器属性**:

- **UUID**: `ECUC:ec10775c-9dc4-49d9-b17b-73c202f875ed`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPUdpVehicleAnnouncementConnection`
- **多重性**: [1..255]

**容器描述**:

This container describes the UDP multicast connections to the lower layer SoAd module.

######## 参数配置

此容器包含 **1** 个参数：

######### BOOLEAN 类型参数

########## 1. DoIPRequestAddressAssignment

- **UUID**: `ECUC:67eff5dd-1c6e-902a-5fca-f998126ea83e`
- **参数名**: `DoIPRequestAddressAssignment`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: The DoIP module shall request IP address assignment by calling SoAd_RequestIpAddrAssignment() for the TcpIpLocalAddr related to this DoIpConnection.

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. DoIPSoAdUdpVehicleAnnouncementTxPdu

**容器属性**:

- **UUID**: `ECUC:ca2c98f1-142e-4d74-b3e2-a2c7a5d2a5a7`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPSoAdUdpVehicleAnnouncementTxPdu`
- **多重性**: [1..1]

**容器描述**:

This container describes the vehicle announcement TxPdu sent via the SoAd.

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. DoIPSoAdUdpVehicleAnnouncementTxPduId

- **UUID**: `ECUC:d714703b-f033-4dcf-91de-1b6f531e9af7`
- **参数名**: `DoIPSoAdUdpVehicleAnnouncementTxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **描述**: The DoIPSoAdUdpVehicleAnnouncementTxPduId is required by the API call DoIP_SoAdIfTxConfirmation() that is called by the SoAd to confirm that the IPdu has been transmitted successfully.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. DoIPSoAdUdpVehicleAnnouncementTxPduRef

- **UUID**: `ECUC:90da376e-29ea-4262-aa92-05bf32a3971e`
- **引用名**: `DoIPSoAdUdpVehicleAnnouncementTxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the "global" PDU structure to allow harmonization of handle IDs in the COM-Stack.

####### 14. DoIPSoAdUdpVehicleAnnouncementTxPdu

**容器属性**:

- **UUID**: `ECUC:ca2c98f1-142e-4d74-b3e2-a2c7a5d2a5a7`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPSoAdUdpVehicleAnnouncementTxPdu`
- **多重性**: [1..1]

**容器描述**:

This container describes the vehicle announcement TxPdu sent via the SoAd.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. DoIPSoAdUdpVehicleAnnouncementTxPduId

- **UUID**: `ECUC:d714703b-f033-4dcf-91de-1b6f531e9af7`
- **参数名**: `DoIPSoAdUdpVehicleAnnouncementTxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **描述**: The DoIPSoAdUdpVehicleAnnouncementTxPduId is required by the API call DoIP_SoAdIfTxConfirmation() that is called by the SoAd to confirm that the IPdu has been transmitted successfully.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. DoIPSoAdUdpVehicleAnnouncementTxPduRef

- **UUID**: `ECUC:90da376e-29ea-4262-aa92-05bf32a3971e`
- **引用名**: `DoIPSoAdUdpVehicleAnnouncementTxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the "global" PDU structure to allow harmonization of handle IDs in the COM-Stack.

####### 15. DoIPFurtherActionByteCallback

**容器属性**:

- **UUID**: `ECUC:5aac8f6a-2a4d-4d01-af2e-645e910e158d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPFurtherActionByteCallback`
- **多重性**: [0..1]

**容器描述**:

This container describes the Callbackfunction to get the Further Action byte. This container shall always be present. If the DoIPFurtherActionByteDirect parameter is not present, the DoIP module will use an RPort of ServiceInterface CallbackGetFurtherActionByte with the name "CBGetFurtherActionByte_<shortname of enclosing DoIPInterface container>".

######## 参数配置

此容器包含 **1** 个参数：

######### FUNCTION-NAME 类型参数

########## 1. DoIPFurtherActionByteDirect

- **UUID**: `ECUC:b16ec364-7eb2-447e-ad3a-c55fe58378cb`
- **参数名**: `DoIPFurtherActionByteDirect`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **函数变体**:
- **描述**: Direct C Callback function to get the OEM specific Further Action Byte for the DoIP vehicle identification response/vehicle announcement. If the DoIPFurtherActionByteDirect parameter is present, the DoIP module will not use an RPort of ServiceInterface "CBGetFurtherActionByte" but will call the configured function.

####### 16. DoIPRoutingActivation

**容器属性**:

- **UUID**: `ECUC:8c07e2b0-4dd1-45fc-89ae-19a97da7e734`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPRoutingActivation`
- **多重性**: [0..255]

**容器描述**:

This container describes the routing activation possibilities by representing for each container a possible routing activation request message to the DoIP entity and the according references to the activated diagnostic messages.

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. DoIPRoutingActivationNumber

- **UUID**: `ECUC:335e310b-8d47-48bf-b643-5c12468a5f01`
- **参数名**: `DoIPRoutingActivationNumber`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Identifies the Routing activation Number which is received for a DoIP routing activation request message.

######### BOOLEAN 类型参数

########## 1. DoIPRoutingActivationSecurityRequired

- **UUID**: `ECUC:d645dea9-213c-4ac7-9407-a6cc7586ae8f`
- **参数名**: `DoIPRoutingActivationSecurityRequired`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Indicates if a routing activation requires a secure TCP connection

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. DoIPTargetAddressRef

- **UUID**: `ECUC:ebc9f44b-f588-4a77-a371-08bfa7d33272`
- **引用名**: `DoIPTargetAddressRef`
- **引用类型**: REFERENCE
- **多重性**: [1..65535]
- **目标**: `DoIPTargetAddress`
- **完整路径**: `/AUTOSAR/EcucDefs/DoIP/DoIPConfigSet/DoIPInterface/DoIPConnections/DoIPTargetAddress`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to all DoIPTargetAddress which are activated on this Routing activation.

######## 配置容器

本模块包含 **2** 个配置容器：

######### 1. DoIPRoutingActivationAuthenticationCallback

**容器属性**:

- **UUID**: `ECUC:726377c7-0039-4edc-b57c-dd98bc5e99b7`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPRoutingActivationAuthenticationCallback`
- **多重性**: [0..1]

**容器描述**:

Container describes the Callbackfunction to call on a Routing Activation Request for Authentication. If this container is configured but the DoIPRoutingActivationAuthenticationFunc parameter is not present, the DoIP module will use an RPort of ServiceInterface <RoutingActivation>_RoutingActivation with the name "CB<RoutingActivation>RoutingActivation". <RoutingActivation> is the ShortName of the DoIPRoutingActiviation container.

########## 参数配置

此容器包含 **3** 个参数：

########### INTEGER 类型参数

############ 1. DoIPRoutingActivationAuthenticationReqLength

- **UUID**: `ECUC:2abdcf96-9b8e-4936-afc0-ede76b21f3a7`
- **参数名**: `DoIPRoutingActivationAuthenticationReqLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Describes the amount of bytes used to handle to the authentication function on routing activation. If 0 is configured as length the parameter AuthenticationReqData will not be handled to the API.

############ 2. DoIPRoutingActivationAuthenticationResLength

- **UUID**: `ECUC:45e1fc22-6491-40ed-87b8-7917007771a8`
- **参数名**: `DoIPRoutingActivationAuthenticationResLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Describes the amount of bytes used to read by the authentication function on routing activation. If 0 is configured as length the parameter AuthenticationResData will not be fetched via the API.

########### FUNCTION-NAME 类型参数

############ 1. DoIPRoutingActivationAuthenticationFunc

- **UUID**: `ECUC:05ef7a06-64da-467c-be24-d40bac66acc3`
- **参数名**: `DoIPRoutingActivationAuthenticationFunc`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **函数变体**:
- **描述**: Direct C Callback function to trigger the authentication function for routing activation. If the DoIPRoutingActivationAuthenticationFunc parameter is present, the DoIP module will not use an RPort of ServiceInterface <RoutingActivation>_RoutingActivation but call the configured function.

######### 2. DoIPRoutingActivationConfirmationCallback

**容器属性**:

- **UUID**: `ECUC:7e1d1ce3-eff6-43ab-a071-e6b83dfa4855`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPRoutingActivationConfirmationCallback`
- **多重性**: [0..1]

**容器描述**:

Container describes the Callbackfunction to call on a Routing Activation Request for Confirmation. If this container is configured but the DoIPRoutingActivationConfirmationFunc parameter is not present the DoIP module will use an RPort of ServiceInterface <RoutingActivation>_RoutingActivation with the name "CB<RoutingActivation>RoutingActivation". <RoutingActivation> is the ShortName of the DoIPRoutingActiviation container.

########## 参数配置

此容器包含 **3** 个参数：

########### INTEGER 类型参数

############ 1. DoIPRoutingActivationConfirmationReqLength

- **UUID**: `ECUC:b5b1030f-ad9f-4bbf-b2a0-9674bf5f20a7`
- **参数名**: `DoIPRoutingActivationConfirmationReqLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Describes the amount of bytes used to handle to the confirmation function on routing activation. If 0 is configured as length the parameter ConfirmedReqData will not be handled to the API.

############ 2. DoIPRoutingActivationConfirmationResLength

- **UUID**: `ECUC:701e1997-d200-4ee4-8372-e5eb0dc94c56`
- **参数名**: `DoIPRoutingActivationConfirmationResLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Describes the amount of bytes used to read by the confirmation function on routing activation. If 0 is configured as length the parameter ConfirmedResData will not be fetched via the API.

########### FUNCTION-NAME 类型参数

############ 1. DoIPRoutingActivationConfirmationFunc

- **UUID**: `ECUC:4630dc00-f4e8-4bf0-b18c-1a98a4f2f7c9`
- **参数名**: `DoIPRoutingActivationConfirmationFunc`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **函数变体**:
- **描述**: Direct C Callback function to trigger the confirmation function for routing activation. If the DoIPRoutingActivationConfirmationFunc parameter is present the DoIP module will not use an RPort of ServiceInterface <RoutingActivation>_RoutingActivation but call the configured function.

####### 17. DoIPRoutingActivationAuthenticationCallback

**容器属性**:

- **UUID**: `ECUC:726377c7-0039-4edc-b57c-dd98bc5e99b7`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPRoutingActivationAuthenticationCallback`
- **多重性**: [0..1]

**容器描述**:

Container describes the Callbackfunction to call on a Routing Activation Request for Authentication. If this container is configured but the DoIPRoutingActivationAuthenticationFunc parameter is not present, the DoIP module will use an RPort of ServiceInterface <RoutingActivation>_RoutingActivation with the name "CB<RoutingActivation>RoutingActivation". <RoutingActivation> is the ShortName of the DoIPRoutingActiviation container.

######## 参数配置

此容器包含 **3** 个参数：

######### INTEGER 类型参数

########## 1. DoIPRoutingActivationAuthenticationReqLength

- **UUID**: `ECUC:2abdcf96-9b8e-4936-afc0-ede76b21f3a7`
- **参数名**: `DoIPRoutingActivationAuthenticationReqLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Describes the amount of bytes used to handle to the authentication function on routing activation. If 0 is configured as length the parameter AuthenticationReqData will not be handled to the API.

########## 2. DoIPRoutingActivationAuthenticationResLength

- **UUID**: `ECUC:45e1fc22-6491-40ed-87b8-7917007771a8`
- **参数名**: `DoIPRoutingActivationAuthenticationResLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Describes the amount of bytes used to read by the authentication function on routing activation. If 0 is configured as length the parameter AuthenticationResData will not be fetched via the API.

######### FUNCTION-NAME 类型参数

########## 1. DoIPRoutingActivationAuthenticationFunc

- **UUID**: `ECUC:05ef7a06-64da-467c-be24-d40bac66acc3`
- **参数名**: `DoIPRoutingActivationAuthenticationFunc`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **函数变体**:
- **描述**: Direct C Callback function to trigger the authentication function for routing activation. If the DoIPRoutingActivationAuthenticationFunc parameter is present, the DoIP module will not use an RPort of ServiceInterface <RoutingActivation>_RoutingActivation but call the configured function.

####### 18. DoIPRoutingActivationConfirmationCallback

**容器属性**:

- **UUID**: `ECUC:7e1d1ce3-eff6-43ab-a071-e6b83dfa4855`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPRoutingActivationConfirmationCallback`
- **多重性**: [0..1]

**容器描述**:

Container describes the Callbackfunction to call on a Routing Activation Request for Confirmation. If this container is configured but the DoIPRoutingActivationConfirmationFunc parameter is not present the DoIP module will use an RPort of ServiceInterface <RoutingActivation>_RoutingActivation with the name "CB<RoutingActivation>RoutingActivation". <RoutingActivation> is the ShortName of the DoIPRoutingActiviation container.

######## 参数配置

此容器包含 **3** 个参数：

######### INTEGER 类型参数

########## 1. DoIPRoutingActivationConfirmationReqLength

- **UUID**: `ECUC:b5b1030f-ad9f-4bbf-b2a0-9674bf5f20a7`
- **参数名**: `DoIPRoutingActivationConfirmationReqLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Describes the amount of bytes used to handle to the confirmation function on routing activation. If 0 is configured as length the parameter ConfirmedReqData will not be handled to the API.

########## 2. DoIPRoutingActivationConfirmationResLength

- **UUID**: `ECUC:701e1997-d200-4ee4-8372-e5eb0dc94c56`
- **参数名**: `DoIPRoutingActivationConfirmationResLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Describes the amount of bytes used to read by the confirmation function on routing activation. If 0 is configured as length the parameter ConfirmedResData will not be fetched via the API.

######### FUNCTION-NAME 类型参数

########## 1. DoIPRoutingActivationConfirmationFunc

- **UUID**: `ECUC:4630dc00-f4e8-4bf0-b18c-1a98a4f2f7c9`
- **参数名**: `DoIPRoutingActivationConfirmationFunc`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **函数变体**:
- **描述**: Direct C Callback function to trigger the confirmation function for routing activation. If the DoIPRoutingActivationConfirmationFunc parameter is present the DoIP module will not use an RPort of ServiceInterface <RoutingActivation>_RoutingActivation but call the configured function.

####### 19. DoIPTester

**容器属性**:

- **UUID**: `ECUC:5ec2063c-2a23-4da2-be67-e7cd0a80ee93`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPTester`
- **多重性**: [0..255]

**容器描述**:

This container describes the properties of the possible connectable Tester for the DoIP entity.

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. DoIPNumByteDiagAckNack

- **UUID**: `ECUC:2cdb3b03-189a-4c0d-847c-ec5cbe717265`
- **参数名**: `DoIPNumByteDiagAckNack`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Specifies the number of original Diagnostic request bytes the DoIP entity responses on a NACK of a diagnostic response message to the Tester.

########## 2. DoIPTesterSA

- **UUID**: `ECUC:44ccb383-1ad0-47a4-a3c4-5056f05a922d`
- **参数名**: `DoIPTesterSA`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Source Address of the Tester sent via routing activation or diagnostic message.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. DoIPRoutingActivationRef

- **UUID**: `ECUC:cc241bfa-5d3c-4e9b-b190-f764add15a77`
- **引用名**: `DoIPRoutingActivationRef`
- **引用类型**: REFERENCE
- **多重性**: [1..255]
- **目标**: `DoIPRoutingActivation`
- **完整路径**: `/AUTOSAR/EcucDefs/DoIP/DoIPConfigSet/DoIPInterface/DoIPRoutingActivation`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to a DoIPRoutingActivation describing the possible routing activations of the DoIPTester

##### 2. DoIPInterface

**容器属性**:

- **UUID**: `ECUC:789e2362-020e-4531-b21a-6f65ae92c662`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPInterface`
- **多重性**: [1..255]

**容器描述**:

This container defines a logical IP interface and collects properties to configure this interface.

###### 参数配置

此容器包含 **12** 个参数：

####### INTEGER 类型参数

######## 1. DoIPInterfaceId

- **UUID**: `ECUC:1b2e63b0-6029-4653-b54a-f59977514a0c`
- **参数名**: `DoIPInterfaceId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **描述**: This parameter is an identifier of the DoIPInterface. The value of this parameter will be assigned to the symbolic name derived from the container short name.

######## 2. DoIPMaxTesterConnections

- **UUID**: `ECUC:4ee8c2a0-3924-41c7-a5d1-3bcf431efb0e`
- **参数名**: `DoIPMaxTesterConnections`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Maximum amount of tester connections that shall be maintained at one time before alive check is performed.

######## 3. DoIPVehicleAnnouncementCount

- **UUID**: `ECUC:18720174-b4fb-4222-8e3b-9de228019753`
- **参数名**: `DoIPVehicleAnnouncementCount`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [1..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Number of vehicle announcement messages on IP address assignment. Represents parameter A_DoIP_Announce_Num of ISO 13400-2:2012.

####### BOOLEAN 类型参数

######## 1. DoIPInterfaceActLineCtrl

- **UUID**: `ECUC:6e2237e3-5bac-41e9-bf4a-ae8559979fa6`
- **参数名**: `DoIPInterfaceActLineCtrl`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: This attribute defines whether the network interface

######## 2. DoIPUseMacAddressForIdentification

- **UUID**: `ECUC:364c701f-a202-4a4b-b7bc-ee6cf58cddb3`
- **参数名**: `DoIPUseMacAddressForIdentification`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Provided the information if a configured EID at vehicle identification response/vehicle announment is used or the MAC address.

######## 3. DoIPUseVehicleIdentificationSyncStatus

- **UUID**: `ECUC:77dc8eda-649f-4728-9915-a08f25f81905`
- **参数名**: `DoIPUseVehicleIdentificationSyncStatus`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Defines if the optional VIN/GID synchronization status is used additionally in the vehicle identification/announcement.

####### FLOAT 类型参数

######## 1. DoIPAliveCheckResponseTimeout

- **UUID**: `ECUC:a680c7fa-c06d-4139-b2a8-e60b1ee21fa6`
- **参数名**: `DoIPAliveCheckResponseTimeout`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0..INF]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Timeout  in [s] for waiting for a response to an Alive Check request before the connection is considered to be disconnected. Represents parameter T_TCP_AliveCheck of ISO 13400-2:2012.

######## 2. DoIPGeneralInactivityTime

- **UUID**: `ECUC:3c672e92-2dff-4c0d-98eb-0c9379bcafec`
- **参数名**: `DoIPGeneralInactivityTime`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0..INF]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Timeout in [s] for maximum inactivity of a TCP socket connection before the DoIP module will close the according socket connection. Represents parameter T_TCP_General_Inactivity of ISO 13400-2:2012

######## 3. DoIPInitialInactivityTime

- **UUID**: `ECUC:f455792f-afbc-4de1-ab70-30d56a927828`
- **参数名**: `DoIPInitialInactivityTime`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0..INF]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Timeout in [s] used for initial inactivity of a connected TCP socket connection directly after socket connection. Represents parameter T_TCP_Initial_Inactivity of ISO 13400-2:2012

######## 4. DoIPInitialVehicleAnnouncementTime

- **UUID**: `ECUC:f2ce0a2d-fc67-453a-8b22-6f0f033507b2`
- **参数名**: `DoIPInitialVehicleAnnouncementTime`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0..INF]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Time to wait in [s] for sending first vehicle anouncement message after IP address assignment. Represents parameter A_DoIP_Announce_Wait of ISO 13400-2:2012

######## 5. DoIPVehicleAnnouncementInterval

- **UUID**: `ECUC:53d5e0b6-56d1-459d-a3ec-69ce6e1c46c1`
- **参数名**: `DoIPVehicleAnnouncementInterval`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **取值范围**: [0..INF]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Time to wait in [s] for sending subsequent vehicle anouncement messages. Represents parameter A_DoIP_Announce_Interval of ISO 13400-2:2012

####### ENUMERATION 类型参数

######## 1. DoIPInterfaceAnnouncementStart

- **UUID**: `ECUC:c7a33c91-d135-444a-8806-80515d8ae9fe`
- **参数名**: `DoIPInterfaceAnnouncementStart`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `DOIP_AUTOMATIC_ANNOUNCE`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `DOIP_AUTOMATIC_ANNOUNCE` (来源: AUTOSAR_ECUC)
  - `DOIP_ONTRIGGER_ANNOUNCE` (来源: AUTOSAR_ECUC)
- **描述**: This attribute defines, when vehicle announcement is started on a DoIPInterface

###### 配置容器

本模块包含 **18** 个配置容器：

####### 1. DoIPChannel

**容器属性**:

- **UUID**: `ECUC:ce8927a0-58c7-4099-a996-3ee43001e9e8`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPChannel`
- **多重性**: [1..65536]

**容器描述**:

Configuration of one DoIPChannel.

######## 引用关系

此容器包含 **2** 个引用：

######### REFERENCE 类型引用

########## 1. DoIPChannelSARef

- **UUID**: `ECUC:893cf71a-c06b-4044-812c-8df50e45d13e`
- **引用名**: `DoIPChannelSARef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `DoIPTester`
- **完整路径**: `/AUTOSAR/EcucDefs/DoIP/DoIPConfigSet/DoIPInterface/DoIPTester`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the DoIPTester.

########## 2. DoIPChannelTARef

- **UUID**: `ECUC:cbe1685e-4306-4efc-8345-5a1446b28405`
- **引用名**: `DoIPChannelTARef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `DoIPTargetAddress`
- **完整路径**: `/AUTOSAR/EcucDefs/DoIP/DoIPConfigSet/DoIPInterface/DoIPConnections/DoIPTargetAddress`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the target address.

######## 配置容器

本模块包含 **2** 个配置容器：

######### 1. DoIPPduRRxPdu

**容器属性**:

- **UUID**: `ECUC:63341ec1-b4ca-4bbc-82b5-a883d528b7c1`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPPduRRxPdu`
- **多重性**: [0..1]

**容器描述**:

This container contains the Rx Pdus to connect with the Rx Pdus of the PduR.

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. DoIPPduRRxPduId

- **UUID**: `ECUC:affbfe09-cf4f-43ed-91f0-957c1e71f17f`
- **参数名**: `DoIPPduRRxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **描述**: The DoIPPduRRxPduId is required by the API call DoIP_TpCancelReceive.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. DoIPPduRRxPduRef

- **UUID**: `ECUC:0fb53490-8f12-418b-a048-feaf0c60d6b0`
- **引用名**: `DoIPPduRRxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the "global" Pdu structure to allow harmonization of handle IDs in the COM-Stack.

######### 2. DoIPPduRTxPdu

**容器属性**:

- **UUID**: `ECUC:ecf769bc-a264-4426-a107-185d357d42b4`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPPduRTxPdu`
- **多重性**: [0..1]

**容器描述**:

This container contains the Tx Pdus to connect with the Tx Pdus of the PduR.  If the parameter is not configured the channel is for functional addressing.

########## 参数配置

此容器包含 **2** 个参数：

########### INTEGER 类型参数

############ 1. DoIPPduRTxPduId

- **UUID**: `ECUC:4ec22559-5780-41ca-af56-0b32ecdd6dae`
- **参数名**: `DoIPPduRTxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **描述**: The DoIPPduRTxPduId is required by DoIP_TpTransmit or DoIP_IfTransmit and DoIP_TpCancelTransmit.

########### ENUMERATION 类型参数

############ 1. DoIPPduType

- **UUID**: `ECUC:17c8aace-cda8-471d-8cb2-e474dda9c61a`
- **参数名**: `DoIPPduType`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `DOIP_TPPDU`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `DOIP_IFPDU` (来源: AUTOSAR_ECUC)
  - `DOIP_TPPDU` (来源: AUTOSAR_ECUC)
- **描述**: API Type to use for communication with PduR. DOIP_IFPDU for UUDT messages, DOIP_TPPDU for all other diagnostic messages.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. DoIPPduRTxPduRef

- **UUID**: `ECUC:f703fb82-d2e7-4545-a97c-3275ff0bfc5d`
- **引用名**: `DoIPPduRTxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the "global" Pdu structure to allow harmonization of handle IDs in the COM-Stack.

####### 2. DoIPPduRRxPdu

**容器属性**:

- **UUID**: `ECUC:63341ec1-b4ca-4bbc-82b5-a883d528b7c1`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPPduRRxPdu`
- **多重性**: [0..1]

**容器描述**:

This container contains the Rx Pdus to connect with the Rx Pdus of the PduR.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. DoIPPduRRxPduId

- **UUID**: `ECUC:affbfe09-cf4f-43ed-91f0-957c1e71f17f`
- **参数名**: `DoIPPduRRxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **描述**: The DoIPPduRRxPduId is required by the API call DoIP_TpCancelReceive.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. DoIPPduRRxPduRef

- **UUID**: `ECUC:0fb53490-8f12-418b-a048-feaf0c60d6b0`
- **引用名**: `DoIPPduRRxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the "global" Pdu structure to allow harmonization of handle IDs in the COM-Stack.

####### 3. DoIPPduRTxPdu

**容器属性**:

- **UUID**: `ECUC:ecf769bc-a264-4426-a107-185d357d42b4`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPPduRTxPdu`
- **多重性**: [0..1]

**容器描述**:

This container contains the Tx Pdus to connect with the Tx Pdus of the PduR.  If the parameter is not configured the channel is for functional addressing.

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. DoIPPduRTxPduId

- **UUID**: `ECUC:4ec22559-5780-41ca-af56-0b32ecdd6dae`
- **参数名**: `DoIPPduRTxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **描述**: The DoIPPduRTxPduId is required by DoIP_TpTransmit or DoIP_IfTransmit and DoIP_TpCancelTransmit.

######### ENUMERATION 类型参数

########## 1. DoIPPduType

- **UUID**: `ECUC:17c8aace-cda8-471d-8cb2-e474dda9c61a`
- **参数名**: `DoIPPduType`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `DOIP_TPPDU`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `DOIP_IFPDU` (来源: AUTOSAR_ECUC)
  - `DOIP_TPPDU` (来源: AUTOSAR_ECUC)
- **描述**: API Type to use for communication with PduR. DOIP_IFPDU for UUDT messages, DOIP_TPPDU for all other diagnostic messages.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. DoIPPduRTxPduRef

- **UUID**: `ECUC:f703fb82-d2e7-4545-a97c-3275ff0bfc5d`
- **引用名**: `DoIPPduRTxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the "global" Pdu structure to allow harmonization of handle IDs in the COM-Stack.

####### 4. DoIPConnections

**容器属性**:

- **UUID**: `ECUC:06a174a5-5ad6-4b7a-8ce8-c64883f2e5c5`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPConnections`
- **多重性**: [1..1]

**容器描述**:

Container contains all lower layer connection specific information, i.e. the single Pdu References and Handle IDs to the SoAd.

######## 配置容器

本模块包含 **9** 个配置容器：

######### 1. DoIPTargetAddress

**容器属性**:

- **UUID**: `ECUC:11b8faaf-bc59-49fe-97b5-29df73fa6ee7`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPTargetAddress`
- **多重性**: [1..65535]

**容器描述**:

This container describes a possible TargetAddress that is supported by DoIP.

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. DoIPTargetAddressValue

- **UUID**: `ECUC:c46011a4-ab1a-42cf-a2f8-b71632fcfd59`
- **参数名**: `DoIPTargetAddressValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Valid Target Address of a DoIP target address.

######### 2. DoIPTcpConnection

**容器属性**:

- **UUID**: `ECUC:e3ccdc1d-8a6b-40a0-abbf-59a1db67e267`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPTcpConnection`
- **多重性**: [1..255]

**容器描述**:

This container describes a TCP connection to the lower layer SoAd module.

########## 参数配置

此容器包含 **2** 个参数：

########### BOOLEAN 类型参数

############ 1. DoIPRequestAddressAssignment

- **UUID**: `ECUC:5fac5a9e-0915-86f1-5a0e-df77eade14b8`
- **参数名**: `DoIPRequestAddressAssignment`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: The DoIP module shall request IP address assignment by calling SoAd_RequestIpAddrAssignment() for the TcpIpLocalAddr related to this DoIpConnection.

############ 2. DoIPTcpConnectionSecurityRequired

- **UUID**: `ECUC:e723d1bf-784e-4527-892c-4fcbf9e11e05`
- **参数名**: `DoIPTcpConnectionSecurityRequired`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Indicates if the associated TCP socket uses a secure connection (e.g. TLS)

########## 配置容器

本模块包含 **2** 个配置容器：

########### 1. DoIPSoAdTcpRxPdu

**容器属性**:

- **UUID**: `ECUC:f8ff31c4-d60d-4316-b021-67cb31934ee7`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPSoAdTcpRxPdu`
- **多重性**: [1..1]

**容器描述**:

This container describes a Rx PDU received via SoAd over TCP

############ 参数配置

此容器包含 **1** 个参数：

############# INTEGER 类型参数

############## 1. DoIPSoAdTcpRxPduId

- **UUID**: `ECUC:87bc6f78-b949-44dd-a958-16f6c2003d78`
- **参数名**: `DoIPSoAdTcpRxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **描述**: The DoIPSoAdTcpRxPduId is required by the API call DoIP_SoAdTpRxIndication to receive I-PDUs from the SoAd.

############ 引用关系

此容器包含 **1** 个引用：

############# REFERENCE 类型引用

############## 1. DoIPSoAdTcpRxPduRef

- **UUID**: `ECUC:7fa9533f-a369-48ce-8666-1982b51d007d`
- **引用名**: `DoIPSoAdTcpRxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the "global" Pdu structure to allow harmonization of handle IDs in the COM-Stack.

########### 2. DoIPSoAdTcpTxPdu

**容器属性**:

- **UUID**: `ECUC:b94850e4-7ec7-4c7a-95d7-e883570c386f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPSoAdTcpTxPdu`
- **多重性**: [1..1]

**容器描述**:

This container describes a Tx PDU sent via SoAd over TCP

############ 参数配置

此容器包含 **1** 个参数：

############# INTEGER 类型参数

############## 1. DoIPSoAdTcpTxPduId

- **UUID**: `ECUC:18866fc8-b1b6-4749-866c-8d0dff665d6e`
- **参数名**: `DoIPSoAdTcpTxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **描述**: The DoIPSoAdTcpTxPduId is required by the API call DoIP_SoAdTpTxConfirmation that is called by the SoAd to confirm that the IPdu has been transmitted successfully.

############ 引用关系

此容器包含 **1** 个引用：

############# REFERENCE 类型引用

############## 1. DoIPSoAdTcpTxPduRef

- **UUID**: `ECUC:71678586-2f21-4e4f-aefc-997db5b282a4`
- **引用名**: `DoIPSoAdTcpTxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the "global" Pdu structure to allow harmonization of handle IDs in the COM-Stack.

######### 3. DoIPSoAdTcpRxPdu

**容器属性**:

- **UUID**: `ECUC:f8ff31c4-d60d-4316-b021-67cb31934ee7`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPSoAdTcpRxPdu`
- **多重性**: [1..1]

**容器描述**:

This container describes a Rx PDU received via SoAd over TCP

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. DoIPSoAdTcpRxPduId

- **UUID**: `ECUC:87bc6f78-b949-44dd-a958-16f6c2003d78`
- **参数名**: `DoIPSoAdTcpRxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **描述**: The DoIPSoAdTcpRxPduId is required by the API call DoIP_SoAdTpRxIndication to receive I-PDUs from the SoAd.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. DoIPSoAdTcpRxPduRef

- **UUID**: `ECUC:7fa9533f-a369-48ce-8666-1982b51d007d`
- **引用名**: `DoIPSoAdTcpRxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the "global" Pdu structure to allow harmonization of handle IDs in the COM-Stack.

######### 4. DoIPSoAdTcpTxPdu

**容器属性**:

- **UUID**: `ECUC:b94850e4-7ec7-4c7a-95d7-e883570c386f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPSoAdTcpTxPdu`
- **多重性**: [1..1]

**容器描述**:

This container describes a Tx PDU sent via SoAd over TCP

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. DoIPSoAdTcpTxPduId

- **UUID**: `ECUC:18866fc8-b1b6-4749-866c-8d0dff665d6e`
- **参数名**: `DoIPSoAdTcpTxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **描述**: The DoIPSoAdTcpTxPduId is required by the API call DoIP_SoAdTpTxConfirmation that is called by the SoAd to confirm that the IPdu has been transmitted successfully.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. DoIPSoAdTcpTxPduRef

- **UUID**: `ECUC:71678586-2f21-4e4f-aefc-997db5b282a4`
- **引用名**: `DoIPSoAdTcpTxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the "global" Pdu structure to allow harmonization of handle IDs in the COM-Stack.

######### 5. DoIPUdpConnection

**容器属性**:

- **UUID**: `ECUC:113b6883-6d62-4e20-9cb6-680252dad2b0`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPUdpConnection`
- **多重性**: [1..255]

**容器描述**:

This Container describes a Udp connection to the lower layer SoAd module.

########## 参数配置

此容器包含 **1** 个参数：

########### BOOLEAN 类型参数

############ 1. DoIPRequestAddressAssignment

- **UUID**: `ECUC:8d1ae703-ec0c-9471-4b05-edd862510501`
- **参数名**: `DoIPRequestAddressAssignment`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: The DoIP module shall request IP address assignment by calling SoAd_RequestIpAddrAssignment() for the TcpIpLocalAddr related to this DoIpConnection.

########## 配置容器

本模块包含 **2** 个配置容器：

########### 1. DoIPSoAdUdpRxPdu

**容器属性**:

- **UUID**: `ECUC:799689c9-1f1f-4245-8228-18b7bf0c2dee`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPSoAdUdpRxPdu`
- **多重性**: [1..1]

**容器描述**:

This container describes a Rx PDU received via SoAd over UDP.

############ 参数配置

此容器包含 **1** 个参数：

############# INTEGER 类型参数

############## 1. DoIPSoAdUdpRxPduId

- **UUID**: `ECUC:103f1b68-c87a-4b28-ad2b-a9a27b600be2`
- **参数名**: `DoIPSoAdUdpRxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **描述**: The DoIPSoAdUdpRxPduId is required by the API call DoIP_SoAdIfRxIndication to receive I-PDUs from the SoAd.

############ 引用关系

此容器包含 **1** 个引用：

############# REFERENCE 类型引用

############## 1. DoIPSoAdUdpRxPduRef

- **UUID**: `ECUC:fd7f5cdf-7cf4-45f4-a627-2d343a8f7ed5`
- **引用名**: `DoIPSoAdUdpRxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the "global" Pdu structure to allow harmonization of handle IDs in the COM-Stack.

########### 2. DoIPSoAdUdpTxPdu

**容器属性**:

- **UUID**: `ECUC:b3d21ded-7966-4862-8d48-ddf2775239cc`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPSoAdUdpTxPdu`
- **多重性**: [1..1]

**容器描述**:

This container describes a Tx PDU sent via SoAd over UDP.

############ 参数配置

此容器包含 **1** 个参数：

############# INTEGER 类型参数

############## 1. DoIPSoAdUdpTxPduId

- **UUID**: `ECUC:2f55a1ec-664b-4bd6-9da3-2f80f2a73746`
- **参数名**: `DoIPSoAdUdpTxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **描述**: The DoIPSoAdUdpTxPduId is required by the API call DoIP_SoAdIfTxConfirmation that is called by the SoAd to confirm that the IPdu has been transmitted successfully.

############ 引用关系

此容器包含 **1** 个引用：

############# REFERENCE 类型引用

############## 1. DoIPSoAdUdpTxPduRef

- **UUID**: `ECUC:c31e5dee-28e5-4b32-8cec-51f54e77a3a3`
- **引用名**: `DoIPSoAdUdpTxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the "global" Pdu structure to allow harmonization of handle IDs in the COM-Stack.

######### 6. DoIPSoAdUdpRxPdu

**容器属性**:

- **UUID**: `ECUC:799689c9-1f1f-4245-8228-18b7bf0c2dee`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPSoAdUdpRxPdu`
- **多重性**: [1..1]

**容器描述**:

This container describes a Rx PDU received via SoAd over UDP.

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. DoIPSoAdUdpRxPduId

- **UUID**: `ECUC:103f1b68-c87a-4b28-ad2b-a9a27b600be2`
- **参数名**: `DoIPSoAdUdpRxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **描述**: The DoIPSoAdUdpRxPduId is required by the API call DoIP_SoAdIfRxIndication to receive I-PDUs from the SoAd.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. DoIPSoAdUdpRxPduRef

- **UUID**: `ECUC:fd7f5cdf-7cf4-45f4-a627-2d343a8f7ed5`
- **引用名**: `DoIPSoAdUdpRxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the "global" Pdu structure to allow harmonization of handle IDs in the COM-Stack.

######### 7. DoIPSoAdUdpTxPdu

**容器属性**:

- **UUID**: `ECUC:b3d21ded-7966-4862-8d48-ddf2775239cc`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPSoAdUdpTxPdu`
- **多重性**: [1..1]

**容器描述**:

This container describes a Tx PDU sent via SoAd over UDP.

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. DoIPSoAdUdpTxPduId

- **UUID**: `ECUC:2f55a1ec-664b-4bd6-9da3-2f80f2a73746`
- **参数名**: `DoIPSoAdUdpTxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **描述**: The DoIPSoAdUdpTxPduId is required by the API call DoIP_SoAdIfTxConfirmation that is called by the SoAd to confirm that the IPdu has been transmitted successfully.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. DoIPSoAdUdpTxPduRef

- **UUID**: `ECUC:c31e5dee-28e5-4b32-8cec-51f54e77a3a3`
- **引用名**: `DoIPSoAdUdpTxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the "global" Pdu structure to allow harmonization of handle IDs in the COM-Stack.

######### 8. DoIPUdpVehicleAnnouncementConnection

**容器属性**:

- **UUID**: `ECUC:ec10775c-9dc4-49d9-b17b-73c202f875ed`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPUdpVehicleAnnouncementConnection`
- **多重性**: [1..255]

**容器描述**:

This container describes the UDP multicast connections to the lower layer SoAd module.

########## 参数配置

此容器包含 **1** 个参数：

########### BOOLEAN 类型参数

############ 1. DoIPRequestAddressAssignment

- **UUID**: `ECUC:67eff5dd-1c6e-902a-5fca-f998126ea83e`
- **参数名**: `DoIPRequestAddressAssignment`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: The DoIP module shall request IP address assignment by calling SoAd_RequestIpAddrAssignment() for the TcpIpLocalAddr related to this DoIpConnection.

########## 配置容器

本模块包含 **1** 个配置容器：

########### 1. DoIPSoAdUdpVehicleAnnouncementTxPdu

**容器属性**:

- **UUID**: `ECUC:ca2c98f1-142e-4d74-b3e2-a2c7a5d2a5a7`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPSoAdUdpVehicleAnnouncementTxPdu`
- **多重性**: [1..1]

**容器描述**:

This container describes the vehicle announcement TxPdu sent via the SoAd.

############ 参数配置

此容器包含 **1** 个参数：

############# INTEGER 类型参数

############## 1. DoIPSoAdUdpVehicleAnnouncementTxPduId

- **UUID**: `ECUC:d714703b-f033-4dcf-91de-1b6f531e9af7`
- **参数名**: `DoIPSoAdUdpVehicleAnnouncementTxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **描述**: The DoIPSoAdUdpVehicleAnnouncementTxPduId is required by the API call DoIP_SoAdIfTxConfirmation() that is called by the SoAd to confirm that the IPdu has been transmitted successfully.

############ 引用关系

此容器包含 **1** 个引用：

############# REFERENCE 类型引用

############## 1. DoIPSoAdUdpVehicleAnnouncementTxPduRef

- **UUID**: `ECUC:90da376e-29ea-4262-aa92-05bf32a3971e`
- **引用名**: `DoIPSoAdUdpVehicleAnnouncementTxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the "global" PDU structure to allow harmonization of handle IDs in the COM-Stack.

######### 9. DoIPSoAdUdpVehicleAnnouncementTxPdu

**容器属性**:

- **UUID**: `ECUC:ca2c98f1-142e-4d74-b3e2-a2c7a5d2a5a7`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPSoAdUdpVehicleAnnouncementTxPdu`
- **多重性**: [1..1]

**容器描述**:

This container describes the vehicle announcement TxPdu sent via the SoAd.

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. DoIPSoAdUdpVehicleAnnouncementTxPduId

- **UUID**: `ECUC:d714703b-f033-4dcf-91de-1b6f531e9af7`
- **参数名**: `DoIPSoAdUdpVehicleAnnouncementTxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **描述**: The DoIPSoAdUdpVehicleAnnouncementTxPduId is required by the API call DoIP_SoAdIfTxConfirmation() that is called by the SoAd to confirm that the IPdu has been transmitted successfully.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. DoIPSoAdUdpVehicleAnnouncementTxPduRef

- **UUID**: `ECUC:90da376e-29ea-4262-aa92-05bf32a3971e`
- **引用名**: `DoIPSoAdUdpVehicleAnnouncementTxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the "global" PDU structure to allow harmonization of handle IDs in the COM-Stack.

####### 5. DoIPTargetAddress

**容器属性**:

- **UUID**: `ECUC:11b8faaf-bc59-49fe-97b5-29df73fa6ee7`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPTargetAddress`
- **多重性**: [1..65535]

**容器描述**:

This container describes a possible TargetAddress that is supported by DoIP.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. DoIPTargetAddressValue

- **UUID**: `ECUC:c46011a4-ab1a-42cf-a2f8-b71632fcfd59`
- **参数名**: `DoIPTargetAddressValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Valid Target Address of a DoIP target address.

####### 6. DoIPTcpConnection

**容器属性**:

- **UUID**: `ECUC:e3ccdc1d-8a6b-40a0-abbf-59a1db67e267`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPTcpConnection`
- **多重性**: [1..255]

**容器描述**:

This container describes a TCP connection to the lower layer SoAd module.

######## 参数配置

此容器包含 **2** 个参数：

######### BOOLEAN 类型参数

########## 1. DoIPRequestAddressAssignment

- **UUID**: `ECUC:5fac5a9e-0915-86f1-5a0e-df77eade14b8`
- **参数名**: `DoIPRequestAddressAssignment`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: The DoIP module shall request IP address assignment by calling SoAd_RequestIpAddrAssignment() for the TcpIpLocalAddr related to this DoIpConnection.

########## 2. DoIPTcpConnectionSecurityRequired

- **UUID**: `ECUC:e723d1bf-784e-4527-892c-4fcbf9e11e05`
- **参数名**: `DoIPTcpConnectionSecurityRequired`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Indicates if the associated TCP socket uses a secure connection (e.g. TLS)

######## 配置容器

本模块包含 **2** 个配置容器：

######### 1. DoIPSoAdTcpRxPdu

**容器属性**:

- **UUID**: `ECUC:f8ff31c4-d60d-4316-b021-67cb31934ee7`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPSoAdTcpRxPdu`
- **多重性**: [1..1]

**容器描述**:

This container describes a Rx PDU received via SoAd over TCP

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. DoIPSoAdTcpRxPduId

- **UUID**: `ECUC:87bc6f78-b949-44dd-a958-16f6c2003d78`
- **参数名**: `DoIPSoAdTcpRxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **描述**: The DoIPSoAdTcpRxPduId is required by the API call DoIP_SoAdTpRxIndication to receive I-PDUs from the SoAd.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. DoIPSoAdTcpRxPduRef

- **UUID**: `ECUC:7fa9533f-a369-48ce-8666-1982b51d007d`
- **引用名**: `DoIPSoAdTcpRxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the "global" Pdu structure to allow harmonization of handle IDs in the COM-Stack.

######### 2. DoIPSoAdTcpTxPdu

**容器属性**:

- **UUID**: `ECUC:b94850e4-7ec7-4c7a-95d7-e883570c386f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPSoAdTcpTxPdu`
- **多重性**: [1..1]

**容器描述**:

This container describes a Tx PDU sent via SoAd over TCP

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. DoIPSoAdTcpTxPduId

- **UUID**: `ECUC:18866fc8-b1b6-4749-866c-8d0dff665d6e`
- **参数名**: `DoIPSoAdTcpTxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **描述**: The DoIPSoAdTcpTxPduId is required by the API call DoIP_SoAdTpTxConfirmation that is called by the SoAd to confirm that the IPdu has been transmitted successfully.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. DoIPSoAdTcpTxPduRef

- **UUID**: `ECUC:71678586-2f21-4e4f-aefc-997db5b282a4`
- **引用名**: `DoIPSoAdTcpTxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the "global" Pdu structure to allow harmonization of handle IDs in the COM-Stack.

####### 7. DoIPSoAdTcpRxPdu

**容器属性**:

- **UUID**: `ECUC:f8ff31c4-d60d-4316-b021-67cb31934ee7`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPSoAdTcpRxPdu`
- **多重性**: [1..1]

**容器描述**:

This container describes a Rx PDU received via SoAd over TCP

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. DoIPSoAdTcpRxPduId

- **UUID**: `ECUC:87bc6f78-b949-44dd-a958-16f6c2003d78`
- **参数名**: `DoIPSoAdTcpRxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **描述**: The DoIPSoAdTcpRxPduId is required by the API call DoIP_SoAdTpRxIndication to receive I-PDUs from the SoAd.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. DoIPSoAdTcpRxPduRef

- **UUID**: `ECUC:7fa9533f-a369-48ce-8666-1982b51d007d`
- **引用名**: `DoIPSoAdTcpRxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the "global" Pdu structure to allow harmonization of handle IDs in the COM-Stack.

####### 8. DoIPSoAdTcpTxPdu

**容器属性**:

- **UUID**: `ECUC:b94850e4-7ec7-4c7a-95d7-e883570c386f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPSoAdTcpTxPdu`
- **多重性**: [1..1]

**容器描述**:

This container describes a Tx PDU sent via SoAd over TCP

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. DoIPSoAdTcpTxPduId

- **UUID**: `ECUC:18866fc8-b1b6-4749-866c-8d0dff665d6e`
- **参数名**: `DoIPSoAdTcpTxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **描述**: The DoIPSoAdTcpTxPduId is required by the API call DoIP_SoAdTpTxConfirmation that is called by the SoAd to confirm that the IPdu has been transmitted successfully.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. DoIPSoAdTcpTxPduRef

- **UUID**: `ECUC:71678586-2f21-4e4f-aefc-997db5b282a4`
- **引用名**: `DoIPSoAdTcpTxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the "global" Pdu structure to allow harmonization of handle IDs in the COM-Stack.

####### 9. DoIPUdpConnection

**容器属性**:

- **UUID**: `ECUC:113b6883-6d62-4e20-9cb6-680252dad2b0`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPUdpConnection`
- **多重性**: [1..255]

**容器描述**:

This Container describes a Udp connection to the lower layer SoAd module.

######## 参数配置

此容器包含 **1** 个参数：

######### BOOLEAN 类型参数

########## 1. DoIPRequestAddressAssignment

- **UUID**: `ECUC:8d1ae703-ec0c-9471-4b05-edd862510501`
- **参数名**: `DoIPRequestAddressAssignment`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: The DoIP module shall request IP address assignment by calling SoAd_RequestIpAddrAssignment() for the TcpIpLocalAddr related to this DoIpConnection.

######## 配置容器

本模块包含 **2** 个配置容器：

######### 1. DoIPSoAdUdpRxPdu

**容器属性**:

- **UUID**: `ECUC:799689c9-1f1f-4245-8228-18b7bf0c2dee`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPSoAdUdpRxPdu`
- **多重性**: [1..1]

**容器描述**:

This container describes a Rx PDU received via SoAd over UDP.

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. DoIPSoAdUdpRxPduId

- **UUID**: `ECUC:103f1b68-c87a-4b28-ad2b-a9a27b600be2`
- **参数名**: `DoIPSoAdUdpRxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **描述**: The DoIPSoAdUdpRxPduId is required by the API call DoIP_SoAdIfRxIndication to receive I-PDUs from the SoAd.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. DoIPSoAdUdpRxPduRef

- **UUID**: `ECUC:fd7f5cdf-7cf4-45f4-a627-2d343a8f7ed5`
- **引用名**: `DoIPSoAdUdpRxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the "global" Pdu structure to allow harmonization of handle IDs in the COM-Stack.

######### 2. DoIPSoAdUdpTxPdu

**容器属性**:

- **UUID**: `ECUC:b3d21ded-7966-4862-8d48-ddf2775239cc`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPSoAdUdpTxPdu`
- **多重性**: [1..1]

**容器描述**:

This container describes a Tx PDU sent via SoAd over UDP.

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. DoIPSoAdUdpTxPduId

- **UUID**: `ECUC:2f55a1ec-664b-4bd6-9da3-2f80f2a73746`
- **参数名**: `DoIPSoAdUdpTxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **描述**: The DoIPSoAdUdpTxPduId is required by the API call DoIP_SoAdIfTxConfirmation that is called by the SoAd to confirm that the IPdu has been transmitted successfully.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. DoIPSoAdUdpTxPduRef

- **UUID**: `ECUC:c31e5dee-28e5-4b32-8cec-51f54e77a3a3`
- **引用名**: `DoIPSoAdUdpTxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the "global" Pdu structure to allow harmonization of handle IDs in the COM-Stack.

####### 10. DoIPSoAdUdpRxPdu

**容器属性**:

- **UUID**: `ECUC:799689c9-1f1f-4245-8228-18b7bf0c2dee`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPSoAdUdpRxPdu`
- **多重性**: [1..1]

**容器描述**:

This container describes a Rx PDU received via SoAd over UDP.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. DoIPSoAdUdpRxPduId

- **UUID**: `ECUC:103f1b68-c87a-4b28-ad2b-a9a27b600be2`
- **参数名**: `DoIPSoAdUdpRxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **描述**: The DoIPSoAdUdpRxPduId is required by the API call DoIP_SoAdIfRxIndication to receive I-PDUs from the SoAd.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. DoIPSoAdUdpRxPduRef

- **UUID**: `ECUC:fd7f5cdf-7cf4-45f4-a627-2d343a8f7ed5`
- **引用名**: `DoIPSoAdUdpRxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the "global" Pdu structure to allow harmonization of handle IDs in the COM-Stack.

####### 11. DoIPSoAdUdpTxPdu

**容器属性**:

- **UUID**: `ECUC:b3d21ded-7966-4862-8d48-ddf2775239cc`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPSoAdUdpTxPdu`
- **多重性**: [1..1]

**容器描述**:

This container describes a Tx PDU sent via SoAd over UDP.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. DoIPSoAdUdpTxPduId

- **UUID**: `ECUC:2f55a1ec-664b-4bd6-9da3-2f80f2a73746`
- **参数名**: `DoIPSoAdUdpTxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **描述**: The DoIPSoAdUdpTxPduId is required by the API call DoIP_SoAdIfTxConfirmation that is called by the SoAd to confirm that the IPdu has been transmitted successfully.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. DoIPSoAdUdpTxPduRef

- **UUID**: `ECUC:c31e5dee-28e5-4b32-8cec-51f54e77a3a3`
- **引用名**: `DoIPSoAdUdpTxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the "global" Pdu structure to allow harmonization of handle IDs in the COM-Stack.

####### 12. DoIPUdpVehicleAnnouncementConnection

**容器属性**:

- **UUID**: `ECUC:ec10775c-9dc4-49d9-b17b-73c202f875ed`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPUdpVehicleAnnouncementConnection`
- **多重性**: [1..255]

**容器描述**:

This container describes the UDP multicast connections to the lower layer SoAd module.

######## 参数配置

此容器包含 **1** 个参数：

######### BOOLEAN 类型参数

########## 1. DoIPRequestAddressAssignment

- **UUID**: `ECUC:67eff5dd-1c6e-902a-5fca-f998126ea83e`
- **参数名**: `DoIPRequestAddressAssignment`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: The DoIP module shall request IP address assignment by calling SoAd_RequestIpAddrAssignment() for the TcpIpLocalAddr related to this DoIpConnection.

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. DoIPSoAdUdpVehicleAnnouncementTxPdu

**容器属性**:

- **UUID**: `ECUC:ca2c98f1-142e-4d74-b3e2-a2c7a5d2a5a7`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPSoAdUdpVehicleAnnouncementTxPdu`
- **多重性**: [1..1]

**容器描述**:

This container describes the vehicle announcement TxPdu sent via the SoAd.

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. DoIPSoAdUdpVehicleAnnouncementTxPduId

- **UUID**: `ECUC:d714703b-f033-4dcf-91de-1b6f531e9af7`
- **参数名**: `DoIPSoAdUdpVehicleAnnouncementTxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **描述**: The DoIPSoAdUdpVehicleAnnouncementTxPduId is required by the API call DoIP_SoAdIfTxConfirmation() that is called by the SoAd to confirm that the IPdu has been transmitted successfully.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. DoIPSoAdUdpVehicleAnnouncementTxPduRef

- **UUID**: `ECUC:90da376e-29ea-4262-aa92-05bf32a3971e`
- **引用名**: `DoIPSoAdUdpVehicleAnnouncementTxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the "global" PDU structure to allow harmonization of handle IDs in the COM-Stack.

####### 13. DoIPSoAdUdpVehicleAnnouncementTxPdu

**容器属性**:

- **UUID**: `ECUC:ca2c98f1-142e-4d74-b3e2-a2c7a5d2a5a7`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPSoAdUdpVehicleAnnouncementTxPdu`
- **多重性**: [1..1]

**容器描述**:

This container describes the vehicle announcement TxPdu sent via the SoAd.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. DoIPSoAdUdpVehicleAnnouncementTxPduId

- **UUID**: `ECUC:d714703b-f033-4dcf-91de-1b6f531e9af7`
- **参数名**: `DoIPSoAdUdpVehicleAnnouncementTxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **描述**: The DoIPSoAdUdpVehicleAnnouncementTxPduId is required by the API call DoIP_SoAdIfTxConfirmation() that is called by the SoAd to confirm that the IPdu has been transmitted successfully.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. DoIPSoAdUdpVehicleAnnouncementTxPduRef

- **UUID**: `ECUC:90da376e-29ea-4262-aa92-05bf32a3971e`
- **引用名**: `DoIPSoAdUdpVehicleAnnouncementTxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the "global" PDU structure to allow harmonization of handle IDs in the COM-Stack.

####### 14. DoIPFurtherActionByteCallback

**容器属性**:

- **UUID**: `ECUC:5aac8f6a-2a4d-4d01-af2e-645e910e158d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPFurtherActionByteCallback`
- **多重性**: [0..1]

**容器描述**:

This container describes the Callbackfunction to get the Further Action byte. This container shall always be present. If the DoIPFurtherActionByteDirect parameter is not present, the DoIP module will use an RPort of ServiceInterface CallbackGetFurtherActionByte with the name "CBGetFurtherActionByte_<shortname of enclosing DoIPInterface container>".

######## 参数配置

此容器包含 **1** 个参数：

######### FUNCTION-NAME 类型参数

########## 1. DoIPFurtherActionByteDirect

- **UUID**: `ECUC:b16ec364-7eb2-447e-ad3a-c55fe58378cb`
- **参数名**: `DoIPFurtherActionByteDirect`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **函数变体**:
- **描述**: Direct C Callback function to get the OEM specific Further Action Byte for the DoIP vehicle identification response/vehicle announcement. If the DoIPFurtherActionByteDirect parameter is present, the DoIP module will not use an RPort of ServiceInterface "CBGetFurtherActionByte" but will call the configured function.

####### 15. DoIPRoutingActivation

**容器属性**:

- **UUID**: `ECUC:8c07e2b0-4dd1-45fc-89ae-19a97da7e734`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPRoutingActivation`
- **多重性**: [0..255]

**容器描述**:

This container describes the routing activation possibilities by representing for each container a possible routing activation request message to the DoIP entity and the according references to the activated diagnostic messages.

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. DoIPRoutingActivationNumber

- **UUID**: `ECUC:335e310b-8d47-48bf-b643-5c12468a5f01`
- **参数名**: `DoIPRoutingActivationNumber`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Identifies the Routing activation Number which is received for a DoIP routing activation request message.

######### BOOLEAN 类型参数

########## 1. DoIPRoutingActivationSecurityRequired

- **UUID**: `ECUC:d645dea9-213c-4ac7-9407-a6cc7586ae8f`
- **参数名**: `DoIPRoutingActivationSecurityRequired`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Indicates if a routing activation requires a secure TCP connection

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. DoIPTargetAddressRef

- **UUID**: `ECUC:ebc9f44b-f588-4a77-a371-08bfa7d33272`
- **引用名**: `DoIPTargetAddressRef`
- **引用类型**: REFERENCE
- **多重性**: [1..65535]
- **目标**: `DoIPTargetAddress`
- **完整路径**: `/AUTOSAR/EcucDefs/DoIP/DoIPConfigSet/DoIPInterface/DoIPConnections/DoIPTargetAddress`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to all DoIPTargetAddress which are activated on this Routing activation.

######## 配置容器

本模块包含 **2** 个配置容器：

######### 1. DoIPRoutingActivationAuthenticationCallback

**容器属性**:

- **UUID**: `ECUC:726377c7-0039-4edc-b57c-dd98bc5e99b7`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPRoutingActivationAuthenticationCallback`
- **多重性**: [0..1]

**容器描述**:

Container describes the Callbackfunction to call on a Routing Activation Request for Authentication. If this container is configured but the DoIPRoutingActivationAuthenticationFunc parameter is not present, the DoIP module will use an RPort of ServiceInterface <RoutingActivation>_RoutingActivation with the name "CB<RoutingActivation>RoutingActivation". <RoutingActivation> is the ShortName of the DoIPRoutingActiviation container.

########## 参数配置

此容器包含 **3** 个参数：

########### INTEGER 类型参数

############ 1. DoIPRoutingActivationAuthenticationReqLength

- **UUID**: `ECUC:2abdcf96-9b8e-4936-afc0-ede76b21f3a7`
- **参数名**: `DoIPRoutingActivationAuthenticationReqLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Describes the amount of bytes used to handle to the authentication function on routing activation. If 0 is configured as length the parameter AuthenticationReqData will not be handled to the API.

############ 2. DoIPRoutingActivationAuthenticationResLength

- **UUID**: `ECUC:45e1fc22-6491-40ed-87b8-7917007771a8`
- **参数名**: `DoIPRoutingActivationAuthenticationResLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Describes the amount of bytes used to read by the authentication function on routing activation. If 0 is configured as length the parameter AuthenticationResData will not be fetched via the API.

########### FUNCTION-NAME 类型参数

############ 1. DoIPRoutingActivationAuthenticationFunc

- **UUID**: `ECUC:05ef7a06-64da-467c-be24-d40bac66acc3`
- **参数名**: `DoIPRoutingActivationAuthenticationFunc`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **函数变体**:
- **描述**: Direct C Callback function to trigger the authentication function for routing activation. If the DoIPRoutingActivationAuthenticationFunc parameter is present, the DoIP module will not use an RPort of ServiceInterface <RoutingActivation>_RoutingActivation but call the configured function.

######### 2. DoIPRoutingActivationConfirmationCallback

**容器属性**:

- **UUID**: `ECUC:7e1d1ce3-eff6-43ab-a071-e6b83dfa4855`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPRoutingActivationConfirmationCallback`
- **多重性**: [0..1]

**容器描述**:

Container describes the Callbackfunction to call on a Routing Activation Request for Confirmation. If this container is configured but the DoIPRoutingActivationConfirmationFunc parameter is not present the DoIP module will use an RPort of ServiceInterface <RoutingActivation>_RoutingActivation with the name "CB<RoutingActivation>RoutingActivation". <RoutingActivation> is the ShortName of the DoIPRoutingActiviation container.

########## 参数配置

此容器包含 **3** 个参数：

########### INTEGER 类型参数

############ 1. DoIPRoutingActivationConfirmationReqLength

- **UUID**: `ECUC:b5b1030f-ad9f-4bbf-b2a0-9674bf5f20a7`
- **参数名**: `DoIPRoutingActivationConfirmationReqLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Describes the amount of bytes used to handle to the confirmation function on routing activation. If 0 is configured as length the parameter ConfirmedReqData will not be handled to the API.

############ 2. DoIPRoutingActivationConfirmationResLength

- **UUID**: `ECUC:701e1997-d200-4ee4-8372-e5eb0dc94c56`
- **参数名**: `DoIPRoutingActivationConfirmationResLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Describes the amount of bytes used to read by the confirmation function on routing activation. If 0 is configured as length the parameter ConfirmedResData will not be fetched via the API.

########### FUNCTION-NAME 类型参数

############ 1. DoIPRoutingActivationConfirmationFunc

- **UUID**: `ECUC:4630dc00-f4e8-4bf0-b18c-1a98a4f2f7c9`
- **参数名**: `DoIPRoutingActivationConfirmationFunc`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **函数变体**:
- **描述**: Direct C Callback function to trigger the confirmation function for routing activation. If the DoIPRoutingActivationConfirmationFunc parameter is present the DoIP module will not use an RPort of ServiceInterface <RoutingActivation>_RoutingActivation but call the configured function.

####### 16. DoIPRoutingActivationAuthenticationCallback

**容器属性**:

- **UUID**: `ECUC:726377c7-0039-4edc-b57c-dd98bc5e99b7`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPRoutingActivationAuthenticationCallback`
- **多重性**: [0..1]

**容器描述**:

Container describes the Callbackfunction to call on a Routing Activation Request for Authentication. If this container is configured but the DoIPRoutingActivationAuthenticationFunc parameter is not present, the DoIP module will use an RPort of ServiceInterface <RoutingActivation>_RoutingActivation with the name "CB<RoutingActivation>RoutingActivation". <RoutingActivation> is the ShortName of the DoIPRoutingActiviation container.

######## 参数配置

此容器包含 **3** 个参数：

######### INTEGER 类型参数

########## 1. DoIPRoutingActivationAuthenticationReqLength

- **UUID**: `ECUC:2abdcf96-9b8e-4936-afc0-ede76b21f3a7`
- **参数名**: `DoIPRoutingActivationAuthenticationReqLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Describes the amount of bytes used to handle to the authentication function on routing activation. If 0 is configured as length the parameter AuthenticationReqData will not be handled to the API.

########## 2. DoIPRoutingActivationAuthenticationResLength

- **UUID**: `ECUC:45e1fc22-6491-40ed-87b8-7917007771a8`
- **参数名**: `DoIPRoutingActivationAuthenticationResLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Describes the amount of bytes used to read by the authentication function on routing activation. If 0 is configured as length the parameter AuthenticationResData will not be fetched via the API.

######### FUNCTION-NAME 类型参数

########## 1. DoIPRoutingActivationAuthenticationFunc

- **UUID**: `ECUC:05ef7a06-64da-467c-be24-d40bac66acc3`
- **参数名**: `DoIPRoutingActivationAuthenticationFunc`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **函数变体**:
- **描述**: Direct C Callback function to trigger the authentication function for routing activation. If the DoIPRoutingActivationAuthenticationFunc parameter is present, the DoIP module will not use an RPort of ServiceInterface <RoutingActivation>_RoutingActivation but call the configured function.

####### 17. DoIPRoutingActivationConfirmationCallback

**容器属性**:

- **UUID**: `ECUC:7e1d1ce3-eff6-43ab-a071-e6b83dfa4855`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPRoutingActivationConfirmationCallback`
- **多重性**: [0..1]

**容器描述**:

Container describes the Callbackfunction to call on a Routing Activation Request for Confirmation. If this container is configured but the DoIPRoutingActivationConfirmationFunc parameter is not present the DoIP module will use an RPort of ServiceInterface <RoutingActivation>_RoutingActivation with the name "CB<RoutingActivation>RoutingActivation". <RoutingActivation> is the ShortName of the DoIPRoutingActiviation container.

######## 参数配置

此容器包含 **3** 个参数：

######### INTEGER 类型参数

########## 1. DoIPRoutingActivationConfirmationReqLength

- **UUID**: `ECUC:b5b1030f-ad9f-4bbf-b2a0-9674bf5f20a7`
- **参数名**: `DoIPRoutingActivationConfirmationReqLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Describes the amount of bytes used to handle to the confirmation function on routing activation. If 0 is configured as length the parameter ConfirmedReqData will not be handled to the API.

########## 2. DoIPRoutingActivationConfirmationResLength

- **UUID**: `ECUC:701e1997-d200-4ee4-8372-e5eb0dc94c56`
- **参数名**: `DoIPRoutingActivationConfirmationResLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Describes the amount of bytes used to read by the confirmation function on routing activation. If 0 is configured as length the parameter ConfirmedResData will not be fetched via the API.

######### FUNCTION-NAME 类型参数

########## 1. DoIPRoutingActivationConfirmationFunc

- **UUID**: `ECUC:4630dc00-f4e8-4bf0-b18c-1a98a4f2f7c9`
- **参数名**: `DoIPRoutingActivationConfirmationFunc`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **函数变体**:
- **描述**: Direct C Callback function to trigger the confirmation function for routing activation. If the DoIPRoutingActivationConfirmationFunc parameter is present the DoIP module will not use an RPort of ServiceInterface <RoutingActivation>_RoutingActivation but call the configured function.

####### 18. DoIPTester

**容器属性**:

- **UUID**: `ECUC:5ec2063c-2a23-4da2-be67-e7cd0a80ee93`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPTester`
- **多重性**: [0..255]

**容器描述**:

This container describes the properties of the possible connectable Tester for the DoIP entity.

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. DoIPNumByteDiagAckNack

- **UUID**: `ECUC:2cdb3b03-189a-4c0d-847c-ec5cbe717265`
- **参数名**: `DoIPNumByteDiagAckNack`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Specifies the number of original Diagnostic request bytes the DoIP entity responses on a NACK of a diagnostic response message to the Tester.

########## 2. DoIPTesterSA

- **UUID**: `ECUC:44ccb383-1ad0-47a4-a3c4-5056f05a922d`
- **参数名**: `DoIPTesterSA`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Source Address of the Tester sent via routing activation or diagnostic message.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. DoIPRoutingActivationRef

- **UUID**: `ECUC:cc241bfa-5d3c-4e9b-b190-f764add15a77`
- **引用名**: `DoIPRoutingActivationRef`
- **引用类型**: REFERENCE
- **多重性**: [1..255]
- **目标**: `DoIPRoutingActivation`
- **完整路径**: `/AUTOSAR/EcucDefs/DoIP/DoIPConfigSet/DoIPInterface/DoIPRoutingActivation`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to a DoIPRoutingActivation describing the possible routing activations of the DoIPTester

##### 3. DoIPChannel

**容器属性**:

- **UUID**: `ECUC:ce8927a0-58c7-4099-a996-3ee43001e9e8`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPChannel`
- **多重性**: [1..65536]

**容器描述**:

Configuration of one DoIPChannel.

###### 引用关系

此容器包含 **2** 个引用：

####### REFERENCE 类型引用

######## 1. DoIPChannelSARef

- **UUID**: `ECUC:893cf71a-c06b-4044-812c-8df50e45d13e`
- **引用名**: `DoIPChannelSARef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `DoIPTester`
- **完整路径**: `/AUTOSAR/EcucDefs/DoIP/DoIPConfigSet/DoIPInterface/DoIPTester`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the DoIPTester.

######## 2. DoIPChannelTARef

- **UUID**: `ECUC:cbe1685e-4306-4efc-8345-5a1446b28405`
- **引用名**: `DoIPChannelTARef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `DoIPTargetAddress`
- **完整路径**: `/AUTOSAR/EcucDefs/DoIP/DoIPConfigSet/DoIPInterface/DoIPConnections/DoIPTargetAddress`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the target address.

###### 配置容器

本模块包含 **2** 个配置容器：

####### 1. DoIPPduRRxPdu

**容器属性**:

- **UUID**: `ECUC:63341ec1-b4ca-4bbc-82b5-a883d528b7c1`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPPduRRxPdu`
- **多重性**: [0..1]

**容器描述**:

This container contains the Rx Pdus to connect with the Rx Pdus of the PduR.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. DoIPPduRRxPduId

- **UUID**: `ECUC:affbfe09-cf4f-43ed-91f0-957c1e71f17f`
- **参数名**: `DoIPPduRRxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **描述**: The DoIPPduRRxPduId is required by the API call DoIP_TpCancelReceive.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. DoIPPduRRxPduRef

- **UUID**: `ECUC:0fb53490-8f12-418b-a048-feaf0c60d6b0`
- **引用名**: `DoIPPduRRxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the "global" Pdu structure to allow harmonization of handle IDs in the COM-Stack.

####### 2. DoIPPduRTxPdu

**容器属性**:

- **UUID**: `ECUC:ecf769bc-a264-4426-a107-185d357d42b4`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPPduRTxPdu`
- **多重性**: [0..1]

**容器描述**:

This container contains the Tx Pdus to connect with the Tx Pdus of the PduR.  If the parameter is not configured the channel is for functional addressing.

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. DoIPPduRTxPduId

- **UUID**: `ECUC:4ec22559-5780-41ca-af56-0b32ecdd6dae`
- **参数名**: `DoIPPduRTxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **描述**: The DoIPPduRTxPduId is required by DoIP_TpTransmit or DoIP_IfTransmit and DoIP_TpCancelTransmit.

######### ENUMERATION 类型参数

########## 1. DoIPPduType

- **UUID**: `ECUC:17c8aace-cda8-471d-8cb2-e474dda9c61a`
- **参数名**: `DoIPPduType`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `DOIP_TPPDU`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `DOIP_IFPDU` (来源: AUTOSAR_ECUC)
  - `DOIP_TPPDU` (来源: AUTOSAR_ECUC)
- **描述**: API Type to use for communication with PduR. DOIP_IFPDU for UUDT messages, DOIP_TPPDU for all other diagnostic messages.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. DoIPPduRTxPduRef

- **UUID**: `ECUC:f703fb82-d2e7-4545-a97c-3275ff0bfc5d`
- **引用名**: `DoIPPduRTxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the "global" Pdu structure to allow harmonization of handle IDs in the COM-Stack.

##### 4. DoIPPduRRxPdu

**容器属性**:

- **UUID**: `ECUC:63341ec1-b4ca-4bbc-82b5-a883d528b7c1`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPPduRRxPdu`
- **多重性**: [0..1]

**容器描述**:

This container contains the Rx Pdus to connect with the Rx Pdus of the PduR.

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. DoIPPduRRxPduId

- **UUID**: `ECUC:affbfe09-cf4f-43ed-91f0-957c1e71f17f`
- **参数名**: `DoIPPduRRxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **描述**: The DoIPPduRRxPduId is required by the API call DoIP_TpCancelReceive.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. DoIPPduRRxPduRef

- **UUID**: `ECUC:0fb53490-8f12-418b-a048-feaf0c60d6b0`
- **引用名**: `DoIPPduRRxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the "global" Pdu structure to allow harmonization of handle IDs in the COM-Stack.

##### 5. DoIPPduRTxPdu

**容器属性**:

- **UUID**: `ECUC:ecf769bc-a264-4426-a107-185d357d42b4`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPPduRTxPdu`
- **多重性**: [0..1]

**容器描述**:

This container contains the Tx Pdus to connect with the Tx Pdus of the PduR.  If the parameter is not configured the channel is for functional addressing.

###### 参数配置

此容器包含 **2** 个参数：

####### INTEGER 类型参数

######## 1. DoIPPduRTxPduId

- **UUID**: `ECUC:4ec22559-5780-41ca-af56-0b32ecdd6dae`
- **参数名**: `DoIPPduRTxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **描述**: The DoIPPduRTxPduId is required by DoIP_TpTransmit or DoIP_IfTransmit and DoIP_TpCancelTransmit.

####### ENUMERATION 类型参数

######## 1. DoIPPduType

- **UUID**: `ECUC:17c8aace-cda8-471d-8cb2-e474dda9c61a`
- **参数名**: `DoIPPduType`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `DOIP_TPPDU`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `DOIP_IFPDU` (来源: AUTOSAR_ECUC)
  - `DOIP_TPPDU` (来源: AUTOSAR_ECUC)
- **描述**: API Type to use for communication with PduR. DOIP_IFPDU for UUDT messages, DOIP_TPPDU for all other diagnostic messages.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. DoIPPduRTxPduRef

- **UUID**: `ECUC:f703fb82-d2e7-4545-a97c-3275ff0bfc5d`
- **引用名**: `DoIPPduRTxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the "global" Pdu structure to allow harmonization of handle IDs in the COM-Stack.

##### 6. DoIPConnections

**容器属性**:

- **UUID**: `ECUC:06a174a5-5ad6-4b7a-8ce8-c64883f2e5c5`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPConnections`
- **多重性**: [1..1]

**容器描述**:

Container contains all lower layer connection specific information, i.e. the single Pdu References and Handle IDs to the SoAd.

###### 配置容器

本模块包含 **9** 个配置容器：

####### 1. DoIPTargetAddress

**容器属性**:

- **UUID**: `ECUC:11b8faaf-bc59-49fe-97b5-29df73fa6ee7`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPTargetAddress`
- **多重性**: [1..65535]

**容器描述**:

This container describes a possible TargetAddress that is supported by DoIP.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. DoIPTargetAddressValue

- **UUID**: `ECUC:c46011a4-ab1a-42cf-a2f8-b71632fcfd59`
- **参数名**: `DoIPTargetAddressValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Valid Target Address of a DoIP target address.

####### 2. DoIPTcpConnection

**容器属性**:

- **UUID**: `ECUC:e3ccdc1d-8a6b-40a0-abbf-59a1db67e267`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPTcpConnection`
- **多重性**: [1..255]

**容器描述**:

This container describes a TCP connection to the lower layer SoAd module.

######## 参数配置

此容器包含 **2** 个参数：

######### BOOLEAN 类型参数

########## 1. DoIPRequestAddressAssignment

- **UUID**: `ECUC:5fac5a9e-0915-86f1-5a0e-df77eade14b8`
- **参数名**: `DoIPRequestAddressAssignment`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: The DoIP module shall request IP address assignment by calling SoAd_RequestIpAddrAssignment() for the TcpIpLocalAddr related to this DoIpConnection.

########## 2. DoIPTcpConnectionSecurityRequired

- **UUID**: `ECUC:e723d1bf-784e-4527-892c-4fcbf9e11e05`
- **参数名**: `DoIPTcpConnectionSecurityRequired`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Indicates if the associated TCP socket uses a secure connection (e.g. TLS)

######## 配置容器

本模块包含 **2** 个配置容器：

######### 1. DoIPSoAdTcpRxPdu

**容器属性**:

- **UUID**: `ECUC:f8ff31c4-d60d-4316-b021-67cb31934ee7`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPSoAdTcpRxPdu`
- **多重性**: [1..1]

**容器描述**:

This container describes a Rx PDU received via SoAd over TCP

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. DoIPSoAdTcpRxPduId

- **UUID**: `ECUC:87bc6f78-b949-44dd-a958-16f6c2003d78`
- **参数名**: `DoIPSoAdTcpRxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **描述**: The DoIPSoAdTcpRxPduId is required by the API call DoIP_SoAdTpRxIndication to receive I-PDUs from the SoAd.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. DoIPSoAdTcpRxPduRef

- **UUID**: `ECUC:7fa9533f-a369-48ce-8666-1982b51d007d`
- **引用名**: `DoIPSoAdTcpRxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the "global" Pdu structure to allow harmonization of handle IDs in the COM-Stack.

######### 2. DoIPSoAdTcpTxPdu

**容器属性**:

- **UUID**: `ECUC:b94850e4-7ec7-4c7a-95d7-e883570c386f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPSoAdTcpTxPdu`
- **多重性**: [1..1]

**容器描述**:

This container describes a Tx PDU sent via SoAd over TCP

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. DoIPSoAdTcpTxPduId

- **UUID**: `ECUC:18866fc8-b1b6-4749-866c-8d0dff665d6e`
- **参数名**: `DoIPSoAdTcpTxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **描述**: The DoIPSoAdTcpTxPduId is required by the API call DoIP_SoAdTpTxConfirmation that is called by the SoAd to confirm that the IPdu has been transmitted successfully.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. DoIPSoAdTcpTxPduRef

- **UUID**: `ECUC:71678586-2f21-4e4f-aefc-997db5b282a4`
- **引用名**: `DoIPSoAdTcpTxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the "global" Pdu structure to allow harmonization of handle IDs in the COM-Stack.

####### 3. DoIPSoAdTcpRxPdu

**容器属性**:

- **UUID**: `ECUC:f8ff31c4-d60d-4316-b021-67cb31934ee7`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPSoAdTcpRxPdu`
- **多重性**: [1..1]

**容器描述**:

This container describes a Rx PDU received via SoAd over TCP

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. DoIPSoAdTcpRxPduId

- **UUID**: `ECUC:87bc6f78-b949-44dd-a958-16f6c2003d78`
- **参数名**: `DoIPSoAdTcpRxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **描述**: The DoIPSoAdTcpRxPduId is required by the API call DoIP_SoAdTpRxIndication to receive I-PDUs from the SoAd.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. DoIPSoAdTcpRxPduRef

- **UUID**: `ECUC:7fa9533f-a369-48ce-8666-1982b51d007d`
- **引用名**: `DoIPSoAdTcpRxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the "global" Pdu structure to allow harmonization of handle IDs in the COM-Stack.

####### 4. DoIPSoAdTcpTxPdu

**容器属性**:

- **UUID**: `ECUC:b94850e4-7ec7-4c7a-95d7-e883570c386f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPSoAdTcpTxPdu`
- **多重性**: [1..1]

**容器描述**:

This container describes a Tx PDU sent via SoAd over TCP

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. DoIPSoAdTcpTxPduId

- **UUID**: `ECUC:18866fc8-b1b6-4749-866c-8d0dff665d6e`
- **参数名**: `DoIPSoAdTcpTxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **描述**: The DoIPSoAdTcpTxPduId is required by the API call DoIP_SoAdTpTxConfirmation that is called by the SoAd to confirm that the IPdu has been transmitted successfully.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. DoIPSoAdTcpTxPduRef

- **UUID**: `ECUC:71678586-2f21-4e4f-aefc-997db5b282a4`
- **引用名**: `DoIPSoAdTcpTxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the "global" Pdu structure to allow harmonization of handle IDs in the COM-Stack.

####### 5. DoIPUdpConnection

**容器属性**:

- **UUID**: `ECUC:113b6883-6d62-4e20-9cb6-680252dad2b0`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPUdpConnection`
- **多重性**: [1..255]

**容器描述**:

This Container describes a Udp connection to the lower layer SoAd module.

######## 参数配置

此容器包含 **1** 个参数：

######### BOOLEAN 类型参数

########## 1. DoIPRequestAddressAssignment

- **UUID**: `ECUC:8d1ae703-ec0c-9471-4b05-edd862510501`
- **参数名**: `DoIPRequestAddressAssignment`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: The DoIP module shall request IP address assignment by calling SoAd_RequestIpAddrAssignment() for the TcpIpLocalAddr related to this DoIpConnection.

######## 配置容器

本模块包含 **2** 个配置容器：

######### 1. DoIPSoAdUdpRxPdu

**容器属性**:

- **UUID**: `ECUC:799689c9-1f1f-4245-8228-18b7bf0c2dee`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPSoAdUdpRxPdu`
- **多重性**: [1..1]

**容器描述**:

This container describes a Rx PDU received via SoAd over UDP.

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. DoIPSoAdUdpRxPduId

- **UUID**: `ECUC:103f1b68-c87a-4b28-ad2b-a9a27b600be2`
- **参数名**: `DoIPSoAdUdpRxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **描述**: The DoIPSoAdUdpRxPduId is required by the API call DoIP_SoAdIfRxIndication to receive I-PDUs from the SoAd.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. DoIPSoAdUdpRxPduRef

- **UUID**: `ECUC:fd7f5cdf-7cf4-45f4-a627-2d343a8f7ed5`
- **引用名**: `DoIPSoAdUdpRxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the "global" Pdu structure to allow harmonization of handle IDs in the COM-Stack.

######### 2. DoIPSoAdUdpTxPdu

**容器属性**:

- **UUID**: `ECUC:b3d21ded-7966-4862-8d48-ddf2775239cc`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPSoAdUdpTxPdu`
- **多重性**: [1..1]

**容器描述**:

This container describes a Tx PDU sent via SoAd over UDP.

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. DoIPSoAdUdpTxPduId

- **UUID**: `ECUC:2f55a1ec-664b-4bd6-9da3-2f80f2a73746`
- **参数名**: `DoIPSoAdUdpTxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **描述**: The DoIPSoAdUdpTxPduId is required by the API call DoIP_SoAdIfTxConfirmation that is called by the SoAd to confirm that the IPdu has been transmitted successfully.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. DoIPSoAdUdpTxPduRef

- **UUID**: `ECUC:c31e5dee-28e5-4b32-8cec-51f54e77a3a3`
- **引用名**: `DoIPSoAdUdpTxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the "global" Pdu structure to allow harmonization of handle IDs in the COM-Stack.

####### 6. DoIPSoAdUdpRxPdu

**容器属性**:

- **UUID**: `ECUC:799689c9-1f1f-4245-8228-18b7bf0c2dee`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPSoAdUdpRxPdu`
- **多重性**: [1..1]

**容器描述**:

This container describes a Rx PDU received via SoAd over UDP.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. DoIPSoAdUdpRxPduId

- **UUID**: `ECUC:103f1b68-c87a-4b28-ad2b-a9a27b600be2`
- **参数名**: `DoIPSoAdUdpRxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **描述**: The DoIPSoAdUdpRxPduId is required by the API call DoIP_SoAdIfRxIndication to receive I-PDUs from the SoAd.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. DoIPSoAdUdpRxPduRef

- **UUID**: `ECUC:fd7f5cdf-7cf4-45f4-a627-2d343a8f7ed5`
- **引用名**: `DoIPSoAdUdpRxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the "global" Pdu structure to allow harmonization of handle IDs in the COM-Stack.

####### 7. DoIPSoAdUdpTxPdu

**容器属性**:

- **UUID**: `ECUC:b3d21ded-7966-4862-8d48-ddf2775239cc`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPSoAdUdpTxPdu`
- **多重性**: [1..1]

**容器描述**:

This container describes a Tx PDU sent via SoAd over UDP.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. DoIPSoAdUdpTxPduId

- **UUID**: `ECUC:2f55a1ec-664b-4bd6-9da3-2f80f2a73746`
- **参数名**: `DoIPSoAdUdpTxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **描述**: The DoIPSoAdUdpTxPduId is required by the API call DoIP_SoAdIfTxConfirmation that is called by the SoAd to confirm that the IPdu has been transmitted successfully.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. DoIPSoAdUdpTxPduRef

- **UUID**: `ECUC:c31e5dee-28e5-4b32-8cec-51f54e77a3a3`
- **引用名**: `DoIPSoAdUdpTxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the "global" Pdu structure to allow harmonization of handle IDs in the COM-Stack.

####### 8. DoIPUdpVehicleAnnouncementConnection

**容器属性**:

- **UUID**: `ECUC:ec10775c-9dc4-49d9-b17b-73c202f875ed`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPUdpVehicleAnnouncementConnection`
- **多重性**: [1..255]

**容器描述**:

This container describes the UDP multicast connections to the lower layer SoAd module.

######## 参数配置

此容器包含 **1** 个参数：

######### BOOLEAN 类型参数

########## 1. DoIPRequestAddressAssignment

- **UUID**: `ECUC:67eff5dd-1c6e-902a-5fca-f998126ea83e`
- **参数名**: `DoIPRequestAddressAssignment`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: The DoIP module shall request IP address assignment by calling SoAd_RequestIpAddrAssignment() for the TcpIpLocalAddr related to this DoIpConnection.

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. DoIPSoAdUdpVehicleAnnouncementTxPdu

**容器属性**:

- **UUID**: `ECUC:ca2c98f1-142e-4d74-b3e2-a2c7a5d2a5a7`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPSoAdUdpVehicleAnnouncementTxPdu`
- **多重性**: [1..1]

**容器描述**:

This container describes the vehicle announcement TxPdu sent via the SoAd.

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. DoIPSoAdUdpVehicleAnnouncementTxPduId

- **UUID**: `ECUC:d714703b-f033-4dcf-91de-1b6f531e9af7`
- **参数名**: `DoIPSoAdUdpVehicleAnnouncementTxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **描述**: The DoIPSoAdUdpVehicleAnnouncementTxPduId is required by the API call DoIP_SoAdIfTxConfirmation() that is called by the SoAd to confirm that the IPdu has been transmitted successfully.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. DoIPSoAdUdpVehicleAnnouncementTxPduRef

- **UUID**: `ECUC:90da376e-29ea-4262-aa92-05bf32a3971e`
- **引用名**: `DoIPSoAdUdpVehicleAnnouncementTxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the "global" PDU structure to allow harmonization of handle IDs in the COM-Stack.

####### 9. DoIPSoAdUdpVehicleAnnouncementTxPdu

**容器属性**:

- **UUID**: `ECUC:ca2c98f1-142e-4d74-b3e2-a2c7a5d2a5a7`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPSoAdUdpVehicleAnnouncementTxPdu`
- **多重性**: [1..1]

**容器描述**:

This container describes the vehicle announcement TxPdu sent via the SoAd.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. DoIPSoAdUdpVehicleAnnouncementTxPduId

- **UUID**: `ECUC:d714703b-f033-4dcf-91de-1b6f531e9af7`
- **参数名**: `DoIPSoAdUdpVehicleAnnouncementTxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **描述**: The DoIPSoAdUdpVehicleAnnouncementTxPduId is required by the API call DoIP_SoAdIfTxConfirmation() that is called by the SoAd to confirm that the IPdu has been transmitted successfully.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. DoIPSoAdUdpVehicleAnnouncementTxPduRef

- **UUID**: `ECUC:90da376e-29ea-4262-aa92-05bf32a3971e`
- **引用名**: `DoIPSoAdUdpVehicleAnnouncementTxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the "global" PDU structure to allow harmonization of handle IDs in the COM-Stack.

##### 7. DoIPTargetAddress

**容器属性**:

- **UUID**: `ECUC:11b8faaf-bc59-49fe-97b5-29df73fa6ee7`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPTargetAddress`
- **多重性**: [1..65535]

**容器描述**:

This container describes a possible TargetAddress that is supported by DoIP.

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. DoIPTargetAddressValue

- **UUID**: `ECUC:c46011a4-ab1a-42cf-a2f8-b71632fcfd59`
- **参数名**: `DoIPTargetAddressValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Valid Target Address of a DoIP target address.

##### 8. DoIPTcpConnection

**容器属性**:

- **UUID**: `ECUC:e3ccdc1d-8a6b-40a0-abbf-59a1db67e267`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPTcpConnection`
- **多重性**: [1..255]

**容器描述**:

This container describes a TCP connection to the lower layer SoAd module.

###### 参数配置

此容器包含 **2** 个参数：

####### BOOLEAN 类型参数

######## 1. DoIPRequestAddressAssignment

- **UUID**: `ECUC:5fac5a9e-0915-86f1-5a0e-df77eade14b8`
- **参数名**: `DoIPRequestAddressAssignment`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: The DoIP module shall request IP address assignment by calling SoAd_RequestIpAddrAssignment() for the TcpIpLocalAddr related to this DoIpConnection.

######## 2. DoIPTcpConnectionSecurityRequired

- **UUID**: `ECUC:e723d1bf-784e-4527-892c-4fcbf9e11e05`
- **参数名**: `DoIPTcpConnectionSecurityRequired`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Indicates if the associated TCP socket uses a secure connection (e.g. TLS)

###### 配置容器

本模块包含 **2** 个配置容器：

####### 1. DoIPSoAdTcpRxPdu

**容器属性**:

- **UUID**: `ECUC:f8ff31c4-d60d-4316-b021-67cb31934ee7`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPSoAdTcpRxPdu`
- **多重性**: [1..1]

**容器描述**:

This container describes a Rx PDU received via SoAd over TCP

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. DoIPSoAdTcpRxPduId

- **UUID**: `ECUC:87bc6f78-b949-44dd-a958-16f6c2003d78`
- **参数名**: `DoIPSoAdTcpRxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **描述**: The DoIPSoAdTcpRxPduId is required by the API call DoIP_SoAdTpRxIndication to receive I-PDUs from the SoAd.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. DoIPSoAdTcpRxPduRef

- **UUID**: `ECUC:7fa9533f-a369-48ce-8666-1982b51d007d`
- **引用名**: `DoIPSoAdTcpRxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the "global" Pdu structure to allow harmonization of handle IDs in the COM-Stack.

####### 2. DoIPSoAdTcpTxPdu

**容器属性**:

- **UUID**: `ECUC:b94850e4-7ec7-4c7a-95d7-e883570c386f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPSoAdTcpTxPdu`
- **多重性**: [1..1]

**容器描述**:

This container describes a Tx PDU sent via SoAd over TCP

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. DoIPSoAdTcpTxPduId

- **UUID**: `ECUC:18866fc8-b1b6-4749-866c-8d0dff665d6e`
- **参数名**: `DoIPSoAdTcpTxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **描述**: The DoIPSoAdTcpTxPduId is required by the API call DoIP_SoAdTpTxConfirmation that is called by the SoAd to confirm that the IPdu has been transmitted successfully.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. DoIPSoAdTcpTxPduRef

- **UUID**: `ECUC:71678586-2f21-4e4f-aefc-997db5b282a4`
- **引用名**: `DoIPSoAdTcpTxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the "global" Pdu structure to allow harmonization of handle IDs in the COM-Stack.

##### 9. DoIPSoAdTcpRxPdu

**容器属性**:

- **UUID**: `ECUC:f8ff31c4-d60d-4316-b021-67cb31934ee7`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPSoAdTcpRxPdu`
- **多重性**: [1..1]

**容器描述**:

This container describes a Rx PDU received via SoAd over TCP

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. DoIPSoAdTcpRxPduId

- **UUID**: `ECUC:87bc6f78-b949-44dd-a958-16f6c2003d78`
- **参数名**: `DoIPSoAdTcpRxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **描述**: The DoIPSoAdTcpRxPduId is required by the API call DoIP_SoAdTpRxIndication to receive I-PDUs from the SoAd.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. DoIPSoAdTcpRxPduRef

- **UUID**: `ECUC:7fa9533f-a369-48ce-8666-1982b51d007d`
- **引用名**: `DoIPSoAdTcpRxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the "global" Pdu structure to allow harmonization of handle IDs in the COM-Stack.

##### 10. DoIPSoAdTcpTxPdu

**容器属性**:

- **UUID**: `ECUC:b94850e4-7ec7-4c7a-95d7-e883570c386f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPSoAdTcpTxPdu`
- **多重性**: [1..1]

**容器描述**:

This container describes a Tx PDU sent via SoAd over TCP

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. DoIPSoAdTcpTxPduId

- **UUID**: `ECUC:18866fc8-b1b6-4749-866c-8d0dff665d6e`
- **参数名**: `DoIPSoAdTcpTxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **描述**: The DoIPSoAdTcpTxPduId is required by the API call DoIP_SoAdTpTxConfirmation that is called by the SoAd to confirm that the IPdu has been transmitted successfully.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. DoIPSoAdTcpTxPduRef

- **UUID**: `ECUC:71678586-2f21-4e4f-aefc-997db5b282a4`
- **引用名**: `DoIPSoAdTcpTxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the "global" Pdu structure to allow harmonization of handle IDs in the COM-Stack.

##### 11. DoIPUdpConnection

**容器属性**:

- **UUID**: `ECUC:113b6883-6d62-4e20-9cb6-680252dad2b0`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPUdpConnection`
- **多重性**: [1..255]

**容器描述**:

This Container describes a Udp connection to the lower layer SoAd module.

###### 参数配置

此容器包含 **1** 个参数：

####### BOOLEAN 类型参数

######## 1. DoIPRequestAddressAssignment

- **UUID**: `ECUC:8d1ae703-ec0c-9471-4b05-edd862510501`
- **参数名**: `DoIPRequestAddressAssignment`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: The DoIP module shall request IP address assignment by calling SoAd_RequestIpAddrAssignment() for the TcpIpLocalAddr related to this DoIpConnection.

###### 配置容器

本模块包含 **2** 个配置容器：

####### 1. DoIPSoAdUdpRxPdu

**容器属性**:

- **UUID**: `ECUC:799689c9-1f1f-4245-8228-18b7bf0c2dee`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPSoAdUdpRxPdu`
- **多重性**: [1..1]

**容器描述**:

This container describes a Rx PDU received via SoAd over UDP.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. DoIPSoAdUdpRxPduId

- **UUID**: `ECUC:103f1b68-c87a-4b28-ad2b-a9a27b600be2`
- **参数名**: `DoIPSoAdUdpRxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **描述**: The DoIPSoAdUdpRxPduId is required by the API call DoIP_SoAdIfRxIndication to receive I-PDUs from the SoAd.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. DoIPSoAdUdpRxPduRef

- **UUID**: `ECUC:fd7f5cdf-7cf4-45f4-a627-2d343a8f7ed5`
- **引用名**: `DoIPSoAdUdpRxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the "global" Pdu structure to allow harmonization of handle IDs in the COM-Stack.

####### 2. DoIPSoAdUdpTxPdu

**容器属性**:

- **UUID**: `ECUC:b3d21ded-7966-4862-8d48-ddf2775239cc`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPSoAdUdpTxPdu`
- **多重性**: [1..1]

**容器描述**:

This container describes a Tx PDU sent via SoAd over UDP.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. DoIPSoAdUdpTxPduId

- **UUID**: `ECUC:2f55a1ec-664b-4bd6-9da3-2f80f2a73746`
- **参数名**: `DoIPSoAdUdpTxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **描述**: The DoIPSoAdUdpTxPduId is required by the API call DoIP_SoAdIfTxConfirmation that is called by the SoAd to confirm that the IPdu has been transmitted successfully.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. DoIPSoAdUdpTxPduRef

- **UUID**: `ECUC:c31e5dee-28e5-4b32-8cec-51f54e77a3a3`
- **引用名**: `DoIPSoAdUdpTxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the "global" Pdu structure to allow harmonization of handle IDs in the COM-Stack.

##### 12. DoIPSoAdUdpRxPdu

**容器属性**:

- **UUID**: `ECUC:799689c9-1f1f-4245-8228-18b7bf0c2dee`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPSoAdUdpRxPdu`
- **多重性**: [1..1]

**容器描述**:

This container describes a Rx PDU received via SoAd over UDP.

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. DoIPSoAdUdpRxPduId

- **UUID**: `ECUC:103f1b68-c87a-4b28-ad2b-a9a27b600be2`
- **参数名**: `DoIPSoAdUdpRxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **描述**: The DoIPSoAdUdpRxPduId is required by the API call DoIP_SoAdIfRxIndication to receive I-PDUs from the SoAd.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. DoIPSoAdUdpRxPduRef

- **UUID**: `ECUC:fd7f5cdf-7cf4-45f4-a627-2d343a8f7ed5`
- **引用名**: `DoIPSoAdUdpRxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the "global" Pdu structure to allow harmonization of handle IDs in the COM-Stack.

##### 13. DoIPSoAdUdpTxPdu

**容器属性**:

- **UUID**: `ECUC:b3d21ded-7966-4862-8d48-ddf2775239cc`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPSoAdUdpTxPdu`
- **多重性**: [1..1]

**容器描述**:

This container describes a Tx PDU sent via SoAd over UDP.

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. DoIPSoAdUdpTxPduId

- **UUID**: `ECUC:2f55a1ec-664b-4bd6-9da3-2f80f2a73746`
- **参数名**: `DoIPSoAdUdpTxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **描述**: The DoIPSoAdUdpTxPduId is required by the API call DoIP_SoAdIfTxConfirmation that is called by the SoAd to confirm that the IPdu has been transmitted successfully.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. DoIPSoAdUdpTxPduRef

- **UUID**: `ECUC:c31e5dee-28e5-4b32-8cec-51f54e77a3a3`
- **引用名**: `DoIPSoAdUdpTxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the "global" Pdu structure to allow harmonization of handle IDs in the COM-Stack.

##### 14. DoIPUdpVehicleAnnouncementConnection

**容器属性**:

- **UUID**: `ECUC:ec10775c-9dc4-49d9-b17b-73c202f875ed`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPUdpVehicleAnnouncementConnection`
- **多重性**: [1..255]

**容器描述**:

This container describes the UDP multicast connections to the lower layer SoAd module.

###### 参数配置

此容器包含 **1** 个参数：

####### BOOLEAN 类型参数

######## 1. DoIPRequestAddressAssignment

- **UUID**: `ECUC:67eff5dd-1c6e-902a-5fca-f998126ea83e`
- **参数名**: `DoIPRequestAddressAssignment`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: The DoIP module shall request IP address assignment by calling SoAd_RequestIpAddrAssignment() for the TcpIpLocalAddr related to this DoIpConnection.

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. DoIPSoAdUdpVehicleAnnouncementTxPdu

**容器属性**:

- **UUID**: `ECUC:ca2c98f1-142e-4d74-b3e2-a2c7a5d2a5a7`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPSoAdUdpVehicleAnnouncementTxPdu`
- **多重性**: [1..1]

**容器描述**:

This container describes the vehicle announcement TxPdu sent via the SoAd.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. DoIPSoAdUdpVehicleAnnouncementTxPduId

- **UUID**: `ECUC:d714703b-f033-4dcf-91de-1b6f531e9af7`
- **参数名**: `DoIPSoAdUdpVehicleAnnouncementTxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **描述**: The DoIPSoAdUdpVehicleAnnouncementTxPduId is required by the API call DoIP_SoAdIfTxConfirmation() that is called by the SoAd to confirm that the IPdu has been transmitted successfully.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. DoIPSoAdUdpVehicleAnnouncementTxPduRef

- **UUID**: `ECUC:90da376e-29ea-4262-aa92-05bf32a3971e`
- **引用名**: `DoIPSoAdUdpVehicleAnnouncementTxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the "global" PDU structure to allow harmonization of handle IDs in the COM-Stack.

##### 15. DoIPSoAdUdpVehicleAnnouncementTxPdu

**容器属性**:

- **UUID**: `ECUC:ca2c98f1-142e-4d74-b3e2-a2c7a5d2a5a7`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPSoAdUdpVehicleAnnouncementTxPdu`
- **多重性**: [1..1]

**容器描述**:

This container describes the vehicle announcement TxPdu sent via the SoAd.

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. DoIPSoAdUdpVehicleAnnouncementTxPduId

- **UUID**: `ECUC:d714703b-f033-4dcf-91de-1b6f531e9af7`
- **参数名**: `DoIPSoAdUdpVehicleAnnouncementTxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **描述**: The DoIPSoAdUdpVehicleAnnouncementTxPduId is required by the API call DoIP_SoAdIfTxConfirmation() that is called by the SoAd to confirm that the IPdu has been transmitted successfully.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. DoIPSoAdUdpVehicleAnnouncementTxPduRef

- **UUID**: `ECUC:90da376e-29ea-4262-aa92-05bf32a3971e`
- **引用名**: `DoIPSoAdUdpVehicleAnnouncementTxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the "global" PDU structure to allow harmonization of handle IDs in the COM-Stack.

##### 16. DoIPFurtherActionByteCallback

**容器属性**:

- **UUID**: `ECUC:5aac8f6a-2a4d-4d01-af2e-645e910e158d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPFurtherActionByteCallback`
- **多重性**: [0..1]

**容器描述**:

This container describes the Callbackfunction to get the Further Action byte. This container shall always be present. If the DoIPFurtherActionByteDirect parameter is not present, the DoIP module will use an RPort of ServiceInterface CallbackGetFurtherActionByte with the name "CBGetFurtherActionByte_<shortname of enclosing DoIPInterface container>".

###### 参数配置

此容器包含 **1** 个参数：

####### FUNCTION-NAME 类型参数

######## 1. DoIPFurtherActionByteDirect

- **UUID**: `ECUC:b16ec364-7eb2-447e-ad3a-c55fe58378cb`
- **参数名**: `DoIPFurtherActionByteDirect`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **函数变体**:
- **描述**: Direct C Callback function to get the OEM specific Further Action Byte for the DoIP vehicle identification response/vehicle announcement. If the DoIPFurtherActionByteDirect parameter is present, the DoIP module will not use an RPort of ServiceInterface "CBGetFurtherActionByte" but will call the configured function.

##### 17. DoIPRoutingActivation

**容器属性**:

- **UUID**: `ECUC:8c07e2b0-4dd1-45fc-89ae-19a97da7e734`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPRoutingActivation`
- **多重性**: [0..255]

**容器描述**:

This container describes the routing activation possibilities by representing for each container a possible routing activation request message to the DoIP entity and the according references to the activated diagnostic messages.

###### 参数配置

此容器包含 **2** 个参数：

####### INTEGER 类型参数

######## 1. DoIPRoutingActivationNumber

- **UUID**: `ECUC:335e310b-8d47-48bf-b643-5c12468a5f01`
- **参数名**: `DoIPRoutingActivationNumber`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Identifies the Routing activation Number which is received for a DoIP routing activation request message.

####### BOOLEAN 类型参数

######## 1. DoIPRoutingActivationSecurityRequired

- **UUID**: `ECUC:d645dea9-213c-4ac7-9407-a6cc7586ae8f`
- **参数名**: `DoIPRoutingActivationSecurityRequired`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Indicates if a routing activation requires a secure TCP connection

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. DoIPTargetAddressRef

- **UUID**: `ECUC:ebc9f44b-f588-4a77-a371-08bfa7d33272`
- **引用名**: `DoIPTargetAddressRef`
- **引用类型**: REFERENCE
- **多重性**: [1..65535]
- **目标**: `DoIPTargetAddress`
- **完整路径**: `/AUTOSAR/EcucDefs/DoIP/DoIPConfigSet/DoIPInterface/DoIPConnections/DoIPTargetAddress`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to all DoIPTargetAddress which are activated on this Routing activation.

###### 配置容器

本模块包含 **2** 个配置容器：

####### 1. DoIPRoutingActivationAuthenticationCallback

**容器属性**:

- **UUID**: `ECUC:726377c7-0039-4edc-b57c-dd98bc5e99b7`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPRoutingActivationAuthenticationCallback`
- **多重性**: [0..1]

**容器描述**:

Container describes the Callbackfunction to call on a Routing Activation Request for Authentication. If this container is configured but the DoIPRoutingActivationAuthenticationFunc parameter is not present, the DoIP module will use an RPort of ServiceInterface <RoutingActivation>_RoutingActivation with the name "CB<RoutingActivation>RoutingActivation". <RoutingActivation> is the ShortName of the DoIPRoutingActiviation container.

######## 参数配置

此容器包含 **3** 个参数：

######### INTEGER 类型参数

########## 1. DoIPRoutingActivationAuthenticationReqLength

- **UUID**: `ECUC:2abdcf96-9b8e-4936-afc0-ede76b21f3a7`
- **参数名**: `DoIPRoutingActivationAuthenticationReqLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Describes the amount of bytes used to handle to the authentication function on routing activation. If 0 is configured as length the parameter AuthenticationReqData will not be handled to the API.

########## 2. DoIPRoutingActivationAuthenticationResLength

- **UUID**: `ECUC:45e1fc22-6491-40ed-87b8-7917007771a8`
- **参数名**: `DoIPRoutingActivationAuthenticationResLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Describes the amount of bytes used to read by the authentication function on routing activation. If 0 is configured as length the parameter AuthenticationResData will not be fetched via the API.

######### FUNCTION-NAME 类型参数

########## 1. DoIPRoutingActivationAuthenticationFunc

- **UUID**: `ECUC:05ef7a06-64da-467c-be24-d40bac66acc3`
- **参数名**: `DoIPRoutingActivationAuthenticationFunc`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **函数变体**:
- **描述**: Direct C Callback function to trigger the authentication function for routing activation. If the DoIPRoutingActivationAuthenticationFunc parameter is present, the DoIP module will not use an RPort of ServiceInterface <RoutingActivation>_RoutingActivation but call the configured function.

####### 2. DoIPRoutingActivationConfirmationCallback

**容器属性**:

- **UUID**: `ECUC:7e1d1ce3-eff6-43ab-a071-e6b83dfa4855`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPRoutingActivationConfirmationCallback`
- **多重性**: [0..1]

**容器描述**:

Container describes the Callbackfunction to call on a Routing Activation Request for Confirmation. If this container is configured but the DoIPRoutingActivationConfirmationFunc parameter is not present the DoIP module will use an RPort of ServiceInterface <RoutingActivation>_RoutingActivation with the name "CB<RoutingActivation>RoutingActivation". <RoutingActivation> is the ShortName of the DoIPRoutingActiviation container.

######## 参数配置

此容器包含 **3** 个参数：

######### INTEGER 类型参数

########## 1. DoIPRoutingActivationConfirmationReqLength

- **UUID**: `ECUC:b5b1030f-ad9f-4bbf-b2a0-9674bf5f20a7`
- **参数名**: `DoIPRoutingActivationConfirmationReqLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Describes the amount of bytes used to handle to the confirmation function on routing activation. If 0 is configured as length the parameter ConfirmedReqData will not be handled to the API.

########## 2. DoIPRoutingActivationConfirmationResLength

- **UUID**: `ECUC:701e1997-d200-4ee4-8372-e5eb0dc94c56`
- **参数名**: `DoIPRoutingActivationConfirmationResLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Describes the amount of bytes used to read by the confirmation function on routing activation. If 0 is configured as length the parameter ConfirmedResData will not be fetched via the API.

######### FUNCTION-NAME 类型参数

########## 1. DoIPRoutingActivationConfirmationFunc

- **UUID**: `ECUC:4630dc00-f4e8-4bf0-b18c-1a98a4f2f7c9`
- **参数名**: `DoIPRoutingActivationConfirmationFunc`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **函数变体**:
- **描述**: Direct C Callback function to trigger the confirmation function for routing activation. If the DoIPRoutingActivationConfirmationFunc parameter is present the DoIP module will not use an RPort of ServiceInterface <RoutingActivation>_RoutingActivation but call the configured function.

##### 18. DoIPRoutingActivationAuthenticationCallback

**容器属性**:

- **UUID**: `ECUC:726377c7-0039-4edc-b57c-dd98bc5e99b7`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPRoutingActivationAuthenticationCallback`
- **多重性**: [0..1]

**容器描述**:

Container describes the Callbackfunction to call on a Routing Activation Request for Authentication. If this container is configured but the DoIPRoutingActivationAuthenticationFunc parameter is not present, the DoIP module will use an RPort of ServiceInterface <RoutingActivation>_RoutingActivation with the name "CB<RoutingActivation>RoutingActivation". <RoutingActivation> is the ShortName of the DoIPRoutingActiviation container.

###### 参数配置

此容器包含 **3** 个参数：

####### INTEGER 类型参数

######## 1. DoIPRoutingActivationAuthenticationReqLength

- **UUID**: `ECUC:2abdcf96-9b8e-4936-afc0-ede76b21f3a7`
- **参数名**: `DoIPRoutingActivationAuthenticationReqLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Describes the amount of bytes used to handle to the authentication function on routing activation. If 0 is configured as length the parameter AuthenticationReqData will not be handled to the API.

######## 2. DoIPRoutingActivationAuthenticationResLength

- **UUID**: `ECUC:45e1fc22-6491-40ed-87b8-7917007771a8`
- **参数名**: `DoIPRoutingActivationAuthenticationResLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Describes the amount of bytes used to read by the authentication function on routing activation. If 0 is configured as length the parameter AuthenticationResData will not be fetched via the API.

####### FUNCTION-NAME 类型参数

######## 1. DoIPRoutingActivationAuthenticationFunc

- **UUID**: `ECUC:05ef7a06-64da-467c-be24-d40bac66acc3`
- **参数名**: `DoIPRoutingActivationAuthenticationFunc`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **函数变体**:
- **描述**: Direct C Callback function to trigger the authentication function for routing activation. If the DoIPRoutingActivationAuthenticationFunc parameter is present, the DoIP module will not use an RPort of ServiceInterface <RoutingActivation>_RoutingActivation but call the configured function.

##### 19. DoIPRoutingActivationConfirmationCallback

**容器属性**:

- **UUID**: `ECUC:7e1d1ce3-eff6-43ab-a071-e6b83dfa4855`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPRoutingActivationConfirmationCallback`
- **多重性**: [0..1]

**容器描述**:

Container describes the Callbackfunction to call on a Routing Activation Request for Confirmation. If this container is configured but the DoIPRoutingActivationConfirmationFunc parameter is not present the DoIP module will use an RPort of ServiceInterface <RoutingActivation>_RoutingActivation with the name "CB<RoutingActivation>RoutingActivation". <RoutingActivation> is the ShortName of the DoIPRoutingActiviation container.

###### 参数配置

此容器包含 **3** 个参数：

####### INTEGER 类型参数

######## 1. DoIPRoutingActivationConfirmationReqLength

- **UUID**: `ECUC:b5b1030f-ad9f-4bbf-b2a0-9674bf5f20a7`
- **参数名**: `DoIPRoutingActivationConfirmationReqLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Describes the amount of bytes used to handle to the confirmation function on routing activation. If 0 is configured as length the parameter ConfirmedReqData will not be handled to the API.

######## 2. DoIPRoutingActivationConfirmationResLength

- **UUID**: `ECUC:701e1997-d200-4ee4-8372-e5eb0dc94c56`
- **参数名**: `DoIPRoutingActivationConfirmationResLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Describes the amount of bytes used to read by the confirmation function on routing activation. If 0 is configured as length the parameter ConfirmedResData will not be fetched via the API.

####### FUNCTION-NAME 类型参数

######## 1. DoIPRoutingActivationConfirmationFunc

- **UUID**: `ECUC:4630dc00-f4e8-4bf0-b18c-1a98a4f2f7c9`
- **参数名**: `DoIPRoutingActivationConfirmationFunc`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **函数变体**:
- **描述**: Direct C Callback function to trigger the confirmation function for routing activation. If the DoIPRoutingActivationConfirmationFunc parameter is present the DoIP module will not use an RPort of ServiceInterface <RoutingActivation>_RoutingActivation but call the configured function.

##### 20. DoIPTester

**容器属性**:

- **UUID**: `ECUC:5ec2063c-2a23-4da2-be67-e7cd0a80ee93`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPTester`
- **多重性**: [0..255]

**容器描述**:

This container describes the properties of the possible connectable Tester for the DoIP entity.

###### 参数配置

此容器包含 **2** 个参数：

####### INTEGER 类型参数

######## 1. DoIPNumByteDiagAckNack

- **UUID**: `ECUC:2cdb3b03-189a-4c0d-847c-ec5cbe717265`
- **参数名**: `DoIPNumByteDiagAckNack`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Specifies the number of original Diagnostic request bytes the DoIP entity responses on a NACK of a diagnostic response message to the Tester.

######## 2. DoIPTesterSA

- **UUID**: `ECUC:44ccb383-1ad0-47a4-a3c4-5056f05a922d`
- **参数名**: `DoIPTesterSA`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Source Address of the Tester sent via routing activation or diagnostic message.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. DoIPRoutingActivationRef

- **UUID**: `ECUC:cc241bfa-5d3c-4e9b-b190-f764add15a77`
- **引用名**: `DoIPRoutingActivationRef`
- **引用类型**: REFERENCE
- **多重性**: [1..255]
- **目标**: `DoIPRoutingActivation`
- **完整路径**: `/AUTOSAR/EcucDefs/DoIP/DoIPConfigSet/DoIPInterface/DoIPRoutingActivation`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to a DoIPRoutingActivation describing the possible routing activations of the DoIPTester

##### 21. DoIPGeneral

**容器属性**:

- **UUID**: `a200892b-4c11-4c77-b67f-2952d1f89fa8`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPGeneral`
- **多重性**: [1..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container specifies the general configuration parameters of the DoIP module.

###### 参数配置

此容器包含 **21** 个参数：

####### INTEGER 类型参数

######## 1. DoIPGIDInvalidityPattern

- **UUID**: `bdf5e8e8-4413-464e-9cb0-8de8ccb334ca`
- **参数名**: `DoIPGIDInvalidityPattern`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies the Byte pattern that is used for response messages if no valid GID could be retrieved.

######## 2. DoIPMaxRequestBytes

- **UUID**: `1dc915a9-732a-43a8-aef7-863930443e13`
- **参数名**: `DoIPMaxRequestBytes`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..18446744073709551615]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies the maximum allowed bytes of a DoIP message request without the DoIP header.

######## 3. DoIPMaxTesterConnections

- **UUID**: `07f5b919-fdf8-42f7-adf5-9bb3adaf5f10`
- **参数名**: `DoIPMaxTesterConnections`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Maximum ammount of tester connections that shall be maintained at one time before alive check is performed.

######## 4. DoIPVehicleAnnouncementRepetition

- **UUID**: `67c2379d-043a-47c4-85ef-fed9b25185e6`
- **参数名**: `DoIPVehicleAnnouncementRepetition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Amount of repetitions of the vehicle announcement message on IP address assignment. Represents parameter A_DoIP_Annunce_Num of ISO 13400-2:2012

######## 5. DoIPVinInvalidityPattern

- **UUID**: `03d1fd23-6844-4ce8-a957-a235ad2196c0`
- **参数名**: `DoIPVinInvalidityPattern`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies the Byte pattern that is used for response messages if no valid VIN could be retrieved.

####### BOOLEAN 类型参数

######## 1. DoIPDevelopmentErrorDetect

- **UUID**: `c28940cb-abef-45c2-b81b-4acc74805f22`
- **参数名**: `DoIPDevelopmentErrorDetect`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Pre-processor switch for enabling development error detection support.

######## 2. DoIPDhcpOptionVinUse

- **UUID**: `34eca337-52b5-4f79-b980-6dfd71924ce3`
- **参数名**: `DoIPDhcpOptionVinUse`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: If DoIPDhcpOptionVinUse is set to true the DoIP module will add the VIN to the Dhcp host name if no valid Dhcp host name is already set.

######## 3. DoIPEntityStatusMaxByteFieldUse

- **UUID**: `a3eae043-90c1-4201-99b0-544baa6daa37`
- **参数名**: `DoIPEntityStatusMaxByteFieldUse`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter is used to distinguish the optional support of the Max data size element of a diagnostic entity status response.

######## 4. DoIPUseEIDasGID

- **UUID**: `bad7e06b-1634-436d-8300-99dff78ddc70`
- **参数名**: `DoIPUseEIDasGID`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies if the DoIP entity shall use its EID if it is the Master for vehicle identification gid on the vehicle identification/vehicle announcement.

######## 5. DoIPUseMacAddressForIdentification

- **UUID**: `e4ac2e8b-253b-4854-a364-afd28ec5978d`
- **参数名**: `DoIPUseMacAddressForIdentification`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Provided the information if a configured EID at vehicle identification response/vehicle announment is used or the MAC address.

######## 6. DoIPUseVehicleIdentificationSyncStatus

- **UUID**: `5ea10f94-5872-4c20-8f2f-c7075d2f2a44`
- **参数名**: `DoIPUseVehicleIdentificationSyncStatus`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines if the optional VIN/GID synchronization status is used additionally in the vehicle identification/announcement.

######## 7. DoIPVersionInfoApi

- **UUID**: `0df20c8e-36cd-42b1-ba65-bb9bdba72b35`
- **参数名**: `DoIPVersionInfoApi`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Activates the DoIP_GetVersionInfo() API.

######## 8. DoIPVinGidMaster

- **UUID**: `20d5dfb6-e29c-4cc9-a9ff-68bb282ac904`
- **参数名**: `DoIPVinGidMaster`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies if the DoIP entity is the Vehicle identification Master for the GID (Group ID).

####### FLOAT 类型参数

######## 1. DoIPAliveCheckResponseTimeout

- **UUID**: `793e123f-c484-4b36-bbc1-5bf785f30557`
- **参数名**: `DoIPAliveCheckResponseTimeout`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0..Inf]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Timeout  in [s] for waiting for a response to an Alive Check request before the connection is considered to be disconnected. Represents parameter T_TCP_AliveCheck of ISO 13400-2:2012.

######## 2. DoIPGeneralInactivityTime

- **UUID**: `4f72ae2d-e209-4d55-80e4-1b1a184fdf7f`
- **参数名**: `DoIPGeneralInactivityTime`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0..Inf]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Timeout in [s] for maximum inactivity of a TCP socket connection before the DoIP module will close the according socket connection. Represents parameter T_TCP_General_Inactivity of ISO 13400-2:2012

######## 3. DoIPInitialInactivityTime

- **UUID**: `6cee6e0a-89a7-432d-a52d-02778cb163b1`
- **参数名**: `DoIPInitialInactivityTime`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0..Inf]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Timeout in [s] used for initial inactivity of a connected TCP socket connection directly after socket connection. Represents parameter T_TCP_Initial_Inactivity of ISO 13400-2:2012

######## 4. DoIPInitialVehicleAnnouncementTime

- **UUID**: `a7f39a11-cdac-4b86-bb77-a4ff32f15a50`
- **参数名**: `DoIPInitialVehicleAnnouncementTime`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0..Inf]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Time to wait in [s] for sending first vehicle anouncement message after IP address assignment. Represents parameter A_DoIP_Announce_Wait of ISO 13400-2:2012

######## 5. DoIPMainFunctionPeriod

- **UUID**: `45805d43-26d8-499f-a62b-aac4ff4fa6ef`
- **参数名**: `DoIPMainFunctionPeriod`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0..Inf]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Determines the frequency at which the DoIP_MainFunction() is called in [s].

######## 6. DoIPVehicleAnnouncementInterval

- **UUID**: `7f8a0d21-9ee1-4c44-ad90-69c57b6bca35`
- **参数名**: `DoIPVehicleAnnouncementInterval`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0..Inf]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Time to wait in [s] for sending subsequent vehicle anouncement messages. Represents parameter A_DoIP_Announce_Interval of ISO 13400-2:2012

####### STRING 类型参数

######## 1. DoIPHeaderFileInclusion

- **UUID**: `be23b072-c4b1-42f1-9a54-8724b30ad635`
- **参数名**: `DoIPHeaderFileInclusion`
- **数据类型**: STRING
- **多重性**: [0..infinite]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of the header file(s) to be included by the DoIP module containing the used C-callback declarations.

####### ENUMERATION 类型参数

######## 1. DoIPNodeType

- **UUID**: `61c81de9-2eba-4604-b9d9-d1ac5b7f839b`
- **参数名**: `DoIPNodeType`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `DOIP_GATEWAY` (来源: AUTOSAR_ECUC)
  - `DOIP_NODE` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Describes the Type of the DoIP node.

###### 配置容器

本模块包含 **3** 个配置容器：

####### 1. DoIPGetGid

**容器属性**:

- **UUID**: `404eacad-16bf-4d40-8cbe-c29de0edbdd5`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPGetGid`
- **多重性**: [0..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container describes the Callbackfunction to get the GID.

######## 参数配置

此容器包含 **1** 个参数：

######### FUNCTION-NAME 类型参数

########## 1. DoIPGetGID

- **UUID**: `345849a7-a78d-4180-bf69-3515f9cc891a`
- **参数名**: `DoIPGetGID`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Direct C Callback function to get the GID of the DoIP entity. If the DoIPGetGID parameter is present, the DoIP module will not use an RPort of ServiceInterface CallbackGetGID but call the configured function.

####### 2. DoIPPowerModeCallback

**容器属性**:

- **UUID**: `6e539553-d1c8-43ab-b1a3-203d615f12f9`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPPowerModeCallback`
- **多重性**: [1..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container describes the Callbackfunction to get the Power Mode. This container shall always be present.

######## 参数配置

此容器包含 **1** 个参数：

######### FUNCTION-NAME 类型参数

########## 1. DoIPPowerMode

- **UUID**: `94c460ea-9181-4043-8dab-35fc02b0c798`
- **参数名**: `DoIPPowerMode`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Direct C Callback function to get the Power Mode of the DoIP entity. If the DoIPPowerMode parameter is present, the DoIP module will not use an RPort of ServiceInterface CallbackGetPowerMode but will call the configured function.

####### 3. DoIPTriggerGidSynchronization

**容器属性**:

- **UUID**: `6b8b0f97-aa8a-42a5-987f-b025ebb6c347`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPTriggerGidSynchronization`
- **多重性**: [0..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container describes the Callbackfunction to trigger the GID synchronisation.

######## 参数配置

此容器包含 **1** 个参数：

######### FUNCTION-NAME 类型参数

########## 1. DoIPTriggerGIDSynchronzation

- **UUID**: `bec04140-0464-4b01-8f65-e8c59aa1b004`
- **参数名**: `DoIPTriggerGIDSynchronzation`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Direct C Callback function to trigger the synchronization of the GID. If the DoIPTriggerGIDSynchronzation parameter is present, the DoIP module will not use an RPort of ServiceInterface CallbackTriggerGIDSynchronization but call the configured function.

##### 22. DoIPGetGid

**容器属性**:

- **UUID**: `404eacad-16bf-4d40-8cbe-c29de0edbdd5`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPGetGid`
- **多重性**: [0..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container describes the Callbackfunction to get the GID.

###### 参数配置

此容器包含 **1** 个参数：

####### FUNCTION-NAME 类型参数

######## 1. DoIPGetGID

- **UUID**: `345849a7-a78d-4180-bf69-3515f9cc891a`
- **参数名**: `DoIPGetGID`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Direct C Callback function to get the GID of the DoIP entity. If the DoIPGetGID parameter is present, the DoIP module will not use an RPort of ServiceInterface CallbackGetGID but call the configured function.

##### 23. DoIPPowerModeCallback

**容器属性**:

- **UUID**: `6e539553-d1c8-43ab-b1a3-203d615f12f9`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPPowerModeCallback`
- **多重性**: [1..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container describes the Callbackfunction to get the Power Mode. This container shall always be present.

###### 参数配置

此容器包含 **1** 个参数：

####### FUNCTION-NAME 类型参数

######## 1. DoIPPowerMode

- **UUID**: `94c460ea-9181-4043-8dab-35fc02b0c798`
- **参数名**: `DoIPPowerMode`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Direct C Callback function to get the Power Mode of the DoIP entity. If the DoIPPowerMode parameter is present, the DoIP module will not use an RPort of ServiceInterface CallbackGetPowerMode but will call the configured function.

##### 24. DoIPTriggerGidSynchronization

**容器属性**:

- **UUID**: `6b8b0f97-aa8a-42a5-987f-b025ebb6c347`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPTriggerGidSynchronization`
- **多重性**: [0..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container describes the Callbackfunction to trigger the GID synchronisation.

###### 参数配置

此容器包含 **1** 个参数：

####### FUNCTION-NAME 类型参数

######## 1. DoIPTriggerGIDSynchronzation

- **UUID**: `bec04140-0464-4b01-8f65-e8c59aa1b004`
- **参数名**: `DoIPTriggerGIDSynchronzation`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Direct C Callback function to trigger the synchronization of the GID. If the DoIPTriggerGIDSynchronzation parameter is present, the DoIP module will not use an RPort of ServiceInterface CallbackTriggerGIDSynchronization but call the configured function.

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

1. **DoIP**
