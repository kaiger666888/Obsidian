# FblSb - 完整配置文档

*此文档由ARXML文件自动生成，采用层次化结构展示*

**生成时间**: 2025-06-16 14:48:10

## 📑 目录

- [📄 文件信息](#-文件信息)
- [🔧 模块定义](#-模块定义)
  - [FblSb](#fblsb)
- [📦 包结构](#-包结构)
- [⚡ 实现信息](#-实现信息)
- [⚙️ 配置信息](#️-配置信息)

## 📄 文件信息

### Schema信息
- **Schema位置**: `http://autosar.org/schema/r4.0 AUTOSAR_4-3-0.xsd`
- **命名空间**: `http://autosar.org/schema/r4.0`

## 🔧 模块定义

### 1. FblSb

#### 基本信息

- **UUID**: `74ca2fbb-00f6-47c3-bae9-a0419594cf8f`
- **模块名称**: `FblSb`
- **类别**: `VENDOR_SPECIFIC_MODULE_DEFINITION`
- **多重性**: [1..1]
- **支持的变体**:
  - VARIANT-PRE-COMPILE

#### 模块描述

Configuration of the FblSb (Secure Boot) module.

#### 版本历史

共有 **1** 个版本记录：

##### 1. 版本 1.00.02

- **发布日期**: 2019-05-22T15:15:52+02:00
- **发布者**: visrie

**变更内容**:

#### 配置容器

本模块包含 **2** 个配置容器：

##### 1. FblSbGeneral

**容器属性**:

- **UUID**: `45d85720-8bd7-40df-a851-5bf78818a64e`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FblSbGeneral`
- **多重性**: [1..1]
- **需要索引**: false

**容器描述**:

General configuration parameters of the FblSb.

###### 参数配置

此容器包含 **7** 个参数：

####### INTEGER 类型参数

######## 1. FblSbSecureBootUpdateSignatureLength

- **UUID**: `eb6cea2e-9491-426a-9bbe-d608f2f21fba`
- **参数名**: `FblSbSecureBootUpdateSignatureLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Length of the signature used by the vHsm during the SecureBootUpdate sequence.
Automatically filled out in case the algorithm is already known.

####### BOOLEAN 类型参数

######## 1. FblSbCopyFlashDriver

- **UUID**: `987a1b63-e7b5-4ede-8bb4-3f7a735fb7a6`
- **参数名**: `FblSbCopyFlashDriver`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Enables or disables the copy flash driver API (FblSb_CopyFlashDriver), which copies the internal code flash driver into RAM.
True: Copy routine is available.
False: Copy routine is deactivated.

######## 2. FblSbHeaderVerification

- **UUID**: `da3fb37e-59ed-4ae7-8369-1c6b36c37083`
- **参数名**: `FblSbHeaderVerification`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: If enabled it is possible to verify the header structure separately

######## 3. FblSbFblLbtVerification

- **UUID**: `b136836b-5d47-4129-9365-a84f6c419714`
- **参数名**: `FblSbFblLbtVerification`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: If enabled it is possible to verify the LBT of the FBL separately

######## 4. FblSbVerificationList

- **UUID**: `31b666d9-eac5-482f-9969-24cd64e525b0`
- **参数名**: `FblSbVerificationList`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Specify if a verification list in the FblBmHdrHeader structure is required

####### STRING 类型参数

######## 1. FblSbUserConfigFile

- **UUID**: `2537f622-70b1-4281-a6f3-b1ac204b1fe0`
- **参数名**: `FblSbUserConfigFile`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **字符串变体**:
  - 默认值: `FblSb_UserCfg.h`
- **描述**: Reference to an external text file that will be included during generation to FblSb_Cfg.h.
The content of the user configuration file will be added at the end of the generated module configuration file and allows altering or extending the generated code.

Caution: User configuration files can cause the software module to malfunction and must only be used with great care!

####### ENUMERATION 类型参数

######## 1. FblSbSecureBootUpdateSignatureAlgorithm

- **UUID**: `e485d6c1-c81f-4ace-a3b6-94bf287f0c46`
- **参数名**: `FblSbSecureBootUpdateSignatureAlgorithm`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `ED25519`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `ED25519`
  - `ECDSA_256`
  - `ECDSA_384`
  - `ECDSA_512`
  - `RSA_512`
  - `RSA_1024`
  - `RSA_2048`
  - `RSA_3072`
  - `RSA_4096`
  - `CUSTOM`
- **描述**: Specifies the algorithm used by the vHsm to determine the length of the signature.

Note: If the algorithm is not listed, use CUSTOM and manually enter the signature length in FblSbSecureBootUpdateSignatureLength.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. FblSbInitialStartupKeyRef

- **UUID**: `c3499718-5feb-41c3-8df7-85cf7a475ffd`
- **引用名**: `FblSbInitialStartupKeyRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `CsmKey`
- **完整路径**: `/MICROSAR/Csm/CsmKeys/CsmKey`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **需要索引**: false
- **描述**: Specifies the key, which is used to determine the initial startup.
Note, that this key should be a WriteOnce key in the vHsm.

##### 2. FblSbMacOperation

**容器属性**:

- **UUID**: `768908f8-7b2e-43e8-b305-05fd93d6ebee`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FblSbMacOperation`
- **多重性**: [1..256]
- **需要索引**: false

**容器描述**:

Container for configuration of the MacOperation used to generate and verify MACs.

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. FblSbMacOperationId

- **UUID**: `13520393-647a-480d-950f-a165544886cc`
- **参数名**: `FblSbMacOperationId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..255]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Identifier of the MacOperation.

###### 引用关系

此容器包含 **3** 个引用：

####### REFERENCE 类型引用

######## 1. FblSbMacGenerationRef

- **UUID**: `2875f3ab-fef9-405c-a31a-2beae484a2b4`
- **引用名**: `FblSbMacGenerationRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `CsmJob`
- **完整路径**: `/MICROSAR/Csm/CsmJobs/CsmJob`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **需要索引**: false
- **描述**: This parameter refers to the used CsmJob to perform a SecureBootUpdate.

######## 2. FblSbMacVerificationRef

- **UUID**: `7c7d3849-2593-42a3-8690-106fc9eaf7e7`
- **引用名**: `FblSbMacVerificationRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `CsmJob`
- **完整路径**: `/MICROSAR/Csm/CsmJobs/CsmJob`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **需要索引**: false
- **描述**: This parameter refers to the used CsmJob to perform a SecureBoot (Verify).

######## 3. FblSbMacVerificationForceSequentialRef

- **UUID**: `9580ec75-7ce3-41fb-bd6f-4351dceb9496`
- **引用名**: `FblSbMacVerificationForceSequentialRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `CsmJob`
- **完整路径**: `/MICROSAR/Csm/CsmJobs/CsmJob`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **需要索引**: false
- **描述**: This parameter refers to the used CsmJob to perform a SecureBoot (Verify) Forced Sequential. This option is used in case the Bootloader should perform implicitly a SecureBootUpdate during the initial startup to update the SecureBootSegments in the vHsm.

## 📦 包结构

此ARXML文件包含 **1** 个包：

### 1. MICROSAR

- **UUID**: `ff55d029-386d-43a2-b3c2-dfef4c7a5e36`
- **包名称**: `MICROSAR`
- **包含元素数量**: 4

#### 包含的元素

##### BSW-IMPLEMENTATION 类型元素

1. **FblSb_Impl**

##### ECUC-MODULE-DEF 类型元素

1. **FblSb**

##### ECUC-MODULE-CONFIGURATION-VALUES 类型元素

1. **FblSb_Pre**
2. **FblSb_Rec**

## ⚡ 实现信息

此ARXML文件包含 **1** 个实现：

### 1. FblSb_Impl

- **UUID**: `2633263f-a3c3-4b69-8c0e-acef8c0b4cae`
- **实现名称**: `FblSb_Impl`
- **编程语言**: C
- **软件版本**: 1.00.00
- **供应商ID**: 30
- **AUTOSAR版本**: 4.03.00
- **代码生成器**: DaVinci Configurator

## ⚙️ 配置信息

此ARXML文件包含 **2** 个配置：

### 1. FblSb_Pre

- **UUID**: `8bf17c98-4dd9-48ce-8ea4-1fb53d032ae3`
- **配置名称**: `FblSb_Pre`
- **定义引用**: `/MICROSAR/FblSb`

### 2. FblSb_Rec

- **UUID**: `3e1f9515-c56f-4588-a56c-6a0fee4c6e64`
- **配置名称**: `FblSb_Rec`
- **定义引用**: `/MICROSAR/FblSb`
