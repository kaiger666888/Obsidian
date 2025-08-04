# J1939Rm - 完整配置文档

*此文档由ARXML文件自动生成，采用层次化结构展示*

**生成时间**: 2025-06-16 14:48:50

## 📑 目录

- [📄 文件信息](#-文件信息)
- [🔧 模块定义](#-模块定义)
  - [J1939Rm](#j1939rm)
- [📦 包结构](#-包结构)

## 📄 文件信息

### Schema信息
- **Schema位置**: `http://autosar.org/schema/r4.0 AUTOSAR_4-0-3.xsd`
- **命名空间**: `http://autosar.org/schema/r4.0`

## 🔧 模块定义

### 1. J1939Rm

#### 基本信息

- **UUID**: `ECUC:27255541-a605-4c97-b9be-d05032a8b461`
- **模块名称**: `J1939Rm`
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

本模块包含 **12** 个配置容器：

##### 1. J1939RmConfigSet

**容器属性**:

- **UUID**: `ECUC:5cf1a263-c0ee-4a24-a485-704ec78413a7`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `J1939RmConfigSet`
- **多重性**: [1..1]
- **多配置容器**: true

**容器描述**:

This container is a MultipleConfigurationContainer, i.e. this container and its sub-containers exist once per configuration set.

###### 配置容器

本模块包含 **10** 个配置容器：

####### 1. J1939RmChannel

**容器属性**:

- **UUID**: `ECUC:7e0aa11e-4b45-4a32-9b33-2fa5e2907640`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `J1939RmChannel`
- **多重性**: [1..infinite]
- **构建后可变**: true
- **多配置容器**: false

**容器描述**:

Contains the parameters for a CAN channel supported by the J1939 Request Manager.

######## 参数配置

此容器包含 **3** 个参数：

######### INTEGER 类型参数

########## 1. J1939RmAckQueueSize

- **UUID**: `ECUC:5dcee440-f4bb-46d6-a787-4a19d98560f2`
- **参数名**: `J1939RmAckQueueSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Number of transmitted acknowledgements that can be stored.

########## 2. J1939RmRequestQueueSize

- **UUID**: `ECUC:32b3c018-dd5e-462d-9f5c-8a88a11af231`
- **参数名**: `J1939RmRequestQueueSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Number of transmitted requests that can be stored.

########## 3. J1939RmRequestTimeoutMonitors

- **UUID**: `ECUC:a829bbce-af3a-476b-bac4-727fedfc827c`
- **参数名**: `J1939RmRequestTimeoutMonitors`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Number of transmitted requests that can be monitored for timeout.

######## 引用关系

此容器包含 **1** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. J1939RmComMNetworkHandleRef

- **UUID**: `ECUC:17cfd20c-d369-473a-800b-2010c8a5be28`
- **引用名**: `J1939RmComMNetworkHandleRef`
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

本模块包含 **4** 个配置容器：

######### 1. J1939RmAckmRxPdu

**容器属性**:

- **UUID**: `ECUC:c29fc910-2ae7-4d23-b3d6-471a6a664ece`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `J1939RmAckmRxPdu`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Contains the configuration of the I-PDU used to receive the Acknowledgement PG.

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. J1939RmAckmRxPduId

- **UUID**: `ECUC:384018fd-c035-4758-b3ce-3588af856fe3`
- **参数名**: `J1939RmAckmRxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The I-PDU identifier used for RxIndication from PduR.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. J1939RmAckmRxPduRef

- **UUID**: `ECUC:df89fcd4-edb0-45d2-874e-2c632c2981e8`
- **引用名**: `J1939RmAckmRxPduRef`
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

######### 2. J1939RmAckmTxPdu

**容器属性**:

- **UUID**: `ECUC:3dc55eb3-e8d0-4c21-98bf-5e34edce9502`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `J1939RmAckmTxPdu`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Contains the configuration of the I-PDU used to transmit the Acknowledgement PG.

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. J1939RmAckmTxPduId

- **UUID**: `ECUC:b31cb398-8dd5-4b8c-b239-63e5c1adf9a0`
- **参数名**: `J1939RmAckmTxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The I-PDU identifier used for TxConfirmation from PduR.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. J1939RmAckmTxPduRef

- **UUID**: `ECUC:1d59d5a3-b579-4d8f-abd9-81307a195a58`
- **引用名**: `J1939RmAckmTxPduRef`
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

######### 3. J1939RmRqstRxPdu

**容器属性**:

- **UUID**: `ECUC:479965fe-361f-48f3-8cb4-093697565b3f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `J1939RmRqstRxPdu`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Contains the configuration of the I-PDU used to receive the Request PG.

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. J1939RmRqstRxPduId

- **UUID**: `ECUC:a54ac773-f61b-4092-bf95-94fa8249e93a`
- **参数名**: `J1939RmRqstRxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The I-PDU identifier used for RxIndication from PduR.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. J1939RmRqstRxPduRef

- **UUID**: `ECUC:a1b2b442-997d-4e4e-9785-137bbba46565`
- **引用名**: `J1939RmRqstRxPduRef`
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

######### 4. J1939RmRqstTxPdu

**容器属性**:

- **UUID**: `ECUC:58f0f75c-0764-429f-80d7-83187edbee73`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `J1939RmRqstTxPdu`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Contains the configuration of the I-PDU used to transmit the Request PG.

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. J1939RmRqstTxPduId

- **UUID**: `ECUC:c837bbfe-c073-44d7-9b6e-30fe89bdb70d`
- **参数名**: `J1939RmRqstTxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The I-PDU identifier used for TxConfirmation from PduR.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. J1939RmRqstTxPduRef

- **UUID**: `ECUC:5efc2cae-3d15-4cff-b893-ba702661b8e7`
- **引用名**: `J1939RmRqstTxPduRef`
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

####### 2. J1939RmAckmRxPdu

**容器属性**:

- **UUID**: `ECUC:c29fc910-2ae7-4d23-b3d6-471a6a664ece`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `J1939RmAckmRxPdu`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Contains the configuration of the I-PDU used to receive the Acknowledgement PG.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. J1939RmAckmRxPduId

- **UUID**: `ECUC:384018fd-c035-4758-b3ce-3588af856fe3`
- **参数名**: `J1939RmAckmRxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The I-PDU identifier used for RxIndication from PduR.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. J1939RmAckmRxPduRef

- **UUID**: `ECUC:df89fcd4-edb0-45d2-874e-2c632c2981e8`
- **引用名**: `J1939RmAckmRxPduRef`
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

####### 3. J1939RmAckmTxPdu

**容器属性**:

- **UUID**: `ECUC:3dc55eb3-e8d0-4c21-98bf-5e34edce9502`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `J1939RmAckmTxPdu`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Contains the configuration of the I-PDU used to transmit the Acknowledgement PG.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. J1939RmAckmTxPduId

- **UUID**: `ECUC:b31cb398-8dd5-4b8c-b239-63e5c1adf9a0`
- **参数名**: `J1939RmAckmTxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The I-PDU identifier used for TxConfirmation from PduR.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. J1939RmAckmTxPduRef

- **UUID**: `ECUC:1d59d5a3-b579-4d8f-abd9-81307a195a58`
- **引用名**: `J1939RmAckmTxPduRef`
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

####### 4. J1939RmRqstRxPdu

**容器属性**:

- **UUID**: `ECUC:479965fe-361f-48f3-8cb4-093697565b3f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `J1939RmRqstRxPdu`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Contains the configuration of the I-PDU used to receive the Request PG.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. J1939RmRqstRxPduId

- **UUID**: `ECUC:a54ac773-f61b-4092-bf95-94fa8249e93a`
- **参数名**: `J1939RmRqstRxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The I-PDU identifier used for RxIndication from PduR.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. J1939RmRqstRxPduRef

- **UUID**: `ECUC:a1b2b442-997d-4e4e-9785-137bbba46565`
- **引用名**: `J1939RmRqstRxPduRef`
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

####### 5. J1939RmRqstTxPdu

**容器属性**:

- **UUID**: `ECUC:58f0f75c-0764-429f-80d7-83187edbee73`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `J1939RmRqstTxPdu`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Contains the configuration of the I-PDU used to transmit the Request PG.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. J1939RmRqstTxPduId

- **UUID**: `ECUC:c837bbfe-c073-44d7-9b6e-30fe89bdb70d`
- **参数名**: `J1939RmRqstTxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The I-PDU identifier used for TxConfirmation from PduR.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. J1939RmRqstTxPduRef

- **UUID**: `ECUC:5efc2cae-3d15-4cff-b893-ba702661b8e7`
- **引用名**: `J1939RmRqstTxPduRef`
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

####### 6. J1939RmNode

**容器属性**:

- **UUID**: `ECUC:d453e997-a0a0-403c-aa6d-34845c74418b`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `J1939RmNode`
- **多重性**: [1..infinite]
- **构建后可变**: true
- **多配置容器**: false

**容器描述**:

Contains the parameters for the support of a logical J1939 node (identified by an ECU address).

######## 引用关系

此容器包含 **2** 个引用：

######### REFERENCE 类型引用

########## 1. J1939RmNodeChannelRef

- **UUID**: `ECUC:aa122285-1c57-41e0-99da-41c9602f34ba`
- **引用名**: `J1939RmNodeChannelRef`
- **引用类型**: REFERENCE
- **多重性**: [1..infinite]
- **目标**: `J1939RmChannel`
- **完整路径**: `/AUTOSAR/EcucDefs/J1939Rm/J1939RmConfigSet/J1939RmChannel`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the channels this node has access to.

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. J1939RmNmNodeRef

- **UUID**: `ECUC:07bed225-fddd-4e71-96ed-cd22d87229fc`
- **引用名**: `J1939RmNmNodeRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `J1939NmNode`
- **完整路径**: `/AUTOSAR/EcucDefs/J1939Nm/J1939NmConfigSet/J1939NmNode`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the corresponding J1939Nm node.

######## 配置容器

本模块包含 **4** 个配置容器：

######### 1. J1939RmUser

**容器属性**:

- **UUID**: `ECUC:e534c545-1a58-4f2f-8e41-95d1106733a8`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `J1939RmUser`
- **多重性**: [1..infinite]
- **构建后可变**: true
- **多配置容器**: false

**容器描述**:

Contains the configuration of a module that uses the request and acknowledgement interfaces of J1939Rm.

########## 参数配置

此容器包含 **10** 个参数：

########### INTEGER 类型参数

############ 1. J1939RmUserAckPGN

- **UUID**: `ECUC:37997ea0-3065-4aaa-a9e2-40bc6b88a3bc`
- **参数名**: `J1939RmUserAckPGN`
- **数据类型**: INTEGER
- **多重性**: [0..infinite]
- **取值范围**: [0..262143]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: PGN supported to be acknowledged to this module. The PGNs supported by different modules should usually be disjunctive. This parameter shall not be set for J1939RmUserType J1939RM_USER_J1939NM, J1939RM_USER_J1939DCM, and J1939RM_USER_COM.

############ 2. J1939RmUserComIPduRequestQueueSize

- **UUID**: `ECUC:b386ec3b-587c-4d51-ba58-98c6387c910c`
- **参数名**: `J1939RmUserComIPduRequestQueueSize`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Number of received requests that can be stored for COM I-PDUs of this user.

############ 3. J1939RmUserId

- **UUID**: `ECUC:1fe9bba9-b2d6-43c3-affc-43271705f1b7`
- **参数名**: `J1939RmUserId`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Identifier used by a module using J1939Rm. This parameter is only required when the module uses transmission of requests.

############ 4. J1939RmUserPGN

- **UUID**: `ECUC:0f89743c-31e4-49da-ad13-a85775c09d1b`
- **参数名**: `J1939RmUserPGN`
- **数据类型**: INTEGER
- **多重性**: [0..infinite]
- **取值范围**: [0..262143]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: PGN supported to be requested from this module. The PGNs supported by different modules should usually be disjunctive. This parameter is predefined to AC (0x0EE00) for J1939RmUserType J1939RM_USER_J1939NM and is derived from the J1939Dcm PDUs in the system description for J1939RmUserType J1939RM_USER_J1939DCM. It shall not be set for J1939RmUserType J1939RM_USER_COM.

########### BOOLEAN 类型参数

############ 1. J1939RmUserAckIndication

- **UUID**: `ECUC:67fed1f0-296d-4d40-9387-9481dc72a908`
- **参数名**: `J1939RmUserAckIndication`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enable AckIndication for this module. In case of CDD, the name is <apiServicePrefix>_AckIndication. In case of RTE, the port is defined as J1939RmRPort<J1939RmUserId>, and the operation is called AckIndication. This parameter shall not be set for J1939RmUserType J1939RM_USER_J1939NM, J1939RM_USER_J1939DCM, or J1939RM_USER_COM.

############ 2. J1939RmUserRequestIndication

- **UUID**: `ECUC:d4306c2d-71d4-41e5-b6c0-bc1354a535df`
- **参数名**: `J1939RmUserRequestIndication`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enable RequestIndication for this module. In case of J1939Nm or J1939Dcm, the name is fixed. In case of CDD, the name is <apiServicePrefix>_RequestIndication. In case of RTE, the port is defined as J1939RmRPort<J1939RmUserId>, and the operation is called RequestIndication. This parameter shall not be set for J1939RmUserType J1939RM_USER_COM.

############ 3. J1939RmUserSendAck

- **UUID**: `ECUC:8311a6fb-8b7b-41ff-8de9-c1d692af5ca4`
- **参数名**: `J1939RmUserSendAck`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enable the SendAck API for this module. In case of RTE, the port is defined as J1939RmPPort<J1939RmUserId>, and the operation is called SendAck. This parameter shall not be set for J1939RmUserType J1939RM_USER_J1939NM or J1939RM_USER_COM.

############ 4. J1939RmUserSendRequest

- **UUID**: `ECUC:1466d83f-619c-4bc9-9e6f-cc6c27153c4b`
- **参数名**: `J1939RmUserSendRequest`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enable the SendRequest API for this module. In case of RTE, the port is defined as J1939RmPPort<J1939RmUserId>, and the operation is called SendRequest. This parameter shall not be set for J1939RmUserType J1939RM_USER_J1939NM, J1939RM_USER_J1939DCM, or J1939RM_USER_COM.

############ 5. J1939RmUserTimeoutSupervision

- **UUID**: `ECUC:a5425ede-c411-4f83-af88-3a68127893d3`
- **参数名**: `J1939RmUserTimeoutSupervision`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enable RequestTimeoutIndication and CancelRequestTimeout for this module. RequestTimeoutIndication: In case of CDD, the name is <apiServicePrefix>_RequestTimeoutIndication.

########### ENUMERATION 类型参数

############ 1. J1939RmUserType

- **UUID**: `ECUC:ee94106e-ef27-4982-a16f-8380a6eb1794`
- **参数名**: `J1939RmUserType`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `J1939RM_CDD` (来源: AUTOSAR_ECUC)
  - `J1939RM_RTE` (来源: AUTOSAR_ECUC)
  - `J1939RM_USER_COM` (来源: AUTOSAR_ECUC)
  - `J1939RM_USER_J1939DCM` (来源: AUTOSAR_ECUC)
  - `J1939RM_USER_J1939NM` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Type of module using J1939Rm.

########## 引用关系

此容器包含 **1** 个引用：

########### FOREIGN-REFERENCE 类型引用

############ 1. J1939RmUserCddRef

- **UUID**: `ECUC:074f9e81-f250-420f-b47c-2fd7c9430c42`
- **引用名**: `J1939RmUserCddRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [0..1]
- **目标类型**: ECUC-MODULE-CONFIGURATION-VALUES
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the CDD module description. This parameter is only required for J1939RmUserType J1939RM_USER_CDD.

########## 配置容器

本模块包含 **3** 个配置容器：

########### 1. J1939RmComIPdu

**容器属性**:

- **UUID**: `ECUC:895c7730-bd1b-4c1a-819d-d5a5c83a0001`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `J1939RmComIPdu`
- **多重性**: [0..infinite]
- **构建后可变**: true
- **多配置容器**: false

**容器描述**:

Contains the configuration of an I-PDU that is to be transmitted on request by COM. This configuration container is only relevant for J1939RmUserType J1939RM_USER_COM.

############ 参数配置

此容器包含 **3** 个参数：

############# INTEGER 类型参数

############## 1. J1939RmComIPduDA

- **UUID**: `ECUC:319fe995-75c2-4673-9548-d6615a3911e1`
- **参数名**: `J1939RmComIPduDA`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..253]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Destination address of the COM I-PDU.

############## 2. J1939RmComIPduPGN

- **UUID**: `ECUC:e25ddae6-8a07-4ede-9340-dd08d4a54df3`
- **参数名**: `J1939RmComIPduPGN`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..262143]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: PGN of the COM I-PDU.

############## 3. J1939RmComIPduSA

- **UUID**: `ECUC:203a04b4-8064-46f2-9f2a-be9f3ce6391d`
- **参数名**: `J1939RmComIPduSA`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..253]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Source address of the COM I-PDU.

############ 配置容器

本模块包含 **2** 个配置容器：

############# 1. J1939RmLowerComIPdu

**容器属性**:

- **UUID**: `ECUC:7934f63c-95a7-4b79-8d06-02be6e0ea367`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `J1939RmLowerComIPdu`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

Contains the configuration of the I-PDU that is sent from J1939Rm to CanIf or J1939Tp.

############## 参数配置

此容器包含 **1** 个参数：

############### INTEGER 类型参数

################ 1. J1939RmLowerComIPduId

- **UUID**: `ECUC:7338e5b5-35e0-491e-9aef-c4dffdf83796`
- **参数名**: `J1939RmLowerComIPduId`
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

############## 引用关系

此容器包含 **1** 个引用：

############### REFERENCE 类型引用

################ 1. J1939RmLowerComIPduRef

- **UUID**: `ECUC:9f97cfd5-beb1-4cac-8b4f-fddb4554023b`
- **引用名**: `J1939RmLowerComIPduRef`
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

############# 2. J1939RmUpperComIPdu

**容器属性**:

- **UUID**: `ECUC:a8bbbdfa-1c66-4428-ad89-272b41945433`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `J1939RmUpperComIPdu`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

Contains the configuration of the I-PDU that is sent from COM to J1939Rm.

############## 参数配置

此容器包含 **1** 个参数：

############### INTEGER 类型参数

################ 1. J1939RmUpperComIPduId

- **UUID**: `ECUC:bc462154-84f8-45c6-bb6d-924ddc6947c6`
- **参数名**: `J1939RmUpperComIPduId`
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

############## 引用关系

此容器包含 **1** 个引用：

############### REFERENCE 类型引用

################ 1. J1939RmUpperComIPduRef

- **UUID**: `ECUC:e1ebaf35-cb54-438c-8ee7-68c218ac6c1d`
- **引用名**: `J1939RmUpperComIPduRef`
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

########### 2. J1939RmLowerComIPdu

**容器属性**:

- **UUID**: `ECUC:7934f63c-95a7-4b79-8d06-02be6e0ea367`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `J1939RmLowerComIPdu`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

Contains the configuration of the I-PDU that is sent from J1939Rm to CanIf or J1939Tp.

############ 参数配置

此容器包含 **1** 个参数：

############# INTEGER 类型参数

############## 1. J1939RmLowerComIPduId

- **UUID**: `ECUC:7338e5b5-35e0-491e-9aef-c4dffdf83796`
- **参数名**: `J1939RmLowerComIPduId`
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

############## 1. J1939RmLowerComIPduRef

- **UUID**: `ECUC:9f97cfd5-beb1-4cac-8b4f-fddb4554023b`
- **引用名**: `J1939RmLowerComIPduRef`
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

########### 3. J1939RmUpperComIPdu

**容器属性**:

- **UUID**: `ECUC:a8bbbdfa-1c66-4428-ad89-272b41945433`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `J1939RmUpperComIPdu`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

Contains the configuration of the I-PDU that is sent from COM to J1939Rm.

############ 参数配置

此容器包含 **1** 个参数：

############# INTEGER 类型参数

############## 1. J1939RmUpperComIPduId

- **UUID**: `ECUC:bc462154-84f8-45c6-bb6d-924ddc6947c6`
- **参数名**: `J1939RmUpperComIPduId`
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

############## 1. J1939RmUpperComIPduRef

- **UUID**: `ECUC:e1ebaf35-cb54-438c-8ee7-68c218ac6c1d`
- **引用名**: `J1939RmUpperComIPduRef`
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

######### 2. J1939RmComIPdu

**容器属性**:

- **UUID**: `ECUC:895c7730-bd1b-4c1a-819d-d5a5c83a0001`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `J1939RmComIPdu`
- **多重性**: [0..infinite]
- **构建后可变**: true
- **多配置容器**: false

**容器描述**:

Contains the configuration of an I-PDU that is to be transmitted on request by COM. This configuration container is only relevant for J1939RmUserType J1939RM_USER_COM.

########## 参数配置

此容器包含 **3** 个参数：

########### INTEGER 类型参数

############ 1. J1939RmComIPduDA

- **UUID**: `ECUC:319fe995-75c2-4673-9548-d6615a3911e1`
- **参数名**: `J1939RmComIPduDA`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..253]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Destination address of the COM I-PDU.

