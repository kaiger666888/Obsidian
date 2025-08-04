# vHsm - 完整配置文档

*此文档由ARXML文件自动生成，采用层次化结构展示*

**生成时间**: 2025-06-16 14:50:57

## 📑 目录

- [📄 文件信息](#-文件信息)
- [🔧 模块定义](#-模块定义)
  - [vHsm](#vhsm)
- [📦 包结构](#-包结构)
- [⚡ 实现信息](#-实现信息)
- [⚙️ 配置信息](#️-配置信息)

## 📄 文件信息

### Schema信息
- **Schema位置**: `http://autosar.org/schema/r4.0 AUTOSAR_4-0-3.xsd`
- **命名空间**: `http://autosar.org/schema/r4.0`

## 🔧 模块定义

### 1. vHsm

#### 基本信息

- **UUID**: `62c8f908-5b61-4147-af49-0027fa3dea6f`
- **模块名称**: `vHsm`
- **类别**: `VENDOR_SPECIFIC_MODULE_DEFINITION`
- **多重性**: [1..1]
- **支持的变体**:
  - VARIANT-PRE-COMPILE

#### 模块描述

Configuration of the vHsm module.

#### 版本历史

共有 **18** 个版本记录：

##### 1. 版本 1.00.00

- **状态**: beta
- **发布日期**: 2017-12-07T05:11:56+01:00
- **发布者**: visrpp

**变更内容**:

##### 2. 版本 1.01.00

- **状态**: released
- **发布日期**: 2018-03-28T10:27:32+02:00
- **发布者**: vistof

**变更内容**:

##### 3. 版本 2.00.00

- **状态**: released
- **发布日期**: 2018-10-02T18:30:32+02:00
- **发布者**: visrpp

**变更内容**:

##### 4. 版本 2.00.01

- **状态**: released
- **发布日期**: 2018-10-16T14:42:07+02:00
- **发布者**: vistof

**变更内容**:

##### 5. 版本 2.00.02

- **状态**: released
- **发布日期**: 2018-10-25T12:14:42+02:00
- **发布者**: vistof

**变更内容**:

##### 6. 版本 2.01.00

- **状态**: released
- **发布日期**: 2019-01-02T15:29:52+01:00
- **发布者**: vistof

**变更内容**:

##### 7. 版本 2.01.01

- **状态**: released
- **发布日期**: 2019-05-06T10:38:16+02:00
- **发布者**: vistof

**变更内容**:

##### 8. 版本 2.01.02

- **状态**: released
- **发布日期**: 2019-07-01T10:12:14+02:00
- **发布者**: vistof

**变更内容**:

##### 9. 版本 2.01.03

- **状态**: released
- **发布日期**: 2019-07-08T15:53:17+02:00
- **发布者**: vistof

**变更内容**:

##### 10. 版本 3.00.00

- **状态**: released
- **发布日期**: 2019-08-02T09:17:05+02:00
- **发布者**: vistof

**变更内容**:

##### 11. 版本 3.00.01

- **状态**: released
- **发布日期**: 2019-09-13T11:11:47+02:00
- **发布者**: vistof

**变更内容**:

##### 12. 版本 3.01.00

- **状态**: released
- **发布日期**: 2019-10-18T10:23:32+02:00
- **发布者**: vistof

**变更内容**:

##### 13. 版本 4.00.00

- **状态**: released
- **发布日期**: 2019-12-06T09:58:05+01:00
- **发布者**: vistof

**变更内容**:

##### 14. 版本 4.01.00

- **状态**: released
- **发布日期**: 2020-04-21T13:38:23+02:00
- **发布者**: vistof

**变更内容**:

##### 15. 版本 4.02.00

- **状态**: released
- **发布日期**: 2020-05-27T13:32:54+02:00
- **发布者**: vistof

**变更内容**:

##### 16. 版本 4.02.01

- **状态**: released
- **发布日期**: 2020-06-16T16:47:52+02:00
- **发布者**: vistof

**变更内容**:

##### 17. 版本 5.00.00

- **状态**: released
- **发布日期**: 2020-06-24T15:00:52+02:00
- **发布者**: vistof, visdil

**变更内容**:

##### 18. 版本 5.00.01

- **状态**: released
- **发布日期**: 2020-12-09T14:39:08+01:00
- **发布者**: vistof

**变更内容**:

#### 配置容器

本模块包含 **32** 个配置容器：

##### 1. vHsmGeneral

**容器属性**:

- **UUID**: `6efed118-7a29-46a0-b21b-eab82f9f614c`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vHsmGeneral`
- **多重性**: [1..1]
- **构建后可变**: false

**容器描述**:

Container for the configuration of the vHsm Firmware

###### 参数配置

此容器包含 **11** 个参数：

####### INTEGER 类型参数

######## 1. vHsmSoftResetLimit

- **UUID**: `d4c987c3-cb99-436d-b8b6-9013f5e4b05c`
- **参数名**: `vHsmSoftResetLimit`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `8`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Maximum number of software resets before going to halt.

This may not be available on all platforms.

####### BOOLEAN 类型参数

######## 1. vHsmDevErrorDetect

- **UUID**: `6e2d9fb5-9fd0-42c5-98a8-e99174cce57c`
- **参数名**: `vHsmDevErrorDetect`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enable DET

######## 2. vHsmRedirection

- **UUID**: `048bb603-38c7-47ae-80aa-023e614d7b62`
- **参数名**: `vHsmRedirection`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enable job input/output redirection to key elements. This is a Autosar 4.4 feature. Therefore a Crypto driver is needed which also supports this feature.

######## 3. vHsmEnableRamLoopCallout

- **UUID**: `b3057521-f300-4474-80a7-5027b9260205`
- **参数名**: `vHsmEnableRamLoopCallout`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enable a callout which is cyclically called during the RAM loop.

######## 4. vHsmGenerateRandomIpcValues

- **UUID**: `df9cda0d-e35a-4aea-beb5-4709deb350f5`
- **参数名**: `vHsmGenerateRandomIpcValues`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Generate two uint32 and a 16 byte array of random data to the IPC.
This random data can be read from IPC at startup without using a Crypto driver.
Use-Cases are e.g. canary for stack protection.

When enabled, this may increase the startup time significantly depending on the hardware.

######## 5. vHsmGenerateRandomStackProtectionCanary

- **UUID**: `2e563f99-dbae-402f-b138-7e95b55b7b20`
- **参数名**: `vHsmGenerateRandomStackProtectionCanary`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Generate a uint32 value used as canary for stack protection.

When enabled, this may increase the startup time significantly depending on the hardware.

####### FLOAT 类型参数

######## 1. vHsmMainFunctionPeriod

- **UUID**: `d4824866-103c-416d-9dd1-563e2172c7c5`
- **参数名**: `vHsmMainFunctionPeriod`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **默认值**: `0.01`
- **取值范围**: [0..3600]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies the period of main function vHsm_MainFunction in seconds.

If the parameter is available, the cyclic operations of the vHsm are processed in a cyclic task.
If the parameter is not set the cyclic operations are  processed in background task

####### STRING 类型参数

######## 1. vHsmUserRevision

- **UUID**: `2dff7260-7d4b-4db1-a8bb-f1c92bf63bec`
- **参数名**: `vHsmUserRevision`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **字符串变体**:
  - 默认值: `0`
  - 最大长度: 255
  - 最小长度: 1
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter is freely configurable and is synced to the application configuration (/MICROSAR/Crypto_30_vHsm/Crypto/CryptovHsm/CryptoHsmUserRevision). Use this to have a compare value that the configuration of application and vHSM are in sync.

######## 2. vHsmUserConfigurationFile

- **UUID**: `25bbc549-c776-4395-8732-b25b6781af69`
- **参数名**: `vHsmUserConfigurationFile`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **字符串变体**:
  - 默认值: `vHsm_UserCfg.h`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to an external text file that will be included during generation to vHsm_Cfg.h.
The content of the user configuration file will be added at the end of the generated module configuration file and allows altering or extending the generated code.
Caution: User configuration files can cause the software module to malfunction and must only be used with great care.

####### ENUMERATION 类型参数

######## 1. vHsmAdditionalSettings

- **UUID**: `3ef37db1-befc-4ccd-9f66-f3bcdb23b488`
- **参数名**: `vHsmAdditionalSettings`
- **数据类型**: ENUMERATION
- **多重性**: [0..infinite]
- **默认值**: `ENABLE_API_GET_CODE_FLASH_ADDRESS`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `ENABLE_API_CODE_FLASH_ACCESS` (来源: Vector Informatik)
  - `ENABLE_API_RESET_VECTOR` (来源: Vector Informatik)
  - `ENABLE_API_GET_IPC_ADDRESS` (来源: Vector Informatik)
  - `ENABLE_API_PREPARE_JOB_DATA` (来源: Vector Informatik)
  - `ENABLE_API_GET_CODE_FLASH_ADDRESS` (来源: Vector Informatik)
  - `ENABLE_API_HALT` (来源: Vector Informatik)
  - `ENABLE_UNALIGNED_ACCESS` (来源: Vector Informatik)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter provides hardware specific settings for the vHsm Hal component,
 e.g. enables several Hal callouts in the vHsm_Core component.

This parameter is set automatically by Hal implementation so Integrator shall not modify it.

######## 2. vHsmInvalidNvMBlockBehaviour

- **UUID**: `6c3ac9f0-ad46-4601-9968-2594c8f15dc2`
- **参数名**: `vHsmInvalidNvMBlockBehaviour`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `VHSM_IGNORE_INVALID_BLOCKS`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `VHSM_PERSIST_NVMCONFIGBLOCK` (来源: Vector Informatik)
  - `VHSM_IGNORE_INVALID_BLOCKS` (来源: Vector Informatik)
  - `VHSM_PERSIST_INVALID_BLOCKS` (来源: Vector Informatik)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: If NvM blocks have never been written they will produce an error during ReadAll at startup of the vHsm.

Make sure to persist all NvM Blocks during the first startup at least once or always  ignore the error about invalid blocks by setting this option to VHSM_IGNORE_INVALID_BLOCKS
Otherwise the vHsm will trigger a software reset on the next startup.

Persisting all blocks during first startup can be done by either setting this option to VHSM_REPERSIST_INVALID_BLOCKS or calling vHsm_NvM_Repersist() in vHsm_FirstStartup_Callout().

Info: If a NvM Block is read as invalid, the contained keys will have the init values as configured in the LibCv driver.

###### 引用关系

此容器包含 **2** 个引用：

####### SYMBOLIC-NAME-REFERENCE 类型引用

######## 1. ErrorLogEventLogRef

- **UUID**: `a727c7ba-16ac-47be-b9a7-edbdac71b4ce`
- **引用名**: `ErrorLogEventLogRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `vHsmLogEvent`
- **完整路径**: `/MICROSAR/vHsm/vHsmLog/vHsmLogEvent`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the log event where the error log shall be stored.
The error log has been moved from a key element to the new event log.

######## 2. vHsmRandomCsmJobRef

- **UUID**: `c5abded2-c596-4613-a00f-eaa976cd7951`
- **引用名**: `vHsmRandomCsmJobRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `CsmJob`
- **完整路径**: `/AUTOSAR/EcucDefs/Csm/CsmJobs/CsmJob`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a CSM job which will be used to define the primary random source of the vHsm firmware.

This random job will be used for vHsm_MemRand() and esl_getBytesRNG()

If the CSM job is executed in another driver other than the HAL, it may be necessary to seed the key in vHsm_InitThree_Callout() beforehand.

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. vHsmMemoryArea

**容器属性**:

- **UUID**: `9fba760e-00cf-44a8-854a-dfc305e8cf3d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vHsmMemoryArea`
- **多重性**: [1..infinite]
- **构建后可变**: false

**容器描述**:

Whitelist of the memory sections which is regarded as valid memory for input and/or output depending on the configuration.

Attention!
Keep in mind that a wrong configuration may expose vHsm internal secure memory areas to be used inside jobs.

######## 参数配置

此容器包含 **7** 个参数：

######### INTEGER 类型参数

########## 1. vHsmMemoryAreaStart

- **UUID**: `bf2756c9-8847-491f-9330-fbf8bcdfc853`
- **参数名**: `vHsmMemoryAreaStart`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Start address of the memory area

########## 2. vHsmMemoryAreaStop

- **UUID**: `89fbbeaa-0cf9-4d05-9fc0-23b1257be938`
- **参数名**: `vHsmMemoryAreaStop`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `4294967295`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: End address of the memory area

########## 3. vHsmMemoryAreaId

- **UUID**: `58d03241-06a3-4d3b-8ec0-4034676b6d47`
- **参数名**: `vHsmMemoryAreaId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Id of the memory area

########## 4. vHsmMemoryAreaPriority

- **UUID**: `f914effe-b535-45e2-96f3-ed969ad6b0d9`
- **参数名**: `vHsmMemoryAreaPriority`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The priority of the memory area.
The higher the value, the higher the areas priority.
The area with the highest priority will be checked first.
To get the best performance assign a high priority to areas which are used very often.

######### BOOLEAN 类型参数

########## 1. vHsmAllowDynamicConfig

- **UUID**: `c8506444-1a9f-43cb-864f-d362c4a08212`
- **参数名**: `vHsmAllowDynamicConfig`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: For some memory sections the Hal can configure the boundaries during runtime.

######### ENUMERATION 类型参数

########## 1. vHsmMemoryAreaType

- **UUID**: `289b0fcd-c887-4fd5-a92b-2e2a815faca2`
- **参数名**: `vHsmMemoryAreaType`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `VHSM_MEMORY_AREA_READ`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `VHSM_MEMORY_AREA_READWRITE` (来源: Vector Informatik)
  - `VHSM_MEMORY_AREA_READ` (来源: Vector Informatik)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Type of the memory area

########## 2. vHsmMemoryAreaUser

- **UUID**: `30b07470-ffc1-4b91-8fbd-01b6a9e9979b`
- **参数名**: `vHsmMemoryAreaUser`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `BOTH`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `HSM` (来源: Vector Informatik)
  - `HOST` (来源: Vector Informatik)
  - `BOTH` (来源: Vector Informatik)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines which core uses this memory area.

HSM:
- The Hsm will use this area for the whitelist during pointer checking
- The Area will not be synchronized to the memory areas of the driver on the host application core.

HOST:
- The Hsm will ignore this area during pointer checking.
- This area will be synchronized to the driver on host application core

BOTH:
- The Hsm will use this area for the whitelist during pointer checking
- This area will be synchronized to the driver on host application core

##### 2. vHsmMemoryArea

**容器属性**:

- **UUID**: `9fba760e-00cf-44a8-854a-dfc305e8cf3d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vHsmMemoryArea`
- **多重性**: [1..infinite]
- **构建后可变**: false

**容器描述**:

Whitelist of the memory sections which is regarded as valid memory for input and/or output depending on the configuration.

Attention!
Keep in mind that a wrong configuration may expose vHsm internal secure memory areas to be used inside jobs.

###### 参数配置

此容器包含 **7** 个参数：

####### INTEGER 类型参数

######## 1. vHsmMemoryAreaStart

- **UUID**: `bf2756c9-8847-491f-9330-fbf8bcdfc853`
- **参数名**: `vHsmMemoryAreaStart`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Start address of the memory area

######## 2. vHsmMemoryAreaStop

- **UUID**: `89fbbeaa-0cf9-4d05-9fc0-23b1257be938`
- **参数名**: `vHsmMemoryAreaStop`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `4294967295`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: End address of the memory area

######## 3. vHsmMemoryAreaId

- **UUID**: `58d03241-06a3-4d3b-8ec0-4034676b6d47`
- **参数名**: `vHsmMemoryAreaId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Id of the memory area

######## 4. vHsmMemoryAreaPriority

- **UUID**: `f914effe-b535-45e2-96f3-ed969ad6b0d9`
- **参数名**: `vHsmMemoryAreaPriority`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The priority of the memory area.
The higher the value, the higher the areas priority.
The area with the highest priority will be checked first.
To get the best performance assign a high priority to areas which are used very often.

####### BOOLEAN 类型参数

######## 1. vHsmAllowDynamicConfig

- **UUID**: `c8506444-1a9f-43cb-864f-d362c4a08212`
- **参数名**: `vHsmAllowDynamicConfig`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: For some memory sections the Hal can configure the boundaries during runtime.

####### ENUMERATION 类型参数

######## 1. vHsmMemoryAreaType

- **UUID**: `289b0fcd-c887-4fd5-a92b-2e2a815faca2`
- **参数名**: `vHsmMemoryAreaType`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `VHSM_MEMORY_AREA_READ`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `VHSM_MEMORY_AREA_READWRITE` (来源: Vector Informatik)
  - `VHSM_MEMORY_AREA_READ` (来源: Vector Informatik)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Type of the memory area

######## 2. vHsmMemoryAreaUser

- **UUID**: `30b07470-ffc1-4b91-8fbd-01b6a9e9979b`
- **参数名**: `vHsmMemoryAreaUser`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `BOTH`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `HSM` (来源: Vector Informatik)
  - `HOST` (来源: Vector Informatik)
  - `BOTH` (来源: Vector Informatik)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines which core uses this memory area.

HSM:
- The Hsm will use this area for the whitelist during pointer checking
- The Area will not be synchronized to the memory areas of the driver on the host application core.

HOST:
- The Hsm will ignore this area during pointer checking.
- This area will be synchronized to the driver on host application core

BOTH:
- The Hsm will use this area for the whitelist during pointer checking
- This area will be synchronized to the driver on host application core

##### 3. vHsmDevelopment

**容器属性**:

- **UUID**: `c0fbe557-aa27-4fd7-b90a-1ae2b9b93fa2`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vHsmDevelopment`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

This container must only be used during development

###### 参数配置

此容器包含 **8** 个参数：

####### BOOLEAN 类型参数

######## 1. vHsmOptionByteModification

- **UUID**: `d0b9c514-1d89-40b5-ad79-c86c1d8850d8`
- **参数名**: `vHsmOptionByteModification`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This option enables the application cores to edit the option bytes.

If enabled, this renders the HSM unsecure, because the HSM can be disabled completely!
This is not available on all hardware platforms.

######## 2. vHsmTraceInfo

- **UUID**: `3b5a5546-2eef-408f-98c1-1ac067d1a243`
- **参数名**: `vHsmTraceInfo`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Print out debug information on the console in the multi debugger.

######## 3. vHsmTraceWarning

- **UUID**: `b7d10e7b-2933-4f57-9172-6fefa912d322`
- **参数名**: `vHsmTraceWarning`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Print out debug information on the console in the multi debugger.

######## 4. vHsmTraceDebug

- **UUID**: `e5d4b74d-bd7d-466b-ad8f-76306af54e22`
- **参数名**: `vHsmTraceDebug`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Print out debug information on the console in the multi debugger.

######## 5. vHsmTraceError

- **UUID**: `fdca1819-123d-4210-ab79-d58494eb1e5f`
- **参数名**: `vHsmTraceError`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Print out debug information on the console in the multi debugger.

######## 6. vHsmTraceKeyStorage

- **UUID**: `d938940e-930d-4e0b-a1ce-4a8747eb411b`
- **参数名**: `vHsmTraceKeyStorage`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Print the state and changes of the KeyStorage

######## 7. vHsmUpgradeProtectionModification

- **UUID**: `a1cfc72e-c1e7-480f-83a2-e7744a185cb5`
- **参数名**: `vHsmUpgradeProtectionModification`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This option enables the application cores to edit the upgrade protection.

If enabled, this renders the HSM unsecure, because the HSM can be disabled completely!
This is not available on all hardware platforms.

######## 8. vHsmEnableSecureBootAutostart

- **UUID**: `e6f142a2-2f7a-48f9-86f5-e190b3463328`
- **参数名**: `vHsmEnableSecureBootAutostart`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enable the autostart of secure boot

##### 4. vHsmChannelMapping

**容器属性**:

- **UUID**: `c2b9428e-20a2-4dd6-b23f-8272f754fd66`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vHsmChannelMapping`
- **多重性**: [1..1]
- **构建后可变**: false

**容器描述**:

This container is for defining the which CryIf channels are used for the different use cases

###### 引用关系

此容器包含 **1** 个引用：

####### SYMBOLIC-NAME-REFERENCE 类型引用

######## 1. vHsmKeyManagementChannel

- **UUID**: `ce10766e-93b0-4f18-9b08-213b028e28f4`
- **引用名**: `vHsmKeyManagementChannel`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `CryIfChannel`
- **完整路径**: `/MICROSAR/CryIf/CryIfChannel`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Channel which is used to transfer the key management APIs

##### 5. vHsmKeyMapping

**容器属性**:

- **UUID**: `927c0845-01bc-4c5b-b08d-7453bcd11ca0`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vHsmKeyMapping`
- **多重性**: [1..1]
- **构建后可变**: false

**容器描述**:

This container is for defining which Crypto keys are used for the different use cases.
Also the key properties can be defined here (e.g. Write Once, Secure Boot protected)

###### 引用关系

此容器包含 **2** 个引用：

####### SYMBOLIC-NAME-REFERENCE 类型引用

######## 1. vHsmSecureBootProtectedKeys

- **UUID**: `f4db5357-c292-48ee-9218-5207d5dd1fa0`
- **引用名**: `vHsmSecureBootProtectedKeys`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..infinite]
- **目标**: `CryIfKey`
- **完整路径**: `/AUTOSAR/EcucDefs/CryIf/CryIfKey`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The references keys are marked as invalid at startup and can only be used if secure boot has been successful.
Setting the key as valid when secure boot has not finished is not allowed.

######## 2. vHsmInternalOnlyKeys

- **UUID**: `dbba1888-86fe-4900-a676-e1081162bebd`
- **引用名**: `vHsmInternalOnlyKeys`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..infinite]
- **目标**: `CryIfKey`
- **完整路径**: `/AUTOSAR/EcucDefs/CryIf/CryIfKey`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Keys which can only be used internally.
Jobs and key management functions from the application will return an error.

###### 配置容器

本模块包含 **2** 个配置容器：

####### 1. vHsmRandomInit

**容器属性**:

- **UUID**: `225d2318-8de7-4c1a-9bdc-df5d98ed0ead`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vHsmRandomInit`
- **多重性**: [0..infinite]
- **构建后可变**: false

**容器描述**:

A key and its element can be initialized with random value and set to valid at the first startup

######## 引用关系

此容器包含 **2** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. vHsmRandomInitKey

- **UUID**: `458085cc-4c07-490b-b4fd-eb634c3be327`
- **引用名**: `vHsmRandomInitKey`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `CryptoKey`
- **完整路径**: `/AUTOSAR/EcucDefs/Crypto/CryptoKeys/CryptoKey`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the key

########## 2. vHsmRandomInitKeyElement

- **UUID**: `b0fbe4a9-ad8f-4024-9847-6588bac26daf`
- **引用名**: `vHsmRandomInitKeyElement`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `CryptoKeyElement`
- **完整路径**: `/AUTOSAR/EcucDefs/Crypto/CryptoKeyElements/CryptoKeyElement`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the key element in the key which will be completely filled with random data and set to valid during the first startup.

####### 2. vHsmKeyRouting

**容器属性**:

- **UUID**: `6d451e3a-14ab-443e-9485-cbbd241e267f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vHsmKeyRouting`
- **多重性**: [0..infinite]
- **构建后可变**: false

**容器描述**:

A key routing gives the vHSM the possibility to call key operations of another driver for the given key. Due to this, Custom driver or Hardware driver can participate on the key functions, can extend or prohibit the execution or simply bypass them.

######## 引用关系

此容器包含 **2** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. vHsmRoutedKeys

- **UUID**: `9b3cb659-e8ca-4cd5-a8c9-ad5a4724b29f`
- **引用名**: `vHsmRoutedKeys`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..infinite]
- **目标**: `CryIfKey`
- **完整路径**: `/AUTOSAR/EcucDefs/CryIf/CryIfKey`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: If a key operation on the referenced key is received, it will be routed to the key operation handler of the given module instead of the owning module.

Example:
When the application core calls KeyElementSet on a key routed to the vHsm_Hal crypto driver, the API vHsm_Hal_KeyElementSet is called inside the vHsm Firmware.
Due to this, the referenced key can be used for e.g. le the vHsm Firmware enter a RAM loop or to request data flash access.

######### FOREIGN-REFERENCE 类型引用

########## 1. vHsmCryptoModuleRef

- **UUID**: `68332f91-61a8-462e-926d-b4ec3df3edc1`
- **引用名**: `vHsmCryptoModuleRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [1..1]
- **目标类型**: ECUC-MODULE-CONFIGURATION-VALUES
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a Crypto Module which shall receive the keys of the routing. It is up to the modules implementation to forward the request to the original receiver (e.g. Crypto_30_LibCv) if necessary.

##### 6. vHsmRandomInit

**容器属性**:

- **UUID**: `225d2318-8de7-4c1a-9bdc-df5d98ed0ead`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vHsmRandomInit`
- **多重性**: [0..infinite]
- **构建后可变**: false

**容器描述**:

A key and its element can be initialized with random value and set to valid at the first startup

###### 引用关系

此容器包含 **2** 个引用：

####### SYMBOLIC-NAME-REFERENCE 类型引用

######## 1. vHsmRandomInitKey

- **UUID**: `458085cc-4c07-490b-b4fd-eb634c3be327`
- **引用名**: `vHsmRandomInitKey`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `CryptoKey`
- **完整路径**: `/AUTOSAR/EcucDefs/Crypto/CryptoKeys/CryptoKey`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the key

######## 2. vHsmRandomInitKeyElement

- **UUID**: `b0fbe4a9-ad8f-4024-9847-6588bac26daf`
- **引用名**: `vHsmRandomInitKeyElement`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `CryptoKeyElement`
- **完整路径**: `/AUTOSAR/EcucDefs/Crypto/CryptoKeyElements/CryptoKeyElement`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the key element in the key which will be completely filled with random data and set to valid during the first startup.

##### 7. vHsmKeyRouting

**容器属性**:

- **UUID**: `6d451e3a-14ab-443e-9485-cbbd241e267f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vHsmKeyRouting`
- **多重性**: [0..infinite]
- **构建后可变**: false

**容器描述**:

A key routing gives the vHSM the possibility to call key operations of another driver for the given key. Due to this, Custom driver or Hardware driver can participate on the key functions, can extend or prohibit the execution or simply bypass them.

###### 引用关系

此容器包含 **2** 个引用：

####### SYMBOLIC-NAME-REFERENCE 类型引用

######## 1. vHsmRoutedKeys

- **UUID**: `9b3cb659-e8ca-4cd5-a8c9-ad5a4724b29f`
- **引用名**: `vHsmRoutedKeys`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..infinite]
- **目标**: `CryIfKey`
- **完整路径**: `/AUTOSAR/EcucDefs/CryIf/CryIfKey`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: If a key operation on the referenced key is received, it will be routed to the key operation handler of the given module instead of the owning module.

Example:
When the application core calls KeyElementSet on a key routed to the vHsm_Hal crypto driver, the API vHsm_Hal_KeyElementSet is called inside the vHsm Firmware.
Due to this, the referenced key can be used for e.g. le the vHsm Firmware enter a RAM loop or to request data flash access.

####### FOREIGN-REFERENCE 类型引用

######## 1. vHsmCryptoModuleRef

- **UUID**: `68332f91-61a8-462e-926d-b4ec3df3edc1`
- **引用名**: `vHsmCryptoModuleRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [1..1]
- **目标类型**: ECUC-MODULE-CONFIGURATION-VALUES
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a Crypto Module which shall receive the keys of the routing. It is up to the modules implementation to forward the request to the original receiver (e.g. Crypto_30_LibCv) if necessary.

##### 8. vHsmIpc

**容器属性**:

- **UUID**: `6e3f3877-037c-46c0-a85b-eaaa36c6b2ca`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vHsmIpc`
- **多重性**: [1..1]
- **构建后可变**: false

**容器描述**:

Used to configure the IPC.

###### 参数配置

此容器包含 **2** 个参数：

####### INTEGER 类型参数

######## 1. vHsmIpcChannels

- **UUID**: `790bc7f0-10c4-40e8-af9d-42d03db0febf`
- **参数名**: `vHsmIpcChannels`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `4`
- **取值范围**: [1..255]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Each IPC Instance consists of one or more channels. Each channel can hold a job request.
The vHsm will poll the channels inside an IPC one after another and will process the containing jobs.

######## 2. vHsmIpcProtocolVersion

- **UUID**: `646e931f-f637-45fc-9e54-38fdbaceeee8`
- **参数名**: `vHsmIpcProtocolVersion`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `2`
- **取值范围**: [1..2]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Protocol version used to communicate with the vHsm Driver over IPC.

Protocol Version 1 is deprecated!

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. vHsmIpcInstance

**容器属性**:

- **UUID**: `ae5437ef-fbaa-4b58-8aed-db7c2ed2c750`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vHsmIpcInstance`
- **多重性**: [1..255]
- **构建后可变**: false

**容器描述**:

This container represents an IPC instance and therefore the number of distinct memory areas of which each contain an IPC which will be polled for incoming jobs.

If there are more than one Instance of a corresponding vHSM Crypto Driver on application side (e,g, one per core) , create one instance for each.

######## 参数配置

此容器包含 **6** 个参数：

######### INTEGER 类型参数

########## 1. vHsmIpcHardwareUnit

- **UUID**: `b624cdd4-0c72-4288-be48-ed9bc8213f25`
- **参数名**: `vHsmIpcHardwareUnit`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..255]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Id of the Hw IPC which is used to determine the init state of the IPC or to provide the ready state of the HSM

Most platforms only have one hardware unit. Therefore the parameter is mostly set to 0.
Depending on the used platform, a hardware unit can either be a dedicated IPC hardware/channel or just a register.

########## 2. vHsmResponseInterruptFlagSetMask

- **UUID**: `ebdc4004-fb44-41a6-b937-cd113c7adcd3`
- **参数名**: `vHsmResponseInterruptFlagSetMask`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `1`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The mask which will be written to the register which triggers an interrupt the the Host core

########## 3. vHsmIpcInstanceId

- **UUID**: `e84cbfe3-4c6f-4eb4-8c52-eb086055cec0`
- **参数名**: `vHsmIpcInstanceId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..255]
- **来源**: Vector Informatik
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Id of the Ipc instance

########## 4. vHsmResponseInterruptFlagSetAddress

- **UUID**: `3d552f29-e4da-4716-86fc-6056c39cb82f`
- **参数名**: `vHsmResponseInterruptFlagSetAddress`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Address of the register which is used to trigger the interrupt to the host core

######### STRING 类型参数

########## 1. vHsmDriverPreconfigDestination

- **UUID**: `531a0767-5bba-4d56-bc74-c5baec6582f5`
- **参数名**: `vHsmDriverPreconfigDestination`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **字符串变体**:
  - 默认值: `$(GenDataFolder)/vHsmPreconfig_$(InstanceName)/Crypto_30_vHsm_bswmd_Pre.arxml`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The vHSM is always generation a Pre-Config file for the Crypto_30_vHsm which can be used to sync the configuration between the vHsm and the driver which is located inside another SIP.
With this parameter, the target folder and filename of the generated Pre-Config file can be influenced.
If parameter is no present or empty, the pre config is generated in the following directory:
$(GenDataFolder)/vHsmPreconfig_$(InstanceName)/Crypto_30_vHsm_bswmd_Pre.arxml

The Pre-Config file will contain:
- The available primitives inside the vHsm_LibCv driver object
- The available and configured keys of the LibCv driver including its types and elements.
- Some vHSM data like Protocol and Sync parameter

Specify the path to the file e.g.:
- C:\Vector\vHsm\Crypto_30_vHsm_bswmd_Pre.arxml
- $(DpaProjectFolder)\Config\vHsmPreConfig\Crypto_30_vHsm_bswmd_Pre.arxml

Beside the DaVinci Configurator variables, $(InstanceName) can be used as placeholder to use the shortname of this IPC instance in the path.

Attention: Target folder should exist, only the last folder can be created during generation! 

In the application configuration of the other SIP containing the crypto driver, add the folder with the generated Pre-Config to the Additional Definitions using the Project Settings Dialog.

########## 2. vHsmIpcAddress

- **UUID**: `6f9c3ecd-262d-46a2-bb31-1856fcefe15c`
- **参数名**: `vHsmIpcAddress`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **字符串变体**:
  - 默认值: `VHSM_IPC_MEMORY_ADDRESS`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Linker-Symbol or Address of the IPC memory.

If this parameter is not available, the vHsm Firmware generates a buffer (shared IPC memory) which needs to be linked to the correct address in the memory.

If the parameter is created, the address is used and no buffer is created.
The memory area needs to be reserved e.g. by the linker scrip

######## 引用关系

此容器包含 **1** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. vHsmDriverObjectMapping

- **UUID**: `ec42139c-b063-48c9-b7ca-46c93f0015c6`
- **引用名**: `vHsmDriverObjectMapping`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..infinite]
- **目标**: `CryIfChannel`
- **完整路径**: `/MICROSAR/CryIf/CryIfChannel`
- **来源**: Vector Informatik
- **需要索引**: true
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Map the driver objects of the application side to CryIf channels on the vHsm.

When IPC Protocol Version 1 is used, the following mapping is requested.
0: Crypto_30_vHsm_Core
1: Crypto_30_vHsm_Hal
2: Crypto_30_vHsm_LibCv
3: Crypto_30_vHsm_KeyM

##### 9. vHsmIpcInstance

**容器属性**:

- **UUID**: `ae5437ef-fbaa-4b58-8aed-db7c2ed2c750`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vHsmIpcInstance`
- **多重性**: [1..255]
- **构建后可变**: false

**容器描述**:

This container represents an IPC instance and therefore the number of distinct memory areas of which each contain an IPC which will be polled for incoming jobs.

If there are more than one Instance of a corresponding vHSM Crypto Driver on application side (e,g, one per core) , create one instance for each.

###### 参数配置

此容器包含 **6** 个参数：

####### INTEGER 类型参数

######## 1. vHsmIpcHardwareUnit

- **UUID**: `b624cdd4-0c72-4288-be48-ed9bc8213f25`
- **参数名**: `vHsmIpcHardwareUnit`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..255]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Id of the Hw IPC which is used to determine the init state of the IPC or to provide the ready state of the HSM

Most platforms only have one hardware unit. Therefore the parameter is mostly set to 0.
Depending on the used platform, a hardware unit can either be a dedicated IPC hardware/channel or just a register.

######## 2. vHsmResponseInterruptFlagSetMask

- **UUID**: `ebdc4004-fb44-41a6-b937-cd113c7adcd3`
- **参数名**: `vHsmResponseInterruptFlagSetMask`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `1`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The mask which will be written to the register which triggers an interrupt the the Host core

######## 3. vHsmIpcInstanceId

- **UUID**: `e84cbfe3-4c6f-4eb4-8c52-eb086055cec0`
- **参数名**: `vHsmIpcInstanceId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..255]
- **来源**: Vector Informatik
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Id of the Ipc instance

######## 4. vHsmResponseInterruptFlagSetAddress

- **UUID**: `3d552f29-e4da-4716-86fc-6056c39cb82f`
- **参数名**: `vHsmResponseInterruptFlagSetAddress`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Address of the register which is used to trigger the interrupt to the host core

####### STRING 类型参数

######## 1. vHsmDriverPreconfigDestination

- **UUID**: `531a0767-5bba-4d56-bc74-c5baec6582f5`
- **参数名**: `vHsmDriverPreconfigDestination`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **字符串变体**:
  - 默认值: `$(GenDataFolder)/vHsmPreconfig_$(InstanceName)/Crypto_30_vHsm_bswmd_Pre.arxml`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The vHSM is always generation a Pre-Config file for the Crypto_30_vHsm which can be used to sync the configuration between the vHsm and the driver which is located inside another SIP.
With this parameter, the target folder and filename of the generated Pre-Config file can be influenced.
If parameter is no present or empty, the pre config is generated in the following directory:
$(GenDataFolder)/vHsmPreconfig_$(InstanceName)/Crypto_30_vHsm_bswmd_Pre.arxml

The Pre-Config file will contain:
- The available primitives inside the vHsm_LibCv driver object
- The available and configured keys of the LibCv driver including its types and elements.
- Some vHSM data like Protocol and Sync parameter

Specify the path to the file e.g.:
- C:\Vector\vHsm\Crypto_30_vHsm_bswmd_Pre.arxml
- $(DpaProjectFolder)\Config\vHsmPreConfig\Crypto_30_vHsm_bswmd_Pre.arxml

Beside the DaVinci Configurator variables, $(InstanceName) can be used as placeholder to use the shortname of this IPC instance in the path.

Attention: Target folder should exist, only the last folder can be created during generation! 

In the application configuration of the other SIP containing the crypto driver, add the folder with the generated Pre-Config to the Additional Definitions using the Project Settings Dialog.

######## 2. vHsmIpcAddress

- **UUID**: `6f9c3ecd-262d-46a2-bb31-1856fcefe15c`
- **参数名**: `vHsmIpcAddress`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **字符串变体**:
  - 默认值: `VHSM_IPC_MEMORY_ADDRESS`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Linker-Symbol or Address of the IPC memory.

If this parameter is not available, the vHsm Firmware generates a buffer (shared IPC memory) which needs to be linked to the correct address in the memory.

If the parameter is created, the address is used and no buffer is created.
The memory area needs to be reserved e.g. by the linker scrip

###### 引用关系

此容器包含 **1** 个引用：

####### SYMBOLIC-NAME-REFERENCE 类型引用

######## 1. vHsmDriverObjectMapping

- **UUID**: `ec42139c-b063-48c9-b7ca-46c93f0015c6`
- **引用名**: `vHsmDriverObjectMapping`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..infinite]
- **目标**: `CryIfChannel`
- **完整路径**: `/MICROSAR/CryIf/CryIfChannel`
- **来源**: Vector Informatik
- **需要索引**: true
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Map the driver objects of the application side to CryIf channels on the vHsm.

When IPC Protocol Version 1 is used, the following mapping is requested.
0: Crypto_30_vHsm_Core
1: Crypto_30_vHsm_Hal
2: Crypto_30_vHsm_LibCv
3: Crypto_30_vHsm_KeyM

##### 10. vHsmFirmwareUpdate

**容器属性**:

- **UUID**: `da86fe5e-0b93-4cf8-900f-25bc7e5e1b73`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vHsmFirmwareUpdate`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Used to configure the vHsm Firmware Update

###### 参数配置

此容器包含 **2** 个参数：

####### BOOLEAN 类型参数

######## 1. vHsmJumpToUpdaterRestriction

- **UUID**: `5184cbd4-6de3-4909-b02e-15c25693ef5a`
- **参数名**: `vHsmJumpToUpdaterRestriction`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Allow the jump to updater only when the firmware update job was successful.
If this option is disabled, a preceding firmware update job is not necessary to be able to let the vHsm Firmware jump to the updater.

####### LINKER-SYMBOL 类型参数

######## 1. vHsmUpdaterAddress

- **UUID**: `b3cb75a0-3b22-43fa-b51b-930e1c53a849`
- **参数名**: `vHsmUpdaterAddress`
- **数据类型**: LINKER-SYMBOL
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **字符串变体**:
  - 默认值: `VHSM_FIRMWARE_UPDATER`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Label of the Address of the vhsm Firmware Updater.

This label will be used as jump address after Crypto_30_vHsm_KeyElementSet has been called for the key element CRYPTO_KE_CUSTOM_VHSM_FIRMWARE_UPDATE_START_UPDATER after a firmware update job has been executed successfully.

###### 引用关系

此容器包含 **4** 个引用：

####### SYMBOLIC-NAME-REFERENCE 类型引用

######## 1. vHsmFirmwareUpdateCsmJobSignatureVerifyRef

- **UUID**: `15b38ec8-3d1f-427f-b3ee-0e4133f00b31`
- **引用名**: `vHsmFirmwareUpdateCsmJobSignatureVerifyRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `CsmJob`
- **完整路径**: `/AUTOSAR/EcucDefs/Csm/CsmJobs/CsmJob`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the Job used for the signature verification over the received update container containing the encrypted firmware.

######## 2. vHsmFirmwareUpdateCsmJobDecryptRef

- **UUID**: `78c1ec6d-e64c-4f4d-a78f-1ffd7e81dcda`
- **引用名**: `vHsmFirmwareUpdateCsmJobDecryptRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `CsmJob`
- **完整路径**: `/AUTOSAR/EcucDefs/Csm/CsmJobs/CsmJob`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the Job used for the decryption of the received encrypted firmware to get the firmware binary as plaintext.

When recryption shall not be done, delete this reference.

######## 3. vHsmFirmwareUpdateCsmJobMacGenerateRef

- **UUID**: `d72ddfbb-b2e1-4618-be99-a8d7fd50ac2d`
- **引用名**: `vHsmFirmwareUpdateCsmJobMacGenerateRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `CsmJob`
- **完整路径**: `/AUTOSAR/EcucDefs/Csm/CsmJobs/CsmJob`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the Job used for the MAC generation over the decrypted firmware binary.

######## 4. vHsmFirmwareUpdateCsmJobEncryptRef

- **UUID**: `7466da66-b53d-4ef8-9ae0-27beaf93e541`
- **引用名**: `vHsmFirmwareUpdateCsmJobEncryptRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `CsmJob`
- **完整路径**: `/AUTOSAR/EcucDefs/Csm/CsmJobs/CsmJob`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the Job used for the encryption of the firmware binary. The result can be stored by the application core and will later be used by the vHsm Updater.

When recryption shall not be done, delete this reference.

##### 11. vHsmSecureBoot

**容器属性**:

- **UUID**: `ed63441e-1670-44d9-a1d4-0ff0f9d73233`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vHsmSecureBoot`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Configure secure boot related parameters

###### 参数配置

此容器包含 **6** 个参数：

####### INTEGER 类型参数

######## 1. vHsmSecureBootSplitSize

- **UUID**: `60cdbf90-0e02-4fc9-9018-687809697869`
- **参数名**: `vHsmSecureBootSplitSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `256`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: During secure boot it is possible to do job processing in the meantime. To get a low latency in job processing, the secure boot segment check can be divided into multiple computation chunks. The number of bytes which will be checked in each chunk can be configured with this parameter.

######## 2. vHsmSecureBootQueueSize

- **UUID**: `7961004b-557e-4e55-85e7-78f6978ff6e9`
- **参数名**: `vHsmSecureBootQueueSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `10`
- **取值范围**: [2..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Number of parallel secure boot segments which can be processed.

######## 3. vHsmSecureBootCyclicVerificationSplitSize

- **UUID**: `f2ee7574-9bbd-4306-a34c-0cb38ee7747f`
- **参数名**: `vHsmSecureBootCyclicVerificationSplitSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `256`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: During secure boot it is possible to do job processing in the meantime. To get a low latency in job processing, the cyclic verification of secure boot segment can be divided into multiple computation chunks. The number of bytes which will be checked in each chunk can be configured with this parameter.

####### BOOLEAN 类型参数

######## 1. vHsmSecureBootSegmentSuccessCallout

- **UUID**: `b828e08c-7b1b-40e7-9ed3-65e5b0c4911b`
- **参数名**: `vHsmSecureBootSegmentSuccessCallout`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enable triggering the call of vHsm_SecureBoot_SegmentSuccess_Callout(groupId) if the verification of a segment was successful.

######## 2. vHsmSecureBootForcedSequentialProcessingOnFirstVerification

- **UUID**: `9c336ebe-7b4b-473f-b74c-3911e1c42b77`
- **参数名**: `vHsmSecureBootForcedSequentialProcessingOnFirstVerification`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Force parallel segments to be processed sequential/immediately on their first verification. This leads to the CMAC being written to the data flash and will be always available for comparison on subsequent startups.

Info:
On the first verification of a secure boot slot, there will be write access to the data flash because of storing the CMAC.
This can lead to issues when performing parallel secure boot verification on platforms which are not able to process concurrent data flash access from HSM and Application core at the same time.

Enabling the option is only needed when:
- Platform does not allow concurrent data flash access
- Parallel segments have not been provisioned with the secure boot update

Attention:
- Enabling this option may lead to increased startup time during the first startup when there are autostart groups containing parallel segments.
- Ensure that when the segment verification is triggered from the application core, the HSM is allowed to write to the data flash.

####### ENUMERATION 类型参数

######## 1. vHsmSecureBootStorageMethod

- **UUID**: `e8f5c7cb-f6eb-4960-a2d1-525022084432`
- **参数名**: `vHsmSecureBootStorageMethod`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `VHSM_STORAGE_IN_NVM`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `VHSM_STORAGE_IN_CSM` (来源: Vector Informatik)
  - `VHSM_STORAGE_IN_NVM` (来源: Vector Informatik)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Select the storage type of the secure boot information.

VHSM_STORAGE_IN_NVM:
The NvM is directly used for the key storage. This reduces memory overhead (RAM, Data and Code flash).

VHSM_STORAGE_IN_CSM (deprecated):
Keys and key elements are used to store the secure boot information.
Persisting is done by the LibCv driver with the help of the NvM in the background.

###### 配置容器

本模块包含 **12** 个配置容器：

####### 1. vHsmSecureBootGroup

**容器属性**:

- **UUID**: `218f87a7-0e59-4b76-8291-6a2682932dfc`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vHsmSecureBootGroup`
- **多重性**: [1..infinite]
- **构建后可变**: false

**容器描述**:

Container describing a secure boot group which can be used to group and process multiple segments at once.

Also the autostart behavior and its conditions can be configured for each secure boot group.

All segments in a group can be reconfigured with a secure boot update.

######## 参数配置

此容器包含 **6** 个参数：

######### INTEGER 类型参数

########## 1. vHsmSecureBootGroupId

- **UUID**: `0f20a585-b001-4c85-b44d-dc742c5f94ea`
- **参数名**: `vHsmSecureBootGroupId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Unique Id can be chosen freely to identify a Secure Boot Group used in the Segmentation List.

########## 2. vHsmNvBlockRevision

- **UUID**: `c8515822-0448-413c-b04e-3cd90c52b351`
- **参数名**: `vHsmNvBlockRevision`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Revision of the NvBlock.

If this parameter is changed, the CRC will change and the NvBlock will be invalid which will result in the secure boot beeing set to initial values.

########## 3. vHsmNvBlockCrcLayoutChecksum

- **UUID**: `823ccd68-bd86-4fdf-90e5-80113ec5e13d`
- **参数名**: `vHsmNvBlockCrcLayoutChecksum`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: CRC checksum over the NvBlock layout.
If the CRC does not match the data flash content, the secure boot information for this group will b set to the initial values.

CRC Calculation is influenced by:
- Number of segments
- Tag length of the reerenced verification method
- Tag handling
- NvBlock revision

######### BOOLEAN 类型参数

########## 1. vHsmAutostart

- **UUID**: `4e0369e2-20c8-4058-9139-5c31718bc93a`
- **参数名**: `vHsmAutostart`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: TRUE:
The verification will be started during startup of the vHsm.
This can be restricted by a runtime condition like a custom callout. See /MICROSAR/vHsm/vHsmSecureBoot/vHsmSecureBootGroup/vHsmAutostartCondition

FALSE:
The verification of the slot is started by e.g the bootloader.

########## 2. vHsmCyclicVerification

- **UUID**: `cf0eddf9-d32d-4d99-9626-01b626507166`
- **参数名**: `vHsmCyclicVerification`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: If enabled, this option will restart the verification of the group and the contained parallel and sequential segments.
This way, the segments will be verified continuously.

######### ENUMERATION 类型参数

########## 1. vHsmTagHandling

- **UUID**: `8dd10d58-8832-45d9-9e4e-d3fc0f141a1a`
- **参数名**: `vHsmTagHandling`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `VHSM_GROUP_TAG`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `VHSM_GROUP_TAG` (来源: Vector Informatik)
  - `VHSM_PROCESSING_TAG` (来源: Vector Informatik)
  - `VHSM_SEGMENT_TAG` (来源: Vector Informatik)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: A tag is needed in order to detect memory manipulations in flash.
The different methods of tag handling are described below with specific advantages (+) and disadvantages (-).

VHSM_GROUP_TAG
- Sanctions and processing must be same for all segments in the group
- SegmentList during secure boot update can either contain sequential or parallel segments. (Processing mode NONE is additionally possible in both cases)
- Single segments can not be selected for processing individually during secure boot

VHSM_PROCESSING_TAG:
+ Each group needs to store 2 tags
+ SegmentList during secure boot update can contain both sequential and parallel segements
+ Different algorithms for sequential and parallel jobs are possible
- Sanction must be the same for all segments in the group -> only one sanction is triggered if one of the segments fail 
- Single segments can not be selected for processing individually processing

VHSM_SEGMENT_TAG:
+ SegmentList during secure boot update can contain both sequential and parallel segements
+ Sanctions can be configured for each segment individually
+ Starting the secure boot processing of a single segment is possible
- Each segment needs to store a tag.
- Sequential and Parallel Csm jobs need to use the same algorithm

######## 引用关系

此容器包含 **2** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. vHsmKeyRef

- **UUID**: `ce6fe3f9-9584-474b-9798-e5425838bed1`
- **引用名**: `vHsmKeyRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `CryIfKey`
- **完整路径**: `/AUTOSAR/EcucDefs/CryIf/CryIfKey`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This key can be used in a MacVerify job to start a verification of the whole SecureBootGroup when no input data containg the GroupId is provided.

KeyRef is deprecated

########## 2. vHsmNvBlockDescriptor

- **UUID**: `e5da539a-d481-421d-8998-c335cd495019`
- **引用名**: `vHsmNvBlockDescriptor`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `NvMBlockDescriptor`
- **完整路径**: `/AUTOSAR/EcucDefs/NvM/NvMBlockDescriptor`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a NvM block descriptor which will be used to persist the secure boot information of this secure boot group.

######## 配置容器

本模块包含 **8** 个配置容器：

######### 1. vHsmCustomCallout

**容器属性**:

- **UUID**: `70f2bcd9-687f-4697-af41-008ad7a4659d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vHsmCustomCallout`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

boolean vHsm_Custom_IsSecureBootAllowAutostart_Callout(vHsm_SecureBootGroupIterType secureBootGroupIndex) is called.
If the function returns TRUE, the autostart will be performed. This can be used for e.g. checking the current reset vector.

######### 2. vHsmSecureBootSegment

**容器属性**:

- **UUID**: `35777e45-8dbf-4d3f-858c-dae853063b66`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vHsmSecureBootSegment`
- **多重性**: [0..infinite]
- **构建后可变**: false

**容器描述**:

A secure boot segment is a memory area which can be secured with a CMAC during secure boot.
A segment is part of a group and can be updated with secure software download or as part of a secure boot update.

########## 引用关系

此容器包含 **1** 个引用：

########### SYMBOLIC-NAME-REFERENCE 类型引用

############ 1. vHsmKeyRef

- **UUID**: `d8c1b9c8-4c75-4716-8db9-bf607b1a4eef`
- **引用名**: `vHsmKeyRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `CryIfKey`
- **完整路径**: `/AUTOSAR/EcucDefs/CryIf/CryIfKey`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: When storage method is set to VHSM_STORAGE_IN_CSM:
The referenced key is used to store the information of this segment
It will contain the address, size, tag and sanction.
The values will be updated to new values with the secure software download or secure boot update.

Key Ref is deprecated

########## 配置容器

本模块包含 **1** 个配置容器：

########### 1. vHsmSecureBootSegmentInitValues

**容器属性**:

- **UUID**: `4c7f1d37-8e2f-4c19-8ffe-d45bef25fefe`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vHsmSecureBootSegmentInitValues`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Init values for the segment. The values can be changed during runtime with secure boot update and secure software download.

############ 参数配置

此容器包含 **4** 个参数：

############# INTEGER 类型参数

############## 1. vHsmAddress

- **UUID**: `0c0de5a6-de65-4635-848a-066775ddcd7a`
- **参数名**: `vHsmAddress`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is the init value which will be stored during the startup.

Attention:
It will overwrite the init value configured for the key element!

############## 2. vHsmLength

- **UUID**: `a23e1739-3c6b-4182-b604-2e46a2426e13`
- **参数名**: `vHsmLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is the init value which will be stored during the startup.

Attention:
It will overwrite the init value configured for the key element!

############# ENUMERATION 类型参数

############## 1. vHsmSanction

- **UUID**: `f58d3edc-b54f-4260-ac6b-8b587f769adc`
- **参数名**: `vHsmSanction`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `SANCTION_RESET`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `SANCTION_NONE`
  - `SANCTION_RESET`
  - `SANCTION_HALT`
  - `SANCTION_CUSTOM`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The sanction which shall be performed

############## 2. vHsmSecureBootMode

- **UUID**: `81343282-e3ed-461b-b3d0-81d9a4eaff5b`
- **参数名**: `vHsmSecureBootMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `SEQUENTIAL`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `SEQUENTIAL`
  - `PARALLEL`
  - `NONE`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Processing Type of the segment.

######### 3. vHsmSecureBootSegmentInitValues

**容器属性**:

- **UUID**: `4c7f1d37-8e2f-4c19-8ffe-d45bef25fefe`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vHsmSecureBootSegmentInitValues`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Init values for the segment. The values can be changed during runtime with secure boot update and secure software download.

########## 参数配置

此容器包含 **4** 个参数：

########### INTEGER 类型参数

############ 1. vHsmAddress

- **UUID**: `0c0de5a6-de65-4635-848a-066775ddcd7a`
- **参数名**: `vHsmAddress`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is the init value which will be stored during the startup.

Attention:
It will overwrite the init value configured for the key element!

############ 2. vHsmLength

- **UUID**: `a23e1739-3c6b-4182-b604-2e46a2426e13`
- **参数名**: `vHsmLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is the init value which will be stored during the startup.

Attention:
It will overwrite the init value configured for the key element!

########### ENUMERATION 类型参数

############ 1. vHsmSanction

- **UUID**: `f58d3edc-b54f-4260-ac6b-8b587f769adc`
- **参数名**: `vHsmSanction`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `SANCTION_RESET`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `SANCTION_NONE`
  - `SANCTION_RESET`
  - `SANCTION_HALT`
  - `SANCTION_CUSTOM`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The sanction which shall be performed

############ 2. vHsmSecureBootMode

- **UUID**: `81343282-e3ed-461b-b3d0-81d9a4eaff5b`
- **参数名**: `vHsmSecureBootMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `SEQUENTIAL`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `SEQUENTIAL`
  - `PARALLEL`
  - `NONE`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Processing Type of the segment.

######### 4. vHsmCustomCalloutCyclic

**容器属性**:

- **UUID**: `065a1e5e-3cd4-4ab9-b8e0-1dffcca6adb5`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vHsmCustomCalloutCyclic`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

boolean vHsm_Custom_IsSecureBootAllowCyclic_Callout(vHsm_SecureBootGroupIterType secureBootGroupIndex, uint32 secureBootGroup) is called.
If the function returns TRUE, the cyclic verification will be performed. This can be used for disabling the cyclic verification during FBL and only enable it during APPL runtime.

######### 5. vHsmCompareInternalTag

**容器属性**:

- **UUID**: `6fe03620-c0d0-48f7-ad35-8d74ef30db6a`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vHsmCompareInternalTag`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Compare a computed Tag (e.g. Cmac or Hash) against a Tag stored in the NvM.

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. vHsmTagLength

- **UUID**: `8f773b00-5a2a-43e9-91a0-fc42f9b5d816`
- **参数名**: `vHsmTagLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `16`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Length of the Tag (e.g. CMAC or HASH)

Autofilled with information from CsmJobs

########## 引用关系

此容器包含 **1** 个引用：

########### SYMBOLIC-NAME-REFERENCE 类型引用

############ 1. vHsmVerificationJobRef

- **UUID**: `8f46e262-de8a-4181-8d80-6c7b9da07267`
- **引用名**: `vHsmVerificationJobRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `vHsmSecureBootVerificationJob`
- **完整路径**: `/MICROSAR/vHsm/vHsmSecureBoot/vHsmSecureBootVerificationJob`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a job tuple containing the references for sequential and parallel jobs

######### 6. vHsmAutostartCondition

**容器属性**:

- **UUID**: `5892b0e1-1c3f-4ec1-bb8f-0af7e32dee09`
- **容器类型**: CHOICE-CONTAINER
- **容器名称**: `vHsmAutostartCondition`
- **多重性**: [0..1]
- **构建后可变**: false

**容器选择**:

- **vHsmCustomCallout**
  - UUID: `70f2bcd9-687f-4697-af41-008ad7a4659d`
  - 描述: boolean vHsm_Custom_IsSecureBootAllowAutostart_Callout(vHsm_SecureBootGroupIterType secureBootGroupIndex) is called.
If the function returns TRUE, the autostart will be performed. This can be used for e.g. checking the current reset vector.

**容器描述**:

Define a condition under which the autostart will be performed.
This way, the autostart of a group can be blocked if a condition is not met.

######### 7. vHsmCyclicCondition

**容器属性**:

- **UUID**: `5b43cd09-83c1-476e-a114-4c34b33a630e`
- **容器类型**: CHOICE-CONTAINER
- **容器名称**: `vHsmCyclicCondition`
- **多重性**: [0..1]
- **构建后可变**: false

**容器选择**:

- **vHsmCustomCalloutCyclic**
  - UUID: `065a1e5e-3cd4-4ab9-b8e0-1dffcca6adb5`
  - 描述: boolean vHsm_Custom_IsSecureBootAllowCyclic_Callout(vHsm_SecureBootGroupIterType secureBootGroupIndex, uint32 secureBootGroup) is called.
If the function returns TRUE, the cyclic verification will be performed. This can be used for disabling the cyclic verification during FBL and only enable it during APPL runtime.

**容器描述**:

Define a condition under which the autostart will be performed.
This way, the autostart of a group can be blocked if a condition is not met.

######### 8. vHsmVerificationMethod

**容器属性**:

- **UUID**: `0bf5a696-87f9-43e4-bed3-da26c2118384`
- **容器类型**: CHOICE-CONTAINER
- **容器名称**: `vHsmVerificationMethod`
- **多重性**: [1..1]
- **构建后可变**: false

**容器选择**:

- **vHsmCompareInternalTag**
  - UUID: `6fe03620-c0d0-48f7-ad35-8d74ef30db6a`
  - 描述: Compare a computed Tag (e.g. Cmac or Hash) against a Tag stored in the NvM.

**容器描述**:

Method which shall be used to validate the secure boot group

####### 2. vHsmCustomCallout

**容器属性**:

- **UUID**: `70f2bcd9-687f-4697-af41-008ad7a4659d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vHsmCustomCallout`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

boolean vHsm_Custom_IsSecureBootAllowAutostart_Callout(vHsm_SecureBootGroupIterType secureBootGroupIndex) is called.
If the function returns TRUE, the autostart will be performed. This can be used for e.g. checking the current reset vector.

####### 3. vHsmSecureBootSegment

**容器属性**:

- **UUID**: `35777e45-8dbf-4d3f-858c-dae853063b66`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vHsmSecureBootSegment`
- **多重性**: [0..infinite]
- **构建后可变**: false

**容器描述**:

A secure boot segment is a memory area which can be secured with a CMAC during secure boot.
A segment is part of a group and can be updated with secure software download or as part of a secure boot update.

######## 引用关系

此容器包含 **1** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. vHsmKeyRef

- **UUID**: `d8c1b9c8-4c75-4716-8db9-bf607b1a4eef`
- **引用名**: `vHsmKeyRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `CryIfKey`
- **完整路径**: `/AUTOSAR/EcucDefs/CryIf/CryIfKey`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: When storage method is set to VHSM_STORAGE_IN_CSM:
The referenced key is used to store the information of this segment
It will contain the address, size, tag and sanction.
The values will be updated to new values with the secure software download or secure boot update.

Key Ref is deprecated

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. vHsmSecureBootSegmentInitValues

**容器属性**:

- **UUID**: `4c7f1d37-8e2f-4c19-8ffe-d45bef25fefe`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vHsmSecureBootSegmentInitValues`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Init values for the segment. The values can be changed during runtime with secure boot update and secure software download.

########## 参数配置

此容器包含 **4** 个参数：

########### INTEGER 类型参数

############ 1. vHsmAddress

- **UUID**: `0c0de5a6-de65-4635-848a-066775ddcd7a`
- **参数名**: `vHsmAddress`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is the init value which will be stored during the startup.

Attention:
It will overwrite the init value configured for the key element!

############ 2. vHsmLength

- **UUID**: `a23e1739-3c6b-4182-b604-2e46a2426e13`
- **参数名**: `vHsmLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is the init value which will be stored during the startup.

Attention:
It will overwrite the init value configured for the key element!

########### ENUMERATION 类型参数

############ 1. vHsmSanction

- **UUID**: `f58d3edc-b54f-4260-ac6b-8b587f769adc`
- **参数名**: `vHsmSanction`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `SANCTION_RESET`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `SANCTION_NONE`
  - `SANCTION_RESET`
  - `SANCTION_HALT`
  - `SANCTION_CUSTOM`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The sanction which shall be performed

############ 2. vHsmSecureBootMode

- **UUID**: `81343282-e3ed-461b-b3d0-81d9a4eaff5b`
- **参数名**: `vHsmSecureBootMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `SEQUENTIAL`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `SEQUENTIAL`
  - `PARALLEL`
  - `NONE`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Processing Type of the segment.

####### 4. vHsmSecureBootSegmentInitValues

**容器属性**:

- **UUID**: `4c7f1d37-8e2f-4c19-8ffe-d45bef25fefe`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vHsmSecureBootSegmentInitValues`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Init values for the segment. The values can be changed during runtime with secure boot update and secure software download.

######## 参数配置

此容器包含 **4** 个参数：

######### INTEGER 类型参数

########## 1. vHsmAddress

- **UUID**: `0c0de5a6-de65-4635-848a-066775ddcd7a`
- **参数名**: `vHsmAddress`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is the init value which will be stored during the startup.

Attention:
It will overwrite the init value configured for the key element!

########## 2. vHsmLength

- **UUID**: `a23e1739-3c6b-4182-b604-2e46a2426e13`
- **参数名**: `vHsmLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is the init value which will be stored during the startup.

Attention:
It will overwrite the init value configured for the key element!

######### ENUMERATION 类型参数

########## 1. vHsmSanction

- **UUID**: `f58d3edc-b54f-4260-ac6b-8b587f769adc`
- **参数名**: `vHsmSanction`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `SANCTION_RESET`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `SANCTION_NONE`
  - `SANCTION_RESET`
  - `SANCTION_HALT`
  - `SANCTION_CUSTOM`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The sanction which shall be performed

########## 2. vHsmSecureBootMode

- **UUID**: `81343282-e3ed-461b-b3d0-81d9a4eaff5b`
- **参数名**: `vHsmSecureBootMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `SEQUENTIAL`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `SEQUENTIAL`
  - `PARALLEL`
  - `NONE`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Processing Type of the segment.

####### 5. vHsmCustomCalloutCyclic

**容器属性**:

- **UUID**: `065a1e5e-3cd4-4ab9-b8e0-1dffcca6adb5`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vHsmCustomCalloutCyclic`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

boolean vHsm_Custom_IsSecureBootAllowCyclic_Callout(vHsm_SecureBootGroupIterType secureBootGroupIndex, uint32 secureBootGroup) is called.
If the function returns TRUE, the cyclic verification will be performed. This can be used for disabling the cyclic verification during FBL and only enable it during APPL runtime.

####### 6. vHsmCompareInternalTag

**容器属性**:

- **UUID**: `6fe03620-c0d0-48f7-ad35-8d74ef30db6a`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vHsmCompareInternalTag`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Compare a computed Tag (e.g. Cmac or Hash) against a Tag stored in the NvM.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. vHsmTagLength

- **UUID**: `8f773b00-5a2a-43e9-91a0-fc42f9b5d816`
- **参数名**: `vHsmTagLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `16`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Length of the Tag (e.g. CMAC or HASH)

Autofilled with information from CsmJobs

######## 引用关系

此容器包含 **1** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. vHsmVerificationJobRef

- **UUID**: `8f46e262-de8a-4181-8d80-6c7b9da07267`
- **引用名**: `vHsmVerificationJobRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `vHsmSecureBootVerificationJob`
- **完整路径**: `/MICROSAR/vHsm/vHsmSecureBoot/vHsmSecureBootVerificationJob`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a job tuple containing the references for sequential and parallel jobs

####### 7. vHsmSecureBootUpdate

**容器属性**:

- **UUID**: `759eef6d-a201-430c-8e3c-2d85b4194263`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vHsmSecureBootUpdate`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

This container configures the CSM jobs used for hash and signature generation. Secureboot update uses a signed segment list to update the secure boot segments of a group.

######## 引用关系

此容器包含 **2** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. vHsmCsmSignatureJobReference

- **UUID**: `53191050-f523-4adb-b3a9-6997cd3f16e7`
- **引用名**: `vHsmCsmSignatureJobReference`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `CsmJob`
- **完整路径**: `/AUTOSAR/EcucDefs/Csm/CsmJobs/CsmJob`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter references a CSM signature job used to calculate signatures for secure boot update.

########## 2. vHsmCsmHashJobReference

- **UUID**: `8a0dd456-9e80-4081-b910-3a0de851c7f5`
- **引用名**: `vHsmCsmHashJobReference`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `CsmJob`
- **完整路径**: `/AUTOSAR/EcucDefs/Csm/CsmJobs/CsmJob`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter references a CSM hash job used for secure secure boot update.

####### 8. vHsmSecureSoftwareDownload

**容器属性**:

- **UUID**: `db59c55e-0214-468c-a324-c4c58279172f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vHsmSecureSoftwareDownload`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

This container configured the key, channel und primitive used during secure software download which uses signed data to update a single secure boot segment.

Deprecated

######## 参数配置

此容器包含 **1** 个参数：

######### BOOLEAN 类型参数

########## 1. vHsmAllowAddressChange

- **UUID**: `0610360e-507b-4311-9937-85a836519c16`
- **参数名**: `vHsmAllowAddressChange`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Allow the change of the address during secure software download.
If disabled, this implies that a correct init value for the address is already set in each secure boot segment.

######## 引用关系

此容器包含 **1** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. vHsmCsmSignatureJobReference

- **UUID**: `0a3eab80-eeee-480d-bf16-f2c295febe18`
- **引用名**: `vHsmCsmSignatureJobReference`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `CsmJob`
- **完整路径**: `/AUTOSAR/EcucDefs/Csm/CsmJobs/CsmJob`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter references a CSM signature job used to calculate the signature for secure software download

####### 9. vHsmSecureBootVerificationJob

**容器属性**:

- **UUID**: `f69436fc-1371-4686-9f92-b5ab4cf405ad`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vHsmSecureBootVerificationJob`
- **多重性**: [1..infinite]
- **构建后可变**: false

**容器描述**:

Contains the jobs which will be used for verification.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. vHsmSecureBootVerificationJobId

- **UUID**: `e4e86f4f-de35-454c-acbc-251448d0f260`
- **参数名**: `vHsmSecureBootVerificationJobId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Id of the verification job

######## 引用关系

此容器包含 **2** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. vHsmCsmJobSequentialRef

- **UUID**: `6ab801eb-55aa-4629-ae24-d7b147f3a7b0`
- **引用名**: `vHsmCsmJobSequentialRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `CsmJob`
- **完整路径**: `/AUTOSAR/EcucDefs/Csm/CsmJobs/CsmJob`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a CSM job which will be used for the sequential verification of the secure boot group.

########## 2. vHsmCsmJobParallelRef

- **UUID**: `6d887bca-e698-40c8-a398-866fb3bd48dc`
- **引用名**: `vHsmCsmJobParallelRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `CsmJob`
- **完整路径**: `/AUTOSAR/EcucDefs/Csm/CsmJobs/CsmJob`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a CSM job which will be used for the parallel verification of the secure boot group.

####### 10. vHsmAutostartCondition

**容器属性**:

- **UUID**: `5892b0e1-1c3f-4ec1-bb8f-0af7e32dee09`
- **容器类型**: CHOICE-CONTAINER
- **容器名称**: `vHsmAutostartCondition`
- **多重性**: [0..1]
- **构建后可变**: false

**容器选择**:

- **vHsmCustomCallout**
  - UUID: `70f2bcd9-687f-4697-af41-008ad7a4659d`
  - 描述: boolean vHsm_Custom_IsSecureBootAllowAutostart_Callout(vHsm_SecureBootGroupIterType secureBootGroupIndex) is called.
If the function returns TRUE, the autostart will be performed. This can be used for e.g. checking the current reset vector.

**容器描述**:

Define a condition under which the autostart will be performed.
This way, the autostart of a group can be blocked if a condition is not met.

####### 11. vHsmCyclicCondition

**容器属性**:

- **UUID**: `5b43cd09-83c1-476e-a114-4c34b33a630e`
- **容器类型**: CHOICE-CONTAINER
- **容器名称**: `vHsmCyclicCondition`
- **多重性**: [0..1]
- **构建后可变**: false

**容器选择**:

- **vHsmCustomCalloutCyclic**
  - UUID: `065a1e5e-3cd4-4ab9-b8e0-1dffcca6adb5`
  - 描述: boolean vHsm_Custom_IsSecureBootAllowCyclic_Callout(vHsm_SecureBootGroupIterType secureBootGroupIndex, uint32 secureBootGroup) is called.
If the function returns TRUE, the cyclic verification will be performed. This can be used for disabling the cyclic verification during FBL and only enable it during APPL runtime.

**容器描述**:

Define a condition under which the autostart will be performed.
This way, the autostart of a group can be blocked if a condition is not met.

####### 12. vHsmVerificationMethod

**容器属性**:

- **UUID**: `0bf5a696-87f9-43e4-bed3-da26c2118384`
- **容器类型**: CHOICE-CONTAINER
- **容器名称**: `vHsmVerificationMethod`
- **多重性**: [1..1]
- **构建后可变**: false

**容器选择**:

- **vHsmCompareInternalTag**
  - UUID: `6fe03620-c0d0-48f7-ad35-8d74ef30db6a`
  - 描述: Compare a computed Tag (e.g. Cmac or Hash) against a Tag stored in the NvM.

**容器描述**:

Method which shall be used to validate the secure boot group

##### 12. vHsmSecureBootGroup

**容器属性**:

- **UUID**: `218f87a7-0e59-4b76-8291-6a2682932dfc`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vHsmSecureBootGroup`
- **多重性**: [1..infinite]
- **构建后可变**: false

**容器描述**:

Container describing a secure boot group which can be used to group and process multiple segments at once.

Also the autostart behavior and its conditions can be configured for each secure boot group.

All segments in a group can be reconfigured with a secure boot update.

###### 参数配置

此容器包含 **6** 个参数：

####### INTEGER 类型参数

######## 1. vHsmSecureBootGroupId

- **UUID**: `0f20a585-b001-4c85-b44d-dc742c5f94ea`
- **参数名**: `vHsmSecureBootGroupId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Unique Id can be chosen freely to identify a Secure Boot Group used in the Segmentation List.

######## 2. vHsmNvBlockRevision

- **UUID**: `c8515822-0448-413c-b04e-3cd90c52b351`
- **参数名**: `vHsmNvBlockRevision`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Revision of the NvBlock.

If this parameter is changed, the CRC will change and the NvBlock will be invalid which will result in the secure boot beeing set to initial values.

######## 3. vHsmNvBlockCrcLayoutChecksum

- **UUID**: `823ccd68-bd86-4fdf-90e5-80113ec5e13d`
- **参数名**: `vHsmNvBlockCrcLayoutChecksum`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: CRC checksum over the NvBlock layout.
If the CRC does not match the data flash content, the secure boot information for this group will b set to the initial values.

CRC Calculation is influenced by:
- Number of segments
- Tag length of the reerenced verification method
- Tag handling
- NvBlock revision

####### BOOLEAN 类型参数

######## 1. vHsmAutostart

- **UUID**: `4e0369e2-20c8-4058-9139-5c31718bc93a`
- **参数名**: `vHsmAutostart`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: TRUE:
The verification will be started during startup of the vHsm.
This can be restricted by a runtime condition like a custom callout. See /MICROSAR/vHsm/vHsmSecureBoot/vHsmSecureBootGroup/vHsmAutostartCondition

FALSE:
The verification of the slot is started by e.g the bootloader.

######## 2. vHsmCyclicVerification

- **UUID**: `cf0eddf9-d32d-4d99-9626-01b626507166`
- **参数名**: `vHsmCyclicVerification`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: If enabled, this option will restart the verification of the group and the contained parallel and sequential segments.
This way, the segments will be verified continuously.

####### ENUMERATION 类型参数

######## 1. vHsmTagHandling

- **UUID**: `8dd10d58-8832-45d9-9e4e-d3fc0f141a1a`
- **参数名**: `vHsmTagHandling`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `VHSM_GROUP_TAG`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `VHSM_GROUP_TAG` (来源: Vector Informatik)
  - `VHSM_PROCESSING_TAG` (来源: Vector Informatik)
  - `VHSM_SEGMENT_TAG` (来源: Vector Informatik)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: A tag is needed in order to detect memory manipulations in flash.
The different methods of tag handling are described below with specific advantages (+) and disadvantages (-).

VHSM_GROUP_TAG
- Sanctions and processing must be same for all segments in the group
- SegmentList during secure boot update can either contain sequential or parallel segments. (Processing mode NONE is additionally possible in both cases)
- Single segments can not be selected for processing individually during secure boot

VHSM_PROCESSING_TAG:
+ Each group needs to store 2 tags
+ SegmentList during secure boot update can contain both sequential and parallel segements
+ Different algorithms for sequential and parallel jobs are possible
- Sanction must be the same for all segments in the group -> only one sanction is triggered if one of the segments fail 
- Single segments can not be selected for processing individually processing

VHSM_SEGMENT_TAG:
+ SegmentList during secure boot update can contain both sequential and parallel segements
+ Sanctions can be configured for each segment individually
+ Starting the secure boot processing of a single segment is possible
- Each segment needs to store a tag.
- Sequential and Parallel Csm jobs need to use the same algorithm

###### 引用关系

此容器包含 **2** 个引用：

####### SYMBOLIC-NAME-REFERENCE 类型引用

######## 1. vHsmKeyRef

- **UUID**: `ce6fe3f9-9584-474b-9798-e5425838bed1`
- **引用名**: `vHsmKeyRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `CryIfKey`
- **完整路径**: `/AUTOSAR/EcucDefs/CryIf/CryIfKey`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This key can be used in a MacVerify job to start a verification of the whole SecureBootGroup when no input data containg the GroupId is provided.

KeyRef is deprecated

######## 2. vHsmNvBlockDescriptor

- **UUID**: `e5da539a-d481-421d-8998-c335cd495019`
- **引用名**: `vHsmNvBlockDescriptor`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `NvMBlockDescriptor`
- **完整路径**: `/AUTOSAR/EcucDefs/NvM/NvMBlockDescriptor`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a NvM block descriptor which will be used to persist the secure boot information of this secure boot group.

###### 配置容器

本模块包含 **8** 个配置容器：

####### 1. vHsmCustomCallout

**容器属性**:

- **UUID**: `70f2bcd9-687f-4697-af41-008ad7a4659d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vHsmCustomCallout`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

boolean vHsm_Custom_IsSecureBootAllowAutostart_Callout(vHsm_SecureBootGroupIterType secureBootGroupIndex) is called.
If the function returns TRUE, the autostart will be performed. This can be used for e.g. checking the current reset vector.

####### 2. vHsmSecureBootSegment

**容器属性**:

- **UUID**: `35777e45-8dbf-4d3f-858c-dae853063b66`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vHsmSecureBootSegment`
- **多重性**: [0..infinite]
- **构建后可变**: false

**容器描述**:

A secure boot segment is a memory area which can be secured with a CMAC during secure boot.
A segment is part of a group and can be updated with secure software download or as part of a secure boot update.

######## 引用关系

此容器包含 **1** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. vHsmKeyRef

- **UUID**: `d8c1b9c8-4c75-4716-8db9-bf607b1a4eef`
- **引用名**: `vHsmKeyRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `CryIfKey`
- **完整路径**: `/AUTOSAR/EcucDefs/CryIf/CryIfKey`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: When storage method is set to VHSM_STORAGE_IN_CSM:
The referenced key is used to store the information of this segment
It will contain the address, size, tag and sanction.
The values will be updated to new values with the secure software download or secure boot update.

Key Ref is deprecated

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. vHsmSecureBootSegmentInitValues

**容器属性**:

- **UUID**: `4c7f1d37-8e2f-4c19-8ffe-d45bef25fefe`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vHsmSecureBootSegmentInitValues`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Init values for the segment. The values can be changed during runtime with secure boot update and secure software download.

########## 参数配置

此容器包含 **4** 个参数：

########### INTEGER 类型参数

############ 1. vHsmAddress

- **UUID**: `0c0de5a6-de65-4635-848a-066775ddcd7a`
- **参数名**: `vHsmAddress`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is the init value which will be stored during the startup.

Attention:
It will overwrite the init value configured for the key element!

############ 2. vHsmLength

- **UUID**: `a23e1739-3c6b-4182-b604-2e46a2426e13`
- **参数名**: `vHsmLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is the init value which will be stored during the startup.

Attention:
It will overwrite the init value configured for the key element!

########### ENUMERATION 类型参数

############ 1. vHsmSanction

- **UUID**: `f58d3edc-b54f-4260-ac6b-8b587f769adc`
- **参数名**: `vHsmSanction`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `SANCTION_RESET`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `SANCTION_NONE`
  - `SANCTION_RESET`
  - `SANCTION_HALT`
  - `SANCTION_CUSTOM`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The sanction which shall be performed

############ 2. vHsmSecureBootMode

- **UUID**: `81343282-e3ed-461b-b3d0-81d9a4eaff5b`
- **参数名**: `vHsmSecureBootMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `SEQUENTIAL`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `SEQUENTIAL`
  - `PARALLEL`
  - `NONE`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Processing Type of the segment.

####### 3. vHsmSecureBootSegmentInitValues

**容器属性**:

- **UUID**: `4c7f1d37-8e2f-4c19-8ffe-d45bef25fefe`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vHsmSecureBootSegmentInitValues`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Init values for the segment. The values can be changed during runtime with secure boot update and secure software download.

######## 参数配置

此容器包含 **4** 个参数：

######### INTEGER 类型参数

########## 1. vHsmAddress

- **UUID**: `0c0de5a6-de65-4635-848a-066775ddcd7a`
- **参数名**: `vHsmAddress`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is the init value which will be stored during the startup.

Attention:
It will overwrite the init value configured for the key element!

########## 2. vHsmLength

- **UUID**: `a23e1739-3c6b-4182-b604-2e46a2426e13`
- **参数名**: `vHsmLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is the init value which will be stored during the startup.

Attention:
It will overwrite the init value configured for the key element!

######### ENUMERATION 类型参数

########## 1. vHsmSanction

- **UUID**: `f58d3edc-b54f-4260-ac6b-8b587f769adc`
- **参数名**: `vHsmSanction`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `SANCTION_RESET`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `SANCTION_NONE`
  - `SANCTION_RESET`
  - `SANCTION_HALT`
  - `SANCTION_CUSTOM`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The sanction which shall be performed

########## 2. vHsmSecureBootMode

- **UUID**: `81343282-e3ed-461b-b3d0-81d9a4eaff5b`
- **参数名**: `vHsmSecureBootMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `SEQUENTIAL`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `SEQUENTIAL`
  - `PARALLEL`
  - `NONE`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Processing Type of the segment.

####### 4. vHsmCustomCalloutCyclic

**容器属性**:

- **UUID**: `065a1e5e-3cd4-4ab9-b8e0-1dffcca6adb5`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vHsmCustomCalloutCyclic`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

boolean vHsm_Custom_IsSecureBootAllowCyclic_Callout(vHsm_SecureBootGroupIterType secureBootGroupIndex, uint32 secureBootGroup) is called.
If the function returns TRUE, the cyclic verification will be performed. This can be used for disabling the cyclic verification during FBL and only enable it during APPL runtime.

####### 5. vHsmCompareInternalTag

**容器属性**:

- **UUID**: `6fe03620-c0d0-48f7-ad35-8d74ef30db6a`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vHsmCompareInternalTag`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Compare a computed Tag (e.g. Cmac or Hash) against a Tag stored in the NvM.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. vHsmTagLength

- **UUID**: `8f773b00-5a2a-43e9-91a0-fc42f9b5d816`
- **参数名**: `vHsmTagLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `16`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Length of the Tag (e.g. CMAC or HASH)

Autofilled with information from CsmJobs

######## 引用关系

此容器包含 **1** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. vHsmVerificationJobRef

- **UUID**: `8f46e262-de8a-4181-8d80-6c7b9da07267`
- **引用名**: `vHsmVerificationJobRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `vHsmSecureBootVerificationJob`
- **完整路径**: `/MICROSAR/vHsm/vHsmSecureBoot/vHsmSecureBootVerificationJob`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a job tuple containing the references for sequential and parallel jobs

####### 6. vHsmAutostartCondition

**容器属性**:

- **UUID**: `5892b0e1-1c3f-4ec1-bb8f-0af7e32dee09`
- **容器类型**: CHOICE-CONTAINER
- **容器名称**: `vHsmAutostartCondition`
- **多重性**: [0..1]
- **构建后可变**: false

**容器选择**:

- **vHsmCustomCallout**
  - UUID: `70f2bcd9-687f-4697-af41-008ad7a4659d`
  - 描述: boolean vHsm_Custom_IsSecureBootAllowAutostart_Callout(vHsm_SecureBootGroupIterType secureBootGroupIndex) is called.
If the function returns TRUE, the autostart will be performed. This can be used for e.g. checking the current reset vector.

**容器描述**:

Define a condition under which the autostart will be performed.
This way, the autostart of a group can be blocked if a condition is not met.

####### 7. vHsmCyclicCondition

**容器属性**:

- **UUID**: `5b43cd09-83c1-476e-a114-4c34b33a630e`
- **容器类型**: CHOICE-CONTAINER
- **容器名称**: `vHsmCyclicCondition`
- **多重性**: [0..1]
- **构建后可变**: false

**容器选择**:

- **vHsmCustomCalloutCyclic**
  - UUID: `065a1e5e-3cd4-4ab9-b8e0-1dffcca6adb5`
  - 描述: boolean vHsm_Custom_IsSecureBootAllowCyclic_Callout(vHsm_SecureBootGroupIterType secureBootGroupIndex, uint32 secureBootGroup) is called.
If the function returns TRUE, the cyclic verification will be performed. This can be used for disabling the cyclic verification during FBL and only enable it during APPL runtime.

**容器描述**:

Define a condition under which the autostart will be performed.
This way, the autostart of a group can be blocked if a condition is not met.

####### 8. vHsmVerificationMethod

**容器属性**:

- **UUID**: `0bf5a696-87f9-43e4-bed3-da26c2118384`
- **容器类型**: CHOICE-CONTAINER
- **容器名称**: `vHsmVerificationMethod`
- **多重性**: [1..1]
- **构建后可变**: false

**容器选择**:

- **vHsmCompareInternalTag**
  - UUID: `6fe03620-c0d0-48f7-ad35-8d74ef30db6a`
  - 描述: Compare a computed Tag (e.g. Cmac or Hash) against a Tag stored in the NvM.

**容器描述**:

Method which shall be used to validate the secure boot group

##### 13. vHsmCustomCallout

**容器属性**:

- **UUID**: `70f2bcd9-687f-4697-af41-008ad7a4659d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vHsmCustomCallout`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

boolean vHsm_Custom_IsSecureBootAllowAutostart_Callout(vHsm_SecureBootGroupIterType secureBootGroupIndex) is called.
If the function returns TRUE, the autostart will be performed. This can be used for e.g. checking the current reset vector.

##### 14. vHsmSecureBootSegment

**容器属性**:

- **UUID**: `35777e45-8dbf-4d3f-858c-dae853063b66`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vHsmSecureBootSegment`
- **多重性**: [0..infinite]
- **构建后可变**: false

**容器描述**:

A secure boot segment is a memory area which can be secured with a CMAC during secure boot.
A segment is part of a group and can be updated with secure software download or as part of a secure boot update.

###### 引用关系

此容器包含 **1** 个引用：

####### SYMBOLIC-NAME-REFERENCE 类型引用

######## 1. vHsmKeyRef

- **UUID**: `d8c1b9c8-4c75-4716-8db9-bf607b1a4eef`
- **引用名**: `vHsmKeyRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `CryIfKey`
- **完整路径**: `/AUTOSAR/EcucDefs/CryIf/CryIfKey`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: When storage method is set to VHSM_STORAGE_IN_CSM:
The referenced key is used to store the information of this segment
It will contain the address, size, tag and sanction.
The values will be updated to new values with the secure software download or secure boot update.

Key Ref is deprecated

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. vHsmSecureBootSegmentInitValues

**容器属性**:

- **UUID**: `4c7f1d37-8e2f-4c19-8ffe-d45bef25fefe`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vHsmSecureBootSegmentInitValues`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Init values for the segment. The values can be changed during runtime with secure boot update and secure software download.

######## 参数配置

此容器包含 **4** 个参数：

######### INTEGER 类型参数

########## 1. vHsmAddress

- **UUID**: `0c0de5a6-de65-4635-848a-066775ddcd7a`
- **参数名**: `vHsmAddress`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is the init value which will be stored during the startup.

Attention:
It will overwrite the init value configured for the key element!

########## 2. vHsmLength

- **UUID**: `a23e1739-3c6b-4182-b604-2e46a2426e13`
- **参数名**: `vHsmLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is the init value which will be stored during the startup.

Attention:
It will overwrite the init value configured for the key element!

######### ENUMERATION 类型参数

########## 1. vHsmSanction

- **UUID**: `f58d3edc-b54f-4260-ac6b-8b587f769adc`
- **参数名**: `vHsmSanction`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `SANCTION_RESET`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `SANCTION_NONE`
  - `SANCTION_RESET`
  - `SANCTION_HALT`
  - `SANCTION_CUSTOM`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The sanction which shall be performed

########## 2. vHsmSecureBootMode

- **UUID**: `81343282-e3ed-461b-b3d0-81d9a4eaff5b`
- **参数名**: `vHsmSecureBootMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `SEQUENTIAL`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `SEQUENTIAL`
  - `PARALLEL`
  - `NONE`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Processing Type of the segment.

##### 15. vHsmSecureBootSegmentInitValues

**容器属性**:

- **UUID**: `4c7f1d37-8e2f-4c19-8ffe-d45bef25fefe`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vHsmSecureBootSegmentInitValues`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Init values for the segment. The values can be changed during runtime with secure boot update and secure software download.

###### 参数配置

此容器包含 **4** 个参数：

####### INTEGER 类型参数

######## 1. vHsmAddress

- **UUID**: `0c0de5a6-de65-4635-848a-066775ddcd7a`
- **参数名**: `vHsmAddress`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is the init value which will be stored during the startup.

Attention:
It will overwrite the init value configured for the key element!

######## 2. vHsmLength

- **UUID**: `a23e1739-3c6b-4182-b604-2e46a2426e13`
- **参数名**: `vHsmLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is the init value which will be stored during the startup.

Attention:
It will overwrite the init value configured for the key element!

####### ENUMERATION 类型参数

######## 1. vHsmSanction

- **UUID**: `f58d3edc-b54f-4260-ac6b-8b587f769adc`
- **参数名**: `vHsmSanction`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `SANCTION_RESET`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `SANCTION_NONE`
  - `SANCTION_RESET`
  - `SANCTION_HALT`
  - `SANCTION_CUSTOM`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The sanction which shall be performed

######## 2. vHsmSecureBootMode

- **UUID**: `81343282-e3ed-461b-b3d0-81d9a4eaff5b`
- **参数名**: `vHsmSecureBootMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `SEQUENTIAL`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `SEQUENTIAL`
  - `PARALLEL`
  - `NONE`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Processing Type of the segment.

##### 16. vHsmCustomCalloutCyclic

**容器属性**:

- **UUID**: `065a1e5e-3cd4-4ab9-b8e0-1dffcca6adb5`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vHsmCustomCalloutCyclic`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

boolean vHsm_Custom_IsSecureBootAllowCyclic_Callout(vHsm_SecureBootGroupIterType secureBootGroupIndex, uint32 secureBootGroup) is called.
If the function returns TRUE, the cyclic verification will be performed. This can be used for disabling the cyclic verification during FBL and only enable it during APPL runtime.

##### 17. vHsmCompareInternalTag

**容器属性**:

- **UUID**: `6fe03620-c0d0-48f7-ad35-8d74ef30db6a`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vHsmCompareInternalTag`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Compare a computed Tag (e.g. Cmac or Hash) against a Tag stored in the NvM.

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. vHsmTagLength

- **UUID**: `8f773b00-5a2a-43e9-91a0-fc42f9b5d816`
- **参数名**: `vHsmTagLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `16`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Length of the Tag (e.g. CMAC or HASH)

Autofilled with information from CsmJobs

###### 引用关系

此容器包含 **1** 个引用：

####### SYMBOLIC-NAME-REFERENCE 类型引用

######## 1. vHsmVerificationJobRef

- **UUID**: `8f46e262-de8a-4181-8d80-6c7b9da07267`
- **引用名**: `vHsmVerificationJobRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `vHsmSecureBootVerificationJob`
- **完整路径**: `/MICROSAR/vHsm/vHsmSecureBoot/vHsmSecureBootVerificationJob`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a job tuple containing the references for sequential and parallel jobs

##### 18. vHsmSecureBootUpdate

**容器属性**:

- **UUID**: `759eef6d-a201-430c-8e3c-2d85b4194263`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vHsmSecureBootUpdate`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

This container configures the CSM jobs used for hash and signature generation. Secureboot update uses a signed segment list to update the secure boot segments of a group.

###### 引用关系

此容器包含 **2** 个引用：

####### SYMBOLIC-NAME-REFERENCE 类型引用

######## 1. vHsmCsmSignatureJobReference

- **UUID**: `53191050-f523-4adb-b3a9-6997cd3f16e7`
- **引用名**: `vHsmCsmSignatureJobReference`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `CsmJob`
- **完整路径**: `/AUTOSAR/EcucDefs/Csm/CsmJobs/CsmJob`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter references a CSM signature job used to calculate signatures for secure boot update.

######## 2. vHsmCsmHashJobReference

- **UUID**: `8a0dd456-9e80-4081-b910-3a0de851c7f5`
- **引用名**: `vHsmCsmHashJobReference`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `CsmJob`
- **完整路径**: `/AUTOSAR/EcucDefs/Csm/CsmJobs/CsmJob`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter references a CSM hash job used for secure secure boot update.

##### 19. vHsmSecureSoftwareDownload

**容器属性**:

- **UUID**: `db59c55e-0214-468c-a324-c4c58279172f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vHsmSecureSoftwareDownload`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

This container configured the key, channel und primitive used during secure software download which uses signed data to update a single secure boot segment.

Deprecated

###### 参数配置

此容器包含 **1** 个参数：

####### BOOLEAN 类型参数

######## 1. vHsmAllowAddressChange

- **UUID**: `0610360e-507b-4311-9937-85a836519c16`
- **参数名**: `vHsmAllowAddressChange`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Allow the change of the address during secure software download.
If disabled, this implies that a correct init value for the address is already set in each secure boot segment.

###### 引用关系

此容器包含 **1** 个引用：

####### SYMBOLIC-NAME-REFERENCE 类型引用

######## 1. vHsmCsmSignatureJobReference

- **UUID**: `0a3eab80-eeee-480d-bf16-f2c295febe18`
- **引用名**: `vHsmCsmSignatureJobReference`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `CsmJob`
- **完整路径**: `/AUTOSAR/EcucDefs/Csm/CsmJobs/CsmJob`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter references a CSM signature job used to calculate the signature for secure software download

##### 20. vHsmSecureBootVerificationJob

**容器属性**:

- **UUID**: `f69436fc-1371-4686-9f92-b5ab4cf405ad`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vHsmSecureBootVerificationJob`
- **多重性**: [1..infinite]
- **构建后可变**: false

**容器描述**:

Contains the jobs which will be used for verification.

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. vHsmSecureBootVerificationJobId

- **UUID**: `e4e86f4f-de35-454c-acbc-251448d0f260`
- **参数名**: `vHsmSecureBootVerificationJobId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Id of the verification job

###### 引用关系

此容器包含 **2** 个引用：

####### SYMBOLIC-NAME-REFERENCE 类型引用

######## 1. vHsmCsmJobSequentialRef

- **UUID**: `6ab801eb-55aa-4629-ae24-d7b147f3a7b0`
- **引用名**: `vHsmCsmJobSequentialRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `CsmJob`
- **完整路径**: `/AUTOSAR/EcucDefs/Csm/CsmJobs/CsmJob`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a CSM job which will be used for the sequential verification of the secure boot group.

######## 2. vHsmCsmJobParallelRef

- **UUID**: `6d887bca-e698-40c8-a398-866fb3bd48dc`
- **引用名**: `vHsmCsmJobParallelRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `CsmJob`
- **完整路径**: `/AUTOSAR/EcucDefs/Csm/CsmJobs/CsmJob`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a CSM job which will be used for the parallel verification of the secure boot group.

##### 21. vHsmLog

**容器属性**:

- **UUID**: `2cce0c23-cbf9-41f5-a2b5-52546e7629ae`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vHsmLog`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container for the events

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. vHsmLogEvent

**容器属性**:

- **UUID**: `784f28e0-5bbb-46a1-ae56-b52a4fe1e913`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vHsmLogEvent`
- **多重性**: [1..infinite]
- **构建后可变**: false

**容器描述**:

Container for the event log

######## 参数配置

此容器包含 **10** 个参数：

######### INTEGER 类型参数

########## 1. vHsmCounterSize

- **UUID**: `4a979839-22d5-460c-bd08-e8d6269918f7`
- **参数名**: `vHsmCounterSize`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `4`
- **取值范围**: [1..4]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Size of the counter which is incremented on each occurrence of the event.
Valid values are 1, 2 or 4 bytes.

########## 2. vHsmTimestampSize

- **UUID**: `f538231c-8460-4b93-ab5b-f26ddf82fdb5`
- **参数名**: `vHsmTimestampSize`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The content of the timestamp will be filled with the vHsm_Log_GetTimestamp_Callout(LogEventId)

########## 3. vHsmLogEventId

- **UUID**: `14fa4252-ea6e-481b-ba08-c6e59d6c7760`
- **参数名**: `vHsmLogEventId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Id of the event

########## 4. vHsmDataSize

- **UUID**: `b996c53e-9da7-44fc-af5d-b0ee178b0451`
- **参数名**: `vHsmDataSize`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Size of the event data

########## 5. vHsmMaxEntries

- **UUID**: `9198c07d-0797-4af6-abcd-fe1590427859`
- **参数名**: `vHsmMaxEntries`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Maximum number of entries before old entries are overwritten

########## 6. vHsmFillLevelThreshold

- **UUID**: `5ce739f1-2da8-49da-bf64-b7089374cecd`
- **参数名**: `vHsmFillLevelThreshold`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `1`
- **取值范围**: [1..100]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: If the fill level is reached the function vHsm_Log_FillLevelReachedCallout(vHsmLogEventId) is called.

If the fill level is set to 100 and the callout appears, all subsequent events will overwrite older entries from now on.

######### BOOLEAN 类型参数

########## 1. vHsmDiscardWhenFull

- **UUID**: `5f8923c8-5cb8-4979-aec7-cb053a9e40d6`
- **参数名**: `vHsmDiscardWhenFull`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Discard new elements when the log is full.
Otherwise the last element will be overwritten.

########## 2. vHsmEventCallout

- **UUID**: `cd743c73-42b3-4841-9106-32761cb45211`
- **参数名**: `vHsmEventCallout`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The function vHsm_Log_EventCallout(logEventId) is called when the event occurs

######### ENUMERATION 类型参数

########## 1. vHsmNvProcessing

- **UUID**: `6a03cd31-d04b-47fa-8faf-1b5853f7e438`
- **参数名**: `vHsmNvProcessing`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `NV_PROCESSING_IMMEDIATE`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `NV_PROCESSING_DEFERRED` (来源: Vector Informatik)
  - `NV_PROCESSING_IMMEDIATE` (来源: Vector Informatik)
  - `NV_PROCESSING_NONE` (来源: Vector Informatik)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This option defines how the log for this event will be persisted.

########## 2. vHsmExportStrategy

- **UUID**: `5f0df92a-cf07-4a65-b010-f8c9bbd1f748`
- **参数名**: `vHsmExportStrategy`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `EXPORT_ALL_FILO`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `EXPORT_LATEST` (来源: Vector Informatik)
  - `EXPORT_OLDEST` (来源: Vector Informatik)
  - `EXPORT_ALL_FIFO` (来源: Vector Informatik)
  - `EXPORT_NONE` (来源: Vector Informatik)
  - `EXPORT_OCCURRENCES` (来源: Vector Informatik)
  - `EXPORT_ALL_FILO` (来源: Vector Informatik)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Configure the way the log will be exported.

######## 引用关系

此容器包含 **1** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. vHsmNvBlockDescriptor

- **UUID**: `78318b31-b32c-4b6a-8ca2-aea7a00d6b1d`
- **引用名**: `vHsmNvBlockDescriptor`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `NvMBlockDescriptor`
- **完整路径**: `/AUTOSAR/EcucDefs/NvM/NvMBlockDescriptor`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a NvM block descriptor which will be used to persist the log of this event.

##### 22. vHsmLogEvent

**容器属性**:

- **UUID**: `784f28e0-5bbb-46a1-ae56-b52a4fe1e913`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vHsmLogEvent`
- **多重性**: [1..infinite]
- **构建后可变**: false

**容器描述**:

Container for the event log

###### 参数配置

此容器包含 **10** 个参数：

####### INTEGER 类型参数

######## 1. vHsmCounterSize

- **UUID**: `4a979839-22d5-460c-bd08-e8d6269918f7`
- **参数名**: `vHsmCounterSize`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `4`
- **取值范围**: [1..4]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Size of the counter which is incremented on each occurrence of the event.
Valid values are 1, 2 or 4 bytes.

######## 2. vHsmTimestampSize

- **UUID**: `f538231c-8460-4b93-ab5b-f26ddf82fdb5`
- **参数名**: `vHsmTimestampSize`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The content of the timestamp will be filled with the vHsm_Log_GetTimestamp_Callout(LogEventId)

######## 3. vHsmLogEventId

- **UUID**: `14fa4252-ea6e-481b-ba08-c6e59d6c7760`
- **参数名**: `vHsmLogEventId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Id of the event

######## 4. vHsmDataSize

- **UUID**: `b996c53e-9da7-44fc-af5d-b0ee178b0451`
- **参数名**: `vHsmDataSize`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Size of the event data

######## 5. vHsmMaxEntries

- **UUID**: `9198c07d-0797-4af6-abcd-fe1590427859`
- **参数名**: `vHsmMaxEntries`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Maximum number of entries before old entries are overwritten

######## 6. vHsmFillLevelThreshold

- **UUID**: `5ce739f1-2da8-49da-bf64-b7089374cecd`
- **参数名**: `vHsmFillLevelThreshold`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `1`
- **取值范围**: [1..100]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: If the fill level is reached the function vHsm_Log_FillLevelReachedCallout(vHsmLogEventId) is called.

If the fill level is set to 100 and the callout appears, all subsequent events will overwrite older entries from now on.

####### BOOLEAN 类型参数

######## 1. vHsmDiscardWhenFull

- **UUID**: `5f8923c8-5cb8-4979-aec7-cb053a9e40d6`
- **参数名**: `vHsmDiscardWhenFull`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Discard new elements when the log is full.
Otherwise the last element will be overwritten.

######## 2. vHsmEventCallout

- **UUID**: `cd743c73-42b3-4841-9106-32761cb45211`
- **参数名**: `vHsmEventCallout`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The function vHsm_Log_EventCallout(logEventId) is called when the event occurs

####### ENUMERATION 类型参数

######## 1. vHsmNvProcessing

- **UUID**: `6a03cd31-d04b-47fa-8faf-1b5853f7e438`
- **参数名**: `vHsmNvProcessing`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `NV_PROCESSING_IMMEDIATE`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `NV_PROCESSING_DEFERRED` (来源: Vector Informatik)
  - `NV_PROCESSING_IMMEDIATE` (来源: Vector Informatik)
  - `NV_PROCESSING_NONE` (来源: Vector Informatik)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This option defines how the log for this event will be persisted.

######## 2. vHsmExportStrategy

- **UUID**: `5f0df92a-cf07-4a65-b010-f8c9bbd1f748`
- **参数名**: `vHsmExportStrategy`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `EXPORT_ALL_FILO`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `EXPORT_LATEST` (来源: Vector Informatik)
  - `EXPORT_OLDEST` (来源: Vector Informatik)
  - `EXPORT_ALL_FIFO` (来源: Vector Informatik)
  - `EXPORT_NONE` (来源: Vector Informatik)
  - `EXPORT_OCCURRENCES` (来源: Vector Informatik)
  - `EXPORT_ALL_FILO` (来源: Vector Informatik)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Configure the way the log will be exported.

###### 引用关系

此容器包含 **1** 个引用：

####### SYMBOLIC-NAME-REFERENCE 类型引用

######## 1. vHsmNvBlockDescriptor

- **UUID**: `78318b31-b32c-4b6a-8ca2-aea7a00d6b1d`
- **引用名**: `vHsmNvBlockDescriptor`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `NvMBlockDescriptor`
- **完整路径**: `/AUTOSAR/EcucDefs/NvM/NvMBlockDescriptor`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a NvM block descriptor which will be used to persist the log of this event.

##### 23. vHsmScheduling

**容器属性**:

- **UUID**: `79493da4-ec3c-4b22-ac30-98ab9e8204ee`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vHsmScheduling`
- **多重性**: [1..1]
- **构建后可变**: false

**容器描述**:

Container to configure scheduling and parallel processing with the help of the OS or interrupts triggered to vHSM

###### 参数配置

此容器包含 **3** 个参数：

####### BOOLEAN 类型参数

######## 1. vHsmOsSupport

- **UUID**: `bb2f743a-599f-46ed-ae3f-c4bb65768a03`
- **参数名**: `vHsmOsSupport`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enable this option when OS is available and shall be used.
This way, different driver objects can be processed in different tasks with various priorities.

######## 2. vHsmInterruptMode

- **UUID**: `69133f66-0a32-4008-bd05-a5f79da56731`
- **参数名**: `vHsmInterruptMode`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Fetch the jobs only inside the ISR. If disabled, fetching will be performed in MainLoop.

This option needs to be disabled when a driver on application core is used (< R24) which does not trigger interrupts at each job request.
Do not use interrupt processed jobs if this option is disabled.

####### ENUMERATION 类型参数

######## 1. vHsmIsrForProcessing

- **UUID**: `436a8719-26a2-4e99-af21-865a50d4be6b`
- **参数名**: `vHsmIsrForProcessing`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `CATEGORY_1`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CATEGORY_1` (来源: Vector Informatik)
  - `CATEGORY_2` (来源: Vector Informatik)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Select the category of the ISR in which the channels to be processed directly in ISR will be executed.

CATEGORY_1:
- Fastest processing time
- No additional context switches
- Stack must be reserved manually

CATEGORY_2:
- Additional context switch necessary to switch from ISR1 to ISR2
- OS can be used to configure the stack size

###### 引用关系

此容器包含 **1** 个引用：

####### SYMBOLIC-NAME-REFERENCE 类型引用

######## 1. vHsmIsrProcessedChannel

- **UUID**: `ab85e6bd-ed2f-489c-90cd-0bd474922632`
- **引用名**: `vHsmIsrProcessedChannel`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..infinite]
- **目标**: `CryIfChannel`
- **完整路径**: `/MICROSAR/CryIf/CryIfChannel`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: A channel referenced here is directly executed from the interrupt context.

- Do not reference channels here when the driver does not trigger interrupts to the vHsm each time it sends a job request.
Info: Only drivers from R24 and above will trigger interrupts.
- vHsmInterruptMode must be enabled

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. vHsmSchedulableEntities

**容器属性**:

- **UUID**: `3f0f7e6a-7c8e-46b3-90ee-333e77a96f42`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vHsmSchedulableEntities`
- **多重性**: [1..infinite]
- **构建后可变**: false

**容器描述**:

Each schedulable entity will create a runnable which can be mapped to a task. All referenced channels will be then processed in this task, when a corresponding job is received from the IPC.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. vHsmSchedulableEntityId

- **UUID**: `a0591d81-58d8-448a-a0b3-7e1dd604c995`
- **参数名**: `vHsmSchedulableEntityId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Id of the task mapping

######## 引用关系

此容器包含 **1** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. vHsmChannelRef

- **UUID**: `07b966eb-165e-4dd3-a27d-1ae689ed4cca`
- **引用名**: `vHsmChannelRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..infinite]
- **目标**: `CryIfChannel`
- **完整路径**: `/MICROSAR/CryIf/CryIfChannel`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The referenced channels will be processed inside the task referenced in this task mapping container

##### 24. vHsmSchedulableEntities

**容器属性**:

- **UUID**: `3f0f7e6a-7c8e-46b3-90ee-333e77a96f42`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vHsmSchedulableEntities`
- **多重性**: [1..infinite]
- **构建后可变**: false

**容器描述**:

Each schedulable entity will create a runnable which can be mapped to a task. All referenced channels will be then processed in this task, when a corresponding job is received from the IPC.

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. vHsmSchedulableEntityId

- **UUID**: `a0591d81-58d8-448a-a0b3-7e1dd604c995`
- **参数名**: `vHsmSchedulableEntityId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Id of the task mapping

###### 引用关系

此容器包含 **1** 个引用：

####### SYMBOLIC-NAME-REFERENCE 类型引用

######## 1. vHsmChannelRef

- **UUID**: `07b966eb-165e-4dd3-a27d-1ae689ed4cca`
- **引用名**: `vHsmChannelRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..infinite]
- **目标**: `CryIfChannel`
- **完整路径**: `/MICROSAR/CryIf/CryIfChannel`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The referenced channels will be processed inside the task referenced in this task mapping container

##### 25. vHsmPublishedInformation

**容器属性**:

- **UUID**: `e2df46de-e987-4e6e-a8d0-2cb456e22854`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vHsmPublishedInformation`
- **多重性**: [1..1]
- **构建后可变**: false

**容器描述**:

vHsmPublishedInformation is used for additional published parameters and information.
This container is pre-configured and shall not be configured manually.

###### 配置容器

本模块包含 **4** 个配置容器：

####### 1. vHsmDerivativeInformation

**容器属性**:

- **UUID**: `a96a3932-9803-455b-a159-ffe7543aa5e8`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vHsmDerivativeInformation`
- **多重性**: [1..1]
- **构建后可变**: false

**容器描述**:

Contains all derivative specific information needed by the vHsm generator.

######## 配置容器

本模块包含 **3** 个配置容器：

######### 1. vHsmIpcHardwareUnit

**容器属性**:

- **UUID**: `11f229c0-7fee-46b0-82e6-10c582ad7f96`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vHsmIpcHardwareUnit`
- **多重性**: [1..32]
- **构建后可变**: false

**容器描述**:

A hardware ipc can be used by an IPC instance to share information about e.g IPC initialized state and HSM ready.

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. vHsmIpcHardwareUnitId

- **UUID**: `e0fb2daa-5680-4f83-8e46-c8ce6f703a4a`
- **参数名**: `vHsmIpcHardwareUnitId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Id of the hardware unit

########## 配置容器

本模块包含 **2** 个配置容器：

########### 1. Hsm

**容器属性**:

- **UUID**: `c8c4b9cd-23b1-4776-b68b-15bc3ec8a133`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `Hsm`
- **多重性**: [1..1]
- **构建后可变**: false

**容器描述**:

Contains the register addresses needed by the HSM

############ 参数配置

此容器包含 **3** 个参数：

############# INTEGER 类型参数

############## 1. vHsmHost2HsmAddress

- **UUID**: `243887e9-2bfc-4620-88d6-4663ea21abae`
- **参数名**: `vHsmHost2HsmAddress`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Address of the register which is used to communicate from Host to the HSM core

############## 2. vHsmHsm2HostAddress

- **UUID**: `9aaf4702-78ab-41a7-9d72-9fe763028acf`
- **参数名**: `vHsmHsm2HostAddress`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Address of the register which is used to communicate from HSM to the Host core

############## 3. vHsmResponseInterruptFlagSetAddress

- **UUID**: `85bcc19b-2ba3-4561-8663-5113d07dcab2`
- **参数名**: `vHsmResponseInterruptFlagSetAddress`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The address to use by vHsm for triggering an interrupt to the Host

########### 2. Host

**容器属性**:

- **UUID**: `afe99d29-3eb4-4a5c-b9e7-942fbee4c50f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `Host`
- **多重性**: [1..1]
- **构建后可变**: false

**容器描述**:

Contains the register addresses needed by the Host

############ 参数配置

此容器包含 **5** 个参数：

############# INTEGER 类型参数

############## 1. vHsmHost2HsmAddress

- **UUID**: `ac99964d-806a-415b-8293-996f00860ba9`
- **参数名**: `vHsmHost2HsmAddress`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Address of the register which is used to communicate from Host to the HSM core

############## 2. vHsmHsm2HostAddress

- **UUID**: `937ca682-d861-4700-81ec-7d164bf48364`
- **参数名**: `vHsmHsm2HostAddress`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Address of the register which is used to communicate from HSM to the Host core

############## 3. vHsmRequestInterruptFlagSetAddress

- **UUID**: `0a98ea29-02db-4916-9ed6-ec38e5e3dde5`
- **参数名**: `vHsmRequestInterruptFlagSetAddress`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The address used by Crypto Driver of the Host to trigger an interrupt to the vHsm

############## 4. vHsmResponseInterruptFlagClearAddress

- **UUID**: `304209cc-4f75-49eb-a09c-b792bfa864da`
- **参数名**: `vHsmResponseInterruptFlagClearAddress`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The address used in the Crypto Driver of the Host to clear the ISR flag of a response ISR from Hsm.

############## 5. vHsmResponseInterruptFlagClearValue

- **UUID**: `cd32b1be-41a2-4665-9ed7-b3e74a3e4e75`
- **参数名**: `vHsmResponseInterruptFlagClearValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `1`
- **取值范围**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Value which needs to be written by the Crypto Driver of the Host to the given address to clear the response flag.

######### 2. Hsm

**容器属性**:

- **UUID**: `c8c4b9cd-23b1-4776-b68b-15bc3ec8a133`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `Hsm`
- **多重性**: [1..1]
- **构建后可变**: false

**容器描述**:

Contains the register addresses needed by the HSM

########## 参数配置

此容器包含 **3** 个参数：

########### INTEGER 类型参数

############ 1. vHsmHost2HsmAddress

- **UUID**: `243887e9-2bfc-4620-88d6-4663ea21abae`
- **参数名**: `vHsmHost2HsmAddress`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Address of the register which is used to communicate from Host to the HSM core

############ 2. vHsmHsm2HostAddress

- **UUID**: `9aaf4702-78ab-41a7-9d72-9fe763028acf`
- **参数名**: `vHsmHsm2HostAddress`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Address of the register which is used to communicate from HSM to the Host core

############ 3. vHsmResponseInterruptFlagSetAddress

- **UUID**: `85bcc19b-2ba3-4561-8663-5113d07dcab2`
- **参数名**: `vHsmResponseInterruptFlagSetAddress`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The address to use by vHsm for triggering an interrupt to the Host

######### 3. Host

**容器属性**:

- **UUID**: `afe99d29-3eb4-4a5c-b9e7-942fbee4c50f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `Host`
- **多重性**: [1..1]
- **构建后可变**: false

**容器描述**:

Contains the register addresses needed by the Host

########## 参数配置

此容器包含 **5** 个参数：

########### INTEGER 类型参数

############ 1. vHsmHost2HsmAddress

- **UUID**: `ac99964d-806a-415b-8293-996f00860ba9`
- **参数名**: `vHsmHost2HsmAddress`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Address of the register which is used to communicate from Host to the HSM core

############ 2. vHsmHsm2HostAddress

- **UUID**: `937ca682-d861-4700-81ec-7d164bf48364`
- **参数名**: `vHsmHsm2HostAddress`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Address of the register which is used to communicate from HSM to the Host core

############ 3. vHsmRequestInterruptFlagSetAddress

- **UUID**: `0a98ea29-02db-4916-9ed6-ec38e5e3dde5`
- **参数名**: `vHsmRequestInterruptFlagSetAddress`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The address used by Crypto Driver of the Host to trigger an interrupt to the vHsm

############ 4. vHsmResponseInterruptFlagClearAddress

- **UUID**: `304209cc-4f75-49eb-a09c-b792bfa864da`
- **参数名**: `vHsmResponseInterruptFlagClearAddress`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The address used in the Crypto Driver of the Host to clear the ISR flag of a response ISR from Hsm.

############ 5. vHsmResponseInterruptFlagClearValue

- **UUID**: `cd32b1be-41a2-4665-9ed7-b3e74a3e4e75`
- **参数名**: `vHsmResponseInterruptFlagClearValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `1`
- **取值范围**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Value which needs to be written by the Crypto Driver of the Host to the given address to clear the response flag.

####### 2. vHsmIpcHardwareUnit

**容器属性**:

- **UUID**: `11f229c0-7fee-46b0-82e6-10c582ad7f96`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vHsmIpcHardwareUnit`
- **多重性**: [1..32]
- **构建后可变**: false

**容器描述**:

A hardware ipc can be used by an IPC instance to share information about e.g IPC initialized state and HSM ready.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. vHsmIpcHardwareUnitId

- **UUID**: `e0fb2daa-5680-4f83-8e46-c8ce6f703a4a`
- **参数名**: `vHsmIpcHardwareUnitId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Id of the hardware unit

######## 配置容器

本模块包含 **2** 个配置容器：

######### 1. Hsm

**容器属性**:

- **UUID**: `c8c4b9cd-23b1-4776-b68b-15bc3ec8a133`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `Hsm`
- **多重性**: [1..1]
- **构建后可变**: false

**容器描述**:

Contains the register addresses needed by the HSM

########## 参数配置

此容器包含 **3** 个参数：

########### INTEGER 类型参数

############ 1. vHsmHost2HsmAddress

- **UUID**: `243887e9-2bfc-4620-88d6-4663ea21abae`
- **参数名**: `vHsmHost2HsmAddress`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Address of the register which is used to communicate from Host to the HSM core

############ 2. vHsmHsm2HostAddress

- **UUID**: `9aaf4702-78ab-41a7-9d72-9fe763028acf`
- **参数名**: `vHsmHsm2HostAddress`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Address of the register which is used to communicate from HSM to the Host core

############ 3. vHsmResponseInterruptFlagSetAddress

- **UUID**: `85bcc19b-2ba3-4561-8663-5113d07dcab2`
- **参数名**: `vHsmResponseInterruptFlagSetAddress`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The address to use by vHsm for triggering an interrupt to the Host

######### 2. Host

**容器属性**:

- **UUID**: `afe99d29-3eb4-4a5c-b9e7-942fbee4c50f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `Host`
- **多重性**: [1..1]
- **构建后可变**: false

**容器描述**:

Contains the register addresses needed by the Host

########## 参数配置

此容器包含 **5** 个参数：

########### INTEGER 类型参数

############ 1. vHsmHost2HsmAddress

- **UUID**: `ac99964d-806a-415b-8293-996f00860ba9`
- **参数名**: `vHsmHost2HsmAddress`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Address of the register which is used to communicate from Host to the HSM core

############ 2. vHsmHsm2HostAddress

- **UUID**: `937ca682-d861-4700-81ec-7d164bf48364`
- **参数名**: `vHsmHsm2HostAddress`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Address of the register which is used to communicate from HSM to the Host core

############ 3. vHsmRequestInterruptFlagSetAddress

- **UUID**: `0a98ea29-02db-4916-9ed6-ec38e5e3dde5`
- **参数名**: `vHsmRequestInterruptFlagSetAddress`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The address used by Crypto Driver of the Host to trigger an interrupt to the vHsm

############ 4. vHsmResponseInterruptFlagClearAddress

- **UUID**: `304209cc-4f75-49eb-a09c-b792bfa864da`
- **参数名**: `vHsmResponseInterruptFlagClearAddress`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The address used in the Crypto Driver of the Host to clear the ISR flag of a response ISR from Hsm.

############ 5. vHsmResponseInterruptFlagClearValue

- **UUID**: `cd32b1be-41a2-4665-9ed7-b3e74a3e4e75`
- **参数名**: `vHsmResponseInterruptFlagClearValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `1`
- **取值范围**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Value which needs to be written by the Crypto Driver of the Host to the given address to clear the response flag.

####### 3. Hsm

**容器属性**:

- **UUID**: `c8c4b9cd-23b1-4776-b68b-15bc3ec8a133`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `Hsm`
- **多重性**: [1..1]
- **构建后可变**: false

**容器描述**:

Contains the register addresses needed by the HSM

######## 参数配置

此容器包含 **3** 个参数：

######### INTEGER 类型参数

########## 1. vHsmHost2HsmAddress

- **UUID**: `243887e9-2bfc-4620-88d6-4663ea21abae`
- **参数名**: `vHsmHost2HsmAddress`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Address of the register which is used to communicate from Host to the HSM core

########## 2. vHsmHsm2HostAddress

- **UUID**: `9aaf4702-78ab-41a7-9d72-9fe763028acf`
- **参数名**: `vHsmHsm2HostAddress`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Address of the register which is used to communicate from HSM to the Host core

########## 3. vHsmResponseInterruptFlagSetAddress

- **UUID**: `85bcc19b-2ba3-4561-8663-5113d07dcab2`
- **参数名**: `vHsmResponseInterruptFlagSetAddress`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The address to use by vHsm for triggering an interrupt to the Host

####### 4. Host

**容器属性**:

- **UUID**: `afe99d29-3eb4-4a5c-b9e7-942fbee4c50f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `Host`
- **多重性**: [1..1]
- **构建后可变**: false

**容器描述**:

Contains the register addresses needed by the Host

######## 参数配置

此容器包含 **5** 个参数：

######### INTEGER 类型参数

########## 1. vHsmHost2HsmAddress

- **UUID**: `ac99964d-806a-415b-8293-996f00860ba9`
- **参数名**: `vHsmHost2HsmAddress`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Address of the register which is used to communicate from Host to the HSM core

########## 2. vHsmHsm2HostAddress

- **UUID**: `937ca682-d861-4700-81ec-7d164bf48364`
- **参数名**: `vHsmHsm2HostAddress`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Address of the register which is used to communicate from HSM to the Host core

########## 3. vHsmRequestInterruptFlagSetAddress

- **UUID**: `0a98ea29-02db-4916-9ed6-ec38e5e3dde5`
- **参数名**: `vHsmRequestInterruptFlagSetAddress`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The address used by Crypto Driver of the Host to trigger an interrupt to the vHsm

########## 4. vHsmResponseInterruptFlagClearAddress

- **UUID**: `304209cc-4f75-49eb-a09c-b792bfa864da`
- **参数名**: `vHsmResponseInterruptFlagClearAddress`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The address used in the Crypto Driver of the Host to clear the ISR flag of a response ISR from Hsm.

########## 5. vHsmResponseInterruptFlagClearValue

- **UUID**: `cd32b1be-41a2-4665-9ed7-b3e74a3e4e75`
- **参数名**: `vHsmResponseInterruptFlagClearValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `1`
- **取值范围**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Value which needs to be written by the Crypto Driver of the Host to the given address to clear the response flag.

##### 26. vHsmDerivativeInformation

**容器属性**:

- **UUID**: `a96a3932-9803-455b-a159-ffe7543aa5e8`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vHsmDerivativeInformation`
- **多重性**: [1..1]
- **构建后可变**: false

**容器描述**:

Contains all derivative specific information needed by the vHsm generator.

###### 配置容器

本模块包含 **3** 个配置容器：

####### 1. vHsmIpcHardwareUnit

**容器属性**:

- **UUID**: `11f229c0-7fee-46b0-82e6-10c582ad7f96`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vHsmIpcHardwareUnit`
- **多重性**: [1..32]
- **构建后可变**: false

**容器描述**:

A hardware ipc can be used by an IPC instance to share information about e.g IPC initialized state and HSM ready.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. vHsmIpcHardwareUnitId

- **UUID**: `e0fb2daa-5680-4f83-8e46-c8ce6f703a4a`
- **参数名**: `vHsmIpcHardwareUnitId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Id of the hardware unit

######## 配置容器

本模块包含 **2** 个配置容器：

######### 1. Hsm

**容器属性**:

- **UUID**: `c8c4b9cd-23b1-4776-b68b-15bc3ec8a133`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `Hsm`
- **多重性**: [1..1]
- **构建后可变**: false

**容器描述**:

Contains the register addresses needed by the HSM

########## 参数配置

此容器包含 **3** 个参数：

########### INTEGER 类型参数

############ 1. vHsmHost2HsmAddress

- **UUID**: `243887e9-2bfc-4620-88d6-4663ea21abae`
- **参数名**: `vHsmHost2HsmAddress`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Address of the register which is used to communicate from Host to the HSM core

############ 2. vHsmHsm2HostAddress

- **UUID**: `9aaf4702-78ab-41a7-9d72-9fe763028acf`
- **参数名**: `vHsmHsm2HostAddress`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Address of the register which is used to communicate from HSM to the Host core

############ 3. vHsmResponseInterruptFlagSetAddress

- **UUID**: `85bcc19b-2ba3-4561-8663-5113d07dcab2`
- **参数名**: `vHsmResponseInterruptFlagSetAddress`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The address to use by vHsm for triggering an interrupt to the Host

######### 2. Host

**容器属性**:

- **UUID**: `afe99d29-3eb4-4a5c-b9e7-942fbee4c50f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `Host`
- **多重性**: [1..1]
- **构建后可变**: false

**容器描述**:

Contains the register addresses needed by the Host

########## 参数配置

此容器包含 **5** 个参数：

########### INTEGER 类型参数

############ 1. vHsmHost2HsmAddress

- **UUID**: `ac99964d-806a-415b-8293-996f00860ba9`
- **参数名**: `vHsmHost2HsmAddress`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Address of the register which is used to communicate from Host to the HSM core

############ 2. vHsmHsm2HostAddress

- **UUID**: `937ca682-d861-4700-81ec-7d164bf48364`
- **参数名**: `vHsmHsm2HostAddress`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Address of the register which is used to communicate from HSM to the Host core

############ 3. vHsmRequestInterruptFlagSetAddress

- **UUID**: `0a98ea29-02db-4916-9ed6-ec38e5e3dde5`
- **参数名**: `vHsmRequestInterruptFlagSetAddress`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The address used by Crypto Driver of the Host to trigger an interrupt to the vHsm

############ 4. vHsmResponseInterruptFlagClearAddress

- **UUID**: `304209cc-4f75-49eb-a09c-b792bfa864da`
- **参数名**: `vHsmResponseInterruptFlagClearAddress`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The address used in the Crypto Driver of the Host to clear the ISR flag of a response ISR from Hsm.

############ 5. vHsmResponseInterruptFlagClearValue

- **UUID**: `cd32b1be-41a2-4665-9ed7-b3e74a3e4e75`
- **参数名**: `vHsmResponseInterruptFlagClearValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `1`
- **取值范围**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Value which needs to be written by the Crypto Driver of the Host to the given address to clear the response flag.

####### 2. Hsm

**容器属性**:

- **UUID**: `c8c4b9cd-23b1-4776-b68b-15bc3ec8a133`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `Hsm`
- **多重性**: [1..1]
- **构建后可变**: false

**容器描述**:

Contains the register addresses needed by the HSM

######## 参数配置

此容器包含 **3** 个参数：

######### INTEGER 类型参数

########## 1. vHsmHost2HsmAddress

- **UUID**: `243887e9-2bfc-4620-88d6-4663ea21abae`
- **参数名**: `vHsmHost2HsmAddress`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Address of the register which is used to communicate from Host to the HSM core

########## 2. vHsmHsm2HostAddress

- **UUID**: `9aaf4702-78ab-41a7-9d72-9fe763028acf`
- **参数名**: `vHsmHsm2HostAddress`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Address of the register which is used to communicate from HSM to the Host core

########## 3. vHsmResponseInterruptFlagSetAddress

- **UUID**: `85bcc19b-2ba3-4561-8663-5113d07dcab2`
- **参数名**: `vHsmResponseInterruptFlagSetAddress`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The address to use by vHsm for triggering an interrupt to the Host

####### 3. Host

**容器属性**:

- **UUID**: `afe99d29-3eb4-4a5c-b9e7-942fbee4c50f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `Host`
- **多重性**: [1..1]
- **构建后可变**: false

**容器描述**:

Contains the register addresses needed by the Host

######## 参数配置

此容器包含 **5** 个参数：

######### INTEGER 类型参数

########## 1. vHsmHost2HsmAddress

- **UUID**: `ac99964d-806a-415b-8293-996f00860ba9`
- **参数名**: `vHsmHost2HsmAddress`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Address of the register which is used to communicate from Host to the HSM core

########## 2. vHsmHsm2HostAddress

- **UUID**: `937ca682-d861-4700-81ec-7d164bf48364`
- **参数名**: `vHsmHsm2HostAddress`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Address of the register which is used to communicate from HSM to the Host core

########## 3. vHsmRequestInterruptFlagSetAddress

- **UUID**: `0a98ea29-02db-4916-9ed6-ec38e5e3dde5`
- **参数名**: `vHsmRequestInterruptFlagSetAddress`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The address used by Crypto Driver of the Host to trigger an interrupt to the vHsm

########## 4. vHsmResponseInterruptFlagClearAddress

- **UUID**: `304209cc-4f75-49eb-a09c-b792bfa864da`
- **参数名**: `vHsmResponseInterruptFlagClearAddress`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The address used in the Crypto Driver of the Host to clear the ISR flag of a response ISR from Hsm.

########## 5. vHsmResponseInterruptFlagClearValue

- **UUID**: `cd32b1be-41a2-4665-9ed7-b3e74a3e4e75`
- **参数名**: `vHsmResponseInterruptFlagClearValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `1`
- **取值范围**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Value which needs to be written by the Crypto Driver of the Host to the given address to clear the response flag.

##### 27. vHsmIpcHardwareUnit

**容器属性**:

- **UUID**: `11f229c0-7fee-46b0-82e6-10c582ad7f96`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vHsmIpcHardwareUnit`
- **多重性**: [1..32]
- **构建后可变**: false

**容器描述**:

A hardware ipc can be used by an IPC instance to share information about e.g IPC initialized state and HSM ready.

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. vHsmIpcHardwareUnitId

- **UUID**: `e0fb2daa-5680-4f83-8e46-c8ce6f703a4a`
- **参数名**: `vHsmIpcHardwareUnitId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Id of the hardware unit

###### 配置容器

本模块包含 **2** 个配置容器：

####### 1. Hsm

**容器属性**:

- **UUID**: `c8c4b9cd-23b1-4776-b68b-15bc3ec8a133`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `Hsm`
- **多重性**: [1..1]
- **构建后可变**: false

**容器描述**:

Contains the register addresses needed by the HSM

######## 参数配置

此容器包含 **3** 个参数：

######### INTEGER 类型参数

########## 1. vHsmHost2HsmAddress

- **UUID**: `243887e9-2bfc-4620-88d6-4663ea21abae`
- **参数名**: `vHsmHost2HsmAddress`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Address of the register which is used to communicate from Host to the HSM core

########## 2. vHsmHsm2HostAddress

- **UUID**: `9aaf4702-78ab-41a7-9d72-9fe763028acf`
- **参数名**: `vHsmHsm2HostAddress`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Address of the register which is used to communicate from HSM to the Host core

########## 3. vHsmResponseInterruptFlagSetAddress

- **UUID**: `85bcc19b-2ba3-4561-8663-5113d07dcab2`
- **参数名**: `vHsmResponseInterruptFlagSetAddress`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The address to use by vHsm for triggering an interrupt to the Host

####### 2. Host

**容器属性**:

- **UUID**: `afe99d29-3eb4-4a5c-b9e7-942fbee4c50f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `Host`
- **多重性**: [1..1]
- **构建后可变**: false

**容器描述**:

Contains the register addresses needed by the Host

######## 参数配置

此容器包含 **5** 个参数：

######### INTEGER 类型参数

########## 1. vHsmHost2HsmAddress

- **UUID**: `ac99964d-806a-415b-8293-996f00860ba9`
- **参数名**: `vHsmHost2HsmAddress`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Address of the register which is used to communicate from Host to the HSM core

########## 2. vHsmHsm2HostAddress

- **UUID**: `937ca682-d861-4700-81ec-7d164bf48364`
- **参数名**: `vHsmHsm2HostAddress`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Address of the register which is used to communicate from HSM to the Host core

########## 3. vHsmRequestInterruptFlagSetAddress

- **UUID**: `0a98ea29-02db-4916-9ed6-ec38e5e3dde5`
- **参数名**: `vHsmRequestInterruptFlagSetAddress`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The address used by Crypto Driver of the Host to trigger an interrupt to the vHsm

########## 4. vHsmResponseInterruptFlagClearAddress

- **UUID**: `304209cc-4f75-49eb-a09c-b792bfa864da`
- **参数名**: `vHsmResponseInterruptFlagClearAddress`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The address used in the Crypto Driver of the Host to clear the ISR flag of a response ISR from Hsm.

########## 5. vHsmResponseInterruptFlagClearValue

- **UUID**: `cd32b1be-41a2-4665-9ed7-b3e74a3e4e75`
- **参数名**: `vHsmResponseInterruptFlagClearValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `1`
- **取值范围**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Value which needs to be written by the Crypto Driver of the Host to the given address to clear the response flag.

##### 28. Hsm

**容器属性**:

- **UUID**: `c8c4b9cd-23b1-4776-b68b-15bc3ec8a133`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `Hsm`
- **多重性**: [1..1]
- **构建后可变**: false

**容器描述**:

Contains the register addresses needed by the HSM

###### 参数配置

此容器包含 **3** 个参数：

####### INTEGER 类型参数

######## 1. vHsmHost2HsmAddress

- **UUID**: `243887e9-2bfc-4620-88d6-4663ea21abae`
- **参数名**: `vHsmHost2HsmAddress`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Address of the register which is used to communicate from Host to the HSM core

######## 2. vHsmHsm2HostAddress

- **UUID**: `9aaf4702-78ab-41a7-9d72-9fe763028acf`
- **参数名**: `vHsmHsm2HostAddress`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Address of the register which is used to communicate from HSM to the Host core

######## 3. vHsmResponseInterruptFlagSetAddress

- **UUID**: `85bcc19b-2ba3-4561-8663-5113d07dcab2`
- **参数名**: `vHsmResponseInterruptFlagSetAddress`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The address to use by vHsm for triggering an interrupt to the Host

##### 29. Host

**容器属性**:

- **UUID**: `afe99d29-3eb4-4a5c-b9e7-942fbee4c50f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `Host`
- **多重性**: [1..1]
- **构建后可变**: false

**容器描述**:

Contains the register addresses needed by the Host

###### 参数配置

此容器包含 **5** 个参数：

####### INTEGER 类型参数

######## 1. vHsmHost2HsmAddress

- **UUID**: `ac99964d-806a-415b-8293-996f00860ba9`
- **参数名**: `vHsmHost2HsmAddress`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Address of the register which is used to communicate from Host to the HSM core

######## 2. vHsmHsm2HostAddress

- **UUID**: `937ca682-d861-4700-81ec-7d164bf48364`
- **参数名**: `vHsmHsm2HostAddress`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Address of the register which is used to communicate from HSM to the Host core

######## 3. vHsmRequestInterruptFlagSetAddress

- **UUID**: `0a98ea29-02db-4916-9ed6-ec38e5e3dde5`
- **参数名**: `vHsmRequestInterruptFlagSetAddress`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The address used by Crypto Driver of the Host to trigger an interrupt to the vHsm

######## 4. vHsmResponseInterruptFlagClearAddress

- **UUID**: `304209cc-4f75-49eb-a09c-b792bfa864da`
- **参数名**: `vHsmResponseInterruptFlagClearAddress`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The address used in the Crypto Driver of the Host to clear the ISR flag of a response ISR from Hsm.

######## 5. vHsmResponseInterruptFlagClearValue

- **UUID**: `cd32b1be-41a2-4665-9ed7-b3e74a3e4e75`
- **参数名**: `vHsmResponseInterruptFlagClearValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `1`
- **取值范围**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Value which needs to be written by the Crypto Driver of the Host to the given address to clear the response flag.

##### 30. vHsmAutostartCondition

**容器属性**:

- **UUID**: `5892b0e1-1c3f-4ec1-bb8f-0af7e32dee09`
- **容器类型**: CHOICE-CONTAINER
- **容器名称**: `vHsmAutostartCondition`
- **多重性**: [0..1]
- **构建后可变**: false

**容器选择**:

- **vHsmCustomCallout**
  - UUID: `70f2bcd9-687f-4697-af41-008ad7a4659d`
  - 描述: boolean vHsm_Custom_IsSecureBootAllowAutostart_Callout(vHsm_SecureBootGroupIterType secureBootGroupIndex) is called.
If the function returns TRUE, the autostart will be performed. This can be used for e.g. checking the current reset vector.

**容器描述**:

Define a condition under which the autostart will be performed.
This way, the autostart of a group can be blocked if a condition is not met.

##### 31. vHsmCyclicCondition

**容器属性**:

- **UUID**: `5b43cd09-83c1-476e-a114-4c34b33a630e`
- **容器类型**: CHOICE-CONTAINER
- **容器名称**: `vHsmCyclicCondition`
- **多重性**: [0..1]
- **构建后可变**: false

**容器选择**:

- **vHsmCustomCalloutCyclic**
  - UUID: `065a1e5e-3cd4-4ab9-b8e0-1dffcca6adb5`
  - 描述: boolean vHsm_Custom_IsSecureBootAllowCyclic_Callout(vHsm_SecureBootGroupIterType secureBootGroupIndex, uint32 secureBootGroup) is called.
If the function returns TRUE, the cyclic verification will be performed. This can be used for disabling the cyclic verification during FBL and only enable it during APPL runtime.

**容器描述**:

Define a condition under which the autostart will be performed.
This way, the autostart of a group can be blocked if a condition is not met.

##### 32. vHsmVerificationMethod

**容器属性**:

- **UUID**: `0bf5a696-87f9-43e4-bed3-da26c2118384`
- **容器类型**: CHOICE-CONTAINER
- **容器名称**: `vHsmVerificationMethod`
- **多重性**: [1..1]
- **构建后可变**: false

**容器选择**:

- **vHsmCompareInternalTag**
  - UUID: `6fe03620-c0d0-48f7-ad35-8d74ef30db6a`
  - 描述: Compare a computed Tag (e.g. Cmac or Hash) against a Tag stored in the NvM.

**容器描述**:

Method which shall be used to validate the secure boot group

## 📦 包结构

此ARXML文件包含 **1** 个包：

### 1. MICROSAR

- **UUID**: `ff55d029-386d-43a2-b3c2-dfef4c7a5e36`
- **包名称**: `MICROSAR`
- **包含元素数量**: 5

#### 包含的元素

##### BSW-IMPLEMENTATION 类型元素

1. **vHsm_Impl**

##### ECUC-MODULE-DEF 类型元素

1. **vHsm**

##### ECUC-MODULE-CONFIGURATION-VALUES 类型元素

1. **vHsm_Pre**
2. **vHsm_Rec**
3. **vHsm_Rec_Class1**

## ⚡ 实现信息

此ARXML文件包含 **1** 个实现：

### 1. vHsm_Impl

- **UUID**: `256fa2ea-6057-46c5-bf74-59a9bee2133a`
- **实现名称**: `vHsm_Impl`
- **编程语言**: C
- **软件版本**: 5.00.01
- **供应商ID**: 30
- **AUTOSAR版本**: 4.03.00
- **代码生成器**: DaVinci Configurator

## ⚙️ 配置信息

此ARXML文件包含 **3** 个配置：

### 1. vHsm_Pre

- **UUID**: `8e3cc499-0ea0-4edf-811e-2be608f49ea9`
- **配置名称**: `vHsm_Pre`
- **定义引用**: `/MICROSAR/vHsm`

### 2. vHsm_Rec

- **UUID**: `d7d198ab-5261-4414-a19d-bd4daa62273a`
- **配置名称**: `vHsm_Rec`
- **定义引用**: `/MICROSAR/vHsm`

### 3. vHsm_Rec_Class1

- **UUID**: `9be18496-e119-47c6-9d1c-d72fbe722bf7`
- **配置名称**: `vHsm_Rec_Class1`
- **定义引用**: `/MICROSAR/vHsm`
