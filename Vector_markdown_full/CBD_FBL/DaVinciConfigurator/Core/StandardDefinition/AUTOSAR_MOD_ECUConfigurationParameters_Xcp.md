# Xcp - 完整配置文档

*此文档由ARXML文件自动生成，采用层次化结构展示*

**生成时间**: 2025-06-16 14:48:59

## 📑 目录

- [📄 文件信息](#-文件信息)
- [🔧 模块定义](#-模块定义)
  - [Xcp](#xcp)
- [📦 包结构](#-包结构)

## 📄 文件信息

### Schema信息
- **Schema位置**: `http://autosar.org/schema/r4.0 AUTOSAR_4-0-3.xsd`
- **命名空间**: `http://autosar.org/schema/r4.0`

## 🔧 模块定义

### 1. Xcp

#### 基本信息

- **UUID**: `ECUC:922942fb-6d0c-448b-b576-27276fbb1677`
- **模块名称**: `Xcp`
- **多重性**: [0..1]
- **支持的变体**:
  - VARIANT-POST-BUILD
  - VARIANT-PRE-COMPILE

#### 模块描述

Configuration of the XCP module

#### 版本历史

共有 **1** 个版本记录：

##### 1. 版本 4.2.0

- **发布日期**: 2011-11-09
- **发布者**: AUTOSAR

*此版本无详细变更记录*

#### 配置容器

本模块包含 **11** 个配置容器：

##### 1. XcpConfig

**容器属性**:

- **UUID**: `ECUC:08857b83-4fee-4257-9376-e7552df68ca9`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `XcpConfig`
- **多重性**: [1..1]
- **多配置容器**: true

###### 配置容器

本模块包含 **9** 个配置容器：

####### 1. XcpDaqList

**容器属性**:

- **UUID**: `ECUC:9dc99070-39d1-4cb7-bf19-245216fd72ca`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `XcpDaqList`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

This container contains the configuration of the DAQs.

######## 参数配置

此容器包含 **4** 个参数：

######### INTEGER 类型参数

########## 1. XcpDaqListNumber

- **UUID**: `ECUC:7ae0af73-57f0-4430-9099-c84305c83ce4`
- **参数名**: `XcpDaqListNumber`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65534]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Index number of the DAQ list

########## 2. XcpMaxOdt

- **UUID**: `ECUC:deda1974-043a-400f-8998-2b69a537e7d7`
- **参数名**: `XcpMaxOdt`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..252]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: MAX_ODT indicates the maximum amount of ODTs in this DAQ list

########## 3. XcpMaxOdtEntries

- **UUID**: `ECUC:ebc4ec8f-9bcc-4284-befa-fda296bc41b1`
- **参数名**: `XcpMaxOdtEntries`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter indicates the maximum amount of entries in an ODT of this DAQ list (STATIC configuration).

######### ENUMERATION 类型参数

########## 1. XcpDaqListType

- **UUID**: `ECUC:46551e77-32e5-401c-bb0c-415619f1109a`
- **参数名**: `XcpDaqListType`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `DAQ` (来源: AUTOSAR_ECUC)
  - `DAQ_STIM` (来源: AUTOSAR_ECUC)
  - `STIM` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This indicates whether this DAQ list represents a DAQ or a STIM.

######## 配置容器

本模块包含 **3** 个配置容器：

######### 1. XcpDto

**容器属性**:

- **UUID**: `ECUC:60a6ecc4-2b81-4fe9-89d8-d37b7abbabc6`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `XcpDto`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

This container collects data transfer object specific parameters for the DAQ list.

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. XcpDtoPid

- **UUID**: `ECUC:ab9cfb60-f4fb-4f29-bd2d-3bd3567225cc`
- **参数名**: `XcpDtoPid`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..251]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Packet identifier (PID) of the DTO that identifies the ODT the content of the DTO.

########## 引用关系

此容器包含 **1** 个引用：

########### CHOICE-REFERENCE 类型引用

############ 1. XcpDto2PduMapping

- **UUID**: `ECUC:1f98cbe3-d6bd-44c7-9575-68f54b302fc7`
- **引用名**: `XcpDto2PduMapping`
- **引用类型**: CHOICE-REFERENCE
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **目标引用列表**:
  - `/AUTOSAR/EcucDefs/Xcp/XcpConfig/XcpPdu/XcpRxPdu`
  - `/AUTOSAR/EcucDefs/Xcp/XcpConfig/XcpPdu/XcpTxPdu`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This reference specifies the mapping of the DTO to the PDUs from the lower-layer interfaces (CanIf, FrIf, SoAd and Cdd).

######### 2. XcpOdt

**容器属性**:

- **UUID**: `ECUC:2819db23-acc0-43fe-b4d5-89a6c424aa8d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `XcpOdt`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

This container contains ODT-specific parameter for the DAQ list.

########## 参数配置

此容器包含 **2** 个参数：

########### INTEGER 类型参数

############ 1. XcpOdtEntryMaxSize

- **UUID**: `ECUC:2bb441f0-5e50-4b64-b973-c2274d28fa27`
- **参数名**: `XcpOdtEntryMaxSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..254]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter indicates the upper limit for the size of the element described by an ODT entry. Depending on the DaqListType this ODT belongs to it describes the limit for a DAQ (MAX_ODT_ENTRY_SIZE_DAQ) or a STIM (MAX_ODT_ENTRY_SIZE_STIM).

############ 2. XcpOdtNumber

- **UUID**: `ECUC:5c11368f-1932-4c78-9f9d-e1fef07a1bde`
- **参数名**: `XcpOdtNumber`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..251]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Index number of this ODT within the DAQ list.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. XcpOdt2DtoMapping

