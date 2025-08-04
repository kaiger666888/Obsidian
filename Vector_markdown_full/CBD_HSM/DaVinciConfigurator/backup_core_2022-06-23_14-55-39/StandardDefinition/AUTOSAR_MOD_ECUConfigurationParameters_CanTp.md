# CanTp - 完整配置文档

*此文档由ARXML文件自动生成，采用层次化结构展示*

**生成时间**: 2025-06-16 14:51:09

## 📑 目录

- [📄 文件信息](#-文件信息)
- [🔧 模块定义](#-模块定义)
  - [CanTp](#cantp)
- [📦 包结构](#-包结构)

## 📄 文件信息

### Schema信息
- **Schema位置**: `http://autosar.org/schema/r4.0 AUTOSAR_4-0-3.xsd`
- **命名空间**: `http://autosar.org/schema/r4.0`

## 🔧 模块定义

### 1. CanTp

#### 基本信息

- **UUID**: `ECUC:ba6a8f4a-27d6-4452-8bd6-331300657557`
- **模块名称**: `CanTp`
- **多重性**: [0..1]
- **支持的变体**:
  - VARIANT-POST-BUILD
  - VARIANT-PRE-COMPILE

#### 模块描述

Configuration of the CanTp (CAN Transport Protocol) module.

#### 版本历史

共有 **1** 个版本记录：

##### 1. 版本 4.2.0

- **发布日期**: 2011-11-09
- **发布者**: AUTOSAR

*此版本无详细变更记录*

#### 配置容器

本模块包含 **15** 个配置容器：

##### 1. CanTpConfig

**容器属性**:

- **UUID**: `ECUC:bda25515-3634-4597-9be2-8d5d1405d9e7`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CanTpConfig`
- **多重性**: [1..1]
- **多配置容器**: true

**容器描述**:

This container contains the configuration parameters and sub containers of the AUTOSAR CanTp module. This container is a MultipleConfigurationContainer, i.e. this container and its sub-containers exist once per configuration set.

###### 参数配置

此容器包含 **1** 个参数：

####### FLOAT 类型参数

######## 1. CanTpMainFunctionPeriod

- **UUID**: `ECUC:9411ad02-2e5e-499f-b474-41daf0a62d3b`
- **参数名**: `CanTpMainFunctionPeriod`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0..0.255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Allow to configure the time for the MainFunction (as float in seconds). Please note: This period shall be the same as call cycle time of the periodic task were CanTp Main function is called.

###### 配置容器

本模块包含 **13** 个配置容器：

####### 1. CanTpChannel

**容器属性**:

- **UUID**: `ECUC:755e5d1d-0639-40a4-aed2-3e537d79362a`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CanTpChannel`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

This container contains the configuration parameters of the CanTp channel.

######## 参数配置

此容器包含 **1** 个参数：

######### ENUMERATION 类型参数

########## 1. CanTpChannelMode

- **UUID**: `ECUC:6a4ebc88-1ecd-4bf2-b3e5-7fa3000a974b`
- **参数名**: `CanTpChannelMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `CANTP_MODE_FULL_DUPLEX` (来源: AUTOSAR_ECUC)
  - `CANTP_MODE_HALF_DUPLEX` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The CAN Transport Layer supports half and full duplex channel modes.

######## 配置容器

本模块包含 **12** 个配置容器：

######### 1. CanTpRxNSdu

**容器属性**:

- **UUID**: `ECUC:252c3693-8f61-4fdb-bc0f-defd6a327590`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CanTpRxNSdu`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

The following parameters needs to be configured for each CAN N-SDU that the CanTp module receives via the CanTpChannel.

########## 参数配置

此容器包含 **11** 个参数：

########### INTEGER 类型参数

############ 1. CanTpBs

- **UUID**: `ECUC:9e272594-cfed-4b05-acf4-140870cfaf98`
- **参数名**: `CanTpBs`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Sets the number of N-PDUs the CanTp receiver allows the sender to send, before waiting for an authorization to continue transmission of the following N-PDUs.For further details on this parameter value see ISO 15765-2 specification.

############ 2. CanTpRxDl

- **UUID**: `ECUC:6a9438bd-0b3d-4005-9ce1-474fe7bf5d8d`
- **参数名**: `CanTpRxDl`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Data Length Code of this RxNsdu. In case of variable message length, this value indicates the minimum data length.

############ 3. CanTpRxNSduId

- **UUID**: `ECUC:3a4bcfb0-4e57-4fac-a38a-2fe13b81ba11`
- **参数名**: `CanTpRxNSduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Unique identifier user by the upper layer to call CanTp_CancelReceive, CanTp_ChangeParameter and CanTp_ReadParameter.

############ 4. CanTpRxWftMax

- **UUID**: `ECUC:690b3798-af94-47b2-bb18-c3c5dea0b89c`
- **参数名**: `CanTpRxWftMax`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter indicates how many Flow Control wait N-PDUs can be consecutively transmitted by the receiver. It is local to the node and is not transmitted inside the FC protocol data unit.

########### FLOAT 类型参数

############ 1. CanTpNar

- **UUID**: `ECUC:7f55eb6a-9157-4409-b921-d055c6043c74`
- **参数名**: `CanTpNar`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **取值范围**: [0..Inf]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Value in seconds of the N_Ar timeout. N_Ar is the time for transmission of a CAN frame (any N_PDU) on the receiver side.

############ 2. CanTpNbr

- **UUID**: `ECUC:52b014bc-5bc7-46ac-b56b-5451de79a28f`
- **参数名**: `CanTpNbr`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0..Inf]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Value in seconds of the performance requirement for (N_Br + N_Ar). N_Br is the elapsed time between the receiving indication of a FF or CF or the transmit confirmation of a FC, until the transmit request of the next FC.

############ 3. CanTpNcr

- **UUID**: `ECUC:4d6b2bf7-3aa8-47aa-9d36-57087f5352fa`
- **参数名**: `CanTpNcr`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **取值范围**: [0..Inf]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Value in seconds of the N_Cr timeout. N_Cr is the time until reception of the next Consecutive Frame N_PDU.

############ 4. CanTpSTmin

- **UUID**: `ECUC:d6287381-1914-4ab1-8da6-3ba8d004928b`
- **参数名**: `CanTpSTmin`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **取值范围**: [0..Inf]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Sets the duration of the minimum time the CanTp sender shall wait between the transmissions of two CF N-PDUs.

########### ENUMERATION 类型参数

############ 1. CanTpRxAddressingFormat

- **UUID**: `ECUC:fb78a30b-39a0-4018-8840-efb008c07a7c`
- **参数名**: `CanTpRxAddressingFormat`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `CANTP_EXTENDED` (来源: AUTOSAR_ECUC)
  - `CANTP_MIXED` (来源: AUTOSAR_ECUC)
  - `CANTP_STANDARD` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Declares which communication addressing mode is supported for this Rx N-SDU.

############ 2. CanTpRxPaddingActivation

- **UUID**: `ECUC:02a6f989-3eac-466e-b153-684542f925bc`
- **参数名**: `CanTpRxPaddingActivation`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `CANTP_OFF` (来源: AUTOSAR_ECUC)
  - `CANTP_ON` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines if the receive frame uses padding or not.

############ 3. CanTpRxTaType

- **UUID**: `ECUC:f1a0d9e6-3b2c-4a26-bcd2-356d1f5798b5`
- **参数名**: `CanTpRxTaType`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `CANTP_FUNCTIONAL` (来源: AUTOSAR_ECUC)
  - `CANTP_PHYSICAL` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Declares the communication type of this Rx N-SDU.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. CanTpRxNSduRef

- **UUID**: `ECUC:6d3d5f1b-598b-4468-9e3d-46dadb685fb2`
- **引用名**: `CanTpRxNSduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a Pdu in the COM-Stack.

########## 配置容器

本模块包含 **5** 个配置容器：

########### 1. CanTpNAe

**容器属性**:

- **UUID**: `ECUC:18b8222f-bd64-9aaf-705f-908e2a662c4d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CanTpNAe`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Contains the parameters needed to configure each RxNSdu or TxNSdu with CanTpAddressingFormat set to CanTpMixed.

############ 参数配置

此容器包含 **1** 个参数：

############# INTEGER 类型参数

############## 1. CanTpNAe

- **UUID**: `ECUC:ca4f6d74-43cf-de56-284c-f15c15991332`
- **参数名**: `CanTpNAe`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: If an RxNsdu or a TxNsdu is configured for mixed addressing

########### 2. CanTpNSa

**容器属性**:

- **UUID**: `ECUC:8ba3d8bb-3ecd-9132-3f29-4896b1409dad`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CanTpNSa`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Contains the parameters needed to configure each RxNSdu or TxNSdu with CanTpAddressingFormat set to CanTpExtended.

############ 参数配置

此容器包含 **1** 个参数：

############# INTEGER 类型参数

############## 1. CanTpNSa

- **UUID**: `ECUC:c9dd6e8d-70ce-ddc3-c92d-60ad6a671331`
- **参数名**: `CanTpNSa`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: If an RxNSdu or a TxNSdu is configured for extended addressing format, this parameter contains the transport protocol source address's value.

########### 3. CanTpNTa

**容器属性**:

- **UUID**: `ECUC:8a934eab-6a33-91e1-712b-19e06eac0399`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CanTpNTa`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

The following parameters need to be configured for each RxNsdu or TxNsdu with the CanTpAddressingFormat set to CanTpExtended.

############ 参数配置

此容器包含 **1** 个参数：

############# INTEGER 类型参数

############## 1. CanTpNTa

- **UUID**: `ECUC:16997313-3400-def4-0328-fd07f2930985`
- **参数名**: `CanTpNTa`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: If an RxNsdu or a TxNsdu is configured for extended addressing format, this parameter contains the transport protocol target address's value.

########### 4. CanTpRxNPdu

**容器属性**:

- **UUID**: `ECUC:036c8537-7034-4cc4-bafc-40765f860705`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CanTpRxNPdu`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

Used for grouping of the ID of a PDU and the Reference to a PDU.

############ 参数配置

此容器包含 **1** 个参数：

############# INTEGER 类型参数

############## 1. CanTpRxNPduId

- **UUID**: `ECUC:40262159-8c60-41ec-a8d8-981f42899648`
- **参数名**: `CanTpRxNPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The N-PDU identifier attached to the RxNsdu is identified by CanTpRxNSduId.

############ 引用关系

此容器包含 **1** 个引用：

############# REFERENCE 类型引用

############## 1. CanTpRxNPduRef

- **UUID**: `ECUC:b15ae189-a46c-4a18-be34-77f25a1d0465`
- **引用名**: `CanTpRxNPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a Pdu in the COM-Stack.

########### 5. CanTpTxFcNPdu

**容器属性**:

- **UUID**: `ECUC:4991f892-f334-4fcc-b92b-2bbca315c562`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CanTpTxFcNPdu`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Used for grouping of the ID of a PDU and the Reference to a PDU.

############ 参数配置

此容器包含 **1** 个参数：

############# INTEGER 类型参数

############## 1. CanTpTxFcNPduConfirmationPduId

- **UUID**: `ECUC:c00d752b-13ad-4699-b3be-e597181b1072`
- **参数名**: `CanTpTxFcNPduConfirmationPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Handle Id to be used by the CanIf to confirm the transmission of the CanTpTxFcNPdu to the CanIf module.

############ 引用关系

此容器包含 **1** 个引用：

############# REFERENCE 类型引用

############## 1. CanTpTxFcNPduRef

- **UUID**: `ECUC:4ea37b19-102e-4005-9da7-59e0a1f8fc4f`
- **引用名**: `CanTpTxFcNPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a Pdu in the COM-Stack.

######### 2. CanTpNAe

**容器属性**:

- **UUID**: `ECUC:18b8222f-bd64-9aaf-705f-908e2a662c4d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CanTpNAe`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Contains the parameters needed to configure each RxNSdu or TxNSdu with CanTpAddressingFormat set to CanTpMixed.

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. CanTpNAe

- **UUID**: `ECUC:ca4f6d74-43cf-de56-284c-f15c15991332`
- **参数名**: `CanTpNAe`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: If an RxNsdu or a TxNsdu is configured for mixed addressing

######### 3. CanTpNSa

**容器属性**:

- **UUID**: `ECUC:8ba3d8bb-3ecd-9132-3f29-4896b1409dad`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CanTpNSa`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Contains the parameters needed to configure each RxNSdu or TxNSdu with CanTpAddressingFormat set to CanTpExtended.

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. CanTpNSa

- **UUID**: `ECUC:c9dd6e8d-70ce-ddc3-c92d-60ad6a671331`
- **参数名**: `CanTpNSa`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: If an RxNSdu or a TxNSdu is configured for extended addressing format, this parameter contains the transport protocol source address's value.

######### 4. CanTpNTa

**容器属性**:

- **UUID**: `ECUC:8a934eab-6a33-91e1-712b-19e06eac0399`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CanTpNTa`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

The following parameters need to be configured for each RxNsdu or TxNsdu with the CanTpAddressingFormat set to CanTpExtended.

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. CanTpNTa

- **UUID**: `ECUC:16997313-3400-def4-0328-fd07f2930985`
- **参数名**: `CanTpNTa`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: If an RxNsdu or a TxNsdu is configured for extended addressing format, this parameter contains the transport protocol target address's value.

######### 5. CanTpRxNPdu

**容器属性**:

- **UUID**: `ECUC:036c8537-7034-4cc4-bafc-40765f860705`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CanTpRxNPdu`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

Used for grouping of the ID of a PDU and the Reference to a PDU.

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. CanTpRxNPduId

- **UUID**: `ECUC:40262159-8c60-41ec-a8d8-981f42899648`
- **参数名**: `CanTpRxNPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The N-PDU identifier attached to the RxNsdu is identified by CanTpRxNSduId.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. CanTpRxNPduRef

- **UUID**: `ECUC:b15ae189-a46c-4a18-be34-77f25a1d0465`
- **引用名**: `CanTpRxNPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a Pdu in the COM-Stack.

######### 6. CanTpTxFcNPdu

**容器属性**:

- **UUID**: `ECUC:4991f892-f334-4fcc-b92b-2bbca315c562`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CanTpTxFcNPdu`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Used for grouping of the ID of a PDU and the Reference to a PDU.

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. CanTpTxFcNPduConfirmationPduId

- **UUID**: `ECUC:c00d752b-13ad-4699-b3be-e597181b1072`
- **参数名**: `CanTpTxFcNPduConfirmationPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Handle Id to be used by the CanIf to confirm the transmission of the CanTpTxFcNPdu to the CanIf module.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. CanTpTxFcNPduRef

- **UUID**: `ECUC:4ea37b19-102e-4005-9da7-59e0a1f8fc4f`
- **引用名**: `CanTpTxFcNPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a Pdu in the COM-Stack.

######### 7. CanTpTxNSdu

**容器属性**:

- **UUID**: `ECUC:ae23c5cc-da8f-4952-a69e-1ac11ae31634`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CanTpTxNSdu`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

The following parameters needs to be configured for each CAN N-SDU that the CanTp module transmits via the CanTpChannel.

########## 参数配置

此容器包含 **9** 个参数：

########### INTEGER 类型参数

############ 1. CanTpTxDl

- **UUID**: `ECUC:6d465ca6-e501-4e27-b43b-ed0e00e02a21`
- **参数名**: `CanTpTxDl`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Data Length Code of this TxNsdu. In case of variable length message, this value indicates the minimum data length.

############ 2. CanTpTxNSduId

- **UUID**: `ECUC:a798e4bd-fb6c-4e1f-97eb-0b8b02f47a63`
- **参数名**: `CanTpTxNSduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Unique identifier to a structure that contains all useful information to process the transmission of a TxNsdu.

########### BOOLEAN 类型参数

############ 1. CanTpTc

- **UUID**: `ECUC:aaf45ff0-1683-409e-8948-a14484b30250`
- **参数名**: `CanTpTc`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: switch for enabling Transmit Cancellation.

########### FLOAT 类型参数

############ 1. CanTpNas

- **UUID**: `ECUC:aa8cbd96-3f51-45d3-b7dd-97df8cab52b0`
- **参数名**: `CanTpNas`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0..Inf]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Value in second of the N_As timeout. N_As is the time for transmission of a CAN frame (any N_PDU) on the part of the sender.

############ 2. CanTpNbs

- **UUID**: `ECUC:f9170c8d-c626-4740-b605-6e0984eeaaa9`
- **参数名**: `CanTpNbs`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **取值范围**: [0..Inf]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Value in seconds of the N_Bs timeout. N_Bs is the time of transmission until reception of the next Flow Control N_PDU.

############ 3. CanTpNcs

- **UUID**: `ECUC:76ef9dbd-266a-4a13-a9cc-ed92e147d5c3`
- **参数名**: `CanTpNcs`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **取值范围**: [0..Inf]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Value in seconds of the performance requirement of (N_Cs + N_As). N_Cs is the time which elapses between the transmit request of a CF N-PDU until the transmit request of the next CF N-PDU.

########### ENUMERATION 类型参数

############ 1. CanTpTxAddressingFormat

- **UUID**: `ECUC:882d2f8d-fd9d-4a01-985f-cbbb3f2874a3`
- **参数名**: `CanTpTxAddressingFormat`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `CANTP_EXTENDED` (来源: AUTOSAR_ECUC)
  - `CANTP_MIXED` (来源: AUTOSAR_ECUC)
  - `CANTP_STANDARD` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Declares which communication addressing format is supported for this TxNsdu.

############ 2. CanTpTxPaddingActivation

- **UUID**: `ECUC:bd869917-f0fd-430c-838f-18795134106d`
- **参数名**: `CanTpTxPaddingActivation`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `CANTP_OFF` (来源: AUTOSAR_ECUC)
  - `CANTP_ON` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines if the transmit frame use padding or not.

############ 3. CanTpTxTaType

- **UUID**: `ECUC:9b3c8f7b-911d-4cb9-a607-bf5f6d38bc4d`
- **参数名**: `CanTpTxTaType`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `CANTP_FUNCTIONAL` (来源: AUTOSAR_ECUC)
  - `CANTP_PHYSICAL` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Declares the communication type of this TxNsdu.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. CanTpTxNSduRef

- **UUID**: `ECUC:8c314f3c-266b-42b1-849a-b67aa94d59c9`
- **引用名**: `CanTpTxNSduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a Pdu in the COM-Stack.

########## 配置容器

本模块包含 **5** 个配置容器：

########### 1. CanTpNAe

**容器属性**:

- **UUID**: `ECUC:a1afb169-0892-9426-5aed-cc51db16ccf1`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CanTpNAe`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Contains the parameters needed to configure each RxNSdu or TxNSdu with CanTpAddressingFormat set to CanTpMixed.

############ 参数配置

此容器包含 **1** 个参数：

############# INTEGER 类型参数

############## 1. CanTpNAe

- **UUID**: `ECUC:5346fcad-8efd-d7cd-12db-2d1fc649b3d6`
- **参数名**: `CanTpNAe`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: If an RxNsdu or a TxNsdu is configured for mixed addressing

########### 2. CanTpNSa

**容器属性**:

- **UUID**: `ECUC:149b67f4-89fb-8aa9-29b7-845a61f13e51`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CanTpNSa`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Contains the parameters needed to configure each RxNSdu or TxNSdu with CanTpAddressingFormat set to CanTpExtended.

############ 参数配置

此容器包含 **1** 个参数：

############# INTEGER 类型参数

############## 1. CanTpNSa

- **UUID**: `ECUC:52d4fdc6-bbfc-d73a-b3bb-9c711b17b3d5`
- **参数名**: `CanTpNSa`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: If an RxNSdu or a TxNSdu is configured for extended addressing format, this parameter contains the transport protocol source address's value.

########### 3. CanTpNTa

**容器属性**:

- **UUID**: `ECUC:138adde4-b561-8b58-5bb9-55a41f5ca43d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CanTpNTa`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

The following parameters need to be configured for each RxNsdu or TxNsdu with the CanTpAddressingFormat set to CanTpExtended.

############ 参数配置

此容器包含 **1** 个参数：

############# INTEGER 类型参数

############## 1. CanTpNTa

- **UUID**: `ECUC:9f91024c-7f2e-d86b-edb7-38cba343aa29`
- **参数名**: `CanTpNTa`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: If an RxNsdu or a TxNsdu is configured for extended addressing format, this parameter contains the transport protocol target address's value.

########### 4. CanTpRxFcNPdu

**容器属性**:

- **UUID**: `ECUC:0f204774-e365-43f9-b770-fb106ee7ee72`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CanTpRxFcNPdu`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Used for grouping of the ID of a PDU and the Reference to a PDU.

############ 参数配置

此容器包含 **1** 个参数：

############# INTEGER 类型参数

############## 1. CanTpRxFcNPduId

- **UUID**: `ECUC:4e87ce7d-00bc-4a88-b1b5-daa96e41b0e1`
- **参数名**: `CanTpRxFcNPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: N-PDU identifier attached to the FC N-PDU of this TxNsdu identified by CanTpTxNSduId.

############ 引用关系

此容器包含 **1** 个引用：

############# REFERENCE 类型引用

############## 1. CanTpRxFcNPduRef

- **UUID**: `ECUC:1d5ecce4-71e5-44df-92a3-5411a32d0f8b`
- **引用名**: `CanTpRxFcNPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a Pdu in the COM-Stack.

########### 5. CanTpTxNPdu

**容器属性**:

- **UUID**: `ECUC:3074d8ed-ed78-4948-a3da-3d0384d43dc8`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CanTpTxNPdu`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

Used for grouping of the ID of a PDU and the Reference to a PDU.

############ 参数配置

此容器包含 **1** 个参数：

############# INTEGER 类型参数

############## 1. CanTpTxNPduConfirmationPduId

- **UUID**: `ECUC:ccbbf2b0-f1a1-4144-9c70-8d1162d42095`
- **参数名**: `CanTpTxNPduConfirmationPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Handle Id to be used by the CanIf to confirm the transmission of the CanTpTxNPdu to the CanIf module.

############ 引用关系

此容器包含 **1** 个引用：

############# REFERENCE 类型引用

############## 1. CanTpTxNPduRef

- **UUID**: `ECUC:9637f1c5-6d62-4765-9ac6-f09367865b65`
- **引用名**: `CanTpTxNPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a Pdu in the COM-Stack.

######### 8. CanTpNAe

**容器属性**:

- **UUID**: `ECUC:a1afb169-0892-9426-5aed-cc51db16ccf1`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CanTpNAe`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Contains the parameters needed to configure each RxNSdu or TxNSdu with CanTpAddressingFormat set to CanTpMixed.

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. CanTpNAe

- **UUID**: `ECUC:5346fcad-8efd-d7cd-12db-2d1fc649b3d6`
- **参数名**: `CanTpNAe`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: If an RxNsdu or a TxNsdu is configured for mixed addressing

######### 9. CanTpNSa

**容器属性**:

- **UUID**: `ECUC:149b67f4-89fb-8aa9-29b7-845a61f13e51`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CanTpNSa`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Contains the parameters needed to configure each RxNSdu or TxNSdu with CanTpAddressingFormat set to CanTpExtended.

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. CanTpNSa

- **UUID**: `ECUC:52d4fdc6-bbfc-d73a-b3bb-9c711b17b3d5`
- **参数名**: `CanTpNSa`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: If an RxNSdu or a TxNSdu is configured for extended addressing format, this parameter contains the transport protocol source address's value.

######### 10. CanTpNTa

**容器属性**:

- **UUID**: `ECUC:138adde4-b561-8b58-5bb9-55a41f5ca43d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CanTpNTa`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

The following parameters need to be configured for each RxNsdu or TxNsdu with the CanTpAddressingFormat set to CanTpExtended.

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. CanTpNTa

- **UUID**: `ECUC:9f91024c-7f2e-d86b-edb7-38cba343aa29`
- **参数名**: `CanTpNTa`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: If an RxNsdu or a TxNsdu is configured for extended addressing format, this parameter contains the transport protocol target address's value.

######### 11. CanTpRxFcNPdu

**容器属性**:

- **UUID**: `ECUC:0f204774-e365-43f9-b770-fb106ee7ee72`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CanTpRxFcNPdu`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Used for grouping of the ID of a PDU and the Reference to a PDU.

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. CanTpRxFcNPduId

- **UUID**: `ECUC:4e87ce7d-00bc-4a88-b1b5-daa96e41b0e1`
- **参数名**: `CanTpRxFcNPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: N-PDU identifier attached to the FC N-PDU of this TxNsdu identified by CanTpTxNSduId.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. CanTpRxFcNPduRef

- **UUID**: `ECUC:1d5ecce4-71e5-44df-92a3-5411a32d0f8b`
- **引用名**: `CanTpRxFcNPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a Pdu in the COM-Stack.

######### 12. CanTpTxNPdu

**容器属性**:

- **UUID**: `ECUC:3074d8ed-ed78-4948-a3da-3d0384d43dc8`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CanTpTxNPdu`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

Used for grouping of the ID of a PDU and the Reference to a PDU.

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. CanTpTxNPduConfirmationPduId

- **UUID**: `ECUC:ccbbf2b0-f1a1-4144-9c70-8d1162d42095`
- **参数名**: `CanTpTxNPduConfirmationPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Handle Id to be used by the CanIf to confirm the transmission of the CanTpTxNPdu to the CanIf module.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. CanTpTxNPduRef

- **UUID**: `ECUC:9637f1c5-6d62-4765-9ac6-f09367865b65`
- **引用名**: `CanTpTxNPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a Pdu in the COM-Stack.

####### 2. CanTpRxNSdu

**容器属性**:

- **UUID**: `ECUC:252c3693-8f61-4fdb-bc0f-defd6a327590`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CanTpRxNSdu`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

The following parameters needs to be configured for each CAN N-SDU that the CanTp module receives via the CanTpChannel.

######## 参数配置

此容器包含 **11** 个参数：

######### INTEGER 类型参数

########## 1. CanTpBs

- **UUID**: `ECUC:9e272594-cfed-4b05-acf4-140870cfaf98`
- **参数名**: `CanTpBs`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Sets the number of N-PDUs the CanTp receiver allows the sender to send, before waiting for an authorization to continue transmission of the following N-PDUs.For further details on this parameter value see ISO 15765-2 specification.

########## 2. CanTpRxDl

- **UUID**: `ECUC:6a9438bd-0b3d-4005-9ce1-474fe7bf5d8d`
- **参数名**: `CanTpRxDl`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Data Length Code of this RxNsdu. In case of variable message length, this value indicates the minimum data length.

########## 3. CanTpRxNSduId

- **UUID**: `ECUC:3a4bcfb0-4e57-4fac-a38a-2fe13b81ba11`
- **参数名**: `CanTpRxNSduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Unique identifier user by the upper layer to call CanTp_CancelReceive, CanTp_ChangeParameter and CanTp_ReadParameter.

########## 4. CanTpRxWftMax

- **UUID**: `ECUC:690b3798-af94-47b2-bb18-c3c5dea0b89c`
- **参数名**: `CanTpRxWftMax`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter indicates how many Flow Control wait N-PDUs can be consecutively transmitted by the receiver. It is local to the node and is not transmitted inside the FC protocol data unit.

######### FLOAT 类型参数

########## 1. CanTpNar

- **UUID**: `ECUC:7f55eb6a-9157-4409-b921-d055c6043c74`
- **参数名**: `CanTpNar`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **取值范围**: [0..Inf]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Value in seconds of the N_Ar timeout. N_Ar is the time for transmission of a CAN frame (any N_PDU) on the receiver side.

########## 2. CanTpNbr

- **UUID**: `ECUC:52b014bc-5bc7-46ac-b56b-5451de79a28f`
- **参数名**: `CanTpNbr`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0..Inf]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Value in seconds of the performance requirement for (N_Br + N_Ar). N_Br is the elapsed time between the receiving indication of a FF or CF or the transmit confirmation of a FC, until the transmit request of the next FC.

########## 3. CanTpNcr

- **UUID**: `ECUC:4d6b2bf7-3aa8-47aa-9d36-57087f5352fa`
- **参数名**: `CanTpNcr`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **取值范围**: [0..Inf]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Value in seconds of the N_Cr timeout. N_Cr is the time until reception of the next Consecutive Frame N_PDU.

########## 4. CanTpSTmin

- **UUID**: `ECUC:d6287381-1914-4ab1-8da6-3ba8d004928b`
- **参数名**: `CanTpSTmin`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **取值范围**: [0..Inf]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Sets the duration of the minimum time the CanTp sender shall wait between the transmissions of two CF N-PDUs.

######### ENUMERATION 类型参数

########## 1. CanTpRxAddressingFormat

- **UUID**: `ECUC:fb78a30b-39a0-4018-8840-efb008c07a7c`
- **参数名**: `CanTpRxAddressingFormat`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `CANTP_EXTENDED` (来源: AUTOSAR_ECUC)
  - `CANTP_MIXED` (来源: AUTOSAR_ECUC)
  - `CANTP_STANDARD` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Declares which communication addressing mode is supported for this Rx N-SDU.

########## 2. CanTpRxPaddingActivation

- **UUID**: `ECUC:02a6f989-3eac-466e-b153-684542f925bc`
- **参数名**: `CanTpRxPaddingActivation`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `CANTP_OFF` (来源: AUTOSAR_ECUC)
  - `CANTP_ON` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines if the receive frame uses padding or not.

########## 3. CanTpRxTaType

- **UUID**: `ECUC:f1a0d9e6-3b2c-4a26-bcd2-356d1f5798b5`
- **参数名**: `CanTpRxTaType`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `CANTP_FUNCTIONAL` (来源: AUTOSAR_ECUC)
  - `CANTP_PHYSICAL` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Declares the communication type of this Rx N-SDU.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. CanTpRxNSduRef

- **UUID**: `ECUC:6d3d5f1b-598b-4468-9e3d-46dadb685fb2`
- **引用名**: `CanTpRxNSduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a Pdu in the COM-Stack.

######## 配置容器

本模块包含 **5** 个配置容器：

######### 1. CanTpNAe

**容器属性**:

- **UUID**: `ECUC:18b8222f-bd64-9aaf-705f-908e2a662c4d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CanTpNAe`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Contains the parameters needed to configure each RxNSdu or TxNSdu with CanTpAddressingFormat set to CanTpMixed.

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. CanTpNAe

- **UUID**: `ECUC:ca4f6d74-43cf-de56-284c-f15c15991332`
- **参数名**: `CanTpNAe`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: If an RxNsdu or a TxNsdu is configured for mixed addressing

######### 2. CanTpNSa

**容器属性**:

- **UUID**: `ECUC:8ba3d8bb-3ecd-9132-3f29-4896b1409dad`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CanTpNSa`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Contains the parameters needed to configure each RxNSdu or TxNSdu with CanTpAddressingFormat set to CanTpExtended.

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. CanTpNSa

- **UUID**: `ECUC:c9dd6e8d-70ce-ddc3-c92d-60ad6a671331`
- **参数名**: `CanTpNSa`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: If an RxNSdu or a TxNSdu is configured for extended addressing format, this parameter contains the transport protocol source address's value.

######### 3. CanTpNTa

**容器属性**:

- **UUID**: `ECUC:8a934eab-6a33-91e1-712b-19e06eac0399`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CanTpNTa`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

The following parameters need to be configured for each RxNsdu or TxNsdu with the CanTpAddressingFormat set to CanTpExtended.

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. CanTpNTa

- **UUID**: `ECUC:16997313-3400-def4-0328-fd07f2930985`
- **参数名**: `CanTpNTa`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: If an RxNsdu or a TxNsdu is configured for extended addressing format, this parameter contains the transport protocol target address's value.

######### 4. CanTpRxNPdu

**容器属性**:

- **UUID**: `ECUC:036c8537-7034-4cc4-bafc-40765f860705`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CanTpRxNPdu`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

Used for grouping of the ID of a PDU and the Reference to a PDU.

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. CanTpRxNPduId

- **UUID**: `ECUC:40262159-8c60-41ec-a8d8-981f42899648`
- **参数名**: `CanTpRxNPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The N-PDU identifier attached to the RxNsdu is identified by CanTpRxNSduId.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. CanTpRxNPduRef

- **UUID**: `ECUC:b15ae189-a46c-4a18-be34-77f25a1d0465`
- **引用名**: `CanTpRxNPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a Pdu in the COM-Stack.

######### 5. CanTpTxFcNPdu

**容器属性**:

- **UUID**: `ECUC:4991f892-f334-4fcc-b92b-2bbca315c562`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CanTpTxFcNPdu`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Used for grouping of the ID of a PDU and the Reference to a PDU.

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. CanTpTxFcNPduConfirmationPduId

- **UUID**: `ECUC:c00d752b-13ad-4699-b3be-e597181b1072`
- **参数名**: `CanTpTxFcNPduConfirmationPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Handle Id to be used by the CanIf to confirm the transmission of the CanTpTxFcNPdu to the CanIf module.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. CanTpTxFcNPduRef

- **UUID**: `ECUC:4ea37b19-102e-4005-9da7-59e0a1f8fc4f`
- **引用名**: `CanTpTxFcNPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a Pdu in the COM-Stack.

####### 3. CanTpNAe

**容器属性**:

- **UUID**: `ECUC:18b8222f-bd64-9aaf-705f-908e2a662c4d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CanTpNAe`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Contains the parameters needed to configure each RxNSdu or TxNSdu with CanTpAddressingFormat set to CanTpMixed.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. CanTpNAe

- **UUID**: `ECUC:ca4f6d74-43cf-de56-284c-f15c15991332`
- **参数名**: `CanTpNAe`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: If an RxNsdu or a TxNsdu is configured for mixed addressing

####### 4. CanTpNSa

**容器属性**:

- **UUID**: `ECUC:8ba3d8bb-3ecd-9132-3f29-4896b1409dad`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CanTpNSa`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Contains the parameters needed to configure each RxNSdu or TxNSdu with CanTpAddressingFormat set to CanTpExtended.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. CanTpNSa

- **UUID**: `ECUC:c9dd6e8d-70ce-ddc3-c92d-60ad6a671331`
- **参数名**: `CanTpNSa`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: If an RxNSdu or a TxNSdu is configured for extended addressing format, this parameter contains the transport protocol source address's value.

####### 5. CanTpNTa

**容器属性**:

- **UUID**: `ECUC:8a934eab-6a33-91e1-712b-19e06eac0399`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CanTpNTa`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

The following parameters need to be configured for each RxNsdu or TxNsdu with the CanTpAddressingFormat set to CanTpExtended.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. CanTpNTa

- **UUID**: `ECUC:16997313-3400-def4-0328-fd07f2930985`
- **参数名**: `CanTpNTa`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: If an RxNsdu or a TxNsdu is configured for extended addressing format, this parameter contains the transport protocol target address's value.

####### 6. CanTpRxNPdu

**容器属性**:

- **UUID**: `ECUC:036c8537-7034-4cc4-bafc-40765f860705`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CanTpRxNPdu`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

Used for grouping of the ID of a PDU and the Reference to a PDU.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. CanTpRxNPduId

- **UUID**: `ECUC:40262159-8c60-41ec-a8d8-981f42899648`
- **参数名**: `CanTpRxNPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The N-PDU identifier attached to the RxNsdu is identified by CanTpRxNSduId.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. CanTpRxNPduRef

- **UUID**: `ECUC:b15ae189-a46c-4a18-be34-77f25a1d0465`
- **引用名**: `CanTpRxNPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a Pdu in the COM-Stack.

####### 7. CanTpTxFcNPdu

**容器属性**:

- **UUID**: `ECUC:4991f892-f334-4fcc-b92b-2bbca315c562`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CanTpTxFcNPdu`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Used for grouping of the ID of a PDU and the Reference to a PDU.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. CanTpTxFcNPduConfirmationPduId

- **UUID**: `ECUC:c00d752b-13ad-4699-b3be-e597181b1072`
- **参数名**: `CanTpTxFcNPduConfirmationPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Handle Id to be used by the CanIf to confirm the transmission of the CanTpTxFcNPdu to the CanIf module.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. CanTpTxFcNPduRef

- **UUID**: `ECUC:4ea37b19-102e-4005-9da7-59e0a1f8fc4f`
- **引用名**: `CanTpTxFcNPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a Pdu in the COM-Stack.

####### 8. CanTpTxNSdu

**容器属性**:

- **UUID**: `ECUC:ae23c5cc-da8f-4952-a69e-1ac11ae31634`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CanTpTxNSdu`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

The following parameters needs to be configured for each CAN N-SDU that the CanTp module transmits via the CanTpChannel.

######## 参数配置

此容器包含 **9** 个参数：

######### INTEGER 类型参数

########## 1. CanTpTxDl

- **UUID**: `ECUC:6d465ca6-e501-4e27-b43b-ed0e00e02a21`
- **参数名**: `CanTpTxDl`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Data Length Code of this TxNsdu. In case of variable length message, this value indicates the minimum data length.

########## 2. CanTpTxNSduId

- **UUID**: `ECUC:a798e4bd-fb6c-4e1f-97eb-0b8b02f47a63`
- **参数名**: `CanTpTxNSduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Unique identifier to a structure that contains all useful information to process the transmission of a TxNsdu.

######### BOOLEAN 类型参数

########## 1. CanTpTc

- **UUID**: `ECUC:aaf45ff0-1683-409e-8948-a14484b30250`
- **参数名**: `CanTpTc`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: switch for enabling Transmit Cancellation.

######### FLOAT 类型参数

########## 1. CanTpNas

- **UUID**: `ECUC:aa8cbd96-3f51-45d3-b7dd-97df8cab52b0`
- **参数名**: `CanTpNas`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0..Inf]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Value in second of the N_As timeout. N_As is the time for transmission of a CAN frame (any N_PDU) on the part of the sender.

########## 2. CanTpNbs

- **UUID**: `ECUC:f9170c8d-c626-4740-b605-6e0984eeaaa9`
- **参数名**: `CanTpNbs`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **取值范围**: [0..Inf]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Value in seconds of the N_Bs timeout. N_Bs is the time of transmission until reception of the next Flow Control N_PDU.

########## 3. CanTpNcs

- **UUID**: `ECUC:76ef9dbd-266a-4a13-a9cc-ed92e147d5c3`
- **参数名**: `CanTpNcs`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **取值范围**: [0..Inf]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Value in seconds of the performance requirement of (N_Cs + N_As). N_Cs is the time which elapses between the transmit request of a CF N-PDU until the transmit request of the next CF N-PDU.

######### ENUMERATION 类型参数

########## 1. CanTpTxAddressingFormat

- **UUID**: `ECUC:882d2f8d-fd9d-4a01-985f-cbbb3f2874a3`
- **参数名**: `CanTpTxAddressingFormat`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `CANTP_EXTENDED` (来源: AUTOSAR_ECUC)
  - `CANTP_MIXED` (来源: AUTOSAR_ECUC)
  - `CANTP_STANDARD` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Declares which communication addressing format is supported for this TxNsdu.

########## 2. CanTpTxPaddingActivation

- **UUID**: `ECUC:bd869917-f0fd-430c-838f-18795134106d`
- **参数名**: `CanTpTxPaddingActivation`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `CANTP_OFF` (来源: AUTOSAR_ECUC)
  - `CANTP_ON` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines if the transmit frame use padding or not.

########## 3. CanTpTxTaType

- **UUID**: `ECUC:9b3c8f7b-911d-4cb9-a607-bf5f6d38bc4d`
- **参数名**: `CanTpTxTaType`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `CANTP_FUNCTIONAL` (来源: AUTOSAR_ECUC)
  - `CANTP_PHYSICAL` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Declares the communication type of this TxNsdu.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. CanTpTxNSduRef

- **UUID**: `ECUC:8c314f3c-266b-42b1-849a-b67aa94d59c9`
- **引用名**: `CanTpTxNSduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a Pdu in the COM-Stack.

######## 配置容器

本模块包含 **5** 个配置容器：

######### 1. CanTpNAe

**容器属性**:

- **UUID**: `ECUC:a1afb169-0892-9426-5aed-cc51db16ccf1`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CanTpNAe`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Contains the parameters needed to configure each RxNSdu or TxNSdu with CanTpAddressingFormat set to CanTpMixed.

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. CanTpNAe

- **UUID**: `ECUC:5346fcad-8efd-d7cd-12db-2d1fc649b3d6`
- **参数名**: `CanTpNAe`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: If an RxNsdu or a TxNsdu is configured for mixed addressing

######### 2. CanTpNSa

**容器属性**:

- **UUID**: `ECUC:149b67f4-89fb-8aa9-29b7-845a61f13e51`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CanTpNSa`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Contains the parameters needed to configure each RxNSdu or TxNSdu with CanTpAddressingFormat set to CanTpExtended.

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. CanTpNSa

- **UUID**: `ECUC:52d4fdc6-bbfc-d73a-b3bb-9c711b17b3d5`
- **参数名**: `CanTpNSa`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: If an RxNSdu or a TxNSdu is configured for extended addressing format, this parameter contains the transport protocol source address's value.

######### 3. CanTpNTa

**容器属性**:

- **UUID**: `ECUC:138adde4-b561-8b58-5bb9-55a41f5ca43d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CanTpNTa`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

The following parameters need to be configured for each RxNsdu or TxNsdu with the CanTpAddressingFormat set to CanTpExtended.

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. CanTpNTa

- **UUID**: `ECUC:9f91024c-7f2e-d86b-edb7-38cba343aa29`
- **参数名**: `CanTpNTa`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: If an RxNsdu or a TxNsdu is configured for extended addressing format, this parameter contains the transport protocol target address's value.

######### 4. CanTpRxFcNPdu

**容器属性**:

- **UUID**: `ECUC:0f204774-e365-43f9-b770-fb106ee7ee72`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CanTpRxFcNPdu`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Used for grouping of the ID of a PDU and the Reference to a PDU.

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. CanTpRxFcNPduId

- **UUID**: `ECUC:4e87ce7d-00bc-4a88-b1b5-daa96e41b0e1`
- **参数名**: `CanTpRxFcNPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: N-PDU identifier attached to the FC N-PDU of this TxNsdu identified by CanTpTxNSduId.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. CanTpRxFcNPduRef

- **UUID**: `ECUC:1d5ecce4-71e5-44df-92a3-5411a32d0f8b`
- **引用名**: `CanTpRxFcNPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a Pdu in the COM-Stack.

######### 5. CanTpTxNPdu

**容器属性**:

- **UUID**: `ECUC:3074d8ed-ed78-4948-a3da-3d0384d43dc8`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CanTpTxNPdu`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

Used for grouping of the ID of a PDU and the Reference to a PDU.

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. CanTpTxNPduConfirmationPduId

- **UUID**: `ECUC:ccbbf2b0-f1a1-4144-9c70-8d1162d42095`
- **参数名**: `CanTpTxNPduConfirmationPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Handle Id to be used by the CanIf to confirm the transmission of the CanTpTxNPdu to the CanIf module.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. CanTpTxNPduRef

- **UUID**: `ECUC:9637f1c5-6d62-4765-9ac6-f09367865b65`
- **引用名**: `CanTpTxNPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a Pdu in the COM-Stack.

####### 9. CanTpNAe

**容器属性**:

- **UUID**: `ECUC:a1afb169-0892-9426-5aed-cc51db16ccf1`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CanTpNAe`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Contains the parameters needed to configure each RxNSdu or TxNSdu with CanTpAddressingFormat set to CanTpMixed.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. CanTpNAe

- **UUID**: `ECUC:5346fcad-8efd-d7cd-12db-2d1fc649b3d6`
- **参数名**: `CanTpNAe`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: If an RxNsdu or a TxNsdu is configured for mixed addressing

####### 10. CanTpNSa

**容器属性**:

- **UUID**: `ECUC:149b67f4-89fb-8aa9-29b7-845a61f13e51`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CanTpNSa`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Contains the parameters needed to configure each RxNSdu or TxNSdu with CanTpAddressingFormat set to CanTpExtended.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. CanTpNSa

- **UUID**: `ECUC:52d4fdc6-bbfc-d73a-b3bb-9c711b17b3d5`
- **参数名**: `CanTpNSa`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: If an RxNSdu or a TxNSdu is configured for extended addressing format, this parameter contains the transport protocol source address's value.

####### 11. CanTpNTa

**容器属性**:

- **UUID**: `ECUC:138adde4-b561-8b58-5bb9-55a41f5ca43d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CanTpNTa`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

The following parameters need to be configured for each RxNsdu or TxNsdu with the CanTpAddressingFormat set to CanTpExtended.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. CanTpNTa

- **UUID**: `ECUC:9f91024c-7f2e-d86b-edb7-38cba343aa29`
- **参数名**: `CanTpNTa`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: If an RxNsdu or a TxNsdu is configured for extended addressing format, this parameter contains the transport protocol target address's value.

####### 12. CanTpRxFcNPdu

**容器属性**:

- **UUID**: `ECUC:0f204774-e365-43f9-b770-fb106ee7ee72`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CanTpRxFcNPdu`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Used for grouping of the ID of a PDU and the Reference to a PDU.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. CanTpRxFcNPduId

- **UUID**: `ECUC:4e87ce7d-00bc-4a88-b1b5-daa96e41b0e1`
- **参数名**: `CanTpRxFcNPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: N-PDU identifier attached to the FC N-PDU of this TxNsdu identified by CanTpTxNSduId.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. CanTpRxFcNPduRef

- **UUID**: `ECUC:1d5ecce4-71e5-44df-92a3-5411a32d0f8b`
- **引用名**: `CanTpRxFcNPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a Pdu in the COM-Stack.

####### 13. CanTpTxNPdu

**容器属性**:

- **UUID**: `ECUC:3074d8ed-ed78-4948-a3da-3d0384d43dc8`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CanTpTxNPdu`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

Used for grouping of the ID of a PDU and the Reference to a PDU.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. CanTpTxNPduConfirmationPduId

- **UUID**: `ECUC:ccbbf2b0-f1a1-4144-9c70-8d1162d42095`
- **参数名**: `CanTpTxNPduConfirmationPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Handle Id to be used by the CanIf to confirm the transmission of the CanTpTxNPdu to the CanIf module.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. CanTpTxNPduRef

- **UUID**: `ECUC:9637f1c5-6d62-4765-9ac6-f09367865b65`
- **引用名**: `CanTpTxNPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a Pdu in the COM-Stack.

##### 2. CanTpChannel

**容器属性**:

- **UUID**: `ECUC:755e5d1d-0639-40a4-aed2-3e537d79362a`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CanTpChannel`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

This container contains the configuration parameters of the CanTp channel.

###### 参数配置

此容器包含 **1** 个参数：

####### ENUMERATION 类型参数

######## 1. CanTpChannelMode

- **UUID**: `ECUC:6a4ebc88-1ecd-4bf2-b3e5-7fa3000a974b`
- **参数名**: `CanTpChannelMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `CANTP_MODE_FULL_DUPLEX` (来源: AUTOSAR_ECUC)
  - `CANTP_MODE_HALF_DUPLEX` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The CAN Transport Layer supports half and full duplex channel modes.

###### 配置容器

本模块包含 **12** 个配置容器：

####### 1. CanTpRxNSdu

**容器属性**:

- **UUID**: `ECUC:252c3693-8f61-4fdb-bc0f-defd6a327590`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CanTpRxNSdu`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

The following parameters needs to be configured for each CAN N-SDU that the CanTp module receives via the CanTpChannel.

######## 参数配置

此容器包含 **11** 个参数：

######### INTEGER 类型参数

########## 1. CanTpBs

- **UUID**: `ECUC:9e272594-cfed-4b05-acf4-140870cfaf98`
- **参数名**: `CanTpBs`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Sets the number of N-PDUs the CanTp receiver allows the sender to send, before waiting for an authorization to continue transmission of the following N-PDUs.For further details on this parameter value see ISO 15765-2 specification.

########## 2. CanTpRxDl

- **UUID**: `ECUC:6a9438bd-0b3d-4005-9ce1-474fe7bf5d8d`
- **参数名**: `CanTpRxDl`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Data Length Code of this RxNsdu. In case of variable message length, this value indicates the minimum data length.

########## 3. CanTpRxNSduId

- **UUID**: `ECUC:3a4bcfb0-4e57-4fac-a38a-2fe13b81ba11`
- **参数名**: `CanTpRxNSduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Unique identifier user by the upper layer to call CanTp_CancelReceive, CanTp_ChangeParameter and CanTp_ReadParameter.

########## 4. CanTpRxWftMax

- **UUID**: `ECUC:690b3798-af94-47b2-bb18-c3c5dea0b89c`
- **参数名**: `CanTpRxWftMax`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter indicates how many Flow Control wait N-PDUs can be consecutively transmitted by the receiver. It is local to the node and is not transmitted inside the FC protocol data unit.

######### FLOAT 类型参数

########## 1. CanTpNar

- **UUID**: `ECUC:7f55eb6a-9157-4409-b921-d055c6043c74`
- **参数名**: `CanTpNar`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **取值范围**: [0..Inf]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Value in seconds of the N_Ar timeout. N_Ar is the time for transmission of a CAN frame (any N_PDU) on the receiver side.

########## 2. CanTpNbr

- **UUID**: `ECUC:52b014bc-5bc7-46ac-b56b-5451de79a28f`
- **参数名**: `CanTpNbr`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0..Inf]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Value in seconds of the performance requirement for (N_Br + N_Ar). N_Br is the elapsed time between the receiving indication of a FF or CF or the transmit confirmation of a FC, until the transmit request of the next FC.

########## 3. CanTpNcr

- **UUID**: `ECUC:4d6b2bf7-3aa8-47aa-9d36-57087f5352fa`
- **参数名**: `CanTpNcr`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **取值范围**: [0..Inf]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Value in seconds of the N_Cr timeout. N_Cr is the time until reception of the next Consecutive Frame N_PDU.

########## 4. CanTpSTmin

- **UUID**: `ECUC:d6287381-1914-4ab1-8da6-3ba8d004928b`
- **参数名**: `CanTpSTmin`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **取值范围**: [0..Inf]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Sets the duration of the minimum time the CanTp sender shall wait between the transmissions of two CF N-PDUs.

######### ENUMERATION 类型参数

########## 1. CanTpRxAddressingFormat

- **UUID**: `ECUC:fb78a30b-39a0-4018-8840-efb008c07a7c`
- **参数名**: `CanTpRxAddressingFormat`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `CANTP_EXTENDED` (来源: AUTOSAR_ECUC)
  - `CANTP_MIXED` (来源: AUTOSAR_ECUC)
  - `CANTP_STANDARD` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Declares which communication addressing mode is supported for this Rx N-SDU.

########## 2. CanTpRxPaddingActivation

- **UUID**: `ECUC:02a6f989-3eac-466e-b153-684542f925bc`
- **参数名**: `CanTpRxPaddingActivation`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `CANTP_OFF` (来源: AUTOSAR_ECUC)
  - `CANTP_ON` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines if the receive frame uses padding or not.

########## 3. CanTpRxTaType

- **UUID**: `ECUC:f1a0d9e6-3b2c-4a26-bcd2-356d1f5798b5`
- **参数名**: `CanTpRxTaType`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `CANTP_FUNCTIONAL` (来源: AUTOSAR_ECUC)
  - `CANTP_PHYSICAL` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Declares the communication type of this Rx N-SDU.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. CanTpRxNSduRef

- **UUID**: `ECUC:6d3d5f1b-598b-4468-9e3d-46dadb685fb2`
- **引用名**: `CanTpRxNSduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a Pdu in the COM-Stack.

######## 配置容器

本模块包含 **5** 个配置容器：

######### 1. CanTpNAe

**容器属性**:

- **UUID**: `ECUC:18b8222f-bd64-9aaf-705f-908e2a662c4d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CanTpNAe`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Contains the parameters needed to configure each RxNSdu or TxNSdu with CanTpAddressingFormat set to CanTpMixed.

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. CanTpNAe

- **UUID**: `ECUC:ca4f6d74-43cf-de56-284c-f15c15991332`
- **参数名**: `CanTpNAe`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: If an RxNsdu or a TxNsdu is configured for mixed addressing

######### 2. CanTpNSa

**容器属性**:

- **UUID**: `ECUC:8ba3d8bb-3ecd-9132-3f29-4896b1409dad`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CanTpNSa`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Contains the parameters needed to configure each RxNSdu or TxNSdu with CanTpAddressingFormat set to CanTpExtended.

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. CanTpNSa

- **UUID**: `ECUC:c9dd6e8d-70ce-ddc3-c92d-60ad6a671331`
- **参数名**: `CanTpNSa`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: If an RxNSdu or a TxNSdu is configured for extended addressing format, this parameter contains the transport protocol source address's value.

######### 3. CanTpNTa

**容器属性**:

- **UUID**: `ECUC:8a934eab-6a33-91e1-712b-19e06eac0399`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CanTpNTa`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

The following parameters need to be configured for each RxNsdu or TxNsdu with the CanTpAddressingFormat set to CanTpExtended.

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. CanTpNTa

- **UUID**: `ECUC:16997313-3400-def4-0328-fd07f2930985`
- **参数名**: `CanTpNTa`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: If an RxNsdu or a TxNsdu is configured for extended addressing format, this parameter contains the transport protocol target address's value.

######### 4. CanTpRxNPdu

**容器属性**:

- **UUID**: `ECUC:036c8537-7034-4cc4-bafc-40765f860705`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CanTpRxNPdu`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

Used for grouping of the ID of a PDU and the Reference to a PDU.

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. CanTpRxNPduId

- **UUID**: `ECUC:40262159-8c60-41ec-a8d8-981f42899648`
- **参数名**: `CanTpRxNPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The N-PDU identifier attached to the RxNsdu is identified by CanTpRxNSduId.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. CanTpRxNPduRef

- **UUID**: `ECUC:b15ae189-a46c-4a18-be34-77f25a1d0465`
- **引用名**: `CanTpRxNPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a Pdu in the COM-Stack.

######### 5. CanTpTxFcNPdu

**容器属性**:

- **UUID**: `ECUC:4991f892-f334-4fcc-b92b-2bbca315c562`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CanTpTxFcNPdu`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Used for grouping of the ID of a PDU and the Reference to a PDU.

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. CanTpTxFcNPduConfirmationPduId

- **UUID**: `ECUC:c00d752b-13ad-4699-b3be-e597181b1072`
- **参数名**: `CanTpTxFcNPduConfirmationPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Handle Id to be used by the CanIf to confirm the transmission of the CanTpTxFcNPdu to the CanIf module.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. CanTpTxFcNPduRef

- **UUID**: `ECUC:4ea37b19-102e-4005-9da7-59e0a1f8fc4f`
- **引用名**: `CanTpTxFcNPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a Pdu in the COM-Stack.

####### 2. CanTpNAe

**容器属性**:

- **UUID**: `ECUC:18b8222f-bd64-9aaf-705f-908e2a662c4d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CanTpNAe`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Contains the parameters needed to configure each RxNSdu or TxNSdu with CanTpAddressingFormat set to CanTpMixed.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. CanTpNAe

- **UUID**: `ECUC:ca4f6d74-43cf-de56-284c-f15c15991332`
- **参数名**: `CanTpNAe`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: If an RxNsdu or a TxNsdu is configured for mixed addressing

####### 3. CanTpNSa

**容器属性**:

- **UUID**: `ECUC:8ba3d8bb-3ecd-9132-3f29-4896b1409dad`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CanTpNSa`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Contains the parameters needed to configure each RxNSdu or TxNSdu with CanTpAddressingFormat set to CanTpExtended.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. CanTpNSa

- **UUID**: `ECUC:c9dd6e8d-70ce-ddc3-c92d-60ad6a671331`
- **参数名**: `CanTpNSa`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: If an RxNSdu or a TxNSdu is configured for extended addressing format, this parameter contains the transport protocol source address's value.

####### 4. CanTpNTa

**容器属性**:

- **UUID**: `ECUC:8a934eab-6a33-91e1-712b-19e06eac0399`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CanTpNTa`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

The following parameters need to be configured for each RxNsdu or TxNsdu with the CanTpAddressingFormat set to CanTpExtended.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. CanTpNTa

- **UUID**: `ECUC:16997313-3400-def4-0328-fd07f2930985`
- **参数名**: `CanTpNTa`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: If an RxNsdu or a TxNsdu is configured for extended addressing format, this parameter contains the transport protocol target address's value.

####### 5. CanTpRxNPdu

**容器属性**:

- **UUID**: `ECUC:036c8537-7034-4cc4-bafc-40765f860705`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CanTpRxNPdu`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

Used for grouping of the ID of a PDU and the Reference to a PDU.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. CanTpRxNPduId

- **UUID**: `ECUC:40262159-8c60-41ec-a8d8-981f42899648`
- **参数名**: `CanTpRxNPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The N-PDU identifier attached to the RxNsdu is identified by CanTpRxNSduId.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. CanTpRxNPduRef

- **UUID**: `ECUC:b15ae189-a46c-4a18-be34-77f25a1d0465`
- **引用名**: `CanTpRxNPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a Pdu in the COM-Stack.

####### 6. CanTpTxFcNPdu

**容器属性**:

- **UUID**: `ECUC:4991f892-f334-4fcc-b92b-2bbca315c562`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CanTpTxFcNPdu`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Used for grouping of the ID of a PDU and the Reference to a PDU.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. CanTpTxFcNPduConfirmationPduId

- **UUID**: `ECUC:c00d752b-13ad-4699-b3be-e597181b1072`
- **参数名**: `CanTpTxFcNPduConfirmationPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Handle Id to be used by the CanIf to confirm the transmission of the CanTpTxFcNPdu to the CanIf module.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. CanTpTxFcNPduRef

- **UUID**: `ECUC:4ea37b19-102e-4005-9da7-59e0a1f8fc4f`
- **引用名**: `CanTpTxFcNPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a Pdu in the COM-Stack.

####### 7. CanTpTxNSdu

**容器属性**:

- **UUID**: `ECUC:ae23c5cc-da8f-4952-a69e-1ac11ae31634`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CanTpTxNSdu`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

The following parameters needs to be configured for each CAN N-SDU that the CanTp module transmits via the CanTpChannel.

######## 参数配置

此容器包含 **9** 个参数：

######### INTEGER 类型参数

########## 1. CanTpTxDl

- **UUID**: `ECUC:6d465ca6-e501-4e27-b43b-ed0e00e02a21`
- **参数名**: `CanTpTxDl`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Data Length Code of this TxNsdu. In case of variable length message, this value indicates the minimum data length.

########## 2. CanTpTxNSduId

- **UUID**: `ECUC:a798e4bd-fb6c-4e1f-97eb-0b8b02f47a63`
- **参数名**: `CanTpTxNSduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Unique identifier to a structure that contains all useful information to process the transmission of a TxNsdu.

######### BOOLEAN 类型参数

########## 1. CanTpTc

- **UUID**: `ECUC:aaf45ff0-1683-409e-8948-a14484b30250`
- **参数名**: `CanTpTc`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: switch for enabling Transmit Cancellation.

######### FLOAT 类型参数

########## 1. CanTpNas

- **UUID**: `ECUC:aa8cbd96-3f51-45d3-b7dd-97df8cab52b0`
- **参数名**: `CanTpNas`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0..Inf]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Value in second of the N_As timeout. N_As is the time for transmission of a CAN frame (any N_PDU) on the part of the sender.

########## 2. CanTpNbs

- **UUID**: `ECUC:f9170c8d-c626-4740-b605-6e0984eeaaa9`
- **参数名**: `CanTpNbs`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **取值范围**: [0..Inf]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Value in seconds of the N_Bs timeout. N_Bs is the time of transmission until reception of the next Flow Control N_PDU.

########## 3. CanTpNcs

- **UUID**: `ECUC:76ef9dbd-266a-4a13-a9cc-ed92e147d5c3`
- **参数名**: `CanTpNcs`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **取值范围**: [0..Inf]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Value in seconds of the performance requirement of (N_Cs + N_As). N_Cs is the time which elapses between the transmit request of a CF N-PDU until the transmit request of the next CF N-PDU.

######### ENUMERATION 类型参数

########## 1. CanTpTxAddressingFormat

- **UUID**: `ECUC:882d2f8d-fd9d-4a01-985f-cbbb3f2874a3`
- **参数名**: `CanTpTxAddressingFormat`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `CANTP_EXTENDED` (来源: AUTOSAR_ECUC)
  - `CANTP_MIXED` (来源: AUTOSAR_ECUC)
  - `CANTP_STANDARD` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Declares which communication addressing format is supported for this TxNsdu.

########## 2. CanTpTxPaddingActivation

- **UUID**: `ECUC:bd869917-f0fd-430c-838f-18795134106d`
- **参数名**: `CanTpTxPaddingActivation`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `CANTP_OFF` (来源: AUTOSAR_ECUC)
  - `CANTP_ON` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines if the transmit frame use padding or not.

########## 3. CanTpTxTaType

- **UUID**: `ECUC:9b3c8f7b-911d-4cb9-a607-bf5f6d38bc4d`
- **参数名**: `CanTpTxTaType`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `CANTP_FUNCTIONAL` (来源: AUTOSAR_ECUC)
  - `CANTP_PHYSICAL` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Declares the communication type of this TxNsdu.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. CanTpTxNSduRef

- **UUID**: `ECUC:8c314f3c-266b-42b1-849a-b67aa94d59c9`
- **引用名**: `CanTpTxNSduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a Pdu in the COM-Stack.

######## 配置容器

本模块包含 **5** 个配置容器：

######### 1. CanTpNAe

**容器属性**:

- **UUID**: `ECUC:a1afb169-0892-9426-5aed-cc51db16ccf1`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CanTpNAe`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Contains the parameters needed to configure each RxNSdu or TxNSdu with CanTpAddressingFormat set to CanTpMixed.

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. CanTpNAe

- **UUID**: `ECUC:5346fcad-8efd-d7cd-12db-2d1fc649b3d6`
- **参数名**: `CanTpNAe`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: If an RxNsdu or a TxNsdu is configured for mixed addressing

######### 2. CanTpNSa

**容器属性**:

- **UUID**: `ECUC:149b67f4-89fb-8aa9-29b7-845a61f13e51`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CanTpNSa`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Contains the parameters needed to configure each RxNSdu or TxNSdu with CanTpAddressingFormat set to CanTpExtended.

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. CanTpNSa

- **UUID**: `ECUC:52d4fdc6-bbfc-d73a-b3bb-9c711b17b3d5`
- **参数名**: `CanTpNSa`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: If an RxNSdu or a TxNSdu is configured for extended addressing format, this parameter contains the transport protocol source address's value.

######### 3. CanTpNTa

**容器属性**:

- **UUID**: `ECUC:138adde4-b561-8b58-5bb9-55a41f5ca43d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CanTpNTa`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

The following parameters need to be configured for each RxNsdu or TxNsdu with the CanTpAddressingFormat set to CanTpExtended.

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. CanTpNTa

- **UUID**: `ECUC:9f91024c-7f2e-d86b-edb7-38cba343aa29`
- **参数名**: `CanTpNTa`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: If an RxNsdu or a TxNsdu is configured for extended addressing format, this parameter contains the transport protocol target address's value.

######### 4. CanTpRxFcNPdu

**容器属性**:

- **UUID**: `ECUC:0f204774-e365-43f9-b770-fb106ee7ee72`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CanTpRxFcNPdu`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Used for grouping of the ID of a PDU and the Reference to a PDU.

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. CanTpRxFcNPduId

- **UUID**: `ECUC:4e87ce7d-00bc-4a88-b1b5-daa96e41b0e1`
- **参数名**: `CanTpRxFcNPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: N-PDU identifier attached to the FC N-PDU of this TxNsdu identified by CanTpTxNSduId.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. CanTpRxFcNPduRef

- **UUID**: `ECUC:1d5ecce4-71e5-44df-92a3-5411a32d0f8b`
- **引用名**: `CanTpRxFcNPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a Pdu in the COM-Stack.

######### 5. CanTpTxNPdu

**容器属性**:

- **UUID**: `ECUC:3074d8ed-ed78-4948-a3da-3d0384d43dc8`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CanTpTxNPdu`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

Used for grouping of the ID of a PDU and the Reference to a PDU.

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. CanTpTxNPduConfirmationPduId

- **UUID**: `ECUC:ccbbf2b0-f1a1-4144-9c70-8d1162d42095`
- **参数名**: `CanTpTxNPduConfirmationPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Handle Id to be used by the CanIf to confirm the transmission of the CanTpTxNPdu to the CanIf module.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. CanTpTxNPduRef

- **UUID**: `ECUC:9637f1c5-6d62-4765-9ac6-f09367865b65`
- **引用名**: `CanTpTxNPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a Pdu in the COM-Stack.

####### 8. CanTpNAe

**容器属性**:

- **UUID**: `ECUC:a1afb169-0892-9426-5aed-cc51db16ccf1`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CanTpNAe`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Contains the parameters needed to configure each RxNSdu or TxNSdu with CanTpAddressingFormat set to CanTpMixed.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. CanTpNAe

- **UUID**: `ECUC:5346fcad-8efd-d7cd-12db-2d1fc649b3d6`
- **参数名**: `CanTpNAe`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: If an RxNsdu or a TxNsdu is configured for mixed addressing

####### 9. CanTpNSa

**容器属性**:

- **UUID**: `ECUC:149b67f4-89fb-8aa9-29b7-845a61f13e51`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CanTpNSa`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Contains the parameters needed to configure each RxNSdu or TxNSdu with CanTpAddressingFormat set to CanTpExtended.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. CanTpNSa

- **UUID**: `ECUC:52d4fdc6-bbfc-d73a-b3bb-9c711b17b3d5`
- **参数名**: `CanTpNSa`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: If an RxNSdu or a TxNSdu is configured for extended addressing format, this parameter contains the transport protocol source address's value.

####### 10. CanTpNTa

**容器属性**:

- **UUID**: `ECUC:138adde4-b561-8b58-5bb9-55a41f5ca43d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CanTpNTa`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

The following parameters need to be configured for each RxNsdu or TxNsdu with the CanTpAddressingFormat set to CanTpExtended.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. CanTpNTa

- **UUID**: `ECUC:9f91024c-7f2e-d86b-edb7-38cba343aa29`
- **参数名**: `CanTpNTa`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: If an RxNsdu or a TxNsdu is configured for extended addressing format, this parameter contains the transport protocol target address's value.

####### 11. CanTpRxFcNPdu

**容器属性**:

- **UUID**: `ECUC:0f204774-e365-43f9-b770-fb106ee7ee72`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CanTpRxFcNPdu`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Used for grouping of the ID of a PDU and the Reference to a PDU.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. CanTpRxFcNPduId

- **UUID**: `ECUC:4e87ce7d-00bc-4a88-b1b5-daa96e41b0e1`
- **参数名**: `CanTpRxFcNPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: N-PDU identifier attached to the FC N-PDU of this TxNsdu identified by CanTpTxNSduId.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. CanTpRxFcNPduRef

- **UUID**: `ECUC:1d5ecce4-71e5-44df-92a3-5411a32d0f8b`
- **引用名**: `CanTpRxFcNPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a Pdu in the COM-Stack.

####### 12. CanTpTxNPdu

**容器属性**:

- **UUID**: `ECUC:3074d8ed-ed78-4948-a3da-3d0384d43dc8`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CanTpTxNPdu`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

Used for grouping of the ID of a PDU and the Reference to a PDU.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. CanTpTxNPduConfirmationPduId

- **UUID**: `ECUC:ccbbf2b0-f1a1-4144-9c70-8d1162d42095`
- **参数名**: `CanTpTxNPduConfirmationPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Handle Id to be used by the CanIf to confirm the transmission of the CanTpTxNPdu to the CanIf module.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. CanTpTxNPduRef

- **UUID**: `ECUC:9637f1c5-6d62-4765-9ac6-f09367865b65`
- **引用名**: `CanTpTxNPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a Pdu in the COM-Stack.

##### 3. CanTpRxNSdu

**容器属性**:

- **UUID**: `ECUC:252c3693-8f61-4fdb-bc0f-defd6a327590`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CanTpRxNSdu`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

The following parameters needs to be configured for each CAN N-SDU that the CanTp module receives via the CanTpChannel.

###### 参数配置

此容器包含 **11** 个参数：

####### INTEGER 类型参数

######## 1. CanTpBs

- **UUID**: `ECUC:9e272594-cfed-4b05-acf4-140870cfaf98`
- **参数名**: `CanTpBs`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Sets the number of N-PDUs the CanTp receiver allows the sender to send, before waiting for an authorization to continue transmission of the following N-PDUs.For further details on this parameter value see ISO 15765-2 specification.

######## 2. CanTpRxDl

- **UUID**: `ECUC:6a9438bd-0b3d-4005-9ce1-474fe7bf5d8d`
- **参数名**: `CanTpRxDl`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Data Length Code of this RxNsdu. In case of variable message length, this value indicates the minimum data length.

######## 3. CanTpRxNSduId

- **UUID**: `ECUC:3a4bcfb0-4e57-4fac-a38a-2fe13b81ba11`
- **参数名**: `CanTpRxNSduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Unique identifier user by the upper layer to call CanTp_CancelReceive, CanTp_ChangeParameter and CanTp_ReadParameter.

######## 4. CanTpRxWftMax

- **UUID**: `ECUC:690b3798-af94-47b2-bb18-c3c5dea0b89c`
- **参数名**: `CanTpRxWftMax`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter indicates how many Flow Control wait N-PDUs can be consecutively transmitted by the receiver. It is local to the node and is not transmitted inside the FC protocol data unit.

####### FLOAT 类型参数

######## 1. CanTpNar

- **UUID**: `ECUC:7f55eb6a-9157-4409-b921-d055c6043c74`
- **参数名**: `CanTpNar`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **取值范围**: [0..Inf]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Value in seconds of the N_Ar timeout. N_Ar is the time for transmission of a CAN frame (any N_PDU) on the receiver side.

######## 2. CanTpNbr

- **UUID**: `ECUC:52b014bc-5bc7-46ac-b56b-5451de79a28f`
- **参数名**: `CanTpNbr`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0..Inf]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Value in seconds of the performance requirement for (N_Br + N_Ar). N_Br is the elapsed time between the receiving indication of a FF or CF or the transmit confirmation of a FC, until the transmit request of the next FC.

######## 3. CanTpNcr

- **UUID**: `ECUC:4d6b2bf7-3aa8-47aa-9d36-57087f5352fa`
- **参数名**: `CanTpNcr`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **取值范围**: [0..Inf]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Value in seconds of the N_Cr timeout. N_Cr is the time until reception of the next Consecutive Frame N_PDU.

######## 4. CanTpSTmin

- **UUID**: `ECUC:d6287381-1914-4ab1-8da6-3ba8d004928b`
- **参数名**: `CanTpSTmin`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **取值范围**: [0..Inf]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Sets the duration of the minimum time the CanTp sender shall wait between the transmissions of two CF N-PDUs.

####### ENUMERATION 类型参数

######## 1. CanTpRxAddressingFormat

- **UUID**: `ECUC:fb78a30b-39a0-4018-8840-efb008c07a7c`
- **参数名**: `CanTpRxAddressingFormat`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `CANTP_EXTENDED` (来源: AUTOSAR_ECUC)
  - `CANTP_MIXED` (来源: AUTOSAR_ECUC)
  - `CANTP_STANDARD` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Declares which communication addressing mode is supported for this Rx N-SDU.

######## 2. CanTpRxPaddingActivation

- **UUID**: `ECUC:02a6f989-3eac-466e-b153-684542f925bc`
- **参数名**: `CanTpRxPaddingActivation`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `CANTP_OFF` (来源: AUTOSAR_ECUC)
  - `CANTP_ON` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines if the receive frame uses padding or not.

######## 3. CanTpRxTaType

- **UUID**: `ECUC:f1a0d9e6-3b2c-4a26-bcd2-356d1f5798b5`
- **参数名**: `CanTpRxTaType`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `CANTP_FUNCTIONAL` (来源: AUTOSAR_ECUC)
  - `CANTP_PHYSICAL` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Declares the communication type of this Rx N-SDU.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. CanTpRxNSduRef

- **UUID**: `ECUC:6d3d5f1b-598b-4468-9e3d-46dadb685fb2`
- **引用名**: `CanTpRxNSduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a Pdu in the COM-Stack.

###### 配置容器

本模块包含 **5** 个配置容器：

####### 1. CanTpNAe

**容器属性**:

- **UUID**: `ECUC:18b8222f-bd64-9aaf-705f-908e2a662c4d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CanTpNAe`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Contains the parameters needed to configure each RxNSdu or TxNSdu with CanTpAddressingFormat set to CanTpMixed.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. CanTpNAe

- **UUID**: `ECUC:ca4f6d74-43cf-de56-284c-f15c15991332`
- **参数名**: `CanTpNAe`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: If an RxNsdu or a TxNsdu is configured for mixed addressing

####### 2. CanTpNSa

**容器属性**:

- **UUID**: `ECUC:8ba3d8bb-3ecd-9132-3f29-4896b1409dad`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CanTpNSa`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Contains the parameters needed to configure each RxNSdu or TxNSdu with CanTpAddressingFormat set to CanTpExtended.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. CanTpNSa

- **UUID**: `ECUC:c9dd6e8d-70ce-ddc3-c92d-60ad6a671331`
- **参数名**: `CanTpNSa`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: If an RxNSdu or a TxNSdu is configured for extended addressing format, this parameter contains the transport protocol source address's value.

####### 3. CanTpNTa

**容器属性**:

- **UUID**: `ECUC:8a934eab-6a33-91e1-712b-19e06eac0399`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CanTpNTa`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

The following parameters need to be configured for each RxNsdu or TxNsdu with the CanTpAddressingFormat set to CanTpExtended.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. CanTpNTa

- **UUID**: `ECUC:16997313-3400-def4-0328-fd07f2930985`
- **参数名**: `CanTpNTa`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: If an RxNsdu or a TxNsdu is configured for extended addressing format, this parameter contains the transport protocol target address's value.

####### 4. CanTpRxNPdu

**容器属性**:

- **UUID**: `ECUC:036c8537-7034-4cc4-bafc-40765f860705`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CanTpRxNPdu`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

Used for grouping of the ID of a PDU and the Reference to a PDU.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. CanTpRxNPduId

- **UUID**: `ECUC:40262159-8c60-41ec-a8d8-981f42899648`
- **参数名**: `CanTpRxNPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The N-PDU identifier attached to the RxNsdu is identified by CanTpRxNSduId.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. CanTpRxNPduRef

- **UUID**: `ECUC:b15ae189-a46c-4a18-be34-77f25a1d0465`
- **引用名**: `CanTpRxNPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a Pdu in the COM-Stack.

####### 5. CanTpTxFcNPdu

**容器属性**:

- **UUID**: `ECUC:4991f892-f334-4fcc-b92b-2bbca315c562`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CanTpTxFcNPdu`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Used for grouping of the ID of a PDU and the Reference to a PDU.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. CanTpTxFcNPduConfirmationPduId

- **UUID**: `ECUC:c00d752b-13ad-4699-b3be-e597181b1072`
- **参数名**: `CanTpTxFcNPduConfirmationPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Handle Id to be used by the CanIf to confirm the transmission of the CanTpTxFcNPdu to the CanIf module.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. CanTpTxFcNPduRef

- **UUID**: `ECUC:4ea37b19-102e-4005-9da7-59e0a1f8fc4f`
- **引用名**: `CanTpTxFcNPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a Pdu in the COM-Stack.

##### 4. CanTpNAe

**容器属性**:

- **UUID**: `ECUC:18b8222f-bd64-9aaf-705f-908e2a662c4d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CanTpNAe`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Contains the parameters needed to configure each RxNSdu or TxNSdu with CanTpAddressingFormat set to CanTpMixed.

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. CanTpNAe

- **UUID**: `ECUC:ca4f6d74-43cf-de56-284c-f15c15991332`
- **参数名**: `CanTpNAe`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: If an RxNsdu or a TxNsdu is configured for mixed addressing

##### 5. CanTpNSa

**容器属性**:

- **UUID**: `ECUC:8ba3d8bb-3ecd-9132-3f29-4896b1409dad`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CanTpNSa`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Contains the parameters needed to configure each RxNSdu or TxNSdu with CanTpAddressingFormat set to CanTpExtended.

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. CanTpNSa

- **UUID**: `ECUC:c9dd6e8d-70ce-ddc3-c92d-60ad6a671331`
- **参数名**: `CanTpNSa`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: If an RxNSdu or a TxNSdu is configured for extended addressing format, this parameter contains the transport protocol source address's value.

##### 6. CanTpNTa

**容器属性**:

- **UUID**: `ECUC:8a934eab-6a33-91e1-712b-19e06eac0399`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CanTpNTa`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

The following parameters need to be configured for each RxNsdu or TxNsdu with the CanTpAddressingFormat set to CanTpExtended.

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. CanTpNTa

- **UUID**: `ECUC:16997313-3400-def4-0328-fd07f2930985`
- **参数名**: `CanTpNTa`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: If an RxNsdu or a TxNsdu is configured for extended addressing format, this parameter contains the transport protocol target address's value.

##### 7. CanTpRxNPdu

**容器属性**:

- **UUID**: `ECUC:036c8537-7034-4cc4-bafc-40765f860705`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CanTpRxNPdu`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

Used for grouping of the ID of a PDU and the Reference to a PDU.

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. CanTpRxNPduId

- **UUID**: `ECUC:40262159-8c60-41ec-a8d8-981f42899648`
- **参数名**: `CanTpRxNPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The N-PDU identifier attached to the RxNsdu is identified by CanTpRxNSduId.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. CanTpRxNPduRef

- **UUID**: `ECUC:b15ae189-a46c-4a18-be34-77f25a1d0465`
- **引用名**: `CanTpRxNPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a Pdu in the COM-Stack.

##### 8. CanTpTxFcNPdu

**容器属性**:

- **UUID**: `ECUC:4991f892-f334-4fcc-b92b-2bbca315c562`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CanTpTxFcNPdu`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Used for grouping of the ID of a PDU and the Reference to a PDU.

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. CanTpTxFcNPduConfirmationPduId

- **UUID**: `ECUC:c00d752b-13ad-4699-b3be-e597181b1072`
- **参数名**: `CanTpTxFcNPduConfirmationPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Handle Id to be used by the CanIf to confirm the transmission of the CanTpTxFcNPdu to the CanIf module.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. CanTpTxFcNPduRef

- **UUID**: `ECUC:4ea37b19-102e-4005-9da7-59e0a1f8fc4f`
- **引用名**: `CanTpTxFcNPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a Pdu in the COM-Stack.

##### 9. CanTpTxNSdu

**容器属性**:

- **UUID**: `ECUC:ae23c5cc-da8f-4952-a69e-1ac11ae31634`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CanTpTxNSdu`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

The following parameters needs to be configured for each CAN N-SDU that the CanTp module transmits via the CanTpChannel.

###### 参数配置

此容器包含 **9** 个参数：

####### INTEGER 类型参数

######## 1. CanTpTxDl

- **UUID**: `ECUC:6d465ca6-e501-4e27-b43b-ed0e00e02a21`
- **参数名**: `CanTpTxDl`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Data Length Code of this TxNsdu. In case of variable length message, this value indicates the minimum data length.

######## 2. CanTpTxNSduId

- **UUID**: `ECUC:a798e4bd-fb6c-4e1f-97eb-0b8b02f47a63`
- **参数名**: `CanTpTxNSduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Unique identifier to a structure that contains all useful information to process the transmission of a TxNsdu.

####### BOOLEAN 类型参数

######## 1. CanTpTc

- **UUID**: `ECUC:aaf45ff0-1683-409e-8948-a14484b30250`
- **参数名**: `CanTpTc`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: switch for enabling Transmit Cancellation.

####### FLOAT 类型参数

######## 1. CanTpNas

- **UUID**: `ECUC:aa8cbd96-3f51-45d3-b7dd-97df8cab52b0`
- **参数名**: `CanTpNas`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0..Inf]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Value in second of the N_As timeout. N_As is the time for transmission of a CAN frame (any N_PDU) on the part of the sender.

