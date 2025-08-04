# Xcp - 完整配置文档

*此文档由ARXML文件自动生成，采用层次化结构展示*

**生成时间**: 2025-06-16 14:46:03

## 📑 目录

- [📄 文件信息](#-文件信息)
- [🔧 模块定义](#-模块定义)
  - [Xcp](#xcp)
- [📦 包结构](#-包结构)
- [⚡ 实现信息](#-实现信息)
- [⚙️ 配置信息](#️-配置信息)

## 📄 文件信息

### Schema信息
- **Schema位置**: `http://autosar.org/schema/r4.0 AUTOSAR_4-0-3.xsd`
- **命名空间**: `http://autosar.org/schema/r4.0`

## 🔧 模块定义

### 1. Xcp

#### 基本信息

- **UUID**: `0d66cf89-0ded-413a-a135-a1b719e0e012`
- **模块名称**: `Xcp`
- **类别**: `VENDOR_SPECIFIC_MODULE_DEFINITION`
- **多重性**: [0..1]
- **支持的变体**:
  - VARIANT-PRE-COMPILE
  - VARIANT-POST-BUILD-LOADABLE
  - VARIANT-POST-BUILD-SELECTABLE

#### 模块描述

Universal Calibration Protocol. XCP is a protocol description based on the ASAM standard between a master (tool) and a slave (device), which provides possibility to calibrate and measure data on the slave.
#Xcp #CANape #CAN #Ethernet #FR #ASAM #AUTOSAR

#### 版本历史

共有 **10** 个版本记录：

##### 1. 版本 1.00.00

- **发布日期**: 2016-12-01
- **发布者**: AUTOSAR

*此版本无详细变更记录*

##### 2. 版本 1.01.00

- **发布日期**: 2017-06-02T13:15:11+02:00
- **发布者**: vishr

**变更内容**:

##### 3. 版本 1.01.01

- **发布日期**: 2018-09-14T09:40:04+02:00
- **发布者**: vishr

**变更内容**:

##### 4. 版本 3.00.00

- **发布日期**: 2019-03-27T07:42:19+01:00
- **发布者**: vishr

**变更内容**:

##### 5. 版本 4.00.00

- **发布日期**: 2020-07-31T12:51:00+02:00
- **发布者**: vishr

**变更内容**:

##### 6. 版本 4.00.01

- **发布日期**: 2020-09-23T10:00:00+02:00
- **发布者**: vishr

**变更内容**:

##### 7. 版本 5.00.00

- **发布日期**: 2021-04-27T07:48:22+02:00
- **发布者**: vishr

**变更内容**:

##### 8. 版本 5.01.00

- **发布日期**: 2021-11-17T14:04:56+01:00
- **发布者**: vishr

**变更内容**:

##### 9. 版本 5.03.00

- **发布日期**: 2021-12-16T07:50:55+01:00
- **发布者**: vishr

**变更内容**:

##### 10. 版本 6.00.00

- **发布日期**: 2024-01-04T08:53:06+01:00
- **发布者**: vishr

**变更内容**:

#### 配置容器

本模块包含 **27** 个配置容器：

##### 1. XcpConfig

**容器属性**:

- **UUID**: `9c04a022-367a-4cd5-9023-36af72183949`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `XcpConfig`
- **多重性**: [1..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container contains the parameters for DAQ, Event, Sector and PDU information

###### 配置容器

本模块包含 **14** 个配置容器：

####### 1. XcpDaqList

**容器属性**:

- **UUID**: `4a8f77c0-be02-4f67-9c28-98da711af256`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `XcpDaqList`
- **多重性**: [0..0]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container contains the configuration of the DAQs.

Container not supported!

######## 参数配置

此容器包含 **4** 个参数：

######### INTEGER 类型参数

########## 1. XcpDaqListNumber

- **UUID**: `1c8dad8a-3e30-4e52-856d-88919b37a518`
- **参数名**: `XcpDaqListNumber`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65534]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Index number of the DAQ list

########## 2. XcpMaxOdt

- **UUID**: `6d3c30f6-d714-488c-9913-b4cf7965bc8b`
- **参数名**: `XcpMaxOdt`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..252]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: MAX_ODT indicates the maximum amount of ODTs in this DAQ list
(STATIC configuration)

########## 3. XcpMaxOdtEntries

- **UUID**: `cc332f4a-1ca0-4f8b-a353-5b00030ece36`
- **参数名**: `XcpMaxOdtEntries`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter indicates the maximum amount of entries in an ODT of this DAQ list (STATIC configuration).

######### ENUMERATION 类型参数

########## 1. XcpDaqListType

- **UUID**: `9dca6965-806c-43cf-a923-dfed2c6ff2cf`
- **参数名**: `XcpDaqListType`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `DAQ` (来源: AUTOSAR_ECUC)
  - `DAQ_STIM` (来源: AUTOSAR_ECUC)
  - `STIM` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This indicates whether this DAQ list represents a DAQ or a STIM.

######## 配置容器

本模块包含 **3** 个配置容器：

######### 1. XcpDto

**容器属性**:

- **UUID**: `c68e6cf6-0119-4ca4-9f8b-8d62c33b78d0`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `XcpDto`
- **多重性**: [0..infinite]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container collects data transfer object specific parameters for the DAQ list.

Container not supported!

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. XcpDtoPid

- **UUID**: `4c003d10-593f-4f33-9ee2-720e4c05c4c2`
- **参数名**: `XcpDtoPid`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..251]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Packet identifier (PID) of the DTO that identifies the ODT the content of the DTO.

########## 引用关系

此容器包含 **1** 个引用：

########### CHOICE-REFERENCE 类型引用

############ 1. XcpDto2PduMapping

- **UUID**: `f24ad608-e696-41d1-b4d3-ea43f3b1c1ce`
- **引用名**: `XcpDto2PduMapping`
- **引用类型**: CHOICE-REFERENCE
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **目标引用列表**:
  - `/AUTOSAR/EcucDefs/Xcp/XcpConfig/XcpPdu/XcpRxPdu`
  - `/AUTOSAR/EcucDefs/Xcp/XcpConfig/XcpPdu/XcpTxPdu`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This reference specifies the mapping of the DTO to the PDUs from the lower-layer interfaces (CanIf, FrIf, SoAd and Cdd).
A reference to a XcpRxPdu is only feasible if the the DaqListType is DAQ_STIM.
A reference to a XcpTxPdu is only feasible if the DaqListType is DAQ.

######### 2. XcpOdt

**容器属性**:

- **UUID**: `7e9240c6-9ffb-44b2-9cc4-4903fcdb293d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `XcpOdt`
- **多重性**: [0..infinite]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container contains ODT-specific parameter for the DAQ list.

Container not supported!

########## 参数配置

此容器包含 **2** 个参数：

########### INTEGER 类型参数

############ 1. XcpOdtEntryMaxSize

- **UUID**: `ac2c6e65-f40a-444d-827d-20209e06c132`
- **参数名**: `XcpOdtEntryMaxSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..254]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter indicates the upper limit for the size of the element described by an ODT entry. Depending on the DaqListType this ODT belongs to it describes the limit for a DAQ (MAX_ODT_ENTRY_SIZE_DAQ) or a STIM (MAX_ODT_ENTRY_SIZE_STIM).

############ 2. XcpOdtNumber

- **UUID**: `2dfda5c6-11b5-4d91-a5b0-2ef44421d49a`
- **参数名**: `XcpOdtNumber`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..251]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Index number of this ODT within the DAQ list.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. XcpOdt2DtoMapping

- **UUID**: `9d721f28-ecc6-43be-8670-cd0c131176de`
- **引用名**: `XcpOdt2DtoMapping`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `XcpDto`
- **完整路径**: `/AUTOSAR/EcucDefs/Xcp/XcpConfig/XcpDaqList/XcpDto`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This reference maps the ODT to the according DTO in which it will be transmitted.

########## 配置容器

本模块包含 **1** 个配置容器：

########### 1. XcpOdtEntry

**容器属性**:

- **UUID**: `88869fa2-bdba-4beb-93e3-e5b0a6b11955`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `XcpOdtEntry`
- **多重性**: [0..infinite]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container collects all configuration parameters that comprise an ODT entry.

Container not supported!

############ 参数配置

此容器包含 **3** 个参数：

############# INTEGER 类型参数

############## 1. XcpOdtEntryLength

- **UUID**: `8e0a56a5-24b0-49d4-a369-9ebc3811a8ab`
- **参数名**: `XcpOdtEntryLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Length of the referenced memory area that is referenced by the ODT entry.

############## 2. XcpOdtEntryNumber

- **UUID**: `0d7b3b2a-e689-448f-a78e-4efb45d12d97`
- **参数名**: `XcpOdtEntryNumber`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..254]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Index number of the ODT entry

############# LINKER-SYMBOL 类型参数

############## 1. XcpOdtEntryAddress

- **UUID**: `07530c73-f6b9-4ba5-b072-53f4d2f5f54c`
- **参数名**: `XcpOdtEntryAddress`
- **数据类型**: LINKER-SYMBOL
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Memory address that the ODT entry is referencing to.

######### 3. XcpOdtEntry

**容器属性**:

- **UUID**: `88869fa2-bdba-4beb-93e3-e5b0a6b11955`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `XcpOdtEntry`
- **多重性**: [0..infinite]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container collects all configuration parameters that comprise an ODT entry.

Container not supported!

########## 参数配置

此容器包含 **3** 个参数：

########### INTEGER 类型参数

############ 1. XcpOdtEntryLength

- **UUID**: `8e0a56a5-24b0-49d4-a369-9ebc3811a8ab`
- **参数名**: `XcpOdtEntryLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Length of the referenced memory area that is referenced by the ODT entry.

############ 2. XcpOdtEntryNumber

- **UUID**: `0d7b3b2a-e689-448f-a78e-4efb45d12d97`
- **参数名**: `XcpOdtEntryNumber`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..254]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Index number of the ODT entry

########### LINKER-SYMBOL 类型参数

############ 1. XcpOdtEntryAddress

- **UUID**: `07530c73-f6b9-4ba5-b072-53f4d2f5f54c`
- **参数名**: `XcpOdtEntryAddress`
- **数据类型**: LINKER-SYMBOL
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Memory address that the ODT entry is referencing to.

####### 2. XcpDto

**容器属性**:

- **UUID**: `c68e6cf6-0119-4ca4-9f8b-8d62c33b78d0`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `XcpDto`
- **多重性**: [0..infinite]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container collects data transfer object specific parameters for the DAQ list.

Container not supported!

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. XcpDtoPid

- **UUID**: `4c003d10-593f-4f33-9ee2-720e4c05c4c2`
- **参数名**: `XcpDtoPid`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..251]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Packet identifier (PID) of the DTO that identifies the ODT the content of the DTO.

######## 引用关系

此容器包含 **1** 个引用：

######### CHOICE-REFERENCE 类型引用

########## 1. XcpDto2PduMapping

- **UUID**: `f24ad608-e696-41d1-b4d3-ea43f3b1c1ce`
- **引用名**: `XcpDto2PduMapping`
- **引用类型**: CHOICE-REFERENCE
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **目标引用列表**:
  - `/AUTOSAR/EcucDefs/Xcp/XcpConfig/XcpPdu/XcpRxPdu`
  - `/AUTOSAR/EcucDefs/Xcp/XcpConfig/XcpPdu/XcpTxPdu`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This reference specifies the mapping of the DTO to the PDUs from the lower-layer interfaces (CanIf, FrIf, SoAd and Cdd).
A reference to a XcpRxPdu is only feasible if the the DaqListType is DAQ_STIM.
A reference to a XcpTxPdu is only feasible if the DaqListType is DAQ.

####### 3. XcpOdt

**容器属性**:

- **UUID**: `7e9240c6-9ffb-44b2-9cc4-4903fcdb293d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `XcpOdt`
- **多重性**: [0..infinite]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container contains ODT-specific parameter for the DAQ list.

Container not supported!

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. XcpOdtEntryMaxSize

- **UUID**: `ac2c6e65-f40a-444d-827d-20209e06c132`
- **参数名**: `XcpOdtEntryMaxSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..254]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter indicates the upper limit for the size of the element described by an ODT entry. Depending on the DaqListType this ODT belongs to it describes the limit for a DAQ (MAX_ODT_ENTRY_SIZE_DAQ) or a STIM (MAX_ODT_ENTRY_SIZE_STIM).

########## 2. XcpOdtNumber

- **UUID**: `2dfda5c6-11b5-4d91-a5b0-2ef44421d49a`
- **参数名**: `XcpOdtNumber`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..251]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Index number of this ODT within the DAQ list.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. XcpOdt2DtoMapping

- **UUID**: `9d721f28-ecc6-43be-8670-cd0c131176de`
- **引用名**: `XcpOdt2DtoMapping`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `XcpDto`
- **完整路径**: `/AUTOSAR/EcucDefs/Xcp/XcpConfig/XcpDaqList/XcpDto`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This reference maps the ODT to the according DTO in which it will be transmitted.

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. XcpOdtEntry

**容器属性**:

- **UUID**: `88869fa2-bdba-4beb-93e3-e5b0a6b11955`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `XcpOdtEntry`
- **多重性**: [0..infinite]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container collects all configuration parameters that comprise an ODT entry.

Container not supported!

########## 参数配置

此容器包含 **3** 个参数：

########### INTEGER 类型参数

############ 1. XcpOdtEntryLength

- **UUID**: `8e0a56a5-24b0-49d4-a369-9ebc3811a8ab`
- **参数名**: `XcpOdtEntryLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Length of the referenced memory area that is referenced by the ODT entry.

############ 2. XcpOdtEntryNumber

- **UUID**: `0d7b3b2a-e689-448f-a78e-4efb45d12d97`
- **参数名**: `XcpOdtEntryNumber`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..254]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Index number of the ODT entry

########### LINKER-SYMBOL 类型参数

############ 1. XcpOdtEntryAddress

- **UUID**: `07530c73-f6b9-4ba5-b072-53f4d2f5f54c`
- **参数名**: `XcpOdtEntryAddress`
- **数据类型**: LINKER-SYMBOL
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Memory address that the ODT entry is referencing to.

####### 4. XcpOdtEntry

**容器属性**:

- **UUID**: `88869fa2-bdba-4beb-93e3-e5b0a6b11955`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `XcpOdtEntry`
- **多重性**: [0..infinite]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container collects all configuration parameters that comprise an ODT entry.

Container not supported!

######## 参数配置

此容器包含 **3** 个参数：

######### INTEGER 类型参数

########## 1. XcpOdtEntryLength

- **UUID**: `8e0a56a5-24b0-49d4-a369-9ebc3811a8ab`
- **参数名**: `XcpOdtEntryLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Length of the referenced memory area that is referenced by the ODT entry.

########## 2. XcpOdtEntryNumber

- **UUID**: `0d7b3b2a-e689-448f-a78e-4efb45d12d97`
- **参数名**: `XcpOdtEntryNumber`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..254]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Index number of the ODT entry

######### LINKER-SYMBOL 类型参数

########## 1. XcpOdtEntryAddress

- **UUID**: `07530c73-f6b9-4ba5-b072-53f4d2f5f54c`
- **参数名**: `XcpOdtEntryAddress`
- **数据类型**: LINKER-SYMBOL
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Memory address that the ODT entry is referencing to.

####### 5. XcpDemEventParameterRefs

**容器属性**:

- **UUID**: `22ee9576-ed4f-4b4d-a16c-a67fed622840`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `XcpDemEventParameterRefs`
- **多重性**: [0..0]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

Container for the references to DemEventParameter elements which shall be invoked using the API Dem_ReportErrorStatus API in case the corresponding error occurs. The EventId is taken from the referenced DemEventParameter's DemEventId value. The standardized errors are provided in the container and can be extended by vendor specific error references.

Container not supported.

######## 引用关系

此容器包含 **1** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. XCP_E_INIT_FAILED

- **UUID**: `df87ad8f-155f-4408-b0dd-7e7fd4beec2a`
- **引用名**: `XCP_E_INIT_FAILED`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `DemEventParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemConfigSet/DemEventParameter`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Reference to the DemEventParameter which shall be issued when the error "Initialization of XCP failed" has occured.

####### 6. XcpTransportLayer

**容器属性**:

- **UUID**: `fb7cefd7-49a1-4938-8b46-9c5c18bb5d53`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `XcpTransportLayer`
- **多重性**: [1..1]
- **构建后可变**: false

**容器描述**:

Container to configure the available Transport Layer.

######## 配置容器

本模块包含 **3** 个配置容器：

######### 1. XcpOnCan

**容器属性**:

- **UUID**: `7819baaf-d770-4466-9a83-0b6b83bf4cba`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `XcpOnCan`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container contains all parameter for the XcpOnCan Transport Layer.

########## 参数配置

此容器包含 **7** 个参数：

########### INTEGER 类型参数

############ 1. XcpOnCanMaxCto

- **UUID**: `df12328d-0f89-40e0-b128-c8ec0535dab1`
- **参数名**: `XcpOnCanMaxCto`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `8`
- **取值范围**: [8..64]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Maximum size of Command Transfer Objects (e.g. for polling)

############ 2. XcpOnCanMaxDto

- **UUID**: `c3c05064-a5ca-4f19-8605-a201ba09e281`
- **参数名**: `XcpOnCanMaxDto`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `8`
- **取值范围**: [8..64]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Maximum size of Data Transfer Objects (e.g. for DAQ)

############ 3. XcpOnCanConfirmationTimeout

- **UUID**: `b20df3f7-ddb3-4ae7-9134-2fe9a15f1a3b`
- **参数名**: `XcpOnCanConfirmationTimeout`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `10`
- **取值范围**: [2..65535]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter defines the number of MainFunction cycles until a Tx confirmation timeout is detected and the respective PDU buffer is reset.

########### BOOLEAN 类型参数

############ 1. XcpOnCanMultiConnectionProtection

- **UUID**: `34446795-9ab5-4ae2-a9dc-75ac9068d7dd`
- **参数名**: `XcpOnCanMultiConnectionProtection`
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
- **描述**: Prevents a connection from a second XCP Master on a different CAN channel, when the first XCP Master has already established a connection.

############ 2. XcpOnCanVariableDlc

- **UUID**: `371bc189-a6f9-4662-848b-047e8b16d604`
- **参数名**: `XcpOnCanVariableDlc`
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
- **描述**: Allow CAN frames with a variable length. If disabled the frames have always the length of the PDU, which can be e.g. 8 Bytes on CAN or 64 Bytes on CAN-FD.

############ 3. XcpPduMode

- **UUID**: `77e1be04-e5c4-43ab-822f-8c55511fe12e`
- **参数名**: `XcpPduMode`
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
- **描述**: If this parameter is enabled an API is enabled that allows the application to delay transmission readyness of the transport layer. This is useful if transmission shall be prevented as long as the underlying bus system is not ready to prevent message loss.

########### STRING 类型参数

############ 1. XcpOnCanUserConfigFile

- **UUID**: `ce2e9365-2bee-4b1f-994c-df81836d92be`
- **参数名**: `XcpOnCanUserConfigFile`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: A configuration file is generated by DaVinci Configurator Pro. If you want to overwrite settings in the generated configuration file, you can specify a path to a user defined configuration file.

The user defined configuration file will be included at the end of the generated file. Therefore definitions in the user defined configuration file can overwrite definitions in the generated configuration file.

The contents of the user defined configuration file is copied to the end of CanXcp_Cfg.h.

######### 2. XcpOnFr

**容器属性**:

- **UUID**: `72ed4be2-d56e-40d5-94f4-7976d8104a9e`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `XcpOnFr`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container contains all parameter for the XcpOnFr Transport Layer.

########## 参数配置

此容器包含 **13** 个参数：

########### INTEGER 类型参数

############ 1. XcpOnFrMaxCto

- **UUID**: `d8f29ae6-f107-4638-982f-51663efd762e`
- **参数名**: `XcpOnFrMaxCto`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `12`
- **取值范围**: [12..254]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter defines the maximum length of Command Transfer Objects (CTO) in bytes. For FlexRay this parameter must be at least 12 and less than the maximum length of the PDU or Link-Layer frame.

############ 2. XcpOnFrMaxDto

- **UUID**: `0c1e0c6b-60ca-4b61-bbbc-756fdf37a81f`
- **参数名**: `XcpOnFrMaxDto`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `12`
- **取值范围**: [12..254]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter defines the maximum length of Data Transfer Objects (DTO). For FlexRay this parameter must be at least 12 and less than the maximum length of the PDU or Link-Layer frame.

############ 3. XcpOnFrConfirmationTimeout

- **UUID**: `0e44a290-e9d1-4af5-ba99-231c7f026c4d`
- **参数名**: `XcpOnFrConfirmationTimeout`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `8`
- **取值范围**: [2..65535]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter defines the number of MainFunction cycles until a Tx confirmation timeout is detected and the respective PDU buffer is reset.

############ 4. XcpOnFrReadCCConfigExtAddr

- **UUID**: `d001f26f-5c7f-4d44-8afe-8f6ac8445c75`
- **参数名**: `XcpOnFrReadCCConfigExtAddr`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `253`
- **取值范围**: [0..255]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: The "Virtual FlexRay Parameters" are accessible with this address extension.

############ 5. XcpOnFrNodeAddress

- **UUID**: `07632362-0e13-43bc-9d2a-6a99d8cae17b`
- **参数名**: `XcpOnFrNodeAddress`
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
- **描述**: This unique node address identifies the XCP slave within a network. This address is normally defined by the system designer and may be the same address as used for the Network Management Node ID.

############ 6. XcpOnFrMaxPDU

- **UUID**: `6b7879db-706b-4077-9b95-e940c64ebaab`
- **参数名**: `XcpOnFrMaxPDU`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `14`
- **取值范围**: [12..254]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter defines the maximum length of PDUs. For FlexRay this parameter must be at least 14 and higher than Max_CTO and Max_DTO.

########### BOOLEAN 类型参数

############ 1. XcpOnFrReadCCConfig

- **UUID**: `261a8ab7-7534-4f39-8083-2c78e1e21a0d`
- **参数名**: `XcpOnFrReadCCConfig`
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
- **描述**: If the "Virtual FlexRay Parameters" feature is enabled, the FlexRay parameters / Communication Controller Config can be read out in a platform independent way. They will be provided as virtual measurement values that can be read at fixed memory locations.

