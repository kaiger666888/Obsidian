# FrArTp - 完整配置文档

*此文档由ARXML文件自动生成，采用层次化结构展示*

**生成时间**: 2025-06-16 14:48:46

## 📑 目录

- [📄 文件信息](#-文件信息)
- [🔧 模块定义](#-模块定义)
  - [FrArTp](#frartp)
- [📦 包结构](#-包结构)

## 📄 文件信息

### Schema信息
- **Schema位置**: `http://autosar.org/schema/r4.0 AUTOSAR_4-0-3.xsd`
- **命名空间**: `http://autosar.org/schema/r4.0`

## 🔧 模块定义

### 1. FrArTp

#### 基本信息

- **UUID**: `ECUC:bfffe61a-1bd7-4b8d-85f7-cee6931cb543`
- **模块名称**: `FrArTp`
- **多重性**: [0..1]
- **支持的变体**:
  - VARIANT-POST-BUILD
  - VARIANT-PRE-COMPILE

#### 模块描述

Configuration of the FrArTp (FlexRay Transport Protocol) module.

#### 版本历史

共有 **1** 个版本记录：

##### 1. 版本 4.2.0

- **发布日期**: 2011-11-09
- **发布者**: AUTOSAR

*此版本无详细变更记录*

#### 配置容器

本模块包含 **8** 个配置容器：

##### 1. FrArTpGeneral

**容器属性**:

- **UUID**: `ECUC:d5bcaff4-567a-4272-8758-7faeee4ae05c`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FrArTpGeneral`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

This container contains the general configuration (parameters) of the FlexRay TP.

###### 参数配置

此容器包含 **8** 个参数：

####### INTEGER 类型参数

######## 1. FrArTpChanNum

- **UUID**: `ECUC:40bcdb28-9d86-4cae-841d-e213b2409b10`
- **参数名**: `FrArTpChanNum`
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

######## 1. FrArTpDevErrorDetect

- **UUID**: `ECUC:8cbe5489-2294-4b35-826c-7e20a3b269e2`
- **参数名**: `FrArTpDevErrorDetect`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Preprocessor switch for enabling development error detection.

######## 2. FrArTpHaveAckRt

- **UUID**: `ECUC:2941d541-7731-416a-a4cb-f758b008bf2e`
- **参数名**: `FrArTpHaveAckRt`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Preprocessor switch for enabling the Acknowledgement and retry mechanisms.

######## 3. FrArTpHaveGrpSeg

- **UUID**: `ECUC:db0c21bb-0d51-42d3-ba97-44552e586054`
- **参数名**: `FrArTpHaveGrpSeg`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Preprocessor switch for enabling segmentation of 1:n messages.

######## 4. FrArTpHaveLm

- **UUID**: `ECUC:f7de932d-8d25-4503-a3ca-e1dba3c182ec`
- **参数名**: `FrArTpHaveLm`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Preprocessor switch for enabling the mechanism for message longer than allowed by.

######## 5. FrArTpHaveTc

- **UUID**: `ECUC:b65f5bc0-3252-486e-a5e8-caef4d3a0c53`
- **参数名**: `FrArTpHaveTc`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Preprocessor switch for enabling Transmit Cancellation.

######## 6. FrArTpVersionInfoApi

- **UUID**: `ECUC:079edbf3-4881-462e-8f1c-89d43738bc62`
- **参数名**: `FrArTpVersionInfoApi`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Preprocessor switch for enabling the Version info API.

####### FLOAT 类型参数

######## 1. FrArTpMainFuncCycle

- **UUID**: `ECUC:d93c4677-c68f-4b7a-af41-002d09edecf8`
- **参数名**: `FrArTpMainFuncCycle`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0..1.024]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter contains the calling period of the TPs Main Function. The parameter is specified in seconds.

##### 2. FrArTpMultipleConfig

**容器属性**:

- **UUID**: `ECUC:97993d4a-7769-4798-aa92-461976ddbef6`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FrArTpMultipleConfig`
- **多重性**: [1..1]
- **多配置容器**: true

**容器描述**:

This container holds one or several multiple configuration sets.

###### 配置容器

本模块包含 **6** 个配置容器：

####### 1. FrArTpChannel

**容器属性**:

- **UUID**: `ECUC:676806cc-fb0f-496e-a505-11dc3ce82ef6`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FrArTpChannel`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

This container contains the configuration (parameters) of one FlexRay TP channel.

######## 参数配置

此容器包含 **23** 个参数：

######### INTEGER 类型参数

########## 1. FrArTpChannelId

- **UUID**: `ECUC:090a8bf9-9bad-45e0-b252-b8911dc92662`
- **参数名**: `FrArTpChannelId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The Id of the channel.

########## 2. FrArTpConNum

- **UUID**: `ECUC:07ed9e2f-0ff4-4c4b-908f-f33321ad2012`
- **参数名**: `FrArTpConNum`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65536]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter states the number of connections used in this channel. At least 256 shall be configurable here.

########## 3. FrArTpMaxAr

- **UUID**: `ECUC:4d538907-b70d-4699-8f56-8e7234286355`
- **参数名**: `FrArTpMaxAr`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the maximum number of trying to send a frame when a TIMEOUT AR occurs (depending on whether retry is configured).

########## 4. FrArTpMaxAs

- **UUID**: `ECUC:4d7d6aaf-92b2-4001-ab30-fe6040a6acb6`
- **参数名**: `FrArTpMaxAs`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the maximum number of trying t osend a frame when a TIMEOUT AS occurs (depending on whether retry is configured)

########## 5. FrArTpMaxBs

- **UUID**: `ECUC:9505fed5-9588-4c03-8b0b-a1627d38b537`
- **参数名**: `FrArTpMaxBs`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines number of consecutive CFs between two FCs (block size). Valid values are 1 .. 16 when retry is activated, and 0 .. 255 otherwise.

########## 6. FrArTpMaxBufReq

- **UUID**: `ECUC:1e0599d8-a1e1-4bb8-aff9-df553fecf023`
- **参数名**: `FrArTpMaxBufReq`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the maximum number of times the FrArTp should send a wait frame FC(WT). It is also used to limit the number of retries for PduR_FrArTpCopyTxData and PduR_FrArTpCopyRxData when no timer is active.

########## 7. FrArTpMaxFrIf

- **UUID**: `ECUC:9bb25c92-1691-4d6c-9f8b-0e4bd1a75ebd`
- **参数名**: `FrArTpMaxFrIf`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the maximum number of trying to send a frame when the FrIf returns an error.

########## 8. FrArTpMaxRn

- **UUID**: `ECUC:89d01884-23a7-478e-b641-52e479415a03`
- **参数名**: `FrArTpMaxRn`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the maximum number of retries (if retry is configured for the particular channel).

######### BOOLEAN 类型参数

########## 1. FrArTpGrpSeg

- **UUID**: `ECUC:fd40e0b6-4a5b-4123-b2f2-5d36a18499f6`
- **参数名**: `FrArTpGrpSeg`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Here can be specified, whether segmentation within a 1:n connection is allowed or not.

########## 2. FrArTpTc

- **UUID**: `ECUC:7fe1452b-6e76-47fd-822b-84d512e89568`
- **参数名**: `FrArTpTc`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: With this switch Transmit Cancellation can be turned on or off for this channel.

########## 3. FrArTpUsePduFc

- **UUID**: `ECUC:ccffe2ef-7493-4e36-bf0b-ba3f7b4f477a`
- **参数名**: `FrArTpUsePduFc`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This switch defines, whether within this channel the dedicated FC/ACK PDU (FrArTpPduFc) shall be used or not. If this is not used FC / ACK frames are sent using the normal IDs, otherwise only FrArTpPduFc shall be used for sending / receiving FC / ACK frames.

######### FLOAT 类型参数

########## 1. FrArTpStMin

- **UUID**: `ECUC:c593f78b-411f-44c5-bdfc-6cd25077dadb`
- **参数名**: `FrArTpStMin`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the minimum amount of time between two succeeding CFs in seconds. Valid values are 0, 100µs, 200µs .. 900µs, 1ms, 2ms .. 127ms. The value can be changed at runtime using the FrArTp_ChangeParameter interface.

########## 2. FrArTpTimeBr

- **UUID**: `ECUC:525037db-2b41-44ec-a323-83e5bb925586`
- **参数名**: `FrArTpTimeBr`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0..65.535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the time in seconds between receiving the last CF of a block or an FF-x (or SF-x) and sending out an FC or AF.

########## 3. FrArTpTimeBuffer

- **UUID**: `ECUC:7889f943-d2cc-462b-b164-f1f867da7b8a`
- **参数名**: `FrArTpTimeBuffer`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0..0.255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the time in seconds of waiting for the next try (if retry is activated) to get a Tx or Rx buffer.

########## 4. FrArTpTimeCs

- **UUID**: `ECUC:52be0e3c-0912-4b1d-80a8-144d2ed34efe`
- **参数名**: `FrArTpTimeCs`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0..65.535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the time in seconds between the sending of two consecutive CFs or  between reception of an FC or AF and sending of the next CF . It is obvious that FRARTP_TIME_CS + FRARTP_TIMEOUT_AS < FRARTP_TIMEOUT_CR must hold (because the transmission duration on the bus has also to be considered). This parameter is defined in ISO 15765-2. It is contained in the configuration as a performance requirement.

########## 5. FrArTpTimeFrIf

- **UUID**: `ECUC:17146ae9-0653-453d-89de-5cd0596ca668`
- **参数名**: `FrArTpTimeFrIf`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0..0.255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the time in seconds of waiting for the next try (if retry is activated) to send via FrIf_Transmit.

########## 6. FrArTpTimeoutAr

- **UUID**: `ECUC:af2272f8-9b82-465a-b640-fefd7582dc0c`
- **参数名**: `FrArTpTimeoutAr`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0..65.535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter states the timeout in seconds between the PDU transmit request of the Transport Layer to the FlexRay Interface and the corresponding confirmation of the FlexRay Interface on the receiver side (for FC or AF).

########## 7. FrArTpTimeoutAs

- **UUID**: `ECUC:d5e8acba-4da6-4ec2-b73c-b11684d92d53`
- **参数名**: `FrArTpTimeoutAs`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0..65.535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter states the timeout in seconds between the PDU transmit request for the first PDU of the group used in the current connection of the Transport Layer to the FlexRay Interface and the corresponding confirmation of the FlexRay Interface (when having sent the last PDU of the

########## 8. FrArTpTimeoutBs

- **UUID**: `ECUC:21b6f6ba-d00f-4ae3-a59c-6abdc1e49bd5`
- **参数名**: `FrArTpTimeoutBs`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0..65.535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the timeout in seconds for waiting for an FC or AF on the sender side in a 1:1 connection.

########## 9. FrArTpTimeoutCr

- **UUID**: `ECUC:76f8dcee-0a17-4eeb-bd8d-c1c719af4a06`
- **参数名**: `FrArTpTimeoutCr`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0..65.535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the timeout value in seconds for waiting for a CF or FF-x (in case of retry) after receiving the last CF or after sending an FC or AF on the receiver side.

######### ENUMERATION 类型参数

########## 1. FrArTpAckType

- **UUID**: `ECUC:7ac80ba2-db0b-4a4c-8ccf-c058e66b5540`
- **参数名**: `FrArTpAckType`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `FRARTP_ACK_WITHOUT_RT` (来源: AUTOSAR_ECUC)
  - `FRARTP_ACK_WITH_RT` (来源: AUTOSAR_ECUC)
  - `FRARTP_NO` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the type of acknowledgement which is used for the specific channel.

########## 2. FrArTpAdrType

- **UUID**: `ECUC:fbf212e1-3eb4-408a-a2e7-952ba8bff386`
- **参数名**: `FrArTpAdrType`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `FRARTP_OB` (来源: AUTOSAR_ECUC)
  - `FRARTP_TB` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter states the addressing type this connection has. The meanings of the values are one byte and two byte.

########## 3. FrArTpLm

- **UUID**: `ECUC:00c0ff2e-ea55-401b-add2-16b714ae2ea7`
- **参数名**: `FrArTpLm`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `FRARTP_ISO` (来源: AUTOSAR_ECUC)
  - `FRARTP_ISO6` (来源: AUTOSAR_ECUC)
  - `FRARTP_L4G` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This specifies the maximum message length for the particular channel.

######## 配置容器

本模块包含 **5** 个配置容器：

######### 1. FrArTpConnection

**容器属性**:

- **UUID**: `ECUC:13a80df6-16e8-4e9b-940b-bbb23b65795a`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FrArTpConnection`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

This container contains the configuration (parameters) of one FlexRay TP connection.

########## 参数配置

此容器包含 **3** 个参数：

########### INTEGER 类型参数

############ 1. FrArTpLa

- **UUID**: `ECUC:e954e143-e9a7-4b6c-852d-8f18e1ca4dda`
- **参数名**: `FrArTpLa`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the Local Address for the respective connection.

############ 2. FrArTpRa

- **UUID**: `ECUC:d61dfa47-2482-40bc-8d65-015f5a973016`
- **参数名**: `FrArTpRa`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the Remote Address for the respective connection.

########### BOOLEAN 类型参数

############ 1. FrArTpMultRec

- **UUID**: `ECUC:16ce2a19-fe14-4138-bccc-d9d65af5b845`
- **参数名**: `FrArTpMultRec`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines, whether this connection is an 1:1 ('false') or an 1:n ('true') connection.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. FrArTpConPduRef

- **UUID**: `ECUC:b67573de-7cb1-4e98-a362-8c7ed26e3e4a`
- **引用名**: `FrArTpConPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..infinite]
- **目标**: `FrArTpPdu`
- **完整路径**: `/AUTOSAR/EcucDefs/FrArTp/FrArTpMultipleConfig/FrArTpChannel/FrArTpPdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Each value defines a PDU to be used for this connection. Thus each value is a PDU-ID given in FrArTpPdu and this array cannot be longer than the array FrArTpPdu.

########## 配置容器

本模块包含 **2** 个配置容器：

########### 1. FrArTpRxSdu

**容器属性**:

- **UUID**: `ECUC:d8731acc-40fe-4633-853b-297b53ec6b1d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FrArTpRxSdu`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Describes the Rx SDU

############ 参数配置

此容器包含 **1** 个参数：

############# INTEGER 类型参数

############## 1. FrArTpSduRxId

- **UUID**: `ECUC:11449a7a-0e5f-4585-806f-e7b9943538f9`
- **参数名**: `FrArTpSduRxId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65536]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a unique identifier for a received message. This Id is used in the CancelReceive API call.

############ 引用关系

此容器包含 **1** 个引用：

############# REFERENCE 类型引用

############## 1. FrArTpRxSduRef

- **UUID**: `ECUC:2fe49c20-df8f-4155-81c1-2a0028c467cd`
- **引用名**: `FrArTpRxSduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a PDU in the global PDU structure.

########### 2. FrArTpTxSdu

**容器属性**:

- **UUID**: `ECUC:dfda3c7c-8f9c-4b60-9906-c46a84e4e450`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FrArTpTxSdu`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Describes the Tx SDU

############ 参数配置

此容器包含 **1** 个参数：

############# INTEGER 类型参数

############## 1. FrArTpSduTxId

- **UUID**: `ECUC:53e537ea-84a2-43cd-a160-3507af15d05c`
- **参数名**: `FrArTpSduTxId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65536]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a unique identifier for a received or a to be transmitted message. With this (and by means of e.g. a lookup table) the PDU Router can route the message appropriately without dealing with the particularities of the Transport Layer. This parameter can also be seen as the identifier of a connection.

############ 引用关系

此容器包含 **1** 个引用：

############# REFERENCE 类型引用

############## 1. FrArTpTxSduRef

- **UUID**: `ECUC:84f2bd32-9b3a-4b4f-8625-4c5869465f63`
- **引用名**: `FrArTpTxSduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a PDU in the global PDU structure.

######### 2. FrArTpRxSdu

**容器属性**:

- **UUID**: `ECUC:d8731acc-40fe-4633-853b-297b53ec6b1d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FrArTpRxSdu`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Describes the Rx SDU

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. FrArTpSduRxId

- **UUID**: `ECUC:11449a7a-0e5f-4585-806f-e7b9943538f9`
- **参数名**: `FrArTpSduRxId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65536]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a unique identifier for a received message. This Id is used in the CancelReceive API call.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. FrArTpRxSduRef

- **UUID**: `ECUC:2fe49c20-df8f-4155-81c1-2a0028c467cd`
- **引用名**: `FrArTpRxSduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a PDU in the global PDU structure.

######### 3. FrArTpTxSdu

**容器属性**:

- **UUID**: `ECUC:dfda3c7c-8f9c-4b60-9906-c46a84e4e450`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FrArTpTxSdu`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Describes the Tx SDU

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. FrArTpSduTxId

- **UUID**: `ECUC:53e537ea-84a2-43cd-a160-3507af15d05c`
- **参数名**: `FrArTpSduTxId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65536]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a unique identifier for a received or a to be transmitted message. With this (and by means of e.g. a lookup table) the PDU Router can route the message appropriately without dealing with the particularities of the Transport Layer. This parameter can also be seen as the identifier of a connection.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. FrArTpTxSduRef

- **UUID**: `ECUC:84f2bd32-9b3a-4b4f-8625-4c5869465f63`
- **引用名**: `FrArTpTxSduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a PDU in the global PDU structure.

######### 4. FrArTpPdu

**容器属性**:

- **UUID**: `ECUC:41f834ea-0a7e-41f1-922b-6ec9fdfca831`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FrArTpPdu`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

Container to hold the PDU parameters.

########## 参数配置

此容器包含 **2** 个参数：

########### INTEGER 类型参数

############ 1. FrArTpPduId

- **UUID**: `ECUC:32c3e70e-66b0-4889-9164-c9b77fd3817f`
- **参数名**: `FrArTpPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65536]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is the identifier of the FlexRay Interface PDUs (Fr N-PDU, Fr L-SDU) in which the Transport Layer Frames of this channel should be transmitted.

########### ENUMERATION 类型参数

############ 1. FrArTpPduDirection

- **UUID**: `ECUC:65ff9cc6-6ff0-4283-91b9-2ef072d144e7`
- **参数名**: `FrArTpPduDirection`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `FRARTP_RX` (来源: AUTOSAR_ECUC)
  - `FRARTP_TX` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the direction of the PDU.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. FrArTpPduRef

- **UUID**: `ECUC:121b4008-ac40-47de-87e5-8aa17f5cccb9`
- **引用名**: `FrArTpPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE

######### 5. FrArTpPduFc

**容器属性**:

- **UUID**: `ECUC:280361eb-2b84-4b66-8694-19e08cc6b8a9`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FrArTpPduFc`
- **多重性**: [0..2]
- **多配置容器**: false

**容器描述**:

This is the identifier of the FlexRay Interface PDUs (Fr N-PDU, Fr L-SDU) in which the Transport Layer Flow Control and Acknowledgement Frames of this channel should be transmitted.

########## 参数配置

此容器包含 **2** 个参数：

########### INTEGER 类型参数

############ 1. FrArTpPduFcId

- **UUID**: `ECUC:c4dd8b01-2977-49fc-8153-c25bb9016a94`
- **参数名**: `FrArTpPduFcId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65536]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is the identifier of the FlexRay Interface PDUs (Fr N-PDU, Fr L-SDU) in which the Transport Layer Flow Control and Acknowledgement Frames of this channel should be transmitted.

