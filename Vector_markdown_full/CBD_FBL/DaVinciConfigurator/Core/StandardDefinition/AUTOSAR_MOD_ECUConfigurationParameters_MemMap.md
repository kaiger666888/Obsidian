# MemMap - 完整配置文档

*此文档由ARXML文件自动生成，采用层次化结构展示*

**生成时间**: 2025-06-16 14:48:53

## 📑 目录

- [📄 文件信息](#-文件信息)
- [🔧 模块定义](#-模块定义)
  - [MemMap](#memmap)
- [📦 包结构](#-包结构)

## 📄 文件信息

### Schema信息
- **Schema位置**: `http://autosar.org/schema/r4.0 AUTOSAR_4-0-3.xsd`
- **命名空间**: `http://autosar.org/schema/r4.0`

## 🔧 模块定义

### 1. MemMap

#### 基本信息

- **UUID**: `ECUC:aa31b7a8-b524-4c87-be84-43fca3822c12`
- **模块名称**: `MemMap`
- **多重性**: [0..1]
- **支持的变体**:
  - VARIANT-PRE-COMPILE

#### 模块描述

Configuration of the MemMap module.

#### 版本历史

共有 **1** 个版本记录：

##### 1. 版本 4.2.0

- **发布日期**: 2011-11-09
- **发布者**: AUTOSAR

*此版本无详细变更记录*

#### 配置容器

本模块包含 **5** 个配置容器：

##### 1. MemMapAddressingModeSet

**容器属性**:

- **UUID**: `ECUC:b9a29699-350e-4955-b78e-47f569142ad4`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `MemMapAddressingModeSet`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

Defines a set of addressing modes which might apply to a SwAddrMethod.

###### 参数配置

此容器包含 **4** 个参数：

####### STRING 类型参数

######## 1. MemMapSupportedAddressingMethodOption

- **UUID**: `ECUC:6d1ca67a-194a-4573-9f95-2fb64da2384c`
- **参数名**: `MemMapSupportedAddressingMethodOption`
- **数据类型**: STRING
- **多重性**: [0..infinite]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
  - 正则表达式: `[a-zA-Z]([a-zA-Z0-9]|_[a-zA-Z0-9])*_?`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This constrains the usage of this addressing mode set for Generic Mappings to swAddrMethods.

######## 2. MemMapSupportedSectionInitializationPolicy

- **UUID**: `ECUC:e907ccf6-062e-43b1-babf-99bb412f2a9e`
- **参数名**: `MemMapSupportedSectionInitializationPolicy`
- **数据类型**: STRING
- **多重性**: [0..infinite]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This constrains the usage of this addressing mode set for Generic Mappings to swAddrMethods.

####### ENUMERATION 类型参数

######## 1. MemMapSupportedMemoryAllocationKeywordPolicy

- **UUID**: `ECUC:f71b072d-046d-478f-9ccb-e3e9316d5d3c`
- **参数名**: `MemMapSupportedMemoryAllocationKeywordPolicy`
- **数据类型**: ENUMERATION
- **多重性**: [0..infinite]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `MEMMAP_ALLOCATION_KEYWORD_POLICY_ADDR_METHOD_SHORT_NAME` (来源: AUTOSAR_ECUC)
  - `MEMMAP_ALLOCATION_KEYWORD_POLICY_ADDR_METHOD_SHORT_NAME_AND_ALIGNMENT` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This constrains the usage of this addressing mode set for Generic Mappings to swAddrMethods.

######## 2. MemMapSupportedSectionType

- **UUID**: `ECUC:3c77ff1c-dee1-49ea-a4d9-33f3f3f2805a`
- **参数名**: `MemMapSupportedSectionType`
- **数据类型**: ENUMERATION
- **多重性**: [0..infinite]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `MEMMAP_SECTION_TYPE_CALIBRATION_OFFLINE` (来源: AUTOSAR_ECUC)
  - `MEMMAP_SECTION_TYPE_CALIBRATION_ONLINE` (来源: AUTOSAR_ECUC)
  - `MEMMAP_SECTION_TYPE_CAL_PRM` (来源: AUTOSAR_ECUC)
  - `MEMMAP_SECTION_TYPE_CODE` (来源: AUTOSAR_ECUC)
  - `MEMMAP_SECTION_TYPE_CONFIG_DATA` (来源: AUTOSAR_ECUC)
  - `MEMMAP_SECTION_TYPE_CONST` (来源: AUTOSAR_ECUC)
  - `MEMMAP_SECTION_TYPE_EXCLUDE_FROM_FLASH` (来源: AUTOSAR_ECUC)
  - `MEMMAP_SECTION_TYPE_USER_DEFINED` (来源: AUTOSAR_ECUC)
  - `MEMMAP_SECTION_TYPE_VAR` (来源: AUTOSAR_ECUC)
  - `MEMMAP_SECTION_TYPE_VAR_FAST` (来源: AUTOSAR_ECUC)
  - `MEMMAP_SECTION_TYPE_VAR_NO_INIT` (来源: AUTOSAR_ECUC)
  - `MEMMAP_SECTION_TYPE_VAR_POWER_ON_INIT` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This constrains the usage of this addressing mode set for Generic Mappings to swAddrMethods.

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. MemMapAddressingMode

**容器属性**:

- **UUID**: `ECUC:80bfe9ef-b7fc-4b51-8dd1-dab1ae3fbeed`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `MemMapAddressingMode`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

Defines a addressing mode with a set of #pragma statements implementing the start and the stop of a section.

######## 参数配置

此容器包含 **3** 个参数：

######### STRING 类型参数

########## 1. MemMapAlignmentSelector

- **UUID**: `ECUC:cc847254-326c-445f-9df8-7548068d871c`
- **参数名**: `MemMapAlignmentSelector`
- **数据类型**: STRING
- **多重性**: [1..infinite]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
  - 正则表达式: `[1-9][0-9]*|0x[0-9a-f]*|0[0-7]*|0b[0-1]*|UNSPECIFIED|UNKNOWN|BOOLEAN|`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines a the alignments for which the MemMapAddressingMode applies.

######### MULTILINE-STRING 类型参数

########## 1. MemMapAddressingModeStart

- **UUID**: `ECUC:9cd47499-3661-462d-81fb-beb77b4eda67`
- **参数名**: `MemMapAddressingModeStart`
- **数据类型**: MULTILINE-STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **多行字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines a set of #pragma statements implementing the start of a section.

########## 2. MemMapAddressingModeStop

- **UUID**: `ECUC:0976b2a0-8e41-4457-9636-eace58400036`
- **参数名**: `MemMapAddressingModeStop`
- **数据类型**: MULTILINE-STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **多行字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines a set of #pragma statements implementing the start of a section.

##### 2. MemMapAddressingMode

**容器属性**:

- **UUID**: `ECUC:80bfe9ef-b7fc-4b51-8dd1-dab1ae3fbeed`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `MemMapAddressingMode`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

Defines a addressing mode with a set of #pragma statements implementing the start and the stop of a section.

###### 参数配置

此容器包含 **3** 个参数：

####### STRING 类型参数

######## 1. MemMapAlignmentSelector

- **UUID**: `ECUC:cc847254-326c-445f-9df8-7548068d871c`
- **参数名**: `MemMapAlignmentSelector`
- **数据类型**: STRING
- **多重性**: [1..infinite]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
  - 正则表达式: `[1-9][0-9]*|0x[0-9a-f]*|0[0-7]*|0b[0-1]*|UNSPECIFIED|UNKNOWN|BOOLEAN|`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines a the alignments for which the MemMapAddressingMode applies.

####### MULTILINE-STRING 类型参数

######## 1. MemMapAddressingModeStart

- **UUID**: `ECUC:9cd47499-3661-462d-81fb-beb77b4eda67`
- **参数名**: `MemMapAddressingModeStart`
- **数据类型**: MULTILINE-STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **多行字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines a set of #pragma statements implementing the start of a section.

######## 2. MemMapAddressingModeStop

- **UUID**: `ECUC:0976b2a0-8e41-4457-9636-eace58400036`
- **参数名**: `MemMapAddressingModeStop`
- **数据类型**: MULTILINE-STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **多行字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines a set of #pragma statements implementing the start of a section.

##### 3. MemMapAllocation

**容器属性**:

- **UUID**: `ECUC:db0cbfa5-d86b-407d-acfa-64a436b1f94d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `MemMapAllocation`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

Defines a set of addressing modes which might apply to a SwAddrMethod.

###### 配置容器

本模块包含 **2** 个配置容器：

####### 1. MemMapGenericMapping

**容器属性**:

- **UUID**: `ECUC:ab992de3-97d5-42b4-8493-2f5be2bc7a30`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `MemMapGenericMapping`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

Defines which SwAddrMethod is implemented with which MemMapAddressingModeSet.

######## 引用关系

此容器包含 **2** 个引用：

######### REFERENCE 类型引用

########## 1. MemMapAddressingModeSetRef

- **UUID**: `ECUC:9b2ed32c-df97-4ae7-8430-3b3adf225003`
- **引用名**: `MemMapAddressingModeSetRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `MemMapAddressingModeSet`
- **完整路径**: `/AUTOSAR/EcucDefs/MemMap/MemMapAddressingModeSet`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the MemMapAddressingModeSet which applies to the MemMapGenericMapping.

######### FOREIGN-REFERENCE 类型引用

########## 1. MemMapSwAddressMethodRef

- **UUID**: `ECUC:ce703d4e-b826-4ecf-a296-9f53d2a913eb`
- **引用名**: `MemMapSwAddressMethodRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [1..1]
- **目标类型**: SW-ADDR-METHOD
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the SwAddrMethod which applies to the MemMapGenericMapping.

####### 2. MemMapSectionSpecificMapping

**容器属性**:

- **UUID**: `ECUC:b1dc433b-fdcc-4d9e-8c1b-2b185aeeab21`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `MemMapSectionSpecificMapping`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

Defines which MemorySection of a BSW Module or a Software Component is implemented with which MemMapAddressingModeSet.

######## 引用关系

此容器包含 **2** 个引用：

######### REFERENCE 类型引用

########## 1. MemMapAddressingModeSetRef

- **UUID**: `ECUC:557c3f43-7697-4644-a538-eca0f577ef55`
- **引用名**: `MemMapAddressingModeSetRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `MemMapAddressingModeSet`
- **完整路径**: `/AUTOSAR/EcucDefs/MemMap/MemMapAddressingModeSet`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the MemMapAddressingModeSet which applies to the MemMapModuleSectionSpecificMapping.

######### FOREIGN-REFERENCE 类型引用

########## 1. MemMapMemorySectionRef

- **UUID**: `ECUC:028cc5c2-4681-4e77-8873-03c4af2327b9`
- **引用名**: `MemMapMemorySectionRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [1..1]
- **目标类型**: MEMORY-SECTION
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the MemorySection which applies to the MemMapSectionSpecificMapping.

##### 4. MemMapGenericMapping

**容器属性**:

- **UUID**: `ECUC:ab992de3-97d5-42b4-8493-2f5be2bc7a30`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `MemMapGenericMapping`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

Defines which SwAddrMethod is implemented with which MemMapAddressingModeSet.

###### 引用关系

此容器包含 **2** 个引用：

####### REFERENCE 类型引用

######## 1. MemMapAddressingModeSetRef

- **UUID**: `ECUC:9b2ed32c-df97-4ae7-8430-3b3adf225003`
- **引用名**: `MemMapAddressingModeSetRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `MemMapAddressingModeSet`
- **完整路径**: `/AUTOSAR/EcucDefs/MemMap/MemMapAddressingModeSet`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the MemMapAddressingModeSet which applies to the MemMapGenericMapping.

####### FOREIGN-REFERENCE 类型引用

######## 1. MemMapSwAddressMethodRef

- **UUID**: `ECUC:ce703d4e-b826-4ecf-a296-9f53d2a913eb`
- **引用名**: `MemMapSwAddressMethodRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [1..1]
- **目标类型**: SW-ADDR-METHOD
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the SwAddrMethod which applies to the MemMapGenericMapping.

##### 5. MemMapSectionSpecificMapping

**容器属性**:

- **UUID**: `ECUC:b1dc433b-fdcc-4d9e-8c1b-2b185aeeab21`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `MemMapSectionSpecificMapping`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

Defines which MemorySection of a BSW Module or a Software Component is implemented with which MemMapAddressingModeSet.

###### 引用关系

此容器包含 **2** 个引用：

####### REFERENCE 类型引用

######## 1. MemMapAddressingModeSetRef

- **UUID**: `ECUC:557c3f43-7697-4644-a538-eca0f577ef55`
- **引用名**: `MemMapAddressingModeSetRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `MemMapAddressingModeSet`
- **完整路径**: `/AUTOSAR/EcucDefs/MemMap/MemMapAddressingModeSet`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the MemMapAddressingModeSet which applies to the MemMapModuleSectionSpecificMapping.

####### FOREIGN-REFERENCE 类型引用

######## 1. MemMapMemorySectionRef

- **UUID**: `ECUC:028cc5c2-4681-4e77-8873-03c4af2327b9`
- **引用名**: `MemMapMemorySectionRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [1..1]
- **目标类型**: MEMORY-SECTION
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the MemorySection which applies to the MemMapSectionSpecificMapping.

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

1. **MemMap**
