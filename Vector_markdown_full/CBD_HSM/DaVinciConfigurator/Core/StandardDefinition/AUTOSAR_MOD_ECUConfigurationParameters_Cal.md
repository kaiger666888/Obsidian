# Cal - 完整配置文档

*此文档由ARXML文件自动生成，采用层次化结构展示*

**生成时间**: 2025-06-16 14:51:35

## 📑 目录

- [📄 文件信息](#-文件信息)
- [🔧 模块定义](#-模块定义)
  - [Cal](#cal)
- [📦 包结构](#-包结构)

## 📄 文件信息

### Schema信息
- **Schema位置**: `http://autosar.org/schema/r4.0 AUTOSAR_4-0-3.xsd`
- **命名空间**: `http://autosar.org/schema/r4.0`

## 🔧 模块定义

### 1. Cal

#### 基本信息

- **UUID**: `ECUC:7d9a2d7e-881c-40f3-aa63-27da2ea178ed`
- **模块名称**: `Cal`
- **多重性**: [0..1]
- **支持的变体**:
  - VARIANT-PRE-COMPILE

#### 模块描述

Configuration of the Cal (CryptoAbstractionLibrary) module.

#### 版本历史

共有 **1** 个版本记录：

##### 1. 版本 4.2.0

- **发布日期**: 2011-11-09
- **发布者**: AUTOSAR

*此版本无详细变更记录*

#### 配置容器

本模块包含 **49** 个配置容器：

##### 1. CalAsymDecrypt

**容器属性**:

- **UUID**: `ECUC:c2b02512-1d6f-45ea-b7ad-768fcf8d52f5`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CalAsymDecrypt`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Container for incorporation of AsymDecrypt primitives.

###### 参数配置

此容器包含 **2** 个参数：

####### INTEGER 类型参数

######## 1. CalAsymDecryptMaxCtxBufByteSize

- **UUID**: `ECUC:45ad4d7f-37a2-463c-9059-bb94a312631f`
- **参数名**: `CalAsymDecryptMaxCtxBufByteSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The maximum, in bytes, of all context buffers used in all CPL primitives which implement an asymmetrical decryption.

######## 2. CalAsymDecryptMaxKeySize

- **UUID**: `ECUC:37f98b68-c1e5-4c64-a1dd-cbdf20e4921c`
- **参数名**: `CalAsymDecryptMaxKeySize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The maximum, in bytes, of all key lengths used in all CPL primitives which implement an asymmetrical decryption.

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. CalAsymDecryptConfig

**容器属性**:

- **UUID**: `ECUC:99a7c886-305c-4c91-a2b3-2809b1e11b0f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CalAsymDecryptConfig`
- **多重性**: [0..32]
- **多配置容器**: false

**容器描述**:

Container for configuration of service AsymDecrypt. The container name serves as a symbolic name for the identifier of a service configuration.

######## 参数配置

此容器包含 **2** 个参数：

######### STRING 类型参数

########## 1. CalAsymDecryptInitConfiguration

- **UUID**: `ECUC:606bede9-3ac0-46ba-ad54-6a592891a23f`
- **参数名**: `CalAsymDecryptInitConfiguration`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of a C symbol which contains the configuration of the underlying cryptographic primitive.

########## 2. CalAsymDecryptPrimitiveName

- **UUID**: `ECUC:c1ac42e3-ded0-443c-97a4-f85c1056e8fe`
- **参数名**: `CalAsymDecryptPrimitiveName`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of the cryptographic primitive to use.

##### 2. CalAsymDecryptConfig

**容器属性**:

- **UUID**: `ECUC:99a7c886-305c-4c91-a2b3-2809b1e11b0f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CalAsymDecryptConfig`
- **多重性**: [0..32]
- **多配置容器**: false

**容器描述**:

Container for configuration of service AsymDecrypt. The container name serves as a symbolic name for the identifier of a service configuration.

###### 参数配置

此容器包含 **2** 个参数：

####### STRING 类型参数

######## 1. CalAsymDecryptInitConfiguration

- **UUID**: `ECUC:606bede9-3ac0-46ba-ad54-6a592891a23f`
- **参数名**: `CalAsymDecryptInitConfiguration`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of a C symbol which contains the configuration of the underlying cryptographic primitive.

######## 2. CalAsymDecryptPrimitiveName

- **UUID**: `ECUC:c1ac42e3-ded0-443c-97a4-f85c1056e8fe`
- **参数名**: `CalAsymDecryptPrimitiveName`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of the cryptographic primitive to use.

##### 3. CalAsymEncrypt

**容器属性**:

- **UUID**: `ECUC:6954f702-9bfb-440a-88c5-206dc0e4ad88`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CalAsymEncrypt`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Container for incorporation of AsymEncrypt primitives.

###### 参数配置

此容器包含 **2** 个参数：

####### INTEGER 类型参数

######## 1. CalAsymEncryptMaxCtxBufByteSize

- **UUID**: `ECUC:62990ba6-a5cf-4c9a-8dfe-502071854dd9`
- **参数名**: `CalAsymEncryptMaxCtxBufByteSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The maximum, in bytes, of all context buffers used in all CPL primitives which implement an asymmetrical encryption.

######## 2. CalAsymEncryptMaxKeySize

- **UUID**: `ECUC:b76c9d68-2e6b-4d9f-bbbe-83a60a6a33c2`
- **参数名**: `CalAsymEncryptMaxKeySize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The maximum, in bytes, of all key lengths used in all CPL primitives which implement an asymmetrical encryption.

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. CalAsymEncryptConfig

**容器属性**:

- **UUID**: `ECUC:d591c6b1-f35b-4e4f-8f35-78e78337ddc8`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CalAsymEncryptConfig`
- **多重性**: [0..32]
- **多配置容器**: false

**容器描述**:

Container for configuration of service AsymEncrypt. The container name serves as a symbolic name for the identifier of a service configuration.

######## 参数配置

此容器包含 **2** 个参数：

######### STRING 类型参数

########## 1. CalAsymEncryptInitConfiguration

- **UUID**: `ECUC:8af3dcaa-3c53-4aba-b232-688e52884686`
- **参数名**: `CalAsymEncryptInitConfiguration`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of a C symbol which contains the configuration of the underlying cryptographic primitive.

########## 2. CalAsymEncryptPrimitiveName

- **UUID**: `ECUC:f04729b5-91f1-4f49-b731-c38e7dc94c24`
- **参数名**: `CalAsymEncryptPrimitiveName`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of the cryptographic primitive to use.

##### 4. CalAsymEncryptConfig

**容器属性**:

- **UUID**: `ECUC:d591c6b1-f35b-4e4f-8f35-78e78337ddc8`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CalAsymEncryptConfig`
- **多重性**: [0..32]
- **多配置容器**: false

**容器描述**:

Container for configuration of service AsymEncrypt. The container name serves as a symbolic name for the identifier of a service configuration.

###### 参数配置

此容器包含 **2** 个参数：

####### STRING 类型参数

######## 1. CalAsymEncryptInitConfiguration

- **UUID**: `ECUC:8af3dcaa-3c53-4aba-b232-688e52884686`
- **参数名**: `CalAsymEncryptInitConfiguration`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of a C symbol which contains the configuration of the underlying cryptographic primitive.

######## 2. CalAsymEncryptPrimitiveName

- **UUID**: `ECUC:f04729b5-91f1-4f49-b731-c38e7dc94c24`
- **参数名**: `CalAsymEncryptPrimitiveName`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of the cryptographic primitive to use.

##### 5. CalAsymPrivateKeyExtract

**容器属性**:

- **UUID**: `ECUC:5b3aa5d9-f98e-4d0e-bc37-c5f92692f57d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CalAsymPrivateKeyExtract`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Container for incorporation of AsymPrivateKeyExtract primitives.

###### 参数配置

此容器包含 **2** 个参数：

####### INTEGER 类型参数

######## 1. CalAsymPrivateKeyExtractMaxCtxBufByteSize

- **UUID**: `ECUC:f6cf1905-541b-4174-841a-918e922b90fa`
- **参数名**: `CalAsymPrivateKeyExtractMaxCtxBufByteSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The maximum, in bytes, of all context buffers used in all CPL primitives which implement an asymmetrical private key extraction.

######## 2. CalAsymPrivateKeyExtractMaxKeySize

- **UUID**: `ECUC:a143f0b9-858f-4572-bf2d-5a302030e55d`
- **参数名**: `CalAsymPrivateKeyExtractMaxKeySize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The maximum, in bytes, of all key lengths used in all CPL primitives which implement an asymmetrical private key extraction.

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. CalAsymPrivateKeyExtractConfig

**容器属性**:

- **UUID**: `ECUC:16e8d036-8426-4c55-8b8b-4b37511af318`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CalAsymPrivateKeyExtractConfig`
- **多重性**: [0..32]
- **多配置容器**: false

**容器描述**:

Container for configuration of service AsymPrivateKeyExtract.

######## 参数配置

此容器包含 **2** 个参数：

######### STRING 类型参数

########## 1. CalAsymPrivateKeyExtractInitConfiguration

- **UUID**: `ECUC:51d30aa7-82c1-4fe6-a67c-e5ed2529aacc`
- **参数名**: `CalAsymPrivateKeyExtractInitConfiguration`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of a C symbol which contains the configuration of the underlying cryptographic primitive.

########## 2. CalAsymPrivateKeyExtractPrimitiveName

- **UUID**: `ECUC:9380adbb-5da7-4f62-806e-3bb05608aa91`
- **参数名**: `CalAsymPrivateKeyExtractPrimitiveName`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of the cryptographic primitive to use.

##### 6. CalAsymPrivateKeyExtractConfig

**容器属性**:

- **UUID**: `ECUC:16e8d036-8426-4c55-8b8b-4b37511af318`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CalAsymPrivateKeyExtractConfig`
- **多重性**: [0..32]
- **多配置容器**: false

**容器描述**:

Container for configuration of service AsymPrivateKeyExtract.

###### 参数配置

此容器包含 **2** 个参数：

####### STRING 类型参数

######## 1. CalAsymPrivateKeyExtractInitConfiguration

- **UUID**: `ECUC:51d30aa7-82c1-4fe6-a67c-e5ed2529aacc`
- **参数名**: `CalAsymPrivateKeyExtractInitConfiguration`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of a C symbol which contains the configuration of the underlying cryptographic primitive.

######## 2. CalAsymPrivateKeyExtractPrimitiveName

- **UUID**: `ECUC:9380adbb-5da7-4f62-806e-3bb05608aa91`
- **参数名**: `CalAsymPrivateKeyExtractPrimitiveName`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of the cryptographic primitive to use.

##### 7. CalAsymPrivateKeyWrapAsym

**容器属性**:

- **UUID**: `ECUC:16b1dc6b-a36e-449c-80dd-42b1849f7d26`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CalAsymPrivateKeyWrapAsym`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Container for incorporation of AsymPrivateKeyWrapAsym primitives.

###### 参数配置

此容器包含 **2** 个参数：

####### INTEGER 类型参数

######## 1. CalAsymPrivateKeyWrapAsymMaxPrivKeySize

- **UUID**: `ECUC:731f5d40-bd32-42c9-a424-e1ebfa814a99`
- **参数名**: `CalAsymPrivateKeyWrapAsymMaxPrivKeySize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The maximum length, in bytes, of all private information types used in all CPL primitives which implement an asymmetrical key wrapping.

######## 2. CalAsymPrivateKeyWrapAsymMaxPubKeySize

- **UUID**: `ECUC:9995d79e-d314-4c42-bd2e-faae5d1e332b`
- **参数名**: `CalAsymPrivateKeyWrapAsymMaxPubKeySize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The maximum length, in bytes, of all public key types used in all CPL primitives which implement an asymmetrical key wrapping.

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. CalAsymPrivateKeyWrapAsymConfig

**容器属性**:

- **UUID**: `ECUC:f62dd31b-d9cd-420f-a2f0-030fd25de322`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CalAsymPrivateKeyWrapAsymConfig`
- **多重性**: [0..32]
- **多配置容器**: false

**容器描述**:

Container for configuration of service AsymPrivateKeyWrapAsym.

######## 参数配置

此容器包含 **2** 个参数：

######### STRING 类型参数

########## 1. CalAsymPrivateKeyWrapAsymInitConfiguration

- **UUID**: `ECUC:2358ab88-4336-40c3-879e-4283e5e86e7d`
- **参数名**: `CalAsymPrivateKeyWrapAsymInitConfiguration`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of a C symbol which contains the configuration of the underlying cryptographic primitive.

########## 2. CalAsymPrivateKeyWrapAsymPrimitiveName

- **UUID**: `ECUC:db5be4a1-bfdc-43ed-924e-c6f5d4bc7cce`
- **参数名**: `CalAsymPrivateKeyWrapAsymPrimitiveName`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of the cryptographic primitive to use.

##### 8. CalAsymPrivateKeyWrapAsymConfig

**容器属性**:

- **UUID**: `ECUC:f62dd31b-d9cd-420f-a2f0-030fd25de322`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CalAsymPrivateKeyWrapAsymConfig`
- **多重性**: [0..32]
- **多配置容器**: false

**容器描述**:

Container for configuration of service AsymPrivateKeyWrapAsym.

###### 参数配置

此容器包含 **2** 个参数：

####### STRING 类型参数

######## 1. CalAsymPrivateKeyWrapAsymInitConfiguration

- **UUID**: `ECUC:2358ab88-4336-40c3-879e-4283e5e86e7d`
- **参数名**: `CalAsymPrivateKeyWrapAsymInitConfiguration`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of a C symbol which contains the configuration of the underlying cryptographic primitive.

######## 2. CalAsymPrivateKeyWrapAsymPrimitiveName

- **UUID**: `ECUC:db5be4a1-bfdc-43ed-924e-c6f5d4bc7cce`
- **参数名**: `CalAsymPrivateKeyWrapAsymPrimitiveName`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of the cryptographic primitive to use.

##### 9. CalAsymPrivateKeyWrapSym

**容器属性**:

- **UUID**: `ECUC:0318a2c1-136c-44e3-bff5-5594777d79b8`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CalAsymPrivateKeyWrapSym`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Container for incorporation of AsymPrivateKeyWrapSym primitives.

###### 参数配置

此容器包含 **2** 个参数：

####### INTEGER 类型参数

######## 1. CalAsymPrivateKeyWrapSymMaxPrivKeySize

- **UUID**: `ECUC:46859cd1-3c15-471b-90b5-b73dc47e103f`
- **参数名**: `CalAsymPrivateKeyWrapSymMaxPrivKeySize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The maximum length, in bytes, of all private information types used in all CPL primitives which implement an asymmetrical key wrapping.

######## 2. CalAsymPrivateKeyWrapSymMaxSymKeySize

- **UUID**: `ECUC:07b7d500-164d-4248-9e7e-edb9948c45ab`
- **参数名**: `CalAsymPrivateKeyWrapSymMaxSymKeySize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The maximum, in bytes, of all key lengths used in all CPL primitives which implement an asymmetrical key wrapping.

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. CalAsymPrivateKeyWrapSymConfig

**容器属性**:

- **UUID**: `ECUC:141dc2be-aa87-48f1-9d9d-a84104b9dcb5`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CalAsymPrivateKeyWrapSymConfig`
- **多重性**: [0..32]
- **多配置容器**: false

**容器描述**:

Container for configuration of service AsymPrivateKeyWrapSym.

######## 参数配置

此容器包含 **2** 个参数：

######### STRING 类型参数

########## 1. CalAsymPrivateKeyWrapSymInitConfiguration

- **UUID**: `ECUC:93df8c89-92b7-433a-983d-b69f175725b8`
- **参数名**: `CalAsymPrivateKeyWrapSymInitConfiguration`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of a C symbol which contains the configuration of the underlying cryptographic primitive.

########## 2. CalAsymPrivateKeyWrapSymPrimitiveName

- **UUID**: `ECUC:8e62c3ed-c8af-4ab0-88c8-c5432d054cc0`
- **参数名**: `CalAsymPrivateKeyWrapSymPrimitiveName`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of the cryptographic primitive to use.

##### 10. CalAsymPrivateKeyWrapSymConfig

**容器属性**:

- **UUID**: `ECUC:141dc2be-aa87-48f1-9d9d-a84104b9dcb5`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CalAsymPrivateKeyWrapSymConfig`
- **多重性**: [0..32]
- **多配置容器**: false

**容器描述**:

Container for configuration of service AsymPrivateKeyWrapSym.

###### 参数配置

此容器包含 **2** 个参数：

####### STRING 类型参数

######## 1. CalAsymPrivateKeyWrapSymInitConfiguration

- **UUID**: `ECUC:93df8c89-92b7-433a-983d-b69f175725b8`
- **参数名**: `CalAsymPrivateKeyWrapSymInitConfiguration`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of a C symbol which contains the configuration of the underlying cryptographic primitive.

######## 2. CalAsymPrivateKeyWrapSymPrimitiveName

- **UUID**: `ECUC:8e62c3ed-c8af-4ab0-88c8-c5432d054cc0`
- **参数名**: `CalAsymPrivateKeyWrapSymPrimitiveName`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of the cryptographic primitive to use.

##### 11. CalAsymPublicKeyExtract

**容器属性**:

- **UUID**: `ECUC:ef7bcb3c-d009-4fb0-bf83-9e85b44d69d1`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CalAsymPublicKeyExtract`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Container for incorporation of AsymPublicKeyExtract primitives.

###### 参数配置

此容器包含 **2** 个参数：

####### INTEGER 类型参数

######## 1. CalAsymPublicKeyExtractMaxCtxBufByteSize

- **UUID**: `ECUC:a6658840-f5d9-4fcc-b794-38bc510e163c`
- **参数名**: `CalAsymPublicKeyExtractMaxCtxBufByteSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The maximum, in bytes, of all context buffers used in all CPL primitives which implement an asymmetrical public key extraction.

######## 2. CalAsymPublicKeyExtractMaxKeySize

- **UUID**: `ECUC:42bc63da-a495-4225-955b-df4cef36d944`
- **参数名**: `CalAsymPublicKeyExtractMaxKeySize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The maximum, in bytes, of all key lengths used in all CPL primitives which implement an asymmetrical public key extraction.

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. CalAsymPublicKeyExtractConfig

**容器属性**:

- **UUID**: `ECUC:86c587fa-6f48-4a6e-88fb-10c1d3004813`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CalAsymPublicKeyExtractConfig`
- **多重性**: [0..32]
- **多配置容器**: false

**容器描述**:

Container for configuration of service AsymPublicKeyExtract.

######## 参数配置

此容器包含 **2** 个参数：

######### STRING 类型参数

########## 1. CalAsymPublicKeyExtractInitConfiguration

- **UUID**: `ECUC:8e447d12-d852-4079-9463-50d421db4f46`
- **参数名**: `CalAsymPublicKeyExtractInitConfiguration`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of a C symbol which contains the configuration of the underlying cryptographic primitive.

########## 2. CalAsymPublicKeyExtractPrimitiveName

- **UUID**: `ECUC:69167f65-fab4-4252-9f3b-bbbca9e55543`
- **参数名**: `CalAsymPublicKeyExtractPrimitiveName`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of the cryptographic primitive to use.

##### 12. CalAsymPublicKeyExtractConfig

**容器属性**:

- **UUID**: `ECUC:86c587fa-6f48-4a6e-88fb-10c1d3004813`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CalAsymPublicKeyExtractConfig`
- **多重性**: [0..32]
- **多配置容器**: false

**容器描述**:

Container for configuration of service AsymPublicKeyExtract.

###### 参数配置

此容器包含 **2** 个参数：

####### STRING 类型参数

######## 1. CalAsymPublicKeyExtractInitConfiguration

- **UUID**: `ECUC:8e447d12-d852-4079-9463-50d421db4f46`
- **参数名**: `CalAsymPublicKeyExtractInitConfiguration`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of a C symbol which contains the configuration of the underlying cryptographic primitive.

######## 2. CalAsymPublicKeyExtractPrimitiveName

- **UUID**: `ECUC:69167f65-fab4-4252-9f3b-bbbca9e55543`
- **参数名**: `CalAsymPublicKeyExtractPrimitiveName`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of the cryptographic primitive to use.

##### 13. CalChecksum

**容器属性**:

- **UUID**: `ECUC:b8d7b754-116e-4061-bbd5-f1584bf62d30`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CalChecksum`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Container for incorporation of Checksum primitives.

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. CalChecksumMaxCtxBufByteSize

- **UUID**: `ECUC:cdf72f4b-e20e-44ca-ad1d-ec93104d1ae5`
- **参数名**: `CalChecksumMaxCtxBufByteSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The maximum, in bytes, of all context buffers used in all CPL primitives which implement a checksum computation.

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. CalChecksumConfig

**容器属性**:

- **UUID**: `ECUC:0c67f22b-47c0-4f61-846e-034d26e89538`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CalChecksumConfig`
- **多重性**: [0..32]
- **多配置容器**: false

**容器描述**:

Container for configuration of service Checksum. The container name serves as a symbolic name for the identifier of a service configuration.

######## 参数配置

此容器包含 **2** 个参数：

######### STRING 类型参数

########## 1. CalChecksumInitConfiguration

- **UUID**: `ECUC:eede1f61-32c3-48e0-b59a-78e21dbcd3b6`
- **参数名**: `CalChecksumInitConfiguration`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of a C symbol which contains the configuration of the underlying cryptographic primitive.

########## 2. CalChecksumPrimitiveName

- **UUID**: `ECUC:0c102bf1-a9c2-496a-8f51-c6dadd85fa50`
- **参数名**: `CalChecksumPrimitiveName`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of the cryptographic primitive to use.

##### 14. CalChecksumConfig

**容器属性**:

- **UUID**: `ECUC:0c67f22b-47c0-4f61-846e-034d26e89538`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CalChecksumConfig`
- **多重性**: [0..32]
- **多配置容器**: false

**容器描述**:

Container for configuration of service Checksum. The container name serves as a symbolic name for the identifier of a service configuration.

###### 参数配置

此容器包含 **2** 个参数：

####### STRING 类型参数

######## 1. CalChecksumInitConfiguration

- **UUID**: `ECUC:eede1f61-32c3-48e0-b59a-78e21dbcd3b6`
- **参数名**: `CalChecksumInitConfiguration`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of a C symbol which contains the configuration of the underlying cryptographic primitive.

######## 2. CalChecksumPrimitiveName

- **UUID**: `ECUC:0c102bf1-a9c2-496a-8f51-c6dadd85fa50`
- **参数名**: `CalChecksumPrimitiveName`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of the cryptographic primitive to use.

##### 15. CalGeneral

**容器属性**:

- **UUID**: `ECUC:7d813e6d-d38d-48d4-bfff-a46f8ec6f674`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CalGeneral`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

Container for common configuration options.

###### 参数配置

此容器包含 **1** 个参数：

####### STRING 类型参数

######## 1. CalMaxAlignScalarType

- **UUID**: `ECUC:1ca75bb2-f39f-4655-97e9-10f2b129ea52`
- **参数名**: `CalMaxAlignScalarType`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The scalar type which has the maximum alignment restrictions on the given platform.

##### 16. CalHash

**容器属性**:

- **UUID**: `ECUC:983a4ad8-fe68-429b-8127-2d43c16b729a`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CalHash`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Container for incorporation of Hash primitives.

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. CalHashMaxCtxBufByteSize

- **UUID**: `ECUC:eda55c7c-5886-4134-aba2-4009777fe1e6`
- **参数名**: `CalHashMaxCtxBufByteSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The maximum, in bytes, of all context buffers used in all CPL primitives which implement a hash computation.

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. CalHashConfig

**容器属性**:

- **UUID**: `ECUC:afb56866-a648-48f6-b0bd-a6aa913291fc`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CalHashConfig`
- **多重性**: [0..32]
- **多配置容器**: false

**容器描述**:

Configurations for the Hash service. The container name serves as a symbolic name for the identifier of a service configuration.

######## 参数配置

此容器包含 **2** 个参数：

######### STRING 类型参数

########## 1. CalHashInitConfiguration

- **UUID**: `ECUC:a506efe9-dc26-45e1-80bc-331dda93fa54`
- **参数名**: `CalHashInitConfiguration`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of a C symbol which contains the configuration of the underlying cryptographic primitive.

########## 2. CalHashPrimitiveName

- **UUID**: `ECUC:d7df6a25-8d30-4b48-894d-9656b5069286`
- **参数名**: `CalHashPrimitiveName`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of the cryptographic primitive to use.

##### 17. CalHashConfig

**容器属性**:

- **UUID**: `ECUC:afb56866-a648-48f6-b0bd-a6aa913291fc`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CalHashConfig`
- **多重性**: [0..32]
- **多配置容器**: false

**容器描述**:

Configurations for the Hash service. The container name serves as a symbolic name for the identifier of a service configuration.

###### 参数配置

此容器包含 **2** 个参数：

####### STRING 类型参数

######## 1. CalHashInitConfiguration

- **UUID**: `ECUC:a506efe9-dc26-45e1-80bc-331dda93fa54`
- **参数名**: `CalHashInitConfiguration`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of a C symbol which contains the configuration of the underlying cryptographic primitive.

######## 2. CalHashPrimitiveName

- **UUID**: `ECUC:d7df6a25-8d30-4b48-894d-9656b5069286`
- **参数名**: `CalHashPrimitiveName`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of the cryptographic primitive to use.

##### 18. CalKeyDerive

**容器属性**:

- **UUID**: `ECUC:1cb9ff39-036d-4c46-b893-27ae38c17605`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CalKeyDerive`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Container for incorporation of KeyDerive primitives.

###### 参数配置

此容器包含 **2** 个参数：

####### INTEGER 类型参数

######## 1. CalKeyDeriveMaxCtxBufByteSize

- **UUID**: `ECUC:8711c8bc-3725-430f-a77f-5032e64fc4c6`
- **参数名**: `CalKeyDeriveMaxCtxBufByteSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The maximum, in bytes, of all context buffers used in all CPL primitives which implement a key derivation.

######## 2. CalKeyDeriveMaxKeySize

- **UUID**: `ECUC:95db1898-c86b-4a72-b725-a59364466ddc`
- **参数名**: `CalKeyDeriveMaxKeySize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The maximum, in bytes, of all key lengths used in all CRL primitives which implement a key derivation.

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. CalKeyDeriveConfig

**容器属性**:

- **UUID**: `ECUC:c8ca5182-81f1-4ccd-85fb-2ac691f4f63e`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CalKeyDeriveConfig`
- **多重性**: [0..32]
- **多配置容器**: false

**容器描述**:

Container for configuration of service KeyDerive. The container name serves as a symbolic name for the identifier of a service configuration.

######## 参数配置

此容器包含 **2** 个参数：

######### STRING 类型参数

########## 1. CalKeyDeriveInitConfiguration

- **UUID**: `ECUC:060790a3-40f7-4417-9b92-dde48d01fc13`
- **参数名**: `CalKeyDeriveInitConfiguration`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of a C symbol which contains the configuration of the underlying cryptographic primitive.

########## 2. CalKeyDerivePrimitiveName

- **UUID**: `ECUC:974fe581-b127-46bc-9948-c9aa70ad000e`
- **参数名**: `CalKeyDerivePrimitiveName`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of the cryptographic primitive to use.

##### 19. CalKeyDeriveConfig

**容器属性**:

- **UUID**: `ECUC:c8ca5182-81f1-4ccd-85fb-2ac691f4f63e`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CalKeyDeriveConfig`
- **多重性**: [0..32]
- **多配置容器**: false

**容器描述**:

Container for configuration of service KeyDerive. The container name serves as a symbolic name for the identifier of a service configuration.

###### 参数配置

此容器包含 **2** 个参数：

####### STRING 类型参数

######## 1. CalKeyDeriveInitConfiguration

- **UUID**: `ECUC:060790a3-40f7-4417-9b92-dde48d01fc13`
- **参数名**: `CalKeyDeriveInitConfiguration`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of a C symbol which contains the configuration of the underlying cryptographic primitive.

######## 2. CalKeyDerivePrimitiveName

- **UUID**: `ECUC:974fe581-b127-46bc-9948-c9aa70ad000e`
- **参数名**: `CalKeyDerivePrimitiveName`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of the cryptographic primitive to use.

##### 20. CalKeyExchangeCalcPubVal

**容器属性**:

- **UUID**: `ECUC:54f59a16-893f-49ea-94fe-c0d105975e3c`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CalKeyExchangeCalcPubVal`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Container for incorporation of KeyExchangeCalcPubVal primitives.

###### 参数配置

此容器包含 **3** 个参数：

####### INTEGER 类型参数

######## 1. CalKeyExchangeCalcPubValMaxBaseTypeSize

- **UUID**: `ECUC:d2abb09c-c27e-4e44-a3b3-14cb736f3db9`
- **参数名**: `CalKeyExchangeCalcPubValMaxBaseTypeSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The maximum length, in bytes, of all base types used in all CPL primitives which implement a public value calculation.

######## 2. CalKeyExchangeCalcPubValMaxCtxBufByteSize

- **UUID**: `ECUC:09388930-896a-40d7-95f5-3f48731a6cd6`
- **参数名**: `CalKeyExchangeCalcPubValMaxCtxBufByteSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The maximum, in bytes, of all context buffers used in all CPL primitives which implement a public value calculation.

######## 3. CalKeyExchangeCalcPubValMaxPrivateTypeSize

- **UUID**: `ECUC:342d08b4-37f6-403a-93a1-445ae3c2a31d`
- **参数名**: `CalKeyExchangeCalcPubValMaxPrivateTypeSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The maximum length, in bytes, of all private information types used in all CPL primitives which implement a public value calculation.

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. CalKeyExchangeCalcPubValConfig

**容器属性**:

- **UUID**: `ECUC:6047f1e3-150c-4062-9de5-83009e98ed29`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CalKeyExchangeCalcPubValConfig`
- **多重性**: [0..32]
- **多配置容器**: false

**容器描述**:

Container for configuration of service KeyExchangeCalcPubVal. The container name serves as a symbolic name for the identifier of a service configuration.

######## 参数配置

此容器包含 **2** 个参数：

######### STRING 类型参数

########## 1. CalKeyExchangeCalcPubValInitConfiguration

- **UUID**: `ECUC:c9fea318-8a6d-4693-a210-ee67f39d8b83`
- **参数名**: `CalKeyExchangeCalcPubValInitConfiguration`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of a C symbol which contains the configuration of the underlying cryptographic primitive.

########## 2. CalKeyExchangeCalcPubValPrimitiveName

- **UUID**: `ECUC:9998d915-e42e-4458-a051-82fcc6179f74`
- **参数名**: `CalKeyExchangeCalcPubValPrimitiveName`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of the cryptographic primitive to use.

##### 21. CalKeyExchangeCalcPubValConfig

**容器属性**:

- **UUID**: `ECUC:6047f1e3-150c-4062-9de5-83009e98ed29`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CalKeyExchangeCalcPubValConfig`
- **多重性**: [0..32]
- **多配置容器**: false

**容器描述**:

Container for configuration of service KeyExchangeCalcPubVal. The container name serves as a symbolic name for the identifier of a service configuration.

###### 参数配置

此容器包含 **2** 个参数：

####### STRING 类型参数

######## 1. CalKeyExchangeCalcPubValInitConfiguration

- **UUID**: `ECUC:c9fea318-8a6d-4693-a210-ee67f39d8b83`
- **参数名**: `CalKeyExchangeCalcPubValInitConfiguration`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of a C symbol which contains the configuration of the underlying cryptographic primitive.

######## 2. CalKeyExchangeCalcPubValPrimitiveName

- **UUID**: `ECUC:9998d915-e42e-4458-a051-82fcc6179f74`
- **参数名**: `CalKeyExchangeCalcPubValPrimitiveName`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of the cryptographic primitive to use.

##### 22. CalKeyExchangeCalcSecret

**容器属性**:

- **UUID**: `ECUC:0bbf5f7e-f757-48ab-990b-b49b938aa477`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CalKeyExchangeCalcSecret`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Container for incorporation of KeyExchangeCalcSecret primitives.

###### 参数配置

此容器包含 **3** 个参数：

####### INTEGER 类型参数

######## 1. CalKeyExchangeCalcSecretMaxBaseTypeSize

- **UUID**: `ECUC:9202d352-3dd7-478b-a9f1-0a7331eda4d2`
- **参数名**: `CalKeyExchangeCalcSecretMaxBaseTypeSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The maximum length, in bytes, of all base types used in all CPL primitives which implement a shared secret calculation.

######## 2. CalKeyExchangeCalcSecretMaxCtxBufByteSize

- **UUID**: `ECUC:5299e2f5-c14f-4acf-97e9-58fe7847a70f`
- **参数名**: `CalKeyExchangeCalcSecretMaxCtxBufByteSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The maximum, in bytes, of all context buffers used in all CPL primitives which implement a shared secret calculation.

######## 3. CalKeyExchangeCalcSecretMaxPrivateTypeSize

- **UUID**: `ECUC:961c6c12-62ed-4535-bda4-7c915ff4befa`
- **参数名**: `CalKeyExchangeCalcSecretMaxPrivateTypeSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The maximum length, in bytes, of all private information types used in all CPL primitives which implement a shared secret calculation.

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. CalKeyExchangeCalcSecretConfig

**容器属性**:

- **UUID**: `ECUC:505681d9-7848-4817-80af-ae6cb5fe77d1`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CalKeyExchangeCalcSecretConfig`
- **多重性**: [0..32]
- **多配置容器**: false

**容器描述**:

Container for configuration of service KeyExchangeCalcSecret. The container name serves as a symbolic name for the identifier of a service configuration.

######## 参数配置

此容器包含 **2** 个参数：

######### STRING 类型参数

########## 1. CalKeyExchangeCalcSecretInitConfiguration

- **UUID**: `ECUC:1ace766d-4d32-401c-b0f6-20f707f099cf`
- **参数名**: `CalKeyExchangeCalcSecretInitConfiguration`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of a C symbol which contains the configuration of the underlying cryptographic primitive.

########## 2. CalKeyExchangeCalcSecretPrimitiveName

- **UUID**: `ECUC:ae74d778-36b0-45ed-a5bd-6c9e3ebd669e`
- **参数名**: `CalKeyExchangeCalcSecretPrimitiveName`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of the cryptographic primitive to use.

##### 23. CalKeyExchangeCalcSecretConfig

**容器属性**:

- **UUID**: `ECUC:505681d9-7848-4817-80af-ae6cb5fe77d1`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CalKeyExchangeCalcSecretConfig`
- **多重性**: [0..32]
- **多配置容器**: false

**容器描述**:

Container for configuration of service KeyExchangeCalcSecret. The container name serves as a symbolic name for the identifier of a service configuration.

###### 参数配置

此容器包含 **2** 个参数：

####### STRING 类型参数

######## 1. CalKeyExchangeCalcSecretInitConfiguration

- **UUID**: `ECUC:1ace766d-4d32-401c-b0f6-20f707f099cf`
- **参数名**: `CalKeyExchangeCalcSecretInitConfiguration`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of a C symbol which contains the configuration of the underlying cryptographic primitive.

######## 2. CalKeyExchangeCalcSecretPrimitiveName

- **UUID**: `ECUC:ae74d778-36b0-45ed-a5bd-6c9e3ebd669e`
- **参数名**: `CalKeyExchangeCalcSecretPrimitiveName`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of the cryptographic primitive to use.

##### 24. CalMacGenerate

**容器属性**:

- **UUID**: `ECUC:d88ab491-979c-4e5f-b986-41b9492056d9`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CalMacGenerate`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Container for incorporation of MacGenerate primitives.

###### 参数配置

此容器包含 **2** 个参数：

####### INTEGER 类型参数

######## 1. CalMacGenerateMaxCtxBufByteSize

- **UUID**: `ECUC:ab6c8df7-5d9b-4774-9fbd-3d129c1a9722`
- **参数名**: `CalMacGenerateMaxCtxBufByteSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The maximum, in bytes, of all context buffers used in all CPL primitives which implement a MAC generation.

######## 2. CalMacGenerateMaxKeySize

- **UUID**: `ECUC:0a380b91-ee5e-4e17-9e18-34d356fdc74d`
- **参数名**: `CalMacGenerateMaxKeySize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The maximum, in bytes, of all key lengths used in all CPL primitives which implement a MAC generation.

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. CalMacGenerateConfig

**容器属性**:

- **UUID**: `ECUC:676e518e-d86e-423e-a684-c6092b48bd23`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CalMacGenerateConfig`
- **多重性**: [0..32]
- **多配置容器**: false

**容器描述**:

Configurations for the MacGenerate service. The container name serves as a symbolic name for the identifier of a service configuration.

######## 参数配置

此容器包含 **2** 个参数：

######### STRING 类型参数

########## 1. CalMacGenerateInitConfiguration

- **UUID**: `ECUC:56919315-3e9b-4690-b498-816f55155234`
- **参数名**: `CalMacGenerateInitConfiguration`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of a C symbol which contains the configuration of the underlying cryptographic primitive.

########## 2. CalMacGeneratePrimitiveName

- **UUID**: `ECUC:63570cda-923b-40a7-80af-ae1603d2caf6`
- **参数名**: `CalMacGeneratePrimitiveName`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of the cryptographic primitive to use.

##### 25. CalMacGenerateConfig

**容器属性**:

- **UUID**: `ECUC:676e518e-d86e-423e-a684-c6092b48bd23`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CalMacGenerateConfig`
- **多重性**: [0..32]
- **多配置容器**: false

**容器描述**:

Configurations for the MacGenerate service. The container name serves as a symbolic name for the identifier of a service configuration.

###### 参数配置

此容器包含 **2** 个参数：

####### STRING 类型参数

######## 1. CalMacGenerateInitConfiguration

- **UUID**: `ECUC:56919315-3e9b-4690-b498-816f55155234`
- **参数名**: `CalMacGenerateInitConfiguration`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of a C symbol which contains the configuration of the underlying cryptographic primitive.

######## 2. CalMacGeneratePrimitiveName

- **UUID**: `ECUC:63570cda-923b-40a7-80af-ae1603d2caf6`
- **参数名**: `CalMacGeneratePrimitiveName`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of the cryptographic primitive to use.

##### 26. CalMacVerify

**容器属性**:

- **UUID**: `ECUC:9afc6b54-3bc5-49a6-ad92-3354c2a9e09a`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CalMacVerify`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Container for incorporation of MacVerify primitives.

###### 参数配置

此容器包含 **2** 个参数：

####### INTEGER 类型参数

######## 1. CalMacVerifyMaxCtxBufByteSize

- **UUID**: `ECUC:1b823ea2-7e54-404f-add3-e42389e881a4`
- **参数名**: `CalMacVerifyMaxCtxBufByteSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The maximum, in bytes, of all context buffers used in all CPL primitives which implement a MAC verification.

######## 2. CalMacVerifyMaxKeySize

- **UUID**: `ECUC:429c9ad2-bafe-49a8-8899-3d75f0fa8517`
- **参数名**: `CalMacVerifyMaxKeySize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The maximum, in bytes, of all key lengths used in all CPL primitives which implement a MAC verification.

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. CalMacVerifyConfig

**容器属性**:

- **UUID**: `ECUC:04c7c28a-81e5-4a06-97f4-a44aef32279d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CalMacVerifyConfig`
- **多重性**: [0..32]
- **多配置容器**: false

**容器描述**:

Container for configuration of service MacVerify. The container name serves as a symbolic name for the identifier of a service configuration.

######## 参数配置

此容器包含 **2** 个参数：

######### STRING 类型参数

########## 1. CalMacVerifyInitConfiguration

- **UUID**: `ECUC:0db6135a-2ecd-414c-af07-bcff544557b2`
- **参数名**: `CalMacVerifyInitConfiguration`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of a C symbol which contains the configuration of the underlying cryptographic primitive.

########## 2. CalMacVerifyPrimitiveName

- **UUID**: `ECUC:8849e93f-e34c-407c-bcbf-d475291d2981`
- **参数名**: `CalMacVerifyPrimitiveName`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of the cryptographic primitive to use.

##### 27. CalMacVerifyConfig

**容器属性**:

- **UUID**: `ECUC:04c7c28a-81e5-4a06-97f4-a44aef32279d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CalMacVerifyConfig`
- **多重性**: [0..32]
- **多配置容器**: false

**容器描述**:

Container for configuration of service MacVerify. The container name serves as a symbolic name for the identifier of a service configuration.

###### 参数配置

此容器包含 **2** 个参数：

####### STRING 类型参数

######## 1. CalMacVerifyInitConfiguration

- **UUID**: `ECUC:0db6135a-2ecd-414c-af07-bcff544557b2`
- **参数名**: `CalMacVerifyInitConfiguration`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of a C symbol which contains the configuration of the underlying cryptographic primitive.

######## 2. CalMacVerifyPrimitiveName

- **UUID**: `ECUC:8849e93f-e34c-407c-bcbf-d475291d2981`
- **参数名**: `CalMacVerifyPrimitiveName`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of the cryptographic primitive to use.

##### 28. CalRandomGenerate

**容器属性**:

- **UUID**: `ECUC:15c9bbec-fd88-4744-8563-e8b245477cae`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CalRandomGenerate`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Container for incorporation of RandomGenerate primitives.

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. CalRandomGenerateConfig

**容器属性**:

- **UUID**: `ECUC:3be06fd3-a46d-42a6-a6e7-83c3da56547e`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CalRandomGenerateConfig`
- **多重性**: [0..32]
- **多配置容器**: false

**容器描述**:

Container for configuration of service RandomGenerate. The container name serves as a symbolic name for the identifier of a service configuration.

######## 参数配置

此容器包含 **2** 个参数：

######### STRING 类型参数

########## 1. CalRandomGenerateInitConfiguration

- **UUID**: `ECUC:d31994d7-dc24-4be8-b079-cd7a3f62b41a`
- **参数名**: `CalRandomGenerateInitConfiguration`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of a C symbol which contains the configuration of the underlying cryptographic primitive.

########## 2. CalRandomGeneratePrimitiveName

- **UUID**: `ECUC:703f0519-3619-4715-a475-01f404a460bd`
- **参数名**: `CalRandomGeneratePrimitiveName`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of the cryptographic primitive to use.

##### 29. CalRandomGenerateConfig

**容器属性**:

- **UUID**: `ECUC:3be06fd3-a46d-42a6-a6e7-83c3da56547e`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CalRandomGenerateConfig`
- **多重性**: [0..32]
- **多配置容器**: false

**容器描述**:

Container for configuration of service RandomGenerate. The container name serves as a symbolic name for the identifier of a service configuration.

###### 参数配置

此容器包含 **2** 个参数：

####### STRING 类型参数

######## 1. CalRandomGenerateInitConfiguration

- **UUID**: `ECUC:d31994d7-dc24-4be8-b079-cd7a3f62b41a`
- **参数名**: `CalRandomGenerateInitConfiguration`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of a C symbol which contains the configuration of the underlying cryptographic primitive.

######## 2. CalRandomGeneratePrimitiveName

- **UUID**: `ECUC:703f0519-3619-4715-a475-01f404a460bd`
- **参数名**: `CalRandomGeneratePrimitiveName`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of the cryptographic primitive to use.

##### 30. CalRandomSeed

**容器属性**:

- **UUID**: `ECUC:f331107f-2173-4e57-9317-78f8eeda1df6`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CalRandomSeed`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Container for incorporation of RandomSeed primitives.

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. CalRandomMaxCtxBufByteSize

- **UUID**: `ECUC:ef467bd8-c0f7-4713-a091-e7b849962b87`
- **参数名**: `CalRandomMaxCtxBufByteSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The maximum, in bytes, of all context buffers used in all CPL primitives which implement seeding or generating a random number.

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. CalRandomSeedConfig

**容器属性**:

- **UUID**: `ECUC:32d0487f-dba6-436d-931b-cc3009ac07d3`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CalRandomSeedConfig`
- **多重性**: [0..32]
- **多配置容器**: false

**容器描述**:

Container for configuration of service RandomSeed. The container name serves as a symbolic name for the identifier of a service configuration.

######## 参数配置

此容器包含 **2** 个参数：

######### STRING 类型参数

########## 1. CalRandomSeedInitConfiguration

- **UUID**: `ECUC:4d6f2112-9185-4cdc-b3c3-ea305191f3cd`
- **参数名**: `CalRandomSeedInitConfiguration`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of a C symbol which contains the configuration of the underlying cryptographic primitive.

########## 2. CalRandomSeedPrimitiveName

- **UUID**: `ECUC:a26b0cd5-3f4f-44f8-ab1c-696fbcfb7e6e`
- **参数名**: `CalRandomSeedPrimitiveName`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of the cryptographic primitive to use.

##### 31. CalRandomSeedConfig

**容器属性**:

- **UUID**: `ECUC:32d0487f-dba6-436d-931b-cc3009ac07d3`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CalRandomSeedConfig`
- **多重性**: [0..32]
- **多配置容器**: false

**容器描述**:

Container for configuration of service RandomSeed. The container name serves as a symbolic name for the identifier of a service configuration.

###### 参数配置

此容器包含 **2** 个参数：

####### STRING 类型参数

######## 1. CalRandomSeedInitConfiguration

- **UUID**: `ECUC:4d6f2112-9185-4cdc-b3c3-ea305191f3cd`
- **参数名**: `CalRandomSeedInitConfiguration`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of a C symbol which contains the configuration of the underlying cryptographic primitive.

######## 2. CalRandomSeedPrimitiveName

- **UUID**: `ECUC:a26b0cd5-3f4f-44f8-ab1c-696fbcfb7e6e`
- **参数名**: `CalRandomSeedPrimitiveName`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of the cryptographic primitive to use.

##### 32. CalSignatureGenerate

**容器属性**:

- **UUID**: `ECUC:c9f667d5-c938-4e16-a5cf-dc0a6557457c`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CalSignatureGenerate`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Container for incorporation of SignatureGenerate primitives

###### 参数配置

此容器包含 **2** 个参数：

####### INTEGER 类型参数

######## 1. CalSignatureGenerateMaxCtxBufByteSize

- **UUID**: `ECUC:32c828cf-1ebd-4914-86cf-73da9f17d4f1`
- **参数名**: `CalSignatureGenerateMaxCtxBufByteSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The maximum, in bytes, of all context buffers used in all CPL primitives which implement a signature generation.

######## 2. CalSignatureGenerateMaxKeySize

- **UUID**: `ECUC:15af97e0-1d91-41dc-9dd9-a7f73fc54fce`
- **参数名**: `CalSignatureGenerateMaxKeySize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The maximum, in bytes, of all key lengths used in all CPL primitives which implement a signature generation.

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. CalSignatureGenerateConfig

**容器属性**:

- **UUID**: `ECUC:fba64fb0-3d09-44f0-8c89-27a3ba3783e1`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CalSignatureGenerateConfig`
- **多重性**: [0..32]
- **多配置容器**: false

**容器描述**:

Container for configuration of service SignatureGenerate. The container name serves as a symbolic name for the identifier of a service configuration.

######## 参数配置

此容器包含 **2** 个参数：

######### STRING 类型参数

########## 1. CalSignatureGenerateInitConfiguration

- **UUID**: `ECUC:190fbdd7-2112-4a48-b241-1fcc2991bb59`
- **参数名**: `CalSignatureGenerateInitConfiguration`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of a C symbol which contains the configuration of the underlying cryptographic primitive.

########## 2. CalSignatureGeneratePrimitiveName

- **UUID**: `ECUC:dde18f27-1038-41a8-8605-0ad51aa1ebbe`
- **参数名**: `CalSignatureGeneratePrimitiveName`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of the cryptographic primitive to use.

##### 33. CalSignatureGenerateConfig

**容器属性**:

- **UUID**: `ECUC:fba64fb0-3d09-44f0-8c89-27a3ba3783e1`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CalSignatureGenerateConfig`
- **多重性**: [0..32]
- **多配置容器**: false

**容器描述**:

Container for configuration of service SignatureGenerate. The container name serves as a symbolic name for the identifier of a service configuration.

###### 参数配置

此容器包含 **2** 个参数：

####### STRING 类型参数

######## 1. CalSignatureGenerateInitConfiguration

- **UUID**: `ECUC:190fbdd7-2112-4a48-b241-1fcc2991bb59`
- **参数名**: `CalSignatureGenerateInitConfiguration`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of a C symbol which contains the configuration of the underlying cryptographic primitive.

######## 2. CalSignatureGeneratePrimitiveName

- **UUID**: `ECUC:dde18f27-1038-41a8-8605-0ad51aa1ebbe`
- **参数名**: `CalSignatureGeneratePrimitiveName`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of the cryptographic primitive to use.

##### 34. CalSignatureVerify

**容器属性**:

- **UUID**: `ECUC:0896c97f-29da-4728-b518-a9fb32d757ef`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CalSignatureVerify`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Container for incorporation of SignatureVerify primitives.

###### 参数配置

此容器包含 **2** 个参数：

####### INTEGER 类型参数

######## 1. CalSignatureVerifyMaxCtxBufByteSize

- **UUID**: `ECUC:446c212f-3cce-411b-8b5c-44b7f3727279`
- **参数名**: `CalSignatureVerifyMaxCtxBufByteSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The maximum, in bytes, of all context buffers used in all CPL primitives which implement a signature verification.

######## 2. CalSignatureVerifyMaxKeySize

- **UUID**: `ECUC:6f4d8a51-cab8-44d0-9952-7a6e2c55caad`
- **参数名**: `CalSignatureVerifyMaxKeySize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The maximum, in bytes, of all key lengths used in all CPL primitives which implement a signature verification.

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. CalSignatureVerifyConfig

**容器属性**:

- **UUID**: `ECUC:4ddb2ff1-9ab7-4857-b942-3902c2b3a8c3`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CalSignatureVerifyConfig`
- **多重性**: [0..32]
- **多配置容器**: false

**容器描述**:

Container for configuration of service SignatureVerify. The container name serves as a symbolic name for the identifier of a service configuration.

######## 参数配置

此容器包含 **2** 个参数：

######### STRING 类型参数

########## 1. CalSignatureVerifyInitConfiguration

- **UUID**: `ECUC:31b6c628-78c8-421b-8f71-6e7ec94970d5`
- **参数名**: `CalSignatureVerifyInitConfiguration`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of a C symbol which contains the configuration of the underlying cryptographic primitive.

########## 2. CalSignatureVerifyPrimitiveName

- **UUID**: `ECUC:d5572bd8-c4e1-4579-940b-58ab550d2e3e`
- **参数名**: `CalSignatureVerifyPrimitiveName`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of the cryptographic primitive to use.

##### 35. CalSignatureVerifyConfig

**容器属性**:

- **UUID**: `ECUC:4ddb2ff1-9ab7-4857-b942-3902c2b3a8c3`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CalSignatureVerifyConfig`
- **多重性**: [0..32]
- **多配置容器**: false

**容器描述**:

Container for configuration of service SignatureVerify. The container name serves as a symbolic name for the identifier of a service configuration.

###### 参数配置

此容器包含 **2** 个参数：

####### STRING 类型参数

######## 1. CalSignatureVerifyInitConfiguration

- **UUID**: `ECUC:31b6c628-78c8-421b-8f71-6e7ec94970d5`
- **参数名**: `CalSignatureVerifyInitConfiguration`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of a C symbol which contains the configuration of the underlying cryptographic primitive.

######## 2. CalSignatureVerifyPrimitiveName

- **UUID**: `ECUC:d5572bd8-c4e1-4579-940b-58ab550d2e3e`
- **参数名**: `CalSignatureVerifyPrimitiveName`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of the cryptographic primitive to use.

##### 36. CalSymBlockDecrypt

**容器属性**:

- **UUID**: `ECUC:30c15161-f8c6-4817-9a4c-c6e84bf0cfe1`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CalSymBlockDecrypt`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Container for incorporation of SymBlockDecrypt primitives.

###### 参数配置

此容器包含 **2** 个参数：

####### INTEGER 类型参数

######## 1. CalSymBlockDecryptMaxCtxBufByteSize

- **UUID**: `ECUC:98c3d5ee-bde9-4cb5-9f1d-e95698b418db`
- **参数名**: `CalSymBlockDecryptMaxCtxBufByteSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The maximum, in bytes, of all context buffers used in all CPL primitives which implement a symmetrical block decryption.

######## 2. CalSymBlockDecryptMaxKeySize

- **UUID**: `ECUC:dd0f7b4d-52ea-47b4-8c6e-ac73c1811773`
- **参数名**: `CalSymBlockDecryptMaxKeySize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The maximum, in bytes, of all key lengths used in all CPL primitives which implement a symmetrical block decryption.

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. CalSymBlockDecryptConfig

**容器属性**:

- **UUID**: `ECUC:27c2233c-bd85-4b46-82e7-481d8f9446c8`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CalSymBlockDecryptConfig`
- **多重性**: [0..32]
- **多配置容器**: false

**容器描述**:

Container for configuration of service SymBlockDecrypt. The container name serves as a symbolic name for the identifier of a service configuration.

######## 参数配置

此容器包含 **2** 个参数：

######### STRING 类型参数

########## 1. CalSymBlockDecryptInitConfiguration

- **UUID**: `ECUC:5df8bfb0-4d7b-4b48-af49-311ce14c21b4`
- **参数名**: `CalSymBlockDecryptInitConfiguration`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of a C symbol which contains the configuration of the underlying cryptographic primitive.

########## 2. CalSymBlockDecryptPrimitiveName

- **UUID**: `ECUC:aa7bc88e-e328-4ecd-a1f5-ca1235e2d486`
- **参数名**: `CalSymBlockDecryptPrimitiveName`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of the cryptographic primitive to use.

##### 37. CalSymBlockDecryptConfig

**容器属性**:

- **UUID**: `ECUC:27c2233c-bd85-4b46-82e7-481d8f9446c8`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CalSymBlockDecryptConfig`
- **多重性**: [0..32]
- **多配置容器**: false

**容器描述**:

Container for configuration of service SymBlockDecrypt. The container name serves as a symbolic name for the identifier of a service configuration.

###### 参数配置

此容器包含 **2** 个参数：

####### STRING 类型参数

######## 1. CalSymBlockDecryptInitConfiguration

- **UUID**: `ECUC:5df8bfb0-4d7b-4b48-af49-311ce14c21b4`
- **参数名**: `CalSymBlockDecryptInitConfiguration`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of a C symbol which contains the configuration of the underlying cryptographic primitive.

######## 2. CalSymBlockDecryptPrimitiveName

- **UUID**: `ECUC:aa7bc88e-e328-4ecd-a1f5-ca1235e2d486`
- **参数名**: `CalSymBlockDecryptPrimitiveName`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of the cryptographic primitive to use.

##### 38. CalSymBlockEncrypt

**容器属性**:

- **UUID**: `ECUC:ee9537c9-2dd9-46e4-a7b6-6226c2a490aa`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CalSymBlockEncrypt`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Container for incorporation of SymBlockEncrypt primitives.

###### 参数配置

此容器包含 **2** 个参数：

####### INTEGER 类型参数

######## 1. CalSymBlockEncryptMaxCtxBufByteSize

- **UUID**: `ECUC:c9671303-95a0-4ccd-9bdf-3430ecd33748`
- **参数名**: `CalSymBlockEncryptMaxCtxBufByteSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The maximum, in bytes, of all context buffers used in all CPL primitives which implement a symmetrical block encryption.

######## 2. CalSymBlockEncryptMaxKeySize

- **UUID**: `ECUC:6cead96f-93a9-439a-b30a-30941797d7d8`
- **参数名**: `CalSymBlockEncryptMaxKeySize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The maximum, in bytes, of all key lengths used in all CPL primitives which implement a symmetrical block encryption.

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. CalSymBlockEncryptConfig

**容器属性**:

- **UUID**: `ECUC:61f2c3e0-c9d1-401e-b5bc-885a4299b333`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CalSymBlockEncryptConfig`
- **多重性**: [0..32]
- **多配置容器**: false

**容器描述**:

Container for configuration of service SymBlockEncrypt. The container name serves as a symbolic name for the identifier of a service configuration.

######## 参数配置

此容器包含 **2** 个参数：

######### STRING 类型参数

########## 1. CalSymBlockEncryptInitConfiguration

- **UUID**: `ECUC:3909228c-b3e8-40fd-9071-c0589a663275`
- **参数名**: `CalSymBlockEncryptInitConfiguration`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of a C symbol which contains the configuration of the underlying cryptographic primitive.

########## 2. CalSymBlockEncryptPrimitiveName

- **UUID**: `ECUC:a909e448-87be-4f4c-80a6-0404c0c745f1`
- **参数名**: `CalSymBlockEncryptPrimitiveName`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of the cryptographic primitive to use.

##### 39. CalSymBlockEncryptConfig

**容器属性**:

- **UUID**: `ECUC:61f2c3e0-c9d1-401e-b5bc-885a4299b333`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CalSymBlockEncryptConfig`
- **多重性**: [0..32]
- **多配置容器**: false

**容器描述**:

Container for configuration of service SymBlockEncrypt. The container name serves as a symbolic name for the identifier of a service configuration.

###### 参数配置

此容器包含 **2** 个参数：

####### STRING 类型参数

######## 1. CalSymBlockEncryptInitConfiguration

- **UUID**: `ECUC:3909228c-b3e8-40fd-9071-c0589a663275`
- **参数名**: `CalSymBlockEncryptInitConfiguration`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of a C symbol which contains the configuration of the underlying cryptographic primitive.

######## 2. CalSymBlockEncryptPrimitiveName

- **UUID**: `ECUC:a909e448-87be-4f4c-80a6-0404c0c745f1`
- **参数名**: `CalSymBlockEncryptPrimitiveName`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of the cryptographic primitive to use.

##### 40. CalSymDecrypt

**容器属性**:

- **UUID**: `ECUC:de88d16a-4393-47ef-90ce-94dfd42a9c44`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CalSymDecrypt`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Container for incorporation of SymDecrypt primitives

###### 参数配置

此容器包含 **2** 个参数：

####### INTEGER 类型参数

######## 1. CalSymDecryptMaxCtxBufByteSize

- **UUID**: `ECUC:7e86b49f-ca1e-4969-8d23-6b58a4387f7d`
- **参数名**: `CalSymDecryptMaxCtxBufByteSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The maximum, in bytes, of all context buffers used in all CPL primitives which implement a symmetrical decryption.

######## 2. CalSymDecryptMaxKeySize

- **UUID**: `ECUC:207278f2-5333-4d05-bf17-4acc4b52de50`
- **参数名**: `CalSymDecryptMaxKeySize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The maximum, in bytes, of all key lengths used in all CPL primitives which implement a symmetrical decryption.

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. CalSymDecryptConfig

**容器属性**:

- **UUID**: `ECUC:f413d024-59fa-42d0-8b92-1c64c7d5a1b5`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CalSymDecryptConfig`
- **多重性**: [0..32]
- **多配置容器**: false

**容器描述**:

Container for configuration of service SymDecrypt.

######## 参数配置

此容器包含 **2** 个参数：

######### STRING 类型参数

########## 1. CalSymDecryptInitConfiguration

- **UUID**: `ECUC:a3a3297a-fedf-4f32-9946-d78b46d6894d`
- **参数名**: `CalSymDecryptInitConfiguration`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of a C symbol which contains the configuration of the underlying cryptographic primitive.

########## 2. CalSymDecryptPrimitiveName

- **UUID**: `ECUC:1467d2d9-0718-4aa1-9d15-b864a1bfcc6f`
- **参数名**: `CalSymDecryptPrimitiveName`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of the cryptographic primitive to use.

##### 41. CalSymDecryptConfig

**容器属性**:

- **UUID**: `ECUC:f413d024-59fa-42d0-8b92-1c64c7d5a1b5`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CalSymDecryptConfig`
- **多重性**: [0..32]
- **多配置容器**: false

**容器描述**:

Container for configuration of service SymDecrypt.

###### 参数配置

此容器包含 **2** 个参数：

####### STRING 类型参数

######## 1. CalSymDecryptInitConfiguration

- **UUID**: `ECUC:a3a3297a-fedf-4f32-9946-d78b46d6894d`
- **参数名**: `CalSymDecryptInitConfiguration`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of a C symbol which contains the configuration of the underlying cryptographic primitive.

######## 2. CalSymDecryptPrimitiveName

- **UUID**: `ECUC:1467d2d9-0718-4aa1-9d15-b864a1bfcc6f`
- **参数名**: `CalSymDecryptPrimitiveName`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of the cryptographic primitive to use.

##### 42. CalSymEncrypt

**容器属性**:

- **UUID**: `ECUC:874ca516-3ea1-4673-bdcb-78dcb8e75e34`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CalSymEncrypt`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Container for incorporation of SymEncrypt primitives.

###### 参数配置

此容器包含 **2** 个参数：

####### INTEGER 类型参数

######## 1. CalSymEncryptMaxCtxBufByteSize

- **UUID**: `ECUC:c228691f-bd5d-4d14-b9ed-4db30fa05d33`
- **参数名**: `CalSymEncryptMaxCtxBufByteSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The maximum, in bytes, of all context buffers used in all CPL primitives which implement a symmetrical encryption.

######## 2. CalSymEncryptMaxKeySize

- **UUID**: `ECUC:9b575a02-485b-4815-8432-bcf32b45f39f`
- **参数名**: `CalSymEncryptMaxKeySize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The maximum, in bytes, of all key lengths used in all CPL primitives which implement a symmetrical encryption.

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. CalSymEncryptConfig

**容器属性**:

- **UUID**: `ECUC:58bb6a94-d5f0-4bf6-b922-9a2ae8dcf9ac`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CalSymEncryptConfig`
- **多重性**: [0..32]
- **多配置容器**: false

**容器描述**:

Container for configuration of service SymEncrypt. The container name serves as a symbolic name for the identifier of a service configuration.

######## 参数配置

此容器包含 **2** 个参数：

######### STRING 类型参数

########## 1. CalSymBlockEncryptInitConfiguration

- **UUID**: `ECUC:6e493190-58ea-4034-94da-04ce84ff7225`
- **参数名**: `CalSymBlockEncryptInitConfiguration`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of a C symbol which contains the configuration of the underlying cryptographic primitive.

########## 2. CalSymEncryptPrimitiveName

- **UUID**: `ECUC:0d22d540-3889-4dd5-80bc-4d329748bb00`
- **参数名**: `CalSymEncryptPrimitiveName`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of the cryptographic primitive to use.

##### 43. CalSymEncryptConfig

**容器属性**:

- **UUID**: `ECUC:58bb6a94-d5f0-4bf6-b922-9a2ae8dcf9ac`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CalSymEncryptConfig`
- **多重性**: [0..32]
- **多配置容器**: false

**容器描述**:

Container for configuration of service SymEncrypt. The container name serves as a symbolic name for the identifier of a service configuration.

###### 参数配置

此容器包含 **2** 个参数：

####### STRING 类型参数

######## 1. CalSymBlockEncryptInitConfiguration

- **UUID**: `ECUC:6e493190-58ea-4034-94da-04ce84ff7225`
- **参数名**: `CalSymBlockEncryptInitConfiguration`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of a C symbol which contains the configuration of the underlying cryptographic primitive.

######## 2. CalSymEncryptPrimitiveName

- **UUID**: `ECUC:0d22d540-3889-4dd5-80bc-4d329748bb00`
- **参数名**: `CalSymEncryptPrimitiveName`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of the cryptographic primitive to use.

##### 44. CalSymKeyExtract

**容器属性**:

- **UUID**: `ECUC:fadfb320-923d-4607-80e8-f04e6cbe6787`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CalSymKeyExtract`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Container for incorporation of SymKeyExtract primitives.

###### 参数配置

此容器包含 **2** 个参数：

####### INTEGER 类型参数

######## 1. CalSymKeyExtractMaxCtxBufByteSize

- **UUID**: `ECUC:c4dcf674-b454-4c2c-bd06-a836ab76c3db`
- **参数名**: `CalSymKeyExtractMaxCtxBufByteSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The maximum, in bytes, of all context buffers used in all CPL primitives which implement a symmetrical key extraction.

######## 2. CalSymKeyExtractMaxKeySize

- **UUID**: `ECUC:27a1e153-127b-4b7d-b178-bf24afaa9184`
- **参数名**: `CalSymKeyExtractMaxKeySize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The maximum, in bytes, of all key lengths used in all CPL primitives which implement a symmetrical key extraction.

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. CalSymKeyExtractConfig

**容器属性**:

- **UUID**: `ECUC:f671e200-2693-4ca1-b610-f9edfa2683e9`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CalSymKeyExtractConfig`
- **多重性**: [0..32]
- **多配置容器**: false

**容器描述**:

Container for configuration of service SymKeyExtract. The container name serves as a symbolic name for the identifier of a service configuration.

######## 参数配置

此容器包含 **2** 个参数：

######### STRING 类型参数

########## 1. CalSymKeyExtractInitConfiguration

- **UUID**: `ECUC:b18dbda5-2217-4bfd-8ede-58095ba221ad`
- **参数名**: `CalSymKeyExtractInitConfiguration`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of a C symbol which contains the configuration of the underlying cryptographic primitive.

########## 2. CalSymKeyExtractPrimitiveName

- **UUID**: `ECUC:879aa62c-b8ef-4371-90c9-79bfe6e4e2bc`
- **参数名**: `CalSymKeyExtractPrimitiveName`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of the cryptographic primitive to use.

##### 45. CalSymKeyExtractConfig

**容器属性**:

- **UUID**: `ECUC:f671e200-2693-4ca1-b610-f9edfa2683e9`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CalSymKeyExtractConfig`
- **多重性**: [0..32]
- **多配置容器**: false

**容器描述**:

Container for configuration of service SymKeyExtract. The container name serves as a symbolic name for the identifier of a service configuration.

###### 参数配置

此容器包含 **2** 个参数：

####### STRING 类型参数

######## 1. CalSymKeyExtractInitConfiguration

- **UUID**: `ECUC:b18dbda5-2217-4bfd-8ede-58095ba221ad`
- **参数名**: `CalSymKeyExtractInitConfiguration`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of a C symbol which contains the configuration of the underlying cryptographic primitive.

######## 2. CalSymKeyExtractPrimitiveName

- **UUID**: `ECUC:879aa62c-b8ef-4371-90c9-79bfe6e4e2bc`
- **参数名**: `CalSymKeyExtractPrimitiveName`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of the cryptographic primitive to use.

##### 46. CalSymKeyWrapAsym

**容器属性**:

- **UUID**: `ECUC:e6940cad-173b-4cca-9023-11a4724ea7d5`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CalSymKeyWrapAsym`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Container for incorporation of SymKeyWrapAsym primitives.

###### 参数配置

此容器包含 **2** 个参数：

####### INTEGER 类型参数

######## 1. CalSymKeyWrapAsymMaxPubKeySize

- **UUID**: `ECUC:9fba9927-6edf-405d-b14e-dfc06619ce87`
- **参数名**: `CalSymKeyWrapAsymMaxPubKeySize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The maximum length, in bytes, of all public key  types used in all CPL primitives which implement a symmetrical key wrapping.

######## 2. CalSymKeyWrapAsymMaxSymKeySize

- **UUID**: `ECUC:664ffa6e-cdf0-4239-89fe-ed591362e592`
- **参数名**: `CalSymKeyWrapAsymMaxSymKeySize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The maximum, in bytes, of all key lengths used in all CPL primitives which implement a symmetrical key wrapping.

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. CalSymKeyWrapAsymConfig

**容器属性**:

- **UUID**: `ECUC:32deddc9-6f4d-4e39-a51c-b3ea37a4fcf0`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CalSymKeyWrapAsymConfig`
- **多重性**: [0..32]
- **多配置容器**: false

**容器描述**:

Container for configuration of service SymKeyWrapAsym.

######## 参数配置

此容器包含 **2** 个参数：

######### STRING 类型参数

########## 1. CalSymKeyWrapAsymInitConfiguration

- **UUID**: `ECUC:75bee5f8-3bbd-4b08-b7d2-adbf72f7e8f8`
- **参数名**: `CalSymKeyWrapAsymInitConfiguration`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of a C symbol which contains the configuration of the underlying cryptographic primitive.

########## 2. CalSymKeyWrapAsymPrimitiveName

- **UUID**: `ECUC:3fa84ac3-6b11-49e2-983b-166fd1a72b4a`
- **参数名**: `CalSymKeyWrapAsymPrimitiveName`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of the cryptographic primitive to use.

##### 47. CalSymKeyWrapAsymConfig

**容器属性**:

- **UUID**: `ECUC:32deddc9-6f4d-4e39-a51c-b3ea37a4fcf0`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CalSymKeyWrapAsymConfig`
- **多重性**: [0..32]
- **多配置容器**: false

**容器描述**:

Container for configuration of service SymKeyWrapAsym.

###### 参数配置

此容器包含 **2** 个参数：

####### STRING 类型参数

######## 1. CalSymKeyWrapAsymInitConfiguration

- **UUID**: `ECUC:75bee5f8-3bbd-4b08-b7d2-adbf72f7e8f8`
- **参数名**: `CalSymKeyWrapAsymInitConfiguration`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of a C symbol which contains the configuration of the underlying cryptographic primitive.

######## 2. CalSymKeyWrapAsymPrimitiveName

- **UUID**: `ECUC:3fa84ac3-6b11-49e2-983b-166fd1a72b4a`
- **参数名**: `CalSymKeyWrapAsymPrimitiveName`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of the cryptographic primitive to use.

##### 48. CalSymKeyWrapSym

**容器属性**:

- **UUID**: `ECUC:a48d5fad-4e91-4887-ac82-090b693ab99f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CalSymKeyWrapSym`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Container for incorporation of SymKeyWrapSym primitives.

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. CalSymKeyWrapSymMaxSymKeySize

- **UUID**: `ECUC:b9a42ac3-a2ef-4a64-9b33-4a398fdd2fde`
- **参数名**: `CalSymKeyWrapSymMaxSymKeySize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The maximum, in bytes, of all key lengths used in all CPL primitives which implement a symmetrical key wrapping.

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. CalSymKeyWrapSymConfig

**容器属性**:

- **UUID**: `ECUC:467640ee-e2a3-4818-8044-9c26aa919257`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CalSymKeyWrapSymConfig`
- **多重性**: [0..32]
- **多配置容器**: false

**容器描述**:

Container for configuration of service SymKeyWrapSym.

######## 参数配置

此容器包含 **2** 个参数：

######### STRING 类型参数

########## 1. CalSymKeyWrapSymInitConfiguration

- **UUID**: `ECUC:3ff6e410-231d-4fb5-87ed-05cb4017634f`
- **参数名**: `CalSymKeyWrapSymInitConfiguration`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of a C symbol which contains the configuration of the underlying cryptographic primitive.

########## 2. CalSymKeyWrapSymPrimitiveName

- **UUID**: `ECUC:8835a39e-8f26-4b59-a1b9-285e0a5fc59f`
- **参数名**: `CalSymKeyWrapSymPrimitiveName`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of the cryptographic primitive to use.

##### 49. CalSymKeyWrapSymConfig

**容器属性**:

- **UUID**: `ECUC:467640ee-e2a3-4818-8044-9c26aa919257`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CalSymKeyWrapSymConfig`
- **多重性**: [0..32]
- **多配置容器**: false

**容器描述**:

Container for configuration of service SymKeyWrapSym.

###### 参数配置

此容器包含 **2** 个参数：

####### STRING 类型参数

######## 1. CalSymKeyWrapSymInitConfiguration

- **UUID**: `ECUC:3ff6e410-231d-4fb5-87ed-05cb4017634f`
- **参数名**: `CalSymKeyWrapSymInitConfiguration`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of a C symbol which contains the configuration of the underlying cryptographic primitive.

######## 2. CalSymKeyWrapSymPrimitiveName

- **UUID**: `ECUC:8835a39e-8f26-4b59-a1b9-285e0a5fc59f`
- **参数名**: `CalSymKeyWrapSymPrimitiveName`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of the cryptographic primitive to use.

## 📦 包结构

此ARXML文件包含 **2** 个包：

### 1. AUTOSAR

- **UUID**: `ECUC:AUTOSAR`
- **包名称**: `AUTOSAR`
- **包含元素数量**: 0

### 2. EcucDefs

- **UUID**: `ECUC:ECUCDEFS`
- **包名称**: `EcucDefs`
- **包含元素数量**: 1

#### 包含的元素

##### ECUC-MODULE-DEF 类型元素

1. **Cal**