######## 2. CanTpNbs

- **UUID**: `ECUC:f9170c8d-c626-4740-b605-6e0984eeaaa9`
- **参数名**: `CanTpNbs`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **取值范围**: [0..Inf]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Value in seconds of the N_Bs timeout. N_Bs is the time of transmission until reception of the next Flow Control N_PDU.

######## 3. CanTpNcs

- **UUID**: `ECUC:76ef9dbd-266a-4a13-a9cc-ed92e147d5c3`
- **参数名**: `CanTpNcs`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **取值范围**: [0..Inf]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Value in seconds of the performance requirement of (N_Cs + N_As). N_Cs is the time which elapses between the transmit request of a CF N-PDU until the transmit request of the next CF N-PDU.

####### ENUMERATION 类型参数

######## 1. CanTpTxAddressingFormat

- **UUID**: `ECUC:882d2f8d-fd9d-4a01-985f-cbbb3f2874a3`
- **参数名**: `CanTpTxAddressingFormat`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `CANTP_EXTENDED` (来源: AUTOSAR_ECUC)
  - `CANTP_MIXED` (来源: AUTOSAR_ECUC)
  - `CANTP_STANDARD` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Declares which communication addressing format is supported for this TxNsdu.

######## 2. CanTpTxPaddingActivation

