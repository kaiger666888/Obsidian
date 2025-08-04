# J1939Nm - 完整配置文档

*此文档由ARXML文件自动生成，采用层次化结构展示*

**生成时间**: 2025-06-16 14:46:23

## 📑 目录

- [📄 文件信息](#-文件信息)
- [🔧 模块定义](#-模块定义)
  - [J1939Nm](#j1939nm)
- [📦 包结构](#-包结构)

## 📄 文件信息

### Schema信息
- **Schema位置**: `http://autosar.org/schema/r4.0 AUTOSAR_4-0-3.xsd`
- **命名空间**: `http://autosar.org/schema/r4.0`

## 🔧 模块定义

### 1. J1939Nm

#### 基本信息

- **UUID**: `ECUC:8b3bd06a-097b-4f1d-bdf2-48e72516fcfb`
- **模块名称**: `J1939Nm`
- **多重性**: [0..1]
- **支持的变体**:
  - VARIANT-LINK-TIME
  - VARIANT-POST-BUILD
  - VARIANT-PRE-COMPILE

#### 模块描述

The SAE J1939 Nm module

#### 版本历史

共有 **1** 个版本记录：

##### 1. 版本 4.4.0

- **发布日期**: 2013-10-31
- **发布者**: AUTOSAR

*此版本无详细变更记录*

#### 配置容器

本模块包含 **7** 个配置容器：

##### 1. J1939NmConfigSet

**容器属性**:

- **UUID**: `ECUC:87bed3ae-939d-4412-833a-67416982645a`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `J1939NmConfigSet`
- **多重性**: [1..1]
- **多配置容器**: true

**容器描述**:

This container is a MultipleConfigurationContainer, i.e. this container and its sub-containers exist once per configuration set.

###### 配置容器

本模块包含 **4** 个配置容器：

####### 1. J1939NmChannel

**容器属性**:

- **UUID**: `ECUC:91f209de-2296-44de-bbba-934fa68478a3`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `J1939NmChannel`
- **多重性**: [1..infinite]
- **构建后可变**: true
- **多配置容器**: false

**容器描述**:

Physical CAN channel handled by J1939Nm.

######## 引用关系

此容器包含 **1** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. J1939NmComMNetworkHandleRef

- **UUID**: `ECUC:40ce4e12-8c1a-40bd-aa17-3736a1d0bcc3`
- **引用名**: `J1939NmComMNetworkHandleRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `ComMChannel`
- **完整路径**: `/AUTOSAR/EcucDefs/ComM/ComMConfigSet/ComMChannel`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the channel defined by the ComMChannel providing access to the unique channel index ComMChannelId.

######## 配置容器

本模块包含 **2** 个配置容器：

######### 1. J1939NmRxPdu

**容器属性**:

- **UUID**: `ECUC:cd6ba114-60e2-4a76-903c-9bd53ad0e9f0`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `J1939NmRxPdu`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

Contains the configuration of the I-PDU used to receive the AddressClaimed PG.

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. J1939NmRxPduId

- **UUID**: `ECUC:8b5769b0-b023-4312-b133-225e768d24b9`
- **参数名**: `J1939NmRxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The I-PDU identifier used for RxIndication from CanIf.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. J1939NmRxPduRef

- **UUID**: `ECUC:b160754a-d835-49e6-947c-1bda8bfe67fd`
- **引用名**: `J1939NmRxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the Pdu object representing the I-PDU.

######### 2. J1939NmTxPdu

**容器属性**:

- **UUID**: `ECUC:5290a782-b763-461f-aefa-fd3eaf2438ec`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `J1939NmTxPdu`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

Contains the configuration of the I-PDU used to transmit the AddressClaimed PG.

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. J1939NmTxPduId

- **UUID**: `ECUC:a56515cd-e693-44d6-90ad-9978da64beeb`
- **参数名**: `J1939NmTxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The I-PDU identifier used for TxConfirmation from CanIf.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. J1939NmTxPduRef

- **UUID**: `ECUC:ef0d1c92-2c51-4eda-a348-4edf6545f048`
- **引用名**: `J1939NmTxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the Pdu object representing the I-PDU.

####### 2. J1939NmRxPdu

**容器属性**:

- **UUID**: `ECUC:cd6ba114-60e2-4a76-903c-9bd53ad0e9f0`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `J1939NmRxPdu`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

Contains the configuration of the I-PDU used to receive the AddressClaimed PG.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. J1939NmRxPduId

- **UUID**: `ECUC:8b5769b0-b023-4312-b133-225e768d24b9`
- **参数名**: `J1939NmRxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The I-PDU identifier used for RxIndication from CanIf.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. J1939NmRxPduRef

- **UUID**: `ECUC:b160754a-d835-49e6-947c-1bda8bfe67fd`
- **引用名**: `J1939NmRxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the Pdu object representing the I-PDU.

####### 3. J1939NmTxPdu

**容器属性**:

- **UUID**: `ECUC:5290a782-b763-461f-aefa-fd3eaf2438ec`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `J1939NmTxPdu`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

Contains the configuration of the I-PDU used to transmit the AddressClaimed PG.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. J1939NmTxPduId

- **UUID**: `ECUC:a56515cd-e693-44d6-90ad-9978da64beeb`
- **参数名**: `J1939NmTxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The I-PDU identifier used for TxConfirmation from CanIf.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. J1939NmTxPduRef

- **UUID**: `ECUC:ef0d1c92-2c51-4eda-a348-4edf6545f048`
- **引用名**: `J1939NmTxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the Pdu object representing the I-PDU.

####### 4. J1939NmNode

**容器属性**:

- **UUID**: `ECUC:cccaa4c2-b5e3-40f5-8f09-e27161937982`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `J1939NmNode`
- **多重性**: [1..infinite]
- **构建后可变**: true
- **多配置容器**: false

**容器描述**:

Logical node representing one function handled by J1939Nm.

######## 参数配置

此容器包含 **12** 个参数：

######### INTEGER 类型参数

########## 1. J1939NmNodeId

- **UUID**: `ECUC:076630b4-11af-4476-92b1-8f2977197854`
- **参数名**: `J1939NmNodeId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Unique identifier of this node. May be chosen to be identical with J1939NmNodePreferredAddress, if the same address shall not be used by different nodes on different channels.

########## 2. J1939NmNodeNameECUInstance

- **UUID**: `ECUC:633b21cb-8cd9-4e4a-bd78-2f53f92c6adc`
- **参数名**: `J1939NmNodeNameECUInstance`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..7]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: ECU Instance field of the NAME of this node.

########## 3. J1939NmNodeNameFunction

- **UUID**: `ECUC:124e5383-ff69-4c92-b71d-dfd0c8567365`
- **参数名**: `J1939NmNodeNameFunction`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Function field of the NAME of this node.

########## 4. J1939NmNodeNameFunctionInstance

- **UUID**: `ECUC:20d916a0-3481-4502-bcf7-6e5ff6df7541`
- **参数名**: `J1939NmNodeNameFunctionInstance`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..31]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Function Instance field of the NAME of this node.

########## 5. J1939NmNodeNameIdentityNumber

- **UUID**: `ECUC:d1bd0d42-502e-4ccb-8e81-3a094bc92b18`
- **参数名**: `J1939NmNodeNameIdentityNumber`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..2097151]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Identity Number field of the NAME of this node.

########## 6. J1939NmNodeNameIndustryGroup

- **UUID**: `ECUC:ef2b10d3-f245-4e26-af43-d73d6b7e085c`
- **参数名**: `J1939NmNodeNameIndustryGroup`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..7]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Industry Group field of the NAME of this node.

