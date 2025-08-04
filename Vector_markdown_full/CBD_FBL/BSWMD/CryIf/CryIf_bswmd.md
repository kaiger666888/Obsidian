# CryIf - 完整配置文档

*此文档由ARXML文件自动生成，采用层次化结构展示*

**生成时间**: 2025-06-16 14:47:59

## 📑 目录

- [📄 文件信息](#-文件信息)
- [🔧 模块定义](#-模块定义)
  - [CryIf](#cryif)
- [📦 包结构](#-包结构)
- [⚡ 实现信息](#-实现信息)
- [⚙️ 配置信息](#️-配置信息)

## 📄 文件信息

### Schema信息
- **Schema位置**: `http://autosar.org/schema/r4.0 AUTOSAR_4-3-0.xsd`
- **命名空间**: `http://autosar.org/schema/r4.0`

## 🔧 模块定义

### 1. CryIf

#### 基本信息

- **UUID**: `35f34d85-2f3c-401f-b109-66568f7df130`
- **模块名称**: `CryIf`
- **类别**: `VENDOR_SPECIFIC_MODULE_DEFINITION`
- **多重性**: [0..1]
- **支持的变体**:
  - VARIANT-PRE-COMPILE

#### 模块描述

Configuration of the Crypto Interface.

#### 版本历史

共有 **12** 个版本记录：

##### 1. 版本 1.00.00

- **状态**: beta
- **发布日期**: 2016-07-13T10:23:09+02:00
- **发布者**: visrpp

**变更内容**:

##### 2. 版本 1.00.01

- **状态**: beta
- **发布日期**: 2016-12-06T04:28:20+01:00
- **发布者**: visrpp

**变更内容**:

##### 3. 版本 1.00.02

- **状态**: beta
- **发布日期**: 2016-12-16T09:54:01+01:00
- **发布者**: vismss

**变更内容**:

##### 4. 版本 1.00.03

- **状态**: beta
- **发布日期**: 2017-01-24T10:47:52+01:00
- **发布者**: vismss

**变更内容**:

##### 5. 版本 1.01.00

- **状态**: beta
- **发布日期**: 2017-02-23T11:34:12+01:00
- **发布者**: vismss

**变更内容**:

##### 6. 版本 1.02.00

- **状态**: released
- **发布日期**: 2017-05-05T01:37:14+02:00
- **发布者**: visrpp

**变更内容**:

##### 7. 版本 2.00.00

- **状态**: released
- **发布日期**: 2017-05-12T02:23:20+02:00
- **发布者**: vismss

**变更内容**:

##### 8. 版本 2.01.00

- **状态**: released
- **发布日期**: 2017-07-13T09:26:51+02:00
- **发布者**: visrpp

**变更内容**:

##### 9. 版本 4.00.00

- **状态**: released
- **发布日期**: 2018-11-23T10:28:43+01:00
- **发布者**: vismaw

**变更内容**:

##### 10. 版本 4.01.00

- **状态**: released
- **发布日期**: 2019-03-12T10:31:25+01:00
- **发布者**: vismaw

**变更内容**:

##### 11. 版本 5.00.00

- **状态**: released
- **发布日期**: 2019-12-04T13:06:07+01:00
- **发布者**: vismxe

**变更内容**:

##### 12. 版本 5.01.00

- **状态**: released
- **发布日期**: 2020-08-18T11:23:48+02:00
- **发布者**: vismxe

**变更内容**:

#### 配置容器

本模块包含 **4** 个配置容器：

##### 1. CryIfChannel

**容器属性**:

- **UUID**: `7a885e30-624e-4806-a6e4-935d98b2021b`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CryIfChannel`
- **多重性**: [1..infinite]
- **需要索引**: false

**容器描述**:

Container for incorporation of CryIfChannel.

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. CryIfChannelId

- **UUID**: `19c3e6d4-cd71-47e1-b53e-87941187b7e7`
- **参数名**: `CryIfChannelId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **需要索引**: false
- **描述**: Identifier of the crypto channel.

###### 引用关系

此容器包含 **1** 个引用：

####### SYMBOLIC-NAME-REFERENCE 类型引用

######## 1. CryIfDriverObjectRef

- **UUID**: `6d977689-e5ec-432e-a99f-506b5b1f8ed5`
- **引用名**: `CryIfDriverObjectRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `CryptoDriverObject`
- **完整路径**: `/AUTOSAR/EcucDefs/Crypto/CryptoDriverObjects/CryptoDriverObject`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: This parameter refers to a Crypto Driver Object.

##### 2. CryIfGeneral

**容器属性**:

- **UUID**: `5c9afa9c-e1e5-45e6-a6ab-a8d182909321`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CryIfGeneral`
- **多重性**: [1..1]
- **需要索引**: false

**容器描述**:

Container for incorporation of CryIfGeneral.

###### 参数配置

此容器包含 **6** 个参数：

####### INTEGER 类型参数

######## 1. CryIfMaxNumberOfKeyElements

- **UUID**: `37903d9d-cc2b-4acd-bbe7-aae58a8033ff`
- **参数名**: `CryIfMaxNumberOfKeyElements`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `10`
- **取值范围**: [1..4294967295]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Maximum number of key elements in one key which needs to be copied from one driver to another.

######## 2. CryIfMaxSizeOfKeyElement

- **UUID**: `cebab948-8930-4dcc-8e25-afb05a5f5b22`
- **参数名**: `CryIfMaxSizeOfKeyElement`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `32`
- **取值范围**: [1..4294967295]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Size of the largest key element which needs to be copied from one driver to another.

####### BOOLEAN 类型参数

######## 1. CryIfDevErrorDetect

- **UUID**: `529cbdde-9949-44c3-8b46-e57127772611`
- **参数名**: `CryIfDevErrorDetect`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Switches the development error detection and notification on or off.

######## 2. CryIfVersionInfoApi

- **UUID**: `b70b2cdc-5423-45ff-8609-387c8f5f9940`
- **参数名**: `CryIfVersionInfoApi`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Pre-processor switch to enable and disable availability of the API CryIf_GetVersionInfo().

######## 3. CryIfRedirection

- **UUID**: `19e714cf-8882-4c83-947d-818cc53d132c`
- **参数名**: `CryIfRedirection`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: If enabled, the CryIf supports the redirection feature of ASR 4.4. It is mandatory that the used Csm is also capable of this feature.
If disabled, the CryIf ignores any kind of redirection.

######## 4. CryIfSafeBswChecks

- **UUID**: `b5ae2e19-a65b-458b-9c6c-4169584e148b`
- **参数名**: `CryIfSafeBswChecks`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Enables safety checks. These checks improve robustness. E.g. invalid parameters are checked before function is executed. This attribute has to be enabled for safety projects where this component is mapped to an ASIL partition.

##### 3. CryIfKey

**容器属性**:

- **UUID**: `b2d0f7df-dbc6-4329-980a-351cc558fc63`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CryIfKey`
- **多重性**: [1..infinite]
- **需要索引**: false

**容器描述**:

Container for incorporation of CryIfKey.

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. CryIfKeyId

- **UUID**: `326f0a7c-8669-4b5e-88da-2e8af3ca5a54`
- **参数名**: `CryIfKeyId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **需要索引**: false
- **描述**: Identifier of the CryIf key.

###### 引用关系

此容器包含 **1** 个引用：

####### SYMBOLIC-NAME-REFERENCE 类型引用

######## 1. CryIfKeyRef

- **UUID**: `2b776d9e-016d-402f-b64f-2556a4c9cf02`
- **引用名**: `CryIfKeyRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `CryptoKey`
- **完整路径**: `/AUTOSAR/EcucDefs/Crypto/CryptoKeys/CryptoKey`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: This parameter refers to the crypto driver key.

##### 4. CryIfCryptoModule

**容器属性**:

- **UUID**: `da5ccd59-f6b8-49dc-9d78-d70b7e6ce92f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CryIfCryptoModule`
- **多重性**: [1..infinite]
- **需要索引**: false

**容器描述**:

Container for incorporation of Crypto Modules

###### 参数配置

此容器包含 **5** 个参数：

####### BOOLEAN 类型参数

######## 1. CryIfSupportsKeyElementCopyPartial

- **UUID**: `c20d2cec-ead8-47b7-9664-f9245fcacc70`
- **参数名**: `CryIfSupportsKeyElementCopyPartial`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: If enabled, the referenced driver is capable of the Service Crypto_KeyElementCopyPartial. This API is available since ASR 4.4.x.

######## 2. CryIfCancelJobApiUsesJobType

- **UUID**: `ce7d8635-5d0f-44db-8e0c-ff25c02d192f`
- **参数名**: `CryIfCancelJobApiUsesJobType`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Specifies whether the referenced driver's Job Cancellation interface uses the Crypto_JobType instead of the Crypto_JobInfoType data type.

Set to TRUE for compatibility with ASR R19-11 and the MICROSAR crypto driver.
Set to FALSE for compatibility with third-party crypto drivers implementing ASR 4.4 and older.

Attention: There is an inconsistency in the ASR specs 4.4 and older which, by default, makes it impossible to implement this interface in standard-compliant way. If you set this switch to FALSE, you also need to set the parameter /MICROSAR/Csm/CsmGeneral/CsmJobTypeLayout/CsmJobTypeLayoutVarMembers to TRUE. This circumvents the limitations of the ASR spec and makes it possible to provide a compliant interface.
Note that this Csm switch only exists in MICROSAR Csm 4.2.0 and above. In MICROSAR Csm versions earlier than 5.1.0, the switch resides directly under Csm/CsmGeneral.

####### STRING 类型参数

######## 1. CryIfCryptoIncludeFile

- **UUID**: `8581c0c4-aa8e-4474-aed0-d4672ca6e115`
- **参数名**: `CryIfCryptoIncludeFile`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **字符串变体**:
  - 默认值: `Crypto.h`
  - 最小长度: 3
- **描述**: Include file of the Crypto module. If CryIfCryptoIncludeFile is not existent, the following pattern is applied for inclusion: Crypto_{Vendor Id}_{Vendor Api Infix}.h

######## 2. CryIfCryptoMip

- **UUID**: `53df0fd4-3a16-4d0e-9cb4-021dbaa510b5`
- **参数名**: `CryIfCryptoMip`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **字符串变体**:
  - 默认值: `Crypto`
  - 最小长度: 1
- **描述**: Module implementation prefix for the referenced Crypto Module. If not set, then the Mip is determined from BSW-Configuration in the following way:  Crypto_{Vendor Id}_{Vendor Api Infix}

######## 3. CryIfCryptoKeySetValidAPI

- **UUID**: `26010ec9-75d0-423c-b34f-2ddb2e3eb7cd`
- **参数名**: `CryIfCryptoKeySetValidAPI`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **字符串变体**:
  - 默认值: `KeySetValid`
  - 最小长度: 1
- **描述**: The Crypto Api Crypto_KeyValidSet was renamed in ASR 4.3.1 to Crypto_KeySetValid. In order to ensure compatibility, this parameter enables renaming the API call to the corresponding Crypto driver.

If this parameter is not present, CryIf will default to KeyValidSet.

###### 引用关系

此容器包含 **1** 个引用：

####### FOREIGN-REFERENCE 类型引用

######## 1. CryIfCryptoModuleRef

- **UUID**: `2056c813-d4d8-492e-b38f-17cc86be71ca`
- **引用名**: `CryIfCryptoModuleRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [1..1]
- **目标类型**: ECUC-MODULE-CONFIGURATION-VALUES
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **需要索引**: false
- **描述**: Reference to the Crypto Driver

## 📦 包结构

此ARXML文件包含 **1** 个包：

### 1. MICROSAR

- **UUID**: `ff55d029-386d-43a2-b3c2-dfef4c7a5e36`
- **包名称**: `MICROSAR`
- **包含元素数量**: 4

#### 包含的元素

##### ECUC-MODULE-DEF 类型元素

1. **CryIf**

##### BSW-IMPLEMENTATION 类型元素

1. **CryIf_Impl**

##### ECUC-MODULE-CONFIGURATION-VALUES 类型元素

1. **CryIf_Pre**
2. **CryIf_Rec**

## ⚡ 实现信息

此ARXML文件包含 **1** 个实现：

### 1. CryIf_Impl

- **UUID**: `1b928b59-9187-464e-be5b-b87115a6887b`
- **实现名称**: `CryIf_Impl`
- **编程语言**: C
- **软件版本**: 5.01.00
- **供应商ID**: 30
- **AUTOSAR版本**: 4.04.00
- **代码生成器**: DaVinci Configurator

## ⚙️ 配置信息

此ARXML文件包含 **2** 个配置：

### 1. CryIf_Pre

- **UUID**: `06535b4d-d414-4b2f-a39b-200cd15ac4d8`
- **配置名称**: `CryIf_Pre`
- **定义引用**: `/MICROSAR/CryIf`

### 2. CryIf_Rec

- **UUID**: `7b16aa88-78d6-47a2-8659-c1016052e587`
- **配置名称**: `CryIf_Rec`
- **定义引用**: `/MICROSAR/CryIf`