- **UUID**: `ECUC:bd869917-f0fd-430c-838f-18795134106d`
- **参数名**: `CanTpTxPaddingActivation`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `CANTP_OFF` (来源: AUTOSAR_ECUC)
  - `CANTP_ON` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines if the transmit frame use padding or not.

######## 3. CanTpTxTaType

- **UUID**: `ECUC:9b3c8f7b-911d-4cb9-a607-bf5f6d38bc4d`
- **参数名**: `CanTpTxTaType`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `CANTP_FUNCTIONAL` (来源: AUTOSAR_ECUC)
  - `CANTP_PHYSICAL` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Declares the communication type of this TxNsdu.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. CanTpTxNSduRef

- **UUID**: `ECUC:8c314f3c-266b-42b1-849a-b67aa94d59c9`
- **引用名**: `CanTpTxNSduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a Pdu in the COM-Stack.

###### 配置容器

本模块包含 **5** 个配置容器：

####### 1. CanTpNAe

**容器属性**:

- **UUID**: `ECUC:a1afb169-0892-9426-5aed-cc51db16ccf1`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CanTpNAe`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Contains the parameters needed to configure each RxNSdu or TxNSdu with CanTpAddressingFormat set to CanTpMixed.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. CanTpNAe

- **UUID**: `ECUC:5346fcad-8efd-d7cd-12db-2d1fc649b3d6`
- **参数名**: `CanTpNAe`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: If an RxNsdu or a TxNsdu is configured for mixed addressing