- **UUID**: `ECUC:c459aaa3-a782-4d24-b295-566b3252232a`
- **引用名**: `XcpOdt2DtoMapping`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `XcpDto`
- **完整路径**: `/AUTOSAR/EcucDefs/Xcp/XcpConfig/XcpDaqList/XcpDto`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This reference maps the ODT to the according DTO in which it will be transmitted.

########## 配置容器

本模块包含 **1** 个配置容器：

########### 1. XcpOdtEntry

**容器属性**:

- **UUID**: `ECUC:ab97e61f-e5dc-480b-ae85-b565dfbe5e6f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `XcpOdtEntry`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

This container collects all configuration parameters that comprise an ODT entry.

############ 参数配置

此容器包含 **3** 个参数：

############# INTEGER 类型参数

############## 1. XcpOdtEntryLength

- **UUID**: `ECUC:6f0e3297-da74-46cb-9070-ee5f6849d6be`
- **参数名**: `XcpOdtEntryLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Length of the referenced memory area that is referenced by the ODT entry.

############## 2. XcpOdtEntryNumber

- **UUID**: `ECUC:7276d244-9830-468e-bd5d-645648bf4ade`
- **参数名**: `XcpOdtEntryNumber`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..254]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Index number of the ODT entry

############# LINKER-SYMBOL 类型参数

############## 1. XcpOdtEntryAddress

- **UUID**: `ECUC:7e348e20-5489-4222-8de0-d3a2c9bb8410`
- **参数名**: `XcpOdtEntryAddress`
- **数据类型**: LINKER-SYMBOL
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Memory address that the ODT entry is referencing to.

######### 3. XcpOdtEntry

**容器属性**:

- **UUID**: `ECUC:ab97e61f-e5dc-480b-ae85-b565dfbe5e6f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `XcpOdtEntry`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

This container collects all configuration parameters that comprise an ODT entry.

########## 参数配置

此容器包含 **3** 个参数：

########### INTEGER 类型参数

############ 1. XcpOdtEntryLength

- **UUID**: `ECUC:6f0e3297-da74-46cb-9070-ee5f6849d6be`
- **参数名**: `XcpOdtEntryLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Length of the referenced memory area that is referenced by the ODT entry.

############ 2. XcpOdtEntryNumber

- **UUID**: `ECUC:7276d244-9830-468e-bd5d-645648bf4ade`
- **参数名**: `XcpOdtEntryNumber`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..254]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Index number of the ODT entry

########### LINKER-SYMBOL 类型参数

############ 1. XcpOdtEntryAddress

- **UUID**: `ECUC:7e348e20-5489-4222-8de0-d3a2c9bb8410`
- **参数名**: `XcpOdtEntryAddress`
- **数据类型**: LINKER-SYMBOL
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Memory address that the ODT entry is referencing to.

####### 2. XcpDto

**容器属性**:

- **UUID**: `ECUC:60a6ecc4-2b81-4fe9-89d8-d37b7abbabc6`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `XcpDto`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

This container collects data transfer object specific parameters for the DAQ list.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. XcpDtoPid

- **UUID**: `ECUC:ab9cfb60-f4fb-4f29-bd2d-3bd3567225cc`
- **参数名**: `XcpDtoPid`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..251]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Packet identifier (PID) of the DTO that identifies the ODT the content of the DTO.

######## 引用关系

此容器包含 **1** 个引用：

######### CHOICE-REFERENCE 类型引用

########## 1. XcpDto2PduMapping

- **UUID**: `ECUC:1f98cbe3-d6bd-44c7-9575-68f54b302fc7`
- **引用名**: `XcpDto2PduMapping`
- **引用类型**: CHOICE-REFERENCE
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **目标引用列表**:
  - `/AUTOSAR/EcucDefs/Xcp/XcpConfig/XcpPdu/XcpRxPdu`
  - `/AUTOSAR/EcucDefs/Xcp/XcpConfig/XcpPdu/XcpTxPdu`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This reference specifies the mapping of the DTO to the PDUs from the lower-layer interfaces (CanIf, FrIf, SoAd and Cdd).

####### 3. XcpOdt

**容器属性**:

- **UUID**: `ECUC:2819db23-acc0-43fe-b4d5-89a6c424aa8d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `XcpOdt`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

This container contains ODT-specific parameter for the DAQ list.

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. XcpOdtEntryMaxSize

- **UUID**: `ECUC:2bb441f0-5e50-4b64-b973-c2274d28fa27`
- **参数名**: `XcpOdtEntryMaxSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..254]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter indicates the upper limit for the size of the element described by an ODT entry. Depending on the DaqListType this ODT belongs to it describes the limit for a DAQ (MAX_ODT_ENTRY_SIZE_DAQ) or a STIM (MAX_ODT_ENTRY_SIZE_STIM).

########## 2. XcpOdtNumber

- **UUID**: `ECUC:5c11368f-1932-4c78-9f9d-e1fef07a1bde`
- **参数名**: `XcpOdtNumber`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..251]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Index number of this ODT within the DAQ list.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. XcpOdt2DtoMapping

- **UUID**: `ECUC:c459aaa3-a782-4d24-b295-566b3252232a`
- **引用名**: `XcpOdt2DtoMapping`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `XcpDto`
- **完整路径**: `/AUTOSAR/EcucDefs/Xcp/XcpConfig/XcpDaqList/XcpDto`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This reference maps the ODT to the according DTO in which it will be transmitted.

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. XcpOdtEntry

**容器属性**:

- **UUID**: `ECUC:ab97e61f-e5dc-480b-ae85-b565dfbe5e6f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `XcpOdtEntry`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

This container collects all configuration parameters that comprise an ODT entry.

########## 参数配置

此容器包含 **3** 个参数：

########### INTEGER 类型参数

############ 1. XcpOdtEntryLength

- **UUID**: `ECUC:6f0e3297-da74-46cb-9070-ee5f6849d6be`
- **参数名**: `XcpOdtEntryLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Length of the referenced memory area that is referenced by the ODT entry.

############ 2. XcpOdtEntryNumber

- **UUID**: `ECUC:7276d244-9830-468e-bd5d-645648bf4ade`
- **参数名**: `XcpOdtEntryNumber`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..254]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Index number of the ODT entry

########### LINKER-SYMBOL 类型参数

############ 1. XcpOdtEntryAddress

- **UUID**: `ECUC:7e348e20-5489-4222-8de0-d3a2c9bb8410`
- **参数名**: `XcpOdtEntryAddress`
- **数据类型**: LINKER-SYMBOL
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Memory address that the ODT entry is referencing to.

####### 4. XcpOdtEntry

**容器属性**:

- **UUID**: `ECUC:ab97e61f-e5dc-480b-ae85-b565dfbe5e6f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `XcpOdtEntry`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

This container collects all configuration parameters that comprise an ODT entry.

######## 参数配置

此容器包含 **3** 个参数：

######### INTEGER 类型参数

########## 1. XcpOdtEntryLength

- **UUID**: `ECUC:6f0e3297-da74-46cb-9070-ee5f6849d6be`
- **参数名**: `XcpOdtEntryLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Length of the referenced memory area that is referenced by the ODT entry.

########## 2. XcpOdtEntryNumber

- **UUID**: `ECUC:7276d244-9830-468e-bd5d-645648bf4ade`
- **参数名**: `XcpOdtEntryNumber`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..254]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Index number of the ODT entry

######### LINKER-SYMBOL 类型参数

########## 1. XcpOdtEntryAddress

- **UUID**: `ECUC:7e348e20-5489-4222-8de0-d3a2c9bb8410`
- **参数名**: `XcpOdtEntryAddress`
- **数据类型**: LINKER-SYMBOL
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Memory address that the ODT entry is referencing to.

####### 5. XcpDemEventParameterRefs

**容器属性**:

- **UUID**: `ECUC:b6c92c66-4349-4301-ba59-c5ae05da15a1`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `XcpDemEventParameterRefs`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Container for the references to DemEventParameter elements which shall be invoked using the API Dem_ReportErrorStatus API in case the corresponding error occurs. The EventId is taken from the referenced DemEventParameter's DemEventId value. The standardized errors are provided in the container and can be extended by vendor specific error references.

######## 引用关系

此容器包含 **1** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. XCP_E_INIT_FAILED

- **UUID**: `ECUC:06b1ad04-a91c-4e57-8383-0e3b53757516`
- **引用名**: `XCP_E_INIT_FAILED`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `DemEventParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemConfigSet/DemEventParameter`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the DemEventParameter which shall be issued when the error "Initialization of XCP failed" has occured.

####### 6. XcpEventChannel

**容器属性**:

- **UUID**: `ECUC:799c6452-a17b-4306-9b15-2ae608d34306`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `XcpEventChannel`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

This container contains the configuration of event channels on the XCP slave.

######## 参数配置

此容器包含 **7** 个参数：

######### INTEGER 类型参数

########## 1. XcpEventChannelMaxDaqList

- **UUID**: `ECUC:a622228a-6822-44e8-b8af-e66e56182590`
- **参数名**: `XcpEventChannelMaxDaqList`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Maximum amount of DAQ lists that are handled by this event channel.

########## 2. XcpEventChannelNumber

- **UUID**: `ECUC:859fde79-24d2-4a44-9b75-e35d6266433d`
- **参数名**: `XcpEventChannelNumber`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65534]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Index number of the event channel.

########## 3. XcpEventChannelPriority

- **UUID**: `ECUC:cd8c0bb0-99a2-4896-97a0-577062bf9797`
- **参数名**: `XcpEventChannelPriority`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Priority of the event channel

########## 4. XcpEventChannelTimeCycle

- **UUID**: `ECUC:9d286dc2-0a1c-40cf-a3d7-76102b466ab5`
- **参数名**: `XcpEventChannelTimeCycle`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The event channel time cycle indicates which sampling period is used to process this event channel. A value of 0 means 'Not cyclic'.

######### ENUMERATION 类型参数

########## 1. XcpEventChannelConsistency

- **UUID**: `ECUC:634c0118-18db-48cd-9f20-fdde62d1951b`
- **参数名**: `XcpEventChannelConsistency`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `ODT`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `DAQ` (来源: AUTOSAR_ECUC)
  - `EVENT` (来源: AUTOSAR_ECUC)
  - `ODT` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Type of consistency used by event channel

########## 2. XcpEventChannelTimeUnit

- **UUID**: `ECUC:bded059d-3744-4cfe-88fc-948f0922212f`
- **参数名**: `XcpEventChannelTimeUnit`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
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
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This configuration parameter indicates the unit of the event channel time cycle.

########## 3. XcpEventChannelType

- **UUID**: `ECUC:a82678fb-fc06-4749-8c1f-39a73c6d4dbd`
- **参数名**: `XcpEventChannelType`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `DAQ`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `DAQ` (来源: AUTOSAR_ECUC)
  - `DAQ_STIM` (来源: AUTOSAR_ECUC)
  - `STIM` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This configuration parameter indicates what kind of DAQ list can be allocated to this event channel.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. XcpEventChannelTriggeredDaqListRef

