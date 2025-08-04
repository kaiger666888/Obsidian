# IoHwAb - 完整配置文档

*此文档由ARXML文件自动生成，采用层次化结构展示*

**生成时间**: 2025-06-16 14:45:01

## 📑 目录

- [📄 文件信息](#-文件信息)
- [🔧 模块定义](#-模块定义)
  - [IoHwAb](#iohwab)
- [📦 包结构](#-包结构)
- [⚡ 实现信息](#-实现信息)
- [⚙️ 配置信息](#️-配置信息)

## 📄 文件信息

### Schema信息
- **Schema位置**: `http://autosar.org/schema/r4.0 autosar_4-0-3.xsd`
- **命名空间**: `http://autosar.org/schema/r4.0`

## 🔧 模块定义

### 1. IoHwAb

#### 基本信息

- **UUID**: `1411505c-b6a6-4f01-accb-8e996b92ca84`
- **模块名称**: `IoHwAb`
- **类别**: `VENDOR_SPECIFIC_MODULE_DEFINITION`
- **多重性**: [0..1]
- **支持的变体**:
  - VARIANT-PRE-COMPILE

#### 模块描述

Configuration of the I/O Hardware Abstraction module

#### 版本历史

共有 **25** 个版本记录：

##### 1. 版本 1.02.00

- **状态**: beta
- **发布日期**: 2008-07-10T08:18:29Z
- **发布者**: vircer

**变更内容**:

##### 2. 版本 1.02.01

- **发布日期**: 2008-07-10T08:19:54Z
- **发布者**: vircer

**变更内容**:

##### 3. 版本 1.02.02

- **发布日期**: 2008-08-21T22:26:53Z
- **发布者**: vircer

**变更内容**:

##### 4. 版本 1.03.00

- **发布日期**: 2008-10-02T16:18:14Z
- **发布者**: vircer

**变更内容**:

##### 5. 版本 1.04.00

- **状态**: released
- **发布日期**: 2008-12-10T08:35:15Z
- **发布者**: vircer

**变更内容**:

##### 6. 版本 1.04.01

- **状态**: released
- **发布日期**: 2009-02-24T10:11:18Z
- **发布者**: vircer

**变更内容**:

##### 7. 版本 1.04.02

- **状态**: released
- **发布日期**: 2009-03-16T16:36:08Z
- **发布者**: vircer

**变更内容**:

##### 8. 版本 1.04.03

- **状态**: released
- **发布日期**: 2009-07-09T11:39:47Z
- **发布者**: vircer

**变更内容**:

##### 9. 版本 1.04.04

- **状态**: released
- **发布日期**: 2009-09-23T09:13:05Z
- **发布者**: vircer

**变更内容**:

##### 10. 版本 1.04.05

- **状态**: released
- **发布日期**: 2010-04-21T17:45:23Z
- **发布者**: vircer

**变更内容**:

##### 11. 版本 1.04.06

- **状态**: released
- **发布日期**: 2010-11-26T09:32:53Z
- **发布者**: vircer

**变更内容**:

##### 12. 版本 2.00.00

- **状态**: -
- **发布日期**: 2012-07-11T08:22:28+02:00
- **发布者**: vircer

**变更内容**:

##### 13. 版本 

- **状态**: -
- **发布日期**: 2012-08-14T04:21:30+02:00
- **发布者**: virmfr

**变更内容**:

##### 14. 版本 2.00.01

- **发布日期**: 2012-11-08T12:46:43+01:00
- **发布者**: vircer

**变更内容**:

##### 15. 版本 2.00.02

- **发布日期**: 2012-12-07T09:10:49+01:00
- **发布者**: vircer

**变更内容**:

##### 16. 版本 3.00.00

- **发布日期**: 2013-03-04T02:34:16+01:00
- **发布者**: vircer

**变更内容**:

##### 17. 版本 4.00.00

- **发布日期**: 2013-09-02T03:06:22+02:00
- **发布者**: vircer

**变更内容**:

##### 18. 版本 4.00.01

- **发布日期**: 2014-05-28T01:57:09+02:00
- **发布者**: virchl

**变更内容**:

##### 19. 版本 4.00.01

- **发布日期**: 2014-05-28T01:58:06+02:00
- **发布者**: virchl

**变更内容**:

##### 20. 版本 4.00.02

- **发布日期**: 2014-11-05T02:23:24+01:00
- **发布者**: virchl

**变更内容**:

##### 21. 版本 4.00.03

- **发布日期**: 2015-03-05T04:54:18+01:00
- **发布者**: virchl

**变更内容**:

##### 22. 版本 4.00.03

- **发布日期**: 2015-03-05T04:54:57+01:00
- **发布者**: virchl

**变更内容**:

##### 23. 版本 4.00.04

- **发布日期**: 2015-06-01T09:11:20+02:00
- **发布者**: virchl

**变更内容**:

##### 24. 版本 4.01.00

- **发布日期**: 2015-06-16T05:02:12+02:00
- **发布者**: virchl

**变更内容**:

##### 25. 版本 4.02.00

- **发布日期**: 2018-04-03T10:57:56+02:00
- **发布者**: virchl

**变更内容**:

#### 配置容器

本模块包含 **41** 个配置容器：

##### 1. IoHwAbGeneral

**容器属性**:

- **UUID**: `04878aa0-f789-40ca-8a2a-47cf9d610e05`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IoHwAbGeneral`
- **多重性**: [1..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container contains common configuration options for the I/O Hardware Abstraction module.

###### 参数配置

此容器包含 **4** 个参数：

####### BOOLEAN 类型参数

######## 1. IoHwAbDevErrorDetect

- **UUID**: `db7224c8-bac2-4faf-914a-d5904748f2f4`
- **参数名**: `IoHwAbDevErrorDetect`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter enables/disables development error detection and reporting.

######## 2. IoHwAbVersionInfoApi

- **UUID**: `4e4803dd-c1ce-4bbf-acbd-ec4659f6855d`
- **参数名**: `IoHwAbVersionInfoApi`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Pre-processor switch to enable/disable the API to read out the modules version information.

Note: The function will be removed from the code completely.

######## 3. IoHwAbUseInitFunction

- **UUID**: `3b299c26-f1cc-46fd-aa73-319add1db674`
- **参数名**: `IoHwAbUseInitFunction`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Pre-processor switch to enable/disable the Initialization-API.

Note: The function will be removed from the code completely.

####### STRING 类型参数

######## 1. IoHwAbCfgIncludeList

- **UUID**: `dd6f3e88-0a68-42f1-97f1-b1f8a7154a02`
- **参数名**: `IoHwAbCfgIncludeList`
- **数据类型**: STRING
- **多重性**: [0..infinite]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **字符串变体**:
  - 默认值: `Dio.h`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Include List for used basic software component headers.

##### 2. IoHwAbDatatypes

**容器属性**:

- **UUID**: `43a79e59-99a7-4f8f-a84e-e81e864a5ab3`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IoHwAbDatatypes`
- **多重性**: [1..1]
- **构建后可变**: false

**容器描述**:

Container for the data types configuration. There is a set of base types that cannot be changed, but can be used to create implementation specific types (Type references, Arrays or Structs/Records).

###### 配置容器

本模块包含 **17** 个配置容器：

####### 1. IoHwAbImplementationTypes

**容器属性**:

- **UUID**: `c6d9e636-ceb5-41f8-9c06-5828cc7cf45e`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IoHwAbImplementationTypes`
- **多重性**: [1..1]
- **构建后可变**: false

**容器描述**:

Container for the implementation specific datatypes. Implementation specific datatypes can be configured/assembled by using base datatypes.

######## 配置容器

本模块包含 **15** 个配置容器：

######### 1. IoHwAbTypeReference

**容器属性**:

- **UUID**: `4c4ad53e-8366-4d22-99a4-1ab863f99edf`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IoHwAbTypeReference`
- **多重性**: [0..infinite]
- **构建后可变**: false

**容器描述**:

Container for configuring a type reference. A type reference is a deviation from a base type, i.e. the generated files (e.g. Rte_Type.h) will contain a typedef like the following example:

typedef sint8 BatteryVoltageValue;

########## 引用关系

此容器包含 **1** 个引用：

########### CHOICE-REFERENCE 类型引用

############ 1. IoHwAbTypeReferenceTypeRef

- **UUID**: `be6126a0-a374-41f1-9a7a-9cf53955a504`
- **引用名**: `IoHwAbTypeReferenceTypeRef`
- **引用类型**: CHOICE-REFERENCE
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **需要索引**: false
- **目标引用列表**:
  - `/MICROSAR/IoHwAb/IoHwAbDatatypes/IoHwAbBaseType`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Parameter for the selection of the datatype of the type reference.

########## 配置容器

本模块包含 **11** 个配置容器：

########### 1. IoHwAbInvalidValue

**容器属性**:

- **UUID**: `5ca5978e-f620-4c40-ace2-df3e7b3618de`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IoHwAbInvalidValue`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Optional container for configuring an invalid value for a IoHwAb type reference.

############ 配置容器

本模块包含 **10** 个配置容器：

############# 1. IoHwAbInvalidValueBoolean

**容器属性**:

- **UUID**: `fbc4e248-f3c8-4bc8-bbd2-bfb6677b5882`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IoHwAbInvalidValueBoolean`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container for configuring an invalid value of a type "boolean".

############## 参数配置

此容器包含 **1** 个参数：

############### BOOLEAN 类型参数

################ 1. IoHwAbInvalidValue

- **UUID**: `359e7e9b-bd3d-4c1d-b8df-a0b34939f158`
- **参数名**: `IoHwAbInvalidValue`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This field contains the initial value of a type "boolean".

############# 2. IoHwAbInvalidValueFloat32

**容器属性**:

- **UUID**: `2f2e9da1-4c91-46a2-a9d5-d4efeae48c26`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IoHwAbInvalidValueFloat32`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container for configuring an invalid value of a type "float32".

############## 参数配置

此容器包含 **1** 个参数：

############### FLOAT 类型参数

################ 1. IoHwAbInvalidValue

- **UUID**: `d1e30bf3-35b3-41d7-bdda-eb28b3ec0419`
- **参数名**: `IoHwAbInvalidValue`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This field contains the initial value of a type "float32".

############# 3. IoHwAbInvalidValueFloat64

**容器属性**:

- **UUID**: `e9b907e5-22e6-4ce2-9f2a-6adebe0d3ce5`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IoHwAbInvalidValueFloat64`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container for configuring an invalid value of a type "float64".

############## 参数配置

此容器包含 **1** 个参数：

############### FLOAT 类型参数

################ 1. IoHwAbInvalidValue

- **UUID**: `f815ed02-2ff3-4495-aabf-26014c7ad01f`
- **参数名**: `IoHwAbInvalidValue`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This field contains the initial value of a type "float64".

############# 4. IoHwAbInvalidValueUint8

**容器属性**:

- **UUID**: `f465b96c-d804-4e17-a5ff-ad10d1057eee`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IoHwAbInvalidValueUint8`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container for configuring an invalid value of a type "uint8".

############## 参数配置

此容器包含 **1** 个参数：

############### INTEGER 类型参数

################ 1. IoHwAbInvalidValue

- **UUID**: `f1411f40-dceb-4ec6-97c7-4776f921515a`
- **参数名**: `IoHwAbInvalidValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This field contains the initial value of a type "uint8".

############# 5. IoHwAbInvalidValueUint16

**容器属性**:

- **UUID**: `1f4065c4-b767-4ba2-afe4-c34ac1d97539`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IoHwAbInvalidValueUint16`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container for configuring an invalid value of a type "uint16".

############## 参数配置

此容器包含 **1** 个参数：

############### INTEGER 类型参数

################ 1. IoHwAbInvalidValue

- **UUID**: `76ea2c11-a275-4ff5-9ed1-e2f81e3739b8`
- **参数名**: `IoHwAbInvalidValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This field contains the initial value of a type "uint16".

############# 6. IoHwAbInvalidValueUint32

**容器属性**:

- **UUID**: `2cfbeb44-2968-420f-915f-e456f924f21f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IoHwAbInvalidValueUint32`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container for configuring an invalid value of a type "uint32".

############## 参数配置

此容器包含 **1** 个参数：

############### INTEGER 类型参数

################ 1. IoHwAbInvalidValue

- **UUID**: `41a8d144-1c90-4172-8612-17fd061a8e44`
- **参数名**: `IoHwAbInvalidValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This field contains the initial value of a type "uint32".

############# 7. IoHwAbInvalidValueSint8

**容器属性**:

- **UUID**: `7f46cafe-67b7-498a-b02e-33d259394573`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IoHwAbInvalidValueSint8`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container for configuring an invalid value of a type "sint8".

############## 参数配置

此容器包含 **1** 个参数：

############### INTEGER 类型参数

################ 1. IoHwAbInvalidValue

- **UUID**: `6993ab73-5d35-46ca-86b2-88b5812ca176`
- **参数名**: `IoHwAbInvalidValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [-128..127]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This field contains the initial value of a type "sint8".

############# 8. IoHwAbInvalidValueSint16

**容器属性**:

- **UUID**: `180d975a-2f07-4a24-981f-fd72bc383eb3`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IoHwAbInvalidValueSint16`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container for configuring an invalid value of a type "sint16".

############## 参数配置

此容器包含 **1** 个参数：

############### INTEGER 类型参数

################ 1. IoHwAbInvalidValue

- **UUID**: `f05ebe07-97ab-41d8-831f-9c6c96be8449`
- **参数名**: `IoHwAbInvalidValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [-32768..32767]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This field contains the initial value of a type "sint16".

############# 9. IoHwAbInvalidValueSint32

**容器属性**:

- **UUID**: `e491e955-5ee9-4f76-8b97-ce3df8a76bb3`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IoHwAbInvalidValueSint32`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container for configuring an invalid value of a type "sint32".

############## 参数配置

此容器包含 **1** 个参数：

############### INTEGER 类型参数

################ 1. IoHwAbInvalidValue

- **UUID**: `5216a15f-52b0-4be2-91b5-e2fc593c86d2`
- **参数名**: `IoHwAbInvalidValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [-2147483648..2147483647]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This field contains the initial value of a type "sint32".

############# 10. IoHwAbInvalidValueType

**容器属性**:

- **UUID**: `289ed971-2914-4549-8220-d6145f506b72`
- **容器类型**: CHOICE-CONTAINER
- **容器名称**: `IoHwAbInvalidValueType`
- **多重性**: [1..1]
- **构建后可变**: false

**容器选择**:

- **IoHwAbInvalidValueBoolean**
  - UUID: `fbc4e248-f3c8-4bc8-bbd2-bfb6677b5882`
  - 描述: Container for configuring an invalid value of a type "boolean".
- **IoHwAbInvalidValueFloat32**
  - UUID: `2f2e9da1-4c91-46a2-a9d5-d4efeae48c26`
  - 描述: Container for configuring an invalid value of a type "float32".
- **IoHwAbInvalidValueFloat64**
  - UUID: `e9b907e5-22e6-4ce2-9f2a-6adebe0d3ce5`
  - 描述: Container for configuring an invalid value of a type "float64".
- **IoHwAbInvalidValueUint8**
  - UUID: `f465b96c-d804-4e17-a5ff-ad10d1057eee`
  - 描述: Container for configuring an invalid value of a type "uint8".
- **IoHwAbInvalidValueUint16**
  - UUID: `1f4065c4-b767-4ba2-afe4-c34ac1d97539`
  - 描述: Container for configuring an invalid value of a type "uint16".
- **IoHwAbInvalidValueUint32**
  - UUID: `2cfbeb44-2968-420f-915f-e456f924f21f`
  - 描述: Container for configuring an invalid value of a type "uint32".
- **IoHwAbInvalidValueSint8**
  - UUID: `7f46cafe-67b7-498a-b02e-33d259394573`
  - 描述: Container for configuring an invalid value of a type "sint8".
- **IoHwAbInvalidValueSint16**
  - UUID: `180d975a-2f07-4a24-981f-fd72bc383eb3`
  - 描述: Container for configuring an invalid value of a type "sint16".
- **IoHwAbInvalidValueSint32**
  - UUID: `e491e955-5ee9-4f76-8b97-ce3df8a76bb3`
  - 描述: Container for configuring an invalid value of a type "sint32".

**容器描述**:

This choice container is used for instantiating the appropriate type for the invalid value of the referenced data element.

Example: If the type of the referenced base data type is either an "uint8" or a type reference of an "uint8", the container "IoHwAbInvalidValueUint8" shall be chosen.

########### 2. IoHwAbInvalidValueBoolean

**容器属性**:

- **UUID**: `fbc4e248-f3c8-4bc8-bbd2-bfb6677b5882`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IoHwAbInvalidValueBoolean`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container for configuring an invalid value of a type "boolean".

############ 参数配置

此容器包含 **1** 个参数：

############# BOOLEAN 类型参数

############## 1. IoHwAbInvalidValue

- **UUID**: `359e7e9b-bd3d-4c1d-b8df-a0b34939f158`
- **参数名**: `IoHwAbInvalidValue`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This field contains the initial value of a type "boolean".

########### 3. IoHwAbInvalidValueFloat32

**容器属性**:

- **UUID**: `2f2e9da1-4c91-46a2-a9d5-d4efeae48c26`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IoHwAbInvalidValueFloat32`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container for configuring an invalid value of a type "float32".

############ 参数配置

此容器包含 **1** 个参数：

############# FLOAT 类型参数

############## 1. IoHwAbInvalidValue

- **UUID**: `d1e30bf3-35b3-41d7-bdda-eb28b3ec0419`
- **参数名**: `IoHwAbInvalidValue`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This field contains the initial value of a type "float32".

########### 4. IoHwAbInvalidValueFloat64

**容器属性**:

- **UUID**: `e9b907e5-22e6-4ce2-9f2a-6adebe0d3ce5`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IoHwAbInvalidValueFloat64`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container for configuring an invalid value of a type "float64".

############ 参数配置

此容器包含 **1** 个参数：

############# FLOAT 类型参数

############## 1. IoHwAbInvalidValue

- **UUID**: `f815ed02-2ff3-4495-aabf-26014c7ad01f`
- **参数名**: `IoHwAbInvalidValue`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This field contains the initial value of a type "float64".

########### 5. IoHwAbInvalidValueUint8

**容器属性**:

- **UUID**: `f465b96c-d804-4e17-a5ff-ad10d1057eee`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IoHwAbInvalidValueUint8`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container for configuring an invalid value of a type "uint8".

############ 参数配置

此容器包含 **1** 个参数：

############# INTEGER 类型参数

############## 1. IoHwAbInvalidValue

- **UUID**: `f1411f40-dceb-4ec6-97c7-4776f921515a`
- **参数名**: `IoHwAbInvalidValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This field contains the initial value of a type "uint8".

########### 6. IoHwAbInvalidValueUint16

**容器属性**:

- **UUID**: `1f4065c4-b767-4ba2-afe4-c34ac1d97539`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IoHwAbInvalidValueUint16`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container for configuring an invalid value of a type "uint16".

############ 参数配置

此容器包含 **1** 个参数：

############# INTEGER 类型参数

############## 1. IoHwAbInvalidValue

- **UUID**: `76ea2c11-a275-4ff5-9ed1-e2f81e3739b8`
- **参数名**: `IoHwAbInvalidValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This field contains the initial value of a type "uint16".

########### 7. IoHwAbInvalidValueUint32

**容器属性**:

- **UUID**: `2cfbeb44-2968-420f-915f-e456f924f21f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IoHwAbInvalidValueUint32`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container for configuring an invalid value of a type "uint32".

############ 参数配置

此容器包含 **1** 个参数：

############# INTEGER 类型参数

############## 1. IoHwAbInvalidValue

- **UUID**: `41a8d144-1c90-4172-8612-17fd061a8e44`
- **参数名**: `IoHwAbInvalidValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This field contains the initial value of a type "uint32".

########### 8. IoHwAbInvalidValueSint8

**容器属性**:

- **UUID**: `7f46cafe-67b7-498a-b02e-33d259394573`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IoHwAbInvalidValueSint8`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container for configuring an invalid value of a type "sint8".

############ 参数配置

此容器包含 **1** 个参数：

############# INTEGER 类型参数

############## 1. IoHwAbInvalidValue

- **UUID**: `6993ab73-5d35-46ca-86b2-88b5812ca176`
- **参数名**: `IoHwAbInvalidValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [-128..127]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This field contains the initial value of a type "sint8".

########### 9. IoHwAbInvalidValueSint16

**容器属性**:

- **UUID**: `180d975a-2f07-4a24-981f-fd72bc383eb3`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IoHwAbInvalidValueSint16`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container for configuring an invalid value of a type "sint16".

############ 参数配置

此容器包含 **1** 个参数：

############# INTEGER 类型参数

############## 1. IoHwAbInvalidValue

- **UUID**: `f05ebe07-97ab-41d8-831f-9c6c96be8449`
- **参数名**: `IoHwAbInvalidValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [-32768..32767]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This field contains the initial value of a type "sint16".

########### 10. IoHwAbInvalidValueSint32

**容器属性**:

- **UUID**: `e491e955-5ee9-4f76-8b97-ce3df8a76bb3`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IoHwAbInvalidValueSint32`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container for configuring an invalid value of a type "sint32".

############ 参数配置

此容器包含 **1** 个参数：

############# INTEGER 类型参数

############## 1. IoHwAbInvalidValue

- **UUID**: `5216a15f-52b0-4be2-91b5-e2fc593c86d2`
- **参数名**: `IoHwAbInvalidValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [-2147483648..2147483647]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This field contains the initial value of a type "sint32".

########### 11. IoHwAbInvalidValueType

**容器属性**:

- **UUID**: `289ed971-2914-4549-8220-d6145f506b72`
- **容器类型**: CHOICE-CONTAINER
- **容器名称**: `IoHwAbInvalidValueType`
- **多重性**: [1..1]
- **构建后可变**: false

**容器选择**:

- **IoHwAbInvalidValueBoolean**
  - UUID: `fbc4e248-f3c8-4bc8-bbd2-bfb6677b5882`
  - 描述: Container for configuring an invalid value of a type "boolean".
- **IoHwAbInvalidValueFloat32**
  - UUID: `2f2e9da1-4c91-46a2-a9d5-d4efeae48c26`
  - 描述: Container for configuring an invalid value of a type "float32".
- **IoHwAbInvalidValueFloat64**
  - UUID: `e9b907e5-22e6-4ce2-9f2a-6adebe0d3ce5`
  - 描述: Container for configuring an invalid value of a type "float64".
- **IoHwAbInvalidValueUint8**
  - UUID: `f465b96c-d804-4e17-a5ff-ad10d1057eee`
  - 描述: Container for configuring an invalid value of a type "uint8".
- **IoHwAbInvalidValueUint16**
  - UUID: `1f4065c4-b767-4ba2-afe4-c34ac1d97539`
  - 描述: Container for configuring an invalid value of a type "uint16".
- **IoHwAbInvalidValueUint32**
  - UUID: `2cfbeb44-2968-420f-915f-e456f924f21f`
  - 描述: Container for configuring an invalid value of a type "uint32".
- **IoHwAbInvalidValueSint8**
  - UUID: `7f46cafe-67b7-498a-b02e-33d259394573`
  - 描述: Container for configuring an invalid value of a type "sint8".
- **IoHwAbInvalidValueSint16**
  - UUID: `180d975a-2f07-4a24-981f-fd72bc383eb3`
  - 描述: Container for configuring an invalid value of a type "sint16".
- **IoHwAbInvalidValueSint32**
  - UUID: `e491e955-5ee9-4f76-8b97-ce3df8a76bb3`
  - 描述: Container for configuring an invalid value of a type "sint32".

**容器描述**:

This choice container is used for instantiating the appropriate type for the invalid value of the referenced data element.

Example: If the type of the referenced base data type is either an "uint8" or a type reference of an "uint8", the container "IoHwAbInvalidValueUint8" shall be chosen.

######### 2. IoHwAbInvalidValue

**容器属性**:

- **UUID**: `5ca5978e-f620-4c40-ace2-df3e7b3618de`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IoHwAbInvalidValue`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Optional container for configuring an invalid value for a IoHwAb type reference.

########## 配置容器

本模块包含 **10** 个配置容器：

########### 1. IoHwAbInvalidValueBoolean

**容器属性**:

- **UUID**: `fbc4e248-f3c8-4bc8-bbd2-bfb6677b5882`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IoHwAbInvalidValueBoolean`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container for configuring an invalid value of a type "boolean".

############ 参数配置

此容器包含 **1** 个参数：

############# BOOLEAN 类型参数

############## 1. IoHwAbInvalidValue

- **UUID**: `359e7e9b-bd3d-4c1d-b8df-a0b34939f158`
- **参数名**: `IoHwAbInvalidValue`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This field contains the initial value of a type "boolean".

########### 2. IoHwAbInvalidValueFloat32

**容器属性**:

- **UUID**: `2f2e9da1-4c91-46a2-a9d5-d4efeae48c26`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IoHwAbInvalidValueFloat32`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container for configuring an invalid value of a type "float32".

############ 参数配置

此容器包含 **1** 个参数：

############# FLOAT 类型参数

############## 1. IoHwAbInvalidValue

- **UUID**: `d1e30bf3-35b3-41d7-bdda-eb28b3ec0419`
- **参数名**: `IoHwAbInvalidValue`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This field contains the initial value of a type "float32".

########### 3. IoHwAbInvalidValueFloat64

**容器属性**:

- **UUID**: `e9b907e5-22e6-4ce2-9f2a-6adebe0d3ce5`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IoHwAbInvalidValueFloat64`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container for configuring an invalid value of a type "float64".

############ 参数配置

此容器包含 **1** 个参数：

############# FLOAT 类型参数

############## 1. IoHwAbInvalidValue

- **UUID**: `f815ed02-2ff3-4495-aabf-26014c7ad01f`
- **参数名**: `IoHwAbInvalidValue`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This field contains the initial value of a type "float64".

########### 4. IoHwAbInvalidValueUint8

**容器属性**:

- **UUID**: `f465b96c-d804-4e17-a5ff-ad10d1057eee`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IoHwAbInvalidValueUint8`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container for configuring an invalid value of a type "uint8".

############ 参数配置

此容器包含 **1** 个参数：

############# INTEGER 类型参数

############## 1. IoHwAbInvalidValue

- **UUID**: `f1411f40-dceb-4ec6-97c7-4776f921515a`
- **参数名**: `IoHwAbInvalidValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This field contains the initial value of a type "uint8".

########### 5. IoHwAbInvalidValueUint16

**容器属性**:

- **UUID**: `1f4065c4-b767-4ba2-afe4-c34ac1d97539`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IoHwAbInvalidValueUint16`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container for configuring an invalid value of a type "uint16".

############ 参数配置

此容器包含 **1** 个参数：

############# INTEGER 类型参数

############## 1. IoHwAbInvalidValue

- **UUID**: `76ea2c11-a275-4ff5-9ed1-e2f81e3739b8`
- **参数名**: `IoHwAbInvalidValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This field contains the initial value of a type "uint16".

########### 6. IoHwAbInvalidValueUint32

**容器属性**:

- **UUID**: `2cfbeb44-2968-420f-915f-e456f924f21f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IoHwAbInvalidValueUint32`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container for configuring an invalid value of a type "uint32".

############ 参数配置

此容器包含 **1** 个参数：

############# INTEGER 类型参数

############## 1. IoHwAbInvalidValue

- **UUID**: `41a8d144-1c90-4172-8612-17fd061a8e44`
- **参数名**: `IoHwAbInvalidValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This field contains the initial value of a type "uint32".

########### 7. IoHwAbInvalidValueSint8

**容器属性**:

- **UUID**: `7f46cafe-67b7-498a-b02e-33d259394573`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IoHwAbInvalidValueSint8`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container for configuring an invalid value of a type "sint8".

############ 参数配置

此容器包含 **1** 个参数：

############# INTEGER 类型参数

############## 1. IoHwAbInvalidValue

- **UUID**: `6993ab73-5d35-46ca-86b2-88b5812ca176`
- **参数名**: `IoHwAbInvalidValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [-128..127]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This field contains the initial value of a type "sint8".

########### 8. IoHwAbInvalidValueSint16

**容器属性**:

- **UUID**: `180d975a-2f07-4a24-981f-fd72bc383eb3`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IoHwAbInvalidValueSint16`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container for configuring an invalid value of a type "sint16".

############ 参数配置

此容器包含 **1** 个参数：

############# INTEGER 类型参数

############## 1. IoHwAbInvalidValue

- **UUID**: `f05ebe07-97ab-41d8-831f-9c6c96be8449`
- **参数名**: `IoHwAbInvalidValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [-32768..32767]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This field contains the initial value of a type "sint16".

########### 9. IoHwAbInvalidValueSint32

**容器属性**:

- **UUID**: `e491e955-5ee9-4f76-8b97-ce3df8a76bb3`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IoHwAbInvalidValueSint32`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container for configuring an invalid value of a type "sint32".

############ 参数配置

此容器包含 **1** 个参数：

############# INTEGER 类型参数

############## 1. IoHwAbInvalidValue

- **UUID**: `5216a15f-52b0-4be2-91b5-e2fc593c86d2`
- **参数名**: `IoHwAbInvalidValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [-2147483648..2147483647]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This field contains the initial value of a type "sint32".

########### 10. IoHwAbInvalidValueType

**容器属性**:

- **UUID**: `289ed971-2914-4549-8220-d6145f506b72`
- **容器类型**: CHOICE-CONTAINER
- **容器名称**: `IoHwAbInvalidValueType`
- **多重性**: [1..1]
- **构建后可变**: false

**容器选择**:

- **IoHwAbInvalidValueBoolean**
  - UUID: `fbc4e248-f3c8-4bc8-bbd2-bfb6677b5882`
  - 描述: Container for configuring an invalid value of a type "boolean".
- **IoHwAbInvalidValueFloat32**
  - UUID: `2f2e9da1-4c91-46a2-a9d5-d4efeae48c26`
  - 描述: Container for configuring an invalid value of a type "float32".
- **IoHwAbInvalidValueFloat64**
  - UUID: `e9b907e5-22e6-4ce2-9f2a-6adebe0d3ce5`
  - 描述: Container for configuring an invalid value of a type "float64".
- **IoHwAbInvalidValueUint8**
  - UUID: `f465b96c-d804-4e17-a5ff-ad10d1057eee`
  - 描述: Container for configuring an invalid value of a type "uint8".
- **IoHwAbInvalidValueUint16**
  - UUID: `1f4065c4-b767-4ba2-afe4-c34ac1d97539`
  - 描述: Container for configuring an invalid value of a type "uint16".
- **IoHwAbInvalidValueUint32**
  - UUID: `2cfbeb44-2968-420f-915f-e456f924f21f`
  - 描述: Container for configuring an invalid value of a type "uint32".
- **IoHwAbInvalidValueSint8**
  - UUID: `7f46cafe-67b7-498a-b02e-33d259394573`
  - 描述: Container for configuring an invalid value of a type "sint8".
- **IoHwAbInvalidValueSint16**
  - UUID: `180d975a-2f07-4a24-981f-fd72bc383eb3`
  - 描述: Container for configuring an invalid value of a type "sint16".
- **IoHwAbInvalidValueSint32**
  - UUID: `e491e955-5ee9-4f76-8b97-ce3df8a76bb3`
  - 描述: Container for configuring an invalid value of a type "sint32".

**容器描述**:

This choice container is used for instantiating the appropriate type for the invalid value of the referenced data element.

Example: If the type of the referenced base data type is either an "uint8" or a type reference of an "uint8", the container "IoHwAbInvalidValueUint8" shall be chosen.

######### 3. IoHwAbInvalidValueBoolean

**容器属性**:

- **UUID**: `fbc4e248-f3c8-4bc8-bbd2-bfb6677b5882`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IoHwAbInvalidValueBoolean`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container for configuring an invalid value of a type "boolean".

########## 参数配置

此容器包含 **1** 个参数：

########### BOOLEAN 类型参数

############ 1. IoHwAbInvalidValue

- **UUID**: `359e7e9b-bd3d-4c1d-b8df-a0b34939f158`
- **参数名**: `IoHwAbInvalidValue`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This field contains the initial value of a type "boolean".

######### 4. IoHwAbInvalidValueFloat32

**容器属性**:

- **UUID**: `2f2e9da1-4c91-46a2-a9d5-d4efeae48c26`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IoHwAbInvalidValueFloat32`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container for configuring an invalid value of a type "float32".

########## 参数配置

此容器包含 **1** 个参数：

########### FLOAT 类型参数

############ 1. IoHwAbInvalidValue

- **UUID**: `d1e30bf3-35b3-41d7-bdda-eb28b3ec0419`
- **参数名**: `IoHwAbInvalidValue`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This field contains the initial value of a type "float32".

######### 5. IoHwAbInvalidValueFloat64

**容器属性**:

- **UUID**: `e9b907e5-22e6-4ce2-9f2a-6adebe0d3ce5`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IoHwAbInvalidValueFloat64`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container for configuring an invalid value of a type "float64".

########## 参数配置

此容器包含 **1** 个参数：

########### FLOAT 类型参数

############ 1. IoHwAbInvalidValue

- **UUID**: `f815ed02-2ff3-4495-aabf-26014c7ad01f`
- **参数名**: `IoHwAbInvalidValue`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This field contains the initial value of a type "float64".

######### 6. IoHwAbInvalidValueUint8

**容器属性**:

- **UUID**: `f465b96c-d804-4e17-a5ff-ad10d1057eee`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IoHwAbInvalidValueUint8`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container for configuring an invalid value of a type "uint8".

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. IoHwAbInvalidValue

- **UUID**: `f1411f40-dceb-4ec6-97c7-4776f921515a`
- **参数名**: `IoHwAbInvalidValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This field contains the initial value of a type "uint8".

######### 7. IoHwAbInvalidValueUint16

**容器属性**:

- **UUID**: `1f4065c4-b767-4ba2-afe4-c34ac1d97539`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IoHwAbInvalidValueUint16`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container for configuring an invalid value of a type "uint16".

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. IoHwAbInvalidValue

- **UUID**: `76ea2c11-a275-4ff5-9ed1-e2f81e3739b8`
- **参数名**: `IoHwAbInvalidValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This field contains the initial value of a type "uint16".

######### 8. IoHwAbInvalidValueUint32

**容器属性**:

- **UUID**: `2cfbeb44-2968-420f-915f-e456f924f21f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IoHwAbInvalidValueUint32`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container for configuring an invalid value of a type "uint32".

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. IoHwAbInvalidValue

- **UUID**: `41a8d144-1c90-4172-8612-17fd061a8e44`
- **参数名**: `IoHwAbInvalidValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This field contains the initial value of a type "uint32".

######### 9. IoHwAbInvalidValueSint8

**容器属性**:

- **UUID**: `7f46cafe-67b7-498a-b02e-33d259394573`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IoHwAbInvalidValueSint8`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container for configuring an invalid value of a type "sint8".

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. IoHwAbInvalidValue

- **UUID**: `6993ab73-5d35-46ca-86b2-88b5812ca176`
- **参数名**: `IoHwAbInvalidValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [-128..127]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This field contains the initial value of a type "sint8".

######### 10. IoHwAbInvalidValueSint16

**容器属性**:

- **UUID**: `180d975a-2f07-4a24-981f-fd72bc383eb3`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IoHwAbInvalidValueSint16`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container for configuring an invalid value of a type "sint16".

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. IoHwAbInvalidValue

- **UUID**: `f05ebe07-97ab-41d8-831f-9c6c96be8449`
- **参数名**: `IoHwAbInvalidValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [-32768..32767]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This field contains the initial value of a type "sint16".

######### 11. IoHwAbInvalidValueSint32

**容器属性**:

- **UUID**: `e491e955-5ee9-4f76-8b97-ce3df8a76bb3`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IoHwAbInvalidValueSint32`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container for configuring an invalid value of a type "sint32".

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. IoHwAbInvalidValue

- **UUID**: `5216a15f-52b0-4be2-91b5-e2fc593c86d2`
- **参数名**: `IoHwAbInvalidValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [-2147483648..2147483647]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This field contains the initial value of a type "sint32".

######### 12. IoHwAbArray

**容器属性**:

- **UUID**: `1d9571d0-22d2-47a2-af79-82de8f7c0667`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IoHwAbArray`
- **多重性**: [0..infinite]
- **构建后可变**: false

**容器描述**:

Container for configuring an array type. An array type is the typedef of an array containing n data elements of a base type or a type reference, i.e. the generated files (e.g. Rte_Type.h) will contain a typedef like the following example:

typedef uint8 AlternatorPower_au8[13];

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. IoHwAbArraySize

- **UUID**: `a5f4d81e-a052-40be-9dd0-aacac5846259`
- **参数名**: `IoHwAbArraySize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `5`
- **取值范围**: [0..18446744073709551615]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Parameter for the configuration of the array size, i.e. the number of elements of the selected datatype.

########## 引用关系

此容器包含 **1** 个引用：

########### CHOICE-REFERENCE 类型引用

############ 1. IoHwAbArrayTypeRef

- **UUID**: `483e268d-4de7-4ebe-a5e3-1e4c9bb0abdc`
- **引用名**: `IoHwAbArrayTypeRef`
- **引用类型**: CHOICE-REFERENCE
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **需要索引**: false
- **目标引用列表**:
  - `/MICROSAR/IoHwAb/IoHwAbDatatypes/IoHwAbBaseType`
  - `/MICROSAR/IoHwAb/IoHwAbDatatypes/IoHwAbImplementationTypes/IoHwAbTypeReference`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Parameter for the selection of the datatype of the array elements.

######### 13. IoHwAbRecord

**容器属性**:

- **UUID**: `2dc30056-499e-44bf-92b4-13e8b9147b2d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IoHwAbRecord`
- **多重性**: [0..infinite]
- **构建后可变**: false

**容器描述**:

Container for configuring a record/struct type. An record type is the typedef of a struct containing data elements of a base type or a type reference, i.e. the generated files (e.g. Rte_Type.h) will contain a typedef like the following example:

typedef struct
{
    uint16 Period;
    uint16 ActiveTime;
}DutyCycle;

########## 配置容器

本模块包含 **1** 个配置容器：

########### 1. IoHwAbRecordElement

**容器属性**:

- **UUID**: `fb24fab4-1b14-4d65-ba77-b58f2f2acabb`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IoHwAbRecordElement`
- **多重性**: [1..infinite]
- **构建后可变**: false

**容器描述**:

Container for configuring a record/struct element.

############ 参数配置

此容器包含 **1** 个参数：

############# INTEGER 类型参数

############## 1. IoHwAbRecordElementPosition

- **UUID**: `274130e5-6acd-425a-95be-33c8df98940c`
- **参数名**: `IoHwAbRecordElementPosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..255]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter contains the position of the of the record element inside the record.

############ 引用关系

此容器包含 **1** 个引用：

############# CHOICE-REFERENCE 类型引用

############## 1. IoHwAbRecordElementTypeRef

- **UUID**: `b21ae229-f1b5-431e-a04f-9a9233f48f86`
- **引用名**: `IoHwAbRecordElementTypeRef`
- **引用类型**: CHOICE-REFERENCE
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **需要索引**: false
- **目标引用列表**:
  - `/MICROSAR/IoHwAb/IoHwAbDatatypes/IoHwAbBaseType`
  - `/MICROSAR/IoHwAb/IoHwAbDatatypes/IoHwAbImplementationTypes/IoHwAbTypeReference`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Parameter for the selection of the datatype of the struct/record elements.

######### 14. IoHwAbRecordElement

**容器属性**:

- **UUID**: `fb24fab4-1b14-4d65-ba77-b58f2f2acabb`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IoHwAbRecordElement`
- **多重性**: [1..infinite]
- **构建后可变**: false

**容器描述**:

Container for configuring a record/struct element.

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. IoHwAbRecordElementPosition

- **UUID**: `274130e5-6acd-425a-95be-33c8df98940c`
- **参数名**: `IoHwAbRecordElementPosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..255]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter contains the position of the of the record element inside the record.

########## 引用关系

此容器包含 **1** 个引用：

########### CHOICE-REFERENCE 类型引用

############ 1. IoHwAbRecordElementTypeRef

- **UUID**: `b21ae229-f1b5-431e-a04f-9a9233f48f86`
- **引用名**: `IoHwAbRecordElementTypeRef`
- **引用类型**: CHOICE-REFERENCE
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **需要索引**: false
- **目标引用列表**:
  - `/MICROSAR/IoHwAb/IoHwAbDatatypes/IoHwAbBaseType`
  - `/MICROSAR/IoHwAb/IoHwAbDatatypes/IoHwAbImplementationTypes/IoHwAbTypeReference`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Parameter for the selection of the datatype of the struct/record elements.

######### 15. IoHwAbInvalidValueType

**容器属性**:

- **UUID**: `289ed971-2914-4549-8220-d6145f506b72`
- **容器类型**: CHOICE-CONTAINER
- **容器名称**: `IoHwAbInvalidValueType`
- **多重性**: [1..1]
- **构建后可变**: false

**容器选择**:

- **IoHwAbInvalidValueBoolean**
  - UUID: `fbc4e248-f3c8-4bc8-bbd2-bfb6677b5882`
  - 描述: Container for configuring an invalid value of a type "boolean".
- **IoHwAbInvalidValueFloat32**
  - UUID: `2f2e9da1-4c91-46a2-a9d5-d4efeae48c26`
  - 描述: Container for configuring an invalid value of a type "float32".
- **IoHwAbInvalidValueFloat64**
  - UUID: `e9b907e5-22e6-4ce2-9f2a-6adebe0d3ce5`
  - 描述: Container for configuring an invalid value of a type "float64".
- **IoHwAbInvalidValueUint8**
  - UUID: `f465b96c-d804-4e17-a5ff-ad10d1057eee`
  - 描述: Container for configuring an invalid value of a type "uint8".
- **IoHwAbInvalidValueUint16**
  - UUID: `1f4065c4-b767-4ba2-afe4-c34ac1d97539`
  - 描述: Container for configuring an invalid value of a type "uint16".
- **IoHwAbInvalidValueUint32**
  - UUID: `2cfbeb44-2968-420f-915f-e456f924f21f`
  - 描述: Container for configuring an invalid value of a type "uint32".
- **IoHwAbInvalidValueSint8**
  - UUID: `7f46cafe-67b7-498a-b02e-33d259394573`
  - 描述: Container for configuring an invalid value of a type "sint8".
- **IoHwAbInvalidValueSint16**
  - UUID: `180d975a-2f07-4a24-981f-fd72bc383eb3`
  - 描述: Container for configuring an invalid value of a type "sint16".
- **IoHwAbInvalidValueSint32**
  - UUID: `e491e955-5ee9-4f76-8b97-ce3df8a76bb3`
  - 描述: Container for configuring an invalid value of a type "sint32".

**容器描述**:

This choice container is used for instantiating the appropriate type for the invalid value of the referenced data element.

Example: If the type of the referenced base data type is either an "uint8" or a type reference of an "uint8", the container "IoHwAbInvalidValueUint8" shall be chosen.

####### 2. IoHwAbTypeReference

**容器属性**:

- **UUID**: `4c4ad53e-8366-4d22-99a4-1ab863f99edf`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IoHwAbTypeReference`
- **多重性**: [0..infinite]
- **构建后可变**: false

**容器描述**:

Container for configuring a type reference. A type reference is a deviation from a base type, i.e. the generated files (e.g. Rte_Type.h) will contain a typedef like the following example:

typedef sint8 BatteryVoltageValue;

######## 引用关系

此容器包含 **1** 个引用：

######### CHOICE-REFERENCE 类型引用

########## 1. IoHwAbTypeReferenceTypeRef

- **UUID**: `be6126a0-a374-41f1-9a7a-9cf53955a504`
- **引用名**: `IoHwAbTypeReferenceTypeRef`
- **引用类型**: CHOICE-REFERENCE
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **需要索引**: false
- **目标引用列表**:
  - `/MICROSAR/IoHwAb/IoHwAbDatatypes/IoHwAbBaseType`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Parameter for the selection of the datatype of the type reference.

######## 配置容器

本模块包含 **11** 个配置容器：

######### 1. IoHwAbInvalidValue

**容器属性**:

- **UUID**: `5ca5978e-f620-4c40-ace2-df3e7b3618de`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IoHwAbInvalidValue`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Optional container for configuring an invalid value for a IoHwAb type reference.

########## 配置容器

本模块包含 **10** 个配置容器：

########### 1. IoHwAbInvalidValueBoolean

**容器属性**:

- **UUID**: `fbc4e248-f3c8-4bc8-bbd2-bfb6677b5882`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IoHwAbInvalidValueBoolean`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container for configuring an invalid value of a type "boolean".

############ 参数配置

此容器包含 **1** 个参数：

############# BOOLEAN 类型参数

############## 1. IoHwAbInvalidValue

- **UUID**: `359e7e9b-bd3d-4c1d-b8df-a0b34939f158`
- **参数名**: `IoHwAbInvalidValue`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This field contains the initial value of a type "boolean".

########### 2. IoHwAbInvalidValueFloat32

**容器属性**:

- **UUID**: `2f2e9da1-4c91-46a2-a9d5-d4efeae48c26`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IoHwAbInvalidValueFloat32`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container for configuring an invalid value of a type "float32".

############ 参数配置

此容器包含 **1** 个参数：

############# FLOAT 类型参数

############## 1. IoHwAbInvalidValue

- **UUID**: `d1e30bf3-35b3-41d7-bdda-eb28b3ec0419`
- **参数名**: `IoHwAbInvalidValue`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This field contains the initial value of a type "float32".

########### 3. IoHwAbInvalidValueFloat64

**容器属性**:

- **UUID**: `e9b907e5-22e6-4ce2-9f2a-6adebe0d3ce5`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IoHwAbInvalidValueFloat64`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container for configuring an invalid value of a type "float64".

############ 参数配置

此容器包含 **1** 个参数：

############# FLOAT 类型参数

############## 1. IoHwAbInvalidValue

- **UUID**: `f815ed02-2ff3-4495-aabf-26014c7ad01f`
- **参数名**: `IoHwAbInvalidValue`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This field contains the initial value of a type "float64".

########### 4. IoHwAbInvalidValueUint8

**容器属性**:

- **UUID**: `f465b96c-d804-4e17-a5ff-ad10d1057eee`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IoHwAbInvalidValueUint8`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container for configuring an invalid value of a type "uint8".

############ 参数配置

此容器包含 **1** 个参数：

############# INTEGER 类型参数

############## 1. IoHwAbInvalidValue

- **UUID**: `f1411f40-dceb-4ec6-97c7-4776f921515a`
- **参数名**: `IoHwAbInvalidValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This field contains the initial value of a type "uint8".

########### 5. IoHwAbInvalidValueUint16

**容器属性**:

- **UUID**: `1f4065c4-b767-4ba2-afe4-c34ac1d97539`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IoHwAbInvalidValueUint16`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container for configuring an invalid value of a type "uint16".

############ 参数配置

此容器包含 **1** 个参数：

############# INTEGER 类型参数

############## 1. IoHwAbInvalidValue

- **UUID**: `76ea2c11-a275-4ff5-9ed1-e2f81e3739b8`
- **参数名**: `IoHwAbInvalidValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This field contains the initial value of a type "uint16".

########### 6. IoHwAbInvalidValueUint32

**容器属性**:

- **UUID**: `2cfbeb44-2968-420f-915f-e456f924f21f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IoHwAbInvalidValueUint32`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container for configuring an invalid value of a type "uint32".

############ 参数配置

此容器包含 **1** 个参数：

############# INTEGER 类型参数

############## 1. IoHwAbInvalidValue

- **UUID**: `41a8d144-1c90-4172-8612-17fd061a8e44`
- **参数名**: `IoHwAbInvalidValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This field contains the initial value of a type "uint32".

########### 7. IoHwAbInvalidValueSint8

**容器属性**:

- **UUID**: `7f46cafe-67b7-498a-b02e-33d259394573`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IoHwAbInvalidValueSint8`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container for configuring an invalid value of a type "sint8".

############ 参数配置

此容器包含 **1** 个参数：

############# INTEGER 类型参数

############## 1. IoHwAbInvalidValue

- **UUID**: `6993ab73-5d35-46ca-86b2-88b5812ca176`
- **参数名**: `IoHwAbInvalidValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [-128..127]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This field contains the initial value of a type "sint8".

########### 8. IoHwAbInvalidValueSint16

**容器属性**:

- **UUID**: `180d975a-2f07-4a24-981f-fd72bc383eb3`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IoHwAbInvalidValueSint16`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container for configuring an invalid value of a type "sint16".

############ 参数配置

此容器包含 **1** 个参数：

############# INTEGER 类型参数

############## 1. IoHwAbInvalidValue

- **UUID**: `f05ebe07-97ab-41d8-831f-9c6c96be8449`
- **参数名**: `IoHwAbInvalidValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [-32768..32767]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This field contains the initial value of a type "sint16".

########### 9. IoHwAbInvalidValueSint32

**容器属性**:

- **UUID**: `e491e955-5ee9-4f76-8b97-ce3df8a76bb3`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IoHwAbInvalidValueSint32`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container for configuring an invalid value of a type "sint32".

############ 参数配置

此容器包含 **1** 个参数：

############# INTEGER 类型参数

############## 1. IoHwAbInvalidValue

- **UUID**: `5216a15f-52b0-4be2-91b5-e2fc593c86d2`
- **参数名**: `IoHwAbInvalidValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [-2147483648..2147483647]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This field contains the initial value of a type "sint32".

########### 10. IoHwAbInvalidValueType

**容器属性**:

- **UUID**: `289ed971-2914-4549-8220-d6145f506b72`
- **容器类型**: CHOICE-CONTAINER
- **容器名称**: `IoHwAbInvalidValueType`
- **多重性**: [1..1]
- **构建后可变**: false

**容器选择**:

- **IoHwAbInvalidValueBoolean**
  - UUID: `fbc4e248-f3c8-4bc8-bbd2-bfb6677b5882`
  - 描述: Container for configuring an invalid value of a type "boolean".
- **IoHwAbInvalidValueFloat32**
  - UUID: `2f2e9da1-4c91-46a2-a9d5-d4efeae48c26`
  - 描述: Container for configuring an invalid value of a type "float32".
- **IoHwAbInvalidValueFloat64**
  - UUID: `e9b907e5-22e6-4ce2-9f2a-6adebe0d3ce5`
  - 描述: Container for configuring an invalid value of a type "float64".
- **IoHwAbInvalidValueUint8**
  - UUID: `f465b96c-d804-4e17-a5ff-ad10d1057eee`
  - 描述: Container for configuring an invalid value of a type "uint8".
- **IoHwAbInvalidValueUint16**
  - UUID: `1f4065c4-b767-4ba2-afe4-c34ac1d97539`
  - 描述: Container for configuring an invalid value of a type "uint16".
- **IoHwAbInvalidValueUint32**
  - UUID: `2cfbeb44-2968-420f-915f-e456f924f21f`
  - 描述: Container for configuring an invalid value of a type "uint32".
- **IoHwAbInvalidValueSint8**
  - UUID: `7f46cafe-67b7-498a-b02e-33d259394573`
  - 描述: Container for configuring an invalid value of a type "sint8".
- **IoHwAbInvalidValueSint16**
  - UUID: `180d975a-2f07-4a24-981f-fd72bc383eb3`
  - 描述: Container for configuring an invalid value of a type "sint16".
- **IoHwAbInvalidValueSint32**
  - UUID: `e491e955-5ee9-4f76-8b97-ce3df8a76bb3`
  - 描述: Container for configuring an invalid value of a type "sint32".

**容器描述**:

This choice container is used for instantiating the appropriate type for the invalid value of the referenced data element.

Example: If the type of the referenced base data type is either an "uint8" or a type reference of an "uint8", the container "IoHwAbInvalidValueUint8" shall be chosen.

######### 2. IoHwAbInvalidValueBoolean

**容器属性**:

- **UUID**: `fbc4e248-f3c8-4bc8-bbd2-bfb6677b5882`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IoHwAbInvalidValueBoolean`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container for configuring an invalid value of a type "boolean".

########## 参数配置

此容器包含 **1** 个参数：

########### BOOLEAN 类型参数

############ 1. IoHwAbInvalidValue

- **UUID**: `359e7e9b-bd3d-4c1d-b8df-a0b34939f158`
- **参数名**: `IoHwAbInvalidValue`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This field contains the initial value of a type "boolean".

######### 3. IoHwAbInvalidValueFloat32

**容器属性**:

- **UUID**: `2f2e9da1-4c91-46a2-a9d5-d4efeae48c26`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IoHwAbInvalidValueFloat32`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container for configuring an invalid value of a type "float32".

########## 参数配置

此容器包含 **1** 个参数：

########### FLOAT 类型参数

############ 1. IoHwAbInvalidValue

- **UUID**: `d1e30bf3-35b3-41d7-bdda-eb28b3ec0419`
- **参数名**: `IoHwAbInvalidValue`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This field contains the initial value of a type "float32".

######### 4. IoHwAbInvalidValueFloat64

**容器属性**:

- **UUID**: `e9b907e5-22e6-4ce2-9f2a-6adebe0d3ce5`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IoHwAbInvalidValueFloat64`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container for configuring an invalid value of a type "float64".

########## 参数配置

此容器包含 **1** 个参数：

########### FLOAT 类型参数

############ 1. IoHwAbInvalidValue

- **UUID**: `f815ed02-2ff3-4495-aabf-26014c7ad01f`
- **参数名**: `IoHwAbInvalidValue`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This field contains the initial value of a type "float64".

######### 5. IoHwAbInvalidValueUint8

**容器属性**:

- **UUID**: `f465b96c-d804-4e17-a5ff-ad10d1057eee`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IoHwAbInvalidValueUint8`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container for configuring an invalid value of a type "uint8".

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. IoHwAbInvalidValue

- **UUID**: `f1411f40-dceb-4ec6-97c7-4776f921515a`
- **参数名**: `IoHwAbInvalidValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This field contains the initial value of a type "uint8".

######### 6. IoHwAbInvalidValueUint16

**容器属性**:

- **UUID**: `1f4065c4-b767-4ba2-afe4-c34ac1d97539`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IoHwAbInvalidValueUint16`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container for configuring an invalid value of a type "uint16".

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. IoHwAbInvalidValue

- **UUID**: `76ea2c11-a275-4ff5-9ed1-e2f81e3739b8`
- **参数名**: `IoHwAbInvalidValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This field contains the initial value of a type "uint16".

######### 7. IoHwAbInvalidValueUint32

**容器属性**:

- **UUID**: `2cfbeb44-2968-420f-915f-e456f924f21f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IoHwAbInvalidValueUint32`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container for configuring an invalid value of a type "uint32".

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. IoHwAbInvalidValue

- **UUID**: `41a8d144-1c90-4172-8612-17fd061a8e44`
- **参数名**: `IoHwAbInvalidValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This field contains the initial value of a type "uint32".

######### 8. IoHwAbInvalidValueSint8

**容器属性**:

- **UUID**: `7f46cafe-67b7-498a-b02e-33d259394573`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IoHwAbInvalidValueSint8`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container for configuring an invalid value of a type "sint8".

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. IoHwAbInvalidValue

- **UUID**: `6993ab73-5d35-46ca-86b2-88b5812ca176`
- **参数名**: `IoHwAbInvalidValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [-128..127]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This field contains the initial value of a type "sint8".

######### 9. IoHwAbInvalidValueSint16

**容器属性**:

- **UUID**: `180d975a-2f07-4a24-981f-fd72bc383eb3`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IoHwAbInvalidValueSint16`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container for configuring an invalid value of a type "sint16".

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. IoHwAbInvalidValue

- **UUID**: `f05ebe07-97ab-41d8-831f-9c6c96be8449`
- **参数名**: `IoHwAbInvalidValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [-32768..32767]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This field contains the initial value of a type "sint16".

######### 10. IoHwAbInvalidValueSint32

**容器属性**:

- **UUID**: `e491e955-5ee9-4f76-8b97-ce3df8a76bb3`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IoHwAbInvalidValueSint32`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container for configuring an invalid value of a type "sint32".

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. IoHwAbInvalidValue

- **UUID**: `5216a15f-52b0-4be2-91b5-e2fc593c86d2`
- **参数名**: `IoHwAbInvalidValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [-2147483648..2147483647]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This field contains the initial value of a type "sint32".

######### 11. IoHwAbInvalidValueType

**容器属性**:

- **UUID**: `289ed971-2914-4549-8220-d6145f506b72`
- **容器类型**: CHOICE-CONTAINER
- **容器名称**: `IoHwAbInvalidValueType`
- **多重性**: [1..1]
- **构建后可变**: false

**容器选择**:

- **IoHwAbInvalidValueBoolean**
  - UUID: `fbc4e248-f3c8-4bc8-bbd2-bfb6677b5882`
  - 描述: Container for configuring an invalid value of a type "boolean".
- **IoHwAbInvalidValueFloat32**
  - UUID: `2f2e9da1-4c91-46a2-a9d5-d4efeae48c26`
  - 描述: Container for configuring an invalid value of a type "float32".
- **IoHwAbInvalidValueFloat64**
  - UUID: `e9b907e5-22e6-4ce2-9f2a-6adebe0d3ce5`
  - 描述: Container for configuring an invalid value of a type "float64".
- **IoHwAbInvalidValueUint8**
  - UUID: `f465b96c-d804-4e17-a5ff-ad10d1057eee`
  - 描述: Container for configuring an invalid value of a type "uint8".
- **IoHwAbInvalidValueUint16**
  - UUID: `1f4065c4-b767-4ba2-afe4-c34ac1d97539`
  - 描述: Container for configuring an invalid value of a type "uint16".
- **IoHwAbInvalidValueUint32**
  - UUID: `2cfbeb44-2968-420f-915f-e456f924f21f`
  - 描述: Container for configuring an invalid value of a type "uint32".
- **IoHwAbInvalidValueSint8**
  - UUID: `7f46cafe-67b7-498a-b02e-33d259394573`
  - 描述: Container for configuring an invalid value of a type "sint8".
- **IoHwAbInvalidValueSint16**
  - UUID: `180d975a-2f07-4a24-981f-fd72bc383eb3`
  - 描述: Container for configuring an invalid value of a type "sint16".
- **IoHwAbInvalidValueSint32**
  - UUID: `e491e955-5ee9-4f76-8b97-ce3df8a76bb3`
  - 描述: Container for configuring an invalid value of a type "sint32".

**容器描述**:

This choice container is used for instantiating the appropriate type for the invalid value of the referenced data element.

Example: If the type of the referenced base data type is either an "uint8" or a type reference of an "uint8", the container "IoHwAbInvalidValueUint8" shall be chosen.

####### 3. IoHwAbInvalidValue

**容器属性**:

- **UUID**: `5ca5978e-f620-4c40-ace2-df3e7b3618de`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IoHwAbInvalidValue`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Optional container for configuring an invalid value for a IoHwAb type reference.

######## 配置容器

本模块包含 **10** 个配置容器：

######### 1. IoHwAbInvalidValueBoolean

**容器属性**:

- **UUID**: `fbc4e248-f3c8-4bc8-bbd2-bfb6677b5882`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IoHwAbInvalidValueBoolean`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container for configuring an invalid value of a type "boolean".

########## 参数配置

此容器包含 **1** 个参数：

########### BOOLEAN 类型参数

############ 1. IoHwAbInvalidValue

- **UUID**: `359e7e9b-bd3d-4c1d-b8df-a0b34939f158`
- **参数名**: `IoHwAbInvalidValue`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This field contains the initial value of a type "boolean".

######### 2. IoHwAbInvalidValueFloat32

**容器属性**:

- **UUID**: `2f2e9da1-4c91-46a2-a9d5-d4efeae48c26`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IoHwAbInvalidValueFloat32`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container for configuring an invalid value of a type "float32".

########## 参数配置

此容器包含 **1** 个参数：

########### FLOAT 类型参数

############ 1. IoHwAbInvalidValue

- **UUID**: `d1e30bf3-35b3-41d7-bdda-eb28b3ec0419`
- **参数名**: `IoHwAbInvalidValue`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This field contains the initial value of a type "float32".

######### 3. IoHwAbInvalidValueFloat64

**容器属性**:

- **UUID**: `e9b907e5-22e6-4ce2-9f2a-6adebe0d3ce5`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IoHwAbInvalidValueFloat64`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container for configuring an invalid value of a type "float64".

########## 参数配置

此容器包含 **1** 个参数：

########### FLOAT 类型参数

############ 1. IoHwAbInvalidValue

- **UUID**: `f815ed02-2ff3-4495-aabf-26014c7ad01f`
- **参数名**: `IoHwAbInvalidValue`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This field contains the initial value of a type "float64".

######### 4. IoHwAbInvalidValueUint8

**容器属性**:

- **UUID**: `f465b96c-d804-4e17-a5ff-ad10d1057eee`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IoHwAbInvalidValueUint8`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container for configuring an invalid value of a type "uint8".

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. IoHwAbInvalidValue

- **UUID**: `f1411f40-dceb-4ec6-97c7-4776f921515a`
- **参数名**: `IoHwAbInvalidValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This field contains the initial value of a type "uint8".

######### 5. IoHwAbInvalidValueUint16

**容器属性**:

- **UUID**: `1f4065c4-b767-4ba2-afe4-c34ac1d97539`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IoHwAbInvalidValueUint16`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container for configuring an invalid value of a type "uint16".

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. IoHwAbInvalidValue

- **UUID**: `76ea2c11-a275-4ff5-9ed1-e2f81e3739b8`
- **参数名**: `IoHwAbInvalidValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This field contains the initial value of a type "uint16".

######### 6. IoHwAbInvalidValueUint32

**容器属性**:

- **UUID**: `2cfbeb44-2968-420f-915f-e456f924f21f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IoHwAbInvalidValueUint32`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container for configuring an invalid value of a type "uint32".

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. IoHwAbInvalidValue

- **UUID**: `41a8d144-1c90-4172-8612-17fd061a8e44`
- **参数名**: `IoHwAbInvalidValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This field contains the initial value of a type "uint32".

######### 7. IoHwAbInvalidValueSint8

**容器属性**:

- **UUID**: `7f46cafe-67b7-498a-b02e-33d259394573`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IoHwAbInvalidValueSint8`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container for configuring an invalid value of a type "sint8".

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. IoHwAbInvalidValue

- **UUID**: `6993ab73-5d35-46ca-86b2-88b5812ca176`
- **参数名**: `IoHwAbInvalidValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [-128..127]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This field contains the initial value of a type "sint8".

######### 8. IoHwAbInvalidValueSint16

**容器属性**:

- **UUID**: `180d975a-2f07-4a24-981f-fd72bc383eb3`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IoHwAbInvalidValueSint16`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container for configuring an invalid value of a type "sint16".

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. IoHwAbInvalidValue

- **UUID**: `f05ebe07-97ab-41d8-831f-9c6c96be8449`
- **参数名**: `IoHwAbInvalidValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [-32768..32767]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This field contains the initial value of a type "sint16".

######### 9. IoHwAbInvalidValueSint32

**容器属性**:

- **UUID**: `e491e955-5ee9-4f76-8b97-ce3df8a76bb3`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IoHwAbInvalidValueSint32`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container for configuring an invalid value of a type "sint32".

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. IoHwAbInvalidValue

- **UUID**: `5216a15f-52b0-4be2-91b5-e2fc593c86d2`
- **参数名**: `IoHwAbInvalidValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [-2147483648..2147483647]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This field contains the initial value of a type "sint32".

######### 10. IoHwAbInvalidValueType

**容器属性**:

- **UUID**: `289ed971-2914-4549-8220-d6145f506b72`
- **容器类型**: CHOICE-CONTAINER
- **容器名称**: `IoHwAbInvalidValueType`
- **多重性**: [1..1]
- **构建后可变**: false

**容器选择**:

- **IoHwAbInvalidValueBoolean**
  - UUID: `fbc4e248-f3c8-4bc8-bbd2-bfb6677b5882`
  - 描述: Container for configuring an invalid value of a type "boolean".
- **IoHwAbInvalidValueFloat32**
  - UUID: `2f2e9da1-4c91-46a2-a9d5-d4efeae48c26`
  - 描述: Container for configuring an invalid value of a type "float32".
- **IoHwAbInvalidValueFloat64**
  - UUID: `e9b907e5-22e6-4ce2-9f2a-6adebe0d3ce5`
  - 描述: Container for configuring an invalid value of a type "float64".
- **IoHwAbInvalidValueUint8**
  - UUID: `f465b96c-d804-4e17-a5ff-ad10d1057eee`
  - 描述: Container for configuring an invalid value of a type "uint8".
- **IoHwAbInvalidValueUint16**
  - UUID: `1f4065c4-b767-4ba2-afe4-c34ac1d97539`
  - 描述: Container for configuring an invalid value of a type "uint16".
- **IoHwAbInvalidValueUint32**
  - UUID: `2cfbeb44-2968-420f-915f-e456f924f21f`
  - 描述: Container for configuring an invalid value of a type "uint32".
- **IoHwAbInvalidValueSint8**
  - UUID: `7f46cafe-67b7-498a-b02e-33d259394573`
  - 描述: Container for configuring an invalid value of a type "sint8".
- **IoHwAbInvalidValueSint16**
  - UUID: `180d975a-2f07-4a24-981f-fd72bc383eb3`
  - 描述: Container for configuring an invalid value of a type "sint16".
- **IoHwAbInvalidValueSint32**
  - UUID: `e491e955-5ee9-4f76-8b97-ce3df8a76bb3`
  - 描述: Container for configuring an invalid value of a type "sint32".

**容器描述**:

This choice container is used for instantiating the appropriate type for the invalid value of the referenced data element.

Example: If the type of the referenced base data type is either an "uint8" or a type reference of an "uint8", the container "IoHwAbInvalidValueUint8" shall be chosen.

####### 4. IoHwAbInvalidValueBoolean

**容器属性**:

- **UUID**: `fbc4e248-f3c8-4bc8-bbd2-bfb6677b5882`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IoHwAbInvalidValueBoolean`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container for configuring an invalid value of a type "boolean".

######## 参数配置

此容器包含 **1** 个参数：

######### BOOLEAN 类型参数

########## 1. IoHwAbInvalidValue

- **UUID**: `359e7e9b-bd3d-4c1d-b8df-a0b34939f158`
- **参数名**: `IoHwAbInvalidValue`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This field contains the initial value of a type "boolean".

####### 5. IoHwAbInvalidValueFloat32

**容器属性**:

- **UUID**: `2f2e9da1-4c91-46a2-a9d5-d4efeae48c26`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IoHwAbInvalidValueFloat32`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container for configuring an invalid value of a type "float32".

######## 参数配置

此容器包含 **1** 个参数：

######### FLOAT 类型参数

########## 1. IoHwAbInvalidValue

- **UUID**: `d1e30bf3-35b3-41d7-bdda-eb28b3ec0419`
- **参数名**: `IoHwAbInvalidValue`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This field contains the initial value of a type "float32".

####### 6. IoHwAbInvalidValueFloat64

**容器属性**:

- **UUID**: `e9b907e5-22e6-4ce2-9f2a-6adebe0d3ce5`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IoHwAbInvalidValueFloat64`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container for configuring an invalid value of a type "float64".

######## 参数配置

此容器包含 **1** 个参数：

######### FLOAT 类型参数

########## 1. IoHwAbInvalidValue

- **UUID**: `f815ed02-2ff3-4495-aabf-26014c7ad01f`
- **参数名**: `IoHwAbInvalidValue`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This field contains the initial value of a type "float64".

####### 7. IoHwAbInvalidValueUint8

**容器属性**:

- **UUID**: `f465b96c-d804-4e17-a5ff-ad10d1057eee`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IoHwAbInvalidValueUint8`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container for configuring an invalid value of a type "uint8".

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. IoHwAbInvalidValue

- **UUID**: `f1411f40-dceb-4ec6-97c7-4776f921515a`
- **参数名**: `IoHwAbInvalidValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This field contains the initial value of a type "uint8".

####### 8. IoHwAbInvalidValueUint16

**容器属性**:

- **UUID**: `1f4065c4-b767-4ba2-afe4-c34ac1d97539`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IoHwAbInvalidValueUint16`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container for configuring an invalid value of a type "uint16".

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. IoHwAbInvalidValue

- **UUID**: `76ea2c11-a275-4ff5-9ed1-e2f81e3739b8`
- **参数名**: `IoHwAbInvalidValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This field contains the initial value of a type "uint16".

####### 9. IoHwAbInvalidValueUint32

**容器属性**:

- **UUID**: `2cfbeb44-2968-420f-915f-e456f924f21f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IoHwAbInvalidValueUint32`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container for configuring an invalid value of a type "uint32".

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. IoHwAbInvalidValue

- **UUID**: `41a8d144-1c90-4172-8612-17fd061a8e44`
- **参数名**: `IoHwAbInvalidValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This field contains the initial value of a type "uint32".

####### 10. IoHwAbInvalidValueSint8

**容器属性**:

- **UUID**: `7f46cafe-67b7-498a-b02e-33d259394573`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IoHwAbInvalidValueSint8`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container for configuring an invalid value of a type "sint8".

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. IoHwAbInvalidValue

- **UUID**: `6993ab73-5d35-46ca-86b2-88b5812ca176`
- **参数名**: `IoHwAbInvalidValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [-128..127]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This field contains the initial value of a type "sint8".

####### 11. IoHwAbInvalidValueSint16

**容器属性**:

- **UUID**: `180d975a-2f07-4a24-981f-fd72bc383eb3`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IoHwAbInvalidValueSint16`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container for configuring an invalid value of a type "sint16".

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. IoHwAbInvalidValue

- **UUID**: `f05ebe07-97ab-41d8-831f-9c6c96be8449`
- **参数名**: `IoHwAbInvalidValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [-32768..32767]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This field contains the initial value of a type "sint16".

####### 12. IoHwAbInvalidValueSint32

**容器属性**:

- **UUID**: `e491e955-5ee9-4f76-8b97-ce3df8a76bb3`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IoHwAbInvalidValueSint32`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container for configuring an invalid value of a type "sint32".

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. IoHwAbInvalidValue

- **UUID**: `5216a15f-52b0-4be2-91b5-e2fc593c86d2`
- **参数名**: `IoHwAbInvalidValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [-2147483648..2147483647]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This field contains the initial value of a type "sint32".

####### 13. IoHwAbArray

**容器属性**:

- **UUID**: `1d9571d0-22d2-47a2-af79-82de8f7c0667`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IoHwAbArray`
- **多重性**: [0..infinite]
- **构建后可变**: false

**容器描述**:

Container for configuring an array type. An array type is the typedef of an array containing n data elements of a base type or a type reference, i.e. the generated files (e.g. Rte_Type.h) will contain a typedef like the following example:

typedef uint8 AlternatorPower_au8[13];

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. IoHwAbArraySize

- **UUID**: `a5f4d81e-a052-40be-9dd0-aacac5846259`
- **参数名**: `IoHwAbArraySize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `5`
- **取值范围**: [0..18446744073709551615]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Parameter for the configuration of the array size, i.e. the number of elements of the selected datatype.

######## 引用关系

此容器包含 **1** 个引用：

######### CHOICE-REFERENCE 类型引用

########## 1. IoHwAbArrayTypeRef

- **UUID**: `483e268d-4de7-4ebe-a5e3-1e4c9bb0abdc`
- **引用名**: `IoHwAbArrayTypeRef`
- **引用类型**: CHOICE-REFERENCE
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **需要索引**: false
- **目标引用列表**:
  - `/MICROSAR/IoHwAb/IoHwAbDatatypes/IoHwAbBaseType`
  - `/MICROSAR/IoHwAb/IoHwAbDatatypes/IoHwAbImplementationTypes/IoHwAbTypeReference`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Parameter for the selection of the datatype of the array elements.

####### 14. IoHwAbRecord

**容器属性**:

- **UUID**: `2dc30056-499e-44bf-92b4-13e8b9147b2d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IoHwAbRecord`
- **多重性**: [0..infinite]
- **构建后可变**: false

**容器描述**:

Container for configuring a record/struct type. An record type is the typedef of a struct containing data elements of a base type or a type reference, i.e. the generated files (e.g. Rte_Type.h) will contain a typedef like the following example:

typedef struct
{
    uint16 Period;
    uint16 ActiveTime;
}DutyCycle;

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. IoHwAbRecordElement

**容器属性**:

- **UUID**: `fb24fab4-1b14-4d65-ba77-b58f2f2acabb`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IoHwAbRecordElement`
- **多重性**: [1..infinite]
- **构建后可变**: false

**容器描述**:

Container for configuring a record/struct element.

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. IoHwAbRecordElementPosition

- **UUID**: `274130e5-6acd-425a-95be-33c8df98940c`
- **参数名**: `IoHwAbRecordElementPosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..255]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter contains the position of the of the record element inside the record.

########## 引用关系

此容器包含 **1** 个引用：

########### CHOICE-REFERENCE 类型引用

############ 1. IoHwAbRecordElementTypeRef

- **UUID**: `b21ae229-f1b5-431e-a04f-9a9233f48f86`
- **引用名**: `IoHwAbRecordElementTypeRef`
- **引用类型**: CHOICE-REFERENCE
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **需要索引**: false
- **目标引用列表**:
  - `/MICROSAR/IoHwAb/IoHwAbDatatypes/IoHwAbBaseType`
  - `/MICROSAR/IoHwAb/IoHwAbDatatypes/IoHwAbImplementationTypes/IoHwAbTypeReference`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Parameter for the selection of the datatype of the struct/record elements.

####### 15. IoHwAbRecordElement

**容器属性**:

- **UUID**: `fb24fab4-1b14-4d65-ba77-b58f2f2acabb`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IoHwAbRecordElement`
- **多重性**: [1..infinite]
- **构建后可变**: false

**容器描述**:

Container for configuring a record/struct element.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. IoHwAbRecordElementPosition

- **UUID**: `274130e5-6acd-425a-95be-33c8df98940c`
- **参数名**: `IoHwAbRecordElementPosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..255]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter contains the position of the of the record element inside the record.

######## 引用关系

此容器包含 **1** 个引用：

######### CHOICE-REFERENCE 类型引用

########## 1. IoHwAbRecordElementTypeRef

- **UUID**: `b21ae229-f1b5-431e-a04f-9a9233f48f86`
- **引用名**: `IoHwAbRecordElementTypeRef`
- **引用类型**: CHOICE-REFERENCE
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **需要索引**: false
- **目标引用列表**:
  - `/MICROSAR/IoHwAb/IoHwAbDatatypes/IoHwAbBaseType`
  - `/MICROSAR/IoHwAb/IoHwAbDatatypes/IoHwAbImplementationTypes/IoHwAbTypeReference`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Parameter for the selection of the datatype of the struct/record elements.

####### 16. IoHwAbBaseType

**容器属性**:

- **UUID**: `6e24768e-f576-48b4-91b8-ea629cba7612`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IoHwAbBaseType`
- **多重性**: [9..9]
- **构建后可变**: false

**容器描述**:

Container for the base data types. These types are a representation of the standard types and cannot be changed.

######## 参数配置

此容器包含 **1** 个参数：

######### ENUMERATION 类型参数

########## 1. IoHwAbBaseDataType

- **UUID**: `eab27640-2d90-45a6-9566-42f3c53956b5`
- **参数名**: `IoHwAbBaseDataType`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `IOHWAB_UINT8`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `IOHWAB_UINT8` (来源: Vector Informatik)
  - `IOHWAB_UINT16` (来源: Vector Informatik)
  - `IOHWAB_UINT32` (来源: Vector Informatik)
  - `IOHWAB_SINT8` (来源: Vector Informatik)
  - `IOHWAB_SINT16` (来源: Vector Informatik)
  - `IOHWAB_SINT32` (来源: Vector Informatik)
  - `IOHWAB_BOOL` (来源: Vector Informatik)
  - `IOHWAB_FLOAT32` (来源: Vector Informatik)
  - `IOHWAB_FLOAT64` (来源: Vector Informatik)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Label for the referenced base type. This type should be used within the user blocks instead of the base type itself.

####### 17. IoHwAbInvalidValueType

**容器属性**:

- **UUID**: `289ed971-2914-4549-8220-d6145f506b72`
- **容器类型**: CHOICE-CONTAINER
- **容器名称**: `IoHwAbInvalidValueType`
- **多重性**: [1..1]
- **构建后可变**: false

**容器选择**:

- **IoHwAbInvalidValueBoolean**
  - UUID: `fbc4e248-f3c8-4bc8-bbd2-bfb6677b5882`
  - 描述: Container for configuring an invalid value of a type "boolean".
- **IoHwAbInvalidValueFloat32**
  - UUID: `2f2e9da1-4c91-46a2-a9d5-d4efeae48c26`
  - 描述: Container for configuring an invalid value of a type "float32".
- **IoHwAbInvalidValueFloat64**
  - UUID: `e9b907e5-22e6-4ce2-9f2a-6adebe0d3ce5`
  - 描述: Container for configuring an invalid value of a type "float64".
- **IoHwAbInvalidValueUint8**
  - UUID: `f465b96c-d804-4e17-a5ff-ad10d1057eee`
  - 描述: Container for configuring an invalid value of a type "uint8".
- **IoHwAbInvalidValueUint16**
  - UUID: `1f4065c4-b767-4ba2-afe4-c34ac1d97539`
  - 描述: Container for configuring an invalid value of a type "uint16".
- **IoHwAbInvalidValueUint32**
  - UUID: `2cfbeb44-2968-420f-915f-e456f924f21f`
  - 描述: Container for configuring an invalid value of a type "uint32".
- **IoHwAbInvalidValueSint8**
  - UUID: `7f46cafe-67b7-498a-b02e-33d259394573`
  - 描述: Container for configuring an invalid value of a type "sint8".
- **IoHwAbInvalidValueSint16**
  - UUID: `180d975a-2f07-4a24-981f-fd72bc383eb3`
  - 描述: Container for configuring an invalid value of a type "sint16".
- **IoHwAbInvalidValueSint32**
  - UUID: `e491e955-5ee9-4f76-8b97-ce3df8a76bb3`
  - 描述: Container for configuring an invalid value of a type "sint32".

**容器描述**:

This choice container is used for instantiating the appropriate type for the invalid value of the referenced data element.

Example: If the type of the referenced base data type is either an "uint8" or a type reference of an "uint8", the container "IoHwAbInvalidValueUint8" shall be chosen.

##### 3. IoHwAbImplementationTypes

**容器属性**:

- **UUID**: `c6d9e636-ceb5-41f8-9c06-5828cc7cf45e`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IoHwAbImplementationTypes`
- **多重性**: [1..1]
- **构建后可变**: false

**容器描述**:

Container for the implementation specific datatypes. Implementation specific datatypes can be configured/assembled by using base datatypes.

###### 配置容器

本模块包含 **15** 个配置容器：

####### 1. IoHwAbTypeReference

**容器属性**:

- **UUID**: `4c4ad53e-8366-4d22-99a4-1ab863f99edf`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IoHwAbTypeReference`
- **多重性**: [0..infinite]
- **构建后可变**: false

**容器描述**:

Container for configuring a type reference. A type reference is a deviation from a base type, i.e. the generated files (e.g. Rte_Type.h) will contain a typedef like the following example:

typedef sint8 BatteryVoltageValue;

######## 引用关系

此容器包含 **1** 个引用：

######### CHOICE-REFERENCE 类型引用

########## 1. IoHwAbTypeReferenceTypeRef

- **UUID**: `be6126a0-a374-41f1-9a7a-9cf53955a504`
- **引用名**: `IoHwAbTypeReferenceTypeRef`
- **引用类型**: CHOICE-REFERENCE
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **需要索引**: false
- **目标引用列表**:
  - `/MICROSAR/IoHwAb/IoHwAbDatatypes/IoHwAbBaseType`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Parameter for the selection of the datatype of the type reference.

######## 配置容器

本模块包含 **11** 个配置容器：

######### 1. IoHwAbInvalidValue

**容器属性**:

- **UUID**: `5ca5978e-f620-4c40-ace2-df3e7b3618de`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IoHwAbInvalidValue`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Optional container for configuring an invalid value for a IoHwAb type reference.

########## 配置容器

本模块包含 **10** 个配置容器：

########### 1. IoHwAbInvalidValueBoolean

**容器属性**:

- **UUID**: `fbc4e248-f3c8-4bc8-bbd2-bfb6677b5882`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IoHwAbInvalidValueBoolean`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container for configuring an invalid value of a type "boolean".

############ 参数配置

此容器包含 **1** 个参数：

############# BOOLEAN 类型参数

############## 1. IoHwAbInvalidValue

- **UUID**: `359e7e9b-bd3d-4c1d-b8df-a0b34939f158`
- **参数名**: `IoHwAbInvalidValue`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This field contains the initial value of a type "boolean".

########### 2. IoHwAbInvalidValueFloat32

**容器属性**:

- **UUID**: `2f2e9da1-4c91-46a2-a9d5-d4efeae48c26`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IoHwAbInvalidValueFloat32`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container for configuring an invalid value of a type "float32".

############ 参数配置

此容器包含 **1** 个参数：

############# FLOAT 类型参数

############## 1. IoHwAbInvalidValue

- **UUID**: `d1e30bf3-35b3-41d7-bdda-eb28b3ec0419`
- **参数名**: `IoHwAbInvalidValue`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This field contains the initial value of a type "float32".

########### 3. IoHwAbInvalidValueFloat64

**容器属性**:

- **UUID**: `e9b907e5-22e6-4ce2-9f2a-6adebe0d3ce5`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IoHwAbInvalidValueFloat64`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container for configuring an invalid value of a type "float64".

############ 参数配置

此容器包含 **1** 个参数：

############# FLOAT 类型参数

############## 1. IoHwAbInvalidValue

- **UUID**: `f815ed02-2ff3-4495-aabf-26014c7ad01f`
- **参数名**: `IoHwAbInvalidValue`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This field contains the initial value of a type "float64".

########### 4. IoHwAbInvalidValueUint8

**容器属性**:

- **UUID**: `f465b96c-d804-4e17-a5ff-ad10d1057eee`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IoHwAbInvalidValueUint8`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container for configuring an invalid value of a type "uint8".

############ 参数配置

此容器包含 **1** 个参数：

############# INTEGER 类型参数

############## 1. IoHwAbInvalidValue

- **UUID**: `f1411f40-dceb-4ec6-97c7-4776f921515a`
- **参数名**: `IoHwAbInvalidValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This field contains the initial value of a type "uint8".

########### 5. IoHwAbInvalidValueUint16

**容器属性**:

- **UUID**: `1f4065c4-b767-4ba2-afe4-c34ac1d97539`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IoHwAbInvalidValueUint16`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container for configuring an invalid value of a type "uint16".

############ 参数配置

此容器包含 **1** 个参数：

############# INTEGER 类型参数

############## 1. IoHwAbInvalidValue

- **UUID**: `76ea2c11-a275-4ff5-9ed1-e2f81e3739b8`
- **参数名**: `IoHwAbInvalidValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This field contains the initial value of a type "uint16".

########### 6. IoHwAbInvalidValueUint32

**容器属性**:

- **UUID**: `2cfbeb44-2968-420f-915f-e456f924f21f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IoHwAbInvalidValueUint32`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container for configuring an invalid value of a type "uint32".

############ 参数配置

此容器包含 **1** 个参数：

############# INTEGER 类型参数

############## 1. IoHwAbInvalidValue

- **UUID**: `41a8d144-1c90-4172-8612-17fd061a8e44`
- **参数名**: `IoHwAbInvalidValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This field contains the initial value of a type "uint32".

########### 7. IoHwAbInvalidValueSint8

**容器属性**:

- **UUID**: `7f46cafe-67b7-498a-b02e-33d259394573`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IoHwAbInvalidValueSint8`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container for configuring an invalid value of a type "sint8".

############ 参数配置

此容器包含 **1** 个参数：

############# INTEGER 类型参数

############## 1. IoHwAbInvalidValue

- **UUID**: `6993ab73-5d35-46ca-86b2-88b5812ca176`
- **参数名**: `IoHwAbInvalidValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [-128..127]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This field contains the initial value of a type "sint8".

########### 8. IoHwAbInvalidValueSint16

**容器属性**:

- **UUID**: `180d975a-2f07-4a24-981f-fd72bc383eb3`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IoHwAbInvalidValueSint16`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container for configuring an invalid value of a type "sint16".

############ 参数配置

此容器包含 **1** 个参数：

############# INTEGER 类型参数

############## 1. IoHwAbInvalidValue

- **UUID**: `f05ebe07-97ab-41d8-831f-9c6c96be8449`
- **参数名**: `IoHwAbInvalidValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [-32768..32767]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This field contains the initial value of a type "sint16".

########### 9. IoHwAbInvalidValueSint32

**容器属性**:

- **UUID**: `e491e955-5ee9-4f76-8b97-ce3df8a76bb3`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IoHwAbInvalidValueSint32`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container for configuring an invalid value of a type "sint32".

############ 参数配置

此容器包含 **1** 个参数：

############# INTEGER 类型参数

############## 1. IoHwAbInvalidValue

- **UUID**: `5216a15f-52b0-4be2-91b5-e2fc593c86d2`
- **参数名**: `IoHwAbInvalidValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [-2147483648..2147483647]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This field contains the initial value of a type "sint32".

########### 10. IoHwAbInvalidValueType

**容器属性**:

- **UUID**: `289ed971-2914-4549-8220-d6145f506b72`
- **容器类型**: CHOICE-CONTAINER
- **容器名称**: `IoHwAbInvalidValueType`
- **多重性**: [1..1]
- **构建后可变**: false

**容器选择**:

- **IoHwAbInvalidValueBoolean**
  - UUID: `fbc4e248-f3c8-4bc8-bbd2-bfb6677b5882`
  - 描述: Container for configuring an invalid value of a type "boolean".
- **IoHwAbInvalidValueFloat32**
  - UUID: `2f2e9da1-4c91-46a2-a9d5-d4efeae48c26`
  - 描述: Container for configuring an invalid value of a type "float32".
- **IoHwAbInvalidValueFloat64**
  - UUID: `e9b907e5-22e6-4ce2-9f2a-6adebe0d3ce5`
  - 描述: Container for configuring an invalid value of a type "float64".
- **IoHwAbInvalidValueUint8**
  - UUID: `f465b96c-d804-4e17-a5ff-ad10d1057eee`
  - 描述: Container for configuring an invalid value of a type "uint8".
- **IoHwAbInvalidValueUint16**
  - UUID: `1f4065c4-b767-4ba2-afe4-c34ac1d97539`
  - 描述: Container for configuring an invalid value of a type "uint16".
- **IoHwAbInvalidValueUint32**
  - UUID: `2cfbeb44-2968-420f-915f-e456f924f21f`
  - 描述: Container for configuring an invalid value of a type "uint32".
- **IoHwAbInvalidValueSint8**
  - UUID: `7f46cafe-67b7-498a-b02e-33d259394573`
  - 描述: Container for configuring an invalid value of a type "sint8".
- **IoHwAbInvalidValueSint16**
  - UUID: `180d975a-2f07-4a24-981f-fd72bc383eb3`
  - 描述: Container for configuring an invalid value of a type "sint16".
- **IoHwAbInvalidValueSint32**
  - UUID: `e491e955-5ee9-4f76-8b97-ce3df8a76bb3`
  - 描述: Container for configuring an invalid value of a type "sint32".

**容器描述**:

This choice container is used for instantiating the appropriate type for the invalid value of the referenced data element.

Example: If the type of the referenced base data type is either an "uint8" or a type reference of an "uint8", the container "IoHwAbInvalidValueUint8" shall be chosen.

######### 2. IoHwAbInvalidValueBoolean

**容器属性**:

- **UUID**: `fbc4e248-f3c8-4bc8-bbd2-bfb6677b5882`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IoHwAbInvalidValueBoolean`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container for configuring an invalid value of a type "boolean".

########## 参数配置

此容器包含 **1** 个参数：

########### BOOLEAN 类型参数

############ 1. IoHwAbInvalidValue

- **UUID**: `359e7e9b-bd3d-4c1d-b8df-a0b34939f158`
- **参数名**: `IoHwAbInvalidValue`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This field contains the initial value of a type "boolean".

######### 3. IoHwAbInvalidValueFloat32

**容器属性**:

- **UUID**: `2f2e9da1-4c91-46a2-a9d5-d4efeae48c26`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IoHwAbInvalidValueFloat32`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container for configuring an invalid value of a type "float32".

########## 参数配置

此容器包含 **1** 个参数：

########### FLOAT 类型参数

############ 1. IoHwAbInvalidValue

- **UUID**: `d1e30bf3-35b3-41d7-bdda-eb28b3ec0419`
- **参数名**: `IoHwAbInvalidValue`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This field contains the initial value of a type "float32".

######### 4. IoHwAbInvalidValueFloat64

**容器属性**:

- **UUID**: `e9b907e5-22e6-4ce2-9f2a-6adebe0d3ce5`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IoHwAbInvalidValueFloat64`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container for configuring an invalid value of a type "float64".

########## 参数配置

此容器包含 **1** 个参数：

########### FLOAT 类型参数

############ 1. IoHwAbInvalidValue

- **UUID**: `f815ed02-2ff3-4495-aabf-26014c7ad01f`
- **参数名**: `IoHwAbInvalidValue`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This field contains the initial value of a type "float64".

######### 5. IoHwAbInvalidValueUint8

**容器属性**:

- **UUID**: `f465b96c-d804-4e17-a5ff-ad10d1057eee`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IoHwAbInvalidValueUint8`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container for configuring an invalid value of a type "uint8".

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. IoHwAbInvalidValue

- **UUID**: `f1411f40-dceb-4ec6-97c7-4776f921515a`
- **参数名**: `IoHwAbInvalidValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This field contains the initial value of a type "uint8".

######### 6. IoHwAbInvalidValueUint16

**容器属性**:

- **UUID**: `1f4065c4-b767-4ba2-afe4-c34ac1d97539`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IoHwAbInvalidValueUint16`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container for configuring an invalid value of a type "uint16".

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. IoHwAbInvalidValue

- **UUID**: `76ea2c11-a275-4ff5-9ed1-e2f81e3739b8`
- **参数名**: `IoHwAbInvalidValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This field contains the initial value of a type "uint16".

######### 7. IoHwAbInvalidValueUint32

**容器属性**:

- **UUID**: `2cfbeb44-2968-420f-915f-e456f924f21f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IoHwAbInvalidValueUint32`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container for configuring an invalid value of a type "uint32".

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. IoHwAbInvalidValue

- **UUID**: `41a8d144-1c90-4172-8612-17fd061a8e44`
- **参数名**: `IoHwAbInvalidValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This field contains the initial value of a type "uint32".

######### 8. IoHwAbInvalidValueSint8

**容器属性**:

- **UUID**: `7f46cafe-67b7-498a-b02e-33d259394573`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IoHwAbInvalidValueSint8`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container for configuring an invalid value of a type "sint8".

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. IoHwAbInvalidValue

- **UUID**: `6993ab73-5d35-46ca-86b2-88b5812ca176`
- **参数名**: `IoHwAbInvalidValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [-128..127]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This field contains the initial value of a type "sint8".

######### 9. IoHwAbInvalidValueSint16

**容器属性**:

- **UUID**: `180d975a-2f07-4a24-981f-fd72bc383eb3`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IoHwAbInvalidValueSint16`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container for configuring an invalid value of a type "sint16".

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. IoHwAbInvalidValue

- **UUID**: `f05ebe07-97ab-41d8-831f-9c6c96be8449`
- **参数名**: `IoHwAbInvalidValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [-32768..32767]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This field contains the initial value of a type "sint16".

######### 10. IoHwAbInvalidValueSint32

**容器属性**:

- **UUID**: `e491e955-5ee9-4f76-8b97-ce3df8a76bb3`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IoHwAbInvalidValueSint32`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container for configuring an invalid value of a type "sint32".

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. IoHwAbInvalidValue

- **UUID**: `5216a15f-52b0-4be2-91b5-e2fc593c86d2`
- **参数名**: `IoHwAbInvalidValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [-2147483648..2147483647]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This field contains the initial value of a type "sint32".

######### 11. IoHwAbInvalidValueType

**容器属性**:

- **UUID**: `289ed971-2914-4549-8220-d6145f506b72`
- **容器类型**: CHOICE-CONTAINER
- **容器名称**: `IoHwAbInvalidValueType`
- **多重性**: [1..1]
- **构建后可变**: false

**容器选择**:

- **IoHwAbInvalidValueBoolean**
  - UUID: `fbc4e248-f3c8-4bc8-bbd2-bfb6677b5882`
  - 描述: Container for configuring an invalid value of a type "boolean".
- **IoHwAbInvalidValueFloat32**
  - UUID: `2f2e9da1-4c91-46a2-a9d5-d4efeae48c26`
  - 描述: Container for configuring an invalid value of a type "float32".
- **IoHwAbInvalidValueFloat64**
  - UUID: `e9b907e5-22e6-4ce2-9f2a-6adebe0d3ce5`
  - 描述: Container for configuring an invalid value of a type "float64".
- **IoHwAbInvalidValueUint8**
  - UUID: `f465b96c-d804-4e17-a5ff-ad10d1057eee`
  - 描述: Container for configuring an invalid value of a type "uint8".
- **IoHwAbInvalidValueUint16**
  - UUID: `1f4065c4-b767-4ba2-afe4-c34ac1d97539`
  - 描述: Container for configuring an invalid value of a type "uint16".
- **IoHwAbInvalidValueUint32**
  - UUID: `2cfbeb44-2968-420f-915f-e456f924f21f`
  - 描述: Container for configuring an invalid value of a type "uint32".
- **IoHwAbInvalidValueSint8**
  - UUID: `7f46cafe-67b7-498a-b02e-33d259394573`
  - 描述: Container for configuring an invalid value of a type "sint8".
- **IoHwAbInvalidValueSint16**
  - UUID: `180d975a-2f07-4a24-981f-fd72bc383eb3`
  - 描述: Container for configuring an invalid value of a type "sint16".
- **IoHwAbInvalidValueSint32**
  - UUID: `e491e955-5ee9-4f76-8b97-ce3df8a76bb3`
  - 描述: Container for configuring an invalid value of a type "sint32".

**容器描述**:

This choice container is used for instantiating the appropriate type for the invalid value of the referenced data element.

Example: If the type of the referenced base data type is either an "uint8" or a type reference of an "uint8", the container "IoHwAbInvalidValueUint8" shall be chosen.

####### 2. IoHwAbInvalidValue

**容器属性**:

- **UUID**: `5ca5978e-f620-4c40-ace2-df3e7b3618de`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IoHwAbInvalidValue`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Optional container for configuring an invalid value for a IoHwAb type reference.

######## 配置容器

本模块包含 **10** 个配置容器：

######### 1. IoHwAbInvalidValueBoolean

**容器属性**:

- **UUID**: `fbc4e248-f3c8-4bc8-bbd2-bfb6677b5882`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IoHwAbInvalidValueBoolean`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container for configuring an invalid value of a type "boolean".

########## 参数配置

此容器包含 **1** 个参数：

########### BOOLEAN 类型参数

############ 1. IoHwAbInvalidValue

- **UUID**: `359e7e9b-bd3d-4c1d-b8df-a0b34939f158`
- **参数名**: `IoHwAbInvalidValue`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This field contains the initial value of a type "boolean".

######### 2. IoHwAbInvalidValueFloat32

**容器属性**:

- **UUID**: `2f2e9da1-4c91-46a2-a9d5-d4efeae48c26`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IoHwAbInvalidValueFloat32`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container for configuring an invalid value of a type "float32".

########## 参数配置

此容器包含 **1** 个参数：

########### FLOAT 类型参数

############ 1. IoHwAbInvalidValue

- **UUID**: `d1e30bf3-35b3-41d7-bdda-eb28b3ec0419`
- **参数名**: `IoHwAbInvalidValue`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This field contains the initial value of a type "float32".

######### 3. IoHwAbInvalidValueFloat64

**容器属性**:

- **UUID**: `e9b907e5-22e6-4ce2-9f2a-6adebe0d3ce5`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IoHwAbInvalidValueFloat64`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container for configuring an invalid value of a type "float64".

########## 参数配置

此容器包含 **1** 个参数：

########### FLOAT 类型参数

############ 1. IoHwAbInvalidValue

- **UUID**: `f815ed02-2ff3-4495-aabf-26014c7ad01f`
- **参数名**: `IoHwAbInvalidValue`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This field contains the initial value of a type "float64".

######### 4. IoHwAbInvalidValueUint8

**容器属性**:

- **UUID**: `f465b96c-d804-4e17-a5ff-ad10d1057eee`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IoHwAbInvalidValueUint8`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container for configuring an invalid value of a type "uint8".

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. IoHwAbInvalidValue

- **UUID**: `f1411f40-dceb-4ec6-97c7-4776f921515a`
- **参数名**: `IoHwAbInvalidValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This field contains the initial value of a type "uint8".

######### 5. IoHwAbInvalidValueUint16

**容器属性**:

- **UUID**: `1f4065c4-b767-4ba2-afe4-c34ac1d97539`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IoHwAbInvalidValueUint16`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container for configuring an invalid value of a type "uint16".

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. IoHwAbInvalidValue

- **UUID**: `76ea2c11-a275-4ff5-9ed1-e2f81e3739b8`
- **参数名**: `IoHwAbInvalidValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This field contains the initial value of a type "uint16".

######### 6. IoHwAbInvalidValueUint32

**容器属性**:

- **UUID**: `2cfbeb44-2968-420f-915f-e456f924f21f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IoHwAbInvalidValueUint32`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container for configuring an invalid value of a type "uint32".

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. IoHwAbInvalidValue

- **UUID**: `41a8d144-1c90-4172-8612-17fd061a8e44`
- **参数名**: `IoHwAbInvalidValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This field contains the initial value of a type "uint32".

######### 7. IoHwAbInvalidValueSint8

**容器属性**:

- **UUID**: `7f46cafe-67b7-498a-b02e-33d259394573`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IoHwAbInvalidValueSint8`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container for configuring an invalid value of a type "sint8".

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. IoHwAbInvalidValue

- **UUID**: `6993ab73-5d35-46ca-86b2-88b5812ca176`
- **参数名**: `IoHwAbInvalidValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [-128..127]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This field contains the initial value of a type "sint8".

######### 8. IoHwAbInvalidValueSint16

**容器属性**:

- **UUID**: `180d975a-2f07-4a24-981f-fd72bc383eb3`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IoHwAbInvalidValueSint16`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container for configuring an invalid value of a type "sint16".

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. IoHwAbInvalidValue

- **UUID**: `f05ebe07-97ab-41d8-831f-9c6c96be8449`
- **参数名**: `IoHwAbInvalidValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [-32768..32767]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This field contains the initial value of a type "sint16".

######### 9. IoHwAbInvalidValueSint32

**容器属性**:

- **UUID**: `e491e955-5ee9-4f76-8b97-ce3df8a76bb3`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IoHwAbInvalidValueSint32`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container for configuring an invalid value of a type "sint32".

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. IoHwAbInvalidValue

- **UUID**: `5216a15f-52b0-4be2-91b5-e2fc593c86d2`
- **参数名**: `IoHwAbInvalidValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [-2147483648..2147483647]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This field contains the initial value of a type "sint32".

######### 10. IoHwAbInvalidValueType

**容器属性**:

- **UUID**: `289ed971-2914-4549-8220-d6145f506b72`
- **容器类型**: CHOICE-CONTAINER
- **容器名称**: `IoHwAbInvalidValueType`
- **多重性**: [1..1]
- **构建后可变**: false

**容器选择**:

- **IoHwAbInvalidValueBoolean**
  - UUID: `fbc4e248-f3c8-4bc8-bbd2-bfb6677b5882`
  - 描述: Container for configuring an invalid value of a type "boolean".
- **IoHwAbInvalidValueFloat32**
  - UUID: `2f2e9da1-4c91-46a2-a9d5-d4efeae48c26`
  - 描述: Container for configuring an invalid value of a type "float32".
- **IoHwAbInvalidValueFloat64**
  - UUID: `e9b907e5-22e6-4ce2-9f2a-6adebe0d3ce5`
  - 描述: Container for configuring an invalid value of a type "float64".
- **IoHwAbInvalidValueUint8**
  - UUID: `f465b96c-d804-4e17-a5ff-ad10d1057eee`
  - 描述: Container for configuring an invalid value of a type "uint8".
- **IoHwAbInvalidValueUint16**
  - UUID: `1f4065c4-b767-4ba2-afe4-c34ac1d97539`
  - 描述: Container for configuring an invalid value of a type "uint16".
- **IoHwAbInvalidValueUint32**
  - UUID: `2cfbeb44-2968-420f-915f-e456f924f21f`
  - 描述: Container for configuring an invalid value of a type "uint32".
- **IoHwAbInvalidValueSint8**
  - UUID: `7f46cafe-67b7-498a-b02e-33d259394573`
  - 描述: Container for configuring an invalid value of a type "sint8".
- **IoHwAbInvalidValueSint16**
  - UUID: `180d975a-2f07-4a24-981f-fd72bc383eb3`
  - 描述: Container for configuring an invalid value of a type "sint16".
- **IoHwAbInvalidValueSint32**
  - UUID: `e491e955-5ee9-4f76-8b97-ce3df8a76bb3`
  - 描述: Container for configuring an invalid value of a type "sint32".

**容器描述**:

This choice container is used for instantiating the appropriate type for the invalid value of the referenced data element.

Example: If the type of the referenced base data type is either an "uint8" or a type reference of an "uint8", the container "IoHwAbInvalidValueUint8" shall be chosen.

####### 3. IoHwAbInvalidValueBoolean

**容器属性**:

- **UUID**: `fbc4e248-f3c8-4bc8-bbd2-bfb6677b5882`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IoHwAbInvalidValueBoolean`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container for configuring an invalid value of a type "boolean".

######## 参数配置

此容器包含 **1** 个参数：

######### BOOLEAN 类型参数

########## 1. IoHwAbInvalidValue

- **UUID**: `359e7e9b-bd3d-4c1d-b8df-a0b34939f158`
- **参数名**: `IoHwAbInvalidValue`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This field contains the initial value of a type "boolean".

####### 4. IoHwAbInvalidValueFloat32

**容器属性**:

- **UUID**: `2f2e9da1-4c91-46a2-a9d5-d4efeae48c26`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IoHwAbInvalidValueFloat32`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container for configuring an invalid value of a type "float32".

######## 参数配置

此容器包含 **1** 个参数：

######### FLOAT 类型参数

########## 1. IoHwAbInvalidValue

- **UUID**: `d1e30bf3-35b3-41d7-bdda-eb28b3ec0419`
- **参数名**: `IoHwAbInvalidValue`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This field contains the initial value of a type "float32".

####### 5. IoHwAbInvalidValueFloat64

**容器属性**:

- **UUID**: `e9b907e5-22e6-4ce2-9f2a-6adebe0d3ce5`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IoHwAbInvalidValueFloat64`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container for configuring an invalid value of a type "float64".

######## 参数配置

此容器包含 **1** 个参数：

######### FLOAT 类型参数

########## 1. IoHwAbInvalidValue

- **UUID**: `f815ed02-2ff3-4495-aabf-26014c7ad01f`
- **参数名**: `IoHwAbInvalidValue`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This field contains the initial value of a type "float64".

####### 6. IoHwAbInvalidValueUint8

**容器属性**:

- **UUID**: `f465b96c-d804-4e17-a5ff-ad10d1057eee`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IoHwAbInvalidValueUint8`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container for configuring an invalid value of a type "uint8".

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. IoHwAbInvalidValue

- **UUID**: `f1411f40-dceb-4ec6-97c7-4776f921515a`
- **参数名**: `IoHwAbInvalidValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This field contains the initial value of a type "uint8".

####### 7. IoHwAbInvalidValueUint16

**容器属性**:

- **UUID**: `1f4065c4-b767-4ba2-afe4-c34ac1d97539`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IoHwAbInvalidValueUint16`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container for configuring an invalid value of a type "uint16".

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. IoHwAbInvalidValue

- **UUID**: `76ea2c11-a275-4ff5-9ed1-e2f81e3739b8`
- **参数名**: `IoHwAbInvalidValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This field contains the initial value of a type "uint16".

####### 8. IoHwAbInvalidValueUint32

**容器属性**:

- **UUID**: `2cfbeb44-2968-420f-915f-e456f924f21f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IoHwAbInvalidValueUint32`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container for configuring an invalid value of a type "uint32".

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. IoHwAbInvalidValue

- **UUID**: `41a8d144-1c90-4172-8612-17fd061a8e44`
- **参数名**: `IoHwAbInvalidValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This field contains the initial value of a type "uint32".

####### 9. IoHwAbInvalidValueSint8

**容器属性**:

- **UUID**: `7f46cafe-67b7-498a-b02e-33d259394573`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IoHwAbInvalidValueSint8`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container for configuring an invalid value of a type "sint8".

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. IoHwAbInvalidValue

- **UUID**: `6993ab73-5d35-46ca-86b2-88b5812ca176`
- **参数名**: `IoHwAbInvalidValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [-128..127]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This field contains the initial value of a type "sint8".

####### 10. IoHwAbInvalidValueSint16

**容器属性**:

- **UUID**: `180d975a-2f07-4a24-981f-fd72bc383eb3`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IoHwAbInvalidValueSint16`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container for configuring an invalid value of a type "sint16".

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. IoHwAbInvalidValue

- **UUID**: `f05ebe07-97ab-41d8-831f-9c6c96be8449`
- **参数名**: `IoHwAbInvalidValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [-32768..32767]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This field contains the initial value of a type "sint16".

####### 11. IoHwAbInvalidValueSint32

**容器属性**:

- **UUID**: `e491e955-5ee9-4f76-8b97-ce3df8a76bb3`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IoHwAbInvalidValueSint32`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container for configuring an invalid value of a type "sint32".

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. IoHwAbInvalidValue

- **UUID**: `5216a15f-52b0-4be2-91b5-e2fc593c86d2`
- **参数名**: `IoHwAbInvalidValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [-2147483648..2147483647]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This field contains the initial value of a type "sint32".

####### 12. IoHwAbArray

**容器属性**:

- **UUID**: `1d9571d0-22d2-47a2-af79-82de8f7c0667`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IoHwAbArray`
- **多重性**: [0..infinite]
- **构建后可变**: false

**容器描述**:

Container for configuring an array type. An array type is the typedef of an array containing n data elements of a base type or a type reference, i.e. the generated files (e.g. Rte_Type.h) will contain a typedef like the following example:

typedef uint8 AlternatorPower_au8[13];

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. IoHwAbArraySize

- **UUID**: `a5f4d81e-a052-40be-9dd0-aacac5846259`
- **参数名**: `IoHwAbArraySize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `5`
- **取值范围**: [0..18446744073709551615]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Parameter for the configuration of the array size, i.e. the number of elements of the selected datatype.

######## 引用关系

此容器包含 **1** 个引用：

######### CHOICE-REFERENCE 类型引用

########## 1. IoHwAbArrayTypeRef

- **UUID**: `483e268d-4de7-4ebe-a5e3-1e4c9bb0abdc`
- **引用名**: `IoHwAbArrayTypeRef`
- **引用类型**: CHOICE-REFERENCE
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **需要索引**: false
- **目标引用列表**:
  - `/MICROSAR/IoHwAb/IoHwAbDatatypes/IoHwAbBaseType`
  - `/MICROSAR/IoHwAb/IoHwAbDatatypes/IoHwAbImplementationTypes/IoHwAbTypeReference`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Parameter for the selection of the datatype of the array elements.

####### 13. IoHwAbRecord

**容器属性**:

- **UUID**: `2dc30056-499e-44bf-92b4-13e8b9147b2d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IoHwAbRecord`
- **多重性**: [0..infinite]
- **构建后可变**: false

**容器描述**:

Container for configuring a record/struct type. An record type is the typedef of a struct containing data elements of a base type or a type reference, i.e. the generated files (e.g. Rte_Type.h) will contain a typedef like the following example:

typedef struct
{
    uint16 Period;
    uint16 ActiveTime;
}DutyCycle;

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. IoHwAbRecordElement

**容器属性**:

- **UUID**: `fb24fab4-1b14-4d65-ba77-b58f2f2acabb`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IoHwAbRecordElement`
- **多重性**: [1..infinite]
- **构建后可变**: false

**容器描述**:

Container for configuring a record/struct element.

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. IoHwAbRecordElementPosition

- **UUID**: `274130e5-6acd-425a-95be-33c8df98940c`
- **参数名**: `IoHwAbRecordElementPosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..255]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter contains the position of the of the record element inside the record.

########## 引用关系

此容器包含 **1** 个引用：

########### CHOICE-REFERENCE 类型引用

############ 1. IoHwAbRecordElementTypeRef

- **UUID**: `b21ae229-f1b5-431e-a04f-9a9233f48f86`
- **引用名**: `IoHwAbRecordElementTypeRef`
- **引用类型**: CHOICE-REFERENCE
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **需要索引**: false
- **目标引用列表**:
  - `/MICROSAR/IoHwAb/IoHwAbDatatypes/IoHwAbBaseType`
  - `/MICROSAR/IoHwAb/IoHwAbDatatypes/IoHwAbImplementationTypes/IoHwAbTypeReference`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Parameter for the selection of the datatype of the struct/record elements.

####### 14. IoHwAbRecordElement

**容器属性**:

- **UUID**: `fb24fab4-1b14-4d65-ba77-b58f2f2acabb`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IoHwAbRecordElement`
- **多重性**: [1..infinite]
- **构建后可变**: false

**容器描述**:

Container for configuring a record/struct element.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. IoHwAbRecordElementPosition

- **UUID**: `274130e5-6acd-425a-95be-33c8df98940c`
- **参数名**: `IoHwAbRecordElementPosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..255]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter contains the position of the of the record element inside the record.

######## 引用关系

此容器包含 **1** 个引用：

######### CHOICE-REFERENCE 类型引用

########## 1. IoHwAbRecordElementTypeRef

- **UUID**: `b21ae229-f1b5-431e-a04f-9a9233f48f86`
- **引用名**: `IoHwAbRecordElementTypeRef`
- **引用类型**: CHOICE-REFERENCE
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **需要索引**: false
- **目标引用列表**:
  - `/MICROSAR/IoHwAb/IoHwAbDatatypes/IoHwAbBaseType`
  - `/MICROSAR/IoHwAb/IoHwAbDatatypes/IoHwAbImplementationTypes/IoHwAbTypeReference`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Parameter for the selection of the datatype of the struct/record elements.

####### 15. IoHwAbInvalidValueType

**容器属性**:

- **UUID**: `289ed971-2914-4549-8220-d6145f506b72`
- **容器类型**: CHOICE-CONTAINER
- **容器名称**: `IoHwAbInvalidValueType`
- **多重性**: [1..1]
- **构建后可变**: false

**容器选择**:

- **IoHwAbInvalidValueBoolean**
  - UUID: `fbc4e248-f3c8-4bc8-bbd2-bfb6677b5882`
  - 描述: Container for configuring an invalid value of a type "boolean".
- **IoHwAbInvalidValueFloat32**
  - UUID: `2f2e9da1-4c91-46a2-a9d5-d4efeae48c26`
  - 描述: Container for configuring an invalid value of a type "float32".
- **IoHwAbInvalidValueFloat64**
  - UUID: `e9b907e5-22e6-4ce2-9f2a-6adebe0d3ce5`
  - 描述: Container for configuring an invalid value of a type "float64".
- **IoHwAbInvalidValueUint8**
  - UUID: `f465b96c-d804-4e17-a5ff-ad10d1057eee`
  - 描述: Container for configuring an invalid value of a type "uint8".
- **IoHwAbInvalidValueUint16**
  - UUID: `1f4065c4-b767-4ba2-afe4-c34ac1d97539`
  - 描述: Container for configuring an invalid value of a type "uint16".
- **IoHwAbInvalidValueUint32**
  - UUID: `2cfbeb44-2968-420f-915f-e456f924f21f`
  - 描述: Container for configuring an invalid value of a type "uint32".
- **IoHwAbInvalidValueSint8**
  - UUID: `7f46cafe-67b7-498a-b02e-33d259394573`
  - 描述: Container for configuring an invalid value of a type "sint8".
- **IoHwAbInvalidValueSint16**
  - UUID: `180d975a-2f07-4a24-981f-fd72bc383eb3`
  - 描述: Container for configuring an invalid value of a type "sint16".
- **IoHwAbInvalidValueSint32**
  - UUID: `e491e955-5ee9-4f76-8b97-ce3df8a76bb3`
  - 描述: Container for configuring an invalid value of a type "sint32".

**容器描述**:

This choice container is used for instantiating the appropriate type for the invalid value of the referenced data element.

Example: If the type of the referenced base data type is either an "uint8" or a type reference of an "uint8", the container "IoHwAbInvalidValueUint8" shall be chosen.

##### 4. IoHwAbTypeReference

**容器属性**:

- **UUID**: `4c4ad53e-8366-4d22-99a4-1ab863f99edf`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IoHwAbTypeReference`
- **多重性**: [0..infinite]
- **构建后可变**: false

**容器描述**:

Container for configuring a type reference. A type reference is a deviation from a base type, i.e. the generated files (e.g. Rte_Type.h) will contain a typedef like the following example:

typedef sint8 BatteryVoltageValue;

###### 引用关系

此容器包含 **1** 个引用：

####### CHOICE-REFERENCE 类型引用

######## 1. IoHwAbTypeReferenceTypeRef

- **UUID**: `be6126a0-a374-41f1-9a7a-9cf53955a504`
- **引用名**: `IoHwAbTypeReferenceTypeRef`
- **引用类型**: CHOICE-REFERENCE
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **需要索引**: false
- **目标引用列表**:
  - `/MICROSAR/IoHwAb/IoHwAbDatatypes/IoHwAbBaseType`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Parameter for the selection of the datatype of the type reference.

###### 配置容器

本模块包含 **11** 个配置容器：

####### 1. IoHwAbInvalidValue

**容器属性**:

- **UUID**: `5ca5978e-f620-4c40-ace2-df3e7b3618de`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IoHwAbInvalidValue`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Optional container for configuring an invalid value for a IoHwAb type reference.

######## 配置容器

本模块包含 **10** 个配置容器：

######### 1. IoHwAbInvalidValueBoolean

**容器属性**:

- **UUID**: `fbc4e248-f3c8-4bc8-bbd2-bfb6677b5882`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IoHwAbInvalidValueBoolean`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container for configuring an invalid value of a type "boolean".

########## 参数配置

此容器包含 **1** 个参数：

########### BOOLEAN 类型参数

############ 1. IoHwAbInvalidValue

- **UUID**: `359e7e9b-bd3d-4c1d-b8df-a0b34939f158`
- **参数名**: `IoHwAbInvalidValue`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This field contains the initial value of a type "boolean".

######### 2. IoHwAbInvalidValueFloat32

**容器属性**:

- **UUID**: `2f2e9da1-4c91-46a2-a9d5-d4efeae48c26`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IoHwAbInvalidValueFloat32`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container for configuring an invalid value of a type "float32".

########## 参数配置

此容器包含 **1** 个参数：

########### FLOAT 类型参数

############ 1. IoHwAbInvalidValue

- **UUID**: `d1e30bf3-35b3-41d7-bdda-eb28b3ec0419`
- **参数名**: `IoHwAbInvalidValue`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This field contains the initial value of a type "float32".

######### 3. IoHwAbInvalidValueFloat64

**容器属性**:

- **UUID**: `e9b907e5-22e6-4ce2-9f2a-6adebe0d3ce5`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IoHwAbInvalidValueFloat64`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container for configuring an invalid value of a type "float64".

########## 参数配置

此容器包含 **1** 个参数：

########### FLOAT 类型参数

############ 1. IoHwAbInvalidValue

- **UUID**: `f815ed02-2ff3-4495-aabf-26014c7ad01f`
- **参数名**: `IoHwAbInvalidValue`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This field contains the initial value of a type "float64".

######### 4. IoHwAbInvalidValueUint8

**容器属性**:

- **UUID**: `f465b96c-d804-4e17-a5ff-ad10d1057eee`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IoHwAbInvalidValueUint8`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container for configuring an invalid value of a type "uint8".

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. IoHwAbInvalidValue

- **UUID**: `f1411f40-dceb-4ec6-97c7-4776f921515a`
- **参数名**: `IoHwAbInvalidValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This field contains the initial value of a type "uint8".

######### 5. IoHwAbInvalidValueUint16

**容器属性**:

- **UUID**: `1f4065c4-b767-4ba2-afe4-c34ac1d97539`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IoHwAbInvalidValueUint16`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container for configuring an invalid value of a type "uint16".

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. IoHwAbInvalidValue

- **UUID**: `76ea2c11-a275-4ff5-9ed1-e2f81e3739b8`
- **参数名**: `IoHwAbInvalidValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This field contains the initial value of a type "uint16".

######### 6. IoHwAbInvalidValueUint32

**容器属性**:

- **UUID**: `2cfbeb44-2968-420f-915f-e456f924f21f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IoHwAbInvalidValueUint32`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container for configuring an invalid value of a type "uint32".

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. IoHwAbInvalidValue

- **UUID**: `41a8d144-1c90-4172-8612-17fd061a8e44`
- **参数名**: `IoHwAbInvalidValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This field contains the initial value of a type "uint32".

######### 7. IoHwAbInvalidValueSint8

**容器属性**:

- **UUID**: `7f46cafe-67b7-498a-b02e-33d259394573`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IoHwAbInvalidValueSint8`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container for configuring an invalid value of a type "sint8".

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. IoHwAbInvalidValue

- **UUID**: `6993ab73-5d35-46ca-86b2-88b5812ca176`
- **参数名**: `IoHwAbInvalidValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [-128..127]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This field contains the initial value of a type "sint8".

######### 8. IoHwAbInvalidValueSint16

**容器属性**:

- **UUID**: `180d975a-2f07-4a24-981f-fd72bc383eb3`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IoHwAbInvalidValueSint16`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container for configuring an invalid value of a type "sint16".

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. IoHwAbInvalidValue

- **UUID**: `f05ebe07-97ab-41d8-831f-9c6c96be8449`
- **参数名**: `IoHwAbInvalidValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [-32768..32767]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This field contains the initial value of a type "sint16".

######### 9. IoHwAbInvalidValueSint32

**容器属性**:

- **UUID**: `e491e955-5ee9-4f76-8b97-ce3df8a76bb3`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IoHwAbInvalidValueSint32`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container for configuring an invalid value of a type "sint32".

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. IoHwAbInvalidValue

- **UUID**: `5216a15f-52b0-4be2-91b5-e2fc593c86d2`
- **参数名**: `IoHwAbInvalidValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [-2147483648..2147483647]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This field contains the initial value of a type "sint32".

######### 10. IoHwAbInvalidValueType

**容器属性**:

- **UUID**: `289ed971-2914-4549-8220-d6145f506b72`
- **容器类型**: CHOICE-CONTAINER
- **容器名称**: `IoHwAbInvalidValueType`
- **多重性**: [1..1]
- **构建后可变**: false

**容器选择**:

- **IoHwAbInvalidValueBoolean**
  - UUID: `fbc4e248-f3c8-4bc8-bbd2-bfb6677b5882`
  - 描述: Container for configuring an invalid value of a type "boolean".
- **IoHwAbInvalidValueFloat32**
  - UUID: `2f2e9da1-4c91-46a2-a9d5-d4efeae48c26`
  - 描述: Container for configuring an invalid value of a type "float32".
- **IoHwAbInvalidValueFloat64**
  - UUID: `e9b907e5-22e6-4ce2-9f2a-6adebe0d3ce5`
  - 描述: Container for configuring an invalid value of a type "float64".
- **IoHwAbInvalidValueUint8**
  - UUID: `f465b96c-d804-4e17-a5ff-ad10d1057eee`
  - 描述: Container for configuring an invalid value of a type "uint8".
- **IoHwAbInvalidValueUint16**
  - UUID: `1f4065c4-b767-4ba2-afe4-c34ac1d97539`
  - 描述: Container for configuring an invalid value of a type "uint16".
- **IoHwAbInvalidValueUint32**
  - UUID: `2cfbeb44-2968-420f-915f-e456f924f21f`
  - 描述: Container for configuring an invalid value of a type "uint32".
- **IoHwAbInvalidValueSint8**
  - UUID: `7f46cafe-67b7-498a-b02e-33d259394573`
  - 描述: Container for configuring an invalid value of a type "sint8".
- **IoHwAbInvalidValueSint16**
  - UUID: `180d975a-2f07-4a24-981f-fd72bc383eb3`
  - 描述: Container for configuring an invalid value of a type "sint16".
- **IoHwAbInvalidValueSint32**
  - UUID: `e491e955-5ee9-4f76-8b97-ce3df8a76bb3`
  - 描述: Container for configuring an invalid value of a type "sint32".

**容器描述**:

This choice container is used for instantiating the appropriate type for the invalid value of the referenced data element.

Example: If the type of the referenced base data type is either an "uint8" or a type reference of an "uint8", the container "IoHwAbInvalidValueUint8" shall be chosen.

####### 2. IoHwAbInvalidValueBoolean

**容器属性**:

- **UUID**: `fbc4e248-f3c8-4bc8-bbd2-bfb6677b5882`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IoHwAbInvalidValueBoolean`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container for configuring an invalid value of a type "boolean".

######## 参数配置

此容器包含 **1** 个参数：

######### BOOLEAN 类型参数

########## 1. IoHwAbInvalidValue

- **UUID**: `359e7e9b-bd3d-4c1d-b8df-a0b34939f158`
- **参数名**: `IoHwAbInvalidValue`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This field contains the initial value of a type "boolean".

####### 3. IoHwAbInvalidValueFloat32

**容器属性**:

- **UUID**: `2f2e9da1-4c91-46a2-a9d5-d4efeae48c26`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IoHwAbInvalidValueFloat32`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container for configuring an invalid value of a type "float32".

######## 参数配置

此容器包含 **1** 个参数：

######### FLOAT 类型参数

########## 1. IoHwAbInvalidValue

- **UUID**: `d1e30bf3-35b3-41d7-bdda-eb28b3ec0419`
- **参数名**: `IoHwAbInvalidValue`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This field contains the initial value of a type "float32".

####### 4. IoHwAbInvalidValueFloat64

**容器属性**:

- **UUID**: `e9b907e5-22e6-4ce2-9f2a-6adebe0d3ce5`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IoHwAbInvalidValueFloat64`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container for configuring an invalid value of a type "float64".

######## 参数配置

此容器包含 **1** 个参数：

######### FLOAT 类型参数

########## 1. IoHwAbInvalidValue

- **UUID**: `f815ed02-2ff3-4495-aabf-26014c7ad01f`
- **参数名**: `IoHwAbInvalidValue`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This field contains the initial value of a type "float64".

####### 5. IoHwAbInvalidValueUint8

**容器属性**:

- **UUID**: `f465b96c-d804-4e17-a5ff-ad10d1057eee`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IoHwAbInvalidValueUint8`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container for configuring an invalid value of a type "uint8".

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. IoHwAbInvalidValue

- **UUID**: `f1411f40-dceb-4ec6-97c7-4776f921515a`
- **参数名**: `IoHwAbInvalidValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This field contains the initial value of a type "uint8".

####### 6. IoHwAbInvalidValueUint16

**容器属性**:

- **UUID**: `1f4065c4-b767-4ba2-afe4-c34ac1d97539`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IoHwAbInvalidValueUint16`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container for configuring an invalid value of a type "uint16".

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. IoHwAbInvalidValue

- **UUID**: `76ea2c11-a275-4ff5-9ed1-e2f81e3739b8`
- **参数名**: `IoHwAbInvalidValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This field contains the initial value of a type "uint16".

####### 7. IoHwAbInvalidValueUint32

**容器属性**:

- **UUID**: `2cfbeb44-2968-420f-915f-e456f924f21f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IoHwAbInvalidValueUint32`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container for configuring an invalid value of a type "uint32".

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. IoHwAbInvalidValue

- **UUID**: `41a8d144-1c90-4172-8612-17fd061a8e44`
- **参数名**: `IoHwAbInvalidValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This field contains the initial value of a type "uint32".

####### 8. IoHwAbInvalidValueSint8

**容器属性**:

- **UUID**: `7f46cafe-67b7-498a-b02e-33d259394573`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IoHwAbInvalidValueSint8`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container for configuring an invalid value of a type "sint8".

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. IoHwAbInvalidValue

- **UUID**: `6993ab73-5d35-46ca-86b2-88b5812ca176`
- **参数名**: `IoHwAbInvalidValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [-128..127]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This field contains the initial value of a type "sint8".

####### 9. IoHwAbInvalidValueSint16

**容器属性**:

- **UUID**: `180d975a-2f07-4a24-981f-fd72bc383eb3`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IoHwAbInvalidValueSint16`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container for configuring an invalid value of a type "sint16".

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. IoHwAbInvalidValue

- **UUID**: `f05ebe07-97ab-41d8-831f-9c6c96be8449`
- **参数名**: `IoHwAbInvalidValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [-32768..32767]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This field contains the initial value of a type "sint16".

####### 10. IoHwAbInvalidValueSint32

**容器属性**:

- **UUID**: `e491e955-5ee9-4f76-8b97-ce3df8a76bb3`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IoHwAbInvalidValueSint32`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container for configuring an invalid value of a type "sint32".

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. IoHwAbInvalidValue

- **UUID**: `5216a15f-52b0-4be2-91b5-e2fc593c86d2`
- **参数名**: `IoHwAbInvalidValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [-2147483648..2147483647]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This field contains the initial value of a type "sint32".

####### 11. IoHwAbInvalidValueType

**容器属性**:

- **UUID**: `289ed971-2914-4549-8220-d6145f506b72`
- **容器类型**: CHOICE-CONTAINER
- **容器名称**: `IoHwAbInvalidValueType`
- **多重性**: [1..1]
- **构建后可变**: false

**容器选择**:

- **IoHwAbInvalidValueBoolean**
  - UUID: `fbc4e248-f3c8-4bc8-bbd2-bfb6677b5882`
  - 描述: Container for configuring an invalid value of a type "boolean".
- **IoHwAbInvalidValueFloat32**
  - UUID: `2f2e9da1-4c91-46a2-a9d5-d4efeae48c26`
  - 描述: Container for configuring an invalid value of a type "float32".
- **IoHwAbInvalidValueFloat64**
  - UUID: `e9b907e5-22e6-4ce2-9f2a-6adebe0d3ce5`
  - 描述: Container for configuring an invalid value of a type "float64".
- **IoHwAbInvalidValueUint8**
  - UUID: `f465b96c-d804-4e17-a5ff-ad10d1057eee`
  - 描述: Container for configuring an invalid value of a type "uint8".
- **IoHwAbInvalidValueUint16**
  - UUID: `1f4065c4-b767-4ba2-afe4-c34ac1d97539`
  - 描述: Container for configuring an invalid value of a type "uint16".
- **IoHwAbInvalidValueUint32**
  - UUID: `2cfbeb44-2968-420f-915f-e456f924f21f`
  - 描述: Container for configuring an invalid value of a type "uint32".
- **IoHwAbInvalidValueSint8**
  - UUID: `7f46cafe-67b7-498a-b02e-33d259394573`
  - 描述: Container for configuring an invalid value of a type "sint8".
- **IoHwAbInvalidValueSint16**
  - UUID: `180d975a-2f07-4a24-981f-fd72bc383eb3`
  - 描述: Container for configuring an invalid value of a type "sint16".
- **IoHwAbInvalidValueSint32**
  - UUID: `e491e955-5ee9-4f76-8b97-ce3df8a76bb3`
  - 描述: Container for configuring an invalid value of a type "sint32".

**容器描述**:

This choice container is used for instantiating the appropriate type for the invalid value of the referenced data element.

Example: If the type of the referenced base data type is either an "uint8" or a type reference of an "uint8", the container "IoHwAbInvalidValueUint8" shall be chosen.

##### 5. IoHwAbInvalidValue

**容器属性**:

- **UUID**: `5ca5978e-f620-4c40-ace2-df3e7b3618de`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IoHwAbInvalidValue`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Optional container for configuring an invalid value for a IoHwAb type reference.

###### 配置容器

本模块包含 **10** 个配置容器：

####### 1. IoHwAbInvalidValueBoolean

**容器属性**:

- **UUID**: `fbc4e248-f3c8-4bc8-bbd2-bfb6677b5882`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IoHwAbInvalidValueBoolean`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container for configuring an invalid value of a type "boolean".

######## 参数配置

此容器包含 **1** 个参数：

######### BOOLEAN 类型参数

########## 1. IoHwAbInvalidValue

- **UUID**: `359e7e9b-bd3d-4c1d-b8df-a0b34939f158`
- **参数名**: `IoHwAbInvalidValue`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This field contains the initial value of a type "boolean".

####### 2. IoHwAbInvalidValueFloat32

**容器属性**:

- **UUID**: `2f2e9da1-4c91-46a2-a9d5-d4efeae48c26`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IoHwAbInvalidValueFloat32`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container for configuring an invalid value of a type "float32".

######## 参数配置

此容器包含 **1** 个参数：

######### FLOAT 类型参数

########## 1. IoHwAbInvalidValue

- **UUID**: `d1e30bf3-35b3-41d7-bdda-eb28b3ec0419`
- **参数名**: `IoHwAbInvalidValue`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This field contains the initial value of a type "float32".

####### 3. IoHwAbInvalidValueFloat64

**容器属性**:

- **UUID**: `e9b907e5-22e6-4ce2-9f2a-6adebe0d3ce5`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IoHwAbInvalidValueFloat64`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container for configuring an invalid value of a type "float64".

######## 参数配置

此容器包含 **1** 个参数：

######### FLOAT 类型参数

########## 1. IoHwAbInvalidValue

- **UUID**: `f815ed02-2ff3-4495-aabf-26014c7ad01f`
- **参数名**: `IoHwAbInvalidValue`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This field contains the initial value of a type "float64".

####### 4. IoHwAbInvalidValueUint8

**容器属性**:

- **UUID**: `f465b96c-d804-4e17-a5ff-ad10d1057eee`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IoHwAbInvalidValueUint8`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container for configuring an invalid value of a type "uint8".

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. IoHwAbInvalidValue

- **UUID**: `f1411f40-dceb-4ec6-97c7-4776f921515a`
- **参数名**: `IoHwAbInvalidValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This field contains the initial value of a type "uint8".

####### 5. IoHwAbInvalidValueUint16

**容器属性**:

- **UUID**: `1f4065c4-b767-4ba2-afe4-c34ac1d97539`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IoHwAbInvalidValueUint16`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container for configuring an invalid value of a type "uint16".

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. IoHwAbInvalidValue

- **UUID**: `76ea2c11-a275-4ff5-9ed1-e2f81e3739b8`
- **参数名**: `IoHwAbInvalidValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This field contains the initial value of a type "uint16".

####### 6. IoHwAbInvalidValueUint32

**容器属性**:

- **UUID**: `2cfbeb44-2968-420f-915f-e456f924f21f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IoHwAbInvalidValueUint32`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container for configuring an invalid value of a type "uint32".

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. IoHwAbInvalidValue

- **UUID**: `41a8d144-1c90-4172-8612-17fd061a8e44`
- **参数名**: `IoHwAbInvalidValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This field contains the initial value of a type "uint32".

####### 7. IoHwAbInvalidValueSint8

**容器属性**:

- **UUID**: `7f46cafe-67b7-498a-b02e-33d259394573`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IoHwAbInvalidValueSint8`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container for configuring an invalid value of a type "sint8".

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. IoHwAbInvalidValue

- **UUID**: `6993ab73-5d35-46ca-86b2-88b5812ca176`
- **参数名**: `IoHwAbInvalidValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [-128..127]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This field contains the initial value of a type "sint8".

####### 8. IoHwAbInvalidValueSint16

**容器属性**:

- **UUID**: `180d975a-2f07-4a24-981f-fd72bc383eb3`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IoHwAbInvalidValueSint16`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container for configuring an invalid value of a type "sint16".

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. IoHwAbInvalidValue

- **UUID**: `f05ebe07-97ab-41d8-831f-9c6c96be8449`
- **参数名**: `IoHwAbInvalidValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [-32768..32767]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This field contains the initial value of a type "sint16".

####### 9. IoHwAbInvalidValueSint32

**容器属性**:

- **UUID**: `e491e955-5ee9-4f76-8b97-ce3df8a76bb3`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IoHwAbInvalidValueSint32`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container for configuring an invalid value of a type "sint32".

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. IoHwAbInvalidValue

- **UUID**: `5216a15f-52b0-4be2-91b5-e2fc593c86d2`
- **参数名**: `IoHwAbInvalidValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [-2147483648..2147483647]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This field contains the initial value of a type "sint32".

####### 10. IoHwAbInvalidValueType

**容器属性**:

- **UUID**: `289ed971-2914-4549-8220-d6145f506b72`
- **容器类型**: CHOICE-CONTAINER
- **容器名称**: `IoHwAbInvalidValueType`
- **多重性**: [1..1]
- **构建后可变**: false

**容器选择**:

- **IoHwAbInvalidValueBoolean**
  - UUID: `fbc4e248-f3c8-4bc8-bbd2-bfb6677b5882`
  - 描述: Container for configuring an invalid value of a type "boolean".
- **IoHwAbInvalidValueFloat32**
  - UUID: `2f2e9da1-4c91-46a2-a9d5-d4efeae48c26`
  - 描述: Container for configuring an invalid value of a type "float32".
- **IoHwAbInvalidValueFloat64**
  - UUID: `e9b907e5-22e6-4ce2-9f2a-6adebe0d3ce5`
  - 描述: Container for configuring an invalid value of a type "float64".
- **IoHwAbInvalidValueUint8**
  - UUID: `f465b96c-d804-4e17-a5ff-ad10d1057eee`
  - 描述: Container for configuring an invalid value of a type "uint8".
- **IoHwAbInvalidValueUint16**
  - UUID: `1f4065c4-b767-4ba2-afe4-c34ac1d97539`
  - 描述: Container for configuring an invalid value of a type "uint16".
- **IoHwAbInvalidValueUint32**
  - UUID: `2cfbeb44-2968-420f-915f-e456f924f21f`
  - 描述: Container for configuring an invalid value of a type "uint32".
- **IoHwAbInvalidValueSint8**
  - UUID: `7f46cafe-67b7-498a-b02e-33d259394573`
  - 描述: Container for configuring an invalid value of a type "sint8".
- **IoHwAbInvalidValueSint16**
  - UUID: `180d975a-2f07-4a24-981f-fd72bc383eb3`
  - 描述: Container for configuring an invalid value of a type "sint16".
- **IoHwAbInvalidValueSint32**
  - UUID: `e491e955-5ee9-4f76-8b97-ce3df8a76bb3`
  - 描述: Container for configuring an invalid value of a type "sint32".

**容器描述**:

This choice container is used for instantiating the appropriate type for the invalid value of the referenced data element.

Example: If the type of the referenced base data type is either an "uint8" or a type reference of an "uint8", the container "IoHwAbInvalidValueUint8" shall be chosen.

##### 6. IoHwAbInvalidValueBoolean

**容器属性**:

- **UUID**: `fbc4e248-f3c8-4bc8-bbd2-bfb6677b5882`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IoHwAbInvalidValueBoolean`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container for configuring an invalid value of a type "boolean".

###### 参数配置

此容器包含 **1** 个参数：

####### BOOLEAN 类型参数

######## 1. IoHwAbInvalidValue

- **UUID**: `359e7e9b-bd3d-4c1d-b8df-a0b34939f158`
- **参数名**: `IoHwAbInvalidValue`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This field contains the initial value of a type "boolean".

##### 7. IoHwAbInvalidValueFloat32

**容器属性**:

- **UUID**: `2f2e9da1-4c91-46a2-a9d5-d4efeae48c26`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IoHwAbInvalidValueFloat32`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container for configuring an invalid value of a type "float32".

###### 参数配置

此容器包含 **1** 个参数：

####### FLOAT 类型参数

######## 1. IoHwAbInvalidValue

- **UUID**: `d1e30bf3-35b3-41d7-bdda-eb28b3ec0419`
- **参数名**: `IoHwAbInvalidValue`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This field contains the initial value of a type "float32".

##### 8. IoHwAbInvalidValueFloat64

**容器属性**:

- **UUID**: `e9b907e5-22e6-4ce2-9f2a-6adebe0d3ce5`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IoHwAbInvalidValueFloat64`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container for configuring an invalid value of a type "float64".

###### 参数配置

此容器包含 **1** 个参数：

####### FLOAT 类型参数

######## 1. IoHwAbInvalidValue

- **UUID**: `f815ed02-2ff3-4495-aabf-26014c7ad01f`
- **参数名**: `IoHwAbInvalidValue`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This field contains the initial value of a type "float64".

##### 9. IoHwAbInvalidValueUint8

**容器属性**:

- **UUID**: `f465b96c-d804-4e17-a5ff-ad10d1057eee`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IoHwAbInvalidValueUint8`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container for configuring an invalid value of a type "uint8".

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. IoHwAbInvalidValue

- **UUID**: `f1411f40-dceb-4ec6-97c7-4776f921515a`
- **参数名**: `IoHwAbInvalidValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This field contains the initial value of a type "uint8".

##### 10. IoHwAbInvalidValueUint16

**容器属性**:

- **UUID**: `1f4065c4-b767-4ba2-afe4-c34ac1d97539`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IoHwAbInvalidValueUint16`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container for configuring an invalid value of a type "uint16".

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. IoHwAbInvalidValue

- **UUID**: `76ea2c11-a275-4ff5-9ed1-e2f81e3739b8`
- **参数名**: `IoHwAbInvalidValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This field contains the initial value of a type "uint16".

##### 11. IoHwAbInvalidValueUint32

**容器属性**:

- **UUID**: `2cfbeb44-2968-420f-915f-e456f924f21f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IoHwAbInvalidValueUint32`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container for configuring an invalid value of a type "uint32".

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. IoHwAbInvalidValue

- **UUID**: `41a8d144-1c90-4172-8612-17fd061a8e44`
- **参数名**: `IoHwAbInvalidValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This field contains the initial value of a type "uint32".

##### 12. IoHwAbInvalidValueSint8

**容器属性**:

- **UUID**: `7f46cafe-67b7-498a-b02e-33d259394573`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IoHwAbInvalidValueSint8`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container for configuring an invalid value of a type "sint8".

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. IoHwAbInvalidValue

- **UUID**: `6993ab73-5d35-46ca-86b2-88b5812ca176`
- **参数名**: `IoHwAbInvalidValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [-128..127]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This field contains the initial value of a type "sint8".

##### 13. IoHwAbInvalidValueSint16

**容器属性**:

- **UUID**: `180d975a-2f07-4a24-981f-fd72bc383eb3`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IoHwAbInvalidValueSint16`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container for configuring an invalid value of a type "sint16".

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. IoHwAbInvalidValue

- **UUID**: `f05ebe07-97ab-41d8-831f-9c6c96be8449`
- **参数名**: `IoHwAbInvalidValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [-32768..32767]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This field contains the initial value of a type "sint16".

##### 14. IoHwAbInvalidValueSint32

**容器属性**:

- **UUID**: `e491e955-5ee9-4f76-8b97-ce3df8a76bb3`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IoHwAbInvalidValueSint32`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container for configuring an invalid value of a type "sint32".

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. IoHwAbInvalidValue

- **UUID**: `5216a15f-52b0-4be2-91b5-e2fc593c86d2`
- **参数名**: `IoHwAbInvalidValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [-2147483648..2147483647]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This field contains the initial value of a type "sint32".

##### 15. IoHwAbArray

**容器属性**:

- **UUID**: `1d9571d0-22d2-47a2-af79-82de8f7c0667`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IoHwAbArray`
- **多重性**: [0..infinite]
- **构建后可变**: false

**容器描述**:

Container for configuring an array type. An array type is the typedef of an array containing n data elements of a base type or a type reference, i.e. the generated files (e.g. Rte_Type.h) will contain a typedef like the following example:

typedef uint8 AlternatorPower_au8[13];

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. IoHwAbArraySize

- **UUID**: `a5f4d81e-a052-40be-9dd0-aacac5846259`
- **参数名**: `IoHwAbArraySize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `5`
- **取值范围**: [0..18446744073709551615]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Parameter for the configuration of the array size, i.e. the number of elements of the selected datatype.

###### 引用关系

此容器包含 **1** 个引用：

####### CHOICE-REFERENCE 类型引用

######## 1. IoHwAbArrayTypeRef

- **UUID**: `483e268d-4de7-4ebe-a5e3-1e4c9bb0abdc`
- **引用名**: `IoHwAbArrayTypeRef`
- **引用类型**: CHOICE-REFERENCE
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **需要索引**: false
- **目标引用列表**:
  - `/MICROSAR/IoHwAb/IoHwAbDatatypes/IoHwAbBaseType`
  - `/MICROSAR/IoHwAb/IoHwAbDatatypes/IoHwAbImplementationTypes/IoHwAbTypeReference`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Parameter for the selection of the datatype of the array elements.

##### 16. IoHwAbRecord

**容器属性**:

- **UUID**: `2dc30056-499e-44bf-92b4-13e8b9147b2d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IoHwAbRecord`
- **多重性**: [0..infinite]
- **构建后可变**: false

**容器描述**:

Container for configuring a record/struct type. An record type is the typedef of a struct containing data elements of a base type or a type reference, i.e. the generated files (e.g. Rte_Type.h) will contain a typedef like the following example:

typedef struct
{
    uint16 Period;
    uint16 ActiveTime;
}DutyCycle;

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. IoHwAbRecordElement

**容器属性**:

- **UUID**: `fb24fab4-1b14-4d65-ba77-b58f2f2acabb`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IoHwAbRecordElement`
- **多重性**: [1..infinite]
- **构建后可变**: false

**容器描述**:

Container for configuring a record/struct element.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. IoHwAbRecordElementPosition

- **UUID**: `274130e5-6acd-425a-95be-33c8df98940c`
- **参数名**: `IoHwAbRecordElementPosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..255]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter contains the position of the of the record element inside the record.

######## 引用关系

此容器包含 **1** 个引用：

######### CHOICE-REFERENCE 类型引用

########## 1. IoHwAbRecordElementTypeRef

- **UUID**: `b21ae229-f1b5-431e-a04f-9a9233f48f86`
- **引用名**: `IoHwAbRecordElementTypeRef`
- **引用类型**: CHOICE-REFERENCE
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **需要索引**: false
- **目标引用列表**:
  - `/MICROSAR/IoHwAb/IoHwAbDatatypes/IoHwAbBaseType`
  - `/MICROSAR/IoHwAb/IoHwAbDatatypes/IoHwAbImplementationTypes/IoHwAbTypeReference`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Parameter for the selection of the datatype of the struct/record elements.

##### 17. IoHwAbRecordElement

**容器属性**:

- **UUID**: `fb24fab4-1b14-4d65-ba77-b58f2f2acabb`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IoHwAbRecordElement`
- **多重性**: [1..infinite]
- **构建后可变**: false

**容器描述**:

Container for configuring a record/struct element.

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. IoHwAbRecordElementPosition

- **UUID**: `274130e5-6acd-425a-95be-33c8df98940c`
- **参数名**: `IoHwAbRecordElementPosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..255]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter contains the position of the of the record element inside the record.

###### 引用关系

此容器包含 **1** 个引用：

####### CHOICE-REFERENCE 类型引用

######## 1. IoHwAbRecordElementTypeRef

- **UUID**: `b21ae229-f1b5-431e-a04f-9a9233f48f86`
- **引用名**: `IoHwAbRecordElementTypeRef`
- **引用类型**: CHOICE-REFERENCE
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **需要索引**: false
- **目标引用列表**:
  - `/MICROSAR/IoHwAb/IoHwAbDatatypes/IoHwAbBaseType`
  - `/MICROSAR/IoHwAb/IoHwAbDatatypes/IoHwAbImplementationTypes/IoHwAbTypeReference`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Parameter for the selection of the datatype of the struct/record elements.

##### 18. IoHwAbBaseType

**容器属性**:

- **UUID**: `6e24768e-f576-48b4-91b8-ea629cba7612`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IoHwAbBaseType`
- **多重性**: [9..9]
- **构建后可变**: false

**容器描述**:

Container for the base data types. These types are a representation of the standard types and cannot be changed.

###### 参数配置

此容器包含 **1** 个参数：

####### ENUMERATION 类型参数

######## 1. IoHwAbBaseDataType

- **UUID**: `eab27640-2d90-45a6-9566-42f3c53956b5`
- **参数名**: `IoHwAbBaseDataType`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `IOHWAB_UINT8`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `IOHWAB_UINT8` (来源: Vector Informatik)
  - `IOHWAB_UINT16` (来源: Vector Informatik)
  - `IOHWAB_UINT32` (来源: Vector Informatik)
  - `IOHWAB_SINT8` (来源: Vector Informatik)
  - `IOHWAB_SINT16` (来源: Vector Informatik)
  - `IOHWAB_SINT32` (来源: Vector Informatik)
  - `IOHWAB_BOOL` (来源: Vector Informatik)
  - `IOHWAB_FLOAT32` (来源: Vector Informatik)
  - `IOHWAB_FLOAT64` (来源: Vector Informatik)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Label for the referenced base type. This type should be used within the user blocks instead of the base type itself.

##### 19. IoHwAbRunnable

**容器属性**:

- **UUID**: `5ec4201a-cdd7-41f6-8b43-ada988f0f110`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IoHwAbRunnable`
- **多重性**: [0..infinite]
- **构建后可变**: false

**容器描述**:

Container for configuring a Runnable Entity that will be generated as
- Runnable into the SWC Description File of the I/O Hardware Abstraction
- Function-body in the C-Source that can be filled with user code
A Runnable Entity is called cyclically by the RTE.

Note: More information on Runnables can be found in the 'Virtual Functional Bus' document.

###### 参数配置

此容器包含 **2** 个参数：

####### INTEGER 类型参数

######## 1. IoHwAbTriggerPeriod

- **UUID**: `c457ed9a-d65a-4193-bbce-3096dfeda07f`
- **参数名**: `IoHwAbTriggerPeriod`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `10`
- **取值范围**: [0..65535]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This field contains the trigger time of the Runnable Entity.

####### ENUMERATION 类型参数

######## 1. IoHwAbTimebase

- **UUID**: `d898b49d-5fb4-4d8b-acd3-bc073bb8e7f3`
- **参数名**: `IoHwAbTimebase`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `IoHwAbMSec`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `IoHwAbSec`
  - `IoHwAbMSec`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This field contains the timebase of the trigger's time.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. IoHwAbPortAccessRef

- **UUID**: `c016fced-0ea0-4783-b22c-f45d24c1700c`
- **引用名**: `IoHwAbPortAccessRef`
- **引用类型**: REFERENCE
- **多重性**: [0..infinite]
- **目标**: `IoHwAbSRPortPrototype`
- **完整路径**: `/MICROSAR/IoHwAb/IoHwAbSRPortPrototype`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter configures the port acces of the runnable. It allows to assign Port Prototypes that shall be accessed by this runnable.

##### 20. IoHwAbSRPortPrototype

**容器属性**:

- **UUID**: `d365689f-9d1d-4824-a468-e78fbcb40261`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IoHwAbSRPortPrototype`
- **多重性**: [0..infinite]
- **构建后可变**: false

**容器描述**:

Container for configuring a Sender/Receiver Port Prototype. This container is the instantiation of a Sender/Receiver Port Interface.

Note: More information on Sender/Receiver Port Interfaces can be found in the 'Virtual Functional Bus' document.

###### 参数配置

此容器包含 **1** 个参数：

####### ENUMERATION 类型参数

######## 1. IoHwAbSRDirection

- **UUID**: `bdd1aefe-01ab-4e20-8869-8c5e27f5af2b`
- **参数名**: `IoHwAbSRDirection`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `IOHWAB_RECEIVER`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `IOHWAB_SENDER` (来源: Vector Informatik)
  - `IOHWAB_RECEIVER` (来源: Vector Informatik)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter configures whether the BSW is the sender (PPort -  provides values of data-elements) or the receiver (RPort - reads/consumes values of data-elements ) of the configured signal.

###### 引用关系

此容器包含 **2** 个引用：

####### REFERENCE 类型引用

######## 1. IoHwAbSRPortInterfaceRef

- **UUID**: `eaa22fc8-fd9d-485f-904c-7ae39d286391`
- **引用名**: `IoHwAbSRPortInterfaceRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `IoHwAbSRPortInterface`
- **完整路径**: `/MICROSAR/IoHwAb/IoHwAbSRPortInterface`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter configures which port prototype to use for this Interface. The selected port prototype will be used to instantiate the interface.

####### CHOICE-REFERENCE 类型引用

######## 1. IoHwAbSRUsedMcalEntity

- **UUID**: `e6a05553-5d1b-4571-b24c-53c6d2ef391c`
- **引用名**: `IoHwAbSRUsedMcalEntity`
- **引用类型**: CHOICE-REFERENCE
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **需要索引**: false
- **目标引用列表**:
  - `/MICROSAR/Dio/DioConfig/DioPort/DioChannel`
  - `/MICROSAR/Dio/DioConfig/DioPort/DioChannelGroup`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter documents which 'MCAL entity' has been used for creating this port prototype.

###### 配置容器

本模块包含 **12** 个配置容器：

####### 1. IoHwAbInitValue

**容器属性**:

- **UUID**: `8db6582c-bc06-4eb8-8dd0-563e00247220`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IoHwAbInitValue`
- **多重性**: [0..infinite]
- **构建后可变**: false

**容器描述**:

Container for configuring initial values of the data elements of the corresponding SR PortInterface.

Note: Only the initial values of BaseTypes and TypeReferences can be configured.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. IoHwAbDataElementRef

- **UUID**: `7a4e75c1-d1c0-49df-9d65-f177763e4e31`
- **引用名**: `IoHwAbDataElementRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `IoHwAbDataElement`
- **完整路径**: `/MICROSAR/IoHwAb/IoHwAbSRPortInterface/IoHwAbDataElement`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter configures which data element to use for this initial value.

######## 配置容器

本模块包含 **11** 个配置容器：

######### 1. IoHwAbInitValueFloat32

**容器属性**:

- **UUID**: `a8285005-84fb-4fa1-ad82-4c5c03b8af40`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IoHwAbInitValueFloat32`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container for configuring an initial value of a type "float32".

########## 参数配置

此容器包含 **1** 个参数：

########### FLOAT 类型参数

############ 1. IoHwAbInitValue

- **UUID**: `9d4f5f7a-16ab-41a5-91c8-6779afcd5ad2`
- **参数名**: `IoHwAbInitValue`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This field contains the initial value of a type "float32".

######### 2. IoHwAbInitValueBoolean

**容器属性**:

- **UUID**: `fcb86599-54a1-487f-a3c8-2a9c70957bc9`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IoHwAbInitValueBoolean`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container for configuring an initial value of a type "boolean".

########## 参数配置

此容器包含 **1** 个参数：

########### BOOLEAN 类型参数

############ 1. IoHwAbInitValue

- **UUID**: `9c2e78d0-9a1a-4825-aaf3-ba4375e9bc51`
- **参数名**: `IoHwAbInitValue`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This field contains the initial value of a type "boolean".

######### 3. IoHwAbInitValueUint16

**容器属性**:

- **UUID**: `936dd890-b8eb-49fa-9900-e8885d5e3832`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IoHwAbInitValueUint16`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container for configuring an initial value of a type "uint16".

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. IoHwAbInitValue

- **UUID**: `16cebbb4-2319-4f60-b0bc-954ea15cb63d`
- **参数名**: `IoHwAbInitValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This field contains the initial value of a type "uint16".

######### 4. IoHwAbInitValueFloat64

**容器属性**:

- **UUID**: `8555b2fb-0979-4abd-9d54-8fd53d0c850c`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IoHwAbInitValueFloat64`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container for configuring an initial value of a type "float64".

########## 参数配置

此容器包含 **1** 个参数：

########### FLOAT 类型参数

############ 1. IoHwAbInitValue

- **UUID**: `9a6261fb-62e1-425e-975b-1e2bcf834aeb`
- **参数名**: `IoHwAbInitValue`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This field contains the initial value of a type "float64".

######### 5. IoHwAbInitValueUint8

**容器属性**:

- **UUID**: `1119880a-4a2f-4718-a9d6-fd802c63561e`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IoHwAbInitValueUint8`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container for configuring an initial value of a type "uint8".

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. IoHwAbInitValue

- **UUID**: `4b52093e-04ba-4305-8b53-aea8de1c0ae3`
- **参数名**: `IoHwAbInitValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This field contains the initial value of a type "uint8".

######### 6. IoHwAbInitValueUint32

**容器属性**:

- **UUID**: `9bc6d06b-2a32-4048-8696-4d7324c673ea`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IoHwAbInitValueUint32`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container for configuring an initial value of a type "uint32".

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. IoHwAbInitValue

- **UUID**: `83d63733-ca4d-4c79-9cdb-eabe93775002`
- **参数名**: `IoHwAbInitValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This field contains the initial value of a type "uint32".

######### 7. IoHwAbInitValueSint8

**容器属性**:

- **UUID**: `62621b51-84a4-4650-9c7c-7ea14577a64c`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IoHwAbInitValueSint8`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container for configuring an initial value of a type "sint8".

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. IoHwAbInitValue

- **UUID**: `d2fb2e08-9f3d-4212-8f70-9d85244c9993`
- **参数名**: `IoHwAbInitValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [-128..127]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This field contains the initial value of a type "sint8".

######### 8. IoHwAbInitValueSint16

**容器属性**:

- **UUID**: `164c10a8-41a9-42f4-867b-244723f4de2c`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IoHwAbInitValueSint16`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container for configuring an initial value of a type "sint16".

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. IoHwAbInitValue

- **UUID**: `891ae0f4-45d5-4bc6-beba-b565a515da60`
- **参数名**: `IoHwAbInitValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [-32768..32767]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This field contains the initial value of a type "sint16".

######### 9. IoHwAbInitValueSint32

**容器属性**:

- **UUID**: `748090a0-3c47-413b-9db7-a72182bd7a34`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IoHwAbInitValueSint32`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container for configuring an initial value of a type "sint32".

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. IoHwAbInitValue

- **UUID**: `36e9713d-6052-456b-a421-dc7089c7817f`
- **参数名**: `IoHwAbInitValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [-2147483648..2147483647]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This field contains the initial value of a type "sint32".

######### 10. IoHwAbInitValueArrayOrRecord

**容器属性**:

- **UUID**: `b24022d0-634f-490a-8d93-919811dbadc0`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IoHwAbInitValueArrayOrRecord`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container for configuring an initial value of an array or a record.

########## 参数配置

此容器包含 **1** 个参数：

########### STRING 类型参数

############ 1. IoHwAbInitValue

- **UUID**: `8fe83ab0-128a-49f1-ae2e-a91c0444f7b4`
- **参数名**: `IoHwAbInitValue`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **字符串变体**:
  - 默认值: `{}`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This field contains the initial value of an array or a record.

All values ​​should, as usual with the array / struct notation, stand one after the other, separated by a comma within a curly bracket,

Example - array with size 3 and init values 0, 1 and 2: {0,1,2}

######### 11. IoHwAbInitValueType

**容器属性**:

- **UUID**: `9700037c-7c2a-44ef-8610-4377f12d8d84`
- **容器类型**: CHOICE-CONTAINER
- **容器名称**: `IoHwAbInitValueType`
- **多重性**: [1..1]
- **构建后可变**: false

**容器选择**:

- **IoHwAbInitValueFloat32**
  - UUID: `a8285005-84fb-4fa1-ad82-4c5c03b8af40`
  - 描述: Container for configuring an initial value of a type "float32".
- **IoHwAbInitValueBoolean**
  - UUID: `fcb86599-54a1-487f-a3c8-2a9c70957bc9`
  - 描述: Container for configuring an initial value of a type "boolean".
- **IoHwAbInitValueUint16**
  - UUID: `936dd890-b8eb-49fa-9900-e8885d5e3832`
  - 描述: Container for configuring an initial value of a type "uint16".
- **IoHwAbInitValueFloat64**
  - UUID: `8555b2fb-0979-4abd-9d54-8fd53d0c850c`
  - 描述: Container for configuring an initial value of a type "float64".
- **IoHwAbInitValueUint8**
  - UUID: `1119880a-4a2f-4718-a9d6-fd802c63561e`
  - 描述: Container for configuring an initial value of a type "uint8".
- **IoHwAbInitValueUint32**
  - UUID: `9bc6d06b-2a32-4048-8696-4d7324c673ea`
  - 描述: Container for configuring an initial value of a type "uint32".
- **IoHwAbInitValueSint8**
  - UUID: `62621b51-84a4-4650-9c7c-7ea14577a64c`
  - 描述: Container for configuring an initial value of a type "sint8".
- **IoHwAbInitValueSint16**
  - UUID: `164c10a8-41a9-42f4-867b-244723f4de2c`
  - 描述: Container for configuring an initial value of a type "sint16".
- **IoHwAbInitValueSint32**
  - UUID: `748090a0-3c47-413b-9db7-a72182bd7a34`
  - 描述: Container for configuring an initial value of a type "sint32".
- **IoHwAbInitValueArrayOrRecord**
  - UUID: `b24022d0-634f-490a-8d93-919811dbadc0`
  - 描述: Container for configuring an initial value of an array or a record.

**容器描述**:

This choice container is used for instantiating the appropriate type for the initial value of the referenced data element.

Example: If the type of the referenced data element is either an "uint8" or a type reference of an "uint8", the container "IoHwAbInitValueUint8" shall be chosen.

####### 2. IoHwAbInitValueFloat32

**容器属性**:

- **UUID**: `a8285005-84fb-4fa1-ad82-4c5c03b8af40`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IoHwAbInitValueFloat32`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container for configuring an initial value of a type "float32".

######## 参数配置

此容器包含 **1** 个参数：

######### FLOAT 类型参数

########## 1. IoHwAbInitValue

- **UUID**: `9d4f5f7a-16ab-41a5-91c8-6779afcd5ad2`
- **参数名**: `IoHwAbInitValue`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This field contains the initial value of a type "float32".

####### 3. IoHwAbInitValueBoolean

**容器属性**:

- **UUID**: `fcb86599-54a1-487f-a3c8-2a9c70957bc9`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IoHwAbInitValueBoolean`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container for configuring an initial value of a type "boolean".

######## 参数配置

此容器包含 **1** 个参数：

######### BOOLEAN 类型参数

########## 1. IoHwAbInitValue

- **UUID**: `9c2e78d0-9a1a-4825-aaf3-ba4375e9bc51`
- **参数名**: `IoHwAbInitValue`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This field contains the initial value of a type "boolean".

####### 4. IoHwAbInitValueUint16

**容器属性**:

- **UUID**: `936dd890-b8eb-49fa-9900-e8885d5e3832`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IoHwAbInitValueUint16`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container for configuring an initial value of a type "uint16".

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. IoHwAbInitValue

- **UUID**: `16cebbb4-2319-4f60-b0bc-954ea15cb63d`
- **参数名**: `IoHwAbInitValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This field contains the initial value of a type "uint16".

####### 5. IoHwAbInitValueFloat64

**容器属性**:

- **UUID**: `8555b2fb-0979-4abd-9d54-8fd53d0c850c`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IoHwAbInitValueFloat64`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container for configuring an initial value of a type "float64".

######## 参数配置

此容器包含 **1** 个参数：

######### FLOAT 类型参数

########## 1. IoHwAbInitValue

- **UUID**: `9a6261fb-62e1-425e-975b-1e2bcf834aeb`
- **参数名**: `IoHwAbInitValue`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This field contains the initial value of a type "float64".

####### 6. IoHwAbInitValueUint8

**容器属性**:

- **UUID**: `1119880a-4a2f-4718-a9d6-fd802c63561e`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IoHwAbInitValueUint8`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container for configuring an initial value of a type "uint8".

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. IoHwAbInitValue

- **UUID**: `4b52093e-04ba-4305-8b53-aea8de1c0ae3`
- **参数名**: `IoHwAbInitValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This field contains the initial value of a type "uint8".

####### 7. IoHwAbInitValueUint32

**容器属性**:

- **UUID**: `9bc6d06b-2a32-4048-8696-4d7324c673ea`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IoHwAbInitValueUint32`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container for configuring an initial value of a type "uint32".

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. IoHwAbInitValue

- **UUID**: `83d63733-ca4d-4c79-9cdb-eabe93775002`
- **参数名**: `IoHwAbInitValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This field contains the initial value of a type "uint32".

####### 8. IoHwAbInitValueSint8

**容器属性**:

- **UUID**: `62621b51-84a4-4650-9c7c-7ea14577a64c`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IoHwAbInitValueSint8`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container for configuring an initial value of a type "sint8".

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. IoHwAbInitValue

- **UUID**: `d2fb2e08-9f3d-4212-8f70-9d85244c9993`
- **参数名**: `IoHwAbInitValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [-128..127]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This field contains the initial value of a type "sint8".

####### 9. IoHwAbInitValueSint16

**容器属性**:

- **UUID**: `164c10a8-41a9-42f4-867b-244723f4de2c`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IoHwAbInitValueSint16`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container for configuring an initial value of a type "sint16".

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. IoHwAbInitValue

- **UUID**: `891ae0f4-45d5-4bc6-beba-b565a515da60`
- **参数名**: `IoHwAbInitValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [-32768..32767]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This field contains the initial value of a type "sint16".

####### 10. IoHwAbInitValueSint32

**容器属性**:

- **UUID**: `748090a0-3c47-413b-9db7-a72182bd7a34`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IoHwAbInitValueSint32`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container for configuring an initial value of a type "sint32".

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. IoHwAbInitValue

- **UUID**: `36e9713d-6052-456b-a421-dc7089c7817f`
- **参数名**: `IoHwAbInitValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [-2147483648..2147483647]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This field contains the initial value of a type "sint32".

####### 11. IoHwAbInitValueArrayOrRecord

**容器属性**:

- **UUID**: `b24022d0-634f-490a-8d93-919811dbadc0`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IoHwAbInitValueArrayOrRecord`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container for configuring an initial value of an array or a record.

######## 参数配置

此容器包含 **1** 个参数：

######### STRING 类型参数

########## 1. IoHwAbInitValue

- **UUID**: `8fe83ab0-128a-49f1-ae2e-a91c0444f7b4`
- **参数名**: `IoHwAbInitValue`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **字符串变体**:
  - 默认值: `{}`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This field contains the initial value of an array or a record.

All values ​​should, as usual with the array / struct notation, stand one after the other, separated by a comma within a curly bracket,

Example - array with size 3 and init values 0, 1 and 2: {0,1,2}

####### 12. IoHwAbInitValueType

**容器属性**:

- **UUID**: `9700037c-7c2a-44ef-8610-4377f12d8d84`
- **容器类型**: CHOICE-CONTAINER
- **容器名称**: `IoHwAbInitValueType`
- **多重性**: [1..1]
- **构建后可变**: false

**容器选择**:

- **IoHwAbInitValueFloat32**
  - UUID: `a8285005-84fb-4fa1-ad82-4c5c03b8af40`
  - 描述: Container for configuring an initial value of a type "float32".
- **IoHwAbInitValueBoolean**
  - UUID: `fcb86599-54a1-487f-a3c8-2a9c70957bc9`
  - 描述: Container for configuring an initial value of a type "boolean".
- **IoHwAbInitValueUint16**
  - UUID: `936dd890-b8eb-49fa-9900-e8885d5e3832`
  - 描述: Container for configuring an initial value of a type "uint16".
- **IoHwAbInitValueFloat64**
  - UUID: `8555b2fb-0979-4abd-9d54-8fd53d0c850c`
  - 描述: Container for configuring an initial value of a type "float64".
- **IoHwAbInitValueUint8**
  - UUID: `1119880a-4a2f-4718-a9d6-fd802c63561e`
  - 描述: Container for configuring an initial value of a type "uint8".
- **IoHwAbInitValueUint32**
  - UUID: `9bc6d06b-2a32-4048-8696-4d7324c673ea`
  - 描述: Container for configuring an initial value of a type "uint32".
- **IoHwAbInitValueSint8**
  - UUID: `62621b51-84a4-4650-9c7c-7ea14577a64c`
  - 描述: Container for configuring an initial value of a type "sint8".
- **IoHwAbInitValueSint16**
  - UUID: `164c10a8-41a9-42f4-867b-244723f4de2c`
  - 描述: Container for configuring an initial value of a type "sint16".
- **IoHwAbInitValueSint32**
  - UUID: `748090a0-3c47-413b-9db7-a72182bd7a34`
  - 描述: Container for configuring an initial value of a type "sint32".
- **IoHwAbInitValueArrayOrRecord**
  - UUID: `b24022d0-634f-490a-8d93-919811dbadc0`
  - 描述: Container for configuring an initial value of an array or a record.

**容器描述**:

This choice container is used for instantiating the appropriate type for the initial value of the referenced data element.

Example: If the type of the referenced data element is either an "uint8" or a type reference of an "uint8", the container "IoHwAbInitValueUint8" shall be chosen.

##### 21. IoHwAbInitValue

**容器属性**:

- **UUID**: `8db6582c-bc06-4eb8-8dd0-563e00247220`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IoHwAbInitValue`
- **多重性**: [0..infinite]
- **构建后可变**: false

**容器描述**:

Container for configuring initial values of the data elements of the corresponding SR PortInterface.

Note: Only the initial values of BaseTypes and TypeReferences can be configured.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. IoHwAbDataElementRef

- **UUID**: `7a4e75c1-d1c0-49df-9d65-f177763e4e31`
- **引用名**: `IoHwAbDataElementRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `IoHwAbDataElement`
- **完整路径**: `/MICROSAR/IoHwAb/IoHwAbSRPortInterface/IoHwAbDataElement`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter configures which data element to use for this initial value.

###### 配置容器

本模块包含 **11** 个配置容器：

####### 1. IoHwAbInitValueFloat32

**容器属性**:

- **UUID**: `a8285005-84fb-4fa1-ad82-4c5c03b8af40`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IoHwAbInitValueFloat32`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container for configuring an initial value of a type "float32".

######## 参数配置

此容器包含 **1** 个参数：

######### FLOAT 类型参数

########## 1. IoHwAbInitValue

- **UUID**: `9d4f5f7a-16ab-41a5-91c8-6779afcd5ad2`
- **参数名**: `IoHwAbInitValue`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This field contains the initial value of a type "float32".

####### 2. IoHwAbInitValueBoolean

**容器属性**:

- **UUID**: `fcb86599-54a1-487f-a3c8-2a9c70957bc9`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IoHwAbInitValueBoolean`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container for configuring an initial value of a type "boolean".

######## 参数配置

此容器包含 **1** 个参数：

######### BOOLEAN 类型参数

########## 1. IoHwAbInitValue

- **UUID**: `9c2e78d0-9a1a-4825-aaf3-ba4375e9bc51`
- **参数名**: `IoHwAbInitValue`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This field contains the initial value of a type "boolean".

####### 3. IoHwAbInitValueUint16

**容器属性**:

- **UUID**: `936dd890-b8eb-49fa-9900-e8885d5e3832`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IoHwAbInitValueUint16`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container for configuring an initial value of a type "uint16".

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. IoHwAbInitValue

- **UUID**: `16cebbb4-2319-4f60-b0bc-954ea15cb63d`
- **参数名**: `IoHwAbInitValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This field contains the initial value of a type "uint16".

####### 4. IoHwAbInitValueFloat64

**容器属性**:

- **UUID**: `8555b2fb-0979-4abd-9d54-8fd53d0c850c`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IoHwAbInitValueFloat64`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container for configuring an initial value of a type "float64".

######## 参数配置

此容器包含 **1** 个参数：

######### FLOAT 类型参数

########## 1. IoHwAbInitValue

- **UUID**: `9a6261fb-62e1-425e-975b-1e2bcf834aeb`
- **参数名**: `IoHwAbInitValue`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This field contains the initial value of a type "float64".

####### 5. IoHwAbInitValueUint8

**容器属性**:

- **UUID**: `1119880a-4a2f-4718-a9d6-fd802c63561e`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IoHwAbInitValueUint8`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container for configuring an initial value of a type "uint8".

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. IoHwAbInitValue

- **UUID**: `4b52093e-04ba-4305-8b53-aea8de1c0ae3`
- **参数名**: `IoHwAbInitValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This field contains the initial value of a type "uint8".

####### 6. IoHwAbInitValueUint32

**容器属性**:

- **UUID**: `9bc6d06b-2a32-4048-8696-4d7324c673ea`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IoHwAbInitValueUint32`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container for configuring an initial value of a type "uint32".

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. IoHwAbInitValue

- **UUID**: `83d63733-ca4d-4c79-9cdb-eabe93775002`
- **参数名**: `IoHwAbInitValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This field contains the initial value of a type "uint32".

####### 7. IoHwAbInitValueSint8

**容器属性**:

- **UUID**: `62621b51-84a4-4650-9c7c-7ea14577a64c`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IoHwAbInitValueSint8`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container for configuring an initial value of a type "sint8".

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. IoHwAbInitValue

- **UUID**: `d2fb2e08-9f3d-4212-8f70-9d85244c9993`
- **参数名**: `IoHwAbInitValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [-128..127]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This field contains the initial value of a type "sint8".

####### 8. IoHwAbInitValueSint16

**容器属性**:

- **UUID**: `164c10a8-41a9-42f4-867b-244723f4de2c`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IoHwAbInitValueSint16`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container for configuring an initial value of a type "sint16".

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. IoHwAbInitValue

- **UUID**: `891ae0f4-45d5-4bc6-beba-b565a515da60`
- **参数名**: `IoHwAbInitValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [-32768..32767]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This field contains the initial value of a type "sint16".

####### 9. IoHwAbInitValueSint32

**容器属性**:

- **UUID**: `748090a0-3c47-413b-9db7-a72182bd7a34`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IoHwAbInitValueSint32`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container for configuring an initial value of a type "sint32".

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. IoHwAbInitValue

- **UUID**: `36e9713d-6052-456b-a421-dc7089c7817f`
- **参数名**: `IoHwAbInitValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [-2147483648..2147483647]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This field contains the initial value of a type "sint32".

####### 10. IoHwAbInitValueArrayOrRecord

**容器属性**:

- **UUID**: `b24022d0-634f-490a-8d93-919811dbadc0`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IoHwAbInitValueArrayOrRecord`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container for configuring an initial value of an array or a record.

######## 参数配置

此容器包含 **1** 个参数：

######### STRING 类型参数

########## 1. IoHwAbInitValue

- **UUID**: `8fe83ab0-128a-49f1-ae2e-a91c0444f7b4`
- **参数名**: `IoHwAbInitValue`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **字符串变体**:
  - 默认值: `{}`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This field contains the initial value of an array or a record.

All values ​​should, as usual with the array / struct notation, stand one after the other, separated by a comma within a curly bracket,

Example - array with size 3 and init values 0, 1 and 2: {0,1,2}

####### 11. IoHwAbInitValueType

**容器属性**:

- **UUID**: `9700037c-7c2a-44ef-8610-4377f12d8d84`
- **容器类型**: CHOICE-CONTAINER
- **容器名称**: `IoHwAbInitValueType`
- **多重性**: [1..1]
- **构建后可变**: false

**容器选择**:

- **IoHwAbInitValueFloat32**
  - UUID: `a8285005-84fb-4fa1-ad82-4c5c03b8af40`
  - 描述: Container for configuring an initial value of a type "float32".
- **IoHwAbInitValueBoolean**
  - UUID: `fcb86599-54a1-487f-a3c8-2a9c70957bc9`
  - 描述: Container for configuring an initial value of a type "boolean".
- **IoHwAbInitValueUint16**
  - UUID: `936dd890-b8eb-49fa-9900-e8885d5e3832`
  - 描述: Container for configuring an initial value of a type "uint16".
- **IoHwAbInitValueFloat64**
  - UUID: `8555b2fb-0979-4abd-9d54-8fd53d0c850c`
  - 描述: Container for configuring an initial value of a type "float64".
- **IoHwAbInitValueUint8**
  - UUID: `1119880a-4a2f-4718-a9d6-fd802c63561e`
  - 描述: Container for configuring an initial value of a type "uint8".
- **IoHwAbInitValueUint32**
  - UUID: `9bc6d06b-2a32-4048-8696-4d7324c673ea`
  - 描述: Container for configuring an initial value of a type "uint32".
- **IoHwAbInitValueSint8**
  - UUID: `62621b51-84a4-4650-9c7c-7ea14577a64c`
  - 描述: Container for configuring an initial value of a type "sint8".
- **IoHwAbInitValueSint16**
  - UUID: `164c10a8-41a9-42f4-867b-244723f4de2c`
  - 描述: Container for configuring an initial value of a type "sint16".
- **IoHwAbInitValueSint32**
  - UUID: `748090a0-3c47-413b-9db7-a72182bd7a34`
  - 描述: Container for configuring an initial value of a type "sint32".
- **IoHwAbInitValueArrayOrRecord**
  - UUID: `b24022d0-634f-490a-8d93-919811dbadc0`
  - 描述: Container for configuring an initial value of an array or a record.

**容器描述**:

This choice container is used for instantiating the appropriate type for the initial value of the referenced data element.

Example: If the type of the referenced data element is either an "uint8" or a type reference of an "uint8", the container "IoHwAbInitValueUint8" shall be chosen.

##### 22. IoHwAbInitValueFloat32

**容器属性**:

- **UUID**: `a8285005-84fb-4fa1-ad82-4c5c03b8af40`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IoHwAbInitValueFloat32`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container for configuring an initial value of a type "float32".

###### 参数配置

此容器包含 **1** 个参数：

####### FLOAT 类型参数

######## 1. IoHwAbInitValue

- **UUID**: `9d4f5f7a-16ab-41a5-91c8-6779afcd5ad2`
- **参数名**: `IoHwAbInitValue`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This field contains the initial value of a type "float32".

##### 23. IoHwAbInitValueBoolean

**容器属性**:

- **UUID**: `fcb86599-54a1-487f-a3c8-2a9c70957bc9`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IoHwAbInitValueBoolean`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container for configuring an initial value of a type "boolean".

###### 参数配置

此容器包含 **1** 个参数：

####### BOOLEAN 类型参数

######## 1. IoHwAbInitValue

- **UUID**: `9c2e78d0-9a1a-4825-aaf3-ba4375e9bc51`
- **参数名**: `IoHwAbInitValue`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This field contains the initial value of a type "boolean".

##### 24. IoHwAbInitValueUint16

**容器属性**:

- **UUID**: `936dd890-b8eb-49fa-9900-e8885d5e3832`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IoHwAbInitValueUint16`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container for configuring an initial value of a type "uint16".

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. IoHwAbInitValue

- **UUID**: `16cebbb4-2319-4f60-b0bc-954ea15cb63d`
- **参数名**: `IoHwAbInitValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This field contains the initial value of a type "uint16".

##### 25. IoHwAbInitValueFloat64

**容器属性**:

- **UUID**: `8555b2fb-0979-4abd-9d54-8fd53d0c850c`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IoHwAbInitValueFloat64`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container for configuring an initial value of a type "float64".

###### 参数配置

此容器包含 **1** 个参数：

####### FLOAT 类型参数

######## 1. IoHwAbInitValue

- **UUID**: `9a6261fb-62e1-425e-975b-1e2bcf834aeb`
- **参数名**: `IoHwAbInitValue`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This field contains the initial value of a type "float64".

##### 26. IoHwAbInitValueUint8

**容器属性**:

- **UUID**: `1119880a-4a2f-4718-a9d6-fd802c63561e`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IoHwAbInitValueUint8`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container for configuring an initial value of a type "uint8".

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. IoHwAbInitValue

- **UUID**: `4b52093e-04ba-4305-8b53-aea8de1c0ae3`
- **参数名**: `IoHwAbInitValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This field contains the initial value of a type "uint8".

##### 27. IoHwAbInitValueUint32

**容器属性**:

- **UUID**: `9bc6d06b-2a32-4048-8696-4d7324c673ea`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IoHwAbInitValueUint32`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container for configuring an initial value of a type "uint32".

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. IoHwAbInitValue

- **UUID**: `83d63733-ca4d-4c79-9cdb-eabe93775002`
- **参数名**: `IoHwAbInitValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This field contains the initial value of a type "uint32".

##### 28. IoHwAbInitValueSint8

**容器属性**:

- **UUID**: `62621b51-84a4-4650-9c7c-7ea14577a64c`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IoHwAbInitValueSint8`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container for configuring an initial value of a type "sint8".

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. IoHwAbInitValue

- **UUID**: `d2fb2e08-9f3d-4212-8f70-9d85244c9993`
- **参数名**: `IoHwAbInitValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [-128..127]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This field contains the initial value of a type "sint8".

##### 29. IoHwAbInitValueSint16

**容器属性**:

- **UUID**: `164c10a8-41a9-42f4-867b-244723f4de2c`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IoHwAbInitValueSint16`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container for configuring an initial value of a type "sint16".

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. IoHwAbInitValue

- **UUID**: `891ae0f4-45d5-4bc6-beba-b565a515da60`
- **参数名**: `IoHwAbInitValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [-32768..32767]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This field contains the initial value of a type "sint16".

##### 30. IoHwAbInitValueSint32

**容器属性**:

- **UUID**: `748090a0-3c47-413b-9db7-a72182bd7a34`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IoHwAbInitValueSint32`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container for configuring an initial value of a type "sint32".

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. IoHwAbInitValue

- **UUID**: `36e9713d-6052-456b-a421-dc7089c7817f`
- **参数名**: `IoHwAbInitValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [-2147483648..2147483647]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This field contains the initial value of a type "sint32".

##### 31. IoHwAbInitValueArrayOrRecord

**容器属性**:

- **UUID**: `b24022d0-634f-490a-8d93-919811dbadc0`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IoHwAbInitValueArrayOrRecord`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container for configuring an initial value of an array or a record.

###### 参数配置

此容器包含 **1** 个参数：

####### STRING 类型参数

######## 1. IoHwAbInitValue

- **UUID**: `8fe83ab0-128a-49f1-ae2e-a91c0444f7b4`
- **参数名**: `IoHwAbInitValue`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **字符串变体**:
  - 默认值: `{}`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This field contains the initial value of an array or a record.

All values ​​should, as usual with the array / struct notation, stand one after the other, separated by a comma within a curly bracket,

Example - array with size 3 and init values 0, 1 and 2: {0,1,2}

##### 32. IoHwAbCSPortPrototype

**容器属性**:

- **UUID**: `ceb3ce28-a0cd-4c5a-bfb0-85c5081d0ba2`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IoHwAbCSPortPrototype`
- **多重性**: [0..infinite]
- **构建后可变**: false

**容器描述**:

Container for configuring a Client/Server Port Prototype. This container is the instantiation of a Client/Server Port Interface.

Note: More information on Client/Server Port Interfaces can be found in the 'Virtual Functional Bus' document.

###### 参数配置

此容器包含 **1** 个参数：

####### ENUMERATION 类型参数

######## 1. IoHwAbCSDirection

- **UUID**: `0a18fda0-ece9-41e5-96ec-8610932927d7`
- **参数名**: `IoHwAbCSDirection`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `IOHWAB_CLIENT`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `IOHWAB_CLIENT` (来源: Vector Informatik)
  - `IOHWAB_SERVER` (来源: Vector Informatik)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter configures whether the BSW is the Client (RPort -  requires (=uses or invokes) the operations defined in the interface from an AUTOSAR service) or the Server (PPort -  provides (=implements) the operations defined in the interface to an AUTOSAR service) of the configured signal.

Note: Currently, the I/O Hardware Abstraction only supports Server Ports.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. IoHwAbCSPortInterfaceRef

- **UUID**: `c947af3f-9b8b-4556-973e-3ccf8e2cbbc5`
- **引用名**: `IoHwAbCSPortInterfaceRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `IoHwAbCSPortInterface`
- **完整路径**: `/MICROSAR/IoHwAb/IoHwAbCSPortInterface`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter configures which port prototype to use for this Interface. The selected port prototype will be used to instantiate the interface.

##### 33. IoHwAbSRPortInterface

**容器属性**:

- **UUID**: `8c031295-88b9-4f0d-9792-33891c73722f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IoHwAbSRPortInterface`
- **多重性**: [0..infinite]
- **构建后可变**: false

**容器描述**:

Container for configuring a Sender/Receiver Port Interface. This container holds the configuration elements for configuring a Sender/Receiver 'template'-interface. This interface is being instantiated by a Sender/Receiver Port Prototype.

Note: More information on Sender/Receiver Port Interfaces can be found in the 'Virtual Functional Bus' document.

###### 参数配置

此容器包含 **1** 个参数：

####### ENUMERATION 类型参数

######## 1. IoHwAbTemplate

- **UUID**: `8b892425-e407-4474-90cf-045d3983ad99`
- **参数名**: `IoHwAbTemplate`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `IoHwAb_Template_None`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `IoHwAb_Template_None`
  - `IoHwAb_Template_ReadDioChannel`
  - `IoHwAb_Template_WriteDioChannel`
  - `IoHwAb_Template_ReadDioChannelGroup`
  - `IoHwAb_Template_WriteDioChannelGroup`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter documents which 'template' has been used for creating this port interface.

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. IoHwAbDataElement

**容器属性**:

- **UUID**: `354502cd-2c6e-4f26-bdf7-2381ccdec25c`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IoHwAbDataElement`
- **多重性**: [1..infinite]
- **构建后可变**: false

**容器描述**:

This container configures a data element of the Sender/Receiver Interface.

######## 参数配置

此容器包含 **1** 个参数：

######### ENUMERATION 类型参数

########## 1. IoHwAbInvalidationPolicy

- **UUID**: `5bcf54e6-7f60-4c7a-b771-052c6252d2bc`
- **参数名**: `IoHwAbInvalidationPolicy`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `DontInvalidate`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `DontInvalidate` (来源: Vector Informatik)
  - `Keep` (来源: Vector Informatik)
  - `Replace` (来源: Vector Informatik)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter configures whether the sending component can actively invalidate a particular data element or which strategy of handling invalid values is applied on the receiver side.

######## 引用关系

此容器包含 **1** 个引用：

######### CHOICE-REFERENCE 类型引用

########## 1. IoHwAbDataElementTypeRef

- **UUID**: `05363d1d-facc-4c19-b14c-5daedc64ab49`
- **引用名**: `IoHwAbDataElementTypeRef`
- **引用类型**: CHOICE-REFERENCE
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **需要索引**: false
- **目标引用列表**:
  - `/MICROSAR/IoHwAb/IoHwAbDatatypes/IoHwAbBaseType`
  - `/MICROSAR/IoHwAb/IoHwAbDatatypes/IoHwAbImplementationTypes/IoHwAbTypeReference`
  - `/MICROSAR/IoHwAb/IoHwAbDatatypes/IoHwAbImplementationTypes/IoHwAbArray`
  - `/MICROSAR/IoHwAb/IoHwAbDatatypes/IoHwAbImplementationTypes/IoHwAbRecord`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Parameter for the selection of the datatype of the Port Element.

##### 34. IoHwAbDataElement

**容器属性**:

- **UUID**: `354502cd-2c6e-4f26-bdf7-2381ccdec25c`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IoHwAbDataElement`
- **多重性**: [1..infinite]
- **构建后可变**: false

**容器描述**:

This container configures a data element of the Sender/Receiver Interface.

###### 参数配置

此容器包含 **1** 个参数：

####### ENUMERATION 类型参数

######## 1. IoHwAbInvalidationPolicy

- **UUID**: `5bcf54e6-7f60-4c7a-b771-052c6252d2bc`
- **参数名**: `IoHwAbInvalidationPolicy`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `DontInvalidate`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `DontInvalidate` (来源: Vector Informatik)
  - `Keep` (来源: Vector Informatik)
  - `Replace` (来源: Vector Informatik)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter configures whether the sending component can actively invalidate a particular data element or which strategy of handling invalid values is applied on the receiver side.

###### 引用关系

此容器包含 **1** 个引用：

####### CHOICE-REFERENCE 类型引用

######## 1. IoHwAbDataElementTypeRef

- **UUID**: `05363d1d-facc-4c19-b14c-5daedc64ab49`
- **引用名**: `IoHwAbDataElementTypeRef`
- **引用类型**: CHOICE-REFERENCE
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **需要索引**: false
- **目标引用列表**:
  - `/MICROSAR/IoHwAb/IoHwAbDatatypes/IoHwAbBaseType`
  - `/MICROSAR/IoHwAb/IoHwAbDatatypes/IoHwAbImplementationTypes/IoHwAbTypeReference`
  - `/MICROSAR/IoHwAb/IoHwAbDatatypes/IoHwAbImplementationTypes/IoHwAbArray`
  - `/MICROSAR/IoHwAb/IoHwAbDatatypes/IoHwAbImplementationTypes/IoHwAbRecord`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Parameter for the selection of the datatype of the Port Element.

##### 35. IoHwAbCSPortInterface

**容器属性**:

- **UUID**: `ac73fc59-beab-4361-9514-0431f55398fa`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IoHwAbCSPortInterface`
- **多重性**: [0..infinite]
- **构建后可变**: false

**容器描述**:

Container for configuring a Client/Server Port Interface. This container holds the configuration elements for configuring a Client/Server 'template'-interface. This interface is being instantiated by a Client/Server Port Prototype.

Note: More information on Client/Server Port Interfaces can be found in the 'Virtual Functional Bus' document.

###### 参数配置

此容器包含 **1** 个参数：

####### ENUMERATION 类型参数

######## 1. IoHwAbTemplate

- **UUID**: `7a37b53b-fa3b-4ecf-a48a-c21b11b73f31`
- **参数名**: `IoHwAbTemplate`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `IoHwAb_Template_None`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `IoHwAb_Template_None`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Parameter not used.

This parameter documents which 'template' has been used for creating this port interface.

###### 配置容器

本模块包含 **3** 个配置容器：

####### 1. IoHwAbOperation

**容器属性**:

- **UUID**: `7eeea3b4-c9bf-4734-88ee-7c09cf62a5ed`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IoHwAbOperation`
- **多重性**: [1..infinite]
- **构建后可变**: false

**容器描述**:

Container for configuring a Client/Server Port Operation.

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. IoHwAbOperationArgument

**容器属性**:

- **UUID**: `624b49a8-dbda-4a5b-a288-52775efb1e82`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IoHwAbOperationArgument`
- **多重性**: [0..infinite]
- **构建后可变**: false

**容器描述**:

This container contains the configuration of am Operation Element of a Client/Server Operation. This Operation Element will be generated as function parameter in the I/O Hardware Abstraction implementation.

########## 参数配置

此容器包含 **2** 个参数：

########### INTEGER 类型参数

############ 1. IoHwAbOperationArgumentPosition

- **UUID**: `2bc2e939-46cd-4912-8e28-d26edea1c4be`
- **参数名**: `IoHwAbOperationArgumentPosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..255]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter contains the position of the of the operation argument.

########### ENUMERATION 类型参数

############ 1. IoHwAbArgDirection

- **UUID**: `570fcc0a-910b-4052-ba31-89019e80cf9b`
- **参数名**: `IoHwAbArgDirection`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `IOHWAB_IN`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `IOHWAB_IN` (来源: Vector Informatik)
  - `IOHWAB_OUT` (来源: Vector Informatik)
  - `IOHWAB_INOUT` (来源: Vector Informatik)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Direction of the function parameter:
- In: parameter is given by value
- Out/InOut: parameter given 'by reference' (actually, it is given as a pointer to a variable)

########## 引用关系

此容器包含 **1** 个引用：

########### CHOICE-REFERENCE 类型引用

############ 1. IoHwAbArgTypeRef

- **UUID**: `f0a3a0eb-add2-45aa-be42-e02b944e2445`
- **引用名**: `IoHwAbArgTypeRef`
- **引用类型**: CHOICE-REFERENCE
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **需要索引**: false
- **目标引用列表**:
  - `/MICROSAR/IoHwAb/IoHwAbDatatypes/IoHwAbBaseType`
  - `/MICROSAR/IoHwAb/IoHwAbDatatypes/IoHwAbImplementationTypes/IoHwAbTypeReference`
  - `/MICROSAR/IoHwAb/IoHwAbDatatypes/IoHwAbImplementationTypes/IoHwAbArray`
  - `/MICROSAR/IoHwAb/IoHwAbDatatypes/IoHwAbImplementationTypes/IoHwAbRecord`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Parameter for the selection of the datatype of the Operation Element.

####### 2. IoHwAbOperationArgument

**容器属性**:

- **UUID**: `624b49a8-dbda-4a5b-a288-52775efb1e82`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IoHwAbOperationArgument`
- **多重性**: [0..infinite]
- **构建后可变**: false

**容器描述**:

This container contains the configuration of am Operation Element of a Client/Server Operation. This Operation Element will be generated as function parameter in the I/O Hardware Abstraction implementation.

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. IoHwAbOperationArgumentPosition

- **UUID**: `2bc2e939-46cd-4912-8e28-d26edea1c4be`
- **参数名**: `IoHwAbOperationArgumentPosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..255]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter contains the position of the of the operation argument.

######### ENUMERATION 类型参数

########## 1. IoHwAbArgDirection

- **UUID**: `570fcc0a-910b-4052-ba31-89019e80cf9b`
- **参数名**: `IoHwAbArgDirection`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `IOHWAB_IN`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `IOHWAB_IN` (来源: Vector Informatik)
  - `IOHWAB_OUT` (来源: Vector Informatik)
  - `IOHWAB_INOUT` (来源: Vector Informatik)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Direction of the function parameter:
- In: parameter is given by value
- Out/InOut: parameter given 'by reference' (actually, it is given as a pointer to a variable)

######## 引用关系

此容器包含 **1** 个引用：

######### CHOICE-REFERENCE 类型引用

########## 1. IoHwAbArgTypeRef

- **UUID**: `f0a3a0eb-add2-45aa-be42-e02b944e2445`
- **引用名**: `IoHwAbArgTypeRef`
- **引用类型**: CHOICE-REFERENCE
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **需要索引**: false
- **目标引用列表**:
  - `/MICROSAR/IoHwAb/IoHwAbDatatypes/IoHwAbBaseType`
  - `/MICROSAR/IoHwAb/IoHwAbDatatypes/IoHwAbImplementationTypes/IoHwAbTypeReference`
  - `/MICROSAR/IoHwAb/IoHwAbDatatypes/IoHwAbImplementationTypes/IoHwAbArray`
  - `/MICROSAR/IoHwAb/IoHwAbDatatypes/IoHwAbImplementationTypes/IoHwAbRecord`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Parameter for the selection of the datatype of the Operation Element.

####### 3. IoHwAbApplicationError

**容器属性**:

- **UUID**: `aedc34b8-00af-487c-9c20-aa4a02cfad73`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IoHwAbApplicationError`
- **多重性**: [1..infinite]
- **构建后可变**: false

**容器描述**:

This container configures the name an application error, which may be result of a server call via the port interface. The configured application errors are available to all operations declared in this interface.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. IoHwAbErrorCode

- **UUID**: `60dc9161-9994-4546-9e03-4a8331c30b51`
- **参数名**: `IoHwAbErrorCode`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `1`
- **取值范围**: [1..63]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter configures the numeric value of an application error.

##### 36. IoHwAbOperation

**容器属性**:

- **UUID**: `7eeea3b4-c9bf-4734-88ee-7c09cf62a5ed`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IoHwAbOperation`
- **多重性**: [1..infinite]
- **构建后可变**: false

**容器描述**:

Container for configuring a Client/Server Port Operation.

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. IoHwAbOperationArgument

**容器属性**:

- **UUID**: `624b49a8-dbda-4a5b-a288-52775efb1e82`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IoHwAbOperationArgument`
- **多重性**: [0..infinite]
- **构建后可变**: false

**容器描述**:

This container contains the configuration of am Operation Element of a Client/Server Operation. This Operation Element will be generated as function parameter in the I/O Hardware Abstraction implementation.

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. IoHwAbOperationArgumentPosition

- **UUID**: `2bc2e939-46cd-4912-8e28-d26edea1c4be`
- **参数名**: `IoHwAbOperationArgumentPosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..255]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter contains the position of the of the operation argument.

######### ENUMERATION 类型参数

########## 1. IoHwAbArgDirection

- **UUID**: `570fcc0a-910b-4052-ba31-89019e80cf9b`
- **参数名**: `IoHwAbArgDirection`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `IOHWAB_IN`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `IOHWAB_IN` (来源: Vector Informatik)
  - `IOHWAB_OUT` (来源: Vector Informatik)
  - `IOHWAB_INOUT` (来源: Vector Informatik)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Direction of the function parameter:
- In: parameter is given by value
- Out/InOut: parameter given 'by reference' (actually, it is given as a pointer to a variable)

######## 引用关系

此容器包含 **1** 个引用：

######### CHOICE-REFERENCE 类型引用

########## 1. IoHwAbArgTypeRef

- **UUID**: `f0a3a0eb-add2-45aa-be42-e02b944e2445`
- **引用名**: `IoHwAbArgTypeRef`
- **引用类型**: CHOICE-REFERENCE
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **需要索引**: false
- **目标引用列表**:
  - `/MICROSAR/IoHwAb/IoHwAbDatatypes/IoHwAbBaseType`
  - `/MICROSAR/IoHwAb/IoHwAbDatatypes/IoHwAbImplementationTypes/IoHwAbTypeReference`
  - `/MICROSAR/IoHwAb/IoHwAbDatatypes/IoHwAbImplementationTypes/IoHwAbArray`
  - `/MICROSAR/IoHwAb/IoHwAbDatatypes/IoHwAbImplementationTypes/IoHwAbRecord`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Parameter for the selection of the datatype of the Operation Element.

##### 37. IoHwAbOperationArgument

**容器属性**:

- **UUID**: `624b49a8-dbda-4a5b-a288-52775efb1e82`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IoHwAbOperationArgument`
- **多重性**: [0..infinite]
- **构建后可变**: false

**容器描述**:

This container contains the configuration of am Operation Element of a Client/Server Operation. This Operation Element will be generated as function parameter in the I/O Hardware Abstraction implementation.

###### 参数配置

此容器包含 **2** 个参数：

####### INTEGER 类型参数

######## 1. IoHwAbOperationArgumentPosition

- **UUID**: `2bc2e939-46cd-4912-8e28-d26edea1c4be`
- **参数名**: `IoHwAbOperationArgumentPosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..255]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter contains the position of the of the operation argument.

####### ENUMERATION 类型参数

######## 1. IoHwAbArgDirection

- **UUID**: `570fcc0a-910b-4052-ba31-89019e80cf9b`
- **参数名**: `IoHwAbArgDirection`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `IOHWAB_IN`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `IOHWAB_IN` (来源: Vector Informatik)
  - `IOHWAB_OUT` (来源: Vector Informatik)
  - `IOHWAB_INOUT` (来源: Vector Informatik)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Direction of the function parameter:
- In: parameter is given by value
- Out/InOut: parameter given 'by reference' (actually, it is given as a pointer to a variable)

###### 引用关系

此容器包含 **1** 个引用：

####### CHOICE-REFERENCE 类型引用

######## 1. IoHwAbArgTypeRef

- **UUID**: `f0a3a0eb-add2-45aa-be42-e02b944e2445`
- **引用名**: `IoHwAbArgTypeRef`
- **引用类型**: CHOICE-REFERENCE
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **需要索引**: false
- **目标引用列表**:
  - `/MICROSAR/IoHwAb/IoHwAbDatatypes/IoHwAbBaseType`
  - `/MICROSAR/IoHwAb/IoHwAbDatatypes/IoHwAbImplementationTypes/IoHwAbTypeReference`
  - `/MICROSAR/IoHwAb/IoHwAbDatatypes/IoHwAbImplementationTypes/IoHwAbArray`
  - `/MICROSAR/IoHwAb/IoHwAbDatatypes/IoHwAbImplementationTypes/IoHwAbRecord`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Parameter for the selection of the datatype of the Operation Element.

##### 38. IoHwAbApplicationError

**容器属性**:

- **UUID**: `aedc34b8-00af-487c-9c20-aa4a02cfad73`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IoHwAbApplicationError`
- **多重性**: [1..infinite]
- **构建后可变**: false

**容器描述**:

This container configures the name an application error, which may be result of a server call via the port interface. The configured application errors are available to all operations declared in this interface.

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. IoHwAbErrorCode

- **UUID**: `60dc9161-9994-4546-9e03-4a8331c30b51`
- **参数名**: `IoHwAbErrorCode`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `1`
- **取值范围**: [1..63]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter configures the numeric value of an application error.

##### 39. IoHwAbSchedulable

**容器属性**:

- **UUID**: `a001aaa1-5f22-4721-9c5e-e3f45636102e`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IoHwAbSchedulable`
- **多重性**: [0..infinite]
- **构建后可变**: false

**容器描述**:

Container for configuring a BSW Schedulable Entity that will be generated as
- Schedulable Entity into the Internal Behavior File of the I/O Hardware Abstraction
- Function-body in the C-Source that can be filled with user code
A Runnable Entity is called cyclically by the SchM.

###### 参数配置

此容器包含 **2** 个参数：

####### INTEGER 类型参数

######## 1. IoHwAbBswTriggerPeriod

- **UUID**: `04ef0351-8bf3-4857-9e87-26b21b95add7`
- **参数名**: `IoHwAbBswTriggerPeriod`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `10`
- **取值范围**: [0..65535]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This contains the trigger time of the Schedulable Entity.

####### ENUMERATION 类型参数

######## 1. IoHwAbBswTimebase

- **UUID**: `7235d6af-4934-4c92-ad3c-7ee300a5c2c9`
- **参数名**: `IoHwAbBswTimebase`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `IoHwAbMSec`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `IoHwAbSec`
  - `IoHwAbMSec`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This field contains the timebase of the trigger's time.

##### 40. IoHwAbInvalidValueType

**容器属性**:

- **UUID**: `289ed971-2914-4549-8220-d6145f506b72`
- **容器类型**: CHOICE-CONTAINER
- **容器名称**: `IoHwAbInvalidValueType`
- **多重性**: [1..1]
- **构建后可变**: false

**容器选择**:

- **IoHwAbInvalidValueBoolean**
  - UUID: `fbc4e248-f3c8-4bc8-bbd2-bfb6677b5882`
  - 描述: Container for configuring an invalid value of a type "boolean".
- **IoHwAbInvalidValueFloat32**
  - UUID: `2f2e9da1-4c91-46a2-a9d5-d4efeae48c26`
  - 描述: Container for configuring an invalid value of a type "float32".
- **IoHwAbInvalidValueFloat64**
  - UUID: `e9b907e5-22e6-4ce2-9f2a-6adebe0d3ce5`
  - 描述: Container for configuring an invalid value of a type "float64".
- **IoHwAbInvalidValueUint8**
  - UUID: `f465b96c-d804-4e17-a5ff-ad10d1057eee`
  - 描述: Container for configuring an invalid value of a type "uint8".
- **IoHwAbInvalidValueUint16**
  - UUID: `1f4065c4-b767-4ba2-afe4-c34ac1d97539`
  - 描述: Container for configuring an invalid value of a type "uint16".
- **IoHwAbInvalidValueUint32**
  - UUID: `2cfbeb44-2968-420f-915f-e456f924f21f`
  - 描述: Container for configuring an invalid value of a type "uint32".
- **IoHwAbInvalidValueSint8**
  - UUID: `7f46cafe-67b7-498a-b02e-33d259394573`
  - 描述: Container for configuring an invalid value of a type "sint8".
- **IoHwAbInvalidValueSint16**
  - UUID: `180d975a-2f07-4a24-981f-fd72bc383eb3`
  - 描述: Container for configuring an invalid value of a type "sint16".
- **IoHwAbInvalidValueSint32**
  - UUID: `e491e955-5ee9-4f76-8b97-ce3df8a76bb3`
  - 描述: Container for configuring an invalid value of a type "sint32".

**容器描述**:

This choice container is used for instantiating the appropriate type for the invalid value of the referenced data element.

Example: If the type of the referenced base data type is either an "uint8" or a type reference of an "uint8", the container "IoHwAbInvalidValueUint8" shall be chosen.

##### 41. IoHwAbInitValueType

**容器属性**:

- **UUID**: `9700037c-7c2a-44ef-8610-4377f12d8d84`
- **容器类型**: CHOICE-CONTAINER
- **容器名称**: `IoHwAbInitValueType`
- **多重性**: [1..1]
- **构建后可变**: false

**容器选择**:

- **IoHwAbInitValueFloat32**
  - UUID: `a8285005-84fb-4fa1-ad82-4c5c03b8af40`
  - 描述: Container for configuring an initial value of a type "float32".
- **IoHwAbInitValueBoolean**
  - UUID: `fcb86599-54a1-487f-a3c8-2a9c70957bc9`
  - 描述: Container for configuring an initial value of a type "boolean".
- **IoHwAbInitValueUint16**
  - UUID: `936dd890-b8eb-49fa-9900-e8885d5e3832`
  - 描述: Container for configuring an initial value of a type "uint16".
- **IoHwAbInitValueFloat64**
  - UUID: `8555b2fb-0979-4abd-9d54-8fd53d0c850c`
  - 描述: Container for configuring an initial value of a type "float64".
- **IoHwAbInitValueUint8**
  - UUID: `1119880a-4a2f-4718-a9d6-fd802c63561e`
  - 描述: Container for configuring an initial value of a type "uint8".
- **IoHwAbInitValueUint32**
  - UUID: `9bc6d06b-2a32-4048-8696-4d7324c673ea`
  - 描述: Container for configuring an initial value of a type "uint32".
- **IoHwAbInitValueSint8**
  - UUID: `62621b51-84a4-4650-9c7c-7ea14577a64c`
  - 描述: Container for configuring an initial value of a type "sint8".
- **IoHwAbInitValueSint16**
  - UUID: `164c10a8-41a9-42f4-867b-244723f4de2c`
  - 描述: Container for configuring an initial value of a type "sint16".
- **IoHwAbInitValueSint32**
  - UUID: `748090a0-3c47-413b-9db7-a72182bd7a34`
  - 描述: Container for configuring an initial value of a type "sint32".
- **IoHwAbInitValueArrayOrRecord**
  - UUID: `b24022d0-634f-490a-8d93-919811dbadc0`
  - 描述: Container for configuring an initial value of an array or a record.

**容器描述**:

This choice container is used for instantiating the appropriate type for the initial value of the referenced data element.

Example: If the type of the referenced data element is either an "uint8" or a type reference of an "uint8", the container "IoHwAbInitValueUint8" shall be chosen.

## 📦 包结构

此ARXML文件包含 **1** 个包：

### 1. MICROSAR

- **UUID**: `ff55d029-386d-43a2-b3c2-dfef4c7a5e36`
- **包名称**: `MICROSAR`
- **包含元素数量**: 9

#### 包含的元素

##### ECUC-MODULE-DEF 类型元素

1. **IoHwAb**

##### BSW-IMPLEMENTATION 类型元素

1. **IoHwAb_Impl**

##### ECUC-MODULE-CONFIGURATION-VALUES 类型元素

1. **IoHwAb_Pre**
2. **IoHwAb_Rec**
3. **IoHwAb_Pre_Class2**
4. **IoHwAb_Template_ReadDioChannel**
5. **IoHwAb_Template_WriteDioChannel**
6. **IoHwAb_Template_ReadDioChannelGroup**
7. **IoHwAb_Template_WriteDioChannelGroup**

## ⚡ 实现信息

此ARXML文件包含 **1** 个实现：

### 1. IoHwAb_Impl

- **UUID**: `dfd3cdeb-497b-4a0c-b893-e9035c5817d3`
- **实现名称**: `IoHwAb_Impl`
- **编程语言**: C
- **软件版本**: 3.00.00
- **供应商ID**: 30
- **AUTOSAR版本**: 4.00.03
- **代码生成器**: cMSR

## ⚙️ 配置信息

此ARXML文件包含 **7** 个配置：

### 1. IoHwAb_Pre

- **UUID**: `e67e57c5-97b7-4b78-830b-9b17538ff78a`
- **配置名称**: `IoHwAb_Pre`
- **定义引用**: `/MICROSAR/IoHwAb`

### 2. IoHwAb_Rec

- **UUID**: `5de05a2c-be95-417c-967e-89bfd61ea737`
- **配置名称**: `IoHwAb_Rec`
- **定义引用**: `/MICROSAR/IoHwAb`

### 3. IoHwAb_Pre_Class2

- **UUID**: `8f75d880-099d-4de7-a859-d8c3f4f5dfb3`
- **配置名称**: `IoHwAb_Pre_Class2`
- **定义引用**: `/MICROSAR/IoHwAb`

### 4. IoHwAb_Template_ReadDioChannel

- **UUID**: `1d886999-8483-4010-89ae-d5e09e4e7c70`
- **配置名称**: `IoHwAb_Template_ReadDioChannel`
- **定义引用**: `/MICROSAR/IoHwAb`

### 5. IoHwAb_Template_WriteDioChannel

- **UUID**: `61b062c1-6c4b-44e3-82a9-19af1d2cf0af`
- **配置名称**: `IoHwAb_Template_WriteDioChannel`
- **定义引用**: `/MICROSAR/IoHwAb`

### 6. IoHwAb_Template_ReadDioChannelGroup

- **UUID**: `f5dd085a-658d-4309-988f-7c4db49f01cf`
- **配置名称**: `IoHwAb_Template_ReadDioChannelGroup`
- **定义引用**: `/MICROSAR/IoHwAb`

### 7. IoHwAb_Template_WriteDioChannelGroup

- **UUID**: `9df6eb8f-7358-44da-9902-c2f46c125ce3`
- **配置名称**: `IoHwAb_Template_WriteDioChannelGroup`
- **定义引用**: `/MICROSAR/IoHwAb`