############ 2. J1939RmComIPduPGN

- **UUID**: `ECUC:e25ddae6-8a07-4ede-9340-dd08d4a54df3`
- **参数名**: `J1939RmComIPduPGN`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..262143]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: PGN of the COM I-PDU.

############ 3. J1939RmComIPduSA

- **UUID**: `ECUC:203a04b4-8064-46f2-9f2a-be9f3ce6391d`
- **参数名**: `J1939RmComIPduSA`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..253]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Source address of the COM I-PDU.

########## 配置容器

本模块包含 **2** 个配置容器：

########### 1. J1939RmLowerComIPdu

**容器属性**:

- **UUID**: `ECUC:7934f63c-95a7-4b79-8d06-02be6e0ea367`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `J1939RmLowerComIPdu`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

Contains the configuration of the I-PDU that is sent from J1939Rm to CanIf or J1939Tp.

############ 参数配置

此容器包含 **1** 个参数：

############# INTEGER 类型参数

############## 1. J1939RmLowerComIPduId

- **UUID**: `ECUC:7338e5b5-35e0-491e-9aef-c4dffdf83796`
- **参数名**: `J1939RmLowerComIPduId`
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

############## 1. J1939RmLowerComIPduRef

- **UUID**: `ECUC:9f97cfd5-beb1-4cac-8b4f-fddb4554023b`
- **引用名**: `J1939RmLowerComIPduRef`
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