####### 2. CanTpNSa

**容器属性**:

- **UUID**: `ECUC:149b67f4-89fb-8aa9-29b7-845a61f13e51`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CanTpNSa`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Contains the parameters needed to configure each RxNSdu or TxNSdu with CanTpAddressingFormat set to CanTpExtended.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. CanTpNSa

- **UUID**: `ECUC:52d4fdc6-bbfc-d73a-b3bb-9c711b17b3d5`
- **参数名**: `CanTpNSa`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: If an RxNSdu or a TxNSdu is configured for extended addressing format, this parameter contains the transport protocol source address's value.

####### 3. CanTpNTa

**容器属性**:

- **UUID**: `ECUC:138adde4-b561-8b58-5bb9-55a41f5ca43d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CanTpNTa`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

The following parameters need to be configured for each RxNsdu or TxNsdu with the CanTpAddressingFormat set to CanTpExtended.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. CanTpNTa

- **UUID**: `ECUC:9f91024c-7f2e-d86b-edb7-38cba343aa29`
- **参数名**: `CanTpNTa`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: If an RxNsdu or a TxNsdu is configured for extended addressing format, this parameter contains the transport protocol target address's value.

####### 4. CanTpRxFcNPdu

**容器属性**:

- **UUID**: `ECUC:0f204774-e365-43f9-b770-fb106ee7ee72`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CanTpRxFcNPdu`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Used for grouping of the ID of a PDU and the Reference to a PDU.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. CanTpRxFcNPduId