########### ENUMERATION 类型参数

############ 1. FrArTpPduFcDirection

- **UUID**: `ECUC:34ddae7a-6ebc-4a17-b16a-ed1d1aa507c5`
- **参数名**: `FrArTpPduFcDirection`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `FRARTP_FC_RX` (来源: AUTOSAR_ECUC)
  - `FRARTP_FC_TX` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the direction of the PDU.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. FrArTpPduFcRef

- **UUID**: `ECUC:67298ee3-3c75-4497-b365-075f234aea20`
- **引用名**: `FrArTpPduFcRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE

####### 2. FrArTpConnection

**容器属性**:

- **UUID**: `ECUC:13a80df6-16e8-4e9b-940b-bbb23b65795a`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FrArTpConnection`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

This container contains the configuration (parameters) of one FlexRay TP connection.

######## 参数配置

此容器包含 **3** 个参数：

######### INTEGER 类型参数

########## 1. FrArTpLa

- **UUID**: `ECUC:e954e143-e9a7-4b6c-852d-8f18e1ca4dda`
- **参数名**: `FrArTpLa`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the Local Address for the respective connection.

########## 2. FrArTpRa

- **UUID**: `ECUC:d61dfa47-2482-40bc-8d65-015f5a973016`
- **参数名**: `FrArTpRa`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the Remote Address for the respective connection.