########### 2. J1939RmUpperComIPdu

**容器属性**:

- **UUID**: `ECUC:a8bbbdfa-1c66-4428-ad89-272b41945433`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `J1939RmUpperComIPdu`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

Contains the configuration of the I-PDU that is sent from COM to J1939Rm.

############ 参数配置

此容器包含 **1** 个参数：

############# INTEGER 类型参数

############## 1. J1939RmUpperComIPduId

- **UUID**: `ECUC:bc462154-84f8-45c6-bb6d-924ddc6947c6`
- **参数名**: `J1939RmUpperComIPduId`
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

############## 1. J1939RmUpperComIPduRef

- **UUID**: `ECUC:e1ebaf35-cb54-438c-8ee7-68c218ac6c1d`
- **引用名**: `J1939RmUpperComIPduRef`
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

######### 3. J1939RmLowerComIPdu

**容器属性**:

- **UUID**: `ECUC:7934f63c-95a7-4b79-8d06-02be6e0ea367`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `J1939RmLowerComIPdu`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

Contains the configuration of the I-PDU that is sent from J1939Rm to CanIf or J1939Tp.

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. J1939RmLowerComIPduId

- **UUID**: `ECUC:7338e5b5-35e0-491e-9aef-c4dffdf83796`
- **参数名**: `J1939RmLowerComIPduId`
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

############ 1. J1939RmLowerComIPduRef

- **UUID**: `ECUC:9f97cfd5-beb1-4cac-8b4f-fddb4554023b`
- **引用名**: `J1939RmLowerComIPduRef`
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

######### 4. J1939RmUpperComIPdu

**容器属性**:

- **UUID**: `ECUC:a8bbbdfa-1c66-4428-ad89-272b41945433`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `J1939RmUpperComIPdu`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

Contains the configuration of the I-PDU that is sent from COM to J1939Rm.

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. J1939RmUpperComIPduId

- **UUID**: `ECUC:bc462154-84f8-45c6-bb6d-924ddc6947c6`
- **参数名**: `J1939RmUpperComIPduId`
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

############ 1. J1939RmUpperComIPduRef

- **UUID**: `ECUC:e1ebaf35-cb54-438c-8ee7-68c218ac6c1d`
- **引用名**: `J1939RmUpperComIPduRef`
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

####### 7. J1939RmUser

**容器属性**:

- **UUID**: `ECUC:e534c545-1a58-4f2f-8e41-95d1106733a8`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `J1939RmUser`
- **多重性**: [1..infinite]
- **构建后可变**: true
- **多配置容器**: false

**容器描述**:

Contains the configuration of a module that uses the request and acknowledgement interfaces of J1939Rm.

######## 参数配置

此容器包含 **10** 个参数：

######### INTEGER 类型参数

########## 1. J1939RmUserAckPGN

- **UUID**: `ECUC:37997ea0-3065-4aaa-a9e2-40bc6b88a3bc`
- **参数名**: `J1939RmUserAckPGN`
- **数据类型**: INTEGER
- **多重性**: [0..infinite]
- **取值范围**: [0..262143]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: PGN supported to be acknowledged to this module. The PGNs supported by different modules should usually be disjunctive. This parameter shall not be set for J1939RmUserType J1939RM_USER_J1939NM, J1939RM_USER_J1939DCM, and J1939RM_USER_COM.

########## 2. J1939RmUserComIPduRequestQueueSize

- **UUID**: `ECUC:b386ec3b-587c-4d51-ba58-98c6387c910c`
- **参数名**: `J1939RmUserComIPduRequestQueueSize`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Number of received requests that can be stored for COM I-PDUs of this user.

########## 3. J1939RmUserId

- **UUID**: `ECUC:1fe9bba9-b2d6-43c3-affc-43271705f1b7`
- **参数名**: `J1939RmUserId`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Identifier used by a module using J1939Rm. This parameter is only required when the module uses transmission of requests.

########## 4. J1939RmUserPGN

- **UUID**: `ECUC:0f89743c-31e4-49da-ad13-a85775c09d1b`
- **参数名**: `J1939RmUserPGN`
- **数据类型**: INTEGER
- **多重性**: [0..infinite]
- **取值范围**: [0..262143]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: PGN supported to be requested from this module. The PGNs supported by different modules should usually be disjunctive. This parameter is predefined to AC (0x0EE00) for J1939RmUserType J1939RM_USER_J1939NM and is derived from the J1939Dcm PDUs in the system description for J1939RmUserType J1939RM_USER_J1939DCM. It shall not be set for J1939RmUserType J1939RM_USER_COM.

######### BOOLEAN 类型参数

########## 1. J1939RmUserAckIndication

- **UUID**: `ECUC:67fed1f0-296d-4d40-9387-9481dc72a908`
- **参数名**: `J1939RmUserAckIndication`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enable AckIndication for this module. In case of CDD, the name is <apiServicePrefix>_AckIndication. In case of RTE, the port is defined as J1939RmRPort<J1939RmUserId>, and the operation is called AckIndication. This parameter shall not be set for J1939RmUserType J1939RM_USER_J1939NM, J1939RM_USER_J1939DCM, or J1939RM_USER_COM.

########## 2. J1939RmUserRequestIndication

- **UUID**: `ECUC:d4306c2d-71d4-41e5-b6c0-bc1354a535df`
- **参数名**: `J1939RmUserRequestIndication`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enable RequestIndication for this module. In case of J1939Nm or J1939Dcm, the name is fixed. In case of CDD, the name is <apiServicePrefix>_RequestIndication. In case of RTE, the port is defined as J1939RmRPort<J1939RmUserId>, and the operation is called RequestIndication. This parameter shall not be set for J1939RmUserType J1939RM_USER_COM.

########## 3. J1939RmUserSendAck

- **UUID**: `ECUC:8311a6fb-8b7b-41ff-8de9-c1d692af5ca4`
- **参数名**: `J1939RmUserSendAck`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enable the SendAck API for this module. In case of RTE, the port is defined as J1939RmPPort<J1939RmUserId>, and the operation is called SendAck. This parameter shall not be set for J1939RmUserType J1939RM_USER_J1939NM or J1939RM_USER_COM.

########## 4. J1939RmUserSendRequest

- **UUID**: `ECUC:1466d83f-619c-4bc9-9e6f-cc6c27153c4b`
- **参数名**: `J1939RmUserSendRequest`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enable the SendRequest API for this module. In case of RTE, the port is defined as J1939RmPPort<J1939RmUserId>, and the operation is called SendRequest. This parameter shall not be set for J1939RmUserType J1939RM_USER_J1939NM, J1939RM_USER_J1939DCM, or J1939RM_USER_COM.

########## 5. J1939RmUserTimeoutSupervision

- **UUID**: `ECUC:a5425ede-c411-4f83-af88-3a68127893d3`
- **参数名**: `J1939RmUserTimeoutSupervision`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enable RequestTimeoutIndication and CancelRequestTimeout for this module. RequestTimeoutIndication: In case of CDD, the name is <apiServicePrefix>_RequestTimeoutIndication.

######### ENUMERATION 类型参数

########## 1. J1939RmUserType

