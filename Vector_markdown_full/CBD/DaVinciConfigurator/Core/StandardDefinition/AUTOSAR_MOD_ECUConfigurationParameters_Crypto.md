# Crypto - 完整配置文档

*此文档由ARXML文件自动生成，采用层次化结构展示*

**生成时间**: 2025-06-16 14:46:11

## 📑 目录

- [📄 文件信息](#-文件信息)
- [🔧 模块定义](#-模块定义)
  - [Crypto](#crypto)
- [📦 包结构](#-包结构)

## 📄 文件信息

### Schema信息
- **Schema位置**: `http://autosar.org/schema/r4.0 AUTOSAR_4-0-3.xsd`
- **命名空间**: `http://autosar.org/schema/r4.0`

## 🔧 模块定义

### 1. Crypto

#### 基本信息

- **UUID**: `ceec5ba5-3454-4344-b0c0-b0c2e4226a62`
- **模块名称**: `Crypto`
- **类别**: `STANDARDIZED_MODULE_DEFINITION`
- **多重性**: [0..infinite]
- **支持的变体**:
  - VARIANT-PRE-COMPILE

#### 模块描述

Configuration of the Crypto (CryptoDriver) module

#### 版本历史

共有 **1** 个版本记录：

##### 1. 版本 4.3.0

- **发布者**: AUTOSAR

*此版本无详细变更记录*

#### 配置容器

本模块包含 **13** 个配置容器：

##### 1. CryptoDriverObjects

**容器属性**:

- **UUID**: `46627603-c42a-4b2f-8f5a-d9b3798dac8f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CryptoDriverObjects`
- **多重性**: [1..1]
- **构建后可变**: false

**容器描述**:

Container for CRYPTO Objects

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. CryptoDriverObject

**容器属性**:

- **UUID**: `f88bb4cf-fab6-43aa-bf2e-94736a1d1809`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CryptoDriverObject`
- **多重性**: [0..infinite]
- **构建后可变**: false

**容器描述**:

Configuration of a CryptoDriverObject

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. CryptoDriverObjectId

- **UUID**: `a43e7bb4-9b3b-43ae-a99a-d94ceffacc6e`
- **参数名**: `CryptoDriverObjectId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Identifier of the Crypto Driver Object. The Crypto Driver Object offers different crypto primitives.

########## 2. CryptoQueueSize

- **UUID**: `fa3e7038-898e-4acb-8830-bec5b30f63eb`
- **参数名**: `CryptoQueueSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Size of the queue in the Crypto Driver. Defines the maximum number of jobs in the Crypto Driver Object queue. If it is set to 0, queueing is disabled in the Crypto Driver Object.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. CryptoPrimitiveRef

- **UUID**: `006e0100-747e-4e15-9ee6-bb939f8eb7b8`
- **引用名**: `CryptoPrimitiveRef`
- **引用类型**: REFERENCE
- **多重性**: [1..infinite]
- **目标**: `CryptoPrimitive`
- **完整路径**: `/AUTOSAR/EcucDefs/Crypto/CryptoPrimitives/CryptoPrimitive`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Refers to primitive in the CRYPTO.

##### 2. CryptoDriverObject

**容器属性**:

- **UUID**: `f88bb4cf-fab6-43aa-bf2e-94736a1d1809`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CryptoDriverObject`
- **多重性**: [0..infinite]
- **构建后可变**: false

**容器描述**:

Configuration of a CryptoDriverObject

###### 参数配置

此容器包含 **2** 个参数：

####### INTEGER 类型参数

######## 1. CryptoDriverObjectId

- **UUID**: `a43e7bb4-9b3b-43ae-a99a-d94ceffacc6e`
- **参数名**: `CryptoDriverObjectId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Identifier of the Crypto Driver Object. The Crypto Driver Object offers different crypto primitives.

######## 2. CryptoQueueSize

- **UUID**: `fa3e7038-898e-4acb-8830-bec5b30f63eb`
- **参数名**: `CryptoQueueSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Size of the queue in the Crypto Driver. Defines the maximum number of jobs in the Crypto Driver Object queue. If it is set to 0, queueing is disabled in the Crypto Driver Object.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. CryptoPrimitiveRef

- **UUID**: `006e0100-747e-4e15-9ee6-bb939f8eb7b8`
- **引用名**: `CryptoPrimitiveRef`
- **引用类型**: REFERENCE
- **多重性**: [1..infinite]
- **目标**: `CryptoPrimitive`
- **完整路径**: `/AUTOSAR/EcucDefs/Crypto/CryptoPrimitives/CryptoPrimitive`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Refers to primitive in the CRYPTO.

##### 3. CryptoGeneral

**容器属性**:

- **UUID**: `d518a7c5-5c63-4c61-aeeb-567b1527f32f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CryptoGeneral`
- **多重性**: [1..1]
- **构建后可变**: false

**容器描述**:

Container for common configuration options

###### 参数配置

此容器包含 **3** 个参数：

####### BOOLEAN 类型参数

######## 1. CryptoDevErrorDetect

- **UUID**: `0c34a019-2063-4a05-8261-6d2bdcb77051`
- **参数名**: `CryptoDevErrorDetect`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Switches the development error detection and notification on or off.

######## 2. CryptoVersionInfoApi

- **UUID**: `0b81eeb2-103b-4ba4-9339-3bb76a33fc68`
- **参数名**: `CryptoVersionInfoApi`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Pre-processor switch to enable and disable availability of the API Crypto_GetVersionInfo().

####### FLOAT 类型参数

######## 1. CryptoMainFunctionPeriod

- **UUID**: `54d6a331-fec3-404c-935c-ea8dca05160c`
- **参数名**: `CryptoMainFunctionPeriod`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **取值范围**: [0..Inf]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies the period of main function Crypto_MainFunction in seconds.

##### 4. CryptoKeyElements

**容器属性**:

- **UUID**: `00cb3b38-a756-48ab-b4c7-8ca790b2b09b`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CryptoKeyElements`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container for Crypto key elements

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. CryptoKeyElement

**容器属性**:

- **UUID**: `09ea947a-1c30-4290-9139-6a31db128cb8`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CryptoKeyElement`
- **多重性**: [1..infinite]
- **构建后可变**: false

**容器描述**:

Configuration of a CryptoKeyElement

######## 参数配置

此容器包含 **7** 个参数：

######### INTEGER 类型参数

########## 1. CryptoKeyElementId

- **UUID**: `f9f6cf44-ea63-4e9e-a890-de07b6212447`
- **参数名**: `CryptoKeyElementId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Identifier of the CRYPTO key element

########## 2. CryptoKeyElementSize

- **UUID**: `28af21ca-4fa5-43bd-b4d8-8747a228995b`
- **参数名**: `CryptoKeyElementSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Maximum Size size of a CRYPTO key element in bytes

######### BOOLEAN 类型参数

########## 1. CryptoKeyElementAllowPartialAccess

- **UUID**: `177b7703-001c-42f9-8781-b3fc57252252`
- **参数名**: `CryptoKeyElementAllowPartialAccess`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enable or disable writing and reading the key element with data smaller than the size of the element.

########## 2. CryptoKeyElementPersist

- **UUID**: `d57a0daa-1e8d-4149-ae7f-82f3914ab1d2`
- **参数名**: `CryptoKeyElementPersist`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enable or disable persisting of the key element in non-volatile storage.

######### STRING 类型参数

########## 1. CryptoKeyElementInitValue

- **UUID**: `182da9d3-6c7f-422a-b5b3-3129bb4210dc`
- **参数名**: `CryptoKeyElementInitValue`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Value which will be used to fill the element during initialisation, when the element is not already initialized.

######### ENUMERATION 类型参数

########## 1. CryptoKeyElementReadAccess

- **UUID**: `4f4d0d82-ee09-4b8c-be05-6b837aa704ee`
- **参数名**: `CryptoKeyElementReadAccess`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_RA_ALLOWED` (来源: AUTOSAR_ECUC)
  - `CRYPTO_RA_DENIED` (来源: AUTOSAR_ECUC)
  - `CRYPTO_RA_ENCRYPTED` (来源: AUTOSAR_ECUC)
  - `CRYPTO_RA_INTERNAL_COPY` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Define the reading access rights of the key element.

########## 2. CryptoKeyElementWriteAccess

- **UUID**: `c490528f-fc48-45f7-a06d-4b6382c18c10`
- **参数名**: `CryptoKeyElementWriteAccess`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_WA_ALLOWED` (来源: AUTOSAR_ECUC)
  - `CRYPTO_WA_DENIED` (来源: AUTOSAR_ECUC)
  - `CRYPTO_WA_ENCRYPTED` (来源: AUTOSAR_ECUC)
  - `CRYPTO_WA_INTERNAL_COPY` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Define the writing access rights of the key element

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. CryptoKeyElementVirtualTargetRef

- **UUID**: `726bbd42-a1e0-4560-b95d-7bed3f53d9d5`
- **引用名**: `CryptoKeyElementVirtualTargetRef`
- **引用类型**: REFERENCE
- **多重性**: [1..infinite]
- **目标**: `CryptoKeyElement`
- **完整路径**: `/AUTOSAR/EcucDefs/Crypto/CryptoKeyElements/CryptoKeyElement`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Refers to a key element which will contain the actual data. If the Reference is configured, the key element will be a virtual key element.

##### 5. CryptoKeyElement

**容器属性**:

- **UUID**: `09ea947a-1c30-4290-9139-6a31db128cb8`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CryptoKeyElement`
- **多重性**: [1..infinite]
- **构建后可变**: false

**容器描述**:

Configuration of a CryptoKeyElement

###### 参数配置

此容器包含 **7** 个参数：

####### INTEGER 类型参数

######## 1. CryptoKeyElementId

- **UUID**: `f9f6cf44-ea63-4e9e-a890-de07b6212447`
- **参数名**: `CryptoKeyElementId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Identifier of the CRYPTO key element

######## 2. CryptoKeyElementSize

- **UUID**: `28af21ca-4fa5-43bd-b4d8-8747a228995b`
- **参数名**: `CryptoKeyElementSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Maximum Size size of a CRYPTO key element in bytes

####### BOOLEAN 类型参数

######## 1. CryptoKeyElementAllowPartialAccess

- **UUID**: `177b7703-001c-42f9-8781-b3fc57252252`
- **参数名**: `CryptoKeyElementAllowPartialAccess`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enable or disable writing and reading the key element with data smaller than the size of the element.

######## 2. CryptoKeyElementPersist

- **UUID**: `d57a0daa-1e8d-4149-ae7f-82f3914ab1d2`
- **参数名**: `CryptoKeyElementPersist`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enable or disable persisting of the key element in non-volatile storage.

####### STRING 类型参数

######## 1. CryptoKeyElementInitValue

- **UUID**: `182da9d3-6c7f-422a-b5b3-3129bb4210dc`
- **参数名**: `CryptoKeyElementInitValue`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Value which will be used to fill the element during initialisation, when the element is not already initialized.

####### ENUMERATION 类型参数

######## 1. CryptoKeyElementReadAccess

- **UUID**: `4f4d0d82-ee09-4b8c-be05-6b837aa704ee`
- **参数名**: `CryptoKeyElementReadAccess`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_RA_ALLOWED` (来源: AUTOSAR_ECUC)
  - `CRYPTO_RA_DENIED` (来源: AUTOSAR_ECUC)
  - `CRYPTO_RA_ENCRYPTED` (来源: AUTOSAR_ECUC)
  - `CRYPTO_RA_INTERNAL_COPY` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Define the reading access rights of the key element.

######## 2. CryptoKeyElementWriteAccess

- **UUID**: `c490528f-fc48-45f7-a06d-4b6382c18c10`
- **参数名**: `CryptoKeyElementWriteAccess`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_WA_ALLOWED` (来源: AUTOSAR_ECUC)
  - `CRYPTO_WA_DENIED` (来源: AUTOSAR_ECUC)
  - `CRYPTO_WA_ENCRYPTED` (来源: AUTOSAR_ECUC)
  - `CRYPTO_WA_INTERNAL_COPY` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Define the writing access rights of the key element

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. CryptoKeyElementVirtualTargetRef

- **UUID**: `726bbd42-a1e0-4560-b95d-7bed3f53d9d5`
- **引用名**: `CryptoKeyElementVirtualTargetRef`
- **引用类型**: REFERENCE
- **多重性**: [1..infinite]
- **目标**: `CryptoKeyElement`
- **完整路径**: `/AUTOSAR/EcucDefs/Crypto/CryptoKeyElements/CryptoKeyElement`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Refers to a key element which will contain the actual data. If the Reference is configured, the key element will be a virtual key element.

##### 6. CryptoKeyTypes

**容器属性**:

- **UUID**: `09bd7817-5fbf-43a1-8234-d0544f49baa2`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CryptoKeyTypes`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container for CRYPTO key types

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. CryptoKeyType

**容器属性**:

- **UUID**: `4ecc48f5-02c6-4913-afe1-cfe9240dd7d4`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CryptoKeyType`
- **多重性**: [1..infinite]
- **构建后可变**: false

**容器描述**:

Configuration of a CryptoKeyType

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. CryptoKeyElementRef

- **UUID**: `dee3ef55-ecfd-45da-966b-5910d44537da`
- **引用名**: `CryptoKeyElementRef`
- **引用类型**: REFERENCE
- **多重性**: [1..infinite]
- **目标**: `CryptoKeyElement`
- **完整路径**: `/AUTOSAR/EcucDefs/Crypto/CryptoKeyElements/CryptoKeyElement`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Refers to a pointer in the Crypto Key Element, which holds the data of the crypto key element.

##### 7. CryptoKeyType

**容器属性**:

- **UUID**: `4ecc48f5-02c6-4913-afe1-cfe9240dd7d4`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CryptoKeyType`
- **多重性**: [1..infinite]
- **构建后可变**: false

**容器描述**:

Configuration of a CryptoKeyType

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. CryptoKeyElementRef

- **UUID**: `dee3ef55-ecfd-45da-966b-5910d44537da`
- **引用名**: `CryptoKeyElementRef`
- **引用类型**: REFERENCE
- **多重性**: [1..infinite]
- **目标**: `CryptoKeyElement`
- **完整路径**: `/AUTOSAR/EcucDefs/Crypto/CryptoKeyElements/CryptoKeyElement`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Refers to a pointer in the Crypto Key Element, which holds the data of the crypto key element.

##### 8. CryptoKeys

**容器属性**:

- **UUID**: `d30352cc-ffd3-4f28-9d5f-22cdf84dba18`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CryptoKeys`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container for CRYPTO keys

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. CryptoKey

**容器属性**:

- **UUID**: `ce145c84-e16f-48bc-9d43-d73fb8b11bf1`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CryptoKey`
- **多重性**: [1..infinite]
- **构建后可变**: false

**容器描述**:

Configuration of a CryptoKey

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. CryptoKeyDeriveIterations

- **UUID**: `5ddd775a-2553-4500-acd2-9a8618cfe797`
- **参数名**: `CryptoKeyDeriveIterations`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Holds the number of iterations to be performed by the key derivation primitive

########## 2. CryptoKeyId

- **UUID**: `112fdeb4-f3c0-4b93-9138-59fa75e74ed4`
- **参数名**: `CryptoKeyId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Identifier of the CRYPTO Key

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. CryptoKeyTypeRef

- **UUID**: `90c03c62-9c50-47de-993a-487a7e12692b`
- **引用名**: `CryptoKeyTypeRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `CryptoKeyType`
- **完整路径**: `/AUTOSAR/EcucDefs/Crypto/CryptoKeyTypes/CryptoKeyType`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Refers to a pointer in the CRYPTOto a CryptoKeyType. The CryptoKeyType provides the information which key elements are contained in a CryptoKey.

##### 9. CryptoKey

**容器属性**:

- **UUID**: `ce145c84-e16f-48bc-9d43-d73fb8b11bf1`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CryptoKey`
- **多重性**: [1..infinite]
- **构建后可变**: false

**容器描述**:

Configuration of a CryptoKey

###### 参数配置

此容器包含 **2** 个参数：

####### INTEGER 类型参数

######## 1. CryptoKeyDeriveIterations

- **UUID**: `5ddd775a-2553-4500-acd2-9a8618cfe797`
- **参数名**: `CryptoKeyDeriveIterations`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Holds the number of iterations to be performed by the key derivation primitive

######## 2. CryptoKeyId

- **UUID**: `112fdeb4-f3c0-4b93-9138-59fa75e74ed4`
- **参数名**: `CryptoKeyId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Identifier of the CRYPTO Key

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. CryptoKeyTypeRef

- **UUID**: `90c03c62-9c50-47de-993a-487a7e12692b`
- **引用名**: `CryptoKeyTypeRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `CryptoKeyType`
- **完整路径**: `/AUTOSAR/EcucDefs/Crypto/CryptoKeyTypes/CryptoKeyType`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Refers to a pointer in the CRYPTOto a CryptoKeyType. The CryptoKeyType provides the information which key elements are contained in a CryptoKey.

##### 10. CryptoPrimitives

**容器属性**:

- **UUID**: `897bb70e-e4f0-4485-b4dc-a42bc42c79d5`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CryptoPrimitives`
- **多重性**: [0..infinite]
- **构建后可变**: false

**容器描述**:

Container for CRYPTO primitives

###### 配置容器

本模块包含 **3** 个配置容器：

####### 1. CryptoPrimitive

**容器属性**:

- **UUID**: `e00b68c0-11b3-479c-b32e-7102f06910e9`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CryptoPrimitive`
- **多重性**: [0..infinite]
- **构建后可变**: false

**容器描述**:

Configuration of a CryptoPrimitive

######## 参数配置

此容器包含 **4** 个参数：

######### ENUMERATION 类型参数

########## 1. CryptoPrimitiveAlgorithmFamily

- **UUID**: `b2f80e71-603a-4172-a29e-48d43120076e`
- **参数名**: `CryptoPrimitiveAlgorithmFamily`
- **数据类型**: ENUMERATION
- **多重性**: [1..infinite]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_3DES` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_AES` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_BLAKE_1_256` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_BLAKE_1_512` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_BLAKE_2s_256` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_BLAKE_2s_512` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_BRAINPOOL` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_CHACHA` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_ECCNIST` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_ECIES` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_ED25519` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_NOT_SET` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_RIPEMD160` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_RNG` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_RSA` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SECURECOUNTER` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA1` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA2_224` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA2_256` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA2_384` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA2_512` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA2_512_224` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA2_512_256` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA3_224` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA3_256` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA3_384` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA3_512` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHAKE128` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHAKE256` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SIPHASH` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Determines the algorithm family used for the crypto service

########## 2. CryptoPrimitiveAlgorithmMode

- **UUID**: `c8190d8c-9e7d-48ba-a877-c1037a3ac7ce`
- **参数名**: `CryptoPrimitiveAlgorithmMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..infinite]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOMODE_12ROUNDS` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_20ROUNDS` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_8ROUNDS` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_CBC` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_CFB` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_CMAC` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_CTR` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_CTRDRBG` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_ECB` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_GCM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_GMAC` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_HMAC` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_NOT_SET` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_OFB` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_RSAES_OAEP` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_RSAES_PKCS1_v1_5` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_RSASSA_PKCS1_v1_5` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_RSASSA_PSS` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_XTS` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Determines the algorithm mode used for the crypto service

########## 3. CryptoPrimitiveAlgorithmSecondaryFamily

- **UUID**: `a654242f-c7cf-4a54-b055-6bf9a4601bbf`
- **参数名**: `CryptoPrimitiveAlgorithmSecondaryFamily`
- **数据类型**: ENUMERATION
- **多重性**: [1..infinite]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_3DES` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_AES` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_BLAKE_1_256` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_BLAKE_1_512` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_BLAKE_2s_256` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_BLAKE_2s_512` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_BRAINPOOL` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_CHACHA` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_ECCNIST` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_ECIES` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_ED25519` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_NOT_SET` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_RIPEMD160` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_RNG` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_RSA` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SECURECOUNTER` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA1` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA2_224` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA2_256` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA2_384` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA2_512` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA2_512_224` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA2_512_256` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA3_224` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA3_256` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA3_384` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA3_512` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHAKE128` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHAKE256` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SIPHASH` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Determines the algorithm secondary family used for the crypto service

########## 4. CryptoPrimitiveService

- **UUID**: `2c83056d-194e-42e2-b919-470fec0bede0`
- **参数名**: `CryptoPrimitiveService`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `AEAD_DECRYPT` (来源: AUTOSAR_ECUC)
  - `AEAD_ENCRYPT` (来源: AUTOSAR_ECUC)
  - `DECRYPT` (来源: AUTOSAR_ECUC)
  - `ENCRYPT` (来源: AUTOSAR_ECUC)
  - `HASH` (来源: AUTOSAR_ECUC)
  - `MAC_GENERATE` (来源: AUTOSAR_ECUC)
  - `MAC_VERIFY` (来源: AUTOSAR_ECUC)
  - `RANDOM` (来源: AUTOSAR_ECUC)
  - `SIGNATURE_GENERATE` (来源: AUTOSAR_ECUC)
  - `SIGNATURE_VERIFY` (来源: AUTOSAR_ECUC)
  - `SECCOUNTER_READ` (来源: AUTOSAR_ECUC)
  - `SECCOUNTER_INCREMENT` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Determines the crypto service used for defining the capabilities

####### 2. CryptoPrimitiveAlgorithmFamilyCustom

**容器属性**:

- **UUID**: `80782b84-f80a-4ed3-a26d-c8d671b7954e`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CryptoPrimitiveAlgorithmFamilyCustom`
- **多重性**: [0..infinite]
- **构建后可变**: false

**容器描述**:

Container of custom algorithm family values.
The container name serves as a symbolic name for the identifier of the custom algorithm family type.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. CryptoPrimitiveAlgorithmFamilyCustomId

- **UUID**: `685657df-0ddb-4dee-894d-a4dc6ba47043`
- **参数名**: `CryptoPrimitiveAlgorithmFamilyCustomId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [128..254]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The custom value of this algorithm family

####### 3. CryptoPrimitiveAlgorithmModeCustom

**容器属性**:

- **UUID**: `09dc7e1b-b0f8-489a-9b5c-a2a6af89060c`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CryptoPrimitiveAlgorithmModeCustom`
- **多重性**: [0..infinite]
- **构建后可变**: false

**容器描述**:

Container of custom algorithm family values. 
The container name serves as a symbolic name for the identifier of the custom algorithm mode type.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. CryptoPrimitiveAlgorithmModeCustomId

- **UUID**: `2f9c2e55-7a2a-4275-8349-953e2bbdfe30`
- **参数名**: `CryptoPrimitiveAlgorithmModeCustomId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [128..254]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The custom value of this algorithm mode

##### 11. CryptoPrimitive

**容器属性**:

- **UUID**: `e00b68c0-11b3-479c-b32e-7102f06910e9`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CryptoPrimitive`
- **多重性**: [0..infinite]
- **构建后可变**: false

**容器描述**:

Configuration of a CryptoPrimitive

###### 参数配置

此容器包含 **4** 个参数：

####### ENUMERATION 类型参数

######## 1. CryptoPrimitiveAlgorithmFamily

- **UUID**: `b2f80e71-603a-4172-a29e-48d43120076e`
- **参数名**: `CryptoPrimitiveAlgorithmFamily`
- **数据类型**: ENUMERATION
- **多重性**: [1..infinite]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_3DES` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_AES` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_BLAKE_1_256` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_BLAKE_1_512` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_BLAKE_2s_256` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_BLAKE_2s_512` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_BRAINPOOL` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_CHACHA` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_ECCNIST` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_ECIES` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_ED25519` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_NOT_SET` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_RIPEMD160` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_RNG` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_RSA` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SECURECOUNTER` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA1` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA2_224` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA2_256` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA2_384` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA2_512` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA2_512_224` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA2_512_256` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA3_224` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA3_256` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA3_384` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA3_512` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHAKE128` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHAKE256` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SIPHASH` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Determines the algorithm family used for the crypto service

######## 2. CryptoPrimitiveAlgorithmMode

- **UUID**: `c8190d8c-9e7d-48ba-a877-c1037a3ac7ce`
- **参数名**: `CryptoPrimitiveAlgorithmMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..infinite]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOMODE_12ROUNDS` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_20ROUNDS` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_8ROUNDS` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_CBC` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_CFB` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_CMAC` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_CTR` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_CTRDRBG` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_ECB` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_GCM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_GMAC` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_HMAC` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_NOT_SET` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_OFB` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_RSAES_OAEP` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_RSAES_PKCS1_v1_5` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_RSASSA_PKCS1_v1_5` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_RSASSA_PSS` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_XTS` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Determines the algorithm mode used for the crypto service

######## 3. CryptoPrimitiveAlgorithmSecondaryFamily

- **UUID**: `a654242f-c7cf-4a54-b055-6bf9a4601bbf`
- **参数名**: `CryptoPrimitiveAlgorithmSecondaryFamily`
- **数据类型**: ENUMERATION
- **多重性**: [1..infinite]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_3DES` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_AES` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_BLAKE_1_256` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_BLAKE_1_512` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_BLAKE_2s_256` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_BLAKE_2s_512` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_BRAINPOOL` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_CHACHA` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_ECCNIST` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_ECIES` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_ED25519` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_NOT_SET` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_RIPEMD160` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_RNG` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_RSA` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SECURECOUNTER` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA1` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA2_224` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA2_256` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA2_384` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA2_512` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA2_512_224` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA2_512_256` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA3_224` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA3_256` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA3_384` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA3_512` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHAKE128` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHAKE256` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SIPHASH` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Determines the algorithm secondary family used for the crypto service

######## 4. CryptoPrimitiveService

- **UUID**: `2c83056d-194e-42e2-b919-470fec0bede0`
- **参数名**: `CryptoPrimitiveService`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `AEAD_DECRYPT` (来源: AUTOSAR_ECUC)
  - `AEAD_ENCRYPT` (来源: AUTOSAR_ECUC)
  - `DECRYPT` (来源: AUTOSAR_ECUC)
  - `ENCRYPT` (来源: AUTOSAR_ECUC)
  - `HASH` (来源: AUTOSAR_ECUC)
  - `MAC_GENERATE` (来源: AUTOSAR_ECUC)
  - `MAC_VERIFY` (来源: AUTOSAR_ECUC)
  - `RANDOM` (来源: AUTOSAR_ECUC)
  - `SIGNATURE_GENERATE` (来源: AUTOSAR_ECUC)
  - `SIGNATURE_VERIFY` (来源: AUTOSAR_ECUC)
  - `SECCOUNTER_READ` (来源: AUTOSAR_ECUC)
  - `SECCOUNTER_INCREMENT` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Determines the crypto service used for defining the capabilities

##### 12. CryptoPrimitiveAlgorithmFamilyCustom

**容器属性**:

- **UUID**: `80782b84-f80a-4ed3-a26d-c8d671b7954e`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CryptoPrimitiveAlgorithmFamilyCustom`
- **多重性**: [0..infinite]
- **构建后可变**: false

**容器描述**:

Container of custom algorithm family values.
The container name serves as a symbolic name for the identifier of the custom algorithm family type.

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. CryptoPrimitiveAlgorithmFamilyCustomId

- **UUID**: `685657df-0ddb-4dee-894d-a4dc6ba47043`
- **参数名**: `CryptoPrimitiveAlgorithmFamilyCustomId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [128..254]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The custom value of this algorithm family

##### 13. CryptoPrimitiveAlgorithmModeCustom

**容器属性**:

- **UUID**: `09dc7e1b-b0f8-489a-9b5c-a2a6af89060c`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CryptoPrimitiveAlgorithmModeCustom`
- **多重性**: [0..infinite]
- **构建后可变**: false

**容器描述**:

Container of custom algorithm family values. 
The container name serves as a symbolic name for the identifier of the custom algorithm mode type.

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. CryptoPrimitiveAlgorithmModeCustomId

- **UUID**: `2f9c2e55-7a2a-4275-8349-953e2bbdfe30`
- **参数名**: `CryptoPrimitiveAlgorithmModeCustomId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [128..254]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The custom value of this algorithm mode

## 📦 包结构

此ARXML文件包含 **2** 个包：

### 1. AUTOSAR

- **UUID**: `5d7ec4af-f860-4a81-95b3-79440d2f3bef`
- **包名称**: `AUTOSAR`
- **包含元素数量**: 0

### 2. EcucDefs

- **UUID**: `852cb53e-de1a-4483-8dd4-38d8f9f5db16`
- **包名称**: `EcucDefs`
- **包含元素数量**: 1

#### 包含的元素

##### ECUC-MODULE-DEF 类型元素

1. **Crypto**
