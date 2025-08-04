# FrTp - 完整配置文档

*此文档由ARXML文件自动生成，采用层次化结构展示*

**生成时间**: 2025-06-16 14:51:48

## 📑 目录

- [📄 文件信息](#-文件信息)
- [🔧 模块定义](#-模块定义)
  - [FrTp](#frtp)
- [📦 包结构](#-包结构)

## 📄 文件信息

### Schema信息
- **Schema位置**: `http://autosar.org/schema/r4.0 AUTOSAR_4-0-3.xsd`
- **命名空间**: `http://autosar.org/schema/r4.0`

## 🔧 模块定义

### 1. FrTp

#### 基本信息

- **UUID**: `ECUC:2934096d-28a8-4cd7-bd56-5cd7c19809ba`
- **模块名称**: `FrTp`
- **多重性**: [0..1]
- **支持的变体**:
  - VARIANT-POST-BUILD
  - VARIANT-PRE-COMPILE

#### 模块描述

Configuration of the FlexRay Transport Protocol module according to ISO 10681-2.

#### 版本历史

共有 **1** 个版本记录：

##### 1. 版本 4.2.0

- **发布日期**: 2011-11-09
- **发布者**: AUTOSAR

*此版本无详细变更记录*

#### 配置容器

本模块包含 **10** 个配置容器：

##### 1. FrTpGeneral

**容器属性**:

- **UUID**: `ECUC:75dd14c2-0fdb-4fa2-9ab7-002e922049a1`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FrTpGeneral`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

This container contains the general configuration parameters of the FlexRay Transport Protocol module.

###### 参数配置

此容器包含 **9** 个参数：

####### INTEGER 类型参数

######## 1. FrTpChanNum

- **UUID**: `ECUC:2c60f0d8-b645-49c3-9ae1-2a9d9c5ca3af`
- **参数名**: `FrTpChanNum`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..32]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Preprocessor switch for defining the number of concurrent channels the module supports. Up to 32 channels shall be definable here.

####### BOOLEAN 类型参数

######## 1. FrTpAckRt

- **UUID**: `ECUC:7910a674-32c7-4b67-8eea-598e80fc2e55`
- **参数名**: `FrTpAckRt`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Preprocessor switch for enabling the Acknowledgement and retry mechanisms.

######## 2. FrTpChangeParamApi

- **UUID**: `ECUC:85e4b12b-782f-4e3d-8e90-02c5c3f6f023`
- **参数名**: `FrTpChangeParamApi`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Preprocessor switch for enabling the API to change FrTp communication

######## 3. FrTpDevErrorDetect

- **UUID**: `ECUC:dbe9dcee-eb95-48ec-9f9a-f6cb24e443c9`
- **参数名**: `FrTpDevErrorDetect`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Preprocessor switch for enabling development error detection.

######## 4. FrTpFullDuplexEnable

- **UUID**: `ECUC:6db47148-f6bc-438a-9a44-b2866e298b45`
- **参数名**: `FrTpFullDuplexEnable`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Preprocessor switch for enabling full duplex mechanisms for all channels.

######## 5. FrTpTransmitCancellation

- **UUID**: `ECUC:23763db2-59f4-4aa4-9b85-2c275c821b27`
- **参数名**: `FrTpTransmitCancellation`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Preprocessor switch for enabling Transmit Cancellation.

######## 6. FrTpUnknownMsgLength

- **UUID**: `ECUC:c226ddd7-ae28-4cdd-baca-791fe3cad4e1`
- **参数名**: `FrTpUnknownMsgLength`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Preprocessor switch to support data transfer with unknown message length.

######## 7. FrTpVersionInfoApi

- **UUID**: `ECUC:8ce0d461-1481-4f38-b0f2-dbbb6739c42f`
- **参数名**: `FrTpVersionInfoApi`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Preprocessor switch for enabling the Version info API.

####### FLOAT 类型参数

######## 1. FrTpMainFuncCycle

- **UUID**: `ECUC:5856a139-09b4-4ca8-9bcb-75382ffadae4`
- **参数名**: `FrTpMainFuncCycle`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0..Inf]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter contains the calling period of the TPs Main Function. The parameter is specified in seconds.

##### 2. FrTpMultipleConfig

**容器属性**:

- **UUID**: `ECUC:a9475420-4a73-4ce4-83bb-b93a5cee8dff`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FrTpMultipleConfig`
- **多重性**: [1..1]
- **多配置容器**: true

**容器描述**:

This container holds one or several multiple configuration sets.

###### 配置容器

本模块包含 **8** 个配置容器：

####### 1. FrTpConnection

**容器属性**:

- **UUID**: `ECUC:daf437b6-aa4f-4ef5-92b5-33874ada757a`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FrTpConnection`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

This container contains the connection specific parameters to transfer N-PDUs via FlexRay TP.

######## 参数配置

此容器包含 **4** 个参数：

######### INTEGER 类型参数

########## 1. FrTpLa

- **UUID**: `ECUC:132fb4bd-1955-4930-8d55-7ac3532fdfaf`
- **参数名**: `FrTpLa`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the Local Address for the respective connection. When the local instance is the sender, this is the Source Address within the TP frame. When the local instance is the receiver, this is the Target Address within the TP frame.

########## 2. FrTpRa

- **UUID**: `ECUC:e213f58a-7e1f-4d2a-a4d3-1605a5a82429`
- **参数名**: `FrTpRa`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the Remote Address for the respective connection. When the local instance is the sender, this is the Target Address within the TP frame. When the local instance is the receiver, this is the Source Address within the TP frame.

######### BOOLEAN 类型参数

########## 1. FrTpBandwidthLimitation

- **UUID**: `ECUC:be5bca90-0e33-4c7d-87ad-76dec2d0d2aa`
- **参数名**: `FrTpBandwidthLimitation`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter indicates wheather the connection requires a  bandwidth limitation or not. If FrTpBandwidthLimitation=True the sender shall send a StartFrame always on the first PDU of a PDU-Pool.

########## 2. FrTpMultipleReceiverCon

- **UUID**: `ECUC:3dbd0c29-a62d-4d7b-b708-151974cd4b20`
- **参数名**: `FrTpMultipleReceiverCon`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines, whether this connection is an 1:1 ('false') or an 1:n ('true') connection. If data segmentation is required this parameter is used to check whether segmentation is possible or not. If the connection is 1:n segmentation is not possible and an error will occur.

######## 引用关系

此容器包含 **3** 个引用：

######### REFERENCE 类型引用

########## 1. FrTpConCtrlRef

- **UUID**: `ECUC:af3befcd-45e9-4148-8faf-64746c35f94f`
- **引用名**: `FrTpConCtrlRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `FrTpConnectionControl`
- **完整路径**: `/AUTOSAR/EcucDefs/FrTp/FrTpMultipleConfig/FrTpConnectionControl`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: FrTpConnectionControlReference:

########## 2. FrTpRxPduPoolRef

- **UUID**: `ECUC:e0933913-63de-43ec-8cb5-422fc5309288`
- **引用名**: `FrTpRxPduPoolRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `FrTpRxPduPool`
- **完整路径**: `/AUTOSAR/EcucDefs/FrTp/FrTpMultipleConfig/FrTpRxPduPool`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines a reference to a RxPduPool.

########## 3. FrTpTxPduPoolRef

- **UUID**: `ECUC:ad5e9a14-327d-4303-ae3e-a8b729639193`
- **引用名**: `FrTpTxPduPoolRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `FrTpTxPduPool`
- **完整路径**: `/AUTOSAR/EcucDefs/FrTp/FrTpMultipleConfig/FrTpTxPduPool`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines a reference to a TxPduPool.

######## 配置容器

本模块包含 **2** 个配置容器：

######### 1. FrTpRxSdu

**容器属性**:

- **UUID**: `ECUC:2bebf6ec-219e-49af-8dc8-94e116335a8d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FrTpRxSdu`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This parameter defines the Rx Service Data Unit Identifier (Sdu Id) which uniquely identifies a data transfer (inter-module communication) between FrTp and PDUR.

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. FrTpRxSduId

- **UUID**: `ECUC:3a245a98-cfc3-4f4f-9f95-ed00110038ff`
- **参数名**: `FrTpRxSduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This unique identifier is used for change parameter request or receive cancellation from PduR to FrTp.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. FrTpRxSduRef

- **UUID**: `ECUC:4876e7cb-860a-4233-81db-4a2de8244c33`
- **引用名**: `FrTpRxSduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a PDU in the global PDU structure.

######### 2. FrTpTxSdu

**容器属性**:

- **UUID**: `ECUC:3d26dff5-3b62-4c38-8032-519b289f59bf`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FrTpTxSdu`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This parameter defines the Tx Service Data Unit Identifier (Sdu Id) which uniquely identifies a data transfer (inter-module communication) between FrTp and PDUR.

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. FrTpTxSduId

- **UUID**: `ECUC:486179ae-7b2e-4d16-8eb9-ffc5a767c23c`
- **参数名**: `FrTpTxSduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a unique identifier for a to be transmitted message from the PduR to the FrTp.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. FrTpTxSduRef

- **UUID**: `ECUC:53652bde-41b6-4054-9bf8-bec6d6f95359`
- **引用名**: `FrTpTxSduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a PDU in the global PDU structure.

####### 2. FrTpRxSdu

**容器属性**:

- **UUID**: `ECUC:2bebf6ec-219e-49af-8dc8-94e116335a8d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FrTpRxSdu`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This parameter defines the Rx Service Data Unit Identifier (Sdu Id) which uniquely identifies a data transfer (inter-module communication) between FrTp and PDUR.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. FrTpRxSduId

- **UUID**: `ECUC:3a245a98-cfc3-4f4f-9f95-ed00110038ff`
- **参数名**: `FrTpRxSduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This unique identifier is used for change parameter request or receive cancellation from PduR to FrTp.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. FrTpRxSduRef

- **UUID**: `ECUC:4876e7cb-860a-4233-81db-4a2de8244c33`
- **引用名**: `FrTpRxSduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a PDU in the global PDU structure.

####### 3. FrTpTxSdu

**容器属性**:

- **UUID**: `ECUC:3d26dff5-3b62-4c38-8032-519b289f59bf`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FrTpTxSdu`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This parameter defines the Tx Service Data Unit Identifier (Sdu Id) which uniquely identifies a data transfer (inter-module communication) between FrTp and PDUR.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. FrTpTxSduId

- **UUID**: `ECUC:486179ae-7b2e-4d16-8eb9-ffc5a767c23c`
- **参数名**: `FrTpTxSduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a unique identifier for a to be transmitted message from the PduR to the FrTp.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. FrTpTxSduRef

- **UUID**: `ECUC:53652bde-41b6-4054-9bf8-bec6d6f95359`
- **引用名**: `FrTpTxSduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a PDU in the global PDU structure.

####### 4. FrTpConnectionControl

**容器属性**:

- **UUID**: `ECUC:9ae16791-5e2f-424a-9867-babf691ec3ee`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FrTpConnectionControl`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

This container contains the configuration parameters to control a FlexRay TP connection.

######## 参数配置

此容器包含 **16** 个参数：

######### INTEGER 类型参数

########## 1. FrTpMaxAr

- **UUID**: `ECUC:f92ab95e-285b-447b-b59a-c96296678562`
- **参数名**: `FrTpMaxAr`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the maximum number of trying to send a frame when a TIMEOUT AR occurs.

########## 2. FrTpMaxAs

- **UUID**: `ECUC:f544ed50-692f-4eac-b06e-725f44195f93`
- **参数名**: `FrTpMaxAs`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the maximum number of trying to send a frame when a TIMEOUT AS occurs.

########## 3. FrTpMaxBufferSize

- **UUID**: `ECUC:7f017436-3c7f-46e9-8409-766990b33763`
- **参数名**: `FrTpMaxBufferSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Limits the maximal buffer size the FrTp can choose in order to limit the amount of Tx buffer that will be requested at the sender side in a segmented transfer.

########## 4. FrTpMaxFCWait

- **UUID**: `ECUC:eddb6d0e-550b-4ff2-9c0f-bdad7c7d5462`
- **参数名**: `FrTpMaxFCWait`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the maximum number of FlowControl N-PDUs with FlowState "WAIT"

########## 5. FrTpMaxFrIf

- **UUID**: `ECUC:668f68b3-42bf-40fa-a0b6-2076a2974f93`
- **参数名**: `FrTpMaxFrIf`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the maximum number of trying to send a frame when the FrIf returns an error.

########## 6. FrTpMaxNbrOfNPduPerCycle

- **UUID**: `ECUC:511499e2-c997-4664-b839-cd6fcc37e817`
- **参数名**: `FrTpMaxNbrOfNPduPerCycle`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..31]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter is part of the ISO 10681-2 protocol's FlowControl parameter "Bandwidth Control (BC)". It limits the number of N-Pdus the sender is allowed to transmit within a FlexRay cycle.

########## 7. FrTpMaxRn

- **UUID**: `ECUC:22705c63-9e4a-43a8-a155-2ea0d0e299be`
- **参数名**: `FrTpMaxRn`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the maximum number of retries (if retry is configured).

########## 8. FrTpSCexp

- **UUID**: `ECUC:39029fbb-3d5b-482c-ab05-041cd8751234`
- **参数名**: `FrTpSCexp`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..7]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter is part of the ISO 10681-2 protocol's FlowControl parameter "Bandwidth Control (BC)". It represents the exponent to calculate the minimum number of "Separation Cycles" the sender has to wait for the next transmission of an FrTp N-Pdu.

######### FLOAT 类型参数

########## 1. FrTpTimeBr

- **UUID**: `ECUC:e160a206-95b9-4917-8862-427d65dcc2a0`
- **参数名**: `FrTpTimeBr`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0..0.255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the time in seconds the FrTp requires to transmit a corresponding FlowControl Frame. According to ISO 10681-2 this parameter is a performance requirement.

########## 2. FrTpTimeBuffer

- **UUID**: `ECUC:7e2e5b1b-ae37-4a23-bf2f-32c4bf862e1c`
- **参数名**: `FrTpTimeBuffer`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0..65.535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the time in seconds of waiting for the next try to get a Tx or Rx buffer.

########## 3. FrTpTimeFrIf

- **UUID**: `ECUC:48fc4037-c3db-46b3-94ef-440242853af1`
- **参数名**: `FrTpTimeFrIf`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0..0.255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the time in seconds of waiting for the next try (if retry is activated) to send via FrIf_Transmit.

########## 4. FrTpTimeoutAr

- **UUID**: `ECUC:90038b23-567e-421d-a35c-f82da1d7f0da`
- **参数名**: `FrTpTimeoutAr`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0..65.535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter states the timeout in seconds between the PDU transmit request of the Transport Layer to the FlexRay Interface and the corresponding confirmation of the FlexRay Interface on the receiver side (for FC or AF).

########## 5. FrTpTimeoutAs

- **UUID**: `ECUC:a673b7e0-8b68-4be7-9447-8b9a19e4cfa0`
- **参数名**: `FrTpTimeoutAs`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0..65.535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter specifies the timeout in seconds the FrIf shall confirm a transmitted Pdu to the FrTp.

########## 6. FrTpTimeoutBs

- **UUID**: `ECUC:2ba00d4a-1079-4f0d-936a-5db48acd8cce`
- **参数名**: `FrTpTimeoutBs`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0..65.535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the timeout in seconds for waiting for an FC or AF on the sender side in a 1:1 connection.

########## 7. FrTpTimeoutCr

- **UUID**: `ECUC:2a9422c2-8b51-4ec5-9ab5-3f5a8e8dde97`
- **参数名**: `FrTpTimeoutCr`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0..65.535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the timeout value in seconds a receiver is waiting for a CF or a LF.

######### ENUMERATION 类型参数

########## 1. FrTpAckType

- **UUID**: `ECUC:45e13963-200d-45a5-96e5-3267c92c0ac0`
- **参数名**: `FrTpAckType`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `FRTP_ACK_WITH_RT` (来源: AUTOSAR_ECUC)
  - `FRTP_NO` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the type of acknowledgement which is used for the specific channel.

####### 5. FrTpRxPduPool

**容器属性**:

- **UUID**: `ECUC:78a80c22-51d9-4999-897d-a64c3be59fad`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FrTpRxPduPool`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

This container contains all Pdus that are assigned to that Pdu Pool.

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. FrTpRxPdu

**容器属性**:

- **UUID**: `ECUC:293a3123-98f2-43d0-a74b-3708e5688631`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FrTpRxPdu`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

Container to hold the PDU parameters.

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. FrTpRxPduId

- **UUID**: `ECUC:2ed97a0f-0bee-481c-b44c-303a5f9b4c63`
- **参数名**: `FrTpRxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a unique identifier for a received message which is forwarded from the FrIf to the FrTp.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. FrTpRxPduRef

- **UUID**: `ECUC:57804f45-2cd4-47ec-b5ec-70bd2676da01`
- **引用名**: `FrTpRxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a PDU in the global PDU structure.

####### 6. FrTpRxPdu

**容器属性**:

- **UUID**: `ECUC:293a3123-98f2-43d0-a74b-3708e5688631`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FrTpRxPdu`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

Container to hold the PDU parameters.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. FrTpRxPduId

- **UUID**: `ECUC:2ed97a0f-0bee-481c-b44c-303a5f9b4c63`
- **参数名**: `FrTpRxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a unique identifier for a received message which is forwarded from the FrIf to the FrTp.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. FrTpRxPduRef

- **UUID**: `ECUC:57804f45-2cd4-47ec-b5ec-70bd2676da01`
- **引用名**: `FrTpRxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a PDU in the global PDU structure.

####### 7. FrTpTxPduPool

**容器属性**:

- **UUID**: `ECUC:a2415a14-8390-4b76-b88b-32b28bef741d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FrTpTxPduPool`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

This container contains all Pdus that are assigned to that Pdu Pool.

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. FrTpTxPdu

**容器属性**:

- **UUID**: `ECUC:6c3c184f-27ba-4e88-a02e-b7da04d5d309`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FrTpTxPdu`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

Container to hold the PDU parameters.

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. FrTpTxConfirmationPduId

- **UUID**: `ECUC:8324381f-3689-4616-8019-8b490ac93f8a`
- **参数名**: `FrTpTxConfirmationPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Handle Id to be used by the FrIf to confirm the transmission of the FrTpTxPdu to the FrIf module.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. FrTpTxPduRef

- **UUID**: `ECUC:29602a84-6c32-4014-8e25-d597b357b5ea`
- **引用名**: `FrTpTxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a PDU in the global PDU structure.

####### 8. FrTpTxPdu

**容器属性**:

- **UUID**: `ECUC:6c3c184f-27ba-4e88-a02e-b7da04d5d309`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FrTpTxPdu`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

Container to hold the PDU parameters.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. FrTpTxConfirmationPduId

- **UUID**: `ECUC:8324381f-3689-4616-8019-8b490ac93f8a`
- **参数名**: `FrTpTxConfirmationPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Handle Id to be used by the FrIf to confirm the transmission of the FrTpTxPdu to the FrIf module.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. FrTpTxPduRef

- **UUID**: `ECUC:29602a84-6c32-4014-8e25-d597b357b5ea`
- **引用名**: `FrTpTxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a PDU in the global PDU structure.

##### 3. FrTpConnection

**容器属性**:

- **UUID**: `ECUC:daf437b6-aa4f-4ef5-92b5-33874ada757a`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FrTpConnection`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

This container contains the connection specific parameters to transfer N-PDUs via FlexRay TP.

###### 参数配置

此容器包含 **4** 个参数：

####### INTEGER 类型参数

######## 1. FrTpLa

- **UUID**: `ECUC:132fb4bd-1955-4930-8d55-7ac3532fdfaf`
- **参数名**: `FrTpLa`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the Local Address for the respective connection. When the local instance is the sender, this is the Source Address within the TP frame. When the local instance is the receiver, this is the Target Address within the TP frame.

######## 2. FrTpRa

- **UUID**: `ECUC:e213f58a-7e1f-4d2a-a4d3-1605a5a82429`
- **参数名**: `FrTpRa`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the Remote Address for the respective connection. When the local instance is the sender, this is the Target Address within the TP frame. When the local instance is the receiver, this is the Source Address within the TP frame.

####### BOOLEAN 类型参数

######## 1. FrTpBandwidthLimitation

- **UUID**: `ECUC:be5bca90-0e33-4c7d-87ad-76dec2d0d2aa`
- **参数名**: `FrTpBandwidthLimitation`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter indicates wheather the connection requires a  bandwidth limitation or not. If FrTpBandwidthLimitation=True the sender shall send a StartFrame always on the first PDU of a PDU-Pool.

######## 2. FrTpMultipleReceiverCon

- **UUID**: `ECUC:3dbd0c29-a62d-4d7b-b708-151974cd4b20`
- **参数名**: `FrTpMultipleReceiverCon`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines, whether this connection is an 1:1 ('false') or an 1:n ('true') connection. If data segmentation is required this parameter is used to check whether segmentation is possible or not. If the connection is 1:n segmentation is not possible and an error will occur.

###### 引用关系

此容器包含 **3** 个引用：

####### REFERENCE 类型引用

######## 1. FrTpConCtrlRef

- **UUID**: `ECUC:af3befcd-45e9-4148-8faf-64746c35f94f`
- **引用名**: `FrTpConCtrlRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `FrTpConnectionControl`
- **完整路径**: `/AUTOSAR/EcucDefs/FrTp/FrTpMultipleConfig/FrTpConnectionControl`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: FrTpConnectionControlReference:

######## 2. FrTpRxPduPoolRef

- **UUID**: `ECUC:e0933913-63de-43ec-8cb5-422fc5309288`
- **引用名**: `FrTpRxPduPoolRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `FrTpRxPduPool`
- **完整路径**: `/AUTOSAR/EcucDefs/FrTp/FrTpMultipleConfig/FrTpRxPduPool`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines a reference to a RxPduPool.

######## 3. FrTpTxPduPoolRef

- **UUID**: `ECUC:ad5e9a14-327d-4303-ae3e-a8b729639193`
- **引用名**: `FrTpTxPduPoolRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `FrTpTxPduPool`
- **完整路径**: `/AUTOSAR/EcucDefs/FrTp/FrTpMultipleConfig/FrTpTxPduPool`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines a reference to a TxPduPool.

###### 配置容器

本模块包含 **2** 个配置容器：

####### 1. FrTpRxSdu

**容器属性**:

- **UUID**: `ECUC:2bebf6ec-219e-49af-8dc8-94e116335a8d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FrTpRxSdu`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This parameter defines the Rx Service Data Unit Identifier (Sdu Id) which uniquely identifies a data transfer (inter-module communication) between FrTp and PDUR.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. FrTpRxSduId

- **UUID**: `ECUC:3a245a98-cfc3-4f4f-9f95-ed00110038ff`
- **参数名**: `FrTpRxSduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This unique identifier is used for change parameter request or receive cancellation from PduR to FrTp.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. FrTpRxSduRef

- **UUID**: `ECUC:4876e7cb-860a-4233-81db-4a2de8244c33`
- **引用名**: `FrTpRxSduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a PDU in the global PDU structure.

####### 2. FrTpTxSdu

**容器属性**:

- **UUID**: `ECUC:3d26dff5-3b62-4c38-8032-519b289f59bf`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FrTpTxSdu`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This parameter defines the Tx Service Data Unit Identifier (Sdu Id) which uniquely identifies a data transfer (inter-module communication) between FrTp and PDUR.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. FrTpTxSduId

- **UUID**: `ECUC:486179ae-7b2e-4d16-8eb9-ffc5a767c23c`
- **参数名**: `FrTpTxSduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a unique identifier for a to be transmitted message from the PduR to the FrTp.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. FrTpTxSduRef

- **UUID**: `ECUC:53652bde-41b6-4054-9bf8-bec6d6f95359`
- **引用名**: `FrTpTxSduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a PDU in the global PDU structure.

##### 4. FrTpRxSdu

**容器属性**:

- **UUID**: `ECUC:2bebf6ec-219e-49af-8dc8-94e116335a8d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FrTpRxSdu`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This parameter defines the Rx Service Data Unit Identifier (Sdu Id) which uniquely identifies a data transfer (inter-module communication) between FrTp and PDUR.

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. FrTpRxSduId

- **UUID**: `ECUC:3a245a98-cfc3-4f4f-9f95-ed00110038ff`
- **参数名**: `FrTpRxSduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This unique identifier is used for change parameter request or receive cancellation from PduR to FrTp.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. FrTpRxSduRef

- **UUID**: `ECUC:4876e7cb-860a-4233-81db-4a2de8244c33`
- **引用名**: `FrTpRxSduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a PDU in the global PDU structure.

##### 5. FrTpTxSdu

**容器属性**:

- **UUID**: `ECUC:3d26dff5-3b62-4c38-8032-519b289f59bf`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FrTpTxSdu`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This parameter defines the Tx Service Data Unit Identifier (Sdu Id) which uniquely identifies a data transfer (inter-module communication) between FrTp and PDUR.

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. FrTpTxSduId

- **UUID**: `ECUC:486179ae-7b2e-4d16-8eb9-ffc5a767c23c`
- **参数名**: `FrTpTxSduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a unique identifier for a to be transmitted message from the PduR to the FrTp.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. FrTpTxSduRef

- **UUID**: `ECUC:53652bde-41b6-4054-9bf8-bec6d6f95359`
- **引用名**: `FrTpTxSduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a PDU in the global PDU structure.

##### 6. FrTpConnectionControl

**容器属性**:

- **UUID**: `ECUC:9ae16791-5e2f-424a-9867-babf691ec3ee`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FrTpConnectionControl`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

This container contains the configuration parameters to control a FlexRay TP connection.

###### 参数配置

此容器包含 **16** 个参数：

####### INTEGER 类型参数

######## 1. FrTpMaxAr

- **UUID**: `ECUC:f92ab95e-285b-447b-b59a-c96296678562`
- **参数名**: `FrTpMaxAr`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the maximum number of trying to send a frame when a TIMEOUT AR occurs.

######## 2. FrTpMaxAs

- **UUID**: `ECUC:f544ed50-692f-4eac-b06e-725f44195f93`
- **参数名**: `FrTpMaxAs`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the maximum number of trying to send a frame when a TIMEOUT AS occurs.

######## 3. FrTpMaxBufferSize

- **UUID**: `ECUC:7f017436-3c7f-46e9-8409-766990b33763`
- **参数名**: `FrTpMaxBufferSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Limits the maximal buffer size the FrTp can choose in order to limit the amount of Tx buffer that will be requested at the sender side in a segmented transfer.

######## 4. FrTpMaxFCWait

- **UUID**: `ECUC:eddb6d0e-550b-4ff2-9c0f-bdad7c7d5462`
- **参数名**: `FrTpMaxFCWait`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the maximum number of FlowControl N-PDUs with FlowState "WAIT"

######## 5. FrTpMaxFrIf

- **UUID**: `ECUC:668f68b3-42bf-40fa-a0b6-2076a2974f93`
- **参数名**: `FrTpMaxFrIf`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the maximum number of trying to send a frame when the FrIf returns an error.

######## 6. FrTpMaxNbrOfNPduPerCycle

- **UUID**: `ECUC:511499e2-c997-4664-b839-cd6fcc37e817`
- **参数名**: `FrTpMaxNbrOfNPduPerCycle`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..31]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter is part of the ISO 10681-2 protocol's FlowControl parameter "Bandwidth Control (BC)". It limits the number of N-Pdus the sender is allowed to transmit within a FlexRay cycle.

######## 7. FrTpMaxRn

- **UUID**: `ECUC:22705c63-9e4a-43a8-a155-2ea0d0e299be`
- **参数名**: `FrTpMaxRn`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the maximum number of retries (if retry is configured).

######## 8. FrTpSCexp

- **UUID**: `ECUC:39029fbb-3d5b-482c-ab05-041cd8751234`
- **参数名**: `FrTpSCexp`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..7]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter is part of the ISO 10681-2 protocol's FlowControl parameter "Bandwidth Control (BC)". It represents the exponent to calculate the minimum number of "Separation Cycles" the sender has to wait for the next transmission of an FrTp N-Pdu.

####### FLOAT 类型参数

######## 1. FrTpTimeBr

- **UUID**: `ECUC:e160a206-95b9-4917-8862-427d65dcc2a0`
- **参数名**: `FrTpTimeBr`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0..0.255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the time in seconds the FrTp requires to transmit a corresponding FlowControl Frame. According to ISO 10681-2 this parameter is a performance requirement.

######## 2. FrTpTimeBuffer

- **UUID**: `ECUC:7e2e5b1b-ae37-4a23-bf2f-32c4bf862e1c`
- **参数名**: `FrTpTimeBuffer`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0..65.535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the time in seconds of waiting for the next try to get a Tx or Rx buffer.

######## 3. FrTpTimeFrIf

- **UUID**: `ECUC:48fc4037-c3db-46b3-94ef-440242853af1`
- **参数名**: `FrTpTimeFrIf`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0..0.255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the time in seconds of waiting for the next try (if retry is activated) to send via FrIf_Transmit.

######## 4. FrTpTimeoutAr

- **UUID**: `ECUC:90038b23-567e-421d-a35c-f82da1d7f0da`
- **参数名**: `FrTpTimeoutAr`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0..65.535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter states the timeout in seconds between the PDU transmit request of the Transport Layer to the FlexRay Interface and the corresponding confirmation of the FlexRay Interface on the receiver side (for FC or AF).

######## 5. FrTpTimeoutAs

- **UUID**: `ECUC:a673b7e0-8b68-4be7-9447-8b9a19e4cfa0`
- **参数名**: `FrTpTimeoutAs`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0..65.535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter specifies the timeout in seconds the FrIf shall confirm a transmitted Pdu to the FrTp.

######## 6. FrTpTimeoutBs

- **UUID**: `ECUC:2ba00d4a-1079-4f0d-936a-5db48acd8cce`
- **参数名**: `FrTpTimeoutBs`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0..65.535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the timeout in seconds for waiting for an FC or AF on the sender side in a 1:1 connection.

######## 7. FrTpTimeoutCr

- **UUID**: `ECUC:2a9422c2-8b51-4ec5-9ab5-3f5a8e8dde97`
- **参数名**: `FrTpTimeoutCr`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0..65.535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the timeout value in seconds a receiver is waiting for a CF or a LF.

####### ENUMERATION 类型参数

######## 1. FrTpAckType

- **UUID**: `ECUC:45e13963-200d-45a5-96e5-3267c92c0ac0`
- **参数名**: `FrTpAckType`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `FRTP_ACK_WITH_RT` (来源: AUTOSAR_ECUC)
  - `FRTP_NO` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the type of acknowledgement which is used for the specific channel.

##### 7. FrTpRxPduPool

**容器属性**:

- **UUID**: `ECUC:78a80c22-51d9-4999-897d-a64c3be59fad`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FrTpRxPduPool`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

This container contains all Pdus that are assigned to that Pdu Pool.

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. FrTpRxPdu

**容器属性**:

- **UUID**: `ECUC:293a3123-98f2-43d0-a74b-3708e5688631`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FrTpRxPdu`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

Container to hold the PDU parameters.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. FrTpRxPduId

- **UUID**: `ECUC:2ed97a0f-0bee-481c-b44c-303a5f9b4c63`
- **参数名**: `FrTpRxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a unique identifier for a received message which is forwarded from the FrIf to the FrTp.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. FrTpRxPduRef

- **UUID**: `ECUC:57804f45-2cd4-47ec-b5ec-70bd2676da01`
- **引用名**: `FrTpRxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a PDU in the global PDU structure.

##### 8. FrTpRxPdu

**容器属性**:

- **UUID**: `ECUC:293a3123-98f2-43d0-a74b-3708e5688631`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FrTpRxPdu`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

Container to hold the PDU parameters.

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. FrTpRxPduId

- **UUID**: `ECUC:2ed97a0f-0bee-481c-b44c-303a5f9b4c63`
- **参数名**: `FrTpRxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a unique identifier for a received message which is forwarded from the FrIf to the FrTp.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. FrTpRxPduRef

- **UUID**: `ECUC:57804f45-2cd4-47ec-b5ec-70bd2676da01`
- **引用名**: `FrTpRxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a PDU in the global PDU structure.

##### 9. FrTpTxPduPool

**容器属性**:

- **UUID**: `ECUC:a2415a14-8390-4b76-b88b-32b28bef741d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FrTpTxPduPool`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

This container contains all Pdus that are assigned to that Pdu Pool.

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. FrTpTxPdu

**容器属性**:

- **UUID**: `ECUC:6c3c184f-27ba-4e88-a02e-b7da04d5d309`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FrTpTxPdu`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

Container to hold the PDU parameters.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. FrTpTxConfirmationPduId

- **UUID**: `ECUC:8324381f-3689-4616-8019-8b490ac93f8a`
- **参数名**: `FrTpTxConfirmationPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Handle Id to be used by the FrIf to confirm the transmission of the FrTpTxPdu to the FrIf module.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. FrTpTxPduRef

- **UUID**: `ECUC:29602a84-6c32-4014-8e25-d597b357b5ea`
- **引用名**: `FrTpTxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a PDU in the global PDU structure.

##### 10. FrTpTxPdu

**容器属性**:

- **UUID**: `ECUC:6c3c184f-27ba-4e88-a02e-b7da04d5d309`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FrTpTxPdu`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

Container to hold the PDU parameters.

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. FrTpTxConfirmationPduId

- **UUID**: `ECUC:8324381f-3689-4616-8019-8b490ac93f8a`
- **参数名**: `FrTpTxConfirmationPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Handle Id to be used by the FrIf to confirm the transmission of the FrTpTxPdu to the FrIf module.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. FrTpTxPduRef

- **UUID**: `ECUC:29602a84-6c32-4014-8e25-d597b357b5ea`
- **引用名**: `FrTpTxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a PDU in the global PDU structure.

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

1. **FrTp**