- **UUID**: `ECUC:ee94106e-ef27-4982-a16f-8380a6eb1794`
- **参数名**: `J1939RmUserType`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `J1939RM_CDD` (来源: AUTOSAR_ECUC)
  - `J1939RM_RTE` (来源: AUTOSAR_ECUC)
  - `J1939RM_USER_COM` (来源: AUTOSAR_ECUC)
  - `J1939RM_USER_J1939DCM` (来源: AUTOSAR_ECUC)
  - `J1939RM_USER_J1939NM` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Type of module using J1939Rm.

######## 引用关系

此容器包含 **1** 个引用：

######### FOREIGN-REFERENCE 类型引用

########## 1. J1939RmUserCddRef

- **UUID**: `ECUC:074f9e81-f250-420f-b47c-2fd7c9430c42`
- **引用名**: `J1939RmUserCddRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [0..1]
- **目标类型**: ECUC-MODULE-CONFIGURATION-VALUES
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the CDD module description. This parameter is only required for J1939RmUserType J1939RM_USER_CDD.

######## 配置容器

本模块包含 **3** 个配置容器：

######### 1. J1939RmComIPdu

**容器属性**:

- **UUID**: `ECUC:895c7730-bd1b-4c1a-819d-d5a5c83a0001`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `J1939RmComIPdu`
- **多重性**: [0..infinite]
- **构建后可变**: true
- **多配置容器**: false

**容器描述**:

Contains the configuration of an I-PDU that is to be transmitted on request by COM. This configuration container is only relevant for J1939RmUserType J1939RM_USER_COM.

########## 参数配置

此容器包含 **3** 个参数：

########### INTEGER 类型参数

############ 1. J1939RmComIPduDA

- **UUID**: `ECUC:319fe995-75c2-4673-9548-d6615a3911e1`
- **参数名**: `J1939RmComIPduDA`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..253]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Destination address of the COM I-PDU.

############ 2. J1939RmComIPduPGN

- **UUID**: `ECUC:e25ddae6-8a07-4ede-9340-dd08d4a54df3`
- **参数名**: `J1939RmComIPduPGN`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..262143]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: PGN of the COM I-PDU.

############ 3. J1939RmComIPduSA

- **UUID**: `ECUC:203a04b4-8064-46f2-9f2a-be9f3ce6391d`
- **参数名**: `J1939RmComIPduSA`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..253]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Source address of the COM I-PDU.

########## 配置容器

本模块包含 **2** 个配置容器：

########### 1. J1939RmLowerComIPdu

**容器属性**:

- **UUID**: `ECUC:7934f63c-95a7-4b79-8d06-02be6e0ea367`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `J1939RmLowerComIPdu`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

Contains the configuration of the I-PDU that is sent from J1939Rm to CanIf or J1939Tp.

############ 参数配置

此容器包含 **1** 个参数：

############# INTEGER 类型参数

############## 1. J1939RmLowerComIPduId

- **UUID**: `ECUC:7338e5b5-35e0-491e-9aef-c4dffdf83796`
- **参数名**: `J1939RmLowerComIPduId`
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

############## 1. J1939RmLowerComIPduRef

- **UUID**: `ECUC:9f97cfd5-beb1-4cac-8b4f-fddb4554023b`
- **引用名**: `J1939RmLowerComIPduRef`
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

########### 2. J1939RmUpperComIPdu

**容器属性**:

- **UUID**: `ECUC:a8bbbdfa-1c66-4428-ad89-272b41945433`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `J1939RmUpperComIPdu`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

Contains the configuration of the I-PDU that is sent from COM to J1939Rm.

############ 参数配置

此容器包含 **1** 个参数：

############# INTEGER 类型参数

############## 1. J1939RmUpperComIPduId

- **UUID**: `ECUC:bc462154-84f8-45c6-bb6d-924ddc6947c6`
- **参数名**: `J1939RmUpperComIPduId`
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

############## 1. J1939RmUpperComIPduRef

- **UUID**: `ECUC:e1ebaf35-cb54-438c-8ee7-68c218ac6c1d`
- **引用名**: `J1939RmUpperComIPduRef`
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

######### 2. J1939RmLowerComIPdu

**容器属性**:

- **UUID**: `ECUC:7934f63c-95a7-4b79-8d06-02be6e0ea367`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `J1939RmLowerComIPdu`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

Contains the configuration of the I-PDU that is sent from J1939Rm to CanIf or J1939Tp.

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. J1939RmLowerComIPduId

- **UUID**: `ECUC:7338e5b5-35e0-491e-9aef-c4dffdf83796`
- **参数名**: `J1939RmLowerComIPduId`
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

############ 1. J1939RmLowerComIPduRef

- **UUID**: `ECUC:9f97cfd5-beb1-4cac-8b4f-fddb4554023b`
- **引用名**: `J1939RmLowerComIPduRef`
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

######### 3. J1939RmUpperComIPdu

**容器属性**:

- **UUID**: `ECUC:a8bbbdfa-1c66-4428-ad89-272b41945433`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `J1939RmUpperComIPdu`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

Contains the configuration of the I-PDU that is sent from COM to J1939Rm.

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. J1939RmUpperComIPduId

- **UUID**: `ECUC:bc462154-84f8-45c6-bb6d-924ddc6947c6`
- **参数名**: `J1939RmUpperComIPduId`
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

############ 1. J1939RmUpperComIPduRef

- **UUID**: `ECUC:e1ebaf35-cb54-438c-8ee7-68c218ac6c1d`
- **引用名**: `J1939RmUpperComIPduRef`
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

####### 8. J1939RmComIPdu

**容器属性**:

- **UUID**: `ECUC:895c7730-bd1b-4c1a-819d-d5a5c83a0001`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `J1939RmComIPdu`
- **多重性**: [0..infinite]
- **构建后可变**: true
- **多配置容器**: false

**容器描述**:

Contains the configuration of an I-PDU that is to be transmitted on request by COM. This configuration container is only relevant for J1939RmUserType J1939RM_USER_COM.

######## 参数配置

此容器包含 **3** 个参数：

######### INTEGER 类型参数

########## 1. J1939RmComIPduDA

- **UUID**: `ECUC:319fe995-75c2-4673-9548-d6615a3911e1`
- **参数名**: `J1939RmComIPduDA`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..253]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Destination address of the COM I-PDU.

########## 2. J1939RmComIPduPGN

- **UUID**: `ECUC:e25ddae6-8a07-4ede-9340-dd08d4a54df3`
- **参数名**: `J1939RmComIPduPGN`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..262143]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: PGN of the COM I-PDU.

########## 3. J1939RmComIPduSA

- **UUID**: `ECUC:203a04b4-8064-46f2-9f2a-be9f3ce6391d`
- **参数名**: `J1939RmComIPduSA`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..253]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Source address of the COM I-PDU.

######## 配置容器

本模块包含 **2** 个配置容器：

######### 1. J1939RmLowerComIPdu

**容器属性**:

- **UUID**: `ECUC:7934f63c-95a7-4b79-8d06-02be6e0ea367`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `J1939RmLowerComIPdu`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

Contains the configuration of the I-PDU that is sent from J1939Rm to CanIf or J1939Tp.

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. J1939RmLowerComIPduId

- **UUID**: `ECUC:7338e5b5-35e0-491e-9aef-c4dffdf83796`
- **参数名**: `J1939RmLowerComIPduId`
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

############ 1. J1939RmLowerComIPduRef

- **UUID**: `ECUC:9f97cfd5-beb1-4cac-8b4f-fddb4554023b`
- **引用名**: `J1939RmLowerComIPduRef`
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

######### 2. J1939RmUpperComIPdu

**容器属性**:

- **UUID**: `ECUC:a8bbbdfa-1c66-4428-ad89-272b41945433`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `J1939RmUpperComIPdu`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

Contains the configuration of the I-PDU that is sent from COM to J1939Rm.

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. J1939RmUpperComIPduId

- **UUID**: `ECUC:bc462154-84f8-45c6-bb6d-924ddc6947c6`
- **参数名**: `J1939RmUpperComIPduId`
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

############ 1. J1939RmUpperComIPduRef

- **UUID**: `ECUC:e1ebaf35-cb54-438c-8ee7-68c218ac6c1d`
- **引用名**: `J1939RmUpperComIPduRef`
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

####### 9. J1939RmLowerComIPdu

**容器属性**:

- **UUID**: `ECUC:7934f63c-95a7-4b79-8d06-02be6e0ea367`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `J1939RmLowerComIPdu`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

Contains the configuration of the I-PDU that is sent from J1939Rm to CanIf or J1939Tp.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. J1939RmLowerComIPduId

- **UUID**: `ECUC:7338e5b5-35e0-491e-9aef-c4dffdf83796`
- **参数名**: `J1939RmLowerComIPduId`
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

########## 1. J1939RmLowerComIPduRef

- **UUID**: `ECUC:9f97cfd5-beb1-4cac-8b4f-fddb4554023b`
- **引用名**: `J1939RmLowerComIPduRef`
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

####### 10. J1939RmUpperComIPdu

**容器属性**:

- **UUID**: `ECUC:a8bbbdfa-1c66-4428-ad89-272b41945433`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `J1939RmUpperComIPdu`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

Contains the configuration of the I-PDU that is sent from COM to J1939Rm.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. J1939RmUpperComIPduId

- **UUID**: `ECUC:bc462154-84f8-45c6-bb6d-924ddc6947c6`
- **参数名**: `J1939RmUpperComIPduId`
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

########## 1. J1939RmUpperComIPduRef

- **UUID**: `ECUC:e1ebaf35-cb54-438c-8ee7-68c218ac6c1d`
- **引用名**: `J1939RmUpperComIPduRef`
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

##### 2. J1939RmChannel

**容器属性**:

- **UUID**: `ECUC:7e0aa11e-4b45-4a32-9b33-2fa5e2907640`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `J1939RmChannel`
- **多重性**: [1..infinite]
- **构建后可变**: true
- **多配置容器**: false

**容器描述**:

Contains the parameters for a CAN channel supported by the J1939 Request Manager.

###### 参数配置

此容器包含 **3** 个参数：

####### INTEGER 类型参数

######## 1. J1939RmAckQueueSize

- **UUID**: `ECUC:5dcee440-f4bb-46d6-a787-4a19d98560f2`
- **参数名**: `J1939RmAckQueueSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Number of transmitted acknowledgements that can be stored.