############ 2. XcpOnFrSequenceCounter

- **UUID**: `a10bc529-3139-445f-bf4f-336b5a8f619c`
- **参数名**: `XcpOnFrSequenceCounter`
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
- **描述**: The Sequence Counter is used to detect missing frames as well as to rearrange the ordering of frames if XCP is used asynchronously to the bus, or in the non guaranteed dynamic area of the cycle. If you can not guarantee correct ordering then activate this option. If you are uncertain, then activate this option.

############ 3. XcpOnFrFrameConcatenation

- **UUID**: `687bf5da-45da-4ba8-9ed9-a6fef5b8bc68`
- **参数名**: `XcpOnFrFrameConcatenation`
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
- **描述**: With this attribute you can enable the concatenation of multiple XCP frames into one Protocol Data Unit (PDU). This is useful if your sampling frequency is higher than the FlexRay Cycle, i.e. you call Xcp_Event in a 1ms cycle while you FLexRay cycle is 5ms.

############ 4. XcpOnFrOptimizedCopy

- **UUID**: `c9c9b975-e36a-4e9b-ba5f-605b4caf307a`
- **参数名**: `XcpOnFrOptimizedCopy`
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
- **描述**: If enabled a optimized copy routine is used within the FrXcp. This will improve execution time considerably but requires, on some platforms, certain alignment requirements, e.g. the PDUs must be aligned on a 32bit address within the FlexRay frame.
In most XCP use cases this option can be enabled. If a trap occurs, disable this option.

########### STRING 类型参数

############ 1. XcpOnFrUserConfigFile

- **UUID**: `e5d769da-ea50-4a78-9b82-5b9774a79ca2`
- **参数名**: `XcpOnFrUserConfigFile`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: A configuration file is generated by DaVinci Configurator Pro. If you want to overwrite settings in the generated configuration file, you can specify a path to a user defined configuration file.

The user defined configuration file will be included at the end of the generated file. Therefore definitions in the user defined configuration file can overwrite definitions in the generated configuration file.

The contents of the user defined configuration file is copied to the end of FrXcp_Cfg.h.

########### ENUMERATION 类型参数

############ 1. XcpOnFrFrameAlignment

- **UUID**: `329b0e95-73e5-45a5-8c0a-e46ce59396d1`
- **参数名**: `XcpOnFrFrameAlignment`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `Align8Bit`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `Align8Bit`
  - `Align16Bit`
  - `Align32Bit`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter determines the Alignment of XCP frames within a FlexRay frame. This parameter must be selected according to performance and architectural needs. For details please read the Technical Reference and the ASAM Xcp On FlexRay specification.

############ 2. XcpOnFrTransmissionMode

- **UUID**: `a02a78ad-b278-4a76-b4bb-ac7d3eb23dda`
- **参数名**: `XcpOnFrTransmissionMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `Decoupled`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `Decoupled`
  - `Immediate`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: It is possible to use the XCP either in Immediate or Decoupled Mode. Immediate Mode requires less resources but the FlexRay XCP MainFunctions must be used synchronously to the FlexRay bus. They must be placed such that the their execution finished before actual transmission on the bus happens.

######### 3. XcpOnEth

**容器属性**:

- **UUID**: `1535b67e-580c-43f7-9b76-ae847c503e31`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `XcpOnEth`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container contains all parameter for the XcpOnEth Transport Layer.

########## 参数配置

此容器包含 **10** 个参数：

########### INTEGER 类型参数

############ 1. XcpOnEthMaxCto

- **UUID**: `ff82d678-622e-4ca9-82b4-0e1d602ddee7`
- **参数名**: `XcpOnEthMaxCto`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `255`
- **取值范围**: [8..255]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Maximum size of Command Transfer Objects (e.g. for polling)

############ 2. XcpOnEthMaxDto

- **UUID**: `e0affdbd-5d30-4436-a642-cf5d47392506`
- **参数名**: `XcpOnEthMaxDto`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `255`
- **取值范围**: [8..1448]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Maximum size of Data Transfer Objects (e.g. for DAQ). Maximum size depending on protocol on lower layers, e.g. IPV4 or IPV6 or usage of VLAN.

############ 3. XcpOnEthConfirmationTimeout

- **UUID**: `a5bc5b9c-d60b-41de-8c14-9f43190a0e82`
- **参数名**: `XcpOnEthConfirmationTimeout`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `10`
- **取值范围**: [2..65535]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter defines the number of MainFunction cycles until a Tx confirmation timeout is detected and the respective PDU buffer is reset.

############ 4. XcpBurstSize

- **UUID**: `2738647c-6943-4131-9e84-0531fbb691e8`
- **参数名**: `XcpBurstSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `10`
- **取值范围**: [2..65535]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Defines the number of messages that are sent in a burst. This parameter is only relevant if the parameter Burst Mode is enabled.

########### BOOLEAN 类型参数

############ 1. XcpOnEthMultiConnectionProtection

- **UUID**: `dc91dc93-0427-45b7-b197-5cb8bf29b06a`
- **参数名**: `XcpOnEthMultiConnectionProtection`
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
- **描述**: Prevents a connection from a second XCP Master on a different channel, when the first XCP Master has already established a connection.

############ 2. XcpOnEthOptimizedCopy

- **UUID**: `38511283-4ccb-4d8b-9434-9adf10ceeab2`
- **参数名**: `XcpOnEthOptimizedCopy`
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
- **描述**: If enabled a optimized copy routine is used within the TcpIpXcp. This will improve execution time considerably but requires, on some platforms, certain alignment requirements, e.g. the PDUs must be aligned on a 32bit address within the Ethernet frame.
In most XCP use cases this option can be enabled. If a trap occurs, disable this option.

############ 3. XcpOnEthConcatenationMode

- **UUID**: `e7c4786f-071e-498c-8891-60763f280e3f`
- **参数名**: `XcpOnEthConcatenationMode`
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
- **描述**: If this option is enabled the TcpIpXcp concatenates multiple XCP messages in one Ethernet PDU. This is useful if you use a measurement cycle that is faster than PDUs can be sent on the bus. The concatenation is performed in the MainFunction, therefore the transmission cycle is limited to TcpIpXcp_MainFunction cycles.

############ 4. XcpOnEthBurstMode

- **UUID**: `bf8c7511-e127-4dd7-914e-1eea7549fd1a`
- **参数名**: `XcpOnEthBurstMode`
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
- **描述**: Enables a burst Mode that transmit multiple XCP Frames at once. The Burst Mode can only be enabled if Concatenation Mode is enabled.

############ 5. XcpPduMode

- **UUID**: `bb73f1d1-d077-4ae6-a8c2-d18bab4ef2e7`
- **参数名**: `XcpPduMode`
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
- **描述**: If this parameter is enabled an API is enabled that allows the application to delay transmission readyness of the transport layer. This is useful if transmission shall be prevented as long as the underlying bus system is not ready to prevent message loss.

########### STRING 类型参数

############ 1. XcpOnEthUserConfigFile

- **UUID**: `0f707868-1a7a-4d14-8c57-e7ee793c2cc8`
- **参数名**: `XcpOnEthUserConfigFile`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: A configuration file is generated by DaVinci Configurator Pro. If you want to overwrite settings in the generated configuration file, you can specify a path to a user defined configuration file.

The user defined configuration file will be included at the end of the generated file. Therefore definitions in the user defined configuration file can overwrite definitions in the generated configuration file.

The contents of the user defined configuration file is copied to the end of <Bsw>_Cfg.h.

####### 7. XcpOnCan

**容器属性**:

- **UUID**: `7819baaf-d770-4466-9a83-0b6b83bf4cba`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `XcpOnCan`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container contains all parameter for the XcpOnCan Transport Layer.

######## 参数配置

此容器包含 **7** 个参数：

######### INTEGER 类型参数

########## 1. XcpOnCanMaxCto

- **UUID**: `df12328d-0f89-40e0-b128-c8ec0535dab1`
- **参数名**: `XcpOnCanMaxCto`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `8`
- **取值范围**: [8..64]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Maximum size of Command Transfer Objects (e.g. for polling)

########## 2. XcpOnCanMaxDto

- **UUID**: `c3c05064-a5ca-4f19-8605-a201ba09e281`
- **参数名**: `XcpOnCanMaxDto`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `8`
- **取值范围**: [8..64]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Maximum size of Data Transfer Objects (e.g. for DAQ)

########## 3. XcpOnCanConfirmationTimeout

- **UUID**: `b20df3f7-ddb3-4ae7-9134-2fe9a15f1a3b`
- **参数名**: `XcpOnCanConfirmationTimeout`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `10`
- **取值范围**: [2..65535]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter defines the number of MainFunction cycles until a Tx confirmation timeout is detected and the respective PDU buffer is reset.

######### BOOLEAN 类型参数

########## 1. XcpOnCanMultiConnectionProtection

- **UUID**: `34446795-9ab5-4ae2-a9dc-75ac9068d7dd`
- **参数名**: `XcpOnCanMultiConnectionProtection`
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
- **描述**: Prevents a connection from a second XCP Master on a different CAN channel, when the first XCP Master has already established a connection.

########## 2. XcpOnCanVariableDlc

- **UUID**: `371bc189-a6f9-4662-848b-047e8b16d604`
- **参数名**: `XcpOnCanVariableDlc`
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
- **描述**: Allow CAN frames with a variable length. If disabled the frames have always the length of the PDU, which can be e.g. 8 Bytes on CAN or 64 Bytes on CAN-FD.

########## 3. XcpPduMode

- **UUID**: `77e1be04-e5c4-43ab-822f-8c55511fe12e`
- **参数名**: `XcpPduMode`
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
- **描述**: If this parameter is enabled an API is enabled that allows the application to delay transmission readyness of the transport layer. This is useful if transmission shall be prevented as long as the underlying bus system is not ready to prevent message loss.

######### STRING 类型参数

########## 1. XcpOnCanUserConfigFile

- **UUID**: `ce2e9365-2bee-4b1f-994c-df81836d92be`
- **参数名**: `XcpOnCanUserConfigFile`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: A configuration file is generated by DaVinci Configurator Pro. If you want to overwrite settings in the generated configuration file, you can specify a path to a user defined configuration file.

The user defined configuration file will be included at the end of the generated file. Therefore definitions in the user defined configuration file can overwrite definitions in the generated configuration file.

The contents of the user defined configuration file is copied to the end of CanXcp_Cfg.h.

####### 8. XcpOnFr

**容器属性**:

- **UUID**: `72ed4be2-d56e-40d5-94f4-7976d8104a9e`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `XcpOnFr`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container contains all parameter for the XcpOnFr Transport Layer.

######## 参数配置

此容器包含 **13** 个参数：

######### INTEGER 类型参数

########## 1. XcpOnFrMaxCto

- **UUID**: `d8f29ae6-f107-4638-982f-51663efd762e`
- **参数名**: `XcpOnFrMaxCto`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `12`
- **取值范围**: [12..254]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter defines the maximum length of Command Transfer Objects (CTO) in bytes. For FlexRay this parameter must be at least 12 and less than the maximum length of the PDU or Link-Layer frame.

########## 2. XcpOnFrMaxDto

- **UUID**: `0c1e0c6b-60ca-4b61-bbbc-756fdf37a81f`
- **参数名**: `XcpOnFrMaxDto`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `12`
- **取值范围**: [12..254]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter defines the maximum length of Data Transfer Objects (DTO). For FlexRay this parameter must be at least 12 and less than the maximum length of the PDU or Link-Layer frame.

########## 3. XcpOnFrConfirmationTimeout

- **UUID**: `0e44a290-e9d1-4af5-ba99-231c7f026c4d`
- **参数名**: `XcpOnFrConfirmationTimeout`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `8`
- **取值范围**: [2..65535]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter defines the number of MainFunction cycles until a Tx confirmation timeout is detected and the respective PDU buffer is reset.

########## 4. XcpOnFrReadCCConfigExtAddr

- **UUID**: `d001f26f-5c7f-4d44-8afe-8f6ac8445c75`
- **参数名**: `XcpOnFrReadCCConfigExtAddr`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `253`
- **取值范围**: [0..255]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: The "Virtual FlexRay Parameters" are accessible with this address extension.

########## 5. XcpOnFrNodeAddress

- **UUID**: `07632362-0e13-43bc-9d2a-6a99d8cae17b`
- **参数名**: `XcpOnFrNodeAddress`
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
- **描述**: This unique node address identifies the XCP slave within a network. This address is normally defined by the system designer and may be the same address as used for the Network Management Node ID.

########## 6. XcpOnFrMaxPDU

- **UUID**: `6b7879db-706b-4077-9b95-e940c64ebaab`
- **参数名**: `XcpOnFrMaxPDU`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `14`
- **取值范围**: [12..254]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter defines the maximum length of PDUs. For FlexRay this parameter must be at least 14 and higher than Max_CTO and Max_DTO.

######### BOOLEAN 类型参数

########## 1. XcpOnFrReadCCConfig

- **UUID**: `261a8ab7-7534-4f39-8083-2c78e1e21a0d`
- **参数名**: `XcpOnFrReadCCConfig`
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
- **描述**: If the "Virtual FlexRay Parameters" feature is enabled, the FlexRay parameters / Communication Controller Config can be read out in a platform independent way. They will be provided as virtual measurement values that can be read at fixed memory locations.

########## 2. XcpOnFrSequenceCounter

- **UUID**: `a10bc529-3139-445f-bf4f-336b5a8f619c`
- **参数名**: `XcpOnFrSequenceCounter`
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
- **描述**: The Sequence Counter is used to detect missing frames as well as to rearrange the ordering of frames if XCP is used asynchronously to the bus, or in the non guaranteed dynamic area of the cycle. If you can not guarantee correct ordering then activate this option. If you are uncertain, then activate this option.

########## 3. XcpOnFrFrameConcatenation

- **UUID**: `687bf5da-45da-4ba8-9ed9-a6fef5b8bc68`
- **参数名**: `XcpOnFrFrameConcatenation`
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
- **描述**: With this attribute you can enable the concatenation of multiple XCP frames into one Protocol Data Unit (PDU). This is useful if your sampling frequency is higher than the FlexRay Cycle, i.e. you call Xcp_Event in a 1ms cycle while you FLexRay cycle is 5ms.

########## 4. XcpOnFrOptimizedCopy

- **UUID**: `c9c9b975-e36a-4e9b-ba5f-605b4caf307a`
- **参数名**: `XcpOnFrOptimizedCopy`
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
- **描述**: If enabled a optimized copy routine is used within the FrXcp. This will improve execution time considerably but requires, on some platforms, certain alignment requirements, e.g. the PDUs must be aligned on a 32bit address within the FlexRay frame.
In most XCP use cases this option can be enabled. If a trap occurs, disable this option.

######### STRING 类型参数

########## 1. XcpOnFrUserConfigFile

- **UUID**: `e5d769da-ea50-4a78-9b82-5b9774a79ca2`
- **参数名**: `XcpOnFrUserConfigFile`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: A configuration file is generated by DaVinci Configurator Pro. If you want to overwrite settings in the generated configuration file, you can specify a path to a user defined configuration file.

The user defined configuration file will be included at the end of the generated file. Therefore definitions in the user defined configuration file can overwrite definitions in the generated configuration file.

The contents of the user defined configuration file is copied to the end of FrXcp_Cfg.h.

######### ENUMERATION 类型参数

########## 1. XcpOnFrFrameAlignment

- **UUID**: `329b0e95-73e5-45a5-8c0a-e46ce59396d1`
- **参数名**: `XcpOnFrFrameAlignment`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `Align8Bit`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `Align8Bit`
  - `Align16Bit`
  - `Align32Bit`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter determines the Alignment of XCP frames within a FlexRay frame. This parameter must be selected according to performance and architectural needs. For details please read the Technical Reference and the ASAM Xcp On FlexRay specification.

########## 2. XcpOnFrTransmissionMode

- **UUID**: `a02a78ad-b278-4a76-b4bb-ac7d3eb23dda`
- **参数名**: `XcpOnFrTransmissionMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `Decoupled`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `Decoupled`
  - `Immediate`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: It is possible to use the XCP either in Immediate or Decoupled Mode. Immediate Mode requires less resources but the FlexRay XCP MainFunctions must be used synchronously to the FlexRay bus. They must be placed such that the their execution finished before actual transmission on the bus happens.

####### 9. XcpOnEth

**容器属性**:

- **UUID**: `1535b67e-580c-43f7-9b76-ae847c503e31`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `XcpOnEth`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container contains all parameter for the XcpOnEth Transport Layer.

######## 参数配置

此容器包含 **10** 个参数：

######### INTEGER 类型参数

########## 1. XcpOnEthMaxCto

- **UUID**: `ff82d678-622e-4ca9-82b4-0e1d602ddee7`
- **参数名**: `XcpOnEthMaxCto`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `255`
- **取值范围**: [8..255]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Maximum size of Command Transfer Objects (e.g. for polling)

########## 2. XcpOnEthMaxDto

- **UUID**: `e0affdbd-5d30-4436-a642-cf5d47392506`
- **参数名**: `XcpOnEthMaxDto`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `255`
- **取值范围**: [8..1448]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Maximum size of Data Transfer Objects (e.g. for DAQ). Maximum size depending on protocol on lower layers, e.g. IPV4 or IPV6 or usage of VLAN.

########## 3. XcpOnEthConfirmationTimeout

- **UUID**: `a5bc5b9c-d60b-41de-8c14-9f43190a0e82`
- **参数名**: `XcpOnEthConfirmationTimeout`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `10`
- **取值范围**: [2..65535]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter defines the number of MainFunction cycles until a Tx confirmation timeout is detected and the respective PDU buffer is reset.

########## 4. XcpBurstSize

- **UUID**: `2738647c-6943-4131-9e84-0531fbb691e8`
- **参数名**: `XcpBurstSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `10`
- **取值范围**: [2..65535]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Defines the number of messages that are sent in a burst. This parameter is only relevant if the parameter Burst Mode is enabled.

######### BOOLEAN 类型参数

########## 1. XcpOnEthMultiConnectionProtection

- **UUID**: `dc91dc93-0427-45b7-b197-5cb8bf29b06a`
- **参数名**: `XcpOnEthMultiConnectionProtection`
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
- **描述**: Prevents a connection from a second XCP Master on a different channel, when the first XCP Master has already established a connection.

########## 2. XcpOnEthOptimizedCopy

- **UUID**: `38511283-4ccb-4d8b-9434-9adf10ceeab2`
- **参数名**: `XcpOnEthOptimizedCopy`
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
- **描述**: If enabled a optimized copy routine is used within the TcpIpXcp. This will improve execution time considerably but requires, on some platforms, certain alignment requirements, e.g. the PDUs must be aligned on a 32bit address within the Ethernet frame.
In most XCP use cases this option can be enabled. If a trap occurs, disable this option.

########## 3. XcpOnEthConcatenationMode

- **UUID**: `e7c4786f-071e-498c-8891-60763f280e3f`
- **参数名**: `XcpOnEthConcatenationMode`
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
- **描述**: If this option is enabled the TcpIpXcp concatenates multiple XCP messages in one Ethernet PDU. This is useful if you use a measurement cycle that is faster than PDUs can be sent on the bus. The concatenation is performed in the MainFunction, therefore the transmission cycle is limited to TcpIpXcp_MainFunction cycles.

########## 4. XcpOnEthBurstMode

- **UUID**: `bf8c7511-e127-4dd7-914e-1eea7549fd1a`
- **参数名**: `XcpOnEthBurstMode`
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
- **描述**: Enables a burst Mode that transmit multiple XCP Frames at once. The Burst Mode can only be enabled if Concatenation Mode is enabled.

########## 5. XcpPduMode

- **UUID**: `bb73f1d1-d077-4ae6-a8c2-d18bab4ef2e7`
- **参数名**: `XcpPduMode`
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
- **描述**: If this parameter is enabled an API is enabled that allows the application to delay transmission readyness of the transport layer. This is useful if transmission shall be prevented as long as the underlying bus system is not ready to prevent message loss.

######### STRING 类型参数

########## 1. XcpOnEthUserConfigFile

- **UUID**: `0f707868-1a7a-4d14-8c57-e7ee793c2cc8`
- **参数名**: `XcpOnEthUserConfigFile`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: A configuration file is generated by DaVinci Configurator Pro. If you want to overwrite settings in the generated configuration file, you can specify a path to a user defined configuration file.

The user defined configuration file will be included at the end of the generated file. Therefore definitions in the user defined configuration file can overwrite definitions in the generated configuration file.

The contents of the user defined configuration file is copied to the end of <Bsw>_Cfg.h.

####### 10. XcpEventChannel

**容器属性**:

- **UUID**: `da001bcb-8f20-41bc-a8f2-b2a687e04825`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `XcpEventChannel`
- **多重性**: [0..65535]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

Event channels configuration.

######## 参数配置

此容器包含 **7** 个参数：

######### INTEGER 类型参数

########## 1. XcpEventChannelMaxDaqList

- **UUID**: `6f0e56ec-73dd-4a5d-994c-b3dde39f33d0`
- **参数名**: `XcpEventChannelMaxDaqList`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `1`
- **取值范围**: [1..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Maximum amount of DAQ lists that are handled by this event channel.

########## 2. XcpEventChannelNumber

- **UUID**: `12df7372-3a82-489d-9eb5-b269646849e8`
- **参数名**: `XcpEventChannelNumber`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65534]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Index number of the event channel.

########## 3. XcpEventChannelPriority

- **UUID**: `1f307cc3-c766-492c-b25b-903e3450e45d`
- **参数名**: `XcpEventChannelPriority`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Priority of the event channel

Parameter not supported!

########## 4. XcpEventChannelTimeCycle

- **UUID**: `e9b29913-cc48-40b4-9d3b-27cca0aef5f3`
- **参数名**: `XcpEventChannelTimeCycle`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: The event channel time cycle indicates which sampling period is used to process this event channel. A value of 0 means 'Not cyclic'. The unit is defined by the parameter XcpEventChannelTimeUnit.

######### ENUMERATION 类型参数

########## 1. XcpEventChannelConsistency

- **UUID**: `0067b79b-879f-4fcc-8247-ef6a73d00613`
- **参数名**: `XcpEventChannelConsistency`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `ODT`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `ODT` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Type of consistency used by event channel

########## 2. XcpEventChannelTimeUnit

