# Crypto - 完整配置文档

*此文档由ARXML文件自动生成，采用层次化结构展示*

**生成时间**: 2025-06-16 14:50:59

## 📑 目录

- [📄 文件信息](#-文件信息)
- [🔧 模块定义](#-模块定义)
  - [Crypto](#crypto)
- [📦 包结构](#-包结构)
- [⚡ 实现信息](#-实现信息)

## 📄 文件信息

### Schema信息
- **Schema位置**: `http://autosar.org/schema/r4.0 AUTOSAR_4-0-3.xsd`
- **命名空间**: `http://autosar.org/schema/r4.0`

## 🔧 模块定义

### 1. Crypto

#### 基本信息

- **UUID**: `13af85c9-8ee6-4174-9962-507cad2fcb6e`
- **模块名称**: `Crypto`
- **类别**: `VENDOR_SPECIFIC_MODULE_DEFINITION`
- **多重性**: [0..1]
- **支持的变体**:
  - VARIANT-PRE-COMPILE

#### 模块描述

Crypto Driver for hardware specific functionalities

#### 版本历史

共有 **9** 个版本记录：

##### 1. 版本 1.00.00

- **状态**: released
- **发布日期**: 2018-03-28T09:39:25+02:00
- **发布者**: vistof

**变更内容**:

##### 2. 版本 2.00.00

- **状态**: released
- **发布日期**: 2018-09-27T15:43:08+02:00
- **发布者**: visjhi

**变更内容**:

##### 3. 版本 2.00.02

- **状态**: released
- **发布日期**: 2018-10-26T09:36:48+02:00
- **发布者**: visjhi

**变更内容**:

##### 4. 版本 2.01.00

- **状态**: released
- **发布日期**: 2019-02-11T11:09:31+01:00
- **发布者**: visjhi

**变更内容**:

##### 5. 版本 2.01.01

- **状态**: released
- **发布日期**: 2019-02-25T11:12:13+01:00
- **发布者**: visjhi

**变更内容**:

##### 6. 版本 2.02.00

- **状态**: released
- **发布日期**: 2019-03-20T17:45:12+01:00
- **发布者**: visjhi

**变更内容**:

##### 7. 版本 3.00.00

- **状态**: released
- **发布日期**: 2019-10-14T15:32:34+02:00
- **发布者**: vismhh

**变更内容**:

##### 8. 版本 3.01.00

- **状态**: released
- **发布日期**: 2019-11-22T19:32:58+01:00
- **发布者**: vismhh, visdil

**变更内容**:

##### 9. 版本 3.03.00

- **状态**: released
- **发布日期**: 2020-08-21T11:00:59+02:00
- **发布者**: visdil

**变更内容**:

#### 配置容器

本模块包含 **12** 个配置容器：

##### 1. CryptoDriverObjects

**容器属性**:

- **UUID**: `0e17e3f1-e728-4480-8cb5-d67ef1f666ec`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CryptoDriverObjects`
- **多重性**: [1..1]
- **构建后可变**: false

**容器描述**:

Container for Crypto Driver Objects

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. CryptoDriverObject

**容器属性**:

- **UUID**: `36d23ea6-245a-4a3e-85a1-8b7f9db32fca`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CryptoDriverObject`
- **多重性**: [0..infinite]
- **构建后可变**: false

**容器描述**:

Container for configuration of Crypto Driver Object. The container name 
serves as a symbolic name for the identifier of a Crypto Driver Object.

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. CryptoDriverObjectId

- **UUID**: `3d3238e1-9d79-4196-bb78-0a53c77f19d1`
- **参数名**: `CryptoDriverObjectId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Identifier of the Crypto Driver Object. The Crypto Driver Object offers 
different crypto primitives.

########## 2. CryptoDriverObjectQueueSize

- **UUID**: `84a4e4c9-22a0-4599-9940-0959df1c7ebf`
- **参数名**: `CryptoDriverObjectQueueSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `1`
- **取值范围**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Size of the queue in the Crypto Driver. Defines the maximum number of 
jobs in the Crypto Driver Object queue. If it is set to 0, queueing is disabled 
in the Crypto Driver Object.
This Crypto Driver does not support queuing but uses the buffer for asynchronous processing.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. CryptoPrimitiveRef

- **UUID**: `955aaf42-a4c9-4b55-9074-23736b382a25`
- **引用名**: `CryptoPrimitiveRef`
- **引用类型**: REFERENCE
- **多重性**: [1..infinite]
- **目标**: `CryptoPrimitive`
- **完整路径**: `/MICROSAR/vHsm_Hal/Crypto/CryptoPrimitives/CryptoPrimitive`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Refers to primitive in the CRYPTO. 
The CryptoPrimitive is a pre-configured container of the crypto service that shall be used.

##### 2. CryptoDriverObject

**容器属性**:

- **UUID**: `36d23ea6-245a-4a3e-85a1-8b7f9db32fca`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CryptoDriverObject`
- **多重性**: [0..infinite]
- **构建后可变**: false

**容器描述**:

Container for configuration of Crypto Driver Object. The container name 
serves as a symbolic name for the identifier of a Crypto Driver Object.

###### 参数配置

此容器包含 **2** 个参数：

####### INTEGER 类型参数

######## 1. CryptoDriverObjectId

- **UUID**: `3d3238e1-9d79-4196-bb78-0a53c77f19d1`
- **参数名**: `CryptoDriverObjectId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Identifier of the Crypto Driver Object. The Crypto Driver Object offers 
different crypto primitives.

######## 2. CryptoDriverObjectQueueSize

- **UUID**: `84a4e4c9-22a0-4599-9940-0959df1c7ebf`
- **参数名**: `CryptoDriverObjectQueueSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `1`
- **取值范围**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Size of the queue in the Crypto Driver. Defines the maximum number of 
jobs in the Crypto Driver Object queue. If it is set to 0, queueing is disabled 
in the Crypto Driver Object.
This Crypto Driver does not support queuing but uses the buffer for asynchronous processing.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. CryptoPrimitiveRef

- **UUID**: `955aaf42-a4c9-4b55-9074-23736b382a25`
- **引用名**: `CryptoPrimitiveRef`
- **引用类型**: REFERENCE
- **多重性**: [1..infinite]
- **目标**: `CryptoPrimitive`
- **完整路径**: `/MICROSAR/vHsm_Hal/Crypto/CryptoPrimitives/CryptoPrimitive`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Refers to primitive in the CRYPTO. 
The CryptoPrimitive is a pre-configured container of the crypto service that shall be used.

##### 3. CryptoPrimitives

**容器属性**:

- **UUID**: `fe27842d-c46e-4e06-a843-f8b054622876`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CryptoPrimitives`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container for CRYPTO primitives

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. CryptoPrimitive

**容器属性**:

- **UUID**: `7cff9f20-8611-4ed0-96e9-a99346f6ed4a`
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

- **UUID**: `8e806fe6-a4d9-4562-9d64-e263e4c7e382`
- **参数名**: `CryptoPrimitiveAlgorithmFamily`
- **数据类型**: ENUMERATION
- **多重性**: [1..infinite]
- **默认值**: `CRYPTO_ALGOFAM_NOT_SET`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_NOT_SET`
  - `CRYPTO_ALGOFAM_SHA1`
  - `CRYPTO_ALGOFAM_SHA2_224`
  - `CRYPTO_ALGOFAM_SHA2_256`
  - `CRYPTO_ALGOFAM_SHA2_384`
  - `CRYPTO_ALGOFAM_SHA2_512`
  - `CRYPTO_ALGOFAM_SHA2_512_224`
  - `CRYPTO_ALGOFAM_SHA2_512_256`
  - `CRYPTO_ALGOFAM_SHA3_224`
  - `CRYPTO_ALGOFAM_SHA3_256`
  - `CRYPTO_ALGOFAM_SHA3_384`
  - `CRYPTO_ALGOFAM_SHA3_512`
  - `CRYPTO_ALGOFAM_SHAKE128`
  - `CRYPTO_ALGOFAM_SHAKE256`
  - `CRYPTO_ALGOFAM_RIPEMD160`
  - `CRYPTO_ALGOFAM_BLAKE_1_256`
  - `CRYPTO_ALGOFAM_BLAKE_1_512`
  - `CRYPTO_ALGOFAM_BLAKE_2s_256`
  - `CRYPTO_ALGOFAM_BLAKE_2s_512`
  - `CRYPTO_ALGOFAM_3DES`
  - `CRYPTO_ALGOFAM_AES`
  - `CRYPTO_ALGOFAM_CHACHA`
  - `CRYPTO_ALGOFAM_RSA`
  - `CRYPTO_ALGOFAM_ED25519`
  - `CRYPTO_ALGOFAM_BRAINPOOL`
  - `CRYPTO_ALGOFAM_ECCNIST`
  - `CRYPTO_ALGOFAM_SECURECOUNTER`
  - `CRYPTO_ALGOFAM_RNG`
  - `CRYPTO_ALGOFAM_SIPHASH`
  - `CRYPTO_ALGOFAM_ECIES`
  - `CRYPTO_ALGOFAM_CUSTOM`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Determines the algorithm family used for the crypto service.

########## 2. CryptoPrimitiveAlgorithmMode

- **UUID**: `83a965da-f805-46c3-b157-e1fbe7e57364`
- **参数名**: `CryptoPrimitiveAlgorithmMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..infinite]
- **默认值**: `CRYPTO_ALGOMODE_NOT_SET`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOMODE_NOT_SET`
  - `CRYPTO_ALGOMODE_ECB`
  - `CRYPTO_ALGOMODE_CBC`
  - `CRYPTO_ALGOMODE_CFB`
  - `CRYPTO_ALGOMODE_OFB`
  - `CRYPTO_ALGOMODE_CTR`
  - `CRYPTO_ALGOMODE_GCM`
  - `CRYPTO_ALGOMODE_XTS`
  - `CRYPTO_ALGOMODE_RSAES_OAEP`
  - `CRYPTO_ALGOMODE_RSAES_PKCS1_v1_5`
  - `CRYPTO_ALGOMODE_RSASSA_PSS`
  - `CRYPTO_ALGOMODE_RSASSA_PKCS1_v1_5`
  - `CRYPTO_ALGOMODE_8ROUNDS`
  - `CRYPTO_ALGOMODE_12ROUNDS`
  - `CRYPTO_ALGOMODE_20ROUNDS`
  - `CRYPTO_ALGOMODE_HMAC`
  - `CRYPTO_ALGOMODE_CMAC`
  - `CRYPTO_ALGOMODE_GMAC`
  - `CRYPTO_ALGOMODE_CTRDRBG`
  - `CRYPTO_ALGOMODE_SIPHASH_2_4`
  - `CRYPTO_ALGOMODE_SIPHASH_4_8`
  - `CRYPTO_ALGOMODE_CUSTOM`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Determines the algorithm mode used for the crypto service

########## 3. CryptoPrimitiveService

- **UUID**: `a49dd5e7-3470-4e00-b9ae-875020b528d4`
- **参数名**: `CryptoPrimitiveService`
- **数据类型**: ENUMERATION
- **多重性**: [1..infinite]
- **默认值**: `CRYPTO_MAC_VERIFY`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_MAC_VERIFY`
  - `CRYPTO_MAC_GENERATE`
  - `CRYPTO_SIGNATURE_VERIFY`
  - `CRYPTO_SIGNATURE_GENERATE`
  - `CRYPTO_ENCRYPT`
  - `CRYPTO_DECRYPT`
  - `CRYPTO_AEADENCRYPT`
  - `CRYPTO_AEADDECRYPT`
  - `CRYPTO_HASH`
  - `CRYPTO_RANDOM`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Determines the crypto service used for defining the capabilities

########## 4. CryptoPrimitiveAlgorithmSecondaryFamily

- **UUID**: `2d60b7f8-51ad-48db-b8b7-0f4399954bd5`
- **参数名**: `CryptoPrimitiveAlgorithmSecondaryFamily`
- **数据类型**: ENUMERATION
- **多重性**: [1..infinite]
- **默认值**: `CRYPTO_ALGOFAM_NOT_SET`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_NOT_SET`
  - `CRYPTO_ALGOFAM_SHA1`
  - `CRYPTO_ALGOFAM_SHA2_224`
  - `CRYPTO_ALGOFAM_SHA2_256`
  - `CRYPTO_ALGOFAM_SHA2_384`
  - `CRYPTO_ALGOFAM_SHA2_512`
  - `CRYPTO_ALGOFAM_SHA2_512_224`
  - `CRYPTO_ALGOFAM_SHA2_512_256`
  - `CRYPTO_ALGOFAM_SHA3_224`
  - `CRYPTO_ALGOFAM_SHA3_256`
  - `CRYPTO_ALGOFAM_SHA3_384`
  - `CRYPTO_ALGOFAM_SHA3_512`
  - `CRYPTO_ALGOFAM_SHAKE128`
  - `CRYPTO_ALGOFAM_SHAKE256`
  - `CRYPTO_ALGOFAM_RIPEMD160`
  - `CRYPTO_ALGOFAM_BLAKE_1_256`
  - `CRYPTO_ALGOFAM_BLAKE_1_512`
  - `CRYPTO_ALGOFAM_BLAKE_2s_256`
  - `CRYPTO_ALGOFAM_BLAKE_2s_512`
  - `CRYPTO_ALGOFAM_3DES`
  - `CRYPTO_ALGOFAM_AES`
  - `CRYPTO_ALGOFAM_CHACHA`
  - `CRYPTO_ALGOFAM_RSA`
  - `CRYPTO_ALGOFAM_ED25519`
  - `CRYPTO_ALGOFAM_BRAINPOOL`
  - `CRYPTO_ALGOFAM_ECCNIST`
  - `CRYPTO_ALGOFAM_SECURECOUNTER`
  - `CRYPTO_ALGOFAM_RNG`
  - `CRYPTO_ALGOFAM_SIPHASH`
  - `CRYPTO_ALGOFAM_ECIES`
  - `CRYPTO_ALGOFAM_CUSTOM`
  - `CRYPTO_ALGOFAM_CUSTOM_PADDING_PKCS7`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Determines the algorithm secondary family used for the crypto service

##### 4. CryptoPrimitive

**容器属性**:

- **UUID**: `7cff9f20-8611-4ed0-96e9-a99346f6ed4a`
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

- **UUID**: `8e806fe6-a4d9-4562-9d64-e263e4c7e382`
- **参数名**: `CryptoPrimitiveAlgorithmFamily`
- **数据类型**: ENUMERATION
- **多重性**: [1..infinite]
- **默认值**: `CRYPTO_ALGOFAM_NOT_SET`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_NOT_SET`
  - `CRYPTO_ALGOFAM_SHA1`
  - `CRYPTO_ALGOFAM_SHA2_224`
  - `CRYPTO_ALGOFAM_SHA2_256`
  - `CRYPTO_ALGOFAM_SHA2_384`
  - `CRYPTO_ALGOFAM_SHA2_512`
  - `CRYPTO_ALGOFAM_SHA2_512_224`
  - `CRYPTO_ALGOFAM_SHA2_512_256`
  - `CRYPTO_ALGOFAM_SHA3_224`
  - `CRYPTO_ALGOFAM_SHA3_256`
  - `CRYPTO_ALGOFAM_SHA3_384`
  - `CRYPTO_ALGOFAM_SHA3_512`
  - `CRYPTO_ALGOFAM_SHAKE128`
  - `CRYPTO_ALGOFAM_SHAKE256`
  - `CRYPTO_ALGOFAM_RIPEMD160`
  - `CRYPTO_ALGOFAM_BLAKE_1_256`
  - `CRYPTO_ALGOFAM_BLAKE_1_512`
  - `CRYPTO_ALGOFAM_BLAKE_2s_256`
  - `CRYPTO_ALGOFAM_BLAKE_2s_512`
  - `CRYPTO_ALGOFAM_3DES`
  - `CRYPTO_ALGOFAM_AES`
  - `CRYPTO_ALGOFAM_CHACHA`
  - `CRYPTO_ALGOFAM_RSA`
  - `CRYPTO_ALGOFAM_ED25519`
  - `CRYPTO_ALGOFAM_BRAINPOOL`
  - `CRYPTO_ALGOFAM_ECCNIST`
  - `CRYPTO_ALGOFAM_SECURECOUNTER`
  - `CRYPTO_ALGOFAM_RNG`
  - `CRYPTO_ALGOFAM_SIPHASH`
  - `CRYPTO_ALGOFAM_ECIES`
  - `CRYPTO_ALGOFAM_CUSTOM`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Determines the algorithm family used for the crypto service.

######## 2. CryptoPrimitiveAlgorithmMode

- **UUID**: `83a965da-f805-46c3-b157-e1fbe7e57364`
- **参数名**: `CryptoPrimitiveAlgorithmMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..infinite]
- **默认值**: `CRYPTO_ALGOMODE_NOT_SET`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOMODE_NOT_SET`
  - `CRYPTO_ALGOMODE_ECB`
  - `CRYPTO_ALGOMODE_CBC`
  - `CRYPTO_ALGOMODE_CFB`
  - `CRYPTO_ALGOMODE_OFB`
  - `CRYPTO_ALGOMODE_CTR`
  - `CRYPTO_ALGOMODE_GCM`
  - `CRYPTO_ALGOMODE_XTS`
  - `CRYPTO_ALGOMODE_RSAES_OAEP`
  - `CRYPTO_ALGOMODE_RSAES_PKCS1_v1_5`
  - `CRYPTO_ALGOMODE_RSASSA_PSS`
  - `CRYPTO_ALGOMODE_RSASSA_PKCS1_v1_5`
  - `CRYPTO_ALGOMODE_8ROUNDS`
  - `CRYPTO_ALGOMODE_12ROUNDS`
  - `CRYPTO_ALGOMODE_20ROUNDS`
  - `CRYPTO_ALGOMODE_HMAC`
  - `CRYPTO_ALGOMODE_CMAC`
  - `CRYPTO_ALGOMODE_GMAC`
  - `CRYPTO_ALGOMODE_CTRDRBG`
  - `CRYPTO_ALGOMODE_SIPHASH_2_4`
  - `CRYPTO_ALGOMODE_SIPHASH_4_8`
  - `CRYPTO_ALGOMODE_CUSTOM`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Determines the algorithm mode used for the crypto service

######## 3. CryptoPrimitiveService

- **UUID**: `a49dd5e7-3470-4e00-b9ae-875020b528d4`
- **参数名**: `CryptoPrimitiveService`
- **数据类型**: ENUMERATION
- **多重性**: [1..infinite]
- **默认值**: `CRYPTO_MAC_VERIFY`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_MAC_VERIFY`
  - `CRYPTO_MAC_GENERATE`
  - `CRYPTO_SIGNATURE_VERIFY`
  - `CRYPTO_SIGNATURE_GENERATE`
  - `CRYPTO_ENCRYPT`
  - `CRYPTO_DECRYPT`
  - `CRYPTO_AEADENCRYPT`
  - `CRYPTO_AEADDECRYPT`
  - `CRYPTO_HASH`
  - `CRYPTO_RANDOM`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Determines the crypto service used for defining the capabilities

######## 4. CryptoPrimitiveAlgorithmSecondaryFamily

- **UUID**: `2d60b7f8-51ad-48db-b8b7-0f4399954bd5`
- **参数名**: `CryptoPrimitiveAlgorithmSecondaryFamily`
- **数据类型**: ENUMERATION
- **多重性**: [1..infinite]
- **默认值**: `CRYPTO_ALGOFAM_NOT_SET`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_NOT_SET`
  - `CRYPTO_ALGOFAM_SHA1`
  - `CRYPTO_ALGOFAM_SHA2_224`
  - `CRYPTO_ALGOFAM_SHA2_256`
  - `CRYPTO_ALGOFAM_SHA2_384`
  - `CRYPTO_ALGOFAM_SHA2_512`
  - `CRYPTO_ALGOFAM_SHA2_512_224`
  - `CRYPTO_ALGOFAM_SHA2_512_256`
  - `CRYPTO_ALGOFAM_SHA3_224`
  - `CRYPTO_ALGOFAM_SHA3_256`
  - `CRYPTO_ALGOFAM_SHA3_384`
  - `CRYPTO_ALGOFAM_SHA3_512`
  - `CRYPTO_ALGOFAM_SHAKE128`
  - `CRYPTO_ALGOFAM_SHAKE256`
  - `CRYPTO_ALGOFAM_RIPEMD160`
  - `CRYPTO_ALGOFAM_BLAKE_1_256`
  - `CRYPTO_ALGOFAM_BLAKE_1_512`
  - `CRYPTO_ALGOFAM_BLAKE_2s_256`
  - `CRYPTO_ALGOFAM_BLAKE_2s_512`
  - `CRYPTO_ALGOFAM_3DES`
  - `CRYPTO_ALGOFAM_AES`
  - `CRYPTO_ALGOFAM_CHACHA`
  - `CRYPTO_ALGOFAM_RSA`
  - `CRYPTO_ALGOFAM_ED25519`
  - `CRYPTO_ALGOFAM_BRAINPOOL`
  - `CRYPTO_ALGOFAM_ECCNIST`
  - `CRYPTO_ALGOFAM_SECURECOUNTER`
  - `CRYPTO_ALGOFAM_RNG`
  - `CRYPTO_ALGOFAM_SIPHASH`
  - `CRYPTO_ALGOFAM_ECIES`
  - `CRYPTO_ALGOFAM_CUSTOM`
  - `CRYPTO_ALGOFAM_CUSTOM_PADDING_PKCS7`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Determines the algorithm secondary family used for the crypto service

##### 5. CryptoGeneral

**容器属性**:

- **UUID**: `f489c13a-20f0-4d28-97b0-c62ccee11ff6`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CryptoGeneral`
- **多重性**: [1..1]
- **构建后可变**: false

**容器描述**:

Container for common configuration options.

###### 参数配置

此容器包含 **8** 个参数：

####### INTEGER 类型参数

######## 1. CryptoTrngPrefetchCapacity

- **UUID**: `a92e50bf-abbd-4c4a-9927-144b86ac5f33`
- **参数名**: `CryptoTrngPrefetchCapacity`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `32`
- **取值范围**: [0..128]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Capacity of the Trng Prefetching buffer.
A size greater zero will allocate a buffer which is constantly filled up with random data from the Trng.
This will speed up job requests for random numbers since they have been already generated in the background.
A capacity of 0 will disable Trng Prefetching.

######## 2. CryptoNonPreemptiveChunkSize

- **UUID**: `56099e72-eeb7-4e82-8383-b75ecc9b1c13`
- **参数名**: `CryptoNonPreemptiveChunkSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `1024`
- **取值范围**: [1..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines a threshold in bytes at which data processing of crypto jobs stop to allow asynchronous jobs to interact with the hardware.

The exact amount of bytes to process also depends on the primitive itself.
E.g. AES-128 can only stop every 16 bytes at minimum.

A value of 0xFFFFFFFF disables asynchronous job processing on the hardware.

####### BOOLEAN 类型参数

######## 1. CryptoDevErrorDetect

- **UUID**: `fd65fb95-c6f2-48b7-bd37-358a4f9bfc62`
- **参数名**: `CryptoDevErrorDetect`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Switches the development error detection and notification on or off. 
- True: detection and notification is enabled. 
- False: detection and notification is disabled.

######## 2. CryptoClearWorkspaceBuffers

- **UUID**: `ed27f53b-ea32-48d0-b7ae-91e3f326b646`
- **参数名**: `CryptoClearWorkspaceBuffers`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: For improved security workspace buffers can be cleared before and after usage. This has some influence on runtime performance.

######## 3. CryptoTrngPrefetchWithInterrupt

- **UUID**: `ee6041ad-cdb4-4207-a853-56065e4c21dc`
- **参数名**: `CryptoTrngPrefetchWithInterrupt`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enables/Disables trng number pre-fetching with interrupt of TRNG module

######## 4. CryptoProvideISRs

- **UUID**: `a6528813-bb77-4349-aad1-063f87d554a1`
- **参数名**: `CryptoProvideISRs`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Provide two interrupt service routines.
One is a default handler which does a software reset, the other can handle ECC errors and do a software reset.

######## 5. CryptoApplicationGenerateNoise

- **UUID**: `9ece140c-82b3-4aaa-a742-8cced30f10a3`
- **参数名**: `CryptoApplicationGenerateNoise`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Let application cores generate noise while HSM secure boot is running.

On configurations where the application cores are released by the HSM, the HSM can instruct the application cores (via HSM2HTS register) to generate random noise while it is busy.
This obfuscates what the HSM is processing (power profile) and can protect from side channel attacks.

Only enable this if DMU_SP_PROCONHSMCFG.SSWWAIT is set.

####### ENUMERATION 类型参数

######## 1. CryptoRequestIsrCategory

- **UUID**: `9e636534-f05b-41b9-8396-20249e84c640`
- **参数名**: `CryptoRequestIsrCategory`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `CATEGORY_1`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CATEGORY_1` (来源: Vector Informatik)
  - `NONE` (来源: Vector Informatik)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Select the category of the interrupt triggered by application to indicate a job request. Determines how the interrupt will be processed.

NONE: No interrupt will be processed
CATEGORY_1: Interrupt which is handled by vHsm

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. CryptoKeyDerive

**容器属性**:

- **UUID**: `7560bd9a-8daf-49d6-9c9f-0e96073be742`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CryptoKeyDerive`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container for Key Derivation options.

######## 参数配置

此容器包含 **5** 个参数：

######### INTEGER 类型参数

########## 1. CryptoMaxInputLength

- **UUID**: `6fe940df-ea37-4fe8-a0d2-44925802ada0`
- **参数名**: `CryptoMaxInputLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `100`
- **取值范围**: [3..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the maximal total input Length for Key Derivation in Byte. This value defines the size of an internal buffer for the key derivation.
The concatenated input string (counter | label | zero octet | context | target key length) has to fit into the buffer.

########## 2. CryptoSizeOfTargetKeyLength

- **UUID**: `2539b9d9-c508-4e90-a6d5-301c454cf210`
- **参数名**: `CryptoSizeOfTargetKeyLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `2`
- **取值范围**: [1..4]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The numeric length of the requested target key is concatenated to the input of the KeyDerive function. This parameter sets the length in byte which are concatenated (the length of the binary string).
Additionally the parameter limits the max. length of the derived key.

########## 3. CryptoSizeOfIterationCounter

- **UUID**: `f89d321d-e2ef-4fc1-a6c4-825f28776f9f`
- **参数名**: `CryptoSizeOfIterationCounter`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `1`
- **取值范围**: [1..4]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: On each iteration of the KeyDerive function the iteration counter is concatenated to the input data. This parameter sets the length in byte which are concatenated to the input (length of binary representation of the counter).
Additionally the parameter limits the max. length of the derived key.

########## 4. CryptoMaxOutputKeyLength

- **UUID**: `960668de-d1b7-483a-b688-8ed283f6d9e2`
- **参数名**: `CryptoMaxOutputKeyLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `32`
- **取值范围**: [1..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the maximal length of the output key. This parameter defines the size of an buffer for the key derivation. The output key length is defined as the size of the output key element on id 1.

######### BOOLEAN 类型参数

########## 1. CryptoAddZeroOctet

- **UUID**: `10b1b7cb-ed2a-4c69-8424-82ebdc3ad42f`
- **参数名**: `CryptoAddZeroOctet`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: If this switch is activated a zero octet (0x00) is added between the label and the context input.

######## 引用关系

此容器包含 **1** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. CryptoKeyDeriveDriverObject

- **UUID**: `6182084a-98f2-451f-aa94-ebbba9d83021`
- **引用名**: `CryptoKeyDeriveDriverObject`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `CryptoDriverObject`
- **完整路径**: `/MICROSAR/vHsm_Hal/Crypto/CryptoDriverObjects/CryptoDriverObject`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Driver object for key derivation

##### 6. CryptoKeyDerive

**容器属性**:

- **UUID**: `7560bd9a-8daf-49d6-9c9f-0e96073be742`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CryptoKeyDerive`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container for Key Derivation options.

###### 参数配置

此容器包含 **5** 个参数：

####### INTEGER 类型参数

######## 1. CryptoMaxInputLength

- **UUID**: `6fe940df-ea37-4fe8-a0d2-44925802ada0`
- **参数名**: `CryptoMaxInputLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `100`
- **取值范围**: [3..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the maximal total input Length for Key Derivation in Byte. This value defines the size of an internal buffer for the key derivation.
The concatenated input string (counter | label | zero octet | context | target key length) has to fit into the buffer.

######## 2. CryptoSizeOfTargetKeyLength

- **UUID**: `2539b9d9-c508-4e90-a6d5-301c454cf210`
- **参数名**: `CryptoSizeOfTargetKeyLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `2`
- **取值范围**: [1..4]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The numeric length of the requested target key is concatenated to the input of the KeyDerive function. This parameter sets the length in byte which are concatenated (the length of the binary string).
Additionally the parameter limits the max. length of the derived key.

######## 3. CryptoSizeOfIterationCounter

- **UUID**: `f89d321d-e2ef-4fc1-a6c4-825f28776f9f`
- **参数名**: `CryptoSizeOfIterationCounter`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `1`
- **取值范围**: [1..4]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: On each iteration of the KeyDerive function the iteration counter is concatenated to the input data. This parameter sets the length in byte which are concatenated to the input (length of binary representation of the counter).
Additionally the parameter limits the max. length of the derived key.

######## 4. CryptoMaxOutputKeyLength

- **UUID**: `960668de-d1b7-483a-b688-8ed283f6d9e2`
- **参数名**: `CryptoMaxOutputKeyLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `32`
- **取值范围**: [1..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the maximal length of the output key. This parameter defines the size of an buffer for the key derivation. The output key length is defined as the size of the output key element on id 1.

####### BOOLEAN 类型参数

######## 1. CryptoAddZeroOctet

- **UUID**: `10b1b7cb-ed2a-4c69-8424-82ebdc3ad42f`
- **参数名**: `CryptoAddZeroOctet`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: If this switch is activated a zero octet (0x00) is added between the label and the context input.

###### 引用关系

此容器包含 **1** 个引用：

####### SYMBOLIC-NAME-REFERENCE 类型引用

######## 1. CryptoKeyDeriveDriverObject

- **UUID**: `6182084a-98f2-451f-aa94-ebbba9d83021`
- **引用名**: `CryptoKeyDeriveDriverObject`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `CryptoDriverObject`
- **完整路径**: `/MICROSAR/vHsm_Hal/Crypto/CryptoDriverObjects/CryptoDriverObject`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Driver object for key derivation

##### 7. CryptoKeyElements

**容器属性**:

- **UUID**: `6dd83546-2e5d-4a50-ba17-f5a0885fc8bd`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CryptoKeyElements`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container for CRYPTO key elements.

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. CryptoKeyElement

**容器属性**:

- **UUID**: `10dcb0d0-5f66-4661-921b-4148a7168de9`
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

- **UUID**: `ebda6102-1a14-420c-806e-d7526945e84c`
- **参数名**: `CryptoKeyElementId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `1`
- **取值范围**: [0..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Identifier of the CRYPTO key element

########## 2. CryptoKeyElementSize

- **UUID**: `a685b69f-bf57-4581-b091-a59338eeeafd`
- **参数名**: `CryptoKeyElementSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `16`
- **取值范围**: [1..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Maximum size of a CRYPTO key element in bytes

######### BOOLEAN 类型参数

########## 1. CryptoKeyElementAllowPartialAccess

- **UUID**: `4e752c4b-936b-4444-ae55-e1de8c1816c8`
- **参数名**: `CryptoKeyElementAllowPartialAccess`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enable or disable writing and reading the key element with data smaller than the size of the element.
- True: enable partial access of the key element
- False: disable partial access of the key element

########## 2. CryptoKeyElementPersist

- **UUID**: `eca7754b-30dd-4c47-a9c6-d22bac666743`
- **参数名**: `CryptoKeyElementPersist`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enable or disable persisting of the key element in non-volatile storage.
- True: enable persisting of the key element.
- False: disable persisting of the key element.

######### STRING 类型参数

########## 1. CryptoKeyElementInitValue

- **UUID**: `17677aeb-b421-4742-b38e-2862cc5b082b`
- **参数名**: `CryptoKeyElementInitValue`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **字符串变体**:
  - 默认值: `0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Value which will be used to fill the element during initialization, when the element is not already initialized.

######### ENUMERATION 类型参数

########## 1. CryptoKeyElementReadAccess

- **UUID**: `173fc994-4b7d-42f0-bc3a-79fa78fccc0b`
- **参数名**: `CryptoKeyElementReadAccess`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `RA_ALLOWED`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `RA_ALLOWED` (来源: Vector Informatik)
  - `RA_DENIED` (来源: Vector Informatik)
  - `RA_ENCRYPTED` (来源: Vector Informatik)
  - `RA_INTERNAL_COPY` (来源: Vector Informatik)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Define the reading access rights of the key element.
CRYPTO_RA_DENIED = key element cannot be read from outside the Crypto Driver
CRYPTO_RA INTERNAL_COPY = key element can be copied to another key element in the same crypto driver.
CRYPTO_RA_ALLOWED = key element can be read as plaintext
CRYPTO_RA_ENCRYPTED = key element can be read encrypted. E.g. SHE Ram-Key export.

########## 2. CryptoKeyElementWriteAccess

- **UUID**: `c0369a9c-9e6a-4eb3-bfee-238650068eac`
- **参数名**: `CryptoKeyElementWriteAccess`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `WA_ALLOWED`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `WA_ALLOWED` (来源: Vector Informatik)
  - `WA_DENIED` (来源: Vector Informatik)
  - `WA_ENCRYPTED` (来源: Vector Informatik)
  - `WA_INTERNAL_COPY` (来源: Vector Informatik)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Define the writing access rights of the key element
CRYPTO_WA_DENIED = key element cannot be written from outside the Crypto Driver
CRYPTO_WA INTERNAL_COPY = key element can be filled with another key element in the same crypto driver.
CRYPTO_WA_ALLOWED = key element can be rewritten as plaintext
CRYPTO_WA_ENCRYPTED = key element can be written encrypted. E.g. SHE load key.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. CryptoKeyElementVirtualTargetRef

- **UUID**: `d9e772e0-dda2-4da5-8260-80100d97db82`
- **引用名**: `CryptoKeyElementVirtualTargetRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `CryptoKeyElement`
- **完整路径**: `/MICROSAR/vHsm_Hal/Crypto/CryptoKeyElements/CryptoKeyElement`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Not used.
Refers to a key element which will contain the actual data. If the Reference is configured, the key element will be a virtual key element.

##### 8. CryptoKeyElement

**容器属性**:

- **UUID**: `10dcb0d0-5f66-4661-921b-4148a7168de9`
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

- **UUID**: `ebda6102-1a14-420c-806e-d7526945e84c`
- **参数名**: `CryptoKeyElementId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `1`
- **取值范围**: [0..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Identifier of the CRYPTO key element

######## 2. CryptoKeyElementSize

- **UUID**: `a685b69f-bf57-4581-b091-a59338eeeafd`
- **参数名**: `CryptoKeyElementSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `16`
- **取值范围**: [1..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Maximum size of a CRYPTO key element in bytes

####### BOOLEAN 类型参数

######## 1. CryptoKeyElementAllowPartialAccess

- **UUID**: `4e752c4b-936b-4444-ae55-e1de8c1816c8`
- **参数名**: `CryptoKeyElementAllowPartialAccess`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enable or disable writing and reading the key element with data smaller than the size of the element.
- True: enable partial access of the key element
- False: disable partial access of the key element

######## 2. CryptoKeyElementPersist

- **UUID**: `eca7754b-30dd-4c47-a9c6-d22bac666743`
- **参数名**: `CryptoKeyElementPersist`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enable or disable persisting of the key element in non-volatile storage.
- True: enable persisting of the key element.
- False: disable persisting of the key element.

####### STRING 类型参数

######## 1. CryptoKeyElementInitValue

- **UUID**: `17677aeb-b421-4742-b38e-2862cc5b082b`
- **参数名**: `CryptoKeyElementInitValue`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **字符串变体**:
  - 默认值: `0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Value which will be used to fill the element during initialization, when the element is not already initialized.

####### ENUMERATION 类型参数

######## 1. CryptoKeyElementReadAccess

- **UUID**: `173fc994-4b7d-42f0-bc3a-79fa78fccc0b`
- **参数名**: `CryptoKeyElementReadAccess`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `RA_ALLOWED`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `RA_ALLOWED` (来源: Vector Informatik)
  - `RA_DENIED` (来源: Vector Informatik)
  - `RA_ENCRYPTED` (来源: Vector Informatik)
  - `RA_INTERNAL_COPY` (来源: Vector Informatik)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Define the reading access rights of the key element.
CRYPTO_RA_DENIED = key element cannot be read from outside the Crypto Driver
CRYPTO_RA INTERNAL_COPY = key element can be copied to another key element in the same crypto driver.
CRYPTO_RA_ALLOWED = key element can be read as plaintext
CRYPTO_RA_ENCRYPTED = key element can be read encrypted. E.g. SHE Ram-Key export.

######## 2. CryptoKeyElementWriteAccess

- **UUID**: `c0369a9c-9e6a-4eb3-bfee-238650068eac`
- **参数名**: `CryptoKeyElementWriteAccess`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `WA_ALLOWED`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `WA_ALLOWED` (来源: Vector Informatik)
  - `WA_DENIED` (来源: Vector Informatik)
  - `WA_ENCRYPTED` (来源: Vector Informatik)
  - `WA_INTERNAL_COPY` (来源: Vector Informatik)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Define the writing access rights of the key element
CRYPTO_WA_DENIED = key element cannot be written from outside the Crypto Driver
CRYPTO_WA INTERNAL_COPY = key element can be filled with another key element in the same crypto driver.
CRYPTO_WA_ALLOWED = key element can be rewritten as plaintext
CRYPTO_WA_ENCRYPTED = key element can be written encrypted. E.g. SHE load key.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. CryptoKeyElementVirtualTargetRef

- **UUID**: `d9e772e0-dda2-4da5-8260-80100d97db82`
- **引用名**: `CryptoKeyElementVirtualTargetRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `CryptoKeyElement`
- **完整路径**: `/MICROSAR/vHsm_Hal/Crypto/CryptoKeyElements/CryptoKeyElement`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Not used.
Refers to a key element which will contain the actual data. If the Reference is configured, the key element will be a virtual key element.

##### 9. CryptoKeys

**容器属性**:

- **UUID**: `3ff69b1f-6fbf-46a4-9688-eba4a4ef1380`
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

- **UUID**: `82a1442c-6a9d-4f6f-bc7c-02f6370a7789`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CryptoKey`
- **多重性**: [1..infinite]
- **构建后可变**: false

**容器描述**:

Configuration of a CryptoKey

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. CryptoKeyId

- **UUID**: `6801b894-cfb1-451b-8cb6-6f6f37227ed6`
- **参数名**: `CryptoKeyId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `30000`
- **取值范围**: [30000..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Identifier of the CRYPTO key

########## 2. CryptoKeyDeriveIterations

- **UUID**: `de406d60-8cb9-4dd9-a43f-393bccb845ee`
- **参数名**: `CryptoKeyDeriveIterations`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `1`
- **取值范围**: [1..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Not used.
Holds the number of iterations to be performed by the key derivation primitive.

######## 引用关系

此容器包含 **2** 个引用：

######### REFERENCE 类型引用

########## 1. CryptoKeyTypeRef

- **UUID**: `99a0607c-7af0-483b-8afb-fdd3a25b6f38`
- **引用名**: `CryptoKeyTypeRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `CryptoKeyType`
- **完整路径**: `/MICROSAR/vHsm_Hal/Crypto/CryptoKeyTypes/CryptoKeyType`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Refers to a pointer in the CRYPTO to a CryptoKeyType. The CryptoKeyType provides the information which key elements are contained in a CryptoKey.

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. CryptoKeyAggregationRef

- **UUID**: `4783823c-424d-4f54-b2ec-6d27f0a86653`
- **引用名**: `CryptoKeyAggregationRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `CryptoKey`
- **完整路径**: `/MICROSAR/Crypto_30_LibCv/Crypto/CryptoKeys/CryptoKey`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a key in the LibCv driver of the vHsm.
This key gets extended by the elements of the referenced key so that all elements of the aggregated key are also accessible by this key. 
Furthermore, it is used to store elements as this driver does not provide a Nv storage mechanism.This is i.e. used for the vHsmInfo key where the aggregated key needs to provide and store the UID element.

If the aggregated key contains the same element id as this key, the element of this key is used.
The referenced key can be added to the key routing. This have the effect that the keys are completely paired and all elements are accessible over both key ids.

##### 10. CryptoKey

**容器属性**:

- **UUID**: `82a1442c-6a9d-4f6f-bc7c-02f6370a7789`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CryptoKey`
- **多重性**: [1..infinite]
- **构建后可变**: false

**容器描述**:

Configuration of a CryptoKey

###### 参数配置

此容器包含 **2** 个参数：

####### INTEGER 类型参数

######## 1. CryptoKeyId

- **UUID**: `6801b894-cfb1-451b-8cb6-6f6f37227ed6`
- **参数名**: `CryptoKeyId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `30000`
- **取值范围**: [30000..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Identifier of the CRYPTO key

######## 2. CryptoKeyDeriveIterations

- **UUID**: `de406d60-8cb9-4dd9-a43f-393bccb845ee`
- **参数名**: `CryptoKeyDeriveIterations`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `1`
- **取值范围**: [1..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Not used.
Holds the number of iterations to be performed by the key derivation primitive.

###### 引用关系

此容器包含 **2** 个引用：

####### REFERENCE 类型引用

######## 1. CryptoKeyTypeRef

- **UUID**: `99a0607c-7af0-483b-8afb-fdd3a25b6f38`
- **引用名**: `CryptoKeyTypeRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `CryptoKeyType`
- **完整路径**: `/MICROSAR/vHsm_Hal/Crypto/CryptoKeyTypes/CryptoKeyType`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Refers to a pointer in the CRYPTO to a CryptoKeyType. The CryptoKeyType provides the information which key elements are contained in a CryptoKey.

####### SYMBOLIC-NAME-REFERENCE 类型引用

######## 1. CryptoKeyAggregationRef

- **UUID**: `4783823c-424d-4f54-b2ec-6d27f0a86653`
- **引用名**: `CryptoKeyAggregationRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `CryptoKey`
- **完整路径**: `/MICROSAR/Crypto_30_LibCv/Crypto/CryptoKeys/CryptoKey`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a key in the LibCv driver of the vHsm.
This key gets extended by the elements of the referenced key so that all elements of the aggregated key are also accessible by this key. 
Furthermore, it is used to store elements as this driver does not provide a Nv storage mechanism.This is i.e. used for the vHsmInfo key where the aggregated key needs to provide and store the UID element.

If the aggregated key contains the same element id as this key, the element of this key is used.
The referenced key can be added to the key routing. This have the effect that the keys are completely paired and all elements are accessible over both key ids.

##### 11. CryptoKeyTypes

**容器属性**:

- **UUID**: `6dafdd46-7ca2-42f2-adc2-199abfba8957`
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

- **UUID**: `d90cc407-1eaf-415c-ac5b-baf108a47675`
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

- **UUID**: `b599dd2e-5aec-4108-9708-800d22052b4b`
- **引用名**: `CryptoKeyElementRef`
- **引用类型**: REFERENCE
- **多重性**: [1..infinite]
- **目标**: `CryptoKeyElement`
- **完整路径**: `/MICROSAR/vHsm_Hal/Crypto/CryptoKeyElements/CryptoKeyElement`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Refers to a pointer in the CRYPTO Key Element, which holds the data of the crypto key element.

##### 12. CryptoKeyType

**容器属性**:

- **UUID**: `d90cc407-1eaf-415c-ac5b-baf108a47675`
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

- **UUID**: `b599dd2e-5aec-4108-9708-800d22052b4b`
- **引用名**: `CryptoKeyElementRef`
- **引用类型**: REFERENCE
- **多重性**: [1..infinite]
- **目标**: `CryptoKeyElement`
- **完整路径**: `/MICROSAR/vHsm_Hal/Crypto/CryptoKeyElements/CryptoKeyElement`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Refers to a pointer in the CRYPTO Key Element, which holds the data of the crypto key element.

## 📦 包结构

此ARXML文件包含 **2** 个包：

### 1. MICROSAR

- **UUID**: `ff55d029-386d-43a2-b3c2-dfef4c7a5e36`
- **包名称**: `MICROSAR`
- **包含元素数量**: 0

### 2. vHsm_Hal

- **UUID**: `b4b8e5dd-7621-44f5-b0d0-70346b08094c`
- **包名称**: `vHsm_Hal`
- **包含元素数量**: 2

#### 包含的元素

##### BSW-IMPLEMENTATION 类型元素

1. **Crypto_Impl**

##### ECUC-MODULE-DEF 类型元素

1. **Crypto**

## ⚡ 实现信息

此ARXML文件包含 **1** 个实现：

### 1. Crypto_Impl

- **UUID**: `1a1491f6-7cc9-49cb-a255-e18167548a83`
- **实现名称**: `Crypto_Impl`
- **编程语言**: C
- **软件版本**: 3.03.00
- **供应商ID**: 30
- **AUTOSAR版本**: 4.03.00
- **代码生成器**: DaVinci Configurator