######## 2. J1939RmRequestQueueSize

- **UUID**: `ECUC:32b3c018-dd5e-462d-9f5c-8a88a11af231`
- **参数名**: `J1939RmRequestQueueSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Number of transmitted requests that can be stored.

######## 3. J1939RmRequestTimeoutMonitors

- **UUID**: `ECUC:a829bbce-af3a-476b-bac4-727fedfc827c`
- **参数名**: `J1939RmRequestTimeoutMonitors`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Number of transmitted requests that can be monitored for timeout.

###### 引用关系

此容器包含 **1** 个引用：

####### SYMBOLIC-NAME-REFERENCE 类型引用

######## 1. J1939RmComMNetworkHandleRef

- **UUID**: `ECUC:17cfd20c-d369-473a-800b-2010c8a5be28`
- **引用名**: `J1939RmComMNetworkHandleRef`
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

本模块包含 **4** 个配置容器：

####### 1. J1939RmAckmRxPdu

**容器属性**:

- **UUID**: `ECUC:c29fc910-2ae7-4d23-b3d6-471a6a664ece`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `J1939RmAckmRxPdu`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Contains the configuration of the I-PDU used to receive the Acknowledgement PG.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. J1939RmAckmRxPduId

- **UUID**: `ECUC:384018fd-c035-4758-b3ce-3588af856fe3`
- **参数名**: `J1939RmAckmRxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The I-PDU identifier used for RxIndication from PduR.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. J1939RmAckmRxPduRef

- **UUID**: `ECUC:df89fcd4-edb0-45d2-874e-2c632c2981e8`
- **引用名**: `J1939RmAckmRxPduRef`
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

####### 2. J1939RmAckmTxPdu

**容器属性**:

- **UUID**: `ECUC:3dc55eb3-e8d0-4c21-98bf-5e34edce9502`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `J1939RmAckmTxPdu`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Contains the configuration of the I-PDU used to transmit the Acknowledgement PG.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. J1939RmAckmTxPduId

- **UUID**: `ECUC:b31cb398-8dd5-4b8c-b239-63e5c1adf9a0`
- **参数名**: `J1939RmAckmTxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The I-PDU identifier used for TxConfirmation from PduR.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. J1939RmAckmTxPduRef

- **UUID**: `ECUC:1d59d5a3-b579-4d8f-abd9-81307a195a58`
- **引用名**: `J1939RmAckmTxPduRef`
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

####### 3. J1939RmRqstRxPdu

**容器属性**:

- **UUID**: `ECUC:479965fe-361f-48f3-8cb4-093697565b3f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `J1939RmRqstRxPdu`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Contains the configuration of the I-PDU used to receive the Request PG.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. J1939RmRqstRxPduId

- **UUID**: `ECUC:a54ac773-f61b-4092-bf95-94fa8249e93a`
- **参数名**: `J1939RmRqstRxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The I-PDU identifier used for RxIndication from PduR.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. J1939RmRqstRxPduRef

- **UUID**: `ECUC:a1b2b442-997d-4e4e-9785-137bbba46565`
- **引用名**: `J1939RmRqstRxPduRef`
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

####### 4. J1939RmRqstTxPdu

**容器属性**:

- **UUID**: `ECUC:58f0f75c-0764-429f-80d7-83187edbee73`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `J1939RmRqstTxPdu`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Contains the configuration of the I-PDU used to transmit the Request PG.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. J1939RmRqstTxPduId

- **UUID**: `ECUC:c837bbfe-c073-44d7-9b6e-30fe89bdb70d`
- **参数名**: `J1939RmRqstTxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The I-PDU identifier used for TxConfirmation from PduR.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. J1939RmRqstTxPduRef

- **UUID**: `ECUC:5efc2cae-3d15-4cff-b893-ba702661b8e7`
- **引用名**: `J1939RmRqstTxPduRef`
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

##### 3. J1939RmAckmRxPdu

**容器属性**:

- **UUID**: `ECUC:c29fc910-2ae7-4d23-b3d6-471a6a664ece`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `J1939RmAckmRxPdu`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Contains the configuration of the I-PDU used to receive the Acknowledgement PG.

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. J1939RmAckmRxPduId

- **UUID**: `ECUC:384018fd-c035-4758-b3ce-3588af856fe3`
- **参数名**: `J1939RmAckmRxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The I-PDU identifier used for RxIndication from PduR.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. J1939RmAckmRxPduRef

- **UUID**: `ECUC:df89fcd4-edb0-45d2-874e-2c632c2981e8`
- **引用名**: `J1939RmAckmRxPduRef`
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

##### 4. J1939RmAckmTxPdu

**容器属性**:

- **UUID**: `ECUC:3dc55eb3-e8d0-4c21-98bf-5e34edce9502`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `J1939RmAckmTxPdu`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Contains the configuration of the I-PDU used to transmit the Acknowledgement PG.

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. J1939RmAckmTxPduId

- **UUID**: `ECUC:b31cb398-8dd5-4b8c-b239-63e5c1adf9a0`
- **参数名**: `J1939RmAckmTxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The I-PDU identifier used for TxConfirmation from PduR.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. J1939RmAckmTxPduRef

- **UUID**: `ECUC:1d59d5a3-b579-4d8f-abd9-81307a195a58`
- **引用名**: `J1939RmAckmTxPduRef`
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

##### 5. J1939RmRqstRxPdu

**容器属性**:

- **UUID**: `ECUC:479965fe-361f-48f3-8cb4-093697565b3f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `J1939RmRqstRxPdu`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Contains the configuration of the I-PDU used to receive the Request PG.

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. J1939RmRqstRxPduId

- **UUID**: `ECUC:a54ac773-f61b-4092-bf95-94fa8249e93a`
- **参数名**: `J1939RmRqstRxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The I-PDU identifier used for RxIndication from PduR.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. J1939RmRqstRxPduRef

- **UUID**: `ECUC:a1b2b442-997d-4e4e-9785-137bbba46565`
- **引用名**: `J1939RmRqstRxPduRef`
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

##### 6. J1939RmRqstTxPdu

**容器属性**:

- **UUID**: `ECUC:58f0f75c-0764-429f-80d7-83187edbee73`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `J1939RmRqstTxPdu`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Contains the configuration of the I-PDU used to transmit the Request PG.

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. J1939RmRqstTxPduId

- **UUID**: `ECUC:c837bbfe-c073-44d7-9b6e-30fe89bdb70d`
- **参数名**: `J1939RmRqstTxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The I-PDU identifier used for TxConfirmation from PduR.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. J1939RmRqstTxPduRef

- **UUID**: `ECUC:5efc2cae-3d15-4cff-b893-ba702661b8e7`
- **引用名**: `J1939RmRqstTxPduRef`
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

##### 7. J1939RmNode

**容器属性**:

- **UUID**: `ECUC:d453e997-a0a0-403c-aa6d-34845c74418b`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `J1939RmNode`
- **多重性**: [1..infinite]
- **构建后可变**: true
- **多配置容器**: false

**容器描述**:

Contains the parameters for the support of a logical J1939 node (identified by an ECU address).

###### 引用关系

此容器包含 **2** 个引用：

####### REFERENCE 类型引用

######## 1. J1939RmNodeChannelRef

- **UUID**: `ECUC:aa122285-1c57-41e0-99da-41c9602f34ba`
- **引用名**: `J1939RmNodeChannelRef`
- **引用类型**: REFERENCE
- **多重性**: [1..infinite]
- **目标**: `J1939RmChannel`
- **完整路径**: `/AUTOSAR/EcucDefs/J1939Rm/J1939RmConfigSet/J1939RmChannel`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the channels this node has access to.

####### SYMBOLIC-NAME-REFERENCE 类型引用

######## 1. J1939RmNmNodeRef

- **UUID**: `ECUC:07bed225-fddd-4e71-96ed-cd22d87229fc`
- **引用名**: `J1939RmNmNodeRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `J1939NmNode`
- **完整路径**: `/AUTOSAR/EcucDefs/J1939Nm/J1939NmConfigSet/J1939NmNode`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the corresponding J1939Nm node.

###### 配置容器

本模块包含 **4** 个配置容器：

####### 1. J1939RmUser

**容器属性**:

- **UUID**: `ECUC:e534c545-1a58-4f2f-8e41-95d1106733a8`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `J1939RmUser`
- **多重性**: [1..infinite]
- **构建后可变**: true
- **多配置容器**: false

**容器描述**:

Contains the configuration of a module that uses the request and acknowledgement interfaces of J1939Rm.

######## 参数配置

此容器包含 **10** 个参数：

######### INTEGER 类型参数

########## 1. J1939RmUserAckPGN

- **UUID**: `ECUC:37997ea0-3065-4aaa-a9e2-40bc6b88a3bc`
- **参数名**: `J1939RmUserAckPGN`
- **数据类型**: INTEGER
- **多重性**: [0..infinite]
- **取值范围**: [0..262143]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: PGN supported to be acknowledged to this module. The PGNs supported by different modules should usually be disjunctive. This parameter shall not be set for J1939RmUserType J1939RM_USER_J1939NM, J1939RM_USER_J1939DCM, and J1939RM_USER_COM.

########## 2. J1939RmUserComIPduRequestQueueSize

- **UUID**: `ECUC:b386ec3b-587c-4d51-ba58-98c6387c910c`
- **参数名**: `J1939RmUserComIPduRequestQueueSize`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Number of received requests that can be stored for COM I-PDUs of this user.

########## 3. J1939RmUserId

- **UUID**: `ECUC:1fe9bba9-b2d6-43c3-affc-43271705f1b7`
- **参数名**: `J1939RmUserId`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Identifier used by a module using J1939Rm. This parameter is only required when the module uses transmission of requests.

