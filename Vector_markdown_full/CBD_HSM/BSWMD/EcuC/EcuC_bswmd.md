# EcuC - 完整配置文档

*此文档由ARXML文件自动生成，采用层次化结构展示*

**生成时间**: 2025-06-16 14:50:43

## 📑 目录

- [📄 文件信息](#-文件信息)
- [🔧 模块定义](#-模块定义)
  - [EcuC](#ecuc)
- [📦 包结构](#-包结构)
- [⚡ 实现信息](#-实现信息)
- [⚙️ 配置信息](#️-配置信息)

## 📄 文件信息

### Schema信息
- **Schema位置**: `http://autosar.org/schema/r4.0 AUTOSAR_4-0-3.xsd`
- **命名空间**: `http://autosar.org/schema/r4.0`

## 🔧 模块定义

### 1. EcuC

#### 基本信息

- **UUID**: `e7ae0255-c677-4b91-abf4-16c34a9e3cc9`
- **模块名称**: `EcuC`
- **类别**: `VENDOR_SPECIFIC_MODULE_DEFINITION`
- **多重性**: [0..1]
- **支持的变体**:
  - VARIANT-PRE-COMPILE
  - VARIANT-POST-BUILD-LOADABLE
  - VARIANT-POST-BUILD-SELECTABLE

#### 模块描述

Virtual module to collect ECU Configuration specific / global configuration information.

#### 版本历史

共有 **19** 个版本记录：

##### 1. 版本 1.00.00

- **状态**: released
- **发布日期**: 2012-06-12
- **发布者**: vispsc

**变更内容**:

##### 2. 版本 2.00.00

- **状态**: released
- **发布日期**: 2013-01-25
- **发布者**: visms

**变更内容**:

##### 3. 版本 2.00.00

- **状态**: released
- **发布日期**: 2013-03-05
- **发布者**: visrco

**变更内容**:

##### 4. 版本 2.01.00

- **状态**: released
- **发布日期**: 2013-07-19
- **发布者**: visrco

**变更内容**:

##### 5. 版本 2.01.00

- **状态**: released
- **发布日期**: 2013-08-27
- **发布者**: visms

**变更内容**:

##### 6. 版本 2.01.00

- **状态**: released
- **发布日期**: 2013-08-27
- **发布者**: visms

**变更内容**:

##### 7. 版本 3.00.00

- **状态**: released
- **发布日期**: 2013-12-03T08:08:58+01:00
- **发布者**: visms

**变更内容**:

##### 8. 版本 3.01.00

- **状态**: released
- **发布日期**: 2014-04-02
- **发布者**: vispsc

**变更内容**:

##### 9. 版本 3.01.00

- **状态**: released
- **发布日期**: 2014-04-02
- **发布者**: vispsc

**变更内容**:

##### 10. 版本 3.02.00

- **状态**: released
- **发布日期**: 2015-01-07
- **发布者**: visbms

**变更内容**:

##### 11. 版本 3.02.01

- **状态**: released
- **发布日期**: 2015-05-11
- **发布者**: visbms

**变更内容**:

##### 12. 版本 3.02.01

- **状态**: released
- **发布日期**: 2015-06-01
- **发布者**: visbms

**变更内容**:

##### 13. 版本 3.03.00

- **状态**: released
- **发布日期**: 2015-09-14
- **发布者**: visbms

**变更内容**:

##### 14. 版本 3.03.00

- **状态**: released
- **发布日期**: 2015-10-30
- **发布者**: visbms

**变更内容**:

##### 15. 版本 3.04.00

- **状态**: released
- **发布日期**: 2016-09-23T01:37:22+02:00
- **发布者**: visbbk

**变更内容**:

##### 16. 版本 3.05.00

- **状态**: released
- **发布日期**: 2017-01-13
- **发布者**: visbms

**变更内容**:

##### 17. 版本 4.00.00

- **状态**: released
- **发布日期**: 2018-04-09
- **发布者**: visms

**变更内容**:

##### 18. 版本 4.00.00

- **状态**: released
- **发布日期**: 2018-04-10T09:13:35+02:00
- **发布者**: visms

**变更内容**:

##### 19. 版本 5.00.00

- **状态**: released
- **发布日期**: 2020-01-23T14:25:52+01:00
- **发布者**: visms

**变更内容**:

#### 配置容器

本模块包含 **16** 个配置容器：

##### 1. EcucPartitionCollection

**容器属性**:

- **UUID**: `250d7391-aa05-4962-ab51-b2283a94de3a`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EcucPartitionCollection`
- **多重性**: [0..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

Collection of Partitions defined for this ECU.

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. EcucPartition

**容器属性**:

- **UUID**: `c290eaf4-c340-4db3-8b72-e0f024851811`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EcucPartition`
- **多重性**: [0..infinite]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

Definition of one Partition on this ECU.

######## 参数配置

此容器包含 **3** 个参数：

######### BOOLEAN 类型参数

########## 1. EcucPartitionBswModuleExecution

- **UUID**: `b35725c6-3729-457f-b300-5f607de11f67`
- **参数名**: `EcucPartitionBswModuleExecution`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Denotes the main BSW partition. Satellite-BSW modules may also be executed in other Partitions.

########## 2. PartitionCanBeRestarted

- **UUID**: `d292cd30-5dac-4dd6-99bd-31dcb66d3bef`
- **参数名**: `PartitionCanBeRestarted`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Specifies the requirement whether the Partition can be restarted. If set to true all software executing in this partition shall be capable of handling a restart.

######### ENUMERATION 类型参数

########## 1. ASIL

- **UUID**: `276af71d-d64e-4ed3-9e70-13fb8ec3e81c`
- **参数名**: `ASIL`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `QM`
  - `A`
  - `B`
  - `C`
  - `D`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: ASIL level of this Partition.

######## 引用关系

此容器包含 **1** 个引用：

######### INSTANCE-REFERENCE 类型引用

########## 1. EcucPartitionSoftwareComponentInstanceRef

- **UUID**: `037fad95-0c5f-4224-9728-a965d7692e16`
- **引用名**: `EcucPartitionSoftwareComponentInstanceRef`
- **引用类型**: INSTANCE-REFERENCE
- **多重性**: [0..infinite]
- **目标类型**: SW-COMPONENT-PROTOTYPE
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: References the SW Component instances from the Ecu Extract that shall be executed in this partition.

##### 2. EcucPartition

**容器属性**:

- **UUID**: `c290eaf4-c340-4db3-8b72-e0f024851811`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EcucPartition`
- **多重性**: [0..infinite]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

Definition of one Partition on this ECU.

###### 参数配置

此容器包含 **3** 个参数：

####### BOOLEAN 类型参数

######## 1. EcucPartitionBswModuleExecution

- **UUID**: `b35725c6-3729-457f-b300-5f607de11f67`
- **参数名**: `EcucPartitionBswModuleExecution`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Denotes the main BSW partition. Satellite-BSW modules may also be executed in other Partitions.

######## 2. PartitionCanBeRestarted

- **UUID**: `d292cd30-5dac-4dd6-99bd-31dcb66d3bef`
- **参数名**: `PartitionCanBeRestarted`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Specifies the requirement whether the Partition can be restarted. If set to true all software executing in this partition shall be capable of handling a restart.

####### ENUMERATION 类型参数

######## 1. ASIL

- **UUID**: `276af71d-d64e-4ed3-9e70-13fb8ec3e81c`
- **参数名**: `ASIL`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `QM`
  - `A`
  - `B`
  - `C`
  - `D`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: ASIL level of this Partition.

###### 引用关系

此容器包含 **1** 个引用：

####### INSTANCE-REFERENCE 类型引用

######## 1. EcucPartitionSoftwareComponentInstanceRef

- **UUID**: `037fad95-0c5f-4224-9728-a965d7692e16`
- **引用名**: `EcucPartitionSoftwareComponentInstanceRef`
- **引用类型**: INSTANCE-REFERENCE
- **多重性**: [0..infinite]
- **目标类型**: SW-COMPONENT-PROTOTYPE
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: References the SW Component instances from the Ecu Extract that shall be executed in this partition.

##### 3. EcucPduCollection

**容器属性**:

- **UUID**: `8818c6df-e05f-4ac6-bc7f-5c1d78ad7a6d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EcucPduCollection`
- **多重性**: [0..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

Collection of all Pdu objects flowing through the Com-Stack.

###### 参数配置

此容器包含 **2** 个参数：

####### ENUMERATION 类型参数

######## 1. PduIdTypeEnum

- **UUID**: `db5af8d4-4421-43dd-92d1-1696f40f86e8`
- **参数名**: `PduIdTypeEnum`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `UINT8`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `UINT8` (来源: AUTOSAR_ECUC)
  - `UINT16` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: The PduIdType is used within the entire AUTOSAR Com Stack except for bus drivers. The size of this global type depends on the maximum number of PDUs used within one software module. If no software module deals with more PDUs that 256, this type can be set to uint8. If at least one software module handles more than 256 PDUs, this type must be set to uint16. See AUTOSAR_SWS_CommunicationStackTypes for more details.

######## 2. PduLengthTypeEnum

- **UUID**: `456bc2ee-7fe0-4fde-ae59-a44e3eb9b645`
- **参数名**: `PduLengthTypeEnum`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `UINT8`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `UINT8` (来源: AUTOSAR_ECUC)
  - `UINT16` (来源: AUTOSAR_ECUC)
  - `UINT32` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: The PduLengthType is used within the entire AUTOSAR Com Stack except for bus drivers. The size of this global type depends on the maximum length of PDUs to be sent by an ECU. If no segmentation is used the length depends on the maximum payload size of a frame of the underlying communication system (for FlexRay maximum size is 255 bytes, therefore uint8). If segementation is used it depends on the maximum length of a  segmeneted N-PDU (in general uint16 is used). See AUTOSAR_SWS_CommunicationStackTypes for more details.

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. Pdu

**容器属性**:

- **UUID**: `59474fea-ba35-4722-86c0-298652f79f19`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `Pdu`
- **多重性**: [0..infinite]
- **构建后可变**: true
- **多配置容器**: false

**容器描述**:

One Pdu flowing through the COM-Stack.

######## 参数配置

此容器包含 **4** 个参数：

######### INTEGER 类型参数

########## 1. MetaDataLength

- **UUID**: `ECUC:c838922b-b316-448d-9231-b37db46d7178`
- **参数名**: `MetaDataLength`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [1..4]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Number of additional bytes in PDU data that contain auxiliary information (MetaData) for the PDU, e.g. the CAN ID. These bytes are handled as part of the PDU data and increase the PDU data length accordingly.

########## 2. PduLength

- **UUID**: `4d2889da-1db2-4697-a8c8-9a963ca6659e`
- **参数名**: `PduLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The maximum used length of the Pdu in bytes.

######### BOOLEAN 类型参数

########## 1. DynamicLength

- **UUID**: `cdf3a973-b8fd-4f78-af0c-940a247eda2c`
- **参数名**: `DynamicLength`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines whether the Pdu has dynamic length (true) or not (false). Please note that this parameter is only relevant for UserDefinedPdus, UserDefinedIPdus and J1939DcmIPdus.

########## 2. J1939Requestable

- **UUID**: `b7dd244c-406a-4098-af7f-2761c403d5e1`
- **参数名**: `J1939Requestable`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Specifies whether this PDU can be requested on a J1939 bus using the J1939Rm.

The PDU can be transmitted by COM, the RTE, a CDD, J1939Nm, or J1939Dcm. The configuration of J1939Rm for PDUs with J1939Requestable set to TRUE depends strongly on the transmitting module.

RTE: The application receives a callback via service port interface, and triggers one of the signals of the requestable PDU according to the requested PGN.

COM: J1939Rm calls Com_TriggerIPduSendWithMetaData for the requestable PDU.

CDD: J1939Rm calls <Cdd>_RequestIndication, the CDD sends the PDU corresponding to the requested PGN.

J1939Dcm, J1939Nm: J1939Rm calls <Msn>_RequestIndication to trigger transmission of diagnostic messages and the AddressClaimed message.

######## 引用关系

此容器包含 **1** 个引用：

######### FOREIGN-REFERENCE 类型引用

########## 1. SysTPduToFrameMappingRef

- **UUID**: `d7336ad7-cfea-4d7b-b8b8-1e6a1870a68e`
- **引用名**: `SysTPduToFrameMappingRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [0..1]
- **目标类型**: PDU-TO-FRAME-MAPPING
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Optional reference to the PduToFrameMapping from the SystemTemplate which this Pdu represents.

##### 4. Pdu

**容器属性**:

- **UUID**: `59474fea-ba35-4722-86c0-298652f79f19`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `Pdu`
- **多重性**: [0..infinite]
- **构建后可变**: true
- **多配置容器**: false

**容器描述**:

One Pdu flowing through the COM-Stack.

###### 参数配置

此容器包含 **4** 个参数：

####### INTEGER 类型参数

######## 1. MetaDataLength

- **UUID**: `ECUC:c838922b-b316-448d-9231-b37db46d7178`
- **参数名**: `MetaDataLength`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [1..4]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Number of additional bytes in PDU data that contain auxiliary information (MetaData) for the PDU, e.g. the CAN ID. These bytes are handled as part of the PDU data and increase the PDU data length accordingly.

######## 2. PduLength

- **UUID**: `4d2889da-1db2-4697-a8c8-9a963ca6659e`
- **参数名**: `PduLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The maximum used length of the Pdu in bytes.

####### BOOLEAN 类型参数

######## 1. DynamicLength

- **UUID**: `cdf3a973-b8fd-4f78-af0c-940a247eda2c`
- **参数名**: `DynamicLength`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines whether the Pdu has dynamic length (true) or not (false). Please note that this parameter is only relevant for UserDefinedPdus, UserDefinedIPdus and J1939DcmIPdus.

######## 2. J1939Requestable

- **UUID**: `b7dd244c-406a-4098-af7f-2761c403d5e1`
- **参数名**: `J1939Requestable`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Specifies whether this PDU can be requested on a J1939 bus using the J1939Rm.

The PDU can be transmitted by COM, the RTE, a CDD, J1939Nm, or J1939Dcm. The configuration of J1939Rm for PDUs with J1939Requestable set to TRUE depends strongly on the transmitting module.

RTE: The application receives a callback via service port interface, and triggers one of the signals of the requestable PDU according to the requested PGN.

COM: J1939Rm calls Com_TriggerIPduSendWithMetaData for the requestable PDU.

CDD: J1939Rm calls <Cdd>_RequestIndication, the CDD sends the PDU corresponding to the requested PGN.

J1939Dcm, J1939Nm: J1939Rm calls <Msn>_RequestIndication to trigger transmission of diagnostic messages and the AddressClaimed message.

###### 引用关系

此容器包含 **1** 个引用：

####### FOREIGN-REFERENCE 类型引用

######## 1. SysTPduToFrameMappingRef

- **UUID**: `d7336ad7-cfea-4d7b-b8b8-1e6a1870a68e`
- **引用名**: `SysTPduToFrameMappingRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [0..1]
- **目标类型**: PDU-TO-FRAME-MAPPING
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Optional reference to the PduToFrameMapping from the SystemTemplate which this Pdu represents.

##### 5. EcucPostBuildVariants

**容器属性**:

- **UUID**: `73760d3c-721f-44df-91a9-9a492c8ac9d6`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EcucPostBuildVariants`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Collection of toplevel PostBuildSelectable variants. The PredefinedVariants linked inside this container will determine how many PostBuildSelectableVariants exist. If this container exist the name pattern for initialization of BSW modules will be <Mip>_Config_<PredefinedVariant.shortName>. If this container does not exist the name pattern for initialization of BSW modlues will be <Mip>_Config.

###### 引用关系

此容器包含 **1** 个引用：

####### FOREIGN-REFERENCE 类型引用

######## 1. EcucPostBuildVariantRef

- **UUID**: `cf9d9a82-0fe5-4737-849d-4c8d618a901a`
- **引用名**: `EcucPostBuildVariantRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [1..infinite]
- **目标类型**: PREDEFINED-VARIANT
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Reference to a PredefinedVariant that defines one toplevel postBuild configuration set (covering all post-build capable BSW modules). PredefinedVariants that are referenced here shall contain only PostBuildVariantCriterionValueSets.

##### 6. EcucVariationResolver

**容器属性**:

- **UUID**: `b01d7e06-b50d-48dd-b125-78f6169423f8`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EcucVariationResolver`
- **多重性**: [0..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

Collection of PredefinedVariant elements containing definition of values for SwSystemconst which shall be applied when resolving the variability during ECU Configuration.

###### 引用关系

此容器包含 **1** 个引用：

####### FOREIGN-REFERENCE 类型引用

######## 1. PredefinedVariantRef

- **UUID**: `60d9ff2b-25ba-400f-a7ad-a309ce11ac3f`
- **引用名**: `PredefinedVariantRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [1..infinite]
- **目标类型**: PREDEFINED-VARIANT
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Reference to a predefined variant.

##### 7. EcucGeneral

**容器属性**:

- **UUID**: `3a8a9c86-c771-493f-860d-73c360b86679`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EcucGeneral`
- **多重性**: [1..1]
- **构建后可变**: false

**容器描述**:

Global configuration parameters of the EcuC.

###### 参数配置

此容器包含 **20** 个参数：

####### BOOLEAN 类型参数

######## 1. AtomicBitAccessInBitfield

- **UUID**: `ba4b88ff-9737-42c4-9cf8-79be2e7d7657`
- **参数名**: `AtomicBitAccessInBitfield`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Enables optimization for single bit read and write accesses in bit-fields if the compiler creates an atomic access in all cases.
This is compiler and platform dependent and has to be checked and configured very carefully!

Caution
Enabling this configuration option requires atomic bit access in bit-fields. This option must only be enabled if the before mentioned access type is supported by the hardware, the compiler and the used compiler options. Enabling this option without verifying those conditions may lead to data consistency issues.

######## 2. DummyFunction

- **UUID**: `c3edb1b6-81df-4bcd-82a7-df6586fea68c`
- **参数名**: `DummyFunction`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Dummy functions used to avoid NULL pointer entrance in call tables

######## 3. EcuCSafeBswChecks

- **UUID**: `453635cb-1c1c-4b69-a2de-f22bdd194fd9`
- **参数名**: `EcuCSafeBswChecks`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Selects if safety checks are used. These checks improve robustness as e.g. invalid parameters are checked before function is executed. This attribute has to be enabled for safety projects.

######## 4. DummyStatement

- **UUID**: `91edabf5-2694-4f73-ae83-a577c3023936`
- **参数名**: `DummyStatement`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Dummy statements used to avoid compiler warnings about e.g. unused parameters

######## 5. ConditionalGenerating

- **UUID**: `dec1f223-96fb-4072-8a93-21119b3f4471`
- **参数名**: `ConditionalGenerating`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: If enabled, only the files are written to the output directory which are changed in their content. As a result the time stamps will only be updated if changes have been made. Enabling this feature will result in a reduced compile time. Disable the feature if all files shall be updated with the generation step.

######## 6. EcuCUseStdReturnTypeForRte

- **UUID**: `b3e54002-6d2e-4770-8842-e06fbcfb7d0c`
- **参数名**: `EcuCUseStdReturnTypeForRte`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Defines whether the Std_ReturnType is used for RTE.

####### ENUMERATION 类型参数

######## 1. CPUType

- **UUID**: `9ff6589a-80c2-4715-a2a5-30e026b0adf9`
- **参数名**: `CPUType`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CPU8Bit`
  - `CPU16Bit`
  - `CPU32Bit`
  - `CPU64Bit`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Register width of the CPU in bit.

######## 2. ByteOrder

- **UUID**: `a9f5469a-ebf1-4076-ab90-0c6ae3f3f933`
- **参数名**: `ByteOrder`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `BIG_ENDIAN`
  - `LITTLE_ENDIAN`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Byte order on memory level.

######## 3. BitOrder

- **UUID**: `5fbf7a1b-d35b-4811-bde3-523ba77141bc`
- **参数名**: `BitOrder`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `LSB_to_MSB`
  - `MSB_to_LSB`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Bit order on register level.

######## 4. AtomicVariableAccess

- **UUID**: `1ab92396-1bdc-4f9c-a2d4-6367d3952a70`
- **参数名**: `AtomicVariableAccess`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `Atomic8BitAccess`
  - `Atomic16BitAccess`
  - `Atomic32BitAccess`
  - `Atomic64BitAccess`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Selection of Bit size for atomic read and write accesses of global variables.
This configuration switch is compiler and platform dependent and has to be checked and configured very carefully!

Caution
Setting this configuration option to "Atomic16BitAccess" requires atomic access all global 8 Bit and 16 Bit variables.
Setting this configuration option to "Atomic32BitAccess" requires atomic access all global 8 Bit, 16 Bit and 32 Bit variables.
Setting this configuration option to "Atomic64BitAccess" requires atomic access all global 8 Bit, 16 Bit, 32 Bit and 64 Bit variables.
The optimization must only be enabled if the before mentioned access types are supported by the hardware, the compiler and the used compiler options. Enabling the optimization without verifying those conditions may lead to data consistency issues.

######## 5. SizeOfEnum

- **UUID**: `a8c73017-62eb-4b20-8dd0-3fef8f3be8c4`
- **参数名**: `SizeOfEnum`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `Size8Bit`
  - `Size16Bit`
  - `Size32Bit`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Size of type enum in bit.

######## 6. SizeOfInt

- **UUID**: `84419fda-e899-4fc2-a1cf-26fa68817b35`
- **参数名**: `SizeOfInt`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `Size16Bit`
  - `Size32Bit`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Size of type int in bit.

######## 7. SizeOfROMPointer

- **UUID**: `5412cf4f-7df7-4527-a1d5-2362710314a5`
- **参数名**: `SizeOfROMPointer`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `Size16Bit`
  - `Size24Bit`
  - `Size32Bit`
  - `Size64Bit`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Size of ROM pointer in bit.

######## 8. SizeOfRAMPointer

- **UUID**: `6dfdaa3f-b075-4e1c-8e15-3257e4ba3f16`
- **参数名**: `SizeOfRAMPointer`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `Size16Bit`
  - `Size24Bit`
  - `Size32Bit`
  - `Size64Bit`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Size of RAM pointer in bit.

######## 9. BitFieldDataType

- **UUID**: `899f80b5-0a59-4037-854e-e2c06f8a18ed`
- **参数名**: `BitFieldDataType`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `INT`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `UNSIGNED_CHAR`
  - `UNSIGNED_SHORT`
  - `UNSIGNED_INT`
  - `INT`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Defines the data type of a C bit-field.
The default value is int as defined by MISRA.
Other values can be used, but the compiler may add padding bits into the bit-field structures.

######## 10. StructAlignment

- **UUID**: `01496e9f-a778-4ac9-ab83-431e84b06fc1`
- **参数名**: `StructAlignment`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `Auto`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `Auto`
  - `Align8Bit`
  - `Align16Bit`
  - `Align32Bit`
  - `Align64Bit`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Alignment of struct elements.

Alignment is given in bit:
N bit means, that the address of each struct element in bit must be a multiple of N.

Auto Alignment:
In this case, the alignment of each struct element is determined by its natural alignment requirements.

Remark:
The alignment of the overall struct is done automatically and cannot be configured except for structs in arrays (see StructInArrayAlignment).

######## 11. ArrayAlignment

- **UUID**: `8e9a348e-9f0d-442d-ab6d-26bfff273fe4`
- **参数名**: `ArrayAlignment`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `Auto`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `Auto`
  - `Align8Bit`
  - `Align16Bit`
  - `Align32Bit`
  - `Align64Bit` (来源: Vector Informatik)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Alignment of arrays.

Alignment is given in bit:
N bit means, that the size and the address of an array in bit must be a multiple of N.

Auto Alignment:
In this case, the alignment of an array is the same as the alignment of one array element. The address and the size of the array must be a multiple of this alignment requirement.

######## 12. StructInArrayAlignment

- **UUID**: `f2d8c02e-eb73-4fc0-8ecd-1104cf09b3a7`
- **参数名**: `StructInArrayAlignment`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `Auto`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `Auto`
  - `Align8Bit`
  - `Align16Bit`
  - `Align32Bit`
  - `Align64Bit`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Alignment of structs in an array.

Alignment is given in bit:
N bit means, that the size and the address of the struct in bit must be a multiple of N.

Auto Alignment:
In this case, the alignment of the overall struct is determined by the struct element with the most restrictive alignment requirements.

######## 13. DummyStatementKind

- **UUID**: `bb8802c1-94f7-405f-bfa2-a510aad90343`
- **参数名**: `DummyStatementKind`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `None`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `None`
  - `VoidCast`
  - `SelfAssignment`
  - `UserDefined`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Dummy statements used to avoid compiler warnings about e.g. unused parameters.

######## 14. EcucBswImplementationCodeType

- **UUID**: `0a316ab4-312a-4d5c-8190-2d2544e81d7e`
- **参数名**: `EcucBswImplementationCodeType`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `EcuCSourceCode`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `EcuCSourceCode` (来源: Vector Informatik)
  - `EcuCLibrary` (来源: Vector Informatik)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the realization type of MICROSAR BSW modules with Service-SWC APIs at the point in time when the RTE is build:
- Source Code: All BSW modules with Service SWC interfaces are available as Source Code. This option shall be used by default as it allows the RTE to generate optimized code.
- Library: Some or all BSW modules with Service SWC interface are available as library only. This option requires the RTE to disable some optimization strategies.

###### 配置容器

本模块包含 **6** 个配置容器：

####### 1. PostbuildLoadable

**容器属性**:

- **UUID**: `284c0dc6-5122-49e0-a745-af5b5640b50a`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `PostbuildLoadable`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Post-Build Loadable specific settings.

######## 参数配置

此容器包含 **5** 个参数：

######### INTEGER 类型参数

########## 1. AlignmentFillPattern

- **UUID**: `46c914be-6530-4af8-b03e-5f593eafefbf`
- **参数名**: `AlignmentFillPattern`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..255]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Alignment Fill Pattern. Byte pattern which is used for the inserted padding bytes.

########## 2. PBROMStartAddress

- **UUID**: `905d5412-9be7-45f8-8410-74cd4c770f76`
- **参数名**: `PBROMStartAddress`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Start address of post-build ROM data. The defined memory are is used globally for all modules excluding these defined as IndividualPostBuildLoadableModule.

########## 3. PBRAMStartAddress

- **UUID**: `dc48f891-fc61-499a-a8a9-7f6b100c2a56`
- **参数名**: `PBRAMStartAddress`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Start address of post-build RAM data (flexible RAM management). The defined memory are is used globally for all modules excluding these defined as IndividualPostBuildLoadableModule.

########## 4. PBROMEndAddress

- **UUID**: `5851623e-1a5e-4265-994a-a0da66bb3cfc`
- **参数名**: `PBROMEndAddress`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: End address of available ROM for post-build. The defined memory are is used globally for all modules excluding these defined as IndividualPostBuildLoadableModule.

########## 5. PBRAMEndAddress

- **UUID**: `75b0bd12-b06a-438d-87f2-e97e2a927182`
- **参数名**: `PBRAMEndAddress`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: End address of available RAM for post-build. The defined memory are is used globally for all modules excluding these defined as IndividualPostBuildLoadableModule.

######## 配置容器

本模块包含 **3** 个配置容器：

######### 1. IndividualPostBuildLoadableModule

**容器属性**:

- **UUID**: `505b2be0-b264-498f-8b8d-3bc84cbf9445`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IndividualPostBuildLoadableModule`
- **多重性**: [0..infinite]
- **构建后可变**: false

**容器描述**:

Modules that shall be updated individually need to be configured here. For each module a dedicated Post-Build ROM and RAM memory are need to be defined. Modules that are updated individually must not be part of the global root structure. For each module defined here an individual Hex file will be created.

########## 参数配置

此容器包含 **4** 个参数：

########### INTEGER 类型参数

############ 1. ModulePBROMStartAddress

- **UUID**: `ea77ce7a-7000-4911-9c83-8b7d45ba66e3`
- **参数名**: `ModulePBROMStartAddress`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Start address of post-build ROM data.

############ 2. ModulePBRAMStartAddress

- **UUID**: `48c1e42f-1be4-47c7-a88b-df33a022d1a5`
- **参数名**: `ModulePBRAMStartAddress`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Start address of post-build RAM data (flexible RAM management).

############ 3. ModulePBROMEndAddress

- **UUID**: `171d7ef7-8387-4596-8953-abf179e3a83f`
- **参数名**: `ModulePBROMEndAddress`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: End address of available ROM for post-build.

############ 4. ModulePBRAMEndAddress

- **UUID**: `bf843563-00be-488b-aeb3-df3896ee893e`
- **参数名**: `ModulePBRAMEndAddress`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: End address of available RAM for post-build.

########## 配置容器

本模块包含 **1** 个配置容器：

########### 1. ModuleInitializationStructure

**容器属性**:

- **UUID**: `fd0e3493-ed43-4275-8c02-8e3ed404d542`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ModuleInitializationStructure`
- **多重性**: [0..infinite]
- **构建后可变**: false

**容器描述**:

Defines the name of the module initialzation structure(s) used for BSW initialization. Projects not using post-build selectable have one initialization structure. For these projects the parameter ModuleInitStructureStartAddress need not to be configured as the address is equal to the configured ModulePBROMStartAddress.
Projects using selectable post-build have for each module multiple module intialization structures (one for each identity). For each identity one ModuleInitializationStructure container shall be defined. For each container the ModuleInitStructureStartAddress must be configured according to the location of that structure in ROM. All module initialization structures shall be located sequently directly after ModulePBROMStartAddress.

############ 参数配置

此容器包含 **1** 个参数：

############# INTEGER 类型参数

############## 1. ModuleInitStructureStartAddress

- **UUID**: `257a2501-1542-44e1-8f7d-27bad79e3e1f`
- **参数名**: `ModuleInitStructureStartAddress`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Relevant for post-build selectable projects with multiple module initialization structures.
The indicated addresses must follow directly after the PBROMStartAddress. There may be gaps

 If there is only a single initialization structure this container is not relevant as the start address must be equal to PBROMStartAddress.

######### 2. ModuleInitializationStructure

**容器属性**:

- **UUID**: `fd0e3493-ed43-4275-8c02-8e3ed404d542`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ModuleInitializationStructure`
- **多重性**: [0..infinite]
- **构建后可变**: false

**容器描述**:

Defines the name of the module initialzation structure(s) used for BSW initialization. Projects not using post-build selectable have one initialization structure. For these projects the parameter ModuleInitStructureStartAddress need not to be configured as the address is equal to the configured ModulePBROMStartAddress.
Projects using selectable post-build have for each module multiple module intialization structures (one for each identity). For each identity one ModuleInitializationStructure container shall be defined. For each container the ModuleInitStructureStartAddress must be configured according to the location of that structure in ROM. All module initialization structures shall be located sequently directly after ModulePBROMStartAddress.

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. ModuleInitStructureStartAddress

- **UUID**: `257a2501-1542-44e1-8f7d-27bad79e3e1f`
- **参数名**: `ModuleInitStructureStartAddress`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Relevant for post-build selectable projects with multiple module initialization structures.
The indicated addresses must follow directly after the PBROMStartAddress. There may be gaps

 If there is only a single initialization structure this container is not relevant as the start address must be equal to PBROMStartAddress.

######### 3. GlobalInitializationStructure

**容器属性**:

- **UUID**: `feb40a42-897b-496c-8654-b618ea069ae4`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `GlobalInitializationStructure`
- **多重性**: [0..infinite]
- **构建后可变**: false

**容器描述**:

Defines the name of the global root structure(s) used for BSW initialization. Projects not using post-build selectable have one initialization structure. For these projects the parameter GlobalRootStructureStartAddress need not to be configured as the address is equal to the configured PBROMStartAddress.
Projects using selectable post-build have multiple global root structures (one for each identity). For each identity one GlobalInitializationStructure container shall be defined. For each container the GlobalRootStructureStartAddress must be configured according to the location of that structure in ROM. All global root structures shall be located sequently directly after PBROMStartAddress.

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. GlobalRootStructureStartAddress

- **UUID**: `38877ce6-bbec-4d63-a112-e3fc2efe0a7f`
- **参数名**: `GlobalRootStructureStartAddress`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Start address of post-build ROM data.

####### 2. IndividualPostBuildLoadableModule

**容器属性**:

- **UUID**: `505b2be0-b264-498f-8b8d-3bc84cbf9445`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IndividualPostBuildLoadableModule`
- **多重性**: [0..infinite]
- **构建后可变**: false

**容器描述**:

Modules that shall be updated individually need to be configured here. For each module a dedicated Post-Build ROM and RAM memory are need to be defined. Modules that are updated individually must not be part of the global root structure. For each module defined here an individual Hex file will be created.

######## 参数配置

此容器包含 **4** 个参数：

######### INTEGER 类型参数

########## 1. ModulePBROMStartAddress

- **UUID**: `ea77ce7a-7000-4911-9c83-8b7d45ba66e3`
- **参数名**: `ModulePBROMStartAddress`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Start address of post-build ROM data.

########## 2. ModulePBRAMStartAddress

- **UUID**: `48c1e42f-1be4-47c7-a88b-df33a022d1a5`
- **参数名**: `ModulePBRAMStartAddress`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Start address of post-build RAM data (flexible RAM management).

########## 3. ModulePBROMEndAddress

- **UUID**: `171d7ef7-8387-4596-8953-abf179e3a83f`
- **参数名**: `ModulePBROMEndAddress`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: End address of available ROM for post-build.

########## 4. ModulePBRAMEndAddress

- **UUID**: `bf843563-00be-488b-aeb3-df3896ee893e`
- **参数名**: `ModulePBRAMEndAddress`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: End address of available RAM for post-build.

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. ModuleInitializationStructure

**容器属性**:

- **UUID**: `fd0e3493-ed43-4275-8c02-8e3ed404d542`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ModuleInitializationStructure`
- **多重性**: [0..infinite]
- **构建后可变**: false

**容器描述**:

Defines the name of the module initialzation structure(s) used for BSW initialization. Projects not using post-build selectable have one initialization structure. For these projects the parameter ModuleInitStructureStartAddress need not to be configured as the address is equal to the configured ModulePBROMStartAddress.
Projects using selectable post-build have for each module multiple module intialization structures (one for each identity). For each identity one ModuleInitializationStructure container shall be defined. For each container the ModuleInitStructureStartAddress must be configured according to the location of that structure in ROM. All module initialization structures shall be located sequently directly after ModulePBROMStartAddress.

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. ModuleInitStructureStartAddress

- **UUID**: `257a2501-1542-44e1-8f7d-27bad79e3e1f`
- **参数名**: `ModuleInitStructureStartAddress`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Relevant for post-build selectable projects with multiple module initialization structures.
The indicated addresses must follow directly after the PBROMStartAddress. There may be gaps

 If there is only a single initialization structure this container is not relevant as the start address must be equal to PBROMStartAddress.

####### 3. ModuleInitializationStructure

**容器属性**:

- **UUID**: `fd0e3493-ed43-4275-8c02-8e3ed404d542`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ModuleInitializationStructure`
- **多重性**: [0..infinite]
- **构建后可变**: false

**容器描述**:

Defines the name of the module initialzation structure(s) used for BSW initialization. Projects not using post-build selectable have one initialization structure. For these projects the parameter ModuleInitStructureStartAddress need not to be configured as the address is equal to the configured ModulePBROMStartAddress.
Projects using selectable post-build have for each module multiple module intialization structures (one for each identity). For each identity one ModuleInitializationStructure container shall be defined. For each container the ModuleInitStructureStartAddress must be configured according to the location of that structure in ROM. All module initialization structures shall be located sequently directly after ModulePBROMStartAddress.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. ModuleInitStructureStartAddress

- **UUID**: `257a2501-1542-44e1-8f7d-27bad79e3e1f`
- **参数名**: `ModuleInitStructureStartAddress`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Relevant for post-build selectable projects with multiple module initialization structures.
The indicated addresses must follow directly after the PBROMStartAddress. There may be gaps

 If there is only a single initialization structure this container is not relevant as the start address must be equal to PBROMStartAddress.

####### 4. GlobalInitializationStructure

**容器属性**:

- **UUID**: `feb40a42-897b-496c-8654-b618ea069ae4`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `GlobalInitializationStructure`
- **多重性**: [0..infinite]
- **构建后可变**: false

**容器描述**:

Defines the name of the global root structure(s) used for BSW initialization. Projects not using post-build selectable have one initialization structure. For these projects the parameter GlobalRootStructureStartAddress need not to be configured as the address is equal to the configured PBROMStartAddress.
Projects using selectable post-build have multiple global root structures (one for each identity). For each identity one GlobalInitializationStructure container shall be defined. For each container the GlobalRootStructureStartAddress must be configured according to the location of that structure in ROM. All global root structures shall be located sequently directly after PBROMStartAddress.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. GlobalRootStructureStartAddress

- **UUID**: `38877ce6-bbec-4d63-a112-e3fc2efe0a7f`
- **参数名**: `GlobalRootStructureStartAddress`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Start address of post-build ROM data.

####### 5. BswInitialization

**容器属性**:

- **UUID**: `4ef1ee0a-0680-4229-92a0-8a3e5b95a281`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswInitialization`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Contains all functions

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. InitFunction

**容器属性**:

- **UUID**: `e5399363-cbc5-47e5-807b-4d5d84873cf4`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `InitFunction`
- **多重性**: [0..infinite]
- **构建后可变**: false

**容器描述**:

Name of the init function.

E.g. ComM_Init

########## 参数配置

此容器包含 **6** 个参数：

########### STRING 类型参数

############ 1. Header

- **UUID**: `361a0f50-d495-4c07-b868-cb520f0a437f`
- **参数名**: `Header`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Header which declares function and types.

############ 2. ConfigType

- **UUID**: `022abb92-dac6-4fc6-9b12-4fa01e5090e5`
- **参数名**: `ConfigType`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of ConfigType

############ 3. ConfigPtrName

- **UUID**: `2281ccd9-b4ef-4226-b064-90a3abc6c1dc`
- **参数名**: `ConfigPtrName`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of Config Pointer which shall be passed to function. If Empty no parameter is passed. If Init Function has a pointer, at least a NULL_PTR should be inserted here.

############ 4. ConfigPtrClass

- **UUID**: `665ada5d-8774-4b79-b06e-4cf82ebf520f`
- **参数名**: `ConfigPtrClass`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Memory class of Config Pointer.

############ 5. AdditionalInitCode

- **UUID**: `aaff1f78-a134-41e2-b17f-8124a2d4c0a4`
- **参数名**: `AdditionalInitCode`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Specify additional code which can be referenced from the initialization callouts of EcuM and BswM.

E.g.: Mcu_InitClock()

If it is necessary to call a function with a module pointer from the global postbuild-loadable configuration, the placeholder %CONFIGPTR% can be used:

E.g.: Mcu_Init(%CONFIGPTR%)

########### ENUMERATION 类型参数

############ 1. InitPhase

- **UUID**: `98352724-abbf-4d8e-b10f-1c28a50cb75c`
- **参数名**: `InitPhase`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `INIT_TWO_POST_NVMREADALL`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `NO_INIT` (来源: Vector Informatik)
  - `INIT_MEMORY` (来源: Vector Informatik)
  - `INIT_ZERO` (来源: Vector Informatik)
  - `INIT_ONE_EARLY` (来源: Vector Informatik)
  - `INIT_ONE` (来源: Vector Informatik)
  - `INIT_ONE_LATE` (来源: Vector Informatik)
  - `INIT_TWO_MCAL` (来源: Vector Informatik)
  - `INIT_TWO_TRCV` (来源: Vector Informatik)
  - `INIT_TWO_DRV` (来源: Vector Informatik)
  - `INIT_TWO_IF` (来源: Vector Informatik)
  - `INIT_TWO_COM` (来源: Vector Informatik)
  - `INIT_TWO_SM` (来源: Vector Informatik)
  - `INIT_TWO_NM` (来源: Vector Informatik)
  - `INIT_TWO_TP` (来源: Vector Informatik)
  - `INIT_TWO_SYS` (来源: Vector Informatik)
  - `INIT_TWO_POST_NVMREADALL` (来源: Vector Informatik)
  - `INIT_THREE` (来源: Vector Informatik)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Phase in which this init function shall be called.

########## 引用关系

此容器包含 **1** 个引用：

########### FOREIGN-REFERENCE 类型引用

############ 1. ModuleRef

- **UUID**: `1e22af04-736f-4d08-b501-ef695dd87991`
- **引用名**: `ModuleRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [1..1]
- **目标类型**: ECUC-MODULE-CONFIGURATION-VALUES
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Reference to module for initialization.

####### 6. InitFunction

**容器属性**:

- **UUID**: `e5399363-cbc5-47e5-807b-4d5d84873cf4`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `InitFunction`
- **多重性**: [0..infinite]
- **构建后可变**: false

**容器描述**:

Name of the init function.

E.g. ComM_Init

######## 参数配置

此容器包含 **6** 个参数：

######### STRING 类型参数

########## 1. Header

- **UUID**: `361a0f50-d495-4c07-b868-cb520f0a437f`
- **参数名**: `Header`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Header which declares function and types.

########## 2. ConfigType

- **UUID**: `022abb92-dac6-4fc6-9b12-4fa01e5090e5`
- **参数名**: `ConfigType`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of ConfigType

########## 3. ConfigPtrName

- **UUID**: `2281ccd9-b4ef-4226-b064-90a3abc6c1dc`
- **参数名**: `ConfigPtrName`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of Config Pointer which shall be passed to function. If Empty no parameter is passed. If Init Function has a pointer, at least a NULL_PTR should be inserted here.

########## 4. ConfigPtrClass

- **UUID**: `665ada5d-8774-4b79-b06e-4cf82ebf520f`
- **参数名**: `ConfigPtrClass`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Memory class of Config Pointer.

########## 5. AdditionalInitCode

- **UUID**: `aaff1f78-a134-41e2-b17f-8124a2d4c0a4`
- **参数名**: `AdditionalInitCode`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Specify additional code which can be referenced from the initialization callouts of EcuM and BswM.

E.g.: Mcu_InitClock()

If it is necessary to call a function with a module pointer from the global postbuild-loadable configuration, the placeholder %CONFIGPTR% can be used:

E.g.: Mcu_Init(%CONFIGPTR%)

######### ENUMERATION 类型参数

########## 1. InitPhase

- **UUID**: `98352724-abbf-4d8e-b10f-1c28a50cb75c`
- **参数名**: `InitPhase`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `INIT_TWO_POST_NVMREADALL`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `NO_INIT` (来源: Vector Informatik)
  - `INIT_MEMORY` (来源: Vector Informatik)
  - `INIT_ZERO` (来源: Vector Informatik)
  - `INIT_ONE_EARLY` (来源: Vector Informatik)
  - `INIT_ONE` (来源: Vector Informatik)
  - `INIT_ONE_LATE` (来源: Vector Informatik)
  - `INIT_TWO_MCAL` (来源: Vector Informatik)
  - `INIT_TWO_TRCV` (来源: Vector Informatik)
  - `INIT_TWO_DRV` (来源: Vector Informatik)
  - `INIT_TWO_IF` (来源: Vector Informatik)
  - `INIT_TWO_COM` (来源: Vector Informatik)
  - `INIT_TWO_SM` (来源: Vector Informatik)
  - `INIT_TWO_NM` (来源: Vector Informatik)
  - `INIT_TWO_TP` (来源: Vector Informatik)
  - `INIT_TWO_SYS` (来源: Vector Informatik)
  - `INIT_TWO_POST_NVMREADALL` (来源: Vector Informatik)
  - `INIT_THREE` (来源: Vector Informatik)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Phase in which this init function shall be called.

######## 引用关系

此容器包含 **1** 个引用：

######### FOREIGN-REFERENCE 类型引用

########## 1. ModuleRef

- **UUID**: `1e22af04-736f-4d08-b501-ef695dd87991`
- **引用名**: `ModuleRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [1..1]
- **目标类型**: ECUC-MODULE-CONFIGURATION-VALUES
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Reference to module for initialization.

##### 8. PostbuildLoadable

**容器属性**:

- **UUID**: `284c0dc6-5122-49e0-a745-af5b5640b50a`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `PostbuildLoadable`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Post-Build Loadable specific settings.

###### 参数配置

此容器包含 **5** 个参数：

####### INTEGER 类型参数

######## 1. AlignmentFillPattern

- **UUID**: `46c914be-6530-4af8-b03e-5f593eafefbf`
- **参数名**: `AlignmentFillPattern`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..255]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Alignment Fill Pattern. Byte pattern which is used for the inserted padding bytes.

######## 2. PBROMStartAddress

- **UUID**: `905d5412-9be7-45f8-8410-74cd4c770f76`
- **参数名**: `PBROMStartAddress`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Start address of post-build ROM data. The defined memory are is used globally for all modules excluding these defined as IndividualPostBuildLoadableModule.

######## 3. PBRAMStartAddress

- **UUID**: `dc48f891-fc61-499a-a8a9-7f6b100c2a56`
- **参数名**: `PBRAMStartAddress`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Start address of post-build RAM data (flexible RAM management). The defined memory are is used globally for all modules excluding these defined as IndividualPostBuildLoadableModule.

######## 4. PBROMEndAddress

- **UUID**: `5851623e-1a5e-4265-994a-a0da66bb3cfc`
- **参数名**: `PBROMEndAddress`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: End address of available ROM for post-build. The defined memory are is used globally for all modules excluding these defined as IndividualPostBuildLoadableModule.

######## 5. PBRAMEndAddress

- **UUID**: `75b0bd12-b06a-438d-87f2-e97e2a927182`
- **参数名**: `PBRAMEndAddress`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: End address of available RAM for post-build. The defined memory are is used globally for all modules excluding these defined as IndividualPostBuildLoadableModule.

###### 配置容器

本模块包含 **3** 个配置容器：

####### 1. IndividualPostBuildLoadableModule

**容器属性**:

- **UUID**: `505b2be0-b264-498f-8b8d-3bc84cbf9445`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IndividualPostBuildLoadableModule`
- **多重性**: [0..infinite]
- **构建后可变**: false

**容器描述**:

Modules that shall be updated individually need to be configured here. For each module a dedicated Post-Build ROM and RAM memory are need to be defined. Modules that are updated individually must not be part of the global root structure. For each module defined here an individual Hex file will be created.

######## 参数配置

此容器包含 **4** 个参数：

######### INTEGER 类型参数

########## 1. ModulePBROMStartAddress

- **UUID**: `ea77ce7a-7000-4911-9c83-8b7d45ba66e3`
- **参数名**: `ModulePBROMStartAddress`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Start address of post-build ROM data.

########## 2. ModulePBRAMStartAddress

- **UUID**: `48c1e42f-1be4-47c7-a88b-df33a022d1a5`
- **参数名**: `ModulePBRAMStartAddress`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Start address of post-build RAM data (flexible RAM management).

########## 3. ModulePBROMEndAddress

- **UUID**: `171d7ef7-8387-4596-8953-abf179e3a83f`
- **参数名**: `ModulePBROMEndAddress`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: End address of available ROM for post-build.

########## 4. ModulePBRAMEndAddress

- **UUID**: `bf843563-00be-488b-aeb3-df3896ee893e`
- **参数名**: `ModulePBRAMEndAddress`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: End address of available RAM for post-build.

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. ModuleInitializationStructure

**容器属性**:

- **UUID**: `fd0e3493-ed43-4275-8c02-8e3ed404d542`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ModuleInitializationStructure`
- **多重性**: [0..infinite]
- **构建后可变**: false

**容器描述**:

Defines the name of the module initialzation structure(s) used for BSW initialization. Projects not using post-build selectable have one initialization structure. For these projects the parameter ModuleInitStructureStartAddress need not to be configured as the address is equal to the configured ModulePBROMStartAddress.
Projects using selectable post-build have for each module multiple module intialization structures (one for each identity). For each identity one ModuleInitializationStructure container shall be defined. For each container the ModuleInitStructureStartAddress must be configured according to the location of that structure in ROM. All module initialization structures shall be located sequently directly after ModulePBROMStartAddress.

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. ModuleInitStructureStartAddress

- **UUID**: `257a2501-1542-44e1-8f7d-27bad79e3e1f`
- **参数名**: `ModuleInitStructureStartAddress`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Relevant for post-build selectable projects with multiple module initialization structures.
The indicated addresses must follow directly after the PBROMStartAddress. There may be gaps

 If there is only a single initialization structure this container is not relevant as the start address must be equal to PBROMStartAddress.

####### 2. ModuleInitializationStructure

**容器属性**:

- **UUID**: `fd0e3493-ed43-4275-8c02-8e3ed404d542`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ModuleInitializationStructure`
- **多重性**: [0..infinite]
- **构建后可变**: false

**容器描述**:

Defines the name of the module initialzation structure(s) used for BSW initialization. Projects not using post-build selectable have one initialization structure. For these projects the parameter ModuleInitStructureStartAddress need not to be configured as the address is equal to the configured ModulePBROMStartAddress.
Projects using selectable post-build have for each module multiple module intialization structures (one for each identity). For each identity one ModuleInitializationStructure container shall be defined. For each container the ModuleInitStructureStartAddress must be configured according to the location of that structure in ROM. All module initialization structures shall be located sequently directly after ModulePBROMStartAddress.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. ModuleInitStructureStartAddress

- **UUID**: `257a2501-1542-44e1-8f7d-27bad79e3e1f`
- **参数名**: `ModuleInitStructureStartAddress`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Relevant for post-build selectable projects with multiple module initialization structures.
The indicated addresses must follow directly after the PBROMStartAddress. There may be gaps

 If there is only a single initialization structure this container is not relevant as the start address must be equal to PBROMStartAddress.

####### 3. GlobalInitializationStructure

**容器属性**:

- **UUID**: `feb40a42-897b-496c-8654-b618ea069ae4`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `GlobalInitializationStructure`
- **多重性**: [0..infinite]
- **构建后可变**: false

**容器描述**:

Defines the name of the global root structure(s) used for BSW initialization. Projects not using post-build selectable have one initialization structure. For these projects the parameter GlobalRootStructureStartAddress need not to be configured as the address is equal to the configured PBROMStartAddress.
Projects using selectable post-build have multiple global root structures (one for each identity). For each identity one GlobalInitializationStructure container shall be defined. For each container the GlobalRootStructureStartAddress must be configured according to the location of that structure in ROM. All global root structures shall be located sequently directly after PBROMStartAddress.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. GlobalRootStructureStartAddress

- **UUID**: `38877ce6-bbec-4d63-a112-e3fc2efe0a7f`
- **参数名**: `GlobalRootStructureStartAddress`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Start address of post-build ROM data.

##### 9. IndividualPostBuildLoadableModule

**容器属性**:

- **UUID**: `505b2be0-b264-498f-8b8d-3bc84cbf9445`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IndividualPostBuildLoadableModule`
- **多重性**: [0..infinite]
- **构建后可变**: false

**容器描述**:

Modules that shall be updated individually need to be configured here. For each module a dedicated Post-Build ROM and RAM memory are need to be defined. Modules that are updated individually must not be part of the global root structure. For each module defined here an individual Hex file will be created.

###### 参数配置

此容器包含 **4** 个参数：

####### INTEGER 类型参数

######## 1. ModulePBROMStartAddress

- **UUID**: `ea77ce7a-7000-4911-9c83-8b7d45ba66e3`
- **参数名**: `ModulePBROMStartAddress`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Start address of post-build ROM data.

######## 2. ModulePBRAMStartAddress

- **UUID**: `48c1e42f-1be4-47c7-a88b-df33a022d1a5`
- **参数名**: `ModulePBRAMStartAddress`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Start address of post-build RAM data (flexible RAM management).

######## 3. ModulePBROMEndAddress

- **UUID**: `171d7ef7-8387-4596-8953-abf179e3a83f`
- **参数名**: `ModulePBROMEndAddress`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: End address of available ROM for post-build.

######## 4. ModulePBRAMEndAddress

- **UUID**: `bf843563-00be-488b-aeb3-df3896ee893e`
- **参数名**: `ModulePBRAMEndAddress`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: End address of available RAM for post-build.

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. ModuleInitializationStructure

**容器属性**:

- **UUID**: `fd0e3493-ed43-4275-8c02-8e3ed404d542`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ModuleInitializationStructure`
- **多重性**: [0..infinite]
- **构建后可变**: false

**容器描述**:

Defines the name of the module initialzation structure(s) used for BSW initialization. Projects not using post-build selectable have one initialization structure. For these projects the parameter ModuleInitStructureStartAddress need not to be configured as the address is equal to the configured ModulePBROMStartAddress.
Projects using selectable post-build have for each module multiple module intialization structures (one for each identity). For each identity one ModuleInitializationStructure container shall be defined. For each container the ModuleInitStructureStartAddress must be configured according to the location of that structure in ROM. All module initialization structures shall be located sequently directly after ModulePBROMStartAddress.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. ModuleInitStructureStartAddress

- **UUID**: `257a2501-1542-44e1-8f7d-27bad79e3e1f`
- **参数名**: `ModuleInitStructureStartAddress`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Relevant for post-build selectable projects with multiple module initialization structures.
The indicated addresses must follow directly after the PBROMStartAddress. There may be gaps

 If there is only a single initialization structure this container is not relevant as the start address must be equal to PBROMStartAddress.

##### 10. ModuleInitializationStructure

**容器属性**:

- **UUID**: `fd0e3493-ed43-4275-8c02-8e3ed404d542`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ModuleInitializationStructure`
- **多重性**: [0..infinite]
- **构建后可变**: false

**容器描述**:

Defines the name of the module initialzation structure(s) used for BSW initialization. Projects not using post-build selectable have one initialization structure. For these projects the parameter ModuleInitStructureStartAddress need not to be configured as the address is equal to the configured ModulePBROMStartAddress.
Projects using selectable post-build have for each module multiple module intialization structures (one for each identity). For each identity one ModuleInitializationStructure container shall be defined. For each container the ModuleInitStructureStartAddress must be configured according to the location of that structure in ROM. All module initialization structures shall be located sequently directly after ModulePBROMStartAddress.

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. ModuleInitStructureStartAddress

- **UUID**: `257a2501-1542-44e1-8f7d-27bad79e3e1f`
- **参数名**: `ModuleInitStructureStartAddress`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Relevant for post-build selectable projects with multiple module initialization structures.
The indicated addresses must follow directly after the PBROMStartAddress. There may be gaps

 If there is only a single initialization structure this container is not relevant as the start address must be equal to PBROMStartAddress.

##### 11. GlobalInitializationStructure

**容器属性**:

- **UUID**: `feb40a42-897b-496c-8654-b618ea069ae4`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `GlobalInitializationStructure`
- **多重性**: [0..infinite]
- **构建后可变**: false

**容器描述**:

Defines the name of the global root structure(s) used for BSW initialization. Projects not using post-build selectable have one initialization structure. For these projects the parameter GlobalRootStructureStartAddress need not to be configured as the address is equal to the configured PBROMStartAddress.
Projects using selectable post-build have multiple global root structures (one for each identity). For each identity one GlobalInitializationStructure container shall be defined. For each container the GlobalRootStructureStartAddress must be configured according to the location of that structure in ROM. All global root structures shall be located sequently directly after PBROMStartAddress.

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. GlobalRootStructureStartAddress

- **UUID**: `38877ce6-bbec-4d63-a112-e3fc2efe0a7f`
- **参数名**: `GlobalRootStructureStartAddress`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Start address of post-build ROM data.

##### 12. BswInitialization

**容器属性**:

- **UUID**: `4ef1ee0a-0680-4229-92a0-8a3e5b95a281`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswInitialization`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Contains all functions

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. InitFunction

**容器属性**:

- **UUID**: `e5399363-cbc5-47e5-807b-4d5d84873cf4`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `InitFunction`
- **多重性**: [0..infinite]
- **构建后可变**: false

**容器描述**:

Name of the init function.

E.g. ComM_Init

######## 参数配置

此容器包含 **6** 个参数：

######### STRING 类型参数

########## 1. Header

- **UUID**: `361a0f50-d495-4c07-b868-cb520f0a437f`
- **参数名**: `Header`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Header which declares function and types.

########## 2. ConfigType

- **UUID**: `022abb92-dac6-4fc6-9b12-4fa01e5090e5`
- **参数名**: `ConfigType`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of ConfigType

########## 3. ConfigPtrName

- **UUID**: `2281ccd9-b4ef-4226-b064-90a3abc6c1dc`
- **参数名**: `ConfigPtrName`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of Config Pointer which shall be passed to function. If Empty no parameter is passed. If Init Function has a pointer, at least a NULL_PTR should be inserted here.

########## 4. ConfigPtrClass

- **UUID**: `665ada5d-8774-4b79-b06e-4cf82ebf520f`
- **参数名**: `ConfigPtrClass`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Memory class of Config Pointer.

########## 5. AdditionalInitCode

- **UUID**: `aaff1f78-a134-41e2-b17f-8124a2d4c0a4`
- **参数名**: `AdditionalInitCode`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Specify additional code which can be referenced from the initialization callouts of EcuM and BswM.

E.g.: Mcu_InitClock()

If it is necessary to call a function with a module pointer from the global postbuild-loadable configuration, the placeholder %CONFIGPTR% can be used:

E.g.: Mcu_Init(%CONFIGPTR%)

######### ENUMERATION 类型参数

########## 1. InitPhase

- **UUID**: `98352724-abbf-4d8e-b10f-1c28a50cb75c`
- **参数名**: `InitPhase`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `INIT_TWO_POST_NVMREADALL`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `NO_INIT` (来源: Vector Informatik)
  - `INIT_MEMORY` (来源: Vector Informatik)
  - `INIT_ZERO` (来源: Vector Informatik)
  - `INIT_ONE_EARLY` (来源: Vector Informatik)
  - `INIT_ONE` (来源: Vector Informatik)
  - `INIT_ONE_LATE` (来源: Vector Informatik)
  - `INIT_TWO_MCAL` (来源: Vector Informatik)
  - `INIT_TWO_TRCV` (来源: Vector Informatik)
  - `INIT_TWO_DRV` (来源: Vector Informatik)
  - `INIT_TWO_IF` (来源: Vector Informatik)
  - `INIT_TWO_COM` (来源: Vector Informatik)
  - `INIT_TWO_SM` (来源: Vector Informatik)
  - `INIT_TWO_NM` (来源: Vector Informatik)
  - `INIT_TWO_TP` (来源: Vector Informatik)
  - `INIT_TWO_SYS` (来源: Vector Informatik)
  - `INIT_TWO_POST_NVMREADALL` (来源: Vector Informatik)
  - `INIT_THREE` (来源: Vector Informatik)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Phase in which this init function shall be called.

######## 引用关系

此容器包含 **1** 个引用：

######### FOREIGN-REFERENCE 类型引用

########## 1. ModuleRef

- **UUID**: `1e22af04-736f-4d08-b501-ef695dd87991`
- **引用名**: `ModuleRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [1..1]
- **目标类型**: ECUC-MODULE-CONFIGURATION-VALUES
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Reference to module for initialization.

##### 13. InitFunction

**容器属性**:

- **UUID**: `e5399363-cbc5-47e5-807b-4d5d84873cf4`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `InitFunction`
- **多重性**: [0..infinite]
- **构建后可变**: false

**容器描述**:

Name of the init function.

E.g. ComM_Init

###### 参数配置

此容器包含 **6** 个参数：

####### STRING 类型参数

######## 1. Header

- **UUID**: `361a0f50-d495-4c07-b868-cb520f0a437f`
- **参数名**: `Header`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Header which declares function and types.

######## 2. ConfigType

- **UUID**: `022abb92-dac6-4fc6-9b12-4fa01e5090e5`
- **参数名**: `ConfigType`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of ConfigType

######## 3. ConfigPtrName

- **UUID**: `2281ccd9-b4ef-4226-b064-90a3abc6c1dc`
- **参数名**: `ConfigPtrName`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of Config Pointer which shall be passed to function. If Empty no parameter is passed. If Init Function has a pointer, at least a NULL_PTR should be inserted here.

######## 4. ConfigPtrClass

- **UUID**: `665ada5d-8774-4b79-b06e-4cf82ebf520f`
- **参数名**: `ConfigPtrClass`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Memory class of Config Pointer.

######## 5. AdditionalInitCode

- **UUID**: `aaff1f78-a134-41e2-b17f-8124a2d4c0a4`
- **参数名**: `AdditionalInitCode`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Specify additional code which can be referenced from the initialization callouts of EcuM and BswM.

E.g.: Mcu_InitClock()

If it is necessary to call a function with a module pointer from the global postbuild-loadable configuration, the placeholder %CONFIGPTR% can be used:

E.g.: Mcu_Init(%CONFIGPTR%)

####### ENUMERATION 类型参数

######## 1. InitPhase

- **UUID**: `98352724-abbf-4d8e-b10f-1c28a50cb75c`
- **参数名**: `InitPhase`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `INIT_TWO_POST_NVMREADALL`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `NO_INIT` (来源: Vector Informatik)
  - `INIT_MEMORY` (来源: Vector Informatik)
  - `INIT_ZERO` (来源: Vector Informatik)
  - `INIT_ONE_EARLY` (来源: Vector Informatik)
  - `INIT_ONE` (来源: Vector Informatik)
  - `INIT_ONE_LATE` (来源: Vector Informatik)
  - `INIT_TWO_MCAL` (来源: Vector Informatik)
  - `INIT_TWO_TRCV` (来源: Vector Informatik)
  - `INIT_TWO_DRV` (来源: Vector Informatik)
  - `INIT_TWO_IF` (来源: Vector Informatik)
  - `INIT_TWO_COM` (来源: Vector Informatik)
  - `INIT_TWO_SM` (来源: Vector Informatik)
  - `INIT_TWO_NM` (来源: Vector Informatik)
  - `INIT_TWO_TP` (来源: Vector Informatik)
  - `INIT_TWO_SYS` (来源: Vector Informatik)
  - `INIT_TWO_POST_NVMREADALL` (来源: Vector Informatik)
  - `INIT_THREE` (来源: Vector Informatik)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Phase in which this init function shall be called.

###### 引用关系

此容器包含 **1** 个引用：

####### FOREIGN-REFERENCE 类型引用

######## 1. ModuleRef

- **UUID**: `1e22af04-736f-4d08-b501-ef695dd87991`
- **引用名**: `ModuleRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [1..1]
- **目标类型**: ECUC-MODULE-CONFIGURATION-VALUES
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Reference to module for initialization.

##### 14. InterruptFunctionality

**容器属性**:

- **UUID**: `80e8941d-060a-4bcc-97af-e44f1033119d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `InterruptFunctionality`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Global interrupt configuration for Mcs12 .

###### 参数配置

此容器包含 **2** 个参数：

####### STRING 类型参数

######## 1. GlobalReEnableCat1

- **UUID**: `12d10515-aad3-4693-986b-d41ce7c3f1ba`
- **参数名**: `GlobalReEnableCat1`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Mcs12 specific parameter. It shall contain a c-Code instruction that re-enables Irqs in interrupt context, to allow nested interrupts of different sources with higher priority. This code is mostly an inline assembler instruction and therefore Compiler specific. It is 
used in case that a driver interrupt is configured as category 1.

######## 2. GlobalReEnableCat2

- **UUID**: `b5f30fc3-1951-4828-b292-116647b9ac2f`
- **参数名**: `GlobalReEnableCat2`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Mcs12 specific parameter. It shall contain a c-Code instruction that re-enables Irqs in interrupt context, to allow nested interrupts of different sources with higher priority. This code is mostly an inline assembler instruction and therefore Compiler specific. It is 
used in case that a driver interrupt is configured as category 2.

##### 15. EcucHardware

**容器属性**:

- **UUID**: `3d666da1-abb2-4916-b416-628c04c8ca67`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EcucHardware`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Hardware definition of this Ecu.

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. EcucCoreDefinition

**容器属性**:

- **UUID**: `41b1b2ce-55b2-49e4-a0fc-3a3f6e29f22e`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EcucCoreDefinition`
- **多重性**: [0..infinite]
- **构建后可变**: false

**容器描述**:

Definition of one Core on this Ecu.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. EcucCoreId

- **UUID**: `5743e138-ff1c-40e7-8d6a-f8e9e02aa50f`
- **参数名**: `EcucCoreId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **来源**: Vector Informatik
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: ID of the core.

######## 引用关系

此容器包含 **1** 个引用：

######### FOREIGN-REFERENCE 类型引用

########## 1. EcucCoreHwRef

- **UUID**: `5753e5f3-9e72-4943-8a14-725c3a615e3e`
- **引用名**: `EcucCoreHwRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [0..1]
- **目标类型**: HW-ELEMENT
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Optional reference to the HwElement of HwCategory ProcessingUnit that represents this Core in the ECU Resource Template.

##### 16. EcucCoreDefinition

**容器属性**:

- **UUID**: `41b1b2ce-55b2-49e4-a0fc-3a3f6e29f22e`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EcucCoreDefinition`
- **多重性**: [0..infinite]
- **构建后可变**: false

**容器描述**:

Definition of one Core on this Ecu.

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. EcucCoreId

- **UUID**: `5743e138-ff1c-40e7-8d6a-f8e9e02aa50f`
- **参数名**: `EcucCoreId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **来源**: Vector Informatik
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: ID of the core.

###### 引用关系

此容器包含 **1** 个引用：

####### FOREIGN-REFERENCE 类型引用

######## 1. EcucCoreHwRef

- **UUID**: `5753e5f3-9e72-4943-8a14-725c3a615e3e`
- **引用名**: `EcucCoreHwRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [0..1]
- **目标类型**: HW-ELEMENT
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Optional reference to the HwElement of HwCategory ProcessingUnit that represents this Core in the ECU Resource Template.

## 📦 包结构

此ARXML文件包含 **1** 个包：

### 1. MICROSAR

- **UUID**: `ff55d029-386d-43a2-b3c2-dfef4c7a5e36`
- **包名称**: `MICROSAR`
- **包含元素数量**: 4

#### 包含的元素

##### ECUC-MODULE-DEF 类型元素

1. **EcuC**

##### BSW-IMPLEMENTATION 类型元素

1. **EcuC_Impl**

##### ECUC-MODULE-CONFIGURATION-VALUES 类型元素

1. **EcuC_Pre**
2. **EcuC_Rec**

## ⚡ 实现信息

此ARXML文件包含 **1** 个实现：

### 1. EcuC_Impl

- **UUID**: `99268391-e6bf-4478-b55f-1540fdb26f03`
- **实现名称**: `EcuC_Impl`
- **编程语言**: C
- **软件版本**: 1.00.00
- **供应商ID**: 30
- **AUTOSAR版本**: 4.00.03
- **代码生成器**: DaVinci Configurator

## ⚙️ 配置信息

此ARXML文件包含 **2** 个配置：

### 1. EcuC_Pre

- **UUID**: `0171be56-dc71-4c7c-8410-b5dd1b2686f7`
- **配置名称**: `EcuC_Pre`
- **定义引用**: `/MICROSAR/EcuC`

### 2. EcuC_Rec

- **UUID**: `1ff1e534-74c4-4744-ad65-c6edf4fc1a9c`
- **配置名称**: `EcuC_Rec`
- **定义引用**: `/MICROSAR/EcuC`