- **UUID**: `832823cb-ff01-448e-8e0c-3f42a4b32084`
- **参数名**: `XcpEventChannelTimeUnit`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `TIMESTAMP_UNIT_100MS` (来源: AUTOSAR_ECUC)
  - `TIMESTAMP_UNIT_100NS` (来源: AUTOSAR_ECUC)
  - `TIMESTAMP_UNIT_100PS` (来源: AUTOSAR_ECUC)
  - `TIMESTAMP_UNIT_100US` (来源: AUTOSAR_ECUC)
  - `TIMESTAMP_UNIT_10MS` (来源: AUTOSAR_ECUC)
  - `TIMESTAMP_UNIT_10NS` (来源: AUTOSAR_ECUC)
  - `TIMESTAMP_UNIT_10PS` (来源: AUTOSAR_ECUC)
  - `TIMESTAMP_UNIT_10US` (来源: AUTOSAR_ECUC)
  - `TIMESTAMP_UNIT_1MS` (来源: AUTOSAR_ECUC)
  - `TIMESTAMP_UNIT_1NS` (来源: AUTOSAR_ECUC)
  - `TIMESTAMP_UNIT_1PS` (来源: AUTOSAR_ECUC)
  - `TIMESTAMP_UNIT_1S` (来源: AUTOSAR_ECUC)
  - `TIMESTAMP_UNIT_1US` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This configuration parameter indicates the unit of the event channel time cycle.

########## 3. XcpEventChannelType

- **UUID**: `499044cd-17d2-4b22-b4ec-435e7f42ec65`
- **参数名**: `XcpEventChannelType`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `DAQ`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `DAQ` (来源: AUTOSAR_ECUC)
  - `DAQ_STIM` (来源: AUTOSAR_ECUC)
  - `STIM` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This configuration parameter indicates what kind of DAQ list can be allocated to this event channel:
DAQ: DAQ only
DAQ_STIM: DAQ and STIM List in one event
STIM: STIM only

######## 引用关系

此容器包含 **2** 个引用：

######### REFERENCE 类型引用

########## 1. XcpEventChannelTriggeredDaqListRef

- **UUID**: `3858b318-969f-4041-ac98-e8910e6b986d`
- **引用名**: `XcpEventChannelTriggeredDaqListRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `XcpDaqList`
- **完整路径**: `/AUTOSAR/EcucDefs/Xcp/XcpConfig/XcpDaqList`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: References all DAQ lists that are trigged by this event channel.

Parameter not supported!

########## 2. XcpEventChannelCoreRef

- **UUID**: `949d9f0c-d068-4c77-a0cf-2dc799aac3b3`
- **引用名**: `XcpEventChannelCoreRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `XcpCoreDefinition`
- **完整路径**: `/MICROSAR/Xcp/XcpConfig/XcpCoreDefinition`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This reference defines the associated Core configuration container in which context the Xcp_Event(EventChannel) is called.

####### 11. XcpRxPdu

**容器属性**:

- **UUID**: `899d9752-fc27-431e-8bd1-9d070fe74f37`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `XcpRxPdu`
- **多重性**: [0..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

Rx PDU description.

######## 参数配置

此容器包含 **3** 个参数：

######### INTEGER 类型参数

########## 1. XcpRxPduId

- **UUID**: `2cff12e2-fe3d-42fc-8470-d51300706240`
- **参数名**: `XcpRxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: ID of the PDU that will be received by the XCP module via a Xcp_<module>RxIndication.

######### BOOLEAN 类型参数

########## 1. XcpOnFrPduIsRuntimeConfigurable

- **UUID**: `1a576ed0-e03f-42d4-af7f-22dc2a4b5484`
- **参数名**: `XcpOnFrPduIsRuntimeConfigurable`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `true`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Selects whether the PDU type can be changed during runtime. This is done by the FLX_ASSIGN command and must be supported by the XCP Master.

This parameter is only relevant for FlexRay bus system.

######### ENUMERATION 类型参数

########## 1. XcpOnFrRxPduType

- **UUID**: `b88e419f-f4de-45d9-b748-d5bd1945d06d`
- **参数名**: `XcpOnFrRxPduType`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `Variable`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `Cmd`
  - `Stim`
  - `Variable`
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: XCP Rx PDU type (CMD, STIM) or Variable (type can be assigned during runtime). CMD is used for initial communication. At least one CMD PDU must be present. STIM is a fixed assignment, normally VARIABLE is used for STIM PDUs.

This parameter is only relevant for FlexRay bus system.

######## 引用关系

此容器包含 **2** 个引用：

######### REFERENCE 类型引用

########## 1. XcpRxPduRef

- **UUID**: `575392cd-9ed5-4cc0-9c73-e71b02fe652e`
- **引用名**: `XcpRxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the global PDU definition that identifies the PDU.

########## 2. XcpTxPduContRef

- **UUID**: `3175d513-394a-495a-89e3-064978275244`
- **引用名**: `XcpTxPduContRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `XcpTxPdu`
- **完整路径**: `/MICROSAR/Xcp/XcpConfig/XcpPdu/XcpTxPdu`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter references the Tx PDU used for messages in response to this Rx PDU. This parameter is only relevant for CAN and ETH configurations.

####### 12. XcpTxPdu

**容器属性**:

- **UUID**: `e60035ab-748f-42f4-8f33-aa5a10405716`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `XcpTxPdu`
- **多重性**: [0..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

Tx PDU description.

######## 参数配置

此容器包含 **3** 个参数：

######### INTEGER 类型参数

########## 1. XcpTxPduId

- **UUID**: `2a72766e-b938-441f-81a3-7b98896525a6`
- **参数名**: `XcpTxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The PDU identifier, which has to be used by the lower layer to identify the PDU during TxConfirmation or TriggerTransmit calls to the XCP module.

######### BOOLEAN 类型参数

########## 1. XcpOnFrPduIsRuntimeConfigurable

- **UUID**: `f2598532-bb7f-45dc-847f-b7661861c530`
- **参数名**: `XcpOnFrPduIsRuntimeConfigurable`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `true`
- **来源**: Vector Informatik
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Selects wether the PDU type can be changed during runtime.

This parameter is only relevant for FlexRay bus system.

######### ENUMERATION 类型参数

########## 1. XcpOnFrTxPduType

- **UUID**: `f4df4522-ee8b-408f-a2ab-9ebc8c8305bf`
- **参数名**: `XcpOnFrTxPduType`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `Variable`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `ResErr`
  - `EvServ`
  - `Daq`
  - `Variable`
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: XCP Tx PDU type (RES/ERR, EV/SERV or DAQ) or  Variable (type can be assigned during runtime). RES/ERR is used for initial communication. At least one RES/ERR must be present. DAQ and EV/SERV is a fixed assignment, normally VARIABLE is used for DAQ or EV/SERV PDUs.

This parameter is only relevant for FlexRay bus system.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. XcpTxPduRef

- **UUID**: `b154ce78-aa8c-45e2-897a-2500c2ececd2`
- **引用名**: `XcpTxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the global PDU definition that identifies the PDU.

####### 13. XcpCoreDefinition

**容器属性**:

- **UUID**: `224e4cda-f540-40de-adf9-207576132555`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `XcpCoreDefinition`
- **多重性**: [0..65535]
- **构建后可变**: false

**容器描述**:

Container contains all core specific configuration parameters.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. XcpSendQueueSize

- **UUID**: `f4b820c0-ac2f-4df5-bd17-641e87cfc8b1`
- **参数名**: `XcpSendQueueSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `256`
- **取值范围**: [32..4294967292]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: The size of the transmit queue for this Core in Bytes.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. XcpEcuCCoreDefinitionRef

- **UUID**: `ecb09130-4450-4c82-bd2a-ab5f38265bb9`
- **引用名**: `XcpEcuCCoreDefinitionRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `EcucCoreDefinition`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucHardware/EcucCoreDefinition`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: The reference to the EcuC core definition.

####### 14. XcpPdu

**容器属性**:

- **UUID**: `4b82fde9-6a3b-4024-ada1-43040c74c205`
- **容器类型**: CHOICE-CONTAINER
- **容器名称**: `XcpPdu`
- **多重性**: [2..infinite]
- **构建后可变**: true

**容器选择**:

- **XcpRxPdu**
  - UUID: `899d9752-fc27-431e-8bd1-9d070fe74f37`
  - 描述: Rx PDU description.
- **XcpTxPdu**
  - UUID: `e60035ab-748f-42f4-8f33-aa5a10405716`
  - 描述: Tx PDU description.

**容器描述**:

Description of the Rx and Tx PDUs used for XCP communication. XCP requires at least one Rx and one Tx PDU for Cmd/Res communication.
CAN: No additional PDUs must be defined. Delete redundant PDUs here and if necessary in the IF
FlexRay: Additional PDUs for DAQ/STIM can be defined
TcpIp: No additional PDUs must be defined. Delete redundant PDUs here and if necessary in the IF

##### 2. XcpDaqList

**容器属性**:

- **UUID**: `4a8f77c0-be02-4f67-9c28-98da711af256`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `XcpDaqList`
- **多重性**: [0..0]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container contains the configuration of the DAQs.

Container not supported!

###### 参数配置

此容器包含 **4** 个参数：

####### INTEGER 类型参数

######## 1. XcpDaqListNumber

- **UUID**: `1c8dad8a-3e30-4e52-856d-88919b37a518`
- **参数名**: `XcpDaqListNumber`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65534]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Index number of the DAQ list

######## 2. XcpMaxOdt

- **UUID**: `6d3c30f6-d714-488c-9913-b4cf7965bc8b`
- **参数名**: `XcpMaxOdt`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..252]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: MAX_ODT indicates the maximum amount of ODTs in this DAQ list
(STATIC configuration)

######## 3. XcpMaxOdtEntries

- **UUID**: `cc332f4a-1ca0-4f8b-a353-5b00030ece36`
- **参数名**: `XcpMaxOdtEntries`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter indicates the maximum amount of entries in an ODT of this DAQ list (STATIC configuration).

####### ENUMERATION 类型参数

######## 1. XcpDaqListType

- **UUID**: `9dca6965-806c-43cf-a923-dfed2c6ff2cf`
- **参数名**: `XcpDaqListType`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `DAQ` (来源: AUTOSAR_ECUC)
  - `DAQ_STIM` (来源: AUTOSAR_ECUC)
  - `STIM` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This indicates whether this DAQ list represents a DAQ or a STIM.

###### 配置容器

本模块包含 **3** 个配置容器：

####### 1. XcpDto

**容器属性**:

- **UUID**: `c68e6cf6-0119-4ca4-9f8b-8d62c33b78d0`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `XcpDto`
- **多重性**: [0..infinite]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container collects data transfer object specific parameters for the DAQ list.

Container not supported!

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. XcpDtoPid

- **UUID**: `4c003d10-593f-4f33-9ee2-720e4c05c4c2`
- **参数名**: `XcpDtoPid`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..251]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Packet identifier (PID) of the DTO that identifies the ODT the content of the DTO.

######## 引用关系

此容器包含 **1** 个引用：

######### CHOICE-REFERENCE 类型引用

########## 1. XcpDto2PduMapping

- **UUID**: `f24ad608-e696-41d1-b4d3-ea43f3b1c1ce`
- **引用名**: `XcpDto2PduMapping`
- **引用类型**: CHOICE-REFERENCE
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **目标引用列表**:
  - `/AUTOSAR/EcucDefs/Xcp/XcpConfig/XcpPdu/XcpRxPdu`
  - `/AUTOSAR/EcucDefs/Xcp/XcpConfig/XcpPdu/XcpTxPdu`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This reference specifies the mapping of the DTO to the PDUs from the lower-layer interfaces (CanIf, FrIf, SoAd and Cdd).
A reference to a XcpRxPdu is only feasible if the the DaqListType is DAQ_STIM.
A reference to a XcpTxPdu is only feasible if the DaqListType is DAQ.

####### 2. XcpOdt

**容器属性**:

- **UUID**: `7e9240c6-9ffb-44b2-9cc4-4903fcdb293d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `XcpOdt`
- **多重性**: [0..infinite]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container contains ODT-specific parameter for the DAQ list.

Container not supported!

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. XcpOdtEntryMaxSize

- **UUID**: `ac2c6e65-f40a-444d-827d-20209e06c132`
- **参数名**: `XcpOdtEntryMaxSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..254]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter indicates the upper limit for the size of the element described by an ODT entry. Depending on the DaqListType this ODT belongs to it describes the limit for a DAQ (MAX_ODT_ENTRY_SIZE_DAQ) or a STIM (MAX_ODT_ENTRY_SIZE_STIM).

########## 2. XcpOdtNumber

- **UUID**: `2dfda5c6-11b5-4d91-a5b0-2ef44421d49a`
- **参数名**: `XcpOdtNumber`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..251]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Index number of this ODT within the DAQ list.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. XcpOdt2DtoMapping

- **UUID**: `9d721f28-ecc6-43be-8670-cd0c131176de`
- **引用名**: `XcpOdt2DtoMapping`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `XcpDto`
- **完整路径**: `/AUTOSAR/EcucDefs/Xcp/XcpConfig/XcpDaqList/XcpDto`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This reference maps the ODT to the according DTO in which it will be transmitted.

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. XcpOdtEntry

**容器属性**:

- **UUID**: `88869fa2-bdba-4beb-93e3-e5b0a6b11955`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `XcpOdtEntry`
- **多重性**: [0..infinite]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container collects all configuration parameters that comprise an ODT entry.

Container not supported!

########## 参数配置

此容器包含 **3** 个参数：

########### INTEGER 类型参数

############ 1. XcpOdtEntryLength

- **UUID**: `8e0a56a5-24b0-49d4-a369-9ebc3811a8ab`
- **参数名**: `XcpOdtEntryLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Length of the referenced memory area that is referenced by the ODT entry.

############ 2. XcpOdtEntryNumber

- **UUID**: `0d7b3b2a-e689-448f-a78e-4efb45d12d97`
- **参数名**: `XcpOdtEntryNumber`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..254]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Index number of the ODT entry

########### LINKER-SYMBOL 类型参数

############ 1. XcpOdtEntryAddress

- **UUID**: `07530c73-f6b9-4ba5-b072-53f4d2f5f54c`
- **参数名**: `XcpOdtEntryAddress`
- **数据类型**: LINKER-SYMBOL
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Memory address that the ODT entry is referencing to.

####### 3. XcpOdtEntry

**容器属性**:

- **UUID**: `88869fa2-bdba-4beb-93e3-e5b0a6b11955`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `XcpOdtEntry`
- **多重性**: [0..infinite]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container collects all configuration parameters that comprise an ODT entry.

Container not supported!

######## 参数配置

此容器包含 **3** 个参数：

######### INTEGER 类型参数

########## 1. XcpOdtEntryLength

- **UUID**: `8e0a56a5-24b0-49d4-a369-9ebc3811a8ab`
- **参数名**: `XcpOdtEntryLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Length of the referenced memory area that is referenced by the ODT entry.

########## 2. XcpOdtEntryNumber

- **UUID**: `0d7b3b2a-e689-448f-a78e-4efb45d12d97`
- **参数名**: `XcpOdtEntryNumber`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..254]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Index number of the ODT entry

######### LINKER-SYMBOL 类型参数

########## 1. XcpOdtEntryAddress

- **UUID**: `07530c73-f6b9-4ba5-b072-53f4d2f5f54c`
- **参数名**: `XcpOdtEntryAddress`
- **数据类型**: LINKER-SYMBOL
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Memory address that the ODT entry is referencing to.

##### 3. XcpDto

**容器属性**:

- **UUID**: `c68e6cf6-0119-4ca4-9f8b-8d62c33b78d0`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `XcpDto`
- **多重性**: [0..infinite]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container collects data transfer object specific parameters for the DAQ list.

Container not supported!

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. XcpDtoPid

- **UUID**: `4c003d10-593f-4f33-9ee2-720e4c05c4c2`
- **参数名**: `XcpDtoPid`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..251]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Packet identifier (PID) of the DTO that identifies the ODT the content of the DTO.

###### 引用关系

此容器包含 **1** 个引用：

####### CHOICE-REFERENCE 类型引用

######## 1. XcpDto2PduMapping

- **UUID**: `f24ad608-e696-41d1-b4d3-ea43f3b1c1ce`
- **引用名**: `XcpDto2PduMapping`
- **引用类型**: CHOICE-REFERENCE
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **目标引用列表**:
  - `/AUTOSAR/EcucDefs/Xcp/XcpConfig/XcpPdu/XcpRxPdu`
  - `/AUTOSAR/EcucDefs/Xcp/XcpConfig/XcpPdu/XcpTxPdu`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This reference specifies the mapping of the DTO to the PDUs from the lower-layer interfaces (CanIf, FrIf, SoAd and Cdd).
A reference to a XcpRxPdu is only feasible if the the DaqListType is DAQ_STIM.
A reference to a XcpTxPdu is only feasible if the DaqListType is DAQ.

##### 4. XcpOdt

**容器属性**:

- **UUID**: `7e9240c6-9ffb-44b2-9cc4-4903fcdb293d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `XcpOdt`
- **多重性**: [0..infinite]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container contains ODT-specific parameter for the DAQ list.

Container not supported!

###### 参数配置

此容器包含 **2** 个参数：

####### INTEGER 类型参数

######## 1. XcpOdtEntryMaxSize

- **UUID**: `ac2c6e65-f40a-444d-827d-20209e06c132`
- **参数名**: `XcpOdtEntryMaxSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..254]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter indicates the upper limit for the size of the element described by an ODT entry. Depending on the DaqListType this ODT belongs to it describes the limit for a DAQ (MAX_ODT_ENTRY_SIZE_DAQ) or a STIM (MAX_ODT_ENTRY_SIZE_STIM).

######## 2. XcpOdtNumber

- **UUID**: `2dfda5c6-11b5-4d91-a5b0-2ef44421d49a`
- **参数名**: `XcpOdtNumber`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..251]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Index number of this ODT within the DAQ list.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. XcpOdt2DtoMapping

- **UUID**: `9d721f28-ecc6-43be-8670-cd0c131176de`
- **引用名**: `XcpOdt2DtoMapping`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `XcpDto`
- **完整路径**: `/AUTOSAR/EcucDefs/Xcp/XcpConfig/XcpDaqList/XcpDto`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This reference maps the ODT to the according DTO in which it will be transmitted.

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. XcpOdtEntry

**容器属性**:

- **UUID**: `88869fa2-bdba-4beb-93e3-e5b0a6b11955`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `XcpOdtEntry`
- **多重性**: [0..infinite]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container collects all configuration parameters that comprise an ODT entry.

Container not supported!

######## 参数配置

此容器包含 **3** 个参数：

######### INTEGER 类型参数

########## 1. XcpOdtEntryLength

- **UUID**: `8e0a56a5-24b0-49d4-a369-9ebc3811a8ab`
- **参数名**: `XcpOdtEntryLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Length of the referenced memory area that is referenced by the ODT entry.

########## 2. XcpOdtEntryNumber

- **UUID**: `0d7b3b2a-e689-448f-a78e-4efb45d12d97`
- **参数名**: `XcpOdtEntryNumber`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..254]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Index number of the ODT entry

######### LINKER-SYMBOL 类型参数

########## 1. XcpOdtEntryAddress

- **UUID**: `07530c73-f6b9-4ba5-b072-53f4d2f5f54c`
- **参数名**: `XcpOdtEntryAddress`
- **数据类型**: LINKER-SYMBOL
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Memory address that the ODT entry is referencing to.

##### 5. XcpOdtEntry

**容器属性**:

- **UUID**: `88869fa2-bdba-4beb-93e3-e5b0a6b11955`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `XcpOdtEntry`
- **多重性**: [0..infinite]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container collects all configuration parameters that comprise an ODT entry.

Container not supported!

###### 参数配置

此容器包含 **3** 个参数：

####### INTEGER 类型参数

######## 1. XcpOdtEntryLength

- **UUID**: `8e0a56a5-24b0-49d4-a369-9ebc3811a8ab`
- **参数名**: `XcpOdtEntryLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Length of the referenced memory area that is referenced by the ODT entry.

######## 2. XcpOdtEntryNumber

- **UUID**: `0d7b3b2a-e689-448f-a78e-4efb45d12d97`
- **参数名**: `XcpOdtEntryNumber`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..254]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Index number of the ODT entry

####### LINKER-SYMBOL 类型参数

######## 1. XcpOdtEntryAddress

- **UUID**: `07530c73-f6b9-4ba5-b072-53f4d2f5f54c`
- **参数名**: `XcpOdtEntryAddress`
- **数据类型**: LINKER-SYMBOL
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Memory address that the ODT entry is referencing to.

##### 6. XcpDemEventParameterRefs

**容器属性**:

- **UUID**: `22ee9576-ed4f-4b4d-a16c-a67fed622840`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `XcpDemEventParameterRefs`
- **多重性**: [0..0]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

Container for the references to DemEventParameter elements which shall be invoked using the API Dem_ReportErrorStatus API in case the corresponding error occurs. The EventId is taken from the referenced DemEventParameter's DemEventId value. The standardized errors are provided in the container and can be extended by vendor specific error references.

Container not supported.

###### 引用关系

此容器包含 **1** 个引用：

####### SYMBOLIC-NAME-REFERENCE 类型引用

######## 1. XCP_E_INIT_FAILED

- **UUID**: `df87ad8f-155f-4408-b0dd-7e7fd4beec2a`
- **引用名**: `XCP_E_INIT_FAILED`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `DemEventParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemConfigSet/DemEventParameter`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Reference to the DemEventParameter which shall be issued when the error "Initialization of XCP failed" has occured.

##### 7. XcpTransportLayer

**容器属性**:

- **UUID**: `fb7cefd7-49a1-4938-8b46-9c5c18bb5d53`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `XcpTransportLayer`
- **多重性**: [1..1]
- **构建后可变**: false

**容器描述**:

Container to configure the available Transport Layer.

###### 配置容器

本模块包含 **3** 个配置容器：

####### 1. XcpOnCan

**容器属性**:

- **UUID**: `7819baaf-d770-4466-9a83-0b6b83bf4cba`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `XcpOnCan`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container contains all parameter for the XcpOnCan Transport Layer.

######## 参数配置

此容器包含 **7** 个参数：

######### INTEGER 类型参数

########## 1. XcpOnCanMaxCto