########## 4. J1939RmUserPGN

- **UUID**: `ECUC:0f89743c-31e4-49da-ad13-a85775c09d1b`
- **参数名**: `J1939RmUserPGN`
- **数据类型**: INTEGER
- **多重性**: [0..infinite]
- **取值范围**: [0..262143]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: PGN supported to be requested from this module. The PGNs supported by different modules should usually be disjunctive. This parameter is predefined to AC (0x0EE00) for J1939RmUserType J1939RM_USER_J1939NM and is derived from the J1939Dcm PDUs in the system description for J1939RmUserType J1939RM_USER_J1939DCM. It shall not be set for J1939RmUserType J1939RM_USER_COM.

######### BOOLEAN 类型参数

########## 1. J1939RmUserAckIndication

- **UUID**: `ECUC:67fed1f0-296d-4d40-9387-9481dc72a908`
- **参数名**: `J1939RmUserAckIndication`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enable AckIndication for this module. In case of CDD, the name is <apiServicePrefix>_AckIndication. In case of RTE, the port is defined as J1939RmRPort<J1939RmUserId>, and the operation is called AckIndication. This parameter shall not be set for J1939RmUserType J1939RM_USER_J1939NM, J1939RM_USER_J1939DCM, or J1939RM_USER_COM.

########## 2. J1939RmUserRequestIndication

- **UUID**: `ECUC:d4306c2d-71d4-41e5-b6c0-bc1354a535df`
- **参数名**: `J1939RmUserRequestIndication`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enable RequestIndication for this module. In case of J1939Nm or J1939Dcm, the name is fixed. In case of CDD, the name is <apiServicePrefix>_RequestIndication. In case of RTE, the port is defined as J1939RmRPort<J1939RmUserId>, and the operation is called RequestIndication. This parameter shall not be set for J1939RmUserType J1939RM_USER_COM.

########## 3. J1939RmUserSendAck

- **UUID**: `ECUC:8311a6fb-8b7b-41ff-8de9-c1d692af5ca4`
- **参数名**: `J1939RmUserSendAck`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enable the SendAck API for this module. In case of RTE, the port is defined as J1939RmPPort<J1939RmUserId>, and the operation is called SendAck. This parameter shall not be set for J1939RmUserType J1939RM_USER_J1939NM or J1939RM_USER_COM.

########## 4. J1939RmUserSendRequest

- **UUID**: `ECUC:1466d83f-619c-4bc9-9e6f-cc6c27153c4b`
- **参数名**: `J1939RmUserSendRequest`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enable the SendRequest API for this module. In case of RTE, the port is defined as J1939RmPPort<J1939RmUserId>, and the operation is called SendRequest. This parameter shall not be set for J1939RmUserType J1939RM_USER_J1939NM, J1939RM_USER_J1939DCM, or J1939RM_USER_COM.

########## 5. J1939RmUserTimeoutSupervision

- **UUID**: `ECUC:a5425ede-c411-4f83-af88-3a68127893d3`
- **参数名**: `J1939RmUserTimeoutSupervision`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enable RequestTimeoutIndication and CancelRequestTimeout for this module. RequestTimeoutIndication: In case of CDD, the name is <apiServicePrefix>_RequestTimeoutIndication.

######### ENUMERATION 类型参数

########## 1. J1939RmUserType

- **UUID**: `ECUC:ee94106e-ef27-4982-a16f-8380a6eb1794`
- **参数名**: `J1939RmUserType`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `J1939RM_CDD` (来源: AUTOSAR_ECUC)
  - `J1939RM_RTE` (来源: AUTOSAR_ECUC)
  - `J1939RM_USER_COM` (来源: AUTOSAR_ECUC)
  - `J1939RM_USER_J1939DCM` (来源: AUTOSAR_ECUC)
  - `J1939RM_USER_J1939NM` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Type of module using J1939Rm.

######## 引用关系

此容器包含 **1** 个引用：

######### FOREIGN-REFERENCE 类型引用

########## 1. J1939RmUserCddRef

