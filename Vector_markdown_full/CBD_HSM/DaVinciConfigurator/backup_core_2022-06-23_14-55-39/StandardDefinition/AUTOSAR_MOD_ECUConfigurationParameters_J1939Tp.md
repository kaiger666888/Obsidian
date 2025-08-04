# J1939Tp - 完整配置文档

*此文档由ARXML文件自动生成，采用层次化结构展示*

**生成时间**: 2025-06-16 14:51:23

## 📑 目录

- [📄 文件信息](#-文件信息)
- [🔧 模块定义](#-模块定义)
  - [J1939Tp](#j1939tp)
- [📦 包结构](#-包结构)

## 📄 文件信息

### Schema信息
- **Schema位置**: `http://autosar.org/schema/r4.0 AUTOSAR_4-0-3.xsd`
- **命名空间**: `http://autosar.org/schema/r4.0`

## 🔧 模块定义

### 1. J1939Tp

#### 基本信息

- **UUID**: `ECUC:ac26af59-9d17-4553-8713-c76b08a7e316`
- **模块名称**: `J1939Tp`
- **多重性**: [0..1]
- **支持的变体**:
  - VARIANT-LINK-TIME
  - VARIANT-POST-BUILD
  - VARIANT-PRE-COMPILE

#### 模块描述

Configuration of the J1939Tp (J1939 Transport Protocol) module.

#### 版本历史

共有 **1** 个版本记录：

##### 1. 版本 4.2.0

- **发布日期**: 2011-11-09
- **发布者**: AUTOSAR

*此版本无详细变更记录*

#### 配置容器

本模块包含 **17** 个配置容器：

##### 1. J1939TpConfiguration

**容器属性**:

- **UUID**: `ECUC:002a61c9-c3cf-4ef9-9d1c-551864f217f6`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `J1939TpConfiguration`
- **多重性**: [1..1]
- **多配置容器**: true

**容器描述**:

This container contains the configuration parameters and sub containers of the J1939Tp module that define the communication paths. This container is a MultipleConfigurationContainer, i.e. this container and its sub-containers exist once per configuration set.

###### 配置容器

本模块包含 **15** 个配置容器：

####### 1. J1939TpDemEventParameterRefs

**容器属性**:

- **UUID**: `ECUC:544e12d0-839b-45f8-95e4-c50af8073f51`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `J1939TpDemEventParameterRefs`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Container for the references to DemEventParameter elements which shall be passed to the API Dem_ReportErrorStatus. The EventId is taken from the referenced DemEventParameter's DemEventId value.

######## 引用关系

此容器包含 **1** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. J1939TP_E_COMMUNICATION

- **UUID**: `ECUC:bf44d30a-80f5-4bf3-be80-b9114edcc57e`
- **引用名**: `J1939TP_E_COMMUNICATION`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `DemEventParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemConfigSet/DemEventParameter`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the DemEventParameter which shall be issued after successful or unsuccessful communication.

####### 2. J1939TpRxChannel

**容器属性**:

- **UUID**: `ECUC:16037320-3130-46b8-a81e-cd187da021a2`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `J1939TpRxChannel`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

This container describes a reception channel of the J1939Tp module. One channel is used for all N-SDUs that share the same source address (SA) and the same destination address (BAM: DA = 0xFF, CMDT: DA != 0xFF).

######## 参数配置

此容器包含 **8** 个参数：

######### INTEGER 类型参数

########## 1. J1939TpRxDa

- **UUID**: `fa2babed-3d91-40f1-846f-95ffe96e4e5e`
- **参数名**: `J1939TpRxDa`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..253]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Destination address (DA) of this channel. This parameter is only required for channels with fixed DA which use N-PDUs with MetaData containing the DA.

########## 2. J1939TpRxSa

- **UUID**: `fd542cf7-dc21-4042-81b0-8087674e2b17`
- **参数名**: `J1939TpRxSa`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..253]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Source address (SA) of this channel. This parameter is only required for channels with fixed SA which use N-PDUs with MetaData.

########## 3. J1939TpRxDynamicBufferRatio

- **UUID**: `3cf066de-b179-419e-87a2-744fcb52353c`
- **参数名**: `J1939TpRxDynamicBufferRatio`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `80`
- **取值范围**: [0..100]
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Percentage of available buffer that shall be used for retry.
This parameter is only applicable when "J1939TpRxRetrySupport" and "J1939TpRxDynamicBlockCalculation" are enabled.

########## 4. J1939TpRxPacketsPerBlock

- **UUID**: `58755cd8-190a-43f1-94b5-61adb6a4cea0`
- **参数名**: `J1939TpRxPacketsPerBlock`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `16`
- **取值范围**: [1..255]
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Number of TP.DT frames the receiving J1939Tp module allows the sender to send before waiting for another TP.CM_CTS. This parameter is transmitted in the TP.CM_CTS frame, and is thus only relevant for reception of messages via CMDT. When J1939TpDynamicBlockCalculation is enabled, this parameter specifies a maximum for the calculated value. For further details on this parameter value see SAE J1939/21.

######### BOOLEAN 类型参数

########## 1. J1939TpRxCancellationSupport

- **UUID**: `1f1e7470-e748-489a-94db-be41c8ec60bb`
- **参数名**: `J1939TpRxCancellationSupport`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enable receive cancellation using the API J1939Tp_CancelReceive() for this channel.

########## 2. J1939TpRxDynamicBlockCalculation

- **UUID**: `d28437f0-66f8-4c1f-8f0f-d6a49af28a98`
- **参数名**: `J1939TpRxDynamicBlockCalculation`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enable dynamic calculation of "number of packets that can be sent" value in TP.CM_CTS, based on the size of buffers in upper layers reported via StartOfReception and CopyRxData.

########## 3. J1939TpRxRetrySupport

- **UUID**: `234cc03d-e273-4a2c-b969-746c10734b94`
- **参数名**: `J1939TpRxRetrySupport`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enable support for triggering repetition of failed transmission using TP.CM_CTS with a packet number that has already been sent. Retransmission is triggered when a sequence number is missing or a timeout occurs during reception.

######### ENUMERATION 类型参数

########## 1. J1939TpRxProtocolType

- **UUID**: `087c00ce-2ca5-431a-aac0-3d93b6345b9a`
- **参数名**: `J1939TpRxProtocolType`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `J1939TP_PROTOCOL_BAM` (来源: AUTOSAR_ECUC)
  - `J1939TP_PROTOCOL_CMDT` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Protocol type used by this channel. This parameter is only required for channels with fixed destination address.

######## 配置容器

本模块包含 **6** 个配置容器：

######### 1. J1939TpRxCmNPdu

**容器属性**:

- **UUID**: `0e9f269f-2425-49c6-92db-51f951887f71`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `J1939TpRxCmNPdu`
- **多重性**: [1..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This N-PDU represents the TP.CM frame of a J1939 transport protocol session. TP.CM is used both by BAM and CMDT to initialize the connection. For CMDT, it is also used to abort the connection.

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. J1939TpRxCmNPduId

- **UUID**: `cea0e6f8-b43e-49a7-9528-4f31b1b79b13`
- **参数名**: `J1939TpRxCmNPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - POST-BUILD: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The N-PDU identifier used for communication with CanIf.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. J1939TpRxCmNPduRef

- **UUID**: `d3e6458a-9eef-42a3-a55e-be66b0873d99`
- **引用名**: `J1939TpRxCmNPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the Pdu object representing the N-PDU.

######### 2. J1939TpRxDtNPdu

**容器属性**:

- **UUID**: `6441025b-d64d-4c52-a48d-dc66c6d68cd9`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `J1939TpRxDtNPdu`
- **多重性**: [1..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This N-PDU represents the TP.DT frame of a J1939 transport protocol session. TP.DT is used both by BAM and CMDT to transfer the contents of an N-SDU.

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. J1939TpRxDtNPduId

- **UUID**: `d0256107-6eca-41a1-9f06-8673c147626b`
- **参数名**: `J1939TpRxDtNPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - POST-BUILD: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The N-PDU identifier used for communication with CanIf.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. J1939TpRxDtNPduRef

- **UUID**: `faad0689-d34f-4c1b-b5fe-05a9921024f0`
- **引用名**: `J1939TpRxDtNPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the Pdu object representing the N-PDU.

######### 3. J1939TpRxPg

**容器属性**:

- **UUID**: `ef242648-b124-4e64-90e6-4c85a743bc88`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `J1939TpRxPg`
- **多重性**: [1..infinite]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

Parameter group received by the J1939 transport layer.

########## 参数配置

此容器包含 **2** 个参数：

########### INTEGER 类型参数

############ 1. J1939TpRxPgPGN

- **UUID**: `2990e4d3-16cd-471b-bd13-833d864cf4a8`
- **参数名**: `J1939TpRxPgPGN`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..262143]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the PGN which is represented by the N-SDU.

########### BOOLEAN 类型参数

############ 1. J1939TpRxPgDynLength

- **UUID**: `d8d3015f-5b12-40ae-b272-6abf11876ca7`
- **参数名**: `J1939TpRxPgDynLength`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This flag is set to TRUE when the N-SDU refers to a PGN with variable length.

########## 配置容器

本模块包含 **2** 个配置容器：

########### 1. J1939TpRxDirectNPdu

**容器属性**:

- **UUID**: `9811d4f5-97ad-4b38-879d-5b3c5e88efeb`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `J1939TpRxDirectNPdu`
- **多重性**: [0..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This N-PDU represents the short frame that is used for a dynamic length PGN when it has a length of less that 8 bytes.

############ 参数配置

此容器包含 **1** 个参数：

############# INTEGER 类型参数

############## 1. J1939TpRxDirectNPduId

- **UUID**: `df02e5ec-372a-49be-bfbb-82e5bb546a76`
- **参数名**: `J1939TpRxDirectNPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - POST-BUILD: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The N-PDU identifier used for communication with CanIf.

############ 引用关系

此容器包含 **1** 个引用：

############# REFERENCE 类型引用

############## 1. J1939TpRxDirectNPduRef

- **UUID**: `e3ab6d73-3e5a-4767-80f0-610688793188`
- **引用名**: `J1939TpRxDirectNPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the Pdu object representing the N-PDU.

########### 2. J1939TpRxNSdu

**容器属性**:

- **UUID**: `0a0e5ca3-338c-4c61-9cd9-fe4657783403`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `J1939TpRxNSdu`
- **多重性**: [1..infinite]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container describes the parameters that are relevant for the reception of a specific N-SDU.

############ 参数配置

此容器包含 **1** 个参数：

############# INTEGER 类型参数

############## 1. J1939TpRxNSduId

- **UUID**: `e61a101f-e475-4e66-8e78-3664742582e1`
- **参数名**: `J1939TpRxNSduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - POST-BUILD: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a unique identifier for a received N-SDU. This Id is used in the CancelReceive and ChangeParameter API call.

############ 引用关系

此容器包含 **1** 个引用：

############# REFERENCE 类型引用

############## 1. J1939TpRxNSduRef

- **UUID**: `59ea2a8e-66df-4392-a577-b41ce1fac02d`
- **引用名**: `J1939TpRxNSduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the Pdu object representing the N-SDU.

######### 4. J1939TpRxDirectNPdu

**容器属性**:

- **UUID**: `9811d4f5-97ad-4b38-879d-5b3c5e88efeb`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `J1939TpRxDirectNPdu`
- **多重性**: [0..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This N-PDU represents the short frame that is used for a dynamic length PGN when it has a length of less that 8 bytes.

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. J1939TpRxDirectNPduId

- **UUID**: `df02e5ec-372a-49be-bfbb-82e5bb546a76`
- **参数名**: `J1939TpRxDirectNPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - POST-BUILD: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The N-PDU identifier used for communication with CanIf.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. J1939TpRxDirectNPduRef

- **UUID**: `e3ab6d73-3e5a-4767-80f0-610688793188`
- **引用名**: `J1939TpRxDirectNPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the Pdu object representing the N-PDU.

######### 5. J1939TpRxNSdu

**容器属性**:

- **UUID**: `0a0e5ca3-338c-4c61-9cd9-fe4657783403`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `J1939TpRxNSdu`
- **多重性**: [1..infinite]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container describes the parameters that are relevant for the reception of a specific N-SDU.

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. J1939TpRxNSduId

- **UUID**: `e61a101f-e475-4e66-8e78-3664742582e1`
- **参数名**: `J1939TpRxNSduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - POST-BUILD: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a unique identifier for a received N-SDU. This Id is used in the CancelReceive and ChangeParameter API call.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. J1939TpRxNSduRef

- **UUID**: `59ea2a8e-66df-4392-a577-b41ce1fac02d`
- **引用名**: `J1939TpRxNSduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the Pdu object representing the N-SDU.

######### 6. J1939TpTxFcNPdu

**容器属性**:

- **UUID**: `2631be80-5fb4-41f9-9d72-43bf05246ea4`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `J1939TpTxFcNPdu`
- **多重性**: [0..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This N-PDU represents the TP.CM frame that is used in reverse direction for a J1939 transport protocol session using the CMDT protocol type. TP.CM in reverse direction is used for intermediate and final acknowledgement of received data and to abort the connection.

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. J1939TpTxFcNPduTxConfId

- **UUID**: `453d8289-b9e2-4f56-a175-451a14808e2e`
- **参数名**: `J1939TpTxFcNPduTxConfId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - POST-BUILD: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The N-PDU identifier used for Tx confirmation from CanIf.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. J1939TpTxFcNPduRef

- **UUID**: `23599edf-72bd-48de-bfd8-bd82c0c6b77a`
- **引用名**: `J1939TpTxFcNPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the Pdu object representing the N-PDU.

####### 3. J1939TpRxCmNPdu

**容器属性**:

- **UUID**: `0e9f269f-2425-49c6-92db-51f951887f71`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `J1939TpRxCmNPdu`
- **多重性**: [1..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This N-PDU represents the TP.CM frame of a J1939 transport protocol session. TP.CM is used both by BAM and CMDT to initialize the connection. For CMDT, it is also used to abort the connection.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. J1939TpRxCmNPduId

- **UUID**: `cea0e6f8-b43e-49a7-9528-4f31b1b79b13`
- **参数名**: `J1939TpRxCmNPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - POST-BUILD: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The N-PDU identifier used for communication with CanIf.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. J1939TpRxCmNPduRef

- **UUID**: `d3e6458a-9eef-42a3-a55e-be66b0873d99`
- **引用名**: `J1939TpRxCmNPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the Pdu object representing the N-PDU.

####### 4. J1939TpRxDtNPdu

**容器属性**:

- **UUID**: `6441025b-d64d-4c52-a48d-dc66c6d68cd9`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `J1939TpRxDtNPdu`
- **多重性**: [1..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This N-PDU represents the TP.DT frame of a J1939 transport protocol session. TP.DT is used both by BAM and CMDT to transfer the contents of an N-SDU.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. J1939TpRxDtNPduId

- **UUID**: `d0256107-6eca-41a1-9f06-8673c147626b`
- **参数名**: `J1939TpRxDtNPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - POST-BUILD: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The N-PDU identifier used for communication with CanIf.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. J1939TpRxDtNPduRef

- **UUID**: `faad0689-d34f-4c1b-b5fe-05a9921024f0`
- **引用名**: `J1939TpRxDtNPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the Pdu object representing the N-PDU.

####### 5. J1939TpRxPg

**容器属性**:

- **UUID**: `ef242648-b124-4e64-90e6-4c85a743bc88`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `J1939TpRxPg`
- **多重性**: [1..infinite]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

Parameter group received by the J1939 transport layer.

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. J1939TpRxPgPGN

- **UUID**: `2990e4d3-16cd-471b-bd13-833d864cf4a8`
- **参数名**: `J1939TpRxPgPGN`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..262143]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the PGN which is represented by the N-SDU.

######### BOOLEAN 类型参数

########## 1. J1939TpRxPgDynLength

- **UUID**: `d8d3015f-5b12-40ae-b272-6abf11876ca7`
- **参数名**: `J1939TpRxPgDynLength`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This flag is set to TRUE when the N-SDU refers to a PGN with variable length.

######## 配置容器

本模块包含 **2** 个配置容器：

######### 1. J1939TpRxDirectNPdu

**容器属性**:

- **UUID**: `9811d4f5-97ad-4b38-879d-5b3c5e88efeb`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `J1939TpRxDirectNPdu`
- **多重性**: [0..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This N-PDU represents the short frame that is used for a dynamic length PGN when it has a length of less that 8 bytes.

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. J1939TpRxDirectNPduId

- **UUID**: `df02e5ec-372a-49be-bfbb-82e5bb546a76`
- **参数名**: `J1939TpRxDirectNPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - POST-BUILD: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The N-PDU identifier used for communication with CanIf.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. J1939TpRxDirectNPduRef

- **UUID**: `e3ab6d73-3e5a-4767-80f0-610688793188`
- **引用名**: `J1939TpRxDirectNPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the Pdu object representing the N-PDU.

######### 2. J1939TpRxNSdu

**容器属性**:

- **UUID**: `0a0e5ca3-338c-4c61-9cd9-fe4657783403`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `J1939TpRxNSdu`
- **多重性**: [1..infinite]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container describes the parameters that are relevant for the reception of a specific N-SDU.

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. J1939TpRxNSduId

- **UUID**: `e61a101f-e475-4e66-8e78-3664742582e1`
- **参数名**: `J1939TpRxNSduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - POST-BUILD: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a unique identifier for a received N-SDU. This Id is used in the CancelReceive and ChangeParameter API call.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. J1939TpRxNSduRef

- **UUID**: `59ea2a8e-66df-4392-a577-b41ce1fac02d`
- **引用名**: `J1939TpRxNSduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the Pdu object representing the N-SDU.

####### 6. J1939TpRxDirectNPdu

**容器属性**:

- **UUID**: `9811d4f5-97ad-4b38-879d-5b3c5e88efeb`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `J1939TpRxDirectNPdu`
- **多重性**: [0..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This N-PDU represents the short frame that is used for a dynamic length PGN when it has a length of less that 8 bytes.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. J1939TpRxDirectNPduId

- **UUID**: `df02e5ec-372a-49be-bfbb-82e5bb546a76`
- **参数名**: `J1939TpRxDirectNPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - POST-BUILD: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The N-PDU identifier used for communication with CanIf.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. J1939TpRxDirectNPduRef

- **UUID**: `e3ab6d73-3e5a-4767-80f0-610688793188`
- **引用名**: `J1939TpRxDirectNPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the Pdu object representing the N-PDU.

####### 7. J1939TpRxNSdu

**容器属性**:

- **UUID**: `0a0e5ca3-338c-4c61-9cd9-fe4657783403`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `J1939TpRxNSdu`
- **多重性**: [1..infinite]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container describes the parameters that are relevant for the reception of a specific N-SDU.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. J1939TpRxNSduId

- **UUID**: `e61a101f-e475-4e66-8e78-3664742582e1`
- **参数名**: `J1939TpRxNSduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - POST-BUILD: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a unique identifier for a received N-SDU. This Id is used in the CancelReceive and ChangeParameter API call.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. J1939TpRxNSduRef

- **UUID**: `59ea2a8e-66df-4392-a577-b41ce1fac02d`
- **引用名**: `J1939TpRxNSduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the Pdu object representing the N-SDU.

####### 8. J1939TpTxFcNPdu

**容器属性**:

- **UUID**: `2631be80-5fb4-41f9-9d72-43bf05246ea4`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `J1939TpTxFcNPdu`
- **多重性**: [0..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This N-PDU represents the TP.CM frame that is used in reverse direction for a J1939 transport protocol session using the CMDT protocol type. TP.CM in reverse direction is used for intermediate and final acknowledgement of received data and to abort the connection.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. J1939TpTxFcNPduTxConfId

- **UUID**: `453d8289-b9e2-4f56-a175-451a14808e2e`
- **参数名**: `J1939TpTxFcNPduTxConfId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - POST-BUILD: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The N-PDU identifier used for Tx confirmation from CanIf.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. J1939TpTxFcNPduRef

- **UUID**: `23599edf-72bd-48de-bfd8-bd82c0c6b77a`
- **引用名**: `J1939TpTxFcNPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the Pdu object representing the N-PDU.

####### 9. J1939TpTxChannel

**容器属性**:

- **UUID**: `ECUC:4e8c4bc7-f756-452c-8473-b5e269d5e64d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `J1939TpTxChannel`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

This container describes a transmission channel of the J1939Tp module. One channel is used for all N-SDUs that share the same source address (SA) and the same destination address (BAM: DA = 0xFF, CMDT: DA != 0xFF).

######## 参数配置

此容器包含 **7** 个参数：

######### INTEGER 类型参数

########## 1. J1939TpTxDa

- **UUID**: `0e9b0bf6-3fe9-4d2d-8bb1-bdc2788d159b`
- **参数名**: `J1939TpTxDa`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..253]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Destination address (DA) of this channel. This parameter is only required for channels with fixed DA which use N-PDUs with MetaData containing the DA.

########## 2. J1939TpTxSa

- **UUID**: `d29b9fe6-3f0f-4161-9dc2-962111b83545`
- **参数名**: `J1939TpTxSa`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..253]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Source address (SA) of this channel. This parameter is only required for channels with fixed SA which use N-PDUs with MetaData.

########## 3. J1939TpTxMaxPacketsPerBlock

- **UUID**: `3b350d39-068f-4d5e-9b8e-f73143935032`
- **参数名**: `J1939TpTxMaxPacketsPerBlock`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `255`
- **取值范围**: [1..255]
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Maximum number of TP.DT frames the transmitting J1939Tp module is ready to send before waiting for another TP.CM_CTS. This parameter is transmitted in the TP.CM_RTS frame, and is thus only relevant for transmission of messages via CMDT. When J1939TpDynamicBlockCalculation is enabled, this parameter specifies a maximum for the calculated value. For further details on this parameter value see SAE J1939/21.

######### BOOLEAN 类型参数

########## 1. J1939TpTxCancellationSupport

- **UUID**: `a502790f-4fc8-434a-81c2-313f8bfca0e3`
- **参数名**: `J1939TpTxCancellationSupport`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enable transmit cancellation using the API J1939Tp_CancelTransmit() for this channel.

########## 2. J1939TpTxDynamicBlockCalculation

- **UUID**: `8938007e-29e5-456b-a6a6-b7060b61fe1d`
- **参数名**: `J1939TpTxDynamicBlockCalculation`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enable dynamic calculation of "maximum number of packets that can be sent" value in TP.CM_RTS, based on the available amount of data in upper layers reported via CopyTxData.

########## 3. J1939TpTxRetrySupport

- **UUID**: `06aff745-8ef9-434f-bf86-ae446b1f7f6e`
- **参数名**: `J1939TpTxRetrySupport`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enable support for repetition of failed transmission using TP.CM_CTS with a packet number that has already been sent. Retransmission is handled via the retry feature of PduR_J1939TpCopyTxData.

######### ENUMERATION 类型参数

########## 1. J1939TpTxProtocolType

- **UUID**: `95e81933-1f8e-417c-8fa9-061679e2b7b7`
- **参数名**: `J1939TpTxProtocolType`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `J1939TP_PROTOCOL_BAM` (来源: AUTOSAR_ECUC)
  - `J1939TP_PROTOCOL_CMDT` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Protocol type used by this channel. This parameter is only required for channels with fixed destination address.

######## 配置容器

本模块包含 **6** 个配置容器：

######### 1. J1939TpRxFcNPdu

**容器属性**:

- **UUID**: `5aa512cf-410d-4f4a-9a3c-39a338282e67`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `J1939TpRxFcNPdu`
- **多重性**: [0..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This N-PDU represents the TP.CM frame that is used in reverse direction for a J1939 transport protocol session using the CMDT protocol type. TP.CM in reverse direction is used for intermediate and final acknowledgement of received data and to abort the connection.

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. J1939TpRxFcNPduId

- **UUID**: `a9b0fbe9-1c93-455d-9956-aaa516f558fa`
- **参数名**: `J1939TpRxFcNPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - POST-BUILD: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The N-PDU identifier used for communication with CanIf.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. J1939TpRxFcNPduRef

- **UUID**: `a63fe105-2c0b-4055-99a1-1c30b947f140`
- **引用名**: `J1939TpRxFcNPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the Pdu object representing the N-PDU.

######### 2. J1939TpTxCmNPdu

**容器属性**:

- **UUID**: `0adc2c61-34e9-4518-8ec3-18eb31074cc5`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `J1939TpTxCmNPdu`
- **多重性**: [1..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This N-PDU represents the TP.CM frame of a J1939 transport protocol session. TP.CM is used both by BAM and CMDT to initialize the connection. For CMDT, it is also used to abort the connection.

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. J1939TpTxCmNPduTxConfId

- **UUID**: `f4b7c3ad-2c0c-4988-bda8-63d147a05c51`
- **参数名**: `J1939TpTxCmNPduTxConfId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - POST-BUILD: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The N-PDU identifier used for Tx confirmation from CanIf.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. J1939TpTxCmNPduRef

- **UUID**: `c9500e8c-e8d6-484c-9493-d1442fb35f74`
- **引用名**: `J1939TpTxCmNPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the Pdu object representing the N-PDU.

######### 3. J1939TpTxDtNPdu

**容器属性**:

- **UUID**: `45d64ed4-3b4d-4c5a-abb3-51c1e473c0ba`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `J1939TpTxDtNPdu`
- **多重性**: [1..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This N-PDU represents the TP.DT frame of a J1939 transport protocol session. TP.DT is used both by BAM and CMDT to transfer the contents of an N-SDU.

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. J1939TpTxDtNPduTxConfId

- **UUID**: `2c4e49a4-da98-45db-9f5f-dfac7a6f8834`
- **参数名**: `J1939TpTxDtNPduTxConfId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - POST-BUILD: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The N-PDU identifier used for Tx confirmation from CanIf.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. J1939TpTxDtNPduRef

- **UUID**: `e2affed1-1a48-412f-a840-6f84a2e8bd6e`
- **引用名**: `J1939TpTxDtNPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the Pdu object representing the N-PDU.

######### 4. J1939TpTxPg

**容器属性**:

- **UUID**: `23529746-f2de-4ed9-8594-364ae38da65a`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `J1939TpTxPg`
- **多重性**: [1..infinite]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

Parameter group transmitted by the J1939 transport layer.

########## 参数配置

此容器包含 **2** 个参数：

########### INTEGER 类型参数

############ 1. J1939TpTxPgPGN

- **UUID**: `01f7cf32-9388-43de-8483-c90604e372ad`
- **参数名**: `J1939TpTxPgPGN`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..262143]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the PGN which is represented by the N-SDU.

########### BOOLEAN 类型参数

############ 1. J1939TpTxPgDynLength

- **UUID**: `6967b20d-5ba9-436c-9c7a-f36fcbf3d58a`
- **参数名**: `J1939TpTxPgDynLength`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This flag is set to TRUE when the N-SDU refers to a PGN with variable length.

########## 配置容器

本模块包含 **2** 个配置容器：

########### 1. J1939TpTxDirectNPdu

**容器属性**:

- **UUID**: `e6ebe3a0-eae2-4545-831a-287705fd5140`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `J1939TpTxDirectNPdu`
- **多重性**: [0..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This N-PDU represents the short frame that is used for a dynamic length PGN when it has a length of less that 8 bytes.

############ 参数配置

此容器包含 **1** 个参数：

############# INTEGER 类型参数

############## 1. J1939TpTxDirectNPduTxConfId

- **UUID**: `c3456f58-feeb-4165-98ee-1ed090bfa37f`
- **参数名**: `J1939TpTxDirectNPduTxConfId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - POST-BUILD: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The N-PDU identifier used for Tx confirmation from CanIf.

############ 引用关系

此容器包含 **1** 个引用：

############# REFERENCE 类型引用

############## 1. J1939TpTxDirectNPduRef

- **UUID**: `6524c290-53d9-4e8e-857e-5d31f6d9ec3d`
- **引用名**: `J1939TpTxDirectNPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the Pdu object representing the N-PDU.

########### 2. J1939TpTxNSdu

**容器属性**:

- **UUID**: `b62d24fb-9f8b-4328-9575-f9dc0243183f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `J1939TpTxNSdu`
- **多重性**: [1..infinite]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container describes the parameters that are relevant for the transmission of a specific N-SDU.

############ 参数配置

此容器包含 **1** 个参数：

############# INTEGER 类型参数

############## 1. J1939TpTxNSduId

- **UUID**: `68d6080e-d482-444b-ad98-3027e45ff484`
- **参数名**: `J1939TpTxNSduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - POST-BUILD: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The N-SDU identifier used for communication with PduR.

############ 引用关系

此容器包含 **1** 个引用：

############# REFERENCE 类型引用

############## 1. J1939TpTxNSduRef

- **UUID**: `66259ff6-ed47-4266-8cef-331bead14f38`
- **引用名**: `J1939TpTxNSduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the Pdu object representing the N-SDU.

######### 5. J1939TpTxDirectNPdu

**容器属性**:

- **UUID**: `e6ebe3a0-eae2-4545-831a-287705fd5140`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `J1939TpTxDirectNPdu`
- **多重性**: [0..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This N-PDU represents the short frame that is used for a dynamic length PGN when it has a length of less that 8 bytes.

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. J1939TpTxDirectNPduTxConfId

- **UUID**: `c3456f58-feeb-4165-98ee-1ed090bfa37f`
- **参数名**: `J1939TpTxDirectNPduTxConfId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - POST-BUILD: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The N-PDU identifier used for Tx confirmation from CanIf.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. J1939TpTxDirectNPduRef

- **UUID**: `6524c290-53d9-4e8e-857e-5d31f6d9ec3d`
- **引用名**: `J1939TpTxDirectNPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the Pdu object representing the N-PDU.

######### 6. J1939TpTxNSdu

**容器属性**:

- **UUID**: `b62d24fb-9f8b-4328-9575-f9dc0243183f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `J1939TpTxNSdu`
- **多重性**: [1..infinite]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container describes the parameters that are relevant for the transmission of a specific N-SDU.

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. J1939TpTxNSduId

- **UUID**: `68d6080e-d482-444b-ad98-3027e45ff484`
- **参数名**: `J1939TpTxNSduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - POST-BUILD: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The N-SDU identifier used for communication with PduR.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. J1939TpTxNSduRef

- **UUID**: `66259ff6-ed47-4266-8cef-331bead14f38`
- **引用名**: `J1939TpTxNSduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the Pdu object representing the N-SDU.

####### 10. J1939TpRxFcNPdu

**容器属性**:

- **UUID**: `5aa512cf-410d-4f4a-9a3c-39a338282e67`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `J1939TpRxFcNPdu`
- **多重性**: [0..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This N-PDU represents the TP.CM frame that is used in reverse direction for a J1939 transport protocol session using the CMDT protocol type. TP.CM in reverse direction is used for intermediate and final acknowledgement of received data and to abort the connection.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. J1939TpRxFcNPduId

- **UUID**: `a9b0fbe9-1c93-455d-9956-aaa516f558fa`
- **参数名**: `J1939TpRxFcNPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - POST-BUILD: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The N-PDU identifier used for communication with CanIf.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. J1939TpRxFcNPduRef

- **UUID**: `a63fe105-2c0b-4055-99a1-1c30b947f140`
- **引用名**: `J1939TpRxFcNPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the Pdu object representing the N-PDU.

####### 11. J1939TpTxCmNPdu

**容器属性**:

- **UUID**: `0adc2c61-34e9-4518-8ec3-18eb31074cc5`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `J1939TpTxCmNPdu`
- **多重性**: [1..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This N-PDU represents the TP.CM frame of a J1939 transport protocol session. TP.CM is used both by BAM and CMDT to initialize the connection. For CMDT, it is also used to abort the connection.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. J1939TpTxCmNPduTxConfId

- **UUID**: `f4b7c3ad-2c0c-4988-bda8-63d147a05c51`
- **参数名**: `J1939TpTxCmNPduTxConfId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - POST-BUILD: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The N-PDU identifier used for Tx confirmation from CanIf.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. J1939TpTxCmNPduRef

- **UUID**: `c9500e8c-e8d6-484c-9493-d1442fb35f74`
- **引用名**: `J1939TpTxCmNPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the Pdu object representing the N-PDU.

####### 12. J1939TpTxDtNPdu

**容器属性**:

- **UUID**: `45d64ed4-3b4d-4c5a-abb3-51c1e473c0ba`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `J1939TpTxDtNPdu`
- **多重性**: [1..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This N-PDU represents the TP.DT frame of a J1939 transport protocol session. TP.DT is used both by BAM and CMDT to transfer the contents of an N-SDU.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. J1939TpTxDtNPduTxConfId

- **UUID**: `2c4e49a4-da98-45db-9f5f-dfac7a6f8834`
- **参数名**: `J1939TpTxDtNPduTxConfId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - POST-BUILD: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The N-PDU identifier used for Tx confirmation from CanIf.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. J1939TpTxDtNPduRef

- **UUID**: `e2affed1-1a48-412f-a840-6f84a2e8bd6e`
- **引用名**: `J1939TpTxDtNPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the Pdu object representing the N-PDU.

####### 13. J1939TpTxPg

**容器属性**:

- **UUID**: `23529746-f2de-4ed9-8594-364ae38da65a`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `J1939TpTxPg`
- **多重性**: [1..infinite]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

Parameter group transmitted by the J1939 transport layer.

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. J1939TpTxPgPGN

- **UUID**: `01f7cf32-9388-43de-8483-c90604e372ad`
- **参数名**: `J1939TpTxPgPGN`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..262143]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the PGN which is represented by the N-SDU.

######### BOOLEAN 类型参数

########## 1. J1939TpTxPgDynLength

- **UUID**: `6967b20d-5ba9-436c-9c7a-f36fcbf3d58a`
- **参数名**: `J1939TpTxPgDynLength`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This flag is set to TRUE when the N-SDU refers to a PGN with variable length.

######## 配置容器

本模块包含 **2** 个配置容器：

######### 1. J1939TpTxDirectNPdu

**容器属性**:

- **UUID**: `e6ebe3a0-eae2-4545-831a-287705fd5140`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `J1939TpTxDirectNPdu`
- **多重性**: [0..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This N-PDU represents the short frame that is used for a dynamic length PGN when it has a length of less that 8 bytes.

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. J1939TpTxDirectNPduTxConfId

- **UUID**: `c3456f58-feeb-4165-98ee-1ed090bfa37f`
- **参数名**: `J1939TpTxDirectNPduTxConfId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - POST-BUILD: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The N-PDU identifier used for Tx confirmation from CanIf.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. J1939TpTxDirectNPduRef

- **UUID**: `6524c290-53d9-4e8e-857e-5d31f6d9ec3d`
- **引用名**: `J1939TpTxDirectNPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the Pdu object representing the N-PDU.

######### 2. J1939TpTxNSdu

**容器属性**:

- **UUID**: `b62d24fb-9f8b-4328-9575-f9dc0243183f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `J1939TpTxNSdu`
- **多重性**: [1..infinite]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container describes the parameters that are relevant for the transmission of a specific N-SDU.

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. J1939TpTxNSduId

- **UUID**: `68d6080e-d482-444b-ad98-3027e45ff484`
- **参数名**: `J1939TpTxNSduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - POST-BUILD: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The N-SDU identifier used for communication with PduR.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. J1939TpTxNSduRef

- **UUID**: `66259ff6-ed47-4266-8cef-331bead14f38`
- **引用名**: `J1939TpTxNSduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the Pdu object representing the N-SDU.

####### 14. J1939TpTxDirectNPdu

**容器属性**:

- **UUID**: `e6ebe3a0-eae2-4545-831a-287705fd5140`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `J1939TpTxDirectNPdu`
- **多重性**: [0..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This N-PDU represents the short frame that is used for a dynamic length PGN when it has a length of less that 8 bytes.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. J1939TpTxDirectNPduTxConfId

- **UUID**: `c3456f58-feeb-4165-98ee-1ed090bfa37f`
- **参数名**: `J1939TpTxDirectNPduTxConfId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - POST-BUILD: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The N-PDU identifier used for Tx confirmation from CanIf.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. J1939TpTxDirectNPduRef

- **UUID**: `6524c290-53d9-4e8e-857e-5d31f6d9ec3d`
- **引用名**: `J1939TpTxDirectNPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the Pdu object representing the N-PDU.

####### 15. J1939TpTxNSdu

**容器属性**:

- **UUID**: `b62d24fb-9f8b-4328-9575-f9dc0243183f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `J1939TpTxNSdu`
- **多重性**: [1..infinite]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container describes the parameters that are relevant for the transmission of a specific N-SDU.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. J1939TpTxNSduId

- **UUID**: `68d6080e-d482-444b-ad98-3027e45ff484`
- **参数名**: `J1939TpTxNSduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - POST-BUILD: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The N-SDU identifier used for communication with PduR.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. J1939TpTxNSduRef

- **UUID**: `66259ff6-ed47-4266-8cef-331bead14f38`
- **引用名**: `J1939TpTxNSduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the Pdu object representing the N-SDU.

##### 2. J1939TpDemEventParameterRefs

**容器属性**:

- **UUID**: `ECUC:544e12d0-839b-45f8-95e4-c50af8073f51`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `J1939TpDemEventParameterRefs`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Container for the references to DemEventParameter elements which shall be passed to the API Dem_ReportErrorStatus. The EventId is taken from the referenced DemEventParameter's DemEventId value.

###### 引用关系

此容器包含 **1** 个引用：

####### SYMBOLIC-NAME-REFERENCE 类型引用

######## 1. J1939TP_E_COMMUNICATION

- **UUID**: `ECUC:bf44d30a-80f5-4bf3-be80-b9114edcc57e`
- **引用名**: `J1939TP_E_COMMUNICATION`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `DemEventParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemConfigSet/DemEventParameter`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the DemEventParameter which shall be issued after successful or unsuccessful communication.

##### 3. J1939TpRxChannel

**容器属性**:

- **UUID**: `ECUC:16037320-3130-46b8-a81e-cd187da021a2`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `J1939TpRxChannel`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

This container describes a reception channel of the J1939Tp module. One channel is used for all N-SDUs that share the same source address (SA) and the same destination address (BAM: DA = 0xFF, CMDT: DA != 0xFF).

###### 参数配置

此容器包含 **8** 个参数：

####### INTEGER 类型参数

######## 1. J1939TpRxDa

- **UUID**: `fa2babed-3d91-40f1-846f-95ffe96e4e5e`
- **参数名**: `J1939TpRxDa`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..253]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Destination address (DA) of this channel. This parameter is only required for channels with fixed DA which use N-PDUs with MetaData containing the DA.

######## 2. J1939TpRxSa

- **UUID**: `fd542cf7-dc21-4042-81b0-8087674e2b17`
- **参数名**: `J1939TpRxSa`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..253]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Source address (SA) of this channel. This parameter is only required for channels with fixed SA which use N-PDUs with MetaData.

######## 3. J1939TpRxDynamicBufferRatio

- **UUID**: `3cf066de-b179-419e-87a2-744fcb52353c`
- **参数名**: `J1939TpRxDynamicBufferRatio`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `80`
- **取值范围**: [0..100]
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Percentage of available buffer that shall be used for retry.
This parameter is only applicable when "J1939TpRxRetrySupport" and "J1939TpRxDynamicBlockCalculation" are enabled.

######## 4. J1939TpRxPacketsPerBlock

- **UUID**: `58755cd8-190a-43f1-94b5-61adb6a4cea0`
- **参数名**: `J1939TpRxPacketsPerBlock`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `16`
- **取值范围**: [1..255]
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Number of TP.DT frames the receiving J1939Tp module allows the sender to send before waiting for another TP.CM_CTS. This parameter is transmitted in the TP.CM_CTS frame, and is thus only relevant for reception of messages via CMDT. When J1939TpDynamicBlockCalculation is enabled, this parameter specifies a maximum for the calculated value. For further details on this parameter value see SAE J1939/21.

####### BOOLEAN 类型参数

######## 1. J1939TpRxCancellationSupport

- **UUID**: `1f1e7470-e748-489a-94db-be41c8ec60bb`
- **参数名**: `J1939TpRxCancellationSupport`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enable receive cancellation using the API J1939Tp_CancelReceive() for this channel.

######## 2. J1939TpRxDynamicBlockCalculation

- **UUID**: `d28437f0-66f8-4c1f-8f0f-d6a49af28a98`
- **参数名**: `J1939TpRxDynamicBlockCalculation`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enable dynamic calculation of "number of packets that can be sent" value in TP.CM_CTS, based on the size of buffers in upper layers reported via StartOfReception and CopyRxData.

######## 3. J1939TpRxRetrySupport

- **UUID**: `234cc03d-e273-4a2c-b969-746c10734b94`
- **参数名**: `J1939TpRxRetrySupport`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enable support for triggering repetition of failed transmission using TP.CM_CTS with a packet number that has already been sent. Retransmission is triggered when a sequence number is missing or a timeout occurs during reception.

####### ENUMERATION 类型参数

######## 1. J1939TpRxProtocolType

- **UUID**: `087c00ce-2ca5-431a-aac0-3d93b6345b9a`
- **参数名**: `J1939TpRxProtocolType`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `J1939TP_PROTOCOL_BAM` (来源: AUTOSAR_ECUC)
  - `J1939TP_PROTOCOL_CMDT` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Protocol type used by this channel. This parameter is only required for channels with fixed destination address.

###### 配置容器

本模块包含 **6** 个配置容器：

####### 1. J1939TpRxCmNPdu

**容器属性**:

- **UUID**: `0e9f269f-2425-49c6-92db-51f951887f71`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `J1939TpRxCmNPdu`
- **多重性**: [1..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This N-PDU represents the TP.CM frame of a J1939 transport protocol session. TP.CM is used both by BAM and CMDT to initialize the connection. For CMDT, it is also used to abort the connection.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. J1939TpRxCmNPduId

- **UUID**: `cea0e6f8-b43e-49a7-9528-4f31b1b79b13`
- **参数名**: `J1939TpRxCmNPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - POST-BUILD: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The N-PDU identifier used for communication with CanIf.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. J1939TpRxCmNPduRef

- **UUID**: `d3e6458a-9eef-42a3-a55e-be66b0873d99`
- **引用名**: `J1939TpRxCmNPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the Pdu object representing the N-PDU.

####### 2. J1939TpRxDtNPdu

**容器属性**:

- **UUID**: `6441025b-d64d-4c52-a48d-dc66c6d68cd9`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `J1939TpRxDtNPdu`
- **多重性**: [1..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This N-PDU represents the TP.DT frame of a J1939 transport protocol session. TP.DT is used both by BAM and CMDT to transfer the contents of an N-SDU.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. J1939TpRxDtNPduId

- **UUID**: `d0256107-6eca-41a1-9f06-8673c147626b`
- **参数名**: `J1939TpRxDtNPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - POST-BUILD: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The N-PDU identifier used for communication with CanIf.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. J1939TpRxDtNPduRef

- **UUID**: `faad0689-d34f-4c1b-b5fe-05a9921024f0`
- **引用名**: `J1939TpRxDtNPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the Pdu object representing the N-PDU.

####### 3. J1939TpRxPg

**容器属性**:

- **UUID**: `ef242648-b124-4e64-90e6-4c85a743bc88`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `J1939TpRxPg`
- **多重性**: [1..infinite]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

Parameter group received by the J1939 transport layer.

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. J1939TpRxPgPGN

- **UUID**: `2990e4d3-16cd-471b-bd13-833d864cf4a8`
- **参数名**: `J1939TpRxPgPGN`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..262143]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the PGN which is represented by the N-SDU.

######### BOOLEAN 类型参数

########## 1. J1939TpRxPgDynLength

- **UUID**: `d8d3015f-5b12-40ae-b272-6abf11876ca7`
- **参数名**: `J1939TpRxPgDynLength`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This flag is set to TRUE when the N-SDU refers to a PGN with variable length.

######## 配置容器

本模块包含 **2** 个配置容器：

######### 1. J1939TpRxDirectNPdu

**容器属性**:

- **UUID**: `9811d4f5-97ad-4b38-879d-5b3c5e88efeb`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `J1939TpRxDirectNPdu`
- **多重性**: [0..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This N-PDU represents the short frame that is used for a dynamic length PGN when it has a length of less that 8 bytes.

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. J1939TpRxDirectNPduId

- **UUID**: `df02e5ec-372a-49be-bfbb-82e5bb546a76`
- **参数名**: `J1939TpRxDirectNPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - POST-BUILD: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The N-PDU identifier used for communication with CanIf.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. J1939TpRxDirectNPduRef

- **UUID**: `e3ab6d73-3e5a-4767-80f0-610688793188`
- **引用名**: `J1939TpRxDirectNPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the Pdu object representing the N-PDU.

######### 2. J1939TpRxNSdu

**容器属性**:

- **UUID**: `0a0e5ca3-338c-4c61-9cd9-fe4657783403`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `J1939TpRxNSdu`
- **多重性**: [1..infinite]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container describes the parameters that are relevant for the reception of a specific N-SDU.

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. J1939TpRxNSduId

- **UUID**: `e61a101f-e475-4e66-8e78-3664742582e1`
- **参数名**: `J1939TpRxNSduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - POST-BUILD: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a unique identifier for a received N-SDU. This Id is used in the CancelReceive and ChangeParameter API call.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. J1939TpRxNSduRef

- **UUID**: `59ea2a8e-66df-4392-a577-b41ce1fac02d`
- **引用名**: `J1939TpRxNSduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the Pdu object representing the N-SDU.

####### 4. J1939TpRxDirectNPdu

**容器属性**:

- **UUID**: `9811d4f5-97ad-4b38-879d-5b3c5e88efeb`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `J1939TpRxDirectNPdu`
- **多重性**: [0..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This N-PDU represents the short frame that is used for a dynamic length PGN when it has a length of less that 8 bytes.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. J1939TpRxDirectNPduId

- **UUID**: `df02e5ec-372a-49be-bfbb-82e5bb546a76`
- **参数名**: `J1939TpRxDirectNPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - POST-BUILD: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The N-PDU identifier used for communication with CanIf.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. J1939TpRxDirectNPduRef

- **UUID**: `e3ab6d73-3e5a-4767-80f0-610688793188`
- **引用名**: `J1939TpRxDirectNPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the Pdu object representing the N-PDU.

####### 5. J1939TpRxNSdu

**容器属性**:

- **UUID**: `0a0e5ca3-338c-4c61-9cd9-fe4657783403`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `J1939TpRxNSdu`
- **多重性**: [1..infinite]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container describes the parameters that are relevant for the reception of a specific N-SDU.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. J1939TpRxNSduId

- **UUID**: `e61a101f-e475-4e66-8e78-3664742582e1`
- **参数名**: `J1939TpRxNSduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - POST-BUILD: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a unique identifier for a received N-SDU. This Id is used in the CancelReceive and ChangeParameter API call.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. J1939TpRxNSduRef

- **UUID**: `59ea2a8e-66df-4392-a577-b41ce1fac02d`
- **引用名**: `J1939TpRxNSduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the Pdu object representing the N-SDU.

####### 6. J1939TpTxFcNPdu

**容器属性**:

- **UUID**: `2631be80-5fb4-41f9-9d72-43bf05246ea4`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `J1939TpTxFcNPdu`
- **多重性**: [0..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This N-PDU represents the TP.CM frame that is used in reverse direction for a J1939 transport protocol session using the CMDT protocol type. TP.CM in reverse direction is used for intermediate and final acknowledgement of received data and to abort the connection.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. J1939TpTxFcNPduTxConfId

- **UUID**: `453d8289-b9e2-4f56-a175-451a14808e2e`
- **参数名**: `J1939TpTxFcNPduTxConfId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - POST-BUILD: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The N-PDU identifier used for Tx confirmation from CanIf.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. J1939TpTxFcNPduRef

- **UUID**: `23599edf-72bd-48de-bfd8-bd82c0c6b77a`
- **引用名**: `J1939TpTxFcNPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the Pdu object representing the N-PDU.

##### 4. J1939TpRxCmNPdu

**容器属性**:

- **UUID**: `0e9f269f-2425-49c6-92db-51f951887f71`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `J1939TpRxCmNPdu`
- **多重性**: [1..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This N-PDU represents the TP.CM frame of a J1939 transport protocol session. TP.CM is used both by BAM and CMDT to initialize the connection. For CMDT, it is also used to abort the connection.

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. J1939TpRxCmNPduId

- **UUID**: `cea0e6f8-b43e-49a7-9528-4f31b1b79b13`
- **参数名**: `J1939TpRxCmNPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - POST-BUILD: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The N-PDU identifier used for communication with CanIf.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. J1939TpRxCmNPduRef

- **UUID**: `d3e6458a-9eef-42a3-a55e-be66b0873d99`
- **引用名**: `J1939TpRxCmNPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the Pdu object representing the N-PDU.

##### 5. J1939TpRxDtNPdu

**容器属性**:

- **UUID**: `6441025b-d64d-4c52-a48d-dc66c6d68cd9`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `J1939TpRxDtNPdu`
- **多重性**: [1..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This N-PDU represents the TP.DT frame of a J1939 transport protocol session. TP.DT is used both by BAM and CMDT to transfer the contents of an N-SDU.

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. J1939TpRxDtNPduId

- **UUID**: `d0256107-6eca-41a1-9f06-8673c147626b`
- **参数名**: `J1939TpRxDtNPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - POST-BUILD: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The N-PDU identifier used for communication with CanIf.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. J1939TpRxDtNPduRef

- **UUID**: `faad0689-d34f-4c1b-b5fe-05a9921024f0`
- **引用名**: `J1939TpRxDtNPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the Pdu object representing the N-PDU.

##### 6. J1939TpRxPg

**容器属性**:

- **UUID**: `ef242648-b124-4e64-90e6-4c85a743bc88`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `J1939TpRxPg`
- **多重性**: [1..infinite]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

Parameter group received by the J1939 transport layer.

###### 参数配置

此容器包含 **2** 个参数：

####### INTEGER 类型参数

######## 1. J1939TpRxPgPGN

- **UUID**: `2990e4d3-16cd-471b-bd13-833d864cf4a8`
- **参数名**: `J1939TpRxPgPGN`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..262143]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the PGN which is represented by the N-SDU.

####### BOOLEAN 类型参数

######## 1. J1939TpRxPgDynLength

- **UUID**: `d8d3015f-5b12-40ae-b272-6abf11876ca7`
- **参数名**: `J1939TpRxPgDynLength`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This flag is set to TRUE when the N-SDU refers to a PGN with variable length.

###### 配置容器

本模块包含 **2** 个配置容器：

####### 1. J1939TpRxDirectNPdu

**容器属性**:

- **UUID**: `9811d4f5-97ad-4b38-879d-5b3c5e88efeb`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `J1939TpRxDirectNPdu`
- **多重性**: [0..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This N-PDU represents the short frame that is used for a dynamic length PGN when it has a length of less that 8 bytes.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. J1939TpRxDirectNPduId

- **UUID**: `df02e5ec-372a-49be-bfbb-82e5bb546a76`
- **参数名**: `J1939TpRxDirectNPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - POST-BUILD: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The N-PDU identifier used for communication with CanIf.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. J1939TpRxDirectNPduRef

- **UUID**: `e3ab6d73-3e5a-4767-80f0-610688793188`
- **引用名**: `J1939TpRxDirectNPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the Pdu object representing the N-PDU.

####### 2. J1939TpRxNSdu

**容器属性**:

- **UUID**: `0a0e5ca3-338c-4c61-9cd9-fe4657783403`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `J1939TpRxNSdu`
- **多重性**: [1..infinite]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container describes the parameters that are relevant for the reception of a specific N-SDU.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. J1939TpRxNSduId

- **UUID**: `e61a101f-e475-4e66-8e78-3664742582e1`
- **参数名**: `J1939TpRxNSduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - POST-BUILD: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a unique identifier for a received N-SDU. This Id is used in the CancelReceive and ChangeParameter API call.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. J1939TpRxNSduRef

- **UUID**: `59ea2a8e-66df-4392-a577-b41ce1fac02d`
- **引用名**: `J1939TpRxNSduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the Pdu object representing the N-SDU.

##### 7. J1939TpRxDirectNPdu

**容器属性**:

- **UUID**: `9811d4f5-97ad-4b38-879d-5b3c5e88efeb`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `J1939TpRxDirectNPdu`
- **多重性**: [0..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This N-PDU represents the short frame that is used for a dynamic length PGN when it has a length of less that 8 bytes.

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. J1939TpRxDirectNPduId

- **UUID**: `df02e5ec-372a-49be-bfbb-82e5bb546a76`
- **参数名**: `J1939TpRxDirectNPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - POST-BUILD: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The N-PDU identifier used for communication with CanIf.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. J1939TpRxDirectNPduRef

- **UUID**: `e3ab6d73-3e5a-4767-80f0-610688793188`
- **引用名**: `J1939TpRxDirectNPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the Pdu object representing the N-PDU.

##### 8. J1939TpRxNSdu

**容器属性**:

- **UUID**: `0a0e5ca3-338c-4c61-9cd9-fe4657783403`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `J1939TpRxNSdu`
- **多重性**: [1..infinite]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container describes the parameters that are relevant for the reception of a specific N-SDU.

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. J1939TpRxNSduId

- **UUID**: `e61a101f-e475-4e66-8e78-3664742582e1`
- **参数名**: `J1939TpRxNSduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - POST-BUILD: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a unique identifier for a received N-SDU. This Id is used in the CancelReceive and ChangeParameter API call.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. J1939TpRxNSduRef

- **UUID**: `59ea2a8e-66df-4392-a577-b41ce1fac02d`
- **引用名**: `J1939TpRxNSduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the Pdu object representing the N-SDU.

##### 9. J1939TpTxFcNPdu

**容器属性**:

- **UUID**: `2631be80-5fb4-41f9-9d72-43bf05246ea4`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `J1939TpTxFcNPdu`
- **多重性**: [0..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This N-PDU represents the TP.CM frame that is used in reverse direction for a J1939 transport protocol session using the CMDT protocol type. TP.CM in reverse direction is used for intermediate and final acknowledgement of received data and to abort the connection.

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. J1939TpTxFcNPduTxConfId

- **UUID**: `453d8289-b9e2-4f56-a175-451a14808e2e`
- **参数名**: `J1939TpTxFcNPduTxConfId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - POST-BUILD: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The N-PDU identifier used for Tx confirmation from CanIf.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. J1939TpTxFcNPduRef

- **UUID**: `23599edf-72bd-48de-bfd8-bd82c0c6b77a`
- **引用名**: `J1939TpTxFcNPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the Pdu object representing the N-PDU.

##### 10. J1939TpTxChannel

**容器属性**:

- **UUID**: `ECUC:4e8c4bc7-f756-452c-8473-b5e269d5e64d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `J1939TpTxChannel`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

This container describes a transmission channel of the J1939Tp module. One channel is used for all N-SDUs that share the same source address (SA) and the same destination address (BAM: DA = 0xFF, CMDT: DA != 0xFF).

###### 参数配置

此容器包含 **7** 个参数：

####### INTEGER 类型参数

######## 1. J1939TpTxDa

- **UUID**: `0e9b0bf6-3fe9-4d2d-8bb1-bdc2788d159b`
- **参数名**: `J1939TpTxDa`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..253]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Destination address (DA) of this channel. This parameter is only required for channels with fixed DA which use N-PDUs with MetaData containing the DA.

######## 2. J1939TpTxSa

- **UUID**: `d29b9fe6-3f0f-4161-9dc2-962111b83545`
- **参数名**: `J1939TpTxSa`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..253]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Source address (SA) of this channel. This parameter is only required for channels with fixed SA which use N-PDUs with MetaData.

######## 3. J1939TpTxMaxPacketsPerBlock

- **UUID**: `3b350d39-068f-4d5e-9b8e-f73143935032`
- **参数名**: `J1939TpTxMaxPacketsPerBlock`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `255`
- **取值范围**: [1..255]
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Maximum number of TP.DT frames the transmitting J1939Tp module is ready to send before waiting for another TP.CM_CTS. This parameter is transmitted in the TP.CM_RTS frame, and is thus only relevant for transmission of messages via CMDT. When J1939TpDynamicBlockCalculation is enabled, this parameter specifies a maximum for the calculated value. For further details on this parameter value see SAE J1939/21.

####### BOOLEAN 类型参数

######## 1. J1939TpTxCancellationSupport

- **UUID**: `a502790f-4fc8-434a-81c2-313f8bfca0e3`
- **参数名**: `J1939TpTxCancellationSupport`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enable transmit cancellation using the API J1939Tp_CancelTransmit() for this channel.

######## 2. J1939TpTxDynamicBlockCalculation

- **UUID**: `8938007e-29e5-456b-a6a6-b7060b61fe1d`
- **参数名**: `J1939TpTxDynamicBlockCalculation`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enable dynamic calculation of "maximum number of packets that can be sent" value in TP.CM_RTS, based on the available amount of data in upper layers reported via CopyTxData.

######## 3. J1939TpTxRetrySupport

- **UUID**: `06aff745-8ef9-434f-bf86-ae446b1f7f6e`
- **参数名**: `J1939TpTxRetrySupport`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enable support for repetition of failed transmission using TP.CM_CTS with a packet number that has already been sent. Retransmission is handled via the retry feature of PduR_J1939TpCopyTxData.

####### ENUMERATION 类型参数

######## 1. J1939TpTxProtocolType

- **UUID**: `95e81933-1f8e-417c-8fa9-061679e2b7b7`
- **参数名**: `J1939TpTxProtocolType`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `J1939TP_PROTOCOL_BAM` (来源: AUTOSAR_ECUC)
  - `J1939TP_PROTOCOL_CMDT` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Protocol type used by this channel. This parameter is only required for channels with fixed destination address.

###### 配置容器

本模块包含 **6** 个配置容器：

####### 1. J1939TpRxFcNPdu

**容器属性**:

- **UUID**: `5aa512cf-410d-4f4a-9a3c-39a338282e67`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `J1939TpRxFcNPdu`
- **多重性**: [0..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This N-PDU represents the TP.CM frame that is used in reverse direction for a J1939 transport protocol session using the CMDT protocol type. TP.CM in reverse direction is used for intermediate and final acknowledgement of received data and to abort the connection.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. J1939TpRxFcNPduId

- **UUID**: `a9b0fbe9-1c93-455d-9956-aaa516f558fa`
- **参数名**: `J1939TpRxFcNPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - POST-BUILD: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The N-PDU identifier used for communication with CanIf.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. J1939TpRxFcNPduRef

- **UUID**: `a63fe105-2c0b-4055-99a1-1c30b947f140`
- **引用名**: `J1939TpRxFcNPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the Pdu object representing the N-PDU.

####### 2. J1939TpTxCmNPdu

**容器属性**:

- **UUID**: `0adc2c61-34e9-4518-8ec3-18eb31074cc5`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `J1939TpTxCmNPdu`
- **多重性**: [1..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This N-PDU represents the TP.CM frame of a J1939 transport protocol session. TP.CM is used both by BAM and CMDT to initialize the connection. For CMDT, it is also used to abort the connection.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. J1939TpTxCmNPduTxConfId

- **UUID**: `f4b7c3ad-2c0c-4988-bda8-63d147a05c51`
- **参数名**: `J1939TpTxCmNPduTxConfId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - POST-BUILD: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The N-PDU identifier used for Tx confirmation from CanIf.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. J1939TpTxCmNPduRef

- **UUID**: `c9500e8c-e8d6-484c-9493-d1442fb35f74`
- **引用名**: `J1939TpTxCmNPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the Pdu object representing the N-PDU.

####### 3. J1939TpTxDtNPdu

**容器属性**:

- **UUID**: `45d64ed4-3b4d-4c5a-abb3-51c1e473c0ba`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `J1939TpTxDtNPdu`
- **多重性**: [1..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This N-PDU represents the TP.DT frame of a J1939 transport protocol session. TP.DT is used both by BAM and CMDT to transfer the contents of an N-SDU.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. J1939TpTxDtNPduTxConfId

- **UUID**: `2c4e49a4-da98-45db-9f5f-dfac7a6f8834`
- **参数名**: `J1939TpTxDtNPduTxConfId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - POST-BUILD: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The N-PDU identifier used for Tx confirmation from CanIf.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. J1939TpTxDtNPduRef

- **UUID**: `e2affed1-1a48-412f-a840-6f84a2e8bd6e`
- **引用名**: `J1939TpTxDtNPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the Pdu object representing the N-PDU.

####### 4. J1939TpTxPg

**容器属性**:

- **UUID**: `23529746-f2de-4ed9-8594-364ae38da65a`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `J1939TpTxPg`
- **多重性**: [1..infinite]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

Parameter group transmitted by the J1939 transport layer.

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. J1939TpTxPgPGN

- **UUID**: `01f7cf32-9388-43de-8483-c90604e372ad`
- **参数名**: `J1939TpTxPgPGN`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..262143]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the PGN which is represented by the N-SDU.

######### BOOLEAN 类型参数

########## 1. J1939TpTxPgDynLength

- **UUID**: `6967b20d-5ba9-436c-9c7a-f36fcbf3d58a`
- **参数名**: `J1939TpTxPgDynLength`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This flag is set to TRUE when the N-SDU refers to a PGN with variable length.

######## 配置容器

本模块包含 **2** 个配置容器：

######### 1. J1939TpTxDirectNPdu

**容器属性**:

- **UUID**: `e6ebe3a0-eae2-4545-831a-287705fd5140`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `J1939TpTxDirectNPdu`
- **多重性**: [0..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This N-PDU represents the short frame that is used for a dynamic length PGN when it has a length of less that 8 bytes.

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. J1939TpTxDirectNPduTxConfId

- **UUID**: `c3456f58-feeb-4165-98ee-1ed090bfa37f`
- **参数名**: `J1939TpTxDirectNPduTxConfId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - POST-BUILD: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The N-PDU identifier used for Tx confirmation from CanIf.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. J1939TpTxDirectNPduRef

- **UUID**: `6524c290-53d9-4e8e-857e-5d31f6d9ec3d`
- **引用名**: `J1939TpTxDirectNPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the Pdu object representing the N-PDU.

######### 2. J1939TpTxNSdu

**容器属性**:

- **UUID**: `b62d24fb-9f8b-4328-9575-f9dc0243183f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `J1939TpTxNSdu`
- **多重性**: [1..infinite]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container describes the parameters that are relevant for the transmission of a specific N-SDU.

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. J1939TpTxNSduId

- **UUID**: `68d6080e-d482-444b-ad98-3027e45ff484`
- **参数名**: `J1939TpTxNSduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - POST-BUILD: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The N-SDU identifier used for communication with PduR.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. J1939TpTxNSduRef

- **UUID**: `66259ff6-ed47-4266-8cef-331bead14f38`
- **引用名**: `J1939TpTxNSduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the Pdu object representing the N-SDU.

####### 5. J1939TpTxDirectNPdu

**容器属性**:

- **UUID**: `e6ebe3a0-eae2-4545-831a-287705fd5140`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `J1939TpTxDirectNPdu`
- **多重性**: [0..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This N-PDU represents the short frame that is used for a dynamic length PGN when it has a length of less that 8 bytes.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. J1939TpTxDirectNPduTxConfId

- **UUID**: `c3456f58-feeb-4165-98ee-1ed090bfa37f`
- **参数名**: `J1939TpTxDirectNPduTxConfId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - POST-BUILD: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The N-PDU identifier used for Tx confirmation from CanIf.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. J1939TpTxDirectNPduRef

- **UUID**: `6524c290-53d9-4e8e-857e-5d31f6d9ec3d`
- **引用名**: `J1939TpTxDirectNPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the Pdu object representing the N-PDU.

####### 6. J1939TpTxNSdu

**容器属性**:

- **UUID**: `b62d24fb-9f8b-4328-9575-f9dc0243183f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `J1939TpTxNSdu`
- **多重性**: [1..infinite]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container describes the parameters that are relevant for the transmission of a specific N-SDU.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. J1939TpTxNSduId

- **UUID**: `68d6080e-d482-444b-ad98-3027e45ff484`
- **参数名**: `J1939TpTxNSduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - POST-BUILD: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The N-SDU identifier used for communication with PduR.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. J1939TpTxNSduRef

- **UUID**: `66259ff6-ed47-4266-8cef-331bead14f38`
- **引用名**: `J1939TpTxNSduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the Pdu object representing the N-SDU.

##### 11. J1939TpRxFcNPdu

**容器属性**:

- **UUID**: `5aa512cf-410d-4f4a-9a3c-39a338282e67`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `J1939TpRxFcNPdu`
- **多重性**: [0..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This N-PDU represents the TP.CM frame that is used in reverse direction for a J1939 transport protocol session using the CMDT protocol type. TP.CM in reverse direction is used for intermediate and final acknowledgement of received data and to abort the connection.

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. J1939TpRxFcNPduId

- **UUID**: `a9b0fbe9-1c93-455d-9956-aaa516f558fa`
- **参数名**: `J1939TpRxFcNPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - POST-BUILD: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The N-PDU identifier used for communication with CanIf.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. J1939TpRxFcNPduRef

- **UUID**: `a63fe105-2c0b-4055-99a1-1c30b947f140`
- **引用名**: `J1939TpRxFcNPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the Pdu object representing the N-PDU.

##### 12. J1939TpTxCmNPdu

**容器属性**:

- **UUID**: `0adc2c61-34e9-4518-8ec3-18eb31074cc5`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `J1939TpTxCmNPdu`
- **多重性**: [1..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This N-PDU represents the TP.CM frame of a J1939 transport protocol session. TP.CM is used both by BAM and CMDT to initialize the connection. For CMDT, it is also used to abort the connection.

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. J1939TpTxCmNPduTxConfId

- **UUID**: `f4b7c3ad-2c0c-4988-bda8-63d147a05c51`
- **参数名**: `J1939TpTxCmNPduTxConfId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - POST-BUILD: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The N-PDU identifier used for Tx confirmation from CanIf.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. J1939TpTxCmNPduRef

- **UUID**: `c9500e8c-e8d6-484c-9493-d1442fb35f74`
- **引用名**: `J1939TpTxCmNPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the Pdu object representing the N-PDU.

##### 13. J1939TpTxDtNPdu

**容器属性**:

- **UUID**: `45d64ed4-3b4d-4c5a-abb3-51c1e473c0ba`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `J1939TpTxDtNPdu`
- **多重性**: [1..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This N-PDU represents the TP.DT frame of a J1939 transport protocol session. TP.DT is used both by BAM and CMDT to transfer the contents of an N-SDU.

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. J1939TpTxDtNPduTxConfId

- **UUID**: `2c4e49a4-da98-45db-9f5f-dfac7a6f8834`
- **参数名**: `J1939TpTxDtNPduTxConfId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - POST-BUILD: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The N-PDU identifier used for Tx confirmation from CanIf.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. J1939TpTxDtNPduRef

- **UUID**: `e2affed1-1a48-412f-a840-6f84a2e8bd6e`
- **引用名**: `J1939TpTxDtNPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the Pdu object representing the N-PDU.

##### 14. J1939TpTxPg

**容器属性**:

- **UUID**: `23529746-f2de-4ed9-8594-364ae38da65a`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `J1939TpTxPg`
- **多重性**: [1..infinite]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

Parameter group transmitted by the J1939 transport layer.

###### 参数配置

此容器包含 **2** 个参数：

####### INTEGER 类型参数

######## 1. J1939TpTxPgPGN

- **UUID**: `01f7cf32-9388-43de-8483-c90604e372ad`
- **参数名**: `J1939TpTxPgPGN`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..262143]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the PGN which is represented by the N-SDU.

####### BOOLEAN 类型参数

######## 1. J1939TpTxPgDynLength

- **UUID**: `6967b20d-5ba9-436c-9c7a-f36fcbf3d58a`
- **参数名**: `J1939TpTxPgDynLength`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This flag is set to TRUE when the N-SDU refers to a PGN with variable length.

###### 配置容器

本模块包含 **2** 个配置容器：

####### 1. J1939TpTxDirectNPdu

**容器属性**:

- **UUID**: `e6ebe3a0-eae2-4545-831a-287705fd5140`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `J1939TpTxDirectNPdu`
- **多重性**: [0..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This N-PDU represents the short frame that is used for a dynamic length PGN when it has a length of less that 8 bytes.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. J1939TpTxDirectNPduTxConfId

- **UUID**: `c3456f58-feeb-4165-98ee-1ed090bfa37f`
- **参数名**: `J1939TpTxDirectNPduTxConfId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - POST-BUILD: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The N-PDU identifier used for Tx confirmation from CanIf.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. J1939TpTxDirectNPduRef

- **UUID**: `6524c290-53d9-4e8e-857e-5d31f6d9ec3d`
- **引用名**: `J1939TpTxDirectNPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the Pdu object representing the N-PDU.

####### 2. J1939TpTxNSdu

**容器属性**:

- **UUID**: `b62d24fb-9f8b-4328-9575-f9dc0243183f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `J1939TpTxNSdu`
- **多重性**: [1..infinite]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container describes the parameters that are relevant for the transmission of a specific N-SDU.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. J1939TpTxNSduId

- **UUID**: `68d6080e-d482-444b-ad98-3027e45ff484`
- **参数名**: `J1939TpTxNSduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - POST-BUILD: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The N-SDU identifier used for communication with PduR.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. J1939TpTxNSduRef

- **UUID**: `66259ff6-ed47-4266-8cef-331bead14f38`
- **引用名**: `J1939TpTxNSduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the Pdu object representing the N-SDU.

##### 15. J1939TpTxDirectNPdu

**容器属性**:

- **UUID**: `e6ebe3a0-eae2-4545-831a-287705fd5140`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `J1939TpTxDirectNPdu`
- **多重性**: [0..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This N-PDU represents the short frame that is used for a dynamic length PGN when it has a length of less that 8 bytes.

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. J1939TpTxDirectNPduTxConfId

- **UUID**: `c3456f58-feeb-4165-98ee-1ed090bfa37f`
- **参数名**: `J1939TpTxDirectNPduTxConfId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - POST-BUILD: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The N-PDU identifier used for Tx confirmation from CanIf.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. J1939TpTxDirectNPduRef

- **UUID**: `6524c290-53d9-4e8e-857e-5d31f6d9ec3d`
- **引用名**: `J1939TpTxDirectNPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the Pdu object representing the N-PDU.

##### 16. J1939TpTxNSdu

**容器属性**:

- **UUID**: `b62d24fb-9f8b-4328-9575-f9dc0243183f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `J1939TpTxNSdu`
- **多重性**: [1..infinite]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container describes the parameters that are relevant for the transmission of a specific N-SDU.

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. J1939TpTxNSduId

- **UUID**: `68d6080e-d482-444b-ad98-3027e45ff484`
- **参数名**: `J1939TpTxNSduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - POST-BUILD: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The N-SDU identifier used for communication with PduR.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. J1939TpTxNSduRef

- **UUID**: `66259ff6-ed47-4266-8cef-331bead14f38`
- **引用名**: `J1939TpTxNSduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the Pdu object representing the N-SDU.

##### 17. J1939TpGeneral

**容器属性**:

- **UUID**: `ECUC:49139360-a21c-43bb-8469-400fd36fe9ca`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `J1939TpGeneral`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

This container describes the general configuration parameters of the J1939Tp  module.

###### 参数配置

此容器包含 **6** 个参数：

####### BOOLEAN 类型参数

######## 1. J1939TpCancellationSupport

- **UUID**: `75c47841-b3ee-444b-bab4-8f4e4954f5e2`
- **参数名**: `J1939TpCancellationSupport`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enable transmit and receive cancellation.

######## 2. J1939TpDevErrorDetect

- **UUID**: `429b5637-a6e1-4926-9bbf-930d88df17e4`
- **参数名**: `J1939TpDevErrorDetect`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Switches the Development Error Detection and Notification.

######## 3. J1939TpVersionInfoApi

- **UUID**: `d3d0af45-d8f7-4833-87e7-78514ec1126f`
- **参数名**: `J1939TpVersionInfoApi`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The function J1939Tp_GetVersionInfo is configurable (On/Off) by this configuration parameter.

####### FLOAT 类型参数

######## 1. J1939TpMainFunctionPeriod

- **UUID**: `1881d5bb-2739-40cb-a097-0cfcd597a369`
- **参数名**: `J1939TpMainFunctionPeriod`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0..0.255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Allow to configure the time for the MainFunction (in seconds).

######## 2. J1939TpTxConfTimeout

- **UUID**: `d8ba9af0-a14d-4a86-863a-dd343ef27d99`
- **参数名**: `J1939TpTxConfTimeout`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0..65.535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Timeout in seconds for the CanIf Tx confirmation. After this time the J1939Tp assumes that an N-PDU could not be transmitted.

####### STRING 类型参数

######## 1. J1939TpUserConfigurationFile

- **UUID**: `d15520a6-e2f7-4e97-8519-9f2a13863d7b`
- **参数名**: `J1939TpUserConfigurationFile`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Path to user configuration file. The content of this file is included in J1939Tp_Cfg.h during generation.

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

1. **J1939Tp**
