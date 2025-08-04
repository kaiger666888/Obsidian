# vSecPrim - 完整配置文档

*此文档由ARXML文件自动生成，采用层次化结构展示*

**生成时间**: 2025-06-16 14:48:30

## 📑 目录

- [📄 文件信息](#-文件信息)
- [🔧 模块定义](#-模块定义)
  - [vSecPrim](#vsecprim)
- [📦 包结构](#-包结构)
- [⚡ 实现信息](#-实现信息)
- [⚙️ 配置信息](#️-配置信息)

## 📄 文件信息

### Schema信息
- **Schema位置**: `http://autosar.org/schema/r4.0 AUTOSAR_4-0-3.xsd`
- **命名空间**: `http://autosar.org/schema/r4.0`

## 🔧 模块定义

### 1. vSecPrim

#### 基本信息

- **UUID**: `a09f997f-b6b6-47d8-ae6b-4cc58cee354f`
- **模块名称**: `vSecPrim`
- **类别**: `VENDOR_SPECIFIC_MODULE_DEFINITION`
- **多重性**: [0..1]
- **支持的变体**:
  - VARIANT-PRE-COMPILE
  - VARIANT-LINK-TIME

#### 模块描述

Software Crypto Library

#### 版本历史

共有 **15** 个版本记录：

##### 1. 版本 1.00.00

- **状态**: beta
- **发布日期**: 2018-07-07T02:21:42+02:00
- **发布者**: vismaw

**变更内容**:

##### 2. 版本 1.01.00

- **状态**: released
- **发布日期**: 2018-08-21T19:01:44+02:00
- **发布者**: visrpp

**变更内容**:

##### 3. 版本 2.00.00

- **状态**: released
- **发布日期**: 2018-12-12T08:04:37+01:00
- **发布者**: vismwe

**变更内容**:

##### 4. 版本 2.01.00

- **状态**: released
- **发布日期**: 2019-01-21T08:43:45+01:00
- **发布者**: vismwe

**变更内容**:

##### 5. 版本 2.02.00

- **状态**: released
- **发布日期**: 2019-02-20T13:29:49+01:00
- **发布者**: vismwe

**变更内容**:

##### 6. 版本 3.00.00

- **状态**: released
- **发布日期**: 2019-11-06T16:41:55+01:00
- **发布者**: viseag

**变更内容**:

##### 7. 版本 3.01.00

- **状态**: released
- **发布日期**: 2020-03-12T16:41:55+01:00
- **发布者**: viseag

**变更内容**:

##### 8. 版本 3.01.01

- **状态**: released
- **发布日期**: 2020-03-25T09:52:06+01:00
- **发布者**: vismwe

**变更内容**:

##### 9. 版本 4.00.00

- **状态**: released
- **发布日期**: 2020-04-14T16:41:55+01:00
- **发布者**: viseag

**变更内容**:

##### 10. 版本 4.00.01

- **状态**: released
- **发布日期**: 2020-05-14T11:56:06+01:00
- **发布者**: viseag

**变更内容**:

##### 11. 版本 4.01.00

- **状态**: released
- **发布日期**: 2020-05-19T12:02:55+01:00
- **发布者**: viseag

**变更内容**:

##### 12. 版本 4.02.00

- **状态**: released
- **发布日期**: 2020-07-06T09:15:55+01:00
- **发布者**: viseag

**变更内容**:

##### 13. 版本 5.00.00

- **状态**: released
- **发布日期**: 2020-08-18T09:15:55+01:00
- **发布者**: viseag

**变更内容**:

##### 14. 版本 5.01.00

- **状态**: released
- **发布日期**: 2020-09-04T15:25:55+01:00
- **发布者**: viseag

**变更内容**:

##### 15. 版本 5.02.00

- **状态**: released
- **发布日期**: 2020-10-21T15:20:22+01:00
- **发布者**: viseag

**变更内容**:

#### 配置容器

本模块包含 **14** 个配置容器：

##### 1. vSecPrimBasicAlgorithms

**容器属性**:

- **UUID**: `acd2dd30-01d8-4578-9195-463ffc9701a2`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vSecPrimBasicAlgorithms`
- **多重性**: [1..1]
- **构建后可变**: false

**容器描述**:

Container for basic algorithm configuration.

###### 配置容器

本模块包含 **2** 个配置容器：

####### 1. vSecPrimHash

**容器属性**:

- **UUID**: `915bb2b5-e734-4d17-8b6a-c5825781fcd0`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vSecPrimHash`
- **多重性**: [1..1]
- **构建后可变**: false

**容器描述**:

Container for hash algorithm configuration.

######## 参数配置

此容器包含 **6** 个参数：

######### BOOLEAN 类型参数

########## 1. vSecPrimSHA1Enabled

- **UUID**: `c52b1ff3-402c-488e-826f-eb2f0b90cfa5`
- **参数名**: `vSecPrimSHA1Enabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: If enabled, the following algorithm can be used:
SHA1

########## 2. vSecPrimRIPEMD160Enabled

- **UUID**: `ebf81dbe-59f8-47a9-84ae-fa6f096625ca`
- **参数名**: `vSecPrimRIPEMD160Enabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: If enabled, the following algorithm can be used:
RIPEMD160

########## 3. vSecPrimSHA2_256Enabled

- **UUID**: `f74de5a0-f6cf-4c4c-b2a3-c4cac7dcda6b`
- **参数名**: `vSecPrimSHA2_256Enabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: If enabled, the following algorithms can be used:
SHA2-224
SHA2-256

########## 4. vSecPrimSHA2_512Enabled

- **UUID**: `7ff72a22-3efb-4095-aac1-6e388213bb34`
- **参数名**: `vSecPrimSHA2_512Enabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: If enabled, the following algorithms can be used:
SHA2-384
SHA2-512
SHA2-512_224
SHA2-512_256

########## 5. vSecPrimSHA3Enabled

- **UUID**: `0e318c71-7741-4301-aa0b-a47858919c18`
- **参数名**: `vSecPrimSHA3Enabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: If enabled, the following algorithms can be used:
SHA3-224
SHA3-256
SHA3-384
SHA3-512
SHAKE128
SHAKE256

########## 6. vSecPrimMD5Enabled

- **UUID**: `55f64d77-c82f-4713-9cd2-ea82abeaf28c`
- **参数名**: `vSecPrimMD5Enabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: If enabled, the following algorithm can be used:
MD5

####### 2. vSecPrimRandomNumberGeneration

**容器属性**:

- **UUID**: `3fe98efd-f7d4-4210-8f14-5bf14cccfb76`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vSecPrimRandomNumberGeneration`
- **多重性**: [1..1]
- **构建后可变**: false

**容器描述**:

Container for random number generation algorithm configuration.

######## 参数配置

此容器包含 **3** 个参数：

######### BOOLEAN 类型参数

########## 1. vSecPrimFIPS186Enabled

- **UUID**: `4cebdf01-bf7a-42d3-a2a8-ca2f78b24794`
- **参数名**: `vSecPrimFIPS186Enabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: If enabled, the following algorithm can be used:
FIPS186-2

########## 2. vSecPrimCtrDrbgEnabled

- **UUID**: `835d6814-aefd-4990-9923-c3beb7561dab`
- **参数名**: `vSecPrimCtrDrbgEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: If enabled, the following algorithm can be used:
CTR_DRBG based on AES

########## 3. vSecPrimHashDrbgEnabled

- **UUID**: `96cb9229-7386-42cc-ab52-a60c1666b1d8`
- **参数名**: `vSecPrimHashDrbgEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: If enabled, the following algorithm can be used:
HASH_DRBG based on SHA2-512

##### 2. vSecPrimHash

**容器属性**:

- **UUID**: `915bb2b5-e734-4d17-8b6a-c5825781fcd0`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vSecPrimHash`
- **多重性**: [1..1]
- **构建后可变**: false

**容器描述**:

Container for hash algorithm configuration.

###### 参数配置

此容器包含 **6** 个参数：

####### BOOLEAN 类型参数

######## 1. vSecPrimSHA1Enabled

- **UUID**: `c52b1ff3-402c-488e-826f-eb2f0b90cfa5`
- **参数名**: `vSecPrimSHA1Enabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: If enabled, the following algorithm can be used:
SHA1

######## 2. vSecPrimRIPEMD160Enabled

- **UUID**: `ebf81dbe-59f8-47a9-84ae-fa6f096625ca`
- **参数名**: `vSecPrimRIPEMD160Enabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: If enabled, the following algorithm can be used:
RIPEMD160

######## 3. vSecPrimSHA2_256Enabled

- **UUID**: `f74de5a0-f6cf-4c4c-b2a3-c4cac7dcda6b`
- **参数名**: `vSecPrimSHA2_256Enabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: If enabled, the following algorithms can be used:
SHA2-224
SHA2-256

######## 4. vSecPrimSHA2_512Enabled

- **UUID**: `7ff72a22-3efb-4095-aac1-6e388213bb34`
- **参数名**: `vSecPrimSHA2_512Enabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: If enabled, the following algorithms can be used:
SHA2-384
SHA2-512
SHA2-512_224
SHA2-512_256

######## 5. vSecPrimSHA3Enabled

- **UUID**: `0e318c71-7741-4301-aa0b-a47858919c18`
- **参数名**: `vSecPrimSHA3Enabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: If enabled, the following algorithms can be used:
SHA3-224
SHA3-256
SHA3-384
SHA3-512
SHAKE128
SHAKE256

######## 6. vSecPrimMD5Enabled

- **UUID**: `55f64d77-c82f-4713-9cd2-ea82abeaf28c`
- **参数名**: `vSecPrimMD5Enabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: If enabled, the following algorithm can be used:
MD5

##### 3. vSecPrimRandomNumberGeneration

**容器属性**:

- **UUID**: `3fe98efd-f7d4-4210-8f14-5bf14cccfb76`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vSecPrimRandomNumberGeneration`
- **多重性**: [1..1]
- **构建后可变**: false

**容器描述**:

Container for random number generation algorithm configuration.

###### 参数配置

此容器包含 **3** 个参数：

####### BOOLEAN 类型参数

######## 1. vSecPrimFIPS186Enabled

- **UUID**: `4cebdf01-bf7a-42d3-a2a8-ca2f78b24794`
- **参数名**: `vSecPrimFIPS186Enabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: If enabled, the following algorithm can be used:
FIPS186-2

######## 2. vSecPrimCtrDrbgEnabled

- **UUID**: `835d6814-aefd-4990-9923-c3beb7561dab`
- **参数名**: `vSecPrimCtrDrbgEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: If enabled, the following algorithm can be used:
CTR_DRBG based on AES

######## 3. vSecPrimHashDrbgEnabled

- **UUID**: `96cb9229-7386-42cc-ab52-a60c1666b1d8`
- **参数名**: `vSecPrimHashDrbgEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: If enabled, the following algorithm can be used:
HASH_DRBG based on SHA2-512

##### 4. vSecPrimSymmetricAlgorithms

**容器属性**:

- **UUID**: `215f9c0f-ba08-48cf-8d53-4d67f1732642`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vSecPrimSymmetricAlgorithms`
- **多重性**: [1..1]
- **构建后可变**: false

**容器描述**:

Container for symmetric algorithm configuration.

###### 配置容器

本模块包含 **2** 个配置容器：

####### 1. vSecPrimCipher

**容器属性**:

- **UUID**: `319b3598-8057-464a-a28c-3fc0d134fa88`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vSecPrimCipher`
- **多重性**: [1..1]
- **构建后可变**: false

**容器描述**:

Container for symmetric cipher algorithm configuration.

######## 参数配置

此容器包含 **10** 个参数：

######### BOOLEAN 类型参数

########## 1. vSecPrimAes128Enabled

- **UUID**: `238985cc-c6a7-4bad-bcf4-89bbdbac4a9f`
- **参数名**: `vSecPrimAes128Enabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: If enabled, the following algorithm can be used:
AES128

########## 2. vSecPrimAes192Enabled

- **UUID**: `e9dc7245-1c64-47d7-b3ce-ef716d32b73e`
- **参数名**: `vSecPrimAes192Enabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: If enabled, the following algorithm can be used:
AES192

########## 3. vSecPrimAes256Enabled

- **UUID**: `63e7827d-4d87-4cf7-b73c-ee2c5e93f35e`
- **参数名**: `vSecPrimAes256Enabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: If enabled, the following algorithm can be used:
AES256

########## 4. vSecPrimGcmEnabled

- **UUID**: `c335a626-67d8-4ae6-af0f-5ed01b4d03d9`
- **参数名**: `vSecPrimGcmEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: If enabled, the following algorithms can be used:
AES-GCM

########## 5. vSecPrimAesCcmEnabled

- **UUID**: `f54275aa-7104-4503-a30f-50df3688d4b7`
- **参数名**: `vSecPrimAesCcmEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: If enabled, the following algorithms can be used:
AES128-CCM

########## 6. vSecPrimDesEnabled

- **UUID**: `dc5af78c-9e62-4f5b-b758-d40cd8a129f9`
- **参数名**: `vSecPrimDesEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: If enabled, the following algorithm can be used:
DES

########## 7. vSecPrimRC2Enabled

- **UUID**: `ed0abbc3-4b56-4069-bf37-1838e2f9edfc`
- **参数名**: `vSecPrimRC2Enabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: If enabled, the following algorithm can be used:
RC2 (ARC2)

########## 8. vSecPrimTDesEnabled

- **UUID**: `3abfba1d-7182-4a7d-bad5-56486e13a7f4`
- **参数名**: `vSecPrimTDesEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: If enabled, the following algorithm can be used:
TDES (3DES)

########## 9. vSecPrimChaCha20Enabled

- **UUID**: `a5a73d18-b53c-47b4-ad7c-d7e8e934997f`
- **参数名**: `vSecPrimChaCha20Enabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: If enabled, the following algorithm can be used:
ChaCha20

########## 10. vSecPrimAeadChaCha20Poly1305Enabled

- **UUID**: `a06b772a-eb74-40a4-8408-c00d163a7a38`
- **参数名**: `vSecPrimAeadChaCha20Poly1305Enabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: If enabled, the following algorithm can be used:
Aead with ChaCha20 and Poly1305

####### 2. vSecPrimMac

**容器属性**:

- **UUID**: `6316838e-d7f2-429a-a7c0-eb8811f74687`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vSecPrimMac`
- **多重性**: [1..1]
- **构建后可变**: false

**容器描述**:

Container for Mac algorithm configuration.

######## 参数配置

此容器包含 **8** 个参数：

######### BOOLEAN 类型参数

########## 1. vSecPrimSipHashEnabled

- **UUID**: `cb619d98-7330-4a78-a75f-6eea8aedf81c`
- **参数名**: `vSecPrimSipHashEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: If enabled, the following algorithm can be used:
SipHash

########## 2. vSecPrimCmacEnabled

- **UUID**: `f8fa6879-ff95-45eb-9ee7-303410295260`
- **参数名**: `vSecPrimCmacEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: If enabled, the following algorithm can be used:
CMAC

########## 3. vSecPrimHMacSHA1Enabled

- **UUID**: `22778248-cc46-40d2-942c-ff22894d0b3c`
- **参数名**: `vSecPrimHMacSHA1Enabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: If enabled, the following algorithm can be used:
HMac using SHA1 as hash algorithm

########## 4. vSecPrimHMacRMD160Enabled

- **UUID**: `2dc760bb-367c-44b1-84ad-97bdd313b99c`
- **参数名**: `vSecPrimHMacRMD160Enabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: If enabled, the following algorithm can be used:
HMac using RMD160 as hash algorithm

########## 5. vSecPrimHMacSHA2_256Enabled

- **UUID**: `1e18a65d-1d77-4702-87af-60990c1c31eb`
- **参数名**: `vSecPrimHMacSHA2_256Enabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: If enabled, the following algorithm can be used:
HMac using SHA2_256 as hash algorithm

########## 6. vSecPrimGMacEnabled

- **UUID**: `7471fbdf-dbdf-413f-9ac4-154b75891de3`
- **参数名**: `vSecPrimGMacEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: If enabled, the following algorithm can be used:
GMac

########## 7. vSecPrimPoly1305Enabled

- **UUID**: `6cbaa002-c11b-4a7c-9ccc-cfe2ac2036bf`
- **参数名**: `vSecPrimPoly1305Enabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: If enabled, the following algorithm can be used:
Poly1305

########## 8. vSecPrimHMacSHA2_384Enabled

- **UUID**: `1b73d5f0-2bb6-4171-8242-503f7e9ffdea`
- **参数名**: `vSecPrimHMacSHA2_384Enabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: If enabled, the following algorithm can be used:
HMac using SHA2_384 as hash algorithm

##### 5. vSecPrimCipher

**容器属性**:

- **UUID**: `319b3598-8057-464a-a28c-3fc0d134fa88`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vSecPrimCipher`
- **多重性**: [1..1]
- **构建后可变**: false

**容器描述**:

Container for symmetric cipher algorithm configuration.

###### 参数配置

此容器包含 **10** 个参数：

####### BOOLEAN 类型参数

######## 1. vSecPrimAes128Enabled

- **UUID**: `238985cc-c6a7-4bad-bcf4-89bbdbac4a9f`
- **参数名**: `vSecPrimAes128Enabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: If enabled, the following algorithm can be used:
AES128

######## 2. vSecPrimAes192Enabled

- **UUID**: `e9dc7245-1c64-47d7-b3ce-ef716d32b73e`
- **参数名**: `vSecPrimAes192Enabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: If enabled, the following algorithm can be used:
AES192

######## 3. vSecPrimAes256Enabled

- **UUID**: `63e7827d-4d87-4cf7-b73c-ee2c5e93f35e`
- **参数名**: `vSecPrimAes256Enabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: If enabled, the following algorithm can be used:
AES256

######## 4. vSecPrimGcmEnabled

- **UUID**: `c335a626-67d8-4ae6-af0f-5ed01b4d03d9`
- **参数名**: `vSecPrimGcmEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: If enabled, the following algorithms can be used:
AES-GCM

######## 5. vSecPrimAesCcmEnabled

- **UUID**: `f54275aa-7104-4503-a30f-50df3688d4b7`
- **参数名**: `vSecPrimAesCcmEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: If enabled, the following algorithms can be used:
AES128-CCM

######## 6. vSecPrimDesEnabled

- **UUID**: `dc5af78c-9e62-4f5b-b758-d40cd8a129f9`
- **参数名**: `vSecPrimDesEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: If enabled, the following algorithm can be used:
DES

######## 7. vSecPrimRC2Enabled

- **UUID**: `ed0abbc3-4b56-4069-bf37-1838e2f9edfc`
- **参数名**: `vSecPrimRC2Enabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: If enabled, the following algorithm can be used:
RC2 (ARC2)

######## 8. vSecPrimTDesEnabled

- **UUID**: `3abfba1d-7182-4a7d-bad5-56486e13a7f4`
- **参数名**: `vSecPrimTDesEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: If enabled, the following algorithm can be used:
TDES (3DES)

######## 9. vSecPrimChaCha20Enabled

- **UUID**: `a5a73d18-b53c-47b4-ad7c-d7e8e934997f`
- **参数名**: `vSecPrimChaCha20Enabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: If enabled, the following algorithm can be used:
ChaCha20

######## 10. vSecPrimAeadChaCha20Poly1305Enabled

- **UUID**: `a06b772a-eb74-40a4-8408-c00d163a7a38`
- **参数名**: `vSecPrimAeadChaCha20Poly1305Enabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: If enabled, the following algorithm can be used:
Aead with ChaCha20 and Poly1305

##### 6. vSecPrimMac

**容器属性**:

- **UUID**: `6316838e-d7f2-429a-a7c0-eb8811f74687`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vSecPrimMac`
- **多重性**: [1..1]
- **构建后可变**: false

**容器描述**:

Container for Mac algorithm configuration.

###### 参数配置

此容器包含 **8** 个参数：

####### BOOLEAN 类型参数

######## 1. vSecPrimSipHashEnabled

- **UUID**: `cb619d98-7330-4a78-a75f-6eea8aedf81c`
- **参数名**: `vSecPrimSipHashEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: If enabled, the following algorithm can be used:
SipHash

######## 2. vSecPrimCmacEnabled

- **UUID**: `f8fa6879-ff95-45eb-9ee7-303410295260`
- **参数名**: `vSecPrimCmacEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: If enabled, the following algorithm can be used:
CMAC

######## 3. vSecPrimHMacSHA1Enabled

- **UUID**: `22778248-cc46-40d2-942c-ff22894d0b3c`
- **参数名**: `vSecPrimHMacSHA1Enabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: If enabled, the following algorithm can be used:
HMac using SHA1 as hash algorithm

######## 4. vSecPrimHMacRMD160Enabled

- **UUID**: `2dc760bb-367c-44b1-84ad-97bdd313b99c`
- **参数名**: `vSecPrimHMacRMD160Enabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: If enabled, the following algorithm can be used:
HMac using RMD160 as hash algorithm

######## 5. vSecPrimHMacSHA2_256Enabled

- **UUID**: `1e18a65d-1d77-4702-87af-60990c1c31eb`
- **参数名**: `vSecPrimHMacSHA2_256Enabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: If enabled, the following algorithm can be used:
HMac using SHA2_256 as hash algorithm

######## 6. vSecPrimGMacEnabled

- **UUID**: `7471fbdf-dbdf-413f-9ac4-154b75891de3`
- **参数名**: `vSecPrimGMacEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: If enabled, the following algorithm can be used:
GMac

######## 7. vSecPrimPoly1305Enabled

- **UUID**: `6cbaa002-c11b-4a7c-9ccc-cfe2ac2036bf`
- **参数名**: `vSecPrimPoly1305Enabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: If enabled, the following algorithm can be used:
Poly1305

######## 8. vSecPrimHMacSHA2_384Enabled

- **UUID**: `1b73d5f0-2bb6-4171-8242-503f7e9ffdea`
- **参数名**: `vSecPrimHMacSHA2_384Enabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: If enabled, the following algorithm can be used:
HMac using SHA2_384 as hash algorithm

##### 7. vSecPrimAsymmetricAlgorithms

**容器属性**:

- **UUID**: `8aff8b11-332a-4813-86eb-e8ddde4d6871`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vSecPrimAsymmetricAlgorithms`
- **多重性**: [1..1]
- **构建后可变**: false

**容器描述**:

Container for asymmetric algorithm configuration.

###### 配置容器

本模块包含 **5** 个配置容器：

####### 1. vSecPrimSignature

**容器属性**:

- **UUID**: `c7d15e2a-6b2a-4950-9c1e-77c3b2bbd470`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vSecPrimSignature`
- **多重性**: [1..1]
- **构建后可变**: false

**容器描述**:

Container for signature algorithm configuration.

######## 参数配置

此容器包含 **8** 个参数：

######### BOOLEAN 类型参数

########## 1. vSecPrimRSA_PSS_RIPEMD160Enabled

- **UUID**: `b9f8111b-e690-4036-a96f-d9017923b066`
- **参数名**: `vSecPrimRSA_PSS_RIPEMD160Enabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: If enabled, the following algorithm can be used:
RSA Signature Generation / Verification according to PSS using RIPEMD160 as hash function

########## 2. vSecPrimRSA_PSS_SHA1Enabled

- **UUID**: `07626812-137f-4a0b-b11b-f6933039ed7c`
- **参数名**: `vSecPrimRSA_PSS_SHA1Enabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: If enabled, the following algorithm can be used:
RSA Signature Generation / Verification according to PSS using SHA1 as hash function

########## 3. vSecPrimRSA_PSS_SHA2_256Enabled

- **UUID**: `0f0dc14f-ed72-4e24-a07e-22659ba84623`
- **参数名**: `vSecPrimRSA_PSS_SHA2_256Enabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: If enabled, the following algorithm can be used:
RSA Signature Generation / Verification according to PSS using SHA2_256 as hash function

########## 4. vSecPrimRSA_V15_RIPEMD160Enabled

- **UUID**: `b185b824-cb52-40c9-88eb-49f002d1894c`
- **参数名**: `vSecPrimRSA_V15_RIPEMD160Enabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: If enabled, the following algorithm can be used:
RSA Signature Generation / Verification according to RSASSA-PKCS1-v1_5 using RIPEMD160 as hash function

########## 5. vSecPrimRSA_V15_SHA1Enabled

- **UUID**: `6e451db9-f38b-44ae-8acb-24bc3dc41a61`
- **参数名**: `vSecPrimRSA_V15_SHA1Enabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: If enabled, the following algorithm can be used:
RSA Signature Generation / Verification according to RSASSA-PKCS1-v1_5 using SHA1 as hash function

########## 6. vSecPrimRSA_V15_SHA2_256Enabled

- **UUID**: `467791ae-f714-45fa-82a8-2fc79e3235b7`
- **参数名**: `vSecPrimRSA_V15_SHA2_256Enabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: If enabled, the following algorithm can be used:
RSA Signature Generation / Verification according to RSASSA-PKCS1-v1_5 using SHA2_256 as hash function

########## 7. vSecPrimECDSA_25519Enabled

- **UUID**: `63a20750-3940-4821-8237-9bf83349a700`
- **参数名**: `vSecPrimECDSA_25519Enabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: If enabled, the following algorithm can be used:
ECDSA Signature Generation / Verification according to curve ED25519

########## 8. vSecPrimECDSA_GenericEnabled

- **UUID**: `9229d787-5ef3-4691-aeb9-e3f91cdc25bd`
- **参数名**: `vSecPrimECDSA_GenericEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: If enabled, the following algorithm can be used:
ECDSA Signature Generation / Verification using generic curve

####### 2. vSecPrimKeyExchange

**容器属性**:

- **UUID**: `36efc363-4525-4960-9745-014ff4a6f8f5`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vSecPrimKeyExchange`
- **多重性**: [1..1]
- **构建后可变**: false

**容器描述**:

Container for key exchange algorithm configuration.

######## 参数配置

此容器包含 **4** 个参数：

######### BOOLEAN 类型参数

########## 1. vSecPrimECDH_25519Enabled

- **UUID**: `7f1b4292-57d2-4389-b9e5-06a053c3ed9e`
- **参数名**: `vSecPrimECDH_25519Enabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: If enabled, the following algorithm can be used:
ECDH Key Exchange according to curve ED25519

########## 2. vSecPrimECDH_GenericEnabled

- **UUID**: `7d19381a-6330-45a5-b854-a3ff486904b8`
- **参数名**: `vSecPrimECDH_GenericEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: If enabled, the following algorithm can be used:
ECDH Key Exchange using generic curve

########## 3. vSecPrimECBD_GenericEnabled

- **UUID**: `ab991656-478a-44f0-be90-8f19731230c2`
- **参数名**: `vSecPrimECBD_GenericEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: If enabled, the following algorithm can be used:
EC Burmester Desmedt Key Exchange using generic curve

########## 4. vSecPrimSPAKE2pEnabled

- **UUID**: `76fa5f12-b29e-4f9b-a1cd-023cfd92ffa6`
- **参数名**: `vSecPrimSPAKE2pEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: If enabled, the following algorithm can be used:
SPAKE2+ preamble phase
SPAKE2+ Key Exchange using curve SECP256r1, SHA256, HKDF HMAC SHA256 and CMAC AES128

####### 3. vSecPrimKeyDerivation

**容器属性**:

- **UUID**: `71cf92a2-204b-46de-806d-e7576640dc64`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vSecPrimKeyDerivation`
- **多重性**: [1..1]
- **构建后可变**: false

**容器描述**:

Container for key derivation algorithm configuration.

######## 参数配置

此容器包含 **6** 个参数：

######### BOOLEAN 类型参数

########## 1. vSecPrimPKCS5Enabled

- **UUID**: `3b501b28-af6c-414f-a47b-204dd0f72c50`
- **参数名**: `vSecPrimPKCS5Enabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: If enabled, the following algorithm can be used:
Key Derivation according to PKCS5 / KDF2 with underlying primitive HMAC SHA1.

########## 2. vSecPrimANSI_X963Enabled

- **UUID**: `9f7b109c-97ca-4761-8a89-d46c585c8341`
- **参数名**: `vSecPrimANSI_X963Enabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: If enabled, the following algorithm can be used:
Key Derivation according to ANSI X963 SHA1

########## 3. vSecPrimANSI_X963_SHA256Enabled

- **UUID**: `0306920d-18c9-4451-a8be-4c532fc33f36`
- **参数名**: `vSecPrimANSI_X963_SHA256Enabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: If enabled, the following algorithm can be used:
Key Derivation according to ANSI X963 SHA256

########## 4. vSecPrimPKCS5HMacSHA256Enabled

- **UUID**: `ac683523-b4bc-4f04-a287-56e01361fc41`
- **参数名**: `vSecPrimPKCS5HMacSHA256Enabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: If enabled, the following algorithm can be used:
Key Derivation according to PKCS5 / KDF2 with underlying primitive HMAC SHA256.

########## 5. vSecPrimANSI_X963_SHA512Enabled

- **UUID**: `0e939264-8ad0-4ac4-b518-cd13b5ac9400`
- **参数名**: `vSecPrimANSI_X963_SHA512Enabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: If enabled, the following algorithm can be used:
Key Derivation according to ANSI X963 SHA512

########## 6. vSecPrimHKDF_HMAC_SHA256Enabled

- **UUID**: `98b625b4-421c-46c0-b9a8-422a815c8898`
- **参数名**: `vSecPrimHKDF_HMAC_SHA256Enabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: If enabled, the following algorithm can be used:
Key Derivation according to HKDF HMAC SHA256

####### 4. vSecPrimCipher

**容器属性**:

- **UUID**: `7651f40b-2167-4768-8804-99a2f593194a`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vSecPrimCipher`
- **多重性**: [1..1]
- **构建后可变**: false

**容器描述**:

Container for asymmetric cipher algorithm configuration.

######## 参数配置

此容器包含 **3** 个参数：

######### BOOLEAN 类型参数

########## 1. vSecPrimRSA_OAEP_SHA1Enabled

- **UUID**: `27a63a03-13ce-4aa9-88eb-5bfb02652f81`
- **参数名**: `vSecPrimRSA_OAEP_SHA1Enabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: If enabled, the following algorithm can be used:
RSA Asymmetric encryption according to OAEP using SHA1 as hash algorithm

########## 2. vSecPrimRSA_OAEP_SHA2_256Enabled

- **UUID**: `6ae07ed4-a890-49bf-ae38-472b4432b743`
- **参数名**: `vSecPrimRSA_OAEP_SHA2_256Enabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: If enabled, the following algorithm can be used:
RSA Asymmetric encryption according to OAEP using SHA2_256 as hash algorithm

########## 3. vSecPrimRSA_V15Enabled

- **UUID**: `6cd74a94-128e-4fc7-9f32-45ecd13480b3`
- **参数名**: `vSecPrimRSA_V15Enabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: If enabled, the following algorithm can be used:
RSA Asymmetric encryption according to RSASSA-PKCS1-v1_5

####### 5. vSecPrimKeyGeneration

**容器属性**:

- **UUID**: `f1ee49ef-2dd7-4993-9d2d-2d3ecf488829`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vSecPrimKeyGeneration`
- **多重性**: [1..1]
- **构建后可变**: false

**容器描述**:

Container for key generation algorithm configuration.

######## 参数配置

此容器包含 **1** 个参数：

######### BOOLEAN 类型参数

########## 1. vSecPrimECCEnabled

- **UUID**: `6ae62102-ea57-4024-9f9d-6d295f763419`
- **参数名**: `vSecPrimECCEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: If enabled, the following algorithm can be used:
Key Generation using elliptic curves

##### 8. vSecPrimSignature

**容器属性**:

- **UUID**: `c7d15e2a-6b2a-4950-9c1e-77c3b2bbd470`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vSecPrimSignature`
- **多重性**: [1..1]
- **构建后可变**: false

**容器描述**:

Container for signature algorithm configuration.

###### 参数配置

此容器包含 **8** 个参数：

####### BOOLEAN 类型参数

######## 1. vSecPrimRSA_PSS_RIPEMD160Enabled

- **UUID**: `b9f8111b-e690-4036-a96f-d9017923b066`
- **参数名**: `vSecPrimRSA_PSS_RIPEMD160Enabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: If enabled, the following algorithm can be used:
RSA Signature Generation / Verification according to PSS using RIPEMD160 as hash function

######## 2. vSecPrimRSA_PSS_SHA1Enabled

- **UUID**: `07626812-137f-4a0b-b11b-f6933039ed7c`
- **参数名**: `vSecPrimRSA_PSS_SHA1Enabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: If enabled, the following algorithm can be used:
RSA Signature Generation / Verification according to PSS using SHA1 as hash function

######## 3. vSecPrimRSA_PSS_SHA2_256Enabled

- **UUID**: `0f0dc14f-ed72-4e24-a07e-22659ba84623`
- **参数名**: `vSecPrimRSA_PSS_SHA2_256Enabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: If enabled, the following algorithm can be used:
RSA Signature Generation / Verification according to PSS using SHA2_256 as hash function

######## 4. vSecPrimRSA_V15_RIPEMD160Enabled

- **UUID**: `b185b824-cb52-40c9-88eb-49f002d1894c`
- **参数名**: `vSecPrimRSA_V15_RIPEMD160Enabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: If enabled, the following algorithm can be used:
RSA Signature Generation / Verification according to RSASSA-PKCS1-v1_5 using RIPEMD160 as hash function

######## 5. vSecPrimRSA_V15_SHA1Enabled

- **UUID**: `6e451db9-f38b-44ae-8acb-24bc3dc41a61`
- **参数名**: `vSecPrimRSA_V15_SHA1Enabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: If enabled, the following algorithm can be used:
RSA Signature Generation / Verification according to RSASSA-PKCS1-v1_5 using SHA1 as hash function

######## 6. vSecPrimRSA_V15_SHA2_256Enabled

- **UUID**: `467791ae-f714-45fa-82a8-2fc79e3235b7`
- **参数名**: `vSecPrimRSA_V15_SHA2_256Enabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: If enabled, the following algorithm can be used:
RSA Signature Generation / Verification according to RSASSA-PKCS1-v1_5 using SHA2_256 as hash function

######## 7. vSecPrimECDSA_25519Enabled

- **UUID**: `63a20750-3940-4821-8237-9bf83349a700`
- **参数名**: `vSecPrimECDSA_25519Enabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: If enabled, the following algorithm can be used:
ECDSA Signature Generation / Verification according to curve ED25519

######## 8. vSecPrimECDSA_GenericEnabled

- **UUID**: `9229d787-5ef3-4691-aeb9-e3f91cdc25bd`
- **参数名**: `vSecPrimECDSA_GenericEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: If enabled, the following algorithm can be used:
ECDSA Signature Generation / Verification using generic curve

##### 9. vSecPrimKeyExchange

**容器属性**:

- **UUID**: `36efc363-4525-4960-9745-014ff4a6f8f5`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vSecPrimKeyExchange`
- **多重性**: [1..1]
- **构建后可变**: false

**容器描述**:

Container for key exchange algorithm configuration.

###### 参数配置

此容器包含 **4** 个参数：

####### BOOLEAN 类型参数

######## 1. vSecPrimECDH_25519Enabled

- **UUID**: `7f1b4292-57d2-4389-b9e5-06a053c3ed9e`
- **参数名**: `vSecPrimECDH_25519Enabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: If enabled, the following algorithm can be used:
ECDH Key Exchange according to curve ED25519

######## 2. vSecPrimECDH_GenericEnabled

- **UUID**: `7d19381a-6330-45a5-b854-a3ff486904b8`
- **参数名**: `vSecPrimECDH_GenericEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: If enabled, the following algorithm can be used:
ECDH Key Exchange using generic curve

######## 3. vSecPrimECBD_GenericEnabled

- **UUID**: `ab991656-478a-44f0-be90-8f19731230c2`
- **参数名**: `vSecPrimECBD_GenericEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: If enabled, the following algorithm can be used:
EC Burmester Desmedt Key Exchange using generic curve

######## 4. vSecPrimSPAKE2pEnabled

- **UUID**: `76fa5f12-b29e-4f9b-a1cd-023cfd92ffa6`
- **参数名**: `vSecPrimSPAKE2pEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: If enabled, the following algorithm can be used:
SPAKE2+ preamble phase
SPAKE2+ Key Exchange using curve SECP256r1, SHA256, HKDF HMAC SHA256 and CMAC AES128

##### 10. vSecPrimKeyDerivation

**容器属性**:

- **UUID**: `71cf92a2-204b-46de-806d-e7576640dc64`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vSecPrimKeyDerivation`
- **多重性**: [1..1]
- **构建后可变**: false

**容器描述**:

Container for key derivation algorithm configuration.

###### 参数配置

此容器包含 **6** 个参数：

####### BOOLEAN 类型参数

######## 1. vSecPrimPKCS5Enabled

- **UUID**: `3b501b28-af6c-414f-a47b-204dd0f72c50`
- **参数名**: `vSecPrimPKCS5Enabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: If enabled, the following algorithm can be used:
Key Derivation according to PKCS5 / KDF2 with underlying primitive HMAC SHA1.

######## 2. vSecPrimANSI_X963Enabled

- **UUID**: `9f7b109c-97ca-4761-8a89-d46c585c8341`
- **参数名**: `vSecPrimANSI_X963Enabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: If enabled, the following algorithm can be used:
Key Derivation according to ANSI X963 SHA1

######## 3. vSecPrimANSI_X963_SHA256Enabled

- **UUID**: `0306920d-18c9-4451-a8be-4c532fc33f36`
- **参数名**: `vSecPrimANSI_X963_SHA256Enabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: If enabled, the following algorithm can be used:
Key Derivation according to ANSI X963 SHA256

######## 4. vSecPrimPKCS5HMacSHA256Enabled

- **UUID**: `ac683523-b4bc-4f04-a287-56e01361fc41`
- **参数名**: `vSecPrimPKCS5HMacSHA256Enabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: If enabled, the following algorithm can be used:
Key Derivation according to PKCS5 / KDF2 with underlying primitive HMAC SHA256.

######## 5. vSecPrimANSI_X963_SHA512Enabled

- **UUID**: `0e939264-8ad0-4ac4-b518-cd13b5ac9400`
- **参数名**: `vSecPrimANSI_X963_SHA512Enabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: If enabled, the following algorithm can be used:
Key Derivation according to ANSI X963 SHA512

######## 6. vSecPrimHKDF_HMAC_SHA256Enabled

- **UUID**: `98b625b4-421c-46c0-b9a8-422a815c8898`
- **参数名**: `vSecPrimHKDF_HMAC_SHA256Enabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: If enabled, the following algorithm can be used:
Key Derivation according to HKDF HMAC SHA256

##### 11. vSecPrimCipher

**容器属性**:

- **UUID**: `7651f40b-2167-4768-8804-99a2f593194a`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vSecPrimCipher`
- **多重性**: [1..1]
- **构建后可变**: false

**容器描述**:

Container for asymmetric cipher algorithm configuration.

###### 参数配置

此容器包含 **3** 个参数：

####### BOOLEAN 类型参数

######## 1. vSecPrimRSA_OAEP_SHA1Enabled

- **UUID**: `27a63a03-13ce-4aa9-88eb-5bfb02652f81`
- **参数名**: `vSecPrimRSA_OAEP_SHA1Enabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: If enabled, the following algorithm can be used:
RSA Asymmetric encryption according to OAEP using SHA1 as hash algorithm

######## 2. vSecPrimRSA_OAEP_SHA2_256Enabled

- **UUID**: `6ae07ed4-a890-49bf-ae38-472b4432b743`
- **参数名**: `vSecPrimRSA_OAEP_SHA2_256Enabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: If enabled, the following algorithm can be used:
RSA Asymmetric encryption according to OAEP using SHA2_256 as hash algorithm

######## 3. vSecPrimRSA_V15Enabled

- **UUID**: `6cd74a94-128e-4fc7-9f32-45ecd13480b3`
- **参数名**: `vSecPrimRSA_V15Enabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: If enabled, the following algorithm can be used:
RSA Asymmetric encryption according to RSASSA-PKCS1-v1_5

##### 12. vSecPrimKeyGeneration

**容器属性**:

- **UUID**: `f1ee49ef-2dd7-4993-9d2d-2d3ecf488829`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vSecPrimKeyGeneration`
- **多重性**: [1..1]
- **构建后可变**: false

**容器描述**:

Container for key generation algorithm configuration.

###### 参数配置

此容器包含 **1** 个参数：

####### BOOLEAN 类型参数

######## 1. vSecPrimECCEnabled

- **UUID**: `6ae62102-ea57-4024-9f9d-6d295f763419`
- **参数名**: `vSecPrimECCEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: If enabled, the following algorithm can be used:
Key Generation using elliptic curves

##### 13. vSecPrimOptimization

**容器属性**:

- **UUID**: `ee710804-dbdb-4d57-a443-7b97084737de`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vSecPrimOptimization`
- **多重性**: [1..1]
- **构建后可变**: false

**容器描述**:

Container for optimization configuration options.

###### 参数配置

此容器包含 **5** 个参数：

####### ENUMERATION 类型参数

######## 1. vSecPrimAesSpeedUp

- **UUID**: `e6e79b71-8260-461f-b787-ca9c207ddd64`
- **参数名**: `vSecPrimAesSpeedUp`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `SPEED_UP_LEVEL_3`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `SPEED_UP_LEVEL_0`
  - `SPEED_UP_LEVEL_1`
  - `SPEED_UP_LEVEL_2`
  - `SPEED_UP_LEVEL_3`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Defines the optimization level of the Aes algorithms.
The higher the level, the faster the code will be executed at the cost of a higher memory consumption.

######## 2. vSecPrimSha1SpeedUp

- **UUID**: `e8cf334c-242d-41fa-a621-3f3a69b5e975`
- **参数名**: `vSecPrimSha1SpeedUp`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `SPEED_UP_LEVEL_1`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `SPEED_UP_LEVEL_0`
  - `SPEED_UP_LEVEL_1`
  - `SPEED_UP_LEVEL_2`
  - `SPEED_UP_LEVEL_3`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Defines the optimization level of the SHA1 algorithms.
The higher the level, the faster the code will be executed at the cost of a higher memory consumption.

######## 3. vSecPrimSha256SpeedUp

- **UUID**: `a8a1e11c-6fd6-4c70-848a-5b429279b9c9`
- **参数名**: `vSecPrimSha256SpeedUp`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `SPEED_UP_LEVEL_0`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `SPEED_UP_LEVEL_0`
  - `SPEED_UP_LEVEL_1`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Defines the optimization level of the SHA2_256 algorithms.
The higher the level, the faster the code will be executed at the cost of a higher memory consumption.

######## 4. vSecPrimSha512SpeedUp

- **UUID**: `7148a3b1-130f-413e-9d4e-f9b42e7c5ebe`
- **参数名**: `vSecPrimSha512SpeedUp`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `SPEED_UP_LEVEL_0`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `SPEED_UP_LEVEL_0`
  - `SPEED_UP_LEVEL_1`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Defines the optimization level of the SHA2_512 algorithms.
The higher the level, the faster the code will be executed at the cost of a higher memory consumption.

######## 5. vSecPrimChaCha20SpeedUp

- **UUID**: `23f96131-9f02-4dad-9f20-dc435313a649`
- **参数名**: `vSecPrimChaCha20SpeedUp`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `SPEED_UP_LEVEL_1`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `SPEED_UP_LEVEL_0` (来源: Vector Informatik)
  - `SPEED_UP_LEVEL_1` (来源: Vector Informatik)
  - `SPEED_UP_LEVEL_2` (来源: Vector Informatik)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Defines the optimization level of the ChaCha20 algorithms.
The higher the level, the faster the code will be executed at the cost of a higher memory consumption.

##### 14. vSecPrimGeneral

**容器属性**:

- **UUID**: `73280f6a-154c-483b-b28f-dd51fde62f06`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vSecPrimGeneral`
- **多重性**: [1..1]
- **构建后可变**: false

**容器描述**:

Container for common configuration options.

###### 参数配置

此容器包含 **11** 个参数：

####### INTEGER 类型参数

######## 1. vSecPrimDrbgReseedInterval

- **UUID**: `26d6f730-b062-422b-b1ff-9736beddd7f0`
- **参数名**: `vSecPrimDrbgReseedInterval`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `4294967295`
- **取值范围**: [1..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Number of requests for random number generation with CTR DRBG without reseeding.

######## 2. vSecPrimSPAKE2pMaxAADSize

- **UUID**: `5e1f8f6a-4b68-4234-8f16-f25e399928eb`
- **参数名**: `vSecPrimSPAKE2pMaxAADSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `16`
- **取值范围**: [1..8191]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Maximum size of associated data for SPAKE2+ MAC key derivation in bytes. The range is between 0 and (2^13 - 1) bytes.

######## 3. vSecPrimSPAKE2pPreambleOKMLength

- **UUID**: `99c49cd7-5dcf-4a47-b9cc-cb7d9b051366`
- **参数名**: `vSecPrimSPAKE2pPreambleOKMLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `64`
- **取值范围**: [1..65535]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Maximum size of PBKDF output data for SPAKE2+ in the preamble phase in bytes.

####### BOOLEAN 类型参数

######## 1. vSecPrimClearWorkspaceEnabled

- **UUID**: `f43996d0-b586-4ac9-bff5-161a26132ea2`
- **参数名**: `vSecPrimClearWorkspaceEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: If enabled, the workspace is cleared after the processing of any algorithm has finished.

######## 2. vSecPrimSupportUInt64

- **UUID**: `6b202a99-7e12-446d-95ba-c280a5c42151`
- **参数名**: `vSecPrimSupportUInt64`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Distinguish if uint64 is provided on the platform.

####### STRING 类型参数

######## 1. vSecPrimUserConfigFile

- **UUID**: `1a0f5629-dfc3-49cf-8d16-eb2b2a432108`
- **参数名**: `vSecPrimUserConfigFile`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: User configuration file that shall be part of the vSecPrim configuration.
If you want to overwrite or provide own settings in the generated configuration file, you can specify a path to a user defined configuration file. The user defined configuration file will be included at the end of the generated file. Thus definitions in the user defined configuration file can overwrite definitions in the generated configuration file.

####### ENUMERATION 类型参数

######## 1. vSecPrimRSAMaxKeySize

- **UUID**: `70039845-eb08-4218-ae0a-3afbfd56c704`
- **参数名**: `vSecPrimRSAMaxKeySize`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `RSA_MAX_KEY_SIZE_2048`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `RSA_MAX_KEY_SIZE_2048` (来源: Vector Informatik)
  - `RSA_MAX_KEY_SIZE_1024` (来源: Vector Informatik)
  - `RSA_MAX_KEY_SIZE_4096` (来源: Vector Informatik)
  - `RSA_MAX_KEY_SIZE_512` (来源: Vector Informatik)
  - `RSA_MAX_KEY_SIZE_1536` (来源: Vector Informatik)
  - `RSA_MAX_KEY_SIZE_3072` (来源: Vector Informatik)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Maximum key size in Bits which can be used for the RSA algorithms.
The range is from 512 to 4096 Bit.

######## 2. vSecPrimECPMaxKeySize

- **UUID**: `80415f02-6143-4127-8fd9-20ee69d41fd3`
- **参数名**: `vSecPrimECPMaxKeySize`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `ECP_MAX_KEY_SIZE_256`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `ECP_MAX_KEY_SIZE_160` (来源: Vector Informatik)
  - `ECP_MAX_KEY_SIZE_192` (来源: Vector Informatik)
  - `ECP_MAX_KEY_SIZE_224` (来源: Vector Informatik)
  - `ECP_MAX_KEY_SIZE_256` (来源: Vector Informatik)
  - `ECP_MAX_KEY_SIZE_320` (来源: Vector Informatik)
  - `ECP_MAX_KEY_SIZE_384` (来源: Vector Informatik)
  - `ECP_MAX_KEY_SIZE_512` (来源: Vector Informatik)
  - `ECP_MAX_KEY_SIZE_521` (来源: Vector Informatik)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Maximum key size in Bits which can be used for the ECP algorithms.
The range is from 160 to 521 Bit.

######## 3. vSecPrimWatchdogLevel

- **UUID**: `e2db726d-3ba2-427a-a2c6-c92b59dd14ff`
- **参数名**: `vSecPrimWatchdogLevel`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `WD_LEVEL_0`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `WD_LEVEL_0` (来源: Vector Informatik)
  - `WD_LEVEL_1` (来源: Vector Informatik)
  - `WD_LEVEL_2` (来源: Vector Informatik)
  - `WD_LEVEL_3` (来源: Vector Informatik)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Defines the level of watchdog call frequency.
WD_LEVEL_0: WD is disabled
WD_LEVEL_1: WD called from outer functions only
WD_LEVEL_2: WD called from inner functions as well
WD_LEVEL_3: WD also called in inner hash loops

######## 4. vSecPrimSizeOfEsltLength

- **UUID**: `1655df71-67c6-4597-a104-a80e61c643f0`
- **参数名**: `vSecPrimSizeOfEsltLength`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `SIZE_UINT32`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `SIZE_UINT16` (来源: Vector Informatik)
  - `SIZE_UINT32` (来源: Vector Informatik)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Decide which type is used for eslt_Length.
If size is set to uint16 max input length for single update is limitied to 65535 bytes.

######## 5. vSecPrimCTRDRBGAES128SecurityStrength

- **UUID**: `def73ca4-7160-4569-b368-0f5557d01f33`
- **参数名**: `vSecPrimCTRDRBGAES128SecurityStrength`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `SECURITY_STRENGTH_128`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `SECURITY_STRENGTH_112` (来源: Vector Informatik)
  - `SECURITY_STRENGTH_128` (来源: Vector Informatik)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: The security strength determines the minimum entropy input length for CTR DRBG AES128.

## 📦 包结构

此ARXML文件包含 **1** 个包：

### 1. MICROSAR

- **UUID**: `ff55d029-386d-43a2-b3c2-dfef4c7a5e36`
- **包名称**: `MICROSAR`
- **包含元素数量**: 4

#### 包含的元素

##### BSW-IMPLEMENTATION 类型元素

1. **vSecPrim_Impl**

##### ECUC-MODULE-DEF 类型元素

1. **vSecPrim**

##### ECUC-MODULE-CONFIGURATION-VALUES 类型元素

1. **vSecPrim_Pre**
2. **vSecPrim_Rec**

## ⚡ 实现信息

此ARXML文件包含 **1** 个实现：

### 1. vSecPrim_Impl

- **UUID**: `b0e9f4c5-3717-44da-945d-0d1bd52e681b`
- **实现名称**: `vSecPrim_Impl`
- **编程语言**: C
- **软件版本**: 5.02.00
- **供应商ID**: 30
- **代码生成器**: DaVinci Configurator

## ⚙️ 配置信息

此ARXML文件包含 **2** 个配置：

### 1. vSecPrim_Pre

- **UUID**: `7a21be29-e160-40da-88d4-bd3dd4ef4ae1`
- **配置名称**: `vSecPrim_Pre`
- **定义引用**: `/MICROSAR/vSecPrim`

### 2. vSecPrim_Rec

- **UUID**: `854cfbf3-de54-4594-a693-43e96fb89d0a`
- **配置名称**: `vSecPrim_Rec`
- **定义引用**: `/MICROSAR/vSecPrim`
