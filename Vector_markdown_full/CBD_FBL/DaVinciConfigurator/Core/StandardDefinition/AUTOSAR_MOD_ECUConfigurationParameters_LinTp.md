# LinTp - 完整配置文档

*此文档由ARXML文件自动生成，采用层次化结构展示*

**生成时间**: 2025-06-16 14:48:52

## 📑 目录

- [📄 文件信息](#-文件信息)
- [🔧 模块定义](#-模块定义)
  - [LinTp](#lintp)
- [📦 包结构](#-包结构)

## 📄 文件信息

### Schema信息
- **Schema位置**: `http://autosar.org/schema/r4.0 AUTOSAR_4-0-3.xsd`
- **命名空间**: `http://autosar.org/schema/r4.0`

## 🔧 模块定义

### 1. LinTp

#### 基本信息

- **UUID**: `ECUC:6f8dbcae-995f-4506-b84b-0be0f7a3fdc8`
- **模块名称**: `LinTp`
- **多重性**: [0..1]
- **支持的变体**:
  - VARIANT-LINK-TIME
  - VARIANT-POST-BUILD
  - VARIANT-PRE-COMPILE

#### 模块描述

Singleton descriptor for the LIN Transport Protocol.

#### 版本历史

共有 **1** 个版本记录：

##### 1. 版本 4.2.0

- **发布日期**: 2011-11-09
- **发布者**: AUTOSAR

*此版本无详细变更记录*

#### 配置容器

本模块包含 **5** 个配置容器：

##### 1. LinTpGeneral

**容器属性**:

- **UUID**: `ECUC:507bfde0-7d43-44d2-ba6d-7c896dc3a960`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `LinTpGeneral`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

Container that holds all LIN transport protocol general parameters.

###### 参数配置

此容器包含 **1** 个参数：

####### BOOLEAN 类型参数

######## 1. LinTpVersionInfoApi

- **UUID**: `ECUC:bc909b41-a1bb-4fca-9f1a-77f667a29850`
- **参数名**: `LinTpVersionInfoApi`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Switches the LinTp_GetVersionInfo function ON or OFF.

##### 2. LinTpGlobalConfig

**容器属性**:

- **UUID**: `ECUC:28592dff-ba46-4041-afc5-c7c2bebdbede`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `LinTpGlobalConfig`
- **多重性**: [1..1]
- **多配置容器**: true

**容器描述**:

This container contains the global configuration parameter of the LinTp.

###### 参数配置

此容器包含 **5** 个参数：

####### INTEGER 类型参数

######## 1. LinTpMaxNumberOfRespPendingFrames

- **UUID**: `ECUC:890a3d1a-3e8d-49b5-8790-f58e75209c9e`
- **参数名**: `LinTpMaxNumberOfRespPendingFrames`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Configures the maximum number of allowed response pending frames.

######## 2. LinTpNumberOfRxNSdu

- **UUID**: `ECUC:78bf5c48-fb9d-4f36-b6db-a148eb98a1a7`
- **参数名**: `LinTpNumberOfRxNSdu`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Number of transport protocol messages that can be received for all channels this node is connected to.

######## 3. LinTpNumberOfTxNSdu

- **UUID**: `ECUC:52db9c27-df92-4fee-b6c0-b9bf3d447091`
- **参数名**: `LinTpNumberOfTxNSdu`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Number of transport protocol messages that can be transmitted for all channels this node is connected to.

####### FLOAT 类型参数

######## 1. LinTpP2Max

- **UUID**: `ECUC:f5f9d77d-0657-40f0-802f-8c889a6c248a`
- **参数名**: `LinTpP2Max`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0..5]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: P2 Timeout when a response pending frame is expected in seconds.

######## 2. LinTpP2Timing

- **UUID**: `ECUC:7224db3b-049b-4739-a1de-40d00a6c61c5`
- **参数名**: `LinTpP2Timing`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0..5]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Definition of the P2 timeout observation parameter in seconds.

###### 配置容器

本模块包含 **3** 个配置容器：

####### 1. LinTpChannelConfig

**容器属性**:

- **UUID**: `ECUC:3b714729-b20a-4cd1-a2b2-fe456f2b166f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `LinTpChannelConfig`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

This container contains the channel specific configuration parameter of LinTp.

######## 参数配置

此容器包含 **2** 个参数：

######### BOOLEAN 类型参数

########## 1. LinTpDropNotRequestedNad

- **UUID**: `ECUC:623b4adc-f857-4db4-8df2-6a4239c3ea12`
- **参数名**: `LinTpDropNotRequestedNad`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Configures if TP Frames of not requested LIN-Slaves are dropped or not.

########## 2. LinTpScheduleChangeDiag

- **UUID**: `ECUC:a4f81595-1b5d-411a-b67c-12813b6e908e`
- **参数名**: `LinTpScheduleChangeDiag`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enables or disables the call of BswM_LinTp_RequestMode() to diagnostic request/response schedule.

####### 2. LinTpRxNSdu

**容器属性**:

- **UUID**: `ECUC:36e83088-e486-4dad-a4f7-aadafe50dfbe`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `LinTpRxNSdu`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

For each received N-SDU on any channel the node is connected to.

######## 参数配置

此容器包含 **4** 个参数：

######### INTEGER 类型参数

########## 1. LinTpDl

- **UUID**: `ECUC:65010abc-68cc-4364-b4e1-63ab01696cfc`
- **参数名**: `LinTpDl`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..4095]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Data Length Code of this RxNsdu. In case of variable length message, this value indicates the minimum data length.

########## 2. LinTpRxNSduId

- **UUID**: `ECUC:a260e374-b6ba-43eb-97ad-f35f03b2df6c`
- **参数名**: `LinTpRxNSduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The identifier of the Transport Protocol message. This ID will be the one that is communicated with upper layers.

########## 3. LinTpRxNSduNad

- **UUID**: `ECUC:7d1d4df7-f790-4e69-a075-cbd01e2453a9`
- **参数名**: `LinTpRxNSduNad`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: A N-SDU transported on LIN is identified using the NAD for the specific slave.

######### FLOAT 类型参数

########## 1. LinTpNcr

- **UUID**: `ECUC:afea2bb4-341b-478e-b5c3-85c660cf88be`
- **参数名**: `LinTpNcr`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **取值范围**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Value in seconds of the N_Cr timeout. N_Cr is the time until reception of the next Consecutive Frame N_PDU.

######## 引用关系

此容器包含 **2** 个引用：

######### REFERENCE 类型引用

########## 1. LinTpRxNSduPduRef

- **UUID**: `ECUC:c5020b6e-1867-43c2-8ac6-d986c14c95d8`
- **引用名**: `LinTpRxNSduPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the global PDU

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. LinTpRxNSduChannelRef

- **UUID**: `ECUC:50174cd9-703b-4f07-9f44-7d0cff4acef2`
- **引用名**: `LinTpRxNSduChannelRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `LinIfChannel`
- **完整路径**: `/AUTOSAR/EcucDefs/LinIf/LinIfGlobalConfig/LinIfChannel`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Index of the channel this N-SDU belongs to.

####### 3. LinTpTxNSdu

**容器属性**:

- **UUID**: `ECUC:0f57fcb7-8212-43f3-b93d-775bbe842ee5`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `LinTpTxNSdu`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

For each transmitted N-SDU on any channel the node is connected to.

######## 参数配置

此容器包含 **4** 个参数：

######### INTEGER 类型参数

########## 1. LinTpTxNSduId

- **UUID**: `ECUC:e6fac2a8-b8d9-48c7-a221-b0d95b1a6dbb`
- **参数名**: `LinTpTxNSduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The identifier of the Transport Protocol message. This ID will be the one that is communicated with upper layers.

########## 2. LinTpTxNSduNad

- **UUID**: `ECUC:68bd9442-1566-4238-a020-64413a564106`
- **参数名**: `LinTpTxNSduNad`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: A N-SDU transported on LIN is identified using the NAD for the specific slave.

######### FLOAT 类型参数

########## 1. LinTpNas

- **UUID**: `ECUC:53caf4f4-f8d1-4a6c-b58b-ba5b6587c1a8`
- **参数名**: `LinTpNas`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Value in second of the N_As timeout. N_As is the time for transmission of a LIN frame (any N_PDU) on the part of the sender.

########## 2. LinTpNcs

- **UUID**: `ECUC:8e2477c2-4d97-4bce-ad06-edbe632f95db`
- **参数名**: `LinTpNcs`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **取值范围**: [0..Inf]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Value in seconds of the performance requirement of N_Cs. N_Cs is the time which elapses between the transmit request of a CF N-PDU until the transmit request of the next CF N-PDU.

######## 引用关系

此容器包含 **2** 个引用：

######### REFERENCE 类型引用

########## 1. LinTpTxNSduPduRef

- **UUID**: `ECUC:fc9777f3-1e35-44c4-863c-26936aa20382`
- **引用名**: `LinTpTxNSduPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the global PDU

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. LinTpTxNSduChannelRef

- **UUID**: `ECUC:cf97bb02-8432-4030-a195-bfa294ac463d`
- **引用名**: `LinTpTxNSduChannelRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `LinIfChannel`
- **完整路径**: `/AUTOSAR/EcucDefs/LinIf/LinIfGlobalConfig/LinIfChannel`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Index of the channel this N-SDU belongs to.

##### 3. LinTpChannelConfig

**容器属性**:

- **UUID**: `ECUC:3b714729-b20a-4cd1-a2b2-fe456f2b166f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `LinTpChannelConfig`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

This container contains the channel specific configuration parameter of LinTp.

###### 参数配置

此容器包含 **2** 个参数：

####### BOOLEAN 类型参数

######## 1. LinTpDropNotRequestedNad

- **UUID**: `ECUC:623b4adc-f857-4db4-8df2-6a4239c3ea12`
- **参数名**: `LinTpDropNotRequestedNad`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Configures if TP Frames of not requested LIN-Slaves are dropped or not.

######## 2. LinTpScheduleChangeDiag

- **UUID**: `ECUC:a4f81595-1b5d-411a-b67c-12813b6e908e`
- **参数名**: `LinTpScheduleChangeDiag`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enables or disables the call of BswM_LinTp_RequestMode() to diagnostic request/response schedule.

##### 4. LinTpRxNSdu

**容器属性**:

- **UUID**: `ECUC:36e83088-e486-4dad-a4f7-aadafe50dfbe`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `LinTpRxNSdu`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

For each received N-SDU on any channel the node is connected to.

###### 参数配置

此容器包含 **4** 个参数：

####### INTEGER 类型参数

######## 1. LinTpDl

- **UUID**: `ECUC:65010abc-68cc-4364-b4e1-63ab01696cfc`
- **参数名**: `LinTpDl`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..4095]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Data Length Code of this RxNsdu. In case of variable length message, this value indicates the minimum data length.

######## 2. LinTpRxNSduId

- **UUID**: `ECUC:a260e374-b6ba-43eb-97ad-f35f03b2df6c`
- **参数名**: `LinTpRxNSduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The identifier of the Transport Protocol message. This ID will be the one that is communicated with upper layers.

######## 3. LinTpRxNSduNad

- **UUID**: `ECUC:7d1d4df7-f790-4e69-a075-cbd01e2453a9`
- **参数名**: `LinTpRxNSduNad`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: A N-SDU transported on LIN is identified using the NAD for the specific slave.

####### FLOAT 类型参数

######## 1. LinTpNcr

- **UUID**: `ECUC:afea2bb4-341b-478e-b5c3-85c660cf88be`
- **参数名**: `LinTpNcr`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **取值范围**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Value in seconds of the N_Cr timeout. N_Cr is the time until reception of the next Consecutive Frame N_PDU.

###### 引用关系

此容器包含 **2** 个引用：

####### REFERENCE 类型引用

######## 1. LinTpRxNSduPduRef

- **UUID**: `ECUC:c5020b6e-1867-43c2-8ac6-d986c14c95d8`
- **引用名**: `LinTpRxNSduPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the global PDU

####### SYMBOLIC-NAME-REFERENCE 类型引用

######## 1. LinTpRxNSduChannelRef

- **UUID**: `ECUC:50174cd9-703b-4f07-9f44-7d0cff4acef2`
- **引用名**: `LinTpRxNSduChannelRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `LinIfChannel`
- **完整路径**: `/AUTOSAR/EcucDefs/LinIf/LinIfGlobalConfig/LinIfChannel`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Index of the channel this N-SDU belongs to.

##### 5. LinTpTxNSdu

**容器属性**:

- **UUID**: `ECUC:0f57fcb7-8212-43f3-b93d-775bbe842ee5`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `LinTpTxNSdu`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

For each transmitted N-SDU on any channel the node is connected to.

###### 参数配置

此容器包含 **4** 个参数：

####### INTEGER 类型参数

######## 1. LinTpTxNSduId

- **UUID**: `ECUC:e6fac2a8-b8d9-48c7-a221-b0d95b1a6dbb`
- **参数名**: `LinTpTxNSduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The identifier of the Transport Protocol message. This ID will be the one that is communicated with upper layers.

######## 2. LinTpTxNSduNad

- **UUID**: `ECUC:68bd9442-1566-4238-a020-64413a564106`
- **参数名**: `LinTpTxNSduNad`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: A N-SDU transported on LIN is identified using the NAD for the specific slave.

####### FLOAT 类型参数

######## 1. LinTpNas

- **UUID**: `ECUC:53caf4f4-f8d1-4a6c-b58b-ba5b6587c1a8`
- **参数名**: `LinTpNas`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Value in second of the N_As timeout. N_As is the time for transmission of a LIN frame (any N_PDU) on the part of the sender.

######## 2. LinTpNcs

- **UUID**: `ECUC:8e2477c2-4d97-4bce-ad06-edbe632f95db`
- **参数名**: `LinTpNcs`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **取值范围**: [0..Inf]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Value in seconds of the performance requirement of N_Cs. N_Cs is the time which elapses between the transmit request of a CF N-PDU until the transmit request of the next CF N-PDU.

###### 引用关系

此容器包含 **2** 个引用：

####### REFERENCE 类型引用

######## 1. LinTpTxNSduPduRef

- **UUID**: `ECUC:fc9777f3-1e35-44c4-863c-26936aa20382`
- **引用名**: `LinTpTxNSduPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the global PDU

####### SYMBOLIC-NAME-REFERENCE 类型引用

######## 1. LinTpTxNSduChannelRef

- **UUID**: `ECUC:cf97bb02-8432-4030-a195-bfa294ac463d`
- **引用名**: `LinTpTxNSduChannelRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `LinIfChannel`
- **完整路径**: `/AUTOSAR/EcucDefs/LinIf/LinIfGlobalConfig/LinIfChannel`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Index of the channel this N-SDU belongs to.

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

1. **LinTp**