- **UUID**: `ECUC:7fed113d-be4e-4d87-9ee2-405ca3bc2228`
- **引用名**: `XcpEventChannelTriggeredDaqListRef`
- **引用类型**: REFERENCE
- **多重性**: [1..infinite]
- **目标**: `XcpDaqList`
- **完整路径**: `/AUTOSAR/EcucDefs/Xcp/XcpConfig/XcpDaqList`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: References all DAQ lists that are trigged by this event channel.

####### 7. XcpRxPdu

**容器属性**:

- **UUID**: `ECUC:3b1ca421-d224-4f77-9401-4c2d5504cefa`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `XcpRxPdu`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container specifies received PDUs.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. XcpRxPduId

- **UUID**: `ECUC:26446775-a0c3-456c-aaab-3d65cc5f8002`
- **参数名**: `XcpRxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: ID of the PDU that will be received via a Xcp_<module>RxIndication.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. XcpRxPduRef

- **UUID**: `ECUC:c6c60025-0a48-48cd-9246-2b1cdf5983e3`
- **引用名**: `XcpRxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE

####### 8. XcpTxPdu

**容器属性**:

- **UUID**: `ECUC:fb220126-dc86-4845-ba4e-a3c57370b0f9`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `XcpTxPdu`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container specifies transmission PDUs.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. XcpTxPduId

- **UUID**: `ECUC:9f920c69-c570-4aa9-9ab1-a216fe2a1faa`
- **参数名**: `XcpTxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The PDU identifier, which has to be used by the lower layer BSW module for TxConfirmations or TriggerTransmits.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. XcpTxPduRef

- **UUID**: `ECUC:46f96041-2ea4-4e3a-96be-8380f6104b3f`
- **引用名**: `XcpTxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the external PDU definition.

####### 9. XcpPdu

**容器属性**:

- **UUID**: `ECUC:3261f87c-0cbf-488c-b716-b4f93003f974`
- **容器类型**: CHOICE-CONTAINER
- **容器名称**: `XcpPdu`
- **多重性**: [1..infinite]

**容器选择**:

- **XcpRxPdu**
  - UUID: `ECUC:3b1ca421-d224-4f77-9401-4c2d5504cefa`
  - 描述: This container specifies received PDUs.
- **XcpTxPdu**
  - UUID: `ECUC:fb220126-dc86-4845-ba4e-a3c57370b0f9`
  - 描述: This container specifies transmission PDUs.

**容器描述**:

Contains PDU information. A PDU may be either a transmission PDU or a reception PDU.

##### 2. XcpDaqList

**容器属性**:

- **UUID**: `ECUC:9dc99070-39d1-4cb7-bf19-245216fd72ca`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `XcpDaqList`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

This container contains the configuration of the DAQs.

###### 参数配置

此容器包含 **4** 个参数：

####### INTEGER 类型参数

######## 1. XcpDaqListNumber

- **UUID**: `ECUC:7ae0af73-57f0-4430-9099-c84305c83ce4`
- **参数名**: `XcpDaqListNumber`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65534]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Index number of the DAQ list

######## 2. XcpMaxOdt

- **UUID**: `ECUC:deda1974-043a-400f-8998-2b69a537e7d7`
- **参数名**: `XcpMaxOdt`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..252]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: MAX_ODT indicates the maximum amount of ODTs in this DAQ list

######## 3. XcpMaxOdtEntries

- **UUID**: `ECUC:ebc4ec8f-9bcc-4284-befa-fda296bc41b1`
- **参数名**: `XcpMaxOdtEntries`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter indicates the maximum amount of entries in an ODT of this DAQ list (STATIC configuration).

####### ENUMERATION 类型参数

######## 1. XcpDaqListType

- **UUID**: `ECUC:46551e77-32e5-401c-bb0c-415619f1109a`
- **参数名**: `XcpDaqListType`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `DAQ` (来源: AUTOSAR_ECUC)
  - `DAQ_STIM` (来源: AUTOSAR_ECUC)
  - `STIM` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This indicates whether this DAQ list represents a DAQ or a STIM.

###### 配置容器

本模块包含 **3** 个配置容器：

####### 1. XcpDto

**容器属性**:

- **UUID**: `ECUC:60a6ecc4-2b81-4fe9-89d8-d37b7abbabc6`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `XcpDto`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

This container collects data transfer object specific parameters for the DAQ list.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. XcpDtoPid

- **UUID**: `ECUC:ab9cfb60-f4fb-4f29-bd2d-3bd3567225cc`
- **参数名**: `XcpDtoPid`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..251]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Packet identifier (PID) of the DTO that identifies the ODT the content of the DTO.

######## 引用关系

此容器包含 **1** 个引用：

######### CHOICE-REFERENCE 类型引用

########## 1. XcpDto2PduMapping

- **UUID**: `ECUC:1f98cbe3-d6bd-44c7-9575-68f54b302fc7`
- **引用名**: `XcpDto2PduMapping`
- **引用类型**: CHOICE-REFERENCE
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **目标引用列表**:
  - `/AUTOSAR/EcucDefs/Xcp/XcpConfig/XcpPdu/XcpRxPdu`
  - `/AUTOSAR/EcucDefs/Xcp/XcpConfig/XcpPdu/XcpTxPdu`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This reference specifies the mapping of the DTO to the PDUs from the lower-layer interfaces (CanIf, FrIf, SoAd and Cdd).

####### 2. XcpOdt

**容器属性**:

