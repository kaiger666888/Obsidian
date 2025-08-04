# Crypto - 完整配置文档

*此文档由ARXML文件自动生成，采用层次化结构展示*

**生成时间**: 2025-06-16 14:50:57

## 📑 目录

- [📄 文件信息](#-文件信息)
- [🔧 模块定义](#-模块定义)
  - [Crypto](#crypto)
- [📦 包结构](#-包结构)
- [⚡ 实现信息](#-实现信息)
- [⚙️ 配置信息](#️-配置信息)

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

Crypto Driver for the core functionality of the vHsm

#### 版本历史

共有 **12** 个版本记录：

##### 1. 版本 2.01.00

- **状态**: released
- **发布日期**: 2018-05-15T12:17:02+02:00
- **发布者**: vistof

**变更内容**:

##### 2. 版本 2.01.01

- **状态**: released
- **发布日期**: 2019-05-06T10:39:23+02:00
- **发布者**: vistof

**变更内容**:

##### 3. 版本 2.01.02

- **状态**: released
- **发布日期**: 2019-07-01T10:13:15+02:00
- **发布者**: vistof

**变更内容**:

##### 4. 版本 2.01.03

- **状态**: released
- **发布日期**: 2019-07-08T15:54:06+02:00
- **发布者**: vistof

**变更内容**:

##### 5. 版本 3.00.00

- **状态**: released
- **发布日期**: 2019-08-13T13:33:41+02:00
- **发布者**: vistof

**变更内容**:

##### 6. 版本 3.00.01

- **状态**: released
- **发布日期**: 2019-09-13T13:08:02+02:00
- **发布者**: vistof

**变更内容**:

##### 7. 版本 3.01.00

- **状态**: released
- **发布日期**: 2019-10-18T10:38:27+02:00
- **发布者**: vistof

**变更内容**:

##### 8. 版本 4.00.00

- **状态**: released
- **发布日期**: 2019-12-06T09:57:39+01:00
- **发布者**: vistof

**变更内容**:

##### 9. 版本 4.01.00

- **状态**: released
- **发布日期**: 2020-04-21T13:39:39+02:00
- **发布者**: vistof

**变更内容**:

##### 10. 版本 4.02.00

- **状态**: released
- **发布日期**: 2020-06-03T14:42:38+02:00
- **发布者**: vistof

**变更内容**:

##### 11. 版本 5.00.00

- **状态**: released
- **发布日期**: 2020-07-01T20:18:49+02:00
- **发布者**: vistof

**变更内容**:

##### 12. 版本 5.00.01

- **状态**: released
- **发布日期**: 2020-12-09T14:40:57+01:00
- **发布者**: vistof

**变更内容**:

#### 配置容器

本模块包含 **10** 个配置容器：

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
- **多重性**: [2..2]
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
- **完整路径**: `/MICROSAR/vHsm_Core/Crypto/CryptoPrimitives/CryptoPrimitive`
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
- **多重性**: [2..2]
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
- **完整路径**: `/MICROSAR/vHsm_Core/Crypto/CryptoPrimitives/CryptoPrimitive`
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
  - `CRYPTO_ALGOFAM_CUSTOM_VHSM_SOFTWARE_DOWNLOAD`
  - `CRYPTO_ALGOFAM_CUSTOM_VHSM_SECURE_BOOT`
  - `CRYPTO_ALGOFAM_CUSTOM_VHSM_FIRMWARE_UPDATE`
  - `CRYPTO_ALGOFAM_CUSTOM_VHSM_SECURE_BOOT_UPDATE`
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
  - `CRYPTO_ALGOMODE_CUSTOM_VHSM_FIRMWARE_UPDATE`
  - `CRYPTO_ALGOMODE_CUSTOM_SECURE_BOOT_FORCE_SEQUENTIAL`
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
  - `CRYPTO_ALGOFAM_CUSTOM_VHSM_SOFTWARE_DOWNLOAD`
  - `CRYPTO_ALGOFAM_CUSTOM_VHSM_SECURE_BOOT`
  - `CRYPTO_ALGOFAM_CUSTOM_VHSM_FIRMWARE_UPDATE`
  - `CRYPTO_ALGOFAM_CUSTOM_VHSM_SECURE_BOOT_UPDATE`
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
  - `CRYPTO_ALGOMODE_CUSTOM_VHSM_FIRMWARE_UPDATE`
  - `CRYPTO_ALGOMODE_CUSTOM_SECURE_BOOT_FORCE_SEQUENTIAL`
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
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Determines the algorithm secondary family used for the crypto service

##### 5. CryptoKeys

**容器属性**:

- **UUID**: `671e2213-b7e4-406f-826c-b1e5897d2daf`
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

- **UUID**: `a554ad5f-9ab0-42ec-8eb0-26ebcc51e782`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CryptoKey`
- **多重性**: [3..3]
- **构建后可变**: false

**容器描述**:

Configuration of a CryptoKey

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. CryptoKeyId

- **UUID**: `94955cda-556a-4d8e-94d2-6248e9174542`
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

- **UUID**: `6472b4d1-55fd-45ac-b415-a0dab90ccd65`
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

- **UUID**: `5ea52c2d-debb-479c-8687-1771277eceb4`
- **引用名**: `CryptoKeyTypeRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `CryptoKeyType`
- **完整路径**: `/MICROSAR/vHsm_Core/Crypto/CryptoKeyTypes/CryptoKeyType`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Refers to a pointer in the CRYPTO to a CryptoKeyType. The CryptoKeyType provides the information which key elements are contained in a CryptoKey.

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. CryptoKeyAggregationRef

- **UUID**: `263d1148-f4d7-4a81-ba35-ed58b19c494e`
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

##### 6. CryptoKey

**容器属性**:

- **UUID**: `a554ad5f-9ab0-42ec-8eb0-26ebcc51e782`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CryptoKey`
- **多重性**: [3..3]
- **构建后可变**: false

**容器描述**:

Configuration of a CryptoKey

###### 参数配置

此容器包含 **2** 个参数：

####### INTEGER 类型参数

######## 1. CryptoKeyId

- **UUID**: `94955cda-556a-4d8e-94d2-6248e9174542`
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

- **UUID**: `6472b4d1-55fd-45ac-b415-a0dab90ccd65`
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

- **UUID**: `5ea52c2d-debb-479c-8687-1771277eceb4`
- **引用名**: `CryptoKeyTypeRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `CryptoKeyType`
- **完整路径**: `/MICROSAR/vHsm_Core/Crypto/CryptoKeyTypes/CryptoKeyType`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Refers to a pointer in the CRYPTO to a CryptoKeyType. The CryptoKeyType provides the information which key elements are contained in a CryptoKey.

####### SYMBOLIC-NAME-REFERENCE 类型引用

######## 1. CryptoKeyAggregationRef

- **UUID**: `263d1148-f4d7-4a81-ba35-ed58b19c494e`
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

##### 7. CryptoKeyElements

**容器属性**:

- **UUID**: `621dbfa9-796b-4eec-9b8b-2ae6f000bfbd`
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

- **UUID**: `6ec1431a-7532-411e-b55b-4af24ac0fa18`
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

- **UUID**: `2a17e698-ba56-4e22-a24c-9eddcb348b24`
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

- **UUID**: `c844ddd3-a0c3-450d-841b-b44e518fdfde`
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

- **UUID**: `e552f5a3-ac5e-4936-ada6-5e52e5d1196c`
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

- **UUID**: `13ed2ab0-3d4b-4477-b096-fbbfd507388e`
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

- **UUID**: `b022366a-69eb-45b5-9927-bedb1c4a2e72`
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

- **UUID**: `4851636a-c33f-4ff9-897d-6115180a5c60`
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

- **UUID**: `b5836b39-7191-4d41-824c-c44e557d0978`
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

- **UUID**: `03628e66-73fb-48fc-beed-a28f14bae021`
- **引用名**: `CryptoKeyElementVirtualTargetRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `CryptoKeyElement`
- **完整路径**: `/MICROSAR/vHsm_Core/Crypto/CryptoKeyElements/CryptoKeyElement`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Not used.
Refers to a key element which will contain the actual data. If the Reference is configured, the key element will be a virtual key element.

##### 8. CryptoKeyElement

**容器属性**:

- **UUID**: `6ec1431a-7532-411e-b55b-4af24ac0fa18`
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

- **UUID**: `2a17e698-ba56-4e22-a24c-9eddcb348b24`
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

- **UUID**: `c844ddd3-a0c3-450d-841b-b44e518fdfde`
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

- **UUID**: `e552f5a3-ac5e-4936-ada6-5e52e5d1196c`
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

- **UUID**: `13ed2ab0-3d4b-4477-b096-fbbfd507388e`
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

- **UUID**: `b022366a-69eb-45b5-9927-bedb1c4a2e72`
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

- **UUID**: `4851636a-c33f-4ff9-897d-6115180a5c60`
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

- **UUID**: `b5836b39-7191-4d41-824c-c44e557d0978`
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

- **UUID**: `03628e66-73fb-48fc-beed-a28f14bae021`
- **引用名**: `CryptoKeyElementVirtualTargetRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `CryptoKeyElement`
- **完整路径**: `/MICROSAR/vHsm_Core/Crypto/CryptoKeyElements/CryptoKeyElement`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Not used.
Refers to a key element which will contain the actual data. If the Reference is configured, the key element will be a virtual key element.

##### 9. CryptoKeyTypes

**容器属性**:

- **UUID**: `bfcdebf0-6f6f-4055-acb4-90f09823dbed`
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

- **UUID**: `d68ccf64-6cbe-4c4d-94bf-fb02f3940a4a`
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

- **UUID**: `7c96bf41-7caa-4c41-9ccb-5eb5b20f0a79`
- **引用名**: `CryptoKeyElementRef`
- **引用类型**: REFERENCE
- **多重性**: [1..infinite]
- **目标**: `CryptoKeyElement`
- **完整路径**: `/MICROSAR/vHsm_Core/Crypto/CryptoKeyElements/CryptoKeyElement`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Refers to a pointer in the CRYPTO Key Element, which holds the data of the crypto key element.

##### 10. CryptoKeyType

**容器属性**:

- **UUID**: `d68ccf64-6cbe-4c4d-94bf-fb02f3940a4a`
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

- **UUID**: `7c96bf41-7caa-4c41-9ccb-5eb5b20f0a79`
- **引用名**: `CryptoKeyElementRef`
- **引用类型**: REFERENCE
- **多重性**: [1..infinite]
- **目标**: `CryptoKeyElement`
- **完整路径**: `/MICROSAR/vHsm_Core/Crypto/CryptoKeyElements/CryptoKeyElement`
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

### 2. vHsm_Core

- **UUID**: `b4b8e5dd-7621-44f5-b0d0-70346b08094c`
- **包名称**: `vHsm_Core`
- **包含元素数量**: 4

#### 包含的元素

##### BSW-IMPLEMENTATION 类型元素

1. **Crypto_Impl**

##### ECUC-MODULE-DEF 类型元素

1. **Crypto**

##### ECUC-MODULE-CONFIGURATION-VALUES 类型元素

1. **Crypto_Pre**
2. **Crypto_Rec**

## ⚡ 实现信息

此ARXML文件包含 **1** 个实现：

### 1. Crypto_Impl

- **UUID**: `1a1491f6-7cc9-49cb-a255-e18167548a83`
- **实现名称**: `Crypto_Impl`
- **编程语言**: C
- **软件版本**: 5.00.01
- **供应商ID**: 30
- **AUTOSAR版本**: 4.03.00
- **代码生成器**: DaVinci Configurator

## ⚙️ 配置信息

此ARXML文件包含 **2** 个配置：

### 1. Crypto_Pre

- **UUID**: `21cb80f9-f85e-44c2-91ac-8b5c961a55a8`
- **配置名称**: `Crypto_Pre`
- **定义引用**: `/MICROSAR/vHsm_Core/Crypto`

### 2. Crypto_Rec

- **UUID**: `9f535111-6b7e-4519-b401-0caf653a0931`
- **配置名称**: `Crypto_Rec`
- **定义引用**: `/MICROSAR/vHsm_Core/Crypto`
