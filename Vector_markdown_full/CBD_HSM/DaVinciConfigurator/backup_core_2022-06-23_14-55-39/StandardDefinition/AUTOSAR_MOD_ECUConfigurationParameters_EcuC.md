# EcuC - 完整配置文档

*此文档由ARXML文件自动生成，采用层次化结构展示*

**生成时间**: 2025-06-16 14:51:15

## 📑 目录

- [📄 文件信息](#-文件信息)
- [🔧 模块定义](#-模块定义)
  - [EcuC](#ecuc)
- [📦 包结构](#-包结构)

## 📄 文件信息

### Schema信息
- **Schema位置**: `http://autosar.org/schema/r4.0 AUTOSAR_4-0-3.xsd`
- **命名空间**: `http://autosar.org/schema/r4.0`

## 🔧 模块定义

### 1. EcuC

#### 基本信息

- **UUID**: `ECUC:f72efedf-ee71-4a1b-b4d6-b77adfbf4cf2`
- **模块名称**: `EcuC`
- **多重性**: [0..1]
- **支持的变体**:
  - VARIANT-POST-BUILD
  - VARIANT-PRE-COMPILE

#### 模块描述

Virtual module to collect ECU Configuration specific / global configuration information.

#### 版本历史

共有 **1** 个版本记录：

##### 1. 版本 4.2.0

- **发布日期**: 2011-11-09
- **发布者**: AUTOSAR

*此版本无详细变更记录*

#### 配置容器

本模块包含 **7** 个配置容器：

##### 1. EcucPartitionCollection

**容器属性**:

- **UUID**: `ECUC:ed28c0d5-4e0c-4826-89fa-449203a3ce8e`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EcucPartitionCollection`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Collection of Partitions defined for this ECU.

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. EcucPartition

**容器属性**:

- **UUID**: `ECUC:c11de67e-41cd-4da2-8cfc-01c5e34209be`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EcucPartition`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

Definition of one Partition on this ECU.

######## 参数配置

此容器包含 **2** 个参数：

######### BOOLEAN 类型参数

########## 1. EcucPartitionBswModuleExecution

- **UUID**: `ECUC:72f87183-bf87-4f64-a990-38b29817aa2c`
- **参数名**: `EcucPartitionBswModuleExecution`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Denotes that this partition will execute all BSW Modules. BSW Modules can only be executed in one partition.

########## 2. PartitionCanBeRestarted

- **UUID**: `ECUC:4fbca4af-d17a-463a-9b70-fad218ab42a9`
- **参数名**: `PartitionCanBeRestarted`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies the requirement whether the Partition can be restarted. If set to true all software executing in this partition shall be capable of handling a restart.

######## 引用关系

此容器包含 **1** 个引用：

######### INSTANCE-REFERENCE 类型引用

########## 1. EcucPartitionSoftwareComponentInstanceRef

- **UUID**: `ECUC:fcd3eca6-d43f-42f7-86a1-80043415256b`
- **引用名**: `EcucPartitionSoftwareComponentInstanceRef`
- **引用类型**: INSTANCE-REFERENCE
- **多重性**: [0..infinite]
- **目标类型**: SW-COMPONENT-PROTOTYPE
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: References the SW Component instances from the Ecu Extract that shall be executed in this partition.

##### 2. EcucPartition

**容器属性**:

- **UUID**: `ECUC:c11de67e-41cd-4da2-8cfc-01c5e34209be`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EcucPartition`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

Definition of one Partition on this ECU.

###### 参数配置

此容器包含 **2** 个参数：

####### BOOLEAN 类型参数

######## 1. EcucPartitionBswModuleExecution

- **UUID**: `ECUC:72f87183-bf87-4f64-a990-38b29817aa2c`
- **参数名**: `EcucPartitionBswModuleExecution`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Denotes that this partition will execute all BSW Modules. BSW Modules can only be executed in one partition.

######## 2. PartitionCanBeRestarted

- **UUID**: `ECUC:4fbca4af-d17a-463a-9b70-fad218ab42a9`
- **参数名**: `PartitionCanBeRestarted`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies the requirement whether the Partition can be restarted. If set to true all software executing in this partition shall be capable of handling a restart.

###### 引用关系

此容器包含 **1** 个引用：

####### INSTANCE-REFERENCE 类型引用

######## 1. EcucPartitionSoftwareComponentInstanceRef

- **UUID**: `ECUC:fcd3eca6-d43f-42f7-86a1-80043415256b`
- **引用名**: `EcucPartitionSoftwareComponentInstanceRef`
- **引用类型**: INSTANCE-REFERENCE
- **多重性**: [0..infinite]
- **目标类型**: SW-COMPONENT-PROTOTYPE
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: References the SW Component instances from the Ecu Extract that shall be executed in this partition.

##### 3. EcucPduCollection

**容器属性**:

- **UUID**: `ECUC:cece0b62-6981-43fb-a5b7-d573fdfb2344`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EcucPduCollection`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Collection of all Pdu objects flowing through the Com-Stack.

###### 参数配置

此容器包含 **2** 个参数：

####### ENUMERATION 类型参数

######## 1. PduIdTypeEnum

- **UUID**: `ECUC:58955203-89bd-4dcf-b3d4-c5e83c87080b`
- **参数名**: `PduIdTypeEnum`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `UINT16` (来源: AUTOSAR_ECUC)
  - `UINT8` (来源: AUTOSAR_ECUC)
- **描述**: The PduIdType is used within the entire AUTOSAR Com Stack except for bus drivers. The size of this global type depends on the maximum number of PDUs used within one software module. If no software module deals with more PDUs that 256, this type can be set to uint8. If at least one software module handles more than 256 PDUs, this type must be set to uint16. See AUTOSAR_SWS_CommunicationStackTypes for more details.

######## 2. PduLengthTypeEnum

- **UUID**: `ECUC:3ffce745-6c26-4c88-a57f-cd785b21e467`
- **参数名**: `PduLengthTypeEnum`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `UINT16` (来源: AUTOSAR_ECUC)
  - `UINT32` (来源: AUTOSAR_ECUC)
  - `UINT8` (来源: AUTOSAR_ECUC)
- **描述**: The PduLengthType is used within the entire AUTOSAR Com Stack except for bus drivers. The size of this global type depends on the maximum length of PDUs to be sent by an ECU. If no segmentation is used the length depends on the maximum payload size of a frame of the underlying communication system (for FlexRay maximum size is 255 bytes, therefore uint8). If segementation is used it depends on the maximum length of a  segmeneted N-PDU (in general uint16 is used). See AUTOSAR_SWS_CommunicationStackTypes for more details.

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. Pdu

**容器属性**:

- **UUID**: `ECUC:422a7abf-add2-418a-81a6-af5cdeae1930`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `Pdu`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

One Pdu flowing through the COM-Stack.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. PduLength

- **UUID**: `ECUC:3996a201-ffdf-43d1-a5e8-f88592a78a35`
- **参数名**: `PduLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4095]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Length of the Pdu in bytes.  It should be noted that in former AUTOSAR releases (Rel 2.1, Rel 3.0, Rel 3.1, Rel 4.0 Rev. 1) this parameter was defined in bits.

######## 引用关系

此容器包含 **1** 个引用：

######### FOREIGN-REFERENCE 类型引用

########## 1. SysTPduToFrameMappingRef

- **UUID**: `ECUC:44ff5259-e0d4-4c83-bba5-1d113db79352`
- **引用名**: `SysTPduToFrameMappingRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [0..1]
- **目标类型**: PDU-TO-FRAME-MAPPING
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Optional reference to the PduToFrameMapping from the SystemTemplate which this Pdu represents.

##### 4. Pdu

**容器属性**:

- **UUID**: `ECUC:422a7abf-add2-418a-81a6-af5cdeae1930`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `Pdu`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

One Pdu flowing through the COM-Stack.

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. PduLength

- **UUID**: `ECUC:3996a201-ffdf-43d1-a5e8-f88592a78a35`
- **参数名**: `PduLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4095]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Length of the Pdu in bytes.  It should be noted that in former AUTOSAR releases (Rel 2.1, Rel 3.0, Rel 3.1, Rel 4.0 Rev. 1) this parameter was defined in bits.

###### 引用关系

此容器包含 **1** 个引用：

####### FOREIGN-REFERENCE 类型引用

######## 1. SysTPduToFrameMappingRef

- **UUID**: `ECUC:44ff5259-e0d4-4c83-bba5-1d113db79352`
- **引用名**: `SysTPduToFrameMappingRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [0..1]
- **目标类型**: PDU-TO-FRAME-MAPPING
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Optional reference to the PduToFrameMapping from the SystemTemplate which this Pdu represents.

##### 5. EcucVariationResolver

**容器属性**:

- **UUID**: `ECUC:973d00a5-5e98-4b38-8b7b-ddd518d40317`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EcucVariationResolver`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Collection of PredefinedVariant elements containing definition of values for SwSystemconst which shall be applied when resolving the variability during ECU Configuration.

###### 引用关系

此容器包含 **1** 个引用：

####### FOREIGN-REFERENCE 类型引用

######## 1. PredefinedVariantRef

- **UUID**: `ECUC:84013509-59a1-46d4-ba0d-5bcfb76b941f`
- **引用名**: `PredefinedVariantRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [1..infinite]
- **目标类型**: PREDEFINED-VARIANT
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE

##### 6. EcucHardware

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
- **取值范围**: [0..65535]
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
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Optional reference to the HwElement of HwCategory ProcessingUnit that represents this Core in the ECU Resource Template.

##### 7. EcucCoreDefinition

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
- **取值范围**: [0..65535]
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
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Optional reference to the HwElement of HwCategory ProcessingUnit that represents this Core in the ECU Resource Template.

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

1. **EcuC**
