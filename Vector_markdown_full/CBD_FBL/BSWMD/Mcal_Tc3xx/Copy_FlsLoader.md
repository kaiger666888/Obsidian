# FlsLoader - 完整配置文档

*此文档由ARXML文件自动生成，采用层次化结构展示*

**生成时间**: 2025-06-16 14:48:12

## 📑 目录

- [📄 文件信息](#-文件信息)
- [🔧 模块定义](#-模块定义)
  - [FlsLoader](#flsloader)
- [📦 包结构](#-包结构)

## 📄 文件信息

### Schema信息
- **Schema位置**: `http://autosar.org/schema/r4.0 AUTOSAR_4-2-2.xsd`
- **命名空间**: `http://autosar.org/schema/r4.0`

## 🔧 模块定义

### 1. FlsLoader

#### 基本信息

- **UUID**: `DCE:820c8734-fcba-4a70-ade2-60935d2440cb`
- **模块名称**: `FlsLoader`
- **多重性**: [0..1]
- **支持的变体**:
  - VARIANT-PRE-COMPILE

#### 模块描述

Configuration of the FlsLoader module.

#### 版本历史

共有 **1** 个版本记录：

##### 1. 版本 4.2.2

- **发布日期**: 2014-10-31
- **发布者**: AUTOSAR

*此版本无详细变更记录*

#### 配置容器

本模块包含 **18** 个配置容器：

##### 1. FlsLoaderGeneral

**容器属性**:

- **UUID**: `DCE:39ad22fd-9140-41e4-b7ef-0fce20806dd8`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FlsLoaderGeneral`
- **多重性**: [0..1]

**容器描述**:

FlsLoader driver configuration.

###### 参数配置

此容器包含 **4** 个参数：

####### INTEGER 类型参数

######## 1. FlsLoaderCallOutTime

- **UUID**: `DCE:6a29d629-a176-45ba-a064-c94c873f39c2`
- **参数名**: `FlsLoaderCallOutTime`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `5000000`
- **取值范围**: [10000..4294967295]
- **来源**: INFINEON_AURIX2G
- **描述**: Specifies the maximum time in nanoseconds to wait before invoking call-out function to application

####### BOOLEAN 类型参数

######## 1. FlsLoaderDevErrorDetect

- **UUID**: `DCE:9c9bdd07-25ff-4a12-bd06-df38c2cd5c8f`
- **参数名**: `FlsLoaderDevErrorDetect`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `true`
- **来源**: INFINEON_AURIX2G
- **描述**: Preprocessor switch to enable/disable the FlsLoaderDevErrorDetect.

######## 2. FlsLoaderEnableLockCheck

- **UUID**: `DCE:6a29d629-d176-45ba-a064-c94c8733d9c2`
- **参数名**: `FlsLoaderEnableLockCheck`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **来源**: INFINEON_AURIX2G
- **描述**: Preprocessor switch to enable/disable the Lock Check functionality in Erase and Write API's.

####### FUNCTION-NAME 类型参数

######## 1. FlsLoaderCallOutFunction

- **UUID**: `ECUC:9a658f77-834b-4dd3-add7-59b968176e7d`
- **参数名**: `FlsLoaderCallOutFunction`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **函数变体**:
  - 默认值: `NULL_PTR`
- **描述**: User defined call out function. User can provide either a call out function name or address of call out function. Default value of NULL_PTR is considered as call out disabled.

##### 2. FlsLoaderOptionalApi

**容器属性**:

- **UUID**: `DCE:109b2e3b-0f4a-4315-89d4-d3ddeb193105`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FlsLoaderOptionalApi`
- **多重性**: [0..1]

**容器描述**:

FlsLoader driver optional API Configuration.

###### 参数配置

此容器包含 **3** 个参数：

####### BOOLEAN 类型参数

######## 1. FlsLoaderDeInitApi

- **UUID**: `DCE:3fc4c7b8-6345-4f67-a2f6-4037af1e3d83`
- **参数名**: `FlsLoaderDeInitApi`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **来源**: INFINEON_AURIX2G
- **描述**: Preprocessor switch to enable/disable the FlsLoader_DeInit API.

######## 2. FlsLoaderLockUnlockApi

- **UUID**: `DCE:1e7b66c7-46e8-4b32-9908-e28d89b897e3`
- **参数名**: `FlsLoaderLockUnlockApi`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **来源**: INFINEON_AURIX2G
- **描述**: Preprocessor switch to enable/disable the FlsLoader_Lock and FlsLoader_Unlock APIs

######## 3. FlsLoaderVersionInfoApi

- **UUID**: `DCE:1d80fd03-eadc-4a7f-96f5-4290fdab447f`
- **参数名**: `FlsLoaderVersionInfoApi`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **来源**: INFINEON_AURIX2G
- **描述**: Preprocessor switch to enable/disable the FlsLoader_GetVersionInfo API

##### 3. FlsLoaderPFLASHConfig

**容器属性**:

- **UUID**: `ECUC:d97c27ef-38b0-4bdf-8384-d10c0a3bba83`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FlsLoaderPFLASHConfig`
- **多重性**: [0..1]

**容器描述**:

This container contains the sub containers for each PFLASH Bank configuration.

###### 配置容器

本模块包含 **12** 个配置容器：

####### 1. FlsLoaderPFlash0ProtConfig

**容器属性**:

- **UUID**: `ECUC:6aa61659-c6de-4d25-8713-ac864fdf5e37`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FlsLoaderPFlash0ProtConfig`
- **多重性**: [0..1]

**容器描述**:

PFLASH Bank 0 protection configuration.

######## 参数配置

此容器包含 **9** 个参数：

######### INTEGER 类型参数

########## 1. FlsLoaderPFUcbPW0_0

- **UUID**: `e9afaa0c-2dc7-4390-a7c9-c605ae01c22f`
- **参数名**: `FlsLoaderPFUcbPW0_0`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: 1th least significant word password out of 8 words  password

########## 2. FlsLoaderPFUcbPW0_1

- **UUID**: `e9afaa0c-2dc7-4390-a7c9-c605ae01c22a`
- **参数名**: `FlsLoaderPFUcbPW0_1`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: 2nd least significant word password out of 8 words  password

########## 3. FlsLoaderPFUcbPW1_0

- **UUID**: `e9afaa0c-2dc7-4390-a7c9-c605ae01c23f`
- **参数名**: `FlsLoaderPFUcbPW1_0`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: 3rd least significant word password out of 8 words  password

########## 4. FlsLoaderPFUcbPW1_1

- **UUID**: `e9afaa0c-2dc7-4390-a7c9-c605ae01c32f`
- **参数名**: `FlsLoaderPFUcbPW1_1`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: 4th least significant word password out of 8 words  password

########## 5. FlsLoaderPFUcbPW2_0

- **UUID**: `7f8acec7-f9d9-421b-9d87-2fbf002b3364`
- **参数名**: `FlsLoaderPFUcbPW2_0`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: 5th least significant word password out of 8 words  password

########## 6. FlsLoaderPFUcbPW2_1

- **UUID**: `f158aeb5-c294-4e93-9d36-73b215c02563`
- **参数名**: `FlsLoaderPFUcbPW2_1`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: 6th least significant word password out of 8 words  password

########## 7. FlsLoaderPFUcbPW3_0

- **UUID**: `05f89bd5-22c2-4185-aafd-39b1a2715593`
- **参数名**: `FlsLoaderPFUcbPW3_0`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: 7th least significant word password out of 8 words  password

########## 8. FlsLoaderPFUcbPW3_1

- **UUID**: `a5242655-e895-4777-ab66-6b7ef366ab96`
- **参数名**: `FlsLoaderPFUcbPW3_1`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Most significant word password out of 8 words  password

######### ENUMERATION 类型参数

########## 1. FlsLoaderPFLash0WriteProt

- **UUID**: `6af99e0c-df9d-4f91-80c7-32a09a6f075b`
- **参数名**: `FlsLoaderPFLash0WriteProt`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `NO_PROTECTION`
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `NO_PROTECTION` (来源: INFINEON_AURIX2G)
  - `WRITE_PROTECTION` (来源: INFINEON_AURIX2G)
  - `OTP_PROTECTION` (来源: INFINEON_AURIX2G)
  - `WOP_PROTECTION` (来源: INFINEON_AURIX2G)
- **描述**: PFLASH Bank 0 protection configuration.

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. FlsLoaderPF0Sector

**容器属性**:

- **UUID**: `ECUC:1768f065-a030-4115-8de9-30b561da3ba3`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FlsLoaderPF0Sector`
- **多重性**: [192..192]

**容器描述**:

Configuration of the individual PF0 sectors.

########## 参数配置

此容器包含 **1** 个参数：

########### ENUMERATION 类型参数

############ 1. FlsLoaderPFSectorWriteProtection

- **UUID**: `bf3e4123-a208-4261-aaac-01e1bd166470`
- **参数名**: `FlsLoaderPFSectorWriteProtection`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `NO_PROTECTION`
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `NO_PROTECTION` (来源: INFINEON_AURIX2G)
  - `WRITE_PROTECTION` (来源: INFINEON_AURIX2G)
  - `OTP_PROTECTION` (来源: INFINEON_AURIX2G)
  - `WOP_PROTECTION` (来源: INFINEON_AURIX2G)
- **描述**: Sector Write protection.

####### 2. FlsLoaderPF0Sector

**容器属性**:

- **UUID**: `ECUC:1768f065-a030-4115-8de9-30b561da3ba3`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FlsLoaderPF0Sector`
- **多重性**: [192..192]

**容器描述**:

Configuration of the individual PF0 sectors.

######## 参数配置

此容器包含 **1** 个参数：

######### ENUMERATION 类型参数

########## 1. FlsLoaderPFSectorWriteProtection

- **UUID**: `bf3e4123-a208-4261-aaac-01e1bd166470`
- **参数名**: `FlsLoaderPFSectorWriteProtection`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `NO_PROTECTION`
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `NO_PROTECTION` (来源: INFINEON_AURIX2G)
  - `WRITE_PROTECTION` (来源: INFINEON_AURIX2G)
  - `OTP_PROTECTION` (来源: INFINEON_AURIX2G)
  - `WOP_PROTECTION` (来源: INFINEON_AURIX2G)
- **描述**: Sector Write protection.

####### 3. FlsLoaderPFlash1ProtConfig

**容器属性**:

- **UUID**: `ECUC:6aa61649-c6de-4d25-8713-ac866fdf5e37`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FlsLoaderPFlash1ProtConfig`
- **多重性**: [0..1]

**容器描述**:

PFLASH Bank 1 protection configuration.

######## 参数配置

此容器包含 **1** 个参数：

######### ENUMERATION 类型参数

########## 1. FlsLoaderPFLash1WriteProt

- **UUID**: `6af99e0c-df9d-7f91-80c7-32a49a6f075b`
- **参数名**: `FlsLoaderPFLash1WriteProt`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `NO_PROTECTION`
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `NO_PROTECTION` (来源: INFINEON_AURIX2G)
  - `WRITE_PROTECTION` (来源: INFINEON_AURIX2G)
  - `OTP_PROTECTION` (来源: INFINEON_AURIX2G)
  - `WOP_PROTECTION` (来源: INFINEON_AURIX2G)
- **描述**: PFlash Read/Write protection.

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. FlsLoaderPF1Sector

**容器属性**:

- **UUID**: `ECUC:1733f065-a030-4205-22e9-30b571da3ba3`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FlsLoaderPF1Sector`
- **多重性**: [192..192]

**容器描述**:

PFLASH Bank 1 sector protection configuration.

########## 参数配置

此容器包含 **1** 个参数：

########### ENUMERATION 类型参数

############ 1. FlsLoaderPFSectorWriteProtection

- **UUID**: `bf3e4123-a208-4061-aaac-01e124466470`
- **参数名**: `FlsLoaderPFSectorWriteProtection`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `NO_PROTECTION`
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `NO_PROTECTION` (来源: INFINEON_AURIX2G)
  - `WRITE_PROTECTION` (来源: INFINEON_AURIX2G)
  - `OTP_PROTECTION` (来源: INFINEON_AURIX2G)
  - `WOP_PROTECTION` (来源: INFINEON_AURIX2G)
- **描述**: Sector Write protection.

####### 4. FlsLoaderPF1Sector

**容器属性**:

- **UUID**: `ECUC:1733f065-a030-4205-22e9-30b571da3ba3`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FlsLoaderPF1Sector`
- **多重性**: [192..192]

**容器描述**:

PFLASH Bank 1 sector protection configuration.

######## 参数配置

此容器包含 **1** 个参数：

######### ENUMERATION 类型参数

########## 1. FlsLoaderPFSectorWriteProtection

- **UUID**: `bf3e4123-a208-4061-aaac-01e124466470`
- **参数名**: `FlsLoaderPFSectorWriteProtection`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `NO_PROTECTION`
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `NO_PROTECTION` (来源: INFINEON_AURIX2G)
  - `WRITE_PROTECTION` (来源: INFINEON_AURIX2G)
  - `OTP_PROTECTION` (来源: INFINEON_AURIX2G)
  - `WOP_PROTECTION` (来源: INFINEON_AURIX2G)
- **描述**: Sector Write protection.

####### 5. FlsLoaderPFlash2ProtConfig

**容器属性**:

- **UUID**: `ECUC:6aa61659-c6de-4d25-5713-ac862gdh5e37`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FlsLoaderPFlash2ProtConfig`
- **多重性**: [0..1]

**容器描述**:

PFLASH Bank 2 protection configuration.

######## 参数配置

此容器包含 **1** 个参数：

######### ENUMERATION 类型参数

########## 1. FlsLoaderPFLash2WriteProt

- **UUID**: `6af88e0c-df9d-4f91-80c7-10a09a6f075b`
- **参数名**: `FlsLoaderPFLash2WriteProt`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `NO_PROTECTION`
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `NO_PROTECTION` (来源: INFINEON_AURIX2G)
  - `WRITE_PROTECTION` (来源: INFINEON_AURIX2G)
  - `OTP_PROTECTION` (来源: INFINEON_AURIX2G)
  - `WOP_PROTECTION` (来源: INFINEON_AURIX2G)
- **描述**: PFlash Read/Write protection.

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. FlsLoaderPF2Sector

**容器属性**:

- **UUID**: `ECUC:1768f065-a030-4715-8de9-307761da3ba3`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FlsLoaderPF2Sector`
- **多重性**: [192..192]

**容器描述**:

PFLASH Bank 2 sector protection configuration.

########## 参数配置

此容器包含 **1** 个参数：

########### ENUMERATION 类型参数

############ 1. FlsLoaderPFSectorWriteProtection

- **UUID**: `bf3e4123-a208-4261-aaac-01e1cd166470`
- **参数名**: `FlsLoaderPFSectorWriteProtection`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `NO_PROTECTION`
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `NO_PROTECTION` (来源: INFINEON_AURIX2G)
  - `WRITE_PROTECTION` (来源: INFINEON_AURIX2G)
  - `OTP_PROTECTION` (来源: INFINEON_AURIX2G)
  - `WOP_PROTECTION` (来源: INFINEON_AURIX2G)
- **描述**: Sector Write protection.

####### 6. FlsLoaderPF2Sector

**容器属性**:

- **UUID**: `ECUC:1768f065-a030-4715-8de9-307761da3ba3`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FlsLoaderPF2Sector`
- **多重性**: [192..192]

**容器描述**:

PFLASH Bank 2 sector protection configuration.

######## 参数配置

此容器包含 **1** 个参数：

######### ENUMERATION 类型参数

########## 1. FlsLoaderPFSectorWriteProtection

- **UUID**: `bf3e4123-a208-4261-aaac-01e1cd166470`
- **参数名**: `FlsLoaderPFSectorWriteProtection`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `NO_PROTECTION`
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `NO_PROTECTION` (来源: INFINEON_AURIX2G)
  - `WRITE_PROTECTION` (来源: INFINEON_AURIX2G)
  - `OTP_PROTECTION` (来源: INFINEON_AURIX2G)
  - `WOP_PROTECTION` (来源: INFINEON_AURIX2G)
- **描述**: Sector Write protection.

####### 7. FlsLoaderPFlash3ProtConfig

**容器属性**:

- **UUID**: `ECUC:6aa61659-c6de-7725-8713-ac864fdf5e37`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FlsLoaderPFlash3ProtConfig`
- **多重性**: [0..1]

**容器描述**:

PFLASH Bank 3 protection configuration.

######## 参数配置

此容器包含 **1** 个参数：

######### ENUMERATION 类型参数

########## 1. FlsLoaderPFLash3WriteProt

- **UUID**: `6af99e0c-df7e-4f91-80c7-32a09a6f075b`
- **参数名**: `FlsLoaderPFLash3WriteProt`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `NO_PROTECTION`
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `NO_PROTECTION` (来源: INFINEON_AURIX2G)
  - `WRITE_PROTECTION` (来源: INFINEON_AURIX2G)
  - `OTP_PROTECTION` (来源: INFINEON_AURIX2G)
  - `WOP_PROTECTION` (来源: INFINEON_AURIX2G)
- **描述**: PFlash Read/Write protection.

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. FlsLoaderPF3Sector

**容器属性**:

- **UUID**: `ECUC:1768f065-a030-4205-8de9-30b561d55ba3`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FlsLoaderPF3Sector`
- **多重性**: [192..192]

**容器描述**:

PFLASH Bank 3 sector protection configuration.

########## 参数配置

此容器包含 **1** 个参数：

########### ENUMERATION 类型参数

############ 1. FlsLoaderPFSectorWriteProtection

- **UUID**: `bf3e4123-a208-4261-aaac-01e1ed166470`
- **参数名**: `FlsLoaderPFSectorWriteProtection`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `NO_PROTECTION`
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `NO_PROTECTION` (来源: INFINEON_AURIX2G)
  - `WRITE_PROTECTION` (来源: INFINEON_AURIX2G)
  - `OTP_PROTECTION` (来源: INFINEON_AURIX2G)
  - `WOP_PROTECTION` (来源: INFINEON_AURIX2G)
- **描述**: Sector Write protection.

####### 8. FlsLoaderPF3Sector

**容器属性**:

- **UUID**: `ECUC:1768f065-a030-4205-8de9-30b561d55ba3`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FlsLoaderPF3Sector`
- **多重性**: [192..192]

**容器描述**:

PFLASH Bank 3 sector protection configuration.

######## 参数配置

此容器包含 **1** 个参数：

######### ENUMERATION 类型参数

########## 1. FlsLoaderPFSectorWriteProtection

- **UUID**: `bf3e4123-a208-4261-aaac-01e1ed166470`
- **参数名**: `FlsLoaderPFSectorWriteProtection`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `NO_PROTECTION`
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `NO_PROTECTION` (来源: INFINEON_AURIX2G)
  - `WRITE_PROTECTION` (来源: INFINEON_AURIX2G)
  - `OTP_PROTECTION` (来源: INFINEON_AURIX2G)
  - `WOP_PROTECTION` (来源: INFINEON_AURIX2G)
- **描述**: Sector Write protection.

####### 9. FlsLoaderPFlash4ProtConfig

**容器属性**:

- **UUID**: `ECUC:6aa61659-c6de-4d25-8713-ac994fdf5e37`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FlsLoaderPFlash4ProtConfig`
- **多重性**: [0..1]

**容器描述**:

PFLASH Bank 4 protection configuration.

######## 参数配置

此容器包含 **1** 个参数：

######### ENUMERATION 类型参数

########## 1. FlsLoaderPFLash4WriteProt

- **UUID**: `6af99e0c-779d-4f91-80c7-32a09a6f075b`
- **参数名**: `FlsLoaderPFLash4WriteProt`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `NO_PROTECTION`
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `NO_PROTECTION` (来源: INFINEON_AURIX2G)
  - `WRITE_PROTECTION` (来源: INFINEON_AURIX2G)
  - `OTP_PROTECTION` (来源: INFINEON_AURIX2G)
  - `WOP_PROTECTION` (来源: INFINEON_AURIX2G)
- **描述**: PFlash Read/Write protection.

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. FlsLoaderPF4Sector

**容器属性**:

- **UUID**: `ECUC:1768f065-a030-4205-8de9-322861da3ba3`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FlsLoaderPF4Sector`
- **多重性**: [192..192]

**容器描述**:

PFLASH Bank 1 sector protection configuration.

########## 参数配置

此容器包含 **1** 个参数：

########### ENUMERATION 类型参数

############ 1. FlsLoaderPFSectorWriteProtection

- **UUID**: `bf3e4123-a208-4261-aaac-01e128166470`
- **参数名**: `FlsLoaderPFSectorWriteProtection`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `NO_PROTECTION`
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `NO_PROTECTION` (来源: INFINEON_AURIX2G)
  - `WRITE_PROTECTION` (来源: INFINEON_AURIX2G)
  - `OTP_PROTECTION` (来源: INFINEON_AURIX2G)
  - `WOP_PROTECTION` (来源: INFINEON_AURIX2G)
- **描述**: Sector Write protection.

####### 10. FlsLoaderPF4Sector

**容器属性**:

- **UUID**: `ECUC:1768f065-a030-4205-8de9-322861da3ba3`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FlsLoaderPF4Sector`
- **多重性**: [192..192]

**容器描述**:

PFLASH Bank 1 sector protection configuration.

######## 参数配置

此容器包含 **1** 个参数：

######### ENUMERATION 类型参数

########## 1. FlsLoaderPFSectorWriteProtection

- **UUID**: `bf3e4123-a208-4261-aaac-01e128166470`
- **参数名**: `FlsLoaderPFSectorWriteProtection`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `NO_PROTECTION`
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `NO_PROTECTION` (来源: INFINEON_AURIX2G)
  - `WRITE_PROTECTION` (来源: INFINEON_AURIX2G)
  - `OTP_PROTECTION` (来源: INFINEON_AURIX2G)
  - `WOP_PROTECTION` (来源: INFINEON_AURIX2G)
- **描述**: Sector Write protection.

####### 11. FlsLoaderPFlash5ProtConfig

**容器属性**:

- **UUID**: `ECUC:6aa61659-c6de-4d25-5513-ac864fdf5e37`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FlsLoaderPFlash5ProtConfig`
- **多重性**: [0..1]

**容器描述**:

PFLASH Bank 5 protection configuration.

######## 参数配置

此容器包含 **1** 个参数：

######### ENUMERATION 类型参数

########## 1. FlsLoaderPFLash5WriteProt

- **UUID**: `6af99e0c-df9d-1d91-80c7-32a09a6f075b`
- **参数名**: `FlsLoaderPFLash5WriteProt`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `NO_PROTECTION`
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `NO_PROTECTION` (来源: INFINEON_AURIX2G)
  - `WRITE_PROTECTION` (来源: INFINEON_AURIX2G)
  - `OTP_PROTECTION` (来源: INFINEON_AURIX2G)
  - `WOP_PROTECTION` (来源: INFINEON_AURIX2G)
- **描述**: PFlash Read/Write protection.

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. FlsLoaderPF5Sector

**容器属性**:

- **UUID**: `ECUC:1768f065-a030-4205-8de9-30b561da3ba3`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FlsLoaderPF5Sector`
- **多重性**: [64..64]

**容器描述**:

PFLASH Bank 5 sector protection configuration.

########## 参数配置

此容器包含 **1** 个参数：

########### ENUMERATION 类型参数

############ 1. FlsLoaderPFSectorWriteProtection

- **UUID**: `bf3e4123-a208-4261-aaac-01e12d166470`
- **参数名**: `FlsLoaderPFSectorWriteProtection`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `NO_PROTECTION`
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `NO_PROTECTION` (来源: INFINEON_AURIX2G)
  - `WRITE_PROTECTION` (来源: INFINEON_AURIX2G)
  - `OTP_PROTECTION` (来源: INFINEON_AURIX2G)
  - `WOP_PROTECTION` (来源: INFINEON_AURIX2G)
- **描述**: Sector Write protection.

####### 12. FlsLoaderPF5Sector

**容器属性**:

- **UUID**: `ECUC:1768f065-a030-4205-8de9-30b561da3ba3`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FlsLoaderPF5Sector`
- **多重性**: [64..64]

**容器描述**:

PFLASH Bank 5 sector protection configuration.

######## 参数配置

此容器包含 **1** 个参数：

######### ENUMERATION 类型参数

########## 1. FlsLoaderPFSectorWriteProtection

- **UUID**: `bf3e4123-a208-4261-aaac-01e12d166470`
- **参数名**: `FlsLoaderPFSectorWriteProtection`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `NO_PROTECTION`
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `NO_PROTECTION` (来源: INFINEON_AURIX2G)
  - `WRITE_PROTECTION` (来源: INFINEON_AURIX2G)
  - `OTP_PROTECTION` (来源: INFINEON_AURIX2G)
  - `WOP_PROTECTION` (来源: INFINEON_AURIX2G)
- **描述**: Sector Write protection.

##### 4. FlsLoaderPFlash0ProtConfig

**容器属性**:

- **UUID**: `ECUC:6aa61659-c6de-4d25-8713-ac864fdf5e37`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FlsLoaderPFlash0ProtConfig`
- **多重性**: [0..1]

**容器描述**:

PFLASH Bank 0 protection configuration.

###### 参数配置

此容器包含 **9** 个参数：

####### INTEGER 类型参数

######## 1. FlsLoaderPFUcbPW0_0

- **UUID**: `e9afaa0c-2dc7-4390-a7c9-c605ae01c22f`
- **参数名**: `FlsLoaderPFUcbPW0_0`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: 1th least significant word password out of 8 words  password

######## 2. FlsLoaderPFUcbPW0_1

- **UUID**: `e9afaa0c-2dc7-4390-a7c9-c605ae01c22a`
- **参数名**: `FlsLoaderPFUcbPW0_1`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: 2nd least significant word password out of 8 words  password

######## 3. FlsLoaderPFUcbPW1_0

- **UUID**: `e9afaa0c-2dc7-4390-a7c9-c605ae01c23f`
- **参数名**: `FlsLoaderPFUcbPW1_0`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: 3rd least significant word password out of 8 words  password

######## 4. FlsLoaderPFUcbPW1_1

- **UUID**: `e9afaa0c-2dc7-4390-a7c9-c605ae01c32f`
- **参数名**: `FlsLoaderPFUcbPW1_1`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: 4th least significant word password out of 8 words  password

######## 5. FlsLoaderPFUcbPW2_0

- **UUID**: `7f8acec7-f9d9-421b-9d87-2fbf002b3364`
- **参数名**: `FlsLoaderPFUcbPW2_0`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: 5th least significant word password out of 8 words  password

######## 6. FlsLoaderPFUcbPW2_1

- **UUID**: `f158aeb5-c294-4e93-9d36-73b215c02563`
- **参数名**: `FlsLoaderPFUcbPW2_1`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: 6th least significant word password out of 8 words  password

######## 7. FlsLoaderPFUcbPW3_0

- **UUID**: `05f89bd5-22c2-4185-aafd-39b1a2715593`
- **参数名**: `FlsLoaderPFUcbPW3_0`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: 7th least significant word password out of 8 words  password

######## 8. FlsLoaderPFUcbPW3_1

- **UUID**: `a5242655-e895-4777-ab66-6b7ef366ab96`
- **参数名**: `FlsLoaderPFUcbPW3_1`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Most significant word password out of 8 words  password

####### ENUMERATION 类型参数

######## 1. FlsLoaderPFLash0WriteProt

- **UUID**: `6af99e0c-df9d-4f91-80c7-32a09a6f075b`
- **参数名**: `FlsLoaderPFLash0WriteProt`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `NO_PROTECTION`
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `NO_PROTECTION` (来源: INFINEON_AURIX2G)
  - `WRITE_PROTECTION` (来源: INFINEON_AURIX2G)
  - `OTP_PROTECTION` (来源: INFINEON_AURIX2G)
  - `WOP_PROTECTION` (来源: INFINEON_AURIX2G)
- **描述**: PFLASH Bank 0 protection configuration.

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. FlsLoaderPF0Sector

**容器属性**:

- **UUID**: `ECUC:1768f065-a030-4115-8de9-30b561da3ba3`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FlsLoaderPF0Sector`
- **多重性**: [192..192]

**容器描述**:

Configuration of the individual PF0 sectors.

######## 参数配置

此容器包含 **1** 个参数：

######### ENUMERATION 类型参数

########## 1. FlsLoaderPFSectorWriteProtection

- **UUID**: `bf3e4123-a208-4261-aaac-01e1bd166470`
- **参数名**: `FlsLoaderPFSectorWriteProtection`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `NO_PROTECTION`
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `NO_PROTECTION` (来源: INFINEON_AURIX2G)
  - `WRITE_PROTECTION` (来源: INFINEON_AURIX2G)
  - `OTP_PROTECTION` (来源: INFINEON_AURIX2G)
  - `WOP_PROTECTION` (来源: INFINEON_AURIX2G)
- **描述**: Sector Write protection.

##### 5. FlsLoaderPF0Sector

**容器属性**:

- **UUID**: `ECUC:1768f065-a030-4115-8de9-30b561da3ba3`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FlsLoaderPF0Sector`
- **多重性**: [192..192]

**容器描述**:

Configuration of the individual PF0 sectors.

###### 参数配置

此容器包含 **1** 个参数：

####### ENUMERATION 类型参数

######## 1. FlsLoaderPFSectorWriteProtection

- **UUID**: `bf3e4123-a208-4261-aaac-01e1bd166470`
- **参数名**: `FlsLoaderPFSectorWriteProtection`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `NO_PROTECTION`
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `NO_PROTECTION` (来源: INFINEON_AURIX2G)
  - `WRITE_PROTECTION` (来源: INFINEON_AURIX2G)
  - `OTP_PROTECTION` (来源: INFINEON_AURIX2G)
  - `WOP_PROTECTION` (来源: INFINEON_AURIX2G)
- **描述**: Sector Write protection.

##### 6. FlsLoaderPFlash1ProtConfig

**容器属性**:

- **UUID**: `ECUC:6aa61649-c6de-4d25-8713-ac866fdf5e37`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FlsLoaderPFlash1ProtConfig`
- **多重性**: [0..1]

**容器描述**:

PFLASH Bank 1 protection configuration.

###### 参数配置

此容器包含 **1** 个参数：

####### ENUMERATION 类型参数

######## 1. FlsLoaderPFLash1WriteProt

- **UUID**: `6af99e0c-df9d-7f91-80c7-32a49a6f075b`
- **参数名**: `FlsLoaderPFLash1WriteProt`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `NO_PROTECTION`
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `NO_PROTECTION` (来源: INFINEON_AURIX2G)
  - `WRITE_PROTECTION` (来源: INFINEON_AURIX2G)
  - `OTP_PROTECTION` (来源: INFINEON_AURIX2G)
  - `WOP_PROTECTION` (来源: INFINEON_AURIX2G)
- **描述**: PFlash Read/Write protection.

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. FlsLoaderPF1Sector

**容器属性**:

- **UUID**: `ECUC:1733f065-a030-4205-22e9-30b571da3ba3`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FlsLoaderPF1Sector`
- **多重性**: [192..192]

**容器描述**:

PFLASH Bank 1 sector protection configuration.

######## 参数配置

此容器包含 **1** 个参数：

######### ENUMERATION 类型参数

########## 1. FlsLoaderPFSectorWriteProtection

- **UUID**: `bf3e4123-a208-4061-aaac-01e124466470`
- **参数名**: `FlsLoaderPFSectorWriteProtection`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `NO_PROTECTION`
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `NO_PROTECTION` (来源: INFINEON_AURIX2G)
  - `WRITE_PROTECTION` (来源: INFINEON_AURIX2G)
  - `OTP_PROTECTION` (来源: INFINEON_AURIX2G)
  - `WOP_PROTECTION` (来源: INFINEON_AURIX2G)
- **描述**: Sector Write protection.

##### 7. FlsLoaderPF1Sector

**容器属性**:

- **UUID**: `ECUC:1733f065-a030-4205-22e9-30b571da3ba3`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FlsLoaderPF1Sector`
- **多重性**: [192..192]

**容器描述**:

PFLASH Bank 1 sector protection configuration.

###### 参数配置

此容器包含 **1** 个参数：

####### ENUMERATION 类型参数

######## 1. FlsLoaderPFSectorWriteProtection

- **UUID**: `bf3e4123-a208-4061-aaac-01e124466470`
- **参数名**: `FlsLoaderPFSectorWriteProtection`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `NO_PROTECTION`
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `NO_PROTECTION` (来源: INFINEON_AURIX2G)
  - `WRITE_PROTECTION` (来源: INFINEON_AURIX2G)
  - `OTP_PROTECTION` (来源: INFINEON_AURIX2G)
  - `WOP_PROTECTION` (来源: INFINEON_AURIX2G)
- **描述**: Sector Write protection.

##### 8. FlsLoaderPFlash2ProtConfig

**容器属性**:

- **UUID**: `ECUC:6aa61659-c6de-4d25-5713-ac862gdh5e37`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FlsLoaderPFlash2ProtConfig`
- **多重性**: [0..1]

**容器描述**:

PFLASH Bank 2 protection configuration.

###### 参数配置

此容器包含 **1** 个参数：

####### ENUMERATION 类型参数

######## 1. FlsLoaderPFLash2WriteProt

- **UUID**: `6af88e0c-df9d-4f91-80c7-10a09a6f075b`
- **参数名**: `FlsLoaderPFLash2WriteProt`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `NO_PROTECTION`
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `NO_PROTECTION` (来源: INFINEON_AURIX2G)
  - `WRITE_PROTECTION` (来源: INFINEON_AURIX2G)
  - `OTP_PROTECTION` (来源: INFINEON_AURIX2G)
  - `WOP_PROTECTION` (来源: INFINEON_AURIX2G)
- **描述**: PFlash Read/Write protection.

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. FlsLoaderPF2Sector

**容器属性**:

- **UUID**: `ECUC:1768f065-a030-4715-8de9-307761da3ba3`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FlsLoaderPF2Sector`
- **多重性**: [192..192]

**容器描述**:

PFLASH Bank 2 sector protection configuration.

######## 参数配置

此容器包含 **1** 个参数：

######### ENUMERATION 类型参数

########## 1. FlsLoaderPFSectorWriteProtection

- **UUID**: `bf3e4123-a208-4261-aaac-01e1cd166470`
- **参数名**: `FlsLoaderPFSectorWriteProtection`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `NO_PROTECTION`
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `NO_PROTECTION` (来源: INFINEON_AURIX2G)
  - `WRITE_PROTECTION` (来源: INFINEON_AURIX2G)
  - `OTP_PROTECTION` (来源: INFINEON_AURIX2G)
  - `WOP_PROTECTION` (来源: INFINEON_AURIX2G)
- **描述**: Sector Write protection.

##### 9. FlsLoaderPF2Sector

**容器属性**:

- **UUID**: `ECUC:1768f065-a030-4715-8de9-307761da3ba3`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FlsLoaderPF2Sector`
- **多重性**: [192..192]

**容器描述**:

PFLASH Bank 2 sector protection configuration.

###### 参数配置

此容器包含 **1** 个参数：

####### ENUMERATION 类型参数

######## 1. FlsLoaderPFSectorWriteProtection

- **UUID**: `bf3e4123-a208-4261-aaac-01e1cd166470`
- **参数名**: `FlsLoaderPFSectorWriteProtection`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `NO_PROTECTION`
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `NO_PROTECTION` (来源: INFINEON_AURIX2G)
  - `WRITE_PROTECTION` (来源: INFINEON_AURIX2G)
  - `OTP_PROTECTION` (来源: INFINEON_AURIX2G)
  - `WOP_PROTECTION` (来源: INFINEON_AURIX2G)
- **描述**: Sector Write protection.

##### 10. FlsLoaderPFlash3ProtConfig

**容器属性**:

- **UUID**: `ECUC:6aa61659-c6de-7725-8713-ac864fdf5e37`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FlsLoaderPFlash3ProtConfig`
- **多重性**: [0..1]

**容器描述**:

PFLASH Bank 3 protection configuration.

###### 参数配置

此容器包含 **1** 个参数：

####### ENUMERATION 类型参数

######## 1. FlsLoaderPFLash3WriteProt

- **UUID**: `6af99e0c-df7e-4f91-80c7-32a09a6f075b`
- **参数名**: `FlsLoaderPFLash3WriteProt`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `NO_PROTECTION`
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `NO_PROTECTION` (来源: INFINEON_AURIX2G)
  - `WRITE_PROTECTION` (来源: INFINEON_AURIX2G)
  - `OTP_PROTECTION` (来源: INFINEON_AURIX2G)
  - `WOP_PROTECTION` (来源: INFINEON_AURIX2G)
- **描述**: PFlash Read/Write protection.

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. FlsLoaderPF3Sector

**容器属性**:

- **UUID**: `ECUC:1768f065-a030-4205-8de9-30b561d55ba3`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FlsLoaderPF3Sector`
- **多重性**: [192..192]

**容器描述**:

PFLASH Bank 3 sector protection configuration.

######## 参数配置

此容器包含 **1** 个参数：

######### ENUMERATION 类型参数

########## 1. FlsLoaderPFSectorWriteProtection

- **UUID**: `bf3e4123-a208-4261-aaac-01e1ed166470`
- **参数名**: `FlsLoaderPFSectorWriteProtection`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `NO_PROTECTION`
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `NO_PROTECTION` (来源: INFINEON_AURIX2G)
  - `WRITE_PROTECTION` (来源: INFINEON_AURIX2G)
  - `OTP_PROTECTION` (来源: INFINEON_AURIX2G)
  - `WOP_PROTECTION` (来源: INFINEON_AURIX2G)
- **描述**: Sector Write protection.

##### 11. FlsLoaderPF3Sector

**容器属性**:

- **UUID**: `ECUC:1768f065-a030-4205-8de9-30b561d55ba3`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FlsLoaderPF3Sector`
- **多重性**: [192..192]

**容器描述**:

PFLASH Bank 3 sector protection configuration.

###### 参数配置

此容器包含 **1** 个参数：

####### ENUMERATION 类型参数

######## 1. FlsLoaderPFSectorWriteProtection

- **UUID**: `bf3e4123-a208-4261-aaac-01e1ed166470`
- **参数名**: `FlsLoaderPFSectorWriteProtection`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `NO_PROTECTION`
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `NO_PROTECTION` (来源: INFINEON_AURIX2G)
  - `WRITE_PROTECTION` (来源: INFINEON_AURIX2G)
  - `OTP_PROTECTION` (来源: INFINEON_AURIX2G)
  - `WOP_PROTECTION` (来源: INFINEON_AURIX2G)
- **描述**: Sector Write protection.

##### 12. FlsLoaderPFlash4ProtConfig

**容器属性**:

- **UUID**: `ECUC:6aa61659-c6de-4d25-8713-ac994fdf5e37`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FlsLoaderPFlash4ProtConfig`
- **多重性**: [0..1]

**容器描述**:

PFLASH Bank 4 protection configuration.

###### 参数配置

此容器包含 **1** 个参数：

####### ENUMERATION 类型参数

######## 1. FlsLoaderPFLash4WriteProt

- **UUID**: `6af99e0c-779d-4f91-80c7-32a09a6f075b`
- **参数名**: `FlsLoaderPFLash4WriteProt`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `NO_PROTECTION`
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `NO_PROTECTION` (来源: INFINEON_AURIX2G)
  - `WRITE_PROTECTION` (来源: INFINEON_AURIX2G)
  - `OTP_PROTECTION` (来源: INFINEON_AURIX2G)
  - `WOP_PROTECTION` (来源: INFINEON_AURIX2G)
- **描述**: PFlash Read/Write protection.

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. FlsLoaderPF4Sector

**容器属性**:

- **UUID**: `ECUC:1768f065-a030-4205-8de9-322861da3ba3`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FlsLoaderPF4Sector`
- **多重性**: [192..192]

**容器描述**:

PFLASH Bank 1 sector protection configuration.

######## 参数配置

此容器包含 **1** 个参数：

######### ENUMERATION 类型参数

########## 1. FlsLoaderPFSectorWriteProtection

- **UUID**: `bf3e4123-a208-4261-aaac-01e128166470`
- **参数名**: `FlsLoaderPFSectorWriteProtection`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `NO_PROTECTION`
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `NO_PROTECTION` (来源: INFINEON_AURIX2G)
  - `WRITE_PROTECTION` (来源: INFINEON_AURIX2G)
  - `OTP_PROTECTION` (来源: INFINEON_AURIX2G)
  - `WOP_PROTECTION` (来源: INFINEON_AURIX2G)
- **描述**: Sector Write protection.

##### 13. FlsLoaderPF4Sector

**容器属性**:

- **UUID**: `ECUC:1768f065-a030-4205-8de9-322861da3ba3`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FlsLoaderPF4Sector`
- **多重性**: [192..192]

**容器描述**:

PFLASH Bank 1 sector protection configuration.

###### 参数配置

此容器包含 **1** 个参数：

####### ENUMERATION 类型参数

######## 1. FlsLoaderPFSectorWriteProtection

- **UUID**: `bf3e4123-a208-4261-aaac-01e128166470`
- **参数名**: `FlsLoaderPFSectorWriteProtection`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `NO_PROTECTION`
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `NO_PROTECTION` (来源: INFINEON_AURIX2G)
  - `WRITE_PROTECTION` (来源: INFINEON_AURIX2G)
  - `OTP_PROTECTION` (来源: INFINEON_AURIX2G)
  - `WOP_PROTECTION` (来源: INFINEON_AURIX2G)
- **描述**: Sector Write protection.

##### 14. FlsLoaderPFlash5ProtConfig

**容器属性**:

- **UUID**: `ECUC:6aa61659-c6de-4d25-5513-ac864fdf5e37`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FlsLoaderPFlash5ProtConfig`
- **多重性**: [0..1]

**容器描述**:

PFLASH Bank 5 protection configuration.

###### 参数配置

此容器包含 **1** 个参数：

####### ENUMERATION 类型参数

######## 1. FlsLoaderPFLash5WriteProt

- **UUID**: `6af99e0c-df9d-1d91-80c7-32a09a6f075b`
- **参数名**: `FlsLoaderPFLash5WriteProt`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `NO_PROTECTION`
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `NO_PROTECTION` (来源: INFINEON_AURIX2G)
  - `WRITE_PROTECTION` (来源: INFINEON_AURIX2G)
  - `OTP_PROTECTION` (来源: INFINEON_AURIX2G)
  - `WOP_PROTECTION` (来源: INFINEON_AURIX2G)
- **描述**: PFlash Read/Write protection.

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. FlsLoaderPF5Sector

**容器属性**:

- **UUID**: `ECUC:1768f065-a030-4205-8de9-30b561da3ba3`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FlsLoaderPF5Sector`
- **多重性**: [64..64]

**容器描述**:

PFLASH Bank 5 sector protection configuration.

######## 参数配置

此容器包含 **1** 个参数：

######### ENUMERATION 类型参数

########## 1. FlsLoaderPFSectorWriteProtection

- **UUID**: `bf3e4123-a208-4261-aaac-01e12d166470`
- **参数名**: `FlsLoaderPFSectorWriteProtection`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `NO_PROTECTION`
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `NO_PROTECTION` (来源: INFINEON_AURIX2G)
  - `WRITE_PROTECTION` (来源: INFINEON_AURIX2G)
  - `OTP_PROTECTION` (来源: INFINEON_AURIX2G)
  - `WOP_PROTECTION` (来源: INFINEON_AURIX2G)
- **描述**: Sector Write protection.

##### 15. FlsLoaderPF5Sector

**容器属性**:

- **UUID**: `ECUC:1768f065-a030-4205-8de9-30b561da3ba3`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FlsLoaderPF5Sector`
- **多重性**: [64..64]

**容器描述**:

PFLASH Bank 5 sector protection configuration.

###### 参数配置

此容器包含 **1** 个参数：

####### ENUMERATION 类型参数

######## 1. FlsLoaderPFSectorWriteProtection

- **UUID**: `bf3e4123-a208-4261-aaac-01e12d166470`
- **参数名**: `FlsLoaderPFSectorWriteProtection`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `NO_PROTECTION`
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `NO_PROTECTION` (来源: INFINEON_AURIX2G)
  - `WRITE_PROTECTION` (来源: INFINEON_AURIX2G)
  - `OTP_PROTECTION` (来源: INFINEON_AURIX2G)
  - `WOP_PROTECTION` (来源: INFINEON_AURIX2G)
- **描述**: Sector Write protection.

##### 16. FlsLoaderDFLASHConfig

**容器属性**:

- **UUID**: `ECUC:d93c27ef-38b0-4bdf-8384-d10c0a3bba83`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FlsLoaderDFLASHConfig`
- **多重性**: [0..1]

**容器描述**:

This container contains the configuration parameters and sub containers of the FlsLoader module.

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. FlsLoaderDFlash0ProtConfig

**容器属性**:

- **UUID**: `DCE:108b2e3b-0f4a-4315-89d4-d3ddeb193116`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FlsLoaderDFlash0ProtConfig`
- **多重性**: [0..1]

**容器描述**:

DF protection configuration.

######## 参数配置

此容器包含 **9** 个参数：

######### INTEGER 类型参数

########## 1. FlsLoaderDF0UcbPW0_0

- **UUID**: `e9afaa0c-2dc7-4390-a7c9-c615ae01c46a`
- **参数名**: `FlsLoaderDF0UcbPW0_0`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: 1st least significant word password out of 8 words  password

########## 2. FlsLoaderDF0UcbPW0_1

- **UUID**: `e9afaa0c-2dc7-4390-a7c9-c305ae01c26f`
- **参数名**: `FlsLoaderDF0UcbPW0_1`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: 2nd least significant word password out of 8 words  password

########## 3. FlsLoaderDF0UcbPW1_0

- **UUID**: `e9afaa0c-2dc7-4390-a7c9-c905ae01d34f`
- **参数名**: `FlsLoaderDF0UcbPW1_0`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: 3rd least significant word password out of 8 words  password

########## 4. FlsLoaderDF0UcbPW1_1

- **UUID**: `e9afaa0c-2dc7-4390-a7c9-c805ae02c33f`
- **参数名**: `FlsLoaderDF0UcbPW1_1`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: 4th least significant word password out of 8 words  password

########## 5. FlsLoaderDF0UcbPW2_0

- **UUID**: `e9afaa0c-2dc7-4394-a7c9-c615ae01c46a`
- **参数名**: `FlsLoaderDF0UcbPW2_0`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: 5th least significant word password out of 8 words  password

########## 6. FlsLoaderDF0UcbPW2_1

- **UUID**: `e9afaa0c-2dc7-4393-a7c9-c305ae01c26f`
- **参数名**: `FlsLoaderDF0UcbPW2_1`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: 6th least significant word password out of 8 words  password

########## 7. FlsLoaderDF0UcbPW3_0

- **UUID**: `e9afaa0c-2dc7-4392-a7c9-c905ae01d34f`
- **参数名**: `FlsLoaderDF0UcbPW3_0`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: 7th least significant word password out of 8 words  password

########## 8. FlsLoaderDF0UcbPW3_1

- **UUID**: `e9afaa0c-2dc7-4391-a7c9-c805ae02c33f`
- **参数名**: `FlsLoaderDF0UcbPW3_1`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Most significant word password out of 8 words  password

######### ENUMERATION 类型参数

########## 1. FlsLoaderDF0Prot

- **UUID**: `c37e5f8c-2ef2-472a-98b5-dcc18cbea5cd`
- **参数名**: `FlsLoaderDF0Prot`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `NO_PROTECTION`
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `NO_PROTECTION` (来源: INFINEON_AURIX2G)
  - `READ_PROTECTION` (来源: INFINEON_AURIX2G)
  - `WRITE_PROTECTION` (来源: INFINEON_AURIX2G)
- **描述**: DF0 Read/Write protection.

##### 17. FlsLoaderDFlash0ProtConfig

**容器属性**:

- **UUID**: `DCE:108b2e3b-0f4a-4315-89d4-d3ddeb193116`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FlsLoaderDFlash0ProtConfig`
- **多重性**: [0..1]

**容器描述**:

DF protection configuration.

###### 参数配置

此容器包含 **9** 个参数：

####### INTEGER 类型参数

######## 1. FlsLoaderDF0UcbPW0_0

- **UUID**: `e9afaa0c-2dc7-4390-a7c9-c615ae01c46a`
- **参数名**: `FlsLoaderDF0UcbPW0_0`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: 1st least significant word password out of 8 words  password

######## 2. FlsLoaderDF0UcbPW0_1

- **UUID**: `e9afaa0c-2dc7-4390-a7c9-c305ae01c26f`
- **参数名**: `FlsLoaderDF0UcbPW0_1`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: 2nd least significant word password out of 8 words  password

######## 3. FlsLoaderDF0UcbPW1_0

- **UUID**: `e9afaa0c-2dc7-4390-a7c9-c905ae01d34f`
- **参数名**: `FlsLoaderDF0UcbPW1_0`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: 3rd least significant word password out of 8 words  password

######## 4. FlsLoaderDF0UcbPW1_1

- **UUID**: `e9afaa0c-2dc7-4390-a7c9-c805ae02c33f`
- **参数名**: `FlsLoaderDF0UcbPW1_1`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: 4th least significant word password out of 8 words  password

######## 5. FlsLoaderDF0UcbPW2_0

- **UUID**: `e9afaa0c-2dc7-4394-a7c9-c615ae01c46a`
- **参数名**: `FlsLoaderDF0UcbPW2_0`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: 5th least significant word password out of 8 words  password

######## 6. FlsLoaderDF0UcbPW2_1

- **UUID**: `e9afaa0c-2dc7-4393-a7c9-c305ae01c26f`
- **参数名**: `FlsLoaderDF0UcbPW2_1`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: 6th least significant word password out of 8 words  password

######## 7. FlsLoaderDF0UcbPW3_0

- **UUID**: `e9afaa0c-2dc7-4392-a7c9-c905ae01d34f`
- **参数名**: `FlsLoaderDF0UcbPW3_0`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: 7th least significant word password out of 8 words  password

######## 8. FlsLoaderDF0UcbPW3_1

- **UUID**: `e9afaa0c-2dc7-4391-a7c9-c805ae02c33f`
- **参数名**: `FlsLoaderDF0UcbPW3_1`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Most significant word password out of 8 words  password

####### ENUMERATION 类型参数

######## 1. FlsLoaderDF0Prot

- **UUID**: `c37e5f8c-2ef2-472a-98b5-dcc18cbea5cd`
- **参数名**: `FlsLoaderDF0Prot`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `NO_PROTECTION`
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `NO_PROTECTION` (来源: INFINEON_AURIX2G)
  - `READ_PROTECTION` (来源: INFINEON_AURIX2G)
  - `WRITE_PROTECTION` (来源: INFINEON_AURIX2G)
- **描述**: DF0 Read/Write protection.

##### 18. CommonPublishedInformation

**容器属性**:

- **UUID**: `492f8482-3e2c-4bf1-b27f-01fd7ac35788`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CommonPublishedInformation`
- **多重性**: [0..1]

**容器描述**:

Common container, aggregated by all modules. It contains published information about vendor and versions.

###### 参数配置

此容器包含 **9** 个参数：

####### INTEGER 类型参数

######## 1. ArMajorVersion

- **UUID**: `bd0a8d38-4d8c-4ee9-88fe-1166b258bb8a`
- **参数名**: `ArMajorVersion`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `4`
- **取值范围**: [0..255]
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Major version number of AUTOSAR specification on which the appropriate implementation is based on.

######## 2. ArMinorVersion

- **UUID**: `73f87c7f-e230-4178-bff0-eb2704aae656`
- **参数名**: `ArMinorVersion`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `2`
- **取值范围**: [0..255]
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Minor version number of AUTOSAR specification on which the appropriate implementation is based on.

######## 3. ArPatchVersion

- **UUID**: `2380135d-6778-417a-a34b-e10017d4dd54`
- **参数名**: `ArPatchVersion`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `2`
- **取值范围**: [0..255]
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Patch level version number of AUTOSAR specification on which the appropriate implementation is based on.

######## 4. SwMajorVersion

- **UUID**: `fca015e3-5f28-4cbe-8949-8f4b87d86827`
- **参数名**: `SwMajorVersion`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `10`
- **取值范围**: [0..255]
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Major version number of the vendor specific implementation of the module. The numbering is vendor specific.

######## 5. SwMinorVersion

- **UUID**: `14ab81e0-3d80-43dc-8b92-247e5a542df9`
- **参数名**: `SwMinorVersion`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `40`
- **取值范围**: [0..255]
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Minor version number of the vendor specific implementation of the module. The numbering is vendor specific.

######## 6. SwPatchVersion

- **UUID**: `32e37bfd-18b6-41d1-9248-a81dbe0fe4c5`
- **参数名**: `SwPatchVersion`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..255]
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Patch level version number of the vendor specific implementation of the module. The numbering is vendor specific.

######## 7. ModuleId

- **UUID**: `3b407478-6902-4f80-b7cf-f33b0854e638`
- **参数名**: `ModuleId`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `255`
- **取值范围**: [0..65535]
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Module ID of this module from Module List

######## 8. VendorId

- **UUID**: `7d650b2d-4adb-41f0-a68e-5f0c416501d1`
- **参数名**: `VendorId`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `17`
- **取值范围**: [0..65535]
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Vendor ID of the dedicated implementation of this module according to the AUTOSAR vendor list

####### STRING 类型参数

######## 1. Release

- **UUID**: `3b407478-6902-4f40-b7cf-f33b0854e638`
- **参数名**: `Release`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **字符串变体**:
  - 默认值: `_TRICORE_TC397`
- **描述**: Aurix2G derivative used for the implementation

## 📦 包结构

此ARXML文件包含 **2** 个包：

### 1. AURIX2G

- **UUID**: `ECUC:AUTOSAR`
- **包名称**: `AURIX2G`
- **包含元素数量**: 0

### 2. EcucDefs

- **UUID**: `ECUC:ECUCDEFS`
- **包名称**: `EcucDefs`
- **包含元素数量**: 1

#### 包含的元素

##### ECUC-MODULE-DEF 类型元素

1. **FlsLoader**