- **UUID**: `df12328d-0f89-40e0-b128-c8ec0535dab1`
- **参数名**: `XcpOnCanMaxCto`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `8`
- **取值范围**: [8..64]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Maximum size of Command Transfer Objects (e.g. for polling)

########## 2. XcpOnCanMaxDto

- **UUID**: `c3c05064-a5ca-4f19-8605-a201ba09e281`
- **参数名**: `XcpOnCanMaxDto`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `8`
- **取值范围**: [8..64]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Maximum size of Data Transfer Objects (e.g. for DAQ)

########## 3. XcpOnCanConfirmationTimeout

- **UUID**: `b20df3f7-ddb3-4ae7-9134-2fe9a15f1a3b`
- **参数名**: `XcpOnCanConfirmationTimeout`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `10`
- **取值范围**: [2..65535]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter defines the number of MainFunction cycles until a Tx confirmation timeout is detected and the respective PDU buffer is reset.

######### BOOLEAN 类型参数

########## 1. XcpOnCanMultiConnectionProtection

- **UUID**: `34446795-9ab5-4ae2-a9dc-75ac9068d7dd`
- **参数名**: `XcpOnCanMultiConnectionProtection`
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
- **描述**: Prevents a connection from a second XCP Master on a different CAN channel, when the first XCP Master has already established a connection.

########## 2. XcpOnCanVariableDlc

- **UUID**: `371bc189-a6f9-4662-848b-047e8b16d604`
- **参数名**: `XcpOnCanVariableDlc`
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
- **描述**: Allow CAN frames with a variable length. If disabled the frames have always the length of the PDU, which can be e.g. 8 Bytes on CAN or 64 Bytes on CAN-FD.

########## 3. XcpPduMode

- **UUID**: `77e1be04-e5c4-43ab-822f-8c55511fe12e`
- **参数名**: `XcpPduMode`
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
- **描述**: If this parameter is enabled an API is enabled that allows the application to delay transmission readyness of the transport layer. This is useful if transmission shall be prevented as long as the underlying bus system is not ready to prevent message loss.

######### STRING 类型参数

########## 1. XcpOnCanUserConfigFile

- **UUID**: `ce2e9365-2bee-4b1f-994c-df81836d92be`
- **参数名**: `XcpOnCanUserConfigFile`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: A configuration file is generated by DaVinci Configurator Pro. If you want to overwrite settings in the generated configuration file, you can specify a path to a user defined configuration file.

The user defined configuration file will be included at the end of the generated file. Therefore definitions in the user defined configuration file can overwrite definitions in the generated configuration file.

The contents of the user defined configuration file is copied to the end of CanXcp_Cfg.h.

####### 2. XcpOnFr

**容器属性**:

- **UUID**: `72ed4be2-d56e-40d5-94f4-7976d8104a9e`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `XcpOnFr`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container contains all parameter for the XcpOnFr Transport Layer.

######## 参数配置

此容器包含 **13** 个参数：

######### INTEGER 类型参数

########## 1. XcpOnFrMaxCto

- **UUID**: `d8f29ae6-f107-4638-982f-51663efd762e`
- **参数名**: `XcpOnFrMaxCto`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `12`
- **取值范围**: [12..254]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter defines the maximum length of Command Transfer Objects (CTO) in bytes. For FlexRay this parameter must be at least 12 and less than the maximum length of the PDU or Link-Layer frame.

########## 2. XcpOnFrMaxDto

- **UUID**: `0c1e0c6b-60ca-4b61-bbbc-756fdf37a81f`
- **参数名**: `XcpOnFrMaxDto`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `12`
- **取值范围**: [12..254]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter defines the maximum length of Data Transfer Objects (DTO). For FlexRay this parameter must be at least 12 and less than the maximum length of the PDU or Link-Layer frame.

########## 3. XcpOnFrConfirmationTimeout

- **UUID**: `0e44a290-e9d1-4af5-ba99-231c7f026c4d`
- **参数名**: `XcpOnFrConfirmationTimeout`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `8`
- **取值范围**: [2..65535]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter defines the number of MainFunction cycles until a Tx confirmation timeout is detected and the respective PDU buffer is reset.

########## 4. XcpOnFrReadCCConfigExtAddr

- **UUID**: `d001f26f-5c7f-4d44-8afe-8f6ac8445c75`
- **参数名**: `XcpOnFrReadCCConfigExtAddr`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `253`
- **取值范围**: [0..255]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: The "Virtual FlexRay Parameters" are accessible with this address extension.

########## 5. XcpOnFrNodeAddress

- **UUID**: `07632362-0e13-43bc-9d2a-6a99d8cae17b`
- **参数名**: `XcpOnFrNodeAddress`
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
- **描述**: This unique node address identifies the XCP slave within a network. This address is normally defined by the system designer and may be the same address as used for the Network Management Node ID.

########## 6. XcpOnFrMaxPDU

- **UUID**: `6b7879db-706b-4077-9b95-e940c64ebaab`
- **参数名**: `XcpOnFrMaxPDU`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `14`
- **取值范围**: [12..254]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter defines the maximum length of PDUs. For FlexRay this parameter must be at least 14 and higher than Max_CTO and Max_DTO.

######### BOOLEAN 类型参数

########## 1. XcpOnFrReadCCConfig

- **UUID**: `261a8ab7-7534-4f39-8083-2c78e1e21a0d`
- **参数名**: `XcpOnFrReadCCConfig`
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
- **描述**: If the "Virtual FlexRay Parameters" feature is enabled, the FlexRay parameters / Communication Controller Config can be read out in a platform independent way. They will be provided as virtual measurement values that can be read at fixed memory locations.

########## 2. XcpOnFrSequenceCounter

- **UUID**: `a10bc529-3139-445f-bf4f-336b5a8f619c`
- **参数名**: `XcpOnFrSequenceCounter`
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
- **描述**: The Sequence Counter is used to detect missing frames as well as to rearrange the ordering of frames if XCP is used asynchronously to the bus, or in the non guaranteed dynamic area of the cycle. If you can not guarantee correct ordering then activate this option. If you are uncertain, then activate this option.

########## 3. XcpOnFrFrameConcatenation

- **UUID**: `687bf5da-45da-4ba8-9ed9-a6fef5b8bc68`
- **参数名**: `XcpOnFrFrameConcatenation`
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
- **描述**: With this attribute you can enable the concatenation of multiple XCP frames into one Protocol Data Unit (PDU). This is useful if your sampling frequency is higher than the FlexRay Cycle, i.e. you call Xcp_Event in a 1ms cycle while you FLexRay cycle is 5ms.

########## 4. XcpOnFrOptimizedCopy

- **UUID**: `c9c9b975-e36a-4e9b-ba5f-605b4caf307a`
- **参数名**: `XcpOnFrOptimizedCopy`
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
- **描述**: If enabled a optimized copy routine is used within the FrXcp. This will improve execution time considerably but requires, on some platforms, certain alignment requirements, e.g. the PDUs must be aligned on a 32bit address within the FlexRay frame.
In most XCP use cases this option can be enabled. If a trap occurs, disable this option.

######### STRING 类型参数

########## 1. XcpOnFrUserConfigFile

- **UUID**: `e5d769da-ea50-4a78-9b82-5b9774a79ca2`
- **参数名**: `XcpOnFrUserConfigFile`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: A configuration file is generated by DaVinci Configurator Pro. If you want to overwrite settings in the generated configuration file, you can specify a path to a user defined configuration file.

The user defined configuration file will be included at the end of the generated file. Therefore definitions in the user defined configuration file can overwrite definitions in the generated configuration file.

The contents of the user defined configuration file is copied to the end of FrXcp_Cfg.h.

######### ENUMERATION 类型参数

########## 1. XcpOnFrFrameAlignment

- **UUID**: `329b0e95-73e5-45a5-8c0a-e46ce59396d1`
- **参数名**: `XcpOnFrFrameAlignment`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `Align8Bit`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `Align8Bit`
  - `Align16Bit`
  - `Align32Bit`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter determines the Alignment of XCP frames within a FlexRay frame. This parameter must be selected according to performance and architectural needs. For details please read the Technical Reference and the ASAM Xcp On FlexRay specification.

########## 2. XcpOnFrTransmissionMode

- **UUID**: `a02a78ad-b278-4a76-b4bb-ac7d3eb23dda`
- **参数名**: `XcpOnFrTransmissionMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `Decoupled`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `Decoupled`
  - `Immediate`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: It is possible to use the XCP either in Immediate or Decoupled Mode. Immediate Mode requires less resources but the FlexRay XCP MainFunctions must be used synchronously to the FlexRay bus. They must be placed such that the their execution finished before actual transmission on the bus happens.

####### 3. XcpOnEth

**容器属性**:

- **UUID**: `1535b67e-580c-43f7-9b76-ae847c503e31`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `XcpOnEth`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container contains all parameter for the XcpOnEth Transport Layer.

######## 参数配置

此容器包含 **10** 个参数：

######### INTEGER 类型参数

########## 1. XcpOnEthMaxCto

- **UUID**: `ff82d678-622e-4ca9-82b4-0e1d602ddee7`
- **参数名**: `XcpOnEthMaxCto`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `255`
- **取值范围**: [8..255]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Maximum size of Command Transfer Objects (e.g. for polling)

########## 2. XcpOnEthMaxDto

- **UUID**: `e0affdbd-5d30-4436-a642-cf5d47392506`
- **参数名**: `XcpOnEthMaxDto`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `255`
- **取值范围**: [8..1448]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Maximum size of Data Transfer Objects (e.g. for DAQ). Maximum size depending on protocol on lower layers, e.g. IPV4 or IPV6 or usage of VLAN.

########## 3. XcpOnEthConfirmationTimeout

- **UUID**: `a5bc5b9c-d60b-41de-8c14-9f43190a0e82`
- **参数名**: `XcpOnEthConfirmationTimeout`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `10`
- **取值范围**: [2..65535]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter defines the number of MainFunction cycles until a Tx confirmation timeout is detected and the respective PDU buffer is reset.

########## 4. XcpBurstSize

- **UUID**: `2738647c-6943-4131-9e84-0531fbb691e8`
- **参数名**: `XcpBurstSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `10`
- **取值范围**: [2..65535]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Defines the number of messages that are sent in a burst. This parameter is only relevant if the parameter Burst Mode is enabled.

######### BOOLEAN 类型参数

########## 1. XcpOnEthMultiConnectionProtection

- **UUID**: `dc91dc93-0427-45b7-b197-5cb8bf29b06a`
- **参数名**: `XcpOnEthMultiConnectionProtection`
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
- **描述**: Prevents a connection from a second XCP Master on a different channel, when the first XCP Master has already established a connection.

########## 2. XcpOnEthOptimizedCopy

- **UUID**: `38511283-4ccb-4d8b-9434-9adf10ceeab2`
- **参数名**: `XcpOnEthOptimizedCopy`
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
- **描述**: If enabled a optimized copy routine is used within the TcpIpXcp. This will improve execution time considerably but requires, on some platforms, certain alignment requirements, e.g. the PDUs must be aligned on a 32bit address within the Ethernet frame.
In most XCP use cases this option can be enabled. If a trap occurs, disable this option.

########## 3. XcpOnEthConcatenationMode

- **UUID**: `e7c4786f-071e-498c-8891-60763f280e3f`
- **参数名**: `XcpOnEthConcatenationMode`
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
- **描述**: If this option is enabled the TcpIpXcp concatenates multiple XCP messages in one Ethernet PDU. This is useful if you use a measurement cycle that is faster than PDUs can be sent on the bus. The concatenation is performed in the MainFunction, therefore the transmission cycle is limited to TcpIpXcp_MainFunction cycles.

########## 4. XcpOnEthBurstMode

- **UUID**: `bf8c7511-e127-4dd7-914e-1eea7549fd1a`
- **参数名**: `XcpOnEthBurstMode`
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
- **描述**: Enables a burst Mode that transmit multiple XCP Frames at once. The Burst Mode can only be enabled if Concatenation Mode is enabled.

########## 5. XcpPduMode

- **UUID**: `bb73f1d1-d077-4ae6-a8c2-d18bab4ef2e7`
- **参数名**: `XcpPduMode`
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
- **描述**: If this parameter is enabled an API is enabled that allows the application to delay transmission readyness of the transport layer. This is useful if transmission shall be prevented as long as the underlying bus system is not ready to prevent message loss.

######### STRING 类型参数

########## 1. XcpOnEthUserConfigFile

- **UUID**: `0f707868-1a7a-4d14-8c57-e7ee793c2cc8`
- **参数名**: `XcpOnEthUserConfigFile`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: A configuration file is generated by DaVinci Configurator Pro. If you want to overwrite settings in the generated configuration file, you can specify a path to a user defined configuration file.

The user defined configuration file will be included at the end of the generated file. Therefore definitions in the user defined configuration file can overwrite definitions in the generated configuration file.

The contents of the user defined configuration file is copied to the end of <Bsw>_Cfg.h.

##### 8. XcpOnCan

**容器属性**:

- **UUID**: `7819baaf-d770-4466-9a83-0b6b83bf4cba`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `XcpOnCan`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container contains all parameter for the XcpOnCan Transport Layer.

###### 参数配置

此容器包含 **7** 个参数：

####### INTEGER 类型参数

######## 1. XcpOnCanMaxCto

- **UUID**: `df12328d-0f89-40e0-b128-c8ec0535dab1`
- **参数名**: `XcpOnCanMaxCto`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `8`
- **取值范围**: [8..64]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Maximum size of Command Transfer Objects (e.g. for polling)

######## 2. XcpOnCanMaxDto

- **UUID**: `c3c05064-a5ca-4f19-8605-a201ba09e281`
- **参数名**: `XcpOnCanMaxDto`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `8`
- **取值范围**: [8..64]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Maximum size of Data Transfer Objects (e.g. for DAQ)

######## 3. XcpOnCanConfirmationTimeout

- **UUID**: `b20df3f7-ddb3-4ae7-9134-2fe9a15f1a3b`
- **参数名**: `XcpOnCanConfirmationTimeout`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `10`
- **取值范围**: [2..65535]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter defines the number of MainFunction cycles until a Tx confirmation timeout is detected and the respective PDU buffer is reset.

####### BOOLEAN 类型参数

######## 1. XcpOnCanMultiConnectionProtection

- **UUID**: `34446795-9ab5-4ae2-a9dc-75ac9068d7dd`
- **参数名**: `XcpOnCanMultiConnectionProtection`
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
- **描述**: Prevents a connection from a second XCP Master on a different CAN channel, when the first XCP Master has already established a connection.

######## 2. XcpOnCanVariableDlc

- **UUID**: `371bc189-a6f9-4662-848b-047e8b16d604`
- **参数名**: `XcpOnCanVariableDlc`
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
- **描述**: Allow CAN frames with a variable length. If disabled the frames have always the length of the PDU, which can be e.g. 8 Bytes on CAN or 64 Bytes on CAN-FD.

######## 3. XcpPduMode

- **UUID**: `77e1be04-e5c4-43ab-822f-8c55511fe12e`
- **参数名**: `XcpPduMode`
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
- **描述**: If this parameter is enabled an API is enabled that allows the application to delay transmission readyness of the transport layer. This is useful if transmission shall be prevented as long as the underlying bus system is not ready to prevent message loss.

####### STRING 类型参数

######## 1. XcpOnCanUserConfigFile

- **UUID**: `ce2e9365-2bee-4b1f-994c-df81836d92be`
- **参数名**: `XcpOnCanUserConfigFile`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: A configuration file is generated by DaVinci Configurator Pro. If you want to overwrite settings in the generated configuration file, you can specify a path to a user defined configuration file.

The user defined configuration file will be included at the end of the generated file. Therefore definitions in the user defined configuration file can overwrite definitions in the generated configuration file.

The contents of the user defined configuration file is copied to the end of CanXcp_Cfg.h.

##### 9. XcpOnFr

**容器属性**:

- **UUID**: `72ed4be2-d56e-40d5-94f4-7976d8104a9e`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `XcpOnFr`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container contains all parameter for the XcpOnFr Transport Layer.

###### 参数配置

此容器包含 **13** 个参数：

####### INTEGER 类型参数

######## 1. XcpOnFrMaxCto

- **UUID**: `d8f29ae6-f107-4638-982f-51663efd762e`
- **参数名**: `XcpOnFrMaxCto`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `12`
- **取值范围**: [12..254]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter defines the maximum length of Command Transfer Objects (CTO) in bytes. For FlexRay this parameter must be at least 12 and less than the maximum length of the PDU or Link-Layer frame.

######## 2. XcpOnFrMaxDto

- **UUID**: `0c1e0c6b-60ca-4b61-bbbc-756fdf37a81f`
- **参数名**: `XcpOnFrMaxDto`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `12`
- **取值范围**: [12..254]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter defines the maximum length of Data Transfer Objects (DTO). For FlexRay this parameter must be at least 12 and less than the maximum length of the PDU or Link-Layer frame.

######## 3. XcpOnFrConfirmationTimeout

- **UUID**: `0e44a290-e9d1-4af5-ba99-231c7f026c4d`
- **参数名**: `XcpOnFrConfirmationTimeout`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `8`
- **取值范围**: [2..65535]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter defines the number of MainFunction cycles until a Tx confirmation timeout is detected and the respective PDU buffer is reset.

######## 4. XcpOnFrReadCCConfigExtAddr

- **UUID**: `d001f26f-5c7f-4d44-8afe-8f6ac8445c75`
- **参数名**: `XcpOnFrReadCCConfigExtAddr`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `253`
- **取值范围**: [0..255]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: The "Virtual FlexRay Parameters" are accessible with this address extension.

######## 5. XcpOnFrNodeAddress

- **UUID**: `07632362-0e13-43bc-9d2a-6a99d8cae17b`
- **参数名**: `XcpOnFrNodeAddress`
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
- **描述**: This unique node address identifies the XCP slave within a network. This address is normally defined by the system designer and may be the same address as used for the Network Management Node ID.

######## 6. XcpOnFrMaxPDU

- **UUID**: `6b7879db-706b-4077-9b95-e940c64ebaab`
- **参数名**: `XcpOnFrMaxPDU`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `14`
- **取值范围**: [12..254]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter defines the maximum length of PDUs. For FlexRay this parameter must be at least 14 and higher than Max_CTO and Max_DTO.

####### BOOLEAN 类型参数

######## 1. XcpOnFrReadCCConfig

- **UUID**: `261a8ab7-7534-4f39-8083-2c78e1e21a0d`
- **参数名**: `XcpOnFrReadCCConfig`
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
- **描述**: If the "Virtual FlexRay Parameters" feature is enabled, the FlexRay parameters / Communication Controller Config can be read out in a platform independent way. They will be provided as virtual measurement values that can be read at fixed memory locations.

######## 2. XcpOnFrSequenceCounter

- **UUID**: `a10bc529-3139-445f-bf4f-336b5a8f619c`
- **参数名**: `XcpOnFrSequenceCounter`
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
- **描述**: The Sequence Counter is used to detect missing frames as well as to rearrange the ordering of frames if XCP is used asynchronously to the bus, or in the non guaranteed dynamic area of the cycle. If you can not guarantee correct ordering then activate this option. If you are uncertain, then activate this option.

######## 3. XcpOnFrFrameConcatenation

- **UUID**: `687bf5da-45da-4ba8-9ed9-a6fef5b8bc68`
- **参数名**: `XcpOnFrFrameConcatenation`
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
- **描述**: With this attribute you can enable the concatenation of multiple XCP frames into one Protocol Data Unit (PDU). This is useful if your sampling frequency is higher than the FlexRay Cycle, i.e. you call Xcp_Event in a 1ms cycle while you FLexRay cycle is 5ms.

######## 4. XcpOnFrOptimizedCopy

- **UUID**: `c9c9b975-e36a-4e9b-ba5f-605b4caf307a`
- **参数名**: `XcpOnFrOptimizedCopy`
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
- **描述**: If enabled a optimized copy routine is used within the FrXcp. This will improve execution time considerably but requires, on some platforms, certain alignment requirements, e.g. the PDUs must be aligned on a 32bit address within the FlexRay frame.
In most XCP use cases this option can be enabled. If a trap occurs, disable this option.

####### STRING 类型参数

######## 1. XcpOnFrUserConfigFile

- **UUID**: `e5d769da-ea50-4a78-9b82-5b9774a79ca2`
- **参数名**: `XcpOnFrUserConfigFile`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: A configuration file is generated by DaVinci Configurator Pro. If you want to overwrite settings in the generated configuration file, you can specify a path to a user defined configuration file.

The user defined configuration file will be included at the end of the generated file. Therefore definitions in the user defined configuration file can overwrite definitions in the generated configuration file.

The contents of the user defined configuration file is copied to the end of FrXcp_Cfg.h.

####### ENUMERATION 类型参数

######## 1. XcpOnFrFrameAlignment

- **UUID**: `329b0e95-73e5-45a5-8c0a-e46ce59396d1`
- **参数名**: `XcpOnFrFrameAlignment`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `Align8Bit`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `Align8Bit`
  - `Align16Bit`
  - `Align32Bit`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter determines the Alignment of XCP frames within a FlexRay frame. This parameter must be selected according to performance and architectural needs. For details please read the Technical Reference and the ASAM Xcp On FlexRay specification.

######## 2. XcpOnFrTransmissionMode