######### BOOLEAN 类型参数

########## 1. FrArTpMultRec

- **UUID**: `ECUC:16ce2a19-fe14-4138-bccc-d9d65af5b845`
- **参数名**: `FrArTpMultRec`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines, whether this connection is an 1:1 ('false') or an 1:n ('true') connection.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. FrArTpConPduRef

- **UUID**: `ECUC:b67573de-7cb1-4e98-a362-8c7ed26e3e4a`
- **引用名**: `FrArTpConPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..infinite]
- **目标**: `FrArTpPdu`
- **完整路径**: `/AUTOSAR/EcucDefs/FrArTp/FrArTpMultipleConfig/FrArTpChannel/FrArTpPdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Each value defines a PDU to be used for this connection. Thus each value is a PDU-ID given in FrArTpPdu and this array cannot be longer than the array FrArTpPdu.

######## 配置容器

本模块包含 **2** 个配置容器：

######### 1. FrArTpRxSdu

**容器属性**:

- **UUID**: `ECUC:d8731acc-40fe-4633-853b-297b53ec6b1d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FrArTpRxSdu`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Describes the Rx SDU

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. FrArTpSduRxId

- **UUID**: `ECUC:11449a7a-0e5f-4585-806f-e7b9943538f9`
- **参数名**: `FrArTpSduRxId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65536]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a unique identifier for a received message. This Id is used in the CancelReceive API call.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. FrArTpRxSduRef

- **UUID**: `ECUC:2fe49c20-df8f-4155-81c1-2a0028c467cd`
- **引用名**: `FrArTpRxSduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a PDU in the global PDU structure.

