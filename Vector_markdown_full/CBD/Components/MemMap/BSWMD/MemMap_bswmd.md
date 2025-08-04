# MemMap - 完整配置文档

*此文档由ARXML文件自动生成，采用层次化结构展示*

**生成时间**: 2025-06-16 14:45:20

## 📑 目录

- [📄 文件信息](#-文件信息)
- [🔧 模块定义](#-模块定义)
  - [MemMap](#memmap)
- [📦 包结构](#-包结构)
- [⚡ 实现信息](#-实现信息)

## 📄 文件信息

### Schema信息
- **Schema位置**: `http://autosar.org/schema/r4.0 AUTOSAR_00048.xsd`
- **命名空间**: `http://autosar.org/schema/r4.0`

## 🔧 模块定义

### 1. MemMap

#### 基本信息

- **UUID**: `65ce0432-95ea-4cf4-83a3-4f7c4eb0d2be`
- **模块名称**: `MemMap`
- **类别**: `VENDOR_SPECIFIC_MODULE_DEFINITION`
- **多重性**: [0..1]
- **支持的变体**:
  - VARIANT-PRE-COMPILE

#### 模块描述

The Memory Mapping (MemMap) module is used to generate memory mapping
header files for BSW modules as well as SWCs. These files control
the assigment of code, constants and variables to linker sections.
#Memory #MemoryMapping
#AUTOSAR

#### 版本历史

共有 **11** 个版本记录：

##### 1. 版本 1.0.0

- **状态**: released
- **发布日期**: 2021-02-11
- **发布者**: virleh

**变更内容**:

##### 2. 版本 1.0.1

- **状态**: released
- **发布日期**: 2021-02-15
- **发布者**: virleh

**变更内容**:

##### 3. 版本 1.1.0

- **状态**: released
- **发布日期**: 2021-03-18
- **发布者**: virbse

**变更内容**:

##### 4. 版本 1.2.0

- **状态**: released
- **发布日期**: 2021-04-09
- **发布者**: virleh

**变更内容**:

##### 5. 版本 1.3.0

- **状态**: released
- **发布日期**: 2021-05-12
- **发布者**: virleh

**变更内容**:

##### 6. 版本 1.4.0

- **状态**: released
- **发布日期**: 2021-08-30
- **发布者**: virbse

**变更内容**:

##### 7. 版本 1.5.0

- **状态**: released
- **发布日期**: 2021-11-24
- **发布者**: virleh, visdqk

**变更内容**:

##### 8. 版本 1.6.0

- **状态**: released
- **发布日期**: 2022-08-26
- **发布者**: virleh

**变更内容**:

##### 9. 版本 1.7.0

- **状态**: released
- **发布日期**: 2023-12-08
- **发布者**: asaleh

**变更内容**:

##### 10. 版本 1.8.0

- **状态**: released
- **发布日期**: 2024-06-03
- **发布者**: twurm

**变更内容**:

##### 11. 版本 1.8.1

- **状态**: released
- **发布日期**: 2024-06-07T08:39:22+02:00
- **发布者**: visdqk

**变更内容**:

#### 配置容器

本模块包含 **11** 个配置容器：

##### 1. MemMapAddressingModeSet

**容器属性**:

- **UUID**: `2b4c4db6-7a1e-425f-bebf-b29d782d6181`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `MemMapAddressingModeSet`
- **多重性**: [0..infinite]
- **需要索引**: false

**容器描述**:

Defines a set of addressing modes which might apply to a SwAddrMethod.

###### 参数配置

此容器包含 **5** 个参数：

####### STRING 类型参数

######## 1. MemMapCompilerMemClassSymbolImpl

- **UUID**: `f226f47a-1123-4d6f-8ccf-b9a9180821d4`
- **参数名**: `MemMapCompilerMemClassSymbolImpl`
- **数据类型**: STRING
- **多重性**: [1..1]
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Defines the implementation behind a MemClassSymbol and configures the Compiler Abstraction.

Note: Parameter not used.

######## 2. MemMapSupportedAddressingMethodOption

- **UUID**: `8f8156f6-5d14-4304-966c-9f662d403644`
- **参数名**: `MemMapSupportedAddressingMethodOption`
- **数据类型**: STRING
- **多重性**: [0..infinite]
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: This constrains the usage of this addressing mode set for Generic Mappings to swAddrMethods.

######## 3. MemMapSupportedSectionInitializationPolicy

- **UUID**: `57ba786b-ce64-40e2-a37f-50299bc284a9`
- **参数名**: `MemMapSupportedSectionInitializationPolicy`
- **数据类型**: STRING
- **多重性**: [0..infinite]
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: This constrains the usage of this addressing mode set for Generic Mappings to swAddrMethods.

####### ENUMERATION 类型参数

######## 1. MemMapSupportedMemoryAllocationKeywordPolicy

- **UUID**: `f8850fc8-3a52-4256-991f-a93c45c8b7a3`
- **参数名**: `MemMapSupportedMemoryAllocationKeywordPolicy`
- **数据类型**: ENUMERATION
- **多重性**: [0..infinite]
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `MEMMAP_ALLOCATION_KEYWORD_POLICY_ADDR_METHOD_SHORT_NAME` (来源: AUTOSAR_ECUC)
  - `MEMMAP_ALLOCATION_KEYWORD_POLICY_ADDR_METHOD_SHORT_NAME_AND_ALIGNMENT` (来源: AUTOSAR_ECUC)
- **描述**: This constrains the usage of this addressing mode set for Generic Mappings to swAddrMethods.

######## 2. MemMapSupportedSectionType

- **UUID**: `2ac58bbb-8191-4e29-9837-dd9589271380`
- **参数名**: `MemMapSupportedSectionType`
- **数据类型**: ENUMERATION
- **多重性**: [0..infinite]
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `MEMMAP_SECTION_TYPE_CAL_PRM` (来源: AUTOSAR_ECUC)
  - `MEMMAP_SECTION_TYPE_CODE` (来源: AUTOSAR_ECUC)
  - `MEMMAP_SECTION_TYPE_CONFIG_DATA` (来源: AUTOSAR_ECUC)
  - `MEMMAP_SECTION_TYPE_CONST` (来源: AUTOSAR_ECUC)
  - `MEMMAP_SECTION_TYPE_EXCLUDE_FROM_FLASH` (来源: AUTOSAR_ECUC)
  - `MEMMAP_SECTION_TYPE_VAR` (来源: AUTOSAR_ECUC)
- **描述**: This constrains the usage of this addressing mode set for Generic Mappings to swAddrMethods.

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. MemMapAddressingMode

**容器属性**:

- **UUID**: `070de036-4368-4f78-a22a-0253cde47f19`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `MemMapAddressingMode`
- **多重性**: [1..infinite]
- **需要索引**: false

**容器描述**:

Defines a addressing mode with a set of #pragma statements implementing the start and the stop of a section.

######## 参数配置

此容器包含 **3** 个参数：

######### STRING 类型参数

########## 1. MemMapAlignmentSelector

- **UUID**: `a82bc154-9cea-4f41-866e-490878cd8353`
- **参数名**: `MemMapAlignmentSelector`
- **数据类型**: STRING
- **多重性**: [1..infinite]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Defines a the alignments for which the MemMapAddressingMode applies.

######### MULTILINE-STRING 类型参数

########## 1. MemMapAddressingModeStart

- **UUID**: `9c50f2d3-2e9b-4b6e-b78c-0733ad0530a3`
- **参数名**: `MemMapAddressingModeStart`
- **数据类型**: MULTILINE-STRING
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Defines a set of #pragma statements implementing the start of a section.

########## 2. MemMapAddressingModeStop

- **UUID**: `245a8056-3345-4a29-b6e5-a5f762568004`
- **参数名**: `MemMapAddressingModeStop`
- **数据类型**: MULTILINE-STRING
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Defines a set of #pragma statements implementing the start of a section.

######## 引用关系

此容器包含 **1** 个引用：

######### CHOICE-REFERENCE 类型引用

########## 1. MemMapLinkerLogicalGroupRef

- **UUID**: `30c28846-f675-4ffc-b64a-f72ce89a5723`
- **引用名**: `MemMapLinkerLogicalGroupRef`
- **引用类型**: CHOICE-REFERENCE
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **需要索引**: false
- **目标引用列表**:
  - `/MICROSAR/vLinkGen/vLinkGenMemLayout/vLinkGenLogicalConstGroup`
  - `/MICROSAR/vLinkGen/vLinkGenMemLayout/vLinkGenLogicalVarGroup`
- **描述**: Reference to the vLinkGen logical group to which the MemMapAddressingMode should map.
This reference is required for the automatic pragma generation.

##### 2. MemMapAddressingMode

**容器属性**:

- **UUID**: `070de036-4368-4f78-a22a-0253cde47f19`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `MemMapAddressingMode`
- **多重性**: [1..infinite]
- **需要索引**: false

**容器描述**:

Defines a addressing mode with a set of #pragma statements implementing the start and the stop of a section.

###### 参数配置

此容器包含 **3** 个参数：

####### STRING 类型参数

######## 1. MemMapAlignmentSelector

- **UUID**: `a82bc154-9cea-4f41-866e-490878cd8353`
- **参数名**: `MemMapAlignmentSelector`
- **数据类型**: STRING
- **多重性**: [1..infinite]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Defines a the alignments for which the MemMapAddressingMode applies.

####### MULTILINE-STRING 类型参数

######## 1. MemMapAddressingModeStart

- **UUID**: `9c50f2d3-2e9b-4b6e-b78c-0733ad0530a3`
- **参数名**: `MemMapAddressingModeStart`
- **数据类型**: MULTILINE-STRING
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Defines a set of #pragma statements implementing the start of a section.

######## 2. MemMapAddressingModeStop

- **UUID**: `245a8056-3345-4a29-b6e5-a5f762568004`
- **参数名**: `MemMapAddressingModeStop`
- **数据类型**: MULTILINE-STRING
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Defines a set of #pragma statements implementing the start of a section.

###### 引用关系

此容器包含 **1** 个引用：

####### CHOICE-REFERENCE 类型引用

######## 1. MemMapLinkerLogicalGroupRef

- **UUID**: `30c28846-f675-4ffc-b64a-f72ce89a5723`
- **引用名**: `MemMapLinkerLogicalGroupRef`
- **引用类型**: CHOICE-REFERENCE
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **需要索引**: false
- **目标引用列表**:
  - `/MICROSAR/vLinkGen/vLinkGenMemLayout/vLinkGenLogicalConstGroup`
  - `/MICROSAR/vLinkGen/vLinkGenMemLayout/vLinkGenLogicalVarGroup`
- **描述**: Reference to the vLinkGen logical group to which the MemMapAddressingMode should map.
This reference is required for the automatic pragma generation.

##### 3. MemMapAllocation

**容器属性**:

- **UUID**: `b6006c4c-f939-406e-a8bb-fdce5c3bb470`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `MemMapAllocation`
- **多重性**: [0..infinite]
- **需要索引**: false

**容器描述**:

Defines which MemorySection of a BSW Module or a Software Component is implemented with which MemMapAddressingModeSet.

###### 配置容器

本模块包含 **4** 个配置容器：

####### 1. MemMapGenericMapping

**容器属性**:

- **UUID**: `d455efc4-af28-43f3-b7ec-fadc76467602`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `MemMapGenericMapping`
- **多重性**: [0..infinite]
- **需要索引**: false

**容器描述**:

Defines which SwAddrMethod is implemented with which MemMapAddressingModeSet.

######## 引用关系

此容器包含 **3** 个引用：

######### REFERENCE 类型引用

########## 1. MemMapAddressingModeSetRef

- **UUID**: `7792a1df-15db-4321-a8f1-8a8ff2482e2d`
- **引用名**: `MemMapAddressingModeSetRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `MemMapAddressingModeSet`
- **完整路径**: `/AUTOSAR/EcucDefs/MemMap/MemMapAddressingModeSet`
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to the MemMapAddressingModeSet which applies to the MemMapGenericMapping.

########## 2. MemMapMappingSelectorRef

- **UUID**: `d9748770-a75b-4bd6-97f9-a1d5ad9b7ea6`
- **引用名**: `MemMapMappingSelectorRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `MemMapMappingSelector`
- **完整路径**: `/AUTOSAR/EcucDefs/MemMap/MemMapAllocation/MemMapMappingSelector`
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to a MemMapPrefixSelector. The owning MemMapGenericMapping is only effective for those memories where the MemMapMappingSelector matches.

Note: Parameter not used.

######### FOREIGN-REFERENCE 类型引用

########## 1. MemMapSwAddressMethodRef

- **UUID**: `b2090fe1-e1cf-4eeb-b21e-2e33b684c210`
- **引用名**: `MemMapSwAddressMethodRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [1..infinite]
- **目标类型**: SW-ADDR-METHOD
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to the SwAddrMethod which applies to the MemMapGenericMapping.

####### 2. MemMapMappingSelector

**容器属性**:

- **UUID**: `df3c1dc6-9c56-4ebf-b75d-b4efb33a7910`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `MemMapMappingSelector`
- **多重性**: [0..infinite]
- **需要索引**: false

**容器描述**:

The container holds a section criteria reusable for MemMapGenericMappings.

Note: Container not used.

######## 参数配置

此容器包含 **1** 个参数：

######### STRING 类型参数

########## 1. MemMapPrefixSelector

- **UUID**: `0b54af0a-5aac-4760-aa80-44c98cf34989`
- **参数名**: `MemMapPrefixSelector`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: The parameter MemMapPrefixSelector defines a regular expression which shall be applied to the <PREFIX> part of the memory allocation keywords.

Note: Parameter not used.

####### 3. MemMapSectionSpecificMapping

**容器属性**:

- **UUID**: `f4fd9b32-5882-4906-a04a-2d48b92fa92e`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `MemMapSectionSpecificMapping`
- **多重性**: [0..infinite]
- **需要索引**: false

**容器描述**:

Defines which MemorySection of a BSW Module or a Software Component is implemented with which MemMapAddressingModeSet.

######## 引用关系

此容器包含 **2** 个引用：

######### REFERENCE 类型引用

########## 1. MemMapAddressingModeSetRef

- **UUID**: `dce3cf8d-2efe-4e7b-93e1-3cc6260759c8`
- **引用名**: `MemMapAddressingModeSetRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `MemMapAddressingModeSet`
- **完整路径**: `/AUTOSAR/EcucDefs/MemMap/MemMapAddressingModeSet`
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to the MemMapAddressingModeSet which applies to the MemMapModuleSectionSpecificMapping.

######### FOREIGN-REFERENCE 类型引用

########## 1. MemMapMemorySectionRef

- **UUID**: `cd672fd0-cd1b-430f-964c-8cf89f3fcbf5`
- **引用名**: `MemMapMemorySectionRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [1..infinite]
- **目标类型**: MEMORY-SECTION
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to the MemorySection which applies to the MemMapSectionSpecificMapping.

####### 4. MemMapAdditionalSpecificMapping

**容器属性**:

- **UUID**: `dead7c37-cbf7-49ea-930f-6d0effbedaa8`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `MemMapAdditionalSpecificMapping`
- **多重性**: [0..infinite]
- **需要索引**: false

**容器描述**:

Defines which AdditionalMemorySection is implemented with which MemMapAddressingModeSet.

######## 引用关系

此容器包含 **2** 个引用：

######### REFERENCE 类型引用

########## 1. MemMapAddressingModeSetRef

- **UUID**: `72412142-277d-413b-9fb7-fa955559eaf0`
- **引用名**: `MemMapAddressingModeSetRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `MemMapAddressingModeSet`
- **完整路径**: `/AUTOSAR/EcucDefs/MemMap/MemMapAddressingModeSet`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **需要索引**: false
- **描述**: Reference to the MemMapAddressingModeSet which applies to the MemMapAdditionalSpecificMapping.

########## 2. MemMapAdditionalMemorySectionRef

- **UUID**: `1bb51e72-99fe-4d82-b9f6-747fa8a6a0e0`
- **引用名**: `MemMapAdditionalMemorySectionRef`
- **引用类型**: REFERENCE
- **多重性**: [1..infinite]
- **目标**: `MemMapAdditionalMemorySection`
- **完整路径**: `/MICROSAR/MemMap/MemMapModule/MemMapAdditionalMemorySection`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **需要索引**: false
- **描述**: Reference to the AdditionalMemorySection which applies to the MemMapAdditionalSpecificMapping.

##### 4. MemMapGenericMapping

**容器属性**:

- **UUID**: `d455efc4-af28-43f3-b7ec-fadc76467602`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `MemMapGenericMapping`
- **多重性**: [0..infinite]
- **需要索引**: false

**容器描述**:

Defines which SwAddrMethod is implemented with which MemMapAddressingModeSet.

###### 引用关系

此容器包含 **3** 个引用：

####### REFERENCE 类型引用

######## 1. MemMapAddressingModeSetRef

- **UUID**: `7792a1df-15db-4321-a8f1-8a8ff2482e2d`
- **引用名**: `MemMapAddressingModeSetRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `MemMapAddressingModeSet`
- **完整路径**: `/AUTOSAR/EcucDefs/MemMap/MemMapAddressingModeSet`
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to the MemMapAddressingModeSet which applies to the MemMapGenericMapping.

######## 2. MemMapMappingSelectorRef

- **UUID**: `d9748770-a75b-4bd6-97f9-a1d5ad9b7ea6`
- **引用名**: `MemMapMappingSelectorRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `MemMapMappingSelector`
- **完整路径**: `/AUTOSAR/EcucDefs/MemMap/MemMapAllocation/MemMapMappingSelector`
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to a MemMapPrefixSelector. The owning MemMapGenericMapping is only effective for those memories where the MemMapMappingSelector matches.

Note: Parameter not used.

####### FOREIGN-REFERENCE 类型引用

######## 1. MemMapSwAddressMethodRef

- **UUID**: `b2090fe1-e1cf-4eeb-b21e-2e33b684c210`
- **引用名**: `MemMapSwAddressMethodRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [1..infinite]
- **目标类型**: SW-ADDR-METHOD
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to the SwAddrMethod which applies to the MemMapGenericMapping.

##### 5. MemMapMappingSelector

**容器属性**:

- **UUID**: `df3c1dc6-9c56-4ebf-b75d-b4efb33a7910`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `MemMapMappingSelector`
- **多重性**: [0..infinite]
- **需要索引**: false

**容器描述**:

The container holds a section criteria reusable for MemMapGenericMappings.

Note: Container not used.

###### 参数配置

此容器包含 **1** 个参数：

####### STRING 类型参数

######## 1. MemMapPrefixSelector

- **UUID**: `0b54af0a-5aac-4760-aa80-44c98cf34989`
- **参数名**: `MemMapPrefixSelector`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: The parameter MemMapPrefixSelector defines a regular expression which shall be applied to the <PREFIX> part of the memory allocation keywords.

Note: Parameter not used.

##### 6. MemMapSectionSpecificMapping

**容器属性**:

- **UUID**: `f4fd9b32-5882-4906-a04a-2d48b92fa92e`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `MemMapSectionSpecificMapping`
- **多重性**: [0..infinite]
- **需要索引**: false

**容器描述**:

Defines which MemorySection of a BSW Module or a Software Component is implemented with which MemMapAddressingModeSet.

###### 引用关系

此容器包含 **2** 个引用：

####### REFERENCE 类型引用

######## 1. MemMapAddressingModeSetRef

- **UUID**: `dce3cf8d-2efe-4e7b-93e1-3cc6260759c8`
- **引用名**: `MemMapAddressingModeSetRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `MemMapAddressingModeSet`
- **完整路径**: `/AUTOSAR/EcucDefs/MemMap/MemMapAddressingModeSet`
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to the MemMapAddressingModeSet which applies to the MemMapModuleSectionSpecificMapping.

####### FOREIGN-REFERENCE 类型引用

######## 1. MemMapMemorySectionRef

- **UUID**: `cd672fd0-cd1b-430f-964c-8cf89f3fcbf5`
- **引用名**: `MemMapMemorySectionRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [1..infinite]
- **目标类型**: MEMORY-SECTION
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to the MemorySection which applies to the MemMapSectionSpecificMapping.

##### 7. MemMapAdditionalSpecificMapping

**容器属性**:

- **UUID**: `dead7c37-cbf7-49ea-930f-6d0effbedaa8`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `MemMapAdditionalSpecificMapping`
- **多重性**: [0..infinite]
- **需要索引**: false

**容器描述**:

Defines which AdditionalMemorySection is implemented with which MemMapAddressingModeSet.

###### 引用关系

此容器包含 **2** 个引用：

####### REFERENCE 类型引用

######## 1. MemMapAddressingModeSetRef

- **UUID**: `72412142-277d-413b-9fb7-fa955559eaf0`
- **引用名**: `MemMapAddressingModeSetRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `MemMapAddressingModeSet`
- **完整路径**: `/AUTOSAR/EcucDefs/MemMap/MemMapAddressingModeSet`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **需要索引**: false
- **描述**: Reference to the MemMapAddressingModeSet which applies to the MemMapAdditionalSpecificMapping.

######## 2. MemMapAdditionalMemorySectionRef

- **UUID**: `1bb51e72-99fe-4d82-b9f6-747fa8a6a0e0`
- **引用名**: `MemMapAdditionalMemorySectionRef`
- **引用类型**: REFERENCE
- **多重性**: [1..infinite]
- **目标**: `MemMapAdditionalMemorySection`
- **完整路径**: `/MICROSAR/MemMap/MemMapModule/MemMapAdditionalMemorySection`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **需要索引**: false
- **描述**: Reference to the AdditionalMemorySection which applies to the MemMapAdditionalSpecificMapping.

##### 8. MemMapGenericCompilerMemClass

**容器属性**:

- **UUID**: `3bced468-054c-4824-83a6-94eb1aed4ef4`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `MemMapGenericCompilerMemClass`
- **多重性**: [0..infinite]
- **需要索引**: false

**容器描述**:

The shortName of the container defines the name of the generic Compiler memclass which is global for all using modules, e.g. REGSPACE.

Note: Container not used.

###### 参数配置

此容器包含 **1** 个参数：

####### STRING 类型参数

######## 1. MemMapGenericCompilerMemClassSymbolImpl

- **UUID**: `a7db61ff-db3a-4c53-a1ab-79d03f340676`
- **参数名**: `MemMapGenericCompilerMemClassSymbolImpl`
- **数据类型**: STRING
- **多重性**: [1..1]
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Defines the implementation behind the generic MemClassSymbol and configures the Compiler Abstraction.

Note: Parameter not used.

##### 9. MemMapGeneral

**容器属性**:

- **UUID**: `37620ae1-8c8a-4093-b816-8e506ce10d79`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `MemMapGeneral`
- **多重性**: [1..1]
- **需要索引**: false

**容器描述**:

General configuration parameters of the MemMap.

###### 参数配置

此容器包含 **8** 个参数：

####### BOOLEAN 类型参数

######## 1. MemMapTypedPragmas

- **UUID**: `a7c843c7-596e-4e2a-a77a-b094492383c8`
- **参数名**: `MemMapTypedPragmas`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Specifies whether pragmas are generated with types.
Pragmas that are entered manually are not affected by this parameter.

Note:
This parameter only affects the automatic pragma generation for the Tasking compiler.
The parameter should only be set to "false" when using the platform "ARM". Otherwise it should be set to "true".

######## 2. MemMapGeneratePragmas

- **UUID**: `b5dc786f-340c-4ec1-ac6c-c0ec87533a8d`
- **参数名**: `MemMapGeneratePragmas`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Specifies whether pragmas are generated into the memory mapping header file(s).
If set to "false" the memory mapping header file(s) will not contain any pragmas and
therefore there will be no mapping to linker sections.

######## 3. MemMapGeneratePragmasForNearAddressing

- **UUID**: `fbe97961-8fdd-456a-a505-c7bcf5caa14e`
- **参数名**: `MemMapGeneratePragmasForNearAddressing`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Specifies whether pragmas are generated for near addressing modes (e.g. sdata, sbss, sconst).
If the near addressing mode is not necessary according to the compiler options used, generation
can be disabled with this parameter.

####### STRING 类型参数

######## 1. MemMapPreUserConfigFile

- **UUID**: `05eb9605-f212-4940-921e-296e6dbef0c2`
- **参数名**: `MemMapPreUserConfigFile`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Reference to an external text file that will be included during generation to ANY memory mapping header file.
The content of the user configuration file will be added at the beginning of the generated files and allows altering or extending the generated code.

Note:
In contrast to the other MICROSAR components, MemMap provides the possibility to insert user config files at the beginning and end of the generated memory mapping header files.
See also 'Post User Config File'.

Caution:
User configuration files can cause the software module to malfunction and must only be used with great care!

######## 2. MemMapPostUserConfigFile

- **UUID**: `80d5b562-ef25-4b27-b434-0cfe8ebbad77`
- **参数名**: `MemMapPostUserConfigFile`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Reference to an external text file that will be included during generation to ANY memory mapping header file.
The content of the user configuration file will be added at the end of the generated files and allows altering or extending the generated code.

Note:
In contrast to the other MICROSAR components, MemMap provides the possibility to insert user config files at the beginning and end of the generated memory mapping header files.
See also 'Pre User Config File'.

Caution:
User configuration files can cause the software module to malfunction and must only be used with great care!

####### ENUMERATION 类型参数

######## 1. MemMapGeneration

- **UUID**: `bedeead4-81dd-485b-9ea3-9fc64e6d10f1`
- **参数名**: `MemMapGeneration`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `FULL`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `FULL` (来源: Vector Informatik)
  - `EMPTY` (来源: Vector Informatik)
  - `USER_CONFIG_ONLY` (来源: Vector Informatik)
  - `NON` (来源: Vector Informatik)
- **描述**: Specifies how the module specific memory mapping header file(s) shall be generated.

FULL:
Generates a memory mapping header file for each BSW module and software component type
in the project that has MemorySections configured. In addition the MemMapAdditionalMemorySection(s)
are generated into their respective files.

EMPTY:
Creates the same files as with the generation type FULL. However, the files will be empty in this case.

USER_CONFIG_ONLY:
Creates the same files as with the generation type FULL. However, the files will only contain the contents
of 'Pre User Config File' and 'Post User Config File'.

NON:
None of the files that would be generated with generation type FULL will be created.

######## 2. MemMapCompatibilityGeneration

- **UUID**: `631a805e-806c-462f-ae56-1123f6fbc199`
- **参数名**: `MemMapCompatibilityGeneration`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `FULL`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `FULL` (来源: Vector Informatik)
  - `EMPTY` (来源: Vector Informatik)
  - `USER_CONFIG_ONLY` (来源: Vector Informatik)
  - `NON` (来源: Vector Informatik)
- **描述**: Specifies if and how the compatibility memory mapping header file (MemMap_Compatibility.h) shall be generated.

FULL:
Generates a compatibility memory mapping header file that contains the MemorySections of all BSW modules in the project.

EMPTY:
Generates a compatibility memory mapping header file that is empty.

USER_CONFIG_ONLY:
Generates a compatibility memory mapping header file that only contains the contents of 'Pre User Config File' and 'Post User Config File'.

NON:
No compatibility memory mapping header file will be generated.

######## 3. MemMapErrorChecks

- **UUID**: `1ef58f4c-fbea-4143-93f5-5551423b5e29`
- **参数名**: `MemMapErrorChecks`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `ALL`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `ALL` (来源: Vector Informatik)
  - `AUTOSAR` (来源: Vector Informatik)
  - `NON` (来源: Vector Informatik)
- **描述**: Specifies if and which error checks shall be added to the generated memory mapping header file(s).

Note:
Error checks with a higher level also include the error checks of lower levels, e.g. ALL includes the
error checks of AUTOSAR.

ALL (Level 2):
All possible error checks are added to the memory mapping header file(s).

AUTOSAR (Level 1):
All error checks defined by AUTOSAR are added to the memory mapping header file(s).

NON (Level 0):
No error checks are added to the memory mapping header file(s).

##### 10. MemMapModule

**容器属性**:

- **UUID**: `26fcf09b-264c-44af-9d6b-9190b2db1eb5`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `MemMapModule`
- **多重性**: [0..infinite]
- **需要索引**: false

**容器描述**:

Abstraction layer for grouping AdditionalMemorySections that belong to the same module.

###### 参数配置

此容器包含 **1** 个参数：

####### BOOLEAN 类型参数

######## 1. MemMapGenerateAdditionalMemorySections

- **UUID**: `04be9b94-ae56-40c9-8e9d-9191b6f0bf80`
- **参数名**: `MemMapGenerateAdditionalMemorySections`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Specifies whether the AdditionalMemorySection(s) defined for this module should be
generated into the memory mapping header file(s).

###### 引用关系

此容器包含 **1** 个引用：

####### FOREIGN-REFERENCE 类型引用

######## 1. MemMapModuleRef

- **UUID**: `a15749de-3006-4ddf-9d14-e800c0e8c920`
- **引用名**: `MemMapModuleRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [0..1]
- **目标类型**: ECUC-MODULE-CONFIGURATION-VALUES
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **需要索引**: false
- **描述**: Optional reference that specifies to which module the AdditionalMemorySection(s) belong.

Note:
If this reference is set, the container is typically created by another module's generator.

Caution:
If a module is referenced it must contain a BSW-IMPLEMENTATION. Otherwise none
of the MemMapAdditionalMemorySections contained in the MemMapModule can be generated.

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. MemMapAdditionalMemorySection

**容器属性**:

- **UUID**: `5ab4acf4-0b84-42c6-aac5-6388acc175a9`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `MemMapAdditionalMemorySection`
- **多重性**: [1..infinite]
- **需要索引**: false

**容器描述**:

Vector MemorySections that can be configured in the ECUC.

These MemorySections are generated in addition to the MemorySections
configured according to AUTOSAR.

######## 参数配置

此容器包含 **4** 个参数：

######### STRING 类型参数

########## 1. MemMapMemorySectionAlignment

- **UUID**: `5554a00e-43c9-4c3e-a836-eb488c6160c0`
- **参数名**: `MemMapMemorySectionAlignment`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: The alignment of objects within this AdditionalMemorySection.
The following alignments are supported: BOOLEAN, 8, 16, 32, 64, UNSPECIFIED.

Note:
If this parameter is not set the default alignment "UNSPECIFIED" will be used.

########## 2. MemMapMemorySectionFileName

- **UUID**: `c275d3a1-cf8f-4d64-9cf9-7511d0fcab7d`
- **参数名**: `MemMapMemorySectionFileName`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Specifies the name of the file this AdditionalMemorySection shall be generated into.

Note:
If this parameter is not set the MemMapModuleRef in the parent container
MemMapModule needs to be set.

########## 3. MemMapMemorySectionPrefix

- **UUID**: `9238eb7b-e8f7-40de-b16f-943887bc8a67`
- **参数名**: `MemMapMemorySectionPrefix`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Specifies the {PREFIX} part in the memory allocation keyword {PREFIX}_(START|STOP)_SEC_{SYMBOL}.

Note:
If this parameter is not set the MemMapModuleRef in the parent container
MemMapModule needs to be set.

########## 4. MemMapMemorySectionSymbol

- **UUID**: `8780d7cb-bae2-421d-b36a-2125e5edc44e`
- **参数名**: `MemMapMemorySectionSymbol`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Specifies the {SYMBOL} part in the memory allocation keyword {PREFIX}_(START|STOP)_SEC_{SYMBOL}.

Note:
If this parameter is not set the ShortName of the container this parameter
is contained in will be used as {SYMBOL}.

######## 引用关系

此容器包含 **1** 个引用：

######### FOREIGN-REFERENCE 类型引用

########## 1. MemMapMemorySectionSwAddrMethodRef

- **UUID**: `52053c02-42e9-4f9b-8b96-14e7f6d16287`
- **引用名**: `MemMapMemorySectionSwAddrMethodRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [1..1]
- **目标类型**: SW-ADDR-METHOD
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **需要索引**: false
- **描述**: Reference to the SwAddrMethod this AdditionalMemorySection is associated with.

##### 11. MemMapAdditionalMemorySection

**容器属性**:

- **UUID**: `5ab4acf4-0b84-42c6-aac5-6388acc175a9`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `MemMapAdditionalMemorySection`
- **多重性**: [1..infinite]
- **需要索引**: false

**容器描述**:

Vector MemorySections that can be configured in the ECUC.

These MemorySections are generated in addition to the MemorySections
configured according to AUTOSAR.

###### 参数配置

此容器包含 **4** 个参数：

####### STRING 类型参数

######## 1. MemMapMemorySectionAlignment

- **UUID**: `5554a00e-43c9-4c3e-a836-eb488c6160c0`
- **参数名**: `MemMapMemorySectionAlignment`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: The alignment of objects within this AdditionalMemorySection.
The following alignments are supported: BOOLEAN, 8, 16, 32, 64, UNSPECIFIED.

Note:
If this parameter is not set the default alignment "UNSPECIFIED" will be used.

######## 2. MemMapMemorySectionFileName

- **UUID**: `c275d3a1-cf8f-4d64-9cf9-7511d0fcab7d`
- **参数名**: `MemMapMemorySectionFileName`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Specifies the name of the file this AdditionalMemorySection shall be generated into.

Note:
If this parameter is not set the MemMapModuleRef in the parent container
MemMapModule needs to be set.

######## 3. MemMapMemorySectionPrefix

- **UUID**: `9238eb7b-e8f7-40de-b16f-943887bc8a67`
- **参数名**: `MemMapMemorySectionPrefix`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Specifies the {PREFIX} part in the memory allocation keyword {PREFIX}_(START|STOP)_SEC_{SYMBOL}.

Note:
If this parameter is not set the MemMapModuleRef in the parent container
MemMapModule needs to be set.

######## 4. MemMapMemorySectionSymbol

- **UUID**: `8780d7cb-bae2-421d-b36a-2125e5edc44e`
- **参数名**: `MemMapMemorySectionSymbol`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Specifies the {SYMBOL} part in the memory allocation keyword {PREFIX}_(START|STOP)_SEC_{SYMBOL}.

Note:
If this parameter is not set the ShortName of the container this parameter
is contained in will be used as {SYMBOL}.

###### 引用关系

此容器包含 **1** 个引用：

####### FOREIGN-REFERENCE 类型引用

######## 1. MemMapMemorySectionSwAddrMethodRef

- **UUID**: `52053c02-42e9-4f9b-8b96-14e7f6d16287`
- **引用名**: `MemMapMemorySectionSwAddrMethodRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [1..1]
- **目标类型**: SW-ADDR-METHOD
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **需要索引**: false
- **描述**: Reference to the SwAddrMethod this AdditionalMemorySection is associated with.

## 📦 包结构

此ARXML文件包含 **1** 个包：

### 1. MICROSAR

- **UUID**: `ff55d029-386d-43a2-b3c2-dfef4c7a5e36`
- **包名称**: `MICROSAR`
- **包含元素数量**: 2

#### 包含的元素

##### ECUC-MODULE-DEF 类型元素

1. **MemMap**

##### BSW-IMPLEMENTATION 类型元素

1. **MemMap_Impl**

## ⚡ 实现信息

此ARXML文件包含 **1** 个实现：

### 1. MemMap_Impl

- **UUID**: `2f7f22d7-694b-42ab-8c4e-cf4519575a85`
- **实现名称**: `MemMap_Impl`
- **编程语言**: C
- **软件版本**: 1.07.00
- **供应商ID**: 30
- **AUTOSAR版本**: 4.05.00
- **代码生成器**: DaVinci Configurator