- **UUID**: `ECUC:2819db23-acc0-43fe-b4d5-89a6c424aa8d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `XcpOdt`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

This container contains ODT-specific parameter for the DAQ list.

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. XcpOdtEntryMaxSize

- **UUID**: `ECUC:2bb441f0-5e50-4b64-b973-c2274d28fa27`
- **参数名**: `XcpOdtEntryMaxSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..254]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter indicates the upper limit for the size of the element described by an ODT entry. Depending on the DaqListType this ODT belongs to it describes the limit for a DAQ (MAX_ODT_ENTRY_SIZE_DAQ) or a STIM (MAX_ODT_ENTRY_SIZE_STIM).

########## 2. XcpOdtNumber

- **UUID**: `ECUC:5c11368f-1932-4c78-9f9d-e1fef07a1bde`
- **参数名**: `XcpOdtNumber`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..251]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Index number of this ODT within the DAQ list.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. XcpOdt2DtoMapping

- **UUID**: `ECUC:c459aaa3-a782-4d24-b295-566b3252232a`
- **引用名**: `XcpOdt2DtoMapping`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `XcpDto`
- **完整路径**: `/AUTOSAR/EcucDefs/Xcp/XcpConfig/XcpDaqList/XcpDto`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This reference maps the ODT to the according DTO in which it will be transmitted.

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. XcpOdtEntry

**容器属性**:

- **UUID**: `ECUC:ab97e61f-e5dc-480b-ae85-b565dfbe5e6f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `XcpOdtEntry`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

This container collects all configuration parameters that comprise an ODT entry.

########## 参数配置

此容器包含 **3** 个参数：

########### INTEGER 类型参数

############ 1. XcpOdtEntryLength

- **UUID**: `ECUC:6f0e3297-da74-46cb-9070-ee5f6849d6be`
- **参数名**: `XcpOdtEntryLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Length of the referenced memory area that is referenced by the ODT entry.

############ 2. XcpOdtEntryNumber

- **UUID**: `ECUC:7276d244-9830-468e-bd5d-645648bf4ade`
- **参数名**: `XcpOdtEntryNumber`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..254]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Index number of the ODT entry

########### LINKER-SYMBOL 类型参数

############ 1. XcpOdtEntryAddress

- **UUID**: `ECUC:7e348e20-5489-4222-8de0-d3a2c9bb8410`
- **参数名**: `XcpOdtEntryAddress`
- **数据类型**: LINKER-SYMBOL
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Memory address that the ODT entry is referencing to.

####### 3. XcpOdtEntry

**容器属性**:

- **UUID**: `ECUC:ab97e61f-e5dc-480b-ae85-b565dfbe5e6f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `XcpOdtEntry`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

This container collects all configuration parameters that comprise an ODT entry.

######## 参数配置

此容器包含 **3** 个参数：

######### INTEGER 类型参数

########## 1. XcpOdtEntryLength

- **UUID**: `ECUC:6f0e3297-da74-46cb-9070-ee5f6849d6be`
- **参数名**: `XcpOdtEntryLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Length of the referenced memory area that is referenced by the ODT entry.

########## 2. XcpOdtEntryNumber

- **UUID**: `ECUC:7276d244-9830-468e-bd5d-645648bf4ade`
- **参数名**: `XcpOdtEntryNumber`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..254]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Index number of the ODT entry

######### LINKER-SYMBOL 类型参数

########## 1. XcpOdtEntryAddress

- **UUID**: `ECUC:7e348e20-5489-4222-8de0-d3a2c9bb8410`
- **参数名**: `XcpOdtEntryAddress`
- **数据类型**: LINKER-SYMBOL
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Memory address that the ODT entry is referencing to.

##### 3. XcpDto

**容器属性**:

- **UUID**: `ECUC:60a6ecc4-2b81-4fe9-89d8-d37b7abbabc6`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `XcpDto`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

This container collects data transfer object specific parameters for the DAQ list.

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. XcpDtoPid

- **UUID**: `ECUC:ab9cfb60-f4fb-4f29-bd2d-3bd3567225cc`
- **参数名**: `XcpDtoPid`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..251]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Packet identifier (PID) of the DTO that identifies the ODT the content of the DTO.

###### 引用关系

此容器包含 **1** 个引用：

####### CHOICE-REFERENCE 类型引用

######## 1. XcpDto2PduMapping

- **UUID**: `ECUC:1f98cbe3-d6bd-44c7-9575-68f54b302fc7`
- **引用名**: `XcpDto2PduMapping`
- **引用类型**: CHOICE-REFERENCE
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **目标引用列表**:
  - `/AUTOSAR/EcucDefs/Xcp/XcpConfig/XcpPdu/XcpRxPdu`
  - `/AUTOSAR/EcucDefs/Xcp/XcpConfig/XcpPdu/XcpTxPdu`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This reference specifies the mapping of the DTO to the PDUs from the lower-layer interfaces (CanIf, FrIf, SoAd and Cdd).

##### 4. XcpOdt

**容器属性**:

- **UUID**: `ECUC:2819db23-acc0-43fe-b4d5-89a6c424aa8d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `XcpOdt`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

This container contains ODT-specific parameter for the DAQ list.

###### 参数配置

此容器包含 **2** 个参数：

####### INTEGER 类型参数

######## 1. XcpOdtEntryMaxSize

- **UUID**: `ECUC:2bb441f0-5e50-4b64-b973-c2274d28fa27`
- **参数名**: `XcpOdtEntryMaxSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..254]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter indicates the upper limit for the size of the element described by an ODT entry. Depending on the DaqListType this ODT belongs to it describes the limit for a DAQ (MAX_ODT_ENTRY_SIZE_DAQ) or a STIM (MAX_ODT_ENTRY_SIZE_STIM).

######## 2. XcpOdtNumber