- **UUID**: `ECUC:4e87ce7d-00bc-4a88-b1b5-daa96e41b0e1`
- **参数名**: `CanTpRxFcNPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: N-PDU identifier attached to the FC N-PDU of this TxNsdu identified by CanTpTxNSduId.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. CanTpRxFcNPduRef

- **UUID**: `ECUC:1d5ecce4-71e5-44df-92a3-5411a32d0f8b`
- **引用名**: `CanTpRxFcNPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a Pdu in the COM-Stack.

####### 5. CanTpTxNPdu

**容器属性**:

- **UUID**: `ECUC:3074d8ed-ed78-4948-a3da-3d0384d43dc8`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CanTpTxNPdu`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

Used for grouping of the ID of a PDU and the Reference to a PDU.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. CanTpTxNPduConfirmationPduId

- **UUID**: `ECUC:ccbbf2b0-f1a1-4144-9c70-8d1162d42095`
- **参数名**: `CanTpTxNPduConfirmationPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Handle Id to be used by the CanIf to confirm the transmission of the CanTpTxNPdu to the CanIf module.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. CanTpTxNPduRef

- **UUID**: `ECUC:9637f1c5-6d62-4765-9ac6-f09367865b65`
- **引用名**: `CanTpTxNPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a Pdu in the COM-Stack.

##### 10. CanTpNAe

**容器属性**:

- **UUID**: `ECUC:a1afb169-0892-9426-5aed-cc51db16ccf1`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CanTpNAe`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Contains the parameters needed to configure each RxNSdu or TxNSdu with CanTpAddressingFormat set to CanTpMixed.

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. CanTpNAe

