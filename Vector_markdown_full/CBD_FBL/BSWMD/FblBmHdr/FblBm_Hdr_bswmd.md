# FblBmHdr - 完整配置文档

*此文档由ARXML文件自动生成，采用层次化结构展示*

**生成时间**: 2025-06-16 14:48:08

## 📑 目录

- [📄 文件信息](#-文件信息)
- [🔧 模块定义](#-模块定义)
  - [FblBmHdr](#fblbmhdr)
- [📦 包结构](#-包结构)
- [⚡ 实现信息](#-实现信息)
- [⚙️ 配置信息](#️-配置信息)

## 📄 文件信息

### Schema信息
- **Schema位置**: `http://autosar.org/schema/r4.0 AUTOSAR_4-3-0.xsd`
- **命名空间**: `http://autosar.org/schema/r4.0`

## 🔧 模块定义

### 1. FblBmHdr

#### 基本信息

- **UUID**: `030b1471-217f-4fdd-800e-e77510b11d92`
- **模块名称**: `FblBmHdr`
- **类别**: `VENDOR_SPECIFIC_MODULE_DEFINITION`
- **多重性**: [1..1]
- **支持的变体**:
  - VARIANT-PRE-COMPILE

#### 模块描述

Configuration of the FblBmHdr (Boot Manager Header) module.

#### 版本历史

共有 **1** 个版本记录：

##### 1. 版本 1.02.00

- **发布日期**: 2019-07-24T14:03:29+02:00
- **发布者**: visrcn

**变更内容**:

#### 配置容器

本模块包含 **7** 个配置容器：

##### 1. FblBmHdrGeneral

**容器属性**:

- **UUID**: `f0882ee4-80a3-4513-a89e-11d5f5476a3f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FblBmHdrGeneral`
- **多重性**: [1..1]
- **需要索引**: false

**容器描述**:

General configuration parameters of the FblBmHdr.

###### 参数配置

此容器包含 **3** 个参数：

####### INTEGER 类型参数

######## 1. FblBmHdrMaxVerificationEntries

- **UUID**: `426a63a5-7fb9-4355-b8d7-8aadc6e1d77c`
- **参数名**: `FblBmHdrMaxVerificationEntries`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `1`
- **取值范围**: [0..4294967295]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Specify the maximum number verification ranges, which can be used.

####### BOOLEAN 类型参数

######## 1. FblBmHdrSbVerificationList

- **UUID**: `7d89ff92-8d30-4b6a-812c-a03a3292f53c`
- **参数名**: `FblBmHdrSbVerificationList`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false

####### STRING 类型参数

######## 1. FblBmHdrUserConfigFile

- **UUID**: `8c227328-cdbc-46c3-9c06-18eac5c71e37`
- **参数名**: `FblBmHdrUserConfigFile`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **字符串变体**:
  - 默认值: `FblBmHdr_UserCfg.h`
- **描述**: Reference to an external text file that will be included during generation to FblBmHdr_Cfg.h.
The content of the user configuration file will be added at the end of the generated module configuration file and allows altering or extending the generated code.

Caution: User configuration files can cause the software module to malfunction and must only be used with great care!

##### 2. FblBmHdrTarget

**容器属性**:

- **UUID**: `28966beb-d50e-41dc-b5aa-f7b6b249a58d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FblBmHdrTarget`
- **多重性**: [1..256]
- **需要索引**: false

**容器描述**:

Container to configure the targets.

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. FblBmHdrTargetId

- **UUID**: `2d753e2a-3147-496f-8a3b-8ce87c5cbd15`
- **参数名**: `FblBmHdrTargetId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..255]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Identifier of the Target.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. FblBmHdrTargetMacOpRef

- **UUID**: `621d7c72-de7e-4cf1-8c07-0fc6576da1cf`
- **引用名**: `FblBmHdrTargetMacOpRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `FblSbMacOperation`
- **完整路径**: `/MICROSAR/FblSb/FblSbMacOperation`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **需要索引**: false
- **描述**: This parameter refers to the used MAC operations, which shall be used to verify/generate the MAC.

##### 3. FblBmHdrHeader

**容器属性**:

- **UUID**: `7e29eaf9-2e12-42da-ba42-26f33c8f046e`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FblBmHdrHeader`
- **多重性**: [0..1]
- **需要索引**: false

**容器描述**:

Container to configure the BootManagerHeader.
The generated header needs to be linked to a specific location, which is defined in the LogicalBlockTable.

###### 参数配置

此容器包含 **4** 个参数：

####### INTEGER 类型参数

######## 1. FblBmHdrBlockStartAddress

- **UUID**: `87053ffd-5f39-41bc-8d63-f6b20af86c0a`
- **参数名**: `FblBmHdrBlockStartAddress`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Start address of the complete block.

######## 2. FblBmHdrBlockLength

- **UUID**: `3d885c55-9ed0-44ae-949a-079395d18d74`
- **参数名**: `FblBmHdrBlockLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `1`
- **取值范围**: [1..4294967295]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Length of the complete block in bytes.

####### STRING 类型参数

######## 1. FblBmHdrEntryAddress

- **UUID**: `8fbf7032-73dd-45f9-a98f-320842d6049b`
- **参数名**: `FblBmHdrEntryAddress`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Entry address of the software.
The address can be specified either as a valid decimal (1024) or hexadecimal (0x4000) value, or as a valid linker symbol.

######## 2. FblBmHdrEntryAddressInclude

- **UUID**: `3bc0741c-0fed-45cd-af0d-faa91c0dc8f9`
- **参数名**: `FblBmHdrEntryAddressInclude`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Specify an include file, which contains the declaration of the FblBmHdrEntryAddress symbol in case a linker symbol is used as Entry Address.
If no include file is specified and a linker symbol is used, an extern uint8 array is declared to resolve potential compiler errors.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. FblBmHdrTargetRef

- **UUID**: `505cabfa-881a-48db-b8f3-7c6c9f557ac2`
- **引用名**: `FblBmHdrTargetRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `FblBmHdrTarget`
- **完整路径**: `/MICROSAR/FblBmHdr/FblBmHdrTarget`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **需要索引**: false
- **描述**: This parameter refers to the target for which this header is.

###### 配置容器

本模块包含 **4** 个配置容器：

####### 1. FblBmHdrAuthenticationHeader

**容器属性**:

- **UUID**: `f9328211-0e07-414b-96a9-2f5bd67fc577`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FblBmHdrAuthenticationHeader`
- **多重性**: [0..1]
- **需要索引**: false

**容器描述**:

Configure the address/symbol of the authentication header

######## 参数配置

此容器包含 **2** 个参数：

######### STRING 类型参数

########## 1. FblBmHdrAuthenticationHeaderAddress

- **UUID**: `ee6ae9fc-90f8-4541-a3bf-9d6a269c6642`
- **参数名**: `FblBmHdrAuthenticationHeaderAddress`
- **数据类型**: STRING
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **字符串变体**:
  - 默认值: `0`
- **描述**: Address of the authentication header.
The address can be specified either as a valid decimal (1024) or hexadecimal (0x4000) value, or as a valid linker symbol.

########## 2. FblBmHdrAuthenticationHeaderAddressInclude

- **UUID**: `645337de-1c35-42f9-b328-19b1daef4f9e`
- **参数名**: `FblBmHdrAuthenticationHeaderAddressInclude`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Specify an include file, which contains the declaration of the FblBmHdrAuthenticationHeaderAddress symbol in case a linker symbol is used as Entry Address.
If no include file is specified and a linker symbol is used, an extern uint8 array is declared to resolve potential compiler errors.

####### 2. FblBmHdrVerificationList

**容器属性**:

- **UUID**: `f59e2f48-6f15-48f9-83ad-7d8f4c1ae0f2`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FblBmHdrVerificationList`
- **多重性**: [0..1]
- **需要索引**: false

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. FblBmHdrVerificationRange

**容器属性**:

- **UUID**: `db77bad5-c04c-4163-a0d2-ba8bf4dc2eb6`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FblBmHdrVerificationRange`
- **多重性**: [1..infinite]
- **需要索引**: false

**容器描述**:

Container to configure the verification ranges.

########## 参数配置

此容器包含 **3** 个参数：

########### INTEGER 类型参数

############ 1. FblBmHdrVerificationId

- **UUID**: `e93fc5c5-8f50-4b2a-a9a6-dfda6f66715a`
- **参数名**: `FblBmHdrVerificationId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Identifier of the verification range.

############ 2. FblBmHdrVerificationStartAddress

- **UUID**: `55f1868e-e54b-4c2d-aaec-3ec32342dae2`
- **参数名**: `FblBmHdrVerificationStartAddress`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: This parameter specifies the start address of the verification range.

############ 3. FblBmHdrVerificationLength

- **UUID**: `73d5ee59-20ab-4924-816d-3bf070d4d8af`
- **参数名**: `FblBmHdrVerificationLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `1`
- **取值范围**: [1..4294967295]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: This parameter specifies the length of the verification range in bytes.

####### 3. FblBmHdrVerificationRange

**容器属性**:

- **UUID**: `db77bad5-c04c-4163-a0d2-ba8bf4dc2eb6`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FblBmHdrVerificationRange`
- **多重性**: [1..infinite]
- **需要索引**: false

**容器描述**:

Container to configure the verification ranges.

######## 参数配置

此容器包含 **3** 个参数：

######### INTEGER 类型参数

########## 1. FblBmHdrVerificationId

- **UUID**: `e93fc5c5-8f50-4b2a-a9a6-dfda6f66715a`
- **参数名**: `FblBmHdrVerificationId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Identifier of the verification range.

########## 2. FblBmHdrVerificationStartAddress

- **UUID**: `55f1868e-e54b-4c2d-aaec-3ec32342dae2`
- **参数名**: `FblBmHdrVerificationStartAddress`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: This parameter specifies the start address of the verification range.

########## 3. FblBmHdrVerificationLength

- **UUID**: `73d5ee59-20ab-4924-816d-3bf070d4d8af`
- **参数名**: `FblBmHdrVerificationLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `1`
- **取值范围**: [1..4294967295]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: This parameter specifies the length of the verification range in bytes.

####### 4. FblBmHdrVariant

**容器属性**:

- **UUID**: `19e3f1bf-0615-4101-841b-c4c7214de48d`
- **容器类型**: CHOICE-CONTAINER
- **容器名称**: `FblBmHdrVariant`
- **多重性**: [1..1]
- **需要索引**: false

**容器选择**:

- **FblBmHdrAuthenticationHeader**
  - UUID: `f9328211-0e07-414b-96a9-2f5bd67fc577`
  - 描述: Configure the address/symbol of the authentication header
- **FblBmHdrVerificationList**
  - UUID: `f59e2f48-6f15-48f9-83ad-7d8f4c1ae0f2`
- **FblBmHdrVerificationRange**
  - UUID: `db77bad5-c04c-4163-a0d2-ba8bf4dc2eb6`
  - 描述: Container to configure the verification ranges.

##### 4. FblBmHdrAuthenticationHeader

**容器属性**:

- **UUID**: `f9328211-0e07-414b-96a9-2f5bd67fc577`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FblBmHdrAuthenticationHeader`
- **多重性**: [0..1]
- **需要索引**: false

**容器描述**:

Configure the address/symbol of the authentication header

###### 参数配置

此容器包含 **2** 个参数：

####### STRING 类型参数

######## 1. FblBmHdrAuthenticationHeaderAddress

- **UUID**: `ee6ae9fc-90f8-4541-a3bf-9d6a269c6642`
- **参数名**: `FblBmHdrAuthenticationHeaderAddress`
- **数据类型**: STRING
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **字符串变体**:
  - 默认值: `0`
- **描述**: Address of the authentication header.
The address can be specified either as a valid decimal (1024) or hexadecimal (0x4000) value, or as a valid linker symbol.

######## 2. FblBmHdrAuthenticationHeaderAddressInclude

- **UUID**: `645337de-1c35-42f9-b328-19b1daef4f9e`
- **参数名**: `FblBmHdrAuthenticationHeaderAddressInclude`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Specify an include file, which contains the declaration of the FblBmHdrAuthenticationHeaderAddress symbol in case a linker symbol is used as Entry Address.
If no include file is specified and a linker symbol is used, an extern uint8 array is declared to resolve potential compiler errors.

##### 5. FblBmHdrVerificationList

**容器属性**:

- **UUID**: `f59e2f48-6f15-48f9-83ad-7d8f4c1ae0f2`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FblBmHdrVerificationList`
- **多重性**: [0..1]
- **需要索引**: false

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. FblBmHdrVerificationRange

**容器属性**:

- **UUID**: `db77bad5-c04c-4163-a0d2-ba8bf4dc2eb6`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FblBmHdrVerificationRange`
- **多重性**: [1..infinite]
- **需要索引**: false

**容器描述**:

Container to configure the verification ranges.

######## 参数配置

此容器包含 **3** 个参数：

######### INTEGER 类型参数

########## 1. FblBmHdrVerificationId

- **UUID**: `e93fc5c5-8f50-4b2a-a9a6-dfda6f66715a`
- **参数名**: `FblBmHdrVerificationId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Identifier of the verification range.

########## 2. FblBmHdrVerificationStartAddress

- **UUID**: `55f1868e-e54b-4c2d-aaec-3ec32342dae2`
- **参数名**: `FblBmHdrVerificationStartAddress`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: This parameter specifies the start address of the verification range.

########## 3. FblBmHdrVerificationLength

- **UUID**: `73d5ee59-20ab-4924-816d-3bf070d4d8af`
- **参数名**: `FblBmHdrVerificationLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `1`
- **取值范围**: [1..4294967295]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: This parameter specifies the length of the verification range in bytes.

##### 6. FblBmHdrVerificationRange

**容器属性**:

- **UUID**: `db77bad5-c04c-4163-a0d2-ba8bf4dc2eb6`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FblBmHdrVerificationRange`
- **多重性**: [1..infinite]
- **需要索引**: false

**容器描述**:

Container to configure the verification ranges.

###### 参数配置

此容器包含 **3** 个参数：

####### INTEGER 类型参数

######## 1. FblBmHdrVerificationId

- **UUID**: `e93fc5c5-8f50-4b2a-a9a6-dfda6f66715a`
- **参数名**: `FblBmHdrVerificationId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Identifier of the verification range.

######## 2. FblBmHdrVerificationStartAddress

- **UUID**: `55f1868e-e54b-4c2d-aaec-3ec32342dae2`
- **参数名**: `FblBmHdrVerificationStartAddress`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: This parameter specifies the start address of the verification range.

######## 3. FblBmHdrVerificationLength

- **UUID**: `73d5ee59-20ab-4924-816d-3bf070d4d8af`
- **参数名**: `FblBmHdrVerificationLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `1`
- **取值范围**: [1..4294967295]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: This parameter specifies the length of the verification range in bytes.

##### 7. FblBmHdrVariant

**容器属性**:

- **UUID**: `19e3f1bf-0615-4101-841b-c4c7214de48d`
- **容器类型**: CHOICE-CONTAINER
- **容器名称**: `FblBmHdrVariant`
- **多重性**: [1..1]
- **需要索引**: false

**容器选择**:

- **FblBmHdrAuthenticationHeader**
  - UUID: `f9328211-0e07-414b-96a9-2f5bd67fc577`
  - 描述: Configure the address/symbol of the authentication header
- **FblBmHdrVerificationList**
  - UUID: `f59e2f48-6f15-48f9-83ad-7d8f4c1ae0f2`
- **FblBmHdrVerificationRange**
  - UUID: `db77bad5-c04c-4163-a0d2-ba8bf4dc2eb6`
  - 描述: Container to configure the verification ranges.

## 📦 包结构

此ARXML文件包含 **1** 个包：

### 1. MICROSAR

- **UUID**: `ff55d029-386d-43a2-b3c2-dfef4c7a5e36`
- **包名称**: `MICROSAR`
- **包含元素数量**: 4

#### 包含的元素

##### BSW-IMPLEMENTATION 类型元素

1. **FblBmHdr_Impl**

##### ECUC-MODULE-DEF 类型元素

1. **FblBmHdr**

##### ECUC-MODULE-CONFIGURATION-VALUES 类型元素

1. **FblBmHdr_Pre**
2. **FblBmHdr_Rec**

## ⚡ 实现信息

此ARXML文件包含 **1** 个实现：

### 1. FblBmHdr_Impl

- **UUID**: `917f3349-6097-432b-b3d2-721744960bde`
- **实现名称**: `FblBmHdr_Impl`
- **编程语言**: C
- **软件版本**: 2.00.00
- **供应商ID**: 30
- **AUTOSAR版本**: 4.03.00
- **代码生成器**: DaVinci Configurator

## ⚙️ 配置信息

此ARXML文件包含 **2** 个配置：

### 1. FblBmHdr_Pre

- **UUID**: `54743a1f-eefe-42a6-95c6-f83cf4dc4233`
- **配置名称**: `FblBmHdr_Pre`
- **定义引用**: `/MICROSAR/FblBmHdr`

### 2. FblBmHdr_Rec

- **UUID**: `5321676c-bc2f-44cd-b779-63a64318e0a4`
- **配置名称**: `FblBmHdr_Rec`
- **定义引用**: `/MICROSAR/FblBmHdr`