- **UUID**: `ECUC:5c11368f-1932-4c78-9f9d-e1fef07a1bde`
- **参数名**: `XcpOdtNumber`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..251]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Index number of this ODT within the DAQ list.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. XcpOdt2DtoMapping

- **UUID**: `ECUC:c459aaa3-a782-4d24-b295-566b3252232a`
- **引用名**: `XcpOdt2DtoMapping`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `XcpDto`
- **完整路径**: `/AUTOSAR/EcucDefs/Xcp/XcpConfig/XcpDaqList/XcpDto`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This reference maps the ODT to the according DTO in which it will be transmitted.

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. XcpOdtEntry

**容器属性**:

- **UUID**: `ECUC:ab97e61f-e5dc-480b-ae85-b565dfbe5e6f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `XcpOdtEntry`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

This container collects all configuration parameters that comprise an ODT entry.

######## 参数配置

此容器包含 **3** 个参数：

######### INTEGER 类型参数

########## 1. XcpOdtEntryLength

- **UUID**: `ECUC:6f0e3297-da74-46cb-9070-ee5f6849d6be`
- **参数名**: `XcpOdtEntryLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Length of the referenced memory area that is referenced by the ODT entry.

########## 2. XcpOdtEntryNumber

- **UUID**: `ECUC:7276d244-9830-468e-bd5d-645648bf4ade`
- **参数名**: `XcpOdtEntryNumber`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..254]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Index number of the ODT entry

######### LINKER-SYMBOL 类型参数

########## 1. XcpOdtEntryAddress

- **UUID**: `ECUC:7e348e20-5489-4222-8de0-d3a2c9bb8410`
- **参数名**: `XcpOdtEntryAddress`
- **数据类型**: LINKER-SYMBOL
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Memory address that the ODT entry is referencing to.

##### 5. XcpOdtEntry

**容器属性**:

- **UUID**: `ECUC:ab97e61f-e5dc-480b-ae85-b565dfbe5e6f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `XcpOdtEntry`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

This container collects all configuration parameters that comprise an ODT entry.

###### 参数配置

此容器包含 **3** 个参数：

####### INTEGER 类型参数

######## 1. XcpOdtEntryLength

- **UUID**: `ECUC:6f0e3297-da74-46cb-9070-ee5f6849d6be`
- **参数名**: `XcpOdtEntryLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Length of the referenced memory area that is referenced by the ODT entry.

######## 2. XcpOdtEntryNumber

- **UUID**: `ECUC:7276d244-9830-468e-bd5d-645648bf4ade`
- **参数名**: `XcpOdtEntryNumber`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..254]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Index number of the ODT entry

####### LINKER-SYMBOL 类型参数

######## 1. XcpOdtEntryAddress

- **UUID**: `ECUC:7e348e20-5489-4222-8de0-d3a2c9bb8410`
- **参数名**: `XcpOdtEntryAddress`
- **数据类型**: LINKER-SYMBOL
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Memory address that the ODT entry is referencing to.

##### 6. XcpDemEventParameterRefs

**容器属性**:

- **UUID**: `ECUC:b6c92c66-4349-4301-ba59-c5ae05da15a1`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `XcpDemEventParameterRefs`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Container for the references to DemEventParameter elements which shall be invoked using the API Dem_ReportErrorStatus API in case the corresponding error occurs. The EventId is taken from the referenced DemEventParameter's DemEventId value. The standardized errors are provided in the container and can be extended by vendor specific error references.

###### 引用关系

此容器包含 **1** 个引用：

####### SYMBOLIC-NAME-REFERENCE 类型引用

######## 1. XCP_E_INIT_FAILED

- **UUID**: `ECUC:06b1ad04-a91c-4e57-8383-0e3b53757516`
- **引用名**: `XCP_E_INIT_FAILED`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `DemEventParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemConfigSet/DemEventParameter`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the DemEventParameter which shall be issued when the error "Initialization of XCP failed" has occured.

##### 7. XcpEventChannel

**容器属性**:

- **UUID**: `ECUC:799c6452-a17b-4306-9b15-2ae608d34306`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `XcpEventChannel`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

This container contains the configuration of event channels on the XCP slave.

###### 参数配置

此容器包含 **7** 个参数：

####### INTEGER 类型参数

######## 1. XcpEventChannelMaxDaqList

- **UUID**: `ECUC:a622228a-6822-44e8-b8af-e66e56182590`
- **参数名**: `XcpEventChannelMaxDaqList`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Maximum amount of DAQ lists that are handled by this event channel.

######## 2. XcpEventChannelNumber

- **UUID**: `ECUC:859fde79-24d2-4a44-9b75-e35d6266433d`
- **参数名**: `XcpEventChannelNumber`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65534]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Index number of the event channel.

######## 3. XcpEventChannelPriority

- **UUID**: `ECUC:cd8c0bb0-99a2-4896-97a0-577062bf9797`
- **参数名**: `XcpEventChannelPriority`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Priority of the event channel

######## 4. XcpEventChannelTimeCycle

- **UUID**: `ECUC:9d286dc2-0a1c-40cf-a3d7-76102b466ab5`
- **参数名**: `XcpEventChannelTimeCycle`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The event channel time cycle indicates which sampling period is used to process this event channel. A value of 0 means 'Not cyclic'.

####### ENUMERATION 类型参数

######## 1. XcpEventChannelConsistency

- **UUID**: `ECUC:634c0118-18db-48cd-9f20-fdde62d1951b`
- **参数名**: `XcpEventChannelConsistency`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `ODT`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `DAQ` (来源: AUTOSAR_ECUC)
  - `EVENT` (来源: AUTOSAR_ECUC)
  - `ODT` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Type of consistency used by event channel

