# J1939Dcm - 完整配置文档

*此文档由ARXML文件自动生成，采用层次化结构展示*

**生成时间**: 2025-06-16 14:46:23

## 📑 目录

- [📄 文件信息](#-文件信息)
- [🔧 模块定义](#-模块定义)
  - [J1939Dcm](#j1939dcm)
- [📦 包结构](#-包结构)

## 📄 文件信息

### Schema信息
- **Schema位置**: `http://autosar.org/schema/r4.0 AUTOSAR_4-0-3.xsd`
- **命名空间**: `http://autosar.org/schema/r4.0`

## 🔧 模块定义

### 1. J1939Dcm

#### 基本信息

- **UUID**: `ECUC:cf3f7f17-d451-4134-a7b3-e90b2905a4c3`
- **模块名称**: `J1939Dcm`
- **多重性**: [0..1]
- **支持的变体**:
  - VARIANT-LINK-TIME
  - VARIANT-POST-BUILD
  - VARIANT-PRE-COMPILE

#### 模块描述

The SAE J1939 Dcm module

#### 版本历史

共有 **1** 个版本记录：

##### 1. 版本 4.4.0

- **发布日期**: 2013-10-31
- **发布者**: AUTOSAR

*此版本无详细变更记录*

#### 配置容器

本模块包含 **7** 个配置容器：

##### 1. J1939DcmConfigSet

**容器属性**:

- **UUID**: `ECUC:54d36a7e-56c3-496e-ab52-8668a8543286`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `J1939DcmConfigSet`
- **多重性**: [1..1]
- **多配置容器**: true

**容器描述**:

This container contains the configuration parameters and sub containers of the J1939DCM module supporting multiple configuration sets.

###### 配置容器

本模块包含 **5** 个配置容器：

####### 1. J1939DcmChannel

**容器属性**:

- **UUID**: `ECUC:479961c3-79c3-4dfe-ab40-d2e312782ce6`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `J1939DcmChannel`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

Contains the J1939DcmChannel parameters.

######## 参数配置

此容器包含 **1** 个参数：

######### ENUMERATION 类型参数

########## 1. J1939DcmBusType

- **UUID**: `ECUC:c2832537-bb25-4294-b1aa-0263dedc5354`
- **参数名**: `J1939DcmBusType`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `J1939DCM_ISO9141` (来源: AUTOSAR_ECUC)
  - `J1939DCM_J1587` (来源: AUTOSAR_ECUC)
  - `J1939DCM_J1850` (来源: AUTOSAR_ECUC)
  - `J1939DCM_J1922` (来源: AUTOSAR_ECUC)
  - `J1939DCM_J1939_NETWORK_1` (来源: AUTOSAR_ECUC)
  - `J1939DCM_J1939_NETWORK_2` (来源: AUTOSAR_ECUC)
  - `J1939DCM_J1939_NETWORK_3` (来源: AUTOSAR_ECUC)
  - `J1939DCM_OTHER` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Identifies the communication port

######## 引用关系

此容器包含 **1** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. J1939DcmComMChannelRef

- **UUID**: `ECUC:586413e9-775b-4017-b565-c58b387f0a66`
- **引用名**: `J1939DcmComMChannelRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `ComMChannel`
- **完整路径**: `/AUTOSAR/EcucDefs/ComM/ComMConfigSet/ComMChannel`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the ComMChannel.

####### 2. J1939DcmNode

**容器属性**:

- **UUID**: `ECUC:c3c80278-c732-4da0-a76c-eeede3ba41af`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `J1939DcmNode`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

Contains the parameters for the support of a logical J1939 node (identified by an ECU address).

######## 引用关系

此容器包含 **2** 个引用：

######### REFERENCE 类型引用

########## 1. J1939DcmNodeChannelRef

- **UUID**: `ECUC:3b629c49-6ef1-4a0f-b635-7c707c619f0e`
- **引用名**: `J1939DcmNodeChannelRef`
- **引用类型**: REFERENCE
- **多重性**: [1..infinite]
- **目标**: `J1939DcmChannel`
- **完整路径**: `/AUTOSAR/EcucDefs/J1939Dcm/J1939DcmConfigSet/J1939DcmChannel`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: References to all J1939DcmChannels this node has access to.

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. J1939DcmNmNodeRef

- **UUID**: `ECUC:7c2388e4-11ff-4319-b0f0-a1f58c73cdd5`
- **引用名**: `J1939DcmNmNodeRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..infinite]
- **目标**: `J1939NmNode`
- **完整路径**: `/AUTOSAR/EcucDefs/J1939Nm/J1939NmConfigSet/J1939NmNode`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the corresponding J1939Nm node.

######## 配置容器

本模块包含 **3** 个配置容器：

######### 1. J1939DcmDiagnosticMessageSupport

**容器属性**:

- **UUID**: `ECUC:87be66d8-6859-4b2d-86c6-abc78db9475c`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `J1939DcmDiagnosticMessageSupport`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

Contains parameters to configure the diagnostic message support

########## 参数配置

此容器包含 **1** 个参数：

########### ENUMERATION 类型参数

############ 1. J1939DcmDmxSupport

- **UUID**: `ECUC:9bf1ed6d-d630-46bf-bfba-fcb6a5d7f8f8`
- **参数名**: `J1939DcmDmxSupport`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `J1939DCM_DM10_SUPPORT` (来源: AUTOSAR_ECUC)
  - `J1939DCM_DM11_SUPPORT` (来源: AUTOSAR_ECUC)
  - `J1939DCM_DM12_SUPPORT` (来源: AUTOSAR_ECUC)
  - `J1939DCM_DM13_SUPPORT` (来源: AUTOSAR_ECUC)
  - `J1939DCM_DM14_SUPPORT` (来源: AUTOSAR_ECUC)
  - `J1939DCM_DM15_SUPPORT` (来源: AUTOSAR_ECUC)
  - `J1939DCM_DM16_SUPPORT` (来源: AUTOSAR_ECUC)
  - `J1939DCM_DM17_SUPPORT` (来源: AUTOSAR_ECUC)
  - `J1939DCM_DM18_SUPPORT` (来源: AUTOSAR_ECUC)
  - `J1939DCM_DM19_SUPPORT` (来源: AUTOSAR_ECUC)
  - `J1939DCM_DM1_SUPPORT` (来源: AUTOSAR_ECUC)
  - `J1939DCM_DM20_SUPPORT` (来源: AUTOSAR_ECUC)
  - `J1939DCM_DM21_SUPPORT` (来源: AUTOSAR_ECUC)
  - `J1939DCM_DM22_SUPPORT` (来源: AUTOSAR_ECUC)
  - `J1939DCM_DM23_SUPPORT` (来源: AUTOSAR_ECUC)
  - `J1939DCM_DM24_SUPPORT` (来源: AUTOSAR_ECUC)
  - `J1939DCM_DM25_SUPPORT` (来源: AUTOSAR_ECUC)
  - `J1939DCM_DM26_SUPPORT` (来源: AUTOSAR_ECUC)
  - `J1939DCM_DM27_SUPPORT` (来源: AUTOSAR_ECUC)
  - `J1939DCM_DM28_SUPPORT` (来源: AUTOSAR_ECUC)
  - `J1939DCM_DM29_SUPPORT` (来源: AUTOSAR_ECUC)
  - `J1939DCM_DM2_SUPPORT` (来源: AUTOSAR_ECUC)
  - `J1939DCM_DM30_SUPPORT` (来源: AUTOSAR_ECUC)
  - `J1939DCM_DM31_SUPPORT` (来源: AUTOSAR_ECUC)
  - `J1939DCM_DM32_SUPPORT` (来源: AUTOSAR_ECUC)
  - `J1939DCM_DM33_SUPPORT` (来源: AUTOSAR_ECUC)
  - `J1939DCM_DM34_SUPPORT` (来源: AUTOSAR_ECUC)
  - `J1939DCM_DM35_SUPPORT` (来源: AUTOSAR_ECUC)
  - `J1939DCM_DM36_SUPPORT` (来源: AUTOSAR_ECUC)
  - `J1939DCM_DM37_SUPPORT` (来源: AUTOSAR_ECUC)
  - `J1939DCM_DM38_SUPPORT` (来源: AUTOSAR_ECUC)
  - `J1939DCM_DM39_SUPPORT` (来源: AUTOSAR_ECUC)
  - `J1939DCM_DM3_SUPPORT` (来源: AUTOSAR_ECUC)
  - `J1939DCM_DM40_SUPPORT` (来源: AUTOSAR_ECUC)
  - `J1939DCM_DM41_SUPPORT` (来源: AUTOSAR_ECUC)
  - `J1939DCM_DM42_SUPPORT` (来源: AUTOSAR_ECUC)
  - `J1939DCM_DM43_SUPPORT` (来源: AUTOSAR_ECUC)
  - `J1939DCM_DM44_SUPPORT` (来源: AUTOSAR_ECUC)
  - `J1939DCM_DM45_SUPPORT` (来源: AUTOSAR_ECUC)
  - `J1939DCM_DM46_SUPPORT` (来源: AUTOSAR_ECUC)
  - `J1939DCM_DM47_SUPPORT` (来源: AUTOSAR_ECUC)
  - `J1939DCM_DM48_SUPPORT` (来源: AUTOSAR_ECUC)
  - `J1939DCM_DM49_SUPPORT` (来源: AUTOSAR_ECUC)
  - `J1939DCM_DM4_SUPPORT` (来源: AUTOSAR_ECUC)
  - `J1939DCM_DM50_SUPPORT` (来源: AUTOSAR_ECUC)
  - `J1939DCM_DM51_SUPPORT` (来源: AUTOSAR_ECUC)
  - `J1939DCM_DM52_SUPPORT` (来源: AUTOSAR_ECUC)
  - `J1939DCM_DM5_SUPPORT` (来源: AUTOSAR_ECUC)
  - `J1939DCM_DM6_SUPPORT` (来源: AUTOSAR_ECUC)
  - `J1939DCM_DM7_SUPPORT` (来源: AUTOSAR_ECUC)
  - `J1939DCM_DM8_SUPPORT` (来源: AUTOSAR_ECUC)
  - `J1939DCM_DM9_SUPPORT` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter is used to identify the actual DMx message.

########## 配置容器

本模块包含 **2** 个配置容器：

########### 1. J1939DcmRxPdu

**容器属性**:

- **UUID**: `ECUC:51ff7abe-391b-45d1-8bc7-23ff915747a8`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `J1939DcmRxPdu`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Contains parameters to configure the J1939DcmRxPdu.

############ 参数配置

此容器包含 **1** 个参数：

############# INTEGER 类型参数

############## 1. J1939DcmRxPduId

- **UUID**: `ECUC:47f6f332-a463-4ab4-ae11-2357c1f53117`
- **参数名**: `J1939DcmRxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The I-PDU identifier used for communication with PduR.

############ 引用关系

此容器包含 **1** 个引用：

############# REFERENCE 类型引用

############## 1. J1939DcmRxPduRef

- **UUID**: `ECUC:ca833b0d-d026-408d-a29e-2f6932cc556a`
- **引用名**: `J1939DcmRxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the global Pdu element in the Ecuc module.

########### 2. J1939DcmTxPdu

**容器属性**:

- **UUID**: `ECUC:5cd84b13-9170-4c22-bc15-325eadb42281`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `J1939DcmTxPdu`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Contains parameters to configure the J1939DcmTxPdu.

############ 参数配置

此容器包含 **1** 个参数：

############# INTEGER 类型参数

############## 1. J1939DcmTxPduId

- **UUID**: `ECUC:d5ed5ba0-e2c8-4961-a078-e5c84d9166e4`
- **参数名**: `J1939DcmTxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The I-PDU identifier used to identify the Tx message.

############ 引用关系

此容器包含 **1** 个引用：

############# REFERENCE 类型引用

############## 1. J1939DcmTxPduRef

- **UUID**: `ECUC:91d59c46-3144-499e-91cb-c296b0253830`
- **引用名**: `J1939DcmTxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the global Pdu element in the Ecuc module.

######### 2. J1939DcmRxPdu

**容器属性**:

- **UUID**: `ECUC:51ff7abe-391b-45d1-8bc7-23ff915747a8`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `J1939DcmRxPdu`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Contains parameters to configure the J1939DcmRxPdu.

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. J1939DcmRxPduId

- **UUID**: `ECUC:47f6f332-a463-4ab4-ae11-2357c1f53117`
- **参数名**: `J1939DcmRxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The I-PDU identifier used for communication with PduR.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. J1939DcmRxPduRef

- **UUID**: `ECUC:ca833b0d-d026-408d-a29e-2f6932cc556a`
- **引用名**: `J1939DcmRxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the global Pdu element in the Ecuc module.

######### 3. J1939DcmTxPdu

**容器属性**:

- **UUID**: `ECUC:5cd84b13-9170-4c22-bc15-325eadb42281`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `J1939DcmTxPdu`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Contains parameters to configure the J1939DcmTxPdu.

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. J1939DcmTxPduId

- **UUID**: `ECUC:d5ed5ba0-e2c8-4961-a078-e5c84d9166e4`
- **参数名**: `J1939DcmTxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The I-PDU identifier used to identify the Tx message.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. J1939DcmTxPduRef

- **UUID**: `ECUC:91d59c46-3144-499e-91cb-c296b0253830`
- **引用名**: `J1939DcmTxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the global Pdu element in the Ecuc module.

####### 3. J1939DcmDiagnosticMessageSupport

**容器属性**:

- **UUID**: `ECUC:87be66d8-6859-4b2d-86c6-abc78db9475c`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `J1939DcmDiagnosticMessageSupport`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

Contains parameters to configure the diagnostic message support

######## 参数配置

此容器包含 **1** 个参数：

######### ENUMERATION 类型参数

########## 1. J1939DcmDmxSupport

- **UUID**: `ECUC:9bf1ed6d-d630-46bf-bfba-fcb6a5d7f8f8`
- **参数名**: `J1939DcmDmxSupport`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `J1939DCM_DM10_SUPPORT` (来源: AUTOSAR_ECUC)
  - `J1939DCM_DM11_SUPPORT` (来源: AUTOSAR_ECUC)
  - `J1939DCM_DM12_SUPPORT` (来源: AUTOSAR_ECUC)
  - `J1939DCM_DM13_SUPPORT` (来源: AUTOSAR_ECUC)
  - `J1939DCM_DM14_SUPPORT` (来源: AUTOSAR_ECUC)
  - `J1939DCM_DM15_SUPPORT` (来源: AUTOSAR_ECUC)
  - `J1939DCM_DM16_SUPPORT` (来源: AUTOSAR_ECUC)
  - `J1939DCM_DM17_SUPPORT` (来源: AUTOSAR_ECUC)
  - `J1939DCM_DM18_SUPPORT` (来源: AUTOSAR_ECUC)
  - `J1939DCM_DM19_SUPPORT` (来源: AUTOSAR_ECUC)
  - `J1939DCM_DM1_SUPPORT` (来源: AUTOSAR_ECUC)
  - `J1939DCM_DM20_SUPPORT` (来源: AUTOSAR_ECUC)
  - `J1939DCM_DM21_SUPPORT` (来源: AUTOSAR_ECUC)
  - `J1939DCM_DM22_SUPPORT` (来源: AUTOSAR_ECUC)
  - `J1939DCM_DM23_SUPPORT` (来源: AUTOSAR_ECUC)
  - `J1939DCM_DM24_SUPPORT` (来源: AUTOSAR_ECUC)
  - `J1939DCM_DM25_SUPPORT` (来源: AUTOSAR_ECUC)
  - `J1939DCM_DM26_SUPPORT` (来源: AUTOSAR_ECUC)
  - `J1939DCM_DM27_SUPPORT` (来源: AUTOSAR_ECUC)
  - `J1939DCM_DM28_SUPPORT` (来源: AUTOSAR_ECUC)
  - `J1939DCM_DM29_SUPPORT` (来源: AUTOSAR_ECUC)
  - `J1939DCM_DM2_SUPPORT` (来源: AUTOSAR_ECUC)
  - `J1939DCM_DM30_SUPPORT` (来源: AUTOSAR_ECUC)
  - `J1939DCM_DM31_SUPPORT` (来源: AUTOSAR_ECUC)
  - `J1939DCM_DM32_SUPPORT` (来源: AUTOSAR_ECUC)
  - `J1939DCM_DM33_SUPPORT` (来源: AUTOSAR_ECUC)
  - `J1939DCM_DM34_SUPPORT` (来源: AUTOSAR_ECUC)
  - `J1939DCM_DM35_SUPPORT` (来源: AUTOSAR_ECUC)
  - `J1939DCM_DM36_SUPPORT` (来源: AUTOSAR_ECUC)
  - `J1939DCM_DM37_SUPPORT` (来源: AUTOSAR_ECUC)
  - `J1939DCM_DM38_SUPPORT` (来源: AUTOSAR_ECUC)
  - `J1939DCM_DM39_SUPPORT` (来源: AUTOSAR_ECUC)
  - `J1939DCM_DM3_SUPPORT` (来源: AUTOSAR_ECUC)
  - `J1939DCM_DM40_SUPPORT` (来源: AUTOSAR_ECUC)
  - `J1939DCM_DM41_SUPPORT` (来源: AUTOSAR_ECUC)
  - `J1939DCM_DM42_SUPPORT` (来源: AUTOSAR_ECUC)
  - `J1939DCM_DM43_SUPPORT` (来源: AUTOSAR_ECUC)
  - `J1939DCM_DM44_SUPPORT` (来源: AUTOSAR_ECUC)
  - `J1939DCM_DM45_SUPPORT` (来源: AUTOSAR_ECUC)
  - `J1939DCM_DM46_SUPPORT` (来源: AUTOSAR_ECUC)
  - `J1939DCM_DM47_SUPPORT` (来源: AUTOSAR_ECUC)
  - `J1939DCM_DM48_SUPPORT` (来源: AUTOSAR_ECUC)
  - `J1939DCM_DM49_SUPPORT` (来源: AUTOSAR_ECUC)
  - `J1939DCM_DM4_SUPPORT` (来源: AUTOSAR_ECUC)
  - `J1939DCM_DM50_SUPPORT` (来源: AUTOSAR_ECUC)
  - `J1939DCM_DM51_SUPPORT` (来源: AUTOSAR_ECUC)
  - `J1939DCM_DM52_SUPPORT` (来源: AUTOSAR_ECUC)
  - `J1939DCM_DM5_SUPPORT` (来源: AUTOSAR_ECUC)
  - `J1939DCM_DM6_SUPPORT` (来源: AUTOSAR_ECUC)
  - `J1939DCM_DM7_SUPPORT` (来源: AUTOSAR_ECUC)
  - `J1939DCM_DM8_SUPPORT` (来源: AUTOSAR_ECUC)
  - `J1939DCM_DM9_SUPPORT` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter is used to identify the actual DMx message.

######## 配置容器

本模块包含 **2** 个配置容器：

######### 1. J1939DcmRxPdu

**容器属性**:

- **UUID**: `ECUC:51ff7abe-391b-45d1-8bc7-23ff915747a8`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `J1939DcmRxPdu`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Contains parameters to configure the J1939DcmRxPdu.

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. J1939DcmRxPduId

- **UUID**: `ECUC:47f6f332-a463-4ab4-ae11-2357c1f53117`
- **参数名**: `J1939DcmRxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The I-PDU identifier used for communication with PduR.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. J1939DcmRxPduRef

- **UUID**: `ECUC:ca833b0d-d026-408d-a29e-2f6932cc556a`
- **引用名**: `J1939DcmRxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the global Pdu element in the Ecuc module.

######### 2. J1939DcmTxPdu

**容器属性**:

- **UUID**: `ECUC:5cd84b13-9170-4c22-bc15-325eadb42281`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `J1939DcmTxPdu`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Contains parameters to configure the J1939DcmTxPdu.

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. J1939DcmTxPduId

- **UUID**: `ECUC:d5ed5ba0-e2c8-4961-a078-e5c84d9166e4`
- **参数名**: `J1939DcmTxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The I-PDU identifier used to identify the Tx message.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. J1939DcmTxPduRef

- **UUID**: `ECUC:91d59c46-3144-499e-91cb-c296b0253830`
- **引用名**: `J1939DcmTxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the global Pdu element in the Ecuc module.

####### 4. J1939DcmRxPdu

**容器属性**:

- **UUID**: `ECUC:51ff7abe-391b-45d1-8bc7-23ff915747a8`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `J1939DcmRxPdu`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Contains parameters to configure the J1939DcmRxPdu.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. J1939DcmRxPduId

- **UUID**: `ECUC:47f6f332-a463-4ab4-ae11-2357c1f53117`
- **参数名**: `J1939DcmRxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The I-PDU identifier used for communication with PduR.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. J1939DcmRxPduRef

- **UUID**: `ECUC:ca833b0d-d026-408d-a29e-2f6932cc556a`
- **引用名**: `J1939DcmRxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the global Pdu element in the Ecuc module.

####### 5. J1939DcmTxPdu

**容器属性**:

- **UUID**: `ECUC:5cd84b13-9170-4c22-bc15-325eadb42281`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `J1939DcmTxPdu`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Contains parameters to configure the J1939DcmTxPdu.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. J1939DcmTxPduId

- **UUID**: `ECUC:d5ed5ba0-e2c8-4961-a078-e5c84d9166e4`
- **参数名**: `J1939DcmTxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The I-PDU identifier used to identify the Tx message.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. J1939DcmTxPduRef

- **UUID**: `ECUC:91d59c46-3144-499e-91cb-c296b0253830`
- **引用名**: `J1939DcmTxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the global Pdu element in the Ecuc module.

##### 2. J1939DcmChannel

**容器属性**:

- **UUID**: `ECUC:479961c3-79c3-4dfe-ab40-d2e312782ce6`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `J1939DcmChannel`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

Contains the J1939DcmChannel parameters.

###### 参数配置

此容器包含 **1** 个参数：

####### ENUMERATION 类型参数

######## 1. J1939DcmBusType

- **UUID**: `ECUC:c2832537-bb25-4294-b1aa-0263dedc5354`
- **参数名**: `J1939DcmBusType`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `J1939DCM_ISO9141` (来源: AUTOSAR_ECUC)
  - `J1939DCM_J1587` (来源: AUTOSAR_ECUC)
  - `J1939DCM_J1850` (来源: AUTOSAR_ECUC)
  - `J1939DCM_J1922` (来源: AUTOSAR_ECUC)
  - `J1939DCM_J1939_NETWORK_1` (来源: AUTOSAR_ECUC)
  - `J1939DCM_J1939_NETWORK_2` (来源: AUTOSAR_ECUC)
  - `J1939DCM_J1939_NETWORK_3` (来源: AUTOSAR_ECUC)
  - `J1939DCM_OTHER` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Identifies the communication port

###### 引用关系

此容器包含 **1** 个引用：

####### SYMBOLIC-NAME-REFERENCE 类型引用

######## 1. J1939DcmComMChannelRef

- **UUID**: `ECUC:586413e9-775b-4017-b565-c58b387f0a66`
- **引用名**: `J1939DcmComMChannelRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `ComMChannel`
- **完整路径**: `/AUTOSAR/EcucDefs/ComM/ComMConfigSet/ComMChannel`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the ComMChannel.

##### 3. J1939DcmNode

**容器属性**:

- **UUID**: `ECUC:c3c80278-c732-4da0-a76c-eeede3ba41af`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `J1939DcmNode`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

Contains the parameters for the support of a logical J1939 node (identified by an ECU address).

###### 引用关系

此容器包含 **2** 个引用：

####### REFERENCE 类型引用

######## 1. J1939DcmNodeChannelRef

- **UUID**: `ECUC:3b629c49-6ef1-4a0f-b635-7c707c619f0e`
- **引用名**: `J1939DcmNodeChannelRef`
- **引用类型**: REFERENCE
- **多重性**: [1..infinite]
- **目标**: `J1939DcmChannel`
- **完整路径**: `/AUTOSAR/EcucDefs/J1939Dcm/J1939DcmConfigSet/J1939DcmChannel`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: References to all J1939DcmChannels this node has access to.

####### SYMBOLIC-NAME-REFERENCE 类型引用

######## 1. J1939DcmNmNodeRef

- **UUID**: `ECUC:7c2388e4-11ff-4319-b0f0-a1f58c73cdd5`
- **引用名**: `J1939DcmNmNodeRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..infinite]
- **目标**: `J1939NmNode`
- **完整路径**: `/AUTOSAR/EcucDefs/J1939Nm/J1939NmConfigSet/J1939NmNode`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the corresponding J1939Nm node.

###### 配置容器

本模块包含 **3** 个配置容器：

####### 1. J1939DcmDiagnosticMessageSupport

**容器属性**:

- **UUID**: `ECUC:87be66d8-6859-4b2d-86c6-abc78db9475c`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `J1939DcmDiagnosticMessageSupport`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

Contains parameters to configure the diagnostic message support

######## 参数配置

此容器包含 **1** 个参数：

######### ENUMERATION 类型参数

########## 1. J1939DcmDmxSupport

- **UUID**: `ECUC:9bf1ed6d-d630-46bf-bfba-fcb6a5d7f8f8`
- **参数名**: `J1939DcmDmxSupport`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `J1939DCM_DM10_SUPPORT` (来源: AUTOSAR_ECUC)
  - `J1939DCM_DM11_SUPPORT` (来源: AUTOSAR_ECUC)
  - `J1939DCM_DM12_SUPPORT` (来源: AUTOSAR_ECUC)
  - `J1939DCM_DM13_SUPPORT` (来源: AUTOSAR_ECUC)
  - `J1939DCM_DM14_SUPPORT` (来源: AUTOSAR_ECUC)
  - `J1939DCM_DM15_SUPPORT` (来源: AUTOSAR_ECUC)
  - `J1939DCM_DM16_SUPPORT` (来源: AUTOSAR_ECUC)
  - `J1939DCM_DM17_SUPPORT` (来源: AUTOSAR_ECUC)
  - `J1939DCM_DM18_SUPPORT` (来源: AUTOSAR_ECUC)
  - `J1939DCM_DM19_SUPPORT` (来源: AUTOSAR_ECUC)
  - `J1939DCM_DM1_SUPPORT` (来源: AUTOSAR_ECUC)
  - `J1939DCM_DM20_SUPPORT` (来源: AUTOSAR_ECUC)
  - `J1939DCM_DM21_SUPPORT` (来源: AUTOSAR_ECUC)
  - `J1939DCM_DM22_SUPPORT` (来源: AUTOSAR_ECUC)
  - `J1939DCM_DM23_SUPPORT` (来源: AUTOSAR_ECUC)
  - `J1939DCM_DM24_SUPPORT` (来源: AUTOSAR_ECUC)
  - `J1939DCM_DM25_SUPPORT` (来源: AUTOSAR_ECUC)
  - `J1939DCM_DM26_SUPPORT` (来源: AUTOSAR_ECUC)
  - `J1939DCM_DM27_SUPPORT` (来源: AUTOSAR_ECUC)
  - `J1939DCM_DM28_SUPPORT` (来源: AUTOSAR_ECUC)
  - `J1939DCM_DM29_SUPPORT` (来源: AUTOSAR_ECUC)
  - `J1939DCM_DM2_SUPPORT` (来源: AUTOSAR_ECUC)
  - `J1939DCM_DM30_SUPPORT` (来源: AUTOSAR_ECUC)
  - `J1939DCM_DM31_SUPPORT` (来源: AUTOSAR_ECUC)
  - `J1939DCM_DM32_SUPPORT` (来源: AUTOSAR_ECUC)
  - `J1939DCM_DM33_SUPPORT` (来源: AUTOSAR_ECUC)
  - `J1939DCM_DM34_SUPPORT` (来源: AUTOSAR_ECUC)
  - `J1939DCM_DM35_SUPPORT` (来源: AUTOSAR_ECUC)
  - `J1939DCM_DM36_SUPPORT` (来源: AUTOSAR_ECUC)
  - `J1939DCM_DM37_SUPPORT` (来源: AUTOSAR_ECUC)
  - `J1939DCM_DM38_SUPPORT` (来源: AUTOSAR_ECUC)
  - `J1939DCM_DM39_SUPPORT` (来源: AUTOSAR_ECUC)
  - `J1939DCM_DM3_SUPPORT` (来源: AUTOSAR_ECUC)
  - `J1939DCM_DM40_SUPPORT` (来源: AUTOSAR_ECUC)
  - `J1939DCM_DM41_SUPPORT` (来源: AUTOSAR_ECUC)
  - `J1939DCM_DM42_SUPPORT` (来源: AUTOSAR_ECUC)
  - `J1939DCM_DM43_SUPPORT` (来源: AUTOSAR_ECUC)
  - `J1939DCM_DM44_SUPPORT` (来源: AUTOSAR_ECUC)
  - `J1939DCM_DM45_SUPPORT` (来源: AUTOSAR_ECUC)
  - `J1939DCM_DM46_SUPPORT` (来源: AUTOSAR_ECUC)
  - `J1939DCM_DM47_SUPPORT` (来源: AUTOSAR_ECUC)
  - `J1939DCM_DM48_SUPPORT` (来源: AUTOSAR_ECUC)
  - `J1939DCM_DM49_SUPPORT` (来源: AUTOSAR_ECUC)
  - `J1939DCM_DM4_SUPPORT` (来源: AUTOSAR_ECUC)
  - `J1939DCM_DM50_SUPPORT` (来源: AUTOSAR_ECUC)
  - `J1939DCM_DM51_SUPPORT` (来源: AUTOSAR_ECUC)
  - `J1939DCM_DM52_SUPPORT` (来源: AUTOSAR_ECUC)
  - `J1939DCM_DM5_SUPPORT` (来源: AUTOSAR_ECUC)
  - `J1939DCM_DM6_SUPPORT` (来源: AUTOSAR_ECUC)
  - `J1939DCM_DM7_SUPPORT` (来源: AUTOSAR_ECUC)
  - `J1939DCM_DM8_SUPPORT` (来源: AUTOSAR_ECUC)
  - `J1939DCM_DM9_SUPPORT` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter is used to identify the actual DMx message.

######## 配置容器

本模块包含 **2** 个配置容器：

######### 1. J1939DcmRxPdu

**容器属性**:

- **UUID**: `ECUC:51ff7abe-391b-45d1-8bc7-23ff915747a8`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `J1939DcmRxPdu`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Contains parameters to configure the J1939DcmRxPdu.

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. J1939DcmRxPduId

- **UUID**: `ECUC:47f6f332-a463-4ab4-ae11-2357c1f53117`
- **参数名**: `J1939DcmRxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The I-PDU identifier used for communication with PduR.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. J1939DcmRxPduRef

- **UUID**: `ECUC:ca833b0d-d026-408d-a29e-2f6932cc556a`
- **引用名**: `J1939DcmRxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the global Pdu element in the Ecuc module.

######### 2. J1939DcmTxPdu

**容器属性**:

- **UUID**: `ECUC:5cd84b13-9170-4c22-bc15-325eadb42281`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `J1939DcmTxPdu`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Contains parameters to configure the J1939DcmTxPdu.

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. J1939DcmTxPduId

- **UUID**: `ECUC:d5ed5ba0-e2c8-4961-a078-e5c84d9166e4`
- **参数名**: `J1939DcmTxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The I-PDU identifier used to identify the Tx message.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. J1939DcmTxPduRef

- **UUID**: `ECUC:91d59c46-3144-499e-91cb-c296b0253830`
- **引用名**: `J1939DcmTxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the global Pdu element in the Ecuc module.

####### 2. J1939DcmRxPdu

**容器属性**:

- **UUID**: `ECUC:51ff7abe-391b-45d1-8bc7-23ff915747a8`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `J1939DcmRxPdu`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Contains parameters to configure the J1939DcmRxPdu.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. J1939DcmRxPduId

- **UUID**: `ECUC:47f6f332-a463-4ab4-ae11-2357c1f53117`
- **参数名**: `J1939DcmRxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The I-PDU identifier used for communication with PduR.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. J1939DcmRxPduRef

- **UUID**: `ECUC:ca833b0d-d026-408d-a29e-2f6932cc556a`
- **引用名**: `J1939DcmRxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the global Pdu element in the Ecuc module.

####### 3. J1939DcmTxPdu

**容器属性**:

- **UUID**: `ECUC:5cd84b13-9170-4c22-bc15-325eadb42281`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `J1939DcmTxPdu`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Contains parameters to configure the J1939DcmTxPdu.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. J1939DcmTxPduId

- **UUID**: `ECUC:d5ed5ba0-e2c8-4961-a078-e5c84d9166e4`
- **参数名**: `J1939DcmTxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The I-PDU identifier used to identify the Tx message.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. J1939DcmTxPduRef

- **UUID**: `ECUC:91d59c46-3144-499e-91cb-c296b0253830`
- **引用名**: `J1939DcmTxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the global Pdu element in the Ecuc module.

##### 4. J1939DcmDiagnosticMessageSupport

**容器属性**:

- **UUID**: `ECUC:87be66d8-6859-4b2d-86c6-abc78db9475c`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `J1939DcmDiagnosticMessageSupport`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

Contains parameters to configure the diagnostic message support

###### 参数配置

此容器包含 **1** 个参数：

####### ENUMERATION 类型参数

######## 1. J1939DcmDmxSupport

- **UUID**: `ECUC:9bf1ed6d-d630-46bf-bfba-fcb6a5d7f8f8`
- **参数名**: `J1939DcmDmxSupport`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `J1939DCM_DM10_SUPPORT` (来源: AUTOSAR_ECUC)
  - `J1939DCM_DM11_SUPPORT` (来源: AUTOSAR_ECUC)
  - `J1939DCM_DM12_SUPPORT` (来源: AUTOSAR_ECUC)
  - `J1939DCM_DM13_SUPPORT` (来源: AUTOSAR_ECUC)
  - `J1939DCM_DM14_SUPPORT` (来源: AUTOSAR_ECUC)
  - `J1939DCM_DM15_SUPPORT` (来源: AUTOSAR_ECUC)
  - `J1939DCM_DM16_SUPPORT` (来源: AUTOSAR_ECUC)
  - `J1939DCM_DM17_SUPPORT` (来源: AUTOSAR_ECUC)
  - `J1939DCM_DM18_SUPPORT` (来源: AUTOSAR_ECUC)
  - `J1939DCM_DM19_SUPPORT` (来源: AUTOSAR_ECUC)
  - `J1939DCM_DM1_SUPPORT` (来源: AUTOSAR_ECUC)
  - `J1939DCM_DM20_SUPPORT` (来源: AUTOSAR_ECUC)
  - `J1939DCM_DM21_SUPPORT` (来源: AUTOSAR_ECUC)
  - `J1939DCM_DM22_SUPPORT` (来源: AUTOSAR_ECUC)
  - `J1939DCM_DM23_SUPPORT` (来源: AUTOSAR_ECUC)
  - `J1939DCM_DM24_SUPPORT` (来源: AUTOSAR_ECUC)
  - `J1939DCM_DM25_SUPPORT` (来源: AUTOSAR_ECUC)
  - `J1939DCM_DM26_SUPPORT` (来源: AUTOSAR_ECUC)
  - `J1939DCM_DM27_SUPPORT` (来源: AUTOSAR_ECUC)
  - `J1939DCM_DM28_SUPPORT` (来源: AUTOSAR_ECUC)
  - `J1939DCM_DM29_SUPPORT` (来源: AUTOSAR_ECUC)
  - `J1939DCM_DM2_SUPPORT` (来源: AUTOSAR_ECUC)
  - `J1939DCM_DM30_SUPPORT` (来源: AUTOSAR_ECUC)
  - `J1939DCM_DM31_SUPPORT` (来源: AUTOSAR_ECUC)
  - `J1939DCM_DM32_SUPPORT` (来源: AUTOSAR_ECUC)
  - `J1939DCM_DM33_SUPPORT` (来源: AUTOSAR_ECUC)
  - `J1939DCM_DM34_SUPPORT` (来源: AUTOSAR_ECUC)
  - `J1939DCM_DM35_SUPPORT` (来源: AUTOSAR_ECUC)
  - `J1939DCM_DM36_SUPPORT` (来源: AUTOSAR_ECUC)
  - `J1939DCM_DM37_SUPPORT` (来源: AUTOSAR_ECUC)
  - `J1939DCM_DM38_SUPPORT` (来源: AUTOSAR_ECUC)
  - `J1939DCM_DM39_SUPPORT` (来源: AUTOSAR_ECUC)
  - `J1939DCM_DM3_SUPPORT` (来源: AUTOSAR_ECUC)
  - `J1939DCM_DM40_SUPPORT` (来源: AUTOSAR_ECUC)
  - `J1939DCM_DM41_SUPPORT` (来源: AUTOSAR_ECUC)
  - `J1939DCM_DM42_SUPPORT` (来源: AUTOSAR_ECUC)
  - `J1939DCM_DM43_SUPPORT` (来源: AUTOSAR_ECUC)
  - `J1939DCM_DM44_SUPPORT` (来源: AUTOSAR_ECUC)
  - `J1939DCM_DM45_SUPPORT` (来源: AUTOSAR_ECUC)
  - `J1939DCM_DM46_SUPPORT` (来源: AUTOSAR_ECUC)
  - `J1939DCM_DM47_SUPPORT` (来源: AUTOSAR_ECUC)
  - `J1939DCM_DM48_SUPPORT` (来源: AUTOSAR_ECUC)
  - `J1939DCM_DM49_SUPPORT` (来源: AUTOSAR_ECUC)
  - `J1939DCM_DM4_SUPPORT` (来源: AUTOSAR_ECUC)
  - `J1939DCM_DM50_SUPPORT` (来源: AUTOSAR_ECUC)
  - `J1939DCM_DM51_SUPPORT` (来源: AUTOSAR_ECUC)
  - `J1939DCM_DM52_SUPPORT` (来源: AUTOSAR_ECUC)
  - `J1939DCM_DM5_SUPPORT` (来源: AUTOSAR_ECUC)
  - `J1939DCM_DM6_SUPPORT` (来源: AUTOSAR_ECUC)
  - `J1939DCM_DM7_SUPPORT` (来源: AUTOSAR_ECUC)
  - `J1939DCM_DM8_SUPPORT` (来源: AUTOSAR_ECUC)
  - `J1939DCM_DM9_SUPPORT` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter is used to identify the actual DMx message.

###### 配置容器

本模块包含 **2** 个配置容器：

####### 1. J1939DcmRxPdu

**容器属性**:

- **UUID**: `ECUC:51ff7abe-391b-45d1-8bc7-23ff915747a8`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `J1939DcmRxPdu`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Contains parameters to configure the J1939DcmRxPdu.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. J1939DcmRxPduId

- **UUID**: `ECUC:47f6f332-a463-4ab4-ae11-2357c1f53117`
- **参数名**: `J1939DcmRxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The I-PDU identifier used for communication with PduR.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. J1939DcmRxPduRef

- **UUID**: `ECUC:ca833b0d-d026-408d-a29e-2f6932cc556a`
- **引用名**: `J1939DcmRxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the global Pdu element in the Ecuc module.

####### 2. J1939DcmTxPdu

**容器属性**:

- **UUID**: `ECUC:5cd84b13-9170-4c22-bc15-325eadb42281`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `J1939DcmTxPdu`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Contains parameters to configure the J1939DcmTxPdu.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. J1939DcmTxPduId

- **UUID**: `ECUC:d5ed5ba0-e2c8-4961-a078-e5c84d9166e4`
- **参数名**: `J1939DcmTxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The I-PDU identifier used to identify the Tx message.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. J1939DcmTxPduRef

- **UUID**: `ECUC:91d59c46-3144-499e-91cb-c296b0253830`
- **引用名**: `J1939DcmTxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the global Pdu element in the Ecuc module.

##### 5. J1939DcmRxPdu

**容器属性**:

- **UUID**: `ECUC:51ff7abe-391b-45d1-8bc7-23ff915747a8`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `J1939DcmRxPdu`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Contains parameters to configure the J1939DcmRxPdu.

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. J1939DcmRxPduId

- **UUID**: `ECUC:47f6f332-a463-4ab4-ae11-2357c1f53117`
- **参数名**: `J1939DcmRxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The I-PDU identifier used for communication with PduR.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. J1939DcmRxPduRef

- **UUID**: `ECUC:ca833b0d-d026-408d-a29e-2f6932cc556a`
- **引用名**: `J1939DcmRxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the global Pdu element in the Ecuc module.

##### 6. J1939DcmTxPdu

**容器属性**:

- **UUID**: `ECUC:5cd84b13-9170-4c22-bc15-325eadb42281`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `J1939DcmTxPdu`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Contains parameters to configure the J1939DcmTxPdu.

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. J1939DcmTxPduId

- **UUID**: `ECUC:d5ed5ba0-e2c8-4961-a078-e5c84d9166e4`
- **参数名**: `J1939DcmTxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The I-PDU identifier used to identify the Tx message.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. J1939DcmTxPduRef

- **UUID**: `ECUC:91d59c46-3144-499e-91cb-c296b0253830`
- **引用名**: `J1939DcmTxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the global Pdu element in the Ecuc module.

##### 7. J1939DcmGeneral

**容器属性**:

- **UUID**: `ECUC:b9c7141d-4b7f-4b67-a69a-94b54e5e2350`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `J1939DcmGeneral`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

Contains the general configuration parameters of the module.

###### 参数配置

此容器包含 **8** 个参数：

####### INTEGER 类型参数

######## 1. J1939DcmCommonBufferSize

- **UUID**: `ECUC:75cc5147-5255-4b18-ae07-d333e462e901`
- **参数名**: `J1939DcmCommonBufferSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Size of common buffer (in Bytes). The buffer size should be as large as the longest command or response message.

######## 2. J1939DcmDM1BufferSize

- **UUID**: `ECUC:cfc31919-2f6c-4ec0-919f-afce870be6ab`
- **参数名**: `J1939DcmDM1BufferSize`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [1..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Size of DM1 buffer (in Bytes). The buffer size should be as large as the longest DM1 response message.

######## 3. J1939DcmMaxDTCsPerMainFunction

- **UUID**: `ECUC:8e9c59fd-60eb-4033-a05e-8ffa50bc9b32`
- **参数名**: `J1939DcmMaxDTCsPerMainFunction`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [1..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Maximum threshold of DTCs filtered in a single MainFunction cycle.

######## 4. J1939DcmMaxFreezeFramesPerMainFunction

- **UUID**: `ECUC:dbeea3ec-67a4-4b25-a58a-6ee028e3e33b`
- **参数名**: `J1939DcmMaxFreezeFramesPerMainFunction`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [1..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Maximum threshold of FreezeFrames filtered in a single MainFunction cycle.

######## 5. J1939DcmMaxRatiosPerMainFunction

- **UUID**: `ECUC:618f1f50-57a6-494d-bbd6-a96c0c97a067`
- **参数名**: `J1939DcmMaxRatiosPerMainFunction`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [1..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Maximum threshold of Ratios filtered in a single MainFunction cycle.

####### BOOLEAN 类型参数

######## 1. J1939DcmDevErrorDetect

- **UUID**: `ECUC:e3fe7a83-abdd-4ce3-bb7e-a69b2b4c1395`
- **参数名**: `J1939DcmDevErrorDetect`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Pre-processor switch for enabling development error detection support.

######## 2. J1939DcmVersionInfoApi

- **UUID**: `ECUC:3a2aad50-1a5c-41e0-bf89-4790e65410a8`
- **参数名**: `J1939DcmVersionInfoApi`
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

######## 1. J1939DcmMainFunctionPeriod

- **UUID**: `ECUC:15eb4ec9-68f9-4310-877a-b722370f5e01`
- **参数名**: `J1939DcmMainFunctionPeriod`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0.001..0.255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Call cycle in seconds of J1939Dcm_MainFunction.

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

1. **J1939Dcm**
