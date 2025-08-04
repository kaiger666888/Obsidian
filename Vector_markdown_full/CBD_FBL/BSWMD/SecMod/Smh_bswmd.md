# Smh - 完整配置文档

*此文档由ARXML文件自动生成，采用层次化结构展示*

**生成时间**: 2025-06-16 14:48:24

## 📑 目录

- [📄 文件信息](#-文件信息)
- [🔧 模块定义](#-模块定义)
  - [Smh](#smh)
- [📦 包结构](#-包结构)
- [⚡ 实现信息](#-实现信息)
- [⚙️ 配置信息](#️-配置信息)

## 📄 文件信息

### Schema信息
- **Schema位置**: `http://autosar.org/schema/r4.0 AUTOSAR_4-0-3.xsd`
- **命名空间**: `http://autosar.org/schema/r4.0`

## 🔧 模块定义

### 1. Smh

#### 基本信息

- **UUID**: `42a135ab-ab26-46b2-8715-4f459191ff0c`
- **模块名称**: `Smh`
- **类别**: `VENDOR_SPECIFIC_MODULE_DEFINITION`
- **多重性**: [0..1]
- **支持的变体**:
  - VARIANT-LINK-TIME

#### 模块描述

Configuration of the Smh (SecModHis, Security Module implementing the HIS specification) module.

#### 版本历史

共有 **5** 个版本记录：

##### 1. 版本 3.00.00

- **发布日期**: 2020-03-18T10:15:05+01:00
- **发布者**: visrcn

**变更内容**:

##### 2. 版本 3.01.00

- **发布日期**: 2020-06-25T08:36:41+02:00
- **发布者**: vistbe

**变更内容**:

##### 3. 版本 3.02.00

- **发布日期**: 2020-09-22T11:09:19+02:00
- **发布者**: visrcn

**变更内容**:

##### 4. 版本 3.03.00

- **发布日期**: 2020-11-26T11:10:17+01:00
- **发布者**: vistbe

**变更内容**:

##### 5. 版本 3.03.00

- **发布日期**: 2020-12-02T08:29:47+01:00
- **发布者**: vistbe

**变更内容**:

#### 配置容器

本模块包含 **55** 个配置容器：

##### 1. SmhGeneral

**容器属性**:

- **UUID**: `3912cc2d-5e6f-45b0-8f88-ada71d6762f8`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SmhGeneral`
- **多重性**: [1..1]
- **构建后可变**: false

###### 参数配置

此容器包含 **5** 个参数：

####### INTEGER 类型参数

######## 1. SmhWatchdogCycleCount

- **UUID**: `879b5abc-c7bb-4f0a-a1d8-1562cc8c8cab`
- **参数名**: `SmhWatchdogCycleCount`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `1`
- **取值范围**: [1..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Controls frequency of polling function calls within loops including SEC_WATCHDOG_CYCLE_TRIGGER macro calls, e.g. from Sec_Crc.c.
The called function will typically be the Bootloader Polling (Watchdog Trigger) function and by this configuration will happen every Nth call (where N == configured cycle Count).

####### BOOLEAN 类型参数

######## 1. SmhCryptographicKeysLocatedInRAM

- **UUID**: `f251f1a6-4540-454e-9926-4e99ee9d5285`
- **参数名**: `SmhCryptographicKeysLocatedInRAM`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Specify the location of the SmhCryptographicKeys.

######## 2. SmhProvidevSecPrimRandomFunction

- **UUID**: `01d8e1d8-e7e9-4c3a-b03e-087df9280802`
- **参数名**: `SmhProvidevSecPrimRandomFunction`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: If enabled the SMH will generate the callout esl_getBytesRNG function required by the vSecPrim module. Please check the vSecPrim TechRef/Implementation for the API description. The default implementation of the function just returns E_NOT_OK. User code can be added to the function to implement custom behavior.

####### STRING 类型参数

######## 1. SmhUserConfigFile

- **UUID**: `d60ee34d-b7c2-421a-a062-fa313e606ed2`
- **参数名**: `SmhUserConfigFile`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: If a file path is specified, the file is read and its contents are put at the end of the SMH config file (SecM_cfg.h).

If you want to overwrite some of the settings in the generated configuration file (SecM_cfg.h), you can specify a path to a user defined configuration file. The user defined configuration file will be included at the end of the generated preprocessor switches. Definitions in the user defined configuration file can overwrite definitions in the generated configuration file.

To specify the file name, you can use "$(var)" sequence(s) in the specified path. Each such sequence is replaced by the content of the related environment variable "var".
Additionally you can use following predefined sequences:
$(DpaProjectFolder) Absolute directory of the loaded *.dpa file.
$(EcuProjectName) Name of the project defined in the loaded *.dpa file.
$(EcucFile) Absolute directory "ECUC", defined by the loaded *.dpa file, containing files $(EcuProjectName).ecuc.arxml and $(EcuProjectName).ecuc.Initial.arxml .
$(EcucFolder) Parent directory of $(EcucFile).
$(SipRootPath) Absolute directory "SIP", defined by the loaded *.dpa file.
$(OutputFolder) (Relative) directory "GenData", defined by the loaded *.dpa file. See setting "Root Target Folder" of Configurator 5.
$(ServiceSwcFolder) Absolute directory "ServiceComponents", defined by the loaded *.dpa file.
$(cwd) Current working directory when starting Configurator 5.

RESTRICTIONS: Not all of the settings can be overwritten simply by triggering the preprocessor switch. Some of the options are complex and the code generator generates less or more code depending on the setting.

USE SUCH A FILE ONLY AFTER DISCUSSION WITH VECTOR.

####### ENUMERATION 类型参数

######## 1. SmhOperationMode

- **UUID**: `96d0c63e-90a5-4154-89f3-ffa4238a6a89`
- **参数名**: `SmhOperationMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `PRODUCTION`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `DEVELOP` (来源: Vector Informatik)
  - `PRODUCTION` (来源: Vector Informatik)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: The mode of the security component is set to Production. The setting is displayed for documentation purposes only.

##### 2. SmhEncryption

**容器属性**:

- **UUID**: `490b1396-0554-4d64-acbb-e411721e8ea9`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SmhEncryption`
- **多重性**: [1..1]
- **构建后可变**: false

**容器描述**:

Container to configure the HIS security class
AAA: encryption and decryption

###### 引用关系

此容器包含 **2** 个引用：

####### REFERENCE 类型引用

######## 1. SmhEncryptionDefaultConfig

- **UUID**: `0ea4e4f6-e106-4830-a4fa-002a9b399e86`
- **引用名**: `SmhEncryptionDefaultConfig`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `SmhEncryptionConfig`
- **完整路径**: `/MICROSAR/Smh/SmhEncryption/SmhEncryptionConfig`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Default configuration for encryption (used by SecM_Encryption)

######## 2. SmhDecryptionDefaultConfig

- **UUID**: `59b1100b-4cb2-40c0-a979-9d7550a59fb2`
- **引用名**: `SmhDecryptionDefaultConfig`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `SmhDecryptionConfig`
- **完整路径**: `/MICROSAR/Smh/SmhEncryption/SmhDecryptionConfig`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Default configuration for decryption (used by SecM_Decryption)

###### 配置容器

本模块包含 **2** 个配置容器：

####### 1. SmhEncryptionConfig

**容器属性**:

- **UUID**: `c89fbaa2-0f61-4690-bc57-bdd20e86cb9a`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SmhEncryptionConfig`
- **多重性**: [0..infinite]
- **构建后可变**: false

**容器描述**:

Container to configure encryption jobs.

######## 参数配置

此容器包含 **1** 个参数：

######### FUNCTION-NAME 类型参数

########## 1. SmhFunctionName

- **UUID**: `e8d1db85-8613-4dfe-a3d5-6d7d6005ef8d`
- **参数名**: `SmhFunctionName`
- **数据类型**: FUNCTION-NAME
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Name of the encryption function, e.g.:
SecM_EncryptAes128NoneEcb
SecM_EncryptAes128Iso7816_4Ecb
SecM_EncryptAes192PkcsCbc

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. SmhJobRef

- **UUID**: `0ddfe8a6-affa-4dc6-bc23-8f0fb3d6f2a3`
- **引用名**: `SmhJobRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `SmhJob`
- **完整路径**: `/MICROSAR/Smh/SmhJob`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: This parameter refers to the used SmhEncryption job for encryption.

####### 2. SmhDecryptionConfig

**容器属性**:

- **UUID**: `72d0560c-1e26-4de4-bd30-a06eb5e1af3d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SmhDecryptionConfig`
- **多重性**: [0..infinite]
- **构建后可变**: false

**容器描述**:

Container to configure decryption jobs.

######## 参数配置

此容器包含 **1** 个参数：

######### FUNCTION-NAME 类型参数

########## 1. SmhFunctionName

- **UUID**: `ebb5b0ab-0d1b-4b28-891b-09e9c514f3c6`
- **参数名**: `SmhFunctionName`
- **数据类型**: FUNCTION-NAME
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Name of the decryption function, e.g.:
SecM_DecryptAes128NoneEcb
SecM_DecryptAes128Iso7816_4Ecb
SecM_DecryptAes192PkcsCbc

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. SmhJobRef

- **UUID**: `fb7d327f-be61-4992-b1f9-5a3ac8104631`
- **引用名**: `SmhJobRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `SmhJob`
- **完整路径**: `/MICROSAR/Smh/SmhJob`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: This parameter refers to the used SmhDecryption job for decryption.

##### 3. SmhEncryptionConfig

**容器属性**:

- **UUID**: `c89fbaa2-0f61-4690-bc57-bdd20e86cb9a`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SmhEncryptionConfig`
- **多重性**: [0..infinite]
- **构建后可变**: false

**容器描述**:

Container to configure encryption jobs.

###### 参数配置

此容器包含 **1** 个参数：

####### FUNCTION-NAME 类型参数

######## 1. SmhFunctionName

- **UUID**: `e8d1db85-8613-4dfe-a3d5-6d7d6005ef8d`
- **参数名**: `SmhFunctionName`
- **数据类型**: FUNCTION-NAME
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Name of the encryption function, e.g.:
SecM_EncryptAes128NoneEcb
SecM_EncryptAes128Iso7816_4Ecb
SecM_EncryptAes192PkcsCbc

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. SmhJobRef

- **UUID**: `0ddfe8a6-affa-4dc6-bc23-8f0fb3d6f2a3`
- **引用名**: `SmhJobRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `SmhJob`
- **完整路径**: `/MICROSAR/Smh/SmhJob`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: This parameter refers to the used SmhEncryption job for encryption.

##### 4. SmhDecryptionConfig

**容器属性**:

- **UUID**: `72d0560c-1e26-4de4-bd30-a06eb5e1af3d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SmhDecryptionConfig`
- **多重性**: [0..infinite]
- **构建后可变**: false

**容器描述**:

Container to configure decryption jobs.

###### 参数配置

此容器包含 **1** 个参数：

####### FUNCTION-NAME 类型参数

######## 1. SmhFunctionName

- **UUID**: `ebb5b0ab-0d1b-4b28-891b-09e9c514f3c6`
- **参数名**: `SmhFunctionName`
- **数据类型**: FUNCTION-NAME
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Name of the decryption function, e.g.:
SecM_DecryptAes128NoneEcb
SecM_DecryptAes128Iso7816_4Ecb
SecM_DecryptAes192PkcsCbc

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. SmhJobRef

- **UUID**: `fb7d327f-be61-4992-b1f9-5a3ac8104631`
- **引用名**: `SmhJobRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `SmhJob`
- **完整路径**: `/MICROSAR/Smh/SmhJob`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: This parameter refers to the used SmhDecryption job for decryption.

##### 5. SmhSeedKey

**容器属性**:

- **UUID**: `f8d39132-1716-46c7-a1ff-78ead8396118`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SmhSeedKey`
- **多重性**: [1..1]
- **构建后可变**: false

**容器描述**:

Container for configuration of SeedKey (challenge/response authentication).

###### 参数配置

此容器包含 **2** 个参数：

####### INTEGER 类型参数

######## 1. SmhKeyTimeout

- **UUID**: `0d3559f1-d619-4e76-a9b6-b0e53d88d795`
- **参数名**: `SmhKeyTimeout`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `100`
- **取值范围**: [0..65535]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: This parameter is currently not used and is only provided for compatibility reasons to the HIS specification.
The timeout handling of the authorization is managed within the diagnostic layer, not in the security component according to OEM specification and cannot be adjusted.

######## 2. SmhCallCycle

- **UUID**: `83f51bb1-1369-4345-94c3-676d09c8a1f8`
- **参数名**: `SmhCallCycle`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `10`
- **取值范围**: [0..65535]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Specifies the call cycle to the function SecTask(). Commonly SecTask() is not used. In most cases this parameter is only for HIS-conformance.

###### 配置容器

本模块包含 **7** 个配置容器：

####### 1. SmhSeedConfig

**容器属性**:

- **UUID**: `5553626b-7ec2-4aa6-8fb2-1533e8c90233`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SmhSeedConfig`
- **多重性**: [1..1]
- **构建后可变**: false

**容器描述**:

Container to configure the Seed generation.

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. SmhSeedLength

- **UUID**: `9dddb4f3-4ac0-4853-8140-b7edea73e033`
- **参数名**: `SmhSeedLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `4`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Specify the length of the seed in bytes.

######### ENUMERATION 类型参数

########## 1. SmhSeedType

- **UUID**: `37aa55c6-a8fe-403e-adcc-daf44b005bc7`
- **参数名**: `SmhSeedType`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `HIS`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `HIS`
  - `BYTE_ARRAY`
  - `WORD_ARRAY`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Specify the data structure of the seed:
HIS: Seed is according to the HIS specification
BYTE_ARRAY: Seed is stored in a byte array
WORD_ARRAY: Seed is stored in a word array

Note: BYTE_ARRAY and WORD_ARRAY are deviation from the HIS specification.

######## 配置容器

本模块包含 **4** 个配置容器：

######### 1. SmhEntropy

**容器属性**:

- **UUID**: `494eb420-80fc-442a-b5e3-50c1455b3a9b`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SmhEntropy`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Specify if the Seed generation requires an entropy.

########## 参数配置

此容器包含 **2** 个参数：

########### INTEGER 类型参数

############ 1. SmhEntropySize

- **UUID**: `88cf5149-6faf-4cb0-8d38-d36acc951504`
- **参数名**: `SmhEntropySize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Size of the used entropy

########### ENUMERATION 类型参数

############ 1. SmhEntropyUsage

- **UUID**: `6c8b46bb-f15f-4615-8400-c71db30e531b`
- **参数名**: `SmhEntropyUsage`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `IMPLICIT`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `EXPLICIT`
  - `IMPLICIT`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Specify the usage of the entropy:
EXPLICIT: entropy musst be filled externnally
IMPLICIT: entropy is implicitly filled

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. SmhJobRef

- **UUID**: `8b3e1f14-58be-4cdc-8467-72993d40512e`
- **引用名**: `SmhJobRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `SmhRandomSeed`
- **完整路径**: `/MICROSAR/Smh/SmhJob/SmhRandomSeed`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: This parameter refers to the used SmhRandomSeed job to initialize the entropy.

######### 2. SmhCsm

**容器属性**:

- **UUID**: `23fd0911-1898-4ccb-9f75-512f3580d061`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SmhCsm`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container to configure a respecive SmhJob (CsmJob) to generate a seed.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. SmhJobRef

- **UUID**: `0171dca9-d1ad-476d-aa20-3ee98b90fb64`
- **引用名**: `SmhJobRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `SmhRandomGenerate`
- **完整路径**: `/MICROSAR/Smh/SmhJob/SmhRandomGenerate`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: This parameter refers to the used SmhRadomGenerate job to generate a seed.

######### 3. SmhLcg

**容器属性**:

- **UUID**: `a66578b7-37b5-46e6-9d2b-eeff5e61ac57`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SmhLcg`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container to configure the LCG (linear congruential generator) algorithm.

########## 参数配置

此容器包含 **2** 个参数：

########### INTEGER 类型参数

############ 1. SmhMultiplier

- **UUID**: `08163a60-bfa3-44ed-9017-fbe24b6d2f8d`
- **参数名**: `SmhMultiplier`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `2147001325`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Multiplier of the LCG algorithm.
Default value is taken from BCPL language.

############ 2. SmhIncrement

- **UUID**: `eeadce7a-1748-4f71-8720-a4198f8884b7`
- **参数名**: `SmhIncrement`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `715136305`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Increment of the LCG algorithm.
Default value is taken from BCPL language.

######### 4. SmhSeedGeneration

**容器属性**:

- **UUID**: `6198606c-04b9-421d-bafa-479b40d62f74`
- **容器类型**: CHOICE-CONTAINER
- **容器名称**: `SmhSeedGeneration`
- **多重性**: [1..1]
- **构建后可变**: false

**容器选择**:

- **SmhCsm**
  - UUID: `23fd0911-1898-4ccb-9f75-512f3580d061`
  - 描述: Container to configure a respecive SmhJob (CsmJob) to generate a seed.
- **SmhLcg**
  - UUID: `a66578b7-37b5-46e6-9d2b-eeff5e61ac57`
  - 描述: Container to configure the LCG (linear congruential generator) algorithm.

**容器描述**:

Specify the RNG algorithm

####### 2. SmhEntropy

**容器属性**:

- **UUID**: `494eb420-80fc-442a-b5e3-50c1455b3a9b`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SmhEntropy`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Specify if the Seed generation requires an entropy.

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. SmhEntropySize

- **UUID**: `88cf5149-6faf-4cb0-8d38-d36acc951504`
- **参数名**: `SmhEntropySize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Size of the used entropy

######### ENUMERATION 类型参数

########## 1. SmhEntropyUsage

- **UUID**: `6c8b46bb-f15f-4615-8400-c71db30e531b`
- **参数名**: `SmhEntropyUsage`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `IMPLICIT`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `EXPLICIT`
  - `IMPLICIT`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Specify the usage of the entropy:
EXPLICIT: entropy musst be filled externnally
IMPLICIT: entropy is implicitly filled

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. SmhJobRef

- **UUID**: `8b3e1f14-58be-4cdc-8467-72993d40512e`
- **引用名**: `SmhJobRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `SmhRandomSeed`
- **完整路径**: `/MICROSAR/Smh/SmhJob/SmhRandomSeed`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: This parameter refers to the used SmhRandomSeed job to initialize the entropy.

####### 3. SmhCsm

**容器属性**:

- **UUID**: `23fd0911-1898-4ccb-9f75-512f3580d061`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SmhCsm`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container to configure a respecive SmhJob (CsmJob) to generate a seed.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. SmhJobRef

- **UUID**: `0171dca9-d1ad-476d-aa20-3ee98b90fb64`
- **引用名**: `SmhJobRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `SmhRandomGenerate`
- **完整路径**: `/MICROSAR/Smh/SmhJob/SmhRandomGenerate`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: This parameter refers to the used SmhRadomGenerate job to generate a seed.

####### 4. SmhLcg

**容器属性**:

- **UUID**: `a66578b7-37b5-46e6-9d2b-eeff5e61ac57`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SmhLcg`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container to configure the LCG (linear congruential generator) algorithm.

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. SmhMultiplier

- **UUID**: `08163a60-bfa3-44ed-9017-fbe24b6d2f8d`
- **参数名**: `SmhMultiplier`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `2147001325`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Multiplier of the LCG algorithm.
Default value is taken from BCPL language.

########## 2. SmhIncrement

- **UUID**: `eeadce7a-1748-4f71-8720-a4198f8884b7`
- **参数名**: `SmhIncrement`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `715136305`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Increment of the LCG algorithm.
Default value is taken from BCPL language.

####### 5. SmhKeyConfig

**容器属性**:

- **UUID**: `c739fed7-6288-4444-9181-7255c2d33080`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SmhKeyConfig`
- **多重性**: [1..1]
- **构建后可变**: false

**容器描述**:

Container to configure the key computation parameter.

######## 参数配置

此容器包含 **7** 个参数：

######### INTEGER 类型参数

########## 1. SmhKeyConstant

- **UUID**: `ce941898-c6d5-4487-a8cd-6d347c0f1e15`
- **参数名**: `SmhKeyConstant`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: This is the key constant to adjust the authentication algorithm for a specific ype of ECU.

########## 2. SmhKeyLength

- **UUID**: `797e559d-1aac-4333-881a-3cf57273eb5e`
- **参数名**: `SmhKeyLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `4`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Specify the length of the key in bytes.

########## 3. SmhSecretKeyLength

- **UUID**: `86b85f85-0683-435d-845f-c7bb85c436f6`
- **参数名**: `SmhSecretKeyLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Specify the length of the secret key in bytes.

######### BOOLEAN 类型参数

########## 1. SmhExternalComparison

- **UUID**: `cd87c70b-bce6-44d6-93f0-6e37a655326f`
- **参数名**: `SmhExternalComparison`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: If enaled, the security module will call the function SecM_CompareKeyVendor. This function needs to performt the key computation and the comparison.

########## 2. SmhExtendedApi

- **UUID**: `5cb07f71-fe84-4d89-b495-ade71691de66`
- **参数名**: `SmhExtendedApi`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: If enabled, the parameter SecM_ConstType of SecM_ComputeKey (SecM_ComputeKeyVendor) will change to a structure containing an additional context member.
This is a deviation from the HIS specification. Modified to support configurations, where additional context information is required, e.g. workspace.

########## 3. SmhAsymmetric

- **UUID**: `22bb2b3e-d5ab-4236-9137-e46e4fe960fc`
- **参数名**: `SmhAsymmetric`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: If enabled, the API of SecM_ComputeKey (SecM_ComputeKeyVendor) will change from key=f(seed,k) to seed=f(key,k).
This is a deviation from the HIS specification. Modified to support asymmetric key calculation where only the tester is able to generate the key from the original seed value, e.g. using a private key.

######### ENUMERATION 类型参数

########## 1. SmhKeyType

- **UUID**: `92921747-2d45-4894-a8b6-32ffa4e083ed`
- **参数名**: `SmhKeyType`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `HIS`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `HIS`
  - `BYTE_ARRAY`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Specify the data structure of the key:
HIS: Key is according to the HIS specification
BYTE_ARRAY: Key is stored in a byte array

Note: BYTE_ARRAY are deviation from the HIS specification.

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. SmhKeyJobs

**容器属性**:

- **UUID**: `83115519-7b12-4078-bfba-a9abc1a0ff87`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SmhKeyJobs`
- **多重性**: [0..infinite]
- **构建后可变**: false

**容器描述**:

Container to configure several SmhJobs, which can be used by SecM_ComputeKeyVendor or SecM_CompareKeyVendor.

########## 参数配置

此容器包含 **1** 个参数：

########### FUNCTION-NAME 类型参数

############ 1. SmhFunctionName

- **UUID**: `6b673fea-a66f-4b9a-af5d-8159cf395b03`
- **参数名**: `SmhFunctionName`
- **数据类型**: FUNCTION-NAME
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Configure the function name of the key computation job, e.g.:
- SecM_SeedKeySha512
- SecM_SeedKeyEncrypt

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. SmhJobRef

- **UUID**: `7df7d03d-a9b1-438d-a857-eda5e18381c1`
- **引用名**: `SmhJobRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `SmhJob`
- **完整路径**: `/MICROSAR/Smh/SmhJob`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: References a SmhJob, which shall be used by the key computation.

####### 6. SmhKeyJobs

**容器属性**:

- **UUID**: `83115519-7b12-4078-bfba-a9abc1a0ff87`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SmhKeyJobs`
- **多重性**: [0..infinite]
- **构建后可变**: false

**容器描述**:

Container to configure several SmhJobs, which can be used by SecM_ComputeKeyVendor or SecM_CompareKeyVendor.

######## 参数配置

此容器包含 **1** 个参数：

######### FUNCTION-NAME 类型参数

########## 1. SmhFunctionName

- **UUID**: `6b673fea-a66f-4b9a-af5d-8159cf395b03`
- **参数名**: `SmhFunctionName`
- **数据类型**: FUNCTION-NAME
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Configure the function name of the key computation job, e.g.:
- SecM_SeedKeySha512
- SecM_SeedKeyEncrypt

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. SmhJobRef

- **UUID**: `7df7d03d-a9b1-438d-a857-eda5e18381c1`
- **引用名**: `SmhJobRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `SmhJob`
- **完整路径**: `/MICROSAR/Smh/SmhJob`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: References a SmhJob, which shall be used by the key computation.

####### 7. SmhSeedGeneration

**容器属性**:

- **UUID**: `6198606c-04b9-421d-bafa-479b40d62f74`
- **容器类型**: CHOICE-CONTAINER
- **容器名称**: `SmhSeedGeneration`
- **多重性**: [1..1]
- **构建后可变**: false

**容器选择**:

- **SmhCsm**
  - UUID: `23fd0911-1898-4ccb-9f75-512f3580d061`
  - 描述: Container to configure a respecive SmhJob (CsmJob) to generate a seed.
- **SmhLcg**
  - UUID: `a66578b7-37b5-46e6-9d2b-eeff5e61ac57`
  - 描述: Container to configure the LCG (linear congruential generator) algorithm.

**容器描述**:

Specify the RNG algorithm

##### 6. SmhSeedConfig

**容器属性**:

- **UUID**: `5553626b-7ec2-4aa6-8fb2-1533e8c90233`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SmhSeedConfig`
- **多重性**: [1..1]
- **构建后可变**: false

**容器描述**:

Container to configure the Seed generation.

###### 参数配置

此容器包含 **2** 个参数：

####### INTEGER 类型参数

######## 1. SmhSeedLength

- **UUID**: `9dddb4f3-4ac0-4853-8140-b7edea73e033`
- **参数名**: `SmhSeedLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `4`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Specify the length of the seed in bytes.

####### ENUMERATION 类型参数

######## 1. SmhSeedType

- **UUID**: `37aa55c6-a8fe-403e-adcc-daf44b005bc7`
- **参数名**: `SmhSeedType`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `HIS`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `HIS`
  - `BYTE_ARRAY`
  - `WORD_ARRAY`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Specify the data structure of the seed:
HIS: Seed is according to the HIS specification
BYTE_ARRAY: Seed is stored in a byte array
WORD_ARRAY: Seed is stored in a word array

Note: BYTE_ARRAY and WORD_ARRAY are deviation from the HIS specification.

###### 配置容器

本模块包含 **4** 个配置容器：

####### 1. SmhEntropy

**容器属性**:

- **UUID**: `494eb420-80fc-442a-b5e3-50c1455b3a9b`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SmhEntropy`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Specify if the Seed generation requires an entropy.

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. SmhEntropySize

- **UUID**: `88cf5149-6faf-4cb0-8d38-d36acc951504`
- **参数名**: `SmhEntropySize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Size of the used entropy

######### ENUMERATION 类型参数

########## 1. SmhEntropyUsage

- **UUID**: `6c8b46bb-f15f-4615-8400-c71db30e531b`
- **参数名**: `SmhEntropyUsage`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `IMPLICIT`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `EXPLICIT`
  - `IMPLICIT`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Specify the usage of the entropy:
EXPLICIT: entropy musst be filled externnally
IMPLICIT: entropy is implicitly filled

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. SmhJobRef

- **UUID**: `8b3e1f14-58be-4cdc-8467-72993d40512e`
- **引用名**: `SmhJobRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `SmhRandomSeed`
- **完整路径**: `/MICROSAR/Smh/SmhJob/SmhRandomSeed`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: This parameter refers to the used SmhRandomSeed job to initialize the entropy.

####### 2. SmhCsm

**容器属性**:

- **UUID**: `23fd0911-1898-4ccb-9f75-512f3580d061`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SmhCsm`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container to configure a respecive SmhJob (CsmJob) to generate a seed.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. SmhJobRef

- **UUID**: `0171dca9-d1ad-476d-aa20-3ee98b90fb64`
- **引用名**: `SmhJobRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `SmhRandomGenerate`
- **完整路径**: `/MICROSAR/Smh/SmhJob/SmhRandomGenerate`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: This parameter refers to the used SmhRadomGenerate job to generate a seed.

####### 3. SmhLcg

**容器属性**:

- **UUID**: `a66578b7-37b5-46e6-9d2b-eeff5e61ac57`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SmhLcg`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container to configure the LCG (linear congruential generator) algorithm.

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. SmhMultiplier

- **UUID**: `08163a60-bfa3-44ed-9017-fbe24b6d2f8d`
- **参数名**: `SmhMultiplier`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `2147001325`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Multiplier of the LCG algorithm.
Default value is taken from BCPL language.

########## 2. SmhIncrement

- **UUID**: `eeadce7a-1748-4f71-8720-a4198f8884b7`
- **参数名**: `SmhIncrement`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `715136305`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Increment of the LCG algorithm.
Default value is taken from BCPL language.

####### 4. SmhSeedGeneration

**容器属性**:

- **UUID**: `6198606c-04b9-421d-bafa-479b40d62f74`
- **容器类型**: CHOICE-CONTAINER
- **容器名称**: `SmhSeedGeneration`
- **多重性**: [1..1]
- **构建后可变**: false

**容器选择**:

- **SmhCsm**
  - UUID: `23fd0911-1898-4ccb-9f75-512f3580d061`
  - 描述: Container to configure a respecive SmhJob (CsmJob) to generate a seed.
- **SmhLcg**
  - UUID: `a66578b7-37b5-46e6-9d2b-eeff5e61ac57`
  - 描述: Container to configure the LCG (linear congruential generator) algorithm.

**容器描述**:

Specify the RNG algorithm

##### 7. SmhEntropy

**容器属性**:

- **UUID**: `494eb420-80fc-442a-b5e3-50c1455b3a9b`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SmhEntropy`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Specify if the Seed generation requires an entropy.

###### 参数配置

此容器包含 **2** 个参数：

####### INTEGER 类型参数

######## 1. SmhEntropySize

- **UUID**: `88cf5149-6faf-4cb0-8d38-d36acc951504`
- **参数名**: `SmhEntropySize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Size of the used entropy

####### ENUMERATION 类型参数

######## 1. SmhEntropyUsage

- **UUID**: `6c8b46bb-f15f-4615-8400-c71db30e531b`
- **参数名**: `SmhEntropyUsage`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `IMPLICIT`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `EXPLICIT`
  - `IMPLICIT`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Specify the usage of the entropy:
EXPLICIT: entropy musst be filled externnally
IMPLICIT: entropy is implicitly filled

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. SmhJobRef

- **UUID**: `8b3e1f14-58be-4cdc-8467-72993d40512e`
- **引用名**: `SmhJobRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `SmhRandomSeed`
- **完整路径**: `/MICROSAR/Smh/SmhJob/SmhRandomSeed`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: This parameter refers to the used SmhRandomSeed job to initialize the entropy.

##### 8. SmhCsm

**容器属性**:

- **UUID**: `23fd0911-1898-4ccb-9f75-512f3580d061`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SmhCsm`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container to configure a respecive SmhJob (CsmJob) to generate a seed.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. SmhJobRef

- **UUID**: `0171dca9-d1ad-476d-aa20-3ee98b90fb64`
- **引用名**: `SmhJobRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `SmhRandomGenerate`
- **完整路径**: `/MICROSAR/Smh/SmhJob/SmhRandomGenerate`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: This parameter refers to the used SmhRadomGenerate job to generate a seed.

##### 9. SmhLcg

**容器属性**:

- **UUID**: `a66578b7-37b5-46e6-9d2b-eeff5e61ac57`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SmhLcg`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container to configure the LCG (linear congruential generator) algorithm.

###### 参数配置

此容器包含 **2** 个参数：

####### INTEGER 类型参数

######## 1. SmhMultiplier

- **UUID**: `08163a60-bfa3-44ed-9017-fbe24b6d2f8d`
- **参数名**: `SmhMultiplier`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `2147001325`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Multiplier of the LCG algorithm.
Default value is taken from BCPL language.

######## 2. SmhIncrement

- **UUID**: `eeadce7a-1748-4f71-8720-a4198f8884b7`
- **参数名**: `SmhIncrement`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `715136305`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Increment of the LCG algorithm.
Default value is taken from BCPL language.

##### 10. SmhKeyConfig

**容器属性**:

- **UUID**: `c739fed7-6288-4444-9181-7255c2d33080`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SmhKeyConfig`
- **多重性**: [1..1]
- **构建后可变**: false

**容器描述**:

Container to configure the key computation parameter.

###### 参数配置

此容器包含 **7** 个参数：

####### INTEGER 类型参数

######## 1. SmhKeyConstant

- **UUID**: `ce941898-c6d5-4487-a8cd-6d347c0f1e15`
- **参数名**: `SmhKeyConstant`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: This is the key constant to adjust the authentication algorithm for a specific ype of ECU.

######## 2. SmhKeyLength

- **UUID**: `797e559d-1aac-4333-881a-3cf57273eb5e`
- **参数名**: `SmhKeyLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `4`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Specify the length of the key in bytes.

######## 3. SmhSecretKeyLength

- **UUID**: `86b85f85-0683-435d-845f-c7bb85c436f6`
- **参数名**: `SmhSecretKeyLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Specify the length of the secret key in bytes.

####### BOOLEAN 类型参数

######## 1. SmhExternalComparison

- **UUID**: `cd87c70b-bce6-44d6-93f0-6e37a655326f`
- **参数名**: `SmhExternalComparison`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: If enaled, the security module will call the function SecM_CompareKeyVendor. This function needs to performt the key computation and the comparison.

######## 2. SmhExtendedApi

- **UUID**: `5cb07f71-fe84-4d89-b495-ade71691de66`
- **参数名**: `SmhExtendedApi`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: If enabled, the parameter SecM_ConstType of SecM_ComputeKey (SecM_ComputeKeyVendor) will change to a structure containing an additional context member.
This is a deviation from the HIS specification. Modified to support configurations, where additional context information is required, e.g. workspace.

######## 3. SmhAsymmetric

- **UUID**: `22bb2b3e-d5ab-4236-9137-e46e4fe960fc`
- **参数名**: `SmhAsymmetric`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: If enabled, the API of SecM_ComputeKey (SecM_ComputeKeyVendor) will change from key=f(seed,k) to seed=f(key,k).
This is a deviation from the HIS specification. Modified to support asymmetric key calculation where only the tester is able to generate the key from the original seed value, e.g. using a private key.

####### ENUMERATION 类型参数

######## 1. SmhKeyType

- **UUID**: `92921747-2d45-4894-a8b6-32ffa4e083ed`
- **参数名**: `SmhKeyType`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `HIS`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `HIS`
  - `BYTE_ARRAY`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Specify the data structure of the key:
HIS: Key is according to the HIS specification
BYTE_ARRAY: Key is stored in a byte array

Note: BYTE_ARRAY are deviation from the HIS specification.

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. SmhKeyJobs

**容器属性**:

- **UUID**: `83115519-7b12-4078-bfba-a9abc1a0ff87`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SmhKeyJobs`
- **多重性**: [0..infinite]
- **构建后可变**: false

**容器描述**:

Container to configure several SmhJobs, which can be used by SecM_ComputeKeyVendor or SecM_CompareKeyVendor.

######## 参数配置

此容器包含 **1** 个参数：

######### FUNCTION-NAME 类型参数

########## 1. SmhFunctionName

- **UUID**: `6b673fea-a66f-4b9a-af5d-8159cf395b03`
- **参数名**: `SmhFunctionName`
- **数据类型**: FUNCTION-NAME
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Configure the function name of the key computation job, e.g.:
- SecM_SeedKeySha512
- SecM_SeedKeyEncrypt

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. SmhJobRef

- **UUID**: `7df7d03d-a9b1-438d-a857-eda5e18381c1`
- **引用名**: `SmhJobRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `SmhJob`
- **完整路径**: `/MICROSAR/Smh/SmhJob`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: References a SmhJob, which shall be used by the key computation.

##### 11. SmhKeyJobs

**容器属性**:

- **UUID**: `83115519-7b12-4078-bfba-a9abc1a0ff87`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SmhKeyJobs`
- **多重性**: [0..infinite]
- **构建后可变**: false

**容器描述**:

Container to configure several SmhJobs, which can be used by SecM_ComputeKeyVendor or SecM_CompareKeyVendor.

###### 参数配置

此容器包含 **1** 个参数：

####### FUNCTION-NAME 类型参数

######## 1. SmhFunctionName

- **UUID**: `6b673fea-a66f-4b9a-af5d-8159cf395b03`
- **参数名**: `SmhFunctionName`
- **数据类型**: FUNCTION-NAME
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Configure the function name of the key computation job, e.g.:
- SecM_SeedKeySha512
- SecM_SeedKeyEncrypt

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. SmhJobRef

- **UUID**: `7df7d03d-a9b1-438d-a857-eda5e18381c1`
- **引用名**: `SmhJobRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `SmhJob`
- **完整路径**: `/MICROSAR/Smh/SmhJob`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: References a SmhJob, which shall be used by the key computation.

##### 12. SmhVerification

**容器属性**:

- **UUID**: `cff279e2-a20c-4caa-b48e-962f65c4a9d7`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SmhVerification`
- **多重性**: [1..1]
- **构建后可变**: false

**容器描述**:

Container to configure the HIS security class
DDD: CRC and hash
C: MAC
CCC: Signatures

###### 配置容器

本模块包含 **22** 个配置容器：

####### 1. SmhMonolithicVerification

**容器属性**:

- **UUID**: `b6db6564-d81b-48ce-8949-a13fdbe982db`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SmhMonolithicVerification`
- **多重性**: [1..1]
- **构建后可变**: false

**容器描述**:

Container to configure the monolythic verifications.
Monolythic verifications are used to verify the data after a complete download has been performed (OutputVerification).

######## 参数配置

此容器包含 **9** 个参数：

######### INTEGER 类型参数

########## 1. SmhOperationCountOfWrapper

- **UUID**: `ac221637-3218-4e9d-a2db-22bf43e94484`
- **参数名**: `SmhOperationCountOfWrapper`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `4`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Specify the number of operations:
- SecurityClass Verification
- CRC Total
- Vendor Verification
- CRC Written

########## 2. SmhReadBufferSize

- **UUID**: `19c23fb8-4d2c-4b43-b461-b20127cf10d7`
- **参数名**: `SmhReadBufferSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `64`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Specify the length of the read buffer. The security module will read data with this size from the memory and provides it to the verification function.

######### BOOLEAN 类型参数

########## 1. SmhExportVerificationWrapper

- **UUID**: `e0ddce9a-544a-4eb5-ab83-be5fe8b8a436`
- **参数名**: `SmhExportVerificationWrapper`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Configure if the function SecM_VerificationWrapper can be accessed externally.

########## 2. SmhCheckAddressRangeOverflow

- **UUID**: `af4b6b53-a14e-4a52-90ea-917f9d0ecc81`
- **参数名**: `SmhCheckAddressRangeOverflow`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: If enable, the security module will check that the memory range defined by address and length create an address range overflow.

########## 3. SmhAssertReadCount

- **UUID**: `2490e6b2-ef15-4258-8517-7bbf2146f0b8`
- **参数名**: `SmhAssertReadCount`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Enabled a check to verify that the read count matches the requested read length.

########## 4. SmhCRCTotal

- **UUID**: `1635db7f-a97e-48d4-a121-db760ce89659`
- **参数名**: `SmhCRCTotal`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: The security component always calculates a CRCtotal for a logical block when enabled. Thus, the application is able to verify the values within the application.

########## 5. SmhCRCWritten

- **UUID**: `44d762fd-44f3-4688-a85f-c46cad743e7a`
- **参数名**: `SmhCRCWritten`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: The security component calculates the CRC value of the written (segments) data and compares it against the provided verification data at offset SmhCRCOffset.

########## 6. SmhCRCWrittenGet

- **UUID**: `28122ec7-1abf-40f1-a967-bc5575af82b4`
- **参数名**: `SmhCRCWrittenGet`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: The security component calculates the CRC value of the written (segments) data and provides it to the caller to be verified externally.

######### ENUMERATION 类型参数

########## 1. SmhMemoryAccessMode

- **UUID**: `70e0f7fd-6349-48b0-8968-2e46728f03ca`
- **参数名**: `SmhMemoryAccessMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `ADDRESS`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `ADDRESS` (来源: Vector Informatik)
  - `FILE` (来源: Vector Informatik)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: The access mode of the security component is fixed to the memory access function. The setting is displayed for documentation purposes only.

######## 引用关系

此容器包含 **1** 个引用：

######### CHOICE-REFERENCE 类型引用

########## 1. SmhDefaultMonolithicVerificationConfig

- **UUID**: `0839edb9-4fa5-43f9-b0cd-d467cfb2d009`
- **引用名**: `SmhDefaultMonolithicVerificationConfig`
- **引用类型**: CHOICE-REFERENCE
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **需要索引**: false
- **目标引用列表**:
  - `/MICROSAR/Smh/SmhVerification/SmhMonolithicVerification/SmhSecurityClassDDD/SmhSecurityClassDDDConfig`
  - `/MICROSAR/Smh/SmhVerification/SmhMonolithicVerification/SmhSecurityClassC/SmhSecurityClassCConfig`
  - `/MICROSAR/Smh/SmhVerification/SmhMonolithicVerification/SmhSecurityClassCCC/SmhSecurityClassCCCConfig`
  - `/MICROSAR/Smh/SmhVerification/SmhMonolithicVerification/SmhSecurityClassVendor/SmhSecurityClassVendorConfig`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Default monolithic verification:
SecM_Verification

######## 配置容器

本模块包含 **8** 个配置容器：

######### 1. SmhSecurityClassDDD

**容器属性**:

- **UUID**: `72791700-82db-4ae8-913d-546993a59628`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SmhSecurityClassDDD`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container to configure the monolythic verification for security class DDD.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. SmhDefaultSecurityClassDDDConfig

- **UUID**: `8000ac6e-db98-4d89-ad2e-e5d407d6e2cf`
- **引用名**: `SmhDefaultSecurityClassDDDConfig`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `SmhSecurityClassDDDConfig`
- **完整路径**: `/MICROSAR/Smh/SmhVerification/SmhMonolithicVerification/SmhSecurityClassDDD/SmhSecurityClassDDDConfig`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Default monolythic verification for the security class DDD:
SecM_VerificationClassDDD

########## 配置容器

本模块包含 **1** 个配置容器：

########### 1. SmhSecurityClassDDDConfig

**容器属性**:

- **UUID**: `8b918e7c-9888-4c0f-ab87-064e3f447ed8`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SmhSecurityClassDDDConfig`
- **多重性**: [1..infinite]
- **构建后可变**: false

**容器描述**:

Container to configure the monolythic verifications for security class DDD.

############ 参数配置

此容器包含 **4** 个参数：

############# INTEGER 类型参数

############## 1. SmhSignatureOffset

- **UUID**: `058834c9-af5f-4982-885e-fbfd6a591f78`
- **参数名**: `SmhSignatureOffset`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Specify the offset to the signature (CRC or hash value).

############## 2. SmhCRCOffset

- **UUID**: `f9ad26cf-04f7-460c-bb94-5033c8c860a6`
- **参数名**: `SmhCRCOffset`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Specify the offset to the CRC value (used by CRC written)

############# BOOLEAN 类型参数

############## 1. SmhIncludeAddressAndLengthInSignature

- **UUID**: `db44bc4a-9cca-473b-896d-be630b6785e9`
- **参数名**: `SmhIncludeAddressAndLengthInSignature`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Specify if the address and length of the segments shall be taken into account in the verification.

############# FUNCTION-NAME 类型参数

############## 1. SmhFunctionName

- **UUID**: `ab733ae7-604b-4644-98db-a29bf0b8b00b`
- **参数名**: `SmhFunctionName`
- **数据类型**: FUNCTION-NAME
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Configure the function name to execute the monolythic verification, e.g.:
- SecM_VerificationClassDDD_Crc32
- SecM_VerificationClassDDD_Sha512

############ 引用关系

此容器包含 **2** 个引用：

############# REFERENCE 类型引用

############## 1. SmhStreamVerificationConfig

- **UUID**: `06866c75-743e-46f3-98cd-693b08a484a1`
- **引用名**: `SmhStreamVerificationConfig`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `SmhSecurityClassDDDConfig`
- **完整路径**: `/MICROSAR/Smh/SmhVerification/SmhStreamVerification/SmhSecurityClassDDD/SmhSecurityClassDDDConfig`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Reference to the underlying StreamVerification to eecute the verification operation.

############## 2. SmhVendorVerificationConfig

- **UUID**: `22a7ef68-050b-43d2-9efa-64b75baf9e7b`
- **引用名**: `SmhVendorVerificationConfig`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `SmhSecurityClassVendorConfig`
- **完整路径**: `/MICROSAR/Smh/SmhVerification/SmhStreamVerification/SmhSecurityClassVendor/SmhSecurityClassVendorConfig`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Reference to a VendorVerification to execute next to the CRC/hash verification an additional vendor checksum.

######### 2. SmhSecurityClassDDDConfig

**容器属性**:

- **UUID**: `8b918e7c-9888-4c0f-ab87-064e3f447ed8`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SmhSecurityClassDDDConfig`
- **多重性**: [1..infinite]
- **构建后可变**: false

**容器描述**:

Container to configure the monolythic verifications for security class DDD.

########## 参数配置

此容器包含 **4** 个参数：

########### INTEGER 类型参数

############ 1. SmhSignatureOffset

- **UUID**: `058834c9-af5f-4982-885e-fbfd6a591f78`
- **参数名**: `SmhSignatureOffset`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Specify the offset to the signature (CRC or hash value).

############ 2. SmhCRCOffset

- **UUID**: `f9ad26cf-04f7-460c-bb94-5033c8c860a6`
- **参数名**: `SmhCRCOffset`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Specify the offset to the CRC value (used by CRC written)

########### BOOLEAN 类型参数

############ 1. SmhIncludeAddressAndLengthInSignature

- **UUID**: `db44bc4a-9cca-473b-896d-be630b6785e9`
- **参数名**: `SmhIncludeAddressAndLengthInSignature`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Specify if the address and length of the segments shall be taken into account in the verification.

########### FUNCTION-NAME 类型参数

############ 1. SmhFunctionName

- **UUID**: `ab733ae7-604b-4644-98db-a29bf0b8b00b`
- **参数名**: `SmhFunctionName`
- **数据类型**: FUNCTION-NAME
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Configure the function name to execute the monolythic verification, e.g.:
- SecM_VerificationClassDDD_Crc32
- SecM_VerificationClassDDD_Sha512

########## 引用关系

此容器包含 **2** 个引用：

########### REFERENCE 类型引用

############ 1. SmhStreamVerificationConfig

- **UUID**: `06866c75-743e-46f3-98cd-693b08a484a1`
- **引用名**: `SmhStreamVerificationConfig`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `SmhSecurityClassDDDConfig`
- **完整路径**: `/MICROSAR/Smh/SmhVerification/SmhStreamVerification/SmhSecurityClassDDD/SmhSecurityClassDDDConfig`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Reference to the underlying StreamVerification to eecute the verification operation.

############ 2. SmhVendorVerificationConfig

- **UUID**: `22a7ef68-050b-43d2-9efa-64b75baf9e7b`
- **引用名**: `SmhVendorVerificationConfig`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `SmhSecurityClassVendorConfig`
- **完整路径**: `/MICROSAR/Smh/SmhVerification/SmhStreamVerification/SmhSecurityClassVendor/SmhSecurityClassVendorConfig`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Reference to a VendorVerification to execute next to the CRC/hash verification an additional vendor checksum.

######### 3. SmhSecurityClassC

**容器属性**:

- **UUID**: `9184de9d-b87a-4814-9987-c262b26ccff8`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SmhSecurityClassC`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container to configure the monolythic verification for security class C.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. SmhDefaultSecurityClassCConfig

- **UUID**: `1bb8a08a-2a06-4fad-8757-e8b4999d7a9a`
- **引用名**: `SmhDefaultSecurityClassCConfig`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `SmhSecurityClassCConfig`
- **完整路径**: `/MICROSAR/Smh/SmhVerification/SmhMonolithicVerification/SmhSecurityClassC/SmhSecurityClassCConfig`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Default monolythic verification for the security class C:
SecM_VerificationClassC

########## 配置容器

本模块包含 **1** 个配置容器：

########### 1. SmhSecurityClassCConfig

**容器属性**:

- **UUID**: `08f7a3a0-55c3-4440-bbad-8652231c1afc`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SmhSecurityClassCConfig`
- **多重性**: [1..infinite]
- **构建后可变**: false

**容器描述**:

Container to configure the monolythic verifications for security class C.

############ 参数配置

此容器包含 **4** 个参数：

############# INTEGER 类型参数

############## 1. SmhSignatureOffset

- **UUID**: `2e0853f6-5158-49bb-8a43-0ee955c15bff`
- **参数名**: `SmhSignatureOffset`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Specify the offset to the signature (MAC).

############## 2. SmhCRCOffset

- **UUID**: `9d9b2b54-743d-4914-a914-a375452a81c9`
- **参数名**: `SmhCRCOffset`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Specify the offset to the CRC value (used by CRC written)

############# BOOLEAN 类型参数

############## 1. SmhIncludeAddressAndLengthInSignature

- **UUID**: `e26fa671-08c7-466b-a1a7-de82db5c676c`
- **参数名**: `SmhIncludeAddressAndLengthInSignature`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Specify if the address and length of the segments shall be taken into account in the verification.

############# FUNCTION-NAME 类型参数

############## 1. SmhFunctionName

- **UUID**: `9bd34e8a-f73d-4e0a-9dc9-203ffa5b98ca`
- **参数名**: `SmhFunctionName`
- **数据类型**: FUNCTION-NAME
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Configure the function name to execute the monolythic verification, e.g.:
- SecM_VerificationClassC_HmacSha1
- SecM_VerificationClassC_Cmac

############ 引用关系

此容器包含 **2** 个引用：

############# REFERENCE 类型引用

############## 1. SmhStreamVerificationConfig

- **UUID**: `f7ef63f9-fff4-4b04-a90e-3cbdd667497e`
- **引用名**: `SmhStreamVerificationConfig`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `SmhSecurityClassCConfig`
- **完整路径**: `/MICROSAR/Smh/SmhVerification/SmhStreamVerification/SmhSecurityClassC/SmhSecurityClassCConfig`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Reference to the underlying StreamVerification to eecute the verification operation.

############## 2. SmhVendorVerificationConfig

- **UUID**: `901c9188-01b4-4c53-ac2d-0d0fb0a5359e`
- **引用名**: `SmhVendorVerificationConfig`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `SmhSecurityClassVendorConfig`
- **完整路径**: `/MICROSAR/Smh/SmhVerification/SmhStreamVerification/SmhSecurityClassVendor/SmhSecurityClassVendorConfig`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Reference to a VendorVerification to execute next to the MAC verification an additional vendor checksum.

######### 4. SmhSecurityClassCConfig

**容器属性**:

- **UUID**: `08f7a3a0-55c3-4440-bbad-8652231c1afc`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SmhSecurityClassCConfig`
- **多重性**: [1..infinite]
- **构建后可变**: false

**容器描述**:

Container to configure the monolythic verifications for security class C.

########## 参数配置

此容器包含 **4** 个参数：

########### INTEGER 类型参数

############ 1. SmhSignatureOffset

- **UUID**: `2e0853f6-5158-49bb-8a43-0ee955c15bff`
- **参数名**: `SmhSignatureOffset`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Specify the offset to the signature (MAC).

############ 2. SmhCRCOffset

- **UUID**: `9d9b2b54-743d-4914-a914-a375452a81c9`
- **参数名**: `SmhCRCOffset`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Specify the offset to the CRC value (used by CRC written)

########### BOOLEAN 类型参数

############ 1. SmhIncludeAddressAndLengthInSignature

- **UUID**: `e26fa671-08c7-466b-a1a7-de82db5c676c`
- **参数名**: `SmhIncludeAddressAndLengthInSignature`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Specify if the address and length of the segments shall be taken into account in the verification.

########### FUNCTION-NAME 类型参数

############ 1. SmhFunctionName

- **UUID**: `9bd34e8a-f73d-4e0a-9dc9-203ffa5b98ca`
- **参数名**: `SmhFunctionName`
- **数据类型**: FUNCTION-NAME
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Configure the function name to execute the monolythic verification, e.g.:
- SecM_VerificationClassC_HmacSha1
- SecM_VerificationClassC_Cmac

########## 引用关系

此容器包含 **2** 个引用：

########### REFERENCE 类型引用

############ 1. SmhStreamVerificationConfig

- **UUID**: `f7ef63f9-fff4-4b04-a90e-3cbdd667497e`
- **引用名**: `SmhStreamVerificationConfig`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `SmhSecurityClassCConfig`
- **完整路径**: `/MICROSAR/Smh/SmhVerification/SmhStreamVerification/SmhSecurityClassC/SmhSecurityClassCConfig`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Reference to the underlying StreamVerification to eecute the verification operation.

############ 2. SmhVendorVerificationConfig

- **UUID**: `901c9188-01b4-4c53-ac2d-0d0fb0a5359e`
- **引用名**: `SmhVendorVerificationConfig`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `SmhSecurityClassVendorConfig`
- **完整路径**: `/MICROSAR/Smh/SmhVerification/SmhStreamVerification/SmhSecurityClassVendor/SmhSecurityClassVendorConfig`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Reference to a VendorVerification to execute next to the MAC verification an additional vendor checksum.

######### 5. SmhSecurityClassCCC

**容器属性**:

- **UUID**: `4ab7b0b3-e998-4914-bdd3-8ba54bf23f77`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SmhSecurityClassCCC`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container to configure the monolythic verification for security class CCC.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. SmhDefaultSecurityClassCCCConfig

- **UUID**: `9da32213-c156-452a-82af-9db07b263858`
- **引用名**: `SmhDefaultSecurityClassCCCConfig`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `SmhSecurityClassCCCConfig`
- **完整路径**: `/MICROSAR/Smh/SmhVerification/SmhMonolithicVerification/SmhSecurityClassCCC/SmhSecurityClassCCCConfig`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Default monolythic verification for the security class CCC:
SecM_VerificationClassCCC

########## 配置容器

本模块包含 **1** 个配置容器：

########### 1. SmhSecurityClassCCCConfig

**容器属性**:

- **UUID**: `bb62362a-8553-4d60-a926-a0270adeb73f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SmhSecurityClassCCCConfig`
- **多重性**: [1..infinite]
- **构建后可变**: false

**容器描述**:

Container to configure the monolythic verifications for security class CCC.

############ 参数配置

此容器包含 **4** 个参数：

############# INTEGER 类型参数

############## 1. SmhSignatureOffset

- **UUID**: `8cb8417a-f4e7-4fd7-b389-73e568cbd189`
- **参数名**: `SmhSignatureOffset`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Specify the offset to the signature.

############## 2. SmhCRCOffset

- **UUID**: `00c2cec6-726b-4e53-b151-e8685d67c400`
- **参数名**: `SmhCRCOffset`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Specify the offset to the CRC value (used by CRC written)

############# BOOLEAN 类型参数

############## 1. SmhIncludeAddressAndLengthInSignature

- **UUID**: `97a43d7c-7ece-4506-946e-751f23cee541`
- **参数名**: `SmhIncludeAddressAndLengthInSignature`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Specify if the address and length of the segments shall be taken into account in the verification.

############# FUNCTION-NAME 类型参数

############## 1. SmhFunctionName

- **UUID**: `442fdcd9-13f7-4614-98c5-950f0ed8cee1`
- **参数名**: `SmhFunctionName`
- **数据类型**: FUNCTION-NAME
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Configure the function name to execute the monolythic verification, e.g.:
- SecM_VerificationClassCCC_RsaPssSha256
- SecM_VerificationClassCCC_Ed25519PH

############ 引用关系

此容器包含 **2** 个引用：

############# REFERENCE 类型引用

############## 1. SmhStreamVerificationConfig

- **UUID**: `d59861ca-8eba-456e-b4cf-b28f96b0d983`
- **引用名**: `SmhStreamVerificationConfig`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `SmhSecurityClassCCCConfig`
- **完整路径**: `/MICROSAR/Smh/SmhVerification/SmhStreamVerification/SmhSecurityClassCCC/SmhSecurityClassCCCConfig`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Reference to the underlying StreamVerification to eecute the verification operation.

############## 2. SmhVendorVerificationConfig

- **UUID**: `aae4bd8b-20f5-4871-96c6-f240fa3f4dc4`
- **引用名**: `SmhVendorVerificationConfig`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `SmhSecurityClassVendorConfig`
- **完整路径**: `/MICROSAR/Smh/SmhVerification/SmhStreamVerification/SmhSecurityClassVendor/SmhSecurityClassVendorConfig`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Reference to a VendorVerification to execute next to the signature verification an additional vendor checksum.

######### 6. SmhSecurityClassCCCConfig

**容器属性**:

- **UUID**: `bb62362a-8553-4d60-a926-a0270adeb73f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SmhSecurityClassCCCConfig`
- **多重性**: [1..infinite]
- **构建后可变**: false

**容器描述**:

Container to configure the monolythic verifications for security class CCC.

########## 参数配置

此容器包含 **4** 个参数：

########### INTEGER 类型参数

############ 1. SmhSignatureOffset

- **UUID**: `8cb8417a-f4e7-4fd7-b389-73e568cbd189`
- **参数名**: `SmhSignatureOffset`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Specify the offset to the signature.

############ 2. SmhCRCOffset

- **UUID**: `00c2cec6-726b-4e53-b151-e8685d67c400`
- **参数名**: `SmhCRCOffset`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Specify the offset to the CRC value (used by CRC written)

########### BOOLEAN 类型参数

############ 1. SmhIncludeAddressAndLengthInSignature

- **UUID**: `97a43d7c-7ece-4506-946e-751f23cee541`
- **参数名**: `SmhIncludeAddressAndLengthInSignature`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Specify if the address and length of the segments shall be taken into account in the verification.

########### FUNCTION-NAME 类型参数

############ 1. SmhFunctionName

- **UUID**: `442fdcd9-13f7-4614-98c5-950f0ed8cee1`
- **参数名**: `SmhFunctionName`
- **数据类型**: FUNCTION-NAME
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Configure the function name to execute the monolythic verification, e.g.:
- SecM_VerificationClassCCC_RsaPssSha256
- SecM_VerificationClassCCC_Ed25519PH

########## 引用关系

此容器包含 **2** 个引用：

########### REFERENCE 类型引用

############ 1. SmhStreamVerificationConfig

- **UUID**: `d59861ca-8eba-456e-b4cf-b28f96b0d983`
- **引用名**: `SmhStreamVerificationConfig`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `SmhSecurityClassCCCConfig`
- **完整路径**: `/MICROSAR/Smh/SmhVerification/SmhStreamVerification/SmhSecurityClassCCC/SmhSecurityClassCCCConfig`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Reference to the underlying StreamVerification to eecute the verification operation.

############ 2. SmhVendorVerificationConfig

- **UUID**: `aae4bd8b-20f5-4871-96c6-f240fa3f4dc4`
- **引用名**: `SmhVendorVerificationConfig`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `SmhSecurityClassVendorConfig`
- **完整路径**: `/MICROSAR/Smh/SmhVerification/SmhStreamVerification/SmhSecurityClassVendor/SmhSecurityClassVendorConfig`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Reference to a VendorVerification to execute next to the signature verification an additional vendor checksum.

######### 7. SmhSecurityClassVendor

**容器属性**:

- **UUID**: `023c1e00-aef3-45e5-8e62-e82c30453758`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SmhSecurityClassVendor`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container to configure the monolythic verification for security class Vendor.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. SmhDefaultSecurityClassVendorConfig

- **UUID**: `7fbeb646-9c86-4350-869c-617b0aeb7dc3`
- **引用名**: `SmhDefaultSecurityClassVendorConfig`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `SmhSecurityClassVendorConfig`
- **完整路径**: `/MICROSAR/Smh/SmhVerification/SmhMonolithicVerification/SmhSecurityClassVendor/SmhSecurityClassVendorConfig`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Default monolythic verification for the security class Vendor:
SecM_VerificationClassVendor

########## 配置容器

本模块包含 **1** 个配置容器：

########### 1. SmhSecurityClassVendorConfig

**容器属性**:

- **UUID**: `557f458f-7463-4adc-825b-7a4b4bea2cc4`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SmhSecurityClassVendorConfig`
- **多重性**: [1..infinite]
- **构建后可变**: false

**容器描述**:

Container to configure the monolythic verifications for security class Vendor.

############ 参数配置

此容器包含 **4** 个参数：

############# INTEGER 类型参数

############## 1. SmhSignatureOffset

- **UUID**: `7d727621-728d-44b0-a1df-a481f691ae4b`
- **参数名**: `SmhSignatureOffset`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Specify the offset to the signature.

############## 2. SmhCRCOffset

- **UUID**: `0a018b65-40c3-4884-ad4a-3db5d3bb1d87`
- **参数名**: `SmhCRCOffset`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Specify the offset to the CRC value (used by CRC written)

############# BOOLEAN 类型参数

############## 1. SmhIncludeAddressAndLengthInSignature

- **UUID**: `25259277-f94d-4f9a-8c3d-a537b7245aa9`
- **参数名**: `SmhIncludeAddressAndLengthInSignature`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Specify if the address and length of the segments shall be taken into account in the verification.

############# FUNCTION-NAME 类型参数

############## 1. SmhFunctionName

- **UUID**: `20e24252-7e8e-422d-add4-6ed7e3b75e4d`
- **参数名**: `SmhFunctionName`
- **数据类型**: FUNCTION-NAME
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Configure the function name to execute the monolythic verification.

############ 引用关系

此容器包含 **1** 个引用：

############# REFERENCE 类型引用

############## 1. SmhStreamVerificationConfig

- **UUID**: `94eb1fc3-a08c-416c-9b41-9409ca135742`
- **引用名**: `SmhStreamVerificationConfig`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `SmhSecurityClassVendorConfig`
- **完整路径**: `/MICROSAR/Smh/SmhVerification/SmhStreamVerification/SmhSecurityClassVendor/SmhSecurityClassVendorConfig`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Reference to the underlying StreamVerification to eecute the verification operation.

######### 8. SmhSecurityClassVendorConfig

**容器属性**:

- **UUID**: `557f458f-7463-4adc-825b-7a4b4bea2cc4`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SmhSecurityClassVendorConfig`
- **多重性**: [1..infinite]
- **构建后可变**: false

**容器描述**:

Container to configure the monolythic verifications for security class Vendor.

########## 参数配置

此容器包含 **4** 个参数：

########### INTEGER 类型参数

############ 1. SmhSignatureOffset

- **UUID**: `7d727621-728d-44b0-a1df-a481f691ae4b`
- **参数名**: `SmhSignatureOffset`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Specify the offset to the signature.

############ 2. SmhCRCOffset

- **UUID**: `0a018b65-40c3-4884-ad4a-3db5d3bb1d87`
- **参数名**: `SmhCRCOffset`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Specify the offset to the CRC value (used by CRC written)

########### BOOLEAN 类型参数

############ 1. SmhIncludeAddressAndLengthInSignature

- **UUID**: `25259277-f94d-4f9a-8c3d-a537b7245aa9`
- **参数名**: `SmhIncludeAddressAndLengthInSignature`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Specify if the address and length of the segments shall be taken into account in the verification.

########### FUNCTION-NAME 类型参数

############ 1. SmhFunctionName

- **UUID**: `20e24252-7e8e-422d-add4-6ed7e3b75e4d`
- **参数名**: `SmhFunctionName`
- **数据类型**: FUNCTION-NAME
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Configure the function name to execute the monolythic verification.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. SmhStreamVerificationConfig

- **UUID**: `94eb1fc3-a08c-416c-9b41-9409ca135742`
- **引用名**: `SmhStreamVerificationConfig`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `SmhSecurityClassVendorConfig`
- **完整路径**: `/MICROSAR/Smh/SmhVerification/SmhStreamVerification/SmhSecurityClassVendor/SmhSecurityClassVendorConfig`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Reference to the underlying StreamVerification to eecute the verification operation.

####### 2. SmhSecurityClassDDD

**容器属性**:

- **UUID**: `72791700-82db-4ae8-913d-546993a59628`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SmhSecurityClassDDD`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container to configure the monolythic verification for security class DDD.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. SmhDefaultSecurityClassDDDConfig

- **UUID**: `8000ac6e-db98-4d89-ad2e-e5d407d6e2cf`
- **引用名**: `SmhDefaultSecurityClassDDDConfig`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `SmhSecurityClassDDDConfig`
- **完整路径**: `/MICROSAR/Smh/SmhVerification/SmhMonolithicVerification/SmhSecurityClassDDD/SmhSecurityClassDDDConfig`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Default monolythic verification for the security class DDD:
SecM_VerificationClassDDD

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. SmhSecurityClassDDDConfig

**容器属性**:

- **UUID**: `8b918e7c-9888-4c0f-ab87-064e3f447ed8`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SmhSecurityClassDDDConfig`
- **多重性**: [1..infinite]
- **构建后可变**: false

**容器描述**:

Container to configure the monolythic verifications for security class DDD.

########## 参数配置

此容器包含 **4** 个参数：

########### INTEGER 类型参数

############ 1. SmhSignatureOffset

- **UUID**: `058834c9-af5f-4982-885e-fbfd6a591f78`
- **参数名**: `SmhSignatureOffset`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Specify the offset to the signature (CRC or hash value).

############ 2. SmhCRCOffset

- **UUID**: `f9ad26cf-04f7-460c-bb94-5033c8c860a6`
- **参数名**: `SmhCRCOffset`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Specify the offset to the CRC value (used by CRC written)

########### BOOLEAN 类型参数

############ 1. SmhIncludeAddressAndLengthInSignature

- **UUID**: `db44bc4a-9cca-473b-896d-be630b6785e9`
- **参数名**: `SmhIncludeAddressAndLengthInSignature`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Specify if the address and length of the segments shall be taken into account in the verification.

########### FUNCTION-NAME 类型参数

############ 1. SmhFunctionName

- **UUID**: `ab733ae7-604b-4644-98db-a29bf0b8b00b`
- **参数名**: `SmhFunctionName`
- **数据类型**: FUNCTION-NAME
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Configure the function name to execute the monolythic verification, e.g.:
- SecM_VerificationClassDDD_Crc32
- SecM_VerificationClassDDD_Sha512

########## 引用关系

此容器包含 **2** 个引用：

########### REFERENCE 类型引用

############ 1. SmhStreamVerificationConfig

- **UUID**: `06866c75-743e-46f3-98cd-693b08a484a1`
- **引用名**: `SmhStreamVerificationConfig`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `SmhSecurityClassDDDConfig`
- **完整路径**: `/MICROSAR/Smh/SmhVerification/SmhStreamVerification/SmhSecurityClassDDD/SmhSecurityClassDDDConfig`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Reference to the underlying StreamVerification to eecute the verification operation.

############ 2. SmhVendorVerificationConfig

- **UUID**: `22a7ef68-050b-43d2-9efa-64b75baf9e7b`
- **引用名**: `SmhVendorVerificationConfig`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `SmhSecurityClassVendorConfig`
- **完整路径**: `/MICROSAR/Smh/SmhVerification/SmhStreamVerification/SmhSecurityClassVendor/SmhSecurityClassVendorConfig`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Reference to a VendorVerification to execute next to the CRC/hash verification an additional vendor checksum.

####### 3. SmhSecurityClassDDDConfig

**容器属性**:

- **UUID**: `8b918e7c-9888-4c0f-ab87-064e3f447ed8`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SmhSecurityClassDDDConfig`
- **多重性**: [1..infinite]
- **构建后可变**: false

**容器描述**:

Container to configure the monolythic verifications for security class DDD.

######## 参数配置

此容器包含 **4** 个参数：

######### INTEGER 类型参数

########## 1. SmhSignatureOffset

- **UUID**: `058834c9-af5f-4982-885e-fbfd6a591f78`
- **参数名**: `SmhSignatureOffset`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Specify the offset to the signature (CRC or hash value).

########## 2. SmhCRCOffset

- **UUID**: `f9ad26cf-04f7-460c-bb94-5033c8c860a6`
- **参数名**: `SmhCRCOffset`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Specify the offset to the CRC value (used by CRC written)

######### BOOLEAN 类型参数

########## 1. SmhIncludeAddressAndLengthInSignature

- **UUID**: `db44bc4a-9cca-473b-896d-be630b6785e9`
- **参数名**: `SmhIncludeAddressAndLengthInSignature`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Specify if the address and length of the segments shall be taken into account in the verification.

######### FUNCTION-NAME 类型参数

########## 1. SmhFunctionName

- **UUID**: `ab733ae7-604b-4644-98db-a29bf0b8b00b`
- **参数名**: `SmhFunctionName`
- **数据类型**: FUNCTION-NAME
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Configure the function name to execute the monolythic verification, e.g.:
- SecM_VerificationClassDDD_Crc32
- SecM_VerificationClassDDD_Sha512

######## 引用关系

此容器包含 **2** 个引用：

######### REFERENCE 类型引用

########## 1. SmhStreamVerificationConfig

- **UUID**: `06866c75-743e-46f3-98cd-693b08a484a1`
- **引用名**: `SmhStreamVerificationConfig`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `SmhSecurityClassDDDConfig`
- **完整路径**: `/MICROSAR/Smh/SmhVerification/SmhStreamVerification/SmhSecurityClassDDD/SmhSecurityClassDDDConfig`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Reference to the underlying StreamVerification to eecute the verification operation.

########## 2. SmhVendorVerificationConfig

- **UUID**: `22a7ef68-050b-43d2-9efa-64b75baf9e7b`
- **引用名**: `SmhVendorVerificationConfig`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `SmhSecurityClassVendorConfig`
- **完整路径**: `/MICROSAR/Smh/SmhVerification/SmhStreamVerification/SmhSecurityClassVendor/SmhSecurityClassVendorConfig`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Reference to a VendorVerification to execute next to the CRC/hash verification an additional vendor checksum.

####### 4. SmhSecurityClassC

**容器属性**:

- **UUID**: `9184de9d-b87a-4814-9987-c262b26ccff8`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SmhSecurityClassC`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container to configure the monolythic verification for security class C.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. SmhDefaultSecurityClassCConfig

- **UUID**: `1bb8a08a-2a06-4fad-8757-e8b4999d7a9a`
- **引用名**: `SmhDefaultSecurityClassCConfig`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `SmhSecurityClassCConfig`
- **完整路径**: `/MICROSAR/Smh/SmhVerification/SmhMonolithicVerification/SmhSecurityClassC/SmhSecurityClassCConfig`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Default monolythic verification for the security class C:
SecM_VerificationClassC

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. SmhSecurityClassCConfig

**容器属性**:

- **UUID**: `08f7a3a0-55c3-4440-bbad-8652231c1afc`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SmhSecurityClassCConfig`
- **多重性**: [1..infinite]
- **构建后可变**: false

**容器描述**:

Container to configure the monolythic verifications for security class C.

########## 参数配置

此容器包含 **4** 个参数：

########### INTEGER 类型参数

############ 1. SmhSignatureOffset

- **UUID**: `2e0853f6-5158-49bb-8a43-0ee955c15bff`
- **参数名**: `SmhSignatureOffset`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Specify the offset to the signature (MAC).

############ 2. SmhCRCOffset

- **UUID**: `9d9b2b54-743d-4914-a914-a375452a81c9`
- **参数名**: `SmhCRCOffset`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Specify the offset to the CRC value (used by CRC written)

########### BOOLEAN 类型参数

############ 1. SmhIncludeAddressAndLengthInSignature

- **UUID**: `e26fa671-08c7-466b-a1a7-de82db5c676c`
- **参数名**: `SmhIncludeAddressAndLengthInSignature`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Specify if the address and length of the segments shall be taken into account in the verification.

########### FUNCTION-NAME 类型参数

############ 1. SmhFunctionName

- **UUID**: `9bd34e8a-f73d-4e0a-9dc9-203ffa5b98ca`
- **参数名**: `SmhFunctionName`
- **数据类型**: FUNCTION-NAME
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Configure the function name to execute the monolythic verification, e.g.:
- SecM_VerificationClassC_HmacSha1
- SecM_VerificationClassC_Cmac

########## 引用关系

此容器包含 **2** 个引用：

########### REFERENCE 类型引用

############ 1. SmhStreamVerificationConfig

- **UUID**: `f7ef63f9-fff4-4b04-a90e-3cbdd667497e`
- **引用名**: `SmhStreamVerificationConfig`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `SmhSecurityClassCConfig`
- **完整路径**: `/MICROSAR/Smh/SmhVerification/SmhStreamVerification/SmhSecurityClassC/SmhSecurityClassCConfig`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Reference to the underlying StreamVerification to eecute the verification operation.

############ 2. SmhVendorVerificationConfig

- **UUID**: `901c9188-01b4-4c53-ac2d-0d0fb0a5359e`
- **引用名**: `SmhVendorVerificationConfig`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `SmhSecurityClassVendorConfig`
- **完整路径**: `/MICROSAR/Smh/SmhVerification/SmhStreamVerification/SmhSecurityClassVendor/SmhSecurityClassVendorConfig`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Reference to a VendorVerification to execute next to the MAC verification an additional vendor checksum.

####### 5. SmhSecurityClassCConfig

**容器属性**:

- **UUID**: `08f7a3a0-55c3-4440-bbad-8652231c1afc`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SmhSecurityClassCConfig`
- **多重性**: [1..infinite]
- **构建后可变**: false

**容器描述**:

Container to configure the monolythic verifications for security class C.

######## 参数配置

此容器包含 **4** 个参数：

######### INTEGER 类型参数

########## 1. SmhSignatureOffset

- **UUID**: `2e0853f6-5158-49bb-8a43-0ee955c15bff`
- **参数名**: `SmhSignatureOffset`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Specify the offset to the signature (MAC).

########## 2. SmhCRCOffset

- **UUID**: `9d9b2b54-743d-4914-a914-a375452a81c9`
- **参数名**: `SmhCRCOffset`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Specify the offset to the CRC value (used by CRC written)

######### BOOLEAN 类型参数

########## 1. SmhIncludeAddressAndLengthInSignature

- **UUID**: `e26fa671-08c7-466b-a1a7-de82db5c676c`
- **参数名**: `SmhIncludeAddressAndLengthInSignature`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Specify if the address and length of the segments shall be taken into account in the verification.

######### FUNCTION-NAME 类型参数

########## 1. SmhFunctionName

- **UUID**: `9bd34e8a-f73d-4e0a-9dc9-203ffa5b98ca`
- **参数名**: `SmhFunctionName`
- **数据类型**: FUNCTION-NAME
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Configure the function name to execute the monolythic verification, e.g.:
- SecM_VerificationClassC_HmacSha1
- SecM_VerificationClassC_Cmac

######## 引用关系

此容器包含 **2** 个引用：

######### REFERENCE 类型引用

########## 1. SmhStreamVerificationConfig

- **UUID**: `f7ef63f9-fff4-4b04-a90e-3cbdd667497e`
- **引用名**: `SmhStreamVerificationConfig`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `SmhSecurityClassCConfig`
- **完整路径**: `/MICROSAR/Smh/SmhVerification/SmhStreamVerification/SmhSecurityClassC/SmhSecurityClassCConfig`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Reference to the underlying StreamVerification to eecute the verification operation.

########## 2. SmhVendorVerificationConfig

- **UUID**: `901c9188-01b4-4c53-ac2d-0d0fb0a5359e`
- **引用名**: `SmhVendorVerificationConfig`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `SmhSecurityClassVendorConfig`
- **完整路径**: `/MICROSAR/Smh/SmhVerification/SmhStreamVerification/SmhSecurityClassVendor/SmhSecurityClassVendorConfig`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Reference to a VendorVerification to execute next to the MAC verification an additional vendor checksum.

####### 6. SmhSecurityClassCCC

**容器属性**:

- **UUID**: `4ab7b0b3-e998-4914-bdd3-8ba54bf23f77`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SmhSecurityClassCCC`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container to configure the monolythic verification for security class CCC.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. SmhDefaultSecurityClassCCCConfig

- **UUID**: `9da32213-c156-452a-82af-9db07b263858`
- **引用名**: `SmhDefaultSecurityClassCCCConfig`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `SmhSecurityClassCCCConfig`
- **完整路径**: `/MICROSAR/Smh/SmhVerification/SmhMonolithicVerification/SmhSecurityClassCCC/SmhSecurityClassCCCConfig`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Default monolythic verification for the security class CCC:
SecM_VerificationClassCCC

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. SmhSecurityClassCCCConfig

**容器属性**:

- **UUID**: `bb62362a-8553-4d60-a926-a0270adeb73f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SmhSecurityClassCCCConfig`
- **多重性**: [1..infinite]
- **构建后可变**: false

**容器描述**:

Container to configure the monolythic verifications for security class CCC.

########## 参数配置

此容器包含 **4** 个参数：

########### INTEGER 类型参数

############ 1. SmhSignatureOffset

- **UUID**: `8cb8417a-f4e7-4fd7-b389-73e568cbd189`
- **参数名**: `SmhSignatureOffset`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Specify the offset to the signature.

############ 2. SmhCRCOffset

- **UUID**: `00c2cec6-726b-4e53-b151-e8685d67c400`
- **参数名**: `SmhCRCOffset`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Specify the offset to the CRC value (used by CRC written)

########### BOOLEAN 类型参数

############ 1. SmhIncludeAddressAndLengthInSignature

- **UUID**: `97a43d7c-7ece-4506-946e-751f23cee541`
- **参数名**: `SmhIncludeAddressAndLengthInSignature`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Specify if the address and length of the segments shall be taken into account in the verification.

########### FUNCTION-NAME 类型参数

############ 1. SmhFunctionName

- **UUID**: `442fdcd9-13f7-4614-98c5-950f0ed8cee1`
- **参数名**: `SmhFunctionName`
- **数据类型**: FUNCTION-NAME
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Configure the function name to execute the monolythic verification, e.g.:
- SecM_VerificationClassCCC_RsaPssSha256
- SecM_VerificationClassCCC_Ed25519PH

########## 引用关系

此容器包含 **2** 个引用：

########### REFERENCE 类型引用

############ 1. SmhStreamVerificationConfig

- **UUID**: `d59861ca-8eba-456e-b4cf-b28f96b0d983`
- **引用名**: `SmhStreamVerificationConfig`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `SmhSecurityClassCCCConfig`
- **完整路径**: `/MICROSAR/Smh/SmhVerification/SmhStreamVerification/SmhSecurityClassCCC/SmhSecurityClassCCCConfig`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Reference to the underlying StreamVerification to eecute the verification operation.

############ 2. SmhVendorVerificationConfig

- **UUID**: `aae4bd8b-20f5-4871-96c6-f240fa3f4dc4`
- **引用名**: `SmhVendorVerificationConfig`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `SmhSecurityClassVendorConfig`
- **完整路径**: `/MICROSAR/Smh/SmhVerification/SmhStreamVerification/SmhSecurityClassVendor/SmhSecurityClassVendorConfig`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Reference to a VendorVerification to execute next to the signature verification an additional vendor checksum.

####### 7. SmhSecurityClassCCCConfig

**容器属性**:

- **UUID**: `bb62362a-8553-4d60-a926-a0270adeb73f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SmhSecurityClassCCCConfig`
- **多重性**: [1..infinite]
- **构建后可变**: false

**容器描述**:

Container to configure the monolythic verifications for security class CCC.

######## 参数配置

此容器包含 **4** 个参数：

######### INTEGER 类型参数

########## 1. SmhSignatureOffset

- **UUID**: `8cb8417a-f4e7-4fd7-b389-73e568cbd189`
- **参数名**: `SmhSignatureOffset`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Specify the offset to the signature.

########## 2. SmhCRCOffset

- **UUID**: `00c2cec6-726b-4e53-b151-e8685d67c400`
- **参数名**: `SmhCRCOffset`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Specify the offset to the CRC value (used by CRC written)

######### BOOLEAN 类型参数

########## 1. SmhIncludeAddressAndLengthInSignature

- **UUID**: `97a43d7c-7ece-4506-946e-751f23cee541`
- **参数名**: `SmhIncludeAddressAndLengthInSignature`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Specify if the address and length of the segments shall be taken into account in the verification.

######### FUNCTION-NAME 类型参数

########## 1. SmhFunctionName

- **UUID**: `442fdcd9-13f7-4614-98c5-950f0ed8cee1`
- **参数名**: `SmhFunctionName`
- **数据类型**: FUNCTION-NAME
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Configure the function name to execute the monolythic verification, e.g.:
- SecM_VerificationClassCCC_RsaPssSha256
- SecM_VerificationClassCCC_Ed25519PH

######## 引用关系

此容器包含 **2** 个引用：

######### REFERENCE 类型引用

########## 1. SmhStreamVerificationConfig

- **UUID**: `d59861ca-8eba-456e-b4cf-b28f96b0d983`
- **引用名**: `SmhStreamVerificationConfig`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `SmhSecurityClassCCCConfig`
- **完整路径**: `/MICROSAR/Smh/SmhVerification/SmhStreamVerification/SmhSecurityClassCCC/SmhSecurityClassCCCConfig`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Reference to the underlying StreamVerification to eecute the verification operation.

########## 2. SmhVendorVerificationConfig

- **UUID**: `aae4bd8b-20f5-4871-96c6-f240fa3f4dc4`
- **引用名**: `SmhVendorVerificationConfig`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `SmhSecurityClassVendorConfig`
- **完整路径**: `/MICROSAR/Smh/SmhVerification/SmhStreamVerification/SmhSecurityClassVendor/SmhSecurityClassVendorConfig`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Reference to a VendorVerification to execute next to the signature verification an additional vendor checksum.

####### 8. SmhSecurityClassVendor

**容器属性**:

- **UUID**: `023c1e00-aef3-45e5-8e62-e82c30453758`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SmhSecurityClassVendor`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container to configure the monolythic verification for security class Vendor.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. SmhDefaultSecurityClassVendorConfig

- **UUID**: `7fbeb646-9c86-4350-869c-617b0aeb7dc3`
- **引用名**: `SmhDefaultSecurityClassVendorConfig`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `SmhSecurityClassVendorConfig`
- **完整路径**: `/MICROSAR/Smh/SmhVerification/SmhMonolithicVerification/SmhSecurityClassVendor/SmhSecurityClassVendorConfig`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Default monolythic verification for the security class Vendor:
SecM_VerificationClassVendor

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. SmhSecurityClassVendorConfig

**容器属性**:

- **UUID**: `557f458f-7463-4adc-825b-7a4b4bea2cc4`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SmhSecurityClassVendorConfig`
- **多重性**: [1..infinite]
- **构建后可变**: false

**容器描述**:

Container to configure the monolythic verifications for security class Vendor.

########## 参数配置

此容器包含 **4** 个参数：

########### INTEGER 类型参数

############ 1. SmhSignatureOffset

- **UUID**: `7d727621-728d-44b0-a1df-a481f691ae4b`
- **参数名**: `SmhSignatureOffset`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Specify the offset to the signature.

############ 2. SmhCRCOffset

- **UUID**: `0a018b65-40c3-4884-ad4a-3db5d3bb1d87`
- **参数名**: `SmhCRCOffset`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Specify the offset to the CRC value (used by CRC written)

########### BOOLEAN 类型参数

############ 1. SmhIncludeAddressAndLengthInSignature

- **UUID**: `25259277-f94d-4f9a-8c3d-a537b7245aa9`
- **参数名**: `SmhIncludeAddressAndLengthInSignature`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Specify if the address and length of the segments shall be taken into account in the verification.

########### FUNCTION-NAME 类型参数

############ 1. SmhFunctionName

- **UUID**: `20e24252-7e8e-422d-add4-6ed7e3b75e4d`
- **参数名**: `SmhFunctionName`
- **数据类型**: FUNCTION-NAME
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Configure the function name to execute the monolythic verification.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. SmhStreamVerificationConfig

- **UUID**: `94eb1fc3-a08c-416c-9b41-9409ca135742`
- **引用名**: `SmhStreamVerificationConfig`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `SmhSecurityClassVendorConfig`
- **完整路径**: `/MICROSAR/Smh/SmhVerification/SmhStreamVerification/SmhSecurityClassVendor/SmhSecurityClassVendorConfig`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Reference to the underlying StreamVerification to eecute the verification operation.

####### 9. SmhSecurityClassVendorConfig

**容器属性**:

- **UUID**: `557f458f-7463-4adc-825b-7a4b4bea2cc4`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SmhSecurityClassVendorConfig`
- **多重性**: [1..infinite]
- **构建后可变**: false

**容器描述**:

Container to configure the monolythic verifications for security class Vendor.

######## 参数配置

此容器包含 **4** 个参数：

######### INTEGER 类型参数

########## 1. SmhSignatureOffset

- **UUID**: `7d727621-728d-44b0-a1df-a481f691ae4b`
- **参数名**: `SmhSignatureOffset`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Specify the offset to the signature.

########## 2. SmhCRCOffset

- **UUID**: `0a018b65-40c3-4884-ad4a-3db5d3bb1d87`
- **参数名**: `SmhCRCOffset`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Specify the offset to the CRC value (used by CRC written)

######### BOOLEAN 类型参数

########## 1. SmhIncludeAddressAndLengthInSignature

- **UUID**: `25259277-f94d-4f9a-8c3d-a537b7245aa9`
- **参数名**: `SmhIncludeAddressAndLengthInSignature`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Specify if the address and length of the segments shall be taken into account in the verification.

######### FUNCTION-NAME 类型参数

########## 1. SmhFunctionName

- **UUID**: `20e24252-7e8e-422d-add4-6ed7e3b75e4d`
- **参数名**: `SmhFunctionName`
- **数据类型**: FUNCTION-NAME
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Configure the function name to execute the monolythic verification.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. SmhStreamVerificationConfig

- **UUID**: `94eb1fc3-a08c-416c-9b41-9409ca135742`
- **引用名**: `SmhStreamVerificationConfig`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `SmhSecurityClassVendorConfig`
- **完整路径**: `/MICROSAR/Smh/SmhVerification/SmhStreamVerification/SmhSecurityClassVendor/SmhSecurityClassVendorConfig`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Reference to the underlying StreamVerification to eecute the verification operation.

####### 10. SmhStreamVerification

**容器属性**:

- **UUID**: `3c39b3ca-3331-4d94-b73e-40528c7afacc`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SmhStreamVerification`
- **多重性**: [1..1]
- **构建后可变**: false

**容器描述**:

Container to configure the stream verifications.
Stream verifications are used to verify the data during the download (InputVerification, ProcessedVerification and PipelinedVerification).

######## 引用关系

此容器包含 **1** 个引用：

######### CHOICE-REFERENCE 类型引用

########## 1. SmhDefaultStreamVerificationConfig

- **UUID**: `c2da39ea-e323-4668-ab9f-6acfa5c53ef3`
- **引用名**: `SmhDefaultStreamVerificationConfig`
- **引用类型**: CHOICE-REFERENCE
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **需要索引**: false
- **目标引用列表**:
  - `/MICROSAR/Smh/SmhVerification/SmhStreamVerification/SmhSecurityClassDDD/SmhSecurityClassDDDConfig`
  - `/MICROSAR/Smh/SmhVerification/SmhStreamVerification/SmhSecurityClassC/SmhSecurityClassCConfig`
  - `/MICROSAR/Smh/SmhVerification/SmhStreamVerification/SmhSecurityClassCCC/SmhSecurityClassCCCConfig`
  - `/MICROSAR/Smh/SmhVerification/SmhStreamVerification/SmhSecurityClassVendor/SmhSecurityClassVendorConfig`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Default stream verification:
SecM_VerifySignature

######## 配置容器

本模块包含 **12** 个配置容器：

######### 1. SmhSecurityClassDDD

**容器属性**:

- **UUID**: `f65076e1-6a4f-4afd-8f21-e8faea37fe6d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SmhSecurityClassDDD`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container to configure the stream verification for security class DDD.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. SmhDefaultSecurityClassDDDConfig

- **UUID**: `46906c73-00d0-4ce1-83bd-dd5f4112a3d8`
- **引用名**: `SmhDefaultSecurityClassDDDConfig`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `SmhSecurityClassDDDConfig`
- **完整路径**: `/MICROSAR/Smh/SmhVerification/SmhStreamVerification/SmhSecurityClassDDD/SmhSecurityClassDDDConfig`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Default stream verification for the security class DDD:
SecM_VerifyClassDDD

########## 配置容器

本模块包含 **4** 个配置容器：

########### 1. SmhSecurityClassDDDConfig

**容器属性**:

- **UUID**: `9edb72f4-2681-4d78-b583-25881036d326`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SmhSecurityClassDDDConfig`
- **多重性**: [1..infinite]
- **构建后可变**: false

**容器描述**:

Container to configure the stream verifications for security class DDD.

############ 参数配置

此容器包含 **3** 个参数：

############# BOOLEAN 类型参数

############## 1. SmhUpdateLengthOfHashedData

- **UUID**: `d4134277-9064-464b-a0e2-444e36fc56bc`
- **参数名**: `SmhUpdateLengthOfHashedData`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: If enabled, the security module will update the current length of hashed data in SecM_SignatureParamtype::currentDataLength.

############## 2. SmhComputationOnly

- **UUID**: `a77c5004-72b2-4e59-aee2-025769278b81`
- **参数名**: `SmhComputationOnly`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: If enabled the security module will just compute the CRC/hash without verifying it. The computed CRC/hash is provided via SecM_SignatureParamtype::sigSourceBuffer.

############# FUNCTION-NAME 类型参数

############## 1. SmhFunctionName

- **UUID**: `262ace43-2c7c-4462-9763-63cfd27ebe48`
- **参数名**: `SmhFunctionName`
- **数据类型**: FUNCTION-NAME
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Configure the function name of the stream verification, e.g.:
- SecM_VerifyCrc32
- SecM_VerifyHashSha512

############ 配置容器

本模块包含 **3** 个配置容器：

############# 1. SmhCrc

**容器属性**:

- **UUID**: `d77a32e4-ca21-4c5c-a0ec-75a6fae134fe`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SmhCrc`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container to configure the CRC

############## 引用关系

此容器包含 **1** 个引用：

############### CHOICE-REFERENCE 类型引用

################ 1. SmhCrcRef

- **UUID**: `545924b6-97cc-4283-9bee-5159bda168f9`
- **引用名**: `SmhCrcRef`
- **引用类型**: CHOICE-REFERENCE
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **需要索引**: false
- **目标引用列表**:
  - `/MICROSAR/Smh/SmhCrc/SmhCrc16`
  - `/MICROSAR/Smh/SmhCrc/SmhCrc32`
  - `/MICROSAR/Smh/SmhCrc/SmhCrc64`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: References a CRC configuration, which shall be used by this stream verification.

############# 2. SmhHash

**容器属性**:

- **UUID**: `860c29ac-feed-4843-be72-6b659b349d99`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SmhHash`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container to configure the hash

############## 引用关系

此容器包含 **1** 个引用：

############### REFERENCE 类型引用

################ 1. SmhJobRef

- **UUID**: `935a56dc-ff73-4f9e-9090-032d0f6d04cb`
- **引用名**: `SmhJobRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `SmhJob`
- **完整路径**: `/MICROSAR/Smh/SmhJob`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: References a SmhHash job, which shall be used by this stream verification.

############# 3. SmhSecurityClassDDDType

**容器属性**:

- **UUID**: `d4091ae3-bc5f-49ed-aab5-4f51d555f432`
- **容器类型**: CHOICE-CONTAINER
- **容器名称**: `SmhSecurityClassDDDType`
- **多重性**: [1..1]
- **构建后可变**: false

**容器选择**:

- **SmhCrc**
  - UUID: `d77a32e4-ca21-4c5c-a0ec-75a6fae134fe`
  - 描述: Container to configure the CRC
- **SmhHash**
  - UUID: `860c29ac-feed-4843-be72-6b659b349d99`
  - 描述: Container to configure the hash

**容器描述**:

Specify the type of the security class DDD

########### 2. SmhCrc

**容器属性**:

- **UUID**: `d77a32e4-ca21-4c5c-a0ec-75a6fae134fe`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SmhCrc`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container to configure the CRC

############ 引用关系

此容器包含 **1** 个引用：

############# CHOICE-REFERENCE 类型引用

############## 1. SmhCrcRef

- **UUID**: `545924b6-97cc-4283-9bee-5159bda168f9`
- **引用名**: `SmhCrcRef`
- **引用类型**: CHOICE-REFERENCE
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **需要索引**: false
- **目标引用列表**:
  - `/MICROSAR/Smh/SmhCrc/SmhCrc16`
  - `/MICROSAR/Smh/SmhCrc/SmhCrc32`
  - `/MICROSAR/Smh/SmhCrc/SmhCrc64`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: References a CRC configuration, which shall be used by this stream verification.

########### 3. SmhHash

**容器属性**:

- **UUID**: `860c29ac-feed-4843-be72-6b659b349d99`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SmhHash`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container to configure the hash

############ 引用关系

此容器包含 **1** 个引用：

############# REFERENCE 类型引用

############## 1. SmhJobRef

- **UUID**: `935a56dc-ff73-4f9e-9090-032d0f6d04cb`
- **引用名**: `SmhJobRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `SmhJob`
- **完整路径**: `/MICROSAR/Smh/SmhJob`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: References a SmhHash job, which shall be used by this stream verification.

########### 4. SmhSecurityClassDDDType

**容器属性**:

- **UUID**: `d4091ae3-bc5f-49ed-aab5-4f51d555f432`
- **容器类型**: CHOICE-CONTAINER
- **容器名称**: `SmhSecurityClassDDDType`
- **多重性**: [1..1]
- **构建后可变**: false

**容器选择**:

- **SmhCrc**
  - UUID: `d77a32e4-ca21-4c5c-a0ec-75a6fae134fe`
  - 描述: Container to configure the CRC
- **SmhHash**
  - UUID: `860c29ac-feed-4843-be72-6b659b349d99`
  - 描述: Container to configure the hash

**容器描述**:

Specify the type of the security class DDD

######### 2. SmhSecurityClassDDDConfig

**容器属性**:

- **UUID**: `9edb72f4-2681-4d78-b583-25881036d326`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SmhSecurityClassDDDConfig`
- **多重性**: [1..infinite]
- **构建后可变**: false

**容器描述**:

Container to configure the stream verifications for security class DDD.

########## 参数配置

此容器包含 **3** 个参数：

########### BOOLEAN 类型参数

############ 1. SmhUpdateLengthOfHashedData

- **UUID**: `d4134277-9064-464b-a0e2-444e36fc56bc`
- **参数名**: `SmhUpdateLengthOfHashedData`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: If enabled, the security module will update the current length of hashed data in SecM_SignatureParamtype::currentDataLength.

############ 2. SmhComputationOnly

- **UUID**: `a77c5004-72b2-4e59-aee2-025769278b81`
- **参数名**: `SmhComputationOnly`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: If enabled the security module will just compute the CRC/hash without verifying it. The computed CRC/hash is provided via SecM_SignatureParamtype::sigSourceBuffer.

########### FUNCTION-NAME 类型参数

############ 1. SmhFunctionName

- **UUID**: `262ace43-2c7c-4462-9763-63cfd27ebe48`
- **参数名**: `SmhFunctionName`
- **数据类型**: FUNCTION-NAME
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Configure the function name of the stream verification, e.g.:
- SecM_VerifyCrc32
- SecM_VerifyHashSha512

########## 配置容器

本模块包含 **3** 个配置容器：

########### 1. SmhCrc

**容器属性**:

- **UUID**: `d77a32e4-ca21-4c5c-a0ec-75a6fae134fe`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SmhCrc`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container to configure the CRC

############ 引用关系

此容器包含 **1** 个引用：

############# CHOICE-REFERENCE 类型引用

############## 1. SmhCrcRef

- **UUID**: `545924b6-97cc-4283-9bee-5159bda168f9`
- **引用名**: `SmhCrcRef`
- **引用类型**: CHOICE-REFERENCE
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **需要索引**: false
- **目标引用列表**:
  - `/MICROSAR/Smh/SmhCrc/SmhCrc16`
  - `/MICROSAR/Smh/SmhCrc/SmhCrc32`
  - `/MICROSAR/Smh/SmhCrc/SmhCrc64`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: References a CRC configuration, which shall be used by this stream verification.

########### 2. SmhHash

**容器属性**:

- **UUID**: `860c29ac-feed-4843-be72-6b659b349d99`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SmhHash`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container to configure the hash

############ 引用关系

此容器包含 **1** 个引用：

############# REFERENCE 类型引用

############## 1. SmhJobRef

- **UUID**: `935a56dc-ff73-4f9e-9090-032d0f6d04cb`
- **引用名**: `SmhJobRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `SmhJob`
- **完整路径**: `/MICROSAR/Smh/SmhJob`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: References a SmhHash job, which shall be used by this stream verification.

########### 3. SmhSecurityClassDDDType

**容器属性**:

- **UUID**: `d4091ae3-bc5f-49ed-aab5-4f51d555f432`
- **容器类型**: CHOICE-CONTAINER
- **容器名称**: `SmhSecurityClassDDDType`
- **多重性**: [1..1]
- **构建后可变**: false

**容器选择**:

- **SmhCrc**
  - UUID: `d77a32e4-ca21-4c5c-a0ec-75a6fae134fe`
  - 描述: Container to configure the CRC
- **SmhHash**
  - UUID: `860c29ac-feed-4843-be72-6b659b349d99`
  - 描述: Container to configure the hash

**容器描述**:

Specify the type of the security class DDD

######### 3. SmhCrc

**容器属性**:

- **UUID**: `d77a32e4-ca21-4c5c-a0ec-75a6fae134fe`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SmhCrc`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container to configure the CRC

########## 引用关系

此容器包含 **1** 个引用：

########### CHOICE-REFERENCE 类型引用

############ 1. SmhCrcRef

- **UUID**: `545924b6-97cc-4283-9bee-5159bda168f9`
- **引用名**: `SmhCrcRef`
- **引用类型**: CHOICE-REFERENCE
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **需要索引**: false
- **目标引用列表**:
  - `/MICROSAR/Smh/SmhCrc/SmhCrc16`
  - `/MICROSAR/Smh/SmhCrc/SmhCrc32`
  - `/MICROSAR/Smh/SmhCrc/SmhCrc64`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: References a CRC configuration, which shall be used by this stream verification.

######### 4. SmhHash

**容器属性**:

- **UUID**: `860c29ac-feed-4843-be72-6b659b349d99`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SmhHash`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container to configure the hash

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. SmhJobRef

- **UUID**: `935a56dc-ff73-4f9e-9090-032d0f6d04cb`
- **引用名**: `SmhJobRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `SmhJob`
- **完整路径**: `/MICROSAR/Smh/SmhJob`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: References a SmhHash job, which shall be used by this stream verification.

######### 5. SmhSecurityClassC

**容器属性**:

- **UUID**: `0bbafb93-8d89-4aa2-a917-76ff0cc0016a`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SmhSecurityClassC`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container to configure the stream verification for security class C.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. SmhDefaultSecurityClassCConfig

- **UUID**: `29bb2998-5a48-4047-9169-d03556cff09d`
- **引用名**: `SmhDefaultSecurityClassCConfig`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `SmhSecurityClassCConfig`
- **完整路径**: `/MICROSAR/Smh/SmhVerification/SmhStreamVerification/SmhSecurityClassC/SmhSecurityClassCConfig`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Default stream verification for the security class C:
SecM_VerifyClassC

########## 配置容器

本模块包含 **1** 个配置容器：

########### 1. SmhSecurityClassCConfig

**容器属性**:

- **UUID**: `db313d05-7ad6-453b-bc32-372ecc4c5ec4`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SmhSecurityClassCConfig`
- **多重性**: [1..infinite]
- **构建后可变**: false

**容器描述**:

Container to configure the stream verifications for security class C.

############ 参数配置

此容器包含 **3** 个参数：

############# BOOLEAN 类型参数

############## 1. SmhUpdateLengthOfHashedData

- **UUID**: `1e161cb2-0f71-4990-8d7a-84f8f1fbf05c`
- **参数名**: `SmhUpdateLengthOfHashedData`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: If enabled, the security module will update the current length of hashed data in SecM_SignatureParamtype::currentDataLength.

############## 2. SmhComputationOnly

- **UUID**: `ca7644f1-ecc0-46b1-b73f-f926b42df198`
- **参数名**: `SmhComputationOnly`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: If enabled the security module will just compute the MAC without verifying it. The computed MAC is provided via SecM_SignatureParamtype::sigSourceBuffer.

############# FUNCTION-NAME 类型参数

############## 1. SmhFunctionName

- **UUID**: `c9a732c4-3d9b-4838-a3ed-c21f7878e3c5`
- **参数名**: `SmhFunctionName`
- **数据类型**: FUNCTION-NAME
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Configure the function name of the stream verification, e.g.:
- SecM_VerifyMacHmacSha1
- SecM_VerifyMacCmac

############ 引用关系

此容器包含 **1** 个引用：

############# REFERENCE 类型引用

############## 1. SmhJobRef

- **UUID**: `4443273c-b72e-4faa-ae72-41ee1d2fe23c`
- **引用名**: `SmhJobRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `SmhJob`
- **完整路径**: `/MICROSAR/Smh/SmhJob`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: References a SmhMacVerify or SmhMacGenerate job, which shall be used by this stream verification.

######### 6. SmhSecurityClassCConfig

**容器属性**:

- **UUID**: `db313d05-7ad6-453b-bc32-372ecc4c5ec4`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SmhSecurityClassCConfig`
- **多重性**: [1..infinite]
- **构建后可变**: false

**容器描述**:

Container to configure the stream verifications for security class C.

########## 参数配置

此容器包含 **3** 个参数：

########### BOOLEAN 类型参数

############ 1. SmhUpdateLengthOfHashedData

- **UUID**: `1e161cb2-0f71-4990-8d7a-84f8f1fbf05c`
- **参数名**: `SmhUpdateLengthOfHashedData`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: If enabled, the security module will update the current length of hashed data in SecM_SignatureParamtype::currentDataLength.

############ 2. SmhComputationOnly

- **UUID**: `ca7644f1-ecc0-46b1-b73f-f926b42df198`
- **参数名**: `SmhComputationOnly`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: If enabled the security module will just compute the MAC without verifying it. The computed MAC is provided via SecM_SignatureParamtype::sigSourceBuffer.

########### FUNCTION-NAME 类型参数

############ 1. SmhFunctionName

- **UUID**: `c9a732c4-3d9b-4838-a3ed-c21f7878e3c5`
- **参数名**: `SmhFunctionName`
- **数据类型**: FUNCTION-NAME
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Configure the function name of the stream verification, e.g.:
- SecM_VerifyMacHmacSha1
- SecM_VerifyMacCmac

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. SmhJobRef

- **UUID**: `4443273c-b72e-4faa-ae72-41ee1d2fe23c`
- **引用名**: `SmhJobRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `SmhJob`
- **完整路径**: `/MICROSAR/Smh/SmhJob`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: References a SmhMacVerify or SmhMacGenerate job, which shall be used by this stream verification.

######### 7. SmhSecurityClassCCC

**容器属性**:

- **UUID**: `e8bb9b83-5292-4b97-9d4e-6f37ada0a6c1`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SmhSecurityClassCCC`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container to configure the stream verification for security class CCC.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. SmhDefaultSecurityClassCCCConfig

- **UUID**: `0442501f-54c8-4df8-a5a1-c1a5f7de1398`
- **引用名**: `SmhDefaultSecurityClassCCCConfig`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `SmhSecurityClassCCCConfig`
- **完整路径**: `/MICROSAR/Smh/SmhVerification/SmhStreamVerification/SmhSecurityClassCCC/SmhSecurityClassCCCConfig`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Default stream verification for the security class CCC:
SecM_VerifyClassCCC

########## 配置容器

本模块包含 **2** 个配置容器：

########### 1. SmhSecurityClassCCCConfig

**容器属性**:

- **UUID**: `664dcb07-95ff-4179-8d6e-6ef8f5b49b46`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SmhSecurityClassCCCConfig`
- **多重性**: [1..infinite]
- **构建后可变**: false

**容器描述**:

Container to configure the stream verifications for security class CCC.

############ 参数配置

此容器包含 **2** 个参数：

############# BOOLEAN 类型参数

############## 1. SmhUpdateLengthOfHashedData

- **UUID**: `eec6e339-e8e3-44fa-b123-4e6a0eb5f1f0`
- **参数名**: `SmhUpdateLengthOfHashedData`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: If enabled, the security module will update the current length of hashed data in SecM_SignatureParamtype::currentDataLength.

############# FUNCTION-NAME 类型参数

############## 1. SmhFunctionName

- **UUID**: `2ea862e4-436b-42bd-9762-5fcc32430434`
- **参数名**: `SmhFunctionName`
- **数据类型**: FUNCTION-NAME
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Configure the function name of the stream verification, e.g.:
- SecM_VerifySigRsaPssSha256
- SecM_VerifySigEd25519PH

############ 引用关系

此容器包含 **1** 个引用：

############# REFERENCE 类型引用

############## 1. SmhJobRef

- **UUID**: `d60da727-ed84-438f-b298-500fde867ab8`
- **引用名**: `SmhJobRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `SmhJob`
- **完整路径**: `/MICROSAR/Smh/SmhJob`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: References a SmhSignatureVerify job, which shall be used by this stream verification.

############ 配置容器

本模块包含 **1** 个配置容器：

############# 1. SmhDiscretHashConfig

**容器属性**:

- **UUID**: `4e51524b-a403-48b3-9ada-c1942ae9616f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SmhDiscretHashConfig`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Configure a discrete hash for the verification, which is used to calculate a hash before verifying the signature.

############## 引用关系

此容器包含 **1** 个引用：

############### REFERENCE 类型引用

################ 1. SmhJobRef

- **UUID**: `51d9a895-6b6e-4e9f-88f1-5310319d40d3`
- **引用名**: `SmhJobRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `SmhJob`
- **完整路径**: `/MICROSAR/Smh/SmhJob`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: References a SmhHash job, which shall be used for the discrete hash.

########### 2. SmhDiscretHashConfig

**容器属性**:

- **UUID**: `4e51524b-a403-48b3-9ada-c1942ae9616f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SmhDiscretHashConfig`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Configure a discrete hash for the verification, which is used to calculate a hash before verifying the signature.

############ 引用关系

此容器包含 **1** 个引用：

############# REFERENCE 类型引用

############## 1. SmhJobRef

- **UUID**: `51d9a895-6b6e-4e9f-88f1-5310319d40d3`
- **引用名**: `SmhJobRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `SmhJob`
- **完整路径**: `/MICROSAR/Smh/SmhJob`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: References a SmhHash job, which shall be used for the discrete hash.

######### 8. SmhSecurityClassCCCConfig

**容器属性**:

- **UUID**: `664dcb07-95ff-4179-8d6e-6ef8f5b49b46`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SmhSecurityClassCCCConfig`
- **多重性**: [1..infinite]
- **构建后可变**: false

**容器描述**:

Container to configure the stream verifications for security class CCC.

########## 参数配置

此容器包含 **2** 个参数：

########### BOOLEAN 类型参数

############ 1. SmhUpdateLengthOfHashedData

- **UUID**: `eec6e339-e8e3-44fa-b123-4e6a0eb5f1f0`
- **参数名**: `SmhUpdateLengthOfHashedData`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: If enabled, the security module will update the current length of hashed data in SecM_SignatureParamtype::currentDataLength.

########### FUNCTION-NAME 类型参数

############ 1. SmhFunctionName

- **UUID**: `2ea862e4-436b-42bd-9762-5fcc32430434`
- **参数名**: `SmhFunctionName`
- **数据类型**: FUNCTION-NAME
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Configure the function name of the stream verification, e.g.:
- SecM_VerifySigRsaPssSha256
- SecM_VerifySigEd25519PH

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. SmhJobRef

- **UUID**: `d60da727-ed84-438f-b298-500fde867ab8`
- **引用名**: `SmhJobRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `SmhJob`
- **完整路径**: `/MICROSAR/Smh/SmhJob`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: References a SmhSignatureVerify job, which shall be used by this stream verification.

########## 配置容器

本模块包含 **1** 个配置容器：

########### 1. SmhDiscretHashConfig

**容器属性**:

- **UUID**: `4e51524b-a403-48b3-9ada-c1942ae9616f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SmhDiscretHashConfig`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Configure a discrete hash for the verification, which is used to calculate a hash before verifying the signature.

############ 引用关系

此容器包含 **1** 个引用：

############# REFERENCE 类型引用

############## 1. SmhJobRef

- **UUID**: `51d9a895-6b6e-4e9f-88f1-5310319d40d3`
- **引用名**: `SmhJobRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `SmhJob`
- **完整路径**: `/MICROSAR/Smh/SmhJob`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: References a SmhHash job, which shall be used for the discrete hash.

######### 9. SmhDiscretHashConfig

**容器属性**:

- **UUID**: `4e51524b-a403-48b3-9ada-c1942ae9616f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SmhDiscretHashConfig`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Configure a discrete hash for the verification, which is used to calculate a hash before verifying the signature.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. SmhJobRef

- **UUID**: `51d9a895-6b6e-4e9f-88f1-5310319d40d3`
- **引用名**: `SmhJobRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `SmhJob`
- **完整路径**: `/MICROSAR/Smh/SmhJob`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: References a SmhHash job, which shall be used for the discrete hash.

######### 10. SmhSecurityClassVendor

**容器属性**:

- **UUID**: `56bf5e0a-bd3a-4608-9838-e22f4d0b9b92`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SmhSecurityClassVendor`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container to configure the stream verification for security class CCC.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. SmhDefaultSecurityClassVendorConfig

- **UUID**: `6afe1497-e7b4-42b1-9a0b-b720a388b484`
- **引用名**: `SmhDefaultSecurityClassVendorConfig`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `SmhSecurityClassVendorConfig`
- **完整路径**: `/MICROSAR/Smh/SmhVerification/SmhStreamVerification/SmhSecurityClassVendor/SmhSecurityClassVendorConfig`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Default stream verification for the security class Vendor:
SecM_VerifyClassVendor

########## 配置容器

本模块包含 **1** 个配置容器：

########### 1. SmhSecurityClassVendorConfig

**容器属性**:

- **UUID**: `10b6f3b0-43c8-4825-897d-bde63d0e9513`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SmhSecurityClassVendorConfig`
- **多重性**: [1..infinite]
- **构建后可变**: false

**容器描述**:

Container to configure the stream verifications for security class CCC.

############ 参数配置

此容器包含 **2** 个参数：

############# INTEGER 类型参数

############## 1. SmhSizeOfVendorChecksum

- **UUID**: `cd3c9263-f865-4b17-84c1-39421281e243`
- **参数名**: `SmhSizeOfVendorChecksum`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `1`
- **取值范围**: [0..65535]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Configure the size of the vendor checksum.

############# FUNCTION-NAME 类型参数

############## 1. SmhClassVendorFunctionName

- **UUID**: `ca8ec340-3791-4548-816a-0e9d2459dea8`
- **参数名**: `SmhClassVendorFunctionName`
- **数据类型**: FUNCTION-NAME
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Configure the function name of the stream verification.

######### 11. SmhSecurityClassVendorConfig

**容器属性**:

- **UUID**: `10b6f3b0-43c8-4825-897d-bde63d0e9513`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SmhSecurityClassVendorConfig`
- **多重性**: [1..infinite]
- **构建后可变**: false

**容器描述**:

Container to configure the stream verifications for security class CCC.

########## 参数配置

此容器包含 **2** 个参数：

########### INTEGER 类型参数

############ 1. SmhSizeOfVendorChecksum

- **UUID**: `cd3c9263-f865-4b17-84c1-39421281e243`
- **参数名**: `SmhSizeOfVendorChecksum`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `1`
- **取值范围**: [0..65535]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Configure the size of the vendor checksum.

########### FUNCTION-NAME 类型参数

############ 1. SmhClassVendorFunctionName

- **UUID**: `ca8ec340-3791-4548-816a-0e9d2459dea8`
- **参数名**: `SmhClassVendorFunctionName`
- **数据类型**: FUNCTION-NAME
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Configure the function name of the stream verification.

######### 12. SmhSecurityClassDDDType

**容器属性**:

- **UUID**: `d4091ae3-bc5f-49ed-aab5-4f51d555f432`
- **容器类型**: CHOICE-CONTAINER
- **容器名称**: `SmhSecurityClassDDDType`
- **多重性**: [1..1]
- **构建后可变**: false

**容器选择**:

- **SmhCrc**
  - UUID: `d77a32e4-ca21-4c5c-a0ec-75a6fae134fe`
  - 描述: Container to configure the CRC
- **SmhHash**
  - UUID: `860c29ac-feed-4843-be72-6b659b349d99`
  - 描述: Container to configure the hash

**容器描述**:

Specify the type of the security class DDD

####### 11. SmhSecurityClassDDD

**容器属性**:

- **UUID**: `f65076e1-6a4f-4afd-8f21-e8faea37fe6d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SmhSecurityClassDDD`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container to configure the stream verification for security class DDD.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. SmhDefaultSecurityClassDDDConfig

- **UUID**: `46906c73-00d0-4ce1-83bd-dd5f4112a3d8`
- **引用名**: `SmhDefaultSecurityClassDDDConfig`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `SmhSecurityClassDDDConfig`
- **完整路径**: `/MICROSAR/Smh/SmhVerification/SmhStreamVerification/SmhSecurityClassDDD/SmhSecurityClassDDDConfig`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Default stream verification for the security class DDD:
SecM_VerifyClassDDD

######## 配置容器

本模块包含 **4** 个配置容器：

######### 1. SmhSecurityClassDDDConfig

**容器属性**:

- **UUID**: `9edb72f4-2681-4d78-b583-25881036d326`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SmhSecurityClassDDDConfig`
- **多重性**: [1..infinite]
- **构建后可变**: false

**容器描述**:

Container to configure the stream verifications for security class DDD.

########## 参数配置

此容器包含 **3** 个参数：

########### BOOLEAN 类型参数

############ 1. SmhUpdateLengthOfHashedData

- **UUID**: `d4134277-9064-464b-a0e2-444e36fc56bc`
- **参数名**: `SmhUpdateLengthOfHashedData`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: If enabled, the security module will update the current length of hashed data in SecM_SignatureParamtype::currentDataLength.

############ 2. SmhComputationOnly

- **UUID**: `a77c5004-72b2-4e59-aee2-025769278b81`
- **参数名**: `SmhComputationOnly`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: If enabled the security module will just compute the CRC/hash without verifying it. The computed CRC/hash is provided via SecM_SignatureParamtype::sigSourceBuffer.

########### FUNCTION-NAME 类型参数

############ 1. SmhFunctionName

- **UUID**: `262ace43-2c7c-4462-9763-63cfd27ebe48`
- **参数名**: `SmhFunctionName`
- **数据类型**: FUNCTION-NAME
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Configure the function name of the stream verification, e.g.:
- SecM_VerifyCrc32
- SecM_VerifyHashSha512

########## 配置容器

本模块包含 **3** 个配置容器：

########### 1. SmhCrc

**容器属性**:

- **UUID**: `d77a32e4-ca21-4c5c-a0ec-75a6fae134fe`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SmhCrc`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container to configure the CRC

############ 引用关系

此容器包含 **1** 个引用：

############# CHOICE-REFERENCE 类型引用

############## 1. SmhCrcRef

- **UUID**: `545924b6-97cc-4283-9bee-5159bda168f9`
- **引用名**: `SmhCrcRef`
- **引用类型**: CHOICE-REFERENCE
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **需要索引**: false
- **目标引用列表**:
  - `/MICROSAR/Smh/SmhCrc/SmhCrc16`
  - `/MICROSAR/Smh/SmhCrc/SmhCrc32`
  - `/MICROSAR/Smh/SmhCrc/SmhCrc64`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: References a CRC configuration, which shall be used by this stream verification.

########### 2. SmhHash

**容器属性**:

- **UUID**: `860c29ac-feed-4843-be72-6b659b349d99`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SmhHash`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container to configure the hash

############ 引用关系

此容器包含 **1** 个引用：

############# REFERENCE 类型引用

############## 1. SmhJobRef

- **UUID**: `935a56dc-ff73-4f9e-9090-032d0f6d04cb`
- **引用名**: `SmhJobRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `SmhJob`
- **完整路径**: `/MICROSAR/Smh/SmhJob`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: References a SmhHash job, which shall be used by this stream verification.

########### 3. SmhSecurityClassDDDType

**容器属性**:

- **UUID**: `d4091ae3-bc5f-49ed-aab5-4f51d555f432`
- **容器类型**: CHOICE-CONTAINER
- **容器名称**: `SmhSecurityClassDDDType`
- **多重性**: [1..1]
- **构建后可变**: false

**容器选择**:

- **SmhCrc**
  - UUID: `d77a32e4-ca21-4c5c-a0ec-75a6fae134fe`
  - 描述: Container to configure the CRC
- **SmhHash**
  - UUID: `860c29ac-feed-4843-be72-6b659b349d99`
  - 描述: Container to configure the hash

**容器描述**:

Specify the type of the security class DDD

######### 2. SmhCrc

**容器属性**:

- **UUID**: `d77a32e4-ca21-4c5c-a0ec-75a6fae134fe`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SmhCrc`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container to configure the CRC

########## 引用关系

此容器包含 **1** 个引用：

########### CHOICE-REFERENCE 类型引用

############ 1. SmhCrcRef

- **UUID**: `545924b6-97cc-4283-9bee-5159bda168f9`
- **引用名**: `SmhCrcRef`
- **引用类型**: CHOICE-REFERENCE
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **需要索引**: false
- **目标引用列表**:
  - `/MICROSAR/Smh/SmhCrc/SmhCrc16`
  - `/MICROSAR/Smh/SmhCrc/SmhCrc32`
  - `/MICROSAR/Smh/SmhCrc/SmhCrc64`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: References a CRC configuration, which shall be used by this stream verification.

######### 3. SmhHash

**容器属性**:

- **UUID**: `860c29ac-feed-4843-be72-6b659b349d99`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SmhHash`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container to configure the hash

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. SmhJobRef

- **UUID**: `935a56dc-ff73-4f9e-9090-032d0f6d04cb`
- **引用名**: `SmhJobRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `SmhJob`
- **完整路径**: `/MICROSAR/Smh/SmhJob`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: References a SmhHash job, which shall be used by this stream verification.

######### 4. SmhSecurityClassDDDType

**容器属性**:

- **UUID**: `d4091ae3-bc5f-49ed-aab5-4f51d555f432`
- **容器类型**: CHOICE-CONTAINER
- **容器名称**: `SmhSecurityClassDDDType`
- **多重性**: [1..1]
- **构建后可变**: false

**容器选择**:

- **SmhCrc**
  - UUID: `d77a32e4-ca21-4c5c-a0ec-75a6fae134fe`
  - 描述: Container to configure the CRC
- **SmhHash**
  - UUID: `860c29ac-feed-4843-be72-6b659b349d99`
  - 描述: Container to configure the hash

**容器描述**:

Specify the type of the security class DDD

####### 12. SmhSecurityClassDDDConfig

**容器属性**:

- **UUID**: `9edb72f4-2681-4d78-b583-25881036d326`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SmhSecurityClassDDDConfig`
- **多重性**: [1..infinite]
- **构建后可变**: false

**容器描述**:

Container to configure the stream verifications for security class DDD.

######## 参数配置

此容器包含 **3** 个参数：

######### BOOLEAN 类型参数

########## 1. SmhUpdateLengthOfHashedData

- **UUID**: `d4134277-9064-464b-a0e2-444e36fc56bc`
- **参数名**: `SmhUpdateLengthOfHashedData`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: If enabled, the security module will update the current length of hashed data in SecM_SignatureParamtype::currentDataLength.

########## 2. SmhComputationOnly

- **UUID**: `a77c5004-72b2-4e59-aee2-025769278b81`
- **参数名**: `SmhComputationOnly`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: If enabled the security module will just compute the CRC/hash without verifying it. The computed CRC/hash is provided via SecM_SignatureParamtype::sigSourceBuffer.

######### FUNCTION-NAME 类型参数

########## 1. SmhFunctionName

- **UUID**: `262ace43-2c7c-4462-9763-63cfd27ebe48`
- **参数名**: `SmhFunctionName`
- **数据类型**: FUNCTION-NAME
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Configure the function name of the stream verification, e.g.:
- SecM_VerifyCrc32
- SecM_VerifyHashSha512

######## 配置容器

本模块包含 **3** 个配置容器：

######### 1. SmhCrc

**容器属性**:

- **UUID**: `d77a32e4-ca21-4c5c-a0ec-75a6fae134fe`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SmhCrc`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container to configure the CRC

########## 引用关系

此容器包含 **1** 个引用：

########### CHOICE-REFERENCE 类型引用

############ 1. SmhCrcRef

- **UUID**: `545924b6-97cc-4283-9bee-5159bda168f9`
- **引用名**: `SmhCrcRef`
- **引用类型**: CHOICE-REFERENCE
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **需要索引**: false
- **目标引用列表**:
  - `/MICROSAR/Smh/SmhCrc/SmhCrc16`
  - `/MICROSAR/Smh/SmhCrc/SmhCrc32`
  - `/MICROSAR/Smh/SmhCrc/SmhCrc64`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: References a CRC configuration, which shall be used by this stream verification.

######### 2. SmhHash

**容器属性**:

- **UUID**: `860c29ac-feed-4843-be72-6b659b349d99`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SmhHash`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container to configure the hash

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. SmhJobRef

- **UUID**: `935a56dc-ff73-4f9e-9090-032d0f6d04cb`
- **引用名**: `SmhJobRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `SmhJob`
- **完整路径**: `/MICROSAR/Smh/SmhJob`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: References a SmhHash job, which shall be used by this stream verification.

######### 3. SmhSecurityClassDDDType

**容器属性**:

- **UUID**: `d4091ae3-bc5f-49ed-aab5-4f51d555f432`
- **容器类型**: CHOICE-CONTAINER
- **容器名称**: `SmhSecurityClassDDDType`
- **多重性**: [1..1]
- **构建后可变**: false

**容器选择**:

- **SmhCrc**
  - UUID: `d77a32e4-ca21-4c5c-a0ec-75a6fae134fe`
  - 描述: Container to configure the CRC
- **SmhHash**
  - UUID: `860c29ac-feed-4843-be72-6b659b349d99`
  - 描述: Container to configure the hash

**容器描述**:

Specify the type of the security class DDD

####### 13. SmhCrc

**容器属性**:

- **UUID**: `d77a32e4-ca21-4c5c-a0ec-75a6fae134fe`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SmhCrc`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container to configure the CRC

######## 引用关系

此容器包含 **1** 个引用：

######### CHOICE-REFERENCE 类型引用

########## 1. SmhCrcRef

- **UUID**: `545924b6-97cc-4283-9bee-5159bda168f9`
- **引用名**: `SmhCrcRef`
- **引用类型**: CHOICE-REFERENCE
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **需要索引**: false
- **目标引用列表**:
  - `/MICROSAR/Smh/SmhCrc/SmhCrc16`
  - `/MICROSAR/Smh/SmhCrc/SmhCrc32`
  - `/MICROSAR/Smh/SmhCrc/SmhCrc64`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: References a CRC configuration, which shall be used by this stream verification.

####### 14. SmhHash

**容器属性**:

- **UUID**: `860c29ac-feed-4843-be72-6b659b349d99`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SmhHash`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container to configure the hash

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. SmhJobRef

- **UUID**: `935a56dc-ff73-4f9e-9090-032d0f6d04cb`
- **引用名**: `SmhJobRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `SmhJob`
- **完整路径**: `/MICROSAR/Smh/SmhJob`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: References a SmhHash job, which shall be used by this stream verification.

####### 15. SmhSecurityClassC

**容器属性**:

- **UUID**: `0bbafb93-8d89-4aa2-a917-76ff0cc0016a`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SmhSecurityClassC`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container to configure the stream verification for security class C.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. SmhDefaultSecurityClassCConfig

- **UUID**: `29bb2998-5a48-4047-9169-d03556cff09d`
- **引用名**: `SmhDefaultSecurityClassCConfig`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `SmhSecurityClassCConfig`
- **完整路径**: `/MICROSAR/Smh/SmhVerification/SmhStreamVerification/SmhSecurityClassC/SmhSecurityClassCConfig`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Default stream verification for the security class C:
SecM_VerifyClassC

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. SmhSecurityClassCConfig

**容器属性**:

- **UUID**: `db313d05-7ad6-453b-bc32-372ecc4c5ec4`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SmhSecurityClassCConfig`
- **多重性**: [1..infinite]
- **构建后可变**: false

**容器描述**:

Container to configure the stream verifications for security class C.

########## 参数配置

此容器包含 **3** 个参数：

########### BOOLEAN 类型参数

############ 1. SmhUpdateLengthOfHashedData

- **UUID**: `1e161cb2-0f71-4990-8d7a-84f8f1fbf05c`
- **参数名**: `SmhUpdateLengthOfHashedData`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: If enabled, the security module will update the current length of hashed data in SecM_SignatureParamtype::currentDataLength.

############ 2. SmhComputationOnly

- **UUID**: `ca7644f1-ecc0-46b1-b73f-f926b42df198`
- **参数名**: `SmhComputationOnly`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: If enabled the security module will just compute the MAC without verifying it. The computed MAC is provided via SecM_SignatureParamtype::sigSourceBuffer.

########### FUNCTION-NAME 类型参数

############ 1. SmhFunctionName

- **UUID**: `c9a732c4-3d9b-4838-a3ed-c21f7878e3c5`
- **参数名**: `SmhFunctionName`
- **数据类型**: FUNCTION-NAME
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Configure the function name of the stream verification, e.g.:
- SecM_VerifyMacHmacSha1
- SecM_VerifyMacCmac

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. SmhJobRef

- **UUID**: `4443273c-b72e-4faa-ae72-41ee1d2fe23c`
- **引用名**: `SmhJobRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `SmhJob`
- **完整路径**: `/MICROSAR/Smh/SmhJob`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: References a SmhMacVerify or SmhMacGenerate job, which shall be used by this stream verification.

####### 16. SmhSecurityClassCConfig

**容器属性**:

- **UUID**: `db313d05-7ad6-453b-bc32-372ecc4c5ec4`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SmhSecurityClassCConfig`
- **多重性**: [1..infinite]
- **构建后可变**: false

**容器描述**:

Container to configure the stream verifications for security class C.

######## 参数配置

此容器包含 **3** 个参数：

######### BOOLEAN 类型参数

########## 1. SmhUpdateLengthOfHashedData

- **UUID**: `1e161cb2-0f71-4990-8d7a-84f8f1fbf05c`
- **参数名**: `SmhUpdateLengthOfHashedData`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: If enabled, the security module will update the current length of hashed data in SecM_SignatureParamtype::currentDataLength.

########## 2. SmhComputationOnly

- **UUID**: `ca7644f1-ecc0-46b1-b73f-f926b42df198`
- **参数名**: `SmhComputationOnly`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: If enabled the security module will just compute the MAC without verifying it. The computed MAC is provided via SecM_SignatureParamtype::sigSourceBuffer.

######### FUNCTION-NAME 类型参数

########## 1. SmhFunctionName

- **UUID**: `c9a732c4-3d9b-4838-a3ed-c21f7878e3c5`
- **参数名**: `SmhFunctionName`
- **数据类型**: FUNCTION-NAME
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Configure the function name of the stream verification, e.g.:
- SecM_VerifyMacHmacSha1
- SecM_VerifyMacCmac

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. SmhJobRef

- **UUID**: `4443273c-b72e-4faa-ae72-41ee1d2fe23c`
- **引用名**: `SmhJobRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `SmhJob`
- **完整路径**: `/MICROSAR/Smh/SmhJob`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: References a SmhMacVerify or SmhMacGenerate job, which shall be used by this stream verification.

####### 17. SmhSecurityClassCCC

**容器属性**:

- **UUID**: `e8bb9b83-5292-4b97-9d4e-6f37ada0a6c1`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SmhSecurityClassCCC`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container to configure the stream verification for security class CCC.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. SmhDefaultSecurityClassCCCConfig

- **UUID**: `0442501f-54c8-4df8-a5a1-c1a5f7de1398`
- **引用名**: `SmhDefaultSecurityClassCCCConfig`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `SmhSecurityClassCCCConfig`
- **完整路径**: `/MICROSAR/Smh/SmhVerification/SmhStreamVerification/SmhSecurityClassCCC/SmhSecurityClassCCCConfig`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Default stream verification for the security class CCC:
SecM_VerifyClassCCC

######## 配置容器

本模块包含 **2** 个配置容器：

######### 1. SmhSecurityClassCCCConfig

**容器属性**:

- **UUID**: `664dcb07-95ff-4179-8d6e-6ef8f5b49b46`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SmhSecurityClassCCCConfig`
- **多重性**: [1..infinite]
- **构建后可变**: false

**容器描述**:

Container to configure the stream verifications for security class CCC.

########## 参数配置

此容器包含 **2** 个参数：

########### BOOLEAN 类型参数

############ 1. SmhUpdateLengthOfHashedData

- **UUID**: `eec6e339-e8e3-44fa-b123-4e6a0eb5f1f0`
- **参数名**: `SmhUpdateLengthOfHashedData`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: If enabled, the security module will update the current length of hashed data in SecM_SignatureParamtype::currentDataLength.

########### FUNCTION-NAME 类型参数

############ 1. SmhFunctionName

- **UUID**: `2ea862e4-436b-42bd-9762-5fcc32430434`
- **参数名**: `SmhFunctionName`
- **数据类型**: FUNCTION-NAME
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Configure the function name of the stream verification, e.g.:
- SecM_VerifySigRsaPssSha256
- SecM_VerifySigEd25519PH

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. SmhJobRef

- **UUID**: `d60da727-ed84-438f-b298-500fde867ab8`
- **引用名**: `SmhJobRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `SmhJob`
- **完整路径**: `/MICROSAR/Smh/SmhJob`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: References a SmhSignatureVerify job, which shall be used by this stream verification.

########## 配置容器

本模块包含 **1** 个配置容器：

########### 1. SmhDiscretHashConfig

**容器属性**:

- **UUID**: `4e51524b-a403-48b3-9ada-c1942ae9616f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SmhDiscretHashConfig`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Configure a discrete hash for the verification, which is used to calculate a hash before verifying the signature.

############ 引用关系

此容器包含 **1** 个引用：

############# REFERENCE 类型引用

############## 1. SmhJobRef

- **UUID**: `51d9a895-6b6e-4e9f-88f1-5310319d40d3`
- **引用名**: `SmhJobRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `SmhJob`
- **完整路径**: `/MICROSAR/Smh/SmhJob`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: References a SmhHash job, which shall be used for the discrete hash.

######### 2. SmhDiscretHashConfig

**容器属性**:

- **UUID**: `4e51524b-a403-48b3-9ada-c1942ae9616f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SmhDiscretHashConfig`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Configure a discrete hash for the verification, which is used to calculate a hash before verifying the signature.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. SmhJobRef

- **UUID**: `51d9a895-6b6e-4e9f-88f1-5310319d40d3`
- **引用名**: `SmhJobRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `SmhJob`
- **完整路径**: `/MICROSAR/Smh/SmhJob`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: References a SmhHash job, which shall be used for the discrete hash.

####### 18. SmhSecurityClassCCCConfig

**容器属性**:

- **UUID**: `664dcb07-95ff-4179-8d6e-6ef8f5b49b46`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SmhSecurityClassCCCConfig`
- **多重性**: [1..infinite]
- **构建后可变**: false

**容器描述**:

Container to configure the stream verifications for security class CCC.

######## 参数配置

此容器包含 **2** 个参数：

######### BOOLEAN 类型参数

########## 1. SmhUpdateLengthOfHashedData

- **UUID**: `eec6e339-e8e3-44fa-b123-4e6a0eb5f1f0`
- **参数名**: `SmhUpdateLengthOfHashedData`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: If enabled, the security module will update the current length of hashed data in SecM_SignatureParamtype::currentDataLength.

######### FUNCTION-NAME 类型参数

########## 1. SmhFunctionName

- **UUID**: `2ea862e4-436b-42bd-9762-5fcc32430434`
- **参数名**: `SmhFunctionName`
- **数据类型**: FUNCTION-NAME
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Configure the function name of the stream verification, e.g.:
- SecM_VerifySigRsaPssSha256
- SecM_VerifySigEd25519PH

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. SmhJobRef

- **UUID**: `d60da727-ed84-438f-b298-500fde867ab8`
- **引用名**: `SmhJobRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `SmhJob`
- **完整路径**: `/MICROSAR/Smh/SmhJob`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: References a SmhSignatureVerify job, which shall be used by this stream verification.

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. SmhDiscretHashConfig

**容器属性**:

- **UUID**: `4e51524b-a403-48b3-9ada-c1942ae9616f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SmhDiscretHashConfig`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Configure a discrete hash for the verification, which is used to calculate a hash before verifying the signature.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. SmhJobRef

- **UUID**: `51d9a895-6b6e-4e9f-88f1-5310319d40d3`
- **引用名**: `SmhJobRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `SmhJob`
- **完整路径**: `/MICROSAR/Smh/SmhJob`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: References a SmhHash job, which shall be used for the discrete hash.

####### 19. SmhDiscretHashConfig

**容器属性**:

- **UUID**: `4e51524b-a403-48b3-9ada-c1942ae9616f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SmhDiscretHashConfig`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Configure a discrete hash for the verification, which is used to calculate a hash before verifying the signature.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. SmhJobRef

- **UUID**: `51d9a895-6b6e-4e9f-88f1-5310319d40d3`
- **引用名**: `SmhJobRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `SmhJob`
- **完整路径**: `/MICROSAR/Smh/SmhJob`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: References a SmhHash job, which shall be used for the discrete hash.

####### 20. SmhSecurityClassVendor

**容器属性**:

- **UUID**: `56bf5e0a-bd3a-4608-9838-e22f4d0b9b92`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SmhSecurityClassVendor`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container to configure the stream verification for security class CCC.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. SmhDefaultSecurityClassVendorConfig

- **UUID**: `6afe1497-e7b4-42b1-9a0b-b720a388b484`
- **引用名**: `SmhDefaultSecurityClassVendorConfig`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `SmhSecurityClassVendorConfig`
- **完整路径**: `/MICROSAR/Smh/SmhVerification/SmhStreamVerification/SmhSecurityClassVendor/SmhSecurityClassVendorConfig`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Default stream verification for the security class Vendor:
SecM_VerifyClassVendor

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. SmhSecurityClassVendorConfig

**容器属性**:

- **UUID**: `10b6f3b0-43c8-4825-897d-bde63d0e9513`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SmhSecurityClassVendorConfig`
- **多重性**: [1..infinite]
- **构建后可变**: false

**容器描述**:

Container to configure the stream verifications for security class CCC.

########## 参数配置

此容器包含 **2** 个参数：

########### INTEGER 类型参数

############ 1. SmhSizeOfVendorChecksum

- **UUID**: `cd3c9263-f865-4b17-84c1-39421281e243`
- **参数名**: `SmhSizeOfVendorChecksum`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `1`
- **取值范围**: [0..65535]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Configure the size of the vendor checksum.

########### FUNCTION-NAME 类型参数

############ 1. SmhClassVendorFunctionName

- **UUID**: `ca8ec340-3791-4548-816a-0e9d2459dea8`
- **参数名**: `SmhClassVendorFunctionName`
- **数据类型**: FUNCTION-NAME
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Configure the function name of the stream verification.

####### 21. SmhSecurityClassVendorConfig

**容器属性**:

- **UUID**: `10b6f3b0-43c8-4825-897d-bde63d0e9513`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SmhSecurityClassVendorConfig`
- **多重性**: [1..infinite]
- **构建后可变**: false

**容器描述**:

Container to configure the stream verifications for security class CCC.

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. SmhSizeOfVendorChecksum

- **UUID**: `cd3c9263-f865-4b17-84c1-39421281e243`
- **参数名**: `SmhSizeOfVendorChecksum`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `1`
- **取值范围**: [0..65535]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Configure the size of the vendor checksum.

######### FUNCTION-NAME 类型参数

########## 1. SmhClassVendorFunctionName

- **UUID**: `ca8ec340-3791-4548-816a-0e9d2459dea8`
- **参数名**: `SmhClassVendorFunctionName`
- **数据类型**: FUNCTION-NAME
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Configure the function name of the stream verification.

####### 22. SmhSecurityClassDDDType

**容器属性**:

- **UUID**: `d4091ae3-bc5f-49ed-aab5-4f51d555f432`
- **容器类型**: CHOICE-CONTAINER
- **容器名称**: `SmhSecurityClassDDDType`
- **多重性**: [1..1]
- **构建后可变**: false

**容器选择**:

- **SmhCrc**
  - UUID: `d77a32e4-ca21-4c5c-a0ec-75a6fae134fe`
  - 描述: Container to configure the CRC
- **SmhHash**
  - UUID: `860c29ac-feed-4843-be72-6b659b349d99`
  - 描述: Container to configure the hash

**容器描述**:

Specify the type of the security class DDD

##### 13. SmhMonolithicVerification

**容器属性**:

- **UUID**: `b6db6564-d81b-48ce-8949-a13fdbe982db`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SmhMonolithicVerification`
- **多重性**: [1..1]
- **构建后可变**: false

**容器描述**:

Container to configure the monolythic verifications.
Monolythic verifications are used to verify the data after a complete download has been performed (OutputVerification).

###### 参数配置

此容器包含 **9** 个参数：

####### INTEGER 类型参数

######## 1. SmhOperationCountOfWrapper

- **UUID**: `ac221637-3218-4e9d-a2db-22bf43e94484`
- **参数名**: `SmhOperationCountOfWrapper`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `4`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Specify the number of operations:
- SecurityClass Verification
- CRC Total
- Vendor Verification
- CRC Written

######## 2. SmhReadBufferSize

- **UUID**: `19c23fb8-4d2c-4b43-b461-b20127cf10d7`
- **参数名**: `SmhReadBufferSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `64`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Specify the length of the read buffer. The security module will read data with this size from the memory and provides it to the verification function.

####### BOOLEAN 类型参数

######## 1. SmhExportVerificationWrapper

- **UUID**: `e0ddce9a-544a-4eb5-ab83-be5fe8b8a436`
- **参数名**: `SmhExportVerificationWrapper`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Configure if the function SecM_VerificationWrapper can be accessed externally.

######## 2. SmhCheckAddressRangeOverflow

- **UUID**: `af4b6b53-a14e-4a52-90ea-917f9d0ecc81`
- **参数名**: `SmhCheckAddressRangeOverflow`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: If enable, the security module will check that the memory range defined by address and length create an address range overflow.

######## 3. SmhAssertReadCount

- **UUID**: `2490e6b2-ef15-4258-8517-7bbf2146f0b8`
- **参数名**: `SmhAssertReadCount`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Enabled a check to verify that the read count matches the requested read length.

######## 4. SmhCRCTotal

- **UUID**: `1635db7f-a97e-48d4-a121-db760ce89659`
- **参数名**: `SmhCRCTotal`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: The security component always calculates a CRCtotal for a logical block when enabled. Thus, the application is able to verify the values within the application.

######## 5. SmhCRCWritten

- **UUID**: `44d762fd-44f3-4688-a85f-c46cad743e7a`
- **参数名**: `SmhCRCWritten`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: The security component calculates the CRC value of the written (segments) data and compares it against the provided verification data at offset SmhCRCOffset.

######## 6. SmhCRCWrittenGet

- **UUID**: `28122ec7-1abf-40f1-a967-bc5575af82b4`
- **参数名**: `SmhCRCWrittenGet`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: The security component calculates the CRC value of the written (segments) data and provides it to the caller to be verified externally.

####### ENUMERATION 类型参数

######## 1. SmhMemoryAccessMode

- **UUID**: `70e0f7fd-6349-48b0-8968-2e46728f03ca`
- **参数名**: `SmhMemoryAccessMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `ADDRESS`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `ADDRESS` (来源: Vector Informatik)
  - `FILE` (来源: Vector Informatik)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: The access mode of the security component is fixed to the memory access function. The setting is displayed for documentation purposes only.

###### 引用关系

此容器包含 **1** 个引用：

####### CHOICE-REFERENCE 类型引用

######## 1. SmhDefaultMonolithicVerificationConfig

- **UUID**: `0839edb9-4fa5-43f9-b0cd-d467cfb2d009`
- **引用名**: `SmhDefaultMonolithicVerificationConfig`
- **引用类型**: CHOICE-REFERENCE
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **需要索引**: false
- **目标引用列表**:
  - `/MICROSAR/Smh/SmhVerification/SmhMonolithicVerification/SmhSecurityClassDDD/SmhSecurityClassDDDConfig`
  - `/MICROSAR/Smh/SmhVerification/SmhMonolithicVerification/SmhSecurityClassC/SmhSecurityClassCConfig`
  - `/MICROSAR/Smh/SmhVerification/SmhMonolithicVerification/SmhSecurityClassCCC/SmhSecurityClassCCCConfig`
  - `/MICROSAR/Smh/SmhVerification/SmhMonolithicVerification/SmhSecurityClassVendor/SmhSecurityClassVendorConfig`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Default monolithic verification:
SecM_Verification

###### 配置容器

本模块包含 **8** 个配置容器：

####### 1. SmhSecurityClassDDD

**容器属性**:

- **UUID**: `72791700-82db-4ae8-913d-546993a59628`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SmhSecurityClassDDD`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container to configure the monolythic verification for security class DDD.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. SmhDefaultSecurityClassDDDConfig

- **UUID**: `8000ac6e-db98-4d89-ad2e-e5d407d6e2cf`
- **引用名**: `SmhDefaultSecurityClassDDDConfig`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `SmhSecurityClassDDDConfig`
- **完整路径**: `/MICROSAR/Smh/SmhVerification/SmhMonolithicVerification/SmhSecurityClassDDD/SmhSecurityClassDDDConfig`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Default monolythic verification for the security class DDD:
SecM_VerificationClassDDD

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. SmhSecurityClassDDDConfig

**容器属性**:

- **UUID**: `8b918e7c-9888-4c0f-ab87-064e3f447ed8`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SmhSecurityClassDDDConfig`
- **多重性**: [1..infinite]
- **构建后可变**: false

**容器描述**:

Container to configure the monolythic verifications for security class DDD.

########## 参数配置

此容器包含 **4** 个参数：

########### INTEGER 类型参数

############ 1. SmhSignatureOffset

- **UUID**: `058834c9-af5f-4982-885e-fbfd6a591f78`
- **参数名**: `SmhSignatureOffset`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Specify the offset to the signature (CRC or hash value).

############ 2. SmhCRCOffset

- **UUID**: `f9ad26cf-04f7-460c-bb94-5033c8c860a6`
- **参数名**: `SmhCRCOffset`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Specify the offset to the CRC value (used by CRC written)

########### BOOLEAN 类型参数

############ 1. SmhIncludeAddressAndLengthInSignature

- **UUID**: `db44bc4a-9cca-473b-896d-be630b6785e9`
- **参数名**: `SmhIncludeAddressAndLengthInSignature`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Specify if the address and length of the segments shall be taken into account in the verification.

########### FUNCTION-NAME 类型参数

############ 1. SmhFunctionName

- **UUID**: `ab733ae7-604b-4644-98db-a29bf0b8b00b`
- **参数名**: `SmhFunctionName`
- **数据类型**: FUNCTION-NAME
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Configure the function name to execute the monolythic verification, e.g.:
- SecM_VerificationClassDDD_Crc32
- SecM_VerificationClassDDD_Sha512

########## 引用关系

此容器包含 **2** 个引用：

########### REFERENCE 类型引用

############ 1. SmhStreamVerificationConfig

- **UUID**: `06866c75-743e-46f3-98cd-693b08a484a1`
- **引用名**: `SmhStreamVerificationConfig`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `SmhSecurityClassDDDConfig`
- **完整路径**: `/MICROSAR/Smh/SmhVerification/SmhStreamVerification/SmhSecurityClassDDD/SmhSecurityClassDDDConfig`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Reference to the underlying StreamVerification to eecute the verification operation.

############ 2. SmhVendorVerificationConfig

- **UUID**: `22a7ef68-050b-43d2-9efa-64b75baf9e7b`
- **引用名**: `SmhVendorVerificationConfig`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `SmhSecurityClassVendorConfig`
- **完整路径**: `/MICROSAR/Smh/SmhVerification/SmhStreamVerification/SmhSecurityClassVendor/SmhSecurityClassVendorConfig`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Reference to a VendorVerification to execute next to the CRC/hash verification an additional vendor checksum.

####### 2. SmhSecurityClassDDDConfig

**容器属性**:

- **UUID**: `8b918e7c-9888-4c0f-ab87-064e3f447ed8`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SmhSecurityClassDDDConfig`
- **多重性**: [1..infinite]
- **构建后可变**: false

**容器描述**:

Container to configure the monolythic verifications for security class DDD.

######## 参数配置

此容器包含 **4** 个参数：

######### INTEGER 类型参数

########## 1. SmhSignatureOffset

- **UUID**: `058834c9-af5f-4982-885e-fbfd6a591f78`
- **参数名**: `SmhSignatureOffset`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Specify the offset to the signature (CRC or hash value).

########## 2. SmhCRCOffset

- **UUID**: `f9ad26cf-04f7-460c-bb94-5033c8c860a6`
- **参数名**: `SmhCRCOffset`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Specify the offset to the CRC value (used by CRC written)

######### BOOLEAN 类型参数

########## 1. SmhIncludeAddressAndLengthInSignature

- **UUID**: `db44bc4a-9cca-473b-896d-be630b6785e9`
- **参数名**: `SmhIncludeAddressAndLengthInSignature`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Specify if the address and length of the segments shall be taken into account in the verification.

######### FUNCTION-NAME 类型参数

########## 1. SmhFunctionName

- **UUID**: `ab733ae7-604b-4644-98db-a29bf0b8b00b`
- **参数名**: `SmhFunctionName`
- **数据类型**: FUNCTION-NAME
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Configure the function name to execute the monolythic verification, e.g.:
- SecM_VerificationClassDDD_Crc32
- SecM_VerificationClassDDD_Sha512

######## 引用关系

此容器包含 **2** 个引用：

######### REFERENCE 类型引用

########## 1. SmhStreamVerificationConfig

- **UUID**: `06866c75-743e-46f3-98cd-693b08a484a1`
- **引用名**: `SmhStreamVerificationConfig`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `SmhSecurityClassDDDConfig`
- **完整路径**: `/MICROSAR/Smh/SmhVerification/SmhStreamVerification/SmhSecurityClassDDD/SmhSecurityClassDDDConfig`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Reference to the underlying StreamVerification to eecute the verification operation.

########## 2. SmhVendorVerificationConfig

- **UUID**: `22a7ef68-050b-43d2-9efa-64b75baf9e7b`
- **引用名**: `SmhVendorVerificationConfig`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `SmhSecurityClassVendorConfig`
- **完整路径**: `/MICROSAR/Smh/SmhVerification/SmhStreamVerification/SmhSecurityClassVendor/SmhSecurityClassVendorConfig`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Reference to a VendorVerification to execute next to the CRC/hash verification an additional vendor checksum.

####### 3. SmhSecurityClassC

**容器属性**:

- **UUID**: `9184de9d-b87a-4814-9987-c262b26ccff8`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SmhSecurityClassC`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container to configure the monolythic verification for security class C.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. SmhDefaultSecurityClassCConfig

- **UUID**: `1bb8a08a-2a06-4fad-8757-e8b4999d7a9a`
- **引用名**: `SmhDefaultSecurityClassCConfig`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `SmhSecurityClassCConfig`
- **完整路径**: `/MICROSAR/Smh/SmhVerification/SmhMonolithicVerification/SmhSecurityClassC/SmhSecurityClassCConfig`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Default monolythic verification for the security class C:
SecM_VerificationClassC

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. SmhSecurityClassCConfig

**容器属性**:

- **UUID**: `08f7a3a0-55c3-4440-bbad-8652231c1afc`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SmhSecurityClassCConfig`
- **多重性**: [1..infinite]
- **构建后可变**: false

**容器描述**:

Container to configure the monolythic verifications for security class C.

########## 参数配置

此容器包含 **4** 个参数：

########### INTEGER 类型参数

############ 1. SmhSignatureOffset

- **UUID**: `2e0853f6-5158-49bb-8a43-0ee955c15bff`
- **参数名**: `SmhSignatureOffset`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Specify the offset to the signature (MAC).

############ 2. SmhCRCOffset

- **UUID**: `9d9b2b54-743d-4914-a914-a375452a81c9`
- **参数名**: `SmhCRCOffset`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Specify the offset to the CRC value (used by CRC written)

########### BOOLEAN 类型参数

############ 1. SmhIncludeAddressAndLengthInSignature

- **UUID**: `e26fa671-08c7-466b-a1a7-de82db5c676c`
- **参数名**: `SmhIncludeAddressAndLengthInSignature`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Specify if the address and length of the segments shall be taken into account in the verification.

########### FUNCTION-NAME 类型参数

############ 1. SmhFunctionName

- **UUID**: `9bd34e8a-f73d-4e0a-9dc9-203ffa5b98ca`
- **参数名**: `SmhFunctionName`
- **数据类型**: FUNCTION-NAME
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Configure the function name to execute the monolythic verification, e.g.:
- SecM_VerificationClassC_HmacSha1
- SecM_VerificationClassC_Cmac

########## 引用关系

此容器包含 **2** 个引用：

########### REFERENCE 类型引用

############ 1. SmhStreamVerificationConfig

- **UUID**: `f7ef63f9-fff4-4b04-a90e-3cbdd667497e`
- **引用名**: `SmhStreamVerificationConfig`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `SmhSecurityClassCConfig`
- **完整路径**: `/MICROSAR/Smh/SmhVerification/SmhStreamVerification/SmhSecurityClassC/SmhSecurityClassCConfig`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Reference to the underlying StreamVerification to eecute the verification operation.

############ 2. SmhVendorVerificationConfig

- **UUID**: `901c9188-01b4-4c53-ac2d-0d0fb0a5359e`
- **引用名**: `SmhVendorVerificationConfig`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `SmhSecurityClassVendorConfig`
- **完整路径**: `/MICROSAR/Smh/SmhVerification/SmhStreamVerification/SmhSecurityClassVendor/SmhSecurityClassVendorConfig`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Reference to a VendorVerification to execute next to the MAC verification an additional vendor checksum.

####### 4. SmhSecurityClassCConfig

**容器属性**:

- **UUID**: `08f7a3a0-55c3-4440-bbad-8652231c1afc`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SmhSecurityClassCConfig`
- **多重性**: [1..infinite]
- **构建后可变**: false

**容器描述**:

Container to configure the monolythic verifications for security class C.

######## 参数配置

此容器包含 **4** 个参数：

######### INTEGER 类型参数

########## 1. SmhSignatureOffset

- **UUID**: `2e0853f6-5158-49bb-8a43-0ee955c15bff`
- **参数名**: `SmhSignatureOffset`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Specify the offset to the signature (MAC).

########## 2. SmhCRCOffset

- **UUID**: `9d9b2b54-743d-4914-a914-a375452a81c9`
- **参数名**: `SmhCRCOffset`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Specify the offset to the CRC value (used by CRC written)

######### BOOLEAN 类型参数

########## 1. SmhIncludeAddressAndLengthInSignature

- **UUID**: `e26fa671-08c7-466b-a1a7-de82db5c676c`
- **参数名**: `SmhIncludeAddressAndLengthInSignature`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Specify if the address and length of the segments shall be taken into account in the verification.

######### FUNCTION-NAME 类型参数

########## 1. SmhFunctionName

- **UUID**: `9bd34e8a-f73d-4e0a-9dc9-203ffa5b98ca`
- **参数名**: `SmhFunctionName`
- **数据类型**: FUNCTION-NAME
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Configure the function name to execute the monolythic verification, e.g.:
- SecM_VerificationClassC_HmacSha1
- SecM_VerificationClassC_Cmac

######## 引用关系

此容器包含 **2** 个引用：

######### REFERENCE 类型引用

########## 1. SmhStreamVerificationConfig

- **UUID**: `f7ef63f9-fff4-4b04-a90e-3cbdd667497e`
- **引用名**: `SmhStreamVerificationConfig`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `SmhSecurityClassCConfig`
- **完整路径**: `/MICROSAR/Smh/SmhVerification/SmhStreamVerification/SmhSecurityClassC/SmhSecurityClassCConfig`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Reference to the underlying StreamVerification to eecute the verification operation.

########## 2. SmhVendorVerificationConfig

- **UUID**: `901c9188-01b4-4c53-ac2d-0d0fb0a5359e`
- **引用名**: `SmhVendorVerificationConfig`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `SmhSecurityClassVendorConfig`
- **完整路径**: `/MICROSAR/Smh/SmhVerification/SmhStreamVerification/SmhSecurityClassVendor/SmhSecurityClassVendorConfig`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Reference to a VendorVerification to execute next to the MAC verification an additional vendor checksum.

####### 5. SmhSecurityClassCCC

**容器属性**:

- **UUID**: `4ab7b0b3-e998-4914-bdd3-8ba54bf23f77`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SmhSecurityClassCCC`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container to configure the monolythic verification for security class CCC.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. SmhDefaultSecurityClassCCCConfig

- **UUID**: `9da32213-c156-452a-82af-9db07b263858`
- **引用名**: `SmhDefaultSecurityClassCCCConfig`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `SmhSecurityClassCCCConfig`
- **完整路径**: `/MICROSAR/Smh/SmhVerification/SmhMonolithicVerification/SmhSecurityClassCCC/SmhSecurityClassCCCConfig`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Default monolythic verification for the security class CCC:
SecM_VerificationClassCCC

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. SmhSecurityClassCCCConfig

**容器属性**:

- **UUID**: `bb62362a-8553-4d60-a926-a0270adeb73f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SmhSecurityClassCCCConfig`
- **多重性**: [1..infinite]
- **构建后可变**: false

**容器描述**:

Container to configure the monolythic verifications for security class CCC.

########## 参数配置

此容器包含 **4** 个参数：

########### INTEGER 类型参数

############ 1. SmhSignatureOffset

- **UUID**: `8cb8417a-f4e7-4fd7-b389-73e568cbd189`
- **参数名**: `SmhSignatureOffset`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Specify the offset to the signature.

############ 2. SmhCRCOffset

- **UUID**: `00c2cec6-726b-4e53-b151-e8685d67c400`
- **参数名**: `SmhCRCOffset`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Specify the offset to the CRC value (used by CRC written)

########### BOOLEAN 类型参数

############ 1. SmhIncludeAddressAndLengthInSignature

- **UUID**: `97a43d7c-7ece-4506-946e-751f23cee541`
- **参数名**: `SmhIncludeAddressAndLengthInSignature`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Specify if the address and length of the segments shall be taken into account in the verification.

########### FUNCTION-NAME 类型参数

############ 1. SmhFunctionName

- **UUID**: `442fdcd9-13f7-4614-98c5-950f0ed8cee1`
- **参数名**: `SmhFunctionName`
- **数据类型**: FUNCTION-NAME
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Configure the function name to execute the monolythic verification, e.g.:
- SecM_VerificationClassCCC_RsaPssSha256
- SecM_VerificationClassCCC_Ed25519PH

########## 引用关系

此容器包含 **2** 个引用：

########### REFERENCE 类型引用

############ 1. SmhStreamVerificationConfig

- **UUID**: `d59861ca-8eba-456e-b4cf-b28f96b0d983`
- **引用名**: `SmhStreamVerificationConfig`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `SmhSecurityClassCCCConfig`
- **完整路径**: `/MICROSAR/Smh/SmhVerification/SmhStreamVerification/SmhSecurityClassCCC/SmhSecurityClassCCCConfig`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Reference to the underlying StreamVerification to eecute the verification operation.

############ 2. SmhVendorVerificationConfig

- **UUID**: `aae4bd8b-20f5-4871-96c6-f240fa3f4dc4`
- **引用名**: `SmhVendorVerificationConfig`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `SmhSecurityClassVendorConfig`
- **完整路径**: `/MICROSAR/Smh/SmhVerification/SmhStreamVerification/SmhSecurityClassVendor/SmhSecurityClassVendorConfig`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Reference to a VendorVerification to execute next to the signature verification an additional vendor checksum.

####### 6. SmhSecurityClassCCCConfig

**容器属性**:

- **UUID**: `bb62362a-8553-4d60-a926-a0270adeb73f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SmhSecurityClassCCCConfig`
- **多重性**: [1..infinite]
- **构建后可变**: false

**容器描述**:

Container to configure the monolythic verifications for security class CCC.

######## 参数配置

此容器包含 **4** 个参数：

######### INTEGER 类型参数

########## 1. SmhSignatureOffset

- **UUID**: `8cb8417a-f4e7-4fd7-b389-73e568cbd189`
- **参数名**: `SmhSignatureOffset`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Specify the offset to the signature.

########## 2. SmhCRCOffset

- **UUID**: `00c2cec6-726b-4e53-b151-e8685d67c400`
- **参数名**: `SmhCRCOffset`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Specify the offset to the CRC value (used by CRC written)

######### BOOLEAN 类型参数

########## 1. SmhIncludeAddressAndLengthInSignature

- **UUID**: `97a43d7c-7ece-4506-946e-751f23cee541`
- **参数名**: `SmhIncludeAddressAndLengthInSignature`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Specify if the address and length of the segments shall be taken into account in the verification.

######### FUNCTION-NAME 类型参数

########## 1. SmhFunctionName

- **UUID**: `442fdcd9-13f7-4614-98c5-950f0ed8cee1`
- **参数名**: `SmhFunctionName`
- **数据类型**: FUNCTION-NAME
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Configure the function name to execute the monolythic verification, e.g.:
- SecM_VerificationClassCCC_RsaPssSha256
- SecM_VerificationClassCCC_Ed25519PH

######## 引用关系

此容器包含 **2** 个引用：

######### REFERENCE 类型引用

########## 1. SmhStreamVerificationConfig

- **UUID**: `d59861ca-8eba-456e-b4cf-b28f96b0d983`
- **引用名**: `SmhStreamVerificationConfig`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `SmhSecurityClassCCCConfig`
- **完整路径**: `/MICROSAR/Smh/SmhVerification/SmhStreamVerification/SmhSecurityClassCCC/SmhSecurityClassCCCConfig`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Reference to the underlying StreamVerification to eecute the verification operation.

########## 2. SmhVendorVerificationConfig

- **UUID**: `aae4bd8b-20f5-4871-96c6-f240fa3f4dc4`
- **引用名**: `SmhVendorVerificationConfig`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `SmhSecurityClassVendorConfig`
- **完整路径**: `/MICROSAR/Smh/SmhVerification/SmhStreamVerification/SmhSecurityClassVendor/SmhSecurityClassVendorConfig`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Reference to a VendorVerification to execute next to the signature verification an additional vendor checksum.

####### 7. SmhSecurityClassVendor

**容器属性**:

- **UUID**: `023c1e00-aef3-45e5-8e62-e82c30453758`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SmhSecurityClassVendor`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container to configure the monolythic verification for security class Vendor.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. SmhDefaultSecurityClassVendorConfig

- **UUID**: `7fbeb646-9c86-4350-869c-617b0aeb7dc3`
- **引用名**: `SmhDefaultSecurityClassVendorConfig`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `SmhSecurityClassVendorConfig`
- **完整路径**: `/MICROSAR/Smh/SmhVerification/SmhMonolithicVerification/SmhSecurityClassVendor/SmhSecurityClassVendorConfig`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Default monolythic verification for the security class Vendor:
SecM_VerificationClassVendor

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. SmhSecurityClassVendorConfig

**容器属性**:

- **UUID**: `557f458f-7463-4adc-825b-7a4b4bea2cc4`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SmhSecurityClassVendorConfig`
- **多重性**: [1..infinite]
- **构建后可变**: false

**容器描述**:

Container to configure the monolythic verifications for security class Vendor.

########## 参数配置

此容器包含 **4** 个参数：

########### INTEGER 类型参数

############ 1. SmhSignatureOffset

- **UUID**: `7d727621-728d-44b0-a1df-a481f691ae4b`
- **参数名**: `SmhSignatureOffset`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Specify the offset to the signature.

############ 2. SmhCRCOffset

- **UUID**: `0a018b65-40c3-4884-ad4a-3db5d3bb1d87`
- **参数名**: `SmhCRCOffset`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Specify the offset to the CRC value (used by CRC written)

########### BOOLEAN 类型参数

############ 1. SmhIncludeAddressAndLengthInSignature

- **UUID**: `25259277-f94d-4f9a-8c3d-a537b7245aa9`
- **参数名**: `SmhIncludeAddressAndLengthInSignature`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Specify if the address and length of the segments shall be taken into account in the verification.

########### FUNCTION-NAME 类型参数

############ 1. SmhFunctionName

- **UUID**: `20e24252-7e8e-422d-add4-6ed7e3b75e4d`
- **参数名**: `SmhFunctionName`
- **数据类型**: FUNCTION-NAME
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Configure the function name to execute the monolythic verification.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. SmhStreamVerificationConfig

- **UUID**: `94eb1fc3-a08c-416c-9b41-9409ca135742`
- **引用名**: `SmhStreamVerificationConfig`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `SmhSecurityClassVendorConfig`
- **完整路径**: `/MICROSAR/Smh/SmhVerification/SmhStreamVerification/SmhSecurityClassVendor/SmhSecurityClassVendorConfig`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Reference to the underlying StreamVerification to eecute the verification operation.

####### 8. SmhSecurityClassVendorConfig

**容器属性**:

- **UUID**: `557f458f-7463-4adc-825b-7a4b4bea2cc4`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SmhSecurityClassVendorConfig`
- **多重性**: [1..infinite]
- **构建后可变**: false

**容器描述**:

Container to configure the monolythic verifications for security class Vendor.

######## 参数配置

此容器包含 **4** 个参数：

######### INTEGER 类型参数

########## 1. SmhSignatureOffset

- **UUID**: `7d727621-728d-44b0-a1df-a481f691ae4b`
- **参数名**: `SmhSignatureOffset`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Specify the offset to the signature.

########## 2. SmhCRCOffset

- **UUID**: `0a018b65-40c3-4884-ad4a-3db5d3bb1d87`
- **参数名**: `SmhCRCOffset`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Specify the offset to the CRC value (used by CRC written)

######### BOOLEAN 类型参数

########## 1. SmhIncludeAddressAndLengthInSignature

- **UUID**: `25259277-f94d-4f9a-8c3d-a537b7245aa9`
- **参数名**: `SmhIncludeAddressAndLengthInSignature`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Specify if the address and length of the segments shall be taken into account in the verification.

######### FUNCTION-NAME 类型参数

########## 1. SmhFunctionName

- **UUID**: `20e24252-7e8e-422d-add4-6ed7e3b75e4d`
- **参数名**: `SmhFunctionName`
- **数据类型**: FUNCTION-NAME
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Configure the function name to execute the monolythic verification.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. SmhStreamVerificationConfig

- **UUID**: `94eb1fc3-a08c-416c-9b41-9409ca135742`
- **引用名**: `SmhStreamVerificationConfig`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `SmhSecurityClassVendorConfig`
- **完整路径**: `/MICROSAR/Smh/SmhVerification/SmhStreamVerification/SmhSecurityClassVendor/SmhSecurityClassVendorConfig`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Reference to the underlying StreamVerification to eecute the verification operation.

##### 14. SmhSecurityClassDDD

**容器属性**:

- **UUID**: `72791700-82db-4ae8-913d-546993a59628`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SmhSecurityClassDDD`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container to configure the monolythic verification for security class DDD.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. SmhDefaultSecurityClassDDDConfig

- **UUID**: `8000ac6e-db98-4d89-ad2e-e5d407d6e2cf`
- **引用名**: `SmhDefaultSecurityClassDDDConfig`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `SmhSecurityClassDDDConfig`
- **完整路径**: `/MICROSAR/Smh/SmhVerification/SmhMonolithicVerification/SmhSecurityClassDDD/SmhSecurityClassDDDConfig`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Default monolythic verification for the security class DDD:
SecM_VerificationClassDDD

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. SmhSecurityClassDDDConfig

**容器属性**:

- **UUID**: `8b918e7c-9888-4c0f-ab87-064e3f447ed8`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SmhSecurityClassDDDConfig`
- **多重性**: [1..infinite]
- **构建后可变**: false

**容器描述**:

Container to configure the monolythic verifications for security class DDD.

######## 参数配置

此容器包含 **4** 个参数：

######### INTEGER 类型参数

########## 1. SmhSignatureOffset

- **UUID**: `058834c9-af5f-4982-885e-fbfd6a591f78`
- **参数名**: `SmhSignatureOffset`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Specify the offset to the signature (CRC or hash value).

########## 2. SmhCRCOffset

- **UUID**: `f9ad26cf-04f7-460c-bb94-5033c8c860a6`
- **参数名**: `SmhCRCOffset`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Specify the offset to the CRC value (used by CRC written)

######### BOOLEAN 类型参数

########## 1. SmhIncludeAddressAndLengthInSignature

- **UUID**: `db44bc4a-9cca-473b-896d-be630b6785e9`
- **参数名**: `SmhIncludeAddressAndLengthInSignature`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Specify if the address and length of the segments shall be taken into account in the verification.

######### FUNCTION-NAME 类型参数

########## 1. SmhFunctionName

- **UUID**: `ab733ae7-604b-4644-98db-a29bf0b8b00b`
- **参数名**: `SmhFunctionName`
- **数据类型**: FUNCTION-NAME
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Configure the function name to execute the monolythic verification, e.g.:
- SecM_VerificationClassDDD_Crc32
- SecM_VerificationClassDDD_Sha512

######## 引用关系

此容器包含 **2** 个引用：

######### REFERENCE 类型引用

########## 1. SmhStreamVerificationConfig

- **UUID**: `06866c75-743e-46f3-98cd-693b08a484a1`
- **引用名**: `SmhStreamVerificationConfig`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `SmhSecurityClassDDDConfig`
- **完整路径**: `/MICROSAR/Smh/SmhVerification/SmhStreamVerification/SmhSecurityClassDDD/SmhSecurityClassDDDConfig`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Reference to the underlying StreamVerification to eecute the verification operation.

########## 2. SmhVendorVerificationConfig

- **UUID**: `22a7ef68-050b-43d2-9efa-64b75baf9e7b`
- **引用名**: `SmhVendorVerificationConfig`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `SmhSecurityClassVendorConfig`
- **完整路径**: `/MICROSAR/Smh/SmhVerification/SmhStreamVerification/SmhSecurityClassVendor/SmhSecurityClassVendorConfig`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Reference to a VendorVerification to execute next to the CRC/hash verification an additional vendor checksum.

##### 15. SmhSecurityClassDDDConfig

**容器属性**:

- **UUID**: `8b918e7c-9888-4c0f-ab87-064e3f447ed8`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SmhSecurityClassDDDConfig`
- **多重性**: [1..infinite]
- **构建后可变**: false

**容器描述**:

Container to configure the monolythic verifications for security class DDD.

###### 参数配置

此容器包含 **4** 个参数：

####### INTEGER 类型参数

######## 1. SmhSignatureOffset

- **UUID**: `058834c9-af5f-4982-885e-fbfd6a591f78`
- **参数名**: `SmhSignatureOffset`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Specify the offset to the signature (CRC or hash value).

######## 2. SmhCRCOffset

- **UUID**: `f9ad26cf-04f7-460c-bb94-5033c8c860a6`
- **参数名**: `SmhCRCOffset`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Specify the offset to the CRC value (used by CRC written)

####### BOOLEAN 类型参数

######## 1. SmhIncludeAddressAndLengthInSignature

- **UUID**: `db44bc4a-9cca-473b-896d-be630b6785e9`
- **参数名**: `SmhIncludeAddressAndLengthInSignature`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Specify if the address and length of the segments shall be taken into account in the verification.

####### FUNCTION-NAME 类型参数

######## 1. SmhFunctionName

- **UUID**: `ab733ae7-604b-4644-98db-a29bf0b8b00b`
- **参数名**: `SmhFunctionName`
- **数据类型**: FUNCTION-NAME
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Configure the function name to execute the monolythic verification, e.g.:
- SecM_VerificationClassDDD_Crc32
- SecM_VerificationClassDDD_Sha512

###### 引用关系

此容器包含 **2** 个引用：

####### REFERENCE 类型引用

######## 1. SmhStreamVerificationConfig

- **UUID**: `06866c75-743e-46f3-98cd-693b08a484a1`
- **引用名**: `SmhStreamVerificationConfig`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `SmhSecurityClassDDDConfig`
- **完整路径**: `/MICROSAR/Smh/SmhVerification/SmhStreamVerification/SmhSecurityClassDDD/SmhSecurityClassDDDConfig`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Reference to the underlying StreamVerification to eecute the verification operation.

######## 2. SmhVendorVerificationConfig

- **UUID**: `22a7ef68-050b-43d2-9efa-64b75baf9e7b`
- **引用名**: `SmhVendorVerificationConfig`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `SmhSecurityClassVendorConfig`
- **完整路径**: `/MICROSAR/Smh/SmhVerification/SmhStreamVerification/SmhSecurityClassVendor/SmhSecurityClassVendorConfig`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Reference to a VendorVerification to execute next to the CRC/hash verification an additional vendor checksum.

##### 16. SmhSecurityClassC

**容器属性**:

- **UUID**: `9184de9d-b87a-4814-9987-c262b26ccff8`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SmhSecurityClassC`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container to configure the monolythic verification for security class C.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. SmhDefaultSecurityClassCConfig

- **UUID**: `1bb8a08a-2a06-4fad-8757-e8b4999d7a9a`
- **引用名**: `SmhDefaultSecurityClassCConfig`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `SmhSecurityClassCConfig`
- **完整路径**: `/MICROSAR/Smh/SmhVerification/SmhMonolithicVerification/SmhSecurityClassC/SmhSecurityClassCConfig`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Default monolythic verification for the security class C:
SecM_VerificationClassC

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. SmhSecurityClassCConfig

**容器属性**:

- **UUID**: `08f7a3a0-55c3-4440-bbad-8652231c1afc`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SmhSecurityClassCConfig`
- **多重性**: [1..infinite]
- **构建后可变**: false

**容器描述**:

Container to configure the monolythic verifications for security class C.

######## 参数配置

此容器包含 **4** 个参数：

######### INTEGER 类型参数

########## 1. SmhSignatureOffset

- **UUID**: `2e0853f6-5158-49bb-8a43-0ee955c15bff`
- **参数名**: `SmhSignatureOffset`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Specify the offset to the signature (MAC).

########## 2. SmhCRCOffset

- **UUID**: `9d9b2b54-743d-4914-a914-a375452a81c9`
- **参数名**: `SmhCRCOffset`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Specify the offset to the CRC value (used by CRC written)

######### BOOLEAN 类型参数

########## 1. SmhIncludeAddressAndLengthInSignature

- **UUID**: `e26fa671-08c7-466b-a1a7-de82db5c676c`
- **参数名**: `SmhIncludeAddressAndLengthInSignature`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Specify if the address and length of the segments shall be taken into account in the verification.

######### FUNCTION-NAME 类型参数

########## 1. SmhFunctionName

- **UUID**: `9bd34e8a-f73d-4e0a-9dc9-203ffa5b98ca`
- **参数名**: `SmhFunctionName`
- **数据类型**: FUNCTION-NAME
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Configure the function name to execute the monolythic verification, e.g.:
- SecM_VerificationClassC_HmacSha1
- SecM_VerificationClassC_Cmac

######## 引用关系

此容器包含 **2** 个引用：

######### REFERENCE 类型引用

########## 1. SmhStreamVerificationConfig

- **UUID**: `f7ef63f9-fff4-4b04-a90e-3cbdd667497e`
- **引用名**: `SmhStreamVerificationConfig`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `SmhSecurityClassCConfig`
- **完整路径**: `/MICROSAR/Smh/SmhVerification/SmhStreamVerification/SmhSecurityClassC/SmhSecurityClassCConfig`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Reference to the underlying StreamVerification to eecute the verification operation.

########## 2. SmhVendorVerificationConfig

- **UUID**: `901c9188-01b4-4c53-ac2d-0d0fb0a5359e`
- **引用名**: `SmhVendorVerificationConfig`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `SmhSecurityClassVendorConfig`
- **完整路径**: `/MICROSAR/Smh/SmhVerification/SmhStreamVerification/SmhSecurityClassVendor/SmhSecurityClassVendorConfig`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Reference to a VendorVerification to execute next to the MAC verification an additional vendor checksum.

##### 17. SmhSecurityClassCConfig

**容器属性**:

- **UUID**: `08f7a3a0-55c3-4440-bbad-8652231c1afc`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SmhSecurityClassCConfig`
- **多重性**: [1..infinite]
- **构建后可变**: false

**容器描述**:

Container to configure the monolythic verifications for security class C.

###### 参数配置

此容器包含 **4** 个参数：

####### INTEGER 类型参数

######## 1. SmhSignatureOffset

- **UUID**: `2e0853f6-5158-49bb-8a43-0ee955c15bff`
- **参数名**: `SmhSignatureOffset`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Specify the offset to the signature (MAC).

######## 2. SmhCRCOffset

- **UUID**: `9d9b2b54-743d-4914-a914-a375452a81c9`
- **参数名**: `SmhCRCOffset`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Specify the offset to the CRC value (used by CRC written)

####### BOOLEAN 类型参数

######## 1. SmhIncludeAddressAndLengthInSignature

- **UUID**: `e26fa671-08c7-466b-a1a7-de82db5c676c`
- **参数名**: `SmhIncludeAddressAndLengthInSignature`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Specify if the address and length of the segments shall be taken into account in the verification.

####### FUNCTION-NAME 类型参数

######## 1. SmhFunctionName

- **UUID**: `9bd34e8a-f73d-4e0a-9dc9-203ffa5b98ca`
- **参数名**: `SmhFunctionName`
- **数据类型**: FUNCTION-NAME
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Configure the function name to execute the monolythic verification, e.g.:
- SecM_VerificationClassC_HmacSha1
- SecM_VerificationClassC_Cmac

###### 引用关系

此容器包含 **2** 个引用：

####### REFERENCE 类型引用

######## 1. SmhStreamVerificationConfig

- **UUID**: `f7ef63f9-fff4-4b04-a90e-3cbdd667497e`
- **引用名**: `SmhStreamVerificationConfig`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `SmhSecurityClassCConfig`
- **完整路径**: `/MICROSAR/Smh/SmhVerification/SmhStreamVerification/SmhSecurityClassC/SmhSecurityClassCConfig`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Reference to the underlying StreamVerification to eecute the verification operation.

######## 2. SmhVendorVerificationConfig

- **UUID**: `901c9188-01b4-4c53-ac2d-0d0fb0a5359e`
- **引用名**: `SmhVendorVerificationConfig`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `SmhSecurityClassVendorConfig`
- **完整路径**: `/MICROSAR/Smh/SmhVerification/SmhStreamVerification/SmhSecurityClassVendor/SmhSecurityClassVendorConfig`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Reference to a VendorVerification to execute next to the MAC verification an additional vendor checksum.

##### 18. SmhSecurityClassCCC

**容器属性**:

- **UUID**: `4ab7b0b3-e998-4914-bdd3-8ba54bf23f77`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SmhSecurityClassCCC`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container to configure the monolythic verification for security class CCC.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. SmhDefaultSecurityClassCCCConfig

- **UUID**: `9da32213-c156-452a-82af-9db07b263858`
- **引用名**: `SmhDefaultSecurityClassCCCConfig`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `SmhSecurityClassCCCConfig`
- **完整路径**: `/MICROSAR/Smh/SmhVerification/SmhMonolithicVerification/SmhSecurityClassCCC/SmhSecurityClassCCCConfig`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Default monolythic verification for the security class CCC:
SecM_VerificationClassCCC

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. SmhSecurityClassCCCConfig

**容器属性**:

- **UUID**: `bb62362a-8553-4d60-a926-a0270adeb73f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SmhSecurityClassCCCConfig`
- **多重性**: [1..infinite]
- **构建后可变**: false

**容器描述**:

Container to configure the monolythic verifications for security class CCC.

######## 参数配置

此容器包含 **4** 个参数：

######### INTEGER 类型参数

########## 1. SmhSignatureOffset

- **UUID**: `8cb8417a-f4e7-4fd7-b389-73e568cbd189`
- **参数名**: `SmhSignatureOffset`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Specify the offset to the signature.

########## 2. SmhCRCOffset

- **UUID**: `00c2cec6-726b-4e53-b151-e8685d67c400`
- **参数名**: `SmhCRCOffset`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Specify the offset to the CRC value (used by CRC written)

######### BOOLEAN 类型参数

########## 1. SmhIncludeAddressAndLengthInSignature

- **UUID**: `97a43d7c-7ece-4506-946e-751f23cee541`
- **参数名**: `SmhIncludeAddressAndLengthInSignature`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Specify if the address and length of the segments shall be taken into account in the verification.

######### FUNCTION-NAME 类型参数

########## 1. SmhFunctionName

- **UUID**: `442fdcd9-13f7-4614-98c5-950f0ed8cee1`
- **参数名**: `SmhFunctionName`
- **数据类型**: FUNCTION-NAME
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Configure the function name to execute the monolythic verification, e.g.:
- SecM_VerificationClassCCC_RsaPssSha256
- SecM_VerificationClassCCC_Ed25519PH

######## 引用关系

此容器包含 **2** 个引用：

######### REFERENCE 类型引用

########## 1. SmhStreamVerificationConfig

- **UUID**: `d59861ca-8eba-456e-b4cf-b28f96b0d983`
- **引用名**: `SmhStreamVerificationConfig`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `SmhSecurityClassCCCConfig`
- **完整路径**: `/MICROSAR/Smh/SmhVerification/SmhStreamVerification/SmhSecurityClassCCC/SmhSecurityClassCCCConfig`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Reference to the underlying StreamVerification to eecute the verification operation.

########## 2. SmhVendorVerificationConfig

- **UUID**: `aae4bd8b-20f5-4871-96c6-f240fa3f4dc4`
- **引用名**: `SmhVendorVerificationConfig`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `SmhSecurityClassVendorConfig`
- **完整路径**: `/MICROSAR/Smh/SmhVerification/SmhStreamVerification/SmhSecurityClassVendor/SmhSecurityClassVendorConfig`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Reference to a VendorVerification to execute next to the signature verification an additional vendor checksum.

##### 19. SmhSecurityClassCCCConfig

**容器属性**:

- **UUID**: `bb62362a-8553-4d60-a926-a0270adeb73f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SmhSecurityClassCCCConfig`
- **多重性**: [1..infinite]
- **构建后可变**: false

**容器描述**:

Container to configure the monolythic verifications for security class CCC.

###### 参数配置

此容器包含 **4** 个参数：

####### INTEGER 类型参数

######## 1. SmhSignatureOffset

- **UUID**: `8cb8417a-f4e7-4fd7-b389-73e568cbd189`
- **参数名**: `SmhSignatureOffset`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Specify the offset to the signature.

######## 2. SmhCRCOffset

- **UUID**: `00c2cec6-726b-4e53-b151-e8685d67c400`
- **参数名**: `SmhCRCOffset`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Specify the offset to the CRC value (used by CRC written)

####### BOOLEAN 类型参数

######## 1. SmhIncludeAddressAndLengthInSignature

- **UUID**: `97a43d7c-7ece-4506-946e-751f23cee541`
- **参数名**: `SmhIncludeAddressAndLengthInSignature`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Specify if the address and length of the segments shall be taken into account in the verification.

####### FUNCTION-NAME 类型参数

######## 1. SmhFunctionName

- **UUID**: `442fdcd9-13f7-4614-98c5-950f0ed8cee1`
- **参数名**: `SmhFunctionName`
- **数据类型**: FUNCTION-NAME
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Configure the function name to execute the monolythic verification, e.g.:
- SecM_VerificationClassCCC_RsaPssSha256
- SecM_VerificationClassCCC_Ed25519PH

###### 引用关系

此容器包含 **2** 个引用：

####### REFERENCE 类型引用

######## 1. SmhStreamVerificationConfig

- **UUID**: `d59861ca-8eba-456e-b4cf-b28f96b0d983`
- **引用名**: `SmhStreamVerificationConfig`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `SmhSecurityClassCCCConfig`
- **完整路径**: `/MICROSAR/Smh/SmhVerification/SmhStreamVerification/SmhSecurityClassCCC/SmhSecurityClassCCCConfig`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Reference to the underlying StreamVerification to eecute the verification operation.

######## 2. SmhVendorVerificationConfig

- **UUID**: `aae4bd8b-20f5-4871-96c6-f240fa3f4dc4`
- **引用名**: `SmhVendorVerificationConfig`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `SmhSecurityClassVendorConfig`
- **完整路径**: `/MICROSAR/Smh/SmhVerification/SmhStreamVerification/SmhSecurityClassVendor/SmhSecurityClassVendorConfig`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Reference to a VendorVerification to execute next to the signature verification an additional vendor checksum.

##### 20. SmhSecurityClassVendor

**容器属性**:

- **UUID**: `023c1e00-aef3-45e5-8e62-e82c30453758`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SmhSecurityClassVendor`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container to configure the monolythic verification for security class Vendor.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. SmhDefaultSecurityClassVendorConfig

- **UUID**: `7fbeb646-9c86-4350-869c-617b0aeb7dc3`
- **引用名**: `SmhDefaultSecurityClassVendorConfig`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `SmhSecurityClassVendorConfig`
- **完整路径**: `/MICROSAR/Smh/SmhVerification/SmhMonolithicVerification/SmhSecurityClassVendor/SmhSecurityClassVendorConfig`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Default monolythic verification for the security class Vendor:
SecM_VerificationClassVendor

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. SmhSecurityClassVendorConfig

**容器属性**:

- **UUID**: `557f458f-7463-4adc-825b-7a4b4bea2cc4`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SmhSecurityClassVendorConfig`
- **多重性**: [1..infinite]
- **构建后可变**: false

**容器描述**:

Container to configure the monolythic verifications for security class Vendor.

######## 参数配置

此容器包含 **4** 个参数：

######### INTEGER 类型参数

########## 1. SmhSignatureOffset

- **UUID**: `7d727621-728d-44b0-a1df-a481f691ae4b`
- **参数名**: `SmhSignatureOffset`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Specify the offset to the signature.

########## 2. SmhCRCOffset

- **UUID**: `0a018b65-40c3-4884-ad4a-3db5d3bb1d87`
- **参数名**: `SmhCRCOffset`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Specify the offset to the CRC value (used by CRC written)

######### BOOLEAN 类型参数

########## 1. SmhIncludeAddressAndLengthInSignature

- **UUID**: `25259277-f94d-4f9a-8c3d-a537b7245aa9`
- **参数名**: `SmhIncludeAddressAndLengthInSignature`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Specify if the address and length of the segments shall be taken into account in the verification.

######### FUNCTION-NAME 类型参数

########## 1. SmhFunctionName

- **UUID**: `20e24252-7e8e-422d-add4-6ed7e3b75e4d`
- **参数名**: `SmhFunctionName`
- **数据类型**: FUNCTION-NAME
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Configure the function name to execute the monolythic verification.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. SmhStreamVerificationConfig

- **UUID**: `94eb1fc3-a08c-416c-9b41-9409ca135742`
- **引用名**: `SmhStreamVerificationConfig`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `SmhSecurityClassVendorConfig`
- **完整路径**: `/MICROSAR/Smh/SmhVerification/SmhStreamVerification/SmhSecurityClassVendor/SmhSecurityClassVendorConfig`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Reference to the underlying StreamVerification to eecute the verification operation.

##### 21. SmhSecurityClassVendorConfig

**容器属性**:

- **UUID**: `557f458f-7463-4adc-825b-7a4b4bea2cc4`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SmhSecurityClassVendorConfig`
- **多重性**: [1..infinite]
- **构建后可变**: false

**容器描述**:

Container to configure the monolythic verifications for security class Vendor.

###### 参数配置

此容器包含 **4** 个参数：

####### INTEGER 类型参数

######## 1. SmhSignatureOffset

- **UUID**: `7d727621-728d-44b0-a1df-a481f691ae4b`
- **参数名**: `SmhSignatureOffset`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Specify the offset to the signature.

######## 2. SmhCRCOffset

- **UUID**: `0a018b65-40c3-4884-ad4a-3db5d3bb1d87`
- **参数名**: `SmhCRCOffset`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Specify the offset to the CRC value (used by CRC written)

####### BOOLEAN 类型参数

######## 1. SmhIncludeAddressAndLengthInSignature

- **UUID**: `25259277-f94d-4f9a-8c3d-a537b7245aa9`
- **参数名**: `SmhIncludeAddressAndLengthInSignature`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Specify if the address and length of the segments shall be taken into account in the verification.

####### FUNCTION-NAME 类型参数

######## 1. SmhFunctionName

- **UUID**: `20e24252-7e8e-422d-add4-6ed7e3b75e4d`
- **参数名**: `SmhFunctionName`
- **数据类型**: FUNCTION-NAME
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Configure the function name to execute the monolythic verification.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. SmhStreamVerificationConfig

- **UUID**: `94eb1fc3-a08c-416c-9b41-9409ca135742`
- **引用名**: `SmhStreamVerificationConfig`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `SmhSecurityClassVendorConfig`
- **完整路径**: `/MICROSAR/Smh/SmhVerification/SmhStreamVerification/SmhSecurityClassVendor/SmhSecurityClassVendorConfig`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Reference to the underlying StreamVerification to eecute the verification operation.

##### 22. SmhStreamVerification

**容器属性**:

- **UUID**: `3c39b3ca-3331-4d94-b73e-40528c7afacc`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SmhStreamVerification`
- **多重性**: [1..1]
- **构建后可变**: false

**容器描述**:

Container to configure the stream verifications.
Stream verifications are used to verify the data during the download (InputVerification, ProcessedVerification and PipelinedVerification).

###### 引用关系

此容器包含 **1** 个引用：

####### CHOICE-REFERENCE 类型引用

######## 1. SmhDefaultStreamVerificationConfig

- **UUID**: `c2da39ea-e323-4668-ab9f-6acfa5c53ef3`
- **引用名**: `SmhDefaultStreamVerificationConfig`
- **引用类型**: CHOICE-REFERENCE
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **需要索引**: false
- **目标引用列表**:
  - `/MICROSAR/Smh/SmhVerification/SmhStreamVerification/SmhSecurityClassDDD/SmhSecurityClassDDDConfig`
  - `/MICROSAR/Smh/SmhVerification/SmhStreamVerification/SmhSecurityClassC/SmhSecurityClassCConfig`
  - `/MICROSAR/Smh/SmhVerification/SmhStreamVerification/SmhSecurityClassCCC/SmhSecurityClassCCCConfig`
  - `/MICROSAR/Smh/SmhVerification/SmhStreamVerification/SmhSecurityClassVendor/SmhSecurityClassVendorConfig`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Default stream verification:
SecM_VerifySignature

###### 配置容器

本模块包含 **12** 个配置容器：

####### 1. SmhSecurityClassDDD

**容器属性**:

- **UUID**: `f65076e1-6a4f-4afd-8f21-e8faea37fe6d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SmhSecurityClassDDD`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container to configure the stream verification for security class DDD.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. SmhDefaultSecurityClassDDDConfig

- **UUID**: `46906c73-00d0-4ce1-83bd-dd5f4112a3d8`
- **引用名**: `SmhDefaultSecurityClassDDDConfig`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `SmhSecurityClassDDDConfig`
- **完整路径**: `/MICROSAR/Smh/SmhVerification/SmhStreamVerification/SmhSecurityClassDDD/SmhSecurityClassDDDConfig`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Default stream verification for the security class DDD:
SecM_VerifyClassDDD

######## 配置容器

本模块包含 **4** 个配置容器：

######### 1. SmhSecurityClassDDDConfig

**容器属性**:

- **UUID**: `9edb72f4-2681-4d78-b583-25881036d326`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SmhSecurityClassDDDConfig`
- **多重性**: [1..infinite]
- **构建后可变**: false

**容器描述**:

Container to configure the stream verifications for security class DDD.

########## 参数配置

此容器包含 **3** 个参数：

########### BOOLEAN 类型参数

############ 1. SmhUpdateLengthOfHashedData

- **UUID**: `d4134277-9064-464b-a0e2-444e36fc56bc`
- **参数名**: `SmhUpdateLengthOfHashedData`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: If enabled, the security module will update the current length of hashed data in SecM_SignatureParamtype::currentDataLength.

############ 2. SmhComputationOnly

- **UUID**: `a77c5004-72b2-4e59-aee2-025769278b81`
- **参数名**: `SmhComputationOnly`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: If enabled the security module will just compute the CRC/hash without verifying it. The computed CRC/hash is provided via SecM_SignatureParamtype::sigSourceBuffer.

########### FUNCTION-NAME 类型参数

############ 1. SmhFunctionName

- **UUID**: `262ace43-2c7c-4462-9763-63cfd27ebe48`
- **参数名**: `SmhFunctionName`
- **数据类型**: FUNCTION-NAME
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Configure the function name of the stream verification, e.g.:
- SecM_VerifyCrc32
- SecM_VerifyHashSha512

########## 配置容器

本模块包含 **3** 个配置容器：

########### 1. SmhCrc

**容器属性**:

- **UUID**: `d77a32e4-ca21-4c5c-a0ec-75a6fae134fe`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SmhCrc`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container to configure the CRC

############ 引用关系

此容器包含 **1** 个引用：

############# CHOICE-REFERENCE 类型引用

############## 1. SmhCrcRef

- **UUID**: `545924b6-97cc-4283-9bee-5159bda168f9`
- **引用名**: `SmhCrcRef`
- **引用类型**: CHOICE-REFERENCE
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **需要索引**: false
- **目标引用列表**:
  - `/MICROSAR/Smh/SmhCrc/SmhCrc16`
  - `/MICROSAR/Smh/SmhCrc/SmhCrc32`
  - `/MICROSAR/Smh/SmhCrc/SmhCrc64`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: References a CRC configuration, which shall be used by this stream verification.

########### 2. SmhHash

**容器属性**:

- **UUID**: `860c29ac-feed-4843-be72-6b659b349d99`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SmhHash`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container to configure the hash

############ 引用关系

此容器包含 **1** 个引用：

############# REFERENCE 类型引用

############## 1. SmhJobRef

- **UUID**: `935a56dc-ff73-4f9e-9090-032d0f6d04cb`
- **引用名**: `SmhJobRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `SmhJob`
- **完整路径**: `/MICROSAR/Smh/SmhJob`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: References a SmhHash job, which shall be used by this stream verification.

########### 3. SmhSecurityClassDDDType

**容器属性**:

- **UUID**: `d4091ae3-bc5f-49ed-aab5-4f51d555f432`
- **容器类型**: CHOICE-CONTAINER
- **容器名称**: `SmhSecurityClassDDDType`
- **多重性**: [1..1]
- **构建后可变**: false

**容器选择**:

- **SmhCrc**
  - UUID: `d77a32e4-ca21-4c5c-a0ec-75a6fae134fe`
  - 描述: Container to configure the CRC
- **SmhHash**
  - UUID: `860c29ac-feed-4843-be72-6b659b349d99`
  - 描述: Container to configure the hash

**容器描述**:

Specify the type of the security class DDD

######### 2. SmhCrc

**容器属性**:

- **UUID**: `d77a32e4-ca21-4c5c-a0ec-75a6fae134fe`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SmhCrc`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container to configure the CRC

########## 引用关系

此容器包含 **1** 个引用：

########### CHOICE-REFERENCE 类型引用

############ 1. SmhCrcRef

- **UUID**: `545924b6-97cc-4283-9bee-5159bda168f9`
- **引用名**: `SmhCrcRef`
- **引用类型**: CHOICE-REFERENCE
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **需要索引**: false
- **目标引用列表**:
  - `/MICROSAR/Smh/SmhCrc/SmhCrc16`
  - `/MICROSAR/Smh/SmhCrc/SmhCrc32`
  - `/MICROSAR/Smh/SmhCrc/SmhCrc64`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: References a CRC configuration, which shall be used by this stream verification.

######### 3. SmhHash

**容器属性**:

- **UUID**: `860c29ac-feed-4843-be72-6b659b349d99`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SmhHash`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container to configure the hash

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. SmhJobRef

- **UUID**: `935a56dc-ff73-4f9e-9090-032d0f6d04cb`
- **引用名**: `SmhJobRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `SmhJob`
- **完整路径**: `/MICROSAR/Smh/SmhJob`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: References a SmhHash job, which shall be used by this stream verification.

######### 4. SmhSecurityClassDDDType

**容器属性**:

- **UUID**: `d4091ae3-bc5f-49ed-aab5-4f51d555f432`
- **容器类型**: CHOICE-CONTAINER
- **容器名称**: `SmhSecurityClassDDDType`
- **多重性**: [1..1]
- **构建后可变**: false

**容器选择**:

- **SmhCrc**
  - UUID: `d77a32e4-ca21-4c5c-a0ec-75a6fae134fe`
  - 描述: Container to configure the CRC
- **SmhHash**
  - UUID: `860c29ac-feed-4843-be72-6b659b349d99`
  - 描述: Container to configure the hash

**容器描述**:

Specify the type of the security class DDD

####### 2. SmhSecurityClassDDDConfig

**容器属性**:

- **UUID**: `9edb72f4-2681-4d78-b583-25881036d326`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SmhSecurityClassDDDConfig`
- **多重性**: [1..infinite]
- **构建后可变**: false

**容器描述**:

Container to configure the stream verifications for security class DDD.

######## 参数配置

此容器包含 **3** 个参数：

######### BOOLEAN 类型参数

########## 1. SmhUpdateLengthOfHashedData

- **UUID**: `d4134277-9064-464b-a0e2-444e36fc56bc`
- **参数名**: `SmhUpdateLengthOfHashedData`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: If enabled, the security module will update the current length of hashed data in SecM_SignatureParamtype::currentDataLength.

########## 2. SmhComputationOnly

- **UUID**: `a77c5004-72b2-4e59-aee2-025769278b81`
- **参数名**: `SmhComputationOnly`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: If enabled the security module will just compute the CRC/hash without verifying it. The computed CRC/hash is provided via SecM_SignatureParamtype::sigSourceBuffer.

######### FUNCTION-NAME 类型参数

########## 1. SmhFunctionName

- **UUID**: `262ace43-2c7c-4462-9763-63cfd27ebe48`
- **参数名**: `SmhFunctionName`
- **数据类型**: FUNCTION-NAME
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Configure the function name of the stream verification, e.g.:
- SecM_VerifyCrc32
- SecM_VerifyHashSha512

######## 配置容器

本模块包含 **3** 个配置容器：

######### 1. SmhCrc

**容器属性**:

- **UUID**: `d77a32e4-ca21-4c5c-a0ec-75a6fae134fe`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SmhCrc`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container to configure the CRC

########## 引用关系

此容器包含 **1** 个引用：

########### CHOICE-REFERENCE 类型引用

############ 1. SmhCrcRef

- **UUID**: `545924b6-97cc-4283-9bee-5159bda168f9`
- **引用名**: `SmhCrcRef`
- **引用类型**: CHOICE-REFERENCE
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **需要索引**: false
- **目标引用列表**:
  - `/MICROSAR/Smh/SmhCrc/SmhCrc16`
  - `/MICROSAR/Smh/SmhCrc/SmhCrc32`
  - `/MICROSAR/Smh/SmhCrc/SmhCrc64`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: References a CRC configuration, which shall be used by this stream verification.

######### 2. SmhHash

**容器属性**:

- **UUID**: `860c29ac-feed-4843-be72-6b659b349d99`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SmhHash`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container to configure the hash

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. SmhJobRef

- **UUID**: `935a56dc-ff73-4f9e-9090-032d0f6d04cb`
- **引用名**: `SmhJobRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `SmhJob`
- **完整路径**: `/MICROSAR/Smh/SmhJob`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: References a SmhHash job, which shall be used by this stream verification.

######### 3. SmhSecurityClassDDDType

**容器属性**:

- **UUID**: `d4091ae3-bc5f-49ed-aab5-4f51d555f432`
- **容器类型**: CHOICE-CONTAINER
- **容器名称**: `SmhSecurityClassDDDType`
- **多重性**: [1..1]
- **构建后可变**: false

**容器选择**:

- **SmhCrc**
  - UUID: `d77a32e4-ca21-4c5c-a0ec-75a6fae134fe`
  - 描述: Container to configure the CRC
- **SmhHash**
  - UUID: `860c29ac-feed-4843-be72-6b659b349d99`
  - 描述: Container to configure the hash

**容器描述**:

Specify the type of the security class DDD

####### 3. SmhCrc

**容器属性**:

- **UUID**: `d77a32e4-ca21-4c5c-a0ec-75a6fae134fe`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SmhCrc`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container to configure the CRC

######## 引用关系

此容器包含 **1** 个引用：

######### CHOICE-REFERENCE 类型引用

########## 1. SmhCrcRef

- **UUID**: `545924b6-97cc-4283-9bee-5159bda168f9`
- **引用名**: `SmhCrcRef`
- **引用类型**: CHOICE-REFERENCE
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **需要索引**: false
- **目标引用列表**:
  - `/MICROSAR/Smh/SmhCrc/SmhCrc16`
  - `/MICROSAR/Smh/SmhCrc/SmhCrc32`
  - `/MICROSAR/Smh/SmhCrc/SmhCrc64`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: References a CRC configuration, which shall be used by this stream verification.

####### 4. SmhHash

**容器属性**:

- **UUID**: `860c29ac-feed-4843-be72-6b659b349d99`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SmhHash`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container to configure the hash

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. SmhJobRef

- **UUID**: `935a56dc-ff73-4f9e-9090-032d0f6d04cb`
- **引用名**: `SmhJobRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `SmhJob`
- **完整路径**: `/MICROSAR/Smh/SmhJob`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: References a SmhHash job, which shall be used by this stream verification.

####### 5. SmhSecurityClassC

**容器属性**:

- **UUID**: `0bbafb93-8d89-4aa2-a917-76ff0cc0016a`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SmhSecurityClassC`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container to configure the stream verification for security class C.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. SmhDefaultSecurityClassCConfig

- **UUID**: `29bb2998-5a48-4047-9169-d03556cff09d`
- **引用名**: `SmhDefaultSecurityClassCConfig`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `SmhSecurityClassCConfig`
- **完整路径**: `/MICROSAR/Smh/SmhVerification/SmhStreamVerification/SmhSecurityClassC/SmhSecurityClassCConfig`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Default stream verification for the security class C:
SecM_VerifyClassC

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. SmhSecurityClassCConfig

**容器属性**:

- **UUID**: `db313d05-7ad6-453b-bc32-372ecc4c5ec4`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SmhSecurityClassCConfig`
- **多重性**: [1..infinite]
- **构建后可变**: false

**容器描述**:

Container to configure the stream verifications for security class C.

########## 参数配置

此容器包含 **3** 个参数：

########### BOOLEAN 类型参数

############ 1. SmhUpdateLengthOfHashedData

- **UUID**: `1e161cb2-0f71-4990-8d7a-84f8f1fbf05c`
- **参数名**: `SmhUpdateLengthOfHashedData`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: If enabled, the security module will update the current length of hashed data in SecM_SignatureParamtype::currentDataLength.

############ 2. SmhComputationOnly

- **UUID**: `ca7644f1-ecc0-46b1-b73f-f926b42df198`
- **参数名**: `SmhComputationOnly`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: If enabled the security module will just compute the MAC without verifying it. The computed MAC is provided via SecM_SignatureParamtype::sigSourceBuffer.

########### FUNCTION-NAME 类型参数

############ 1. SmhFunctionName

- **UUID**: `c9a732c4-3d9b-4838-a3ed-c21f7878e3c5`
- **参数名**: `SmhFunctionName`
- **数据类型**: FUNCTION-NAME
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Configure the function name of the stream verification, e.g.:
- SecM_VerifyMacHmacSha1
- SecM_VerifyMacCmac

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. SmhJobRef

- **UUID**: `4443273c-b72e-4faa-ae72-41ee1d2fe23c`
- **引用名**: `SmhJobRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `SmhJob`
- **完整路径**: `/MICROSAR/Smh/SmhJob`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: References a SmhMacVerify or SmhMacGenerate job, which shall be used by this stream verification.

####### 6. SmhSecurityClassCConfig

**容器属性**:

- **UUID**: `db313d05-7ad6-453b-bc32-372ecc4c5ec4`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SmhSecurityClassCConfig`
- **多重性**: [1..infinite]
- **构建后可变**: false

**容器描述**:

Container to configure the stream verifications for security class C.

######## 参数配置

此容器包含 **3** 个参数：

######### BOOLEAN 类型参数

########## 1. SmhUpdateLengthOfHashedData

- **UUID**: `1e161cb2-0f71-4990-8d7a-84f8f1fbf05c`
- **参数名**: `SmhUpdateLengthOfHashedData`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: If enabled, the security module will update the current length of hashed data in SecM_SignatureParamtype::currentDataLength.

########## 2. SmhComputationOnly

- **UUID**: `ca7644f1-ecc0-46b1-b73f-f926b42df198`
- **参数名**: `SmhComputationOnly`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: If enabled the security module will just compute the MAC without verifying it. The computed MAC is provided via SecM_SignatureParamtype::sigSourceBuffer.

######### FUNCTION-NAME 类型参数

########## 1. SmhFunctionName

- **UUID**: `c9a732c4-3d9b-4838-a3ed-c21f7878e3c5`
- **参数名**: `SmhFunctionName`
- **数据类型**: FUNCTION-NAME
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Configure the function name of the stream verification, e.g.:
- SecM_VerifyMacHmacSha1
- SecM_VerifyMacCmac

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. SmhJobRef

- **UUID**: `4443273c-b72e-4faa-ae72-41ee1d2fe23c`
- **引用名**: `SmhJobRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `SmhJob`
- **完整路径**: `/MICROSAR/Smh/SmhJob`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: References a SmhMacVerify or SmhMacGenerate job, which shall be used by this stream verification.

####### 7. SmhSecurityClassCCC

**容器属性**:

- **UUID**: `e8bb9b83-5292-4b97-9d4e-6f37ada0a6c1`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SmhSecurityClassCCC`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container to configure the stream verification for security class CCC.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. SmhDefaultSecurityClassCCCConfig

- **UUID**: `0442501f-54c8-4df8-a5a1-c1a5f7de1398`
- **引用名**: `SmhDefaultSecurityClassCCCConfig`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `SmhSecurityClassCCCConfig`
- **完整路径**: `/MICROSAR/Smh/SmhVerification/SmhStreamVerification/SmhSecurityClassCCC/SmhSecurityClassCCCConfig`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Default stream verification for the security class CCC:
SecM_VerifyClassCCC

######## 配置容器

本模块包含 **2** 个配置容器：

######### 1. SmhSecurityClassCCCConfig

**容器属性**:

- **UUID**: `664dcb07-95ff-4179-8d6e-6ef8f5b49b46`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SmhSecurityClassCCCConfig`
- **多重性**: [1..infinite]
- **构建后可变**: false

**容器描述**:

Container to configure the stream verifications for security class CCC.

########## 参数配置

此容器包含 **2** 个参数：

########### BOOLEAN 类型参数

############ 1. SmhUpdateLengthOfHashedData

- **UUID**: `eec6e339-e8e3-44fa-b123-4e6a0eb5f1f0`
- **参数名**: `SmhUpdateLengthOfHashedData`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: If enabled, the security module will update the current length of hashed data in SecM_SignatureParamtype::currentDataLength.

########### FUNCTION-NAME 类型参数

############ 1. SmhFunctionName

- **UUID**: `2ea862e4-436b-42bd-9762-5fcc32430434`
- **参数名**: `SmhFunctionName`
- **数据类型**: FUNCTION-NAME
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Configure the function name of the stream verification, e.g.:
- SecM_VerifySigRsaPssSha256
- SecM_VerifySigEd25519PH

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. SmhJobRef

- **UUID**: `d60da727-ed84-438f-b298-500fde867ab8`
- **引用名**: `SmhJobRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `SmhJob`
- **完整路径**: `/MICROSAR/Smh/SmhJob`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: References a SmhSignatureVerify job, which shall be used by this stream verification.

########## 配置容器

本模块包含 **1** 个配置容器：

########### 1. SmhDiscretHashConfig

**容器属性**:

- **UUID**: `4e51524b-a403-48b3-9ada-c1942ae9616f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SmhDiscretHashConfig`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Configure a discrete hash for the verification, which is used to calculate a hash before verifying the signature.

############ 引用关系

此容器包含 **1** 个引用：

############# REFERENCE 类型引用

############## 1. SmhJobRef

- **UUID**: `51d9a895-6b6e-4e9f-88f1-5310319d40d3`
- **引用名**: `SmhJobRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `SmhJob`
- **完整路径**: `/MICROSAR/Smh/SmhJob`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: References a SmhHash job, which shall be used for the discrete hash.

######### 2. SmhDiscretHashConfig

**容器属性**:

- **UUID**: `4e51524b-a403-48b3-9ada-c1942ae9616f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SmhDiscretHashConfig`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Configure a discrete hash for the verification, which is used to calculate a hash before verifying the signature.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. SmhJobRef

- **UUID**: `51d9a895-6b6e-4e9f-88f1-5310319d40d3`
- **引用名**: `SmhJobRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `SmhJob`
- **完整路径**: `/MICROSAR/Smh/SmhJob`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: References a SmhHash job, which shall be used for the discrete hash.

####### 8. SmhSecurityClassCCCConfig

**容器属性**:

- **UUID**: `664dcb07-95ff-4179-8d6e-6ef8f5b49b46`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SmhSecurityClassCCCConfig`
- **多重性**: [1..infinite]
- **构建后可变**: false

**容器描述**:

Container to configure the stream verifications for security class CCC.

######## 参数配置

此容器包含 **2** 个参数：

######### BOOLEAN 类型参数

########## 1. SmhUpdateLengthOfHashedData

- **UUID**: `eec6e339-e8e3-44fa-b123-4e6a0eb5f1f0`
- **参数名**: `SmhUpdateLengthOfHashedData`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: If enabled, the security module will update the current length of hashed data in SecM_SignatureParamtype::currentDataLength.

######### FUNCTION-NAME 类型参数

########## 1. SmhFunctionName

- **UUID**: `2ea862e4-436b-42bd-9762-5fcc32430434`
- **参数名**: `SmhFunctionName`
- **数据类型**: FUNCTION-NAME
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Configure the function name of the stream verification, e.g.:
- SecM_VerifySigRsaPssSha256
- SecM_VerifySigEd25519PH

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. SmhJobRef

- **UUID**: `d60da727-ed84-438f-b298-500fde867ab8`
- **引用名**: `SmhJobRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `SmhJob`
- **完整路径**: `/MICROSAR/Smh/SmhJob`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: References a SmhSignatureVerify job, which shall be used by this stream verification.

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. SmhDiscretHashConfig

**容器属性**:

- **UUID**: `4e51524b-a403-48b3-9ada-c1942ae9616f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SmhDiscretHashConfig`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Configure a discrete hash for the verification, which is used to calculate a hash before verifying the signature.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. SmhJobRef

- **UUID**: `51d9a895-6b6e-4e9f-88f1-5310319d40d3`
- **引用名**: `SmhJobRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `SmhJob`
- **完整路径**: `/MICROSAR/Smh/SmhJob`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: References a SmhHash job, which shall be used for the discrete hash.

####### 9. SmhDiscretHashConfig

**容器属性**:

- **UUID**: `4e51524b-a403-48b3-9ada-c1942ae9616f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SmhDiscretHashConfig`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Configure a discrete hash for the verification, which is used to calculate a hash before verifying the signature.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. SmhJobRef

- **UUID**: `51d9a895-6b6e-4e9f-88f1-5310319d40d3`
- **引用名**: `SmhJobRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `SmhJob`
- **完整路径**: `/MICROSAR/Smh/SmhJob`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: References a SmhHash job, which shall be used for the discrete hash.

####### 10. SmhSecurityClassVendor

**容器属性**:

- **UUID**: `56bf5e0a-bd3a-4608-9838-e22f4d0b9b92`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SmhSecurityClassVendor`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container to configure the stream verification for security class CCC.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. SmhDefaultSecurityClassVendorConfig

- **UUID**: `6afe1497-e7b4-42b1-9a0b-b720a388b484`
- **引用名**: `SmhDefaultSecurityClassVendorConfig`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `SmhSecurityClassVendorConfig`
- **完整路径**: `/MICROSAR/Smh/SmhVerification/SmhStreamVerification/SmhSecurityClassVendor/SmhSecurityClassVendorConfig`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Default stream verification for the security class Vendor:
SecM_VerifyClassVendor

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. SmhSecurityClassVendorConfig

**容器属性**:

- **UUID**: `10b6f3b0-43c8-4825-897d-bde63d0e9513`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SmhSecurityClassVendorConfig`
- **多重性**: [1..infinite]
- **构建后可变**: false

**容器描述**:

Container to configure the stream verifications for security class CCC.

########## 参数配置

此容器包含 **2** 个参数：

########### INTEGER 类型参数

############ 1. SmhSizeOfVendorChecksum

- **UUID**: `cd3c9263-f865-4b17-84c1-39421281e243`
- **参数名**: `SmhSizeOfVendorChecksum`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `1`
- **取值范围**: [0..65535]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Configure the size of the vendor checksum.

########### FUNCTION-NAME 类型参数

############ 1. SmhClassVendorFunctionName

- **UUID**: `ca8ec340-3791-4548-816a-0e9d2459dea8`
- **参数名**: `SmhClassVendorFunctionName`
- **数据类型**: FUNCTION-NAME
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Configure the function name of the stream verification.

####### 11. SmhSecurityClassVendorConfig

**容器属性**:

- **UUID**: `10b6f3b0-43c8-4825-897d-bde63d0e9513`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SmhSecurityClassVendorConfig`
- **多重性**: [1..infinite]
- **构建后可变**: false

**容器描述**:

Container to configure the stream verifications for security class CCC.

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. SmhSizeOfVendorChecksum

- **UUID**: `cd3c9263-f865-4b17-84c1-39421281e243`
- **参数名**: `SmhSizeOfVendorChecksum`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `1`
- **取值范围**: [0..65535]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Configure the size of the vendor checksum.

######### FUNCTION-NAME 类型参数

########## 1. SmhClassVendorFunctionName

- **UUID**: `ca8ec340-3791-4548-816a-0e9d2459dea8`
- **参数名**: `SmhClassVendorFunctionName`
- **数据类型**: FUNCTION-NAME
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Configure the function name of the stream verification.

####### 12. SmhSecurityClassDDDType

**容器属性**:

- **UUID**: `d4091ae3-bc5f-49ed-aab5-4f51d555f432`
- **容器类型**: CHOICE-CONTAINER
- **容器名称**: `SmhSecurityClassDDDType`
- **多重性**: [1..1]
- **构建后可变**: false

**容器选择**:

- **SmhCrc**
  - UUID: `d77a32e4-ca21-4c5c-a0ec-75a6fae134fe`
  - 描述: Container to configure the CRC
- **SmhHash**
  - UUID: `860c29ac-feed-4843-be72-6b659b349d99`
  - 描述: Container to configure the hash

**容器描述**:

Specify the type of the security class DDD

##### 23. SmhSecurityClassDDD

**容器属性**:

- **UUID**: `f65076e1-6a4f-4afd-8f21-e8faea37fe6d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SmhSecurityClassDDD`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container to configure the stream verification for security class DDD.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. SmhDefaultSecurityClassDDDConfig

- **UUID**: `46906c73-00d0-4ce1-83bd-dd5f4112a3d8`
- **引用名**: `SmhDefaultSecurityClassDDDConfig`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `SmhSecurityClassDDDConfig`
- **完整路径**: `/MICROSAR/Smh/SmhVerification/SmhStreamVerification/SmhSecurityClassDDD/SmhSecurityClassDDDConfig`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Default stream verification for the security class DDD:
SecM_VerifyClassDDD

###### 配置容器

本模块包含 **4** 个配置容器：

####### 1. SmhSecurityClassDDDConfig

**容器属性**:

- **UUID**: `9edb72f4-2681-4d78-b583-25881036d326`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SmhSecurityClassDDDConfig`
- **多重性**: [1..infinite]
- **构建后可变**: false

**容器描述**:

Container to configure the stream verifications for security class DDD.

######## 参数配置

此容器包含 **3** 个参数：

######### BOOLEAN 类型参数

########## 1. SmhUpdateLengthOfHashedData

- **UUID**: `d4134277-9064-464b-a0e2-444e36fc56bc`
- **参数名**: `SmhUpdateLengthOfHashedData`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: If enabled, the security module will update the current length of hashed data in SecM_SignatureParamtype::currentDataLength.

########## 2. SmhComputationOnly

- **UUID**: `a77c5004-72b2-4e59-aee2-025769278b81`
- **参数名**: `SmhComputationOnly`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: If enabled the security module will just compute the CRC/hash without verifying it. The computed CRC/hash is provided via SecM_SignatureParamtype::sigSourceBuffer.

######### FUNCTION-NAME 类型参数

########## 1. SmhFunctionName

- **UUID**: `262ace43-2c7c-4462-9763-63cfd27ebe48`
- **参数名**: `SmhFunctionName`
- **数据类型**: FUNCTION-NAME
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Configure the function name of the stream verification, e.g.:
- SecM_VerifyCrc32
- SecM_VerifyHashSha512

######## 配置容器

本模块包含 **3** 个配置容器：

######### 1. SmhCrc

**容器属性**:

- **UUID**: `d77a32e4-ca21-4c5c-a0ec-75a6fae134fe`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SmhCrc`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container to configure the CRC

########## 引用关系

此容器包含 **1** 个引用：

########### CHOICE-REFERENCE 类型引用

############ 1. SmhCrcRef

- **UUID**: `545924b6-97cc-4283-9bee-5159bda168f9`
- **引用名**: `SmhCrcRef`
- **引用类型**: CHOICE-REFERENCE
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **需要索引**: false
- **目标引用列表**:
  - `/MICROSAR/Smh/SmhCrc/SmhCrc16`
  - `/MICROSAR/Smh/SmhCrc/SmhCrc32`
  - `/MICROSAR/Smh/SmhCrc/SmhCrc64`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: References a CRC configuration, which shall be used by this stream verification.

######### 2. SmhHash

**容器属性**:

- **UUID**: `860c29ac-feed-4843-be72-6b659b349d99`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SmhHash`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container to configure the hash

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. SmhJobRef

- **UUID**: `935a56dc-ff73-4f9e-9090-032d0f6d04cb`
- **引用名**: `SmhJobRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `SmhJob`
- **完整路径**: `/MICROSAR/Smh/SmhJob`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: References a SmhHash job, which shall be used by this stream verification.

######### 3. SmhSecurityClassDDDType

**容器属性**:

- **UUID**: `d4091ae3-bc5f-49ed-aab5-4f51d555f432`
- **容器类型**: CHOICE-CONTAINER
- **容器名称**: `SmhSecurityClassDDDType`
- **多重性**: [1..1]
- **构建后可变**: false

**容器选择**:

- **SmhCrc**
  - UUID: `d77a32e4-ca21-4c5c-a0ec-75a6fae134fe`
  - 描述: Container to configure the CRC
- **SmhHash**
  - UUID: `860c29ac-feed-4843-be72-6b659b349d99`
  - 描述: Container to configure the hash

**容器描述**:

Specify the type of the security class DDD

####### 2. SmhCrc

**容器属性**:

- **UUID**: `d77a32e4-ca21-4c5c-a0ec-75a6fae134fe`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SmhCrc`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container to configure the CRC

######## 引用关系

此容器包含 **1** 个引用：

######### CHOICE-REFERENCE 类型引用

########## 1. SmhCrcRef

- **UUID**: `545924b6-97cc-4283-9bee-5159bda168f9`
- **引用名**: `SmhCrcRef`
- **引用类型**: CHOICE-REFERENCE
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **需要索引**: false
- **目标引用列表**:
  - `/MICROSAR/Smh/SmhCrc/SmhCrc16`
  - `/MICROSAR/Smh/SmhCrc/SmhCrc32`
  - `/MICROSAR/Smh/SmhCrc/SmhCrc64`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: References a CRC configuration, which shall be used by this stream verification.

####### 3. SmhHash

**容器属性**:

- **UUID**: `860c29ac-feed-4843-be72-6b659b349d99`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SmhHash`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container to configure the hash

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. SmhJobRef

- **UUID**: `935a56dc-ff73-4f9e-9090-032d0f6d04cb`
- **引用名**: `SmhJobRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `SmhJob`
- **完整路径**: `/MICROSAR/Smh/SmhJob`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: References a SmhHash job, which shall be used by this stream verification.

####### 4. SmhSecurityClassDDDType

**容器属性**:

- **UUID**: `d4091ae3-bc5f-49ed-aab5-4f51d555f432`
- **容器类型**: CHOICE-CONTAINER
- **容器名称**: `SmhSecurityClassDDDType`
- **多重性**: [1..1]
- **构建后可变**: false

**容器选择**:

- **SmhCrc**
  - UUID: `d77a32e4-ca21-4c5c-a0ec-75a6fae134fe`
  - 描述: Container to configure the CRC
- **SmhHash**
  - UUID: `860c29ac-feed-4843-be72-6b659b349d99`
  - 描述: Container to configure the hash

**容器描述**:

Specify the type of the security class DDD

##### 24. SmhSecurityClassDDDConfig

**容器属性**:

- **UUID**: `9edb72f4-2681-4d78-b583-25881036d326`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SmhSecurityClassDDDConfig`
- **多重性**: [1..infinite]
- **构建后可变**: false

**容器描述**:

Container to configure the stream verifications for security class DDD.

###### 参数配置

此容器包含 **3** 个参数：

####### BOOLEAN 类型参数

######## 1. SmhUpdateLengthOfHashedData

- **UUID**: `d4134277-9064-464b-a0e2-444e36fc56bc`
- **参数名**: `SmhUpdateLengthOfHashedData`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: If enabled, the security module will update the current length of hashed data in SecM_SignatureParamtype::currentDataLength.

######## 2. SmhComputationOnly

- **UUID**: `a77c5004-72b2-4e59-aee2-025769278b81`
- **参数名**: `SmhComputationOnly`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: If enabled the security module will just compute the CRC/hash without verifying it. The computed CRC/hash is provided via SecM_SignatureParamtype::sigSourceBuffer.

####### FUNCTION-NAME 类型参数

######## 1. SmhFunctionName

- **UUID**: `262ace43-2c7c-4462-9763-63cfd27ebe48`
- **参数名**: `SmhFunctionName`
- **数据类型**: FUNCTION-NAME
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Configure the function name of the stream verification, e.g.:
- SecM_VerifyCrc32
- SecM_VerifyHashSha512

###### 配置容器

本模块包含 **3** 个配置容器：

####### 1. SmhCrc

**容器属性**:

- **UUID**: `d77a32e4-ca21-4c5c-a0ec-75a6fae134fe`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SmhCrc`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container to configure the CRC

######## 引用关系

此容器包含 **1** 个引用：

######### CHOICE-REFERENCE 类型引用

########## 1. SmhCrcRef

- **UUID**: `545924b6-97cc-4283-9bee-5159bda168f9`
- **引用名**: `SmhCrcRef`
- **引用类型**: CHOICE-REFERENCE
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **需要索引**: false
- **目标引用列表**:
  - `/MICROSAR/Smh/SmhCrc/SmhCrc16`
  - `/MICROSAR/Smh/SmhCrc/SmhCrc32`
  - `/MICROSAR/Smh/SmhCrc/SmhCrc64`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: References a CRC configuration, which shall be used by this stream verification.

####### 2. SmhHash

**容器属性**:

- **UUID**: `860c29ac-feed-4843-be72-6b659b349d99`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SmhHash`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container to configure the hash

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. SmhJobRef

- **UUID**: `935a56dc-ff73-4f9e-9090-032d0f6d04cb`
- **引用名**: `SmhJobRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `SmhJob`
- **完整路径**: `/MICROSAR/Smh/SmhJob`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: References a SmhHash job, which shall be used by this stream verification.

####### 3. SmhSecurityClassDDDType

**容器属性**:

- **UUID**: `d4091ae3-bc5f-49ed-aab5-4f51d555f432`
- **容器类型**: CHOICE-CONTAINER
- **容器名称**: `SmhSecurityClassDDDType`
- **多重性**: [1..1]
- **构建后可变**: false

**容器选择**:

- **SmhCrc**
  - UUID: `d77a32e4-ca21-4c5c-a0ec-75a6fae134fe`
  - 描述: Container to configure the CRC
- **SmhHash**
  - UUID: `860c29ac-feed-4843-be72-6b659b349d99`
  - 描述: Container to configure the hash

**容器描述**:

Specify the type of the security class DDD

##### 25. SmhCrc

**容器属性**:

- **UUID**: `d77a32e4-ca21-4c5c-a0ec-75a6fae134fe`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SmhCrc`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container to configure the CRC

###### 引用关系

此容器包含 **1** 个引用：

####### CHOICE-REFERENCE 类型引用

######## 1. SmhCrcRef

- **UUID**: `545924b6-97cc-4283-9bee-5159bda168f9`
- **引用名**: `SmhCrcRef`
- **引用类型**: CHOICE-REFERENCE
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **需要索引**: false
- **目标引用列表**:
  - `/MICROSAR/Smh/SmhCrc/SmhCrc16`
  - `/MICROSAR/Smh/SmhCrc/SmhCrc32`
  - `/MICROSAR/Smh/SmhCrc/SmhCrc64`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: References a CRC configuration, which shall be used by this stream verification.

##### 26. SmhHash

**容器属性**:

- **UUID**: `860c29ac-feed-4843-be72-6b659b349d99`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SmhHash`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container to configure the hash

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. SmhJobRef

- **UUID**: `935a56dc-ff73-4f9e-9090-032d0f6d04cb`
- **引用名**: `SmhJobRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `SmhJob`
- **完整路径**: `/MICROSAR/Smh/SmhJob`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: References a SmhHash job, which shall be used by this stream verification.

##### 27. SmhSecurityClassC

**容器属性**:

- **UUID**: `0bbafb93-8d89-4aa2-a917-76ff0cc0016a`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SmhSecurityClassC`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container to configure the stream verification for security class C.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. SmhDefaultSecurityClassCConfig

- **UUID**: `29bb2998-5a48-4047-9169-d03556cff09d`
- **引用名**: `SmhDefaultSecurityClassCConfig`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `SmhSecurityClassCConfig`
- **完整路径**: `/MICROSAR/Smh/SmhVerification/SmhStreamVerification/SmhSecurityClassC/SmhSecurityClassCConfig`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Default stream verification for the security class C:
SecM_VerifyClassC

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. SmhSecurityClassCConfig

**容器属性**:

- **UUID**: `db313d05-7ad6-453b-bc32-372ecc4c5ec4`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SmhSecurityClassCConfig`
- **多重性**: [1..infinite]
- **构建后可变**: false

**容器描述**:

Container to configure the stream verifications for security class C.

######## 参数配置

此容器包含 **3** 个参数：

######### BOOLEAN 类型参数

########## 1. SmhUpdateLengthOfHashedData

- **UUID**: `1e161cb2-0f71-4990-8d7a-84f8f1fbf05c`
- **参数名**: `SmhUpdateLengthOfHashedData`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: If enabled, the security module will update the current length of hashed data in SecM_SignatureParamtype::currentDataLength.

########## 2. SmhComputationOnly

- **UUID**: `ca7644f1-ecc0-46b1-b73f-f926b42df198`
- **参数名**: `SmhComputationOnly`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: If enabled the security module will just compute the MAC without verifying it. The computed MAC is provided via SecM_SignatureParamtype::sigSourceBuffer.

######### FUNCTION-NAME 类型参数

########## 1. SmhFunctionName

- **UUID**: `c9a732c4-3d9b-4838-a3ed-c21f7878e3c5`
- **参数名**: `SmhFunctionName`
- **数据类型**: FUNCTION-NAME
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Configure the function name of the stream verification, e.g.:
- SecM_VerifyMacHmacSha1
- SecM_VerifyMacCmac

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. SmhJobRef

- **UUID**: `4443273c-b72e-4faa-ae72-41ee1d2fe23c`
- **引用名**: `SmhJobRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `SmhJob`
- **完整路径**: `/MICROSAR/Smh/SmhJob`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: References a SmhMacVerify or SmhMacGenerate job, which shall be used by this stream verification.

##### 28. SmhSecurityClassCConfig

**容器属性**:

- **UUID**: `db313d05-7ad6-453b-bc32-372ecc4c5ec4`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SmhSecurityClassCConfig`
- **多重性**: [1..infinite]
- **构建后可变**: false

**容器描述**:

Container to configure the stream verifications for security class C.

###### 参数配置

此容器包含 **3** 个参数：

####### BOOLEAN 类型参数

######## 1. SmhUpdateLengthOfHashedData

- **UUID**: `1e161cb2-0f71-4990-8d7a-84f8f1fbf05c`
- **参数名**: `SmhUpdateLengthOfHashedData`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: If enabled, the security module will update the current length of hashed data in SecM_SignatureParamtype::currentDataLength.

######## 2. SmhComputationOnly

- **UUID**: `ca7644f1-ecc0-46b1-b73f-f926b42df198`
- **参数名**: `SmhComputationOnly`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: If enabled the security module will just compute the MAC without verifying it. The computed MAC is provided via SecM_SignatureParamtype::sigSourceBuffer.

####### FUNCTION-NAME 类型参数

######## 1. SmhFunctionName

- **UUID**: `c9a732c4-3d9b-4838-a3ed-c21f7878e3c5`
- **参数名**: `SmhFunctionName`
- **数据类型**: FUNCTION-NAME
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Configure the function name of the stream verification, e.g.:
- SecM_VerifyMacHmacSha1
- SecM_VerifyMacCmac

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. SmhJobRef

- **UUID**: `4443273c-b72e-4faa-ae72-41ee1d2fe23c`
- **引用名**: `SmhJobRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `SmhJob`
- **完整路径**: `/MICROSAR/Smh/SmhJob`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: References a SmhMacVerify or SmhMacGenerate job, which shall be used by this stream verification.

##### 29. SmhSecurityClassCCC

**容器属性**:

- **UUID**: `e8bb9b83-5292-4b97-9d4e-6f37ada0a6c1`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SmhSecurityClassCCC`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container to configure the stream verification for security class CCC.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. SmhDefaultSecurityClassCCCConfig

- **UUID**: `0442501f-54c8-4df8-a5a1-c1a5f7de1398`
- **引用名**: `SmhDefaultSecurityClassCCCConfig`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `SmhSecurityClassCCCConfig`
- **完整路径**: `/MICROSAR/Smh/SmhVerification/SmhStreamVerification/SmhSecurityClassCCC/SmhSecurityClassCCCConfig`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Default stream verification for the security class CCC:
SecM_VerifyClassCCC

###### 配置容器

本模块包含 **2** 个配置容器：

####### 1. SmhSecurityClassCCCConfig

**容器属性**:

- **UUID**: `664dcb07-95ff-4179-8d6e-6ef8f5b49b46`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SmhSecurityClassCCCConfig`
- **多重性**: [1..infinite]
- **构建后可变**: false

**容器描述**:

Container to configure the stream verifications for security class CCC.

######## 参数配置

此容器包含 **2** 个参数：

######### BOOLEAN 类型参数

########## 1. SmhUpdateLengthOfHashedData

- **UUID**: `eec6e339-e8e3-44fa-b123-4e6a0eb5f1f0`
- **参数名**: `SmhUpdateLengthOfHashedData`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: If enabled, the security module will update the current length of hashed data in SecM_SignatureParamtype::currentDataLength.

######### FUNCTION-NAME 类型参数

########## 1. SmhFunctionName

- **UUID**: `2ea862e4-436b-42bd-9762-5fcc32430434`
- **参数名**: `SmhFunctionName`
- **数据类型**: FUNCTION-NAME
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Configure the function name of the stream verification, e.g.:
- SecM_VerifySigRsaPssSha256
- SecM_VerifySigEd25519PH

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. SmhJobRef

- **UUID**: `d60da727-ed84-438f-b298-500fde867ab8`
- **引用名**: `SmhJobRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `SmhJob`
- **完整路径**: `/MICROSAR/Smh/SmhJob`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: References a SmhSignatureVerify job, which shall be used by this stream verification.

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. SmhDiscretHashConfig

**容器属性**:

- **UUID**: `4e51524b-a403-48b3-9ada-c1942ae9616f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SmhDiscretHashConfig`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Configure a discrete hash for the verification, which is used to calculate a hash before verifying the signature.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. SmhJobRef

- **UUID**: `51d9a895-6b6e-4e9f-88f1-5310319d40d3`
- **引用名**: `SmhJobRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `SmhJob`
- **完整路径**: `/MICROSAR/Smh/SmhJob`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: References a SmhHash job, which shall be used for the discrete hash.

####### 2. SmhDiscretHashConfig

**容器属性**:

- **UUID**: `4e51524b-a403-48b3-9ada-c1942ae9616f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SmhDiscretHashConfig`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Configure a discrete hash for the verification, which is used to calculate a hash before verifying the signature.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. SmhJobRef

- **UUID**: `51d9a895-6b6e-4e9f-88f1-5310319d40d3`
- **引用名**: `SmhJobRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `SmhJob`
- **完整路径**: `/MICROSAR/Smh/SmhJob`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: References a SmhHash job, which shall be used for the discrete hash.

##### 30. SmhSecurityClassCCCConfig

**容器属性**:

- **UUID**: `664dcb07-95ff-4179-8d6e-6ef8f5b49b46`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SmhSecurityClassCCCConfig`
- **多重性**: [1..infinite]
- **构建后可变**: false

**容器描述**:

Container to configure the stream verifications for security class CCC.

###### 参数配置

此容器包含 **2** 个参数：

####### BOOLEAN 类型参数

######## 1. SmhUpdateLengthOfHashedData

- **UUID**: `eec6e339-e8e3-44fa-b123-4e6a0eb5f1f0`
- **参数名**: `SmhUpdateLengthOfHashedData`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: If enabled, the security module will update the current length of hashed data in SecM_SignatureParamtype::currentDataLength.

####### FUNCTION-NAME 类型参数

######## 1. SmhFunctionName

- **UUID**: `2ea862e4-436b-42bd-9762-5fcc32430434`
- **参数名**: `SmhFunctionName`
- **数据类型**: FUNCTION-NAME
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Configure the function name of the stream verification, e.g.:
- SecM_VerifySigRsaPssSha256
- SecM_VerifySigEd25519PH

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. SmhJobRef

- **UUID**: `d60da727-ed84-438f-b298-500fde867ab8`
- **引用名**: `SmhJobRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `SmhJob`
- **完整路径**: `/MICROSAR/Smh/SmhJob`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: References a SmhSignatureVerify job, which shall be used by this stream verification.

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. SmhDiscretHashConfig

**容器属性**:

- **UUID**: `4e51524b-a403-48b3-9ada-c1942ae9616f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SmhDiscretHashConfig`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Configure a discrete hash for the verification, which is used to calculate a hash before verifying the signature.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. SmhJobRef

- **UUID**: `51d9a895-6b6e-4e9f-88f1-5310319d40d3`
- **引用名**: `SmhJobRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `SmhJob`
- **完整路径**: `/MICROSAR/Smh/SmhJob`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: References a SmhHash job, which shall be used for the discrete hash.

##### 31. SmhDiscretHashConfig

**容器属性**:

- **UUID**: `4e51524b-a403-48b3-9ada-c1942ae9616f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SmhDiscretHashConfig`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Configure a discrete hash for the verification, which is used to calculate a hash before verifying the signature.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. SmhJobRef

- **UUID**: `51d9a895-6b6e-4e9f-88f1-5310319d40d3`
- **引用名**: `SmhJobRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `SmhJob`
- **完整路径**: `/MICROSAR/Smh/SmhJob`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: References a SmhHash job, which shall be used for the discrete hash.

##### 32. SmhSecurityClassVendor

**容器属性**:

- **UUID**: `56bf5e0a-bd3a-4608-9838-e22f4d0b9b92`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SmhSecurityClassVendor`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container to configure the stream verification for security class CCC.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. SmhDefaultSecurityClassVendorConfig

- **UUID**: `6afe1497-e7b4-42b1-9a0b-b720a388b484`
- **引用名**: `SmhDefaultSecurityClassVendorConfig`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `SmhSecurityClassVendorConfig`
- **完整路径**: `/MICROSAR/Smh/SmhVerification/SmhStreamVerification/SmhSecurityClassVendor/SmhSecurityClassVendorConfig`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Default stream verification for the security class Vendor:
SecM_VerifyClassVendor

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. SmhSecurityClassVendorConfig

**容器属性**:

- **UUID**: `10b6f3b0-43c8-4825-897d-bde63d0e9513`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SmhSecurityClassVendorConfig`
- **多重性**: [1..infinite]
- **构建后可变**: false

**容器描述**:

Container to configure the stream verifications for security class CCC.

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. SmhSizeOfVendorChecksum

- **UUID**: `cd3c9263-f865-4b17-84c1-39421281e243`
- **参数名**: `SmhSizeOfVendorChecksum`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `1`
- **取值范围**: [0..65535]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Configure the size of the vendor checksum.

######### FUNCTION-NAME 类型参数

########## 1. SmhClassVendorFunctionName

- **UUID**: `ca8ec340-3791-4548-816a-0e9d2459dea8`
- **参数名**: `SmhClassVendorFunctionName`
- **数据类型**: FUNCTION-NAME
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Configure the function name of the stream verification.

##### 33. SmhSecurityClassVendorConfig

**容器属性**:

- **UUID**: `10b6f3b0-43c8-4825-897d-bde63d0e9513`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SmhSecurityClassVendorConfig`
- **多重性**: [1..infinite]
- **构建后可变**: false

**容器描述**:

Container to configure the stream verifications for security class CCC.

###### 参数配置

此容器包含 **2** 个参数：

####### INTEGER 类型参数

######## 1. SmhSizeOfVendorChecksum

- **UUID**: `cd3c9263-f865-4b17-84c1-39421281e243`
- **参数名**: `SmhSizeOfVendorChecksum`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `1`
- **取值范围**: [0..65535]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Configure the size of the vendor checksum.

####### FUNCTION-NAME 类型参数

######## 1. SmhClassVendorFunctionName

- **UUID**: `ca8ec340-3791-4548-816a-0e9d2459dea8`
- **参数名**: `SmhClassVendorFunctionName`
- **数据类型**: FUNCTION-NAME
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Configure the function name of the stream verification.

##### 34. SmhCryptographicKeys

**容器属性**:

- **UUID**: `957d28cf-a2cd-4661-ba6a-7f192432269c`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SmhCryptographicKeys`
- **多重性**: [1..1]
- **构建后可变**: false

**容器描述**:

Configure the cryptographic keys which are used by the SmhJob to initialize the key elements in the crypto module.

###### 参数配置

此容器包含 **2** 个参数：

####### INTEGER 类型参数

######## 1. SmhElementIdRSAPublicExponent

- **UUID**: `114c36df-6825-492e-92c9-2ea2329f7658`
- **参数名**: `SmhElementIdRSAPublicExponent`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `161`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Key element ID of the RSA public exponent

######## 2. SmhElementIdRSAModulus

- **UUID**: `5fac7892-8aec-4f22-b750-f671271fc435`
- **参数名**: `SmhElementIdRSAModulus`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `160`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Key element ID of the RSA modulus.

###### 配置容器

本模块包含 **6** 个配置容器：

####### 1. SmhKey

**容器属性**:

- **UUID**: `51f91902-e974-4d10-8af0-7d2031f39cd1`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SmhKey`
- **多重性**: [0..infinite]
- **构建后可变**: false

**容器描述**:

Contains the configuration of keys.

######## 参数配置

此容器包含 **1** 个参数：

######### STRING 类型参数

########## 1. SmhDescription

- **UUID**: `1eef5455-8a5f-43cf-a08c-edd6ee6cfe0e`
- **参数名**: `SmhDescription`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Short description of the key.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. SmhKeyValueRef

- **UUID**: `96b5facc-b5d3-4687-a6bb-816d02bf0de4`
- **引用名**: `SmhKeyValueRef`
- **引用类型**: REFERENCE
- **多重性**: [1..infinite]
- **目标**: `SmhKeyValue`
- **完整路径**: `/MICROSAR/Smh/SmhCryptographicKeys/SmhKeyValue`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: References to key values which shall be associated with this key.

####### 2. SmhKeyValue

**容器属性**:

- **UUID**: `3d747438-c9e1-4a6c-aa39-825d20ef896e`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SmhKeyValue`
- **多重性**: [0..infinite]
- **构建后可变**: false

**容器描述**:

Contains the configuration of key values.

######## 参数配置

此容器包含 **3** 个参数：

######### STRING 类型参数

########## 1. SmhSuffix

- **UUID**: `78ccc163-e6ea-4cad-8de8-fe4eb4186258`
- **参数名**: `SmhSuffix`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Additional suffix to the key value.

########## 2. SmhValue

- **UUID**: `b05bbc27-c867-4815-8336-d41b55fa629c`
- **参数名**: `SmhValue`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Actual key value.

The value can be left empty. In this case the security module has no internal key and will only try to write a key if it was provided.

########## 3. SmhDescription

- **UUID**: `a84a0fd4-770f-469e-b444-bc14e7d4494a`
- **参数名**: `SmhDescription`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Short description of the key value.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. SmhCryptoKeyElementRef

- **UUID**: `9d0e79f6-40ed-47db-9cec-a45b9c737fc8`
- **引用名**: `SmhCryptoKeyElementRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `CryptoKeyElement`
- **完整路径**: `/AUTOSAR/EcucDefs/Crypto/CryptoKeyElements/CryptoKeyElement`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: References the associated CryptoKeyElement.

####### 3. SmhKeyOperations

**容器属性**:

- **UUID**: `f8ba7510-e0fc-47a8-b753-7cb82c93f9db`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SmhKeyOperations`
- **多重性**: [1..1]
- **构建后可变**: false

**容器描述**:

Contains the configuration for key operations

######## 配置容器

本模块包含 **3** 个配置容器：

######### 1. SmhAccessKeyElementOperation

**容器属性**:

- **UUID**: `63764dc5-1810-4cdb-ba47-910edc0641c6`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SmhAccessKeyElementOperation`
- **多重性**: [0..infinite]
- **构建后可变**: false

**容器描述**:

Contains the configuration to access (Get/Set) Keys Elements

########## 参数配置

此容器包含 **2** 个参数：

########### STRING 类型参数

############ 1. SmhSetKeyElementMacroName

- **UUID**: `36267b66-8f12-4bb5-b132-faeebb6e7acc`
- **参数名**: `SmhSetKeyElementMacroName`
- **数据类型**: STRING
- **多重性**: [1..1]
- **符号名值**: false
- **需要索引**: false
- **字符串变体**:
  - 最小长度: 1
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Name of the generated function-like macro to set the given key element.

############ 2. SmhGetKeyElementMacroName

- **UUID**: `853cb6b4-3fcb-4bbc-b06f-f598eff5f348`
- **参数名**: `SmhGetKeyElementMacroName`
- **数据类型**: STRING
- **多重性**: [1..1]
- **符号名值**: false
- **需要索引**: false
- **字符串变体**:
  - 最小长度: 1
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Name of the generated function-like macro to get the given key element.

########## 引用关系

此容器包含 **2** 个引用：

########### REFERENCE 类型引用

############ 1. SmhCsmKeyRef

- **UUID**: `cbda49fd-2888-4be2-ad91-caf49aa9ffe1`
- **引用名**: `SmhCsmKeyRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `CsmKey`
- **完整路径**: `/AUTOSAR/EcucDefs/Csm/CsmKeys/CsmKey`
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Reference to the key in CSM

############ 2. SmhCryptographicKeyValueRef

- **UUID**: `2e2cdeed-44f0-47cd-9061-79282723ff26`
- **引用名**: `SmhCryptographicKeyValueRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `SmhKeyValue`
- **完整路径**: `/MICROSAR/Smh/SmhCryptographicKeys/SmhKeyValue`
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Reference to the key value in Smh

######### 2. SmhCopyKeyOperation

**容器属性**:

- **UUID**: `a982cf66-ee1b-4da3-a684-000d987ef32c`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SmhCopyKeyOperation`
- **多重性**: [0..infinite]
- **构建后可变**: false

**容器描述**:

Contains the configuration to copy complete keys

########## 参数配置

此容器包含 **1** 个参数：

########### STRING 类型参数

############ 1. SmhCopyKeyMacroName

- **UUID**: `dbe572ef-7967-432f-911b-7d8df3d59c61`
- **参数名**: `SmhCopyKeyMacroName`
- **数据类型**: STRING
- **多重性**: [1..1]
- **符号名值**: false
- **需要索引**: false
- **字符串变体**:
  - 最小长度: 1
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Name of the generated function-like macro to copy the given key.

########## 引用关系

此容器包含 **2** 个引用：

########### REFERENCE 类型引用

############ 1. SmhSourceCsmKeyRef

- **UUID**: `cb070f8c-2ca8-4d61-a3c7-762ea44201a5`
- **引用名**: `SmhSourceCsmKeyRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `CsmKey`
- **完整路径**: `/AUTOSAR/EcucDefs/Csm/CsmKeys/CsmKey`
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Reference to the source key in CSM

############ 2. SmhTargetCsmKeyRef

- **UUID**: `5e4d8d43-dc11-490a-bf45-d1f1cb83e19d`
- **引用名**: `SmhTargetCsmKeyRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `CsmKey`
- **完整路径**: `/AUTOSAR/EcucDefs/Csm/CsmKeys/CsmKey`
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Reference to the target key in CSM

######### 3. SmhCopyKeyElementOperation

**容器属性**:

- **UUID**: `afbed9cb-6e16-4fb3-b73a-fb2a96099db3`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SmhCopyKeyElementOperation`
- **多重性**: [0..infinite]
- **构建后可变**: false

**容器描述**:

Contains the configuration to copy keys elements

########## 参数配置

此容器包含 **1** 个参数：

########### STRING 类型参数

############ 1. SmhCopyKeyElementMacroName

- **UUID**: `e203688d-6233-49cd-b3b7-6cb3aa55818e`
- **参数名**: `SmhCopyKeyElementMacroName`
- **数据类型**: STRING
- **多重性**: [1..1]
- **符号名值**: false
- **需要索引**: false
- **字符串变体**:
  - 最小长度: 1
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Name of the generated function-like macro to copy the given key element.

########## 引用关系

此容器包含 **4** 个引用：

########### REFERENCE 类型引用

############ 1. SmhSourceCsmKeyRef

- **UUID**: `4f740df9-67f1-437b-b16a-a8c225621055`
- **引用名**: `SmhSourceCsmKeyRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `CsmKey`
- **完整路径**: `/AUTOSAR/EcucDefs/Csm/CsmKeys/CsmKey`
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Reference to the source key in CSM

############ 2. SmhTargetCsmKeyRef

- **UUID**: `1b73cb59-faa7-45c3-886f-f1b2f30648f9`
- **引用名**: `SmhTargetCsmKeyRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `CsmKey`
- **完整路径**: `/AUTOSAR/EcucDefs/Csm/CsmKeys/CsmKey`
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Reference to the target key in CSM

############ 3. SmhSourceCryptographicKeyValueRef

- **UUID**: `3aba8714-6394-418c-ad3d-99695b6ecd63`
- **引用名**: `SmhSourceCryptographicKeyValueRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `SmhKeyValue`
- **完整路径**: `/MICROSAR/Smh/SmhCryptographicKeys/SmhKeyValue`
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Reference to the source key value in Smh

############ 4. SmhTargetCryptographicKeyValueRef

- **UUID**: `9758e996-6669-4e79-b6e0-ada91e5745ec`
- **引用名**: `SmhTargetCryptographicKeyValueRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `SmhKeyValue`
- **完整路径**: `/MICROSAR/Smh/SmhCryptographicKeys/SmhKeyValue`
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Reference to the target key value in Smh

####### 4. SmhAccessKeyElementOperation

**容器属性**:

- **UUID**: `63764dc5-1810-4cdb-ba47-910edc0641c6`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SmhAccessKeyElementOperation`
- **多重性**: [0..infinite]
- **构建后可变**: false

**容器描述**:

Contains the configuration to access (Get/Set) Keys Elements

######## 参数配置

此容器包含 **2** 个参数：

######### STRING 类型参数

########## 1. SmhSetKeyElementMacroName

- **UUID**: `36267b66-8f12-4bb5-b132-faeebb6e7acc`
- **参数名**: `SmhSetKeyElementMacroName`
- **数据类型**: STRING
- **多重性**: [1..1]
- **符号名值**: false
- **需要索引**: false
- **字符串变体**:
  - 最小长度: 1
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Name of the generated function-like macro to set the given key element.

########## 2. SmhGetKeyElementMacroName

- **UUID**: `853cb6b4-3fcb-4bbc-b06f-f598eff5f348`
- **参数名**: `SmhGetKeyElementMacroName`
- **数据类型**: STRING
- **多重性**: [1..1]
- **符号名值**: false
- **需要索引**: false
- **字符串变体**:
  - 最小长度: 1
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Name of the generated function-like macro to get the given key element.

######## 引用关系

此容器包含 **2** 个引用：

######### REFERENCE 类型引用

########## 1. SmhCsmKeyRef

- **UUID**: `cbda49fd-2888-4be2-ad91-caf49aa9ffe1`
- **引用名**: `SmhCsmKeyRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `CsmKey`
- **完整路径**: `/AUTOSAR/EcucDefs/Csm/CsmKeys/CsmKey`
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Reference to the key in CSM

########## 2. SmhCryptographicKeyValueRef

- **UUID**: `2e2cdeed-44f0-47cd-9061-79282723ff26`
- **引用名**: `SmhCryptographicKeyValueRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `SmhKeyValue`
- **完整路径**: `/MICROSAR/Smh/SmhCryptographicKeys/SmhKeyValue`
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Reference to the key value in Smh

####### 5. SmhCopyKeyOperation

**容器属性**:

- **UUID**: `a982cf66-ee1b-4da3-a684-000d987ef32c`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SmhCopyKeyOperation`
- **多重性**: [0..infinite]
- **构建后可变**: false

**容器描述**:

Contains the configuration to copy complete keys

######## 参数配置

此容器包含 **1** 个参数：

######### STRING 类型参数

########## 1. SmhCopyKeyMacroName

- **UUID**: `dbe572ef-7967-432f-911b-7d8df3d59c61`
- **参数名**: `SmhCopyKeyMacroName`
- **数据类型**: STRING
- **多重性**: [1..1]
- **符号名值**: false
- **需要索引**: false
- **字符串变体**:
  - 最小长度: 1
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Name of the generated function-like macro to copy the given key.

######## 引用关系

此容器包含 **2** 个引用：

######### REFERENCE 类型引用

########## 1. SmhSourceCsmKeyRef

- **UUID**: `cb070f8c-2ca8-4d61-a3c7-762ea44201a5`
- **引用名**: `SmhSourceCsmKeyRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `CsmKey`
- **完整路径**: `/AUTOSAR/EcucDefs/Csm/CsmKeys/CsmKey`
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Reference to the source key in CSM

########## 2. SmhTargetCsmKeyRef

- **UUID**: `5e4d8d43-dc11-490a-bf45-d1f1cb83e19d`
- **引用名**: `SmhTargetCsmKeyRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `CsmKey`
- **完整路径**: `/AUTOSAR/EcucDefs/Csm/CsmKeys/CsmKey`
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Reference to the target key in CSM

####### 6. SmhCopyKeyElementOperation

**容器属性**:

- **UUID**: `afbed9cb-6e16-4fb3-b73a-fb2a96099db3`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SmhCopyKeyElementOperation`
- **多重性**: [0..infinite]
- **构建后可变**: false

**容器描述**:

Contains the configuration to copy keys elements

######## 参数配置

此容器包含 **1** 个参数：

######### STRING 类型参数

########## 1. SmhCopyKeyElementMacroName

- **UUID**: `e203688d-6233-49cd-b3b7-6cb3aa55818e`
- **参数名**: `SmhCopyKeyElementMacroName`
- **数据类型**: STRING
- **多重性**: [1..1]
- **符号名值**: false
- **需要索引**: false
- **字符串变体**:
  - 最小长度: 1
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Name of the generated function-like macro to copy the given key element.

######## 引用关系

此容器包含 **4** 个引用：

######### REFERENCE 类型引用

########## 1. SmhSourceCsmKeyRef

- **UUID**: `4f740df9-67f1-437b-b16a-a8c225621055`
- **引用名**: `SmhSourceCsmKeyRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `CsmKey`
- **完整路径**: `/AUTOSAR/EcucDefs/Csm/CsmKeys/CsmKey`
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Reference to the source key in CSM

########## 2. SmhTargetCsmKeyRef

- **UUID**: `1b73cb59-faa7-45c3-886f-f1b2f30648f9`
- **引用名**: `SmhTargetCsmKeyRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `CsmKey`
- **完整路径**: `/AUTOSAR/EcucDefs/Csm/CsmKeys/CsmKey`
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Reference to the target key in CSM

########## 3. SmhSourceCryptographicKeyValueRef

- **UUID**: `3aba8714-6394-418c-ad3d-99695b6ecd63`
- **引用名**: `SmhSourceCryptographicKeyValueRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `SmhKeyValue`
- **完整路径**: `/MICROSAR/Smh/SmhCryptographicKeys/SmhKeyValue`
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Reference to the source key value in Smh

########## 4. SmhTargetCryptographicKeyValueRef

- **UUID**: `9758e996-6669-4e79-b6e0-ada91e5745ec`
- **引用名**: `SmhTargetCryptographicKeyValueRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `SmhKeyValue`
- **完整路径**: `/MICROSAR/Smh/SmhCryptographicKeys/SmhKeyValue`
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Reference to the target key value in Smh

##### 35. SmhKey

**容器属性**:

- **UUID**: `51f91902-e974-4d10-8af0-7d2031f39cd1`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SmhKey`
- **多重性**: [0..infinite]
- **构建后可变**: false

**容器描述**:

Contains the configuration of keys.

###### 参数配置

此容器包含 **1** 个参数：

####### STRING 类型参数

######## 1. SmhDescription

- **UUID**: `1eef5455-8a5f-43cf-a08c-edd6ee6cfe0e`
- **参数名**: `SmhDescription`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Short description of the key.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. SmhKeyValueRef

- **UUID**: `96b5facc-b5d3-4687-a6bb-816d02bf0de4`
- **引用名**: `SmhKeyValueRef`
- **引用类型**: REFERENCE
- **多重性**: [1..infinite]
- **目标**: `SmhKeyValue`
- **完整路径**: `/MICROSAR/Smh/SmhCryptographicKeys/SmhKeyValue`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: References to key values which shall be associated with this key.

##### 36. SmhKeyValue

**容器属性**:

- **UUID**: `3d747438-c9e1-4a6c-aa39-825d20ef896e`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SmhKeyValue`
- **多重性**: [0..infinite]
- **构建后可变**: false

**容器描述**:

Contains the configuration of key values.

###### 参数配置

此容器包含 **3** 个参数：

####### STRING 类型参数

######## 1. SmhSuffix

- **UUID**: `78ccc163-e6ea-4cad-8de8-fe4eb4186258`
- **参数名**: `SmhSuffix`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Additional suffix to the key value.

######## 2. SmhValue

- **UUID**: `b05bbc27-c867-4815-8336-d41b55fa629c`
- **参数名**: `SmhValue`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Actual key value.

The value can be left empty. In this case the security module has no internal key and will only try to write a key if it was provided.

######## 3. SmhDescription

- **UUID**: `a84a0fd4-770f-469e-b444-bc14e7d4494a`
- **参数名**: `SmhDescription`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Short description of the key value.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. SmhCryptoKeyElementRef

- **UUID**: `9d0e79f6-40ed-47db-9cec-a45b9c737fc8`
- **引用名**: `SmhCryptoKeyElementRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `CryptoKeyElement`
- **完整路径**: `/AUTOSAR/EcucDefs/Crypto/CryptoKeyElements/CryptoKeyElement`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: References the associated CryptoKeyElement.

##### 37. SmhKeyOperations

**容器属性**:

- **UUID**: `f8ba7510-e0fc-47a8-b753-7cb82c93f9db`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SmhKeyOperations`
- **多重性**: [1..1]
- **构建后可变**: false

**容器描述**:

Contains the configuration for key operations

###### 配置容器

本模块包含 **3** 个配置容器：

####### 1. SmhAccessKeyElementOperation

**容器属性**:

- **UUID**: `63764dc5-1810-4cdb-ba47-910edc0641c6`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SmhAccessKeyElementOperation`
- **多重性**: [0..infinite]
- **构建后可变**: false

**容器描述**:

Contains the configuration to access (Get/Set) Keys Elements

######## 参数配置

此容器包含 **2** 个参数：

######### STRING 类型参数

########## 1. SmhSetKeyElementMacroName

- **UUID**: `36267b66-8f12-4bb5-b132-faeebb6e7acc`
- **参数名**: `SmhSetKeyElementMacroName`
- **数据类型**: STRING
- **多重性**: [1..1]
- **符号名值**: false
- **需要索引**: false
- **字符串变体**:
  - 最小长度: 1
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Name of the generated function-like macro to set the given key element.

########## 2. SmhGetKeyElementMacroName

- **UUID**: `853cb6b4-3fcb-4bbc-b06f-f598eff5f348`
- **参数名**: `SmhGetKeyElementMacroName`
- **数据类型**: STRING
- **多重性**: [1..1]
- **符号名值**: false
- **需要索引**: false
- **字符串变体**:
  - 最小长度: 1
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Name of the generated function-like macro to get the given key element.

######## 引用关系

此容器包含 **2** 个引用：

######### REFERENCE 类型引用

########## 1. SmhCsmKeyRef

- **UUID**: `cbda49fd-2888-4be2-ad91-caf49aa9ffe1`
- **引用名**: `SmhCsmKeyRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `CsmKey`
- **完整路径**: `/AUTOSAR/EcucDefs/Csm/CsmKeys/CsmKey`
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Reference to the key in CSM

########## 2. SmhCryptographicKeyValueRef

- **UUID**: `2e2cdeed-44f0-47cd-9061-79282723ff26`
- **引用名**: `SmhCryptographicKeyValueRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `SmhKeyValue`
- **完整路径**: `/MICROSAR/Smh/SmhCryptographicKeys/SmhKeyValue`
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Reference to the key value in Smh

####### 2. SmhCopyKeyOperation

**容器属性**:

- **UUID**: `a982cf66-ee1b-4da3-a684-000d987ef32c`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SmhCopyKeyOperation`
- **多重性**: [0..infinite]
- **构建后可变**: false

**容器描述**:

Contains the configuration to copy complete keys

######## 参数配置

此容器包含 **1** 个参数：

######### STRING 类型参数

########## 1. SmhCopyKeyMacroName

- **UUID**: `dbe572ef-7967-432f-911b-7d8df3d59c61`
- **参数名**: `SmhCopyKeyMacroName`
- **数据类型**: STRING
- **多重性**: [1..1]
- **符号名值**: false
- **需要索引**: false
- **字符串变体**:
  - 最小长度: 1
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Name of the generated function-like macro to copy the given key.

######## 引用关系

此容器包含 **2** 个引用：

######### REFERENCE 类型引用

########## 1. SmhSourceCsmKeyRef

- **UUID**: `cb070f8c-2ca8-4d61-a3c7-762ea44201a5`
- **引用名**: `SmhSourceCsmKeyRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `CsmKey`
- **完整路径**: `/AUTOSAR/EcucDefs/Csm/CsmKeys/CsmKey`
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Reference to the source key in CSM

########## 2. SmhTargetCsmKeyRef

- **UUID**: `5e4d8d43-dc11-490a-bf45-d1f1cb83e19d`
- **引用名**: `SmhTargetCsmKeyRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `CsmKey`
- **完整路径**: `/AUTOSAR/EcucDefs/Csm/CsmKeys/CsmKey`
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Reference to the target key in CSM

####### 3. SmhCopyKeyElementOperation

**容器属性**:

- **UUID**: `afbed9cb-6e16-4fb3-b73a-fb2a96099db3`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SmhCopyKeyElementOperation`
- **多重性**: [0..infinite]
- **构建后可变**: false

**容器描述**:

Contains the configuration to copy keys elements

######## 参数配置

此容器包含 **1** 个参数：

######### STRING 类型参数

########## 1. SmhCopyKeyElementMacroName

- **UUID**: `e203688d-6233-49cd-b3b7-6cb3aa55818e`
- **参数名**: `SmhCopyKeyElementMacroName`
- **数据类型**: STRING
- **多重性**: [1..1]
- **符号名值**: false
- **需要索引**: false
- **字符串变体**:
  - 最小长度: 1
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Name of the generated function-like macro to copy the given key element.

######## 引用关系

此容器包含 **4** 个引用：

######### REFERENCE 类型引用

########## 1. SmhSourceCsmKeyRef

- **UUID**: `4f740df9-67f1-437b-b16a-a8c225621055`
- **引用名**: `SmhSourceCsmKeyRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `CsmKey`
- **完整路径**: `/AUTOSAR/EcucDefs/Csm/CsmKeys/CsmKey`
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Reference to the source key in CSM

########## 2. SmhTargetCsmKeyRef

- **UUID**: `1b73cb59-faa7-45c3-886f-f1b2f30648f9`
- **引用名**: `SmhTargetCsmKeyRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `CsmKey`
- **完整路径**: `/AUTOSAR/EcucDefs/Csm/CsmKeys/CsmKey`
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Reference to the target key in CSM

########## 3. SmhSourceCryptographicKeyValueRef

- **UUID**: `3aba8714-6394-418c-ad3d-99695b6ecd63`
- **引用名**: `SmhSourceCryptographicKeyValueRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `SmhKeyValue`
- **完整路径**: `/MICROSAR/Smh/SmhCryptographicKeys/SmhKeyValue`
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Reference to the source key value in Smh

########## 4. SmhTargetCryptographicKeyValueRef

- **UUID**: `9758e996-6669-4e79-b6e0-ada91e5745ec`
- **引用名**: `SmhTargetCryptographicKeyValueRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `SmhKeyValue`
- **完整路径**: `/MICROSAR/Smh/SmhCryptographicKeys/SmhKeyValue`
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Reference to the target key value in Smh

##### 38. SmhAccessKeyElementOperation

**容器属性**:

- **UUID**: `63764dc5-1810-4cdb-ba47-910edc0641c6`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SmhAccessKeyElementOperation`
- **多重性**: [0..infinite]
- **构建后可变**: false

**容器描述**:

Contains the configuration to access (Get/Set) Keys Elements

###### 参数配置

此容器包含 **2** 个参数：

####### STRING 类型参数

######## 1. SmhSetKeyElementMacroName

- **UUID**: `36267b66-8f12-4bb5-b132-faeebb6e7acc`
- **参数名**: `SmhSetKeyElementMacroName`
- **数据类型**: STRING
- **多重性**: [1..1]
- **符号名值**: false
- **需要索引**: false
- **字符串变体**:
  - 最小长度: 1
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Name of the generated function-like macro to set the given key element.

######## 2. SmhGetKeyElementMacroName

- **UUID**: `853cb6b4-3fcb-4bbc-b06f-f598eff5f348`
- **参数名**: `SmhGetKeyElementMacroName`
- **数据类型**: STRING
- **多重性**: [1..1]
- **符号名值**: false
- **需要索引**: false
- **字符串变体**:
  - 最小长度: 1
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Name of the generated function-like macro to get the given key element.

###### 引用关系

此容器包含 **2** 个引用：

####### REFERENCE 类型引用

######## 1. SmhCsmKeyRef

- **UUID**: `cbda49fd-2888-4be2-ad91-caf49aa9ffe1`
- **引用名**: `SmhCsmKeyRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `CsmKey`
- **完整路径**: `/AUTOSAR/EcucDefs/Csm/CsmKeys/CsmKey`
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Reference to the key in CSM

######## 2. SmhCryptographicKeyValueRef

- **UUID**: `2e2cdeed-44f0-47cd-9061-79282723ff26`
- **引用名**: `SmhCryptographicKeyValueRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `SmhKeyValue`
- **完整路径**: `/MICROSAR/Smh/SmhCryptographicKeys/SmhKeyValue`
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Reference to the key value in Smh

##### 39. SmhCopyKeyOperation

**容器属性**:

- **UUID**: `a982cf66-ee1b-4da3-a684-000d987ef32c`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SmhCopyKeyOperation`
- **多重性**: [0..infinite]
- **构建后可变**: false

**容器描述**:

Contains the configuration to copy complete keys

###### 参数配置

此容器包含 **1** 个参数：

####### STRING 类型参数

######## 1. SmhCopyKeyMacroName

- **UUID**: `dbe572ef-7967-432f-911b-7d8df3d59c61`
- **参数名**: `SmhCopyKeyMacroName`
- **数据类型**: STRING
- **多重性**: [1..1]
- **符号名值**: false
- **需要索引**: false
- **字符串变体**:
  - 最小长度: 1
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Name of the generated function-like macro to copy the given key.

###### 引用关系

此容器包含 **2** 个引用：

####### REFERENCE 类型引用

######## 1. SmhSourceCsmKeyRef

- **UUID**: `cb070f8c-2ca8-4d61-a3c7-762ea44201a5`
- **引用名**: `SmhSourceCsmKeyRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `CsmKey`
- **完整路径**: `/AUTOSAR/EcucDefs/Csm/CsmKeys/CsmKey`
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Reference to the source key in CSM

######## 2. SmhTargetCsmKeyRef

- **UUID**: `5e4d8d43-dc11-490a-bf45-d1f1cb83e19d`
- **引用名**: `SmhTargetCsmKeyRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `CsmKey`
- **完整路径**: `/AUTOSAR/EcucDefs/Csm/CsmKeys/CsmKey`
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Reference to the target key in CSM

##### 40. SmhCopyKeyElementOperation

**容器属性**:

- **UUID**: `afbed9cb-6e16-4fb3-b73a-fb2a96099db3`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SmhCopyKeyElementOperation`
- **多重性**: [0..infinite]
- **构建后可变**: false

**容器描述**:

Contains the configuration to copy keys elements

###### 参数配置

此容器包含 **1** 个参数：

####### STRING 类型参数

######## 1. SmhCopyKeyElementMacroName

- **UUID**: `e203688d-6233-49cd-b3b7-6cb3aa55818e`
- **参数名**: `SmhCopyKeyElementMacroName`
- **数据类型**: STRING
- **多重性**: [1..1]
- **符号名值**: false
- **需要索引**: false
- **字符串变体**:
  - 最小长度: 1
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Name of the generated function-like macro to copy the given key element.

###### 引用关系

此容器包含 **4** 个引用：

####### REFERENCE 类型引用

######## 1. SmhSourceCsmKeyRef

- **UUID**: `4f740df9-67f1-437b-b16a-a8c225621055`
- **引用名**: `SmhSourceCsmKeyRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `CsmKey`
- **完整路径**: `/AUTOSAR/EcucDefs/Csm/CsmKeys/CsmKey`
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Reference to the source key in CSM

######## 2. SmhTargetCsmKeyRef

- **UUID**: `1b73cb59-faa7-45c3-886f-f1b2f30648f9`
- **引用名**: `SmhTargetCsmKeyRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `CsmKey`
- **完整路径**: `/AUTOSAR/EcucDefs/Csm/CsmKeys/CsmKey`
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Reference to the target key in CSM

######## 3. SmhSourceCryptographicKeyValueRef

- **UUID**: `3aba8714-6394-418c-ad3d-99695b6ecd63`
- **引用名**: `SmhSourceCryptographicKeyValueRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `SmhKeyValue`
- **完整路径**: `/MICROSAR/Smh/SmhCryptographicKeys/SmhKeyValue`
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Reference to the source key value in Smh

######## 4. SmhTargetCryptographicKeyValueRef

- **UUID**: `9758e996-6669-4e79-b6e0-ada91e5745ec`
- **引用名**: `SmhTargetCryptographicKeyValueRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `SmhKeyValue`
- **完整路径**: `/MICROSAR/Smh/SmhCryptographicKeys/SmhKeyValue`
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Reference to the target key value in Smh

##### 41. SmhCrc

**容器属性**:

- **UUID**: `90fc53dd-83ce-4415-b570-c4ed6b10d9d4`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SmhCrc`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container to configure the CRC module

###### 参数配置

此容器包含 **1** 个参数：

####### ENUMERATION 类型参数

######## 1. SmhCRCType

- **UUID**: `955312ea-cf8e-4d05-a9b5-982e17720d55`
- **参数名**: `SmhCRCType`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRC_16_CCITT`
  - `CRC_32`
  - `CRC_64`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Select the default CRC algorithm. This default CRC will be used for CRCTotal, CRCWritten, SecM_VerifyChecksumCrc and SecM_ComputeCRC.

###### 配置容器

本模块包含 **3** 个配置容器：

####### 1. SmhCrc16

**容器属性**:

- **UUID**: `debe15bf-f292-4bb4-bdaf-a6d0774efdb7`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SmhCrc16`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container to configure the CRC16.

######## 参数配置

此容器包含 **5** 个参数：

######### INTEGER 类型参数

########## 1. SmhInitialValue

- **UUID**: `fa586886-581d-4236-a886-c5d2f2b3a1e2`
- **参数名**: `SmhInitialValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `65535`
- **取值范围**: [0..65535]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Initialization value for CRC.

########## 2. SmhPolynomial

- **UUID**: `b513a094-1eef-4c7b-b17a-b36a803babad`
- **参数名**: `SmhPolynomial`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `4129`
- **取值范围**: [0..65535]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Polynomial of the CRC calculation.
Default value is the CCITT CRC-16 standard.

########## 3. SmhComplementValue

- **UUID**: `cc097bef-ad69-496d-84ba-48eb2940a53b`
- **参数名**: `SmhComplementValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Finalization value for CRC.

######### ENUMERATION 类型参数

########## 1. SmhOptimization

- **UUID**: `d325ccff-4cba-4a6e-a5a5-7dc8e02b27e6`
- **参数名**: `SmhOptimization`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `SPEED`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `SIZE` (来源: Vector Informatik)
  - `SPEED` (来源: Vector Informatik)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Select the optimization of the CRC calculation.

########## 2. SmhMode

- **UUID**: `e3521e3f-73d6-4138-ad93-1f70b0828cdf`
- **参数名**: `SmhMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `NON_REFLECTED`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `REFLECTED`
  - `NON_REFLECTED`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Operation mode of the CRC calculation.

####### 2. SmhCrc32

**容器属性**:

- **UUID**: `74fc67b5-9ced-4ce5-aac6-47c8f14f4407`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SmhCrc32`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container to configure the CRC32.

######## 参数配置

此容器包含 **5** 个参数：

######### INTEGER 类型参数

########## 1. SmhInitialValue

- **UUID**: `b0621824-9b71-4911-8574-6384a6a1c1d5`
- **参数名**: `SmhInitialValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `4294967295`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Initialization value for CRC.

########## 2. SmhPolynomial

- **UUID**: `9789e33b-9c00-4e07-87eb-46339a22d332`
- **参数名**: `SmhPolynomial`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `3988292384`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Polynomial of the CRC calculation.
The default value is a reflected value and can be found in literature in reverse bit order: 0x04C11DB7.

########## 3. SmhComplementValue

- **UUID**: `51709a07-852a-4bbd-9fc7-79c362fa3a97`
- **参数名**: `SmhComplementValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `4294967295`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Finalization value for CRC.

######### ENUMERATION 类型参数

########## 1. SmhOptimization

- **UUID**: `49b8d017-d343-4ee9-97a8-d10935c68fbb`
- **参数名**: `SmhOptimization`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `SPEED`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `SIZE` (来源: Vector Informatik)
  - `SPEED` (来源: Vector Informatik)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Select the optimization of the CRC calculation.

########## 2. SmhMode

- **UUID**: `a93e733a-8a0f-43c9-84cf-53920b14df97`
- **参数名**: `SmhMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `REFLECTED`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `REFLECTED`
  - `NON_REFLECTED`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Operation mode of the CRC calculation.

####### 3. SmhCrc64

**容器属性**:

- **UUID**: `37023ec5-80cb-4d16-9096-07433240f0b6`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SmhCrc64`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container to configure the CRC64.

######## 参数配置

此容器包含 **5** 个参数：

######### INTEGER 类型参数

########## 1. SmhInitialValue

- **UUID**: `b76134f0-518a-4c4d-a228-87139703c66b`
- **参数名**: `SmhInitialValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..18446744073709551615]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Initialization value for CRC.

########## 2. SmhPolynomial

- **UUID**: `662d1e17-b020-45e2-ba67-9d2325f4b738`
- **参数名**: `SmhPolynomial`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `15564440312192434176`
- **取值范围**: [0..18446744073709551615]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Polynomial of the CRC calculation.
The default value is a reflected value and can be found in literature in reverse bit order: 0x1B.

########## 3. SmhComplementValue

- **UUID**: `8628363e-816f-4b0d-859a-3351580d3a72`
- **参数名**: `SmhComplementValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..18446744073709551615]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Finalization value for CRC.

######### ENUMERATION 类型参数

########## 1. SmhOptimization

- **UUID**: `4e0462fb-f941-408d-a758-35bb5b3864a7`
- **参数名**: `SmhOptimization`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `SPEED`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `SIZE` (来源: Vector Informatik)
  - `SPEED` (来源: Vector Informatik)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Select the optimization of the CRC calculation.

########## 2. SmhMode

- **UUID**: `7bc15470-b628-439c-9be1-2e8507c6749e`
- **参数名**: `SmhMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `REFLECTED`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `REFLECTED`
  - `NON_REFLECTED`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Operation mode of the CRC calculation.

##### 42. SmhCrc16

**容器属性**:

- **UUID**: `debe15bf-f292-4bb4-bdaf-a6d0774efdb7`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SmhCrc16`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container to configure the CRC16.

###### 参数配置

此容器包含 **5** 个参数：

####### INTEGER 类型参数

######## 1. SmhInitialValue

- **UUID**: `fa586886-581d-4236-a886-c5d2f2b3a1e2`
- **参数名**: `SmhInitialValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `65535`
- **取值范围**: [0..65535]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Initialization value for CRC.

######## 2. SmhPolynomial

- **UUID**: `b513a094-1eef-4c7b-b17a-b36a803babad`
- **参数名**: `SmhPolynomial`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `4129`
- **取值范围**: [0..65535]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Polynomial of the CRC calculation.
Default value is the CCITT CRC-16 standard.

######## 3. SmhComplementValue

- **UUID**: `cc097bef-ad69-496d-84ba-48eb2940a53b`
- **参数名**: `SmhComplementValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Finalization value for CRC.

####### ENUMERATION 类型参数

######## 1. SmhOptimization

- **UUID**: `d325ccff-4cba-4a6e-a5a5-7dc8e02b27e6`
- **参数名**: `SmhOptimization`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `SPEED`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `SIZE` (来源: Vector Informatik)
  - `SPEED` (来源: Vector Informatik)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Select the optimization of the CRC calculation.

######## 2. SmhMode

- **UUID**: `e3521e3f-73d6-4138-ad93-1f70b0828cdf`
- **参数名**: `SmhMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `NON_REFLECTED`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `REFLECTED`
  - `NON_REFLECTED`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Operation mode of the CRC calculation.

##### 43. SmhCrc32

**容器属性**:

- **UUID**: `74fc67b5-9ced-4ce5-aac6-47c8f14f4407`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SmhCrc32`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container to configure the CRC32.

###### 参数配置

此容器包含 **5** 个参数：

####### INTEGER 类型参数

######## 1. SmhInitialValue

- **UUID**: `b0621824-9b71-4911-8574-6384a6a1c1d5`
- **参数名**: `SmhInitialValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `4294967295`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Initialization value for CRC.

######## 2. SmhPolynomial

- **UUID**: `9789e33b-9c00-4e07-87eb-46339a22d332`
- **参数名**: `SmhPolynomial`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `3988292384`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Polynomial of the CRC calculation.
The default value is a reflected value and can be found in literature in reverse bit order: 0x04C11DB7.

######## 3. SmhComplementValue

- **UUID**: `51709a07-852a-4bbd-9fc7-79c362fa3a97`
- **参数名**: `SmhComplementValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `4294967295`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Finalization value for CRC.

####### ENUMERATION 类型参数

######## 1. SmhOptimization

- **UUID**: `49b8d017-d343-4ee9-97a8-d10935c68fbb`
- **参数名**: `SmhOptimization`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `SPEED`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `SIZE` (来源: Vector Informatik)
  - `SPEED` (来源: Vector Informatik)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Select the optimization of the CRC calculation.

######## 2. SmhMode

- **UUID**: `a93e733a-8a0f-43c9-84cf-53920b14df97`
- **参数名**: `SmhMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `REFLECTED`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `REFLECTED`
  - `NON_REFLECTED`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Operation mode of the CRC calculation.

##### 44. SmhCrc64

**容器属性**:

- **UUID**: `37023ec5-80cb-4d16-9096-07433240f0b6`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SmhCrc64`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container to configure the CRC64.

###### 参数配置

此容器包含 **5** 个参数：

####### INTEGER 类型参数

######## 1. SmhInitialValue

- **UUID**: `b76134f0-518a-4c4d-a228-87139703c66b`
- **参数名**: `SmhInitialValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..18446744073709551615]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Initialization value for CRC.

######## 2. SmhPolynomial

- **UUID**: `662d1e17-b020-45e2-ba67-9d2325f4b738`
- **参数名**: `SmhPolynomial`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `15564440312192434176`
- **取值范围**: [0..18446744073709551615]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Polynomial of the CRC calculation.
The default value is a reflected value and can be found in literature in reverse bit order: 0x1B.

######## 3. SmhComplementValue

- **UUID**: `8628363e-816f-4b0d-859a-3351580d3a72`
- **参数名**: `SmhComplementValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..18446744073709551615]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Finalization value for CRC.

####### ENUMERATION 类型参数

######## 1. SmhOptimization

- **UUID**: `4e0462fb-f941-408d-a758-35bb5b3864a7`
- **参数名**: `SmhOptimization`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `SPEED`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `SIZE` (来源: Vector Informatik)
  - `SPEED` (来源: Vector Informatik)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Select the optimization of the CRC calculation.

######## 2. SmhMode

- **UUID**: `7bc15470-b628-439c-9be1-2e8507c6749e`
- **参数名**: `SmhMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `REFLECTED`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `REFLECTED`
  - `NON_REFLECTED`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Operation mode of the CRC calculation.

##### 45. SmhJob

**容器属性**:

- **UUID**: `43146f85-53c3-46da-88b7-e88354c82ba1`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SmhJob`
- **多重性**: [0..infinite]
- **构建后可变**: false

**容器描述**:

Container for configuration of SmhJob. The container name serves as a symbolic name for the identifier of a job configuration.

###### 配置容器

本模块包含 **8** 个配置容器：

####### 1. SmhHash

**容器属性**:

- **UUID**: `289b53a9-b5a7-42a3-ad40-ed884889b78a`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SmhHash`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container for Hash configurations.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. SmhCsmJobRef

- **UUID**: `519ce0d0-9470-4a02-b231-613b9aae08e0`
- **引用名**: `SmhCsmJobRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `CsmJob`
- **完整路径**: `/AUTOSAR/EcucDefs/Csm/CsmJobs/CsmJob`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Reference to the associated CSM job.

####### 2. SmhEncryption

**容器属性**:

- **UUID**: `8ddca3a7-cd71-43f4-b927-ddd7922e6f14`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SmhEncryption`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container for Encryption configurations.

######## 引用关系

此容器包含 **2** 个引用：

######### REFERENCE 类型引用

########## 1. SmhCsmJobRef

- **UUID**: `01775b08-6b9a-499c-8872-c3850c44fc31`
- **引用名**: `SmhCsmJobRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `CsmJob`
- **完整路径**: `/AUTOSAR/EcucDefs/Csm/CsmJobs/CsmJob`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Reference to the associated CSM job.

########## 2. SmhCryptographicKeyRef

- **UUID**: `08ebe8e8-fd19-4d32-bd95-3268e842887b`
- **引用名**: `SmhCryptographicKeyRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `SmhKey`
- **完整路径**: `/MICROSAR/Smh/SmhCryptographicKeys/SmhKey`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Reference to the cryptographic key associated with this SmhJob.

If the reference is not present the security module is not able to initialize the CryptoKeyElements.

####### 3. SmhDecryption

**容器属性**:

- **UUID**: `43a2caf7-0c2f-44a1-976d-ef61c6896244`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SmhDecryption`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container for Decryption configurations.

######## 引用关系

此容器包含 **2** 个引用：

######### REFERENCE 类型引用

########## 1. SmhCsmJobRef

- **UUID**: `600293ec-0bc1-4fce-86c8-cbbae44d4f8c`
- **引用名**: `SmhCsmJobRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `CsmJob`
- **完整路径**: `/AUTOSAR/EcucDefs/Csm/CsmJobs/CsmJob`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Reference to the associated CSM job.

########## 2. SmhCryptographicKeyRef

- **UUID**: `33d32b30-40ab-4e42-a081-9805bf1da2e6`
- **引用名**: `SmhCryptographicKeyRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `SmhKey`
- **完整路径**: `/MICROSAR/Smh/SmhCryptographicKeys/SmhKey`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Reference to the cryptographic key associated with this SmhJob.

If the reference is not present the security module is not able to initialize the CryptoKeyElements.

####### 4. SmhMacGenerate

**容器属性**:

- **UUID**: `2b50bf5b-378b-4094-8edd-3979a4057cce`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SmhMacGenerate`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container for MacGenerate configurations.

######## 引用关系

此容器包含 **2** 个引用：

######### REFERENCE 类型引用

########## 1. SmhCsmJobRef

- **UUID**: `6e176739-2bc0-4aea-9c0d-458539683c40`
- **引用名**: `SmhCsmJobRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `CsmJob`
- **完整路径**: `/AUTOSAR/EcucDefs/Csm/CsmJobs/CsmJob`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Reference to the associated CSM job.

########## 2. SmhCryptographicKeyRef

- **UUID**: `e0a023eb-b9be-4cf4-87ab-cd0aac2faaa4`
- **引用名**: `SmhCryptographicKeyRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `SmhKey`
- **完整路径**: `/MICROSAR/Smh/SmhCryptographicKeys/SmhKey`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Reference to the cryptographic key associated with this SmhJob.

If the reference is not present the security module is not able to initialize the CryptoKeyElements.

####### 5. SmhMacVerify

**容器属性**:

- **UUID**: `9342664e-bd10-4e51-af19-ab6b4c2eeeef`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SmhMacVerify`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container for MacVerify configurations.

######## 引用关系

此容器包含 **2** 个引用：

######### REFERENCE 类型引用

########## 1. SmhCsmJobRef

- **UUID**: `26037155-ec6f-4993-bcbc-fead30d3fd72`
- **引用名**: `SmhCsmJobRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `CsmJob`
- **完整路径**: `/AUTOSAR/EcucDefs/Csm/CsmJobs/CsmJob`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Reference to the associated CSM job.

########## 2. SmhCryptographicKeyRef

- **UUID**: `b44f015c-77eb-4961-9d47-6d9a7f165638`
- **引用名**: `SmhCryptographicKeyRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `SmhKey`
- **完整路径**: `/MICROSAR/Smh/SmhCryptographicKeys/SmhKey`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Reference to the cryptographic key associated with this SmhJob.

If the reference is not present the security module is not able to initialize the CryptoKeyElements.

####### 6. SmhRandomGenerate

**容器属性**:

- **UUID**: `d263ac77-f9bf-4777-9b16-62252c5f9b55`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SmhRandomGenerate`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container for RandomGenerate configurations.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. SmhCsmJobRef

- **UUID**: `460bee4a-395c-48cf-b668-1a6e6e666cb4`
- **引用名**: `SmhCsmJobRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `CsmJob`
- **完整路径**: `/AUTOSAR/EcucDefs/Csm/CsmJobs/CsmJob`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Reference to the associated CSM job.

####### 7. SmhSignatureVerify

**容器属性**:

- **UUID**: `0c755268-3971-44a3-b107-382d13c1a148`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SmhSignatureVerify`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container for SignatureVerify configurations.

######## 引用关系

此容器包含 **2** 个引用：

######### REFERENCE 类型引用

########## 1. SmhCsmJobRef

- **UUID**: `4547dcb9-c2ed-42af-86a1-c1f3d7370a41`
- **引用名**: `SmhCsmJobRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `CsmJob`
- **完整路径**: `/AUTOSAR/EcucDefs/Csm/CsmJobs/CsmJob`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Reference to the associated CSM job.

########## 2. SmhCryptographicKeyRef

- **UUID**: `321c2ee7-d328-4546-b38e-d1a6f6f0c352`
- **引用名**: `SmhCryptographicKeyRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `SmhKey`
- **完整路径**: `/MICROSAR/Smh/SmhCryptographicKeys/SmhKey`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Reference to the cryptographic key associated with this SmhJob.

If the reference is not present the security module is not able to initialize the CryptoKeyElements.

####### 8. SmhRandomSeed

**容器属性**:

- **UUID**: `0b2d17b6-4c52-4baa-a65f-c71df85acd7a`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SmhRandomSeed`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container for RandomSeed configurations.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. SmhCsmKeyRef

- **UUID**: `8f271121-8682-4b19-a047-96c026e03e07`
- **引用名**: `SmhCsmKeyRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `CsmKey`
- **完整路径**: `/AUTOSAR/EcucDefs/Csm/CsmKeys/CsmKey`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Reference to the associated CSM key.

##### 46. SmhHash

**容器属性**:

- **UUID**: `289b53a9-b5a7-42a3-ad40-ed884889b78a`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SmhHash`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container for Hash configurations.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. SmhCsmJobRef

- **UUID**: `519ce0d0-9470-4a02-b231-613b9aae08e0`
- **引用名**: `SmhCsmJobRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `CsmJob`
- **完整路径**: `/AUTOSAR/EcucDefs/Csm/CsmJobs/CsmJob`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Reference to the associated CSM job.

##### 47. SmhEncryption

**容器属性**:

- **UUID**: `8ddca3a7-cd71-43f4-b927-ddd7922e6f14`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SmhEncryption`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container for Encryption configurations.

###### 引用关系

此容器包含 **2** 个引用：

####### REFERENCE 类型引用

######## 1. SmhCsmJobRef

- **UUID**: `01775b08-6b9a-499c-8872-c3850c44fc31`
- **引用名**: `SmhCsmJobRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `CsmJob`
- **完整路径**: `/AUTOSAR/EcucDefs/Csm/CsmJobs/CsmJob`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Reference to the associated CSM job.

######## 2. SmhCryptographicKeyRef

- **UUID**: `08ebe8e8-fd19-4d32-bd95-3268e842887b`
- **引用名**: `SmhCryptographicKeyRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `SmhKey`
- **完整路径**: `/MICROSAR/Smh/SmhCryptographicKeys/SmhKey`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Reference to the cryptographic key associated with this SmhJob.

If the reference is not present the security module is not able to initialize the CryptoKeyElements.

##### 48. SmhDecryption

**容器属性**:

- **UUID**: `43a2caf7-0c2f-44a1-976d-ef61c6896244`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SmhDecryption`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container for Decryption configurations.

###### 引用关系

此容器包含 **2** 个引用：

####### REFERENCE 类型引用

######## 1. SmhCsmJobRef

- **UUID**: `600293ec-0bc1-4fce-86c8-cbbae44d4f8c`
- **引用名**: `SmhCsmJobRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `CsmJob`
- **完整路径**: `/AUTOSAR/EcucDefs/Csm/CsmJobs/CsmJob`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Reference to the associated CSM job.

######## 2. SmhCryptographicKeyRef

- **UUID**: `33d32b30-40ab-4e42-a081-9805bf1da2e6`
- **引用名**: `SmhCryptographicKeyRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `SmhKey`
- **完整路径**: `/MICROSAR/Smh/SmhCryptographicKeys/SmhKey`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Reference to the cryptographic key associated with this SmhJob.

If the reference is not present the security module is not able to initialize the CryptoKeyElements.

##### 49. SmhMacGenerate

**容器属性**:

- **UUID**: `2b50bf5b-378b-4094-8edd-3979a4057cce`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SmhMacGenerate`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container for MacGenerate configurations.

###### 引用关系

此容器包含 **2** 个引用：

####### REFERENCE 类型引用

######## 1. SmhCsmJobRef

- **UUID**: `6e176739-2bc0-4aea-9c0d-458539683c40`
- **引用名**: `SmhCsmJobRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `CsmJob`
- **完整路径**: `/AUTOSAR/EcucDefs/Csm/CsmJobs/CsmJob`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Reference to the associated CSM job.

######## 2. SmhCryptographicKeyRef

- **UUID**: `e0a023eb-b9be-4cf4-87ab-cd0aac2faaa4`
- **引用名**: `SmhCryptographicKeyRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `SmhKey`
- **完整路径**: `/MICROSAR/Smh/SmhCryptographicKeys/SmhKey`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Reference to the cryptographic key associated with this SmhJob.

If the reference is not present the security module is not able to initialize the CryptoKeyElements.

##### 50. SmhMacVerify

**容器属性**:

- **UUID**: `9342664e-bd10-4e51-af19-ab6b4c2eeeef`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SmhMacVerify`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container for MacVerify configurations.

###### 引用关系

此容器包含 **2** 个引用：

####### REFERENCE 类型引用

######## 1. SmhCsmJobRef

- **UUID**: `26037155-ec6f-4993-bcbc-fead30d3fd72`
- **引用名**: `SmhCsmJobRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `CsmJob`
- **完整路径**: `/AUTOSAR/EcucDefs/Csm/CsmJobs/CsmJob`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Reference to the associated CSM job.

######## 2. SmhCryptographicKeyRef

- **UUID**: `b44f015c-77eb-4961-9d47-6d9a7f165638`
- **引用名**: `SmhCryptographicKeyRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `SmhKey`
- **完整路径**: `/MICROSAR/Smh/SmhCryptographicKeys/SmhKey`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Reference to the cryptographic key associated with this SmhJob.

If the reference is not present the security module is not able to initialize the CryptoKeyElements.

##### 51. SmhRandomGenerate

**容器属性**:

- **UUID**: `d263ac77-f9bf-4777-9b16-62252c5f9b55`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SmhRandomGenerate`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container for RandomGenerate configurations.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. SmhCsmJobRef

- **UUID**: `460bee4a-395c-48cf-b668-1a6e6e666cb4`
- **引用名**: `SmhCsmJobRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `CsmJob`
- **完整路径**: `/AUTOSAR/EcucDefs/Csm/CsmJobs/CsmJob`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Reference to the associated CSM job.

##### 52. SmhSignatureVerify

**容器属性**:

- **UUID**: `0c755268-3971-44a3-b107-382d13c1a148`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SmhSignatureVerify`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container for SignatureVerify configurations.

###### 引用关系

此容器包含 **2** 个引用：

####### REFERENCE 类型引用

######## 1. SmhCsmJobRef

- **UUID**: `4547dcb9-c2ed-42af-86a1-c1f3d7370a41`
- **引用名**: `SmhCsmJobRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `CsmJob`
- **完整路径**: `/AUTOSAR/EcucDefs/Csm/CsmJobs/CsmJob`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Reference to the associated CSM job.

######## 2. SmhCryptographicKeyRef

- **UUID**: `321c2ee7-d328-4546-b38e-d1a6f6f0c352`
- **引用名**: `SmhCryptographicKeyRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `SmhKey`
- **完整路径**: `/MICROSAR/Smh/SmhCryptographicKeys/SmhKey`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Reference to the cryptographic key associated with this SmhJob.

If the reference is not present the security module is not able to initialize the CryptoKeyElements.

##### 53. SmhRandomSeed

**容器属性**:

- **UUID**: `0b2d17b6-4c52-4baa-a65f-c71df85acd7a`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SmhRandomSeed`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container for RandomSeed configurations.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. SmhCsmKeyRef

- **UUID**: `8f271121-8682-4b19-a047-96c026e03e07`
- **引用名**: `SmhCsmKeyRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `CsmKey`
- **完整路径**: `/AUTOSAR/EcucDefs/Csm/CsmKeys/CsmKey`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Reference to the associated CSM key.

##### 54. SmhSeedGeneration

**容器属性**:

- **UUID**: `6198606c-04b9-421d-bafa-479b40d62f74`
- **容器类型**: CHOICE-CONTAINER
- **容器名称**: `SmhSeedGeneration`
- **多重性**: [1..1]
- **构建后可变**: false

**容器选择**:

- **SmhCsm**
  - UUID: `23fd0911-1898-4ccb-9f75-512f3580d061`
  - 描述: Container to configure a respecive SmhJob (CsmJob) to generate a seed.
- **SmhLcg**
  - UUID: `a66578b7-37b5-46e6-9d2b-eeff5e61ac57`
  - 描述: Container to configure the LCG (linear congruential generator) algorithm.

**容器描述**:

Specify the RNG algorithm

##### 55. SmhSecurityClassDDDType

**容器属性**:

- **UUID**: `d4091ae3-bc5f-49ed-aab5-4f51d555f432`
- **容器类型**: CHOICE-CONTAINER
- **容器名称**: `SmhSecurityClassDDDType`
- **多重性**: [1..1]
- **构建后可变**: false

**容器选择**:

- **SmhCrc**
  - UUID: `d77a32e4-ca21-4c5c-a0ec-75a6fae134fe`
  - 描述: Container to configure the CRC
- **SmhHash**
  - UUID: `860c29ac-feed-4843-be72-6b659b349d99`
  - 描述: Container to configure the hash

**容器描述**:

Specify the type of the security class DDD

## 📦 包结构

此ARXML文件包含 **1** 个包：

### 1. MICROSAR

- **UUID**: `ff55d029-386d-43a2-b3c2-dfef4c7a5e36`
- **包名称**: `MICROSAR`
- **包含元素数量**: 4

#### 包含的元素

##### BSW-IMPLEMENTATION 类型元素

1. **Smh_Impl**

##### ECUC-MODULE-DEF 类型元素

1. **Smh**

##### ECUC-MODULE-CONFIGURATION-VALUES 类型元素

1. **Smh_Pre**
2. **Smh_Rec**

## ⚡ 实现信息

此ARXML文件包含 **1** 个实现：

### 1. Smh_Impl

- **UUID**: `cfb19fd2-090b-4f2e-8420-8549d1f8cf11`
- **实现名称**: `Smh_Impl`
- **编程语言**: C
- **软件版本**: 2.09.00
- **供应商ID**: 30
- **AUTOSAR版本**: 4.00.03
- **代码生成器**: DaVinci Configurator

## ⚙️ 配置信息

此ARXML文件包含 **2** 个配置：

### 1. Smh_Pre

- **UUID**: `5b1b7264-c83d-4e21-b6e4-51a18475c2df`
- **配置名称**: `Smh_Pre`
- **定义引用**: `/MICROSAR/Smh`

### 2. Smh_Rec

- **UUID**: `853041df-252b-4097-a690-76892426e640`
- **配置名称**: `Smh_Rec`
- **定义引用**: `/MICROSAR/Smh`