######## 2. XcpEventChannelTimeUnit

- **UUID**: `ECUC:bded059d-3744-4cfe-88fc-948f0922212f`
- **参数名**: `XcpEventChannelTimeUnit`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
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
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This configuration parameter indicates the unit of the event channel time cycle.

######## 3. XcpEventChannelType

- **UUID**: `ECUC:a82678fb-fc06-4749-8c1f-39a73c6d4dbd`
- **参数名**: `XcpEventChannelType`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `DAQ`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `DAQ` (来源: AUTOSAR_ECUC)
  - `DAQ_STIM` (来源: AUTOSAR_ECUC)
  - `STIM` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This configuration parameter indicates what kind of DAQ list can be allocated to this event channel.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. XcpEventChannelTriggeredDaqListRef

- **UUID**: `ECUC:7fed113d-be4e-4d87-9ee2-405ca3bc2228`
- **引用名**: `XcpEventChannelTriggeredDaqListRef`
- **引用类型**: REFERENCE
- **多重性**: [1..infinite]
- **目标**: `XcpDaqList`
- **完整路径**: `/AUTOSAR/EcucDefs/Xcp/XcpConfig/XcpDaqList`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: References all DAQ lists that are trigged by this event channel.

##### 8. XcpRxPdu

**容器属性**:

- **UUID**: `ECUC:3b1ca421-d224-4f77-9401-4c2d5504cefa`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `XcpRxPdu`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container specifies received PDUs.

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. XcpRxPduId

- **UUID**: `ECUC:26446775-a0c3-456c-aaab-3d65cc5f8002`
- **参数名**: `XcpRxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: ID of the PDU that will be received via a Xcp_<module>RxIndication.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. XcpRxPduRef

- **UUID**: `ECUC:c6c60025-0a48-48cd-9246-2b1cdf5983e3`
- **引用名**: `XcpRxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE

##### 9. XcpTxPdu

**容器属性**:

- **UUID**: `ECUC:fb220126-dc86-4845-ba4e-a3c57370b0f9`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `XcpTxPdu`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container specifies transmission PDUs.

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. XcpTxPduId

- **UUID**: `ECUC:9f920c69-c570-4aa9-9ab1-a216fe2a1faa`
- **参数名**: `XcpTxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The PDU identifier, which has to be used by the lower layer BSW module for TxConfirmations or TriggerTransmits.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. XcpTxPduRef

- **UUID**: `ECUC:46f96041-2ea4-4e3a-96be-8380f6104b3f`
- **引用名**: `XcpTxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the external PDU definition.

##### 10. XcpGeneral

**容器属性**:

- **UUID**: `ECUC:0608a81a-a884-4042-a3e2-7c9efe4bcbb6`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `XcpGeneral`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

This container contains the general configuration parameters of the XCP.

###### 参数配置

此容器包含 **23** 个参数：

####### INTEGER 类型参数

######## 1. XcpDaqCount

- **UUID**: `ECUC:ee1e9f87-3ec9-4235-b880-56f8a8f443d8`
- **参数名**: `XcpDaqCount`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Indicates the number of DAQ lists for dynamic configuration.

######## 2. XcpMaxCto

- **UUID**: `ECUC:da8154e0-c2c7-4ced-9170-b80b4d915b39`
- **参数名**: `XcpMaxCto`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [8..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: MAX_CTO shows the maximum length of a CTO packet in bytes.

######## 3. XcpMaxDto

- **UUID**: `ECUC:9bba2e64-6ec6-461a-864a-e9a1305c2aae`
- **参数名**: `XcpMaxDto`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [8..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: MAX_DTO shows the maximum length of a DTO packet in bytes.

######## 4. XcpMaxEventChannel

- **UUID**: `ECUC:46c1cd21-e9b3-441e-bd54-a895a123058a`
- **参数名**: `XcpMaxEventChannel`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE

######## 5. XcpMinDaq

- **UUID**: `ECUC:2fd82b37-993a-4bf0-8ecf-6e5e6979afe5`
- **参数名**: `XcpMinDaq`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Indicates the number of predefined, read only DAQ lists on the XCP slave.

######## 6. XcpOdtCount

- **UUID**: `ECUC:976675c2-924a-4c91-ac6d-f66be706c836`
- **参数名**: `XcpOdtCount`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..252]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter indicates the amount of ODTs of a DAQ list using dynamic DAQ list configuration.

######## 7. XcpOdtEntriesCount

- **UUID**: `ECUC:80f7ce3f-9c9e-4c45-897a-1269f7c00318`
- **参数名**: `XcpOdtEntriesCount`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Indicates the amount of entries into an ODT using dynamic DAQ list configuration.

######## 8. XcpOdtEntrySizeDaq

- **UUID**: `ECUC:a1b46c84-b22d-47d5-abd0-95c4c5bae6e1`
- **参数名**: `XcpOdtEntrySizeDaq`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Indicates the size of an element described by an ODT entry to the DaqListType for a DAQ.

######## 9. XcpOdtEntrySizeStim

- **UUID**: `ECUC:1f126b22-d6db-40ff-a510-1439be550890`
- **参数名**: `XcpOdtEntrySizeStim`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Indicates the size of an element described by an ODT entry to the DaqListType for a stim.

######## 10. XcpTimestampTicks

- **UUID**: `ECUC:0a93cd9a-1ee7-4c63-971c-ae1defcba01f`
- **参数名**: `XcpTimestampTicks`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the timestamp that will increment based TIMESTAMP_TICKS per unit and wrap around if an overflow occurs.

####### BOOLEAN 类型参数

######## 1. XcpDevErrorDetect

- **UUID**: `ECUC:a542355f-3504-4425-8983-3a8de84b6401`
- **参数名**: `XcpDevErrorDetect`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Switches the Development Error Detection and Notification on or off.

######## 2. XcpOnCanEnabled

- **UUID**: `ECUC:2b0c9251-3232-49af-8256-36a72650ff5b`
- **参数名**: `XcpOnCanEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enabling of XCPonCAN functionality

######## 3. XcpOnCddEnabled

- **UUID**: `ECUC:79c5dea3-b6eb-4435-90c1-ccba87b174ed`
- **参数名**: `XcpOnCddEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enabling of XCPonCdd functionality

######## 4. XcpOnEthernetEnabled

- **UUID**: `ECUC:d1dc33e5-893f-4f37-b4a3-0327b5c0f801`
- **参数名**: `XcpOnEthernetEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enabling of XCPonEthernet functionality

######## 5. XcpOnFlexRayEnabled

- **UUID**: `ECUC:cad19cc2-c7f1-43a7-adf0-e5645ff613f3`
- **参数名**: `XcpOnFlexRayEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enabling of XCPonFlexRay functionality

######## 6. XcpPrescalerSupported

- **UUID**: `ECUC:5918fe83-fb99-4aa8-87ae-9685cf376a51`
- **参数名**: `XcpPrescalerSupported`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter enables and disables the support for Prescaler support. True is Enabled, False is disabled

######## 7. XcpSuppressTxSupport

- **UUID**: `ECUC:ab4d5e08-c0d7-441d-b2b8-f8f53621014a`
- **参数名**: `XcpSuppressTxSupport`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Switches the support of suppressing transmission of PDUs per communication channel on or off.

######## 8. XcpVersionInfoApi

- **UUID**: `ECUC:c08055db-ac34-4cff-a83b-b02b7e24d283`
- **参数名**: `XcpVersionInfoApi`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enables/disables the existence of the XCP_GetVersionInfo() API service.

####### FLOAT 类型参数

######## 1. XcpMainFunctionPeriod

- **UUID**: `ECUC:06c1bef6-3ae3-421b-a15c-771588c35a46`
- **参数名**: `XcpMainFunctionPeriod`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0..Inf]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The XCP does not require this information but the BSW scheduler, which invokes the main function, needs it in order to plan its tasks.