######### 2. FrArTpTxSdu

**容器属性**:

- **UUID**: `ECUC:dfda3c7c-8f9c-4b60-9906-c46a84e4e450`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FrArTpTxSdu`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Describes the Tx SDU

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. FrArTpSduTxId

- **UUID**: `ECUC:53e537ea-84a2-43cd-a160-3507af15d05c`
- **参数名**: `FrArTpSduTxId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65536]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a unique identifier for a received or a to be transmitted message. With this (and by means of e.g. a lookup table) the PDU Router can route the message appropriately without dealing with the particularities of the Transport Layer. This parameter can also be seen as the identifier of a connection.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. FrArTpTxSduRef

- **UUID**: `ECUC:84f2bd32-9b3a-4b4f-8625-4c5869465f63`
- **引用名**: `FrArTpTxSduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a PDU in the global PDU structure.

####### 3. FrArTpRxSdu

**容器属性**:

- **UUID**: `ECUC:d8731acc-40fe-4633-853b-297b53ec6b1d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FrArTpRxSdu`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Describes the Rx SDU

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. FrArTpSduRxId

- **UUID**: `ECUC:11449a7a-0e5f-4585-806f-e7b9943538f9`
- **参数名**: `FrArTpSduRxId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65536]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a unique identifier for a received message. This Id is used in the CancelReceive API call.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. FrArTpRxSduRef

- **UUID**: `ECUC:2fe49c20-df8f-4155-81c1-2a0028c467cd`
- **引用名**: `FrArTpRxSduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a PDU in the global PDU structure.

####### 4. FrArTpTxSdu

**容器属性**:

- **UUID**: `ECUC:dfda3c7c-8f9c-4b60-9906-c46a84e4e450`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FrArTpTxSdu`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Describes the Tx SDU

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. FrArTpSduTxId

- **UUID**: `ECUC:53e537ea-84a2-43cd-a160-3507af15d05c`
- **参数名**: `FrArTpSduTxId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65536]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a unique identifier for a received or a to be transmitted message. With this (and by means of e.g. a lookup table) the PDU Router can route the message appropriately without dealing with the particularities of the Transport Layer. This parameter can also be seen as the identifier of a connection.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. FrArTpTxSduRef

- **UUID**: `ECUC:84f2bd32-9b3a-4b4f-8625-4c5869465f63`
- **引用名**: `FrArTpTxSduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a PDU in the global PDU structure.

####### 5. FrArTpPdu

**容器属性**:

