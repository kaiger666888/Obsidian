# FblBm - 完整配置文档

*此文档由ARXML文件自动生成，采用层次化结构展示*

**生成时间**: 2025-06-16 14:48:07

## 📑 目录

- [📄 文件信息](#-文件信息)
- [🔧 模块定义](#-模块定义)
  - [FblBm](#fblbm)
- [📦 包结构](#-包结构)
- [⚡ 实现信息](#-实现信息)
- [⚙️ 配置信息](#️-配置信息)

## 📄 文件信息

### Schema信息
- **Schema位置**: `http://autosar.org/schema/r4.0 AUTOSAR_4-3-0.xsd`
- **命名空间**: `http://autosar.org/schema/r4.0`

## 🔧 模块定义

### 1. FblBm

#### 基本信息

- **UUID**: `19da46ba-9344-4ec7-842d-f875fba16c4f`
- **模块名称**: `FblBm`
- **类别**: `VENDOR_SPECIFIC_MODULE_DEFINITION`
- **多重性**: [1..1]
- **支持的变体**:
  - VARIANT-PRE-COMPILE

#### 模块描述

Configuration of the FblBm (Boot Manager) module.

#### 配置容器

本模块包含 **4** 个配置容器：

##### 1. FblBmGeneral

**容器属性**:

- **UUID**: `403e6b22-3ff3-473a-b83e-3721d4d2d2ea`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FblBmGeneral`
- **多重性**: [1..1]
- **需要索引**: false

**容器描述**:

General configuration parameters of the FblBm.

###### 参数配置

此容器包含 **11** 个参数：

####### INTEGER 类型参数

######## 1. FblBmHeaderAddress

- **UUID**: `e4ac48bd-cfbe-4e40-92ab-af0be8384ce3`
- **参数名**: `FblBmHeaderAddress`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: This is the start address of the BootManager's BmHeader structure (defined in module bm_main.c). TheBootManager header can be located at an arbitrary address using the provided section #pragma instructions.

####### BOOLEAN 类型参数

######## 1. FblBmSecureBoot

- **UUID**: `95bb501b-7fac-446f-a4b6-e8a1c6cbdb00`
- **参数名**: `FblBmSecureBoot`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Enable or disable the secure boot functionality.

True: The BootManager uses the hardware module (SHE/HSM) to verify that the memory has not been altered.
False: The BootManger checks only the validity.

######## 2. FblBmStandaloneMode

- **UUID**: `46323261-8cc7-45cd-82b3-1f006b8fa643`
- **参数名**: `FblBmStandaloneMode`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: This parameter defines whether the BootManager is compiled/linked standalone or with the Bootloader.

True: The BootManager is compiled/linked standalone. BootManager and Bootloader will be two separate projects.
False: The BootManager is compiled/linked together with the Bootloader.

######## 3. FblBmIncludeOemConfiguration

- **UUID**: `99d63198-b0a2-41b6-ac10-3e70be6af13a`
- **参数名**: `FblBmIncludeOemConfiguration`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: This parameter defines whether the OEM configuration file “bm_oem_cfg.h” should be included or not.

True: The header file is included in FblBm_Cfg.h.
False: The header is not included.

######## 4. FblBmIncludeHardwareConfiguration

- **UUID**: `eb21666d-72e1-4c3e-8580-3ed029850bff`
- **参数名**: `FblBmIncludeHardwareConfiguration`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: This parameter defines whether the hardware configuration file “bm_hw_cfg.h” should be included or not.

True: The header file is included in FblBm_Cfg.h.
False: The header is not included.

######## 5. FblBmFailsafeUpdater

- **UUID**: `26a75f74-8bbd-4c39-84cb-a8204437fdf6`
- **参数名**: `FblBmFailsafeUpdater`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Enables or disables the feature failsafe updater, where the Bootmanager is searching for an updater in case the Bootloader is corrupted.

True: BootManager searches for an updater and starts it.
False: BootManager goes into a fail state (see callout function FBLBM_CALLOUT_FATAL_ERROR)

######## 6. FblBmInitializeKeys

- **UUID**: `d68957c7-469d-45f5-822c-dd018b239984`
- **参数名**: `FblBmInitializeKeys`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Enables or disables the feature where the Bootmanager checks if the keys are programmed, see callout function FBLBM_CALLOUT_GET_KEYEMPTY.

True: BootManager calls Bootloader in case keys are determined to be empty.
False: Bootmanager continues sequence normally.

######## 7. FblBmInitializeMacOfBootloader

- **UUID**: `21cc6e6a-0503-4fae-a41b-ba0de056e498`
- **参数名**: `FblBmInitializeMacOfBootloader`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Enables or disables the feature where the Bootmanager checks if the MAC of the Bootloader is present, see callout function FBLBM_CALLOUT_GET_FBL_CMACERASED.

True: BootManager calls Bootloader in case MAC of Bootloader is determined to be not written so yet.
False: Bootmanager continues sequence normally.

####### STRING 类型参数

######## 1. FblBmUserConfigFile

- **UUID**: `00029048-0477-4ec2-933a-b43a4da0790c`
- **参数名**: `FblBmUserConfigFile`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **字符串变体**:
  - 默认值: `FblBm_UserCfg.h`
- **描述**: Reference to an external text file that will be included during generation to FblBm_Cfg.h.
The content of the user configuration file will be added at the end of the generated module configuration file and allows altering or extending the generated code.

Caution: User configuration files can cause the software module to malfunction and must only be used with great care!

######## 2. FblBmUserIncludeHeader

- **UUID**: `6ee30545-3288-4ebe-a7f5-1a4a29ae9d7b`
- **参数名**: `FblBmUserIncludeHeader`
- **数据类型**: STRING
- **多重性**: [0..infinite]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **字符串变体**:
  - 默认值: `0`
- **描述**: This parameter is used to specify additional header files to be included in the generated FblBm_Cfg.h.

Insert complete filenames including extension (e.g. MyHeader.h).

####### ENUMERATION 类型参数

######## 1. FblBmExecutionInstance

- **UUID**: `9d5c2d62-81e9-4b03-944d-8442e99333c3`
- **参数名**: `FblBmExecutionInstance`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `BootManager`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `BootManager` (来源: Vector Informatik)
  - `BootManagerAndFlashBootloader` (来源: Vector Informatik)
  - `FlashBootloader` (来源: Vector Informatik)
  - `FlashBootloaderUpdater` (来源: Vector Informatik)
  - `Application` (来源: Vector Informatik)
  - `Others` (来源: Vector Informatik)
- **描述**: Determines the context the software is getting build.

##### 2. FblBmBootOrder

**容器属性**:

- **UUID**: `3eecdbb3-2898-4f68-b4ae-b26dc699294f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FblBmBootOrder`
- **多重性**: [0..1]
- **需要索引**: false

**容器描述**:

Contains boot targets and related dependency targets

###### 配置容器

本模块包含 **2** 个配置容器：

####### 1. FblBmDependency

**容器属性**:

- **UUID**: `15dfb65e-d82c-4be1-90f2-b30b5ccb54be`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FblBmDependency`
- **多重性**: [0..infinite]
- **需要索引**: false

**容器描述**:

List of all dependency targets, which can be used by the boot targets

######## 参数配置

此容器包含 **1** 个参数：

######### ENUMERATION 类型参数

########## 1. FblBmDisposability

- **UUID**: `7ddaffd1-3e71-4b03-bf76-b69ac9b39128`
- **参数名**: `FblBmDisposability`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `OPTIONAL`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `MANDATORY`
  - `OPTIONAL`
- **描述**: Specify whether the dependency target should be mandatory or optional

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. FblBmDependencyTargetRef

- **UUID**: `1d72dd96-adf8-4f8b-85a9-32180c304f86`
- **引用名**: `FblBmDependencyTargetRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `FblBmHdrTarget`
- **完整路径**: `/MICROSAR/FblBmHdr/FblBmHdrTarget`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **需要索引**: false
- **描述**: This parameter references to a dependency target

####### 2. FblBmBootTarget

**容器属性**:

- **UUID**: `b7f6873b-b229-4bf6-9569-6e26e72e386a`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FblBmBootTarget`
- **多重性**: [1..infinite]
- **需要索引**: false

**容器描述**:

List of all bootable targets

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. FblBmBootOrderId

- **UUID**: `b56e3305-921f-4670-bfae-9d6bd65f6f30`
- **参数名**: `FblBmBootOrderId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Identifier of the boot target order

######## 引用关系

此容器包含 **2** 个引用：

######### REFERENCE 类型引用

########## 1. FblBmBootTargetRef

- **UUID**: `486e3fbf-2ab9-42da-ae28-df2f65a34a63`
- **引用名**: `FblBmBootTargetRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `FblBmHdrTarget`
- **完整路径**: `/MICROSAR/FblBmHdr/FblBmHdrTarget`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **需要索引**: false
- **描述**: This parameter references to a bootable target

########## 2. FblBmDependencyListRef

- **UUID**: `21bae958-54e1-4286-bfab-c88a870b5996`
- **引用名**: `FblBmDependencyListRef`
- **引用类型**: REFERENCE
- **多重性**: [0..infinite]
- **目标**: `FblBmDependency`
- **完整路径**: `/MICROSAR/FblBm/FblBmBootOrder/FblBmDependency`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **需要索引**: false
- **描述**: List of dependency targets. The dependency targets are checked for presence before starting the bootable target.

##### 3. FblBmDependency

**容器属性**:

- **UUID**: `15dfb65e-d82c-4be1-90f2-b30b5ccb54be`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FblBmDependency`
- **多重性**: [0..infinite]
- **需要索引**: false

**容器描述**:

List of all dependency targets, which can be used by the boot targets

###### 参数配置

此容器包含 **1** 个参数：

####### ENUMERATION 类型参数

######## 1. FblBmDisposability

- **UUID**: `7ddaffd1-3e71-4b03-bf76-b69ac9b39128`
- **参数名**: `FblBmDisposability`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `OPTIONAL`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `MANDATORY`
  - `OPTIONAL`
- **描述**: Specify whether the dependency target should be mandatory or optional

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. FblBmDependencyTargetRef

- **UUID**: `1d72dd96-adf8-4f8b-85a9-32180c304f86`
- **引用名**: `FblBmDependencyTargetRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `FblBmHdrTarget`
- **完整路径**: `/MICROSAR/FblBmHdr/FblBmHdrTarget`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **需要索引**: false
- **描述**: This parameter references to a dependency target

##### 4. FblBmBootTarget

**容器属性**:

- **UUID**: `b7f6873b-b229-4bf6-9569-6e26e72e386a`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FblBmBootTarget`
- **多重性**: [1..infinite]
- **需要索引**: false

**容器描述**:

List of all bootable targets

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. FblBmBootOrderId

- **UUID**: `b56e3305-921f-4670-bfae-9d6bd65f6f30`
- **参数名**: `FblBmBootOrderId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Identifier of the boot target order

###### 引用关系

此容器包含 **2** 个引用：

####### REFERENCE 类型引用

######## 1. FblBmBootTargetRef

- **UUID**: `486e3fbf-2ab9-42da-ae28-df2f65a34a63`
- **引用名**: `FblBmBootTargetRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `FblBmHdrTarget`
- **完整路径**: `/MICROSAR/FblBmHdr/FblBmHdrTarget`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **需要索引**: false
- **描述**: This parameter references to a bootable target

######## 2. FblBmDependencyListRef

- **UUID**: `21bae958-54e1-4286-bfab-c88a870b5996`
- **引用名**: `FblBmDependencyListRef`
- **引用类型**: REFERENCE
- **多重性**: [0..infinite]
- **目标**: `FblBmDependency`
- **完整路径**: `/MICROSAR/FblBm/FblBmBootOrder/FblBmDependency`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **需要索引**: false
- **描述**: List of dependency targets. The dependency targets are checked for presence before starting the bootable target.

## 📦 包结构

此ARXML文件包含 **1** 个包：

### 1. MICROSAR

- **UUID**: `ff55d029-386d-43a2-b3c2-dfef4c7a5e36`
- **包名称**: `MICROSAR`
- **包含元素数量**: 4

#### 包含的元素

##### BSW-IMPLEMENTATION 类型元素

1. **FblBm_Impl**

##### ECUC-MODULE-DEF 类型元素

1. **FblBm**

##### ECUC-MODULE-CONFIGURATION-VALUES 类型元素

1. **FblBm_Pre**
2. **FblBm_Rec**

## ⚡ 实现信息

此ARXML文件包含 **1** 个实现：

### 1. FblBm_Impl

- **UUID**: `9bff5ff6-83dd-4055-84b5-65e3c7c852c0`
- **实现名称**: `FblBm_Impl`
- **编程语言**: C
- **软件版本**: 1.00.00
- **供应商ID**: 30
- **AUTOSAR版本**: 4.03.00
- **代码生成器**: DaVinci Configurator

## ⚙️ 配置信息

此ARXML文件包含 **2** 个配置：

### 1. FblBm_Pre

- **UUID**: `f76043ec-647e-4b79-aa40-68e02e285b28`
- **配置名称**: `FblBm_Pre`
- **定义引用**: `/MICROSAR/FblBm`

### 2. FblBm_Rec

- **UUID**: `58444c48-b85b-4341-a9c9-e9a4f31bb202`
- **配置名称**: `FblBm_Rec`
- **定义引用**: `/MICROSAR/FblBm`