########## 7. J1939NmNodeNameManufacturerCode

- **UUID**: `ECUC:08a5086c-3f16-4616-83b1-0a21ef16b14d`
- **参数名**: `J1939NmNodeNameManufacturerCode`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..2047]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Manufacturer Code field of the NAME of this node.

########## 8. J1939NmNodeNameVehicleSystem

- **UUID**: `ECUC:3553c17f-b620-4d8a-8917-d471a24769ac`
- **参数名**: `J1939NmNodeNameVehicleSystem`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..127]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Vehicle System field of the NAME of this node.

########## 9. J1939NmNodeNameVehicleSystemInstance

- **UUID**: `ECUC:4f775893-203a-45ec-87be-5c9f165ea17f`
- **参数名**: `J1939NmNodeNameVehicleSystemInstance`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..15]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Vehicle System Instance field of the NAME of this node.

########## 10. J1939NmNodePreferredAddress

- **UUID**: `ECUC:86331330-8cf2-4ae5-af39-f65878df134e`
- **参数名**: `J1939NmNodePreferredAddress`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..253]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Source address of this node used for address claiming.

######### BOOLEAN 类型参数

########## 1. J1939NmNodeNameArbitraryAddressCapable

- **UUID**: `ECUC:a35df279-672f-4e1b-a2bd-fd4085ad3080`
- **参数名**: `J1939NmNodeNameArbitraryAddressCapable`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Arbitrary Address Capable field of the NAME of this node.

