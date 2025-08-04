# Crypto - 完整配置文档

*此文档由ARXML文件自动生成，采用层次化结构展示*

**生成时间**: 2025-06-16 14:50:58

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

Software Crypto Driver

#### 版本历史

共有 **2** 个版本记录：

##### 1. 版本 1.00.00

- **状态**: beta
- **发布日期**: 2018-05-15T12:18:47+02:00
- **发布者**: vistof

**变更内容**:

##### 2. 版本 1.01.00

- **状态**: released
- **发布日期**: 2018-07-02T15:21:53+02:00
- **发布者**: vistof

**变更内容**:

#### 配置容器

本模块包含 **4** 个配置容器：

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
- **多重性**: [1..1]
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
- **多重性**: [1..1]
- **目标**: `CryptoPrimitive`
- **完整路径**: `/MICROSAR/vHsm_Custom/Crypto/CryptoPrimitives/CryptoPrimitive`
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
- **多重性**: [1..1]
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
- **多重性**: [1..1]
- **目标**: `CryptoPrimitive`
- **完整路径**: `/MICROSAR/vHsm_Custom/Crypto/CryptoPrimitives/CryptoPrimitive`
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
- **多重性**: [0..1]
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
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Determines the algorithm secondary family used for the crypto service

##### 4. CryptoPrimitive

**容器属性**:

- **UUID**: `7cff9f20-8611-4ed0-96e9-a99346f6ed4a`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CryptoPrimitive`
- **多重性**: [0..1]
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
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Determines the algorithm secondary family used for the crypto service

## 📦 包结构

此ARXML文件包含 **2** 个包：

### 1. MICROSAR

- **UUID**: `ff55d029-386d-43a2-b3c2-dfef4c7a5e36`
- **包名称**: `MICROSAR`
- **包含元素数量**: 0

### 2. vHsm_Custom

- **UUID**: `b4b8e5dd-7621-44f5-b0d0-70346b08094c`
- **包名称**: `vHsm_Custom`
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
- **软件版本**: 1.01.00
- **供应商ID**: 30
- **AUTOSAR版本**: 4.03.00
- **代码生成器**: DaVinci Configurator

## ⚙️ 配置信息

此ARXML文件包含 **2** 个配置：

### 1. Crypto_Pre

- **UUID**: `bdfb30ef-8d85-4bbe-8b05-7b01adde4a30`
- **配置名称**: `Crypto_Pre`
- **定义引用**: `/MICROSAR/vHsm_Custom/Crypto`

### 2. Crypto_Rec

- **UUID**: `e649f890-e05c-49fa-908c-1eec1c3882ab`
- **配置名称**: `Crypto_Rec`
- **定义引用**: `/MICROSAR/vHsm_Custom/Crypto`