- **UUID**: `ECUC:41f834ea-0a7e-41f1-922b-6ec9fdfca831`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FrArTpPdu`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

Container to hold the PDU parameters.

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. FrArTpPduId

- **UUID**: `ECUC:32c3e70e-66b0-4889-9164-c9b77fd3817f`
- **参数名**: `FrArTpPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65536]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is the identifier of the FlexRay Interface PDUs (Fr N-PDU, Fr L-SDU) in which the Transport Layer Frames of this channel should be transmitted.

######### ENUMERATION 类型参数

########## 1. FrArTpPduDirection

- **UUID**: `ECUC:65ff9cc6-6ff0-4283-91b9-2ef072d144e7`
- **参数名**: `FrArTpPduDirection`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `FRARTP_RX` (来源: AUTOSAR_ECUC)
  - `FRARTP_TX` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the direction of the PDU.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. FrArTpPduRef

- **UUID**: `ECUC:121b4008-ac40-47de-87e5-8aa17f5cccb9`
- **引用名**: `FrArTpPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE

####### 6. FrArTpPduFc

**容器属性**:

- **UUID**: `ECUC:280361eb-2b84-4b66-8694-19e08cc6b8a9`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FrArTpPduFc`
- **多重性**: [0..2]
- **多配置容器**: false

**容器描述**:

This is the identifier of the FlexRay Interface PDUs (Fr N-PDU, Fr L-SDU) in which the Transport Layer Flow Control and Acknowledgement Frames of this channel should be transmitted.

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. FrArTpPduFcId

- **UUID**: `ECUC:c4dd8b01-2977-49fc-8153-c25bb9016a94`
- **参数名**: `FrArTpPduFcId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65536]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is the identifier of the FlexRay Interface PDUs (Fr N-PDU, Fr L-SDU) in which the Transport Layer Flow Control and Acknowledgement Frames of this channel should be transmitted.

######### ENUMERATION 类型参数

########## 1. FrArTpPduFcDirection

- **UUID**: `ECUC:34ddae7a-6ebc-4a17-b16a-ed1d1aa507c5`
- **参数名**: `FrArTpPduFcDirection`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `FRARTP_FC_RX` (来源: AUTOSAR_ECUC)
  - `FRARTP_FC_TX` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the direction of the PDU.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. FrArTpPduFcRef

- **UUID**: `ECUC:67298ee3-3c75-4497-b365-075f234aea20`
- **引用名**: `FrArTpPduFcRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE

##### 3. FrArTpChannel

**容器属性**:

- **UUID**: `ECUC:676806cc-fb0f-496e-a505-11dc3ce82ef6`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FrArTpChannel`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

This container contains the configuration (parameters) of one FlexRay TP channel.

###### 参数配置

此容器包含 **23** 个参数：

####### INTEGER 类型参数

######## 1. FrArTpChannelId

- **UUID**: `ECUC:090a8bf9-9bad-45e0-b252-b8911dc92662`
- **参数名**: `FrArTpChannelId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The Id of the channel.

######## 2. FrArTpConNum

- **UUID**: `ECUC:07ed9e2f-0ff4-4c4b-908f-f33321ad2012`
- **参数名**: `FrArTpConNum`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65536]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter states the number of connections used in this channel. At least 256 shall be configurable here.

######## 3. FrArTpMaxAr

- **UUID**: `ECUC:4d538907-b70d-4699-8f56-8e7234286355`
- **参数名**: `FrArTpMaxAr`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the maximum number of trying to send a frame when a TIMEOUT AR occurs (depending on whether retry is configured).

######## 4. FrArTpMaxAs

- **UUID**: `ECUC:4d7d6aaf-92b2-4001-ab30-fe6040a6acb6`
- **参数名**: `FrArTpMaxAs`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the maximum number of trying t osend a frame when a TIMEOUT AS occurs (depending on whether retry is configured)

######## 5. FrArTpMaxBs

- **UUID**: `ECUC:9505fed5-9588-4c03-8b0b-a1627d38b537`
- **参数名**: `FrArTpMaxBs`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines number of consecutive CFs between two FCs (block size). Valid values are 1 .. 16 when retry is activated, and 0 .. 255 otherwise.

######## 6. FrArTpMaxBufReq

- **UUID**: `ECUC:1e0599d8-a1e1-4bb8-aff9-df553fecf023`
- **参数名**: `FrArTpMaxBufReq`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the maximum number of times the FrArTp should send a wait frame FC(WT). It is also used to limit the number of retries for PduR_FrArTpCopyTxData and PduR_FrArTpCopyRxData when no timer is active.

######## 7. FrArTpMaxFrIf

- **UUID**: `ECUC:9bb25c92-1691-4d6c-9f8b-0e4bd1a75ebd`
- **参数名**: `FrArTpMaxFrIf`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the maximum number of trying to send a frame when the FrIf returns an error.

######## 8. FrArTpMaxRn

- **UUID**: `ECUC:89d01884-23a7-478e-b641-52e479415a03`
- **参数名**: `FrArTpMaxRn`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the maximum number of retries (if retry is configured for the particular channel).

####### BOOLEAN 类型参数

######## 1. FrArTpGrpSeg

- **UUID**: `ECUC:fd40e0b6-4a5b-4123-b2f2-5d36a18499f6`
- **参数名**: `FrArTpGrpSeg`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Here can be specified, whether segmentation within a 1:n connection is allowed or not.

######## 2. FrArTpTc

- **UUID**: `ECUC:7fe1452b-6e76-47fd-822b-84d512e89568`
- **参数名**: `FrArTpTc`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: With this switch Transmit Cancellation can be turned on or off for this channel.

######## 3. FrArTpUsePduFc

- **UUID**: `ECUC:ccffe2ef-7493-4e36-bf0b-ba3f7b4f477a`
- **参数名**: `FrArTpUsePduFc`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This switch defines, whether within this channel the dedicated FC/ACK PDU (FrArTpPduFc) shall be used or not. If this is not used FC / ACK frames are sent using the normal IDs, otherwise only FrArTpPduFc shall be used for sending / receiving FC / ACK frames.

####### FLOAT 类型参数

######## 1. FrArTpStMin

- **UUID**: `ECUC:c593f78b-411f-44c5-bdfc-6cd25077dadb`
- **参数名**: `FrArTpStMin`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the minimum amount of time between two succeeding CFs in seconds. Valid values are 0, 100µs, 200µs .. 900µs, 1ms, 2ms .. 127ms. The value can be changed at runtime using the FrArTp_ChangeParameter interface.