- **UUID**: `ECUC:5346fcad-8efd-d7cd-12db-2d1fc649b3d6`
- **参数名**: `CanTpNAe`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: If an RxNsdu or a TxNsdu is configured for mixed addressing

##### 11. CanTpNSa

**容器属性**:

- **UUID**: `ECUC:149b67f4-89fb-8aa9-29b7-845a61f13e51`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CanTpNSa`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Contains the parameters needed to configure each RxNSdu or TxNSdu with CanTpAddressingFormat set to CanTpExtended.

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. CanTpNSa

- **UUID**: `ECUC:52d4fdc6-bbfc-d73a-b3bb-9c711b17b3d5`
- **参数名**: `CanTpNSa`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: If an RxNSdu or a TxNSdu is configured for extended addressing format, this parameter contains the transport protocol source address's value.

##### 12. CanTpNTa

**容器属性**:

- **UUID**: `ECUC:138adde4-b561-8b58-5bb9-55a41f5ca43d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CanTpNTa`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

The following parameters need to be configured for each RxNsdu or TxNsdu with the CanTpAddressingFormat set to CanTpExtended.

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. CanTpNTa

- **UUID**: `ECUC:9f91024c-7f2e-d86b-edb7-38cba343aa29`
- **参数名**: `CanTpNTa`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: If an RxNsdu or a TxNsdu is configured for extended addressing format, this parameter contains the transport protocol target address's value.

##### 13. CanTpRxFcNPdu

**容器属性**:

- **UUID**: `ECUC:0f204774-e365-43f9-b770-fb106ee7ee72`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CanTpRxFcNPdu`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Used for grouping of the ID of a PDU and the Reference to a PDU.

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. CanTpRxFcNPduId

