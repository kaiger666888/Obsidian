# DoIP - 完整配置文档

*此文档由ARXML文件自动生成，采用层次化结构展示*

**生成时间**: 2025-06-16 14:51:42

## 📑 目录

- [📄 文件信息](#-文件信息)
- [🔧 模块定义](#-模块定义)
  - [DoIP](#doip)
- [📦 包结构](#-包结构)

## 📄 文件信息

### Schema信息
- **Schema位置**: `http://autosar.org/schema/r4.0 AUTOSAR_4-0-3.xsd`
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

本模块包含 **20** 个配置容器：

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

本模块包含 **15** 个配置容器：

####### 1. DoIPChannel

**容器属性**:

- **UUID**: `eef69e41-b1a0-4b5e-8468-47d0f59a4b79`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPChannel`
- **多重性**: [1..65536]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

Configuration of one DoIPChannel.

######## 引用关系

此容器包含 **2** 个引用：

######### REFERENCE 类型引用

########## 1. DoIPChannelSARef

- **UUID**: `86af5955-9e74-4620-b55f-38d4d9ca71ae`
- **引用名**: `DoIPChannelSARef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `DoIPTester`
- **完整路径**: `/AUTOSAR/EcucDefs/DoIP/DoIPConfigSet/DoIPTester`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the DoIPTester.

########## 2. DoIPChannelTARef

- **UUID**: `a8d6656f-f0b3-49c5-ab9f-159c3bf4c02a`
- **引用名**: `DoIPChannelTARef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `DoIPTargetAddress`
- **完整路径**: `/AUTOSAR/EcucDefs/DoIP/DoIPConfigSet/DoIPConnections/DoIPTargetAddress`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the target address.

######## 配置容器

本模块包含 **2** 个配置容器：

######### 1. DoIPPduRRxPdu

**容器属性**:

- **UUID**: `8e8e65a8-1939-406e-aa0b-6dfb219b42ca`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPPduRRxPdu`
- **多重性**: [1..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container contains the Rx Pdus to connect with the Rx Pdus of the PduR.

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. DoIPPduRRxPduId

- **UUID**: `d1ed6fd3-3843-46d7-ab9f-fd58ab8b9562`
- **参数名**: `DoIPPduRRxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The DoIPPduRRxPduId is required by the API call DoIP_CancelReceive.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. DoIPPduRRxPduRef

- **UUID**: `b7bf4060-ce84-436f-a701-33b9768b0a87`
- **引用名**: `DoIPPduRRxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the "global" Pdu structure to allow harmonization of handle IDs in the COM-Stack.

######### 2. DoIPPduRTxPdu

**容器属性**:

- **UUID**: `6f9c6349-bdd5-4bb9-8280-b3a7d3cf9f6b`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPPduRTxPdu`
- **多重性**: [1..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container contains the Tx Pdus to connect with the Tx Pdus of the PduR.

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. DoIPPduRTxPduId

- **UUID**: `4eee96d2-a3a6-43de-8ca6-849192414879`
- **参数名**: `DoIPPduRTxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The DoIPPduRTxPduId is required by DoIP_Transmit and DoIP_CancelTransmit.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. DoIPPduRTxPduRef

- **UUID**: `6119b2e5-74a7-46f1-a07a-33d48cd9776b`
- **引用名**: `DoIPPduRTxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the "global" Pdu structure to allow harmonization of handle IDs in the COM-Stack.

####### 2. DoIPPduRRxPdu

**容器属性**:

- **UUID**: `8e8e65a8-1939-406e-aa0b-6dfb219b42ca`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPPduRRxPdu`
- **多重性**: [1..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container contains the Rx Pdus to connect with the Rx Pdus of the PduR.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. DoIPPduRRxPduId

- **UUID**: `d1ed6fd3-3843-46d7-ab9f-fd58ab8b9562`
- **参数名**: `DoIPPduRRxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The DoIPPduRRxPduId is required by the API call DoIP_CancelReceive.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. DoIPPduRRxPduRef

- **UUID**: `b7bf4060-ce84-436f-a701-33b9768b0a87`
- **引用名**: `DoIPPduRRxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the "global" Pdu structure to allow harmonization of handle IDs in the COM-Stack.

####### 3. DoIPPduRTxPdu

**容器属性**:

- **UUID**: `6f9c6349-bdd5-4bb9-8280-b3a7d3cf9f6b`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPPduRTxPdu`
- **多重性**: [1..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container contains the Tx Pdus to connect with the Tx Pdus of the PduR.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. DoIPPduRTxPduId

- **UUID**: `4eee96d2-a3a6-43de-8ca6-849192414879`
- **参数名**: `DoIPPduRTxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The DoIPPduRTxPduId is required by DoIP_Transmit and DoIP_CancelTransmit.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. DoIPPduRTxPduRef

- **UUID**: `6119b2e5-74a7-46f1-a07a-33d48cd9776b`
- **引用名**: `DoIPPduRTxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the "global" Pdu structure to allow harmonization of handle IDs in the COM-Stack.

####### 4. DoIPConnections

**容器属性**:

- **UUID**: `a8e99df5-fae8-4860-84b7-5484bc3aa5ea`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPConnections`
- **多重性**: [1..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

Container contains all lower layer connection specific information, i.e. the single Pdu References and Handle IDs to the SoAd.

######## 配置容器

本模块包含 **7** 个配置容器：

######### 1. DoIPTargetAddress

**容器属性**:

- **UUID**: `738662ff-bcd1-4bf9-b33c-a99388e763c4`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPTargetAddress`
- **多重性**: [1..255]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container describes a possible TargetAddress that is supported by DoIP.

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. DoIPTargetAddressValue

- **UUID**: `d166da8b-269c-43a2-9cc1-28897951668b`
- **参数名**: `DoIPTargetAddressValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Valid Target Address of a DoIP target address.

######### 2. DoIPTcpConnection

**容器属性**:

- **UUID**: `1d86f9fa-e08b-434e-8c6a-173985feb32a`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPTcpConnection`
- **多重性**: [1..255]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

Each container describes a tcp connection to the lower layer SoAd module.

########## 配置容器

本模块包含 **2** 个配置容器：

########### 1. DoIPSoAdRxPdu

**容器属性**:

- **UUID**: `b780b617-6160-47fb-922d-2720b32889b0`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPSoAdRxPdu`
- **多重性**: [1..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container contains the Rx Pdus received by DoIP

############ 参数配置

此容器包含 **1** 个参数：

############# INTEGER 类型参数

############## 1. DoIPSoAdRxPduId

- **UUID**: `dfbc0748-ee25-4b04-98ca-27c4b9c26a48`
- **参数名**: `DoIPSoAdRxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The DoIPSoAdRxPduId is required by the API call DoIP_SoAdTpRxIndication to receive I-PDUs from the SoAd.

############ 引用关系

此容器包含 **1** 个引用：

############# REFERENCE 类型引用

############## 1. DoIPSoAdRxPduRef

- **UUID**: `0693db04-cd76-4e47-ab9f-49b3d338cefc`
- **引用名**: `DoIPSoAdRxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the "global" Pdu structure to allow harmonization of handle IDs in the COM-Stack.

########### 2. DoIPSoAdTxPdu

**容器属性**:

- **UUID**: `f764f413-32d6-415e-bf20-06b1f33ac811`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPSoAdTxPdu`
- **多重性**: [1..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container describes the TxPdu sent via the SoAd

############ 参数配置

此容器包含 **1** 个参数：

############# INTEGER 类型参数

############## 1. DoIPSoAdTxPduId

- **UUID**: `0bb68c55-8e46-4757-a573-2f08d3e45943`
- **参数名**: `DoIPSoAdTxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The DoIPSoAdTxPduId is required by the API call DoIP_SoAdTpTxConfirmation that is called by the SoAd to confirm that the IPdu has been transmitted successfully.

############ 引用关系

此容器包含 **1** 个引用：

############# REFERENCE 类型引用

############## 1. DoIPSoAdTxPduRef

- **UUID**: `3c473230-72c7-48c8-b783-565ea21ada9b`
- **引用名**: `DoIPSoAdTxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the "global" Pdu structure to allow harmonization of handle IDs in the COM-Stack.

######### 3. DoIPSoAdRxPdu

**容器属性**:

- **UUID**: `b780b617-6160-47fb-922d-2720b32889b0`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPSoAdRxPdu`
- **多重性**: [1..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container contains the Rx Pdus received by DoIP

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. DoIPSoAdRxPduId

- **UUID**: `dfbc0748-ee25-4b04-98ca-27c4b9c26a48`
- **参数名**: `DoIPSoAdRxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The DoIPSoAdRxPduId is required by the API call DoIP_SoAdTpRxIndication to receive I-PDUs from the SoAd.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. DoIPSoAdRxPduRef

- **UUID**: `0693db04-cd76-4e47-ab9f-49b3d338cefc`
- **引用名**: `DoIPSoAdRxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the "global" Pdu structure to allow harmonization of handle IDs in the COM-Stack.

######### 4. DoIPSoAdTxPdu

**容器属性**:

- **UUID**: `f764f413-32d6-415e-bf20-06b1f33ac811`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPSoAdTxPdu`
- **多重性**: [1..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container describes the TxPdu sent via the SoAd

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. DoIPSoAdTxPduId

- **UUID**: `0bb68c55-8e46-4757-a573-2f08d3e45943`
- **参数名**: `DoIPSoAdTxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The DoIPSoAdTxPduId is required by the API call DoIP_SoAdTpTxConfirmation that is called by the SoAd to confirm that the IPdu has been transmitted successfully.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. DoIPSoAdTxPduRef

- **UUID**: `3c473230-72c7-48c8-b783-565ea21ada9b`
- **引用名**: `DoIPSoAdTxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the "global" Pdu structure to allow harmonization of handle IDs in the COM-Stack.

######### 5. DoIPUdpConnection

**容器属性**:

- **UUID**: `d40873c8-93f6-4a30-8187-2f5b9175faac`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPUdpConnection`
- **多重性**: [1..255]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This Container describes the udp connection to the lower layer SoAd module.

########## 配置容器

本模块包含 **2** 个配置容器：

########### 1. DoIPSoAdRxPdu

**容器属性**:

- **UUID**: `2000490b-fc46-4b42-9762-e9bd84105208`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPSoAdRxPdu`
- **多重性**: [1..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container contains the Rx Pdus received by DoIP

############ 参数配置

此容器包含 **1** 个参数：

############# INTEGER 类型参数

############## 1. DoIPSoAdRxPduId

- **UUID**: `d6d9639f-165e-4837-95e1-18a976bc52f6`
- **参数名**: `DoIPSoAdRxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The DoIPSoAdRxPduId is required by the API call DoIP_SoAdTpRxIndication to receive I-PDUs from the SoAd.

############ 引用关系

此容器包含 **1** 个引用：

############# REFERENCE 类型引用

############## 1. DoIPSoAdRxPduRef

- **UUID**: `77c3f3d4-c8ba-4ab6-b72e-32d5d68bbff1`
- **引用名**: `DoIPSoAdRxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the "global" Pdu structure to allow harmonization of handle IDs in the COM-Stack.

########### 2. DoIPSoAdTxPdu

**容器属性**:

- **UUID**: `60b4dec8-ce99-4a24-8484-4d6853b2fe60`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPSoAdTxPdu`
- **多重性**: [1..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container describes the TxPdu sent via the SoAd

############ 参数配置

此容器包含 **1** 个参数：

############# INTEGER 类型参数

############## 1. DoIPSoAdTxPduId

- **UUID**: `ae89ffc6-eb59-420b-bbe8-31d4006bc7ad`
- **参数名**: `DoIPSoAdTxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The DoIPSoAdTxPduId is required by the API call DoIP_SoAdTpTxConfirmation that is called by the SoAd to confirm that the IPdu has been transmitted successfully.

############ 引用关系

此容器包含 **1** 个引用：

############# REFERENCE 类型引用

############## 1. DoIPSoAdTxPduRef

- **UUID**: `c42b04dc-ce57-4b69-8b1d-953f583173ea`
- **引用名**: `DoIPSoAdTxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the "global" Pdu structure to allow harmonization of handle IDs in the COM-Stack.

######### 6. DoIPSoAdRxPdu

**容器属性**:

- **UUID**: `2000490b-fc46-4b42-9762-e9bd84105208`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPSoAdRxPdu`
- **多重性**: [1..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container contains the Rx Pdus received by DoIP

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. DoIPSoAdRxPduId

- **UUID**: `d6d9639f-165e-4837-95e1-18a976bc52f6`
- **参数名**: `DoIPSoAdRxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The DoIPSoAdRxPduId is required by the API call DoIP_SoAdTpRxIndication to receive I-PDUs from the SoAd.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. DoIPSoAdRxPduRef

- **UUID**: `77c3f3d4-c8ba-4ab6-b72e-32d5d68bbff1`
- **引用名**: `DoIPSoAdRxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the "global" Pdu structure to allow harmonization of handle IDs in the COM-Stack.

######### 7. DoIPSoAdTxPdu

**容器属性**:

- **UUID**: `60b4dec8-ce99-4a24-8484-4d6853b2fe60`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPSoAdTxPdu`
- **多重性**: [1..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container describes the TxPdu sent via the SoAd

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. DoIPSoAdTxPduId

- **UUID**: `ae89ffc6-eb59-420b-bbe8-31d4006bc7ad`
- **参数名**: `DoIPSoAdTxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The DoIPSoAdTxPduId is required by the API call DoIP_SoAdTpTxConfirmation that is called by the SoAd to confirm that the IPdu has been transmitted successfully.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. DoIPSoAdTxPduRef

- **UUID**: `c42b04dc-ce57-4b69-8b1d-953f583173ea`
- **引用名**: `DoIPSoAdTxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the "global" Pdu structure to allow harmonization of handle IDs in the COM-Stack.

####### 5. DoIPTargetAddress

**容器属性**:

- **UUID**: `738662ff-bcd1-4bf9-b33c-a99388e763c4`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPTargetAddress`
- **多重性**: [1..255]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container describes a possible TargetAddress that is supported by DoIP.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. DoIPTargetAddressValue

- **UUID**: `d166da8b-269c-43a2-9cc1-28897951668b`
- **参数名**: `DoIPTargetAddressValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Valid Target Address of a DoIP target address.

####### 6. DoIPTcpConnection

**容器属性**:

- **UUID**: `1d86f9fa-e08b-434e-8c6a-173985feb32a`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPTcpConnection`
- **多重性**: [1..255]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

Each container describes a tcp connection to the lower layer SoAd module.

######## 配置容器

本模块包含 **2** 个配置容器：

######### 1. DoIPSoAdRxPdu

**容器属性**:

- **UUID**: `b780b617-6160-47fb-922d-2720b32889b0`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPSoAdRxPdu`
- **多重性**: [1..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container contains the Rx Pdus received by DoIP

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. DoIPSoAdRxPduId

- **UUID**: `dfbc0748-ee25-4b04-98ca-27c4b9c26a48`
- **参数名**: `DoIPSoAdRxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The DoIPSoAdRxPduId is required by the API call DoIP_SoAdTpRxIndication to receive I-PDUs from the SoAd.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. DoIPSoAdRxPduRef

- **UUID**: `0693db04-cd76-4e47-ab9f-49b3d338cefc`
- **引用名**: `DoIPSoAdRxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the "global" Pdu structure to allow harmonization of handle IDs in the COM-Stack.

######### 2. DoIPSoAdTxPdu

**容器属性**:

- **UUID**: `f764f413-32d6-415e-bf20-06b1f33ac811`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPSoAdTxPdu`
- **多重性**: [1..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container describes the TxPdu sent via the SoAd

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. DoIPSoAdTxPduId

- **UUID**: `0bb68c55-8e46-4757-a573-2f08d3e45943`
- **参数名**: `DoIPSoAdTxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The DoIPSoAdTxPduId is required by the API call DoIP_SoAdTpTxConfirmation that is called by the SoAd to confirm that the IPdu has been transmitted successfully.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. DoIPSoAdTxPduRef

- **UUID**: `3c473230-72c7-48c8-b783-565ea21ada9b`
- **引用名**: `DoIPSoAdTxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the "global" Pdu structure to allow harmonization of handle IDs in the COM-Stack.

####### 7. DoIPSoAdRxPdu

**容器属性**:

- **UUID**: `b780b617-6160-47fb-922d-2720b32889b0`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPSoAdRxPdu`
- **多重性**: [1..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container contains the Rx Pdus received by DoIP

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. DoIPSoAdRxPduId

- **UUID**: `dfbc0748-ee25-4b04-98ca-27c4b9c26a48`
- **参数名**: `DoIPSoAdRxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The DoIPSoAdRxPduId is required by the API call DoIP_SoAdTpRxIndication to receive I-PDUs from the SoAd.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. DoIPSoAdRxPduRef

- **UUID**: `0693db04-cd76-4e47-ab9f-49b3d338cefc`
- **引用名**: `DoIPSoAdRxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the "global" Pdu structure to allow harmonization of handle IDs in the COM-Stack.

####### 8. DoIPSoAdTxPdu

**容器属性**:

- **UUID**: `f764f413-32d6-415e-bf20-06b1f33ac811`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPSoAdTxPdu`
- **多重性**: [1..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container describes the TxPdu sent via the SoAd

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. DoIPSoAdTxPduId

- **UUID**: `0bb68c55-8e46-4757-a573-2f08d3e45943`
- **参数名**: `DoIPSoAdTxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The DoIPSoAdTxPduId is required by the API call DoIP_SoAdTpTxConfirmation that is called by the SoAd to confirm that the IPdu has been transmitted successfully.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. DoIPSoAdTxPduRef

- **UUID**: `3c473230-72c7-48c8-b783-565ea21ada9b`
- **引用名**: `DoIPSoAdTxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the "global" Pdu structure to allow harmonization of handle IDs in the COM-Stack.

####### 9. DoIPUdpConnection

**容器属性**:

- **UUID**: `d40873c8-93f6-4a30-8187-2f5b9175faac`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPUdpConnection`
- **多重性**: [1..255]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This Container describes the udp connection to the lower layer SoAd module.

######## 配置容器

本模块包含 **2** 个配置容器：

######### 1. DoIPSoAdRxPdu

**容器属性**:

- **UUID**: `2000490b-fc46-4b42-9762-e9bd84105208`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPSoAdRxPdu`
- **多重性**: [1..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container contains the Rx Pdus received by DoIP

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. DoIPSoAdRxPduId

- **UUID**: `d6d9639f-165e-4837-95e1-18a976bc52f6`
- **参数名**: `DoIPSoAdRxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The DoIPSoAdRxPduId is required by the API call DoIP_SoAdTpRxIndication to receive I-PDUs from the SoAd.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. DoIPSoAdRxPduRef

- **UUID**: `77c3f3d4-c8ba-4ab6-b72e-32d5d68bbff1`
- **引用名**: `DoIPSoAdRxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the "global" Pdu structure to allow harmonization of handle IDs in the COM-Stack.

######### 2. DoIPSoAdTxPdu

**容器属性**:

- **UUID**: `60b4dec8-ce99-4a24-8484-4d6853b2fe60`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPSoAdTxPdu`
- **多重性**: [1..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container describes the TxPdu sent via the SoAd

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. DoIPSoAdTxPduId

- **UUID**: `ae89ffc6-eb59-420b-bbe8-31d4006bc7ad`
- **参数名**: `DoIPSoAdTxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The DoIPSoAdTxPduId is required by the API call DoIP_SoAdTpTxConfirmation that is called by the SoAd to confirm that the IPdu has been transmitted successfully.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. DoIPSoAdTxPduRef

- **UUID**: `c42b04dc-ce57-4b69-8b1d-953f583173ea`
- **引用名**: `DoIPSoAdTxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the "global" Pdu structure to allow harmonization of handle IDs in the COM-Stack.

####### 10. DoIPSoAdRxPdu

**容器属性**:

- **UUID**: `2000490b-fc46-4b42-9762-e9bd84105208`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPSoAdRxPdu`
- **多重性**: [1..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container contains the Rx Pdus received by DoIP

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. DoIPSoAdRxPduId

- **UUID**: `d6d9639f-165e-4837-95e1-18a976bc52f6`
- **参数名**: `DoIPSoAdRxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The DoIPSoAdRxPduId is required by the API call DoIP_SoAdTpRxIndication to receive I-PDUs from the SoAd.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. DoIPSoAdRxPduRef

- **UUID**: `77c3f3d4-c8ba-4ab6-b72e-32d5d68bbff1`
- **引用名**: `DoIPSoAdRxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the "global" Pdu structure to allow harmonization of handle IDs in the COM-Stack.

####### 11. DoIPSoAdTxPdu

**容器属性**:

- **UUID**: `60b4dec8-ce99-4a24-8484-4d6853b2fe60`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPSoAdTxPdu`
- **多重性**: [1..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container describes the TxPdu sent via the SoAd

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. DoIPSoAdTxPduId

- **UUID**: `ae89ffc6-eb59-420b-bbe8-31d4006bc7ad`
- **参数名**: `DoIPSoAdTxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The DoIPSoAdTxPduId is required by the API call DoIP_SoAdTpTxConfirmation that is called by the SoAd to confirm that the IPdu has been transmitted successfully.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. DoIPSoAdTxPduRef

- **UUID**: `c42b04dc-ce57-4b69-8b1d-953f583173ea`
- **引用名**: `DoIPSoAdTxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the "global" Pdu structure to allow harmonization of handle IDs in the COM-Stack.

####### 12. DoIPRoutingActivation

**容器属性**:

- **UUID**: `a3f863df-8d3a-424e-b358-5af96d6d2a19`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPRoutingActivation`
- **多重性**: [0..255]
- **构建后可变**: true
- **多配置容器**: false

**容器描述**:

This container describes the routing activation possibilities by representing for each container a possible routing activation request message to the DoIP entity and the according references to the activated diagnostic messages.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. DoIPRoutingActivationNumber

- **UUID**: `3e3fed60-6259-403d-80ec-5990e4220de7`
- **参数名**: `DoIPRoutingActivationNumber`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Identifies the Routing activation Number which is received for a DoIP routing activation request message.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. DoIPTargetAddressRef

- **UUID**: `56f74807-4daf-4b15-86f7-3ed91dcb50ff`
- **引用名**: `DoIPTargetAddressRef`
- **引用类型**: REFERENCE
- **多重性**: [1..255]
- **目标**: `DoIPTargetAddress`
- **完整路径**: `/AUTOSAR/EcucDefs/DoIP/DoIPConfigSet/DoIPConnections/DoIPTargetAddress`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to all DoIPTargetAddress which are activated on this Routing activation.

######## 配置容器

本模块包含 **2** 个配置容器：

######### 1. DoIPRoutingActivationAuthenticationCallback

**容器属性**:

- **UUID**: `71d44007-a9ff-405c-98cd-b3d2fe7e1990`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPRoutingActivationAuthenticationCallback`
- **多重性**: [0..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

Container describes the Callbackfunction to call on a Routing Activation Request for Authentication. If this container is configured but the DoIPRoutingAcivationAuthenticationFunc parameter is not present, the DoIP module will use an RPort of ServiceInterface <RoutingActivation>_RoutingActivation with the name "CB<RoutingActivation>RoutingActivation". <RoutingActivation> is the ShortName of the DoIPRoutingActiviation container.

########## 参数配置

此容器包含 **3** 个参数：

########### INTEGER 类型参数

############ 1. DoIPRoutingActivationAuthenticationReqLength

- **UUID**: `10ee88e3-2369-4e42-88ce-47ea6b95cd45`
- **参数名**: `DoIPRoutingActivationAuthenticationReqLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Describes the amount of bytes used to handle to the authentication function on routing activation. If 0 is configured as length the parameter AuthenticationReqData will not be handled to the API.

############ 2. DoIPRoutingActivationAuthenticationResLength

- **UUID**: `0619576e-3da9-45d0-a851-90c63d51cb77`
- **参数名**: `DoIPRoutingActivationAuthenticationResLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Describes the amount of bytes used to read by the authentication function on routing activation. If 0 is configured as length the parameter AuthenticationResData will not be fetched via the API.

########### FUNCTION-NAME 类型参数

############ 1. DoIPRoutingAcivationAuthenticationFunc

- **UUID**: `c9c52180-7e06-4986-b8b6-175f2889e5e3`
- **参数名**: `DoIPRoutingAcivationAuthenticationFunc`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Direct C Callback function to trigger the authentication function for routing activation. If the DoIPRoutingAcivationAuthenticationFunc parameter is present, the DoIP module will not use an RPort of ServiceInterface <RoutingActivation>_RoutingActivation but call the configured function.

######### 2. DoIPRoutingActivationConfirmationCallback

**容器属性**:

- **UUID**: `6f8e5715-be9d-448e-a87b-c0eef99ce37b`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPRoutingActivationConfirmationCallback`
- **多重性**: [0..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

Container describes the Callbackfunction to call on a Routing Activation Request for Confirmation. If this container is configured but the DoIPRoutingAcivationConfirmationFunc parameter is not present the DoIP module will use an RPort of ServiceInterface <RoutingActivation>_RoutingActivation with the name "CB<RoutingActivation>RoutingActivation". <RoutingActivation> is the ShortName of the DoIPRoutingActiviation container.

########## 参数配置

此容器包含 **3** 个参数：

########### INTEGER 类型参数

############ 1. DoIPRoutingActivationConfirmationReqLength

- **UUID**: `6515852f-3fd6-44ba-b796-81511c0bb0c9`
- **参数名**: `DoIPRoutingActivationConfirmationReqLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Describes the amount of bytes used to handle to the confirmation function on routing activation. If 0 is configured as length the parameter ConfirmedReqData will not be handled to the API.

############ 2. DoIPRoutingActivationConfirmationResLength

- **UUID**: `21942a0f-16d4-45ce-9b18-00bc8d9bbca2`
- **参数名**: `DoIPRoutingActivationConfirmationResLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Describes the amount of bytes used to read by the confirmation function on routing activation. If 0 is configured as length the parameter ConfirmedResData will not be fetched via the API.

########### FUNCTION-NAME 类型参数

############ 1. DoIPRoutingAcivationConfirmationFunc

- **UUID**: `db39946a-f4e7-4b4b-a717-c99576579a3e`
- **参数名**: `DoIPRoutingAcivationConfirmationFunc`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Direct C Callback function to trigger the confirmation function for routing activation. If the DoIPRoutingAcivationConfirmationFunc parameter is present the DoIP module will not use an RPort of ServiceInterface <RoutingActivation>_RoutingActivation but call the configured function.

####### 13. DoIPRoutingActivationAuthenticationCallback

**容器属性**:

- **UUID**: `71d44007-a9ff-405c-98cd-b3d2fe7e1990`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPRoutingActivationAuthenticationCallback`
- **多重性**: [0..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

Container describes the Callbackfunction to call on a Routing Activation Request for Authentication. If this container is configured but the DoIPRoutingAcivationAuthenticationFunc parameter is not present, the DoIP module will use an RPort of ServiceInterface <RoutingActivation>_RoutingActivation with the name "CB<RoutingActivation>RoutingActivation". <RoutingActivation> is the ShortName of the DoIPRoutingActiviation container.

######## 参数配置

此容器包含 **3** 个参数：

######### INTEGER 类型参数

########## 1. DoIPRoutingActivationAuthenticationReqLength

- **UUID**: `10ee88e3-2369-4e42-88ce-47ea6b95cd45`
- **参数名**: `DoIPRoutingActivationAuthenticationReqLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Describes the amount of bytes used to handle to the authentication function on routing activation. If 0 is configured as length the parameter AuthenticationReqData will not be handled to the API.

########## 2. DoIPRoutingActivationAuthenticationResLength

- **UUID**: `0619576e-3da9-45d0-a851-90c63d51cb77`
- **参数名**: `DoIPRoutingActivationAuthenticationResLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Describes the amount of bytes used to read by the authentication function on routing activation. If 0 is configured as length the parameter AuthenticationResData will not be fetched via the API.

######### FUNCTION-NAME 类型参数

########## 1. DoIPRoutingAcivationAuthenticationFunc

- **UUID**: `c9c52180-7e06-4986-b8b6-175f2889e5e3`
- **参数名**: `DoIPRoutingAcivationAuthenticationFunc`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Direct C Callback function to trigger the authentication function for routing activation. If the DoIPRoutingAcivationAuthenticationFunc parameter is present, the DoIP module will not use an RPort of ServiceInterface <RoutingActivation>_RoutingActivation but call the configured function.

####### 14. DoIPRoutingActivationConfirmationCallback

**容器属性**:

- **UUID**: `6f8e5715-be9d-448e-a87b-c0eef99ce37b`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPRoutingActivationConfirmationCallback`
- **多重性**: [0..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

Container describes the Callbackfunction to call on a Routing Activation Request for Confirmation. If this container is configured but the DoIPRoutingAcivationConfirmationFunc parameter is not present the DoIP module will use an RPort of ServiceInterface <RoutingActivation>_RoutingActivation with the name "CB<RoutingActivation>RoutingActivation". <RoutingActivation> is the ShortName of the DoIPRoutingActiviation container.

######## 参数配置

此容器包含 **3** 个参数：

######### INTEGER 类型参数

########## 1. DoIPRoutingActivationConfirmationReqLength

- **UUID**: `6515852f-3fd6-44ba-b796-81511c0bb0c9`
- **参数名**: `DoIPRoutingActivationConfirmationReqLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Describes the amount of bytes used to handle to the confirmation function on routing activation. If 0 is configured as length the parameter ConfirmedReqData will not be handled to the API.

########## 2. DoIPRoutingActivationConfirmationResLength

- **UUID**: `21942a0f-16d4-45ce-9b18-00bc8d9bbca2`
- **参数名**: `DoIPRoutingActivationConfirmationResLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Describes the amount of bytes used to read by the confirmation function on routing activation. If 0 is configured as length the parameter ConfirmedResData will not be fetched via the API.

######### FUNCTION-NAME 类型参数

########## 1. DoIPRoutingAcivationConfirmationFunc

- **UUID**: `db39946a-f4e7-4b4b-a717-c99576579a3e`
- **参数名**: `DoIPRoutingAcivationConfirmationFunc`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Direct C Callback function to trigger the confirmation function for routing activation. If the DoIPRoutingAcivationConfirmationFunc parameter is present the DoIP module will not use an RPort of ServiceInterface <RoutingActivation>_RoutingActivation but call the configured function.

####### 15. DoIPTester

**容器属性**:

- **UUID**: `aa1be77a-5cef-40ea-9126-0cd3e7588f5f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPTester`
- **多重性**: [0..255]
- **构建后可变**: true
- **多配置容器**: false

**容器描述**:

This container describes the properties of the possible connectable Tester for the DoIP entity.

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. DoIPNumByteDiagAckNack

- **UUID**: `597517c8-bad9-4b3f-ae96-1a3ffead784c`
- **参数名**: `DoIPNumByteDiagAckNack`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..18446744073709551611]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies the number of original Diagnostic request bytes the DoIP entity responses on a NACK of a diagnostic response message to the Tester.

########## 2. DoIPTesterSA

- **UUID**: `8c8e432f-61d4-4108-af04-86b61fd78c9d`
- **参数名**: `DoIPTesterSA`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Source Address of the Tester sent via routing activation or diagnostic message.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. DoIPRoutingActivationRef

- **UUID**: `3662eb2e-6e34-469a-83b8-a6e77357296d`
- **引用名**: `DoIPRoutingActivationRef`
- **引用类型**: REFERENCE
- **多重性**: [1..255]
- **目标**: `DoIPRoutingActivation`
- **完整路径**: `/AUTOSAR/EcucDefs/DoIP/DoIPConfigSet/DoIPRoutingActivation`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a DoIPRoutingActivation describing the possible routing activations of the DoIPTester

##### 2. DoIPChannel

**容器属性**:

- **UUID**: `eef69e41-b1a0-4b5e-8468-47d0f59a4b79`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPChannel`
- **多重性**: [1..65536]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

Configuration of one DoIPChannel.

###### 引用关系

此容器包含 **2** 个引用：

####### REFERENCE 类型引用

######## 1. DoIPChannelSARef

- **UUID**: `86af5955-9e74-4620-b55f-38d4d9ca71ae`
- **引用名**: `DoIPChannelSARef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `DoIPTester`
- **完整路径**: `/AUTOSAR/EcucDefs/DoIP/DoIPConfigSet/DoIPTester`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the DoIPTester.

######## 2. DoIPChannelTARef

- **UUID**: `a8d6656f-f0b3-49c5-ab9f-159c3bf4c02a`
- **引用名**: `DoIPChannelTARef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `DoIPTargetAddress`
- **完整路径**: `/AUTOSAR/EcucDefs/DoIP/DoIPConfigSet/DoIPConnections/DoIPTargetAddress`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the target address.

###### 配置容器

本模块包含 **2** 个配置容器：

####### 1. DoIPPduRRxPdu

**容器属性**:

- **UUID**: `8e8e65a8-1939-406e-aa0b-6dfb219b42ca`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPPduRRxPdu`
- **多重性**: [1..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container contains the Rx Pdus to connect with the Rx Pdus of the PduR.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. DoIPPduRRxPduId

- **UUID**: `d1ed6fd3-3843-46d7-ab9f-fd58ab8b9562`
- **参数名**: `DoIPPduRRxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The DoIPPduRRxPduId is required by the API call DoIP_CancelReceive.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. DoIPPduRRxPduRef

- **UUID**: `b7bf4060-ce84-436f-a701-33b9768b0a87`
- **引用名**: `DoIPPduRRxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the "global" Pdu structure to allow harmonization of handle IDs in the COM-Stack.

####### 2. DoIPPduRTxPdu

**容器属性**:

- **UUID**: `6f9c6349-bdd5-4bb9-8280-b3a7d3cf9f6b`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPPduRTxPdu`
- **多重性**: [1..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container contains the Tx Pdus to connect with the Tx Pdus of the PduR.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. DoIPPduRTxPduId

- **UUID**: `4eee96d2-a3a6-43de-8ca6-849192414879`
- **参数名**: `DoIPPduRTxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The DoIPPduRTxPduId is required by DoIP_Transmit and DoIP_CancelTransmit.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. DoIPPduRTxPduRef

- **UUID**: `6119b2e5-74a7-46f1-a07a-33d48cd9776b`
- **引用名**: `DoIPPduRTxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the "global" Pdu structure to allow harmonization of handle IDs in the COM-Stack.

##### 3. DoIPPduRRxPdu

**容器属性**:

- **UUID**: `8e8e65a8-1939-406e-aa0b-6dfb219b42ca`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPPduRRxPdu`
- **多重性**: [1..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container contains the Rx Pdus to connect with the Rx Pdus of the PduR.

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. DoIPPduRRxPduId

- **UUID**: `d1ed6fd3-3843-46d7-ab9f-fd58ab8b9562`
- **参数名**: `DoIPPduRRxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The DoIPPduRRxPduId is required by the API call DoIP_CancelReceive.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. DoIPPduRRxPduRef

- **UUID**: `b7bf4060-ce84-436f-a701-33b9768b0a87`
- **引用名**: `DoIPPduRRxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the "global" Pdu structure to allow harmonization of handle IDs in the COM-Stack.

##### 4. DoIPPduRTxPdu

**容器属性**:

- **UUID**: `6f9c6349-bdd5-4bb9-8280-b3a7d3cf9f6b`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPPduRTxPdu`
- **多重性**: [1..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container contains the Tx Pdus to connect with the Tx Pdus of the PduR.

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. DoIPPduRTxPduId

- **UUID**: `4eee96d2-a3a6-43de-8ca6-849192414879`
- **参数名**: `DoIPPduRTxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The DoIPPduRTxPduId is required by DoIP_Transmit and DoIP_CancelTransmit.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. DoIPPduRTxPduRef

- **UUID**: `6119b2e5-74a7-46f1-a07a-33d48cd9776b`
- **引用名**: `DoIPPduRTxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the "global" Pdu structure to allow harmonization of handle IDs in the COM-Stack.

##### 5. DoIPConnections

**容器属性**:

- **UUID**: `a8e99df5-fae8-4860-84b7-5484bc3aa5ea`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPConnections`
- **多重性**: [1..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

Container contains all lower layer connection specific information, i.e. the single Pdu References and Handle IDs to the SoAd.

###### 配置容器

本模块包含 **7** 个配置容器：

####### 1. DoIPTargetAddress

**容器属性**:

- **UUID**: `738662ff-bcd1-4bf9-b33c-a99388e763c4`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPTargetAddress`
- **多重性**: [1..255]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container describes a possible TargetAddress that is supported by DoIP.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. DoIPTargetAddressValue

- **UUID**: `d166da8b-269c-43a2-9cc1-28897951668b`
- **参数名**: `DoIPTargetAddressValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Valid Target Address of a DoIP target address.

####### 2. DoIPTcpConnection

**容器属性**:

- **UUID**: `1d86f9fa-e08b-434e-8c6a-173985feb32a`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPTcpConnection`
- **多重性**: [1..255]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

Each container describes a tcp connection to the lower layer SoAd module.

######## 配置容器

本模块包含 **2** 个配置容器：

######### 1. DoIPSoAdRxPdu

**容器属性**:

- **UUID**: `b780b617-6160-47fb-922d-2720b32889b0`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPSoAdRxPdu`
- **多重性**: [1..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container contains the Rx Pdus received by DoIP

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. DoIPSoAdRxPduId

- **UUID**: `dfbc0748-ee25-4b04-98ca-27c4b9c26a48`
- **参数名**: `DoIPSoAdRxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The DoIPSoAdRxPduId is required by the API call DoIP_SoAdTpRxIndication to receive I-PDUs from the SoAd.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. DoIPSoAdRxPduRef

- **UUID**: `0693db04-cd76-4e47-ab9f-49b3d338cefc`
- **引用名**: `DoIPSoAdRxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the "global" Pdu structure to allow harmonization of handle IDs in the COM-Stack.

######### 2. DoIPSoAdTxPdu

**容器属性**:

- **UUID**: `f764f413-32d6-415e-bf20-06b1f33ac811`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPSoAdTxPdu`
- **多重性**: [1..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container describes the TxPdu sent via the SoAd

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. DoIPSoAdTxPduId

- **UUID**: `0bb68c55-8e46-4757-a573-2f08d3e45943`
- **参数名**: `DoIPSoAdTxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The DoIPSoAdTxPduId is required by the API call DoIP_SoAdTpTxConfirmation that is called by the SoAd to confirm that the IPdu has been transmitted successfully.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. DoIPSoAdTxPduRef

- **UUID**: `3c473230-72c7-48c8-b783-565ea21ada9b`
- **引用名**: `DoIPSoAdTxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the "global" Pdu structure to allow harmonization of handle IDs in the COM-Stack.

####### 3. DoIPSoAdRxPdu

**容器属性**:

- **UUID**: `b780b617-6160-47fb-922d-2720b32889b0`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPSoAdRxPdu`
- **多重性**: [1..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container contains the Rx Pdus received by DoIP

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. DoIPSoAdRxPduId

- **UUID**: `dfbc0748-ee25-4b04-98ca-27c4b9c26a48`
- **参数名**: `DoIPSoAdRxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The DoIPSoAdRxPduId is required by the API call DoIP_SoAdTpRxIndication to receive I-PDUs from the SoAd.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. DoIPSoAdRxPduRef

- **UUID**: `0693db04-cd76-4e47-ab9f-49b3d338cefc`
- **引用名**: `DoIPSoAdRxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the "global" Pdu structure to allow harmonization of handle IDs in the COM-Stack.

####### 4. DoIPSoAdTxPdu

**容器属性**:

- **UUID**: `f764f413-32d6-415e-bf20-06b1f33ac811`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPSoAdTxPdu`
- **多重性**: [1..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container describes the TxPdu sent via the SoAd

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. DoIPSoAdTxPduId

- **UUID**: `0bb68c55-8e46-4757-a573-2f08d3e45943`
- **参数名**: `DoIPSoAdTxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The DoIPSoAdTxPduId is required by the API call DoIP_SoAdTpTxConfirmation that is called by the SoAd to confirm that the IPdu has been transmitted successfully.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. DoIPSoAdTxPduRef

- **UUID**: `3c473230-72c7-48c8-b783-565ea21ada9b`
- **引用名**: `DoIPSoAdTxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the "global" Pdu structure to allow harmonization of handle IDs in the COM-Stack.

####### 5. DoIPUdpConnection

**容器属性**:

- **UUID**: `d40873c8-93f6-4a30-8187-2f5b9175faac`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPUdpConnection`
- **多重性**: [1..255]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This Container describes the udp connection to the lower layer SoAd module.

######## 配置容器

本模块包含 **2** 个配置容器：

######### 1. DoIPSoAdRxPdu

**容器属性**:

- **UUID**: `2000490b-fc46-4b42-9762-e9bd84105208`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPSoAdRxPdu`
- **多重性**: [1..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container contains the Rx Pdus received by DoIP

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. DoIPSoAdRxPduId

- **UUID**: `d6d9639f-165e-4837-95e1-18a976bc52f6`
- **参数名**: `DoIPSoAdRxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The DoIPSoAdRxPduId is required by the API call DoIP_SoAdTpRxIndication to receive I-PDUs from the SoAd.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. DoIPSoAdRxPduRef

- **UUID**: `77c3f3d4-c8ba-4ab6-b72e-32d5d68bbff1`
- **引用名**: `DoIPSoAdRxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the "global" Pdu structure to allow harmonization of handle IDs in the COM-Stack.

######### 2. DoIPSoAdTxPdu

**容器属性**:

- **UUID**: `60b4dec8-ce99-4a24-8484-4d6853b2fe60`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPSoAdTxPdu`
- **多重性**: [1..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container describes the TxPdu sent via the SoAd

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. DoIPSoAdTxPduId

- **UUID**: `ae89ffc6-eb59-420b-bbe8-31d4006bc7ad`
- **参数名**: `DoIPSoAdTxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The DoIPSoAdTxPduId is required by the API call DoIP_SoAdTpTxConfirmation that is called by the SoAd to confirm that the IPdu has been transmitted successfully.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. DoIPSoAdTxPduRef

- **UUID**: `c42b04dc-ce57-4b69-8b1d-953f583173ea`
- **引用名**: `DoIPSoAdTxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the "global" Pdu structure to allow harmonization of handle IDs in the COM-Stack.

####### 6. DoIPSoAdRxPdu

**容器属性**:

- **UUID**: `2000490b-fc46-4b42-9762-e9bd84105208`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPSoAdRxPdu`
- **多重性**: [1..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container contains the Rx Pdus received by DoIP

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. DoIPSoAdRxPduId

- **UUID**: `d6d9639f-165e-4837-95e1-18a976bc52f6`
- **参数名**: `DoIPSoAdRxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The DoIPSoAdRxPduId is required by the API call DoIP_SoAdTpRxIndication to receive I-PDUs from the SoAd.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. DoIPSoAdRxPduRef

- **UUID**: `77c3f3d4-c8ba-4ab6-b72e-32d5d68bbff1`
- **引用名**: `DoIPSoAdRxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the "global" Pdu structure to allow harmonization of handle IDs in the COM-Stack.

####### 7. DoIPSoAdTxPdu

**容器属性**:

- **UUID**: `60b4dec8-ce99-4a24-8484-4d6853b2fe60`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPSoAdTxPdu`
- **多重性**: [1..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container describes the TxPdu sent via the SoAd

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. DoIPSoAdTxPduId

- **UUID**: `ae89ffc6-eb59-420b-bbe8-31d4006bc7ad`
- **参数名**: `DoIPSoAdTxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The DoIPSoAdTxPduId is required by the API call DoIP_SoAdTpTxConfirmation that is called by the SoAd to confirm that the IPdu has been transmitted successfully.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. DoIPSoAdTxPduRef

- **UUID**: `c42b04dc-ce57-4b69-8b1d-953f583173ea`
- **引用名**: `DoIPSoAdTxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the "global" Pdu structure to allow harmonization of handle IDs in the COM-Stack.

##### 6. DoIPTargetAddress

**容器属性**:

- **UUID**: `738662ff-bcd1-4bf9-b33c-a99388e763c4`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPTargetAddress`
- **多重性**: [1..255]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container describes a possible TargetAddress that is supported by DoIP.

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. DoIPTargetAddressValue

- **UUID**: `d166da8b-269c-43a2-9cc1-28897951668b`
- **参数名**: `DoIPTargetAddressValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Valid Target Address of a DoIP target address.

##### 7. DoIPTcpConnection

**容器属性**:

- **UUID**: `1d86f9fa-e08b-434e-8c6a-173985feb32a`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPTcpConnection`
- **多重性**: [1..255]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

Each container describes a tcp connection to the lower layer SoAd module.

###### 配置容器

本模块包含 **2** 个配置容器：

####### 1. DoIPSoAdRxPdu

**容器属性**:

- **UUID**: `b780b617-6160-47fb-922d-2720b32889b0`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPSoAdRxPdu`
- **多重性**: [1..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container contains the Rx Pdus received by DoIP

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. DoIPSoAdRxPduId

- **UUID**: `dfbc0748-ee25-4b04-98ca-27c4b9c26a48`
- **参数名**: `DoIPSoAdRxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The DoIPSoAdRxPduId is required by the API call DoIP_SoAdTpRxIndication to receive I-PDUs from the SoAd.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. DoIPSoAdRxPduRef

- **UUID**: `0693db04-cd76-4e47-ab9f-49b3d338cefc`
- **引用名**: `DoIPSoAdRxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the "global" Pdu structure to allow harmonization of handle IDs in the COM-Stack.

####### 2. DoIPSoAdTxPdu

**容器属性**:

- **UUID**: `f764f413-32d6-415e-bf20-06b1f33ac811`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPSoAdTxPdu`
- **多重性**: [1..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container describes the TxPdu sent via the SoAd

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. DoIPSoAdTxPduId

- **UUID**: `0bb68c55-8e46-4757-a573-2f08d3e45943`
- **参数名**: `DoIPSoAdTxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The DoIPSoAdTxPduId is required by the API call DoIP_SoAdTpTxConfirmation that is called by the SoAd to confirm that the IPdu has been transmitted successfully.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. DoIPSoAdTxPduRef

- **UUID**: `3c473230-72c7-48c8-b783-565ea21ada9b`
- **引用名**: `DoIPSoAdTxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the "global" Pdu structure to allow harmonization of handle IDs in the COM-Stack.

##### 8. DoIPSoAdRxPdu

**容器属性**:

- **UUID**: `b780b617-6160-47fb-922d-2720b32889b0`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPSoAdRxPdu`
- **多重性**: [1..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container contains the Rx Pdus received by DoIP

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. DoIPSoAdRxPduId

- **UUID**: `dfbc0748-ee25-4b04-98ca-27c4b9c26a48`
- **参数名**: `DoIPSoAdRxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The DoIPSoAdRxPduId is required by the API call DoIP_SoAdTpRxIndication to receive I-PDUs from the SoAd.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. DoIPSoAdRxPduRef

- **UUID**: `0693db04-cd76-4e47-ab9f-49b3d338cefc`
- **引用名**: `DoIPSoAdRxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the "global" Pdu structure to allow harmonization of handle IDs in the COM-Stack.

##### 9. DoIPSoAdTxPdu

**容器属性**:

- **UUID**: `f764f413-32d6-415e-bf20-06b1f33ac811`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPSoAdTxPdu`
- **多重性**: [1..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container describes the TxPdu sent via the SoAd

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. DoIPSoAdTxPduId

- **UUID**: `0bb68c55-8e46-4757-a573-2f08d3e45943`
- **参数名**: `DoIPSoAdTxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The DoIPSoAdTxPduId is required by the API call DoIP_SoAdTpTxConfirmation that is called by the SoAd to confirm that the IPdu has been transmitted successfully.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. DoIPSoAdTxPduRef

- **UUID**: `3c473230-72c7-48c8-b783-565ea21ada9b`
- **引用名**: `DoIPSoAdTxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the "global" Pdu structure to allow harmonization of handle IDs in the COM-Stack.

##### 10. DoIPUdpConnection

**容器属性**:

- **UUID**: `d40873c8-93f6-4a30-8187-2f5b9175faac`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPUdpConnection`
- **多重性**: [1..255]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This Container describes the udp connection to the lower layer SoAd module.

###### 配置容器

本模块包含 **2** 个配置容器：

####### 1. DoIPSoAdRxPdu

**容器属性**:

- **UUID**: `2000490b-fc46-4b42-9762-e9bd84105208`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPSoAdRxPdu`
- **多重性**: [1..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container contains the Rx Pdus received by DoIP

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. DoIPSoAdRxPduId

- **UUID**: `d6d9639f-165e-4837-95e1-18a976bc52f6`
- **参数名**: `DoIPSoAdRxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The DoIPSoAdRxPduId is required by the API call DoIP_SoAdTpRxIndication to receive I-PDUs from the SoAd.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. DoIPSoAdRxPduRef

- **UUID**: `77c3f3d4-c8ba-4ab6-b72e-32d5d68bbff1`
- **引用名**: `DoIPSoAdRxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the "global" Pdu structure to allow harmonization of handle IDs in the COM-Stack.

####### 2. DoIPSoAdTxPdu

**容器属性**:

- **UUID**: `60b4dec8-ce99-4a24-8484-4d6853b2fe60`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPSoAdTxPdu`
- **多重性**: [1..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container describes the TxPdu sent via the SoAd

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. DoIPSoAdTxPduId

- **UUID**: `ae89ffc6-eb59-420b-bbe8-31d4006bc7ad`
- **参数名**: `DoIPSoAdTxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The DoIPSoAdTxPduId is required by the API call DoIP_SoAdTpTxConfirmation that is called by the SoAd to confirm that the IPdu has been transmitted successfully.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. DoIPSoAdTxPduRef

- **UUID**: `c42b04dc-ce57-4b69-8b1d-953f583173ea`
- **引用名**: `DoIPSoAdTxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the "global" Pdu structure to allow harmonization of handle IDs in the COM-Stack.

##### 11. DoIPSoAdRxPdu

**容器属性**:

- **UUID**: `2000490b-fc46-4b42-9762-e9bd84105208`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPSoAdRxPdu`
- **多重性**: [1..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container contains the Rx Pdus received by DoIP

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. DoIPSoAdRxPduId

- **UUID**: `d6d9639f-165e-4837-95e1-18a976bc52f6`
- **参数名**: `DoIPSoAdRxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The DoIPSoAdRxPduId is required by the API call DoIP_SoAdTpRxIndication to receive I-PDUs from the SoAd.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. DoIPSoAdRxPduRef

- **UUID**: `77c3f3d4-c8ba-4ab6-b72e-32d5d68bbff1`
- **引用名**: `DoIPSoAdRxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the "global" Pdu structure to allow harmonization of handle IDs in the COM-Stack.

##### 12. DoIPSoAdTxPdu

**容器属性**:

- **UUID**: `60b4dec8-ce99-4a24-8484-4d6853b2fe60`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPSoAdTxPdu`
- **多重性**: [1..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container describes the TxPdu sent via the SoAd

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. DoIPSoAdTxPduId

- **UUID**: `ae89ffc6-eb59-420b-bbe8-31d4006bc7ad`
- **参数名**: `DoIPSoAdTxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The DoIPSoAdTxPduId is required by the API call DoIP_SoAdTpTxConfirmation that is called by the SoAd to confirm that the IPdu has been transmitted successfully.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. DoIPSoAdTxPduRef

- **UUID**: `c42b04dc-ce57-4b69-8b1d-953f583173ea`
- **引用名**: `DoIPSoAdTxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the "global" Pdu structure to allow harmonization of handle IDs in the COM-Stack.

##### 13. DoIPRoutingActivation

**容器属性**:

- **UUID**: `a3f863df-8d3a-424e-b358-5af96d6d2a19`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPRoutingActivation`
- **多重性**: [0..255]
- **构建后可变**: true
- **多配置容器**: false

**容器描述**:

This container describes the routing activation possibilities by representing for each container a possible routing activation request message to the DoIP entity and the according references to the activated diagnostic messages.

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. DoIPRoutingActivationNumber

- **UUID**: `3e3fed60-6259-403d-80ec-5990e4220de7`
- **参数名**: `DoIPRoutingActivationNumber`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Identifies the Routing activation Number which is received for a DoIP routing activation request message.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. DoIPTargetAddressRef

- **UUID**: `56f74807-4daf-4b15-86f7-3ed91dcb50ff`
- **引用名**: `DoIPTargetAddressRef`
- **引用类型**: REFERENCE
- **多重性**: [1..255]
- **目标**: `DoIPTargetAddress`
- **完整路径**: `/AUTOSAR/EcucDefs/DoIP/DoIPConfigSet/DoIPConnections/DoIPTargetAddress`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to all DoIPTargetAddress which are activated on this Routing activation.

###### 配置容器

本模块包含 **2** 个配置容器：

####### 1. DoIPRoutingActivationAuthenticationCallback

**容器属性**:

- **UUID**: `71d44007-a9ff-405c-98cd-b3d2fe7e1990`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPRoutingActivationAuthenticationCallback`
- **多重性**: [0..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

Container describes the Callbackfunction to call on a Routing Activation Request for Authentication. If this container is configured but the DoIPRoutingAcivationAuthenticationFunc parameter is not present, the DoIP module will use an RPort of ServiceInterface <RoutingActivation>_RoutingActivation with the name "CB<RoutingActivation>RoutingActivation". <RoutingActivation> is the ShortName of the DoIPRoutingActiviation container.

######## 参数配置

此容器包含 **3** 个参数：

######### INTEGER 类型参数

########## 1. DoIPRoutingActivationAuthenticationReqLength

- **UUID**: `10ee88e3-2369-4e42-88ce-47ea6b95cd45`
- **参数名**: `DoIPRoutingActivationAuthenticationReqLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Describes the amount of bytes used to handle to the authentication function on routing activation. If 0 is configured as length the parameter AuthenticationReqData will not be handled to the API.

########## 2. DoIPRoutingActivationAuthenticationResLength

- **UUID**: `0619576e-3da9-45d0-a851-90c63d51cb77`
- **参数名**: `DoIPRoutingActivationAuthenticationResLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Describes the amount of bytes used to read by the authentication function on routing activation. If 0 is configured as length the parameter AuthenticationResData will not be fetched via the API.

######### FUNCTION-NAME 类型参数

########## 1. DoIPRoutingAcivationAuthenticationFunc

- **UUID**: `c9c52180-7e06-4986-b8b6-175f2889e5e3`
- **参数名**: `DoIPRoutingAcivationAuthenticationFunc`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Direct C Callback function to trigger the authentication function for routing activation. If the DoIPRoutingAcivationAuthenticationFunc parameter is present, the DoIP module will not use an RPort of ServiceInterface <RoutingActivation>_RoutingActivation but call the configured function.

####### 2. DoIPRoutingActivationConfirmationCallback

**容器属性**:

- **UUID**: `6f8e5715-be9d-448e-a87b-c0eef99ce37b`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPRoutingActivationConfirmationCallback`
- **多重性**: [0..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

Container describes the Callbackfunction to call on a Routing Activation Request for Confirmation. If this container is configured but the DoIPRoutingAcivationConfirmationFunc parameter is not present the DoIP module will use an RPort of ServiceInterface <RoutingActivation>_RoutingActivation with the name "CB<RoutingActivation>RoutingActivation". <RoutingActivation> is the ShortName of the DoIPRoutingActiviation container.

######## 参数配置

此容器包含 **3** 个参数：

######### INTEGER 类型参数

########## 1. DoIPRoutingActivationConfirmationReqLength

- **UUID**: `6515852f-3fd6-44ba-b796-81511c0bb0c9`
- **参数名**: `DoIPRoutingActivationConfirmationReqLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Describes the amount of bytes used to handle to the confirmation function on routing activation. If 0 is configured as length the parameter ConfirmedReqData will not be handled to the API.

########## 2. DoIPRoutingActivationConfirmationResLength

- **UUID**: `21942a0f-16d4-45ce-9b18-00bc8d9bbca2`
- **参数名**: `DoIPRoutingActivationConfirmationResLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Describes the amount of bytes used to read by the confirmation function on routing activation. If 0 is configured as length the parameter ConfirmedResData will not be fetched via the API.

######### FUNCTION-NAME 类型参数

########## 1. DoIPRoutingAcivationConfirmationFunc

- **UUID**: `db39946a-f4e7-4b4b-a717-c99576579a3e`
- **参数名**: `DoIPRoutingAcivationConfirmationFunc`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Direct C Callback function to trigger the confirmation function for routing activation. If the DoIPRoutingAcivationConfirmationFunc parameter is present the DoIP module will not use an RPort of ServiceInterface <RoutingActivation>_RoutingActivation but call the configured function.

##### 14. DoIPRoutingActivationAuthenticationCallback

**容器属性**:

- **UUID**: `71d44007-a9ff-405c-98cd-b3d2fe7e1990`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPRoutingActivationAuthenticationCallback`
- **多重性**: [0..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

Container describes the Callbackfunction to call on a Routing Activation Request for Authentication. If this container is configured but the DoIPRoutingAcivationAuthenticationFunc parameter is not present, the DoIP module will use an RPort of ServiceInterface <RoutingActivation>_RoutingActivation with the name "CB<RoutingActivation>RoutingActivation". <RoutingActivation> is the ShortName of the DoIPRoutingActiviation container.

###### 参数配置

此容器包含 **3** 个参数：

####### INTEGER 类型参数

######## 1. DoIPRoutingActivationAuthenticationReqLength

- **UUID**: `10ee88e3-2369-4e42-88ce-47ea6b95cd45`
- **参数名**: `DoIPRoutingActivationAuthenticationReqLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Describes the amount of bytes used to handle to the authentication function on routing activation. If 0 is configured as length the parameter AuthenticationReqData will not be handled to the API.

######## 2. DoIPRoutingActivationAuthenticationResLength

- **UUID**: `0619576e-3da9-45d0-a851-90c63d51cb77`
- **参数名**: `DoIPRoutingActivationAuthenticationResLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Describes the amount of bytes used to read by the authentication function on routing activation. If 0 is configured as length the parameter AuthenticationResData will not be fetched via the API.

####### FUNCTION-NAME 类型参数

######## 1. DoIPRoutingAcivationAuthenticationFunc

- **UUID**: `c9c52180-7e06-4986-b8b6-175f2889e5e3`
- **参数名**: `DoIPRoutingAcivationAuthenticationFunc`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Direct C Callback function to trigger the authentication function for routing activation. If the DoIPRoutingAcivationAuthenticationFunc parameter is present, the DoIP module will not use an RPort of ServiceInterface <RoutingActivation>_RoutingActivation but call the configured function.

##### 15. DoIPRoutingActivationConfirmationCallback

**容器属性**:

- **UUID**: `6f8e5715-be9d-448e-a87b-c0eef99ce37b`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPRoutingActivationConfirmationCallback`
- **多重性**: [0..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

Container describes the Callbackfunction to call on a Routing Activation Request for Confirmation. If this container is configured but the DoIPRoutingAcivationConfirmationFunc parameter is not present the DoIP module will use an RPort of ServiceInterface <RoutingActivation>_RoutingActivation with the name "CB<RoutingActivation>RoutingActivation". <RoutingActivation> is the ShortName of the DoIPRoutingActiviation container.

###### 参数配置

此容器包含 **3** 个参数：

####### INTEGER 类型参数

######## 1. DoIPRoutingActivationConfirmationReqLength

- **UUID**: `6515852f-3fd6-44ba-b796-81511c0bb0c9`
- **参数名**: `DoIPRoutingActivationConfirmationReqLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Describes the amount of bytes used to handle to the confirmation function on routing activation. If 0 is configured as length the parameter ConfirmedReqData will not be handled to the API.

######## 2. DoIPRoutingActivationConfirmationResLength

- **UUID**: `21942a0f-16d4-45ce-9b18-00bc8d9bbca2`
- **参数名**: `DoIPRoutingActivationConfirmationResLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Describes the amount of bytes used to read by the confirmation function on routing activation. If 0 is configured as length the parameter ConfirmedResData will not be fetched via the API.

####### FUNCTION-NAME 类型参数

######## 1. DoIPRoutingAcivationConfirmationFunc

- **UUID**: `db39946a-f4e7-4b4b-a717-c99576579a3e`
- **参数名**: `DoIPRoutingAcivationConfirmationFunc`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Direct C Callback function to trigger the confirmation function for routing activation. If the DoIPRoutingAcivationConfirmationFunc parameter is present the DoIP module will not use an RPort of ServiceInterface <RoutingActivation>_RoutingActivation but call the configured function.

##### 16. DoIPTester

**容器属性**:

- **UUID**: `aa1be77a-5cef-40ea-9126-0cd3e7588f5f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DoIPTester`
- **多重性**: [0..255]
- **构建后可变**: true
- **多配置容器**: false

**容器描述**:

This container describes the properties of the possible connectable Tester for the DoIP entity.

###### 参数配置

此容器包含 **2** 个参数：

####### INTEGER 类型参数

######## 1. DoIPNumByteDiagAckNack

- **UUID**: `597517c8-bad9-4b3f-ae96-1a3ffead784c`
- **参数名**: `DoIPNumByteDiagAckNack`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..18446744073709551611]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies the number of original Diagnostic request bytes the DoIP entity responses on a NACK of a diagnostic response message to the Tester.

######## 2. DoIPTesterSA

- **UUID**: `8c8e432f-61d4-4108-af04-86b61fd78c9d`
- **参数名**: `DoIPTesterSA`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Source Address of the Tester sent via routing activation or diagnostic message.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. DoIPRoutingActivationRef

- **UUID**: `3662eb2e-6e34-469a-83b8-a6e77357296d`
- **引用名**: `DoIPRoutingActivationRef`
- **引用类型**: REFERENCE
- **多重性**: [1..255]
- **目标**: `DoIPRoutingActivation`
- **完整路径**: `/AUTOSAR/EcucDefs/DoIP/DoIPConfigSet/DoIPRoutingActivation`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a DoIPRoutingActivation describing the possible routing activations of the DoIPTester

##### 17. DoIPGeneral

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

##### 18. DoIPGetGid

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

##### 19. DoIPPowerModeCallback

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

##### 20. DoIPTriggerGidSynchronization

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