######## 2. FrArTpTimeBr

- **UUID**: `ECUC:525037db-2b41-44ec-a323-83e5bb925586`
- **参数名**: `FrArTpTimeBr`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0..65.535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the time in seconds between receiving the last CF of a block or an FF-x (or SF-x) and sending out an FC or AF.

######## 3. FrArTpTimeBuffer

- **UUID**: `ECUC:7889f943-d2cc-462b-b164-f1f867da7b8a`
- **参数名**: `FrArTpTimeBuffer`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0..0.255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the time in seconds of waiting for the next try (if retry is activated) to get a Tx or Rx buffer.

######## 4. FrArTpTimeCs

- **UUID**: `ECUC:52be0e3c-0912-4b1d-80a8-144d2ed34efe`
- **参数名**: `FrArTpTimeCs`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0..65.535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the time in seconds between the sending of two consecutive CFs or  between reception of an FC or AF and sending of the next CF . It is obvious that FRARTP_TIME_CS + FRARTP_TIMEOUT_AS < FRARTP_TIMEOUT_CR must hold (because the transmission duration on the bus has also to be considered). This parameter is defined in ISO 15765-2. It is contained in the configuration as a performance requirement.

######## 5. FrArTpTimeFrIf

- **UUID**: `ECUC:17146ae9-0653-453d-89de-5cd0596ca668`
- **参数名**: `FrArTpTimeFrIf`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0..0.255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the time in seconds of waiting for the next try (if retry is activated) to send via FrIf_Transmit.

######## 6. FrArTpTimeoutAr

- **UUID**: `ECUC:af2272f8-9b82-465a-b640-fefd7582dc0c`
- **参数名**: `FrArTpTimeoutAr`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0..65.535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter states the timeout in seconds between the PDU transmit request of the Transport Layer to the FlexRay Interface and the corresponding confirmation of the FlexRay Interface on the receiver side (for FC or AF).

######## 7. FrArTpTimeoutAs

- **UUID**: `ECUC:d5e8acba-4da6-4ec2-b73c-b11684d92d53`
- **参数名**: `FrArTpTimeoutAs`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0..65.535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter states the timeout in seconds between the PDU transmit request for the first PDU of the group used in the current connection of the Transport Layer to the FlexRay Interface and the corresponding confirmation of the FlexRay Interface (when having sent the last PDU of the

######## 8. FrArTpTimeoutBs

- **UUID**: `ECUC:21b6f6ba-d00f-4ae3-a59c-6abdc1e49bd5`
- **参数名**: `FrArTpTimeoutBs`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0..65.535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the timeout in seconds for waiting for an FC or AF on the sender side in a 1:1 connection.

######## 9. FrArTpTimeoutCr

- **UUID**: `ECUC:76f8dcee-0a17-4eeb-bd8d-c1c719af4a06`
- **参数名**: `FrArTpTimeoutCr`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0..65.535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the timeout value in seconds for waiting for a CF or FF-x (in case of retry) after receiving the last CF or after sending an FC or AF on the receiver side.

####### ENUMERATION 类型参数

######## 1. FrArTpAckType

- **UUID**: `ECUC:7ac80ba2-db0b-4a4c-8ccf-c058e66b5540`
- **参数名**: `FrArTpAckType`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `FRARTP_ACK_WITHOUT_RT` (来源: AUTOSAR_ECUC)
  - `FRARTP_ACK_WITH_RT` (来源: AUTOSAR_ECUC)
  - `FRARTP_NO` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the type of acknowledgement which is used for the specific channel.

######## 2. FrArTpAdrType

- **UUID**: `ECUC:fbf212e1-3eb4-408a-a2e7-952ba8bff386`
- **参数名**: `FrArTpAdrType`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `FRARTP_OB` (来源: AUTOSAR_ECUC)
  - `FRARTP_TB` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter states the addressing type this connection has. The meanings of the values are one byte and two byte.

######## 3. FrArTpLm

- **UUID**: `ECUC:00c0ff2e-ea55-401b-add2-16b714ae2ea7`
- **参数名**: `FrArTpLm`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `FRARTP_ISO` (来源: AUTOSAR_ECUC)
  - `FRARTP_ISO6` (来源: AUTOSAR_ECUC)
  - `FRARTP_L4G` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This specifies the maximum message length for the particular channel.

###### 配置容器

本模块包含 **5** 个配置容器：

####### 1. FrArTpConnection

**容器属性**:

- **UUID**: `ECUC:13a80df6-16e8-4e9b-940b-bbb23b65795a`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FrArTpConnection`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

This container contains the configuration (parameters) of one FlexRay TP connection.

######## 参数配置

此容器包含 **3** 个参数：

######### INTEGER 类型参数

########## 1. FrArTpLa

- **UUID**: `ECUC:e954e143-e9a7-4b6c-852d-8f18e1ca4dda`
- **参数名**: `FrArTpLa`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the Local Address for the respective connection.

########## 2. FrArTpRa

- **UUID**: `ECUC:d61dfa47-2482-40bc-8d65-015f5a973016`
- **参数名**: `FrArTpRa`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the Remote Address for the respective connection.

######### BOOLEAN 类型参数

########## 1. FrArTpMultRec

- **UUID**: `ECUC:16ce2a19-fe14-4138-bccc-d9d65af5b845`
- **参数名**: `FrArTpMultRec`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines, whether this connection is an 1:1 ('false') or an 1:n ('true') connection.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. FrArTpConPduRef

- **UUID**: `ECUC:b67573de-7cb1-4e98-a362-8c7ed26e3e4a`
- **引用名**: `FrArTpConPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..infinite]
- **目标**: `FrArTpPdu`
- **完整路径**: `/AUTOSAR/EcucDefs/FrArTp/FrArTpMultipleConfig/FrArTpChannel/FrArTpPdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Each value defines a PDU to be used for this connection. Thus each value is a PDU-ID given in FrArTpPdu and this array cannot be longer than the array FrArTpPdu.

######## 配置容器

本模块包含 **2** 个配置容器：

######### 1. FrArTpRxSdu

**容器属性**:

- **UUID**: `ECUC:d8731acc-40fe-4633-853b-297b53ec6b1d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FrArTpRxSdu`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Describes the Rx SDU

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. FrArTpSduRxId

- **UUID**: `ECUC:11449a7a-0e5f-4585-806f-e7b9943538f9`
- **参数名**: `FrArTpSduRxId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65536]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a unique identifier for a received message. This Id is used in the CancelReceive API call.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. FrArTpRxSduRef