- **UUID**: `ECUC:4e87ce7d-00bc-4a88-b1b5-daa96e41b0e1`
- **参数名**: `CanTpRxFcNPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: N-PDU identifier attached to the FC N-PDU of this TxNsdu identified by CanTpTxNSduId.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. CanTpRxFcNPduRef

- **UUID**: `ECUC:1d5ecce4-71e5-44df-92a3-5411a32d0f8b`
- **引用名**: `CanTpRxFcNPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a Pdu in the COM-Stack.

##### 14. CanTpTxNPdu

**容器属性**:

- **UUID**: `ECUC:3074d8ed-ed78-4948-a3da-3d0384d43dc8`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CanTpTxNPdu`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

Used for grouping of the ID of a PDU and the Reference to a PDU.

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. CanTpTxNPduConfirmationPduId

- **UUID**: `ECUC:ccbbf2b0-f1a1-4144-9c70-8d1162d42095`
- **参数名**: `CanTpTxNPduConfirmationPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Handle Id to be used by the CanIf to confirm the transmission of the CanTpTxNPdu to the CanIf module.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. CanTpTxNPduRef

- **UUID**: `ECUC:9637f1c5-6d62-4765-9ac6-f09367865b65`
- **引用名**: `CanTpTxNPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a Pdu in the COM-Stack.

##### 15. CanTpGeneral

**容器属性**:

- **UUID**: `ECUC:738fd332-49f9-4028-a587-4dd2cf717e05`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CanTpGeneral`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

