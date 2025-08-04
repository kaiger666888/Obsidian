# CryIf - 完整配置文档

*此文档由ARXML文件自动生成，采用层次化结构展示*

**生成时间**: 2025-06-16 14:51:39

## 📑 目录

- [📄 文件信息](#-文件信息)
- [🔧 模块定义](#-模块定义)
  - [CryIf](#cryif)
- [📦 包结构](#-包结构)

## 📄 文件信息

### Schema信息
- **Schema位置**: `http://autosar.org/schema/r4.0 AUTOSAR_4-0-3.xsd`
- **命名空间**: `http://autosar.org/schema/r4.0`

## 🔧 模块定义

### 1. CryIf

#### 基本信息

- **UUID**: `5c356f6b-b245-448d-ab87-a187670dfc09`
- **模块名称**: `CryIf`
- **类别**: `STANDARDIZED_MODULE_DEFINITION`
- **多重性**: [0..1]
- **支持的变体**:
  - VARIANT-PRE-COMPILE

#### 模块描述

Configuration of the Crypto Interface.

#### 配置容器

本模块包含 **3** 个配置容器：

##### 1. CryIfChannel

**容器属性**:

- **UUID**: `91a69947-1657-4d8d-b5bd-16b642e663ba`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CryIfChannel`
- **多重性**: [0..infinite]
- **构建后可变**: false

**容器描述**:

Container for incorporation of CryIfChannel.

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. CryIfChannelId

- **UUID**: `ce4895de-0771-4952-a43b-8f9e45ef12e9`
- **参数名**: `CryIfChannelId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Identifier of the crypto channel

###### 引用关系

此容器包含 **1** 个引用：

####### SYMBOLIC-NAME-REFERENCE 类型引用

######## 1. CryIfDriverObjectRef

- **UUID**: `6a9a7df6-6b56-4018-b1f4-783319d3b03c`
- **引用名**: `CryIfDriverObjectRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `CryptoDriverObject`
- **完整路径**: `/AUTOSAR/EcucDefs/Crypto/CryptoDriverObjects/CryptoDriverObject`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter refers to a Crypto Driver Object.

##### 2. CryIfGeneral

**容器属性**:

- **UUID**: `6b9a23ff-1bfa-417c-9a9d-0b1a5a821159`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CryIfGeneral`
- **多重性**: [1..1]
- **构建后可变**: false

**容器描述**:

Container for common configuration options.

###### 参数配置

此容器包含 **2** 个参数：

####### BOOLEAN 类型参数

######## 1. CryIfDevErrorDetect

- **UUID**: `0130d24e-7814-434e-976c-89786e823298`
- **参数名**: `CryIfDevErrorDetect`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Switches the development error detection and notification on or off. 
  true: detection and notification is enabled. 
  false: detection and notification is disabled.

######## 2. CryIfVersionInfoApi

- **UUID**: `b70b2cdc-5423-45ff-8609-387c8f5f9940`
- **参数名**: `CryIfVersionInfoApi`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Pre-processor switch to enable and disable availability of the API CryIf_GetVersionInfo().

##### 3. CryIfKey

**容器属性**:

- **UUID**: `f8a4b7b7-b5cd-467e-8146-2767bbc8674a`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CryIfKey`
- **多重性**: [0..infinite]
- **构建后可变**: false

**容器描述**:

Container for Channel configuration

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. CryIfKeyId

- **UUID**: `290b1e96-3cdf-4301-8ecf-08eff0297f1f`
- **参数名**: `CryIfKeyId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Identifier of the key.

###### 引用关系

此容器包含 **1** 个引用：

####### SYMBOLIC-NAME-REFERENCE 类型引用

######## 1. CryIfKeyRef

- **UUID**: `8587f0ef-1152-40e2-b7b0-e404af0329d9`
- **引用名**: `CryIfKeyRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `CryptoKey`
- **完整路径**: `/AUTOSAR/EcucDefs/Crypto/CryptoKeys/CryptoKey`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter refers to the crypto driver key.

## 📦 包结构

此ARXML文件包含 **2** 个包：

### 1. AUTOSAR

- **UUID**: `4b4a8b92-464b-4bfd-b3f4-a30f04980120`
- **包名称**: `AUTOSAR`
- **包含元素数量**: 0

### 2. EcucDefs

- **UUID**: `f65e9e5a-9bce-474f-981c-79940a8dda59`
- **包名称**: `EcucDefs`
- **包含元素数量**: 1

#### 包含的元素

##### ECUC-MODULE-DEF 类型元素

1. **CryIf**