- **UUID**: `ECUC:2fe49c20-df8f-4155-81c1-2a0028c467cd`
- **引用名**: `FrArTpRxSduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a PDU in the global PDU structure.

######### 2. FrArTpTxSdu

**容器属性**:

- **UUID**: `ECUC:dfda3c7c-8f9c-4b60-9906-c46a84e4e450`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FrArTpTxSdu`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Describes the Tx SDU

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. FrArTpSduTxId

- **UUID**: `ECUC:53e537ea-84a2-43cd-a160-3507af15d05c`
- **参数名**: `FrArTpSduTxId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65536]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a unique identifier for a received or a to be transmitted message. With this (and by means of e.g. a lookup table) the PDU Router can route the message appropriately without dealing with the particularities of the Transport Layer. This parameter can also be seen as the identifier of a connection.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. FrArTpTxSduRef

- **UUID**: `ECUC:84f2bd32-9b3a-4b4f-8625-4c5869465f63`
- **引用名**: `FrArTpTxSduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a PDU in the global PDU structure.

####### 2. FrArTpRxSdu

**容器属性**:

- **UUID**: `ECUC:d8731acc-40fe-4633-853b-297b53ec6b1d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FrArTpRxSdu`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Describes the Rx SDU

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. FrArTpSduRxId

- **UUID**: `ECUC:11449a7a-0e5f-4585-806f-e7b9943538f9`
- **参数名**: `FrArTpSduRxId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65536]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a unique identifier for a received message. This Id is used in the CancelReceive API call.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. FrArTpRxSduRef

- **UUID**: `ECUC:2fe49c20-df8f-4155-81c1-2a0028c467cd`
- **引用名**: `FrArTpRxSduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a PDU in the global PDU structure.

####### 3. FrArTpTxSdu

**容器属性**:

- **UUID**: `ECUC:dfda3c7c-8f9c-4b60-9906-c46a84e4e450`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FrArTpTxSdu`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Describes the Tx SDU

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. FrArTpSduTxId

- **UUID**: `ECUC:53e537ea-84a2-43cd-a160-3507af15d05c`
- **参数名**: `FrArTpSduTxId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65536]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a unique identifier for a received or a to be transmitted message. With this (and by means of e.g. a lookup table) the PDU Router can route the message appropriately without dealing with the particularities of the Transport Layer. This parameter can also be seen as the identifier of a connection.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. FrArTpTxSduRef

- **UUID**: `ECUC:84f2bd32-9b3a-4b4f-8625-4c5869465f63`
- **引用名**: `FrArTpTxSduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a PDU in the global PDU structure.

####### 4. FrArTpPdu

**容器属性**:

- **UUID**: `ECUC:41f834ea-0a7e-41f1-922b-6ec9fdfca831`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FrArTpPdu`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

Container to hold the PDU parameters.

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. FrArTpPduId

- **UUID**: `ECUC:32c3e70e-66b0-4889-9164-c9b77fd3817f`
- **参数名**: `FrArTpPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65536]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is the identifier of the FlexRay Interface PDUs (Fr N-PDU, Fr L-SDU) in which the Transport Layer Frames of this channel should be transmitted.

######### ENUMERATION 类型参数

########## 1. FrArTpPduDirection

- **UUID**: `ECUC:65ff9cc6-6ff0-4283-91b9-2ef072d144e7`
- **参数名**: `FrArTpPduDirection`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `FRARTP_RX` (来源: AUTOSAR_ECUC)
  - `FRARTP_TX` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the direction of the PDU.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. FrArTpPduRef

- **UUID**: `ECUC:121b4008-ac40-47de-87e5-8aa17f5cccb9`
- **引用名**: `FrArTpPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE

####### 5. FrArTpPduFc

**容器属性**:

- **UUID**: `ECUC:280361eb-2b84-4b66-8694-19e08cc6b8a9`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FrArTpPduFc`
- **多重性**: [0..2]
- **多配置容器**: false

**容器描述**:

This is the identifier of the FlexRay Interface PDUs (Fr N-PDU, Fr L-SDU) in which the Transport Layer Flow Control and Acknowledgement Frames of this channel should be transmitted.

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. FrArTpPduFcId

- **UUID**: `ECUC:c4dd8b01-2977-49fc-8153-c25bb9016a94`
- **参数名**: `FrArTpPduFcId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65536]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is the identifier of the FlexRay Interface PDUs (Fr N-PDU, Fr L-SDU) in which the Transport Layer Flow Control and Acknowledgement Frames of this channel should be transmitted.

######### ENUMERATION 类型参数

########## 1. FrArTpPduFcDirection

- **UUID**: `ECUC:34ddae7a-6ebc-4a17-b16a-ed1d1aa507c5`
- **参数名**: `FrArTpPduFcDirection`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `FRARTP_FC_RX` (来源: AUTOSAR_ECUC)
  - `FRARTP_FC_TX` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the direction of the PDU.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. FrArTpPduFcRef

- **UUID**: `ECUC:67298ee3-3c75-4497-b365-075f234aea20`
- **引用名**: `FrArTpPduFcRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE

##### 4. FrArTpConnection

**容器属性**:

- **UUID**: `ECUC:13a80df6-16e8-4e9b-940b-bbb23b65795a`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FrArTpConnection`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

This container contains the configuration (parameters) of one FlexRay TP connection.

###### 参数配置

此容器包含 **3** 个参数：

####### INTEGER 类型参数

######## 1. FrArTpLa

- **UUID**: `ECUC:e954e143-e9a7-4b6c-852d-8f18e1ca4dda`
- **参数名**: `FrArTpLa`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the Local Address for the respective connection.

######## 2. FrArTpRa

- **UUID**: `ECUC:d61dfa47-2482-40bc-8d65-015f5a973016`
- **参数名**: `FrArTpRa`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the Remote Address for the respective connection.

####### BOOLEAN 类型参数

######## 1. FrArTpMultRec

- **UUID**: `ECUC:16ce2a19-fe14-4138-bccc-d9d65af5b845`
- **参数名**: `FrArTpMultRec`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines, whether this connection is an 1:1 ('false') or an 1:n ('true') connection.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. FrArTpConPduRef