########## 2. J1939NmNodeStartUpDelay

- **UUID**: `ECUC:3e9bfadc-80ef-467c-8488-d9d90431de26`
- **参数名**: `J1939NmNodeStartUpDelay`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: If enabled, the communication will start after a delay of 250ms after transmission of the initial AddressClaimed. If disabled, communication will start immediately at start-up.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. J1939NmNodeChannelRef

- **UUID**: `ECUC:956f929c-20ba-4df4-b610-904d08dde898`
- **引用名**: `J1939NmNodeChannelRef`
- **引用类型**: REFERENCE
- **多重性**: [1..infinite]
- **目标**: `J1939NmChannel`
- **完整路径**: `/AUTOSAR/EcucDefs/J1939Nm/J1939NmConfigSet/J1939NmChannel`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the channels this node has access to.

##### 2. J1939NmChannel

**容器属性**:

- **UUID**: `ECUC:91f209de-2296-44de-bbba-934fa68478a3`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `J1939NmChannel`
- **多重性**: [1..infinite]
- **构建后可变**: true
- **多配置容器**: false

**容器描述**:

Physical CAN channel handled by J1939Nm.

###### 引用关系

此容器包含 **1** 个引用：

####### SYMBOLIC-NAME-REFERENCE 类型引用

######## 1. J1939NmComMNetworkHandleRef

- **UUID**: `ECUC:40ce4e12-8c1a-40bd-aa17-3736a1d0bcc3`
- **引用名**: `J1939NmComMNetworkHandleRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `ComMChannel`
- **完整路径**: `/AUTOSAR/EcucDefs/ComM/ComMConfigSet/ComMChannel`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the channel defined by the ComMChannel providing access to the unique channel index ComMChannelId.

###### 配置容器

本模块包含 **2** 个配置容器：

####### 1. J1939NmRxPdu

**容器属性**:

- **UUID**: `ECUC:cd6ba114-60e2-4a76-903c-9bd53ad0e9f0`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `J1939NmRxPdu`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

Contains the configuration of the I-PDU used to receive the AddressClaimed PG.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. J1939NmRxPduId

- **UUID**: `ECUC:8b5769b0-b023-4312-b133-225e768d24b9`
- **参数名**: `J1939NmRxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The I-PDU identifier used for RxIndication from CanIf.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. J1939NmRxPduRef

- **UUID**: `ECUC:b160754a-d835-49e6-947c-1bda8bfe67fd`
- **引用名**: `J1939NmRxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the Pdu object representing the I-PDU.

####### 2. J1939NmTxPdu

**容器属性**:

- **UUID**: `ECUC:5290a782-b763-461f-aefa-fd3eaf2438ec`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `J1939NmTxPdu`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

Contains the configuration of the I-PDU used to transmit the AddressClaimed PG.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. J1939NmTxPduId

- **UUID**: `ECUC:a56515cd-e693-44d6-90ad-9978da64beeb`
- **参数名**: `J1939NmTxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The I-PDU identifier used for TxConfirmation from CanIf.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. J1939NmTxPduRef

- **UUID**: `ECUC:ef0d1c92-2c51-4eda-a348-4edf6545f048`
- **引用名**: `J1939NmTxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the Pdu object representing the I-PDU.

##### 3. J1939NmRxPdu

**容器属性**:

- **UUID**: `ECUC:cd6ba114-60e2-4a76-903c-9bd53ad0e9f0`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `J1939NmRxPdu`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

Contains the configuration of the I-PDU used to receive the AddressClaimed PG.

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. J1939NmRxPduId

- **UUID**: `ECUC:8b5769b0-b023-4312-b133-225e768d24b9`
- **参数名**: `J1939NmRxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The I-PDU identifier used for RxIndication from CanIf.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. J1939NmRxPduRef