- **UUID**: `ECUC:074f9e81-f250-420f-b47c-2fd7c9430c42`
- **引用名**: `J1939RmUserCddRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [0..1]
- **目标类型**: ECUC-MODULE-CONFIGURATION-VALUES
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the CDD module description. This parameter is only required for J1939RmUserType J1939RM_USER_CDD.

######## 配置容器

本模块包含 **3** 个配置容器：

######### 1. J1939RmComIPdu

**容器属性**:

- **UUID**: `ECUC:895c7730-bd1b-4c1a-819d-d5a5c83a0001`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `J1939RmComIPdu`
- **多重性**: [0..infinite]
- **构建后可变**: true
- **多配置容器**: false

**容器描述**:

Contains the configuration of an I-PDU that is to be transmitted on request by COM. This configuration container is only relevant for J1939RmUserType J1939RM_USER_COM.

########## 参数配置

此容器包含 **3** 个参数：

########### INTEGER 类型参数

############ 1. J1939RmComIPduDA

- **UUID**: `ECUC:319fe995-75c2-4673-9548-d6615a3911e1`
- **参数名**: `J1939RmComIPduDA`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..253]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Destination address of the COM I-PDU.

############ 2. J1939RmComIPduPGN

- **UUID**: `ECUC:e25ddae6-8a07-4ede-9340-dd08d4a54df3`
- **参数名**: `J1939RmComIPduPGN`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..262143]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: PGN of the COM I-PDU.

############ 3. J1939RmComIPduSA

- **UUID**: `ECUC:203a04b4-8064-46f2-9f2a-be9f3ce6391d`
- **参数名**: `J1939RmComIPduSA`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..253]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Source address of the COM I-PDU.

########## 配置容器

本模块包含 **2** 个配置容器：

########### 1. J1939RmLowerComIPdu

**容器属性**:

- **UUID**: `ECUC:7934f63c-95a7-4b79-8d06-02be6e0ea367`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `J1939RmLowerComIPdu`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

Contains the configuration of the I-PDU that is sent from J1939Rm to CanIf or J1939Tp.

############ 参数配置

此容器包含 **1** 个参数：

############# INTEGER 类型参数

############## 1. J1939RmLowerComIPduId

- **UUID**: `ECUC:7338e5b5-35e0-491e-9aef-c4dffdf83796`
- **参数名**: `J1939RmLowerComIPduId`
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

############## 1. J1939RmLowerComIPduRef

- **UUID**: `ECUC:9f97cfd5-beb1-4cac-8b4f-fddb4554023b`
- **引用名**: `J1939RmLowerComIPduRef`
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

########### 2. J1939RmUpperComIPdu

**容器属性**:

- **UUID**: `ECUC:a8bbbdfa-1c66-4428-ad89-272b41945433`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `J1939RmUpperComIPdu`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

Contains the configuration of the I-PDU that is sent from COM to J1939Rm.

############ 参数配置

此容器包含 **1** 个参数：

############# INTEGER 类型参数

############## 1. J1939RmUpperComIPduId

- **UUID**: `ECUC:bc462154-84f8-45c6-bb6d-924ddc6947c6`
- **参数名**: `J1939RmUpperComIPduId`
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

############## 1. J1939RmUpperComIPduRef

- **UUID**: `ECUC:e1ebaf35-cb54-438c-8ee7-68c218ac6c1d`
- **引用名**: `J1939RmUpperComIPduRef`
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

######### 2. J1939RmLowerComIPdu

**容器属性**:

- **UUID**: `ECUC:7934f63c-95a7-4b79-8d06-02be6e0ea367`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `J1939RmLowerComIPdu`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

Contains the configuration of the I-PDU that is sent from J1939Rm to CanIf or J1939Tp.

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. J1939RmLowerComIPduId

- **UUID**: `ECUC:7338e5b5-35e0-491e-9aef-c4dffdf83796`
- **参数名**: `J1939RmLowerComIPduId`
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

############ 1. J1939RmLowerComIPduRef

- **UUID**: `ECUC:9f97cfd5-beb1-4cac-8b4f-fddb4554023b`
- **引用名**: `J1939RmLowerComIPduRef`
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

######### 3. J1939RmUpperComIPdu

**容器属性**:

- **UUID**: `ECUC:a8bbbdfa-1c66-4428-ad89-272b41945433`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `J1939RmUpperComIPdu`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

Contains the configuration of the I-PDU that is sent from COM to J1939Rm.

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. J1939RmUpperComIPduId

- **UUID**: `ECUC:bc462154-84f8-45c6-bb6d-924ddc6947c6`
- **参数名**: `J1939RmUpperComIPduId`
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

############ 1. J1939RmUpperComIPduRef

- **UUID**: `ECUC:e1ebaf35-cb54-438c-8ee7-68c218ac6c1d`
- **引用名**: `J1939RmUpperComIPduRef`
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

####### 2. J1939RmComIPdu

**容器属性**:

- **UUID**: `ECUC:895c7730-bd1b-4c1a-819d-d5a5c83a0001`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `J1939RmComIPdu`
- **多重性**: [0..infinite]
- **构建后可变**: true
- **多配置容器**: false

**容器描述**:

Contains the configuration of an I-PDU that is to be transmitted on request by COM. This configuration container is only relevant for J1939RmUserType J1939RM_USER_COM.

######## 参数配置

此容器包含 **3** 个参数：

######### INTEGER 类型参数

########## 1. J1939RmComIPduDA

- **UUID**: `ECUC:319fe995-75c2-4673-9548-d6615a3911e1`
- **参数名**: `J1939RmComIPduDA`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..253]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Destination address of the COM I-PDU.

########## 2. J1939RmComIPduPGN

- **UUID**: `ECUC:e25ddae6-8a07-4ede-9340-dd08d4a54df3`
- **参数名**: `J1939RmComIPduPGN`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..262143]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: PGN of the COM I-PDU.

########## 3. J1939RmComIPduSA

- **UUID**: `ECUC:203a04b4-8064-46f2-9f2a-be9f3ce6391d`
- **参数名**: `J1939RmComIPduSA`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..253]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Source address of the COM I-PDU.

######## 配置容器

本模块包含 **2** 个配置容器：

######### 1. J1939RmLowerComIPdu

**容器属性**:

- **UUID**: `ECUC:7934f63c-95a7-4b79-8d06-02be6e0ea367`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `J1939RmLowerComIPdu`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

Contains the configuration of the I-PDU that is sent from J1939Rm to CanIf or J1939Tp.

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. J1939RmLowerComIPduId

- **UUID**: `ECUC:7338e5b5-35e0-491e-9aef-c4dffdf83796`
- **参数名**: `J1939RmLowerComIPduId`
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

############ 1. J1939RmLowerComIPduRef

- **UUID**: `ECUC:9f97cfd5-beb1-4cac-8b4f-fddb4554023b`
- **引用名**: `J1939RmLowerComIPduRef`
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

######### 2. J1939RmUpperComIPdu

**容器属性**:

- **UUID**: `ECUC:a8bbbdfa-1c66-4428-ad89-272b41945433`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `J1939RmUpperComIPdu`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

Contains the configuration of the I-PDU that is sent from COM to J1939Rm.

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. J1939RmUpperComIPduId

- **UUID**: `ECUC:bc462154-84f8-45c6-bb6d-924ddc6947c6`
- **参数名**: `J1939RmUpperComIPduId`
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

############ 1. J1939RmUpperComIPduRef

- **UUID**: `ECUC:e1ebaf35-cb54-438c-8ee7-68c218ac6c1d`
- **引用名**: `J1939RmUpperComIPduRef`
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

####### 3. J1939RmLowerComIPdu

**容器属性**:

- **UUID**: `ECUC:7934f63c-95a7-4b79-8d06-02be6e0ea367`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `J1939RmLowerComIPdu`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

Contains the configuration of the I-PDU that is sent from J1939Rm to CanIf or J1939Tp.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. J1939RmLowerComIPduId

- **UUID**: `ECUC:7338e5b5-35e0-491e-9aef-c4dffdf83796`
- **参数名**: `J1939RmLowerComIPduId`
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

########## 1. J1939RmLowerComIPduRef

- **UUID**: `ECUC:9f97cfd5-beb1-4cac-8b4f-fddb4554023b`
- **引用名**: `J1939RmLowerComIPduRef`
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

####### 4. J1939RmUpperComIPdu

**容器属性**:

- **UUID**: `ECUC:a8bbbdfa-1c66-4428-ad89-272b41945433`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `J1939RmUpperComIPdu`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

Contains the configuration of the I-PDU that is sent from COM to J1939Rm.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. J1939RmUpperComIPduId

- **UUID**: `ECUC:bc462154-84f8-45c6-bb6d-924ddc6947c6`
- **参数名**: `J1939RmUpperComIPduId`
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

########## 1. J1939RmUpperComIPduRef

- **UUID**: `ECUC:e1ebaf35-cb54-438c-8ee7-68c218ac6c1d`
- **引用名**: `J1939RmUpperComIPduRef`
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

##### 8. J1939RmUser

**容器属性**:

- **UUID**: `ECUC:e534c545-1a58-4f2f-8e41-95d1106733a8`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `J1939RmUser`
- **多重性**: [1..infinite]
- **构建后可变**: true
- **多配置容器**: false

**容器描述**:

Contains the configuration of a module that uses the request and acknowledgement interfaces of J1939Rm.

###### 参数配置

此容器包含 **10** 个参数：

####### INTEGER 类型参数

######## 1. J1939RmUserAckPGN

- **UUID**: `ECUC:37997ea0-3065-4aaa-a9e2-40bc6b88a3bc`
- **参数名**: `J1939RmUserAckPGN`
- **数据类型**: INTEGER
- **多重性**: [0..infinite]
- **取值范围**: [0..262143]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: PGN supported to be acknowledged to this module. The PGNs supported by different modules should usually be disjunctive. This parameter shall not be set for J1939RmUserType J1939RM_USER_J1939NM, J1939RM_USER_J1939DCM, and J1939RM_USER_COM.

######## 2. J1939RmUserComIPduRequestQueueSize

- **UUID**: `ECUC:b386ec3b-587c-4d51-ba58-98c6387c910c`
- **参数名**: `J1939RmUserComIPduRequestQueueSize`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Number of received requests that can be stored for COM I-PDUs of this user.

######## 3. J1939RmUserId

- **UUID**: `ECUC:1fe9bba9-b2d6-43c3-affc-43271705f1b7`
- **参数名**: `J1939RmUserId`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Identifier used by a module using J1939Rm. This parameter is only required when the module uses transmission of requests.

######## 4. J1939RmUserPGN

- **UUID**: `ECUC:0f89743c-31e4-49da-ad13-a85775c09d1b`
- **参数名**: `J1939RmUserPGN`
- **数据类型**: INTEGER
- **多重性**: [0..infinite]
- **取值范围**: [0..262143]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: PGN supported to be requested from this module. The PGNs supported by different modules should usually be disjunctive. This parameter is predefined to AC (0x0EE00) for J1939RmUserType J1939RM_USER_J1939NM and is derived from the J1939Dcm PDUs in the system description for J1939RmUserType J1939RM_USER_J1939DCM. It shall not be set for J1939RmUserType J1939RM_USER_COM.

####### BOOLEAN 类型参数

######## 1. J1939RmUserAckIndication

- **UUID**: `ECUC:67fed1f0-296d-4d40-9387-9481dc72a908`
- **参数名**: `J1939RmUserAckIndication`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enable AckIndication for this module. In case of CDD, the name is <apiServicePrefix>_AckIndication. In case of RTE, the port is defined as J1939RmRPort<J1939RmUserId>, and the operation is called AckIndication. This parameter shall not be set for J1939RmUserType J1939RM_USER_J1939NM, J1939RM_USER_J1939DCM, or J1939RM_USER_COM.

######## 2. J1939RmUserRequestIndication

- **UUID**: `ECUC:d4306c2d-71d4-41e5-b6c0-bc1354a535df`
- **参数名**: `J1939RmUserRequestIndication`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enable RequestIndication for this module. In case of J1939Nm or J1939Dcm, the name is fixed. In case of CDD, the name is <apiServicePrefix>_RequestIndication. In case of RTE, the port is defined as J1939RmRPort<J1939RmUserId>, and the operation is called RequestIndication. This parameter shall not be set for J1939RmUserType J1939RM_USER_COM.

######## 3. J1939RmUserSendAck

- **UUID**: `ECUC:8311a6fb-8b7b-41ff-8de9-c1d692af5ca4`
- **参数名**: `J1939RmUserSendAck`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enable the SendAck API for this module. In case of RTE, the port is defined as J1939RmPPort<J1939RmUserId>, and the operation is called SendAck. This parameter shall not be set for J1939RmUserType J1939RM_USER_J1939NM or J1939RM_USER_COM.

######## 4. J1939RmUserSendRequest

- **UUID**: `ECUC:1466d83f-619c-4bc9-9e6f-cc6c27153c4b`
- **参数名**: `J1939RmUserSendRequest`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enable the SendRequest API for this module. In case of RTE, the port is defined as J1939RmPPort<J1939RmUserId>, and the operation is called SendRequest. This parameter shall not be set for J1939RmUserType J1939RM_USER_J1939NM, J1939RM_USER_J1939DCM, or J1939RM_USER_COM.

######## 5. J1939RmUserTimeoutSupervision

- **UUID**: `ECUC:a5425ede-c411-4f83-af88-3a68127893d3`
- **参数名**: `J1939RmUserTimeoutSupervision`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enable RequestTimeoutIndication and CancelRequestTimeout for this module. RequestTimeoutIndication: In case of CDD, the name is <apiServicePrefix>_RequestTimeoutIndication.

####### ENUMERATION 类型参数

######## 1. J1939RmUserType

- **UUID**: `ECUC:ee94106e-ef27-4982-a16f-8380a6eb1794`
- **参数名**: `J1939RmUserType`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `J1939RM_CDD` (来源: AUTOSAR_ECUC)
  - `J1939RM_RTE` (来源: AUTOSAR_ECUC)
  - `J1939RM_USER_COM` (来源: AUTOSAR_ECUC)
  - `J1939RM_USER_J1939DCM` (来源: AUTOSAR_ECUC)
  - `J1939RM_USER_J1939NM` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Type of module using J1939Rm.

###### 引用关系

此容器包含 **1** 个引用：

####### FOREIGN-REFERENCE 类型引用

######## 1. J1939RmUserCddRef

- **UUID**: `ECUC:074f9e81-f250-420f-b47c-2fd7c9430c42`
- **引用名**: `J1939RmUserCddRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [0..1]
- **目标类型**: ECUC-MODULE-CONFIGURATION-VALUES
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the CDD module description. This parameter is only required for J1939RmUserType J1939RM_USER_CDD.

###### 配置容器

本模块包含 **3** 个配置容器：

####### 1. J1939RmComIPdu

**容器属性**:

- **UUID**: `ECUC:895c7730-bd1b-4c1a-819d-d5a5c83a0001`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `J1939RmComIPdu`
- **多重性**: [0..infinite]
- **构建后可变**: true
- **多配置容器**: false

**容器描述**:

Contains the configuration of an I-PDU that is to be transmitted on request by COM. This configuration container is only relevant for J1939RmUserType J1939RM_USER_COM.

######## 参数配置

此容器包含 **3** 个参数：

######### INTEGER 类型参数

########## 1. J1939RmComIPduDA

- **UUID**: `ECUC:319fe995-75c2-4673-9548-d6615a3911e1`
- **参数名**: `J1939RmComIPduDA`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..253]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Destination address of the COM I-PDU.

########## 2. J1939RmComIPduPGN

- **UUID**: `ECUC:e25ddae6-8a07-4ede-9340-dd08d4a54df3`
- **参数名**: `J1939RmComIPduPGN`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..262143]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: PGN of the COM I-PDU.

########## 3. J1939RmComIPduSA