- **UUID**: `ECUC:b67573de-7cb1-4e98-a362-8c7ed26e3e4a`
- **引用名**: `FrArTpConPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..infinite]
- **目标**: `FrArTpPdu`
- **完整路径**: `/AUTOSAR/EcucDefs/FrArTp/FrArTpMultipleConfig/FrArTpChannel/FrArTpPdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Each value defines a PDU to be used for this connection. Thus each value is a PDU-ID given in FrArTpPdu and this array cannot be longer than the array FrArTpPdu.

###### 配置容器

本模块包含 **2** 个配置容器：

####### 1. FrArTpRxSdu

**容器属性**:

- **UUID**: `ECUC:d8731acc-40fe-4633-853b-297b53ec6b1d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FrArTpRxSdu`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Describes the Rx SDU

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. FrArTpSduRxId

- **UUID**: `ECUC:11449a7a-0e5f-4585-806f-e7b9943538f9`
- **参数名**: `FrArTpSduRxId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65536]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a unique identifier for a received message. This Id is used in the CancelReceive API call.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. FrArTpRxSduRef

- **UUID**: `ECUC:2fe49c20-df8f-4155-81c1-2a0028c467cd`
- **引用名**: `FrArTpRxSduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a PDU in the global PDU structure.

####### 2. FrArTpTxSdu

**容器属性**:

- **UUID**: `ECUC:dfda3c7c-8f9c-4b60-9906-c46a84e4e450`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FrArTpTxSdu`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Describes the Tx SDU

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. FrArTpSduTxId

- **UUID**: `ECUC:53e537ea-84a2-43cd-a160-3507af15d05c`
- **参数名**: `FrArTpSduTxId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65536]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a unique identifier for a received or a to be transmitted message. With this (and by means of e.g. a lookup table) the PDU Router can route the message appropriately without dealing with the particularities of the Transport Layer. This parameter can also be seen as the identifier of a connection.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. FrArTpTxSduRef

- **UUID**: `ECUC:84f2bd32-9b3a-4b4f-8625-4c5869465f63`
- **引用名**: `FrArTpTxSduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a PDU in the global PDU structure.

##### 5. FrArTpRxSdu

**容器属性**:

- **UUID**: `ECUC:d8731acc-40fe-4633-853b-297b53ec6b1d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FrArTpRxSdu`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Describes the Rx SDU

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. FrArTpSduRxId

- **UUID**: `ECUC:11449a7a-0e5f-4585-806f-e7b9943538f9`
- **参数名**: `FrArTpSduRxId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65536]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a unique identifier for a received message. This Id is used in the CancelReceive API call.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. FrArTpRxSduRef

- **UUID**: `ECUC:2fe49c20-df8f-4155-81c1-2a0028c467cd`
- **引用名**: `FrArTpRxSduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a PDU in the global PDU structure.

##### 6. FrArTpTxSdu

**容器属性**:

- **UUID**: `ECUC:dfda3c7c-8f9c-4b60-9906-c46a84e4e450`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FrArTpTxSdu`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Describes the Tx SDU

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. FrArTpSduTxId

- **UUID**: `ECUC:53e537ea-84a2-43cd-a160-3507af15d05c`
- **参数名**: `FrArTpSduTxId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65536]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a unique identifier for a received or a to be transmitted message. With this (and by means of e.g. a lookup table) the PDU Router can route the message appropriately without dealing with the particularities of the Transport Layer. This parameter can also be seen as the identifier of a connection.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. FrArTpTxSduRef

- **UUID**: `ECUC:84f2bd32-9b3a-4b4f-8625-4c5869465f63`
- **引用名**: `FrArTpTxSduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a PDU in the global PDU structure.

##### 7. FrArTpPdu

**容器属性**:

- **UUID**: `ECUC:41f834ea-0a7e-41f1-922b-6ec9fdfca831`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FrArTpPdu`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

Container to hold the PDU parameters.

###### 参数配置

此容器包含 **2** 个参数：

####### INTEGER 类型参数

######## 1. FrArTpPduId

- **UUID**: `ECUC:32c3e70e-66b0-4889-9164-c9b77fd3817f`
- **参数名**: `FrArTpPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65536]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is the identifier of the FlexRay Interface PDUs (Fr N-PDU, Fr L-SDU) in which the Transport Layer Frames of this channel should be transmitted.

####### ENUMERATION 类型参数

######## 1. FrArTpPduDirection

- **UUID**: `ECUC:65ff9cc6-6ff0-4283-91b9-2ef072d144e7`
- **参数名**: `FrArTpPduDirection`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `FRARTP_RX` (来源: AUTOSAR_ECUC)
  - `FRARTP_TX` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the direction of the PDU.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. FrArTpPduRef

- **UUID**: `ECUC:121b4008-ac40-47de-87e5-8aa17f5cccb9`
- **引用名**: `FrArTpPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE

##### 8. FrArTpPduFc

**容器属性**:

- **UUID**: `ECUC:280361eb-2b84-4b66-8694-19e08cc6b8a9`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FrArTpPduFc`
- **多重性**: [0..2]
- **多配置容器**: false

**容器描述**:

This is the identifier of the FlexRay Interface PDUs (Fr N-PDU, Fr L-SDU) in which the Transport Layer Flow Control and Acknowledgement Frames of this channel should be transmitted.

###### 参数配置

此容器包含 **2** 个参数：

####### INTEGER 类型参数

######## 1. FrArTpPduFcId

- **UUID**: `ECUC:c4dd8b01-2977-49fc-8153-c25bb9016a94`
- **参数名**: `FrArTpPduFcId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65536]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is the identifier of the FlexRay Interface PDUs (Fr N-PDU, Fr L-SDU) in which the Transport Layer Flow Control and Acknowledgement Frames of this channel should be transmitted.

####### ENUMERATION 类型参数

######## 1. FrArTpPduFcDirection

- **UUID**: `ECUC:34ddae7a-6ebc-4a17-b16a-ed1d1aa507c5`
- **参数名**: `FrArTpPduFcDirection`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `FRARTP_FC_RX` (来源: AUTOSAR_ECUC)
  - `FRARTP_FC_TX` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the direction of the PDU.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. FrArTpPduFcRef

- **UUID**: `ECUC:67298ee3-3c75-4497-b365-075f234aea20`
- **引用名**: `FrArTpPduFcRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE

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

1. **FrArTp**