This container contains the general configuration parameters of the CanTp module.

###### 参数配置

此容器包含 **5** 个参数：

####### INTEGER 类型参数

######## 1. CanTpPaddingByte

- **UUID**: `ECUC:5fddf0b7-8088-444c-a2fa-1d8ecca9a85e`
- **参数名**: `CanTpPaddingByte`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Used for the initialization of unused bytes with a certain value

####### BOOLEAN 类型参数

######## 1. CanTpChangeParameterApi

- **UUID**: `ECUC:d4c70e88-7a39-41a2-aeea-b7bb0ae249ef`
- **参数名**: `CanTpChangeParameterApi`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter, if set to true, enables the CanTp_ChangeParameterRequest Api for this Module.

######## 2. CanTpDevErrorDetect

- **UUID**: `ECUC:d7ad678b-0f30-45a2-b3c2-dd92c02c073e`
- **参数名**: `CanTpDevErrorDetect`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Switches the Development Error Detection and Notification ON or OFF

######## 3. CanTpReadParameterApi

- **UUID**: `ECUC:000c8e11-32d9-404d-8286-f5860e874d97`
- **参数名**: `CanTpReadParameterApi`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter, if set to true, enables the CanTp_ReadParameterApi for this module.

######## 4. CanTpVersionInfoApi

- **UUID**: `ECUC:9fae5ee7-951f-4717-8197-d9fb2cda46aa`
- **参数名**: `CanTpVersionInfoApi`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The function CanTp_GetVersionInfo is configurable (On/Off) by this configuration parameter.

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

1. **CanTp**