- **UUID**: `a02a78ad-b278-4a76-b4bb-ac7d3eb23dda`
- **参数名**: `XcpOnFrTransmissionMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `Decoupled`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `Decoupled`
  - `Immediate`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: It is possible to use the XCP either in Immediate or Decoupled Mode. Immediate Mode requires less resources but the FlexRay XCP MainFunctions must be used synchronously to the FlexRay bus. They must be placed such that the their execution finished before actual transmission on the bus happens.

##### 10. XcpOnEth

**容器属性**:

- **UUID**: `1535b67e-580c-43f7-9b76-ae847c503e31`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `XcpOnEth`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container contains all parameter for the XcpOnEth Transport Layer.

###### 参数配置

此容器包含 **10** 个参数：

####### INTEGER 类型参数

######## 1. XcpOnEthMaxCto

- **UUID**: `ff82d678-622e-4ca9-82b4-0e1d602ddee7`
- **参数名**: `XcpOnEthMaxCto`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `255`
- **取值范围**: [8..255]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Maximum size of Command Transfer Objects (e.g. for polling)

######## 2. XcpOnEthMaxDto

- **UUID**: `e0affdbd-5d30-4436-a642-cf5d47392506`
- **参数名**: `XcpOnEthMaxDto`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `255`
- **取值范围**: [8..1448]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Maximum size of Data Transfer Objects (e.g. for DAQ). Maximum size depending on protocol on lower layers, e.g. IPV4 or IPV6 or usage of VLAN.

######## 3. XcpOnEthConfirmationTimeout

- **UUID**: `a5bc5b9c-d60b-41de-8c14-9f43190a0e82`
- **参数名**: `XcpOnEthConfirmationTimeout`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `10`
- **取值范围**: [2..65535]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter defines the number of MainFunction cycles until a Tx confirmation timeout is detected and the respective PDU buffer is reset.

######## 4. XcpBurstSize

- **UUID**: `2738647c-6943-4131-9e84-0531fbb691e8`
- **参数名**: `XcpBurstSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `10`
- **取值范围**: [2..65535]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Defines the number of messages that are sent in a burst. This parameter is only relevant if the parameter Burst Mode is enabled.

####### BOOLEAN 类型参数

######## 1. XcpOnEthMultiConnectionProtection

- **UUID**: `dc91dc93-0427-45b7-b197-5cb8bf29b06a`
- **参数名**: `XcpOnEthMultiConnectionProtection`
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
- **描述**: Prevents a connection from a second XCP Master on a different channel, when the first XCP Master has already established a connection.

######## 2. XcpOnEthOptimizedCopy

- **UUID**: `38511283-4ccb-4d8b-9434-9adf10ceeab2`
- **参数名**: `XcpOnEthOptimizedCopy`
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
- **描述**: If enabled a optimized copy routine is used within the TcpIpXcp. This will improve execution time considerably but requires, on some platforms, certain alignment requirements, e.g. the PDUs must be aligned on a 32bit address within the Ethernet frame.
In most XCP use cases this option can be enabled. If a trap occurs, disable this option.

######## 3. XcpOnEthConcatenationMode

- **UUID**: `e7c4786f-071e-498c-8891-60763f280e3f`
- **参数名**: `XcpOnEthConcatenationMode`
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
- **描述**: If this option is enabled the TcpIpXcp concatenates multiple XCP messages in one Ethernet PDU. This is useful if you use a measurement cycle that is faster than PDUs can be sent on the bus. The concatenation is performed in the MainFunction, therefore the transmission cycle is limited to TcpIpXcp_MainFunction cycles.

######## 4. XcpOnEthBurstMode

- **UUID**: `bf8c7511-e127-4dd7-914e-1eea7549fd1a`
- **参数名**: `XcpOnEthBurstMode`
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
- **描述**: Enables a burst Mode that transmit multiple XCP Frames at once. The Burst Mode can only be enabled if Concatenation Mode is enabled.

######## 5. XcpPduMode

- **UUID**: `bb73f1d1-d077-4ae6-a8c2-d18bab4ef2e7`
- **参数名**: `XcpPduMode`
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
- **描述**: If this parameter is enabled an API is enabled that allows the application to delay transmission readyness of the transport layer. This is useful if transmission shall be prevented as long as the underlying bus system is not ready to prevent message loss.

####### STRING 类型参数

######## 1. XcpOnEthUserConfigFile

- **UUID**: `0f707868-1a7a-4d14-8c57-e7ee793c2cc8`
- **参数名**: `XcpOnEthUserConfigFile`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: A configuration file is generated by DaVinci Configurator Pro. If you want to overwrite settings in the generated configuration file, you can specify a path to a user defined configuration file.

The user defined configuration file will be included at the end of the generated file. Therefore definitions in the user defined configuration file can overwrite definitions in the generated configuration file.

The contents of the user defined configuration file is copied to the end of <Bsw>_Cfg.h.

##### 11. XcpEventChannel

**容器属性**:

- **UUID**: `da001bcb-8f20-41bc-a8f2-b2a687e04825`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `XcpEventChannel`
- **多重性**: [0..65535]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

Event channels configuration.

###### 参数配置

此容器包含 **7** 个参数：

####### INTEGER 类型参数

######## 1. XcpEventChannelMaxDaqList

- **UUID**: `6f0e56ec-73dd-4a5d-994c-b3dde39f33d0`
- **参数名**: `XcpEventChannelMaxDaqList`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `1`
- **取值范围**: [1..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Maximum amount of DAQ lists that are handled by this event channel.

######## 2. XcpEventChannelNumber

- **UUID**: `12df7372-3a82-489d-9eb5-b269646849e8`
- **参数名**: `XcpEventChannelNumber`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65534]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Index number of the event channel.

######## 3. XcpEventChannelPriority

- **UUID**: `1f307cc3-c766-492c-b25b-903e3450e45d`
- **参数名**: `XcpEventChannelPriority`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Priority of the event channel

Parameter not supported!

######## 4. XcpEventChannelTimeCycle

- **UUID**: `e9b29913-cc48-40b4-9d3b-27cca0aef5f3`
- **参数名**: `XcpEventChannelTimeCycle`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: The event channel time cycle indicates which sampling period is used to process this event channel. A value of 0 means 'Not cyclic'. The unit is defined by the parameter XcpEventChannelTimeUnit.

####### ENUMERATION 类型参数

######## 1. XcpEventChannelConsistency

- **UUID**: `0067b79b-879f-4fcc-8247-ef6a73d00613`
- **参数名**: `XcpEventChannelConsistency`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `ODT`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `ODT` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Type of consistency used by event channel

######## 2. XcpEventChannelTimeUnit

- **UUID**: `832823cb-ff01-448e-8e0c-3f42a4b32084`
- **参数名**: `XcpEventChannelTimeUnit`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `TIMESTAMP_UNIT_100MS` (来源: AUTOSAR_ECUC)
  - `TIMESTAMP_UNIT_100NS` (来源: AUTOSAR_ECUC)
  - `TIMESTAMP_UNIT_100PS` (来源: AUTOSAR_ECUC)
  - `TIMESTAMP_UNIT_100US` (来源: AUTOSAR_ECUC)
  - `TIMESTAMP_UNIT_10MS` (来源: AUTOSAR_ECUC)
  - `TIMESTAMP_UNIT_10NS` (来源: AUTOSAR_ECUC)
  - `TIMESTAMP_UNIT_10PS` (来源: AUTOSAR_ECUC)
  - `TIMESTAMP_UNIT_10US` (来源: AUTOSAR_ECUC)
  - `TIMESTAMP_UNIT_1MS` (来源: AUTOSAR_ECUC)
  - `TIMESTAMP_UNIT_1NS` (来源: AUTOSAR_ECUC)
  - `TIMESTAMP_UNIT_1PS` (来源: AUTOSAR_ECUC)
  - `TIMESTAMP_UNIT_1S` (来源: AUTOSAR_ECUC)
  - `TIMESTAMP_UNIT_1US` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This configuration parameter indicates the unit of the event channel time cycle.

######## 3. XcpEventChannelType

- **UUID**: `499044cd-17d2-4b22-b4ec-435e7f42ec65`
- **参数名**: `XcpEventChannelType`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `DAQ`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `DAQ` (来源: AUTOSAR_ECUC)
  - `DAQ_STIM` (来源: AUTOSAR_ECUC)
  - `STIM` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This configuration parameter indicates what kind of DAQ list can be allocated to this event channel:
DAQ: DAQ only
DAQ_STIM: DAQ and STIM List in one event
STIM: STIM only

###### 引用关系

此容器包含 **2** 个引用：

####### REFERENCE 类型引用

######## 1. XcpEventChannelTriggeredDaqListRef

- **UUID**: `3858b318-969f-4041-ac98-e8910e6b986d`
- **引用名**: `XcpEventChannelTriggeredDaqListRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `XcpDaqList`
- **完整路径**: `/AUTOSAR/EcucDefs/Xcp/XcpConfig/XcpDaqList`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: References all DAQ lists that are trigged by this event channel.

Parameter not supported!

######## 2. XcpEventChannelCoreRef

- **UUID**: `949d9f0c-d068-4c77-a0cf-2dc799aac3b3`
- **引用名**: `XcpEventChannelCoreRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `XcpCoreDefinition`
- **完整路径**: `/MICROSAR/Xcp/XcpConfig/XcpCoreDefinition`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This reference defines the associated Core configuration container in which context the Xcp_Event(EventChannel) is called.

##### 12. XcpRxPdu

**容器属性**:

- **UUID**: `899d9752-fc27-431e-8bd1-9d070fe74f37`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `XcpRxPdu`
- **多重性**: [0..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

Rx PDU description.

###### 参数配置

此容器包含 **3** 个参数：

####### INTEGER 类型参数

######## 1. XcpRxPduId

- **UUID**: `2cff12e2-fe3d-42fc-8470-d51300706240`
- **参数名**: `XcpRxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: ID of the PDU that will be received by the XCP module via a Xcp_<module>RxIndication.

####### BOOLEAN 类型参数

######## 1. XcpOnFrPduIsRuntimeConfigurable

- **UUID**: `1a576ed0-e03f-42d4-af7f-22dc2a4b5484`
- **参数名**: `XcpOnFrPduIsRuntimeConfigurable`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `true`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Selects whether the PDU type can be changed during runtime. This is done by the FLX_ASSIGN command and must be supported by the XCP Master.

This parameter is only relevant for FlexRay bus system.

####### ENUMERATION 类型参数

######## 1. XcpOnFrRxPduType

- **UUID**: `b88e419f-f4de-45d9-b748-d5bd1945d06d`
- **参数名**: `XcpOnFrRxPduType`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `Variable`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `Cmd`
  - `Stim`
  - `Variable`
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: XCP Rx PDU type (CMD, STIM) or Variable (type can be assigned during runtime). CMD is used for initial communication. At least one CMD PDU must be present. STIM is a fixed assignment, normally VARIABLE is used for STIM PDUs.

This parameter is only relevant for FlexRay bus system.

###### 引用关系

此容器包含 **2** 个引用：

####### REFERENCE 类型引用

######## 1. XcpRxPduRef

- **UUID**: `575392cd-9ed5-4cc0-9c73-e71b02fe652e`
- **引用名**: `XcpRxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the global PDU definition that identifies the PDU.

######## 2. XcpTxPduContRef

- **UUID**: `3175d513-394a-495a-89e3-064978275244`
- **引用名**: `XcpTxPduContRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `XcpTxPdu`
- **完整路径**: `/MICROSAR/Xcp/XcpConfig/XcpPdu/XcpTxPdu`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter references the Tx PDU used for messages in response to this Rx PDU. This parameter is only relevant for CAN and ETH configurations.

##### 13. XcpTxPdu

**容器属性**:

- **UUID**: `e60035ab-748f-42f4-8f33-aa5a10405716`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `XcpTxPdu`
- **多重性**: [0..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

Tx PDU description.

###### 参数配置

此容器包含 **3** 个参数：

####### INTEGER 类型参数

######## 1. XcpTxPduId

- **UUID**: `2a72766e-b938-441f-81a3-7b98896525a6`
- **参数名**: `XcpTxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The PDU identifier, which has to be used by the lower layer to identify the PDU during TxConfirmation or TriggerTransmit calls to the XCP module.

####### BOOLEAN 类型参数

######## 1. XcpOnFrPduIsRuntimeConfigurable

- **UUID**: `f2598532-bb7f-45dc-847f-b7661861c530`
- **参数名**: `XcpOnFrPduIsRuntimeConfigurable`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `true`
- **来源**: Vector Informatik
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Selects wether the PDU type can be changed during runtime.

This parameter is only relevant for FlexRay bus system.

####### ENUMERATION 类型参数

######## 1. XcpOnFrTxPduType

- **UUID**: `f4df4522-ee8b-408f-a2ab-9ebc8c8305bf`
- **参数名**: `XcpOnFrTxPduType`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `Variable`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `ResErr`
  - `EvServ`
  - `Daq`
  - `Variable`
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: XCP Tx PDU type (RES/ERR, EV/SERV or DAQ) or  Variable (type can be assigned during runtime). RES/ERR is used for initial communication. At least one RES/ERR must be present. DAQ and EV/SERV is a fixed assignment, normally VARIABLE is used for DAQ or EV/SERV PDUs.

This parameter is only relevant for FlexRay bus system.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. XcpTxPduRef

- **UUID**: `b154ce78-aa8c-45e2-897a-2500c2ececd2`
- **引用名**: `XcpTxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the global PDU definition that identifies the PDU.

##### 14. XcpCoreDefinition

**容器属性**:

- **UUID**: `224e4cda-f540-40de-adf9-207576132555`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `XcpCoreDefinition`
- **多重性**: [0..65535]
- **构建后可变**: false

**容器描述**:

Container contains all core specific configuration parameters.

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. XcpSendQueueSize

- **UUID**: `f4b820c0-ac2f-4df5-bd17-641e87cfc8b1`
- **参数名**: `XcpSendQueueSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `256`
- **取值范围**: [32..4294967292]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: The size of the transmit queue for this Core in Bytes.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. XcpEcuCCoreDefinitionRef

- **UUID**: `ecb09130-4450-4c82-bd2a-ab5f38265bb9`
- **引用名**: `XcpEcuCCoreDefinitionRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `EcucCoreDefinition`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucHardware/EcucCoreDefinition`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: The reference to the EcuC core definition.

##### 15. XcpCmdConfig

**容器属性**:

- **UUID**: `92945727-5d9e-4961-808f-8e932db7b1b2`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `XcpCmdConfig`
- **多重性**: [1..1]
- **构建后可变**: false

**容器描述**:

This container contains all command specific configuration options.

###### 参数配置

此容器包含 **1** 个参数：

####### BOOLEAN 类型参数

######## 1. XcpOpenCommandInterface

- **UUID**: `75faa7ce-24e6-48a8-8fb6-86c188fcc1af`
- **参数名**: `XcpOpenCommandInterface`
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
- **描述**: The 'Open Command Interface' option provides the possibility for the user to implement unsupported commands in the application. For this a user call-back (XcpAppl_OpenCmdIf) is called with a pointer to the command string as parameter.

###### 配置容器

本模块包含 **9** 个配置容器：

####### 1. XcpStandard

**容器属性**:

- **UUID**: `b2ac43ae-b7d3-4eca-9527-43dc66f3c000`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `XcpStandard`
- **多重性**: [1..1]
- **构建后可变**: false

**容器描述**:

This container contains all standard command specific configuration options.

######## 参数配置

此容器包含 **6** 个参数：

######### BOOLEAN 类型参数

########## 1. XcpBlockUpload

- **UUID**: `eec34f52-9176-4b08-bb0a-8a972a36df9e`
- **参数名**: `XcpBlockUpload`
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
- **描述**: The Slave Block Transfer Mode speeds up memory uploads by transmitting an entire block of continuous response packets. There is only a response packet before and after transmission of the entire block.

There are no limitations allowed for the master device.

The slave returns whether it supports Slave Block Transfer Model in the response of the request 'CONNECT'.

########## 2. XcpCommunicationModeInfo

- **UUID**: `53f8739d-aec7-4efc-90ce-e7fd5c6df87b`
- **参数名**: `XcpCommunicationModeInfo`
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
- **描述**: The XCP command 'GET_COMM_MODE_INFO' returns optional information on different Communication Modes supported by the slave and also the version number of the Protocol Layer implementation.

If the master block mode is supported, also the maximum allowed block size and the minimum separation time are returned.
The XCP Protocol Layer supports the Standard Communication model and also the Master Block Transfer Mode and the Slave Block Transfer Mode.

########## 3. XcpGetIdGeneric

- **UUID**: `1cc35841-484d-4fc5-9df0-0f05287a1bdf`
- **参数名**: `XcpGetIdGeneric`
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
- **描述**: The XCP GET_ID command is used for identification purposes.
This option enables an call-back that is called when the XCP Master sends the GET_ID command and can be used to return the requested information (e.g. Map Filename, EPK Number, ...)

########## 4. XcpMemoryReadProtection

- **UUID**: `fc24e9dd-3874-4e26-894d-965372aadf8c`
- **参数名**: `XcpMemoryReadProtection`
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
- **描述**: If enabled the application has to confirm a read access. The memory address is passed as parameter of a application call-back that is used to verify the access. The application has to either grant or deny the memory access.

If disabled XCP immediately reads the data without an request to the application.

########## 5. XcpSeedKey

- **UUID**: `dc9f7771-275c-4c46-b9dc-f7b9d97227f9`
- **参数名**: `XcpSeedKey`
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
- **描述**: Resources within the slave device can be protected by a 'Seed & Key' mechanism.

The following resources can be protected:
 - synchronous data acquisition (DAQ)
 - synchronous data stimulation (STIM)
 - online calibration (CAL)
 - programming (PGM)

########## 6. XcpUserDefinedCommand

- **UUID**: `d384f2dd-fd28-40d2-a5b6-00dd993dd5cd`
- **参数名**: `XcpUserDefinedCommand`
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
- **描述**: The 'User Defined Command' is optional and can be implemented within the application.

However it must not be used to implement functionalities done by other services.

The application call-back function 'XcpAppl_UserService()' is called to perform application specific actions.

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. XcpCRC

**容器属性**:

- **UUID**: `305bd823-64c3-42a7-9327-02deec0ef405`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `XcpCRC`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

The XCP command BUILD_CHECKSUM returns a checksum that is calculated over the memory block defined by the Memory Transfer Address (MTA) and block size. The MTA will be post-incremented by the block size.

If enabled, the checksum type (size of the checksum) and the calculation method must be configured.

########## 参数配置

此容器包含 **4** 个参数：

########### INTEGER 类型参数

############ 1. XcpCRCBlockSize

- **UUID**: `8362f4ec-b651-4b77-92b9-9faca671d739`
- **参数名**: `XcpCRCBlockSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `256`
- **取值范围**: [1..65535]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: As calculation of the checksum is time consuming the calculation can be split in blocks and calculated in the Xcp_MainFunction. If you make this value to small, the calculation time of the checksum might take to long and the Xcp Master runs in an timeout. If this value is to big the runtime of the Xcp_MainFunction might be to long.

########### BOOLEAN 类型参数

############ 1. XcpAUTOSARCRCModuleSupport

- **UUID**: `e7792192-1563-4060-ae0d-35de8d9f553e`
- **参数名**: `XcpAUTOSARCRCModuleSupport`
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
- **描述**: If 'AUTOSAR CRC Module Support' is enabled only the following checksum calculation methods are available:
 - CRC16_CCITT : CRC16 CCITT algorithm (for details please refer to the XCP Protocol Layer Specification)
 - CRC32            : CRC32 algorithm (for details please refer to the XCP Protocol Layer Specification)

The CRC32 algorithm is only supported if the AUTOSAR CRC Module is used.

############ 2. XcpCustomCRC

- **UUID**: `99d276b2-6988-4ac5-bd7e-4b69617be911`
- **参数名**: `XcpCustomCRC`
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
- **描述**: The CustomCRC Option enables a call-back (XcpAppl_CalculateChecksum) that allows the user to implement his own CRC calculation method instead of the built in methods.

########### ENUMERATION 类型参数

############ 1. XcpCRCCalculationMethod

- **UUID**: `30255595-1f8f-4fe6-83d1-c64e4b8206d6`
- **参数名**: `XcpCRCCalculationMethod`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `ADD_12`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `ADD_11`
  - `ADD_12`
  - `ADD_14`
  - `ADD_22`
  - `ADD_24`
  - `ADD_44`
  - `CRC_16_CITT`
  - `CRC_16`
  - `CRC_32`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Defines the algorithm used for calculation of the checksum.

####### 2. XcpCRC

**容器属性**:

- **UUID**: `305bd823-64c3-42a7-9327-02deec0ef405`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `XcpCRC`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

The XCP command BUILD_CHECKSUM returns a checksum that is calculated over the memory block defined by the Memory Transfer Address (MTA) and block size. The MTA will be post-incremented by the block size.

If enabled, the checksum type (size of the checksum) and the calculation method must be configured.

######## 参数配置

此容器包含 **4** 个参数：

######### INTEGER 类型参数

########## 1. XcpCRCBlockSize

- **UUID**: `8362f4ec-b651-4b77-92b9-9faca671d739`
- **参数名**: `XcpCRCBlockSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `256`
- **取值范围**: [1..65535]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: As calculation of the checksum is time consuming the calculation can be split in blocks and calculated in the Xcp_MainFunction. If you make this value to small, the calculation time of the checksum might take to long and the Xcp Master runs in an timeout. If this value is to big the runtime of the Xcp_MainFunction might be to long.

######### BOOLEAN 类型参数

########## 1. XcpAUTOSARCRCModuleSupport

- **UUID**: `e7792192-1563-4060-ae0d-35de8d9f553e`
- **参数名**: `XcpAUTOSARCRCModuleSupport`
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
- **描述**: If 'AUTOSAR CRC Module Support' is enabled only the following checksum calculation methods are available:
 - CRC16_CCITT : CRC16 CCITT algorithm (for details please refer to the XCP Protocol Layer Specification)
 - CRC32            : CRC32 algorithm (for details please refer to the XCP Protocol Layer Specification)

The CRC32 algorithm is only supported if the AUTOSAR CRC Module is used.

########## 2. XcpCustomCRC

- **UUID**: `99d276b2-6988-4ac5-bd7e-4b69617be911`
- **参数名**: `XcpCustomCRC`
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
- **描述**: The CustomCRC Option enables a call-back (XcpAppl_CalculateChecksum) that allows the user to implement his own CRC calculation method instead of the built in methods.

######### ENUMERATION 类型参数

########## 1. XcpCRCCalculationMethod

- **UUID**: `30255595-1f8f-4fe6-83d1-c64e4b8206d6`
- **参数名**: `XcpCRCCalculationMethod`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `ADD_12`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `ADD_11`
  - `ADD_12`
  - `ADD_14`
  - `ADD_22`
  - `ADD_24`
  - `ADD_44`
  - `CRC_16_CITT`
  - `CRC_16`
  - `CRC_32`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Defines the algorithm used for calculation of the checksum.

####### 3. XcpCalibration

**容器属性**:

- **UUID**: `2fd2b155-02fb-4f7e-904c-86e00061ac06`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `XcpCalibration`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

This container contains all calibration command specific configuration options.

If this container exists the following commands are available:
- DOWNLOAD
- DOWNLOAD_NEXT
- DOWNLOAD_MAX
- SHORT_DOWNLOAD
- MODIFY_BITS
Otherwise, these commands will return an ERR_CMD_UNKNOWN error and calibration of parameters will not be possible!

######## 参数配置

此容器包含 **4** 个参数：

######### INTEGER 类型参数

########## 1. XcpMIN_STForBlockDownload

- **UUID**: `2fa8a39f-d7e6-4797-98fe-bfebe5e804ab`
- **参数名**: `XcpMIN_STForBlockDownload`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..255]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: MIN_ST indicates the required minimum separation time between the packets of a block transfer from the master device to the slave device in units of 100 microseconds.