- **UUID**: `ECUC:203a04b4-8064-46f2-9f2a-be9f3ce6391d`
- **参数名**: `J1939RmComIPduSA`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..253]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Source address of the COM I-PDU.

######## 配置容器

本模块包含 **2** 个配置容器：

######### 1. J1939RmLowerComIPdu

**容器属性**:

- **UUID**: `ECUC:7934f63c-95a7-4b79-8d06-02be6e0ea367`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `J1939RmLowerComIPdu`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

Contains the configuration of the I-PDU that is sent from J1939Rm to CanIf or J1939Tp.

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. J1939RmLowerComIPduId

- **UUID**: `ECUC:7338e5b5-35e0-491e-9aef-c4dffdf83796`
- **参数名**: `J1939RmLowerComIPduId`
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

############ 1. J1939RmLowerComIPduRef

- **UUID**: `ECUC:9f97cfd5-beb1-4cac-8b4f-fddb4554023b`
- **引用名**: `J1939RmLowerComIPduRef`
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

######### 2. J1939RmUpperComIPdu

**容器属性**:

- **UUID**: `ECUC:a8bbbdfa-1c66-4428-ad89-272b41945433`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `J1939RmUpperComIPdu`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

Contains the configuration of the I-PDU that is sent from COM to J1939Rm.

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. J1939RmUpperComIPduId

- **UUID**: `ECUC:bc462154-84f8-45c6-bb6d-924ddc6947c6`
- **参数名**: `J1939RmUpperComIPduId`
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

############ 1. J1939RmUpperComIPduRef

- **UUID**: `ECUC:e1ebaf35-cb54-438c-8ee7-68c218ac6c1d`
- **引用名**: `J1939RmUpperComIPduRef`
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

####### 2. J1939RmLowerComIPdu

**容器属性**:

- **UUID**: `ECUC:7934f63c-95a7-4b79-8d06-02be6e0ea367`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `J1939RmLowerComIPdu`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

Contains the configuration of the I-PDU that is sent from J1939Rm to CanIf or J1939Tp.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. J1939RmLowerComIPduId

- **UUID**: `ECUC:7338e5b5-35e0-491e-9aef-c4dffdf83796`
- **参数名**: `J1939RmLowerComIPduId`
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

########## 1. J1939RmLowerComIPduRef

- **UUID**: `ECUC:9f97cfd5-beb1-4cac-8b4f-fddb4554023b`
- **引用名**: `J1939RmLowerComIPduRef`
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

####### 3. J1939RmUpperComIPdu

**容器属性**:

- **UUID**: `ECUC:a8bbbdfa-1c66-4428-ad89-272b41945433`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `J1939RmUpperComIPdu`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

Contains the configuration of the I-PDU that is sent from COM to J1939Rm.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. J1939RmUpperComIPduId

- **UUID**: `ECUC:bc462154-84f8-45c6-bb6d-924ddc6947c6`
- **参数名**: `J1939RmUpperComIPduId`
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

########## 1. J1939RmUpperComIPduRef

- **UUID**: `ECUC:e1ebaf35-cb54-438c-8ee7-68c218ac6c1d`
- **引用名**: `J1939RmUpperComIPduRef`
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

##### 9. J1939RmComIPdu

**容器属性**:

- **UUID**: `ECUC:895c7730-bd1b-4c1a-819d-d5a5c83a0001`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `J1939RmComIPdu`
- **多重性**: [0..infinite]
- **构建后可变**: true
- **多配置容器**: false

**容器描述**:

Contains the configuration of an I-PDU that is to be transmitted on request by COM. This configuration container is only relevant for J1939RmUserType J1939RM_USER_COM.

###### 参数配置

此容器包含 **3** 个参数：

####### INTEGER 类型参数

######## 1. J1939RmComIPduDA

- **UUID**: `ECUC:319fe995-75c2-4673-9548-d6615a3911e1`
- **参数名**: `J1939RmComIPduDA`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..253]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Destination address of the COM I-PDU.

######## 2. J1939RmComIPduPGN

- **UUID**: `ECUC:e25ddae6-8a07-4ede-9340-dd08d4a54df3`
- **参数名**: `J1939RmComIPduPGN`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..262143]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: PGN of the COM I-PDU.

######## 3. J1939RmComIPduSA

- **UUID**: `ECUC:203a04b4-8064-46f2-9f2a-be9f3ce6391d`
- **参数名**: `J1939RmComIPduSA`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..253]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Source address of the COM I-PDU.

###### 配置容器

本模块包含 **2** 个配置容器：

####### 1. J1939RmLowerComIPdu

**容器属性**:

- **UUID**: `ECUC:7934f63c-95a7-4b79-8d06-02be6e0ea367`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `J1939RmLowerComIPdu`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

Contains the configuration of the I-PDU that is sent from J1939Rm to CanIf or J1939Tp.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. J1939RmLowerComIPduId

- **UUID**: `ECUC:7338e5b5-35e0-491e-9aef-c4dffdf83796`
- **参数名**: `J1939RmLowerComIPduId`
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

########## 1. J1939RmLowerComIPduRef

- **UUID**: `ECUC:9f97cfd5-beb1-4cac-8b4f-fddb4554023b`
- **引用名**: `J1939RmLowerComIPduRef`
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

####### 2. J1939RmUpperComIPdu

**容器属性**:

- **UUID**: `ECUC:a8bbbdfa-1c66-4428-ad89-272b41945433`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `J1939RmUpperComIPdu`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

Contains the configuration of the I-PDU that is sent from COM to J1939Rm.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. J1939RmUpperComIPduId

- **UUID**: `ECUC:bc462154-84f8-45c6-bb6d-924ddc6947c6`
- **参数名**: `J1939RmUpperComIPduId`
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

########## 1. J1939RmUpperComIPduRef

- **UUID**: `ECUC:e1ebaf35-cb54-438c-8ee7-68c218ac6c1d`
- **引用名**: `J1939RmUpperComIPduRef`
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

##### 10. J1939RmLowerComIPdu

**容器属性**:

- **UUID**: `ECUC:7934f63c-95a7-4b79-8d06-02be6e0ea367`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `J1939RmLowerComIPdu`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

Contains the configuration of the I-PDU that is sent from J1939Rm to CanIf or J1939Tp.

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. J1939RmLowerComIPduId

- **UUID**: `ECUC:7338e5b5-35e0-491e-9aef-c4dffdf83796`
- **参数名**: `J1939RmLowerComIPduId`
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

######## 1. J1939RmLowerComIPduRef

- **UUID**: `ECUC:9f97cfd5-beb1-4cac-8b4f-fddb4554023b`
- **引用名**: `J1939RmLowerComIPduRef`
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

##### 11. J1939RmUpperComIPdu

**容器属性**:

- **UUID**: `ECUC:a8bbbdfa-1c66-4428-ad89-272b41945433`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `J1939RmUpperComIPdu`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

Contains the configuration of the I-PDU that is sent from COM to J1939Rm.

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. J1939RmUpperComIPduId

- **UUID**: `ECUC:bc462154-84f8-45c6-bb6d-924ddc6947c6`
- **参数名**: `J1939RmUpperComIPduId`
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

######## 1. J1939RmUpperComIPduRef

- **UUID**: `ECUC:e1ebaf35-cb54-438c-8ee7-68c218ac6c1d`
- **引用名**: `J1939RmUpperComIPduRef`
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

##### 12. J1939RmGeneral

**容器属性**:

- **UUID**: `ECUC:5b511604-71f4-4fcc-855b-e14dfcf98b78`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `J1939RmGeneral`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

Contains the general configuration parameters of the module.

###### 参数配置

此容器包含 **9** 个参数：

####### BOOLEAN 类型参数

######## 1. J1939RmDevErrorDetect

- **UUID**: `ECUC:ceb44cc8-860f-44f9-bd1a-ffa67730e875`
- **参数名**: `J1939RmDevErrorDetect`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Pre-processor switch for enabling development error detection support.

######## 2. J1939RmSupportAckIndication

- **UUID**: `ECUC:3604d400-de3f-4289-8096-b362ad169b62`
- **参数名**: `J1939RmSupportAckIndication`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Pre-processor switch for enabling support of acknowledgement indications.

######## 3. J1939RmSupportAckTransmission

- **UUID**: `ECUC:bb26d6d7-9043-4363-b73e-e4831744d154`
- **参数名**: `J1939RmSupportAckTransmission`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Pre-processor switch for enabling support of acknowledgement transmission.

######## 4. J1939RmSupportRequestIndication

- **UUID**: `ECUC:dfb17ab4-18dd-4573-9991-b5542658f1cf`
- **参数名**: `J1939RmSupportRequestIndication`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Pre-processor switch for enabling support of request indications.

######## 5. J1939RmSupportRequestTransmission

- **UUID**: `ECUC:49750482-096b-4af9-a961-9239859cfb16`
- **参数名**: `J1939RmSupportRequestTransmission`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Pre-processor switch for enabling support of request transmission.

######## 6. J1939RmSupportTimeoutSupervision

- **UUID**: `ECUC:a598ff50-095c-4c40-bd21-79db6bf6a85a`
- **参数名**: `J1939RmSupportTimeoutSupervision`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Pre-processor switch for enabling support of request timeout supervision.

######## 7. J1939RmVersionInfoApi

- **UUID**: `ECUC:48e29e97-ddfd-4ada-b709-5f4891496e07`
- **参数名**: `J1939RmVersionInfoApi`
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

######## 1. J1939RmMainFunctionPeriod

- **UUID**: `ECUC:d465d8dd-0f52-4781-976e-90c74758483a`
- **参数名**: `J1939RmMainFunctionPeriod`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0.001..0.255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Execution cycle of J1939Rm_MainFunction in seconds.

######## 2. J1939RmTxConfirmationTimeout

- **UUID**: `ECUC:4d1b62b1-1dc5-42d1-96ab-2108c6b5374f`
- **参数名**: `J1939RmTxConfirmationTimeout`
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

1. **J1939Rm**