- **UUID**: `ECUC:b160754a-d835-49e6-947c-1bda8bfe67fd`
- **引用名**: `J1939NmRxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the Pdu object representing the I-PDU.

##### 4. J1939NmTxPdu

**容器属性**:

- **UUID**: `ECUC:5290a782-b763-461f-aefa-fd3eaf2438ec`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `J1939NmTxPdu`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

Contains the configuration of the I-PDU used to transmit the AddressClaimed PG.

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. J1939NmTxPduId

- **UUID**: `ECUC:a56515cd-e693-44d6-90ad-9978da64beeb`
- **参数名**: `J1939NmTxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The I-PDU identifier used for TxConfirmation from CanIf.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. J1939NmTxPduRef

- **UUID**: `ECUC:ef0d1c92-2c51-4eda-a348-4edf6545f048`
- **引用名**: `J1939NmTxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the Pdu object representing the I-PDU.

##### 5. J1939NmNode

**容器属性**:

- **UUID**: `ECUC:cccaa4c2-b5e3-40f5-8f09-e27161937982`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `J1939NmNode`
- **多重性**: [1..infinite]
- **构建后可变**: true
- **多配置容器**: false

**容器描述**:

Logical node representing one function handled by J1939Nm.

###### 参数配置

此容器包含 **12** 个参数：

####### INTEGER 类型参数

######## 1. J1939NmNodeId

- **UUID**: `ECUC:076630b4-11af-4476-92b1-8f2977197854`
- **参数名**: `J1939NmNodeId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Unique identifier of this node. May be chosen to be identical with J1939NmNodePreferredAddress, if the same address shall not be used by different nodes on different channels.

######## 2. J1939NmNodeNameECUInstance

- **UUID**: `ECUC:633b21cb-8cd9-4e4a-bd78-2f53f92c6adc`
- **参数名**: `J1939NmNodeNameECUInstance`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..7]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: ECU Instance field of the NAME of this node.

######## 3. J1939NmNodeNameFunction

- **UUID**: `ECUC:124e5383-ff69-4c92-b71d-dfd0c8567365`
- **参数名**: `J1939NmNodeNameFunction`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Function field of the NAME of this node.

######## 4. J1939NmNodeNameFunctionInstance

- **UUID**: `ECUC:20d916a0-3481-4502-bcf7-6e5ff6df7541`
- **参数名**: `J1939NmNodeNameFunctionInstance`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..31]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Function Instance field of the NAME of this node.

######## 5. J1939NmNodeNameIdentityNumber

- **UUID**: `ECUC:d1bd0d42-502e-4ccb-8e81-3a094bc92b18`
- **参数名**: `J1939NmNodeNameIdentityNumber`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..2097151]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Identity Number field of the NAME of this node.

######## 6. J1939NmNodeNameIndustryGroup

- **UUID**: `ECUC:ef2b10d3-f245-4e26-af43-d73d6b7e085c`
- **参数名**: `J1939NmNodeNameIndustryGroup`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..7]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Industry Group field of the NAME of this node.

######## 7. J1939NmNodeNameManufacturerCode

- **UUID**: `ECUC:08a5086c-3f16-4616-83b1-0a21ef16b14d`
- **参数名**: `J1939NmNodeNameManufacturerCode`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..2047]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Manufacturer Code field of the NAME of this node.

######## 8. J1939NmNodeNameVehicleSystem

- **UUID**: `ECUC:3553c17f-b620-4d8a-8917-d471a24769ac`
- **参数名**: `J1939NmNodeNameVehicleSystem`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..127]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Vehicle System field of the NAME of this node.

######## 9. J1939NmNodeNameVehicleSystemInstance

- **UUID**: `ECUC:4f775893-203a-45ec-87be-5c9f165ea17f`
- **参数名**: `J1939NmNodeNameVehicleSystemInstance`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..15]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Vehicle System Instance field of the NAME of this node.

######## 10. J1939NmNodePreferredAddress

- **UUID**: `ECUC:86331330-8cf2-4ae5-af39-f65878df134e`
- **参数名**: `J1939NmNodePreferredAddress`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..253]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Source address of this node used for address claiming.

####### BOOLEAN 类型参数

######## 1. J1939NmNodeNameArbitraryAddressCapable