######### BOOLEAN 类型参数

########## 1. XcpBlockDownload

- **UUID**: `a3234a07-1789-40a1-b433-e4274305f773`
- **参数名**: `XcpBlockDownload`
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
- **描述**: The Master Block Transfer Mode speeds up memory downloads by transmitting an entire block of continuous request packets. There is only one response packet after transmission of the entire block.

The XCP Master has to meet the slave's limitations of the maximum block size and the minimum separation time. These communication parameters are responded within the response to 'GET_COMM_MODE_INFO'.

########## 2. XcpModifyBits

- **UUID**: `ed3cfbb7-170e-493e-826f-c17a2427ca2a`
- **参数名**: `XcpModifyBits`
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
- **描述**: If the feature is disabled the command will not be supported. Thus a modify bit request results in a negative response and no change of any bits.

########## 3. XcpShortDownload

- **UUID**: `b835b3c6-c9f3-40c3-b371-8db3de2a4cef`
- **参数名**: `XcpShortDownload`
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
- **描述**: If the feature is disabled the command will not be supported. Thus a short download request results in a negative response.
As the short download command is only applicable on communication busses with a data length greater eight bytes (e.g. FlexRay).

####### 4. XcpDaqAndStim

**容器属性**:

- **UUID**: `d5704d86-873f-4c8c-9a09-e78784af9170`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `XcpDaqAndStim`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

This container contains all DAQ and STIM command specific configuration options.

Data elements located in the slave's memory are transmitted in Data Transfer Objects (DTOs) from slave to master (DAQ) and from master to slave (STIM).

The Object Description Table (ODT) describes the mapping between the synchronous data transfer objects and the slave's memory.

######## 参数配置

此容器包含 **12** 个参数：

######### INTEGER 类型参数

########## 1. XcpMaxNumberOfOdtDaq

- **UUID**: `29532782-b753-456b-a8e6-0b87845c645f`
- **参数名**: `XcpMaxNumberOfOdtDaq`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `123`
- **取值范围**: [1..32767]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: The maximum number of Object Descriptor Table (ODTs) messages for Synchronous Data Acquisition (DAQ).

########## 2. XcpMaxNumberOfOdtEntries

- **UUID**: `55e47ae1-eb2a-493c-b827-758f016fc12e`
- **参数名**: `XcpMaxNumberOfOdtEntries`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `1`
- **取值范围**: [1..65535]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: The maximum number of Object Descriptor Table Entries (ODT entries) for Synchronous Data Acquisition (DAQ) and Stimulation (STIM). This parameter defined the maximum number of measurement values that are supported. Each enumeration of this parameter requires 5 bytes of RAM.

########## 3. XcpMaxNumberOfOdtStim

- **UUID**: `cd1b248b-09a7-4298-aa84-ef137662ce84`
- **参数名**: `XcpMaxNumberOfOdtStim`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `1`
- **取值范围**: [0..192]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: The maximum number of Object Descriptor Tables (ODTs) for Synchronous Data Stimulation (STIM).

######### BOOLEAN 类型参数

########## 1. XcpFixedTimestamp

- **UUID**: `41f2500a-847d-4d18-b98e-794108e36750`
- **参数名**: `XcpFixedTimestamp`
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
- **描述**: If enabled the slave always sends Data Transfer Object (DTO) Packets in time stamped mode.
Otherwise timestamps are dynamically and individually enabled for each DAQ list.

########## 2. XcpGetDAQEventInfo

- **UUID**: `5479c09e-1612-4e9f-a4cc-1df4d64b1fbe`
- **参数名**: `XcpGetDAQEventInfo`
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
- **描述**: The option 'Get DAQ Event Info' enables the XCP command GET_DAQ_EVENT_INFO.

GET_DAQ_EVENT_INFO provides the following information about event channels:

 - Number of event channel
 - Name of event channel
 - Measurement cycle time of event channel
 - Direction of event channel: DAQ, STIM, DAQ&STIM

########## 3. XcpOverrunIndication

- **UUID**: `acb948e9-6de0-402e-98fc-f8f5e62d7d60`
- **参数名**: `XcpOverrunIndication`
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
- **描述**: Overrun situations are indicated to the Master Control System. An overrun situation is e.g. an overflow of the transmit queue. This will be signaled by the MSB of the ODT number being set.

########## 4. XcpResolutionInfo

- **UUID**: `0869770a-83a4-4fe9-a991-d18569d9c690`
- **参数名**: `XcpResolutionInfo`
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
- **描述**: The option 'Resolution Info' enables the command GET_DAQ_RESOLUTION_INFO, which provides information on the resolution of DAQ lists.

########## 5. XcpResumeMode

- **UUID**: `06bb6233-6254-4bb6-84c2-38b9bbd17984`
- **参数名**: `XcpResumeMode`
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
- **描述**: The option 'Resume Mode' or often also called 'Cold Start Measurement' allows automatic data transfer (DAQ, STIM) directly after power-up of the slave without prior connection to the master calibration system.

########## 6. XcpSynchronousDataStimulation

- **UUID**: `70725459-bc62-4cf6-ac0f-e3a5a51182de`
- **参数名**: `XcpSynchronousDataStimulation`
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
- **描述**: 'Synchronous Data Stimulation (STIM)' is the inverse mode of 'Synchronous Data Acquisition (DAQ)'.

Data elements located in the slave's memory are transmitted in Data Transfer Objects from the master device to the slave device.
These data elements are written to RAM upon XCP events.

########## 7. XcpWriteDAQMultiple

- **UUID**: `d77b0b8d-85c2-473b-a286-875e36a04c75`
- **参数名**: `XcpWriteDAQMultiple`
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
- **描述**: If the feature is disabled the Write DAQ Multiple command will not be supported. Thus a Write DAQ Multiple request results in a negative response.
The Write DAQ Multiple command is only applicable on communication busses with a MAX_CTO value of at least 16 bytes (e.g. on FlexRay or Ethernet).

########## 8. XcpComplementaryDAQ

- **UUID**: `bf812982-aa13-44cc-b355-006ea44ac1b1`
- **参数名**: `XcpComplementaryDAQ`
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
- **描述**: This parameter enables the complementary DAQ channel. In this mode a complementary communication channel can be used for DAQ measurement, e.g. memory mapped PCIe data transfer.

######### ENUMERATION 类型参数

########## 1. XcpDAQMessageHeader

- **UUID**: `c6d16d77-5f5c-4391-84e8-70df3a05f4e8`
- **参数名**: `XcpDAQMessageHeader`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `ODT`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `ODT` (来源: Vector Informatik)
  - `ODT_DAQ8` (来源: Vector Informatik)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This Attribute defines the format of the Identification Field in the DAQ message. It defines the size of the Identification Field and hence the number of individual DAQ messages possible. For most use cases an 1Byte header is sufficient.

The options have the following meaning:
ODT: Absolute ODT Identification Field is used (1Byte header).
ODT_DAQ8: Relative ODT, Absolute DAQ 8 Identification Field is used (2Byte header).

ODT = Object Descriptor Table

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. XcpTimeSync

**容器属性**:

- **UUID**: `bab41e75-86c3-440e-95e4-6a647caa2f0c`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `XcpTimeSync`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

If this container is enabled the extended format of GET_DAQ_CLOCK is enabled to support time sync feature with a grand master clock.

########## 参数配置

此容器包含 **3** 个参数：

########### INTEGER 类型参数

############ 1. XcpGMTimestampTicks

- **UUID**: `db8b70f0-15a8-4faf-97a0-07db352194d6`
- **参数名**: `XcpGMTimestampTicks`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `1`
- **取值范围**: [1..65535]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: The grand master timestamp will be increment by TIMESTAMP_TICKS per unit.

########### STRING 类型参数

############ 1. XcpUUID

- **UUID**: `da14e8a4-370b-43d7-be5f-380297adb83c`
- **参数名**: `XcpUUID`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **字符串变体**:
  - 默认值: `0000000000000000`
  - 最大长度: 16
  - 最小长度: 16
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This is the UUID, a 8 byte string, for the free running server clock.

########### ENUMERATION 类型参数

############ 1. XcpGMTimestampUnit

- **UUID**: `38e6f756-ad32-4aee-acf6-7573a519e66d`
- **参数名**: `XcpGMTimestampUnit`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `TIMESTAMP_UNIT_1NS`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `TIMESTAMP_UNIT_100MS`
  - `TIMESTAMP_UNIT_100NS`
  - `TIMESTAMP_UNIT_100PS`
  - `TIMESTAMP_UNIT_100US`
  - `TIMESTAMP_UNIT_10MS`
  - `TIMESTAMP_UNIT_10NS`
  - `TIMESTAMP_UNIT_10PS`
  - `TIMESTAMP_UNIT_10US`
  - `TIMESTAMP_UNIT_1MS`
  - `TIMESTAMP_UNIT_1NS`
  - `TIMESTAMP_UNIT_1PS`
  - `TIMESTAMP_UNIT_1S`
  - `TIMESTAMP_UNIT_1US`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter indicates the resolution of the grand master clock of the slave when transferring data to master. Each timestamp unit is incremented by XcpTimestampTicks.

####### 5. XcpTimeSync

**容器属性**:

- **UUID**: `bab41e75-86c3-440e-95e4-6a647caa2f0c`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `XcpTimeSync`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

If this container is enabled the extended format of GET_DAQ_CLOCK is enabled to support time sync feature with a grand master clock.

######## 参数配置

此容器包含 **3** 个参数：

######### INTEGER 类型参数

########## 1. XcpGMTimestampTicks

- **UUID**: `db8b70f0-15a8-4faf-97a0-07db352194d6`
- **参数名**: `XcpGMTimestampTicks`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `1`
- **取值范围**: [1..65535]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: The grand master timestamp will be increment by TIMESTAMP_TICKS per unit.

######### STRING 类型参数

########## 1. XcpUUID

- **UUID**: `da14e8a4-370b-43d7-be5f-380297adb83c`
- **参数名**: `XcpUUID`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **字符串变体**:
  - 默认值: `0000000000000000`
  - 最大长度: 16
  - 最小长度: 16
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This is the UUID, a 8 byte string, for the free running server clock.

######### ENUMERATION 类型参数

########## 1. XcpGMTimestampUnit

- **UUID**: `38e6f756-ad32-4aee-acf6-7573a519e66d`
- **参数名**: `XcpGMTimestampUnit`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `TIMESTAMP_UNIT_1NS`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `TIMESTAMP_UNIT_100MS`
  - `TIMESTAMP_UNIT_100NS`
  - `TIMESTAMP_UNIT_100PS`
  - `TIMESTAMP_UNIT_100US`
  - `TIMESTAMP_UNIT_10MS`
  - `TIMESTAMP_UNIT_10NS`
  - `TIMESTAMP_UNIT_10PS`
  - `TIMESTAMP_UNIT_10US`
  - `TIMESTAMP_UNIT_1MS`
  - `TIMESTAMP_UNIT_1NS`
  - `TIMESTAMP_UNIT_1PS`
  - `TIMESTAMP_UNIT_1S`
  - `TIMESTAMP_UNIT_1US`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter indicates the resolution of the grand master clock of the slave when transferring data to master. Each timestamp unit is incremented by XcpTimestampTicks.

####### 6. XcpProgramming

**容器属性**:

- **UUID**: `bb91bed4-dd8e-4c7a-a76a-c3ec58e96dc5`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `XcpProgramming`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

This container contains all flash programming command specific configuration options.

The option 'Programming' enables the programming of non-volatile memory by providing user call-backs that have to implement access to the flash driver.

If the internal flash of the microcontroller cannot be programmed while execution of code from the flash, the 'bootloader download' functionality has to be used instead.

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. XcpMinStPgm

- **UUID**: `f6f2627a-5eb0-4a69-837c-db624e263150`
- **参数名**: `XcpMinStPgm`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..255]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter is evaluated by the XCP Master and defines the delay between two consecutive PROGRAM_NEXT frames. Increase this value if the Slave is not fast enough to process multiple PROGRAM_NEXT frames in Block Mode received during a short time frame.
Please note that this is a feature that must be supported by the XCP Master.

######### BOOLEAN 类型参数

########## 1. XcpProgrammingWriteProtection

- **UUID**: `d240a7b4-f78c-486c-8d1d-bff8b2a3c9d1`
- **参数名**: `XcpProgrammingWriteProtection`
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
- **描述**: The option 'Programming Write Protection' enables the programming write protection of non-volatile memory.

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. XcpSector

**容器属性**:

- **UUID**: `9b1f8582-822f-4f09-8ab4-41225a88aa4b`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `XcpSector`
- **多重性**: [0..255]
- **构建后可变**: false

**容器描述**:

XCP Protocol Layer flash sector information. This is plug and play information and describes the flash segments that are present in the uC.

The option 'Processor and Sector Info' enables the commands:

 - GET_PGM_PROCESSOR_INFO
   Transfers the general properties for programming and the total number of available sectors from the slave device to the master device.

 - GET_SECTOR_INFO
   Transfers information on a specific sector from the slave device to the master device.

########## 参数配置

此容器包含 **2** 个参数：

########### INTEGER 类型参数

############ 1. XcpStartAddress

- **UUID**: `e17702e4-579e-4dd1-829e-9185dcc678ec`
- **参数名**: `XcpStartAddress`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Start Address of Sector

############ 2. XcpEndAddress

- **UUID**: `e7bbbbfe-0ec6-45fa-a871-c6ba3b8731f2`
- **参数名**: `XcpEndAddress`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: End Address of Sector

####### 7. XcpSector

**容器属性**:

- **UUID**: `9b1f8582-822f-4f09-8ab4-41225a88aa4b`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `XcpSector`
- **多重性**: [0..255]
- **构建后可变**: false

**容器描述**:

XCP Protocol Layer flash sector information. This is plug and play information and describes the flash segments that are present in the uC.

The option 'Processor and Sector Info' enables the commands:

 - GET_PGM_PROCESSOR_INFO
   Transfers the general properties for programming and the total number of available sectors from the slave device to the master device.

 - GET_SECTOR_INFO
   Transfers information on a specific sector from the slave device to the master device.

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. XcpStartAddress

- **UUID**: `e17702e4-579e-4dd1-829e-9185dcc678ec`
- **参数名**: `XcpStartAddress`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Start Address of Sector

########## 2. XcpEndAddress

- **UUID**: `e7bbbbfe-0ec6-45fa-a871-c6ba3b8731f2`
- **参数名**: `XcpEndAddress`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: End Address of Sector

####### 8. XcpPageSwitching

**容器属性**:

- **UUID**: `f14aff23-79f6-4017-b526-64abdf3e497e`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `XcpPageSwitching`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

If calibration page switching (PAG) is enabled the access mode calibration data segments can be set by a user call-back.
Calibration data segments and their pages are specified by logical numbers.

######## 参数配置

此容器包含 **3** 个参数：

######### BOOLEAN 类型参数

########## 1. XcpCopyPage

- **UUID**: `f31b5bb6-488b-4049-a846-7e280f06fe0b`
- **参数名**: `XcpCopyPage`
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
- **描述**: If more than one calibration page is defined, the slave can copy a calibration page into another.

In principle any page of any segment can be copied to any page of any segment. However, restrictions might be possible.

########## 2. XcpFreezeMode

- **UUID**: `81665a2c-0b96-47de-97b3-d82986eb6b90`
- **参数名**: `XcpFreezeMode`
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
- **描述**: If enabled the commands SET_SEGMENT_MODE and GET_SEGMENT_MODE are enabled and forwarded to the application.

########## 3. XcpGeneralPagingInfo

- **UUID**: `672285ae-ecad-45f0-a5f5-03b8d085e0c4`
- **参数名**: `XcpGeneralPagingInfo`
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
- **描述**: If 'General Paging Info' is enabled the XCP command 'GET_PAG_PROCESSOR_INFO' returns general information on paging.

The following information is transferred from the slave device to the master device:
 - The total number of segments
 - Whether the freeze mode is supported

Specific information for segments or pages is so far not supported.

####### 9. XcpAsynchMessage

**容器属性**:

- **UUID**: `f944fbf2-57d0-417e-b6d3-14ef21b8f273`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `XcpAsynchMessage`
- **多重性**: [1..1]
- **构建后可变**: false

**容器描述**:

This container contains all asynchronous message specific configuration options.

######## 参数配置

此容器包含 **2** 个参数：

######### BOOLEAN 类型参数

########## 1. XcpEventCodes

- **UUID**: `221e32bc-af0b-4438-ba11-9eeb37613404`
- **参数名**: `XcpEventCodes`
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
- **描述**: 'Event Codes' are transmitted within event packets (EV) from the slave device to the master device.
The transmission is not guaranteed since event packets are not acknowledged.

Please refer to the ASAM XCP Protocol Layer specification for the 'Table of Event codes'.

########## 2. XcpServiceRequestMessage

- **UUID**: `322ea142-f98b-4646-9595-43283c0b44ac`
- **参数名**: `XcpServiceRequestMessage`
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
- **描述**: 'Service Request Messages' are always transmitted within service request packets (SERV) by the slave device, in order to request the master device to perform some action.

The transmission is not guaranteed since service request packets are not acknowledged by the master device.

Please also refer to the XCP Protocol Layer specification for the 'Table of service request codes'.

##### 16. XcpStandard

**容器属性**:

- **UUID**: `b2ac43ae-b7d3-4eca-9527-43dc66f3c000`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `XcpStandard`
- **多重性**: [1..1]
- **构建后可变**: false

**容器描述**:

This container contains all standard command specific configuration options.

###### 参数配置

此容器包含 **6** 个参数：

####### BOOLEAN 类型参数

######## 1. XcpBlockUpload

- **UUID**: `eec34f52-9176-4b08-bb0a-8a972a36df9e`
- **参数名**: `XcpBlockUpload`
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
- **描述**: The Slave Block Transfer Mode speeds up memory uploads by transmitting an entire block of continuous response packets. There is only a response packet before and after transmission of the entire block.

There are no limitations allowed for the master device.

The slave returns whether it supports Slave Block Transfer Model in the response of the request 'CONNECT'.

######## 2. XcpCommunicationModeInfo

- **UUID**: `53f8739d-aec7-4efc-90ce-e7fd5c6df87b`
- **参数名**: `XcpCommunicationModeInfo`
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
- **描述**: The XCP command 'GET_COMM_MODE_INFO' returns optional information on different Communication Modes supported by the slave and also the version number of the Protocol Layer implementation.

If the master block mode is supported, also the maximum allowed block size and the minimum separation time are returned.
The XCP Protocol Layer supports the Standard Communication model and also the Master Block Transfer Mode and the Slave Block Transfer Mode.

######## 3. XcpGetIdGeneric

- **UUID**: `1cc35841-484d-4fc5-9df0-0f05287a1bdf`
- **参数名**: `XcpGetIdGeneric`
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
- **描述**: The XCP GET_ID command is used for identification purposes.
This option enables an call-back that is called when the XCP Master sends the GET_ID command and can be used to return the requested information (e.g. Map Filename, EPK Number, ...)

######## 4. XcpMemoryReadProtection

- **UUID**: `fc24e9dd-3874-4e26-894d-965372aadf8c`
- **参数名**: `XcpMemoryReadProtection`
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
- **描述**: If enabled the application has to confirm a read access. The memory address is passed as parameter of a application call-back that is used to verify the access. The application has to either grant or deny the memory access.

If disabled XCP immediately reads the data without an request to the application.

######## 5. XcpSeedKey

- **UUID**: `dc9f7771-275c-4c46-b9dc-f7b9d97227f9`
- **参数名**: `XcpSeedKey`
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
- **描述**: Resources within the slave device can be protected by a 'Seed & Key' mechanism.

The following resources can be protected:
 - synchronous data acquisition (DAQ)
 - synchronous data stimulation (STIM)
 - online calibration (CAL)
 - programming (PGM)

######## 6. XcpUserDefinedCommand

- **UUID**: `d384f2dd-fd28-40d2-a5b6-00dd993dd5cd`
- **参数名**: `XcpUserDefinedCommand`
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
- **描述**: The 'User Defined Command' is optional and can be implemented within the application.

However it must not be used to implement functionalities done by other services.

The application call-back function 'XcpAppl_UserService()' is called to perform application specific actions.

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. XcpCRC

**容器属性**:

- **UUID**: `305bd823-64c3-42a7-9327-02deec0ef405`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `XcpCRC`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

The XCP command BUILD_CHECKSUM returns a checksum that is calculated over the memory block defined by the Memory Transfer Address (MTA) and block size. The MTA will be post-incremented by the block size.

If enabled, the checksum type (size of the checksum) and the calculation method must be configured.

######## 参数配置

此容器包含 **4** 个参数：

######### INTEGER 类型参数

########## 1. XcpCRCBlockSize