####### ENUMERATION 类型参数

######## 1. XcpDaqConfigType

- **UUID**: `ECUC:cb603f68-ba20-4411-9aa6-37b4a13e2f6d`
- **参数名**: `XcpDaqConfigType`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `DAQ_DYNAMIC` (来源: AUTOSAR_ECUC)
  - `DAQ_STATIC` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Sets the DAQ_CONFIG_TYPE bit within the DAQ_PROPERTIES parameter to "static" or to "dynamic". If DAQ_STATIC is selected, the DAQ_CONFIG_TYPE bit is set to "0". If DAQ_DYNAMIC is selected, the DAQ_CONFIG_TYPE bit is set to "1".

######## 2. XcpIdentificationFieldType

- **UUID**: `ECUC:e3448e52-4e2f-46eb-a665-0f89d0db5293`
- **参数名**: `XcpIdentificationFieldType`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `ABSOLUTE` (来源: AUTOSAR_ECUC)
  - `RELATIVE_BYTE` (来源: AUTOSAR_ECUC)
  - `RELATIVE_WORD` (来源: AUTOSAR_ECUC)
  - `RELATIVE_WORD_ALIGNED` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Type of Identification Field the slave will use when transferring DAQ Packets to the master. The master has to use the same Type of Identification Field when transferring STIM Packets to the slave.

######## 3. XcpTimestampType

- **UUID**: `ECUC:62430caa-6294-48d1-adc4-7b6a99e20631`
- **参数名**: `XcpTimestampType`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `FOUR_BYTE` (来源: AUTOSAR_ECUC)
  - `NO_TIME_STAMP` (来源: AUTOSAR_ECUC)
  - `ONE_BYTE` (来源: AUTOSAR_ECUC)
  - `TWO_BYTE` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter indicates the number of bytes used for the timestamp field. In case No_TIME_STAMP is selected the timestamp field is not available.

######## 4. XcpTimestampUnit

- **UUID**: `ECUC:2fb83f31-5a33-4e5c-9db9-7e3c9b3fdf2c`
- **参数名**: `XcpTimestampUnit`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
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
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter indicates the resolution of the data acquisition clock of the slave when transferring data to master.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. XcpCounterRef

- **UUID**: `ECUC:1f49a0bc-99e1-4702-bb6e-3812d811a3b1`
- **引用名**: `XcpCounterRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `OsCounter`
- **完整路径**: `/AUTOSAR/EcucDefs/Os/OsCounter`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter contains a reference to the counter, which is used by XCP.

##### 11. XcpPdu

**容器属性**:

- **UUID**: `ECUC:3261f87c-0cbf-488c-b716-b4f93003f974`
- **容器类型**: CHOICE-CONTAINER
- **容器名称**: `XcpPdu`
- **多重性**: [1..infinite]

**容器选择**:

- **XcpRxPdu**
  - UUID: `ECUC:3b1ca421-d224-4f77-9401-4c2d5504cefa`
  - 描述: This container specifies received PDUs.
- **XcpTxPdu**
  - UUID: `ECUC:fb220126-dc86-4845-ba4e-a3c57370b0f9`
  - 描述: This container specifies transmission PDUs.

**容器描述**:

Contains PDU information. A PDU may be either a transmission PDU or a reception PDU.

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

1. **Xcp**