- **UUID**: `ECUC:a35df279-672f-4e1b-a2bd-fd4085ad3080`
- **参数名**: `J1939NmNodeNameArbitraryAddressCapable`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Arbitrary Address Capable field of the NAME of this node.

######## 2. J1939NmNodeStartUpDelay

- **UUID**: `ECUC:3e9bfadc-80ef-467c-8488-d9d90431de26`
- **参数名**: `J1939NmNodeStartUpDelay`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: If enabled, the communication will start after a delay of 250ms after transmission of the initial AddressClaimed. If disabled, communication will start immediately at start-up.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. J1939NmNodeChannelRef

- **UUID**: `ECUC:956f929c-20ba-4df4-b610-904d08dde898`
- **引用名**: `J1939NmNodeChannelRef`
- **引用类型**: REFERENCE
- **多重性**: [1..infinite]
- **目标**: `J1939NmChannel`
- **完整路径**: `/AUTOSAR/EcucDefs/J1939Nm/J1939NmConfigSet/J1939NmChannel`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the channels this node has access to.

##### 6. J1939NmDemEventParameterRefs

**容器属性**:

- **UUID**: `ECUC:ff361e73-525a-49a7-b3e6-e74158649eaf`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `J1939NmDemEventParameterRefs`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Container for the references to DemEventParameter elements which shall be invoked using the API Dem_ReportErrorStatus in case the corresponding error occurs. The EventId is taken from the referenced DemEventParameter's DemEventId value. The standardized errors are provided in the container and can be extended by vendor specific error references.

###### 引用关系

此容器包含 **1** 个引用：

####### SYMBOLIC-NAME-REFERENCE 类型引用

######## 1. J1939NM_E_ADDRESS_LOST

- **UUID**: `ECUC:514e5619-0217-467f-98db-552dcd982e19`
- **引用名**: `J1939NM_E_ADDRESS_LOST`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `DemEventParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemConfigSet/DemEventParameter`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the DemEventParameter which shall be issued when the ECU failed to claim one of its addresses.

##### 7. J1939NmGeneral

**容器属性**:

- **UUID**: `ECUC:9129f6d0-0e81-4a68-94a3-deaeb5bc1bf2`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `J1939NmGeneral`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

Contains the general configuration parameters of the module.

###### 参数配置

此容器包含 **6** 个参数：

####### BOOLEAN 类型参数

######## 1. J1939NmDevErrorDetect

- **UUID**: `ECUC:110eb439-484b-4167-8849-b7b17156b975`
- **参数名**: `J1939NmDevErrorDetect`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Pre-processor switch for enabling development error detection support.

######## 2. J1939NmVersionInfoApi

- **UUID**: `ECUC:f152aeba-0be9-436f-94be-69acd9fd156d`
- **参数名**: `J1939NmVersionInfoApi`
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

######## 1. J1939NmMainFunctionPeriod

- **UUID**: `ECUC:ba210df4-d3f7-4491-9d59-edd0cad191bd`
- **参数名**: `J1939NmMainFunctionPeriod`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0.001..0.255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Call cycle in seconds of J1939Nm_MainFunction.

######## 2. J1939NmTxConfirmationTimeout

- **UUID**: `ECUC:ac3880f0-50f7-4954-b28f-9ba143aa5d90`
- **参数名**: `J1939NmTxConfirmationTimeout`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0..65.535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Time in seconds to wait for a confirmation after transmission of a message. The behaviour when the time elapses depends on the transmitted message.

####### STRING 类型参数

######## 1. J1939NmUserCalloutHeaderFile

- **UUID**: `ECUC:0bb57cfe-a6d3-4095-bb6d-9b2ad267c91f`
- **参数名**: `J1939NmUserCalloutHeaderFile`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Header file which is included by J1939Nm when J1939NmUserCallout is enabled. This header file must provide the prototype of the <User_AddressClaimedIndication> defined in J1939NmUserCallout.

####### FUNCTION-NAME 类型参数

######## 1. J1939NmUserCallout

- **UUID**: `ECUC:b9d1e12d-f8e7-4953-abaf-7bfd500e8518`
- **参数名**: `J1939NmUserCallout`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **函数变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Pre-processor switch for enabling the <User_AddressClaimedIndication> and defining the name of the callout function.

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

1. **J1939Nm**