- **UUID**: `8362f4ec-b651-4b77-92b9-9faca671d739`
- **参数名**: `XcpCRCBlockSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `256`
- **取值范围**: [1..65535]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: As calculation of the checksum is time consuming the calculation can be split in blocks and calculated in the Xcp_MainFunction. If you make this value to small, the calculation time of the checksum might take to long and the Xcp Master runs in an timeout. If this value is to big the runtime of the Xcp_MainFunction might be to long.

######### BOOLEAN 类型参数

########## 1. XcpAUTOSARCRCModuleSupport

- **UUID**: `e7792192-1563-4060-ae0d-35de8d9f553e`
- **参数名**: `XcpAUTOSARCRCModuleSupport`
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
- **描述**: If 'AUTOSAR CRC Module Support' is enabled only the following checksum calculation methods are available:
 - CRC16_CCITT : CRC16 CCITT algorithm (for details please refer to the XCP Protocol Layer Specification)
 - CRC32            : CRC32 algorithm (for details please refer to the XCP Protocol Layer Specification)

The CRC32 algorithm is only supported if the AUTOSAR CRC Module is used.

########## 2. XcpCustomCRC

- **UUID**: `99d276b2-6988-4ac5-bd7e-4b69617be911`
- **参数名**: `XcpCustomCRC`
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
- **描述**: The CustomCRC Option enables a call-back (XcpAppl_CalculateChecksum) that allows the user to implement his own CRC calculation method instead of the built in methods.

######### ENUMERATION 类型参数

########## 1. XcpCRCCalculationMethod

- **UUID**: `30255595-1f8f-4fe6-83d1-c64e4b8206d6`
- **参数名**: `XcpCRCCalculationMethod`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `ADD_12`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `ADD_11`
  - `ADD_12`
  - `ADD_14`
  - `ADD_22`
  - `ADD_24`
  - `ADD_44`
  - `CRC_16_CITT`
  - `CRC_16`
  - `CRC_32`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Defines the algorithm used for calculation of the checksum.

##### 17. XcpCRC

**容器属性**:

- **UUID**: `305bd823-64c3-42a7-9327-02deec0ef405`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `XcpCRC`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

The XCP command BUILD_CHECKSUM returns a checksum that is calculated over the memory block defined by the Memory Transfer Address (MTA) and block size. The MTA will be post-incremented by the block size.

If enabled, the checksum type (size of the checksum) and the calculation method must be configured.

###### 参数配置

此容器包含 **4** 个参数：

####### INTEGER 类型参数

######## 1. XcpCRCBlockSize

- **UUID**: `8362f4ec-b651-4b77-92b9-9faca671d739`
- **参数名**: `XcpCRCBlockSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `256`
- **取值范围**: [1..65535]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: As calculation of the checksum is time consuming the calculation can be split in blocks and calculated in the Xcp_MainFunction. If you make this value to small, the calculation time of the checksum might take to long and the Xcp Master runs in an timeout. If this value is to big the runtime of the Xcp_MainFunction might be to long.

####### BOOLEAN 类型参数

######## 1. XcpAUTOSARCRCModuleSupport

- **UUID**: `e7792192-1563-4060-ae0d-35de8d9f553e`
- **参数名**: `XcpAUTOSARCRCModuleSupport`
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
- **描述**: If 'AUTOSAR CRC Module Support' is enabled only the following checksum calculation methods are available:
 - CRC16_CCITT : CRC16 CCITT algorithm (for details please refer to the XCP Protocol Layer Specification)
 - CRC32            : CRC32 algorithm (for details please refer to the XCP Protocol Layer Specification)

The CRC32 algorithm is only supported if the AUTOSAR CRC Module is used.

######## 2. XcpCustomCRC

- **UUID**: `99d276b2-6988-4ac5-bd7e-4b69617be911`
- **参数名**: `XcpCustomCRC`
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
- **描述**: The CustomCRC Option enables a call-back (XcpAppl_CalculateChecksum) that allows the user to implement his own CRC calculation method instead of the built in methods.

####### ENUMERATION 类型参数

######## 1. XcpCRCCalculationMethod

- **UUID**: `30255595-1f8f-4fe6-83d1-c64e4b8206d6`
- **参数名**: `XcpCRCCalculationMethod`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `ADD_12`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `ADD_11`
  - `ADD_12`
  - `ADD_14`
  - `ADD_22`
  - `ADD_24`
  - `ADD_44`
  - `CRC_16_CITT`
  - `CRC_16`
  - `CRC_32`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Defines the algorithm used for calculation of the checksum.

##### 18. XcpCalibration

**容器属性**:

- **UUID**: `2fd2b155-02fb-4f7e-904c-86e00061ac06`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `XcpCalibration`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

This container contains all calibration command specific configuration options.

If this container exists the following commands are available:
- DOWNLOAD
- DOWNLOAD_NEXT
- DOWNLOAD_MAX
- SHORT_DOWNLOAD
- MODIFY_BITS
Otherwise, these commands will return an ERR_CMD_UNKNOWN error and calibration of parameters will not be possible!

###### 参数配置

此容器包含 **4** 个参数：

####### INTEGER 类型参数

######## 1. XcpMIN_STForBlockDownload

- **UUID**: `2fa8a39f-d7e6-4797-98fe-bfebe5e804ab`
- **参数名**: `XcpMIN_STForBlockDownload`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..255]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: MIN_ST indicates the required minimum separation time between the packets of a block transfer from the master device to the slave device in units of 100 microseconds.

####### BOOLEAN 类型参数

######## 1. XcpBlockDownload

- **UUID**: `a3234a07-1789-40a1-b433-e4274305f773`
- **参数名**: `XcpBlockDownload`
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
- **描述**: The Master Block Transfer Mode speeds up memory downloads by transmitting an entire block of continuous request packets. There is only one response packet after transmission of the entire block.

The XCP Master has to meet the slave's limitations of the maximum block size and the minimum separation time. These communication parameters are responded within the response to 'GET_COMM_MODE_INFO'.

######## 2. XcpModifyBits

- **UUID**: `ed3cfbb7-170e-493e-826f-c17a2427ca2a`
- **参数名**: `XcpModifyBits`
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
- **描述**: If the feature is disabled the command will not be supported. Thus a modify bit request results in a negative response and no change of any bits.

######## 3. XcpShortDownload

- **UUID**: `b835b3c6-c9f3-40c3-b371-8db3de2a4cef`
- **参数名**: `XcpShortDownload`
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
- **描述**: If the feature is disabled the command will not be supported. Thus a short download request results in a negative response.
As the short download command is only applicable on communication busses with a data length greater eight bytes (e.g. FlexRay).

##### 19. XcpDaqAndStim

**容器属性**:

- **UUID**: `d5704d86-873f-4c8c-9a09-e78784af9170`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `XcpDaqAndStim`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

This container contains all DAQ and STIM command specific configuration options.

Data elements located in the slave's memory are transmitted in Data Transfer Objects (DTOs) from slave to master (DAQ) and from master to slave (STIM).

The Object Description Table (ODT) describes the mapping between the synchronous data transfer objects and the slave's memory.

###### 参数配置

此容器包含 **12** 个参数：

####### INTEGER 类型参数

######## 1. XcpMaxNumberOfOdtDaq

- **UUID**: `29532782-b753-456b-a8e6-0b87845c645f`
- **参数名**: `XcpMaxNumberOfOdtDaq`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `123`
- **取值范围**: [1..32767]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: The maximum number of Object Descriptor Table (ODTs) messages for Synchronous Data Acquisition (DAQ).

######## 2. XcpMaxNumberOfOdtEntries

- **UUID**: `55e47ae1-eb2a-493c-b827-758f016fc12e`
- **参数名**: `XcpMaxNumberOfOdtEntries`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `1`
- **取值范围**: [1..65535]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: The maximum number of Object Descriptor Table Entries (ODT entries) for Synchronous Data Acquisition (DAQ) and Stimulation (STIM). This parameter defined the maximum number of measurement values that are supported. Each enumeration of this parameter requires 5 bytes of RAM.

######## 3. XcpMaxNumberOfOdtStim

- **UUID**: `cd1b248b-09a7-4298-aa84-ef137662ce84`
- **参数名**: `XcpMaxNumberOfOdtStim`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `1`
- **取值范围**: [0..192]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: The maximum number of Object Descriptor Tables (ODTs) for Synchronous Data Stimulation (STIM).

####### BOOLEAN 类型参数

######## 1. XcpFixedTimestamp

- **UUID**: `41f2500a-847d-4d18-b98e-794108e36750`
- **参数名**: `XcpFixedTimestamp`
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
- **描述**: If enabled the slave always sends Data Transfer Object (DTO) Packets in time stamped mode.
Otherwise timestamps are dynamically and individually enabled for each DAQ list.

######## 2. XcpGetDAQEventInfo

- **UUID**: `5479c09e-1612-4e9f-a4cc-1df4d64b1fbe`
- **参数名**: `XcpGetDAQEventInfo`
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
- **描述**: The option 'Get DAQ Event Info' enables the XCP command GET_DAQ_EVENT_INFO.

GET_DAQ_EVENT_INFO provides the following information about event channels:

 - Number of event channel
 - Name of event channel
 - Measurement cycle time of event channel
 - Direction of event channel: DAQ, STIM, DAQ&STIM

######## 3. XcpOverrunIndication

- **UUID**: `acb948e9-6de0-402e-98fc-f8f5e62d7d60`
- **参数名**: `XcpOverrunIndication`
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
- **描述**: Overrun situations are indicated to the Master Control System. An overrun situation is e.g. an overflow of the transmit queue. This will be signaled by the MSB of the ODT number being set.

######## 4. XcpResolutionInfo

- **UUID**: `0869770a-83a4-4fe9-a991-d18569d9c690`
- **参数名**: `XcpResolutionInfo`
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
- **描述**: The option 'Resolution Info' enables the command GET_DAQ_RESOLUTION_INFO, which provides information on the resolution of DAQ lists.

######## 5. XcpResumeMode

- **UUID**: `06bb6233-6254-4bb6-84c2-38b9bbd17984`
- **参数名**: `XcpResumeMode`
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
- **描述**: The option 'Resume Mode' or often also called 'Cold Start Measurement' allows automatic data transfer (DAQ, STIM) directly after power-up of the slave without prior connection to the master calibration system.

######## 6. XcpSynchronousDataStimulation

- **UUID**: `70725459-bc62-4cf6-ac0f-e3a5a51182de`
- **参数名**: `XcpSynchronousDataStimulation`
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
- **描述**: 'Synchronous Data Stimulation (STIM)' is the inverse mode of 'Synchronous Data Acquisition (DAQ)'.

Data elements located in the slave's memory are transmitted in Data Transfer Objects from the master device to the slave device.
These data elements are written to RAM upon XCP events.

######## 7. XcpWriteDAQMultiple

- **UUID**: `d77b0b8d-85c2-473b-a286-875e36a04c75`
- **参数名**: `XcpWriteDAQMultiple`
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
- **描述**: If the feature is disabled the Write DAQ Multiple command will not be supported. Thus a Write DAQ Multiple request results in a negative response.
The Write DAQ Multiple command is only applicable on communication busses with a MAX_CTO value of at least 16 bytes (e.g. on FlexRay or Ethernet).

######## 8. XcpComplementaryDAQ

- **UUID**: `bf812982-aa13-44cc-b355-006ea44ac1b1`
- **参数名**: `XcpComplementaryDAQ`
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
- **描述**: This parameter enables the complementary DAQ channel. In this mode a complementary communication channel can be used for DAQ measurement, e.g. memory mapped PCIe data transfer.

####### ENUMERATION 类型参数

######## 1. XcpDAQMessageHeader

- **UUID**: `c6d16d77-5f5c-4391-84e8-70df3a05f4e8`
- **参数名**: `XcpDAQMessageHeader`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `ODT`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `ODT` (来源: Vector Informatik)
  - `ODT_DAQ8` (来源: Vector Informatik)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This Attribute defines the format of the Identification Field in the DAQ message. It defines the size of the Identification Field and hence the number of individual DAQ messages possible. For most use cases an 1Byte header is sufficient.

The options have the following meaning:
ODT: Absolute ODT Identification Field is used (1Byte header).
ODT_DAQ8: Relative ODT, Absolute DAQ 8 Identification Field is used (2Byte header).

ODT = Object Descriptor Table

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. XcpTimeSync

**容器属性**:

- **UUID**: `bab41e75-86c3-440e-95e4-6a647caa2f0c`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `XcpTimeSync`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

If this container is enabled the extended format of GET_DAQ_CLOCK is enabled to support time sync feature with a grand master clock.

######## 参数配置

此容器包含 **3** 个参数：

######### INTEGER 类型参数

########## 1. XcpGMTimestampTicks

- **UUID**: `db8b70f0-15a8-4faf-97a0-07db352194d6`
- **参数名**: `XcpGMTimestampTicks`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `1`
- **取值范围**: [1..65535]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: The grand master timestamp will be increment by TIMESTAMP_TICKS per unit.

######### STRING 类型参数

########## 1. XcpUUID

- **UUID**: `da14e8a4-370b-43d7-be5f-380297adb83c`
- **参数名**: `XcpUUID`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **字符串变体**:
  - 默认值: `0000000000000000`
  - 最大长度: 16
  - 最小长度: 16
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This is the UUID, a 8 byte string, for the free running server clock.

######### ENUMERATION 类型参数

########## 1. XcpGMTimestampUnit

- **UUID**: `38e6f756-ad32-4aee-acf6-7573a519e66d`
- **参数名**: `XcpGMTimestampUnit`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `TIMESTAMP_UNIT_1NS`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `TIMESTAMP_UNIT_100MS`
  - `TIMESTAMP_UNIT_100NS`
  - `TIMESTAMP_UNIT_100PS`
  - `TIMESTAMP_UNIT_100US`
  - `TIMESTAMP_UNIT_10MS`
  - `TIMESTAMP_UNIT_10NS`
  - `TIMESTAMP_UNIT_10PS`
  - `TIMESTAMP_UNIT_10US`
  - `TIMESTAMP_UNIT_1MS`
  - `TIMESTAMP_UNIT_1NS`
  - `TIMESTAMP_UNIT_1PS`
  - `TIMESTAMP_UNIT_1S`
  - `TIMESTAMP_UNIT_1US`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter indicates the resolution of the grand master clock of the slave when transferring data to master. Each timestamp unit is incremented by XcpTimestampTicks.

##### 20. XcpTimeSync

**容器属性**:

- **UUID**: `bab41e75-86c3-440e-95e4-6a647caa2f0c`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `XcpTimeSync`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

If this container is enabled the extended format of GET_DAQ_CLOCK is enabled to support time sync feature with a grand master clock.

###### 参数配置

此容器包含 **3** 个参数：

####### INTEGER 类型参数

######## 1. XcpGMTimestampTicks

- **UUID**: `db8b70f0-15a8-4faf-97a0-07db352194d6`
- **参数名**: `XcpGMTimestampTicks`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `1`
- **取值范围**: [1..65535]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: The grand master timestamp will be increment by TIMESTAMP_TICKS per unit.

####### STRING 类型参数

######## 1. XcpUUID

- **UUID**: `da14e8a4-370b-43d7-be5f-380297adb83c`
- **参数名**: `XcpUUID`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **字符串变体**:
  - 默认值: `0000000000000000`
  - 最大长度: 16
  - 最小长度: 16
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This is the UUID, a 8 byte string, for the free running server clock.

####### ENUMERATION 类型参数

######## 1. XcpGMTimestampUnit

- **UUID**: `38e6f756-ad32-4aee-acf6-7573a519e66d`
- **参数名**: `XcpGMTimestampUnit`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `TIMESTAMP_UNIT_1NS`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `TIMESTAMP_UNIT_100MS`
  - `TIMESTAMP_UNIT_100NS`
  - `TIMESTAMP_UNIT_100PS`
  - `TIMESTAMP_UNIT_100US`
  - `TIMESTAMP_UNIT_10MS`
  - `TIMESTAMP_UNIT_10NS`
  - `TIMESTAMP_UNIT_10PS`
  - `TIMESTAMP_UNIT_10US`
  - `TIMESTAMP_UNIT_1MS`
  - `TIMESTAMP_UNIT_1NS`
  - `TIMESTAMP_UNIT_1PS`
  - `TIMESTAMP_UNIT_1S`
  - `TIMESTAMP_UNIT_1US`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter indicates the resolution of the grand master clock of the slave when transferring data to master. Each timestamp unit is incremented by XcpTimestampTicks.

##### 21. XcpProgramming

**容器属性**:

- **UUID**: `bb91bed4-dd8e-4c7a-a76a-c3ec58e96dc5`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `XcpProgramming`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

This container contains all flash programming command specific configuration options.

The option 'Programming' enables the programming of non-volatile memory by providing user call-backs that have to implement access to the flash driver.

If the internal flash of the microcontroller cannot be programmed while execution of code from the flash, the 'bootloader download' functionality has to be used instead.

###### 参数配置

此容器包含 **2** 个参数：

####### INTEGER 类型参数

######## 1. XcpMinStPgm

- **UUID**: `f6f2627a-5eb0-4a69-837c-db624e263150`
- **参数名**: `XcpMinStPgm`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..255]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter is evaluated by the XCP Master and defines the delay between two consecutive PROGRAM_NEXT frames. Increase this value if the Slave is not fast enough to process multiple PROGRAM_NEXT frames in Block Mode received during a short time frame.
Please note that this is a feature that must be supported by the XCP Master.

####### BOOLEAN 类型参数

######## 1. XcpProgrammingWriteProtection

- **UUID**: `d240a7b4-f78c-486c-8d1d-bff8b2a3c9d1`
- **参数名**: `XcpProgrammingWriteProtection`
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
- **描述**: The option 'Programming Write Protection' enables the programming write protection of non-volatile memory.

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. XcpSector

**容器属性**:

- **UUID**: `9b1f8582-822f-4f09-8ab4-41225a88aa4b`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `XcpSector`
- **多重性**: [0..255]
- **构建后可变**: false

**容器描述**:

XCP Protocol Layer flash sector information. This is plug and play information and describes the flash segments that are present in the uC.

The option 'Processor and Sector Info' enables the commands:

 - GET_PGM_PROCESSOR_INFO
   Transfers the general properties for programming and the total number of available sectors from the slave device to the master device.

 - GET_SECTOR_INFO
   Transfers information on a specific sector from the slave device to the master device.

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. XcpStartAddress

- **UUID**: `e17702e4-579e-4dd1-829e-9185dcc678ec`
- **参数名**: `XcpStartAddress`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Start Address of Sector

########## 2. XcpEndAddress

- **UUID**: `e7bbbbfe-0ec6-45fa-a871-c6ba3b8731f2`
- **参数名**: `XcpEndAddress`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: End Address of Sector

##### 22. XcpSector

**容器属性**:

- **UUID**: `9b1f8582-822f-4f09-8ab4-41225a88aa4b`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `XcpSector`
- **多重性**: [0..255]
- **构建后可变**: false

**容器描述**:

XCP Protocol Layer flash sector information. This is plug and play information and describes the flash segments that are present in the uC.

The option 'Processor and Sector Info' enables the commands:

 - GET_PGM_PROCESSOR_INFO
   Transfers the general properties for programming and the total number of available sectors from the slave device to the master device.

 - GET_SECTOR_INFO
   Transfers information on a specific sector from the slave device to the master device.

###### 参数配置

此容器包含 **2** 个参数：

####### INTEGER 类型参数

######## 1. XcpStartAddress

- **UUID**: `e17702e4-579e-4dd1-829e-9185dcc678ec`
- **参数名**: `XcpStartAddress`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Start Address of Sector

######## 2. XcpEndAddress

- **UUID**: `e7bbbbfe-0ec6-45fa-a871-c6ba3b8731f2`
- **参数名**: `XcpEndAddress`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: End Address of Sector

##### 23. XcpPageSwitching

**容器属性**:

- **UUID**: `f14aff23-79f6-4017-b526-64abdf3e497e`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `XcpPageSwitching`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

If calibration page switching (PAG) is enabled the access mode calibration data segments can be set by a user call-back.
Calibration data segments and their pages are specified by logical numbers.

###### 参数配置

此容器包含 **3** 个参数：

####### BOOLEAN 类型参数

######## 1. XcpCopyPage

- **UUID**: `f31b5bb6-488b-4049-a846-7e280f06fe0b`
- **参数名**: `XcpCopyPage`
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
- **描述**: If more than one calibration page is defined, the slave can copy a calibration page into another.

In principle any page of any segment can be copied to any page of any segment. However, restrictions might be possible.

######## 2. XcpFreezeMode

- **UUID**: `81665a2c-0b96-47de-97b3-d82986eb6b90`
- **参数名**: `XcpFreezeMode`
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
- **描述**: If enabled the commands SET_SEGMENT_MODE and GET_SEGMENT_MODE are enabled and forwarded to the application.

######## 3. XcpGeneralPagingInfo

- **UUID**: `672285ae-ecad-45f0-a5f5-03b8d085e0c4`
- **参数名**: `XcpGeneralPagingInfo`
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
- **描述**: If 'General Paging Info' is enabled the XCP command 'GET_PAG_PROCESSOR_INFO' returns general information on paging.

The following information is transferred from the slave device to the master device:
 - The total number of segments
 - Whether the freeze mode is supported

Specific information for segments or pages is so far not supported.

##### 24. XcpAsynchMessage

**容器属性**:

- **UUID**: `f944fbf2-57d0-417e-b6d3-14ef21b8f273`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `XcpAsynchMessage`
- **多重性**: [1..1]
- **构建后可变**: false

**容器描述**:

This container contains all asynchronous message specific configuration options.

###### 参数配置

此容器包含 **2** 个参数：

####### BOOLEAN 类型参数

######## 1. XcpEventCodes

- **UUID**: `221e32bc-af0b-4438-ba11-9eeb37613404`
- **参数名**: `XcpEventCodes`
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
- **描述**: 'Event Codes' are transmitted within event packets (EV) from the slave device to the master device.
The transmission is not guaranteed since event packets are not acknowledged.

Please refer to the ASAM XCP Protocol Layer specification for the 'Table of Event codes'.

######## 2. XcpServiceRequestMessage

- **UUID**: `322ea142-f98b-4646-9595-43283c0b44ac`
- **参数名**: `XcpServiceRequestMessage`
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
- **描述**: 'Service Request Messages' are always transmitted within service request packets (SERV) by the slave device, in order to request the master device to perform some action.

The transmission is not guaranteed since service request packets are not acknowledged by the master device.

Please also refer to the XCP Protocol Layer specification for the 'Table of service request codes'.

##### 25. XcpGeneral

**容器属性**:

- **UUID**: `d9eca801-2d8b-4692-8579-055367b63f48`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `XcpGeneral`
- **多重性**: [1..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

General configuration parameters of the XCP.

###### 参数配置

此容器包含 **33** 个参数：

####### INTEGER 类型参数

######## 1. XcpDaqCount

- **UUID**: `398d1dc1-a48a-434e-8bca-9c75a1ae0ae6`
- **参数名**: `XcpDaqCount`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `192`
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Indicates the number of DAQ lists for dynamic configuration.

Parameter not supported!

######## 2. XcpMaxCto

- **UUID**: `6a9e0af4-0e07-44cc-9f1e-72ff755cf966`
- **参数名**: `XcpMaxCto`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `8`
- **取值范围**: [8..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: MAX_CTO shows the maximum length of a CTO packet in bytes.

Parameter not supported!

######## 3. XcpMaxDto

- **UUID**: `2768854f-f697-4974-acd8-b1079d397841`
- **参数名**: `XcpMaxDto`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `8`
- **取值范围**: [8..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: MAX_DTO shows the maximum length of a DTO packet in bytes.

Parameter not supported!

######## 4. XcpMaxEventChannel

- **UUID**: `9c129797-94d8-4ff3-b32a-4f4373e42910`
- **参数名**: `XcpMaxEventChannel`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `255`
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Defines the maximum number of supported Event Channels.

Parameter not supported!

######## 5. XcpMinDaq

- **UUID**: `c83cc863-cda9-4c48-8acb-e175a77b9f96`
- **参数名**: `XcpMinDaq`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Indicates the number of predefined, read only DAQ lists on the XCP slave.

Parameter not supported!

######## 6. XcpOdtCount

- **UUID**: `95f497df-5048-4c7f-ad40-a1adf53ebe83`
- **参数名**: `XcpOdtCount`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `192`
- **取值范围**: [0..252]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter indicates the amount of ODTs of a DAQ list using dynamic DAQ list configuration.

Parameter not supported!

######## 7. XcpOdtEntriesCount

- **UUID**: `46cb029f-e67e-4f8d-8188-94d448e270f6`
- **参数名**: `XcpOdtEntriesCount`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `255`
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Indicates the amount of entries into an ODT using dynamic DAQ list configuration.

Parameter not supported!

######## 8. XcpOdtEntrySizeDaq

- **UUID**: `bf4d4e54-9408-44f7-9c5f-7968f7d08caa`
- **参数名**: `XcpOdtEntrySizeDaq`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `255`
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Indicates the size of an element described by an ODT entry to the DaqListType for a DAQ.

Parameter not supported!

######## 9. XcpOdtEntrySizeStim

- **UUID**: `91d1a05a-05a7-4ddc-a5c2-7543ca6e99b1`
- **参数名**: `XcpOdtEntrySizeStim`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `255`
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Indicates the size of an element described by an ODT entry to the DaqListType for a stim.

Parameter not supported!

######## 10. XcpTimestampTicks

- **UUID**: `a5762361-5b7e-47ea-a648-fe1efeb1f10a`
- **参数名**: `XcpTimestampTicks`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `1`
- **取值范围**: [1..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: The timestamp will be increment by TIMESTAMP_TICKS per unit.

####### BOOLEAN 类型参数

######## 1. XcpDevErrorDetect

- **UUID**: `8ef764ce-d92d-48ea-a15e-a603616b1281`
- **参数名**: `XcpDevErrorDetect`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Switches the Development Error Detection and Notification on or off. 
TRUE: Development Error Detection and Notificiation on
FALSE: Development Error Detection and Notification off

######## 2. XcpOnCanEnabled

- **UUID**: `12bdce11-57ac-4df2-8b4d-7a375cd8ab45`
- **参数名**: `XcpOnCanEnabled`
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
- **描述**: Enabling of XCPonCAN functionality
It is enabled if the respective PDU is present.

######## 3. XcpOnCddEnabled

- **UUID**: `63966c1e-75a3-4a5b-8f89-b6b5832aa830`
- **参数名**: `XcpOnCddEnabled`
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
- **描述**: Enabling of XCPonCdd functionality.

Parameter not supported!

######## 4. XcpOnEthernetEnabled

- **UUID**: `39810e6d-b87b-4948-be1c-3972694b35d5`
- **参数名**: `XcpOnEthernetEnabled`
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
- **描述**: Enabling of XCPonEthernet functionality
It is enabled if the respective PDU is present.

######## 5. XcpOnFlexRayEnabled

- **UUID**: `fd671201-35fe-4fd7-a86f-87d3403ac34f`
- **参数名**: `XcpOnFlexRayEnabled`
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
- **描述**: Enabling of XCPonFlexRay functionality
It is enabled if the respective PDU is present.

######## 6. XcpPrescalerSupported

- **UUID**: `03863537-bfcf-4d80-9c03-d5d7f99060f5`
- **参数名**: `XcpPrescalerSupported`
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
- **描述**: This parameter enables and disables the support for Prescaler support. True is Enabled, False is disabled. The prescaler is a runtime configurable option for each xcp event and can be used to divide down the event call cycle.

Prescaler is always enabled and this Parameter not evaluated!

######## 7. XcpSuppressTxSupport

- **UUID**: `7ae15c7c-9abc-45c3-b912-6b7fedac009c`
- **参数名**: `XcpSuppressTxSupport`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Switches the support of suppressing transmission of PDUs per communication channel on or off.
TRUE: Suppressing of TxPDUs supported
FALSE: Suppressing of TxPDUs not supported

Parameter not supported!

######## 8. XcpVersionInfoApi

- **UUID**: `048da8d6-76b8-4bf2-ae99-254bccbdb6d1`
- **参数名**: `XcpVersionInfoApi`
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
- **描述**: Enables/disables the existence of the XCP_GetVersionInfo() API 
service.
TRUE: XCP_GetVersionInfo() API service exists
FALSE: XCP_GetVersionInfo() API service does not exist

######## 9. XcpBootloaderDownload

- **UUID**: `c87ed047-f21e-4d16-9ab9-42d4f9494f61`
- **参数名**: `XcpBootloaderDownload`
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
- **描述**: In order to reprogram the internal flash of some microcontrollers it is necessary to use a bootloader, because code cannot be executed from flash while programming flash. This Option is used to support a flash kernel by providing a call-back that can be used to bring the applikation in a save state.

######## 10. XcpControl

- **UUID**: `ccd3c1a2-77cf-4570-8c86-a2331b79161c`
- **参数名**: `XcpControl`
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
- **描述**: If enabled the XCP functionality can be enabled/disabled during runtime. The feature may be used to prevent unintended XCP activity by disabling the functionality on a special trigger.

If this option is disabled XCP will always stay activate in the ECU.

######## 11. XcpMultiClientSupport

- **UUID**: `aab70777-6453-4a22-87ef-719c5d619070`
- **参数名**: `XcpMultiClientSupport`
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
- **描述**: Multi Client support.
This option will enable the Xcp protocol layer to handle multiple connections at the same time. The RAM footprint will be multiplied with the number of supported channels.

######## 12. XcpRuntimeMeasurementSupport

- **UUID**: `5a1ec475-c4ce-485e-a306-0bfd8577f250`
- **参数名**: `XcpRuntimeMeasurementSupport`
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
- **描述**: If enabled runtime measurement points are added to the BSW module code and are added to the module configuration of MICROSAR RTM. The available measurement points can be seen and configured in the RTM module configuration. Availability of the MICROSAR RTM module is a prerequisite to make use of the runtime measurement functionality. Runtime measurement should be disabled in production code as measurement points may inflict additional runtime.

######## 13. XcpSafeBswChecks

- **UUID**: `091999c2-00c7-4c83-a152-394cca5cba1c`
- **参数名**: `XcpSafeBswChecks`
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
- **描述**: Selects if safety checks are used. These checks improve robustness as e.g. invalid parameters are checked before function is executed. This attribute has to be enabled for safety projects where this component is mapped to an ASIL partition.

######## 14. XcpSessionStatusAPI

- **UUID**: `6c88d219-5420-4477-a44c-31dac7a33c54`
- **参数名**: `XcpSessionStatusAPI`
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
- **描述**: The API Xcp_GetSessionStatus allows determining the session status of the XCP. It can be used to prevent the communication network to be put to sleep while an XCP communication is active.

######## 15. XcpTypeSafeCopy

- **UUID**: `91d01dce-3e72-4345-b559-47f9789e76f8`
- **参数名**: `XcpTypeSafeCopy`
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
- **描述**: Basic multi core support.
This option will enable a copy operation with 16bit or 32bit data types whereas with this option disabled all copy operations are done byte wise. This will allow data consistency on multi core platform for basic data types as they are copied in one step. If the data types are not aligned on 16 or 32 byte boundaries the copy operation will still be done byte wise.

######## 16. XcpDAQMemAccessByApplication

- **UUID**: `1c567455-6658-4165-b823-40c8c66ed779`
- **参数名**: `XcpDAQMemAccessByApplication`
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
- **描述**: If enabled, memory access for DAQ and STIM is performed via application call-backs.

####### FLOAT 类型参数

######## 1. XcpMainFunctionPeriod

- **UUID**: `2a8bf583-5868-46d7-84d0-e6a5e965414d`
- **参数名**: `XcpMainFunctionPeriod`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `0.005`
- **取值范围**: [0..]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: The XCP does not require this information but the BSW scheduler, which invokes the main function, needs it in order to plan its tasks.

####### STRING 类型参数

######## 1. XcpStationIdentifier

- **UUID**: `8aaa44f7-0763-4faf-ba00-e8872132cad4`
- **参数名**: `XcpStationIdentifier`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: The 'XCP Station Identifier' is an ASAM-MC2 filename without path and file type extension that identifies the ECU's software program version.
It is used for slave device identification and automatic session configuration.

The Master Control System (MCS) can interpret this identifier as file name for the ECU database. The ECU developer should change the XCP station identifier with each program change. This will prevent database using a wrong database and grant the correct access of measurement and calibration objects from the MCS to the ECU.

Another benefit of the usage of the XCP station identifier is the automatic assignment of the correct ECU database at program start of the MCS via the Plug&Play mechanism. The Plug&Play mechanism prevents the user to choose the wrong ECU database.

######## 2. XcpUserConfigFile

- **UUID**: `9a69ad1b-6528-47e8-a251-9efd95e72f6a`
- **参数名**: `XcpUserConfigFile`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: A configuration file (Xcp_Cfg.h) is generated by DaVinci Configurator Pro. If you want to overwrite settings in the generated configuration file, you can specify a path to a user defined configuration file.

The user defined configuration file will be included at the end of the generated file. Therefore definitions in the user defined configuration file can overwrite definitions in the generated configuration file.

The contents of the user defined configuration file is copied to the end of Xcp_Cfg.h.

####### ENUMERATION 类型参数

######## 1. XcpDaqConfigType

- **UUID**: `b9e5e78d-5ba5-4f81-aae3-2ebffd38dd2b`
- **参数名**: `XcpDaqConfigType`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `DAQ_DYNAMIC`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `DAQ_DYNAMIC`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Sets the DAQ_CONFIG_TYPE bit within the DAQ_PROPERTIES parameter to "static" or to "dynamic". If DAQ_STATIC is selected, the DAQ_CONFIG_TYPE bit is set to "0". If DAQ_DYNAMIC is selected, the DAQ_CONFIG_TYPE bit is set to "1".

Parameter not supported!

######## 2. XcpIdentificationFieldType

- **UUID**: `0b2bdb2a-7336-4c56-aee1-4a410c2e276a`
- **参数名**: `XcpIdentificationFieldType`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `ABSOLUTE`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `ABSOLUTE` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Type of Identification Field the slave will use when transferring DAQ Packets to the master. The master has to use the same Type of Identification Field when transferring STIM Packets to the slave.

Parameter not supported!

######## 3. XcpTimestampType

- **UUID**: `0ea39e65-6ddb-4006-91f2-0d5f94ec321b`
- **参数名**: `XcpTimestampType`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `TWO_BYTE`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `FOUR_BYTE`
  - `NO_TIME_STAMP`
  - `ONE_BYTE`
  - `TWO_BYTE`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Number of bytes used for the timestamp field in the XCP message. In case No_TIME_STAMP is selected the timestamp field is not available.

######## 4. XcpTimestampUnit

- **UUID**: `6dd07178-23e3-4817-b9b5-ff14727ccb2d`
- **参数名**: `XcpTimestampUnit`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `TIMESTAMP_UNIT_1MS`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `TIMESTAMP_UNIT_100MS` (来源: AUTOSAR_ECUC)
  - `TIMESTAMP_UNIT_100NS` (来源: AUTOSAR_ECUC)
  - `TIMESTAMP_UNIT_100PS` (来源: AUTOSAR_ECUC)
  - `TIMESTAMP_UNIT_100US` (来源: AUTOSAR_ECUC)
  - `TIMESTAMP_UNIT_10MS` (来源: AUTOSAR_ECUC)
  - `TIMESTAMP_UNIT_10NS` (来源: AUTOSAR_ECUC)
  - `TIMESTAMP_UNIT_10PS` (来源: AUTOSAR_ECUC)
  - `TIMESTAMP_UNIT_10US` (来源: AUTOSAR_ECUC)
  - `TIMESTAMP_UNIT_1MS` (来源: AUTOSAR_ECUC)
  - `TIMESTAMP_UNIT_1NS` (来源: AUTOSAR_ECUC)
  - `TIMESTAMP_UNIT_1PS` (来源: AUTOSAR_ECUC)
  - `TIMESTAMP_UNIT_1S` (来源: AUTOSAR_ECUC)
  - `TIMESTAMP_UNIT_1US` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter indicates the resolution of the data acquisition clock of the slave when transferring data to master. Each timestamp unit is incremented by XcpTimestampTicks.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. XcpCounterRef

- **UUID**: `965263ee-2cd4-43f8-8275-9c4185b12e08`
- **引用名**: `XcpCounterRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `OsCounter`
- **完整路径**: `/AUTOSAR/EcucDefs/Os/OsCounter`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter contains a reference to the counter, which is used by XCP.

Parameter not supported!

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. XcpA2L

**容器属性**:

- **UUID**: `d2ef1975-47ab-42e7-98ae-ade79dbce7c9`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `XcpA2L`
- **多重性**: [1..1]
- **构建后可变**: false

**容器描述**:

This container contains all A2L related configuration parameter.

######## 参数配置

此容器包含 **9** 个参数：

######### INTEGER 类型参数

########## 1. XcpTimeoutT1

- **UUID**: `62d90ed7-c7d5-49de-92e4-961b2503edca`
- **参数名**: `XcpTimeoutT1`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `2000`
- **取值范围**: [0..2147483647]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter specifies the timeout value T1 used for generic response time out handling by the Xcp Master. Value in [ms]

########## 2. XcpTimeoutT2

- **UUID**: `76092480-ae18-4e64-9eb5-9e6d25f58f99`
- **参数名**: `XcpTimeoutT2`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `10000`
- **取值范围**: [0..2147483647]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter specifies the timeout value T2 used for build checksum response time out handling by the Xcp Master. Value in [ms]

########## 3. XcpTimeoutT3

- **UUID**: `3082e285-ece2-4857-980b-6054046e6f77`
- **参数名**: `XcpTimeoutT3`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `2000`
- **取值范围**: [0..2147483647]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter specifies the timeout value T3 used for programming preparation response time out handling by the Xcp Master. Value in [ms]

########## 4. XcpTimeoutT4

- **UUID**: `0b915837-c73e-4e35-aae4-9bd09e285b83`
- **参数名**: `XcpTimeoutT4`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `2000`
- **取值范围**: [0..2147483647]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter specifies the timeout value T4 used for program clear response time out handling by the Xcp Master. Value in [ms]

########## 5. XcpTimeoutT5

- **UUID**: `e6e502fd-8119-488c-96d9-ddff14cc3eb0`
- **参数名**: `XcpTimeoutT5`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `2000`
- **取值范围**: [0..2147483647]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter specifies the timeout value T5 used for programming response time out handling by the Xcp Master. Value in [ms]

########## 6. XcpTimeoutT6

- **UUID**: `d0276abd-4c4a-4b2e-97d7-dadaa0df4cf6`
- **参数名**: `XcpTimeoutT6`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `2000`
- **取值范围**: [0..2147483647]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter specifies the timeout value T6 used for user defined connect response time out handling by the Xcp Master. Value in [ms]

########## 7. XcpTimeoutT7

- **UUID**: `99d8ad35-b69e-4bbc-bb95-dc5425453e27`
- **参数名**: `XcpTimeoutT7`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..2147483647]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter specifies the timeout value T7 used for pre-action waiting for several commands by the Xcp Master. Value in [ms]

######### STRING 类型参数

########## 1. XcpOnFrClusterId

- **UUID**: `afd0bf84-c1d4-4f2a-8307-d9fcdf563399`
- **参数名**: `XcpOnFrClusterId`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: The Cluster ID identifies the Cluster in the Fibex data base to use.

########## 2. XcpOnFrFibex

- **UUID**: `d4bc10c7-791a-4bac-9a11-2949c21b8c2e`
- **参数名**: `XcpOnFrFibex`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This string contains the name of the Fibex data base. The Fibex is used by the Master Tool to get the FlexRay communication parameters.

##### 26. XcpA2L

**容器属性**:

- **UUID**: `d2ef1975-47ab-42e7-98ae-ade79dbce7c9`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `XcpA2L`
- **多重性**: [1..1]
- **构建后可变**: false

**容器描述**:

This container contains all A2L related configuration parameter.

###### 参数配置

此容器包含 **9** 个参数：

####### INTEGER 类型参数

######## 1. XcpTimeoutT1

- **UUID**: `62d90ed7-c7d5-49de-92e4-961b2503edca`
- **参数名**: `XcpTimeoutT1`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `2000`
- **取值范围**: [0..2147483647]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter specifies the timeout value T1 used for generic response time out handling by the Xcp Master. Value in [ms]

######## 2. XcpTimeoutT2

- **UUID**: `76092480-ae18-4e64-9eb5-9e6d25f58f99`
- **参数名**: `XcpTimeoutT2`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `10000`
- **取值范围**: [0..2147483647]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter specifies the timeout value T2 used for build checksum response time out handling by the Xcp Master. Value in [ms]

######## 3. XcpTimeoutT3

- **UUID**: `3082e285-ece2-4857-980b-6054046e6f77`
- **参数名**: `XcpTimeoutT3`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `2000`
- **取值范围**: [0..2147483647]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter specifies the timeout value T3 used for programming preparation response time out handling by the Xcp Master. Value in [ms]

######## 4. XcpTimeoutT4

- **UUID**: `0b915837-c73e-4e35-aae4-9bd09e285b83`
- **参数名**: `XcpTimeoutT4`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `2000`
- **取值范围**: [0..2147483647]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter specifies the timeout value T4 used for program clear response time out handling by the Xcp Master. Value in [ms]

######## 5. XcpTimeoutT5

- **UUID**: `e6e502fd-8119-488c-96d9-ddff14cc3eb0`
- **参数名**: `XcpTimeoutT5`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `2000`
- **取值范围**: [0..2147483647]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter specifies the timeout value T5 used for programming response time out handling by the Xcp Master. Value in [ms]

######## 6. XcpTimeoutT6

- **UUID**: `d0276abd-4c4a-4b2e-97d7-dadaa0df4cf6`
- **参数名**: `XcpTimeoutT6`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `2000`
- **取值范围**: [0..2147483647]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter specifies the timeout value T6 used for user defined connect response time out handling by the Xcp Master. Value in [ms]

######## 7. XcpTimeoutT7

- **UUID**: `99d8ad35-b69e-4bbc-bb95-dc5425453e27`
- **参数名**: `XcpTimeoutT7`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..2147483647]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter specifies the timeout value T7 used for pre-action waiting for several commands by the Xcp Master. Value in [ms]

####### STRING 类型参数

######## 1. XcpOnFrClusterId

- **UUID**: `afd0bf84-c1d4-4f2a-8307-d9fcdf563399`
- **参数名**: `XcpOnFrClusterId`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: The Cluster ID identifies the Cluster in the Fibex data base to use.

######## 2. XcpOnFrFibex

- **UUID**: `d4bc10c7-791a-4bac-9a11-2949c21b8c2e`
- **参数名**: `XcpOnFrFibex`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This string contains the name of the Fibex data base. The Fibex is used by the Master Tool to get the FlexRay communication parameters.

##### 27. XcpPdu

**容器属性**:

- **UUID**: `4b82fde9-6a3b-4024-ada1-43040c74c205`
- **容器类型**: CHOICE-CONTAINER
- **容器名称**: `XcpPdu`
- **多重性**: [2..infinite]
- **构建后可变**: true

**容器选择**:

- **XcpRxPdu**
  - UUID: `899d9752-fc27-431e-8bd1-9d070fe74f37`
  - 描述: Rx PDU description.
- **XcpTxPdu**
  - UUID: `e60035ab-748f-42f4-8f33-aa5a10405716`
  - 描述: Tx PDU description.

**容器描述**:

Description of the Rx and Tx PDUs used for XCP communication. XCP requires at least one Rx and one Tx PDU for Cmd/Res communication.
CAN: No additional PDUs must be defined. Delete redundant PDUs here and if necessary in the IF
FlexRay: Additional PDUs for DAQ/STIM can be defined
TcpIp: No additional PDUs must be defined. Delete redundant PDUs here and if necessary in the IF

## 📦 包结构

此ARXML文件包含 **1** 个包：

### 1. MICROSAR

- **UUID**: `ff55d029-386d-43a2-b3c2-dfef4c7a5e36`
- **包名称**: `MICROSAR`
- **包含元素数量**: 4

#### 包含的元素

##### ECUC-MODULE-DEF 类型元素

1. **Xcp**

##### BSW-IMPLEMENTATION 类型元素

1. **Xcp_Impl**

##### ECUC-MODULE-CONFIGURATION-VALUES 类型元素

1. **Xcp_Pre**
2. **Xcp_Rec**

## ⚡ 实现信息

此ARXML文件包含 **1** 个实现：

### 1. Xcp_Impl

- **UUID**: `00943845-eaad-4834-86e2-957948b44834`
- **实现名称**: `Xcp_Impl`
- **编程语言**: C
- **软件版本**: 7.00.06
- **供应商ID**: 30
- **AUTOSAR版本**: 4.00.03
- **代码生成器**: cMSR

## ⚙️ 配置信息

此ARXML文件包含 **2** 个配置：

### 1. Xcp_Pre

- **UUID**: `b88fc24c-389c-4b47-9c9a-68f483f508e8`
- **配置名称**: `Xcp_Pre`
- **定义引用**: `/MICROSAR/Xcp`

### 2. Xcp_Rec

- **UUID**: `26135d3d-b6e3-4404-bb03-70bd251603ba`
- **配置名称**: `Xcp_Rec`
- **定义引用**: `/MICROSAR/Xcp`
