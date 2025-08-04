# Fee - 完整配置文档

*此文档由ARXML文件自动生成，采用层次化结构展示*

**生成时间**: 2025-06-16 14:48:12

## 📑 目录

- [📄 文件信息](#-文件信息)
- [🔧 模块定义](#-模块定义)
  - [Fee](#fee)
- [📦 包结构](#-包结构)

## 📄 文件信息

### Schema信息
- **Schema位置**: `http://autosar.org/schema/r4.0 AUTOSAR_4-2-2.xsd`
- **命名空间**: `http://autosar.org/schema/r4.0`

## 🔧 模块定义

### 1. Fee

#### 基本信息

- **UUID**: `ECUC:25e46613-7e63-4604-a81c-33867a9d91f7`
- **模块名称**: `Fee`
- **多重性**: [0..1]
- **支持的变体**:
  - VARIANT-POST-BUILD

#### 模块描述

Configuration of the Fee (Flash EEPROM Emulation) module.

#### 版本历史

共有 **1** 个版本记录：

##### 1. 版本 4.2.2

- **发布日期**: 2014-10-31
- **发布者**: AUTOSAR

*此版本无详细变更记录*

#### 配置容器

本模块包含 **6** 个配置容器：

##### 1. FeeBlockConfiguration

**容器属性**:

- **UUID**: `ECUC:3e3f6a41-1274-4d00-b94d-504e69110cfa`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FeeBlockConfiguration`
- **多重性**: [1..21792]

**容器描述**:

Configuration of block specific parameters for the Flash EEPROM Emulation module.

###### 参数配置

此容器包含 **7** 个参数：

####### INTEGER 类型参数

######## 1. FeeBlockNumber

- **UUID**: `ECUC:0a407883-2fc6-4823-a26e-ea079aa7e73f`
- **参数名**: `FeeBlockNumber`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `1`
- **取值范围**: [1..65534]
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **描述**: Block identifier (handle).

######## 2. FeeQsBlockInstances

- **UUID**: `ECUC:0a407881-2fc6-4823-a26e-ea079aa7e73f`
- **参数名**: `FeeQsBlockInstances`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..256]
- **作用域**: ECU
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: number of Block instances (handle).

######## 3. FeeQsBlockAddress

- **UUID**: `ECUC:0a407882-2fc6-4823-a26e-ea079aa7e73f`
- **参数名**: `FeeQsBlockAddress`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..1048575]
- **作用域**: ECU
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Block address in DFlash (handle).

######## 4. FeeBlockSize

- **UUID**: `ECUC:24bf18c3-8512-4334-8585-6c7937444d1d`
- **参数名**: `FeeBlockSize`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `1`
- **取值范围**: [1..65535]
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Size of a logical block in bytes.

######## 5. FeeNumberOfWriteCycles

- **UUID**: `ECUC:b55e41d9-f6b5-4613-937e-2b83fe37a654`
- **参数名**: `FeeNumberOfWriteCycles`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..16777215]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Number of write cycles required for this block.

####### BOOLEAN 类型参数

######## 1. FeeQuasiStaticManager

- **UUID**: `ECUC:b1116e04-53cd-44a7-8056-f43434aa82c8`
- **参数名**: `FeeQuasiStaticManager`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: ECU
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Indicates whether the Block configures is for NVM or Quasi static data Manager.

######## 2. FeeImmediateData

- **UUID**: `ECUC:b1116e94-53cd-44a7-8056-f43434aa82c8`
- **参数名**: `FeeImmediateData`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Marker for high priority data.

###### 引用关系

此容器包含 **1** 个引用：

####### SYMBOLIC-NAME-REFERENCE 类型引用

######## 1. FeeDeviceIndex

- **UUID**: `ECUC:f3bfa469-e131-4f58-bb89-ca7fc4548d25`
- **引用名**: `FeeDeviceIndex`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `FlsGeneral`
- **完整路径**: `/AUTOSAR/EcucDefs/Fls/FlsGeneral`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the device this block is stored in.

##### 2. FeeGeneral

**容器属性**:

- **UUID**: `ECUC:40da9e07-9e9a-4777-85e7-a111b37d8453`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FeeGeneral`
- **多重性**: [0..1]

**容器描述**:

Container for general parameters. These parameters are not specific to a block.

###### 参数配置

此容器包含 **13** 个参数：

####### INTEGER 类型参数

######## 1. FeeVirtualPageSize

- **UUID**: `ECUC:cfc06841-4637-4082-9f2e-57de66655c6f`
- **参数名**: `FeeVirtualPageSize`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `8`
- **取值范围**: [8..8]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: The size in bytes to which logical blocks shall be aligned.

####### BOOLEAN 类型参数

######## 1. FeeDevErrorDetect

- **UUID**: `ECUC:f262f806-4d29-4ef6-b4c1-6167282e1f21`
- **参数名**: `FeeDevErrorDetect`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `true`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Switches the Default Error Tracer (Det) detection and notification ON or OFF.

######## 2. FeeSafetyEnable

- **UUID**: `f262f806-4d29-4ef6-c5c1-6167282e1f21`
- **参数名**: `FeeSafetyEnable`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `true`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter enables the user to avail the functionality to detect and report the safety errors.

######## 3. FeeInitCheckApi

- **UUID**: `ECUC:f262f806-4d29-4ef6-b4c1-6333282e1f21`
- **参数名**: `FeeInitCheckApi`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter enables the user to avail the functionality to check if FEE initialisation is proper.                            true: Fee_17_InitCheck() API is enabled for use.                            false: Fee_17_InitCheck() API is disabled for use.

######## 4. FeePollingMode

- **UUID**: `ECUC:cbbd2e13-d937-4e0f-8546-6ea5cc3b7eeb`
- **参数名**: `FeePollingMode`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Pre-processor switch to enable and disable the polling mode for this module.

######## 5. FeeSetModeSupported

- **UUID**: `ECUC:f064e794-edd8-4288-b518-84c07839383d`
- **参数名**: `FeeSetModeSupported`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Compiler switch to enable/disable the 'SetMode' functionality of the FEE module.

######## 6. FeeVersionInfoApi

- **UUID**: `ECUC:e66783a5-0bb8-4060-83ed-985d387af3a5`
- **参数名**: `FeeVersionInfoApi`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Pre-processor switch to enable / disable the API to read out the modules version information.

####### FLOAT 类型参数

######## 1. FeeMainFunctionPeriod

- **UUID**: `ECUC:a5360d15-f12c-489d-a6c1-d1946bb47b2b`
- **参数名**: `FeeMainFunctionPeriod`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **默认值**: `0.01`
- **取值范围**: [0.001..1.0]
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: The period between successive calls to the main function in seconds.

####### ENUMERATION 类型参数

######## 1. FeeBlockTypeConfigured

- **UUID**: `87cc1eb8-09f0-401c-92ff-abb71996004d`
- **参数名**: `FeeBlockTypeConfigured`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `FEE_DOUBLE_SECTOR_DATA_ONLY`
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `FEE_DOUBLE_SECTOR_DATA_ONLY` (来源: INFINEON_AURIX2G)
  - `FEE_DOUBLE_SECTOR_AND_QUASI_STATIC_DATA` (来源: INFINEON_AURIX2G)
  - `FEE_QUASI_STATIC_DATA_ONLY` (来源: INFINEON_AURIX2G)
- **描述**: This parameter is used to configure the type of Blocks configured

####### FUNCTION-NAME 类型参数

######## 1. FeeNvmJobEndNotification

- **UUID**: `ECUC:3b4f73c8-354a-4d0e-86e6-0e2d07ba5590`
- **参数名**: `FeeNvmJobEndNotification`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **函数变体**:
  - 默认值: `NULL_PTR`
- **描述**: Mapped to the job end notification routine provided by the upper layer module (NvM_JobEndNotification).

######## 2. FeeNvmJobErrorNotification

- **UUID**: `ECUC:9a658f03-834b-4dd3-add7-58b968076e7d`
- **参数名**: `FeeNvmJobErrorNotification`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **函数变体**:
  - 默认值: `NULL_PTR`
- **描述**: Mapped to the job error notification routine provided by the upper layer module (NvM_JobErrorNotification).

######## 3. FeeQsJobEndNotification

- **UUID**: `ECUC:3b4f7399-354a-4d0e-86e6-0e2d07ba5590`
- **参数名**: `FeeQsJobEndNotification`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **函数变体**:
  - 默认值: `NULL_PTR`
- **描述**: Mapped to the job end notification routine provided by the upper layer module (Qs_JobEndNotification).

######## 4. FeeQsJobErrorNotification

- **UUID**: `ECUC:9a658f77-834b-4dd3-add7-58b968076e7d`
- **参数名**: `FeeQsJobErrorNotification`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **函数变体**:
  - 默认值: `NULL_PTR`
- **描述**: Mapped to the job error notification routine provided by the upper layer module (Qs_JobErrorNotification).

##### 3. FeePublishedInformation

**容器属性**:

- **UUID**: `ECUC:c99d74b3-e634-4c09-b512-87583d22c249`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FeePublishedInformation`
- **多重性**: [0..1]

**容器描述**:

Additional published parameters not covered by CommonPublishedInformation container.

###### 参数配置

此容器包含 **2** 个参数：

####### INTEGER 类型参数

######## 1. FeeBlockOverhead

- **UUID**: `ECUC:05f4fdfa-6b05-4960-973e-f62746494b3e`
- **参数名**: `FeeBlockOverhead`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `17`
- **取值范围**: [17..17]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Management overhead per logical block in bytes. The actual overhead per block is calculated as:     (i) If ((FeeBlockSize % 7) == 0): FeeBlockOverhead = ((FeeBlockSize / 7) * 8) + 16 - FeeBlockSize.     (ii)If ((FeeBlockSize % 7) != 0): FeeBlockOverhead = (((FeeBlockSize / 7) + 1) * 8) + 16 - FeeBlockSize.     Note: Integer arithmetic is used in the above calculation.

######## 2. FeePageOverhead

- **UUID**: `ECUC:ff042c2b-4ea3-4cc9-b210-6b4956da10da`
- **参数名**: `FeePageOverhead`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `1`
- **取值范围**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Block management overhead per page in bytes.     Note: This value is applicable only for the pages containing logical block data bytes (i.e., it is not applicable for the pages which contain only implementation specific management data).

##### 4. FeeIfxSpecificConfig

**容器属性**:

- **UUID**: `02f948d0-42c6-6e44-af25-89cd4d729345`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FeeIfxSpecificConfig`
- **多重性**: [0..1]

**容器描述**:

This container has IFX specific parameters required for the working of FEE

###### 参数配置

此容器包含 **16** 个参数：

####### INTEGER 类型参数

######## 1. FeeThresholdValue

- **UUID**: `fb7ccac3-78f4-49ae-92ec-8c3332ee39f2`
- **参数名**: `FeeThresholdValue`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `200`
- **取值范围**: [0..523240]
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter describes the threshold value (in bytes from the end of FEE sector) for triggering garbage collection/sector change.

######## 2. FeeMaxBlockCount

- **UUID**: `4a2531c3-429a-4527-8cd6-4fbe7bc6c4e1`
- **参数名**: `FeeMaxBlockCount`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `1`
- **取值范围**: [1..21792]
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This configuration parameter specifies the total number of blocks throughout all configurations; Note that the blocks which are shared across configurations are counted only once.     This parameter decides the cache table size at pre-compile time. The cache table holds the information of both configured and un-configured blocks.     Configuration of this parameter shall be carefully done. Higher value implies higher RAM area consumption for cache table. Lower value would result in loss of un-configured block(s) during GC (if FeeUnConfigBlkOverflowHandle is FEE_CONTINUE) or illegal state of FEE (if FeeUnConfigBlkOverflowHandle is FEE_STOP_AT_GC).      Example 1: Configuration sets having mutually exclusive blocks:     Configuration A: Number of blocks configured is 10.     Configuration B: Number of blocks configured is 25.     Then, FeeMaxBlockCount = 35.      Example 2: 5 blocks are shared/used by both Configuration A and Configuration B:     Configuration A: Number of blocks configured is 10.     Configuration B: Number of blocks configured is 25.     Then, FeeMaxBlockCount = 30 (i.e., shared blocks are counted only once).

####### BOOLEAN 类型参数

######## 1. FeeUseEraseSuspend

- **UUID**: `a4e7e16f-97ac-4db0-aeea-76aed97f9998`
- **参数名**: `FeeUseEraseSuspend`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter specifies the usage of the erase suspend feature provided by the DFLASH hardware.     If it is configured as TRUE, then the read/write requests from the user are serviced during the erase operation of the GC.     If it is configured as FALSE, then the user request is kept pending till the erase operation is completed.     Note: This parameter can be true only if FlsUseEraseSuspend is true.

######## 2. FeeGetCycleCountApi

- **UUID**: `8b82d416-42ea-4413-a123-a1f7b0c503b0`
- **参数名**: `FeeGetCycleCountApi`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Pre-processor switch to enable / disable the API to get the block cycle count and erase cycle count.

######## 3. FeeEraseAllEnable

- **UUID**: `20632ea9-0cad-4426-a0f4-e236e9c507eb`
- **参数名**: `FeeEraseAllEnable`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter allows the user to configure if the sectors should be erased when FEE reaches an illegal state.     TRUE: An erase all (DF_EEPROM Erase and Format) is performed. In such a case FEE shall resume back to normal state but previous data (if any) cannot be recovered.     FALSE: FEE settles in the illegal state and cannot continue normally. However, data is kept intact in DF_EEPROM and may be recovered.

######## 4. FeeGetPrevDataApi

- **UUID**: `20632ea9-0cad-4426-a0f4-e236e9c507ec`
- **参数名**: `FeeGetPrevDataApi`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter allows the user to read old copy (one instance old) of the required block.

######## 5. FeeCancelAllApi

- **UUID**: `20632ea9-0cad-4426-a0f4-e244e9c507ec`
- **参数名**: `FeeCancelAllApi`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter allows the user to enable cancelling ongoing operation to write high priority quasi static data.

######## 6. FeeVirginFlashIllegalState

- **UUID**: `20632ea9-0cad-4426-a0f4-e236e9c507ed`
- **参数名**: `FeeVirginFlashIllegalState`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter enables FEE to reach illegal state upon detection of virgin flash (DF_EEPROM).               TRUE: Upon detection of virgin flash (DF_EEPROM) - FEE reaches illegal state and calls the configured illegal state notification function.               FALSE: Upon detection of virgin flash (DF_EEPROM) - FEE programs the initial state pages and will be available for user requests.

####### STRING 类型参数

######## 1. FeeStateVarStructure

- **UUID**: `51030966-6cef-4965-98c6-09d2163e46ff`
- **参数名**: `FeeStateVarStructure`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **字符串变体**:
  - 默认值: `Fee_StateVar`
- **描述**: This parameter is the name of the structure, which would contain all the global variables of FEE. Using this user can allocate the space for the variables at his behest to avoid any possible linking problems.

####### ENUMERATION 类型参数

######## 1. FeeUnConfigBlock

- **UUID**: `87cc1e67-09f0-401c-92ff-abb71996004d`
- **参数名**: `FeeUnConfigBlock`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `FEE_UNCONFIG_BLOCK_IGNORE`
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `FEE_UNCONFIG_BLOCK_IGNORE` (来源: INFINEON_AURIX2G)
  - `FEE_UNCONFIG_BLOCK_KEEP` (来源: INFINEON_AURIX2G)
- **描述**: This parameter is used to configure if unconfigured blocks should be copied or not during GC operation

######## 2. FeeUnConfigBlkOverflowHandle

- **UUID**: `87cc1eb8-09f0-401c-92ff-abb71996004f`
- **参数名**: `FeeUnConfigBlkOverflowHandle`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `FEE_CONTINUE`
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `FEE_CONTINUE` (来源: INFINEON_AURIX2G)
  - `FEE_STOP_AT_GC` (来源: INFINEON_AURIX2G)
- **描述**: This parameter is used to configure the behavior of FEE upon detection of overflow of number of unconfigured blocks.     FEE_CONTINUE: Un-configured blocks which could not be accommodated in the cache table, will be lost after the GC. FEE will continue as expected for the currently active configuration.     FEE_STOP_AT_GC: During GC, FEE will enter a pseudo illegal state where only read is allowed but write is not allowed.

######## 3. FeeGcRestart

- **UUID**: `ccb0731b-222b-4118-8c48-f7046b8328c1`
- **参数名**: `FeeGcRestart`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `FEE_GC_RESTART_INIT`
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `FEE_GC_RESTART_INIT` (来源: INFINEON_AURIX2G)
  - `FEE_GC_RESTART_WRITE` (来源: INFINEON_AURIX2G)
- **描述**: This parameter is used to configure Garbage Collection restarting point.     FEE_GC_RESTART_INIT: (if GC was interrupted in previous run) Restart GC after FEE Initialization. Hence, internal activities like repairing state pages, building lookup table are done after Fee_Init is called.     FEE_GC_RESTART_WRITE: (if GC was interrupted in previous run) Restart GC when the first read/write/invalidate request is issued. Also, other internal activities like repairing state pages, building lookup table are done only after the first Read/write/invalidate request is issued

######## 4. FeeMaxBytesPerCycle

- **UUID**: `20632ea9-0acd-4426-4f0a-e236e9c507ec`
- **参数名**: `FeeMaxBytesPerCycle`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `FEE_MAX_BYTES_512`
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `FEE_MAX_BYTES_64` (来源: INFINEON_AURIX2G)
  - `FEE_MAX_BYTES_128` (来源: INFINEON_AURIX2G)
  - `FEE_MAX_BYTES_256` (来源: INFINEON_AURIX2G)
  - `FEE_MAX_BYTES_512` (来源: INFINEON_AURIX2G)
- **描述**: This parameter allows user to configure maximum number of bytes to be processed in one FEE MAIN Function cycle.                       The value is including the extra FEE overhead like header, consecutive page id etc

####### FUNCTION-NAME 类型参数

######## 1. FeeNvmIllegalStateNotification

- **UUID**: `6a28daf7-b174-4e5c-a3fd-e10e22a84bce`
- **参数名**: `FeeNvmIllegalStateNotification`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **函数变体**:
  - 默认值: `NULL_PTR`
- **描述**: This parameter is a pointer to a notification API which is called when Fee (NVM part) reaches an Illegal state. Illegal state here means that FEE is not able to proceed and user should do a power-on reset.                 Illegal notification can also be raised due to HW errors during FEE's internal activities like GC, Initialisation of GC

######## 2. FeeQsIllegalStateNotification

- **UUID**: `6a28daf7-b274-4e5c-a4fd-e10e22a64bce`
- **参数名**: `FeeQsIllegalStateNotification`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **函数变体**:
  - 默认值: `NULL_PTR`
- **描述**: This parameter is a pointer to a notification API which is called when Fee (QS part) reaches an Illegal state.                 Illegal notification is raised If QS area happens to be in virgin state and FeeVirginFlashIllegalState is not set

######## 3. FeeQsHardenErrorNotification

- **UUID**: `6a29daf7-b154-4e5c-a3fd-e10b22a84ace`
- **参数名**: `FeeQsHardenErrorNotification`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **函数变体**:
  - 默认值: `NULL_PTR`
- **描述**: This is a pointer to a notification API which is called by Fee when an error is encountered while performing hardening operation.

##### 5. FeeDemEventParameterRefs

**容器属性**:

- **UUID**: `ECUC:ff042c2b-4ea3-4cc9-b210-6b4956da10d9`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FeeDemEventParameterRefs`
- **多重性**: [0..1]

**容器描述**:

This container contains the references to DemEventParameter elements.

###### 引用关系

此容器包含 **10** 个引用：

####### SYMBOLIC-NAME-REFERENCE 类型引用

######## 1. FEE_E_GC_INIT

- **UUID**: `8dad21b3-69a0-49d9-8e35-ae145a074f38`
- **引用名**: `FEE_E_GC_INIT`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `DemEventParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemConfigSet/DemEventParameter`
- **来源**: INFINEON_AURIX2G
- **描述**: Reference to DemEventParameter for the production error FEE_E_GC_INIT.

######## 2. FEE_E_WRITE

- **UUID**: `8dad21b3-69a0-49d9-8e35-ae135a074f38`
- **引用名**: `FEE_E_WRITE`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `DemEventParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemConfigSet/DemEventParameter`
- **来源**: INFINEON_AURIX2G
- **描述**: Reference to DemEventParameter for the production error FEE_E_WRITE.

######## 3. FEE_E_READ

- **UUID**: `93cbda9d-85f7-46a2-a76f-98a6e718f5f4`
- **引用名**: `FEE_E_READ`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `DemEventParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemConfigSet/DemEventParameter`
- **来源**: INFINEON_AURIX2G
- **描述**: Reference to DemEventParameter for the production error FEE_E_READ.

######## 4. FEE_E_GC_READ

- **UUID**: `93cbda9d-85f7-46a2-a76f-98a6e718f5f5`
- **引用名**: `FEE_E_GC_READ`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `DemEventParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemConfigSet/DemEventParameter`
- **来源**: INFINEON_AURIX2G
- **描述**: Reference to DemEventParameter for the production error FEE_E_GC_READ.

######## 5. FEE_E_GC_WRITE

- **UUID**: `8dad21b3-69a0-49d9-8e35-ae145a174f38`
- **引用名**: `FEE_E_GC_WRITE`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `DemEventParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemConfigSet/DemEventParameter`
- **来源**: INFINEON_AURIX2G
- **描述**: Reference to DemEventParameter for the production error FEE_E_GC_WRITE.

######## 6. FEE_E_GC_ERASE

- **UUID**: `8dad21b3-69a0-49d9-8e35-ae145a064f38`
- **引用名**: `FEE_E_GC_ERASE`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `DemEventParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemConfigSet/DemEventParameter`
- **来源**: INFINEON_AURIX2G
- **描述**: Reference to DemEventParameter for the production error FEE_E_GC_ERASE.

######## 7. FEE_E_INVALIDATE

- **UUID**: `8dad21b3-69a0-49d9-8e35-ae145a074f98`
- **引用名**: `FEE_E_INVALIDATE`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `DemEventParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemConfigSet/DemEventParameter`
- **来源**: INFINEON_AURIX2G
- **描述**: Reference to DemEventParameter for the production error FEE_E_INVALIDATE.

######## 8. FEE_E_WRITE_CYCLES_EXHAUSTED

- **UUID**: `8dad21b3-69a0-49d9-8e35-ae145a074e38`
- **引用名**: `FEE_E_WRITE_CYCLES_EXHAUSTED`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `DemEventParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemConfigSet/DemEventParameter`
- **来源**: INFINEON_AURIX2G
- **描述**: Reference to DemEventParameter for the production error FEE_E_WRITE_CYCLES_EXHAUSTED.

######## 9. FEE_E_GC_TRIG

- **UUID**: `8dad21b3-69a0-49d9-8e35-ae145a074e9a`
- **引用名**: `FEE_E_GC_TRIG`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `DemEventParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemConfigSet/DemEventParameter`
- **来源**: INFINEON_AURIX2G
- **描述**: Reference to DemEventParameter for the production error FEE_E_GC_TRIG.

######## 10. FEE_E_UNCONFIG_BLK_EXCEEDED

- **UUID**: `8dad21b3-69a0-49d9-8e35-ae145a074e99`
- **引用名**: `FEE_E_UNCONFIG_BLK_EXCEEDED`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `DemEventParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemConfigSet/DemEventParameter`
- **来源**: INFINEON_AURIX2G
- **描述**: Reference to DemEventParameter for the production error FEE_E_UNCONFIG_BLK_EXCEEDED.

##### 6. CommonPublishedInformation

**容器属性**:

- **UUID**: `492f8482-3e2c-4bf1-b27f-01fd7a235788`
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

- **UUID**: `73f87c7f-e230-4178-bff0-ea2704aae656`
- **参数名**: `ArMinorVersion`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `2`
- **取值范围**: [0..255]
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Minor version number of AUTOSAR specification on which the appropriate implementation is based on.

######## 3. ArPatchVersion

- **UUID**: `2380135d-6778-417a-a34b-e100aad4dd54`
- **参数名**: `ArPatchVersion`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `2`
- **取值范围**: [0..255]
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Patch level version number of AUTOSAR specification on which the appropriate implementation is based on.

######## 4. SwMajorVersion

- **UUID**: `fca015e3-5f28-4cbe-8949-8fab87d86827`
- **参数名**: `SwMajorVersion`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `10`
- **取值范围**: [0..255]
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Major version number of the vendor specific implementation of the module. The numbering is vendor specific.

######## 5. SwMinorVersion

- **UUID**: `14ab81e0-3d80-43dc-8b92-2a7e5a542df9`
- **参数名**: `SwMinorVersion`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `40`
- **取值范围**: [0..255]
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Minor version number of the vendor specific implementation of the module. The numbering is vendor specific.

######## 6. SwPatchVersion

- **UUID**: `32e37bfd-18b6-41d1-9248-a81dae0fe4c5`
- **参数名**: `SwPatchVersion`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `1`
- **取值范围**: [0..255]
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Patch level version number of the vendor specific implementation of the module. The numbering is vendor specific.

######## 7. ModuleId

- **UUID**: `3b407478-6902-4f80-b7cf-f33b0854e638`
- **参数名**: `ModuleId`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `21`
- **取值范围**: [0..65535]
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Module ID of this module from Module List

######## 8. VendorId

- **UUID**: `7d650b2d-4adb-41f0-aa8e-5f0c416501d1`
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

- **UUID**: `3b407478-6902-4f40-a715-f32b0854e753`
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

1. **Fee**
